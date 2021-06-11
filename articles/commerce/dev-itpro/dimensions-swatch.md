---
title: 製品の分析コード値を見本として表示する設定
description: このトピックでは、Microsoft Dynamics 365 Commerce 本ブで製品分析コード値を見本として構成する方法 について説明します。
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 08564ce7af7412f2501b917b3496942004402611
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117232"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a><span data-ttu-id="d714e-103">製品の分析コード値を見本として表示する設定</span><span class="sxs-lookup"><span data-stu-id="d714e-103">Configure product dimension values to appear as swatches</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d714e-104">このトピックでは、Microsoft Dynamics 365 Commerce 本ブで製品分析コード値を見本として構成する方法 について説明します。</span><span class="sxs-lookup"><span data-stu-id="d714e-104">This topic describes how to configure product dimension values as swatches in Microsoft Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="d714e-105">製品の分析コードに関する詳細については、[製品の分析コード](../../supply-chain/pim/product-dimensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d714e-105">For information about product dimensions, see [Product dimensions](../../supply-chain/pim/product-dimensions.md).</span></span>

<span data-ttu-id="d714e-106">Dynamics 365 Commerce では、製品のバリエーションを表現するために、サイズ、スタイル、カラーの分析コードに対応しています。</span><span class="sxs-lookup"><span data-stu-id="d714e-106">Dynamics 365 Commerce supports the use of size, style, and color dimensions to represent product variants.</span></span> <span data-ttu-id="d714e-107">製品の分析コードにはフレンドリ名が付けられており、製品の詳細ページ (PDP) に表示され、製品のバリエーションを選択できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="d714e-107">Product dimensions have friendly names that are shown on product details pages (PDPs) so that product variants can be selected.</span></span> <span data-ttu-id="d714e-108">たとえば、サイズであれば「小」、「中」、「大」、色であれば「黒」、「茶」などです。</span><span class="sxs-lookup"><span data-stu-id="d714e-108">Examples of these friendly names include "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="d714e-109">しかし、製品のバリエーションが多い場合は、各製品のバリエーションごとに画像を表示するには複数の選択が必要になります。</span><span class="sxs-lookup"><span data-stu-id="d714e-109">However, if a product supports many variations, multiple selections are required to view the image for each product variant.</span></span> <span data-ttu-id="d714e-110">そのため、顧客が製品のバリエーションを参照して選択するのに時間がかかり、面倒な作業となってしまいます。</span><span class="sxs-lookup"><span data-stu-id="d714e-110">Therefore, it can be slow and tedious for customers to browse and select product variants.</span></span>

<span data-ttu-id="d714e-111">PDP に寸法が見本として表示されていれば、顧客は製品のバリエーションを視覚的に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d714e-111">When dimensions are shown as swatches on PDPs, customers get a visual preview of a product's variations.</span></span> <span data-ttu-id="d714e-112">顧客は、色、パターン、テクスチャーの豊富なバリエーションを簡単に閲覧でき、製品のさまざまな組み合わせを素早く確認できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-112">They can easily browse a large variety of colors, patterns, and textures, and can quickly view different combinations of product variations.</span></span>

<span data-ttu-id="d714e-113">分析コードを見本として表示する機能では、Commerce が16進数 (Hex) コードや画像を使って分析コードを見本として表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d714e-113">The display dimensions as swatches feature enables Commerce to use hexadecimal (hex) codes and images to show dimensions as swatches.</span></span> <span data-ttu-id="d714e-114">また、色などの類似うする分析コードを製品の一覧ページでグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-114">In addition, similar dimensions, such as colors, can be grouped on product list pages.</span></span> <span data-ttu-id="d714e-115">たとえば、顧客が青色の製品を検索しているとします。</span><span class="sxs-lookup"><span data-stu-id="d714e-115">For example, a customer is searching for products that are blue.</span></span> <span data-ttu-id="d714e-116">様々な青色の分析コード値がグループ化されている場合、検索結果のリストページには、異なる青の色調のを持つ製品が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-116">If the various blue dimension values are grouped together, the search results list page shows products that have the different shades of blue.</span></span> <span data-ttu-id="d714e-117">分析コードのグルーピングにより、製品の照会エクスペリエンスが大幅に向上し、顧客が1つの商品検索クエリでより多くの商品を見つけられるようになります。</span><span class="sxs-lookup"><span data-stu-id="d714e-117">Dimension grouping significantly improves the product refinement experience and helps customers find more products through a single product search query.</span></span>

> [!NOTE]
> <span data-ttu-id="d714e-118">Dynamics 365 Commerce のバージョン 10.0.20 のリリースから、見本としての分析コードを表示する機能が利用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d714e-118">The display dimensions as swatches feature is available as of the Dynamics 365 Commerce version 10.0.20 release.</span></span>

<span data-ttu-id="d714e-119">次の図は、Commerce PDP上で色が見本として表示される例です。</span><span class="sxs-lookup"><span data-stu-id="d714e-119">The following illustration shows an example where colors appear as swatches on a Commerce PDP.</span></span>

![商品詳細ページの色見本の例](../dev-itpro/media/swatch_pdp.png)

<span data-ttu-id="d714e-121">次の図は、Commerce の検索結果一覧ページで色が見本として表示される例です。</span><span class="sxs-lookup"><span data-stu-id="d714e-121">The following illustration shows an example where colors appear as swatches on a Commerce search results list page.</span></span>

![検索結果一覧ページの色見本の例](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a><span data-ttu-id="d714e-123">Commerce の見本として分析コード表示機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="d714e-123">Enable the display dimensions as swatches feature in Commerce headquarters</span></span>

<span data-ttu-id="d714e-124">コマース本部で分析コードを見本として表示する機能を有効化するには、**ワークスペース \> 機能管理** に移動し、**製品分析コード値の画像サポートを有効化する** 機能を有効化してください。</span><span class="sxs-lookup"><span data-stu-id="d714e-124">To enable the display dimensions as swatches feature in Commerce headquarters, go to **Workspaces \> Feature management**, and turn on the **Enable image support for product dimension values** feature.</span></span> <span data-ttu-id="d714e-125">この機能フラグを有効にすると、Commerce 本部の適切なテーブルに、各分析コードごとに次の3つの新しいフィールドが追加されます: **Hexcode**、**URL** (画像用)、**RefinerGroup**。</span><span class="sxs-lookup"><span data-stu-id="d714e-125">When this feature flag is enabled, three new fields are added for each dimension in the appropriate tables in Commerce headquarters: **Hexcode**, **URL** (for images), and **RefinerGroup**.</span></span>

## <a name="configure-dimension-values-in-commerce-headquarters"></a><span data-ttu-id="d714e-126">Commerce 本部での分析コード値の設定</span><span class="sxs-lookup"><span data-stu-id="d714e-126">Configure dimension values in Commerce headquarters</span></span>

<span data-ttu-id="d714e-127">見本としての分析コード表示機能は、サイズ、スタイル、カラーの分析コードに対応しています。</span><span class="sxs-lookup"><span data-stu-id="d714e-127">The display dimensions as swatches feature is supported for size, style, and color dimensions.</span></span> <span data-ttu-id="d714e-128">Commerce 本部では、適切な分析コードに対応する画像コードと画像 URL の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-128">Hex code and image URL values for the appropriate dimensions can be specified in Commerce headquarters.</span></span> <span data-ttu-id="d714e-129">既定では、分析コードに16進コードと画像URLの値が提供されていない場合、分析コードのフレンドリ名のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-129">By default, if hex code and image URL values aren't provided for a dimension, the system will show the text of the dimension's friendly name.</span></span>

<span data-ttu-id="d714e-130">構成は、次のレベルで実行できます:</span><span class="sxs-lookup"><span data-stu-id="d714e-130">The configuration can be done at any of the following levels:</span></span>

- <span data-ttu-id="d714e-131">**分析コード** -  Commerce 本部で、**色**、**サイズ**、 **スタイル** を検索して、分析コードのページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d714e-131">**Dimension** – In Commerce headquarters, open the page for a dimension by searching for **Color**, **Size**, or **Style**.</span></span> <span data-ttu-id="d714e-132">各ページでは、グリッドに分析コード値が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-132">On each page, a grid lists the dimension values.</span></span> <span data-ttu-id="d714e-133">表示順序、画面表示コード、画像 URL の値を管理できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-133">You can manage the display order, hex code, and image URL values.</span></span> <span data-ttu-id="d714e-134">次の図は、**色** ページの構成例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="d714e-134">The following illustration shows an example configuration on the **Colors** page.</span></span>

    ![[色] ページでの分析コード構成の例](../dev-itpro/media/swatch_Color.PNG)

- <span data-ttu-id="d714e-136">**分析コード グループ** - Dynamics 365 Commerce では、**RefinerGroup** プロパティを使用して分析コード グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-136">**Dimension group** – In Dynamics 365 Commerce, you can use the **RefinerGroup** property to create dimension groups.</span></span> <span data-ttu-id="d714e-137">分析コード グループが定義されている場合は、**色グループ**、**サイズ グループ**、**スタイル グループ** を検索して適切なページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d714e-137">If dimension groups are defined, open the appropriate page by searching for **Color group**, **Size group**, or **Style group**.</span></span> <span data-ttu-id="d714e-138">各ページでは、複数の画像コード、画像URL、絞り込みグループの値を管理できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-138">On each page, you can manage hex code, image URL, and refiner group values.</span></span> <span data-ttu-id="d714e-139">次の図は、**色グループ** ページの構成例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="d714e-139">The following illustration shows an example configuration on the **Color groups** page.</span></span>

    ![[色グループ] ページでの分析コード構成の例](../dev-itpro/media/swatch_colorGroup.PNG)

- <span data-ttu-id="d714e-141">**製品分析コード (製品の作成中)** - 新しい製品を作成する際に、**製品の分析コード** ページを使って分析コード値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="d714e-141">**Product dimension (during product creation)** – When you create a new product, you can use the **Product dimensions** page to enter the dimension values.</span></span> <span data-ttu-id="d714e-142">既存の製品の場合、**Hexcode**、**URL** (画像で使用)、**RefinerGroup** の各フィールドがすでに設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-142">For existing products, the **Hexcode**, **URL** (for images), and **RefinerGroup** fields might already be set.</span></span> <span data-ttu-id="d714e-143">必要に応じて値を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="d714e-143">However, you can change the values as you require.</span></span> <span data-ttu-id="d714e-144">次の図は、**製品分析コード** ページの構成例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="d714e-144">The following illustration shows an example configuration on the **Product dimensions** page.</span></span>

    ![[製品分析コード] ページでの分析コード構成の例](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> <span data-ttu-id="d714e-146">16進コードと画像 URL の設定を管理するプロセスは、分析コードの表示順を管理するのと同じパターンで行われます。</span><span class="sxs-lookup"><span data-stu-id="d714e-146">The process of managing hex code and image URL configurations follows the same pattern that is used to manage the display order of dimensions.</span></span>

## <a name="configure-dimension-values-by-using-hex-codes"></a><span data-ttu-id="d714e-147">16 進数コードを使用した分析コード値の構成</span><span class="sxs-lookup"><span data-stu-id="d714e-147">Configure dimension values by using hex codes</span></span>

<span data-ttu-id="d714e-148">ほとんどの色の分析コードについては、Commerce 本部の分析コードページに16進法のカラー値を記載する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-148">For most color dimensions, a hex code color value should be provided on dimension pages in Commerce headquarters.</span></span> <span data-ttu-id="d714e-149">たとえば、黒色は、16進数で **#00000** という値になります。</span><span class="sxs-lookup"><span data-stu-id="d714e-149">For example, the color black should have a hex code value of **#00000**.</span></span> <span data-ttu-id="d714e-150">Commerce がサイトのページをレンダリングする際に、16進数のコードが色付きの見本で表現されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-150">When Commerce renders a site page, the hex code is represented by a colored swatch.</span></span>

<span data-ttu-id="d714e-151">次の図は、色の分析コードを16進数の値で設定する例です。</span><span class="sxs-lookup"><span data-stu-id="d714e-151">The following illustration shows an example where color dimensions are configured by using hex code values.</span></span>

![16進コードを使用した分析コードの構成例](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a><span data-ttu-id="d714e-153">画像の URL を使用した分析コード値の構成</span><span class="sxs-lookup"><span data-stu-id="d714e-153">Configure dimension values by using image URLs</span></span>

<span data-ttu-id="d714e-154">一部の色分析コードは、色ではなくパターンを表します。</span><span class="sxs-lookup"><span data-stu-id="d714e-154">Some color dimensions represent patterns, not solid colors.</span></span> <span data-ttu-id="d714e-155">たとえば、カラー分析コードを「レオパード」と表現するとします。</span><span class="sxs-lookup"><span data-stu-id="d714e-155">For example, a color dimension might be described as 'leopard.'</span></span> <span data-ttu-id="d714e-156">このような場合、見本の16進コードではなく、公開されている画像を使用することで、より効果的に色の分析コードを表現することができます。</span><span class="sxs-lookup"><span data-stu-id="d714e-156">In these cases, you can more effectively represent the color dimensions by using published images instead of hex codes for swatches.</span></span>

<span data-ttu-id="d714e-157">それぞれの画像を Commerce サイト ビルダーにアップロードして公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-157">You must upload each image to Commerce site builder and publish it.</span></span> <span data-ttu-id="d714e-158">その後、Commerce本部の適切な分析コードページに掲載画像の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="d714e-158">Then enter the image URL for the published image on the appropriate dimension pages in Commerce headquarters.</span></span> <span data-ttu-id="d714e-159">見本として表示する分析コードが選択されていても、16進コードが定義されていない場合、Commerce はページをレンダリングする際に画像検索を行います。</span><span class="sxs-lookup"><span data-stu-id="d714e-159">If a dimension has been selected for display as a swatch, but a hex code isn't defined, Commerce will do an image lookup when it renders the page.</span></span> <span data-ttu-id="d714e-160">画像の検索が失敗すると、Commerce には分析コードのユーザー名のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-160">If the image lookup fails, Commerce will show the text of the dimension's friendly name.</span></span>

<span data-ttu-id="d714e-161">次の図は、**色** ページの構成に画像 URL を使用した例です。</span><span class="sxs-lookup"><span data-stu-id="d714e-161">The following illustration shows an example where image URLs are used for the configuration on the **Colors** page.</span></span>

![画像 URL を使用した分析コードの構成例](../dev-itpro/media/swatch_color_urls.PNG)

<span data-ttu-id="d714e-163">メディア テンプレートを使用すると、製品イメージやカテゴリ イメージと同様に、画像のURLを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-163">You can use a media template to define image URLs, just as you can for product and category images.</span></span> <span data-ttu-id="d714e-164">サイト ビルダーに画像をアップロードする場合は、ファイル名の規則とファイル パスが一貫している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-164">When you upload images to site builder, file name conventions and file paths must be consistent.</span></span>

<span data-ttu-id="d714e-165">次の図は、メディア テンプレートの構成に画像 URL を使用した例です。</span><span class="sxs-lookup"><span data-stu-id="d714e-165">The following illustration shows an example where image URLs are used for the configuration of a media template.</span></span>

![メディア テンプレートの構成例](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a><span data-ttu-id="d714e-167">16 進コードと画像の URL を使用した分析コード値の構成</span><span class="sxs-lookup"><span data-stu-id="d714e-167">Configure dimension values by using both hex codes and image URLs</span></span>

<span data-ttu-id="d714e-168">ほとんどの色分析コードに対して、16 進コードと画像 URL の両方を構成できます。</span><span class="sxs-lookup"><span data-stu-id="d714e-168">For most color dimensions, you can configure both hex codes and image URLs.</span></span> <span data-ttu-id="d714e-169">Commerce レンダリングの代替ロジックは、色見本を表示するために、16 進コードまたは画像 URL のいずれかを自動的に検索します。</span><span class="sxs-lookup"><span data-stu-id="d714e-169">Commerce rendering fallback logic will automatically look for either a hex code or an image URL to show a color swatch.</span></span> <span data-ttu-id="d714e-170">色の分析コードの構成に、16進コードと画像の URL を併用することで、色数が多い場合のイメージ管理が容易になります。</span><span class="sxs-lookup"><span data-stu-id="d714e-170">By using both hex codes and image URLs to configure color dimensions, you help simplify image management when the number of colors is large.</span></span>

<span data-ttu-id="d714e-171">次の図は、**色** ページの構成に 16 進コードと画像 URL を使用した例です。</span><span class="sxs-lookup"><span data-stu-id="d714e-171">The following illustration shows an example where both hex codes and image URLs are used for the configuration on the **Colors** page.</span></span>

![16 進コードと画像 URL を使用した分析コードの構成例](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a><span data-ttu-id="d714e-173">絞り込み条件グループの構成</span><span class="sxs-lookup"><span data-stu-id="d714e-173">Configure refiner groups</span></span>

<span data-ttu-id="d714e-174">分析コード値に対して16 進コードまたは画像 URL を定義する際は、 **RefinerGroup** フィールドに値を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d714e-174">When you define a hex code or image URL for a dimension value, you can also specify a value for the **RefinerGroup** field.</span></span> <span data-ttu-id="d714e-175">このフィールドは、絞り込みエクスペリエンスにおいて類似する分析コード値をグループ化するために使用する分析コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="d714e-175">This field defines the dimension that should be used to group similar dimension values in the refiner experience.</span></span>

<span data-ttu-id="d714e-176">たとえば、色分析コードの値が 「青」、「青のチェック柄」、「ブルーウォッシュ」、「濃い青」の場合、各値は別の調整コードまたは画像 URL にマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="d714e-176">For example, if your color dimension values are "blue," "blue plaid," "blue wash," and "dark blue," each value is mapped to a different hex code or image URL.</span></span> <span data-ttu-id="d714e-177">したがって、各値は該当する製品の PDP と製品カードで異なる色として表示されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-177">Therefore, each value will appear as a different color on PDPs and product cards for the appropriate products.</span></span> <span data-ttu-id="d714e-178">しかし、これらすべての色分析コード値を **RefinerGroup** 値の **青色** にマッピングすると、「青色」の製品を検索すると、分析コードのカラー値が「青」、「青のチェック柄」、「ブルーウォッシュ」、「濃い青」の製品のリストページ検索結果が生成されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-178">However, if you map all those color dimension values to a **RefinerGroup** value of **Blue**, a search for "blue" products will generate list page search results for products that have dimension color values of "blue," "blue plaid," "blue wash," and "dark blue".</span></span>

<span data-ttu-id="d714e-179">次の図の例は、Commerce 本部の **色** と **RefinerGroup** のプロパティ間の関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="d714e-179">The example in the following illustration shows the relationship between the **Color** and **RefinerGroup** properties in Commerce headquarters.</span></span>

![絞り込み条件グループ管理の例](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a><span data-ttu-id="d714e-181">Commerce サイト ビルダーで画像を管理する</span><span class="sxs-lookup"><span data-stu-id="d714e-181">Manage images in Commerce site builder</span></span>

<span data-ttu-id="d714e-182">分析コード値に画像 URL が使用されている場合、対応する画像を Commerce のサイトビルダーにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-182">If image URLs are used for any dimension values, the corresponding images must be uploaded to Commerce site builder.</span></span> <span data-ttu-id="d714e-183">各画像の場所は、Commerce 本部の画像に対して定義されているファイル名とフォルダ パスと一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-183">The location of each image should match the file name and folder path that are defined for the image in Commerce headquarters.</span></span> <span data-ttu-id="d714e-184">イメージ ファイルは、サイト ビルダの適切なカテゴリの場所にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-184">Image files must be uploaded to the appropriate category locations in site builder.</span></span> <span data-ttu-id="d714e-185">たとえば、カラー イメージは **色** カテゴリのフォルダにアップロード する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-185">For example, color images must be uploaded to the **Color** category folder.</span></span> <span data-ttu-id="d714e-186">サイト ビルダーに画像をアップロードする方法の詳細については、[画像のアップロード](../dam-upload-images.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d714e-186">For more information about how to upload images to site builder, see [Upload images](../dam-upload-images.md).</span></span>

<span data-ttu-id="d714e-187">次の図に、**ファイルのアップロード** ダイアログ ボックスを使用して画像をサイト ビルダ メディア ライブラリにアップロードする例を示します。</span><span class="sxs-lookup"><span data-stu-id="d714e-187">The following illustration shows an example where the **Upload files** dialog box is being used to upload images to the site builder media library.</span></span> <span data-ttu-id="d714e-188">選択可能な **サイズ**、**色**、**スタイル** のカテゴリが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="d714e-188">It highlights the **Size**, **Color**, and **Style** categories that are available for selection.</span></span>

![サイトビルダのメディア ライブラリにアップロードする際の画像ファイルのカテゴリーの例](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a><span data-ttu-id="d714e-190">eコマース サイトのページで見本の表示を可能にする</span><span class="sxs-lookup"><span data-stu-id="d714e-190">Enable swatch display on e-commerce site pages</span></span>

<span data-ttu-id="d714e-191">PDP やリストページなど、分析コードの選択が必要な eコマース サイトのページに見本を表示するには、Commerce 本部で分析コードサイトの構成をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-191">Before swatches can appear on e-commerce site pages that require dimension selection, such as PDPs and list pages, you must configure dimension site settings in Commerce headquarters.</span></span> <span data-ttu-id="d714e-192">詳細については、[分析コードのサイト設定の適用](../dimension-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d714e-192">For more information, see [Apply site settings for dimensions](../dimension-settings.md).</span></span>

<span data-ttu-id="d714e-193">さらに、検索結果モジュールの **検索結果に製品属性を含める** プロパティを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-193">In addition, you should enable the **Include product attributes in search results** property for search results modules.</span></span> <span data-ttu-id="d714e-194">サイトでカスタマイズされたカテゴリ ページを使用している場合は、そのページで使用されている検索結果モジュールを更新して、**検索結果に製品属性を含める** プロパティが有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d714e-194">If your site uses customized category pages, you should update the search results modules that are used on those pages, so that the **Include product attributes in search results** property is enabled.</span></span> <span data-ttu-id="d714e-195">詳細については、[検索結果モジュール](../search-result-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d714e-195">For more information, see [Search results module](../search-result-module.md).</span></span>

## <a name="display-swatches-in-pos-and-other-channels"></a><span data-ttu-id="d714e-196">POS および他のチャンネルの表示</span><span class="sxs-lookup"><span data-stu-id="d714e-196">Display swatches in POS and other channels</span></span>

<span data-ttu-id="d714e-197">Commerce では現在、販売時点管理 (POS) やその他のチャネルでの見本の表示に対応できるような、既成の実装機能はありません。</span><span class="sxs-lookup"><span data-stu-id="d714e-197">Commerce doesn't currently have an out-of-box implementation that supports the display of swatches in Point of Sale (POS) and other channels.</span></span> <span data-ttu-id="d714e-198">しかし、見本の表示機能を拡張して、チャンネル API での見本の表示に必要な 16 進コードや画像 URL を返すように実装することはできます。</span><span class="sxs-lookup"><span data-stu-id="d714e-198">However, you can implement swatch display functionality as an extension that makes channel APIs return the hex codes and image URLs that are required to render swatches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d714e-199">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d714e-199">Additional resources</span></span>

[<span data-ttu-id="d714e-200">検索結果モジュール</span><span class="sxs-lookup"><span data-stu-id="d714e-200">Search results module</span></span>](../search-result-module.md)

[<span data-ttu-id="d714e-201">分析コードにサイトの設定を適用する</span><span class="sxs-lookup"><span data-stu-id="d714e-201">Apply site settings for dimensions</span></span>](../dimension-settings.md)

[<span data-ttu-id="d714e-202">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="d714e-202">Product dimensions</span></span>](../../supply-chain/pim/product-dimensions.md)

[<span data-ttu-id="d714e-203">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="d714e-203">Upload image</span></span>](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
