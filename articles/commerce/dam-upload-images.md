---
title: 画像のアップロード
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像のアップロード方法について説明します。
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
ms.openlocfilehash: f562d3376fde6a24e6a1e1a3f7f4192cf290ae90
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594287"
---
# <a name="upload-images"></a><span data-ttu-id="b216a-103">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="b216a-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b216a-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像のアップロード方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b216a-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="b216a-105">概要</span><span class="sxs-lookup"><span data-stu-id="b216a-105">Overview</span></span>

<span data-ttu-id="b216a-106">コマース サイト ビルダーのメディア ライブラリーを使用すると、フォルダーを使用してイメージを単独または一括でアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="b216a-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="b216a-107">イメージの変更コンポーネントを使用すると、さまざまなビューポートとそのブレークポイントに対する画像が自動的に最適化されるので、最大解像度と品質で画像のバージョンをアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b216a-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="b216a-108">アップロード中に指定された画像情報</span><span class="sxs-lookup"><span data-stu-id="b216a-108">Image information specified during upload</span></span>

<span data-ttu-id="b216a-109">画像をアップロードする場合は、次の情報を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b216a-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="b216a-110">**タイトル、代替テキスト、説明、キーワード**: イメージのメタデータまたは画像。</span><span class="sxs-lookup"><span data-stu-id="b216a-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="b216a-111">タイトルと代替テキストは必要な値です。</span><span class="sxs-lookup"><span data-stu-id="b216a-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="b216a-112">**カテゴリの選択**:</span><span class="sxs-lookup"><span data-stu-id="b216a-112">**Select category**:</span></span>
    - <span data-ttu-id="b216a-113">**なし**: E コマースのストーリーテリング イメージまたは画像に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b216a-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="b216a-114">**製品、カテゴリ、顧客、従業員、カタログ**: Dynamics 365 Commerce オムニ チャネルのイメージまたは画像に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b216a-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="b216a-115">**アップロード後にアセットを公開**: このチェック ボックスがオンになっている場合は、アップロード後すぐにイメージまたは画像が公開されます。</span><span class="sxs-lookup"><span data-stu-id="b216a-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="b216a-116">カテゴリが割り当てられた画像の資産には、特定のカテゴリの資産の検索を支援するキーワードとして自動的にカテゴリにタグが付けられます。</span><span class="sxs-lookup"><span data-stu-id="b216a-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="b216a-117">オムニ チャネル画像の命名規則</span><span class="sxs-lookup"><span data-stu-id="b216a-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="b216a-118">メディア ライブラリをオムニ チャネル画像のバックエンドとしてコンフィギュレーションしている場合は、イメージ カテゴリを使用して、アップロードしたイメージが属するカテゴリを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b216a-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="b216a-119">また、販売時点管理 (POS)などのその他のチャネルによって、画像が正しく取得されているか確認するために命名規則も用意されています。</span><span class="sxs-lookup"><span data-stu-id="b216a-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="b216a-120">既定の命名規則は、カテゴリによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b216a-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="b216a-121">カタログの画像は、"**/カタログ/\{LanguageId\}/\{CatalogName\}.jpg**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="b216a-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="b216a-122">カテゴリ画像は、"**/カテゴリ/\{CategoryName\}.png**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="b216a-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="b216a-123">顧客の画像は、"**/顧客/\{CustomerNumber\}.jpg**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="b216a-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="b216a-124">従業員の画像は、"**/作業者/\{WorkerNumber\}.jpg**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="b216a-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="b216a-125">製品画像は、"**/製品/\{ProductNumber\}_000_001.png**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="b216a-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="b216a-126">001 は画像の順序で、001、002、003、004、または 005 とすることができます</span><span class="sxs-lookup"><span data-stu-id="b216a-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="b216a-127">製品バリアントの画像は、"**/製品/\{ProductNumber\}\_\{サイズ\}\_\{色\}\_\{スタイル\}\_000_001.png**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="b216a-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="b216a-128">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="b216a-128">Upload an image</span></span>

<span data-ttu-id="b216a-129">サイト ビルダーの画像をアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b216a-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b216a-130">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="b216a-131">コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="b216a-132">ファイル エクスプローラー ウィンドウで、アップロードする 1 つまたはそれ以上の画像ファイルに移動して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="b216a-133">**メディア項目のアップロード** ダイアログ ボックスで、必要なタイトルと代替テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="b216a-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="b216a-134">オプションの説明とキーワードを入力し、必要に応じてカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="b216a-135">画像をアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b216a-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="b216a-136">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="b216a-137">画像のフォルダのアップロード</span><span class="sxs-lookup"><span data-stu-id="b216a-137">Upload a folder of images</span></span>

<span data-ttu-id="b216a-138">サイト ビルダー内の画像のフォルダを一括アップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b216a-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b216a-139">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="b216a-140">コマンド バーで、**アップロード \> フォルダのアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="b216a-141">ファイル エクスプローラー ウィンドウで、アップロードするフォルダに移動して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="b216a-142">**メディア項目のアップロード** ダイアログ ボックスで、オプションのキーワードを入力し、必要に応じてカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="b216a-143">フォルダをアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b216a-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="b216a-144">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b216a-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b216a-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b216a-145">Additional resources</span></span>

[<span data-ttu-id="b216a-146">資産管理の概要をデジタル化</span><span class="sxs-lookup"><span data-stu-id="b216a-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="b216a-147">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="b216a-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="b216a-148">ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="b216a-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="b216a-149">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="b216a-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="b216a-150">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="b216a-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="b216a-151">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="b216a-151">Upload and serve static files</span></span>](upload-serve-static-files.md)
