---
title: ツールバーおよびリストのサブパターン
description: この記事では、ツールバーとリストのフォームのサブパターンについて説明します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 15931
ms.assetid: a60f829b-e496-453b-9e58-f7cb4d67114f
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c002e37d3c008ac6cbdd6f591308d7ed31efc93b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189734"
---
# <a name="toolbar-and-list-subpattern"></a><span data-ttu-id="cda0c-103">ツールバーおよびリストのサブパターン</span><span class="sxs-lookup"><span data-stu-id="cda0c-103">Toolbar and List subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cda0c-104">この記事では、ツールバーとリストのフォームのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cda0c-104">This article provides information about the Toolbar and List form subpattern.</span></span> <span data-ttu-id="cda0c-105">このサブパターンは、親エンティティの子コレクションを表形式グリッドまたはツリーのいずれかとして表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0c-105">This subpattern is used to show child collections for the parent entity as either a tabular grid or a tree.</span></span> 

## <a name="usage"></a><span data-ttu-id="cda0c-106">用途</span><span class="sxs-lookup"><span data-stu-id="cda0c-106">Usage</span></span>

<span data-ttu-id="cda0c-107">このサブパターンは、親エンティティの子コレクションを表形式グリッドまたはツリーのいずれかとして表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0c-107">This subpattern is used to show child collections for the parent entity as either a tabular grid or a tree.</span></span> <span data-ttu-id="cda0c-108">ツールバーに含まれるアクションは 10 個未満です。</span><span class="sxs-lookup"><span data-stu-id="cda0c-108">The toolbar contains fewer than 10 actions.</span></span> <span data-ttu-id="cda0c-109">グリッドを使用している場合は、10 未満のフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cda0c-109">If a grid is used, it contains fewer than 10 fields.</span></span> <span data-ttu-id="cda0c-110">この記事では、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cda0c-110">This article describes two patterns:</span></span>

-   <span data-ttu-id="cda0c-111">**ツールバーおよびリスト** – これはパターンの基本的なバージョンであり、既定で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cda0c-111">**Toolbar and list** – This is the basic version of the pattern and should be used by default.</span></span>
-   <span data-ttu-id="cda0c-112">**ツールバーおよびリスト (二重)** – このバリアントには、2 つのリストおよび各リストの上のオプションのツールバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cda0c-112">**Toolbar and list (double)** – This variant includes two lists and an optional toolbar above each list.</span></span>

## <a name="wireframes"></a><span data-ttu-id="cda0c-113">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="cda0c-113">Wireframes</span></span>
### <a name="toolbar-and-list"></a><span data-ttu-id="cda0c-114">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="cda0c-114">Toolbar and list</span></span>

<span data-ttu-id="cda0c-115">[![ツールバーとリストのフォームのワイヤーフレーム](./media/toolbarlist1.png)](./media/toolbarlist1.png)</span><span class="sxs-lookup"><span data-stu-id="cda0c-115">[![Wireframe for Toolbar and List form](./media/toolbarlist1.png)](./media/toolbarlist1.png)</span></span>

### <a name="toolbar-and-list-double"></a><span data-ttu-id="cda0c-116">ツールバーおよびリスト (ダブル)</span><span class="sxs-lookup"><span data-stu-id="cda0c-116">Toolbar and list (double)</span></span>

<span data-ttu-id="cda0c-117">[![ツールバーとリスト (ダブル) のフォームのワイヤーフレーム](./media/toolbarlist2.png)](./media/toolbarlist2.png)</span><span class="sxs-lookup"><span data-stu-id="cda0c-117">[![Wireframe for Toolbar and List (double) form](./media/toolbarlist2.png)](./media/toolbarlist2.png)</span></span>

## <a name="model"></a><span data-ttu-id="cda0c-118">モデル</span><span class="sxs-lookup"><span data-stu-id="cda0c-118">Model</span></span>
### <a name="toolbar-and-list--high-level-structure"></a><span data-ttu-id="cda0c-119">ツールバーおよびリスト - 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="cda0c-119">Toolbar and list – High-level structure</span></span>

