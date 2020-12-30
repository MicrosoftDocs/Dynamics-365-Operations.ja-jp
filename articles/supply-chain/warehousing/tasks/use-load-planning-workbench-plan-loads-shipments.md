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
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c37a98a3728cb1233a6e1207975a6b8f23f8120d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432343"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="f8c17-103">積荷計画ワークベンチを使用した積荷および出荷の計画</span><span class="sxs-lookup"><span data-stu-id="f8c17-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8c17-104">このトピックでは、販売注文の積荷を作成するための積荷計画ワークベンチの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="f8c17-105">前提条件として、まず販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="f8c17-106">この手順は、配送コーディネーターの日常の作業一部です。</span><span class="sxs-lookup"><span data-stu-id="f8c17-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="f8c17-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="f8c17-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="f8c17-108">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="f8c17-108">Create a sales order</span></span>
1. <span data-ttu-id="f8c17-109">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 注文 > すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="f8c17-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-110">Select **New**.</span></span>
3. <span data-ttu-id="f8c17-111">**顧客口座** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8c17-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f8c17-112">勘定 **US-004** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="f8c17-113">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-113">Select **OK**.</span></span>
6. <span data-ttu-id="f8c17-114">**品目番号** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8c17-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f8c17-115">品目 **A0001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-115">Select item **A0001**.</span></span> <span data-ttu-id="f8c17-116">**A0001** は輸送管理に対して有効になっています。</span><span class="sxs-lookup"><span data-stu-id="f8c17-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="f8c17-117">**サイト** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開き、次に品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="f8c17-118">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="f8c17-119">**倉庫** フィールドに、この例の場合、「24」と入力します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="f8c17-120">この倉庫は、輸送管理および高度な倉庫管理で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="f8c17-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="f8c17-121">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-121">Select **Save**.</span></span>
12. <span data-ttu-id="f8c17-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8c17-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="f8c17-123">新しい積荷の作成</span><span class="sxs-lookup"><span data-stu-id="f8c17-123">Create a new load</span></span>
1. <span data-ttu-id="f8c17-124">**ナビゲーション ウィンドウ > モジュール > 輸送管理 > 計画 > 積荷計画ワークベンチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="f8c17-125">**販売明細行** タブを選択します。次に、作成した販売注文の積荷を構築します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="f8c17-126">積荷は、発注書、移動オーダー、および販売注文からの供給と需要に基づいて作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f8c17-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="f8c17-127">アクション ウィンドウで、**供給と需要** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="f8c17-128">**新しい積荷へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-128">Select **To new load**.</span></span>
5. <span data-ttu-id="f8c17-129">**読み込みテンプレート ID** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8c17-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="f8c17-130">積荷のテンプレートには、積荷全体の重量および容積の最大測定値を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="f8c17-131">たとえば、積荷テンプレートは、コンテナーまたはトラックのサイズを表す場合があります。</span><span class="sxs-lookup"><span data-stu-id="f8c17-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="f8c17-132">品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-132">Select an item.</span></span>
6. <span data-ttu-id="f8c17-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="f8c17-134">積荷のレートと工順</span><span class="sxs-lookup"><span data-stu-id="f8c17-134">Rate and route the load</span></span>
1. <span data-ttu-id="f8c17-135">**評価とルート指定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="f8c17-136">**レート工順ワークベンチ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="f8c17-137">**レート ショップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="f8c17-138">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f8c17-139">**割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c17-139">Select **Assign**.</span></span>
6. <span data-ttu-id="f8c17-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8c17-140">Close the page.</span></span>

