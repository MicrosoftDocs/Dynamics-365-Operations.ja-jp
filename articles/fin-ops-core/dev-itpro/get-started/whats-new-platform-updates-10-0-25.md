---
title: 財務と運用アプリのバージョン 10.0.25 のプラットフォーム更新プログラム (2022 年 4 月)
description: この記事では、財務と運用アプリのバージョン 10.0.25 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 02/09/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: c072a37daf05911ec8cc4f59bab77f048bbfc6ee
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066148"
---
# <a name="platform-updates-for-version-10025-of-finance-and-operations-apps-april-2022"></a>財務と運用アプリのバージョン 10.0.25 のプラットフォーム更新プログラム (2022 年 4 月)

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのバージョン 10.0.25 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6316 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 1 月
- **リリースの一般提供 (自己更新):** 2022 年 3 月
- **リリースの一般提供 (自動更新):** 2022 年 4 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。

機能管理の使用方法の詳細については、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

| 機能領域    | フィーチャー | 詳細 |  に  によって有効化 |
|-----------------|---------|------------------|---------------------------|
| Web クライアント | **バッチ ジョブの優先度のスケジュール**<br><br>優先順位に基づくスケジューリングではバッチ グループをバッチ サーバーから切り離し、バッチ グループの優先順位を定義できます。<br><br>バッチ ジョブをバッチ サーバーに割り当てる必要はなくなりました。 代わりに、使用可能なバッチサーバー間でタスクが実行される順序を決定するために、業務要件に基づく相対的なスケジューリング優先順位が使用されます。 | [優先順位に基づくバッチスケジューリング](../sysadmin/priority-based-batch-scheduling.md) | 機能管理 (*バッチの優先順位に基づくスケジューリング*) |
| Web クライアント | [垂直方向にスクロールするワークスペース](/dynamics365-release-plan/2022wave1/finance-operations/finance-operations-crossapp-capabilities/vertically-scrolling-workspaces)  | <ul><li>[ワークスペースのフォーム パターン](../user-interface/workspace-form-pattern.md)</li><li>[運用ワークスペースの構築](../user-interface/build-workspaces.md)</li></ul> | 内部ワークスペースが最新の視覚に移行されました。 視覚的な一貫性を維持するには、外部ワークスペースを移行する必要があります。  |
| Web クライアント  | <p>**jQuery UI を1.13.0 にアップグレード**</p><p>この機能は、財務と運用アプリケーションの jQuery ユーザー インターフェイス (UI) をバージョン 1.13.0 (1.12.1 から) にアップグレードします。 この機能を有効にする前に、拡張可能なコントロールまたはカスタム JavaScript コード、特に jQuery UI API を利用するものをテストする必要があります。 この機能は、2022 年秋リリースで必須となることを目標としていますが、影響を受けるAPI の移行に時間をかけるために、現在はオプションです。</p> | | 機能管理<br>(*jQuery UI を 1.13.0 にアップグレード*)|
| Web クライアント  | [ダイアログに対応した保存済みビュー](/dynamics365-release-plan/2022wave1/finance-operations/finance-operations-crossapp-capabilities/updates-saved-views-personalization#view-support-for-dialogs)  | [保存されたビューを十分に活用するフォームの作成](../user-interface/understanding-saved-views.md)  | 機能管理<br>(*ダイアログに対応した保存済みビュー*)  |
| Web クライアント  | [タスク シングル ページとタスク ダブル ページのビューにクエリを保存できるようにする](/dynamics365-release-plan/2022wave1/finance-operations/finance-operations-crossapp-capabilities/updates-saved-views-personalization#queries-on-views-on-task-pages)  | [保存されたビューを十分に活用するフォームの作成](../user-interface/understanding-saved-views.md)  | 機能管理<br>(*タスク シングル ページとタスク ダブル ページのビューにクエリを保存できるようにする*)  |
| Web クライアント  | [(プレビュー) ワークスペースに対応した保存済みビュー](/dynamics365-release-plan/2022wave1/finance-operations/finance-operations-crossapp-capabilities/updates-saved-views-personalization#view-support-for-workspaces)  | <ul><li>[保存されたビューを十分に活用するフォームの作成](../user-interface/understanding-saved-views.md)</li><li>[ユーザー エクスペリエンスのパーソナライズ](../../fin-ops/get-started/personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace)</li></ul>  | 機能管理<br>(*ワークスペースに対応した保存済みビュー*)  |
| Web クライアント  | <p>**グループ化されたグリッドに対する改善された並べ替えサポート**</p><p>ユーザーがグリッド内のデータを 1 つ以上の列でグループ化した場合、グループ化されていない列で並べ替えると、グループ化はそのまま残り、選択した列に基づいて各グループ内のデータが並べ替えられます</p> | [グリッド機能](../../fin-ops/get-started/grid-capabilities.md#sorting-grouped-data) | 機能管理における **グリッド内でのグループ化** 機能の既定値 |
| 開発者ツール | <p>***システムの前に入力する*から個々のグリッドをオプトアウトする**</p><p>新しいグリッドの *システム機能より前に入力する* 方法で、コード パターンが機能しないフォームでは、開発者は非同期行の検証から個々のグリッドを選択し、レガシの同期動作に戻す場合があります。</p> | [グリッド機能](../../fin-ops/get-started/grid-capabilities.md) | 開発者のオプトイン |
| 開発者ツール  | <p>**値が異なる X++ の単体テスト**</p><p>X++ の単体テストでは、SysTestRow 属性を活用して、複数の値が異なるテスト メソッドを再使用できます。</p>  | [複数の値をテストするための SysTestRow 属性](../perf-test/systest-row.md) | 既定   |
| 開発者ツール  | <p>**ダウンタイムなしでカスタム X++ スクリプトの実行**</p><p>この機能を使用すると、Microsoft Dynamics Lifecycle Services (LCS) を経由したり、システムを中断したりせずに、カスタム X ++ スクリプトを含む配置可能パッケージをアップロードして実行できます。 したがって、ダウンタイムが中断することなく、マイナー データの不整合を修正できます。</p> | [ダウンタイムなしでカスタム X++ スクリプトの実行](../deployment/run-custom-scripts.md)  | 既定 |
| 開発者ツール | <p>**保存されたビューはカスタム フィルターをサポートする**</p><p>新しい API は、カスタム フィルターが保存されたビューとシームレスに機能するために使用できます。 具体的には、カスタム フィルターでビュー定義をトリガーして、未保存の変更があるものとしてマークを付けることができます。カスタム フィルター コントロールは、クエリに対するシステムの変更をリッスンして、コントロール値がクエリと同期していることを確認できます。</p> | [保存されたビューを十分に活用するフォームの作成](../user-interface/understanding-saved-views.md) | 開発者のオプトイン |
| 開発者ツール | <p>**保存されたビューからの個々のフォームをオプトアウトする**</p><p>保存されたビューを助長しないコーディング パターンを含むフォームの場合、開発者は保存されたビュー サポートの個々のフォームをオプトアウトすることができます。 つまり、フォームでビュー セレクターを使用できないし、公開機能はありません。</p> | [保存されたビューを十分に活用するフォームの作成](../user-interface/understanding-saved-views.md) | 開発者のオプトイン |


### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868) を参照してください。

### <a name="dynamics-365-2022-release-wave-1-plan"></a>Dynamics 365: 2022 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2022 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) の記事では、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md)の記事に廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。

