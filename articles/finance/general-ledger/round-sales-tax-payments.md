---
title: 売上税の支払と丸めのルール
description: この記事は、売上税所轄官庁の丸めに関するルールの設定の機能と、売上税の決済と転記のジョブ中に売上税残高を丸める方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186328"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="a9503-103">売上税の支払と丸めのルール</span><span class="sxs-lookup"><span data-stu-id="a9503-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9503-104">この記事は、売上税所轄官庁の丸めに関するルールの設定の機能と、売上税の決済と転記のジョブ中に売上税残高を丸める方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a9503-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="a9503-105">定期的に、売上税は税務当局に報告し、支払を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9503-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="a9503-106">これは、[売上税] ページの売上税の決済と転記のプロセスで実行できます。</span><span class="sxs-lookup"><span data-stu-id="a9503-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="a9503-107">ある期間の売上税は売上税勘定に対して決済し、売上税残高は売上税支払決済勘定に転記します。</span><span class="sxs-lookup"><span data-stu-id="a9503-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="a9503-108">売上税決済決済勘定に転記されている売上税残高は、売上税所轄官庁の要件に応じて [売上税] ページの丸めルールの設定によって丸めることができます。</span><span class="sxs-lookup"><span data-stu-id="a9503-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="a9503-109">丸め誤差は、[総勘定元帳] の [自動トランザクションの勘定] フィールドで選択されている、売上税の丸め勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a9503-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="a9503-110">下の例では、売上税所轄官庁の丸めルールがどのように機能するかを説明します。</span><span class="sxs-lookup"><span data-stu-id="a9503-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="a9503-111">例</span><span class="sxs-lookup"><span data-stu-id="a9503-111">Examples</span></span>

