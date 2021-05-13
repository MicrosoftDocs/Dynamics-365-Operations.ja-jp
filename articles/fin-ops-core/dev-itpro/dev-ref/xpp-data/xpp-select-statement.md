---
title: 明細書を選択
description: このトピックでは、X++ 言語での select ステートメントについて説明します。
author: robinarh
ms.date: 06/16/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ec8eba1b738f30a171eb27ec967c41deae4127db
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865882"
---
# <a name="select-statement"></a><span data-ttu-id="58ae5-103">明細書を選択</span><span class="sxs-lookup"><span data-stu-id="58ae5-103">Select statement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58ae5-104">**select** ステートメントは、データベースからデータをフェッチまたは操作します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-104">The **select** statement fetches or manipulates data from the database.</span></span>

+ <span data-ttu-id="58ae5-105">すべての **選択** ステートメントではレコードをフェッチするためテーブル変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-105">All **select** statements use a table variable to fetch records.</span></span> <span data-ttu-id="58ae5-106">この変数は、**select** 文を実行する前に宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-106">This variable must be declared before a **select** statement can be run.</span></span>
+ <span data-ttu-id="58ae5-107">**select** ステートメントは、レコードを 1 つだけ、またはフィールドをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="58ae5-107">The **select** statement fetches only one record, or field.</span></span> <span data-ttu-id="58ae5-108">複数のレコードをフェッチまたは移動したりするには、**next** ステートメントまたは **[while select](xpp-while-select.md)** ステートメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-108">To fetch or traverse multiple records, you can use the **next** statement or the **[while select](xpp-while-select.md)** statement.</span></span>

    + <span data-ttu-id="58ae5-109">**next** ステートメントは、テーブルの次のレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="58ae5-109">The **next** statement fetches the next record in the table.</span></span> <span data-ttu-id="58ae5-110">**選択** ステートメントの前に、**次** ステートメントがある場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-110">If no **select** statement precedes the **next** statement, an error occurs.</span></span> <span data-ttu-id="58ae5-111">**次** ステートメントを使用する場合、**firstOnly** 検索オプションを使用しません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-111">If you use a **next** statement, don't use the **firstOnly** find option.</span></span>
    + <span data-ttu-id="58ae5-112">**while select** ステートメントを使用して複数のレコードを移動する方がより適切です。</span><span class="sxs-lookup"><span data-stu-id="58ae5-112">It's more appropriate to use a **while select** statement to traverse multiple records.</span></span>

+ <span data-ttu-id="58ae5-113">**select** ステートメントの結果はテーブル バッファ変数に返されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-113">The results of a **select** statement are returned in a table buffer variable.</span></span>
+ <span data-ttu-id="58ae5-114">**選択** ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-114">If you use a field list in the **select** statement, only those fields are available in the table variable.</span></span>

## <a name="select-example"></a><span data-ttu-id="58ae5-115">例の選択</span><span class="sxs-lookup"><span data-stu-id="58ae5-115">Select example</span></span>

<span data-ttu-id="58ae5-116">次の例では、CustTable テーブルの最初の行のすべての列をフェッチし、その行の **AccountNum** 列に値を出力します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-116">The following example fetches all the columns in the first row of the CustTable table and prints the value in the **AccountNum** column of that row.</span></span>

```xpp
CustTable custTable;
select * from custTable;
info("AccountNum: " + custTable.AccountNum);
```

