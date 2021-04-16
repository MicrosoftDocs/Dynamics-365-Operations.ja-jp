---
title: デュアル レポート
description: このトピックでは、International Financial Reporting Standard (国際会計基準 - IFRS) レポートと資産のリースにおける法定報告の要件を満たす方法を、例を挙げて説明します。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815983"
---
# <a name="dual-reporting"></a><span data-ttu-id="db4f9-103">二重レポート</span><span class="sxs-lookup"><span data-stu-id="db4f9-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db4f9-104">このトピックでは、International Financial Reporting Standard (国際会計基準 - IFRS) レポートと資産のリースにおける法定報告の要件を満たす方法を、例を挙げて説明します。</span><span class="sxs-lookup"><span data-stu-id="db4f9-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="db4f9-105">Microsoft Dynamics 365 Finance の転記階層に関する知識が必要であり、ここで挙げる例を簡単に理解することができます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="db4f9-106">例</span><span class="sxs-lookup"><span data-stu-id="db4f9-106">Example</span></span>

<span data-ttu-id="db4f9-107">以下の例では、イタリアの法定報告に基づき、現金基準法と IFRS の両方の報告方法を用いてリースを会計処理しています。</span><span class="sxs-lookup"><span data-stu-id="db4f9-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="db4f9-108">この会社では、イタリアの法的要件と IFRS 16 号の要件の両方について、3 冊の帳簿を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db4f9-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="db4f9-109">IFRS 16 号には 1 冊の帳簿が必要であり、法的要件には 1 冊の帳簿が必要であり、法的な転記を自動的に取り消すには、1 冊の帳簿が必要です。</span><span class="sxs-lookup"><span data-stu-id="db4f9-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="db4f9-110">この帳簿は、次の表に示すように設定されています。</span><span class="sxs-lookup"><span data-stu-id="db4f9-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="db4f9-111">**IFRS 16 号の帳簿**</span><span class="sxs-lookup"><span data-stu-id="db4f9-111">**IFRS 16 book**</span></span>

<span data-ttu-id="db4f9-112">IFRS 16 号の帳簿は、IFRS 16 号の勘定の標準に準拠するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="db4f9-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="db4f9-113">このドキュメントに記載されているすべての入力は、カスタム レイヤーに転記されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="db4f9-114">氏名</span><span class="sxs-lookup"><span data-stu-id="db4f9-114">Name</span></span>                                    | <span data-ttu-id="db4f9-115">説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="db4f9-116">帳簿タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-116">Book type</span></span>                               | <span data-ttu-id="db4f9-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="db4f9-117">IFRS 16</span></span>        |
| <span data-ttu-id="db4f9-118">帳簿の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-118">Book description</span></span>                        | <span data-ttu-id="db4f9-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="db4f9-119">IFRS 16</span></span>        |
| <span data-ttu-id="db4f9-120">転記階層</span><span class="sxs-lookup"><span data-stu-id="db4f9-120">Posting Layer</span></span>                           | <span data-ttu-id="db4f9-121">カスタム レイヤー 1</span><span class="sxs-lookup"><span data-stu-id="db4f9-121">Custom layer 1</span></span> |
| <span data-ttu-id="db4f9-122">リース タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-122">Lease Type</span></span>                              | <span data-ttu-id="db4f9-123">Finance</span><span class="sxs-lookup"><span data-stu-id="db4f9-123">Finance</span></span>        |
| <span data-ttu-id="db4f9-124">会計フレームワーク</span><span class="sxs-lookup"><span data-stu-id="db4f9-124">Accounting Framework</span></span>                    | <span data-ttu-id="db4f9-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="db4f9-125">IFRS 16</span></span>        |
| <span data-ttu-id="db4f9-126">リース期間 / 耐用年数の設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="db4f9-127">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-127">0.00</span></span>           |
| <span data-ttu-id="db4f9-128">現在の価値 / 資産の公正価値の設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="db4f9-129">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-129">0.00</span></span>           |
| <span data-ttu-id="db4f9-130">短期的しきい値</span><span class="sxs-lookup"><span data-stu-id="db4f9-130">Short-term threshold</span></span>                    | <span data-ttu-id="db4f9-131">12</span><span class="sxs-lookup"><span data-stu-id="db4f9-131">12</span></span>             |
| <span data-ttu-id="db4f9-132">少額しきい値</span><span class="sxs-lookup"><span data-stu-id="db4f9-132">Low Value Threshold</span></span>                     | <span data-ttu-id="db4f9-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-133">5,000.00</span></span>       |
| <span data-ttu-id="db4f9-134">仕入先への支払い</span><span class="sxs-lookup"><span data-stu-id="db4f9-134">Pay to Vendor</span></span>                           | <span data-ttu-id="db4f9-135">なし</span><span class="sxs-lookup"><span data-stu-id="db4f9-135">No</span></span>             |

<span data-ttu-id="db4f9-136">**法定帳簿**</span><span class="sxs-lookup"><span data-stu-id="db4f9-136">**Statutory book**</span></span>

