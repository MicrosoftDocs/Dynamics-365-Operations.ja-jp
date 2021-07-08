---
title: フィールドおよびフィールド グループのサブパターン
description: このトピックでは、フィールドおよびフィールド グループ フォームのサブパターンについて説明します。
author: jasongre
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 12384
ms.assetid: f3bf8d00-8e6d-4af7-ab7e-3ff47fce9e21
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d47b613f97d3f1b43649bc580ce4c08e6d2fefd5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189322"
---
# <a name="fields-and-field-groups-subpattern"></a><span data-ttu-id="153c4-103">フィールドおよびフィールド グループのサブパターン</span><span class="sxs-lookup"><span data-stu-id="153c4-103">Fields and Field Groups subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="153c4-104">このトピックでは、フィールドおよびフィールド グループ フォームのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="153c4-104">This topic provides information about the Field and Field Groups form subpattern.</span></span> <span data-ttu-id="153c4-105">これは、最も一般的なデータ入力サブパターンです。</span><span class="sxs-lookup"><span data-stu-id="153c4-105">This is the most common data entry subpattern.</span></span> <span data-ttu-id="153c4-106">複数のフィールドまたはフィールドのグループを表示するのに動的な数の列を使用します。</span><span class="sxs-lookup"><span data-stu-id="153c4-106">It uses a dynamic number of columns to present multiple fields or groups of fields.</span></span>

## <a name="usage"></a><span data-ttu-id="153c4-107">用途</span><span class="sxs-lookup"><span data-stu-id="153c4-107">Usage</span></span>

<span data-ttu-id="153c4-108">フィールドおよびフィールド グループは最も一般的なデータ入力サブパターンであり、複数のフィールドまたはフィールドのグループを表示する動的列の数を使用します。</span><span class="sxs-lookup"><span data-stu-id="153c4-108">Field and Field Groups is the most common data entry subpattern and uses a dynamic number of columns to present multiple fields or groups of fields.</span></span> <span data-ttu-id="153c4-109">このサブパターンは、動的な高さや幅を持つコントロール (グリッド、ツリー、ラジオボタン、リストボックス、リストビューなどの)、または高さや幅の大きいコントロール (Chart など) では使用されません。</span><span class="sxs-lookup"><span data-stu-id="153c4-109">This subpattern is not used with controls that have dynamic height or width (for example Grid, Tree, RadioButton, ListBox, or ListView), or controls that have larger height or width (for example, Chart).</span></span> <span data-ttu-id="153c4-110">このパターン内のグループ コントロールを使用して、ラベルの下のフィールドをグループ化するか、テーブル フィールド グループにバインドすることができます。</span><span class="sxs-lookup"><span data-stu-id="153c4-110">The group controls within this pattern can be used either to group fields under a label or to bind to a table field group.</span></span>

### <a name="typical-contents"></a><span data-ttu-id="153c4-111">標準的な内容</span><span class="sxs-lookup"><span data-stu-id="153c4-111">Typical contents</span></span>

-   <span data-ttu-id="153c4-112">クイック タブの直接の子としてのグループまたはフィールド</span><span class="sxs-lookup"><span data-stu-id="153c4-112">Groups or Fields as immediate children of the FastTab</span></span>
-   <span data-ttu-id="153c4-113">フィールドを含むグループ</span><span class="sxs-lookup"><span data-stu-id="153c4-113">Groups containing Fields</span></span>
-   <span data-ttu-id="153c4-114">他のサブパターンを含めることができます:</span><span class="sxs-lookup"><span data-stu-id="153c4-114">Can contain other subpatterns:</span></span>
    -   <span data-ttu-id="153c4-115">水平フィールドおよびボタン グループ</span><span class="sxs-lookup"><span data-stu-id="153c4-115">Horizontal fields and button group</span></span>

