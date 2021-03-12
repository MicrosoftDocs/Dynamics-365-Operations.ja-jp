---
title: カート モジュール
description: このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: abb9909c03577763ff7e6242c9395a58159df6ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985982"
---
# <a name="cart-module"></a><span data-ttu-id="4c38c-103">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c38c-104">このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4c38c-105">概要</span><span class="sxs-lookup"><span data-stu-id="4c38c-105">Overview</span></span>

<span data-ttu-id="4c38c-106">カート モジュールでは、顧客がチェックアウトに進む前にカートに追加された品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="4c38c-107">モジュールには注文集計も表示され、顧客はプロモーション コードを適用または削除できます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="4c38c-108">カート モジュールでは、サインインしたチェックアウトとゲスト チェックアウトがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4c38c-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="4c38c-109">また、**ショッピングに戻る** リンクもサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4c38c-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="4c38c-110">**サイト設定 \> 拡張子 \> 工順** で、このリンクの工順をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="4c38c-111">カート モジュールは、サイト全体で利用可能なブラウザー Cookie であるカート ID に基づいてデータをレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="4c38c-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="4c38c-112">次の図は、Fabrikam のサイトにおける買い物カゴ ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c38c-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Fabrikam サイトにおける買い物カゴ モジュールの例](./media/cart2.PNG)

<span data-ttu-id="4c38c-114">次の図は、Fabrikam のサイトにおける買い物カゴ ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="4c38c-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="4c38c-115">この例では、明細行品目の手数料があります。</span><span class="sxs-lookup"><span data-stu-id="4c38c-115">In this example, there is a handling fee for a line item.</span></span>

