---
title: ソース コードからユーザー入力パラメーターのデータ ソース値を開始する
description: このトピックでは、ソース コードからユーザー入力パラメーター タイプのデータ ソース値を開始する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: f9a13c131908fd02a8bfeee9253d131a56248f32
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686702"
---
# <a name="initiate-data-source-values-of-the-user-input-parameter-type-from-source-code"></a>ソース コードからユーザー入力パラメーターのデータ ソース値を開始する

[!include [banner](../includes/banner.md)]

ER [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)および ER [形式](general-electronic-reporting.md#FormatComponentOutbound)コンポーネントを設計する場合は、*ユーザー入力パラメーター* タイプを使用して、ER フォーマットの実行が開始される前に実行時に提供される必要な値を取得します。 このダイアログ ボックスは、必要なパラメーターを別のページに入力した場合、または ER フォーマットを無人 (バッチ) モードで実行した場合に、プログラムを使用してオフにすることができます。 ER ダイアログ ボックスがオフになっている場合、ソース コードから *ユーザー入力パラメーター* タイプのデータ ソース値を開始する必要があります。

## <a name="format-components-for-outgoing-electronic-documents"></a>送信する電子ドキュメントの形式のコンポーネント

送信ドキュメントを生成するには、ER [形式](general-electronic-reporting.md#FormatComponentOutbound)をコンフィギュレーションします。 この形式をコンフィギュレーションすると、送信ドキュメントに入力するために使用されるデータ ソースとして ER [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components)が選択されます。 ER [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)をコンフィギュレーションして、選択したデータ モデルが実行時にアプリケーション データによってどのように入力されるかを指定します。 モデル マッピングを設計するときは、データ ソースを指定して、さまざまなソースから目的の値を収集しし、それらをデータ モデルに入力します。 特に、*ユーザー入力パラメーター* タイプのデータ ソースを使用して、ER 形式を最初に[実行](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export)したときに表示される ER ユーザー ダイアログ ボックスでユーザーが入力した値をデータ モデルに入力できます。 

送信ドキュメントを生成するようにコンフィギュレーションされた ER 形式の場合、`ERObjectsFactory` クラスの `createFormatMappingRunByFormatMappingId()` メソッドの `_showPromptDialog` パラメーターを使用して、ER ダイアログ ボックスをプログラムでオフにすることができます。 この場合、ソースコードから *ユーザー入力パラメーター* タイプのデータ ソースの値を開始する必要があります。 それには、次のパターンを使用します。

```xpp
ERModelDefinitionInputParametersAction Obj = new ERModelDefinitionInputParametersAction();
Obj.addParameter(<path to an ER data source>, <data source value>);
ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingID, fileName, false)
            .withParameter(Obj)
            .run();
```

送信ドキュメントを生成するようにコンフィギュレーションされている ER フォーマットの場合、ER データ ソースへのパスは、スラッシュ (**/**) 文字で区切られた接頭語と接尾語から構成されます。 接頭語は、実行中の ER 形式に存在する *モデル* タイプのデータ ソースの名前を表します。 接尾語は、関連する [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components)の実装として実行中の ER 形式で使用される [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)に存在する *ユーザー入力パラメーター* タイプのデータ ソースへのパスを表します。

> [!TIP]
> データ ソース パスのノードは、スラッシュ (**/**) 文字で区切られ ます。 `ERPath::Combine()` メソッドを使用して、パスを作成します。

詳細については、例として使用できる `BankPaymBalanceXML` アプリケーション クラスのソース コードを確認してください。 グローバル リポジトリから、このアプリケーション クラスを使用して Finance インスタンスに呼び出される **BLWI 形式 (BE)** ER 形式 [コンフィギュレーション](general-electronic-reporting.md#Configuration)を[インポート](er-download-configurations-global-repo.md)します。 基準 **BLWI モデル** のコンフィギュレーションは、インポートされた ER 形式のコンフィギュレーションと共に自動的にインポートされます。

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

`email`、`fromDate`、および `toDate` 変数は、ER 形式が呼び出される前に ER ダイアログ ボックス以外のページに入力された値を格納するために使用されます。 このクラスの `runER()` メソッドは、これらの変数を使用して複数のデータ ソースの値を開始する ER 形式のマッピングを[実行](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export)します。 このようなデータ ソースのすべてのパスの接頭語 (サンプル コードの `erParmEmail`、`erParmFromDate`、または `erParmToDate` 定数など) は、*モデル* タイプ (**モデル** 値) の形式データ ソースの名前として定義されます。

![「モデル」 データ ソースを含む「BLWI 形式 (BE)」 コンフィギュレーションのデータ ソースの一覧を示す ER 形式デザイナー](./media/er-initiate-uip-data-source-value-from-source-code-1.png)

このようなデータ ソースのすべてのパスの接尾語は、実行時に使用されるモデル マッピングの関連データ ソースへのパスとして定義されます。 サンプル コードでは、`parameters.Email`、`parameters.FromDate`、または `parameters.ToDate` を含めることができます。

![「ユーザー入力パラメーター」 タイプのデータ ソースを含む「BLWI モデル マッピング」 コンフィギュレーションのデータ ソースの一覧を示す ER モデル マッピング デザイナー](./media/er-initiate-uip-data-source-value-from-source-code-2.png)

## <a name="format-components-for-inbound-electronic-documents"></a>受信電子ドキュメントの形式のコンポーネント

受信ドキュメントを解析して、アプリケーション データを更新するために[実行](general-electronic-reporting.md#FormatComponentInbound)できる ER [形式](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import)を構成することもできます。 この形式には、受信ドキュメントのコンテンツに基づいてアプリケーション データを更新するために使用される *宛先* タイプのモデル マッピングを参照する形式マッピングが含まれている必要があります。 このタイプのモデル マッピングでは、*ユーザー入力パラメーター* タイプのデータ ソースを使用して、実行時に ER ユーザー ダイアログ ボックスから値を取得し、アプリケーション データの更新に使用することもできます。

受信ドキュメントを解析するために ER 形式が実行される場合、`ERObjectsFactory` クラスの `createMappingDestinationRunByImportFormatMappingId()` メソッドの `_showPromptDialog` パラメーターを使用して、ER ダイアログ ボックスをプログラムでオフにすることができます。

受信ドキュメントを解析するようにコンフィギュレーションされている ER 形式の場合、ER データ ソースへのパスは、実行中の ER 形式から呼び出されてアプリケーション データを更新する *宛先* タイプのモデル マッピングに存在する *ユーザー入力パラメーター* タイプのデータ ソースへのパスとして構築されます。

詳細については、例として使用できる `BankStatementImportBatch` アプリケーション クラスのソース コードを確認してください。

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

`$ExecutionID`、`$gerConfigName`、および `$AccountId` データ ソースの値を開始するために使用される `_executionID`、`_gerConfigName`、および `bankAccount` 変数に注意してください。

グローバル リポジトリから、このアプリケーション クラスを使用して Finance インスタンスに呼び出される **Camt.053 形式** の ER 形式 コンフィギュレーションをインポートします。 **口座取引明細書モデル** のコンフィギュレーションは、インポートされた ER 形式のコンフィギュレーションと共に自動的にインポートされます。 さらに、アプリケーション データの更新に使用するモデル マッピングを含む **口座取引明細書のマッピング先** ER コンフィギュレーションをインポートします。

![「ユーザー入力パラメーター」 タイプのデータ ソースを含む「口座取引明細書のマッピング先」コンフィギュレーションのデータ ソースの一覧を示す ER モデル マッピング デザイナー](./media/er-initiate-uip-data-source-value-from-source-code-3.png)

## <a name="limitations"></a>制限
実行時に使用される ER モデル マッピングでコンフィギュレーションされた *ユーザー入力パラメーター* タイプのデータ ソース値のみを開始できます。 ER 形式でコンフィギュレーションされた *ユーザー入力パラメーター* タイプのデータ ソース値は、ソース コードから開始できません。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[受信したドキュメントを解析する](er-parse-incoming-documents.md)
