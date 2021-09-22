---
title: キャンセルされた発注書は、ワークスペースの下書き一覧に表示されます
description: キャンセルされた発注書は、発注書準備ワークスペースの下書き一覧に表示されます
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476898"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>キャンセルされた発注書は、ワークスペースの下書き一覧に表示されます

## <a name="symptoms"></a>現象

*確認済* 状態の発注書をキャンセルした後で、そのキャンセルされた発注書は、**発注書** 準備ワークスペースのドラフト発注書の一覧に表示されます。

## <a name="resolution"></a>解決策

この問題は、変更管理の対象になる発注書に対してのみ発生します。 これは、このキャンセルに必要のある変更が懸念されることから発生します。 この承認は、システムによって自動的に行うことができます。 したがって、このプロセスでは、キャンセルされた発注書を承認ワークフローに送信して、*承認済* 状態にすることができます。 この時点で、**発注書の準備** ワークスペースのドラフト発注書の一覧にその発注書が表示されなくなります。
