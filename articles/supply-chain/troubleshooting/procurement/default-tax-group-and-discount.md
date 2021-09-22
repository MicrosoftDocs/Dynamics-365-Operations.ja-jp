---
title: 既定の税グループと現金割引が請求先/元 ID から入力されていません
description: 既定の税グループと既定の現金割引が請求先/元 ID から入力されていません
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476869"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>既定の税グループと現金割引が請求先/元 ID から入力されていません

## <a name="symptoms"></a>現象

顧客 ID とは異なる請求元仕入先を使用している場合、既定の税グループと既定の現金割引は、発注書が作成されるときに請求先/元 ID から入力されません。

## <a name="resolution"></a>解決策

この動作は仕様です。 税グループ、現金割引、およびその他の価格情報の既定値は、請求先/元 ID ではなく顧客 ID に基づいています。
