---
title: "カスタム パターンを使用したテスト フォーム"
description: "このトピックでは、カスタム パターンを使用してフォームをテストする方法について説明します。"
author: jasongre
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 28291
ms.assetid: 2245dd9f-7ef7-46cc-9e1b-e00fc66526ec
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 81acea25b6e502bc3cbe6e8c8fd280eb03539cf5
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="test-forms-that-use-custom-patterns"></a><span data-ttu-id="83422-103">カスタム パターンを使用したテスト フォーム</span><span class="sxs-lookup"><span data-stu-id="83422-103">Test forms that use custom patterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83422-104">このトピックでは、カスタム パターンを使用してフォームをテストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="83422-104">This topic how to test forms using custom patterns.</span></span>

<a name="introduction"></a><span data-ttu-id="83422-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="83422-105">Introduction</span></span>
------------

<span data-ttu-id="83422-106">フォーム パターンに従うことによって、さまざまなメリットが得られます。</span><span class="sxs-lookup"><span data-stu-id="83422-106">By adhering to form patterns, you gain various benefits.</span></span> <span data-ttu-id="83422-107">たとえば、フォームのパターンは正しくレイアウト プロパティを設定して、フォームが応答しやすいように配置されます。</span><span class="sxs-lookup"><span data-stu-id="83422-107">For example, form patterns correctly set layout properties so that forms are laid out responsively.</span></span> <span data-ttu-id="83422-108">ただし、フォーム パターンの補充が欠落している場合 (たとえば、現在多くの拡張コントロールのサポートがない場合)、またはフォームまたはコンテナーに任意のパターンに適合しない固有の要件/用途がある場合、開発者はカスタムにパターンを設定できます。</span><span class="sxs-lookup"><span data-stu-id="83422-108">However, when form pattern coverage is lacking (for example, there currently isn't support for many extensible controls), or when a form or container has unique requirements/uses that don't fit any pattern, developers can set the pattern to Custom.</span></span> <span data-ttu-id="83422-109">開発者は、正しい、応答フォーム レイアウトを作成する責任を負います。</span><span class="sxs-lookup"><span data-stu-id="83422-109">The developer then becomes responsible for ensuring a correct and responsive form layout.</span></span>

## <a name="forms-that-use-custom-patterns"></a><span data-ttu-id="83422-110">カスタム パターンを使用したフォーム</span><span class="sxs-lookup"><span data-stu-id="83422-110">Forms that use custom patterns</span></span>
<span data-ttu-id="83422-111">カスタム パターンを使用するフォームは、**フォーム パターン** レポートを使用することにより見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="83422-111">You can find the forms that use custom patterns by using the **Form Patterns** report.</span></span> <span data-ttu-id="83422-112">レポートを実行する詳細については、[フォーム パターン アドイン](form-pattern-add-ins.md) を参照してください。レポートを実行した後、**パーセンテージ補充されるコントロール**列をフィルター処理して 100% 補充より少ないフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="83422-112">For information on running the report, see [Form pattern add-ins](form-pattern-add-ins.md). After running the report, filter the **Percent covered controls** column to show forms that have less than 100-percent coverage.</span></span> <span data-ttu-id="83422-113">最上位レベルのカスタム パターンを持つフォームについては、**カスタム**が**パターン**列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="83422-113">For forms that have a top-level Custom pattern, **Custom** will appear in the **Patterns** column.</span></span> 

## <a name="testing-configurations"></a><span data-ttu-id="83422-114">コンフィギュレーションのテスト</span><span class="sxs-lookup"><span data-stu-id="83422-114">Testing configurations</span></span>
### <a name="key-resolution"></a><span data-ttu-id="83422-115">キー ソリューション</span><span class="sxs-lookup"><span data-stu-id="83422-115">Key resolution</span></span>

-   <span data-ttu-id="83422-116">1366 × 768 は、画面サイズが 12 ～ 23 インチの標準的な解像度です。</span><span class="sxs-lookup"><span data-stu-id="83422-116">1366 × 768 is a typical resolution on screen sizes that are between 12 and 23 inches.</span></span> <span data-ttu-id="83422-117">したがって、この解決策はテストのための良いベースラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="83422-117">Therefore, this resolution provides a good baseline for testing.</span></span>
-   <span data-ttu-id="83422-118">1920 × 1080 など高解像度でもテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="83422-118">It's also a good idea to test on a higher resolution, such as 1920 × 1080.</span></span>

### <a name="parameters"></a><span data-ttu-id="83422-119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83422-119">Parameters</span></span>

-   <span data-ttu-id="83422-120">ブラウザー</span><span class="sxs-lookup"><span data-stu-id="83422-120">Browser</span></span>
    -   <span data-ttu-id="83422-121">Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="83422-121">Internet Explorer 11</span></span>
    -   <span data-ttu-id="83422-122">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="83422-122">Google Chrome</span></span>
    -   <span data-ttu-id="83422-123">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="83422-123">Microsoft Edge</span></span>
    -   <span data-ttu-id="83422-124">Apple Safari (iPad) – Safari でクラウド URL を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83422-124">Apple Safari (on iPad) – You'll have to point Safari to a cloud URL.</span></span>
        -   <span data-ttu-id="83422-125">ランドスケープおよびポートレート モード</span><span class="sxs-lookup"><span data-stu-id="83422-125">Landscape and portrait modes</span></span>
-   <span data-ttu-id="83422-126">密度</span><span class="sxs-lookup"><span data-stu-id="83422-126">Density</span></span>
    -   <span data-ttu-id="83422-127">低密度</span><span class="sxs-lookup"><span data-stu-id="83422-127">Low density</span></span>
    -   <span data-ttu-id="83422-128">高密度</span><span class="sxs-lookup"><span data-stu-id="83422-128">High density</span></span>
-   <span data-ttu-id="83422-129">ビューポートのサイズ</span><span class="sxs-lookup"><span data-stu-id="83422-129">Viewport size</span></span>
    -   <span data-ttu-id="83422-130">最大化されたウィンドウ</span><span class="sxs-lookup"><span data-stu-id="83422-130">Maximized window</span></span>
    -   <span data-ttu-id="83422-131">タブレットで縦モードをシミュレートするスナップ ビュー (画面の半分)</span><span class="sxs-lookup"><span data-stu-id="83422-131">Snap view (half the screen) to simulate portrait mode on a tablet</span></span>
-   <span data-ttu-id="83422-132">ズーム</span><span class="sxs-lookup"><span data-stu-id="83422-132">Zoom</span></span>
    -   <span data-ttu-id="83422-133">50 ～ 200 パーセント</span><span class="sxs-lookup"><span data-stu-id="83422-133">50 to 200 percent</span></span>

### <a name="steps"></a><span data-ttu-id="83422-134">ステップ</span><span class="sxs-lookup"><span data-stu-id="83422-134">Steps</span></span>

<span data-ttu-id="83422-135">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83422-135">Follow these steps.</span></span> <span data-ttu-id="83422-136">各ステップで、フォームのレイアウトの問題を確認します。</span><span class="sxs-lookup"><span data-stu-id="83422-136">At each step, examine your form for layout issues.</span></span> <span data-ttu-id="83422-137">検証の一環として、すべてのタブ ページ、および展開/折りたたみコンテンツのグループを確認します。</span><span class="sxs-lookup"><span data-stu-id="83422-137">As part of your examination, look at all tab pages, and any groups that can expand/collapse content.</span></span>

1.  <span data-ttu-id="83422-138">全画面のサイズでブラウザー ウィンドウを開き、(低密度で) フォーム/コントロールへ移動します。</span><span class="sxs-lookup"><span data-stu-id="83422-138">Open a browser window at full-screen size, and navigate to your form/control (in low density).</span></span> <span data-ttu-id="83422-139">1366 × 768 の解像度でテストを開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="83422-139">It's a good idea to starting your testing at a resolution of 1366 × 768.</span></span>
2.  <span data-ttu-id="83422-140">Windows ログ キー + 左方向キーを押し、ブラウザー ウィンドウをスナップ ビューに切り替えます (画面の半分)。</span><span class="sxs-lookup"><span data-stu-id="83422-140">Press the Windows log key+Left Arrow to switch the browser window to Snap view (half the screen).</span></span>
3.  <span data-ttu-id="83422-141">ブラウザーを横幅最大までゆっくりと横方向にサイズ変更します。</span><span class="sxs-lookup"><span data-stu-id="83422-141">Slowly resize the browser horizontally back to full width.</span></span> <span data-ttu-id="83422-142">ときどき停止して、フォーム レイアウトを評価します。</span><span class="sxs-lookup"><span data-stu-id="83422-142">Stop at intervals, and evaluate the form layout.</span></span>
4.  <span data-ttu-id="83422-143">ブラウザーを高さ最大から画面の半分の高さまでゆっくりと縦方向にサイズ変更します。</span><span class="sxs-lookup"><span data-stu-id="83422-143">Slowly resize the browser vertically from full height to half-screen height.</span></span> <span data-ttu-id="83422-144">ときどき停止して、フォーム レイアウトを評価します。</span><span class="sxs-lookup"><span data-stu-id="83422-144">Stop at intervals, and evaluate the form layout.</span></span>
5.  <span data-ttu-id="83422-145">ブラウザー ウィンドウを全画面のサイズに最大化します。</span><span class="sxs-lookup"><span data-stu-id="83422-145">Maximize the browser window to full-screen size.</span></span> <span data-ttu-id="83422-146">ズーム レベル (50%、75%、125%、150% および 200%) を調整し、フォーム レイアウトを評価します。</span><span class="sxs-lookup"><span data-stu-id="83422-146">Adjust the zoom levels (50 percent, 75 percent, 125 percent, 150 percent, and 200 percent), and evaluate the form layout.</span></span>
6.  <span data-ttu-id="83422-147">高密度でサニティ チェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="83422-147">Do a sanity check in high density.</span></span>
7.  <span data-ttu-id="83422-148">他のブラウザでサニティ チェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="83422-148">Do a sanity check in other browsers.</span></span>

## <a name="visual-issues-that-you-might-encounter"></a><span data-ttu-id="83422-149">遭遇する可能性のある視覚的な問題</span><span class="sxs-lookup"><span data-stu-id="83422-149">Visual issues that you might encounter</span></span>
### <a name="questions-to-answer-while-youre-testing"></a><span data-ttu-id="83422-150">テストしている間に答える質問</span><span class="sxs-lookup"><span data-stu-id="83422-150">Questions to answer while you're testing</span></span>

-   <span data-ttu-id="83422-151">フォームは使用可能ですか。</span><span class="sxs-lookup"><span data-stu-id="83422-151">Is the form usable?</span></span>
-   <span data-ttu-id="83422-152">フォームのすべてにアクセスできますか。</span><span class="sxs-lookup"><span data-stu-id="83422-152">Can I reach everything on the form?</span></span> <span data-ttu-id="83422-153">(小規模なビューポートで複数のスクロール バーを移動する必要が生じる場合があります。)</span><span class="sxs-lookup"><span data-stu-id="83422-153">(You might have to move multiple scrollbars in smaller viewports.)</span></span>

### <a name="issues-that-might-suggest-problems-with-the-layout-metadata"></a><span data-ttu-id="83422-154">レイアウト メタデータに関する問題を示す問題</span><span class="sxs-lookup"><span data-stu-id="83422-154">Issues that might suggest problems with the layout metadata</span></span>

-   <span data-ttu-id="83422-155">フォームの内容は、使用可能な領域に基づいて調整されていません。</span><span class="sxs-lookup"><span data-stu-id="83422-155">Form content isn't being adjusted based on the available space.</span></span>
-   <span data-ttu-id="83422-156">グリッドおよびその他の「塗りつぶし」コントロールは、完全な高さと幅を占有しません。</span><span class="sxs-lookup"><span data-stu-id="83422-156">Grids and other “fill” controls aren't taking up the full height/width.</span></span>
-   <span data-ttu-id="83422-157">コンテナーはまったく表示されません (フォームの一部にアクセスするためのスクロールバーはありません)。</span><span class="sxs-lookup"><span data-stu-id="83422-157">Containers aren't showing up at all (there are no scrollbars that you can use to get to parts of the form).</span></span>
    -   <span data-ttu-id="83422-158">この問題は、使用可能な高さ/幅がない場合、**SizeToAvailable** コンテナーで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="83422-158">This issue can occur with **SizeToAvailable** containers when there is no available height/width.</span></span>
-   <span data-ttu-id="83422-159">予備の (不要な) スクロール バーがあります。</span><span class="sxs-lookup"><span data-stu-id="83422-159">There are extra (unnecessary) scrollbars.</span></span>
    -   <span data-ttu-id="83422-160">特に一部のコンテナー (グリッドやタブ ページなど) では、高さが最小であるために、小規模のビューポートでスクロール バーが多くなることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="83422-160">You should expect more scrollbars in smaller viewports, especially because some containers (for example, grids and tab pages) have a minimum height.</span></span>
    -   <span data-ttu-id="83422-161">この問題は、**SizeToAvailable** でなければならない **SizeToContent** コンテナーで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="83422-161">This issue can occur with **SizeToContent** containers that should be **SizeToAvailable**.</span></span>

### <a name="other-knownexpected-issues"></a><span data-ttu-id="83422-162">その他の既知の/正常な問題</span><span class="sxs-lookup"><span data-stu-id="83422-162">Other known/expected issues</span></span>

-   <span data-ttu-id="83422-163">ツールバーに水平スクロール バーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83422-163">Horizontal scrollbars appear on Toolbars.</span></span>
    -   <span data-ttu-id="83422-164">ツールバー上のすべてのボタンを表示するだけの十分な幅がない場合、水平スクロール バーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83422-164">Where there isn't enough width to show all the buttons on a Toolbar, a horizontal scrollbar will appear.</span></span> <span data-ttu-id="83422-165">この問題は、ツールバーのオーバーフロー動作を展開するフレームワークの配送によってすぐに解決されます。</span><span class="sxs-lookup"><span data-stu-id="83422-165">This issue will be resolved soon by a framework deliverable that will implement overflow behavior on Toolbars.</span></span>
-   <span data-ttu-id="83422-166">ランダム入力コントロールの境界線が、さまざまなズーム レベルで欠落しています。</span><span class="sxs-lookup"><span data-stu-id="83422-166">Random input control borders are missing at various zoom levels.</span></span>
    -   <span data-ttu-id="83422-167">これは、既知の問題であり、1721990 で追跡されます。</span><span class="sxs-lookup"><span data-stu-id="83422-167">This is a known issue and is tracked by 1721990.</span></span>
-   <span data-ttu-id="83422-168">グリッドで利用可能な領域がグリッドの高さの最小値 (200 ピクセル) よりも少ないため、グリッドは追加のスクロール バーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="83422-168">Grids receive extra scrollbars, because the space that is available for the grid is less than the grid's minimum height (200 px).</span></span>
    -   <span data-ttu-id="83422-169">この最小高さの縮小/除去を調査するための今後の作業項目があります。</span><span class="sxs-lookup"><span data-stu-id="83422-169">We have a future work item to investigate reducing/removing this minimum height.</span></span>
-   <span data-ttu-id="83422-170">**SizeToAvailable** 幅の StaticText コントロールが同じ **SizeToAvailable** 幅のグループ内にあるときは、水平スクロール バーがある幅で表示されます (Internet Explorer のみ)。</span><span class="sxs-lookup"><span data-stu-id="83422-170">When StaticText controls that have **SizeToAvailable** width are inside a group that also has **SizeToAvailable** width, horizontal scrollbars appear at some widths (Internet Explorer only).</span></span>
    -   <span data-ttu-id="83422-171">ブラウザーには、このシナリオでスクロールバーが表示される原因となる計算エラーがあります。</span><span class="sxs-lookup"><span data-stu-id="83422-171">The browser has a calculation error that sometimes causes scrollbars to appear in this scenario.</span></span>

## <a name="appendix"></a><span data-ttu-id="83422-172">付録</span><span class="sxs-lookup"><span data-stu-id="83422-172">Appendix</span></span>
### <a name="informationguidelines-about-layout"></a><span data-ttu-id="83422-173">レイアウトに関する情報/ガイドライン</span><span class="sxs-lookup"><span data-stu-id="83422-173">Information/guidelines about layout</span></span>

<span data-ttu-id="83422-174">レイアウトのプロパティに関する情報、および避ける必要があるシナリオに関するガイドラインについては、[ページ レイアウト](page-layout.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83422-174">For information about the layout properties, and for guidelines about scenarios that you should avoid, see [Page layout](page-layout.md).</span></span>




