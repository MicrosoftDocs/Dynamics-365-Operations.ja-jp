---
title: オンプレミス配置の倉庫管理アプリを構成
description: このトピックでは、オンプレミス展開でのウェアハウス アプリの前提条件について説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 24861
ms.assetid: 63e43066-76c7-400b-be7d-d14785e7985d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 820a557dc77f259c9503f02c7eac9eadfa8f9512
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369023"
---
# <a name="configure-the-warehousing-app-for-on-premises-deployments"></a><span data-ttu-id="ee626-103">オンプレミス配置の倉庫管理アプリを構成</span><span class="sxs-lookup"><span data-stu-id="ee626-103">Configure the Warehousing app for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee626-104">このトピックでは、オンプレミス配置の Microsoft Dynamics 365 for Finance and Operations - Warehousing の構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee626-104">This topic describes how to configure Microsoft Dynamics 365 for Finance and Operations - Warehousing for on-premises deployments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ee626-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="ee626-105">Prerequisites</span></span>
<span data-ttu-id="ee626-106">倉庫管理アプリは Android および Windows オペレーティング システムで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee626-106">The Warehousing app is available on Android and Windows operating systems.</span></span> <span data-ttu-id="ee626-107">オンプレミスの展開にこのアプリを使用するには、少なくともバージョン 1.1.1.0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee626-107">To use the app for on-premises deployments, at a minimum, it must be version 1.1.1.0.</span></span> <span data-ttu-id="ee626-108">Microsoft Dynamics 365 for Finance and Operations が次のサポートされているバージョンの 1 つである必要もあります。</span><span class="sxs-lookup"><span data-stu-id="ee626-108">You must also have one of the following supported versions of Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ee626-109">ハードウェアおよびソフトウェア環境で構成がサポートされているかどうかを評価するには、次の表の情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee626-109">Use the information in the following table to evaluate if your hardware and software environment supports the configuration.</span></span>

| <span data-ttu-id="ee626-110">プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="ee626-110">Platform</span></span>               | <span data-ttu-id="ee626-111">バージョン</span><span class="sxs-lookup"><span data-stu-id="ee626-111">Version</span></span>                                                                            |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee626-112">Android</span><span class="sxs-lookup"><span data-stu-id="ee626-112">Android</span></span>                | <span data-ttu-id="ee626-113">4.4 以上</span><span class="sxs-lookup"><span data-stu-id="ee626-113">4.4 and up</span></span>                                                                         |
| <span data-ttu-id="ee626-114">Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="ee626-114">Windows (UWP)</span></span>          | <span data-ttu-id="ee626-115">Windows 10 (すべてのバージョン)</span><span class="sxs-lookup"><span data-stu-id="ee626-115">Windows 10 (all versions)</span></span>                                                          |
| <span data-ttu-id="ee626-116">アプリのバージョン</span><span class="sxs-lookup"><span data-stu-id="ee626-116">App version</span></span>            | <span data-ttu-id="ee626-117">1.1.1.0 以上</span><span class="sxs-lookup"><span data-stu-id="ee626-117">1.1.1.0 and above</span></span>                                                                  |
| <span data-ttu-id="ee626-118">Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ee626-118">Microsoft Dynamics 365</span></span> | <span data-ttu-id="ee626-119">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 11 (オンプレミス)</span><span class="sxs-lookup"><span data-stu-id="ee626-119">Dynamics 365 for Finance and Operations platform update 11 (on-premises)</span></span> |

