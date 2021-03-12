---
title: 購入ボックス モジュール
description: このトピックでは、購入ボックス モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae3da8ee77636a2d2257e01f5876f5542469f7da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986057"
---
# <a name="buy-box-module"></a><span data-ttu-id="2f088-103">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f088-104">このトピックでは、購入ボックス モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f088-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2f088-105">概要</span><span class="sxs-lookup"><span data-stu-id="2f088-105">Overview</span></span>

<span data-ttu-id="2f088-106">*購入ボックス* という用語は、通常 "折りたたみの上" である製品の詳細ページの領域を指し、製品購買に必要な最も重要な情報すべてをホストします。</span><span class="sxs-lookup"><span data-stu-id="2f088-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="2f088-107">("折りたたみの上" である領域はページが最初に読み込まれたときに表示されるため、ユーザーは下にスクロールして表示する必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="2f088-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="2f088-108">購入ボックス モジュールは、製品の詳細ページの購入ボックス領域に表示されるすべてのモジュールをホストするために使用する特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="2f088-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="2f088-109">製品の詳細ページの URL には、製品 ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2f088-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="2f088-110">購買ボックス モジュールの表示に必要なすべての情報は、この製品 ID から派生します。</span><span class="sxs-lookup"><span data-stu-id="2f088-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="2f088-111">製品 ID が指定されていない場合、購入ボックス モジュールはページに正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="2f088-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="2f088-112">したがって、購入ボックス モジュールは、製品コンテキストがあるページでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f088-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="2f088-113">製品コンテキストがないページ (ホーム ページやマーケティング ページなど) で使用するには、追加のカスタマイズを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f088-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="2f088-114">以下の図は、[商品の詳細] ページにある [購入ボックス] モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f088-114">The following image shows an example of a buy box module on a product details page.</span></span>

