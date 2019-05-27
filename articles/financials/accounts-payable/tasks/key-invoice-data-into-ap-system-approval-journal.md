---
title: 承認仕訳帳を使用した AP システムの主請求書データ
description: このタスク ガイドでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法を示します。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550377"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="2abed-103">承認仕訳帳を使用した AP システムの主請求書データ</span><span class="sxs-lookup"><span data-stu-id="2abed-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2abed-104">このタスク ガイドでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2abed-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="2abed-105">請求書の作成と転記</span><span class="sxs-lookup"><span data-stu-id="2abed-105">Create and post and invoice</span></span>
1. <span data-ttu-id="2abed-106">[買掛金勘定] > [請求書] > [仕入帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2abed-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="2abed-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-107">Click New.</span></span>
3. <span data-ttu-id="2abed-108">使用する仕入帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="2abed-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="2abed-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2abed-110">登録を開いて経費明細行を入力するには [明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="2abed-111">仕入先を選択してください。</span><span class="sxs-lookup"><span data-stu-id="2abed-111">Select a vendor.</span></span> <span data-ttu-id="2abed-112">たとえば、US-104 を入力または選択</span><span class="sxs-lookup"><span data-stu-id="2abed-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="2abed-113">[請求書] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2abed-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="2abed-114">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2abed-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="2abed-115">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2abed-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="2abed-116">[承認者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2abed-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2abed-117">承認者を強調表示して [選択] をクリックすると、その承認者を選択します。</span><span class="sxs-lookup"><span data-stu-id="2abed-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="2abed-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-118">Click Post.</span></span>
13. <span data-ttu-id="2abed-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2abed-119">Close the page.</span></span>
14. <span data-ttu-id="2abed-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2abed-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="2abed-121">請求書の承認</span><span class="sxs-lookup"><span data-stu-id="2abed-121">Approve an invoice</span></span>
1. <span data-ttu-id="2abed-122">[買掛金勘定] > [請求書] > [請求書の承認] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2abed-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="2abed-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-123">Click New.</span></span>
3. <span data-ttu-id="2abed-124">使用する請求書承認仕訳帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="2abed-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="2abed-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2abed-126">明細行をクリックすると、承認する請求書を選択できるページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2abed-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="2abed-127">[伝票の検索] を選択すると、承認待ちの請求書をすべて表示します。</span><span class="sxs-lookup"><span data-stu-id="2abed-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="2abed-128">作成した請求書をマークします。</span><span class="sxs-lookup"><span data-stu-id="2abed-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="2abed-129">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-129">Click Select.</span></span>
    * <span data-ttu-id="2abed-130">上の手順で選択した伝票は、選択後にこのリストに移動されます。</span><span class="sxs-lookup"><span data-stu-id="2abed-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="2abed-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-131">Click OK.</span></span>
10. <span data-ttu-id="2abed-132">請求書に経費勘定を追加するには、勘定番号フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="2abed-133">勘定番号を入力し、Tab キーでこのフィールドから移動します。</span><span class="sxs-lookup"><span data-stu-id="2abed-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="2abed-134">たとえば、600120 と入力します。</span><span class="sxs-lookup"><span data-stu-id="2abed-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="2abed-135">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-135">Click Post.</span></span>
13. <span data-ttu-id="2abed-136">転記されたエントリを表示するには、[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2abed-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="2abed-137">承認保留中の請求書の勘定は、取消されて実際の経費勘定に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2abed-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

