---
title: ビデオ プレーヤー モジュール
description: このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885904"
---
# <a name="video-player-module"></a><span data-ttu-id="9e174-103">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-103">Video player module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9e174-104">このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e174-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9e174-105">概要</span><span class="sxs-lookup"><span data-stu-id="9e174-105">Overview</span></span>

<span data-ttu-id="9e174-106">ビデオ プレーヤー モジュールは、ビデオの再生をサポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-106">Video player modules are used to support video playback.</span></span> <span data-ttu-id="9e174-107">ストア スタート キットには、アンビエント ビデオ プレーヤー モジュールと、ビデオ プレーヤー モジュールという 2 つのビデオ プレーヤー モジュールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9e174-107">Two video player modules are provided in the store starter kit: the ambient video player module and the video player module.</span></span> <span data-ttu-id="9e174-108">どちらのプレイヤーも、.mp4 メディア タイプをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9e174-108">Both players support the .mp4 media type.</span></span>

## <a name="ambient-video-player-module"></a><span data-ttu-id="9e174-109">アンビエント ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-109">Ambient video player module</span></span>

<span data-ttu-id="9e174-110">アンビエント ビデオ プレーヤー モジュールは、短い情報ビデオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9e174-110">The ambient video player module supports short informational videos.</span></span> <span data-ttu-id="9e174-111">5 秒未満のビデオに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e174-111">It should be used for videos that are less than five seconds long.</span></span> <span data-ttu-id="9e174-112">このプレーヤーは、再生や一時停止など、限られたビデオ再生機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9e174-112">This player supports limited video playback capabilities, such as play and pause.</span></span>

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a><span data-ttu-id="9e174-113">E コマースでのアンビエント ビデオ プレーヤー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="9e174-113">Examples of ambient video player modules in e-Commerce</span></span>

- <span data-ttu-id="9e174-114">ホーム ページの新製品を強調するための短い情報ビデオ</span><span class="sxs-lookup"><span data-stu-id="9e174-114">Short informational videos that highlight new products on the home page</span></span>
- <span data-ttu-id="9e174-115">製品の詳細ページの製品機能を強調するため短い情報ビデオ</span><span class="sxs-lookup"><span data-stu-id="9e174-115">Short informational videos that highlight product features on a product details page</span></span>

### <a name="ambient-video-player-module-properties"></a><span data-ttu-id="9e174-116">アンビエント ビデオ プレーヤー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="9e174-116">Ambient video player module properties</span></span>

| <span data-ttu-id="9e174-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="9e174-117">Property name</span></span>     | <span data-ttu-id="9e174-118">金額</span><span class="sxs-lookup"><span data-stu-id="9e174-118">Value</span></span>                 | <span data-ttu-id="9e174-119">説明</span><span class="sxs-lookup"><span data-stu-id="9e174-119">Description</span></span> |
|-------------------|-----------------------|-------------|
| <span data-ttu-id="9e174-120">自動再生</span><span class="sxs-lookup"><span data-stu-id="9e174-120">Autoplay</span></span>          | <span data-ttu-id="9e174-121">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-121">**True** or **False**</span></span> | <span data-ttu-id="9e174-122">値が **True** に設定されている場合、ビデオは自動的に再生されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-122">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="9e174-123">ミュート</span><span class="sxs-lookup"><span data-stu-id="9e174-123">Mute</span></span>              | <span data-ttu-id="9e174-124">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-124">**True** or **False**</span></span> | <span data-ttu-id="9e174-125">値が **True** に設定されている場合、オーディオはミュートされます。</span><span class="sxs-lookup"><span data-stu-id="9e174-125">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="9e174-126">このプレーヤーの既定値は **True** です。</span><span class="sxs-lookup"><span data-stu-id="9e174-126">For this player, the default value is **True**.</span></span> <span data-ttu-id="9e174-127">Google Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-127">In the Google Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="9e174-128">ループ</span><span class="sxs-lookup"><span data-stu-id="9e174-128">Loop</span></span>              | <span data-ttu-id="9e174-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-129">**True** or **False**</span></span> | <span data-ttu-id="9e174-130">値が **True** に設定されている場合、ビデオはループで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-130">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="9e174-131">メディア</span><span class="sxs-lookup"><span data-stu-id="9e174-131">Media</span></span>             |  <span data-ttu-id="9e174-132">ビデオ ファイル パスおよび名前</span><span class="sxs-lookup"><span data-stu-id="9e174-132">Video file path and name</span></span> | <span data-ttu-id="9e174-133">ビデオ プレーヤーによって再生されるビデオ ファイル</span><span class="sxs-lookup"><span data-stu-id="9e174-133">The video file that is played by the video player.</span></span> |
| <span data-ttu-id="9e174-134">再生コントロール</span><span class="sxs-lookup"><span data-stu-id="9e174-134">Playback controls</span></span> | <span data-ttu-id="9e174-135">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-135">**True** or **False**</span></span> | <span data-ttu-id="9e174-136">値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-136">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="9e174-137">この値が **False** に設定されている場合は、再生/一時停止ボタンが表示されませんが、ユーザーはキーボードを使用してビデオを一時停止および再開できます。</span><span class="sxs-lookup"><span data-stu-id="9e174-137">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |

