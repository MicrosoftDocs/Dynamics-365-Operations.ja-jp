--- 
title: "モデル マッピングを定義し、電子申告 (ER) 用のデータ ソースを選択する"
description: "次の手順では、システム管理者または電子申告開発者ロールのユーザーがどのように電子申告 (ER) データ モデルのデータ ソースを選択できるか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 512e24b5d0e20f00890e2a9abfe45b660a913913
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="817ee-103">モデル マッピングを定義し、電子申告 (ER) 用のデータ ソースを選択する</span><span class="sxs-lookup"><span data-stu-id="817ee-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="817ee-104">次の手順では、システム管理者または電子申告開発者ロールのユーザーがどのように電子申告 (ER) データ モデルのデータ ソースを選択できるか説明します。</span><span class="sxs-lookup"><span data-stu-id="817ee-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="817ee-105">データ ソースは、設計時には選択したデータ モデルの個々のコンポーネントにバインドされ、実行時には業務データがそのデータ モデルに設定されます。</span><span class="sxs-lookup"><span data-stu-id="817ee-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="817ee-106">この例では、サンプル会社 Litware、Inc. に対して作成された既存のデータ モデルのデータ ソースを選択します。これらの手順を完了するには、最初に「新しいデータ モデルの作成」手順でステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="817ee-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="817ee-107">電子申告コンフィギュレーション ツリーを開きます</span><span class="sxs-lookup"><span data-stu-id="817ee-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="817ee-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="817ee-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="817ee-109">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="817ee-110">新しいモデル マッピングの挿入</span><span class="sxs-lookup"><span data-stu-id="817ee-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="817ee-111">ツリーで、「支払 (単純化モデル)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="817ee-112">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-112">Click Designer.</span></span>
3. <span data-ttu-id="817ee-113">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="817ee-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-114">Click New.</span></span>
    * <span data-ttu-id="817ee-115">これにより、データ ソースにデータ モデルをマップする新しいレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="817ee-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="817ee-116">この例では、目的の支払タイプ「口座振替」のために、データ ソースにデータ モデルをマップします。</span><span class="sxs-lookup"><span data-stu-id="817ee-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="817ee-117">特定のデータ モデルに複数のマッピングを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="817ee-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="817ee-118">たとえば、口座引落や口座振替などの異なる支払タイプのマッピングを作成できます。</span><span class="sxs-lookup"><span data-stu-id="817ee-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="817ee-119">この例では、口座振替のマッピングを作成します。</span><span class="sxs-lookup"><span data-stu-id="817ee-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="817ee-120">[名前] フィールドで、「CT マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="817ee-121">CT マッピング</span><span class="sxs-lookup"><span data-stu-id="817ee-121">CT mapping</span></span>  
6. <span data-ttu-id="817ee-122">[説明] フィールドに、「支払モデル マッピング CT」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="817ee-123">支払モデル マッピング CT</span><span class="sxs-lookup"><span data-stu-id="817ee-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="817ee-124">[定義] フィールドに、「CustomerCreditTransferInitiation」を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="817ee-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="817ee-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="817ee-126">[定義の変更] を解決します。</span><span class="sxs-lookup"><span data-stu-id="817ee-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="817ee-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="817ee-128">現在のモデル マッピングに必要なデータ ソースの定義</span><span class="sxs-lookup"><span data-stu-id="817ee-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="817ee-129">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-129">Click Designer.</span></span>
2. <span data-ttu-id="817ee-130">ツリーで、[Dynamics 365 for Operations\Table records] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="817ee-131">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-131">Click Add root.</span></span>
    * <span data-ttu-id="817ee-132">支払トランザクションにアクセスするために、このデータ ソースを入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="817ee-133">[名前] フィールドで、「Transactions」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="817ee-134">トランザクション</span><span class="sxs-lookup"><span data-stu-id="817ee-134">Transactions</span></span>  
