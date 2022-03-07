---
title: Finance and Operations アプリ バージョン 10.0.13 のプラットフォーム更新プログラム (2020 年 10 月)
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.13 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 42916eb8f41c74decfa83a4125c2b52e3569f0007805ae645cd896870517b902
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769844"
---
# <a name="platform-updates-for-version-10013-of-finance-and-operations-apps-october-2020"></a>Finance and Operations アプリ バージョン 10.0.13 のプラットフォーム更新プログラム (2020 年 10 月)

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.13 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 (この更新プログラムは、*プラットフォーム更新プログラム 37* と呼ばれていました)。このバージョンには、ビルド番号 7.0.5746 が付与されており、次のスケジュールで利用できます:

- **プレビュー リリース:** 2020 年 7 月
- **一般提供 (自己更新):** 2020 年 9 月
- **自動更新:** 2020 年 10 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

-  Visual Studio ツールには Microsoft .NET 4.7.2 ランタイムが必要<br>- 詳細については、[Microsoft 以外が管理する開発者 VM に必要なアクション](https://community.dynamics.com/365/financeandoperations/b/newdynamicsax/posts/action-required---net-version-and-visual-studio-2017) を参照してください。

-  優先順位に基づく調整<br>- 詳細については、[優先順位に基づく調整](../data-entities/priority-based-throttling.md) を参照してください。 

-  [保存されているビュー - 一般提供](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- 詳細については、[保存されているビュー](../../fin-ops/get-started/saved-views.md) を参照してください。 

-  [新しいグリッド コントロール - 一般提供](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/new-grid-control--general-availability)<br>- 詳細については、[グリッド機能](../../fin-ops/get-started/grid-capabilities.md) を参照してください。 

-  [3 つの jQuery コンポーネント ライブラリのアップグレード](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/upgrade-three-jquery-components-libraries)

-  [タスク記録でコントロール状態の検証を許可する](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/new-task-recorder-capabilities)<br>- 詳細については、[タスク レコーダー リソース](../user-interface/task-recorder.md#validate) の「検証」セクションを参照してください。 この機能を Regression Suite Automation Tool (RSAT) と組み合わせて使用するには、[RSAT 2.0](https://www.microsoft.com/en-us/download/details.aspx?id=57357) に更新する必要があります。  


## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=476824&dbType=3&qc=18d329e7d9887a622bada690791f5814dbbef22bb6f4eaada3718299f40132fd) を参照してください。

### <a name="dynamics-365-2020-release-wave-2-plan"></a>Dynamics 365: 2020 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2020 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2020wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]