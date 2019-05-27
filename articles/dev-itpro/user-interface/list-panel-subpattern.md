---
title: リスト パネルのサブパターン
description: この記事では、リスト パネル フォームのサブパターンに関する情報を提供します。 アプリケーション チームはこのサブパターンを使用して相互にデータを移動する 2 つのリストを管理します。
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
ms.custom: 12433
ms.assetid: 81df4016-d7b9-4376-8a78-bdd435d686f6
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4aefd708e01efb9fa2e8cc31aab2b26c173e41d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537179"
---
# <a name="list-panel-subpattern"></a><span data-ttu-id="ae3ee-104">リスト パネルのサブパターン</span><span class="sxs-lookup"><span data-stu-id="ae3ee-104">List Panel subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae3ee-105">この記事では、リスト パネル フォームのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-105">This article provides information about the List Panel form subpattern.</span></span> <span data-ttu-id="ae3ee-106">アプリケーション チームはこのサブパターンを使用して相互にデータを移動する 2 つのリストを管理します。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-106">Application teams use this subpattern to manage two lists that move data between each other.</span></span>

<a name="usage"></a><span data-ttu-id="ae3ee-107">用途</span><span class="sxs-lookup"><span data-stu-id="ae3ee-107">Usage</span></span>
-----

<span data-ttu-id="ae3ee-108">リスト パネルは、アプリケーション チームがそれぞれの間でデータを移動する 2 つのリストを管理するために使用するサブパターンです。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-108">List Panel is the subpattern that application teams use to manage two lists that move data between each other.</span></span> <span data-ttu-id="ae3ee-109">このパターンは、相互にデータを移動する 2 つのリストを管理する **SysListPanel** クラス (プログラム的) アプローチのモデル化バージョンを表すことを意図しています。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-109">This pattern is meant to represent a modeled version of the **SysListPanel** class (programmatic) approach of managing two lists that move data between each other.</span></span> <span data-ttu-id="ae3ee-110">リスト パネル サブパターンは、次のコントロールに対して適用できます。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-110">The List Panel subpattern can be applied on the following controls:</span></span>

-   <span data-ttu-id="ae3ee-111">TabPage コントロール</span><span class="sxs-lookup"><span data-stu-id="ae3ee-111">TabPage control</span></span>
-   <span data-ttu-id="ae3ee-112">グループ コントロール</span><span class="sxs-lookup"><span data-stu-id="ae3ee-112">Group control</span></span>

## <a name="wireframe"></a><span data-ttu-id="ae3ee-113">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="ae3ee-113">Wireframe</span></span>
<span data-ttu-id="ae3ee-114">[![ListPanel(1)](./media/listpanel1-1024x339.png)](./media/listpanel1.png)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-114">[![ListPanel(1)](./media/listpanel1-1024x339.png)](./media/listpanel1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="ae3ee-115">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="ae3ee-115">Pattern changes</span></span>
<span data-ttu-id="ae3ee-116">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-116">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="ae3ee-117">リスト (Grid/ListView) およびツリー コントロールがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-117">List (Grid/ListView) and Tree controls are supported.</span></span>
-   <span data-ttu-id="ae3ee-118">右側のパネルは選択したセクションです。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-118">The right panel is the selected section.</span></span>
-   <span data-ttu-id="ae3ee-119">左側のパネルは利用可能なセクションです。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-119">The left panel is the available section.</span></span>
-   <span data-ttu-id="ae3ee-120">6 つのボタンをアクションとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-120">Six buttons are available as actions:</span></span>
    -   <span data-ttu-id="ae3ee-121">追加</span><span class="sxs-lookup"><span data-stu-id="ae3ee-121">Add</span></span>
    -   <span data-ttu-id="ae3ee-122">削除</span><span class="sxs-lookup"><span data-stu-id="ae3ee-122">Remove</span></span>
    -   <span data-ttu-id="ae3ee-123">すべて追加 (オプション)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-123">Add All (Optional)</span></span>
    -   <span data-ttu-id="ae3ee-124">すべて削除 (オプション)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-124">Remove All (Optional)</span></span>
    -   <span data-ttu-id="ae3ee-125">上へ移動 (オプション)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-125">Move Up (Optional)</span></span>
    -   <span data-ttu-id="ae3ee-126">下へ移動 (オプション)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-126">Move Down (Optional)</span></span>

## <a name="model"></a><span data-ttu-id="ae3ee-127">モデル</span><span class="sxs-lookup"><span data-stu-id="ae3ee-127">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="ae3ee-128">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="ae3ee-128">High-level structure</span></span>

