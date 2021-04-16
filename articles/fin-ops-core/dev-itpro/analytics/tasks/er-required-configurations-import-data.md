---
title: ER 外部ファイルからデータをインポートするために必要なコンフィギュレーションの作成
description: このトピックでは、外部ファイルから Microsoft Dynamics 365 Finance アプリにデータをインポートできるように電子申告コンフィギュレーションを設計します。
author: NickSelin
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2194bdc918035bf3aebe9b90ddc8a30f9937bb0c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751465"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a><span data-ttu-id="1379b-103">ER 外部ファイルからデータをインポートするために必要なコンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="1379b-103">ER Create required configurations to import data from an external file</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1379b-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) コンフィギュレーションを設計して、外部ファイルからアプリケーションにデータをインポートする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1379b-104">The following steps explain how a user in the System administrator or Electronic reporting developer role can design Electronic reporting (ER) configurations to import data in to the application from an external file.</span></span> <span data-ttu-id="1379b-105">この例では、サンプル会社 Litware, Inc. に必要となる ER 構成を作成します。これらのステップを完了するには、まずタスク ガイド「ER 構成プロバイダを作成し、アクティブとしてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-105">In this example, you will create the required ER configurations for the sample company, Litware, Inc. To complete these steps, you must first complete the steps in the Task guide, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="1379b-106">これらのステップは、USMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="1379b-106">These steps can be completed using the USMF data set.</span></span> <span data-ttu-id="1379b-107">次のファイルをダウンロードしてローカルに保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="1379b-107">You must also download and save the following files locally:</span></span> 

