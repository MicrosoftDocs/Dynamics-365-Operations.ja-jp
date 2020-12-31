---
title: データ エンティティの動作プロパティ
description: このトピックでは、そのエンティティのデータ ソースであるテーブルまたはビューのプロパティ値をオーバーライドさせるビヘイビア データ エンティティのプロパティについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91c4b2914f58f8545ab1846481b99378658da33e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688214"
---
# <a name="behavioral-properties-on-data-entities"></a><span data-ttu-id="3373e-103">データ エンティティの動作プロパティ</span><span class="sxs-lookup"><span data-stu-id="3373e-103">Behavioral properties on data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3373e-104">すべてのデータ エンティティには、そのエンティティのデータソースであるテーブルまたはビューの同じプロパティ値をオーバーライドできるようにするプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="3373e-104">Every data entity has properties that let you override the same property values on the tables or views that are the data sources of that entity.</span></span> <span data-ttu-id="3373e-105">選択内容は、エンティティの動作に影響します。</span><span class="sxs-lookup"><span data-stu-id="3373e-105">Your choices affect the behavior of the entity.</span></span> <span data-ttu-id="3373e-106">次の表では、最初の列に、このトピックで説明したプロパティが一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="3373e-106">In the following table, the first column lists the properties that are discussed in this topic.</span></span> <span data-ttu-id="3373e-107">一番上の行には、エンティティ デザイナーでプロパティが見つかったレベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-107">The top row lists the levels where the property is found in the entity designer.</span></span> <span data-ttu-id="3373e-108">レベルは、精度の細かい順に一覧表示されます。データ ソース レベルはエンティティ レベルよりも細かく、フィールド レベルほどは細かくはありません。</span><span class="sxs-lookup"><span data-stu-id="3373e-108">The levels are listed in order of increasing granularity: the data source level is more granular than the entity level but less granular than the field level.</span></span>

|  &nbsp;           | <span data-ttu-id="3373e-109">エンティティ レベル</span><span class="sxs-lookup"><span data-stu-id="3373e-109">Entity level</span></span> | <span data-ttu-id="3373e-110">データ ソース レベル</span><span class="sxs-lookup"><span data-stu-id="3373e-110">Data source level</span></span> | <span data-ttu-id="3373e-111">フィールド レベル</span><span class="sxs-lookup"><span data-stu-id="3373e-111">Field level</span></span> |
|-------------------|--------------|-------------------|-------------|
| <span data-ttu-id="3373e-112">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3373e-112">ReadOnly</span></span>          | <span data-ttu-id="3373e-113">適用</span><span class="sxs-lookup"><span data-stu-id="3373e-113">Applies</span></span>      | <span data-ttu-id="3373e-114">適用</span><span class="sxs-lookup"><span data-stu-id="3373e-114">Applies</span></span>           | <span data-ttu-id="3373e-115">.</span><span class="sxs-lookup"><span data-stu-id="3373e-115">.</span></span>           |
| <span data-ttu-id="3373e-116">AllowEdit</span><span class="sxs-lookup"><span data-stu-id="3373e-116">AllowEdit</span></span>         | <span data-ttu-id="3373e-117">.</span><span class="sxs-lookup"><span data-stu-id="3373e-117">.</span></span>            | <span data-ttu-id="3373e-118">.</span><span class="sxs-lookup"><span data-stu-id="3373e-118">.</span></span>                 | <span data-ttu-id="3373e-119">適用</span><span class="sxs-lookup"><span data-stu-id="3373e-119">Applies</span></span>     |
| <span data-ttu-id="3373e-120">AllowEditOnCreate</span><span class="sxs-lookup"><span data-stu-id="3373e-120">AllowEditOnCreate</span></span> | <span data-ttu-id="3373e-121">.</span><span class="sxs-lookup"><span data-stu-id="3373e-121">.</span></span>            | <span data-ttu-id="3373e-122">.</span><span class="sxs-lookup"><span data-stu-id="3373e-122">.</span></span>                 | <span data-ttu-id="3373e-123">適用</span><span class="sxs-lookup"><span data-stu-id="3373e-123">Applies</span></span>     |
| <span data-ttu-id="3373e-124">必須</span><span class="sxs-lookup"><span data-stu-id="3373e-124">Mandatory</span></span>         | <span data-ttu-id="3373e-125">.</span><span class="sxs-lookup"><span data-stu-id="3373e-125">.</span></span>            | <span data-ttu-id="3373e-126">.</span><span class="sxs-lookup"><span data-stu-id="3373e-126">.</span></span>                 | <span data-ttu-id="3373e-127">適用</span><span class="sxs-lookup"><span data-stu-id="3373e-127">Applies</span></span>     |

