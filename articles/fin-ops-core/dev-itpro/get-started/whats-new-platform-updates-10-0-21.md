---
title: 財務と運用アプリのバージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)
description: この記事では、財務と運用アプリのバージョン 10.0.21 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 10/28/2021
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
ms.openlocfilehash: c398cde5a3ecc82147ea5581ce1f6e0bf09a1e20
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068217"
---
# <a name="platform-updates-for-version-10021-of-finance-and-operations-apps-october-2021"></a>財務と運用アプリのバージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのバージョン 10.0.21 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6129 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 8 月
- **リリースの一般提供 (手動更新):** 2021 年 9 月
- **リリースの一般提供 (自動更新):** 2021 年 10 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

使用する前に、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)を使用して一部の機能を有効にする必要があります。

| 機能領域   | フィーチャー                                                  | 詳細                                                                    |
|----------------|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| クライアント機能 | [保存したビューに対する法人サポートの改善](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/improved-legal-entity-support-saved-views)  | [保存されているビュー](../../fin-ops/get-started/saved-views.md) |
| クライアント機能 | [クライアント機能の状態の更新](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states-version-10021) | 該当なし |
| システム管理 | [機能管理の完全な機能ライフサイクルに対する強化されたサポート](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/enhanced-support-full-feature-lifecycle-feature-management)| [機能管理の概要](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| 可用性の監視 | [Service Fabric 環境の統合的な監視](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/synthetic-monitoring-service-fabric-environments) | 該当なし | 
| 開発者ツール | Visual Studio 2019 が正式にサポートされるようになりました。 | [Visual Studioの開発ツール](../dev-tools/development-tools-overview.md) |

## <a name="features-turned-on-by-default-in-this-release"></a>このリリースで、既定で有効になる機能

次の表に、10.0.21 で既定で有効になる機能の一覧を示します。 有効にした機能のほとんどは [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) でオフにできます。

| 機能名 | 日付を有効にする | 機能の追加日 | 機能状態 | モジュール |
| :--- | :--- | :--- | :--- | :--- |
| 電子申告フレームワークで EPPlus ライブラリの使用を有効にします | 2021/9/1 | 2020/1/6 | 既定で有効 | 組織管理 |
| Microsoft Office 形式から PDF に電子申告送信ドキュメントを変換する | 2021/9/1 | 2020/1/6 | 既定で有効 | 組織管理 |
| ビジネス ドキュメント管理の Office と同様の UI エクスペリエンス | 2021/9/1 | 2019/11/11 | 既定で有効 | 組織管理 |
| ビジネス ドキュメントの管理 | 2021/9/1 | 2019/6/3 | 既定で有効 | 組織管理 |
| 保存されているビュー | 2021/9/1 | 2019/6/9 | 既定で有効 | システム管理 |
| 新しいグリッド コントロール | 2021/9/1 | 2019/10/7 | 既定で有効 | システム管理 |
| グリッド内でのグループ化 | 2021/9/1 | 2019/12/19 | 既定で有効 | システム管理 |
| メール ディストリビューター バッチ ジョブのメールの有効期限 | 2021/9/1 | 2020/2/19 | 既定で有効 | システム管理 |
| 個人用設定を使用してフィールドを必要と指定する | 2021/9/1 | 2020/4/1 | 既定で有効 | システム管理 |
| 関連ドキュメントの添付ファイル ボタンを表示 | 2021/9/1 | 2020/4/24 | 必須 | システム管理 |
| レポート PDF ビューアー | 2021/9/1 | 2020/4/24 | 既定で有効 | システム管理 |
| レポート PDF ビューアーでのエクスポートを有効にする | 2021/9/1 | 2020/6/14 | 既定で有効 | システム管理 |
| レポート PDF ビューアーでのネットワーク印刷を有効にする | 2021/9/1 | 2020/6/14 | 既定で有効 | システム管理 |
| Key Vault クライアント キャッシュ | 2021/9/1 | 2020/8/17 | 既定で有効 | システム管理 |
| タスク記録でコントロール状態の検証を許可する | 2021/9/1 | 2020/8/17 | 必須 | システム管理 |
| レポート PDF ビューアー コントロールでドリル スルー リンクを有効にします。 | 2021/9/1 | 2020/8/17 | 既定で有効 | システム管理 |
| グリッドの列を固定する | 2021/9/1 | 2021/2/20 | 既定で有効 | システム管理 |
| 新しいカラー ピッカー コントロール | 2021/9/1 | 2021/9/1 | 既定で有効 | システム管理 |
| ワークフロー メッセージ処理バッチ ジョブの複数の実行を防止します。 | 2021/9/1 | 2021/9/1 | 既定で有効 | ワークフロー |
| バッチ アフィニティをリセットします | 2021/9/1 | 2021/9/1 | 既定で有効 | ワークフロー |
| ワークフローの通知アクション | 2021/9/1 | 2020/8/22 | 既定で有効 | ワークフロー |

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166) を参照してください。

### <a name="dynamics-365-2021-release-wave-2-plan"></a>Dynamics 365: 2021 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) の記事では、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md)の記事に廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。

