---
title: データベース ポイントインタイム復元 (PITR)
description: このトピックでは、Finance and Operations のデータベースのポイントインタイム復元を実行する方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6134652bbb07edfc74593baa473990b81890a873
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681098"
---
# <a name="database-point-in-time-restore-pitr"></a>データベース ポイントインタイム復元 (PITR)

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) を使用し、サンドボックス ユーザー受け入れテスト (UAT) 環境のポイントインタイム復元 (PITR) を実行することができます。 Microsoft は、業務および財務報告用のデータベースの[自動バックアップ](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)を、実稼働環境の場合は 28 日間、サンドボックス環境の場合は 14 日間維持します。

## <a name="self-service-point-in-time-restore"></a>セルフサービスポイントインタイム復元
[!include [pitr](../includes/dbmovement-pitr.md)]

### <a name="restore-operation-failed"></a>失敗した操作の復元
失敗した場合、**ロールバック** を実行するオプションを使用できます。 操作が最初に失敗をした後に ロールバック オプションを選択すると、ターゲット サンドボックス環境は、復元開始前の状態に復元されます。 ターゲット サンドボックスに存在するカスタマイズが、新しく復元されたデータとのデータベースの同期を完了できない場合、ロールバックが必要になることがよくあります。

失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。

### <a name="data-elements-that-need-attention-after-restore"></a>復元後に注意が必要なデータの要素
以前の時点からデータベースを復元する場合、データベースは "現状のまま" 提供されることに注意してください。 例えば、システム内のバッチ ジョブやその他のデータ要素が進行中の状態になる可能性があります。 これらの要素は、手動で確認が必要となります。

### <a name="environment-administrator"></a>環境管理者
対象の環境のシステム管理者アカウント (**Admin** の **UserId** 値を持つアカウント) が、対象の環境に存在する web.config ファイルで検出された値にリセットされます。 この値は、LCS の管理者アカウントの値と一致している必要があります。 使用するアカウントをプレビューするには、LCS でターゲット サンドボックス環境の **環境詳細** ページに移動します。 環境が最初に展開されたときに **環境管理者** フィールドで選択された値は、トランザクション データベースのシステム管理者に更新されます。 環境のテナントが環境管理者のテナントになります。

環境で管理者ユーザー プロビジョニング ツールを使用して、web.config ファイルの値を変更した場合、値は LCS の値と一致しない可能性があります。 別のアカウントが必要な場合は、ターゲット サンドボックス環境の割り当てを解除して削除し、別のアカウントを選択して再展開する必要があります。 その後、データを復元するために別のデータベース更新アクションを実行することができます。

## <a name="steps-to-complete-after-a-database-restore-for-environments-that-use-commerce-functionality"></a>コマース機能を使用する環境のデータベース復元後に実行する手順
[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="known-issues"></a>既知の問題

### <a name="breaking-the-chain-of-available-restore-points"></a>使用可能な復元ポイントのチェーンの中断
頻繁に使用するいくつかのアクションは、以前に使用したデータベースと同じ復元ポイント履歴を持たない新しいデータベースを作成します。 このアクションには、ポイント イン タイム復元、データベースの更新、データベースのインポート、実稼働環境からサンドボックス環境へのポイント イン タイム復元などが含まれます。 さらに、データベースの更新時に環境に適用するソフトウェア展開可能なパッケージが失敗し、LCS のロールバック機能を使用する場合、ロールバック機能はデータベースのポイント イン タイム復元を実行し、その復元は新しいデータベースも作成します。 

新しいデータベースには、復元ポイント履歴はありませんが、その時点から新しい復元ポイントを取得し始めます。 前述のアクションのいずれかを実行した後、同じ復元日時を使用して再度実行することはできません。

### <a name="restore-is-denied-for-environments-that-run-platform-update-20-or-earlier"></a>プラットフォーム 更新プログラム 20 以前が稼働している環境では、復元は拒否されます
環境でプラットフォーム更新 20 以前を実行している場合は、データベース復元の処理を実行することはできません。 詳細については、[ソフトウェアのライフサイクル ポリシーとクラウド リリース](..//migration-upgrade/versions-update-policy.md)で現在サポートされているプラットフォーム更新の一覧を参照してください。
