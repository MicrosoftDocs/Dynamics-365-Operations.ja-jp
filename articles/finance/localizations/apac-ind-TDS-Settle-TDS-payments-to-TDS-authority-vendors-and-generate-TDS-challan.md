---
title: TDS 所轄官庁の仕入先への TDS 支払いの決済と TDS チャランの作成
description: このトピックでは、源泉徴収 (TDS) の支払で控除された税を TDS 所轄官庁の仕入先に決済する方法について説明します。
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023395"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="a3bac-103">TDS 所轄官庁の仕入先への TDS 支払いの決済と TDS チャランの作成</span><span class="sxs-lookup"><span data-stu-id="a3bac-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3bac-104">このトピックでは、源泉徴収 (TDS) の支払で控除された税を TDS 所轄官庁の仕入先に決済する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="a3bac-105">**買掛金勘定 \> 支払 \> 仕入先支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="a3bac-106">[![仕入先支払仕訳帳明細ページ](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="a3bac-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="a3bac-107">**仕入先支払仕訳帳** ページで **新規** を選択して仕訳帳行を作成します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="a3bac-108">**勘定** フィールドで、TDS 支払を決済する TDS 所轄官庁の仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="a3bac-109">**決済トランザクション** を選択して **決済トランザクション** ページを開き、TDS 所轄官庁の仕入先の決済済 TDS トランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="a3bac-110">ある決済期間の決済済みの TDS 取引は、以下のように表示されます:</span><span class="sxs-lookup"><span data-stu-id="a3bac-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="a3bac-111">評価カテゴリの性質が **会社** となっている TDS トランザクションは、1つのトランザクション明細として表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="a3bac-112">評価カテゴリの性質が **HUF**、**会社**、**個別**、**AOP**、**BOI**、**地方自治体**、**その他** となっている TDS トランザクションは、1つのトランザクション明細行として示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="a3bac-113">**金額** フィールドには、TDS 所轄官庁の仕入先に支払われる TDS の合計金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="a3bac-114">決済レコードに含まれる異なる TDS トランザクションを表示するには、**源泉徴収税のトランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="a3bac-115">このページでは、決済期間の決済プロセスに含まれている各 TDS トランザクションの分割を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="a3bac-116">**概要** タブで、TDS 所轄官庁の仕入先に対して決済する TDS トランザクションのチェック ボックスを **マーク** します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="a3bac-117">**概要** タブには、各 TDS トランザクションについての次の情報が表示されます:</span><span class="sxs-lookup"><span data-stu-id="a3bac-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="a3bac-118">**日付** – トランザクションの日付です。</span><span class="sxs-lookup"><span data-stu-id="a3bac-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="a3bac-119">**伝票** – 元帳の伝票番号です。</span><span class="sxs-lookup"><span data-stu-id="a3bac-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="a3bac-120">**ソース** - TDS 取引が転記されたモジュールです。</span><span class="sxs-lookup"><span data-stu-id="a3bac-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="a3bac-121">**仕入先/顧客** - TDS を控除する仕入先または顧客の勘定番号です。</span><span class="sxs-lookup"><span data-stu-id="a3bac-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="a3bac-122">**控除対象/当事者の名前** - TDS を控除する仕入先または顧客の名前です。</span><span class="sxs-lookup"><span data-stu-id="a3bac-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="a3bac-123">**評価の対象の性質** - 控除対象者が所属する被査定者の性質です。</span><span class="sxs-lookup"><span data-stu-id="a3bac-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="a3bac-124">**金額** – TDSが計算された請求書の金額です。</span><span class="sxs-lookup"><span data-stu-id="a3bac-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="a3bac-125">**税額** - 取引に対して計算された TDS の額です。</span><span class="sxs-lookup"><span data-stu-id="a3bac-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3bac-126">TDS 所轄官庁の仕入先に対して決済しない TDS トランザクションについては、チェック ボックスの **マーク** をオフにします。</span><span class="sxs-lookup"><span data-stu-id="a3bac-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="a3bac-127">**全般** タブの **PAN** 欄には、控除対象者の固定勘定番号 (PAN) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="a3bac-128">**日付** フィールドには TDS 計算の日付が表示され、**値** フィールドには TDS 計算に使用された合計の割合が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="a3bac-129">TDS トランザクションの伝票エントリを表示するには、**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="a3bac-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-130">Close the page.</span></span>
10. <span data-ttu-id="a3bac-131">**源泉徴収税コンポーネント** を選択すると、**源泉徴収税コンポーネント** ページが開き、特定の TDS 税コードについて TDS 税コンポーネントごとに計算された TDS が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="a3bac-132">**概要** タブの **税コンポーネント** フィールド には、トランザクションに使用された TDS 税コンポーネントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="a3bac-133">**金額** フィールドには、TDS 税コンポーネント用に計算された TDS の金額が基本通貨で表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="a3bac-134">**累計金額** フィールドには、すべての決済済トランザクションの TDS の税コンポーネントに対して計算された TDS の合計金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="a3bac-135">**金額** タブの **既定の通貨** セクションには、TDS の税コンポーネントに対して計算された TDS 金額が既定通貨で表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="a3bac-136">**副通貨** セクションには、副通貨での金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="a3bac-137">**源泉徴収税コンポーネント** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="a3bac-138">**オープン トランザクションの編集** ページの **金額** フィールドで、決済期間に TDS 所轄官庁の仕入先に対して決済する合計金額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="a3bac-139">異なる TDS 決済期間の TDS 取引を TDS の所轄官庁の仕入先に決済するには、その取引のチェックボックスを **マーク** します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="a3bac-140">**オープン トランザクションの編集** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3bac-141">**源泉徴収税トランザクション** ページで決済対象として選択されたトランザクションが少数の場合は、**オープントランザクション編集** ページの **訂正** フィールドで、選択したトランザクションの 合計 TDS 額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="a3bac-142">修正金額は、**仕訳伝票** ページの仕訳帳行で更新され、**オープン トランザクションの編集** ページが閉じられます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="a3bac-143">**仕訳伝票** ページで、**借方** フィールドに、TDS 所轄官庁の仕入先に支払う合計金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="a3bac-144">相手勘定の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3bac-145">TDS の取引に異なる税勘定番号 (TAN) がある場合、**仕訳伝票** ページで TAN ごとに仕訳が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="a3bac-146">**支払手数料** タブの **手数料ID** フィールドで、手数料タイプが **利息** または **その他** の手数料 ID を選択して 、TDS 所轄官庁の仕入先に対して行われた遅延支払に対して支払手数料を請求します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="a3bac-147">**税金情報** タブの **会社情報** セクション で、**名前** フィールドに会社名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="a3bac-148">**源泉徴収税** セクションの、**税勘定番号 (TAN)** フィールドには、そのトランザクション明細に関連付けられている TAN が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="a3bac-149">仕訳を検証して転記します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="a3bac-150">**トランザクション \> チャラン情報** を選択し、トランザクションの チャラン情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="a3bac-151">**伝票** フィールドには、トランザクションの伝票番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="a3bac-152">TDS の金額を帳簿記入で預ける場合は、**帳簿記入 された TDS の預け金** チェックボックスを選択してください。</span><span class="sxs-lookup"><span data-stu-id="a3bac-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="a3bac-153">**チャランの番号** フィールドに、TDS 所轄官庁の仕入先に対する支払に使用するチャラン番号を入力してください。</span><span class="sxs-lookup"><span data-stu-id="a3bac-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="a3bac-154">**日付け** フィールドにチャランの日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="a3bac-155">**銀行名** フィールドで、TDS 所轄官庁の仕入先に支払う TDS 金額の預金を行う銀行の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="a3bac-156">このフィールドには、**買掛金勘定 \> すべての仕入先 \> 設定 \> 銀行口座** の TDS 所轄官庁の仕入先に設定された全ての銀行口座がリストアップされています。</span><span class="sxs-lookup"><span data-stu-id="a3bac-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="a3bac-157">**BSR コード** フィールドに、銀行の基本統計返品 (BSR) コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="a3bac-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="a3bac-158">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="a3bac-159">例</span><span class="sxs-lookup"><span data-stu-id="a3bac-159">Example</span></span>

