---
title: キャッシュ フロー予測の有効化 (プレビュー)
description: このトピックでは、財務インサイトでキャッシュ フロー予測機能を有効にする方法について説明します。
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818731"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="3d989-103">キャッシュ フロー予測の有効化 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3d989-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3d989-104">このトピックでは、財務インサイトでキャッシュ フロー予測機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3d989-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="3d989-105">キャッシュ フローで支払予測を使用するには、[顧客支払予測の有効化](enable-cust-paymnt-prediction.md) で説明されているように、顧客支払予測機能を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d989-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="3d989-106">Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="3d989-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="3d989-107">次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3d989-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="3d989-108">(Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)</span><span class="sxs-lookup"><span data-stu-id="3d989-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="3d989-109">Microsoft Dynamics 365 Finance の配置が Service Fabric 配置である場合は、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="3d989-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="3d989-110">財務インサイト チームは既にフライトを有効にしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d989-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="3d989-111">**機能管理** ワークスペースに機能が表示されない場合や、有効にしようとしたときに問題が発生した場合は、<fiap@microsoft.com> に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="3d989-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="3d989-112">**機能管理** ワークスペースを開き、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="3d989-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="3d989-113">**更新プログラムの確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d989-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="3d989-114">以下の機能を有効にします:</span><span class="sxs-lookup"><span data-stu-id="3d989-114">Turn on the following features:</span></span>

        - <span data-ttu-id="3d989-115">新しいグリッド コントロール</span><span class="sxs-lookup"><span data-stu-id="3d989-115">New grid control</span></span>
        - <span data-ttu-id="3d989-116">グリッド内でのグループ化 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3d989-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="3d989-117">顧客支払予測 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3d989-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="3d989-118">キャッシュ フロー予測 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3d989-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="3d989-119">**現金および銀行管理 \> キャッシュ フロー予測の設定** に移動し、予測に含める流動資産勘定を追加します。</span><span class="sxs-lookup"><span data-stu-id="3d989-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d989-120">流動資産勘定が設定されていない場合は、キャッシュ フローを生成できません。</span><span class="sxs-lookup"><span data-stu-id="3d989-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="3d989-121">**現金および銀行管理 \> 設定 \> 財務インサイト (プレビュー) \> キャッシュ フロー予測** に移動し、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="3d989-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="3d989-122">**キャッシュ フロー予測** タブで、**機能の有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d989-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="3d989-123">**予測モデルの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d989-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="3d989-124">キャッシュ フロー予測機能の詳細については、[キャッシュ フロー予測](cash-flow-forecast-intro.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d989-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="3d989-125">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="3d989-125">Privacy notice</span></span>

<span data-ttu-id="3d989-126">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="3d989-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]