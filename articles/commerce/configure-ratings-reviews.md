---
title: 評価とレビューのコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770484"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="0a5ee-103">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0a5ee-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0a5ee-104">このトピックでは、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0a5ee-105">概要</span><span class="sxs-lookup"><span data-stu-id="0a5ee-105">Overview</span></span>

<span data-ttu-id="0a5ee-106">E コマース Web サイトの評価およびレビューでは、それらの製品に対する他の顧客の意見を示すことによって顧客が購入決定を行う前に製品について学ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="0a5ee-107">E コマース Web サイトは、評価とレビューも製品に関する顧客フィードバックを収集するためのメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="0a5ee-108">評価は、製品リスト ページ、カテゴリ リスト ページ、検索結果ページ、およびその他のサイト ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="0a5ee-109">ヒストグラムと製品レビューの評価は、製品の詳細ページ (PDP) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="0a5ee-110">**レビューを書く**ボタンで、顧客は製品の評価およびレビューを送信できます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="0a5ee-111">PDP 上の評価とレビュー モジュール</span><span class="sxs-lookup"><span data-stu-id="0a5ee-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="0a5ee-112">3 つのモジュールは、PDP 上の評価とレビューの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="0a5ee-113">レビューの書き込みモジュール</span><span class="sxs-lookup"><span data-stu-id="0a5ee-113">Write review module</span></span>
- <span data-ttu-id="0a5ee-114">製品レビュー リスト モジュール</span><span class="sxs-lookup"><span data-stu-id="0a5ee-114">Product reviews list module</span></span>
- <span data-ttu-id="0a5ee-115">評価ヒストグラム モジュール</span><span class="sxs-lookup"><span data-stu-id="0a5ee-115">Ratings histogram module</span></span>
 
