---
title: "管理者のアクセス権がないクラウド ホスト開発環境で作業している Retail 開発者向けのコンフィギュレーション手順"
description: "このトピックは、クラウドでホストされている開発マシンで作業している Retail 開発者向けのコンフィギュレーション手順について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 01/16/2018
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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 80fbac7e993b47c70423739ec2716a344bde55c5
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="configuration-steps-for-retail-developers-working-on-cloud-hosted-development-environments-with-no-administrator-access"></a><span data-ttu-id="f317a-103">管理者のアクセス権がないクラウド ホスト開発環境で作業している Retail 開発者向けのコンフィギュレーション手順</span><span class="sxs-lookup"><span data-stu-id="f317a-103">Configuration steps for Retail developers working on cloud-hosted development environments with no administrator access</span></span>

[!INCLUDE [banner](../../includes/banner.md)]

<span data-ttu-id="f317a-104">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 時点で、顧客は Microsoft サブスクリプションで実行中の開発またはビルド環境で仮想マシン (VM) 管理者アカウントにアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="f317a-104">As of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, Platform update 12, customers will no longer have access to virtual machine (VM) administrator accounts on development or build environments that are running in Microsoft subscriptions.</span></span> <span data-ttu-id="f317a-105">この制限は、プラットフォーム更新 12 (またはそれ以降) 環境の新しい展開にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f317a-105">This restriction only applies to new deployments of Platform update 12 (or newer) environments.</span></span> <span data-ttu-id="f317a-106">この更新プログラムの前に展開され、プラットフォーム更新プログラム 12 に更新された環境では、引き続き管理者アクセス権が与えられます。</span><span class="sxs-lookup"><span data-stu-id="f317a-106">Environments that were deployed before this update, and  have been updated to Platform update 12, will still have administrator access.</span></span>

<span data-ttu-id="f317a-107">リモート デスクトップ (RDP) を使用して、Lifecycle Services (LCS) 環境ページに用意されている非管理ユーザーを使用するこれらの制限された環境にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="f317a-107">You can use a remote desktop (RDP) to access these restricted environments using the non-admin user provided on the Lifecycle Services (LCS) environment page.</span></span> <span data-ttu-id="f317a-108">このブログの記事には、これらの VM へのアクセス方法に関する詳細が含まれています。https://blogs.msdn.microsoft.com/lcs/2017/10/31/restricted-admin-access-with-platform-12-updates/</span><span class="sxs-lookup"><span data-stu-id="f317a-108">This blog post contains more information about how to access these VMs: https://blogs.msdn.microsoft.com/lcs/2017/10/31/restricted-admin-access-with-platform-12-updates/</span></span>

<span data-ttu-id="f317a-109">小売開発者は、クラウドにホストされた開発仮想マシンに管理アクセスできません。</span><span class="sxs-lookup"><span data-stu-id="f317a-109">Retail developers do not have administrative access to cloud-hosted development virtual machines.</span></span> <span data-ttu-id="f317a-110">Modern POS (MPOS) 開発は、クラウド POS を使用する場合に可能です。</span><span class="sxs-lookup"><span data-stu-id="f317a-110">Modern POS (MPOS) development is possible if you use Cloud POS.</span></span> <span data-ttu-id="f317a-111">Retail アプリケーションの開発を開始する前に、次のようにクラウド POS を構成します。</span><span class="sxs-lookup"><span data-stu-id="f317a-111">Before starting development on any Retail application, configure Cloud POS as follows:</span></span>


