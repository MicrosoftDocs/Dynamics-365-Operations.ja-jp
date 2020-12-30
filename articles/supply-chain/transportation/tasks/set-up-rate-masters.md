---
title: レート マスターの設定
description: この手順では、レート マスターを設定する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432425"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="729f2-103">レート マスターの設定</span><span class="sxs-lookup"><span data-stu-id="729f2-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="729f2-104">この手順では、レート マスターを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="729f2-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="729f2-105">物流マネージャーは、通常、配送業者によって署名された契約に応じて、レート マスターを設定します。</span><span class="sxs-lookup"><span data-stu-id="729f2-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="729f2-106">このシナリオでは、航空運送業者のレート マスターを設定します。</span><span class="sxs-lookup"><span data-stu-id="729f2-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="729f2-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="729f2-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="729f2-108">ブレーク マスターを設定する</span><span class="sxs-lookup"><span data-stu-id="729f2-108">Set up break master</span></span>

1. <span data-ttu-id="729f2-109">**輸送管理 > 設定 > 評価 > ブレーク マスター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="729f2-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="729f2-110">分割マスターは価格構成とブレークポイントを定義するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="729f2-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="729f2-111">価格構成には物理的分析コードを基盤とした階層化された価格設定が使用されています。</span><span class="sxs-lookup"><span data-stu-id="729f2-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="729f2-112">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-112">Select **New**.</span></span>
1. <span data-ttu-id="729f2-113">**ブレーク マスター** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="729f2-114">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="729f2-115">**データ型** フィールドで、データ型を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="729f2-116">**比較** フィールドで、(演算子を使用して) 要求された比較の種類を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="729f2-117">**ブレーク単位** フィールドに、ブレーク単位を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="729f2-118">**詳細** セクションで、価格決定構造のために必要なブレークをいくつか作成します。</span><span class="sxs-lookup"><span data-stu-id="729f2-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="729f2-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="729f2-120">レート マスターの設定</span><span class="sxs-lookup"><span data-stu-id="729f2-120">Set up rate master</span></span>

1. <span data-ttu-id="729f2-121">**輸送管理 > 設定 > 評価 > レート マスター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="729f2-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="729f2-122">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-122">Select **New**.</span></span>
1. <span data-ttu-id="729f2-123">**レート マスター** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="729f2-124">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="729f2-125">**評価メタデータ ID** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="729f2-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="729f2-126">評価のメタデータ ID は、レート マスターを使用して輸送管理エンジンに予想されるメタデータを定義するように、レート マスターに必要なデータを特定します。</span><span class="sxs-lookup"><span data-stu-id="729f2-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="729f2-127">この例の場合、P2P オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-127">For this example, select the P2P option.</span></span> <span data-ttu-id="729f2-128">デモ データで既に定義されています。</span><span class="sxs-lookup"><span data-stu-id="729f2-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="729f2-129">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="729f2-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="729f2-131">レート基準の設定</span><span class="sxs-lookup"><span data-stu-id="729f2-131">Set up rate base</span></span>

1. <span data-ttu-id="729f2-132">**レート基準** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="729f2-133">レート基準は分割マスターに定義されているブレークポイントのレートを構成するため、配送業者のレートを特定し、手数料構造を設定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="729f2-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="729f2-134">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-134">Select **New**.</span></span>
3. <span data-ttu-id="729f2-135">**レート基準** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="729f2-136">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="729f2-137">**ブレーク マスター** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="729f2-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="729f2-138">分割マスターは価格構成とブレークポイントを定義するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="729f2-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="729f2-139">価格構成には物理的分析コードを基盤とした階層化された価格設定が使用されています。</span><span class="sxs-lookup"><span data-stu-id="729f2-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="729f2-140">この例の場合、重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="729f2-140">For this example, use weight.</span></span> <span data-ttu-id="729f2-141">デモ データで既に定義されています。</span><span class="sxs-lookup"><span data-stu-id="729f2-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="729f2-142">一覧で、強調表示した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="729f2-143">**詳細** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="729f2-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="729f2-144">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-144">Select **New**.</span></span>
10. <span data-ttu-id="729f2-145">**配送元郵便番号** フィールドに、「30301」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="729f2-146">**配送先郵便番号** フィールドに、「30318」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="729f2-147">**配送先国/地域** フィールドに、「USA」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="729f2-148">**<1.00 ポンド** フィールドに、「100」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="729f2-149">負荷の合計重量が 1 ポンド未満である場合、ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="729f2-150">**<5.00 ポンド** フィールドに、「300」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="729f2-151">負荷の合計重量が 5 ポンド未満である場合、ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="729f2-152">**<20.00 ポンド** フィールドに、「500」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="729f2-153">負荷の合計重量が 20 ポンド未満である場合、ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="729f2-154">**<100.00 ポンド** フィールドに、「1000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="729f2-155">負荷の合計重量が 100 ポンド未満である場合、ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="729f2-156">**<1,000.00 ポンド** フィールドに、「3000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="729f2-157">負荷の合計重量が 1000 ポンド未満である場合、ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="729f2-158">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-158">Select **Save**.</span></span>
19. <span data-ttu-id="729f2-159">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="729f2-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="729f2-160">レート基準の割り当て</span><span class="sxs-lookup"><span data-stu-id="729f2-160">Assign rate base</span></span>

1. <span data-ttu-id="729f2-161">**レート基準の割り当て** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="729f2-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="729f2-162">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-162">Select **New**.</span></span>
    * <span data-ttu-id="729f2-163">各レート マスターに対して、複数のレート基準の割り当てを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="729f2-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="729f2-164">これによって、コピー先、サービス、または異なるレート基準によって、各配送業者における複数の異なる価格ポイントを作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="729f2-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="729f2-165">この手順では、1 つのレート基準の割り当てのみを作成します。</span><span class="sxs-lookup"><span data-stu-id="729f2-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="729f2-166">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="729f2-167">**レート基準** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="729f2-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="729f2-168">一覧で、強調表示した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="729f2-169">**サービス** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="729f2-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="729f2-170">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="729f2-171">一覧で、強調表示した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="729f2-172">**集荷郵便番号** フィールドに、「98052」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="729f2-173">このレート基準の割り当てがどの郵便番号に対して有効であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="729f2-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="729f2-174">**集荷国/地域** フィールドに、「USA」と入力します。</span><span class="sxs-lookup"><span data-stu-id="729f2-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="729f2-175">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="729f2-175">Select **Save**.</span></span>
