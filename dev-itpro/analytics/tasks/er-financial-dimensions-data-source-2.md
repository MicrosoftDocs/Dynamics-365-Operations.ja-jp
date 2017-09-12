--- 
title: "電子申告 (ER) 用のデータ ソースとして財務分析コードを使用するためのモデルをマップする"
description: "次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.openlocfilehash: 58a0ce881e5cb8d459256244a144cf51dc357299
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="e37d8-103">電子申告 (ER) 用のデータ ソースとして財務分析コードを使用するためのモデルをマップする</span><span class="sxs-lookup"><span data-stu-id="e37d8-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e37d8-104">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="e37d8-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="e37d8-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e37d8-106">これらの手順を実施するには、まず「データ ソース (パート1：デザインデータモデル）手順としてのER使用・財務分析コード」にある手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e37d8-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="e37d8-107">必要なデータ ソースをモデルマッピングに加える</span><span class="sxs-lookup"><span data-stu-id="e37d8-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="e37d8-108">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e37d8-109">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="e37d8-110">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-110">Click Designer.</span></span>
4. <span data-ttu-id="e37d8-111">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="e37d8-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-112">Click New.</span></span>
6. <span data-ttu-id="e37d8-113">[定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="e37d8-114">[名称] フィールドで、「分析コードデータ・マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="e37d8-115">[説明] フィールドで、「分析コードデータ・マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="e37d8-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-116">Click Save.</span></span>
10. <span data-ttu-id="e37d8-117">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-117">Click Designer.</span></span>
11. <span data-ttu-id="e37d8-118">ツリーで、[Dynamics 365 for Operations\Table] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="e37d8-119">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-119">Click Add root.</span></span>
13. <span data-ttu-id="e37d8-120">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="e37d8-121">[テーブル] フィールドに「CompanyInfo」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="e37d8-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-122">Click OK.</span></span>
16. <span data-ttu-id="e37d8-123">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="e37d8-124">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-124">Click Add root.</span></span>
    * <span data-ttu-id="e37d8-125">このデータ ソースでは、データソースとしてそのモデルを使用するレポートについて財務分析コードをどのように定義するのか示します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="e37d8-126">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="e37d8-127">「分析コードのフィールドを要求する」で [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="e37d8-128">ユーザー ダイアログ フォームの実行時に分析コードを選択できるよう、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="e37d8-129">「いいえ」を選択しますと、現インスタンスのすべての財務分析コードが既定値で使用されることになります。</span><span class="sxs-lookup"><span data-stu-id="e37d8-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="e37d8-130">「財務分析コードの選択」のフィールドで、「法人」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="e37d8-131">ルックアップ フィールドの現インスタンスについて「分析コードを希望」を選択するには、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="e37d8-132">ルックアップ フィールドの会社について「分析コード」を選択するには、「法人」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="e37d8-133">分析コードを選択して、ユーザーが単一の分析コードセットを使用して分析コードを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="e37d8-134">「主勘定のフィールドを要求する」で、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="e37d8-135">ユーザーが分析コードリストの一部として主勘定を選択できるように、「主勘定を要求する」に「はい」と設定します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="e37d8-136">「いいえ」に設定しますと、主勘定は分析コードのリストに含まれなくなり、オプションの「主勘定を必須にしますか」が有効になります。</span><span class="sxs-lookup"><span data-stu-id="e37d8-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="e37d8-137">「主勘定を必須にしますか」のオプションが「はい」に設定されますと、ユーザーの選択にかかわらず主勘定が分析コードのリストに含まれます。</span><span class="sxs-lookup"><span data-stu-id="e37d8-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="e37d8-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-138">Click OK.</span></span>
23. <span data-ttu-id="e37d8-139">ツリーで、[Dynamics 365 for Operations\Table records] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="e37d8-140">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-140">Click Add root.</span></span>
25. <span data-ttu-id="e37d8-141">[名称] フィールドで、「LedgerJournal」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="e37d8-142">[クエリの要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="e37d8-143">[表] フィールドで、「LedgerJournalTable」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="e37d8-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="e37d8-145">データ モデル・エレメントを追加したデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="e37d8-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="e37d8-146">ツリーで、「Journal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="e37d8-147">ツリーで、「Journal\Transaction」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="e37d8-148">ツリーで、「Journal\Transaction\Dimensions data」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="e37d8-149">ツリーで、Dimensions setting」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="e37d8-150">ツリーで、「LedgerJournal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="e37d8-151">ツリーで、「LedgerJournal\<Relations」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="e37d8-152">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="e37d8-153">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Voucher」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="e37d8-154">ツリーで、「Journal\Transaction\Voucher」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="e37d8-155">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-155">Click Bind.</span></span>
11. <span data-ttu-id="e37d8-156">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="e37d8-157">たとえば、LedgerDimensionに設定されている財務分析コードについては、相当するデータソースの品目が使用できます（LedgerDimension.分析コード）。</span><span class="sxs-lookup"><span data-stu-id="e37d8-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="e37d8-158">このデータ ソースの品目は、記録のリストとして設定された分析コードの財務分析コードを示します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="e37d8-159">つりーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="e37d8-160">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="e37d8-161">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="e37d8-162">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="e37d8-163">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="e37d8-164">ツリーで、「Journal\Transaction\Dimensions data\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="e37d8-165">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-165">Click Bind.</span></span>
19. <span data-ttu-id="e37d8-166">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="e37d8-167">ツリーで、「Journal\Transaction\Dimensions data\Description」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="e37d8-168">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-168">Click Bind.</span></span>
22. <span data-ttu-id="e37d8-169">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="e37d8-170">ツリーで、「Journal\Transaction\Dimensions data\Code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="e37d8-171">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-171">Click Bind.</span></span>
25. <span data-ttu-id="e37d8-172">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="e37d8-173">ツリーで、「Journal\Transaction\Dimensions data」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="e37d8-174">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-174">Click Bind.</span></span>
28. <span data-ttu-id="e37d8-175">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="e37d8-176">ツリーで、「Journal\Transaction\Debit」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="e37d8-177">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-177">Click Bind.</span></span>
31. <span data-ttu-id="e37d8-178">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="e37d8-179">ツリーで、「Journal\Transaction\Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="e37d8-180">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-180">Click Bind.</span></span>
34. <span data-ttu-id="e37d8-181">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="e37d8-182">ツリーで、「Journal\Transaction\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="e37d8-183">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-183">Click Bind.</span></span>
37. <span data-ttu-id="e37d8-184">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="e37d8-185">ツリーで、「Journal\Transaction\Credit」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="e37d8-186">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-186">Click Bind.</span></span>
40. <span data-ttu-id="e37d8-187">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="e37d8-188">ツリーで、「Journal\Transaction」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="e37d8-189">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-189">Click Bind.</span></span>
43. <span data-ttu-id="e37d8-190">ツリーで、[LedgerJournal\Journal batch number(JournalNum)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="e37d8-191">ツリーで、「Journal\Batch」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="e37d8-192">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-192">Click Bind.</span></span>
46. <span data-ttu-id="e37d8-193">ツリーで、「LedgerJournal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="e37d8-194">ツリーで、「Journal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="e37d8-195">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-195">Click Bind.</span></span>
49. <span data-ttu-id="e37d8-196">ツリーで、「Dimensions」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="e37d8-197">ツリーで、「Dimensions\Main account and dimensions」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="e37d8-198">ツリーで、「Dimensions\Main account and dimensions\Definition」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="e37d8-199">ツリーで、「Dimensions\Main account and dimensions\Definition\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="e37d8-200">ツリーで、「Dimensions setting\Code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="e37d8-201">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-201">Click Bind.</span></span>
55. <span data-ttu-id="e37d8-202">ツリーで、「Dimensions\Main account and dimensions\Definition\Report column name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="e37d8-203">ツリーで、「Dimensions setting\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="e37d8-204">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-204">Click Bind.</span></span>
58. <span data-ttu-id="e37d8-205">ツリーで、「Dimensions\Main account and dimensions」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="e37d8-206">ツリーで、「Dimensions setting」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="e37d8-207">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-207">Click Bind.</span></span>
61. <span data-ttu-id="e37d8-208">ツリーで、「Company」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="e37d8-209">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-209">Click Edit.</span></span>
63. <span data-ttu-id="e37d8-210">expressionAsStringTextのフィールドで、Company.'find()'.'name()を入力します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="e37d8-211">会社.'検索()'.'名称()'</span><span class="sxs-lookup"><span data-stu-id="e37d8-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="e37d8-212">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-212">Click Save.</span></span>
65. <span data-ttu-id="e37d8-213">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e37d8-213">Close the page.</span></span>
66. <span data-ttu-id="e37d8-214">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-214">Click Save.</span></span>
67. <span data-ttu-id="e37d8-215">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e37d8-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="e37d8-216">この手形モデル バージョンを実行します。</span><span class="sxs-lookup"><span data-stu-id="e37d8-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="e37d8-217">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e37d8-217">Close the page.</span></span>
2. <span data-ttu-id="e37d8-218">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e37d8-218">Close the page.</span></span>
3. <span data-ttu-id="e37d8-219">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-219">Click Change status.</span></span>
4. <span data-ttu-id="e37d8-220">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-220">Click Complete.</span></span>
5. <span data-ttu-id="e37d8-221">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37d8-221">Click OK.</span></span>


