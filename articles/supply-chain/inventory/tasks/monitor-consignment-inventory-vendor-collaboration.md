---
title: 仕入先コラボレーションを使用した委託販売在庫の監視
description: この手順は、顧客との委託販売で置いた製品の在庫レベルに関する情報を表示する際の仕入先との連携方法を示します。
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e397c12b9f605d1c864ce053477090ed8c1700
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839274"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>仕入先コラボレーションを使用した委託販売在庫の監視

[!include [banner](../../includes/banner.md)]

この手順は、顧客との委託販売で置いた製品の在庫レベルに関する情報を表示する際の仕入先との連携方法を示します。 顧客が在庫品目の所有権を取得したときの在庫品目の移動状況をチェックすることができます。 デモ データの会社 USMF でこの手順を使用できます。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="view-consumed-inventory"></a>移動した在庫品目を表示する
1. [仕入先コラボレーション] > [委託販売在庫] > [委託販売在庫から受領された製品] の順に移動します。
    * リストは、委託製品在庫の所有権が仕入先から顧客に変更されたとき生成された製品受領明細行を示します。 数量およびその他の情報を確認するには、右にスクロールします。 このリストにある情報で顧客の請求書を生成することができます。 また、データを Microsoft Excel にエクスポートできます。   
2. [発注書を表示] をクリックします。
3. [明細行の詳細] セクションを展開します。
    * 明細行が委託製品としてマークされます。ヘッダー セクションは発注書が「受領」の状態であることを示します。  
4. ページを閉じます。

## <a name="view-on-hand-inventory"></a>手持在庫の表示
1. [仕入先コラボレーション] > [委託販売在庫] > [手持委託販売在庫] の順に移動します。
    * 手持委託製品在庫ページは、顧客の倉庫で所有している在庫を示します。 [規模のタブを表示] をクリックして、サイトや倉庫などその他の規模を表示できます。   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]