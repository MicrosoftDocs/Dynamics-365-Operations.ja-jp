---
title: 販売注文明細行で品目を構成すると、テキストが上書きされる
description: 販売注文明細行で製品が構成されている場合、変更されたテキストは標準テキストで上書きされます。 明細行を構成する前ではなく、構成した後にテキストを変更します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476830"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>販売注文明細行で製品を構成すると、品目テキストが上書きされる

## <a name="symptoms"></a>現象

この問題は、構成可能品目の販売注文明細行を作成し、品目テキストを変更した場合に発生します。 品目を構成してから **OK** をクリックすると、テキストは標準テキストで上書きされます。

## <a name="resolution"></a>解決策

この動作は予期されています。 テキスト フィールドには、バリアント名が含まれており、行を構成した後にのみ入力されます。 したがって、行を構成した後でなくても、テキストを変更する必要があります。
