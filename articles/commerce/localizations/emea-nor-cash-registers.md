---
title: ノルウェイのキャッシュ レジスター機能
description: この記事では、Microsoft Dynamics 365 Commerce のノルウェーで利用可能なキャッシュ レジスター機能の概要と、機能を設定するためのガイドラインを説明します。
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 30bd5ad8c1513c3d56cc4aa0a77b70fe38d31e0a
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346021"
---
# <a name="cash-register-functionality-for-norway"></a>ノルウェイのキャッシュ レジスター機能

[!include[banner](../includes/banner.md)]

この記事では、ノルウェーで使用可能な  Dynamics 365 Commerce のキャッシュ レジスター機能の概要を示します。 また、機能を設定するためのガイドラインを示します。 この機能は次の部分で構成されています:

- すべての国や地域の顧客が利用できる、共通の POS 機能。 たとえば、レシートのコピーが複数印刷されるのを防ぐオプションがあります。
- 販売トランザクション用のデジタル署名など、ノルウェー特有の機能。

## <a name="overview-of-cash-register-functionality-for-norway"></a>ノルウェー向けキャッシュ レジスター機能の概要

### <a name="common-pos-features"></a>一般的な POS 機能

すべての国や地域の顧客が利用できる POS 機能については、[Dynamics 365 Retail のヘルプリソース](../index.md)をご覧ください。

これまで、すべての国や地域の顧客に提供していた以下の POS ローカライズ機能を、ノルウェー向けに特別に利用できるようになりました。

- **レシートのテキスト フィールドを大きなフォントサイズで印刷します。** レシート形式デザイナーの **フォント サイズ** パラメータを使用して、レシート形式のフィールドに大きなフォント サイズを使用するように指定できます。 (大きな文字サイズは通常の文字サイズの約 2倍です。) たとえば、レシートのコピーに「コピー」の表示を大きな文字で印刷したい場合などに使用します。
- **POS 監査イベント ログにレシート コピーの印刷を登録します。** POS 機能プロファイルの **監査** パラメータを使用すると、レシートのコピーを印刷したり、その他の POS 監査イベントを登録することができます。 監査イベントはチャネル データベースと本部に登録されます。 監査イベントは、**監査イベント** ページで表示できます。
- **レシートのコピーが複数回印刷されるのを防ぐ。** POS 機能プロファイルの **監査** パラメータが有効な場合、POS 権限の **レシートのコピーを許可する** は、レシートのコピーを印刷できるかどうかを制御します。 また、レシートのコピーが複数回印刷されないようにするオプションもあります。

また、以下の POS 機能はノルウェー向けに実装されたものですが、すべての国・地域の顧客が利用できるようになりました。

- **POS 監査イベント ログにイベントを追加登録する。** POS 機能プロファイルの **監査** パラメーターを有効にすると、以下のイベントが POS 監査イベントログに登録されます。

    - 価格の確認
    - 税の上書き
    - 明細行の数量修正
    - チャネル データベースからのトランザクションの消去

### <a name="norway-specific-pos-features"></a>ノルウェー固有のPOS機能

POS 機能プロファイルの **ISO コード** のパラメーターが **いいえ** に設定されている場合、以下のノルウェー固有の POS 機能が有効になります。

#### <a name="digital-signing-of-sales-transactions"></a>販売トランザクションのデジタル署名

すべての販売トランザクションはデジタル署名されています。 署名は、トランザクションが確定すると同時に作成され、POS トランザクションの仕訳帳に記録されます。 この署名は、監査目的でエクスポートされる仕訳帳でも利用可能です。

現金販売のトランザクションのみ署名されます。 署名プロセスから除外したトランザクションの例を次に示します。

- 前払い (顧客預金口座の預金)
- 販売注文の販売注文 (顧客注文預金)
- ギフト カードの発行
- 非販売トランザクション (釣銭入力、支払/入金などの削除)

署名されるデータは、次のデータ フィールドで構成されるテキスト文字列です。 データ フィールドはセミコロンで区切られています。

1. 同じ POS に対する前回の署名(最初の取引にはゼロ \[**0**\] が使用されます。)
2. トランザクション日
3. トランザクションの時刻
4. 連続した署名済トランザクション番号
5. 税込トランザクション金額
6. 税抜きトランザクション金額

デジタル署名プロセスでは、SHA-1 ハッシュ関数を持つ RSA 1024 ビットの鍵を使用します (RSA-SHA1-1024)。 Commerce Scale Unit にインストールされている証明書は、署名に使用されます。 証明書の一意の識別子 (フットプリント) は、署名とともに記録されます。

署名は、取引データと共に店舗のデータベースと本部 (HQ) のデータベースに保存されます。 トランザクションの署名は、その生成に使用されたトランザクション データとともに、**小売店トランザクション** ページの **会計トランザクション** クイックタブで確認できます。

