---
title: 売上税の支払と丸めのルール
description: この記事は、売上税所轄官庁の丸めに関するルールの設定の機能と、売上税の決済と転記のジョブ中に売上税残高を丸める方法を説明します。
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: pacheren
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97f1a30c541a302755826bb8f77205bc060ec159
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897189"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="8b1ad-103">売上税の支払と丸めのルール</span><span class="sxs-lookup"><span data-stu-id="8b1ad-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b1ad-104">この記事は、売上税所轄官庁の丸めに関するルールの設定の機能と、売上税の決済と転記のジョブ中に売上税残高を丸める方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="8b1ad-105">定期的に、売上税は税務当局に報告し、支払を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="8b1ad-106">これは、[売上税] ページの売上税の決済と転記のプロセスで実行できます。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="8b1ad-107">ある期間の売上税は売上税勘定に対して決済し、売上税残高は売上税支払決済勘定に転記します。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="8b1ad-108">売上税決済決済勘定に転記されている売上税残高は、売上税所轄官庁の要件に応じて [売上税] ページの丸めルールの設定によって丸めることができます。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="8b1ad-109">丸め誤差は、[総勘定元帳] の [自動トランザクションの勘定] フィールドで選択されている、売上税の丸め勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="8b1ad-110">下の例では、売上税所轄官庁の丸めルールがどのように機能するかを説明します。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="8b1ad-111">例</span><span class="sxs-lookup"><span data-stu-id="8b1ad-111">Examples</span></span>

