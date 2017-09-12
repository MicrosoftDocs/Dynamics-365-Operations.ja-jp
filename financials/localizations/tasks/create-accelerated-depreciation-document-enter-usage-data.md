--- 
title: "増加償却ドキュメントの作成および使用状況データの入力 (日本)"
description: "日本では、加速償却は、原則ドキュメントごとに申告されます。"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ca2071a1f8523be519f7025e81569249e23f0903
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-accelerated-depreciation-document-and-enter-usage-data-japan"></a><span data-ttu-id="b8339-103">増加償却ドキュメントの作成および使用状況データの入力 (日本)</span><span class="sxs-lookup"><span data-stu-id="b8339-103">Create an accelerated depreciation document and enter usage data (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8339-104">日本では、加速償却は、原則ドキュメントごとに申告されます。</span><span class="sxs-lookup"><span data-stu-id="b8339-104">For Japan, Accelerated depreciation is declared on a per document basis.</span></span> <span data-ttu-id="b8339-105">各ドキュメントには複数の固定資産を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b8339-105">Each document can contain multiple fixed assets.</span></span> <span data-ttu-id="b8339-106">加速償却額を取得するためには、加速償却ドキュメントで過剰使用率を計算し、通常の減価償却量によって乗算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8339-106">You must calculate an overuse rate on the accelerated depreciation document and multiply it by the ordinary depreciation amount to get the amount for the accelerated depreciation.</span></span> 



<span data-ttu-id="b8339-107">加速償却申告の詳細はドキュメントに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="b8339-107">The details of the accelerated depreciation declaration are listed on the document.</span></span> <span data-ttu-id="b8339-108">確認済加速償却ドキュメントのみ転記用の加速償却提案で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8339-108">Only a confirmed accelerated depreciation document can be used at accelerated depreciation proposal for posting.</span></span> 



<span data-ttu-id="b8339-109">この手順は、加速償却プロファイルを含む固定資産の作成、加速償却ドキュメントの作成および固定資産への割り当てについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b8339-109">This procedure walks you through creating a fixed asset with an accelerated depreciation profile and then creating an accelerated depreciation document and assigning the fixed asset to it.</span></span> <span data-ttu-id="b8339-110">最後に、固定資産の超過使用時間を入力し、ドキュメント上で過剰使用率の計算ができます。</span><span class="sxs-lookup"><span data-stu-id="b8339-110">Finally, you can enter the overuse hours for the fixed asset and calculate overuse rate on the document.</span></span>



<span data-ttu-id="b8339-111">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8339-111">In order to complete this procedure, the Fixed asset configuration key must be selected.</span></span>



<span data-ttu-id="b8339-112">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="b8339-112">This procedure was created using the demo data company JPMF.</span></span>


## <a name="create-a-fixed-asset-with-accelerated-depreciation"></a><span data-ttu-id="b8339-113">減価償却により固定資産を作成します</span><span class="sxs-lookup"><span data-stu-id="b8339-113">Create a fixed asset with accelerated depreciation</span></span>
1. <span data-ttu-id="b8339-114">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8339-114">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="b8339-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-115">Click New.</span></span>
3. <span data-ttu-id="b8339-116">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-116">In the Fixed asset group field, type a value.</span></span>
    * <span data-ttu-id="b8339-117">例 : VEHI-M</span><span class="sxs-lookup"><span data-stu-id="b8339-117">Example: VEHI-M</span></span>  
4. <span data-ttu-id="b8339-118">参照用として固定資産番号を記録</span><span class="sxs-lookup"><span data-stu-id="b8339-118">Note the fixed asset number for later reference</span></span>
5. <span data-ttu-id="b8339-119">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-119">In the Name field, type a value.</span></span>
6. <span data-ttu-id="b8339-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-120">Click Save.</span></span>
7. <span data-ttu-id="b8339-121">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-121">Click Books.</span></span>
8. <span data-ttu-id="b8339-122">[減価償却] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b8339-122">Expand the Depreciation section.</span></span>
    * <span data-ttu-id="b8339-123">[加速償却プロファイル] フィールドが正しく構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b8339-123">Confirm that the Accelerated depreciation profile field is configured properly.</span></span>  
    * <span data-ttu-id="b8339-124">既存の固定資産には、加速償却プロファイルを適用するために手動でこの値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b8339-124">For the existing fixed assets, you can also manually enter this value to apply accelerated depreciation profile to it.</span></span>  

