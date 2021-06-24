---
title: 定期請求書の設定と処理
description: この記事は、定期的な請求書の設定および処理の方法を説明します。 定期的に同じ金額に対して請求書を発行する場合に、定期的な請求書を使用できます。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834dc64ce531fb614bc7836e0def16f27ecf5e18
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188641"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="98be5-104">定期請求書の設定と処理</span><span class="sxs-lookup"><span data-stu-id="98be5-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98be5-105">この記事は、定期的な請求書の設定および処理の方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="98be5-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="98be5-106">定期的に同じ金額に対して請求書を発行する場合に、定期的な請求書を使用できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

## <a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="98be5-107">定期的な自由書式の請求書テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="98be5-107">Create a recurring free text invoice template</span></span>

<span data-ttu-id="98be5-108">同じサービスに関する請求を定期的に顧客に行うには、請求書を作成する場合でも、請求書の作成に再利用できる自由書式の請求書テンプレートを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98be5-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="98be5-109">このテンプレートには、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98be5-109">This template contains the following information:</span></span>

-   <span data-ttu-id="98be5-110">税グループ、支払条件、および支払方法などのヘッダー情報</span><span class="sxs-lookup"><span data-stu-id="98be5-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="98be5-111">サービスの説明、収益勘定、単価、請求金額などの明細行情報</span><span class="sxs-lookup"><span data-stu-id="98be5-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="98be5-112">出荷または処理の請求</span><span class="sxs-lookup"><span data-stu-id="98be5-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="98be5-113">コスト センター、事業単位などの財務分析コード情報を伴う勘定配布</span><span class="sxs-lookup"><span data-stu-id="98be5-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="98be5-114">実際には、請求書全体を作成し、テンプレートとして保存します。</span><span class="sxs-lookup"><span data-stu-id="98be5-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="98be5-115">**定期請求書** ページを使用してテンプレートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="98be5-116">顧客への自由書式の請求書テンプレートの割り当て、および繰り返し詳細の入力</span><span class="sxs-lookup"><span data-stu-id="98be5-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="98be5-117">テンプレートの作成後、請求先の顧客にテンプレートを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="98be5-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="98be5-118">また、請求をいつ、どのくらいの頻度で使用するか指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98be5-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="98be5-119">**顧客** ページの **請求書** タブでテンプレートを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="98be5-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="98be5-120">一覧にテンプレートを追加し、次の情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="98be5-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="98be5-121">必要に応じた、定期請求の開始日と終了日</span><span class="sxs-lookup"><span data-stu-id="98be5-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="98be5-122">定期請求の頻度 (たとえば、毎日または月に一度)</span><span class="sxs-lookup"><span data-stu-id="98be5-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="98be5-123">最大請求金額 (この情報が必要な場合)</span><span class="sxs-lookup"><span data-stu-id="98be5-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="98be5-124">顧客はさまざまな頻度の複数のテンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="98be5-125">定期請求書の生成</span><span class="sxs-lookup"><span data-stu-id="98be5-125">Generate the recurring invoices</span></span>
<span data-ttu-id="98be5-126">**定期請求書** ページには、定期的な請求書テンプレートを処理するタスクがあります。</span><span class="sxs-lookup"><span data-stu-id="98be5-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="98be5-127">請求書を生成する請求日およびテンプレートを指定します。</span><span class="sxs-lookup"><span data-stu-id="98be5-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="98be5-128">請求書が生成され、処理される請求書の各グループに固有の再実行 ID 番号が請求書に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="98be5-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

## <a name="post-recurring-free-text-invoices"></a><span data-ttu-id="98be5-129">定期的な自由書式の請求書の転記</span><span class="sxs-lookup"><span data-stu-id="98be5-129">Post recurring free text invoices</span></span>

<span data-ttu-id="98be5-130">定期請求書が生成された後、請求書の再実行 ID が **定期請求書** ページの転記タスクに表示されます。</span><span class="sxs-lookup"><span data-stu-id="98be5-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="98be5-131">リンクをクリックすることにより、再実行 ID の請求書をすべて表示できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="98be5-132">再実行 ID の請求書の確認中に、請求書を個別に削除できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="98be5-133">顧客の再実行設定をそのテンプレートに対してリセットすると、あとで再生成できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="98be5-134">再実行 ID の請求書は、1 つ、複数、またはすべてを転記できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="98be5-135">ワークフローが有効な場合、請求書を転記する前に **送信** をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98be5-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

## <a name="print-recurring-free-text-invoices"></a><span data-ttu-id="98be5-136">定期的な自由書式の請求書の印刷</span><span class="sxs-lookup"><span data-stu-id="98be5-136">Print recurring free text invoices</span></span>

<span data-ttu-id="98be5-137">定期請求書が転記された後、自由書式の請求書のリスト ページから請求書を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="98be5-138">選択した請求書を印刷でき、また印刷する請求書の範囲を選択できます。</span><span class="sxs-lookup"><span data-stu-id="98be5-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]