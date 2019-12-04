---
title: 顧客支払に関するインサイト (プレビュー)
description: このトピックでは、個々の顧客の一般的な支払方法について理解を深め、他の方法よりも早くコレクション プロセスの開始を正当化する状況を特定できる支払インサイト機能について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773994"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="8de6e-103">顧客支払に関するインサイト (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="8de6e-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8de6e-104">このトピックでは、個々の顧客の一般的な支払方法について理解を深め、他の方法で実行するよりも早くコレクション プロセスの開始を正当化する状況を特定できる支払インサイト機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8de6e-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="8de6e-105">概要</span><span class="sxs-lookup"><span data-stu-id="8de6e-105">Overview</span></span>

<span data-ttu-id="8de6e-106">多くの場合、組織にとって顧客が請求書に支払を行う時を予測するのは難しいことです。</span><span class="sxs-lookup"><span data-stu-id="8de6e-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="8de6e-107">このインサイトの欠如により、不正確なキャッシュ フロー予測、コレクション プロセスの開始の遅れ、および支払滞納する顧客にリリースされた注文につながります。</span><span class="sxs-lookup"><span data-stu-id="8de6e-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="8de6e-108">顧客支払インサイト (プレビュー) は、組織が顧客請求書に支払が行われる時を予測し、期限厳守で支払が行われる確度を改善するコレクション戦略を作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="8de6e-109">予測</span><span class="sxs-lookup"><span data-stu-id="8de6e-109">Predictions</span></span>

<span data-ttu-id="8de6e-110">支払予測を使用すると、組織は、遅く支払われそうな請求書を簡単に識別して業務プロセスを改善でき、期限厳守で支払われる可能性を高める適切な措置を講じることができます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="8de6e-111">過去の請求書、支払および顧客データを活用する機械学習モデルを使用して、顧客支払インサイト (プレビュー) は、顧客が未払の請求書を支払う時をより正確に予測します。</span><span class="sxs-lookup"><span data-stu-id="8de6e-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="8de6e-112">各未処理の請求書について、顧客支払インサイト (プレビュー) は 3 つの確度を予測します。</span><span class="sxs-lookup"><span data-stu-id="8de6e-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="8de6e-113">期限厳守で支払われる確度</span><span class="sxs-lookup"><span data-stu-id="8de6e-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="8de6e-114">遅く支払われる確度</span><span class="sxs-lookup"><span data-stu-id="8de6e-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="8de6e-115">かなり遅く支払われる確度</span><span class="sxs-lookup"><span data-stu-id="8de6e-115">Probability of payment being made very late</span></span>

<span data-ttu-id="8de6e-116">3 つのバケットである期限厳守、遅延、かなりの遅延のいずれかで顧客が支払う合計支払額を組織が理解できるようにするため、顧客支払インサイト (プレビュー) は予期される支払いの集計ビューも提供します。</span><span class="sxs-lookup"><span data-stu-id="8de6e-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="8de6e-117">[![支払予測の集計ビュー](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="8de6e-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="8de6e-118">また、各請求書には期限厳守の支払いの確度が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="8de6e-119">期限厳守の支払の確度が 50% 未満の場合、請求書は赤い丸でタグ付けられ、これらの請求書にコレクション注意を払う必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="8de6e-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="8de6e-120">[![支払確度の一覧](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="8de6e-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="8de6e-121">顧客支払インサイト (プレビュー) は、予測の影響を受ける上位要因、顧客とのビジネスの現在の状態、および顧客の支払動作履歴に関する詳細など、予測を説明するためのコンテキスト情報も提供します。</span><span class="sxs-lookup"><span data-stu-id="8de6e-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="8de6e-122">多くのビジネスでは、コレクション プロセスはリアクティブな活動です。請求書の期日が来るまでコレクション プロセスは開始されません。</span><span class="sxs-lookup"><span data-stu-id="8de6e-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="8de6e-123">顧客支払インサイト (プレビュー) を使用すると、組織はコレクションをより積極的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="8de6e-124">トランザクションがコレクション プロセスを開始するまで待機する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8de6e-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="8de6e-125">代わりに、支払予測機能を使用して、プロアクティブなコレクションが期限厳守で支払われる確度を改善するかどうかを特定できます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="8de6e-126">また支払予測は、ビジネスがコレクション プロセスを早い段階で開始するための判断に必要な情報も提供します。</span><span class="sxs-lookup"><span data-stu-id="8de6e-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="8de6e-127">方法</span><span class="sxs-lookup"><span data-stu-id="8de6e-127">Methodology</span></span>

<span data-ttu-id="8de6e-128">AI ソリューションの開発と展開は困難です。</span><span class="sxs-lookup"><span data-stu-id="8de6e-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="8de6e-129">データ科学者、領域の専門家およびエンジニアのチームが、使用可能な AI ソリューションの作成、開発、展開、および管理を行うために長期間働く必要があります。</span><span class="sxs-lookup"><span data-stu-id="8de6e-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="8de6e-130">Finance で AI ソリューションを展開および使用しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="8de6e-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="8de6e-131">Microsoft AI Builder の上に構築された Finance で AI ソリューションをパッケージ化しています。</span><span class="sxs-lookup"><span data-stu-id="8de6e-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="8de6e-132">ボタンを一度クリックするだけで、エンド ユーザーは AI ソリューションを展開し、インテリジェント予測の利点を活用できます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="8de6e-133">組織が予測の正確性に満足していない場合、パワー ユーザーはもう一度のクリックで、AI builder の拡張機能エクスペリエンスに入力し、予測生成に使用するフィールドを選択または選択解除できます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="8de6e-134">準備が整ったら、変更をトレーニングおよび公開できます。新しくトレーニングされたモデルは Finance での予測に対して自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="8de6e-135">顧客支払インサイト (プレビュー) の入手方法</span><span class="sxs-lookup"><span data-stu-id="8de6e-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="8de6e-136">顧客支払インサイト (プレビュー) に関心を持っている場合、[顧客支払インサイト (プレビュー)](mailto:fiap@microsoft.com) へ電子メールを送信してください。</span><span class="sxs-lookup"><span data-stu-id="8de6e-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="8de6e-137">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="8de6e-137">Privacy Notice</span></span>

<span data-ttu-id="8de6e-138">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよびセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル契約には含まれておらず、(3) 個人データや、その他法律上または規制順守要件の対象となるデータを処理することはできず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="8de6e-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


