---
title: 水平フィールドおよびボタン グループのサブパターン
description: この記事では、水平フィールドおよびボタン グループ フォームのサブパターンに関する情報を提供します。 このサブパターンは、フォーム上の個々のフィールドのアクションを定義する必要があるときに使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 12464
ms.assetid: 56b16f26-d4d3-4052-9ebc-0878b09cc00d
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60be0e67f88ec5523b62f0a5f667695f409038f7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560055"
---
# <a name="horizontal-fields-and-buttons-group-subpattern"></a><span data-ttu-id="d13c1-104">水平フィールドおよびボタン グループのサブパターン</span><span class="sxs-lookup"><span data-stu-id="d13c1-104">Horizontal Fields and Buttons Group subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d13c1-105">この記事では、水平フィールドおよびボタン グループ フォームのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d13c1-105">This article provides information about the Horizontal Fields and Buttons Group form subpattern.</span></span> <span data-ttu-id="d13c1-106">このサブパターンは、フォーム上の個々のフィールドのアクションを定義する必要があるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d13c1-106">This subpattern is used when actions must be defined for an individual field on a form.</span></span>

<a name="usage"></a><span data-ttu-id="d13c1-107">用途</span><span class="sxs-lookup"><span data-stu-id="d13c1-107">Usage</span></span>
-----

<span data-ttu-id="d13c1-108">このサブパターンは、フォーム上の個々のフィールドのアクションを定義する必要があるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d13c1-108">This subpattern is used when actions must be defined for an individual field on a form.</span></span> <span data-ttu-id="d13c1-109">これらのボタンはフィールドの右側に配置され、アクションをフィールドと視覚的に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="d13c1-109">The buttons are laid out just to the right of the field to visually associate the actions with the field.</span></span> <span data-ttu-id="d13c1-110">ボタンには、アイコンのみ (テキストなし) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d13c1-110">The buttons should display only an icon (no text).</span></span> <span data-ttu-id="d13c1-111">セクションまたはフォーム全体に関連付けられているアクションは、そのセクションまたはフォーム上にあるツールバーまたは ActionPane に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c1-111">Actions that are associated with a section or an entire form should be placed in a Toolbar or ActionPane above that section or form.</span></span>

### <a name="typical-contents"></a><span data-ttu-id="d13c1-112">標準的な内容</span><span class="sxs-lookup"><span data-stu-id="d13c1-112">Typical contents</span></span>

-   <span data-ttu-id="d13c1-113">1-2 フィールド</span><span class="sxs-lookup"><span data-stu-id="d13c1-113">1–2 fields</span></span>
-   <span data-ttu-id="d13c1-114">1-3 ボタン</span><span class="sxs-lookup"><span data-stu-id="d13c1-114">1–3 buttons</span></span>

