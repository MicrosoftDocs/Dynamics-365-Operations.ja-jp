---
title: "ダイアログ削除のフォーム パターン"
description: "このトピックでは、ドロップ ダイアログ フォームのパターンについて説明します。 このパターンは、フィールド数が 7 以下の場合にアクションを開始するために使用されます。"
author: jasongre
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 16041
ms.assetid: 94ffa218-de7d-4d13-9a8a-461cad0970b3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 55dfee0686632ba09f1de91ae28d4b002a73b986
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="drop-dialog-form-pattern"></a><span data-ttu-id="55b6f-104">ダイアログ削除のフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="55b6f-104">Drop Dialog form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55b6f-105">このトピックでは、ドロップ ダイアログ フォームのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-105">This topic provides information about the Drop Dialog form pattern.</span></span> <span data-ttu-id="55b6f-106">このパターンは、フィールド数が 7 以下の場合にアクションを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="55b6f-106">This pattern is used to initiate actions when the number of fields is seven or fewer.</span></span> 

<a name="usage"></a><span data-ttu-id="55b6f-107">用途</span><span class="sxs-lookup"><span data-stu-id="55b6f-107">Usage</span></span>
-----

<span data-ttu-id="55b6f-108">ダイアログ削除パターンは、フィールド数が 7 以下の場合にアクションを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="55b6f-108">The Drop Dialog pattern is used to initiate actions when the number of fields is seven or fewer.</span></span> <span data-ttu-id="55b6f-109">ドロップ ダイアログはユーザーが使用するのが素早く簡単で、スライダーとして表示される完全なダイアログよりも軽量です。</span><span class="sxs-lookup"><span data-stu-id="55b6f-109">Drop dialogs are quick and easy for users to use, and are more lightweight than a full dialog that is presented as a slider.</span></span> <span data-ttu-id="55b6f-110">ドロップ ダイアログは、メニューとして使うには軽量であることを示します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-110">Drop dialogs should feel as lightweight to use as a menu.</span></span> <span data-ttu-id="55b6f-111">このドキュメントでは、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-111">Two patterns are described in this document:</span></span>

-   <span data-ttu-id="55b6f-112">**ドロップ ダイアログ** - これは、基本的なドロップ ダイアログ パターンです。</span><span class="sxs-lookup"><span data-stu-id="55b6f-112">**Drop dialog** – This is the basic Drop dialog pattern.</span></span> <span data-ttu-id="55b6f-113">ドロップ ダイアログが編集可能な場合は、これが使用する正しいパターンです。</span><span class="sxs-lookup"><span data-stu-id="55b6f-113">If your Drop dialog is editable, this is the correct pattern to use.</span></span>
-   <span data-ttu-id="55b6f-114">**ドロップ ダイアログ (読み取り専用)** - このドロップ ダイアログ パターンは、編集できない情報フォーム用です。</span><span class="sxs-lookup"><span data-stu-id="55b6f-114">**Drop dialog (read only)** – This Drop dialog pattern is for informational forms that aren't editable.</span></span> <span data-ttu-id="55b6f-115">このバリエーションには **OK** ボタンはありません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-115">This variation doesn't have an **OK** button.</span></span>

## <a name="wireframe"></a><span data-ttu-id="55b6f-116">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="55b6f-116">Wireframe</span></span>
### <a name="drop-dialog-basic"></a><span data-ttu-id="55b6f-117">ドロップ ダイアログ (basic)</span><span class="sxs-lookup"><span data-stu-id="55b6f-117">Drop dialog (basic)</span></span>

<span data-ttu-id="55b6f-118">[![DropDialog(1)](./media/dropdialog1.png)](./media/dropdialog1.png)</span><span class="sxs-lookup"><span data-stu-id="55b6f-118">[![DropDialog(1)](./media/dropdialog1.png)](./media/dropdialog1.png)</span></span>

