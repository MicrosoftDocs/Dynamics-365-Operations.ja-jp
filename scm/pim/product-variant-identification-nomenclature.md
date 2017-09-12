---
title: "製品バリアント番号と名前の分類"
description: "このトピックでは、固定形式 [製品マスター番号 - コンフィギュレーション - サイズ - 色 - スタイル] を置換するために製品番号の分類を設定する方法を説明します。 新しい分類には、製品マスター番号、有効な製品分析コード、および選択したテキストの区切り記号を含む対象の形式があります。 製品名の分類を作成することもできます。 最後に、制約ベースの製品コンフィギュレーターによって作成されるコンフィギュレーションを識別するための分類を構築できます。 これらの分類は、選択した属性を含めることができます。"
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="10534-107">製品バリアント番号と名前の分類</span><span class="sxs-lookup"><span data-stu-id="10534-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="10534-108">このトピックでは、固定形式 [製品マスター番号 - コンフィギュレーション - サイズ - 色 - スタイル] を置換するために製品番号の分類を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="10534-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="10534-109">新しい分類には、製品マスター番号、有効な製品分析コード、および選択したテキストの区切り記号を含む対象の形式があります。</span><span class="sxs-lookup"><span data-stu-id="10534-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="10534-110">製品名の分類を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="10534-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="10534-111">最後に、制約ベースの製品コンフィギュレーターによって作成されるコンフィギュレーションを識別するための分類を構築できます。</span><span class="sxs-lookup"><span data-stu-id="10534-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="10534-112">これらの分類は、選択した属性を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="10534-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="10534-113">製品バリアント番号および製品バリアント名の新しい分類では、製品バリアントの識別子に区分を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="10534-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="10534-114">これらの区分には、製品マスター番号と名前、製品分析コード ID と名前、番号順序、テキストの定数、および属性を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="10534-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="10534-115">この機能により、販売注文または発注書を作成するための特定の製品バリアントをすばやく検索できます。</span><span class="sxs-lookup"><span data-stu-id="10534-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="10534-116">[**製品の分類**] ページを使用して、製品バリアント番号と製品バリアント名の両方に対する分類を作成できます。</span><span class="sxs-lookup"><span data-stu-id="10534-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="10534-117">このページを開くには、[**製品情報管理**] &gt; [**設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10534-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="10534-118">事前定義された製品バリアントの分類</span><span class="sxs-lookup"><span data-stu-id="10534-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="10534-119">製品バリアントが、次の 3 つのコンフィギュレーション テクノロジのいずれか 1 つに従って製品マスターに対して生成されます:</span><span class="sxs-lookup"><span data-stu-id="10534-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="10534-120">事前に定義されたバリアント</span><span class="sxs-lookup"><span data-stu-id="10534-120">Predefined variants</span></span>
-   <span data-ttu-id="10534-121">制約ベース</span><span class="sxs-lookup"><span data-stu-id="10534-121">Constraint-based</span></span>
-   <span data-ttu-id="10534-122">分析コード ベース</span><span class="sxs-lookup"><span data-stu-id="10534-122">Dimension-based</span></span>

<span data-ttu-id="10534-123">各製品バリアントに番号と名前があり、製品バリアント ID の分類により、各製品のバリアント番号または名前に含まれる区分を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="10534-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="10534-124">[**製品の分類**] ページで次の区分を選択できます。</span><span class="sxs-lookup"><span data-stu-id="10534-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="10534-125">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="10534-125">Product master number</span></span>
-   <span data-ttu-id="10534-126">製品マスター名</span><span class="sxs-lookup"><span data-stu-id="10534-126">Product master name</span></span>
-   <span data-ttu-id="10534-127">番号順序値</span><span class="sxs-lookup"><span data-stu-id="10534-127">Number sequence value</span></span>
-   <span data-ttu-id="10534-128">テキスト定数</span><span class="sxs-lookup"><span data-stu-id="10534-128">Text constant</span></span>
-   <span data-ttu-id="10534-129">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="10534-129">Product dimensions</span></span>
    -   <span data-ttu-id="10534-130">コンフィギュレーション ID または名前</span><span class="sxs-lookup"><span data-stu-id="10534-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="10534-131">色 ID または名前</span><span class="sxs-lookup"><span data-stu-id="10534-131">Color ID or name</span></span>
    -   <span data-ttu-id="10534-132">サイズ ID または名前</span><span class="sxs-lookup"><span data-stu-id="10534-132">Size ID or name</span></span>
    -   <span data-ttu-id="10534-133">スタイル ID または名前</span><span class="sxs-lookup"><span data-stu-id="10534-133">Style ID or name</span></span>

<span data-ttu-id="10534-134">製品バリアント ID 番号の分類を定義した後に、製品分析コード グループに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="10534-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="10534-135">その後、この製品分析コード グループを参照するすべての製品の製品マスターに、分類に基づいて製品バリアント番号が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="10534-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="10534-136">ただし、製品バリアント名の分類を製品分析コード グループに関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="10534-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="10534-137">製品バリアント ID の分類を製品マスターに直接割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="10534-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="10534-138">この場合は、製品マスターに属している製品バリアントに、分類に従って製品バリアント番号と名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="10534-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="10534-139">例</span><span class="sxs-lookup"><span data-stu-id="10534-139">Example</span></span>

<span data-ttu-id="10534-140">T シャツ (TS1234) は、3 つのサイズ (S、M、L)、4 つの色 (赤、緑、青、黄色) および 2 つのスタイル (ポロ、V ネック) で作成されます。</span><span class="sxs-lookup"><span data-stu-id="10534-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="10534-141">したがって、24 のバリエーションが可能です (= 3 × 4 × 2)。</span><span class="sxs-lookup"><span data-stu-id="10534-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="10534-142">次の区分を持つ製品バリアント番号の分類を作成します。</span><span class="sxs-lookup"><span data-stu-id="10534-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="10534-143">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="10534-143">Product master number</span></span>
2.  <span data-ttu-id="10534-144">テキスト定数: "-"</span><span class="sxs-lookup"><span data-stu-id="10534-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="10534-145">色</span><span class="sxs-lookup"><span data-stu-id="10534-145">Color</span></span>
4.  <span data-ttu-id="10534-146">テキスト定数: "-"</span><span class="sxs-lookup"><span data-stu-id="10534-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="10534-147">サイズ</span><span class="sxs-lookup"><span data-stu-id="10534-147">Size</span></span>
6.  <span data-ttu-id="10534-148">テキスト定数: "-"</span><span class="sxs-lookup"><span data-stu-id="10534-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="10534-149">スタイル</span><span class="sxs-lookup"><span data-stu-id="10534-149">Style</span></span>

<span data-ttu-id="10534-150">この場合、赤、S、ポロの製品バリアント番号は TS1234-Red-Small-Polo になります。</span><span class="sxs-lookup"><span data-stu-id="10534-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="10534-151">制約ベースのコンフィギュレーションの分類</span><span class="sxs-lookup"><span data-stu-id="10534-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="10534-152">制約ベースのコンフィギュレーションの場合、製品分析コードのコンフィギュレーションに対して専門の分類を作成できます。</span><span class="sxs-lookup"><span data-stu-id="10534-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="10534-153">[**製品の分類**] ページで次の区分を選択できます。</span><span class="sxs-lookup"><span data-stu-id="10534-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="10534-154">番号順序値</span><span class="sxs-lookup"><span data-stu-id="10534-154">Number sequence value</span></span>
-   <span data-ttu-id="10534-155">テキスト定数</span><span class="sxs-lookup"><span data-stu-id="10534-155">Text constant</span></span>
-   <span data-ttu-id="10534-156">属性値</span><span class="sxs-lookup"><span data-stu-id="10534-156">Attribute value</span></span>

<span data-ttu-id="10534-157">製品コンフィギュレーション モデルの各コンポーネントで、独自のコンフィギュレーションの分類を使用できます。</span><span class="sxs-lookup"><span data-stu-id="10534-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="10534-158">コンポーネントに属する属性のみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="10534-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="10534-159">サブコンポーネントまたはユーザー要件の属性は使用できません。</span><span class="sxs-lookup"><span data-stu-id="10534-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="10534-160">例</span><span class="sxs-lookup"><span data-stu-id="10534-160">Example</span></span>

<span data-ttu-id="10534-161">製品コンフィギュレーション モデルには 2 つの属性があるルート コンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="10534-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="10534-162">材料 (プラスチック、木材、スチール)</span><span class="sxs-lookup"><span data-stu-id="10534-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="10534-163">期間 (10...100)</span><span class="sxs-lookup"><span data-stu-id="10534-163">Length (10...100)</span></span>

<span data-ttu-id="10534-164">次の区分を持つコンフィギュレーションの分類を作成します。</span><span class="sxs-lookup"><span data-stu-id="10534-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="10534-165">属性値: 材料</span><span class="sxs-lookup"><span data-stu-id="10534-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="10534-166">テキスト定数: "AAA"</span><span class="sxs-lookup"><span data-stu-id="10534-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="10534-167">属性値: 長さ</span><span class="sxs-lookup"><span data-stu-id="10534-167">Attribute value: Length</span></span>

<span data-ttu-id="10534-168">この場合、78 の長さの木材が材料のコンフィギュレーション ID は WoodAAA78 になります。</span><span class="sxs-lookup"><span data-stu-id="10534-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="10534-169">分析コードベースのコンフィギュレーションの分類</span><span class="sxs-lookup"><span data-stu-id="10534-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="10534-170">分析コードベースのコンフィギュレーションの場合、製品分析コードのコンフィギュレーションに対して専門の分類を作成できます。</span><span class="sxs-lookup"><span data-stu-id="10534-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="10534-171">[**製品の分類**] ページで次の区分を選択できます。</span><span class="sxs-lookup"><span data-stu-id="10534-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="10534-172">番号順序値</span><span class="sxs-lookup"><span data-stu-id="10534-172">Number sequence value</span></span>
-   <span data-ttu-id="10534-173">テキスト定数</span><span class="sxs-lookup"><span data-stu-id="10534-173">Text constant</span></span>
-   <span data-ttu-id="10534-174">コンフィギュレーション グループ品目</span><span class="sxs-lookup"><span data-stu-id="10534-174">Configuration group item</span></span>

<span data-ttu-id="10534-175">コンフィギュレーションの分類は、部品表 (BOM) に対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="10534-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="10534-176">例</span><span class="sxs-lookup"><span data-stu-id="10534-176">Example</span></span>

<span data-ttu-id="10534-177">BOM には、2 つのコンフィギュレーション グループに分割される 4 つの BOM 明細行があります。</span><span class="sxs-lookup"><span data-stu-id="10534-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="10534-178">BOM 明細行: M0007、 標準キャビネット</span><span class="sxs-lookup"><span data-stu-id="10534-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="10534-179">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="10534-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="10534-180">BOM 明細行: M0008、ハイ エンド キャビネット</span><span class="sxs-lookup"><span data-stu-id="10534-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="10534-181">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="10534-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="10534-182">BOM 明細行: M0021、フロント グリルの布</span><span class="sxs-lookup"><span data-stu-id="10534-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="10534-183">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="10534-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="10534-184">BOM 明細行: M0022、フロント グリルの金属</span><span class="sxs-lookup"><span data-stu-id="10534-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="10534-185">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="10534-185">Configuration group: Front grill</span></span>

<span data-ttu-id="10534-186">次の区分を持つコンフィギュレーションの分類を作成します。</span><span class="sxs-lookup"><span data-stu-id="10534-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="10534-187">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="10534-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="10534-188">テキスト定数: "&"</span><span class="sxs-lookup"><span data-stu-id="10534-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="10534-189">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="10534-189">Configuration group: Front grill</span></span>

<span data-ttu-id="10534-190">この場合、布のフロント グリルが付いた標準キャビネットのコンフィギュレーション ID は M0007&M0021 になります。</span><span class="sxs-lookup"><span data-stu-id="10534-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="10534-191">製品バリアントおよびコンフィギュレーションの組み合わせの分類</span><span class="sxs-lookup"><span data-stu-id="10534-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="10534-192">制約ベースのコンフィギュレーション テクノロジまたは分析コードベースのコンフィギュレーション テクノロジを使用して、製品マスターの製品バリアントを設定する場合、製品バリアントの製品バリアント番号にコンフィギュレーション分析コードの分類を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="10534-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="10534-193">バリアントをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="10534-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="10534-194">[**製品の分類**] ページで、コンフィギュレーション分析コードを含む製品バリアント番号の分類を定義します。</span><span class="sxs-lookup"><span data-stu-id="10534-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="10534-195">コンフィギュレーション分析コードを持つ製品分析コード グループにこの分類を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="10534-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="10534-196">コンポーネントのためのコンフィギュレーションの分類を定義するか、または製品のバリアントをコンフィギュレーションするために使用される BOM を定義します。</span><span class="sxs-lookup"><span data-stu-id="10534-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="10534-197">製品バリアント名の分類を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="10534-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="10534-198">コンフィギュレーション ID または名前を含めるには、製品バリアント名をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="10534-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="10534-199">制約ベースの製品コンフィギュレーションの例</span><span class="sxs-lookup"><span data-stu-id="10534-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="10534-200">この例では、次の区分から構成される製品バリアント番号の分類を使用します。</span><span class="sxs-lookup"><span data-stu-id="10534-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="10534-201">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="10534-201">Product master number</span></span>
2.  <span data-ttu-id="10534-202">テキスト定数 "\_"</span><span class="sxs-lookup"><span data-stu-id="10534-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="10534-203">構成</span><span class="sxs-lookup"><span data-stu-id="10534-203">Configuration</span></span>

<span data-ttu-id="10534-204">コンフィギュレーションの分類は、次の区分を使用して構成されます。</span><span class="sxs-lookup"><span data-stu-id="10534-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="10534-205">属性値: 材料</span><span class="sxs-lookup"><span data-stu-id="10534-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="10534-206">テキスト定数: "AAA"</span><span class="sxs-lookup"><span data-stu-id="10534-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="10534-207">属性値: 長さ</span><span class="sxs-lookup"><span data-stu-id="10534-207">Attribute value: Length</span></span>

<span data-ttu-id="10534-208">セグメントに次の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="10534-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="10534-209">製品マスター番号 = **M0099**</span><span class="sxs-lookup"><span data-stu-id="10534-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="10534-210">材料 = **プラスチック**</span><span class="sxs-lookup"><span data-stu-id="10534-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="10534-211">長さ = **12**</span><span class="sxs-lookup"><span data-stu-id="10534-211">Length = **12**</span></span>

<span data-ttu-id="10534-212">この場合、製品バリアント番号は M0099\_PlasticAAA12 になります。</span><span class="sxs-lookup"><span data-stu-id="10534-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="10534-213">分析コードベースのコンフィギュレーションの例</span><span class="sxs-lookup"><span data-stu-id="10534-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="10534-214">この例では、次の区分から構成される製品バリアント番号の分類を使用します。</span><span class="sxs-lookup"><span data-stu-id="10534-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="10534-215">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="10534-215">Product master number</span></span>
2.  <span data-ttu-id="10534-216">テキスト定数 "//"</span><span class="sxs-lookup"><span data-stu-id="10534-216">Text constant "//"</span></span>
3.  <span data-ttu-id="10534-217">構成</span><span class="sxs-lookup"><span data-stu-id="10534-217">Configuration</span></span>

<span data-ttu-id="10534-218">コンフィギュレーションの分類は、次の区分を使用して構成されます。</span><span class="sxs-lookup"><span data-stu-id="10534-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="10534-219">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="10534-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="10534-220">テキスト定数: "&"</span><span class="sxs-lookup"><span data-stu-id="10534-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="10534-221">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="10534-221">Configuration group: Front grill</span></span>

<span data-ttu-id="10534-222">セグメントに次の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="10534-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="10534-223">製品マスター番号 = **D0123**</span><span class="sxs-lookup"><span data-stu-id="10534-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="10534-224">キャビネット= **M0008**</span><span class="sxs-lookup"><span data-stu-id="10534-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="10534-225">フロント グリル = **M0022**</span><span class="sxs-lookup"><span data-stu-id="10534-225">Front grill = **M0022**</span></span>

<span data-ttu-id="10534-226">この場合、製品のリアント番号は D0123//M0008&M0022 になります。</span><span class="sxs-lookup"><span data-stu-id="10534-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="10534-227">競合数</span><span class="sxs-lookup"><span data-stu-id="10534-227">Numbering conflicts</span></span>
<span data-ttu-id="10534-228">場合によっては、設定する製品バリアント番号の分類によって一意の製品バリアント番号が作成されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="10534-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="10534-229">たとえば、事前に定義されたバリアント コンフィギュレーション テクノロジを使用する製品マスターの分類に、有効な製品分析コードが含まれていないと、製品バリアント番号は一意になりません。</span><span class="sxs-lookup"><span data-stu-id="10534-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="10534-230">競合を処理する方法は、コンフィギュレーション テクノロジによって異なります。</span><span class="sxs-lookup"><span data-stu-id="10534-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="10534-231">事前に定義されたバリアント</span><span class="sxs-lookup"><span data-stu-id="10534-231">Predefined variants</span></span>

<span data-ttu-id="10534-232">製品バリアントの手動の作成または自動的な生成を試み、複数の製品バリアントが同じ製品バリアント番号になる場合は、エラーになります。</span><span class="sxs-lookup"><span data-stu-id="10534-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="10534-233">このシナリオを回避するには、製品の分析コード グループのすべての有効な製品分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="10534-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="10534-234">または、製品バリアント番号が一意であることを保証するために役立つ番号順序を含めます。</span><span class="sxs-lookup"><span data-stu-id="10534-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="10534-235">制約ベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="10534-235">Constraint-based configurations</span></span>

<span data-ttu-id="10534-236">分類によっては、システムはコンフィギュレーションに対して一意ではない製品バリアント番号を割り当てようとする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10534-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="10534-237">この場合、システムは製品バリアント番号としてコンフィギュレーション分析コードの番号順序を代わりに使用します。こうした場合は、警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="10534-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="10534-238">このシナリオを避けるには、一意の製品バリアント番号を保証するために役立つ十分な属性を分類に含めます。</span><span class="sxs-lookup"><span data-stu-id="10534-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="10534-239">また、コンポーネントに対して [**再利用**] オプションがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="10534-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="10534-240">分析コードベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="10534-240">Dimension-based configurations</span></span>

<span data-ttu-id="10534-241">コンフィギュレーション プロセスの 1 つのステップ中に、分類に基づいてコンフィギュレーション値が提案されます。</span><span class="sxs-lookup"><span data-stu-id="10534-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="10534-242">このステップでは、コンフィギュレーションの値を手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="10534-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="10534-243">コンフィギュレーションを保存すると、コンフィギュレーション値が一意かどうかが確認されます。</span><span class="sxs-lookup"><span data-stu-id="10534-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="10534-244">入力した値が一意でない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="10534-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="10534-245">コンフィギュレーションを保存するためには、一意のコンフィギュレーション値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10534-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="10534-246">参照</span><span class="sxs-lookup"><span data-stu-id="10534-246">See also</span></span>
--------

[<span data-ttu-id="10534-247">事前定義済製品バリアントの製品番号に関する用語の作成</span><span class="sxs-lookup"><span data-stu-id="10534-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="10534-248">コンフィギュレーション済製品バリアントにおける製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="10534-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


