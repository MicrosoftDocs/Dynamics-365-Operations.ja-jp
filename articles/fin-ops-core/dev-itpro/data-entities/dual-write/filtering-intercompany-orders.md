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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="bb95b-103">[Orders] と [OrderLines] の同期を回避するために会社間注文をフィルターする</span><span class="sxs-lookup"><span data-stu-id="bb95b-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb95b-104">会社間注文をフィルター処理して **注文** エンティティと **OrderLines** エンティティの同期を回避できます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="bb95b-105">一部のシナリオでは、Customer Engagement アプリで会社間注文の詳細は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="bb95b-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="bb95b-106">各標準 Common Data Service エンティティは、**IntercompanyOrder** フィールドへの参照を使用して拡張され、デュアル書き込みマップは、フィルターの追加フィールドを参照するように変更されます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="bb95b-107">この結果、会社間注文が同期されなくなります。</span><span class="sxs-lookup"><span data-stu-id="bb95b-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="bb95b-108">このプロセスは、Customer Engagement アプリで不要なデータを回避します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="bb95b-109">**IntercompanyOrder** の参照を **CDS 販売注文ヘッダー** に追加します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="bb95b-110">この値は、会社間注文に対してのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="bb95b-111">フィールド **IntercompanyOrder** は、**SalesTable** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="ターゲット、SalesOrderHeader にステージングをマッピングする":::
    
2. <span data-ttu-id="bb95b-113">**CDS 販売注文ヘッダー** が拡張されたら、マッピングで **IntercompanyOrder** フィールドが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="bb95b-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="bb95b-114">フィルターを `INTERCOMPANYORDER == ""` でクエリ文字列として適用します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="販売注文ヘッダー、クエリの編集":::

3. <span data-ttu-id="bb95b-116">**IntercompanyInventTransId** への参照を **CDS 販売注文明細行** に追加します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="bb95b-117">この値は、会社間注文に対してのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="bb95b-118">フィールド **InterCompanyInventTransID** は、**SalesLine** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="ターゲット、SalesOrderLine にステージングをマッピングする":::

4. <span data-ttu-id="bb95b-120">**CDS 販売注文ヘッダー** が拡張されたら、マッピングで **IntercompanyInventTransId** フィールドが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="bb95b-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="bb95b-121">フィルターを `INTERCOMPANYINVENTTRANSID == ""` でクエリ文字列として適用します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="販売注文明細行、クエリを編集":::

5. <span data-ttu-id="bb95b-123">ステップ 1 とステップ 2 で Common Data Service エンティティを拡張したときと同じ方法で、**売上請求書のヘッダー V2** と **売上請求書の明細行 V2** を拡張します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="bb95b-124">次に、フィルター クエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-124">Then add the filter queries.</span></span> <span data-ttu-id="bb95b-125">**売上請求書ヘッダー V2** のフィルター文字列は、`(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` になります。</span><span class="sxs-lookup"><span data-stu-id="bb95b-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="bb95b-126">**売上請求書の明細行 V2** のフィルター文字列は、`INTERCOMPANYINVENTTRANSID == ""` になります。</span><span class="sxs-lookup"><span data-stu-id="bb95b-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="ターゲット、販売請求書ヘッダーにステージングをマッピングする":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="販売請求書ヘッダー、クエリの編集":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="販売請求書の明細行、クエリの編集":::

6. <span data-ttu-id="bb95b-130">**見積書** エンティティには会社間関係がありません。</span><span class="sxs-lookup"><span data-stu-id="bb95b-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="bb95b-131">他のユーザーが会社間顧客に対する見積を作成した場合は、**CustGroup** フィールドを使用して、これらのすべての顧客を 1 つの顧客グループに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="bb95b-132">ヘッダーと明細行を拡張して **CustGroup** フィールドを追加してから、このグループを含めないようにフィルターすることもできます。</span><span class="sxs-lookup"><span data-stu-id="bb95b-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="ターゲット、Sales Quotation Headerにステージングをマッピングする":::

7. <span data-ttu-id="bb95b-134">**見積** エンティティの範囲を指定したら、クエリ文字列として `CUSTGROUP !=  "<company>"` にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="bb95b-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="販売見積ヘッダー、クエリの編集":::
