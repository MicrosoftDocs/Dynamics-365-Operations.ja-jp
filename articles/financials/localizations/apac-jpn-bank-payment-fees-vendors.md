---
title: 仕入先負担の銀行支払手数料 (日本)
description: このトピックでは、日本の仕入先負担の銀行支払手数料についてよく寄せられる質問に回答します。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymFeeBankRule_JP, VendPaymFeeGroup_JP, VendPaymModeFee
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10214
ms.assetid: aa8a8ef3-1e5e-4174-817b-3b98e1e51509
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 896138d821a68c0126b9340b0e057140170d59d1
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850723"
---
# <a name="bank-payment-fees-covered-by-vendors-in-japan"></a><span data-ttu-id="4483f-103">仕入先負担の銀行支払手数料 (日本)</span><span class="sxs-lookup"><span data-stu-id="4483f-103">Bank payment fees covered by vendors in Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4483f-104">日本では、銀行支払手数料は通常、仕入先 (受領当事者) によって負担されます。</span><span class="sxs-lookup"><span data-stu-id="4483f-104">In Japan, the bank payment fees are usually covered by vendors (the receiving party).</span></span> <span data-ttu-id="4483f-105">このトピックでは、仕入先負担の銀行支払手数料についてよく寄せられる質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="4483f-105">This topic answers some of the frequently asked questions about bank payment fees that are covered by vendors.</span></span>

<span data-ttu-id="4483f-106">仕入先への支払を行うとき、銀行支払手数料を自分の法人か、または仕入先が負担することができます。</span><span class="sxs-lookup"><span data-stu-id="4483f-106">When you make payments to a vendor, the bank payment fees can be covered by you or by the vendor.</span></span> <span data-ttu-id="4483f-107">仕入先が銀行支払手数料を負担するとき、会社の仕入先への各支払から銀行支払手数料を自動的に差し引くようにプロセスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4483f-107">When the vendor covers the bank payment fees, you can set up the process in such a way that bank payment fees are automatically deducted from each payment that the company makes to the vendor.</span></span> <span data-ttu-id="4483f-108">仕入先の銀行支払手数料を設定および計算するには、次の作業を実行します。</span><span class="sxs-lookup"><span data-stu-id="4483f-108">Complete the following tasks to set up and calculate the bank payment fees for a vendor:</span></span>

1.  <span data-ttu-id="4483f-109">仕入先が銀行支払手数料を負担することを指示します。</span><span class="sxs-lookup"><span data-stu-id="4483f-109">Indicate that the vendor covers the bank payment fees.</span></span>
2.  <span data-ttu-id="4483f-110">会社が仕入先へ行う支払から差し引かれる銀行支払手数料を計算するための支払ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="4483f-110">Create a payment rule to calculate the bank payment fees that are deducted from payments that the company makes to the vendor.</span></span>
3.  <span data-ttu-id="4483f-111">支払ルールを使用して支払手数料を設定します。</span><span class="sxs-lookup"><span data-stu-id="4483f-111">Set up a payment fee by using the payment rule.</span></span>
4.  <span data-ttu-id="4483f-112">銀行支払手数料を支払う仕入先について、支払を作成および転記します。</span><span class="sxs-lookup"><span data-stu-id="4483f-112">Create and post a payment for the vendor who pays the bank payment fees.</span></span>
5.  <span data-ttu-id="4483f-113">支払ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="4483f-113">Generate the payment file.</span></span>

## <a name="can-i-specify-criteria-that-i-can-use-to-calculate-bank-payment-fees"></a><span data-ttu-id="4483f-114">銀行支払手数料の計算に使用できる基準を指定できますか</span><span class="sxs-lookup"><span data-stu-id="4483f-114">Can I specify criteria that I can use to calculate bank payment fees?</span></span>
<span data-ttu-id="4483f-115">はい。</span><span class="sxs-lookup"><span data-stu-id="4483f-115">Yes.</span></span> <span data-ttu-id="4483f-116">**銀行手数料組合せ**ページで、支払手数料の計算に使用できる基準を設定する銀行ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4483f-116">On the **Bank rules for payment fee** page, you can create a bank rule to set up criteria that you can use to calculate payment fees.</span></span> <span data-ttu-id="4483f-117">銀行ルールを作成したら、それ使用して、**支払手数料**ページで支払手数料を設定できます。</span><span class="sxs-lookup"><span data-stu-id="4483f-117">After you create the bank rule, you can use it to set up a payment fee on the **Payment fee** page.</span></span> <span data-ttu-id="4483f-118">たとえば、銀行口座について次のルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4483f-118">For example, you can create the following rules for bank accounts.</span></span>

