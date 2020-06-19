---
title: CSS 上書きファイルの作業
description: このトピックでは、Microsoft Dynamics 365 Commerce のカスケード スタイル シート (CSS) 上書きファイルを使用する理由、タイミング、および方法について説明します。
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411250"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="1e0e1-103">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="1e0e1-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1e0e1-104">このトピックでは、Microsoft Dynamics 365 Commerce のカスケード スタイル シート (CSS) 上書きファイルを使用する理由、タイミング、および方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1e0e1-105">概要</span><span class="sxs-lookup"><span data-stu-id="1e0e1-105">Overview</span></span>

<span data-ttu-id="1e0e1-106">通常、永続的なサイト スタイルは、サイトのテーマを通じて処理される必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="1e0e1-107">テーマでは、サイトの任意のページにあるモジュールの基本的な CSS およびスタイル設定を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="1e0e1-108">テーマは Dynamics 365 Commerce オンライン ソフトウェア開発キット (SDK) を使用して作成され、Microsoft Dynamics Lifecycle Services (LCS) を通じて Web サイトに配置されます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1e0e1-109">SDK のテーマ デバッグ機能およびモジュール インターフェイス コンフィギュレーションは、サイト開発者がカスタマイズ可能でまとまりのあるサイト デザイン パッケージを作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="1e0e1-110">これらのデザイン パッケージをサイトに配置すると、サイト作成者はサイト開発の代わりにコンテンツの作成、編集、公開に焦点を合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="1e0e1-111">テーマの通常のライフサイクルの場合、SDK と LCS の展開パイプラインを使用してスタイルを変更する開発者への依存は、一部のシナリオでは禁止されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="1e0e1-112">サイトのプロトタイプまたは修正プログラムは、SDK がコンフィギュレーションされていない場合、または LCS 展開を待つ時間がない場合には煩雑に感じることがあります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="1e0e1-113">これらのシナリオでは、CSS 上書きファイルが役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="1e0e1-114">コマース作成ツールでは、認証されたユーザーが CSS ファイルをアップロードし、確認してから、それを有効にしてサイト テーマを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="1e0e1-115">SDK または LCS 展開のオーバーヘッドは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="1e0e1-116">CSS 上書きファイルで指定された上書きは、単一のテキスト スタイルへの変更と同じくらい小さい場合もあれば、完全なブランド オーバーホールと同じくらい広範囲の場合もあります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="1e0e1-117">CSS 上書きファイルを使用する前に、次の制限事項に注意してください。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="1e0e1-118">1 つのサイトで一度に有効化できるのは、1 つの CSS 上書きファイルのみです。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="1e0e1-119">したがって、すべての有効な上書きが単一の上書きファイルに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="1e0e1-120">コマース作成ツールでは上書きを確認できますが、上書きによって導入される任意のバグを特定するのに役立つ専用のデバッグ機能はありません。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="1e0e1-121">つまり、CSS 上書きファイルを使用する場合、SDK がモジュールと作成検証に対して提供する同じツールセットはありません。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="1e0e1-122">ただし、CSS 上書きファイルは、完全なテーマの更新が開発および展開される前に、デザインのプロトタイプを作成したり、修正プログラムを実装したりする迅速な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="1e0e1-123">CSS 上書きファイルの作成</span><span class="sxs-lookup"><span data-stu-id="1e0e1-123">Create a CSS override file</span></span>

<span data-ttu-id="1e0e1-124">CSS 上書きファイルを作成するには、任意の統合開発環境 (IDE)、テキスト エディター、またはソース コード エディターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="1e0e1-125">一般的なアプローチとして、ブラウザーで標準の Web デバッガーを使用して、既存のサイトのスタイル セレクター、プロパティ、および値を識別します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="1e0e1-126">ほとんどのブラウザーでは、デバッガーで値の変更とプレビューを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="1e0e1-127">必要な変更を特定した後、それを独自の CSS ファイルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="1e0e1-128">CSS 上書きファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="1e0e1-128">Upload a CSS override file</span></span>

