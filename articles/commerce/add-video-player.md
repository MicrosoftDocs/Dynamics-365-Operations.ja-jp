---
title: ビデオ プレーヤー モジュール
description: このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 32504351f712c83ba8f593c17d2e51c532374311
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785332"
---
# <a name="video-player-module"></a><span data-ttu-id="a1a01-103">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-103">Video player module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a1a01-104">このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a1a01-105">概要</span><span class="sxs-lookup"><span data-stu-id="a1a01-105">Overview</span></span>

<span data-ttu-id="a1a01-106">ビデオ プレーヤー モジュールは、ビデオの再生をサポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-106">Video player modules are used to support video playback.</span></span> <span data-ttu-id="a1a01-107">ストア スタート キットには、アンビエント ビデオ プレーヤー モジュールと、ビデオ プレーヤー モジュールという 2 つのビデオ プレーヤー モジュールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="a1a01-107">Two video player modules are provided in the store starter kit: the ambient video player module and the video player module.</span></span> <span data-ttu-id="a1a01-108">どちらのプレイヤーも、.mp4 メディア タイプをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a1a01-108">Both players support the .mp4 media type.</span></span>

## <a name="ambient-video-player-module"></a><span data-ttu-id="a1a01-109">アンビエント ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-109">Ambient video player module</span></span>

<span data-ttu-id="a1a01-110">アンビエント ビデオ プレーヤー モジュールは、短い情報ビデオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a1a01-110">The ambient video player module supports short informational videos.</span></span> <span data-ttu-id="a1a01-111">5 秒未満のビデオに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1a01-111">It should be used for videos that are less than five seconds long.</span></span> <span data-ttu-id="a1a01-112">このプレーヤーは、再生や一時停止など、限られたビデオ再生機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a1a01-112">This player supports limited video playback capabilities, such as play and pause.</span></span>

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a><span data-ttu-id="a1a01-113">E コマースでのアンビエント ビデオ プレーヤー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="a1a01-113">Examples of ambient video player modules in e-Commerce</span></span>

- <span data-ttu-id="a1a01-114">ホーム ページの新製品を強調するための短い情報ビデオ</span><span class="sxs-lookup"><span data-stu-id="a1a01-114">Short informational videos that highlight new products on the home page</span></span>
- <span data-ttu-id="a1a01-115">製品の詳細ページの製品機能を強調するため短い情報ビデオ</span><span class="sxs-lookup"><span data-stu-id="a1a01-115">Short informational videos that highlight product features on a product details page</span></span>

### <a name="ambient-video-player-module-properties"></a><span data-ttu-id="a1a01-116">アンビエント ビデオ プレーヤー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a1a01-116">Ambient video player module properties</span></span>

| <span data-ttu-id="a1a01-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a1a01-117">Property name</span></span>     | <span data-ttu-id="a1a01-118">金額</span><span class="sxs-lookup"><span data-stu-id="a1a01-118">Value</span></span>                 | <span data-ttu-id="a1a01-119">説明</span><span class="sxs-lookup"><span data-stu-id="a1a01-119">Description</span></span> |
|-------------------|-----------------------|-------------|
| <span data-ttu-id="a1a01-120">自動再生</span><span class="sxs-lookup"><span data-stu-id="a1a01-120">Autoplay</span></span>          | <span data-ttu-id="a1a01-121">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-121">**True** or **False**</span></span> | <span data-ttu-id="a1a01-122">値が **True** に設定されている場合、ビデオは自動的に再生されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-122">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="a1a01-123">ミュート</span><span class="sxs-lookup"><span data-stu-id="a1a01-123">Mute</span></span>              | <span data-ttu-id="a1a01-124">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-124">**True** or **False**</span></span> | <span data-ttu-id="a1a01-125">値が **True** に設定されている場合、オーディオはミュートされます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-125">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="a1a01-126">このプレーヤーの既定値は **True** です。</span><span class="sxs-lookup"><span data-stu-id="a1a01-126">For this player, the default value is **True**.</span></span> <span data-ttu-id="a1a01-127">Google Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-127">In the Google Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="a1a01-128">ループ</span><span class="sxs-lookup"><span data-stu-id="a1a01-128">Loop</span></span>              | <span data-ttu-id="a1a01-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-129">**True** or **False**</span></span> | <span data-ttu-id="a1a01-130">値が **True** に設定されている場合、ビデオはループで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-130">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="a1a01-131">メディア</span><span class="sxs-lookup"><span data-stu-id="a1a01-131">Media</span></span>             |  <span data-ttu-id="a1a01-132">ビデオ ファイル パスおよび名前</span><span class="sxs-lookup"><span data-stu-id="a1a01-132">Video file path and name</span></span> | <span data-ttu-id="a1a01-133">ビデオ プレーヤーによって再生されるビデオ ファイル</span><span class="sxs-lookup"><span data-stu-id="a1a01-133">The video file that is played by the video player.</span></span> |
| <span data-ttu-id="a1a01-134">再生コントロール</span><span class="sxs-lookup"><span data-stu-id="a1a01-134">Playback controls</span></span> | <span data-ttu-id="a1a01-135">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-135">**True** or **False**</span></span> | <span data-ttu-id="a1a01-136">値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-136">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="a1a01-137">この値が **False** に設定されている場合は、再生/一時停止ボタンが表示されませんが、ユーザーはキーボードを使用してビデオを一時停止および再開できます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-137">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |

