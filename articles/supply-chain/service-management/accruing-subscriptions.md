---
title: 定期売買の発生
description: サービスの定期売買では、手数料トランザクションを請求した日付に続く期間に、収益を手動で見越計上します。
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a2b581c8ae52f4c379e8e511dc898a8d106d149
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908063"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="f3bb7-103">定期売買の発生</span><span class="sxs-lookup"><span data-stu-id="f3bb7-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f3bb7-104">サービスの定期売買では、手数料トランザクションを請求した日付に続く期間に、収益を手動で見越計上します。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="f3bb7-105">発生期間は、定期売買手数料に対して設定した請求期間に対して作成されるもので、定期売買の期間コードに基づいています。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="f3bb7-106">未収収益は、見越計上およびリバースが可能です。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="f3bb7-107">貸方金額の見越計上</span><span class="sxs-lookup"><span data-stu-id="f3bb7-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="f3bb7-108">請求した定期売買金額を貸方転記する場合は、見越計上金額を 2 つの方法で取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="f3bb7-109">トランザクションの訂正票提案を作成する前に、各未収収益トランザクションを個別に取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="f3bb7-110">これが手動の方法です。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-110">This is the manual method.</span></span> <span data-ttu-id="f3bb7-111">(手動)</span><span class="sxs-lookup"><span data-stu-id="f3bb7-111">(manual)</span></span>

  - <span data-ttu-id="f3bb7-112">訂正票が転記された日または見越計上の元の転記日に未収金額を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="f3bb7-113">詳細については、[定期売買パラメータ (フォーム)](/dynamicsax-2012//subscription-parameters-form) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-113">For more information, see [Subscription parameters (form)](/dynamicsax-2012//subscription-parameters-form).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="f3bb7-114">要件の設定</span><span class="sxs-lookup"><span data-stu-id="f3bb7-114">Setup requirements</span></span>

<span data-ttu-id="f3bb7-115">収益を見越計上するには、次のようにデータ要件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="f3bb7-116">勘定の設定</span><span class="sxs-lookup"><span data-stu-id="f3bb7-116">Account setup</span></span>

<span data-ttu-id="f3bb7-117">**プロジェクト** モジュールで **仕掛品 - 定期売買** および **未収収益 - 定期売買** 勘定を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="f3bb7-118">未収収益を転記すると、**仕掛品 - 定期売買** 勘定が見越計上金額で借方転記され、**未収収益 - 定期売買** 勘定が見越計上金額で貸方転記されます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="f3bb7-119">定期売買収益の見越計上に使用する勘定の設定</span><span class="sxs-lookup"><span data-stu-id="f3bb7-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="f3bb7-120">**プロジェクト管理および会計** \> **設定** \> **転記** \> **元帳転記の設定** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="f3bb7-121">**収益勘定** タブをクリックし、アカウントを設定するため **仕掛品 - 定期売買** または **未収収益 - 定期売買** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="f3bb7-122">定期売買グループの設定</span><span class="sxs-lookup"><span data-stu-id="f3bb7-122">Subscription group setup</span></span>

<span data-ttu-id="f3bb7-123">定期売買の見越計上を可能にするには、**未収収益** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="f3bb7-124">これは、定期売買に関連付けられたグループの **定期売買グループ** フォームにあります。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="f3bb7-125">**サービス管理** \> **設定** \> **サービスの定期売買** \> **定期売買グループ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="f3bb7-126">定期売買グループに対する収益の見越計上の有効化</span><span class="sxs-lookup"><span data-stu-id="f3bb7-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="f3bb7-127">**サービス管理** \> **設定** \> **サービスの定期売買** \> **定期売買グループ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="f3bb7-128">期間</span><span class="sxs-lookup"><span data-stu-id="f3bb7-128">Periods</span></span>

<span data-ttu-id="f3bb7-129">請求期間コードを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="f3bb7-130">請求と同じ期間内に収益を見越計上しない場合は、発生期間も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="f3bb7-131">次の表に、各請求期間に対して設定できる発生期間の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3bb7-132">請求期間</span><span class="sxs-lookup"><span data-stu-id="f3bb7-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="f3bb7-133">発生期間</span><span class="sxs-lookup"><span data-stu-id="f3bb7-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3bb7-134"><strong>年</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f3bb7-135"><strong>年</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="f3bb7-136"><strong>四半期</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="f3bb7-137"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="f3bb7-138"><strong>日</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3bb7-139"><strong>四半期</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f3bb7-140"><strong>四半期</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="f3bb7-141"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="f3bb7-142"><strong>日</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3bb7-143"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f3bb7-144"><strong>月</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="f3bb7-145"><strong>日</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3bb7-146"><strong>週</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f3bb7-147"><strong>日</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3bb7-148"><strong>日</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="f3bb7-149"><strong>日</strong></span><span class="sxs-lookup"><span data-stu-id="f3bb7-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f3bb7-150">請求期間の設定は、定期売買グループ全体の設定の必須部分です。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="f3bb7-151">定期売買グループに発生期間も設定するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="f3bb7-152">定期売買グループの発生期間を設定すると、この期間が **期間コード** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="f3bb7-153">このフィールドは、定期売買の収益を見越計上する際に **未収の定期売買収益** フォームにあります。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="f3bb7-154">ただし、発生期間は定期売買グループに関する必須の情報ではありません。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f3bb7-155">次のパスを使用して<STRONG>未収の定期売買収益</STRONG>フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="f3bb7-156"><STRONG>サービス管理</STRONG>&gt;<STRONG>定期処理</STRONG>&gt;<STRONG>サービスの定期売買</STRONG>&gt;<STRONG>未収の定期売買収益</STRONG>の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="f3bb7-157">トランザクション</span><span class="sxs-lookup"><span data-stu-id="f3bb7-157">Transactions</span></span>

<span data-ttu-id="f3bb7-158">未収収益を転記するときに作成される元帳トランザクションの数を制御できます。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="f3bb7-159">定期売買で、元帳トランザクションを合計または行ごとのどちらとして作成するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="f3bb7-160">未収トランザクションに表示する転記詳細のレベルの指定</span><span class="sxs-lookup"><span data-stu-id="f3bb7-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="f3bb7-161">**プロジェクト管理と会計** \> **設定** \> **プロジェクト管理および会計パラメーター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="f3bb7-162">**請求書** フィールドの **財務** タブで、**合計** または **明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3bb7-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="f3bb7-163">参照</span><span class="sxs-lookup"><span data-stu-id="f3bb7-163">See also</span></span>

[<span data-ttu-id="f3bb7-164">未収の定期売買収益</span><span class="sxs-lookup"><span data-stu-id="f3bb7-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]