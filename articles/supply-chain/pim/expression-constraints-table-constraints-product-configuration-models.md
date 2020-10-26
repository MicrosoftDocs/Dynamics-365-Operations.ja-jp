---
title: 製品コンフィギュレーション モデルでの式の制約とテーブルの制約
description: このトピックでは、式の制約およびテーブル制約の使用について説明します。 制約は、販売注文、販売見積、発注書、または製造オーダーのための製品をコンフィギュレーションするときに選択できる属性値を制御します。 制約の作成方法に基づいて、式の制約またはテーブル制約を使用できます。
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979831"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="aad73-105">製品コンフィギュレーション モデルでの式の制約とテーブルの制約</span><span class="sxs-lookup"><span data-stu-id="aad73-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aad73-106">このトピックでは、式の制約およびテーブル制約の使用について説明します。</span><span class="sxs-lookup"><span data-stu-id="aad73-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="aad73-107">制約は、販売注文、販売見積、発注書、または製造オーダーのための製品をコンフィギュレーションするときに選択できる属性値を制御します。</span><span class="sxs-lookup"><span data-stu-id="aad73-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="aad73-108">制約の作成方法に基づいて、式の制約またはテーブル制約を使用できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="aad73-109">制約は、販売注文、販売見積、発注書、または製造オーダーのための製品をコンフィギュレーションするときに選択できる属性値の制御に使用します。</span><span class="sxs-lookup"><span data-stu-id="aad73-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="aad73-110">制約の作成方法に基づいて、式の制約またはテーブル制約を使用できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="aad73-111">式の制約とは</span><span class="sxs-lookup"><span data-stu-id="aad73-111">What are expression constraints?</span></span>
<span data-ttu-id="aad73-112">式の制約の特徴は、式が算術演算子およびブール演算子と関数を使用することです。</span><span class="sxs-lookup"><span data-stu-id="aad73-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="aad73-113">式の制約は、製品コンフィギュレーション モデルの特定のコンポーネントに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="aad73-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="aad73-114">他のコンポーネントで再利用することも、また他のコンポーネントと共有することもできません。</span><span class="sxs-lookup"><span data-stu-id="aad73-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="aad73-115">ただし、コンポーネントの式の制約は、コンポーネントのサブコンポーネントの属性を参照できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="aad73-116">テーブル制約とは</span><span class="sxs-lookup"><span data-stu-id="aad73-116">What are table constraints?</span></span>
<span data-ttu-id="aad73-117">テーブル制約では、製品のコンフィギュレーション時に属性として許される値の組み合わせをリストします。</span><span class="sxs-lookup"><span data-stu-id="aad73-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="aad73-118">テーブル制約の定義は、総称的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="aad73-119">製品コンフィギュレーション モデルのコンポーネントのテーブル制約を作成する場合、テーブル制約定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="aad73-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="aad73-120">許される組み合わせを作成するには、特定のタイプの属性をコンポーネントに追加します。</span><span class="sxs-lookup"><span data-stu-id="aad73-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="aad73-121">各属性タイプは特定の値を所有します。</span><span class="sxs-lookup"><span data-stu-id="aad73-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="aad73-122">テーブル制約の例</span><span class="sxs-lookup"><span data-stu-id="aad73-122">Example of a table constraint</span></span>

<span data-ttu-id="aad73-123">この例では、スピーカーのコンフィギュレーションを特定のキャビネットの仕上げと前グリルに限定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="aad73-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="aad73-124">最初の表には、コンフィギュレーションで一般に使用できるキャビネットの仕上げと前グリルを示します。</span><span class="sxs-lookup"><span data-stu-id="aad73-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="aad73-125">値は、**キャビネットの仕上げ**と**前グリル**の属性タイプで定義されます。</span><span class="sxs-lookup"><span data-stu-id="aad73-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="aad73-126">属性の型</span><span class="sxs-lookup"><span data-stu-id="aad73-126">Attribute type</span></span> | <span data-ttu-id="aad73-127">値</span><span class="sxs-lookup"><span data-stu-id="aad73-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="aad73-128">キャビネットの仕上げ</span><span class="sxs-lookup"><span data-stu-id="aad73-128">Cabinet finish</span></span> | <span data-ttu-id="aad73-129">黒、カシ、シタン、白</span><span class="sxs-lookup"><span data-stu-id="aad73-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="aad73-130">前グリル</span><span class="sxs-lookup"><span data-stu-id="aad73-130">Front grill</span></span>    | <span data-ttu-id="aad73-131">黒、メタル、白</span><span class="sxs-lookup"><span data-stu-id="aad73-131">Black, Metal, White</span></span>         |