#### <a name="receipts"></a>受入

ノルウェーの入庫には、カスタムフィールドを使用して実装された追加情報を含めることができます。

- **レシート タイトル** - レシート形式のレイアウトにフィールドを追加して、レシートのタイプを識別できます。 たとえば、販売入庫には 「販売入庫」 というテキストが含まれます。
- **署名済トランザクションの連番** - 署名済トランザクションの連番をレシートに表示することで、印刷されたレシートとデータベース内のデジタル署名を関連付けることができます。
- **入庫合計** - レシート合計のカスタム フィールドでは、トランザクションの合計金額から売上以外の金額を除外しています。 非売上金額には、次の操作の金額が含まれます:

    - 前払い (顧客預金口座の預金)
    - 販売注文の販売注文 (顧客注文預金)
    - ギフト カードの発行
    - 資金をギフト カードに加算する

#### <a name="x-and-z-reports"></a>X レポートと Z レポート

X レポートと Z レポートに含まれる情報は、ノルウェーの要件に基づいて提供されます。 たとえば、**現金販売額の合計s** には現金販売トランザクションの金額のみが含まれ、ギフトカード発行や前払いなどは含まれません。 また、現金売上高は、品目グループと支払方法ごとに表示されます。 さらに、累積の **売上総計** と **返品総計** の金額が維持され、印刷されます。

#### <a name="saf-t-cash-register-audit-file"></a>SAF-T キャッシュ レジスター監査ファイル

POS トランザクション仕訳帳は、定義済みの標準監査ファイル - 税 (SAF-T) キャッシュ レジスター形式でエクスポートできます。 監査ファイルには、組織に関する情報、関連するマスターデータ (品目グループ、品目、税コードなど)、現金売上取引データとそれらの取引に対する署名、売上以外のイベントデータ、期末レポートデータなどが含まれています。

監査ファイルをエクスポートできるのは、次のような場合です:

- 店舗ごと
- すべての店舗
- 端末ごと
- すべての端末

また、ある法人から別の法人に代わってレポートを送信することもできます。 この場合、法人からエクスポートを実行し、レポートの送信者として法人を指定する必要があります。

SAF-T キャッシュ レジスター フォーマットは、本部では[電子レポート](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)を使って実装されています。 

## <a name="setting-up-commerce-for-norway"></a>Commerce をノルウェー向けに設定する

このセクションでは、ノルウェーに固有で推奨される設定について説明します。 詳細については、 [Dynamics 365 Retailのヘルプ リソース](../index.md) を参照してください。

ノルウェー固有の機能を使用するには、以下の作業を行う必要があります:

- 法人のプライマリ アドレスの **国/地域** フィールドを **NOR** (ノルウェー) に設定します。
- ノルウェーにあるすべての店舗の POS 機能プロファイルで、**ISO コード** フィールドを **NO** (ノルウェー) に設定します。

ノルウェーに対して次の設定を指定する必要があります。

### <a name="enable-features-for-norway"></a>ノルウェー用の機能を有効にする

Commerce headquarters の **機能の管理** ワークスペースで、次の機能を有効にする必要があります。

- (ノルウェー) POS で追加監査イベントを有効にする
- (ノルウェー) POS の営業終了明細書で追加情報を有効にする

### <a name="set-up-the-legal-entity"></a>法人を設定する

法人の名前が指定されている必要があります。 この名前は、X レポートと Z レポートに印刷されます。

さらに、**銀行口座情報** クイックタブの **ルーティング ナンバー** フィールドで、組織番号を指定します。

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>ノルウェーの要件に応じた付加価値税 (VAT) の設定


消費税コード、消費税グループ、品目の消費税グループを作成する必要があります。 また、製品やサービスの消費税情報を設定する必要があります。 消費税の設定と使用方法の詳細については、[消費税の概要](../../finance/general-ledger/indirect-taxes-overview.md)を参照してください。

また、ノルウェーにある店舗では、消費税グループを指定して、**価格に消費税を含める** オプションを有効にする必要があります。

### <a name="set-up-functionality-profiles"></a>機能プロファイルを設定する

監査を有効にして、領収書の番号付けを設定する必要があります。

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>POS 権限グループと店舗従業員の個別権限の設定を更新する

**レシートコピーの印刷** 許可を適切な値に設定します:

- **常に許可する** - オペレータは、レシートのコピーを複数回印刷できます。
- **一度のみ許可する** - オペレータは、レシートのコピーを一度のみ印刷できます。
- **一度だけ許可し、HQ DB が利用可能な場合のみ許可する** - オペレーターがレシートのコピーを印刷できるのは 1 度だけで、HQ データベースが Commerce Data Exchange を介して利用できる場合のみです。リアルタイム サービスでは、どの店舗でも過去にレシートのコピーが印刷されていないことを確認できるようになっています。
- **許可しない** - オペレーターがレシートのコピーを印刷できません。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>カスタム フィールドを設定して、販売領収書の領収書形式で使用できるようにする

