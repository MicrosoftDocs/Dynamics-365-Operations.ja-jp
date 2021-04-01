---
title: 評価とレビュー モジュール
description: このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページで使用される評価とレビューのモジュールについて説明します。
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 26658ebdbc70613baf30c344664133b9cf5911ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243772"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="38b5a-103">評価およびレビュー モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38b5a-104">このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページ (PDP) で使用される評価とレビューのモジュールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="38b5a-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="38b5a-105">E コマース Web サイトの評価およびレビューは、購入を決定する前に顧客が製品について学習するのに役立ち、製品に関する他の顧客のフィードバックを収集するメカニズムでもあります。</span><span class="sxs-lookup"><span data-stu-id="38b5a-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="38b5a-106">評価は、製品リスト ページ、カテゴリ リスト ページ、検索結果ページ、およびその他のサイト ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="38b5a-107">ヒストグラムと製品レビューの評価は、製品の詳細ページ (PDP) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="38b5a-108">**レビューを書く** ボタンで、顧客は製品の評価およびレビューを送信できます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="38b5a-109">これらの PDP 機能は、評価とレビュー モジュールによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="38b5a-110">PDP 上の評価とレビュー モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="38b5a-111">3 つのモジュールは、PDP 上の評価とレビューの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="38b5a-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="38b5a-112">レビューの書き込みモジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-112">Write review module</span></span>
- <span data-ttu-id="38b5a-113">製品レビュー リスト モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-113">Product reviews list module</span></span>
- <span data-ttu-id="38b5a-114">評価ヒストグラム モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-114">Ratings histogram module</span></span>
 
<span data-ttu-id="38b5a-115">次の図は、PDP の評価とレビュー モジュールがどのようなものかを示しています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![PDP 上の評価とレビュー モジュール](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="38b5a-117">E コマース サイト上の複数の PDP 間で評価とレビュー モジュールのコンフィグレーションを共有できるように、PDP テンプレートとレイアウトを最適化する方法の詳細は、[テンプレートとレイアウトの概要](templates-layouts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38b5a-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="38b5a-118">次の図は、**モジュールの追加** ダイアログ ボックスがどのように Dynamics 365 Commerce の評価とレビュー モジュールで表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="38b5a-119">![モジュールの追加ダイアログ ボックス](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="38b5a-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="38b5a-120">レビューの書き込みモジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-120">Write review module</span></span>

<span data-ttu-id="38b5a-121">レビューの書き込みモジュールには、ユーザーがサインインし、評価を割り当て、製品のレビューを書くことのできる **レビューを書く** ボタンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="38b5a-122">このモジュールで、ユーザーが以前に送信した評価またはレビューを編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="38b5a-123">このモジュールは通常、PDP 上の評価ヒストグラムおよび製品レビュー リスト モジュールの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="38b5a-124">次の図は、顧客が **レビューを書く** を選択したときに表示される **レビューを書く** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="38b5a-125">顧客は、このダイアログ ボックスを使用して評価およびレビューを送信できます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="38b5a-126">![レビューを書くダイアログ ボックス](media/rnr-eCommerce-write-review-module.png) 次の表は、オーサリング ツールでコンフィギュレーションする必要があるレビューの書き込みモジュール プロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="38b5a-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="38b5a-127">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="38b5a-127">Property name</span></span> | <span data-ttu-id="38b5a-128">金額</span><span class="sxs-lookup"><span data-stu-id="38b5a-128">Value</span></span>        | <span data-ttu-id="38b5a-129">プロパティの説明</span><span class="sxs-lookup"><span data-stu-id="38b5a-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="38b5a-130">氏名</span><span class="sxs-lookup"><span data-stu-id="38b5a-130">Name</span></span>          | <span data-ttu-id="38b5a-131">レビューの書き込み</span><span class="sxs-lookup"><span data-stu-id="38b5a-131">Write review</span></span> | <span data-ttu-id="38b5a-132">レビューの書き込みモジュールの名前。</span><span class="sxs-lookup"><span data-stu-id="38b5a-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="38b5a-133">評価ヒストグラム モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-133">Ratings histogram module</span></span>

<span data-ttu-id="38b5a-134">評価ヒストグラム モジュールは、評価ヒストグラムを表示します。</span><span class="sxs-lookup"><span data-stu-id="38b5a-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="38b5a-135">このモジュールは通常、レビューの書き込みモジュールと PDP の製品レビュー リスト モジュールの間に表示されます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="38b5a-136">評価ヒストグラム モジュールには、コンフィギュレーションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="38b5a-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="38b5a-137">PDP テンプレートにモジュールを追加するだけです。</span><span class="sxs-lookup"><span data-stu-id="38b5a-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="38b5a-138">次の図は、評価とレビュー モジュールが Dynamics 365 Commerce PDP 上で表示されるようコンフィギュレーションされているときに、どのような PDP テンプレートが表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="38b5a-139">![PDP 上で表示されるよう評価とレビューがコンフィギュレーションされている場合の PDP テンプレート](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="38b5a-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="38b5a-140">製品レビュー リスト モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-140">Product reviews list module</span></span>

<span data-ttu-id="38b5a-141">製品レビュー リスト モジュールは、製品レビューのリストと共に並べ替え、フィルタ、およびページネーション オプションを表示します。</span><span class="sxs-lookup"><span data-stu-id="38b5a-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="38b5a-142">このモジュールは通常、PDP の評価ヒストグラム モジュールの後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="38b5a-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="38b5a-143">次の表は、オーサリング ツールでコンフィギュレーションする必要がある 製品レビュー リスト モジュール プロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="38b5a-144">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="38b5a-144">Property name</span></span>              | <span data-ttu-id="38b5a-145">金額</span><span class="sxs-lookup"><span data-stu-id="38b5a-145">Value</span></span> | <span data-ttu-id="38b5a-146">プロパティの説明</span><span class="sxs-lookup"><span data-stu-id="38b5a-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="38b5a-147">各ページに表示されるレビュー</span><span class="sxs-lookup"><span data-stu-id="38b5a-147">Reviews shown on each page</span></span> | <span data-ttu-id="38b5a-148">10</span><span class="sxs-lookup"><span data-stu-id="38b5a-148">10</span></span>    | <span data-ttu-id="38b5a-149">PDP で一度に表示されるレビューの数</span><span class="sxs-lookup"><span data-stu-id="38b5a-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="38b5a-150">ユーザーがレビュー ページを移動できるように、**次へ** と **前へ** ボタンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="38b5a-151">評価ヒストグラム - 概要ビュー</span><span class="sxs-lookup"><span data-stu-id="38b5a-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="38b5a-152">製品レビュー リスト モジュールには、評価ヒストグラム モジュールを追加できるスロットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="38b5a-153">次の図は、Dynamics 365 Commerce の製品 レビュー リスト モジュールに評価ヒストグラム モジュールを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="38b5a-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![製品レビュー リスト モジュールにおける評価ヒストグラム モジュールの追加](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="38b5a-155">追加リソース</span><span class="sxs-lookup"><span data-stu-id="38b5a-155">Additional resources</span></span>

[<span data-ttu-id="38b5a-156">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="38b5a-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="38b5a-157">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="38b5a-158">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="38b5a-159">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="38b5a-160">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="38b5a-161">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="38b5a-162">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="38b5a-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]