---
title: ツールバーおよびリストのサブパターン
description: この記事では、ツールバーとリストのフォームのサブパターンについて説明します。 このサブパターンは、親エンティティの子コレクションを表形式グリッドまたはツリーのいずれかとして表示するために使用されます。
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
ms.custom: 15931
ms.assetid: a60f829b-e496-453b-9e58-f7cb4d67114f
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 684f08fcc33d3edd7006afb957e3fde55db43ba2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1511511"
---
# <a name="toolbar-and-list-subpattern"></a><span data-ttu-id="66f61-104">ツールバーおよびリストのサブパターン</span><span class="sxs-lookup"><span data-stu-id="66f61-104">Toolbar and List subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66f61-105">この記事では、ツールバーとリストのフォームのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="66f61-105">This article provides information about the Toolbar and List form subpattern.</span></span> <span data-ttu-id="66f61-106">このサブパターンは、親エンティティの子コレクションを表形式グリッドまたはツリーのいずれかとして表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="66f61-106">This subpattern is used to show child collections for the parent entity as either a tabular grid or a tree.</span></span> 

<a name="usage"></a><span data-ttu-id="66f61-107">用途</span><span class="sxs-lookup"><span data-stu-id="66f61-107">Usage</span></span>
-----

<span data-ttu-id="66f61-108">このサブパターンは、親エンティティの子コレクションを表形式グリッドまたはツリーのいずれかとして表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="66f61-108">This subpattern is used to show child collections for the parent entity as either a tabular grid or a tree.</span></span> <span data-ttu-id="66f61-109">ツールバーに含まれるアクションは 10 個未満です。</span><span class="sxs-lookup"><span data-stu-id="66f61-109">The toolbar contains fewer than 10 actions.</span></span> <span data-ttu-id="66f61-110">グリッドを使用している場合は、10 未満のフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="66f61-110">If a grid is used, it contains fewer than 10 fields.</span></span> <span data-ttu-id="66f61-111">この記事では、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="66f61-111">This article describes two patterns:</span></span>

-   <span data-ttu-id="66f61-112">**ツールバーおよびリスト** – これはパターンの基本的なバージョンであり、既定で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66f61-112">**Toolbar and list** – This is the basic version of the pattern and should be used by default.</span></span>
-   <span data-ttu-id="66f61-113">**ツールバーおよびリスト (二重)** – このバリアントには、2 つのリストおよび各リストの上のオプションのツールバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="66f61-113">**Toolbar and list (double)** – This variant includes two lists and an optional toolbar above each list.</span></span>

## <a name="wireframes"></a><span data-ttu-id="66f61-114">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="66f61-114">Wireframes</span></span>
### <a name="toolbar-and-list"></a><span data-ttu-id="66f61-115">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="66f61-115">Toolbar and list</span></span>

<span data-ttu-id="66f61-116">[![ToolbarList(1)](./media/toolbarlist1.png)](./media/toolbarlist1.png)</span><span class="sxs-lookup"><span data-stu-id="66f61-116">[![ToolbarList(1)](./media/toolbarlist1.png)](./media/toolbarlist1.png)</span></span>

### <a name="toolbar-and-list-double"></a><span data-ttu-id="66f61-117">ツールバーおよびリスト (ダブル)</span><span class="sxs-lookup"><span data-stu-id="66f61-117">Toolbar and list (double)</span></span>

<span data-ttu-id="66f61-118">[![ToolbarList(2)](./media/toolbarlist2.png)](./media/toolbarlist2.png)</span><span class="sxs-lookup"><span data-stu-id="66f61-118">[![ToolbarList(2)](./media/toolbarlist2.png)](./media/toolbarlist2.png)</span></span>

## <a name="model"></a><span data-ttu-id="66f61-119">モデル</span><span class="sxs-lookup"><span data-stu-id="66f61-119">Model</span></span>
### <a name="toolbar-and-list--high-level-structure"></a><span data-ttu-id="66f61-120">ツールバーおよびリスト - 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="66f61-120">Toolbar and list – High-level structure</span></span>

