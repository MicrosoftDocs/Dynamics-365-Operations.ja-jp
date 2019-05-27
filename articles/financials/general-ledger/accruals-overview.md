---
title: 見越計上の概要
description: この記事は、見越し計上について説明し、その設定方法およびトランザクションの作成方法に関する情報を提供します。
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23c6a3402e4bc4a22d764017ba56554001300a67
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557385"
---
# <a name="accruals-overview"></a><span data-ttu-id="32cc8-103">見越計上の概要</span><span class="sxs-lookup"><span data-stu-id="32cc8-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32cc8-104">この記事は、見越し計上について説明し、その設定方法およびトランザクションの作成方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="32cc8-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="32cc8-105">発生主義会計では、見越計上は、支払を受け取ったときではなく獲得した期間に認識された収益を追跡するために、支払ったときではなく経費の発生時に認識された経費 (原価) を追跡するために、使用されます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="32cc8-106">発生主義スキーマ</span><span class="sxs-lookup"><span data-stu-id="32cc8-106">Accrual schemes</span></span>
<span data-ttu-id="32cc8-107">発生主義スキーマが繰延収益と原価を設定するために使用され、同じ発生主義スキーマが、収益と原価の両方に使用できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="32cc8-108">元帳計上では、原価または収益が適切な期間に認識されるように、仕訳帳明細行の原価または収益を再配分します。</span><span class="sxs-lookup"><span data-stu-id="32cc8-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="32cc8-109">**発生主義スキーマ**ページで、発生主義スキーマが適用される場合に使用する借方勘定と貸方勘定を指定します。</span><span class="sxs-lookup"><span data-stu-id="32cc8-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="32cc8-110">**借方** – 定義した主勘定は、仕訳帳伝票の明細行の借方主勘定と置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="32cc8-111">この勘定は、元帳計上トランザクションに基づく繰延の取消にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="32cc8-112">**貸方** – 定義した主勘定は、仕訳帳伝票の明細行の貸方主勘定と置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="32cc8-113">この勘定は、元帳計上トランザクションに基づく繰延の取消にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="32cc8-114">使用する勘定を決定した後、見越計上トランザクションの作成時に伝票番号の作成方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="32cc8-115">また、トランザクションの発生頻度、トランザクションの作成回数、およびトランザクションの転記時期を指定できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="32cc8-116">発生主義スキーマの作成後、元帳計上機能を使用して、一部の仕訳帳で発生主義スキーマを使用できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="32cc8-117">元帳計上</span><span class="sxs-lookup"><span data-stu-id="32cc8-117">Ledger accruals</span></span>
<span data-ttu-id="32cc8-118">仕訳帳を入力すると、**機能**メニューの**元帳計**をクリックできます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="32cc8-119">その後、発生主義スキーマを選択すると、発生主義スキーマによって決定される、その期間にわたって分割される仕訳帳からの基準額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="32cc8-120">たとえば、1 月に 1 年間全体の従業員の保険料を 12,000 支払う場合、各月の保険料を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32cc8-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="32cc8-121">開始日は選択できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-121">You can select the start date.</span></span> <span data-ttu-id="32cc8-122">また、金額が勘定または相手勘定に基づくかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="32cc8-123">選択後に、**トランザクション**をクリックして、発生主義スキーマに基づいて作成されたすべてのトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="32cc8-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="32cc8-124">たとえば、1 年間の保険料 12,000 を分割する場合、各月では 1,000 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="32cc8-125">仕訳帳を転記した後、**伝票トランザクション**照会ページを使用して、トランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="32cc8-126">発生主義スキーマが適用できない場合 (たとえば、販売注文請求書または発注請求書が含まれる場合)、前払金額を貸方転記し、経費金額を借方転記できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="32cc8-127">その後、発生主義スキーマの適用時に**相殺**を選択できます。</span><span class="sxs-lookup"><span data-stu-id="32cc8-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="32cc8-128">詳細については、[発生主義スキーマの作成](tasks/create-accrual-schemes.md) および [元帳発生トランザクションの作成](tasks/create-ledger-accrual-transactions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32cc8-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>
