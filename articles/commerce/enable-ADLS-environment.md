---
title: Dynamics 365 Commerce 環境での Azure Data Lake Storage の有効化
description: このトピックでは、Dynamics 365 Commerce 環境に対して、製品推奨事項を有効にする前提条件である Azure Data Lake Storage を有効化し、テストする方法について説明します。
author: bebeale
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61f96dae0643e3383afd91864e4c145f3b5c04c8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792610"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="08ebd-103">Dynamics 365 Commerce 環境での Azure Data Lake Storage の有効化</span><span class="sxs-lookup"><span data-stu-id="08ebd-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08ebd-104">このトピックでは、Dynamics 365 Commerce 環境に対して、製品推奨事項を有効にする前提条件である Azure Data Lake Storage を有効化し、テストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="08ebd-105">Dynamics 365 Commerce ソリューションにおいて、すべての製品およびトランザクションの情報は環境のエンティティ格納で追跡されます。</span><span class="sxs-lookup"><span data-stu-id="08ebd-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="08ebd-106">このデータを、データ分析、ビジネス インテリジェンス、パーソナライズされた推奨事項などの他の Dynamics 365 サービスからアクセスできるようにするには、顧客所有の Azure Data Lake Storage Gen 2 ソリューションに環境を接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ebd-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="08ebd-107">Azure Data Lake Storage が環境でコンフィギュレーションされている場合、まだ保護が行われていて、顧客のコントロール下にある間、すべての必要なデータはエンティティ格納からミラーリングされます。</span><span class="sxs-lookup"><span data-stu-id="08ebd-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="08ebd-108">製品の推奨事項または個人用設定の推奨事項が環境でも有効になっている場合、製品の推奨事項スタックに Azure Data Lake Storage の専用フォルダーへのアクセス許可が付与され、顧客のデータを取得し、それに基づいた推奨事項を計算することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="08ebd-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08ebd-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="08ebd-109">Prerequisites</span></span>

<span data-ttu-id="08ebd-110">顧客は、所有する Azure サブスクリプションで Azure Data Lake Storage をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ebd-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="08ebd-111">このトピックでは、Azure サブスクリプションの購入または Azure Data Lake Storage が有効なストレージ アカウントの設定については扱いません。</span><span class="sxs-lookup"><span data-stu-id="08ebd-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="08ebd-112">Azure Data Lake Storage の詳細については、[Azure Data Lake Storage Gen2 公式ドキュメント](https://azure.microsoft.com/pricing/details/storage/data-lake) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08ebd-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="08ebd-113">コンフィギュレーションの手順</span><span class="sxs-lookup"><span data-stu-id="08ebd-113">Configuration steps</span></span>

<span data-ttu-id="08ebd-114">このセクションでは、製品の推奨事項に関連する環境で Azure Data Lake Storage を有効にするために必要なコンフィギュレーション手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="08ebd-115">Azure Data Lake Storage を有効にするために必要な手順の詳しい概要については、[エンティティ格納を Data Lake として使用可能にする](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08ebd-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="08ebd-116">環境での Azure Data Lake Storage の有効化</span><span class="sxs-lookup"><span data-stu-id="08ebd-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="08ebd-117">環境のバック オフィス ポータルにログインします。</span><span class="sxs-lookup"><span data-stu-id="08ebd-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="08ebd-118">**システム パラメーター** を検索し、**データ接続** タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="08ebd-119">**Data Lake 統合の有効化** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="08ebd-120">**Data Lake のトリクル更新** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="08ebd-121">次に、次の必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="08ebd-122">**アプリケーション ID** // **アプリケーション シークレット** // **DNS 名** - Azure Data Lake Storage シークレットが保存されている KeyVault に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ebd-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="08ebd-123">**シークレット名** - KeyVault に格納されていて、Azure Data Lake Storage の認証に使用されるシークレット名。</span><span class="sxs-lookup"><span data-stu-id="08ebd-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="08ebd-124">ページ左上隅の変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="08ebd-125">次の図は、Azure Data Lake Storage コンフィギュレーションの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="08ebd-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Azure Data Lake Storage コンフィギュレーションの例](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="08ebd-127">Azure Data Lake Storage 接続のテスト</span><span class="sxs-lookup"><span data-stu-id="08ebd-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="08ebd-128">**Azure Key Vault のテスト** のリンクを使用して KeyVault への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="08ebd-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="08ebd-129">**Azure Storage のテスト** のリンクを使用して Azure Data Lake Storage への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="08ebd-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="08ebd-130">テストに失敗した場合、上記の手順で追加した KeyVault 情報がすべて正しいことを確認してから、再試行してください。</span><span class="sxs-lookup"><span data-stu-id="08ebd-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="08ebd-131">接続テストが成功したら、エンティティ格納の自動更新を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ebd-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="08ebd-132">エンティティ格納の自動更新を有効にするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="08ebd-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="08ebd-133">**エンティティ格納** を検索します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="08ebd-134">左のリストで、**RetailSales** エントリに移動し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="08ebd-135">**自動更新の有効化** が **はい** に設定されていることを確認してから **更新** を選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08ebd-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="08ebd-136">次の図は、自動更新が有効になっているエンティティ格納の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="08ebd-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![自動更新が有効になっているエンティティ格納の例](./media/exampleADLSConfig2.png)

<span data-ttu-id="08ebd-138">Azure Data Lake Storage が環境に対してコンフィギュレーションされました。</span><span class="sxs-lookup"><span data-stu-id="08ebd-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="08ebd-139">まだ完了していない場合、環境に対する [製品推奨事項および個人用設定の有効化](enable-product-recommendations.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="08ebd-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08ebd-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="08ebd-140">Additional resources</span></span>

[<span data-ttu-id="08ebd-141">エンティティ格納を Data Lake として使用可能にする</span><span class="sxs-lookup"><span data-stu-id="08ebd-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="08ebd-142">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="08ebd-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="08ebd-143">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="08ebd-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="08ebd-144">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="08ebd-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="08ebd-145">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="08ebd-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="08ebd-146">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="08ebd-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="08ebd-147">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="08ebd-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="08ebd-148">トランザクション画面への推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="08ebd-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="08ebd-149">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="08ebd-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="08ebd-150">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="08ebd-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="08ebd-151">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="08ebd-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="08ebd-152">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="08ebd-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
