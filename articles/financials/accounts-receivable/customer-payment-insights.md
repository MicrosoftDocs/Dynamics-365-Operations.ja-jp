---
title: 顧客支払インサイト (プレビュー)
description: このトピックでは、請求書に支払が行われる時を予測し、組織が期限厳守で支払が行われる確度を改善するための最適化戦略を作成するのに、顧客支払インサイトがどのように役立つかについて説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566252"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="19bad-103">顧客支払インサイト (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="19bad-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="19bad-104">この機能は対象となるリリースの一部であり、ユーザーがプライベート プレビューを希望した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="19bad-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="19bad-105">この機能は、次回の一般提供リリースに含まれます。</span><span class="sxs-lookup"><span data-stu-id="19bad-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="19bad-106">概要</span><span class="sxs-lookup"><span data-stu-id="19bad-106">Overview</span></span>

<span data-ttu-id="19bad-107">多くの場合、組織にとって顧客が請求書に支払を行う時を予測するのは難しいことです。</span><span class="sxs-lookup"><span data-stu-id="19bad-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="19bad-108">このインサイトの欠如により、不正確なキャッシュ フロー予測、非能率的なコレクション プロセス、および貸方リスクをもたらす顧客に注文がリリースされる可能性が生じることがあります。</span><span class="sxs-lookup"><span data-stu-id="19bad-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="19bad-109">顧客支払インサイト (プレビュー) は、請求書に支払が行われる時を予測するために機械学習を使用します。</span><span class="sxs-lookup"><span data-stu-id="19bad-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="19bad-110">また顧客支払の期限厳守の確度を最大にするように設計された最適化戦略も提供します。</span><span class="sxs-lookup"><span data-stu-id="19bad-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="19bad-111">予測</span><span class="sxs-lookup"><span data-stu-id="19bad-111">Predictions</span></span>

<span data-ttu-id="19bad-112">支払の予測によって、組織は次の事柄により業務プロセスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="19bad-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="19bad-113">遅い支払が予測される請求書を簡単に識別します。</span><span class="sxs-lookup"><span data-stu-id="19bad-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="19bad-114">支払が期限厳守で行われる可能性を改善する適切な措置を講じます。</span><span class="sxs-lookup"><span data-stu-id="19bad-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="19bad-115">顧客支払インサイト (プレビュー) は、請求書に支払が行われる時を予測するために機械学習を使用します。</span><span class="sxs-lookup"><span data-stu-id="19bad-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="19bad-116">請求書に支払が行われる時を予測するのに使用される機械学習モデルを作成するために、過去の請求書、支払、および顧客データを使用します。</span><span class="sxs-lookup"><span data-stu-id="19bad-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="19bad-117">各未処理の請求書について、顧客支払インサイト (プレビュー) は 3 つの確度を予測します。</span><span class="sxs-lookup"><span data-stu-id="19bad-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="19bad-118">期限厳守で支払が行われる確度 (請求書の期日内)。</span><span class="sxs-lookup"><span data-stu-id="19bad-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="19bad-119">請求書の期日から 30 日以内に支払が行われる確度。</span><span class="sxs-lookup"><span data-stu-id="19bad-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="19bad-120">請求書の期日から 30 日を超えて支払が行われる確度。</span><span class="sxs-lookup"><span data-stu-id="19bad-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="19bad-121">支払の確度は予測のセクションで表示できます。</span><span class="sxs-lookup"><span data-stu-id="19bad-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="19bad-122">[![支払の予測](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="19bad-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="19bad-123">各請求書には、上記のように定義した 3 つの予測支払確度シナリオのいずれかを使用した、成功支払確度も割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="19bad-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="19bad-124">最上位の支払確度を持つシナリオが成功するシナリオになります。</span><span class="sxs-lookup"><span data-stu-id="19bad-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="19bad-125">たとえば、請求書に対して、期日厳守で支払が行われる確度が 71%、請求書の期日から 30 日以内に支払が行われる確度が 13%、請求書の期日から 30 日を超えて支払が行われる確度が 16% と予測されたとします。</span><span class="sxs-lookup"><span data-stu-id="19bad-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="19bad-126">最上位の確度は請求書が期限厳守のシナリオに含まれることを示しているので、請求書には期限厳守で支払が行われる確度がタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="19bad-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="19bad-127">[![支払の予測](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="19bad-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="19bad-128">最適化戦略</span><span class="sxs-lookup"><span data-stu-id="19bad-128">Optimization strategies</span></span>

<span data-ttu-id="19bad-129">支払の予測に加えて、顧客支払インサイト (プレビュー) は期限厳守で支払が行われる可能性を改善するための最適化戦略を使用できます。</span><span class="sxs-lookup"><span data-stu-id="19bad-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="19bad-130">これにより、ユーザーが請求書および顧客のパラメーターを調整することによって、組織は「what-if」分析ができるようになり、期限厳守で請求書の支払を受け取れる確度により、対応する効果を比較することができます。</span><span class="sxs-lookup"><span data-stu-id="19bad-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="19bad-131">たとえば、組織は期限厳守で支払を受け取れる確度により、請求書の現金割引を更新する効果を評価したいことがあります。</span><span class="sxs-lookup"><span data-stu-id="19bad-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="19bad-132">請求書が新しい割引を使用するように最適化された場合、請求書に対する支払を期限厳守で受け取れる確度により、ユーザーは割引を適用する効果を確認できます。</span><span class="sxs-lookup"><span data-stu-id="19bad-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="19bad-133">期限厳守で支払を回収するメリットと比較した時、割引を適用する原価が最小になる場合、組織は将来のすべてのオープン注文に選択した割引を適用するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="19bad-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="19bad-134">現在、顧客支払インサイト (プレビュー) の最適化戦略として使用可能なのは割引のみです。</span><span class="sxs-lookup"><span data-stu-id="19bad-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="19bad-135">[![最適化された予測](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="19bad-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="19bad-136">顧客支払インサイト (プレビュー) の入手方法</span><span class="sxs-lookup"><span data-stu-id="19bad-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="19bad-137">顧客支払インサイト (プレビュー) に関心を持っている場合、[Finance インサイト プレビュー チーム](mailto:fiap@microsoft.com) へ電子メールを送信してください。</span><span class="sxs-lookup"><span data-stu-id="19bad-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="19bad-138">プライバシーに関する声明</span><span class="sxs-lookup"><span data-stu-id="19bad-138">Privacy Statement</span></span>

<span data-ttu-id="19bad-139">プレビューは米国の顧客データを保存します。</span><span class="sxs-lookup"><span data-stu-id="19bad-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="19bad-140">さらに、プレビューは (1) Dynamics 365 for Finance and Operations サービスを下回るプライバシーおよびセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル契約には含まれておらず、(3) 個人データや、その他法律上または規制順守要件の対象となるデータを処理することはできず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="19bad-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
