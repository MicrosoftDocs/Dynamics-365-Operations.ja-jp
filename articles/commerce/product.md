---
title: POS で製品推奨事項を追加する
description: このトピックでは、POS (販売時点管理) デバイスでの製品推奨事項の使用について説明します。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 437913343d16490fd49a458b5c7a17132be293c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230939"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="8edb8-103">POS で製品推奨事項を追加する</span><span class="sxs-lookup"><span data-stu-id="8edb8-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8edb8-104">製品の推奨事項は、本質的に、すべてのコマース スペースにまたがる変形力のあるビジネス アプリケーションであり、リッチで魅力的な、カスタマイズされた製品検索エクスペリエンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="8edb8-105">POS にこの機能を実装するには、[POS デバイスに推奨事項を追加する方法](add-recommendations-control-pos-screen.md)の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="8edb8-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="8edb8-106">製品推奨機能の詳細については、[製品推奨事項の概要](../commerce/product-recommendations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8edb8-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="8edb8-107">シナリオ</span><span class="sxs-lookup"><span data-stu-id="8edb8-107">Scenarios</span></span>

<span data-ttu-id="8edb8-108">製品推奨事項は、以下の POS シナリオで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="8edb8-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="8edb8-109">これらは、Cloud POS または Modern POS (MPOS) で利用できます。</span><span class="sxs-lookup"><span data-stu-id="8edb8-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="8edb8-110">**製品の詳細** ページ:</span><span class="sxs-lookup"><span data-stu-id="8edb8-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="8edb8-111">店舗スタッフが、異なるチャネル間で以前のトランザクションを調べるときに **製品の詳細** ページを参照する場合、推奨サービスは、一緒に購入される可能性が高い追加アイテムを提案します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="8edb8-112">[![製品詳細ページの推奨事項](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="8edb8-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="8edb8-113">**トランザクション** ページ:</span><span class="sxs-lookup"><span data-stu-id="8edb8-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="8edb8-114">推奨エンジンは、一緒に頻繁に購入されるバスケット内の品目の一覧全体に基づいて、品目を提案します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8edb8-115">**トランザクション** ページに推奨事項を表示するには、小売業者は Dynamics 365 Commerce の画面レイアウトを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8edb8-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8edb8-116">**推奨事項** コントロールは、**トランザクション** ページにドロップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8edb8-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="8edb8-117">[![トランザクション ページの推奨事項](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="8edb8-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="8edb8-118">コマースをコンフィギュレーションして POS 推奨事項を有効化する</span><span class="sxs-lookup"><span data-stu-id="8edb8-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="8edb8-119">製品推奨事項を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="8edb8-120">サービスが **10.0.6 ビルド** に更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="8edb8-121">ビジネスで[製品推奨事項を有効化する](../commerce/enable-product-recommendations.md)の指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="8edb8-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="8edb8-122">オプション: トランザクション画面に推奨事項を表示するには、**画面レイアウト** に移動して画面レイアウトを選択し、**画面レイアウト デザイナー** を起動し、必要に応じて **レコメンデーション** コントロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="8edb8-123">**コマース パラメーター** に移動し、**機械学習** を選択し、**POS 推奨事項の有効化** で **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="8edb8-124">POS に関する推奨事項を表示するには、グローバル構成ジョブ **1110** を実行します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="8edb8-125">POS 画面レイアウト設計者の変更を反映するには、チャネル構成ジョブ **1070** を実行します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="8edb8-126">[製品推奨事項] が既に有効な場合の問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="8edb8-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="8edb8-127">**コマース パラメーター** \> **推奨事項リスト** \> **製品推奨事項の無効化** に移動し、**グローバル構成ジョブ \[9999\]** を実行します。</span><span class="sxs-lookup"><span data-stu-id="8edb8-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="8edb8-128">**画面レイアウト デザイナー** を使用して **推奨事項コントロール** をトランザクション画面に追加した場合、それも削除してください。</span><span class="sxs-lookup"><span data-stu-id="8edb8-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="8edb8-129">他にご質問がある場合は、[製品推奨事項に関するよく寄せられる質問](../commerce/faq-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8edb8-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8edb8-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8edb8-130">Additional resources</span></span>

[<span data-ttu-id="8edb8-131">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="8edb8-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8edb8-132">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="8edb8-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="8edb8-133">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="8edb8-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8edb8-134">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="8edb8-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8edb8-135">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="8edb8-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8edb8-136">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="8edb8-136">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="8edb8-137">トランザクション画面への推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="8edb8-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8edb8-138">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="8edb8-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8edb8-139">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="8edb8-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8edb8-140">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="8edb8-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8edb8-141">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="8edb8-141">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]