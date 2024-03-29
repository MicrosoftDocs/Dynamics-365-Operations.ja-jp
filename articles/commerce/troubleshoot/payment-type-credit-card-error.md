---
title: 販売注文ページで支払タイプが、クレジット カード エラーである必要があります
description: この記事には、注文の同期後に販売注文ページにエラー メッセージが表示される場合に役立つトラブルシューティング ガイドが含まれます。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285635"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>販売注文ページで、"支払タイプが、クレジット カード" エラーである必要があります

[!include [banner](../../includes/banner.md)]

この記事には、注文の同期後に販売注文ページにエラー メッセージが表示される場合に役立つトラブルシューティング ガイドが含まれます。

## <a name="description"></a>説明

注文を同期した後に販売注文ページを開くと、"クレジット カード番号が指定されているので、支払タイプはクレジット カードである必要があります。" というエラー メッセージが表示されます

![支払タイプはクレジット カードである必要がありますというエラー。](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>解決策

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Commerce 本社での支払タイプの設定

1. **売掛金勘定 \> 支払設定 \> 支払条件** の順に移動します。
1. 左ナビゲーションで、支払条件を選択します。
1. **支払タイプ** フィールドで、**クレジット カード** が選択されている必要があります。

## <a name="additional-resources"></a>追加リソース

[オンラインの販売と支払の転記](../tasks/posting-online-sales-payments.md)
