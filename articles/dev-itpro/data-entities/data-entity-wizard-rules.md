---
title: データ エンティティ ウィザード ルール
description: このトピックでは、代理外部キー フィールドのナチュラル キー拡張と子/親関係の拡張について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 6234
ms.assetid: 551ac5d6-980c-487f-a15c-66d7ab80924a
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16ed5b22fcea4b2e43e3b9c38930c8776ba00e4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368514"
---
# <a name="data-entity-wizard-rules"></a><span data-ttu-id="02662-103">データ エンティティ ウィザード ルール</span><span class="sxs-lookup"><span data-stu-id="02662-103">Data entity wizard rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02662-104">このトピックでは、代理外部キー フィールドのナチュラル キー拡張と子/親関係の拡張について説明します。</span><span class="sxs-lookup"><span data-stu-id="02662-104">This topic provides information about the natural key expansion of surrogate foreign key fields and the expansion of child/parent relations.</span></span>

## <a name="natural-key-expansion-of-surrogate-foreign-keys"></a><span data-ttu-id="02662-105">代理外部キーのナチュラル キー拡張</span><span class="sxs-lookup"><span data-stu-id="02662-105">Natural key expansion of surrogate foreign keys</span></span>

<span data-ttu-id="02662-106">代理外部キー フィールドの拡張データ型は、**RefRecId** または派生である必要があります。</span><span class="sxs-lookup"><span data-stu-id="02662-106">A surrogate foreign key field's extended data type must be **RefRecId** or a derivative.</span></span> <span data-ttu-id="02662-107">代理外部キー フィールドのナチュラル キー拡張は、次の一覧のルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="02662-107">The natural key expansion of a surrogate foreign key field uses the rules in the following list.</span></span> <span data-ttu-id="02662-108">これらのルールは、評価の順に記載されています。</span><span class="sxs-lookup"><span data-stu-id="02662-108">These rules are listed in the order of evaluation.</span></span>

1. <span data-ttu-id="02662-109">**交換キー** – 交換キー フィールド</span><span class="sxs-lookup"><span data-stu-id="02662-109">**Replacement key** – The replacement key fields</span></span>
2. <span data-ttu-id="02662-110">**主キー** – プライマリ インデックス キー フィールド</span><span class="sxs-lookup"><span data-stu-id="02662-110">**Primary key** – The primary index key fields</span></span>
3. <span data-ttu-id="02662-111">**代替キー** - 最初の固有の代替キー</span><span class="sxs-lookup"><span data-stu-id="02662-111">**Alternate key** – The first unique alternate key</span></span>
4. <span data-ttu-id="02662-112">**自動 ID キー** - 自動 ID フィールド</span><span class="sxs-lookup"><span data-stu-id="02662-112">**Auto-identification key** – The auto-identification fields</span></span>