<span data-ttu-id="a3bac-160">期間 2009/04/01 は、定期 TDS 決済プロセスを使用して **賃借** TDS コンポーネント グループに対して決済されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="a3bac-161">TDS 決済期間の TDS 仕入先権限勘定に、TDS の合計金額 141,625.00 が転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="a3bac-162">この金額は、TDS 所轄官庁の仕入先の **オープン トランザクション編集** ページの **金額** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="a3bac-163">**源泉徴収税トランザクション** を選択して、期間に対して決済された異なる TDS トランザクションを表示する場合は、次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="a3bac-164">TDS 金額</span><span class="sxs-lookup"><span data-stu-id="a3bac-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="a3bac-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-165">16,995.00</span></span>  |
| <span data-ttu-id="a3bac-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-166">22,660.00</span></span>  |
| <span data-ttu-id="a3bac-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-167">28,325.00</span></span>  |
| <span data-ttu-id="a3bac-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-168">16,995.00</span></span>  |
| <span data-ttu-id="a3bac-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-169">28,325.00</span></span>  |
| <span data-ttu-id="a3bac-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-170">16,995.00</span></span>  |
| <span data-ttu-id="a3bac-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-171">11,330.00</span></span>  |

<span data-ttu-id="a3bac-172">特定の TDS 金額では、**源泉徴収税コンポーネント** を選択すると、特定の TDS 税コードの TDS 税要素ごとに計算された TDS が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="a3bac-173">この例では、TDS の金額 16,995.00 に対して **源泉徴収税のコンポーネント** を選択しています。</span><span class="sxs-lookup"><span data-stu-id="a3bac-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="a3bac-174">トランザクションのコンポーネントごとに計算された税額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="a3bac-175">税コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a3bac-175">Tax component</span></span> | <span data-ttu-id="a3bac-176">日数</span><span class="sxs-lookup"><span data-stu-id="a3bac-176">Amount</span></span>    | <span data-ttu-id="a3bac-177">累計金額</span><span class="sxs-lookup"><span data-stu-id="a3bac-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="a3bac-178">TDS</span><span class="sxs-lookup"><span data-stu-id="a3bac-178">TDS</span></span>           | <span data-ttu-id="a3bac-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-179">1,5000.00</span></span> | <span data-ttu-id="a3bac-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-180">125,000.00</span></span>         |
| <span data-ttu-id="a3bac-181">割増金</span><span class="sxs-lookup"><span data-stu-id="a3bac-181">Surcharge</span></span>     | <span data-ttu-id="a3bac-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-182">1,500.00</span></span>  | <span data-ttu-id="a3bac-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-183">12,500.00</span></span>          |
| <span data-ttu-id="a3bac-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="a3bac-184">PE-Cess</span></span>       | <span data-ttu-id="a3bac-185">330.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-185">330.00</span></span>    | <span data-ttu-id="a3bac-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-186">2,750.00</span></span>           |
| <span data-ttu-id="a3bac-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="a3bac-187">SHE Cess</span></span>      | <span data-ttu-id="a3bac-188">165.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-188">165.00</span></span>    | <span data-ttu-id="a3bac-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="a3bac-189">1,375.00</span></span>           |

<span data-ttu-id="a3bac-190">**源泉徴収税トランザクション** ページで決済対象の TDS 金額 16,995.00、22,660.00、2,8325.00 のみを選択した場合、**オープン トランザクションの編集** ページの **修正** フィールドには、決済対象の合計金額が **67,980.00** と表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="a3bac-191">この取引が決済用にマークされ、**オープン トランザクションの編集** ページが閉じられると、**仕訳伝票** ページの **借方** フィールドに金額 **67,980.00** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="a3bac-192">以上で、仕訳帳を転記し、TDS チャランを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="a3bac-193">TDS 所轄官庁の仕入先に支払われる前払い金の調整</span><span class="sxs-lookup"><span data-stu-id="a3bac-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="a3bac-194">TDS 所轄官庁の仕入先に支払われた前払い金を実際の支払いに調整するには、**買掛金勘定 \> 仕入先 \> すべての仕入先 \> トランザクションの編集** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a3bac-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="a3bac-195">実際の支払いが前払い金を上回った場合、その取引に対して 2 つのチャラン番号が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="a3bac-196">ただし、TDS の照会では、最初のチャラン番号のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3bac-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