## <a name="wireframe"></a><span data-ttu-id="153c4-116">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="153c4-116">Wireframe</span></span>
<span data-ttu-id="153c4-117">[![フィールドとフィールド グループのワイヤフレーム](./media/fieldsfieldgroups1.png)](./media/fieldsfieldgroups1.png)</span><span class="sxs-lookup"><span data-stu-id="153c4-117">[![Wireframe for Field and Field Groups](./media/fieldsfieldgroups1.png)](./media/fieldsfieldgroups1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="153c4-118">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="153c4-118">Pattern changes</span></span>
<span data-ttu-id="153c4-119">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="153c4-119">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="153c4-120">フィールドを 2 つ以上の列に強制するため、明示的な列とグループの使用を削除しました。</span><span class="sxs-lookup"><span data-stu-id="153c4-120">Removed explicit columns and the use of groups to force fields into two or three (or more) columns.</span></span>
-   <span data-ttu-id="153c4-121">固定列から動的列に変更されました。</span><span class="sxs-lookup"><span data-stu-id="153c4-121">Changed from fixed columns to dynamic columns.</span></span>

## <a name="model"></a><span data-ttu-id="153c4-122">モデル</span><span class="sxs-lookup"><span data-stu-id="153c4-122">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="153c4-123">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="153c4-123">High-level structure</span></span>

- <span data-ttu-id="153c4-124">\[コンテナー\] (列 = 入力)</span><span class="sxs-lookup"><span data-stu-id="153c4-124">\[Container\] (Columns=Fill)</span></span>

    - <span data-ttu-id="153c4-125">*フィールド グループ (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="153c4-125">*FieldGroups (Group) \[0..N\]*</span></span>

        - <span data-ttu-id="153c4-126">フィールド ($Field) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="153c4-126">Fields ($Field) \[1..N\]</span></span>
        - <span data-ttu-id="153c4-127">*ActionableFields (グループ)\[0..N\]* 水平フィールドとボタン グループ サブパターンを模倣します</span><span class="sxs-lookup"><span data-stu-id="153c4-127">*ActionableFields (Group) \[0..N\]* mimics the Horizontal Fields and Button Group subpattern</span></span>

    - <span data-ttu-id="153c4-128">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="153c4-128">*Fields ($Field) \[0..N\]*</span></span>
    - <span data-ttu-id="153c4-129">*ActionableFields (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="153c4-129">*ActionableFields (Group) \[0..N\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="153c4-130">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="153c4-130">Core components</span></span>

-   <span data-ttu-id="153c4-131">FieldsAndFieldGroups サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="153c4-131">Apply the FieldsAndFieldGroups subpattern to the container control.</span></span>
-   <span data-ttu-id="153c4-132">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="153c4-132">Address BP Warnings:</span></span>
    -   <span data-ttu-id="153c4-133">繰り越されたチェックである AX6.3 BP 以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="153c4-133">No additional BP checks are required beyond the AX6.3 BP that were checks carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="153c4-134">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="153c4-134">Related patterns</span></span>

-   [<span data-ttu-id="153c4-135">水平フィールドおよびボタン グループ</span><span class="sxs-lookup"><span data-stu-id="153c4-135">Horizontal Fields and Buttons Group</span></span>](horizontal-fields-buttons-group-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="153c4-136">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="153c4-136">UX guidelines</span></span>
<span data-ttu-id="153c4-137">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="153c4-137">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="153c4-138">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="153c4-138">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="153c4-139">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="153c4-139">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="153c4-140">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="153c4-140">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="153c4-141">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="153c4-141">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="153c4-142">**フィールドおよびフィールド グループのガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="153c4-142">**Fields and Field Groups guidelines:**</span></span>
    -   <span data-ttu-id="153c4-143">グループ内のフィールドは、ページ全体を越えて移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="153c4-143">The fields in groups should flow across the entire page.</span></span> <span data-ttu-id="153c4-144">[![ページ間を通過するグループのフィールド例](./media/fieldsfieldgroups2.png)](./media/fieldsfieldgroups2.png)</span><span class="sxs-lookup"><span data-stu-id="153c4-144">[![Example of fields in groups flowing across page](./media/fieldsfieldgroups2.png)](./media/fieldsfieldgroups2.png)</span></span>
    -   <span data-ttu-id="153c4-145">可能な場合は、不要なフィールド グループのラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="153c4-145">When possible, remove unnecessary field group labels.</span></span>
    -   <span data-ttu-id="153c4-146">フィールドが分かりやすくグループ分けされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="153c4-146">Verify that you have an understandable grouping for your fields.</span></span>
    -   <span data-ttu-id="153c4-147">すべてのフィールドがラベルを持つグループにあるか、またはグループ ラベルを表示しないかです。</span><span class="sxs-lookup"><span data-stu-id="153c4-147">Either all fields should be in Groups that have labels, or no Group labels should be shown.</span></span>

## <a name="examples"></a><span data-ttu-id="153c4-148">例</span><span class="sxs-lookup"><span data-stu-id="153c4-148">Examples</span></span>
<span data-ttu-id="153c4-149">フォーム: **InventLocation (LocationNames)** [![フォーム例](./media/fieldsfieldgroups3.png)](./media/fieldsfieldgroups3.png)</span><span class="sxs-lookup"><span data-stu-id="153c4-149">Form: **InventLocation (LocationNames)** [![Example of form](./media/fieldsfieldgroups3.png)](./media/fieldsfieldgroups3.png)</span></span>

## <a name="resources"></a><span data-ttu-id="153c4-150">リソース</span><span class="sxs-lookup"><span data-stu-id="153c4-150">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="153c4-151">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="153c4-151">Typically used by patterns</span></span>

-   [<span data-ttu-id="153c4-152">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="153c4-152">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="153c4-153">目次</span><span class="sxs-lookup"><span data-stu-id="153c4-153">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="153c4-154">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="153c4-154">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="153c4-155">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="153c4-155">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="153c4-156">付録</span><span class="sxs-lookup"><span data-stu-id="153c4-156">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="153c4-157">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="153c4-157">Frequently asked questions</span></span>

<span data-ttu-id="153c4-158">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="153c4-158">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="153c4-159">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="153c4-159">Open issues</span></span>

-   <span data-ttu-id="153c4-160">ツールでは、パターン定義のコンテンツを模倣する代わりに、HorizontalFieldsButtonsGroup サブパターンを明示的に使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="153c4-160">Tooling must allow explicit use of the HorizontalFieldsButtonsGroup subpattern instead of mimicking content in the pattern definition.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="153c4-161">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="153c4-161">AX 2012 content</span></span>

<span data-ttu-id="153c4-162">**InventLocation**[![フォーム例](./media/fieldsfieldgroups4.png)](./media/fieldsfieldgroups4.png)</span><span class="sxs-lookup"><span data-stu-id="153c4-162">**InventLocation** [![Example of form](./media/fieldsfieldgroups4.png)](./media/fieldsfieldgroups4.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]