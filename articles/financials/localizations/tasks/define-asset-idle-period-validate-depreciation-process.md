--- 
title: "資産のアイドル期間の定義および減価償却プロセスの検証 (日本)"
description: "このタスクでは、固定資産のアイドル期間の定義について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 70a57144c612d962c1067b7cc691e211f548b0d0
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="define-asset-idle-period-and-validate-depreciation-process-japan"></a><span data-ttu-id="62a4b-103">資産のアイドル期間の定義および減価償却プロセスの検証 (日本)</span><span class="sxs-lookup"><span data-stu-id="62a4b-103">Define asset idle period and validate depreciation process (Japan)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62a4b-104">このタスクでは、固定資産のアイドル期間の定義について説明します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-104">Use this task to learn how to define fixed asset idle period.</span></span> 

<span data-ttu-id="62a4b-105">プロファイルまたは提案を検証します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-105">Validate profile and proposal.</span></span>



<span data-ttu-id="62a4b-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62a4b-106">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="62a4b-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-107">This task uses the JPMF demo company data.</span></span>


## <a name="assign-number-sequence-in-fa-parameter-form"></a><span data-ttu-id="62a4b-108">FA パラメーター フォームの番号順序の割り当て</span><span class="sxs-lookup"><span data-stu-id="62a4b-108">Assign number sequence in FA parameter form</span></span>
1. <span data-ttu-id="62a4b-109">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-109">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="62a4b-110">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-110">Click the Number sequences tab.</span></span>
3. <span data-ttu-id="62a4b-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="62a4b-112">照会 = 固定資産のアイドル期間</span><span class="sxs-lookup"><span data-stu-id="62a4b-112">Reference = Fixed asset idle period</span></span>  
4. <span data-ttu-id="62a4b-113">[番号順序コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-113">In the Number sequence code field, enter or select a value.</span></span>
5. <span data-ttu-id="62a4b-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-114">Click Save.</span></span>
6. <span data-ttu-id="62a4b-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62a4b-115">Close the page.</span></span>

## <a name="assign-idle-period-for-a-fixed-asset"></a><span data-ttu-id="62a4b-116">固定資産のアイドル期間の割り当て</span><span class="sxs-lookup"><span data-stu-id="62a4b-116">Assign idle period for a Fixed asset</span></span>
1. <span data-ttu-id="62a4b-117">[固定資産] > [定期処理のタスク] > [固定資産へのアイドル期間の割り当て] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-117">Go to Fixed assets > Periodic tasks > Assign idle period to a fixed asset.</span></span>
2. <span data-ttu-id="62a4b-118">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-118">Click New.</span></span>
3. <span data-ttu-id="62a4b-119">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-119">In the Description field, type a value.</span></span>
4. <span data-ttu-id="62a4b-120">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-120">Expand the General section.</span></span>
5. <span data-ttu-id="62a4b-121">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-121">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="62a4b-122">開始日 = 01/01/2016</span><span class="sxs-lookup"><span data-stu-id="62a4b-122">From date = 01/01/2016</span></span>  
6. <span data-ttu-id="62a4b-123">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-123">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="62a4b-124">終了日 = 12/31/2017</span><span class="sxs-lookup"><span data-stu-id="62a4b-124">To date = 12/31/2017</span></span>  
7. <span data-ttu-id="62a4b-125">[理由] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-125">In the Reason field, type a value.</span></span>
8. <span data-ttu-id="62a4b-126">[アイドル期間] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-126">Expand the Idle Periods section.</span></span>
9. <span data-ttu-id="62a4b-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-127">Click New.</span></span>
10. <span data-ttu-id="62a4b-128">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-128">In the Fixed asset group field, enter or select a value.</span></span>
    * <span data-ttu-id="62a4b-129">EQUP-M</span><span class="sxs-lookup"><span data-stu-id="62a4b-129">EQUP-M</span></span>  
11. <span data-ttu-id="62a4b-130">[固定資産番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-130">In the Fixed asset number field, enter or select a value.</span></span>
    * <span data-ttu-id="62a4b-131">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="62a4b-131">EQUPM-000024</span></span>  
12. <span data-ttu-id="62a4b-132">[帳簿] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-132">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="62a4b-133">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="62a4b-133">200NDB_CUR</span></span>  
13. <span data-ttu-id="62a4b-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-134">Click Save.</span></span>
14. <span data-ttu-id="62a4b-135">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-135">Click Confirm.</span></span>
15. <span data-ttu-id="62a4b-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62a4b-136">Close the page.</span></span>

## <a name="validate-fixed-asset-book"></a><span data-ttu-id="62a4b-137">[固定資産帳簿] の検証</span><span class="sxs-lookup"><span data-stu-id="62a4b-137">Validate Fixed asset book</span></span>
1. <span data-ttu-id="62a4b-138">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-138">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="62a4b-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-139">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="62a4b-140">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="62a4b-140">EQUPM-000024</span></span>  
3. <span data-ttu-id="62a4b-141">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-141">Click Books.</span></span>
4. <span data-ttu-id="62a4b-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-142">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="62a4b-143">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="62a4b-143">200NDB_CUR</span></span>  
5. <span data-ttu-id="62a4b-144">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-144">Click Functions.</span></span>
6. <span data-ttu-id="62a4b-145">[アイドル期間の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-145">Click Update idle periods.</span></span>
    * <span data-ttu-id="62a4b-146">固定資産帳簿に対して作成されたアイドル期間の検証が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="62a4b-146">Validate the idle period created for the fixed asset book is listed</span></span>  
7. <span data-ttu-id="62a4b-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62a4b-147">Close the page.</span></span>
8. <span data-ttu-id="62a4b-148">[プロファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-148">Click Profile.</span></span>
    * <span data-ttu-id="62a4b-149">アイドル期間に対する減価償却がゼロと表示されるプロファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-149">Validate the profile displays zero depreciation for the idle period</span></span>  
9. <span data-ttu-id="62a4b-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62a4b-150">Close the page.</span></span>
10. <span data-ttu-id="62a4b-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62a4b-151">Close the page.</span></span>
11. <span data-ttu-id="62a4b-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62a4b-152">Close the page.</span></span>

## <a name="execute-depreciation-proposal"></a><span data-ttu-id="62a4b-153">償却提案の実行</span><span class="sxs-lookup"><span data-stu-id="62a4b-153">Execute depreciation proposal</span></span>
1. <span data-ttu-id="62a4b-154">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-154">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="62a4b-155">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-155">Click New.</span></span>
3. <span data-ttu-id="62a4b-156">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-156">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="62a4b-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-157">Click Save.</span></span>
5. <span data-ttu-id="62a4b-158">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-158">Click Lines.</span></span>
6. <span data-ttu-id="62a4b-159">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-159">Click Proposals.</span></span>
7. <span data-ttu-id="62a4b-160">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-160">Click Depreciation proposal.</span></span>
8. <span data-ttu-id="62a4b-161">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-161">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="62a4b-162">終了日 = 12/31/2017</span><span class="sxs-lookup"><span data-stu-id="62a4b-162">To date = 12/31/2017</span></span>  
9. <span data-ttu-id="62a4b-163">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-163">Expand the Records to include section.</span></span>
10. <span data-ttu-id="62a4b-164">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-164">Click Filter.</span></span>
11. <span data-ttu-id="62a4b-165">[リセット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-165">Click Reset.</span></span>
12. <span data-ttu-id="62a4b-166">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-166">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="62a4b-167">フィールド = 固定資産番号</span><span class="sxs-lookup"><span data-stu-id="62a4b-167">Field = Fixed asset number</span></span>  
13. <span data-ttu-id="62a4b-168">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-168">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="62a4b-169">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="62a4b-169">EQUPM-000024</span></span>  
14. <span data-ttu-id="62a4b-170">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-170">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="62a4b-171">フィールド = 予約</span><span class="sxs-lookup"><span data-stu-id="62a4b-171">Field = Book</span></span>  
15. <span data-ttu-id="62a4b-172">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="62a4b-172">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="62a4b-173">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="62a4b-173">200NDB_CUR</span></span>  
16. <span data-ttu-id="62a4b-174">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-174">Click OK.</span></span>
17. <span data-ttu-id="62a4b-175">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62a4b-175">Click OK.</span></span>
    * <span data-ttu-id="62a4b-176">アイドル期間に対して作成された特別償却の仕訳帳は検証なし</span><span class="sxs-lookup"><span data-stu-id="62a4b-176">Validate no depreciation journal is created for the idle period</span></span>  


