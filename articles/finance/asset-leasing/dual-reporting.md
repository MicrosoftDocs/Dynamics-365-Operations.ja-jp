---
title: デュアル レポート
description: このトピックでは、International Financial Reporting Standard (国際会計基準 - IFRS) レポートと資産のリースにおける法定報告の要件を満たす方法を、例を挙げて説明します。
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
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229553"
---
# <a name="dual-reporting"></a><span data-ttu-id="aae96-103">二重レポート</span><span class="sxs-lookup"><span data-stu-id="aae96-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aae96-104">このトピックでは、International Financial Reporting Standard (国際会計基準 - IFRS) レポートと資産のリースにおける法定報告の要件を満たす方法を、例を挙げて説明します。</span><span class="sxs-lookup"><span data-stu-id="aae96-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="aae96-105">Microsoft Dynamics 365 Finance の転記階層に関する知識が必要であり、ここで挙げる例を簡単に理解することができます。</span><span class="sxs-lookup"><span data-stu-id="aae96-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="aae96-106">例</span><span class="sxs-lookup"><span data-stu-id="aae96-106">Example</span></span>

<span data-ttu-id="aae96-107">以下の例では、イタリアの法定報告に基づき、現金基準法と IFRS の両方の報告方法を用いてリースを会計処理しています。</span><span class="sxs-lookup"><span data-stu-id="aae96-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="aae96-108">この会社では、イタリアの法的要件と IFRS 16 号の要件の両方について、3 冊の帳簿を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae96-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="aae96-109">IFRS 16 号には 1 冊の帳簿が必要であり、法的要件には 1 冊の帳簿が必要であり、法的な転記を自動的に取り消すには、1 冊の帳簿が必要です。</span><span class="sxs-lookup"><span data-stu-id="aae96-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="aae96-110">この帳簿は、次の表に示すように設定されています。</span><span class="sxs-lookup"><span data-stu-id="aae96-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="aae96-111">**IFRS 16 号の帳簿**</span><span class="sxs-lookup"><span data-stu-id="aae96-111">**IFRS 16 book**</span></span>

<span data-ttu-id="aae96-112">IFRS 16 号の帳簿は、IFRS 16 号の勘定の標準に準拠するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="aae96-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="aae96-113">このドキュメントに記載されているすべての入力は、カスタム レイヤーに転記されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="aae96-114">氏名</span><span class="sxs-lookup"><span data-stu-id="aae96-114">Name</span></span>                                    | <span data-ttu-id="aae96-115">説明</span><span class="sxs-lookup"><span data-stu-id="aae96-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="aae96-116">帳簿タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-116">Book type</span></span>                               | <span data-ttu-id="aae96-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="aae96-117">IFRS 16</span></span>        |
| <span data-ttu-id="aae96-118">帳簿の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-118">Book description</span></span>                        | <span data-ttu-id="aae96-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="aae96-119">IFRS 16</span></span>        |
| <span data-ttu-id="aae96-120">転記階層</span><span class="sxs-lookup"><span data-stu-id="aae96-120">Posting Layer</span></span>                           | <span data-ttu-id="aae96-121">カスタム レイヤー 1</span><span class="sxs-lookup"><span data-stu-id="aae96-121">Custom layer 1</span></span> |
| <span data-ttu-id="aae96-122">リース タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-122">Lease Type</span></span>                              | <span data-ttu-id="aae96-123">Finance</span><span class="sxs-lookup"><span data-stu-id="aae96-123">Finance</span></span>        |
| <span data-ttu-id="aae96-124">会計フレームワーク</span><span class="sxs-lookup"><span data-stu-id="aae96-124">Accounting Framework</span></span>                    | <span data-ttu-id="aae96-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="aae96-125">IFRS 16</span></span>        |
| <span data-ttu-id="aae96-126">リース期間 / 耐用年数の設定</span><span class="sxs-lookup"><span data-stu-id="aae96-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="aae96-127">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-127">0.00</span></span>           |
| <span data-ttu-id="aae96-128">現在の価値 / 資産の公正価値の設定</span><span class="sxs-lookup"><span data-stu-id="aae96-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="aae96-129">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-129">0.00</span></span>           |
| <span data-ttu-id="aae96-130">短期的しきい値</span><span class="sxs-lookup"><span data-stu-id="aae96-130">Short-term threshold</span></span>                    | <span data-ttu-id="aae96-131">12</span><span class="sxs-lookup"><span data-stu-id="aae96-131">12</span></span>             |
| <span data-ttu-id="aae96-132">少額しきい値</span><span class="sxs-lookup"><span data-stu-id="aae96-132">Low Value Threshold</span></span>                     | <span data-ttu-id="aae96-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-133">5,000.00</span></span>       |
| <span data-ttu-id="aae96-134">仕入先への支払い</span><span class="sxs-lookup"><span data-stu-id="aae96-134">Pay to Vendor</span></span>                           | <span data-ttu-id="aae96-135">なし</span><span class="sxs-lookup"><span data-stu-id="aae96-135">No</span></span>             |

<span data-ttu-id="aae96-136">**法定帳簿**</span><span class="sxs-lookup"><span data-stu-id="aae96-136">**Statutory book**</span></span>

