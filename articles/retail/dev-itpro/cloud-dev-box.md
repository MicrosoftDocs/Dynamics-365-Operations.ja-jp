---
title: "管理者アクセスのないクラウド ホスト開発環境での開発"
description: "このトピックは、クラウドでホストされている開発マシンで作業している Retail 開発者向けのコンフィギュレーション手順について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 07/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2017-12-08
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: a0fc60a16e5fa2f924a3394d701553d8e7652095
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="development-in-cloud-hosted-development-environments-without-admin-access"></a><span data-ttu-id="e0a6a-103">管理者アクセスのないクラウド ホスト開発環境での開発</span><span class="sxs-lookup"><span data-stu-id="e0a6a-103">Development in cloud-hosted development environments without admin access</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0a6a-104">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 時点で、顧客は Microsoft サブスクリプションで実行中の開発またはビルド環境で仮想マシン (VM) 管理者アカウントにアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-104">As of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, Platform update 12, customers will no longer have access to virtual machine (VM) administrator accounts on development or build environments that are running in Microsoft subscriptions.</span></span> <span data-ttu-id="e0a6a-105">この制限は、プラットフォーム更新 12 (またはそれ以降) 環境の新しい展開にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-105">This restriction only applies to new deployments of Platform update 12 (or newer) environments.</span></span> <span data-ttu-id="e0a6a-106">この更新プログラムの前に展開され、プラットフォーム更新プログラム 12 に更新された環境では、引き続き管理者アクセス権が与えられます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-106">Environments that were deployed before this update, and  have been updated to Platform update 12, will still have administrator access.</span></span>

<span data-ttu-id="e0a6a-107">リモート デスクトップ (RDP) を使用して、Lifecycle Services (LCS) 環境ページに用意されている非管理ユーザーを使用するこれらの制限された環境にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-107">You can use a remote desktop (RDP) to access these restricted environments using the non-admin user provided on the Lifecycle Services (LCS) environment page.</span></span> <span data-ttu-id="e0a6a-108">管理者アクセスを許可しない環境の詳細については、[管理者アクセスを許可しない開発用 およびビルド用 VM に関するよく寄せられる質問](../../dev-itpro/sysadmin/VMs-no-admin-access.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-108">For more information about environments that don't allow administrator access, see [Development and build VMs that don't allow administrator access FAQ](../../dev-itpro/sysadmin/VMs-no-admin-access.md).</span></span>

<span data-ttu-id="e0a6a-109">Lifecycle Services (LCS) の Microsoft Azure サブスクリプションを使用する環境を配置する場合、この環境では管理者アクセス権がありません。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-109">If you deploy an environment using Microsoft Azure subscription in Lifecycle Services (LCS), then you will not have admin access in this environment.</span></span> <span data-ttu-id="e0a6a-110">ご使用の環境で管理者アクセス権が必要な場合は、Azure サブスクリプションを使用し、LCS を使用して環境を配置してください。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-110">If you need admin access in your environment, use your Azure subscription and deploy the environment using LCS.</span></span> <span data-ttu-id="e0a6a-111">ダウンロード可能な VHD を使用して Azure 仮想マシン (VM) に配置したり、ローカルでホストしたりして完全な管理者権限を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-111">You can also use the downloadable VHD and deploy it in your Azure virtual machine (VM) or host it locally to get full admin access.</span></span>

