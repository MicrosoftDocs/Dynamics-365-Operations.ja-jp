---
title: リスト パネルのサブパターン
description: この記事では、リスト パネル フォームのサブパターンに関する情報を提供します。このサブパターンは、互いにデータを移動する 2 つのリストを管理します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 12433
ms.assetid: 81df4016-d7b9-4376-8a78-bdd435d686f6
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df6aea1de9fde3661c9236a39025ad6d52110bb
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189300"
---
# <a name="list-panel-subpattern"></a><span data-ttu-id="d41ca-103">リスト パネルのサブパターン</span><span class="sxs-lookup"><span data-stu-id="d41ca-103">List Panel subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d41ca-104">この記事では、リスト パネル フォームのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d41ca-104">This article provides information about the List Panel form subpattern.</span></span> <span data-ttu-id="d41ca-105">アプリケーション チームはこのサブパターンを使用して相互にデータを移動する 2 つのリストを管理します。</span><span class="sxs-lookup"><span data-stu-id="d41ca-105">Application teams use this subpattern to manage two lists that move data between each other.</span></span>

## <a name="usage"></a><span data-ttu-id="d41ca-106">用途</span><span class="sxs-lookup"><span data-stu-id="d41ca-106">Usage</span></span>

<span data-ttu-id="d41ca-107">リスト パネルは、アプリケーション チームがそれぞれの間でデータを移動する 2 つのリストを管理するために使用するサブパターンです。</span><span class="sxs-lookup"><span data-stu-id="d41ca-107">List Panel is the subpattern that application teams use to manage two lists that move data between each other.</span></span> <span data-ttu-id="d41ca-108">このパターンは、相互にデータを移動する 2 つのリストを管理する **SysListPanel** クラス (プログラム的) アプローチのモデル化バージョンを表すことを意図しています。</span><span class="sxs-lookup"><span data-stu-id="d41ca-108">This pattern is meant to represent a modeled version of the **SysListPanel** class (programmatic) approach of managing two lists that move data between each other.</span></span> <span data-ttu-id="d41ca-109">リスト パネル サブパターンは、次のコントロールに対して適用できます。</span><span class="sxs-lookup"><span data-stu-id="d41ca-109">The List Panel subpattern can be applied on the following controls:</span></span>

-   <span data-ttu-id="d41ca-110">TabPage コントロール</span><span class="sxs-lookup"><span data-stu-id="d41ca-110">TabPage control</span></span>
-   <span data-ttu-id="d41ca-111">グループ コントロール</span><span class="sxs-lookup"><span data-stu-id="d41ca-111">Group control</span></span>