- <span data-ttu-id="66f61-121">\[コンテナ\]</span><span class="sxs-lookup"><span data-stu-id="66f61-121">\[Container\]</span></span>

    - <span data-ttu-id="66f61-122">*ツールバー (ActionPane、スタイル = ストリップ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-122">*Toolbar (ActionPane, Style=Strip) \[Optional\]*</span></span>
    - <span data-ttu-id="66f61-123">*CustomFilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-123">*CustomFilterGroup (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="66f61-124">グリッド | ツリー | ListView | テーブル</span><span class="sxs-lookup"><span data-stu-id="66f61-124">Grid | Tree | ListView | Table</span></span>
    - <span data-ttu-id="66f61-125">*フッター (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-125">*Footer (Group) \[Optional\]*</span></span>

### <a name="toolbar-and-list-double--high-level-structure"></a><span data-ttu-id="66f61-126">ツールバーおよびリスト (ダブル) - 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="66f61-126">Toolbar and list (double) – High-level structure</span></span>

- <span data-ttu-id="66f61-127">\[コンテナ\]</span><span class="sxs-lookup"><span data-stu-id="66f61-127">\[Container\]</span></span>

    - <span data-ttu-id="66f61-128">*ツールバー1 (ActionPane、スタイル = ストリップ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-128">*Toolbar1 (ActionPane, Style=Strip) \[Optional\]*</span></span>
    - <span data-ttu-id="66f61-129">*CustomFilterGroup1 (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-129">*CustomFilterGroup1 (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="66f61-130">グリッド | ツリー | ListView | テーブル</span><span class="sxs-lookup"><span data-stu-id="66f61-130">Grid | Tree | ListView | Table</span></span>
    - <span data-ttu-id="66f61-131">*ツールバー2 (ActionPane、スタイル = ストリップ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-131">*Toolbar2 (ActionPane, Style=Strip) \[Optional\]*</span></span>
    - <span data-ttu-id="66f61-132">*CustomFilterGroup2 (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-132">*CustomFilterGroup2 (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="66f61-133">グリッド | ツリー | ListView | テーブル</span><span class="sxs-lookup"><span data-stu-id="66f61-133">Grid | Tree | ListView | Table</span></span>
    - <span data-ttu-id="66f61-134">*フッター (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="66f61-134">*Footer (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="66f61-135">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="66f61-135">Core components</span></span>

-   <span data-ttu-id="66f61-136">ToolbarList サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="66f61-136">Apply the ToolbarList subpattern to a container control.</span></span>
-   <span data-ttu-id="66f61-137">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="66f61-137">Address BP Warnings:</span></span>
    -   <span data-ttu-id="66f61-138">**Grid.DataSource** を空にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="66f61-138">**Grid.DataSource** must not be empty.</span></span>
    -   <span data-ttu-id="66f61-139">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="66f61-139">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="66f61-140">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="66f61-140">Related patterns</span></span>

-   [<span data-ttu-id="66f61-141">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="66f61-141">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="66f61-142">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="66f61-142">UX guidelines</span></span>
<span data-ttu-id="66f61-143">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="66f61-143">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="66f61-144">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="66f61-144">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="66f61-145">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="66f61-145">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="66f61-146">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="66f61-146">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="66f61-147">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="66f61-147">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="66f61-148">**ツールバー** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="66f61-148">**Toolbar** **guidelines:**</span></span>

-   <span data-ttu-id="66f61-149">ツールバーのガイドラインは、Dynamics AX の [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="66f61-149">Toolbar guidelines have been consolidated into the Dynamics AX [General Form Guidelines ](general-form-guidelines.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="66f61-150">例</span><span class="sxs-lookup"><span data-stu-id="66f61-150">Examples</span></span>
### <a name="toolbar-and-list"></a><span data-ttu-id="66f61-151">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="66f61-151">Toolbar and list</span></span>

<span data-ttu-id="66f61-152">フォーム: **VendTable (TabCommunication)**</span><span class="sxs-lookup"><span data-stu-id="66f61-152">Form: **VendTable (TabCommunication)**</span></span> 

<span data-ttu-id="66f61-153">[![ToolbarList(3)](./media/toolbarlist3.png)](./media/toolbarlist3.png)</span><span class="sxs-lookup"><span data-stu-id="66f61-153">[![ToolbarList(3)](./media/toolbarlist3.png)](./media/toolbarlist3.png)</span></span>

### <a name="toolbar-and-list-double"></a><span data-ttu-id="66f61-154">ツールバーおよびリスト (ダブル)</span><span class="sxs-lookup"><span data-stu-id="66f61-154">Toolbar and list (double)</span></span>

<span data-ttu-id="66f61-155">フォーム: **SalesQuickQuote (TabPageExistingItems)**</span><span class="sxs-lookup"><span data-stu-id="66f61-155">Form: **SalesQuickQuote (TabPageExistingItems)**</span></span> 

<span data-ttu-id="66f61-156">[![ToolbarList(4)](./media/toolbarlist4.png)](./media/toolbarlist4.png)</span><span class="sxs-lookup"><span data-stu-id="66f61-156">[![ToolbarList(4)](./media/toolbarlist4.png)](./media/toolbarlist4.png)</span></span>

## <a name="resources"></a><span data-ttu-id="66f61-157">リソース</span><span class="sxs-lookup"><span data-stu-id="66f61-157">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="66f61-158">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="66f61-158">Typically used by patterns</span></span>

-   [<span data-ttu-id="66f61-159">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="66f61-159">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="66f61-160">目次</span><span class="sxs-lookup"><span data-stu-id="66f61-160">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="66f61-161">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="66f61-161">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="66f61-162">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="66f61-162">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="66f61-163">付録</span><span class="sxs-lookup"><span data-stu-id="66f61-163">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="66f61-164">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="66f61-164">Frequently asked questions</span></span>

<span data-ttu-id="66f61-165">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="66f61-165">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="66f61-166">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="66f61-166">Open issues</span></span>

-   <span data-ttu-id="66f61-167">**CommandButton.Command には、既定のアイコン、ラベル、およびツールチップを提供する追加アクションと削除アクションが含まれていますか。**</span><span class="sxs-lookup"><span data-stu-id="66f61-167">**Does CommandButton.Command contain Add and Remove actions that provide the default icon, label, and tooltip?**</span></span>
    -   <span data-ttu-id="66f61-168">まだありません。</span><span class="sxs-lookup"><span data-stu-id="66f61-168">Not yet.</span></span> <span data-ttu-id="66f61-169">配送できる 1052359 は、追加および削除コマンドの既定設定を調べます。</span><span class="sxs-lookup"><span data-stu-id="66f61-169">Deliverable 1052359 will look at setting these defaults for Add and Remove commands.</span></span>
-   <span data-ttu-id="66f61-170">**移行コンテキストでアイコンのグループ間の区切り記号は重要ですか。**</span><span class="sxs-lookup"><span data-stu-id="66f61-170">**Do we care about separators between groups of icons in a migration context?**</span></span>
    -   <span data-ttu-id="66f61-171">現在、ツールバーのボタン グループ間の区切り記号を表示しません。</span><span class="sxs-lookup"><span data-stu-id="66f61-171">Currently, we don't show separators between button groups on toolbars.</span></span>

### <a name="microsoft-dynamics-ax-2012-content"></a><span data-ttu-id="66f61-172">Microsoft Dynamics AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="66f61-172">Microsoft Dynamics AX 2012 content</span></span>

<span data-ttu-id="66f61-173">**VendTable**</span><span class="sxs-lookup"><span data-stu-id="66f61-173">**VendTable**</span></span> 

<span data-ttu-id="66f61-174">[![ToolbarList(5)](./media/toolbarlist5.png)](./media/toolbarlist5.png)</span><span class="sxs-lookup"><span data-stu-id="66f61-174">[![ToolbarList(5)](./media/toolbarlist5.png)](./media/toolbarlist5.png)</span></span>