## <a name="entity-level"></a><span data-ttu-id="3373e-128">エンティティ レベル</span><span class="sxs-lookup"><span data-stu-id="3373e-128">Entity level</span></span>
<span data-ttu-id="3373e-129">データ エンティティのデザイナーで、ルート ノードの名前をクリックすると、**プロパティ** ウィンドウに **読み取り専用** プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="3373e-129">In the designer for your data entity, when you click the name at the root node, the **Properties** pane includes the **Is Read Only** property.</span></span> <span data-ttu-id="3373e-130">次のテーブルは、このプロパティの **Yes** と **No** 値の間の動作上の相違点を示しています。</span><span class="sxs-lookup"><span data-stu-id="3373e-130">The following table describes the behavioral differences between the **Yes** and **No** values of this property.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3373e-131">グループ化</span><span class="sxs-lookup"><span data-stu-id="3373e-131">Group</span></span></th>
<th><span data-ttu-id="3373e-132">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="3373e-132">Property name</span></span></th>
<th><span data-ttu-id="3373e-133">表示名</span><span class="sxs-lookup"><span data-stu-id="3373e-133">Display name</span></span></th>
<th><span data-ttu-id="3373e-134">値</span><span class="sxs-lookup"><span data-stu-id="3373e-134">Values</span></span></th>
<th><span data-ttu-id="3373e-135">既定</span><span class="sxs-lookup"><span data-stu-id="3373e-135">Default</span></span></th>
<th><span data-ttu-id="3373e-136">説明</span><span class="sxs-lookup"><span data-stu-id="3373e-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3373e-137">動作</span><span class="sxs-lookup"><span data-stu-id="3373e-137">Behavior</span></span></td>
<td><span data-ttu-id="3373e-138">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="3373e-138">IsReadOnly</span></span></td>
<td><span data-ttu-id="3373e-139">読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="3373e-139">Is Read Only</span></span></td>
<td><span data-ttu-id="3373e-140">いいえ、はい</span><span class="sxs-lookup"><span data-stu-id="3373e-140">No, Yes</span></span></td>
<td><span data-ttu-id="3373e-141">無</span><span class="sxs-lookup"><span data-stu-id="3373e-141">No</span></span></td>
<td><ul>
<li><span data-ttu-id="3373e-142"><strong>いいえ:</strong> エンティティのデザイナー内の個別のデータ ソース ノードが <strong>IsReadOnly</strong> = <strong>はい</strong>に設定されて<em>いない限り</em>、データ変更操作 (CUD) <em>は</em>許可されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-142"><strong>No:</strong> Data modification operations (CUD) <em>are</em> allowed, <em>unless</em> an individual data source node in the entity's designer is set to <strong>IsReadOnly</strong> = <strong>Yes</strong>.</span></span></li>
<li><span data-ttu-id="3373e-143"><strong>はい:</strong> エンティティのデザイナ内の個々のデータソースノードの <strong>IsReadOnly</strong> 設定に関係なく、読み取り操作のみが許可されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-143"><strong>Yes:</strong> Only read operations are allowed, regardless of the <strong>IsReadOnly</strong> settings on the individual data source nodes in the entity's designer.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3373e-144">主にエクスポートに使用されるエンティティに対して、**IsReadOnly** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3373e-144">You would set **IsReadOnly** to **Yes** for entities that are consumed mainly for export.</span></span>

