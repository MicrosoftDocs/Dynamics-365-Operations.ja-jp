---
title: "ハブ連結を使用した積荷計画"
description: "この記事では、同じ顧客に別の倉庫からの商品を配送する場合、または同じ倉庫に複数の仕入先から商品が配送された場合に、1 つのハブに出荷を統合する機能について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3145febe40108e50b263514de1ca541dd914b7c5
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="94b42-103">ハブ連結を使用した積荷計画</span><span class="sxs-lookup"><span data-stu-id="94b42-103">Plan loads using hub consolidation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="94b42-104">この記事では、同じ顧客に別の倉庫からの商品を配送する場合、または同じ倉庫に複数の仕入先から商品が配送された場合に、1 つのハブに出荷を統合する機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="94b42-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="94b42-105">同じ顧客に別の倉庫からの商品を配送する場合、または同じ倉庫に複数の仕入先から製品が配送された場合に、1 つのハブに出荷を統合するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="94b42-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="94b42-106">積荷構築</span><span class="sxs-lookup"><span data-stu-id="94b42-106">Building loads</span></span>
<span data-ttu-id="94b42-107">ハブの統合を使用する前に、[**輸送管理パラメーター**] ページの [**輸送計画中**] オプションを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b42-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="94b42-108">統合が行われるハブを作成する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="94b42-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="94b42-109">次の図は、ハブの統合の例を示します。</span><span class="sxs-lookup"><span data-stu-id="94b42-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="94b42-110">この例では、異なる倉庫からの販売注文が同じお客様に配送されます。</span><span class="sxs-lookup"><span data-stu-id="94b42-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="94b42-111">[**積荷計画ワークベンチ**] ページを使用して、通常の方法で販売注文に基づいて基本的な積荷が作成されます。</span><span class="sxs-lookup"><span data-stu-id="94b42-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="94b42-112">顧客に配送される前に 1 つのハブにある 2 つの積荷を統合するため、[**積荷計画ワークベンチ**] ページの [**輸送**] フィールドで、[**ハブの連結**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="94b42-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="94b42-113">各積荷に対して適切なハブを選択すると、「配送先」の行先としてのハブが積荷に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="94b42-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="94b42-114">[**積荷計画ワークベンチ**] ページの [**供給と需要**] セクションには、2 つの「輸送要求明細行」もあります。</span><span class="sxs-lookup"><span data-stu-id="94b42-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="94b42-115">次にこれらの 2 つの明細行を新しい積荷に追加します。</span><span class="sxs-lookup"><span data-stu-id="94b42-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="94b42-116">この新しい積荷には、両方の販売注文明細行があり、「集荷先」の住所としてのハブ、「配送」先としての顧客 A もあります。</span><span class="sxs-lookup"><span data-stu-id="94b42-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="94b42-117">次に 3 つの積荷の配送準備が完了し、他の積荷と同様にルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="94b42-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="94b42-118">各積荷に対する、出荷配送業者のシステム提案の選択もできます。</span><span class="sxs-lookup"><span data-stu-id="94b42-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="94b42-119">[![ハブの連結](./media/hubconsol.jpg)](./media/hubconsol.jpg) 複数の移動オーダーに対して積荷を統合するために、同一の方法を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="94b42-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="94b42-120">この例では、前の図での顧客 A は、倉庫です。</span><span class="sxs-lookup"><span data-stu-id="94b42-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="94b42-121">または、積荷を複数の発注書に統合できます。それにより同じ倉庫に異なるベンダーから積荷が配送されます。</span><span class="sxs-lookup"><span data-stu-id="94b42-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="94b42-122">複数の統合ハブを作成することが可能で、異なる倉庫から複数の積荷を複数のハブに統合できます。</span><span class="sxs-lookup"><span data-stu-id="94b42-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="94b42-123">基本的な積荷を構築し、ハブの統合オプションを使用した後に、統合輸送要求明細行を使用して、新しい積荷を構築します。</span><span class="sxs-lookup"><span data-stu-id="94b42-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="94b42-124">次に積荷をレートおよびルートします。</span><span class="sxs-lookup"><span data-stu-id="94b42-124">You then rate and route your loads.</span></span>




