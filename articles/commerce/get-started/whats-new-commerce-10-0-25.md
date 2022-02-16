---
title: Dynamics 365 Commerce 10.0.25 の機能のプレビュー (2022 月 4 月)
description: このトピックでは、Dynamics 365 Commerce 10.0.25 の新機能または変更された機能について説明します。
author: josaw1
ms.date: 01/31/2021
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
ms.openlocfilehash: 5ef59deaef2394ed9352c1f942a6909c0d670e3a
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087651"
---
# <a name="preview-features-in-dynamics-365-commerce-10025-april-2022"></a>Dynamics 365 Commerce 10.0.25 の機能のプレビュー (2022 月 4 月)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 10.0.25 の新機能または変更された機能について列挙します。 このバージョンのビルド番号は 10.0.1149 で、次のスケジュールで使用できます。

- **リリースのプレビュー**: 2022 年 1 月
- **リリースの一般提供 (自己更新)**: 2022 年 3 月
- **リリースの一般提供 (自動更新)**: 2022 年 4 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。 機能を有効にする方法を確認するには、*有効化* 列を参照してください。 機能管理の使用方法の詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。 このトピックが最初に公開された後に、ビルドに加えた機能を含めるために、このトピックを更新することがあります。

| 機能領域   | フィーチャー                                                  | 詳細                                          |   に  によって有効化             |
|----------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| B2B | サインインした B2B ユーザーをモックする | [ローカル開発中にサインイン状態をモックする](../e-commerce-extensibility/mock-sign-in.md) | 開発者のオプトイン | 
| E コマース | [サイトコア コンテンツ ハブとの統合](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/integration-sitecore-content-hub) | データ コネクタは、Dynamics 365 Commerce の製品とカテゴリのデータをサイトコア コンテンツ ハブ インスタンスに自動的にプッシュし、Commerce チャネルの追加のデジタル資産管理と製品強化オプションを可能にします。 | サイト ビルダー |
| E コマース | [eコマースでの PayPal カート チェックアウト サポート](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/paypal-cart-checkout-support-e-commerce) | [PayPal 向け Dynamics 365 Payment Connector](../paypal.md)| 開発者のオプトイン |
| E コマース | [価格に売上税が含まれる場合の eコマースの税内訳の表示/非表示](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/show-or-hide-tax-breakdown-e-commerce-when-prices-include-sales-tax) |  企業では、eコマース チャネルのカート、チェックアウト、確認、および注文の詳細ページの注文集計で、税金情報を明示的に表示または非表示にできます。 | サイト ビルダー |
| グローバリゼーション | [POS からの直接会計統合](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/direct-fiscal-integration-pos) | [コマース チャネルの会計統合の概要](../localizations/fiscal-integration-for-retail-channel.md) | 開発者のオプトイン| 
| グローバリゼーション | [拡張会計コネクタ構成](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/enhanced-fiscal-connector-configuration) | [コマース チャネルの会計統合の概要](../localizations/fiscal-integration-for-retail-channel.md) | 開発者のオプトイン| 
| グローバリゼーション | インドの QR コードの参照を更新 | [インド向け QR コードの生成とレシートへの印刷](../localizations/ind-generate-qr-code-print-receipt.md) | 開発者のオプトイン|
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

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)トピックでは、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