<span data-ttu-id="1e0e1-129">コマースのサイトで CSS ファイルをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1e0e1-130">作成ツールで、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="1e0e1-131">左のナビゲーション ウィンドウで、**デザイン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e0e1-132">使用しているコマース作成ツールのバージョンによっては、**デザイン**を選択する前に、ナビゲーション ウィンドウの**設定**の展開が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="1e0e1-133">メインのデザイン ウィンドウの上部で、**CSS 上書き**タブが選択されていない場合はそれを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="1e0e1-134">**使用可能な CSS 上書き**で、**CSS ファイルのアップロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="1e0e1-135">ファイル エクスプローラー ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="1e0e1-136">ファイル エクスプローラーで、CSS ファイルを参照して選択し、**開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="1e0e1-137">アップロードした CSS ファイルは、**使用可能な CSS 上書き**の下に表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="1e0e1-138">CSS 上書きファイルのプレビュー</span><span class="sxs-lookup"><span data-stu-id="1e0e1-138">Preview a CSS override file</span></span>

<span data-ttu-id="1e0e1-139">実際のサイトで CSS 上書きファイルを有効にする前にプレビューするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="1e0e1-140">左側のナビゲーション ウィンドウで、**デザイン**をクリックしてから、**CSS 上書き**タブの、**使用可能な CSS 上書き**で、プレビューする CSS ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="1e0e1-141">CSS ファイル名の横にある、**プレビュー サイト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="1e0e1-142">**URL の選択**ダイアログ ボックスで、上書きを適用するサイトの URL を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="1e0e1-143">選択した URL に対して複数のバリアントがある場合、表示される**プレビュー バリエーション** ダイアログ ボックスで目的のバリアントを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="1e0e1-144">新しいブラウザー タブまたはウィンドウが開き、サイトに対してスタイルの上書きを検証できます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="1e0e1-145">その後、URL を認証された他のコマース ユーザーと共有して、確認やフィードバックを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="1e0e1-146">実際のサイトで CSS 上書きファイルを有効化する</span><span class="sxs-lookup"><span data-stu-id="1e0e1-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="1e0e1-147">CSS 上書きファイルをプレビューして承認した後、実際のサイトで有効化できます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="1e0e1-148">サイトで一度に有効化できるのは、1 つの CSS 上書きファイルのみです。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="1e0e1-149">新しい上書きファイルを有効にすると、以前の上書きファイルが無効になります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="1e0e1-150">したがって、すべての必要な上書きが単一の CSS 上書きファイルに存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="1e0e1-151">CSS 上書きファイルを有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="1e0e1-152">左側のナビゲーション ウィンドウで、**デザイン**をクリックしてから、**CSS 上書き**タブの、**使用可能な CSS 上書き**で、有効にする CSS ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="1e0e1-153">CSS ファイル名の下で、**有効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="1e0e1-154">上書きファイルは、実際のサイトで直ちに有効になります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="1e0e1-155">実際のサイトで CSS 上書きファイルを無効化する</span><span class="sxs-lookup"><span data-stu-id="1e0e1-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="1e0e1-156">サイトの CSS 上書きファイルを無効化するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="1e0e1-157">左側のナビゲーション ウィンドウで、**デザイン**をクリックしてから、**CSS 上書き**タブの、**使用可能な CSS 上書き**で、無効にする CSS ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="1e0e1-158">CSS ファイル名の下で、**無効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="1e0e1-159">上書きファイルは、実際のサイトで直ちに無効になります。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="1e0e1-160">CSS 上書きファイルの追加オプションにアクセスするには、CSS ファイル名の横で省略記号 (**...**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="1e0e1-161">**ダウンロード**、**名前変更**、および**置換**オプションは、既存の CSS 上書きファイルを迅速に変更するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1e0e1-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e0e1-162">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1e0e1-162">Additional resources</span></span>

[<span data-ttu-id="1e0e1-163">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="1e0e1-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="1e0e1-164">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="1e0e1-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="1e0e1-165">スタイル プリセットを使用して作業する</span><span class="sxs-lookup"><span data-stu-id="1e0e1-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="1e0e1-166">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="1e0e1-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="1e0e1-167">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="1e0e1-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="1e0e1-168">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="1e0e1-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="1e0e1-169">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="1e0e1-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="1e0e1-170">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="1e0e1-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
