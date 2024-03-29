---
title: Dynamics 365 Commerce 10.0.23 (2022 年 1 月) の新機能と変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.23 のプレビュー リリースの新機能または変更された機能について説明します。
author: josaw1
ms.date: 04/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 4d757ee7443b447be3f0906f2875b8b757cd022d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065445"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10023-january-2022"></a>Dynamics 365 Commerce 10.0.23 (2022 年 1 月) の新機能と変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 10.0.23 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.1037 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 10 月
- **リリースの一般提供 (セルフ更新)**: 2021 年 12 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。 機能を有効にする方法を確認するには、次のテーブルで **有効化** 列を参照してください。 機能管理の使用方法の詳細については、[機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を参照してください。

| 機能領域   | フィーチャー                                                  | 詳細                                          |   に  によって有効化             |
|----------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Dynamics 365 Sales の統合 |   Dynamics 365 Sales を活用して、Commerce の企業間 (B2B) サイトから生成された見込み客を管理します。  | Commerce B2B Webサイトに対するビジネス パートナーの承認を管理するには、Sales を使用します。 Sales ソリューションに既に投資している組織は、B2B の e コマースのビジネス パートナー承認プロセスに対して、その潜在顧客と営業案件の概念を使用できます。 [Dynamics 365 Sales を使った B2B e コマース Web サイトでビジネス パートナー ユーザーを管理する](../b2b/prospect-management-sales.md) を参照してください。 | アプリのソースを使用する  |
|  グローバル アドレス帳| 住所の設定で国/地域ごとに既定の都道府県を定義する | グローバル アドレス帳の住所設定で国/地域ごとに既定の都道府県を定義できるようになりました。 既定の都道府県が設定されている場合は、その国/地域に新しい郡または市のレコードが作成される際、それが都道府県フィールドに入力された規定値になります。 詳細については、[住所の設定](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md)を参照してください。 | 既定で有効 |
|   グローバリゼーション |  [(インド) e コマースの GST](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/gst-e-commerce-india)    |  この機能により、インドの Dynamics 365 Commerce 顧客は、商品及びサービス税 (GST) が e コマース注文で計算されるよう確認することで、e コマース機能を実装できます。 詳細については、[インド向け e コマース サイトの商品及びサービス税 (GST) 統合](../localizations/apac-ind-e-commerce.md)を参照してください。  |  機能管理  |
|   グローバリゼーション |   (東ヨーロッパ) 小売明細書に対する売上請求書および支払の決済の改善   |  この機能により、小売明細書から生成された売上請求書および支払の自動決済を正常に行います。 この機能は、チェコ共和国、エストニア、ハンガリー、ラトビア、リトアニア、ポーランド、ロシアに適用されます。   |  既定で有効  |
|   販売促進 |   [フラット化された割引テーブルを使用して改善された価格決定の計算パフォーマンス](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/improved-pricing-computation-performance-using-flattened-discount-tables)   |   [小売割引](../retail-discounts-overview.md)  |  機能管理 (*フラット化された割引テーブル機能を使用して割引の計算パフォーマンスを向上させます。*)  |
|   Office 統合  |   トランザクション イベント用の電子メール テンプレートの作成  |  [トランザクション イベント用の電子メール テンプレートの作成](../email-templates-transactions.md)   | 既定で有効  |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.23 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.23 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874) を参照してください。

Commerce 固有の重大な変更を加える場合は、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください。

### <a name="dynamics-365-2021-release-wave-2-plan"></a>Dynamics 365: 2021 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

