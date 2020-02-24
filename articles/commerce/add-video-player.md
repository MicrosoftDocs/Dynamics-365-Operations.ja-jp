---
title: ビデオ プレーヤー モジュール
description: このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025657"
---
# <a name="video-player-module"></a><span data-ttu-id="5c40b-103">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="5c40b-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5c40b-104">このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c40b-105">概要</span><span class="sxs-lookup"><span data-stu-id="5c40b-105">Overview</span></span>

<span data-ttu-id="5c40b-106">ビデオ プレーヤー モジュールは、ビデオの再生をサポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="5c40b-107">コンテンツ管理システム (CMS) にビデオ コンテンツをアップロードして使用可能であれば、任意のページに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="5c40b-108">ビデオ プレーヤー モジュールは、.mp4 メディア タイプがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c40b-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="5c40b-109">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="5c40b-109">Video player module</span></span>

<span data-ttu-id="5c40b-110">ビデオ プレーヤー モジュールは、E コマース サイト上にビデオを紹介するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="5c40b-111">再生、一時停止、フルサイズ モード、音声ガイド、クローズド キャプションなど、すべての再生機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5c40b-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="5c40b-112">また、ビデオ プレーヤー モジュールでは、Microsoft のアクセシビリティ標準を満たすための、クローズド キャプションのカスタマイズもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c40b-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="5c40b-113">たとえば、フォント サイズや背景色をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="5c40b-114">ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックもサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c40b-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="5c40b-115">ビデオが CMS にアップロードされると、セカンダリ オーディオ トラックもアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="5c40b-116">ユーザーが選択した場合、ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックを再生できます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="5c40b-117">E コマースでのビデオ プレーヤー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="5c40b-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="5c40b-118">製品の詳細ページまたはマーケティング ページの説明ビデオ</span><span class="sxs-lookup"><span data-stu-id="5c40b-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="5c40b-119">プロモーション ビデオまたはマーケティング ページのポリシーに関するビデオ</span><span class="sxs-lookup"><span data-stu-id="5c40b-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="5c40b-120">製品の詳細ページまたはマーケティング ページの製品機能を強調するマーケティング ビデオ</span><span class="sxs-lookup"><span data-stu-id="5c40b-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="5c40b-121">ビデオ プレーヤー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="5c40b-121">Video player module properties</span></span>