<span data-ttu-id="58ae5-117">データ選択のその他の例については、[データの選択](xpp-select.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-117">For more examples of data selection, see [Select data](xpp-select.md).</span></span>

## <a name="insert-example"></a><span data-ttu-id="58ae5-118">例の挿入</span><span class="sxs-lookup"><span data-stu-id="58ae5-118">Insert example</span></span>

<span data-ttu-id="58ae5-119">次の例では、新しいレコードを CustTable テーブルに挿入します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-119">The following example inserts a new record into the CustTable table.</span></span> <span data-ttu-id="58ae5-120">新しいレコードの **AccountNum** 列は **2000** に設定され、**CustGroup** 列は **1** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-120">The **AccountNum** column of the new record is set to **2000**, and the **CustGroup** column is set to **1**.</span></span> <span data-ttu-id="58ae5-121">レコードの他のフィールドは空白になります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-121">Other fields in the record will be blank.</span></span>

```xpp
ttsBegin;
    CustTable custTable;
    select forUpdate custTable;
    custTable.AccountNum = '2000';
    custTable.CustGroup = '1';
    custTable.insert();
ttsCommit;
```

<span data-ttu-id="58ae5-122">データの挿入に関するその他の例については、[データの挿入](xpp-insert.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-122">For more examples of data insertion, see [Insert data](xpp-insert.md).</span></span>

## <a name="update-example"></a><span data-ttu-id="58ae5-123">例の更新</span><span class="sxs-lookup"><span data-stu-id="58ae5-123">Update example</span></span>

<span data-ttu-id="58ae5-124">次の例では、更新する CustTable テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-124">The following example selects the CustTable table for update.</span></span> <span data-ttu-id="58ae5-125">**AccountNum** フィールドの値が **2000** に等しいレコードのみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-125">Only records where the value of the **AccountNum** field equals **2000** are updated.</span></span> <span data-ttu-id="58ae5-126">**next** への呼び出しはなく、この例では **select while** ステートメントを使用していないため、1 つのレコードのみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-126">Because there is no call to **next**, and this example doesn't use a **select while** statement, only one record is updated.</span></span> <span data-ttu-id="58ae5-127">**CreditMax** フィールドの値が **5000** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-127">The value of the **CreditMax** field is changed to **5000**.</span></span>

```xpp
ttsBegin;
    CustTable custTable;
    select forUpdate custTable
        where custTable.AccountNum == '2000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

<span data-ttu-id="58ae5-128">データの更新に関するその他の例については、[データの更新](xpp-update.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-128">For more examples of data updates, see [Update data](xpp-update.md).</span></span>

## <a name="delete-example"></a><span data-ttu-id="58ae5-129">例の削除</span><span class="sxs-lookup"><span data-stu-id="58ae5-129">Delete example</span></span>

<span data-ttu-id="58ae5-130">次の例では、**AccountNum** フィールドが **2000** である CustTable テーブルのすべてのレコードがデータベースから削除されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-130">In the following example, all records in the CustTable table where the **AccountNum** field equals **2000** are deleted from the database.</span></span> <span data-ttu-id="58ae5-131">一度に 1 つのレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-131">One record is deleted at a time.</span></span>

```xpp
ttsBegin;
    CustTable custTable;
    while select forUpdate CustTable
        where custTable.AccountNum == '2000'
    {
        custTable.delete();
    }
ttsCommit;
```

<span data-ttu-id="58ae5-132">データの削除に関するその他の例については、[データの削除](xpp-select.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-132">For more examples of data deletion, see [Delete data](xpp-select.md).</span></span>

## <a name="syntax-of-the-select-statement"></a><span data-ttu-id="58ae5-133">Select ステートメントの構文</span><span class="sxs-lookup"><span data-stu-id="58ae5-133">Syntax of the select statement</span></span>

<span data-ttu-id="58ae5-134">構文では次の記号が使用されています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-134">The following symbols are used in the syntax:</span></span>

+ <span data-ttu-id="58ae5-135">**\[\]** – かっこはオプションの要素を囲みます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-135">**\[\]** – Brackets enclose an optional element.</span></span>
+ <span data-ttu-id="58ae5-136">**{}** – 中かっこは、0 回以上含めることができる要素を囲みます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-136">**{}** – Braces enclose an element that can be included zero or more times.</span></span>
+ <span data-ttu-id="58ae5-137">**\+** – プラス記号は、1回以上含めることができる要素を示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-137">**\+** – A plus sign indicates an element that can be included one or more times.</span></span>
+ <span data-ttu-id="58ae5-138">**|** – バーはオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-138">**|** – A bar indicates options.</span></span> 

| <span data-ttu-id="58ae5-139">記号</span><span class="sxs-lookup"><span data-stu-id="58ae5-139">Symbol</span></span>                |   | <span data-ttu-id="58ae5-140">式</span><span class="sxs-lookup"><span data-stu-id="58ae5-140">Expression</span></span> |
|-----------------------|---|------------|
| <span data-ttu-id="58ae5-141">*SelectStatement*</span><span class="sxs-lookup"><span data-stu-id="58ae5-141">*SelectStatement*</span></span>     | = | <span data-ttu-id="58ae5-142">*パラメーター* を **選択する**</span><span class="sxs-lookup"><span data-stu-id="58ae5-142">**select** *Parameters*</span></span> |
| <span data-ttu-id="58ae5-143">*パラメーター*</span><span class="sxs-lookup"><span data-stu-id="58ae5-143">*Parameters*</span></span>          | = | <span data-ttu-id="58ae5-144">{ *FindOption* } \[ *FieldList* **from** \] *TableBufferVariable* \[ *IndexClause* \] \[ *Options* \] \[ *WhereClause* \] \[ *JoinClause* \]</span><span class="sxs-lookup"><span data-stu-id="58ae5-144">{ *FindOption* } \[ *FieldList* **from** \] *TableBufferVariable* \[ *IndexClause* \] \[ *Options* \] \[ *WhereClause* \] \[ *JoinClause* \]</span></span> |
| <span data-ttu-id="58ae5-145">*FindOption*</span><span class="sxs-lookup"><span data-stu-id="58ae5-145">*FindOption*</span></span>          | = | <span data-ttu-id="58ae5-146">**crossCompany** \[**:** *ContainerVariable*\] \| **reverse** \| **firstFast** \| *FirstOption* \| **forUpdate** \| **noFetch** \| *ForceOption* \| **forceSelectOrder** \| **forceNestedLoop** \| *LockOption* \| **repeatableRead** \| **validTimeState**</span><span class="sxs-lookup"><span data-stu-id="58ae5-146">**crossCompany** \[**:** *ContainerVariable*\] \| **reverse** \| **firstFast** \| *FirstOption* \| **forUpdate** \| **noFetch** \| *ForceOption* \| **forceSelectOrder** \| **forceNestedLoop** \| *LockOption* \| **repeatableRead** \| **validTimeState**</span></span> |
| <span data-ttu-id="58ae5-147">*FirstOption*</span><span class="sxs-lookup"><span data-stu-id="58ae5-147">*FirstOption*</span></span>         | = | <span data-ttu-id="58ae5-148">**firstOnly** \| **firstOnly10** \| **firstOnly100** \| **firstOnly1000**</span><span class="sxs-lookup"><span data-stu-id="58ae5-148">**firstOnly** \| **firstOnly10** \| **firstOnly100** \| **firstOnly1000**</span></span> |
| <span data-ttu-id="58ae5-149">*LockOption*</span><span class="sxs-lookup"><span data-stu-id="58ae5-149">*LockOption*</span></span>          | = | <span data-ttu-id="58ae5-150">**optimisticLock** \| **pessimisticLock**</span><span class="sxs-lookup"><span data-stu-id="58ae5-150">**optimisticLock** \| **pessimisticLock**</span></span> |
| <span data-ttu-id="58ae5-151">*ForceOption*</span><span class="sxs-lookup"><span data-stu-id="58ae5-151">*ForceOption*</span></span>         | = | <span data-ttu-id="58ae5-152">**forcePlaceholders** \| **forceLiterals**</span><span class="sxs-lookup"><span data-stu-id="58ae5-152">**forcePlaceholders** \| **forceLiterals**</span></span> |
| <span data-ttu-id="58ae5-153">*FieldList*</span><span class="sxs-lookup"><span data-stu-id="58ae5-153">*FieldList*</span></span>           | = | <span data-ttu-id="58ae5-154">{ *フィールド* } \| **\***</span><span class="sxs-lookup"><span data-stu-id="58ae5-154">{ *Field* } \| **\***</span></span> |
| <span data-ttu-id="58ae5-155">*フィールド*</span><span class="sxs-lookup"><span data-stu-id="58ae5-155">*Field*</span></span>               | = | <span data-ttu-id="58ae5-156">*集計* **(** *FieldIdentifier* **)** \| *FieldIdentifier*</span><span class="sxs-lookup"><span data-stu-id="58ae5-156">*Aggregate* **(** *FieldIdentifier* **)** \| *FieldIdentifier*</span></span> |
| <span data-ttu-id="58ae5-157">*集計*</span><span class="sxs-lookup"><span data-stu-id="58ae5-157">*Aggregate*</span></span>           | = | <span data-ttu-id="58ae5-158">**合計** \| **平均** \| **minof** \| **maxof** \| **集計**</span><span class="sxs-lookup"><span data-stu-id="58ae5-158">**sum** \| **avg** \| **minof** \| **maxof** \| **count**</span></span> |
| <span data-ttu-id="58ae5-159">*オプション*</span><span class="sxs-lookup"><span data-stu-id="58ae5-159">*Options*</span></span>             | = | <span data-ttu-id="58ae5-160">*OrderClause* \| *IndexClause*</span><span class="sxs-lookup"><span data-stu-id="58ae5-160">*OrderClause* \| *IndexClause*</span></span> |
| <span data-ttu-id="58ae5-161">*OrderClause*</span><span class="sxs-lookup"><span data-stu-id="58ae5-161">*OrderClause*</span></span>         | = | <span data-ttu-id="58ae5-162">\[*OrderBy* \[*GroupBy*\]\] \| \[*GroupBy* \[*OrderBy*\]\]</span><span class="sxs-lookup"><span data-stu-id="58ae5-162">\[*OrderBy* \[*GroupBy*\]\] \| \[*GroupBy* \[*OrderBy*\]\]</span></span> |
| <span data-ttu-id="58ae5-163">*OrderBy*</span><span class="sxs-lookup"><span data-stu-id="58ae5-163">*OrderBy*</span></span>             | = | <span data-ttu-id="58ae5-164">**order** \[**by**\] *FieldOrder* {**、** *FieldOrder* }</span><span class="sxs-lookup"><span data-stu-id="58ae5-164">**order** \[**by**\] *FieldOrder* {**,** *FieldOrder* }</span></span> |
| <span data-ttu-id="58ae5-165">*GroupBy*</span><span class="sxs-lookup"><span data-stu-id="58ae5-165">*GroupBy*</span></span>             | = | <span data-ttu-id="58ae5-166">**group** \[**by**\] *FieldOrder* {**、** *FieldOrder* }</span><span class="sxs-lookup"><span data-stu-id="58ae5-166">**group** \[**by**\] *FieldOrder* {**,** *FieldOrder* }</span></span> |
| <span data-ttu-id="58ae5-167">*FieldOrder*</span><span class="sxs-lookup"><span data-stu-id="58ae5-167">*FieldOrder*</span></span>          | = | <span data-ttu-id="58ae5-168">*FieldIdentifier* \[ **asc** \| **desc** \]</span><span class="sxs-lookup"><span data-stu-id="58ae5-168">*FieldIdentifier* \[ **asc** \| **desc** \]</span></span> |
| <span data-ttu-id="58ae5-169">*IndexClause*</span><span class="sxs-lookup"><span data-stu-id="58ae5-169">*IndexClause*</span></span>         | = | <span data-ttu-id="58ae5-170">**インデックス** *IndexName* \| **インデックス ヒント** *IndexName*</span><span class="sxs-lookup"><span data-stu-id="58ae5-170">**index** *IndexName* \| **index hint** *IndexName*</span></span> |
| <span data-ttu-id="58ae5-171">*WhereClause*</span><span class="sxs-lookup"><span data-stu-id="58ae5-171">*WhereClause*</span></span>         | = | <span data-ttu-id="58ae5-172">**where** *式* *InClause*</span><span class="sxs-lookup"><span data-stu-id="58ae5-172">**where** *Expression* *InClause*</span></span> |
| <span data-ttu-id="58ae5-173">*InClause*</span><span class="sxs-lookup"><span data-stu-id="58ae5-173">*InClause*</span></span>            | = | <span data-ttu-id="58ae5-174">**in** *リスト*</span><span class="sxs-lookup"><span data-stu-id="58ae5-174">**in** *List*</span></span> |
| <span data-ttu-id="58ae5-175">*JoinClause*</span><span class="sxs-lookup"><span data-stu-id="58ae5-175">*JoinClause*</span></span>          | = | <span data-ttu-id="58ae5-176">\[**exists** \| **notexists** \| **outer** \] **join** *Parameters*</span><span class="sxs-lookup"><span data-stu-id="58ae5-176">\[**exists** \| **notexists** \| **outer** \] **join** *Parameters*</span></span> |
| <span data-ttu-id="58ae5-177">*ContainerVariable*</span><span class="sxs-lookup"><span data-stu-id="58ae5-177">*ContainerVariable*</span></span>   | = | <span data-ttu-id="58ae5-178">コンテナー。</span><span class="sxs-lookup"><span data-stu-id="58ae5-178">A container.</span></span> |
| <span data-ttu-id="58ae5-179">*式*</span><span class="sxs-lookup"><span data-stu-id="58ae5-179">*Expression*</span></span>          | = | <span data-ttu-id="58ae5-180">式。</span><span class="sxs-lookup"><span data-stu-id="58ae5-180">An expression.</span></span> |
| <span data-ttu-id="58ae5-181">*TableBufferVariable*</span><span class="sxs-lookup"><span data-stu-id="58ae5-181">*TableBufferVariable*</span></span> | = | <span data-ttu-id="58ae5-182">結果の変数名。</span><span class="sxs-lookup"><span data-stu-id="58ae5-182">The variable name for the results.</span></span> |
| <span data-ttu-id="58ae5-183">*FieldIdentifier*</span><span class="sxs-lookup"><span data-stu-id="58ae5-183">*FieldIdentifier*</span></span>     | = | <span data-ttu-id="58ae5-184">テーブルでのフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="58ae5-184">The name of a field in the table.</span></span> |
| <span data-ttu-id="58ae5-185">*IndexName*</span><span class="sxs-lookup"><span data-stu-id="58ae5-185">*IndexName*</span></span>           | = | <span data-ttu-id="58ae5-186">テーブルのインデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="58ae5-186">The name of an index for a table.</span></span> |
| <span data-ttu-id="58ae5-187">*リスト*</span><span class="sxs-lookup"><span data-stu-id="58ae5-187">*List*</span></span>                | = | <span data-ttu-id="58ae5-188">値の配列。</span><span class="sxs-lookup"><span data-stu-id="58ae5-188">An array of values.</span></span> |

## <a name="aggregate-functions"></a><span data-ttu-id="58ae5-189">集計関数</span><span class="sxs-lookup"><span data-stu-id="58ae5-189">Aggregate functions</span></span>

<span data-ttu-id="58ae5-190">集計関数は、レコードのグループに対する単一のフィールドで計算を実行します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-190">The aggregate functions perform calculations on a single field over a group of records.</span></span>

+ <span data-ttu-id="58ae5-191">集計関数を実行したフィールドに結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-191">The result is returned in the field that you perform the aggregate function over.</span></span>
+ <span data-ttu-id="58ae5-192">結果のフィールドは、**group by** 句の集計値とフィールドです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-192">The fields in the results are the aggregate values and the fields in the **group by** clause.</span></span>
+ <span data-ttu-id="58ae5-193">整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-193">You can count, average, or sum only integer and real fields.</span></span>
+ <span data-ttu-id="58ae5-194">**sum** 関数が **null** を返す場合、行は返されません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-194">In cases where the **sum** function will return **null**, no rows are returned.</span></span>

### <a name="differences-between-x-and-sql"></a><span data-ttu-id="58ae5-195">X++ と SQL 間の違い</span><span class="sxs-lookup"><span data-stu-id="58ae5-195">Differences between X++ and SQL</span></span>

<span data-ttu-id="58ae5-196">業界標準の SQL では、データベース クエリに集計関数を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-196">In industry-standard SQL, a database query can contain aggregate functions.</span></span> <span data-ttu-id="58ae5-197">例では、**count(RecID)** および **sum(columnA)** があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-197">Examples include **count(RecID)** and **sum(columnA)**.</span></span> <span data-ttu-id="58ae5-198">集計関数が使用されるが、どの行も **WHERE** 句と一致しないときは、行は、集計の結果を保持するために行を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-198">When an aggregate function is used, but no rows match the **where** clause, a row must be returned to hold the result of the aggregates.</span></span> <span data-ttu-id="58ae5-199">返された行では、**count** 関数には **0** (ゼロ)、**sum** 関数には **null** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-199">The row that is returned shows the value **0** (zero) for the **count** function and **null** for the **sum** function.</span></span> <span data-ttu-id="58ae5-200">X++ はデータベースの **null** 値の概念をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-200">X++ doesn't support the concept of **null** values for the database.</span></span> <span data-ttu-id="58ae5-201">したがって、**sum** 関数が **null** を返す場合、行はユーザーに返されません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-201">Therefore, in cases where the **sum** function will return **null**, no row is returned to the user.</span></span> <span data-ttu-id="58ae5-202">また、すべてのデータ型は、状況によっては **null** 値として処理される特定の値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-202">Additionally, every data type has a specific value that is treated as a **null** value in some circumstances.</span></span>

## <a name="grouping-and-ordering-the-query-results"></a><span data-ttu-id="58ae5-203">クエリ結果のグループ化および順序付け</span><span class="sxs-lookup"><span data-stu-id="58ae5-203">Grouping and ordering the query results</span></span>

<span data-ttu-id="58ae5-204">クエリは複数の **group by** 句を持つことができますが、フィールドは 1 つの **group by** 句のテーブル名で修飾できます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-204">A query can have multiple **group by** clauses, but the fields can be qualified by a table name in only one **group by** clause.</span></span> <span data-ttu-id="58ae5-205">テーブル名の修飾子を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="58ae5-205">We recommend that you use table name qualifiers.</span></span> <span data-ttu-id="58ae5-206">**order by** 句は、**group by** と同じ構文パターンに従います。</span><span class="sxs-lookup"><span data-stu-id="58ae5-206">The **order by** clause follows the same syntax patterns as **group by**.</span></span> <span data-ttu-id="58ae5-207">両方の句が提供されている場合は、**join** (または **from**) 句の後に表示する必要があり、両方とも同じ **join** 句に存在する **where** 句よりも前にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-207">Both clauses, if they are provided, must appear after the **join** (or **from**) clause, and both must appear before any **where** clause that exists on the same **join** clause.</span></span> <span data-ttu-id="58ae5-208">すべての **group by**、**order by**、および **where** の各句を、最後の **join** 句のすぐ後に表示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="58ae5-208">We recommend that all **group by**, **order by**, and **where** clauses appear immediately after the last **join** clause.</span></span> <span data-ttu-id="58ae5-209">次の例は、フィールドがテーブル名で修飾されている **group by** 句を示しています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-209">The following example shows a **group by** clause where a field is qualified by a table name.</span></span>

```xpp
CustTable custTable;
CustGroup custGroup;
struct groupSummary = new struct("int CustomerCount; str CustGroup");

while select count(CreditMax) from custTable
    join custGroup
    order by custGroup.Name
    group by custGroup.CustGroup
    where custTable.CustGroup == custGroup.CustGroup
        && custGroup.Name like "*Days*"
{

    groupSummary.value("CustomerCount", custTable.CreditMax);
    groupSummary.value("CustGroup", custGroup.CustGroup);
    info(groupSummary.toString());
}

// Example output:
// (CustomerCount:1; CustGroup:"1")
// (CustomerCount:3; CustGroup:"2")
```

## <a name="join-tables"></a><span data-ttu-id="58ae5-210">テーブルの結合</span><span class="sxs-lookup"><span data-stu-id="58ae5-210">Join tables</span></span>

<span data-ttu-id="58ae5-211">次の例は、**select** ステートメントの一部として内部結合を実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-211">The following example shows how an inner join can be performed as part of a **select** statement.</span></span> <span data-ttu-id="58ae5-212">この例では、**order by** 句も表示されており、各フィールドはテーブル名で修飾されています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-212">The example also shows an **order by** clause where each field is qualified by a table name.</span></span> <span data-ttu-id="58ae5-213">したがって、1 つの **order by** 句のみを使用して、取得したレコードのソート方法を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-213">Therefore, you can use just one **order by** clause to control how the retrieved records are sorted.</span></span>

```xpp
CustTable custTable;
CustGroup custGroup;
struct output = new struct("int AccountNum; str CustGroup");

while select AccountNum from custTable
    join Name from custGroup
    order by custGroup.Name, custTable.AccountNum
    where custTable.CustGroup == custGroup.CustGroup
{
    info(custGroup.Name + ': ' + custTable.AccountNum);
}

// Example output:
// Days1: 6000
// Days1: 6001
// Days2: 5000
```

## <a name="using-where-order-by-and-index-hint-together-in-a-query"></a><span data-ttu-id="58ae5-214">クエリで where、order by、および index hint を一緒に使用する</span><span class="sxs-lookup"><span data-stu-id="58ae5-214">Using where, order by, and index hint together in a query</span></span>

<span data-ttu-id="58ae5-215">返されるデータを並べ替えるには、**select** ステートメントで **order by** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-215">You use the **order by** keyword in **select** statements to order the data that is returned.</span></span> <span data-ttu-id="58ae5-216">**index hint** キーワードを使用して、クエリで使用するインデックスを指定し、インデックスで定義された方法で選択したレコードを並び替えます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-216">Use the **index hint** keyword to specify the index that should be used in the query, and to sort the selected records in the manner that is defined by the index.</span></span> <span data-ttu-id="58ae5-217">インデックスは、レコードの選択を最適化します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-217">Indexes optimize the selection of records.</span></span> <span data-ttu-id="58ae5-218">特定の順序でレコードを選択するには、**インデックス ヒント** キーワードを **並べ替え** の式と組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-218">To select records in a specific order, combine the **index hint** keyword with an **order by** expression.</span></span> <span data-ttu-id="58ae5-219">出力を逆順に並べ替えるには、**逆** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-219">If you want the output to be sorted in reverse order, use the **reverse** keyword.</span></span> <span data-ttu-id="58ae5-220">テーブルのインデックスが無効になっている場合 (インデックスの **有効** プロパティが **いいえ** に設定されている場合)、索引を参照する **選択** ステートメントは引き続き有効です。</span><span class="sxs-lookup"><span data-stu-id="58ae5-220">If a table index has been disabled (that is, if the index's **Enabled** property is set to **No**), the **select** statement that references the index is still valid.</span></span> <span data-ttu-id="58ae5-221">ただし、インデックスがデータベースに存在しないため、データベースはデータを並べ替えるヒントとしてインデックスを使用できません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-221">However, the database can't use the index as a hint to sort the data, because the index doesn't exist in the database.</span></span> <span data-ttu-id="58ae5-222">次のテーブルは、**select** ステートメントで **index hint** および **order by** キーワードを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-222">The following table shows how to use the **index hint** and **order by** keywords in **select** statements.</span></span>

| <span data-ttu-id="58ae5-223">タスク</span><span class="sxs-lookup"><span data-stu-id="58ae5-223">Task</span></span> | <span data-ttu-id="58ae5-224">明細書を選択</span><span class="sxs-lookup"><span data-stu-id="58ae5-224">select statement</span></span> |
|------|-----|
| <span data-ttu-id="58ae5-225">注文が重要でない場合は、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-225">Select records when the order isn't significant.</span></span> | <span data-ttu-id="58ae5-226">select ..</span><span class="sxs-lookup"><span data-stu-id="58ae5-226">select ..</span></span> <span data-ttu-id="58ae5-227">where ...</span><span class="sxs-lookup"><span data-stu-id="58ae5-227">where ...</span></span> |
| <span data-ttu-id="58ae5-228">注文が重要な場合は、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-228">Select records when the order is significant.</span></span> | <span data-ttu-id="58ae5-229">select ..</span><span class="sxs-lookup"><span data-stu-id="58ae5-229">select ..</span></span> <span data-ttu-id="58ae5-230">order by ... where ...</span><span class="sxs-lookup"><span data-stu-id="58ae5-230">order by ... where ...</span></span> |
| <span data-ttu-id="58ae5-231">レコードを選択し、特定のインデックスを強制的に使用します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-231">Select records, and force a specific index to be used.</span></span> | <span data-ttu-id="58ae5-232">select ..</span><span class="sxs-lookup"><span data-stu-id="58ae5-232">select ..</span></span> <span data-ttu-id="58ae5-233">index hint ... where ...</span><span class="sxs-lookup"><span data-stu-id="58ae5-233">index hint ... where ...</span></span> |
| <span data-ttu-id="58ae5-234">注文が重要な場合は、レコードを選択し、特定のインデックスを強制的に使用します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-234">Select records when the order is significant, and force a specific index to be used.</span></span> | <span data-ttu-id="58ae5-235">select ..</span><span class="sxs-lookup"><span data-stu-id="58ae5-235">select ..</span></span> <span data-ttu-id="58ae5-236">index hint ... order by ... where ...</span><span class="sxs-lookup"><span data-stu-id="58ae5-236">index hint ... order by ... where ...</span></span> |

<span data-ttu-id="58ae5-237">次の例は、顧客の範囲と期日に基づいて、SalesTable テーブルからトランザクションを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-237">The following example shows how to select transactions from the SalesTable table, based on a range of customers and due dates.</span></span>

```xpp
SalesTable salesTable;
select salesTable
    index hint CustIdx
    order by CustAccount
    where
        salesTable.CustAccount >= '3000'
        && salesTable.CustAccount <= '4000'
        && salesTable.FixedDueDate >= 12\12\2004
        && salesTable.FixedDueDate <= 05\05\2009;
```

## <a name="asc-keyword"></a><span data-ttu-id="58ae5-238">asc キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-238">asc keyword</span></span>

<span data-ttu-id="58ae5-239">**asc** キーワードは、**order by** または **group by** 句のオプションです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-239">The **asc** keyword is an option on the **order by** or **group by** clause.</span></span> <span data-ttu-id="58ae5-240">昇順の並べ替え順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-240">It specifies an ascending sort order.</span></span> <span data-ttu-id="58ae5-241">**昇順** または **降順** のどちらも指定されない場合、並べ替えは降順になります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-241">If neither **asc** nor **desc** is specified, the sort is ascending.</span></span>

```xpp
CustTable custTable;
select * from custTable
    order by Value asc;
```

## <a name="avg-keyword"></a><span data-ttu-id="58ae5-242">avg キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-242">avg keyword</span></span>

<span data-ttu-id="58ae5-243">**avg** キーワードはフィールドの平均を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-243">The **avg** keyword returns the average of the fields.</span></span>

```xpp
CustTable custTable;
select avg(Value) from custTable;
info(int642Str(custTable.Value));
```

## <a name="count-keyword"></a><span data-ttu-id="58ae5-244">count キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-244">count keyword</span></span>

<span data-ttu-id="58ae5-245">**count** キーワードは、レコードの数を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-245">The **count** keyword returns the number of records.</span></span>

```xpp
CustTable custTable;
int64 iCountRows;
select count(RecID) from custTable;
iCountRows = custTable.RecID;
info('Rows: ' + int642Str(iCountRows));
```

## <a name="crosscompany-keyword"></a><span data-ttu-id="58ae5-246">crossCompany キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-246">crossCompany keyword</span></span>

<span data-ttu-id="58ae5-247">**crossCompany** キーワードは、ユーザーが読み取りを承認されているすべての会社のデータを返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-247">The **crossCompany** keyword returns data for all companies that the user is authorized to read from.</span></span> <span data-ttu-id="58ae5-248">コンテナを追加して関連する会社の数を削減することができます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-248">You can add a container to reduce the number of companies that are involved.</span></span> <span data-ttu-id="58ae5-249">次の例では、ユーザーが読み取りを承認されている会社のデータを返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-249">The following example returns data for companies that the user is authorized to read from.</span></span> <span data-ttu-id="58ae5-250">結果は **dat** および **dmo** 会社に限定されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-250">Results are limited to the **dat** and **dmo** companies.</span></span>

```xpp
CustTable custTable;
container conCompanies = ['dat','dmo'];
select crossCompany :conCompanies
    * from custTable;
```

## <a name="desc-keyword"></a><span data-ttu-id="58ae5-251">降順キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-251">desc keyword</span></span>

<span data-ttu-id="58ae5-252">**desc** キーワードは、**order by** または **group by** 句のオプションです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-252">The **desc** keyword is an option on the **order by** or **group by** clause.</span></span> <span data-ttu-id="58ae5-253">降順の並べ替え順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-253">It specifies a descending sort order.</span></span> <span data-ttu-id="58ae5-254">**昇順** または **降順** のどちらも指定されない場合、並べ替えは降順になります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-254">If neither **asc** nor **desc** is specified, the sort is ascending.</span></span>

```xpp
CustTable custTable;
select * from custTable
    order by Value desc;
```

## <a name="exists-keyword"></a><span data-ttu-id="58ae5-255">exists キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-255">exists keyword</span></span>

<span data-ttu-id="58ae5-256">**exists** キーワードは、ブール値と **結合** 句を返すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-256">The **exists** keyword is a method that returns a Boolean value and a **join** clause.</span></span>

```xpp
CtrTable ctrTable;
CustTable custTable;
while select AccountNum, Value from custTable
    order by AccountNum
    exists join * from ctrTable
    where (ctrTable.AccountNum == custTable.AccountNum)
{
}
```

## <a name="firstfast-keyword"></a><span data-ttu-id="58ae5-257">firstFast キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-257">firstFast keyword</span></span>

<span data-ttu-id="58ae5-258">**Firstfast** キーワードは優先順位のヒントです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-258">The **firstFast** keyword is a priority hint.</span></span> <span data-ttu-id="58ae5-259">最初の行はより迅速に表示されますが、このオプションの合計戻り時間は遅くなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-259">The first row appears more quickly, but the total return time for this option might be slower.</span></span> <span data-ttu-id="58ae5-260">**firstFast** ヒントは、すべてのページから自動的に発行されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-260">The **firstFast** hint is automatically issued from all pages.</span></span>

<span data-ttu-id="58ae5-261">次のコード例では、最初の行をすばやく返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-261">The following code example quickly returns the first row.</span></span>

```xpp
CustTable custTable;
select firstFast custTable
    order by AccountNum;
```

## <a name="firstonly-firstonly10-firstonly100-and-firstonly1000-keywords"></a><span data-ttu-id="58ae5-262">firstOnly、firstOnly10、firstOnly100、および firstOnly1000 キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-262">firstOnly, firstOnly10, firstOnly100, and firstOnly1000 keywords</span></span>

<span data-ttu-id="58ae5-263">**firstOnly** キーワードは、限られた数の行を返すことによって、フェッチを高速化します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-263">The **firstOnly** keywords speed up the fetch by returning a limited number of rows.</span></span> <span data-ttu-id="58ae5-264">クエリに **firstOnly** を含めると、ランタイムはテーブル バッファーを返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-264">When you include **firstOnly** in your query, the runtime returns a table buffer.</span></span> <span data-ttu-id="58ae5-265">**firstOnly** を省略すると、レコードを反復処理できるオブジェクトがランタイムによって割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-265">When you omit **firstOnly**, the runtime allocates an object that can iterate over records.</span></span> <span data-ttu-id="58ae5-266">パフォーマンスの観点から、最初のレコードをフェッチすることを目的とする場合のみ **firstOnly** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-266">From a performance perspective, you should use **firstOnly** only when your intent is to fetch the first record.</span></span>

| <span data-ttu-id="58ae5-267">キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-267">Keyword</span></span>       | <span data-ttu-id="58ae5-268">説明</span><span class="sxs-lookup"><span data-stu-id="58ae5-268">Description</span></span>                |
|---------------|----------------------------|
| <span data-ttu-id="58ae5-269">firstOnly</span><span class="sxs-lookup"><span data-stu-id="58ae5-269">firstOnly</span></span>     | <span data-ttu-id="58ae5-270">最初の行のみを返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-270">Return only the first row.</span></span> |
| <span data-ttu-id="58ae5-271">firstOnly10</span><span class="sxs-lookup"><span data-stu-id="58ae5-271">firstOnly10</span></span>   | <span data-ttu-id="58ae5-272">10 行を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-272">Return 10 rows.</span></span>            |
| <span data-ttu-id="58ae5-273">firstOnly100</span><span class="sxs-lookup"><span data-stu-id="58ae5-273">firstOnly100</span></span>  | <span data-ttu-id="58ae5-274">100 行を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-274">Return 100 rows.</span></span>           |
| <span data-ttu-id="58ae5-275">firstOnly1000</span><span class="sxs-lookup"><span data-stu-id="58ae5-275">firstOnly1000</span></span> | <span data-ttu-id="58ae5-276">1,000 行を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-276">Return 1,000 rows.</span></span>         |

<span data-ttu-id="58ae5-277">次のコード例では、結果の最初の行のみが返されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-277">The following code example returns only the first row of the results.</span></span>

```xpp
CustTable custTable;
select firstOnly custTable
    index hint AccountIdx
    where custTable.AccountNum == '5000';
```

## <a name="forceliterals-keyword"></a><span data-ttu-id="58ae5-278">forceLiterals キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-278">forceLiterals keyword</span></span>

<span data-ttu-id="58ae5-279">**forceLiterals** キーワードは、最適化時に Microsoft SQL Server データベースに対して **where** 句で使用される実際値を明らかにするように、カーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-279">The **forceLiterals** keyword instructs the kernel to reveal the actual values that are used in **where** clauses to the Microsoft SQL Server database at the time of optimization.</span></span> <span data-ttu-id="58ae5-280">**forceLiterals** および **forcePlaceholders** キーワードは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="58ae5-280">The **forceLiterals** and **forcePlaceholders** keywords are mutually exclusive.</span></span> <span data-ttu-id="58ae5-281">詳細については、[forcePlaceholders キーワード](#forceplaceholders-keyword) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-281">For more information, see the [forcePlaceholders keyword](#forceplaceholders-keyword) section.</span></span>

> [!WARNING]
> <span data-ttu-id="58ae5-282">**選択** 明細書に **forceLiterals** キーワードは使用しないでください。SQL インジェクションのセキュリティ脅威にさらされるためです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-282">You should not use the **forceLiterals** keyword in **select** statements, because it could expose code to an SQL injection security threat.</span></span>

## <a name="forcenestedloop-keyword"></a><span data-ttu-id="58ae5-283">forceNestedLoop キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-283">forceNestedLoop keyword</span></span>

<span data-ttu-id="58ae5-284">**forceNestedLoop** キーワードを使用すると、SQL Server データベースはネストループ アルゴリズムを使用して、結合アルゴリズムを含む特定の SQL ステートメントを処理します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-284">The **forceNestedLoop** keyword forces the SQL Server database to use a nested-loop algorithm to process a particular SQL statement that contains a join algorithm.</span></span> <span data-ttu-id="58ae5-285">したがって、2 番目のテーブルのレコードがフェッチされる前に、1 番目のテーブルのレコードがフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-285">Therefore, a record from the first table is fetched before any records from the second table are fetched.</span></span> <span data-ttu-id="58ae5-286">通常、ハッシュ結合やマージ結合などの他の結合アルゴリズムが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-286">Typically, other join algorithms, such as hash joins and merge joins, are considered.</span></span> <span data-ttu-id="58ae5-287">このキーワードは、**forceSelectOrder** キーワードと組み合わされることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-287">This keyword is often combined with the **forceSelectOrder** keyword.</span></span>

```xpp
CustGroup custGroup;
CustTable custTable;

while select forceNestedLoop custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    Info(custTable.CustGroup);
}
```

## <a name="forceplaceholders-keyword"></a><span data-ttu-id="58ae5-288">forcePlaceholders キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-288">forcePlaceholders keyword</span></span>

<span data-ttu-id="58ae5-289">**forcePlaceholders** キーワードは、最適化時に SQL Server データベースに対して **where** 句で使用される実際値を明らかに **しない** ように、カーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-289">The **forcePlaceholders** keyword instructs the kernel **not** to reveal the actual values that are used in **where** clauses to the SQL Server database at the time of optimization.</span></span> <span data-ttu-id="58ae5-290">既定では、この動作は **結合** ステートメントではないすべてのステートメントで使用されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-290">By default, this behavior is used in all statements that aren't **join** statements.</span></span> <span data-ttu-id="58ae5-291">このキーワードを使用する利点は、他の検索値がある同様の明細書のアクセス計画をカーネルが再利用できることです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-291">The advantage of using this keyword is that the kernel can reuse the access plan for similar statements that have other search values.</span></span> <span data-ttu-id="58ae5-292">欠点は、アクセス計画が計算されても、データの配布が不均一になる可能性があるという事実が考慮されないことです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-292">The disadvantage is that, although the access plan is computed, the fact that data distribution might be uneven isn't considered.</span></span> <span data-ttu-id="58ae5-293">アクセス計画は、平均的なアクセス計画です。</span><span class="sxs-lookup"><span data-stu-id="58ae5-293">The access plan is an on-average access plan.</span></span> <span data-ttu-id="58ae5-294">**forcePlaceholders** および **forceLiterals** キーワードは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="58ae5-294">The **forcePlaceholders** and **forceLiterals** keywords are mutually exclusive.</span></span>

<span data-ttu-id="58ae5-295">次の例では、**CustTable** テーブルと結合されている **CustGroup** テーブルを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-295">The following example iterates through the **CustGroup** table that is joined with the **CustTable** table.</span></span>

```xpp
CustGroup custGroup;
CustTable custTable;

while select forcePlaceholders custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    Info(custTable.CustGroup);
}
```

## <a name="forceselectorder-keyword"></a><span data-ttu-id="58ae5-296">forceSelectOrder キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-296">forceSelectOrder keyword</span></span>

<span data-ttu-id="58ae5-297">**forceSelectOrder** キーワードを指定すると、SQL Server データベースは指定した順序で結合内のテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="58ae5-297">The **forceSelectOrder** keyword forces the SQL Server database to access the tables in a join in the specified order.</span></span> <span data-ttu-id="58ae5-298">2 つのテーブルが結合している場合、明細書の最初のテーブルに最初にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="58ae5-298">If two tables are joined, the first table in the statement is always accessed first.</span></span> <span data-ttu-id="58ae5-299">このキーワードは、**forceNestedLoop** キーワードと組み合わされることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-299">This keyword is often combined with the **forceNestedLoop** keyword.</span></span>

<span data-ttu-id="58ae5-300">次の例では、**CustGroup** フィールドの CustGroup および CustTable テーブルを結合します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-300">The following example joins the CustGroup and CustTable tables on the **CustGroup** field.</span></span>

```xpp
CustGroup custGroup;
CustTable custTable;