![購入ボックス モジュールの例](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="2f088-116">購入ボックス モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="2f088-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="2f088-117">製品の詳細ページでは、購入ボックスは 2 つの領域に分割されます: 左側にメディア領域、右側にコンテンツ領域。</span><span class="sxs-lookup"><span data-stu-id="2f088-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="2f088-118">既定では、メディア領域列の幅とコンテンツ領域列の幅の比率は 2:1 になります。</span><span class="sxs-lookup"><span data-stu-id="2f088-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="2f088-119">モバイル デバイスでは 2 つの領域が積み重ねられ、一方の領域がもう一方の領域の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f088-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="2f088-120">テーマを使用して、列の幅やスタック ランクをカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f088-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="2f088-121">購入ボックス モジュールは、製品のタイトル、説明、価格、および評価をレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="2f088-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="2f088-122">また、顧客は、サイズ、スタイル、色などの製品属性が異なる製品バリアントを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f088-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="2f088-123">製品バリアントが選択されると、購入ボックスの他のプロパティ (製品の説明や画像など) が更新されて、バリアント情報が反映されます。</span><span class="sxs-lookup"><span data-stu-id="2f088-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="2f088-124">数量セレクターは、顧客が購入する品目の数量を指定できるようにするために用意されています。</span><span class="sxs-lookup"><span data-stu-id="2f088-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="2f088-125">購入できる最大数量は、サイト設定で定義できます。</span><span class="sxs-lookup"><span data-stu-id="2f088-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="2f088-126">購入 ボックスから、カートへの製品の追加、欲しい物リストへの製品の追加、集配場所の選択などのアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f088-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="2f088-127">これらのアクションは、製品または製品バリアントに対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="2f088-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="2f088-128">製品を欲しい物リストに追加するには、顧客がサインインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f088-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="2f088-129">テーマを使用すると、購入ボックスの製品プロパティとアクション コントロールの順序を削除または変更できます。</span><span class="sxs-lookup"><span data-stu-id="2f088-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="2f088-130">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="2f088-130">Module properties</span></span>

- <span data-ttu-id="2f088-131">**ヘッダー タグ** ー このプロパティは、製品タイトルのヘッダー タグを定義します。</span><span class="sxs-lookup"><span data-stu-id="2f088-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="2f088-132">購入ボックスがページの一番上にある場合は、アクセシビリティ標準を満たすため、このプロパティを **h1** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f088-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

- <span data-ttu-id="2f088-133">**類似した外観のものを買う** - このプロパティを使用すると、現在表示されている商品に似ている商品へのリンクを購入ボックスに表示できます。</span><span class="sxs-lookup"><span data-stu-id="2f088-133">**Enable "shop similar looks" recommendations** - This property allows the buy box to show links to products that look similar to the currently viewed item.</span></span> <span data-ttu-id="2f088-134">この機能は、コマースのリリース 10.0.13 およびこれ以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="2f088-134">This feature is available in Commerce release 10.0.13 and later.</span></span>

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="2f088-135">購入用ボックス モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-135">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="2f088-136">**メディア ギャラリー** – このモジュールは、製品の詳細ページに製品の画像を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f088-136">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="2f088-137">このモジュールの詳細については、[メディア ギャラリー モジュール](media-gallery-module.md) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="2f088-137">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="2f088-138">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="2f088-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="2f088-139">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="2f088-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="2f088-140">このモジュールの詳細については、[店舗セレクタ モジュール](store-selector.md) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="2f088-140">For more information about this module, see [Store selector module](store-selector.md).</span></span>
- <span data-ttu-id="2f088-141">**ソーシャル共有** - このモジュールを [購入] ボックスに追加すると、ユーザーがソーシャル メディアで製品情報を共有できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2f088-141">**Social share** - This module can be added to the buy box to allow users to share product information on social media.</span></span> <span data-ttu-id="2f088-142">詳細については、[ソーシャル シェア モジュール](social-share-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f088-142">For more information, see [Social share module](social-share-module.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="2f088-143">購入ボックス モジュール設定</span><span class="sxs-lookup"><span data-stu-id="2f088-143">Buy box module settings</span></span>

<span data-ttu-id="2f088-144">以下の購入ボックス モジュールは、**サイト設定 \> 拡張** で構成可能です :</span><span class="sxs-lookup"><span data-stu-id="2f088-144">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="2f088-145">**カートの明細行の数量上限** – このプロパティは、カートに追加できる各品目の最大数を指定する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f088-145">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="2f088-146">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="2f088-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="2f088-147">**在庫** - 在庫設定の適用方法については、[在庫設定を適用する](inventory-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f088-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="2f088-148">**製品をカートに追加する** - このプロパティは、品目がカートに追加された後の動作を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f088-148">**Add product to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="2f088-149">使用可能な値は、**カート ページに移動**、**カート ページに移動しない**、**通知を表示** です。</span><span class="sxs-lookup"><span data-stu-id="2f088-149">The possible values are **Navigate to cart page**, **Do not navigate to cart page**, and **Show notification**.</span></span> <span data-ttu-id="2f088-150">この値が **カート ページに移動** に設定されている場合は、ユーザーが品目を追加した後はカート ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="2f088-150">When the value is set to **Navigate to cart page**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="2f088-151">この値が **カート ページに移動しない** に設定されている場合は、ユーザーが品目を追加した後もカート ページに移動しません。</span><span class="sxs-lookup"><span data-stu-id="2f088-151">When the value is set to **Do not navigate to cart page**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="2f088-152">この値が **通知を表示** に設定されている場合、ユーザーに確認の通知が表示され、引き続き製品の詳細ページを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="2f088-152">When the value is set to **Show notification**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2f088-153">**製品をカートに追加** サイト設定は、Dynamics 365 Commerce 10.0.11 リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f088-153">The **Add product to cart** site settings are available in the Dynamics 365 Commerce 10.0.11 release.</span></span> <span data-ttu-id="2f088-154">古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f088-154">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="2f088-155">appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="2f088-155">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

<span data-ttu-id="2f088-156">次の画像では、Fabrikam サイトにおいて "カートに追加された" 際の確認通知の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f088-156">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

![通知モジュールの例](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="2f088-158">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="2f088-158">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="2f088-159">購入ボックス モジュールでは、Commerce Scale Unit アプリケーションのプログラム インターフェース (API) を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="2f088-159">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="2f088-160">製品の詳細ページの製品 ID は、すべての情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f088-160">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="2f088-161">購入ボックス モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="2f088-161">Add a buy box module to a page</span></span>

<span data-ttu-id="2f088-162">新しいページに購入ボックス モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2f088-162">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2f088-163">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f088-163">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="2f088-164">**新規フラグメント** ダイアログ ボックスで、**ボックスを購入** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-164">In the **New fragment** dialog box, select the **Buy box** module.</span></span>
1. <span data-ttu-id="2f088-165">**フラグメント名** で、名前に **購入ボックス フラグメント** と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-165">Under **Fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-166">購入用ボックス モジュールを含む **メディア ギャラリー** スロットにて、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-166">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f088-167">**モジュールの追加** ダイアログ ボックスで、**メディア ギャラリー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-167">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-168">購入用ボックス モジュールを含む **店舗セレクター** スロットにて、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-168">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f088-169">**モジュールの追加** ダイアログ ボックスで、**店舗セレクター** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-169">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-170">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="2f088-170">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2f088-171">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f088-171">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2f088-172">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**PDP のテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-172">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-173">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-173">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f088-174">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-174">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-175">既定のページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-175">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="2f088-176">**ページ フラグメントの選択** ダイアログ ボックスで、作成済の **購入ボックス フラグメント** フラグメントを選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-176">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-177">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="2f088-177">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2f088-178">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f088-178">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2f088-179">**テンプレートの選択** ダイアログ ボックスで、**PDP テンプレート** のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-179">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="2f088-180">**ページ名** 配下で、 **ページの PDP** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-180">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-181">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-181">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="2f088-182">**ページ フラグメントの選択** ダイアログ ボックスで、作成済の **購入ボックス フラグメント** フラグメントを選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f088-182">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="2f088-183">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="2f088-183">Save and preview the page.</span></span> <span data-ttu-id="2f088-184">**?productid=&lt;product id&gt;** クエリ文字列パラメーターをプレビュー ページの URL に追加します。</span><span class="sxs-lookup"><span data-stu-id="2f088-184">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="2f088-185">このようにして、製品コンテキストを使用してプレビュー ページの読み込みと表示を行います。</span><span class="sxs-lookup"><span data-stu-id="2f088-185">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="2f088-186">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="2f088-186">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="2f088-187">製品の詳細ページに、購入ボックスが表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f088-187">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f088-188">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2f088-188">Additional resources</span></span>

[<span data-ttu-id="2f088-189">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="2f088-189">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2f088-190">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-190">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="2f088-191">メディア ギャラリー モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-191">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="2f088-192">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-192">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2f088-193">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-193">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2f088-194">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-194">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2f088-195">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-195">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2f088-196">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-196">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2f088-197">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-197">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="2f088-198">ソーシャル共有モジュール</span><span class="sxs-lookup"><span data-stu-id="2f088-198">Social share module</span></span>](social-share-module.md)

[<span data-ttu-id="2f088-199">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="2f088-199">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="2f088-200">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="2f088-200">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
