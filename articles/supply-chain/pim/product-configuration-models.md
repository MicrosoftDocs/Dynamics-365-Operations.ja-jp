---
title: 製品コンフィギュレーション モデルの概要
description: この記事では、製品コンフィギュレーション モデルに関連する用語と概念を定義します。 製品コンフィギュレーション モデルを使用すると、単一の製品に多数の製品バリアントをコンフィギュレーションするのに使用できるノーブランド商品の構造を構築することができます。
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87d61203d36722194b98a247609fa126b71b846c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431735"
---
# <a name="product-configuration-models-overview"></a><span data-ttu-id="36ab2-104">製品コンフィギュレーション モデルの概要</span><span class="sxs-lookup"><span data-stu-id="36ab2-104">Product configuration models overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36ab2-105">この記事では、製品コンフィギュレーション モデルに関連する用語と概念を定義します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-105">This article defines terms and concepts that are relevant to product configuration models.</span></span> <span data-ttu-id="36ab2-106">製品コンフィギュレーション モデルを使用すると、単一の製品に多数の製品バリアントをコンフィギュレーションするのに使用できるノーブランド商品の構造を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-106">Product configuration models let you build a generic product structure that can be used to configure many product variants for a single product.</span></span>

<span data-ttu-id="36ab2-107">製品コンフィギュレーション モデルは、ノーブランド商品の構造を表すために作成されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-107">Product configuration models are created to represent a generic product structure.</span></span> <span data-ttu-id="36ab2-108">製品コンフィギュレーション モデルを設定した後に、固有の部品表 (BOM) および固有の工順がある特徴的製品のバリアントをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-108">After you've set up a product configuration model, you can configure a distinct product variant that has a unique bill of materials (BOM) and a unique route.</span></span> <span data-ttu-id="36ab2-109">製品コンフィギュレーション モデルは宣言制約と必須計算の両方を使用して、異なる製品バリアント間の関係と制限を処理します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-109">Product configuration models use both declarative constraints and imperative calculations to handle the relations and limitations between different product variants.</span></span> <span data-ttu-id="36ab2-110">販売注文、販売見積、発注書、および製造オーダーの品目をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-110">You can configure items on sales orders, sales quotations, purchase orders, and production orders.</span></span> <span data-ttu-id="36ab2-111">次の表に、テーブル制約ベースの条件および概念を示します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-111">The following table describes the table constraint–based terms and concepts.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36ab2-112">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="36ab2-112">Components</span></span></td>
<td><span data-ttu-id="36ab2-113">コンポーネントは製品コンフィギュレーション モデルの主要な構成要素です。</span><span class="sxs-lookup"><span data-stu-id="36ab2-113">Components are the main building blocks of a product configuration model.</span></span> <span data-ttu-id="36ab2-114">コンポーネントは<strong>制約ベースの製品コンフィギュレーション モデルの詳細</strong>ページのツリー構造に表示されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-114">Components are displayed in a tree structure on the <strong>Constraint-based product configuration model details</strong> page.</span></span> <span data-ttu-id="36ab2-115">コンポーネントは次の要素を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-115">Components can contain the following elements:</span></span>
<ul>
<li><span data-ttu-id="36ab2-116">属性</span><span class="sxs-lookup"><span data-stu-id="36ab2-116">Attributes</span></span></li>
<li><span data-ttu-id="36ab2-117">制約</span><span class="sxs-lookup"><span data-stu-id="36ab2-117">Constraints</span></span></li>
<li><span data-ttu-id="36ab2-118">計算</span><span class="sxs-lookup"><span data-stu-id="36ab2-118">Calculations</span></span></li>
<li><span data-ttu-id="36ab2-119">サブコンポーネント</span><span class="sxs-lookup"><span data-stu-id="36ab2-119">Subcomponents</span></span></li>
<li><span data-ttu-id="36ab2-120">ユーザーの要件</span><span class="sxs-lookup"><span data-stu-id="36ab2-120">User requirements</span></span></li>
<li><span data-ttu-id="36ab2-121">BOM 明細行</span><span class="sxs-lookup"><span data-stu-id="36ab2-121">BOM lines</span></span></li>
<li><span data-ttu-id="36ab2-122">工順工程</span><span class="sxs-lookup"><span data-stu-id="36ab2-122">Route operations</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ab2-123">属性</span><span class="sxs-lookup"><span data-stu-id="36ab2-123">Attributes</span></span></td>
<td><span data-ttu-id="36ab2-124">属性は製品コンフィギュレーション モデルのすべての機能を表します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-124">Attributes describe all the features of the product configuration model.</span></span> <span data-ttu-id="36ab2-125">属性は特徴的製品の構成時に選択できる機能の指定に使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-125">You can use attributes to specify the features that can be selected when a distinct product is configured.</span></span> <span data-ttu-id="36ab2-126">属性は制約および条件に使用されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-126">Attributes are used in constraints and conditions.</span></span> <span data-ttu-id="36ab2-127">属性を作成して製品コンフィギュレーション モデルに追加する際には、関連する属性タイプが参照されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-127">When attributes are created and added to a product configuration model, the related attribute types are referenced.</span></span> <span data-ttu-id="36ab2-128">属性には既定値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-128">A default value can be set for an attribute.</span></span> <span data-ttu-id="36ab2-129">既定値は、製品コンフィギュレーション モデルのコンフィギュレーション時に、コンフィギュレーション ユーザー インターフェイス (UI) で使用されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-129">The default value is used in the configuration user interface (UI) when the product configuration model is configured.</span></span> <span data-ttu-id="36ab2-130">属性は、必須、読み取り専用、または非表示にするように指定できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-130">You can specify that an attribute is mandatory, read-only, or hidden.</span></span>
<ul>
<li><span data-ttu-id="36ab2-131"><strong>必須</strong> – 製品の構成時に属性に設定する必要がある値。</span><span class="sxs-lookup"><span data-stu-id="36ab2-131"><strong>Mandatory</strong> – A value must be set for the attribute when the product is configured.</span></span></li>
<li><span data-ttu-id="36ab2-132"><strong>読み取り専用</strong> – 属性値はコンフィギュレーション セッション中に表示されますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="36ab2-132"><strong>Read-only</strong> – The attribute value is displayed during a configuration session, but it can&#39;t be changed.</span></span></li>
<li><span data-ttu-id="36ab2-133"><strong>非表示</strong> – 属性値は制約と条件に含まれますが、コンフィギュレーション セッション中には表示されません。</span><span class="sxs-lookup"><span data-stu-id="36ab2-133"><strong>Hidden</strong> – The attribute value is included in constraints and conditions, but isn&#39;t displayed during a configuration session.</span></span></li>
</ul>
<span data-ttu-id="36ab2-134">また、属性の条件も指定できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-134">You can also specify a condition for attributes.</span></span> <span data-ttu-id="36ab2-135">条件を満たした場合は、必須属性に値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-135">If the condition is met, a value must be entered for the mandatory attribute.</span></span> <span data-ttu-id="36ab2-136">条件は、製品コンフィギュレーション モデルに含める属性、BOM 明細行、および工順工程に対して満たす必要のある式です。</span><span class="sxs-lookup"><span data-stu-id="36ab2-136">Conditions are expressions that must be met for attributes, BOM lines, and route operations to be included in a product configuration model.</span></span> <span data-ttu-id="36ab2-137">条件で参照する属性はすべて必須となります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-137">Any attribute that is referenced in a condition becomes mandatory.</span></span> <span data-ttu-id="36ab2-138"><strong>属性</strong>タブで必須として属性を選択することをお勧めします。これは、必須の属性を識別しやすいためです。</span><span class="sxs-lookup"><span data-stu-id="36ab2-138">We recommend that you select attributes as mandatory on the <strong>Attributes</strong> tab. This can make it easier to identify mandatory attributes.</span></span> <span data-ttu-id="36ab2-139">属性値は、コンフィギュレーションの再利用に重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="36ab2-139">Attribute values are an important part of reusing configurations.</span></span> <span data-ttu-id="36ab2-140">システムは、コンフィギュレーション セッション中にユーザーが行った選択と一致するコンフィギュレーションがあるかどうかを、属性値を使用して判断します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-140">The system uses attribute values to determine whether a configuration exists that matches the selections that a user made during a configuration session.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ab2-141">属性タイプ</span><span class="sxs-lookup"><span data-stu-id="36ab2-141">Attribute types</span></span></td>
<td><span data-ttu-id="36ab2-142">属性タイプは、コンフィギュレーション製品モデルで使用されている属性のデータ型のセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-142">Attribute types specify the set of data types for attributes that are used in a product configuration model.</span></span> <span data-ttu-id="36ab2-143">次の属性タイプが使用されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-143">The following attribute types are used:</span></span>
<ul>
<li><span data-ttu-id="36ab2-144">範囲の有無にかかわらない<strong>整数</strong></span><span class="sxs-lookup"><span data-stu-id="36ab2-144"><strong>Integer</strong> with or without a range</span></span></li>
<li><span data-ttu-id="36ab2-145"><strong>実数</strong></span><span class="sxs-lookup"><span data-stu-id="36ab2-145"><strong>Decimal</strong></span></span></li>
<li><span data-ttu-id="36ab2-146">固定リストの有無にかかわらない<strong>テキスト</strong></span><span class="sxs-lookup"><span data-stu-id="36ab2-146"><strong>Text</strong> with or without a fixed list</span></span></li>
<li><span data-ttu-id="36ab2-147"><strong>ブール値</strong></span><span class="sxs-lookup"><span data-stu-id="36ab2-147"><strong>Boolean</strong></span></span></li>
</ul>
<span data-ttu-id="36ab2-148">属性タイプが範囲のある<strong>ブール型</strong>、<strong>整数</strong>、または固定リストのある<strong>テキスト</strong>の場合、値のセットは製品コンフィギュレーション モデルが設定されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-148">If the attribute type is <strong>Boolean</strong>, <strong>Integer</strong> with a range, or <strong>Text</strong> with a fixed list, the set of values is available when a product configuration model is set up.</span></span> <span data-ttu-id="36ab2-149"><strong>注記:</strong> 製品コンフィギュレーション ソルバー では、<strong>ブール型</strong>、固定リストのある <strong>テキスト</strong>、および範囲のある <strong>整数</strong> のみを属性タイプとして認識します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-149"><strong>Note:</strong> The Product configuration solver recognizes only the following attribute types: <strong>Boolean</strong>, <strong>Text</strong> with a fixed list, and <strong>Integer</strong> with a range.</span></span> <span data-ttu-id="36ab2-150">したがって、式の制約と条件ではこれらの属性タイプのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-150">Therefore, only these attribute types can be used in expression constraints and conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ab2-151">制約</span><span class="sxs-lookup"><span data-stu-id="36ab2-151">Constraints</span></span></td>
<td><span data-ttu-id="36ab2-152">制約はプロダクト モデルのコンフィギュレーションの制限を表します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-152">Constraints describe the restrictions of the product model configuration.</span></span> <span data-ttu-id="36ab2-153">制約を使用することで、製品がコンフィギュレーションされている時に、必ず有効値のみが選択されるようになります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-153">Constraints are used to guarantee that only valid values are selected when a product is being configured.</span></span> <span data-ttu-id="36ab2-154">制約は式の制約やテーブルの制約のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="36ab2-154">Constraints can be either expression constraints or table constraints:</span></span>
<ul>
<li><span data-ttu-id="36ab2-155">式の制約は関連付けられたコンポーネントにのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-155">Expression constraints can be used only for the component that they are tied to.</span></span> <span data-ttu-id="36ab2-156">コンポーネントの式の制約は、コンポーネントのサブコンポーネントの属性を参照できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-156">The expression constraints for a component can reference attributes of the component&#39;s subcomponents.</span></span> <span data-ttu-id="36ab2-157">製品 Solver configuration は制約の決済に使用されます。制約を書き込む際には Solver の構文を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-157">The Product configuration solver is used to solve the constraints, and you must use the solver syntax when you write the constraints.</span></span> <span data-ttu-id="36ab2-158">詳細については、式の制約およびテーブルの制約に関するトピック リンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="36ab2-158">For more information, see the topic link about expression constraints and table constraints.</span></span></li>
<li><span data-ttu-id="36ab2-159">テーブル制約は、製品コンフィギュレーション モデル内のコンポーネントに適用する前に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-159">Table constraints must be defined before they can be applied to a component in a product configuration model.</span></span> <span data-ttu-id="36ab2-160">テーブルの制約は、ユーザーまたはシステムに定義されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-160">Table constraints can be either user-defined or system-defined.</span></span> <span data-ttu-id="36ab2-161">ユーザー定義のテーブル制約は、属性タイプで定義されている属性値の組み合わせセットの説明に使用できるマトリックス タイプです。</span><span class="sxs-lookup"><span data-stu-id="36ab2-161">A user-defined table constraint is a type of matrix that can be used to describe the set of combinations for the attribute values that are defined by attribute types.</span></span> <span data-ttu-id="36ab2-162">たとえば、スピーカー生産の場合、ユーザー定義のテーブル制約のマトリックスには、スピーカーの表面処理とグリルの列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-162">For example, if speakers are produced, the matrix for a user-defined table constraint might have columns for the speaker finish and grill.</span></span></li>
</ul><span data-ttu-id="36ab2-163">
<strong>例</strong> スピーカーの表面処理には黒、カシ、シタン、白色の 4 つが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="36ab2-163">
<strong>Example</strong> Speakers are available in four finishes: Black, Oak, Rosewood, and White.</span></span> <span data-ttu-id="36ab2-164">スピーカーには、ブラック、メタル、またはホワイトの 3 つの前グリルがあります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-164">The speakers can have one of three front grills: Black, Metal, or White.</span></span> <span data-ttu-id="36ab2-165">ブラック仕上げはすべてのグリルで利用できますが、他の仕上げは特定のグリルに限られています。</span><span class="sxs-lookup"><span data-stu-id="36ab2-165">The Black finish is available for all grills, but the other finishes are limited to specific grills.</span></span> <span data-ttu-id="36ab2-166">次の表には、<strong>テーブルの制約の編集</strong>ページの<strong>許可済み組み合わせ</strong>タブに表示される情報の例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-166">The following table shows an example of the information that is displayed on the <strong>Allowed combinations</strong> tab on the <strong>Edit table constraint</strong> page.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="36ab2-167">キャビネットの仕上げ</span><span class="sxs-lookup"><span data-stu-id="36ab2-167">Cabinet finish</span></span></th>
<th><span data-ttu-id="36ab2-168">前グリル</span><span class="sxs-lookup"><span data-stu-id="36ab2-168">Front grill</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36ab2-169">黒</span><span class="sxs-lookup"><span data-stu-id="36ab2-169">Black</span></span></td>
<td><span data-ttu-id="36ab2-170">黒</span><span class="sxs-lookup"><span data-stu-id="36ab2-170">Black</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ab2-171">黒</span><span class="sxs-lookup"><span data-stu-id="36ab2-171">Black</span></span></td>
<td><span data-ttu-id="36ab2-172">メタル</span><span class="sxs-lookup"><span data-stu-id="36ab2-172">Metal</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ab2-173">黒</span><span class="sxs-lookup"><span data-stu-id="36ab2-173">Black</span></span></td>
<td><span data-ttu-id="36ab2-174">白</span><span class="sxs-lookup"><span data-stu-id="36ab2-174">White</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ab2-175">カシ</span><span class="sxs-lookup"><span data-stu-id="36ab2-175">Oak</span></span></td>
<td><span data-ttu-id="36ab2-176">黒</span><span class="sxs-lookup"><span data-stu-id="36ab2-176">Black</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ab2-177">シタン</span><span class="sxs-lookup"><span data-stu-id="36ab2-177">Rosewood</span></span></td>
<td><span data-ttu-id="36ab2-178">白</span><span class="sxs-lookup"><span data-stu-id="36ab2-178">White</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ab2-179">白</span><span class="sxs-lookup"><span data-stu-id="36ab2-179">White</span></span></td>
<td><span data-ttu-id="36ab2-180">黒</span><span class="sxs-lookup"><span data-stu-id="36ab2-180">Black</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ab2-181">白</span><span class="sxs-lookup"><span data-stu-id="36ab2-181">White</span></span></td>
<td><span data-ttu-id="36ab2-182">白</span><span class="sxs-lookup"><span data-stu-id="36ab2-182">White</span></span></td>
</tr>
</tbody>
</table>
<span data-ttu-id="36ab2-183">システム定義のテーブル制約は、属性タイプと Supply Chain Management テーブルのフィールドとの間のマッピングを表します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-183">A system-defined table constraint represents a mapping between an attribute type and a field in a Supply Chain Management table.</span></span> <span data-ttu-id="36ab2-184">システム定義のテーブル制約は、属性タイプとフィールドを動的にリンクさせます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-184">A system-defined table constraint dynamically links the attribute type to the field.</span></span> <span data-ttu-id="36ab2-185">このリンクを使用すると、製品コンフィギュレーション モデルの属性が、フィールドのデータを Supply Chain Management テーブルに反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-185">The link enables the attribute in a product configuration model to reflect the data of the field in the Supply Chain Management table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ab2-186">計算</span><span class="sxs-lookup"><span data-stu-id="36ab2-186">Calculations</span></span></td>
<td><span data-ttu-id="36ab2-187">計算は制約の補足を表します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-187">Calculations represent a supplement to constraints.</span></span> <span data-ttu-id="36ab2-188"><strong>小数</strong> および <strong>整数</strong> 型の算術演算、または固定リストのある <strong>テキスト</strong> および <strong>ブール</strong> 型の属性に関係する論理工程を実行する計算を使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-188">You can use a calculation to perform arithmetic operations on attributes of the <strong>Decimal</strong> and <strong>Integer</strong> types, or logical operations that involve attributes of the <strong>Text</strong> with a fixed list and <strong>Boolean</strong> types.</span></span> <span data-ttu-id="36ab2-189">計算には計算式の結果を保持するターゲット属性があります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-189">A calculation has a target attribute that will hold the result of the calculation expression.</span></span> <span data-ttu-id="36ab2-190">式エディタを使用して計算式を構築します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-190">The calculation expression is built by using the expression editor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ab2-191">サブコンポーネント</span><span class="sxs-lookup"><span data-stu-id="36ab2-191">Subcomponents</span></span></td>
<td><span data-ttu-id="36ab2-192">サブコンポーネントには、製品コンフィギュレーション モデルのツリー構造が反映されます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-192">Subcomponents reflect the tree structure of the product configuration model.</span></span> <span data-ttu-id="36ab2-193">サブコンポーネントは製品コンフィギュレーション モデル構造の作成に使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-193">You can use subcomponents to build the structure of the product configuration model.</span></span> <span data-ttu-id="36ab2-194">サブコンポーネントは既存のコンポーネントを参照します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-194">Subcomponents reference existing components.</span></span> <span data-ttu-id="36ab2-195">したがって、サブコンポーネントによって、複数の製品コンフィギュレーション モデルのコンポーネントの再利用が容易になります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-195">Therefore, subcomponents encourage the reuse of components in multiple product configuration models.</span></span> <span data-ttu-id="36ab2-196">サブコンポーネントの <strong>BOM 明細行の詳細</strong>ページでは、サブコンポーネントに固有の値を選択できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-196">On the <strong>BOM line details</strong> page for a subcomponent, you can select a distinct value for the subcomponent.</span></span> <span data-ttu-id="36ab2-197">また、製品コンフィギュレーション モデルの設定時に選択する値の属性を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-197">Alternatively, you can select an attribute that the value is selected for when the product configuration model is set up.</span></span> <span data-ttu-id="36ab2-198">コンポーネントまたはサブコンポーネントとして製品を含めるには、製品の作成時に<strong>製品の作成</strong>ページの次の情報を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-198">To include a product as a component or subcomponent, you must specify the following information on the <strong>Create product</strong> page when you create the product:</span></span>
<ul>
<li><span data-ttu-id="36ab2-199"><strong>製品タイプ</strong> フィールドで、<strong>品目</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-199">In the <strong>Product type</strong> field, select <strong>Item</strong>.</span></span></li>
<li><span data-ttu-id="36ab2-200"><strong>製品サブタイプ</strong> フィールドで、<strong>製品マスター</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-200">In the <strong>Product subtype</strong> field, select <strong>Product master</strong>.</span></span></li>
<li><span data-ttu-id="36ab2-201"><strong>コンフィギュレーション テクノロジ</strong> フィールドで、<strong>制約ベースのコンフィギュレーション</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-201">In the <strong>Configuration technology</strong> field, select <strong>Constraint-based configuration</strong>.</span></span></li>
</ul>
<span data-ttu-id="36ab2-202">リリースされた製品をコンポーネントまたはサブコンポーネントとして使用できるかどうかは、<strong>リリース済製品の詳細</strong> ページの <strong>一般</strong> タブで確認できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-202">You can view whether a released product can be used as a component or subcomponent on the <strong>General</strong> tab of the <strong>Released product details</strong> page.</span></span> <span data-ttu-id="36ab2-203"><strong>コンフィギュレーション テクノロジ</strong> フィールドで、<strong>制約ベースのコンフィギュレーション</strong> を選択した場合、製品はコンポーネントまたはサブコンポーネントとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-203">If <strong>Constraint-based configuration</strong> is selected in the <strong>Configuration technology</strong> field, the product can be used as a component or subcomponent.</span></span> <span data-ttu-id="36ab2-204">サブコンポーネントは、コンフィギュレーション セッション中にユーザーに表示されないように、非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-204">You can hide subcomponents so that they aren&#39;t displayed to the user during a configuration session.</span></span> <span data-ttu-id="36ab2-205">属性、サブコンポーネント、およびサブコンポーネントに関連付けられたユーザー要件も非表示になります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-205">Attributes, subcomponents, and user requirements that are related to the subcomponent are also hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ab2-206">ユーザーの要件</span><span class="sxs-lookup"><span data-stu-id="36ab2-206">User requirements</span></span></td>
<td><span data-ttu-id="36ab2-207">ユーザー要件は、ユーザー要件と特定のコンポーネントおよび属性との間の抽象的概念を表します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-207">User requirements represent an abstraction between user requirements and specific components and attributes.</span></span> <span data-ttu-id="36ab2-208">ユーザー要件は品目にはマップできません。</span><span class="sxs-lookup"><span data-stu-id="36ab2-208">You can&#39;t map a user requirement to an item.</span></span> <span data-ttu-id="36ab2-209">たとえば、顧客がホーム シアター システムを購入しようとしているとします。</span><span class="sxs-lookup"><span data-stu-id="36ab2-209">For example, a customer is shopping for a home theater system.</span></span> <span data-ttu-id="36ab2-210">販売担当者は、システムをインストールする部屋のサイズを顧客に質問することで、必要なワットを決められます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-210">The sales representative might ask about the size of the room where the customer plans to install the system, to determine how many watts are required.</span></span> <span data-ttu-id="36ab2-211">この例では、部屋のサイズが、特定のコンポーネントに適切な属性値を決定する際のユーザー要件となります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-211">In this example, the room size can be a user requirement that helps determine the appropriate attribute value for a specific component.</span></span> <span data-ttu-id="36ab2-212">ユーザー要件は、コンフィギュレーション セッション中にユーザーに表示されないように、非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-212">You can hide user requirements so that they aren&#39;t displayed to the user during a configuration session.</span></span> <span data-ttu-id="36ab2-213">属性、サブコンポーネント、およびユーザー要件に関連付けられたユーザー要件も非表示になります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-213">Attributes, subcomponents, and user requirements that are related to the user requirement are also hidden.</span></span> <span data-ttu-id="36ab2-214">ユーザー要件を非表示にするかどうかの条件は記述できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-214">You can write a condition to control whether a user requirement can be hidden.</span></span> <span data-ttu-id="36ab2-215">条件を記述するには、OML (Optimization Modeling Language) の構文を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36ab2-215">You must write the condition by using Optimization Modeling Language (OML) syntax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ab2-216">BOM 明細行</span><span class="sxs-lookup"><span data-stu-id="36ab2-216">BOM lines</span></span></td>
<td><span data-ttu-id="36ab2-217">BOM 明細行は、製品コンフィギュレーション モデルのコンポーネントの個々の材料を表します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-217">BOM lines represent the individual materials of the components in the product configuration model.</span></span> <span data-ttu-id="36ab2-218"><strong>BOM 明細行の詳細</strong>ページで、すべての品目を選択できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-218">On the <strong>BOM line details</strong> page, all items are available for selection.</span></span> <span data-ttu-id="36ab2-219">BOM 明細行には、特徴的製品のバリアントに対して選択した BOM 明細行が、製品コンフィギュレーション モデル設定時のユーザーの選択に基づいて変わるように条件を追加できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-219">A condition can be added to the BOM line, so that the BOM lines that are selected for a distinct product variant can vary, based on the user&#39;s selection when the product configuration model is set up.</span></span> <span data-ttu-id="36ab2-220">条件は、製品コンフィギュレーション モデルに含める属性、BOM 明細行、および工順工程に対して満たす必要のある式です。</span><span class="sxs-lookup"><span data-stu-id="36ab2-220">Conditions are expressions that must be met for attributes, BOM lines, and route operations to be included in a product configuration model.</span></span> <span data-ttu-id="36ab2-221"><strong>BOM明細行の詳細</strong>ページで、固有の値を選択できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-221">On the <strong>BOM line details</strong> page, you can select a distinct value.</span></span> <span data-ttu-id="36ab2-222">また、製品コンフィギュレーション モデルの設定時に選択する値の属性にマップさせることもできます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-222">Alternatively, you can map to an attribute that the value is selected for when the product configuration model is set up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ab2-223">工順工程</span><span class="sxs-lookup"><span data-stu-id="36ab2-223">Route operations</span></span></td>
<td><span data-ttu-id="36ab2-224"><strong>工順工程の詳細</strong>ページで、固有の値を選択できます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-224">On the <strong>Route operation details</strong> page, you can select a distinct value.</span></span> <span data-ttu-id="36ab2-225">また、製品コンフィギュレーション モデルの設定時に選択する値の属性にマップさせることもできます。</span><span class="sxs-lookup"><span data-stu-id="36ab2-225">Alternatively, you can map to an attribute that the value is selected for when the product configuration model is set up.</span></span> <span data-ttu-id="36ab2-226">条件は式の制約と同じように記述します。</span><span class="sxs-lookup"><span data-stu-id="36ab2-226">Conditions are written like expression constraints.</span></span> <span data-ttu-id="36ab2-227">条件は、製品コンフィギュレーション モデルに含める属性、BOM 明細行、および工順工程に対して満たす必要のある式です。</span><span class="sxs-lookup"><span data-stu-id="36ab2-227">Conditions are expressions that must be met for attributes, BOM lines, and route operations to be included in a product configuration model.</span></span></td>
</tr>
</tbody>
</table>





