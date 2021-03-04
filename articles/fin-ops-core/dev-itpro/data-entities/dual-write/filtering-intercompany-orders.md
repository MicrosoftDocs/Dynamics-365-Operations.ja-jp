---
title: '[Orders] と [OrderLines] の同期を回避するために会社間注文をフィルターする'
description: このトピックは会社間注文をフィルターして [Orders] と [OrderLines] の同期を回避する方法について説明します。
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701036"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>[Orders] と [OrderLines] の同期を回避するために会社間注文をフィルターする

[!include [banner](../../includes/banner.md)]

会社間注文をフィルター処理して **注文** エンティティと **OrderLines** エンティティの同期を回避できます。 一部のシナリオでは、Customer Engagement アプリで会社間注文の詳細は必要ありません。

各標準 Common Data Service エンティティは、**IntercompanyOrder** フィールドへの参照を使用して拡張され、デュアル書き込みマップは、フィルターの追加フィールドを参照するように変更されます。 この結果、会社間注文が同期されなくなります。 このプロセスは、Customer Engagement アプリで不要なデータを回避します。

1. **IntercompanyOrder** の参照を **CDS 販売注文ヘッダー** に追加します。 この値は、会社間注文に対してのみ設定されます。 フィールド **IntercompanyOrder** は、**SalesTable** で使用できます。

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="ターゲット、SalesOrderHeader にステージングをマッピングする":::
    
2. **CDS 販売注文ヘッダー** が拡張されたら、マッピングで **IntercompanyOrder** フィールドが使用可能になります。 フィルターを `INTERCOMPANYORDER == ""` でクエリ文字列として適用します。

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="販売注文ヘッダー、クエリの編集":::

3. **IntercompanyInventTransId** への参照を **CDS 販売注文明細行** に追加します。  この値は、会社間注文に対してのみ設定されます。 フィールド **InterCompanyInventTransID** は、**SalesLine** で使用できます。

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="ターゲット、SalesOrderLine にステージングをマッピングする":::

4. **CDS 販売注文ヘッダー** が拡張されたら、マッピングで **IntercompanyInventTransId** フィールドが使用可能になります。 フィルターを `INTERCOMPANYINVENTTRANSID == ""` でクエリ文字列として適用します。

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="販売注文明細行、クエリを編集":::

5. ステップ 1 とステップ 2 で Common Data Service エンティティを拡張したときと同じ方法で、**売上請求書のヘッダー V2** と **売上請求書の明細行 V2** を拡張します。 次に、フィルター クエリを追加します。 **売上請求書ヘッダー V2** のフィルター文字列は、`(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` になります。 **売上請求書の明細行 V2** のフィルター文字列は、`INTERCOMPANYINVENTTRANSID == ""` になります。

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="ターゲット、販売請求書ヘッダーにステージングをマッピングする":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="販売請求書ヘッダー、クエリの編集":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="販売請求書の明細行、クエリの編集":::

6. **見積書** エンティティには会社間関係がありません。 他のユーザーが会社間顧客に対する見積を作成した場合は、**CustGroup** フィールドを使用して、これらのすべての顧客を 1 つの顧客グループに含めることができます。  ヘッダーと明細行を拡張して **CustGroup** フィールドを追加してから、このグループを含めないようにフィルターすることもできます。

    :::image type="content" source="media/filter-cust-group.png" alt-text="ターゲット、Sales Quotation Headerにステージングをマッピングする":::

7. **見積** エンティティの範囲を指定したら、クエリ文字列として `CUSTGROUP !=  "<company>"` にフィルターを適用します。

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="販売見積ヘッダー、クエリの編集":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]