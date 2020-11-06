---
title: カート モジュール
description: このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39026ec56ebf25342410330f2ba3e2e7773dfd6a
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055430"
---
# <a name="cart-module"></a><span data-ttu-id="abafc-103">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="abafc-104">このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="abafc-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="abafc-105">概要</span><span class="sxs-lookup"><span data-stu-id="abafc-105">Overview</span></span>

<span data-ttu-id="abafc-106">カート モジュールでは、顧客がチェックアウトに進む前にカートに追加された品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="abafc-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="abafc-107">モジュールには注文集計も表示され、顧客はプロモーション コードを適用または削除できます。</span><span class="sxs-lookup"><span data-stu-id="abafc-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="abafc-108">カート モジュールでは、サインインしたチェックアウトとゲスト チェックアウトがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="abafc-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="abafc-109">また、 **ショッピングに戻る** リンクもサポートされています。</span><span class="sxs-lookup"><span data-stu-id="abafc-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="abafc-110">**サイト設定 \> 拡張子 \> 工順** で、このリンクの工順をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="abafc-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="abafc-111">カート モジュールは、サイト全体で利用可能なブラウザー Cookie であるカート ID に基づいてデータをレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="abafc-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="abafc-112">次の図は、Fabrikam のサイトにおける買い物カゴ ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="abafc-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Fabrikam サイトにおける買い物カゴ モジュールの例](./media/cart2.PNG)

<span data-ttu-id="abafc-114">次の図は、Fabrikam のサイトにおける買い物カゴ ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="abafc-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="abafc-115">この例では、明細行品目の手数料があります。</span><span class="sxs-lookup"><span data-stu-id="abafc-115">In this example, there is a handling fee for a line item.</span></span>

