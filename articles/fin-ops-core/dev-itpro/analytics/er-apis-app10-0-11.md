---
title: Application update 10.0.11 での電子申告フレームワーク API の変更
description: このトピックでは、Microsoft Dynamics 365 Finance バージョン10.0.11 で電子申告フレームワーク の API がどのように変更されたのかについて説明します。
author: NickSelin
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: f0e5a27cb53904f87e0c8c27b354550688784592
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751196"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10011"></a>Application update 10.0.11 での電子申告フレームワーク API の変更

[!include [banner](../includes/banner.md)]

このトピックでは、電子申告（ER）フレームワークのアプリケーション プログラミング インターフェース（API）が、Microsoft Dynamics 365 Finance  バージョン10.0.11でどのように変更されたかについて説明します。

## <a name="api-to-run-a-format-mapping-for-the-generation-of-outbound-documents"></a>送信ドキュメントの生成に対して形式マッピングを実行する API

[送信ドキュメント](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) を生成するには、ER  [形式マッピング](general-electronic-reporting.md#FormatComponentInbound) を実行する必要があります。 ほとんどの ER 形式のマッピングには、**データ モデル** 型のデータ ソースが含まれています。 実行時には、特定の [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)が、データソースが設定されている [データモデル](general-electronic-reporting.md#data-model-and-model-mapping-components) の実装として識別される必要があります。

ER フレームワークの [初期](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) API を使用してソースコードの実行ポイントから ER 形式のマッピングを呼び出すと、モデル マッピング コンポーネントを含む、対応する ER [構成](general-electronic-reporting.md#Configuration)の設定（既定のモデルマッピング フラグと国/地域コード）を考慮したモデル マッピングが見つかります。 詳細については、[国のコンテキスト依存 ER モデル マッピングを構成する](er-country-dependent-model-mapping.md) を参照してください。

場合によっては、X++ コードの特定の場所から ER 形式のマッピングが呼び出された場合、最も適切なモデル マッピングを検索するための追加の基準を指定する必要があります。 たとえば、ER 形式マッピングは、2 つのモデル マッピングを持つデータ モデルを使用して設定されています。 最初のモデルマッピングは、現在使用可能なすべての実行ポイントから、この ER 形式のマッピングを呼び出すたびに円滑に実行されるようにするため、既定のモデルマッピングとしてマークされています。 X + + では、この ER 形式マッピングを呼び出す新たな実行ポイントを実装します。 この方法では、この呼び出しの他の条件（指定された引数や現在のアプリケーション インスタンスの利用可能なリソースなど）によって、そのモデルマッピングの方がより良いパフォーマンスを発揮すると判断されるため、データモデルに2番目のモデルマッピングを使用するように強制します。

この設定を完了するには、統合ポイントを使用してモデル マッピングを構成します。 **データソース** ウィンドウでは、この統合ポイントのコンポーネントとして、モデル マッピングの単一のデータソースを選択できます。 続いて **編集** を選択して、このデータ ソースのプロパティを変更します。

![編集を選択して、このデータ ソースのプロパティを変更します。](./media/er-api-ds-integration-point1.png)

**データソースのプロパティ** ダイアログ ボックスで、**統合ポイント** オプションを **はい** に設定すると、データソースを統合ポイントのコンポーネントとしてマークできます。

![統合ポイント オプションの設定](./media/er-api-ds-integration-point2.png)

ER フレームワークの新しい API を使用して ER 形式のマッピングを呼び出し、特定の統合ポイントを含むように設定されたモデル マッピングを強制的に使用することができます。 次の例では、この新しい API の使用方法を解説します。

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
using Microsoft.Dynamics365.LocalizationFramework.XppSupportLayer;

class ERIntegrationPointCodeSamples extends RunBaseBatch
{
    private ERFormatMappingId formatMappingId;

    public void run()
    {
        var runner = ERObjectsFactory::createFormatMappingRunByFormatMappingId(this.formatMappingId, 'OutboundFileName', true);
        var integration_point = new ERIntegrationPointFactory().WithObjectIntegrationPoint('SalesInvoiceDP').ToIntegrationPoint();
        /// new ERIntegrationPointFactory().WithTableRecordsIntegrationPoint(tableName)
        /// new ERIntegrationPointFactory().WithTableIntegrationPoint(tableName)
        /// new ERIntegrationPointFactory().WithObjectIntegrationPoint(className)
        /// new ERIntegrationPointFactory().WithClassIntegrationPoint(className)
        runner.withIntegrationPoint(integration_point).run();
    }
}
```

> [!NOTE]
> - モデルマッピング統合ポイントのコンポーネントとしてマークできるのは、**テーブル レコード**、**テーブル**、**クラス**、**オブジェクト** タイプのデータソースのみです。
> - 現在、モデルマッピング統合ポイントの構成要素として使用できるデータ ソースは単一のものに限られています。
> - その他の既存の基準に加えて、統合ポイントは最適なモデル マッピングの選択時に考慮されます。
> - 実行時に、実行中の ER 形式のマッピングに適用可能なモデル マッピングの中から、要求された統合ポイントを持つモデル マッピングが複数検出された場合は、エラーが発生します。

## <a name="api-to-show-a-format-mapping-lookup"></a>フォーマット マッピング ルックアップを表示する API

ER フレームワークの [初期](er-apis-app73.md#code-to-display-a-format-mapping-lookup)の API は、ER 形式のマッピングを検索するために使用されます。 データ モデル名とコンテナー名をテキスト定数として使用します。 このルックアップでは、以下すべての条件を満たす one data model の ER 形式マッピングのみを提供しています：

- この名前は指定されています。
- その基準は ER 構成リストで最初に満たされています。

ER フレームワークの新しい API により、構成された統合ポイントを使用して同じルックアップを実装することができます。 このルックアップは、指定された統合ポイントを持つモデル マッピングが利用可能な **データモデル** タイプのデータソースを含むすべての ER 形式のマッピングを提供します。 このルックアップで提供される ER 形式のマッピングは、データソースとして異なるモデル マッピングを使用することができます。

次の例では、この新しい API の使用方法を解説します。

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
using Microsoft.Dynamics365.LocalizationFramework.XppSupportLayer;

class ERIntegrationPointCodeSamples extends RunBaseBatch
{
    private ERFormatMappingId formatMappingId;

    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        var integration_point = new ERIntegrationPointFactory().WithIntegrationPointKey('SalesInvoiceDP').ToIntegrationPoint();
        ERObjectsFactory::createFormatMappingTableLookupForIntegrationPoint(
            integration_point,
            _referenceGroupControl
            ).performFormLookup();
    }
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]