### <a name="drop-dialog-read-only"></a><span data-ttu-id="55b6f-119">ドロップ ダイアログ (読み取り専用)</span><span class="sxs-lookup"><span data-stu-id="55b6f-119">Drop dialog (read only)</span></span>

<span data-ttu-id="55b6f-120">[![DropDialog(2)](./media/dropdialog2.png)](./media/dropdialog2.png)</span><span class="sxs-lookup"><span data-stu-id="55b6f-120">[![DropDialog(2)](./media/dropdialog2.png)](./media/dropdialog2.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="55b6f-121">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="55b6f-121">Pattern changes</span></span>
<span data-ttu-id="55b6f-122">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-122">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="55b6f-123">エラー メッセージの手動処理が必要なくなりました。</span><span class="sxs-lookup"><span data-stu-id="55b6f-123">Manual handling of error messages is no longer required.</span></span>

## <a name="model"></a><span data-ttu-id="55b6f-124">モデル</span><span class="sxs-lookup"><span data-stu-id="55b6f-124">Model</span></span>
### <a name="drop-dialog-basic--high-level-structure"></a><span data-ttu-id="55b6f-125">ドロップ ダイアログ (basic) – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="55b6f-125">Drop dialog (basic) – High-level structure</span></span>

- <span data-ttu-id="55b6f-126">デザイン</span><span class="sxs-lookup"><span data-stu-id="55b6f-126">Design</span></span>

    - <span data-ttu-id="55b6f-127">*SecondaryInstruction (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="55b6f-127">*SecondaryInstruction (StaticText) \[optional\]*</span></span>
    - <span data-ttu-id="55b6f-128">DialogContent (Group)</span><span class="sxs-lookup"><span data-stu-id="55b6f-128">DialogContent (Group)</span></span>
    - <span data-ttu-id="55b6f-129">DialogCommitContainer (ButtonGroup)</span><span class="sxs-lookup"><span data-stu-id="55b6f-129">DialogCommitContainer (ButtonGroup)</span></span>

        - <span data-ttu-id="55b6f-130">OKButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="55b6f-130">OKButton ($Button)</span></span>

### <a name="drop-dialog-read-only--high-level-structure"></a><span data-ttu-id="55b6f-131">ドロップ ダイアログ (読み取り専用) – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="55b6f-131">Drop dialog (read only) – High-level structure</span></span>

- <span data-ttu-id="55b6f-132">デザイン</span><span class="sxs-lookup"><span data-stu-id="55b6f-132">Design</span></span>

    - <span data-ttu-id="55b6f-133">*SecondaryInstruction (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="55b6f-133">*SecondaryInstruction (StaticText) \[optional\]*</span></span>
    - <span data-ttu-id="55b6f-134">DialogContent (Group)</span><span class="sxs-lookup"><span data-stu-id="55b6f-134">DialogContent (Group)</span></span>

### <a name="core-components"></a><span data-ttu-id="55b6f-135">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="55b6f-135">Core components</span></span>

-   <span data-ttu-id="55b6f-136">**Form.Design** にドロップ ダイアログ パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-136">Apply the Drop Dialog pattern on **Form.Design**.</span></span>
-   <span data-ttu-id="55b6f-137">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-137">Address BP Warnings:</span></span>
    -   <span data-ttu-id="55b6f-138">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-138">**Design.Caption** isn't empty.</span></span>
    -   <span data-ttu-id="55b6f-139">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-139">The form must be referenced by at least one menu item.</span></span>
    -   <span data-ttu-id="55b6f-140">**StaticText.Text** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-140">**StaticText.Text** isn't empty.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="55b6f-141">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="55b6f-141">Related patterns</span></span>

-   [<span data-ttu-id="55b6f-142">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="55b6f-142">Dialog</span></span>](dialog-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="55b6f-143">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="55b6f-143">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="55b6f-144">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="55b6f-144">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="55b6f-145">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="55b6f-145">Toolbar and List</span></span>](toolbar-list-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="55b6f-146">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="55b6f-146">UX guidelines</span></span>
<span data-ttu-id="55b6f-147">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="55b6f-147">The verification checklist shows you the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="55b6f-148">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-148">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="55b6f-149">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-149">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="55b6f-150">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="55b6f-150">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="55b6f-151">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="55b6f-151">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="55b6f-152">**ドロップ ダイアログ ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="55b6f-152">**Drop dialog guidelines:**</span></span>

-   <span data-ttu-id="55b6f-153">次の条件に当てはまる場合は、ドロップ ダイアログを使用する必要があります:</span><span class="sxs-lookup"><span data-stu-id="55b6f-153">A Drop dialog should be used if the following conditions exist:</span></span>
    -   <span data-ttu-id="55b6f-154">7 つ以下のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-154">There are seven or fewer fields.</span></span>
    -   <span data-ttu-id="55b6f-155">ユーザーは、簡単に情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="55b6f-155">The user can enter the information quickly.</span></span>
    -   <span data-ttu-id="55b6f-156">最小限のフィールド検証が必要です。</span><span class="sxs-lookup"><span data-stu-id="55b6f-156">Minimal field validation is required.</span></span>
    -   <span data-ttu-id="55b6f-157">追加の子フォームを開くボタンはありません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-157">There are no buttons that open additional child forms.</span></span>
        -   <span data-ttu-id="55b6f-158">**例外:** ルックアップ、拡張プレビュー、および表示の詳細のナビゲーション</span><span class="sxs-lookup"><span data-stu-id="55b6f-158">**Exceptions:** Lookups, Enhanced preview, and View details navigation</span></span>
    -   <span data-ttu-id="55b6f-159">編集可能なグリッドはありません (選択専用のグリッドは使用できます)。</span><span class="sxs-lookup"><span data-stu-id="55b6f-159">There is no editable grid (select-only grids are allowed).</span></span>
-   <span data-ttu-id="55b6f-160">ドロップ ダイアログが最初に開いたときに、フォーカスは、ドロップ ダイアログの最初の編集可能なフィールドにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-160">Focus should be in the first editable field on the Drop dialog when it is first opened.</span></span>
-   <span data-ttu-id="55b6f-161">ドロップ ダイアログには、上部に**主な指示**がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-161">A Drop dialog should have a **main instruction** at the top.</span></span>
    -   <span data-ttu-id="55b6f-162">主な指示は、ユーザーがドロップ ダイアログで行うべきことを簡潔に説明するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-162">The main instruction should be used to explain concisely what the user should do in the Drop dialog.</span></span> <span data-ttu-id="55b6f-163">指示は、特定の明細書、命令的な指示、または質問でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-163">The instruction should be a specific statement, an imperative direction, or a question.</span></span> <span data-ttu-id="55b6f-164">適切な手順では、操作の仕組みにだけに重点を置くのではなく、ドロップ ダイアログを使用してユーザーの目的を伝達します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-164">Good instructions communicate the user’s objective with the Drop dialog rather than focusing purely on the mechanics of manipulating it.</span></span>
    -   <span data-ttu-id="55b6f-165">主な指示が明細書である場合、最終的な期間を含めません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-165">A final period should not be included if the main instruction is a statement.</span></span> <span data-ttu-id="55b6f-166">指示が質問である場合、疑問符が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-166">If the instruction is a question, a question mark should be included.</span></span>
    -   <span data-ttu-id="55b6f-167">主要な指示に加えて、ユーザへの二次命令が表示され、ユーザがドロップ ダイアログを理解または使用するのに役立つ追加情報を提示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-167">Besides the main instruction, a secondary instruction to the user should be displayed, and it should present additional information that will help the user understand or use the Drop dialog.</span></span> <span data-ttu-id="55b6f-168">2 番目の指示は、大文字小文字の完全な文で構成する必要があり、文末の句点を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-168">The secondary instruction should consist of a complete sentence in sentence case and should have end punctuation.</span></span>
        -   <span data-ttu-id="55b6f-169">**例外:** 追加指示が主要な指示をわずかに異なる言い方で単に繰り返す場合は、それを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="55b6f-169">**Exception:** If the additional instruction merely repeats the main instruction with slightly different wording, don't include it.</span></span>
-   <span data-ttu-id="55b6f-170">ドロップ ダイアログには、**コンテンツ**領域が必要です。</span><span class="sxs-lookup"><span data-stu-id="55b6f-170">A Drop dialog should have a **content** area.</span></span>
    -   <span data-ttu-id="55b6f-171">検証エラーを避けるために、制約された入力コントロールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-171">Constrained input controls should be used to avoid validation errors.</span></span> <span data-ttu-id="55b6f-172">例には、選択リスト、チェック ボックス、オプション ボタン、およびコマンド リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="55b6f-172">Examples include selection lists, check boxes, radio buttons, and command links.</span></span>
    -   <span data-ttu-id="55b6f-173">可能な場合は、入力ごとに適切な既定値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-173">Reasonable defaults for each input should be provided whenever possible.</span></span>
-   <span data-ttu-id="55b6f-174">ドロップ ダイアログには、次のような**コミット**ボタン領域が必要です:</span><span class="sxs-lookup"><span data-stu-id="55b6f-174">A Drop dialog should have a **commit** button area that:</span></span>
    -   <span data-ttu-id="55b6f-175">**キャンセル**ボタンを、**持たない**でください。</span><span class="sxs-lookup"><span data-stu-id="55b6f-175">Does **not** have a **Cancel** button.</span></span>
    -   <span data-ttu-id="55b6f-176">ドロップ ダイアログの既定のボタンとしてマークされるボタンがあります (ボタンが存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="55b6f-176">Has a button that is marked as the default button of the Drop dialog (if a button exists).</span></span>
    -   <span data-ttu-id="55b6f-177">既定のボタンのラベルは、主な指示に記述されているアクションを実装する動詞でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-177">The label of the default button should be a verb that implements the action that is described in the main instruction.</span></span> <span data-ttu-id="55b6f-178">たとえば、主要な指示が「新製品の作成」である場合、ボタン ラベルは**作成**となります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-178">For example, if the main instruction is “Create new product,” the button label should be **Create**.</span></span> <span data-ttu-id="55b6f-179">ボタンの適切な動詞がない場合は、**OK** を使用します。</span><span class="sxs-lookup"><span data-stu-id="55b6f-179">If there is no appropriate verb for the button, use **OK**.</span></span>
    -   <span data-ttu-id="55b6f-180">コミット ボタン領域には、独自の意味を持ち、主な指示への応答である特定のコミット ボタン ラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="55b6f-180">The commit button area should have specific commit button labels that make sense on their own and are a response to the main instruction.</span></span>

<span data-ttu-id="55b6f-181">ドロップ ダイアログには、次の項目は**ありません**:</span><span class="sxs-lookup"><span data-stu-id="55b6f-181">A Drop dialog should **not** have the following:</span></span>

-   <span data-ttu-id="55b6f-182">ドロップ ダイアログのツールバーまたは ActionPane の任意の場所。</span><span class="sxs-lookup"><span data-stu-id="55b6f-182">A toolbar or ActionPane anywhere in the Drop dialog.</span></span>
-   <span data-ttu-id="55b6f-183">別のページに移動するか、他のダイアログを開くボタン。</span><span class="sxs-lookup"><span data-stu-id="55b6f-183">Buttons that navigate to another page or open other dialogs.</span></span> <span data-ttu-id="55b6f-184">(拡張プレビューを使用できます。)</span><span class="sxs-lookup"><span data-stu-id="55b6f-184">(Enhanced previews are allowed.)</span></span>
-   <span data-ttu-id="55b6f-185">フィールド グループ。</span><span class="sxs-lookup"><span data-stu-id="55b6f-185">Field groups.</span></span> <span data-ttu-id="55b6f-186">ラジオ ボタンやチェック ボックス グループなどの例外があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-186">There are exceptions, such as a radio button or check box group.</span></span>
-   <span data-ttu-id="55b6f-187">タブ コントロール。</span><span class="sxs-lookup"><span data-stu-id="55b6f-187">A tab control.</span></span>
-   <span data-ttu-id="55b6f-188">情報ボックス。</span><span class="sxs-lookup"><span data-stu-id="55b6f-188">FactBoxes.</span></span>
-   <span data-ttu-id="55b6f-189">FastTabs。</span><span class="sxs-lookup"><span data-stu-id="55b6f-189">FastTabs.</span></span>

## <a name="examples"></a><span data-ttu-id="55b6f-190">例</span><span class="sxs-lookup"><span data-stu-id="55b6f-190">Examples</span></span>
### <a name="drop-dialog-basic"></a><span data-ttu-id="55b6f-191">ドロップ ダイアログ (basic)</span><span class="sxs-lookup"><span data-stu-id="55b6f-191">Drop dialog (basic)</span></span>

<span data-ttu-id="55b6f-192">Form: **CustCollectionsNewActivityAction** (**売掛金勘定** &gt; **共通** &gt; **コレクション** &gt; **コレクション**の順にクリックし、詳細に移動する行を選択し、**アクション**をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="55b6f-192">Form: **CustCollectionsNewActivityAction** (Click **Accounts receivable** &gt; **Common** &gt; **Collections** &gt; **Collections**, select a row to move to details, and then click **Action**.)</span></span> 

<span data-ttu-id="55b6f-193">[![DropDialog(3)](./media/dropdialog3.png)](./media/dropdialog3.png)</span><span class="sxs-lookup"><span data-stu-id="55b6f-193">[![DropDialog(3)](./media/dropdialog3.png)](./media/dropdialog3.png)</span></span>

### <a name="drop-dialog-read-only"></a><span data-ttu-id="55b6f-194">ドロップ ダイアログ (読み取り専用)</span><span class="sxs-lookup"><span data-stu-id="55b6f-194">Drop dialog (read only)</span></span>

<span data-ttu-id="55b6f-195">このパターンは現在製品で使用されていません。</span><span class="sxs-lookup"><span data-stu-id="55b6f-195">This pattern isn't currently used in the product.</span></span>

## <a name="appendix"></a><span data-ttu-id="55b6f-196">付録</span><span class="sxs-lookup"><span data-stu-id="55b6f-196">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="55b6f-197">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="55b6f-197">Frequently asked questions</span></span>

<span data-ttu-id="55b6f-198">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-198">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="55b6f-199">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="55b6f-199">Open issues</span></span>

-   <span data-ttu-id="55b6f-200">**垂直フィールドおよびフィールド グループのサブパターン はドロップ ダイアログに追加する必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="55b6f-200">**Should a vertical Fields and Field Groups subpattern be added for Drop dialogs?**</span></span>
    -   <span data-ttu-id="55b6f-201">いいえ、通常のフィールドおよびフィールド グループのパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55b6f-201">No, you should use the normal Fields and Field Groups pattern.</span></span>
-   <span data-ttu-id="55b6f-202">**ボタンは左揃えまたは右揃えにすべきですか。**</span><span class="sxs-lookup"><span data-stu-id="55b6f-202">**Should buttons be left-aligned or right-aligned?**</span></span>
    -   <span data-ttu-id="55b6f-203">右揃え。</span><span class="sxs-lookup"><span data-stu-id="55b6f-203">Right-aligned.</span></span> <span data-ttu-id="55b6f-204">パターンは現在はこれを実施しています。</span><span class="sxs-lookup"><span data-stu-id="55b6f-204">The pattern is currently enforcing this.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="55b6f-205">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="55b6f-205">AX 2012 content</span></span>

<span data-ttu-id="55b6f-206">[![DropDialog(4)](./media/dropdialog4.png)](./media/dropdialog4.png)</span><span class="sxs-lookup"><span data-stu-id="55b6f-206">[![DropDialog(4)](./media/dropdialog4.png)](./media/dropdialog4.png)</span></span>