<span data-ttu-id="02662-113">ナチュラル キーで入れ子になっている代理外部キー フィールドは、再帰的に展開されます。</span><span class="sxs-lookup"><span data-stu-id="02662-113">Surrogate foreign key fields that are nested in the natural key are recursively expanded.</span></span> <span data-ttu-id="02662-114">定期的な入れ子になったサロゲートは、最初の事例に限定されます。</span><span class="sxs-lookup"><span data-stu-id="02662-114">Recurring nested surrogates are limited to the first occurrence.</span></span> <span data-ttu-id="02662-115">代理外部キーの **is mapped** プロパティを選択すると (つまり、プロパティを **true** に設定すると)、関連するデータソースがエンティティに自動的に追加され、関連するデータソースにあるナチュラル キーの各フィールドの **is mapped** プロパティが選択されます。</span><span class="sxs-lookup"><span data-stu-id="02662-115">If you select the **is mapped** property of a surrogate foreign key (that is, if you set the property to **true**), the related data source is automatically added to the entity, and the **is mapped** property of each field in the related data source's natural key is selected.</span></span> <span data-ttu-id="02662-116">さらに、入れ子になった代理外部キーのデータ ソースは、再帰的にエンティティに追加されます。</span><span class="sxs-lookup"><span data-stu-id="02662-116">In addition, any nested surrogate foreign key data sources are recursively added to the entity.</span></span> <span data-ttu-id="02662-117">代理外部キーの **is mapped** プロパティ (つまりプロパティを **false** に設定する場合) をクリアする場合、関連するデータ ソースが自動的に削除され、エンティティとネストされた代理外部データ ソースから自動的にマップ解除されます。</span><span class="sxs-lookup"><span data-stu-id="02662-117">If you clear the **is mapped** property of a surrogate foreign key (that is, if you set the property to **false**), the related data source are automatically removed and unmapped from the entity and any nested surrogate foreign key data sources.</span></span> <span data-ttu-id="02662-118">代理外部キー フィールドの **is mapped** プロパティを選択し、クリアした結果と **データ ソースの追加** および **Remove data source** ボタンを使用した結果は異なります。</span><span class="sxs-lookup"><span data-stu-id="02662-118">The effect of selecting and clearing the **is mapped** property of a surrogate foreign key field differs from the effect of using the **Add data source** and **Remove data source** buttons.</span></span> <span data-ttu-id="02662-119">代理外部キー データ ソースを追加すると、親データ ソースの代理外部キー フィールドの **is mapped** プロパティは自動的に **true** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="02662-119">If you add a surrogate foreign key data source, the **is mapped** property of the parent data source surrogate foreign key field isn't automatically set to **true**.</span></span> <span data-ttu-id="02662-120">代理外部キー データ ソースを削除すると、親データ ソースの代理外部キー フィールドの **is mapped** プロパティは自動的に **false** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="02662-120">If you are removing a surrogate foreign key data source, the **is mapped** property of the parent data source surrogate foreign key field isn't automatically set to **false**.</span></span> <span data-ttu-id="02662-121">既定では、ルート データ ソースの代理外部キーフィールドの**マップされている**プロパティは **true** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="02662-121">By default, the **is mapped** property of the root data source's surrogate foreign key field is set to **true**.</span></span> <span data-ttu-id="02662-122">したがって、規定では、代理外部キー関係は 1 つのレベルに拡張されます。</span><span class="sxs-lookup"><span data-stu-id="02662-122">Therefore, by default, surrogate foreign key relations are expanded to one level.</span></span>

## <a name="expansion-of-parentchild-relations"></a><span data-ttu-id="02662-123">親または子の関係の展開</span><span class="sxs-lookup"><span data-stu-id="02662-123">Expansion of parent/child relations</span></span>
<span data-ttu-id="02662-124">親/子の関係は、子テーブルでの関係として保存されている構成/拡張子関係です。</span><span class="sxs-lookup"><span data-stu-id="02662-124">Parent/child relations are composition/extension relations that are stored as a relation on the child table.</span></span> <span data-ttu-id="02662-125">親テーブルはリレーションを検出しません。</span><span class="sxs-lookup"><span data-stu-id="02662-125">The parent table doesn't detect the relation.</span></span> <span data-ttu-id="02662-126">親/子の関係は、代理外部キー関係またはナチュラル外部キーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="02662-126">A parent/child relation can be either a surrogate foreign key relation or a natural foreign key.</span></span> <span data-ttu-id="02662-127">親/子の関係は、次のルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="02662-127">Parent/child relations use the following rules:</span></span>

- <span data-ttu-id="02662-128">子テーブルのコレクションは、相互参照データベースに親テーブルへの「型参照」関係を照会することによって取得できます。</span><span class="sxs-lookup"><span data-stu-id="02662-128">The collection of child tables is obtained by querying the cross-reference database for "type reference" relations to the parent table.</span></span>
- <span data-ttu-id="02662-129">子テーブルは、親テーブルと同じテーブル グループに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="02662-129">The child table must belong to the same table group as the parent table.</span></span>
- <span data-ttu-id="02662-130">子と親**関係タイプ** プロパティは、**アソシエーション**、**合成**、**リンク**、**集約**のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="02662-130">The relation between the child and parent **relationship type** property must be **association**, **composition**, **link**, or **aggregation**.</span></span>
- <span data-ttu-id="02662-131">子と親 **基数**プロパティの間の関係は、**厳密に 1 つ**または **0 または 1** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="02662-131">The relation between the child and parent **cardinality** property must be **exactly one** or **zero or one**.</span></span>
- <span data-ttu-id="02662-132">子と親 **関連テーブル基数**プロパティの間の関係は、**厳密に 1 つ**または **0 または 1** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="02662-132">The relation between the child and parent **related table cardinality** property must be **exactly one** or **zero or one**.</span></span>