| <span data-ttu-id="4483f-119">[ルールの条件]</span><span class="sxs-lookup"><span data-stu-id="4483f-119">Condition for the rule</span></span>                               | <span data-ttu-id="4483f-120">ID</span><span class="sxs-lookup"><span data-stu-id="4483f-120">ID</span></span>                | <span data-ttu-id="4483f-121">サード パーティ銀行グループ</span><span class="sxs-lookup"><span data-stu-id="4483f-121">Third party bank group</span></span> | <span data-ttu-id="4483f-122">続柄</span><span class="sxs-lookup"><span data-stu-id="4483f-122">Relationship</span></span> | <span data-ttu-id="4483f-123">会社の銀行グループ</span><span class="sxs-lookup"><span data-stu-id="4483f-123">Company bank group</span></span> |
|------------------------------------------------------|-------------------|------------------------|--------------|--------------------|
| <span data-ttu-id="4483f-124">同じ銀行の銀行口座</span><span class="sxs-lookup"><span data-stu-id="4483f-124">Bank accounts in the same bank</span></span>                       | <span data-ttu-id="4483f-125">Bank\_Same</span><span class="sxs-lookup"><span data-stu-id="4483f-125">Bank\_Same</span></span>        | <span data-ttu-id="4483f-126">銀行コード</span><span class="sxs-lookup"><span data-stu-id="4483f-126">Bank code</span></span>              | =            | <span data-ttu-id="4483f-127">銀行コード</span><span class="sxs-lookup"><span data-stu-id="4483f-127">Bank code</span></span>          |
| <span data-ttu-id="4483f-128">同じ銀行の異なる支店の銀行口座</span><span class="sxs-lookup"><span data-stu-id="4483f-128">Bank accounts in different branches of the same bank</span></span> | <span data-ttu-id="4483f-129">Branch\_Different</span><span class="sxs-lookup"><span data-stu-id="4483f-129">Branch\_Different</span></span> | <span data-ttu-id="4483f-130">銀行コード</span><span class="sxs-lookup"><span data-stu-id="4483f-130">Bank code</span></span>              | =            | <span data-ttu-id="4483f-131">銀行コード</span><span class="sxs-lookup"><span data-stu-id="4483f-131">Bank code</span></span>          |
|                                                      |                   | <span data-ttu-id="4483f-132">支店コード</span><span class="sxs-lookup"><span data-stu-id="4483f-132">Branch code</span></span>            | &lt;&gt;     | <span data-ttu-id="4483f-133">支店コード</span><span class="sxs-lookup"><span data-stu-id="4483f-133">Branch code</span></span>        |
| <span data-ttu-id="4483f-134">異なる銀行の銀行口座</span><span class="sxs-lookup"><span data-stu-id="4483f-134">Bank accounts in different banks</span></span>                     | <span data-ttu-id="4483f-135">Bank\_Diff</span><span class="sxs-lookup"><span data-stu-id="4483f-135">Bank\_Diff</span></span>        | <span data-ttu-id="4483f-136">銀行コード</span><span class="sxs-lookup"><span data-stu-id="4483f-136">Bank code</span></span>              | &lt;&gt;     | <span data-ttu-id="4483f-137">銀行コード</span><span class="sxs-lookup"><span data-stu-id="4483f-137">Bank code</span></span>          |

## <a name="can-i-set-up-a-rule-to-compare-values"></a><span data-ttu-id="4483f-138">値を比較するルールを設定できますか。</span><span class="sxs-lookup"><span data-stu-id="4483f-138">Can I set up a rule to compare values?</span></span>
<span data-ttu-id="4483f-139">はい。</span><span class="sxs-lookup"><span data-stu-id="4483f-139">Yes.</span></span> <span data-ttu-id="4483f-140">**値** フィールドで指定した値を、**銀行手数料組合せ** ページの **サード パーティ銀行グループ** フィールドで選択したフィルター値に対して比較するルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4483f-140">You can set up a rule to compare the value that you specify in the **Value** field to the filter value that you select in the **Third party bank group** field on the **Bank rules for payment fee** page.</span></span> <span data-ttu-id="4483f-141">たとえば、銀行コード 001 の特定の銀行に適用するルールを作成するには、**サード パーティ銀行グループ**フィールドで**銀行コード**を選択し、**リレーションシップ**フィールドで **=** を選択し、**値**フィールドに **001** を入力します。</span><span class="sxs-lookup"><span data-stu-id="4483f-141">For example, to create a bank rule that applies to a bank that has a bank code of 001, select **Bank code** in the **Third party bank group** field, select **=** in the **Relationship** field, and then enter **001** in the **Value** field.</span></span>