## <a name="video-player-module"></a><span data-ttu-id="a1a01-138">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-138">Video player module</span></span>

<span data-ttu-id="a1a01-139">ビデオ プレーヤー モジュールは、E コマース サイト上にビデオを紹介するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-139">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="a1a01-140">再生、一時停止、フルサイズ モード、クローズド キャプションなど、すべての再生機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a1a01-140">It supports all playback capabilities, such as play, pause, full-size mode, and closed captions.</span></span> <span data-ttu-id="a1a01-141">また、ビデオ プレーヤー モジュールでは、Microsoft のアクセシビリティ標準を満たすための、クローズド キャプションのカスタマイズもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a1a01-141">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="a1a01-142">たとえば、フォント サイズや背景色をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-142">For example, you can customize the font size and background color.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="a1a01-143">E コマースでのビデオ プレーヤー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="a1a01-143">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="a1a01-144">製品の詳細ページまたはマーケティング ページの説明ビデオ</span><span class="sxs-lookup"><span data-stu-id="a1a01-144">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="a1a01-145">プロモーション ビデオまたはマーケティング ページのポリシーに関するビデオ</span><span class="sxs-lookup"><span data-stu-id="a1a01-145">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="a1a01-146">製品の詳細ページまたはマーケティング ページの製品機能を強調するマーケティング ビデオ</span><span class="sxs-lookup"><span data-stu-id="a1a01-146">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="a1a01-147">ビデオ プレーヤー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a1a01-147">Video player module properties</span></span>

| <span data-ttu-id="a1a01-148">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a1a01-148">Property name</span></span>         | <span data-ttu-id="a1a01-149">金額</span><span class="sxs-lookup"><span data-stu-id="a1a01-149">Value</span></span>                               | <span data-ttu-id="a1a01-150">説明</span><span class="sxs-lookup"><span data-stu-id="a1a01-150">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="a1a01-151">自動再生</span><span class="sxs-lookup"><span data-stu-id="a1a01-151">Auto play</span></span>             | <span data-ttu-id="a1a01-152">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-152">**True** or **False**</span></span>               | <span data-ttu-id="a1a01-153">値が **True** に設定されている場合、ビデオは自動的に再生されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-153">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="a1a01-154">ミュート</span><span class="sxs-lookup"><span data-stu-id="a1a01-154">Mute</span></span>                  | <span data-ttu-id="a1a01-155">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-155">**True** or **False**</span></span>               | <span data-ttu-id="a1a01-156">値が **True** に設定されている場合、オーディオはミュートされます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-156">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="a1a01-157">このプレーヤーの既定値は **False** です。</span><span class="sxs-lookup"><span data-stu-id="a1a01-157">For this player, the default value is **False**.</span></span> <span data-ttu-id="a1a01-158">Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-158">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="a1a01-159">ループ</span><span class="sxs-lookup"><span data-stu-id="a1a01-159">Loop</span></span>                  | <span data-ttu-id="a1a01-160">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-160">**True** or **False**</span></span>               | <span data-ttu-id="a1a01-161">値が **True** に設定されている場合、ビデオはループで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-161">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="a1a01-162">メディア</span><span class="sxs-lookup"><span data-stu-id="a1a01-162">Media</span></span>                 | <span data-ttu-id="a1a01-163">ビデオ ファイル パスおよび名前</span><span class="sxs-lookup"><span data-stu-id="a1a01-163">Video file path and name</span></span> | <span data-ttu-id="a1a01-164">ビデオ プレーヤーで再生されるビデオ ファイル</span><span class="sxs-lookup"><span data-stu-id="a1a01-164">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="a1a01-165">再生コントロール</span><span class="sxs-lookup"><span data-stu-id="a1a01-165">Playback controls</span></span>     | <span data-ttu-id="a1a01-166">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-166">**True** or **False**</span></span>               | <span data-ttu-id="a1a01-167">値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-167">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="a1a01-168">この値が **False** に設定されている場合は、再生/一時停止ボタンが表示されませんが、ユーザーはキーボードを使用してビデオを一時停止および再開できます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-168">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |
| <span data-ttu-id="a1a01-169">フルスクリーン再生</span><span class="sxs-lookup"><span data-stu-id="a1a01-169">Play fullscreen</span></span>       | <span data-ttu-id="a1a01-170">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-170">**True** or **False**</span></span>               | <span data-ttu-id="a1a01-171">値が **True** に設定されている場合、ビデオはフルスクリーン モードで再生されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-171">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="a1a01-172">コントロール</span><span class="sxs-lookup"><span data-stu-id="a1a01-172">Controls</span></span>              | <span data-ttu-id="a1a01-173">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-173">**True** or **False**</span></span>               | <span data-ttu-id="a1a01-174">値が **True** に設定されている場合は、すべてのコントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-174">When the value is set to **True**, all controls are shown.</span></span> <span data-ttu-id="a1a01-175">これらのコントロールには、再生ボタンと一時停止ボタン、進捗状況インジケーター、およびクローズド キャプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-175">These controls include play and pause buttons, a progress indicator, and closed captions.</span></span> |
| <span data-ttu-id="a1a01-176">ポスター フレームを非表示にする</span><span class="sxs-lookup"><span data-stu-id="a1a01-176">Hide poster frame</span></span>     | <span data-ttu-id="a1a01-177">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="a1a01-177">**True** or **False**</span></span>               | <span data-ttu-id="a1a01-178">ビデオにはポスター フレームを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-178">A video can have a poster frame.</span></span> <span data-ttu-id="a1a01-179">このプロパティの値が **True** に設定されている場合、ポスター フレームは非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="a1a01-179">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="a1a01-180">マスク レベル</span><span class="sxs-lookup"><span data-stu-id="a1a01-180">Mask level</span></span>            | <span data-ttu-id="a1a01-181">**0** から **100** までの数字</span><span class="sxs-lookup"><span data-stu-id="a1a01-181">A number from **0** through **100**</span></span> | <span data-ttu-id="a1a01-182">スタイル設定のためにビデオに適用されるマスク。</span><span class="sxs-lookup"><span data-stu-id="a1a01-182">The mask that is applied to the video for styling.</span></span> |
| <span data-ttu-id="a1a01-183">フルスクリーン アイコン スタイル</span><span class="sxs-lookup"><span data-stu-id="a1a01-183">Fullscreen icon style</span></span> | <span data-ttu-id="a1a01-184">**正方形**または**矢印**</span><span class="sxs-lookup"><span data-stu-id="a1a01-184">**Square** or **Arrow**</span></span>             | <span data-ttu-id="a1a01-185">ビデオ プレーヤーに表示されるフルスクリーン アイコンのスタイル。</span><span class="sxs-lookup"><span data-stu-id="a1a01-185">The style of the full-screen icon that is shown in the video player.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="a1a01-186">ビデオ プレーヤー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="a1a01-186">Add a video player module to a page</span></span>

