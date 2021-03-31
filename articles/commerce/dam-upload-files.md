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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222540"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="fdaa7-103">画像とビデオ以外のファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="fdaa7-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fdaa7-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像とビデオ以外のファイルをアップロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="fdaa7-105">概要</span><span class="sxs-lookup"><span data-stu-id="fdaa7-105">Overview</span></span>

<span data-ttu-id="fdaa7-106">コマース サイト ビルダーのメディア ライブラリーでは、画像またはビデオ以外のバイナリ資産のアップロードがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="fdaa7-107">たとえば、Microsoft Excel、Microsoft Word、Microsoft PowerPoint、または PDF ファイルをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="fdaa7-108">次のドキュメント タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-108">The following document types are supported:</span></span>
- <span data-ttu-id="fdaa7-109">7Z</span><span class="sxs-lookup"><span data-stu-id="fdaa7-109">7Z</span></span>
- <span data-ttu-id="fdaa7-110">AVI</span><span class="sxs-lookup"><span data-stu-id="fdaa7-110">AVI</span></span>
- <span data-ttu-id="fdaa7-111">CS</span><span class="sxs-lookup"><span data-stu-id="fdaa7-111">CS</span></span>
- <span data-ttu-id="fdaa7-112">CSS</span><span class="sxs-lookup"><span data-stu-id="fdaa7-112">CSS</span></span>
- <span data-ttu-id="fdaa7-113">DOC</span><span class="sxs-lookup"><span data-stu-id="fdaa7-113">DOC</span></span>
- <span data-ttu-id="fdaa7-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="fdaa7-114">DOCX</span></span>
- <span data-ttu-id="fdaa7-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="fdaa7-115">EPUB</span></span>
- <span data-ttu-id="fdaa7-116">GIF</span><span class="sxs-lookup"><span data-stu-id="fdaa7-116">GIF</span></span>
- <span data-ttu-id="fdaa7-117">INDD</span><span class="sxs-lookup"><span data-stu-id="fdaa7-117">INDD</span></span>
- <span data-ttu-id="fdaa7-118">JAR</span><span class="sxs-lookup"><span data-stu-id="fdaa7-118">JAR</span></span>
- <span data-ttu-id="fdaa7-119">JPG</span><span class="sxs-lookup"><span data-stu-id="fdaa7-119">JPG</span></span>
- <span data-ttu-id="fdaa7-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="fdaa7-120">JPEG</span></span>
- <span data-ttu-id="fdaa7-121">JS</span><span class="sxs-lookup"><span data-stu-id="fdaa7-121">JS</span></span>
- <span data-ttu-id="fdaa7-122">MP3</span><span class="sxs-lookup"><span data-stu-id="fdaa7-122">MP3</span></span>
- <span data-ttu-id="fdaa7-123">MP4</span><span class="sxs-lookup"><span data-stu-id="fdaa7-123">MP4</span></span>
- <span data-ttu-id="fdaa7-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="fdaa7-124">MPEG</span></span>
- <span data-ttu-id="fdaa7-125">MPG</span><span class="sxs-lookup"><span data-stu-id="fdaa7-125">MPG</span></span>
- <span data-ttu-id="fdaa7-126">ODP</span><span class="sxs-lookup"><span data-stu-id="fdaa7-126">ODP</span></span>
- <span data-ttu-id="fdaa7-127">ODS</span><span class="sxs-lookup"><span data-stu-id="fdaa7-127">ODS</span></span>
- <span data-ttu-id="fdaa7-128">ODT</span><span class="sxs-lookup"><span data-stu-id="fdaa7-128">ODT</span></span>
- <span data-ttu-id="fdaa7-129">PDF</span><span class="sxs-lookup"><span data-stu-id="fdaa7-129">PDF</span></span>
- <span data-ttu-id="fdaa7-130">PNG</span><span class="sxs-lookup"><span data-stu-id="fdaa7-130">PNG</span></span>
- <span data-ttu-id="fdaa7-131">PPT</span><span class="sxs-lookup"><span data-stu-id="fdaa7-131">PPT</span></span>
- <span data-ttu-id="fdaa7-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="fdaa7-132">PPTX</span></span>
- <span data-ttu-id="fdaa7-133">PS</span><span class="sxs-lookup"><span data-stu-id="fdaa7-133">PS</span></span>
- <span data-ttu-id="fdaa7-134">QXP</span><span class="sxs-lookup"><span data-stu-id="fdaa7-134">QXP</span></span>
- <span data-ttu-id="fdaa7-135">RAR</span><span class="sxs-lookup"><span data-stu-id="fdaa7-135">RAR</span></span>
- <span data-ttu-id="fdaa7-136">RTF</span><span class="sxs-lookup"><span data-stu-id="fdaa7-136">RTF</span></span>
- <span data-ttu-id="fdaa7-137">SVG</span><span class="sxs-lookup"><span data-stu-id="fdaa7-137">SVG</span></span>
- <span data-ttu-id="fdaa7-138">TAR</span><span class="sxs-lookup"><span data-stu-id="fdaa7-138">TAR</span></span>
- <span data-ttu-id="fdaa7-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="fdaa7-139">TGZ</span></span>
- <span data-ttu-id="fdaa7-140">TXT</span><span class="sxs-lookup"><span data-stu-id="fdaa7-140">TXT</span></span>
- <span data-ttu-id="fdaa7-141">WMV</span><span class="sxs-lookup"><span data-stu-id="fdaa7-141">WMV</span></span>
- <span data-ttu-id="fdaa7-142">XLS</span><span class="sxs-lookup"><span data-stu-id="fdaa7-142">XLS</span></span>
- <span data-ttu-id="fdaa7-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="fdaa7-143">XLSX</span></span>
- <span data-ttu-id="fdaa7-144">XML</span><span class="sxs-lookup"><span data-stu-id="fdaa7-144">XML</span></span>
- <span data-ttu-id="fdaa7-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="fdaa7-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="fdaa7-146">ファイルをアップロード</span><span class="sxs-lookup"><span data-stu-id="fdaa7-146">Upload a file</span></span>

<span data-ttu-id="fdaa7-147">コマース サイト ビルダーでファイルをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fdaa7-148">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="fdaa7-149">コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="fdaa7-150">ファイル エクスプローラーで、1 つ以上のファイルを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="fdaa7-151">**メディア項目のアップロード** ダイアログ ボックスで、タイトル、説明、キーワードのメタデータを必要に応じて入力します。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="fdaa7-152">ファイルをアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="fdaa7-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaa7-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdaa7-154">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fdaa7-154">Additional resources</span></span>

[<span data-ttu-id="fdaa7-155">資産管理の概要をデジタル化</span><span class="sxs-lookup"><span data-stu-id="fdaa7-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="fdaa7-156">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="fdaa7-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="fdaa7-157">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="fdaa7-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="fdaa7-158">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="fdaa7-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="fdaa7-159">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="fdaa7-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="fdaa7-160">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="fdaa7-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]