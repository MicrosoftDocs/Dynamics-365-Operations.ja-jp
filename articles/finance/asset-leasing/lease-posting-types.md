---
title: リース転記タイプ
description: このトピックでは、資産のリース契約トランザクションに使用される転記タイプについて説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b79b02f7e241783d19a315ccff5bb6874a238c38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995421"
---
# <a name="lease-posting-types"></a><span data-ttu-id="943dc-103">リース転記タイプ</span><span class="sxs-lookup"><span data-stu-id="943dc-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="943dc-104">このトピックでは、資産のリース契約トランザクションに使用される転記タイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="943dc-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="943dc-105">リース資産</span><span class="sxs-lookup"><span data-stu-id="943dc-105">Lease asset</span></span>

<span data-ttu-id="943dc-106">この勘定は、使用権 (ROU) 資産に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="943dc-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="943dc-107">この勘定では、リースが最初に新しいリース会計標準によって認識されると借方に転記され、 Accounting Standards Codification Topic 842 (ASC 842) および International Financial Reporting Standard 16 (IFRS 16) の元、借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="943dc-108">変更されたリースの場合、この勘定は、変更によってリース負債が増加または減少したかどうかに応じて、借方または貸方になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="943dc-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="943dc-109">**仕訳入力の例:** 初期認識</span><span class="sxs-lookup"><span data-stu-id="943dc-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="943dc-110">**借方:** リース資産 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="943dc-111">**貸方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="943dc-112">リース負債</span><span class="sxs-lookup"><span data-stu-id="943dc-112">Lease liability</span></span>

<span data-ttu-id="943dc-113">この勘定は、新しい IFRS 16 および ASC 842 基準で支払が割引されるときに発生するリース負債に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="943dc-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="943dc-114">この勘定は、新しい標準でリースが最初に認識されたときに貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="943dc-115">リース支払を借方に転記し、未収利息の貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="943dc-116">**仕訳入力の例:** 初期認識</span><span class="sxs-lookup"><span data-stu-id="943dc-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="943dc-117">**借方:** リース資産 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="943dc-118">**貸方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="943dc-119">**仕訳入力の例:** 未収利息</span><span class="sxs-lookup"><span data-stu-id="943dc-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="943dc-120">**借方:** 支払利息 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="943dc-121">**貸方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="943dc-122">**仕訳入力の例:** リース支払</span><span class="sxs-lookup"><span data-stu-id="943dc-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="943dc-123">**借方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="943dc-124">**貸方:** 仕入先支払/リース支払 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="943dc-125">短期リース負債</span><span class="sxs-lookup"><span data-stu-id="943dc-125">Short-term lease liability</span></span>

<span data-ttu-id="943dc-126">この勘定は、短期のリース負債の再分類仕訳入力が転記されるときに、短期のリース負債に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="943dc-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="943dc-127">この勘定では、月の最後の日に償却スケジュールからの短期負債が貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="943dc-128">ただし、翌月の初日にも同じ金額が借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="943dc-129">**仕訳入力の例:** 短期的なリース負債の再分類</span><span class="sxs-lookup"><span data-stu-id="943dc-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="943dc-130">**借方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="943dc-131">**貸方:** 短期的なリース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="943dc-132">**借方:** 短期的なリース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="943dc-133">**貸方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="943dc-134">減価償却費</span><span class="sxs-lookup"><span data-stu-id="943dc-134">Depreciation expense</span></span>

