---
title: メディア ギャラリー モジュール
description: このトピックでは、メディア ギャラリー モジュールを取り上げ、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 647387bafe8866cb1bee8c57675629af796f33e6
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817185"
---
# <a name="media-gallery-module"></a><span data-ttu-id="6d80a-103">メディア ギャラリー モジュール</span><span class="sxs-lookup"><span data-stu-id="6d80a-103">Media gallery module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6d80a-104">このトピックでは、メディア ギャラリー モジュールを取り上げ、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-104">This topic covers media gallery modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6d80a-105">概要</span><span class="sxs-lookup"><span data-stu-id="6d80a-105">Overview</span></span>

<span data-ttu-id="6d80a-106">メディア ギャラリー モジュールは、ギャラリー ビューに 1 つ以上の画像を表示します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-106">Media gallery modules show one or more images in a gallery view.</span></span> <span data-ttu-id="6d80a-107">メディア ギャラリー モジュールは、水平方向 (画像の下の行として) または垂直方向 (画像の横の列として) のいずれかに配置できるサムネイル画像をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6d80a-107">Media gallery modules support thumbnail images, which can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="6d80a-108">また、メディア ギャラリー モジュールには、画像をズーム (拡大) したり、全画面モードで表示したりする機能も用意されています。</span><span class="sxs-lookup"><span data-stu-id="6d80a-108">Media gallery modules also provide capabilities that enable images to be zoomed (magnified) or viewed in full-screen mode.</span></span> <span data-ttu-id="6d80a-109">メディア ギャラリー モジュールでレンダリングするには、Commerce サイト ビルダーのメディア ライブラリでイメージが使用可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6d80a-109">To be rendered in a media gallery module, an image must be available in the Commerce site builder Media Library.</span></span> <span data-ttu-id="6d80a-110">現時点では、メディア ギャラリー モジュールでサポートしているのは画像のみです。</span><span class="sxs-lookup"><span data-stu-id="6d80a-110">Currently, media gallery modules support only images.</span></span>

<span data-ttu-id="6d80a-111">既定のモードで、メディア ギャラリー モジュールは、製品の詳細ページ (PDP) のページ コンテキストから使用できる製品 ID を使用して、対応する製品画像をレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="6d80a-111">In the default mode, a media gallery module uses the product ID that is available from the page context of a product details page (PDP) to render the corresponding product images.</span></span> <span data-ttu-id="6d80a-112">Commerce Headquarters で、すべての製品に対してメディア ファイル パスを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-112">In Commerce headquarters, a media file path must be defined for all products.</span></span> <span data-ttu-id="6d80a-113">その後、Commerce Headquarters で製品に対して定義されたファイル パスに従って、サイト ビルダー メディア ライブラリに画像をアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-113">Images should then be uploaded to the site builder Media Library according to the file path that was defined for the products in Commerce headquarters.</span></span> <span data-ttu-id="6d80a-114">これらの画像には、製品および製品バリアントの画像が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-114">These images include images for products and any product variants.</span></span> <span data-ttu-id="6d80a-115">サイト ビルダーのメディア ライブラリーに画像をアップロードする方法の詳細については、[画像のアップロード](dam-upload-images.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d80a-115">For more information about how to upload images to site builder Media Library, see [Upload images](dam-upload-images.md).</span></span>

<span data-ttu-id="6d80a-116">または、製品 ID またはページ コンテキストに依存しない画像ギャラリー ページで、完全に精選された一連の画像をホストすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-116">Alternatively, a media gallery module can host a fully curated set of images on an image gallery page, where there are no dependencies on the product ID or page context.</span></span> <span data-ttu-id="6d80a-117">この場合、画像をサイト ビルダーのメディア ライブラリーにアップロードし、サイト ビルダーで指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-117">In this case, images must be uploaded to site builder Media Library and specified in site builder.</span></span>

<span data-ttu-id="6d80a-118">メディア ギャラリー モジュールの使用例を次に示します:</span><span class="sxs-lookup"><span data-stu-id="6d80a-118">Here are some usage examples for media gallery modules:</span></span>

