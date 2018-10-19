--- 
title: "OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="8a9f4-103">OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="8a9f4-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a9f4-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="8a9f4-105">このコンフィギュレーションは、仕入先支払を処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="8a9f4-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順は GBSI 会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="8a9f4-107">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="8a9f4-108">テンプレートを作成するときにインポートされる Excel ファイルも必要です。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="8a9f4-109">このファイルは[支払レポートのテンプレート](https://go.microsoft.com/fwlink/?linkid=862266) からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="8a9f4-110">支払データ モデルのコンフィギュレーションをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="8a9f4-111">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8a9f4-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8a9f4-113">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーを選択します。このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順の最初のステップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="8a9f4-114">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-114">Click Set active.</span></span>
4. <span data-ttu-id="8a9f4-115">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-115">Click Repositories.</span></span>
    * <span data-ttu-id="8a9f4-116">運営リソース タイプのリポジトリを、必要に応じて選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="8a9f4-117">利用可能であれば、新しいリポジトリの作成に関する次の手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="8a9f4-118">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="8a9f4-119">[設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="8a9f4-120">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-120">Click Create repository.</span></span>
8. <span data-ttu-id="8a9f4-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-121">Click OK.</span></span>
9. <span data-ttu-id="8a9f4-122">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-122">Click Open.</span></span>
10. <span data-ttu-id="8a9f4-123">ツリーで、「支払モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="8a9f4-124">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-124">Click Import.</span></span>
    * <span data-ttu-id="8a9f4-125">このデータ モデルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-125">Import this data model.</span></span> <span data-ttu-id="8a9f4-126">これは、新しい形式のコンフィギュレーションでデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="8a9f4-127">このコンフィギュレーションが既にインポートされている場合は、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="8a9f4-128">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-128">Click Yes.</span></span>
13. <span data-ttu-id="8a9f4-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-129">Close the page.</span></span>
14. <span data-ttu-id="8a9f4-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="8a9f4-131">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="8a9f4-131">Create a new format configuration</span></span>
1. <span data-ttu-id="8a9f4-132">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="8a9f4-133">ツリーで、「支払モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="8a9f4-134">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8a9f4-135">[新規] フィールドで、「PaymentModel データ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="8a9f4-136">PaymentModel のデータ モデルに基づく形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="8a9f4-137">[名前] フィールドに、「サンプル ワークシート レポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="8a9f4-138">サンプル ワークシート レポート</span><span class="sxs-lookup"><span data-stu-id="8a9f4-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="8a9f4-139">[説明] フィールドに、「仕入先の支払用サンプル ワークシート レポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="8a9f4-140">仕入先の支払用サンプル ワークシート レポート。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="8a9f4-141">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="8a9f4-142">「CustomerCreditTransferInitiation」の定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="8a9f4-143">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="8a9f4-144">OPENXML ワークシート形式で新しいドキュメントを設計します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="8a9f4-145">ツリーで、「Payment model\Sample worksheet report」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="8a9f4-146">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-146">Click Designer.</span></span>
3. <span data-ttu-id="8a9f4-147">アクション ウィンドウで、[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="8a9f4-148">[Excel からインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="8a9f4-149">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-149">Click Attachments.</span></span>
    * <span data-ttu-id="8a9f4-150">既存の Excel ドキュメントをテンプレートとして添付します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="8a9f4-151">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-151">Click New.</span></span>
7. <span data-ttu-id="8a9f4-152">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-152">Click File.</span></span>
    * <span data-ttu-id="8a9f4-153">既存の Excel ファイルをポイントします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="8a9f4-154">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-154">Close the page.</span></span>
9. <span data-ttu-id="8a9f4-155">[テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="8a9f4-156">テンプレートとして使用する Excel の添付ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="8a9f4-157">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-157">Click OK.</span></span>
    * <span data-ttu-id="8a9f4-158">ER 形式のコンポーネントが、MS Excel ドキュメント参照の構造 (名前付き範囲) に基づく設計形式で作成されていることに注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="8a9f4-159">通貨コード別の合計を計算する新しいデータ ソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="8a9f4-160">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8a9f4-161">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="8a9f4-162">ツリーで、「Functions\Group by」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="8a9f4-163">[名前] フィールドで、「PaymentByCurrency」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="8a9f4-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="8a9f4-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="8a9f4-165">[次の基準でグループを編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-165">Click Edit group by.</span></span>
6. <span data-ttu-id="8a9f4-166">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="8a9f4-167">ツリーで、[model\Payments] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="8a9f4-168">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-168">Click Add field to.</span></span>
9. <span data-ttu-id="8a9f4-169">[グループ化の対象] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-169">Click What to group.</span></span>
10. <span data-ttu-id="8a9f4-170">ツリーで、[model\Payments] を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="8a9f4-171">ツリーで、「model\Payments\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="8a9f4-172">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-172">Click Add field to.</span></span>
13. <span data-ttu-id="8a9f4-173">[グループ化されたフィールド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="8a9f4-174">ツリーで、「model\Payments\Instructed Amount(InstructedAmount)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="8a9f4-175">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-175">Click Add field to.</span></span>
16. <span data-ttu-id="8a9f4-176">[集計] フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="8a9f4-177">[方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="8a9f4-178">合計集計機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="8a9f4-179">[名前] フィールドに、「TotalInstructuredAmount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="8a9f4-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="8a9f4-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="8a9f4-181">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-181">Click Save.</span></span>
20. <span data-ttu-id="8a9f4-182">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-182">Close the page.</span></span>
21. <span data-ttu-id="8a9f4-183">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="8a9f4-184">データ ソースへの形式のコンポーネントのマッピング</span><span class="sxs-lookup"><span data-stu-id="8a9f4-184">Map format components to data sources</span></span>
1. <span data-ttu-id="8a9f4-185">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="8a9f4-186">ツリーで、[model\Payments] を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="8a9f4-187">ツリーで、「model\Payments\Initiating Party(InitiatingParty)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="8a9f4-188">ツリーで、「model\Payments\Initiating Party(InitiatingParty)\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="8a9f4-189">ツリーで、「Excel\ReportHeader」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="8a9f4-190">ツリーで、「Excel\ReportHeader\CompanyName」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="8a9f4-191">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-191">Click Bind.</span></span>
8. <span data-ttu-id="8a9f4-192">ツリーで、[model\Payments\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="8a9f4-193">ツリーで、「model\Payments\Creditor\Identification」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="8a9f4-194">ツリーで、「model\Payments\Creditor\Identification\Source ID(SourceID)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="8a9f4-195">ツリーで、「Excel\PaymLines」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="8a9f4-196">ツリーで、「Excel\PaymLines\VendAccountName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="8a9f4-197">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-197">Click Bind.</span></span>
14. <span data-ttu-id="8a9f4-198">ツリーで、[model\Payments\Creditor\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="8a9f4-199">ツリーで、「Excel\PaymLines\VendName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="8a9f4-200">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-200">Click Bind.</span></span>
17. <span data-ttu-id="8a9f4-201">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="8a9f4-202">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="8a9f4-203">ツリーで、「Excel\PaymLines\Bank」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="8a9f4-204">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-204">Click Bind.</span></span>
21. <span data-ttu-id="8a9f4-205">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="8a9f4-206">ツリーで、「Excel\PaymLines\RoutingNumber」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="8a9f4-207">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-207">Click Bind.</span></span>
24. <span data-ttu-id="8a9f4-208">ツリーで、「model\Payments\Creditor Account(CreditorAccount)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="8a9f4-209">ツリーで、「model\Payments\Creditor Account(CreditorAccount)\Identification」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="8a9f4-210">ツリーで、「model\Payments\Creditor Account(CreditorAccount)\Identification\Number」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="8a9f4-211">ツリーで、「Excel\PaymLines\AccountNumber」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="8a9f4-212">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-212">Click Bind.</span></span>
29. <span data-ttu-id="8a9f4-213">ツリーで、「model\Payments\Instructed Amount(InstructedAmount)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="8a9f4-214">ツリーで、「Excel\PaymLines\Debit」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="8a9f4-215">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-215">Click Bind.</span></span>
32. <span data-ttu-id="8a9f4-216">ツリーで、[model\Payments\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="8a9f4-217">ツリーで、「model\Payments\Creditor Account(CreditorAccount)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="8a9f4-218">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="8a9f4-219">ツリーで、「model\Payments\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="8a9f4-220">ツリーで、「Excel\PaymLines\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="8a9f4-221">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-221">Click Bind.</span></span>
38. <span data-ttu-id="8a9f4-222">ツリーで、「PaymentByCurrency」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="8a9f4-223">ツリーで、「PaymentByCurrency\grouped」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="8a9f4-224">ツリーで、「PaymentByCurrency\grouped\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="8a9f4-225">ツリーで、「Excel\SummaryLines」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="8a9f4-226">ツリーで、「Excel\SummaryLines\SummaryCurrency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="8a9f4-227">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-227">Click Bind.</span></span>
44. <span data-ttu-id="8a9f4-228">ツリーで、「PaymentByCurrency\aggregated」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="8a9f4-229">ツリーで、「PaymentByCurrency\aggregated\TotalInstructuredAmount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="8a9f4-230">ツリーで、「Excel\SummaryLines\SummaryAmount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="8a9f4-231">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-231">Click Bind.</span></span>
48. <span data-ttu-id="8a9f4-232">ツリーで、「PaymentByCurrency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="8a9f4-233">ツリーで、[Excel\SummaryLines] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="8a9f4-234">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-234">Click Bind.</span></span>
51. <span data-ttu-id="8a9f4-235">ツリーで、[model\Payments] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="8a9f4-236">ツリーで、「Excel\PaymLines」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="8a9f4-237">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-237">Click Bind.</span></span>
54. <span data-ttu-id="8a9f4-238">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-238">Click Save.</span></span>
55. <span data-ttu-id="8a9f4-239">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="8a9f4-240">支払処理用に作成されたコンフィギュレーションを使用する</span><span class="sxs-lookup"><span data-stu-id="8a9f4-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="8a9f4-241">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-241">Click Change status.</span></span>
2. <span data-ttu-id="8a9f4-242">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-242">Click Complete.</span></span>
3. <span data-ttu-id="8a9f4-243">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-243">Click OK.</span></span>
4. <span data-ttu-id="8a9f4-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-244">Close the page.</span></span>
5. <span data-ttu-id="8a9f4-245">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-245">Close the page.</span></span>
6. <span data-ttu-id="8a9f4-246">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="8a9f4-247">クイック フィルターを使用して、[支払い方法] フィールドに値「Electronic」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="8a9f4-248">電子</span><span class="sxs-lookup"><span data-stu-id="8a9f4-248">Electronic</span></span>  
8. <span data-ttu-id="8a9f4-249">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-249">Click Edit.</span></span>
9. <span data-ttu-id="8a9f4-250">[ファイル形式] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="8a9f4-251">[一般的な電子申告] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="8a9f4-252">[エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="8a9f4-253">「サンプル ワークシート レポート」のコンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="8a9f4-254">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-254">Click Save.</span></span>
13. <span data-ttu-id="8a9f4-255">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="8a9f4-256">支払仕訳帳の処理のテスト用に作成されたコンフィギュレーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="8a9f4-257">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8a9f4-258">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-258">Click New.</span></span>
    * <span data-ttu-id="8a9f4-259">新しい支払仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="8a9f4-260">[名前] フィールドに、「VendaPay」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="8a9f4-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="8a9f4-261">VendPay</span></span>  
4. <span data-ttu-id="8a9f4-262">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-262">Click Lines.</span></span>
5. <span data-ttu-id="8a9f4-263">[口座] フィールドで、「GB_SI_000001」値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="8a9f4-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="8a9f4-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="8a9f4-265">[借方] を「1000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="8a9f4-266">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-266">Click New.</span></span>
8. <span data-ttu-id="8a9f4-267">[口座] フィールドで、「GB_SI_000005」値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="8a9f4-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="8a9f4-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="8a9f4-269">[借方] を「2000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="8a9f4-270">[通貨] フィールドに、「EUR」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="8a9f4-271">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8a9f4-271">EUR</span></span>  
11. <span data-ttu-id="8a9f4-272">[相殺アカウント] フィールドで、「GBSI OPER」値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8a9f4-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8a9f4-273">GBSI OPER</span></span>  
12. <span data-ttu-id="8a9f4-274">[支払方法] フィールドで、「電子」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8a9f4-275">電子</span><span class="sxs-lookup"><span data-stu-id="8a9f4-275">Electronic</span></span>  
13. <span data-ttu-id="8a9f4-276">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-276">Click Save.</span></span>
14. <span data-ttu-id="8a9f4-277">[支払の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-277">Click Generate payments.</span></span>
15. <span data-ttu-id="8a9f4-278">[支払方法] フィールドで、「電子」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8a9f4-279">電子</span><span class="sxs-lookup"><span data-stu-id="8a9f4-279">Electronic</span></span>  
16. <span data-ttu-id="8a9f4-280">[ファイル名] フィールドに、「Payments」を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="8a9f4-281">たとえば、[支払] と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="8a9f4-282">[銀行口座] フィールドで、「GBSI OPER」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8a9f4-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8a9f4-283">GBSI OPER</span></span>  
18. <span data-ttu-id="8a9f4-284">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-284">Click OK.</span></span>
19. <span data-ttu-id="8a9f4-285">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-285">Click OK.</span></span>
    * <span data-ttu-id="8a9f4-286">この支払メッセージに使用される各通貨コードの支払明細行および合計の詳細を含む、作成されたワークシートを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a9f4-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


