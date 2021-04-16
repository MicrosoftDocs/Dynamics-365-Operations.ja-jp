---
title: 画像のアップロード
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像アップロードの方法について説明します。
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799232"
---
# <a name="upload-images"></a><span data-ttu-id="2a51e-103">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="2a51e-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a51e-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像アップロードの方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="2a51e-105">コマース サイト ビルダーのメディア ライブラリーを使用すると、フォルダーを使用してイメージを単独または一括でアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="2a51e-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="2a51e-106">イメージの変更コンポーネントを使用すると、さまざまなビューポートとそのブレークポイントに対する画像が自動的に最適化されるので、最大解像度と品質で画像のバージョンをアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a51e-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="2a51e-107">アップロード中に指定された画像情報</span><span class="sxs-lookup"><span data-stu-id="2a51e-107">Image information specified during upload</span></span>

<span data-ttu-id="2a51e-108">画像をアップロードする場合は、次の情報を指定できます。</span><span class="sxs-lookup"><span data-stu-id="2a51e-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="2a51e-109">**タイトル、代替テキスト、説明、キーワード**: イメージのメタデータまたは画像。</span><span class="sxs-lookup"><span data-stu-id="2a51e-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="2a51e-110">タイトルと代替テキストは必要な値です。</span><span class="sxs-lookup"><span data-stu-id="2a51e-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="2a51e-111">**カテゴリの選択**:</span><span class="sxs-lookup"><span data-stu-id="2a51e-111">**Select category**:</span></span>
    - <span data-ttu-id="2a51e-112">**なし**: E コマースのストーリーテリング イメージまたは画像に使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a51e-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="2a51e-113">**製品、カテゴリ、顧客、従業員、カタログ**: Dynamics 365 Commerce オムニ チャネルのイメージまたは画像に使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a51e-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="2a51e-114">**アップロード後にアセットを公開**: このチェック ボックスがオンになっている場合は、アップロード後すぐにイメージまたは画像が公開されます。</span><span class="sxs-lookup"><span data-stu-id="2a51e-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="2a51e-115">カテゴリが割り当てられた画像の資産には、特定のカテゴリの資産の検索を支援するキーワードとして自動的にカテゴリにタグが付けられます。</span><span class="sxs-lookup"><span data-stu-id="2a51e-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="2a51e-116">オムニ チャネル画像の命名規則</span><span class="sxs-lookup"><span data-stu-id="2a51e-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="2a51e-117">メディア ライブラリをオムニ チャネル画像のバックエンドとしてコンフィギュレーションしている場合は、イメージ カテゴリを使用して、アップロードしたイメージが属するカテゴリを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2a51e-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="2a51e-118">また、販売時点管理 (POS)などのその他のチャネルによって、画像が正しく取得されているか確認するために命名規則も用意されています。</span><span class="sxs-lookup"><span data-stu-id="2a51e-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="2a51e-119">既定の命名規則は、カテゴリによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2a51e-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="2a51e-120">カタログの画像は、"**/カタログ/\{LanguageId\}/\{CatalogName\}.jpg**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="2a51e-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="2a51e-121">カテゴリ画像は、"**/カテゴリ/\{CategoryName\}.png**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="2a51e-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="2a51e-122">顧客の画像は、"**/顧客/\{CustomerNumber\}.jpg**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="2a51e-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="2a51e-123">従業員の画像は、"**/作業者/\{WorkerNumber\}.jpg**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="2a51e-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="2a51e-124">製品画像は、"**/製品/\{ProductNumber\}_000_001.png**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="2a51e-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="2a51e-125">001 は画像の順序で、001、002、003、004、または 005 とすることができます</span><span class="sxs-lookup"><span data-stu-id="2a51e-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="2a51e-126">製品バリアントの画像は、"**/製品/\{ProductNumber\} \^ \{スタイル\} \^ \{サイズ\} \^ \{色\} \^\_000_001.png**" という名前にする必要があります</span><span class="sxs-lookup"><span data-stu-id="2a51e-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="2a51e-127">例 : 93039 \^ \^ 2 \^ Black \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="2a51e-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="2a51e-128">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="2a51e-128">Upload an image</span></span>

<span data-ttu-id="2a51e-129">サイト ビルダーの画像をアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2a51e-130">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="2a51e-131">コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="2a51e-132">ファイル エクスプローラー ウィンドウで、アップロードする 1 つまたはそれ以上の画像ファイルに移動して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="2a51e-133">**メディア項目のアップロード** ダイアログ ボックスで、必要なタイトルと代替テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="2a51e-134">オプションの説明とキーワードを入力し、必要に応じてカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="2a51e-135">画像をアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2a51e-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="2a51e-136">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="2a51e-137">画像のフォルダのアップロード</span><span class="sxs-lookup"><span data-stu-id="2a51e-137">Upload a folder of images</span></span>

<span data-ttu-id="2a51e-138">サイト ビルダー内の画像のフォルダを一括アップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2a51e-139">左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="2a51e-140">コマンド バーで、**アップロード \> フォルダのアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="2a51e-141">ファイル エクスプローラー ウィンドウで、アップロードするフォルダに移動して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="2a51e-142">**メディア項目のアップロード** ダイアログ ボックスで、オプションのキーワードを入力し、必要に応じてカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="2a51e-143">フォルダをアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2a51e-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="2a51e-144">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a51e-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a51e-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2a51e-145">Additional resources</span></span>

[<span data-ttu-id="2a51e-146">資産管理の概要をデジタル化</span><span class="sxs-lookup"><span data-stu-id="2a51e-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="2a51e-147">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="2a51e-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="2a51e-148">ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="2a51e-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="2a51e-149">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="2a51e-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="2a51e-150">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="2a51e-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="2a51e-151">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="2a51e-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
