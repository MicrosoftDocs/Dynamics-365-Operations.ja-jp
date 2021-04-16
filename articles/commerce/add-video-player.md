---
title: ビデオ プレーヤー モジュール
description: このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: aa1efa6ce959439c49983553edfaf247c8e8dcd5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797410"
---
# <a name="video-player-module"></a><span data-ttu-id="0d787-103">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="0d787-103">Video player module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d787-104">このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d787-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0d787-105">ビデオ プレーヤー モジュールは、ビデオの再生をサポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-105">The video player module is used to support video playback.</span></span> <span data-ttu-id="0d787-106">コンテンツ管理システム (CMS) にビデオ コンテンツをアップロードして使用可能であれば、任意のページに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="0d787-106">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="0d787-107">ビデオ プレーヤー モジュールは、.mp4 メディア タイプがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0d787-107">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="0d787-108">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="0d787-108">Video player module</span></span>

<span data-ttu-id="0d787-109">ビデオ プレーヤー モジュールは、E コマース サイト上にビデオを紹介するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d787-109">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="0d787-110">再生、一時停止、フルサイズ モード、音声ガイド、クローズド キャプションなど、すべての再生機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0d787-110">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="0d787-111">また、ビデオ プレーヤー モジュールでは、Microsoft のアクセシビリティ標準を満たすための、クローズド キャプションのカスタマイズもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0d787-111">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="0d787-112">たとえば、フォント サイズや背景色をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="0d787-112">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="0d787-113">ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックもサポートします。</span><span class="sxs-lookup"><span data-stu-id="0d787-113">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="0d787-114">ビデオが CMS にアップロードされると、セカンダリ オーディオ トラックもアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="0d787-114">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="0d787-115">ユーザーが選択した場合、ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックを再生できます。</span><span class="sxs-lookup"><span data-stu-id="0d787-115">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="0d787-116">E コマースでのビデオ プレーヤー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="0d787-116">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="0d787-117">製品の詳細ページまたはマーケティング ページの説明ビデオ</span><span class="sxs-lookup"><span data-stu-id="0d787-117">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="0d787-118">プロモーション ビデオまたはマーケティング ページのポリシーに関するビデオ</span><span class="sxs-lookup"><span data-stu-id="0d787-118">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="0d787-119">製品の詳細ページまたはマーケティング ページの製品機能を強調するマーケティング ビデオ</span><span class="sxs-lookup"><span data-stu-id="0d787-119">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="0d787-120">以下の図は、ホーム ページにおけるビデオ プレイヤー モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0d787-120">The following image shows an example of a video player module on a home page.</span></span>

