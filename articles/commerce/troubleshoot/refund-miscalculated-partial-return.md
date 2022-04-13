---
title: 返品数量に基づいて間違って計算された払戻可能な請求金額
description: このトピックには、レジ担当者が、販売時点管理 (POS) で、返品された品目の数量に対する払戻額が誤っていることに気づいた場合に使用できるトラブルシューティング ガイドが含まれています。
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/28/2022
ms.locfileid: "8490216"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>返品数量に基づいて間違って計算された払戻可能な請求金額

[!include [banner](../../includes/banner.md)]

このトピックには、レジ担当者が、販売時点管理 (POS) で、返品された品目の数量に対する払戻額が誤っていることに気づいた場合に使用できるトラブルシューティング ガイドが含まれています。

## <a name="description"></a>Description

顧客は、明細行レベルの払戻可能な請求金額を含む販売注文に対して購入した品目の一部を返品します。 しかし、POS では、払戻の一部が表示される代わりに、すべての請求金額が払戻可能として表示されます。

たとえば、顧客が、1 つ $5 の品目を 5 つ購入して、合計 $25 支払ったとします。 この顧客は 5 つの内 3 つの品目を返品しました。 ただし、レジ担当者には、返品された 3 つの品目の合計 $15 ではなく、払戻可能金額 $25 が POS に表示されます。

## <a name="resolution"></a>解決策

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>払戻された数量に基づく払戻請求を有効化機能をオンにする

Microsoft Dynamics 365 Commerce のバージョン 10.0.26 では、**払戻された数量に基づく払戻請求を有効化** 機能を使用すると、返品された数量に基づいて、明細行レベルの払戻可能金額を計算することができます。

Commerce 本社の **払戻された数量に基づく払戻請求の有効化** 機能を有効にするには、次の手順に従います。

1. **機能管理** ワークスペース (**システム管理者 \> ワークスペース \> 機能管理**) を開きます。
1. 使用可能な機能の一覧で、**払戻された数量に基づく払戻請求の有効化** 機能を検索して選択します。
1. 右側のペインで、**今すぐ有効にする** を選択します。
