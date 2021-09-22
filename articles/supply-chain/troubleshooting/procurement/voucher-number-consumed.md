---
title: 製品受領伝票番号は、伝票を生成しない場合でも消費される
description: 製品受領時に財務伝票が生成されていない場合でも、製品受領伝票番号が消費される
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476870"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>製品受領伝票番号は、伝票を生成しない場合でも消費される

## <a name="symptoms"></a>現象

製品受領書で財務伝票が生成されていない場合でも、製品受領伝票番号が消費されます。

## <a name="resolution"></a>解決策

品目モデルグループで **製品受領書の未収負債** オプションが *いいえ* に設定されている場合、一般会計への転記は行われません。 ただし、補助元帳で会計を目的として現物イベントが記録され、そのイベントに伝票番号が必要な場合があります。 この伝票番号は、在庫トランザクションで参照される伝票番号です。

[製品受領時に雑費を転記する](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/) のブログ記事に説明されている通り、**製品受領時に負債を見越計上** オプションを *はい* に設定することを推奨します。