<span data-ttu-id="db4f9-137">法定帳簿は現金基準の帳簿であり、リース料を毎月の家賃として支払う現金額として会計処理します。</span><span class="sxs-lookup"><span data-stu-id="db4f9-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="db4f9-138">この本は、使用権 (ROU) 資産やリース負債に関する法的責任を負わないものとします。</span><span class="sxs-lookup"><span data-stu-id="db4f9-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="db4f9-139">氏名</span><span class="sxs-lookup"><span data-stu-id="db4f9-139">Name</span></span>                                    | <span data-ttu-id="db4f9-140">説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="db4f9-141">帳簿タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-141">Book type</span></span>                               | <span data-ttu-id="db4f9-142">法令</span><span class="sxs-lookup"><span data-stu-id="db4f9-142">Statutory</span></span>   |
| <span data-ttu-id="db4f9-143">帳簿の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-143">Book description</span></span>                        | <span data-ttu-id="db4f9-144">ローカル GAAP</span><span class="sxs-lookup"><span data-stu-id="db4f9-144">Local GAAP</span></span>  |
| <span data-ttu-id="db4f9-145">転記階層</span><span class="sxs-lookup"><span data-stu-id="db4f9-145">Posting Layer</span></span>                           | <span data-ttu-id="db4f9-146">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-146">Current</span></span>     |
| <span data-ttu-id="db4f9-147">リース タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-147">Lease Type</span></span>                              | <span data-ttu-id="db4f9-148">自動</span><span class="sxs-lookup"><span data-stu-id="db4f9-148">Automatic</span></span>   |
| <span data-ttu-id="db4f9-149">会計フレームワーク</span><span class="sxs-lookup"><span data-stu-id="db4f9-149">Accounting Framework</span></span>                    | <span data-ttu-id="db4f9-150">現金主義</span><span class="sxs-lookup"><span data-stu-id="db4f9-150">Cash basis</span></span>  |
| <span data-ttu-id="db4f9-151">リース期間 / 耐用年数の設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="db4f9-152">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-152">0.00</span></span>        |
| <span data-ttu-id="db4f9-153">現在の価値 / 資産の公正価値の設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="db4f9-154">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-154">0.00</span></span>        |
| <span data-ttu-id="db4f9-155">短期的しきい値</span><span class="sxs-lookup"><span data-stu-id="db4f9-155">Short-term threshold</span></span>                    | <span data-ttu-id="db4f9-156">0</span><span class="sxs-lookup"><span data-stu-id="db4f9-156">0</span></span>           |
| <span data-ttu-id="db4f9-157">少額しきい値</span><span class="sxs-lookup"><span data-stu-id="db4f9-157">Low Value Threshold</span></span>                     | <span data-ttu-id="db4f9-158">0</span><span class="sxs-lookup"><span data-stu-id="db4f9-158">0</span></span>           |
| <span data-ttu-id="db4f9-159">仕入先への支払い</span><span class="sxs-lookup"><span data-stu-id="db4f9-159">Pay to Vendor</span></span>                           | <span data-ttu-id="db4f9-160">なし</span><span class="sxs-lookup"><span data-stu-id="db4f9-160">No</span></span>          |

<span data-ttu-id="db4f9-161">**法定取消帳簿**</span><span class="sxs-lookup"><span data-stu-id="db4f9-161">**Statutory reversal book**</span></span>

<span data-ttu-id="db4f9-162">法定取消帳簿は、法定帳簿と同じ方法で設定されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="db4f9-163">氏名</span><span class="sxs-lookup"><span data-stu-id="db4f9-163">Name</span></span>                                    | <span data-ttu-id="db4f9-164">説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="db4f9-165">帳簿タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-165">Book type</span></span>                               | <span data-ttu-id="db4f9-166">法定取消帳簿</span><span class="sxs-lookup"><span data-stu-id="db4f9-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="db4f9-167">帳簿の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-167">Book description</span></span>                        | <span data-ttu-id="db4f9-168">法定帳簿の取消</span><span class="sxs-lookup"><span data-stu-id="db4f9-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="db4f9-169">転記階層</span><span class="sxs-lookup"><span data-stu-id="db4f9-169">Posting Layer</span></span>                           | <span data-ttu-id="db4f9-170">カスタム レイヤー 1</span><span class="sxs-lookup"><span data-stu-id="db4f9-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="db4f9-171">リース タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-171">Lease Type</span></span>                              | <span data-ttu-id="db4f9-172">自動</span><span class="sxs-lookup"><span data-stu-id="db4f9-172">Automatic</span></span>                      |
| <span data-ttu-id="db4f9-173">会計フレームワーク</span><span class="sxs-lookup"><span data-stu-id="db4f9-173">Accounting Framework</span></span>                    | <span data-ttu-id="db4f9-174">現金主義</span><span class="sxs-lookup"><span data-stu-id="db4f9-174">Cash basis</span></span>                     |
| <span data-ttu-id="db4f9-175">リース期間 / 耐用年数の設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="db4f9-176">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-176">0.00</span></span>                           |
| <span data-ttu-id="db4f9-177">現在の価値 / 資産の公正価値の設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="db4f9-178">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-178">0.00</span></span>                           |
| <span data-ttu-id="db4f9-179">短期的しきい値</span><span class="sxs-lookup"><span data-stu-id="db4f9-179">Short-term threshold</span></span>                    | <span data-ttu-id="db4f9-180">0</span><span class="sxs-lookup"><span data-stu-id="db4f9-180">0</span></span>                              |
| <span data-ttu-id="db4f9-181">少額しきい値</span><span class="sxs-lookup"><span data-stu-id="db4f9-181">Low Value Threshold</span></span>                     | <span data-ttu-id="db4f9-182">0</span><span class="sxs-lookup"><span data-stu-id="db4f9-182">0</span></span>                              |
| <span data-ttu-id="db4f9-183">仕入先への支払い</span><span class="sxs-lookup"><span data-stu-id="db4f9-183">Pay to Vendor</span></span>                           | <span data-ttu-id="db4f9-184">なし</span><span class="sxs-lookup"><span data-stu-id="db4f9-184">No</span></span>                             |

<span data-ttu-id="db4f9-185">この例では、**全般** および **支払スケジュールの明細** タブで以下の設定を持つリースが作成されています。</span><span class="sxs-lookup"><span data-stu-id="db4f9-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="db4f9-186">**全般タブ**</span><span class="sxs-lookup"><span data-stu-id="db4f9-186">**General tab**</span></span>

