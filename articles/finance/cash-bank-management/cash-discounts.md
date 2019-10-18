---
title: 現金割引
description: 現金割引は、買掛金勘定および売掛金勘定に設定され、共有されます。  現金割引の使用可能なオプションは、顧客請求書または仕入先請求書で定義でき、現金割引日以内に請求書が支払われた場合に適用されます。
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 139fb4fdb7d4f8034bff5e9668dc794f29fb327e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178687"
---
# <a name="cash-discounts"></a><span data-ttu-id="cd726-104">現金割引</span><span class="sxs-lookup"><span data-stu-id="cd726-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd726-105">現金割引は、買掛金勘定および売掛金勘定に設定され、共有されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="cd726-106">現金割引の使用可能なオプションは、顧客請求書または仕入先請求書で定義でき、現金割引日以内に請求書が支払われた場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="cd726-107">現金割引</span><span class="sxs-lookup"><span data-stu-id="cd726-107">Cash discounts</span></span>

<span data-ttu-id="cd726-108">両方の顧客または仕入先に対する現金割引は、現金割引ページで作成できます。</span><span class="sxs-lookup"><span data-stu-id="cd726-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="cd726-109">また、[次の割引コード] フィールドを使用して、前の現金割引日の期限が切れると順に適用される一連の現金割引を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="cd726-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="cd726-110">詳細については、このトピックで後述する「例 : 一連の現金割引」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd726-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="cd726-111">請求書、貸方トランザクション (支払票または訂正票)、またはその両方で、その法人の会計通貨以外の通貨で入力されている場合、為替レートを使用して計算される現金割引は支払票または訂正票の日付に基づきます。</span><span class="sxs-lookup"><span data-stu-id="cd726-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="cd726-112">請求書と信用状ドキュメントが異なる法人で入力され、法人の会計通貨が異なる場合、為替レートは、信用状ドキュメントの日付時点で、請求書の法人から取得されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="cd726-113">詳細については、このトピックで後述する 「例 : 現金割引の為替レート」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd726-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="cd726-114">現金割引主勘定の既定順序</span><span class="sxs-lookup"><span data-stu-id="cd726-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="cd726-115">現金割引を受けられる期間内に請求書が決済されると、次の既定優先順位に従って現金割引主勘定に自動的に現金割引が転記されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="cd726-116">顧客の未処理トランザクションの決済ページまたは仕入先の未処理トランザクションの決済ページの [代替現金割引勘定] フィールドで指定されている主勘定。</span><span class="sxs-lookup"><span data-stu-id="cd726-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="cd726-117">請求書の売上税コードに割り当てられている元帳転記グループの [顧客現金割引] フィールドまたは [仕入先現金割引] フィールドで指定されている主勘定。</span><span class="sxs-lookup"><span data-stu-id="cd726-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="cd726-118">元帳転記グループ ページの元帳転記グループを設定して、売上税コード ページの売上税コードに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="cd726-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="cd726-119">決済される請求書に含まれる現金割引コードの [顧客割引の主勘定] フィールドまたは [仕入先割引の主勘定] フィールドの現金割引ページにある主転記勘定。</span><span class="sxs-lookup"><span data-stu-id="cd726-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="cd726-120">自動トランザクションの勘定ページで定義された現金割引の主勘定。</span><span class="sxs-lookup"><span data-stu-id="cd726-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="cd726-121">例: 一連の現金割引</span><span class="sxs-lookup"><span data-stu-id="cd726-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="cd726-122">3 つの現金割引コードを次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="cd726-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="cd726-123">コード 5D10% – 金額が 5 日以内に支払われた場合は 10% の現金割引を行う。</span><span class="sxs-lookup"><span data-stu-id="cd726-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="cd726-124">コード 10D5% –金額が 10 日以内に支払われた場合は 5% の現金割引を行う。</span><span class="sxs-lookup"><span data-stu-id="cd726-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="cd726-125">コード 14D2% – 金額が 14 日以内に支払われた場合は 2% の現金割引を行う。</span><span class="sxs-lookup"><span data-stu-id="cd726-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="cd726-126">[次の割引コード] フィールド:</span><span class="sxs-lookup"><span data-stu-id="cd726-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="cd726-127">5D10% コードの場合は、10D5% を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd726-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="cd726-128">10D5% コードの場合は、14D2% を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd726-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="cd726-129">14D2% コードの場合は、[次の割引コード] フィールドを空欄のままにします。</span><span class="sxs-lookup"><span data-stu-id="cd726-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="cd726-130">3 つの現金割引は、支払期日が請求書の前の現金割引の日付を超えていると適用されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="cd726-131">現金割引の日付が現金割引期間に当てはまる請求書が支払われる場合、現金割引は 1 つだけ許可されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="cd726-132">例: 現金割引の為替レート</span><span class="sxs-lookup"><span data-stu-id="cd726-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="cd726-133">法人の会計通貨は EUR で、次の為替レートは USD で指定されています。</span><span class="sxs-lookup"><span data-stu-id="cd726-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="cd726-134">2 月 1 日 = 110</span><span class="sxs-lookup"><span data-stu-id="cd726-134">February 1 = 110</span></span>
-   <span data-ttu-id="cd726-135">3 月 1 日 = 80</span><span class="sxs-lookup"><span data-stu-id="cd726-135">March 1 = 80</span></span>

<span data-ttu-id="cd726-136">現金割引条件が 20D2% の 1000 USD の請求書が、2 月 15 日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="cd726-137">請求書の会計通貨金額は 1100 EUR です。</span><span class="sxs-lookup"><span data-stu-id="cd726-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="cd726-138">3 月 1 日に 980 USD の支払が請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="cd726-139">現金割引金額は 20 USD です。</span><span class="sxs-lookup"><span data-stu-id="cd726-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="cd726-140">支払の会計通貨金額は 784 EUR です。</span><span class="sxs-lookup"><span data-stu-id="cd726-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="cd726-141">現金割引の会計通貨金額は 3 月 1 日現在の為替レートを使用して計算されます。20 \* 80 / 100 = 16 EUR。</span><span class="sxs-lookup"><span data-stu-id="cd726-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="cd726-142">[一部支払の現金割引を計算] オプションが売掛金勘定パラメーターまたは買掛金管理パラメーター ページで選択されている場合、それぞれの一部支払の日に有効となる為替レートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd726-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 

