---
title: オンプレミス診断
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 配置の診断データを公開するための情報を提供します。
author: PeterRFriis
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: Platform Update 12
ms.openlocfilehash: d472a3fd0c7234447146e5e704baa9c0415267c8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344858"
---
# <a name="on-premises-diagnostics"></a>オンプレミス診断

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 は、最新式の Azure Diagnostic Tool を使用して、クラウド ベースの顧客の機能を提供する Azure Services の正常性およびパフォーマンスを監視します。 Finance + Operations (オンプレミス) で実装し、オンプレミス ソリューションの正常性とパフォーマンスを監視できるようにするには、いくつかのサード パーティ製品が利用可能です。 

このトピックでは、Elastic Stack の設定とコンフィギュレーション、サード パーティ製品、およびオンプレミス ソリューションの診断モニタリングを提供できる多くの選択肢の 1 つについて説明します。

診断ソリューションを検討する際、次の実装の基礎を検討してください。

- 診断システムは、30 日分に相当する診断情報を収集し、格納できる必要があります。
- 診断リポジトリは、多くのクライアント コンピューターで共有できるように中心的な場所に設定する必要があります。
- イベント タイプ、分類、およびデータを含む構造化診断イベントを作成します。
- 未加工のテキスト (逆シリアル化) に格納されているイベントを簡単に照会および検索します。
- イベントに機密情報や個人データを格納しないでください。

> [!NOTE]
> 既定では、Elastic Stack クラスター内の通信は HTTPS 経由で送信されません。 リスクを考慮し、それらのリスクの軽減策を準備または実装していない限り、Elastic スタックを設定しないでください。 X-Pack の支払済バージョン は、Elastic Stack のコミュニケーションを暗号化するために使用されます。 設定の詳細については、クラスタでの TLS の設定を参照してください。 オープン ソース Elasticsearch プラグイン もあります。 ドキュメントによると、Microsoft はこのプラグインをテストしていませんが、HTTPS を有効にすることができます。 Microsoft では、HTTPs、VPN、または別のセキュリティで保護された、暗号化されたプロトコルを使用して、暗号化された通信を常に使用することをお勧めします。 コンテンツにエンド ユーザー、顧客、個人または機密データが含まれている場合、多くの業界認定および法律では、暗号化された送信を使用する必要があります。

## <a name="diagnostic-data-guidelines"></a>診断データのガイドライン
Finance + Operations (オンプレミス) の配置と実行を診断するためには、診断データへのアクセスが必要です。 クラウドの配置では、マイクロソフトは、サービスの診断データを保存して監視し、環境を健全に保ちます。 オンプレミス配置に関しては、顧客がこのタスクを担当します。

使用したい診断データ ストアおよびクエリ ツールを選択することができます。 ただし、最低限、ツールは、次のタスクを実行する必要があります。

- ストアは、30 日間分の診断データを格納できます。
- イベントが集約される場所に格納されると、サポート エンジニアは問題に関連するイベントを検索する複数のマシン間を切り替える必要がありません。
- イベントは、イベント タイプおよびイベント データに基づいて、発見が可能です。
- イベント データ (XML 形式) では、逆シリアル化すると、イベント データを照会および移動が可能です。

## <a name="elastic-stack-example"></a>Elastic スタックの例
前のセクションに表示されている診断データのガイドラインを満たすため、Microsoft は Elastic スタックの設定をテストしました。 この設定には次のコンポーネントが含まれています。

