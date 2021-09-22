---
title: インポートされた注文明細行に売買契約条件が適用されない
description: 売買契約価格および割引は、データ管理を介してインポートされた販売明細行または発注書明細行には適用されない
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476904"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>インポートされた注文明細行に売買契約条件が適用されない

## <a name="symptoms"></a>現象

販売注文または発注書の明細行に適用可能な売買契約は、データ管理を介してインポートされた明細行には適用されません。 ただし、手動で作成された販売注文または発注書の明細行には、同じ売買契約が適用されます。

## <a name="cause"></a>原因

データ管理を介してインポートされた発注書の明細行に価格情報が既に含まれている場合、それらの明細行に対する売買契約は再評価されません。 たとえば、**行割引の割合** または価格と割引のいずれかの値が、明細行に設定されている場合、その明細行に対して売買契約は検索されません。

## <a name="workaround"></a>回避策

この動作は予期されるものであり、販売注文と発注書の両方で類似しています。

回避策として、価格情報を設定せずに発注書の明細行をインポートします。 その結果、売買契約が適用され、定義された売買契約に基づいて発注書の明細行が更新されます。
