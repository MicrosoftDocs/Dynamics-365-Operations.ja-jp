---
title: Finance and Operations アプリ バージョン 10.0.17 のプラットフォーム更新プログラム (2021 年 4 月)
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.17 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 592bf827f1fad0a703dc67534e4e34c3b594f6c5
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923397"
---
# <a name="platform-updates-for-version-10017-of-finance-and-operations-apps-april-2021"></a>Finance and Operations アプリ バージョン 10.0.17 のプラットフォーム更新プログラム (2021 年 4 月)

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.17 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.5934 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 2 月
- **リリースの一般提供 (自己更新):** 2021 年 3 月
- **リリースの一般提供 (自動更新):** 2021 年 4 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

-  Visual Studio 2017 は、X++ ツールの主要なサポート バージョンになりました。 Visual Studio 2015 は非推奨です。<br>- 詳細については、[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md#visual-studio-2015)を参照してください。

-  [(プレビュー) 組織ビューの翻訳サポート](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/translation-support-organizational-saved-views)<br>- 詳細については、[保存されているビュー](../../fin-ops/get-started/saved-views.md) を参照してください。

-  [React 17 にアップグレードする](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/upgrade-react-17)

-  [グリッド内の列の固定](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/freeze-columns-grids)<br>- 詳細については、[グリッド機能](../../fin-ops/get-started/grid-capabilities.md) を参照してください。

-  [クライアント機能の状態の更新](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states)<br>- このリリースで既定でオンになっていた、または必須になったクライアント機能の詳細については、リリース プランを参照してください。 

-  独立系ソフトウェア ベンダー (ISV) のライセンス ステータスの表示<br>- ISV ライセンスのステータスおよび有効期限を表示できるようになりました。 詳細については、[独立系ソフトウェア ベンダーのライセンス ステータスの表示](../sysadmin/view-isv-license-status.md)を参照してください。

- [executeQueryWithParameters](../dev-ref/query-with-parameters.md) メソッド<br>- このメソッドは、SQL インジェクション攻撃を軽減するのに役立つステートメント パラメーターを使用して SQL クエリを実行します。

- [バッチの通知](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/batch-notifications)<br>- 詳細については、[バッチ ビジネス イベント](../business-events/system-business-events.md) を参照してください。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=510c0f86ac24207edecf80d9f313de2065ba105446736042428e3b5489fdf607) を参照してください。

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2021wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]