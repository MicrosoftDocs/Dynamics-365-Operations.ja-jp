---
title: ER 構成で起こるトラブルシューティング パフォーマンスの問題
description: このトピックでは、電子申告 (ER) 構成で起こるパフォーマンスの問題を検索して修正する方法について説明します。
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b5f5308f171b6cd4224debec897dbde133e6d8424673aabfab51e6b83b9014e2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744389"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>ER 構成で起こるトラブルシューティング パフォーマンスの問題

このトピックでは、[電子申告](general-electronic-reporting.md) (ER) [構成](general-electronic-reporting.md#Configuration) で起こるパフォーマンスの問題を検索して解決する方法について説明します。

通常、パフォーマンス調査は複数のステップで構成されます。

1. データの [収集](#collecting-data)。
2. 収集したデータを分析します。
3. 分析結果に基づいて、ER 構成を使用して [変更する](#making-changes) か、データをさらに収集することを決定します。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="analyze-execution-time"></a>実行時間の分析

実行時間は、同じ環境で実行されている他のタスクや、データを初めて呼び出したときにデータを使用するキャッシュなど、予測できない要因によって異なる場合があります。 そのため、実行と測定を数回繰り返す必要があります。

パフォーマンスの問題は、レポートで使用する ER 形式の構成が原因でない場合があります。 その場合は、ER 形式の構成を開くために使用する X++ コードが原因です。

1. [アクション センター](#infolog-time) または [イベント ログ](#event-log-time) で、レポートの実行時間を確認します。
2. レポートの実行時間とシナリオの合計実行時間を比較します。
3. レポートの実行時間が合計実行時間よりかなり短い場合は、レポートで処理されるデータ量を考慮してください。

    - レポートで処理されるデータが少量の場合、問題は構成の読み込み時間に関係する可能性があります。
    - レポートで処理されるデータが大量にある場合、問題は前処理の X++ に関係する可能性があります。 [Trace Parser](#analyze-trace-parser-trace) を使用してこのケースを分析します。

    その他のケースについては、次のセクションを参照してください。

4. 異なる量のデータを含む複数のテストを実行して、実行時間がデータ量にどう影響されているかを判断します。

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Trace Parser トレースの分析

小規模な例を準備するか、またはレポート生成時に複数のトレースをランダムに収集します。

次に、[Trace Parser](#trace-parser) で標準のボトムツーアップ分析を行い、次の質問に答えます。

- 時間消費に関して優れたメソッドは何ですか。
- これらのメソッドに必要な時間は、全体のどの時間ですか。

クエリに対して同じ質問に答えます。

メソッドの先頭に "ER" が付いている場合は、次のセクションに進みます。

アプリケーション スイートで作成されたメソッドまたはクエリが表示された場合は、汎用的な最適化 (インデックスの作成など) を検討してください。

呼び出し回数を分析します。 この回数が予想よりも大幅に多い場合は、対応する構成ノードをキャッシュすることを検討してください。

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>データベース呼び出しの分析

少量のデータを含む例を準備し、[ER トレース](#electronic-reporting-traces) を収集できるようにします 。

次に、ER モデル マッピング デザイナーでトレースを開き、ページの下部を確認します。 次の質問に答えます。

- 重複したクエリはありますか。 ある場合は、次のいずれかの修正を検討してください。

    - 1 つの親レコード内に複数の呼び出しがあると思われる場合は、[キャッシュを使用する](#use-caching)。
    - 異なるレコード内に同じ呼び出しがあると思われる場合は、[キャッシュされパラメータ化された計算フィールドを使用する](#cached-parameterized)。
    - データベースから多数の異なるレコードを読み取る必要がある場合、[**統合** データ ソースを使用します](#use-join-datasource)。

- クエリおよびフェッチされたレコードの数は、データの合計数と一致しますか。 たとえば、ドキュメントに明細行が 10 ある場合、レポートが 10 または 1,000 の明細行を抽出したと統計に表示されていますか。 フェッチされるレコードが多数ある場合は、次のいずれかの方法で修正を考慮してください。

    - [**場所** 機能の代わりに **フィルター** 機能を使用して](#filter) SQL サーバー側のデータを処理します。
    - キャッシュを使用して、同じデータをフェッチするのを防ぎます。
    - [収集したデータ機能を使用して](#collected-data)、要約処理に必要な同じデータをフェッチするのを防ぎます。

### <a name="analyze-perfview-traces"></a>PerfView 追跡の分析

[PerfView](#perfview) は経験豊富な開発者のためのツールです。 次の手順の詳細については、[時計時刻調査の基本](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics) を参照してください。

1. スレッド時間を使用して追跡を収集します。
2. **runUnattended** を使用するスタックのみを含めて、構成が実行されているスレッドのみをフィルター処理する必要があります。 (**IncPats** の入力ボックスに **runUnattended** を追加します。)
3. すべての CPU、ネットワーク、およびブロックされた時間を折りたたみます。
4. [PerfView 用の ER プリセット](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml) を読み込みます。
5. **ER** \> **その他のプリセット** を選択します。
6. 名前を確認します。

    - ほとんどの時間を消費するプラットフォーム コードが表示されます。
    - ダブルタップ (またはダブルクリック) し、**呼び出し先** を上方向に移動して確認します。

        接頭語 "ERExpression" を持つクラスおよび式に関連する関数のクラスがある場合は、クラス名に基づいて関数名を変更でき、ER レポジトリを参照して属性を表示できます。

### <a name="fixes"></a>修正

- クエリが CPU 時間の大部分を消費する場合は、クエリの数を減らしてください。

    - 重複するクエリの [ER 追跡を確認します](#analyze-database-calls)。
    - フェッチされるレコード数を確認し、理論的にフェッチするデータの量を評価します。

- 使用している機能がほとんどの CPU 時間を消費する場合は、リソースを最も消費する構成で場所を探してください。
- データ収集機能が CPU 時間の大半を消費する場合、モデル マッピング側で *SQL グループ別* に置き換えることを検討してください。

### <a name="collecting-data"></a><a name="collecting-data"></a>データ収集

環境によっては、使用可能なデータを収集する方法がいくつかあります。

- 合計実行時間を確認する。

    - アクション センターから
    - イベント ログから

- 実行をプロファイルする。

    - ER ツールを使用
    - Trace Parser を使用
    - PerfView を使用

#### <a name="collecting-data-in-a-production-environment"></a>運用環境でデータの収集

運用環境でのみ問題を再現できる場合があります。 次の方法でデータを収集できます。

- [Trace Parser](../perf-test/trace-trace-tutorial.md) トレースを使用
- [ER 実行](trace-execution-er-troubleshoot-perf.md) トレースを使用
- 合計実行時間を使用

#### <a name="collecting-data-in-a-development-environment"></a>開発環境でデータの収集

運用環境で使用できるツールの他に、開発環境で使用できるツールもあります。

- イベント ログ (Microsoft-Dynamics-ElectronicReporting)。 このログを使用すると、合計実行時間を確認できます。
- 一般的な .NETツール (PerfView など)。

また、開発環境では柔軟性が増すため、実験しやすくなります。 たとえば、レポートの一部をオフにすると実行時間への影響を確認できます。

### <a name="tools"></a><a name="tools"></a>ツール

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>アクション センターでの実行時間

ER では、アクション センターで構成の実行時間を表示できます。 このオプションは、対話型セッションで特定のユーザーと会社に対してのみ使用することができます。 この機能を使用するには、次の手順に従います。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。
3. **ユーザー パラメーター** ダイアログ ボックスで、**ファイル生成時間の表示** オプションを **はい** に設定します。

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>イベント ログでの実行時間

1. Windows イベント ビューアーを開きます。
2. **アプリケーションとサービス ログ** で、**Microsoft-Dynamics-ElectronicReporting/Operational** を開きます。
3. **EventID=2** の **FormatMapingRun** イベントを検索します。これらのイベントには、経過時間に関する情報が含まれます。

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Trace Parser トレース 

ER は X++ に実装されているので、一般的な X++ ツールを使用してパフォーマンスを分析できます。 詳細については、[Trace Parser を使用したトレースの取得](../perf-test/trace-trace-tutorial.md) を参照してください。

この方法にはいくつかの制限があります。 ER の一部が C# に実装されているため、表示できない詳細があります。 ただし、データの使用状況の詳細は表示できます。 また、長いレポートを実行すると、トレースのストレージ制限を超える可能性があります。

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER トレース

ER は独自のトレースを収集し、そのトレースには視覚化および分析ツールが含まれます。 詳細については、[電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング](trace-execution-er-troubleshoot-perf.md) を参照してください。

#### <a name="perfview"></a><a name="perfview"></a>PerfView

X++ と ER の両方が .NET プラットフォーム上に実装されているので、共通の .NET ツールを使用できます。 たとえば、無料の [PerfView](https://github.com/Microsoft/perfview) ツールを使用できます。

また、コマンド ラインからデータを収集することもできます。 たとえば、次の Windows PowerShell スクリプトは、マシンであらゆる形式の実行が停止されるまでの実行時間を収集します。

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

この方法にはいくつかの制限があります。 マシンへの管理アクセス権が必要です。 また、難易度がかなり高いため経験豊富な開発者である必要があります。

### <a name="making-changes"></a><a name="making-changes"></a>変更の実行

#### <a name="use-caching"></a><a name="use-caching"></a>キャッシュの使用

キャッシュによってデータの再フェッチに必要な時間が短縮されますが、メモリが必要です。 フェッチされたデータの量が大きくない場合は、キャッシュを使用します。 キャッシュの使用方法の詳細と例については、[実行トレースの情報に基づいてモデル マッピングを改善する](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) を参照してください。

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>キャッシュされパラメーター化された計算済フィールドの使用

値を繰り返し検索する必要がある場合があります。 例には、アカウント名やアカウント番号が含まれます。 時間を節約するために、トップ レベルのパラメーターを含む計算済フィールドを作成し、そのフィールドをキャッシュに追加します。

この方法は、キャッシュされたデータのサイズが小さい場合にのみ使用することをお勧めします。 詳細については、[パラメーター化された計算済みフィールド データ ソースを追加して ER のパフォーマンスを向上させる](er-calculated-field-ds-performance.md) を参照してください。

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>結合データ ソースを作成する

**結合** データ ソースを使用すると、接続されている複数のレコードを 1 つのクエリでフェッチすることができます。 接続されている各レコードをフェッチするために個別のクエリを使用する必要はありません。 たとえば、行が 1,000 あり、リレーションごとに各行の品目データをフェッチすると、1,001 クエリ (= 1,000 + 1) になります。 **結合** データ ソースを使用する場合は、同じデータをフェッチするのに必要なクエリは 1 つのみです。 詳細については、[ER モデル マッピングの結合データ ソースを使用して、複数のアプリケーション テーブルからデータを入手する](er-join-data-sources.md) を参照してください。

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>WHERE 関数の代わりに FILTER 関数を使用します

**[FILTER](er-functions-list-filter.md)** 関数は、SQL Server で条件を実行しますが、**WHERE** 関数は一覧からすべてのデータをフェッチし (一度に 1 つのレコード) 各レコードの条件を適用します。 たとえば、1,000 あるレコードの中からレコードを 1 つ選択するとします。 **WHERE** を使用すると、1,000 のレコードすべてがフェッチされます。 ただし、**FILTER** を使用すると、ちょうど 1 つのレコードがフェッチされます。 **FILTER** では、データベース側でインデックスを使用できます。

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>収集されたデータ機能または累積データ ソースの使用

コンフィギュレーションに、以前にレポート別にフェッチされたデータを集計する *グループ化* コンポーネントがある場合、そのコンポーネントは、すべてのデータを再度フェッチします。 収集したデータ機能を使用すると、ER は最初のフェッチ時にデータを累積できるようになります。 詳細については、[集計と合計を実行するのに必要な ER 構成形式](tasks/er-format-counting-summing-2.md) を参照してください。

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>X++ の構成の一部を再書き込みする

ER は、テーブルおよびクラスの呼び出しメソッド (拡張子を含む) をサポートします。 パフォーマンスを向上させるために、X++ でモデル マッピングの一部を再書き込みしてください。

ER は次のソースからデータを消費できます。

- クラス (**オブジェクト** および **クラス** データ ソース)
- テーブル (**テーブル** および **テーブル レコード** のデータ ソース)

[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) は、呼び出しコードから事前に計算されたデータを送信することもできます。 アプリケーション スイートには、このアプローチの例が多数あります。
