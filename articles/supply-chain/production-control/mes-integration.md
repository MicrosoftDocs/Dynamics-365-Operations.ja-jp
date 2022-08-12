---
title: サード パーティ製造システムとの統合
description: この記事では、Microsoft Dynamics 365 Supply Chain Management をサード パーティの製造実行システム (MES) と統合する方法について説明します。
author: johanhoffmann
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 46f6db3dd9942131b379216e6fffe5551d6c8fc3
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068034"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>サード パーティ製造システムとの統合

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management を使用する一部の製造組織は、Dynamics 365 のネイティブ機能を使用して機械、設備、人員の製造活動を管理します。 ただし、他の製造組織、特に高度な製造要件を持つ組織では、サード パーティの製造実行システム (MES) が使用されます。 たとえば、組織が業種に特化したサード パーティの MES ソリューションを選択する場合があります。

統合ソリューションでは、データ交換が完全に自動化され、ほぼリアルタイムで行われます。 したがって、データは両方のシステムで最新の状態に維持され、手動でデータを入力する必要はありません。 たとえば、材料消費を MES に登録すると、統合によって Dynamics 365 にも同じ消費が登録されます。 したがって、最新の在庫レコードは、計画や販売など、他の重要なプロセスで使用できます。

Supply Chain Management のユーザーは、このソリューションをより速く、簡単に、および安く、サード パーティの MES と統合することができます。 次の機能を提供します:

