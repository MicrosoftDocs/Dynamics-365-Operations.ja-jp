---
title: 単一レベル構造を使用した BOM の計算 (2016 年 2 月)
description: この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013eddf1ba8e8cab3c87cb1f063d9bf886b0f833
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821396"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="3d40c-103">単一レベル構造を使用した BOM の計算 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="3d40c-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d40c-104">この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3d40c-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="3d40c-105">これは、BOM 計算シリーズの 6 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="3d40c-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="3d40c-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="3d40c-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="3d40c-107">[リリースされた製品] に進みます。</span><span class="sxs-lookup"><span data-stu-id="3d40c-107">Go to Released products.</span></span>
2. <span data-ttu-id="3d40c-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="3d40c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3d40c-109">製品 BOM_1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d40c-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="3d40c-110">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d40c-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="3d40c-111">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d40c-111">Click Item price.</span></span>
5. <span data-ttu-id="3d40c-112">[品目原価の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d40c-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="3d40c-113">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d40c-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="3d40c-114">[原価計算バージョン] フィールドで、ドロップ ダウン ボタンをクリックして、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="3d40c-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3d40c-115">このデモでは、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d40c-115">For this demo, select 10.</span></span> <span data-ttu-id="3d40c-116">これは、原価価格をコンポーネントに追加する際に使用される、同じ原価バージョンです。</span><span class="sxs-lookup"><span data-stu-id="3d40c-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="3d40c-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d40c-117">Click OK.</span></span>
8. <span data-ttu-id="3d40c-118">[計算の詳細の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d40c-118">Click View calculation details.</span></span>
    * <span data-ttu-id="3d40c-119">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d40c-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="3d40c-120">コストの構成は次のとおりです:  \*    10 は ITEM_A から、 10 は ITEM_B から、 10 は BOM_2 から派生します。</span><span class="sxs-lookup"><span data-stu-id="3d40c-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="3d40c-121">この場合、BOM_2 は計算によってではなく、標準原価 10 として入力されたので、その詳細はありません。</span><span class="sxs-lookup"><span data-stu-id="3d40c-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="3d40c-122">\*    7 は一定のコストである段取り時間から派生し、追加の 7 は実行時操作 (プロセス) から派生します。</span><span class="sxs-lookup"><span data-stu-id="3d40c-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="3d40c-123">\*    間接原価に対応する他の金額もあります。</span><span class="sxs-lookup"><span data-stu-id="3d40c-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="3d40c-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="3d40c-124">@SysTaskRecorder:_RequestClose</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]