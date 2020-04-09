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
ms.openlocfilehash: 788397b5c9a3f42e373f7cdad256c1ee3d058e57
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143768"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="0eda6-103">承認仕訳帳を使用した買掛金勘定への請求書データの入力</span><span class="sxs-lookup"><span data-stu-id="0eda6-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0eda6-104">このトピックでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="0eda6-105">請求書の作成と転記</span><span class="sxs-lookup"><span data-stu-id="0eda6-105">Create and post and invoice</span></span>
1. <span data-ttu-id="0eda6-106">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 仕入帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="0eda6-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-107">Select **New**.</span></span>
3. <span data-ttu-id="0eda6-108">使用する仕入帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="0eda6-109">登録を開いて経費明細行を入力するには、**明細行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="0eda6-110">仕入先を選択してください。</span><span class="sxs-lookup"><span data-stu-id="0eda6-110">Select a vendor.</span></span> <span data-ttu-id="0eda6-111">たとえば、`US-104` を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="0eda6-112">**請求書**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="0eda6-113">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="0eda6-114">**貸方**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="0eda6-115">**承認者**フィールドで、ドロップダウン メニューから承認者を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="0eda6-116">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="0eda6-117">請求書の承認</span><span class="sxs-lookup"><span data-stu-id="0eda6-117">Approve an invoice</span></span>
1. <span data-ttu-id="0eda6-118">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 請求書の承認**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="0eda6-119">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-119">Select **New**.</span></span>
3. <span data-ttu-id="0eda6-120">使用する請求書承認仕訳帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="0eda6-121">**明細行**を選択すると、承認する請求書を選択できるページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0eda6-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="0eda6-122">**伝票の検索**を選択すると、承認待ちの請求書をすべて表示します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="0eda6-123">作成した請求書をマークし、**選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0eda6-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="0eda6-124">上の手順で選択した伝票は、選択後にこのリストに移動されます。</span><span class="sxs-lookup"><span data-stu-id="0eda6-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="0eda6-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-125">Select **OK**.</span></span>
8. <span data-ttu-id="0eda6-126">請求書に経費勘定を追加するには、**勘定番号**フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="0eda6-127">勘定番号を入力し、Tab キーでこのフィールドから移動します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="0eda6-128">たとえば、「`600120`」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="0eda6-129">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0eda6-129">Select **Post**.</span></span>
11. <span data-ttu-id="0eda6-130">転記されたエントリを表示するには、**伝票**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0eda6-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="0eda6-131">承認保留中の請求書の勘定は、取消されて実際の経費勘定に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="0eda6-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