<span data-ttu-id="e0a6a-112">この環境に管理者アクセス権がない場合、Modern POS を使用してテストおよびデバッグすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-112">If you don’t have admin access in the environment, you will not be able to test and debug using Modern POS.</span></span> <span data-ttu-id="e0a6a-113">カスタマイズをテストしている場合は、POS のすべての小売カスタマイズを行うことができます。その環境でクラウド POS を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-113">You can still do all retail customization for POS if you are testing the customization, you must use Cloud POS in that environment.</span></span> <span data-ttu-id="e0a6a-114">カスタマイズの観点からは、Cloud POS および Modern POS に違いはありません - どのカスタマイズも Cloud POS および Modern POS の両方で機能します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-114">From a customization perspective, there is no difference between Cloud POS and Modern POS - any customization will work both in Cloud POS and Modern POS.</span></span> <span data-ttu-id="e0a6a-115">ハードウェアおよびその他のシナリオの、ブラウザー固有もしくは UWP アプリ固有のロジックを追加しない限り、Modern POS か、その逆で作業するために Cloud POS で完了したカスタマイズの追加のロジックやコードはありません。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-115">There is no additional logic or code for customization completed in Cloud POS in order to work in Modern POS or vice versa, unless you added logic that is browser-specific or UWP app- specific for Hardware and other scenarios.</span></span> <span data-ttu-id="e0a6a-116">別のオプションは、Modern POS を使用した環境ですべての開発を実行し、MPOS をインストールするための管理者アクセス権限を持つ他の環境でテストすることです。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-116">Another option is to do all development work in the environment using Modern POS and test it in some other environment where you have admin access to install MPOS.</span></span> <span data-ttu-id="e0a6a-117">ほとんどの場合はクラウド POS を使用してテストすることができます。オフラインのシナリオをテストするか予想します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-117">In most cases, you should be able to test using Cloud POS, expect if you want to test for offline scenarious.</span></span> <span data-ttu-id="e0a6a-118">オフライン シナリオをテストする場合は、ビルド スクリプトを使用して Modern POS インストーラーを作成し、テスト環境またはその他のいくつかの POS レジスターでテストできます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-118">If you want to test offline scenarios, you can create a Modern POS installer using the build script, and then test it in your test environment or some other POS registers.</span></span>

<span data-ttu-id="e0a6a-119">**クラウド POS を開発に使用している場合は、クラウド POS プロジェクトを開く前に以下の設定を行います**</span><span class="sxs-lookup"><span data-stu-id="e0a6a-119">**If you are using Cloud POS for development, set up the following configuration before opening the Cloud POS project**</span></span>

1. <span data-ttu-id="e0a6a-120">Visual Studio を開き、**表示** > **アプリケーション エクスプ ローラー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-120">Open Visual Studio and click **View** > **Application Explorer**.</span></span> <span data-ttu-id="e0a6a-121">インターネット インフォメーション サービス (IIS) Express が配置されているすべての Retail Web サイトで開始するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-121">Wait for Internet Information Services (IIS) Express to start with all the Retail websites deployed.</span></span> <span data-ttu-id="e0a6a-122">タスク バーに IIS トレー アイコンが表示され、Cloud POS や Retail Server など、Retail のウェブサイトがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-122">You should see the IIS tray icon in the task bar with all the Retail websites running, such as Cloud POS and Retail Server.</span></span>
4. <span data-ttu-id="e0a6a-123">CRT/RS 拡張をデバッグするには、CRT/RS プロジェクトを IIS Express プロセスに添付します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-123">To debug CRT/RS extensions, attach the CRT/RS project to the IIS Express process.</span></span>
5. <span data-ttu-id="e0a6a-124">Retail SDK からクラウド POS プロジェクトを開くと、次のエラーで IIS Express が失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-124">When you open the Cloud POS project from the Retail SDK, IIS Express may fail with the following error.</span></span> 

    ```
    Filename: redirection.config
    Error: Cannot read configuration file
    ``` 
    <span data-ttu-id="e0a6a-125">この問題を解決するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-125">To resolve this issue:</span></span>
    1. <span data-ttu-id="e0a6a-126">Visual Studio を閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-126">Close Visual Studio.</span></span>
    2. <span data-ttu-id="e0a6a-127">**%userprofile%\Documents\IISExpress\config** フォルダーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-127">Rename the **%userprofile%\Documents\IISExpress\config** folder.</span></span> <span data-ttu-id="e0a6a-128">ステップ *iv* の新しい場所に、**applicationhost.config** のコピーがあるので、ファイルを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-128">Do not delete the files because you will copy the **applicationhost.config** file to a new location in step *iv*.</span></span>
    3. <span data-ttu-id="e0a6a-129">Cloud POS プロジェクトを使用して Visual Studio を再度起動します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-129">Start Visual Studio again with the Cloud POS project.</span></span> <span data-ttu-id="e0a6a-130">**%userprofile%\Documents\IISExpress\config** フォルダーは、既定の構成ファイルを使用して再作成されます。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-130">The **%userprofile%\Documents\IISExpress\config** folder will be recreated with the default config files.</span></span>
    4. <span data-ttu-id="e0a6a-131">**applicationhost.config** ファイルを、ステップ *ii* で名前を変更したフォルダーから、ステップ *iii* で作成したフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-131">Copy the **applicationhost.config** file from the folder that you renamed in step *ii*, to the folder created in step *iii*.</span></span> 

