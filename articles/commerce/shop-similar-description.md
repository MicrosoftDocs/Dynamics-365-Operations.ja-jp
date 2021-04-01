---
title: "\"同じような説明を探す\" 推奨事項の有効化"
description: このトピックでは、Microsoft Dynamics 365 Commerce で、"同じような説明を探す" 製品推奨事項を有効にする方法について説明します。
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
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
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234392"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="c4803-103">"同じような説明を探す" 推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="c4803-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c4803-104">このトピックでは、Microsoft Dynamics 365 Commerce で、"同じような説明を探す" 製品推奨事項を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c4803-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c4803-105">Dynamics 365 Commerce の「類似した説明を探す」 のおすすめ候補機能は、人工知能と機械学習 (AI-ML) を使って、顧客が探しているものと似たような記述のある商品を推奨してくれます。</span><span class="sxs-lookup"><span data-stu-id="c4803-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="c4803-106">Commerce のすべての小売チャネルで「類似した説明を探す」のおすすめ候補を利用できるようにすることで、小売業者は顧客が欲しいものを簡単に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="c4803-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="c4803-107">「類似した説明を探す」のおすすめ候補機能は、種子製品の製品名と説明を使用して、小売業者の製品カタログから類似製品を検索して推奨します。</span><span class="sxs-lookup"><span data-stu-id="c4803-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="c4803-108">「類似した説明を探す」 のレコメンドは、販売時点管理 (POS) と eコマースの両方のエクスペリエンスで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="c4803-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="c4803-109">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="c4803-109">Example scenarios</span></span>

<span data-ttu-id="c4803-110">以下のシナリオ例では、「類似した説明を探す」機能が提供できるお推奨タイプを示しています。</span><span class="sxs-lookup"><span data-stu-id="c4803-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="c4803-111">顧客は、レトロスタイルの角縁メガネを見て、小売業者の業界の文脈で、似たようなデザインの他のメガネのおすすめ候補のセットを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="c4803-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="c4803-112">顧客は、以前に小売業者から購入したコーヒーの味を発見するために「類似した説明を探す」のおすすめ候補機能を使用しています。</span><span class="sxs-lookup"><span data-stu-id="c4803-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="c4803-113">「類似した説明を探す」おすすめ候補機能の有効化</span><span class="sxs-lookup"><span data-stu-id="c4803-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="c4803-114">製品の推奨は、ストレージを Azure Data Lake Storage  Gen2 に移行した Commerce ユーザーのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c4803-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c4803-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="c4803-115">Prerequisites</span></span>

<span data-ttu-id="c4803-116">「類似した説明を探す」のおすすめ候補を顧客に表示するには、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4803-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="c4803-117">Commerce 本社での [製品推奨を有効にします](enable-product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="c4803-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="c4803-118">メディア サーバーが HTTPS 呼び出しをサポートしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c4803-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="c4803-119">「おすすめ候補」 おすすめ候補の有効化</span><span class="sxs-lookup"><span data-stu-id="c4803-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="c4803-120">Commerce 本部の「類似した説明を探す」おすすめ候補機能をオンにするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c4803-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c4803-121">**機能管理**  ワークスペースで、利用可能な機能の一覧から、**類似した説明を探す** を検索します。</span><span class="sxs-lookup"><span data-stu-id="c4803-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="c4803-122">右側のペインで、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4803-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="c4803-123">機能をオンにすると、商品のおすすめ候補リストの生成を開始します。</span><span class="sxs-lookup"><span data-stu-id="c4803-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="c4803-124">これらのリストが利用可能になり、オンラインや POS 端末で確認できるようになるまでには、最大で 1 日かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c4803-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="c4803-125">この機能をオフにした場合でも、他のタイプの製品推奨事項には影響されません。</span><span class="sxs-lookup"><span data-stu-id="c4803-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="c4803-126">製品推奨の詳細については、[製品推奨の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4803-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="c4803-127">「類似した説明を探す」ボタンを製品の詳細ページに追加する</span><span class="sxs-lookup"><span data-stu-id="c4803-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="c4803-128">Commerce 本部のおすすめ候補機能 「類似した説明を探す」 をオンにした後、任意の商品詳細ページ (PDP) の購入ボックスに **類似した説明を探す** ボタンを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c4803-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="c4803-129">このボタンを選択した顧客は、視覚的に類似した商品を表示する専用の **類似した説明を探す** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="c4803-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="c4803-130">顧客はセレクターを使用して、製品をさらに詳細にフィルタ処理することができます。</span><span class="sxs-lookup"><span data-stu-id="c4803-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="c4803-131">Commerce サイト ビルダーを使用することで、**類似した説明を探す** ボタンを PDP に追加するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="c4803-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c4803-132">購入ボックス モジュールを含む既存のサイト ビルダー ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c4803-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="c4803-133">左のナビゲーション ウィンドウで、購入ボックスモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4803-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="c4803-134">右側のナビゲーション ペインで、**類似した説明を探すリンク** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="c4803-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="c4803-135">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4803-135">Select **Save**.</span></span>
1. <span data-ttu-id="c4803-136">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="c4803-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="c4803-137">ページの発行後に、PDP には **類似した説明を探すリンク** ボタンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="c4803-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="c4803-138">次の図は、サイト ビルダーの PDP 例上の **類似した説明を探すリンク** チェック ボックスと **類似した説明を探す** ボタンを示しています。</span><span class="sxs-lookup"><span data-stu-id="c4803-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![サイト ビルダーの PDP 上で、[類似した説明を探すリンク] チェック ボックスと [類似した説明を探す] ボタンを有効化します](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="c4803-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c4803-140">Additional resources</span></span>

[<span data-ttu-id="c4803-141">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="c4803-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c4803-142">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="c4803-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="c4803-143">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="c4803-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c4803-144">"同じような商品を探す" 推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="c4803-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="c4803-145">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="c4803-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c4803-146">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="c4803-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c4803-147">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c4803-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]