| <span data-ttu-id="db4f9-187">フィールド</span><span class="sxs-lookup"><span data-stu-id="db4f9-187">Field</span></span>                      | <span data-ttu-id="db4f9-188">先頭値</span><span class="sxs-lookup"><span data-stu-id="db4f9-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="db4f9-189">追加借入利子率</span><span class="sxs-lookup"><span data-stu-id="db4f9-189">Incremental borrowing rate</span></span> | <span data-ttu-id="db4f9-190">5%</span><span class="sxs-lookup"><span data-stu-id="db4f9-190">5%</span></span>               |
| <span data-ttu-id="db4f9-191">開始日</span><span class="sxs-lookup"><span data-stu-id="db4f9-191">Commencement date</span></span>          | <span data-ttu-id="db4f9-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="db4f9-192">1/1/2020</span></span>         |
| <span data-ttu-id="db4f9-193">リース グループ</span><span class="sxs-lookup"><span data-stu-id="db4f9-193">Lease group</span></span>                | <span data-ttu-id="db4f9-194">建設物</span><span class="sxs-lookup"><span data-stu-id="db4f9-194">Buildings</span></span>        |
| <span data-ttu-id="db4f9-195">仕入先</span><span class="sxs-lookup"><span data-stu-id="db4f9-195">Vendor</span></span>                     | <span data-ttu-id="db4f9-196">1001</span><span class="sxs-lookup"><span data-stu-id="db4f9-196">1001</span></span>             |
| <span data-ttu-id="db4f9-197">資産の公正価値</span><span class="sxs-lookup"><span data-stu-id="db4f9-197">Fair value of the asset</span></span>    | <span data-ttu-id="db4f9-198">245,000</span><span class="sxs-lookup"><span data-stu-id="db4f9-198">245,000</span></span>          |
| <span data-ttu-id="db4f9-199">資産の耐用年数</span><span class="sxs-lookup"><span data-stu-id="db4f9-199">Asset useful life</span></span>          | <span data-ttu-id="db4f9-200">120</span><span class="sxs-lookup"><span data-stu-id="db4f9-200">120</span></span>              |
| <span data-ttu-id="db4f9-201">定期支払のタイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-201">Annuity type</span></span>               | <span data-ttu-id="db4f9-202">通常の定期支払</span><span class="sxs-lookup"><span data-stu-id="db4f9-202">Ordinary annuity</span></span> |
| <span data-ttu-id="db4f9-203">複合間隔</span><span class="sxs-lookup"><span data-stu-id="db4f9-203">Compounding interval</span></span>       | <span data-ttu-id="db4f9-204">月 1 回</span><span class="sxs-lookup"><span data-stu-id="db4f9-204">Monthly</span></span>          |

<span data-ttu-id="db4f9-205">**支払スケジュール明細行タブ**</span><span class="sxs-lookup"><span data-stu-id="db4f9-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="db4f9-206">フィールド</span><span class="sxs-lookup"><span data-stu-id="db4f9-206">Field</span></span>             | <span data-ttu-id="db4f9-207">先頭値</span><span class="sxs-lookup"><span data-stu-id="db4f9-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="db4f9-208">開始日</span><span class="sxs-lookup"><span data-stu-id="db4f9-208">Start date</span></span>        | <span data-ttu-id="db4f9-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="db4f9-209">1/1/2020</span></span>   |
| <span data-ttu-id="db4f9-210">間隔</span><span class="sxs-lookup"><span data-stu-id="db4f9-210">Period interval</span></span>   | <span data-ttu-id="db4f9-211">月数</span><span class="sxs-lookup"><span data-stu-id="db4f9-211">Months</span></span>     |
| <span data-ttu-id="db4f9-212">期間</span><span class="sxs-lookup"><span data-stu-id="db4f9-212">Periods</span></span>           | <span data-ttu-id="db4f9-213">24</span><span class="sxs-lookup"><span data-stu-id="db4f9-213">24</span></span>         |
| <span data-ttu-id="db4f9-214">終了日</span><span class="sxs-lookup"><span data-stu-id="db4f9-214">End date</span></span>          | <span data-ttu-id="db4f9-215">2020/12/31</span><span class="sxs-lookup"><span data-stu-id="db4f9-215">12/31/2020</span></span> |
| <span data-ttu-id="db4f9-216">支払頻度</span><span class="sxs-lookup"><span data-stu-id="db4f9-216">Payment frequency</span></span> | <span data-ttu-id="db4f9-217">月 1 回</span><span class="sxs-lookup"><span data-stu-id="db4f9-217">Monthly</span></span>    |
| <span data-ttu-id="db4f9-218">支払額</span><span class="sxs-lookup"><span data-stu-id="db4f9-218">Payment amount</span></span>    | <span data-ttu-id="db4f9-219">1.000</span><span class="sxs-lookup"><span data-stu-id="db4f9-219">1,000</span></span>      |

