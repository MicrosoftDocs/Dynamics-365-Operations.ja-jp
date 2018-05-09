--- 
title: "製品モデルのルートの管理"
description: "この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 25d9530fc137b443b99a183b9d10886585c7b65f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="7e962-103">製品モデルのルートの管理</span><span class="sxs-lookup"><span data-stu-id="7e962-103">Maintain a route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e962-104">この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="7e962-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="7e962-105">この手順は、このプロセスを説明するために、デモ会社 USMF の [ハイエンド スピーカー] モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e962-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="7e962-106">工順工程の追加</span><span class="sxs-lookup"><span data-stu-id="7e962-106">Add a route operation</span></span>
1. <span data-ttu-id="7e962-107">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="7e962-108">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="7e962-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7e962-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7e962-110">この練習の [ハイエンド スピーカー] モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e962-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="7e962-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7e962-112">[工順工程] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7e962-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="7e962-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-113">Click Add.</span></span>
7. <span data-ttu-id="7e962-114">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e962-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="7e962-115">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e962-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="7e962-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="7e962-117">工順工程の詳細の入力</span><span class="sxs-lookup"><span data-stu-id="7e962-117">Enter route operation details</span></span>
1. <span data-ttu-id="7e962-118">[工順工程の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-118">Click Route operation details.</span></span>
2. <span data-ttu-id="7e962-119">[操作] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7e962-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="7e962-120">[工程</span><span class="sxs-lookup"><span data-stu-id="7e962-120">In the Oper.</span></span> <span data-ttu-id="7e962-121">一連番号</span><span class="sxs-lookup"><span data-stu-id="7e962-121">No.</span></span> <span data-ttu-id="7e962-122">フィールドで番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e962-122">field, enter a number.</span></span>
    * <span data-ttu-id="7e962-123">工程番号が工順を決定します。</span><span class="sxs-lookup"><span data-stu-id="7e962-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="7e962-124">工順工程の各プロパティは、静的値を取得するか、または属性にマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="7e962-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="7e962-125">属性へのマッピングは、コンフィギュレーションの一部として設定された値になります。</span><span class="sxs-lookup"><span data-stu-id="7e962-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="7e962-126">[工順グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7e962-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="7e962-127">工順グループは、原価計算、消費、設定の重要な動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="7e962-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="7e962-128">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="7e962-129">[時間] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-129">Click the Times tab.</span></span>
7. <span data-ttu-id="7e962-130">処理数量 フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e962-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="7e962-131">一つの工程間で処理される数量を決定します。</span><span class="sxs-lookup"><span data-stu-id="7e962-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="7e962-132">[時間変換係数] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e962-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="7e962-133">時間の比率を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e962-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="7e962-134">[設定] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e962-134">Select the Set check box.</span></span>
10. <span data-ttu-id="7e962-135">[実行時間] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e962-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="7e962-136">指定した数量に対する処理時間を決定します。</span><span class="sxs-lookup"><span data-stu-id="7e962-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="7e962-137">[リソース要件] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="7e962-138">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-138">Click Add.</span></span>
13. <span data-ttu-id="7e962-139">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="7e962-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="7e962-140">[要件のタイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e962-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="7e962-141">保有している特定のリソースまたは機能を指定するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7e962-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="7e962-142">[要件] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7e962-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="7e962-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e962-143">Click OK.</span></span>


