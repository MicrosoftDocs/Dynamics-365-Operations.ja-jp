---
title: テーブル マップの正常性チェックのエラー コード
description: この記事では、テーブル マップの正常性チェックのエラー コードについて説明します。
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: d3f413f34296fd01da6741bb49658285394cbd17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288763"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>テーブル マップの正常性チェックのエラー コード

[!include [banner](../../includes/banner.md)]



この記事では、テーブル マップの正常性チェックのエラー コードについて説明します。

## <a name="error-100"></a>エラー 100

エラー メッセージは、"財務と運用のレコメンデーションを実行するために最低限必要な財務と運用プラットフォームのバージョンは PU 43 です" になります。

この機能には、財務と運用アプリのバージョン 10.0.19 以降のプラットフォーム更新プログラムが必要です。

## <a name="error-400"></a>エラー 400

エラー メッセージは、"エンティティ \{finance and operations UniqueEntityName\} のビジネス イベント登録データが見つかりません。つまり、マップが実行されていないか、すべてのフィールド マッピングが単一方向であるかのいずれかです。" になります。

## <a name="error-500"></a>エラー 500

エラー メッセージは、"プロジェクト \{project name\} にプロジェクト構成がありません。 これはプロジェクトが有効になっていないか、すべてのフィールド マッピングが Customer Engagement から財務と運用への単一方向である可能性があります。"

テーブル マップのマッピングを確認します。 これらが Customer Engagement アプリから財務と運用アプリへの単一方向の場合、財務と運用アプリから Dataverse への実同期化のトラフィックは生成されません。

## <a name="error-900"></a>エラー 900

このエラー メッセージは、"エンティティ \{finance and operations UniqueEntityName\} のソース フィルター \{sourceFilter\} が無効" です。

財務と運用アプリのテーブル マップで指定されたソース フィルターの構文が正しくありません。 このフィルター基準を検証するには、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps) を参照してください。

## <a name="error-1000"></a>エラー 1000

エラー メッセージは、"二重書き込みライブ同期に使用されるエンティティ \{finance and operations UniqueEntityName\} クエリは \{finance and operations EntityFilterQueryString\} です。 クエリ基準を満たすレコードは、同期のためにピックアップされます。" です。

返されたエンティティ クエリは、エンティティのバッキング SQL クエリです。 ライブ同期のために収集されるビジネス データを決定するクエリに対して、内部結合またはフィルタが適用されたかどうかを確認します。 二重書き込みライブ同期のために取得されるレコードごとに実行する必要がある、内部結合およびフィルターの選択は必須です。

## <a name="error-1300"></a>エラー 1300

エラー メッセージは、"エンティティ \{finance and operations EntityMetadata.EntityProperties.LogicalEntityName\} 向けのバーチャル フィールド \{s.EntityFieldName\} は、二重書き込み向けに追跡できない場合があります。"

財務と運用テーブルからの仮想フィールドは追跡に対して有効になっていません。 ライブ同期ではデータを同期できますが、列に対して行われた変更をピックアップできません。

## <a name="error-1500"></a>エラー 1500

エラーメッセージは、"データソース \{datasource.DataSourceName\} の追跡を可能にするには、非ルックアップ フィールドに少なくとも 1 つのフィールドがマップされている 必要があります。" です。

エンティティからのデータ ソースに、デュアル書き込み用にマップされたフィールドが存在しません。 基になるテーブルに対する変更は、デュアル書き込みでは追跡されません。

## <a name="error-1600"></a>エラー 1600

エラー メッセージは、"データソース: エンティティ \{finance and operations EntityMetadata.EntityProperties.LogicalEntityName\} の \{datasource.DataSourceName\} には範囲があります。 範囲の条件を満たすレコードだけが出荷用に選択されます。" です。

財務と運用アプリのエンティティは、フィルター範囲が有効になっているデータ ソースを使用できます。 これらの範囲により、ライブ同期の一部として取得されるレコードが定義されます。 一部のレコードが財務と運用アプリから Dataverse にスキップされた場合は、そのレコードがエンティティの範囲基準を 満たされているかどうかを確認します。 このチェックを簡単に実行するには、次の例のような SQL クエリを実行します。

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>エラー 1700

エラー メッセージは、"テーブル: エンティティ \{datasourceTable.Key.entityName\} の \{datasourceTable.Key.subscribedTableName\} は、エンティティ \{origTableToEntityMaps.EntityName\} に対して追跡されています。 複数のエンティティについて追跡される同じテーブルが、ライブ同期トランザクションのシステム パフォーマンスに影響する可能性があります。" です。

同じテーブルが複数のエンティティによって追跡される場合、そのテーブルに対する変更により、リンクされたエンティティに対するデュアル 書き込み評価がトリガーされます。 フィルター句は有効なレコードのみを送信しますが、実行時間の長いクエリや最適化されていないクエリ プランがある場合、評価でパフォーマンス上の問題が発生する可能性があります。 この問題は、ビジネスの視点からは避けれない可能性があります。 ただし、複数のエンティティにまたがるテーブルが多い場合は、エンティティ クエリのエンティティの簡略化や、最適化のチェックを検討する必要があります。

## <a name="error-1800"></a>エラー 1800
エラー メッセージは、"Datasource : {} for entity CustCustomerV3Entity には範囲値が含まれます。 Dataverse から財務およびオペレーションへの受信レコードのアップセルは、エンティティの範囲の値によって影響を受ける可能性があります。 フィルター条件に一致しないレコードを持つ Dataverse から財務と運用へのレコード更新をテストして、設定を検証してください。"

財務およびオペレーション アプリケーションでエンティティに範囲が指定されている場合、Dataverse から財務アプリケーションと Operations アプリケーションへの受信同期で、この範囲の基準に一致しないレコードの更新動作をテストする必要があります。 範囲に一致しないレコードは、エンティティによって挿入操作として処理されます。 基になるテーブルに既存のレコードがある場合、挿入は失敗します。 本稼働に配置する前に、すべてのシナリオでこの使用例をテストすることをお勧めします。

## <a name="error-1900"></a>エラー 1900
エラー メッセージは、"Entity: {}にはデータ ソースが指定されています。このデータ ソースは、発信二重書き込みで追跡されません。 これは、ライブ同期のパフォーマンスに影響を与えることがあります。 実行クエリを最適化するには、財務と運用でエンティティを変更して、使用されていないデータ ソースやテーブルを削除するか、getEntityRecordIdsImpactedByTableChange を実装してください。"

財務と運用アプリとの実際のライブ同期で追跡に使用されていないデータ ソースが多い場合、エンティティのパフォーマンスが生同期に影響を与える可能性があります。追跡されたテーブルを最適化するには、getEntityRecordIdsImpactedByTableChange メソッドを使用します。

## <a name="error-5000"></a>エラー 5000
エラー メッセージは、"同期プラグインがエンティティ アカウントのデータ管理イベントに登録されています。 これらは、初期同期および Dataverse へのライブ同期インポートのパフォーマンスに影響する可能性があります。 最も高いパフォーマンスを得る場合は、プラグインを非同期処理に変更してください。 登録済みのプラグインの一覧 {}。"

Dataverse エンティティの同期プラグインは、トランザクション負荷が追加されるため、ライブ同期および初期同期のパフォーマンスに影響する可能性があります。 特定のエンティティで最初の同期や同期で読み込み時間が遅い場合に、プラグインをオフにするか、これらのプラグインを同期させる方法をお勧めします。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

