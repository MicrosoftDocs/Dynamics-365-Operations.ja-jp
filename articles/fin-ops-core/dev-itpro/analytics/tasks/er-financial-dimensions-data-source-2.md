---
title: ER 財務分析コードをデータ ソースとして使用する (第 2 部 - モデル マッピング)
description: このトピックでは、財務分析コードを ER レポートのデータ ソースとして使用するために、電子申告 (ER) モデルを構成する方法について説明します。 (第 2 部)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59f65962ef8f6ae79190b6595a313831eca53830
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570171"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="d5754-104">ER 財務分析コードをデータ ソースとして使用する (第 2 部 - モデル マッピング)</span><span class="sxs-lookup"><span data-stu-id="d5754-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5754-105">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="d5754-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d5754-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="d5754-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d5754-107">これらの手順を実施するには、まず 「ER 財務分析コードをデータソースとして使用する （パート1：デザインデータ モデル）」に記載の手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5754-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="d5754-108">必要なデータ ソースをモデルマッピングに加える</span><span class="sxs-lookup"><span data-stu-id="d5754-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="d5754-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5754-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d5754-110">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d5754-111">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-111">Click Designer.</span></span>
4. <span data-ttu-id="d5754-112">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="d5754-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-113">Click New.</span></span>
6. <span data-ttu-id="d5754-114">[定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="d5754-115">[名称] フィールドで、「分析コードデータ・マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="d5754-116">[説明] フィールドで、「分析コードデータ・マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="d5754-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-117">Click Save.</span></span>
10. <span data-ttu-id="d5754-118">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-118">Click Designer.</span></span>
11. <span data-ttu-id="d5754-119">ツリーで、'Dynamics 365 for Operations\Table を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="d5754-120">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-120">Click Add root.</span></span>
13. <span data-ttu-id="d5754-121">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="d5754-122">[テーブル] フィールドに「CompanyInfo」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="d5754-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-123">Click OK.</span></span>
16. <span data-ttu-id="d5754-124">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="d5754-125">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-125">Click Add root.</span></span>
    * <span data-ttu-id="d5754-126">このデータ ソースでは、データソースとしてそのモデルを使用するレポートについて財務分析コードをどのように定義するのか示します。</span><span class="sxs-lookup"><span data-stu-id="d5754-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="d5754-127">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="d5754-128">「分析コードのフィールドを要求する」で [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="d5754-129">ユーザー ダイアログ フォームの実行時に分析コードを選択できるよう、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="d5754-130">「いいえ」を選択しますと、現インスタンスのすべての財務分析コードが既定値で使用されることになります。</span><span class="sxs-lookup"><span data-stu-id="d5754-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="d5754-131">「財務分析コードの選択」のフィールドで、「法人」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="d5754-132">ルックアップ フィールドの現インスタンスについて「分析コードを希望」を選択するには、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="d5754-133">ルックアップ フィールドの会社について「分析コード」を選択するには、「法人」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="d5754-134">分析コードを選択して、ユーザーが単一の分析コードセットを使用して分析コードを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d5754-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="d5754-135">「主勘定のフィールドを要求する」で、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="d5754-136">「主勘定を要求する」 を 「はい」 に設定することで、分析コードリストの一部として主勘定を選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d5754-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="d5754-137">「いいえ」 に設定すると、主勘定は分析コードのリストに含まれなくなり、 「主勘定を必須にする」 オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="d5754-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="d5754-138">「主勘定を必須にする」 オプションが 「はい」 に設定されると、ユーザーの選択にかかわらず主勘定が分析コードのリストに含まれます。</span><span class="sxs-lookup"><span data-stu-id="d5754-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="d5754-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-139">Click OK.</span></span>
<span data-ttu-id="d5754-140">![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="d5754-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="d5754-141">ツリーで、'Dynamics 365 for Operations\Table records'を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="d5754-142">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-142">Click Add root.</span></span>
25. <span data-ttu-id="d5754-143">[名称] フィールドで、「LedgerJournal」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="d5754-144">[クエリの要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="d5754-145">[表] フィールドで、「LedgerJournalTable」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="d5754-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-146">Click OK.</span></span>
<span data-ttu-id="d5754-147">![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="d5754-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="d5754-148">データ モデル・エレメントを追加したデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="d5754-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="d5754-149">ツリーで、「Journal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="d5754-150">ツリーで、「Journal\Transaction」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="d5754-151">ツリーで、「Journal\Transaction\Dimensions data」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="d5754-152">ツリーで、Dimensions setting」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="d5754-153">ツリーで、「LedgerJournal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="d5754-154">ツリーで、「LedgerJournal\<Relations」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="d5754-155">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="d5754-156">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Voucher」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="d5754-157">ツリーで、「Journal\Transaction\Voucher」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="d5754-158">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-158">Click Bind.</span></span>
11. <span data-ttu-id="d5754-159">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="d5754-160">たとえば、LedgerDimensionに設定されている財務分析コードについては、相当するデータソースの品目が使用できます（LedgerDimension.分析コード）。</span><span class="sxs-lookup"><span data-stu-id="d5754-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="d5754-161">このデータ ソースの品目は、レコードのリストとして設定された分析コードの財務分析コードを示します。</span><span class="sxs-lookup"><span data-stu-id="d5754-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="d5754-162">つりーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="d5754-163">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="d5754-164">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="d5754-165">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="d5754-166">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="d5754-167">ツリーで、「Journal\Transaction\Dimensions data\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="d5754-168">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-168">Click Bind.</span></span>
19. <span data-ttu-id="d5754-169">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="d5754-170">ツリーで、「Journal\Transaction\Dimensions data\Description」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="d5754-171">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-171">Click Bind.</span></span>
22. <span data-ttu-id="d5754-172">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="d5754-173">ツリーで、「Journal\Transaction\Dimensions data\Code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="d5754-174">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-174">Click Bind.</span></span>
25. <span data-ttu-id="d5754-175">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="d5754-176">ツリーで、「Journal\Transaction\Dimensions data」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="d5754-177">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-177">Click Bind.</span></span>
<span data-ttu-id="d5754-178">![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="d5754-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="d5754-179">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="d5754-180">ツリーで、「Journal\Transaction\Debit」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="d5754-181">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-181">Click Bind.</span></span>
31. <span data-ttu-id="d5754-182">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="d5754-183">ツリーで、「Journal\Transaction\Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="d5754-184">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-184">Click Bind.</span></span>
34. <span data-ttu-id="d5754-185">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="d5754-186">ツリーで、「Journal\Transaction\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="d5754-187">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-187">Click Bind.</span></span>
37. <span data-ttu-id="d5754-188">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="d5754-189">ツリーで、「Journal\Transaction\Credit」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="d5754-190">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-190">Click Bind.</span></span>
40. <span data-ttu-id="d5754-191">ツリーで、「LedgerJournal\<Relations\LedgerJournalTrans」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="d5754-192">ツリーで、「Journal\Transaction」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="d5754-193">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-193">Click Bind.</span></span>
43. <span data-ttu-id="d5754-194">ツリーで、[LedgerJournal\Journal batch number(JournalNum)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="d5754-195">ツリーで、「Journal\Batch」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="d5754-196">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-196">Click Bind.</span></span>
46. <span data-ttu-id="d5754-197">ツリーで、「LedgerJournal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="d5754-198">ツリーで、「Journal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="d5754-199">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-199">Click Bind.</span></span>
49. <span data-ttu-id="d5754-200">ツリーで、「Dimensions」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="d5754-201">ツリーで、「Dimensions\Main account and dimensions」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="d5754-202">ツリーで、「Dimensions\Main account and dimensions\Definition」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d5754-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="d5754-203">ツリーで、「Dimensions\Main account and dimensions\Definition\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="d5754-204">ツリーで、「Dimensions setting\Code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="d5754-205">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-205">Click Bind.</span></span>
55. <span data-ttu-id="d5754-206">ツリーで、「Dimensions\Main account and dimensions\Definition\Report column name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="d5754-207">ツリーで、「Dimensions setting\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="d5754-208">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-208">Click Bind.</span></span>
58. <span data-ttu-id="d5754-209">ツリーで、「Dimensions\Main account and dimensions」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="d5754-210">ツリーで、「Dimensions setting」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="d5754-211">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-211">Click Bind.</span></span>
61. <span data-ttu-id="d5754-212">ツリーで、「Company」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5754-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="d5754-213">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-213">Click Edit.</span></span>
63. <span data-ttu-id="d5754-214">expressionAsStringTextのフィールドで、Company.'find()'.'name()を入力します。</span><span class="sxs-lookup"><span data-stu-id="d5754-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="d5754-215">会社.'検索()'.'名称()'</span><span class="sxs-lookup"><span data-stu-id="d5754-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="d5754-216">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-216">Click Save.</span></span>
<span data-ttu-id="d5754-217">![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="d5754-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="d5754-218">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5754-218">Close the page.</span></span>
66. <span data-ttu-id="d5754-219">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-219">Click Save.</span></span>
67. <span data-ttu-id="d5754-220">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5754-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="d5754-221">このドラフト モデルのバージョンを実行します。</span><span class="sxs-lookup"><span data-stu-id="d5754-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="d5754-222">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5754-222">Close the page.</span></span>
2. <span data-ttu-id="d5754-223">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5754-223">Close the page.</span></span>
3. <span data-ttu-id="d5754-224">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-224">Click Change status.</span></span>
4. <span data-ttu-id="d5754-225">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-225">Click Complete.</span></span>
5. <span data-ttu-id="d5754-226">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5754-226">Click OK.</span></span>
<span data-ttu-id="d5754-227">![ER モデル マッピング デザイナーのページ](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="d5754-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]