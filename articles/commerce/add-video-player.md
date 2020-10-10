---
title: ビデオ プレーヤー モジュール
description: このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 3cf7ead9a5340d5db37a87bdf131ba87681d5a82
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817064"
---
# <a name="video-player-module"></a><span data-ttu-id="f2173-103">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="f2173-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f2173-104">このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2173-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f2173-105">概要</span><span class="sxs-lookup"><span data-stu-id="f2173-105">Overview</span></span>

<span data-ttu-id="f2173-106">ビデオ プレーヤー モジュールは、ビデオの再生をサポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="f2173-107">コンテンツ管理システム (CMS) にビデオ コンテンツをアップロードして使用可能であれば、任意のページに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f2173-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="f2173-108">ビデオ プレーヤー モジュールは、.mp4 メディア タイプがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f2173-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="f2173-109">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="f2173-109">Video player module</span></span>

<span data-ttu-id="f2173-110">ビデオ プレーヤー モジュールは、E コマース サイト上にビデオを紹介するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f2173-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="f2173-111">再生、一時停止、フルサイズ モード、音声ガイド、クローズド キャプションなど、すべての再生機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f2173-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="f2173-112">また、ビデオ プレーヤー モジュールでは、Microsoft のアクセシビリティ標準を満たすための、クローズド キャプションのカスタマイズもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f2173-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="f2173-113">たとえば、フォント サイズや背景色をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="f2173-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="f2173-114">ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックもサポートします。</span><span class="sxs-lookup"><span data-stu-id="f2173-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="f2173-115">ビデオが CMS にアップロードされると、セカンダリ オーディオ トラックもアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="f2173-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="f2173-116">ユーザーが選択した場合、ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックを再生できます。</span><span class="sxs-lookup"><span data-stu-id="f2173-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="f2173-117">E コマースでのビデオ プレーヤー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="f2173-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="f2173-118">製品の詳細ページまたはマーケティング ページの説明ビデオ</span><span class="sxs-lookup"><span data-stu-id="f2173-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="f2173-119">プロモーション ビデオまたはマーケティング ページのポリシーに関するビデオ</span><span class="sxs-lookup"><span data-stu-id="f2173-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="f2173-120">製品の詳細ページまたはマーケティング ページの製品機能を強調するマーケティング ビデオ</span><span class="sxs-lookup"><span data-stu-id="f2173-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="f2173-121">以下の図は、ホーム ページにおけるビデオ プレイヤー モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f2173-121">The following image shows an example of a video player module on a home page.</span></span>

