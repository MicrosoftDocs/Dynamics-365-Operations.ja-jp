---
title: 製品分析コード
description: 4 つの製品分析コードがあります - 色、構成、サイズ、およびスタイルです。 分析コード グループで製品分析コードを組み合わせて、製品マスターに分析コード グループを割り当てます。 製品分析コードの組み合わせは、製品バリアントの定義方法を決定します。
author: cvocph
manager: tfehr
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5e9b10fa18ada9534ce5e279d4f1f09973a802b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208435"
---
# <a name="product-dimensions"></a><span data-ttu-id="bc124-105">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="bc124-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc124-106">4 つの製品分析コードがあります - 色、構成、サイズ、およびスタイルです。</span><span class="sxs-lookup"><span data-stu-id="bc124-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="bc124-107">分析コード グループで製品分析コードを組み合わせて、製品マスターに分析コード グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="bc124-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="bc124-108">製品分析コードの組み合わせは、製品バリアントの定義方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="bc124-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="bc124-109">製品分析コードは、製品バリアントを識別するために役立つ特性です。</span><span class="sxs-lookup"><span data-stu-id="bc124-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="bc124-110">製品バリアントを定義するために製品分析コードの組み合わせを使用できます。</span><span class="sxs-lookup"><span data-stu-id="bc124-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="bc124-111">製品バリアントを作成するには、製品マスターに対して少なくとも 1 つ製品分析コードを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc124-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>

## <a name="product-variants"></a><span data-ttu-id="bc124-112">製品バリアント</span><span class="sxs-lookup"><span data-stu-id="bc124-112">Product variants</span></span>