<span data-ttu-id="aad73-132">次の表には、**色と仕上げ**テーブルの制約によって定義される組み合わせを示します。</span><span class="sxs-lookup"><span data-stu-id="aad73-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="aad73-133">このテーブルの制約を使用すると、カシの仕上げと黒いグリルのスピーカー、シタンの仕上げと白いグリルのスピーカーなどをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="aad73-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="aad73-134">完了</span><span class="sxs-lookup"><span data-stu-id="aad73-134">Finish</span></span>         | <span data-ttu-id="aad73-135">グリル</span><span class="sxs-lookup"><span data-stu-id="aad73-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="aad73-136">カシ</span><span class="sxs-lookup"><span data-stu-id="aad73-136">Oak</span></span>            | <span data-ttu-id="aad73-137">黒</span><span class="sxs-lookup"><span data-stu-id="aad73-137">Black</span></span>                       |
| <span data-ttu-id="aad73-138">シタン</span><span class="sxs-lookup"><span data-stu-id="aad73-138">Rosewood</span></span>       | <span data-ttu-id="aad73-139">白</span><span class="sxs-lookup"><span data-stu-id="aad73-139">White</span></span>                       |
| <span data-ttu-id="aad73-140">白</span><span class="sxs-lookup"><span data-stu-id="aad73-140">White</span></span>          | <span data-ttu-id="aad73-141">黒</span><span class="sxs-lookup"><span data-stu-id="aad73-141">Black</span></span>                       |
| <span data-ttu-id="aad73-142">白</span><span class="sxs-lookup"><span data-stu-id="aad73-142">White</span></span>          | <span data-ttu-id="aad73-143">白</span><span class="sxs-lookup"><span data-stu-id="aad73-143">White</span></span>                       |
| <span data-ttu-id="aad73-144">黒</span><span class="sxs-lookup"><span data-stu-id="aad73-144">Black</span></span>          | <span data-ttu-id="aad73-145">黒</span><span class="sxs-lookup"><span data-stu-id="aad73-145">Black</span></span>                       |
| <span data-ttu-id="aad73-146">黒</span><span class="sxs-lookup"><span data-stu-id="aad73-146">Black</span></span>          | <span data-ttu-id="aad73-147">メタル</span><span class="sxs-lookup"><span data-stu-id="aad73-147">Metal</span></span>                       | 