- <span data-ttu-id="ae3ee-129">\[コンテナ\]</span><span class="sxs-lookup"><span data-stu-id="ae3ee-129">\[Container\]</span></span>

    - <span data-ttu-id="ae3ee-130">*CustomFilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ae3ee-130">*CustomFilterGroup (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="ae3ee-131">ListPanelGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-131">ListPanelGroup (Group)</span></span>

        - <span data-ttu-id="ae3ee-132">AvailablePanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-132">AvailablePanel (Group)</span></span>

            - <span data-ttu-id="ae3ee-133">グリッド | ツリー | ListView | ListBox</span><span class="sxs-lookup"><span data-stu-id="ae3ee-133">Grid | Tree | ListView | ListBox</span></span>

        - <span data-ttu-id="ae3ee-134">ActionPanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-134">ActionPanel (Group)</span></span>

            - <span data-ttu-id="ae3ee-135">AddButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-135">AddButton (Button)</span></span>
            - <span data-ttu-id="ae3ee-136">RemoveButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-136">RemoveButton (Button)</span></span>
            - <span data-ttu-id="ae3ee-137">*AllAllButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ae3ee-137">*AllAllButton (Button) \[Optional\]*</span></span>
            - <span data-ttu-id="ae3ee-138">*RemoveAllButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ae3ee-138">*RemoveAllButton (Button) \[Optional\]*</span></span>

        - <span data-ttu-id="ae3ee-139">SelectedPanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-139">SelectedPanel (Group)</span></span>

            - <span data-ttu-id="ae3ee-140">グリッド | ツリー | ListView | ListBox\*</span><span class="sxs-lookup"><span data-stu-id="ae3ee-140">Grid | Tree | ListView | ListBox\*</span></span>

        - <span data-ttu-id="ae3ee-141">*MoveUpDownPanel \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ae3ee-141">*MoveUpDownPanel \[Optional\]*</span></span>

            - <span data-ttu-id="ae3ee-142">MoveUpButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-142">MoveUpButton (Button)</span></span>
            - <span data-ttu-id="ae3ee-143">MoveDownButton (ボタン)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-143">MoveDownButton (Button)</span></span>

### <a name="core-components"></a><span data-ttu-id="ae3ee-144">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae3ee-144">Core components</span></span>

-   <span data-ttu-id="ae3ee-145">ListPanel サブパターンをコンテナー (TabPage またはグループ) コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-145">Apply the ListPanel subpattern to the container (TabPage or Group) control.</span></span>
-   <span data-ttu-id="ae3ee-146">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-146">Address BP Warnings:</span></span>
    -   <span data-ttu-id="ae3ee-147">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-147">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="ae3ee-148">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ae3ee-148">UX guidelines</span></span>
<span data-ttu-id="ae3ee-149">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-149">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="ae3ee-150">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-150">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="ae3ee-151">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-151">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="ae3ee-152">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="ae3ee-152">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="ae3ee-153">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-153">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="ae3ee-154">例</span><span class="sxs-lookup"><span data-stu-id="ae3ee-154">Examples</span></span>
<span data-ttu-id="ae3ee-155">フォーム: **SalesSummaryParameters (GroupQuotation)**</span><span class="sxs-lookup"><span data-stu-id="ae3ee-155">Form: **SalesSummaryParameters (GroupQuotation)**</span></span> 

<span data-ttu-id="ae3ee-156">[![ListPanel(3)](./media/listpanel3.png)](./media/listpanel3.png)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-156">[![ListPanel(3)](./media/listpanel3.png)](./media/listpanel3.png)</span></span>

## <a name="resources"></a><span data-ttu-id="ae3ee-157">リソース</span><span class="sxs-lookup"><span data-stu-id="ae3ee-157">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="ae3ee-158">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="ae3ee-158">Typically used by patterns</span></span>

-   [<span data-ttu-id="ae3ee-159">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="ae3ee-159">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="ae3ee-160">目次</span><span class="sxs-lookup"><span data-stu-id="ae3ee-160">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="ae3ee-161">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="ae3ee-161">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="ae3ee-162">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="ae3ee-162">Dialog</span></span>](dialog-form-pattern.md)
-   [<span data-ttu-id="ae3ee-163">ウィザード</span><span class="sxs-lookup"><span data-stu-id="ae3ee-163">Wizard</span></span>](wizard-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="ae3ee-164">付録</span><span class="sxs-lookup"><span data-stu-id="ae3ee-164">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="ae3ee-165">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ae3ee-165">Frequently asked questions</span></span>

<span data-ttu-id="ae3ee-166">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="ae3ee-166">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="ae3ee-167">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="ae3ee-167">Open issues</span></span>

-   <span data-ttu-id="ae3ee-168">なし</span><span class="sxs-lookup"><span data-stu-id="ae3ee-168">None</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="ae3ee-169">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="ae3ee-169">AX 2012 content</span></span>

<span data-ttu-id="ae3ee-170">[![ListPanel(4)](./media/listpanel4.png)](./media/listpanel4.png)</span><span class="sxs-lookup"><span data-stu-id="ae3ee-170">[![ListPanel(4)](./media/listpanel4.png)](./media/listpanel4.png)</span></span>
