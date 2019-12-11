---
title: AI-ML ベースの製品推奨事項結果の管理
description: このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品勧告の結果を調整する方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770073"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="45f3b-103">AI-ML ベースの製品推奨事項結果の管理</span><span class="sxs-lookup"><span data-stu-id="45f3b-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="45f3b-104">このトピックでは、人為的知能の機械学習 (AI-ML) に基づいて製品勧告の結果を調整する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="45f3b-105">製品の推奨設定を有効にすると、既定の設定が有効になります。これらのパラメーターは、多くのニーズに対して機能する場合があります。</span><span class="sxs-lookup"><span data-stu-id="45f3b-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="45f3b-106">結果が製品の販売活動に適合しているかどうかを、評価するための計画を立てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="45f3b-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="45f3b-107">再テストの前に、必要に応じてパラメーターを変更する前に、数日間結果を評価することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="45f3b-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="45f3b-108">推奨リスト パラメーターの理解</span><span class="sxs-lookup"><span data-stu-id="45f3b-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="45f3b-109">パラメーターを変更する前に、それらが以下の結果にどのように影響するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="45f3b-110">トレンド製品リスト</span><span class="sxs-lookup"><span data-stu-id="45f3b-110">Trending product list</span></span>

<span data-ttu-id="45f3b-111">**トレンド**製品リストには、次の 2 つの変更可能なパラメーターがあります: ![たとえば、トレンド リストの既定パラメーター](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="45f3b-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="45f3b-112">**過去 X 日間の新製品を含める** - 現在の日付を使用して製品候補を選択できるようになるまで、指定した日数以内に追加された製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="45f3b-113">写真の既定値では、古いものから 180 日以内の製品はトレンド製品リストで使用されることが示されています。</span><span class="sxs-lookup"><span data-stu-id="45f3b-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="45f3b-114">**過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="45f3b-115">この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、トレンド製品リストでの製品の配置を決定するために使れることが提案されます。</span><span class="sxs-lookup"><span data-stu-id="45f3b-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="45f3b-116">ベスト セラー製品リスト</span><span class="sxs-lookup"><span data-stu-id="45f3b-116">Best selling product list</span></span>

<span data-ttu-id="45f3b-117">ビジネスに応じて、最適の販売は、トランザクション データを使用して製品を注文する場合でも、トレンドとは異なる結果をもたらします。</span><span class="sxs-lookup"><span data-stu-id="45f3b-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="45f3b-118">ベスト セラーは、品揃えの日付に基づいて中断しないのでまだ非常に人気があり、古い製品はトレンド リストから削除されている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="45f3b-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="45f3b-119">**ベスト セラー**製品リストには、変更可能なパラメーターが 1 つあります。</span><span class="sxs-lookup"><span data-stu-id="45f3b-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![ベスト セラー リストの既定パラメーターの例](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="45f3b-121">**過去 X 日間の販売を含める** - 現在の日付を使用して製品を注文できるようになるまで、指定した日数以内に発生した販売取引を表示します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="45f3b-122">この既定値では、過去 30 日以内の製品に対して行われたすべての購買が、ベスト セラー製品リストでの製品の配置を決定するために使れることが提案されます。</span><span class="sxs-lookup"><span data-stu-id="45f3b-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="45f3b-123">推奨リストからの製品を手動で追加または削除</span><span class="sxs-lookup"><span data-stu-id="45f3b-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="45f3b-124">新規、トレンド、またはベスト セラー用</span><span class="sxs-lookup"><span data-stu-id="45f3b-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="45f3b-125">**小売** > **製品推奨事項** > **推奨パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="45f3b-126">小売共有パラメーターのリストでは、**推奨リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="45f3b-127">リストの追加または製品をリストから削除を選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="45f3b-128">テーブルに製品を追加するには、**行の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="45f3b-129">製品列の下で、**名前**または**製品番号**で製品を検索します。
![新規製品リストで製品検索の例](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="45f3b-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="45f3b-130">行タイプ列で、次の 2 つのオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="45f3b-131">**含める**: 製品をリストの先頭に強制的に追加</span><span class="sxs-lookup"><span data-stu-id="45f3b-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="45f3b-132">**除外**: リスト![新規製品リストから製品を含めるまたは除外する例](./media/examplenewlistconfiguration2.png) に表示される製品を削除</span><span class="sxs-lookup"><span data-stu-id="45f3b-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="45f3b-133">**表示順序**を変更して、**含める**とマークされた製品がリストに表示される順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="45f3b-134">2 つの製品が同じ**表示順序**の値を持つ場合、これら 2 つの結果の最終的な順序は、バック オフィスとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="45f3b-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="45f3b-135">テーブルから製品を削除するには: 削除する行を選び、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="45f3b-136">好きな人または頻繁に一緒に購入したリスト</span><span class="sxs-lookup"><span data-stu-id="45f3b-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="45f3b-137">マシン ラーニングを使用して、**よく一緒に購入**または**人気製品**リストのコンテキストで、コンシューマー向け購入パターンを分析し、固有のシード製品に対して共通に購入した関連製品を推奨することができます。</span><span class="sxs-lookup"><span data-stu-id="45f3b-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="45f3b-138">**シード製品**とは、結果を生成する製品です。</span><span class="sxs-lookup"><span data-stu-id="45f3b-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="45f3b-139">推奨リストを手動で調整するコンテキストでは、この製品の結果を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="45f3b-140">シード製品の結果を手動で追加または削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="45f3b-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="45f3b-141">**シード製品**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="45f3b-142">**製品**列の下で、**名前**または**製品番号**で製品を検索します。
![よく一緒に購入したリストで製品検索の例](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="45f3b-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="45f3b-143">**行タイプ**列で、次の 2 つのオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="45f3b-144">**含める**: 製品をリストの先頭に強制的に追加</span><span class="sxs-lookup"><span data-stu-id="45f3b-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="45f3b-145">**除外** - リストに表示される製品を削除</span><span class="sxs-lookup"><span data-stu-id="45f3b-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="45f3b-146">![よく一緒に購入したリストの製品を含める、または除外する例](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="45f3b-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="45f3b-147">テーブルから製品を削除するには: 削除する行を選び、削除を選択します。</span><span class="sxs-lookup"><span data-stu-id="45f3b-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="45f3b-148">追加リソース</span><span class="sxs-lookup"><span data-stu-id="45f3b-148">Additional resources</span></span>

[<span data-ttu-id="45f3b-149">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="45f3b-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="45f3b-150">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="45f3b-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="45f3b-151">ページへの製品推奨リストの追加</span><span class="sxs-lookup"><span data-stu-id="45f3b-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
