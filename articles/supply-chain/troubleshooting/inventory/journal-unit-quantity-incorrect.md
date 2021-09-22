---
title: 在庫仕訳帳で単位と単位数量が正しく機能しない
description: 在庫仕訳帳で単位と単位数量が正しく機能しない
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476857"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>在庫仕訳帳で単位と単位数量が正しく機能しない

## <a name="symptoms"></a>現象

在庫仕訳帳の単位と数量を使用すると、次のいずれかの問題が発生する場合があります。

- リリースされた製品に換算単位が設定されている間は、在庫仕訳帳に単位数量または単位数量は表示されません。また、在庫仕訳帳で単位を変更したりは変更できます。
- 在庫仕訳帳には **数量** フィールドと **単位** フィールドが表示されますが、**単位数量** フィールド は表示されます。 単位を変更して数量を入力して仕訳帳を転記すると、仕訳帳には引き続きその数量の元の測定単位が表示されます。

## <a name="resolution"></a>解決策

この問題を解決するには、次の手順に従います。

1. **機能管理** ワークスペースで、*在庫仕訳帳の測定単位と単位数量の使用* 機能が有効になっていることを確認します。 この機能により、**単位** と **単位数量** フィールドが仕訳帳に追加されます。
1. 機能が有効になった後は、次の方法で **数量**、**単位数量**、**単位** フィールドを使用します。

    - **数量** - リリースされた製品に対して定義されている既定の単位を使用して数量を指定します。 ただし、既定の単位自体は、ここには表示されません。 既定の単位と **単位** フィールドで選択した単位の間に換算が設定されている場合、**数量** フィールドは、**単位数量** フィールドと **単位** フィールドでの選択内容に基づいて自動的に更新されます。
    - **単位数量** – **単位** フィールドで選択された単位を使った数量を指定します。
    - **単位** - **単位数量** フィールドの値に適用する単位を選択します。
