---
title: Dynamics 365 Commerce 10.0.29 (2022 年 10 月) のプレビュー
description: この記事では、Microsoft Dynamics 365 Commerce 10.0.29 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 08/17/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 1e05f53f9ecb0a1994828172f6999a0bd5c208bc
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306235"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>Dynamics 365 Commerce 10.0.29 (2022 年 10 月) のプレビュー

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce プレビュー バージョン 10.0.29 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1326 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 8 月
- **リリースの一般提供 (自己更新)**: 2022 年 9 月
- **リリースの一般提供 (自動更新)**: 2022 年 10 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに追加された機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---------|------------------|----------------|--------------| 
| B2B | [チャネル全体の販売契約書のサポートを有効にする](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | この機能により、企業間 (B2B) の販売組織は Commerce headquarters の販売契約を使用して、購入者の契約に基づく価格を定義できます。 B2B 購入者が eコマースの Web サイトで買い物をすると、B2B 購入者の組織用に設定された契約ベースの価格が、製品の検出、購入、およびチェックアウト エクスペリエンス全体に自動的に適用されます。 | 機能管理<p>*コマース チャネル全体での販売契約書のサポート* |
| Customer Service | [Dynamics 365 Customer Service 用オムニチャネルを使用して顧客サービスを有効にする](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | カスタマイズされた快適なコマース エクスペリエンスを消費者に提供するには、最上位のカスアマー サポート エクスペリエンスが重要です。 現物店舗、オンライン チャンネル、ソーシャル チャンネルなど、現在複数のコマース タッチポイントが存在します。 消費者は、こうしたすべてのタッチポイントについて、カスタマイズされたサポート エクスペリエンスを期待しています。 この機能を使用すると、Dynamics 365 Customer Service 用オムニチャネルと統合することで、カートの販売への変換を増やし、顧客とのカスタマイズされたエンゲージメントを強化して、顧客サービスを向上できます。 | 管理者/作成者によって有効化 |
| eコマース | eコマースでの製品比較のサポート | 買い物客がさまざまなカテゴリの製品を比較し、自分で適切な購買の意思決定ができるようにします。 この機能は、企業と顧客間 (B2C) サイトと B2B サイトの両方で使用できます。 | サイト ビルダー | 
| ギフト カード | 会社間データ共有の小売ギフト カード テーブルのサポート | Dynamics headquarters は、Dynamics アーキテクチャの特定のテーブルに対して会社間データ共有を有効にする機能をサポートしています。 Dynamics 365 Commerce では、この機能で、小売ギフト カード テーブル に対して会社間データ共有のサポートを追加します。 そのため、ある会社のギフト カードのデータを環境内の別の会社に複製することができます。 元の会社のギフト カード テーブルに行った変更は、複製する会社のギフト カード テーブルに共有されます。 | 開発者 |
| グローバリゼーション | [新しい Commerce SD Kに対する Commerce ローカライズ機能の有効化](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-commerce-localization-features-new-commerce-sdk) | この新しい機能により、機能管理フレームワークまたはパラメーターを使用して Commerce Headquarters の Commerce ローカライズ機能を活用できます。 会計統合サンプルが、新しい Commerce SDK に組み込まれ、独立した梱包がサポートされるようになりました。 また、この機能により、グローバルな Commerce 顧客が Store Commerce アプリを使用する方法も採用されます。<p><p>このリリースには、[オーストリア](../localizations/emea-aut-fi-sample.md)、[チェコ共和国](../localizations/emea-cze-fi-sample.md)、 [フランス](../localizations/emea-fra-cash-registers.md)、[ドイツ](../localizations/emea-deu-fi-sample.md)、[イタリア](../localizations/emea-ita-fpi-sample.md)、[ノルウェー](../localizations/emea-nor-cash-registers.md)、および[ポーランド](../localizations/emea-pol-fpi-sample.md)の編集機能と会計統合サンプルが含まれています。 | 管理者/作成者によって有効化 |
| 業績 | "顧客の編集" シナリオの RTS 依存関係の削除 | 販売時点管理 (POS) および eコマース チャネルでは、高可用性とハイ パフォーマンスがデフォルト期待されます。 こうした期待に応えるために、Dynamics 365 Commerce チャネルは、顧客情報を編集する際に、Commerce headquarters とのリアルタイムの通信に依存する必要がなくなりました。 非同期顧客および非同期でない顧客に対して顧客情報を非同期的に編集する機能を使用すると、Commerce headquarters へのリアルタイムの呼び出しを減らすのに役立ちます。 | 管理者/作成者によって有効化 |

## <a name="feature-state-changes-in-this-release"></a>このリリースでの機能の状態変更

次の表に、バージョン 10.0.29 で必須となった、または既定でオンになった機能の一覧を示します。 これらのすべての機能は、バージョン 10.0.29 に更新すると、システムに対して自動的に有効になります。 必須機能はオフにできませんが、既定で有効になっている機能は[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用してオフにすることができます。

テーブルには、以前はパブリック プレビューでしたが、バージョン 10.0.29 で一般に利用できるように変更された機能も一覧表示しています。 この変更は、これらの機能は現在運用環境での使用が推奨されることを示しています。 特に断りのない限り、既定では、これらの機能は無効になっています。 そのため、使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用してこれらの機能を有効にする必要があります。

| フィーチャー | タイトル | 新しい機能の状態 |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(ブラジル) ブラジルに固有の Commerce 機能 | 既定で有効 |
| RetailAdvancedGTETaxAdjustmentFeature | (インド) Retail POS で小売トランザクション用に計算された GST を小売明細書に適用する | 既定で有効 |
| RetailChronologicalInvoicePostingFeature_IT | (イタリア) 時系列順に転記されていない小売請求書を有効にする | 既定で有効 |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (メキシコ) 小売 CFDI グローバルの割引調整 | 既定で有効 |
| RetailFiscalIntegrationConfigurationEnhancementFeature | 会計統合技術プロファイルの上書き | 既定で有効 |
| RetailFiscalIntegrationConnectorLocationFeature | POS レジスターからの直接会計統合 | 既定で有効 |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | 会計統合データのローカル ストレージ バックアップ | 既定で有効 |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | ドキュメントの登録の延期 | 既定で有効 |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | POS レジスターの会計登録状態 | 既定で有効 |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (インド) eコマース注文の請求書住所に基づいて販売税を計算します。 | 既定で有効 |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (ポーランド) 小売請求書の既定の販売ドキュメントの状態 | 既定で有効 |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (メキシコ) Retail CFDI グローバルの税基準額の丸め再計算。 | 既定で有効 |
| RetailSupplementaryInvoiceFeature | 小売店舗で完了した現金売りトランザクションの補助請求書を有効にする | 既定で有効 |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  在庫バッファーと在庫レベルを有効化する    |  既定で有効|
|RetailInboundOutboundInventoryValidationFeature|   POS の入庫および出庫の在庫処理で検証を有効化する   |   既定で有効   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  拡張 eコマース チャネル側在庫計算ロジック |   既定で有効   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    販売時点管理の在庫調整   |  既定で有効  |
| RetailMultiplePickupDeliveryModeFeature |  複数の集荷配送モードのサポート     |   必須    |
|  RetailProductAvailabilityOptimizationFeature |   最適化された製品可用性の計算  |  必須 |
|   RetailPricingDataManagerV2Feature   |   Commerce 価格決定エンジンのパフォーマンスを向上 |   必須 |
|  RetailPricingPreventUnintendedRecalculationFeature   | 意図しない商取引注文の価格計算を禁止する    |  必須  |
| RetailTeamsIntegration    |   Microsoft Teams の統合の有効化| 必須   |  
| ConsumerEFDSyncProcessFeature_BR | (ブラジル) NFC-e 同期処理 | 既定で有効 |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | 会計統合フレームワークの内部および外部コネクタのサポート | 必須 |
| RetailTaxRegistrationIdEnableFeature_BR | (ブラジル) 税務登録番号によって Retail POS で顧客を検索します | 必須 |
| RetailTaxRegistrationIdEnableFeature_IN | (インド) 税務登録番号によって Retail POS で顧客を検索します | 必須 |
| RetailTaxRegistrationIdEnableFeature_IT | (イタリア) Retail POS での顧客情報管理 | 必須 |
| RetailTaxRegistrationIdEnableFeature_PL | (ポーランド) Retail POS での顧客情報管理 | 必須 |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (インドの商品及びサービス税) 元の請求書への参照を含む訂正票を更新します | 必須 |
| RetailUserDefinedCertificateProfileFeature | 小売店舗のユーザー定義の証明書プロファイル | 必須 |
  

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Commerce 10.0.29 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.29 のプラットフォーム更新プログラム (2022 年 10 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). を参照してください。 

### <a name="bug-fixes"></a>バグ修正

バージョン 10.0.29 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c) を参照してください。 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2022wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