<span data-ttu-id="a9503-112">ある期間の合計売上税として -98,765.43 の貸方残高があるとします。</span><span class="sxs-lookup"><span data-stu-id="a9503-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="a9503-113">法人が支払ったよりも多くの売上税を徴収したためです。</span><span class="sxs-lookup"><span data-stu-id="a9503-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="a9503-114">したがって、法人が税務当局に金銭を負っています。</span><span class="sxs-lookup"><span data-stu-id="a9503-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="a9503-115">この法人では、最も近い 1.00 単位に残高を丸めることにしました。</span><span class="sxs-lookup"><span data-stu-id="a9503-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="a9503-116">売上税の会計を担当するユーザーは、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="a9503-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="a9503-117">[税] &gt; [間接税] &gt; [売上税] &gt; [売上税所轄官庁] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9503-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="a9503-118">[全般] クイック タブで、[丸めフォーム] フィールドで [標準] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9503-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="a9503-119">[丸め] フィールドに 1.00 と入力します。</span><span class="sxs-lookup"><span data-stu-id="a9503-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="a9503-120">税務署に売上税を支払う時期になったら、[売上税の決済と転記] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9503-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="a9503-121">([税] &gt; [申告] &gt; [売上税] &gt; [売上税の決済と転記] の順にクリックします。)</span><span class="sxs-lookup"><span data-stu-id="a9503-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="a9503-122">売上税決済勘定では、未払税金の金額 98,765.43 が 98,765 に丸められます。</span><span class="sxs-lookup"><span data-stu-id="a9503-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="a9503-123">以下の表では、 [売上税所轄官庁] ページの [丸めフォーム] フィールドで使用できる各丸め方法を使用して、98,765.43 の量を丸める方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a9503-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="a9503-124">丸めフォームのオプション</span><span class="sxs-lookup"><span data-stu-id="a9503-124">Rounding form option</span></span>                | <span data-ttu-id="a9503-125">丸める値 = 0.01</span><span class="sxs-lookup"><span data-stu-id="a9503-125">Round-off value = 0.01</span></span> | <span data-ttu-id="a9503-126">丸める値 = 0.10</span><span class="sxs-lookup"><span data-stu-id="a9503-126">Round-off value = 0.10</span></span> | <span data-ttu-id="a9503-127">丸める値 = 1.00</span><span class="sxs-lookup"><span data-stu-id="a9503-127">Round-off value = 1.00</span></span> | <span data-ttu-id="a9503-128">丸める値 = 100.00</span><span class="sxs-lookup"><span data-stu-id="a9503-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="a9503-129">標準</span><span class="sxs-lookup"><span data-stu-id="a9503-129">Normal</span></span>                              | <span data-ttu-id="a9503-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a9503-130">98,765.43</span></span>              | <span data-ttu-id="a9503-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="a9503-131">98,765.40</span></span>              | <span data-ttu-id="a9503-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a9503-132">98,765.00</span></span>              | <span data-ttu-id="a9503-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="a9503-133">98,800.00</span></span>                |
| <span data-ttu-id="a9503-134">下方修正</span><span class="sxs-lookup"><span data-stu-id="a9503-134">Downward</span></span>                            | <span data-ttu-id="a9503-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a9503-135">98,765.43</span></span>              | <span data-ttu-id="a9503-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="a9503-136">98,765.40</span></span>              | <span data-ttu-id="a9503-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a9503-137">98,765.00</span></span>              | <span data-ttu-id="a9503-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="a9503-138">98,700.00</span></span>                |
| <span data-ttu-id="a9503-139">切り上げ</span><span class="sxs-lookup"><span data-stu-id="a9503-139">Rounding-up</span></span>                         | <span data-ttu-id="a9503-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a9503-140">98,765.43</span></span>              | <span data-ttu-id="a9503-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="a9503-141">98,765.50</span></span>              | <span data-ttu-id="a9503-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="a9503-142">98,766.00</span></span>              | <span data-ttu-id="a9503-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="a9503-143">98,800.00</span></span>                |
| <span data-ttu-id="a9503-144">自社の利益、与信残高に対して</span><span class="sxs-lookup"><span data-stu-id="a9503-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="a9503-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a9503-145">98,765.43</span></span>              | <span data-ttu-id="a9503-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="a9503-146">98,765.40</span></span>              | <span data-ttu-id="a9503-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="a9503-147">98,765.00</span></span>              | <span data-ttu-id="a9503-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="a9503-148">98,700.00</span></span>                |
| <span data-ttu-id="a9503-149">自社の利益、借方残高に対して</span><span class="sxs-lookup"><span data-stu-id="a9503-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="a9503-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="a9503-150">98,765.43</span></span>              | <span data-ttu-id="a9503-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="a9503-151">98,765.50</span></span>              | <span data-ttu-id="a9503-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="a9503-152">98,766.00</span></span>              | <span data-ttu-id="a9503-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="a9503-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="a9503-154">丸めが 0.00 であるため、丸めは全くありません</span><span class="sxs-lookup"><span data-stu-id="a9503-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="a9503-155">丸め (1.0151, 0.00) = 1.0151 丸め (1.0149, 0.00) = 1.0149</span><span class="sxs-lookup"><span data-stu-id="a9503-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="a9503-156">通常の丸め、および丸め精度は 0.01</span><span class="sxs-lookup"><span data-stu-id="a9503-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="a9503-157">丸め</span><span class="sxs-lookup"><span data-stu-id="a9503-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="a9503-158">計算プロセス</span><span class="sxs-lookup"><span data-stu-id="a9503-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a9503-159">丸め (1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="a9503-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="a9503-160">丸め (1.015 / 0.01, 0) = 丸め (101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="a9503-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="a9503-161">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="a9503-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a9503-162">丸め (1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="a9503-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a9503-163">丸め (1.014 / 0.01, 0) = 丸め (101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="a9503-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="a9503-164">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="a9503-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a9503-165">丸め (1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="a9503-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a9503-166">丸め (1.011 / 0.02, 0) = 丸め (50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="a9503-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="a9503-167">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="a9503-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a9503-168">丸め (1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="a9503-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a9503-169">丸め (1.009 / 0.02, 0) = 丸め (50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="a9503-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="a9503-170">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="a9503-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="a9503-171">[自社の利益] を選択した場合、丸めは常に、法人の利益になります。</span><span class="sxs-lookup"><span data-stu-id="a9503-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="a9503-172">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9503-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="a9503-173">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="a9503-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="a9503-174">売上税支払の作成</span><span class="sxs-lookup"><span data-stu-id="a9503-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="a9503-175">ドキュメントの売上トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="a9503-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="a9503-176">転記された売上税トランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="a9503-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="a9503-177">round 関数</span><span class="sxs-lookup"><span data-stu-id="a9503-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