5. <span data-ttu-id="817ee-135">[ラベル] フィールドに「Transactions」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="817ee-136">トランザクション</span><span class="sxs-lookup"><span data-stu-id="817ee-136">Transactions</span></span>  
6. <span data-ttu-id="817ee-137">[ヘルプ] フィールドに、「Ledger journal lines」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="817ee-138">仕訳元帳明細行</span><span class="sxs-lookup"><span data-stu-id="817ee-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="817ee-139">[クエリの要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="817ee-140">[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-140">Select Yes.</span></span>  
8. <span data-ttu-id="817ee-141">[テーブル] フィールドで、「LedgerJournalTrans」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="817ee-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="817ee-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="817ee-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-143">Click OK.</span></span>
    * <span data-ttu-id="817ee-144">現在のデータ モデルのデータ ソースとして、LedgerJournalTrans テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="817ee-145">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="817ee-146">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-146">Click Add.</span></span>
    * <span data-ttu-id="817ee-147">[追加] をクリックして、新しい計算済フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="817ee-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="817ee-148">[名前] フィールドに、「$EndToEndID」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="817ee-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="817ee-149">$EndToEndID</span></span>  
13. <span data-ttu-id="817ee-150">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-150">Click Edit formula.</span></span>
14. <span data-ttu-id="817ee-151">ツリーで、[String\CONCATENATE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="817ee-152">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-152">Click Add function.</span></span>
16. <span data-ttu-id="817ee-153">ツリーで、[Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="817ee-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="817ee-154">ツリーで、[Transactions\Voucher] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="817ee-155">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-155">Click Add data source.</span></span>
19. <span data-ttu-id="817ee-156">[フォーミュラ] フィールドに、「CONCATENATE(Transactions.Voucher, "-",」を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="817ee-157">フォーミュラの最後に、「, “-“,」を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="817ee-158">ツリーで、[String\TEXT] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="817ee-159">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-159">Click Add function.</span></span>
22. <span data-ttu-id="817ee-160">ツリーで、[Transactions\Record-ID(RecId)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="817ee-161">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-161">Click Add data source.</span></span>
24. <span data-ttu-id="817ee-162">[フォーミュラ] フィールドに、「CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))」を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="817ee-163">フォーミュラの最後に、「))」を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="817ee-164">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-164">Click Save.</span></span>
    * <span data-ttu-id="817ee-165">作成したフォーミュラでエラーが検出されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="817ee-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="817ee-166">フォーミュラ エディタ コントロールの下にある [エラー] タブを参照してください。</span><span class="sxs-lookup"><span data-stu-id="817ee-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="817ee-167">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="817ee-167">Close the page.</span></span>
27. <span data-ttu-id="817ee-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-168">Click OK.</span></span>
    * <span data-ttu-id="817ee-169">このデータ ソースに計算済フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="817ee-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="817ee-170">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-170">Click Add.</span></span>
    * <span data-ttu-id="817ee-171">[追加] をクリックして、新しい計算済フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="817ee-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="817ee-172">[名前] フィールドに、「$Amount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="817ee-173">$金額</span><span class="sxs-lookup"><span data-stu-id="817ee-173">$Amount</span></span>  
