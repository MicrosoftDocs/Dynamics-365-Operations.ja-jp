---
title: 財務と運用アプリのバージョン 10.0.31 のプラットフォーム更新プログラム (2023 年 2 月)
description: この記事では、財務と運用アプリのバージョン 10.0.31 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: twheeloc
ms.date: 09/29/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2022-10-14
ms.openlocfilehash: 38eec47f34e1ae3a1bef7fcbef571685c5ff0725
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691011"
---
# <a name="platform-updates-for-version-10031-of-finance-and-operations-apps-february-2023"></a>財務と運用アプリのバージョン 10.0.31 のプラットフォーム更新プログラム (2023 年 2 月)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、財務と運用アプリのバージョン 10.0.31 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6651 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 10 月
- **リリースの一般提供 (手動更新):** 2023 年 1 月
- **リリースの一般提供 (自動更新):** 2023 年 2 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。

| モジュールまたは機能エリア | 機能名 | 詳細 |  に  によって有効化 |
|---|---|---|---|
| データ管理 | テーブルおよびデータ エンティティに対する行バージョン変更追跡の許可 (プレビュー) | [テーブルおよびデータ エンティティに対する行バージョン変更追跡の許可](../data-entities/rowversion-change-track.md) を参照してください。 | 既定 |
| Power Platform | Dataverse で財務と運用の仮想テーブルの変更を追跡する (プレビュー) | [Dataverse で財務と運用の仮想テーブルの変更を追跡する](../power-platform/track-changes-fin-ops-virtual-table.md) を参照してください。 | 既定 |
| システム管理 | マスター会社のデータ共有ポリシー (プレビュー) | [会社間データ共有の概要](../sysadmin/srs-overview.md) を参照してください。 | 機能管理 |
| システム管理 | 新しい SecurityRole メタデータ プロパティ | <p>新しい **SecurityRole** メタデータ プロパティ **UI から削除可能** が追加され、財務と運用アプリを使用してシステム ロールが削除されるのを回避できるようになりました。 既定値は **はい** です。 値が **いいえ** に設定されている場合は、削除アクションを実行すると「NN は削除できないシステム ロールです」というエラー メッセージが表示されます。</p>[![UI プロパティから削除できます。](../media/CanBeDeletedFromUI.jpg)](../media/CanBeDeletedFromUI.jpg) | 既定 |
| システム管理 | 新しいテーブル メタデータ プロパティ | <p>新しい **テーブル** メタデータ プロパティ **DisableDatabaseLog** を使用すると、テーブルがデータベース ログに追加されるのを防ぐことができます。 既定値は **いいえ** です。 値が **はい** に設定されている場合、データベース ログの設定時にテーブルを追加できません。</p>[![DisableDatabaseLog プロパティ。](../media/DisableDatabaseLogging.jpg)](../media/DisableDatabaseLogging.jpg) | 既定 | 

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグ修正については、Microsoft Dynamics Lifecycle Services にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525) を参照してください。

### <a name="dynamics-365-2022-release-wave-2-plan"></a>Dynamics 365: 2022 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2022 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2022wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
