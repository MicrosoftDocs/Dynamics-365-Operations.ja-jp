--- 
title: "資産のアイドル期間の定義および減価償却プロセスの検証"
description: "このタスクでは、固定資産のアイドル期間の定義について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters, AssetIdlePeriodAssign_JP, AssetTable, AssetBook, AssetIdlePeriodUpdate_JP, AssetProfile, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 70867f19f405e202e44505a2e932e9c35ca550de
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="define-asset-idle-period-and-validate-depreciation-process"></a><span data-ttu-id="e26ee-103">資産のアイドル期間の定義および減価償却プロセスの検証</span><span class="sxs-lookup"><span data-stu-id="e26ee-103">Define asset idle period and validate depreciation process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e26ee-104">このタスクでは、固定資産のアイドル期間の定義について説明します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-104">Use this task to learn how to define fixed asset idle period.</span></span> 

<span data-ttu-id="e26ee-105">プロファイルまたは提案を検証します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-105">Validate profile and proposal.</span></span>



<span data-ttu-id="e26ee-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e26ee-106">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="e26ee-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-107">This task uses the JPMF demo company data.</span></span>


## <a name="assign-number-sequence-in-fa-parameter-form"></a><span data-ttu-id="e26ee-108">FA パラメーター フォームの番号順序の割り当て</span><span class="sxs-lookup"><span data-stu-id="e26ee-108">Assign number sequence in FA parameter form</span></span>
1. <span data-ttu-id="e26ee-109">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-109">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="e26ee-110">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-110">Click the Number sequences tab.</span></span>
3. <span data-ttu-id="e26ee-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e26ee-112">照会 = 固定資産のアイドル期間</span><span class="sxs-lookup"><span data-stu-id="e26ee-112">Reference = Fixed asset idle period</span></span>  
4. <span data-ttu-id="e26ee-113">[番号順序コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-113">In the Number sequence code field, enter or select a value.</span></span>
5. <span data-ttu-id="e26ee-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-114">Click Save.</span></span>
6. <span data-ttu-id="e26ee-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e26ee-115">Close the page.</span></span>

## <a name="assign-idle-period-for-a-fixed-asset"></a><span data-ttu-id="e26ee-116">固定資産のアイドル期間の割り当て</span><span class="sxs-lookup"><span data-stu-id="e26ee-116">Assign idle period for a Fixed asset</span></span>
1. <span data-ttu-id="e26ee-117">[固定資産] > [定期処理のタスク] > [固定資産へのアイドル期間の割り当て] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-117">Go to Fixed assets > Periodic tasks > Assign idle period to a fixed asset.</span></span>
2. <span data-ttu-id="e26ee-118">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-118">Click New.</span></span>
3. <span data-ttu-id="e26ee-119">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-119">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e26ee-120">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-120">Expand the General section.</span></span>
5. <span data-ttu-id="e26ee-121">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-121">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="e26ee-122">開始日 = 01/01/2016</span><span class="sxs-lookup"><span data-stu-id="e26ee-122">From date = 01/01/2016</span></span>  
6. <span data-ttu-id="e26ee-123">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-123">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e26ee-124">終了日 = 12/31/2017</span><span class="sxs-lookup"><span data-stu-id="e26ee-124">To date = 12/31/2017</span></span>  
7. <span data-ttu-id="e26ee-125">[理由] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-125">In the Reason field, type a value.</span></span>
8. <span data-ttu-id="e26ee-126">[アイドル期間] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-126">Expand the Idle Periods section.</span></span>
9. <span data-ttu-id="e26ee-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-127">Click New.</span></span>
10. <span data-ttu-id="e26ee-128">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-128">In the Fixed asset group field, enter or select a value.</span></span>
    * <span data-ttu-id="e26ee-129">EQUP-M</span><span class="sxs-lookup"><span data-stu-id="e26ee-129">EQUP-M</span></span>  
11. <span data-ttu-id="e26ee-130">[固定資産番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-130">In the Fixed asset number field, enter or select a value.</span></span>
    * <span data-ttu-id="e26ee-131">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="e26ee-131">EQUPM-000024</span></span>  
12. <span data-ttu-id="e26ee-132">[帳簿] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-132">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="e26ee-133">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="e26ee-133">200NDB_CUR</span></span>  
13. <span data-ttu-id="e26ee-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-134">Click Save.</span></span>
14. <span data-ttu-id="e26ee-135">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-135">Click Confirm.</span></span>
15. <span data-ttu-id="e26ee-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e26ee-136">Close the page.</span></span>

## <a name="validate-fixed-asset-book"></a><span data-ttu-id="e26ee-137">[固定資産帳簿] の検証</span><span class="sxs-lookup"><span data-stu-id="e26ee-137">Validate Fixed asset book</span></span>
1. <span data-ttu-id="e26ee-138">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-138">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="e26ee-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-139">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e26ee-140">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="e26ee-140">EQUPM-000024</span></span>  
3. <span data-ttu-id="e26ee-141">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-141">Click Books.</span></span>
4. <span data-ttu-id="e26ee-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-142">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e26ee-143">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="e26ee-143">200NDB_CUR</span></span>  
5. <span data-ttu-id="e26ee-144">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-144">Click Functions.</span></span>
6. <span data-ttu-id="e26ee-145">[アイドル期間の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-145">Click Update idle periods.</span></span>
    * <span data-ttu-id="e26ee-146">固定資産帳簿に対して作成されたアイドル期間の検証が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="e26ee-146">Validate the idle period created for the fixed asset book is listed</span></span>  
7. <span data-ttu-id="e26ee-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e26ee-147">Close the page.</span></span>
8. <span data-ttu-id="e26ee-148">[プロファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-148">Click Profile.</span></span>
    * <span data-ttu-id="e26ee-149">アイドル期間に対する減価償却がゼロと表示されるプロファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-149">Validate the profile displays zero depreciation for the idle period</span></span>  
9. <span data-ttu-id="e26ee-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e26ee-150">Close the page.</span></span>
10. <span data-ttu-id="e26ee-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e26ee-151">Close the page.</span></span>
11. <span data-ttu-id="e26ee-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e26ee-152">Close the page.</span></span>

## <a name="execute-depreciation-proposal"></a><span data-ttu-id="e26ee-153">償却提案の実行</span><span class="sxs-lookup"><span data-stu-id="e26ee-153">Execute depreciation proposal</span></span>
1. <span data-ttu-id="e26ee-154">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-154">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="e26ee-155">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-155">Click New.</span></span>
3. <span data-ttu-id="e26ee-156">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-156">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="e26ee-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-157">Click Save.</span></span>
5. <span data-ttu-id="e26ee-158">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-158">Click Lines.</span></span>
6. <span data-ttu-id="e26ee-159">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-159">Click Proposals.</span></span>
7. <span data-ttu-id="e26ee-160">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-160">Click Depreciation proposal.</span></span>
8. <span data-ttu-id="e26ee-161">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-161">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e26ee-162">終了日 = 12/31/2017</span><span class="sxs-lookup"><span data-stu-id="e26ee-162">To date = 12/31/2017</span></span>  
9. <span data-ttu-id="e26ee-163">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-163">Expand the Records to include section.</span></span>
10. <span data-ttu-id="e26ee-164">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-164">Click Filter.</span></span>
11. <span data-ttu-id="e26ee-165">[リセット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-165">Click Reset.</span></span>
12. <span data-ttu-id="e26ee-166">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-166">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e26ee-167">フィールド = 固定資産番号</span><span class="sxs-lookup"><span data-stu-id="e26ee-167">Field = Fixed asset number</span></span>  
13. <span data-ttu-id="e26ee-168">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-168">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="e26ee-169">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="e26ee-169">EQUPM-000024</span></span>  
14. <span data-ttu-id="e26ee-170">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-170">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e26ee-171">フィールド = 予約</span><span class="sxs-lookup"><span data-stu-id="e26ee-171">Field = Book</span></span>  
15. <span data-ttu-id="e26ee-172">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e26ee-172">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="e26ee-173">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="e26ee-173">200NDB_CUR</span></span>  
16. <span data-ttu-id="e26ee-174">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-174">Click OK.</span></span>
17. <span data-ttu-id="e26ee-175">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e26ee-175">Click OK.</span></span>
    * <span data-ttu-id="e26ee-176">アイドル期間に対して作成された特別償却の仕訳帳は検証なし</span><span class="sxs-lookup"><span data-stu-id="e26ee-176">Validate no depreciation journal is created for the idle period</span></span>  


