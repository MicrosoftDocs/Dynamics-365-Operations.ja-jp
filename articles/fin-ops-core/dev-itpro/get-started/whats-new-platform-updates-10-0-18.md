---
title: Finance and Operations アプリ バージョン 10.0.18 のプラットフォーム更新プログラム (2021 年 5 月)
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.18 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2021-03-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5bdf98754f38a06eb16ab54804d1f6944387324d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752762"
---
# <a name="platform-updates-for-version-10018-of-finance-and-operations-apps-may-2021"></a>Finance and Operations アプリ バージョン 10.0.18 のプラットフォーム更新プログラム (2021 年 5 月)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.18 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.5968 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 3 月
- **リリースの一般提供 (自己更新):** 2021 年 4 月
- **リリースの一般提供 (自動更新):** 2021 年 5 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

-  [OWIN OpenID Connect にアップグレードされた Finance and Operations アプリの認証](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/authentication-finance-operations-apps-upgraded-owin-openid-connect)

-  [Excel アドインの公開バッチサイズのコンフィギュレーションを許可する](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/allow-configuration-publish-batch-size-excel-add-in)<br>- 詳細については、[Excel を使用したエンティティ データの表示と更新](../office-integration/use-excel-add-in.md)を参照してください。

- [追加の NuGet ファイルには、ホストされる Azure DevOps のビルド パイプラインへの手動更新が必要です](../dev-tools/pipeline-nuget-split.md)

-  [それらのルックアップ コントロールを使用するコンボ ボックス用に相互作用パターンを調整する](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/align-interaction-patterns-combo-boxes-those-look-up-controls)

- [(プレビュー) 必須の非バインド コントロールへの入力を確認する](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/ensure-required-unbound-controls-are-filled)

- 管理者による既定ドキュメント タイプの選択を許可する<br>- 詳細については、[ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md) を参照してください。

- グローバル アドレス帳の更新<br>- 詳細については、[アドレス帳に関するよく寄せられる質問](../../fin-ops/organization-administration/qa-address-books.md) を参照してください。

-  バッチ ジョブの自動再試行設定<br>- クラウド アプリケーションでは、データベースへの接続が失われる可能性があります。 現時点では、アプリケーションが接続を失った場合、バッチ ジョブは終了します。 リリース 10.0.18 では、すべての Microsoft バッチ ジョブにフラグを設定する **再試行可能** フラグが導入されました。 このフラグは、一時的な接続が失われたとき、バッチ ジョブを安全に再試行するために使用されます。 これは完全に拡張可能なプロパティで、カスタム バッチ ジョブで再試行プロパティを設定するために拡張されます。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=561679&dbType=3&qc=13bb1641c1be430ead8b21ae3d4e0f800d5b81c39b3a56e890db1de7ede59e46) を参照してください。

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 1 プラン](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
