---
title: "取消による減価償却の影響"
description: "この記事は、固定資産トランザクションの取消の潜在的な影響について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fbef7cb9a9fb18809dff96d4a44454d0dc6a31fc
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="8606d-103">取消による減価償却の影響</span><span class="sxs-lookup"><span data-stu-id="8606d-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8606d-104">この記事は、固定資産トランザクションの取消の潜在的な影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="8606d-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="8606d-105">固定資産トランザクション、および固定資産に関連付けられたトランザクションを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="8606d-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="8606d-106">また、取り消したトランザクションを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="8606d-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="8606d-107">資産の帳簿に最後に転記されたトランザクションではないトランザクションの取消または無効化ができます。</span><span class="sxs-lookup"><span data-stu-id="8606d-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="8606d-108">最初に、減価償却トランザクションが、取消の対象の減価償却トランザクションの後に転記されたかどうかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8606d-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="8606d-109">これは、トランザクションを取り消すときに、減価償却の再計算が行われないためです。</span><span class="sxs-lookup"><span data-stu-id="8606d-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="8606d-110">したがって、例で示すように、減価償却は、取消後、多くの場合、過大または過小になることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="8606d-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="8606d-111">トランザクションを取り消したときに減価償却が正確であるようにするために、減価償却が再計算されないことを伝えるメッセージが表示された場合は、取消を続行しないでください。</span><span class="sxs-lookup"><span data-stu-id="8606d-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="8606d-112">代わりに、取消の対象の減価償却トランザクションの後に転記された減価償却トランザクションを先に取り消してから、取消を続けます。</span><span class="sxs-lookup"><span data-stu-id="8606d-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="8606d-113">このようにすると、減価償却の再計算に関する警告が表示されず、取消を続けることができます。</span><span class="sxs-lookup"><span data-stu-id="8606d-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="8606d-114">次の例では、先に減価償却トランザクションを取り消さずに、メッセージを無視して処理を続けた場合に行われる計算を示します。</span><span class="sxs-lookup"><span data-stu-id="8606d-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="8606d-115">例 1:  減価償却が過大になる</span><span class="sxs-lookup"><span data-stu-id="8606d-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="8606d-116">ある資産には、5 年の耐用期間と定額法での減価償却 (60 減価償却期間) が設定されています。</span><span class="sxs-lookup"><span data-stu-id="8606d-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="8606d-117">この例では、減価償却が過大になります。</span><span class="sxs-lookup"><span data-stu-id="8606d-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="8606d-118">資産トランザクション履歴</span><span class="sxs-lookup"><span data-stu-id="8606d-118">Asset transaction history</span></span>

| <span data-ttu-id="8606d-119">日付</span><span class="sxs-lookup"><span data-stu-id="8606d-119">Date</span></span>       | <span data-ttu-id="8606d-120">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="8606d-120">Transaction type</span></span>                                                          | <span data-ttu-id="8606d-121">金額</span><span class="sxs-lookup"><span data-stu-id="8606d-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="8606d-122">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8606d-122">January 1</span></span>  | <span data-ttu-id="8606d-123">取得</span><span class="sxs-lookup"><span data-stu-id="8606d-123">Acquisition</span></span>                                                               | <span data-ttu-id="8606d-124">59,000.00</span><span class="sxs-lookup"><span data-stu-id="8606d-124">59,000.00</span></span>                                 |
| <span data-ttu-id="8606d-125">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8606d-125">January 1</span></span>  | <span data-ttu-id="8606d-126">取得原価調整</span><span class="sxs-lookup"><span data-stu-id="8606d-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="8606d-127">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8606d-127">1,000.00</span></span>                                  |
| <span data-ttu-id="8606d-128">1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8606d-128">January 31</span></span> | <span data-ttu-id="8606d-129">減価償却 (1 期減価償却の提案を使用して計算)</span><span class="sxs-lookup"><span data-stu-id="8606d-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="8606d-130">1,000.00 計算: 簿価額 (59,000 + 1,000) / 残りの減価償却期間数 (60)</span><span class="sxs-lookup"><span data-stu-id="8606d-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="8606d-131">取消アクション</span><span class="sxs-lookup"><span data-stu-id="8606d-131">Reversal action</span></span>

| <span data-ttu-id="8606d-132">日付</span><span class="sxs-lookup"><span data-stu-id="8606d-132">Date</span></span>      | <span data-ttu-id="8606d-133">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="8606d-133">Transaction type</span></span>                | <span data-ttu-id="8606d-134">金額</span><span class="sxs-lookup"><span data-stu-id="8606d-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="8606d-135">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8606d-135">January 1</span></span> | <span data-ttu-id="8606d-136">取得原価調整取消</span><span class="sxs-lookup"><span data-stu-id="8606d-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="8606d-137">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8606d-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="8606d-138">減価償却の影響</span><span class="sxs-lookup"><span data-stu-id="8606d-138">Depreciation effect</span></span>

