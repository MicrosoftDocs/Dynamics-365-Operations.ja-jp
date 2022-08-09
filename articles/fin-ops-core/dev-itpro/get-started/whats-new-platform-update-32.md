---
title: 財務と運用アプリのプラットフォーム更新プログラム 32 (2020 年 2 月) の新機能および変更された機能
description: この記事では、財務と運用アプリに関するプラットフォーム更新プログラム 32 のプレビュー機能について記載しています。
author: sericks007
ms.date: 02/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: Platform update 32
ms.openlocfilehash: 47f99510f68e755bf003cb772c4ad00a0a313363
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066891"
---
# <a name="whats-new-or-changed-in-platform-update-32-for-finance-and-operations-apps-february-2020"></a>財務と運用アプリのプラットフォーム更新プログラム 32 (2020 年 2 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのプラットフォーム更新プログラム 32 用の新機能または変更された機能を一覧表示します。 このバージョンのビルド番号は 7.0.5493 で、次のスケジュールで使用できます。

- **プレビュー リリース** 2019 年 12 月
- **一般提供 (自己更新):** 2020 年 1 月
- **自動更新:** 2020 年 2 月

プラットフォーム更新プログラム 32 の詳細については [追加リソース](whats-new-platform-update-32.md#additional-resources) を参照してください。

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

### <a name="file-size-limit-for-data-management-export-has-been-removed"></a>データ管理エクスポートのファイル サイズ制限が削除されました

詳細情報については、[データ管理エクスポートのファイル サイズ制限が削除されました](/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-management-export-file-size-limit-removed)を参照してください。

### <a name="finance-and-operations-aos-kernel-improvements"></a>財務と運用 AOS (カーネル) の改善

この機能の詳細については、[財務と運用 AOS (カーネル) の改善](https://community.dynamics.com/365/financeandoperations/b/newdynamicsax/posts/finance-and-operations-aos-kernel-improvements) を参照してください。

### <a name="continued-stabilization-of-saved-views"></a>保存されたビューの継続的な安定化

この機能の詳細については、[ユーザーの生産性 – 保存されたビュー](/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/user-productivity-saved-views)を参照してください。

### <a name="improved-responsiveness-of-action-panes-on-smaller-screens"></a>小さい画面上でアクション ペインの応答性が向上

この機能の詳細については、[モバイル デバイス エクスペリエンスの向上 – フェーズ 1 ](/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/improved-experience-mobile-devices-phase-1)を参照してください。

### <a name="ability-to-filter-on-blank-values-by-using-the-filter-pane-and-filters-in-grid-column-headers"></a>グリッド列ヘッダーのフィルター ウィンドウとフィルターを使用して、空白の値をフィルター処理する機能

この機能の詳細については、[ユーザーの生産性 – フィルター処理の強化](/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/user-productivity-filtering-enhancements)を参照してください。

### <a name="continued-evolution-of-the-new-grid"></a>新しいグリッド進化の継続

この機能の詳細については、[ユーザーの生産性 – 新規グリッド](/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/user-productivity-new-grid)を参照してください。

### <a name="priority-based-scheduling-for-batch-jobs"></a>バッチ ジョブの優先度のスケジュール
[バッチ ジョブの優先度スケジュール](/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/priority-based-scheduling-batch-jobs)機能の既存のバッチ ジョブとタスクを準備できるように 2 つの新しいシステム バッチ ジョブを導入しました。 その 2 つの新しいシステム バッチは、次のようなものです。

- **バッチ ジョブにバッチ グループの関連付けをシードするシステム ジョブ:** このバッチ ジョブは、クラス名 **SysMigrateBatchGroupsForPriorityBasedScheduling** で、バッチ ジョブをバッチ グループに関連付けます。
- **期限切れのバッチレコードを削除するシステムジョブ:** このバッチ ジョブでは、クラス名 **SysCleanupBatchHeartbeatTable** で、新しい内部監視 **BatchHeartbeatTable** テーブルを削除します。

バッチ ジョブ優先度のスケジューリング機能は、現在、制限付きプレビュー中です。 バッチ ジョブは無停止で設計されており、機能が有効になっていない場合は、現在のバッチ ジョブの機能や処理に影響はありません。

## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-32-bug-fixes"></a>プラットフォーム アップデート 32 のバグ修正プログラム

プラットフォーム更新プログラム 32 の一部である各更新プログラムに含まれるバグ修正の詳細については、LCS にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=400369&dbType=3&qc=30ab94ba46d00083bda800e9a50600fa1fdf63a47c33e8e83f74774b6d245f27)を参照してください。

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2019wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) の記事では、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md)の記事に廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
