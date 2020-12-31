---
title: Dynamics 365 Finance + Operations (on-premises) での認証
description: このトピックでは、認証プロセスの仕組みに関する背景情報を提供して、問題が生じる場合に解決できるようにします。
author: faix
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d06d61ac5ff661ab2ab0af7fdb3141c54e34b321
ms.sourcegitcommit: 0297fd1f594c59a39014a592231ce5999b173848
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/02/2020
ms.locfileid: "4659850"
---
# <a name="authentication-in-dynamics-365-finance--operations-on-premises"></a><span data-ttu-id="64b13-103">Dynamics 365 Finance + Operations (on-premises) での認証</span><span class="sxs-lookup"><span data-stu-id="64b13-103">Authentication in Dynamics 365 Finance + Operations (on-premises)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="64b13-104">このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) の認証について説明します。</span><span class="sxs-lookup"><span data-stu-id="64b13-104">This topic explains authentication in Dynamics 365 Finance + Operations (on-premises).</span></span> <span data-ttu-id="64b13-105">このトピックでは、プロセスが機能する方法に関する背景情報も提供して、認証に関する問題が発生する場合に解決できるようにします。</span><span class="sxs-lookup"><span data-stu-id="64b13-105">This topic also provides background information about how the process works so that if you encounter issues with authentication you can work to resolve them.</span></span>

## <a name="the-url-for-active-directory-federation-services-ad-fs"></a><span data-ttu-id="64b13-106">フェデレーション サービス (AD FS) の URL</span><span class="sxs-lookup"><span data-stu-id="64b13-106">The URL for Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="64b13-107">認証プロセスの最初の部分は、Active Directory フェデレーションサービス (AD FS) の URL を提供することです。</span><span class="sxs-lookup"><span data-stu-id="64b13-107">The first part of the authentication process is to provide the URL for Active Directory Federation Services (AD FS).</span></span> <span data-ttu-id="64b13-108">この URL は次のようになります。`https://adfs.contoso.com/adfs/.well-known/openid-configuration`</span><span class="sxs-lookup"><span data-stu-id="64b13-108">This URL will be similar to: `https://adfs.contoso.com/adfs/.well-known/openid-configuration`</span></span> 

