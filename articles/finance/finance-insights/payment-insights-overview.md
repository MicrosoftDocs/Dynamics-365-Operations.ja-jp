---
title: 顧客支払予測 (プレビュー)
description: このトピックでは、顧客の一般的な支払方法を理解するために役立つ支払インサイト機能について説明します。 この機能を使用すると、コレクション プロセスを開始したとしても、それ以外の状況を把握することができます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
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
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f306f9437b78005d8b8aa11f0b6f210ebdd4fd2a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995068"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="ffe60-104">顧客支払予測 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="ffe60-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ffe60-105">このトピックでは、顧客の一般的な支払方法を理解するために役立つ支払インサイト機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="ffe60-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="ffe60-106">この機能を使用すると、コレクション プロセスを開始したとしても、それ以外の状況を把握することができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="ffe60-107">概要</span><span class="sxs-lookup"><span data-stu-id="ffe60-107">Overview</span></span>

<span data-ttu-id="ffe60-108">多くの場合、組織にとって顧客が請求書に支払を行う時を予測するのは難しいことです。</span><span class="sxs-lookup"><span data-stu-id="ffe60-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="ffe60-109">分析情報が不足していると、次のような問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ffe60-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="ffe60-110">キャッシュフロー予測の正確性の低下</span><span class="sxs-lookup"><span data-stu-id="ffe60-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="ffe60-111">開始が遅すぎる回収プロセス</span><span class="sxs-lookup"><span data-stu-id="ffe60-111">Collections processes that start too late</span></span>
- <span data-ttu-id="ffe60-112">顧客にリリースされる顧客に対して既定で支払を行う可能性のある注文</span><span class="sxs-lookup"><span data-stu-id="ffe60-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="ffe60-113">顧客支払予測 (プレビュー) は、組織が顧客が請求書を支払う時を予測するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="ffe60-114">したがって、これらのユーザーは、時間どおりに支払われる可能性を高めるための回収戦略を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="ffe60-115">予測</span><span class="sxs-lookup"><span data-stu-id="ffe60-115">Predictions</span></span>

<span data-ttu-id="ffe60-116">支払予測を使用すると、組織は支払いが遅延する可能性が高い請求書を識別することで業務プロセスを改善できます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="ffe60-117">組織では、この情報を使用して、期日までに支払われる可能性を高めるアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="ffe60-118">顧客支払予測機能では、機械学習モデルを使用して、顧客が未払の請求書を支払うタイミングをより正確に予測します。</span><span class="sxs-lookup"><span data-stu-id="ffe60-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="ffe60-119">この機械学習モデルには、過去の請求書、支払、および顧客データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ffe60-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="ffe60-120">未処理の各請求書に対して、この機能は次の 3 つの支払確度を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="ffe60-121">支払が期日までに実行される確度</span><span class="sxs-lookup"><span data-stu-id="ffe60-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="ffe60-122">支払が遅延して実行される確度</span><span class="sxs-lookup"><span data-stu-id="ffe60-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="ffe60-123">支払が非常に遅い確度</span><span class="sxs-lookup"><span data-stu-id="ffe60-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="ffe60-124">この機能では、予測支払の集計ビューも提供されます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="ffe60-125">[![支払予測の集計ビュー](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="ffe60-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="ffe60-126">各請求書には期限内支払いの確度が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="ffe60-127">期限支払いの確度が 50 パーセント未満の請求書は赤い丸でタグ付けられ、この請求書は回収代行業者からのアクションが必要かもしれないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ffe60-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="ffe60-128">[![支払確度の一覧](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="ffe60-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="ffe60-129">顧客支払予測機能では、予測を説明するためのコンテキスト情報も提供されます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="ffe60-130">この情報には、予測の影響を受けるトップ要素、顧客との取引の現在の状態、および顧客の過去の支払動作に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="ffe60-131">多くの企業では、回収プロセスは最有効化活動となっています。</span><span class="sxs-lookup"><span data-stu-id="ffe60-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="ffe60-132">つまり、回収プロセスは、請求書の期日になるまで開始されません。</span><span class="sxs-lookup"><span data-stu-id="ffe60-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="ffe60-133">顧客支払予測 (プレビュー) を使用すると、組織はコレクションをより積極的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="ffe60-134">トランザクションがコレクション プロセスを開始するまで待機する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ffe60-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="ffe60-135">代わりに、支払予測機能を使用して、プロアクティブなコレクションで期日内支払いの確度を改善するかどうかを判断することができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="ffe60-136">方法</span><span class="sxs-lookup"><span data-stu-id="ffe60-136">Methodology</span></span>

<span data-ttu-id="ffe60-137">従来は、人工知能 (AI) ソリューションを開発および配置することは困難でした。</span><span class="sxs-lookup"><span data-stu-id="ffe60-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="ffe60-138">データ科学者、領域の専門家 (SME)、およびエンジニアのチームが、使用可能な AI ソリューションの作成、開発、展開、および管理を行うために長期間働く必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffe60-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="ffe60-139">顧客支払予測を使用すると、Microsoft Dynamics 365 Finance で AI ソリューションを簡単に導入および使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ffe60-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="ffe60-140">Microsoft は、Microsoft AI Builder の上に構築された AI ソリューションをパッケージ化しています。</span><span class="sxs-lookup"><span data-stu-id="ffe60-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="ffe60-141">したがって、ユーザーは、AI ソリューションを 1 回のマウスクリックで配置することにより、インテリジェント予測のメリットを活用することができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="ffe60-142">予測の正確性に満足しない場合は、パワー ユーザーは (ここでも 1 回のクリックで)、AI Builder の拡張機能のエクスペリエンスへと入り、予測生成に使用するフィールドを選択または選択解除できます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="ffe60-143">準備が整ったら、モデルを "トレーニング" して変更を公開することができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="ffe60-144">新しくトレーニングしたモデルは、Dynamics 365 Finance で予測を生成するために自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="ffe60-145">リリースの詳細</span><span class="sxs-lookup"><span data-stu-id="ffe60-145">Release details</span></span>

<span data-ttu-id="ffe60-146">財務インサイトのパブリック プレビューは、米国、ヨーロッパ、および英国でのデプロイの試行ができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="ffe60-147">Microsoft は、その他の地域へのサポートも段階的に追加しています。</span><span class="sxs-lookup"><span data-stu-id="ffe60-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="ffe60-148">パブリック プレビュー機能は、Tier-2 のサンドボックス環境でのみ有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="ffe60-149">サンドボックス環境で作成された設定および AI モデルは、運用環境に移行できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ffe60-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="ffe60-150">詳細については、[Microsoft Dynamics 365 プレビューの補足の使用条件](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffe60-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="ffe60-151">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="ffe60-151">Privacy notice</span></span>

<span data-ttu-id="ffe60-152">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="ffe60-152">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