<span data-ttu-id="aae96-137">法定帳簿は現金基準の帳簿であり、リース料を毎月の家賃として支払う現金額として会計処理します。</span><span class="sxs-lookup"><span data-stu-id="aae96-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="aae96-138">この本は、使用権 (ROU) 資産やリース負債に関する法的責任を負わないものとします。</span><span class="sxs-lookup"><span data-stu-id="aae96-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="aae96-139">氏名</span><span class="sxs-lookup"><span data-stu-id="aae96-139">Name</span></span>                                    | <span data-ttu-id="aae96-140">説明</span><span class="sxs-lookup"><span data-stu-id="aae96-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="aae96-141">帳簿タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-141">Book type</span></span>                               | <span data-ttu-id="aae96-142">法令</span><span class="sxs-lookup"><span data-stu-id="aae96-142">Statutory</span></span>   |
| <span data-ttu-id="aae96-143">帳簿の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-143">Book description</span></span>                        | <span data-ttu-id="aae96-144">ローカル GAAP</span><span class="sxs-lookup"><span data-stu-id="aae96-144">Local GAAP</span></span>  |
| <span data-ttu-id="aae96-145">転記階層</span><span class="sxs-lookup"><span data-stu-id="aae96-145">Posting Layer</span></span>                           | <span data-ttu-id="aae96-146">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-146">Current</span></span>     |
| <span data-ttu-id="aae96-147">リース タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-147">Lease Type</span></span>                              | <span data-ttu-id="aae96-148">自動</span><span class="sxs-lookup"><span data-stu-id="aae96-148">Automatic</span></span>   |
| <span data-ttu-id="aae96-149">会計フレームワーク</span><span class="sxs-lookup"><span data-stu-id="aae96-149">Accounting Framework</span></span>                    | <span data-ttu-id="aae96-150">現金主義</span><span class="sxs-lookup"><span data-stu-id="aae96-150">Cash basis</span></span>  |
| <span data-ttu-id="aae96-151">リース期間 / 耐用年数の設定</span><span class="sxs-lookup"><span data-stu-id="aae96-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="aae96-152">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-152">0.00</span></span>        |
| <span data-ttu-id="aae96-153">現在の価値 / 資産の公正価値の設定</span><span class="sxs-lookup"><span data-stu-id="aae96-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="aae96-154">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-154">0.00</span></span>        |
| <span data-ttu-id="aae96-155">短期的しきい値</span><span class="sxs-lookup"><span data-stu-id="aae96-155">Short-term threshold</span></span>                    | <span data-ttu-id="aae96-156">0</span><span class="sxs-lookup"><span data-stu-id="aae96-156">0</span></span>           |
| <span data-ttu-id="aae96-157">少額しきい値</span><span class="sxs-lookup"><span data-stu-id="aae96-157">Low Value Threshold</span></span>                     | <span data-ttu-id="aae96-158">0</span><span class="sxs-lookup"><span data-stu-id="aae96-158">0</span></span>           |
| <span data-ttu-id="aae96-159">仕入先への支払い</span><span class="sxs-lookup"><span data-stu-id="aae96-159">Pay to Vendor</span></span>                           | <span data-ttu-id="aae96-160">なし</span><span class="sxs-lookup"><span data-stu-id="aae96-160">No</span></span>          |

<span data-ttu-id="aae96-161">**法定取消帳簿**</span><span class="sxs-lookup"><span data-stu-id="aae96-161">**Statutory reversal book**</span></span>

<span data-ttu-id="aae96-162">法定取消帳簿は、法定帳簿と同じ方法で設定されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="aae96-163">氏名</span><span class="sxs-lookup"><span data-stu-id="aae96-163">Name</span></span>                                    | <span data-ttu-id="aae96-164">説明</span><span class="sxs-lookup"><span data-stu-id="aae96-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="aae96-165">帳簿タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-165">Book type</span></span>                               | <span data-ttu-id="aae96-166">法定取消帳簿</span><span class="sxs-lookup"><span data-stu-id="aae96-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="aae96-167">帳簿の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-167">Book description</span></span>                        | <span data-ttu-id="aae96-168">法定帳簿の取消</span><span class="sxs-lookup"><span data-stu-id="aae96-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="aae96-169">転記階層</span><span class="sxs-lookup"><span data-stu-id="aae96-169">Posting Layer</span></span>                           | <span data-ttu-id="aae96-170">カスタム レイヤー 1</span><span class="sxs-lookup"><span data-stu-id="aae96-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="aae96-171">リース タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-171">Lease Type</span></span>                              | <span data-ttu-id="aae96-172">自動</span><span class="sxs-lookup"><span data-stu-id="aae96-172">Automatic</span></span>                      |
| <span data-ttu-id="aae96-173">会計フレームワーク</span><span class="sxs-lookup"><span data-stu-id="aae96-173">Accounting Framework</span></span>                    | <span data-ttu-id="aae96-174">現金主義</span><span class="sxs-lookup"><span data-stu-id="aae96-174">Cash basis</span></span>                     |
| <span data-ttu-id="aae96-175">リース期間 / 耐用年数の設定</span><span class="sxs-lookup"><span data-stu-id="aae96-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="aae96-176">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-176">0.00</span></span>                           |
| <span data-ttu-id="aae96-177">現在の価値 / 資産の公正価値の設定</span><span class="sxs-lookup"><span data-stu-id="aae96-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="aae96-178">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-178">0.00</span></span>                           |
| <span data-ttu-id="aae96-179">短期的しきい値</span><span class="sxs-lookup"><span data-stu-id="aae96-179">Short-term threshold</span></span>                    | <span data-ttu-id="aae96-180">0</span><span class="sxs-lookup"><span data-stu-id="aae96-180">0</span></span>                              |
| <span data-ttu-id="aae96-181">少額しきい値</span><span class="sxs-lookup"><span data-stu-id="aae96-181">Low Value Threshold</span></span>                     | <span data-ttu-id="aae96-182">0</span><span class="sxs-lookup"><span data-stu-id="aae96-182">0</span></span>                              |
| <span data-ttu-id="aae96-183">仕入先への支払い</span><span class="sxs-lookup"><span data-stu-id="aae96-183">Pay to Vendor</span></span>                           | <span data-ttu-id="aae96-184">なし</span><span class="sxs-lookup"><span data-stu-id="aae96-184">No</span></span>                             |

<span data-ttu-id="aae96-185">この例では、**全般** および **支払スケジュールの明細** タブで以下の設定を持つリースが作成されています。</span><span class="sxs-lookup"><span data-stu-id="aae96-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="aae96-186">**全般タブ**</span><span class="sxs-lookup"><span data-stu-id="aae96-186">**General tab**</span></span>

