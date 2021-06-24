---
title: 製品バリアント番号と名前の分類
description: このトピックでは、固定形式 [製品マスター番号 - コンフィギュレーション - サイズ - 色 - スタイル] を置換するために製品番号の分類を設定する方法を説明します。
author: roxanadiaconu
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edab3420cbd39539358c03fe4d6b3646433f8ec5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190163"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="930ae-103">製品バリアント番号と名前の分類</span><span class="sxs-lookup"><span data-stu-id="930ae-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="930ae-104">このトピックでは、固定形式 [製品マスター番号 - コンフィギュレーション - サイズ - 色 - スタイル] を置換するために製品番号の分類を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="930ae-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="930ae-105">新しい分類には、製品マスター番号、有効な製品分析コード、および選択したテキストの区切り記号を含む対象の形式があります。</span><span class="sxs-lookup"><span data-stu-id="930ae-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="930ae-106">製品名の分類を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="930ae-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="930ae-107">最後に、制約ベースの製品コンフィギュレーターによって作成されるコンフィギュレーションを識別するための分類を構築できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="930ae-108">これらの分類は、選択した属性を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="930ae-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="930ae-109">製品バリアント番号および製品バリアント名の新しい分類では、製品バリアントの識別子に区分を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="930ae-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="930ae-110">これらの区分には、製品マスター番号と名前、製品分析コード ID と名前、番号順序、テキストの定数、および属性を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="930ae-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="930ae-111">この機能により、販売注文または発注書を作成するための特定の製品バリアントをすばやく検索できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="930ae-112">**製品の分類** ページを使用して、製品バリアント番号と製品バリアント名の両方に対する分類を作成できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="930ae-113">このページを開くには、**製品情報管理** &gt; **設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="930ae-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="930ae-114">事前定義された製品バリアントの分類</span><span class="sxs-lookup"><span data-stu-id="930ae-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="930ae-115">製品バリアントが、次の 3 つのコンフィギュレーション テクノロジのいずれか 1 つに従って製品マスターに対して生成されます:</span><span class="sxs-lookup"><span data-stu-id="930ae-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="930ae-116">事前に定義されたバリアント</span><span class="sxs-lookup"><span data-stu-id="930ae-116">Predefined variants</span></span>
-   <span data-ttu-id="930ae-117">制約ベース</span><span class="sxs-lookup"><span data-stu-id="930ae-117">Constraint-based</span></span>
-   <span data-ttu-id="930ae-118">分析コード ベース</span><span class="sxs-lookup"><span data-stu-id="930ae-118">Dimension-based</span></span>

<span data-ttu-id="930ae-119">各製品バリアントに番号と名前があり、製品バリアント ID の分類により、各製品のバリアント番号または名前に含まれる区分を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="930ae-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="930ae-120">**製品の分類** ページで次の区分を選択できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="930ae-121">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="930ae-121">Product master number</span></span>
-   <span data-ttu-id="930ae-122">製品マスター名</span><span class="sxs-lookup"><span data-stu-id="930ae-122">Product master name</span></span>
-   <span data-ttu-id="930ae-123">番号順序値</span><span class="sxs-lookup"><span data-stu-id="930ae-123">Number sequence value</span></span>
-   <span data-ttu-id="930ae-124">テキスト定数</span><span class="sxs-lookup"><span data-stu-id="930ae-124">Text constant</span></span>
-   <span data-ttu-id="930ae-125">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="930ae-125">Product dimensions</span></span>
    -   <span data-ttu-id="930ae-126">コンフィギュレーション ID または名前</span><span class="sxs-lookup"><span data-stu-id="930ae-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="930ae-127">色 ID または名前</span><span class="sxs-lookup"><span data-stu-id="930ae-127">Color ID or name</span></span>
    -   <span data-ttu-id="930ae-128">サイズ ID または名前</span><span class="sxs-lookup"><span data-stu-id="930ae-128">Size ID or name</span></span>
    -   <span data-ttu-id="930ae-129">スタイル ID または名前</span><span class="sxs-lookup"><span data-stu-id="930ae-129">Style ID or name</span></span>

