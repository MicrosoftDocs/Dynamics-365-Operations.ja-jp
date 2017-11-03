---
title: "複数の立ち寄りを伴なう貨物輸送ルートを計画する"
description: "この記事では、Dynamics 365 for Finance and Operations で輸送ルートを計画するために使用するさまざまな要素について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fea84bc0f40a1a25ce0cc252b6bb58fad2a2a501
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a><span data-ttu-id="22796-103">複数の立ち寄りを伴なう貨物輸送ルートを計画する</span><span class="sxs-lookup"><span data-stu-id="22796-103">Plan freight transportation routes with multiple stops</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="22796-104">この記事では、Microsoft Dynamics 365 for Finance and Operations、Enterprise エディションで輸送ルートを計画するために使用するさまざまな要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="22796-104">This article describes the various elements that you use to plan transportation routes in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="22796-105">複数の立ち寄りを伴う複雑な輸送ルートには、ルート計画およびルート ガイドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="22796-105">You can use route plans and route guides for complex transportation routes that have multiple stops.</span></span> <span data-ttu-id="22796-106">同じルートが定期的に使用される場合は、定期ルートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="22796-106">If the same route will be used on a regular basis, you can set up a scheduled route.</span></span>

## <a name="route-plans"></a><span data-ttu-id="22796-107">工順計画</span><span class="sxs-lookup"><span data-stu-id="22796-107">Route plans</span></span>
<span data-ttu-id="22796-108">ルート計画には、ルート上の立ち寄り先、および各セグメントに使用される配送業者に関する情報を提供しているルート セグメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="22796-108">A route plan contains route segments that provide information about the stops that are visited on the route and the carriers that are used for each segment.</span></span> <span data-ttu-id="22796-109">ルート上の立ち寄り先をハブとして定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22796-109">You must define the stops on the route as hubs.</span></span> <span data-ttu-id="22796-110">ハブは、仕入先、倉庫、顧客や、配送業者を変更する積地とすることができます。</span><span class="sxs-lookup"><span data-stu-id="22796-110">A hub can be a vendor, a warehouse, a customer, or even just a reloading place where you change carrier.</span></span> <span data-ttu-id="22796-111">各セグメントに対して、さまざまな請求金額の「スポット レート」を定義できます。</span><span class="sxs-lookup"><span data-stu-id="22796-111">For each segment, you can define “spot rates” for various charges.</span></span> <span data-ttu-id="22796-112">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="22796-112">Here are some examples:</span></span>

-   <span data-ttu-id="22796-113">指定されたセグメントへの旅費の請求金額</span><span class="sxs-lookup"><span data-stu-id="22796-113">Charges for travelling to the given segments</span></span>
-   <span data-ttu-id="22796-114">商品のピックアップ料金</span><span class="sxs-lookup"><span data-stu-id="22796-114">Charges for a picking up the goods</span></span>
-   <span data-ttu-id="22796-115">商品配送料金</span><span class="sxs-lookup"><span data-stu-id="22796-115">Charges for dropping off the goods</span></span>

<span data-ttu-id="22796-116">各ルート計画は、ルート ガイドと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="22796-116">Each route plan must be associated with a route guide.</span></span>

## <a name="route-guides"></a><span data-ttu-id="22796-117">ルート ガイド</span><span class="sxs-lookup"><span data-stu-id="22796-117">Route guides</span></span>
<span data-ttu-id="22796-118">ルート ガイドは、積荷を特定のルート計画と照合するための基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="22796-118">A route guide defines the criteria for matching a load to a specific route plan.</span></span> <span data-ttu-id="22796-119">例えば、発送元のハブと目的地のハブ、コンテナー容積または重量の制限、および出荷の配送業者、サービス、またはグループを指定できます。</span><span class="sxs-lookup"><span data-stu-id="22796-119">For example, you can specify an origin hub and a destination hub, limits for the container volume or weight, and a shipping carrier, service, or group.</span></span> <span data-ttu-id="22796-120">ルート ガイドは、積荷を手動または自動でルートと照合できる [**レート工順ワークベンチ**] ページで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="22796-120">Route guides are available on the **Rate route workbench** page, where loads can be matched to routes either manually or automatically.</span></span> <span data-ttu-id="22796-121">定期ルートのルート ガイドの場合は、[**積荷構築ワークベンチ**] ページでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="22796-121">If the route guide is for a scheduled route, it's also available on the **Load building workbench** page.</span></span>