<span data-ttu-id="aad73-148">システム定義テーブル制約とユーザー定義テーブル制約を作成できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="aad73-149">詳細については、[システム定義およびユーザー定義のテーブル制約](system-defined-user-defined-table-constraints.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aad73-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="aad73-150">どのような構文で制約を記述しますか。</span><span class="sxs-lookup"><span data-stu-id="aad73-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="aad73-151">制約を記述するには、OML (Optimization Modeling Language) の構文を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aad73-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="aad73-152">システムでは、Microsoft Solver Foundation 制約ソルバーを使用して制約を解決します。</span><span class="sxs-lookup"><span data-stu-id="aad73-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="aad73-153">テーブル制約または式の制約の使用</span><span class="sxs-lookup"><span data-stu-id="aad73-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="aad73-154">制約を作成する方法に基づいて、式の制約またはテーブル制約のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="aad73-155">テーブル制約はマトリックスとして構築しますが、式の制約は個別の文です。</span><span class="sxs-lookup"><span data-stu-id="aad73-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="aad73-156">製品をコンフィギュレーションするとき、使用する制約の種類は重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="aad73-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="aad73-157">2 つのメソッドの違いを次に示します。</span><span class="sxs-lookup"><span data-stu-id="aad73-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="aad73-158">次の制約設定を使用して製品をコンフィギュレーションする場合、以下の組み合わせを使用できますます。</span><span class="sxs-lookup"><span data-stu-id="aad73-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="aad73-159">色が黒、サイズが 30 または 50 の製品</span><span class="sxs-lookup"><span data-stu-id="aad73-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="aad73-160">色が赤、サイズが 20 の製品</span><span class="sxs-lookup"><span data-stu-id="aad73-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="aad73-161">テーブル制約の設定</span><span class="sxs-lookup"><span data-stu-id="aad73-161">Table constraint setup</span></span>

| <span data-ttu-id="aad73-162">色</span><span class="sxs-lookup"><span data-stu-id="aad73-162">Color</span></span> | <span data-ttu-id="aad73-163">サイズ</span><span class="sxs-lookup"><span data-stu-id="aad73-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="aad73-164">黒</span><span class="sxs-lookup"><span data-stu-id="aad73-164">Black</span></span> | <span data-ttu-id="aad73-165">30</span><span class="sxs-lookup"><span data-stu-id="aad73-165">30</span></span>   |
| <span data-ttu-id="aad73-166">黒</span><span class="sxs-lookup"><span data-stu-id="aad73-166">Black</span></span> | <span data-ttu-id="aad73-167">50</span><span class="sxs-lookup"><span data-stu-id="aad73-167">50</span></span>   |
| <span data-ttu-id="aad73-168">赤</span><span class="sxs-lookup"><span data-stu-id="aad73-168">Red</span></span>   | <span data-ttu-id="aad73-169">20</span><span class="sxs-lookup"><span data-stu-id="aad73-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="aad73-170">式の制約設定</span><span class="sxs-lookup"><span data-stu-id="aad73-170">Expression constraint setup</span></span>

<span data-ttu-id="aad73-171">(色 == "黒" & (サイズ == "30" | サイズ == "50")) | (色 == "赤" & サイズ = "20")</span><span class="sxs-lookup"><span data-stu-id="aad73-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="aad73-172">式の制約の記述時に使用するのは演算子かまたはインフィックス表記法か</span><span class="sxs-lookup"><span data-stu-id="aad73-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="aad73-173">式の制約の記述には、使用可能なプレフィックス演算子か、またはインフィックス表記法のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="aad73-174">演算子 **Min**、**Max**、および **Abs** については、インフィックス表記法を使用できません。</span><span class="sxs-lookup"><span data-stu-id="aad73-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="aad73-175">これらの演算子は、ほとんどのプログラム言語に標準の演算子として含まれています。</span><span class="sxs-lookup"><span data-stu-id="aad73-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="aad73-176">式の制約の記述には、どんな演算子やインフィックス表記法を使用できますか。</span><span class="sxs-lookup"><span data-stu-id="aad73-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="aad73-177">次の表は、製品コンフィギュレーション モデル内のコンポーネントの式の制約を記述するときに使用できる演算子とインフィックス表記法を示します。</span><span class="sxs-lookup"><span data-stu-id="aad73-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="aad73-178">この最初のテーブルの例では、インフィックス表記法または演算子のいずれかを使用して式を記述する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="aad73-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aad73-179">オペレーター</span><span class="sxs-lookup"><span data-stu-id="aad73-179">Operator</span></span></th>
<th><span data-ttu-id="aad73-180">説明</span><span class="sxs-lookup"><span data-stu-id="aad73-180">Description</span></span></th>
<th><span data-ttu-id="aad73-181">構文</span><span class="sxs-lookup"><span data-stu-id="aad73-181">Syntax</span></span></th>
<th><span data-ttu-id="aad73-182">例</span><span class="sxs-lookup"><span data-stu-id="aad73-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aad73-183">Implies</span><span class="sxs-lookup"><span data-stu-id="aad73-183">Implies</span></span></td>
<td><span data-ttu-id="aad73-184">これは最初の条件が false、2 番目の条件が true、または両方とも true の場合に true です。</span><span class="sxs-lookup"><span data-stu-id="aad73-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="aad73-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="aad73-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-186"><strong>オペレーター:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="aad73-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="aad73-187"><strong>インフィックス表記法:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="aad73-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aad73-188">かつ</span><span class="sxs-lookup"><span data-stu-id="aad73-188">And</span></span></td>
<td><span data-ttu-id="aad73-189">これは、すべての条件が true の場合にのみ true です。</span><span class="sxs-lookup"><span data-stu-id="aad73-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="aad73-190">条件数が 0 の場合、<strong>True</strong> になります。</span><span class="sxs-lookup"><span data-stu-id="aad73-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="aad73-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="aad73-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-192"><strong>オペレーター:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="aad73-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="aad73-193"><strong>インフィックス表記法:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="aad73-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aad73-194">又は</span><span class="sxs-lookup"><span data-stu-id="aad73-194">Or</span></span></td>
<td><span data-ttu-id="aad73-195">これは、任意の条件が true の場合に true です。</span><span class="sxs-lookup"><span data-stu-id="aad73-195">This is true if any condition is true.</span></span> <span data-ttu-id="aad73-196">条件数が 0 の場合、<strong>False</strong> になります。</span><span class="sxs-lookup"><span data-stu-id="aad73-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="aad73-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="aad73-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-198"><strong>オペレーター:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="aad73-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="aad73-199"><strong>インフィックス表記法:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="aad73-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aad73-200">プラス</span><span class="sxs-lookup"><span data-stu-id="aad73-200">Plus</span></span></td>
<td><span data-ttu-id="aad73-201">これにより要件が合計されます。</span><span class="sxs-lookup"><span data-stu-id="aad73-201">This sums its conditions.</span></span> <span data-ttu-id="aad73-202">条件数が 0 の場合、<strong>0</strong> になります。</span><span class="sxs-lookup"><span data-stu-id="aad73-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="aad73-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="aad73-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-204"><strong>オペレーター:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="aad73-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="aad73-205"><strong>インフィックス表記法:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="aad73-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aad73-206">マイナス</span><span class="sxs-lookup"><span data-stu-id="aad73-206">Minus</span></span></td>
<td><span data-ttu-id="aad73-207">これは引数を無効にします。</span><span class="sxs-lookup"><span data-stu-id="aad73-207">This negates its argument.</span></span> <span data-ttu-id="aad73-208">これは条件がきっかり 1 つの場合に限ります。</span><span class="sxs-lookup"><span data-stu-id="aad73-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="aad73-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="aad73-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-210"><strong>オペレーター:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="aad73-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="aad73-211"><strong>インフィックス表記法:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="aad73-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aad73-212">Abs</span><span class="sxs-lookup"><span data-stu-id="aad73-212">Abs</span></span></td>
<td><span data-ttu-id="aad73-213">これは、条件の絶対値を取ります。</span><span class="sxs-lookup"><span data-stu-id="aad73-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="aad73-214">これは条件がきっかり 1 つの場合に限ります。</span><span class="sxs-lookup"><span data-stu-id="aad73-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="aad73-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="aad73-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="aad73-216"><strong>オペレーター:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="aad73-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aad73-217">時間</span><span class="sxs-lookup"><span data-stu-id="aad73-217">Times</span></span></td>
<td><span data-ttu-id="aad73-218">これは、条件の製品を取ります。</span><span class="sxs-lookup"><span data-stu-id="aad73-218">This takes the product of its conditions.</span></span> <span data-ttu-id="aad73-219">条件数が 0 の場合、<strong>1</strong> になります。</span><span class="sxs-lookup"><span data-stu-id="aad73-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="aad73-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="aad73-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-221"><strong>オペレーター:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="aad73-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="aad73-222"><strong>インフィックス表記法:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="aad73-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aad73-223">パワー</span><span class="sxs-lookup"><span data-stu-id="aad73-223">Power</span></span></td>
<td><span data-ttu-id="aad73-224">これは、指数関数を取ります。</span><span class="sxs-lookup"><span data-stu-id="aad73-224">This takes an exponential.</span></span> <span data-ttu-id="aad73-225">これはべき乗を右から左に適用します。</span><span class="sxs-lookup"><span data-stu-id="aad73-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="aad73-226">(つまり、右結合です)。したがって、<strong>Power[a, b, c]</strong> は <strong>Power[a, Power[b, c]]</strong> と等価です。</span><span class="sxs-lookup"><span data-stu-id="aad73-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="aad73-227"><strong>Power</strong> は、指数が正の定数の場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="aad73-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="aad73-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="aad73-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-229"><strong>オペレーター:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="aad73-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="aad73-230"><strong>インフィックス表記法:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="aad73-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aad73-231">最大</span><span class="sxs-lookup"><span data-stu-id="aad73-231">Max</span></span></td>
<td><span data-ttu-id="aad73-232">これにより、最大条件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="aad73-232">This produces the largest condition.</span></span> <span data-ttu-id="aad73-233">条件数が 0 の場合、<strong>Infinity</strong> (無限) になります。</span><span class="sxs-lookup"><span data-stu-id="aad73-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="aad73-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="aad73-234">Max[args]</span></span></td>
<td><span data-ttu-id="aad73-235"><strong>オペレーター: </strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="aad73-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aad73-236">最小</span><span class="sxs-lookup"><span data-stu-id="aad73-236">Min</span></span></td>
<td><span data-ttu-id="aad73-237">これにより、最小条件が作成されます。</span><span class="sxs-lookup"><span data-stu-id="aad73-237">This produces the smallest condition.</span></span> <span data-ttu-id="aad73-238">条件数が 0 の場合、<strong>Infinity</strong> (無限) になります。</span><span class="sxs-lookup"><span data-stu-id="aad73-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="aad73-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="aad73-239">Min[args]</span></span></td>
<td><span data-ttu-id="aad73-240"><strong>オペレーター:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="aad73-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aad73-241">ない</span><span class="sxs-lookup"><span data-stu-id="aad73-241">Not</span></span></td>
<td><span data-ttu-id="aad73-242">これにより、条件の論理逆数が作成されます。</span><span class="sxs-lookup"><span data-stu-id="aad73-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="aad73-243">これは条件がきっかり 1 つの場合に限ります。</span><span class="sxs-lookup"><span data-stu-id="aad73-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="aad73-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="aad73-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="aad73-245"><strong>オペレーター:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="aad73-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="aad73-246"><strong>インフィックス表記法:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="aad73-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aad73-247">次の表の例は、インフィックス表記法を記述する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="aad73-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="aad73-248">インフィックス表記法</span><span class="sxs-lookup"><span data-stu-id="aad73-248">Infix notation</span></span>   |                                          <span data-ttu-id="aad73-249">説明</span><span class="sxs-lookup"><span data-stu-id="aad73-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="aad73-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="aad73-250">x + y + z</span></span>     |                                           <span data-ttu-id="aad73-251">追加</span><span class="sxs-lookup"><span data-stu-id="aad73-251">Addition</span></span>                                            |
|    <span data-ttu-id="aad73-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="aad73-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="aad73-253">乗算</span><span class="sxs-lookup"><span data-stu-id="aad73-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="aad73-254">x - y</span><span class="sxs-lookup"><span data-stu-id="aad73-254">x - y</span></span>       | <span data-ttu-id="aad73-255">バイナリ減算は、2 番目の値が負であるバイナリ加算と同様に変換されます。</span><span class="sxs-lookup"><span data-stu-id="aad73-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="aad73-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="aad73-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="aad73-257">右結合の累乗法</span><span class="sxs-lookup"><span data-stu-id="aad73-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="aad73-258">!x</span><span class="sxs-lookup"><span data-stu-id="aad73-258">!x</span></span>         |                                          <span data-ttu-id="aad73-259">ブール値の not</span><span class="sxs-lookup"><span data-stu-id="aad73-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="aad73-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="aad73-260">x -: y</span></span>       |                                      <span data-ttu-id="aad73-261">Boolean の意味</span><span class="sxs-lookup"><span data-stu-id="aad73-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="aad73-262">x</span><span class="sxs-lookup"><span data-stu-id="aad73-262">x</span></span>         |                                               <span data-ttu-id="aad73-263">y</span><span class="sxs-lookup"><span data-stu-id="aad73-263">y</span></span>                                               |
|     <span data-ttu-id="aad73-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="aad73-264">x & y & z</span></span>     |                                          <span data-ttu-id="aad73-265">ブール値 and</span><span class="sxs-lookup"><span data-stu-id="aad73-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="aad73-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="aad73-266">x == y == z</span></span>    |                                           <span data-ttu-id="aad73-267">等式</span><span class="sxs-lookup"><span data-stu-id="aad73-267">Equality</span></span>                                            |
|    <span data-ttu-id="aad73-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="aad73-268">x != y != z</span></span>    |                                           <span data-ttu-id="aad73-269">明確</span><span class="sxs-lookup"><span data-stu-id="aad73-269">Distinct</span></span>                                            |
|  <span data-ttu-id="aad73-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="aad73-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="aad73-271">次の値より小さい</span><span class="sxs-lookup"><span data-stu-id="aad73-271">Less than</span></span>                                           |
|  <span data-ttu-id="aad73-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="aad73-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="aad73-273">次の値より大きい</span><span class="sxs-lookup"><span data-stu-id="aad73-273">Greater than</span></span>                                          |
| <span data-ttu-id="aad73-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="aad73-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="aad73-275">以下</span><span class="sxs-lookup"><span data-stu-id="aad73-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="aad73-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="aad73-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="aad73-277">以上</span><span class="sxs-lookup"><span data-stu-id="aad73-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="aad73-278">(x)</span><span class="sxs-lookup"><span data-stu-id="aad73-278">(x)</span></span>        |                           <span data-ttu-id="aad73-279">かっこは既定の優先順位より優先されます。</span><span class="sxs-lookup"><span data-stu-id="aad73-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="aad73-280">式の制約がなぜ正しく検証されないのですか。</span><span class="sxs-lookup"><span data-stu-id="aad73-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="aad73-281">製品コンフィギュレーション モデルの属性、コンポーネント、またはサブコンポーネントのソルバー名として予約済みのキーワードは使用できません。</span><span class="sxs-lookup"><span data-stu-id="aad73-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="aad73-282">ここでは、使用できない予約済みキーワードの一覧を示します:</span><span class="sxs-lookup"><span data-stu-id="aad73-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="aad73-283">シーリング</span><span class="sxs-lookup"><span data-stu-id="aad73-283">Ceiling</span></span>
-   <span data-ttu-id="aad73-284">要素</span><span class="sxs-lookup"><span data-stu-id="aad73-284">Element</span></span>
-   <span data-ttu-id="aad73-285">等しい</span><span class="sxs-lookup"><span data-stu-id="aad73-285">Equal</span></span>
-   <span data-ttu-id="aad73-286">フロア</span><span class="sxs-lookup"><span data-stu-id="aad73-286">Floor</span></span>
-   <span data-ttu-id="aad73-287">次の場合</span><span class="sxs-lookup"><span data-stu-id="aad73-287">If</span></span>
-   <span data-ttu-id="aad73-288">未満</span><span class="sxs-lookup"><span data-stu-id="aad73-288">Less</span></span>
-   <span data-ttu-id="aad73-289">大きい</span><span class="sxs-lookup"><span data-stu-id="aad73-289">Greater</span></span>
-   <span data-ttu-id="aad73-290">Implies</span><span class="sxs-lookup"><span data-stu-id="aad73-290">Implies</span></span>
-   <span data-ttu-id="aad73-291">ログ</span><span class="sxs-lookup"><span data-stu-id="aad73-291">Log</span></span>
-   <span data-ttu-id="aad73-292">最大</span><span class="sxs-lookup"><span data-stu-id="aad73-292">Max</span></span>
-   <span data-ttu-id="aad73-293">最小</span><span class="sxs-lookup"><span data-stu-id="aad73-293">Min</span></span>
-   <span data-ttu-id="aad73-294">マイナス</span><span class="sxs-lookup"><span data-stu-id="aad73-294">Minus</span></span>
-   <span data-ttu-id="aad73-295">プラス</span><span class="sxs-lookup"><span data-stu-id="aad73-295">Plus</span></span>
-   <span data-ttu-id="aad73-296">パワー</span><span class="sxs-lookup"><span data-stu-id="aad73-296">Power</span></span>
-   <span data-ttu-id="aad73-297">時間</span><span class="sxs-lookup"><span data-stu-id="aad73-297">Times</span></span>
-   <span data-ttu-id="aad73-298">スロット</span><span class="sxs-lookup"><span data-stu-id="aad73-298">Slot</span></span>
-   <span data-ttu-id="aad73-299">モデル</span><span class="sxs-lookup"><span data-stu-id="aad73-299">Model</span></span>
-   <span data-ttu-id="aad73-300">意思決定</span><span class="sxs-lookup"><span data-stu-id="aad73-300">Decision</span></span>
-   <span data-ttu-id="aad73-301">目標</span><span class="sxs-lookup"><span data-stu-id="aad73-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="aad73-302">追加リソース</span><span class="sxs-lookup"><span data-stu-id="aad73-302">Additional resources</span></span>
--------

[<span data-ttu-id="aad73-303">式の制約の作成</span><span class="sxs-lookup"><span data-stu-id="aad73-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="aad73-304">製品コンフィギュレーション モデルへの計算の追加</span><span class="sxs-lookup"><span data-stu-id="aad73-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