| <span data-ttu-id="aae96-187">フィールド</span><span class="sxs-lookup"><span data-stu-id="aae96-187">Field</span></span>                      | <span data-ttu-id="aae96-188">先頭値</span><span class="sxs-lookup"><span data-stu-id="aae96-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="aae96-189">追加借入利子率</span><span class="sxs-lookup"><span data-stu-id="aae96-189">Incremental borrowing rate</span></span> | <span data-ttu-id="aae96-190">5%</span><span class="sxs-lookup"><span data-stu-id="aae96-190">5%</span></span>               |
| <span data-ttu-id="aae96-191">開始日</span><span class="sxs-lookup"><span data-stu-id="aae96-191">Commencement date</span></span>          | <span data-ttu-id="aae96-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="aae96-192">1/1/2020</span></span>         |
| <span data-ttu-id="aae96-193">リース グループ</span><span class="sxs-lookup"><span data-stu-id="aae96-193">Lease group</span></span>                | <span data-ttu-id="aae96-194">建設物</span><span class="sxs-lookup"><span data-stu-id="aae96-194">Buildings</span></span>        |
| <span data-ttu-id="aae96-195">仕入先</span><span class="sxs-lookup"><span data-stu-id="aae96-195">Vendor</span></span>                     | <span data-ttu-id="aae96-196">1001</span><span class="sxs-lookup"><span data-stu-id="aae96-196">1001</span></span>             |
| <span data-ttu-id="aae96-197">資産の公正価値</span><span class="sxs-lookup"><span data-stu-id="aae96-197">Fair value of the asset</span></span>    | <span data-ttu-id="aae96-198">245,000</span><span class="sxs-lookup"><span data-stu-id="aae96-198">245,000</span></span>          |
| <span data-ttu-id="aae96-199">資産の耐用年数</span><span class="sxs-lookup"><span data-stu-id="aae96-199">Asset useful life</span></span>          | <span data-ttu-id="aae96-200">120</span><span class="sxs-lookup"><span data-stu-id="aae96-200">120</span></span>              |
| <span data-ttu-id="aae96-201">定期支払のタイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-201">Annuity type</span></span>               | <span data-ttu-id="aae96-202">通常の定期支払</span><span class="sxs-lookup"><span data-stu-id="aae96-202">Ordinary annuity</span></span> |
| <span data-ttu-id="aae96-203">複合間隔</span><span class="sxs-lookup"><span data-stu-id="aae96-203">Compounding interval</span></span>       | <span data-ttu-id="aae96-204">月 1 回</span><span class="sxs-lookup"><span data-stu-id="aae96-204">Monthly</span></span>          |

<span data-ttu-id="aae96-205">**支払スケジュール明細行タブ**</span><span class="sxs-lookup"><span data-stu-id="aae96-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="aae96-206">フィールド</span><span class="sxs-lookup"><span data-stu-id="aae96-206">Field</span></span>             | <span data-ttu-id="aae96-207">先頭値</span><span class="sxs-lookup"><span data-stu-id="aae96-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="aae96-208">開始日</span><span class="sxs-lookup"><span data-stu-id="aae96-208">Start date</span></span>        | <span data-ttu-id="aae96-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="aae96-209">1/1/2020</span></span>   |
| <span data-ttu-id="aae96-210">間隔</span><span class="sxs-lookup"><span data-stu-id="aae96-210">Period interval</span></span>   | <span data-ttu-id="aae96-211">月数</span><span class="sxs-lookup"><span data-stu-id="aae96-211">Months</span></span>     |
| <span data-ttu-id="aae96-212">期間</span><span class="sxs-lookup"><span data-stu-id="aae96-212">Periods</span></span>           | <span data-ttu-id="aae96-213">24</span><span class="sxs-lookup"><span data-stu-id="aae96-213">24</span></span>         |
| <span data-ttu-id="aae96-214">終了日</span><span class="sxs-lookup"><span data-stu-id="aae96-214">End date</span></span>          | <span data-ttu-id="aae96-215">2020/12/31</span><span class="sxs-lookup"><span data-stu-id="aae96-215">12/31/2020</span></span> |
| <span data-ttu-id="aae96-216">支払頻度</span><span class="sxs-lookup"><span data-stu-id="aae96-216">Payment frequency</span></span> | <span data-ttu-id="aae96-217">月 1 回</span><span class="sxs-lookup"><span data-stu-id="aae96-217">Monthly</span></span>    |
| <span data-ttu-id="aae96-218">支払額</span><span class="sxs-lookup"><span data-stu-id="aae96-218">Payment amount</span></span>    | <span data-ttu-id="aae96-219">1.000</span><span class="sxs-lookup"><span data-stu-id="aae96-219">1,000</span></span>      |