while select forceSelectOrder custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    Info(custTable.CustGroup);
}
```

## <a name="forupdate-keyword"></a><span data-ttu-id="58ae5-301">forUpdate キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-301">forUpdate keyword</span></span>

<span data-ttu-id="58ae5-302">**forUpdate** キーワードは、更新用にのみレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-302">The **forUpdate** keyword selects records for update only.</span></span> <span data-ttu-id="58ae5-303">基になるデータベースによっては、レコードが他のユーザーのためにロックされるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-303">Depending on the underlying database, the records might be locked for other users.</span></span> <span data-ttu-id="58ae5-304">次の例では、**AccountNum** の値が **2000** であるレコードの更新のために、CustTable テーブルの **CreditMax** 列を選択します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-304">The following example selects the **CreditMax** column in the CustTable table for update, for the record where the **AccountNum** value is **2000**.</span></span>

```xpp
ttsBegin;
    CustTable custTable;
    select forUpdate custTable
        where custTable.AccountNum == '2000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

## <a name="group-by-keyword"></a><span data-ttu-id="58ae5-305">group by キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-305">group by keyword</span></span>

<span data-ttu-id="58ae5-306">**group by** キーワードは、選択したレコードをフィールドごとにグループ化するようデータベースに指示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-306">The **group by** keyword instructs the database to group selected records by fields.</span></span>

