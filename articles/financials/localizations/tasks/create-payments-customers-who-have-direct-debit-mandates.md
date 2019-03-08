---
title: 口座引落の委任状がある顧客の支払の作成
description: この手順では、口座引落がコンフィギュレーションされており支払対象の請求書のある顧客用に、ISO20022 の口座引落支払ファイルを生成するプロセスを説明します。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6781ac38fff6344bfc9546c3ffd2253fb3ef712c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "342135"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="a97b7-103">口座引落の委任状がある顧客の支払の作成</span><span class="sxs-lookup"><span data-stu-id="a97b7-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a97b7-104">この手順では、口座引落がコンフィギュレーションされており支払対象の請求書のある顧客用に、ISO20022 の口座引落支払ファイルを生成するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="a97b7-105">請求書の作成および転記はオプションです。</span><span class="sxs-lookup"><span data-stu-id="a97b7-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="a97b7-106">支払われる請求書の代わりに、顧客が支払を行うシナリオをサポートするために、支払ファイルを生成する前に仕訳帳の委任状を選択できます。</span><span class="sxs-lookup"><span data-stu-id="a97b7-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="a97b7-107">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="a97b7-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="a97b7-108">これは、5 つのうち 5 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="a97b7-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="a97b7-109">このタスクを完了するために、以前のタスクを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="a97b7-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="a97b7-110">まず、顧客支払電子申告コンフィギュレーションをインポートし、支払方法をコンフィギュレーションする必要があります。また会社および顧客情報を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a97b7-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="a97b7-111">口座引落情報を含む自由書式の請求書を転記</span><span class="sxs-lookup"><span data-stu-id="a97b7-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="a97b7-112">[売掛金勘定] > [請求書] > [すべての自由書式の請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="a97b7-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-113">Click New.</span></span>
3. <span data-ttu-id="a97b7-114">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="a97b7-115">たとえば、[DE-010] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="a97b7-116">[支払方法] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="a97b7-117">例えば、</span><span class="sxs-lookup"><span data-stu-id="a97b7-117">For example.</span></span> <span data-ttu-id="a97b7-118">[電子] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-118">select Electronic.</span></span>  
5. <span data-ttu-id="a97b7-119">[口座引落の委任状 ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="a97b7-120">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-120">Click Add line.</span></span>
7. <span data-ttu-id="a97b7-121">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="a97b7-122">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="a97b7-123">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="a97b7-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-124">Click Post.</span></span>
11. <span data-ttu-id="a97b7-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="a97b7-126">支払の作成</span><span class="sxs-lookup"><span data-stu-id="a97b7-126">Create a payment</span></span>
1. <span data-ttu-id="a97b7-127">[売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="a97b7-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-128">Click New.</span></span>
3. <span data-ttu-id="a97b7-129">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="a97b7-130">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-130">Click Lines.</span></span>
5. <span data-ttu-id="a97b7-131">[支払提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="a97b7-132">[支払提案の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="a97b7-133">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="a97b7-134">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-134">Click Filter.</span></span>
9. <span data-ttu-id="a97b7-135">リストで、[顧客トランザクション] テーブルの行、および [支払方法] フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="a97b7-136">支払するための顧客トランザクションの選択には、すべての基準を適用できます。</span><span class="sxs-lookup"><span data-stu-id="a97b7-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="a97b7-137">この例では、トランザクションをフィルターする支払方法として [電子] を使用します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="a97b7-138">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a97b7-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="a97b7-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-139">Click OK.</span></span>
12. <span data-ttu-id="a97b7-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-140">Click OK.</span></span>
13. <span data-ttu-id="a97b7-141">[支払の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a97b7-141">Click Create payments.</span></span>

## <a name="generate-a-payment-file"></a><span data-ttu-id="a97b7-142">支払ファイルの生成</span><span class="sxs-lookup"><span data-stu-id="a97b7-142">Generate a payment file</span></span>

