---
title: 行き詰まったバッチ ジョブのリセット
description: このトピックでは、行き詰ったバッチ ジョブの問題の解決方法について説明します。
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 01ef0bf8ccc486614eec42d3fb6f0b2941fc47c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794952"
---
# <a name="reset-stuck-batch-jobs"></a>行き詰まったバッチ ジョブのリセット

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>出庫

Microsoft Dynamics 365 Human Resources では、**実行中** または **キャンセル中** のいずれかの状態で処理が行き詰まり、バッチ ジョブ処理が完了しないという問題が発生する可能性があります。

## <a name="resolution"></a>解像度

バッチ ジョブが **実行中** または **キャンセル中** の状態で処理されなくなった場合は、ジョブを強制的にキャンセルすることでステータス をリセットできます。 キャンセルした後は、バッチ ジョブを **待機中** ステータスに設定してリセットできます。 その後、次回スケジュールされたバッチ実行で実行するために、再度取得されます。

1. **システム管理** ワークスペースで 、**リンク** ページ を選択し、**バッチ ジョブ** を選択します。

2. **バッチ ジョブ** リスト ページで、リセットする必要があるジョブを選択します。

3. アクション リボンで、**強制キャンセル** を選択し、アクションを確定します。

   > [!NOTE]
   > **強制キャンセル** アクションは、選択したバッチ ジョブのステータスが **実行中** または **キャンセル中** であり、ジョブに対してバッチの実行またはキャンセルのプロセスが実行されている場合にのみ使用できます。

4. アクション リボンで、**ステータスの変更** を選択します。

5. **新しいステータスの選択** ページで、**待機中** を選択してから、**OK** を選択します。

   ![新しいバッチ ジョブ ステータスの選択](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>参照

[時間後にバッチ ジョブのスケジュールを設定してパフォーマンスを最適化する](hr-admin-troubleshooting-batch-jobs.md)<br>
[自動クリーンアップ タスクを使用したパフォーマンスの最適化](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
