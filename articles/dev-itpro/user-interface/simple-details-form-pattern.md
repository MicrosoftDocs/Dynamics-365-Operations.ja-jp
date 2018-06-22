---
title: "簡易詳細のフォーム パターン"
description: "この記事では、簡易詳細のフォーム パターンについて説明します。 このパターンは、フィールドの単純なセットだけがユーザーに提示されなければならない場合に使用されます。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 14791
ms.assetid: ee67618d-edc8-4bc5-bccc-6872c4af6273
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cd0c9a87781c618e90de24e23914d8aa0ffd1ebf
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="simple-details-form-pattern"></a><span data-ttu-id="17b5c-104">簡易詳細のフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="17b5c-104">Simple Details form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17b5c-105">この記事では、簡易詳細のフォーム パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="17b5c-105">This article describes the Simple Details form pattern.</span></span> <span data-ttu-id="17b5c-106">このパターンは、フィールドの単純なセットだけがユーザーに提示されなければならない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-106">This pattern is used when only a simple set of fields must be presented to the user.</span></span>

<a name="usage"></a><span data-ttu-id="17b5c-107">用途</span><span class="sxs-lookup"><span data-stu-id="17b5c-107">Usage</span></span>
-----

<span data-ttu-id="17b5c-108">簡易詳細パターンは、フィールドの単純なセットだけがユーザーに提示されなければならない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-108">The Simple Details pattern is used when only a simple set of fields must be presented to the user.</span></span> <span data-ttu-id="17b5c-109">例には、合計および顧客残高の表示が含まれます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-109">Examples include the display of totals and customer balances.</span></span> <span data-ttu-id="17b5c-110">通常、シンプル・ディテール・パターンではビュー・モードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-110">Typically, view mode is used for the Simple Details pattern.</span></span> <span data-ttu-id="17b5c-111">ただし、フォームが編集可能な情報を提供する場合、編集モードは親フォームに同期される必要があります。</span><span class="sxs-lookup"><span data-stu-id="17b5c-111">However, in cases where the form provides editable information, the edit mode should be synced to the parent form.</span></span> <span data-ttu-id="17b5c-112">このドキュメントでは、4 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="17b5c-112">Four patterns are described in this document:</span></span>

-   <span data-ttu-id="17b5c-113">**ツールバーおよびフィールド付き簡易詳細** – これは基本の簡易詳細パターンで、複数のフィールドがこのフォームで表示されます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-113">**Simple Details w/Toolbar and Fields** – This is the basic Simple Details pattern, in which several fields are displayed in the form.</span></span> <span data-ttu-id="17b5c-114">これらのフィールドは、オプションでグループ内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-114">The fields can optionally appear inside Groups.</span></span>
-   <span data-ttu-id="17b5c-115">**クイック タブ付き簡易詳細** – これは、フィールドがクイック タブに編成されているときに使用する簡易詳細パターンです。</span><span class="sxs-lookup"><span data-stu-id="17b5c-115">**Simple Details w/Fast Tabs** – This is the Simple Details pattern that should be used when fields are organized into FastTabs.</span></span>
-   <span data-ttu-id="17b5c-116">**標準タブ付き簡易詳細** – これは、フィールドが標準タブに編成されているときに使用する簡易詳細パターンです。</span><span class="sxs-lookup"><span data-stu-id="17b5c-116">**Simple Details w/Standard Tabs** – This is the Simple Details pattern that should be used when fields are organized into traditional tabs.</span></span>
-   <span data-ttu-id="17b5c-117">**パノラマ付き簡易詳細** – これは、情報がパノラマ形式で表示されることを意図された情報の場合に使用する簡易詳細パターンです。</span><span class="sxs-lookup"><span data-stu-id="17b5c-117">**Simple Details w/Panorama** – This is the Simple Details pattern that should be used when information is intended to be displayed in a panorama format.</span></span>

