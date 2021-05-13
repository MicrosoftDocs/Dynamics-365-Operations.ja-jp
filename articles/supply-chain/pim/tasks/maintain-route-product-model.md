---
title: 製品モデルのルートの管理
description: この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921268"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="cc5a6-103">製品モデルのルートの管理</span><span class="sxs-lookup"><span data-stu-id="cc5a6-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc5a6-104">この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="cc5a6-105">この手順は、このプロセスを説明するために、デモ会社 USMF の [ハイエンド スピーカー] モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="cc5a6-106">工順工程の追加</span><span class="sxs-lookup"><span data-stu-id="cc5a6-106">Add a route operation</span></span>

1. <span data-ttu-id="cc5a6-107">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="cc5a6-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cc5a6-109">この練習の [ハイエンド スピーカー] モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="cc5a6-110">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="cc5a6-111">**工順工程** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="cc5a6-112">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-112">Select **Add**.</span></span>
1. <span data-ttu-id="cc5a6-113">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="cc5a6-114">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="cc5a6-115">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="cc5a6-116">工順工程の詳細の入力</span><span class="sxs-lookup"><span data-stu-id="cc5a6-116">Enter route operation details</span></span>

1. <span data-ttu-id="cc5a6-117">**工順工程の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="cc5a6-118">**工程** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="cc5a6-119">**工程番号**</span><span class="sxs-lookup"><span data-stu-id="cc5a6-119">In the **Oper. No.**</span></span> <span data-ttu-id="cc5a6-120">フィールドで番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-120">field, enter a number.</span></span>
    * <span data-ttu-id="cc5a6-121">工程番号が工順を決定します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="cc5a6-122">工順工程の各プロパティは、静的値を取得するか、または属性にマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="cc5a6-123">属性へのマッピングは、コンフィギュレーションの一部として設定された値になります。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="cc5a6-124">**工順グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="cc5a6-125">工順グループは、原価計算、消費、設定の重要な動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="cc5a6-126">**設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="cc5a6-127">**時間** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="cc5a6-128">**処理数量** フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="cc5a6-129">一つの工程間で処理される数量を決定します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="cc5a6-130">**時間変換係数** フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="cc5a6-131">時間の比率を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="cc5a6-132">**設定** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="cc5a6-133">**実行時間** フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="cc5a6-134">指定した数量に対する処理時間を決定します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="cc5a6-135">**リソース要件** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="cc5a6-136">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-136">Select **Add**.</span></span>
1. <span data-ttu-id="cc5a6-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="cc5a6-138">**要件のタイプ** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="cc5a6-139">保有している特定のリソースまたは機能を指定するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="cc5a6-140">**要件** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="cc5a6-141">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc5a6-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]