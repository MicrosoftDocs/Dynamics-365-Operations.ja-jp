---
title: X++ データの選択と操作の概要
description: このトピックでは、X++ データの選択と操作についてのトピックへのリンクを提供します。
author: robinarh
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 5367c141e11734eb65296d648e8c21df8d91fa02
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753018"
---
# <a name="x-data-selection-and-manipulation-overview"></a><span data-ttu-id="d23bc-103">X++ データの選択と操作の概要</span><span class="sxs-lookup"><span data-stu-id="d23bc-103">X++ data selection and manipulation overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d23bc-104">データベースに格納されているデータを取得し変更するため、SQL ステートメントを対話式またはソース コード内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d23bc-104">You can use SQL statements, either interactively or in source code, to retrieve and modify data that is stored in the database.</span></span> <span data-ttu-id="d23bc-105">これらのタスクには、**select** ステートメントおよび API メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d23bc-105">You can use the **select** statement and API methods for these tasks:</span></span>

- <span data-ttu-id="d23bc-106">[データの選択](xpp-select.md): 表示または変更するデータを選択します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-106">[Select data](xpp-select.md): Select the data to view or modify.</span></span>

    - <span data-ttu-id="d23bc-107">**[select](xpp-select-statement.md) ステートメント** – レコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="d23bc-107">**[select](xpp-select-statement.md) statement** – Fetch records.</span></span>

- <span data-ttu-id="d23bc-108">[データの挿入](xpp-insert.md): 1 つ以上の新しいレコードをテーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-108">[Insert data](xpp-insert.md): Add one or more new records to a table.</span></span>

    - <span data-ttu-id="d23bc-109">**[insert](xpp-insert.md#insert-method) および [doInsert](xpp-insert.md#do-insert-method) メソッド** – 一度に 1 つのレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-109">**[insert](xpp-insert.md#insert-method) and [doInsert](xpp-insert.md#do-insert-method) methods** – Insert one record at a time.</span></span>
    - <span data-ttu-id="d23bc-110">**[insert\_recordset](xpp-insert.md#insert-recordset-statement)、[RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)、および [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) メソッド** – 複数のレコードを同時に挿入します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-110">**[insert\_recordset](xpp-insert.md#insert-recordset-statement), [RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase), and [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) methods** – Insert multiple records at the same time.</span></span>

- <span data-ttu-id="d23bc-111">[データの更新](xpp-update.md): 既存のテーブル レコードでデータを変更します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-111">[Update data](xpp-update.md): Modify the data in existing table records.</span></span>

    - <span data-ttu-id="d23bc-112">**[update](xpp-update.md#update-method) および [doUpdate](xpp-update.md#do-update-method) メソッド** – 一度に 1 つのレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-112">**[update](xpp-update.md#update-method) and [doUpdate](xpp-update.md#do-update-method) methods** – Update one record at a time.</span></span>
    - <span data-ttu-id="d23bc-113">**[update\_recordset](xpp-update.md#update-recordset-statement) ステートメント** – 複数のレコードを同時に更新します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-113">**[update\_recordset](xpp-update.md#update-recordset-statement) statement** – Update multiple records at the same time.</span></span>

- <span data-ttu-id="d23bc-114">[データの削除](xpp-delete.md): 既存のレコードをテーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-114">[Delete data](xpp-delete.md): Remove existing records from a table.</span></span>

    - <span data-ttu-id="d23bc-115">**[delete](xpp-delete.md#delete-method) および [doDelete](xpp-delete.md#do-delete-method) メソッド** – 一度に 1 つのレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-115">**[delete](xpp-delete.md#delete-method) and [doDelete](xpp-delete.md#do-delete-method) methods** – Delete one record at a time.</span></span>
    - <span data-ttu-id="d23bc-116">**[delete\_from](xpp-delete.md#delete-from-statement) ステートメント** – 複数のレコードを同時に削除します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-116">**[delete\_from](xpp-delete.md#delete-from-statement) statement** – Delete multiple records at the same time.</span></span>

<span data-ttu-id="d23bc-117">データ アクセスに使用するその他のステートメントを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-117">Here are some other statements that you will use in data access:</span></span>

- <span data-ttu-id="d23bc-118">[while select](xpp-while-select.md) ステートメント</span><span class="sxs-lookup"><span data-stu-id="d23bc-118">[while select](xpp-while-select.md) statement</span></span>
- <span data-ttu-id="d23bc-119">[select](xpp-select-expression.md) 式</span><span class="sxs-lookup"><span data-stu-id="d23bc-119">[select](xpp-select-expression.md) expression</span></span>
- <span data-ttu-id="d23bc-120">[next](xpp-select.md) ステートメント</span><span class="sxs-lookup"><span data-stu-id="d23bc-120">[next](xpp-select.md) statement</span></span>

<span data-ttu-id="d23bc-121">[トランザクションの整合性](xpp-transaction.md) により、データの破損を防ぎ、スケーラビリティを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="d23bc-121">[Transactional integrity](xpp-transaction.md) helps prevent data corruption and improve scalability.</span></span>

<span data-ttu-id="d23bc-122">[セット ベースからレコード単位への操作の変換](xpp-data-perf.md) トピックでは、レコード セット ベースのステートメントおよびメソッドをより効率的に使用するための情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d23bc-122">The [Conversion of operations from set-based to record-by-record](xpp-data-perf.md) topic provides information about how you can use the record set–based statements and methods more efficiently.</span></span>

<span data-ttu-id="d23bc-123">[SysDa クラス](../sysda.md)を使用してデータを取得および変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="d23bc-123">You can also use the [SysDa classes](../sysda.md) to retrieve and modify data.</span></span> <span data-ttu-id="d23bc-124">拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。</span><span class="sxs-lookup"><span data-stu-id="d23bc-124">The extensible SysDa API provides almost all the data access possibilities that are available in X++.</span></span>

<span data-ttu-id="d23bc-125">**executeQueryWithParameters** API は、[SQL インジェクション攻撃の軽減](../query-with-parameters.md) に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d23bc-125">The **executeQueryWithParameters** API can help [mitigate a SQL injection attack](../query-with-parameters.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]