<span data-ttu-id="930ae-130">製品バリアント ID 番号の分類を定義した後に、製品分析コード グループに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="930ae-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="930ae-131">その後、この製品分析コード グループを参照するすべての製品の製品マスターに、分類に基づいて製品バリアント番号が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="930ae-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="930ae-132">ただし、製品バリアント名の分類を製品分析コード グループに関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="930ae-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="930ae-133">製品バリアント ID の分類を製品マスターに直接割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="930ae-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="930ae-134">この場合は、製品マスターに属している製品バリアントに、分類に従って製品バリアント番号と名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="930ae-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="930ae-135">例</span><span class="sxs-lookup"><span data-stu-id="930ae-135">Example</span></span>

<span data-ttu-id="930ae-136">T シャツ (TS1234) は、3 つのサイズ (S、M、L)、4 つの色 (赤、緑、青、黄色) および 2 つのスタイル (ポロ、V ネック) で作成されます。</span><span class="sxs-lookup"><span data-stu-id="930ae-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="930ae-137">したがって、24 のバリエーションが可能です (= 3 × 4 × 2)。</span><span class="sxs-lookup"><span data-stu-id="930ae-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="930ae-138">次の区分を持つ製品バリアント番号の分類を作成します。</span><span class="sxs-lookup"><span data-stu-id="930ae-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="930ae-139">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="930ae-139">Product master number</span></span>
2.  <span data-ttu-id="930ae-140">テキスト定数: "-"</span><span class="sxs-lookup"><span data-stu-id="930ae-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="930ae-141">色</span><span class="sxs-lookup"><span data-stu-id="930ae-141">Color</span></span>
4.  <span data-ttu-id="930ae-142">テキスト定数: "-"</span><span class="sxs-lookup"><span data-stu-id="930ae-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="930ae-143">サイズ</span><span class="sxs-lookup"><span data-stu-id="930ae-143">Size</span></span>
6.  <span data-ttu-id="930ae-144">テキスト定数: "-"</span><span class="sxs-lookup"><span data-stu-id="930ae-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="930ae-145">スタイル</span><span class="sxs-lookup"><span data-stu-id="930ae-145">Style</span></span>

<span data-ttu-id="930ae-146">この場合、赤、S、ポロの製品バリアント番号は TS1234-Red-Small-Polo になります。</span><span class="sxs-lookup"><span data-stu-id="930ae-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="930ae-147">制約ベースのコンフィギュレーションの分類</span><span class="sxs-lookup"><span data-stu-id="930ae-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="930ae-148">制約ベースのコンフィギュレーションの場合、製品分析コードのコンフィギュレーションに対して専門の分類を作成できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="930ae-149">**製品の分類** ページで次の区分を選択できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="930ae-150">番号順序値</span><span class="sxs-lookup"><span data-stu-id="930ae-150">Number sequence value</span></span>
-   <span data-ttu-id="930ae-151">テキスト定数</span><span class="sxs-lookup"><span data-stu-id="930ae-151">Text constant</span></span>
-   <span data-ttu-id="930ae-152">属性値</span><span class="sxs-lookup"><span data-stu-id="930ae-152">Attribute value</span></span>

<span data-ttu-id="930ae-153">製品コンフィギュレーション モデルの各コンポーネントで、独自のコンフィギュレーションの分類を使用できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="930ae-154">コンポーネントに属する属性のみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="930ae-155">サブコンポーネントまたはユーザー要件の属性は使用できません。</span><span class="sxs-lookup"><span data-stu-id="930ae-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="930ae-156">例</span><span class="sxs-lookup"><span data-stu-id="930ae-156">Example</span></span>

