---
title: 販売注文ページで支払タイプが、クレジット カード エラーである必要があります
description: このトピックでは、注文の同期後に販売注文ページにエラー メッセージが表示される場合に役立つトラブルシューティングガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018413"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>販売注文ページで、"支払タイプが、クレジット カード" エラーである必要があります

[!include [banner](../../includes/banner.md)]

このトピックでは、注文の同期後に販売注文ページにエラー メッセージが表示される場合に役立つトラブルシューティングガイドを示します。

## <a name="description"></a>説明

注文を同期した後に販売注文ページを開くと、"クレジット カード番号が指定されているので、支払タイプはクレジット カードである必要があります。" というエラー メッセージが表示されます

![支払タイプはクレジット カード エラーである必要があります](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>解像度

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Commerce 本社での支払タイプの設定

1. **売掛金勘定 \> 支払設定 \> 支払条件** の順に移動します。
1. 左ナビゲーションで、支払条件を選択します。
1. **支払タイプ** フィールドで、**クレジット カード** が選択されている必要があります。

## <a name="additional-resources"></a>追加リソース

[オンラインの販売と支払の転記](../tasks/posting-online-sales-payments.md)