## <a name="install-the-developer-topology-prerequisites"></a><span data-ttu-id="e0a6a-132">開発者トポロジの前提条件のインストール</span><span class="sxs-lookup"><span data-stu-id="e0a6a-132">Install the Developer topology prerequisites</span></span>

<span data-ttu-id="e0a6a-133">クラウド ホスト開発環境には Typescript バージョン 2.2.2 が既定で含まれておらず、既定の Windows ホスト ファイルにはローカル デバッグに使用するクラウド POS URLが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-133">Cloud-hosted development environments do not include Typescript version 2.2.2 by default, and the default Windows host file does not contain the Cloud POS URL to use for local debugging.</span></span> <span data-ttu-id="e0a6a-134">**開発者トポロジの前提条件** パッケージは、Typescript 2.2.2 をインストールし、Cloud POS URL を使用して Windows ホスト ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-134">The **Developer topology prerequisites** package installs Typescript 2.2.2 and updates the Windows host file with your Cloud POS URL.</span></span> <span data-ttu-id="e0a6a-135">パッケージの展開には数分かかります。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-135">Deploying the package will take a few minutes.</span></span> 


<span data-ttu-id="e0a6a-136">開発者トポロジの前提条件をインストールするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-136">To install the Developer topology prerequisites:</span></span>

   1. <span data-ttu-id="e0a6a-137">Lifecycle Services (https://lcs.dynamics.com) に移動しサインインします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-137">Go to Lifecycle Services (https://lcs.dynamics.com) and sign in.</span></span>
   2. <span data-ttu-id="e0a6a-138">**プロジェクト** で、開発環境が展開されているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-138">Under **Projects**, select the project where your dev environment is deployed.</span></span>
   3. <span data-ttu-id="e0a6a-139">**追加ツール** セクションで、**アセット ライブラリ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-139">In the **More tools** section, click the **Asset library** tile.</span></span>
   4. <span data-ttu-id="e0a6a-140">アセット ライブラリ タイプとして **ソフトウェア配置可能パッケージ** を選択し、**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-140">Select **Software deployable package** for the Asset library type and click **Import**.</span></span>
   5. <span data-ttu-id="e0a6a-141">**共有アセット ライブラリ リスト**で、**開発者トポロジの前提条件**を選択して**選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-141">In the **Shared asset library list**, select **Developer topology prerequisites** and click **Pick**.</span></span>
   6. <span data-ttu-id="e0a6a-142">**環境**セクションに移動し、開発環境をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-142">Go to the **Environments** section, and click your development environment.</span></span>
   7. <span data-ttu-id="e0a6a-143">**管理**タブをクリックし、**更新プログラムの適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-143">Click the **Maintain** tab and select **Apply updates**.</span></span>
   8. <span data-ttu-id="e0a6a-144">**開発者トポロジの前提条件** を選択し、**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0a6a-144">Select **Developer topology prerequisites** and click **Apply**.</span></span>