<span data-ttu-id="930ae-157">製品コンフィギュレーション モデルには 2 つの属性があるルート コンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="930ae-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="930ae-158">材料 (プラスチック、木材、スチール)</span><span class="sxs-lookup"><span data-stu-id="930ae-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="930ae-159">期間 (10...100)</span><span class="sxs-lookup"><span data-stu-id="930ae-159">Length (10...100)</span></span>

<span data-ttu-id="930ae-160">次の区分を持つコンフィギュレーションの分類を作成します。</span><span class="sxs-lookup"><span data-stu-id="930ae-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="930ae-161">属性値: 材料</span><span class="sxs-lookup"><span data-stu-id="930ae-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="930ae-162">テキスト定数: "AAA"</span><span class="sxs-lookup"><span data-stu-id="930ae-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="930ae-163">属性値: 長さ</span><span class="sxs-lookup"><span data-stu-id="930ae-163">Attribute value: Length</span></span>

<span data-ttu-id="930ae-164">この場合、78 の長さの木材が材料のコンフィギュレーション ID は WoodAAA78 になります。</span><span class="sxs-lookup"><span data-stu-id="930ae-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="930ae-165">分析コードベースのコンフィギュレーションの分類</span><span class="sxs-lookup"><span data-stu-id="930ae-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="930ae-166">分析コードベースのコンフィギュレーションの場合、製品分析コードのコンフィギュレーションに対して専門の分類を作成できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="930ae-167">**製品の分類** ページで次の区分を選択できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="930ae-168">番号順序値</span><span class="sxs-lookup"><span data-stu-id="930ae-168">Number sequence value</span></span>
-   <span data-ttu-id="930ae-169">テキスト定数</span><span class="sxs-lookup"><span data-stu-id="930ae-169">Text constant</span></span>
-   <span data-ttu-id="930ae-170">コンフィギュレーション グループ品目</span><span class="sxs-lookup"><span data-stu-id="930ae-170">Configuration group item</span></span>

<span data-ttu-id="930ae-171">コンフィギュレーションの分類は、部品表 (BOM) に対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="930ae-172">例</span><span class="sxs-lookup"><span data-stu-id="930ae-172">Example</span></span>

<span data-ttu-id="930ae-173">BOM には、2 つのコンフィギュレーション グループに分割される 4 つの BOM 明細行があります。</span><span class="sxs-lookup"><span data-stu-id="930ae-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="930ae-174">BOM 明細行: M0007、 標準キャビネット</span><span class="sxs-lookup"><span data-stu-id="930ae-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="930ae-175">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="930ae-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="930ae-176">BOM 明細行: M0008、ハイ エンド キャビネット</span><span class="sxs-lookup"><span data-stu-id="930ae-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="930ae-177">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="930ae-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="930ae-178">BOM 明細行: M0021、フロント グリルの布</span><span class="sxs-lookup"><span data-stu-id="930ae-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="930ae-179">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="930ae-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="930ae-180">BOM 明細行: M0022、フロント グリルの金属</span><span class="sxs-lookup"><span data-stu-id="930ae-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="930ae-181">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="930ae-181">Configuration group: Front grill</span></span>

<span data-ttu-id="930ae-182">次の区分を持つコンフィギュレーションの分類を作成します。</span><span class="sxs-lookup"><span data-stu-id="930ae-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="930ae-183">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="930ae-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="930ae-184">テキスト定数: "&"</span><span class="sxs-lookup"><span data-stu-id="930ae-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="930ae-185">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="930ae-185">Configuration group: Front grill</span></span>