- [主要な製造実行プロセス](#processes-available-for-mes-integration)をサポートするビジネス イベントおよびインターフェイス
- イベント処理履歴を追跡し、失敗したプロセスのトラブルシューティングと修正を行う集中型ダッシュボード

次の図は、統合ソリューションで交換されるビジネス イベント、プロセス、およびメッセージの一般的なコレクションを示しています。

![典型的な統合シナリオ。](media/3p-mes-scenario.png "典型的な統合シナリオ。")

## <a name="turn-on-the-mes-integration-feature"></a>MES 統合フィーチャーを有効にする

次の手順で説明されている通り、この機能を使用する前に、管理者はシステムでこれらの機能を有効にする必要があります。

1. **システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。
1. **時間/出席** ライセンス キーが有効になっている (チェック マークが表示されている) 必要があります。 このライセンス キーは、製造実行システムの機能とデータを制御するため必要です。 無効にした場合は、次の手順を実行します。
    1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。
    1. **ライセンス コンフィギュレーション** ページで 、**時間と出勤** チェック ボックスを オンにします。
    1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします
1. **システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。
1. 次の方法で一覧表示されている機能を有効にします ([機能管理概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) も参照してください):
    - **モジュール:** *生産制御*
    - **フィーチャー名:** *製造実行システム統合*

## <a name="processes-available-for-mes-integration"></a>MES 統合で使用できるプロセス

次のプロセスのすべてまたは一部を統合に対して有効にできます。

| プロセス名 | Description |
|---|---|
| 製造オーダーのリリースと製造オーダーのステータス変更に関するビジネス イベント | このプロセスは、MES がリッスンして生産する必要がある製造オーダーに関する情報を得るビジネス イベントを提供します。 製造オーダーに関連する参照データは、Open Data Protocol (OData) エンティティまたはデータ エンティティを通じて Supply Chain Management から MES に共有される予定です。 |
| 製造オーダーの開始 | このプロセスにより、MES を使用して開始される製造オーダーに関する情報が Supply Chain Management に提供されます。 これにより、両方のシステムですべての製造活動を最新ビューで確認できます。 |
| 生産済みまたは仕損済み数量のレポート | このプロセスにより、MES を使用して製造ジョブでレポートされる完成品とエラー数量のレポートに関する情報が Supply Chain Management に提供されます。 これにより、作業現場監督が生産計画の進捗状況を最新のビューで確認できます。 |
| 原材料消費のレポート | このプロセスにより、消費される材料の数量に関する MES からの情報が Supply Chain Management に提供されます。 計画や販売など、他の重要なプロセスで使用できる最新の在庫レコードを構成します。 |
| 工程にかかる時間のレポート | このプロセスにより、特定の工程で使用された時間に関する情報が Supply Chain Management に提供されます。 |
| 製造オーダーの終了 | このプロセスは、MES によって製造オーダーが *終了* ステータスに更新された時点で Supply Chain Management に通知されます。 このステータスは、製造オーダーでこれ以上数量が生産されない状態を示します。 |

## <a name="monitor-incoming-messages"></a>受信メッセージの監視

システムへの着信メッセージを監視するには、**製造実行システム統合** ページを開きます。 このページでは、問題を表示、処理、およびトラブルシューティングできます。

特定の製造オーダーのすべてのメッセージは、受信した順番に処理されます。 ただし、バッチ ジョブが並行して処理されるため、他の製造オーダーに対するメッセージは、受信した順番に処理されない場合があります。 エラーが発生した場合、状態を *失敗* に設定する前に、バッチ ジョブは各メッセージの処理を 3 回試みます。

## <a name="call-the-api"></a>API の呼び出し

MES 統合 API を呼び出す場合は、次のエンドポイント URL に `POST` 要求を送信します。

`/api/services/SysMessageServices/SysMessageService/SendMessage`

送信する要求の本文は、次の例のようになります。 必要に応じて、`_companyId`、`_messageType` および `_messageContent` の値を置換します。 API がサポートする各種のメッセージ タイプ、およびそれらのコンテンツのデザイン方法については、次のセクションを参照してください。

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API メッセージ タイプとコンテンツ

ここでは、MES 統合 API を通じて交換できるメッセージの各タイプについて説明します。

### <a name="start-production-order-message"></a>製造オーダー メッセージの開始

*製造オーダーの開始* メッセージの場合、`_messageType` 値は `ProdProductionOrderStart` です。 次の表に、このメッセージがサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `ProductionOrderNumber` | 必須 | 文字列 |
| `StartedQuantity` | オプション | 実績 |
| `StartedDate` | オプション | 日付 |
| `AutomaticBOMConsumptionRule` | オプション | 列挙 (FlushingPrincip \| Always \| Never) |

### <a name="report-as-finished-message"></a>[完了レポート] メッセージ

*完了レポート* メッセージの場合、`_messageType` 値は `ProdProductionOrderReportFinished` です。 次の表に、このメッセージがサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `ProductionOrderNumber` | 必須 | 文字列 |
| `ReportFinishedLines` | 必須 | 行 (少なくとも 1 つ) の一覧。各行には、次の表で説明されているペイロード データが含まれています |

次の表に、`ProdProductionOrderReportFinished` メッセージの `ReportFinishedLines` セクションの各行がサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `LineNumber` | オプション | 実績 |
| `ItemNumber` | オプション | 文字列|
| `ProductionType` | オプション | 列挙 (MainItem \| Formula \| BOM \| Co_Product \| By_Product \| None)、拡張可能 |
| `ReportedErrorQuantity` | オプション | 実績|
| `ReportedGoodQuantity` | オプション | 実績|
| `ReportedErrorCatchWeightQuantity` | オプション | 実績 |
| `ReportedGoodCatchWeightQuantity` | オプション | 実績 |
| `AcceptError` | オプション | 列挙 (はい \| いいえ) |
| `ErrorCause` | オプション | 列挙 (None \| Material \| Machine \| OperatingStaff)、拡張可能 |
| `ExecutedDateTime` | オプション | DateTime |
| `ReportAsFinishedDate` | オプション | 日付 |
| `AutomaticBOMConsumptionRule` | オプション | 列挙 (FlushingPrincip \| Always \| Never) |
| `AutomaticRouteConsumptionRule` | オプション |列挙 (RouteDependent \| Always \| Never) |
| `RespectFlushingPrincipleDuringOverproduction` | オプション | 列挙 (はい \| いいえ) |
| `ProductionJournalNameId` | オプション | 文字列 |
| `PickingListProductionJournalNameId` | オプション | 文字列|
| `RouteCardProductionJournalNameId` | オプション | 文字列 |
| `FromOperationNumber` | オプション | 整数|
| `ToOperationNumber` | オプション | 整数|
| `InventoryLotId` | オプション | 文字列 |
| `BaseValue` | オプション | 文字列 |
| `EndJob` | オプション | 列挙 (はい \| いいえ) |
| `EndPickingList` | オプション | 列挙 (はい \| いいえ) |
| `EndRouteCard` | オプション | 列挙 (はい \| いいえ) |
| `PostNow` | オプション | 列挙 (はい \| いいえ) |
| `AutoUpdate` | オプション | 列挙 (はい \| いいえ) |
| `ProductColorId` | オプション | 文字列|
| `ProductConfigurationId` | オプション | 文字列 |
| `ProductSizeId` | オプション | 文字列 |
| `ProductStyleId` | オプション | 文字列 |
| `ProductVersionId` | オプション | 文字列 |
| `ItemBatchNumber` | オプション | 文字列 |
| `ProductSerialNumber` | オプション | 文字列 |
| `LicensePlateNumber` | オプション | 文字列 |
| `InventoryStatusId` | オプション | 文字列 |
| `ProductionWarehouseId` | オプション | 文字列 |
| `ProductionSiteId` | オプション | 文字列 |
| `ProductionWarehouseLocationId` | オプション | 文字列 |
| `InventoryDimension1` から `InventoryDimension12` | オプション | 文字列 |

12 の拡張可能な分析コード (`InventoryDimension1`～`InventoryDimension12`) は、カスタマイズが必要であり、常に使用されるとは限りません。 詳細については、[拡張機能を通じた新しい在庫分析コードの追加](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md)を参照してください。

### <a name="material-consumption-picking-list-message"></a>材料消費 (ピッキング リスト) メッセージ

*材料消費 (ピッキング リスト)* メッセージの場合、`_messageType` 値は `ProdProductionOrderPickingList` です。 次の表に、このメッセージがサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `ProductionOrderNumber` | 必須 | 文字列 |
| `JournalNameId` | オプション | 文字列 |
| `PickingListLines` | 必須 | 行 (少なくとも 1 つ) の一覧。各行には、次の表で説明されているペイロード データが含まれています |

次の表に、`ProdProductionOrderPickingList` メッセージの `PickingListLines` セクションの各行がサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `ItemNumber` | 必須 | 文字列 |
| `ConsumptionBOMQuantity` | オプション | 実績 |
| `ProposalBOMQuantity` | オプション | 実績 |
| `ScrapBOMQuantity` | オプション | 実績 |
| `BOMUnitSymbol` | オプション | 文字列 |
| `ConsumptionInventoryQuantity` | オプション | 実績 |
| `ProposalInventoryQuantity` | オプション | 実績 |
| `ConsumptionCatchWeightQuantity` | オプション | 実績 |
| `ProposalCatchWeightQuantity` | オプション | 実績 |
| `ConsumptionDate` | オプション | 日付 |
| `OperationNumber` | オプション | 整数 |
| `LineNumber` | オプション | 実績 |
| `PositionNumber` | オプション | 文字列 |
| `IsConsumptionEnded` | オプション | 列挙 (はい \| いいえ) |
| `ErrorCause` | オプション | 列挙 (None \| Material \| Machine \| OperatingStaff)、拡張可能 |
| `InventoryLotId` | オプション | 文字列 |

### <a name="time-used-for-operation-route-card-message"></a>工程に使用される時間 (ルート カード) メッセージ

*工程に使用される時間 (ルート カード)* メッセージの場合、`_messageType` の値は `ProdProductionOrderRouteCard` です。 次の表に、このメッセージがサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `ProductionOrderNumber` | 必須 | 文字列 |
| `JournalNameId` | オプション | 文字列 |
| `RouteCardLines` | 必須 | 行 (少なくとも 1 つ) の一覧。各行には、次の表で説明されているペイロード データが含まれています |

次の表に、`ProdProductionOrderRouteCard` メッセージの `RouteCardLines` セクションの各行がサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `OperationNumber` | 必須 | 整数 |
| `OperationPriority` | オプション | 列挙 (Primary \| Secondary1 \| Secondary2 \| ... \| Secondary20) |
| `OperationId` | オプション | 文字列 |
| `OperationsResourceId` | オプション | 文字列 |
| `Worker` | オプション | 文字列 |
| `HoursRouteCostCategoryId` | オプション | 文字列 |
| `QuantityRouteCostCategoryId` | オプション | 文字列 |
| `HourlyRate` | オプション | 実績 |
| `Hours` | オプション | 実績 |
| `GoodQuantity` | オプション | 実績 |
| `ErrorQuantity` | オプション | 実績 |
| `CatchWeightGoodQuantity` | オプション | 実績 |
| `CatchWeightErrorQuantity` | オプション | 実績 |
| `QuantityPrice` | オプション | 実績 |
| `ProcessingPercentage` | オプション | 実績 |
| `ConsumptionDate` | オプション | 日付 |
| `TaskType` | オプション | 列挙 (QueueBefore \| Setup \| Process \| Overlap \| Transport \| QueueAfter \| Burden) |
| `ErrorCause` | オプション | 列挙 (None \| Material \| Machine \| OperatingStaff)、拡張可能 |
| `OperationCompleted` | オプション | 列挙 (はい \| いいえ) |
| `BOMConsumption` | オプション | 列挙 (はい \| いいえ) |
| `ReportAsFinished` | オプション | 列挙 (はい \| いいえ) |

### <a name="end-production-order-message"></a>製造オーダー メッセージの終了

*製造オーダーの終了* メッセージの場合、`_messageType` 値は `ProdProductionOrderEnd` です。 次の表に、このメッセージがサポートするフィールドを示します。

| フィールド名 | Status | 種類 |
|---|---|---|
| `ProductionOrderNumber` | 必須 | 文字列 |
| `ExecutedDateTime` | オプション | DateTime |
| `EndedDate` | オプション | 日付 |
| `UseTimeAndAttendanceCost` | オプション | 列挙 (はい \| いいえ) |
| `AutoReportAsFinished` | オプション | 列挙 (はい \| いいえ) |
| `AutoUpdate` | オプション | 列挙 (はい \| いいえ) |

## <a name="other-production-information"></a>その他の製造情報

メッセージは、作業現場で発生するアクションやイベントをサポートします。 メッセージは、この記事で説明する MES 統合フレームワークを使用して処理されます。 この設計では、MES と共有する他の参照情報 (製品関連情報や、特定の製造オーダーで使用され、特定の設定および構成時間を含む部品表またはルートなど) は、ファイル転送または OData で [データ エンティティ](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#data-entities) を使用してシステムから取得されます。

## <a name="receive-feedback-about-the-state-of-a-message"></a>メッセージの状態に関するフィードバックの受信

MES から Supply Chain Management にメッセージが送信された後に、そのメッセージの状態に関するフィードバックを Supply Chain Management から返すのが有用な場合があります。 次の例では、このビヘイビアーが関連するケースの例を示します。

- MES 統合の監督を担当する担当者はいません。
- MES 統合の監督を担当する担当者は、メッセージが失敗したときに、対処が必要であることがわかるよう、電子メールで通知を受け取りたいと思っています。
- 現場のオペレーターまたは IT 部門の担当者がアクションを行う必要がある場合は、MES にエラー メッセージを表示する必要があります。
- MES は、エラー メッセージ (製造オーダーの開始に失敗したなど) が表示された後に注文スケジュールを再計算する必要があります。

そのような場合は、Supply Chain Management の標準警告機能を活用できます。 標準警告のしくみについては、次のリソースを参照してください。

- ヘルプ記事: [警告の概要](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- ビデオ : [財務と運用の警告ルール オプション](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

たとえば、メッセージの状態に関するフィードバックを提供するために、次の警告を設定できます。

- メッセージが *失敗* した場合に使用されるビジネス イベント (「外部送信」) を作成します。
- IT 管理者または生産現場マネージャに通知と電子メールを送信します。