<span data-ttu-id="bc124-113">製品バリアントは品目とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="bc124-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="bc124-114">品目は、有形製品のことで、サービスとは異なるものです。</span><span class="sxs-lookup"><span data-stu-id="bc124-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="bc124-115">サービス タイプの製品マスターを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="bc124-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="bc124-116">[Service] タイプを使用して、サービスを含む製品バリアントを指定できます。</span><span class="sxs-lookup"><span data-stu-id="bc124-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="bc124-117">たとえば、上級顧問や若手のコンサルタントによって実行される、コンサルタント作業および作業の製品バリアントに、製品マスターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="bc124-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="bc124-118">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="bc124-118">Product dimensions</span></span>
<span data-ttu-id="bc124-119">次の 4 つの製品分析コードがあります: 色、構成、サイズ、およびスタイルです。</span><span class="sxs-lookup"><span data-stu-id="bc124-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="bc124-120">製品バリアントは、製品分析コードの値に基づいて生成することができます。</span><span class="sxs-lookup"><span data-stu-id="bc124-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="bc124-121">サイズ、色およびスタイルなどの製品分析コード値は、**サイズ**、**色** および**スタイル**ページで作成できます。これらのページは、次の場所からアクセスできます: **製品情報管理** &gt; **設定** &gt; **分析コードおよびバリアント グループ** &gt; **サイズ / 色 / スタイル**。</span><span class="sxs-lookup"><span data-stu-id="bc124-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="bc124-122">[コンフィギュレーション分析コード] の製品分析コードの値は、通常、[製品コンフィギュレーター] または [分析コード ベースのコンフィギュレーター] を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="bc124-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="bc124-123">製品分析コードは**製品分析コード** ページで作成および管理することもできます。以下の場所からアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="bc124-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="bc124-124">**製品情報管理** &gt; **製品** &gt; **製品マスター**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc124-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="bc124-125">**アクション ペイン**で、**製品分析コード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc124-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="bc124-126">**製品情報管理** &gt; **製品** &gt; **すべての製品および製品マスター**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc124-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="bc124-127">製品マスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc124-127">Select a product master.</span></span> <span data-ttu-id="bc124-128">**アクション ペイン**で、**製品分析コード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc124-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="bc124-129">**製品情報管理** &gt; **リリースされた製品**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc124-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="bc124-130">製品マスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc124-130">Select a product master.</span></span> <span data-ttu-id="bc124-131">**アクション ペイン**で、**製品**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc124-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="bc124-132">**製品マスター** グループで、**製品分析コード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc124-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="bc124-133">1 つの品目に対して作成できるバリアントの数は、可能な製品分析コードの組み合わせの数により制限されます。</span><span class="sxs-lookup"><span data-stu-id="bc124-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="bc124-134">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="bc124-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc124-135">たとえば、ある注文明細行上で製品を使用する場合、製品分析コードを選択して、使用する製品バリアントを特定します。</span><span class="sxs-lookup"><span data-stu-id="bc124-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="bc124-136">例</span><span class="sxs-lookup"><span data-stu-id="bc124-136">Example</span></span>
<span data-ttu-id="bc124-137">ある会社がデニム ジーンズを販売しています。</span><span class="sxs-lookup"><span data-stu-id="bc124-137">A company sells denim jeans.</span></span> <span data-ttu-id="bc124-138">品目 "ジーンズ" には、色分析コードとサイズ分析コードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc124-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="bc124-139">販売されるジーンズには、3 種類の色と 6 種類のサイズがあります。</span><span class="sxs-lookup"><span data-stu-id="bc124-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="bc124-140">色: 青、黒、茶。サイズ: XS、S、M、L、XL、XXL。すべてのサイズで 3 色すべてが用意されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="bc124-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="bc124-141">すべての組み合わせが使用可能な場合、18 タイプのジーンズを作成します。</span><span class="sxs-lookup"><span data-stu-id="bc124-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="bc124-142">この例では、次の 9 種類の製品バリアントの組み合わせのみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="bc124-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="bc124-143">色</span><span class="sxs-lookup"><span data-stu-id="bc124-143">Color</span></span> | <span data-ttu-id="bc124-144">サイズ</span><span class="sxs-lookup"><span data-stu-id="bc124-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="bc124-145">青</span><span class="sxs-lookup"><span data-stu-id="bc124-145">Blue</span></span>  | <span data-ttu-id="bc124-146">XS</span><span class="sxs-lookup"><span data-stu-id="bc124-146">XS</span></span>   |
| <span data-ttu-id="bc124-147">青</span><span class="sxs-lookup"><span data-stu-id="bc124-147">Blue</span></span>  | <span data-ttu-id="bc124-148">S</span><span class="sxs-lookup"><span data-stu-id="bc124-148">S</span></span>    |
| <span data-ttu-id="bc124-149">青</span><span class="sxs-lookup"><span data-stu-id="bc124-149">Blue</span></span>  | <span data-ttu-id="bc124-150">M</span><span class="sxs-lookup"><span data-stu-id="bc124-150">M</span></span>    |
| <span data-ttu-id="bc124-151">黒</span><span class="sxs-lookup"><span data-stu-id="bc124-151">Black</span></span> | <span data-ttu-id="bc124-152">M</span><span class="sxs-lookup"><span data-stu-id="bc124-152">M</span></span>    |
| <span data-ttu-id="bc124-153">黒</span><span class="sxs-lookup"><span data-stu-id="bc124-153">Black</span></span> | <span data-ttu-id="bc124-154">L</span><span class="sxs-lookup"><span data-stu-id="bc124-154">L</span></span>    |
| <span data-ttu-id="bc124-155">黒</span><span class="sxs-lookup"><span data-stu-id="bc124-155">Black</span></span> | <span data-ttu-id="bc124-156">XL</span><span class="sxs-lookup"><span data-stu-id="bc124-156">XL</span></span>   |
| <span data-ttu-id="bc124-157">茶</span><span class="sxs-lookup"><span data-stu-id="bc124-157">Brown</span></span> | <span data-ttu-id="bc124-158">L</span><span class="sxs-lookup"><span data-stu-id="bc124-158">L</span></span>    |
| <span data-ttu-id="bc124-159">茶</span><span class="sxs-lookup"><span data-stu-id="bc124-159">Brown</span></span> | <span data-ttu-id="bc124-160">XL</span><span class="sxs-lookup"><span data-stu-id="bc124-160">XL</span></span>   |
| <span data-ttu-id="bc124-161">茶</span><span class="sxs-lookup"><span data-stu-id="bc124-161">Brown</span></span> | <span data-ttu-id="bc124-162">XXL</span><span class="sxs-lookup"><span data-stu-id="bc124-162">XXL</span></span>  |





