---
title: 注文ステータスが請求後も部分的にリリースされたままになる
description: 場合によっては、販売注文のステータスが注文の請求が行われた後も部分的にリリースされたままになることがあります。 このページでは、理由と回避策について説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476886"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>注文ステータスが販売注文の請求が行われた後も部分的にリリースされたままになる

## <a name="symptoms"></a>現象

販売注文は出荷注文ですが、その中の 1 つ以上の品目の荷渡方法が異なります。 注文が請求された後も、まだリリース ステータスが *部分的にリリース済み* になっています。

たとえば、販売注文には配送用と集荷用の 2 つの項目があります。 出荷と集荷の両方が完了しています。 したがって、両方の明細行が請求されています。 ただし、リリース ステータスはまだ *部分的にリリース済み* と表示されますが、これは誤解を招くことになります。

## <a name="workaround"></a>回避策

リリース ステータスは、品目が倉庫管理に対して有効になっている注文明細行に対してのみ適用されます。 したがって、このシナリオではリリース ステータスが *部分的にリリース済み* の ままになります。 Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 リリース ステータスを更新するには、梱包明細および請求プロセスの一部として拡張機能を追加することができます。