<span data-ttu-id="db4f9-220">このリースを 2 つのフレームワークで考慮するには、現在の転記階層とカスタム転記階層を使用します。</span><span class="sxs-lookup"><span data-stu-id="db4f9-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="db4f9-221">以下の表は、各報告基準の下で財務情報を公正に表示することが要求される仕訳の例です。</span><span class="sxs-lookup"><span data-stu-id="db4f9-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="db4f9-222">リースの最初の月についての各仕訳入力の詳細な説明については後述します。</span><span class="sxs-lookup"><span data-stu-id="db4f9-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="db4f9-223">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="db4f9-224">説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="db4f9-225">法定帳簿 (現在の層)</span><span class="sxs-lookup"><span data-stu-id="db4f9-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="db4f9-226">現在のレイヤーの合計</span><span class="sxs-lookup"><span data-stu-id="db4f9-226">Current layer total</span></span></th>
<th><span data-ttu-id="db4f9-227">取消帳簿 (カスタム層)</span><span class="sxs-lookup"><span data-stu-id="db4f9-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="db4f9-228">IFRS 16 号 帳簿 (カスタム層)</span><span class="sxs-lookup"><span data-stu-id="db4f9-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="db4f9-229">現在のレイヤー + カスタム層の合計</span><span class="sxs-lookup"><span data-stu-id="db4f9-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="db4f9-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="db4f9-230">JE-100</span></span></th>
<th><span data-ttu-id="db4f9-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="db4f9-231">JE-110</span></span></th>
<th><span data-ttu-id="db4f9-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="db4f9-232">JE-120</span></span></th>
<th><span data-ttu-id="db4f9-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="db4f9-233">JE-130</span></span></th>
<th><span data-ttu-id="db4f9-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="db4f9-234">JE-140</span></span></th>
<th><span data-ttu-id="db4f9-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="db4f9-235">JE-150</span></span></th>
<th><span data-ttu-id="db4f9-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="db4f9-236">JE-160</span></span></th>
<th><span data-ttu-id="db4f9-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="db4f9-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="db4f9-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db4f9-246">1</span><span class="sxs-lookup"><span data-stu-id="db4f9-246">1</span></span></td>
<td><span data-ttu-id="db4f9-247">リース経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-247">Lease expense</span></span></td>
<td><span data-ttu-id="db4f9-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-249">1,000.00</span></span></td>
<td><span data-ttu-id="db4f9-250">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-251">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-252">2</span><span class="sxs-lookup"><span data-stu-id="db4f9-252">2</span></span></td>
<td><span data-ttu-id="db4f9-253">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="db4f9-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-254">3.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-255">3.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-256">3.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-257">3</span><span class="sxs-lookup"><span data-stu-id="db4f9-257">3</span></span></td>
<td><span data-ttu-id="db4f9-258">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-259">5.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-260">5.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-261">5.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-262">4</span><span class="sxs-lookup"><span data-stu-id="db4f9-262">4</span></span></td>
<td><span data-ttu-id="db4f9-263">清算勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-263">Clearing account</span></span></td>
<td><span data-ttu-id="db4f9-264">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-264">-1,000.00</span></span></td>
<td><span data-ttu-id="db4f9-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-266">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-266">0.00</span></span></td>
<td><span data-ttu-id="db4f9-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-268">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-269">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-270">5</span><span class="sxs-lookup"><span data-stu-id="db4f9-270">5</span></span></td>
<td><span data-ttu-id="db4f9-271">買掛金</span><span class="sxs-lookup"><span data-stu-id="db4f9-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-272">-1,008.00</span></span></td>
<td><span data-ttu-id="db4f9-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-273">1,008.00</span></span></td>
<td><span data-ttu-id="db4f9-274">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-275">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-276">6</span><span class="sxs-lookup"><span data-stu-id="db4f9-276">6</span></span></td>
<td><span data-ttu-id="db4f9-277">使用権資産</span><span class="sxs-lookup"><span data-stu-id="db4f9-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-278">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="db4f9-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-281">7</span><span class="sxs-lookup"><span data-stu-id="db4f9-281">7</span></span></td>
<td><span data-ttu-id="db4f9-282">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="db4f9-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-283">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-284">-22,794.00</span></span></td>
<td><span data-ttu-id="db4f9-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-285">1,000.00</span></span></td>
<td><span data-ttu-id="db4f9-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="db4f9-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-288">8</span><span class="sxs-lookup"><span data-stu-id="db4f9-288">8</span></span></td>
<td><span data-ttu-id="db4f9-289">支払利息</span><span class="sxs-lookup"><span data-stu-id="db4f9-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-290">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-291">94.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-292">94.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-293">9</span><span class="sxs-lookup"><span data-stu-id="db4f9-293">9</span></span></td>
<td><span data-ttu-id="db4f9-294">現金</span><span class="sxs-lookup"><span data-stu-id="db4f9-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-295">-1,008.00</span></span></td>
<td><span data-ttu-id="db4f9-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-298">10</span><span class="sxs-lookup"><span data-stu-id="db4f9-298">10</span></span></td>
<td><span data-ttu-id="db4f9-299">減価償却費</span><span class="sxs-lookup"><span data-stu-id="db4f9-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-300">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-301">949.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-301">949.75</span></span></td>
<td><span data-ttu-id="db4f9-302">949.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-303">11</span><span class="sxs-lookup"><span data-stu-id="db4f9-303">11</span></span></td>
<td><span data-ttu-id="db4f9-304">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="db4f9-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-305">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-306">-949.75</span></span></td>
<td><span data-ttu-id="db4f9-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db4f9-308">前の表に示すように、法定報告書と IFRS 報告書の両方で報告が必要な帳簿は 3 冊です。</span><span class="sxs-lookup"><span data-stu-id="db4f9-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="db4f9-309">法定帳簿には、流動層の下の現金主義会計のルールに従って、リース支払を記録しています。</span><span class="sxs-lookup"><span data-stu-id="db4f9-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="db4f9-310">法的取消帳簿により、法的仕訳入力が取り消されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="db4f9-311">IFRS 16 号の帳簿では、IFRS 16 号に必要な仕訳入力が作成されています。</span><span class="sxs-lookup"><span data-stu-id="db4f9-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="db4f9-312">リースは 1 回だけ入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db4f9-312">You must enter a lease only one time.</span></span> <span data-ttu-id="db4f9-313">その後、**帳簿** ページを開いて、このリースに関連付けられているすべての帳簿を表示できます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="db4f9-314">帳簿を作成する際には、これらの 3 つのすべてが同じリース レコードに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="db4f9-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="db4f9-315">最初の仕訳入力には、法定帳簿でのリース経費が記録されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="db4f9-316">支払は、一括で作成することも、法定帳簿の支払予定表を選択して作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="db4f9-317">この例では、次の仕訳入力が支払スケジュールからの法定帳簿に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="db4f9-318">リース支払 – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="db4f9-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="db4f9-319">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-319">Account type</span></span> | <span data-ttu-id="db4f9-320">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-320">Account number</span></span> | <span data-ttu-id="db4f9-321">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-321">Layer</span></span>   | <span data-ttu-id="db4f9-322">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-322">Account description</span></span> | <span data-ttu-id="db4f9-323">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-323">Debit</span></span>    | <span data-ttu-id="db4f9-324">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="db4f9-325">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-325">Ledger</span></span>       | <span data-ttu-id="db4f9-326">1</span><span class="sxs-lookup"><span data-stu-id="db4f9-326">1</span></span>              | <span data-ttu-id="db4f9-327">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-327">Current</span></span> | <span data-ttu-id="db4f9-328">リース経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-328">Lease expense</span></span>       | <span data-ttu-id="db4f9-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-329">1,000.00</span></span> |          |
| <span data-ttu-id="db4f9-330">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-330">Ledger</span></span>       | <span data-ttu-id="db4f9-331">4</span><span class="sxs-lookup"><span data-stu-id="db4f9-331">4</span></span>              | <span data-ttu-id="db4f9-332">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-332">Current</span></span> | <span data-ttu-id="db4f9-333">清算勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-333">Clearing account</span></span>    |          | <span data-ttu-id="db4f9-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-334">1,000.00</span></span> |