```xpp
CustTable custTable;
while select sum(CreditMax) from custTable
    group by CustGroup
{
    info(custTable.CustGroup + ' ' + int642Str(custTable.CreditMax));
}
```

## <a name="in-keyword"></a><span data-ttu-id="58ae5-307">in キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-307">in keyword</span></span>

<span data-ttu-id="58ae5-308">**in** キーワードは、値がリストに含まれている行をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-308">The **in** keyword filters rows where a value is contained in a list.</span></span>

<span data-ttu-id="58ae5-309">**in** キーワードを使用しない場合、記述するコードは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-309">If you don't use the **in** keyword, the code that you write will resemble the following example.</span></span>

```X++
// This code doesn't use the in keyword.
private CostAmountStdAdjustment calcCostAmountStdAdjustment()
{
    InventSettlement inventSettlement;

    select sum(CostAmountAdjustment) from inventSettlement
        where inventSettlement.TransRecId == this.RecId
            && inventSettlement.Cancelled == NoYes::No
            && (inventSettlement.OperationsPosting == LedgerpostingType::purchStdProfit
                || inventSettlement.OperationsPosting == LedgerpostingType::purchStdLoss
                || inventSettlement.OperationsPosting == LedgerpostingType::InventStdProfit
                || inventSettlement.OperationsPosting == LedgerpostingType::InventStdLoss);

    return inventSettlement.CostAmountAdjustment;
}
```