<span data-ttu-id="930ae-186">この場合、布のフロント グリルが付いた標準キャビネットの構成 ID は M0007&M0021 になります。</span><span class="sxs-lookup"><span data-stu-id="930ae-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="930ae-187">製品バリアントおよびコンフィギュレーションの組み合わせの分類</span><span class="sxs-lookup"><span data-stu-id="930ae-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="930ae-188">制約ベースのコンフィギュレーション テクノロジまたは分析コードベースのコンフィギュレーション テクノロジを使用して、製品マスターの製品バリアントを設定する場合、製品バリアントの製品バリアント番号にコンフィギュレーション分析コードの分類を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="930ae-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="930ae-189">バリアントをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="930ae-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="930ae-190">**製品の分類** ページで、コンフィギュレーション分析コードを含む製品バリアント番号の分類を定義します。</span><span class="sxs-lookup"><span data-stu-id="930ae-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="930ae-191">コンフィギュレーション分析コードを持つ製品分析コード グループにこの分類を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="930ae-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="930ae-192">コンポーネントのためのコンフィギュレーションの分類を定義するか、または製品のバリアントをコンフィギュレーションするために使用される BOM を定義します。</span><span class="sxs-lookup"><span data-stu-id="930ae-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="930ae-193">製品バリアント名の分類を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="930ae-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="930ae-194">コンフィギュレーション ID または名前を含めるには、製品バリアント名をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="930ae-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="930ae-195">制約ベースの製品コンフィギュレーションの例</span><span class="sxs-lookup"><span data-stu-id="930ae-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="930ae-196">この例では、次の区分から構成される製品バリアント番号の分類を使用します。</span><span class="sxs-lookup"><span data-stu-id="930ae-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="930ae-197">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="930ae-197">Product master number</span></span>
2.  <span data-ttu-id="930ae-198">テキスト定数 "\_"</span><span class="sxs-lookup"><span data-stu-id="930ae-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="930ae-199">構成</span><span class="sxs-lookup"><span data-stu-id="930ae-199">Configuration</span></span>

<span data-ttu-id="930ae-200">コンフィギュレーションの分類は、次の区分を使用して構成されます。</span><span class="sxs-lookup"><span data-stu-id="930ae-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="930ae-201">属性値: 材料</span><span class="sxs-lookup"><span data-stu-id="930ae-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="930ae-202">テキスト定数: "AAA"</span><span class="sxs-lookup"><span data-stu-id="930ae-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="930ae-203">属性値: 長さ</span><span class="sxs-lookup"><span data-stu-id="930ae-203">Attribute value: Length</span></span>

<span data-ttu-id="930ae-204">セグメントに次の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="930ae-205">製品マスター番号 = **M0099**</span><span class="sxs-lookup"><span data-stu-id="930ae-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="930ae-206">材料 = **プラスチック**</span><span class="sxs-lookup"><span data-stu-id="930ae-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="930ae-207">長さ = **12**</span><span class="sxs-lookup"><span data-stu-id="930ae-207">Length = **12**</span></span>

<span data-ttu-id="930ae-208">この場合、製品バリアント番号は M0099\_PlasticAAA12 になります。</span><span class="sxs-lookup"><span data-stu-id="930ae-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="930ae-209">分析コードベースのコンフィギュレーションの例</span><span class="sxs-lookup"><span data-stu-id="930ae-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="930ae-210">この例では、次の区分から構成される製品バリアント番号の分類を使用します。</span><span class="sxs-lookup"><span data-stu-id="930ae-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="930ae-211">製品マスター番号</span><span class="sxs-lookup"><span data-stu-id="930ae-211">Product master number</span></span>
2.  <span data-ttu-id="930ae-212">テキスト定数 "//"</span><span class="sxs-lookup"><span data-stu-id="930ae-212">Text constant "//"</span></span>
3.  <span data-ttu-id="930ae-213">構成</span><span class="sxs-lookup"><span data-stu-id="930ae-213">Configuration</span></span>

<span data-ttu-id="930ae-214">コンフィギュレーションの分類は、次の区分を使用して構成されます。</span><span class="sxs-lookup"><span data-stu-id="930ae-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="930ae-215">コンフィギュレーション グループ: キャビネット</span><span class="sxs-lookup"><span data-stu-id="930ae-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="930ae-216">テキスト定数: "&"</span><span class="sxs-lookup"><span data-stu-id="930ae-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="930ae-217">コンフィギュレーション グループ: フロント グリル</span><span class="sxs-lookup"><span data-stu-id="930ae-217">Configuration group: Front grill</span></span>

