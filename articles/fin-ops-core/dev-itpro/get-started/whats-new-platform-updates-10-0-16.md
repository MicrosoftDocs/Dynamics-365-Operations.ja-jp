---
title: Finance and Operations アプリのバージョン 10.0.16 のプラットフォーム更新プログラム (2021 年 2 月)
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.16 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
manager: AnnBe
ms.date: 11/30/2020
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
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ac900ae3843def8776bf2170a36ff8f4cc8f1e36
ms.sourcegitcommit: 35cb173f0d356f00e2f50464ab77c3802ad28fbf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/21/2021
ms.locfileid: "5033868"
---
# <a name="platform-updates-for-version-10016-of-finance-and-operations-apps-february-2021"></a>Finance and Operations アプリのバージョン 10.0.16 のプラットフォーム更新プログラム (2021 年 2 月)

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ バージョン 10.0.16 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.5860 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2020 年 11 月
- **リリースの一般提供 (手動更新):** 2021 年 1 月
- **リリースの一般提供 (自動更新):** 2021 年 2 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。

-  ユーザー セッション管理<br>- 管理者は、個々のユーザーに対して最大セッション タイムアウトを設定できます。  このセッションの範囲は、1 時間から 2160 時間です。  このセッション長の期限が切れた場合、ユーザーは資格情報を使用してサインインする必要があります。 詳細については、[ユーザー セッション管理](../sysadmin/user-session-management.md) を参照してください。

-  'セッション アイドル タイムアウト' から 'セッション非活動タイムアウト' への名前変更<br>- 最大ユーザー セッションと非活動ユーザー セッションの間でセッション タイムアウトのタイプを区別するために、名前の変更が実装されました。 詳細については、[セッション非活動タイムアウトの設定](../sysadmin/session-idle-timeout.md) を参照してください。

-  Visual Studio 2015 のサポートの削除<br>- バージョン 10.0.16 は、Visual Studio 2015 をサポートする最新のバージョンです。 詳細については、[Visual Studio 2015 のサポートの削除](removed-deprecated-features-platform-updates.md#visual-studio-2015) を参照してください。

-  [電子メールの調整](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/email-throttling)<br>- この機能を使用すると、非対話型の電子メール プロバイダーは 1 分あたりの電子メール送信制限に従うことができます。これにより、プロバイダーが処理できる数よりも多くの電子メールをシステムが送信しようとしたときに現在トリガーされているエラーが防止されます。 電子メール調整を有効にすると、Microsoft 365 電子メール プロバイダーの送信制限が自動的に設定されます。他のすべての電子メール プロバイダーについては、手動での構成が必要です。 詳細については、[電子メールのコンフィギュレーションと送信](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email) を参照してください。

-  [ドキュメントの (添付ファイル) 履歴](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/document-attachment-history)<br>- このドキュメント管理機能では、レコードの添付ファイルの履歴メカニズムが作成されます。 これにより、個々の添付ファイルに関連するアクションの監査を組織で管理することができます。 たとえば、添付ファイルがいつ作成されたか、削除保留中のマークが付けられたか、復元、削除、移動されたか、誰がアクションを実行したかを確認できます。 既定の履歴保持期間は 180 日間ですが、これは **ドキュメント管理パラメータ** ページでコンフィギュレーションできます。 詳細については、[ドキュメント管理のコンフィギュレーション](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) を参照してください。

-  [グリッド機能を使用したグループ化の一般提供](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/grouping-subtotals-grids-general-availability)<br>- 詳細については、[グリッド機能](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities#grouping-tabular-data) を参照してください。

-  [新しい HTML エディター コントロール](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/new-html-editor-control)<br>

-  メッセージ ::addaction API の強化<br>- メッセージ ::addaction API は、メッセージがアクション センターまたはメッセージの詳細ウィンドウにルーティングされたときに、そのアクションを通知に表示するようになりました。 詳細については、[メッセージング API](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/messaging-api-center-bar-details#message) を参照してください。

- [SQL インジェクション攻撃の緩和](../dev-ref/query-with-parameters.md)<br>- 新しい **Statement.executeQueryWithParameters** API を使用して、SQL インジェクション攻撃を緩和します。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=528995&dbType=3&qc=267a545fabd24e111868bedc16716f5713a785ed096cdb6209526f41631e41db) を参照してください。

### <a name="dynamics-365-2020-release-wave-2-plan"></a>Dynamics 365: 2020 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2020 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックでは、削除された機能、または Finance and Operations アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md) のトピックに廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
