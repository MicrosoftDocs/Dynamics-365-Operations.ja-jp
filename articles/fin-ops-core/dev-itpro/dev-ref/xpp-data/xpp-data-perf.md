---
title: セット ベースからレコード単位への操作の変換
description: このトピックでは、X++ 言語での SQL 操作を高速化する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150273
ms.assetid: 999a5ecf-559b-4d66-8b05-9a8e477e0518
ms.search.region: Global
ms.author: robinr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 6740f235f087a88a0379b2c92745f5d396a7a55f
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505946"
---
# <a name="conversion-of-operations-from-set-based-to-record-by-record"></a><span data-ttu-id="bfe96-103">セット ベースからレコード単位への操作の変換</span><span class="sxs-lookup"><span data-stu-id="bfe96-103">Conversion of operations from set-based to record-by-record</span></span>

<span data-ttu-id="bfe96-104">次のステートメントおよびメソッドを使用して、アプリケーションとデータベース間の通信を減らすことにより、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="bfe96-104">You can use the following statements and methods to improve performance by reducing communication between the application and the database:</span></span>

- [<span data-ttu-id="bfe96-105">delete_from</span><span class="sxs-lookup"><span data-stu-id="bfe96-105">delete_from</span></span>](xpp-delete.md#delete-from-statement)
- [<span data-ttu-id="bfe96-106">update_recordset</span><span class="sxs-lookup"><span data-stu-id="bfe96-106">update_recordset</span></span>](xpp-update.md#update-recordset-statement)
- [<span data-ttu-id="bfe96-107">insert_recordset</span><span class="sxs-lookup"><span data-stu-id="bfe96-107">insert_recordset</span></span>](xpp-insert.md#insert-recordset-statement)
- [<span data-ttu-id="bfe96-108">RecordSortedList.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="bfe96-108">RecordSortedList.insertDatabase</span></span>](../system-classes/recordsortedlist-class.md#method-insertdatabase)
- [<span data-ttu-id="bfe96-109">RecordInsertList.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="bfe96-109">RecordInsertList.insertDatabase</span></span>](../system-classes/recordinsertlist-class.md#method-insertdatabase)

<span data-ttu-id="bfe96-110">これらのレコード セット ベースの操作をより低速のレコードごとの操作に変換できる状況があります。</span><span class="sxs-lookup"><span data-stu-id="bfe96-110">There are situations where these record set–based operations can be converted to slower record-by-record operations.</span></span> <span data-ttu-id="bfe96-111">次のテーブルは、これらの状況を識別します。</span><span class="sxs-lookup"><span data-stu-id="bfe96-111">The following table identifies these situations.</span></span>

|    | <span data-ttu-id="bfe96-112">delete\_from</span><span class="sxs-lookup"><span data-stu-id="bfe96-112">delete\_from</span></span> | <span data-ttu-id="bfe96-113">update\_recordset</span><span class="sxs-lookup"><span data-stu-id="bfe96-113">update\_recordset</span></span> | <span data-ttu-id="bfe96-114">insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="bfe96-114">insert\_recordset</span></span> | <span data-ttu-id="bfe96-115">RecordSortedList</span><span class="sxs-lookup"><span data-stu-id="bfe96-115">RecordSortedList</span></span><br><span data-ttu-id="bfe96-116">RecordInsertList</span><span class="sxs-lookup"><span data-stu-id="bfe96-116">RecordInsertList</span></span> | <span data-ttu-id="bfe96-117">上書きに使用</span><span class="sxs-lookup"><span data-stu-id="bfe96-117">Used to override</span></span> |
|----|--------------|-------------------|-------------------|--------------------------------------|------------------|
<span data-ttu-id="bfe96-118">非 SQL テーブル</span><span class="sxs-lookup"><span data-stu-id="bfe96-118">Non-SQL tables</span></span> | <span data-ttu-id="bfe96-119">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-119">Yes</span></span> | <span data-ttu-id="bfe96-120">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-120">Yes</span></span> | <span data-ttu-id="bfe96-121">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-121">Yes</span></span> | <span data-ttu-id="bfe96-122">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-122">Yes</span></span> | <span data-ttu-id="bfe96-123">該当なし</span><span class="sxs-lookup"><span data-stu-id="bfe96-123">Not applicable</span></span>
<span data-ttu-id="bfe96-124">アクションの削除</span><span class="sxs-lookup"><span data-stu-id="bfe96-124">Delete actions</span></span> | <span data-ttu-id="bfe96-125">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-125">Yes</span></span> | <span data-ttu-id="bfe96-126">無</span><span class="sxs-lookup"><span data-stu-id="bfe96-126">No</span></span> | <span data-ttu-id="bfe96-127">無</span><span class="sxs-lookup"><span data-stu-id="bfe96-127">No</span></span> | <span data-ttu-id="bfe96-128">無</span><span class="sxs-lookup"><span data-stu-id="bfe96-128">No</span></span> | <span data-ttu-id="bfe96-129">**skipDeleteActions**</span><span class="sxs-lookup"><span data-stu-id="bfe96-129">**skipDeleteActions**</span></span>
<span data-ttu-id="bfe96-130">データベース ログの有効化</span><span class="sxs-lookup"><span data-stu-id="bfe96-130">The database log is enabled</span></span> | <span data-ttu-id="bfe96-131">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-131">Yes</span></span> | <span data-ttu-id="bfe96-132">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-132">Yes</span></span> | <span data-ttu-id="bfe96-133">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-133">Yes</span></span> | <span data-ttu-id="bfe96-134">無</span><span class="sxs-lookup"><span data-stu-id="bfe96-134">No</span></span> | <span data-ttu-id="bfe96-135">**skipDatabaseLog**</span><span class="sxs-lookup"><span data-stu-id="bfe96-135">**skipDatabaseLog**</span></span>
<span data-ttu-id="bfe96-136">オーバーライドされたメソッド</span><span class="sxs-lookup"><span data-stu-id="bfe96-136">Overridden method</span></span> | <span data-ttu-id="bfe96-137">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-137">Yes</span></span> | <span data-ttu-id="bfe96-138">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-138">Yes</span></span> | <span data-ttu-id="bfe96-139">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-139">Yes</span></span> | <span data-ttu-id="bfe96-140">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-140">Yes</span></span> | <span data-ttu-id="bfe96-141">**skipDataMethods**</span><span class="sxs-lookup"><span data-stu-id="bfe96-141">**skipDataMethods**</span></span>
<span data-ttu-id="bfe96-142">テーブルに警告が設定されている</span><span class="sxs-lookup"><span data-stu-id="bfe96-142">Alerts are set up for the table</span></span> | <span data-ttu-id="bfe96-143">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-143">Yes</span></span> | <span data-ttu-id="bfe96-144">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-144">Yes</span></span> | <span data-ttu-id="bfe96-145">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-145">Yes</span></span> | <span data-ttu-id="bfe96-146">無</span><span class="sxs-lookup"><span data-stu-id="bfe96-146">No</span></span> | <span data-ttu-id="bfe96-147">**skipEvents**</span><span class="sxs-lookup"><span data-stu-id="bfe96-147">**skipEvents**</span></span>
<span data-ttu-id="bfe96-148">テーブルの **ValidTimeStateFieldType** プロパティが、なしに等しくない</span><span class="sxs-lookup"><span data-stu-id="bfe96-148">The **ValidTimeStateFieldType** property on a table isn't equal to None</span></span> | <span data-ttu-id="bfe96-149">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-149">Yes</span></span> | <span data-ttu-id="bfe96-150">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-150">Yes</span></span> | <span data-ttu-id="bfe96-151">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-151">Yes</span></span> | <span data-ttu-id="bfe96-152">有</span><span class="sxs-lookup"><span data-stu-id="bfe96-152">Yes</span></span> | <span data-ttu-id="bfe96-153">該当なし</span><span class="sxs-lookup"><span data-stu-id="bfe96-153">Not applicable</span></span>

<span data-ttu-id="bfe96-154">**上書きに使用**列で表示される設定を使用して、パフォーマンスに悪影響を与える 1 つまたは複数の要因を明示的にスキップまたは無視します。</span><span class="sxs-lookup"><span data-stu-id="bfe96-154">You can use the settings that are shown in the **Used to override** column to explicitly skip or ignore one or more factors that adversely affect performance.</span></span> <span data-ttu-id="bfe96-155">何らかの理由で前述の SQL 操作のいずれかがレコードごとの操作にダウングレードされた場合、すべての**スキップ\*** 設定も無視されます。</span><span class="sxs-lookup"><span data-stu-id="bfe96-155">If for some reason, one of the previously mentioned SQL operations is downgraded to a record-by-record operation, all the **skip\*** settings are also ignored.</span></span> <span data-ttu-id="bfe96-156">たとえば、次のコードでは、コンテナーまたはメモ フィールドが myTable で定義されている場合はこの方法をスキップする必要があると明確に示されていても、myTable テーブルで**挿入**メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="bfe96-156">For example, in the following code, the **insert** method on the myTable table is run, even though it's explicitly stated that this method should be skipped if a container or memo field is defined for myTable.</span></span>

```xpp
public void tutorialRecordInsertList()
{
    MyTable myTable;
    RecordInsertList insertList = new RecordInsertList(
        myTable.TableId,
        True);
    int i;
    for ( i = 1; i <=  100; i++ )
    {
        myTable.value = i;
        insertList.add(myTable);
    }
    insertList.insertDatabase();
}
```
