---
title: セット ベースからレコード単位への操作の変換
description: このトピックでは、X++ 言語での SQL 操作を高速化する方法について説明します。
author: RobinARH
ms.date: 06/16/2020
ms.topic: article
audience: Developer
ms.reviewer: robinr
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: b4526466c6580f2d240fe584ded323d385768e4c
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923247"
---
# <a name="conversion-of-operations-from-set-based-to-record-by-record"></a><span data-ttu-id="6018d-103">セットベースからレコード単位への操作の変換</span><span class="sxs-lookup"><span data-stu-id="6018d-103">Conversion of operations from set-based to record-by-record</span></span>

<span data-ttu-id="6018d-104">次のステートメントとメソッドを使用して、アプリケーションとデータベース間の通信を減らすことにより、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="6018d-104">You can use the following statements and methods to help improve performance by reducing communication between the application and the database:</span></span>

- [<span data-ttu-id="6018d-105">delete_from</span><span class="sxs-lookup"><span data-stu-id="6018d-105">delete_from</span></span>](xpp-delete.md#delete-from-statement)
- [<span data-ttu-id="6018d-106">update_recordset</span><span class="sxs-lookup"><span data-stu-id="6018d-106">update_recordset</span></span>](xpp-update.md#update-recordset-statement)
- [<span data-ttu-id="6018d-107">insert_recordset</span><span class="sxs-lookup"><span data-stu-id="6018d-107">insert_recordset</span></span>](xpp-insert.md#insert-recordset-statement)
- [<span data-ttu-id="6018d-108">RecordSortedList.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="6018d-108">RecordSortedList.insertDatabase</span></span>](/dotnet/api/dynamics.ax.application#method-insertdatabase)
- [<span data-ttu-id="6018d-109">RecordInsertList.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="6018d-109">RecordInsertList.insertDatabase</span></span>](/dotnet/api/dynamics.ax.application#method-insertdatabase)

<span data-ttu-id="6018d-110">状況によっては、これらのレコード セット ベースの操作をより低速のレコードごとの操作に変換できます。</span><span class="sxs-lookup"><span data-stu-id="6018d-110">In some situations, these record set–based operations can be converted to slower record-by-record operations.</span></span> <span data-ttu-id="6018d-111">次のテーブルは、これらの状況を識別します。</span><span class="sxs-lookup"><span data-stu-id="6018d-111">The following table identifies these situations.</span></span>

| <span data-ttu-id="6018d-112">状況</span><span class="sxs-lookup"><span data-stu-id="6018d-112">Situation</span></span> | <span data-ttu-id="6018d-113">delete\_from</span><span class="sxs-lookup"><span data-stu-id="6018d-113">delete\_from</span></span> | <span data-ttu-id="6018d-114">update\_recordset</span><span class="sxs-lookup"><span data-stu-id="6018d-114">update\_recordset</span></span> | <span data-ttu-id="6018d-115">insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="6018d-115">insert\_recordset</span></span> | <span data-ttu-id="6018d-116">RecordSortedList, RecordInsertList</span><span class="sxs-lookup"><span data-stu-id="6018d-116">RecordSortedList, RecordInsertList</span></span> | <span data-ttu-id="6018d-117">上書きに使用</span><span class="sxs-lookup"><span data-stu-id="6018d-117">Used to override</span></span> |
|---|--------------|-------------------|-------------------|--------------------------------------|------------------|
| <span data-ttu-id="6018d-118">非 SQL テーブル</span><span class="sxs-lookup"><span data-stu-id="6018d-118">Non-SQL tables</span></span> | <span data-ttu-id="6018d-119">有</span><span class="sxs-lookup"><span data-stu-id="6018d-119">Yes</span></span> | <span data-ttu-id="6018d-120">有</span><span class="sxs-lookup"><span data-stu-id="6018d-120">Yes</span></span> | <span data-ttu-id="6018d-121">有</span><span class="sxs-lookup"><span data-stu-id="6018d-121">Yes</span></span> | <span data-ttu-id="6018d-122">有</span><span class="sxs-lookup"><span data-stu-id="6018d-122">Yes</span></span> | <span data-ttu-id="6018d-123">該当なし</span><span class="sxs-lookup"><span data-stu-id="6018d-123">Not applicable</span></span> |
| <span data-ttu-id="6018d-124">アクションの削除</span><span class="sxs-lookup"><span data-stu-id="6018d-124">Delete actions</span></span> | <span data-ttu-id="6018d-125">有</span><span class="sxs-lookup"><span data-stu-id="6018d-125">Yes</span></span> | <span data-ttu-id="6018d-126">無</span><span class="sxs-lookup"><span data-stu-id="6018d-126">No</span></span> | <span data-ttu-id="6018d-127">無</span><span class="sxs-lookup"><span data-stu-id="6018d-127">No</span></span> | <span data-ttu-id="6018d-128">無</span><span class="sxs-lookup"><span data-stu-id="6018d-128">No</span></span> | <span data-ttu-id="6018d-129">**skipDeleteActions**</span><span class="sxs-lookup"><span data-stu-id="6018d-129">**skipDeleteActions**</span></span> |
| <span data-ttu-id="6018d-130">データベース ログが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="6018d-130">The database log is enabled.</span></span> | <span data-ttu-id="6018d-131">有</span><span class="sxs-lookup"><span data-stu-id="6018d-131">Yes</span></span> | <span data-ttu-id="6018d-132">有</span><span class="sxs-lookup"><span data-stu-id="6018d-132">Yes</span></span> | <span data-ttu-id="6018d-133">有</span><span class="sxs-lookup"><span data-stu-id="6018d-133">Yes</span></span> | <span data-ttu-id="6018d-134">無</span><span class="sxs-lookup"><span data-stu-id="6018d-134">No</span></span> | <span data-ttu-id="6018d-135">**skipDatabaseLog**</span><span class="sxs-lookup"><span data-stu-id="6018d-135">**skipDatabaseLog**</span></span> |
| <span data-ttu-id="6018d-136">オーバーライドされたメソッド</span><span class="sxs-lookup"><span data-stu-id="6018d-136">Overridden method</span></span> | <span data-ttu-id="6018d-137">有</span><span class="sxs-lookup"><span data-stu-id="6018d-137">Yes</span></span> | <span data-ttu-id="6018d-138">有</span><span class="sxs-lookup"><span data-stu-id="6018d-138">Yes</span></span> | <span data-ttu-id="6018d-139">有</span><span class="sxs-lookup"><span data-stu-id="6018d-139">Yes</span></span> | <span data-ttu-id="6018d-140">有</span><span class="sxs-lookup"><span data-stu-id="6018d-140">Yes</span></span> | <span data-ttu-id="6018d-141">**skipDataMethods**</span><span class="sxs-lookup"><span data-stu-id="6018d-141">**skipDataMethods**</span></span> |
| <span data-ttu-id="6018d-142">警告はテーブルの設定をします。</span><span class="sxs-lookup"><span data-stu-id="6018d-142">Alerts are set up for the table.</span></span> | <span data-ttu-id="6018d-143">有</span><span class="sxs-lookup"><span data-stu-id="6018d-143">Yes</span></span> | <span data-ttu-id="6018d-144">有</span><span class="sxs-lookup"><span data-stu-id="6018d-144">Yes</span></span> | <span data-ttu-id="6018d-145">有</span><span class="sxs-lookup"><span data-stu-id="6018d-145">Yes</span></span> | <span data-ttu-id="6018d-146">無</span><span class="sxs-lookup"><span data-stu-id="6018d-146">No</span></span> | <span data-ttu-id="6018d-147">**skipEvents**</span><span class="sxs-lookup"><span data-stu-id="6018d-147">**skipEvents**</span></span> |
| <span data-ttu-id="6018d-148">テーブルの **ValidTimeStateFieldType** プロパティが **なし** 以外の値に設定されています。</span><span class="sxs-lookup"><span data-stu-id="6018d-148">The **ValidTimeStateFieldType** property on a table is set to a value other than **None**.</span></span> | <span data-ttu-id="6018d-149">あり</span><span class="sxs-lookup"><span data-stu-id="6018d-149">Yes</span></span> | <span data-ttu-id="6018d-150">あり</span><span class="sxs-lookup"><span data-stu-id="6018d-150">Yes</span></span> | <span data-ttu-id="6018d-151">あり</span><span class="sxs-lookup"><span data-stu-id="6018d-151">Yes</span></span> | <span data-ttu-id="6018d-152">あり</span><span class="sxs-lookup"><span data-stu-id="6018d-152">Yes</span></span> | <span data-ttu-id="6018d-153">適用できません</span><span class="sxs-lookup"><span data-stu-id="6018d-153">Not applicable</span></span> |

<span data-ttu-id="6018d-154">「上書きに使用」列で表示される **スキップ\**設定を使用して、パフォーマンスに悪影響を与える 1 つまた複数の要因を明示的にスキップまたは無視できます。何らかの理由で、前述の SQL 操作のいずれかがレコードごとの操作にダウングレードされた場合、すべての\* スキップ\**設定は無視されます。たとえば、次のコードでは、コンテナーまたはメモ フィールドが myTable で定義されている場合はこの方法をスキップする必要があると明確に示されていても、myTable テーブルで\* 挿入\*\* メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="6018d-154">You can use the **skip\**_ settings that are shown in the "Used to override" column to explicitly skip or ignore one or more factors that adversely affect performance. If one of the previously mentioned SQL operations is downgraded to a record-by-record operation, all the _\* skip\**_ settings are ignored. In the following example code, the _\* insert\*\* method on the myTable table is run, even though it's explicitly stated that this method should be skipped if a container or memo field is defined for myTable.</span></span>

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]