| <span data-ttu-id="5c40b-122">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5c40b-122">Property name</span></span>         | <span data-ttu-id="5c40b-123">金額</span><span class="sxs-lookup"><span data-stu-id="5c40b-123">Value</span></span>                               | <span data-ttu-id="5c40b-124">説明</span><span class="sxs-lookup"><span data-stu-id="5c40b-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="5c40b-125">自動再生</span><span class="sxs-lookup"><span data-stu-id="5c40b-125">Auto play</span></span>             | <span data-ttu-id="5c40b-126">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5c40b-126">**True** or **False**</span></span>               | <span data-ttu-id="5c40b-127">値が **True** に設定されている場合、ビデオは自動的に再生されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="5c40b-128">ミュート</span><span class="sxs-lookup"><span data-stu-id="5c40b-128">Mute</span></span>                  | <span data-ttu-id="5c40b-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5c40b-129">**True** or **False**</span></span>               | <span data-ttu-id="5c40b-130">値が **True** に設定されている場合、オーディオはミュートされます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="5c40b-131">このプレーヤーの既定値は **False** です。</span><span class="sxs-lookup"><span data-stu-id="5c40b-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="5c40b-132">Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="5c40b-133">ループ</span><span class="sxs-lookup"><span data-stu-id="5c40b-133">Loop</span></span>                  | <span data-ttu-id="5c40b-134">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5c40b-134">**True** or **False**</span></span>               | <span data-ttu-id="5c40b-135">値が **True** に設定されている場合、ビデオはループで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="5c40b-136">メディア</span><span class="sxs-lookup"><span data-stu-id="5c40b-136">Media</span></span>                 | <span data-ttu-id="5c40b-137">ビデオ ファイル パスおよび名前</span><span class="sxs-lookup"><span data-stu-id="5c40b-137">Video file path and name</span></span> | <span data-ttu-id="5c40b-138">ビデオ プレーヤーで再生されるビデオ ファイル</span><span class="sxs-lookup"><span data-stu-id="5c40b-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="5c40b-139">フルスクリーン再生</span><span class="sxs-lookup"><span data-stu-id="5c40b-139">Play fullscreen</span></span>       | <span data-ttu-id="5c40b-140">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5c40b-140">**True** or **False**</span></span>               | <span data-ttu-id="5c40b-141">値が **True** に設定されている場合、ビデオはフルスクリーン モードで再生されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="5c40b-142">再生/一時停止トリガー</span><span class="sxs-lookup"><span data-stu-id="5c40b-142">Play pause trigger</span></span>    | <span data-ttu-id="5c40b-143">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5c40b-143">**True** or **False**</span></span>               | <span data-ttu-id="5c40b-144">値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="5c40b-145">ビデオ プレーヤーのコントロール</span><span class="sxs-lookup"><span data-stu-id="5c40b-145">Video player controls</span></span> | <span data-ttu-id="5c40b-146">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5c40b-146">**True** or **False**</span></span>               | <span data-ttu-id="5c40b-147">値が **True** に設定されている場合は、すべてのビデオ プレーヤー コントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="5c40b-148">これらのコントロールには、再生ボタンと一時停止ボタン、進捗状況インジケーター、およびクローズド キャプション オプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="5c40b-149">ポスター画像の非表示</span><span class="sxs-lookup"><span data-stu-id="5c40b-149">Hide poster image</span></span>     | <span data-ttu-id="5c40b-150">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5c40b-150">**True** or **False**</span></span>               | <span data-ttu-id="5c40b-151">ビデオにはポスター フレームを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-151">A video can have a poster frame.</span></span> <span data-ttu-id="5c40b-152">このプロパティの値が **True** に設定されている場合、ポスター フレームは非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="5c40b-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="5c40b-153">マスク レベル</span><span class="sxs-lookup"><span data-stu-id="5c40b-153">Mask level</span></span>            | <span data-ttu-id="5c40b-154">**0** から **100** までの数字</span><span class="sxs-lookup"><span data-stu-id="5c40b-154">A number from **0** through **100**</span></span> | <span data-ttu-id="5c40b-155">スタイル設定のためにビデオに適用されるマスク。</span><span class="sxs-lookup"><span data-stu-id="5c40b-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="5c40b-156">ビデオ プレーヤー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="5c40b-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="5c40b-157">ビデオ プレーヤー モジュールを作成する前に、まずビデオをメディア ライブラリにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c40b-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="5c40b-158">新しいページにビデオ プレーヤー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5c40b-159">**ビデオ プレーヤー テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="5c40b-160">既定のページの**メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="5c40b-161">コンテナー モジュールで、ビデオ プレーヤーおよびアンビエント ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="5c40b-162">テンプレートの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="5c40b-163">作成したビデオ プレーヤー テンプレートを使用して、**ビデオ プレーヤー ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="5c40b-164">新しいページの**メイン** スロットで、ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="5c40b-165">ビデオ プレーヤー モジュールのプロパティ ウィンドウで、**ビデオの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="5c40b-166">**メディアの選択**ダイアログ ボックスで、ビデオを選択し、**新しいメディア項目のアップロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="5c40b-167">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="5c40b-167">Save and preview the page.</span></span> <span data-ttu-id="5c40b-168">ページにビデオ モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-168">You should see the video module on the page.</span></span> <span data-ttu-id="5c40b-169">その他の設定を変更して、モジュールの動作をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="5c40b-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="5c40b-170">ページの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="5c40b-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c40b-171">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5c40b-171">Additional resources</span></span>

[<span data-ttu-id="5c40b-172">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="5c40b-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5c40b-173">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="5c40b-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="5c40b-174">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="5c40b-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="5c40b-175">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="5c40b-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="5c40b-176">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="5c40b-176">Content block module</span></span>](add-hero-module.md)
