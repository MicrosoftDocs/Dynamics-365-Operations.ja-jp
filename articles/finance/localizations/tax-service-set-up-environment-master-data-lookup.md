---
title: マスター データ検索用の環境の設定
description: このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021347"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="a75b2-103">マスター データ検索用の環境の設定</span><span class="sxs-lookup"><span data-stu-id="a75b2-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a75b2-104">このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="a75b2-105">Lifecycle Services (LCS) の Power Platform 統合を設定します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="a75b2-106">詳細については、[Microsoft Power Platform 統合 - アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a75b2-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="a75b2-107">Dynamics 365 Finance および Microsoft Dataverse を設定します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="a75b2-108">詳細については、[ソリューションの入手](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution)および[認証と承認](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a75b2-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="a75b2-109">次のエンティティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-109">Set up the following entities.</span></span> <span data-ttu-id="a75b2-110">詳細については、[仮想エンティティの有効化](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a75b2-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="a75b2-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="a75b2-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-112">CurrencyEntity</span></span>
      - <span data-ttu-id="a75b2-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="a75b2-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="a75b2-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="a75b2-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="a75b2-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="a75b2-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="a75b2-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="a75b2-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="a75b2-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="a75b2-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="a75b2-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="a75b2-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="a75b2-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="a75b2-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="a75b2-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="a75b2-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="a75b2-125">Dynamics 365 Regulatory Configuration Service (RCS) を設定します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="a75b2-126">Microsoft に対するサービス要求を作成して、次の機能のフライティングを有効にします:</span><span class="sxs-lookup"><span data-stu-id="a75b2-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="a75b2-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="a75b2-127">ERCdsFeature</span></span>
      - <span data-ttu-id="a75b2-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="a75b2-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="a75b2-129">**機能管理** ワークスペースに移動し、次の機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a75b2-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="a75b2-130">(プレビュー) 電子申告 Dataverse データ ソース サポート</span><span class="sxs-lookup"><span data-stu-id="a75b2-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="a75b2-131">(プレビュー) 税サービス Dataverse のデータソース サポート</span><span class="sxs-lookup"><span data-stu-id="a75b2-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="a75b2-132">(プレビュー) グローバリゼーション機能</span><span class="sxs-lookup"><span data-stu-id="a75b2-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="a75b2-133">テナント管理者アカウントを使用して RCS にログインします。</span><span class="sxs-lookup"><span data-stu-id="a75b2-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="a75b2-134">**電子申告** > **接続アプリケーション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="a75b2-135">**新規** を選択してレコードを追加し、次のフィールド情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="a75b2-136">**名前** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="a75b2-137">**タイプ** フィールドで、**Dataverse** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="a75b2-138">**アプリケーション** フィールドに、Dataverse URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="a75b2-139">**テナント** フィールドに、テナントを入力します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="a75b2-140">**カスタム URL** フィールドに、Dataverse URL を入力し、"/api/data/v9.1" を追加します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="a75b2-141">**接続の確認** を選択し、接続プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="a75b2-142">[![接続の確認ボタン](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="a75b2-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="a75b2-143">**電子申告** > **税コンフィギュレーション** に移動し、[税コンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2158352)から税コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="a75b2-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="a75b2-144">[![税コンフィギュレーション ページ、税データ モデル ツリー](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="a75b2-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="a75b2-145">**課税対象ドキュメント モデル マッピング** または Microsoft コンフィギュレーションを使用している場合は **Dataverse モデル マッピング** に移動し、**接続アプリケーション** フィールドで、手順 7 で作成したレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="a75b2-146">**モデル マッピングの既定値** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a75b2-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="a75b2-147">[![モデル マッピング ページ](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="a75b2-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
