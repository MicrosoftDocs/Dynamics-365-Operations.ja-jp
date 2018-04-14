--- 
title: "積荷計画ワークベンチを使用した積荷および出荷の計画"
description: "この手順では、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e948861920897cae7570984f97e3ff3893924a28
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="636a1-103">積荷計画ワークベンチを使用した積荷および出荷の計画</span><span class="sxs-lookup"><span data-stu-id="636a1-103">Plan loads and shipments using the Load planning workbench</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="636a1-104">この手順では、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="636a1-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="636a1-105">前提条件として、まず販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="636a1-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="636a1-106">この手順は、配送コーディネーターの日常の作業一部です。</span><span class="sxs-lookup"><span data-stu-id="636a1-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="636a1-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="636a1-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="636a1-108">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="636a1-108">Create a sales order</span></span>
1. <span data-ttu-id="636a1-109">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="636a1-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="636a1-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-110">Click New.</span></span>
3. <span data-ttu-id="636a1-111">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="636a1-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="636a1-112">勘定 US-004 を選択します。</span><span class="sxs-lookup"><span data-stu-id="636a1-112">Select account US-004.</span></span>
5. <span data-ttu-id="636a1-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-113">Click OK.</span></span>
6. <span data-ttu-id="636a1-114">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="636a1-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="636a1-115">品目 A0001 を選択します。</span><span class="sxs-lookup"><span data-stu-id="636a1-115">Select item A0001.</span></span>
    * <span data-ttu-id="636a1-116">A0001 は輸送管理に対して有効になっています。</span><span class="sxs-lookup"><span data-stu-id="636a1-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="636a1-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="636a1-118">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="636a1-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="636a1-119">[倉庫] フィールドに、「24」と入力します。</span><span class="sxs-lookup"><span data-stu-id="636a1-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="636a1-120">この例では、倉庫 24 を選択します。</span><span class="sxs-lookup"><span data-stu-id="636a1-120">In this example select warehouse 24.</span></span> <span data-ttu-id="636a1-121">この倉庫は、輸送管理および高度な倉庫管理で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="636a1-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="636a1-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-122">Click Save.</span></span>
12. <span data-ttu-id="636a1-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="636a1-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="636a1-124">新しい積荷の作成</span><span class="sxs-lookup"><span data-stu-id="636a1-124">Create a new load</span></span>
1. <span data-ttu-id="636a1-125">[配送管理] > [計画] > [積荷計画ワークベンチ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="636a1-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="636a1-126">[販売明細行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="636a1-127">次に、作成した販売注文の積荷を構築します。</span><span class="sxs-lookup"><span data-stu-id="636a1-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="636a1-128">積荷は、発注書、移動オーダー、および販売注文からの供給と需要に基づいて作成することができます。</span><span class="sxs-lookup"><span data-stu-id="636a1-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="636a1-129">アクション ウィンドウで、[供給と需要] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="636a1-130">[新しい積荷へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-130">Click To new load.</span></span>
5. <span data-ttu-id="636a1-131">[読み込みテンプレート ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="636a1-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="636a1-132">積荷のテンプレートには、積荷全体の重量および容積の最大測定値を定義します。</span><span class="sxs-lookup"><span data-stu-id="636a1-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="636a1-133">たとえば、積荷テンプレートは、コンテナーまたはトラックのサイズを表す場合があります。</span><span class="sxs-lookup"><span data-stu-id="636a1-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="636a1-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="636a1-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="636a1-136">積荷のレートと工順</span><span class="sxs-lookup"><span data-stu-id="636a1-136">Rate and route the load</span></span>
1. <span data-ttu-id="636a1-137">[評価とルート指定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="636a1-138">[工順ワークベンチの評価] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="636a1-139">[レート ショップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-139">Click Rate shop.</span></span>
4. <span data-ttu-id="636a1-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="636a1-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="636a1-141">[割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="636a1-141">Click Assign.</span></span>
6. <span data-ttu-id="636a1-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="636a1-142">Close the page.</span></span>
7. <span data-ttu-id="636a1-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="636a1-143">Close the page.</span></span>