<span data-ttu-id="db4f9-335">買掛金勘定の担当者は、Dynamics 365 の標準機能を利用して、資産リース以外のリースに対する支払請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="db4f9-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="db4f9-336">しかし、借方勘定に **リースの経費** を選択する代わりに、買掛金勘定の担当者は次の入力を生成する精算勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="db4f9-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="db4f9-337">AP プロセス – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="db4f9-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="db4f9-338">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-338">Account type</span></span> | <span data-ttu-id="db4f9-339">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-339">Account number</span></span> | <span data-ttu-id="db4f9-340">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-340">Layer</span></span>   | <span data-ttu-id="db4f9-341">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-341">Account description</span></span> | <span data-ttu-id="db4f9-342">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-342">Debit</span></span>    | <span data-ttu-id="db4f9-343">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="db4f9-344">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-344">Ledger</span></span>       | <span data-ttu-id="db4f9-345">4</span><span class="sxs-lookup"><span data-stu-id="db4f9-345">4</span></span>              | <span data-ttu-id="db4f9-346">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-346">Current</span></span> | <span data-ttu-id="db4f9-347">清算勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-347">Clearing account</span></span>    | <span data-ttu-id="db4f9-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-348">1,000.00</span></span> |          |
| <span data-ttu-id="db4f9-349">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-349">Ledger</span></span>       | <span data-ttu-id="db4f9-350">2</span><span class="sxs-lookup"><span data-stu-id="db4f9-350">2</span></span>              | <span data-ttu-id="db4f9-351">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-351">Current</span></span> | <span data-ttu-id="db4f9-352">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="db4f9-352">Bank fee</span></span>            | <span data-ttu-id="db4f9-353">3.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-353">3.00</span></span>     |          |
| <span data-ttu-id="db4f9-354">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-354">Ledger</span></span>       | <span data-ttu-id="db4f9-355">3</span><span class="sxs-lookup"><span data-stu-id="db4f9-355">3</span></span>              | <span data-ttu-id="db4f9-356">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-356">Current</span></span> | <span data-ttu-id="db4f9-357">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-357">VAT expense</span></span>         | <span data-ttu-id="db4f9-358">5.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-358">5.00</span></span>     |          |
| <span data-ttu-id="db4f9-359">仕入先</span><span class="sxs-lookup"><span data-stu-id="db4f9-359">Vendor</span></span>       | <span data-ttu-id="db4f9-360">5</span><span class="sxs-lookup"><span data-stu-id="db4f9-360">5</span></span>              | <span data-ttu-id="db4f9-361">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-361">Current</span></span> | <span data-ttu-id="db4f9-362">買掛金</span><span class="sxs-lookup"><span data-stu-id="db4f9-362">Accounts payable</span></span>    |          | <span data-ttu-id="db4f9-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-363">1,008.00</span></span> |

<span data-ttu-id="db4f9-364">仕入先に対して明細書を発行すると、通常の支払い手続きを行います。</span><span class="sxs-lookup"><span data-stu-id="db4f9-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="db4f9-365">このプロセスでは、次の仕訳入力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="db4f9-366">現金支払 – 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="db4f9-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="db4f9-367">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-367">Account type</span></span> | <span data-ttu-id="db4f9-368">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-368">Account number</span></span> | <span data-ttu-id="db4f9-369">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-369">Layer</span></span>   | <span data-ttu-id="db4f9-370">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-370">Account description</span></span> | <span data-ttu-id="db4f9-371">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-371">Debit</span></span>    | <span data-ttu-id="db4f9-372">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="db4f9-373">仕入先</span><span class="sxs-lookup"><span data-stu-id="db4f9-373">Vendor</span></span>       | <span data-ttu-id="db4f9-374">5</span><span class="sxs-lookup"><span data-stu-id="db4f9-374">5</span></span>              | <span data-ttu-id="db4f9-375">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-375">Current</span></span> | <span data-ttu-id="db4f9-376">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-376">Accounts Payable</span></span>    | <span data-ttu-id="db4f9-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-377">1,008.00</span></span> |          |
| <span data-ttu-id="db4f9-378">銀行</span><span class="sxs-lookup"><span data-stu-id="db4f9-378">Bank</span></span>         | <span data-ttu-id="db4f9-379">9</span><span class="sxs-lookup"><span data-stu-id="db4f9-379">9</span></span>              | <span data-ttu-id="db4f9-380">現行</span><span class="sxs-lookup"><span data-stu-id="db4f9-380">Current</span></span> | <span data-ttu-id="db4f9-381">現金</span><span class="sxs-lookup"><span data-stu-id="db4f9-381">Cash</span></span>                |          | <span data-ttu-id="db4f9-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-382">1,008.00</span></span> |

