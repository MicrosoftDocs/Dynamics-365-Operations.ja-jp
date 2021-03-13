---
title: 予測モデルの改善 (プレビュー)
description: このトピックでは、予測モデルのパフォーマンスを向上させるために使用できる機能について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 2bcdea4a2a8f4386b274077cd1e95398fb6fac37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009371"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="f8c1e-103">予測モデルの改善 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f8c1e-104">このトピックでは、予測モデルのパフォーマンスを向上させるために使用できる機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="f8c1e-105">Microsoft Dynamics 365 Finance での  **顧客支払い予測** ワークスペースのモデルの改善を開始します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="f8c1e-106">次に、改善手順が AI Builder で完了します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="f8c1e-107">過去の実績の選択</span><span class="sxs-lookup"><span data-stu-id="f8c1e-107">Select historical outcomes</span></span>

<span data-ttu-id="f8c1e-108">**期限遵守**、**遅延**、**非常に遅い** の 3 つの結果から、請求書に対して可能な 3 つの結果を最初に選択します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="f8c1e-109">3 つの結果をすべて選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-109">All three outcomes should be selected.</span></span> <span data-ttu-id="f8c1e-110">いずれかの結果の選択を解除すると、請求書がトレーニング プロセスからフィルターで除外され、予測の精度が低下します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="f8c1e-111">[![実績の確認](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="f8c1e-112">組織で 2 つの結果しか必要としない場合は、**遅延** と **非常に遅い** のしきい値を 0 (ゼロ) 日に変更します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="f8c1e-113">このようにして、予測を効果的に、**期限遵守** または **遅延** のバイナリ状態に効果的に折りたたむことができ ます。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="f8c1e-114">フィールドの選択</span><span class="sxs-lookup"><span data-stu-id="f8c1e-114">Select fields</span></span>

<span data-ttu-id="f8c1e-115">モデルに含めるフィールドを選択している場合は、Azure data lakeでデータにマッピングされている Microsoft Dataverse テーブルで使用可能なすべてのフィールドが一覧に含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="f8c1e-116">一部のフィールドは選択 **しない** でください。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="f8c1e-117">選択されていないフィールドは、次の 3 つのカテゴリのいずれかに分類されます。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="f8c1e-118">このフィールドは Dataverse テーブルに必要ですが、Data Lake にはこのフィールドのバッキング データがありません。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="f8c1e-119">このフィールドは ID であるため、機械学習機能に対しては意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="f8c1e-120">このフィールドは、予測では使用できない情報を表します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="f8c1e-121">次のセクションでは、請求書エンティティおよび顧客エンティティに使用できるフィールドと、トレーニング対象として選択 **しない** フィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="f8c1e-122">これらの各フィールドに指定されたカテゴリは、上の一覧のカテゴリを参照します。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="f8c1e-123">請求書 Dataverse テーブル</span><span class="sxs-lookup"><span data-stu-id="f8c1e-123">Invoice Dataverse table</span></span>

<span data-ttu-id="f8c1e-124">次の図は、請求書テーブルで使用できるフィールドを示しています。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="f8c1e-125">[![請求書テーブルで使用できるフィールド](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="f8c1e-126">次のフィールドは、トレーニング対象として選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="f8c1e-127">**請求元仕入先** (カテゴリ 2)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="f8c1e-128">**終了済** (カテゴリ 3) – このフィールドは、(決算された) トレーニングと予測 (決算されていない) の請求書をフィルター処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="f8c1e-129">**名前** (カテゴリ 1)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-129">**Name** (category 1)</span></span>
- <span data-ttu-id="f8c1e-130">**ソース ID** (カテゴリ 2)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="f8c1e-131">**ソース レコード** (カテゴリ 2)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="f8c1e-132">**ソース テーブル** (カテゴリ 2)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="f8c1e-133">顧客 Dataverse テーブル</span><span class="sxs-lookup"><span data-stu-id="f8c1e-133">Customer Dataverse table</span></span>

<span data-ttu-id="f8c1e-134">次の図は、顧客テーブルで使用できるフィールドを示しています。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="f8c1e-135">[![顧客テーブルで使用できるフィールド](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="f8c1e-136">次のフィールドは、トレーニング対象として選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="f8c1e-137">**行の固有キー** (カテゴリ 2)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="f8c1e-138">フィルター</span><span class="sxs-lookup"><span data-stu-id="f8c1e-138">Filters</span></span>

<span data-ttu-id="f8c1e-139">現在、フィルターでは顧客支払予測シナリオはサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="f8c1e-140">したがって、**このステップをスキップ** を選択して、概要ページに進みます。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="f8c1e-141">[![フィルターを使用したフォーカス モデル](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="f8c1e-142">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="f8c1e-142">Privacy notice</span></span>
<span data-ttu-id="f8c1e-143">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="f8c1e-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
