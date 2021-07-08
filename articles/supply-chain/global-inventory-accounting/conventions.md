---
title: 規則
description: このトピックでは、グローバル在庫会計で原価を転記する方法を確立するための規則の設定方法について説明します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273186"
---
# <a name="conventions"></a><span data-ttu-id="7d927-103">規則</span><span class="sxs-lookup"><span data-stu-id="7d927-103">Conventions</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="7d927-104">規則は、システム動作に影響を及ぼす一連のポリシーのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="7d927-104">A convention is a container for a set of policies that affect system behavior.</span></span> <span data-ttu-id="7d927-105">業務上の要件に基づいて、グローバル在庫会計で原価を転記する方法を確立するさまざまなポリシーの組み合わせを使用して、規則を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d927-105">Based on your business requirements, you must define conventions by using a combination of the various policies that establish how costs should be accounted in Global Inventory Accounting.</span></span> <span data-ttu-id="7d927-106">各規則を 1 つ以上の元帳に関連付け、元帳間で適用される会計ポリシーで整合性を確保できます。</span><span class="sxs-lookup"><span data-stu-id="7d927-106">You can associate each convention with one or more ledgers to ensure consistency in accounting policies that are applied across ledgers.</span></span>

<span data-ttu-id="7d927-107">規則を設定するには、**グローバル在庫会計 \> 設定 \> 規則** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7d927-107">To set up your conventions, go to **Global inventory accounting \> Setup \> Conventions**.</span></span> <span data-ttu-id="7d927-108">各規則ごとに、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="7d927-108">For each convention, set the following fields:</span></span>

- <span data-ttu-id="7d927-109">**名前** - 規則の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d927-109">**Name** – Enter the name of the convention.</span></span>
- <span data-ttu-id="7d927-110">**説明** – 規則の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d927-110">**Description** – Enter a description of the convention.</span></span>
- <span data-ttu-id="7d927-111">**原価オブジェクト ポリシー** – 原価オブジェクト ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d927-111">**Cost Object policy** – Select a cost object policy.</span></span> <span data-ttu-id="7d927-112">これらのポリシーでは、在庫金額の計算および管理にシステムが適用する粒度のレベルが決定されます。</span><span class="sxs-lookup"><span data-stu-id="7d927-112">These policies determine the level of granularity that the system applies to calculate and maintain the inventory value.</span></span> <span data-ttu-id="7d927-113">次の事前定義済みのオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d927-113">The following predefined options are available:</span></span>

    - <span data-ttu-id="7d927-114">品目</span><span class="sxs-lookup"><span data-stu-id="7d927-114">Product</span></span>
    - <span data-ttu-id="7d927-115">製品 – サイト</span><span class="sxs-lookup"><span data-stu-id="7d927-115">Product – Site</span></span>
    - <span data-ttu-id="7d927-116">製品 – サイト – 倉庫</span><span class="sxs-lookup"><span data-stu-id="7d927-116">Product – Site – Warehouse</span></span>

    <span data-ttu-id="7d927-117">たとえば、すべての在庫移動 (流入または流出) に対して *製品 – サイト* を選択した場合、システムにより各製品の在庫原価がサイト レベルで計算および管理されます。</span><span class="sxs-lookup"><span data-stu-id="7d927-117">For example, if you select *Product – Site*, for every inventory movement (inflow or outflow), the system calculates and maintains the inventory cost of each product at the site level.</span></span> <span data-ttu-id="7d927-118">したがって、倉庫レベルなど、下位レベルの在庫移動は在庫金額に影響しません。</span><span class="sxs-lookup"><span data-stu-id="7d927-118">Therefore, inventory movements at lower levels, such as the warehouse level, don't affect the inventory value.</span></span> <span data-ttu-id="7d927-119">(倉庫レベル移動の例として 1 つのサイトにある 2 つの倉庫間の品目の移動があります。) 同様に、倉庫レベルなどの下位レベルの在庫原価を表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d927-119">(An example of a warehouse-level transfer is an item transfer between two warehouses in one site.) Likewise, you can't view the inventory cost at a lower level, such as the warehouse level.</span></span>