## <a name="video-player-module"></a><span data-ttu-id="9e174-138">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-138">Video player module</span></span>

<span data-ttu-id="9e174-139">ビデオ プレーヤー モジュールは、E コマース サイト上にビデオを紹介するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e174-139">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="9e174-140">再生、一時停止、フルサイズ モード、クローズド キャプションなど、すべての再生機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9e174-140">It supports all playback capabilities, such as play, pause, full-size mode, and closed captions.</span></span> <span data-ttu-id="9e174-141">また、ビデオ プレーヤー モジュールでは、Microsoft のアクセシビリティ標準を満たすための、クローズド キャプションのカスタマイズもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9e174-141">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="9e174-142">たとえば、フォント サイズや背景色をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="9e174-142">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="9e174-143">ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックもサポートします。</span><span class="sxs-lookup"><span data-stu-id="9e174-143">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="9e174-144">ビデオがアップロードされると、セカンダリ オーディオ トラックもアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="9e174-144">When a video is uploaded, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="9e174-145">ユーザーが選択した場合、ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックを再生できます。</span><span class="sxs-lookup"><span data-stu-id="9e174-145">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="9e174-146">E コマースでのビデオ プレーヤー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="9e174-146">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="9e174-147">製品の詳細ページまたはマーケティング ページの説明ビデオ</span><span class="sxs-lookup"><span data-stu-id="9e174-147">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="9e174-148">プロモーション ビデオまたはマーケティング ページのポリシーに関するビデオ</span><span class="sxs-lookup"><span data-stu-id="9e174-148">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="9e174-149">製品の詳細ページまたはマーケティング ページの製品機能を強調するマーケティング ビデオ</span><span class="sxs-lookup"><span data-stu-id="9e174-149">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="9e174-150">ビデオ プレーヤー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="9e174-150">Video player module properties</span></span>

| <span data-ttu-id="9e174-151">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="9e174-151">Property name</span></span>         | <span data-ttu-id="9e174-152">金額</span><span class="sxs-lookup"><span data-stu-id="9e174-152">Value</span></span>                               | <span data-ttu-id="9e174-153">説明</span><span class="sxs-lookup"><span data-stu-id="9e174-153">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="9e174-154">自動再生</span><span class="sxs-lookup"><span data-stu-id="9e174-154">Auto play</span></span>             | <span data-ttu-id="9e174-155">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-155">**True** or **False**</span></span>               | <span data-ttu-id="9e174-156">値が **True** に設定されている場合、ビデオは自動的に再生されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-156">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="9e174-157">ミュート</span><span class="sxs-lookup"><span data-stu-id="9e174-157">Mute</span></span>                  | <span data-ttu-id="9e174-158">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-158">**True** or **False**</span></span>               | <span data-ttu-id="9e174-159">値が **True** に設定されている場合、オーディオはミュートされます。</span><span class="sxs-lookup"><span data-stu-id="9e174-159">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="9e174-160">このプレーヤーの既定値は **False** です。</span><span class="sxs-lookup"><span data-stu-id="9e174-160">For this player, the default value is **False**.</span></span> <span data-ttu-id="9e174-161">Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-161">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="9e174-162">ループ</span><span class="sxs-lookup"><span data-stu-id="9e174-162">Loop</span></span>                  | <span data-ttu-id="9e174-163">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-163">**True** or **False**</span></span>               | <span data-ttu-id="9e174-164">値が **True** に設定されている場合、ビデオはループで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-164">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="9e174-165">メディア</span><span class="sxs-lookup"><span data-stu-id="9e174-165">Media</span></span>                 | <span data-ttu-id="9e174-166">ビデオ ファイル パスおよび名前</span><span class="sxs-lookup"><span data-stu-id="9e174-166">Video file path and name</span></span> | <span data-ttu-id="9e174-167">ビデオ プレーヤーで再生されるビデオ ファイル</span><span class="sxs-lookup"><span data-stu-id="9e174-167">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="9e174-168">再生コントロール</span><span class="sxs-lookup"><span data-stu-id="9e174-168">Playback controls</span></span>     | <span data-ttu-id="9e174-169">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-169">**True** or **False**</span></span>               | <span data-ttu-id="9e174-170">値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-170">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="9e174-171">この値が **False** に設定されている場合は、再生/一時停止ボタンが表示されませんが、ユーザーはキーボードを使用してビデオを一時停止および再開できます。</span><span class="sxs-lookup"><span data-stu-id="9e174-171">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |
| <span data-ttu-id="9e174-172">フルスクリーン再生</span><span class="sxs-lookup"><span data-stu-id="9e174-172">Play fullscreen</span></span>       | <span data-ttu-id="9e174-173">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-173">**True** or **False**</span></span>               | <span data-ttu-id="9e174-174">値が **True** に設定されている場合、ビデオはフルスクリーン モードで再生されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-174">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="9e174-175">コントロール</span><span class="sxs-lookup"><span data-stu-id="9e174-175">Controls</span></span>              | <span data-ttu-id="9e174-176">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-176">**True** or **False**</span></span>               | <span data-ttu-id="9e174-177">値が **True** に設定されている場合は、すべてのコントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-177">When the value is set to **True**, all controls are shown.</span></span> <span data-ttu-id="9e174-178">これらのコントロールには、再生ボタンと一時停止ボタン、進捗状況インジケーター、およびクローズド キャプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e174-178">These controls include play and pause buttons, a progress indicator, and closed captions.</span></span> |
| <span data-ttu-id="9e174-179">ポスター フレームを非表示にする</span><span class="sxs-lookup"><span data-stu-id="9e174-179">Hide poster frame</span></span>     | <span data-ttu-id="9e174-180">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="9e174-180">**True** or **False**</span></span>               | <span data-ttu-id="9e174-181">ビデオにはポスター フレームを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9e174-181">A video can have a poster frame.</span></span> <span data-ttu-id="9e174-182">このプロパティの値が **True** に設定されている場合、ポスター フレームは非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="9e174-182">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="9e174-183">マスク レベル</span><span class="sxs-lookup"><span data-stu-id="9e174-183">Mask level</span></span>            | <span data-ttu-id="9e174-184">**0** から **100** までの数字</span><span class="sxs-lookup"><span data-stu-id="9e174-184">A number from **0** through **100**</span></span> | <span data-ttu-id="9e174-185">スタイル設定のためにビデオに適用されるマスク。</span><span class="sxs-lookup"><span data-stu-id="9e174-185">The mask that is applied to the video for styling.</span></span> |
| <span data-ttu-id="9e174-186">フルスクリーン アイコン スタイル</span><span class="sxs-lookup"><span data-stu-id="9e174-186">Fullscreen icon style</span></span> | <span data-ttu-id="9e174-187">**正方形**または**矢印**</span><span class="sxs-lookup"><span data-stu-id="9e174-187">**Square** or **Arrow**</span></span>             | <span data-ttu-id="9e174-188">ビデオ プレーヤーに表示されるフルスクリーン アイコンのスタイル。</span><span class="sxs-lookup"><span data-stu-id="9e174-188">The style of the full-screen icon that is shown in the video player.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="9e174-189">ビデオ プレーヤー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="9e174-189">Add a video player module to a page</span></span>

