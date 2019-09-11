---
title: 着荷の概要プロファイルの設定
description: このトピックでは、着荷の概要プロファイルの設定を中心に説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c6bcbb71f52e0ec5f979f8d79c896d10689a1b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867234"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="60756-103">着荷の概要プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="60756-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60756-104">このトピックでは、着荷の概要プロファイルの設定を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="60756-104">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="60756-105">着荷の概要プロファイルは、ユーザーが [着荷の概要] ページを開いた際に適用されるルールのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="60756-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="60756-106">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="60756-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="60756-107">通常、この手順を実施するのは、入荷係です。</span><span class="sxs-lookup"><span data-stu-id="60756-107">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="60756-108">ナビゲーションウィンドウで、**モジュール > 在庫管理 > セットアップ > 配送 > 着荷の概要プロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="60756-108">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="60756-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-109">Select **New**.</span></span> <span data-ttu-id="60756-110">トラックに満載の積荷を降ろす作業を同じ倉庫でほとんど行う場合、入庫登録のプロセスを簡略化するために着荷の概要プロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60756-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="60756-111">**着荷の概要プロファイル名**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60756-111">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="60756-112">**明細行の表示**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-112">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="60756-113">領収書に表示する明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-113">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="60756-114">**すべて** – ステータスに関係なく、すべての明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="60756-114">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="60756-115">**処理中** – 処理が完了または部分的である領収書の明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="60756-115">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="60756-116">これは、各明細行のすべての、あるいは一部の数量が着荷仕訳帳に登録されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="60756-116">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="60756-117">**未完了** – 処理がなし、または部分的である領収書の明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="60756-117">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="60756-118">これらは、着荷仕訳帳に各明細行がまったく登録されていないか、その一部だけが登録されている状態を表します。</span><span class="sxs-lookup"><span data-stu-id="60756-118">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="60756-119">**着荷オプション** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="60756-119">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="60756-120">**繰越日数**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60756-120">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="60756-121">これは、これから数日間 (設定した日数によります) の内に入庫すると予定されている入庫の明細行を表示するフィルターを設定します 。</span><span class="sxs-lookup"><span data-stu-id="60756-121">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="60756-122">**遡及日数**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60756-122">In the **Days back** field, type a value.</span></span> <span data-ttu-id="60756-123">これは、今日より前の数日に入庫すると予定されている入庫の明細行を表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="60756-123">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="60756-124">**倉庫**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60756-124">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="60756-125">1 つ以上の倉庫にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="60756-125">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="60756-126">**荷渡方法**フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-126">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="60756-127">この荷渡方法の入庫明細行のみを表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="60756-127">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="60756-128">**名前**フィールドで WHS を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-128">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="60756-129">**倉庫**フィールドで、倉庫 24 を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-129">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="60756-130">これは、このプロファイルを使用する登録済明細行に使用される既定の倉庫です。</span><span class="sxs-lookup"><span data-stu-id="60756-130">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="60756-131">**場所**フィールドで、**ベイドア**を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-131">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="60756-132">これは、このプロファイルを使用する登録済明細行に使用される既定の保管場所です。</span><span class="sxs-lookup"><span data-stu-id="60756-132">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="60756-133">**着荷クエリの詳細**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="60756-133">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="60756-134">**サイトに制限**フィールドで、サイト 2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-134">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="60756-135">このサイトの入庫明細行のみを表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="60756-135">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="60756-136">**発注書**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="60756-136">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="60756-137">発注書から明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-137">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="60756-138">**移動**オーダー オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="60756-138">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="60756-139">移動オーダーから明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-139">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="60756-140">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="60756-140">Select **Save**.</span></span>
18. <span data-ttu-id="60756-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="60756-141">Close the page.</span></span>