<span data-ttu-id="02662-133">既定では、親/子関係は展開されません。</span><span class="sxs-lookup"><span data-stu-id="02662-133">By default, parent/child relations aren't expanded.</span></span> <span data-ttu-id="02662-134">**データ ソースの追加** ボタンを使用して、それらを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02662-134">You must add them by using the **Add data source** button.</span></span> <span data-ttu-id="02662-135">Microsoft Visual Studio でプロジェクトの既定の動作を変更するには、**親/子の展開** オプションを **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="02662-135">To change the default behavior for a project in Microsoft Visual Studio, set the **Expand parent/child** option to **true**.</span></span>

### <a name="using-label-text-as-field-names"></a><span data-ttu-id="02662-136">ラベル テキストをフィールド名として使用</span><span class="sxs-lookup"><span data-stu-id="02662-136">Using label text as field names</span></span>

<span data-ttu-id="02662-137">次の規則により、オプションが選択されたときにフィールド名としてラベル テキストを使用することができます (**true**)。</span><span class="sxs-lookup"><span data-stu-id="02662-137">The following rules enable label text to be used as the field name when the option is selected (**true**):</span></span>

- <span data-ttu-id="02662-138">すべての空白はラベル テキストから削除されます。</span><span class="sxs-lookup"><span data-stu-id="02662-138">All whitespace is removed from the label text.</span></span>
- <span data-ttu-id="02662-139">ラベル テキストは 77 文字に切り捨てられ、一意の 3 桁の数値識別子 (000 〜 999) が追加されます。</span><span class="sxs-lookup"><span data-stu-id="02662-139">The label text is truncated to 77 characters, and then a unique three-digit numeric identifier (000 through 999) is added.</span></span>
- <span data-ttu-id="02662-140">ラベル テキストは、**NamedElement.IsValid** メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="02662-140">The label text is passed to the **NamedElement.IsValid** method.</span></span> <span data-ttu-id="02662-141">名前が有効である場合は、フィールド名として使用できます。</span><span class="sxs-lookup"><span data-stu-id="02662-141">If the name is valid, it can be used as the field name.</span></span> <span data-ttu-id="02662-142">そうしないと、ラベル テキストは使用されず、フィールド名前が変更されません。</span><span class="sxs-lookup"><span data-stu-id="02662-142">Otherwise, the label text isn't used, and the field name remains unchanged.</span></span>

### <a name="the-is-mandatory-field"></a><span data-ttu-id="02662-143">Is 必須項目</span><span class="sxs-lookup"><span data-stu-id="02662-143">The Is mandatory field</span></span>

<span data-ttu-id="02662-144">データ エンティティ フィールドの既定値は **自動** です。この値は明示的に変更されない限り使用されます。</span><span class="sxs-lookup"><span data-stu-id="02662-144">The default value of data entity fields is **auto**. This value is used unless it's explicitly changed.</span></span> <span data-ttu-id="02662-145">関係については、関連するフィールドの**必須**プロパティは、フィールドの**必須**値の値に基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="02662-145">For relations, the related field's **Is mandatory** property is set based on the value of the field's **Is mandatory** value.</span></span>

- <span data-ttu-id="02662-146">フィールドの**必須**プロパティと関連するフィールドの**必須**プロパティが両方とも **true** である場合は、両方のフィールドが **true** に明示的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="02662-146">If the field's **Is mandatory** property and the related field's **Is mandatory** are both **true**, both fields are explicitly set to **true**.</span></span>
- <span data-ttu-id="02662-147">フィールドの**必須**プロパティと関連するフィールドの**必須**プロパティが両方とも **false** である場合は、両方のフィールドが **false** に明示的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="02662-147">If the field's **Is mandatory** property and the related field's **Is mandatory** are both **false**, both fields are explicitly set to **false**.</span></span>

<span data-ttu-id="02662-148">フィールドの**必須**プロパティと関連するフィールドの**必須**プロパティの値が異なる場合は、両方のフィールドは変わりません。</span><span class="sxs-lookup"><span data-stu-id="02662-148">If the field's **Is mandatory** property and the related field's **Is mandatory** property differ in value, both fields remain unchanged.</span></span> <span data-ttu-id="02662-149">この場合、**自動**の既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="02662-149">In this case, the default value of **auto** is used.</span></span>
