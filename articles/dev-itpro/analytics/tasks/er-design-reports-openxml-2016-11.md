--- 
title: "OpenXML 形式でレポートを生成するための ER コンフィギュレーションのデザイン"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="150f0-103">OpenXML 形式でレポートを生成するための ER コンフィギュレーションのデザイン</span><span class="sxs-lookup"><span data-stu-id="150f0-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="150f0-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="150f0-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="150f0-105">このコンフィギュレーションは、仕入先支払を処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="150f0-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="150f0-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順は GBSI 会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="150f0-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="150f0-107">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="150f0-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="150f0-108">Microsoft Excel ファイル、[支払レポートのテンプレート](https://go.microsoft.com/fwlink/?linkid=862266) をダウンロードして保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="150f0-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="150f0-109">支払データ モデルのコンフィギュレーションをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="150f0-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="150f0-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="150f0-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="150f0-111">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="150f0-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="150f0-112">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーを選択します。このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順の最初のステップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="150f0-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="150f0-113">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-113">Click Set active.</span></span>
4. <span data-ttu-id="150f0-114">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-114">Click Repositories.</span></span>
    * <span data-ttu-id="150f0-115">運営リソース タイプのリポジトリを、必要に応じて選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="150f0-116">利用可能であれば、新しいリポジトリの作成に関する次の手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="150f0-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="150f0-117">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="150f0-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="150f0-118">[設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="150f0-119">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-119">Click Create repository.</span></span>
8. <span data-ttu-id="150f0-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-120">Click OK.</span></span>
9. <span data-ttu-id="150f0-121">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-121">Click Open.</span></span>
10. <span data-ttu-id="150f0-122">ツリーで、「支払モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="150f0-123">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-123">Click Import.</span></span>
    * <span data-ttu-id="150f0-124">このデータ モデルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="150f0-124">Import this data model.</span></span> <span data-ttu-id="150f0-125">これは、新しい形式のコンフィギュレーションでデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="150f0-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="150f0-126">このコンフィギュレーションが既にインポートされている場合は、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="150f0-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="150f0-127">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-127">Click Yes.</span></span>
13. <span data-ttu-id="150f0-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-128">Close the page.</span></span>
14. <span data-ttu-id="150f0-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="150f0-130">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="150f0-130">Create a new format configuration</span></span>
1. <span data-ttu-id="150f0-131">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="150f0-132">ツリーで、「支払モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="150f0-133">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="150f0-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="150f0-134">[新規] フィールドで、「PaymentModel データ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="150f0-135">PaymentModel のデータ モデルに基づく形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="150f0-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="150f0-136">[名前] フィールドに、「サンプル ワークシート レポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="150f0-137">サンプル ワークシート レポート</span><span class="sxs-lookup"><span data-stu-id="150f0-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="150f0-138">[説明] フィールドに、「仕入先の支払用サンプル ワークシート レポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="150f0-139">仕入先の支払用サンプル ワークシート レポート。</span><span class="sxs-lookup"><span data-stu-id="150f0-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="150f0-140">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="150f0-141">「CustomerCreditTransferInitiation」の定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="150f0-142">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="150f0-143">OPENXML ワークシート形式で新しいドキュメントを設計します。</span><span class="sxs-lookup"><span data-stu-id="150f0-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="150f0-144">ツリーで、「Payment model\Sample worksheet report」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="150f0-145">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-145">Click Designer.</span></span>
3. <span data-ttu-id="150f0-146">アクション ウィンドウで、[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="150f0-147">[Excel からインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="150f0-148">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-148">Click Attachments.</span></span>
    * <span data-ttu-id="150f0-149">既存の Excel ドキュメントをテンプレートとして添付します。</span><span class="sxs-lookup"><span data-stu-id="150f0-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="150f0-150">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-150">Click New.</span></span>
7. <span data-ttu-id="150f0-151">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-151">Click File.</span></span>
    * <span data-ttu-id="150f0-152">既存の Excel ファイルをポイントします。</span><span class="sxs-lookup"><span data-stu-id="150f0-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="150f0-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-153">Close the page.</span></span>
9. <span data-ttu-id="150f0-154">[テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="150f0-155">テンプレートとして使用する Excel の添付ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="150f0-156">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-156">Click OK.</span></span>
    * <span data-ttu-id="150f0-157">ER 形式のコンポーネントが、MS Excel ドキュメント参照の構造 (名前付き範囲) に基づく設計形式で作成されていることに注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="150f0-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="150f0-158">通貨コード別の合計を計算する新しいデータ ソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="150f0-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="150f0-159">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="150f0-160">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="150f0-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="150f0-161">ツリーで、「Functions\Group by」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="150f0-162">[名前] フィールドで、「PaymentByCurrency」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="150f0-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="150f0-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="150f0-164">[次の基準でグループを編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-164">Click Edit group by.</span></span>
6. <span data-ttu-id="150f0-165">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="150f0-166">ツリーで、[model\Payments] を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="150f0-167">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-167">Click Add field to.</span></span>
9. <span data-ttu-id="150f0-168">[グループ化の対象] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-168">Click What to group.</span></span>
10. <span data-ttu-id="150f0-169">ツリーで、[model\Payments] を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="150f0-170">ツリーで、「model\Payments\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="150f0-171">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-171">Click Add field to.</span></span>
13. <span data-ttu-id="150f0-172">[グループ化されたフィールド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="150f0-173">ツリーで、「model\Payments\Instructed Amount(InstructedAmount)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="150f0-174">[フィールドの追加先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-174">Click Add field to.</span></span>
16. <span data-ttu-id="150f0-175">[集計] フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="150f0-176">[方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="150f0-177">合計集計機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="150f0-178">[名前] フィールドに、「TotalInstructuredAmount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="150f0-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="150f0-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="150f0-180">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-180">Click Save.</span></span>
20. <span data-ttu-id="150f0-181">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-181">Close the page.</span></span>
21. <span data-ttu-id="150f0-182">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="150f0-183">データ ソースへの形式のコンポーネントのマッピング</span><span class="sxs-lookup"><span data-stu-id="150f0-183">Map format components to data sources</span></span>
1. <span data-ttu-id="150f0-184">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="150f0-185">ツリーで、[model\Payments] を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="150f0-186">ツリーで、「model\Payments\Initiating Party(InitiatingParty)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="150f0-187">ツリーで、「model\Payments\Initiating Party(InitiatingParty)\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="150f0-188">ツリーで、「Excel\ReportHeader」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="150f0-189">ツリーで、「Excel\ReportHeader\CompanyName」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="150f0-190">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-190">Click Bind.</span></span>
8. <span data-ttu-id="150f0-191">ツリーで、[model\Payments\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="150f0-192">ツリーで、「model\Payments\Creditor\Identification」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="150f0-193">ツリーで、「model\Payments\Creditor\Identification\Source ID(SourceID)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="150f0-194">ツリーで、「Excel\PaymLines」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="150f0-195">ツリーで、「Excel\PaymLines\VendAccountName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="150f0-196">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-196">Click Bind.</span></span>
14. <span data-ttu-id="150f0-197">ツリーで、[model\Payments\Creditor\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="150f0-198">ツリーで、「Excel\PaymLines\VendName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="150f0-199">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-199">Click Bind.</span></span>
17. <span data-ttu-id="150f0-200">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="150f0-201">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="150f0-202">ツリーで、「Excel\PaymLines\Bank」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="150f0-203">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-203">Click Bind.</span></span>
21. <span data-ttu-id="150f0-204">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="150f0-205">ツリーで、「Excel\PaymLines\RoutingNumber」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="150f0-206">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-206">Click Bind.</span></span>
24. <span data-ttu-id="150f0-207">ツリーで、「model\Payments\Creditor Account(CreditorAccount)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="150f0-208">ツリーで、「model\Payments\Creditor Account(CreditorAccount)\Identification」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="150f0-209">ツリーで、「model\Payments\Creditor Account(CreditorAccount)\Identification\Number」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="150f0-210">ツリーで、「Excel\PaymLines\AccountNumber」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="150f0-211">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-211">Click Bind.</span></span>
29. <span data-ttu-id="150f0-212">ツリーで、「model\Payments\Instructed Amount(InstructedAmount)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="150f0-213">ツリーで、「Excel\PaymLines\Debit」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="150f0-214">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-214">Click Bind.</span></span>
32. <span data-ttu-id="150f0-215">ツリーで、[model\Payments\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="150f0-216">ツリーで、「model\Payments\Creditor Account(CreditorAccount)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="150f0-217">ツリーで、「model\Payments\Creditor Agent(CreditorAgent)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="150f0-218">ツリーで、「model\Payments\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="150f0-219">ツリーで、「Excel\PaymLines\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="150f0-220">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-220">Click Bind.</span></span>
38. <span data-ttu-id="150f0-221">ツリーで、「PaymentByCurrency」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="150f0-222">ツリーで、「PaymentByCurrency\grouped」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="150f0-223">ツリーで、「PaymentByCurrency\grouped\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="150f0-224">ツリーで、「Excel\SummaryLines」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="150f0-225">ツリーで、「Excel\SummaryLines\SummaryCurrency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="150f0-226">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-226">Click Bind.</span></span>
44. <span data-ttu-id="150f0-227">ツリーで、「PaymentByCurrency\aggregated」を展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="150f0-228">ツリーで、「PaymentByCurrency\aggregated\TotalInstructuredAmount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="150f0-229">ツリーで、「Excel\SummaryLines\SummaryAmount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="150f0-230">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-230">Click Bind.</span></span>
48. <span data-ttu-id="150f0-231">ツリーで、「PaymentByCurrency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="150f0-232">ツリーで、[Excel\SummaryLines] を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="150f0-233">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-233">Click Bind.</span></span>
51. <span data-ttu-id="150f0-234">ツリーで、[model\Payments] を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="150f0-235">ツリーで、「Excel\PaymLines」を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="150f0-236">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-236">Click Bind.</span></span>
54. <span data-ttu-id="150f0-237">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-237">Click Save.</span></span>
55. <span data-ttu-id="150f0-238">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="150f0-239">支払処理用に作成されたコンフィギュレーションを使用する</span><span class="sxs-lookup"><span data-stu-id="150f0-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="150f0-240">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-240">Click Change status.</span></span>
2. <span data-ttu-id="150f0-241">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-241">Click Complete.</span></span>
3. <span data-ttu-id="150f0-242">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-242">Click OK.</span></span>
4. <span data-ttu-id="150f0-243">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-243">Close the page.</span></span>
5. <span data-ttu-id="150f0-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-244">Close the page.</span></span>
6. <span data-ttu-id="150f0-245">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="150f0-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="150f0-246">クイック フィルターを使用して、[支払い方法] フィールドに値「Electronic」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="150f0-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="150f0-247">電子</span><span class="sxs-lookup"><span data-stu-id="150f0-247">Electronic</span></span>  
8. <span data-ttu-id="150f0-248">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-248">Click Edit.</span></span>
9. <span data-ttu-id="150f0-249">[ファイル形式] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="150f0-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="150f0-250">[一般的な電子申告] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="150f0-251">[エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="150f0-252">「サンプル ワークシート レポート」のコンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="150f0-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="150f0-253">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-253">Click Save.</span></span>
13. <span data-ttu-id="150f0-254">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="150f0-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="150f0-255">支払仕訳帳の処理のテスト用に作成されたコンフィギュレーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="150f0-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="150f0-256">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="150f0-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="150f0-257">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-257">Click New.</span></span>
    * <span data-ttu-id="150f0-258">新しい支払仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="150f0-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="150f0-259">[名前] フィールドに、「VendaPay」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="150f0-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="150f0-260">VendPay</span></span>  
4. <span data-ttu-id="150f0-261">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-261">Click Lines.</span></span>
5. <span data-ttu-id="150f0-262">[口座] フィールドで、「GB_SI_000001」値を指定します。</span><span class="sxs-lookup"><span data-stu-id="150f0-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="150f0-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="150f0-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="150f0-264">[借方] を「1000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="150f0-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="150f0-265">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-265">Click New.</span></span>
8. <span data-ttu-id="150f0-266">[口座] フィールドで、「GB_SI_000005」値を指定します。</span><span class="sxs-lookup"><span data-stu-id="150f0-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="150f0-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="150f0-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="150f0-268">[借方] を「2000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="150f0-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="150f0-269">[通貨] フィールドに、「EUR」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="150f0-270">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="150f0-270">EUR</span></span>  
11. <span data-ttu-id="150f0-271">[相殺アカウント] フィールドで、「GBSI OPER」値を指定します。</span><span class="sxs-lookup"><span data-stu-id="150f0-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="150f0-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="150f0-272">GBSI OPER</span></span>  
12. <span data-ttu-id="150f0-273">[支払方法] フィールドで、「電子」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="150f0-274">電子</span><span class="sxs-lookup"><span data-stu-id="150f0-274">Electronic</span></span>  
13. <span data-ttu-id="150f0-275">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-275">Click Save.</span></span>
14. <span data-ttu-id="150f0-276">[支払の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-276">Click Generate payments.</span></span>
15. <span data-ttu-id="150f0-277">[支払方法] フィールドで、「電子」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="150f0-278">電子</span><span class="sxs-lookup"><span data-stu-id="150f0-278">Electronic</span></span>  
16. <span data-ttu-id="150f0-279">[ファイル名] フィールドに、「Payments」を入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="150f0-280">たとえば、[支払] と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="150f0-281">[銀行口座] フィールドで、「GBSI OPER」と入力します。</span><span class="sxs-lookup"><span data-stu-id="150f0-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="150f0-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="150f0-282">GBSI OPER</span></span>  
18. <span data-ttu-id="150f0-283">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-283">Click OK.</span></span>
19. <span data-ttu-id="150f0-284">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="150f0-284">Click OK.</span></span>
    * <span data-ttu-id="150f0-285">この支払メッセージに使用される各通貨コードの支払明細行および合計の詳細を含む、作成されたワークシートを確認します。</span><span class="sxs-lookup"><span data-stu-id="150f0-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