1. <span data-ttu-id="f317a-112">Visual Studio を開き、**表示** > **アプリケーション エクスプ ローラー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f317a-112">Open Visual Studio and click **View** > **Application Explorer**.</span></span> <span data-ttu-id="f317a-113">インターネット インフォメーション サービス (IIS) Express が配置されているすべての Retail Web サイトで開始するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="f317a-113">Wait for Internet Information Services (IIS) Express to start with all the Retail websites deployed.</span></span> <span data-ttu-id="f317a-114">タスク バーに IIS トレー アイコンが表示され、Cloud POS や Retail Server など、Retail のウェブサイトがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="f317a-114">You should see the IIS tray icon in the task bar with all the Retail websites running, such as Cloud POS and Retail Server.</span></span>
4. <span data-ttu-id="f317a-115">CRT/RS 拡張をデバッグするには、CRT/RS プロジェクトを IIS Express プロセスに添付します。</span><span class="sxs-lookup"><span data-stu-id="f317a-115">To debug CRT/RS extensions, attach the CRT/RS project to the IIS Express process.</span></span>
5. <span data-ttu-id="f317a-116">Retail SDK からクラウド POS プロジェクトを開くと、次のエラーで IIS Express が失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="f317a-116">When you open the Cloud POS project from the Retail SDK, IIS Express may fail with the following error.</span></span> 

    ```
    Filename: redirection.config
    Error: Cannot read configuration file
    ``` 
    <span data-ttu-id="f317a-117">この問題を解決するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="f317a-117">To resolve this issue:</span></span>
    1. <span data-ttu-id="f317a-118">Visual Studio を閉じます。</span><span class="sxs-lookup"><span data-stu-id="f317a-118">Close Visual Studio.</span></span>
    2. <span data-ttu-id="f317a-119">**%userprofile%\Documents\IISExpress\config** フォルダーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="f317a-119">Rename the **%userprofile%\Documents\IISExpress\config** folder.</span></span> <span data-ttu-id="f317a-120">ステップ *iv* の新しい場所に、**applicationhost.config** のコピーがあるので、ファイルを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="f317a-120">Do not delete the files because you will copy the **applicationhost.config** file to a new location in step *iv*.</span></span>
    3. <span data-ttu-id="f317a-121">Cloud POS プロジェクトを使用して Visual Studio を再度起動します。</span><span class="sxs-lookup"><span data-stu-id="f317a-121">Start Visual Studio again with the Cloud POS project.</span></span> <span data-ttu-id="f317a-122">**%userprofile%\Documents\IISExpress\config** フォルダーは、既定の構成ファイルを使用して再作成されます。</span><span class="sxs-lookup"><span data-stu-id="f317a-122">The **%userprofile%\Documents\IISExpress\config** folder will be recreated with the default config files.</span></span>
    4. <span data-ttu-id="f317a-123">**applicationhost.config** ファイルを、ステップ *ii* で名前を変更したフォルダーから、ステップ *iii* で作成したフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f317a-123">Copy the **applicationhost.config** file from the folder that you renamed in step *ii*, to the folder created in step *iii*.</span></span> 

## <a name="install-the-developer-topology-prerequisites"></a><span data-ttu-id="f317a-124">開発者トポロジの前提条件のインストール</span><span class="sxs-lookup"><span data-stu-id="f317a-124">Install the Developer topology prerequisites</span></span>

<span data-ttu-id="f317a-125">クラウド ホスト開発環境には Typescript バージョン 2.2.2 が既定で含まれておらず、既定の Windows ホスト ファイルにはローカル デバッグに使用するクラウド POS URLが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f317a-125">Cloud-hosted development environments do not include Typescript version 2.2.2 by default, and the default Windows host file does not contain the Cloud POS URL to use for local debugging.</span></span> <span data-ttu-id="f317a-126">**開発者トポロジの前提条件** パッケージは、Typescript 2.2.2 をインストールし、Cloud POS URL を使用して Windows ホスト ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="f317a-126">The **Developer topology prerequisites** package installs Typescript 2.2.2 and updates the Windows host file with your Cloud POS URL.</span></span> <span data-ttu-id="f317a-127">パッケージの展開には数分かかります。</span><span class="sxs-lookup"><span data-stu-id="f317a-127">Deploying the package will take a few minutes.</span></span> 


<span data-ttu-id="f317a-128">開発者トポロジの前提条件をインストールするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="f317a-128">To install the Developer topology prerequisites:</span></span>

   1. <span data-ttu-id="f317a-129">Lifecycle Services (https://lcs.dynamics.com) に移動しサインインします。</span><span class="sxs-lookup"><span data-stu-id="f317a-129">Go to Lifecycle Services (https://lcs.dynamics.com) and sign in.</span></span>
   2. <span data-ttu-id="f317a-130">**プロジェクト** で、開発環境が展開されているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="f317a-130">Under **Projects**, select the project where your dev environment is deployed.</span></span>
   3. <span data-ttu-id="f317a-131">**追加ツール** セクションで、**アセット ライブラリ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f317a-131">In the **More tools** section, click the **Asset library** tile.</span></span>
   4. <span data-ttu-id="f317a-132">アセット ライブラリ タイプとして **ソフトウェア配置可能パッケージ** を選択し、**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f317a-132">Select **Software deployable package** for the Asset library type and click **Import**.</span></span>
   5. <span data-ttu-id="f317a-133">**共有アセット ライブラリ リスト**で、**開発者トポロジの前提条件**を選択して**選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f317a-133">In the **Shared asset library list**, select **Developer topology prerequisites** and click **Pick**.</span></span>
   6. <span data-ttu-id="f317a-134">**環境**セクションに移動し、開発環境をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f317a-134">Go to the **Environments** section, and click your development environment.</span></span>
   7. <span data-ttu-id="f317a-135">**管理**タブをクリックし、**更新プログラムの適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f317a-135">Click the **Maintain** tab and select **Apply updates**.</span></span>
   8. <span data-ttu-id="f317a-136">**開発者トポロジの前提条件** を選択し、**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f317a-136">Select **Developer topology prerequisites** and click **Apply**.</span></span>

