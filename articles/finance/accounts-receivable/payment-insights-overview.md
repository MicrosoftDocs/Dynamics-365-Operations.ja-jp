---
title: 顧客支払に関するインサイト (プレビュー)
description: このトピックでは、個々の顧客の一般的な支払方法を理解するために役立つ支払インサイト機能について説明します。 この機能を使用すると、他の方法よりも早くコレクション プロセスを開始することを正当化する状況を特定するのに役立ちます。
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
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d01f15223b4665caec16d6a4e51a5121a0ed94ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012167"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="c3216-104">顧客支払に関するインサイト (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="c3216-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c3216-105">このトピックでは、個々の顧客の一般的な支払方法を理解するために役立つ支払インサイト機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3216-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="c3216-106">この機能を使用すると、他の方法よりも早くコレクション プロセスを開始することを正当化する状況を特定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c3216-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="c3216-107">概要</span><span class="sxs-lookup"><span data-stu-id="c3216-107">Overview</span></span>

<span data-ttu-id="c3216-108">顧客が請求書に支払を行う時を予測するのは難しいことです。</span><span class="sxs-lookup"><span data-stu-id="c3216-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="c3216-109">このインサイトの欠如により、不正確なキャッシュ フロー予測、コレクション プロセスの開始の遅れ、および支払滞納する顧客にリリースされた注文につながります。</span><span class="sxs-lookup"><span data-stu-id="c3216-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="c3216-110">顧客支払インサイト (プレビュー) は、組織が顧客が請求書を支払う時を予測するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c3216-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="c3216-111">この情報は、組織が期日どおりに支払いを受ける可能性を高めるための回収戦略を作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c3216-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="c3216-112">予測</span><span class="sxs-lookup"><span data-stu-id="c3216-112">Predictions</span></span>

<span data-ttu-id="c3216-113">支払予測を使用すると、組織は、遅く支払われそうな請求書を簡単に識別して業務プロセスを改善でき、期限厳守で支払われる可能性を高める適切な措置を講じることができます。</span><span class="sxs-lookup"><span data-stu-id="c3216-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="c3216-114">過去の請求書、支払および顧客データを活用する機械学習モデルを使用して、顧客支払インサイト (プレビュー) は、顧客が未払の請求書を支払う時をより正確に予測します。</span><span class="sxs-lookup"><span data-stu-id="c3216-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="c3216-115">各未処理の請求書について、顧客支払インサイト (プレビュー) は 3 つの確度を予測します。</span><span class="sxs-lookup"><span data-stu-id="c3216-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="c3216-116">期限厳守で支払われる確度</span><span class="sxs-lookup"><span data-stu-id="c3216-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="c3216-117">遅く支払われる確度</span><span class="sxs-lookup"><span data-stu-id="c3216-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="c3216-118">かなり遅く支払われる確度</span><span class="sxs-lookup"><span data-stu-id="c3216-118">Probability of payment being made very late</span></span>

<span data-ttu-id="c3216-119">3 つのバケットである期日通り、遅延、かなりの遅延のいずれかで顧客が支払う合計支払額を組織が理解できるようにするため、顧客支払インサイト (プレビュー) は予期される支払いの集計ビューも提供します。</span><span class="sxs-lookup"><span data-stu-id="c3216-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="c3216-120">[![支払予測の集計ビュー](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="c3216-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="c3216-121">また、各請求書には期限厳守の支払いの確度が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c3216-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="c3216-122">期限厳守の支払の確度が 50% 未満の場合、請求書は赤い丸でタグ付けられ、これらの請求書にコレクション注意を払う必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="c3216-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="c3216-123">[![支払確度の一覧](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="c3216-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="c3216-124">顧客支払インサイト (プレビュー) は、予測の影響を受ける上位要因、顧客とのビジネスの現在の状態、および顧客の支払動作履歴に関する詳細など、予測を説明するためのコンテキスト情報も提供します。</span><span class="sxs-lookup"><span data-stu-id="c3216-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="c3216-125">多くのビジネスでは、コレクション プロセスはリアクティブな活動です。請求書の期日が来るまでコレクション プロセスは開始されません。</span><span class="sxs-lookup"><span data-stu-id="c3216-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="c3216-126">顧客支払インサイト (プレビュー) を使用すると、組織はコレクションをより積極的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c3216-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="c3216-127">トランザクションがコレクション プロセスを開始するまで待機する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c3216-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="c3216-128">代わりに、支払予測機能を使用して、プロアクティブなコレクションが期限厳守で支払われる確度を改善するかどうかを特定できます。</span><span class="sxs-lookup"><span data-stu-id="c3216-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="c3216-129">また支払予測は、ビジネスがコレクション プロセスを早い段階で開始するための判断に必要な情報も提供します。</span><span class="sxs-lookup"><span data-stu-id="c3216-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="c3216-130">方法</span><span class="sxs-lookup"><span data-stu-id="c3216-130">Methodology</span></span>

<span data-ttu-id="c3216-131">AI ソリューションの開発と展開は困難です。</span><span class="sxs-lookup"><span data-stu-id="c3216-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="c3216-132">データ科学者、領域の専門家、およびエンジニアのチームが、使用可能な AI ソリューションの作成、開発、展開、および管理を行うために長期間働く必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3216-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="c3216-133">Finance で AI ソリューションを展開および使用しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="c3216-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="c3216-134">Microsoft AI Builder の上に構築された Finance で AI ソリューションをパッケージ化しています。</span><span class="sxs-lookup"><span data-stu-id="c3216-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="c3216-135">ボタンを一度クリックするだけで、エンド ユーザーは AI ソリューションを展開し、インテリジェント予測の利点を活用できます。</span><span class="sxs-lookup"><span data-stu-id="c3216-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="c3216-136">組織が予測の正確性に満足していない場合、パワー ユーザーはもう一度のクリックで、AI builder の拡張機能エクスペリエンスに入力し、予測生成に使用するフィールドを選択または選択解除できます。</span><span class="sxs-lookup"><span data-stu-id="c3216-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="c3216-137">準備が整ったら、変更をトレーニングおよび公開できます。新しくトレーニングされたモデルは Finance での予測に対して自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="c3216-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="c3216-138">顧客支払インサイト (プレビュー) の入手方法</span><span class="sxs-lookup"><span data-stu-id="c3216-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="c3216-139">顧客支払インサイト (プレビュー) にご興味がありましたら、[顧客支払インサイト (プレビュー)](mailto:fiap@microsoft.com) へ電子メールを送信してください。</span><span class="sxs-lookup"><span data-stu-id="c3216-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="c3216-140">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="c3216-140">Privacy Notice</span></span>

<span data-ttu-id="c3216-141">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよびセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル契約には含まれておらず、(3) 個人データや、その他法律上または規制順守要件の対象となるデータを処理することはできず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="c3216-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


