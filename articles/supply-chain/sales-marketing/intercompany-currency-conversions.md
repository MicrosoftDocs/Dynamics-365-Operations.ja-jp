---
title: 会社間通貨換算
description: このトピックでは、会社間取引の通貨換算について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f0af05c324bb67744ba6650e3d7a4ba8b958040e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671901"
---
# <a name="intercompany-currency-conversions"></a>会社間通貨換算

[!include [banner](../../includes/banner.md)]

元の販売注文と会社間発注書の通貨コードが異なる場合、同期が有効になっていると、次のフィールドは通貨換算されます:

- **単価**
- **販売諸費用** または **仕入諸掛**
- **割引**
- **複数行割引**

これらのフィールドは、会社間販売注文明細行と同期されます。

ただし、会社間発注書と会社間販売注文書の通貨は常に同期されるため、次のフィールドは通貨換算を使用せずに同期化されます:

- **単価**
- **販売諸費用** または **仕入諸掛**
- **割引**
- **割引率**
- **複数行割引**
- **複数行割引の割合**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
