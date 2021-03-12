---
title: 一般仕訳帳明細行での消費税計算
description: このトピックでは、一般仕訳帳明細行のさまざまなタイプの勘定 (仕入先、顧客、元帳、およびプロジェクト) に対する消費税がどのように計算されるかについて説明します。
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e420632c248b5b43d4983c5eb483cac580e67f20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975561"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="667aa-103">一般仕訳帳明細行での消費税計算</span><span class="sxs-lookup"><span data-stu-id="667aa-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="667aa-104">このトピックでは、一般仕訳帳明細行のさまざまなタイプの勘定 (仕入先、顧客、元帳、およびプロジェクト) に対する消費税がどのように計算されるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="667aa-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="667aa-105">プロセスは、次の 3 つの手順に分けられます。</span><span class="sxs-lookup"><span data-stu-id="667aa-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="667aa-106">消費税提示方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="667aa-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="667aa-107">一時的な消費税テーブルに保管される消費税金額を決定します。</span><span class="sxs-lookup"><span data-stu-id="667aa-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="667aa-108">伝票の消費税金額および勘定を決定します。</span><span class="sxs-lookup"><span data-stu-id="667aa-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="667aa-109">消費税提示方法を決定する</span><span class="sxs-lookup"><span data-stu-id="667aa-109">Determine the sales tax direction</span></span>

<span data-ttu-id="667aa-110">消費税提示方法が決定される方法は、伝票の勘定のタイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="667aa-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="667aa-111">消費税提示方法は、勘定タイプと消費税コードの組み合わせによって決まります。</span><span class="sxs-lookup"><span data-stu-id="667aa-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="667aa-112">次のセクションでは、その可能性についてさらに詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="667aa-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="667aa-113">勘定タイプはプロジェクトの場合</span><span class="sxs-lookup"><span data-stu-id="667aa-113">Account type is Project</span></span>

<span data-ttu-id="667aa-114">伝票に勘定タイプが **プロジェクト** である仕訳帳明細行がある場合、伝票の仕訳帳明細行すべてに同じ税提示方法が適用されます。</span><span class="sxs-lookup"><span data-stu-id="667aa-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="667aa-115">以下の図は、ルールを示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-115">The following illustration shows the rule.</span></span> <span data-ttu-id="667aa-116">次の点は、プロジェクト勘定に対して可能性のある税提示方法を示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="667aa-117">•   消費税コードが使用税である場合、消費税提示方法は使用税になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="667aa-118">•   消費税コードが免税である場合、消費税提示方法は免税仕入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="667aa-119">•   消費税コードがイントラコム VAT である場合、消費税提示方法は消費税支払になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="667aa-120">•   消費税コードが逆請求である場合、消費税提示方法は消費税支払になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="667aa-121">それ以外の場合、消費税提示方法は消費税収入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="667aa-122">次の図では、ルールをグラフィック表示しています。</span><span class="sxs-lookup"><span data-stu-id="667aa-122">The following diagram illustrates the rule graphically.</span></span>

