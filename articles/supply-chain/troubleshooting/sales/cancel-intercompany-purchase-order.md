---
title: 販売注文にリンクされている会社間発注書をキャンセルできません
description: Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.13 およびそれ移行では、販売注文にリンクされている会社間発注書をキャンセルできるようになりました。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5041ef377d9bf2c21e191c3cf1950f47eeba8555
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476863"
---
# <a name="cant-cancel-an-intercompany-purchase-order-thats-linked-to-a-sales-order"></a>販売注文にリンクされている会社間発注書をキャンセルできません

## <a name="symptoms"></a>現象

販売注文にリンクされている会社間発注書をキャンセルしようとする場合は、次のエラー メッセージが表示される場合があります。

> 残余更新数量によって符号が変わるため、数量を減らすことはできません。

## <a name="resolution"></a>解決策

この問題は、Microsoft Dynamics 365 Supply Chain Management バージョン10.0.13 で修正されました。 これ以降のバージョンでは、販売注文にリンクされている会社間発注書をキャンセルできるようになりました。
