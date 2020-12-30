---
title: 標準原価の更新の管理
description: 標準原価データの更新は、1 バージョン アプローチまたは 2 バージョン アプローチという 2 つの異なるアプローチを使用して管理できます。
author: AndersGirke
manager: tfehr
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a7beeafa6d0bb22a687278ccebc3127409e1ee0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432016"
---
# <a name="manage-standard-cost-updates"></a><span data-ttu-id="54798-103">標準原価の更新の管理</span><span class="sxs-lookup"><span data-stu-id="54798-103">Manage standard cost updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54798-104">標準原価データの更新は、1 バージョン アプローチまたは 2 バージョン アプローチという 2 つの異なるアプローチを使用して管理できます。</span><span class="sxs-lookup"><span data-stu-id="54798-104">Updates to standard cost data can be managed by using two different approaches - the one-version approach or the two-version approach.</span></span> 

<span data-ttu-id="54798-105">1 バージョン アプローチでは、すべての原価レコードを格納する 1 つの原価バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="54798-105">The one-version approach uses a single costing version that contains all cost records.</span></span> <span data-ttu-id="54798-106">これらのレコードには、オリジナルの原価とすべての原価の更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="54798-106">These records include the original costs and all cost updates.</span></span>

<span data-ttu-id="54798-107">2 バージョン アプローチは、オリジナルの原価のレコードを含む 1 つのバージョンとすべての原価の更新のレコードを含む 2 番目のバージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="54798-107">The two-version approach uses one version that contains records of the original costs and a second version that contains records of all cost updates.</span></span> <span data-ttu-id="54798-108">2 バージョン アプローチの概念を使用すると、複数の差分更新を識別できます。</span><span class="sxs-lookup"><span data-stu-id="54798-108">A primary advantage of the two-version approach is the clear delineation and tracking of cost updates in a separate costing version, without affecting the original costing version.</span></span> <span data-ttu-id="54798-109">2 バージョン アプローチを使用すると、複数の差分更新を識別できます。この場合、差分更新ごとに、差分原価レコードを格納する別個の原価バージョンが用意されます。</span><span class="sxs-lookup"><span data-stu-id="54798-109">The two-version approach can be used to identify multiple incremental updates, where each incremental update has a separate costing version that contains the incremental cost records.</span></span> 

<span data-ttu-id="54798-110">**例**</span><span class="sxs-lookup"><span data-stu-id="54798-110">**Example**</span></span> 

<span data-ttu-id="54798-111">次の例では、1 バージョンと 2 バージョン アプローチを製造環境における標準原価更新に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="54798-111">The following example illustrates how the one-version and two-version approaches can be used for updating standard costs in a manufacturing environment.</span></span> <span data-ttu-id="54798-112">たとえば、新しい品目やエラー修正を反映する更新です。</span><span class="sxs-lookup"><span data-stu-id="54798-112">For example, updates that reflect new items or error corrections.</span></span> <span data-ttu-id="54798-113">単一の原価バージョンが、当年の標準原価を表すと仮定します。</span><span class="sxs-lookup"><span data-stu-id="54798-113">Assume that a single costing version represents the standard costs for the current year.</span></span> <span data-ttu-id="54798-114">このバージョンの識別子は 2016-STD です。</span><span class="sxs-lookup"><span data-stu-id="54798-114">The identifier for this version is 2016-STD.</span></span> <span data-ttu-id="54798-115">バージョン 2016-STD には、すべての品目の現在の有効原価が格納されています。</span><span class="sxs-lookup"><span data-stu-id="54798-115">Version 2016-STD contains the current active costs for all items.</span></span> <span data-ttu-id="54798-116">また、このバージョンには、すべての品目とすべての工順関連原価カテゴリの現在の有効原価と、2016 年度の開始時に明らかであった間接費の計算式が格納されています。</span><span class="sxs-lookup"><span data-stu-id="54798-116">Additionally, it contains all routing-related cost categories and overhead calculation formulas that were known at the start of the year 2016.</span></span> <span data-ttu-id="54798-117">2016-STD は、オリジナルの原価計算バージョンです。</span><span class="sxs-lookup"><span data-stu-id="54798-117">2016-STD is the original costing version.</span></span>

