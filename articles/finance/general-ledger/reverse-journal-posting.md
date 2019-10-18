---
title: 仕訳帳の転記の取消
description: このトピックでは、伝票トランザクション リストまたは財務仕訳帳から伝票を取り消けせるようにする能力について説明します。
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248588"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="5e314-103">仕訳帳の転記の取消</span><span class="sxs-lookup"><span data-stu-id="5e314-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e314-104">このトピックでは、仕訳帳全体、またはその発生元に関係なく伝票トランザクション リストから 1 つ以上の伝票を取り消すことができるようにする Microsoft Dynamics 365 Finance 能力について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e314-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="5e314-105">仕訳帳の取り消し</span><span class="sxs-lookup"><span data-stu-id="5e314-105">Reversing journals</span></span>

<span data-ttu-id="5e314-106">仕訳帳明細行は個別に取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="5e314-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="5e314-107">仕訳帳転記の取消により、財務仕訳帳全体を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="5e314-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="5e314-108">仕訳帳を取り消すには:</span><span class="sxs-lookup"><span data-stu-id="5e314-108">To reverse a journal:</span></span> 
- <span data-ttu-id="5e314-109">財務仕訳帳を開き、転記された仕訳帳のフィルター処理を行います</span><span class="sxs-lookup"><span data-stu-id="5e314-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="5e314-110">ページ上部の取消メニューをクリックします</span><span class="sxs-lookup"><span data-stu-id="5e314-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="5e314-111">伝票および伝票明細行の合計数が、取り消される明細行の合計金額と共に表示されます</span><span class="sxs-lookup"><span data-stu-id="5e314-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="5e314-112">既存のトランザクションの日付を使用する場合ははいを選択し、新しく入力する場合はいいえを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e314-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="5e314-113">場合によっては、元のトランザクションの期間が終了していることがあり、取消のために新しいトランザクション日付を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e314-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="5e314-114">いいえを選択した場合、取消のためにトランザクションの日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e314-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="5e314-115">取消トランザクションに追加するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="5e314-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="5e314-116">取消ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="5e314-116">Click the Reverse button</span></span>

<span data-ttu-id="5e314-117">トランザクションは取り消されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="5e314-118">伝票明細行の数が 100 行を超える場合、バッチ処理を使用して取消プロセスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="5e314-119">実行されたバッチ ジョブのコメントを表示することにより、取消の結果を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="5e314-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="5e314-120">失敗はすべてバッチ ジョブ履歴に記録されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="5e314-121">伝票明細行の数が 100 行以下である場合、取消プロセスがすぐに実行されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="5e314-122">結果は、取消ができなかったすべての伝票および取消ができなかった理由を表示するダイアログ内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="5e314-123">OK をクリックしてダイアログを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5e314-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="5e314-124">伝票トランザクション リストから伝票を取り消します。</span><span class="sxs-lookup"><span data-stu-id="5e314-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="5e314-125">また、すべての補助元帳間で**伝票のトランザクション リスト**から伝票を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="5e314-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="5e314-126">さらに、一度に複数の伝票を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="5e314-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="5e314-127">複数の伝票を取り消すには:</span><span class="sxs-lookup"><span data-stu-id="5e314-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="5e314-128">ページ上部の取消メニューをクリックします</span><span class="sxs-lookup"><span data-stu-id="5e314-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="5e314-129">伝票および伝票明細行の合計数が、取り消される明細行の合計金額と共に表示されます</span><span class="sxs-lookup"><span data-stu-id="5e314-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="5e314-130">既存のトランザクションの日付を使用する場合ははいを選択し、新しく入力する場合はいいえを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e314-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="5e314-131">場合によっては、元のトランザクションの期間が終了していることがあり、取消のために新しいトランザクション日付を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e314-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="5e314-132">いいえを選択した場合、取消のためにトランザクションの日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e314-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="5e314-133">取消トランザクションに追加するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="5e314-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="5e314-134">取消ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="5e314-134">Click the Reverse button</span></span>

<span data-ttu-id="5e314-135">トランザクションは取り消されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="5e314-136">伝票明細行の数が 100 行を超える場合、バッチ処理を使用して取消プロセスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="5e314-137">実行されたバッチ ジョブのコメントを表示することにより、取消の結果を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="5e314-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="5e314-138">失敗はすべてバッチ ジョブ履歴に記録されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="5e314-139">伝票明細行の数が 100 行以下である場合、取消プロセスがすぐに実行されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="5e314-140">結果は、取消ができなかったすべての伝票および取消ができなかった理由を表示するダイアログ内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e314-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="5e314-141">OK をクリックしてダイアログを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5e314-141">Click on Ok to close the dialog.</span></span>

