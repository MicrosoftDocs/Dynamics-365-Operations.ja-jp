---
title: Finance and Operations アプリ (2021 年 11 月) のバージョン 10.0.22 のプラットフォーム更新プログラム
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.22 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 12/01/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2021-08-31
ms.openlocfilehash: fc5bb858a952cace54c9753448e5a9725c7a9b55
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883834"
---
# <a name="platform-updates-for-version-10022-of-finance-and-operations-apps-november-2021"></a>Finance and Operations アプリ (2021 年 11 月) のバージョン 10.0.22 のプラットフォーム更新プログラム

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.22 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6164 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 9 月
- **リリースの一般提供 (手動更新):** 2021 年 10 月
- **リリースの一般提供 (自動更新):** 2021 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features)を参照してください。

| 機能領域    | フィーチャー | 詳細 |  に  によって有効化|
|-----------------|---------|------------------|---------------------------|
| クライアント機能 | [オープンソース ソフトウェア更新 – Moment のアップグレードと jQWidgets の削除](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/open-source-software-update-upgrade-moment-remove-jqwidgets)| 該当なし | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| クライアント機能 | [新しいカラー ピッカー コントロール](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/new-color-picker-control) | 該当なし | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| クライアント機能 | <p>**階層ビューアー コントロールへの視覚的な更新**</p><p>特に 400% ズーム シナリオでは、アクセシビリティを向上させるために HierarchyViewer コントロールに変更が加えられました。 これらの変更には、すべてのズーム レベルでのコントロールの可読性を高めるために、コントロールを再スタイルして Fluent デザイン言語で合わせることが含まれます。 | [HierarchyViewer コントロール](../user-interface/hierarchy-viewer-control.md) | 既定 |
| バッチ処理 | <p>**バッチ OData API**</p><p>バッチ機能により、バッチ ジョブを再キューするために使用できる Open Data Protocol (OData) アプリケーション プログラミング インターフェイス (API) が公開されるようになりました。 顧客は、OData エンドポイントを使用して、ターミナル状態にあるバッチ ジョブを再キューできます。 この機能は、Microsoft Power Automate、カスタム API その他を使用することで任意の自動化と統合できます。 | [バッチ OData API](../sysadmin/batch-odata-api.md) | 既定 |
| Microsoft Power Platform 統合 | <p>Microsoft Power Platform 統合で新しいシナリオが有効になります。 次にいくつか例を挙げます。</p><ul><li>統合の設定</li><li>二重書き込みおよび仮想エンティティの自動設定</li><li>合理化されたユーザー設定</li><li>Finance and Operations アプリ ビジネス イベントおよび Microsoft Dataverse のデータ イベント</li><li>改善された開発ツール</li><li>強化されたアドイン エクスペリエンス</li></ul> | [Power Platform 収束性により有効化された新しいシナリオ](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/new-scenarios-enabled-power-platform-convergence) | 既定 |
| Power BI |  Power BI embedded および Power BI.com 統合は、10.0.22 リリースの一部としてアップグレードされ、最新の Power BI Desktop リリースと互換性があります。 この変更により、ユーザーはワークスペース レポートの編集時に Power BI Desktop の最新バージョンを使用できるようになりました。 これはインフラストラクチャの変更であり、環境がリリース 10.0.22 にアップグレードされると自動的に行われます。    | [PowerBI.com 統合の構成](../analytics/configure-power-bi-integration.md)<br><br>[Power BI Desktop を使用した分析レポートの作成](../analytics/author-distribute-power-bi-reports.md) | 既定 |


## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) を参照してください。

### <a name="dynamics-365-2021-release-wave-2-plan"></a>Dynamics 365: 2021 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
