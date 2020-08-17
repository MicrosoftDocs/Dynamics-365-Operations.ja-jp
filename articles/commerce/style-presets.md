---
title: スタイル プリセットの作業
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーでのサイト スタイル プリセットの作業方法について説明します。
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 250f2386cefee8bef45df66c4eef31b4e7fc2686
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621274"
---
# <a name="work-with-style-presets"></a><span data-ttu-id="141d7-103">スタイル プリセットの作業</span><span class="sxs-lookup"><span data-stu-id="141d7-103">Work with style presets</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="141d7-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーでのサイト スタイル プリセットの作業方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="141d7-104">This topic describes how to work with site style presets in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="141d7-105">概要</span><span class="sxs-lookup"><span data-stu-id="141d7-105">Overview</span></span>

<span data-ttu-id="141d7-106">スタイル プリセットは、サイトのテーマ全体のすべてのカスタム スタイル値の保存されたセットです。</span><span class="sxs-lookup"><span data-stu-id="141d7-106">A style preset is a stored set of all authorable style values across a site's theme.</span></span> <span data-ttu-id="141d7-107">これを使用すると、サイト ビルダーからサイトの外観をすぐに変更できます。</span><span class="sxs-lookup"><span data-stu-id="141d7-107">It can be used to immediately change the look of a site from site builder.</span></span> <span data-ttu-id="141d7-108">スタイルのプリセットにより、Commerce サイト ビルダーの作成者は、カスケード スタイルシート (CSS) を使用したり、テーマを配置することなく、サイト全体のスタイル値をすばやく変更、プレビュー、およびアクティブにできます。</span><span class="sxs-lookup"><span data-stu-id="141d7-108">Style presets let Commerce site builder authors quickly change, preview, and activate a set of style values across their site, without having to use Cascading Style Sheets (CSS) or deploy themes.</span></span> <span data-ttu-id="141d7-109">スタイル変数の一般的な例としては、スタイルのプリセットを使用して管理できるフォント スタイル、ボタン スタイル、サイト カラーなどがあります。</span><span class="sxs-lookup"><span data-stu-id="141d7-109">Font styles, button styles, and site colors are typical examples of style variables that can be managed through style presets.</span></span>

<span data-ttu-id="141d7-110">サイトで使用できるスタイル変数のセットは、サイトのテナントに配置されているテーマとモジュール ライブラリによって決まります。</span><span class="sxs-lookup"><span data-stu-id="141d7-110">The set of style variables that is available in a site is determined by the theme and module library that is deployed to a site's tenant.</span></span> <span data-ttu-id="141d7-111">Dynamics 365 Commerce オンライン ソフトウェア開発キット (SDK) を使用すると、開発者は、特定のテーマに対して必要な数のカスタム スタイル変数を実装できるようになります。</span><span class="sxs-lookup"><span data-stu-id="141d7-111">The Dynamics 365 Commerce online software development kit (SDK) lets developers implement as many (or as few) authorable style variables as they require for a given theme.</span></span> <span data-ttu-id="141d7-112">より多くのスタイル変数を有効にすることによって、テーマ開発者は、サイト ビルダーの作成者にサイト スタイルの最終決定を任せることができます。</span><span class="sxs-lookup"><span data-stu-id="141d7-112">By enabling more style variables, a theme developer can put final choices about site styles into the hands of site builder authors.</span></span> <span data-ttu-id="141d7-113">したがって、開発者以外はツール セットを使用してサイト スタイルを更新およびプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="141d7-113">Therefore, non-developers can update and preview site styles by using the toolset.</span></span> <span data-ttu-id="141d7-114">また、この機能は、テーマや CSS を直接変更したり不要なオーバーヘッドを生じたりするようなシナリオで役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="141d7-114">The capability is also useful for any scenario where direct changes to themes or CSS will cause unnecessary overhead.</span></span>

