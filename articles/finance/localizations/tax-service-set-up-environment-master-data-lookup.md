---
title: マスター データ検索用の環境の設定
description: このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869079"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="5e41e-103">マスター データ検索用の環境の設定</span><span class="sxs-lookup"><span data-stu-id="5e41e-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="5e41e-104">このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="5e41e-105">Lifecycle Services (LCS) の Power Platform 統合を設定します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="5e41e-106">詳細については、[Microsoft Power Platform 統合 - アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e41e-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="5e41e-107">Dynamics 365 Finance および Microsoft Dataverse を設定します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="5e41e-108">詳細については、[ソリューションの入手](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution)および[認証と承認](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e41e-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="5e41e-109">[税サービス仮想エンティティ](https://go.microsoft.com/fwlink/?linkid=2158160)から *前提条件の税サービス仮想エンティティ ソリューション* をインポートします。</span><span class="sxs-lookup"><span data-stu-id="5e41e-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="5e41e-110">Dynamics 365 Regulatory Configuration Service (RCS) を設定します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="5e41e-111">Microsoft に対するサービス要求を作成して、次の機能のフライティングを有効にします:</span><span class="sxs-lookup"><span data-stu-id="5e41e-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="5e41e-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="5e41e-112">ERCdsFeature</span></span>
      - <span data-ttu-id="5e41e-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="5e41e-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="5e41e-114">Finance で、**機能の管理** ワークスペースに移動し、次の機能を有効にします:</span><span class="sxs-lookup"><span data-stu-id="5e41e-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="5e41e-115">(プレビュー) 電子申告 Dataverse データ ソース サポート</span><span class="sxs-lookup"><span data-stu-id="5e41e-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="5e41e-116">(プレビュー) 税サービス Dataverse のデータソース サポート</span><span class="sxs-lookup"><span data-stu-id="5e41e-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="5e41e-117">(プレビュー) グローバリゼーション機能</span><span class="sxs-lookup"><span data-stu-id="5e41e-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="5e41e-118">テナント管理者アカウントを使用して RCS にログインします。</span><span class="sxs-lookup"><span data-stu-id="5e41e-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="5e41e-119">**電子申告** > **接続アプリケーション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="5e41e-120">**新規** を選択してレコードを追加し、次のフィールド情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="5e41e-121">**名前** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="5e41e-122">**タイプ** フィールドで、**Dataverse** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="5e41e-123">**アプリケーション** フィールドに、Dataverse URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="5e41e-124">**テナント** フィールドに、テナントを入力します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="5e41e-125">**カスタム URL** フィールドに、Dataverse URL を入力し、"/api/data/v9.1" を追加します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="5e41e-126">**接続の確認** を選択し、接続プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="5e41e-127">[![接続の確認ボタン](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="5e41e-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="5e41e-128">**電子申告** > **税コンフィギュレーション** に移動し、[税コンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2158352)から税コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="5e41e-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="5e41e-129">[![税コンフィギュレーション ページ、税データ モデル ツリー](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="5e41e-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="5e41e-130">**課税対象ドキュメント モデル マッピング** または Microsoft コンフィギュレーションを使用している場合は **Dataverse モデル マッピング** に移動し、**接続アプリケーション** フィールドで、手順 7 で作成したレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="5e41e-131">**モデル マッピングの既定値** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5e41e-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="5e41e-132">[![モデル マッピング ページ](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="5e41e-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
