---
title: 在庫仕訳帳がロックされている場合にワークフロー バッチ ジョブが機能しない
description: 使用している在庫仕訳帳の 1 つが、ある操作によってロックされ、ロック解除されない
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
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476849"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>在庫仕訳帳がロックされている場合にワークフロー バッチ ジョブが機能しない

## <a name="symptoms"></a>現象

使用している在庫仕訳帳の 1 つが、ある操作によってロックされ、ロック解除されません。 たとえば、転記中に不明なエラーが発生した場合 (システム ロック操作)、仕訳帳はシステム ロック状態のままです。 この場合、ワークフロー作業項目ハンドラーは検証をロックしている間にエラーを修正します。

## <a name="resolution"></a>解決策

Supply Chain Management の SQL Server インスタンスにログインし、**InventJournalTable.SystemBlocked** が *1* に設定されているかどうかを確認します。 その場合は、仕訳帳がロックの状態ではない事を確認してから、**InventJournalTable.SystemBlocked** を *0* にリセットしてください。
