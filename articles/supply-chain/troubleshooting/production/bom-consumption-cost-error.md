---
title: BOM consumptionCost 値が注文を終了しようとする場合にエラーが発生する
description: 製造オーダーを終了しようとしている場合は、BOM consumptionCost 値が負である必要があるというエラー メッセージが表示される場合があります。 問題が修正されました。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 737329d06022e899df8e4de5a27d76b21480da9e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476883"
---
# <a name="cant-end-a-production-order-because-of-a-bom-consumptioncost-value-error"></a>BOM consumptionCost 値のエラーが原因で製造オーダーを終了できない

## <a name="symptoms"></a>現象

製造オーダーを終了しようとする際に、次のエラー メッセージが表示されます:

> BOM consumptionCost 値の計算は、在庫からの発行時に負である必要があります。

## <a name="resolution"></a>解決策

この問題は、リリース 10.0.15 で修正されました。
