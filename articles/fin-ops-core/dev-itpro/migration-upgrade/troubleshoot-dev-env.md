---
title: アップグレード中の開発環境のトラブルシューティング
description: この記事では、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) レベル 1 開発環境へのアップグレードに関するトラブルシューティング ガイドを提供します。
author: ttreen
ms.date: 04/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: ''
ms.search.form: 2022-04-08
ms.openlocfilehash: 0be296b6f0dcd43ac3ef2e9e3f1871fa92de41ac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890435"
---
# <a name="troubleshoot-development-environments-during-upgrade"></a>アップグレード中の開発環境のトラブルシューティング

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) レベル 1 開発環境へのアップグレードに関するトラブルシューティング ガイドを提供します。

## <a name="scenario-1-the-data-upgrade-is-running-slowly-on-the-tier-1-development-environment"></a>シナリオ 1: レベル 1 の開発環境でのデータのアップグレードの実行が遅いです。

**ソリューション**

Microsoft Dynamics Lifecycle Services (LCS) から仮想マシン (VM) を配置する場合は、Premium Storage を使用します。

## <a name="scenario-2-log-files-on-dynamics-ax-2012-sql-database-ax-fill-up-the-disk"></a>シナリオ 2: Dynamics AX 2012 SQL データベース AX のログ ファイルがディスクを埋めます。

**ソリューション**

データベースの復旧モードを **単純** に設定します。

## <a name="scenario-3-a-failed-to-create-a-session-error-is-generated-during-a-prerequisite-step"></a>シナリオ 3: 前提条件の手順の間に「セッションの作成に失敗しました」というエラーが生成されます。

アップグレードの前提条件の手順の一部として実行される追加同期または部分同期時に、ダウンロードした同期ログで次のようなエラーが発生する場合があります。

> DBSync のモニタリングを停止しました。 Microsot.Dynamics.Ax.Xpp.ErrorException: セッションの作成に失敗しました。ユーザーに Microsoft Dynamics 365 for Finance and Operations にログオンするための適切な権限があることを確認してください。

**考えられる原因**

- **Application** または **info** クラスを拡張するカスタマイズがあり、そのカスタマイズにより Application Object Server (AOS) の応答が停止する場合があります。
- **SysClientSessions** テーブルでは、セッションが古く、または破損している可能性があります。

**ソリューション**

1. **Application** または **Info** クラス周辺の「顧客検証」カスタマイズ拡張機能のカスタム コード ベースがデモ データベースに対して動作するようにしてください。
2. 次の SQL コマンドを使用して **SysClientSessions** テーブルからレコードを切り詰め、もう一度やり直してください。

    ```SQL
    TRUNCATE TABLE SYSCLIENTSESSIONS;
    ```
