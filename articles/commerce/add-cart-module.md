---
title: カート モジュール
description: このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411276"
---
# <a name="cart-module"></a><span data-ttu-id="7d0b3-103">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7d0b3-104">このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d0b3-105">概要</span><span class="sxs-lookup"><span data-stu-id="7d0b3-105">Overview</span></span>

<span data-ttu-id="7d0b3-106">カート モジュールでは、顧客がチェックアウトに進む前にカートに追加された品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="7d0b3-107">モジュールには注文集計も表示され、顧客はプロモーション コードを適用または削除できます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="7d0b3-108">カート モジュールでは、サインインしたチェックアウトとゲスト チェックアウトがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="7d0b3-109">また、**ショッピングに戻る**リンクもサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="7d0b3-110">**サイト設定 \> 拡張子 \> 工順**で、このリンクの工順をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="7d0b3-111">カート モジュールは、サイト全体で利用可能なブラウザー Cookie であるカート ID に基づいてデータをレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="7d0b3-112">次の図は、Fabrikam のサイトにおける買い物カゴ ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![買い物カゴ モジュールの例](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="7d0b3-114">カート モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="7d0b3-114">Cart module properties and slots</span></span>

<span data-ttu-id="7d0b3-115">カート モジュールには、**ヘッダー** プロパティがあり、**ショッピング バッグ**や**カート内の品目**などの値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="7d0b3-116">カート モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="7d0b3-117">**テキスト ブロック** – このモジュールは、カート モジュールのカスタム メッセージングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="7d0b3-118">メッセージは、コンテンツ管理システム (CMS) よって発生します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="7d0b3-119">"注文に関する問題については、1-800-Fabrikam にお問い合わせください" などのメッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="7d0b3-120">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="7d0b3-121">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="7d0b3-122">このモジュールの詳細については、[ストア セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="7d0b3-123">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d0b3-123">Module properties</span></span>

<span data-ttu-id="7d0b3-124">以下の買い物カゴ モジュールは、**サイト設定 \> 拡張**で構成可能です :</span><span class="sxs-lookup"><span data-stu-id="7d0b3-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="7d0b3-125">**最大数量** – このプロパティは、カートに追加できる各品目の最大数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="7d0b3-126">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="7d0b3-127">**在庫** - 在庫設定の適用方法については、[在庫設定を適用する](inventory-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="7d0b3-128">**ショッピングに戻る** – このプロパティは、**ショッピングに戻る**リンクの工順を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="7d0b3-129">このルートはサイト レベルで設定でき、小売業者は、顧客をサイトのホーム ページや他のページに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="7d0b3-130">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="7d0b3-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="7d0b3-131">カート モジュールでは、Commerce Scale Unit API を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="7d0b3-132">ブラウザー Cookie からのカート ID は、Commerce Scale Unit API からすべての製品情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="7d0b3-133">カート モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="7d0b3-133">Add a cart module to a page</span></span>

<span data-ttu-id="7d0b3-134">新しいページにカート モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7d0b3-135">**ページ フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="7d0b3-136">**新規ページ フラグメント** ダイアログ ボックスで、**買い物カゴ** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="7d0b3-137">**ページ フラグメント名**配下で、**買い物カゴ フラグメント**の名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="7d0b3-138">**買い物カゴ** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="7d0b3-139">右側の [プロパティ] ウィンドウで、鉛筆の記号を選択し、フィールドに見出しテキストを入力し、続いてチェックマーク記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="7d0b3-140">**買い物カゴ** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d0b3-141">**モジュールの追加** ダイアログ ボックスで、**店舗セレクター** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7d0b3-142">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7d0b3-143">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7d0b3-144">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、テンプレートの名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="7d0b3-145">アウトライン ツリーで**本文** スロットを選択し、省略記号 (**...**) を選択し、続いて**フラグメントのの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="7d0b3-146">**ページ フラグメントの選択** ダイアログ ボックスで、前述の手順で作成した**買い物カゴ フラグメント**を選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7d0b3-147">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7d0b3-148">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7d0b3-149">**フラグメントの選択** ダイアログ ボックスで、作成したテンプレートを選択し、ページ名を入力し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="7d0b3-150">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="7d0b3-151">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="7d0b3-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d0b3-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7d0b3-152">Additional resources</span></span>

[<span data-ttu-id="7d0b3-153">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="7d0b3-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7d0b3-154">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7d0b3-155">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="7d0b3-156">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7d0b3-157">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7d0b3-158">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7d0b3-159">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7d0b3-160">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7d0b3-161">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="7d0b3-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="7d0b3-162">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="7d0b3-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
