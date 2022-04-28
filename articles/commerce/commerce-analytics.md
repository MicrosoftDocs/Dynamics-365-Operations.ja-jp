---
title: Commerce 分析 (プレビュー)
description: このトピックでは、Microsoft Dynamics 365 Commerce で分析機能をインストールして使用する方法について説明します。
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 63d6e5ef7e883578106495d5ec778bbd686ee92d
ms.sourcegitcommit: 722854cb0d302d01ce3d9580ac80dc7c23d19bf5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2022
ms.locfileid: "8550010"
---
# <a name="commerce-analytics-preview"></a>Commerce 分析 (プレビュー)

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce に含まれる機能分析機能である Commerc e分析 (プレビュー) のインストール方法について説明します 。

## <a name="commerce-analytics-preview-live-demo"></a>Commerce 分析 (プレビュー) のライブ デモ

[Commerce Analytics (プレビュー) のライブ デモ](https://aka.ms/CommerceAnalyticsDemo)を体験できます 。

![Commerce 分析 (プレビュー) Summary](media/CommerceAnalytics_Summary.png)
![Commerce 分析 (プレビュー) Payments](media/CommerceAnalytics_Payments.png)
![Commerce 分析 (プレビュー) Web アクティビティ](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Commerce 分析 (プレビュー) システム アーキテクチャ

### <a name="key-components"></a>主要コンポーネント

Commerce 分析 (プレビュー) は、次の主要なコンポーネントで構成されています:

- すぐに使用できる対話型 Power BI レポート
- Azure Synapse Analytics の SQL ビュー
- Azure Data Lake 内のエンティティとオントロジー データ
- Data Lake の生データ

![Commerce 分析システム アーキテクチャの主要コンポーネント](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>データ フロー

#### <a name="step-1-data-generation"></a>手順1: データの生成

データは、以下のいずれかのソースから、トランザクションデータや行動データとして取得されます。

- コールセンターの関連付けでは、Commerce HQ クライアントを使用して販売注文を処理します。
- 販売時点管理 (POS) のレジ担当者が販売トランザクションを処理します。
- Headless Commerce (Commerce Scale Unit) を使用して、カスタム アプリケーションに売上を作成します。
- e コマースのコンテンツは、eコ マースの Web サイトを参照します。
- e コマースのコンテンツは、eコ マースの Web サイトを参照します。
- データは Dynamics 365 Connected Spaces など、他のシステムによって作成されます 。

#### <a name="step-2-ingestion-and-pre-processing"></a>手順 2: インジェストと事前処理

トランザクションのデータは、直接 (コマース本部のクライアントに直接取り込まれた注文の場合) または Commerce Scale Unit を経由して (POS、eコマース、または Headless Commerceを使用するカスタムクライアントで取得される注文の場合) Commerce HQ に送られます。

そして、「Data Lake へのエクスポート」機能を使って、トランザクションデータを生データとしてデータ レイクにコピーします。 データ レイクでは、生データは Tables フォルダに格納されます。

eコマースのWeb 活動のデータは、データ レイクに直接送信されます。 Dynamics 365 Connected Spaces などの他のシステムで作成されたデータは、それらのシステムから直接データ レイクに送られます。

#### <a name="step-3-transformation-and-aggregation"></a>手順3: 変換と集計

生データがデータ レイクに入った後、Commerce の分析サービスはそれを読み取り、変換しと集約を行い、論理的エンティティ (エンティティ フォルダ) と集約されたメトリクス (in the オントロジー フォルダ) の形でデータ レイクに書き込みます。

#### <a name="step-4-querying"></a>手順4: クエリ

Azure Synapse Analytics は、Transact-SQL (T-SQL) インターフェースを介して Data Lake のデータを照会するために使用します。 このインターフェイスには SQL ビューが含まれます。 SQL ビューを使用すると、T-SQL クライアント (アドホック分析用) を介して直接、または Power BI などの可視化ツールを介して、データ レイク内のデータを連携して照会することができます。

#### <a name="step-5-modeling-and-serving"></a>手順 5: モデリングとサービス

Azure Synapse Analytics で照会されたデータは、Power BI のセマンティック モデルに転送されます。 データの種類に応じて、定期的にメモリ内 Power BI にインポートするか、実行時に直接クエリするかを選択します。

最後に、データは Power BI のビジュアルで表示され、ユーザーはそれを確認したり、操作したりすることができます。

## <a name="commerce-analytics-preview-functional-overview"></a>Commerce 分析 (プレビュー) 機能の概要

### <a name="summary"></a>要約

Commerce 分析のテンプレート アプリには、以下の主要なレポート ページが含まれています:

1. [トップ レベル フィルタ](#TopLevelFilters)
2. [製品](#ProductsPage)
3. [顧客](#CustomersPage)
4. [チャネル](#ChannelsPage)
5. [販売注文](#SalesPage)
6. [余白](#MarginsPage)
7. [返品](#ReturnsPage)
8. [割引](#DiscountsPage)
9. [支払利息](#PaymentsPage)
10. [顧客](#CustomersPage)
11. [比較](#ComparisonPage)
12. [Web 活動](#WebActivityPage)
13. [Web アクティビティ - トップ レベル のフィルター](#WebActivityTopLevelFilters)

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> トップ レベル フィルター

- 日付の設定

    - 年
    - 四半期
    - 月
    - 週
    - 日付

- チャネル設定

    - 法人
    - チャネル タイプ
    - 顧客タイプ
    - 販売タイプ
    - チャンネル
    - 組織階層

- 製品の設定

    - カテゴリ階層
    - カテゴリ

#### <a name="products"></a><a name="ProductsPage"></a> 製品

- 営業
- Margin
- 返品

#### <a name="customers"></a><a name="CustomersPage"></a>顧客

- 営業
- Margin
- 返品

#### <a name="channels"></a><a name="ChannelsPage"></a> チャネル

- 営業
- Margin
- 返品

### <a name="sales"></a>営業 <a name="SalesPage"></a>

- 出荷場所別
- チャンネル/店舗/ターミナル別
- 従業員別
- 日付別
- 時間別
- 製品カテゴリ別

### <a name="margins"></a><a name="MarginsPage"></a> 利益幅

- 出荷場所別
- 副産物
- 日付別

### <a name="returns"></a><a name="ReturnsPage"></a> 返品

- 金額別返品

    - 店舗を使用
    - 副産物
    - 日付別

- トランザクション別返品

    - 店舗を使用
    - 副産物
    - 日付別

### <a name="discounts"></a><a name="DiscountsPage"></a> 割引

- 店舗を使用
- 副産物
- 日付別
- 分解

    - 法人
    - 店舗
    - 割引タイプ
    - 割引名
    - 製品

### <a name="payments"></a><a name="PaymentsPage"></a> 支払

- チャンネル/ターミナル別
- 支払い方法/種類別
- 日付別
- 分解

    - 法人
    - チャネル タイプ
    - 店舗
    - ターミナル
    - 支払方法

### <a name="customers"></a><a name="CustomersPage"></a>顧客

- 有効期間の値 (LTV)

    LTVは、顧客が Dynamics 365 Commerce のすべての販売チャネル (POS、eコマース、コール センターを含む) で使用した合計金額に基づいて算出されます。

- Recency

    直近の情報は、顧客が組織と最後に取引をしてからの日数に基づいて計算されます。 現在、直近情報では、eコマースの閲覧履歴など、取引以外のエンゲージメント シグナルは考慮されていません。

- 頻度

    頻度は、顧客の組織との取引エンゲージメントに基づいて算出されます。 現在、頻度では、eコマースの閲覧履歴など、取引以外のエンゲージメント シグナルは考慮されていません。

- リレーションシップの長さ

    リレーションシップの長さは、顧客のレコードがシステムに作成されてからの日数に基づいて計算されます。

- トランザクション数

### <a name="comparison"></a><a name="ComparisonPage"></a> 比較

- 期間別の製品比較

    - 販売と販売の差額
    - 利益幅と利益幅の差額

- 期間別の顧客

    - 販売と販売の差額
    - 利益幅と利益幅の差額

### <a name="web-activity"></a><a name="WebActivityPage"></a> Web アクティビティ

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> トップ レベル フィルター

- 日付範囲
- チャネル タイプ
- チャンネル
- カテゴリ階層

#### <a name="acquisitions"></a>取得

- ページ ビュー

    - 国または地域別
    - 副産物
    - ユーザー別のサインインの状態
    - 日付別

- E コマースの注文
- 変換率

    - 日付別

- 変換用じょうご

    - ページ タイプ別ページ ビュー (ホーム ページ、カテゴリ ページ、または製品の詳細ページ)
    - カートに追加
    - チェックアウト
    - 購買

#### <a name="sessions"></a>セッション

セッションとは、ユーザーがeコマースを訪問した際のエピソードを意味します。 セッションは、30 分間操作されなかった場合、または 24 時間操作された場合に終了したとみなされます。

- 国または地域別
- 発生元別 (外部参照元)
- ユーザー別のサインインの状態
- セッション カウント

    - 日付別
    - エントリ ページ別

- セッションごとの注文

    - 日付別

- セッションのバウンス率

    セッション バウンスとは、ユーザーが eコマースにアクセスした直後に離脱したセッションを意味します。 詳細については、[バウンス率](https://en.wikipedia.org/wiki/Bounce_rate)を参照してください。

- セッション単位のクリック

#### <a name="visitors"></a>閲覧者

eコマース サイトの匿名の訪問者は、ユーザーが使用している特定のブラウザと特定のデバイスに基づいて一意に識別されます。 Commerce では、異なるブラウザやデバイスを介した匿名の訪問者を追跡することはできません。 同じデバイスで同じブラウザを使用する匿名の訪問者は、ブラウザのキャッシュデータが消去されるか、一定期間 (通常は12ヶ月) が経過するかいずれかが発生するまで、複数のユーザーセッションにわたって一意に識別されます。

訪問者がサインインした状態で eコマースを閲覧した場合、Commerce 分析は訪問者に関する追加情報を提供することができます。 この情報は、すべての Dynamics 365 Commerce 販売チャネル (POS、eコマース、コールセンターを含む) における訪問者の過去の購入の結果として、組織が持つ既存の関係に基づいています。 追加情報には、現在の期間、関係の長さ、有効期間の値、頻度データが含まれます。

- 訪問者の利益幅
- 訪問者の平均注文数
- 来場者平均売上
- eコマースの変更カウント

    - 日付別
    - 場所別

        現在、Commerce分析では、eコマースの訪問者のロケーションを把握するために、国や地域レベルの細分性しか提供できません。

    - 最新性別

        直近の情報は、顧客が組織と最後に取引をしてからの日数に基づいて計算されます。 現在、直近情報では、eコマースの閲覧履歴など、取引以外のエンゲージメント シグナルは考慮されていません。

    - リレーションシップの長さ別

        リレーションシップの長さは、顧客のレコードがシステムに作成されてからの日数に基づいて計算されます。

    - 有効期間の値 (LTV) 別

        LTVは、顧客が Dynamics 365 Commerce のすべての販売チャネル (POS、eコマース、コール センターを含む) で使用した合計金額に基づいて算出されます。

    - 頻度別

        頻度は、顧客の組織との取引エンゲージメントに基づいて算出されます。 現在、頻度では、eコマースの閲覧履歴など、取引以外のエンゲージメント シグナルは考慮されていません。

#### <a name="impressions"></a>インプレッション

インプレッションとは、eコマースの訪問者が商品のビジュアルを一度だけ表示することです。 たとえば、eコマースの訪問者がeコマース サイトのホームページに移動し、**売上げ上位** のリスト モジュールでヨガマットの商品を見たとします。 その後、訪問者は同じヨガマット製品を **あなたへのおすすめ** のリストモジュールで閲覧します。 この例には、2つの製品の変更方法を含みます。

現在、インプレッションは以下のサーフェスで追跡されます:

- リスト (**おすすめ**、**売上げ上位**、**あなたへのおすすめ**、**人気上昇中** など)
- カート モジュール
- 検索結果コンテナー
- カテゴリ検索結果のコンテナー

現在、カルーセル モジュールやカスタム ビジュアルに表示された商品は、インプレッション関連の指標にはカウントされません。

**インプレッション レポート** ページには次のメトリックスが表示されます:

- インプレッションのカウント

    - ページ タイプとモジュール別

        ページタイプとは、eコマースサイトの各ページに定義されているページの一般的なタイプを表わします。 モジュール タイプは、商品が表示されているEコマースのビジュアル モジュールのタイプを表わします。

        モジュール別のインプレッションを表示するには、ページやモジュールを視覚にドリルダウンする必要がある場合があります。

    - 副産物
    - ユーザー別のサインインの状態
    - 日付別

- インプレッションのクリック数

    インプレッション クリックは、eコマース サイトの訪問者が商品のビジュアルを選択した際に発生するものです。 通常、訪問者はこの製品の詳細ページに移動します。

- インプレッション クリック率 (CTR)

    CTRは、インプレッション クリック数の合計をインプレッション数の合計で割ったものです。

## <a name="commerce-analytics-preview-installation"></a>Commerce 分析 (プレビュー) のインストール

> [!NOTE]
> Commerce 分析 (プレビュー) はプレビュー段階であり、アメリカ合衆国、カナダ、イギリス、ヨーロッパ、東南アジア、東アジア、オーストラリア、および日本の地域でで利用できます。 Finance and Operations 環境がそれらの地域にある場合は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、環境でこの機能を有効にできます。 この機能を使用するには、[Azure Data Lake へのエクスポートを構成](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) を参照してください。

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Commerce分析の有効化と構成 (プレビュー)

Commerce分析 (プレビュー) をインストールするには、Azure サブスクリプションのリソースを作成するアクセス許可が必要です。 LCSに にアドインをインストールする権限も必要となります。

Commerce 分析 (プレビュー) を有効にして設定するには、次の手順に従います。

1. [Commerce 分析 (プレビュー) のプレビュー サブリンク フォームを送信する](#joinPreview)
2. [Data Lake へのエクスポート アドインの有効化と構成](#enableExportToDataLake)。
3. [Azure Synapse workspace をインストールして構成します](#configureAzureSynapse)。
4. [キー コンテナーにシークレットを追加する](#addSecrets)。
5. [Commerce analytics (プレビュー) の有効化と構成をします](#enableCommerceAnalyticsAddin)。
6. [Power BI テンプレート アプリをインストールします](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Commerce 分析 (プレビュー) 用の取り込みフォームを送信する

[Commerce 分析 (プレビュー) のプレビュー サブリンク フォーム](https://forms.office.com/r/vW5VLJGXZ2)を送信します。 要求の処理後は、フォームに入力されたメールアドレスに確認メールが送信されます。

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>Data Lake へのエクスポート アドインの有効化と構成

> [!IMPORTANT]
> Data Lake アドインにエクスポートを設定する場合は、Data Lake アドインにエクスポート設定ページの **リアルタイム データの変更** チェック ボックスをオフにして、リアルタイムのデータ変更を選択解除します。 **リアルタイム データ変更** 機能はプレビュー 機能であり、現在 Commerce 分析でサポートされていない機能です。 この機能を有効にすると、Commerce 分析は Data Lake にあるデータを処理できなくなり、Power BI レポートのほとんどにデータが表示されなくなります。

Commerce 分析 (プレビュー) は、データ入力にエクスポート機能に依存し、Commerce 本部のデータを Data Lake にエクスポートして、データの鮮度を保ちます。 Commerce 分析 (プレビュー) を構成する前に、[Azure Data へのエクスポートを構成する](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) に記載手順に従って Data Lake へのエクスポートの有効化と構成をします。

Data Lake アドインへのエクスポートを設定している間に、以下の情報を後で入力する必要があるので、メモしておいてください:

- <a name="keyVault"></a>提供した鍵保管庫のドメイン ネーム システム (DNS) 名。
- 指定した シークレット名で、アプリケーション ID とアプリケーション シークレットを含むもの。 詳細については、[キー コンテナーにシークレットを追加する](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets) を参照してください。

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Azure Synapse workspace のインストールと構成

Commerce 分析 (プレビュー) では、Azure Synapse workspace に Synapse SQL on-demand をプロビジョニングする必要があります。 Azure Synapse workspace のインストールと構成は、以下の手順で行います。

1. Azure サブスクリプションに Azure Synapse workspace をインストールします。 詳細については、[クイックスタート: シナプス ワークスペースを作成する](/azure/synapse-analytics/quickstart-create-workspace)を参照してください。
1. <a name="serverlessep"></a>ワークスペースのプロビジョニングが完了した後は、リソースの概要ページを開き、**Serverless SQL エンドポイント** の値をメモしておきます。 次のセクションで、この値をキー コンテナーに格納する必要があります。
1. 概要ページで、**オープンな構文スタジオ** のリンクを選択 して、ワークスペースの Azure Synapse Studio を開きます。
1. 左側のメニューで、**管理** を選択します。 メニュー名を確認するには、左メニューの展開リンクを選択する必要がある場合があります。
1. **セキュリティ グループ** で、**アクセス制御** を選択します。 
1. **追加** を選択します。
1. **ロールの 割り当ての追加** ウィンドウで、次の表に示すオプションを設定します。

    | オプション | 値 |
    |--------|-------|
    | スコープ | **ワークスペース** を選択します。 |
    | ロール | **Synapse SQL の管理** を選択します。|
    | ユーザーの選択 | [Data Lake にエクスポート アドインのインストール時に作成した](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication)アプリケーションの名前を検索します。 アプリケーションが検索結果として表示されたら、それを選択します。 **選択されたユーザー、グループ、またはサービスプリンシパル** のセクションにアプリケーションが表示されます。 |

1. **適用** を選択し、ロールの割り当てを完了します。 アプリケーションには、Synapse SQL 管理者特権が付与されます。 したがって、Commerce 分析 (プレビュー) LCS アドインの構成中に必要なビューが作成される可能性があります。

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>キー コンテナーにシークレットを追加する

Data Lake へのエクスポート アドインの構成時に使用したのと同じ [キー コンテナー](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault) に、次の表に示すシークレットを追加する必要があります。 各シークレットには、シークレット名と指定された値を指定する必要があります。

|  推奨されたシークレット名 | シークレットの値 | シークレット値の例 |
|---------|---------|---------|
| synapse-sql-server | [Azure Synapse workspace を構成する](#serverlessep)際に注目したサーバーレス SQL エンドポイントの値です。 | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | SQL 読み取り専用ユーザーに設定するパスワードです。 Power BI レポートは、このパスワードを使用してサーバーレス SQL に接続します。 パスワードを設定するには、組織のパスワード ポリシーに従います。 | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Commerce 分析 (プレビュー) アドインの有効化と構成

LCS に Commerce 分析 (プレビュー) アドインをインストールするには、使用する予定の環境の LCS の環境管理者である必要があります。

Commerce 分析 (プレビュー) アドインをインストールして構成するには、以下の手順に従います。

1. [LCS](https://lcs.dynamics.com/) にログインし、ご利用の環境に移動します。
2. **環境アドイン** タブの、**環境** ページで、**新しいアドインのインストール** を選択します。
3. ダイアログ ボックスで、**Commerce 分析 (プレビュー)** を選択します。
4. **アドインの設定** ダイアログ ボックスで、次の情報を入力します。

    | 情報 | ソース | サンプル値 |
    |---|---|---|
    | Azure Active Directory (Azure AD) テナント ID | [Azure ポータル](https://portal.azure.com/) にログインし、**Azure Active Directory** サービスを開きます。 続いて **プロパティ** ページを開き、**テナント ID** フィールドの値をコピーします。 | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | Azure キー コンテナーの DNS 名 | キー コンテナーの DNS 名 を入力します。 この値は、[Data Lake へのエクスポート アドイン](#keyVault)を設定する際にメモしておく必要があります。 | `https://contosod365datafeedpoc.vault.azure.net/` |
    | アプリケーション ID を含むシークレット名 | アプリケーション ID を格納するシークレット名を入力します。 この値は、[Data Lake へのエクスポート アドイン](#keyVault)を設定する際にメモしておく必要があります。 | `app-id` |
    | アプリケーションのシークレットを含むシークレット名 | アプリケーションのシークレットを格納するシークレット名を入力します。 この値は、[Data Lake へのエクスポート アドイン](#keyVault)を設定する際にメモしておく必要があります。 | `app-secret` |
    | Azure Synapse のサーバーレス SQL エンドポイントを含むシークレット名 | サーバーレス SQL のエンド ポイントを格納するシークレット名を入力します。 [キー値ーにシークレットを追加](#addSecrets)している間に、シークレットを作成する必要があります。 | `synapse-sql-server` |
    | Azure Synapse の SQL 読み取り専用ユーザーに設定するパスワードが含まれるシークレット名 | サーバーレス SQL 読み取り専用ユーザーに設定するパスワードを格納するファイル名を入力します。 このユーザーはユーザー用に作成され、Power BI レポートではサーバーレス SQL サーバーに接続するために使用される必要があります。 [キー値ーにシークレットを追加](#addSecrets)している間に、シークレットを作成する必要があります。 | `readonly-sql-pwd` |

1. チェック ボックスをオンにしてサービス条件を承認し、**インストール** を選択します。

    システムは、Commerce 分析 (プレビュー) アドインを環境に合わせてインストールし、構成します。 このプロセスには数分かかる場合があります。 完了後は、 **Commerce 分析 (プレビュー)** が、**環境** ページに表示され、状態が **インストール済** に変化します。

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI テンプレート アプリをインストールします

Commerce 分析 (プレビュー) の Power BI テンプレート アプリのインストールには、以下の手順で行います:

1. 組織のアカウント ID を使用して [Power BI ポータル](https://powerbi.microsoft.com/) にサインインします。
1. [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) にアクセスして、Commerce 分析 (プレビュー) Power BI のテンプレート アプリをインストールします。 または、[Dynamics 365 Commerce 分析の AppSource ページ](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) にアクセスし、**今すぐ取得** を選択します。
1. 初めてこのアプリをインストールする場合は、手順 5 に進んでください。 以前にインストールしたことがある場合、アプリのアップデートには以下のオプションが適用されます:

    - **ワークスペースとアプリの更新** – 既存のテンプレート アプリを更新し、アプリのインスタンス名やアクセス許可の構成など、既存のアプリの設定を上書きします。
    - **アプリを更新せずにワークスペースのコンテンツのみを更新する** – 既存のテンプレート アプリをアップデートしても、既存のアプリの設定は保持されます。 *このオプションは、アプリのアップデートに推奨されるオプションです。*
    - **アプリの別のコピーを新しいワークスペースにインストールする** – 新しいワークスペースを作成し、その中に既存のテンプレート アプリのコピーを作成します。 既存のワークスペースはそのまま残します。

1. アップデート方法を選択して、**インストール** を選択します。
1. 左のペインで **Apps** を選択して、インストールしたアプリを開きます。
1. **接続** を選択して、アプリとデータソースを接続します。 以前にアプリをインストールしたことがある場合は、黄色いメッセージ バーにある **データを接続する** リンクを選択します。
1. 次のフィールドを設定します。

    | フィールド | 値 |
    |---|---|
    | サーバー | [Azure Synapse workspace を作成した](#serverlessep)後にメモしておいたサーバーレス SQL のエンドポイントを入力します。 |
    | データベース | **CommerceAnalytics** と入力します。 |
    | 言語 | リストから値を選択します。 このフィールドは、ローカライズされた商品名やカテゴリー名に使用されます。 値は大文字と小文字を区別します。 |
    | 期間の設定 | リストから値を選択します。 選択された月数のデータが Power BI データセットに取り込まれます。 選択した値は、データセットのサイズとの同期に必要となる時間に影響します。 |

1. **次へ** を選択します。 Azure Synapse SQL データベースに接続するための認証情報の入力を求められたら、次の表に示すようにフィールドの値を設定します。

    | フィールド | 値 |
    |---|---|
    | 認証メソッド | **Basic** を選択します。 |
    | ユーザー名 | **reportreadonlyuser** を入力します。 |
    | パスワード | [SQL 読み取り専用ユーザー用にキー コンテナーに保存した](#roUser)パスワードを入力します。 |

1. **サインインしてスツ属する** を選択します。
1. データセットの更新が完了するまで待機します。 続いて **アプリの編集** を選択してアプリのワークスペースを開き、データセットの更新状況を確認することができます。 アプリのワークスペースでは、オプションとして、データセットの自動更新スケジュールの設定、アクセス許可の管理、アプリのインスタンス名の変更も可能です。

### <a name="privacy"></a><a name="privacy"></a>プライバシー

Microsoft にとってお客様のプライバシーは重要です。 詳細については、Microsoft [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=521839)をお読みください。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
