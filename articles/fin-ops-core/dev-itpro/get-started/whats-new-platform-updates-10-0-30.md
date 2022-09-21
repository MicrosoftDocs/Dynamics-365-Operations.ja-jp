---
title: 財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラム (2022 年 11 月)
description: この記事では、財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 08/19/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2022-08-19
ms.openlocfilehash: 42ef08523fd33642be7d67230bc9d60c111bf7da
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405524"
---
# <a name="platform-updates-for-version-10030-of-finance-and-operations-apps-november-2022"></a>財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラム (2022 年 11 月)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6592 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 9 月
- **リリースの一般提供 (手動更新):** 2022 年 10 月
- **リリースの一般提供 (自動更新):** 2022 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。

| モジュールまたは機能エリア | フィーチャー名 | 詳細 |  に  によって有効化 |
|---|---|---|---|
| Web クライアント | プレビューから一般に入手可能に移行する[コンボ ボックスおよびルックアップ コントロールのキーボード インタラクションを標準化する](/dynamics365-release-plan/2022wave1/finance-operations/finance-operations-crossapp-capabilities/standardize-keyboard-interaction-combo-box-lookup-controls) | [キーボード ショートカット](../../fin-ops/get-started/shortcut-keys.md) | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| Web クライアント | <p>**グループ化されたカード リストおよび複数列カード リストの新しいグリッド コントロールのサポート**</p><p>このようなタイプのカード リストを含むページは、レガシ グリッド コントロールを使用する際に自動的に元に戻さなくなくなりました。 また、グループ化されたカード リストまたは複数列のカードのため、`forceLegacyGrid()` API は削除しても安全です。</p> | [グリッド機能](../../fin-ops/get-started/grid-capabilities.md) | 既定で有効  |

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。

### <a name="dynamics-365-2022-release-wave-2-plan"></a>Dynamics 365: 2022 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2022 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2022wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