<span data-ttu-id="9e174-190">新しいページにビデオ プレーヤー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9e174-190">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9e174-191">**ビデオ プレーヤー テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e174-191">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="9e174-192">既定のページの**メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="9e174-192">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="9e174-193">コンテナー モジュールで、ビデオ プレーヤーおよびアンビエント ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="9e174-193">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="9e174-194">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="9e174-194">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="9e174-195">作成したビデオ プレーヤー テンプレートを使用して、**ビデオ プレーヤー ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e174-195">Use the video player template that you just created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="9e174-196">新しいページの**メイン** スロットで、アンビエント ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="9e174-196">In the **Main** slot of the new page, add an ambient video player module.</span></span>
1. <span data-ttu-id="9e174-197">アンビエント ビデオ プレーヤー モジュールの設定で、**メディア**に移動し、ビデオ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="9e174-197">In the settings for the ambient video player module, go to **Media**, and upload a video file.</span></span> <span data-ttu-id="9e174-198">**自動再生**、**ループ**などのプロパティは、必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="9e174-198">You can change the **Autoplay**, **Loop**, and other properties as you require.</span></span>
1. <span data-ttu-id="9e174-199">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="9e174-199">Save and preview the page.</span></span>
1. <span data-ttu-id="9e174-200">新しいページの**メイン** スロットで、ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="9e174-200">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="9e174-201">ビデオ プレーヤー モジュールの設定で、**メディア**に移動し、ビデオ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="9e174-201">In the settings for the video player module, go to **Media**, and upload a video file.</span></span>
1. <span data-ttu-id="9e174-202">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="9e174-202">Save and preview the page.</span></span> <span data-ttu-id="9e174-203">ページに両方のビデオ モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e174-203">You should see both video modules on the page.</span></span> <span data-ttu-id="9e174-204">その他の設定を変更して、各モジュールの動作をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="9e174-204">You can change additional settings to customize the behavior of each module.</span></span>
1. <span data-ttu-id="9e174-205">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="9e174-205">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e174-206">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9e174-206">Additional resources</span></span>

[<span data-ttu-id="9e174-207">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="9e174-207">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9e174-208">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-208">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="9e174-209">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-209">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="9e174-210">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-210">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9e174-211">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-211">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="9e174-212">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-212">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="9e174-213">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="9e174-213">Hero module</span></span>](add-hero-module.md)