| <span data-ttu-id="8606d-139">日付</span><span class="sxs-lookup"><span data-stu-id="8606d-139">Date</span></span>        | <span data-ttu-id="8606d-140">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="8606d-140">Transaction type</span></span>        | <span data-ttu-id="8606d-141">金額</span><span class="sxs-lookup"><span data-stu-id="8606d-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8606d-142">2 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8606d-142">February 28</span></span> | <span data-ttu-id="8606d-143">償却 (提案)</span><span class="sxs-lookup"><span data-stu-id="8606d-143">Depreciation (proposal)</span></span> | <span data-ttu-id="8606d-144">983.05 計算: 簿価額 (59,000 - 1,000 減価償却) / 残りの減価償却期間数 (59)</span><span class="sxs-lookup"><span data-stu-id="8606d-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="8606d-145">減価償却は 16.95 (1000 - 983.05) だけ過大です。</span><span class="sxs-lookup"><span data-stu-id="8606d-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="8606d-146">例 2 : 減価償却が過小になる</span><span class="sxs-lookup"><span data-stu-id="8606d-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="8606d-147">ある資産には、5 年の耐用期間と定額法での減価償却 (60 減価償却期間) が設定されています。</span><span class="sxs-lookup"><span data-stu-id="8606d-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="8606d-148">この例では、減価償却が過小になります。</span><span class="sxs-lookup"><span data-stu-id="8606d-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="8606d-149">資産トランザクション履歴</span><span class="sxs-lookup"><span data-stu-id="8606d-149">Asset transaction history</span></span>

| <span data-ttu-id="8606d-150">日付</span><span class="sxs-lookup"><span data-stu-id="8606d-150">Date</span></span>       | <span data-ttu-id="8606d-151">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="8606d-151">Transaction type</span></span>                                                          | <span data-ttu-id="8606d-152">金額</span><span class="sxs-lookup"><span data-stu-id="8606d-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="8606d-153">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8606d-153">January 1</span></span>  | <span data-ttu-id="8606d-154">取得</span><span class="sxs-lookup"><span data-stu-id="8606d-154">Acquisition</span></span>                                                               | <span data-ttu-id="8606d-155">59,000.00</span><span class="sxs-lookup"><span data-stu-id="8606d-155">59,000.00</span></span>                                   |
| <span data-ttu-id="8606d-156">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8606d-156">January 1</span></span>  | <span data-ttu-id="8606d-157">評価減調整</span><span class="sxs-lookup"><span data-stu-id="8606d-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="8606d-158">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8606d-158">1,000.00</span></span>                                    |
| <span data-ttu-id="8606d-159">1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8606d-159">January 31</span></span> | <span data-ttu-id="8606d-160">減価償却 (1 期減価償却の提案を使用して計算)</span><span class="sxs-lookup"><span data-stu-id="8606d-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="8606d-161">966.67 計算: 簿価額 (59,000 - 1,000) / 残りの減価償却期間数 (60)</span><span class="sxs-lookup"><span data-stu-id="8606d-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="8606d-162">取消アクション</span><span class="sxs-lookup"><span data-stu-id="8606d-162">Reversal action</span></span>

| <span data-ttu-id="8606d-163">日付</span><span class="sxs-lookup"><span data-stu-id="8606d-163">Date</span></span>      | <span data-ttu-id="8606d-164">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="8606d-164">Transaction type</span></span>               | <span data-ttu-id="8606d-165">金額</span><span class="sxs-lookup"><span data-stu-id="8606d-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="8606d-166">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8606d-166">January 1</span></span> | <span data-ttu-id="8606d-167">評価減調整取消</span><span class="sxs-lookup"><span data-stu-id="8606d-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="8606d-168">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8606d-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="8606d-169">減価償却の影響</span><span class="sxs-lookup"><span data-stu-id="8606d-169">Depreciation effect</span></span>

| <span data-ttu-id="8606d-170">日付</span><span class="sxs-lookup"><span data-stu-id="8606d-170">Date</span></span>        | <span data-ttu-id="8606d-171">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="8606d-171">Transaction type</span></span>        | <span data-ttu-id="8606d-172">金額</span><span class="sxs-lookup"><span data-stu-id="8606d-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8606d-173">2 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8606d-173">February 28</span></span> | <span data-ttu-id="8606d-174">償却 (提案)</span><span class="sxs-lookup"><span data-stu-id="8606d-174">Depreciation (proposal)</span></span> | <span data-ttu-id="8606d-175">983.62 計算: 簿価額 (59,000 - 966.67 減価償却) / 残りの減価償却期間数 (59)</span><span class="sxs-lookup"><span data-stu-id="8606d-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="8606d-176">減価償却は 16.95 (983.62 - 966.67) だけ過小です。</span><span class="sxs-lookup"><span data-stu-id="8606d-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="8606d-177">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="8606d-177">Additional resources</span></span>
--------

[<span data-ttu-id="8606d-178">固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="8606d-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)




