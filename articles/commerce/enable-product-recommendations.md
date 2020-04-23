---
title: 製品推奨事項の有効化
description: このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259797"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="a478c-103">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="a478c-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a478c-104">このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a478c-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="a478c-105">製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="a478c-106">推奨事項のプレチェック</span><span class="sxs-lookup"><span data-stu-id="a478c-106">Recommendations pre-check</span></span>

<span data-ttu-id="a478c-107">有効にする前に、製品の推奨事項は、Azure Data Lake Storage (ADLS) を使用するようにストレージを移行した Commerce の顧客に対してのみサポートされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="a478c-108">推奨事項を有効にするには、次のコンフィギュレーションをバック オフィスで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a478c-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="a478c-109">ADLS が購入され、環境内で正常に検証されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a478c-109">Ensure that ADLS has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="a478c-110">詳細については、[ADLS が購入され、環境内で正常に検証されていることを確認する](enable-ADLS-environment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-110">For more information, see [Ensure that ADLS has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="a478c-111">エンティティ格納の更新が自動化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a478c-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="a478c-112">詳細については、[エンティティ格納の更新が自動化されていることを確認する](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="a478c-113">Azure AD ID コンフィギュレーションに推奨事項のエントリが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a478c-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="a478c-114">このアクションを実行する方法の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="a478c-115">さらに、RetailSale の測定が有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a478c-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="a478c-116">この設定プロセスの詳細については、[測定の使用](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="a478c-117">Azure AD ID コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a478c-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="a478c-118">この手順は、サービス (IaaS) コンフィギュレーションとしてのインフラストラクチャを実行するすべての顧客に必要です。</span><span class="sxs-lookup"><span data-stu-id="a478c-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="a478c-119">Service Fabric (SF) で実行している顧客については、この手順が自動的に行われ、設定が予想どおりに構成されていることを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a478c-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="a478c-120">セットアップ</span><span class="sxs-lookup"><span data-stu-id="a478c-120">Setup</span></span>

1. <span data-ttu-id="a478c-121">バック オフィスから、**Azure Active Directory アプリケーション** ページを検索します。</span><span class="sxs-lookup"><span data-stu-id="a478c-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="a478c-122">"RecommendationSystemApplication-1" のエントリが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a478c-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="a478c-123">エントリが存在しない場合は、次の情報を含む新しいエントリを追加します:</span><span class="sxs-lookup"><span data-stu-id="a478c-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="a478c-124">**クライアント ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="a478c-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="a478c-125">**名前** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="a478c-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="a478c-126">**ユーザー ID** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="a478c-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="a478c-127">ページを保存して閉じる。</span><span class="sxs-lookup"><span data-stu-id="a478c-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="a478c-128">推奨事項を有効にする</span><span class="sxs-lookup"><span data-stu-id="a478c-128">Turn on recommendations</span></span>

<span data-ttu-id="a478c-129">製品推奨事項を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a478c-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="a478c-130">**Retail と Commerce &gt; 製品推奨事項 &gt; 推奨パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a478c-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="a478c-131">共有パラメーターのリストで、**推奨リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a478c-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="a478c-132">**推奨事項を有効にする**のオプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a478c-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![推奨事項の有効化](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="a478c-134">この手順では、製品推奨リストを生成するプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="a478c-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="a478c-135">リストが有効になり、販売時点管理 (POS) または Dynamics 365 Commerce で表示できるようになるまでに、数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a478c-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="a478c-136">推奨リスト パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a478c-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="a478c-137">既定では、AI-ML ベースの製品推奨リストは推奨値を提供します。</span><span class="sxs-lookup"><span data-stu-id="a478c-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="a478c-138">業務の流れに合わせて、既定の推奨値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="a478c-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="a478c-139">既定のパラメーターを変更する方法の詳細については、[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="a478c-140">POS デバイスの推奨事項を表示する</span><span class="sxs-lookup"><span data-stu-id="a478c-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="a478c-141">Commerce バック オフィスで推奨事項を有効にした後、レイアウト ツールを使用して、推奨事項パネルをコントロール POS 画面に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a478c-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="a478c-142">このプロセスの詳細については、[POS デバイスのトランザクション画面への推奨設定コントロールの追加](add-recommendations-control-pos-screen.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="a478c-143">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="a478c-143">Enable personalized recommendations</span></span>

<span data-ttu-id="a478c-144">Dynamics 365 Commerce では、小売業者がパーソナライズされた製品推奨事項 (個人用設定とも呼ばれます) を使用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a478c-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="a478c-145">この方法で、カスタマイズされた推奨事項をオンラインの顧客エクスペリエンスおよび販売時点管理に組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="a478c-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="a478c-146">個人用設定機能をオンにすると、システムはユーザーの購入情報と製品情報を関連付けて、個別の製品推奨事項を生成できます。</span><span class="sxs-lookup"><span data-stu-id="a478c-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="a478c-147">カスタマイズされた推奨事項の詳細については、[カスタマイズされた推奨事項の有効化](personalized-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a478c-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a478c-148">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a478c-148">Additional resources</span></span>

[<span data-ttu-id="a478c-149">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="a478c-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a478c-150">Dynamics 365 Commerce 環境での ADLS の有効化</span><span class="sxs-lookup"><span data-stu-id="a478c-150">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a478c-151">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="a478c-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a478c-152">カスタマイズされた製品推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="a478c-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a478c-153">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="a478c-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a478c-154">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="a478c-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a478c-155">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="a478c-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a478c-156">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="a478c-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a478c-157">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="a478c-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a478c-158">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="a478c-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

