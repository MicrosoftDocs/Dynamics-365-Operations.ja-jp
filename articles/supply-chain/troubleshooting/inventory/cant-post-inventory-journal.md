---
title: 在庫仕訳帳ワークフローが未完了なので、仕訳帳を処理できません
description: 仕訳帳承認ワークフローを送信すると、ワークフロー処理の応答が停止され、仕訳帳を編集または処理できます。
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488970"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>在庫仕訳帳ワークフローが未完了なので、仕訳帳を処理できません

## <a name="symptoms"></a>現象

仕訳帳承認ワークフローを送信すると、ワークフロー処理の応答が停止され、仕訳帳を編集または処理できます。

## <a name="resolution"></a>解決策

ワークフロー処理が完了しないのはいくつかの理由があります。 次の問題を確認してください。

- **在庫管理 &gt; 設定 &gt; 在庫管理ワークフロー** に移動し、影響を受けるワークフローの構成を確認します。 詳細については、[仕訳帳承認ワークフロー](../../inventory/inventory-journal-workflow.md) を参照してください。
- ワークフローに例外またはエラーが発生する可能性があります。 影響を受けるワークフローの作業項目履歴を確認して、ワークフローを終了する申請エラーが含まれるかどうかを確認します。
- 在庫仕訳帳は、承認されている場合にのみ更新または編集できます。 リコールが有効な場合は、仕訳帳を取り消してみてください。 ワークフロー バッチ ジョブの実行が複数の理由で中断される場合があります。 このような理由の一部は、ワークフロー フレームワークの問題が原因である可能性があります。
