---
title: 顧客の前払
description: このトピックでは、顧客の前払 (顧客預金とも呼ばれる) の設定および処理方法について説明します。
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019423"
---
# <a name="customer-prepayments"></a><span data-ttu-id="b8fe5-103">顧客の前払</span><span class="sxs-lookup"><span data-stu-id="b8fe5-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8fe5-104">顧客の前払は、顧客からの支払を受け取る際に使用されますが、支払を決済できる請求書はありません。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="b8fe5-105">これらのタイプの支払は、顧客預金とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="b8fe5-106">顧客の前払を設定および処理するプロセスは、次の基本的な手順で構成されます。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="b8fe5-107">前払の顧客転記プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="b8fe5-108">**前払仕訳伝票パラメータを使用して転記** をパラメーター設定します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="b8fe5-109">顧客支払仕訳帳を作成し、各行の **前払仕訳帳伝票** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="b8fe5-110">顧客支払仕訳帳を転記します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="b8fe5-111">請求書が生成された後、**オープントランザクションの決済** ページを使用して前払を決済します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="b8fe5-112">前払の顧客転記プロファイルを作成する</span><span class="sxs-lookup"><span data-stu-id="b8fe5-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="b8fe5-113">通常、商品やサービスが提供される前、または請求書がシステムに存在する前に、顧客からの前払または預金を受け入れる場合は、現金を勘定科目表の資産ではなく負債として記録します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="b8fe5-114">ただし、一般会計でこれらの金額を記録する要件は、国または地域によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="b8fe5-115">そのため、適用される地域規定については、会計士に相談してください。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="b8fe5-116">通常、前払に使用できる転記プロファイルを作成するプロセスは、他の転記プロファイルを作成するプロセスと同じです。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="b8fe5-117">基本差額は、**集計勘定** フィールドで選択した 主要勘定 です。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="b8fe5-118">詳細については、[顧客転記プロファイル](customer-posting-profiles.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="b8fe5-119">顧客前払のパラメータの定義</span><span class="sxs-lookup"><span data-stu-id="b8fe5-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="b8fe5-120">顧客前払用にシステムを構成する際に考慮する必要がある売掛金勘定パラメータは、主に 2 つがあります。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="b8fe5-121">パラメーターをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="b8fe5-122">**売掛金勘定 \> 設定 \> 売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="b8fe5-123">オプション: **元帳と売上税** タブの **支払** クイック タブで、**前払仕訳伝票の売上税** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="b8fe5-124">**前払仕訳帳伝票を含む転記プロファイル** フィールドで、顧客の前払を転記するときに使用する顧客転記プロファイル を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="b8fe5-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="b8fe5-126">顧客前払伝票の作成</span><span class="sxs-lookup"><span data-stu-id="b8fe5-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="b8fe5-127">顧客支払仕訳帳を作成する場合、すべての前払について、**顧客支払仕訳帳** ページで **前払仕訳伝票** オプションを **はい** に設定 する必要 があります。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="b8fe5-128">顧客前払を作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="b8fe5-129">**売掛金勘定 \> 支払 \> 支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="b8fe5-130">**新規** を選択して仕訳を作成します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="b8fe5-131">**名前** フィールドで、使用する仕訳名を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b8fe5-132">前の手順で **前払仕訳帳伝票の売上税** オプションを **はい** に設定した場合は、**金額に売上税** パラメータが含まれる仕訳帳名を選択する 必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="b8fe5-133">オプション: **説明** フィールドに、詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="b8fe5-134">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-134">Select **Lines**.</span></span>
6. <span data-ttu-id="b8fe5-135">空白行が存在しない場合は、**新規** を選択して行を作成します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="b8fe5-136">**日付** フィールドに、前払を転記する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="b8fe5-137">**アカウント** フィールドで、前払の顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="b8fe5-138">オプション: **説明** フィールドに、トランザクションの詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="b8fe5-139">**クレジット** フィールドに前払の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="b8fe5-140">**相手勘定** フィールドで、支払をオフセットする相手を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="b8fe5-141">たとえば、支払を転記する銀行口座または主要口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="b8fe5-142">**支払方法** フィールドに、顧客の支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="b8fe5-143">**支払い** タブで、**前払仕訳伝票** オプションを　**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="b8fe5-144">追加の前払を転記する必要がある場合は、手順7 ~ 13 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="b8fe5-145">**投稿** を選択して、仕訳帳明細行を確定します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="b8fe5-146">請求書による前払の決済</span><span class="sxs-lookup"><span data-stu-id="b8fe5-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="b8fe5-147">**顧客支払** ワークスペースを使用すると、完全に決済されていない支払を簡単に見つけて決済できます。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="b8fe5-148">**ホーム** ダッシュボード で 、**顧客支払** のサイズを選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="b8fe5-149">**顧客トランザクション** セクションの **支払の決済** タブで、決済する支払を検索および選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="b8fe5-150">**トランザクションの決済** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="b8fe5-151">請求書および決済される支払の **マーク** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="b8fe5-152">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-152">Select **Post**.</span></span>

<span data-ttu-id="b8fe5-153">オープン トランザクションの決済方法の詳細については、[決済の概要](/cash-bank-management/settlement-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8fe5-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