<span data-ttu-id="58ae5-310">**in** キーワードを使用する場合、記述するコードは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-310">If you use the **in** keyword, the code that you write will resemble the following example.</span></span>

```X++
// This code uses the in keyword.
private CostAmountStdAdjustment calcCostAmountStdAdjustment()
{
    InventSettlement inventSettlement;
    container ledgerPostingTypes = this.ledgerPostingTypesForCostAmountStdAdjustmentCalculation();

    select sum(CostAmountAdjustment) from inventSettlement
        where inventSettlement.TransRecId == this.RecId
            && inventSettlement.Cancelled == NoYes::No
            && inventSettlement.OperationsPosting in ledgerPostingTypes;

    return inventSettlement.CostAmountAdjustment;
}

protected container ledgerPostingTypesForCostAmountStdAdjustmentCalculation()
{
return [
    LedgerPostingType::purchStdProfit,
    LedgerPostingType::PurchStdLoss,
    LedgerPostingType::InventStdProfit,
    LedgerPostingType::InventStdLoss
];
}
```

## <a name="index-keyword"></a><span data-ttu-id="58ae5-311">index キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-311">index keyword</span></span>

<span data-ttu-id="58ae5-312">**index** キーワードは、選択されたレコードをインデックスで指定されたとおりに並べ替えるようデータベースに指示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-312">The **index** keyword instructs the database to sort the selected records as specified by the index.</span></span>