<span data-ttu-id="930ae-218">セグメントに次の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="930ae-219">製品マスター番号 = **D0123**</span><span class="sxs-lookup"><span data-stu-id="930ae-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="930ae-220">キャビネット= **M0008**</span><span class="sxs-lookup"><span data-stu-id="930ae-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="930ae-221">フロント グリル = **M0022**</span><span class="sxs-lookup"><span data-stu-id="930ae-221">Front grill = **M0022**</span></span>

<span data-ttu-id="930ae-222">この場合、製品のリアント番号は D0123//M0008&M0022 になります。</span><span class="sxs-lookup"><span data-stu-id="930ae-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="930ae-223">競合数</span><span class="sxs-lookup"><span data-stu-id="930ae-223">Numbering conflicts</span></span>
<span data-ttu-id="930ae-224">場合によっては、設定する製品バリアント番号の分類によって一意の製品バリアント番号が作成されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="930ae-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="930ae-225">たとえば、事前に定義されたバリアント コンフィギュレーション テクノロジを使用する製品マスターの分類に、有効な製品分析コードが含まれていないと、製品バリアント番号は一意になりません。</span><span class="sxs-lookup"><span data-stu-id="930ae-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="930ae-226">競合を処理する方法は、コンフィギュレーション テクノロジによって異なります。</span><span class="sxs-lookup"><span data-stu-id="930ae-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="930ae-227">事前に定義されたバリアント</span><span class="sxs-lookup"><span data-stu-id="930ae-227">Predefined variants</span></span>

<span data-ttu-id="930ae-228">製品バリアントの手動の作成または自動的な生成を試み、複数の製品バリアントが同じ製品バリアント番号になる場合は、エラーになります。</span><span class="sxs-lookup"><span data-stu-id="930ae-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="930ae-229">このシナリオを回避するには、製品の分析コード グループのすべての有効な製品分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="930ae-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="930ae-230">または、製品バリアント番号が一意であることを保証するために役立つ番号順序を含めます。</span><span class="sxs-lookup"><span data-stu-id="930ae-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="930ae-231">制約ベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="930ae-231">Constraint-based configurations</span></span>

<span data-ttu-id="930ae-232">分類によっては、システムはコンフィギュレーションに対して一意ではない製品バリアント番号を割り当てようとする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="930ae-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="930ae-233">この場合、システムは製品バリアント番号としてコンフィギュレーション分析コードの番号順序を代わりに使用します。こうした場合は、警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="930ae-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="930ae-234">このシナリオを避けるには、一意の製品バリアント番号を保証するために役立つ十分な属性を分類に含めます。</span><span class="sxs-lookup"><span data-stu-id="930ae-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="930ae-235">また、コンポーネントに対して **再利用** オプションがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="930ae-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="930ae-236">分析コードベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="930ae-236">Dimension-based configurations</span></span>

<span data-ttu-id="930ae-237">コンフィギュレーション プロセスの 1 つのステップ中に、分類に基づいてコンフィギュレーション値が提案されます。</span><span class="sxs-lookup"><span data-stu-id="930ae-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="930ae-238">このステップでは、コンフィギュレーションの値を手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="930ae-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="930ae-239">コンフィギュレーションを保存すると、コンフィギュレーション値が一意かどうかが確認されます。</span><span class="sxs-lookup"><span data-stu-id="930ae-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="930ae-240">入力した値が一意でない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="930ae-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="930ae-241">コンフィギュレーションを保存するためには、一意のコンフィギュレーション値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="930ae-241">To save the configuration, you must enter a unique configuration value.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="930ae-242">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="930ae-242">Additional resources</span></span>

[<span data-ttu-id="930ae-243">事前定義された製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="930ae-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="930ae-244">コンフィギュレーション済製品バリアントにおける製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="930ae-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]