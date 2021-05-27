---
title: 製品推奨事項の有効化
description: このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 873266405638cd277eb748ad7e966ba8a4976b13
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019862"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="47f05-103">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="47f05-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47f05-104">このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="47f05-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="47f05-105">製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="47f05-106">推奨事項のプレチェック</span><span class="sxs-lookup"><span data-stu-id="47f05-106">Recommendations pre-check</span></span>

<span data-ttu-id="47f05-107">有効にする前に、製品の推奨事項は、Azure Data Lake Storage を使用するようにストレージを移行した Commerce の顧客に対してのみサポートされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="47f05-108">推奨事項を有効にするには、次のコンフィギュレーションをバック オフィスで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47f05-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="47f05-109">Azure Data Lake Storage が購入され、環境内で正常に検証されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="47f05-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="47f05-110">詳細については、[Azure Data Lake Storage が購入され、環境内で正常に検証されていることを確認する](enable-ADLS-environment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="47f05-111">エンティティ格納の更新が自動化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="47f05-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="47f05-112">詳細については、[エンティティ格納の更新が自動化されていることを確認する](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="47f05-113">Azure AD ID コンフィギュレーションに推奨事項のエントリが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="47f05-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="47f05-114">このアクションを実行する方法の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="47f05-115">さらに、RetailSale の測定が有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="47f05-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="47f05-116">この設定プロセスの詳細については、[測定の使用](/dynamics365/ai/customer-insights/pm-measures) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-116">To learn more about this set up process, see [Work with measures](/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="47f05-117">Azure AD ID コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="47f05-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="47f05-118">この手順は、サービス (IaaS) コンフィギュレーションとしてのインフラストラクチャを実行するすべての顧客に必要です。</span><span class="sxs-lookup"><span data-stu-id="47f05-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="47f05-119">Service Fabric (SF) で実行している顧客については、この手順が自動的に行われ、設定が予想どおりに構成されていることを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="47f05-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="47f05-120">セットアップ</span><span class="sxs-lookup"><span data-stu-id="47f05-120">Setup</span></span>

1. <span data-ttu-id="47f05-121">バック オフィスから、**Azure Active Directory アプリケーション** ページを検索します。</span><span class="sxs-lookup"><span data-stu-id="47f05-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="47f05-122">"RecommendationSystemApplication-1" のエントリが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="47f05-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="47f05-123">エントリが存在しない場合は、次の情報を含む新しいエントリを追加します:</span><span class="sxs-lookup"><span data-stu-id="47f05-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="47f05-124">**クライアント ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="47f05-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="47f05-125">**名前** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="47f05-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="47f05-126">**ユーザー ID** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="47f05-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="47f05-127">ページを保存して閉じる。</span><span class="sxs-lookup"><span data-stu-id="47f05-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="47f05-128">推奨事項を有効にする</span><span class="sxs-lookup"><span data-stu-id="47f05-128">Turn on recommendations</span></span>

<span data-ttu-id="47f05-129">製品推奨事項を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="47f05-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="47f05-130">Commerce Headquarters で、**機能管理** を検索します。</span><span class="sxs-lookup"><span data-stu-id="47f05-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="47f05-131">**すべて** を選択して、使用可能な機能の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="47f05-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="47f05-132">検索ボックスに、**推奨事項** を入力します。</span><span class="sxs-lookup"><span data-stu-id="47f05-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="47f05-133">**製品推奨事項** 機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="47f05-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="47f05-134">**製品推奨事項** プロパティ ペインで、**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47f05-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![推奨事項の有効化](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="47f05-136">この手順では、製品推奨リストを生成するプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="47f05-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="47f05-137">リストが有効になり、販売時点管理 (POS) または Dynamics 365 Commerce で表示できるようになるまでに、数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="47f05-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="47f05-138">推奨リスト パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="47f05-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="47f05-139">既定では、AI-ML ベースの製品推奨リストは推奨値を提供します。</span><span class="sxs-lookup"><span data-stu-id="47f05-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="47f05-140">業務の流れに合わせて、既定の推奨値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="47f05-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="47f05-141">既定のパラメーターを変更する方法の詳細については、[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="47f05-142">POS デバイスの推奨事項を表示する</span><span class="sxs-lookup"><span data-stu-id="47f05-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="47f05-143">Commerce バック オフィスで推奨事項を有効にした後、レイアウト ツールを使用して、推奨事項パネルをコントロール POS 画面に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47f05-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="47f05-144">このプロセスの詳細については、[POS デバイスのトランザクション画面への推奨設定コントロールの追加](add-recommendations-control-pos-screen.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="47f05-145">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="47f05-145">Enable personalized recommendations</span></span>

<span data-ttu-id="47f05-146">Dynamics 365 Commerce では、小売業者がパーソナライズされた製品推奨事項 (個人用設定とも呼ばれます) を使用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="47f05-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="47f05-147">この方法で、カスタマイズされた推奨事項をオンラインの顧客エクスペリエンスおよび販売時点管理に組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="47f05-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="47f05-148">個人用設定機能をオンにすると、システムはユーザーの購入情報と製品情報を関連付けて、個別の製品推奨事項を生成できます。</span><span class="sxs-lookup"><span data-stu-id="47f05-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="47f05-149">カスタマイズされた推奨事項の詳細については、[カスタマイズされた推奨事項の有効化](personalized-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47f05-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47f05-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="47f05-150">Additional resources</span></span>

[<span data-ttu-id="47f05-151">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="47f05-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="47f05-152">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="47f05-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="47f05-153">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="47f05-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="47f05-154">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="47f05-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="47f05-155">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="47f05-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="47f05-156">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="47f05-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="47f05-157">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="47f05-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="47f05-158">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="47f05-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="47f05-159">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="47f05-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="47f05-160">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="47f05-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="47f05-161">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="47f05-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]