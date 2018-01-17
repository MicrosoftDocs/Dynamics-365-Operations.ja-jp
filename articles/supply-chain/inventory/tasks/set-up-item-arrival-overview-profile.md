---
title: "着荷の概要プロファイルの設定"
description: "このタスクでは、着荷の概要プロファイルの設定を中心に説明します。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d4248882608a3d1e23c8c9e9dc8069caaa8352c2
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="eccb4-103">着荷の概要プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="eccb4-103">Set up an item arrival overview profile</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eccb4-104">このタスクでは、着荷の概要プロファイルの設定を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="eccb4-105">着荷の概要プロファイルは、ユーザーが [着荷の概要] ページを開いた際に適用されるルールのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="eccb4-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="eccb4-106">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="eccb4-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="eccb4-107">通常、この手順を実施するのは、入荷係です。</span><span class="sxs-lookup"><span data-stu-id="eccb4-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="eccb4-108">[在庫管理] > [設定] > [配送] > [着荷の概要プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="eccb4-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eccb4-109">Click New.</span></span>
    * <span data-ttu-id="eccb4-110">トラックに満載の積荷を降ろす作業を同じ倉庫でほとんど行う場合、入庫登録のプロセスを簡略化するために着荷の概要プロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eccb4-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="eccb4-111">[着荷の概要プロファイル名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="eccb4-112">[明細行の表示] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="eccb4-113">表示する領収書の明細行を選択: [すべて] – 状態にかかわらずすべての明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="eccb4-114">[処理中] – 処理が [完了] または [部分的] である領収書の明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="eccb4-115">これは、各明細行のすべての、あるいは一部の数量が着荷仕訳帳に登録されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="eccb4-116">[未完了] – 処理が [なし] または [部分的] である領収書の明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="eccb4-117">これらは、着荷仕訳帳に各明細行がまったく登録されていないか、その一部だけが登録されている状態を表します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="eccb4-118">[着荷オプション] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="eccb4-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="eccb4-119">[繰越日数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="eccb4-120">これは、これから数日間 (設定した日数によります) の内に入庫すると予定されている入庫の明細行を表示するフィルターを設定します 。</span><span class="sxs-lookup"><span data-stu-id="eccb4-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="eccb4-121">[遡及日数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="eccb4-122">これは、今日より前の数日に入庫すると予定されている入庫の明細行を表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="eccb4-123">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="eccb4-124">1 つ以上の倉庫にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="eccb4-125">[荷渡方法] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="eccb4-126">この荷渡方法の入庫明細行のみを表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="eccb4-127">[名前] フィールドで [WHS] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="eccb4-128">[倉庫] フィールドで、倉庫 24 を選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="eccb4-129">これは、このプロファイルを使用する登録済明細行に使用される既定の倉庫です。</span><span class="sxs-lookup"><span data-stu-id="eccb4-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="eccb4-130">[場所] フィールドで、[ベイドア] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="eccb4-131">これは、このプロファイルを使用する登録済明細行に使用される既定の保管場所です。</span><span class="sxs-lookup"><span data-stu-id="eccb4-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="eccb4-132">[着荷クエリの詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="eccb4-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="eccb4-133">[サイトに制限] フィールドで、サイト 2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="eccb4-134">このサイトの入庫明細行のみを表示するフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="eccb4-135">[発注書] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="eccb4-136">発注書から明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="eccb4-137">[移動オーダー] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="eccb4-138">移動オーダーから明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="eccb4-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="eccb4-139">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eccb4-139">Click Save.</span></span>
18. <span data-ttu-id="eccb4-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eccb4-140">Close the page.</span></span>

