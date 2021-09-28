---
title: Azure Data Explorer を使用して、生の情報ログをクエリします
description: このトピックでは、Azure Data Explorer を使用して、生の情報ログをクエリする方法について説明します。
author: andreashofmann1
ms.date: 09/13/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: andreash
ms.search.validFrom: 2021-08-20
ms.openlocfilehash: e59b0d67c9ff391fb25da3831fc8b966cff50aa4
ms.sourcegitcommit: 59d507c0dd6f0bec3ab72034e12d582133ab2a52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2021
ms.locfileid: "7496826"
---
# <a name="use-azure-data-explorer-to-query-raw-information-logs"></a>Azure Data Explorer を使用して、生の情報ログをクエリします

[!include[banner](../includes/banner.md)]

顧客、パートナー、コンサルタント、またはサポート エンジニアが、Finance and Operations アプリの低レベル セキュリティ データを参照する必要がある場合があります。 これらの使用例には、エラーのトラブル シューティング、パフォーマンス関連の調査、または Finance and Operations アプリ動作に関するいくつかの追加の理解を取得しようとしている場合があります。 権限のあるユーザーは、Lifecycle Services (LCS) の環境監視機能を使用してアクセスでき、さまざまな方法でフィルタ処理して、LCS の[生の情報ログ](monitoring-diagnostics.md#raw-information-logs) の内部に表示することもできます。 データ グリッドを使用して、ログ エントリを検査できます。 LCS ではより洗練されたピボットを許可しないので、ユーザーは Excel をその目的に使用できます。 利用統計情報は、CSV 形式でダウンロードおよび書式設定できます。 

Excel は、このデータの高度なクエリには最適なツールではありません。 その目的に適したより良いデザイン ツールは、Azure Data Explorer です。 高性能なデータ分析向けに最適化された革新的クエリ言語であるクストを提供します。 、発生の *特定のプロセスが発生した頻度*、*発生の 90% はどのくらいかかりましたか*、*1 時間毎にどのくらいの頻度で正しいアクションが 1 日のコースで実行されたか*、などの質問への回答が非常に簡単になり、強力なグラフィックを使用してバックアップすることができます。 

これらのタイプのグラフィックの外観の例を 2 つ示します。

![棒グラフの例 1}](media/ADE1.png)

![棒グラフの例 2}](media/ADE2.png)

Azure Data Explorer のあまり知られていない機能は、CSV ファイルをサポートすることです。 Azure Data Explorer を使用すると、CSV データ ファイルをアップロードおよびステージ済みとして取得し、これらのファイルをクストの言語でクエリできます。 Azure Data Explorer クラスターを設定するには、[クイック スタート: Azure Data Explorer クラスターおよびデータベースの作成](/azure/data-explorer/create-cluster-database-portal) を参照してください。

## <a name="steps-to-upload-to-azure-data-explorer"></a>Azure Data Explorer にアップロードする手順
Azure Data Explorer にアップロードするには、次の手順に従ってください。 

1.  LCS の生のログ ページでクエリを実行します。
    > [!NOTE]
    > 次の手順では、時間間隔またはフィルタを調整して正しいデータに移動します (エクスポートの場合、行の制限は 5000 になります)。
   
2.  グリッドを Excel にエクスポートします。

    ![LCS の環境モニタリング ページです。](media/ADE3.png)

3.  Excel でファイルを開き、変更せずに保存します (これにより、書式設定の問題が修正されます)。
4.  Azure Data Explorer では、ツリー ビューでクラスターを右クリックし、**新しいデータを取り込む** を選択します。 次のページで、**ローカル ファイルからデータを取り込む** を選択します。

    ![新しいデータの取り込みをクリックします。](media/ADE4.png)

5.  クラスターを選択します。 インポートするデータの新しいテーブル名を指定し、インポートする CSV ファイルを最大 10 件のファイル選択します。 CSV フォーマットを選択します。 データがインポートされるまで、**次へ** を選びます。

    ![データがインポートされます。](media/ADE5.png)

6. **クエリ** タイルを選び、データに対してクスト クエリを書き込む場所を表示します。 

    ![クエリ タイルを使用します。](media/ADE6.png)

クスト クエリの言語については、[チュートリアル: Azure Data Explorer および Azure Monitor でクストのクエリを使用する](/azure/data-explorer/kusto/query/tutorial?pivots=azuredataexplorer) を参照してください。

## <a name="sample-queries"></a>サンプル クエリ
### <a name="analysis-of-sql-queries-occurring-in-the-commerce-runtime-custom-or-built-in"></a>Commerce Runtime で発生している SQL クエリの分析 (カスタムまたは組み込み)

```kusto
new2
| where EventId == 1809 // designates SQL finished trace
| project executionTimeMilliseconds, sqlQuery
| summarize NumAllCalls=count(), TotalDuration=sum(executionTimeMilliseconds), AvgDuration = avg(executionTimeMilliseconds), 
    percentiles(executionTimeMilliseconds, 90) by tostring(substring(sqlQuery, 0, 70))
| where percentile_executionTimeMilliseconds_90 > 1
| order by TotalDuration desc
```

### <a name="performance-of-any-retailserver-calls--100ms"></a>任意の RetailServer 呼び出し > 100ms のパフォーマンス

```kusto
// run this for the data
new2
| where EventId == 5009 // designates a RetailServer finished trace
| project executionTimeMilliseconds, apiAction
| summarize NumAllCalls=count(), TotalDuration=sum(executionTimeMilliseconds), AvgDuration = avg(executionTimeMilliseconds), percentiles(executionTimeMilliseconds, 90) by tostring(apiAction)
| where percentile_executionTimeMilliseconds_90 > 100
| order by percentile_executionTimeMilliseconds_90 desc

// include this for the chart
| project apiAction, percentile_executionTimeMilliseconds_90
| render columnchart
```
