---
title: Dynamics 365 Finance 10.0.21 (2021 年 10 月) の新機能または変更された機能
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.21 プレビュー リリースの新機能または変更された機能について説明します。
author: kfend
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: e856faa696b8a17a0f12f1228cded2a8f031b725cc12b735fa7a9eefe253cb28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756236"
---
# <a name="preview-features-in-dynamics-365-finance-10021-october-2021"></a>Dynamics 365 Finance 10.0.21 の機能のプレビュー (2021 年 10 月)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.21 の新機能または変更された機能について説明します。 このバージョンには 10.0.960.20 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー**: 2021 年 8 月
- **リリースの一般提供 (手動更新)**: 2021 年 9 月
- **リリースの一般提供 (自動更新)**: 2021 年 10 月

## <a name="known-deployment-issue"></a>配置に関する既知の問題
IaaS にリリース 10.0.21 を配置する場合、次のような配置警告が表示される場合があります。

**警告コード:** 95017

**警告メッセージ:** スクリプト [SetupDiagnostics] が VM に対して実行に失敗

警告があっても配置は機能しますが、Lifecycle Services (LCS) では次のような既知の問題が発生する可能性があります。

-   **環境の監視** ページでは、**詳細バージョン情報の表示** リンクは表示されません。したがって、環境にインストールされているモジュールの特定のバージョンは表示されません。 このデータがないと、修正プログラムを適用するプロセスがこのデータを使用して、モジュール バージョンの前提条件が満たされていることを確認するため、後続の修正プログラムが失敗することがあります。 PEAP/プレビュー ビルドを生産で使用したり、修正プログラムを適用することができないため、影響は最小限に抑える必要があります。
-   SQL インサイトの **環境監視** ページの **パフォーマンス メトリックス** タブと **インデックス分析** タブでは、データは表示されません。 その他の **環境監視** 機能は、意図したとおりに機能します。
-   **フル システム診断** ページにはアクセスできません。 夜間のコレクター実行のステータスとそのルールによって検出された問題に関する関連データも表示されません。


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365/release-plans)を参照してください。 このトピックが最初に公開された後に、ビルドに加えた機能を含めるために、このトピックを更新することがあります。

| 機能領域 | フィーチャー | 詳細 |
|----|----|----|
| 電子請求 | [コンフィギュレーション可能なイタリアの電子請求書](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-configurable-italian-electronic-invoice) | [電子請求の概要](../localizations/e-invoicing-service-overview.md) |
| 電子請求 | [コンフィギュレーション可能なフィンランドの電子請求書](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-configurable-finnish-electronic-invoice) | [電子請求の概要](../localizations/e-invoicing-service-overview.md) |
| 電子請求 | [コンフィギュレーション可能な各国向けの PEPPOL 電子請求書](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-configurable-cross-country-peppol-electronic-invoice) | [電子請求の概要](../localizations/e-invoicing-service-overview.md) |
| 電子請求 | [コンフィギュレーション可能なブラジルの E-Invoice (NF-e)](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing--configurable-brazilian-e-invoice-nf-e) | [電子請求の概要](../localizations/e-invoicing-service-overview.md) |
| 電子請求 | [コンフィギュレーション可能なブラジルのサービスの E-Invoice (NFS-e)](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-configurable-brazilian-e-invoice-services-nfs-e) | [電子請求の概要](../localizations/e-invoicing-service-overview.md) |
| 税額の計算 | [税計算サービス](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance/tax-calculation-service-ga) | [税の計算の概要](../localizations/global-tax-calcuation-service-overview.md) |
| 税額の計算 | [税計算サービス – 複数の VAT 登録番号のサポート](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance/tax-calculation-service-supporting-multiple-vat-id-ga) | [複数の VAT 登録番号](../localizations/emea-multiple-vat-registration-numbers.md) |
| 税額の計算 | [税計算サービス – 移動オーダーのサポート税](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance/tax-calculation-service-supporting-tax-transfer-order-ga) | [移動オーダーに対する税金機能のサポート](../localizations/tasks/Tax-feature-support-for-transfer-order.md) |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。 これらの機能を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で明示的にそれらを有効にする必要があります。

