---
title: AI-ML ベースの製品推奨事項結果の調整
description: このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品勧告の結果を調整する方法について説明します。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9e370faed7feb0640959a9fcc4b608f18f9ffc1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263949"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="307fe-103">AI-ML ベースの製品推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="307fe-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="307fe-104">このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品推奨事項の結果を調整する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="307fe-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="307fe-105">製品の推奨設定を有効にすると、既定の設定が有効になります。これらのパラメーターは、多くのニーズに対して機能する場合があります。</span><span class="sxs-lookup"><span data-stu-id="307fe-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="307fe-106">結果が製品の販売活動に適合しているかどうかを、評価するための計画を立てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="307fe-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="307fe-107">再テストの前に、必要に応じてパラメーターを変更する前に、数日間結果を評価することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="307fe-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="307fe-108">推奨リスト パラメーターの理解</span><span class="sxs-lookup"><span data-stu-id="307fe-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="307fe-109">パラメーターを変更する前に、それらが以下の結果にどのように影響するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="307fe-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="307fe-110">「トレンド」製品リスト</span><span class="sxs-lookup"><span data-stu-id="307fe-110">"Trending" product list</span></span>

<span data-ttu-id="307fe-111">「トレンド」製品リストには、変更可能なパラメーターが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="307fe-111">The "Trending" product list has two parameters that can be changed:</span></span>

![「トレンド」リストの既定パラメーターの例](./media/exampletrendingparameters.png)

1. <span data-ttu-id="307fe-113">**過去 X 日間の新製品を含める** - 現在の日付を使用して製品候補を選択できるようになるまで、指定した日数以内に追加された製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="307fe-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="307fe-114">写真の既定値では、古いものから 180 日以内の製品はトレンド製品リストで使用されることが示されています。</span><span class="sxs-lookup"><span data-stu-id="307fe-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="307fe-115">**過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。</span><span class="sxs-lookup"><span data-stu-id="307fe-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="307fe-116">この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、トレンド製品リストでの製品の配置を決定するために使れることが提案されます。</span><span class="sxs-lookup"><span data-stu-id="307fe-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="307fe-117">「ベスト セラー」製品リスト</span><span class="sxs-lookup"><span data-stu-id="307fe-117">"Best selling" product list</span></span>

<span data-ttu-id="307fe-118">ビジネスに応じて、「ベスト セラー」リストは、トランザクション データを使用して製品を注文する場合でも、トレンドとは異なる結果をもたらします。</span><span class="sxs-lookup"><span data-stu-id="307fe-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="307fe-119">ベスト セラーは、品揃えの日付に基づいて中断しないのでまだ非常に人気があり、古い製品はトレンド リストから削除されている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="307fe-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="307fe-120">「ベスト セラー」製品リストには、変更可能なパラメーターが 1 つあります。</span><span class="sxs-lookup"><span data-stu-id="307fe-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![ベスト セラー リストの既定パラメーターの例](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="307fe-122">**過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。</span><span class="sxs-lookup"><span data-stu-id="307fe-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="307fe-123">この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、ベスト セラー製品リストでの製品の配置を決定するために使れることが提案されます。</span><span class="sxs-lookup"><span data-stu-id="307fe-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="307fe-124">推奨リストからの製品を手動で追加または削除</span><span class="sxs-lookup"><span data-stu-id="307fe-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="307fe-125">「新規」、「トレンド」、または「ベスト セラー」リスト用</span><span class="sxs-lookup"><span data-stu-id="307fe-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="307fe-126">**Retail と Commerce** > **製品推奨事項** > **推奨パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="307fe-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="307fe-127">共有パラメーターのリストで、**推奨リスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="307fe-128">リストの追加または製品をリストから削除を選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="307fe-129">テーブルに製品を追加するには、**行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="307fe-130">製品列で、**名前** または **製品番号** で製品を検索します。</span><span class="sxs-lookup"><span data-stu-id="307fe-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![新しい製品リストでの製品の検索例](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="307fe-132">行タイプ列で、次の 2 つのオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="307fe-133">**含める**: 製品をリストの先頭に強制的に追加</span><span class="sxs-lookup"><span data-stu-id="307fe-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="307fe-134">**除外** - リストに表示される製品を削除</span><span class="sxs-lookup"><span data-stu-id="307fe-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![新しい製品リストに製品を含めるまたは除外する例](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="307fe-136">**表示順序** を変更して、**含める** とマークされた製品がリストに表示される順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="307fe-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="307fe-137">2 つの製品が同じ **表示順序** の値を持つ場合、これら 2 つの結果の最終的な順序は、バック オフィスとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="307fe-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="307fe-138">テーブルから製品を削除するには: 削除する行を選び、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="307fe-139">「人気製品」「よく一緒に購入される」リスト用</span><span class="sxs-lookup"><span data-stu-id="307fe-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="307fe-140">「よく一緒に購入される」または「人気製品」リストのコンテキストでは、機械学習を使用してコンシューマー向け購入パターンを分析し、固有のシード製品に対して共通に購入した関連製品を推奨することができます。</span><span class="sxs-lookup"><span data-stu-id="307fe-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="307fe-141">*シード製品* とは、結果を生成する製品です。</span><span class="sxs-lookup"><span data-stu-id="307fe-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="307fe-142">推奨リストを手動で調整するコンテキストでは、この製品の結果を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="307fe-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="307fe-143">シード製品の結果を手動で追加または削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="307fe-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="307fe-144">**シード製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="307fe-145">**製品** 列の下で、**名前** または **製品番号** で製品を検索します。
![よく一緒に購入したリストで製品検索の例](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="307fe-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="307fe-146">**行タイプ** 列で、次の 2 つのオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="307fe-147">**含める**: 製品をリストの先頭に強制的に追加</span><span class="sxs-lookup"><span data-stu-id="307fe-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="307fe-148">**除外** - リストに表示される製品を削除</span><span class="sxs-lookup"><span data-stu-id="307fe-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="307fe-149">![よく一緒に購入したリストの製品を含める、または除外する例](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="307fe-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="307fe-150">テーブルから製品を削除するには: 削除する行を選び、削除を選択します。</span><span class="sxs-lookup"><span data-stu-id="307fe-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="307fe-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="307fe-151">Additional resources</span></span>

[<span data-ttu-id="307fe-152">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="307fe-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="307fe-153">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="307fe-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="307fe-154">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="307fe-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="307fe-155">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="307fe-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="307fe-156">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="307fe-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="307fe-157">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="307fe-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="307fe-158">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="307fe-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="307fe-159">トランザクション画面への推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="307fe-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="307fe-160">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="307fe-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="307fe-161">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="307fe-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="307fe-162">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="307fe-162">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]