![ビデオ プレイヤー モジュールの例](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="f2173-123">ビデオ プレーヤー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="f2173-123">Video player module properties</span></span>

| <span data-ttu-id="f2173-124">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="f2173-124">Property name</span></span>         | <span data-ttu-id="f2173-125">先頭値</span><span class="sxs-lookup"><span data-stu-id="f2173-125">Value</span></span>                               | <span data-ttu-id="f2173-126">説明</span><span class="sxs-lookup"><span data-stu-id="f2173-126">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="f2173-127">自動再生</span><span class="sxs-lookup"><span data-stu-id="f2173-127">Auto play</span></span>             | <span data-ttu-id="f2173-128">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f2173-128">**True** or **False**</span></span>               | <span data-ttu-id="f2173-129">値が **True** に設定されている場合、ビデオは自動的に再生されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-129">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="f2173-130">ミュート</span><span class="sxs-lookup"><span data-stu-id="f2173-130">Mute</span></span>                  | <span data-ttu-id="f2173-131">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f2173-131">**True** or **False**</span></span>               | <span data-ttu-id="f2173-132">値が **True** に設定されている場合、オーディオはミュートされます。</span><span class="sxs-lookup"><span data-stu-id="f2173-132">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="f2173-133">このプレーヤーの既定値は **False** です。</span><span class="sxs-lookup"><span data-stu-id="f2173-133">For this player, the default value is **False**.</span></span> <span data-ttu-id="f2173-134">Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-134">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="f2173-135">ループ</span><span class="sxs-lookup"><span data-stu-id="f2173-135">Loop</span></span>                  | <span data-ttu-id="f2173-136">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f2173-136">**True** or **False**</span></span>               | <span data-ttu-id="f2173-137">値が **True** に設定されている場合、ビデオはループで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-137">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="f2173-138">メディア</span><span class="sxs-lookup"><span data-stu-id="f2173-138">Media</span></span>                 | <span data-ttu-id="f2173-139">ビデオ ファイル パスおよび名前</span><span class="sxs-lookup"><span data-stu-id="f2173-139">Video file path and name</span></span> | <span data-ttu-id="f2173-140">ビデオ プレーヤーで再生されるビデオ ファイル</span><span class="sxs-lookup"><span data-stu-id="f2173-140">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="f2173-141">フルスクリーン再生</span><span class="sxs-lookup"><span data-stu-id="f2173-141">Play fullscreen</span></span>       | <span data-ttu-id="f2173-142">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f2173-142">**True** or **False**</span></span>               | <span data-ttu-id="f2173-143">値が **True** に設定されている場合、ビデオはフルスクリーン モードで再生されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-143">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="f2173-144">再生/一時停止トリガー</span><span class="sxs-lookup"><span data-stu-id="f2173-144">Play pause trigger</span></span>    | <span data-ttu-id="f2173-145">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f2173-145">**True** or **False**</span></span>               | <span data-ttu-id="f2173-146">値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-146">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="f2173-147">ビデオ プレーヤーのコントロール</span><span class="sxs-lookup"><span data-stu-id="f2173-147">Video player controls</span></span> | <span data-ttu-id="f2173-148">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f2173-148">**True** or **False**</span></span>               | <span data-ttu-id="f2173-149">値が **True** に設定されている場合は、すべてのビデオ プレーヤー コントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-149">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="f2173-150">これらのコントロールには、再生ボタンと一時停止ボタン、進捗状況インジケーター、およびクローズド キャプション オプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f2173-150">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="f2173-151">ポスター画像の非表示</span><span class="sxs-lookup"><span data-stu-id="f2173-151">Hide poster image</span></span>     | <span data-ttu-id="f2173-152">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f2173-152">**True** or **False**</span></span>               | <span data-ttu-id="f2173-153">ビデオにはポスター フレームを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f2173-153">A video can have a poster frame.</span></span> <span data-ttu-id="f2173-154">このプロパティの値が **True** に設定されている場合、ポスター フレームは非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="f2173-154">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="f2173-155">マスク レベル</span><span class="sxs-lookup"><span data-stu-id="f2173-155">Mask level</span></span>            | <span data-ttu-id="f2173-156">**0** から **100** までの数字</span><span class="sxs-lookup"><span data-stu-id="f2173-156">A number from **0** through **100**</span></span> | <span data-ttu-id="f2173-157">スタイル設定のためにビデオに適用されるマスク。</span><span class="sxs-lookup"><span data-stu-id="f2173-157">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="f2173-158">ビデオ プレーヤー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="f2173-158">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="f2173-159">ビデオ プレーヤー モジュールを作成する前に、まずビデオをメディア ライブラリにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2173-159">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="f2173-160">新しいページにビデオ プレーヤー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f2173-160">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f2173-161">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2173-161">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f2173-162">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**ビデオプレイヤーのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-162">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-163">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-163">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2173-164">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-164">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-165">**既定のページ**モジュールの**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-165">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2173-166">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-166">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-167">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-167">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2173-168">**モジュールの追加** ダイアログ ボックスで、**ビデオ プレイヤー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-168">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-169">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="f2173-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="f2173-170">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2173-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f2173-171">**テンプレートの選択** ダイアログ ボックスで、作成したビデオ プレイヤーのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-171">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="f2173-172">**ページ名**配下で、 **ビデオ プレイヤーのページ**を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-172">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-173">新規ページの**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-173">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2173-174">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-174">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-175">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-175">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2173-176">**モジュールの追加** ダイアログ ボックスで、**ビデオ プレイヤー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-176">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-177">ビデオ プレイヤー モジュールのプロパティ ウィンドウで、**ビデオの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-177">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="f2173-178">**メディアの選択**ダイアログ ボックスで、ビデオを選択し、**新しいメディア項目のアップロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-178">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="f2173-179">ファイル エクスプローラーで、1 つ以上のビデオ ファイルを選択し、**開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-179">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="f2173-180">**メディア項目のアップロード** ダイアログ ボックスで、必要に応じてタイトルとその他の情報を入力し、**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-180">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="f2173-181">**メディアの選択** ダイアログ ボックスで、 **閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2173-181">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="f2173-182">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="f2173-182">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f2173-183">ページにビデオ モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2173-183">You should see the video module on the page.</span></span> <span data-ttu-id="f2173-184">その他の設定を変更して、モジュールの動作をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="f2173-184">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="f2173-185">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="f2173-185">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f2173-186">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f2173-186">Additional resources</span></span>

[<span data-ttu-id="f2173-187">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="f2173-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f2173-188">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="f2173-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f2173-189">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="f2173-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="f2173-190">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="f2173-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f2173-191">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="f2173-191">Content block module</span></span>](add-hero-module.md)
