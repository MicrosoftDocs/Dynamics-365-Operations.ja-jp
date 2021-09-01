---
title: Finance and Operations アプリ バージョン 10.0.20 のプラットフォーム更新プログラム (2021 年 8 月)
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.20 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4b30be719f15dc906ad4d8128e8a441b5afdb93e9e4dbddce2d93676a5035219
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720664"
---
# <a name="platform-updates-for-version-10020-of-finance-and-operations-apps-august-2021"></a>Finance and Operations アプリ バージョン 10.0.20 のプラットフォーム更新プログラム (2021 年 8 月)

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.20 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6060 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 5 月
- **リリースの一般提供 (手動更新):** 2021 年 7 月
- **リリースの一般提供 (自動更新):** 2021 年 7 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。 

| 機能領域   | 機能                                                  | 詳細                                                                    |
|----------------|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| システム管理 | [Internet Explorer サポート終了通知](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/internet-explorer-end-of-support-notifications)| [クラウド配置のシステム要件](../../fin-ops/get-started/system-requirements.md)</br></br>[オンプレミス配置のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md) |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース
次のヘルプ トピックが最近追加されたか大幅に更新されました。 前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りませんが、既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新されたトピック |
|--------------|-----------------------|
| Power Platform 統合 | [Finance and Operations アプリと Microsoft Power Platform の統合](../power-platform/overview.md)<br>[仮想エンティティの概要](../power-platform/virtual-entities-overview.md)<br>[アドインの概要](../power-platform/add-ins-overview.md)<br>[二重書き込みの新機能および変更された機能](../data-entities/dual-write/whats-new-dual-write.md)<br>[Lifecycle Services からの二重書き込みの設定](../data-entities/dual-write/lcs-setup.md)<br>[ユーザー指定のチームの所有者](../data-entities/dual-write/user-specified-team-owner.md)<br>[既存 Finance and Operations アプリの二重書き込みを有効化](../data-entities/dual-write/enable-dual-write.md)<br>[二重書き込みウィザードを使用して環境をリンクする](../data-entities/dual-write/link-your-environment.md) |
| Office 統合 | [Microsoft Office で開くメニューのカスタマイズ](../office-integration/customize-open-office-menu.md) |
|  データベース| [サンドボックス環境への生産データベースのポイントインタイム復元](../database/database-pitr-prod-sandbox.md)<br>[データベース ポイントインタイム復元 (PITR)](../database/database-point-in-time-restore.md)<br>[データベースの更新](../database/database-refresh.md)<br>[ゴールデン コンフィギュレーション プロモーション](../database/dbmovement-scenario-goldenconfig.md) |
| ユーザーの生産性| [カスタム フィールドの作成と操作](../../fin-ops/get-started/user-defined-fields.md)<br>[保存されているビュー](../../fin-ops/get-started/saved-views.md)<br>[ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md) |
| セルフサービス配置   | [セルフサービス環境の計画メンテナンスに関する FAQ](../deployment/plannedmaintenance-selfservice.md)  |
| オンプレミス配置| [オンプレミス環境の設定と配置 (Platform update 41 以降)](../deployment/setup-deploy-on-premises-pu41.md) |
| Lifecycle Services (LCS) | [Lifecycle Services (LCS) のアセット ライブラリ](../lifecycle-services/asset-library.md) |
| 開発| [ISV Studio を使用した ISV パッケージからの X++ モジュールのリンク](../dev-tools/isv-studio-solutions.md) |
| 削除済みまたは非推奨の機能 | [以前のリリースの削除済みまたは非推奨の機能](../migration-upgrade/deprecated-features.md) |


## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8) を参照してください。

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2021wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