<span data-ttu-id="141d7-115">カスタム スタイル変数が有効になっているテーマでは、既定のスタイル プリセットが必要です。</span><span class="sxs-lookup"><span data-stu-id="141d7-115">Themes where authorable style variables are enabled require a default style preset.</span></span> <span data-ttu-id="141d7-116">必要に応じて、配置されたテーマ パッケージの一部として追加のプリセット オプションを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="141d7-116">They can optionally include additional preset options as part of a deployed theme package.</span></span> <span data-ttu-id="141d7-117">たとえば、1 つの既定の "モダン ライト" スタイル プリセットを持つテーマを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="141d7-117">For example, a theme can be deployed that has a single default "modern light" style preset.</span></span> <span data-ttu-id="141d7-118">また、既定のプリセットに加えて、"モダン ダーク"、"ビンテージ ライト"、または "ビンテージ ダーク" などの追加のスタイル プリセット オプションが含まれている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="141d7-118">Alternatively, it might include additional style preset options besides the default preset, such as "modern dark," "vintage light," or "vintage dark."</span></span> <span data-ttu-id="141d7-119">これらの組み込みテーマの事前設定は、開発者によって作成され、新しいサイト デザインの開始点として使用できます。</span><span class="sxs-lookup"><span data-stu-id="141d7-119">These built-in theme presets are created by developers and can be used as starting points for new site designs.</span></span>

<span data-ttu-id="141d7-120">サイト ビルダーでは、作成者は、テーマの組み込みプリセットから選択するか、有効なスタイル変数を使用して独自のスタイル プリセットとカスタマイズを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="141d7-120">In site builder, authors can select among a theme's built-in presets, or they can create their own style presets and customizations by using the enabled style variables.</span></span> <span data-ttu-id="141d7-121">実際のサイトで有効にする前に、スタイル プリセットをサイト ビルダーでプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="141d7-121">A style preset can be previewed in site builder before it's activated on the live site.</span></span> <span data-ttu-id="141d7-122">作成者のスタイルの変更がレビューされた後、スタイルのプリセットを実際のサイトに対して "有効" に設定できます。</span><span class="sxs-lookup"><span data-stu-id="141d7-122">After an author's style changes are reviewed, the style preset can then be set to "active" for the live site.</span></span>

## <a name="preview-a-style-preset"></a><span data-ttu-id="141d7-123">スタイル プリセットのプレビュー</span><span class="sxs-lookup"><span data-stu-id="141d7-123">Preview a style preset</span></span>

<span data-ttu-id="141d7-124">サイト ビルダーでサイトのスタイル プリセットをプレビューするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="141d7-124">To preview a style preset on your site in site builder, follow these steps.</span></span>

