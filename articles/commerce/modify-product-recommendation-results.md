---
title: AI-ML ベースの製品推奨事項結果の調整
description: このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品勧告の結果を調整する方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4631ef03e1d73b70d80e774d1efa4909e619bbc0
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127931"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="49386-103">AI-ML ベースの製品推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="49386-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="49386-104">このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品推奨事項の結果を調整する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="49386-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="49386-105">製品の推奨設定を有効にすると、既定の設定が有効になります。これらのパラメーターは、多くのニーズに対して機能する場合があります。</span><span class="sxs-lookup"><span data-stu-id="49386-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="49386-106">結果が製品の販売活動に適合しているかどうかを、評価するための計画を立てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="49386-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="49386-107">再テストの前に、必要に応じてパラメーターを変更する前に、数日間結果を評価することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="49386-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="49386-108">推奨リスト パラメーターの理解</span><span class="sxs-lookup"><span data-stu-id="49386-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="49386-109">パラメーターを変更する前に、それらが以下の結果にどのように影響するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="49386-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="49386-110">「トレンド」製品リスト</span><span class="sxs-lookup"><span data-stu-id="49386-110">"Trending" product list</span></span>

<span data-ttu-id="49386-111">「トレンド」製品リストには、変更可能なパラメーターが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="49386-111">The "Trending" product list has two parameters that can be changed:</span></span>

![「トレンド」リストの既定パラメーターの例](./media/exampletrendingparameters.png)

1. <span data-ttu-id="49386-113">**過去 X 日間の新製品を含める** - 現在の日付を使用して製品候補を選択できるようになるまで、指定した日数以内に追加された製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="49386-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="49386-114">写真の既定値では、古いものから 180 日以内の製品はトレンド製品リストで使用されることが示されています。</span><span class="sxs-lookup"><span data-stu-id="49386-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="49386-115">**過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。</span><span class="sxs-lookup"><span data-stu-id="49386-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="49386-116">この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、トレンド製品リストでの製品の配置を決定するために使れることが提案されます。</span><span class="sxs-lookup"><span data-stu-id="49386-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="49386-117">「ベスト セラー」製品リスト</span><span class="sxs-lookup"><span data-stu-id="49386-117">"Best selling" product list</span></span>

<span data-ttu-id="49386-118">ビジネスに応じて、「ベスト セラー」リストは、トランザクション データを使用して製品を注文する場合でも、トレンドとは異なる結果をもたらします。</span><span class="sxs-lookup"><span data-stu-id="49386-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="49386-119">ベスト セラーは、品揃えの日付に基づいて中断しないのでまだ非常に人気があり、古い製品はトレンド リストから削除されている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="49386-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="49386-120">「ベスト セラー」製品リストには、変更可能なパラメーターが 1 つあります。</span><span class="sxs-lookup"><span data-stu-id="49386-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![ベスト セラー リストの既定パラメーターの例](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="49386-122">**過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。</span><span class="sxs-lookup"><span data-stu-id="49386-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="49386-123">この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、ベスト セラー製品リストでの製品の配置を決定するために使れることが提案されます。</span><span class="sxs-lookup"><span data-stu-id="49386-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="49386-124">推奨リストからの製品を手動で追加または削除</span><span class="sxs-lookup"><span data-stu-id="49386-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="49386-125">「新規」、「トレンド」、または「ベスト セラー」リスト用</span><span class="sxs-lookup"><span data-stu-id="49386-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="49386-126">**Retail と Commerce** > **製品推奨事項** > **推奨パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="49386-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="49386-127">共有パラメーターのリストで、**推奨リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="49386-128">リストの追加または製品をリストから削除を選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="49386-129">テーブルに製品を追加するには、**行の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="49386-130">製品列で、**名前**または**製品番号**で製品を検索します。</span><span class="sxs-lookup"><span data-stu-id="49386-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![新しい製品リストでの製品の検索例](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="49386-132">行タイプ列で、次の 2 つのオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="49386-133">**含める**: 製品をリストの先頭に強制的に追加</span><span class="sxs-lookup"><span data-stu-id="49386-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="49386-134">**除外** - リストに表示される製品を削除</span><span class="sxs-lookup"><span data-stu-id="49386-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![新しい製品リストに製品を含めるまたは除外する例](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="49386-136">**表示順序**を変更して、**含める**とマークされた製品がリストに表示される順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="49386-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="49386-137">2 つの製品が同じ**表示順序**の値を持つ場合、これら 2 つの結果の最終的な順序は、バック オフィスとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="49386-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="49386-138">テーブルから製品を削除するには: 削除する行を選び、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="49386-139">「人気製品」「よく一緒に購入される」リスト用</span><span class="sxs-lookup"><span data-stu-id="49386-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="49386-140">「よく一緒に購入される」または「人気製品」リストのコンテキストでは、機械学習を使用してコンシューマー向け購入パターンを分析し、固有のシード製品に対して共通に購入した関連製品を推奨することができます。</span><span class="sxs-lookup"><span data-stu-id="49386-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="49386-141">*シード製品*とは、結果を生成する製品です。</span><span class="sxs-lookup"><span data-stu-id="49386-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="49386-142">推奨リストを手動で調整するコンテキストでは、この製品の結果を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="49386-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="49386-143">シード製品の結果を手動で追加または削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="49386-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="49386-144">**シード製品**を選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="49386-145">**製品**列の下で、**名前**または**製品番号**で製品を検索します。
![よく一緒に購入したリストで製品検索の例](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="49386-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="49386-146">**行タイプ**列で、次の 2 つのオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="49386-147">**含める**: 製品をリストの先頭に強制的に追加</span><span class="sxs-lookup"><span data-stu-id="49386-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="49386-148">**除外** - リストに表示される製品を削除</span><span class="sxs-lookup"><span data-stu-id="49386-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="49386-149">![よく一緒に購入したリストの製品を含める、または除外する例](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="49386-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="49386-150">テーブルから製品を削除するには: 削除する行を選び、削除を選択します。</span><span class="sxs-lookup"><span data-stu-id="49386-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="49386-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="49386-151">Additional resources</span></span>

[<span data-ttu-id="49386-152">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="49386-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="49386-153">Dynamics 365 Commerce 環境での ADLS の有効化</span><span class="sxs-lookup"><span data-stu-id="49386-153">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="49386-154">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="49386-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="49386-155">カスタマイズされた推奨事項を有効にする</span><span class="sxs-lookup"><span data-stu-id="49386-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="49386-156">カスタマイズされた製品推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="49386-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="49386-157">E コマース サイトへの推奨リストの追加</span><span class="sxs-lookup"><span data-stu-id="49386-157">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="49386-158">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="49386-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="49386-159">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="49386-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="49386-160">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="49386-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="49386-161">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="49386-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="49386-162">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="49386-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