<span data-ttu-id="db4f9-383">この時点で、このリースを法定の報告要件に基づいて完全に会計処理されており、現在の層を使用して試算表を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="db4f9-384">システムからは、次の図を含む試算表が返されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="db4f9-385">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="db4f9-386">説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="db4f9-387">法定帳簿 (現在の層)</span><span class="sxs-lookup"><span data-stu-id="db4f9-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="db4f9-388">現在のレイヤーの合計</span><span class="sxs-lookup"><span data-stu-id="db4f9-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="db4f9-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="db4f9-389">JE-100</span></span></th>
<th><span data-ttu-id="db4f9-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="db4f9-390">JE-110</span></span></th>
<th><span data-ttu-id="db4f9-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="db4f9-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="db4f9-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="db4f9-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="db4f9-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db4f9-395">1</span><span class="sxs-lookup"><span data-stu-id="db4f9-395">1</span></span></td>
<td><span data-ttu-id="db4f9-396">リース経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-396">Lease expense</span></span></td>
<td><span data-ttu-id="db4f9-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-399">2</span><span class="sxs-lookup"><span data-stu-id="db4f9-399">2</span></span></td>
<td><span data-ttu-id="db4f9-400">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="db4f9-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-401">3.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-402">3.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-403">3</span><span class="sxs-lookup"><span data-stu-id="db4f9-403">3</span></span></td>
<td><span data-ttu-id="db4f9-404">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-405">5.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-406">5.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-407">4</span><span class="sxs-lookup"><span data-stu-id="db4f9-407">4</span></span></td>
<td><span data-ttu-id="db4f9-408">清算勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-408">Clearing account</span></span></td>
<td><span data-ttu-id="db4f9-409">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-409">-1,000.00</span></span></td>
<td><span data-ttu-id="db4f9-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-411">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-412">5</span><span class="sxs-lookup"><span data-stu-id="db4f9-412">5</span></span></td>
<td><span data-ttu-id="db4f9-413">買掛金</span><span class="sxs-lookup"><span data-stu-id="db4f9-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="db4f9-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-414">-1,008.00</span></span></td>
<td><span data-ttu-id="db4f9-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-415">1,008.00</span></span></td>
<td><span data-ttu-id="db4f9-416">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-417">6</span><span class="sxs-lookup"><span data-stu-id="db4f9-417">6</span></span></td>
<td><span data-ttu-id="db4f9-418">使用権資産</span><span class="sxs-lookup"><span data-stu-id="db4f9-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-419">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-420">7</span><span class="sxs-lookup"><span data-stu-id="db4f9-420">7</span></span></td>
<td><span data-ttu-id="db4f9-421">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="db4f9-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-422">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-423">8</span><span class="sxs-lookup"><span data-stu-id="db4f9-423">8</span></span></td>
<td><span data-ttu-id="db4f9-424">支払利息</span><span class="sxs-lookup"><span data-stu-id="db4f9-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-425">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-426">9</span><span class="sxs-lookup"><span data-stu-id="db4f9-426">9</span></span></td>
<td><span data-ttu-id="db4f9-427">現金</span><span class="sxs-lookup"><span data-stu-id="db4f9-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-428">-1,008.00</span></span></td>
<td><span data-ttu-id="db4f9-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-430">10</span><span class="sxs-lookup"><span data-stu-id="db4f9-430">10</span></span></td>
<td><span data-ttu-id="db4f9-431">減価償却費</span><span class="sxs-lookup"><span data-stu-id="db4f9-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-432">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db4f9-433">11</span><span class="sxs-lookup"><span data-stu-id="db4f9-433">11</span></span></td>
<td><span data-ttu-id="db4f9-434">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="db4f9-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="db4f9-435">0.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db4f9-436">IFRS 16 号の数字を使って同じ試算表を実行する場合は、法定会計の仕訳を取り消して、IFRS 16号の仕訳を転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db4f9-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="db4f9-437">この例では、法定仕訳を取り消すにあたり、法定帳簿と同じ設定でありながら、反対の転記プロファイルを持つ法定取消帳簿が含まれています。</span><span class="sxs-lookup"><span data-stu-id="db4f9-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="db4f9-438">たとえば、法定帳簿はリース費用勘定を *引き落とし* ていますが、取消帳簿はこの勘定を *計上* します。</span><span class="sxs-lookup"><span data-stu-id="db4f9-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="db4f9-439">これらの関係は、**資産リースパラメーター** ページ (**資産リース \> 設定 \> 資産のリース パラメーター**) の資産リースの転記勘定で簡単に定義できます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="db4f9-440">法定帳簿に使用されたものと同じプロセスが取消帳簿に使用されると、次の仕訳入力が作成されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="db4f9-441">この違いは、取消帳簿が法定帳簿からの取消記載を記載している点にあります。</span><span class="sxs-lookup"><span data-stu-id="db4f9-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="db4f9-442">取消の入力は、カスタム層にも作成されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="db4f9-443">試算表を現在の層で実行すると、取消仕訳の入力は含まれません。</span><span class="sxs-lookup"><span data-stu-id="db4f9-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="db4f9-444">リース支払 – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="db4f9-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="db4f9-445">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-445">Account type</span></span> | <span data-ttu-id="db4f9-446">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-446">Account number</span></span> | <span data-ttu-id="db4f9-447">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-447">Layer</span></span>  | <span data-ttu-id="db4f9-448">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-448">Account description</span></span> | <span data-ttu-id="db4f9-449">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-449">Debit</span></span>    | <span data-ttu-id="db4f9-450">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="db4f9-451">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-451">Ledger</span></span>       | <span data-ttu-id="db4f9-452">4</span><span class="sxs-lookup"><span data-stu-id="db4f9-452">4</span></span>              | <span data-ttu-id="db4f9-453">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-453">Custom</span></span> | <span data-ttu-id="db4f9-454">清算勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-454">Clearing account</span></span>    | <span data-ttu-id="db4f9-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-455">1,000.00</span></span> |          |
| <span data-ttu-id="db4f9-456">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-456">Ledger</span></span>       | <span data-ttu-id="db4f9-457">1</span><span class="sxs-lookup"><span data-stu-id="db4f9-457">1</span></span>              | <span data-ttu-id="db4f9-458">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-458">Custom</span></span> | <span data-ttu-id="db4f9-459">リース経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-459">Lease expense</span></span>       |          | <span data-ttu-id="db4f9-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-460">1,000.00</span></span> |

<span data-ttu-id="db4f9-461">以上で法定仕訳の入力が削除されたため、IFRS 16号で要求されている仕訳をすべて IFRS 16号の帳簿に計上することになります。</span><span class="sxs-lookup"><span data-stu-id="db4f9-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="db4f9-462">これらの入力には、使用権資産と負債の当初認識および、利息と減価償却の記録が含まれます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="db4f9-463">当初認識 – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="db4f9-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="db4f9-464">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-464">Account type</span></span> | <span data-ttu-id="db4f9-465">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-465">Account number</span></span> | <span data-ttu-id="db4f9-466">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-466">Layer</span></span>  | <span data-ttu-id="db4f9-467">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-467">Account description</span></span>      | <span data-ttu-id="db4f9-468">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-468">Debit</span></span>     | <span data-ttu-id="db4f9-469">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="db4f9-470">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-470">Ledger</span></span>       | <span data-ttu-id="db4f9-471">6</span><span class="sxs-lookup"><span data-stu-id="db4f9-471">6</span></span>              | <span data-ttu-id="db4f9-472">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-472">Custom</span></span> | <span data-ttu-id="db4f9-473">使用権資産</span><span class="sxs-lookup"><span data-stu-id="db4f9-473">ROU Asset</span></span>                | <span data-ttu-id="db4f9-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="db4f9-474">22,793.90</span></span> |           |
| <span data-ttu-id="db4f9-475">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-475">Ledger</span></span>       | <span data-ttu-id="db4f9-476">7</span><span class="sxs-lookup"><span data-stu-id="db4f9-476">7</span></span>              | <span data-ttu-id="db4f9-477">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-477">Custom</span></span> | <span data-ttu-id="db4f9-478">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="db4f9-478">Finance lease obligation</span></span> |           | <span data-ttu-id="db4f9-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="db4f9-479">22,793.90</span></span> |