<span data-ttu-id="aae96-220">このリースを 2 つのフレームワークで考慮するには、現在の転記階層とカスタム転記階層を使用します。</span><span class="sxs-lookup"><span data-stu-id="aae96-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="aae96-221">以下の表は、各報告基準の下で財務情報を公正に表示することが要求される仕訳の例です。</span><span class="sxs-lookup"><span data-stu-id="aae96-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="aae96-222">リースの最初の月についての各仕訳入力の詳細な説明については後述します。</span><span class="sxs-lookup"><span data-stu-id="aae96-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="aae96-223">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="aae96-224">説明</span><span class="sxs-lookup"><span data-stu-id="aae96-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="aae96-225">法定帳簿 (現在の層)</span><span class="sxs-lookup"><span data-stu-id="aae96-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="aae96-226">現在のレイヤーの合計</span><span class="sxs-lookup"><span data-stu-id="aae96-226">Current layer total</span></span></th>
<th><span data-ttu-id="aae96-227">取消帳簿 (カスタム層)</span><span class="sxs-lookup"><span data-stu-id="aae96-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="aae96-228">IFRS 16 号 帳簿 (カスタム層)</span><span class="sxs-lookup"><span data-stu-id="aae96-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="aae96-229">現在のレイヤー + カスタム層の合計</span><span class="sxs-lookup"><span data-stu-id="aae96-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="aae96-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="aae96-230">JE-100</span></span></th>
<th><span data-ttu-id="aae96-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="aae96-231">JE-110</span></span></th>
<th><span data-ttu-id="aae96-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="aae96-232">JE-120</span></span></th>
<th><span data-ttu-id="aae96-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="aae96-233">JE-130</span></span></th>
<th><span data-ttu-id="aae96-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="aae96-234">JE-140</span></span></th>
<th><span data-ttu-id="aae96-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="aae96-235">JE-150</span></span></th>
<th><span data-ttu-id="aae96-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="aae96-236">JE-160</span></span></th>
<th><span data-ttu-id="aae96-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="aae96-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="aae96-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aae96-246">1</span><span class="sxs-lookup"><span data-stu-id="aae96-246">1</span></span></td>
<td><span data-ttu-id="aae96-247">リース経費</span><span class="sxs-lookup"><span data-stu-id="aae96-247">Lease expense</span></span></td>
<td><span data-ttu-id="aae96-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-249">1,000.00</span></span></td>
<td><span data-ttu-id="aae96-250">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-251">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-252">2</span><span class="sxs-lookup"><span data-stu-id="aae96-252">2</span></span></td>
<td><span data-ttu-id="aae96-253">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="aae96-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-254">3.00</span><span class="sxs-lookup"><span data-stu-id="aae96-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-255">3.00</span><span class="sxs-lookup"><span data-stu-id="aae96-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-256">3.00</span><span class="sxs-lookup"><span data-stu-id="aae96-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-257">3</span><span class="sxs-lookup"><span data-stu-id="aae96-257">3</span></span></td>
<td><span data-ttu-id="aae96-258">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="aae96-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-259">5.00</span><span class="sxs-lookup"><span data-stu-id="aae96-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-260">5.00</span><span class="sxs-lookup"><span data-stu-id="aae96-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-261">5.00</span><span class="sxs-lookup"><span data-stu-id="aae96-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-262">4</span><span class="sxs-lookup"><span data-stu-id="aae96-262">4</span></span></td>
<td><span data-ttu-id="aae96-263">清算勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-263">Clearing account</span></span></td>
<td><span data-ttu-id="aae96-264">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-264">-1,000.00</span></span></td>
<td><span data-ttu-id="aae96-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-266">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-266">0.00</span></span></td>
<td><span data-ttu-id="aae96-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-268">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-269">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-270">5</span><span class="sxs-lookup"><span data-stu-id="aae96-270">5</span></span></td>
<td><span data-ttu-id="aae96-271">買掛金</span><span class="sxs-lookup"><span data-stu-id="aae96-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-272">-1,008.00</span></span></td>
<td><span data-ttu-id="aae96-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-273">1,008.00</span></span></td>
<td><span data-ttu-id="aae96-274">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-275">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-276">6</span><span class="sxs-lookup"><span data-stu-id="aae96-276">6</span></span></td>
<td><span data-ttu-id="aae96-277">使用権資産</span><span class="sxs-lookup"><span data-stu-id="aae96-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-278">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="aae96-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="aae96-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-281">7</span><span class="sxs-lookup"><span data-stu-id="aae96-281">7</span></span></td>
<td><span data-ttu-id="aae96-282">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="aae96-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-283">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="aae96-284">-22,794.00</span></span></td>
<td><span data-ttu-id="aae96-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-285">1,000.00</span></span></td>
<td><span data-ttu-id="aae96-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="aae96-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="aae96-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-288">8</span><span class="sxs-lookup"><span data-stu-id="aae96-288">8</span></span></td>
<td><span data-ttu-id="aae96-289">支払利息</span><span class="sxs-lookup"><span data-stu-id="aae96-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-290">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-291">94.97</span><span class="sxs-lookup"><span data-stu-id="aae96-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-292">94.97</span><span class="sxs-lookup"><span data-stu-id="aae96-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-293">9</span><span class="sxs-lookup"><span data-stu-id="aae96-293">9</span></span></td>
<td><span data-ttu-id="aae96-294">現金</span><span class="sxs-lookup"><span data-stu-id="aae96-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-295">-1,008.00</span></span></td>
<td><span data-ttu-id="aae96-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-298">10</span><span class="sxs-lookup"><span data-stu-id="aae96-298">10</span></span></td>
<td><span data-ttu-id="aae96-299">減価償却費</span><span class="sxs-lookup"><span data-stu-id="aae96-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-300">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-301">949.75</span><span class="sxs-lookup"><span data-stu-id="aae96-301">949.75</span></span></td>
<td><span data-ttu-id="aae96-302">949.75</span><span class="sxs-lookup"><span data-stu-id="aae96-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-303">11</span><span class="sxs-lookup"><span data-stu-id="aae96-303">11</span></span></td>
<td><span data-ttu-id="aae96-304">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="aae96-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-305">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="aae96-306">-949.75</span></span></td>
<td><span data-ttu-id="aae96-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="aae96-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aae96-308">前の表に示すように、法定報告書と IFRS 報告書の両方で報告が必要な帳簿は 3 冊です。</span><span class="sxs-lookup"><span data-stu-id="aae96-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="aae96-309">法定帳簿には、流動層の下の現金主義会計のルールに従って、リース支払を記録しています。</span><span class="sxs-lookup"><span data-stu-id="aae96-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="aae96-310">法的取消帳簿により、法的仕訳入力が取り消されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="aae96-311">IFRS 16 号の帳簿では、IFRS 16 号に必要な仕訳入力が作成されています。</span><span class="sxs-lookup"><span data-stu-id="aae96-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="aae96-312">リースは 1 回だけ入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae96-312">You must enter a lease only one time.</span></span> <span data-ttu-id="aae96-313">その後、**帳簿** ページを開いて、このリースに関連付けられているすべての帳簿を表示できます。</span><span class="sxs-lookup"><span data-stu-id="aae96-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="aae96-314">帳簿を作成する際には、これらの 3 つのすべてが同じリース レコードに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae96-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="aae96-315">最初の仕訳入力には、法定帳簿でのリース経費が記録されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="aae96-316">支払は、一括で作成することも、法定帳簿の支払予定表を選択して作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="aae96-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="aae96-317">この例では、次の仕訳入力が支払スケジュールからの法定帳簿に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="aae96-318">リース支払 – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="aae96-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="aae96-319">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-319">Account type</span></span> | <span data-ttu-id="aae96-320">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-320">Account number</span></span> | <span data-ttu-id="aae96-321">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-321">Layer</span></span>   | <span data-ttu-id="aae96-322">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-322">Account description</span></span> | <span data-ttu-id="aae96-323">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-323">Debit</span></span>    | <span data-ttu-id="aae96-324">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="aae96-325">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-325">Ledger</span></span>       | <span data-ttu-id="aae96-326">1</span><span class="sxs-lookup"><span data-stu-id="aae96-326">1</span></span>              | <span data-ttu-id="aae96-327">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-327">Current</span></span> | <span data-ttu-id="aae96-328">リース経費</span><span class="sxs-lookup"><span data-stu-id="aae96-328">Lease expense</span></span>       | <span data-ttu-id="aae96-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-329">1,000.00</span></span> |          |
| <span data-ttu-id="aae96-330">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-330">Ledger</span></span>       | <span data-ttu-id="aae96-331">4</span><span class="sxs-lookup"><span data-stu-id="aae96-331">4</span></span>              | <span data-ttu-id="aae96-332">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-332">Current</span></span> | <span data-ttu-id="aae96-333">清算勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-333">Clearing account</span></span>    |          | <span data-ttu-id="aae96-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-334">1,000.00</span></span> |

