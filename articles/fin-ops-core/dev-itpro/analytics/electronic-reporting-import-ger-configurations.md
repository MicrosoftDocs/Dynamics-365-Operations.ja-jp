---
title: 電子申告 (ER) コンフィギュレーションのインポート
description: このトピックでは、Lifecycle Services (LCS) からローカルのビジネス データ アプリケーションに電子申告 (ER) の構成をインポートする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport
audience: Developer
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: 435a3b375a6c6aa67e317f8a42c46e3704f01e19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687142"
---
# <a name="import-electronic-reporting-er-configurations"></a><span data-ttu-id="6b3f5-103">電子申告 (ER) コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="6b3f5-103">Import Electronic reporting (ER) configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b3f5-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) からローカルのビジネス データ アプリケーションに電子申告 (ER) のコンフィギュレーションをダウンロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS) to a local business data application.</span></span> <span data-ttu-id="6b3f5-105">また、ER リポジトリからローカル ビジネス データ (LBD) アプリケーションに ER 構成をアップロードする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-105">It also explains how to upload the ER configurations from an ER repository to the local business data (LBD) application.</span></span>

1. <span data-ttu-id="6b3f5-106">次のロールのいずれかを使用して、ローカル ビジネス データ アプリケーションにログインします。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-106">Sign in to your local business data application by using one of the following roles:</span></span>

    * <span data-ttu-id="6b3f5-107">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="6b3f5-107">Electronic reporting developer</span></span>
    * <span data-ttu-id="6b3f5-108">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="6b3f5-108">Electronic reporting functional consultant</span></span>
    * <span data-ttu-id="6b3f5-109">システム管理者</span><span class="sxs-lookup"><span data-stu-id="6b3f5-109">System administrator</span></span>

2. <span data-ttu-id="6b3f5-110">**組織管理** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-110">Go to **Organization administration** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="6b3f5-111">**コンフィギュレーション プロバイダー** セクションで、会社に関連付けられている ER プロバイダーのカードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-111">In the **Configuration providers** section, select the card for the ER provider that is associated with your company.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b3f5-112">新しい ER ソリューション プロバイダを登録する方法については、**構成プロバイダーを作成し、アクティブとしてマークする<** タスク ガイドを再生してください。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-112">To learn how to register a new ER solution provider, play the **Create a configuration provider and mark it as active** task guide.</span></span>

4. <span data-ttu-id="6b3f5-113">選択したタイルで、**リポジトリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-113">On the selected tile, click **Repositories**.</span></span>


5. <span data-ttu-id="6b3f5-114">**コンフィギュレーション リポジトリ** ページのグリッドで、**ファイル システム** タイプの既存のリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **File system** type.</span></span> <span data-ttu-id="6b3f5-115">このリポジトリがグリッドに表示されない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-115">If the repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="6b3f5-116">**追加** をクリックして新しいリポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="6b3f5-117">リポジトリ タイプとして、**FILE SYSTEM** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-117">Select **FILE SYSTEM** as the repository type.</span></span>
    3. <span data-ttu-id="6b3f5-118">**リポジトリの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="6b3f5-119">リポジトリの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-119">Enter a name and description for the repository.</span></span>
    5. <span data-ttu-id="6b3f5-120">レポジトリの作業ディレクトリのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-120">Enter the path of the working directory for this repository.</span></span> <span data-ttu-id="6b3f5-121">このパスは、リポジトリに属する ER 構成が格納されるローカル ファイル システムのフォルダーを指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-121">This path should point to a folder of the local file system where the ER configurations that belong to the repository will be stored.</span></span>
    6. <span data-ttu-id="6b3f5-122">**OK** をクリックして、新しいリポジトリを確認および保存します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-122">Click **OK** to confirm and save the new repository.</span></span>
    7. <span data-ttu-id="6b3f5-123">グリッドで、**ファイル システム** タイプの新しいリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-123">In the grid, select the new repository of the **File system** type.</span></span>

6. <span data-ttu-id="6b3f5-124">ブラウザーで、別のタブを開き、LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-124">In your browser, open another tab, and sign in to LCS.</span></span>
7. <span data-ttu-id="6b3f5-125">共有アセット ライブラリで、**GER コンフィギュレーション** アセット タイプを選択してから **すべてダウンロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-125">In the Shared asset library, select the **GER Configuration** asset type, and then click **Download all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b3f5-126">すべての ER コンフィギュレーションはダウンロードのため ZIP ファイルに入れられます。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-126">All the ER configurations will be put into a zip file for download.</span></span>

8. <span data-ttu-id="6b3f5-127">ファイルを開いて、すべての ER コンフィギュレーションを選択し、**ファイル システム** タイプのリポジトリの作業ディレクトリにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-127">Open the file, select all the ER configurations, and then copy them to the working directory for the repository of the **File system** type.</span></span>
9. <span data-ttu-id="6b3f5-128">**ER リポジトリ** ページの、**Dynamics 365 for Finance and Operations** タブで、**開く** をクリックして、選択されたリポジトリの ER コンフィギュレーションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-128">On the **ER repositories** page, on the **Dynamics 365 for Finance and Operations** tab, click **Open** to view the list of ER configurations for the selected repository.</span></span>
10. <span data-ttu-id="6b3f5-129">左ウィンドウの **コンフィギュレーション** ツリーで、ER コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-129">In the **Configurations** tree in the left pane, select an ER configuration.</span></span>
11. <span data-ttu-id="6b3f5-130">**バージョン** クイック タブで、ER コンフィギュレーションの必要なバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-130">On the **Versions** FastTab, select the required version of the ER configuration.</span></span>
12. <span data-ttu-id="6b3f5-131">**インポート** をクリックして、このリポジトリから現在のインスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-131">Click **Import** to download the selected version from this repository to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b3f5-132">**インポート** ボタンは、既存の ER コンフィギュレーション バージョンには使用できません。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-132">The **Import** button is unavailable for existing ER configuration versions.</span></span>

> [!NOTE]
> <span data-ttu-id="6b3f5-133">ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-133">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="6b3f5-134">不整合または問題が検出されると、通知を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-134">You might be notified about inconsistencies or issues that are discovered.</span></span> <span data-ttu-id="6b3f5-135">インポートしたコンフィギュレーションのバージョンを使用する前に、こうした不整合や問題を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-135">You must resolve these inconsistencies or issues before you can use the imported configuration version.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6b3f5-136">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="6b3f5-136">Frequently asked questions</span></span>

<span data-ttu-id="6b3f5-137">**質問:** 共有アセット ライブラリで **すべてダウンロード** をクリックすると、次の警告が表示されます: Zip の生成が進行中です。数分後にもう一度お試しください。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-137">**Question:** When I click **Download all** in the Shared asset library, I receive the following warning: “Zip generation is in progress, please try again in a few minutes.”</span></span> <span data-ttu-id="6b3f5-138">なぜこの警告を受信するのですか。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-138">Why do I receive this warning?</span></span>

<span data-ttu-id="6b3f5-139">**回答:** これは、新しいコンフィギュレーションが共有アセット ライブラリに追加され、ER コンフィギュレーションがアーカイブされているため、この警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b3f5-139">**Answer:** You receive this warning because a new configuration is added to the Shared asset library, and the ER configuration is being archived.</span></span>