## <a name="wireframe"></a><span data-ttu-id="d41ca-112">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="d41ca-112">Wireframe</span></span>
<span data-ttu-id="d41ca-113">[![リスト パネルのワイヤーフレーム](./media/listpanel1-1024x339.png)](./media/listpanel1.png)</span><span class="sxs-lookup"><span data-stu-id="d41ca-113">[![List Panel wireframe](./media/listpanel1-1024x339.png)](./media/listpanel1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="d41ca-114">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="d41ca-114">Pattern changes</span></span>
<span data-ttu-id="d41ca-115">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d41ca-115">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="d41ca-116">リスト (Grid/ListView) およびツリー コントロールがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d41ca-116">List (Grid/ListView) and Tree controls are supported.</span></span>
-   <span data-ttu-id="d41ca-117">右側のパネルは選択したセクションです。</span><span class="sxs-lookup"><span data-stu-id="d41ca-117">The right panel is the selected section.</span></span>
-   <span data-ttu-id="d41ca-118">左側のパネルは利用可能なセクションです。</span><span class="sxs-lookup"><span data-stu-id="d41ca-118">The left panel is the available section.</span></span>
-   <span data-ttu-id="d41ca-119">6 つのボタンをアクションとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="d41ca-119">Six buttons are available as actions:</span></span>
    -   <span data-ttu-id="d41ca-120">追加</span><span class="sxs-lookup"><span data-stu-id="d41ca-120">Add</span></span>
    -   <span data-ttu-id="d41ca-121">削除</span><span class="sxs-lookup"><span data-stu-id="d41ca-121">Remove</span></span>
    -   <span data-ttu-id="d41ca-122">すべて追加 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d41ca-122">Add All (Optional)</span></span>
    -   <span data-ttu-id="d41ca-123">すべて削除 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d41ca-123">Remove All (Optional)</span></span>
    -   <span data-ttu-id="d41ca-124">上へ移動 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d41ca-124">Move Up (Optional)</span></span>
    -   <span data-ttu-id="d41ca-125">下へ移動 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d41ca-125">Move Down (Optional)</span></span>

## <a name="model"></a><span data-ttu-id="d41ca-126">モデル</span><span class="sxs-lookup"><span data-stu-id="d41ca-126">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="d41ca-127">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="d41ca-127">High-level structure</span></span>

- <span data-ttu-id="d41ca-128">\[コンテナ\]</span><span class="sxs-lookup"><span data-stu-id="d41ca-128">\[Container\]</span></span>

    - <span data-ttu-id="d41ca-129">*CustomFilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="d41ca-129">*CustomFilterGroup (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="d41ca-130">ListPanelGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="d41ca-130">ListPanelGroup (Group)</span></span>

        - <span data-ttu-id="d41ca-131">AvailablePanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="d41ca-131">AvailablePanel (Group)</span></span>

            - <span data-ttu-id="d41ca-132">グリッド | ツリー | ListView | ListBox</span><span class="sxs-lookup"><span data-stu-id="d41ca-132">Grid | Tree | ListView | ListBox</span></span>

        - <span data-ttu-id="d41ca-133">ActionPanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="d41ca-133">ActionPanel (Group)</span></span>

            - <span data-ttu-id="d41ca-134">AddButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="d41ca-134">AddButton (Button)</span></span>
            - <span data-ttu-id="d41ca-135">RemoveButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="d41ca-135">RemoveButton (Button)</span></span>
            - <span data-ttu-id="d41ca-136">*AllAllButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="d41ca-136">*AllAllButton (Button) \[Optional\]*</span></span>
            - <span data-ttu-id="d41ca-137">*RemoveAllButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="d41ca-137">*RemoveAllButton (Button) \[Optional\]*</span></span>

        - <span data-ttu-id="d41ca-138">SelectedPanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="d41ca-138">SelectedPanel (Group)</span></span>

            - <span data-ttu-id="d41ca-139">グリッド | ツリー | ListView | ListBox\*</span><span class="sxs-lookup"><span data-stu-id="d41ca-139">Grid | Tree | ListView | ListBox\*</span></span>

        - <span data-ttu-id="d41ca-140">*MoveUpDownPanel \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="d41ca-140">*MoveUpDownPanel \[Optional\]*</span></span>

            - <span data-ttu-id="d41ca-141">MoveUpButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="d41ca-141">MoveUpButton (Button)</span></span>
            - <span data-ttu-id="d41ca-142">MoveDownButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="d41ca-142">MoveDownButton (Button)</span></span>

### <a name="core-components"></a><span data-ttu-id="d41ca-143">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d41ca-143">Core components</span></span>

-   <span data-ttu-id="d41ca-144">ListPanel サブパターンをコンテナー (TabPage またはグループ) コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="d41ca-144">Apply the ListPanel subpattern to the container (TabPage or Group) control.</span></span>
-   <span data-ttu-id="d41ca-145">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="d41ca-145">Address BP Warnings:</span></span>
    -   <span data-ttu-id="d41ca-146">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="d41ca-146">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="d41ca-147">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="d41ca-147">UX guidelines</span></span>
<span data-ttu-id="d41ca-148">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="d41ca-148">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="d41ca-149">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d41ca-149">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="d41ca-150">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="d41ca-150">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="d41ca-151">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="d41ca-151">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="d41ca-152">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="d41ca-152">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="d41ca-153">例</span><span class="sxs-lookup"><span data-stu-id="d41ca-153">Examples</span></span>
<span data-ttu-id="d41ca-154">フォーム: **SalesSummaryParameters (GroupQuotation)**</span><span class="sxs-lookup"><span data-stu-id="d41ca-154">Form: **SalesSummaryParameters (GroupQuotation)**</span></span> 

<span data-ttu-id="d41ca-155">[![リスト パネルの例](./media/listpanel3.png)](./media/listpanel3.png)</span><span class="sxs-lookup"><span data-stu-id="d41ca-155">[![List Panel example](./media/listpanel3.png)](./media/listpanel3.png)</span></span>

## <a name="resources"></a><span data-ttu-id="d41ca-156">リソース</span><span class="sxs-lookup"><span data-stu-id="d41ca-156">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="d41ca-157">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="d41ca-157">Typically used by patterns</span></span>

-   [<span data-ttu-id="d41ca-158">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="d41ca-158">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="d41ca-159">目次</span><span class="sxs-lookup"><span data-stu-id="d41ca-159">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="d41ca-160">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="d41ca-160">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="d41ca-161">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="d41ca-161">Dialog</span></span>](dialog-form-pattern.md)
-   [<span data-ttu-id="d41ca-162">ウィザード</span><span class="sxs-lookup"><span data-stu-id="d41ca-162">Wizard</span></span>](wizard-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="d41ca-163">付録</span><span class="sxs-lookup"><span data-stu-id="d41ca-163">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="d41ca-164">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d41ca-164">Frequently asked questions</span></span>

<span data-ttu-id="d41ca-165">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="d41ca-165">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="d41ca-166">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="d41ca-166">Open issues</span></span>

-   <span data-ttu-id="d41ca-167">なし</span><span class="sxs-lookup"><span data-stu-id="d41ca-167">None</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="d41ca-168">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="d41ca-168">AX 2012 content</span></span>

<span data-ttu-id="d41ca-169">[![リスト パネルの例](./media/listpanel4.png)](./media/listpanel4.png)</span><span class="sxs-lookup"><span data-stu-id="d41ca-169">[![List Panel example](./media/listpanel4.png)](./media/listpanel4.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]