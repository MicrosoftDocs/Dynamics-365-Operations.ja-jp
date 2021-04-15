---
title: 評価とレビューのコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5161755b9e15e93fbb5eeb6404ea0820f7068ea7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796078"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="5785e-103">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5785e-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5785e-104">このトピックでは、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5785e-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5785e-105">概要</span><span class="sxs-lookup"><span data-stu-id="5785e-105">Overview</span></span>

<span data-ttu-id="5785e-106">E コマース ウェブ サイトの評価およびレビューでは、それらの製品に対する他の顧客の意見を示すことによって、顧客が購入決定を行う前に製品について学ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="5785e-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="5785e-107">E コマース Web サイトは、評価とレビューも製品に関する顧客フィードバックを収集するためのメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="5785e-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="5785e-108">評価とレビューを表示するようサイトをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="5785e-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="5785e-109">テナント ID、レビュー テキストの長さ、レビュー タイトルの長さなどの評価とレビューのコンフィギュレーション値は、サイト レベルでコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="5785e-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="5785e-110">評価とレビューを表示するサイトをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5785e-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="5785e-111">**ホーム \> サイト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5785e-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="5785e-112">サイトの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="5785e-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="5785e-113">**サイト 設定 \> 拡張** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5785e-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="5785e-114">**レビュー テキストの最大長** フィールドに、レビュー テキストに設定できる最大文字数を入力します (たとえば **1000**)。</span><span class="sxs-lookup"><span data-stu-id="5785e-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="5785e-115">**レビュー タイトルの最大長** フィールドに、レビュー タイトルに設定できるの最大文字数を入力します (たとえば **55**)。</span><span class="sxs-lookup"><span data-stu-id="5785e-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="5785e-116">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5785e-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="5785e-117">次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="5785e-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![評価とレビューを表示するようサイトをコンフィギュレーションする](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="5785e-119">製品評価を PDP のレビュー セクションにリンクする</span><span class="sxs-lookup"><span data-stu-id="5785e-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="5785e-120">製品評価は、PDP 上部にある製品タイトルの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5785e-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="5785e-121">製品評価は、同じ PDP の **レビュー** セクションにリンクされるようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="5785e-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="5785e-122">製品評価を PDP の **レビュー** セクションにリンクするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5785e-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="5785e-123">PDP テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="5785e-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="5785e-124">**購入ボックス コンテナー モジュールの設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5785e-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="5785e-125">**購入ボックス** の **製品評価** を選択し、**クリックして完全にレビュー モジュールにリンクする** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5785e-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="5785e-126">次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="5785e-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![製品評価を PDP のレビュー セクションにリンクする](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="5785e-128">プライバシーおよびポリシー ページへのリンクをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="5785e-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="5785e-129">プライバシーおよびポリシー ページへのリンクをコンフィギュレーションするには次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5785e-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="5785e-130">**ホーム \> サイト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5785e-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="5785e-131">サイトの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="5785e-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="5785e-132">**サイト 設定 \> 拡張** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5785e-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="5785e-133">**ルート** タブの **RNR プライバシーおよびポリシー** で **リンクの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5785e-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="5785e-134">リンクが既に入力されており、置き換えたい場合は、リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="5785e-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="5785e-135">**リンクの追加** ダイアログ ボックスで、プライバシーおよびポリシー ページのリンクを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5785e-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="5785e-136">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5785e-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="5785e-137">次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="5785e-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![プライバシーおよびポリシー ページへのリンクをコンフィギュレーションします。](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="5785e-139">製品詳細ページに評価とレビュー モジュールをコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5785e-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="5785e-140">製品詳細ページの評価とレビュー モジュールのコンフィギュレーションについては、 [評価とレビュー モジュール](ratings-reviews-modules.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5785e-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5785e-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5785e-141">Additional resources</span></span>

[<span data-ttu-id="5785e-142">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="5785e-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="5785e-143">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="5785e-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="5785e-144">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="5785e-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="5785e-145">製品詳細ページに評価とレビュー モジュールをコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5785e-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="5785e-146">Dynamics 365 Retail の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="5785e-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]