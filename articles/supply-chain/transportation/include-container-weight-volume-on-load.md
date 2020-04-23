---
title: 積荷のコンテナーの重量と容積を含める
description: このトピックでは、積荷のコンテナーの重量と容積を含めるための機能を設定および適用する方法について説明します。
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e6b29bf2e42ea2df3d36f39fa577078009aa584
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206291"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="f8b52-103">積荷のコンテナーの重量と容積を含める</span><span class="sxs-lookup"><span data-stu-id="f8b52-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8b52-104">積荷のコンテナーの重量と容積を含める機能は、積載するコンテナーと品目の合計重量および容積を明確に表示します。</span><span class="sxs-lookup"><span data-stu-id="f8b52-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="f8b52-105">積荷には単一または複数の出荷が含まれており、これらの出荷には単一つの販売注文または複数の販売注文に属する特徴的品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f8b52-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="f8b52-106">品目は、コンテナーに内部格納され、コンテナーは積荷に積載されます。</span><span class="sxs-lookup"><span data-stu-id="f8b52-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="f8b52-107">コンテナーの外部にある品目も、積荷の一部となります。</span><span class="sxs-lookup"><span data-stu-id="f8b52-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="f8b52-108">これらの条件に基づき、システムはコンテナーと品目両方の重量および容積を考慮して、積荷の重量および容積を計算します。</span><span class="sxs-lookup"><span data-stu-id="f8b52-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="f8b52-109">計算された値が詳細でない場合は、積荷の重量および容積の実際の値を入力することで調整できます。</span><span class="sxs-lookup"><span data-stu-id="f8b52-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="f8b52-110">重量および容積の値は、輸送管理プロセスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8b52-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="f8b52-111">たとえば、値は工順ワークベンチの評価に使用されます。それは積荷のレートとルートを定義するのに役立ち、輸送業者および配送担当者のチェックインにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8b52-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f8b52-112">該当する場所</span><span class="sxs-lookup"><span data-stu-id="f8b52-112">Where it applies</span></span>

<span data-ttu-id="f8b52-113">積荷のコンテナーの重量と容積を含める機能は、工順ワークベンチの評価、輸送業者、および配送担当者のチェックインなどの、輸送管理プロセスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="f8b52-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="f8b52-114">設定方法</span><span class="sxs-lookup"><span data-stu-id="f8b52-114">How it is set up</span></span>

<span data-ttu-id="f8b52-115">考慮する必要がある積荷のコンテナーの数は、コンテナーの重量および容積、さらに使用されるコンテナーの割合に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="f8b52-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="f8b52-116">コンテナーの重量と容積を設定するには、**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー タイプ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8b52-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="f8b52-117">コンテナー使用率の割合を設定するには、**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー グループ** の順にクリックし、**コンテナー使用率の割合** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8b52-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>