<span data-ttu-id="0a5ee-116">次の図は、PDP の評価とレビュー モジュールがどのようなものかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![PDP 上の評価とレビュー モジュール](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="0a5ee-118">E コマース サイト上の複数の PDP 間で評価とレビュー モジュールのコンフィグレーションを共有できるように、PDP テンプレートとレイアウトを最適化する方法の詳細は、[テンプレートとレイアウトの概要](templates-layouts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="0a5ee-119">次の図は、**モジュールの追加**ダイアログ ボックスがどのように Dynamics 365 Commerce の評価とレビュー モジュールで表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![モジュールの追加ダイアログ ボックス](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="0a5ee-121">レビューの書き込みモジュール</span><span class="sxs-lookup"><span data-stu-id="0a5ee-121">Write review module</span></span>

<span data-ttu-id="0a5ee-122">レビューの書き込みモジュールには、ユーザーがサインインし、評価を割り当て、製品のレビューを書くことのできる**レビューを書く**ボタンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="0a5ee-123">このモジュールで、ユーザーが以前に送信した評価またはレビューを編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="0a5ee-124">このモジュールは通常、PDP 上の評価ヒストグラムおよび製品レビュー リスト モジュールの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="0a5ee-125">次の図は、顧客が**レビューを書く**を選択したときに表示される**レビューを書く**ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="0a5ee-126">顧客は、このダイアログ ボックスを使用して評価およびレビューを送信できます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![レビューを書くダイアログ ボックス](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="0a5ee-128">次の表は、オーサリング ツールでコンフィギュレーションする必要がある レビューの書き込みモジュール プロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0a5ee-129">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0a5ee-129">Property name</span></span> | <span data-ttu-id="0a5ee-130">金額</span><span class="sxs-lookup"><span data-stu-id="0a5ee-130">Value</span></span>        | <span data-ttu-id="0a5ee-131">プロパティの説明</span><span class="sxs-lookup"><span data-stu-id="0a5ee-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="0a5ee-132">氏名</span><span class="sxs-lookup"><span data-stu-id="0a5ee-132">Name</span></span>          | <span data-ttu-id="0a5ee-133">レビューの書き込み</span><span class="sxs-lookup"><span data-stu-id="0a5ee-133">Write review</span></span> | <span data-ttu-id="0a5ee-134">レビューの書き込みモジュールの名前。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="0a5ee-135">評価ヒストグラム モジュール</span><span class="sxs-lookup"><span data-stu-id="0a5ee-135">Ratings histogram module</span></span>

<span data-ttu-id="0a5ee-136">評価ヒストグラム モジュールは、評価ヒストグラムを表示します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="0a5ee-137">このモジュールは通常、レビューの書き込みモジュールと PDP の製品レビュー リスト モジュールの間に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="0a5ee-138">評価ヒストグラム モジュールには、コンフィギュレーションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="0a5ee-139">PDP テンプレートにモジュールを追加するだけです。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="0a5ee-140">次の図は、評価とレビュー モジュールが Dynamics 365 Commerce PDP 上で表示されるようコンフィギュレーションされているときに、どのような PDP テンプレートが表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP 上で表示されるよう評価とレビューがコンフィギュレーションされている場合の PDP テンプレート](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="0a5ee-142">製品レビュー リスト モジュール</span><span class="sxs-lookup"><span data-stu-id="0a5ee-142">Product reviews list module</span></span>

<span data-ttu-id="0a5ee-143">製品レビュー リスト モジュールは、製品レビューのリストと共に並べ替え、フィルタ、およびページネーション オプションを表示します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="0a5ee-144">このモジュールは通常、PDP の評価ヒストグラム モジュールの後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="0a5ee-145">次の表は、オーサリング ツールでコンフィギュレーションする必要がある 製品レビュー リスト モジュール プロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0a5ee-146">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0a5ee-146">Property name</span></span>              | <span data-ttu-id="0a5ee-147">金額</span><span class="sxs-lookup"><span data-stu-id="0a5ee-147">Value</span></span> | <span data-ttu-id="0a5ee-148">プロパティの説明</span><span class="sxs-lookup"><span data-stu-id="0a5ee-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="0a5ee-149">各ページに表示されるレビュー</span><span class="sxs-lookup"><span data-stu-id="0a5ee-149">Reviews shown on each page</span></span> | <span data-ttu-id="0a5ee-150">10</span><span class="sxs-lookup"><span data-stu-id="0a5ee-150">10</span></span>    | <span data-ttu-id="0a5ee-151">PDP で一度に表示されるレビューの数</span><span class="sxs-lookup"><span data-stu-id="0a5ee-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="0a5ee-152">ユーザーがレビュー ページを移動できるように、**次へ**と**前へ**ボタンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="0a5ee-153">評価ヒストグラム - 概要ビュー</span><span class="sxs-lookup"><span data-stu-id="0a5ee-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="0a5ee-154">製品レビュー リスト モジュールには、評価ヒストグラム モジュールを追加できるスロットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="0a5ee-155">次の図は、Dynamics 365 Commerce の製品 レビュー リスト モジュールに評価ヒストグラム モジュールを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![製品レビュー リスト モジュールにおける評価ヒストグラム モジュールの追加](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="0a5ee-157">評価とレビューを表示するようサイトをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="0a5ee-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="0a5ee-158">テナント ID、レビュー テキストの長さ、レビュー タイトルの長さなどの評価とレビューのコンフィギュレーション値は、サイト レベルでコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="0a5ee-159">評価とレビューを表示するサイトをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="0a5ee-160">**ホーム \> サイト**に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0a5ee-161">サイトの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="0a5ee-162">**サイト管理 \> 拡張性**に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="0a5ee-163">**レビュー テキストの最大長**フィールドに、レビュー テキストに設定できる最大文字数を入力します (たとえば **1000**)。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="0a5ee-164">**レビュー タイトルの最大長**フィールドに、レビュー タイトルに設定できる最大文字数を入力します (たとえば、**55**)。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="0a5ee-165">**保存と公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0a5ee-166">次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![評価とレビューを表示するようサイトをコンフィギュレーションする](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="0a5ee-168">製品評価を PDP のレビュー セクションにリンクする</span><span class="sxs-lookup"><span data-stu-id="0a5ee-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="0a5ee-169">製品評価は、PDP 上部にある製品タイトルの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="0a5ee-170">製品評価は、同じ PDP の**レビュー** セクションにリンクされるようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="0a5ee-171">製品評価を PDP の**レビュー**セクションにリンクするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="0a5ee-172">PDP テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="0a5ee-173">**購入ボックス コンテナー モジュールの設定**に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="0a5ee-174">**購入ボックス**の**製品評価**を選択し、**クリックして完全にレビュー モジュールにリンクする**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="0a5ee-175">次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![製品評価を PDP のレビュー セクションにリンクする](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="0a5ee-177">プライバシーおよびポリシー ページへのリンクをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="0a5ee-178">プライバシーおよびポリシー ページへのリンクをコンフィギュレーションするには次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="0a5ee-179">**ホーム \> サイト**に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0a5ee-180">サイトの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="0a5ee-181">**サイト管理 \> 拡張性**に移動します</span><span class="sxs-lookup"><span data-stu-id="0a5ee-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="0a5ee-182">**ルート** タブの**RNR プライバシーおよびポリシー**で**リンクの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="0a5ee-183">リンクが既に入力されており、置き換えたい場合は、リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="0a5ee-184">**リンクの追加**ダイアログ ボックスで、プライバシーおよびポリシー ページのリンクを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="0a5ee-185">**保存と公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0a5ee-186">次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0a5ee-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![プライバシーおよびポリシー ページへのリンクをコンフィギュレーションします。](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="0a5ee-188">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0a5ee-188">Additional resources</span></span>

[<span data-ttu-id="0a5ee-189">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="0a5ee-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="0a5ee-190">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="0a5ee-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="0a5ee-191">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="0a5ee-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="0a5ee-192">Dynamics 365 Retail の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="0a5ee-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