<span data-ttu-id="943dc-135">この勘定は、IFRS 16、ASC 842 下の使用権資産、および IAS 17 と ASC 840 下のファイナンス リースに関連する使用権資産の減価償却に関連する経費に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="943dc-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="943dc-136">この勘定では、使用権資産が月ごとに償却されるときに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="943dc-137">**仕訳入力の例:** 未収減価償却</span><span class="sxs-lookup"><span data-stu-id="943dc-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="943dc-138">**借方:** 減価償却経費 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="943dc-139">**貸方:** 減価償却累計額 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="943dc-140">リース変更に伴う利益/損失</span><span class="sxs-lookup"><span data-stu-id="943dc-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="943dc-141">この勘定は、リース変更によって発生した利益または損失に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="943dc-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="943dc-142">リースの変更によって、使用権資産のキャリー額を超える金額が変更によってリース負債を低減した場合、リースの変更時にゲインが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="943dc-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="943dc-143">たとえば、リースには $150,000 のリース負債に対する現在のキャリー額と $100,000 の使用権資産のキャリー額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="943dc-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="943dc-144">リースが変更され、この変更により、$40,000 の将来の最小リース支払 (PVFMLP) の現在の値が新しくなります。</span><span class="sxs-lookup"><span data-stu-id="943dc-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="943dc-145">したがって、リース負債は $110,000 ($150,000 – $40,000) で借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="943dc-146">使用権資産が $100,000 にしかならないため、$110,000 が減少すると、資産が 0 (ゼロ) 以下に減少します。</span><span class="sxs-lookup"><span data-stu-id="943dc-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="943dc-147">したがって、会計のガイダンスでは、残余を利益勘定に記帳する必要があることが示されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="943dc-148">この場合、最終的な仕訳入力は、$110,000 に対するリース負債の借方、$100,000 のリース資産への貸方、および $10,000 に対する利益勘定になります。</span><span class="sxs-lookup"><span data-stu-id="943dc-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="943dc-149">**仕訳入力の例:** リース変更</span><span class="sxs-lookup"><span data-stu-id="943dc-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="943dc-150">**借方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="943dc-151">**貸方:** リース資産 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="943dc-152">**貸方:** 利益 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="943dc-153">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="943dc-153">Accumulated depreciation</span></span>

<span data-ttu-id="943dc-154">この勘定は、使用権資産の資産控除勘定に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="943dc-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="943dc-155">この勘定では、減価償却経費を転記するときに貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="943dc-156">**仕訳入力の例:** 未収減価償却</span><span class="sxs-lookup"><span data-stu-id="943dc-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="943dc-157">**借方:** 減価償却経費 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="943dc-158">**貸方:** 減価償却累計額 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="943dc-159">利益剰余金</span><span class="sxs-lookup"><span data-stu-id="943dc-159">Retained earnings</span></span>

<span data-ttu-id="943dc-160">この感情は留保利益に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="943dc-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="943dc-161">この勘定は、完全な振り返りメソッドを使用するか、または類型キャッチアップ オプション A メソッドを使用して、切り替え調整仕訳入力で借方または貸方に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="943dc-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="943dc-162">初期使用権資産とリース負債の差額が、留保収益に記帳されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="943dc-163">まれな場合ですが、リースの変更によって、使用権資産がリース負債に等しくなるように、財務に対するリースの分類が財務上から工程に変更される場合は、その利益がリースの変更によって影響を受けることがあります。</span><span class="sxs-lookup"><span data-stu-id="943dc-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="943dc-164">**仕訳入力の例:** 切り替えの調整 (完全な振り返りまたは累積キャッチアップ オプション A メソッド)</span><span class="sxs-lookup"><span data-stu-id="943dc-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="943dc-165">**借方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="943dc-166">**貸方:** リース資産 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="943dc-167">**貸方:** 留保利益 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="943dc-168">変動支払</span><span class="sxs-lookup"><span data-stu-id="943dc-168">Variable payment</span></span>