<span data-ttu-id="aae96-335">買掛金勘定の担当者は、Dynamics 365 の標準機能を利用して、資産リース以外のリースに対する支払請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="aae96-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="aae96-336">しかし、借方勘定に **リースの経費** を選択する代わりに、買掛金勘定の担当者は次の入力を生成する精算勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae96-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="aae96-337">AP プロセス – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="aae96-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="aae96-338">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-338">Account type</span></span> | <span data-ttu-id="aae96-339">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-339">Account number</span></span> | <span data-ttu-id="aae96-340">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-340">Layer</span></span>   | <span data-ttu-id="aae96-341">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-341">Account description</span></span> | <span data-ttu-id="aae96-342">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-342">Debit</span></span>    | <span data-ttu-id="aae96-343">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="aae96-344">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-344">Ledger</span></span>       | <span data-ttu-id="aae96-345">4</span><span class="sxs-lookup"><span data-stu-id="aae96-345">4</span></span>              | <span data-ttu-id="aae96-346">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-346">Current</span></span> | <span data-ttu-id="aae96-347">清算勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-347">Clearing account</span></span>    | <span data-ttu-id="aae96-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-348">1,000.00</span></span> |          |
| <span data-ttu-id="aae96-349">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-349">Ledger</span></span>       | <span data-ttu-id="aae96-350">2</span><span class="sxs-lookup"><span data-stu-id="aae96-350">2</span></span>              | <span data-ttu-id="aae96-351">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-351">Current</span></span> | <span data-ttu-id="aae96-352">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="aae96-352">Bank fee</span></span>            | <span data-ttu-id="aae96-353">3.00</span><span class="sxs-lookup"><span data-stu-id="aae96-353">3.00</span></span>     |          |
| <span data-ttu-id="aae96-354">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-354">Ledger</span></span>       | <span data-ttu-id="aae96-355">3</span><span class="sxs-lookup"><span data-stu-id="aae96-355">3</span></span>              | <span data-ttu-id="aae96-356">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-356">Current</span></span> | <span data-ttu-id="aae96-357">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="aae96-357">VAT expense</span></span>         | <span data-ttu-id="aae96-358">5.00</span><span class="sxs-lookup"><span data-stu-id="aae96-358">5.00</span></span>     |          |
| <span data-ttu-id="aae96-359">仕入先</span><span class="sxs-lookup"><span data-stu-id="aae96-359">Vendor</span></span>       | <span data-ttu-id="aae96-360">5</span><span class="sxs-lookup"><span data-stu-id="aae96-360">5</span></span>              | <span data-ttu-id="aae96-361">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-361">Current</span></span> | <span data-ttu-id="aae96-362">買掛金</span><span class="sxs-lookup"><span data-stu-id="aae96-362">Accounts payable</span></span>    |          | <span data-ttu-id="aae96-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-363">1,008.00</span></span> |

<span data-ttu-id="aae96-364">仕入先に対して明細書を発行すると、通常の支払い手続きを行います。</span><span class="sxs-lookup"><span data-stu-id="aae96-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="aae96-365">このプロセスでは、次の仕訳入力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="aae96-366">現金支払 – 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="aae96-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="aae96-367">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-367">Account type</span></span> | <span data-ttu-id="aae96-368">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-368">Account number</span></span> | <span data-ttu-id="aae96-369">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-369">Layer</span></span>   | <span data-ttu-id="aae96-370">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-370">Account description</span></span> | <span data-ttu-id="aae96-371">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-371">Debit</span></span>    | <span data-ttu-id="aae96-372">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="aae96-373">仕入先</span><span class="sxs-lookup"><span data-stu-id="aae96-373">Vendor</span></span>       | <span data-ttu-id="aae96-374">5</span><span class="sxs-lookup"><span data-stu-id="aae96-374">5</span></span>              | <span data-ttu-id="aae96-375">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-375">Current</span></span> | <span data-ttu-id="aae96-376">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-376">Accounts Payable</span></span>    | <span data-ttu-id="aae96-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-377">1,008.00</span></span> |          |
| <span data-ttu-id="aae96-378">銀行</span><span class="sxs-lookup"><span data-stu-id="aae96-378">Bank</span></span>         | <span data-ttu-id="aae96-379">9</span><span class="sxs-lookup"><span data-stu-id="aae96-379">9</span></span>              | <span data-ttu-id="aae96-380">現行</span><span class="sxs-lookup"><span data-stu-id="aae96-380">Current</span></span> | <span data-ttu-id="aae96-381">現金</span><span class="sxs-lookup"><span data-stu-id="aae96-381">Cash</span></span>                |          | <span data-ttu-id="aae96-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-382">1,008.00</span></span> |