**言語テキスト** ページで、領収書 レイアウト用のカスタム フィールドのラベルに次のレコードを追加します。 テーブルに表示されている **言語 ID**、**テキスト ID**、および **テキスト** の値は、単なる例に過ぎません。 要件に合わせてそれらを変更できます。

| 言語 ID | テキスト                   | テキスト ID |
|-------------|------------------------|---------|
| ja-JP       | レシートのタイトル          | 900011  |
| ja       | ギフト カードです           | 900012  |
| ja       | 合計 (販売)          | 900013  |
| ja       | 税の合計 (販売)      | 900014  |
| ja       | 税込合計 (販売) | 900015  |
| ja       | 税額 (販売)     | 900016  |
| ja       | 現金トランザクション ID    | 900017  |

**カスタム フィールド** ページで、領収書 レイアウトのカスタム フィールドに次のレコードを追加します。 **キャプション テキスト ID** の値は、**言語テキスト** ページで指定した **テキスト ID** の値に対応している必要があることに注意してください。

| Name                            | 種類    | キャプション テキスト ID |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | 受信 | 900011          |
| IsGiftCard                      | 受信 | 900012          |
| SalesTotalExt                   | 受信 | 900013          |
| TaxTotalExt                     | 受信 | 900014          |
| TotalWithTaxExt                 | 受信 | 900015          |
| AmountPerTaxExt                 | 受信 | 900016          |
| CashTransactionSequentialNumber | 受信 | 900017          |

> [!NOTE]
> 上の表にあるように、正しいカスタム フィールド名を指定することが重要です。 カスタム フィールド名が正確でない場合、領収書のデータが失われます。

### <a name="configure-receipt-formats"></a>レシート形式を設定する

すべての必須のレシート形式について、**印刷動作** フィールドの値をレシート形式で **常に印刷** に変更します。

領収書の形式デザイナーで、次のカスタム フィールドを適切な領収書セクションに追加します。 フィールド名は、前のセクションで定義した言語テキストに対応していることに注意してください。

1. ヘッダー:

    - **レシート タイトル** - このフィールドはレシートのタイプを識別します。
    - **現金 トランザクション ID** - このフィールドは、署名された現金取引の連番を印刷します。

2. 明細:

    - **ギフト カードである** - このフィールドは、ギフト カードの発行またはギフト カードへの追加の操作に関連するレシートの行を示します。

3. フッター:

    - **合計 (売上)** - このフィールドは、レシートの現金販売額の合計を印刷します。 税抜金額。 前払いとギフト カードの操作は除きます。
    - **合計 (売上)** - このフィールドは、現金販売の場合、レシートの合計税額を印刷します。 前払いとギフト カードの操作は除きます。
    - **税込み合計 (売上)** - このフィールドは、レシートの現金販売額の合計を印刷します。 税込金額。 前払いとギフト カードの操作は除きます。
    - **税額 (売上)** - このフィールドは、税コードごとの現金販売に対するレシートの税額を印刷します。 前払いとギフト カードの操作は除きます。

領収書形式の使用方法の詳細については、[領収書形式の設定とデザイン](../receipt-templates-printing.md)を参照してください。

### <a name="configure-the-saf-t-cash-register-export-format"></a>SAF-T キャッシュ レジスターのエクスポート フォーマットの設定

SAF-T キャッシュ レジスターの設定は、Microsoft Dynamics Lifecycle Services (LCS) からダウンロードできます。 詳細については、[電子申告の構成のインポート](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md) を参照してください。 以下の設定をダウンロードする必要があります:

- **小売チャンネル data.version.1** - データ モデルの構成。
- **DMM 小売チャンネル data.version.1.14** - データ モデル マッピングの構成。
- **NO SAF T Cash Register.version.1.20** - 形式の構成。

設定をインポートした後、**Commerce パラメーター** ページの **電子ドキュメント** タブにある **SAF-T キャッシュ レジスターのエクスポート形式** フィールドで、インポートされたフォーマット設定の名前を選択します。

また、必要なマスター データをあらかじめ定義された SAF-T 標準コードにマッピングする必要があります。 詳細については、ノルウェー税務局が提供する SAF-T キャッシュ レジスターのドキュメントをご参照ください。 マッピングを作成するには、次のページで新しい **SAF-T キャッシュ レジスターコード** のフィールドを設定する必要があります:

- 品目グループ
- 支払方法
- 消費税コード

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

ノルウェー固有の機能を有効にするには、チャネル コンポーネントを構成する必要があります。 詳細については、[配置ガイドライン](emea-nor-fi-deployment.md)を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
