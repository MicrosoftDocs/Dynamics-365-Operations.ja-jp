---
title: 画像とビデオ以外のファイルのアップロード
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像とビデオ以外のバイナリ ファイルをアップロードする方法について説明します。
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
ms.openlocfilehash: 4acd3bec32cdfe627f6eb33dd5dc652f7cff74a8
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594215"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="61ab1-103">画像とビデオ以外のファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="61ab1-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61ab1-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像とビデオ以外のファイルをアップロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="61ab1-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="61ab1-105">概要</span><span class="sxs-lookup"><span data-stu-id="61ab1-105">Overview</span></span>

<span data-ttu-id="61ab1-106">コマース サイト ビルダーのメディア ライブラリーでは、画像またはビデオ以外のバイナリ資産のアップロードがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="61ab1-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="61ab1-107">たとえば、Microsoft Excel、Microsoft Word、Microsoft PowerPoint、または PDF ファイルをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="61ab1-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="61ab1-108">次のドキュメント タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="61ab1-108">The following document types are supported:</span></span>
- <span data-ttu-id="61ab1-109">7Z</span><span class="sxs-lookup"><span data-stu-id="61ab1-109">7Z</span></span>
- <span data-ttu-id="61ab1-110">AVI</span><span class="sxs-lookup"><span data-stu-id="61ab1-110">AVI</span></span>
- <span data-ttu-id="61ab1-111">CS</span><span class="sxs-lookup"><span data-stu-id="61ab1-111">CS</span></span>
- <span data-ttu-id="61ab1-112">CSS</span><span class="sxs-lookup"><span data-stu-id="61ab1-112">CSS</span></span>
- <span data-ttu-id="61ab1-113">DOC</span><span class="sxs-lookup"><span data-stu-id="61ab1-113">DOC</span></span>
- <span data-ttu-id="61ab1-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="61ab1-114">DOCX</span></span>
- <span data-ttu-id="61ab1-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="61ab1-115">EPUB</span></span>
- <span data-ttu-id="61ab1-116">GIF</span><span class="sxs-lookup"><span data-stu-id="61ab1-116">GIF</span></span>
- <span data-ttu-id="61ab1-117">INDD</span><span class="sxs-lookup"><span data-stu-id="61ab1-117">INDD</span></span>
- <span data-ttu-id="61ab1-118">JAR</span><span class="sxs-lookup"><span data-stu-id="61ab1-118">JAR</span></span>
- <span data-ttu-id="61ab1-119">JPG</span><span class="sxs-lookup"><span data-stu-id="61ab1-119">JPG</span></span>
- <span data-ttu-id="61ab1-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="61ab1-120">JPEG</span></span>
- <span data-ttu-id="61ab1-121">JS</span><span class="sxs-lookup"><span data-stu-id="61ab1-121">JS</span></span>
- <span data-ttu-id="61ab1-122">MP3</span><span class="sxs-lookup"><span data-stu-id="61ab1-122">MP3</span></span>
- <span data-ttu-id="61ab1-123">MP4</span><span class="sxs-lookup"><span data-stu-id="61ab1-123">MP4</span></span>
- <span data-ttu-id="61ab1-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="61ab1-124">MPEG</span></span>
- <span data-ttu-id="61ab1-125">MPG</span><span class="sxs-lookup"><span data-stu-id="61ab1-125">MPG</span></span>
- <span data-ttu-id="61ab1-126">ODP</span><span class="sxs-lookup"><span data-stu-id="61ab1-126">ODP</span></span>
- <span data-ttu-id="61ab1-127">ODS</span><span class="sxs-lookup"><span data-stu-id="61ab1-127">ODS</span></span>
- <span data-ttu-id="61ab1-128">ODT</span><span class="sxs-lookup"><span data-stu-id="61ab1-128">ODT</span></span>
- <span data-ttu-id="61ab1-129">PDF</span><span class="sxs-lookup"><span data-stu-id="61ab1-129">PDF</span></span>
- <span data-ttu-id="61ab1-130">PNG</span><span class="sxs-lookup"><span data-stu-id="61ab1-130">PNG</span></span>
- <span data-ttu-id="61ab1-131">PPT</span><span class="sxs-lookup"><span data-stu-id="61ab1-131">PPT</span></span>
- <span data-ttu-id="61ab1-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="61ab1-132">PPTX</span></span>
- <span data-ttu-id="61ab1-133">PS</span><span class="sxs-lookup"><span data-stu-id="61ab1-133">PS</span></span>
- <span data-ttu-id="61ab1-134">QXP</span><span class="sxs-lookup"><span data-stu-id="61ab1-134">QXP</span></span>
- <span data-ttu-id="61ab1-135">RAR</span><span class="sxs-lookup"><span data-stu-id="61ab1-135">RAR</span></span>
- <span data-ttu-id="61ab1-136">RTF</span><span class="sxs-lookup"><span data-stu-id="61ab1-136">RTF</span></span>
- <span data-ttu-id="61ab1-137">SVG</span><span class="sxs-lookup"><span data-stu-id="61ab1-137">SVG</span></span>
- <span data-ttu-id="61ab1-138">TAR</span><span class="sxs-lookup"><span data-stu-id="61ab1-138">TAR</span></span>
- <span data-ttu-id="61ab1-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="61ab1-139">TGZ</span></span>
- <span data-ttu-id="61ab1-140">TXT</span><span class="sxs-lookup"><span data-stu-id="61ab1-140">TXT</span></span>
- <span data-ttu-id="61ab1-141">WMV</span><span class="sxs-lookup"><span data-stu-id="61ab1-141">WMV</span></span>
- <span data-ttu-id="61ab1-142">XLS</span><span class="sxs-lookup"><span data-stu-id="61ab1-142">XLS</span></span>
- <span data-ttu-id="61ab1-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="61ab1-143">XLSX</span></span>
- <span data-ttu-id="61ab1-144">XML</span><span class="sxs-lookup"><span data-stu-id="61ab1-144">XML</span></span>
- <span data-ttu-id="61ab1-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="61ab1-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="61ab1-146">ファイルをアップロード</span><span class="sxs-lookup"><span data-stu-id="61ab1-146">Upload a file</span></span>

<span data-ttu-id="61ab1-147">コマース サイト ビルダーでファイルをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="61ab1-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="61ab1-148">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61ab1-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="61ab1-149">コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61ab1-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="61ab1-150">ファイル エクスプローラーで、1 つ以上のファイルを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61ab1-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="61ab1-151">**メディア項目のアップロード** ダイアログ ボックスで、タイトル、説明、キーワードのメタデータを必要に応じて入力します。</span><span class="sxs-lookup"><span data-stu-id="61ab1-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="61ab1-152">ファイルをアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="61ab1-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="61ab1-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61ab1-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61ab1-154">追加リソース</span><span class="sxs-lookup"><span data-stu-id="61ab1-154">Additional resources</span></span>

[<span data-ttu-id="61ab1-155">資産管理の概要をデジタル化</span><span class="sxs-lookup"><span data-stu-id="61ab1-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="61ab1-156">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="61ab1-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="61ab1-157">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="61ab1-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="61ab1-158">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="61ab1-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="61ab1-159">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="61ab1-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="61ab1-160">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="61ab1-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
