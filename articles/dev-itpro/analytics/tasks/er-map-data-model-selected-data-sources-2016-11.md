---
title: ER データ モデルを選択したデータ ソースにマップする
description: 次の手順では、「システム管理者」または「電子申告開発者」ロールのユーザーが、選択した Dynamics 365 for Finance and Operations Enterprise Edition データ ソースに電子申告 (ER) データ モデルをマップする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551233"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="eea69-103">ER データ モデルを選択したデータ ソースにマップする</span><span class="sxs-lookup"><span data-stu-id="eea69-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eea69-104">次の手順では、「システム管理者」または「電子申告開発者」ロールのユーザーが、選択した Dynamics 365 for Finance and Operations Enterprise Edition データ ソースに電子申告 (ER) データ モデルをマップする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="eea69-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="eea69-105">このマッピング モデルは、電子支払ドキュメントを管理するために使用するコンフィギュレーションの書式設定で、データ ソースとして後で使用されます。</span><span class="sxs-lookup"><span data-stu-id="eea69-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="eea69-106">この例では、サンプル会社 Litware、Inc. のデータ モデルをデータ ソースにマップします。</span><span class="sxs-lookup"><span data-stu-id="eea69-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="eea69-107">これらの手順を完了するには、最初に「モデル マッピングのためのデータ ソースの選択」の手順でステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eea69-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="eea69-108">ER コンフィギュレーション ツリーを開く</span><span class="sxs-lookup"><span data-stu-id="eea69-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="eea69-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eea69-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="eea69-110">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="eea69-111">作成したモデル マッピングの選択</span><span class="sxs-lookup"><span data-stu-id="eea69-111">Select created model mapping</span></span>
1. <span data-ttu-id="eea69-112">ツリーで、「支払 (単純化モデル)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="eea69-113">モデル コンフィギュレーション「支払 (単純化モデル)」が事前に作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eea69-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="eea69-114">そうでない場合は、今すぐ停止し、タスク ガイド「選択したドメインのデータ モデルに対する新しいコンフィギュレーションの作成」の完了後に戻ります。</span><span class="sxs-lookup"><span data-stu-id="eea69-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="eea69-115">[モデル デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-115">Click Model designer.</span></span>
3. <span data-ttu-id="eea69-116">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="eea69-117">「CT mapping」のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="eea69-118">CT マッピング</span><span class="sxs-lookup"><span data-stu-id="eea69-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="eea69-119">データ モデルの要素のために作成したデータ ソースのバインド</span><span class="sxs-lookup"><span data-stu-id="eea69-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="eea69-120">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-120">Click Designer.</span></span>
2. <span data-ttu-id="eea69-121">ツリーで、[処理日時 (ProcessingDateTime)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="eea69-122">ツリーで、[Processing date(ProcessingDateTime)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="eea69-123">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-123">Click Bind.</span></span>
5. <span data-ttu-id="eea69-124">ツリーで、[Payment message identification(MessageIdentification)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="eea69-125">ツリーで、[Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="eea69-126">ツリーで、[Transactions\Journal batch number(JournalNum)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="eea69-127">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-127">Click Bind.</span></span>
9. <span data-ttu-id="eea69-128">ツリーで、[Payments] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="eea69-129">ツリーで、[Transactions] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="eea69-130">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-130">Click Bind.</span></span>
12. <span data-ttu-id="eea69-131">ツリーで、[Payments= Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="eea69-132">ツリーで、[Payments= Transactions\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="eea69-133">ツリーで、[Payments= Transactions\Creditor\Account] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="eea69-134">ツリーで、[Payments= Transactions\Creditor\Account\Currency code(Currency)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="eea69-135">ツリーで、[Transactions\vendBankAccountInTransactionCompany()] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="eea69-136">ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="eea69-137">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-137">Click Bind.</span></span>
19. <span data-ttu-id="eea69-138">ツリーで、[Payments= Transactions\Creditor\Account\IBAN code(IBAN)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="eea69-139">ツリーで、[Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="eea69-140">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-140">Click Bind.</span></span>
22. <span data-ttu-id="eea69-141">ツリーで、[Payments= Transactions\Creditor\Account\Number] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="eea69-142">ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="eea69-143">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-143">Click Bind.</span></span>
25. <span data-ttu-id="eea69-144">ツリーで、[Payments= Transactions\Creditor\Agent] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="eea69-145">ツリーで、[Payments= Transactions\Creditor\Agent\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="eea69-146">ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Name] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="eea69-147">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-147">Click Bind.</span></span>
29. <span data-ttu-id="eea69-148">ツリーで、[Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="eea69-149">ツリーで、[Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="eea69-150">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-150">Click Bind.</span></span>
32. <span data-ttu-id="eea69-151">ツリーで、[Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="eea69-152">ツリーで、[Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="eea69-153">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-153">Click Bind.</span></span>
35. <span data-ttu-id="eea69-154">ツリーで、[Payments= Transactions\Creditor\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="eea69-155">ツリーで、[Transactions\findVendTable()] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="eea69-156">ツリーで、[Transactions\findVendTable()\name()] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="eea69-157">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-157">Click Bind.</span></span>
39. <span data-ttu-id="eea69-158">ツリーで、[Payments= Transactions\Currency code(Currency)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="eea69-159">ツリーで、[Transactions\>Relations] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="eea69-160">ツリーで、[Transactions\>Relations\Currency table(Currency)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="eea69-161">ツリーで、[Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="eea69-162">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-162">Click Bind.</span></span>
44. <span data-ttu-id="eea69-163">ツリーで、[Payments= Transactions\Debtor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="eea69-164">ツリーで、[Payments= Transactions\Debtor\Account] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="eea69-165">ツリーで、[Payments= Transactions\Debtor\Account\Currency code(Currency)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="eea69-166">ツリーで、[Bank Account(BankAccount)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="eea69-167">ツリーで、[Bank Account(BankAccount)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="eea69-168">ツリーで、[Bank Account(BankAccount)\Currency(CurrencyCode)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="eea69-169">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-169">Click Bind.</span></span>
51. <span data-ttu-id="eea69-170">ツリーで、[Bank Account(BankAccount)\IBAN] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="eea69-171">ツリーで、[Payments= Transactions\Debtor\Account\IBAN code(IBAN)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="eea69-172">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-172">Click Bind.</span></span>
54. <span data-ttu-id="eea69-173">ツリーで、[Payments= Transactions\Debtor\Account\Number] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="eea69-174">ツリーで、[Bank Account(BankAccount)\Bank account number(AccountNum)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="eea69-175">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-175">Click Bind.</span></span>
57. <span data-ttu-id="eea69-176">ツリーで、[Payments= Transactions\Debtor\Agent] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="eea69-177">ツリーで、[Payments= Transactions\Debtor\Agent\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="eea69-178">ツリーで、[Bank Account(BankAccount)\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="eea69-179">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-179">Click Bind.</span></span>
61. <span data-ttu-id="eea69-180">ツリーで、[Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="eea69-181">ツリーで、[Bank Account(BankAccount)\Routing number(RegistrationNum)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="eea69-182">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-182">Click Bind.</span></span>
64. <span data-ttu-id="eea69-183">ツリーで、[Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="eea69-184">ツリーで、[Bank Account(BankAccount)\SWIFT code(SWIFTNo)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="eea69-185">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-185">Click Bind.</span></span>
67. <span data-ttu-id="eea69-186">ツリーで、[Payments= Transactions\Debtor\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="eea69-187">ツリーで、[Company information(Company)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="eea69-188">ツリーで、[Company information(Company)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="eea69-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="eea69-189">ツリーで、[Company information(Company)\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="eea69-190">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-190">Click Bind.</span></span>
72. <span data-ttu-id="eea69-191">ツリーで、[Payments= Transactions\Description] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="eea69-192">ツリーで、[Transactions\Description(Txt)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="eea69-193">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-193">Click Bind.</span></span>
75. <span data-ttu-id="eea69-194">ツリーで、[Payments= Transactions\End to end identification code(End2EndID)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="eea69-195">ツリーで、[Transactions\$EndToEndID] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="eea69-196">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-196">Click Bind.</span></span>
78. <span data-ttu-id="eea69-197">ツリーで、[Payments= Transactions\Instructed amount(InstructedAmount)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="eea69-198">ツリーで、[Transactions\$Amount] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="eea69-199">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-199">Click Bind.</span></span>
81. <span data-ttu-id="eea69-200">ツリーで、[Payments= Transactions\Transaction date(TransactionDate)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="eea69-201">ツリーで、[Transactions\Date(TransDate)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="eea69-202">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="eea69-203">作成したマップの検証</span><span class="sxs-lookup"><span data-stu-id="eea69-203">Validate created mapping</span></span>
1. <span data-ttu-id="eea69-204">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-204">Click Validate.</span></span>
    * <span data-ttu-id="eea69-205">新しいマッピングを検証し、すべてのバインディングが要件を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eea69-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="eea69-206">[エラー リスト] セクションを展開または折りたたむには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="eea69-207">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-207">Click Save.</span></span>
4. <span data-ttu-id="eea69-208">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eea69-208">Close the page.</span></span>
5. <span data-ttu-id="eea69-209">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eea69-209">Close the page.</span></span>
6. <span data-ttu-id="eea69-210">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eea69-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="eea69-211">モデル コンフィギュレーションの現在のバージョンのステータスの変更</span><span class="sxs-lookup"><span data-stu-id="eea69-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="eea69-212">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-212">Click Change status.</span></span>
    * <span data-ttu-id="eea69-213">支払形式の設計に使用できるように、指定のモデルのコンフィギュレーションの状態を [ドラフト] から [完了] に変更します。</span><span class="sxs-lookup"><span data-stu-id="eea69-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="eea69-214">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-214">Click Complete.</span></span>
    * <span data-ttu-id="eea69-215">[完了] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-215">Select Complete.</span></span>  
3. <span data-ttu-id="eea69-216">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea69-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="eea69-217">例えば、「バージョン 1」。</span><span class="sxs-lookup"><span data-stu-id="eea69-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="eea69-218">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea69-218">Click OK.</span></span>
5. <span data-ttu-id="eea69-219">現在のコンフィギュレーションの完了したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="eea69-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="eea69-220">作成したコンフィギュレーションが完了したバージョン 1 として保存されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eea69-220">Note that the created configuration is saved as completed version 1.</span></span>  

