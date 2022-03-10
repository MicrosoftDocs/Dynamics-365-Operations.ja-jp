---
title: 注文の分割時に開始された検査指示の数量が更新されない
description: 検査指示を作成してそれを分割しようとすると、注文数量が分割された残りの数量に更新されません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713497"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>注文の分割時に開始された検査指示の数量が更新されない

KB 番号: 4613113

## <a name="symptoms"></a>現象

検査指示を作成してそれを分割しようとすると、注文数量が分割後の残り数量に更新されません。

## <a name="resolution"></a>解像度

検査指示で作成された元の数量を確実に追跡できるように、システムは検査指示から元の数量を変更しません。 ただし、検査指示から分割される数量はシステムによって追跡されます。 この追跡を行うには、`QuantityThatHasSplitIntoOtherQuarantineOrders` という名前の付いたデータベース フィールドが使用されます。 ただし、このフィールドはユーザー インターフェイス (UI) に表示されません。
