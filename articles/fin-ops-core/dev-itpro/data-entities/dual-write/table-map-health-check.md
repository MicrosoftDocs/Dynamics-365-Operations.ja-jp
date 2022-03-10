---
title: テーブル マップの正常性チェックのエラー コード
description: このトピックでは、テーブル マップの正常性チェックのエラー コードについて説明します。
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061281"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>テーブル マップの正常性チェックのエラー コード

[!include [banner](../../includes/banner.md)]



このトピックでは、テーブル マップの正常性チェックのエラー コードについて説明します。

## <a name="error-100"></a>エラー 100

エラーメッセージは、"Finance and Operations の推奨を実行するために最低限必要な Finance and Operations プラットフォーム のバージョンは PU 43 です" になります。

この機能には、財務と運用アプリのバージョン 10.0.19 以降のプラットフォームを更新する必要 があります。

## <a name="error-400"></a>エラー 400

エラー メッセージは、"エンティティ \{Finance and Operations UniqueEntityName\} のビジネス イベント登録データが見つかりません。つまり、マップが実行されていないか、すべてのフィールド マッピングが単一方向であるかのいずれかです。" になります。

## <a name="error-500"></a>エラー 500

エラー メッセージは、"プロジェクト \{project name\} にプロジェクト構成がありません。 これはプロジェクトが有効になっていないか、すべてのフィールド マッピングが Customer Engagement から Finance and Operations への単一方向である可能性があります。"

テーブル マップのマッピングを確認します。 これらが Customer Engagement アプリから 財務と運用アプリへの単一方向の場合、財務と運用アプリから Dataverse への実同期化のトラフィックは生成されません。

## <a name="error-900"></a>エラー 900

このエラー メッセージは、"無効なソース フィルター \{sourceFilter\} format for entity \{Finance and Operations UniqueEntityName\}" です。

財務と運用アプリのテーブル マップで指定されたソース フィルターの構文が正しくありません。 このフィルター基準を検証するには、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps) を参照してください。

## <a name="error-1000"></a>エラー 1000

エラー メッセージは、"デュアル書き込みライブ同期に使用されるエンティティ \{Finance and Operations UniqueEntityName\} クエリは \{Finance and Operations EntityFilterQueryString\}  です。 クエリ基準を満たすレコードは、同期のためにピックアップされます。" です。

返されたエンティティ クエリは、エンティティのバッキング SQL クエリです。 ライブ同期のために収集されるビジネス データを決定するクエリに対して、内部結合またはフィルタが適用されたかどうかを確認します。 二重書き込みライブ同期のために取得されるレコードごとに実行する必要がある、内部結合およびフィルターの選択は必須です。

## <a name="error-1300"></a>エラー 1300

エラー メッセージは、"エンティティ \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} 向けのバーチャル フィールド \{s.EntityFieldName\} は、デュアル書き込み向けに追跡できない場合があります。"

Finance and Operations テーブルからの仮想フィールドは追跡に対して有効になっていません。 ライブ同期ではデータを同期できますが、列に対して行われた変更をピックアップできません。

## <a name="error-1500"></a>エラー 1500

エラーメッセージは、"データソース \{datasource.DataSourceName\} の追跡を可能にするには、非ルックアップ フィールドに少なくとも 1 つのフィールドがマップされている 必要があります。" です。

エンティティからのデータ ソースに、デュアル書き込み用にマップされたフィールドが存在しません。 基になるテーブルに対する変更は、デュアル書き込みでは追跡されません。

## <a name="error-1600"></a>エラー 1600

エラー メッセージは、"データソース: エンティティ \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} の \{datasource.DataSourceName\} には範囲があります。 範囲の条件を満たすレコードだけが出荷用に選択されます。" です。

財務と運用アプリのエンティティは、フィルター範囲が有効になっているデータ ソースを使用できます。 これらの範囲により、ライブ同期の一部として取得されるレコードが定義されます。 一部のレコードが財務と運用アプリから Dataverse にスキップされた場合は、そのレコードがエンティティの範囲基準を 満たされているかどうかを確認します。 このチェックを簡単に実行するには、次の例のような SQL クエリを実行します。

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>エラー 1700

エラー メッセージは、"テーブル: エンティティ \{datasourceTable.Key.entityName\} の \{datasourceTable.Key.subscribedTableName\} は、エンティティ \{origTableToEntityMaps.EntityName\} に対して追跡されています。 複数のエンティティについて追跡される同じテーブルが、ライブ同期トランザクションのシステム パフォーマンスに影響する可能性があります。" です。

同じテーブルが複数のエンティティによって追跡される場合、そのテーブルに対する変更により、リンクされたエンティティに対するデュアル 書き込み評価がトリガーされます。 フィルター句は有効なレコードのみを送信しますが、実行時間の長いクエリや最適化されていないクエリ プランがある場合、評価でパフォーマンス上の問題が発生する可能性があります。 この問題は、ビジネスの視点からは避けれない可能性があります。 ただし、複数のエンティティにまたがるテーブルが多い場合は、エンティティ クエリのエンティティの簡略化や、最適化のチェックを検討する必要があります。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
