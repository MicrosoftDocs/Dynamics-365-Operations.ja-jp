---
title: 着荷の概要プロファイルの設定
description: このトピックでは、着荷の概要プロファイルの設定を中心に説明します。
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ecfe132d9b0e096c5fdf015f80a6efb34c9b178
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961435"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="364d2-103">着荷の概要プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="364d2-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="364d2-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="364d2-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="364d2-105">このトピックでは、着荷の概要プロファイルの設定を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="364d2-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="364d2-106">着荷の概要プロファイルは、ユーザーが [着荷の概要] ページを開いた際に適用されるルールのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="364d2-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="364d2-107">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="364d2-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="364d2-108">通常、この手順を実施するのは、入荷係です。</span><span class="sxs-lookup"><span data-stu-id="364d2-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="364d2-109">ナビゲーションウィンドウで、**モジュール > 在庫管理 > セットアップ > 配送 > 着荷の概要プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="364d2-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="364d2-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-110">Select **New**.</span></span> <span data-ttu-id="364d2-111">トラックに満載の積荷を降ろす作業を同じ倉庫でほとんど行う場合、入庫登録のプロセスを簡略化するために着荷の概要プロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="364d2-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="364d2-112">**着荷の概要プロファイル名** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="364d2-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="364d2-113">**明細行の表示** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="364d2-114">領収書に表示する明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="364d2-115">**すべて** – ステータスに関係なく、すべての明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="364d2-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="364d2-116">**処理中** – 処理が完了または部分的である領収書の明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="364d2-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="364d2-117">これは、各明細行のすべての、あるいは一部の数量が着荷仕訳帳に登録されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="364d2-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="364d2-118">**未完了** – 処理がなし、または部分的である領収書の明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="364d2-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="364d2-119">これらは、着荷仕訳帳に各明細行がまったく登録されていないか、その一部だけが登録されている状態を表します。</span><span class="sxs-lookup"><span data-stu-id="364d2-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="364d2-120">**着荷オプション** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="364d2-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="364d2-121">**繰越日数** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="364d2-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="364d2-122">これは、これから数日間 (設定した日数によります) の内に入庫すると予定されている入庫の明細行を表示するフィルターを設定します 。</span><span class="sxs-lookup"><span data-stu-id="364d2-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="364d2-123">**遡及日数** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="364d2-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="364d2-124">これは、今日より前の数日に入庫すると予定されている入庫の明細行を表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="364d2-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="364d2-125">**倉庫** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="364d2-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="364d2-126">1 つ以上の倉庫にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="364d2-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="364d2-127">**荷渡方法** フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="364d2-128">この荷渡方法の入庫明細行のみを表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="364d2-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="364d2-129">**名前** フィールドで WHS を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="364d2-130">**倉庫** フィールドで、倉庫 24 を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="364d2-131">これは、このプロファイルを使用する登録済明細行に使用される既定の倉庫です。</span><span class="sxs-lookup"><span data-stu-id="364d2-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="364d2-132">**場所** フィールドで、**ベイドア** を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="364d2-133">これは、このプロファイルを使用する登録済明細行に使用される既定の保管場所です。</span><span class="sxs-lookup"><span data-stu-id="364d2-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="364d2-134">**着荷クエリの詳細** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="364d2-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="364d2-135">**サイトに制限** フィールドで、サイト 2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="364d2-136">このサイトの入庫明細行のみを表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="364d2-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="364d2-137">**発注書** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="364d2-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="364d2-138">発注書から明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="364d2-139">**移動** オーダー オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="364d2-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="364d2-140">移動オーダーから明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="364d2-141">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="364d2-141">Select **Save**.</span></span>
18. <span data-ttu-id="364d2-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="364d2-142">Close the page.</span></span>

