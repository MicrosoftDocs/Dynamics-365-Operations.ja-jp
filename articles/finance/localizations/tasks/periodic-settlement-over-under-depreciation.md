---
title: 償却超過額/償却不足額の定期決済
description: このタスクでは、損金の減価償却費を計算および記録する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm, AssetDepPreTaxDedProcess_JP, AssetDepPreTaxDedProcessDetail_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcfa65881aee2ef1d9bd6e04d5c6b398cfc6e4c6
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981622"
---
# <a name="periodic-settlement-of-over-and-under-depreciation"></a><span data-ttu-id="dbed0-103">償却超過額/償却不足額の定期決済</span><span class="sxs-lookup"><span data-stu-id="dbed0-103">Periodic settlement of over and under depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbed0-104">このタスクでは、損金の減価償却費を計算および記録する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-104">Use this task to learn how to calculate and record depreciation expense for deductible expense.</span></span>



<span data-ttu-id="dbed0-105">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-105">This task uses the JPMF demo company data.</span></span>




## <a name="fixed-asset-depreciation"></a><span data-ttu-id="dbed0-106">固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="dbed0-106">Fixed asset depreciation</span></span>
1. <span data-ttu-id="dbed0-107">次の順に移動します: [固定資産] ></span><span class="sxs-lookup"><span data-stu-id="dbed0-107">Go to Fixed assets > ..</span></span> <span data-ttu-id="dbed0-108">> [固定資産仕訳帳]。</span><span class="sxs-lookup"><span data-stu-id="dbed0-108">> Fixed assets journal.</span></span>
2. <span data-ttu-id="dbed0-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-109">Click New.</span></span>
3. <span data-ttu-id="dbed0-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="dbed0-111">例: FAD</span><span class="sxs-lookup"><span data-stu-id="dbed0-111">Example: FAD</span></span>  
4. <span data-ttu-id="dbed0-112">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-112">Click Lines.</span></span>
5. <span data-ttu-id="dbed0-113">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-113">Click Proposals.</span></span>
6. <span data-ttu-id="dbed0-114">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-114">Click Depreciation proposal.</span></span>
7. <span data-ttu-id="dbed0-115">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-115">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="dbed0-116">例: 3/31/ 2016</span><span class="sxs-lookup"><span data-stu-id="dbed0-116">Example: 3/31/2016</span></span>  
8. <span data-ttu-id="dbed0-117">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-117">Click Filter.</span></span>
9. <span data-ttu-id="dbed0-118">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-118">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="dbed0-119">たとえば、固定資産番号 = BUILM-000005 に設定します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-119">For example, set Fixed asset number = BUILM-000005</span></span>  
10. <span data-ttu-id="dbed0-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-120">Click OK.</span></span>
11. <span data-ttu-id="dbed0-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-121">Click OK.</span></span>
    * <span data-ttu-id="dbed0-122">原価償却仕訳帳が作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-122">Verify that the depreciation journal  was created.</span></span>  
12. <span data-ttu-id="dbed0-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-123">Click Post.</span></span>

## <a name="over-and-under-depr-settlements"></a><span data-ttu-id="dbed0-124">償却超過/償却不足決済</span><span class="sxs-lookup"><span data-stu-id="dbed0-124">Over and under depr settlements</span></span>
1. <span data-ttu-id="dbed0-125">[固定資産] > [定期処理のタスク] > [償却超過/償却不足額の決済] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-125">Go to Fixed assets > Periodic tasks > Settlement of over depreciation or under depreciation amount.</span></span>
2. <span data-ttu-id="dbed0-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-126">Click New.</span></span>
3. <span data-ttu-id="dbed0-127">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-127">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="dbed0-128">例: 03/31/2016</span><span class="sxs-lookup"><span data-stu-id="dbed0-128">Example: 03/31/2016</span></span>  
4. <span data-ttu-id="dbed0-129">[仕訳帳名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-129">In the Journal name field, type a value.</span></span>
    * <span data-ttu-id="dbed0-130">例: FAD_TAX</span><span class="sxs-lookup"><span data-stu-id="dbed0-130">Example: FAD_TAX</span></span>  
5. <span data-ttu-id="dbed0-131">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-131">Expand the Records to include section.</span></span>
6. <span data-ttu-id="dbed0-132">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-132">Click Filter.</span></span>
7. <span data-ttu-id="dbed0-133">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-133">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="dbed0-134">たとえば、固定資産番号 = BUILM-000005 に設定します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-134">For example, set the Fixed asset number = BUILM-000005</span></span>  
8. <span data-ttu-id="dbed0-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-135">Click OK.</span></span>
9. <span data-ttu-id="dbed0-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-136">Click OK.</span></span>
10. <span data-ttu-id="dbed0-137">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-137">Refresh the page.</span></span>
    * <span data-ttu-id="dbed0-138">結果はすぐに表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="dbed0-138">The results may not appear instantly.</span></span> <span data-ttu-id="dbed0-139">更新をクリックして、結果が作成されたか表示します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-139">Click refresh to see if the result is created.</span></span>  
11. <span data-ttu-id="dbed0-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dbed0-141">[ステータス] = [ドラフト] である新しい結果をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-141">Click the new result with Status = Draft.</span></span>  
12. <span data-ttu-id="dbed0-142">[決済結果の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-142">Click View settlement results.</span></span>
    * <span data-ttu-id="dbed0-143">正しい結果が作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dbed0-143">Verify that the correct result is created.</span></span>  
13. <span data-ttu-id="dbed0-144">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbed0-144">Click Post.</span></span>

