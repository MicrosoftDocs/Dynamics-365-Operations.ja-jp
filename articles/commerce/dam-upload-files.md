---
title: 画像とビデオ以外のファイルのアップロード
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像とビデオ以外のバイナリ ファイルをアップロードする方法について説明します。
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799256"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="1c457-103">画像とビデオ以外のファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="1c457-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c457-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像とビデオ以外のファイルをアップロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1c457-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="1c457-105">コマース サイト ビルダーのメディア ライブラリーでは、画像またはビデオ以外のバイナリ資産のアップロードがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1c457-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="1c457-106">たとえば、Microsoft Excel、Microsoft Word、Microsoft PowerPoint、または PDF ファイルをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="1c457-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="1c457-107">次のドキュメント タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1c457-107">The following document types are supported:</span></span>
- <span data-ttu-id="1c457-108">7Z</span><span class="sxs-lookup"><span data-stu-id="1c457-108">7Z</span></span>
- <span data-ttu-id="1c457-109">AVI</span><span class="sxs-lookup"><span data-stu-id="1c457-109">AVI</span></span>
- <span data-ttu-id="1c457-110">CS</span><span class="sxs-lookup"><span data-stu-id="1c457-110">CS</span></span>
- <span data-ttu-id="1c457-111">CSS</span><span class="sxs-lookup"><span data-stu-id="1c457-111">CSS</span></span>
- <span data-ttu-id="1c457-112">DOC</span><span class="sxs-lookup"><span data-stu-id="1c457-112">DOC</span></span>
- <span data-ttu-id="1c457-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="1c457-113">DOCX</span></span>
- <span data-ttu-id="1c457-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="1c457-114">EPUB</span></span>
- <span data-ttu-id="1c457-115">GIF</span><span class="sxs-lookup"><span data-stu-id="1c457-115">GIF</span></span>
- <span data-ttu-id="1c457-116">INDD</span><span class="sxs-lookup"><span data-stu-id="1c457-116">INDD</span></span>
- <span data-ttu-id="1c457-117">JAR</span><span class="sxs-lookup"><span data-stu-id="1c457-117">JAR</span></span>
- <span data-ttu-id="1c457-118">JPG</span><span class="sxs-lookup"><span data-stu-id="1c457-118">JPG</span></span>
- <span data-ttu-id="1c457-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="1c457-119">JPEG</span></span>
- <span data-ttu-id="1c457-120">JS</span><span class="sxs-lookup"><span data-stu-id="1c457-120">JS</span></span>
- <span data-ttu-id="1c457-121">MP3</span><span class="sxs-lookup"><span data-stu-id="1c457-121">MP3</span></span>
- <span data-ttu-id="1c457-122">MP4</span><span class="sxs-lookup"><span data-stu-id="1c457-122">MP4</span></span>
- <span data-ttu-id="1c457-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="1c457-123">MPEG</span></span>
- <span data-ttu-id="1c457-124">MPG</span><span class="sxs-lookup"><span data-stu-id="1c457-124">MPG</span></span>
- <span data-ttu-id="1c457-125">ODP</span><span class="sxs-lookup"><span data-stu-id="1c457-125">ODP</span></span>
- <span data-ttu-id="1c457-126">ODS</span><span class="sxs-lookup"><span data-stu-id="1c457-126">ODS</span></span>
- <span data-ttu-id="1c457-127">ODT</span><span class="sxs-lookup"><span data-stu-id="1c457-127">ODT</span></span>
- <span data-ttu-id="1c457-128">PDF</span><span class="sxs-lookup"><span data-stu-id="1c457-128">PDF</span></span>
- <span data-ttu-id="1c457-129">PNG</span><span class="sxs-lookup"><span data-stu-id="1c457-129">PNG</span></span>
- <span data-ttu-id="1c457-130">PPT</span><span class="sxs-lookup"><span data-stu-id="1c457-130">PPT</span></span>
- <span data-ttu-id="1c457-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="1c457-131">PPTX</span></span>
- <span data-ttu-id="1c457-132">PS</span><span class="sxs-lookup"><span data-stu-id="1c457-132">PS</span></span>
- <span data-ttu-id="1c457-133">QXP</span><span class="sxs-lookup"><span data-stu-id="1c457-133">QXP</span></span>
- <span data-ttu-id="1c457-134">RAR</span><span class="sxs-lookup"><span data-stu-id="1c457-134">RAR</span></span>
- <span data-ttu-id="1c457-135">RTF</span><span class="sxs-lookup"><span data-stu-id="1c457-135">RTF</span></span>
- <span data-ttu-id="1c457-136">SVG</span><span class="sxs-lookup"><span data-stu-id="1c457-136">SVG</span></span>
- <span data-ttu-id="1c457-137">TAR</span><span class="sxs-lookup"><span data-stu-id="1c457-137">TAR</span></span>
- <span data-ttu-id="1c457-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="1c457-138">TGZ</span></span>
- <span data-ttu-id="1c457-139">TXT</span><span class="sxs-lookup"><span data-stu-id="1c457-139">TXT</span></span>
- <span data-ttu-id="1c457-140">WMV</span><span class="sxs-lookup"><span data-stu-id="1c457-140">WMV</span></span>
- <span data-ttu-id="1c457-141">XLS</span><span class="sxs-lookup"><span data-stu-id="1c457-141">XLS</span></span>
- <span data-ttu-id="1c457-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="1c457-142">XLSX</span></span>
- <span data-ttu-id="1c457-143">XML</span><span class="sxs-lookup"><span data-stu-id="1c457-143">XML</span></span>
- <span data-ttu-id="1c457-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="1c457-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="1c457-145">ファイルをアップロード</span><span class="sxs-lookup"><span data-stu-id="1c457-145">Upload a file</span></span>

<span data-ttu-id="1c457-146">コマース サイト ビルダーでファイルをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1c457-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1c457-147">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c457-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="1c457-148">コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c457-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="1c457-149">ファイル エクスプローラーで、1 つ以上のファイルを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c457-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="1c457-150">**メディア項目のアップロード** ダイアログ ボックスで、タイトル、説明、キーワードのメタデータを必要に応じて入力します。</span><span class="sxs-lookup"><span data-stu-id="1c457-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="1c457-151">ファイルをアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="1c457-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="1c457-152">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c457-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c457-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1c457-153">Additional resources</span></span>

[<span data-ttu-id="1c457-154">資産管理の概要をデジタル化</span><span class="sxs-lookup"><span data-stu-id="1c457-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="1c457-155">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="1c457-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="1c457-156">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="1c457-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="1c457-157">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="1c457-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="1c457-158">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="1c457-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="1c457-159">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="1c457-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
