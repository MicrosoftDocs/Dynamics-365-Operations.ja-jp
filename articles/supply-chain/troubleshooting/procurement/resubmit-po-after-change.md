---
title: 変更後にワークフローに発注書を再送信する際のエラー
description: 変更後にワークフローに発注書を再送信する際のエラー
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476923"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>変更後にワークフローに発注書を再送信する際のエラー


## <a name="symptoms"></a>現象

変更後に発注書を再送信すると、ワークフローで次のエラーが発生します。

> 停止 (エラー): X + + 例外: 発注書 PO0000569 に対する変更は、変更管理が次で有効になっている場合にのみ [ドラフト] 状態でのみ許可されます。<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

この問題は、変更を要求する前に発注書が *確認済* 状態になっていた場合にのみ発生します。 発注書が *承認済* 状態になっている場合に変更を要求すると、ワークフローを正常に処理できます。

## <a name="resolution"></a>解決策

この問題は、発注書の配分に不整合があるために発生することがあります。

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。

この問題は、[この Microsoft サポート技術情報 (KB) の記事 ](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) を通じて修正されます。