```xpp
CustTable custTable;
while select AccountNum, Value from custTable
    index AccountIdx
{
    Info(custTable.AccountNum +  ": " + int642Str(custTable.Value));
}
```

## <a name="index-hint-keyword"></a><span data-ttu-id="58ae5-313">index hint キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-313">index hint keyword</span></span>

<span data-ttu-id="58ae5-314">**index hint** キーワードは、特定のインデックスを使用して、選択されたレコードをインデックスで指定されたとおりに並べ替えるためのヒントをデータベースに提供します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-314">The **index hint** keyword gives the database a hint to use a specific index to sort the selected records as specified in the index.</span></span> <span data-ttu-id="58ae5-315">データベースはヒントを無視できます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-315">The database can ignore the hint.</span></span> <span data-ttu-id="58ae5-316">インデックス ヒントが正しくない場合はパフォーマンスに大きな影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-316">An incorrect index hint can greatly affect performance.</span></span> <span data-ttu-id="58ae5-317">インデックス ヒントは、動的な **where** 句または **order by** 句がない SQL ステートメント、およびヒントの効果を確認できる SQL ステートメントにのみ適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-317">Index hints should be applied only to SQL statements that don't have dynamic **where** clauses or **order by** clauses, and where the effect of the hint can be verified.</span></span>

<span data-ttu-id="58ae5-318">クエリで **index hint** を使用する前に、テーブルで **allowIndexHint(true)** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-318">Before you can use **index hint** in queries, you must call **allowIndexHint(true)** on the table.</span></span> <span data-ttu-id="58ae5-319">**index hint** の既定の動作 **false** であり、ヒントは無視されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-319">The default behavior for **index hint** is **false**, and the hint is ignored.</span></span>

> [!WARNING]
> <span data-ttu-id="58ae5-320">**index hint** は慎重に注意して使用し、パフォーマンスが向上することが確実な場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-320">You should use **index hint** sparingly and with caution, and only when you can be sure that it improves performance.</span></span> <span data-ttu-id="58ae5-321">**index hint** キーワードと API を使用すると、必要に応じて正しいヒントを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-321">The **index hint** keyword and API let you pass the correct hints when they are required.</span></span> <span data-ttu-id="58ae5-322">疑問がある場合は、**index hint** の使用を避けてください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-322">If you're ever in doubt, avoid using **index hint**.</span></span>

<span data-ttu-id="58ae5-323">次の例では、**AccountIdx** インデックスを使用して、クエリ内のレコードを CustTable テーブルで並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-323">In the following example, the **AccountIdx** index is used to sort the records in the query on the CustTable table.</span></span>

```xpp
str _accountNum = '111';
CustTable custTable;
custTable.allowIndexHint(true);

while select forUpdate custTable
    index hint AccountIdx
    where custTable.AccountNum == _accountNum
{
}
```

## <a name="join-keyword"></a><span data-ttu-id="58ae5-324">join キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-324">join keyword</span></span>

<span data-ttu-id="58ae5-325">**join** キーワードは、両方のテーブルで共有される列のテーブルを結合するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-325">The **join** keyword is used to join tables on a column that is shared by both tables.</span></span> <span data-ttu-id="58ae5-326">SQL に見られるような **on** キーワードがないため、結合基準は **where** 句で指定されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-326">The join criteria are specified in a **where** clause, because there is no **on** keyword, such as is found in SQL.</span></span> <span data-ttu-id="58ae5-327">このキーワードは、テーブルをループして関連テーブルのトランザクションを更新する場合に必要な SQL ステートメントの数を減らします。</span><span class="sxs-lookup"><span data-stu-id="58ae5-327">This keyword reduces the number of SQL statements that are required if you want to loop through a table and update transactions in a related table.</span></span> <span data-ttu-id="58ae5-328">たとえば、テーブル内の 500 のレコードを処理し、別のテーブルで関連するレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-328">For example, you process 500 records in a table and want to update related records in another table.</span></span> <span data-ttu-id="58ae5-329">入れ子になった **while select** を使用する場合、データベースへの 501 トリップがあります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-329">If you use a nested **while select**, there will be 501 trips to the database.</span></span> <span data-ttu-id="58ae5-330">ただし、**結合** を使用する場合、データベースへのトリップは 1 回だけになります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-330">However, if you use a **join**, there will be just one trip to the database.</span></span>

```xpp
CustTable custTable;
CustGroup custGroup;
int totalCredit;

while select custGroup
    join custTable
    where custGroup.CustGroup == custTable.CustGroup
{
    totalCredit += custTable.CreditMax;
}
}
```

## <a name="maxof-keyword"></a><span data-ttu-id="58ae5-331">maxof キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-331">maxof keyword</span></span>

<span data-ttu-id="58ae5-332">**maxof** キーワードはフィールドの最大値を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-332">The **maxof** keyword returns the maximum of the fields.</span></span>

```xpp
CustTable custTable;
select maxof(CreditMax) from custTable;
info(int642Str(custTable.Value));
```

## <a name="minof-keyword"></a><span data-ttu-id="58ae5-333">minof キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-333">minof keyword</span></span>

<span data-ttu-id="58ae5-334">**minof** キーワードはフィールドの最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-334">The **minof** keyword returns the minimum of the fields.</span></span>

