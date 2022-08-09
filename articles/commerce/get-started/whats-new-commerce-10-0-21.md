---
title: Dynamics 365 Commerce 10.0.21 (2021 年 10 月) の新機能と変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.21 のプレビュー リリースの新機能または変更された機能について説明します。
author: josaw1
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-08-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 7936ce901789f3f5b4f4b53dcfbfc3be3941ac40
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069952"
---
# <a name="whats-new-and-changed-in-dynamics-365-commerce-10021-october-2021"></a>Dynamics 365 Commerce 10.0.21 (2021 年 10 月) の新機能と変更された機能

[!include [banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 Commerce 10.0.21 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.960 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 8 月
- **リリースの一般提供 (手動更新):** 2021 年 9 月
- **リリースの一般提供 (自動更新):** 2021 年 10 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

| 機能領域   | フィーチャー                                                  | 詳細                                                                    |
|----------------|----------------------------------------------------------|-------------------------------------------------------------------------------------|
|  B2B           |   [B2B e コマース ビジネス パートナー ユーザー管理者権限の付与と取り消し](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/grant-revoke-b2b-e-commerce-business-partner-user-admin-privileges)    |   [B2B eコマース Web サイトでのビジネス パートナー ユーザーの管理](../b2b/manage-b2b-users.md)   |
|  B2B          |  [e コマースチャネルのカタログのサポート](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/support-catalogs-e-commerce-channel)   |  パートナーと交渉した製品および特別価格を反映する、パートナー固有のカタログを作成します。   |
|  配置   |   Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用  |  [Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/Update-retail-channel.md)     |
| E コマース   |   [e コマースの再注文に関する拡張エクスペリエンス](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/enhanced-reordering-experience-e-commerce)  |   この機能により、e コマース サイトの既存の再注文 (「再購入」) の機能が拡張されます。   |
|  拡張性  |  Cloud Scale Unit 拡張機能の削除   |  [Cloud Scale Unit 拡張機能の削除](../dev-itpro/retail-sdk/remove-csu-package.md)      |
|  グローバリゼーション  |   [ロシア向け Commerce ローカライズ](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/commerce-localization-russia)       |   [ロシア向け Commerce ローカライズ](../localizations/rus-commerce-localization.md)には、ロシアにおける Dynamics 365 Commerce の実装に必要不可欠な機能が含まれます。  |
|  グローバリゼーション  |   (ブラジル) 臨時に完了した売上のキャンセルと返品       |   これで、NFC-e 代替モードで完了した販売トランザクションに対して返品やキャンセルの作成ができるようになりました。 詳細については、[ブラジル向け Commerce POS の NFC-e ドキュメントのキャンセルと返品](../localizations/latam-bra-nfce-cancel-return.md)を参照してください。  |
|   販売促進   |  見本の在庫認識  |  [製品分析コード値を見本として表示するように構成する](../dev-itpro/dimensions-swatch.md)    |
|  パフォーマンス  | [パフォーマンスへの影響による、小売トランザクション テーブルに対するカスタム クエリ変更追跡コンフィギュレーションの適用](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/enforce-custom-query-change-tracking-configurations-retail-transaction-tables-due-performance-impacts)   | この機能により、小売トランザクション テーブルで変更追跡機能とデータ管理エクスポート フレームワークを組み合わせて使用すると、Commerce のパフォーマンスが向上します。  |
|  販売時点管理 (POS)  |  意図しない商取引注文の価格計算を禁止する     |  [販売時点管理 (POS) の顧客注文](../customer-orders-overview.md)           |
|  販売時点管理 (POS)  |   [POS による店舗内の場所での在庫移動のサポート](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/support-inventory-movement-between-in-store-locations-pos)   |  POS から直接、店舗内の場所での在庫移動を有効にできます。   |
| 販売時点管理 (POS) オフライン   |   Modern POS オフライン監視ダッシュボード、シームレスなオフライン弾力性、および信頼性の向上   |   この機能セットは、10.0.20 リリースに追加でバックポートされています。  [Commerce のオフライン データベースの実装とトラブルシューティング](../dev-itpro/implementation-considerations-offline.md)  |
|   ターゲット設定   |  [顧客区分とターゲット接地](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/customer-segmentation-targeting)  |  [デバイス、市場、および位置情報のターゲット設定](../targeting-overview.md)    |

## <a name="features-turned-on-by-default-in-this-release"></a>このリリースで、既定で有効になる機能

次の表に、10.0.21 で既定で有効になる機能の一覧を示します。 有効にした機能のほとんどは [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) でオフにできます。

| 機能名 | 日付を有効にする | 機能の追加日 | 機能状態 |
| :--- | :--- | :--- | :--- |
| (インド) 税務登録番号によって Retail POS で顧客を検索します | 2021/9/1 | 2019/8/31 | 既定で有効 |
| (インドの商品及びサービス税) 元の請求書への参照を含む訂正票を更新します | 2021/9/1 | 2019/6/3 | 既定で有効 |
| (イタリア) Retail POS での顧客情報管理 | 2021/9/1 | 2019/10/7 | 既定で有効 |
| (ポーランド) Retail POS での顧客情報管理 | 2021/9/1 | 2019/12/19 | 既定で有効 |
| 意図していないコマース注文の価格計算を防止します。 | 2021/9/1 | 2021/9/1 | 既定で有効 |
| 受領書の電子メールの値が既定の顧客から新しい顧客にコピーされないようにします。 | 2021/9/1 | 2021/9/1 | 既定で有効 |
| 小売店舗のユーザー定義の証明書プロファイル | 2021/9/1 | 2020/9/30 | 既定で有効 |
| 会計統合フレームワークの内部および外部コネクタのサポート | 2021/9/1 | 2020/6/24 | 既定で有効 |


## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.21 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.21 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de) を参照してください。

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

