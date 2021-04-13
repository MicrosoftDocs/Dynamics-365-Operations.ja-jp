---
title: ソース コードからユーザー入力パラメーターのデータ ソース値を開始する
description: このトピックでは、ソース コードからユーザー入力パラメーター タイプのデータ ソース値を開始する方法について説明します。
author: NickSelin
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 702254c8e9f4ca1dc1f185e70e82c6f552dcd06f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743991"
---
# <a name="initiate-data-source-values-of-the-user-input-parameter-type-from-source-code"></a><span data-ttu-id="0a5ac-103">ソース コードからユーザー入力パラメーターのデータ ソース値を開始する</span><span class="sxs-lookup"><span data-stu-id="0a5ac-103">Initiate data source values of the USER INPUT PARAMETER type from source code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a5ac-104">ER [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)および ER [形式](general-electronic-reporting.md#FormatComponentOutbound)コンポーネントを設計する場合は、*ユーザー入力パラメーター* タイプを使用して、ER フォーマットの実行が開始される前に実行時に提供される必要な値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-104">When you design ER [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) and ER [format](general-electronic-reporting.md#FormatComponentOutbound) components, use the data sources of the *User input parameter* type to obtain the necessary values offered at runtime before the execution of an ER format begins.</span></span> <span data-ttu-id="0a5ac-105">このダイアログ ボックスは、必要なパラメーターを別のページに入力した場合、または ER フォーマットを無人 (バッチ) モードで実行した場合に、プログラムを使用してオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-105">This dialog box can be programmatically turned off when the required parameters are entered on another page or when an ER format is executed in unattended (batch) mode.</span></span> <span data-ttu-id="0a5ac-106">ER ダイアログ ボックスがオフになっている場合、ソース コードから *ユーザー入力パラメーター* タイプのデータ ソース値を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-106">When the ER dialog box is turned off, you must initiate the data source values of the *User input parameter* type from source code.</span></span>

## <a name="format-components-for-outgoing-electronic-documents"></a><span data-ttu-id="0a5ac-107">送信する電子ドキュメントの形式のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="0a5ac-107">Format components for outgoing electronic documents</span></span>