<span data-ttu-id="a1a01-187">新しいページにビデオ プレーヤー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-187">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a1a01-188">**ビデオ プレーヤー テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-188">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="a1a01-189">既定のページの**メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-189">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="a1a01-190">コンテナー モジュールで、ビデオ プレーヤーおよびアンビエント ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-190">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="a1a01-191">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-191">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="a1a01-192">作成したビデオ プレーヤー テンプレートを使用して、**ビデオ プレーヤー ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-192">Use the video player template that you just created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="a1a01-193">新しいページの**メイン** スロットで、アンビエント ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-193">In the **Main** slot of the new page, add an ambient video player module.</span></span>
1. <span data-ttu-id="a1a01-194">アンビエント ビデオ プレーヤー モジュールの設定で、**メディア**に移動し、ビデオ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="a1a01-194">In the settings for the ambient video player module, go to **Media**, and upload a video file.</span></span> <span data-ttu-id="a1a01-195">**自動再生**、**ループ**などのプロパティは、必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-195">You can change the **Autoplay**, **Loop**, and other properties as you require.</span></span>
1. <span data-ttu-id="a1a01-196">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="a1a01-196">Save and preview the page.</span></span>
1. <span data-ttu-id="a1a01-197">新しいページの**メイン** スロットで、ビデオ プレーヤー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-197">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="a1a01-198">ビデオ プレーヤー モジュールの設定で、**メディア**に移動し、ビデオ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="a1a01-198">In the settings for the video player module, go to **Media**, and upload a video file.</span></span>
1. <span data-ttu-id="a1a01-199">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="a1a01-199">Save and preview the page.</span></span> <span data-ttu-id="a1a01-200">ページに両方のビデオ モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-200">You should see both video modules on the page.</span></span> <span data-ttu-id="a1a01-201">その他の設定を変更して、各モジュールの動作をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="a1a01-201">You can change additional settings to customize the behavior of each module.</span></span>
1. <span data-ttu-id="a1a01-202">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="a1a01-202">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1a01-203">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a1a01-203">Additional resources</span></span>

[<span data-ttu-id="a1a01-204">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="a1a01-204">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a1a01-205">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-205">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="a1a01-206">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-206">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a1a01-207">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-207">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a1a01-208">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-208">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="a1a01-209">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-209">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="a1a01-210">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="a1a01-210">Hero module</span></span>](add-hero-module.md)