## <a name="wireframe"></a><span data-ttu-id="17b5c-118">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="17b5c-118">Wireframe</span></span>

<span data-ttu-id="17b5c-119">[![ワイヤーフレーム](./media/simpledetails1-1024x578.png)](./media/simpledetails1.png)</span><span class="sxs-lookup"><span data-stu-id="17b5c-119">[![Wireframe](./media/simpledetails1-1024x578.png)](./media/simpledetails1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="17b5c-120">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="17b5c-120">Pattern changes</span></span>
<span data-ttu-id="17b5c-121">現在のバージョンの Microsoft Dynamics AX にこのパターンを使用するための計画された変更はありません。</span><span class="sxs-lookup"><span data-stu-id="17b5c-121">There are no planned changes for the use of this pattern in the current version of Microsoft Dynamics AX.</span></span>

## <a name="model"></a><span data-ttu-id="17b5c-122">モデル</span><span class="sxs-lookup"><span data-stu-id="17b5c-122">Model</span></span>
### <a name="simple-details-wtoolbar-and-fields--high-level-structure"></a><span data-ttu-id="17b5c-123">ツール バーおよびフィールド付き簡易詳細: 高度レベル構造</span><span class="sxs-lookup"><span data-stu-id="17b5c-123">Simple Details w/Toolbar and Fields – High-level structure</span></span>

- <span data-ttu-id="17b5c-124">デザイン</span><span class="sxs-lookup"><span data-stu-id="17b5c-124">Design</span></span>

    - <span data-ttu-id="17b5c-125">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="17b5c-125">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="17b5c-126">本文 (グループ) – **注記:** フィールドのサブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-126">Body (Group) – **Note:** A field subpattern is used.</span></span>

### <a name="simple-details-wfasttabs--high-level-structure"></a><span data-ttu-id="17b5c-127">クイック タブ付き簡易詳細 – 高レベル構造</span><span class="sxs-lookup"><span data-stu-id="17b5c-127">Simple Details w/FastTabs – High-level structure</span></span>

- <span data-ttu-id="17b5c-128">デザイン</span><span class="sxs-lookup"><span data-stu-id="17b5c-128">Design</span></span>

    - <span data-ttu-id="17b5c-129">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="17b5c-129">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="17b5c-130">*HeaderGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="17b5c-130">*HeaderGroup (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="17b5c-131">本文 (タブ、Style=FastTabs)</span><span class="sxs-lookup"><span data-stu-id="17b5c-131">Body (Tab, Style=FastTabs)</span></span>

        - <span data-ttu-id="17b5c-132">BodyTabPages (TabPage 反復 1..N)</span><span class="sxs-lookup"><span data-stu-id="17b5c-132">BodyTabPages (TabPage repeats 1..N)</span></span>

    - <span data-ttu-id="17b5c-133">*FooterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="17b5c-133">*FooterGroup (Group) \[Optional\]*</span></span>

### <a name="simple-details-wstandard-tabs--high-level-structure"></a><span data-ttu-id="17b5c-134">標準タブ付き簡易詳細 – 高レベル構造</span><span class="sxs-lookup"><span data-stu-id="17b5c-134">Simple Details w/Standard Tabs – High-level structure</span></span>

- <span data-ttu-id="17b5c-135">デザイン</span><span class="sxs-lookup"><span data-stu-id="17b5c-135">Design</span></span>

    - <span data-ttu-id="17b5c-136">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="17b5c-136">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="17b5c-137">*HeaderGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="17b5c-137">*HeaderGroup (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="17b5c-138">本文 (タブ、Style=Tabs)</span><span class="sxs-lookup"><span data-stu-id="17b5c-138">Body (Tab, Style=Tabs)</span></span>

        - <span data-ttu-id="17b5c-139">BodyTabPages (TabPage 反復 1..N)</span><span class="sxs-lookup"><span data-stu-id="17b5c-139">BodyTabPages (TabPage repeats 1..N)</span></span>

    - <span data-ttu-id="17b5c-140">*FooterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="17b5c-140">*FooterGroup (Group) \[Optional\]*</span></span>

### <a name="simple-details-wpanorama--high-level-structure"></a><span data-ttu-id="17b5c-141">パノラマ付き簡易詳細 – 高レベル構造</span><span class="sxs-lookup"><span data-stu-id="17b5c-141">Simple Details w/Panorama – High-level structure</span></span>

- <span data-ttu-id="17b5c-142">デザイン</span><span class="sxs-lookup"><span data-stu-id="17b5c-142">Design</span></span>

    - <span data-ttu-id="17b5c-143">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="17b5c-143">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="17b5c-144">本文 (タブ、Style=Panorama)</span><span class="sxs-lookup"><span data-stu-id="17b5c-144">Body (Tab, Style=Panorama)</span></span>

        - <span data-ttu-id="17b5c-145">BodyTabPages (TabPage 反復 1..N)</span><span class="sxs-lookup"><span data-stu-id="17b5c-145">BodyTabPages (TabPage repeats 1..N)</span></span>

    - <span data-ttu-id="17b5c-146">*FooterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="17b5c-146">*FooterGroup (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="17b5c-147">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="17b5c-147">Core components</span></span>

1.  <span data-ttu-id="17b5c-148">**Form.Design** に SimpleDetails パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="17b5c-148">Apply the SimpleDetails pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="17b5c-149">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="17b5c-149">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="17b5c-150">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="17b5c-150">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="17b5c-151">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="17b5c-151">The form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="17b5c-152">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="17b5c-152">**TabPage.Caption** isn't empty.</span></span>
    4.  <span data-ttu-id="17b5c-153">MainMenu に、SimpleDetails フォームを参照するメニュー項目を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="17b5c-153">MainMenu must not contain menu items that reference a SimpleDetails form.</span></span>

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="17b5c-154">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="17b5c-154">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="17b5c-155">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="17b5c-155">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="17b5c-156">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="17b5c-156">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   [<span data-ttu-id="17b5c-157">表形式フィールド</span><span class="sxs-lookup"><span data-stu-id="17b5c-157">Tabular Fields</span></span>](tabular-fields-subpattern.md)
-   [<span data-ttu-id="17b5c-158">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="17b5c-158">Toolbar and List</span></span>](toolbar-list-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="17b5c-159">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="17b5c-159">UX guidelines</span></span>
<span data-ttu-id="17b5c-160">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="17b5c-160">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="17b5c-161">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="17b5c-161">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="17b5c-162">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="17b5c-162">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="17b5c-163">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="17b5c-163">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="17b5c-164">標準フォーム ガイドラインは、Dynamics AX の[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="17b5c-164">Standard form guidelines have been consolidated into the Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="17b5c-165">**簡易詳細** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="17b5c-165">**Simple Details** **guidelines:**</span></span>

-   <span data-ttu-id="17b5c-166">フォーム ページには、エンティティを正確に説明するフォーム キャプションが表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="17b5c-166">The form page should display a Form Caption that accurately describes the entity.</span></span>
    -   <span data-ttu-id="17b5c-167">フォーム キャプションは、単数形にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17b5c-167">The Form Caption should be in a singular form.</span></span>

## <a name="examples"></a><span data-ttu-id="17b5c-168">例</span><span class="sxs-lookup"><span data-stu-id="17b5c-168">Examples</span></span>
### <a name="simple-details-wtoolbar-and-fields"></a><span data-ttu-id="17b5c-169">ツール バーおよびフィールド付き簡易詳細</span><span class="sxs-lookup"><span data-stu-id="17b5c-169">Simple Details w/Toolbar and Fields</span></span>

<span data-ttu-id="17b5c-170">フォーム: **AgreementLine**</span><span class="sxs-lookup"><span data-stu-id="17b5c-170">Form: **AgreementLine**</span></span> 

<span data-ttu-id="17b5c-171">[![ツールバーおよびフィールド付き簡易詳細](./media/simpledetails2-1024x688.png)](./media/simpledetails2.png)</span><span class="sxs-lookup"><span data-stu-id="17b5c-171">[![Simple Details w/Toolbar and Fields](./media/simpledetails2-1024x688.png)](./media/simpledetails2.png)</span></span>

### <a name="simple-details-wfasttabs"></a><span data-ttu-id="17b5c-172">クイック タブ付き簡易詳細</span><span class="sxs-lookup"><span data-stu-id="17b5c-172">Simple Details w/FastTabs</span></span>

<span data-ttu-id="17b5c-173">フォーム: **PlanActivityServiceDetails**</span><span class="sxs-lookup"><span data-stu-id="17b5c-173">Form: **PlanActivityServiceDetails**</span></span> 

<span data-ttu-id="17b5c-174">[![クイック タブ付き簡易詳細](./media/simpledetails3-1024x587.png)](./media/simpledetails3.png)</span><span class="sxs-lookup"><span data-stu-id="17b5c-174">[![Simple Details w/FastTab](./media/simpledetails3-1024x587.png)](./media/simpledetails3.png)</span></span>

### <a name="simple-details-wstandard-tabs"></a><span data-ttu-id="17b5c-175">標準タブ付き簡易詳細</span><span class="sxs-lookup"><span data-stu-id="17b5c-175">Simple Details w/Standard Tabs</span></span>

<span data-ttu-id="17b5c-176">フォーム: **HcmEmploymentDateManager** (**人事管理** &gt; **共通** &gt; **作業者** &gt; **作業者**の順にクリックし、**一般** &gt; **バージョン** &gt; **職歴**の順にクリックし、それから**日付マネージャー**をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="17b5c-176">Form: **HcmEmploymentDateManager** (Click **Human Resources** &gt; **Common** &gt; **Workers** &gt; **Workers**, click **General** &gt; **Versions** &gt; **Employment History**, and then click **Date Manager**.)</span></span> 

<span data-ttu-id="17b5c-177">[![標準タブ付き簡易詳細](./media/simpledetails4-1024x588.png)](./media/simpledetails4.png)</span><span class="sxs-lookup"><span data-stu-id="17b5c-177">[![Simple Details w/Standard Tabs](./media/simpledetails4-1024x588.png)](./media/simpledetails4.png)</span></span>

### <a name="simple-details-wpanorama"></a><span data-ttu-id="17b5c-178">パノラマ付き簡易詳細</span><span class="sxs-lookup"><span data-stu-id="17b5c-178">Simple Details w/Panorama</span></span>

<span data-ttu-id="17b5c-179">フォーム: **PdsMRCEventTracker**</span><span class="sxs-lookup"><span data-stu-id="17b5c-179">Form: **PdsMRCEventTracker**</span></span> 

<span data-ttu-id="17b5c-180">[![パノラマ付き簡易詳細](./media/simpledetails5-1024x510.png)](./media/simpledetails5.png)</span><span class="sxs-lookup"><span data-stu-id="17b5c-180">[![Simple Details w/Panorama](./media/simpledetails5-1024x510.png)](./media/simpledetails5.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="17b5c-181">付録</span><span class="sxs-lookup"><span data-stu-id="17b5c-181">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="17b5c-182">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="17b5c-182">Frequently asked questions</span></span>

<span data-ttu-id="17b5c-183">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="17b5c-183">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="17b5c-184">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="17b5c-184">Open issues</span></span>

-   <span data-ttu-id="17b5c-185">少量の関連するコンテンツを表示する簡易詳細のフォームに、全ページ フォーム以外のプレゼンテーションを設ける必要があるかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="17b5c-185">Investigate whether Simple Details forms that show a small amount of related content should have a different presentation than a full-page form.</span></span>
