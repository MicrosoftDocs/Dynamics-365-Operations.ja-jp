---
title: X++ データの選択と操作の概要
description: このトピックでは、X++ 言語での select ステートメントについて説明します。
author: robinarh
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150273
ms.search.region: Global
ms.author: robinr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 0788129db2ebb809601be770b3233b88aeff4bab
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505952"
---
# <a name="x-data-selection-and-manipulation-overview"></a><span data-ttu-id="d3911-103">X++ データの選択と操作の概要</span><span class="sxs-lookup"><span data-stu-id="d3911-103">X++ data selection and manipulation overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3911-104">データベースに格納されているデータを取得し変更するため、SQL ステートメントを対話的またはソース コード内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d3911-104">You can use SQL statements, either interactively or within source code, to retrieve and modify data that is stored in the database.</span></span> <span data-ttu-id="d3911-105">これらのタスクには、**select** ステートメントおよび API メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3911-105">You can use the **select** statement and API methods for these tasks:</span></span>

- <span data-ttu-id="d3911-106">[データの選択](xpp-select.md): 表示または変更するデータを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3911-106">[Select data](xpp-select.md): Select the data to view or modify.</span></span>

    - <span data-ttu-id="d3911-107">[select ステートメント](xpp-select-statement.md): レコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="d3911-107">[select statement](xpp-select-statement.md): Fetches records.</span></span>

- <span data-ttu-id="d3911-108">[データの挿入](xpp-insert.md): 1 つ以上の新しいレコードをテーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="d3911-108">[Insert data](xpp-insert.md): Add one or more new records to a table.</span></span>

    - <span data-ttu-id="d3911-109">[insert](xpp-insert.md#insert-method) および [doinsert](xpp-insert.md#do-insert-method) メソッド: 一度に 1 つのレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="d3911-109">[insert](xpp-insert.md#insert-method) and [doInsert](xpp-insert.md#do-insert-method) methods: Insert one record at a time.</span></span>
    - <span data-ttu-id="d3911-110">[insert\_recordset](xpp-insert.md#insert-recordset-statement)、[RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)、および [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) メソッド: 複数のレコードを同時に挿入します。</span><span class="sxs-lookup"><span data-stu-id="d3911-110">[insert\_recordset](xpp-insert.md#insert-recordset-statement), [RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase), and [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) methods: Insert multiple records at the same time.</span></span>

- <span data-ttu-id="d3911-111">[データの更新](xpp-update.md): 既存のテーブル レコードでデータを変更します。</span><span class="sxs-lookup"><span data-stu-id="d3911-111">[Update data](xpp-update.md): Modify data in existing table records.</span></span>

    - <span data-ttu-id="d3911-112">[update](xpp-update.md#update-method) および [doUpdate](xpp-update.md#do-update-method) メソッド: 一度に 1 つのレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="d3911-112">[update](xpp-update.md#update-method) and [doUpdate](xpp-update.md#do-update-method) methods: Update one record at a time.</span></span>
    - <span data-ttu-id="d3911-113">[update\_recordset](xpp-update.md#update-recordset-statement) ステートメント: 複数のレコードを同時に更新します。</span><span class="sxs-lookup"><span data-stu-id="d3911-113">[update\_recordset](xpp-update.md#update-recordset-statement) statement: Updates multiple records at the same time.</span></span>

- <span data-ttu-id="d3911-114">[データの削除](xpp-delete.md): 既存のレコードをテーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="d3911-114">[Delete data](xpp-delete.md): Remove existing records from a table.</span></span>

    - <span data-ttu-id="d3911-115">[delete](xpp-delete.md#delete-method) および [doDelete](xpp-delete.md#do-delete-method) メソッド: 一度に 1 つのレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="d3911-115">[delete](xpp-delete.md#delete-method) and [doDelete](xpp-delete.md#do-delete-method) methods: Delete one record at a time.</span></span>
    - <span data-ttu-id="d3911-116">[delete\_from](xpp-delete.md#delete-from-statement) ステートメント: 複数のレコードを同時に削除します。</span><span class="sxs-lookup"><span data-stu-id="d3911-116">[delete\_from](xpp-delete.md#delete-from-statement) statement: Deletes multiple records at the same time.</span></span>

<span data-ttu-id="d3911-117">データ アクセスに使用するその他のステートメントを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d3911-117">Other statements that you'll use in data access are:</span></span>

- <span data-ttu-id="d3911-118">[while select](xpp-while-select.md) ステートメント。</span><span class="sxs-lookup"><span data-stu-id="d3911-118">[while select](xpp-while-select.md) statement.</span></span>
- <span data-ttu-id="d3911-119">[select 式](xpp-select-expression.md)。</span><span class="sxs-lookup"><span data-stu-id="d3911-119">[select expression](xpp-select-expression.md).</span></span>
- <span data-ttu-id="d3911-120">[next](xpp-select.md) ステートメント。</span><span class="sxs-lookup"><span data-stu-id="d3911-120">[next](xpp-select.md) statement.</span></span>

<span data-ttu-id="d3911-121">[トランザクションの整合性](xpp-transaction.md)により、データの破損を防ぎ、スケーラビリティを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="d3911-121">[Transactional integrity](xpp-transaction.md) helps prevent data corruption and help improve scalability.</span></span>

<span data-ttu-id="d3911-122">[セット ベースからレコードごとへの操作の変換](xpp-data-perf.md)では、レコードセット ベースのステートメントおよびメソッドを効率的に使用するための追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3911-122">[Conversion of operations from set-based to record-by-record](xpp-data-perf.md) provides additional information on using the recordset-based statements and methods efficiently.</span></span>

<span data-ttu-id="d3911-123">[SysDa クラス](../sysda.md)を使用してデータを取得および変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="d3911-123">You can also use the [SysDa classes](../sysda.md) to retrieve and modify data.</span></span> <span data-ttu-id="d3911-124">拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。</span><span class="sxs-lookup"><span data-stu-id="d3911-124">The extensible SysDa API provides almost all the data access possibilities that are available in X++.</span></span>
