---
title: Finance and Operations アプリ (2021 年 11 月) のバージョン 10.0.22 のプラットフォーム更新プログラム
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.22 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 09/03/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2021-08-31
ms.openlocfilehash: 256340ba1ae2ef73936362b7529bb3483b36d8c3
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472520"
---
# <a name="platform-updates-for-version-10022-of-finance-and-operations-apps-november-2021"></a>Finance and Operations アプリ (2021 年 11 月) のバージョン 10.0.22 のプラットフォーム更新プログラム

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.22 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6164 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 9 月
- **リリースの一般提供 (手動更新):** 2021 年 10 月
- **リリースの一般提供 (自動更新):** 2021 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features)を参照してください。

| 機能領域    | フィーチャー | 詳細 | 機能を有効にする方法 |
|-----------------|---------|------------------|---------------------------|
| クライアント機能 | <p>**オープンソース ソフトウェア更新: Moment のアップグレードと jqWidgets の削除**</p><p>この機能により、Moment.js がバージョン (2.22.2 から) 2.29.1 にアップグレードされ、Finance and Operations アプリから jQWidgets ライブラリが削除されます。 現在 jQWidgets を使用している唯一のコア コントロールは、HTML エディター コントロールとカラー ピッカーです。 これらの両方のコントロールを jqWidgets 以外のコントロールにアップグレードするには、新しい HTML エディター コントロールと新しいカラー ピッカー コントロール機能を使用します。</p><p>**重要:** この機能を有効にする前に、任意の拡張可能なコントロールまたはカスタム JavaScript コード、特に、jQWidgets または Moment アプリケーション プログラミング インターフェイス (API) を使用するコントロールとコードをテストする必要があります。 この機能は、2022 年 4 月リリースで必須となる予定です。 ただし、影響を受ける API の移行期間のため、現在はオプションです。</p> | 適用できません | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| クライアント機能 | <p>**新しいカラー ピッカー コントロール**</p><p>この機能は、既存のカラー ピッカー コントロールを [Fluent ColorPicker コントロール](https://developer.microsoft.com/fluentui#/controls/web/colorpicker)に置き換えて、他の Microsoft 製品とのエクスペリエンスを調整します。</p> | 適用できません | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) |
| クライアント機能 | <p>**階層ビューアー コントロールへの視覚的な更新**</p><p>特に 400% ズーム シナリオでは、アクセシビリティを向上させるために HierarchyViewer コントロールに変更が加えられました。 これらの変更には、すべてのズーム レベルでのコントロールの可読性を高めるために、コントロールを再スタイルして Fluent デザイン言語で合わせることが含まれます。 | [HierarchyViewer コントロール](../user-interface/hierarchy-viewer-control.md) | 既定 |

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) を参照してください。

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。