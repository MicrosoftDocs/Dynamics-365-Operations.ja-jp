---
title: 品揃え管理
description: このトピックでは、Dynamics 365 Commerce での品揃え管理の基本概念について説明し、プロジェクトの実装に関する考慮事項を提供します。
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: 981d1c604a7ed461f207e78c8c7f073aff03be9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980001"
---
# <a name="assortment-management"></a><span data-ttu-id="4388c-103">品揃え管理</span><span class="sxs-lookup"><span data-stu-id="4388c-103">Assortment management</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="4388c-104">概要</span><span class="sxs-lookup"><span data-stu-id="4388c-104">Overview</span></span>

<span data-ttu-id="4388c-105">Dynamics 365 Commerce では、チャンネル間で製品の可用性を管理できる *品揃え* を提供しています。</span><span class="sxs-lookup"><span data-stu-id="4388c-105">Dynamics 365 Commerce provides *assortments* that let you manage product availability across channels.</span></span> <span data-ttu-id="4388c-106">品揃えでは、特定の店舗および特定の期間に利用可能な商品が決まります。</span><span class="sxs-lookup"><span data-stu-id="4388c-106">Assortments determine which products are available at specific stores and during a specific period.</span></span>

<span data-ttu-id="4388c-107">Commerce で、品揃えは 1 つまたは複数のチャネル (または組織階層が使用される場合は一連のチャネル) を 1 つまたは複数の製品 (またはカテゴリ階層を使用する場合は製品のグループ) にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="4388c-107">In Commerce, an assortment is a mapping of one or more channels (or groups of channels, when organization hierarchies are used) to one or more products (or groups of products, when category hierarchies are used).</span></span>

<span data-ttu-id="4388c-108">チャネル全体の製品組み合わせは、チャネルに割り当てられている公開された品揃えによって決まります。</span><span class="sxs-lookup"><span data-stu-id="4388c-108">The overall product mix of a channel is determined by the published assortments that are assigned to the channel.</span></span> <span data-ttu-id="4388c-109">したがって、チャネルごとに複数の有効な品揃えをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-109">Therefore, you can configure multiple active assortments per channel.</span></span>

### <a name="basic-assortment-setup"></a><span data-ttu-id="4388c-110">基本的な品揃えの設定</span><span class="sxs-lookup"><span data-stu-id="4388c-110">Basic assortment setup</span></span>

<span data-ttu-id="4388c-111">次の例では、店舗ごとに固有の品揃えを構成します。</span><span class="sxs-lookup"><span data-stu-id="4388c-111">In the following example, a unique assortment is configured for each store.</span></span> <span data-ttu-id="4388c-112">この場合は、店舗 1 で製品 1 のみが使用可能であり、店舗 2 で製品 2 のみが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="4388c-112">In this case, only product 1 is available at store 1, and only product 2 is available at store 2.</span></span>

![各製品は、1 つの店舗で使用可能です](./media/Managing-assortments-figure1.png)

<span data-ttu-id="4388c-114">店舗 1 で製品 2 を利用するために、品揃え 1 に製品を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-114">To make product 2 available at store 1, you can add the product to assortment 1.</span></span>

![製品 2 が品揃え 1 に追加されます](./media/Managing-assortments-figure2.png)

<span data-ttu-id="4388c-116">または、品揃え 2 に、店舗 1 を追加できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-116">Alternatively, you can add store 1 to assortment 2.</span></span>

