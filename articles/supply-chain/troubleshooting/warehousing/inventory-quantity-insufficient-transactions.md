---
title: トランザクションが不十分なために在庫数量が更新されない
description: 指定された分析コードを持つ品目 %2 に対し十分な在庫トランザクションがないために、在庫数量 -1% を更新できない可能性があります。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476827"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>トランザクションが不十分なのでシステムが在庫数量を更新できない

## <a name="symptoms"></a>現象

この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。 次のエラー メッセージが表示されます。

> 品目 %2 (分析コード サイズ=%3、色=%4、追加=%5、サイト=%6、倉庫=%7、場所=%8、在庫ステータス=あり、ライセンス プレート=%9、ロット ID %12 での参照 ID %11 のバッチ番号=%10) の在庫トランザクションが不足しているため、在庫数量 -%1 を更新できませんでした。

## <a name="resolution"></a>解決策

在庫トランザクションで、数量が物理的に引当されていないことを確認してください。 たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。
