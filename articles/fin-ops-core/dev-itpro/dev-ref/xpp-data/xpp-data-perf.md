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
ms.openlocfilehash: a00a419ec942c06d1e9af9a4a67f168a06a020af
ms.sourcegitcommit: 94863c587e8acacc7c2e7811e84de66c312cc017
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/29/2020
ms.locfileid: "3637832"
---
# <a name="conversion-of-operations-from-set-based-to-record-by-record"></a><span data-ttu-id="d5cb5-103">セットベースからレコード単位への操作の変換</span><span class="sxs-lookup"><span data-stu-id="d5cb5-103">Conversion of operations from set-based to record-by-record</span></span>

<span data-ttu-id="d5cb5-104">次のステートメントとメソッドを使用して、アプリケーションとデータベース間の通信を減らすことにより、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-104">You can use the following statements and methods to help improve performance by reducing communication between the application and the database:</span></span>

- [<span data-ttu-id="d5cb5-105">delete_from</span><span class="sxs-lookup"><span data-stu-id="d5cb5-105">delete_from</span></span>](xpp-delete.md#delete-from-statement)
- [<span data-ttu-id="d5cb5-106">update_recordset</span><span class="sxs-lookup"><span data-stu-id="d5cb5-106">update_recordset</span></span>](xpp-update.md#update-recordset-statement)
- [<span data-ttu-id="d5cb5-107">insert_recordset</span><span class="sxs-lookup"><span data-stu-id="d5cb5-107">insert_recordset</span></span>](xpp-insert.md#insert-recordset-statement)
- [<span data-ttu-id="d5cb5-108">RecordSortedList.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="d5cb5-108">RecordSortedList.insertDatabase</span></span>](../system-classes/recordsortedlist-class.md#method-insertdatabase)
- [<span data-ttu-id="d5cb5-109">RecordInsertList.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="d5cb5-109">RecordInsertList.insertDatabase</span></span>](../system-classes/recordinsertlist-class.md#method-insertdatabase)

<span data-ttu-id="d5cb5-110">状況によっては、これらのレコード セット ベースの操作をより低速のレコードごとの操作に変換できます。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-110">In some situations, these record set–based operations can be converted to slower record-by-record operations.</span></span> <span data-ttu-id="d5cb5-111">次のテーブルは、これらの状況を識別します。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-111">The following table identifies these situations.</span></span>

| <span data-ttu-id="d5cb5-112">状況</span><span class="sxs-lookup"><span data-stu-id="d5cb5-112">Situation</span></span> | <span data-ttu-id="d5cb5-113">delete\_from</span><span class="sxs-lookup"><span data-stu-id="d5cb5-113">delete\_from</span></span> | <span data-ttu-id="d5cb5-114">update\_recordset</span><span class="sxs-lookup"><span data-stu-id="d5cb5-114">update\_recordset</span></span> | <span data-ttu-id="d5cb5-115">insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="d5cb5-115">insert\_recordset</span></span> | <span data-ttu-id="d5cb5-116">RecordSortedList, RecordInsertList</span><span class="sxs-lookup"><span data-stu-id="d5cb5-116">RecordSortedList, RecordInsertList</span></span> | <span data-ttu-id="d5cb5-117">上書きに使用</span><span class="sxs-lookup"><span data-stu-id="d5cb5-117">Used to override</span></span> |
|---|--------------|-------------------|-------------------|--------------------------------------|------------------|
| <span data-ttu-id="d5cb5-118">非 SQL テーブル</span><span class="sxs-lookup"><span data-stu-id="d5cb5-118">Non-SQL tables</span></span> | <span data-ttu-id="d5cb5-119">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-119">Yes</span></span> | <span data-ttu-id="d5cb5-120">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-120">Yes</span></span> | <span data-ttu-id="d5cb5-121">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-121">Yes</span></span> | <span data-ttu-id="d5cb5-122">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-122">Yes</span></span> | <span data-ttu-id="d5cb5-123">該当なし</span><span class="sxs-lookup"><span data-stu-id="d5cb5-123">Not applicable</span></span> |
| <span data-ttu-id="d5cb5-124">アクションの削除</span><span class="sxs-lookup"><span data-stu-id="d5cb5-124">Delete actions</span></span> | <span data-ttu-id="d5cb5-125">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-125">Yes</span></span> | <span data-ttu-id="d5cb5-126">無</span><span class="sxs-lookup"><span data-stu-id="d5cb5-126">No</span></span> | <span data-ttu-id="d5cb5-127">無</span><span class="sxs-lookup"><span data-stu-id="d5cb5-127">No</span></span> | <span data-ttu-id="d5cb5-128">無</span><span class="sxs-lookup"><span data-stu-id="d5cb5-128">No</span></span> | <span data-ttu-id="d5cb5-129">**skipDeleteActions**</span><span class="sxs-lookup"><span data-stu-id="d5cb5-129">**skipDeleteActions**</span></span> |
| <span data-ttu-id="d5cb5-130">データベース ログが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-130">The database log is enabled.</span></span> | <span data-ttu-id="d5cb5-131">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-131">Yes</span></span> | <span data-ttu-id="d5cb5-132">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-132">Yes</span></span> | <span data-ttu-id="d5cb5-133">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-133">Yes</span></span> | <span data-ttu-id="d5cb5-134">無</span><span class="sxs-lookup"><span data-stu-id="d5cb5-134">No</span></span> | <span data-ttu-id="d5cb5-135">**skipDatabaseLog**</span><span class="sxs-lookup"><span data-stu-id="d5cb5-135">**skipDatabaseLog**</span></span> |
| <span data-ttu-id="d5cb5-136">オーバーライドされたメソッド</span><span class="sxs-lookup"><span data-stu-id="d5cb5-136">Overridden method</span></span> | <span data-ttu-id="d5cb5-137">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-137">Yes</span></span> | <span data-ttu-id="d5cb5-138">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-138">Yes</span></span> | <span data-ttu-id="d5cb5-139">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-139">Yes</span></span> | <span data-ttu-id="d5cb5-140">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-140">Yes</span></span> | <span data-ttu-id="d5cb5-141">**skipDataMethods**</span><span class="sxs-lookup"><span data-stu-id="d5cb5-141">**skipDataMethods**</span></span> |
| <span data-ttu-id="d5cb5-142">警告はテーブルの設定をします。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-142">Alerts are set up for the table.</span></span> | <span data-ttu-id="d5cb5-143">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-143">Yes</span></span> | <span data-ttu-id="d5cb5-144">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-144">Yes</span></span> | <span data-ttu-id="d5cb5-145">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-145">Yes</span></span> | <span data-ttu-id="d5cb5-146">無</span><span class="sxs-lookup"><span data-stu-id="d5cb5-146">No</span></span> | <span data-ttu-id="d5cb5-147">**skipEvents**</span><span class="sxs-lookup"><span data-stu-id="d5cb5-147">**skipEvents**</span></span> |
| <span data-ttu-id="d5cb5-148">テーブルの **ValidTimeStateFieldType** プロパティが**なし**以外の値に設定されています。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-148">The **ValidTimeStateFieldType** property on a table is set to a value other than **None**.</span></span> | <span data-ttu-id="d5cb5-149">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-149">Yes</span></span> | <span data-ttu-id="d5cb5-150">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-150">Yes</span></span> | <span data-ttu-id="d5cb5-151">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-151">Yes</span></span> | <span data-ttu-id="d5cb5-152">有</span><span class="sxs-lookup"><span data-stu-id="d5cb5-152">Yes</span></span> | <span data-ttu-id="d5cb5-153">該当なし</span><span class="sxs-lookup"><span data-stu-id="d5cb5-153">Not applicable</span></span> |

<span data-ttu-id="d5cb5-154">「上書きに使用」列で表示される**スキップ\*** 設定を使用して、パフォーマンスに悪影響を与える 1 つまたは複数の要因を明示的にスキップまたは無視できます。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-154">You can use the **skip\*** settings that are shown in the "Used to override" column to explicitly skip or ignore one or more factors that adversely affect performance.</span></span> <span data-ttu-id="d5cb5-155">何らかの理由で、前述の SQL 操作のいずれかがレコードごとの操作にダウングレードされた場合、すべての**スキップ\*** 設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-155">If, for some reason, one of the previously mentioned SQL operations is downgraded to a record-by-record operation, all the **skip\*** settings are ignored.</span></span> <span data-ttu-id="d5cb5-156">たとえば、次のコードでは、コンテナーまたはメモ フィールドが myTable で定義されている場合はこの方法をスキップする必要があると明確に示されていても、myTable テーブルで**挿入**メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5cb5-156">For example, in the following code, the **insert** method on the myTable table is run, even though it's explicitly stated that this method should be skipped if a container or memo field is defined for myTable.</span></span>

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
