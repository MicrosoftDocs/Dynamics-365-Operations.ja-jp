---
title: ファントム品目
description: このトピックでは、部品表 (BOM) の明細行および Microsoft Dynamics 365 for Finance and Operations のフォーミュラで、ファントム明細行タイプを使用する方法を詳細に説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "341813"
---
# <a name="phantom-items"></a><span data-ttu-id="9c89a-103">ファントム品目</span><span class="sxs-lookup"><span data-stu-id="9c89a-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c89a-104">このトピックでは、部品表 (BOM) の明細行およびフォーミュラで、ファントム明細行タイプを利用する方法を詳細に説明します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="9c89a-105">次の図では、(a) は製品 H およびパーツ F と G の BOM、(b) は製品 H およびパーツ F の工順シートです。</span><span class="sxs-lookup"><span data-stu-id="9c89a-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![製品 H およびパーツ F](media/product-H-part-F.png)


<span data-ttu-id="9c89a-107">次の図は、2 つのレベルでの BOM 構造の例を示します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="9c89a-108">完成した製品 H は、機械アセンブリの製品を表します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="9c89a-109">機械アセンブリは、2 つの材料 (A と B) を持つ電気単位 (F)、および 2 つの材料 (C と D) も持つ梱包材のグループ (G) の 2 つの部分から構成されます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="9c89a-110">他の材料 (E) は、機械の一般的なアセンブリで使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-110">Another material (E) is used during the general assembly of the machine.</span></span>

![製品 H およびパーツ F](media/product-H-part-B.png)

<span data-ttu-id="9c89a-112">前の図は製品 H のエンジニアリング BOM を表します。この構造はパーツおよび機械アセンブリ全体のコンポーネントの適正な概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="9c89a-113">ただし、製品デザイナーがこの方法で表される BOM を好む場合でも、この構造では作業現場で機械が構築される方法が正しく表されていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9c89a-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="9c89a-114">たとえば、前の図でエンジニアリング BOM は、その電気単位 F が別のワーク オーダーで別のパーツとして組み立てられていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="9c89a-115">ただし、作業現場では、別のワーク オーダーとしてではなく、機械アセンブリ全体のパーツとして電気単位を組み立てるのにより最適であると判断される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9c89a-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="9c89a-116">このエンジニアリング BOM は、パーツ G が別のパーツであることも示します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="9c89a-117">ただし、この構造では、パーツ G は現物パーツでなく梱包材のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="9c89a-118">したがって、エンジニアリング BOM は製品のデザインおよびそのデザインのメンテナンスに大きな価値を提供しますが、製品の製造実行プロセスをサポートする最も論理的な方法ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9c89a-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="9c89a-119">対照的に、製造 BOM は製品を構築する最善の方法を表します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="9c89a-120">次の図は、前のエンジニアリング BOM を製造 BOM に移行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="9c89a-121">この図では、(a) は製品 H の BOM、b は製品 H の工順シートです。</span><span class="sxs-lookup"><span data-stu-id="9c89a-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="9c89a-122">この構造では、パーツ F および G の概念がなく、これらのパーツで構成される材料が次の BOM レベルに上昇したことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="9c89a-123">2 つの操作シートがあったエンジニアリング BOM とは異なり、製造 BOM には 1 つの操作シートのみがあります。</span><span class="sxs-lookup"><span data-stu-id="9c89a-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="9c89a-124">パーツ G にリンクされた梱包操作も上昇し、製品 H の操作シートの一部になりました。電気単位のアセンブリは最初の操作です。</span><span class="sxs-lookup"><span data-stu-id="9c89a-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="9c89a-125">この単位は次の操作である機械アセンブリに使用されるため、この順序は理にかなっています。</span><span class="sxs-lookup"><span data-stu-id="9c89a-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="9c89a-126">最後の操作は、2 つの梱包材 (C と D) を消費する梱包操作です。</span><span class="sxs-lookup"><span data-stu-id="9c89a-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="9c89a-127">Microsoft Dynamics 365 for Finance and Operations、ファントム BOM 明細行タイプを通してエンジニアリング BOM と製造 BOM 間での移行が有効になります。</span><span class="sxs-lookup"><span data-stu-id="9c89a-127">In Microsoft Dynamics 365 for Finance and Operations, the transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="9c89a-128">「ファントム」という用語が示すように、パーツ F および G が 2 つの BOM タイプ間の移行中に実在しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="9c89a-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="9c89a-129">この例では、エンジニアリング BOM で、ファントム明細行タイプがパーツ F および G の BOM 明細行に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="9c89a-130">製造オーダーまたはバッチ オーダーが作成されると、エンジニアリング BOM は製造オーダーまたはバッチ オーダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="9c89a-131">次に、前の図に示すように、オーダーの見積時にエンジニアリング BOM から製造 BOM への移行が発生します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="9c89a-132">2 番目の図の操作シートから、操作用に梱包材 C および D が入力されます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="9c89a-133">複数レベルのファントム BOM 構造</span><span class="sxs-lookup"><span data-stu-id="9c89a-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="9c89a-134">次の図に示すように、ファントム明細行タイプは複数レベルの BOM 構造で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="9c89a-135">この図では、(a) は製品 G の BOM、(b) はパーツ E と F および製品 G の工順シートです。</span><span class="sxs-lookup"><span data-stu-id="9c89a-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![工順シートを含む製品 G およびパーツ F](media/product-G-route-sheet-G.png)


<span data-ttu-id="9c89a-137">次の図では、パーツ E および F の BOM 明細行が、明細行タイプがファントムであるようコンフィギュレーションされている場合に、製造 BOM と工順シートの計算結果を示します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="9c89a-138">この図では、(a) は製品 G の BOM、(b) は製品 G の工順シートです。</span><span class="sxs-lookup"><span data-stu-id="9c89a-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![製品 G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="9c89a-140">ファントムおよび工順ネットワーク</span><span class="sxs-lookup"><span data-stu-id="9c89a-140">Phantom and route network</span></span>
<span data-ttu-id="9c89a-141">ファントム BOM は、工順ネットワークのある BOM にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="9c89a-142">工順ネットワークでは、1 つ以上の操作が並列実行されます。</span><span class="sxs-lookup"><span data-stu-id="9c89a-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="9c89a-143">次の図は、複数レベルの BOM で使用される工順ネットワークの例を示します。</span><span class="sxs-lookup"><span data-stu-id="9c89a-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="9c89a-144">この図では、(a) は製品 G およびパーツ F のBOM、(b) は工順ネットワークのある製品 G およびパーツ F の工順シートです。</span><span class="sxs-lookup"><span data-stu-id="9c89a-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![製品 G およびパーツ F](media/product-G-part-F.png)


<span data-ttu-id="9c89a-146">次の図では、(a) は製品 G およびパーツ F の BOM、(b) は製品 G およびパーツ F の工順シートです。</span><span class="sxs-lookup"><span data-stu-id="9c89a-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![工順シートを含む製品 G およびパーツ F](media/product-G-part-F-with-route-sheet.png)
