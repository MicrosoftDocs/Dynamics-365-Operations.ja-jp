---
title: 出荷残数をキャンセルすると、発注書が確認済の状態に移動します
description: 変更管理が有効になっている発注書で出荷更新待ちがキャンセルされた場合、発注書は確認済状態になります
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476888"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>出荷残数をキャンセルすると、発注書が確認済の状態に移動します

## <a name="symptoms"></a>現象

変更管理の対象となる発注書の場合、要求される唯一の変更が 1 つ以上の明細行の出荷残余の取消である場合、発注書は承認された時点で直接 *確認済* 状態になり、仕訳帳は作成されません。

## <a name="resolution"></a>解決策

配送残余をキャンセルしても、確認仕訳帳の内容には影響しません。 この機能は、明細行が部分的に入庫され、発注書が仕入先に対して確認された後に、プロセス ステップで残余品質をキャンセルする必要がある場合に使用します。

この数量を発注書の確認書に反映する必要がある場合は、購買注文明細行で数量を調整して、確認が必要になるようにする必要があります。 また、その明細行に何も入庫されていない場合は、数量を削除できます。 この場合、再確認が要求されます。