| 機能領域 | 機能&nbsp;管理の機能&nbsp;名&nbsp; | 詳細 |
|---|---|---|
| 買掛金  | プロセス自動化 – クエリ フィルターを変更するために追加された追加サポート   | この機能を使用すると、シリーズで、または個々に発生するプロセスの作成や編集に使用する、プロセスの自動化クエリを処理するテーブルおよびフィルタを追加できます。  |
| 買掛金   | 仕入先請求書のワークフローへの転記と送信のブロック   | この機能により、仕入先請求書がワークフロー プロセスに転記および送信されないようになります。 仕入先請求書に請求数量が照合された製品受領書の数量より少ない明細行が含まれる場合、これらのプロセスをブロックできます。 代わりに、買掛金勘定の担当者に問題について警告するメッセージが表示されるため、担当者はワークフローへの転記または送信前に修正できます。   |
| 買掛金   | 仕入先請求書の貸方記入を有効にする   | この機能により、仕入先請求書の貸方記入機能が有効になります   |
| 買掛金勘定および売掛金勘定   | 先日付小切手を使用した銀行口座への支払仕訳帳転記の満期日の検証   |  セッション日付が満期日と同じかそれ以降である場合に、先日付小切手を使用した支払仕訳帳の転記を仕入先および顧客に許可します。  |
| 売掛金管理  | 販売注文の訂正票の転記中に取消対象の事前請求書を選択します  | 販売注文の訂正票の転記中に取消対象の事前請求書を選択できます。 |
| 売掛金管理   | バッチ タスク サイズの行数   | 売掛金勘定の「バッチ タスクのドキュメント明細行の数」パラメーターが導入され、バッチ タスクごとに転記されるドキュメント明細行の数を制限できます。 このパラメーターは、確認書、ピッキング リスト、梱包明細、および請求書の転記に影響します。   |
| 現金および銀行管理  | 顧客決済現金割引率のセット ベースの更新をオフにする  | この機能により、現金割引の日付に対する顧客決済が個別に更新されます。 通常、現金割引の日付の処理が大幅に遅くなるので、現金割引の日付を個別に処理することはお勧めしません。 ただし、現金割引の日付の更新時にデッドロック例外が一貫して発生する場合、現金割引の日付を個別に更新することが役立ちます。 <br> この拡張機能を有効にした後、**売掛金勘定パラメーター** ページに移動し、デッドロックが発生した各会社について、**顧客決済現金割引率のセット ベースの更新をオフにする** パラメーターを **はい** に設定します。 このパラメーターにアクセスするには、**売掛金勘定** > **設定** > **売掛金勘定パラメーター** > **決済** > **オプション** に移動します。 |
| 与信および回収   | 督促状の作成パフォーマンスの向上   | この機能により、督促状の作成プロセスが高速化されます。 これは作成プロセス全体で役立ちますが、このパフォーマンスの向上は、少数の顧客に多数のトランザクションがある場合に特に役立ちます。   |
| Finance Insights   |  顧客支払予測  |  この機能は、請求書に支払が行われる時を予測するために機械学習を使用します。 請求書に支払が行われる時を予測するのに使用される機械学習モデルを作成するために、過去の請求書、支払、および顧客データを使用します。 この機能は、Power AI サービスと特定のデータ フィールドを使用して予測を作成します。 予測の精度を改善するため、機能の設定時に、組織に関連する Power AI の追加のデータ フィールドを選択できます。  |
| 会計帳簿  | (ブラジル) 5011 および 2055 イベントの SPED Reinf の更新   | この修正により、2021 年 4 月に公開されたバージョン 1.5.01 の EFD-Reinf 開発者ガイド マニュアルで導入された更新プログラムが有効になります。 主な変更は、イベント 5011 および 2055 を照会するサービス名とパラメーターに関連しています。   |
| 会計帳簿  | (ブラジル) NFC-e 同期処理   | この機能により、Retail POS ターミナルおよび Commerce 本社で、NFC-e 同期処理が有効になります。   |
| 固定資産   | 減価償却仕訳帳の資産帳簿のロック   | この機能を使用すると、別の未転記の仕訳帳で選択された資産帳簿への減価償却の転記を回避できます。 この機能は固定資産パラメーターで有効にします。   |
| 一般会計 | 大規模な連結のためのパフォーマンスの向上   | 各バッチで効率的に実行できるように、総勘定元帳の連結のパフォーマンスを向上させました。 拡張機能は総勘定元帳のデータを並列処理することで機能し、カスタマイズする必要がある場合のために拡張ポイントが追加されました。   |
| 一般会計   | 保留タイプ トランザクションを含む試算表の生成   | この機能を使用すると、試算表の詳細レポートに含める特定の保留タイプのトランザクションを選択できます。   |
| 一般会計   |  一般会計の年度末拡張機能  | 年度末締処理テンプレートの設定は新しい設定ページに移動します。 既存の年度末決算ページは、総勘定元帳の外貨再評価と同じように変更され、年度末決算処理が実行または取り消されるごとに一覧が表示されます。 会計マネージャーは、新しいページから年度末決算を開始できます。 <br> 会計マネージャーは、年度末決算を取り消す場合に、適切な法人の最新の会計年度を選択し、年度末決算の取消ボタンを選択できます。 取消では、前年度末決算の会計エントリが削除され、年度末決算は自動的に再実行されません。 <br> 会計年度および法人のプロセスを再開することで、年度末決算を再実行できます。 このプロセスでは、引き続き総勘定元帳パラメーター設定を使用して、年度末決算の再実行で新規トランザクションまたは変更されたトランザクションのみを考慮するか、前のトランザクションを完全に取り消して、すべてのトランザクションのプロセスを再実行するか決定します。  |
| 税申告   | (インド) 請求書の請求合計値に源泉徴収 (TSC) を含める    | この機能が有効な場合、ユーザーは販売および仕入請求書の合計値に、TCS (源泉徴収) 税額を含めることができるようになります。   |


## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム
Dynamics 365 Finance 10.0.21 には、プラットフォーム更新プログラムが含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.21 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md) を参照してください。 

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166) を参照してください。

### <a name="regulatory-updates"></a>規制の更新
Finance and Operations アプリの規制の更新については、[規制の更新](../localizations/regulatory-updates.md)を参照してください。 規制の更新を調べるもう 1 つの方法は、LCS にログインして、問題検索ツールを使用して予定されている規制更新を表示することです。 問題検索では、国、機能の種類、およびリリースを使用して検索を実行できます。 

### <a name="dynamics-365-2021-release-wave-plans"></a>Dynamics 365: 2021 リリース ウェーブ プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 Finance 2021 リリース ウェーブ 1](/dynamics365/release-plan/2021wave1/finance-operations/dynamics365-finance) および [Dynamics 365 Finance 2021 リリース ウェーブ 2](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際にそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Finance で削除または廃止された機能](removed-deprecated-features-finance.md) トピックでは、Dynamics 365 Finance で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
