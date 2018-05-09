--- 
title: "単一レベル構造を使用した BOM の計算 (2016 年 2 月のみ)"
description: "この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a318b2308f8cd5c3650a392aed53185df6f81dc
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a><span data-ttu-id="cb075-103">単一レベル構造を使用した BOM の計算 (2016 年 2 月のみ)</span><span class="sxs-lookup"><span data-stu-id="cb075-103">Calculate a BOM by using a single level structure (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb075-104">この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cb075-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="cb075-105">これは、BOM 計算シリーズの 6 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="cb075-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="cb075-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="cb075-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="cb075-107">[リリースされた製品] に進みます。</span><span class="sxs-lookup"><span data-stu-id="cb075-107">Go to Released products.</span></span>
2. <span data-ttu-id="cb075-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cb075-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cb075-109">製品 BOM_1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb075-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="cb075-110">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb075-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="cb075-111">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb075-111">Click Item price.</span></span>
5. <span data-ttu-id="cb075-112">[品目原価の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb075-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="cb075-113">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb075-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="cb075-114">[原価計算バージョン] フィールドで、ドロップ ダウン ボタンをクリックして、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cb075-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cb075-115">このデモでは、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb075-115">For this demo, select 10.</span></span> <span data-ttu-id="cb075-116">これは、原価価格をコンポーネントに追加する際に使用される、同じ原価バージョンです。</span><span class="sxs-lookup"><span data-stu-id="cb075-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="cb075-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb075-117">Click OK.</span></span>
8. <span data-ttu-id="cb075-118">[計算の詳細の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb075-118">Click View calculation details.</span></span>
    * <span data-ttu-id="cb075-119">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb075-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="cb075-120">以下に原価の構成を示します。 •    10 は ITEM_A から派生し、10 は ITEM_B から派生し、10 は BOM_2 から派生します。</span><span class="sxs-lookup"><span data-stu-id="cb075-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="cb075-121">この場合、BOM_2 は計算によってではなく、標準原価 10 として入力されたので、その詳細はありません。</span><span class="sxs-lookup"><span data-stu-id="cb075-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="cb075-122">•  7 は段取り時間から派生します。これは一定の原価であり、追加の 7 は実行時工程 (プロセス) から派生します。</span><span class="sxs-lookup"><span data-stu-id="cb075-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="cb075-123">•   また、間接原価に対応するその他の金額も存在します。</span><span class="sxs-lookup"><span data-stu-id="cb075-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. @SysTaskRecorder:_RequestClose