-   <span data-ttu-id="54798-118">**原価データの更新に対する 1 バージョン アプローチ** − 1 バージョン アプローチでは、オリジナルの原価バージョンである 2016-STD に、すべての原価レコードが格納されます。</span><span class="sxs-lookup"><span data-stu-id="54798-118">**One-version approach to cost data updates** − In the one-version approach, the original costing version 2016-STD contains all cost records.</span></span> <span data-ttu-id="54798-119">原価の更新は 2016-STD に記録され、ステータスが "保留中" に設定されます。</span><span class="sxs-lookup"><span data-stu-id="54798-119">Cost updates are recorded in 2016-STD and are set to a status of ”Pending.”</span></span> <span data-ttu-id="54798-120">保留中の原価を新しい購入品目に対して手動で入力したり、製造品目について計算して修正を反映したりできます。</span><span class="sxs-lookup"><span data-stu-id="54798-120">The pending costs can be manually entered for new purchased items, or they can be calculated for a manufactured item to reflect corrections.</span></span> <span data-ttu-id="54798-121">1 バージョン アプローチを使用する場合は、すべての有効原価が原価バージョンに格納されるため、予備のデータ ソースは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="54798-121">When the one-version approach is used, the BOM calculations do not require a fallback data source because all active costs are contained in the costing version.</span></span> <span data-ttu-id="54798-122">保留中の原価が有効になった後、オリジナルの原価バージョン 2016-STD に、現在のすべての有効原価が再度格納されます。</span><span class="sxs-lookup"><span data-stu-id="54798-122">After the pending costs become active, the original costing version 2016-STD will again contain all the current active costs.</span></span>
-   <span data-ttu-id="54798-123">**原価データの更新に対する 2 バージョン アプローチ** : 2 バージョン アプローチでは、原価の更新だけを格納する追加の原価バージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="54798-123">**Two-version approach to cost data updates** − The two-version approach requires an additional costing version that contains only the cost updates.</span></span> <span data-ttu-id="54798-124">このバージョンの識別子は 2016-STD-CHANGES です。</span><span class="sxs-lookup"><span data-stu-id="54798-124">The identifier for this version is 2016-STD-CHANGES.</span></span> <span data-ttu-id="54798-125">原価の更新は 2016-STD-CHANGES に記録され、ステータスが "保留中" に設定されます。</span><span class="sxs-lookup"><span data-stu-id="54798-125">Cost updates are recorded in 2016-STD-CHANGES and are set to a status of “Pending.”</span></span> <span data-ttu-id="54798-126">2 バージョン アプローチの場合、製造品目の保留中の原価の BOM の計算は、予備のデータ ソースを必要とします。</span><span class="sxs-lookup"><span data-stu-id="54798-126">With the two-version approach, the BOM calculations of pending costs for manufactured items require a fallback data source.</span></span> <span data-ttu-id="54798-127">これは、追加の原価バージョン 2016-STD-CHANGES には、原価データのサブセットだけが格納されるためです。</span><span class="sxs-lookup"><span data-stu-id="54798-127">This is because the additional costing version 2016-STD-CHANGES contains only a subset of cost data.</span></span> <span data-ttu-id="54798-128">予備は、有効原価として、または原価バージョン 2016-STD として表現できます。これは、2016-STD-CHANGES 内に原価データが含まれない場合、どちらで表現しても、原価データのソースが識別されるためです。</span><span class="sxs-lookup"><span data-stu-id="54798-128">The fallback can be expressed as the active costs or as the costing version 2016-STD, because both identify the source of cost data when it is not included in 2016-STD-CHANGES.</span></span> <span data-ttu-id="54798-129">保留中の原価が有効化になった後、原価バージョン 2016-STD-CHANGES には、更新を反映する現在の有効原価が格納され、オリジナルの原価バージョン 2016-STD は変更されません。</span><span class="sxs-lookup"><span data-stu-id="54798-129">After the pending costs become active, the costing version 2016-STD-CHANGES will contain the current active costs that reflect the updates, whereas the original costing version 2016-STD will be untouched.</span></span> <span data-ttu-id="54798-130">2 バージョン アプローチを使用する場合は、更新を禁止するようにオリジナルの原価バージョンのブロック ポリシーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54798-130">When the two-version approach is used, blocking policies for the original costing version should be set up to prevent updates.</span></span> <span data-ttu-id="54798-131">指定された開始日と、更新を許可するブロック ポリシーを選択により使用していることを除いて、追加の原価バージョンに対して同一のポリシーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54798-131">Identical blocking policies should be set up for the additional costing version, except for the specified from-date and the selective use of blocking policies to allow for updates.</span></span> <span data-ttu-id="54798-132">指定された開始日は、スケジュールされた有効化日付を反映するように、変更バッチごとに更新される必要があります。</span><span class="sxs-lookup"><span data-stu-id="54798-132">The specified from-date should be updated with each batch of changes to reflect the scheduled activation date.</span></span>

<span data-ttu-id="54798-133">この例では 1 つの追加の原価計算バージョンを使用して 2016 年度中の更新を管理します。</span><span class="sxs-lookup"><span data-stu-id="54798-133">This example used one additional costing version for managing updates throughout the year 2016.</span></span> <span data-ttu-id="54798-134">更新のバッチごとに異なるバージョンなどが使用され、複数の追加の原価計算バージョンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="54798-134">More than one additional costing version can be used, such as a separate version for each batch of updates.</span></span> <span data-ttu-id="54798-135">複数の追加の原価を使用する場合は、有効原価が複数の原価バージョンに拡散されるため、予備を有効原価として表現する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54798-135">When more than one additional costing is used, the fallback must be expressed as the active costs, because the active costs are spread over multiple costing versions.</span></span>





