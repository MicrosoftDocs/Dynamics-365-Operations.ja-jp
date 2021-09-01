---
title: Dynamics 365 Commerce 10.0.21 の機能のプレビュー (2021 年 10 月)
description: このトピックでは、Dynamics 365 Commerce 10.0.21 のプレビュー リリースの新機能または変更された機能について説明します。
author: josaw1
ms.date: 08/02/2021
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
ms.openlocfilehash: 744c76e064f735e9d39751bc0731440bc6378b1a
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345106"
---
# <a name="preview-features-in-in-dynamics-365-commerce-10021-october-2021"></a>Dynamics 365 Commerce 10.0.21 の機能のプレビュー (2021 年 10 月)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 10.0.21 の新機能または変更された機能について列挙します。 このバージョンのビルド番号は 10.0.960 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 8 月
- **リリースの一般提供 (手動更新):** 2021 年 9 月
- **リリースの一般提供 (自動更新):** 2021 年 10 月

## <a name="known-deployment-issue"></a>配置に関する既知の問題
IaaS にリリース 10.0.21 を配置する場合、次のような配置警告が表示される場合があります。

**警告コード:** 95017

**警告メッセージ:** スクリプト [SetupDiagnostics] が VM に対して実行に失敗

警告があっても配置は機能しますが、Lifecycle Services (LCS) では次のような既知の問題が発生する可能性があります。

-   **環境の監視** ページでは、**詳細バージョン情報の表示** リンクは表示されません。したがって、環境にインストールされているモジュールの特定のバージョンは表示されません。 このデータがないと、修正プログラムを適用するプロセスがこのデータを使用して、モジュール バージョンの前提条件が満たされていることを確認するため、後続の修正プログラムが失敗することがあります。 PEAP/プレビュー ビルドを生産で使用したり、修正プログラムを適用することができないため、影響は最小限に抑える必要があります。
-   SQL インサイトの **環境監視** ページの **パフォーマンス メトリックス** タブと **インデックス分析** タブでは、データは表示されません。 その他の **環境監視** 機能は、意図したとおりに機能します。
-   **フル システム診断** ページにはアクセスできません。 夜間のコレクター実行のステータスとそのルールによって検出された問題に関する関連データも表示されません。


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

| 機能領域   | フィーチャー                                                  | 詳細                                                                    |
|----------------|----------------------------------------------------------|-------------------------------------------------------------------------------------|
|  B2B           |   [B2B e コマース ビジネス パートナー ユーザー管理者権限の付与と取り消し](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/grant-revoke-b2b-e-commerce-business-partner-user-admin-privileges.md)    |   [B2B eコマース Web サイトでのビジネス パートナー ユーザーの管理](../b2b/manage-b2b-users.md)   |
|  B2B          |  [e コマースチャネルのカタログのサポート](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/support-catalogs-e-commerce-channel.md)   |  パートナーと交渉した製品および特別価格を反映する、パートナー固有のカタログを作成します。   |
|  配置   |   Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用  |  [Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/Update-retail-channel.md)     |
|  拡張性  |  Cloud Scale Unit 拡張機能の削除   |  [Cloud Scale Unit 拡張機能の削除](../dev-itpro/retail-sdk/remove-csu-package.md)      |
|  販売時点管理 (POS)  |  意図しない商取引注文の価格計算を禁止する     |  [販売時点管理 (POS) の顧客注文](../customer-orders-overview.md)           |
|  販売時点管理 (POS)  |   [POS による店舗内の場所での在庫移動のサポート](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/support-inventory-movement-between-in-store-locations-pos.md)   |  POS から直接、店舗内の場所での在庫移動を有効にできます。   |
|  グローバリゼーション        |   ロシア向け Dynamics 365 Commerce での前払            |  [ロシア向け Dynamics 365 Commerce での前払](../localizations/rus-commerce-prepayments.md)   |
|  グローバリゼーション  |   ロシア向け Dynamics 365 Commerce ローカライズの設定       |   [ロシア向け Dynamics 365 Commerce ローカライズの設定](../localizations/rus-commerce-setup.md)  |
|   販売促進   |  見本の在庫認識  |  [製品分析コード値を見本として表示するように構成する](../dev-itpro/dimensions-swatch.md)    |
|   ターゲットを設定する   |  [顧客区分とターゲット接地](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/customer-segmentation-targeting.md)  |  [デバイス、市場、および位置情報のターゲット設定](../targeting-overview.md)    |
|  業績  | [パフォーマンスへの影響による、小売トランザクション テーブルに対するカスタム クエリ変更追跡コンフィギュレーションの適用](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/enforce-custom-query-change-tracking-configurations-retail-transaction-tables-due-performance-impacts.md)   | この機能により、小売トランザクション テーブルで変更追跡機能とデータ管理エクスポート フレームワークを組み合わせて使用すると、Commerce のパフォーマンスが向上します。  |
| E コマース   |   [e コマースの再注文に関する拡張エクスペリエンス](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/enhanced-reordering-experience-e-commerce.md)  |   この機能により、e コマース サイトの既存の再注文 (「再購入」) の機能が拡張されます。   |


## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.21 には、プラットフォーム更新プログラムが含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.21 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de) を参照してください。

Commerce 固有の重大な変更を加える場合は、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください。

### <a name="dynamics-365-2021-release-wave-2-plan"></a>Dynamics 365: 2021 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)トピックでは、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]