---
title: Dynamics 365 Commerce 10.0.25 (2022 年 4 月) の新機能および変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.25 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 04/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 99219520f7d1d821351b56afacc5432c35d2e7a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906714"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10025-april-2022"></a>Dynamics 365 Commerce 10.0.25 (2022 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 10.0.25 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.1149 で、次のスケジュールで使用できます。

- **リリースのプレビュー**: 2022 年 1 月
- **リリースの一般提供 (自己更新)**: 2022 年 3 月
- **リリースの一般提供 (自動更新)**: 2022 年 4 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。 機能を有効にする方法を確認するには、*有効化* 列を参照してください。 機能管理の使用方法の詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域   | フィーチャー                                                  | 詳細                                          |   に  によって有効化             |
|----------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| POS | [Store Commerce アプリ](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/store-commerce-app-chromium-rendering-engine-integrated-hardware-support) | Commerce での Store Commerce アプリは、物理店舗に対する次世代の提供です。 Modern 販売時点管理 (MPOS) とクラウド販売時点管理 (CPOS) を 1 つのアプリケーションに統合して小売業者の配置の選択肢を提供し、パフォーマンスを向上させ、より優れたアプリケーション ライフサイクル管理 (ALM) を提供します。 また、拡張機能を含め、MPOS および CPOS のすべての機能が保持されます。 [Store Commerce アプリ](../dev-itpro/store-commerce.md) を参照してください。 |オプトイン | 
| POS  | [POS 在庫操作での追加フィルター オプションのサポート](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/additional-filter-options-pos-inventory-operations) |  この機能により、POS 在庫操作間で一般に要求される追加フィルター オプションがサポートされます。これにより、不必要な拡張機能が削除され、店舗在庫操作の効率が大幅に向上します。 | 機能管理<p>*POS 在庫操作の追加のフィルター オプション* |
| B2B | サインインした B2B ユーザーをモックする | [ローカル開発中にサインイン状態をモックする](../e-commerce-extensibility/mock-sign-in.md) | 開発者のオプトイン | 
| E コマース | [サイトコア コンテンツ ハブとの統合](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/integration-sitecore-content-hub) | データ コネクタは、Dynamics 365 Commerce の製品とカテゴリのデータをサイトコア コンテンツ ハブ インスタンスに自動的にプッシュし、Commerce チャネルの追加のデジタル資産管理と製品強化オプションを可能にします。 | サイト ビルダー |
| E コマース | [eコマースでの PayPal カート チェックアウト サポート](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/paypal-cart-checkout-support-e-commerce) | [PayPal 向け Dynamics 365 Payment Connector](../paypal.md)| 開発者のオプトイン |
| E コマース | [価格に売上税が含まれる場合の eコマースの税内訳の表示/非表示](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/show-or-hide-tax-breakdown-e-commerce-when-prices-include-sales-tax) |  企業では、eコマース チャネルのカート、チェックアウト、確認、および注文の詳細ページの注文集計で、税金情報を明示的に表示または非表示にできます。 | サイト ビルダー |
| eコマース    | 複数のコンテンツ項目タイプの名前変更 | サイト ビルダーでは、サイト、テンプレート、フラグメント、レイアウトなど、複数のコンテンツ項目タイプの名前の変更がサポートされます。 詳細については、[サイトの名前変更](../create-ecommerce-site.md#rename-your-site)[テンプレートの名前変更](../work-with-templates.md#rename-a-template)[フラグメントの名前変更](../work-with-fragments.md#rename-a-fragment)[ページの名前変更](../add-new-page.md#specify-the-page-name)[レイアウトの名前変更](../work-with-layouts.md#rename-a-preset-layout)[オーディエンスの名前変更](../targeting-overview.md#rename-an-audience-in-site-builder) を参照してください。  |  サイト ビルダー   |
| グローバリゼーション | [POS からの直接会計統合](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/direct-fiscal-integration-pos) | この機能では、POS で実行される会計コネクタを作成する機能を追加することで、会計統合フレームワークを拡張します。 このタイプのコネクタは、HTTP API を提供する会計デバイスまたはサービスと通信し、店舗内でプラグインやデプロイされる専用の物理マシンが不要になります。 詳細については、[コマース チャネルの会計統合の概要](../localizations/fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) および [コネクタ技術プロファイルを作成する ](../localizations/setting-up-fiscal-integration-for-retail-channel.md#create-connector-technical-profiles) を参照してください。 | 機能管理<p>*POS レジスターからの直接会計統合*| 
| グローバリゼーション | [拡張会計コネクタ構成](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/enhanced-fiscal-connector-configuration) | この機能は、ハードウェア プロファイル レベルに加えて、個々の POS レジスター レベルでの会計コネクタの接続設定を定義するオプションを追加することにより、会計統合フレームワークを拡張します。 これにより、店舗内の異なる POS レジスターで使用される個々の会計デバイスまたはサービス インスタンスに対して、異なる接続設定を構成することができます。 詳細については、[コネクタ技術プロファイルを作成する](../localizations/setting-up-fiscal-integration-for-retail-channel.md#create-connector-technical-profiles) を参照してください。 |  機能管理<p>*会計統合技術プロファイルの上書き* | 
|明細書 |  明細書転記機能の改良  | [明細書転記機能の改良](../statement-posting-EOD.md) | コマース パラメーター |



## <a name="additional-resources"></a>追加リソース

### <a name="modernizing-the-commerce-in-store-technology-stack"></a>Commerce の店舗内テクノロジー スタックの近代化

[Dynamics 365 Commerce 店舗内テクノロジー スタックの近代化](https://download.microsoft.com/download/2/2/3/22310579-4b89-4703-becb-9c48aac3cd9c/Modernizing-the-Dynamics-365-Commerce-In-Store-Technology-Stack.pdf) ホワイト ペーパーでは、Commerce の店舗内ソリューションの活用方法、新しい近代化の取り組みについての説明と、顧客やパートナーが新しい Store Commerce アプリおよび Commerce SDK を導入する計画を立て支援する詳細なリリース タイムラインが記述されています。 

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.25 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.25 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580) を参照してください。

Commerce 固有の重大な変更を加える場合は、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください。

### <a name="dynamics-365-2022-release-wave-1-plan"></a>Dynamics 365: 2022 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2022 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