<span data-ttu-id="aae96-383">この時点で、このリースを法定の報告要件に基づいて完全に会計処理されており、現在の層を使用して試算表を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="aae96-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="aae96-384">システムからは、次の図を含む試算表が返されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="aae96-385">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="aae96-386">説明</span><span class="sxs-lookup"><span data-stu-id="aae96-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="aae96-387">法定帳簿 (現在の層)</span><span class="sxs-lookup"><span data-stu-id="aae96-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="aae96-388">現在のレイヤーの合計</span><span class="sxs-lookup"><span data-stu-id="aae96-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="aae96-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="aae96-389">JE-100</span></span></th>
<th><span data-ttu-id="aae96-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="aae96-390">JE-110</span></span></th>
<th><span data-ttu-id="aae96-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="aae96-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="aae96-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="aae96-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="aae96-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aae96-395">1</span><span class="sxs-lookup"><span data-stu-id="aae96-395">1</span></span></td>
<td><span data-ttu-id="aae96-396">リース経費</span><span class="sxs-lookup"><span data-stu-id="aae96-396">Lease expense</span></span></td>
<td><span data-ttu-id="aae96-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-399">2</span><span class="sxs-lookup"><span data-stu-id="aae96-399">2</span></span></td>
<td><span data-ttu-id="aae96-400">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="aae96-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-401">3.00</span><span class="sxs-lookup"><span data-stu-id="aae96-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-402">3.00</span><span class="sxs-lookup"><span data-stu-id="aae96-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-403">3</span><span class="sxs-lookup"><span data-stu-id="aae96-403">3</span></span></td>
<td><span data-ttu-id="aae96-404">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="aae96-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-405">5.00</span><span class="sxs-lookup"><span data-stu-id="aae96-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-406">5.00</span><span class="sxs-lookup"><span data-stu-id="aae96-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-407">4</span><span class="sxs-lookup"><span data-stu-id="aae96-407">4</span></span></td>
<td><span data-ttu-id="aae96-408">清算勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-408">Clearing account</span></span></td>
<td><span data-ttu-id="aae96-409">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-409">-1,000.00</span></span></td>
<td><span data-ttu-id="aae96-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-411">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-412">5</span><span class="sxs-lookup"><span data-stu-id="aae96-412">5</span></span></td>
<td><span data-ttu-id="aae96-413">買掛金</span><span class="sxs-lookup"><span data-stu-id="aae96-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="aae96-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-414">-1,008.00</span></span></td>
<td><span data-ttu-id="aae96-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-415">1,008.00</span></span></td>
<td><span data-ttu-id="aae96-416">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-417">6</span><span class="sxs-lookup"><span data-stu-id="aae96-417">6</span></span></td>
<td><span data-ttu-id="aae96-418">使用権資産</span><span class="sxs-lookup"><span data-stu-id="aae96-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-419">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-420">7</span><span class="sxs-lookup"><span data-stu-id="aae96-420">7</span></span></td>
<td><span data-ttu-id="aae96-421">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="aae96-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-422">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-423">8</span><span class="sxs-lookup"><span data-stu-id="aae96-423">8</span></span></td>
<td><span data-ttu-id="aae96-424">支払利息</span><span class="sxs-lookup"><span data-stu-id="aae96-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-425">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-426">9</span><span class="sxs-lookup"><span data-stu-id="aae96-426">9</span></span></td>
<td><span data-ttu-id="aae96-427">現金</span><span class="sxs-lookup"><span data-stu-id="aae96-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-428">-1,008.00</span></span></td>
<td><span data-ttu-id="aae96-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="aae96-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-430">10</span><span class="sxs-lookup"><span data-stu-id="aae96-430">10</span></span></td>
<td><span data-ttu-id="aae96-431">減価償却費</span><span class="sxs-lookup"><span data-stu-id="aae96-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-432">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aae96-433">11</span><span class="sxs-lookup"><span data-stu-id="aae96-433">11</span></span></td>
<td><span data-ttu-id="aae96-434">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="aae96-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="aae96-435">0.00</span><span class="sxs-lookup"><span data-stu-id="aae96-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aae96-436">IFRS 16 号の数字を使って同じ試算表を実行する場合は、法定会計の仕訳を取り消して、IFRS 16号の仕訳を転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae96-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="aae96-437">この例では、法定仕訳を取り消すにあたり、法定帳簿と同じ設定でありながら、反対の転記プロファイルを持つ法定取消帳簿が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aae96-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="aae96-438">たとえば、法定帳簿はリース費用勘定を *引き落とし* ていますが、取消帳簿はこの勘定を *計上* します。</span><span class="sxs-lookup"><span data-stu-id="aae96-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="aae96-439">これらの関係は、**資産リースパラメーター** ページ (**資産リース \> 設定 \> 資産のリース パラメーター**) の資産リースの転記勘定で簡単に定義できます。</span><span class="sxs-lookup"><span data-stu-id="aae96-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="aae96-440">法定帳簿に使用されたものと同じプロセスが取消帳簿に使用されると、次の仕訳入力が作成されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="aae96-441">この違いは、取消帳簿が法定帳簿からの取消記載を記載している点にあります。</span><span class="sxs-lookup"><span data-stu-id="aae96-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="aae96-442">取消の入力は、カスタム層にも作成されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="aae96-443">試算表を現在の層で実行すると、取消仕訳の入力は含まれません。</span><span class="sxs-lookup"><span data-stu-id="aae96-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="aae96-444">リース支払 – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="aae96-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="aae96-445">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-445">Account type</span></span> | <span data-ttu-id="aae96-446">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-446">Account number</span></span> | <span data-ttu-id="aae96-447">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-447">Layer</span></span>  | <span data-ttu-id="aae96-448">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-448">Account description</span></span> | <span data-ttu-id="aae96-449">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-449">Debit</span></span>    | <span data-ttu-id="aae96-450">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="aae96-451">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-451">Ledger</span></span>       | <span data-ttu-id="aae96-452">4</span><span class="sxs-lookup"><span data-stu-id="aae96-452">4</span></span>              | <span data-ttu-id="aae96-453">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-453">Custom</span></span> | <span data-ttu-id="aae96-454">清算勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-454">Clearing account</span></span>    | <span data-ttu-id="aae96-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-455">1,000.00</span></span> |          |
| <span data-ttu-id="aae96-456">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-456">Ledger</span></span>       | <span data-ttu-id="aae96-457">1</span><span class="sxs-lookup"><span data-stu-id="aae96-457">1</span></span>              | <span data-ttu-id="aae96-458">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-458">Custom</span></span> | <span data-ttu-id="aae96-459">リース経費</span><span class="sxs-lookup"><span data-stu-id="aae96-459">Lease expense</span></span>       |          | <span data-ttu-id="aae96-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-460">1,000.00</span></span> |

<span data-ttu-id="aae96-461">以上で法定仕訳の入力が削除されたため、IFRS 16号で要求されている仕訳をすべて IFRS 16号の帳簿に計上することになります。</span><span class="sxs-lookup"><span data-stu-id="aae96-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="aae96-462">これらの入力には、使用権資産と負債の当初認識および、利息と減価償却の記録が含まれます。</span><span class="sxs-lookup"><span data-stu-id="aae96-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="aae96-463">当初認識 – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="aae96-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="aae96-464">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-464">Account type</span></span> | <span data-ttu-id="aae96-465">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-465">Account number</span></span> | <span data-ttu-id="aae96-466">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-466">Layer</span></span>  | <span data-ttu-id="aae96-467">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-467">Account description</span></span>      | <span data-ttu-id="aae96-468">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-468">Debit</span></span>     | <span data-ttu-id="aae96-469">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="aae96-470">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-470">Ledger</span></span>       | <span data-ttu-id="aae96-471">6</span><span class="sxs-lookup"><span data-stu-id="aae96-471">6</span></span>              | <span data-ttu-id="aae96-472">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-472">Custom</span></span> | <span data-ttu-id="aae96-473">使用権資産</span><span class="sxs-lookup"><span data-stu-id="aae96-473">ROU Asset</span></span>                | <span data-ttu-id="aae96-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="aae96-474">22,793.90</span></span> |           |
| <span data-ttu-id="aae96-475">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-475">Ledger</span></span>       | <span data-ttu-id="aae96-476">7</span><span class="sxs-lookup"><span data-stu-id="aae96-476">7</span></span>              | <span data-ttu-id="aae96-477">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-477">Custom</span></span> | <span data-ttu-id="aae96-478">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="aae96-478">Finance lease obligation</span></span> |           | <span data-ttu-id="aae96-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="aae96-479">22,793.90</span></span> |

