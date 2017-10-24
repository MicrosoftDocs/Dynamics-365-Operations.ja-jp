--- 
title: "減価償却税申告のフォーム 26 (日本)"
description: "このタスクでは、登録番号の固定資産への割り当て方法と申告 26 レポートの印刷について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3e6bc8267c6adb9e82f0c11885b211be3bd75c9a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="form-26-for-depreciable-tax-declaration-japan"></a><span data-ttu-id="2569e-103">減価償却税申告のフォーム 26 (日本)</span><span class="sxs-lookup"><span data-stu-id="2569e-103">Form 26 for depreciable tax declaration (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2569e-104">このタスクでは、登録番号の固定資産への割り当て方法と申告 26 レポートの印刷について説明します。</span><span class="sxs-lookup"><span data-stu-id="2569e-104">This task walks you through assigning a registration number to a fixed asset and printing the form 26 report.</span></span>

<span data-ttu-id="2569e-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2569e-105">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>

<span data-ttu-id="2569e-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="2569e-106">This task uses the JPMF demo company data.</span></span> <span data-ttu-id="2569e-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="2569e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-registration-number"></a><span data-ttu-id="2569e-108">登録番号の作成</span><span class="sxs-lookup"><span data-stu-id="2569e-108">Create a registration number</span></span>
1. <span data-ttu-id="2569e-109">[組織管理] > [組織] > [法人] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2569e-109">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="2569e-110">登録 ID をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-110">Click Registration IDs.</span></span>
3. <span data-ttu-id="2569e-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-111">Click New.</span></span>
4. <span data-ttu-id="2569e-112">[目的] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-112">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="2569e-113">目的 = 固定資産</span><span class="sxs-lookup"><span data-stu-id="2569e-113">Purpose = Fixed asset</span></span>  
5. <span data-ttu-id="2569e-114">[名前または説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-114">In the Name or description field, type a value.</span></span>
6. <span data-ttu-id="2569e-115">[住所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2569e-115">Expand the Address section.</span></span>
7. <span data-ttu-id="2569e-116">[国/地域] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-116">In the Country/region field, type a value.</span></span>
8. <span data-ttu-id="2569e-117">[都道府県] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-117">In the State field, enter or select a value.</span></span>
9. <span data-ttu-id="2569e-118">[市町村] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-118">In the City field, enter or select a value.</span></span>
10. <span data-ttu-id="2569e-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-119">Click Save.</span></span>
11. <span data-ttu-id="2569e-120">[登録 ID] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2569e-120">Expand the Registration ID section.</span></span>
12. <span data-ttu-id="2569e-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-121">Click Add.</span></span>
13. <span data-ttu-id="2569e-122">[登録タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-122">In the Registration type field, enter or select a value.</span></span>
14. <span data-ttu-id="2569e-123">[登録番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-123">In the Registration number field, type a value.</span></span>
15. <span data-ttu-id="2569e-124">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-124">Click the General tab.</span></span>
16. <span data-ttu-id="2569e-125">[有効開始] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-125">In the Effective field, enter a date.</span></span>
17. <span data-ttu-id="2569e-126">[減価償却方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-126">In the Depreciation method field, select an option.</span></span>
18. <span data-ttu-id="2569e-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-127">Click Save.</span></span>

## <a name="create-a-fixed-asset-location-and-assign-registration-number"></a><span data-ttu-id="2569e-128">固定資産の場所の作成および登録番号の割り当て</span><span class="sxs-lookup"><span data-stu-id="2569e-128">Create a fixed asset location and assign registration number</span></span>
1. <span data-ttu-id="2569e-129">[固定資産] > [設定] > [固定資産の属性] > [固定資産の場所] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2569e-129">Go to Fixed assets > Setup > Fixed asset attributes > Fixed assets locations.</span></span>
2. <span data-ttu-id="2569e-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-130">Click New.</span></span>
3. <span data-ttu-id="2569e-131">[場所] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-131">In the Location field, type a value.</span></span>
4. <span data-ttu-id="2569e-132">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-132">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2569e-133">[住所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2569e-133">Expand the Address section.</span></span>
6. <span data-ttu-id="2569e-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-134">Click New.</span></span>
7. <span data-ttu-id="2569e-135">[名前または説明] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-135">In the Name or description field, enter or select a value.</span></span>
8. <span data-ttu-id="2569e-136">[登録番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-136">In the Registration number field, enter or select a value.</span></span>
9. <span data-ttu-id="2569e-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-137">Click OK.</span></span>
10. <span data-ttu-id="2569e-138">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-138">Click Save.</span></span>

## <a name="define-location-to-the-fixed-asset-group"></a><span data-ttu-id="2569e-139">固定資産グループへの場所の定義</span><span class="sxs-lookup"><span data-stu-id="2569e-139">Define location to the Fixed asset group</span></span>
1. <span data-ttu-id="2569e-140">[固定資産] > [設定] > [固定資産グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2569e-140">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="2569e-141">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2569e-142">たとえば、[VEHI-A] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-142">For example, select VEHI-A.</span></span>  
3. <span data-ttu-id="2569e-143">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-143">Click Edit.</span></span>
4. <span data-ttu-id="2569e-144">[場所] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-144">In the Location field, enter or select a value.</span></span>
5. <span data-ttu-id="2569e-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-145">Click Save.</span></span>

## <a name="create-a-fixed-asset"></a><span data-ttu-id="2569e-146">固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="2569e-146">Create a fixed asset</span></span>
1. <span data-ttu-id="2569e-147">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2569e-147">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="2569e-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-148">Click New.</span></span>
3. <span data-ttu-id="2569e-149">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-149">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="2569e-150">[場所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2569e-150">Expand the Location section.</span></span>
    * <span data-ttu-id="2569e-151">固定資産の場所の既定値の検証</span><span class="sxs-lookup"><span data-stu-id="2569e-151">Validate Location defaults for the fixed asset</span></span>  

## <a name="create-an-acquisition"></a><span data-ttu-id="2569e-152">取得の作成</span><span class="sxs-lookup"><span data-stu-id="2569e-152">Create an acquisition</span></span>
1. <span data-ttu-id="2569e-153">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2569e-153">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="2569e-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-154">Click New.</span></span>
3. <span data-ttu-id="2569e-155">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-155">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="2569e-156">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-156">Click Save.</span></span>
5. <span data-ttu-id="2569e-157">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-157">Click Lines.</span></span>
6. <span data-ttu-id="2569e-158">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-158">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="2569e-159">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2569e-159">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="2569e-160">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2569e-160">In the Debit field, enter a number.</span></span>
9. <span data-ttu-id="2569e-161">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2569e-161">Click Post.</span></span>

## <a name="verify-the-form-26-report"></a><span data-ttu-id="2569e-162">申告 26 レポートの確認</span><span class="sxs-lookup"><span data-stu-id="2569e-162">Verify the Form 26 report</span></span>
1. <span data-ttu-id="2569e-163">[固定資産] > [照会およびレポート] > [減価償却資産申告レポート] > [申告 26: 償却資産税の元帳レポート] と移動します。</span><span class="sxs-lookup"><span data-stu-id="2569e-163">Go to Fixed assets > Inquiries and reports > Depreciable asset declaration reports > Form 26: Depreciable assets taxation ledger report.</span></span>
2. <span data-ttu-id="2569e-164">[暦年] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-164">In the Calendar year field, enter or select a value.</span></span>
3. <span data-ttu-id="2569e-165">[事業所用家屋資産番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-165">In the Office building asset number field, enter or select a value.</span></span>
4. <span data-ttu-id="2569e-166">[登録番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2569e-166">In the Registration number field, enter or select a value.</span></span>
    * <span data-ttu-id="2569e-167">必要な場所でレポートを表示/保存します。</span><span class="sxs-lookup"><span data-stu-id="2569e-167">Open/save the report in the required location.</span></span>  <span data-ttu-id="2569e-168">印刷レポートの検証、固定資産を登録番号ごとに分類してグループ化します。</span><span class="sxs-lookup"><span data-stu-id="2569e-168">Validate the printed report,  the Fixed assets been sorted and grouped by registration number</span></span>  
    * <span data-ttu-id="2569e-169">同様の固定資産の分類 n グループが、申告 26-1 n 申告 26-2 レポートに提示されます</span><span class="sxs-lookup"><span data-stu-id="2569e-169">Similar sorting n grouping of fixed asset is provided for the Form 26-1 n Form 26-2 reports</span></span>  