![品目に対する取扱手数料がある買い物カゴ モジュールの例](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="4c38c-117">カート モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="4c38c-117">Cart module properties and slots</span></span>

| <span data-ttu-id="4c38c-118">プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c38c-118">Property</span></span> | <span data-ttu-id="4c38c-119">値</span><span class="sxs-lookup"><span data-stu-id="4c38c-119">Values</span></span> | <span data-ttu-id="4c38c-120">説明</span><span class="sxs-lookup"><span data-stu-id="4c38c-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4c38c-121">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="4c38c-121">Heading</span></span> | <span data-ttu-id="4c38c-122">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="4c38c-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4c38c-123">"ショッピング バッグ" や "カート内の品目" などのカートのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="4c38c-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="4c38c-124">在庫切れエラーを表示する</span><span class="sxs-lookup"><span data-stu-id="4c38c-124">Show out of stock errors</span></span> | <span data-ttu-id="4c38c-125">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="4c38c-125">**True** or **False**</span></span> | <span data-ttu-id="4c38c-126">このプロパティが **True** に設定されている場合、カート ページには在庫関連エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="4c38c-127">サイトに在庫チェックを適用する場合は、このプロパティを **True** に設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4c38c-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="4c38c-128">明細行品目の送料を表示する</span><span class="sxs-lookup"><span data-stu-id="4c38c-128">Show shipping charges for line items</span></span> | <span data-ttu-id="4c38c-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="4c38c-129">**True** or **False**</span></span> | <span data-ttu-id="4c38c-130">このプロパティが **True** に設定されていて、この情報が使用可能な場合、カート明細行品目に出荷費用が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="4c38c-131">この機能は、ユーザーがチェックアウト フローでのみ出荷を選択するので、Fabrikam のテーマではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4c38c-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="4c38c-132">ただし、該当する場合は、この機能を他のワークフローで有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="4c38c-133">使用可能なプロモーションの表示</span><span class="sxs-lookup"><span data-stu-id="4c38c-133">Show available promotions</span></span>| <span data-ttu-id="4c38c-134">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="4c38c-134">**True** or **False**</span></span> | <span data-ttu-id="4c38c-135">このプロパティが **True** に設定されている場合は、カート内の品目に基づいて利用できるプロモーションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-135">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="4c38c-136">この機能は Dynamics 365 Commerce 10.0.16 リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-136">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="4c38c-137">カート モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-137">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="4c38c-138">**テキスト ブロック** – このモジュールは、カート モジュールのカスタム メッセージングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4c38c-138">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="4c38c-139">メッセージは、コンテンツ管理システム (CMS) よって発生します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-139">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="4c38c-140">"注文に関する問題については、1-800-Fabrikam にお問い合わせください" などのメッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-140">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="4c38c-141">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-141">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="4c38c-142">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-142">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="4c38c-143">このモジュールの詳細については、[ストア セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c38c-143">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="4c38c-144">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c38c-144">Module properties</span></span>

<span data-ttu-id="4c38c-145">以下の買い物カゴ モジュールは、**サイト設定 \> 拡張** で構成可能です :</span><span class="sxs-lookup"><span data-stu-id="4c38c-145">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="4c38c-146">**最大数量** – このプロパティは、カートに追加できる各品目の最大数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-146">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="4c38c-147">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="4c38c-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="4c38c-148">**在庫** - 在庫設定の適用方法については、[在庫設定を適用する](inventory-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c38c-148">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="4c38c-149">**ショッピングに戻る** – このプロパティは、**ショッピングに戻る** リンクの工順を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-149">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="4c38c-150">このルートはサイト レベルで設定でき、小売業者は、顧客をサイトのホーム ページや他のページに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-150">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c38c-151">Dynamics 365 Commerce 10.0.14 リリース以降では、買い物カゴにある品目は、コマース本社のオンライン ストアのオンライン機能プロファイルで定義されている設定に基づいて集計されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-151">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="4c38c-152">オンライン機能プロファイルを作成し、集計に必要なプロパティを設定する方法の詳細については、[オンライン機能プロファイルの作成](online-functionality-profile.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c38c-152">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="4c38c-153">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="4c38c-153">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="4c38c-154">カート モジュールでは、Commerce Scale Unit API を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-154">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="4c38c-155">ブラウザー Cookie からのカート ID は、Commerce Scale Unit API からすべての製品情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4c38c-155">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="4c38c-156">カート モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="4c38c-156">Add a cart module to a page</span></span>

<span data-ttu-id="4c38c-157">新しいページにカート モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-157">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4c38c-158">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-158">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="4c38c-159">**新規フラグメント** ダイアログ ボックスで、**カート** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-159">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="4c38c-160">**フラグメント名** で、名前に **カート フラグメント** と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-160">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="4c38c-161">**買い物カゴ** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-161">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="4c38c-162">右側の [プロパティ] ウィンドウで、鉛筆の記号を選択し、フィールドに見出しテキストを入力し、続いてチェックマーク記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-162">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="4c38c-163">**買い物カゴ** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-163">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4c38c-164">**モジュールの追加** ダイアログ ボックスで、**店舗セレクター** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-164">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4c38c-165">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-165">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4c38c-166">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-166">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="4c38c-167">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、テンプレートの名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-167">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="4c38c-168">アウトライン ツリーで **本文** スロットを選択し、省略記号 (**...**) を選択し、続いて **フラグメントのの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-168">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="4c38c-169">**ページ フラグメントの選択** ダイアログ ボックスで、フラグメントに **カート フラグメント** を選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-169">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="4c38c-170">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4c38c-171">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="4c38c-172">**フラグメントの選択** ダイアログ ボックスで、作成したテンプレートを選択し、ページ名を入力し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-172">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="4c38c-173">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="4c38c-173">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="4c38c-174">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="4c38c-174">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c38c-175">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4c38c-175">Additional resources</span></span>

[<span data-ttu-id="4c38c-176">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-176">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4c38c-177">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4c38c-178">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-178">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4c38c-179">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-179">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4c38c-180">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-180">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4c38c-181">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-181">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="4c38c-182">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-182">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4c38c-183">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="4c38c-183">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="4c38c-184">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="4c38c-184">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="4c38c-185">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="4c38c-185">Create an online functionality profile</span></span>](online-functionality-profile.md)
