---
title: 製品推奨事項の有効化
description: このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770142"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="c8b22-103">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="c8b22-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c8b22-104">このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="c8b22-105">製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8b22-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="c8b22-106">推奨事項のプレチェック</span><span class="sxs-lookup"><span data-stu-id="c8b22-106">Recommendations pre-check</span></span>
<span data-ttu-id="c8b22-107">有効にする前に、製品の推奨事項は、ビルド 10.0.6 をサポートし、BDL を使用するようにストレージを移行した F&O の顧客に対してのみサポートされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c8b22-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="c8b22-108">さらに、RetailSale の測定が有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="c8b22-109">この設定プロセスの詳細については、[こちら](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8b22-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="c8b22-110">推奨事項を有効にする</span><span class="sxs-lookup"><span data-stu-id="c8b22-110">Turn on recommendations</span></span>

<span data-ttu-id="c8b22-111">製品推奨事項を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="c8b22-112">**小売** &gt; **製品推奨事項** &gt; **推奨パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="c8b22-113">小売共有パラメーターのリストで、**推奨リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="c8b22-114">**推奨事項を有効にする**のオプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![製品推奨事項の有効化](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="c8b22-116">この手順では、製品推奨リストを生成するプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="c8b22-117">リストが有効になり、販売時点管理 (POS) または Dynamics 365 for Commerce で表示できるようになるまでに、最大数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8b22-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="c8b22-118">推奨リスト パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c8b22-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="c8b22-119">既定では、AI-ML ベースの製品推奨リストは推奨値を提供します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="c8b22-120">業務の流れに合わせて、既定の推奨値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c8b22-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="c8b22-121">既定のパラメーターを変更する方法の詳細については、[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8b22-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="c8b22-122">POS デバイスの推奨事項を表示する</span><span class="sxs-lookup"><span data-stu-id="c8b22-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="c8b22-123">バック オフィスで推奨事項を有効にした後、レイアウト ツールを介して、推奨事項パネルをコントロール POS 画面に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8b22-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="c8b22-124">このプロセスの詳細については、[こちら](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8b22-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c8b22-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c8b22-125">Additional resources</span></span>

[<span data-ttu-id="c8b22-126">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="c8b22-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c8b22-127">ページへの製品推奨リストの追加</span><span class="sxs-lookup"><span data-stu-id="c8b22-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="c8b22-128">POS デバイスへの推奨事項パネルの追加</span><span class="sxs-lookup"><span data-stu-id="c8b22-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


