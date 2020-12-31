---
title: データの更新
description: このトピックでは、X++ 言語での update および doUpdate メソッドについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 81db9b1e2092493ccf1d97fc443936bb4d54d41b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408733"
---
# <a name="update-data"></a><span data-ttu-id="2f682-103">データの更新</span><span class="sxs-lookup"><span data-stu-id="2f682-103">Update data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f682-104">データベースに格納されているテーブルの 1 つまたは複数の行を更新するため、SQL ステートメントを対話的またはソース コード内で使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f682-104">You can use SQL statements, either interactively or in source code, to update one or more rows in a table that is stored in the database.</span></span>

+ <span data-ttu-id="2f682-105">**[update メソッド](#update-method)** – バッファーの内容で現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="2f682-105">**[update method](#update-method)** – Update the current record with the contents of the buffer.</span></span> <span data-ttu-id="2f682-106">また、適切なシステム フィールドも更新します。</span><span class="sxs-lookup"><span data-stu-id="2f682-106">Also update the appropriate system fields.</span></span>
+ <span data-ttu-id="2f682-107">**[doUpdate メソッド](#do-update-method)** – 一度に 1 行を更新します。</span><span class="sxs-lookup"><span data-stu-id="2f682-107">**[doUpdate method](#do-update-method)** – Update one row at a time.</span></span>
+ <span data-ttu-id="2f682-108">**[update\_recordset ステートメント](#update-recordset-statement)** – 複数のレコードを 1 回のデータベース トリップで更新します。</span><span class="sxs-lookup"><span data-stu-id="2f682-108">**[update\_recordset statement](#update-recordset-statement)** – Update multiple records in one database trip.</span></span> <span data-ttu-id="2f682-109">**update\_recordset** ステートメントを使用することにより、アプリケーションとデータベース間の通信が減少します。</span><span class="sxs-lookup"><span data-stu-id="2f682-109">By using the **update\_recordset** statement, you reduce communication between the application and the database.</span></span> <span data-ttu-id="2f682-110">したがって、パフォーマンスの向上に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f682-110">Therefore, you help increase performance.</span></span> <span data-ttu-id="2f682-111">場合によっては、レコードのセットに基づく操作をレコードごとの操作に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="2f682-111">In some situations, record set–based operations can fall back to record-by-record operations.</span></span> <span data-ttu-id="2f682-112">詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f682-112">For more information, see [Conversion of operations from set-based to record-by-record](xpp-data-perf.md).</span></span>

## <a name="update-method"></a><a id="update-method"></a><span data-ttu-id="2f682-113">update メソッド</span><span class="sxs-lookup"><span data-stu-id="2f682-113">update method</span></span>

<span data-ttu-id="2f682-114">**update** メソッドは、バッファーの内容で現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="2f682-114">The **update** method updates the current record with the contents of the buffer.</span></span> <span data-ttu-id="2f682-115">また、適切なシステム フィールドも更新されます。</span><span class="sxs-lookup"><span data-stu-id="2f682-115">It also updates the appropriate system fields.</span></span> <span data-ttu-id="2f682-116">オプションの **where** 句は、テーブルの各行を処理するときに **update** メソッドでテストされる条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f682-116">The optional **where** clause specifies a condition that the **update** method tests as it processes each row of the table.</span></span> <span data-ttu-id="2f682-117">その条件に対する **true** をテストする行のみ新しい値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="2f682-117">Only those rows that test **true** against the condition are updated with the new values.</span></span>

<span data-ttu-id="2f682-118">次の例では、更新する CustTable テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f682-118">The following example selects the CustTable table for update.</span></span> <span data-ttu-id="2f682-119">**AccountNum** フィールドの値が **4000** に等しいレコードのみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="2f682-119">Only records where the value of the **AccountNum** field equals **4000** are updated.</span></span> <span data-ttu-id="2f682-120">**next** への呼び出しはなく、この例では **select while** ステートメントを使用していないため、1 つのレコードのみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="2f682-120">Because there is no call to **next**, and this example doesn't use a **select while** statement, only one record is updated.</span></span> <span data-ttu-id="2f682-121">**CreditMax** フィールドの値が **5000** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="2f682-121">The value of the **CreditMax** field is changed to **5000**.</span></span>

```xpp
CustTable custTable;
ttsBegin;
    select forUpdate custTable
        where custTable.AccountNum == '4000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

## <a name="doupdate-method"></a><a id="do-update-method"></a><span data-ttu-id="2f682-122">doUpdate メソッド</span><span class="sxs-lookup"><span data-stu-id="2f682-122">doUpdate method</span></span>

<span data-ttu-id="2f682-123">**update** メソッドの動作をオーバーライドするには、**doUpdate** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2f682-123">To override the behavior of the **update** method, use the **doUpdate** method.</span></span> <span data-ttu-id="2f682-124">**doUpdate** メソッドは、バッファーの内容で現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="2f682-124">The **doUpdate** method updates the current record with the contents of the buffer.</span></span> <span data-ttu-id="2f682-125">また、適切なシステム フィールドも更新されます。</span><span class="sxs-lookup"><span data-stu-id="2f682-125">It also updates the appropriate system fields.</span></span> <span data-ttu-id="2f682-126">テーブルでの **更新** メソッドをバイパスする必要があるときは、**doUpdate** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f682-126">You should use the **doUpdate** method when the **update** method on the table must be bypassed.</span></span> <span data-ttu-id="2f682-127">**doUpdate** テーブル メソッドの構文は、**void doUpdate()** です。</span><span class="sxs-lookup"><span data-stu-id="2f682-127">The syntax for a **doUpdate** table method is **void doUpdate()**.</span></span>

> [!WARNING]
> <span data-ttu-id="2f682-128">**doUpdate** の呼び出しは、データベース イベント ハンドラー (たとえば **onUpdating** および **onUpdated**)、コマンド チェーン **onUpdate()**、および **update()** の呼び出し自体を含むすべてのロジックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="2f682-128">A call to **doUpdate** skips all logic, including database event handlers (for example **onUpdating** and **onUpdated**), chain-of-command **onUpdate()**, and the **update()** call itself.</span></span> <span data-ttu-id="2f682-129">一般に、**doUpdate** を使用することは不適切なプラクティスと見なされており、使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="2f682-129">It's generally considered bad practice to use **doUpdate**, and we don't recommend that you use it.</span></span>

```xpp
CustTable custTable;
ttsBegin;
select forUpdate custTable
    where custTable.CreditMax == 3000;
if (custTable)
{
    custTable.CreditMax += 1000;
    custTable.doUpdate();
}
ttsCommit;
```

## <a name="update_recordset-statement"></a><a id="update-recordset-statement"></a><span data-ttu-id="2f682-130">update\_recordset ステートメント</span><span class="sxs-lookup"><span data-stu-id="2f682-130">update\_recordset statement</span></span>

<span data-ttu-id="2f682-131">**update\_recordset** 演算子は、サーバーへの 1 回のアクセスで複数のレコードを更新するレコード セット ベースの演算子です。</span><span class="sxs-lookup"><span data-stu-id="2f682-131">The **update\_recordset** operator is a record set–based operator that updates multiple records in one trip to the server.</span></span> <span data-ttu-id="2f682-132">したがって、Microsoft SQL Server の機能は、一部のタスクのパフォーマンスを向上させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f682-132">Therefore, the power of Microsoft SQL Server can help improve the performance of some tasks.</span></span> <span data-ttu-id="2f682-133">**update\_recordset** ステートメントは X++ の **delete\_from** と SQL の **update set** に似ています。</span><span class="sxs-lookup"><span data-stu-id="2f682-133">The **update\_recordset** statement resembles **delete\_from** in X++ and **update set** in SQL.</span></span> <span data-ttu-id="2f682-134">フェッチ、変更、および更新によって各レコードを個別に取得することはありません。</span><span class="sxs-lookup"><span data-stu-id="2f682-134">It doesn't retrieve each record separately by fetching, changing, and updating.</span></span> <span data-ttu-id="2f682-135">代わりに、データベース サーバー側の SQL スタイル レコード セットで機能します。</span><span class="sxs-lookup"><span data-stu-id="2f682-135">Instead, it works on an SQL-style record set on the database server side.</span></span> <span data-ttu-id="2f682-136">**更新** メソッドがオーバーライドされた場合、実装は、一度に 1 つのレコードが更新される古典的なループ構造に戻されます。</span><span class="sxs-lookup"><span data-stu-id="2f682-136">If the **update** method is overridden, the implementation falls back to a classic looping construction, where one record at a time is updated.</span></span> <span data-ttu-id="2f682-137">(この動作は、削除対象の **削除の\_対象** の動作に似ています。) したがって、構築は、一時テーブルとテーブル全体 - キャッシュされたテーブルで、ループ構造を使用して動作します。</span><span class="sxs-lookup"><span data-stu-id="2f682-137">(This behavior resembles the behavior of **delete\_from** for deletions.) Therefore, the construction works on temporary tables and whole table–cached tables by using the looping construction.</span></span>

<span data-ttu-id="2f682-138">次の例では、CustTable テーブルを更新し、**CreditMax** の値が **0** (ゼロ) よりも大きいレコードに対して **CreditMax** 列の値を **1000** 増分します。</span><span class="sxs-lookup"><span data-stu-id="2f682-138">The following example updates the CustTable table and increments the value in the **CreditMax** column by **1000** for records where the **CreditMax** value is more than **0** (zero).</span></span>

```xpp
CustTable custTable;
ttsBegin;
update_recordset custTable
    setting CreditMax = custTable.CreditMax + 1000
    where custTable.CreditMax > 0;
ttsCommit;
```

<span data-ttu-id="2f682-139">次の例では、複数の列を更新します。</span><span class="sxs-lookup"><span data-stu-id="2f682-139">The following example updates multiple columns.</span></span>

```xpp
CustTable custTable;
ttsBegin;
update_recordset custTable
    setting
        CreditMax = custTable.CreditMax + 1000,
        AccountStatement = CustAccountStatement::Always
    where custTable.CreditMax > 0;
ttsCommit;
```

<span data-ttu-id="2f682-140">次の例は、**update\_recordset** ステートメントが複数のテーブルの結合をサポートしていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="2f682-140">The following example shows that the **update\_recordset** statement supports joins of several tables.</span></span> <span data-ttu-id="2f682-141">結合されたテーブルのデータを使用して、更新中のテーブル内のフィールドに値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2f682-141">Data from the joined tables can be used to assign values to fields in the table that is being updated.</span></span>

```xpp
TableEmployee tabEmpl;
TableDepartment tabDept;
TableProject tabProj;
update_recordset tabEmpl
    setting
        currentStatusDescription = tabDept.DeptName + ", " + tabProj .ProjName
join tabDept
    where tabDept.DeptId == tabEmpl.DeptId
join tabProj
    where tabProj.ProjId == tabEmpl .ProjId;
```