<span data-ttu-id="64b13-109">この URL は [Configure AD FS](./setup-deploy-on-premises-pu12.md#configureadfs) 内のデプロイの指示で検索できます。</span><span class="sxs-lookup"><span data-stu-id="64b13-109">You'll find this URL in the deployment instructions found in [Configure AD FS](./setup-deploy-on-premises-pu12.md#configureadfs).</span></span> <span data-ttu-id="64b13-110">デプロイ中に、URL を使用して、各 AOS インスタンスの AOS スタートアップ変数のさまざまなオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="64b13-110">During deployment, the URL is used to set various options in the AOS startup variables of each AOS instance.</span></span> <span data-ttu-id="64b13-111">これらのスタートアップ変数は、Service Fabric ディレクトリにある .XML 構成ファイルに配置されています。</span><span class="sxs-lookup"><span data-stu-id="64b13-111">These startup variables reside in an .XML config file located in a Service Fabric directory.</span></span> <span data-ttu-id="64b13-112">このディレクトリはマシンによって異なりますが、パスは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="64b13-112">This directory will vary from machine to machine, but the path should look similar to:</span></span>

<span data-ttu-id="64b13-113">C:\\ProgramData\\SF\\AOS_10\\Fabric\\work\\Applications\\AXSFType_App218\\AXSF.Package.1.0.xml</span><span class="sxs-lookup"><span data-stu-id="64b13-113">C:\\ProgramData\\SF\\AOS_10\\Fabric\\work\\Applications\\AXSFType_App218\\AXSF.Package.1.0.xml</span></span>

## <a name="xml-configuration-file"></a><span data-ttu-id="64b13-114">XML 構成ファイル</span><span class="sxs-lookup"><span data-stu-id="64b13-114">XML configuration file</span></span>
<span data-ttu-id="64b13-115">AXSF.Package.Current.xml と呼ばれるファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="64b13-115">There is a file called AXSF.Package.Current.xml.</span></span> <span data-ttu-id="64b13-116">このファイルは、Finance and Operations デプロイの AXSF.Package.1.0.xml のコピーです。</span><span class="sxs-lookup"><span data-stu-id="64b13-116">This file will be a copy of the AXSF.Package.1.0.xml in Finance and Operations deployments.</span></span> <span data-ttu-id="64b13-117">AXSF.Package.Current.xml ファイルは、現在実行中の AOS インスタンス (AxService.exe) を初期化するために使用された変数を表します。</span><span class="sxs-lookup"><span data-stu-id="64b13-117">The AXSF.Package.Current.xml file represents the variable that have been used to initialize the currently running AOS instance (AxService.exe).</span></span>

<span data-ttu-id="64b13-118">この構成ファイル (各 AOS マシン上にある) 内には、AD FS の Lifecycle Services (LCS) のデプロイ設定から設定されているセクションのいくつかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64b13-118">Within this configuration file (which is on each AOS machine), you'll find some sections that are set from the Lifecycle Services (LCS) deployment setting for AD FS.</span></span>

```xml
<Section Name="Aad">
    <Parameter Name="AADIssuerNameFormat" Value="http://ADFS.contoso.com/{0}/services/trust" />
    <Parameter Name="AADLoginWsfedEndpointFormat" Value="https://ADFS.contoso.com/{0}/wsfed" />
    <Parameter Name="AADMetadataLocationFormat" Value="https://ADFS.contoso.com/FederationMetadata/2007-06/FederationMetadata.xml" />
    <Parameter Name="AADTenantId" Value="adfs" />
    <Parameter Name="AADValidAudience" Value="https://ax.contoso.com/" />
    <Parameter Name="ACSServiceEndpoint" Value="https://accounts.accesscontrol.windows-ppe.net/tokens/OAuth/2" />
    <Parameter Name="ACSServicePrincipal" Value="00000001-0001-0000-c000-000000000000" />
    <Parameter Name="ADFSEndpoint" Value="https://ADFS.contoso.com/adfs" />
    <Parameter Name="ADFSIdentifier" Value="http://ADFS.contoso.com/adfs/services/trust" />
    <Parameter Name="FederationMetadataLocation" Value="https://ADFS.contoso.com/FederationMetadata/2007-06/FederationMetadata.xml" />
    <Parameter Name="Realm" Value="spn:00000015-0000-0000-c000-000000000000" />
    <Parameter Name="TenantDomainGUID" Value="adfs" />
    <Parameter Name="TrustedServiceAppIds" Value="913c6de4-2a4a-4a61-a9ce-945d2b2ce2e0" />
</Section>
```
<span data-ttu-id="64b13-119">また、次のセクションも確認できます。</span><span class="sxs-lookup"><span data-stu-id="64b13-119">You will also find the following sections.</span></span>

```xml
<Section Name="OfficeApps">
    <Parameter Name="AppInsightsKey" Value="" />
    <Parameter Name="AuthClientId" Value="d8230a86-015d-4c14-bcd6-c7fb65176b16" />
</Section>
<Section Name="OpenIDConnect">
    <Parameter Name="ClientID" Value="d8230a86-015d-4c14-bcd6-c7fb65176b16" />
    <Parameter Name="Metadata" Value="https://ADFS.contoso.com/adfs/.well-known/openid-configuration" />
</Section>
<Section Name="Provisioning">
    <Parameter Name="AdminIdentityProvider" Value="http://ADFS.contoso.com/adfs/services/trust" />
    <Parameter Name="AdminPrincipalName" Value="axserviceuser@contoso.com" />
</Section>
```

> [!NOTE]
> <span data-ttu-id="64b13-120">上記の設定は、Microsoft 365 の互換性で構成されているデプロイを示します。</span><span class="sxs-lookup"><span data-stu-id="64b13-120">The settings shown above represent a deployment configured with Microsoft 365 compatibility.</span></span> <span data-ttu-id="64b13-121">詳細については、[AD FS Microsoft 365 の互換性](./onprem-adfscompatibility.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64b13-121">For more information, see [AD FS Microsoft 365 compatibility](./onprem-adfscompatibility.md).</span></span>

## <a name="configuration-values-used-by-the-aos"></a><span data-ttu-id="64b13-122">AOS によって使用される構成値</span><span class="sxs-lookup"><span data-stu-id="64b13-122">Configuration values used by the AOS</span></span>
<span data-ttu-id="64b13-123">AOSでは、上記の構成値が使用され、ユーザーが要求をアプリケーション URL に送信するときに、認証されていない要求をリダイレクトする場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="64b13-123">The AOS uses the configuration values above to determine where to redirect an unauthenticated request when a user sends a request to the application URL.</span></span>

1. <span data-ttu-id="64b13-124">要求はブラウザーによりアプリケーション URL (`https://ax.contoso.com/namespaces/AXSF/`) に送信されます。</span><span class="sxs-lookup"><span data-stu-id="64b13-124">Request is sent by the browser to the application URL (`https://ax.contoso.com/namespaces/AXSF/`).</span></span>
2. <span data-ttu-id="64b13-125">要求はゲートウェイにより処理され、対話型のセッションを受け入れる AOS ノードに転送されます。</span><span class="sxs-lookup"><span data-stu-id="64b13-125">The request is processed by the Gateway and gets forwarded to an AOS node that accepts interactive sessions.</span></span>
3. <span data-ttu-id="64b13-126">要求は AOS サーバーに到達し、認証 Cookie を確認します。</span><span class="sxs-lookup"><span data-stu-id="64b13-126">The request reaches the AOS server and checks for the authentication cookies.</span></span>
4. <span data-ttu-id="64b13-127">認証は行われないので、AOS サーバーは AD FS で認証するようにユーザーにリダイレクト要求を返します。</span><span class="sxs-lookup"><span data-stu-id="64b13-127">No authentication is present so the AOS server returns a redirect request for the user to authenticate with AD FS.</span></span> <span data-ttu-id="64b13-128">この時点で、AOS はアフィニティ Cookie も設定して、ユーザー セッションをその AOS にバインドします。</span><span class="sxs-lookup"><span data-stu-id="64b13-128">At this point, the AOS also sets an affinity cookie to bind the user session to that AOS.</span></span>
5. <span data-ttu-id="64b13-129">ゲートウェイは応答を受信し、ブラウザーに転送して戻します。</span><span class="sxs-lookup"><span data-stu-id="64b13-129">The Gateway receives the response and forwards it back to the browser.</span></span>
6. <span data-ttu-id="64b13-130">ブラウザーはリダイレクト要求を受信し、ユーザーがサインインできるように AD FS 認証ページを表示します。</span><span class="sxs-lookup"><span data-stu-id="64b13-130">The browser receives the redirect request and displays the AD FS authentication page so the user signs in.</span></span>
7. <span data-ttu-id="64b13-131">AD FS に対して正常に認証されると、AD FS はユーザーをアプリケーション URL にリダイレクトし、認証 Cookie を提供します。</span><span class="sxs-lookup"><span data-stu-id="64b13-131">When successfully authenticated against AD FS, the AD FS then redirects the user back to the application URL and provides the authentication cookies.</span></span>
8. <span data-ttu-id="64b13-132">ゲートウェイはこの応答を受信し、アフィニティされた要求を適切な AOS ノードに転送します。</span><span class="sxs-lookup"><span data-stu-id="64b13-132">The Gateway receives this response and forwards the affinitized request to the appropriate AOS node.</span></span>
9. <span data-ttu-id="64b13-133">AOS は、提供されている認証情報を確認し、**UserInfo** テーブルに対して検証し、ユーザーが申請へのアクセスを許可されているか、およびどのアクセス許可が使用できるかを判断します。</span><span class="sxs-lookup"><span data-stu-id="64b13-133">The AOS checks the authentication information provided and checks against the **UserInfo** table to determine whether the user is allowed to access the application and which permissions are available.</span></span>
    
<span data-ttu-id="64b13-134">AOS 構成ファイルの値が正しくない場合、通常は環境を配置するときに AD FS エンドポイントに対して提供された値が正しくないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="64b13-134">If values in the AOS config file are incorrect, then that typically means the value provided for the AD FS endpoint when deploying the environment was incorrect.</span></span> <span data-ttu-id="64b13-135">最も簡単な方法は、正しい値を使用して、LCS から環境を削除して再配置することです。</span><span class="sxs-lookup"><span data-stu-id="64b13-135">The easiest thing is to delete and redeploy the environment from LCS with the correct value.</span></span> <span data-ttu-id="64b13-136">構成ファイルは手動で編集できますが、安全のために再配置をします。</span><span class="sxs-lookup"><span data-stu-id="64b13-136">It is possible to manually edit the configuration files, but to be safe, do a redeploy.</span></span> <span data-ttu-id="64b13-137">それ以外の場合は、各 AOS ノードで各サービス操作を実行した後に、手動で値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64b13-137">Otherwise you will need to manually change the values after each servicing operation on each AOS node.</span></span> <span data-ttu-id="64b13-138">構成ファイルを編集する場合は、AOS サービス (AxService.exe) を再起動して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64b13-138">If you do edit the config files, then you need to restart the AOS service (AxService.exe) for it to take effect.</span></span> <span data-ttu-id="64b13-139">Service Fabric Explorer から行うことができます (**ノード** にある AOS ノードを右クリックし、**再起動** を選択し、状態が緑に変更するまで少なくとも 1 分程度待機します)。</span><span class="sxs-lookup"><span data-stu-id="64b13-139">You can do that from the Service Fabric explorer (right-click the AOS node under **Nodes**, choose **Restart**, and then wait at least a minute for the status to change to green).</span></span> <span data-ttu-id="64b13-140">マシンを再起動することもできます。</span><span class="sxs-lookup"><span data-stu-id="64b13-140">You can also reboot the machine.</span></span>

<span data-ttu-id="64b13-141">アプリケーション URL にアクセスするときに 500 エラーが発生するのは、AD FS に対して無効な URL がある可能性があることを示しています。</span><span class="sxs-lookup"><span data-stu-id="64b13-141">Receiving a 500 error when accessing the application URL is an indication that there may be an invalid URL for AD FS.</span></span> <span data-ttu-id="64b13-142">これは、AOS の起動時にその URL を使用して AD FS サーバーから情報を取得するためです。</span><span class="sxs-lookup"><span data-stu-id="64b13-142">This is because on startup the AOS will use that URL to obtain information from the AD FS server.</span></span> <span data-ttu-id="64b13-143">URL が正確でないかまたはアクセスできない場合、AOS を起動することはできません。</span><span class="sxs-lookup"><span data-stu-id="64b13-143">If the URL is incorrect or inaccessible, the AOS will be unable to start.</span></span>

## <a name="ad-fs"></a><span data-ttu-id="64b13-144">AD FS</span><span class="sxs-lookup"><span data-stu-id="64b13-144">AD FS</span></span>
<span data-ttu-id="64b13-145">認証プロセスの 2 番目の部分は、AD FS 自体です。</span><span class="sxs-lookup"><span data-stu-id="64b13-145">The second part of the authentication process is AD FS itself.</span></span> <span data-ttu-id="64b13-146">AD FS サーバーで、AD FS Management を開き ((**コントロール パネル > システムとセキュリティ > 管理ツール**)、**アプリケーション グループ** に移動すると、**Microsoft Dynamics 365 for Operations オンプレミス** と呼ばれるグループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64b13-146">On the AD FS server if you open AD FS Management ((from **Control Panel > System and Security > Administrative Tools**), and go to **Application groups**, you'll find a group called **Microsoft Dynamics 365 for Operations On-premises**.</span></span> <span data-ttu-id="64b13-147">このグループ内では、Dynamics 365 アプリケーションの AD FS の設定が格納されます。</span><span class="sxs-lookup"><span data-stu-id="64b13-147">Within this group, the settings for AD FS for your Dynamics 365 application are stored.</span></span>

![AD FS 申請グループの設定](media/ADFS.png)

<span data-ttu-id="64b13-149">AD FS は、クライアント ID および URL を使用して、アクセスの要求を受け付けるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="64b13-149">AD FS uses the client ID and the URLs to determine whether the request for access should be honored.</span></span> <span data-ttu-id="64b13-150">上記のスクリーンショットのクライアント ID は、前述の OfficeApps および OpenIDConnect セクションで指定された ID と一致していることがわかります。</span><span class="sxs-lookup"><span data-stu-id="64b13-150">You will notice that the client ID from the screenshot above matches the IDs specified in the OfficeApps and OpenIDConnect sections from earlier.</span></span> <span data-ttu-id="64b13-151">クライアント ID とリダイレクト URL の両方が AOS が要求しているものと一致しない場合、AD FS は認証の要求を拒否します。</span><span class="sxs-lookup"><span data-stu-id="64b13-151">If both the client ID and the redirect URL don't match what the AOS is requesting, then AD FS will deny the request to authenticate.</span></span> <span data-ttu-id="64b13-152">このような場合は、AD FS サーバーのイベントのログオンにエラーが見つかります。</span><span class="sxs-lookup"><span data-stu-id="64b13-152">If that happens, you'll find an error in the event log on the AD FS server.</span></span> <span data-ttu-id="64b13-153">**アプリケーションとサービス ログ > AD FS > 管理者** に、AD FS の特別なイベント ログがあります。</span><span class="sxs-lookup"><span data-stu-id="64b13-153">There's a special event log for AD FS under **Application and Services logs > AD FS > Admin**.</span></span>

![AD FS のイベント ログ エラー](media/ADFSredirectwrong.png)

<span data-ttu-id="64b13-155">AD FS 申請グループの設定に誤りがある場合、イベント ログに探していた値を説明するエラーが見つかる可能性が高いので、何が正しく設定されていないのかを判断することができます。</span><span class="sxs-lookup"><span data-stu-id="64b13-155">If any of the AD FS application group setup is incorrect, you're likely see an error in the event log that explains the value it was looking for, so you can determine what is set incorrectly.</span></span>