## <a name="acquire-the-fixed-asset"></a><span data-ttu-id="b8339-125">固定資産の取得</span><span class="sxs-lookup"><span data-stu-id="b8339-125">Acquire the fixed asset</span></span>
1. <span data-ttu-id="b8339-126">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8339-126">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="b8339-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-127">Click New.</span></span>
3. <span data-ttu-id="b8339-128">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-128">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b8339-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-129">Click Save.</span></span>
5. <span data-ttu-id="b8339-130">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-130">Click Lines.</span></span>
6. <span data-ttu-id="b8339-131">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-131">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="b8339-132">事前に記録した固定資産番号の使用</span><span class="sxs-lookup"><span data-stu-id="b8339-132">Use the previously noted fixed asset number</span></span>
8. <span data-ttu-id="b8339-133">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-133">In the Debit field, enter a number.</span></span>
9. <span data-ttu-id="b8339-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-134">Click Save.</span></span>
10. <span data-ttu-id="b8339-135">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-135">Click Post.</span></span>

## <a name="enter-overuse-information-in-the-accelerated-depreciation-document"></a><span data-ttu-id="b8339-136">加速償却ドキュメントの過剰使用量の情報を入力</span><span class="sxs-lookup"><span data-stu-id="b8339-136">Enter overuse information in the accelerated depreciation document</span></span>
1. <span data-ttu-id="b8339-137">[固定資産] > [定期処理タスク] > [加速償却] > [加速償却ドキュメント] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8339-137">Go to Fixed assets > Periodic tasks > Accelerated depreciation > Accelerated depreciation document.</span></span>
2. <span data-ttu-id="b8339-138">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-138">Click New.</span></span>
3. <span data-ttu-id="b8339-139">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-139">In the Description field, type a value.</span></span>
4. <span data-ttu-id="b8339-140">[固定資産設備グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-140">In the Fixed asset equipment group field, type a value.</span></span>
5. <span data-ttu-id="b8339-141">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-141">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="b8339-142">[開始日] および [終了日] は、加速償却を申請および申告するための申告期間を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8339-142">The From date and To date are used to define the declaration period during which to apply and to declare the accelerated depreciation.</span></span>  
6. <span data-ttu-id="b8339-143">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-143">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="b8339-144">[開始日] および [終了日] は、加速償却を申請および申告するための申告期間を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8339-144">The From date and To date are used to define the declaration period during which to apply and to declare the accelerated depreciation.</span></span>  
7. <span data-ttu-id="b8339-145">[固定資産と作業時間の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b8339-145">Expand the Fixed assets and working hours detail section.</span></span>
    * <span data-ttu-id="b8339-146">データを正確で完全にするため、固定資産によって勤務時間を入力することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b8339-146">It is recommended to enter working hours by fixed assets so that the data is accurate and complete.</span></span>  
8. <span data-ttu-id="b8339-147">クエリで [追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-147">Click Add by query.</span></span>
9. <span data-ttu-id="b8339-148">[基準] フィールドで適切な固定資産をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="b8339-148">In the Criteria field, Filter the proper fixed assets.</span></span>
10. <span data-ttu-id="b8339-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-149">Click OK.</span></span>
11. <span data-ttu-id="b8339-150">[計画済] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8339-150">In the Planned field, enter a number.</span></span>
    * <span data-ttu-id="b8339-151">[予定時刻] 以外で、適用される場合 [予約済] か、または [実際の時間] に入力できます。</span><span class="sxs-lookup"><span data-stu-id="b8339-151">Other than Planned hours, you can also choose to enter Reserved or Actual hours if they apply.</span></span>  
12. <span data-ttu-id="b8339-152">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-152">Click Save.</span></span>
13. <span data-ttu-id="b8339-153">[1 日あたりの平均時間の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-153">Click Calculate daily average hour.</span></span>
    * <span data-ttu-id="b8339-154">[過剰使用率] が計算および更新されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b8339-154">Confirm that the Overuse rate is calculated and updated.</span></span>  
    * <span data-ttu-id="b8339-155">既に過剰使用率を計算した場合、計算ステップを省いて過剰使用率を直接入力し、提案目的でドキュメントを確定することができます。</span><span class="sxs-lookup"><span data-stu-id="b8339-155">If you have already calculated the Overuse rate you can choose to skip the calculate step and directly enter the Overuse rate and confirm the document for proposal purpose.</span></span>  
14. <span data-ttu-id="b8339-156">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8339-156">Click Confirm.</span></span>
    * <span data-ttu-id="b8339-157">確認済 [加速償却ドキュメント] のみ提案として使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8339-157">Only confirmed Accelerated depreciation documents can be used for the proposal.</span></span>  