## <a name="wireframe"></a><span data-ttu-id="d13c1-115">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="d13c1-115">Wireframe</span></span>
<span data-ttu-id="d13c1-116">[![HorizontalFieldsButtons(1)](./media/horizontalfieldsbuttons1.png)](./media/horizontalfieldsbuttons1.png)</span><span class="sxs-lookup"><span data-stu-id="d13c1-116">[![HorizontalFieldsButtons(1)](./media/horizontalfieldsbuttons1.png)](./media/horizontalfieldsbuttons1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="d13c1-117">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="d13c1-117">Pattern changes</span></span>
<span data-ttu-id="d13c1-118">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d13c1-118">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="d13c1-119">フィールドとボタンのレイアウトには、**ArrangeMethod**=**HorizontalLeft** という単一の列が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d13c1-119">The layout of fields and buttons will use a single column, where **ArrangeMethod**=**HorizontalLeft**.</span></span>

## <a name="model"></a><span data-ttu-id="d13c1-120">モデル</span><span class="sxs-lookup"><span data-stu-id="d13c1-120">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="d13c1-121">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="d13c1-121">High-level structure</span></span>

- <span data-ttu-id="d13c1-122">グループ (ArrangeMethod=HorizontalLeft)</span><span class="sxs-lookup"><span data-stu-id="d13c1-122">Group (ArrangeMethod=HorizontalLeft)</span></span>

    - <span data-ttu-id="d13c1-123">フィールド</span><span class="sxs-lookup"><span data-stu-id="d13c1-123">Field</span></span>
    - <span data-ttu-id="d13c1-124">*フィールド (オプション)*</span><span class="sxs-lookup"><span data-stu-id="d13c1-124">*Field (optional)*</span></span>
    - <span data-ttu-id="d13c1-125">ボタン (1-3 ボタン)</span><span class="sxs-lookup"><span data-stu-id="d13c1-125">Buttons (1–3 buttons)</span></span>

### <a name="core-components"></a><span data-ttu-id="d13c1-126">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d13c1-126">Core components</span></span>

-   <span data-ttu-id="d13c1-127">HorizontalFieldsButtonsGroup サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="d13c1-127">Apply the HorizontalFieldsButtonsGroup subpattern to the container control.</span></span>
-   <span data-ttu-id="d13c1-128">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="d13c1-128">Address BP Warnings:</span></span>
    -   <span data-ttu-id="d13c1-129">ボタンは 3 つ以下にしてください。</span><span class="sxs-lookup"><span data-stu-id="d13c1-129">There should be no more than three buttons.</span></span>
    -   <span data-ttu-id="d13c1-130">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="d13c1-130">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="d13c1-131">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="d13c1-131">Related patterns</span></span>

-   [<span data-ttu-id="d13c1-132">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="d13c1-132">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   <span data-ttu-id="d13c1-133">水平フィールド</span><span class="sxs-lookup"><span data-stu-id="d13c1-133">Horizontal Fields</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="d13c1-134">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="d13c1-134">UX guidelines</span></span>
<span data-ttu-id="d13c1-135">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="d13c1-135">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="d13c1-136">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d13c1-136">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="d13c1-137">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="d13c1-137">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="d13c1-138">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="d13c1-138">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="d13c1-139">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="d13c1-139">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="d13c1-140">**水平フィールドおよびボタン グループのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="d13c1-140">**Horizontal Fields and Buttons Group guidelines:**</span></span>
    -   <span data-ttu-id="d13c1-141">フィールド + ボタンの幅は、列の標準サイズを超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="d13c1-141">The width of the fields + buttons should not exceed the standard size of a column.</span></span>
    -   <span data-ttu-id="d13c1-142">ボタンにはシンボル イメージが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c1-142">Buttons should have a symbol image assigned.</span></span>
    -   <span data-ttu-id="d13c1-143">ボタンにはツールヒントが必要です。</span><span class="sxs-lookup"><span data-stu-id="d13c1-143">Buttons should have tooltips.</span></span>
    -   <span data-ttu-id="d13c1-144">最大 3 つのボタンが必要です。</span><span class="sxs-lookup"><span data-stu-id="d13c1-144">There should be a maximum of three buttons.</span></span> <span data-ttu-id="d13c1-145">最後のボタンはメニュー ボタンです。</span><span class="sxs-lookup"><span data-stu-id="d13c1-145">The last button can be a menu button.</span></span>

## <a name="examples"></a><span data-ttu-id="d13c1-146">例</span><span class="sxs-lookup"><span data-stu-id="d13c1-146">Examples</span></span>
<span data-ttu-id="d13c1-147">フォーム: **SalesTable (GroupHeaderAddressHeaderOverview)** [![HorizontalFieldsButtons(2)](./media/horizontalfieldsbuttons2.png)](./media/horizontalfieldsbuttons2.png)</span><span class="sxs-lookup"><span data-stu-id="d13c1-147">Form: **SalesTable (GroupHeaderAddressHeaderOverview)** [![HorizontalFieldsButtons(2)](./media/horizontalfieldsbuttons2.png)](./media/horizontalfieldsbuttons2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="d13c1-148">リソース</span><span class="sxs-lookup"><span data-stu-id="d13c1-148">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="d13c1-149">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="d13c1-149">Typically used by patterns</span></span>

-   [<span data-ttu-id="d13c1-150">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="d13c1-150">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="d13c1-151">目次</span><span class="sxs-lookup"><span data-stu-id="d13c1-151">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="d13c1-152">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="d13c1-152">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="d13c1-153">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="d13c1-153">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="d13c1-154">付録</span><span class="sxs-lookup"><span data-stu-id="d13c1-154">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="d13c1-155">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d13c1-155">Frequently asked questions</span></span>

<span data-ttu-id="d13c1-156">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="d13c1-156">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="d13c1-157">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="d13c1-157">Open issues</span></span>

-   <span data-ttu-id="d13c1-158">なし</span><span class="sxs-lookup"><span data-stu-id="d13c1-158">None</span></span>

### <a name="dynamics-ax-2012-content"></a><span data-ttu-id="d13c1-159">Dynamics AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="d13c1-159">Dynamics AX 2012 content</span></span>

<span data-ttu-id="d13c1-160">**SalesTable** [![HorizontalFieldsButtons(3)](./media/horizontalfieldsbuttons3.png)](./media/horizontalfieldsbuttons3.png)</span><span class="sxs-lookup"><span data-stu-id="d13c1-160">**SalesTable** [![HorizontalFieldsButtons(3)](./media/horizontalfieldsbuttons3.png)](./media/horizontalfieldsbuttons3.png)</span></span>
