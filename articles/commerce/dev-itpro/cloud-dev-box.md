---
title: 管理者のアクセス権を使用しないクラウド ホスト環境での開発
description: このトピックでは、クラウドでホストされている開発マシンで作業しているコマース開発者向けのコンフィギュレーション手順について説明します。
author: mugunthanm
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2017-12-08
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8a53852987a4a0fd8d80d382c6f33590c6c715ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791219"
---
# <a name="development-in-cloud-hosted-environments-without-admin-access"></a><span data-ttu-id="11d10-103">管理者のアクセス権を使用しないクラウド ホスト環境での開発</span><span class="sxs-lookup"><span data-stu-id="11d10-103">Development in cloud-hosted environments without admin access</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11d10-104">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、プラットフォーム更新プログラム 12 では、Microsoft 定期購読を実行している開発または構築環境で仮想マシン (VM) 管理者アカウントにアクセスできなくなり、Microsoft 定期購読を使用して層 1 環境を配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="11d10-104">As of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, Platform update 12, you will no longer have access to virtual machine (VM) administrator accounts on development or build environments that are running Microsoft subscriptions and you will not be able to deploy Tier 1 environment using a Microsoft subscription.</span></span>

<span data-ttu-id="11d10-105">リモート デスクトップ (RDP) を使用して、Lifecycle Services (LCS) 環境ページに用意されている非管理ユーザーを使用するこれらの制限された環境にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="11d10-105">You can use a remote desktop (RDP) to access these restricted environments using the non-admin user provided on the Lifecycle Services (LCS) environment page.</span></span> <span data-ttu-id="11d10-106">管理者アクセスを許可しない環境の詳細については、[管理者アクセスを許可しない開発用 およびビルド用 VM に関するよく寄せられる質問](../../dev-itpro/sysadmin/VMs-no-admin-access.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11d10-106">For more information about environments that don't allow administrator access, see [Development and build VMs that don't allow administrator access FAQ](../../dev-itpro/sysadmin/VMs-no-admin-access.md).</span></span>

<span data-ttu-id="11d10-107">ご使用の環境で管理者アクセス権が必要な場合は、Azure サブスクリプションを使用し、LCS を使用して環境を配置してください。</span><span class="sxs-lookup"><span data-stu-id="11d10-107">If you need admin access in your environment, use your Azure subscription and deploy the environment using LCS.</span></span> <span data-ttu-id="11d10-108">ダウンロード可能な VHD を使用して Azure VM に配置したり、ローカルでホストしたりして完全な管理者権限を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="11d10-108">You can also use the downloadable VHD and deploy it in your Azure VM or host it locally to get full admin access.</span></span>

<span data-ttu-id="11d10-109">この環境に管理者アクセス権がない場合、Modern POS を使用してテストおよびデバッグすることはできません。</span><span class="sxs-lookup"><span data-stu-id="11d10-109">If you don’t have admin access in the environment, you will not be able to test and debug using Modern POS.</span></span> <span data-ttu-id="11d10-110">カスタマイズをテストしている場合は、POS のすべてのコマース カスタマイズを行うことができ、その環境でクラウド POS を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11d10-110">You can still do all commerce customization for POS if you are testing the customization, you must use Cloud POS in that environment.</span></span> <span data-ttu-id="11d10-111">カスタマイズの観点からは、Cloud POS および Modern POS に違いはありません - どのカスタマイズも Cloud POS および Modern POS の両方で機能します。</span><span class="sxs-lookup"><span data-stu-id="11d10-111">From a customization perspective, there is no difference between Cloud POS and Modern POS - any customization will work both in Cloud POS and Modern POS.</span></span> <span data-ttu-id="11d10-112">ハードウェアおよびその他のシナリオの、ブラウザー固有もしくは UWP アプリ固有のロジックを追加しない限り、Modern POS か、その逆で作業するために Cloud POS で完了したカスタマイズの追加のロジックやコードはありません。</span><span class="sxs-lookup"><span data-stu-id="11d10-112">There is no additional logic or code for customization completed in Cloud POS in order to work in Modern POS or vice versa, unless you added logic that is browser-specific or UWP app- specific for Hardware and other scenarios.</span></span> <span data-ttu-id="11d10-113">別のオプションは、Modern POS を使用した環境ですべての開発を実行し、MPOS をインストールするための管理者アクセス権限を持つ他の環境でテストすることです。</span><span class="sxs-lookup"><span data-stu-id="11d10-113">Another option is to do all development work in the environment using Modern POS and test it in some other environment where you have admin access to install MPOS.</span></span> <span data-ttu-id="11d10-114">ほとんどの場合はクラウド POS を使用してテストすることが可能で、オフラインのシナリオをテストするか予想します。</span><span class="sxs-lookup"><span data-stu-id="11d10-114">In most cases, you should be able to test using Cloud POS, expect if you want to test for offline scenarios.</span></span> <span data-ttu-id="11d10-115">オフライン シナリオをテストする場合は、ビルド スクリプトを使用して Modern POS インストーラーを作成し、テスト環境またはその他のいくつかの POS レジスターでテストできます。</span><span class="sxs-lookup"><span data-stu-id="11d10-115">If you want to test offline scenarios, you can create a Modern POS installer using the build script, and then test it in your test environment or some other POS registers.</span></span>

<span data-ttu-id="11d10-116">**クラウド POS を開発に使用している場合は、クラウド POS プロジェクトを開く前に以下の設定を行います**</span><span class="sxs-lookup"><span data-stu-id="11d10-116">**If you are using Cloud POS for development, set up the following configuration before opening the Cloud POS project**</span></span>

1. <span data-ttu-id="11d10-117">Visual Studio を開き、**表示** > **アプリケーション エクスプローラー** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="11d10-117">Open Visual Studio and go to **View** > **Application Explorer**.</span></span> <span data-ttu-id="11d10-118">インターネット インフォメーション サービス (IIS) Express が配置されているすべてのコマース Web サイトで開始するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="11d10-118">Wait for Internet Information Services (IIS) Express to start with all the Commerce websites deployed.</span></span> <span data-ttu-id="11d10-119">タスク バーに IIS トレー アイコンが表示され、クラウド POS や Commerce Scale Unit など、すべての Web サイトがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="11d10-119">You should see the IIS tray icon in the task bar with all the websites running, such as Cloud POS and Commerce Scale Unit.</span></span>
4. <span data-ttu-id="11d10-120">CRT/RS 拡張をデバッグするには、CRT/RS プロジェクトを IIS Express プロセスに添付します。</span><span class="sxs-lookup"><span data-stu-id="11d10-120">To debug CRT/RS extensions, attach the CRT/RS project to the IIS Express process.</span></span>
5. <span data-ttu-id="11d10-121">Retail SDK からクラウド POS プロジェクトを開くと、次のエラーで IIS Express が失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="11d10-121">When you open the Cloud POS project from the Retail SDK, IIS Express may fail with the following error.</span></span> 

    ```Console
    Filename: redirection.config
    Error: Cannot read configuration file
    ``` 

<span data-ttu-id="11d10-122">**この問題を解決するには**</span><span class="sxs-lookup"><span data-stu-id="11d10-122">**To resolve this issue**</span></span>

1. <span data-ttu-id="11d10-123">Visual Studio を閉じます。</span><span class="sxs-lookup"><span data-stu-id="11d10-123">Close Visual Studio.</span></span>
2. <span data-ttu-id="11d10-124">**aspnet.config** および **redirection.config** ファイルを **%userprofile%\Documents\IISExpress\config** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="11d10-124">Copy the **aspnet.config** and **redirection.config** files to **%userprofile%\Documents\IISExpress\config**.</span></span>
3. <span data-ttu-id="11d10-125">**%userprofile%\Documents\IISExpress\config** フォルダー内の **applicationhost.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="11d10-125">Open the **applicationhost.config** file in the **%userprofile%\Documents\IISExpress\config** folder.</span></span>
4. <span data-ttu-id="11d10-126">**applicationhost.config** で、RetailCloudPos の physcialPath を変更し、SDK の場所をポイントするようにします。</span><span class="sxs-lookup"><span data-stu-id="11d10-126">In **applicationhost.config**, change the physcialPath of RetailCloudPos to point to your SDK location.</span></span>
   <span data-ttu-id="11d10-127">たとえば、physicalPath="K:\RetailSDK\POS\Web" です。</span><span class="sxs-lookup"><span data-stu-id="11d10-127">For example, physicalPath="K:\RetailSDK\POS\Web".</span></span> <span data-ttu-id="11d10-128">全体的なセクションは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="11d10-128">The overall section will look like the following:</span></span>
   
    ```xml
   <site name="RetailCloudPOs" id="4" serverAutoStart="true">
        <application path="/" applicationPool="Dynamics365">
            <virtualDirectory path="/" physicalPath="K:\RetailSDK\POS\Web" />
        </application>
    ```
5. <span data-ttu-id="11d10-129">変更を **applicationhost.config** に保存します</span><span class="sxs-lookup"><span data-stu-id="11d10-129">Save the changes to **applicationhost.config**</span></span> 
6. <span data-ttu-id="11d10-130">**%userprofile%\Documents\IISExpress\config** フォルダーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="11d10-130">Rename the **%userprofile%\Documents\IISExpress\config** folder.</span></span> <span data-ttu-id="11d10-131">**ステップ 8** の新しい場所に **applicationhost.config** ファイルをコピーするため、ファイルを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="11d10-131">Do not delete the files because you will copy the **applicationhost.config** file to a new location in **step 8**.</span></span>
7. <span data-ttu-id="11d10-132">Cloud POS プロジェクトに対して、Visual Studio を再度起動します。</span><span class="sxs-lookup"><span data-stu-id="11d10-132">Start Visual Studio again with the Cloud POS project.</span></span> <span data-ttu-id="11d10-133">**%userprofile%\Documents\IISExpress\config** フォルダーが、既定の構成ファイルを使用して再作成されます。</span><span class="sxs-lookup"><span data-stu-id="11d10-133">The **%userprofile%\Documents\IISExpress\config** folder will be recreated with the default config files.</span></span>
8. <span data-ttu-id="11d10-134">**applicationhost.config** ファイルを、**ステップ 6** で名前を変更したフォルダーから、**ステップ 7** で作成したフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="11d10-134">Copy the **applicationhost.config** file from the folder that you renamed in **step 6**, to the folder created in **step 7**.</span></span> 
9. <span data-ttu-id="11d10-135">\RetailSDK\POS\Web\Pos.Web.csproj を編集し、既定の **IISURL** ノードを使用しているクラウド POS URL に変更してから **UseIIS** を false に設定します。</span><span class="sxs-lookup"><span data-stu-id="11d10-135">Edit ..\RetailSDK\POS\Web\Pos.Web.csproj and change the default **IISURL** node value to your Cloud POS URL and set **UseIIS** to false.</span></span>
```    
    Ex:  
    <UseIIS>False</UseIIS>
    <IISUrl>https://YourCPOSURL.com</IISUrl>
```
10. <span data-ttu-id="11d10-136">Pos.Web プロジェクトを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11d10-136">Right-click the Pos.Web project and select **Properties**.</span></span>
11. <span data-ttu-id="11d10-137">**プロパティ** ウィンドウで、**Web** タブを選択します。**URL の開始** を選び、URL の開始をクラウド POS URL として設定し、ドロップ ダウン メニューから **サーバー セクションで、IIS Express をサーバーとして選択** を実行し、**プロジェクト URL** をクラウド POS URL として設定します。</span><span class="sxs-lookup"><span data-stu-id="11d10-137">In the **Properties** window, select the **Web** tab. Select the **Start URL radio** option and set the start URL as your Cloud POS URL and under the **Servers section select IIS Express as the server** from the drop down menu and set the **Project URL** as your cloud POS URL.</span></span> 

<span data-ttu-id="11d10-138">開発に対して IIS を使用している場合は (管理者アクセス権を持つ VMs)、UseIIS ノード値を False に設定し、サーバー ドロップ ダウン メニューからローカル IIS を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11d10-138">If you are using IIS for development (VMs with admin access), then you need to set the UseIIS node value to False and select Local IIS from the Server drop-down menu.</span></span>

<span data-ttu-id="11d10-139">たとえば、`https://usnconeboxax1pos.cloud.onebox.dynamics.com`。</span><span class="sxs-lookup"><span data-stu-id="11d10-139">For example, `https://usnconeboxax1pos.cloud.onebox.dynamics.com`.</span></span>

12. <span data-ttu-id="11d10-140">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="11d10-140">Save the changes.</span></span>
13. <span data-ttu-id="11d10-141">Pos Web プロジェクトを右クリックし、**StartUp プロジェクトとして設定** を選択ます。</span><span class="sxs-lookup"><span data-stu-id="11d10-141">Right-click the Pos.Web project and select **Set as StartUp Project**.</span></span>
14. <span data-ttu-id="11d10-142">F5 キーを押して Pos.Web プロジェクトを実行するか、Visual Studio メニューの **実行** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="11d10-142">Press F5 to run the Pos.Web Project or click the **Run** button in the Visual Studio menu.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
