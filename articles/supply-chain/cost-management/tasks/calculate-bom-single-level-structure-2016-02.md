---
title: 単一レベル構造を使用した BOM の計算 (2016 年 2 月)
description: この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e02e76cd5762fc683290eeee49d23c9fed8d4503
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150519"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="d2efb-103">単一レベル構造を使用した BOM の計算 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="d2efb-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2efb-104">この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d2efb-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="d2efb-105">これは、BOM 計算シリーズの 6 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="d2efb-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="d2efb-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="d2efb-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="d2efb-107">[リリースされた製品] に進みます。</span><span class="sxs-lookup"><span data-stu-id="d2efb-107">Go to Released products.</span></span>
2. <span data-ttu-id="d2efb-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d2efb-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2efb-109">製品 BOM_1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2efb-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="d2efb-110">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2efb-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="d2efb-111">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2efb-111">Click Item price.</span></span>
5. <span data-ttu-id="d2efb-112">[品目原価の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2efb-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="d2efb-113">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2efb-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="d2efb-114">[原価計算バージョン] フィールドで、ドロップ ダウン ボタンをクリックして、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d2efb-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d2efb-115">このデモでは、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2efb-115">For this demo, select 10.</span></span> <span data-ttu-id="d2efb-116">これは、原価価格をコンポーネントに追加する際に使用される、同じ原価バージョンです。</span><span class="sxs-lookup"><span data-stu-id="d2efb-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="d2efb-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2efb-117">Click OK.</span></span>
8. <span data-ttu-id="d2efb-118">[計算の詳細の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2efb-118">Click View calculation details.</span></span>
    * <span data-ttu-id="d2efb-119">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2efb-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="d2efb-120">コストの構成は次のとおりです:  \*    10 は ITEM_A から、 10 は ITEM_B から、 10 は BOM_2 から派生します。</span><span class="sxs-lookup"><span data-stu-id="d2efb-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="d2efb-121">この場合、BOM_2 は計算によってではなく、標準原価 10 として入力されたので、その詳細はありません。</span><span class="sxs-lookup"><span data-stu-id="d2efb-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="d2efb-122">\*    7 は一定のコストである段取り時間から派生し、追加の 7 は実行時操作 (プロセス) から派生します。</span><span class="sxs-lookup"><span data-stu-id="d2efb-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="d2efb-123">\*    間接原価に対応する他の金額もあります。</span><span class="sxs-lookup"><span data-stu-id="d2efb-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="d2efb-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="d2efb-124">@SysTaskRecorder:_RequestClose</span></span>