## <a name="data-source-level"></a><span data-ttu-id="3373e-145">データ ソース レベル</span><span class="sxs-lookup"><span data-stu-id="3373e-145">Data source level</span></span>
<span data-ttu-id="3373e-146">データ エンティティに 3 つのデータ ソースがある場合は、その中から 2 つではなく、1 つのデータ ソースのデータを変更するために、エンティティを使用するためのプロセスを許可する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3373e-146">If a data entity has three data sources, you might want to allow processes to use the entity to modify the data in one of the data sources but not in the other two.</span></span> <span data-ttu-id="3373e-147">読み取り専用データ ソースは参照目的で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3373e-147">A read-only data source can be used for lookup purposes.</span></span> <span data-ttu-id="3373e-148">エンティティ デザイナーを使用すると、この非常に制度の高い制御を達成することができます。</span><span class="sxs-lookup"><span data-stu-id="3373e-148">You can use the entity designer to achieve this extra degree of granular control.</span></span> <span data-ttu-id="3373e-149">エンティティの **メタデータ**&gt;**データ ソース** ノードで、エンティティ ノードを選択すると、その 1 つのデータソースの **IsReadOnly** プロパティの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3373e-149">Under the entity's **Metadata** &gt; **Data Sources** node, you can select an entity node and then set the **IsReadOnly** property value for that one data source.</span></span> <span data-ttu-id="3373e-150">次のテーブルでは、データ ソース レベルの **IsReadOnly** 設定とエンティティ レベルの相互作用について説明します。</span><span class="sxs-lookup"><span data-stu-id="3373e-150">The following table describes the interaction between the **IsReadOnly** settings at the data source level and the entity level.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3373e-151">グループ化</span><span class="sxs-lookup"><span data-stu-id="3373e-151">Group</span></span></th>
<th><span data-ttu-id="3373e-152">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="3373e-152">Property name</span></span></th>
<th><span data-ttu-id="3373e-153">表示名</span><span class="sxs-lookup"><span data-stu-id="3373e-153">Display name</span></span></th>
<th><span data-ttu-id="3373e-154">値</span><span class="sxs-lookup"><span data-stu-id="3373e-154">Values</span></span></th>
<th><span data-ttu-id="3373e-155">既定</span><span class="sxs-lookup"><span data-stu-id="3373e-155">Default</span></span></th>
<th><span data-ttu-id="3373e-156">説明</span><span class="sxs-lookup"><span data-stu-id="3373e-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3373e-157">動作</span><span class="sxs-lookup"><span data-stu-id="3373e-157">Behavior</span></span></td>
<td><span data-ttu-id="3373e-158">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="3373e-158">IsReadOnly</span></span></td>
<td><span data-ttu-id="3373e-159">読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="3373e-159">Is Read Only</span></span></td>
<td><span data-ttu-id="3373e-160">いいえ、はい</span><span class="sxs-lookup"><span data-stu-id="3373e-160">No, Yes</span></span></td>
<td><span data-ttu-id="3373e-161">無</span><span class="sxs-lookup"><span data-stu-id="3373e-161">No</span></span></td>
<td><ul>
<li><span data-ttu-id="3373e-162"><strong>いいえ:</strong> エンティティ レベルで <strong>IsReadOnly</strong> が<strong>はい</strong>に設定されて<em>いない限り</em>、データ変更操作 (CUD) <em>は</em>データ ソースで許可されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-162"><strong>No:</strong> Data modification operations (CUD) <em>are</em> allowed on the data source, <em>unless</em> <strong>IsReadOnly</strong> is set to <strong>Yes</strong> at the entity level.</span></span></li>
<li><span data-ttu-id="3373e-163"><strong>はい:</strong> エンティティの <strong>IsReadOnly</strong> 設定に関係なく、操作のみが許可されます</span><span class="sxs-lookup"><span data-stu-id="3373e-163"><strong>Yes:</strong> Only operations are allowed, regardless of the <strong>IsReadOnly</strong> setting on the entity.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="field-level"></a><span data-ttu-id="3373e-164">フィールド レベル</span><span class="sxs-lookup"><span data-stu-id="3373e-164">Field level</span></span>
<span data-ttu-id="3373e-165">フィールド レベルにおいて、**AllowEdit** と **AllowEditOnCreate** プロパティは **IsReadOnly** プロパティの代わりに利用可能です。</span><span class="sxs-lookup"><span data-stu-id="3373e-165">At the field level, the **AllowEdit** and **AllowEditOnCreate** properties are available instead of an **IsReadOnly** property.</span></span> <span data-ttu-id="3373e-166">2 つの **許可** プロパティには、3 番目の利用可能な値として **自動** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3373e-166">The two **Allow** properties include **Auto** as a third available value.</span></span> <span data-ttu-id="3373e-167">**自動** 値は、基になっているテーブルのフィールドにある値を継承します。</span><span class="sxs-lookup"><span data-stu-id="3373e-167">The **Auto** value inherits the value that is on the field in the underlying table.</span></span>

