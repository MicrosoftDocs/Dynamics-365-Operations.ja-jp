---
title: 日本の支払手数料の設定
description: このタスクでは、日本の支払手数料の設定について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankGroup,  VendPaymFeeGroup_JP, VendTable, PaymFeeBankRule_JP, SysFieldLookUp, VendPaymFee, VendPaymModeFee, TaxGroupLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ed96d0f8bc57154afc31a9579035ee9a595c64d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371132"
---
# <a name="setup-payment-fee-for-japan"></a><span data-ttu-id="7f697-103">日本の支払手数料の設定</span><span class="sxs-lookup"><span data-stu-id="7f697-103">Setup payment fee for Japan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f697-104">このタスクでは、日本の支払手数料の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f697-104">This task walks you through setting up a payment fee for Japan.</span></span>



<span data-ttu-id="7f697-105">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="7f697-105">This task was created using the demo data company JPMF.</span></span>


## <a name="create-a-bank-group"></a><span data-ttu-id="7f697-106">銀行グループの作成</span><span class="sxs-lookup"><span data-stu-id="7f697-106">Create a bank group</span></span>
1. <span data-ttu-id="7f697-107">[現金および銀行管理] > [設定] > [銀行グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f697-107">Go to Cash and bank management > Setup > Bank groups.</span></span>
2. <span data-ttu-id="7f697-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-108">Click New.</span></span>
3. <span data-ttu-id="7f697-109">[銀行グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-109">In the Bank groups field, type a value.</span></span>
4. <span data-ttu-id="7f697-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7f697-111">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f697-111">Expand the General section.</span></span>
6. <span data-ttu-id="7f697-112">[銀行コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-112">In the Bank code field, type a value.</span></span>
7. <span data-ttu-id="7f697-113">[支店コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-113">In the Branch code field, type a value.</span></span>
8. <span data-ttu-id="7f697-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-114">Click Save.</span></span>

## <a name="create-a-vendor-payment-fee-group"></a><span data-ttu-id="7f697-115">仕入先の支払手数料グループの作成</span><span class="sxs-lookup"><span data-stu-id="7f697-115">Create a vendor payment fee group</span></span>
1. <span data-ttu-id="7f697-116">[買掛金勘定] > [支払の設定] > [ベンダー支払手数料グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f697-116">Go to Accounts payable > Payment setup > Vendor payment fee groups.</span></span>
2. <span data-ttu-id="7f697-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-117">Click New.</span></span>
3. <span data-ttu-id="7f697-118">[ベンダー支払手数料グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-118">In the Vendor payment fee group field, type a value.</span></span>
    * <span data-ttu-id="7f697-119">例: 「PaymFee」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-119">For example: enter 'PaymFee'.</span></span>  
4. <span data-ttu-id="7f697-120">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-120">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7f697-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-121">Click Save.</span></span>

## <a name="specify-a-payment-fee-group-for-a-vendor"></a><span data-ttu-id="7f697-122">仕入先の支払手数料のグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f697-122">Specify a payment fee group for a vendor</span></span>
1. <span data-ttu-id="7f697-123">[買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f697-123">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="7f697-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-124">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7f697-125">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-125">Click Edit.</span></span>
4. <span data-ttu-id="7f697-126">[支払] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f697-126">Expand the Payment section.</span></span>
5. <span data-ttu-id="7f697-127">[ベンダー支払手数料グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f697-127">In the Vendor payment fee group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7f697-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f697-129">例: 「VendPayFee」 を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-129">For example: select 'VendPayFee'.</span></span>  
7. <span data-ttu-id="7f697-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-130">Click Save.</span></span>

## <a name="create-bank-rules-for-payment-fee"></a><span data-ttu-id="7f697-131">銀行手数料組合せの作成</span><span class="sxs-lookup"><span data-stu-id="7f697-131">Create bank rules for payment fee</span></span>
1. <span data-ttu-id="7f697-132">[買掛金勘定] > [支払の設定] > [銀行手数料組合せ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f697-132">Go to Accounts payable > Payment setup > Bank rules for payment fee.</span></span>
2. <span data-ttu-id="7f697-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-133">Click New.</span></span>
3. <span data-ttu-id="7f697-134">[ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-134">In the ID field, type a value.</span></span>
4. <span data-ttu-id="7f697-135">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-135">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7f697-136">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f697-136">Expand the General section.</span></span>
6. <span data-ttu-id="7f697-137">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-137">Click Add.</span></span>
    * <span data-ttu-id="7f697-138">1 つ以上のフィルターを追加し、銀行ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f697-138">Add one or more filters to create the bank rule.</span></span>  
7. <span data-ttu-id="7f697-139">[サード パーティ銀行グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f697-139">In the Third party bank group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7f697-140">ベンダーの銀行基準を入力してフィルター処理します。。</span><span class="sxs-lookup"><span data-stu-id="7f697-140">Enter the vendor's bank criteria to filter.</span></span>  
8. <span data-ttu-id="7f697-141">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-141">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="7f697-142">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f697-143">例: 「銀行コード」 を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-143">For example: select 'Bank code'.</span></span>  
10. <span data-ttu-id="7f697-144">[法人の銀行グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f697-144">In the Company bank group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7f697-145">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-145">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f697-146">支払手数料生成ルールの基準を追加するには、手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7f697-146">Repeat the steps to add criteria for the payment fee generation rule.</span></span>  
    * <span data-ttu-id="7f697-147">1 つの銀行ルールの基準の適用には、「AND」論理を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f697-147">The criteria in one bank rule are applied using 'AND' logic.</span></span>  
12. <span data-ttu-id="7f697-148">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-148">Click Save.</span></span>

## <a name="create-a-payment-fee"></a><span data-ttu-id="7f697-149">支払手数料の作成</span><span class="sxs-lookup"><span data-stu-id="7f697-149">Create a payment fee</span></span>
1. <span data-ttu-id="7f697-150">[買掛金勘定] > [支払の設定] > [支払手数料] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f697-150">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="7f697-151">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-151">Click New.</span></span>
3. <span data-ttu-id="7f697-152">[手数料 ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-152">In the Fee ID field, type a value.</span></span>
4. <span data-ttu-id="7f697-153">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-153">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7f697-154">[手数料説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-154">In the Fee description field, type a value.</span></span>
6. <span data-ttu-id="7f697-155">[請求] フィールドで [元帳] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-155">In the Charge field, select 'Ledger'.</span></span>
7. <span data-ttu-id="7f697-156">[勘定科目] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f697-156">In the Ledger account field, specify the desired values.</span></span>
8. <span data-ttu-id="7f697-157">[支払手数料勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f697-157">In the Payment fee account field, specify the desired values.</span></span>
9. <span data-ttu-id="7f697-158">[仕訳帳タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-158">In the Journal type field, select an option.</span></span>
    * <span data-ttu-id="7f697-159">例: 「仕入れ先出金」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-159">For example: select 'Vendor disbursement'.</span></span>  
10. <span data-ttu-id="7f697-160">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-160">Click Save.</span></span>
11. <span data-ttu-id="7f697-161">[支払手数料の設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-161">Click Payment fee setup.</span></span>
12. <span data-ttu-id="7f697-162">[グループ化] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-162">In the Groupings field, select an option.</span></span>
    * <span data-ttu-id="7f697-163">例: 「グループ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-163">For example: select 'Group'.</span></span>  
13. <span data-ttu-id="7f697-164">[関連銀行] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f697-164">In the Bank relation field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="7f697-165">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-165">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f697-166">例: 「0001_009」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-166">For example: select '0001_009'.</span></span>  
15. <span data-ttu-id="7f697-167">[ベンダー グループ タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-167">In the Vendor group type field, select an option.</span></span>
    * <span data-ttu-id="7f697-168">「グループ」を選択すると、コンフィギュレーションがより簡単になります。</span><span class="sxs-lookup"><span data-stu-id="7f697-168">If you select 'Group', it can be easier to configure.</span></span>  
16. <span data-ttu-id="7f697-169">[ベンダー勘定/グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-169">In the Vendor account/group field, type a value.</span></span>
    * <span data-ttu-id="7f697-170">例: 「VendPayFee」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-170">For example: enter 'VendPayFee'.</span></span>  
17. <span data-ttu-id="7f697-171">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f697-171">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="7f697-172">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-172">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f697-173">例: 「銀行」 を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-173">For example: select 'Bank'.</span></span>  
19. <span data-ttu-id="7f697-174">[支払手数料の銀行ルール ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-174">In the Bank rule ID for payment fee field, type a value.</span></span>
    * <span data-ttu-id="7f697-175">例: 「DiffBank」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-175">For example: enter 'DiffBank'.</span></span>  
20. <span data-ttu-id="7f697-176">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-176">Click the General tab.</span></span>
21. <span data-ttu-id="7f697-177">[支払通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-177">In the Payment currency field, type a value.</span></span>
    * <span data-ttu-id="7f697-178">例: 「JPY」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-178">For example: enter 'JPY'.</span></span>  
22. <span data-ttu-id="7f697-179">[最小] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-179">In the Minimum field, enter a number.</span></span>
    * <span data-ttu-id="7f697-180">例: 「30000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-180">For example: enter '30000'.</span></span>  
23. <span data-ttu-id="7f697-181">[割合/金額] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-181">In the Percentage/Amount field, select an option.</span></span>
    * <span data-ttu-id="7f697-182">例: 「金額」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-182">For example: select 'Amount'.</span></span>  
24. <span data-ttu-id="7f697-183">[手数料金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-183">In the Fee amount field, enter a number.</span></span>
    * <span data-ttu-id="7f697-184">フィールド「630」の設定</span><span class="sxs-lookup"><span data-stu-id="7f697-184">Set field '630'</span></span>  
25. <span data-ttu-id="7f697-185">[手数料の通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-185">In the Fee currency field, type a value.</span></span>
    * <span data-ttu-id="7f697-186">例: 「JPY」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f697-186">For example: enter 'JPY'.</span></span>  
26. <span data-ttu-id="7f697-187">[売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f697-187">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="7f697-188">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-188">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f697-189">例: 「JP」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-189">For example: select 'JP'.</span></span>  
28. <span data-ttu-id="7f697-190">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f697-190">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="7f697-191">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-191">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f697-192">例: 「課税対象」 を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f697-192">For example: select 'Taxable'.</span></span>  
30. <span data-ttu-id="7f697-193">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f697-193">Click Save.</span></span>

