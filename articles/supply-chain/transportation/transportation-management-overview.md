---
title: "輸送管理の概要"
description: "このトピックでは、Microsoft Dynamics 365 for Finance および Operations の輸送管理機能の概要が示されます。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 918167a3ab72b3d3665cf710d8e509417b94a056
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="transportation-management-overview"></a><span data-ttu-id="34400-103">輸送管理の概要</span><span class="sxs-lookup"><span data-stu-id="34400-103">Transportation management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34400-104">このトピックでは、Microsoft Dynamics 365 for Finance および Operations の輸送管理機能の概要が示されます。</span><span class="sxs-lookup"><span data-stu-id="34400-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="34400-105">輸送管理では、会社の配送の送受信オーダーの仕入先とルート指定の解決策の識別を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="34400-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="34400-106">たとえば、出荷用の最速のルートまたは最低費用レートを識別できます。</span><span class="sxs-lookup"><span data-stu-id="34400-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="34400-107">次の表では、Microsoft Dynamics 365 for Finance および Operations で輸送管理を使用する主要なシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="34400-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34400-108">シナリオ</span><span class="sxs-lookup"><span data-stu-id="34400-108">Scenario</span></span></th>
<th><span data-ttu-id="34400-109">輸送管理が役立つ方法</span><span class="sxs-lookup"><span data-stu-id="34400-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34400-110">配送活動に外部物流プロバイダを使用します。</span><span class="sxs-lookup"><span data-stu-id="34400-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="34400-111">入庫または出庫輸送に輸送管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="34400-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34400-112">会社の固有フリートを、出荷または集配のために使用でき、配送料が顧客に渡されます。</span><span class="sxs-lookup"><span data-stu-id="34400-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="34400-113">出荷プロセスで、配送料を確認し、顧客に渡すために輸送管理を使用できます。</span><span class="sxs-lookup"><span data-stu-id="34400-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="34400-114">ただし、配送業者の請求書調整プロセスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="34400-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34400-115">会社の固有フリートは、出荷または集配のために使用できますが、製品の価格に輸送費が含まれているため、配送料は顧客には渡されません。</span><span class="sxs-lookup"><span data-stu-id="34400-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="34400-116">多くの輸送管理機能は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="34400-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="34400-117">ただし、配送率を確認し、それに応じて販売価格を調整する場合、配送管理を使用できます。</span><span class="sxs-lookup"><span data-stu-id="34400-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34400-118">同じ会社の別の法人によって物流サービスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="34400-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="34400-119">その他の配送業者など、他の法人による処理によって輸送管理を使用できます。</span><span class="sxs-lookup"><span data-stu-id="34400-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="34400-120">法人間の経済取引を自動化することはできません。</span><span class="sxs-lookup"><span data-stu-id="34400-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="34400-121">そのため、これらのトランザクションを手動で処理する必要があります (発注書の作成など)。</span><span class="sxs-lookup"><span data-stu-id="34400-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="34400-122">物流サービスを提供する法人の場合でも、配送率を決定するために輸送管理を使用できます。</span><span class="sxs-lookup"><span data-stu-id="34400-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="34400-123">Finance および Operations の配送計画</span><span class="sxs-lookup"><span data-stu-id="34400-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="34400-124">輸送管理では、 輸送計画は注文またはその注文に基づいて作成された出荷に基づきます。</span><span class="sxs-lookup"><span data-stu-id="34400-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="34400-125">出荷は特定の時点で常に存在しますが、輸送計画に必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="34400-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="34400-126">移動オーダーは出荷シナリオの一部で、販売注文と共に計画できます。</span><span class="sxs-lookup"><span data-stu-id="34400-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![積荷図面](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="34400-128">入庫輸送</span><span class="sxs-lookup"><span data-stu-id="34400-128">Inbound transportation</span></span>
<span data-ttu-id="34400-129">仕入先から品目を発注し、その品目を倉庫に配達する必要がある場合は、品目の輸送を自分で手配することができます。</span><span class="sxs-lookup"><span data-stu-id="34400-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="34400-130">入庫積荷の輸送および入庫の計画に、Finance および Operations を使用できます。</span><span class="sxs-lookup"><span data-stu-id="34400-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="34400-131">次の図は、入庫積荷用の輸送を計画するための業務プロセス フローを示します。</span><span class="sxs-lookup"><span data-stu-id="34400-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![積荷の入庫輸送の業務プロセス フロー](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="34400-133">出庫輸送</span><span class="sxs-lookup"><span data-stu-id="34400-133">Outbound transportation</span></span>
<span data-ttu-id="34400-134">会社の倉庫から顧客に特定の品目を出荷する場合は、出荷積荷を計画および処理できます。</span><span class="sxs-lookup"><span data-stu-id="34400-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="34400-135">出庫積荷の輸送および出荷の計画に、Finance および Operations を使用できます。</span><span class="sxs-lookup"><span data-stu-id="34400-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="34400-136">次の図は、出荷用の出荷積荷を計画および処理するための業務プロセス フローを示します。</span><span class="sxs-lookup"><span data-stu-id="34400-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![出庫積荷の計画および処理](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="34400-138">積荷構築</span><span class="sxs-lookup"><span data-stu-id="34400-138">Load building</span></span>
<span data-ttu-id="34400-139">Finance および Operations には、容積ベースの積荷構築戦略という積荷構築戦略が用意されています。</span><span class="sxs-lookup"><span data-stu-id="34400-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="34400-140">この戦略を使用すると、積荷テンプレートの高さと重量に対して指定される最大値を使用できるし、または新しい値を入力して設定を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="34400-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="34400-141">この戦略を使用するには、[**積荷構築ワークベンチ**] ページの [**設定**] クイック タブの [**積荷構築戦略**] フィールドで戦略を選択します。</span><span class="sxs-lookup"><span data-stu-id="34400-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="34400-142">また、アプリケーション オブジェクト ツリー (AOT) で新しいクラスを作成して、独自の積荷構築戦略を追加できます。</span><span class="sxs-lookup"><span data-stu-id="34400-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