1. <span data-ttu-id="141d7-125">サイトの左側のナビゲーション ウィンドウで、**サイト設定 \>のデザイン** に移動します。</span><span class="sxs-lookup"><span data-stu-id="141d7-125">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="141d7-126">デザイン エディターの上部にある **スタイル プリセット** タブの **使用可能なプリセット** リストでプリセットを選択し、**表示** をクリックしてプリセット エディターに移動します。</span><span class="sxs-lookup"><span data-stu-id="141d7-126">On the **Style presets** tab at the top of the design editor, in the **Available presets** list, select a preset, and then select **View** to go to the preset editor.</span></span>

    <span data-ttu-id="141d7-127">現在、**使用可能なプリセット** の一覧にプリセットが存在しない場合は、[カスタム スタイル プリセットの作成](#create-a-custom-style-preset) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="141d7-127">If there are currently no presets in the **Available presets** list, see [Create a custom style preset](#create-a-custom-style-preset) for information about how to create a custom style preset.</span></span>

    > [!NOTE]
    > <span data-ttu-id="141d7-128">テーマに含まれていたプリセットは、**組み込み** のバッジで示されます。</span><span class="sxs-lookup"><span data-stu-id="141d7-128">Presets that were included with the theme are indicated by a **Built-in** badge.</span></span> <span data-ttu-id="141d7-129">これらの組み込みのプリセットは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="141d7-129">These built-in presets are read-only.</span></span> <span data-ttu-id="141d7-130">組み込みのプリセットを新しいカスタマイズ可能なプリセットとしてコピーするには、省略記号ボタン (**...**) を選択し、**名前を付けて保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-130">To copy a built-in preset as a new customizable preset, select the ellipsis button (**...**) for the preset, and then select **Save as**.</span></span>

1. <span data-ttu-id="141d7-131">コマンド バーで、**プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-131">On the command bar, select **Preview**.</span></span>
1. <span data-ttu-id="141d7-132">スタイル プリセットをプレビューを使用するために自分のサイトからの URL を選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-132">Select a URL from your site to use to preview the style preset, and then select **OK**.</span></span>
1. <span data-ttu-id="141d7-133">バリアントの名前を選択して、プレビューするチャンネル固有でロケール固有の URL バリアントを選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-133">Select the channel-specific and locale-specific URL variant to preview by selecting the variant's name.</span></span> <span data-ttu-id="141d7-134">新しいプレビュー ブラウザ ウィンドウが開き、選択したスタイルのプリセットが指定したページに適用されます。</span><span class="sxs-lookup"><span data-stu-id="141d7-134">A new preview browser window is opened, where the selected style preset is applied to the specified page.</span></span>

> [!NOTE]
> <span data-ttu-id="141d7-135">プレビュー URL は永続的で認証されています。</span><span class="sxs-lookup"><span data-stu-id="141d7-135">The preview URL is persistent and authenticated.</span></span> <span data-ttu-id="141d7-136">したがって、実際のサイトで "有効" に設定する前に、認証された他の同僚にコピーして貼り付けて送信し、確認することができます。</span><span class="sxs-lookup"><span data-stu-id="141d7-136">Therefore, you can copy, paste, and send it to other authenticated co-workers for review before you set it to "active" on your live site.</span></span> <span data-ttu-id="141d7-137">また、プレビュー URL は、さまざまなデバイス、さまざまなブラウザー、さまざまな画面でスタイルをチェックする場合にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="141d7-137">The preview URL is also useful for checking styles on different devices, in different browsers, and on different screens.</span></span>

> [!TIP]
> <span data-ttu-id="141d7-138">スタイル プリセットを編集する間に、別のブラウザ ウィンドウでプレビュー ブラウザ ウィンドウを開いたままにしておくと、変更をすぐに検証できます。</span><span class="sxs-lookup"><span data-stu-id="141d7-138">While you edit a style preset, you might find it helpful to leave the preview browser window for it open in a separate browser window, so that you can quickly validate your changes.</span></span> <span data-ttu-id="141d7-139">プリセットに変更を保存した後、開いたプレビュー ブラウザ ウィンドウを更新して、ユーザー エクスペリエンスを検証します。</span><span class="sxs-lookup"><span data-stu-id="141d7-139">After you save your changes to a preset, refresh the open preview browser window to validate the user experience.</span></span>

## <a name="create-a-custom-style-preset"></a><span data-ttu-id="141d7-140">カスタム スタイルのプリセットを作成する</span><span class="sxs-lookup"><span data-stu-id="141d7-140">Create a custom style preset</span></span>

<span data-ttu-id="141d7-141">サイト ビルダーでカスタム スタイル プリセットを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="141d7-141">To create a custom style preset in site builder, follow these steps.</span></span>

1. <span data-ttu-id="141d7-142">サイトの左側のナビゲーション ウィンドウで、**サイト設定 \>のデザイン** に移動します。</span><span class="sxs-lookup"><span data-stu-id="141d7-142">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="141d7-143">デザイン エディターの上部にある **スタイル プリセット** タブのコマンド バーで、**新規プリセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-143">On the **Style presets** tab at the top of the design editor, on the command bar, select **New preset**.</span></span>
1. <span data-ttu-id="141d7-144">新規プリセットの名前と説明を入力して、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-144">Enter a name and description for the new preset, and then select **Save**.</span></span> <span data-ttu-id="141d7-145">このテーマの既定値を出発点として使用する、新しいカスタマイズ可能なプリセットが作成されます。</span><span class="sxs-lookup"><span data-stu-id="141d7-145">A new customizable preset is created that uses the theme's default values as a starting point.</span></span>

> [!NOTE]
> <span data-ttu-id="141d7-146">また、既存のプリセットから新しいカスタム スタイルのプリセットを作成するには、そのプリセットの省略符号ボタン (**...**) を選択し、**名前を付けて保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-146">You can also create a new custom style preset from any existing preset by selecting the ellipsis button (**...**) for that preset and then selecting **Save as**.</span></span> <span data-ttu-id="141d7-147">または、プリセット エディタのコマンドバーで **名前を付けて保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-147">Alternatively, select **Save as** on the command bar in the preset editor.</span></span>

## <a name="modify-global-and-module-type-style-values"></a><span data-ttu-id="141d7-148">グローバル タイプとモジュール タイプのスタイル値の変更</span><span class="sxs-lookup"><span data-stu-id="141d7-148">Modify global and module type style values</span></span>

<span data-ttu-id="141d7-149">一部のテーマのスタイル変数は、複数のモジュールタイプの間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="141d7-149">Some of a theme's style variables are shared among multiple module types.</span></span> <span data-ttu-id="141d7-150">これらのスタイル変数は、*グローバル* スタイル変数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="141d7-150">These style variables are referred to as *global* style variables.</span></span> <span data-ttu-id="141d7-151">例としては、プライマリ サイトの色、既定のフォント スタイル、ボタンのスタイルなどがあります。</span><span class="sxs-lookup"><span data-stu-id="141d7-151">Examples include primary site colors, default font styles, and button styles.</span></span> <span data-ttu-id="141d7-152">グローバル変数を設定することにより、さまざまな種類のモジュールに対して外観を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="141d7-152">By setting global variables, you might change the look across many different module types.</span></span>

<span data-ttu-id="141d7-153">一部のスタイル値は、モジュール タイプに固有の場合もあれば、既定のグローバル値を上書きする必要がある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="141d7-153">Some style values can be unique to a module type, or they might have to optionally override a default global value.</span></span> <span data-ttu-id="141d7-154">サイトのテーマによって、モジュール タイプのスタイル変数が実装されている場合、サイト ビルダーの作成者は、グローバル設定とは別にモジュール タイプのスタイルをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="141d7-154">If a site's theme has implemented module type style variables, site builder authors can customize the style of a module type independently of the global settings.</span></span> <span data-ttu-id="141d7-155">モジュール タイプ変数は、テーマのグローバル スタイル変数を補強または上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="141d7-155">Module type variables can either augment or override the global style variables in a theme.</span></span>

> [!NOTE]
> <span data-ttu-id="141d7-156">サイトのスタイル値の階層は、次のような方法で動作します。</span><span class="sxs-lookup"><span data-stu-id="141d7-156">The hierarchy of style values in a site behaves in the following manner.</span></span> <span data-ttu-id="141d7-157">スタイル値は右方向に表示され、その左にあるスタイル値は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="141d7-157">Style values that appear farther to the right override the style values to the left of them.</span></span>
>
> <span data-ttu-id="141d7-158">テーマの既定値 \<グローバルスタイル値 \<モジュール タイプ スタイル値 \<CSS上書き</span><span class="sxs-lookup"><span data-stu-id="141d7-158">Theme default values \< Global style values \< Module type style values \< CSS override</span></span>

<span data-ttu-id="141d7-159">サイト ビルダーでスタイル プリセットのグローバル タイプの値かモジュールタイプの値を変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="141d7-159">To change a style preset's global or module type values in site builder, follow these steps.</span></span>

1. <span data-ttu-id="141d7-160">サイトの左側のナビゲーション ウィンドウで、**サイト設定 \>のデザイン** に移動します。</span><span class="sxs-lookup"><span data-stu-id="141d7-160">In the left navigation pane for your site, go to **Site Settings \> Design**.</span></span>
1. <span data-ttu-id="141d7-161">デザインエディターの上部にある **スタイル プリセット** タブで、プリセット エディターに移動するスタイル プリセットの **表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-161">On the **Style presets** tab at the top of the design editor, select **View** for any style preset to go to the preset editor.</span></span>
1. <span data-ttu-id="141d7-162">**プレビュー** を選択し、URLの選択の手順に従って、プリセットのフルブラウザー ウィンドウ プレビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="141d7-162">Select **Preview**, and then follow the URL selection steps to open a full-browser-window preview for your preset.</span></span> <span data-ttu-id="141d7-163">このプレビュー ブラウザ ウィンドウは開いたままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="141d7-163">Leave this preview browser window open.</span></span>
1. <span data-ttu-id="141d7-164">プリセット エディターで、右上にある **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-164">In the preset editor, select **Edit** in the upper right.</span></span>
1. <span data-ttu-id="141d7-165">グローバル スタイルの値を変更するには、エディターのスタイル変数コントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="141d7-165">Use the style variable controls in the editor to change some global style values.</span></span>
1. <span data-ttu-id="141d7-166">エディターの最上部で、**グローバル** タブの右側にある **モジュール** タブで、スタイルを設定する必要があるモジュールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-166">At the top of the editor, on the **Modules** tab to the right of the **Global** tab, select a module type that must be styled.</span></span>
1. <span data-ttu-id="141d7-167">スタイル コントロールを使用して、モジュール タイプの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="141d7-167">Use the style controls to change some values for the module type.</span></span>
1. <span data-ttu-id="141d7-168">変更をプレビューする準備ができたら、コマンドバーの **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-168">When you're ready to preview your changes, select **Save** on the command bar.</span></span>
1. <span data-ttu-id="141d7-169">開いているプレビュー ブラウザー ウィンドウに戻り、最新の状態に更新します。</span><span class="sxs-lookup"><span data-stu-id="141d7-169">Return to the open preview browser window, and refresh it.</span></span> <span data-ttu-id="141d7-170">完全ブラウザ ウィンドウのプレビューは、さまざまな表示ブレークポイント、異なるブラウザー、異なるデバイス プラットフォームでスタイルの変更をチェックする場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="141d7-170">The full-browser-window preview is useful for checking style changes at different view breakpoints, in different browsers, and on different device platforms.</span></span>
1. <span data-ttu-id="141d7-171">すべての変更が完了して検証されたら、エディターの右上にある **編集の完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-171">When all changes have been completed and validated, select **Finish editing** in the upper right of the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="141d7-172">サイトで現在有効なスタイル プリセットを編集している場合、青色の **有効な** バッジがエディターに表示されます。</span><span class="sxs-lookup"><span data-stu-id="141d7-172">If you're editing the style preset that is currently active on your site, you will see a blue **Active** badge in the editor.</span></span> <span data-ttu-id="141d7-173">このバッジは、プリセットが Web サイト上で現在有効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="141d7-173">This badge indicates that the preset is currently live on your website.</span></span> <span data-ttu-id="141d7-174">有効なプリセットを変更する場合は、**発行** を選択してその変更を実際のサイトにプッシュします。</span><span class="sxs-lookup"><span data-stu-id="141d7-174">If you change the active preset, select **Publish** to push those changes to your live site.</span></span>

## <a name="make-a-new-style-preset-active-on-your-live-site"></a><span data-ttu-id="141d7-175">実際のサイトで新しいスタイルのプリセットを有効にする</span><span class="sxs-lookup"><span data-stu-id="141d7-175">Make a new style preset active on your live site</span></span>

<span data-ttu-id="141d7-176">サイトの新しい有効なプリセットとしてスタイル プリセットを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="141d7-176">To set a style preset as the new active preset on your site, follow these steps.</span></span>

- <span data-ttu-id="141d7-177">次のいずれかの場所で、**有効なボタンとして設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="141d7-177">Select the **Set as active button** in one of these places:</span></span>

    - <span data-ttu-id="141d7-178">スタイル プリセット エディターのコマンドバー</span><span class="sxs-lookup"><span data-stu-id="141d7-178">The command bar in the style preset editor</span></span>
    - <span data-ttu-id="141d7-179">**サイト設定 \> デザイン** の **スタイル プリセット** のメイン ビューにある利用可能なプリセットの省略記号メニュー (**...**)</span><span class="sxs-lookup"><span data-stu-id="141d7-179">The ellipsis menu (**...**) for any available preset in the main view on the **Style presets** tab at **Site Settings \> Design**</span></span>

<span data-ttu-id="141d7-180">プリセットのスタイル値が一般公開 Web サイト全体で有効になります。</span><span class="sxs-lookup"><span data-stu-id="141d7-180">The preset's style values are made active across your public-facing website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="141d7-181">追加リソース</span><span class="sxs-lookup"><span data-stu-id="141d7-181">Additional resources</span></span>

[<span data-ttu-id="141d7-182">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="141d7-182">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="141d7-183">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="141d7-183">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="141d7-184">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="141d7-184">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="141d7-185">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="141d7-185">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="141d7-186">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="141d7-186">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="141d7-187">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="141d7-187">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="141d7-188">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="141d7-188">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="141d7-189">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="141d7-189">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
