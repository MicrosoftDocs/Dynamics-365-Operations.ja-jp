---
title: プロセス レポートの間接原価には削除された製造オーダーが含まれます
description: プロセス レポートの間接原価には、部分的に処理され、後で削除された製造オーダーに関する情報が表示されます。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751772"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>プロセス レポートの間接原価には削除された製造オーダーが含まれます

KB 番号: 4612748

## <a name="symptoms"></a>現象

**プロセス レポートの間接原価** には、部分的に処理され、後で削除された製造オーダーに関する情報が表示されます。

## <a name="resolution"></a>解像度

製造オーダーを取り消す場合は、その製造オーダーのすべてのトランザクションも取り消します。 製造オーダーを削除すると、補助元帳テーブルと総勘定元帳に関連付いたすべてのトランザクションが保持されます。 レポートには、補助元帳テーブルのトランザクションが表示されます。 特定の製造オーダーの場合、正味値は 0.00 である必要があります。