![ビデオ プレイヤー モジュールの例](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="0d787-122">ビデオ プレーヤー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="0d787-122">Video player module properties</span></span>

| <span data-ttu-id="0d787-123">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0d787-123">Property name</span></span>         | <span data-ttu-id="0d787-124">先頭値</span><span class="sxs-lookup"><span data-stu-id="0d787-124">Value</span></span>                               | <span data-ttu-id="0d787-125">説明</span><span class="sxs-lookup"><span data-stu-id="0d787-125">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="0d787-126">自動再生</span><span class="sxs-lookup"><span data-stu-id="0d787-126">Auto play</span></span>             | <span data-ttu-id="0d787-127">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0d787-127">**True** or **False**</span></span>               | <span data-ttu-id="0d787-128">値が **True** に設定されている場合、ビデオは自動的に再生されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-128">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="0d787-129">ミュート</span><span class="sxs-lookup"><span data-stu-id="0d787-129">Mute</span></span>                  | <span data-ttu-id="0d787-130">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0d787-130">**True** or **False**</span></span>               | <span data-ttu-id="0d787-131">値が **True** に設定されている場合、オーディオはミュートされます。</span><span class="sxs-lookup"><span data-stu-id="0d787-131">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="0d787-132">このプレーヤーの既定値は **False** です。</span><span class="sxs-lookup"><span data-stu-id="0d787-132">For this player, the default value is **False**.</span></span> <span data-ttu-id="0d787-133">Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-133">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="0d787-134">ループ</span><span class="sxs-lookup"><span data-stu-id="0d787-134">Loop</span></span>                  | <span data-ttu-id="0d787-135">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0d787-135">**True** or **False**</span></span>               | <span data-ttu-id="0d787-136">値が **True** に設定されている場合、ビデオはループで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-136">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="0d787-137">メディア</span><span class="sxs-lookup"><span data-stu-id="0d787-137">Media</span></span>                 | <span data-ttu-id="0d787-138">ビデオ ファイル パスおよび名前</span><span class="sxs-lookup"><span data-stu-id="0d787-138">Video file path and name</span></span> | <span data-ttu-id="0d787-139">ビデオ プレーヤーで再生されるビデオ ファイル</span><span class="sxs-lookup"><span data-stu-id="0d787-139">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="0d787-140">フルスクリーン再生</span><span class="sxs-lookup"><span data-stu-id="0d787-140">Play fullscreen</span></span>       | <span data-ttu-id="0d787-141">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0d787-141">**True** or **False**</span></span>               | <span data-ttu-id="0d787-142">値が **True** に設定されている場合、ビデオはフルスクリーン モードで再生されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-142">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="0d787-143">再生/一時停止トリガー</span><span class="sxs-lookup"><span data-stu-id="0d787-143">Play pause trigger</span></span>    | <span data-ttu-id="0d787-144">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0d787-144">**True** or **False**</span></span>               | <span data-ttu-id="0d787-145">値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-145">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="0d787-146">ビデオ プレーヤーのコントロール</span><span class="sxs-lookup"><span data-stu-id="0d787-146">Video player controls</span></span> | <span data-ttu-id="0d787-147">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0d787-147">**True** or **False**</span></span>               | <span data-ttu-id="0d787-148">値が **True** に設定されている場合は、すべてのビデオ プレーヤー コントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-148">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="0d787-149">これらのコントロールには、再生ボタンと一時停止ボタン、進捗状況インジケーター、およびクローズド キャプション オプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d787-149">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="0d787-150">ポスター画像の非表示</span><span class="sxs-lookup"><span data-stu-id="0d787-150">Hide poster image</span></span>     | <span data-ttu-id="0d787-151">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0d787-151">**True** or **False**</span></span>               | <span data-ttu-id="0d787-152">ビデオにはポスター フレームを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0d787-152">A video can have a poster frame.</span></span> <span data-ttu-id="0d787-153">このプロパティの値が **True** に設定されている場合、ポスター フレームは非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="0d787-153">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="0d787-154">マスク レベル</span><span class="sxs-lookup"><span data-stu-id="0d787-154">Mask level</span></span>            | <span data-ttu-id="0d787-155">**0** から **100** までの数字</span><span class="sxs-lookup"><span data-stu-id="0d787-155">A number from **0** through **100**</span></span> | <span data-ttu-id="0d787-156">スタイル設定のためにビデオに適用されるマスク。</span><span class="sxs-lookup"><span data-stu-id="0d787-156">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="0d787-157">ビデオ プレーヤー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="0d787-157">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="0d787-158">ビデオ プレーヤー モジュールを作成する前に、まずビデオをメディア ライブラリにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d787-158">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="0d787-159">新しいページにビデオ プレーヤー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0d787-159">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0d787-160">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d787-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0d787-161">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**ビデオプレイヤーのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-161">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-162">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-162">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d787-163">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-163">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-164">**既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-164">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d787-165">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-165">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-166">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-166">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d787-167">**モジュールの追加** ダイアログ ボックスで、**ビデオ プレイヤー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-167">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-168">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="0d787-168">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="0d787-169">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d787-169">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0d787-170">**テンプレートの選択** ダイアログ ボックスで、作成したビデオ プレイヤーのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-170">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="0d787-171">**ページ名** 配下で、 **ビデオ プレイヤーのページ** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-171">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-172">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-172">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d787-173">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-173">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-174">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-174">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d787-175">**モジュールの追加** ダイアログ ボックスで、**ビデオ プレイヤー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-175">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-176">ビデオ プレイヤー モジュールのプロパティ ウィンドウで、**ビデオの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-176">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="0d787-177">**メディアの選択** ダイアログ ボックスで、ビデオを選択し、**新しいメディア項目のアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-177">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="0d787-178">ファイル エクスプローラーで、1 つ以上のビデオ ファイルを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-178">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="0d787-179">**メディア項目のアップロード** ダイアログ ボックスで、必要に応じてタイトルとその他の情報を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-179">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="0d787-180">**メディアの選択** ダイアログ ボックスで、 **閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d787-180">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="0d787-181">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="0d787-181">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="0d787-182">ページにビデオ モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d787-182">You should see the video module on the page.</span></span> <span data-ttu-id="0d787-183">その他の設定を変更して、モジュールの動作をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="0d787-183">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="0d787-184">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="0d787-184">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0d787-185">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0d787-185">Additional resources</span></span>

[<span data-ttu-id="0d787-186">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="0d787-186">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0d787-187">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="0d787-187">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="0d787-188">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="0d787-188">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="0d787-189">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="0d787-189">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="0d787-190">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="0d787-190">Content block module</span></span>](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]