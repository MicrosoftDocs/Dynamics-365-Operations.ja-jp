---
title: 顧客支払予測の有効化 (プレビュー)
description: このトピックでは、財務インサイトで顧客支払予測機能をオンにし構成する方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b8c5fc4a915aa0aba6ff683fac59379f6e319fff
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256814"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="8610a-103">顧客支払予測の有効化 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="8610a-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8610a-104">このトピックでは、財務インサイトで顧客支払予測機能をオンにし構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8610a-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="8610a-105">**機能管理** ワークスペースで機能を有効にし、**財務インサイト パラメーター** ページで構成設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="8610a-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="8610a-106">このトピックには、機能を効果的に使用するために役立つ情報も含まれています。</span><span class="sxs-lookup"><span data-stu-id="8610a-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="8610a-107">次の手順を実行する前に、[財務インサイトの構成](configure-for-fin-insites.md) トピックの前提条件の手順を必ず完了してください。</span><span class="sxs-lookup"><span data-stu-id="8610a-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="8610a-108">Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="8610a-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="8610a-109">次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8610a-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="8610a-110">(Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)</span><span class="sxs-lookup"><span data-stu-id="8610a-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="8610a-111">Microsoft Dynamics 365 Finance の配置が Service Fabric 配置である場合は、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="8610a-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="8610a-112">財務インサイト チームは既にフライトを有効にしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8610a-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="8610a-113">**機能管理** ワークスペースに機能が表示されない場合や、有効にしようとしたときに問題が発生した場合は、<fiap@microsoft.com> に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="8610a-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="8610a-114">顧客支払に関するインサイト機能を有効にします:</span><span class="sxs-lookup"><span data-stu-id="8610a-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="8610a-115">**システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8610a-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="8610a-116">**顧客支払に関するインサイト (プレビュー)** と呼ばれる機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="8610a-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="8610a-117">**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8610a-117">Select **Enable now**.</span></span>

    <span data-ttu-id="8610a-118">これで、顧客支払に関するインサイト機能が有効になり、構成する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="8610a-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="8610a-119">顧客支払に関するインサイト機能を構成します:</span><span class="sxs-lookup"><span data-stu-id="8610a-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="8610a-120">**与信および回収 \> 設定 \> 財務インサイト \> 財務インサイト パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8610a-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="8610a-121">[![機能を構成する前の財務インサイト パラメーター ページ](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="8610a-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="8610a-122">**財務インサイト パラメーター** ページの **顧客支払に関するインサイト** タブで、**予測モデルに使用されるデータ フィールドの表示** リンクを選択して、**予測モデルのデータ フィールド** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8610a-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="8610a-123">ここでは、顧客支払予測に対して人工知能 (AI) 予測モデルを作成するために使用されるフィールドの既定の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="8610a-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="8610a-124">既定のフィールド一覧を使用して予測モデルを作成するには、**予測モデルのデータ フィールド** ページを閉じて、**財務インサイト パラメーター** ページで **機能の有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8610a-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="8610a-125">"かなりの遅延" トランザクション期間を指定して、**かなりの遅延** の予測バケットがビジネスにとって何を意味するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="8610a-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="8610a-126">未処理の請求書ごとに、システムは、以下の 3 つのバケットで支払いの確率を予測します: **期限内**、**遅延**、**かなりの遅延**。</span><span class="sxs-lookup"><span data-stu-id="8610a-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="8610a-127">**期限内** – このバケットには、トランザクションの期日またはそれ以前に支払われると予測される支払が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8610a-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="8610a-128">**遅延** – このバケットには、トランザクション期日後ではあるが、"かなりの遅延" トランザクション期間の開始前に支払われると予測される支払が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8610a-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="8610a-129">**かなりの遅延** – このバケットには、"かなりの遅延" トランザクション期間の開始後に支払われると予測される支払が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8610a-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8610a-130">"かなりの遅延" トランザクション期間を変更し、顧客支払の AI 予測モデルが作成された後に **遅延しきい値の変更** を選択した場合、既存の予測モデルが削除され、新しいモデルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8610a-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="8610a-131">新しい予測モデルは、それを定義するために入力された設定に基づいて、トランザクションを "かなりの遅延" 期間に移動します。</span><span class="sxs-lookup"><span data-stu-id="8610a-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="8610a-132">"かなりの遅延" トランザクション期間の定義が完了したら、**予測モデルの作成** を選択し、予測モデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8610a-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="8610a-133">**財務インサイト パラメーター** ページの **予測モデル** セクションには、予測モデルの状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8610a-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8610a-134">予測モデルの作成中はいつでも、**モデル作成のリセット** を選択して、プロセスを再起動できます。</span><span class="sxs-lookup"><span data-stu-id="8610a-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="8610a-135">これで、機能が構成され、使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="8610a-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="8610a-136">機能を有効にして構成し、予測モデルを作成して実行すると、次の図に示すように、**財務インサイト パラメーター** ページの **予測モデル** セクションにモデルの精度が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8610a-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="8610a-137">[![財務インサイト パラメーター ページの予測モデルの正確性](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="8610a-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="8610a-138">リリースの詳細</span><span class="sxs-lookup"><span data-stu-id="8610a-138">Release details</span></span>

<span data-ttu-id="8610a-139">財務インサイトのパブリック プレビューは、米国、ヨーロッパ、および英国での試用版の展開に使用できます。</span><span class="sxs-lookup"><span data-stu-id="8610a-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="8610a-140">Microsoft は、より多くの地域に対するサポートを段階的に追加しています。</span><span class="sxs-lookup"><span data-stu-id="8610a-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="8610a-141">パブリック プレビュー機能は、Tier-2 のサンドボックス環境でのみ有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8610a-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="8610a-142">サンドボックス環境で作成された設定および AI モデルは、運用環境に移行できません。</span><span class="sxs-lookup"><span data-stu-id="8610a-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="8610a-143">詳細については、[Microsoft Dynamics 365 プレビューの補足の使用条件](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8610a-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="8610a-144">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="8610a-144">Privacy notice</span></span>

<span data-ttu-id="8610a-145">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="8610a-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]