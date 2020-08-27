---
title: X++ データの選択と操作の概要
description: このトピックでは、X++ データの選択と操作についてのトピックへのリンクを提供します。
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
ms.openlocfilehash: a468c3747a722c2e006dd17ff769922a418d5094
ms.sourcegitcommit: 94863c587e8acacc7c2e7811e84de66c312cc017
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/29/2020
ms.locfileid: "3637838"
---
# <a name="x-data-selection-and-manipulation-overview"></a><span data-ttu-id="1ee41-103">X++ データの選択と操作の概要</span><span class="sxs-lookup"><span data-stu-id="1ee41-103">X++ data selection and manipulation overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ee41-104">データベースに格納されているデータを取得し変更するため、SQL ステートメントを対話式またはソース コード内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1ee41-104">You can use SQL statements, either interactively or in source code, to retrieve and modify data that is stored in the database.</span></span> <span data-ttu-id="1ee41-105">これらのタスクには、**select** ステートメントおよび API メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1ee41-105">You can use the **select** statement and API methods for these tasks:</span></span>

- <span data-ttu-id="1ee41-106">[データの選択](xpp-select.md): 表示または変更するデータを選択します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-106">[Select data](xpp-select.md): Select the data to view or modify.</span></span>

    - <span data-ttu-id="1ee41-107">**[select](xpp-select-statement.md) ステートメント** – レコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="1ee41-107">**[select](xpp-select-statement.md) statement** – Fetch records.</span></span>

- <span data-ttu-id="1ee41-108">[データの挿入](xpp-insert.md): 1 つ以上の新しいレコードをテーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-108">[Insert data](xpp-insert.md): Add one or more new records to a table.</span></span>

    - <span data-ttu-id="1ee41-109">**[insert](xpp-insert.md#insert-method) および [doInsert](xpp-insert.md#do-insert-method) メソッド** – 一度に 1 つのレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-109">**[insert](xpp-insert.md#insert-method) and [doInsert](xpp-insert.md#do-insert-method) methods** – Insert one record at a time.</span></span>
    - <span data-ttu-id="1ee41-110">**[insert\_recordset](xpp-insert.md#insert-recordset-statement)、[RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)、および [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) メソッド** – 複数のレコードを同時に挿入します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-110">**[insert\_recordset](xpp-insert.md#insert-recordset-statement), [RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase), and [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) methods** – Insert multiple records at the same time.</span></span>

- <span data-ttu-id="1ee41-111">[データの更新](xpp-update.md): 既存のテーブル レコードでデータを変更します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-111">[Update data](xpp-update.md): Modify the data in existing table records.</span></span>

    - <span data-ttu-id="1ee41-112">**[update](xpp-update.md#update-method) および [doUpdate](xpp-update.md#do-update-method) メソッド** – 一度に 1 つのレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-112">**[update](xpp-update.md#update-method) and [doUpdate](xpp-update.md#do-update-method) methods** – Update one record at a time.</span></span>
    - <span data-ttu-id="1ee41-113">**[update\_recordset](xpp-update.md#update-recordset-statement) ステートメント** – 複数のレコードを同時に更新します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-113">**[update\_recordset](xpp-update.md#update-recordset-statement) statement** – Update multiple records at the same time.</span></span>

- <span data-ttu-id="1ee41-114">[データの削除](xpp-delete.md): 既存のレコードをテーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-114">[Delete data](xpp-delete.md): Remove existing records from a table.</span></span>

    - <span data-ttu-id="1ee41-115">**[delete](xpp-delete.md#delete-method) および [doDelete](xpp-delete.md#do-delete-method) メソッド** – 一度に 1 つのレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-115">**[delete](xpp-delete.md#delete-method) and [doDelete](xpp-delete.md#do-delete-method) methods** – Delete one record at a time.</span></span>
    - <span data-ttu-id="1ee41-116">**[delete\_from](xpp-delete.md#delete-from-statement) ステートメント** – 複数のレコードを同時に削除します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-116">**[delete\_from](xpp-delete.md#delete-from-statement) statement** – Delete multiple records at the same time.</span></span>

<span data-ttu-id="1ee41-117">データ アクセスに使用するその他のステートメントを次に示します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-117">Here are some other statements that you will use in data access:</span></span>

- <span data-ttu-id="1ee41-118">[while select](xpp-while-select.md) ステートメント</span><span class="sxs-lookup"><span data-stu-id="1ee41-118">[while select](xpp-while-select.md) statement</span></span>
- <span data-ttu-id="1ee41-119">[select](xpp-select-expression.md) 式</span><span class="sxs-lookup"><span data-stu-id="1ee41-119">[select](xpp-select-expression.md) expression</span></span>
- <span data-ttu-id="1ee41-120">[next](xpp-select.md) ステートメント</span><span class="sxs-lookup"><span data-stu-id="1ee41-120">[next](xpp-select.md) statement</span></span>

<span data-ttu-id="1ee41-121">[トランザクションの整合性](xpp-transaction.md) により、データの破損を防ぎ、スケーラビリティを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="1ee41-121">[Transactional integrity](xpp-transaction.md) helps prevent data corruption and improve scalability.</span></span>

<span data-ttu-id="1ee41-122">[セット ベースからレコード単位への操作の変換](xpp-data-perf.md) トピックでは、レコード セット ベースのステートメントおよびメソッドをより効率的に使用するための情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="1ee41-122">The [Conversion of operations from set-based to record-by-record](xpp-data-perf.md) topic provides information about how you can use the record set–based statements and methods more efficiently.</span></span>

<span data-ttu-id="1ee41-123">[SysDa クラス](../sysda.md)を使用してデータを取得および変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="1ee41-123">You can also use the [SysDa classes](../sysda.md) to retrieve and modify data.</span></span> <span data-ttu-id="1ee41-124">拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。</span><span class="sxs-lookup"><span data-stu-id="1ee41-124">The extensible SysDa API provides almost all the data access possibilities that are available in X++.</span></span>
