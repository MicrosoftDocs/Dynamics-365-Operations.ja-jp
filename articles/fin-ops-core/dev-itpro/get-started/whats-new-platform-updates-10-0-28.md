---
title: 財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラム (2022 年 8 月)
description: この記事では、財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 07/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2022-05-11
ms.openlocfilehash: 34857b1f96a703471f6c648e95a10085c7c50abf
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219325"
---
# <a name="platform-updates-for-version-10028-of-finance-and-operations-apps-august-2022"></a>財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラム (2022 年 8 月)

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6441 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 5 月
- **リリースの一般提供 (手動更新):** 2022 年 7 月
- **リリースの一般提供 (自動更新):** 2022 年 7 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|--------------|---------|------------------|------------|
| Web クライアント | <p>**Highcharts をバージョン 4 からバージョン 9 にアップグレード**</p><p>この機能は、財務と運用アプリのチャート JavaScript ライブラリをバージョン 9 にアップグレードします。 新しいライブラリを使用すると、チャートやグラフをアプリで構築、展開、使用するときに、より豊富な視覚化セットを使用できます。 この機能を有効にする前に、Highcharts アプリケーション プログラミングインターフェイス (APIs) を使用する拡張可能なコントロールまたはカスタム JavaScript コードをテストして、アップグレードに問題がないことを確認する必要があります。 この機能は、2023 年 4 月のリリースで必須となることを目標としていますが、影響を受ける API の移行に時間をかけるために、現在はオプションです。</p> | 該当なし | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| Web クライアント  | [システム通知管理の有効化](/dynamics365-release-plan/2022wave1/finance-operations/finance-operations-crossapp-capabilities/enable-system-notification-management) | 該当なし | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) |

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) を参照してください。

### <a name="dynamics-365-2022-release-wave-1-plan"></a>Dynamics 365: 2022 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2022 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) の記事では、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md)の記事に廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。

