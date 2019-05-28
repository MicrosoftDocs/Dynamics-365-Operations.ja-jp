---
title: データベース ポイントインタイム復元 (PITR)
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースのポイントインタイム復元を実行する方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a75a9ed7df3c65cf55d6f0c4e05fcb409c05bb03
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537095"
---
# <a name="database-point-in-time-restore-pitr"></a>データベース ポイントインタイム復元 (PITR)

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) を使用し、Dynamics 365 for Finance and Operations サンドボックス ユーザー受け入れテスト (UAT) 環境のポイントインタイム復元 (PITR) を実行できます。 

## <a name="self-service-point-in-time-restore"></a>セルフサービスポイントインタイム復元
[!include [pitr](../includes/dbmovement-pitr.md)]

### <a name="restore-operation-failed"></a>失敗した操作の復元
失敗した場合、**ロールバック**を実行するオプションを使用できます。  工程が最初に失敗した後にロールバック オプションをクリックすると、対象となるサンドボックス環境が復元の開始前の状態に戻されます。 これにより、以前のデータベースが Azure SQL Server の削除されたデータベースの記憶域から復元されます。 新しく復元されたデータでデータベースの同期を完了できないをターゲット サンドボックスにカスタマイズがある場合は、これがよく必要になります。  

失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。

### <a name="data-elements-that-need-attention-after-restore"></a>復元後に注意が必要なデータの要素
前の時点からデータベースを復元する場合は、データベースがそのまま提供されることに留意してください。 つまり、システム内のバッチ ジョブとその他のデータ要素は進行中の状態の可能性があります。 これらは、手動の確認が必要となります。

### <a name="environment-administrator"></a>環境管理者
対象となる環境のシステム管理者アカウント ('Admin' の UserId) は、ターゲットの web.config file ファイルにある値にリセットされます。  これは、Lifecycle Services の管理者と同じ値になります。 これがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの **環境の詳細** ページにアクセスします。  環境が最初に展開されたときに選択された **環境管理者** フィールドの値は、トランザクション データベース内のシステム管理者となるように更新されます。 これは、環境のテナントが環境管理者のテナントとなることも意味します。  

web.config ファイルを別の値に変更するために環境で管理者ユーザー プロビジョニング ツールを使用した場合は、Lifecycle Services の内容と一致しない可能性があります。  別のアカウントを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。 この後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。

## <a name="steps-to-complete-after-a-database-restore-for-environments-that-use-retail-functionality"></a>Retail 機能を使用する環境のデータベース復元後に実行する手順
[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="known-issues"></a>既知の問題

### <a name="point-in-time-restore-breaks-the-chain-of-available-restore-points"></a>ポイントインタイム復元により利用可能な復元ポイントのチェーンが壊れる
復元データベース処理は、常に前の時点のスナップショットに基づいて新しいデータベースを作成します。  このため、新しいデータベースには、復元の履歴はありませんが、今後使用される新しい復元ポイントを取得し始めます。 つまり、ポイントインタイム復元を実行した後、同じ復元日時を使って復元することはできなくなります。  

今後、Lifecycle Services チームは、削除されたデータベースの復元履歴を活用することで時点でポイントインタイム復元を向上させるよう努めます。  これによって、破壊試験などのシナリオで同じ時点に継続的に復元できるようになります。  これは、LCS の今後のリリースで修正されます。

### <a name="restore-is-denied-for-environments-running-platform-update-3-or-earlier"></a>プラットフォーム アップデート 3 以前を実行する環境で復元が拒否される
環境でプラットフォーム更新 3 以前を実行している場合は、データベース復元の処理を実行することはできません。 詳細は、[現在サポートされているプラットフォーム更新の一覧](..//migration-upgrade/versions-update-policy.md)を参照してください。


