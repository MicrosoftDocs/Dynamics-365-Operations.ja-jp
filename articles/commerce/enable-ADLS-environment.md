---
title: Dynamics 365 Commerce 環境での ADLS の有効化
description: このトピックでは、Dynamics 365 Commerce 環境に対して、製品推奨事項を有効にする前提条件である Azure Data Lake Storage (ADLS) を有効化し、テストする方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553e1512ba72559923403eef741ce08222172a09
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127770"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="c5edf-103">Dynamics 365 Commerce 環境での ADLS の有効化</span><span class="sxs-lookup"><span data-stu-id="c5edf-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5edf-104">このトピックでは、Dynamics 365 Commerce 環境に対して、製品推奨事項を有効にする前提条件である Azure Data Lake Storage (ADLS) を有効化し、テストする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="c5edf-105">概要</span><span class="sxs-lookup"><span data-stu-id="c5edf-105">Overview</span></span>

<span data-ttu-id="c5edf-106">Dynamics 365 Commerce ソリューションにおいて、すべての製品およびトランザクションの情報は環境のエンティティ格納で追跡されます。</span><span class="sxs-lookup"><span data-stu-id="c5edf-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="c5edf-107">このデータを、データ分析、ビジネス インテリジェンス、パーソナライズされた推奨事項などの他の Dynamics 365 サービスからアクセスできるようにするには、顧客所有の Azure Data Lake Storage Gen 2 (ADLS) ソリューションに環境を接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5edf-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="c5edf-108">ADLS が環境でコンフィギュレーションされている場合、まだ保護が行われていて、顧客のコントロール下にある間、すべての必要なデータはエンティティ格納からミラーリングされます。</span><span class="sxs-lookup"><span data-stu-id="c5edf-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="c5edf-109">製品の推奨事項または個人用設定の推奨事項が環境でも有効になっている場合、製品の推奨事項スタックに ADLS の専用フォルダーへのアクセス許可が付与され、顧客のデータを取得し、それに基づいた推奨事項を計算することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="c5edf-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c5edf-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="c5edf-110">Prerequisites</span></span>

<span data-ttu-id="c5edf-111">顧客は、所有する Azure サブスクリプションで ADLS をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5edf-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="c5edf-112">このトピックでは、Azure サブスクリプションの購入または ADLS が有効なストレージ アカウントの設定については扱いません。</span><span class="sxs-lookup"><span data-stu-id="c5edf-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="c5edf-113">ADLS の詳細については、[ADLS 公式ドキュメント](https://azure.microsoft.com/pricing/details/storage/data-lake) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5edf-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="c5edf-114">コンフィギュレーションの手順</span><span class="sxs-lookup"><span data-stu-id="c5edf-114">Configuration steps</span></span>

<span data-ttu-id="c5edf-115">このセクションでは、環境で ADLS を有効にするために必要なコンフィギュレーション手順について扱います。</span><span class="sxs-lookup"><span data-stu-id="c5edf-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="c5edf-116">環境での ADLS の有効化</span><span class="sxs-lookup"><span data-stu-id="c5edf-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="c5edf-117">環境のバック オフィス ポータルにログインします。</span><span class="sxs-lookup"><span data-stu-id="c5edf-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="c5edf-118">**システム パラメーター**を検索し、**データ接続**タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="c5edf-119">**Data Lake 統合の有効化**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="c5edf-120">**Data Lake のトリクル更新**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="c5edf-121">次に、次の必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="c5edf-122">**アプリケーション ID** // **アプリケーション シークレット** // **DNS 名** - ADLS シークレットが保存されている KeyVault に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5edf-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="c5edf-123">**シークレット名** - KeyVault に格納されていて、ADLS の認証に使用されるシークレット名。</span><span class="sxs-lookup"><span data-stu-id="c5edf-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="c5edf-124">ページ左上隅の変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="c5edf-125">次の図は、ADLS コンフィギュレーションの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c5edf-125">The following image shows an example ADLS configuration.</span></span>

![ADLS コンフィギュレーションの例](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="c5edf-127">ADLS 接続のテスト</span><span class="sxs-lookup"><span data-stu-id="c5edf-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="c5edf-128">**Azure Key Vault のテスト**のリンクを使用して KeyVault への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="c5edf-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="c5edf-129">**Azure Storage のテスト**のリンクを使用して ADLS への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="c5edf-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="c5edf-130">テストに失敗した場合、上記の手順で追加した KeyVault 情報がすべて正しいことを確認してから、再試行してください。</span><span class="sxs-lookup"><span data-stu-id="c5edf-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="c5edf-131">接続テストが成功したら、エンティティ格納の自動更新を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5edf-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="c5edf-132">エンティティ格納の自動更新を有効にするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c5edf-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="c5edf-133">**エンティティ格納**を検索します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="c5edf-134">左のリストで、**RetailSales** エントリに移動し、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="c5edf-135">**自動更新の有効化**が**はい**に設定されていることを確認してから**更新**を選択し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5edf-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="c5edf-136">次の図は、自動更新が有効になっているエンティティ格納の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c5edf-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![自動更新が有効になっているエンティティ格納の例](./media/exampleADLSConfig2.png)

<span data-ttu-id="c5edf-138">環境に対して ADLS がコンフィギュレーションされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c5edf-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="c5edf-139">まだ完了していない場合、環境に対する [製品推奨事項および個人用設定の有効化](enable-product-recommendations.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c5edf-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5edf-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c5edf-140">Additional resources</span></span>

[<span data-ttu-id="c5edf-141">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="c5edf-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c5edf-142">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="c5edf-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c5edf-143">カスタマイズされた推奨事項を有効にする</span><span class="sxs-lookup"><span data-stu-id="c5edf-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="c5edf-144">カスタマイズされた製品推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="c5edf-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="c5edf-145">E コマース サイトへの推奨リストの追加</span><span class="sxs-lookup"><span data-stu-id="c5edf-145">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="c5edf-146">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="c5edf-146">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="c5edf-147">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="c5edf-147">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="c5edf-148">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="c5edf-148">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c5edf-149">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="c5edf-149">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c5edf-150">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="c5edf-150">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="c5edf-151">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c5edf-151">Product recommendations FAQ</span></span>](faq-recommendations.md)