- **Elasticsearch** – ストレージ、イベント インデックス作成、およびイベント クエリの実行。 Elasticsearch の詳細については、[Elastic Web サイト](https://www.elastic.co/products/elasticsearch)を参照してください。
- **Logstash** – 負荷分散およびイベント データ変換用。
- **Winlogbeat** – 診断データ収集用。
- **Kibana** – Elasticsearch に格納されているデータを照会するためのインタフェース。

> [!NOTE]
> 既定では、Elastic Stack クラスター内の通信は HTTPS 経由で送信され **ない** ようになっています。 リスクを考慮し、それらのリスクの軽減策を準備または実装していない限り、Elastic スタックを設定しないでください。 X-Pack の[支払済バージョン](https://www.elastic.co/subscriptions) は、Elastic Stack のコミュニケーションを暗号化するために使用されます。 設定の詳細については、[クラスタでの TLS の設定](https://www.elastic.co/guide/en/x-pack/current/ssl-tls.html)を参照してください。 オープン ソース [Elasticsearch プラグイン](https://github.com/floragunncom/search-guard-ssl) もあります。 ドキュメントによると、Microsoft はこのプラグインをテストしていませんが、HTTPS を有効にすることができます。

Elastic スタックを展開する場合、このトピックで説明されている手順を実行するなら異なる経験になるかもしれません。 テストでは、Microsoft は、Elastic Stack コンポーネントのバージョン 6.2.3 と、Microsoft Dynamics 365 for Finance and Operations 7.3 およびプラットフォーム更新プログラム 12 を使用しました。

このトピックでは、Elastic スタック がオンプレミス配置のために動作するために必要な設定、およびコンフィギュレーションの手順を Microsoft がどのように処理したかについて説明します。 Finance + Operations (オンプレミス) に関連していないガイダンスについては、Elastic.co のドキュメントを参照してください。

## <a name="install-and-configure-the-elastic-stack"></a>Elastic スタックのインストールと構成
Winlogbeat を除くすべての Elastic スタックのホストされているコンポーネントはすべて Java 上で動作します。 テスト シナリオでは、Microsoft は最初に Elasticsearch、Logstash、または Kibana (つまり、すべてのオーケストレータ ノード) を実行する各ノードに、Java ランタイム環境 (JRE) 8 (64 ビット) の最新バージョンをダウンロードしてインストールしました。 [https://www.oracle.com/technetwork/java/javase/downloads/index.html](https://www.oracle.com/technetwork/java/javase/downloads/index.html) から Java 8 を取得することができます。

2018 年 6 月現在、Elastic スタックは Java 8 で実行します。 Java の新しいバージョンで実行しようとすると、すべてが動作しない可能性があります。

> [!NOTE]
> Linux では、Winlogbeat を除く、全体の Elastic Stack をホストできます。 テストでは、Microsoft が Microsoft Windows サーバー 2016 の仮想マシン (Vm) のスタックをホストしました。

各ノード上のさまざまなコンポーネントのファイアウォールで、ポートを開くことを忘れないようにしてください。

設定中に行き詰まった場合、Elastic.co には Elastic スタックのインストールとコンフィギュレーションについての広範かつ適切なドキュメントがあります。 特定のタイプのエラーについては、Web 検索で Elastic.co フォーラムと StackOverflow の両方から信頼性の高い結果が得られます。

### <a name="component-matrix"></a>コンポーネントのマトリックス
テストでは、Microsoft は小規模から中規模の配置用の次の設定を使用しました。

| ノード            | Elasticsearch | Logstash | Kibana | Winlogbeat |
|-----------------|---------------|----------|--------|------------|
| オーケストレータ #1 | x             |          |        | x          |
| オーケストレータ #2 | x             | x        |        | x          |
| オーケストレータ #3 |               | x        | x      | x          |
| AOS #1...*n*    |               |          |        | x          |

> [!IMPORTANT]
> Microsoft は、テスト目的で、ELK インストールのために オーケストレータ機械を使用しました。 オーケストレーション サービスから重要なリソースを奪う可能性があるため、実稼動環境または重要なサンドボックス環境で ELK のインストールにオーケストレータ マシンを使用しないでください。 代わりに、別のマシンを使用して ELK サービスをホストします。

### <a name="elasticsearch"></a>Elasticsearch
Elasticsearch のインストールは、非常に簡単です。 テストでは、Microsoft が、「[Microsoft Windows インストーラー (MSI) ファイル](https://www.elastic.co/downloads/elasticsearch)」をオーケストレータ #1 および オーケストレータ #2 ノードにダウンロードしました。 インストーラの既定の設定のほとんどはそのままにしておくことができます。 このセクションでは、Microsoft が変更した設定について説明します。

オペレーティング システム (OS) が再起動された場合に、Elasticsearch がもう一度実行を開始するのを容易にするために、Microsoft は、それを Windows 上でサービスとしてインストールしました。 インストーラーを使用して、サービスを設定できます。

インストーラーの **コンフィギュレーション** で、Microsoft は、各 Elasticsearch ノードをクラスターにインストールするときに、同じクラスター名を使用しました。

Microsoft はすべての Elasticsearch ノードを Data、Master、Ingest という 3 つの役割をすべて実行するように設定しました。

Kibana と Elasticsearch の使用量に応じて、メモリ増設を検討してください。 C:\\ProgramData\\Elastic\\Elasticsearch\\config\\jvm.options ファイルの -Xm オプションを後で変更し、Elasticsearch を再起動することによって、この設定を変更することができます。

設定した Elasticsearch ノードの数に応じて、検出の最小マスターノードを適切に設定できます。 わからない場合は、マスター ノードを空にしておくことができます。 探索および Node の詳細については、[Node](https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-node.html) を参照してください。

発見可能性に関しては、**ネットワークの設定** で、Microsoft は、各ノードの **ネットワーク ホスト** 値をノードの IP アドレスに設定し、すべての Elasticsearch ノードの IP アドレスを、各ノードの **Unicast Hosts** リストに追加します。 たとえば、IP アドレスが 10.0.0.12 のオーケストレータ #1 の場合、Microsoft は **Network host** の値を **10.0.0.12** に設定し、次の IP アドレスを **Unicast Hosts** リストに追加しました。10.0.0.12 および 10.0.0.13 (10.0.0.13 はオーケストレータ #2)

**Elasticsearch 6.3 以降のバージョンをインストールする場合、この段落は無視できます。** 今または後で、X-Pack をインストールすることができます。 設定および X-Pack をインストールする必要があるかどうかに関する詳細については、このトピックの「X-Pack」を参照してください。 ここでは、X-Pack がどういうものか理解していない限り、インストールしないでください。

> [!IMPORTANT]
> ファイアウォールの HTTP ポート (既定では、ポート 9200) と、ノード通信ポート (既定では、ポート 9300) を開きます。

インストールが成功したことを確認するには、ブラウザーを起動し、アプリケーションのアドレスを開きます。 いくつかの JavaScript Object Notation (JSON) 出力が表示されます。

### <a name="logstash"></a>Logstash
テストの設定では、Microsoft は、Winlogbeat のいくつかのイベントで調整が必要なことがわかりました。 Logstash は、その機能を提供します。

Microsoft は Logstash をオーケストレータ #2 および オーケストレータ #3 ノードで C:\\ELK\\Logstash にダウンロードしました。

Logstash が起動時に実行されることを確認するために、Non-Sucking サービス マネージャー (NSSM) を使用して、Logstash バッチ スクリプトのサービスを設定しました。

1. Nssm.exe を Logstash の bin フォルダーにコピーする (たとえば、C:\\ELK\\Logstash\\6.2.4\\bin\\) 。
2. bin フォルダーから Windows PowerShell を開き、次のコマンドを実行します。

    ```Console
    .\nssm.exe install Logstash
    ```

3. **アプリケーション** タブで、次のフィールドを設定して、**保存** をクリックします。

    - **パス:** C:\\ELK\\Logstash\\6.2.4\\bin\\logstash.bat
    - **起動ディレクトリ:** C:\\ELK\\Logstash\6.2.4
    - **引数:** -f C:\\ELK\\Logstash\\config\\logstash-dyn365finops.conf

    (より多くの設定ができます。 ただし、今のところ、これらの設定で十分です。)

4. 次のコマンドを実行します。

    ```Console
    .\nssm.exe start Logstash
    ```

Microsoft が実行したテストでは、NSSM には、インストールされたサービスの再起動に問題がありました。 Logstash と Kibana に対し NSSM は 100% の信頼性がなかったため、サービスは OS 起動サービスとして扱われました。

Microsoft は、logstash-dyn365finops.conf という Logstash の構成ファイルを作成しました。 このファイルは、LCS 共有アセット ライブラリの「LBD 診断構成」と呼ばれる zip ファイルのモデル アセット タイプで使用できます。 [LCS 共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary) に移動して、このファイルをダウンロードします。 抽出した後 C:\\ELK\\Logstash\\6.2.4\\config に配置する必要があります。このファイルは、診断で有用な変換を実行します。

設定のためコンフィギュレーションを行うには、クラスターの Elasticsearch ノードを指すように、**出力** セクションの **ホスト** フィールドを変更する必要があります。 たとえば、**ホスト** を **\["ORCH1:9200", "ORCH2:9200"\]** に変更します。

構成は、次のセクションから Winlogbeat 構成を使用してテストされました。

ビートが Logstash にデータを送信できるように、Logstash をホストしているコンピューターのファイアウォールで、Winlogbeat ポート (既定では、ポート 5044) を開くことを忘れないでください。

### <a name="winlogbeat"></a>Winlogbeat
Microsoft は Winlogbeat を C:\\ELK\\Winlogbeat の 各 Application Object Server (AOS) およびオーケストレータ ノードにダウンロードし、winlogbeat.yml file を構成しました。 Winlogbeat のサンプル構成ファイルは、LCS 共有アセット ライブラリの「LBD 診断構成」と呼ばれる zip ファイルのモデル アセット タイプで使用できます。 [LCS 共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary) に移動して、このファイルをダウンロードします。 

設定のためコンフィギュレーションを行うには、すべての Logstash ノードを指すように **output.logstash.hosts** フィールドを変更する必要があります。 Winlogbeat は、負荷分散を処理します。

Winlogbeat が Orchestrator ノード上で実行されている場合、**Tags** フィールドは **AOS** から  **ORCH** もしくはそれに類する値に変更できます。 Microsoft は **fields.env** フィールドを使用して、配置環境 (サンド ボックス、サンド ボックス -n、または生産) を設定します。 このようにして、複数の環境およびノード タイプからのデータが照会されると、より明確な分離が行われます。

Winlogbeat には、サービス インストーラーが含まれています。 Microsoft は、このインストーラーを使用して、各ノード上のサービスとして Winlogbeat を設定しました。 Windows ロゴキーと R キーを同時に押して、ツールの実行を開始し、次のコマンドを実行します。

```powershell
powershell.exe -ExecutionPolicy Bypass -File C:\ELK\Winlogbeat\install-service-winlogbeat.ps1
```

### <a name="kibana"></a>Kibana
Kibana は、Elasticsearch の診断データをクエリするインターフェイスを提供します。

Microsoft は Kibana を C:\\ELK\\Kibana にダウンロードし、次の方法で kibana.yml ファイルを構成しました。

```Console
server.host: "10.0.0.14"
server.name: "Dyn365FinOps On-Premises Diagnostics"
elasticsearch.url: "http://ORCH1:9200"
```

Kibana から、Microsoft は **管理** タブでインデックス パターンを定義しなければなりませんでした。インデックス パターンは名前でインデックスをグループ化するため、1 つのインデックス パターンが作成された 2 つのインデックス: 配置-\* およびランタイム-\* を必要とするためです。 インデックス名は、大文字と小文字が区別されます。

Microsoft は、既定のパターンとしてランタイム -\* インデックス パターンを設定しました。 **管理** タブのインデックス パターンを確認するときは、アスタリスク (\*) をクリックします。 インデックス パターンが、**Discover** タブに表示されます。

[![ランタイム インデックス パターン。](./media/runtime-index-patter.png)](./media/runtime-index-patter.png)

Microsoft は Kibana を Logstash と同じ方法でサービスとして実行し、Kibana が OS の起動時に起動されるようにしました。 Logstash とは異なり、kibana.bat は、コンフィギュレーション ファイルのパスは必要ありません。 したがって、C:\\ELK\\Kibana\\6.2.4\\bin\\kibana.bat を参照する NSSM サービスをインストールできます。

ネットワーク上で Kibana を参照したいなら、Kibana 用のポートを開くことに注意してください。 既定のポートは 5601 です。

#### <a name="example-queries-on-the-discover-tab-in-kibana"></a>Kibana の検出タブでのクエリの例
次のサンプル クエリでは、診断データの調査を開始できます。 例に示されているもの以上のものが必要な場合、次のクエリのいずれかをお試しください。

- **低速データベース クエリの検索:** 検索フィールドに **低速** と入力して、イベント データのどこかに「低速」という単語が含まれているイベントを検索します。 より正確にするには、**AosDatabaseSlowQuery** のタスク名を持つイベントを検索し、検索フィールドに **TaskName:AosDatabaseSlowQuery** と入力します。
- **最新の例外を見つける:** **例外** を検索フィールドに入力して、例外をスローしたイベント、または例外を処理してログに記録したイベントを探します。 Kibana の右上隅で、検索を制限する必要がある期間を選択します。 そこで設定したタイム フレームは、タブの間で保持されます。 したがって、**視覚化** タブ上のデータは選択されているタイム フレームに反映されます。

    [![検索の時間枠。](./media/time-visualize.png)](./media/time-visualize.png) 

- **AOS ノードからイベントを検索:** ノードからすべてのイベントを検索するために、検索フィールドに **host:AOS1** と入力します。
- **他のイベントと最も近い、特定のイベントを見つける:** 興味のあるイベントが見つかったら、そのイベントのヘッダーの横にある **関連するドキュメントを表示します** をクリックして、同時に発生したイベントを見つけます。 同時に発生した、異なる Application Object Server (AOS) ノードからのイベントが表示されている場合、追加のフィルターを追加して、必要なノードからのイベントのみを表示できます。

    [![関連するドキュメントを表示します。](./media/events-with-proximity.PNG)](./media/events-with-proximity.PNG)

#### <a name="thirty-day-data-retention"></a>30 日間のデータの保持
古いデータからハード ディスクを保持するために、Microsoft は Curator v5.5 を使用して 30 日以上経過したインデックスをクリーンアップしました。

Microsoft はキュレーターを C:\\ELK\\Curator でオーケストレータ ノードのいずれかにダウンロードします。 [zip ファイル「LBD診断構成」のモデル アセット タイプのLCS 共有アセットライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary) で使用可能なサンプル構成ファイル curator.yml は、 次に、C:\\ELK\\Curator に配置して、キュレーター を Elasticsearch クラスターに接続します。 特定のサーバーを参照するにはファイルを編集する必要があります。 

キュレーターはアクションを実行し、Microsoft は「30day_data_retention_actions.yml」というアクション構成ファイルを作成して、C:\\ELK\\Curator 内の 30 日経過したインデックスをクリーンアップします。 留保構成ファイルは、LCS 共有アセット ライブラリの「LBD 診断構成」と呼ばれる zip ファイルのモデル アセット タイプで使用できます。 [LCS 共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary) に移動して、このファイルをダウンロードします。

Microsoft は、Windows タスク スケジューラの基本的なタスクを作成します。 このタスクは、土曜日と日曜日に毎週トリガーを持ち、トリガーにはプログラムを開始するための次の設定があります。

- **プログラム/スクリプト:** C:\\ELK\\Curator\\curator.exe
- **引数を追加:** --curator.yml のコンフィグレーション .\\30 日\_データ\_保存\_actions.yml
- **開始:** C:\\ELK\\Curator

## <a name="x-pack"></a>X-Pack
> [!IMPORTANT]
> 2018 年 6 月現在、バージョン 6.3 以降の Elastic スタック コンポーネントがリリースされています。 この更新されたバージョンでは、X-Pack の無料機能を毎年ライセンスを更新することなくデフォルトで有効にすること、また、後で有料機能にオプトインすることで、X-Pack をより上手く処理します。 6.3 よりも前の Elastic スタック バージョンをインストールしている場合、このセクションの内容は設定に部分的にのみ適用されます。

Elasticsearch のインストール時に X-Pack をインストールするように選択できます。 代わりに、[インストールをすることができます。](https://www.elastic.co/guide/en/x-pack/current/installing-xpack.html)。

X-Pack には無料の基本ライセンスがあり、毎年更新する必要があります。

Microsoft では、Kibana からコンマ区切り値 (CSV) 形式でエクスポートするデータのクエリを有効にするために無料版がインストールされています。 X-Pack ではその他の便利な機能がありますが、いくつかは有料サブスクリプションでのみ使用可能です。

無料の機能だけを有効にし、他の X-Pack の試用版の機能を使用しないように、Microsoft は、elasticsearch.yml および kibana.yml のコンフィギュレーション ファイルに次の設定を追加しました。

```Console
xpack.graph.enabled: false
xpack.ml.enabled: false
xpack.security.enabled: false
xpack.watcher.enabled: false
```

これらの設定は、セキュリティ モジュールが有効ではないため、Kibana と Elasticsearch が資格情報を求めることも停止します。

X-Pack を動作させるには、logstash.yml 構成ファイルも次のように構成する必要があります。

```Console
xpack.monitoring.elasticsearch.url: "http://orch1:9200"
```

X-Pack の支払済バージョンには、クラスター、パスワードで保護されたデータ アクセスなどの接続に使用するための HTTPS 暗号化が含まれています。 X-Pack の詳細については、[Elastic Web サイト](https://www.elastic.co/products/x-pack)を参照してください。

### <a name="export-a-query-to-a-csv-file"></a>CSV ファイルへのクエリのエクスポート
Kibana では、**検出** タブで、クエリを作成し、保存します。 クエリを保存した後、**検出** ページの上部にある **レポート** タブの **CSV を生成** をクリックします。

## <a name="troubleshooting"></a>トラブルシューティング
### <a name="you-dont-receive-any-data-in-kibana"></a>Kibana 内のデータを受信しません
Kibana で、何もデータを受け取っていない場合、Winlogbeat から Logstash、Elasticsearch、および Kibana のログを確認してください。 Winlogbeat のインストールでは、C:\\ProgramData\\winlogbeat\\Logs にログが記録されますが、他の Elastic スタック コンポーネントはログをインストール パスに近づけることに注意してください (例: C:\\ELK\\Elasticsearch\\logs)。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
