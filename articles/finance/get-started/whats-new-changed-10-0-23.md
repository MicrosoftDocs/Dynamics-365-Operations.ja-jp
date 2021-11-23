---
title: Dynamics 365 Finance 10.0.23 の新機能または変更された機能
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.23 プレビュー リリースの新機能または変更された機能について説明します。
author: kfend
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: dbe4b303182bd9016fce9b6772a4c50122925b18
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647773"
---
# <a name="preview-features-in-dynamics-365-finance-10023"></a>Dynamics 365 Finance 10.0.23 の機能のプレビュー

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.23 の新機能または変更された機能について説明します。 このバージョンには 10.0.1037 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー**: 2021 年 10 月
- **リリースの一般提供 (セルフ更新)**: 2021 年 12 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365/release-plans/) を参照してください。 このトピックが最初に公開された後に、ビルドに加えた機能を含めるために、このトピックを更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化  |
|----|----|----|----|
| グローバル アドレス帳 | 住所の設定で国/地域ごとに既定の都道府県を定義する | グローバル アドレス帳の住所設定で国/地域ごとに既定の都道府県を定義できるようになりました。 既定の都道府県が設定されている場合は、その国/地域に新しい郡または市のレコードが作成される際、それが都道府県フィールドに入力された規定値になります。 詳細については、[住所の設定](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md)を参照してください | 既定で有効になっています。 |
|税の計算    | [自由形式の請求書との統合](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance/tax-calculation-service--integration-free-text-invoice)   | [税計算 Finance and Operations との統合](/dynamics365/finance/localizations/tax-calculation-data-model-overview)   | 自動的に管理者、作成者、マーケティング担当者、またはアナリスト   |
|電子請求    | [イタリア SDI システムへのコンフィギュレーション可能な電子請求書の送信](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance/electronic-invoicing-service-configurable-e-invoice-submission-italian-sdi-sistema-di-interscambio-system-preview)   | [電子請求の概要](/dynamics365/finance/localizations/e-invoicing-service-overview)   | 管理者、作成者、またはアナリスト   |
|   買掛金  | [仕入先未処理トランザクション レポート](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance/open-vendor-transaction-report)  |  [仕入先請求書の概要](../accounts-payable/vendor-invoices-overview.md) |  機能管理   |
|  買掛金  | [買掛金勘定で数量オプション パラメーターに基づいて請求明細行を作成](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance/create-invoice-lines-based-quantity-option-parameter-accounts-payable)  | [仕入先請求書をインポートする際に請求明細行を生成する](../accounts-payable/auto-create-invc-lines-at-import.md) | 自動的 |


## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。 これらの機能を使用または無効にする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で実行する必要があります。

| 機能領域 | 機能管理の機能名 | 詳細 |  
|---|---|---|
| 税の計算  |移動オーダーの税機能   | この機能は 10.0.23 で強化され、移動オーダードキュメントへの税情報の印刷を有効化します。 詳細については、[移動オーダー ドキュメントに税情報を印刷する](https://go.microsoft.com/fwlink/?linkid=2174529)を参照してください。   |  
| 税の計算   |税計算サービス   |この機能は 10.0.23 で強化され、日本、マレーシア、シンガポール、およびタイでの法人の基本住所をサポートしています。 詳細については、[税の計算の概要](../localizations/global-tax-calcuation-service-overview.md)トピックで、**サポートされる国/地域** セクションを参照してください。  |  
| グローバリゼーション  | (ロシア) 在庫残高回転率レポートの計算をバッチで実行する  | この機能を使用すると、在庫残高回転率レポートをバッチで実行したり、計算の結果を保存してから、レポートを表示したりできます。  |
| グローバリゼーション  | (ロシア) 販売注文の会計伝票の修正フラグに従って、Storno 資産在庫トランザクションを転記する  | この機能は、ロシアの貸方票定性機能に影響します。 これはロシア 受注の会計伝票の訂正フラグに応じて、逆資産在庫取引を計上します。 この機能を有効にした場合、在庫トランザクションの財務伝票の **訂正** フラグと在庫トランザクションで **Storno** フラグの間の不一致はこれ以上ありません。  | 
| グローバリゼーション  | (チェコ) 前払消費税金額を取り消すために消費税金額の手動入力を有効にする | この機能を使用すると、前払に対する仕入先請求書の決済時に、前払消費税金額を取り消す必要がある場合、消費税金額を手動で入力できます。 ユーザーが請求書と前払を決済用にマークすると、取り消すために消費税金額を入力する、消費税金額の取り消しが表示されます。 これが表示されるのは、前払の消費税率が請求消費税率と異なる場合です。  | 
| 売上認識基準  | ライセンス コンフィギュレーションから機能管理への売上認識基準の変換 | 売上認識基準機能は、機能管理を使用して有効または無効にできます。 ユーザーは、**機能管理** ワークスペースで **売上認識基準** モジュールを有効にできます。 今後、**売上認識基準** コンフィギュレーション キーは非推奨になります。 コンフィギュレーション キーは引き続き使用できますが、非推奨であるため、このコンフィギュレーション キーを切り替えても、売上認識基準機能には影響はありません。   |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム
Dynamics 365 Finance 10.0.23 には、プラットフォーム更新プログラムが含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.23 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md) を参照してください。 

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=XXXX) を参照してください。 このリリースでは次の問題が修正されています。

| 問題| Description |  
|---|---|
| トランザクション ログの日付フィルター  | Dynamics 365 Finance を使用すると、総勘定元帳内で転記されるデータの数は増加し続けます。 この増加は、トランザクション ログを開く際のパフォーマンスに影響します。 トランザクション ログを表示する際のパフォーマンスを改善するため、この変更により、最後の 7 日間に転記されたトランザクションを表示する既定の日付フィルター付きページが開きます。 既定のフィルターは、**日付** 列のフィルターを使用して変更できます。   |  
| トランザクション ログの日付フィルター   | 多くの場合、プロセスの実行中に、日付範囲の連結プロセスを再開します。 これは、プロセスが正しく開始されなかったと思われる場合や、開始された後に停滞した場合に起こります。 プロセスが再開されると、その日付範囲で開始したプロセスの実行中に、同じ日付範囲が連結に対して入力されます。 連結トランザクションに移動して、連結プロセスの実行中に同じ日付範囲の連結結果を削除しようとする場合があります。 同じデータ セットに対して複数のプロセスを同時に実行すると、問題が発生する可能性があります。 別の連結が既に進行中の場合に、同じ日付範囲では連結プロセスまたは削除を実行できないことを確認する検証を行う、という変更が追加されました。 この変更の一環として、リアルタイムではなくバッチを使用して連結を実行する必要があります。 |  

### <a name="regulatory-updates"></a>規制の更新
Finance and Operations アプリの規制の更新については、[規制の更新](../localizations/regulatory-updates.md)を参照してください。 規制の更新を調べるもう 1 つの方法は、LCS にログインして、問題検索ツールを使用して予定されている規制更新を表示することです。 問題検索では、国、機能の種類、およびリリースを使用して検索を実行できます。 

### <a name="dynamics-365-2021-release-wave-2-plans"></a>Dynamics 365: 2021 リリース ウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 Finance 2021 リリース ウェーブ 2](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance)をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際にそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Finance で削除または廃止された機能](removed-deprecated-features-finance.md) トピックでは、Dynamics 365 Finance で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
