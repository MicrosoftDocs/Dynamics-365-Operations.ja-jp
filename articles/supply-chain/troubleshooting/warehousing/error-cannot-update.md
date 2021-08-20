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
ms.openlocfilehash: da5905fb7ed1e890c85e891843379aa07de3279bd8972d6fc57136aa703c9ea4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762797"
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
