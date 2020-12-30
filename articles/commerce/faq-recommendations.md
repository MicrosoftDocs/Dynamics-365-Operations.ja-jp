---
title: 製品推奨事項に関するよく寄せられる質問
description: このトピックでは、製品推奨事項またはその結果に関連する問題のトラブルシューティングに使用できる、プロセスおよびツールに関する情報を提供します。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cf3df2267671b50c20b28dbdb1c6a21696bf2515
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413643"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="b5952-103">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b5952-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b5952-104">このトピックでは、[製品推奨事項](product-recommendations.md)またはその結果に関連する問題のトラブルシューティングに使用できる、プロセスおよびツールに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b5952-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="b5952-105">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="b5952-105">Best practices</span></span>
<span data-ttu-id="b5952-106">製品マスターとバリアントの概念を活用することは非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="b5952-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="b5952-107">親製品マスターに対するバリアントの正確なグループ化は、リスト アルゴリズムとサービスがより良いモデルを作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b5952-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="b5952-108">さらにこのサービスは、密接に関係するすべてのバリアントをリストに含める代わりに、製品のインスタンスを 1 つだけ提供します。</span><span class="sxs-lookup"><span data-stu-id="b5952-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="b5952-109">密接に関係するすべてのバリアントがリストに追加されると、エラーまたは重複する結果が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5952-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="b5952-110">製品が推奨リストに見つからないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="b5952-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="b5952-111">通常、製品推奨リストに品目が含まれていない場合は、製品コンフィギュレーションに問題がある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5952-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="b5952-112">たとえば、製品の開始日または終了日が正しくない場合や、分析コードの構成に誤りがある場合、または製品が正しいチャンネル品揃えに含まれていない場合などが考えられます。</span><span class="sxs-lookup"><span data-stu-id="b5952-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="b5952-113">人為的知能の機械学習 (AI-ML) に基づく推奨リストに品目が含まれていない場合、その品目は推奨リストの基準に適合していないか、推奨リストを表示するための十分な購入トランザクションがない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5952-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="b5952-114">次の手順を確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5952-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="b5952-115">**製品推奨事項が本社で有効になっていることを確認します。**</span><span class="sxs-lookup"><span data-stu-id="b5952-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="b5952-116">このサービスを有効にする方法の詳細については、[製品推奨事項の有効化](enable-product-recommendations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="b5952-117">**主要製品のプロパティが設定されていることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="b5952-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="b5952-118">たとえば、製品の品揃えは **含める** ように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5952-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="b5952-119">**新たに類別された製品については、製品が新しい一覧に表示されるまでに最大で 3 時間かかる場合があります。**</span><span class="sxs-lookup"><span data-stu-id="b5952-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="b5952-120">**製品がトレンド、ベストセラー、人気製品、またはよく一緒に購入されるものに表示されない場合、その製品に対して十分なトランザクションがない可能性があります。**</span><span class="sxs-lookup"><span data-stu-id="b5952-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="b5952-121">この場合、さらにトランザクションが発生するのを待つか、既定の推奨リスト パラメーターを更新するか、手動操作で推奨製品リストの結果を変更します。</span><span class="sxs-lookup"><span data-stu-id="b5952-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="b5952-122">推奨パラメーターの詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="b5952-123">**製品がリストの推奨基準を満たしていることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="b5952-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="b5952-124">製品推奨パラメーターの詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="b5952-125">低い推奨結果が返されないようにするにはどうすればよいでしょうか。</span><span class="sxs-lookup"><span data-stu-id="b5952-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="b5952-126">推奨リストは、結果を生成するために大量のトランザクションを必要とします。</span><span class="sxs-lookup"><span data-stu-id="b5952-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="b5952-127">したがって、ユーザーが完全なトランザクション履歴データを提供することが重要になってきます。</span><span class="sxs-lookup"><span data-stu-id="b5952-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="b5952-128">さらに、トランザクションがないか、トランザクションがほとんどない製品には、通常 **人気製品** または **よく一緒に購入される製品** のような結果も含まれません。また **トレンド** や **ベストセラー** の推奨リストにも表示されません。</span><span class="sxs-lookup"><span data-stu-id="b5952-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="b5952-129">この状況は、非常に新しい製品、または購入数が少ない古い製品でよく発生します。</span><span class="sxs-lookup"><span data-stu-id="b5952-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="b5952-130">人気のある新しい製品は、この問題を容易に解決できます。</span><span class="sxs-lookup"><span data-stu-id="b5952-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="b5952-131">次の手順を実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5952-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="b5952-132">**製品がそのリストの推奨基準を満たしていることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="b5952-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="b5952-133">製品推奨パラメーターの詳細については、AI-ML ベースの製品推奨事項の結果の変更を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="b5952-134">**製品が新しい場合は、製品のトランザクションがさらに増えるまで、推奨リストを変更することを検討してください。**</span><span class="sxs-lookup"><span data-stu-id="b5952-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="b5952-135">推奨リスト結果の変更方法の詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="b5952-136">**製品がそのリストの推奨基準を満たしていることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="b5952-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="b5952-137">製品推奨パラメーターの詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="b5952-138">**製品が新しい場合は、製品のトランザクションがさらに増えるまで、推奨リストを変更することを検討してください**。</span><span class="sxs-lookup"><span data-stu-id="b5952-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="b5952-139">推奨リスト結果の変更方法の詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="b5952-140">製品を削除しても、店舗でそれを閲覧することはできますか。</span><span class="sxs-lookup"><span data-stu-id="b5952-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="b5952-141">業務上の必要性に応じて、アルゴリズムによって生成されたリストを調整できます。</span><span class="sxs-lookup"><span data-stu-id="b5952-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="b5952-142">ただし、製品が推奨リストから削除された場合、その製品は店舗内で引き続き検出可能になります。</span><span class="sxs-lookup"><span data-stu-id="b5952-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="b5952-143">製品推奨事項の結果の変更方法の詳細については、[AI-ML ベースの製品推奨事項の結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="b5952-144">店舗での品目の検出をブロックする必要がある場合は、**品目分類** の値を **除外** に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5952-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="b5952-145">E コマース ページにリストを追加する方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="b5952-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="b5952-146">製品推奨事項ページを E コマース Web サイトに追加する方法の詳細については、[製品推奨リストをページに追加する](add-reco-list-to-page.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="b5952-147">POS で推奨事項を有効にするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="b5952-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="b5952-148">製品の推奨事項を有効にした後、制御 POS 画面に推奨事項パネルを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5952-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="b5952-149">詳細については、[POS デバイスのトランザクション画面に推奨事項コントロールを追加](add-recommendations-control-pos-screen.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5952-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5952-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b5952-150">Additional resources</span></span>

[<span data-ttu-id="b5952-151">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="b5952-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b5952-152">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="b5952-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b5952-153">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="b5952-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b5952-154">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="b5952-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b5952-155">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="b5952-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b5952-156">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="b5952-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="b5952-157">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="b5952-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b5952-158">トランザクション画面への推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="b5952-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b5952-159">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="b5952-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b5952-160">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="b5952-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b5952-161">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="b5952-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
