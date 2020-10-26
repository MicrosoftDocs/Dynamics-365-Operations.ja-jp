---
title: 複数レベル構造を使用した BOM の計算 (2016 年 2 月)
description: この手順は、原価表に基づく複数レベル展開を使用して、完成品のコストを計算する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f0ec28a20d32fc38cd6e77a76a02fc9544db3ca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977075"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="9e167-103">複数レベル構造を使用した BOM の計算 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="9e167-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e167-104">この手順は、原価表に基づく複数レベル展開を使用して、完成品のコストを計算する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9e167-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="9e167-105">これは、BOM 計算シリーズの 7 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="9e167-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="9e167-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="9e167-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="9e167-107">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e167-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9e167-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e167-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e167-109">製品 BOM_1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e167-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="9e167-110">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e167-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="9e167-111">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e167-111">Click Item price.</span></span>
5. <span data-ttu-id="9e167-112">[品目原価の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e167-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="9e167-113">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e167-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="9e167-114">[原価計算バージョン] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e167-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="9e167-115">原価計算バージョン 20 を選択します。その理由は、これが予定原価タイプであり、展開モードが複数レベルのためです。</span><span class="sxs-lookup"><span data-stu-id="9e167-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="9e167-116">複数レベル展開モードは、予定原価およびシミュレーション用です。</span><span class="sxs-lookup"><span data-stu-id="9e167-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="9e167-117">これは、標準原価には使用されません。</span><span class="sxs-lookup"><span data-stu-id="9e167-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="9e167-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e167-118">Click OK.</span></span>
8. <span data-ttu-id="9e167-119">[計算の詳細の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e167-119">Click View calculation details.</span></span>
    * <span data-ttu-id="9e167-120">省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e167-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="9e167-121">この場合、このシリーズの最初のタスク ガイドで有効化された標準原価 10 ではなく、原材料、プロセス、および合計 29,40 の間接費を考慮して BOM_2 がどのように計算されたかに注目してください。</span><span class="sxs-lookup"><span data-stu-id="9e167-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="9e167-122">[原価計算表] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e167-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="9e167-123">[原価計算表] タブに移動したとき、原価グループごとの合計が以前のタスク ガイド内で行った計算と比較して異なります。</span><span class="sxs-lookup"><span data-stu-id="9e167-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="9e167-124">[レベル] フィールドで、「複数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e167-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="9e167-125">[複数] を選択すると、原価は BOM_2 の構成に従って分類されます。すなわち、10 は M1 原価グループ (ITEM_C) から派生し、15,60 は原価グループが L2 の製造から派生します。</span><span class="sxs-lookup"><span data-stu-id="9e167-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="9e167-126">また、間接原価も変化します。</span><span class="sxs-lookup"><span data-stu-id="9e167-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="9e167-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e167-127">Close the page.</span></span>
12. <span data-ttu-id="9e167-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e167-128">Close the page.</span></span>

