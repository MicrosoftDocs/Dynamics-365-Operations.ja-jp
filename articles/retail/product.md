---
title: POS の製品推奨事項
description: このトピックでは、POS (販売時点管理) デバイスでの製品推奨事項の使用について説明します。
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278386"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="6c65f-103">POS の製品推奨事項</span><span class="sxs-lookup"><span data-stu-id="6c65f-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c65f-104">製品の推奨事項は、本質的に、すべての小売スペースにまたがる変形力のあるビジネス アプリケーションであり、リッチで魅力的な、カスタマイズされた製品検索エクスペリエンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-104">At its core, product Recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="6c65f-105">POS にこの機能を実装するには、[POS デバイスに推奨事項を追加する方法](add-recommendations-control-pos-screen.md)の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="6c65f-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="6c65f-106">製品推奨機能の詳細については、[製品推奨事項の概要](../commerce/product-recommendations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c65f-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="6c65f-107">シナリオ</span><span class="sxs-lookup"><span data-stu-id="6c65f-107">Scenarios</span></span>

<span data-ttu-id="6c65f-108">製品推奨事項は、以下の POS シナリオで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6c65f-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="6c65f-109">これらは、Cloud POS または Modern POS (MPOS) で利用できます。</span><span class="sxs-lookup"><span data-stu-id="6c65f-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="6c65f-110">**製品の詳細** ページ:</span><span class="sxs-lookup"><span data-stu-id="6c65f-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="6c65f-111">• 店舗スタッフが、異なるチャネル間で以前のトランザクションを調べるときに**製品の詳細** ページを参照する場合、推薦サービスは、一緒に購入される可能性が高い追加アイテムを提案します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-111">• If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="6c65f-112">[![製品詳細ページの推奨事項](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="6c65f-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="6c65f-113">**トランザクション** ページ:</span><span class="sxs-lookup"><span data-stu-id="6c65f-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="6c65f-114">• 推奨エンジンは、一緒に頻繁に購入されるバスケット内の品目の一覧全体に基づいて、品目を提案します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-114">• The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c65f-115">**トランザクション** ページに推奨事項を表示するには、小売業者は Dynamics 365 for Retail の画面レイアウトを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c65f-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="6c65f-116">**推奨事項** コントロールは、**トランザクション** ページにドロップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c65f-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="6c65f-117">[![トランザクション ページの推奨事項](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="6c65f-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a><span data-ttu-id="6c65f-118">Dynamics 365 Retail をコンフィギュレーションして POS 推奨事項を有効化する</span><span class="sxs-lookup"><span data-stu-id="6c65f-118">Configure Dynamics 365 Retail to enable POS recommendations</span></span>

<span data-ttu-id="6c65f-119">製品推奨事項を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="6c65f-120">サービスが **10.0.6 ビルド**に更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="6c65f-121">ビジネスで[製品推奨事項を有効化する](../commerce/enable-product-recommendations.md)の指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="6c65f-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="6c65f-122">オプション: トランザクション画面に推奨事項を表示するには、**画面レイアウト** に移動して画面レイアウトを選択し、**画面レイアウト デザイナー** を起動し、必要に応じて **レコメンデーション** コントロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="6c65f-123">**小売パラメーター** に移動し、**機械学習** を選択し、**POS 推奨事項の有効化** で **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-123">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="6c65f-124">POS に関する推奨事項を表示するには、グローバル構成ジョブ **1110** を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="6c65f-125">POS 画面レイアウト設計者の変更を反映するには、チャネル構成ジョブ **1070** を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="6c65f-126">[製品推奨事項] が既に有効な場合の問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="6c65f-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="6c65f-127">**小売パラメーター** \> **推奨事項リスト** \> **製品推奨事項の無効化**に移動し、**グローバル構成ジョブ \[9999\]** を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c65f-127">Navigate to **Retail Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="6c65f-128">**画面レイアウト デザイナー** を使用して **推奨事項コントロール** をトランザクション画面に追加した場合、それも削除してください。</span><span class="sxs-lookup"><span data-stu-id="6c65f-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="6c65f-129">他にご質問がある場合は、[推奨事項に関するよく寄せられる質問](../commerce/faq-recommendations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c65f-129">If you have additional questions, check out the [Recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c65f-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6c65f-130">Additional resources</span></span>

<span data-ttu-id="6c65f-131">[POS デバイスのトランザクション ページに推奨事項コントロールを追加する](add-recommendations-control-pos-screen.md)
[製品推奨事項の概要](../commerce/product-recommendations.md)
[製品推奨事項の有効化](../commerce/enable-product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="6c65f-131">[Add a recommendations control to the transaction page on a POS device](add-recommendations-control-pos-screen.md)
[Product recommendations overview](../commerce/product-recommendations.md)
[Enable product recommendations](../commerce/enable-product-recommendations.md)</span></span> 
