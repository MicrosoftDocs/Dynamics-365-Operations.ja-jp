---
title: Finance and Operations アプリ バージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.21 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 09/13/2021
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
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 02456e4875d4f579d35974bdbef536fbd99db7f7
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487977"
---
# <a name="platform-updates-for-version-10021-of-finance-and-operations-apps-october-2021"></a>Finance and Operations アプリ バージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.21 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6129 で、次のスケジュールで使用できます。

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

使用する前に、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)を使用して一部の機能を有効にする必要があります。

| 機能領域   | フィーチャー                                                  | 詳細                                                                    |
|----------------|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| クライアント機能 | [保存したビューに対する法人サポートの改善](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/improved-legal-entity-support-saved-views)  | [保存されているビュー](../../fin-ops/get-started/saved-views.md) |
| システム管理 | [機能管理の完全な機能ライフサイクルに対する強化されたサポート](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/enhanced-support-full-feature-lifecycle-feature-management)| [機能管理の概要](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| 可用性の監視 | **可用性の問題に対する強化された自動監視**<br><br>Microsoft は、統合的な監視を通じて、API モニターを継続的に監視し、顧客が自身で問題を見つける前に API 問題を事前に可視化できるようになります。 この追加により、ビルドアウト展開を検証する調査の設定、サービス展開サイクルに依存しないサービス/シナリオの監視、依存関係の可用性テストなど、特定のシナリオでのエンド ツー エンド補充ができます。 <br><br> 顧客は、Azure Active Directory アプリケーション (監視アプリ)、Microsoft 管理のユーザー アカウント (アプリ ユーザーの監視)、アプリ ユーザーを監視するためのセキュリティ ロールとセキュリティ職務権限、OData エンティティ (/data/SysMonDatas) など、一部の新しい要素が環境に追加されたことがわかります。 <br><br>必要な唯一のアクション項目は、可用性の監視が意図したとおりに機能するよう、これらの任意の要素を削除または変更してはならない点です。 | 適用できません | 
| 開発者ツール | Visual Studio 2019 が正式にサポートされるようになりました。 | [Visual Studioの開発ツール](../dev-tools/development-tools-overview.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166) を参照してください。

### <a name="dynamics-365-2021-release-wave-2-plan"></a>Dynamics 365: 2021 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