![品目に対する取扱手数料がある買い物カゴ モジュールの例](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="abafc-117">カート モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="abafc-117">Cart module properties and slots</span></span>

| <span data-ttu-id="abafc-118">プロパティ</span><span class="sxs-lookup"><span data-stu-id="abafc-118">Property</span></span> | <span data-ttu-id="abafc-119">値</span><span class="sxs-lookup"><span data-stu-id="abafc-119">Values</span></span> | <span data-ttu-id="abafc-120">説明</span><span class="sxs-lookup"><span data-stu-id="abafc-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="abafc-121">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="abafc-121">Heading</span></span> | <span data-ttu-id="abafc-122">ヘッダー テキストとヘッダー タグ ( **H1** 、 **H2** 、 **H3** 、 **H4** 、 **H5** 、または **H6** )</span><span class="sxs-lookup"><span data-stu-id="abafc-122">Heading text and a heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="abafc-123">"ショッピング バッグ" や "カート内の品目" などのカートのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="abafc-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="abafc-124">在庫切れエラーを表示する</span><span class="sxs-lookup"><span data-stu-id="abafc-124">Show out of stock errors</span></span> | <span data-ttu-id="abafc-125">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="abafc-125">**True** or **False**</span></span> | <span data-ttu-id="abafc-126">このプロパティが **True** に設定されている場合、カート ページには在庫関連エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="abafc-126">If this property is set to **True** , the cart page will show stock-related errors.</span></span> <span data-ttu-id="abafc-127">サイトに在庫チェックを適用する場合は、このプロパティを **True** に設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="abafc-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="abafc-128">明細行品目の送料を表示する</span><span class="sxs-lookup"><span data-stu-id="abafc-128">Show shipping charges for line items</span></span> | <span data-ttu-id="abafc-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="abafc-129">**True** or **False**</span></span> | <span data-ttu-id="abafc-130">このプロパティが **True** に設定されていて、この情報が使用可能な場合、カート明細行品目に出荷費用が表示されます。</span><span class="sxs-lookup"><span data-stu-id="abafc-130">If this property is set to **True** , cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="abafc-131">この機能は、ユーザーがチェックアウト フローでのみ出荷を選択するので、Fabrikam のテーマではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="abafc-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="abafc-132">ただし、該当する場合は、この機能を他のワークフローで有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="abafc-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="abafc-133">カート モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="abafc-134">**テキスト ブロック** – このモジュールは、カート モジュールのカスタム メッセージングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="abafc-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="abafc-135">メッセージは、コンテンツ管理システム (CMS) よって発生します。</span><span class="sxs-lookup"><span data-stu-id="abafc-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="abafc-136">"注文に関する問題については、1-800-Fabrikam にお問い合わせください" などのメッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="abafc-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="abafc-137">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="abafc-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="abafc-138">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="abafc-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="abafc-139">このモジュールの詳細については、[ストア セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abafc-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="abafc-140">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="abafc-140">Module properties</span></span>

<span data-ttu-id="abafc-141">以下の買い物カゴ モジュールは、 **サイト設定 \> 拡張** で構成可能です :</span><span class="sxs-lookup"><span data-stu-id="abafc-141">The following cart module settings can be configured at **Site Settings \> Extensions** :</span></span>

- <span data-ttu-id="abafc-142">**最大数量** – このプロパティは、カートに追加できる各品目の最大数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="abafc-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="abafc-143">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="abafc-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="abafc-144">**在庫** - 在庫設定の適用方法については、[在庫設定を適用する](inventory-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abafc-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="abafc-145">**ショッピングに戻る** – このプロパティは、 **ショッピングに戻る** リンクの工順を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="abafc-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="abafc-146">このルートはサイト レベルで設定でき、小売業者は、顧客をサイトのホーム ページや他のページに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="abafc-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abafc-147">Dynamics 365 Commerce 10.0.14 リリース以降では、買い物カゴにある品目は、コマース本社のオンライン ストアのオンライン機能プロファイルで定義されている設定に基づいて集計されます。</span><span class="sxs-lookup"><span data-stu-id="abafc-147">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="abafc-148">オンライン機能プロファイルを作成し、集計に必要なプロパティを設定する方法の詳細については、[オンライン機能プロファイルの作成](online-functionality-profile.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abafc-148">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="abafc-149">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="abafc-149">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="abafc-150">カート モジュールでは、Commerce Scale Unit API を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="abafc-150">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="abafc-151">ブラウザー Cookie からのカート ID は、Commerce Scale Unit API からすべての製品情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="abafc-151">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="abafc-152">カート モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="abafc-152">Add a cart module to a page</span></span>

<span data-ttu-id="abafc-153">新しいページにカート モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="abafc-153">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="abafc-154">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="abafc-154">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="abafc-155">**新規フラグメント** ダイアログ ボックスで、 **カート** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-155">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="abafc-156">**フラグメント名** で、名前に **カート フラグメント** と入力し、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-156">Under **Fragment name** , enter the name **Cart fragment** , and then select **OK**.</span></span>
1. <span data-ttu-id="abafc-157">**買い物カゴ** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-157">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="abafc-158">右側の [プロパティ] ウィンドウで、鉛筆の記号を選択し、フィールドに見出しテキストを入力し、続いてチェックマーク記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-158">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="abafc-159">**買い物カゴ** スロットの省略ボタン ( **...** ) を選択し、 **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-159">In the **Cart** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="abafc-160">**モジュールの追加** ダイアログ ボックスで、 **店舗セレクター** モジュールを選択して、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-160">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="abafc-161">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="abafc-161">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="abafc-162">**テンプレート** に移動し、 **新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="abafc-162">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="abafc-163">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、テンプレートの名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="abafc-163">In the **New Template** dialog box, under **Template name** , enter a name for the template.</span></span>
1. <span data-ttu-id="abafc-164">アウトライン ツリーで **本文** スロットを選択し、省略記号 ( **...** ) を選択し、続いて **フラグメントのの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-164">In the outline tree, select the **Body** slot, select the ellipsis ( **...** ), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="abafc-165">**ページ フラグメントの選択** ダイアログ ボックスで、フラグメントに **カート フラグメント** を選択して、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-165">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="abafc-166">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="abafc-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="abafc-167">**ページ** に移動し、 **新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="abafc-167">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="abafc-168">**フラグメントの選択** ダイアログ ボックスで、作成したテンプレートを選択し、ページ名を入力し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abafc-168">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="abafc-169">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="abafc-169">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="abafc-170">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="abafc-170">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abafc-171">追加リソース</span><span class="sxs-lookup"><span data-stu-id="abafc-171">Additional resources</span></span>

[<span data-ttu-id="abafc-172">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-172">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="abafc-173">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-173">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="abafc-174">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-174">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="abafc-175">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-175">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="abafc-176">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-176">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="abafc-177">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-177">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="abafc-178">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="abafc-178">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="abafc-179">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="abafc-179">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="abafc-180">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="abafc-180">Create an online functionality profile</span></span>](online-functionality-profile.md)
