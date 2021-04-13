---
title: 水平フィールドおよびボタン グループのサブパターン
description: この記事では、個々のフィールドにアクションを定義する必要があるときに使用される、水平フィールドおよびボタン グループのサブパターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 12464
ms.assetid: 56b16f26-d4d3-4052-9ebc-0878b09cc00d
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0f79add42ef4a5183770b1edbb7f24d8035a48d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749237"
---
# <a name="horizontal-fields-and-buttons-group-subpattern"></a><span data-ttu-id="eb89a-103">水平フィールドおよびボタン グループのサブパターン</span><span class="sxs-lookup"><span data-stu-id="eb89a-103">Horizontal Fields and Buttons Group subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb89a-104">この記事では、水平フィールドおよびボタン グループ フォームのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="eb89a-104">This article provides information about the Horizontal Fields and Buttons Group form subpattern.</span></span> <span data-ttu-id="eb89a-105">このサブパターンは、フォーム上の個々のフィールドのアクションを定義する必要があるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb89a-105">This subpattern is used when actions must be defined for an individual field on a form.</span></span>

<a name="usage"></a><span data-ttu-id="eb89a-106">用途</span><span class="sxs-lookup"><span data-stu-id="eb89a-106">Usage</span></span>
-----

<span data-ttu-id="eb89a-107">このサブパターンは、フォーム上の個々のフィールドのアクションを定義する必要があるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb89a-107">This subpattern is used when actions must be defined for an individual field on a form.</span></span> <span data-ttu-id="eb89a-108">これらのボタンはフィールドの右側に配置され、アクションをフィールドと視覚的に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="eb89a-108">The buttons are laid out just to the right of the field to visually associate the actions with the field.</span></span> <span data-ttu-id="eb89a-109">ボタンには、アイコンのみ (テキストなし) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb89a-109">The buttons should display only an icon (no text).</span></span> <span data-ttu-id="eb89a-110">セクションまたはフォーム全体に関連付けられているアクションは、そのセクションまたはフォーム上にあるツールバーまたは ActionPane に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb89a-110">Actions that are associated with a section or an entire form should be placed in a Toolbar or ActionPane above that section or form.</span></span>

### <a name="typical-contents"></a><span data-ttu-id="eb89a-111">標準的な内容</span><span class="sxs-lookup"><span data-stu-id="eb89a-111">Typical contents</span></span>

-   <span data-ttu-id="eb89a-112">1-2 フィールド</span><span class="sxs-lookup"><span data-stu-id="eb89a-112">1–2 fields</span></span>
-   <span data-ttu-id="eb89a-113">1-3 ボタン</span><span class="sxs-lookup"><span data-stu-id="eb89a-113">1–3 buttons</span></span>

