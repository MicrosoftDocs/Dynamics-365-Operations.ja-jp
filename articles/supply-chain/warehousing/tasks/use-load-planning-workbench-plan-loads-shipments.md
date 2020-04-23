---
title: 積荷計画ワークベンチを使用した積荷および出荷の計画
description: このトピックでは、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a6af2f0623744f2cddf46c0310231afb0870fd7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216738"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="81339-103">積荷計画ワークベンチを使用した積荷および出荷の計画</span><span class="sxs-lookup"><span data-stu-id="81339-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81339-104">このトピックでは、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="81339-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="81339-105">前提条件として、まず販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="81339-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="81339-106">この手順は、配送コーディネーターの日常の作業一部です。</span><span class="sxs-lookup"><span data-stu-id="81339-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="81339-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="81339-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="81339-108">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="81339-108">Create a sales order</span></span>
1. <span data-ttu-id="81339-109">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 注文 > すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="81339-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="81339-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-110">Select **New**.</span></span>
3. <span data-ttu-id="81339-111">**顧客口座**フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="81339-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="81339-112">勘定 **US-004** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="81339-113">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-113">Select **OK**.</span></span>
6. <span data-ttu-id="81339-114">**品目番号**フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="81339-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="81339-115">品目 **A0001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-115">Select item **A0001**.</span></span> <span data-ttu-id="81339-116">**A0001** は輸送管理に対して有効になっています。</span><span class="sxs-lookup"><span data-stu-id="81339-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="81339-117">**サイト** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開き、次に品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="81339-118">**数量**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="81339-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="81339-119">**倉庫**フィールドに、この例の場合、「24」と入力します。</span><span class="sxs-lookup"><span data-stu-id="81339-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="81339-120">この倉庫は、輸送管理および高度な倉庫管理で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="81339-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="81339-121">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-121">Select **Save**.</span></span>
12. <span data-ttu-id="81339-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81339-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="81339-123">新しい積荷の作成</span><span class="sxs-lookup"><span data-stu-id="81339-123">Create a new load</span></span>
1. <span data-ttu-id="81339-124">**ナビゲーション ウィンドウ > モジュール > 輸送管理 > 計画 > 積荷計画ワークベンチ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="81339-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="81339-125">**販売明細行**タブを選択します。次に、作成した販売注文の積荷を構築します。</span><span class="sxs-lookup"><span data-stu-id="81339-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="81339-126">積荷は、発注書、移動オーダー、および販売注文からの供給と需要に基づいて作成することができます。</span><span class="sxs-lookup"><span data-stu-id="81339-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="81339-127">アクション ウィンドウで、**供給と需要**を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="81339-128">**新しい積荷へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-128">Select **To new load**.</span></span>
5. <span data-ttu-id="81339-129">**読み込みテンプレート ID** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="81339-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="81339-130">積荷のテンプレートには、積荷全体の重量および容積の最大測定値を定義します。</span><span class="sxs-lookup"><span data-stu-id="81339-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="81339-131">たとえば、積荷テンプレートは、コンテナーまたはトラックのサイズを表す場合があります。</span><span class="sxs-lookup"><span data-stu-id="81339-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="81339-132">品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-132">Select an item.</span></span>
6. <span data-ttu-id="81339-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="81339-134">積荷のレートと工順</span><span class="sxs-lookup"><span data-stu-id="81339-134">Rate and route the load</span></span>
1. <span data-ttu-id="81339-135">**評価とルート指定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="81339-136">**レート工順ワークベンチ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="81339-137">**レート ショップ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="81339-138">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="81339-139">**割り当て**を選択します。</span><span class="sxs-lookup"><span data-stu-id="81339-139">Select **Assign**.</span></span>
6. <span data-ttu-id="81339-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81339-140">Close the page.</span></span>