| <span data-ttu-id="1379b-108">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="1379b-108">Content description</span></span>                       | <span data-ttu-id="1379b-109">ファイル名</span><span class="sxs-lookup"><span data-stu-id="1379b-109">File name</span></span>                                     |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="1379b-110">ER データ モデル構成 - 1099</span><span class="sxs-lookup"><span data-stu-id="1379b-110">ER data model configuration - 1099</span></span> | [<span data-ttu-id="1379b-111">1099model,xml</span><span class="sxs-lookup"><span data-stu-id="1379b-111">1099model,xml</span></span>](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| <span data-ttu-id="1379b-112">ER フォーマット構成 - 1099</span><span class="sxs-lookup"><span data-stu-id="1379b-112">ER format configuration - 1099</span></span>    | [<span data-ttu-id="1379b-113">1099format.xml</span><span class="sxs-lookup"><span data-stu-id="1379b-113">1099format.xml</span></span>](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| <span data-ttu-id="1379b-114">XML 形式の受信ドキュメントのサンプル</span><span class="sxs-lookup"><span data-stu-id="1379b-114">Sample of the incoming document in XML format</span></span>                          | [<span data-ttu-id="1379b-115">1099entries.xml</span><span class="sxs-lookup"><span data-stu-id="1379b-115">1099entries.xml</span></span>](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| <span data-ttu-id="1379b-116">受信ドキュメントのデータを管理するブックのサンプル</span><span class="sxs-lookup"><span data-stu-id="1379b-116">Sample of the workbook to manage data of incoming document</span></span>                          | [<span data-ttu-id="1379b-117">1099entries.xlsx</span><span class="sxs-lookup"><span data-stu-id="1379b-117">1099entries.xlsx</span></span>](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

<span data-ttu-id="1379b-118">ER は、ビジネス ユーザーに対し、外部データ ファイルを、.XML または .TXT 形式でインポートするプロセスを構成するための機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="1379b-118">ER offers business users the ability to configure the process of importing external data files to tables in either .XML or .TXT format.</span></span> <span data-ttu-id="1379b-119">最初に、インポートするデータを表す、抽象データ モデルと ER データ モデルのコンフィギュレーションを設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-119">First, an abstract data model and an ER data model configuration must be designed to represent the data that you are importing.</span></span> <span data-ttu-id="1379b-120">次に、インポートするファイルの構造を定義、およびデータをファイルから抽象データ モデルにポートするために使用する方法を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-120">Next, you need to define the structure of the file that you are importing and the method that you will use to port the data from the file to the abstract data model.</span></span> <span data-ttu-id="1379b-121">その抽象データ モデルのために、設計されたデータ モデルに配置される ER 形式のコンフィギュレーションを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-121">The ER format configuration that maps to the designed data model must be created for that abstract data model.</span></span> <span data-ttu-id="1379b-122">次に、インポート データが抽象データ モデル データとして存在する方法、およびテーブルを更新するための使用方法を説明するマッピングで、データ モデルのコンフィギュレーションを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-122">Then, the data model configuration must be extended with a mapping that describes how the imported data is persisted as abstract data model data and how it is used to update tables.</span></span>  <span data-ttu-id="1379b-123">ER データ モデルの構成には、アプリケーションの送信先に対するデータ モデルのバインドを記述する新しいモデル マッピングを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-123">The ER data model configuration must be appended with a new model mapping that describes the binding of the data model to the application's destinations.</span></span>  

<span data-ttu-id="1379b-124">次のシナリオでは、ER データのインポート機能を示します。</span><span class="sxs-lookup"><span data-stu-id="1379b-124">The following scenario shows the ER data import capabilities.</span></span> <span data-ttu-id="1379b-125">これには、外部で追跡された仕入先の取引が含まれ、その後、1099 の仕入先の決済で報告されるようにインポートされたベンダー取引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1379b-125">This includes vendor transactions that are tracked externally and then imported to be reported later in Vendor's settlement for 1099's.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="1379b-126">新しい ER モデル コンフィギュレーションの追加</span><span class="sxs-lookup"><span data-stu-id="1379b-126">Add a new ER model configuration</span></span>
1. <span data-ttu-id="1379b-127">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1379b-127">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="1379b-128">サンプル会社 'Litware, Inc.' の構成プロバイダーを確認する</span><span class="sxs-lookup"><span data-stu-id="1379b-128">Verify that the configuration provider for sample company 'Litware, Inc.'</span></span> <span data-ttu-id="1379b-129">使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1379b-129">is available and marked as active.</span></span> <span data-ttu-id="1379b-130">この構成プロバイダーが表示されない場合は、まず 「構成プロバイダを作成し、アクティブとしてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-130">If you don't see this configuration provider, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   

2. <span data-ttu-id="1379b-131">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-131">Click Reporting configurations.</span></span>

    <span data-ttu-id="1379b-132">データのインポートをサポートするために新しいモデルを作成する代わりに、既にダウンロードしてあるファイル 1099model.xml をロードします。</span><span class="sxs-lookup"><span data-stu-id="1379b-132">Instead of creating of a new model to support data import, load the file, 1099model.xml, that you previously downloaded.</span></span> <span data-ttu-id="1379b-133">このファイルには、仕入先のトランザクションのカスタム データ モデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1379b-133">This file contains the custom data model of vendors' transactions.</span></span> <span data-ttu-id="1379b-134">このデータ モデルは、AOT データ エンティティ内にあるデータ コンポーネントにマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="1379b-134">This data model is mapped to the data components that are in the AOT data entity.</span></span>   

3. <span data-ttu-id="1379b-135">[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-135">Click Exchange.</span></span>
4. <span data-ttu-id="1379b-136">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-136">Click Load from XML file.</span></span>

    <span data-ttu-id="1379b-137">[参照] をクリックし、以前ダウンロードした 1099model.xml ファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="1379b-137">Click Browse and navigate to the 1099model.xml file that you previously downloaded.</span></span>  

5. <span data-ttu-id="1379b-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-138">Click OK.</span></span>
6. <span data-ttu-id="1379b-139">ツリーで、[1099 Payments model] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-139">In the tree, select '1099 Payments model'.</span></span>

## <a name="review-data-model-settings"></a><span data-ttu-id="1379b-140">データ モデルの設定の確認</span><span class="sxs-lookup"><span data-stu-id="1379b-140">Review data model settings</span></span>
1. <span data-ttu-id="1379b-141">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-141">Click Designer.</span></span>

    <span data-ttu-id="1379b-142">このモデルは、ビジネスの観点から仕入先の取引を表すために設計されたもので、実装とは異なります。</span><span class="sxs-lookup"><span data-stu-id="1379b-142">This model is designed to represent vendors' transactions from the business standpoint and are separate from the implementation.</span></span>   

2. <span data-ttu-id="1379b-143">ツリーで、[1099-MISC] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-143">In the tree, expand '1099-MISC'.</span></span>
3. <span data-ttu-id="1379b-144">ツリーで、[1099-MISC\Transactions] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-144">In the tree, select '1099-MISC\Transactions'.</span></span>
4. <span data-ttu-id="1379b-145">ツリーで、[1099-MISC\Transactions] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-145">In the tree, expand '1099-MISC\Transactions'.</span></span>

    <span data-ttu-id="1379b-146">このモデルのトランザクションの要素は、個々のトランザクションを表します。</span><span class="sxs-lookup"><span data-stu-id="1379b-146">The Transactions element of this model represents individual transactions.</span></span> <span data-ttu-id="1379b-147">子要素は、トランザクションごとに、仕入先の口座およびトランザクションの日付などの必須情報を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="1379b-147">The child elements are used to specify required details, such as vendor account and transaction date, for each transaction.</span></span>   

5. <span data-ttu-id="1379b-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-148">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a><span data-ttu-id="1379b-149">データのインポートをサポートする新しい ER 書式のコンフィギュレーションの追加</span><span class="sxs-lookup"><span data-stu-id="1379b-149">Add a new ER format configuration that supports data import</span></span>
<span data-ttu-id="1379b-150">このサブタスクの手順は、外部ファイルからのデータ インポートを管理するために、書式コンフィギュレーションを新規作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1379b-150">The steps in this subtask show you how a new format configuration can be created to manage data import from external files.</span></span>   
1. <span data-ttu-id="1379b-151">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1379b-151">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="1379b-152">[新規] フィールドで、「1099 Payments model のデータ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1379b-152">In the New field, enter 'Format based on data model 1099 Payments model'.</span></span>
3. <span data-ttu-id="1379b-153">[データのインポートのサポート] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-153">Select Yes in the Supports data import field.</span></span>
4. <span data-ttu-id="1379b-154">ESC キーを押してこのページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-154">Press ESC key to close this page.</span></span>

    <span data-ttu-id="1379b-155">データのインポートをサポートするために新しい書式を作成する代わりに、既にダウンロードしてあるファイル 1099format.xml をロードします。</span><span class="sxs-lookup"><span data-stu-id="1379b-155">Instead of creating a new format to support data import, load the 1099format.xml file that you previously downloaded.</span></span> <span data-ttu-id="1379b-156">このファイルには、インポートするファイルの定義済み構造と、ベンダーのトランザクションのカスタムデータモデルへの構造のマッピングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1379b-156">This file contains the defined structure of the file you are importing and the mapping of the structure to the custom data model of vendors' transactions.</span></span>   
5. <span data-ttu-id="1379b-157">[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-157">Click Exchange.</span></span>
6. <span data-ttu-id="1379b-158">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-158">Click Load from XML file.</span></span>
    <span data-ttu-id="1379b-159">[参照] をクリックし、以前ダウンロードした 1099format.xml ファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="1379b-159">Click Browse and navigate to the 1099format.xml file that you previously downloaded.</span></span>  
7. <span data-ttu-id="1379b-160">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-160">Click OK.</span></span>
8. <span data-ttu-id="1379b-161">ツリーで、[1099 Payments model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-161">In the tree, expand '1099 Payments model'.</span></span>
9. <span data-ttu-id="1379b-162">ツリーで、[1099 Payments model\Format for importing vendors' transactions] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-162">In the tree, select '1099 Payments model\Format for importing vendors' transactions'.</span></span>

## <a name="review-format-settings"></a><span data-ttu-id="1379b-163">書式設定の確認</span><span class="sxs-lookup"><span data-stu-id="1379b-163">Review format settings</span></span>
1. <span data-ttu-id="1379b-164">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-164">Click Designer.</span></span>
2. <span data-ttu-id="1379b-165">[詳細の表示] をオンに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="1379b-165">Toggle 'Show details' on.</span></span>
3. <span data-ttu-id="1379b-166">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-166">Click Expand/collapse.</span></span>
4. <span data-ttu-id="1379b-167">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-167">Click Expand/collapse.</span></span>

    <span data-ttu-id="1379b-168">設計された形式は、外部ファイルの予想構造を表します。</span><span class="sxs-lookup"><span data-stu-id="1379b-168">The designed format represents the expected structure of the external file.</span></span> <span data-ttu-id="1379b-169">このファイルは XML 形式であり、決済のルート要素を含んでいる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-169">This file must be in XML format and have the settlement root element.</span></span> <span data-ttu-id="1379b-170">各仕入先の取引は、ゼロ対多の多様性を持つように定義されている取引要素で表されます。</span><span class="sxs-lookup"><span data-stu-id="1379b-170">Each vendor's transaction is represented by the transaction element that is defined as having zero-to-many multiplicity.</span></span> <span data-ttu-id="1379b-171">つまり、受信ファイルが 0 個から複数のトランザクションの範囲を含む可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-171">This means that the incoming file may contain anywhere from zero to multiple transactions.</span></span> <span data-ttu-id="1379b-172">「取引 」要素のネストされた要素は、単一の取引の属性を表します。</span><span class="sxs-lookup"><span data-stu-id="1379b-172">Nested elements of the 'transaction' element represent a single transaction's attributes.</span></span> <span data-ttu-id="1379b-173">国を除くすべての属性が、必須としてマークされていることに注意してください。これはインポートするファイルに含める必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="1379b-173">Note that all attributes, except country, are marked as mandatory, meaning that it is required to have them in the importing file.</span></span>   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a><span data-ttu-id="1379b-174">データ モデルに対する書式マッピングの設定の確認</span><span class="sxs-lookup"><span data-stu-id="1379b-174">Review the settings of the format mapping to the data model</span></span>
1. <span data-ttu-id="1379b-175">[形式をモデルにマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-175">Click Map format to model.</span></span>

    <span data-ttu-id="1379b-176">マッピング 「仕入れ先の取引をインポートする 」 には、受信する XML ファイルからカスタム データモデルの選択された部分へのデータ転送のルールを含んでおり、1099-MISC の定義を選択することで設定されます。</span><span class="sxs-lookup"><span data-stu-id="1379b-176">The mapping 'For importing vendors' transactions' contains the data transfer rules from the incoming XML file to the selected part of the custom data model, which is defined by selecting the1099-MISC definition.</span></span>  

2. <span data-ttu-id="1379b-177">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-177">Click Designer.</span></span>
3. <span data-ttu-id="1379b-178">[詳細の表示] をオンに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="1379b-178">Toggle 'Show details' on.</span></span>
4. <span data-ttu-id="1379b-179">ツリーで、[format: Record] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-179">In the tree, expand 'format: Record'.</span></span>
5. <span data-ttu-id="1379b-180">ツリーで、[format: Record] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-180">In the tree, select 'format: Record'.</span></span>

    <span data-ttu-id="1379b-181">設計された形式が、ここではデータ ソース コンポーネントとして示されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-181">Note that the designed format is presented here as a data source component.</span></span>  

6. <span data-ttu-id="1379b-182">ツリーで、`format: Record\*settlement: XML Element 1..1 (settlement): Record` を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-182">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record`.</span></span>
7. <span data-ttu-id="1379b-183">ツリーで、`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list` を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-183">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`.</span></span>
8. <span data-ttu-id="1379b-184">ツリーで、`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record` を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-184">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.</span></span>
9. <span data-ttu-id="1379b-185">ツリーで、`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record` を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-185">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`.</span></span>
10. <span data-ttu-id="1379b-186">ツリーで、`format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record` を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-186">In the tree, select `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.</span></span>

    <span data-ttu-id="1379b-187">事前定義された「フォーマット 」データ ソース 構成では、必須およびオプションのフォーマット要素の表示が異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-187">Note that the presentation of mandatory and optional format elements is different in the predefined 'format' data source component.</span></span>  
11. <span data-ttu-id="1379b-188">ツリーで、[Transactions: Record list= format.settlement.'$enumerated'] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-188">In the tree, expand 'Transactions: Record list= format.settlement.'$enumerated''.</span></span>

    <span data-ttu-id="1379b-189">インポート ファイルの構造を定義する書式の要素が、カスタム データ モデルの要素にバインドされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-189">Note that the elements of the format that defines the structure of the imported file are bound to the elements of the custom data model.</span></span> <span data-ttu-id="1379b-190">これらのバインドに基づき、インポートされた XML ファイルの内容は、実行時に既存のデータ モデル内に格納されます。</span><span class="sxs-lookup"><span data-stu-id="1379b-190">Based on these bindings, the content of the imported XML file will be stored at run-time in the existing data model.</span></span> <span data-ttu-id="1379b-191">国要素のバインディングに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-191">Pay attention to the binding of the country element.</span></span> <span data-ttu-id="1379b-192">このような要素を持たない入力ファイルの取引要素については、既定の国コード 「USA 」 がデータ モデルに取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="1379b-192">For any transaction element in the incoming file that has no such element, the default country code 'USA' will be populated in the data model.</span></span>  

12. <span data-ttu-id="1379b-193">[検証] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-193">Click the Validations tab.</span></span>

    <span data-ttu-id="1379b-194">この書式マッピングには、ビジネス観点からインポートされたデータの正確性を検証する、ユーザー定義のロジックが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-194">This format mapping may contain user-defined logic to validate the accuracy of the imported data from a business standpoint.</span></span> <span data-ttu-id="1379b-195">例えば、設定に基づいて、定義された国コードのないインポート ファイル内の取引については、情報ログで警告メッセージが生成され、ユーザーに通知し、取引のシーケンス番号を示します。</span><span class="sxs-lookup"><span data-stu-id="1379b-195">For example, based on the setting, for any transaction in the importing file without a defined country code, a warning message will be generated in the Infolog informing the user about the case and indicating the transaction's sequence number.</span></span>  

13. <span data-ttu-id="1379b-196">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-196">Close the page.</span></span>

## <a name="run-the-format-mapping-to-the-data-model"></a><span data-ttu-id="1379b-197">データ モデルに対する書式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="1379b-197">Run the format mapping to the data model</span></span>
<span data-ttu-id="1379b-198">テストのため、この書式マッピングを実行します。</span><span class="sxs-lookup"><span data-stu-id="1379b-198">Execute this format mapping for testing purposes.</span></span> <span data-ttu-id="1379b-199">以前ダウンロードしたファイル、1099entries.xml を使用します。</span><span class="sxs-lookup"><span data-stu-id="1379b-199">Use the file 1099entries.xml that you previously downloaded.</span></span> <span data-ttu-id="1379b-200">このファイルは、仕入先トランザクションを管理するために使用する 1099entries.xlsx ワークブックからエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="1379b-200">You can export this file from the 1099entries.xlsx workbook that is used to manage vendor transactions.</span></span> <span data-ttu-id="1379b-201">生成された出力は選択された XML ファイルからインポートされ、実際のインポート時にカスタム データ モデルを設定します。</span><span class="sxs-lookup"><span data-stu-id="1379b-201">The generated output will be imported from the selected XML file and populate the custom data model at real import.</span></span>  

1. <span data-ttu-id="1379b-202">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-202">Click Run.</span></span>

    <span data-ttu-id="1379b-203">[参照] をクリックし、以前ダウンロードした 1099entries.xml ファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="1379b-203">Click Browse and navigate to the 1099entries.xml file that you previously downloaded.</span></span>  

2. <span data-ttu-id="1379b-204">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-204">Click OK.</span></span>

    <span data-ttu-id="1379b-205">インポートされたファイルのトランザクションに国コードが無いことに関する警告メッセージに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-205">Note the warning message about a missing country code for a transaction in the imported file.</span></span>  
    
    <span data-ttu-id="1379b-206">選択ファイルからインポートされてデータ モデルにポートされたデータを表す出力を、XML 書式で確認します。</span><span class="sxs-lookup"><span data-stu-id="1379b-206">Review the output in XML format, which represents the data that has been imported from the selected file and ported to the data model.</span></span>   

3. <span data-ttu-id="1379b-207">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-207">Close the page.</span></span>
4. <span data-ttu-id="1379b-208">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-208">Close the page.</span></span>

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a><span data-ttu-id="1379b-209">出力先に対する書式マッピングの設定の確認</span><span class="sxs-lookup"><span data-stu-id="1379b-209">Review the settings for the model mapping to the destinations</span></span>
1. <span data-ttu-id="1379b-210">ツリーで、[1099 Payments model] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-210">In the tree, select '1099 Payments model'.</span></span>
2. <span data-ttu-id="1379b-211">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-211">Click Designer.</span></span>
3. <span data-ttu-id="1379b-212">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-212">Click Map model to datasource.</span></span>

    <span data-ttu-id="1379b-213">1099 の手動トランザクション インポート用マッピングは、宛先の方向タイプで定義されました。</span><span class="sxs-lookup"><span data-stu-id="1379b-213">The mapping For 1099 manual transactions import has been defined with the To destination direction type.</span></span> <span data-ttu-id="1379b-214">つまり、データのインポートをサポートするための入力がされ、アプリケーション内のテーブルを更新するために、インポートされた外部ファイルおよび抽象データとして存在するデータが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1379b-214">This means that it has been entered to support data import and contains the setting of rules defining how the imported external file and persisted as abstract data model data is used to update tables in the application.</span></span>  

4. <span data-ttu-id="1379b-215">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-215">Click Designer.</span></span>
5. <span data-ttu-id="1379b-216">ツリーで、[model: Data model 1099 Payments model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-216">In the tree, expand 'model: Data model 1099 Payments model'.</span></span>
6. <span data-ttu-id="1379b-217">ツリーで、[model: Data model 1099 Payments model\Transactions: Record list] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-217">In the tree, expand 'model: Data model 1099 Payments model\Transactions: Record list'.</span></span>

    <span data-ttu-id="1379b-218">設計されたモデルが、ここではデータ ソース要素として示されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-218">Note that the designed model is presented here as a data source element.</span></span> <span data-ttu-id="1379b-219">実行時に、外部ファイルからインポートされたデータが格納されます。</span><span class="sxs-lookup"><span data-stu-id="1379b-219">At runtime, it will contain the data that is imported from the external file.</span></span> <span data-ttu-id="1379b-220">システム内でトランザクションの仕入先口座の入力が可能であるか、国および都道府県コードを入力する組合せ等が存在するかどうかなどを含め、インポート データが現在のアプリケーションのデータに準拠するように、複数のテーブルがデータ ソースとして追加されました。</span><span class="sxs-lookup"><span data-stu-id="1379b-220">Several tables were added as data source elements to ensure that the imported data is compliant with the data of the current application, including whether the importing transaction vendor account is available in the system, whether the combination of the importing country and state codes exists, etc.</span></span>  

7. <span data-ttu-id="1379b-221">ツリーで、[model: Data model 1099 Payments model\Transactions: Record list\$failed: Calculated field = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-221">In the tree, select 'model: Data model 1099 Payments model\Transactions: Record list\$failed: Calculated field = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean'.</span></span>
8. <span data-ttu-id="1379b-222">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-222">Click Edit.</span></span>
9. <span data-ttu-id="1379b-223">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-223">Click Edit formula.</span></span>

    <span data-ttu-id="1379b-224">1 つのインポートされた取引に対して少なくとも 1 つの検証が失敗した場合、この取引はデータソース属性 「$failed」 によって失敗したものとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="1379b-224">When at least one validation fails for a single imported transaction, this transaction will be marked as failed by the data source attribute '$failed'.</span></span>  

10. <span data-ttu-id="1379b-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-225">Close the page.</span></span>
11. <span data-ttu-id="1379b-226">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-226">Click Cancel.</span></span>
12. <span data-ttu-id="1379b-227">ツリーで、[tax1099trans: Table 'VendSettlementTax1099' records= model.Validated] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-227">In the tree, select 'tax1099trans: Table 'VendSettlementTax1099' records= model.Validated'.</span></span>
13. <span data-ttu-id="1379b-228">[宛先の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-228">Click Edit destination.</span></span>

    <span data-ttu-id="1379b-229">インポートされたデータでアプリケーション テーブルが更新される方法を指定するため、この ER 宛先が追加されました。</span><span class="sxs-lookup"><span data-stu-id="1379b-229">This ER destination was added to specify how the imported data will update the application tables.</span></span> <span data-ttu-id="1379b-230">この場合、データ テーブル VendSettlementTax1099 が選択されました。</span><span class="sxs-lookup"><span data-stu-id="1379b-230">In this case, the data table VendSettlementTax1099 has been selected.</span></span> <span data-ttu-id="1379b-231">レコード アクションの挿入が選択されているため、インポートされたトランザクションは VendSettlementTax1099 テーブルに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="1379b-231">Because the record action Insert has been selected, the imported transactions will be inserted in the table VendSettlementTax1099.</span></span> <span data-ttu-id="1379b-232">単一のモデル マッピングに複数の宛先が含まれる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-232">Note that a single model mapping may contain several destinations.</span></span> <span data-ttu-id="1379b-233">つまり、インポートしたデータを使って、複数のアプリケーションのテーブルを一度に更新することができます。</span><span class="sxs-lookup"><span data-stu-id="1379b-233">This means that the imported data can be used to update multiple application's tables at once.</span></span> <span data-ttu-id="1379b-234">テーブル、ビュー、およびデータ エンティティは、ER 宛先として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1379b-234">Tables, views, and data entities can be used as ER destinations.</span></span>   

    <span data-ttu-id="1379b-235">このアクションのために特別に設計されたアプリケーション (ボタンまたはメニュー項目など) 内の点からマッピングがコールされる場合、ER の宛先は統合点としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-235">If the mapping will be called from a point in the application (such as button or menu item) that was specifically designed for this action, the ER destination should be marked as the integration point.</span></span> <span data-ttu-id="1379b-236">この例では、ERTableDestination#VendSettlementTax1099 の点です。</span><span class="sxs-lookup"><span data-stu-id="1379b-236">In this example this is the ERTableDestination#VendSettlementTax1099 point.</span></span>  

14. <span data-ttu-id="1379b-237">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-237">Click Cancel.</span></span>
15. <span data-ttu-id="1379b-238">[すべて表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-238">Click Show all.</span></span>
16. <span data-ttu-id="1379b-239">[マップ済みのものだけを表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-239">Click Show mapped only.</span></span>
17. <span data-ttu-id="1379b-240">ツリーで、['tax1099trans: Table 'VendSettlementTax1099' records= model.Validated] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1379b-240">In the tree, expand 'tax1099trans: Table 'VendSettlementTax1099' records= model.Validated'.</span></span>

    <span data-ttu-id="1379b-241">唯一検証されたトランザクションを含むデータ ソース要素が、作成された宛先にバインドされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-241">Note that the data source element that contains the only validated transactions is bound to the created destination.</span></span> <span data-ttu-id="1379b-242">インポートした取引をフィルター処理して、アプリケーションのデータと互換性のない取引をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="1379b-242">You can filter the imported transactions to skip the ones that are incompatible with the applications' data.</span></span>  

18. <span data-ttu-id="1379b-243">ツリーで、['failed: Table 'VendSettlementTax1099Entity' records= model.Failed] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-243">In the tree, select 'failed: Table 'VendSettlementTax1099Entity' records= model.Failed'.</span></span>
19. <span data-ttu-id="1379b-244">[検証] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-244">Click the Validations tab.</span></span>

    <span data-ttu-id="1379b-245">このモデル マッピングには、既存のアプリケーション データからインポートされたデータの正確性を検証する、ユーザー定義のロジックが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-245">This model mapping may contain user-defined logic to validate the correctness of the imported data from the existing application data.</span></span> <span data-ttu-id="1379b-246">たとえば、現在の設定に応じて、インポート ファイルのトランザクションにシステム内に無い仕入れ先口座が含まれる場合、ユーザーに通知して、不正確な仕入先の口座コードを示す警告メッセージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="1379b-246">For example, based on the present setting, for any transaction in the imported file with a vendor account that is not in the system, a warning message will be generated informing the user and indicating the incorrect vendor account code.</span></span>  

    <span data-ttu-id="1379b-247">[検証後のアクション] オプションを各検証に使用して、インポート処理を継続するか停止するか、既に実行された挿入や更新を保持するかロールバックするか指定することができることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-247">Note that the Post validation action option can be used for each validation, to specify whether the import process must be continued or stopped, as well as if the already performed inserts/updates can be kept or rolled back.</span></span>  

20. <span data-ttu-id="1379b-248">[マップ済みのものだけを表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-248">Click Show mapped only.</span></span>
21. <span data-ttu-id="1379b-249">[すべて表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-249">Click Show all.</span></span>
22. <span data-ttu-id="1379b-250">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-250">Close the page.</span></span>

    <span data-ttu-id="1379b-251">このモデル マッピングを実行して、設計された形式およびモデル マッピングをテストします。</span><span class="sxs-lookup"><span data-stu-id="1379b-251">Execute this model mapping to test the designed format and model mappings.</span></span> <span data-ttu-id="1379b-252">1099entries.xml ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="1379b-252">Use the file 1099entries.xml.</span></span> <span data-ttu-id="1379b-253">選択したファイルからのデータはシステムにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="1379b-253">The data from the selected file will be imported in to the system.</span></span>  

23. <span data-ttu-id="1379b-254">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-254">Click Run.</span></span>

    <span data-ttu-id="1379b-255">ダイアログ ボックス内に、インポートされたファイルをパースしてからデータをデータ モデルにポートするために使用する、書式マッピングに関する追加質問が含まれていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-255">Note that the dialog box contains no additional questions about the format mapping that must be used to parse the imported file and then port the data to the data model.</span></span> <span data-ttu-id="1379b-256">これは、このモデルを使用する書式が現在 1 つのみ存在するためです。これはデータ インポートをサポートするために設計されたとマークされています。</span><span class="sxs-lookup"><span data-stu-id="1379b-256">This is because there is currently only one format that uses this model, which is marked as designed to support data import.</span></span>  
    
    <span data-ttu-id="1379b-257">インポートされたトランザクションを、手動で入力済みまたはインポート済みの他のトランザクションと区別するための、伝票 ID を定義します。</span><span class="sxs-lookup"><span data-stu-id="1379b-257">Define the voucher ID to differentiate the imported transactions from other transactions that may already have been entered manually or imported.</span></span>  

24. <span data-ttu-id="1379b-258">[伝票 ID の入力] フィールドで、'IMPORT-001' と入力します。</span><span class="sxs-lookup"><span data-stu-id="1379b-258">In the Enter voucher id field, type 'IMPORT-001'.</span></span>

    <span data-ttu-id="1379b-259">'1099entries.xml' ファイルを参照して取得します。</span><span class="sxs-lookup"><span data-stu-id="1379b-259">Browse to get the '1099entries.xml' file.</span></span>  

25. <span data-ttu-id="1379b-260">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-260">Click OK.</span></span>

    <span data-ttu-id="1379b-261">生成された警告の一覧には、不正確な仕入先口座、不正確な税 1099 ボックス コード、不足している国コード等に関する情報が用意されます。この警告の一覧と、実行 XML ファイルに含まれるコンテンツを比較します。</span><span class="sxs-lookup"><span data-stu-id="1379b-261">The list of generated warnings provides information about incorrect vendor accounts, an incorrect tax 1099 box code, missing country codes, etc. Compare this list of warnings to the content that is included in the execution XML file.</span></span>  

26. <span data-ttu-id="1379b-262">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-262">Close the page.</span></span>
27. <span data-ttu-id="1379b-263">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-263">Close the page.</span></span>
28. <span data-ttu-id="1379b-264">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-264">Close the page.</span></span>
29. <span data-ttu-id="1379b-265">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-265">Close the page.</span></span>
30. <span data-ttu-id="1379b-266">[買掛金勘定] > [定期処理のタスク] > [税金 1099] > [1099s の仕入先決済] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1379b-266">Go to Accounts payable > Periodic tasks > Tax 1099 > Vendor settlement for 1099s.</span></span>

    <span data-ttu-id="1379b-267">このフォームでは、インポートされたトランザクションに基づいて作成された Tax1099Summary テーブルに、累積的なトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="1379b-267">This form shows the cumulative transactions in the Tax1099Summary table that have been created based on imported transactions.</span></span>  

31. <span data-ttu-id="1379b-268">[開始日] フィールドで、日付を「2000-01-01」に設定します。</span><span class="sxs-lookup"><span data-stu-id="1379b-268">In the From date field, set the date to '2000-01-01'.</span></span>
32. <span data-ttu-id="1379b-269">[手動 1099 トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-269">Click Manual 1099 transactions.</span></span>

    <span data-ttu-id="1379b-270">このフォームには、手動で追加されたトランザクションと、直前にインポートされたトランザクションのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1379b-270">This form contains the list of transactions that were added manually and those that we just imported.</span></span>  

33. <span data-ttu-id="1379b-271">[伝票列] フィルターを開きます。</span><span class="sxs-lookup"><span data-stu-id="1379b-271">Open Voucher column filter.</span></span>
34. <span data-ttu-id="1379b-272">[次の値で始まる] フィルター演算子を使用して、[伝票] フィールドに "IMPORT-001" を入力します。</span><span class="sxs-lookup"><span data-stu-id="1379b-272">Enter a filter value of "IMPORT-001" on the "Voucher" field using the "begins with" filter operator.</span></span>

## <a name="review-the-relationship-between-model-and-format-mappings"></a><span data-ttu-id="1379b-273">モデルと書式マッピング間の関係の確認</span><span class="sxs-lookup"><span data-stu-id="1379b-273">Review the relationship between model and format mappings</span></span>
1. <span data-ttu-id="1379b-274">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-274">Close the page.</span></span>
2. <span data-ttu-id="1379b-275">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-275">Close the page.</span></span>
3. <span data-ttu-id="1379b-276">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1379b-276">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="1379b-277">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-277">Click Reporting configurations.</span></span>
5. <span data-ttu-id="1379b-278">ツリーで、[1099 Payments model] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-278">In the tree, select '1099 Payments model'.</span></span>

    <span data-ttu-id="1379b-279">同じデータの .TXT ファイル形式でのインポートをサポートすると仮定します。</span><span class="sxs-lookup"><span data-stu-id="1379b-279">Assume that you want to support importing the same data but from a .TXT file format.</span></span>   

6. <span data-ttu-id="1379b-280">[コンフィギュレーションの作成] をクリックすると、ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="1379b-280">Click Create configuration to open the dialog box.</span></span> 
7. <span data-ttu-id="1379b-281">[新規] フィールドで、「1099 Payments model のデータ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1379b-281">In the New field, enter 'Format based on data model 1099 Payments model'.</span></span>
8. <span data-ttu-id="1379b-282">[名前] フィールドに、「TXT ファイルからデータをインポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1379b-282">In the Name field, type 'Import data from TXT file'.</span></span>
9. <span data-ttu-id="1379b-283">[データのインポートのサポート] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-283">Select Yes in the Supports data import field.</span></span>
10. <span data-ttu-id="1379b-284">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-284">Click Create configuration.</span></span>
11. <span data-ttu-id="1379b-285">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-285">Click Designer.</span></span>
12. <span data-ttu-id="1379b-286">[形式をモデルにマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-286">Click Map format to model.</span></span>
13. <span data-ttu-id="1379b-287">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-287">Click New.</span></span>
14. <span data-ttu-id="1379b-288">[定義] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-288">In the Definition field, enter or select a value.</span></span>

    <span data-ttu-id="1379b-289">[1099-MISC] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-289">Select '1099-MISC' option.</span></span>  

15. <span data-ttu-id="1379b-290">[名前] フィールドに、「TXT ファイルからデータをインポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1379b-290">In the Name field, type 'Import data from TXT file'.</span></span>
16. <span data-ttu-id="1379b-291">[説明] フィールドに、「TXT ファイルからデータをインポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1379b-291">In the Description field, type 'Import data from TXT file'.</span></span>
17. <span data-ttu-id="1379b-292">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-292">Click Save.</span></span>
18. <span data-ttu-id="1379b-293">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-293">Close the page.</span></span>
19. <span data-ttu-id="1379b-294">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-294">Close the page.</span></span>
20. <span data-ttu-id="1379b-295">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-295">Click Edit.</span></span>

    <span data-ttu-id="1379b-296">修正プログラム 「KB 4012871 異なるバージョンの Dynamics 365 Finance に展開するための異なる種類の前提条件を指定する機能を備えた、分離された構成でのGERモデル マッピングのサポート」 ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)) をインストールした場合、入力したフォーマット設定に対して次の手順 「'モデル マッピングの既定' のフラグをオンにする」 を実行します。</span><span class="sxs-lookup"><span data-stu-id="1379b-296">If you installed the hotfix "KB 4012871 Support of GER model mappings in separated configurations with an ability to specify different kinds of prerequisites for deploying them on different versions of Dynamics 365 Finance" ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), execute the next step "Turn the flag 'Default for model mapping' on" for the entered format configuration.</span></span> <span data-ttu-id="1379b-297">それ以外の場合、次のステップをスキップします。</span><span class="sxs-lookup"><span data-stu-id="1379b-297">Skip the next step otherwise.</span></span>  

21. <span data-ttu-id="1379b-298">[モデル マッピング] フィールドの既定値で [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-298">Select Yes in the Default for model-mapping field.</span></span>
22. <span data-ttu-id="1379b-299">ツリーで、[1099 Payments model] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-299">In the tree, select '1099 Payments model'.</span></span>
23. <span data-ttu-id="1379b-300">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-300">Click Designer.</span></span>
24. <span data-ttu-id="1379b-301">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-301">Click Map model to datasource.</span></span>
25. <span data-ttu-id="1379b-302">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-302">Click Run.</span></span>

    <span data-ttu-id="1379b-303">修正プログラム KB 4012871 異なるバージョンで展開するために異なる種類の要件を指定する機能を使用した別個のコンフィギュレーションでの GER モデル マッピングのサポート ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)) をインストールした場合、ルックアップ フィールドで目的のモデル マッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="1379b-303">If you installed the hotfix, KB 4012871 Support of GER model mappings in separated configurations with an ability to specify different kinds of prerequisites for deploying them on different versions ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), select the preferred model mapping in the lookup field.</span></span> <span data-ttu-id="1379b-304">修正プログラムをまだインストールしていない場合、マッピングは既定の書式設定の定義で既に選択されているため、次のステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="1379b-304">If you haven't installed the hotfix yet, skip to the next step as the mapping has already been selected by the definition of the default format configuration.</span></span>  
    
    <span data-ttu-id="1379b-305">修正プログラムの KB 4012871 がインストールされていない場合、インポートするファイルの解析に使用される追加のモデル マッピング質問がダイアログ ボックスに含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1379b-305">If you have not installed the hotfix, KB 4012871, notice that the dialog box contains an additional model-mapping question that is used to parse the file that you are importing.</span></span> <span data-ttu-id="1379b-306">次にデータはダイアログ ボックスからデータ モデルにポートされます。</span><span class="sxs-lookup"><span data-stu-id="1379b-306">The data is then ported from the dialog box to the data model.</span></span> <span data-ttu-id="1379b-307">現時点では、インポートする計画のファイル タイプに応じてどの書式マッピングを使用する必要があるか選択することができます。</span><span class="sxs-lookup"><span data-stu-id="1379b-307">Currently, you can choose which format mapping must be used depending on the type of file that you plan to import.</span></span>  
    
    <span data-ttu-id="1379b-308">アクション用に特別に設計されたアプリケーション内のポイントからこのモデル マッピングをコールする場合は、ER の出力先および書式マッピングを統合の一部としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1379b-308">If you plan to call this model mapping from a point in the application that is specifically designed for the action, the ER destination and the format mapping must be marked as part of the integration.</span></span>  

26. <span data-ttu-id="1379b-309">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1379b-309">Click Cancel.</span></span>
27. <span data-ttu-id="1379b-310">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-310">Close the page.</span></span>
28. <span data-ttu-id="1379b-311">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1379b-311">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
