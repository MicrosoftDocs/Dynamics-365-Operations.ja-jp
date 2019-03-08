---
title: レート マスターの設定
description: この手順では、レート マスターを設定する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462bfce89fa77c8830a93a22b0dd6c8c8fb2cde6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "344918"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="51724-103">レート マスターの設定</span><span class="sxs-lookup"><span data-stu-id="51724-103">Set up rate masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51724-104">この手順では、レート マスターを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="51724-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="51724-105">物流マネージャーは、通常、配送業者によって署名された契約に応じて、レート マスターを設定します。</span><span class="sxs-lookup"><span data-stu-id="51724-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="51724-106">このシナリオでは、航空運送業者のレート マスターを設定します。</span><span class="sxs-lookup"><span data-stu-id="51724-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="51724-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="51724-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="51724-108">レート マスターの設定</span><span class="sxs-lookup"><span data-stu-id="51724-108">Set up rate master</span></span>
1. <span data-ttu-id="51724-109">[輸送管理] > [設定] > [評価] > [レート マスター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="51724-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="51724-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-110">Click New.</span></span>
3. <span data-ttu-id="51724-111">[レート マスター] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="51724-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="51724-113">[評価メタデータ ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="51724-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="51724-114">評価のメタデータ ID は、レート マスターを使用して TMS エンジンに予想されるメタデータを定義するように、レート マスターに必要なデータを特定します。</span><span class="sxs-lookup"><span data-stu-id="51724-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="51724-115">この例の場合、P2P オプションを選択します</span><span class="sxs-lookup"><span data-stu-id="51724-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="51724-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="51724-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="51724-118">レート基準の設定</span><span class="sxs-lookup"><span data-stu-id="51724-118">Set up rate base</span></span>
1. <span data-ttu-id="51724-119">[レート基準] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-119">Click Rate base.</span></span>
    * <span data-ttu-id="51724-120">レート基準は分割マスターに定義されているブレークポイントのレートを構成するため、配送業者のレートを特定し、手数料構造を設定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="51724-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="51724-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-121">Click New.</span></span>
3. <span data-ttu-id="51724-122">[レート基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="51724-123">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="51724-124">[ブレーク マスター] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="51724-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="51724-125">分割マスターは価格構成とブレークポイントを定義するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="51724-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="51724-126">価格構成には物理的分析コードを基盤とした階層化された価格設定が使用されています。</span><span class="sxs-lookup"><span data-stu-id="51724-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="51724-127">この例の場合、重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="51724-127">For this example, use weight</span></span>
7. <span data-ttu-id="51724-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="51724-129">[詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="51724-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="51724-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-130">Click New.</span></span>
10. <span data-ttu-id="51724-131">[配送元郵便番号] フィールドに、「30301」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="51724-132">[配送先郵便番号] フィールドに、「30318」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="51724-133">[配送先国/地域] フィールドに、「USA」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="51724-134">[<1.00 ポンド] フィールドに、「100」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="51724-135">負荷の合計重量が 1 ポンド未満である場合、1 ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="51724-136">[<5.00 Lbs] フィールドに、「300」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="51724-137">負荷の合計重量が 5 ポンド未満である場合、5 ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="51724-138">[<20.00 Lbs] フィールドに、「500」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="51724-139">負荷の合計重量が 20 ポンド未満である場合、20 ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="51724-140">[<100.00 Lbs] フィールドに、「1000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="51724-141">負荷の合計重量が 100 ポンド未満である場合、100 ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="51724-142">[<1,000.00 Lbs] フィールドに、「3000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="51724-143">負荷の合計重量が 1000 ポンド未満である場合、1000 ポンドあたりのレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="51724-144">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-144">Click Save.</span></span>
19. <span data-ttu-id="51724-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="51724-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="51724-146">レート基準の割り当て</span><span class="sxs-lookup"><span data-stu-id="51724-146">Assign rate base</span></span>
1. <span data-ttu-id="51724-147">[レート基準の割り当て] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="51724-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="51724-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-148">Click New.</span></span>
    * <span data-ttu-id="51724-149">各レート マスターに対して、複数のレート基準の割り当てを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="51724-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="51724-150">これによって、コピー先、サービス、または異なるレート基準によって、各配送業者における複数の異なる価格ポイントを作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="51724-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="51724-151">この手順では、1 つのレート基準の割り当てのみを作成します。</span><span class="sxs-lookup"><span data-stu-id="51724-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="51724-152">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="51724-153">[レート基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="51724-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="51724-154">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="51724-155">[サービス] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="51724-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="51724-156">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="51724-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="51724-157">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="51724-158">[集荷郵便番号] フィールドに、「98052」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="51724-159">このレート基準の割り当てがどの郵便番号に対して有効であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="51724-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="51724-160">[集荷国/地域] フィールドに、「USA」と入力します。</span><span class="sxs-lookup"><span data-stu-id="51724-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="51724-161">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="51724-161">Click Save.</span></span>