![プロジェクト勘定に対する税提示方法の可能性](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="667aa-124">勘定タイプが仕入先の場合</span><span class="sxs-lookup"><span data-stu-id="667aa-124">Account type is Vendor</span></span>

<span data-ttu-id="667aa-125">伝票に勘定タイプが **仕入先** である仕訳帳明細行がある場合、伝票の仕訳帳明細行すべてに同じ税提示方法が適用されます。</span><span class="sxs-lookup"><span data-stu-id="667aa-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="667aa-126">次の点は、仕入先勘定に対して可能性のある税提示方法を示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="667aa-127">•   消費税コードが使用税である場合、消費税提示方法は使用税になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="667aa-128">•   消費税コードが免税である場合、消費税提示方法は免税仕入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="667aa-129">•   消費税コードがイントラコム VAT である場合、消費税提示方法は消費税支払になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="667aa-130">•   消費税コードが逆請求である場合、消費税提示方法は消費税支払になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="667aa-131">それ以外の場合、消費税提示方法は消費税収入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="667aa-132">次の図では、ルールをグラフィック表示しています。</span><span class="sxs-lookup"><span data-stu-id="667aa-132">The following diagram illustrates the rule graphically.</span></span>

![仕入先勘定に対する税提示方法の可能性](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="667aa-134">勘定タイプが顧客の場合</span><span class="sxs-lookup"><span data-stu-id="667aa-134">Account type is Customer</span></span>

<span data-ttu-id="667aa-135">伝票に勘定タイプが **顧客** である仕訳帳明細行がある場合、伝票の仕訳帳明細行すべてに同じ税提示方法が適用されます。</span><span class="sxs-lookup"><span data-stu-id="667aa-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="667aa-136">次の点は、顧客勘定に対して可能性のある税提示方法を示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="667aa-137">•   消費税コードが免税である場合、消費税提示方法は免税仕入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="667aa-138">•   消費税コードがイントラコム VAT である場合、消費税提示方法は消費税収入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="667aa-139">•   消費税コードが逆請求である場合、消費税提示方法は消費税収入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="667aa-140">それ以外の場合、消費税提示方法は消費税支払になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="667aa-141">次の図では、ルールをグラフィック表示しています。</span><span class="sxs-lookup"><span data-stu-id="667aa-141">The following diagram illustrates the rule graphically.</span></span>

![顧客勘定に対する税提示方法の可能性](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="667aa-143">勘定タイプが元帳の場合</span><span class="sxs-lookup"><span data-stu-id="667aa-143">Account type is Ledger</span></span>

<span data-ttu-id="667aa-144">次の図は、伝票に勘定タイプが **元帳** である仕訳帳明細行のみがある場合に適用されるルールを示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="667aa-145">次の点は、元帳勘定に対して可能性のある税提示方法を示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="667aa-146">•   消費税コードが使用税である場合、消費税提示方法は使用税になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="667aa-147">•   消費税コードが免税である場合、消費税提示方法は免税仕入になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="667aa-148">それ以外は、仕訳帳金額が借方 (正) の場合、消費税提示方法は消費税収入になります。仕訳帳金額が貸方 (負) の場合、消費税提示方法は消費税支払になります。</span><span class="sxs-lookup"><span data-stu-id="667aa-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="667aa-149">次の図では、ルールをグラフィック表示しています。</span><span class="sxs-lookup"><span data-stu-id="667aa-149">The following diagram illustrates the rule graphically.</span></span>

![元帳勘定に対する税提示方法の可能性](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="667aa-151">消費税提示方法を上書きする</span><span class="sxs-lookup"><span data-stu-id="667aa-151">Override the sales tax direction</span></span>

<span data-ttu-id="667aa-152">伝票に勘定タイプが **元帳** である明細行のみが含まれている場合は、消費税提示方法を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="667aa-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="667aa-153">**一般会計 \> 勘定科目表 \> 勘定 \> 主勘定** の順に移動し、**法人の上書き** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="667aa-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="667aa-154">消費税金額を決定する</span><span class="sxs-lookup"><span data-stu-id="667aa-154">Determine the sales tax amount</span></span>

<span data-ttu-id="667aa-155">このセクションでは、消費税金額の符号の計算方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="667aa-155">This section describes how the sales tax amount sign is calculated.</span></span>

![消費税トランザクション ページ](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="667aa-157">次の表では、一時的な消費税テーブルで消費税金額の符号を決定する一般的なルールを示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="667aa-158">仕訳帳明細行の金額</span><span class="sxs-lookup"><span data-stu-id="667aa-158">Journal line amount</span></span> | <span data-ttu-id="667aa-159">消費税提示方法</span><span class="sxs-lookup"><span data-stu-id="667aa-159">Sales tax direction</span></span>  | <span data-ttu-id="667aa-160">消費税金額の符号</span><span class="sxs-lookup"><span data-stu-id="667aa-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="667aa-161">正</span><span class="sxs-lookup"><span data-stu-id="667aa-161">Positive</span></span>            | <span data-ttu-id="667aa-162">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-162">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-163">正</span><span class="sxs-lookup"><span data-stu-id="667aa-163">Positive</span></span>              |
| <span data-ttu-id="667aa-164">正</span><span class="sxs-lookup"><span data-stu-id="667aa-164">Positive</span></span>            | <span data-ttu-id="667aa-165">消費税支払</span><span class="sxs-lookup"><span data-stu-id="667aa-165">Sales Tax Payable</span></span>    | <span data-ttu-id="667aa-166">負</span><span class="sxs-lookup"><span data-stu-id="667aa-166">Negative</span></span>              |
| <span data-ttu-id="667aa-167">負</span><span class="sxs-lookup"><span data-stu-id="667aa-167">Negative</span></span>            | <span data-ttu-id="667aa-168">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-168">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-169">負</span><span class="sxs-lookup"><span data-stu-id="667aa-169">Negative</span></span>              |
| <span data-ttu-id="667aa-170">負</span><span class="sxs-lookup"><span data-stu-id="667aa-170">Negative</span></span>            | <span data-ttu-id="667aa-171">消費税支払</span><span class="sxs-lookup"><span data-stu-id="667aa-171">Sales Tax Payable</span></span>    | <span data-ttu-id="667aa-172">正</span><span class="sxs-lookup"><span data-stu-id="667aa-172">Positive</span></span>              |

<span data-ttu-id="667aa-173">**元帳** 明細行で消費税グループまたは品目消費税グループが選択されている場合、**プロジェクト** または **元帳** 明細行のみを持つ伝票に対して特別なルールがあります。</span><span class="sxs-lookup"><span data-stu-id="667aa-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="667aa-174">このルールは、一般仕訳帳の独立した消費税計算機能を有効にすることにより制御されます。</span><span class="sxs-lookup"><span data-stu-id="667aa-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="667aa-175">この機能をオフにすると、**元帳** 明細行の税金額は、**プロジェクト** 明細行の借方/貸方の方向を使用します。</span><span class="sxs-lookup"><span data-stu-id="667aa-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="667aa-176">機能をオンにすると、**元帳** 明細行の税金額はそれ自体の借方/貸方の方向を使用します。</span><span class="sxs-lookup"><span data-stu-id="667aa-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="667aa-177">次の表では、各シナリオのルールを示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="667aa-178">**機能がオンになっている場合のルール**</span><span class="sxs-lookup"><span data-stu-id="667aa-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="667aa-179">プロジェクトの仕訳帳明細行の金額</span><span class="sxs-lookup"><span data-stu-id="667aa-179">Journal line amount of project</span></span> | <span data-ttu-id="667aa-180">消費税提示方法</span><span class="sxs-lookup"><span data-stu-id="667aa-180">Sales tax direction</span></span>  | <span data-ttu-id="667aa-181">消費税金額の符号</span><span class="sxs-lookup"><span data-stu-id="667aa-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="667aa-182">正</span><span class="sxs-lookup"><span data-stu-id="667aa-182">Positive</span></span>                       | <span data-ttu-id="667aa-183">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-183">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-184">正</span><span class="sxs-lookup"><span data-stu-id="667aa-184">Positive</span></span>              |
| <span data-ttu-id="667aa-185">負</span><span class="sxs-lookup"><span data-stu-id="667aa-185">Negative</span></span>                       | <span data-ttu-id="667aa-186">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-186">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-187">負</span><span class="sxs-lookup"><span data-stu-id="667aa-187">Negative</span></span>              |

<span data-ttu-id="667aa-188">**機能がオフになっている場合のルール**</span><span class="sxs-lookup"><span data-stu-id="667aa-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="667aa-189">元帳の仕訳帳明細行の金額</span><span class="sxs-lookup"><span data-stu-id="667aa-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="667aa-190">消費税提示方法</span><span class="sxs-lookup"><span data-stu-id="667aa-190">Sales tax direction</span></span>  | <span data-ttu-id="667aa-191">消費税金額の符号</span><span class="sxs-lookup"><span data-stu-id="667aa-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="667aa-192">正</span><span class="sxs-lookup"><span data-stu-id="667aa-192">Positive</span></span>                       | <span data-ttu-id="667aa-193">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-193">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-194">正</span><span class="sxs-lookup"><span data-stu-id="667aa-194">Positive</span></span>              |
| <span data-ttu-id="667aa-195">負</span><span class="sxs-lookup"><span data-stu-id="667aa-195">Negative</span></span>                       | <span data-ttu-id="667aa-196">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-196">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-197">負</span><span class="sxs-lookup"><span data-stu-id="667aa-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="667aa-198">伝票の消費税金額および勘定を決定する</span><span class="sxs-lookup"><span data-stu-id="667aa-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="667aa-199">消費税を転記すると、元帳転記グループ プロファイルから主勘定が取得されます。</span><span class="sxs-lookup"><span data-stu-id="667aa-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="667aa-200">消費税が売掛金である場合、システムではプロファイルで指定されている消費税収入の勘定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="667aa-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="667aa-201">買掛金である消費税の場合、システムではプロファイルで指定されている消費税支払の勘定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="667aa-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="667aa-202">次の表では、一般的なルールを示します。</span><span class="sxs-lookup"><span data-stu-id="667aa-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="667aa-203">消費税提示方法</span><span class="sxs-lookup"><span data-stu-id="667aa-203">Sales tax direction</span></span>  | <span data-ttu-id="667aa-204">消費税金額の符号</span><span class="sxs-lookup"><span data-stu-id="667aa-204">Sales tax amount sign</span></span> | <span data-ttu-id="667aa-205">売上税勘定</span><span class="sxs-lookup"><span data-stu-id="667aa-205">Sales tax account</span></span>      | <span data-ttu-id="667aa-206">伝票の金額</span><span class="sxs-lookup"><span data-stu-id="667aa-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="667aa-207">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-207">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-208">正</span><span class="sxs-lookup"><span data-stu-id="667aa-208">Positive</span></span>              | <span data-ttu-id="667aa-209">税収入の勘定</span><span class="sxs-lookup"><span data-stu-id="667aa-209">Tax Receivable Account</span></span> | <span data-ttu-id="667aa-210">正 (借方)</span><span class="sxs-lookup"><span data-stu-id="667aa-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="667aa-211">消費税収入</span><span class="sxs-lookup"><span data-stu-id="667aa-211">Sales Tax Receivable</span></span> | <span data-ttu-id="667aa-212">負</span><span class="sxs-lookup"><span data-stu-id="667aa-212">Negative</span></span>              | <span data-ttu-id="667aa-213">税収入の勘定</span><span class="sxs-lookup"><span data-stu-id="667aa-213">Tax Receivable Account</span></span> | <span data-ttu-id="667aa-214">負 (貸方)</span><span class="sxs-lookup"><span data-stu-id="667aa-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="667aa-215">消費税支払</span><span class="sxs-lookup"><span data-stu-id="667aa-215">Sales Tax Payable</span></span>    | <span data-ttu-id="667aa-216">正</span><span class="sxs-lookup"><span data-stu-id="667aa-216">Positive</span></span>              | <span data-ttu-id="667aa-217">税支払の勘定</span><span class="sxs-lookup"><span data-stu-id="667aa-217">Tax Payable Account</span></span>    | <span data-ttu-id="667aa-218">負 (貸方)</span><span class="sxs-lookup"><span data-stu-id="667aa-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="667aa-219">消費税支払</span><span class="sxs-lookup"><span data-stu-id="667aa-219">Sales Tax Payable</span></span>    | <span data-ttu-id="667aa-220">負</span><span class="sxs-lookup"><span data-stu-id="667aa-220">Negative</span></span>              | <span data-ttu-id="667aa-221">税支払の勘定</span><span class="sxs-lookup"><span data-stu-id="667aa-221">Tax Payable Account</span></span>    | <span data-ttu-id="667aa-222">正 (借方)</span><span class="sxs-lookup"><span data-stu-id="667aa-222">Positive (Debit)</span></span>  |
