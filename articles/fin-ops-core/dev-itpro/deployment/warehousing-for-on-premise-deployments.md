---
title: オンプレミス配置の倉庫管理アプリを構成
description: このトピックでは、オンプレミス展開でのウェアハウス アプリの前提条件について説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 24861
ms.assetid: 63e43066-76c7-400b-be7d-d14785e7985d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d119ab23c0b2bfc668131cd5b354b709d8045afb
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026203"
---
# <a name="configure-the-warehousing-app-for-on-premises-deployments"></a><span data-ttu-id="82259-103">オンプレミス配置の倉庫管理アプリを構成</span><span class="sxs-lookup"><span data-stu-id="82259-103">Configure the Warehousing app for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82259-104">このトピックでは、オンプレミス配置の Dynamics 365 for Finance and Operations – Warehousing アプリの構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="82259-104">This topic describes how to configure Dynamics 365 for Finance and Operations – Warehousing app for on-premises deployments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="82259-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="82259-105">Prerequisites</span></span>
<span data-ttu-id="82259-106">倉庫管理アプリは Android および Windows オペレーティング システムで使用できます。</span><span class="sxs-lookup"><span data-stu-id="82259-106">The Warehousing app is available on Android and Windows operating systems.</span></span> <span data-ttu-id="82259-107">オンプレミスの展開にこのアプリを使用するには、少なくともバージョン 1.1.1.0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="82259-107">To use the app for on-premises deployments, at a minimum, it must be version 1.1.1.0.</span></span> <span data-ttu-id="82259-108">Dynamics 365 Finance + Operations (オンプレミス) が次のサポートされているバージョンの 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="82259-108">You must also have one of the following supported versions of Dynamics 365 Finance + Operations (on-premises).</span></span> <span data-ttu-id="82259-109">ハードウェアおよびソフトウェア環境で構成がサポートされているかどうかを評価するには、次の表の情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="82259-109">Use the information in the following table to evaluate if your hardware and software environment supports the configuration.</span></span>

| <span data-ttu-id="82259-110">プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="82259-110">Platform</span></span>               | <span data-ttu-id="82259-111">バージョン</span><span class="sxs-lookup"><span data-stu-id="82259-111">Version</span></span>                                                                            |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82259-112">Android</span><span class="sxs-lookup"><span data-stu-id="82259-112">Android</span></span>                | <span data-ttu-id="82259-113">4.4 以上</span><span class="sxs-lookup"><span data-stu-id="82259-113">4.4 and up</span></span>                                                                         |
| <span data-ttu-id="82259-114">Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="82259-114">Windows (UWP)</span></span>          | <span data-ttu-id="82259-115">Windows 10 (すべてのバージョン)</span><span class="sxs-lookup"><span data-stu-id="82259-115">Windows 10 (all versions)</span></span>                                                          |
| <span data-ttu-id="82259-116">アプリのバージョン</span><span class="sxs-lookup"><span data-stu-id="82259-116">App version</span></span>            | <span data-ttu-id="82259-117">1.1.1.0 以上</span><span class="sxs-lookup"><span data-stu-id="82259-117">1.1.1.0 and above</span></span>                                                                  |
| <span data-ttu-id="82259-118">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="82259-118">Dynamics 365</span></span> | <span data-ttu-id="82259-119">Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="82259-119">Dynamics 365 Finance + Operations (on-premises) with Platform update 11</span></span> |

