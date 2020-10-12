---
title: 調達ワークフローに関するトラブルシューティング
description: このトピックでは、調達ワークフロー中に発生する可能性がある問題を修正する方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 940a6c39ac83e7388d4e1a08b656b75df81ed801
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834384"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>調達ワークフローに関するトラブルシューティング

このトピックでは、調達ワークフロー中に発生する可能性がある問題を修正する方法について説明します。

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>変更後に発注書をワークフローに再送信するときのエラー: "発注書 X に対する変更は、変更管理が有効になったときにのみ下書きの状態で許可されます"

この問題は、変更を要求する前に発注書が *確認済* 状態になっていた場合にのみ発生します。 発注書が *承認済* 状態になっている場合に変更を要求すると、ワークフローを正常に処理できます。

### <a name="error-description"></a>エラーの説明

変更後に発注書を再送信すると、ワークフローで次のエラーが発生します。

> 停止 (エラー): X + + 例外: 発注書 PO0000569 に対する変更は、変更管理が次で有効になっている場合にのみ [ドラフト] 状態でのみ許可されます。<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>問題の解決

この問題は、発注書の配分に不整合があるために発生することがあります。

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。

この問題は、[この Microsoft サポート技術情報 (KB) の記事 ](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) を通じて修正されます。

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>1 つ以上の勘定配布が、過剰配布されているか、配布中であるかのいずれかです。

この問題は、発注書の配分に不整合があるために発生することがあります。

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>変更管理が有効になっている発注書で出荷更新待ちがキャンセルされた場合、発注書は確認済状態になります。

### <a name="issue-description"></a>問題の説明

変更管理の対象となる発注書の場合、要求される唯一の変更が 1 つ以上の明細行の出荷残余の取消である場合、発注書は承認された時点で直接 *確認済* 状態になり、仕訳帳は作成されません。

### <a name="issue-resolution"></a>問題の解決

配送残余をキャンセルしても、確認仕訳帳の内容には影響しません。 この機能は、明細行が部分的に入庫され、発注書が仕入先に対して確認された後に、プロセス ステップで残余品質をキャンセルする必要がある場合に使用します。

この数量を発注書の確認書に反映する必要がある場合は、購買注文明細行で数量を調整して、確認が必要になるようにする必要があります。 また、その明細行に何も入庫されていない場合は、数量を削除できます。 この場合、再確認が要求されます。

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>キャンセルされた発注書は、発注書準備ワークスペースの下書き一覧に表示されます。

### <a name="issue-description"></a>問題の説明

*確認済* 状態の発注書をキャンセルした後で、そのキャンセルされた発注書は、**発注書** 準備ワークスペースのドラフト発注書の一覧に表示されます。

### <a name="issue-resolution"></a>問題の解決

この問題は、変更管理の対象になる発注書に対してのみ発生します。 これは、このキャンセルに必要のある変更が懸念されることから発生します。 この承認は、システムによって自動的に行うことができます。 したがって、このプロセスでは、キャンセルされた発注書を承認ワークフローに送信して、*承認済* 状態にすることができます。 この時点で、**発注書の準備** ワークスペースのドラフト発注書の一覧にその発注書が表示されなくなります。

