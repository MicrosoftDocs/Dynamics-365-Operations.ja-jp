---
title: "信用保証状"
description: "この記事は、信用保証状に関する情報を提供します。 信用保証状で銀行は、銀行の顧客がある者に対して支払や義務を履行しない場合に、銀行がその者に特定の金額を支払うことに合意します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c2072c571d584185e867f221c24dc44cdbad1dd6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="letters-of-guarantee"></a><span data-ttu-id="05537-104">信用保証状</span><span class="sxs-lookup"><span data-stu-id="05537-104">Letters of guarantee</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05537-105">この記事は、信用保証状に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="05537-105">This article provides information about letters of guarantee.</span></span> <span data-ttu-id="05537-106">信用保証状で銀行は、銀行の顧客がある者に対して支払や義務を履行しない場合に、銀行がその者に特定の金額を支払うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="05537-106">In a letter of guarantee, a bank agrees to pay a specific amount of money to a person if one of the bank's customers defaults on a payment or obligation to that person.</span></span> 

<span data-ttu-id="05537-107">信用保証状とは、銀行の顧客 (第一債務者) が第三者 (受益者) に対して支払や義務を履行しない場合に、銀行 (保証人) が受益者に設定金額を支払う契約です。</span><span class="sxs-lookup"><span data-stu-id="05537-107">A letter of guarantee is an agreement by a bank (the guarantor) to pay a set amount of money to some person (the beneficiary) if a bank customer (the principal) defaults on a payment or an obligation to the beneficiary.</span></span> <span data-ttu-id="05537-108">信用保証状は譲渡できません。</span><span class="sxs-lookup"><span data-stu-id="05537-108">Letters of guarantee aren't transferable.</span></span> <span data-ttu-id="05537-109">また、契約に記名された受益者にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="05537-109">They apply only to the beneficiary who is named in the agreement.</span></span> <span data-ttu-id="05537-110">第一債務者は、契約条項に従って信用保証状の金額の増額または減額を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="05537-110">The principal can request an increase or decrease in the value of a letter of guarantee, subject to the terms of the agreement.</span></span> 

<span data-ttu-id="05537-111">信用保証状を清算するには、受益者が元の信用保証状を提出し、第一債務者の債務不履行を有効期限前に銀行に通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05537-111">To liquidate a letter of guarantee, the beneficiary must submit the original letter of guarantee and inform the bank of the principal’s default before the expiration date.</span></span> <span data-ttu-id="05537-112">その後、銀行は、信用保証状の支払条件に従って、受益者の勘定に対して未払金額を支払います。</span><span class="sxs-lookup"><span data-stu-id="05537-112">The bank then pays the amount that is due to the beneficiary's account, according to the terms in the letter of guarantee.</span></span> <span data-ttu-id="05537-113">銀行は、支払の割合を保証金として留保します。</span><span class="sxs-lookup"><span data-stu-id="05537-113">The bank reserves a percentage of the payment as a margin.</span></span> <span data-ttu-id="05537-114">割合は、契約条項で合意および指定されます。</span><span class="sxs-lookup"><span data-stu-id="05537-114">The percentage is agreed upon and specified in the terms of the agreement.</span></span> 

<span data-ttu-id="05537-115">信用保証状の目的を追跡するコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="05537-115">You can create a code to track the purpose of a letter of guarantee.</span></span> <span data-ttu-id="05537-116">督促状がキャンセルされた場合、信用保証状に関連付けることができる理由も指定できます。</span><span class="sxs-lookup"><span data-stu-id="05537-116">You can also specify the reasons that can be associated with a letter of guarantee when the letter is canceled.</span></span> <span data-ttu-id="05537-117">**支払目的コード** および **銀行の理由** ページで目的コードと銀行の理由を表示できます。</span><span class="sxs-lookup"><span data-stu-id="05537-117">You can view the purpose codes and bank reasons on the **Payment purpose codes** and **Bank reasons** pages.</span></span> 

<span data-ttu-id="05537-118">**信用保証状** ページを使用して、次のタスクを完成します。</span><span class="sxs-lookup"><span data-stu-id="05537-118">You can use the **Letter of guarantee** page to complete these tasks:</span></span>

-   <span data-ttu-id="05537-119">正しい元帳エントリを作成し、手動入力を不要にします。</span><span class="sxs-lookup"><span data-stu-id="05537-119">Create correct ledger entries, and eliminate manual entry.</span></span>
-   <span data-ttu-id="05537-120">すべての金銭的トランザクションと非金銭的トランザクションを記録し、信用保証状の残高を追跡します。</span><span class="sxs-lookup"><span data-stu-id="05537-120">Record all monetary and nonmonetary transactions, and track balances of letters of guarantee.</span></span>
-   <span data-ttu-id="05537-121">信用保証状のステータスおよび有効期限を記録し、追跡します。</span><span class="sxs-lookup"><span data-stu-id="05537-121">Record and track the status and expiration of letters of guarantee.</span></span>
-   <span data-ttu-id="05537-122">信用保証状を保有する銀行の一覧を示すレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="05537-122">Generate a report that lists the banks that are holding letters of guarantee.</span></span>