| <span data-ttu-id="4483f-142">[ルールの条件]</span><span class="sxs-lookup"><span data-stu-id="4483f-142">Condition for the rule</span></span>                     | <span data-ttu-id="4483f-143">サード パーティ銀行グループ</span><span class="sxs-lookup"><span data-stu-id="4483f-143">Third party bank group</span></span> | <span data-ttu-id="4483f-144">続柄</span><span class="sxs-lookup"><span data-stu-id="4483f-144">Relationship</span></span> | <span data-ttu-id="4483f-145">先頭値</span><span class="sxs-lookup"><span data-stu-id="4483f-145">Value</span></span> |
|--------------------------------------------|------------------------|--------------|-------|
| <span data-ttu-id="4483f-146">値に割り当てる銀行口座</span><span class="sxs-lookup"><span data-stu-id="4483f-146">A bank account that is assigned to a value</span></span> | <span data-ttu-id="4483f-147">銀行コード</span><span class="sxs-lookup"><span data-stu-id="4483f-147">Bank code</span></span>              | =            | <span data-ttu-id="4483f-148">001</span><span class="sxs-lookup"><span data-stu-id="4483f-148">001</span></span>   |

## <a name="how-can-i-calculate-the-consumption-tax-on-the-bank-payment-fees"></a><span data-ttu-id="4483f-149">銀行支払手数料の消費税はどのように計算できますか。</span><span class="sxs-lookup"><span data-stu-id="4483f-149">How can I calculate the consumption tax on the bank payment fees?</span></span>
<span data-ttu-id="4483f-150">銀行支払手数料の消費税の計算するには、**支払手数料の設定**ページの**全般**タブで次の情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="4483f-150">To calculate the consumption tax on the bank payment fees, set up the following information on the **General** tab of the **Payment fee setup** page:</span></span>

-   <span data-ttu-id="4483f-151">支払額に **手数料金額** フィールドの税を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4483f-151">Specify whether the payment amounts in the **Fee amount** field include taxes.</span></span> <span data-ttu-id="4483f-152">手数料の金額に売上税を含めるには、**支払仕訳帳**ページの**設定**タブで **金額に売上税を含める**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="4483f-152">To include sales tax in the fee amount, on the **Payment journal** page, on the **Setup** tab, select the **Amounts include sales tax** check box.</span></span>
-   <span data-ttu-id="4483f-153">**支払方法**フィールドで支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="4483f-153">In the **Method of payment** field, select the payment method.</span></span>
-   <span data-ttu-id="4483f-154">**割合/金額**フィールドで、**パーセンテージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4483f-154">In the **Percentage/Amount** field, select **Percent**.</span></span>
-   <span data-ttu-id="4483f-155">**手数料金額**フィールドで、支払手数料率を指定します。</span><span class="sxs-lookup"><span data-stu-id="4483f-155">In the **Fee amount** field, specify the payment fee percentage.</span></span>
-   <span data-ttu-id="4483f-156">**最小**と**最大**フィールドで、支払のしきい値を設定します。</span><span class="sxs-lookup"><span data-stu-id="4483f-156">In the **Minimum** and **Maximum** fields, set the payment threshold.</span></span>

## <a name="how-can-i-differentiate-bank-accounts-from-the-same-bank"></a><span data-ttu-id="4483f-157">同じ銀行の銀行口座を区別することができますか。</span><span class="sxs-lookup"><span data-stu-id="4483f-157">How can I differentiate bank accounts from the same bank?</span></span>
<span data-ttu-id="4483f-158">同じ銀行内の 2 つの銀行口座を区別するには、銀行ルールのフィルターとして銀行グループを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4483f-158">To differentiate two different bank accounts within the same bank, you can use the bank group as a filter for the bank rule.</span></span> <span data-ttu-id="4483f-159">**銀行手数料組合せ**ページの**サード パーティ銀行グループ**と**会社の銀行グループ**フィールドで**銀行グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4483f-159">On the **Bank rules for payment fee** page, in the **Third party bank group** and **Company bank group** fields, select **Bank groups**.</span></span> <span data-ttu-id="4483f-160">次に、**リレーションシップ**フィールドで、**&lt;&gt;** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4483f-160">Then, in the **Relationship** field, select **&lt;&gt;**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4483f-161">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="4483f-161">Additional resources</span></span>
- [<span data-ttu-id="4483f-162">支払手数料の生成および転記</span><span class="sxs-lookup"><span data-stu-id="4483f-162">Generate and post payment fee</span></span>](./tasks/post-payment-fee.md)