## <a name="wireframe"></a><span data-ttu-id="eb89a-114">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="eb89a-114">Wireframe</span></span>
<span data-ttu-id="eb89a-115">[![水平フィールドとボタン グループ フォーム サブパターンのワイヤーフレーム](./media/horizontalfieldsbuttons1.png)](./media/horizontalfieldsbuttons1.png)</span><span class="sxs-lookup"><span data-stu-id="eb89a-115">[![Wireframe for Horizontal Fields and Buttons Group form subpattern](./media/horizontalfieldsbuttons1.png)](./media/horizontalfieldsbuttons1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="eb89a-116">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="eb89a-116">Pattern changes</span></span>
<span data-ttu-id="eb89a-117">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="eb89a-117">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="eb89a-118">フィールドとボタンのレイアウトには、**ArrangeMethod**=**HorizontalLeft** という単一の列が使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb89a-118">The layout of fields and buttons will use a single column, where **ArrangeMethod**=**HorizontalLeft**.</span></span>

## <a name="model"></a><span data-ttu-id="eb89a-119">モデル</span><span class="sxs-lookup"><span data-stu-id="eb89a-119">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="eb89a-120">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="eb89a-120">High-level structure</span></span>

- <span data-ttu-id="eb89a-121">グループ (ArrangeMethod=HorizontalLeft)</span><span class="sxs-lookup"><span data-stu-id="eb89a-121">Group (ArrangeMethod=HorizontalLeft)</span></span>

    - <span data-ttu-id="eb89a-122">フィールド</span><span class="sxs-lookup"><span data-stu-id="eb89a-122">Field</span></span>
    - <span data-ttu-id="eb89a-123">*フィールド (オプション)*</span><span class="sxs-lookup"><span data-stu-id="eb89a-123">*Field (optional)*</span></span>
    - <span data-ttu-id="eb89a-124">ボタン (1-3 ボタン)</span><span class="sxs-lookup"><span data-stu-id="eb89a-124">Buttons (1–3 buttons)</span></span>

### <a name="core-components"></a><span data-ttu-id="eb89a-125">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="eb89a-125">Core components</span></span>

-   <span data-ttu-id="eb89a-126">HorizontalFieldsButtonsGroup サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="eb89a-126">Apply the HorizontalFieldsButtonsGroup subpattern to the container control.</span></span>
-   <span data-ttu-id="eb89a-127">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="eb89a-127">Address BP Warnings:</span></span>
    -   <span data-ttu-id="eb89a-128">ボタンは 3 つ以下にしてください。</span><span class="sxs-lookup"><span data-stu-id="eb89a-128">There should be no more than three buttons.</span></span>
    -   <span data-ttu-id="eb89a-129">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="eb89a-129">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="eb89a-130">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="eb89a-130">Related patterns</span></span>

-   [<span data-ttu-id="eb89a-131">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="eb89a-131">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   <span data-ttu-id="eb89a-132">水平フィールド</span><span class="sxs-lookup"><span data-stu-id="eb89a-132">Horizontal Fields</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="eb89a-133">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="eb89a-133">UX guidelines</span></span>
<span data-ttu-id="eb89a-134">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="eb89a-134">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="eb89a-135">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="eb89a-135">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="eb89a-136">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="eb89a-136">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="eb89a-137">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="eb89a-137">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="eb89a-138">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="eb89a-138">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="eb89a-139">**水平フィールドおよびボタン グループのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="eb89a-139">**Horizontal Fields and Buttons Group guidelines:**</span></span>
    -   <span data-ttu-id="eb89a-140">フィールド + ボタンの幅は、列の標準サイズを超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="eb89a-140">The width of the fields + buttons should not exceed the standard size of a column.</span></span>
    -   <span data-ttu-id="eb89a-141">ボタンにはシンボル イメージが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb89a-141">Buttons should have a symbol image assigned.</span></span>
    -   <span data-ttu-id="eb89a-142">ボタンにはツールヒントが必要です。</span><span class="sxs-lookup"><span data-stu-id="eb89a-142">Buttons should have tooltips.</span></span>
    -   <span data-ttu-id="eb89a-143">最大 3 つのボタンが必要です。</span><span class="sxs-lookup"><span data-stu-id="eb89a-143">There should be a maximum of three buttons.</span></span> <span data-ttu-id="eb89a-144">最後のボタンはメニュー ボタンです。</span><span class="sxs-lookup"><span data-stu-id="eb89a-144">The last button can be a menu button.</span></span>

## <a name="examples"></a><span data-ttu-id="eb89a-145">例</span><span class="sxs-lookup"><span data-stu-id="eb89a-145">Examples</span></span>
<span data-ttu-id="eb89a-146">フォーム: **SalesTable (GroupHeaderAddressHeaderOverview)**</span><span class="sxs-lookup"><span data-stu-id="eb89a-146">Form: **SalesTable (GroupHeaderAddressHeaderOverview)**</span></span> 

<span data-ttu-id="eb89a-147">[![フォーム例](./media/horizontalfieldsbuttons2.png)](./media/horizontalfieldsbuttons2.png)</span><span class="sxs-lookup"><span data-stu-id="eb89a-147">[![Example of form](./media/horizontalfieldsbuttons2.png)](./media/horizontalfieldsbuttons2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="eb89a-148">リソース</span><span class="sxs-lookup"><span data-stu-id="eb89a-148">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="eb89a-149">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="eb89a-149">Typically used by patterns</span></span>

-   [<span data-ttu-id="eb89a-150">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="eb89a-150">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="eb89a-151">目次</span><span class="sxs-lookup"><span data-stu-id="eb89a-151">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="eb89a-152">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="eb89a-152">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="eb89a-153">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="eb89a-153">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="eb89a-154">付録</span><span class="sxs-lookup"><span data-stu-id="eb89a-154">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="eb89a-155">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="eb89a-155">Frequently asked questions</span></span>

<span data-ttu-id="eb89a-156">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="eb89a-156">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="eb89a-157">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="eb89a-157">Open issues</span></span>

-   <span data-ttu-id="eb89a-158">なし</span><span class="sxs-lookup"><span data-stu-id="eb89a-158">None</span></span>

### <a name="dynamics-ax-2012-content"></a><span data-ttu-id="eb89a-159">Dynamics AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="eb89a-159">Dynamics AX 2012 content</span></span>
<span data-ttu-id="eb89a-160">**SalesTable**</span><span class="sxs-lookup"><span data-stu-id="eb89a-160">**SalesTable**</span></span> 

<span data-ttu-id="eb89a-161">[![フォーム例](./media/horizontalfieldsbuttons3.png)](./media/horizontalfieldsbuttons3.png)</span><span class="sxs-lookup"><span data-stu-id="eb89a-161">[![Example of form](./media/horizontalfieldsbuttons3.png)](./media/horizontalfieldsbuttons3.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]