<span data-ttu-id="aae96-480">リース支払は、他のリース支払と同じように転記されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="aae96-481">清算勘定を使用する理由は、現金を一度だけ貸方に確実に転記するためです。</span><span class="sxs-lookup"><span data-stu-id="aae96-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="aae96-482">リース支払 – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="aae96-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="aae96-483">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-483">Account type</span></span> | <span data-ttu-id="aae96-484">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-484">Account number</span></span> | <span data-ttu-id="aae96-485">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-485">Layer</span></span>  | <span data-ttu-id="aae96-486">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-486">Account description</span></span>      | <span data-ttu-id="aae96-487">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-487">Debit</span></span>    | <span data-ttu-id="aae96-488">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="aae96-489">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-489">Ledger</span></span>       | <span data-ttu-id="aae96-490">7</span><span class="sxs-lookup"><span data-stu-id="aae96-490">7</span></span>              | <span data-ttu-id="aae96-491">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-491">Custom</span></span> | <span data-ttu-id="aae96-492">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="aae96-492">Finance lease obligation</span></span> | <span data-ttu-id="aae96-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-493">1,000.00</span></span> |          |
| <span data-ttu-id="aae96-494">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-494">Ledger</span></span>       | <span data-ttu-id="aae96-495">4</span><span class="sxs-lookup"><span data-stu-id="aae96-495">4</span></span>              | <span data-ttu-id="aae96-496">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-496">Custom</span></span> | <span data-ttu-id="aae96-497">清算勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-497">Clearing account</span></span>         |          | <span data-ttu-id="aae96-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="aae96-498">1,000.00</span></span> |

<span data-ttu-id="aae96-499">支払利息の仕訳入力は、負債の償却スケジュールから生成されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="aae96-500">支払利息 – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="aae96-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="aae96-501">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-501">Account type</span></span> | <span data-ttu-id="aae96-502">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-502">Account number</span></span> | <span data-ttu-id="aae96-503">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-503">Layer</span></span>  | <span data-ttu-id="aae96-504">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-504">Account description</span></span>      | <span data-ttu-id="aae96-505">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-505">Debit</span></span> | <span data-ttu-id="aae96-506">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="aae96-507">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-507">Ledger</span></span>       | <span data-ttu-id="aae96-508">8</span><span class="sxs-lookup"><span data-stu-id="aae96-508">8</span></span>              | <span data-ttu-id="aae96-509">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-509">Custom</span></span> | <span data-ttu-id="aae96-510">支払利息</span><span class="sxs-lookup"><span data-stu-id="aae96-510">Interest expense</span></span>         | <span data-ttu-id="aae96-511">94.97</span><span class="sxs-lookup"><span data-stu-id="aae96-511">94.97</span></span> |        |
| <span data-ttu-id="aae96-512">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-512">Ledger</span></span>       | <span data-ttu-id="aae96-513">7</span><span class="sxs-lookup"><span data-stu-id="aae96-513">7</span></span>              | <span data-ttu-id="aae96-514">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-514">Custom</span></span> | <span data-ttu-id="aae96-515">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="aae96-515">Finance lease obligation</span></span> |       | <span data-ttu-id="aae96-516">94.97</span><span class="sxs-lookup"><span data-stu-id="aae96-516">94.97</span></span>  |

<span data-ttu-id="aae96-517">減価償却費の仕訳は、資産の減価償却スケジュールから生成されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="aae96-518">減価償却費 – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="aae96-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="aae96-519">勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="aae96-519">Account type</span></span> | <span data-ttu-id="aae96-520">勘定番号</span><span class="sxs-lookup"><span data-stu-id="aae96-520">Account number</span></span> | <span data-ttu-id="aae96-521">レイヤー</span><span class="sxs-lookup"><span data-stu-id="aae96-521">Layer</span></span>  | <span data-ttu-id="aae96-522">勘定の説明</span><span class="sxs-lookup"><span data-stu-id="aae96-522">Account description</span></span>      | <span data-ttu-id="aae96-523">借方</span><span class="sxs-lookup"><span data-stu-id="aae96-523">Debit</span></span>  | <span data-ttu-id="aae96-524">貸方</span><span class="sxs-lookup"><span data-stu-id="aae96-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="aae96-525">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-525">Ledger</span></span>       | <span data-ttu-id="aae96-526">10</span><span class="sxs-lookup"><span data-stu-id="aae96-526">10</span></span>             | <span data-ttu-id="aae96-527">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-527">Custom</span></span> | <span data-ttu-id="aae96-528">減価償却費</span><span class="sxs-lookup"><span data-stu-id="aae96-528">Depreciation expense</span></span>     | <span data-ttu-id="aae96-529">949.75</span><span class="sxs-lookup"><span data-stu-id="aae96-529">949.75</span></span> |        |
| <span data-ttu-id="aae96-530">会計</span><span class="sxs-lookup"><span data-stu-id="aae96-530">Ledger</span></span>       | <span data-ttu-id="aae96-531">11</span><span class="sxs-lookup"><span data-stu-id="aae96-531">11</span></span>             | <span data-ttu-id="aae96-532">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="aae96-532">Custom</span></span> | <span data-ttu-id="aae96-533">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="aae96-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="aae96-534">949.75</span><span class="sxs-lookup"><span data-stu-id="aae96-534">949.75</span></span> |