## <a name="scheduled-routes"></a><span data-ttu-id="22796-122">スケジュール済み工順</span><span class="sxs-lookup"><span data-stu-id="22796-122">Scheduled routes</span></span>
<span data-ttu-id="22796-123">定期ルートは、出荷日のスケジュールが決まっている事前定義されたルート計画です。</span><span class="sxs-lookup"><span data-stu-id="22796-123">A scheduled route is a predefined route plan that has a schedule for the shipping dates.</span></span> <span data-ttu-id="22796-124">定期ルートと非定期ルートは、積荷が割り当てられる方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="22796-124">Scheduled routes and non-scheduled routes differ in the way that loads are assigned to them.</span></span> <span data-ttu-id="22796-125">[レート工順ワークベンチ] を使用して非定期ルートを割り当てると、積荷とルート ガイドだけが検証されます。</span><span class="sxs-lookup"><span data-stu-id="22796-125">If you assign a non-scheduled route by using the Rate route workbench, only the load and the route guide are validated.</span></span> <span data-ttu-id="22796-126">定期ルートを割り当てると、注文書とハブの日付および住所、およびルート計画上の日付も考慮されます。</span><span class="sxs-lookup"><span data-stu-id="22796-126">If you assign a scheduled route, the dates and addresses from the orders and the hubs, and the date on the route plan, are also considered.</span></span> <span data-ttu-id="22796-127">手動で積荷を定期ルートに割り当てる場合は、[レート工順ワークベンチ] ページを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="22796-127">You don't have to use the Rate route workbench page to manually assign loads to a scheduled route.</span></span> <span data-ttu-id="22796-128">代わりに、[積荷構築ワークベンチ] を使用して、指定された定期ルートに対して販売注文の顧客の住所および配送日に基づいて積荷を構築するよう提案することができます。</span><span class="sxs-lookup"><span data-stu-id="22796-128">Instead, you can use the Load building workbench to suggest that loads be built based on the customer addresses and delivery dates from sales orders for a given scheduled route.</span></span> <span data-ttu-id="22796-129">定期ルートの場合、ルート計画の発送元と発送先のハブは固定となります。</span><span class="sxs-lookup"><span data-stu-id="22796-129">For scheduled routes, the route plan will have fixed origin and destination hubs.</span></span> <span data-ttu-id="22796-130">通常、出荷配送業者およびサービスはすべてのセグメントで同じですが、変えることもできます。</span><span class="sxs-lookup"><span data-stu-id="22796-130">Typically, the shipping carrier and service will be the same for all segments, but they can differ.</span></span> <span data-ttu-id="22796-131">発送元のハブは、ルート上の立ち寄り先である顧客の郵便番号を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="22796-131">The destination hubs are created by using the postal codes of the customers that are visited on the route.</span></span> <span data-ttu-id="22796-132">1 つのルート計画に対して複数のルート スケジュールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="22796-132">Several route schedules can be defined for one route plan.</span></span> <span data-ttu-id="22796-133">ルート計画は、ルート ガイドと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="22796-133">The route plan must be associated with a route guide.</span></span> <span data-ttu-id="22796-134">ただし定期ルートの場合、計画に関連付けることができるルート ガイドは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="22796-134">However, for scheduled routes, the plan can be associated with only one route guide.</span></span> <span data-ttu-id="22796-135">工順スケジュールは、[**工順スケジュール**] ページで実際のルートを作成するためだけに使用されます。</span><span class="sxs-lookup"><span data-stu-id="22796-135">The route schedule is used only to create the actual routes on the **Route schedule** page.</span></span> <span data-ttu-id="22796-136">[積荷構築ワークベンチ] で積荷を提案する際に、既定の積荷テンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="22796-136">You can use the default load template when you propose loads on the Load building workbench.</span></span>

## <a name="load-building-workbench"></a><span data-ttu-id="22796-137">積荷構築ワークベンチ</span><span class="sxs-lookup"><span data-stu-id="22796-137">Load building workbench</span></span>
<span data-ttu-id="22796-138">[積荷構築ワークベンチ] では、販売注文の顧客の住所と配送日、および使用可能な定期ルートを使用して積荷を提案します。</span><span class="sxs-lookup"><span data-stu-id="22796-138">The Load building workbench uses the customer addresses and delivery dates from sales orders, and the scheduled routes that are available, to propose a load.</span></span> <span data-ttu-id="22796-139">既定では、ルートからの値がワークベンチに入力されます。</span><span class="sxs-lookup"><span data-stu-id="22796-139">By default, the values from the route are entered on the workbench.</span></span> <span data-ttu-id="22796-140">ただし、ルート上の「開始」日より前の「開始」日を選択できます。</span><span class="sxs-lookup"><span data-stu-id="22796-140">However, you can select a "from" date that is earlier than the "from" date on the route.</span></span> <span data-ttu-id="22796-141">荷重を提案すると、すべてのオープン販売注文の配送日と配送先住所がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="22796-141">When a load is proposed, the delivery address and delivery date of all open sales orders are checked.</span></span> <span data-ttu-id="22796-142">配送先住所の郵便番号がルート計画のハブの郵便番号と一致していて、配送日が基準で選択されている範囲内であれば、積荷に対して販売注文が提案されます。</span><span class="sxs-lookup"><span data-stu-id="22796-142">If the postal code of the delivery address matches the postal code of a hub in the route plan, and if the delivery date is within the range that is selected in the criteria, the sales order is proposed for the load.</span></span> <span data-ttu-id="22796-143">積荷テンプレートの容量も考慮されます。</span><span class="sxs-lookup"><span data-stu-id="22796-143">The capacity of the load template is also considered.</span></span> <span data-ttu-id="22796-144">1 度に 1 つの積荷だけが提案されます。</span><span class="sxs-lookup"><span data-stu-id="22796-144">Only one load is proposed at a time.</span></span> <span data-ttu-id="22796-145">含まれていない販売注文がある場合は、別の積荷テンプレート (たとえば、より大型のトラックやコンテナー用の積荷テンプレートなど) を使用するか、特別配送を計画する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="22796-145">If you have a sales order that isn't included, you might have to use a different load template (for example, a load template for a bigger truck or container) or plan an extra delivery.</span></span>