```xpp
CustTable custTable;
select minof(CreditMax) from custTable;
info(int642Str(custTable.Value));
```

## <a name="nofetch-keyword"></a><span data-ttu-id="58ae5-335">noFetch キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-335">noFetch keyword</span></span>

<span data-ttu-id="58ae5-336">**noFetch** キーワードは、今すぐレコードを取得する必要がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-336">The **noFetch** keyword indicates that no records should be fetched now.</span></span> <span data-ttu-id="58ae5-337">このキーワードは通常、**select** 文の結果を、実際のフェッチを実行するクエリなどの別のアプリケーション オブジェクトに渡すときに使用します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-337">Typically, this keyword is used when the result of the **select** statement is passed on to another application object, such as a query that performs the actual fetch.</span></span>

<span data-ttu-id="58ae5-338">次の例では、クエリ変数を作成しますがレコードはフェッチしません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-338">The following example creates a query variable but doesn't fetch the records.</span></span>

```xpp
CustTable custTable;
select noFetch custTable
    order by AccountNum;
```

## <a name="notexists-keyword"></a><span data-ttu-id="58ae5-339">notExists キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-339">notExists keyword</span></span>

<span data-ttu-id="58ae5-340">転記がない場合にのみ、**notExists** キーワードが選択されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-340">The **notExists** keyword is selected only if there are no posts.</span></span>

``` xpp
CustTable custTable;
CtrTable ctrTable;

while select AccountNum, Value from custTable
    order by AccountNum
    notExists join * from ctrTable
    where (ctrTable.AccountNum == custTable.AccountNum)
{
}
```

## <a name="optimisticlock-keyword"></a><span data-ttu-id="58ae5-341">optimisticLock キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-341">optimisticLock keyword</span></span>

<span data-ttu-id="58ae5-342">**optimisticLock** キーワードは、テーブルに異なる値が設定されていても、オプティミスティック同時実行制御を使用してステートメントを実行させます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-342">The **optimisticLock** keyword forces a statement to run by using optimistic concurrency control, even if a different value is set on the table.</span></span>

```xpp
CustTable custTable;
select optimisticLock custTable
    where custTable.AccountNum > '1000';
```

## <a name="order-by-keyword"></a><span data-ttu-id="58ae5-343">order by キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-343">order by keyword</span></span>

<span data-ttu-id="58ae5-344">**order by** キーワードは、選択されたレコードを **order by** リストのフィールドで並べ替えるようデータベースに指示します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-344">The **order by** keyword instructs the database to sort the selected records by the fields in the **order by** list.</span></span> <span data-ttu-id="58ae5-345">キーワード **by** はオプションです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-345">The keyword **by** is optional.</span></span>

```xpp
CustTable custTable;
select * from custTable
    order by accountNum desc
    where custTable.AccountNum > '100';
info("AccountNum: " + custTable.AccountNum);
```

<span data-ttu-id="58ae5-346">次の例では、CustTable テーブルの最も高い **AccountNum** 値を出力します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-346">The following example prints the highest **AccountNum** value in the CustTable table.</span></span>

```xpp
CustTable custTable;
select reverse custTable
    order by accountNum;
info("AccountNum: " + custTable.AccountNum);
```

## <a name="outer-keyword"></a><span data-ttu-id="58ae5-347">outer キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-347">outer keyword</span></span>

<span data-ttu-id="58ae5-348">**outer** キーワードは、最初に名前が付けられたテーブルからすべての行を返します。2 番目に名前が付けられたテーブルで一致するものがない行も返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-348">The **outer** keyword returns all rows from the table that is named first, even rows that have no match in the table that is named second.</span></span> <span data-ttu-id="58ae5-349">この結合は左外部結合です。</span><span class="sxs-lookup"><span data-stu-id="58ae5-349">This join is a left outer join.</span></span> <span data-ttu-id="58ae5-350">既定値は、他の結合テーブルの一致する行から取得できなかったデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-350">Default values are substituted for any data that could not be obtained from a matching row in the other joined table.</span></span>

<span data-ttu-id="58ae5-351">**left** キーワードはなく、右外部結合もありません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-351">There is no **left** keyword, and there is no right outer join.</span></span>

<span data-ttu-id="58ae5-352">内部結合については、**on** 句でフィルター処理する場合の動作は **where** 句でフィルター処理する場合の動作と同じです。</span><span class="sxs-lookup"><span data-stu-id="58ae5-352">For an inner join, the behavior if you filter on an **on** clause is the same as the behavior if you filter on the **where** clause.</span></span>

```xpp
CustTable custTable;
CustGroup custGroupTable;

while select CustGroup from custGroupTable
    order by CustGroup
    outer join * from custGroupTable
    where custTable.CustGroup == custGroupTable.CustGroup
{
    Info(custTable.CustGroup + ', ' + custGroupTable.Name);
}
```

<span data-ttu-id="58ae5-353">次の例は、2 つのテーブルに基づいています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-353">The following example is based on two tables.</span></span> <span data-ttu-id="58ae5-354">フィールド タイプとサンプル データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-354">The field types and example data are included.</span></span> <span data-ttu-id="58ae5-355">SalesOrder 親テーブルと SalesOrderLine 子テーブルの間には、一対多の関係があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-355">There is a one-to-many relationship between the SalesOrder parent table and the SalesOrderLine child table.</span></span> <span data-ttu-id="58ae5-356">SalesOrder テーブルの各行に対して、 SalesOrderLine テーブルには 0 (ゼロ) またはそれ以上の行があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-356">For each row in the SalesOrder table, there are 0 (zero) or more rows in the SalesOrderLine table.</span></span> <span data-ttu-id="58ae5-357">SalesOrder テーブルには 2 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-357">There are two rows in the SalesOrder table.</span></span>

| <span data-ttu-id="58ae5-358">SalesOrderID (整数、主キー)</span><span class="sxs-lookup"><span data-stu-id="58ae5-358">SalesOrderID (integer, primary key)</span></span> | <span data-ttu-id="58ae5-359">DateAdded (日付)</span><span class="sxs-lookup"><span data-stu-id="58ae5-359">DateAdded (date)</span></span> |
|-------------------------------------|------------------|
| <span data-ttu-id="58ae5-360">1</span><span class="sxs-lookup"><span data-stu-id="58ae5-360">1</span></span>                                   | <span data-ttu-id="58ae5-361">2010-01-01</span><span class="sxs-lookup"><span data-stu-id="58ae5-361">2010-01-01</span></span>       |
| <span data-ttu-id="58ae5-362">2</span><span class="sxs-lookup"><span data-stu-id="58ae5-362">2</span></span>                                   | <span data-ttu-id="58ae5-363">2010-02-02</span><span class="sxs-lookup"><span data-stu-id="58ae5-363">2010-02-02</span></span>       |

<span data-ttu-id="58ae5-364">SalesOrderLine テーブルには、**SalesOrderID** という名前の外部キー フィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-364">The SalesOrderLine table contains a foreign key field that is named **SalesOrderID**.</span></span> <span data-ttu-id="58ae5-365">このフィールドは、SalesOrder テーブルの主キー列を参照します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-365">This field references the primary key column of the SalesOrder table.</span></span> <span data-ttu-id="58ae5-366">**2** の **SalesOrderID** 値は、SalesOrderLine テーブルのデータには発生しません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-366">A **SalesOrderID** value of **2** doesn't occur in the data for the SalesOrderLine table.</span></span>

| <span data-ttu-id="58ae5-367">SalesOrderLineID (文字列、主キー)</span><span class="sxs-lookup"><span data-stu-id="58ae5-367">SalesOrderLineID (string, primary key)</span></span> | <span data-ttu-id="58ae5-368">数量 (整数)</span><span class="sxs-lookup"><span data-stu-id="58ae5-368">Quantity (integer)</span></span> | <span data-ttu-id="58ae5-369">SalesOrderID (整数、外部キー)</span><span class="sxs-lookup"><span data-stu-id="58ae5-369">SalesOrderID (integer, foreign key)</span></span> |
|----------------------------------------|--------------------|-------------------------------------|
| <span data-ttu-id="58ae5-370">AA</span><span class="sxs-lookup"><span data-stu-id="58ae5-370">AA</span></span>                                     | <span data-ttu-id="58ae5-371">32</span><span class="sxs-lookup"><span data-stu-id="58ae5-371">32</span></span>                 | <span data-ttu-id="58ae5-372">1</span><span class="sxs-lookup"><span data-stu-id="58ae5-372">1</span></span>                                   |
| <span data-ttu-id="58ae5-373">BB</span><span class="sxs-lookup"><span data-stu-id="58ae5-373">BB</span></span>                                     | <span data-ttu-id="58ae5-374">67</span><span class="sxs-lookup"><span data-stu-id="58ae5-374">67</span></span>                 | <span data-ttu-id="58ae5-375">1</span><span class="sxs-lookup"><span data-stu-id="58ae5-375">1</span></span>                                   |
| <span data-ttu-id="58ae5-376">CC</span><span class="sxs-lookup"><span data-stu-id="58ae5-376">CC</span></span>                                     | <span data-ttu-id="58ae5-377">66</span><span class="sxs-lookup"><span data-stu-id="58ae5-377">66</span></span>                 | <span data-ttu-id="58ae5-378">1</span><span class="sxs-lookup"><span data-stu-id="58ae5-378">1</span></span>                                   |

