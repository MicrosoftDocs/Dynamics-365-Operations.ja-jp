---
title: 仕訳帳の転記の取消
description: このトピックでは、伝票トランザクション リストまたは財務仕訳帳から伝票を取り消けせるようにする能力について説明します。
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3244d857a9135249130672501f8b766ff9a0680
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980941"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="aa165-103">仕訳帳の転記の取消</span><span class="sxs-lookup"><span data-stu-id="aa165-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa165-104">このトピックでは、仕訳帳全体、またはその発生元に関係なく伝票トランザクション リストから 1 つ以上の伝票を取り消すことができるようにする Microsoft Dynamics 365 Finance の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa165-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="aa165-105">仕訳帳の取り消し</span><span class="sxs-lookup"><span data-stu-id="aa165-105">Reversing journals</span></span>

<span data-ttu-id="aa165-106">仕訳帳明細行は個別に取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="aa165-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="aa165-107">仕訳帳転記の取消により、財務仕訳帳全体を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="aa165-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="aa165-108">仕訳帳を取り消すには:</span><span class="sxs-lookup"><span data-stu-id="aa165-108">To reverse a journal:</span></span> 

- <span data-ttu-id="aa165-109">財務仕訳帳を開き、転記された仕訳帳のフィルター処理を行います。</span><span class="sxs-lookup"><span data-stu-id="aa165-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="aa165-110">ページ上部の**取消**メニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa165-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="aa165-111">伝票および伝票明細行の合計数が、取り消される明細行の合計金額と共に表示されます</span><span class="sxs-lookup"><span data-stu-id="aa165-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="aa165-112">既存のトランザクションの日付を使用する場合は**はい**を選択し、新しく入力する場合は**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa165-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="aa165-113">場合によっては、元のトランザクションの期間が終了していることがあり、取消のために新しいトランザクション日付を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa165-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="aa165-114">**いいえ**を選択した場合、取消のためにトランザクションの日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="aa165-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="aa165-115">取消トランザクションに追加するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="aa165-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="aa165-116">**取消**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa165-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="aa165-117">トランザクションは取り消されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="aa165-118">伝票に 100 行を超える明細行がある場合、バッチ処理を使用して取消プロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="aa165-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="aa165-119">バッチ ジョブのコメントを表示することにより、結果を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="aa165-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="aa165-120">取消が行われなかったトランザクションはすべて、バッチ ジョブの履歴に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="aa165-121">伝票に 100 行以下の明細行がある場合、取消プロセスがすぐに実行されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="aa165-122">結果は、取消ができなかった理由にしたがって、取消ができなかったすべての伝票を表示するダイアログ ボックス内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="aa165-123">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aa165-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="aa165-124">伝票トランザクション リストから伝票を取り消します。</span><span class="sxs-lookup"><span data-stu-id="aa165-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="aa165-125">また、すべての補助元帳間で**伝票のトランザクション リスト**から伝票を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="aa165-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="aa165-126">さらに、一度に複数の伝票を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="aa165-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="aa165-127">複数の伝票を取り消すには:</span><span class="sxs-lookup"><span data-stu-id="aa165-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="aa165-128">ページ上部の**取消**メニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa165-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="aa165-129">伝票および伝票明細行の合計数が、取り消される明細行の合計金額と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="aa165-130">既存のトランザクションの日付を使用する場合は**はい**を選択し、新しく入力する場合は**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa165-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="aa165-131">場合によっては、元のトランザクションの期間が終了していることがあり、取消を行うために新しいトランザクション日付を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa165-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="aa165-132">**いいえ**を選択した場合、取消のためにトランザクションの日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="aa165-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="aa165-133">取消トランザクションについて説明するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="aa165-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="aa165-134">**取消**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa165-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="aa165-135">トランザクションは取り消されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="aa165-136">100 行を超える伝票明細行がある場合、バッチ処理を使用して取消プロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="aa165-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="aa165-137">バッチ ジョブのコメントを表示することにより、結果を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="aa165-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="aa165-138">取消が行われなかったトランザクションはすべて、バッチ ジョブの履歴に記録されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="aa165-139">伝票明細行の数が 100 行以下である場合、取消プロセスがすぐに実行されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="aa165-140">結果は、取消ができなかった理由にしたがって、取消ができなかったすべての伝票を表示するダイアログ ボックス内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa165-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="aa165-141">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aa165-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="aa165-142">トランザクションを取り消すことができるのは、取消のためのビジネス ルールに合致している場合だけです。</span><span class="sxs-lookup"><span data-stu-id="aa165-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="aa165-143">このトピックで説明されている機能を使用して仕入先支払を取り消すことはできません。</span><span class="sxs-lookup"><span data-stu-id="aa165-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="aa165-144">仕入先支払は、[仕入先支払の取消](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment) に一覧表示されている手順に従って取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa165-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

