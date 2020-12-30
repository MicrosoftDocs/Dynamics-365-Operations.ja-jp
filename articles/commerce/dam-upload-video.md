---
title: ビデオのアップロード
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーのビデオのアップロード方法について説明します。
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8dd9e710f9a6ea593a0673e7902fadf84ca05cff
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594311"
---
# <a name="upload-videos"></a><span data-ttu-id="83304-103">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="83304-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83304-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーのビデオのアップロード方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="83304-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="83304-105">概要</span><span class="sxs-lookup"><span data-stu-id="83304-105">Overview</span></span>

<span data-ttu-id="83304-106">コマース サイト ビルダーのメディア ライブラリーを使用すると、ビデオをアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="83304-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="83304-107">イメージの変更コンポーネントを使用すると、さまざまなビューポートとそのブレークポイントに対するビデオが適切に変換されるので、最大速度と解像度でビデオのバージョンをアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="83304-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="83304-108">アップロード中に指定されたビデオ情報</span><span class="sxs-lookup"><span data-stu-id="83304-108">Video information specified during upload</span></span>

<span data-ttu-id="83304-109">ビデオをアップロードする場合は、次の情報を指定できます。</span><span class="sxs-lookup"><span data-stu-id="83304-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="83304-110">**タイトル、説明、キーワード**: ビデオのメタデータ。</span><span class="sxs-lookup"><span data-stu-id="83304-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="83304-111">**クローズド キャプションの自動生成**: ビデオに対してクローズド キャプションを自動的に生成するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="83304-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="83304-112">**クローズド キャプション**: 使用するクローズド キャプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="83304-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="83304-113">**通常オーディオ**: 使用する通常のオーディオ トラックを指定します。</span><span class="sxs-lookup"><span data-stu-id="83304-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="83304-114">**サムネイル**: ビデオのサムネイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="83304-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="83304-115">指定しない場合は、自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="83304-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="83304-116">**記述オーディオ**: 使用する記述オーディオ トラックを指定します。</span><span class="sxs-lookup"><span data-stu-id="83304-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="83304-117">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="83304-117">Upload a video</span></span>

<span data-ttu-id="83304-118">サイト ビルダー内のビデオをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83304-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="83304-119">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83304-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="83304-120">コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83304-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="83304-121">ファイル エクスプローラー ウィンドウで、アップロードする 1 つまたはそれ以上のビデオ ファイルに移動して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83304-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="83304-122">**メディア項目のアップロード** ダイアログ ボックスで、必要なタイトルと代替テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="83304-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="83304-123">オプションの説明とキーワードを入力し、必要に応じてカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="83304-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="83304-124">画像をアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします</span><span class="sxs-lookup"><span data-stu-id="83304-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="83304-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83304-125">Select **OK**.</span></span>

<span data-ttu-id="83304-126">複数のタイプの資産を同時に アップロードしている場合(画像やビデオなど)、**メディア項目のアップロード** ダイアログ ボックスでは、キーワードの指定、アップロード後にファイルをすぐに公開するかどうか、およびビデオ ファイルにクローズ ドキャプションを自動的に生成するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="83304-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="83304-127">すべての資産が同じキーワードを共有します。</span><span class="sxs-lookup"><span data-stu-id="83304-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83304-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="83304-128">Additional resources</span></span>

[<span data-ttu-id="83304-129">資産管理の概要をデジタル化</span><span class="sxs-lookup"><span data-stu-id="83304-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="83304-130">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="83304-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="83304-131">ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="83304-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="83304-132">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="83304-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="83304-133">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="83304-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="83304-134">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="83304-134">Upload and serve static files</span></span>](upload-serve-static-files.md)
