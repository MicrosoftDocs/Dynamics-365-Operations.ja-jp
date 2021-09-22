---
title: ピッキング リスト登録時に場所が選択された場合にエラーが発生します
description: ピッキング リスト登録時に場所が選択された場合にエラーが発生します。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef34b4fdcc572c56319f6cbf4913d822d8857595
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474967"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>ピッキング リスト登録時に場所が選択された場合にエラーが発生します

KB 番号: 4613106

## <a name="symptoms"></a>現象

この問題は、販売注文の自動予約を自動的に行うシステムが構成されている場合に発生します。 ピッキング リスト登録行の場所を選択しようとする場合、倉庫管理 (WMS) の予約プロセスを使用するときに次のエラー メッセージが表示されます。

> 数量を新しい分析コードで更新できない

この問題は、指定した場所に十分な在庫がないので発生する可能性があります。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。

倉庫レベルの引当プロセスを使用する場合、すべての在庫分析コード レベルで在庫在庫の引当が行われなかったり、指定した場所に十分な在庫が存在しない場合は、ピッキング ラインからの手動引当プロセスを使用することをお勧めします。 その後、*ロットの引当* 機能を使用して、利用可能なすべての在庫数量に、在庫場所などの低い引当 を配分できます。
