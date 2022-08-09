---
title: 財務と運用アプリのバージョン 10.0.26 のプラットフォーム更新プログラム (2022 年 5 月)
description: この記事では、財務と運用アプリのバージョン 10.0.26 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 03/04/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2022-03-04
ms.openlocfilehash: a1617b7a22ec0046b3c4e24e0c177affa7152578
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067738"
---
# <a name="platform-updates-for-version-10026-of-finance-and-operations-apps-may-2022"></a>財務と運用アプリのバージョン 10.0.26 のプラットフォーム更新プログラム (2022 年 5 月)

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのバージョン 10.0.26 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6354 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 3 月
- **リリースの一般提供 (自己更新):** 2022 年 4 月
- **リリースの一般提供 (自動更新):** 2022 年 5 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。

| 機能領域    | フィーチャー | 詳細 |  に  によって有効化 |
|-----------------|---------|------------------|---------------------------|
| クライアント  | <p>**フルページ フォームのタビング動作を合理化する**</p><p>これまで財務と運用アプリでは、フルページ フォームの各領域 (ナビゲーション バー、メイン フォーム、アクション ウィンドウなど) のすべてのコントロール間をタブで移動していました。 ページ上の別の領域にフォーカスを移動するには、マウスまたは専用のキーボード ショートカットを使用する必要がありました。 この機能を使用すると、これらのタビング コンテナーが削除されるため、ユーザーが作業している領域に関係なく、特別なキーボード ショートカットを必要とせずに、フルページ フォームのすべてのコントロールをタブで移動できます。<br><br>既存のキーボード ショートカットは、ユーザーがページ上の領域間をすばやく移動する手段としてそのまま機能します。 | [キーボード ショートカット](../../fin-ops/get-started/shortcut-keys.md)  | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)  |
| クライアント  | <p>**ユーザーがタイル サイズを選択および変更できるようにする**</p><p>この機能により、ユーザーはワークスペース内のタイルのサイズを 4 つの使用可能なサイズのいずれかに変更できます。 ワークスペースに新しいタイルを追加するユーザーは、構成ダイアログで目的のタイル サイズを選択できます。</p><p>この機能はプレビューリ リースでは使用できないことに注意してください。</p> | [ユーザー エクスペリエンスのパーソナライズ](../../fin-ops/get-started/personalize-user-experience.md)  | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)  |  

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) を参照してください。

### <a name="dynamics-365-2022-release-wave-1-plan"></a>Dynamics 365: 2022 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2022 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) の記事では、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md)の記事に廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。

