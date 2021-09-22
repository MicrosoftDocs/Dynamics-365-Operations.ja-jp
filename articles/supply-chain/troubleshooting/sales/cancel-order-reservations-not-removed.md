---
title: 注文のキャンセル時に引き出しは削除できません
description: その注文に関連付けられている作業がキャンセルされて取り消されるまで、販売注文をキャンセルすることはできません。 そのためには、次の 3 つの手順に従います。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476887"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>注文のキャンセル時に引き出しは削除できません

## <a name="symptoms"></a>現象

作業が販売注文に関連付けられ、その注文をキャンセルしようとする場合は、次のエラー メッセージが表示されます。

> 引当に依存する作業が作成されているために、引当を削除できません。

作業がキャンセルされて取り消されるまで、その販売注文をキャンセルすることはできません。 この要件は、販売注文に関連付けられている作業が終了されている場合にも適用されます。

## <a name="resolution"></a>解決策

この問題を解決するには、次の手順に従います:

1. 作業をキャンセルし、在庫を目的の場所に戻します。 販売注文の該当する負荷に移動し、読み込み行の **ピッキング済数量の削減** またはアクション ペインでの **作業の取消し** を選択します。

    この時点で、職場のステータスは *キャンセル済* になり、新しい在庫移動作業が自動的に作成および処理されて、在庫が取消時点で説明した保管場所に戻されます。

2. 負荷を削除します。 また、出荷も削除されます。

3. これで、販売注文に移動してキャンセルすることができます。
