---
title: Dynamics 365 Commerce 10.0.20 (2021 年 8 月) の新機能と変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.20 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 05/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ce9889da9720556b52ccf2369eb55aba21128af7
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069614"
---
# <a name="whats-new-and-changed-in-dynamics-365-commerce-10020-august-2021"></a>Dynamics 365 Commerce 10.0.20 (2021 年 8 月) の新機能と変更された機能

[!include [banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 Commerce 10.0.20 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.886 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 5 月
- **リリースの一般提供 (手動更新):** 2021 年 7 月
- **リリースの一般提供 (自動更新):** 2021 年 7 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

| 機能領域   | 機能                                                  | 詳細                                                                    |
|----------------|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| 製品分析コード |  Commerce 本社で製品の分析コード値を見本として構成します。  |  [製品の分析コード値を見本として表示する設定](../dev-itpro/dimensions-swatch.md)|
| 製品分析コード |  Commerce 本社での表示設定を構成します。 |  [製品の分析コードの表示設定を適用する](../dimension-settings.md) |
| 販売時点管理 (POS) | 販売時点管理 (POS) でシリアル番号管理された製品の返品 | [販売時点管理 (POS) でシリアル番号管理された製品の返品](../pos-serial-returns.md)|
| 販売時点管理 (POS) | 販売時点管理 (POS) での返品の作成 | [販売時点管理 (POS) での返品の作成](../pos-returns.md) |
| 販売時点管理 (POS) | [Chromium レンダリング エンジンおよび統合されたハードウェア サポートを含む Store Commerce アプリ](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/store-commerce-app-chromium-rendering-engine-integrated-hardware-support)  |  [Microsoft Dynamics 365 Commerce での Store Commerce アプリ (プレビュー)](../dev-itpro/store-commerce.md)  |
| 販売時点管理 (POS)  | [POS からの在庫調整のサポート](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/support-inventory-adjustments-pos)  |   POS を使用して、在庫の出し入れの調整を行います。 |
| 支払利息  | [ウォレット スタイルの支払方法の初期設定サポート](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/out-of-box-support-wallet-style-payment-methods)  | [Wallet 支払サポート](../wallets.md) |
|  支払利息 |  [店頭チェックアウトでのリファクターされた支払処理](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/refactored-payment-processing-storefront-checkout)  | この機能により、支払プロセッサへの認証要求数が減少し、欧州連合の強力な顧客認証 (SCA) へのより良いサポートが追加されます。 |
| E コマース  |  [ゲスト顧客の注文の検索を有効にする](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/enable-order-lookup-guest-customers)   | この機能は、ゲスト チェックアウトの注文の検索を有効にします。 |
|   E コマース|  [在庫を認識するように強化された e コマース製品の検出](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/enhanced-e-commerce-product-discovery-be-inventory-aware)  | [在庫設定の適用](../inventory-settings.md)<br>[検索結果モジュール](../search-result-module.md) | 
| E コマース  |  [E コマースの在庫状態検索の API に対する拡張機能](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/enhancements-e-commerce-inventory-availability-lookup-apis)  |  この機能によって、GetEstimatedAvailability API および GetEstimatedProductAvahouseAvailability API に拡張機能が提供されます。  |
|  E コマース   |   [最新の e コマース サイトを表示するための没入型テーマ](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/immersive-theme-showcase-modern-e-commerce-site)   | この新しいテーマを使用して、e コマース サイトで最新かつ没入型のエクスペリエンスを構築します。 |
| グローバリゼーション |  [ブラジル向け Adyen 支払コネクタ](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/adyen-payment-connector-brazil)    |  ブラジルにある店舗での支払操作をサポートするには、Adyen 向け Dynamics 365 支払コネクタを使用します。 | 
|  グローバリゼーション |   [ブラジル向けの SAT 統合](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/sat-integration-brazil)  |  この機能は、ハードウェア ステーションに接続された、SAT (Sistema Autenticeleticelesor de Cupons Fiscais Eletrautros) デバイスでの小売販売の会計登録を有効にします。 | 
| グローバリゼーション | 特定の Commerce 機能が有効な場合、Commerce サイト ビルダーのグローバル構成プロパティを表示、非表示、または無効にすることができます。  | [有効な機能に基づくサイト ビルダーのグローバル構成設定のコンフィギュレーション](../e-commerce-extensibility/config-settings-for-features.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.20 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.20 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8) を参照してください。

Commerce 固有の重大な変更を加える場合は、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください。

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2021wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

