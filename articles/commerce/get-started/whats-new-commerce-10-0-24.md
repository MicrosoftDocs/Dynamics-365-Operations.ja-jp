---
title: Dynamics 365 Commerce 10.0.24 の新機能および変更された機能 (2022 年 2 月)
description: この記事では、Dynamics 365 Commerce 10.0.24 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-12-31
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e662e3afe0b74e053cac9e88203662021fb7f1c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894486"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10024-february-2022"></a>Dynamics 365 Commerce 10.0.24 の新機能および変更された機能 (2022 年 2 月)

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 10.0.24 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.1084 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 12 月
- **リリースの一般提供 (手動更新):** 2022 年 1 月
- **リリースの一般提供 (自動更新):** 2022 年 2 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。 機能を有効にする方法を確認するには、*有効化* 列を参照してください。 機能管理の使用方法の詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域   | フィーチャー                                                  | 詳細                                          |   に  によって有効化             |
|----------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
|  B2B         | PDP および簡易注文入力ページでの製品バリアントのマトリックス ビューをサポートしています。        | [B2B eコマース サイトの設定](../b2b/set-up-b2b-site.md)            | サイト ビルダー |
|  在庫   |  [POS の在庫棚卸操作の改善](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/improved-stock-count-operation-pos)  | この機能により、POS アプリの在庫棚卸操作に対するいくつかの機能およびエクスペリエンス拡張機能が導入されます。  | 機能管理<p>*POS の在庫棚卸操作の改善*  |
| 支払 | [POS での集荷注文処理に対する支払フローの改善](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/improvements-payment-flows-pick-up-order-processing-pos) | [店舗内での受取に使用できる複数の支払方法](../dev-itpro/multiple-payments-pickup.md) | 機能管理<p>*オムニ チャネル支払* |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次のテーブルは、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能のいずれかをオンまたはオフにする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で次のテーブルの *機能管理の機能名* 列に示されている名前を使用してリストする必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 顧客管理  | 顧客の拡張非同期作成を有効にする  | この機能により、非同期モードで顧客を作成する際に、タイトル、所属、および二次連絡先情報の収集が可能になります。  詳細については、[顧客作成モードを非同期化する](../async-customer-mode.md)を参照してください。 |
| 本社の設定   |  本社の更新後に "コマース スケジューラの初期化" を実行する |  [Commerce Data Exchange ベスト プラクティス](../dev-itpro/cdx-best-practices.md) |


## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.24 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.24 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f) を参照してください。

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