30. <span data-ttu-id="817ee-174">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-174">Click Edit formula.</span></span>
31. <span data-ttu-id="817ee-175">ツリーで、[Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="817ee-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="817ee-176">ツリーで、[Transactions\Debit(AmountCurDebit)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="817ee-177">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-177">Click Add data source.</span></span>
34. <span data-ttu-id="817ee-178">[フォーミュラ] フィールドに、「Transactions.AmountCurDebit - 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="817ee-179">フォーミュラの最後に、「-」を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="817ee-180">ツリーで、[Transactions\Credit(AmountCurCredit)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="817ee-181">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-181">Click Add data source.</span></span>
37. <span data-ttu-id="817ee-182">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-182">Click Save.</span></span>
38. <span data-ttu-id="817ee-183">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="817ee-183">Close the page.</span></span>
39. <span data-ttu-id="817ee-184">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-184">Click OK.</span></span>
    * <span data-ttu-id="817ee-185">これにより、現在のデータ モデルの選択したデータ ソースに [$Amount] 計算済フィールドが追加されます。</span><span class="sxs-lookup"><span data-stu-id="817ee-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="817ee-186">ツリーで、[Transactions\$Amount] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="817ee-187">ツリーで、[Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="817ee-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="817ee-188">ツリーで、[Transactions\$Amount] を展開するかまた折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="817ee-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="817ee-189">ツリーで、「Transactions」を展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="817ee-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="817ee-190">ツリーで、[Dynamics 365 for Operations\Table records] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="817ee-191">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-191">Click Add root.</span></span>
    * <span data-ttu-id="817ee-192">このデータ ソースを入力して、会社の銀行口座情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="817ee-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="817ee-193">[名前] フィールドに、「BankAccount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="817ee-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="817ee-194">BankAccount</span></span>  
47. <span data-ttu-id="817ee-195">[ラベル] フィールドに「Bank Account」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="817ee-196">銀行口座</span><span class="sxs-lookup"><span data-stu-id="817ee-196">Bank Account</span></span>  
48. <span data-ttu-id="817ee-197">[ヘルプ] フィールドに「Bank Account」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="817ee-198">銀行口座</span><span class="sxs-lookup"><span data-stu-id="817ee-198">Bank Account</span></span>  
49. <span data-ttu-id="817ee-199">[クエリの要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="817ee-200">[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-200">Select Yes.</span></span>  
50. <span data-ttu-id="817ee-201">[テーブル] フィールドに「BankAccountTable」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="817ee-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="817ee-202">BankAccountTable</span></span>  
51. <span data-ttu-id="817ee-203">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-203">Click OK.</span></span>
    * <span data-ttu-id="817ee-204">現在のデータ モデルのデータ ソースとして、BankAccountTable テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="817ee-205">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-205">Click Add root.</span></span>
    * <span data-ttu-id="817ee-206">このデータ ソースを入力して、会社の必要条件にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="817ee-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="817ee-207">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="817ee-208">法人</span><span class="sxs-lookup"><span data-stu-id="817ee-208">Company</span></span>  
54. <span data-ttu-id="817ee-209">[ラベル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="817ee-210">会社情報</span><span class="sxs-lookup"><span data-stu-id="817ee-210">Company information</span></span>  
55. <span data-ttu-id="817ee-211">[ヘルプ] フィールドに、「Company information」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="817ee-212">会社情報</span><span class="sxs-lookup"><span data-stu-id="817ee-212">Company information</span></span>  
56. <span data-ttu-id="817ee-213">[クエリの要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="817ee-214">[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-214">Select Yes.</span></span>  
57. <span data-ttu-id="817ee-215">[テーブル] フィールドに「CompanyInfo」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="817ee-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="817ee-216">CompanyInfo</span></span>  
58. <span data-ttu-id="817ee-217">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-217">Click OK.</span></span>
    * <span data-ttu-id="817ee-218">現在のデータ モデルのデータ ソースとして、CompanyInfo テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="817ee-219">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="817ee-220">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-220">Click Add root.</span></span>
    * <span data-ttu-id="817ee-221">新しいデータ ソースとして計算済フィールドを挿入します。</span><span class="sxs-lookup"><span data-stu-id="817ee-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="817ee-222">[名前] フィールドに、「ProcessingDateTime」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="817ee-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="817ee-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="817ee-224">[ラベル] フィールドに、「処理日時」と入力します。</span><span class="sxs-lookup"><span data-stu-id="817ee-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="817ee-225">処理日時</span><span class="sxs-lookup"><span data-stu-id="817ee-225">Processing date & time</span></span>  
63. <span data-ttu-id="817ee-226">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-226">Click Edit formula.</span></span>
64. <span data-ttu-id="817ee-227">ツリーで、「Date/time\SESSIONNOW」を選択します。</span><span class="sxs-lookup"><span data-stu-id="817ee-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="817ee-228">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-228">Click Add function.</span></span>
66. <span data-ttu-id="817ee-229">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-229">Click Save.</span></span>
67. <span data-ttu-id="817ee-230">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="817ee-230">Close the page.</span></span>
68. <span data-ttu-id="817ee-231">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-231">Click OK.</span></span>
    * <span data-ttu-id="817ee-232">現在のデータ モデルのデータ ソースとして、[ProcessingDateTime] 計算済フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="817ee-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="817ee-233">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="817ee-233">Click Save.</span></span>
70. <span data-ttu-id="817ee-234">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="817ee-234">Close the page.</span></span>
71. <span data-ttu-id="817ee-235">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="817ee-235">Close the page.</span></span>
72. <span data-ttu-id="817ee-236">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="817ee-236">Close the page.</span></span>