<span data-ttu-id="db4f9-480">リース支払は、他のリース支払と同じように転記されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="db4f9-481">清算勘定を使用する理由は、現金を一度だけ貸方に確実に転記するためです。</span><span class="sxs-lookup"><span data-stu-id="db4f9-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="db4f9-482">リース支払 – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="db4f9-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="db4f9-483">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-483">Account type</span></span> | <span data-ttu-id="db4f9-484">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-484">Account number</span></span> | <span data-ttu-id="db4f9-485">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-485">Layer</span></span>  | <span data-ttu-id="db4f9-486">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-486">Account description</span></span>      | <span data-ttu-id="db4f9-487">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-487">Debit</span></span>    | <span data-ttu-id="db4f9-488">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="db4f9-489">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-489">Ledger</span></span>       | <span data-ttu-id="db4f9-490">7</span><span class="sxs-lookup"><span data-stu-id="db4f9-490">7</span></span>              | <span data-ttu-id="db4f9-491">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-491">Custom</span></span> | <span data-ttu-id="db4f9-492">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="db4f9-492">Finance lease obligation</span></span> | <span data-ttu-id="db4f9-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-493">1,000.00</span></span> |          |
| <span data-ttu-id="db4f9-494">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-494">Ledger</span></span>       | <span data-ttu-id="db4f9-495">4</span><span class="sxs-lookup"><span data-stu-id="db4f9-495">4</span></span>              | <span data-ttu-id="db4f9-496">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-496">Custom</span></span> | <span data-ttu-id="db4f9-497">清算勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-497">Clearing account</span></span>         |          | <span data-ttu-id="db4f9-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-498">1,000.00</span></span> |

<span data-ttu-id="db4f9-499">支払利息の仕訳入力は、負債の償却スケジュールから生成されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="db4f9-500">支払利息 – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="db4f9-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="db4f9-501">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-501">Account type</span></span> | <span data-ttu-id="db4f9-502">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-502">Account number</span></span> | <span data-ttu-id="db4f9-503">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-503">Layer</span></span>  | <span data-ttu-id="db4f9-504">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-504">Account description</span></span>      | <span data-ttu-id="db4f9-505">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-505">Debit</span></span> | <span data-ttu-id="db4f9-506">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="db4f9-507">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-507">Ledger</span></span>       | <span data-ttu-id="db4f9-508">8</span><span class="sxs-lookup"><span data-stu-id="db4f9-508">8</span></span>              | <span data-ttu-id="db4f9-509">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-509">Custom</span></span> | <span data-ttu-id="db4f9-510">支払利息</span><span class="sxs-lookup"><span data-stu-id="db4f9-510">Interest expense</span></span>         | <span data-ttu-id="db4f9-511">94.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-511">94.97</span></span> |        |
| <span data-ttu-id="db4f9-512">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-512">Ledger</span></span>       | <span data-ttu-id="db4f9-513">7</span><span class="sxs-lookup"><span data-stu-id="db4f9-513">7</span></span>              | <span data-ttu-id="db4f9-514">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-514">Custom</span></span> | <span data-ttu-id="db4f9-515">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="db4f9-515">Finance lease obligation</span></span> |       | <span data-ttu-id="db4f9-516">94.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-516">94.97</span></span>  |

<span data-ttu-id="db4f9-517">減価償却費の仕訳は、資産の減価償却スケジュールから生成されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="db4f9-518">減価償却費 – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="db4f9-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="db4f9-519">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="db4f9-519">Account type</span></span> | <span data-ttu-id="db4f9-520">勘定番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-520">Account number</span></span> | <span data-ttu-id="db4f9-521">レイヤー</span><span class="sxs-lookup"><span data-stu-id="db4f9-521">Layer</span></span>  | <span data-ttu-id="db4f9-522">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-522">Account description</span></span>      | <span data-ttu-id="db4f9-523">借方</span><span class="sxs-lookup"><span data-stu-id="db4f9-523">Debit</span></span>  | <span data-ttu-id="db4f9-524">貸方</span><span class="sxs-lookup"><span data-stu-id="db4f9-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="db4f9-525">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-525">Ledger</span></span>       | <span data-ttu-id="db4f9-526">10</span><span class="sxs-lookup"><span data-stu-id="db4f9-526">10</span></span>             | <span data-ttu-id="db4f9-527">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-527">Custom</span></span> | <span data-ttu-id="db4f9-528">減価償却費</span><span class="sxs-lookup"><span data-stu-id="db4f9-528">Depreciation expense</span></span>     | <span data-ttu-id="db4f9-529">949.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-529">949.75</span></span> |        |
| <span data-ttu-id="db4f9-530">会計</span><span class="sxs-lookup"><span data-stu-id="db4f9-530">Ledger</span></span>       | <span data-ttu-id="db4f9-531">11</span><span class="sxs-lookup"><span data-stu-id="db4f9-531">11</span></span>             | <span data-ttu-id="db4f9-532">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="db4f9-532">Custom</span></span> | <span data-ttu-id="db4f9-533">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="db4f9-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="db4f9-534">949.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-534">949.75</span></span> |

