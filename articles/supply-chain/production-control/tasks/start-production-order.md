---
title: 製造オーダーの開始
description: この手順では、作業現場での製造オーダーの開始方法を説明します。
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e444f6c521c47964b9b9b864b62fb486102c2fc7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210390"
---
# <a name="start-a-production-order"></a><span data-ttu-id="aba01-103">製造オーダーの開始</span><span class="sxs-lookup"><span data-stu-id="aba01-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aba01-104">この手順では、作業現場での製造オーダーの開始方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="aba01-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="aba01-105">時間および材料の消費は、このプロセスでレポートされます。</span><span class="sxs-lookup"><span data-stu-id="aba01-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="aba01-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="aba01-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aba01-107">これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 5 番目です。</span><span class="sxs-lookup"><span data-stu-id="aba01-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="aba01-108">製造オーダーの開始</span><span class="sxs-lookup"><span data-stu-id="aba01-108">Start a production order</span></span>
1. <span data-ttu-id="aba01-109">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="aba01-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="aba01-110">ステータスが [リリース済] の製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="aba01-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="aba01-111">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="aba01-112">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-112">Click Start.</span></span>
    * <span data-ttu-id="aba01-113">このページで、製造オーダーの開始を確認できます。</span><span class="sxs-lookup"><span data-stu-id="aba01-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="aba01-114">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-114">Click the General tab.</span></span>
5. <span data-ttu-id="aba01-115">[開始行程</span><span class="sxs-lookup"><span data-stu-id="aba01-115">In the From Oper.</span></span> <span data-ttu-id="aba01-116">一連番号</span><span class="sxs-lookup"><span data-stu-id="aba01-116">No.</span></span> <span data-ttu-id="aba01-117">フィールドで、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="aba01-117">field, enter '10'.</span></span>
6. <span data-ttu-id="aba01-118">[自動工順消費] フィールドで、「常に」を選択します。</span><span class="sxs-lookup"><span data-stu-id="aba01-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="aba01-119">[工順カード転記] チェック ボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="aba01-120">[自動 BOM 消費] フィールドで、「常に」を選択します。</span><span class="sxs-lookup"><span data-stu-id="aba01-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="aba01-121">[ピッキング リスト転記] チェックボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="aba01-122">[ピッキング リストの印刷] チェックボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="aba01-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-123">Click OK.</span></span>
    * <span data-ttu-id="aba01-124">これは、製造オーダーに使用される材料を示す印刷されたピッキング リストです。</span><span class="sxs-lookup"><span data-stu-id="aba01-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="aba01-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aba01-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="aba01-126">ピッキング リストの検証</span><span class="sxs-lookup"><span data-stu-id="aba01-126">Validate the picking list</span></span>
1. <span data-ttu-id="aba01-127">アクション ウィンドウで、[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="aba01-128">[ピッキング リスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-128">Click Picking list.</span></span>
3. <span data-ttu-id="aba01-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="aba01-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="aba01-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="aba01-131">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-131">Click Edit.</span></span>
6. <span data-ttu-id="aba01-132">[消費] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="aba01-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="aba01-133">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-133">Click Post.</span></span>
8. <span data-ttu-id="aba01-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-134">Click OK.</span></span>
    * <span data-ttu-id="aba01-135">ピッキング リスト仕訳帳には、製造オーダーによって消費される材料が転記されます。</span><span class="sxs-lookup"><span data-stu-id="aba01-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="aba01-136">見積数量と実際の消費量に差がある場合は、仕訳帳を転記する前に調整することができます。</span><span class="sxs-lookup"><span data-stu-id="aba01-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="aba01-137">[グリッド パネル] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="aba01-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aba01-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="aba01-139">工順カード仕訳帳の確認</span><span class="sxs-lookup"><span data-stu-id="aba01-139">Verify the route card journal</span></span>
1. <span data-ttu-id="aba01-140">アクション ウィンドウで、[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="aba01-141">[工順カード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-141">Click Route card.</span></span>
3. <span data-ttu-id="aba01-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="aba01-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="aba01-143">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="aba01-144">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-144">Click Edit.</span></span>
6. <span data-ttu-id="aba01-145">[時間] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="aba01-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="aba01-146">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-146">Click Post.</span></span>
8. <span data-ttu-id="aba01-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aba01-147">Click OK.</span></span>
    * <span data-ttu-id="aba01-148">[工順カード仕訳帳] では、個々の工程にかかった時間が記録されます。</span><span class="sxs-lookup"><span data-stu-id="aba01-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="aba01-149">良品および不良品の数量をレポートできます。</span><span class="sxs-lookup"><span data-stu-id="aba01-149">Good and error quantity can also be reported.</span></span>  
