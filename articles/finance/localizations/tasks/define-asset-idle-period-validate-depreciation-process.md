---
title: 資産のアイドル期間の定義および減価償却プロセスの検証
description: このタスクでは、固定資産のアイドル期間の定義について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetIdlePeriodAssign_JP, AssetTable, AssetBook, AssetIdlePeriodUpdate_JP, AssetProfile, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3914a2158302ead7ff9561fa5f82843f3d96a4d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408191"
---
# <a name="define-asset-idle-period-and-validate-depreciation-process"></a><span data-ttu-id="5ae3e-103">資産のアイドル期間の定義および減価償却プロセスの検証</span><span class="sxs-lookup"><span data-stu-id="5ae3e-103">Define asset idle period and validate depreciation process</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ae3e-104">このタスクでは、固定資産のアイドル期間の定義について説明します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-104">Use this task to learn how to define fixed asset idle period.</span></span> 

<span data-ttu-id="5ae3e-105">プロファイルまたは提案を検証します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-105">Validate profile and proposal.</span></span>



<span data-ttu-id="5ae3e-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-106">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="5ae3e-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-107">This task uses the JPMF demo company data.</span></span>


## <a name="assign-number-sequence-in-fa-parameter-form"></a><span data-ttu-id="5ae3e-108">FA パラメーター フォームの番号順序の割り当て</span><span class="sxs-lookup"><span data-stu-id="5ae3e-108">Assign number sequence in FA parameter form</span></span>
1. <span data-ttu-id="5ae3e-109">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-109">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="5ae3e-110">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-110">Click the Number sequences tab.</span></span>
3. <span data-ttu-id="5ae3e-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5ae3e-112">照会 = 固定資産のアイドル期間</span><span class="sxs-lookup"><span data-stu-id="5ae3e-112">Reference = Fixed asset idle period</span></span>  
4. <span data-ttu-id="5ae3e-113">[番号順序コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-113">In the Number sequence code field, enter or select a value.</span></span>
5. <span data-ttu-id="5ae3e-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-114">Click Save.</span></span>
6. <span data-ttu-id="5ae3e-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-115">Close the page.</span></span>

## <a name="assign-idle-period-for-a-fixed-asset"></a><span data-ttu-id="5ae3e-116">固定資産のアイドル期間の割り当て</span><span class="sxs-lookup"><span data-stu-id="5ae3e-116">Assign idle period for a Fixed asset</span></span>
1. <span data-ttu-id="5ae3e-117">[固定資産] > [定期処理のタスク] > [固定資産へのアイドル期間の割り当て] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-117">Go to Fixed assets > Periodic tasks > Assign idle period to a fixed asset.</span></span>
2. <span data-ttu-id="5ae3e-118">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-118">Click New.</span></span>
3. <span data-ttu-id="5ae3e-119">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-119">In the Description field, type a value.</span></span>
4. <span data-ttu-id="5ae3e-120">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-120">Expand the General section.</span></span>
5. <span data-ttu-id="5ae3e-121">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-121">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="5ae3e-122">開始日 = 01/01/2016</span><span class="sxs-lookup"><span data-stu-id="5ae3e-122">From date = 01/01/2016</span></span>  
6. <span data-ttu-id="5ae3e-123">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-123">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="5ae3e-124">終了日 = 12/31/2017</span><span class="sxs-lookup"><span data-stu-id="5ae3e-124">To date = 12/31/2017</span></span>  
7. <span data-ttu-id="5ae3e-125">[理由] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-125">In the Reason field, type a value.</span></span>
8. <span data-ttu-id="5ae3e-126">[アイドル期間] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-126">Expand the Idle Periods section.</span></span>
9. <span data-ttu-id="5ae3e-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-127">Click New.</span></span>
10. <span data-ttu-id="5ae3e-128">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-128">In the Fixed asset group field, enter or select a value.</span></span>
    * <span data-ttu-id="5ae3e-129">EQUP-M</span><span class="sxs-lookup"><span data-stu-id="5ae3e-129">EQUP-M</span></span>  
11. <span data-ttu-id="5ae3e-130">[固定資産番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-130">In the Fixed asset number field, enter or select a value.</span></span>
    * <span data-ttu-id="5ae3e-131">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="5ae3e-131">EQUPM-000024</span></span>  
12. <span data-ttu-id="5ae3e-132">[帳簿] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-132">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="5ae3e-133">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="5ae3e-133">200NDB_CUR</span></span>  
13. <span data-ttu-id="5ae3e-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-134">Click Save.</span></span>
14. <span data-ttu-id="5ae3e-135">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-135">Click Confirm.</span></span>
15. <span data-ttu-id="5ae3e-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-136">Close the page.</span></span>

## <a name="validate-fixed-asset-book"></a><span data-ttu-id="5ae3e-137">[固定資産帳簿] の検証</span><span class="sxs-lookup"><span data-stu-id="5ae3e-137">Validate Fixed asset book</span></span>
1. <span data-ttu-id="5ae3e-138">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-138">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="5ae3e-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-139">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5ae3e-140">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="5ae3e-140">EQUPM-000024</span></span>  
3. <span data-ttu-id="5ae3e-141">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-141">Click Books.</span></span>
4. <span data-ttu-id="5ae3e-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-142">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5ae3e-143">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="5ae3e-143">200NDB_CUR</span></span>  
5. <span data-ttu-id="5ae3e-144">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-144">Click Functions.</span></span>
6. <span data-ttu-id="5ae3e-145">[アイドル期間の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-145">Click Update idle periods.</span></span>
    * <span data-ttu-id="5ae3e-146">固定資産帳簿に対して作成されたアイドル期間の検証が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-146">Validate the idle period created for the fixed asset book is listed</span></span>  
7. <span data-ttu-id="5ae3e-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-147">Close the page.</span></span>
8. <span data-ttu-id="5ae3e-148">[プロファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-148">Click Profile.</span></span>
    * <span data-ttu-id="5ae3e-149">アイドル期間に対する減価償却がゼロと表示されるプロファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-149">Validate the profile displays zero depreciation for the idle period</span></span>  
9. <span data-ttu-id="5ae3e-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-150">Close the page.</span></span>
10. <span data-ttu-id="5ae3e-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-151">Close the page.</span></span>
11. <span data-ttu-id="5ae3e-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-152">Close the page.</span></span>

## <a name="execute-depreciation-proposal"></a><span data-ttu-id="5ae3e-153">償却提案の実行</span><span class="sxs-lookup"><span data-stu-id="5ae3e-153">Execute depreciation proposal</span></span>
1. <span data-ttu-id="5ae3e-154">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-154">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="5ae3e-155">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-155">Click New.</span></span>
3. <span data-ttu-id="5ae3e-156">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-156">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="5ae3e-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-157">Click Save.</span></span>
5. <span data-ttu-id="5ae3e-158">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-158">Click Lines.</span></span>
6. <span data-ttu-id="5ae3e-159">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-159">Click Proposals.</span></span>
7. <span data-ttu-id="5ae3e-160">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-160">Click Depreciation proposal.</span></span>
8. <span data-ttu-id="5ae3e-161">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-161">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="5ae3e-162">終了日 = 12/31/2017</span><span class="sxs-lookup"><span data-stu-id="5ae3e-162">To date = 12/31/2017</span></span>  
9. <span data-ttu-id="5ae3e-163">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-163">Expand the Records to include section.</span></span>
10. <span data-ttu-id="5ae3e-164">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-164">Click Filter.</span></span>
11. <span data-ttu-id="5ae3e-165">[リセット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-165">Click Reset.</span></span>
12. <span data-ttu-id="5ae3e-166">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-166">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5ae3e-167">フィールド = 固定資産番号</span><span class="sxs-lookup"><span data-stu-id="5ae3e-167">Field = Fixed asset number</span></span>  
13. <span data-ttu-id="5ae3e-168">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-168">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="5ae3e-169">EQUPM-000024</span><span class="sxs-lookup"><span data-stu-id="5ae3e-169">EQUPM-000024</span></span>  
14. <span data-ttu-id="5ae3e-170">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-170">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5ae3e-171">フィールド = 予約</span><span class="sxs-lookup"><span data-stu-id="5ae3e-171">Field = Book</span></span>  
15. <span data-ttu-id="5ae3e-172">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-172">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="5ae3e-173">200NDB_CUR</span><span class="sxs-lookup"><span data-stu-id="5ae3e-173">200NDB_CUR</span></span>  
16. <span data-ttu-id="5ae3e-174">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-174">Click OK.</span></span>
17. <span data-ttu-id="5ae3e-175">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-175">Click OK.</span></span>
    * <span data-ttu-id="5ae3e-176">アイドル期間に対して作成された特別償却の仕訳帳は検証なし</span><span class="sxs-lookup"><span data-stu-id="5ae3e-176">Validate no depreciation journal is created for the idle period</span></span>  