- <span data-ttu-id="7d927-120">**入力測定基準ポリシー** – 入力測定基準ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d927-120">**Input measurement basis policy** – Select an input measurement basis policy.</span></span> <span data-ttu-id="7d927-121">これらのポリシーでは、在庫勘定にフローする原価と請求される原価が決定されます。</span><span class="sxs-lookup"><span data-stu-id="7d927-121">These policies determine the costs that should flow into the inventory account and the costs that should be charged.</span></span> <span data-ttu-id="7d927-122">次のオプションは取引会社に関連します。</span><span class="sxs-lookup"><span data-stu-id="7d927-122">The following options are relevant for trading companies:</span></span>

    - <span data-ttu-id="7d927-123">**通常の履歴** – すべての原価コンポーネントが在庫勘定にフローします。</span><span class="sxs-lookup"><span data-stu-id="7d927-123">**Normal historical** – All the cost components flow into the inventory account.</span></span>
    - <span data-ttu-id="7d927-124">**標準** – 標準原価は在庫勘定にフローし、適用される原価と実際原価の差が差異勘定に請求されます。</span><span class="sxs-lookup"><span data-stu-id="7d927-124">**Standard** – Standard cost flows into the inventory accounts, and the difference between the applied cost and the actual costs is charged to variance accounts.</span></span> <span data-ttu-id="7d927-125">*標準* 入力測定基準ポリシーを作成する場合は、最初に、品目の標準原価をポリシーで参照できる価格リストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d927-125">If you want to create a *Standard* input measurement basis policy, you must first create a price list where the policy can look up the item's standard cost.</span></span>
    - <span data-ttu-id="7d927-126">**価格リスト** – グローバル在庫会計では、複数の法人からの品目価格のフェッチがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7d927-126">**Price lists** – Global Inventory Accounting supports fetching item prices from multiple legal entities.</span></span> <span data-ttu-id="7d927-127">入力測定基準ポリシーで使用する価格リストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7d927-127">You can define a price list that the input measurement basis policy will use.</span></span> <span data-ttu-id="7d927-128">このようにして、システムは品目価格を参照する場所を認識します。</span><span class="sxs-lookup"><span data-stu-id="7d927-128">In this way, the system will know where to look up the item price.</span></span> <span data-ttu-id="7d927-129">価格リストを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7d927-129">Follow these steps to set up price lists:</span></span>

        1. <span data-ttu-id="7d927-130">**名前** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d927-130">In the **Name** field, enter a name.</span></span>
        1. <span data-ttu-id="7d927-131">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d927-131">In the **Description** field, enter a description.</span></span>
        1. <span data-ttu-id="7d927-132">**原価タイプ** フィールドで、原価タイプ (*標準原価* または *予定原価*) を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d927-132">In the **Costing type** field, select a costing type (*Standard cost* or *Planned cost*).</span></span>
        1. <span data-ttu-id="7d927-133">**原価タイプ** フィールドで、価格タイプ (*価格*、*購入* または *販売価格*) を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d927-133">In the **Price type** field, select a price type (*Cost*, *Purchase*, or *Sales price*).</span></span>
        1. <span data-ttu-id="7d927-134">原価計算バージョンを追加します。</span><span class="sxs-lookup"><span data-stu-id="7d927-134">Add a costing version.</span></span>
        1. <span data-ttu-id="7d927-135">アクション ペインで、**価格** を選択して価格リストの品目価格を検証します。</span><span class="sxs-lookup"><span data-stu-id="7d927-135">On the Action Pane, select **Price** to validate the item prices on the price list.</span></span>

- <span data-ttu-id="7d927-136">**原価フロー前提条件ポリシー** – 原価フロー前提条件ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d927-136">**Cost flow assumption policy** – Select a cost flow assumption policy.</span></span> <span data-ttu-id="7d927-137">これらのポリシーでは、在庫から原価を削除する方法や、売却済商品の原価として報告する方法が決定されます。</span><span class="sxs-lookup"><span data-stu-id="7d927-137">These policies determine how costs are removed from inventory and reported as the cost of goods sold.</span></span> <span data-ttu-id="7d927-138">次の事前定義済みのオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d927-138">The following predefined options are available:</span></span>

    - <span data-ttu-id="7d927-139">平均</span><span class="sxs-lookup"><span data-stu-id="7d927-139">Average</span></span>
    - <span data-ttu-id="7d927-140">固有 – バッチ</span><span class="sxs-lookup"><span data-stu-id="7d927-140">Specific – Batch</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d927-141">グローバル在庫会計は、永続的な在庫システムです。</span><span class="sxs-lookup"><span data-stu-id="7d927-141">Global Inventory Accounting is a perpetual inventory system.</span></span> <span data-ttu-id="7d927-142">したがって、システムはトランザクション単位ベースで在庫金額を追跡します。</span><span class="sxs-lookup"><span data-stu-id="7d927-142">Therefore, the system tracks the inventory value on a transaction-by-transaction basis.</span></span>

- <span data-ttu-id="7d927-143">**原価要素ポリシー** – 原価要素ポリシーを定義し、このフィールドにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="7d927-143">**Cost element policy** – You can define cost element policies and link them to this field.</span></span> <span data-ttu-id="7d927-144">*原価要素* は、イベントによって消費されるリソースの原価です。</span><span class="sxs-lookup"><span data-stu-id="7d927-144">A *cost element* is the cost of a resource that is consumed by an event.</span></span> <span data-ttu-id="7d927-145">原価要素を使用して、原価を追跡および分類できます。</span><span class="sxs-lookup"><span data-stu-id="7d927-145">You can use cost elements to track and categorize costs.</span></span> <span data-ttu-id="7d927-146">原価要素ポリシーを作成するには、次の場所に情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d927-146">To create cost element policies, enter information in the following places:</span></span>

    - <span data-ttu-id="7d927-147">**名前** フィールド</span><span class="sxs-lookup"><span data-stu-id="7d927-147">**Name** field</span></span>
    - <span data-ttu-id="7d927-148">**説明** フィールド</span><span class="sxs-lookup"><span data-stu-id="7d927-148">**Description** field</span></span>
    - <span data-ttu-id="7d927-149">**原価要素** リスト</span><span class="sxs-lookup"><span data-stu-id="7d927-149">**Cost element** list</span></span>
    - <span data-ttu-id="7d927-150">**ルール** グリッド</span><span class="sxs-lookup"><span data-stu-id="7d927-150">**Rules** grid</span></span>

    <span data-ttu-id="7d927-151">在庫金額をさらに細分しない場合は、1 つの原価要素を含む原価要素リストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d927-151">If you don't want to break down the inventory value further, you must still create a cost element list that has a single cost element.</span></span> <span data-ttu-id="7d927-152">その後、すべての関連する測定タイプ (原価コンポーネント) をその原価要素にマップするには、原価要素ポリシーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d927-152">You must then create a cost element policy to map all the relevant measurement types (cost components) to that cost element.</span></span>