> [!NOTE]
> <span data-ttu-id="3373e-168">**自動** の値は、計算フィールドや仮想フィールドなどのマップされていないフィールドでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="3373e-168">The **Auto** value isn't available for unmapped fields, such as computed or virtual fields.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3373e-169">グループ化</span><span class="sxs-lookup"><span data-stu-id="3373e-169">Group</span></span></th>
<th><span data-ttu-id="3373e-170">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="3373e-170">Property name</span></span></th>
<th><span data-ttu-id="3373e-171">表示名</span><span class="sxs-lookup"><span data-stu-id="3373e-171">Display name</span></span></th>
<th><span data-ttu-id="3373e-172">先頭値</span><span class="sxs-lookup"><span data-stu-id="3373e-172">Value</span></span></th>
<th><span data-ttu-id="3373e-173">既定</span><span class="sxs-lookup"><span data-stu-id="3373e-173">Default</span></span></th>
<th><span data-ttu-id="3373e-174">説明</span><span class="sxs-lookup"><span data-stu-id="3373e-174">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3373e-175">動作</span><span class="sxs-lookup"><span data-stu-id="3373e-175">Behavior</span></span></td>
<td><span data-ttu-id="3373e-176">AllowEditOnCreate</span><span class="sxs-lookup"><span data-stu-id="3373e-176">AllowEditOnCreate</span></span></td>
<td><span data-ttu-id="3373e-177">作成時の編集を許可</span><span class="sxs-lookup"><span data-stu-id="3373e-177">Allow edit on create</span></span></td>
<td><span data-ttu-id="3373e-178">自動、いいえ、はい</span><span class="sxs-lookup"><span data-stu-id="3373e-178">Auto, No, Yes</span></span></td>
<td><span data-ttu-id="3373e-179">自動</span><span class="sxs-lookup"><span data-stu-id="3373e-179">Auto</span></span></td>
<td><ul>
<li><span data-ttu-id="3373e-180"><strong>自動:</strong> 基になるテーブル フィールドから、プロパティを継承します。</span><span class="sxs-lookup"><span data-stu-id="3373e-180"><strong>Auto:</strong> The property is inherited from the underlying table field.</span></span>
<blockquote>[!NOTE] <span data-ttu-id="3373e-181"><strong>自動</strong>の値は、計算フィールドや仮想フィールドなどのマップされていないフィールドでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="3373e-181">The <strong>Auto</strong> value isn't available for unmapped fields, such as computed or virtual fields.</span></span></blockquote>
</li>
<li><span data-ttu-id="3373e-182"><strong>いいえ:</strong> ユーザーは、このフィールドのデータを新しいレコードで変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="3373e-182"><strong>No:</strong> Users aren't allowed to modify the data for this field in a new record.</span></span></li>
<li><span data-ttu-id="3373e-183"><strong>はい:</strong> ユーザーは、このフィールドのデータを新しいレコードに対して変更することができます。</span><span class="sxs-lookup"><span data-stu-id="3373e-183"><strong>Yes:</strong> Users are allowed to modify the data for this field for a new record.</span></span></li>
</ul>
<span data-ttu-id="3373e-184">この動作は、すべてのコンシューマー (X++、OData など) に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-184">This behavior is enforced for all consumers – X++, OData, and so on.</span></span>
<blockquote>[!IMPORTANT] <span data-ttu-id="3373e-185"><strong>いいえ</strong>および<strong>はい</strong>の値は、基になるテーブル内のフィールドの設定を上書き<em>しません</em>。</span><span class="sxs-lookup"><span data-stu-id="3373e-185">The <strong>No</strong> and <strong>Yes</strong> values do <em>not</em> override the setting on the field in the underlying table.</span></span></blockquote></td>
</tr>
<tr>
<td><span data-ttu-id="3373e-186">動作</span><span class="sxs-lookup"><span data-stu-id="3373e-186">Behavior</span></span></td>
<td><span data-ttu-id="3373e-187">AllowEdit</span><span class="sxs-lookup"><span data-stu-id="3373e-187">AllowEdit</span></span></td>
<td><span data-ttu-id="3373e-188">編集を許可</span><span class="sxs-lookup"><span data-stu-id="3373e-188">Allow edit</span></span></td>
<td><span data-ttu-id="3373e-189">自動、いいえ、はい</span><span class="sxs-lookup"><span data-stu-id="3373e-189">Auto, No, Yes</span></span></td>
<td><span data-ttu-id="3373e-190">自動</span><span class="sxs-lookup"><span data-stu-id="3373e-190">Auto</span></span></td>
<td><span data-ttu-id="3373e-191">動作は、<strong>AllowEditOnCreate</strong> の動作と同じですが、作成されている新しいレコードではなく、<em>既存の</em>レコードへの更新に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-191">The behavior is the same as the behavior for <strong>AllowEditOnCreate</strong>, but it applies to updates to <em>existing</em> records instead of new records that are being created.</span></span> <span data-ttu-id="3373e-192">この動作は、すべてのコンシューマー (X++、OData など) に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-192">This behavior is enforced for all consumers – X++, OData, and so on.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3373e-193">動作</span><span class="sxs-lookup"><span data-stu-id="3373e-193">Behavior</span></span></td>
<td><span data-ttu-id="3373e-194">必須</span><span class="sxs-lookup"><span data-stu-id="3373e-194">Mandatory</span></span></td>
<td><span data-ttu-id="3373e-195">必須</span><span class="sxs-lookup"><span data-stu-id="3373e-195">Mandatory</span></span></td>
<td><span data-ttu-id="3373e-196">自動、いいえ、はい</span><span class="sxs-lookup"><span data-stu-id="3373e-196">Auto, No, Yes</span></span></td>
<td><span data-ttu-id="3373e-197">自動</span><span class="sxs-lookup"><span data-stu-id="3373e-197">Auto</span></span></td>
<td><span data-ttu-id="3373e-198"><strong>自動:</strong> 基になるテーブル フィールドから、プロパティを継承します。</span><span class="sxs-lookup"><span data-stu-id="3373e-198"><strong>Auto:</strong> The property is inherited from the underlying table field.</span></span> <span data-ttu-id="3373e-199">この動作は、すべてのコンシューマー (X++、OData など) に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3373e-199">This behavior is enforced for all consumers – X++, OData, and so on.</span></span>
<blockquote>[!IMPORTANT] <span data-ttu-id="3373e-200"><strong>いいえ</strong>および<strong>はい</strong>の値は、基になるテーブル内のフィールドの設定を上書き<em>しません</em>。</span><span class="sxs-lookup"><span data-stu-id="3373e-200">The <strong>No</strong> and <strong>Yes</strong> values do <em>not</em> override the setting on the field in the underlying table.</span></span></blockquote></td>
</tr>
</tbody>
</table>
