---
title: Dynamics 365 Commerce 10.0.26 (2022 年 5 月) の新機能および変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.26 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 04/22/2022
ms.topic: article
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-03-31
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 34b08debdfe82fbe4cfaa6c7f3be3d454493945a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070226"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10026-may-2022"></a>Dynamics 365 Commerce 10.0.26 (2022 年 5 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 10.0.26 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.1192 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 3 月
- **リリースの一般提供 (自己更新):** 2022 年 4 月
- **リリースの一般提供 (自動更新):** 2022 年 5 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域   | フィーチャー                                                  | 詳細                                          |   に  によって有効化             |
|----------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
|   グローバリゼーション      |    [ブラジル向け Adyen に対応した Dynamics 365 Payment Connector を使用した分割払い](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/payments-installments-dynamics-365-payment-connector-adyen-brazil)    |   この機能は、Adyen に対応した Dynamics 365 Payment Connector の機能を拡張し、ブラジルへの分割払いをサポートします。 詳細については、[ブラジル向け Commerce POS の Adyen に対応した Dynamics 365 Payment Connector](../localizations/latam-bra-adyen.md) を参照してください。       | 詳細については、[Dynamics 365 の Adyen 支払コネクタの設定](https://docs.adyen.com/plugins/microsoft-dynamics)を参照してください。 |
|   グローバリゼーション      |    [POS と EFR との直接会計統合のサンプル](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/direct-fiscal-integration-pos)    |     この機能では、POS で実行される会計コネクタを作成する機能を追加することで、会計統合フレームワークを拡張します。 このタイプのコネクタは、HTTP API を提供する会計デバイスまたはサービスと通信し、店舗内でプラグインやデプロイされる専用の物理マシンが不要になります。 このリリースでは、[オーストリア](../localizations/emea-aut-fi-sample.md)、[チェコ共和国](../localizations/emea-cze-fi-sample.md)、および[ドイツ](../localizations/emea-deu-fi-sample.md) の POS からの直接会計統合のサンプルが提供されます。   | 機能管理<p>*POS レジスターからの直接会計統合*<p>会計登録プロセスの構成 |
|   グローバリゼーション      |    [選択した POS レジスターの会計登録の無効化](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/enhanced-fiscal-connector-configuration)    |   この機能は、会計登録が有効な店舗で選択した POS レジスターの会計登録を無効にするオプションを追加して、会計年度統合フレームワークを拡張します。 店舗関係者は、非販売操作 (在庫管理操作など) にレジスターを利用したり、売上を作成し、その売上を会計登録が可能なレジスターに反映させたりできるようになります。 詳細については、[会計登録制限を使用したレジスターの設定](../localizations/setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions)を参照してください。 | 機能管理<p>*POS レジスターの会計登録状態* |
|  支払  |   [eコマースでの PayPal カート チェックアウト サポート](/dynamics365-release-plan/2022wave1/commerce/dynamics365-commerce/paypal-cart-checkout-support-e-commerce) | [PayPal 向け Dynamics 365 Payment Connector](../paypal.md)| 開発者のオプトイン |
| Store Commerce |  [Store Commerce は、デュアル ディスプレイをサポートして、カート関連の情報を表示する](../retail-peripherals-overview.md) | デュアル ディスプレイでは顧客向けディスプレイにカート関連の情報が表示され、 [デュアル ディスプレイはカスタム情報を表示するために拡張できます](../dev-itpro/pos-dual-display-extension.md)。| オプトイン |



## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.26 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.26 のプラットフォーム更新プログラム (2022 年 5 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) を参照してください。

Commerce 固有の重大な変更を加える場合は、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