<span data-ttu-id="ee626-120">アプリでオンプレミス リソースにアクセスできるようにするには、AOS および Active Directory フェデレーション サービス（AD FS）の DNS レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee626-120">To be able to reach your on-premises resources with the app, you will need to create DNS records for your AOS and for Active Directory Federation Services (AD FS).</span></span> <span data-ttu-id="ee626-121">ガイダンスについては、[DNS ゾーンの作成とレコードの追加](setup-deploy-on-premises-pu12.md#setup) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee626-121">For guidance, see [Create DNS zones, and add a record](setup-deploy-on-premises-pu12.md#setup).</span></span>

## <a name="create-an-application-entry-in-ad-fs"></a><span data-ttu-id="ee626-122">AD FS でアプリケーション エントリを作成する</span><span class="sxs-lookup"><span data-stu-id="ee626-122">Create an application entry in AD FS</span></span>
<span data-ttu-id="ee626-123">AD FS およびFinance and Operations 間で認証を正常に交換するために、AD FS アプリケーション グループの下の AD FS にアプリケーション エントリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee626-123">For a successful authentication exchange between AD FS and Finance and Operations, an application entry must be registered in AD FS under an AD FS application group.</span></span> <span data-ttu-id="ee626-124">このアプリケーション エントリを作成するには、AD FS がインストールされているマシンで次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ee626-124">To create this application entry, run the following Windows PowerShell commands on a machine where the AD FS is installed.</span></span> <span data-ttu-id="ee626-125">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="ee626-125">The user account must have enough permissions to administer AD FS.</span></span>

1.  <span data-ttu-id="ee626-126">アプリケーションのエントリを作成する Windows PowerShell コンソールに、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="ee626-126">Enter the following command in the Windows PowerShell console to create the application entry</span></span>  
    
        Add-AdfsClient -Name 'Dynamics 365 for Finance and Operations - Warehousing' -ClientId ([guid]::NewGuid()) -ClientType Confidential -GenerateClientSecret -RedirectUri '\<Resource URL\>' -ADUserPrincipalName '\<Admin user\>' 

    - <span data-ttu-id="ee626-127">\<リソース URL\> は、たとえば `https://ax.d365ffo.onprem.contoso.com` などです (`https://ax.d365ffo.onprem.contoso.com` は、Finance and Operations にアクセスするための URL です)。</span><span class="sxs-lookup"><span data-stu-id="ee626-127">The \<Resource URL\> can, for example, be `https://ax.d365ffo.onprem.contoso.com` (where `https://ax.d365ffo.onprem.contoso.com` is the URL to access Finance and Operations).</span></span>
    - <span data-ttu-id="ee626-128">\<管理者ユーザー\> は、AD FS コンピューターへの管理者のアクセス権を持つ任意のユーザーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="ee626-128">The \<Admin user\> can be any user with admin access to the AD FS machine.</span></span>

2.  <span data-ttu-id="ee626-129">受信した値を保存します。</span><span class="sxs-lookup"><span data-stu-id="ee626-129">Save the values that you received.</span></span>

3.  <span data-ttu-id="ee626-130">アプリケーションへのアクセス許可を付与するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ee626-130">Run the following command to grant permission to the application.</span></span>  
    
        Grant-AdfsApplicationPermission -ClientRoleIdentifier '\<Client ID received in previous steps\>' -ServerRoleIdentifier '\<Resource URL\>' -ScopeNames 'openid'

## <a name="create-and-configure-a-user-account"></a><span data-ttu-id="ee626-131">ユーザー アカウントの作成およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ee626-131">Create and configure a user account</span></span>

<span data-ttu-id="ee626-132">Dynamics 365 for Finance and Operations で AD FS アプリケーションを使用できるようにするには、倉庫管理アプリのユーザーと同じユーザー資格情報を使用して Microsoft Dynamics 365 でユーザー アカウントを作成する必要があります:</span><span class="sxs-lookup"><span data-stu-id="ee626-132">To enable Dynamics 365 for Finance and Operations to use your AD FS application, you must create a user account in Microsoft Dynamics 365 with the same user credentials as the user of the Warehousing app:</span></span>

1.  <span data-ttu-id="ee626-133">Finance and Operations でユーザーを作成し、倉庫管理モバイル デバイス ユーザー ロールをユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ee626-133">Create a user in Finance and Operations and assign the Warehousing mobile device user role to the user.</span></span>

    <span data-ttu-id="ee626-134">a.</span><span class="sxs-lookup"><span data-stu-id="ee626-134">a.</span></span>  <span data-ttu-id="ee626-135">**システム管理** \> **共通** \> **ユーザー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ee626-135">Go to **System administration** \> **Common** \> **Users**.</span></span>
    
    <span data-ttu-id="ee626-136">b.</span><span class="sxs-lookup"><span data-stu-id="ee626-136">b.</span></span>  <span data-ttu-id="ee626-137">新規ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee626-137">Create a new user.</span></span>
    
    <span data-ttu-id="ee626-138">c.</span><span class="sxs-lookup"><span data-stu-id="ee626-138">c.</span></span>  <span data-ttu-id="ee626-139">例のスクリーンショットに示されているように、倉庫モバイル デバイス ユーザー ロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ee626-139">Assign the warehouse mobile device user role, as shown in the example screenshot.</span></span>

    ![ユーザーの作成およびコンフィギュレーション](media/wmapp-users.png)

2.  <span data-ttu-id="ee626-141">AD FS アプリケーションと倉庫保管アプリ ユーザーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ee626-141">Associate your AD FS application with the Warehousing app user.</span></span>

    <span data-ttu-id="ee626-142">a.</span><span class="sxs-lookup"><span data-stu-id="ee626-142">a.</span></span>  <span data-ttu-id="ee626-143">Finance and Operations で、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee626-143">In Finance and Operations, click **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span>
    
    <span data-ttu-id="ee626-144">b.</span><span class="sxs-lookup"><span data-stu-id="ee626-144">b.</span></span>  <span data-ttu-id="ee626-145">新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee626-145">Create a new line.</span></span>
    
    <span data-ttu-id="ee626-146">c.</span><span class="sxs-lookup"><span data-stu-id="ee626-146">c.</span></span>  <span data-ttu-id="ee626-147">AD FS でアプリケーション エントリを作成したときに取得したクライアント ID を入力します (「AD FS でのアプリケーション エントリの作成」の手順 2)。</span><span class="sxs-lookup"><span data-stu-id="ee626-147">Enter the client ID that you obtained when you created an application entry in AD FS (step 2 in "Create an application entry in AD FS").</span></span> <span data-ttu-id="ee626-148">名前を入力し、倉庫管理アプリ ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee626-148">Enter a name, and select the Warehousing app user.</span></span>

    ![<span data-ttu-id="ee626-149">Azure Active Drectory アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ee626-149">Azure Active Drectory applications</span></span> ](media/azure-active-directory.png)

## <a name="certificates"></a><span data-ttu-id="ee626-150">証明書</span><span class="sxs-lookup"><span data-stu-id="ee626-150">Certificates</span></span> 

<span data-ttu-id="ee626-151">アプリがインストールされているデバイスに、リソースにアクセスする適切な証明書があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ee626-151">Make sure that the devices with the app installed have the correct certificates to access the resources.</span></span> <span data-ttu-id="ee626-152">自己署名証明書を使用している場合、コンピューター アカウント/ユーザー アカウントの信頼されているルートに star(AX) と AD FS をインポートすることで、これらが各デバイスにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee626-152">If you are using self-signed certificates, these will need to be installed on each device by importing star(AX) and AD FS to the trusted route of the computer account/user account.</span></span> <span data-ttu-id="ee626-153">詳細については、[自己署名証明書の作成およびエクスポート](https://technet.microsoft.com/en-us/library/ff710475(v=ws.10).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee626-153">For more information, see [Create and export a self-signed certificate](https://technet.microsoft.com/en-us/library/ff710475(v=ws.10).aspx).</span></span>

## <a name="configure-the-application"></a><span data-ttu-id="ee626-154">アプリケーションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ee626-154">Configure the application</span></span>

<span data-ttu-id="ee626-155">AD FS アプリケーションを使用して Finance and Operations サーバーに接続するには、デバイス上で倉庫管理アプリを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee626-155">You must configure the Warehousing app on the device to connect to the Finance and Operations server through the AD FS application.</span></span>

1.  <span data-ttu-id="ee626-156">アプリで**接続設定**を開きます。</span><span class="sxs-lookup"><span data-stu-id="ee626-156">In the app, open **Connection settings**.</span></span>
2.  <span data-ttu-id="ee626-157">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee626-157">Enter the following information:</span></span>

    <span data-ttu-id="ee626-158">a.</span><span class="sxs-lookup"><span data-stu-id="ee626-158">a.</span></span>  <span data-ttu-id="ee626-159">**Active Directory クライアント ID** - AD FS でアプリケーション エントリを作成したときに取得したクライアント ID (「AD FS でのアプリケーション エントリの作成」の手順 2)。</span><span class="sxs-lookup"><span data-stu-id="ee626-159">**Active Directory Client ID** - The client ID that you obtained when  you created an application entry in AD FS (step 2 in "Create an application entry in AD FS").</span></span>

    <span data-ttu-id="ee626-160">b.</span><span class="sxs-lookup"><span data-stu-id="ee626-160">b.</span></span>  <span data-ttu-id="ee626-161">**Active Directory クライアント シークレット** - AD FS でアプリケーション エントリを作成したときに取得したクライアント シークレット。</span><span class="sxs-lookup"><span data-stu-id="ee626-161">**Active Directory Client Secret** - The client secret obtained when you created an application entry in AD FS.</span></span>

    <span data-ttu-id="ee626-162">c.</span><span class="sxs-lookup"><span data-stu-id="ee626-162">c.</span></span>  <span data-ttu-id="ee626-163">**Active Directory リソース** - Finance and Operations AOS の DNS URL。</span><span class="sxs-lookup"><span data-stu-id="ee626-163">**Active Directory Resource** - The DNS URL for Finance and Operations AOS.</span></span> <span data-ttu-id="ee626-164">URL に「/namespaces/AXSF」を追加します。</span><span class="sxs-lookup"><span data-stu-id="ee626-164">Append the URL with '/namespaces/AXSF'.</span></span> 
        <span data-ttu-id="ee626-165">例: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF`</span><span class="sxs-lookup"><span data-stu-id="ee626-165">For example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF`</span></span>

    <span data-ttu-id="ee626-166">d.</span><span class="sxs-lookup"><span data-stu-id="ee626-166">d.</span></span>  <span data-ttu-id="ee626-167">**Active Directory テナント** - Finance and Operations AD FS マシンの DNS URL。</span><span class="sxs-lookup"><span data-stu-id="ee626-167">**Active Directory Tenant** - The DNS URL for Finance and Operations AD FS machine.</span></span> <span data-ttu-id="ee626-168">URL に「/adfs/oauth2」を追加します。</span><span class="sxs-lookup"><span data-stu-id="ee626-168">Append the URL with '/adfs/oauth2'.</span></span> 
        <span data-ttu-id="ee626-169">例: `https://adfs.d365ffo.onprem.contoso.com/adfs/oauth2` ADFS マシン (例では CNAME は `https://adfs.d365ffo.onprem.contoso.com` です) の CNAME を使用していることを確認します</span><span class="sxs-lookup"><span data-stu-id="ee626-169">For example: `https://adfs.d365ffo.onprem.contoso.com/adfs/oauth2` Make sure to use the CNAME of the ADFS machine (in the example the CNAME is `https://adfs.d365ffo.onprem.contoso.com`)</span></span>

3.  <span data-ttu-id="ee626-170">**会社** - Finance and Operations にアプリケーションが接続する法的エンティティを入力します。</span><span class="sxs-lookup"><span data-stu-id="ee626-170">**Company** - Enter the legal entity in Finance and Operations to which you want the application to connect.</span></span>
4.  <span data-ttu-id="ee626-171">アプリケーションの左上隅にある **戻る** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee626-171">Select the **Back** button in the top-left corner of the application.</span></span>

    <span data-ttu-id="ee626-172">アプリケーションは Finance and Operations サーバーに接続し、倉庫ワーカーのログイン画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee626-172">The application will now connect to your Finance and Operations server and the log-in screen for the warehouse worker will display.</span></span>