<span data-ttu-id="db4f9-535">これらすべての仕訳入力が作成され、転記されると、次のような "カスタム層 1" の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="db4f9-536">最後の列には、銀行手数料、付加価値税 (VAT) の費用、前の層からの現金の減額が含まれていますが、法定報告仕訳帳のエントリは含まれていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="db4f9-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="db4f9-537">したがって、本来的なデュアルレポート機能を実現できます。</span><span class="sxs-lookup"><span data-stu-id="db4f9-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="db4f9-538">この時点で、会社は試算表を実行し、現在のレイヤーとカスタム レイヤーを結合して IFRS 試算表を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db4f9-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="db4f9-539">口座番号</span><span class="sxs-lookup"><span data-stu-id="db4f9-539">Account No</span></span> | <span data-ttu-id="db4f9-540">説明</span><span class="sxs-lookup"><span data-stu-id="db4f9-540">Description</span></span>              | <span data-ttu-id="db4f9-541">法定帳簿\-現在のレイヤー \-JE \-100 \-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-542">法定帳簿\-現在のレイヤー \-JE \-110 \-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-543">法定帳簿\-現在のレイヤー \-JE \-120 \-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-544">現在のレイヤー \- 合計</span><span class="sxs-lookup"><span data-stu-id="db4f9-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="db4f9-545">取消帳簿\-カスタム レイヤー\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-546">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-547">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-548">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-549">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="db4f9-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="db4f9-550">カスタム レイヤー\+ 現在のレイヤー \- 合計</span><span class="sxs-lookup"><span data-stu-id="db4f9-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="db4f9-551">1</span><span class="sxs-lookup"><span data-stu-id="db4f9-551">1</span></span>          | <span data-ttu-id="db4f9-552">リース経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-552">Lease expense</span></span>            | <span data-ttu-id="db4f9-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="db4f9-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-554">1,000\.00</span></span>               |   | <span data-ttu-id="db4f9-555">\-1,000</span><span class="sxs-lookup"><span data-stu-id="db4f9-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="db4f9-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-556">0\.00</span></span>                                   |
| <span data-ttu-id="db4f9-557">2</span><span class="sxs-lookup"><span data-stu-id="db4f9-557">2</span></span>          | <span data-ttu-id="db4f9-558">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="db4f9-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="db4f9-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="db4f9-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="db4f9-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-561">3\.00</span></span>                                   |
| <span data-ttu-id="db4f9-562">3</span><span class="sxs-lookup"><span data-stu-id="db4f9-562">3</span></span>          | <span data-ttu-id="db4f9-563">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="db4f9-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="db4f9-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="db4f9-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="db4f9-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-566">5\.00</span></span>                                   |
| <span data-ttu-id="db4f9-567">4</span><span class="sxs-lookup"><span data-stu-id="db4f9-567">4</span></span>          | <span data-ttu-id="db4f9-568">清算勘定</span><span class="sxs-lookup"><span data-stu-id="db4f9-568">Clearing account</span></span>         | <span data-ttu-id="db4f9-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="db4f9-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="db4f9-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-571">0\.00</span></span>                   |   | <span data-ttu-id="db4f9-572">1.000</span><span class="sxs-lookup"><span data-stu-id="db4f9-572">1,000</span></span>                                           |                                                | <span data-ttu-id="db4f9-573">\-1,000</span><span class="sxs-lookup"><span data-stu-id="db4f9-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="db4f9-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-574">0\.00</span></span>                                   |
| <span data-ttu-id="db4f9-575">5</span><span class="sxs-lookup"><span data-stu-id="db4f9-575">5</span></span>          | <span data-ttu-id="db4f9-576">買掛金</span><span class="sxs-lookup"><span data-stu-id="db4f9-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="db4f9-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="db4f9-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-578">1,008\.00</span></span>                                         | <span data-ttu-id="db4f9-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="db4f9-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-580">0\.00</span></span>                                   |
| <span data-ttu-id="db4f9-581">6</span><span class="sxs-lookup"><span data-stu-id="db4f9-581">6</span></span>          | <span data-ttu-id="db4f9-582">使用権資産</span><span class="sxs-lookup"><span data-stu-id="db4f9-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="db4f9-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="db4f9-584">22,794</span><span class="sxs-lookup"><span data-stu-id="db4f9-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="db4f9-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="db4f9-585">22,793\.90</span></span>                              |
| <span data-ttu-id="db4f9-586">7</span><span class="sxs-lookup"><span data-stu-id="db4f9-586">7</span></span>          | <span data-ttu-id="db4f9-587">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="db4f9-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="db4f9-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="db4f9-589">\-22,794</span><span class="sxs-lookup"><span data-stu-id="db4f9-589">\-22,794</span></span>                                       | <span data-ttu-id="db4f9-590">1.000</span><span class="sxs-lookup"><span data-stu-id="db4f9-590">1,000</span></span>                                          | <span data-ttu-id="db4f9-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="db4f9-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="db4f9-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="db4f9-593">8</span><span class="sxs-lookup"><span data-stu-id="db4f9-593">8</span></span>          | <span data-ttu-id="db4f9-594">支払利息</span><span class="sxs-lookup"><span data-stu-id="db4f9-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="db4f9-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="db4f9-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="db4f9-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="db4f9-597">94\.97</span></span>                                  |
| <span data-ttu-id="db4f9-598">9</span><span class="sxs-lookup"><span data-stu-id="db4f9-598">9</span></span>          | <span data-ttu-id="db4f9-599">現金</span><span class="sxs-lookup"><span data-stu-id="db4f9-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="db4f9-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="db4f9-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="db4f9-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="db4f9-603">10</span><span class="sxs-lookup"><span data-stu-id="db4f9-603">10</span></span>         | <span data-ttu-id="db4f9-604">減価償却費</span><span class="sxs-lookup"><span data-stu-id="db4f9-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="db4f9-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="db4f9-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-606">949\.75</span></span>                                        | <span data-ttu-id="db4f9-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-607">949\.75</span></span>                                 |
| <span data-ttu-id="db4f9-608">11</span><span class="sxs-lookup"><span data-stu-id="db4f9-608">11</span></span>         | <span data-ttu-id="db4f9-609">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="db4f9-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="db4f9-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="db4f9-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="db4f9-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-611">\-949\.75</span></span>                                      | <span data-ttu-id="db4f9-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="db4f9-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]