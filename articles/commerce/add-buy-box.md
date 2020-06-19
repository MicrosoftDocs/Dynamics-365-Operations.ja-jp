---
title: 購入ボックス モジュール
description: このトピックでは、購入ボックス モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 583937be92b62991cd13f0806df4a0a6c9ac049c
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411345"
---
# <a name="buy-box-module"></a><span data-ttu-id="7e1f2-103">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-103">Buy box module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7e1f2-104">このトピックでは、購入ボックス モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7e1f2-105">概要</span><span class="sxs-lookup"><span data-stu-id="7e1f2-105">Overview</span></span>

<span data-ttu-id="7e1f2-106">*購入ボックス*という用語は、通常 "折りたたみの上" である製品の詳細ページの領域を指し、製品購買に必要な最も重要な情報すべてをホストします。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="7e1f2-107">("折りたたみの上" である領域はページが最初に読み込まれたときに表示されるため、ユーザーは下にスクロールして表示する必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="7e1f2-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="7e1f2-108">購入ボックス モジュールは、製品の詳細ページの購入ボックス領域に表示されるすべてのモジュールをホストするために使用する特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="7e1f2-109">製品の詳細ページの URL には、製品 ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="7e1f2-110">購買ボックス モジュールの表示に必要なすべての情報は、この製品 ID から派生します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="7e1f2-111">製品 ID が指定されていない場合、購入ボックス モジュールはページに正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="7e1f2-112">したがって、購入ボックス モジュールは、製品コンテキストがあるページでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="7e1f2-113">製品コンテキストがないページ (ホーム ページやマーケティング ページなど) で使用するには、追加のカスタマイズを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="7e1f2-114">以下の図は、[商品の詳細] ページにある [購入ボックス] モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-114">The following image shows an example of a buy box module on a product details page.</span></span>

![購入ボックス モジュールの例](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="7e1f2-116">購入ボックス モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="7e1f2-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="7e1f2-117">製品の詳細ページでは、購入ボックスは 2 つの領域に分割されます: 左側にメディア領域、右側にコンテンツ領域。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="7e1f2-118">既定では、メディア領域列の幅とコンテンツ領域列の幅の比率は 2:1 になります。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="7e1f2-119">モバイル デバイスでは 2 つの領域が積み重ねられ、一方の領域がもう一方の領域の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="7e1f2-120">テーマを使用して、列の幅やスタック ランクをカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="7e1f2-121">購入ボックス モジュールは、製品のタイトル、説明、価格、および評価をレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="7e1f2-122">また、顧客は、サイズ、スタイル、色などの製品属性が異なる製品バリアントを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="7e1f2-123">製品バリアントが選択されると、購入ボックスの他のプロパティ (製品の説明や画像など) が更新されて、バリアント情報が反映されます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="7e1f2-124">数量セレクターは、顧客が購入する品目の数量を指定できるようにするために用意されています。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="7e1f2-125">購入できる最大数量は、サイト設定で定義できます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="7e1f2-126">購入 ボックスから、カートへの製品の追加、欲しい物リストへの製品の追加、集配場所の選択などのアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="7e1f2-127">これらのアクションは、製品または製品バリアントに対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="7e1f2-128">製品を欲しい物リストに追加するには、顧客がサインインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="7e1f2-129">テーマを使用すると、購入ボックスの製品プロパティとアクション コントロールの順序を削除または変更できます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="7e1f2-130">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="7e1f2-130">Module properties</span></span>

- <span data-ttu-id="7e1f2-131">**ヘッダー タグ** ー このプロパティは、製品タイトルのヘッダー タグを定義します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="7e1f2-132">購入ボックスがページの一番上にある場合は、アクセシビリティ標準を満たすため、このプロパティを **h1** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="7e1f2-133">購入用ボックス モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="7e1f2-134">**メディア ギャラリー** – このモジュールは、製品の詳細ページに製品の画像を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="7e1f2-135">一対多の画像をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-135">It can support one to many images.</span></span> <span data-ttu-id="7e1f2-136">サムネイル画像もサポートします。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-136">It also supports thumbnail images.</span></span> <span data-ttu-id="7e1f2-137">サムネイル画像は、水平方向 (画像の下の行) または垂直方向 (画像の横の列) のいずれかに配置できます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-137">The thumbnail images can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="7e1f2-138">メディア ギャラリー モジュールは、購入ボックス モジュールの**メディア** スロットに追加できます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-138">The media gallery module can be added to the **Media** slot in the buy box module.</span></span> <span data-ttu-id="7e1f2-139">現在、画像のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-139">It currently supports only images.</span></span> 
- <span data-ttu-id="7e1f2-140">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="7e1f2-141">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="7e1f2-142">このモジュールの詳細については、[店舗セレクタ モジュール](store-selector.md) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-142">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="7e1f2-143">購入ボックス モジュール設定</span><span class="sxs-lookup"><span data-stu-id="7e1f2-143">Buy box module settings</span></span>

<span data-ttu-id="7e1f2-144">以下の購入ボックス モジュールは、**サイト設定 \> 拡張**で構成可能です :</span><span class="sxs-lookup"><span data-stu-id="7e1f2-144">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="7e1f2-145">**カートの明細行の数量上限** – このプロパティは、カートに追加できる各品目の最大数を指定する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-145">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="7e1f2-146">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="7e1f2-147">**在庫** - 在庫設定の適用方法については、[在庫設定を適用する](inventory-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="7e1f2-148">**カートに追加する** - このプロパティは、品目がカートに追加された後の動作を指定する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-148">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="7e1f2-149">使用可能な値は、**カートに移動する**、**カートに移動しない**、**通知を表示する** です。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-149">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="7e1f2-150">この値が **カートに移動する**に設定されている場合は 、ユーザーが品目を追加した後はカートのページに移動します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-150">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="7e1f2-151">この値が **カートに移動しない**に設定されている場合は 、ユーザーが品目を追加した後もカートのページに移動しません。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-151">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="7e1f2-152">この値が**通知を表示する**に設定されている場合、ユーザーに確認の通知が表示され、引き続き製品の詳細ページを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-152">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="7e1f2-153">次の画像では、Fabrikam サイトにおいて "カートに追加された" 際の確認通知の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-153">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![通知モジュールの例](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="7e1f2-155">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="7e1f2-155">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="7e1f2-156">購入ボックス モジュールでは、Commerce Scale Unit アプリケーションのプログラム インターフェース (API) を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-156">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="7e1f2-157">製品の詳細ページの製品 ID は、すべての情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-157">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="7e1f2-158">購入ボックス モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="7e1f2-158">Add a buy box module to a page</span></span>

<span data-ttu-id="7e1f2-159">新しいページに購入ボックス モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-159">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7e1f2-160">**ページ フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-160">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="7e1f2-161">**新規ページ フラグメント** ダイアログ ボックスで、**購入ボックス** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-161">In the **New Page Fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="7e1f2-162">**ページ フラグメント名**配下で、**購入ボックス フラグメント**の名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-162">Under **Page Fragment Name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-163">購入用ボックス モジュールを含む**メディア ギャラリー** スロットにて、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-163">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7e1f2-164">**モジュールの追加** ダイアログ ボックスで、**メディア ギャラリー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-164">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-165">購入用ボックス モジュールを含む**店舗セレクター** スロットにて、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-165">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7e1f2-166">**モジュールの追加** ダイアログ ボックスで、**店舗セレクター** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-166">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-167">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-167">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7e1f2-168">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-168">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7e1f2-169">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**PDP のテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-169">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-170">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-170">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7e1f2-171">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-171">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-172">既定のページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**ページ フラグメントの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-172">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="7e1f2-173">**ページ フラグメントの選択** ダイアログ ボックスで、前述の手順で作成した**購入ボックス フラグメント**を選択し、続いて**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-173">In the **Select Page Fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-174">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-174">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7e1f2-175">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-175">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7e1f2-176">**テンプレートの選択** ダイアログ ボックスで、**PDP テンプレート**のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-176">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="7e1f2-177">**ページ名**配下で、 **ページの PDP**を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-177">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-178">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**ページ フラグメントの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-178">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="7e1f2-179">**ページ フラグメントの選択** ダイアログ ボックスで、前述の手順で作成した**購入ボックス フラグメント**を選択し、続いて**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-179">In the **Select Page Fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="7e1f2-180">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-180">Save and preview the page.</span></span> <span data-ttu-id="7e1f2-181">**?productid=&lt;product id&gt;** クエリ文字列パラメーターをプレビュー ページの URL に追加します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-181">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="7e1f2-182">このようにして、製品コンテキストを使用してプレビュー ページの読み込みと表示を行います。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-182">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="7e1f2-183">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-183">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="7e1f2-184">製品の詳細ページに、購入ボックスが表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e1f2-184">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e1f2-185">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7e1f2-185">Additional resources</span></span>

[<span data-ttu-id="7e1f2-186">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="7e1f2-186">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7e1f2-187">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-187">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="7e1f2-188">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-188">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7e1f2-189">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-189">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7e1f2-190">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-190">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7e1f2-191">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-191">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7e1f2-192">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-192">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7e1f2-193">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-193">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7e1f2-194">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="7e1f2-194">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="7e1f2-195">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="7e1f2-195">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
