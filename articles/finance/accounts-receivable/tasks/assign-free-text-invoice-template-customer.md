---
title: 顧客への自由書式の請求書テンプレートの割り当て
description: このタスクは顧客に自由書式の請求書テンプレートを割り当てる方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19742c53406cd1c616e8be1172b93157437132e8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140332"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="cd1bd-103">顧客への自由書式の請求書テンプレートの割り当て</span><span class="sxs-lookup"><span data-stu-id="cd1bd-103">Assign a free text invoice template to a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd1bd-104">このタスクは顧客に自由書式の請求書テンプレートを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="cd1bd-105">このタスクは USMF デモ会社を使用し、A/R の請求書の管理および処理を担当するユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="cd1bd-106">**ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 顧客 > すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="cd1bd-107">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cd1bd-108">**アクション ウィンドウ**で、**請求書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="cd1bd-109">**定期的な請求書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="cd1bd-110">自由書式の請求書テンプレートを顧客に割り当て、請求書を顧客に送信する頻度を指定するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="cd1bd-111">顧客に新しいテンプレートを割り当てる場合は、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="cd1bd-112">**テンプレート** フィールドで、顧客に割り当てる自由書式の請求書のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="cd1bd-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cd1bd-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cd1bd-115">**請求開始日**フィールドに、最初の請求書が生成される日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="cd1bd-116">**定期処理の終了**セクションで、定期的な終了を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="cd1bd-117">次のいずれかを選択します: 終了日なし – 顧客口座からテンプレートが削除されるまで請求書は無期限に生成されます。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="cd1bd-118">請求終了日 – このオプションを選択し、請求書を生成できる最後の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="cd1bd-119">**最大累計金額** フィールドに、請求書の生成が停止するまでの最大累計金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-119">In the **Maximum cumulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="cd1bd-120">選択したテンプレートを使用して達する最大累積金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="cd1bd-121">たとえば、1,000.00 を入力し、100.00 の月次請求書をそれぞれ生成した場合、10 番目の請求書が生成された後に請求書の生成は停止します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="cd1bd-122">**既定値を使用して定期的な請求書を生成する**セクションで、自由書式の請求書テンプレートまたは顧客口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="cd1bd-123">請求書を作成する場合、自由書式の請求書テンプレートを使うか、顧客 ID を使って言語、転記プロファイル、消費税グループ、品目消費税グループ、リスト コード、配送先の国 / 地域、通貨、支払条件、支払方法、支払仕様、支払スケジュール、現金割引、財務分析コード、振替送金伝票についての規定値を決定するか選択します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="cd1bd-124">**定期的なアイテムのパターン** フィールドで、定期的なアイテムのパターンを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="cd1bd-125">[毎日] – [間隔] フィールドでこのオプションを選択し、日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="cd1bd-126">たとえば、15 を入力すると、請求書はこの顧客に対して 15 日ごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="cd1bd-127">[毎週] – [間隔] フィールドでこのオプションを選択し、週の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="cd1bd-128">たとえば、2 を入力すると、請求書はこの顧客に対して 2 週間おきに生成されます。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="cd1bd-129">[毎月] – [間隔] フィールドでこのオプションを選択し、月数を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="cd1bd-130">たとえば、6 を入力すると、請求書はこの顧客に対して 6 か月ごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="cd1bd-131">[毎年] – [間隔] フィールドでこのオプションを選択し、年数を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="cd1bd-132">たとえば、2 を入力すると、請求書はこの顧客に対して 2 年ごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="cd1bd-133">**間隔**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd1bd-133">In the **Per** field, enter a number.</span></span>

