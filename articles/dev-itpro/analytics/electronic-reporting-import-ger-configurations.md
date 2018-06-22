---
title: "電子申告コンフィギュレーションのインポート"
description: "このトピックでは、Lifecycle Services (LCS) からローカルのビジネス データ アプリケーションに電子申告 (ER) の構成をインポートする方法について説明します。"
author: NickSelin
manager: AnnBe
ms.date: 06/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport
audience: Developer
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 151bf7e56a36392f8df1f7a46a513e3b467bf6c5
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="import-electronic-reporting-configurations"></a><span data-ttu-id="46e80-103">電子申告コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="46e80-103">Import Electronic reporting configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46e80-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) からローカルのビジネス データ アプリケーションに電子申告 (ER) の構成をダウンロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="46e80-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS) to a local business data application.</span></span> <span data-ttu-id="46e80-105">また、ER リポジトリからローカル ビジネス データ (LBD) アプリケーションに ER 構成をアップロードする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="46e80-105">It also explains how to upload the ER configurations from an ER repository to the local business data (LBD) application.</span></span>

1. <span data-ttu-id="46e80-106">次のロールのいずれかを使用して、ローカル ビジネス データ アプリケーションにログインします。</span><span class="sxs-lookup"><span data-stu-id="46e80-106">Sign in to your local business data application by using one of the following roles:</span></span>

    * <span data-ttu-id="46e80-107">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="46e80-107">Electronic reporting developer</span></span>
    * <span data-ttu-id="46e80-108">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="46e80-108">Electronic reporting functional consultant</span></span>
    * <span data-ttu-id="46e80-109">システム管理者</span><span class="sxs-lookup"><span data-stu-id="46e80-109">System administrator</span></span>

2. <span data-ttu-id="46e80-110">**組織管理** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="46e80-110">Go to **Organization administration** > **Electronic reporting**.</span></span>
3. <span data-ttu-id="46e80-111">**コンフィギュレーション プロバイダー** セクションで、会社に関連付けられている ER プロバイダーのカードを選択します。</span><span class="sxs-lookup"><span data-stu-id="46e80-111">In the **Configuration providers** section, select the card for the ER provider that is associated with your company.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46e80-112">新しい ER ソリューション プロバイダを登録する方法については、**構成プロバイダーを作成し、アクティブとしてマークする<** タスク ガイドを再生してください。</span><span class="sxs-lookup"><span data-stu-id="46e80-112">To learn how to register a new ER solution provider, play the **Create a configuration provider and mark it as active** task guide.</span></span>

4. <span data-ttu-id="46e80-113">選択したタイルで、**リポジトリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="46e80-113">On the selected tile, click **Repositories**.</span></span>

    ![ER プロバイダー タブのリポジトリ ボタン](media/ger-providers-tiles.png)

5. <span data-ttu-id="46e80-115">**コンフィギュレーション リポジトリ**ページのグリッドで、**ファイル システム**タイプの既存のリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="46e80-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **File system** type.</span></span> <span data-ttu-id="46e80-116">このリポジトリがグリッドに表示されない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="46e80-116">If the repository doesn't appear in the grid, follow these steps:</span></span>

   1. <span data-ttu-id="46e80-117">**追加**をクリックして新しいリポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="46e80-117">Click **Add** to add a new repository.</span></span>
   2. <span data-ttu-id="46e80-118">リポジトリ タイプとして、**FILE SYSTEM** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46e80-118">Select **FILE SYSTEM** as the repository type.</span></span>
   3. <span data-ttu-id="46e80-119">**リポジトリの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="46e80-119">Click **Create repository**.</span></span>
   4. <span data-ttu-id="46e80-120">リポジトリの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="46e80-120">Enter a name and description for the repository.</span></span>
   5. <span data-ttu-id="46e80-121">レポジトリの作業ディレクトリのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="46e80-121">Enter the path of the working directory for this repository.</span></span> <span data-ttu-id="46e80-122">このパスは、リポジトリに属する ER 構成が格納されるローカル ファイル システムのフォルダーを指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="46e80-122">This path should point to a folder of the local file system where the ER configurations that belong to the repository will be stored.</span></span>
   6. <span data-ttu-id="46e80-123">**OK** をクリックして、新しいリポジトリを確認および保存します。</span><span class="sxs-lookup"><span data-stu-id="46e80-123">Click **OK** to confirm and save the new repository.</span></span>
   7. <span data-ttu-id="46e80-124">グリッドで、**ファイル システム** タイプの新しいリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="46e80-124">In the grid, select the new repository of the **File system** type.</span></span>

      ![グリッドのファイル システム タイプのリポジトリ](media/ger-file-repository.png)

