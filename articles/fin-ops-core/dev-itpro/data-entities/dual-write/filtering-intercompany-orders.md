---
title: 会社間注文をフィルター処理して Orders および OrderLines の同期を回避する
description: このトピックでは、会社間注文をフィルタ処理して、Orders と OrderLines エンティティが同期されないようにする方法について説明します。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 342db8c1b4337145bfd61f5698ff6de25434a400
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796609"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="1a98f-103">会社間注文をフィルター処理して Orders および OrderLines の同期を回避する</span><span class="sxs-lookup"><span data-stu-id="1a98f-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a98f-104">会社間注文をフィルター処理して **Orders** テーブルと **OrderLines** テーブルが同期されないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="1a98f-105">一部のシナリオでは、Customer Engagement アプリで会社間注文の詳細は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="1a98f-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="1a98f-106">各標準 Dataverse テーブルは、**IntercompanyOrder** 列への参照を使用して拡張され、デュアル書き込みマップは、フィルターの追加列を参照するように変更されます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="1a98f-107">したがって、会社間注文は同期されなくなります。</span><span class="sxs-lookup"><span data-stu-id="1a98f-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="1a98f-108">このプロセスは、Customer Engagement アプリで不要なデータを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="1a98f-109">**IntercompanyOrder** 列への参照を追加して、**CDS 販売注文ヘッダー** テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="1a98f-110">この列は、会社間注文でのみ入力されます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="1a98f-111">**IntercompanyOrder** 列は、**SalesTable** テーブルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS 販売注文ヘッダーのターゲット ページにステージングをマップする":::

2. <span data-ttu-id="1a98f-113">**CDS 販売注文ヘッダー** が拡張されたら、マッピングで **IntercompanyOrder** 列が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="1a98f-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="1a98f-114">クエリ文字列として `INTERCOMPANYORDER == ""` を含むフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS 販売注文ヘッダーのクエリ ダイアログ ボックスを編集する":::

3. <span data-ttu-id="1a98f-116">**IntercompanyInventTransId** 列への参照を追加して、**CDS 販売注文明細行** テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="1a98f-117">この列は、会社間注文でのみ入力されます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="1a98f-118">**InterCompanyInventTransId** 列は、**SalesLine** テーブルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS 販売注文明細行のターゲット ページにステージングをマップする":::

4. <span data-ttu-id="1a98f-120">**CDS 販売注文明細行** が拡張されたら、マッピングで **IntercompanyInventTransId** 列が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="1a98f-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="1a98f-121">クエリ文字列として `INTERCOMPANYINVENTTRANSID == ""` を含むフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS 販売注文明細行のクエリ ダイアログ ボックスを編集する":::

5. <span data-ttu-id="1a98f-123">手順 1 と 2 を繰り返して、**売上請求書ヘッダー V2** テーブルを拡張し、フィルター クエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="1a98f-124">この場合は、フィルターのクエリ文字列として `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="売上請求書ヘッダー V2 のターゲット ページにステージングをマップする":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="売上請求書ヘッダー V2 のクエリ ダイアログ ボックスを編集する":::

6. <span data-ttu-id="1a98f-127">手順 3 と 4 を繰り返して、**売上請求明細行 V2** テーブルを拡張し、フィルター クエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="1a98f-128">この場合は、フィルターのクエリ文字列として `INTERCOMPANYINVENTTRANSID == ""` を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="売上請求明細行 V2 のクエリ ダイアログ ボックスを編集する":::

7. <span data-ttu-id="1a98f-130">**見積書** テーブルには会社間関係がありません。</span><span class="sxs-lookup"><span data-stu-id="1a98f-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="1a98f-131">他のユーザーが会社間顧客に対する見積を作成した場合は、**CustGroup** 列を使用して、そのすべての顧客を 1 つの顧客グループに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="1a98f-132">**CustGroup** 列を追加してヘッダーと行を拡張し、グループが含まれないようにフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="1a98f-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS 販売見積書ヘッダーのターゲット ページにステージングをマップする":::

8. <span data-ttu-id="1a98f-134">**見積書** を拡張した後、クエリ文字列として `CUSTGROUP != "<company>"` を含むフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="1a98f-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS 販売見積ヘッダーのクエリ ダイアログ ボックスを編集する":::