<span data-ttu-id="05537-123">次の表では、信用保証状で実行できるアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="05537-123">The following table describes the actions that you can perform on a letter of guarantee.</span></span>

| <span data-ttu-id="05537-124">アクション</span><span class="sxs-lookup"><span data-stu-id="05537-124">Action</span></span>              | <span data-ttu-id="05537-125">目的</span><span class="sxs-lookup"><span data-stu-id="05537-125">Purpose</span></span>                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05537-126">銀行に送信</span><span class="sxs-lookup"><span data-stu-id="05537-126">Submit to bank</span></span>      | <span data-ttu-id="05537-127">信用保証状の要求を銀行に送信します。</span><span class="sxs-lookup"><span data-stu-id="05537-127">Submit the letter of guarantee request to the bank.</span></span>                                                                       |
| <span data-ttu-id="05537-128">銀行から受信</span><span class="sxs-lookup"><span data-stu-id="05537-128">Receive from bank</span></span>   | <span data-ttu-id="05537-129">銀行が送信された要求に合意すると、銀行から信用保証状を回収します。</span><span class="sxs-lookup"><span data-stu-id="05537-129">After the bank agrees to the submitted request, collect the letter of guarantee from the bank.</span></span>                            |
| <span data-ttu-id="05537-130">受益者に渡す</span><span class="sxs-lookup"><span data-stu-id="05537-130">Give to beneficiary</span></span> | <span data-ttu-id="05537-131">銀行から信用保証状を受信した後に、信用保証状を受益者に付与します。</span><span class="sxs-lookup"><span data-stu-id="05537-131">After you receive the letter of guarantee from the bank, provide the letter of guarantee to the beneficiary.</span></span>              |
| <span data-ttu-id="05537-132">値の増加</span><span class="sxs-lookup"><span data-stu-id="05537-132">Increase value</span></span>      | <span data-ttu-id="05537-133">受益者と第一債務者が合意した場合は、金銭価値を増やします。</span><span class="sxs-lookup"><span data-stu-id="05537-133">If the beneficiary and the principal agree, increase the monetary value.</span></span>                                                  |
| <span data-ttu-id="05537-134">値の減少</span><span class="sxs-lookup"><span data-stu-id="05537-134">Decrease value</span></span>      | <span data-ttu-id="05537-135">受益者と第一債務者が合意した場合は、金銭価値を減らします。</span><span class="sxs-lookup"><span data-stu-id="05537-135">If the beneficiary and the principal agree, decrease the monetary value.</span></span>                                                  |
| <span data-ttu-id="05537-136">拡張</span><span class="sxs-lookup"><span data-stu-id="05537-136">Extend</span></span>              | <span data-ttu-id="05537-137">信用保証状を受益者に付与した後、延長が必要であれば、有効期間を延長します。</span><span class="sxs-lookup"><span data-stu-id="05537-137">After you provide the letter of guarantee to the beneficiary, extend the period of validity, if an extension is required.</span></span> |
| <span data-ttu-id="05537-138">キャンセル</span><span class="sxs-lookup"><span data-stu-id="05537-138">Cancel</span></span>              | <span data-ttu-id="05537-139">信用保証状が要求された目的が適用されない場合は、契約をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="05537-139">When the purpose that the letter of guarantee was requested for no longer applies, cancel the agreement.</span></span>                  |
| <span data-ttu-id="05537-140">清算する</span><span class="sxs-lookup"><span data-stu-id="05537-140">Liquidate</span></span>           | <span data-ttu-id="05537-141">受益者が銀行に信用保証状を提示した場合、信用保証状を清算します。</span><span class="sxs-lookup"><span data-stu-id="05537-141">When the beneficiary presents the letter of guarantee to the bank, cash out the letter of guarantee.</span></span>                      |


<span data-ttu-id="05537-142">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="05537-142">For more information, see the following topics:</span></span>

[<span data-ttu-id="05537-143">信用保証状のトランザクション</span><span class="sxs-lookup"><span data-stu-id="05537-143">Letter of guarantee transaction</span></span>](tasks/letter-guarantee-transaction.md)

[<span data-ttu-id="05537-144">信用保証状についての銀行融資と転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="05537-144">Set up bank facilities and posting profiles for letters of guarantee</span></span>](tasks/set-up-bank-facilities-posting-profiles.md)