<span data-ttu-id="82259-120">アプリでオンプレミス リソースにアクセスできるようにするには、AOS および Active Directory フェデレーション サービス（AD FS）の DNS レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82259-120">To be able to reach your on-premises resources with the app, you will need to create DNS records for your AOS and for Active Directory Federation Services (AD FS).</span></span> <span data-ttu-id="82259-121">ガイダンスについては、[DNS ゾーンの作成とレコードの追加](setup-deploy-on-premises-pu12.md#setup) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82259-121">For guidance, see [Create DNS zones, and add a record](setup-deploy-on-premises-pu12.md#setup).</span></span>

## <a name="create-an-application-entry-in-ad-fs"></a><span data-ttu-id="82259-122">AD FS でアプリケーション エントリを作成する</span><span class="sxs-lookup"><span data-stu-id="82259-122">Create an application entry in AD FS</span></span>
<span data-ttu-id="82259-123">AD FS および Finance + Operations 間で認証を正常に交換するために、AD FS アプリケーション グループの下の AD FS にアプリケーション エントリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82259-123">For a successful authentication exchange between AD FS and Finance + Operations, an application entry must be registered in AD FS under an AD FS application group.</span></span> <span data-ttu-id="82259-124">このアプリケーション エントリを作成するには、AD FS がインストールされているマシンで次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="82259-124">To create this application entry, run the following Windows PowerShell commands on a machine where the AD FS is installed.</span></span> <span data-ttu-id="82259-125">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="82259-125">The user account must have enough permissions to administer AD FS.</span></span>

1.  <span data-ttu-id="82259-126">アプリケーションのエントリを作成する Windows PowerShell コンソールに、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="82259-126">Enter the following command in the Windows PowerShell console to create the application entry.</span></span>  

    ```powershell
    Add-AdfsClient -Name 'Dynamics 365 for Finance and Operations - Warehousing' -ClientId ([guid]::NewGuid()) -ClientType Confidential -GenerateClientSecret -RedirectUri '\<Resource URL\>' -ADUserPrincipalName '\<Admin user\>' 
    ```

    - <span data-ttu-id="82259-127">\<リソース URL\> は、たとえば `https://ax.d365ffo.onprem.contoso.com` などです (`https://ax.d365ffo.onprem.contoso.com` は、Finance + Operations にアクセスするための URL です)。</span><span class="sxs-lookup"><span data-stu-id="82259-127">The \<Resource URL\> can, for example, be `https://ax.d365ffo.onprem.contoso.com` (where `https://ax.d365ffo.onprem.contoso.com` is the URL to access Finance + Operations).</span></span>
    - <span data-ttu-id="82259-128">\<管理者ユーザー\> は、AD FS コンピューターへの管理者のアクセス権を持つ任意のユーザーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="82259-128">The \<Admin user\> can be any user with admin access to the AD FS machine.</span></span>

2.  <span data-ttu-id="82259-129">受信した値を保存します。</span><span class="sxs-lookup"><span data-stu-id="82259-129">Save the values that you received.</span></span>

3.  <span data-ttu-id="82259-130">アプリケーションへのアクセス許可を付与するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="82259-130">Run the following command to grant permission to the application.</span></span>  
    
    ```powershell
    Grant-AdfsApplicationPermission -ClientRoleIdentifier '\<Client ID received in previous steps\>' -ServerRoleIdentifier '\<Resource URL\>' -ScopeNames 'openid'
    ```

## <a name="create-and-configure-a-user-account"></a><span data-ttu-id="82259-131">ユーザー アカウントの作成およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="82259-131">Create and configure a user account</span></span>

<span data-ttu-id="82259-132">Finance + Operations で AD FS アプリケーションを使用できるようにするには、倉庫管理アプリのユーザーと同じユーザー資格情報を使用して Microsoft Dynamics 365 でユーザー アカウントを作成する必要があります:</span><span class="sxs-lookup"><span data-stu-id="82259-132">To enable Finance + Operations to use your AD FS application, you must create a user account in Microsoft Dynamics 365 with the same user credentials as the user of the Warehousing app:</span></span>

1.  <span data-ttu-id="82259-133">Finance + Operations でユーザーを作成し、倉庫管理モバイル デバイス ユーザー ロールをユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="82259-133">Create a user in Finance + Operations and assign the Warehousing mobile device user role to the user.</span></span>

    <span data-ttu-id="82259-134">a.</span><span class="sxs-lookup"><span data-stu-id="82259-134">a.</span></span>  <span data-ttu-id="82259-135">**システム管理** \> **共通** \> **ユーザー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82259-135">Go to **System administration** \> **Common** \> **Users**.</span></span>
    
    <span data-ttu-id="82259-136">b.</span><span class="sxs-lookup"><span data-stu-id="82259-136">b.</span></span>  <span data-ttu-id="82259-137">新規ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="82259-137">Create a new user.</span></span>
    
    <span data-ttu-id="82259-138">c.</span><span class="sxs-lookup"><span data-stu-id="82259-138">c.</span></span>  <span data-ttu-id="82259-139">例のスクリーンショットに示されているように、倉庫モバイル デバイス ユーザー ロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="82259-139">Assign the warehouse mobile device user role, as shown in the example screenshot.</span></span>

    ![ユーザーの作成およびコンフィギュレーション](media/wmapp-users.png)

2.  <span data-ttu-id="82259-141">AD FS アプリケーションと倉庫保管アプリ ユーザーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="82259-141">Associate your AD FS application with the Warehousing app user.</span></span>

    <span data-ttu-id="82259-142">a.</span><span class="sxs-lookup"><span data-stu-id="82259-142">a.</span></span>  <span data-ttu-id="82259-143">Finance + Operations で、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82259-143">In Finance + Operations, click **System administration** \> **Setup** \> **Azure Active Directory applications**.</span></span>
    
    <span data-ttu-id="82259-144">b.</span><span class="sxs-lookup"><span data-stu-id="82259-144">b.</span></span>  <span data-ttu-id="82259-145">新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="82259-145">Create a new line.</span></span>
    
    <span data-ttu-id="82259-146">c.</span><span class="sxs-lookup"><span data-stu-id="82259-146">c.</span></span>  <span data-ttu-id="82259-147">AD FS でアプリケーション エントリを作成したときに取得したクライアント ID を入力します (「AD FS でのアプリケーション エントリの作成」の手順 2)。</span><span class="sxs-lookup"><span data-stu-id="82259-147">Enter the client ID that you obtained when you created an application entry in AD FS (step 2 in "Create an application entry in AD FS").</span></span> <span data-ttu-id="82259-148">名前を入力し、倉庫管理アプリ ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="82259-148">Enter a name, and select the Warehousing app user.</span></span>

    ![<span data-ttu-id="82259-149">Azure Active Drectory アプリケーション</span><span class="sxs-lookup"><span data-stu-id="82259-149">Azure Active Drectory applications</span></span> ](media/azure-active-directory.png)

## <a name="certificates"></a><span data-ttu-id="82259-150">証明書</span><span class="sxs-lookup"><span data-stu-id="82259-150">Certificates</span></span> 

<span data-ttu-id="82259-151">アプリがインストールされているデバイスに、リソースにアクセスする適切な証明書があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="82259-151">Make sure that the devices with the app installed have the correct certificates to access the resources.</span></span> <span data-ttu-id="82259-152">自己署名証明書を使用している場合、コンピューター アカウント/ユーザー アカウントの信頼されているルートに star(AX) と AD FS をインポートすることで、これらが各デバイスにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="82259-152">If you are using self-signed certificates, these will need to be installed on each device by importing star(AX) and AD FS to the trusted route of the computer account/user account.</span></span> <span data-ttu-id="82259-153">詳細については、[自己署名証明書の作成およびエクスポート](https://technet.microsoft.com/library/ff710475(v=ws.10).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82259-153">For more information, see [Create and export a self-signed certificate](https://technet.microsoft.com/library/ff710475(v=ws.10).aspx).</span></span>

## <a name="configure-the-application"></a><span data-ttu-id="82259-154">アプリケーションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="82259-154">Configure the application</span></span>

<span data-ttu-id="82259-155">AD FS アプリケーションを使用してサーバーに接続するには、デバイス上で倉庫管理アプリを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82259-155">You must configure the Warehousing app on the device to connect to the server through the AD FS application.</span></span>

1.  <span data-ttu-id="82259-156">アプリで**接続設定**を開きます。</span><span class="sxs-lookup"><span data-stu-id="82259-156">In the app, open **Connection settings**.</span></span>
2.  <span data-ttu-id="82259-157">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="82259-157">Enter the following information:</span></span>

    <span data-ttu-id="82259-158">a.</span><span class="sxs-lookup"><span data-stu-id="82259-158">a.</span></span>  <span data-ttu-id="82259-159">**Active Directory クライアント ID** - AD FS でアプリケーション エントリを作成したときに取得したクライアント ID (「AD FS でのアプリケーション エントリの作成」の手順 2)。</span><span class="sxs-lookup"><span data-stu-id="82259-159">**Active Directory Client ID** - The client ID that you obtained when  you created an application entry in AD FS (step 2 in "Create an application entry in AD FS").</span></span>

    <span data-ttu-id="82259-160">b.</span><span class="sxs-lookup"><span data-stu-id="82259-160">b.</span></span>  <span data-ttu-id="82259-161">**Active Directory クライアント シークレット** - AD FS でアプリケーション エントリを作成したときに取得したクライアント シークレット。</span><span class="sxs-lookup"><span data-stu-id="82259-161">**Active Directory Client Secret** - The client secret obtained when you created an application entry in AD FS.</span></span>

    <span data-ttu-id="82259-162">c.</span><span class="sxs-lookup"><span data-stu-id="82259-162">c.</span></span>  <span data-ttu-id="82259-163">**Active Directory リソース** - AOS の DNS URL。</span><span class="sxs-lookup"><span data-stu-id="82259-163">**Active Directory Resource** - The DNS URL for the AOS.</span></span> <span data-ttu-id="82259-164">URL に「/namespaces/AXSF」を追加します。</span><span class="sxs-lookup"><span data-stu-id="82259-164">Append the URL with '/namespaces/AXSF'.</span></span> 
        <span data-ttu-id="82259-165">例: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF`</span><span class="sxs-lookup"><span data-stu-id="82259-165">For example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF`</span></span>

    <span data-ttu-id="82259-166">d.</span><span class="sxs-lookup"><span data-stu-id="82259-166">d.</span></span>  <span data-ttu-id="82259-167">**Active Directory テナント** - AD FS マシンの DNS URL。</span><span class="sxs-lookup"><span data-stu-id="82259-167">**Active Directory Tenant** - The DNS URL for the AD FS machine.</span></span> <span data-ttu-id="82259-168">URL に「/adfs/oauth2」を追加します。</span><span class="sxs-lookup"><span data-stu-id="82259-168">Append the URL with '/adfs/oauth2'.</span></span> 
        <span data-ttu-id="82259-169">例: `https://adfs.d365ffo.onprem.contoso.com/adfs/oauth2` ADFS マシン (例では CNAME は `https://adfs.d365ffo.onprem.contoso.com` です) の CNAME を使用していることを確認します</span><span class="sxs-lookup"><span data-stu-id="82259-169">For example: `https://adfs.d365ffo.onprem.contoso.com/adfs/oauth2` Make sure to use the CNAME of the ADFS machine (in the example the CNAME is `https://adfs.d365ffo.onprem.contoso.com`)</span></span>

3.  <span data-ttu-id="82259-170">**会社** - アプリケーションが接続する法的エンティティを入力します。</span><span class="sxs-lookup"><span data-stu-id="82259-170">**Company** - Enter the legal entity to which you want the application to connect.</span></span>
4.  <span data-ttu-id="82259-171">アプリケーションの左上隅にある **戻る** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="82259-171">Select the **Back** button in the top-left corner of the application.</span></span>

    <span data-ttu-id="82259-172">アプリケーションはサーバーに接続し、倉庫ワーカーのログイン画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="82259-172">The application will now connect to your server and the log-in screen for the warehouse worker will display.</span></span>
    
5. <span data-ttu-id="82259-173">倉庫アプリのテレメトリ ID がない場合、いくつかエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="82259-173">If you do not have a telemetry ID for the Warehouse app, you might encounter some errors.</span></span> <span data-ttu-id="82259-174">これは、既知の問題です。</span><span class="sxs-lookup"><span data-stu-id="82259-174">This is a known issue.</span></span> <span data-ttu-id="82259-175">回避策は既存のクライアントにサインインしてテレメトリ ID を取得することです。</span><span class="sxs-lookup"><span data-stu-id="82259-175">The workaround is to sign in to an existing client to get a Telemetry ID.</span></span> <span data-ttu-id="82259-176">この問題は、将来のリリースで修正されます。</span><span class="sxs-lookup"><span data-stu-id="82259-176">This issue will be fixed in a future release.</span></span>
