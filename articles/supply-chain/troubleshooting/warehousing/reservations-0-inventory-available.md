---
title: 0.00 を使用できるので在庫予約はできない
description: 在庫で使用できるのは 0.00 のみであるため、システムで予約できないというエラーが発生しました。 この問題は、未処理の作業が原因で発生している可能性があります。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476907"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>在庫で 0.00 を使用できるのでシステム予約はできません

## <a name="symptoms"></a>現象

この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。 次のエラー メッセージが表示されます。

> 在庫で使用できるのは 0.00 のみであるため、現物手持在庫 (サイト=%1、倉庫=%2、在庫ステータス=あり、バッチ番号=%3、所有者=%4: %5) を引当することはできません。

## <a name="resolution"></a>解決策

この問題は、未処理の作業が原因で発生している可能性があります。 作業を完了するか、作業の作成を行わずに入庫します。 在庫トランザクションで、数量が物理的に引当されていないことを確認してください。 たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。