<span data-ttu-id="943dc-169">この勘定は、ASC 842、ASC 840、および IAS 17 リース下でのインデックスの再評価によって生成された変動リース支払に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="943dc-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="943dc-170">このリース支払スケジュールでは、変動支払は **変動支払** 列に含まれています。</span><span class="sxs-lookup"><span data-stu-id="943dc-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="943dc-171">変動支払を含む支払スケジュール明細行に対して請求書を作成するときに、この勘定は借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="943dc-172">**仕訳入力の例:** リース支払</span><span class="sxs-lookup"><span data-stu-id="943dc-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="943dc-173">**借方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="943dc-174">**借方:** 変動支払 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="943dc-175">**貸方:** 仕入先支払/リース支払 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="943dc-176">繰延賃料資産 (負債)</span><span class="sxs-lookup"><span data-stu-id="943dc-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="943dc-177">この勘定は、賃貸繰延扱いのリースによって生産される繰延賃料資産または負債に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="943dc-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="943dc-178">リース支払額がその期間の定額賃貸経費を超えている場合、この勘定では、請求書が繰延賃料料として転記されるときに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="943dc-179">リース支払が期間の定額の賃貸経費を下回っている場合は、貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="943dc-180">**仕訳入力の例:** リース支払 (繰延賃料扱いのリース)</span><span class="sxs-lookup"><span data-stu-id="943dc-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="943dc-181">**借方:** リース経費 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="943dc-182">**貸方:** 繰延賃料 (負債) XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="943dc-183">**貸方:** 仕入先支払/リース支払 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="943dc-184">リース経費</span><span class="sxs-lookup"><span data-stu-id="943dc-184">Lease expense</span></span>

<span data-ttu-id="943dc-185">リースが繰延賃料扱いのリースとして分類される場合、この勘定はリース経費に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="943dc-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="943dc-186">この勘定では、請求書が繰延賃料扱いリースに対して転記されるときに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="943dc-187">**仕訳入力の例:** リース支払 (繰延賃料扱いのリース)</span><span class="sxs-lookup"><span data-stu-id="943dc-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="943dc-188">**借方:** リース経費 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="943dc-189">**貸方:** 繰延賃料 (負債) XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="943dc-190">**貸方:** 仕入先支払/リース支払 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="943dc-191">減損経費</span><span class="sxs-lookup"><span data-stu-id="943dc-191">Impairment expense</span></span>

<span data-ttu-id="943dc-192">この勘定は、リースが減損された場合に対して転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="943dc-193">この勘定は借方に転記されますが、使用権資産勘定は直接貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="943dc-194">**仕訳入力の例:** リース支払</span><span class="sxs-lookup"><span data-stu-id="943dc-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="943dc-195">**借方:** 減損経費 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="943dc-196">**貸方:** 使用権資産 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="943dc-197">リース支払</span><span class="sxs-lookup"><span data-stu-id="943dc-197">Lease payment</span></span>

<span data-ttu-id="943dc-198">**支払先仕入先** パラメータがオフになっている場合に、勘定に対して転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="943dc-199">このパラメータがオフになっている場合、この勘定は仕入先の支払の代わりに貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="943dc-200">**仕訳入力の例:** リース支払</span><span class="sxs-lookup"><span data-stu-id="943dc-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="943dc-201">**借方:** リース負債 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="943dc-202">**貸方:** リース支払 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="943dc-203">経費タイプの転記</span><span class="sxs-lookup"><span data-stu-id="943dc-203">Expense type postings</span></span>

<span data-ttu-id="943dc-204">経費タイプごとに選択された勘定は、その経費タイプの支払が生成されるときに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="943dc-205">たとえば、**保険** 経費タイプに指定されている勘定は、保険経費の履行コスト スケジュールから請求書または支払仕訳入力が作成されるたびに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="943dc-206">**仕訳入力の例:** 保険支払</span><span class="sxs-lookup"><span data-stu-id="943dc-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="943dc-207">**借方:** 保険経費タイプの勘定 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="943dc-208">**貸方:** オフセット勘定 XXX</span><span class="sxs-lookup"><span data-stu-id="943dc-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="943dc-209">オフセット勘定は、履行コスト支払スケジュールの明細行のリース レベルで選択されます。</span><span class="sxs-lookup"><span data-stu-id="943dc-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="943dc-210">このオフセット勘定は、仕入先に関連付けるか、勘定科目で関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="943dc-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
