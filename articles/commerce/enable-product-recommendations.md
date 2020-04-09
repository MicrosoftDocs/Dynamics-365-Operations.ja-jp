---
title: 製品推奨事項の有効化
description: このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154416"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="b0375-103">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="b0375-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0375-104">このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0375-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="b0375-105">製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0375-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="b0375-106">推奨事項のプレチェック</span><span class="sxs-lookup"><span data-stu-id="b0375-106">Recommendations pre-check</span></span>

<span data-ttu-id="b0375-107">有効にする前に、製品の推奨事項は、Azure Data Lake Storage (ADLS) を使用するようにストレージを移行した Commerce の顧客に対してのみサポートされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b0375-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="b0375-108">ADLS を有効にする手順については、[Dynamics 365 環境で ADLS を有効にする方法](enable-ADLS-environment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0375-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="b0375-109">さらに、RetailSale の測定が有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0375-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="b0375-110">この設定プロセスの詳細については、[こちら](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0375-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="b0375-111">推奨事項を有効にする</span><span class="sxs-lookup"><span data-stu-id="b0375-111">Turn on recommendations</span></span>

<span data-ttu-id="b0375-112">製品推奨事項を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0375-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="b0375-113">**Retail と Commerce &gt; 製品推奨事項 &gt; 推奨パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0375-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="b0375-114">共有パラメーターのリストで、**推奨リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0375-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="b0375-115">**推奨事項を有効にする**のオプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b0375-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![製品推奨事項の有効化](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="b0375-117">この手順では、製品推奨リストを生成するプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="b0375-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="b0375-118">リストが有効になり、販売時点管理 (POS) または Dynamics 365 Commerce で表示できるようになるまでに、最大数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b0375-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="b0375-119">推奨リスト パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b0375-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="b0375-120">既定では、AI-ML ベースの製品推奨リストは推奨値を提供します。</span><span class="sxs-lookup"><span data-stu-id="b0375-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="b0375-121">業務の流れに合わせて、既定の推奨値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="b0375-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="b0375-122">既定のパラメーターを変更する方法の詳細については、[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0375-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="b0375-123">POS デバイスの推奨事項を表示する</span><span class="sxs-lookup"><span data-stu-id="b0375-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="b0375-124">Commerce バック オフィスで推奨事項を有効にした後、レイアウト ツールを使用して、推奨事項パネルをコントロール POS 画面に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0375-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="b0375-125">このプロセスの詳細については、[POS デバイスのトランザクション画面への推奨設定コントロールの追加](add-recommendations-control-pos-screen.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0375-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="b0375-126">パーソナライズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="b0375-126">Enable personalized recommendations</span></span>

<span data-ttu-id="b0375-127">パーソナライズされた推奨事項を受信する方法の詳細については、[パーソナライズされた推奨事項の有効化](personalized-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0375-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0375-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b0375-128">Additional resources</span></span>

[<span data-ttu-id="b0375-129">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="b0375-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b0375-130">Dynamics 365 Commerce 環境での ADLS の有効化</span><span class="sxs-lookup"><span data-stu-id="b0375-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b0375-131">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="b0375-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b0375-132">カスタマイズされた製品推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="b0375-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b0375-133">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="b0375-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b0375-134">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="b0375-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b0375-135">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="b0375-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b0375-136">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="b0375-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b0375-137">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="b0375-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b0375-138">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b0375-138">Product recommendations FAQ</span></span>](faq-recommendations.md)