![店舗 1 が品揃え 2 に追加されます](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a><span data-ttu-id="4388c-118">組織階層</span><span class="sxs-lookup"><span data-stu-id="4388c-118">Organization hierarchies</span></span>

<span data-ttu-id="4388c-119">複数のチャネルが同じ製品の品揃えを共有する場合、Commerce の品揃えの組織階層を使用して、品揃えを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-119">In situations where multiple channels share the same product assortments, you can configure the assortments by using the Commerce assortment organization hierarchy.</span></span> <span data-ttu-id="4388c-120">この階層のノードが追加されると、そのノードとその子ノード内のすべてのチャネルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4388c-120">When nodes from this hierarchy are added, all channels in that node and its child nodes will be included.</span></span>

![組織階層](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a><span data-ttu-id="4388c-122">製品カテゴリ</span><span class="sxs-lookup"><span data-stu-id="4388c-122">Product categories</span></span>

<span data-ttu-id="4388c-123">同様に、製品側では、製品カテゴリ階層を使用して製品のグループを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-123">Similarly, on the product side, you can include groups of products by using product category hierarchies.</span></span> <span data-ttu-id="4388c-124">1 つ以上のカテゴリ階層ノードを含めることにより、品揃えをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="4388c-124">You can configure assortments by including one or more category hierarchy nodes.</span></span> <span data-ttu-id="4388c-125">この場合、品揃えでは、そのカテゴリ ノードとその子ノードにすべての製品が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4388c-125">In this case, the assortment will include all products in that category node and its child nodes.</span></span>

![製品カテゴリ](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a><span data-ttu-id="4388c-127">除外した製品またはカテゴリ</span><span class="sxs-lookup"><span data-stu-id="4388c-127">Excluded products or categories</span></span>

<span data-ttu-id="4388c-128">品揃えに製品とカテゴリを含めることに加えて、除外オプションを使用して、特定の製品またはカテゴリを品揃えから除外するかどうかを定義できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-128">In addition to including products and categories in assortments, you can use the Exclude option to define specific products or categories that should be excluded from assortments.</span></span> <span data-ttu-id="4388c-129">次の例では、製品 2 を除き、すべての製品を特定のカテゴリに含めるとします。</span><span class="sxs-lookup"><span data-stu-id="4388c-129">In the following example, you want to include all the products in a specific category, except product 2.</span></span> <span data-ttu-id="4388c-130">この場合は、品揃え製品を定義、またはその他のカテゴリ ノードを追加して作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4388c-130">In this case, you don't have to define the assortment product by product or create additional category nodes.</span></span> <span data-ttu-id="4388c-131">代わりに、カテゴリを含めるだけで製品を除外することができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-131">Instead, you can just include the category but exclude the product.</span></span>

> [!NOTE]
> <span data-ttu-id="4388c-132">製品が定義ごと 1 つ以上の品揃えに含まれているか除外されている場合、製品は常に除外されたものとみなされます。</span><span class="sxs-lookup"><span data-stu-id="4388c-132">If a product is both included and excluded in one or more assortments by definition, the product will always be considered excluded.</span></span>

![除外された製品](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a><span data-ttu-id="4388c-134">グローバルおよびリリースされた製品</span><span class="sxs-lookup"><span data-stu-id="4388c-134">Global and released products</span></span>

<span data-ttu-id="4388c-135">品揃えは、グローバル レベルで定義され、複数の法人からのチャネルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-135">Assortments are defined at a global level and can contain channels from multiple legal entities.</span></span> <span data-ttu-id="4388c-136">品揃えに含まれている製品およびカテゴリも、法人間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="4388c-136">The products and categories that are included in assortments are also shared across legal entities.</span></span> <span data-ttu-id="4388c-137">ただし、チャネルで実際に販売、注文、カウント、または受信する前に、製品をリリースする必要があります (たとえば、販売時点管理 \[POS\] にて)。</span><span class="sxs-lookup"><span data-stu-id="4388c-137">However, a product must be released before it can actually be sold, ordered, counted, or received in the channel (for example, in the point of sale \[POS\]).</span></span> <span data-ttu-id="4388c-138">したがって、異なる法人の 2 つの店舗で同じ製品を含む品揃えを共有することはできますが、商品はその法人にリリースされた場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-138">Therefore, although two stores in different legal entities can share an assortment that contains the same products, the products are available only if they have been released to those legal entities.</span></span>

### <a name="dynamic-and-static-assortments"></a><span data-ttu-id="4388c-139">動的および静的品揃え</span><span class="sxs-lookup"><span data-stu-id="4388c-139">Dynamic and static assortments</span></span>

<span data-ttu-id="4388c-140">特定のチャネルと製品で、または組織単位とカテゴリを含めることによって、品揃えを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-140">Assortments can be defined with specific channels and products or by including organization units and categories.</span></span> <span data-ttu-id="4388c-141">これらのグループへの参照を含む品揃えは、動的品揃えと見なされます。</span><span class="sxs-lookup"><span data-stu-id="4388c-141">Assortments including references to these groups are considered dynamic assortments.</span></span> <span data-ttu-id="4388c-142">品揃えが有効な間に定義またはこれらのグループの内容が変更された場合、品揃えの定義も変更されます。</span><span class="sxs-lookup"><span data-stu-id="4388c-142">If the definition or contents of those groups change while the assortment is active, the definition of the assortment will also change.</span></span>

<span data-ttu-id="4388c-143">たとえば、製品のカテゴリを参照できるように品揃えは最初に定義され、公開されます。</span><span class="sxs-lookup"><span data-stu-id="4388c-143">For example, an assortment is originally defined and published so that it references a category of products.</span></span> <span data-ttu-id="4388c-144">後で追加の製品がカテゴリに加えられると、それらの製品は自動的に既存の品揃えの定義に追加されます。</span><span class="sxs-lookup"><span data-stu-id="4388c-144">If additional products are later added to the category, those products are automatically included in the definition of the existing assortment.</span></span> <span data-ttu-id="4388c-145">品揃えに製品を手動で追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4388c-145">You don't have to manually add the products to the assortment.</span></span> <span data-ttu-id="4388c-146">同様に、組織単位が別のノードに追加された場合、組織単位の品揃えはその定義に基づいて自動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="4388c-146">Similarly, if an organization unit is added to a different node, the organization unit's assortment is automatically adjusted based on that definition.</span></span>

### <a name="stopped-products"></a><span data-ttu-id="4388c-147">停止された製品</span><span class="sxs-lookup"><span data-stu-id="4388c-147">Stopped products</span></span>

<span data-ttu-id="4388c-148">**既存の注文** 設定を有効にして、販売プロセスのためにリリースされた製品を「停止」することができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-148">You can "stop" released products for the sales process by turning on a setting in the **Default order** settings.</span></span> <span data-ttu-id="4388c-149">この設定には、製品の有効期間の終了時と、どのチャネルでも販売されない時に最もよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="4388c-149">This setting is most often used when a product is at the end of its life and should not be sold at any channel.</span></span> <span data-ttu-id="4388c-150">品揃えはこの設定を尊重し、品揃えコンフィギュレーションに関係なく、停止された製品を関連付けすることはしません。</span><span class="sxs-lookup"><span data-stu-id="4388c-150">Assortments respect this setting, and stopped products won't be assorted, regardless of the assortment configuration.</span></span>

### <a name="blocked-products"></a><span data-ttu-id="4388c-151">ブロックされた製品</span><span class="sxs-lookup"><span data-stu-id="4388c-151">Blocked products</span></span>

<span data-ttu-id="4388c-152">製品の販売を停止することに加えて、製品の販売を一時的にブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-152">In addition to stopping sales of a product, you can temporarily block sales of a product.</span></span> <span data-ttu-id="4388c-153">リリース済製品の **Commerce** タブでこの設定をコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-153">You can configure this setting on the **Commerce** tab of a released product.</span></span> <span data-ttu-id="4388c-154">ブロックされた製品はまだ類別されていますが、製品を販売できないことを示すメッセージが POS に届きます。</span><span class="sxs-lookup"><span data-stu-id="4388c-154">Blocked products are still assorted, but you will receive a message in the POS that states that the product can't be sold.</span></span>

### <a name="date-effectivity"></a><span data-ttu-id="4388c-155">日付の有効期間</span><span class="sxs-lookup"><span data-stu-id="4388c-155">Date effectivity</span></span>

<span data-ttu-id="4388c-156">品揃えの日付は有効です。</span><span class="sxs-lookup"><span data-stu-id="4388c-156">Assortments are date-effective.</span></span> <span data-ttu-id="4388c-157">したがって、小売業者は、製品がチャネルごとに利用可能かどうかをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-157">Therefore, retailers can configure when products should or should not be available per channel.</span></span> <span data-ttu-id="4388c-158">事前に品揃えを定義して公開し、開始日と終了日を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-158">You can define and publish assortments ahead of time, and specify the start and end dates.</span></span> <span data-ttu-id="4388c-159">その製品は、指定された日付に自動的に利用可能または利用不可になります。</span><span class="sxs-lookup"><span data-stu-id="4388c-159">The products will automatically become available or unavailable on the specified dates.</span></span>

### <a name="process-assortments-batch-job"></a><span data-ttu-id="4388c-160">品揃えのバッチ ジョブを処理</span><span class="sxs-lookup"><span data-stu-id="4388c-160">Process assortments batch job</span></span>

<span data-ttu-id="4388c-161">Commerce で定義されている品揃えは、有効にする前に処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4388c-161">Assortments that are defined in Commerce must be processed before they take effect.</span></span> <span data-ttu-id="4388c-162">この処理が実行されるのは、以下の理由によります。</span><span class="sxs-lookup"><span data-stu-id="4388c-162">This processing is done for the following reasons:</span></span>

- <span data-ttu-id="4388c-163">品揃えの定義は、チャネルがより簡単にそれらを消費できるように、非正規化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4388c-163">Assortment definitions must be de-normalized so that channels can more easily consume them.</span></span> <span data-ttu-id="4388c-164">チャネルの製品の組み合わせは、さまざまな日付範囲にまたがる複数の品揃えによって定義できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-164">A product mix for a channel can be defined through multiple assortments that span various date ranges.</span></span> <span data-ttu-id="4388c-165">この情報の一部が事前にサーバーで計算されると、チャネルでのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="4388c-165">When some of this information is calculated ahead of time on the server, performance at the channel is improved.</span></span>
- <span data-ttu-id="4388c-166">品揃えの製品およびチャネルは、品揃え外部で変更できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-166">The products and channels in the assortment can change outside the assortment itself.</span></span> <span data-ttu-id="4388c-167">カテゴリまたは組織単位への参照を含む動的品揃えは、現在の割り当てに基づいてレコードを含めるか除外するかできるように、定期的に処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4388c-167">Dynamic assortments that contain references to categories or organization units must be processed periodically so that they include or exclude records, based on their current assignment.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="4388c-168">実装の考慮事項</span><span class="sxs-lookup"><span data-stu-id="4388c-168">Implementation considerations</span></span>

<span data-ttu-id="4388c-169">Commerce 実装のための品揃えを計画および管理する場合、次の実装要件を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="4388c-169">Consider the following implementation requirements as you plan and manage assortments for your Commerce implementation:</span></span>

- <span data-ttu-id="4388c-170">**データ レプリケーションとデータベース サイズ** – 品揃えは、ビジネス ニーズを使用して製品の可用性を管理するのに役立ちますが、チャネルとオフライン データベースのサイズを管理するためにも重要なツールです。</span><span class="sxs-lookup"><span data-stu-id="4388c-170">**Data replication and database size** – Although assortments help serve the business need to manage product availability, they are also an important tool for managing the size of channel and offline databases.</span></span> <span data-ttu-id="4388c-171">適切に管理された品揃えは、チャネルとオフライン データベースに処理および複製しなければならないデータの量を減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4388c-171">Well-managed assortments help reduce the amount of data that must be processed and replicated to channel and offline databases.</span></span> <span data-ttu-id="4388c-172">これらは、保存する必要があるレコードの数を減らすためにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4388c-172">They also help reduce the number of records that must be persisted.</span></span> <span data-ttu-id="4388c-173">これらのデータベース内の少数のレコードによって、製品のトランザクション、検索、および参照する品目を追加する場合に、パフォーマンスを向上させます。</span><span class="sxs-lookup"><span data-stu-id="4388c-173">Fewer records in these databases will increase performance when you add items to a transaction, search, and browse for products.</span></span>
- <span data-ttu-id="4388c-174">**有効日/期限が切れる品揃え** - チャネルおよびオフライン データベースの製品数を管理する最も効果的なツールの 1 つは、品揃えの日付の有効期間です。</span><span class="sxs-lookup"><span data-stu-id="4388c-174">**Date-effective/expiring assortments** – One of the most effective tools for managing the number of products in channel and offline databases is the date effectivity of assortments.</span></span> <span data-ttu-id="4388c-175">季節製品、または耐用年数が過ぎた製品の品揃えを自由回答式 (無期限) に残しておく場合、これらのデータベースは無制限に拡大します。</span><span class="sxs-lookup"><span data-stu-id="4388c-175">If you leave open-ended (non-expiring) assortments for seasonal products or products that are at the end of their life, these databases will grow indefinitely.</span></span> <span data-ttu-id="4388c-176">さまざまなアプローチを使用して、この状況を管理できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-176">You can use various approaches to help manage this situation.</span></span> <span data-ttu-id="4388c-177">たとえば、季節製品と常に利用可能な製品に対して、個別の品揃えを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-177">For example, you can maintain separate assortments for seasonal products and products that are always available.</span></span>
- <span data-ttu-id="4388c-178">**品揃えの範囲外の販売と返品** – この機能は、店舗のコア製品の組み合わせに属する製品に対して使用可能な製品の数を制限することで、小売業者が品揃えを効率的に管理できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-178">**Sales and returns outside assortments** – This capability helps retailers effectively manage their assortments by letting them limit the number of available products to products that belong to the core product mix for the store.</span></span> <span data-ttu-id="4388c-179">この機能は、製品が誤って品揃えから除外された場合や製品が品揃えの有効期限外に返品された場合にも、小売業者が対応できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4388c-179">This capability also helps retailers handle situations where a product was mistakenly omitted from an assortment, or where a product was returned outside the effective dates for the assortment.</span></span>

<span data-ttu-id="4388c-180">製品データがチャネル データベースに存在しない場合にも、製品の販売、返品、または顧客注文にすることができるように、POS は必要な情報を取得し、リアルタイムで本社に電話をかけることができます。</span><span class="sxs-lookup"><span data-stu-id="4388c-180">If product data doesn't exist in the channel database, the POS makes real-time calls to headquarters to retrieve the required information, so that the product can be sold, returned, or put on a customer order.</span></span> <span data-ttu-id="4388c-181">この方法で取得された製品情報は、そのトランザクションの範囲内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="4388c-181">Product information that is retrieved in this manner is available only during the scope of that transaction.</span></span> <span data-ttu-id="4388c-182">製品は、品揃え定義に追加されません。</span><span class="sxs-lookup"><span data-stu-id="4388c-182">The product isn't added to the assortment definition.</span></span> <span data-ttu-id="4388c-183">したがって、必要に応じて後続のリアルタイム コールが行われます。</span><span class="sxs-lookup"><span data-stu-id="4388c-183">Therefore, subsequent real-time calls will be made as required.</span></span>