<span data-ttu-id="0a5ac-108">送信ドキュメントを生成するには、ER [形式](general-electronic-reporting.md#FormatComponentOutbound)をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-108">You can configure an ER [format](general-electronic-reporting.md#FormatComponentOutbound) to generate an outbound document.</span></span> <span data-ttu-id="0a5ac-109">この形式をコンフィギュレーションすると、送信ドキュメントに入力するために使用されるデータ ソースとして ER [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components)が選択されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-109">When you configure the format, an ER [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) is selected as the data source used to fill in the outbound document.</span></span> <span data-ttu-id="0a5ac-110">ER [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)をコンフィギュレーションして、選択したデータ モデルが実行時にアプリケーション データによってどのように入力されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-110">Configure an ER [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) to specify how the selected data model is filled in by application data at runtime.</span></span> <span data-ttu-id="0a5ac-111">モデル マッピングを設計するときは、データ ソースを指定して、さまざまなソースから目的の値を収集しし、それらをデータ モデルに入力します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-111">When you design your model mapping, specify data sources to collect the desired values from different sources and populate them to your data model.</span></span> <span data-ttu-id="0a5ac-112">特に、*ユーザー入力パラメーター* タイプのデータ ソースを使用して、ER 形式を最初に[実行](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export)したときに表示される ER ユーザー ダイアログ ボックスでユーザーが入力した値をデータ モデルに入力できます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-112">Among others, you might use data sources of the *User input parameter* type to fill in your data model with values that are entered by users on the ER user dialog box that is offered when you first [run](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) an ER format.</span></span> 

<span data-ttu-id="0a5ac-113">送信ドキュメントを生成するようにコンフィギュレーションされた ER 形式の場合、`ERObjectsFactory` クラスの `createFormatMappingRunByFormatMappingId()` メソッドの `_showPromptDialog` パラメーターを使用して、ER ダイアログ ボックスをプログラムでオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-113">For an ER format that is configured to generate an outbound document, the ER dialog box can be programmatically turned off by using the `_showPromptDialog` parameter of the `createFormatMappingRunByFormatMappingId()` method of the `ERObjectsFactory` class.</span></span> <span data-ttu-id="0a5ac-114">この場合、ソースコードから *ユーザー入力パラメーター* タイプのデータ ソースの値を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-114">In this case, you need to initiate values of data sources of the *User input parameter* type from the source code.</span></span> <span data-ttu-id="0a5ac-115">それには、次のパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-115">To do this, use the following pattern.</span></span>

```xpp
ERModelDefinitionInputParametersAction Obj = new ERModelDefinitionInputParametersAction();
Obj.addParameter(<path to an ER data source>, <data source value>);
ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingID, fileName, false)
            .withParameter(Obj)
            .run();
```

<span data-ttu-id="0a5ac-116">送信ドキュメントを生成するようにコンフィギュレーションされている ER フォーマットの場合、ER データ ソースへのパスは、スラッシュ (**/**) 文字で区切られた接頭語と接尾語から構成されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-116">For ER formats that are configured to generate an outbound document, the path to an ER data source is constructed from the prefix and the suffix that are separated by a slash ( **/** ) character.</span></span> <span data-ttu-id="0a5ac-117">接頭語は、実行中の ER 形式に存在する *モデル* タイプのデータ ソースの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-117">The prefix represents the name of a data source of the *Model* type that resides in the running ER format.</span></span> <span data-ttu-id="0a5ac-118">接尾語は、関連する [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components)の実装として実行中の ER 形式で使用される [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)に存在する *ユーザー入力パラメーター* タイプのデータ ソースへのパスを表します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-118">The suffix represents the path to a data source of the *User input parameter* type that resides in a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) that is used by the running ER format as the implementation of the relevant [data model](general-electronic-reporting.md#data-model-and-model-mapping-components).</span></span>

> [!TIP]
> <span data-ttu-id="0a5ac-119">データ ソース パスのノードは、スラッシュ (**/**) 文字で区切られ ます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-119">The nodes of a data source path are separated by a slash ( **/** ) character.</span></span> <span data-ttu-id="0a5ac-120">`ERPath::Combine()` メソッドを使用して、パスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-120">Use the `ERPath::Combine()` method to construct a path.</span></span>

<span data-ttu-id="0a5ac-121">詳細については、例として使用できる `BankPaymBalanceXML` アプリケーション クラスのソース コードを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-121">For more information, review the source code of the `BankPaymBalanceXML` application class that can be used as an example.</span></span> <span data-ttu-id="0a5ac-122">グローバル リポジトリから、このアプリケーション クラスを使用して Finance インスタンスに呼び出される **BLWI 形式 (BE)** ER 形式 [コンフィギュレーション](general-electronic-reporting.md#Configuration)を[インポート](er-download-configurations-global-repo.md)します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-122">From the Global repository, [import](er-download-configurations-global-repo.md) the **BLWI format (BE)** ER format [configuration](general-electronic-reporting.md#Configuration) that is called  to your Finance instance by using this application class.</span></span> <span data-ttu-id="0a5ac-123">基準 **BLWI モデル** のコンフィギュレーションは、インポートされた ER 形式のコンフィギュレーションと共に自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-123">The base **BLWI model** configuration is imported automatically with the imported ER format configuration.</span></span>

```x++
    /// <summary>
    /// Runs export via ER solution.
    /// </summary>
    [Microsoft.Dynamics.BusinessPlatform.SharedTypes.InternalUseOnlyAttribute]
    protected void runER()
    {
        const str erParmEmail = 'model/parameters.Email';
        const str erParmFromDate = 'model/parameters.FromDate';
        const str erParmToDate = 'model/parameters.ToDate';
        const str erParmSurveyCode = 'model/parameters.SurveyCode';

        ERModelDefinitionInputParametersAction modelDefinitionInputParametersAction = new ERModelDefinitionInputParametersAction();

        modelDefinitionInputParametersAction.addParameter(erParmEmail, email)
            .addParameter(erParmFromDate, fromDate)
            .addParameter(erParmToDate, toDate)
            .addParameter(erParmSurveyCode, BankPaymBalanceSurvey::find(surveyCodeRecId).SurveyCode);

        ERObjectsFactory::createFormatMappingRunByFormatMappingId(tradeBLWIParameters.ERFormatMappingID, fileName)
            .withFileDestination(fileDestination)
            .withParameter(modelDefinitionInputParametersAction)
            .run();
    }
```

<span data-ttu-id="0a5ac-124">`email`、`fromDate`、および `toDate` 変数は、ER 形式が呼び出される前に ER ダイアログ ボックス以外のページに入力された値を格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-124">The `email`, `fromDate`, and `toDate` variables are used to store values that have been entered on other pages other than the ER dialog box before an ER format has been called.</span></span> <span data-ttu-id="0a5ac-125">このクラスの `runER()` メソッドは、これらの変数を使用して複数のデータ ソースの値を開始する ER 形式のマッピングを[実行](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export)します。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-125">The `runER()` method of this class [runs](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) an ER format mapping that uses these variables to initiate values of several data sources.</span></span> <span data-ttu-id="0a5ac-126">このようなデータ ソースのすべてのパスの接頭語 (サンプル コードの `erParmEmail`、`erParmFromDate`、または `erParmToDate` 定数など) は、*モデル* タイプ (**モデル** 値) の形式データ ソースの名前として定義されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-126">The prefix of every path of such a data source (such as `erParmEmail`, `erParmFromDate`, or `erParmToDate` constants in the sample code) is defined as the name of a format data source of the *Model* type (**model** value).</span></span>

![「モデル」 データ ソースを含む「BLWI 形式 (BE)」 コンフィギュレーションのデータ ソースの一覧を示す ER 形式デザイナー](./media/er-initiate-uip-data-source-value-from-source-code-1.png)

<span data-ttu-id="0a5ac-128">このようなデータ ソースのすべてのパスの接尾語は、実行時に使用されるモデル マッピングの関連データ ソースへのパスとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-128">The suffix of every path of such a data source is defined as the path to the relevant data source of a model mapping that is used at runtime.</span></span> <span data-ttu-id="0a5ac-129">サンプル コードでは、`parameters.Email`、`parameters.FromDate`、または `parameters.ToDate` を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-129">In the sample code, this can include `parameters.Email`, `parameters.FromDate`, or `parameters.ToDate`.</span></span>

![「ユーザー入力パラメーター」 タイプのデータ ソースを含む「BLWI モデル マッピング」 コンフィギュレーションのデータ ソースの一覧を示す ER モデル マッピング デザイナー](./media/er-initiate-uip-data-source-value-from-source-code-2.png)

## <a name="format-components-for-inbound-electronic-documents"></a><span data-ttu-id="0a5ac-131">受信電子ドキュメントの形式のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="0a5ac-131">Format components for inbound electronic documents</span></span>

<span data-ttu-id="0a5ac-132">受信ドキュメントを解析して、アプリケーション データを更新するために[実行](general-electronic-reporting.md#FormatComponentInbound)できる ER [形式](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import)を構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-132">You can also configure an ER [format](general-electronic-reporting.md#FormatComponentInbound) that can be [run](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) to parse an inbound document and update application data.</span></span> <span data-ttu-id="0a5ac-133">この形式には、受信ドキュメントのコンテンツに基づいてアプリケーション データを更新するために使用される *宛先* タイプのモデル マッピングを参照する形式マッピングが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-133">This format must contain a format mapping that refers to a model mapping of the *To destination* type that is used to update application data based on the content of an inbound document.</span></span> <span data-ttu-id="0a5ac-134">このタイプのモデル マッピングでは、*ユーザー入力パラメーター* タイプのデータ ソースを使用して、実行時に ER ユーザー ダイアログ ボックスから値を取得し、アプリケーション データの更新に使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-134">In this type of model mapping, you can also use data sources of the *User input parameter* type to get values at runtime from the ER user dialog box and then use them for application data update.</span></span>

<span data-ttu-id="0a5ac-135">受信ドキュメントを解析するために ER 形式が実行される場合、`ERObjectsFactory` クラスの `createMappingDestinationRunByImportFormatMappingId()` メソッドの `_showPromptDialog` パラメーターを使用して、ER ダイアログ ボックスをプログラムでオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-135">When an ER format is executed to parse an inbound document, the ER dialog box can be programmatically turned off by using the `_showPromptDialog` parameter of the `createMappingDestinationRunByImportFormatMappingId()` method of the `ERObjectsFactory` class.</span></span>

<span data-ttu-id="0a5ac-136">受信ドキュメントを解析するようにコンフィギュレーションされている ER 形式の場合、ER データ ソースへのパスは、実行中の ER 形式から呼び出されてアプリケーション データを更新する *宛先* タイプのモデル マッピングに存在する *ユーザー入力パラメーター* タイプのデータ ソースへのパスとして構築されます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-136">For ER formats that are configured to parse an inbound document, the path to an ER data source is constructed as the path to a data source of the *User input parameter* type that resides in a model mapping of the *To destination* type that is called from the running ER format to update application data.</span></span>

<span data-ttu-id="0a5ac-137">詳細については、例として使用できる `BankStatementImportBatch` アプリケーション クラスのソース コードを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-137">For more information, review the source code of the `BankStatementImportBatch` application class that can be used as an example.</span></span>

```xpp
        var integrationPoint = classStr(ERTableDestination) + '#' + tableStr(BankStatementDocumentEntity);
        ERmodelDefinitionInputParametersAction inputParameters = new ERmodelDefinitionInputParametersAction();
        inputParameters.addParameter('$ExecutionID', _executionID)
            .addParameter('$gerConfigName', _gerConfigName)
            .addParameter('$AccountId', bankAccount);

        var runner = ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId(_erModelMappingId, integrationPoint);
        runner.withParameter(inputParameters);
        runner.init();
        
        if (runner.promptsContractedModelMapping())
        {
            var parameters = runner.getParameters();
            var traverser = new ERModelDefinitionParametersTraverser(parameters);
            while (traverser.moveNext())
            {
                ERIImportFormatDataSourceContract current = ERCast::asObject(traverser.current()) as ERImportFormatDataSourceContract;
                if (current)
                {
                    current.parmInputDataStream(File::UseFileFromURL(DMFStagingWriter::getDownloadURLFromFileId(_uploadedStatement)));
                }
            }
        }

        runner.runUnattended();
```

<span data-ttu-id="0a5ac-138">`$ExecutionID`、`$gerConfigName`、および `$AccountId` データ ソースの値を開始するために使用される `_executionID`、`_gerConfigName`、および `bankAccount` 変数に注意してください。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-138">Pay attention to the `_executionID`, `_gerConfigName`, and `bankAccount` variables that are used to initiate the values of the `$ExecutionID`, `$gerConfigName`, and `$AccountId` data sources.</span></span>

<span data-ttu-id="0a5ac-139">グローバル リポジトリから、このアプリケーション クラスを使用して Finance インスタンスに呼び出される **Camt.053 形式** の ER 形式 コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-139">From the Global repository, import the **Camt.053 Format** ER format configuration that is called by using this application class to your Finance instance.</span></span> <span data-ttu-id="0a5ac-140">**口座取引明細書モデル** のコンフィギュレーションは、インポートされた ER 形式のコンフィギュレーションと共に自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-140">The **Bank statement model** configuration is imported automatically with the imported ER format configuration.</span></span> <span data-ttu-id="0a5ac-141">さらに、アプリケーション データの更新に使用するモデル マッピングを含む **口座取引明細書のマッピング先** ER コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-141">Additionally, import the **Bank statement mapping to destination** ER configuration that contains a model mapping using to update application data.</span></span>

![「ユーザー入力パラメーター」 タイプのデータ ソースを含む「口座取引明細書のマッピング先」コンフィギュレーションのデータ ソースの一覧を示す ER モデル マッピング デザイナー](./media/er-initiate-uip-data-source-value-from-source-code-3.png)

## <a name="limitations"></a><span data-ttu-id="0a5ac-143">制限</span><span class="sxs-lookup"><span data-stu-id="0a5ac-143">Limitations</span></span>
<span data-ttu-id="0a5ac-144">実行時に使用される ER モデル マッピングでコンフィギュレーションされた *ユーザー入力パラメーター* タイプのデータ ソース値のみを開始できます。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-144">You can only initiate data source values of the *User input parameter* type that are configured in an ER model mapping that is used at runtime.</span></span> <span data-ttu-id="0a5ac-145">ER 形式でコンフィギュレーションされた *ユーザー入力パラメーター* タイプのデータ ソース値は、ソース コードから開始できません。</span><span class="sxs-lookup"><span data-stu-id="0a5ac-145">The data source values of the *User input parameter* type that are configured in an ER format can't be initiated from the source code.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a5ac-146">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0a5ac-146">Additional resources</span></span>

[<span data-ttu-id="0a5ac-147">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="0a5ac-147">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="0a5ac-148">受信したドキュメントを解析する</span><span class="sxs-lookup"><span data-stu-id="0a5ac-148">Parse incoming documents</span></span>](er-parse-incoming-documents.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]