<span data-ttu-id="aae96-535">これらすべての仕訳入力が作成され、転記されると、次のような "カスタム層 1" の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aae96-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="aae96-536">最後の列には、銀行手数料、付加価値税 (VAT) の費用、前の層からの現金の減額が含まれていますが、法定報告仕訳帳のエントリは含まれていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="aae96-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="aae96-537">したがって、本来的なデュアルレポート機能を実現できます。</span><span class="sxs-lookup"><span data-stu-id="aae96-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="aae96-538">この時点で、会社は試算表を実行し、現在のレイヤーとカスタム レイヤーを結合して IFRS 試算表を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae96-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="aae96-539">口座番号</span><span class="sxs-lookup"><span data-stu-id="aae96-539">Account No</span></span> | <span data-ttu-id="aae96-540">説明</span><span class="sxs-lookup"><span data-stu-id="aae96-540">Description</span></span>              | <span data-ttu-id="aae96-541">法定帳簿\-現在のレイヤー \-JE \-100 \-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-542">法定帳簿\-現在のレイヤー \-JE \-110 \-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-543">法定帳簿\-現在のレイヤー \-JE \-120 \-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-544">現在のレイヤー \- 合計</span><span class="sxs-lookup"><span data-stu-id="aae96-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="aae96-545">取消帳簿\-カスタム レイヤー\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-546">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-547">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-548">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-549">IFRS 16 号帳簿\-カスタム レイヤー\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="aae96-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="aae96-550">カスタム レイヤー\+ 現在のレイヤー \- 合計</span><span class="sxs-lookup"><span data-stu-id="aae96-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="aae96-551">1</span><span class="sxs-lookup"><span data-stu-id="aae96-551">1</span></span>          | <span data-ttu-id="aae96-552">リース経費</span><span class="sxs-lookup"><span data-stu-id="aae96-552">Lease expense</span></span>            | <span data-ttu-id="aae96-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="aae96-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-554">1,000\.00</span></span>               |   | <span data-ttu-id="aae96-555">\-1,000</span><span class="sxs-lookup"><span data-stu-id="aae96-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="aae96-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-556">0\.00</span></span>                                   |
| <span data-ttu-id="aae96-557">2</span><span class="sxs-lookup"><span data-stu-id="aae96-557">2</span></span>          | <span data-ttu-id="aae96-558">銀行手数料</span><span class="sxs-lookup"><span data-stu-id="aae96-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="aae96-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="aae96-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="aae96-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-561">3\.00</span></span>                                   |
| <span data-ttu-id="aae96-562">3</span><span class="sxs-lookup"><span data-stu-id="aae96-562">3</span></span>          | <span data-ttu-id="aae96-563">VAT 経費</span><span class="sxs-lookup"><span data-stu-id="aae96-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="aae96-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="aae96-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="aae96-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-566">5\.00</span></span>                                   |
| <span data-ttu-id="aae96-567">4</span><span class="sxs-lookup"><span data-stu-id="aae96-567">4</span></span>          | <span data-ttu-id="aae96-568">清算勘定</span><span class="sxs-lookup"><span data-stu-id="aae96-568">Clearing account</span></span>         | <span data-ttu-id="aae96-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="aae96-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="aae96-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-571">0\.00</span></span>                   |   | <span data-ttu-id="aae96-572">1.000</span><span class="sxs-lookup"><span data-stu-id="aae96-572">1,000</span></span>                                           |                                                | <span data-ttu-id="aae96-573">\-1,000</span><span class="sxs-lookup"><span data-stu-id="aae96-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="aae96-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-574">0\.00</span></span>                                   |
| <span data-ttu-id="aae96-575">5</span><span class="sxs-lookup"><span data-stu-id="aae96-575">5</span></span>          | <span data-ttu-id="aae96-576">買掛金</span><span class="sxs-lookup"><span data-stu-id="aae96-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="aae96-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="aae96-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-578">1,008\.00</span></span>                                         | <span data-ttu-id="aae96-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="aae96-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-580">0\.00</span></span>                                   |
| <span data-ttu-id="aae96-581">6</span><span class="sxs-lookup"><span data-stu-id="aae96-581">6</span></span>          | <span data-ttu-id="aae96-582">使用権資産</span><span class="sxs-lookup"><span data-stu-id="aae96-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="aae96-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="aae96-584">22,794</span><span class="sxs-lookup"><span data-stu-id="aae96-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="aae96-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="aae96-585">22,793\.90</span></span>                              |
| <span data-ttu-id="aae96-586">7</span><span class="sxs-lookup"><span data-stu-id="aae96-586">7</span></span>          | <span data-ttu-id="aae96-587">ファイナンス リースの責務</span><span class="sxs-lookup"><span data-stu-id="aae96-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="aae96-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="aae96-589">\-22,794</span><span class="sxs-lookup"><span data-stu-id="aae96-589">\-22,794</span></span>                                       | <span data-ttu-id="aae96-590">1.000</span><span class="sxs-lookup"><span data-stu-id="aae96-590">1,000</span></span>                                          | <span data-ttu-id="aae96-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="aae96-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="aae96-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="aae96-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="aae96-593">8</span><span class="sxs-lookup"><span data-stu-id="aae96-593">8</span></span>          | <span data-ttu-id="aae96-594">支払利息</span><span class="sxs-lookup"><span data-stu-id="aae96-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="aae96-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="aae96-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="aae96-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="aae96-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="aae96-597">94\.97</span></span>                                  |
| <span data-ttu-id="aae96-598">9</span><span class="sxs-lookup"><span data-stu-id="aae96-598">9</span></span>          | <span data-ttu-id="aae96-599">現金</span><span class="sxs-lookup"><span data-stu-id="aae96-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="aae96-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="aae96-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="aae96-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="aae96-603">10</span><span class="sxs-lookup"><span data-stu-id="aae96-603">10</span></span>         | <span data-ttu-id="aae96-604">減価償却費</span><span class="sxs-lookup"><span data-stu-id="aae96-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="aae96-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="aae96-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="aae96-606">949\.75</span></span>                                        | <span data-ttu-id="aae96-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="aae96-607">949\.75</span></span>                                 |
| <span data-ttu-id="aae96-608">11</span><span class="sxs-lookup"><span data-stu-id="aae96-608">11</span></span>         | <span data-ttu-id="aae96-609">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="aae96-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="aae96-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="aae96-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="aae96-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="aae96-611">\-949\.75</span></span>                                      | <span data-ttu-id="aae96-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="aae96-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]