<span data-ttu-id="58ae5-379">次のコードでは、**select** ステートメントで 2 つのテーブルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-379">The following code has a **select** statement that reads the two tables.</span></span> <span data-ttu-id="58ae5-380">**select** ステートメントには、左の **outer join** 句が含まれています。</span><span class="sxs-lookup"><span data-stu-id="58ae5-380">The **select** statement includes a left **outer join** clause.</span></span> <span data-ttu-id="58ae5-381">結合基準とデータ フィルターは両方とも **where** 句にあります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-381">Both the join criteria and the data filter are on the **where** clause.</span></span> <span data-ttu-id="58ae5-382">コードからの出力も表示されます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-382">The output from the code is also shown.</span></span> <span data-ttu-id="58ae5-383">出力の 2 番目のレコードには、値が **2** の **SalesOrderID** があります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-383">The second record in the output has a **SalesOrderID** value of **2**.</span></span> <span data-ttu-id="58ae5-384">ただし、その値は SalesOrderLine テーブルに存在しません。</span><span class="sxs-lookup"><span data-stu-id="58ae5-384">However, that value isn't present in the SalesOrderLine table.</span></span> <span data-ttu-id="58ae5-385">したがって、2 番目のレコードのフィールドの一部には、整数の場合は **0**、文字列の場合は長さゼロの文字列が既定値となります。</span><span class="sxs-lookup"><span data-stu-id="58ae5-385">Therefore, some of the fields in the second record have default values: **0** for an integer and a zero-length string for a string.</span></span>

```xpp
SalesOrder recSalesOrder;
SalesOrderLine recSalesOrderLine;
struct struct4 = new struct
    ("int SalesOrderID;"
    + "date DateAdded;"
    + "str SalesOrderLineID;"
    + "int Quantity"
    );
while select *
    from
        recSalesOrder
        outer join recSalesOrderLine
    where
        recSalesOrder.SalesOrderID == recSalesOrderLine.SalesOrderID
        && recSalesOrderLine.Quantity == 66
{
    struct4.value("SalesOrderID", recSalesOrder.SalesOrderID);
    struct4.value("DateAdded", recSalesOrder.DateAdded);
    struct4.value("SalesOrderLineID", recSalesOrderLine.SalesOrderLineID);
    struct4.value("Quantity", recSalesOrderLine.Quantity);
    info(struct4.toString());
}

// Example output:
// (SalesOrderID:1; DateAdded:2010/1/1; SalesOrderLineID:"CC"; Quantity:66)
// (SalesOrderID:2; DateAdded:2010/2/2; SalesOrderLineID:""; Quantity:0)
```

## <a name="pessimisticlock-keyword"></a><span data-ttu-id="58ae5-386">pessimisticLock キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-386">pessimisticLock keyword</span></span>

<span data-ttu-id="58ae5-387">**pessimisticLock** キーワードは、テーブルに異なる値が設定されていても、ペシミスティック同時実行制御を使用してステートメントを実行させます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-387">The **pessimisticLock** keyword forces a statement to run by using pessimistic concurrency control, even if a different value is set on the table.</span></span>

```xpp
CustTable custTable;
select pessimisticLock custTable
    where custTable.AccountNum > '1000';
```

## <a name="repeatableread-keyword"></a><span data-ttu-id="58ae5-388">repeatableRead キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-388">repeatableRead keyword</span></span>

<span data-ttu-id="58ae5-389">この **repeatableRead** キーワードは、他の取引が現在の取引内のロジックによって読み取られたデータを変更する前に、現在の取引を完了する必要があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-389">This **repeatableRead** keyword specifies that the current transaction must be completed before other transactions can modify data that has been read by logic inside the current transaction.</span></span> <span data-ttu-id="58ae5-390">明示的なトランザクションは **ttsAbort** または最も外側の **ttsCommit** のいずれかで完了します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-390">An explicit transaction is completed at either **ttsAbort** or the outermost **ttsCommit**.</span></span> <span data-ttu-id="58ae5-391">スタンドアロンの **select** 明細書では、トランザクション期間は **select** コマンドの期間です。</span><span class="sxs-lookup"><span data-stu-id="58ae5-391">For a standalone **select** statement, the transaction duration is the duration of the **select** command.</span></span> <span data-ttu-id="58ae5-392">ただし、このキーワードがコードに表示されない場合でも、データベースは時に、個々の **選択** ステートメントの **repeatableRead** と同等のものを実施します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-392">However, the database sometimes enforces the equivalent of **repeatableRead** in individual **select** statements, even if this keyword doesn't appear in your code.</span></span> <span data-ttu-id="58ae5-393">(動作は、テーブルをスキャンするかどうかを決定するためにデータベースが使用する方法によって異なります。) 詳細については、基になるリレーショナル データベース製品のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58ae5-393">(The behavior depends on the method that the database uses to determine whether it should scan the tables.) For more information, see the documentation for the underlying relational database product.</span></span>

## <a name="reverse-keyword"></a><span data-ttu-id="58ae5-394">reverse キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-394">reverse keyword</span></span>

<span data-ttu-id="58ae5-395">**reverse** キーワードは、逆の順序レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-395">The **reverse** keyword returns records in reverse order.</span></span>

```xpp
CustTable custTable;
select reverse custTable
    order by AccountNum;
```

## <a name="sum-keyword"></a><span data-ttu-id="58ae5-396">sum キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-396">sum keyword</span></span>

<span data-ttu-id="58ae5-397">**sum** キーワードはフィールドの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-397">The **sum** keyword returns the sum of the fields.</span></span> <span data-ttu-id="58ae5-398">すべてのアカウント、注文明細行などの合計を計算するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="58ae5-398">It can be used to sum all accounts, order lines, and so on.</span></span>

```xpp
CustTable custTable;
select sum(CreditMax) from custTable;
info(int642Str(custTable.Value));
```

## <a name="validtimestate-keyword"></a><span data-ttu-id="58ae5-399">validTimeState キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-399">validTimeState keyword</span></span>

<span data-ttu-id="58ae5-400">**validTimeState** キーワードは、**ValidTimeStateFieldType** プロパティが **なし** 以外の値に設定されているテーブルの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-400">The **validTimeState** keyword selects rows from a table where the **ValidTimeStateFieldType** property is set to a value other than **None**.</span></span>

```xpp
CustPackingSlipTransHistory history;
utcDateTime dateFrom, dateTo = DateTimeUtil::utcNow();
anytype recid = -1;
select
    validTimeState(dateFrom, dateTo)
    *
    from history;
recid = history.RecId;
info('RecId:' + int642Str(recid));
```

## <a name="where-keyword"></a><span data-ttu-id="58ae5-401">where キーワード</span><span class="sxs-lookup"><span data-stu-id="58ae5-401">where keyword</span></span>

<span data-ttu-id="58ae5-402">**where** キーワードは、式が **true** であるテーブルのからの行をフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-402">The **where** keyword filters rows from a table where the expression is **true**.</span></span>

<span data-ttu-id="58ae5-403">次の例では、**AccountNum** の値が 100 を超える顧客を検索します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-403">The following example finds a customer that has an **AccountNum** value that is more than 100.</span></span>

```xpp
CustTable custTable;
select * from custTable
    where custTable.AccountNum > '100';
info("AccountNum: " + custTable.AccountNum);
```

<span data-ttu-id="58ae5-404">次の例では、100 よりも大きい、最小の **AccountNum** 値を出力します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-404">The following examples prints the lowest **AccountNum** value that is more than 100.</span></span>

```xpp
CustTable custTable;
select * from custTable
    order by accountNum
    where custTable.AccountNum > '100';
info("AccountNum: " + custTable.AccountNum);
```

<span data-ttu-id="58ae5-405">次の例では、100 よりも大きい、最大の **AccountNum** 値を出力します。</span><span class="sxs-lookup"><span data-stu-id="58ae5-405">The following example prints the highest **AccountNum** value that is more than 100.</span></span>

```xpp
CustTable custTable;
select * from custTable
    order by accountNum desc
    where custTable.accountNum > "100";
info("AccountNum: " + custTable.AccountNum);
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]