6. <span data-ttu-id="46e80-126">ブラウザーで、別のタブを開き、LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="46e80-126">In your browser, open another tab, and sign in to LCS.</span></span>
7. <span data-ttu-id="46e80-127">共有アセット ライブラリで、**GER コンフィギュレーション** アセット タイプを選択してから**すべてダウンロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="46e80-127">In the Shared asset library, select the **GER Configuration** asset type, and then click **Download all**.</span></span>

    ![共有アセット ライブラリで全てのボタンをダウンロード](media/ger-lcs-shared-asset-library.png)
    
    > [!NOTE]
    > <span data-ttu-id="46e80-129">すべての ER コンフィギュレーションはダウンロードのため ZIP ファイルに入れられます。</span><span class="sxs-lookup"><span data-stu-id="46e80-129">All the ER configurations will be put into a zip file for download.</span></span>
    
8. <span data-ttu-id="46e80-130">ファイルを開いて、すべての ER コンフィギュレーションを選択し、**ファイル システム**タイプのリポジトリの作業ディレクトリにコピーします。</span><span class="sxs-lookup"><span data-stu-id="46e80-130">Open the file, select all the ER configurations, and then copy them to the working directory for the repository of the **File system** type.</span></span>
9. <span data-ttu-id="46e80-131">**ER リポジトリ**ページの、**Dynamics 365 for Finance and Operations** タブで、**開始**をクリックして、選択されたポジトリの ER コンフィギュレーションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="46e80-131">On the **ER repositories** page, on the **Dynamics 365 for Finance and Operations** tab, click **Open** to view the list of ER configurations for the selected repository.</span></span>
10. <span data-ttu-id="46e80-132">左ウィンドウの**コンフィギュレーション** ツリーで、ER コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="46e80-132">In the **Configurations** tree in the left pane, select an ER configuration.</span></span>
11. <span data-ttu-id="46e80-133">**バージョン**クイック タブで、ER コンフィギュレーションの必要なバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="46e80-133">On the **Versions** FastTab, select the required version of the ER configuration.</span></span>
12. <span data-ttu-id="46e80-134">**インポート**をクリックして、このリポジトリから現在のインスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="46e80-134">Click **Import** to download the selected version from this repository to the current instance.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="46e80-135">**インポート** ボタンは、既存の ER コンフィギュレーション バージョンには使用できません。</span><span class="sxs-lookup"><span data-stu-id="46e80-135">The **Import** button is unavailable for existing ER configuration versions.</span></span> 

> [!NOTE]
> <span data-ttu-id="46e80-136">ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。</span><span class="sxs-lookup"><span data-stu-id="46e80-136">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="46e80-137">不整合または問題が検出されると、通知を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="46e80-137">You might be notified about inconsistencies or issues that are discovered.</span></span> <span data-ttu-id="46e80-138">インポートしたコンフィギュレーションのバージョンを使用する前に、こうした不整合や問題を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46e80-138">You must resolve these inconsistencies or issues before you can use the imported configuration version.</span></span> 

## <a name="frequently-asked-questions"></a><span data-ttu-id="46e80-139">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="46e80-139">Frequently asked questions</span></span>

<span data-ttu-id="46e80-140">**質問:** 共有アセット ライブラリで**すべてダウンロード**をクリックすると、次の警告が表示されます: Zip の生成が進行中です。数分後にもう一度お試しください。</span><span class="sxs-lookup"><span data-stu-id="46e80-140">**Question:** When I click **Download all** in the Shared asset library, I receive the following warning: “Zip generation is in progress, please try again in a few minutes.”</span></span> <span data-ttu-id="46e80-141">なぜこの警告を受信するのですか。</span><span class="sxs-lookup"><span data-stu-id="46e80-141">Why do I receive this warning?</span></span>

<span data-ttu-id="46e80-142">**回答:** これは、新しいコンフィギュレーションが共有アセット ライブラリに追加され、ER コンフィギュレーションがアーカイブされているため、この警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="46e80-142">**Answer:** You receive this warning because a new configuration is added to the Shared asset library, and the ER configuration is being archived.</span></span>

