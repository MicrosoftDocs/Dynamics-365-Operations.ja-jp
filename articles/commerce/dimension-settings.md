---
title: 製品分析コードの表示設定を適用する
description: このトピックでは、商品の分析コードの表示設定と、Microsoft Dynamics 365 Commerce で適用する方法について説明します。
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117233"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="7f15c-103">製品分析コードの表示設定を適用する</span><span class="sxs-lookup"><span data-stu-id="7f15c-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7f15c-104">このトピックでは、商品の分析コードの表示設定と、Microsoft Dynamics 365 Commerce で適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f15c-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7f15c-105">Dynamics 365 Commerce では、製品のバリエーションを区別するために、サイズ、スタイル、カラーの分析コードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f15c-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="7f15c-106">通常、分析コードでは、サイズが "小"、"中"、"大"、色が "黒"、"茶" などのテキスト値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f15c-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="7f15c-107">しかし、多くのバリエーションがある製品の場合、それぞれのバリエーションの画像を表示させる複数の選択が必要となるため、製品のバリエーションの参照が困難になります。</span><span class="sxs-lookup"><span data-stu-id="7f15c-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="7f15c-108">Commerce のバージョン 10.0.20 では、商品のバリエーションをより簡単に閲覧できるように、画像や 16 進数 (hex) コードを使って分析コードを見本として表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7f15c-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="7f15c-109">分析コードの定義は、Commerce のサイトビルダーの、**サイト設定 \> 拡張機能 \> 分析コードの設定** で行います。</span><span class="sxs-lookup"><span data-stu-id="7f15c-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="7f15c-110">以下の図は、サイト ビルダー内における分析コードの表示例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7f15c-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Commerce サイト ビルダーでのサイト設定例](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="7f15c-112">次の 2 つの分析コード設定を使用できます:</span><span class="sxs-lookup"><span data-stu-id="7f15c-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="7f15c-113">**画像として表示する分析コード** - 商品詳細ページ (PDP) や検索結果一覧ページなど、eコマース サイトのページで見本として表示する寸法を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f15c-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="7f15c-114">色、サイズ、スタイルの分析コードはどのような組み合わせでも見本として表示できます。</span><span class="sxs-lookup"><span data-stu-id="7f15c-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="7f15c-115">見本としての表示に分析コードが選択されている場合、Commerce モジュールのレンダリングは、利用可能な 16 進コードの見本の構成を探して選択します。</span><span class="sxs-lookup"><span data-stu-id="7f15c-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="7f15c-116">16 進コードが構成されていない場合、システム ロジックは画像の URL 見本の構成を探します。</span><span class="sxs-lookup"><span data-stu-id="7f15c-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="7f15c-117">16 進コードも画像 URL も設定されていない場合は、テキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f15c-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="7f15c-118">次の図は、eコマースの PDP に色見本やサイズ見本が含まれている例です。</span><span class="sxs-lookup"><span data-stu-id="7f15c-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="7f15c-119">この例では、カラー分析コードに調整コードが構成されています。</span><span class="sxs-lookup"><span data-stu-id="7f15c-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="7f15c-120">そのため、見本は色として表示されています。</span><span class="sxs-lookup"><span data-stu-id="7f15c-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="7f15c-121">しかし、サイズの分析コードには 16 進数も画像 URL も構成されていません。</span><span class="sxs-lookup"><span data-stu-id="7f15c-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="7f15c-122">そのため、テキストは表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f15c-122">Therefore, text is shown.</span></span>

    ![eコマースの商品詳細ページに色見本として表示されるカラー分析コードの例](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="7f15c-124">**製品カードに表示する分析コード** - リストやリストページに表示される商品カードに表示する分析コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f15c-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="7f15c-125">分析コードを製品カードに表示する前に、その分析コードに対してこの設定を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f15c-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="7f15c-126">**画像として表示する分析コード** も有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f15c-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="7f15c-127">商品カードの見本選択の動作は、カラー分析コードに合わせて最適化されています。</span><span class="sxs-lookup"><span data-stu-id="7f15c-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="7f15c-128">他の分析コードの場合、見本の選択動作をカスタマイズするために、ビューの拡張機能が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7f15c-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="7f15c-129">次の図は、電子コマース サイトのリスト ページに色見本を含む商品カードがある場合の例です。</span><span class="sxs-lookup"><span data-stu-id="7f15c-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![eコマースの一覧ページに色見本として表示されるカラー分析コードの例](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="7f15c-131">サイトのページに見本として表示されるように製品の分析コードを設定する方法については、[製品の分析コード値を見本として表示する設定](./dev-itpro/dimensions-swatch.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="7f15c-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f15c-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7f15c-132">Additional resources</span></span>

[<span data-ttu-id="7f15c-133">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="7f15c-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7f15c-134">検索結果モジュール</span><span class="sxs-lookup"><span data-stu-id="7f15c-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="7f15c-135">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="7f15c-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7f15c-136">製品の分析コード値を見本として表示する設定</span><span class="sxs-lookup"><span data-stu-id="7f15c-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