<span data-ttu-id="8b1ad-112">ある期間の合計売上税として -98,765.43 の貸方残高があるとします。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="8b1ad-113">法人が支払ったよりも多くの売上税を徴収したためです。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="8b1ad-114">したがって、法人が税務当局に金銭を負っています。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="8b1ad-115">この法人では、最も近い 1.00 単位に残高を丸めることにしました。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="8b1ad-116">売上税の会計を担当するユーザーは、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="8b1ad-117">**税** > **間接税** > **売上税** > **売上税所轄官庁** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="8b1ad-118">**一般** クイック タブの **丸め形式** フィールドで、**標準** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="8b1ad-119">**丸め** フィールドで、1.00 と入力します。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="8b1ad-120">税務署に売上税を支払う時期になったら、**税** > **申告** > **売上税** > **売上税の決済と転記** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="8b1ad-121">売上税決済勘定では、未払い税金額の **98,765.43** が **98,765** に丸められていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="8b1ad-122">以下の表では、**売上税所轄官庁** ページで使用できる **丸め形式** フィールドで使用できる各丸め方法を使用して、98,765.43 の金額を丸める方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="8b1ad-123">丸め値が 0.00 に設定されている場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="8b1ad-124">通常の丸めの場合、丸めの動作は **丸め誤差 = 0.01**" と同じになります。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="8b1ad-125">**丸めフォームのオプション**、**下方**、**切り上げ**、および **独自の利点** については、この動作は **丸め誤差 = 1.00** と同じです。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="8b1ad-126">丸めフォームのオプション</span><span class="sxs-lookup"><span data-stu-id="8b1ad-126">Rounding form option</span></span>                | <span data-ttu-id="8b1ad-127">丸める値 = 0.01</span><span class="sxs-lookup"><span data-stu-id="8b1ad-127">Round-off value = 0.01</span></span> | <span data-ttu-id="8b1ad-128">丸める値 = 0.10</span><span class="sxs-lookup"><span data-stu-id="8b1ad-128">Round-off value = 0.10</span></span> | <span data-ttu-id="8b1ad-129">丸める値 = 1.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-129">Round-off value = 1.00</span></span> | <span data-ttu-id="8b1ad-130">丸める値 = 100.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-130">Round-off value = 100.00</span></span> | <span data-ttu-id="8b1ad-131">丸める値 = 0.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="8b1ad-132">標準</span><span class="sxs-lookup"><span data-stu-id="8b1ad-132">Normal</span></span>                              | <span data-ttu-id="8b1ad-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="8b1ad-133">98,765.43</span></span>              | <span data-ttu-id="8b1ad-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="8b1ad-134">98,765.40</span></span>              | <span data-ttu-id="8b1ad-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-135">98,765.00</span></span>              | <span data-ttu-id="8b1ad-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-136">98,800.00</span></span>                | <span data-ttu-id="8b1ad-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="8b1ad-137">98,765.43</span></span>                |
| <span data-ttu-id="8b1ad-138">下方修正</span><span class="sxs-lookup"><span data-stu-id="8b1ad-138">Downward</span></span>                            | <span data-ttu-id="8b1ad-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="8b1ad-139">98,765.43</span></span>              | <span data-ttu-id="8b1ad-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="8b1ad-140">98,765.40</span></span>              | <span data-ttu-id="8b1ad-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-141">98,765.00</span></span>              | <span data-ttu-id="8b1ad-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-142">98,700.00</span></span>                | <span data-ttu-id="8b1ad-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-143">98,765.00</span></span>                |
| <span data-ttu-id="8b1ad-144">切り上げ</span><span class="sxs-lookup"><span data-stu-id="8b1ad-144">Rounding-up</span></span>                         | <span data-ttu-id="8b1ad-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="8b1ad-145">98,765.43</span></span>              | <span data-ttu-id="8b1ad-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="8b1ad-146">98,765.50</span></span>              | <span data-ttu-id="8b1ad-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-147">98,766.00</span></span>              | <span data-ttu-id="8b1ad-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-148">98,800.00</span></span>                | <span data-ttu-id="8b1ad-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-149">98,766.00</span></span>                |
| <span data-ttu-id="8b1ad-150">自社の利益、与信残高に対して</span><span class="sxs-lookup"><span data-stu-id="8b1ad-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="8b1ad-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="8b1ad-151">98,765.43</span></span>              | <span data-ttu-id="8b1ad-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="8b1ad-152">98,765.40</span></span>              | <span data-ttu-id="8b1ad-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-153">98,765.00</span></span>              | <span data-ttu-id="8b1ad-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-154">98,700.00</span></span>                | <span data-ttu-id="8b1ad-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-155">98,765.00</span></span>                |
| <span data-ttu-id="8b1ad-156">自社の利益、借方残高に対して</span><span class="sxs-lookup"><span data-stu-id="8b1ad-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="8b1ad-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="8b1ad-157">98,765.43</span></span>              | <span data-ttu-id="8b1ad-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="8b1ad-158">98,765.50</span></span>              | <span data-ttu-id="8b1ad-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-159">98,766.00</span></span>              | <span data-ttu-id="8b1ad-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-160">98,800.00</span></span>                | <span data-ttu-id="8b1ad-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="8b1ad-162">通常の丸め、および丸め精度は 0.01</span><span class="sxs-lookup"><span data-stu-id="8b1ad-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="8b1ad-163">丸めています</span><span class="sxs-lookup"><span data-stu-id="8b1ad-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="8b1ad-164">計算プロセス</span><span class="sxs-lookup"><span data-stu-id="8b1ad-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8b1ad-165">丸め (1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="8b1ad-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="8b1ad-166">丸め (1.015 / 0.01, 0) = 丸め (101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="8b1ad-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="8b1ad-167">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="8b1ad-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8b1ad-168">丸め (1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="8b1ad-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="8b1ad-169">丸め (1.014 / 0.01, 0) = 丸め (101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="8b1ad-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="8b1ad-170">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="8b1ad-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8b1ad-171">丸め (1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="8b1ad-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="8b1ad-172">丸め (1.011 / 0.02, 0) = 丸め (50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="8b1ad-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="8b1ad-173">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="8b1ad-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="8b1ad-174">丸め (1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="8b1ad-175">丸め (1.009 / 0.02, 0) = 丸め (50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="8b1ad-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="8b1ad-176">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="8b1ad-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="8b1ad-177">[自社の利益] を選択した場合、丸めは常に、法人の利益になります。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="8b1ad-178">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b1ad-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="8b1ad-179">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="8b1ad-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="8b1ad-180">消費税支払の作成</span><span class="sxs-lookup"><span data-stu-id="8b1ad-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="8b1ad-181">ドキュメントの消費税トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="8b1ad-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="8b1ad-182">転記された消費税トランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="8b1ad-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- <span data-ttu-id="8b1ad-183">[round 関数](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="8b1ad-183">[round Function](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