- <span data-ttu-id="6d80a-119">PDP での製品画像のレンダリング</span><span class="sxs-lookup"><span data-stu-id="6d80a-119">Rendering product images on a PDP</span></span>
- <span data-ttu-id="6d80a-120">製品マーケティング ページでの製品画像のレンダリング</span><span class="sxs-lookup"><span data-stu-id="6d80a-120">Rendering product images on a product marketing page</span></span>
- <span data-ttu-id="6d80a-121">精選された一連の画像をギャラリー ページなどのマーケティング ページに表示</span><span class="sxs-lookup"><span data-stu-id="6d80a-121">Showcasing a curated set of images on a marketing page, such as a gallery page</span></span>

<span data-ttu-id="6d80a-122">次の図に示す例では、PDP 上の購入ボックスが、メディア ギャラリー モジュールを使用して製品画像をホストします。</span><span class="sxs-lookup"><span data-stu-id="6d80a-122">In the example in the following illustration, a buy box on a PDP hosts product images by using a media gallery module.</span></span>

![メディア ギャラリー モジュールを使用して製品画像をホストする製品詳細ページの購入ボックスの例](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a><span data-ttu-id="6d80a-124">メディア ギャラリーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="6d80a-124">Media gallery properties</span></span>

| <span data-ttu-id="6d80a-125">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="6d80a-125">Property name</span></span> | <span data-ttu-id="6d80a-126">値</span><span class="sxs-lookup"><span data-stu-id="6d80a-126">Values</span></span> | <span data-ttu-id="6d80a-127">説明</span><span class="sxs-lookup"><span data-stu-id="6d80a-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="6d80a-128">画像ソース</span><span class="sxs-lookup"><span data-stu-id="6d80a-128">Image source</span></span> | <span data-ttu-id="6d80a-129">**ページ コンテキスト** または **製品 ID**</span><span class="sxs-lookup"><span data-stu-id="6d80a-129">**Page context** or **Product ID**</span></span> | <span data-ttu-id="6d80a-130">既定値は **ページ コンテキスト** です。</span><span class="sxs-lookup"><span data-stu-id="6d80a-130">The default value is **Page context**.</span></span> <span data-ttu-id="6d80a-131">**ページ コンテキスト** が選択されている場合、モジュールは、ページが製品 ID 情報を提供することを想定します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-131">If **Page context** is selected, the module expects the page to provide the product ID information.</span></span> <span data-ttu-id="6d80a-132">**製品 ID** を選択した場合は、画像の製品 IDを **製品 ID** プロパティの値として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-132">If **Product ID** is selected, the product ID for an image must be provided as the value of the **Product ID** property.</span></span> <span data-ttu-id="6d80a-133">この機能は、Commerce バージョン 10.0.12 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-133">This capability is available in Commerce version 10.0.12.</span></span> |
| <span data-ttu-id="6d80a-134">製品 ID</span><span class="sxs-lookup"><span data-stu-id="6d80a-134">Product ID</span></span> | <span data-ttu-id="6d80a-135">製品 ID</span><span class="sxs-lookup"><span data-stu-id="6d80a-135">A product ID</span></span> | <span data-ttu-id="6d80a-136">このプロパティは、**画像ソース** プロパティの値が **製品 ID** である場合にのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-136">This property is applicable only if the value of the **Image source** property is **Product ID**.</span></span> |
| <span data-ttu-id="6d80a-137">画像ズーム</span><span class="sxs-lookup"><span data-stu-id="6d80a-137">Image zoom</span></span> | <span data-ttu-id="6d80a-138">**インライン** または **コンテナー**</span><span class="sxs-lookup"><span data-stu-id="6d80a-138">**Inline** or **Container**</span></span> | <span data-ttu-id="6d80a-139">このプロパティを使用すると、ユーザーはメディア ギャラリー モジュールの画像をズームできます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-139">This property lets the user zoom images in the media gallery module.</span></span> <span data-ttu-id="6d80a-140">画像は、インラインまたは画像の横にある別のコンテナーでズームできます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-140">An image can be zoomed either inline or in a separate container next to the image.</span></span> <span data-ttu-id="6d80a-141">この機能は、10.0.12 で使用できます</span><span class="sxs-lookup"><span data-stu-id="6d80a-141">This capability is available in 10.0.12</span></span> |
| <span data-ttu-id="6d80a-142">ズーム スケール</span><span class="sxs-lookup"><span data-stu-id="6d80a-142">Zoom scale</span></span> | <span data-ttu-id="6d80a-143">10 進数</span><span class="sxs-lookup"><span data-stu-id="6d80a-143">A decimal number</span></span> | <span data-ttu-id="6d80a-144">このプロパティは、画像のズーム倍率を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-144">This property specifies the scale factor for zooming images.</span></span> <span data-ttu-id="6d80a-145">たとえば、値が **2.5** に設定されている場合、画像は 2.5 倍に拡大されます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-145">For example, if the value is set to **2.5**, images are magnified 2.5 times.</span></span>|
| <span data-ttu-id="6d80a-146">全画面表示</span><span class="sxs-lookup"><span data-stu-id="6d80a-146">Full screen</span></span> | <span data-ttu-id="6d80a-147">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="6d80a-147">**True** or **False**</span></span> | <span data-ttu-id="6d80a-148">このプロパティは、画像を全画面表示モードで表示できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-148">This property specifies whether images can be viewed in full-screen mode.</span></span> <span data-ttu-id="6d80a-149">全画面表示モードでは、ズーム機能がオンになっている場合、画像をさらに拡大することもできます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-149">In full-screen mode, images can be also be further magnified if the zoom capability is turned on.</span></span> <span data-ttu-id="6d80a-150">この機能は、Commerce バージョン 10.0.13 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-150">This capability is available in Commerce version 10.0.13.</span></span> |
| <span data-ttu-id="6d80a-151">イメージ</span><span class="sxs-lookup"><span data-stu-id="6d80a-151">Images</span></span> | <span data-ttu-id="6d80a-152">サイト ビルダーのメディア ライブラリーから選択された画像</span><span class="sxs-lookup"><span data-stu-id="6d80a-152">Images that are selected from site builder Media Library</span></span> | <span data-ttu-id="6d80a-153">製品からレンダリングするだけでなく、メディア ギャラリー モジュール用に画像を精選することもできます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-153">In addition to being rendered from a product, images can be curated for a media gallery module.</span></span> <span data-ttu-id="6d80a-154">これらの画像は、使用可能な製品画像に追加されます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-154">These images will be appended to any product images that are available.</span></span> <span data-ttu-id="6d80a-155">この機能は、Commerce バージョン 10.0.12 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-155">This capability is available in Commerce version 10.0.12.</span></span> |
| <span data-ttu-id="6d80a-156">サムネイルの向き</span><span class="sxs-lookup"><span data-stu-id="6d80a-156">Thumbnail orientation</span></span> | <span data-ttu-id="6d80a-157">**垂直** または **水平**</span><span class="sxs-lookup"><span data-stu-id="6d80a-157">**Vertical** or **Horizontal**</span></span> | <span data-ttu-id="6d80a-158">このプロパティでは、サムネイル画像を垂直ストリップと水平ストリップのどちらで表示するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-158">This property specifies whether thumbnail images should be shown in a vertical strip or a horizontal strip.</span></span> |

<span data-ttu-id="6d80a-159">次の図は、全画面およびズーム オプションが使用できるメディア ギャラリー モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6d80a-159">The following illustration shows an example of a media gallery module where the full-screen and zoom options are available.</span></span>

![全画面およびズーム オプションが使用できるメディア ギャラリー モジュールの例](./media/ecommerce-media-zoom.png)

<span data-ttu-id="6d80a-161">次の図は、精選された画像がある (つまり、指定された画像が製品 ID またはページ コンテキストに依存しない) メディア ギャラリ モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6d80a-161">The following illustration shows an example of a media gallery module that has curated images (that is, the specified images aren't dependent on the product ID or page context).</span></span>

![精選された画像があるメディア ギャラリー モジュールの例](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="6d80a-163">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="6d80a-163">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="6d80a-164">画像ソースがページ コンテキストから派生している場合は、PDP からの製品 ID を使用して画像を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-164">When the image source is derived from the page context, the product ID from the PDP is used to retrieve the images.</span></span> <span data-ttu-id="6d80a-165">メディア ギャラリー モジュールでは、Commerce Scale Unit アプリケーションのプログラム インターフェース (API) を使用して製品の画像ファイル パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-165">The media gallery module retrieves the image file path for products by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="6d80a-166">その後、画像はメディア ライブラリから取得され、モジュールでレンダリングできるようになります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-166">The images are then pulled from the Media Library so that they can be rendered in the module.</span></span>

## <a name="add-a-media-gallery-module-to-a-page"></a><span data-ttu-id="6d80a-167">メディア ギャラリー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="6d80a-167">Add a media gallery module to a page</span></span>

<span data-ttu-id="6d80a-168">マーケティング ページにメディア ギャラリー モジュールを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d80a-168">To add a media gallery module to a marketing page, follow these steps.</span></span>

1. <span data-ttu-id="6d80a-169">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-169">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6d80a-170">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**マーケティング テンプレート** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-170">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6d80a-171">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-171">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6d80a-172">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-172">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6d80a-173">既定のページの **メイン** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-173">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6d80a-174">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-174">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6d80a-175">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-175">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6d80a-176">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-176">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="6d80a-177">**テンプレートの選択** ダイアログ ボックスで、**マーケティング テンプレート** のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-177">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="6d80a-178">**ページ名** で、**メディア ギャラリー ページ** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-178">Under **Page name**, enter **Media gallery page**, and then select **OK**.</span></span>
1. <span data-ttu-id="6d80a-179">新規ページの**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-179">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6d80a-180">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-180">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6d80a-181">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-181">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6d80a-182">**モジュールの追加** ダイアログ ボックスで、**メディア ギャラリー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-182">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6d80a-183">メディア ギャラリー モジュールのプロパティ ペインの **画像ソース** で、**Productid** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-183">In the property pane for the media gallery module, under **Image source**, select **Productid**.</span></span> <span data-ttu-id="6d80a-184">次に **製品 ID** フィールドに、製品 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-184">Then, in the **Product id** field, enter a product ID.</span></span>
1. <span data-ttu-id="6d80a-185">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="6d80a-185">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="6d80a-186">ギャラリー ビューで製品の画像を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-186">You should be able to see the images for the product in a gallery view.</span></span>
1. <span data-ttu-id="6d80a-187">精選された画像のみを使用するには、プロパティ ペインの **画像ソース** で **Productid** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-187">To use only curated images, in the property pane, under **Image source**, select **Productid**.</span></span> <span data-ttu-id="6d80a-188">次に、**画像** で、**画像の追加** を必要な回数だけ選択して、メディア ライブラリから画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-188">Then, under **Images**, select **Add an image** as many times as required to add images from the Media Library.</span></span>
1. <span data-ttu-id="6d80a-189">**画像のズーム**、**ズーム係数**、**サムネイルの向き** など、設定する追加のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-189">Set any additional properties that you want to set, such as **Image zoom**, **Zoom factor**, and **Thumbnails orientation**.</span></span>
1. <span data-ttu-id="6d80a-190">完了したら、**保存** を選択し、**編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-190">When you've finished, select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d80a-191">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6d80a-191">Additional resources</span></span>

[<span data-ttu-id="6d80a-192">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="6d80a-192">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6d80a-193">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="6d80a-193">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6d80a-194">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="6d80a-194">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6d80a-195">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="6d80a-195">Upload images</span></span>](dam-upload-images.md)
