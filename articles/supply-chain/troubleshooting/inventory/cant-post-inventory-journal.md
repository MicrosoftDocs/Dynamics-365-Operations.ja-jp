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
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476838"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>在庫仕訳帳ワークフローが未完了なので、仕訳帳を処理できません

## <a name="symptoms"></a>現象

仕訳帳承認ワークフローを送信すると、ワークフロー処理の応答が停止され、仕訳帳を編集または処理できます。

## <a name="resolution"></a>解決策

ワークフロー処理が完了しないのはいくつかの理由があります。 次の問題を確認してください。

- **在庫管理 &gt; 設定 &gt; 在庫管理ワークフロー** に移動し、影響を受けるワークフローの構成を確認します。 詳細については、[仕訳帳承認ワークフロー](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md) を参照してください。
- ワークフローに例外またはエラーが発生する可能性があります。 影響を受けるワークフローの作業項目履歴を確認して、ワークフローを終了する申請エラーが含まれるかどうかを確認します。
- 在庫仕訳帳は、承認されている場合にのみ更新または編集できます。 リコールが有効な場合は、仕訳帳を取り消してみてください。 ワークフロー バッチ ジョブの実行が複数の理由で中断される場合があります。 このような理由の一部は、ワークフロー フレームワークの問題が原因である可能性があります。