- <span data-ttu-id="cda0c-120">\[コンテナー\]</span><span class="sxs-lookup"><span data-stu-id="cda0c-120">\[Container\]</span></span>

    - <span data-ttu-id="cda0c-121">*ツールバー (ActionPane、スタイル = ストリップ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-121">*Toolbar (ActionPane, Style=Strip) \[Optional\]*</span></span>
    - <span data-ttu-id="cda0c-122">*CustomFilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-122">*CustomFilterGroup (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="cda0c-123">グリッド | ツリー | ListView | テーブル</span><span class="sxs-lookup"><span data-stu-id="cda0c-123">Grid | Tree | ListView | Table</span></span>
    - <span data-ttu-id="cda0c-124">*フッター (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-124">*Footer (Group) \[Optional\]*</span></span>

### <a name="toolbar-and-list-double--high-level-structure"></a><span data-ttu-id="cda0c-125">ツールバーおよびリスト (ダブル) - 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="cda0c-125">Toolbar and list (double) – High-level structure</span></span>

- <span data-ttu-id="cda0c-126">\[コンテナ\]</span><span class="sxs-lookup"><span data-stu-id="cda0c-126">\[Container\]</span></span>

    - <span data-ttu-id="cda0c-127">*ツールバー1 (ActionPane、スタイル = ストリップ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-127">*Toolbar1 (ActionPane, Style=Strip) \[Optional\]*</span></span>
    - <span data-ttu-id="cda0c-128">*CustomFilterGroup1 (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-128">*CustomFilterGroup1 (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="cda0c-129">グリッド | ツリー | ListView | テーブル</span><span class="sxs-lookup"><span data-stu-id="cda0c-129">Grid | Tree | ListView | Table</span></span>
    - <span data-ttu-id="cda0c-130">*ツールバー2 (ActionPane、スタイル = ストリップ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-130">*Toolbar2 (ActionPane, Style=Strip) \[Optional\]*</span></span>
    - <span data-ttu-id="cda0c-131">*CustomFilterGroup2 (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-131">*CustomFilterGroup2 (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="cda0c-132">グリッド | ツリー | ListView | テーブル</span><span class="sxs-lookup"><span data-stu-id="cda0c-132">Grid | Tree | ListView | Table</span></span>
    - <span data-ttu-id="cda0c-133">*フッター (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="cda0c-133">*Footer (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="cda0c-134">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cda0c-134">Core components</span></span>

-   <span data-ttu-id="cda0c-135">ToolbarList サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="cda0c-135">Apply the ToolbarList subpattern to a container control.</span></span>
-   <span data-ttu-id="cda0c-136">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="cda0c-136">Address BP Warnings:</span></span>
    -   <span data-ttu-id="cda0c-137">**Grid.DataSource** を空にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cda0c-137">**Grid.DataSource** must not be empty.</span></span>
    -   <span data-ttu-id="cda0c-138">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="cda0c-138">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="cda0c-139">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="cda0c-139">Related patterns</span></span>

-   [<span data-ttu-id="cda0c-140">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="cda0c-140">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="cda0c-141">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="cda0c-141">UX guidelines</span></span>
<span data-ttu-id="cda0c-142">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="cda0c-142">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="cda0c-143">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="cda0c-143">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="cda0c-144">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="cda0c-144">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="cda0c-145">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="cda0c-145">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="cda0c-146">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="cda0c-146">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="cda0c-147">**ツールバー** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="cda0c-147">**Toolbar** **guidelines:**</span></span>

-   <span data-ttu-id="cda0c-148">ツールバーのガイドラインは、Dynamics AX の [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="cda0c-148">Toolbar guidelines have been consolidated into the Dynamics AX [General Form Guidelines ](general-form-guidelines.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="cda0c-149">例</span><span class="sxs-lookup"><span data-stu-id="cda0c-149">Examples</span></span>
### <a name="toolbar-and-list"></a><span data-ttu-id="cda0c-150">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="cda0c-150">Toolbar and list</span></span>

<span data-ttu-id="cda0c-151">フォーム: **VendTable (TabCommunication)**</span><span class="sxs-lookup"><span data-stu-id="cda0c-151">Form: **VendTable (TabCommunication)**</span></span> 

<span data-ttu-id="cda0c-152">[![ツールバーおよびリストの例](./media/toolbarlist3.png)](./media/toolbarlist3.png)</span><span class="sxs-lookup"><span data-stu-id="cda0c-152">[![Toolbar and List example](./media/toolbarlist3.png)](./media/toolbarlist3.png)</span></span>

### <a name="toolbar-and-list-double"></a><span data-ttu-id="cda0c-153">ツールバーおよびリスト (ダブル)</span><span class="sxs-lookup"><span data-stu-id="cda0c-153">Toolbar and list (double)</span></span>

<span data-ttu-id="cda0c-154">フォーム: **SalesQuickQuote (TabPageExistingItems)**</span><span class="sxs-lookup"><span data-stu-id="cda0c-154">Form: **SalesQuickQuote (TabPageExistingItems)**</span></span> 

<span data-ttu-id="cda0c-155">[![ツールバーおよびリスト (ダブル) の例](./media/toolbarlist4.png)](./media/toolbarlist4.png)</span><span class="sxs-lookup"><span data-stu-id="cda0c-155">[![Toolbar and List (double) example](./media/toolbarlist4.png)](./media/toolbarlist4.png)</span></span>

## <a name="resources"></a><span data-ttu-id="cda0c-156">リソース</span><span class="sxs-lookup"><span data-stu-id="cda0c-156">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="cda0c-157">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="cda0c-157">Typically used by patterns</span></span>

-   [<span data-ttu-id="cda0c-158">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="cda0c-158">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="cda0c-159">目次</span><span class="sxs-lookup"><span data-stu-id="cda0c-159">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="cda0c-160">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="cda0c-160">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="cda0c-161">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="cda0c-161">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="cda0c-162">付録</span><span class="sxs-lookup"><span data-stu-id="cda0c-162">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="cda0c-163">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="cda0c-163">Frequently asked questions</span></span>

<span data-ttu-id="cda0c-164">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="cda0c-164">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="cda0c-165">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="cda0c-165">Open issues</span></span>

-   <span data-ttu-id="cda0c-166">**CommandButton.Command には、既定のアイコン、ラベル、およびツールチップを提供する追加アクションと削除アクションが含まれていますか。**</span><span class="sxs-lookup"><span data-stu-id="cda0c-166">**Does CommandButton.Command contain Add and Remove actions that provide the default icon, label, and tooltip?**</span></span>
    -   <span data-ttu-id="cda0c-167">まだありません。</span><span class="sxs-lookup"><span data-stu-id="cda0c-167">Not yet.</span></span> <span data-ttu-id="cda0c-168">配送できる 1052359 は、追加および削除コマンドの既定設定を調べます。</span><span class="sxs-lookup"><span data-stu-id="cda0c-168">Deliverable 1052359 will look at setting these defaults for Add and Remove commands.</span></span>
-   <span data-ttu-id="cda0c-169">**移行コンテキストでアイコンのグループ間の区切り記号は重要ですか。**</span><span class="sxs-lookup"><span data-stu-id="cda0c-169">**Do we care about separators between groups of icons in a migration context?**</span></span>
    -   <span data-ttu-id="cda0c-170">現在、ツールバーのボタン グループ間の区切り記号を表示しません。</span><span class="sxs-lookup"><span data-stu-id="cda0c-170">Currently, we don't show separators between button groups on toolbars.</span></span>

### <a name="microsoft-dynamics-ax-2012-content"></a><span data-ttu-id="cda0c-171">Microsoft Dynamics AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="cda0c-171">Microsoft Dynamics AX 2012 content</span></span>

<span data-ttu-id="cda0c-172">**VendTable**</span><span class="sxs-lookup"><span data-stu-id="cda0c-172">**VendTable**</span></span> 

<span data-ttu-id="cda0c-173">[![以前のバージョンの例](./media/toolbarlist5.png)](./media/toolbarlist5.png)</span><span class="sxs-lookup"><span data-stu-id="cda0c-173">[![Previous version example](./media/toolbarlist5.png)](./media/toolbarlist5.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]