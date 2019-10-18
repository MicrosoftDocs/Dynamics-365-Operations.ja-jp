---
title: 承認仕訳帳を使用した買掛金勘定への請求書データの入力
description: このトピックでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178721"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="a2f17-103">承認仕訳帳を使用した買掛金勘定への請求書データの入力</span><span class="sxs-lookup"><span data-stu-id="a2f17-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2f17-104">このトピックでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="a2f17-105">請求書の作成と転記</span><span class="sxs-lookup"><span data-stu-id="a2f17-105">Create and post and invoice</span></span>
1. <span data-ttu-id="a2f17-106">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 仕入帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="a2f17-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-107">Select **New**.</span></span>
3. <span data-ttu-id="a2f17-108">使用する仕入帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="a2f17-109">登録を開いて経費明細行を入力するには、**明細行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="a2f17-110">仕入先を選択してください。</span><span class="sxs-lookup"><span data-stu-id="a2f17-110">Select a vendor.</span></span> <span data-ttu-id="a2f17-111">たとえば、`US-104` を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="a2f17-112">**請求書**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="a2f17-113">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="a2f17-114">**貸方**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="a2f17-115">**承認者**フィールドで、ドロップダウン メニューから承認者を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="a2f17-116">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="a2f17-117">請求書の承認</span><span class="sxs-lookup"><span data-stu-id="a2f17-117">Approve an invoice</span></span>
1. <span data-ttu-id="a2f17-118">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 請求書の承認**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="a2f17-119">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-119">Select **New**.</span></span>
3. <span data-ttu-id="a2f17-120">使用する請求書承認仕訳帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="a2f17-121">**明細行**を選択すると、承認する請求書を選択できるページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2f17-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="a2f17-122">**伝票の検索**を選択すると、承認待ちの請求書をすべて表示します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="a2f17-123">作成した請求書をマークし、**選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2f17-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="a2f17-124">上の手順で選択した伝票は、選択後にこのリストに移動されます。</span><span class="sxs-lookup"><span data-stu-id="a2f17-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="a2f17-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-125">Select **OK**.</span></span>
8. <span data-ttu-id="a2f17-126">請求書に経費勘定を追加するには、**勘定番号**フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="a2f17-127">勘定番号を入力し、Tab キーでこのフィールドから移動します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="a2f17-128">たとえば、「`600120`」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="a2f17-129">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f17-129">Select **Post**.</span></span>
11. <span data-ttu-id="a2f17-130">転記されたエントリを表示するには、**伝票**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2f17-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="a2f17-131">承認保留中の請求書の勘定は、取消されて実際の経費勘定に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="a2f17-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  
