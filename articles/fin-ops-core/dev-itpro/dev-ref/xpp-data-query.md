---
title: X++ データの選択と操作
description: このトピックでは、X++ 言語でのデータの選択と操作のサポートについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150273
ms.assetid: 999a5ecf-559b-4d66-8b05-9a8e477e0518
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: a8a6e992cb2a38ff9e4f7581f46fc15775077b7f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183351"
---
# <a name="x-data-selection-and-manipulation"></a><span data-ttu-id="01f31-103">X++ データの選択と操作</span><span class="sxs-lookup"><span data-stu-id="01f31-103">X++ data selection and manipulation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01f31-104">このトピックでは、X++ 言語でのデータの選択と操作のサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="01f31-104">This topic describes the support for data selection and manipulation in the X++ language.</span></span>

<span data-ttu-id="01f31-105">データベースに格納されているデータにアクセスして取得するため、SQL ステートメントを対話的またはソース コード内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-105">You can use SQL statements, either interactively or within source code, to access and retrieve data that is stored in the database.</span></span> <span data-ttu-id="01f31-106">データの操作には、次のステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-106">You use the following statements for data manipulation:</span></span>

-   <span data-ttu-id="01f31-107">**選択** – 変更するデータを選択します。</span><span class="sxs-lookup"><span data-stu-id="01f31-107">**select** – Select the data to modify.</span></span>
-   <span data-ttu-id="01f31-108">**挿入** – 1 つ以上の新しいレコードをテーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="01f31-108">**insert** – Add one or more new records to a table.</span></span>
-   <span data-ttu-id="01f31-109">**更新** – 既存のテーブル レコードのデータを変更します。</span><span class="sxs-lookup"><span data-stu-id="01f31-109">**update** – Modify data in existing table records.</span></span>
-   <span data-ttu-id="01f31-110">**削除** – 既存のレコードをテーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="01f31-110">**delete** – Remove existing records from a table.</span></span>

<span data-ttu-id="01f31-111">データを変更する前に、**選択**ステートメントを使用して更新するデータを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-111">Before any data can be changed, you must use a **select** statement to select the data to update.</span></span> <span data-ttu-id="01f31-112">**select forUpdate** コマンドは、更新のためにのみレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="01f31-112">The **select forUpdate** command selects records for update only.</span></span> <span data-ttu-id="01f31-113">**insert**、**update**、**delete** ステートメントは、一度に 1 つのレコードに対して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="01f31-113">The **insert**, **update**, and **delete** statements perform operations on one record at a time.</span></span> <span data-ttu-id="01f31-114">**array insert**、**insert\_recordset**、**RecordInsertList**、**update\_recordset** ステートメントは、同時に複数のレコードに対して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="01f31-114">The **array insert**, **insert\_recordset**, **RecordInsertList**, and **update\_recordset** statements perform operations on multiple records at the same time.</span></span>

## <a name="select-statements"></a><span data-ttu-id="01f31-115">select ステートメント</span><span class="sxs-lookup"><span data-stu-id="01f31-115">select statements</span></span>
<span data-ttu-id="01f31-116">**select** ステートメントは、データベースからデータをフェッチまたは操作します。</span><span class="sxs-lookup"><span data-stu-id="01f31-116">The **select** statement fetches or manipulates data from the database.</span></span> <span data-ttu-id="01f31-117">すべての**選択**ステートメントではレコードをフェッチするためテーブル変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-117">All **select** statements use a table variable to fetch records.</span></span> <span data-ttu-id="01f31-118">この変数は、**select** 文を実行する前に宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-118">This variable must be declared before a **select** statement can be run.</span></span> <span data-ttu-id="01f31-119">**select** ステートメントは、レコードを 1 つだけ、またはフィールドをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="01f31-119">The **select** statement fetches only one record, or field.</span></span> <span data-ttu-id="01f31-120">追加のレコードを取得するには、**次** のステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-120">To fetch additional records, you can use the **next** statement.</span></span> <span data-ttu-id="01f31-121">**next** ステートメントは、テーブルの次のレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="01f31-121">The **next** statement fetches the next record in the table.</span></span> <span data-ttu-id="01f31-122">**選択**ステートメントの前に、**次**ステートメントがある場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="01f31-122">If no **select** statement precedes the **next** statement, an error occurs.</span></span> <span data-ttu-id="01f31-123">**次**ステートメントを使用する場合、**firstOnly** 検索オプションを使用しません。</span><span class="sxs-lookup"><span data-stu-id="01f31-123">If you use a **next** statement, don't use the **firstOnly** find option.</span></span> <span data-ttu-id="01f31-124">複数のレコードを通過する必要がある場合は、**while** **select** ステートメントを使用する方がより適切です。</span><span class="sxs-lookup"><span data-stu-id="01f31-124">If you must traverse several records, it's more appropriate to use a **while** **select** statement.</span></span> <span data-ttu-id="01f31-125">**select** ステートメントの結果はテーブル バッファ変数に返されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-125">The results of a **select** statement are returned in a table buffer variable.</span></span> <span data-ttu-id="01f31-126">**選択**ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-126">If you use a field list in the **select** statement, only those fields are available in the table variable.</span></span> <span data-ttu-id="01f31-127">**sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-127">If you use aggregate functions, such as **sum** or **count**, the results are returned in the fields that you perform the **sum** or **count** over.</span></span> <span data-ttu-id="01f31-128">整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-128">You can count, average, or sum only integer and real fields.</span></span>

## <a name="syntax-of-select-statements"></a><span data-ttu-id="01f31-129">Select 文の構文</span><span class="sxs-lookup"><span data-stu-id="01f31-129">Syntax of select statements</span></span>

|                   |   |    |
|-------------------|---|----|
|<span data-ttu-id="01f31-130">*SelectStatement*</span><span class="sxs-lookup"><span data-stu-id="01f31-130">*SelectStatement*</span></span>  | = | <span data-ttu-id="01f31-131"><i>パラメーター</i>を**選択する**</span><span class="sxs-lookup"><span data-stu-id="01f31-131">**select** <i>Parameters</i></span></span>  |
|<span data-ttu-id="01f31-132">[*パラメーター*]</span><span class="sxs-lookup"><span data-stu-id="01f31-132">*Parameters*</span></span>       | = | <span data-ttu-id="01f31-133">**\[ \[** *FindOptions* **\]** **\[** *FieldList* **から \] \]** *TableBufferVariable* **\[** *IndexClause* **\]** **\[** *オプション* **\]** **\[** *WhereClause* **\]** **\[** *JoinClause* **\]**</span><span class="sxs-lookup"><span data-stu-id="01f31-133">**\[ \[** *FindOptions* **\]** **\[** *FieldList* **from \] \]** *TableBufferVariable* **\[** *IndexClause* **\]** **\[** *Options* **\]** **\[** *WhereClause* **\]** **\[** *JoinClause* **\]**</span></span> |
|<span data-ttu-id="01f31-134">*FindOptions*</span><span class="sxs-lookup"><span data-stu-id="01f31-134">*FindOptions*</span></span>      | = | <span data-ttu-id="01f31-135">**crossCompany** \| **reverse** \| **firstFast** \| \[ **firstOnly** \| **firstOnly10** \| **firstOnly100** \| **firstOnly1000** \] \| **forUpdate** \| **noFetch** \| \[**forcePlaceholders** \| **forceLiterals**\] \| **forceselectorder** \| **forceNestedLoop** \| **repeatableRead** \| **validTimeState**</span><span class="sxs-lookup"><span data-stu-id="01f31-135">**crossCompany** \| **reverse** \| **firstFast** \| \[ **firstOnly** \| **firstOnly10** \| **firstOnly100** \| **firstOnly1000** \] \| **forUpdate** \| **noFetch** \| \[**forcePlaceholders** \| **forceLiterals**\] \| **forceselectorder** \| **forceNestedLoop** \| **repeatableRead** \| **validTimeState**</span></span> |                                              |
|<span data-ttu-id="01f31-136">*FieldList*</span><span class="sxs-lookup"><span data-stu-id="01f31-136">*FieldList*</span></span>        | = | <span data-ttu-id="01f31-137">*フィールド* **{ ,** *フィールド* **}** \| \*</span><span class="sxs-lookup"><span data-stu-id="01f31-137">*Field* **{ ,** *Field* **}** \| \*</span></span> |
|<span data-ttu-id="01f31-138">*フィールド*</span><span class="sxs-lookup"><span data-stu-id="01f31-138">*Field*</span></span>            | = | <span data-ttu-id="01f31-139">*集計* **(** \*FieldIdentifier\*\*\*)</span><span class="sxs-lookup"><span data-stu-id="01f31-139">*Aggregate* **(** *FieldIdentifier* \*\*)</span></span> |
|<span data-ttu-id="01f31-140">*集計*</span><span class="sxs-lookup"><span data-stu-id="01f31-140">*Aggregate*</span></span>        | = | <span data-ttu-id="01f31-141">**合計** \| **平均** \| **minof** \| **maxof** \| **集計**</span><span class="sxs-lookup"><span data-stu-id="01f31-141">**sum** \| **avg** \| **minof** \| **maxof** \| **count**</span></span> |
|<span data-ttu-id="01f31-142">*オプション*</span><span class="sxs-lookup"><span data-stu-id="01f31-142">*Options*</span></span>          | = | <span data-ttu-id="01f31-143">\[ **order by**, **group by**, *FieldIdentifier* \[ **昇順** \| **降順** \] {, *FieldIdentifier* \[ **昇順** \| **降順** \] }] \| \[  *IndexClause* \]</span><span class="sxs-lookup"><span data-stu-id="01f31-143">\[ **order by**, **group by**, *FieldIdentifier* \[ **asc** \| **desc** \] {, *FieldIdentifier* \[ **asc** \| **desc** \] }] \| \[  *IndexClause* \]</span></span>
|<span data-ttu-id="01f31-144">*IndexClause*</span><span class="sxs-lookup"><span data-stu-id="01f31-144">*IndexClause*</span></span>      | = | <span data-ttu-id="01f31-145">**インデックス** *IndexName* \| **インデックス ヒント** *IndexName*</span><span class="sxs-lookup"><span data-stu-id="01f31-145">**index** *IndexName* \| **index hint** *IndexName*</span></span> |
|<span data-ttu-id="01f31-146">*WhereClause*</span><span class="sxs-lookup"><span data-stu-id="01f31-146">*WhereClause*</span></span>      | = | <span data-ttu-id="01f31-147">**WHERE** *式*</span><span class="sxs-lookup"><span data-stu-id="01f31-147">**where** *Expression*</span></span> |
|<span data-ttu-id="01f31-148">*JoinClause*</span><span class="sxs-lookup"><span data-stu-id="01f31-148">*JoinClause*</span></span>       | = | <span data-ttu-id="01f31-149">\[**exists** \| **notexists** \| **outer** ] **join**  *Parameters*</span><span class="sxs-lookup"><span data-stu-id="01f31-149">\[**exists** \| **notexists** \| **outer** ] **join**  *Parameters*</span></span>|

### <a name="keywords-that-are-used-in-select-statements"></a><span data-ttu-id="01f31-150">select ステートメントで使用されるキーワード</span><span class="sxs-lookup"><span data-stu-id="01f31-150">Keywords that are used in select statements</span></span>

| <span data-ttu-id="01f31-151">キーワード</span><span class="sxs-lookup"><span data-stu-id="01f31-151">Keyword</span></span>           | <span data-ttu-id="01f31-152">説明</span><span class="sxs-lookup"><span data-stu-id="01f31-152">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="01f31-153">asc</span><span class="sxs-lookup"><span data-stu-id="01f31-153">asc</span></span>               | <span data-ttu-id="01f31-154">このキーワードは、**order by** または **group by** のオプションです。</span><span class="sxs-lookup"><span data-stu-id="01f31-154">This keyword is an option on the **order by** or **group by** clause.</span></span> <span data-ttu-id="01f31-155">昇順の並べ替えを指定します。</span><span class="sxs-lookup"><span data-stu-id="01f31-155">It specifies an ascending sort.</span></span> <span data-ttu-id="01f31-156">**昇順**または**降順**のどちらも指定されない場合、並べ替えは降順になります。</span><span class="sxs-lookup"><span data-stu-id="01f31-156">If neither **asc** nor **desc** is specified, the sort is ascending.</span></span>  |
| <span data-ttu-id="01f31-157">avg</span><span class="sxs-lookup"><span data-stu-id="01f31-157">avg</span></span>               | <span data-ttu-id="01f31-158">このキーワードはフィールドの平均を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-158">This keyword returns the average of the fields.</span></span>|
| <span data-ttu-id="01f31-159">カウント</span><span class="sxs-lookup"><span data-stu-id="01f31-159">count</span></span>             | <span data-ttu-id="01f31-160">このキーワードは、レコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-160">This keyword returns the number of records.</span></span> |
| <span data-ttu-id="01f31-161">crossCompany</span><span class="sxs-lookup"><span data-stu-id="01f31-161">crossCompany</span></span>      | <span data-ttu-id="01f31-162">このキーワードは、ユーザーが読み取りを承認されているすべての会社のデータを戻します。</span><span class="sxs-lookup"><span data-stu-id="01f31-162">This keyword returns data for all companies that the user is authorized to read from.</span></span> <span data-ttu-id="01f31-163">コンテナを追加して関連する会社の数を削減することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-163">You can add a container to reduce the number of companies that are involved.</span></span>  |
| <span data-ttu-id="01f31-164">desc</span><span class="sxs-lookup"><span data-stu-id="01f31-164">desc</span></span>              | <span data-ttu-id="01f31-165">このキーワードは、**order by** または **group by** のオプションです。</span><span class="sxs-lookup"><span data-stu-id="01f31-165">This keyword is an option on the **order by** or **group by** clause.</span></span> <span data-ttu-id="01f31-166">降順の並べ替えを指定します。</span><span class="sxs-lookup"><span data-stu-id="01f31-166">It specifies a descending sort.</span></span> <span data-ttu-id="01f31-167">**昇順**または**降順**のどちらも指定されない場合、並べ替えは降順になります。</span><span class="sxs-lookup"><span data-stu-id="01f31-167">If neither **asc** nor **desc** is specified, the sort is ascending.</span></span> |
| <span data-ttu-id="01f31-168">exists</span><span class="sxs-lookup"><span data-stu-id="01f31-168">exists</span></span>            | <span data-ttu-id="01f31-169">このキーワードは、ブール値と**結合**句を返すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="01f31-169">This keyword is a method that returns a Boolean value and a **join** clause.</span></span> |
| <span data-ttu-id="01f31-170">firstFast</span><span class="sxs-lookup"><span data-stu-id="01f31-170">firstFast</span></span>         | <span data-ttu-id="01f31-171">このキーワードは優先順位のヒントです。</span><span class="sxs-lookup"><span data-stu-id="01f31-171">This keyword is a priority hint.</span></span> <span data-ttu-id="01f31-172">最初の行はより迅速に表示されますが、このオプションの合計戻り時間は遅くなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-172">Although the first row appears more quickly, but the total return time for this option might be slower.</span></span> <span data-ttu-id="01f31-173">**firstFast** ヒントは、すべてのページから自動的に発行されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-173">The **firstFast** hint is automatically issued from all pages.</span></span> |
| <span data-ttu-id="01f31-174">firstOnly</span><span class="sxs-lookup"><span data-stu-id="01f31-174">firstOnly</span></span>         | <span data-ttu-id="01f31-175">このキーワードを使用すると、最初の行のみを戻すことでフェッチを高速化できます。</span><span class="sxs-lookup"><span data-stu-id="01f31-175">This keyword helps speed up the fetch by returning only the first row.</span></span> |
| <span data-ttu-id="01f31-176">firstOnly10</span><span class="sxs-lookup"><span data-stu-id="01f31-176">firstOnly10</span></span>       | <span data-ttu-id="01f31-177">このキーワードは **firstOnly** と同じですが、1 つではなく 10 行を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-177">This keyword is the same as **firstOnly**, but it returns 10 rows instead of one.</span></span> |
| <span data-ttu-id="01f31-178">firstOnly100</span><span class="sxs-lookup"><span data-stu-id="01f31-178">firstOnly100</span></span>      | <span data-ttu-id="01f31-179">このキーワードは **firstOnly** と同じですが、1 つではなく 100 行を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-179">This keyword is the same as **firstOnly**, but it returns 100 rows instead of one.</span></span> |
| <span data-ttu-id="01f31-180">firstOnly1000</span><span class="sxs-lookup"><span data-stu-id="01f31-180">firstOnly1000</span></span>     | <span data-ttu-id="01f31-181">このキーワードは **firstOnly** と同じですが、1 つではなく 1,000 行を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-181">This keyword is the same as **firstOnly**, but it returns 1,000 rows instead of one.</span></span> |
| <span data-ttu-id="01f31-182">forceLiterals</span><span class="sxs-lookup"><span data-stu-id="01f31-182">forceLiterals</span></span>     | <span data-ttu-id="01f31-183">このキーワードは、最適化時に Microsoft SQL Server データベースに対して **where** 句で使用される実際値を明らかするように、カーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-183">This keyword instructs the kernel to reveal the actual values that are used in **where** clauses to the Microsoft SQL Server database at the time of optimization.</span></span> <span data-ttu-id="01f31-184">**forceLiterals** および **forcePlaceholders** キーワードは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="01f31-184">The **forceLiterals** and **forcePlaceholders** keywords are mutually exclusive.</span></span> <span data-ttu-id="01f31-185">**選択** 明細書に **forceLiterals** キーワードは使用しないでください。SQL インジェクションのセキュリティ脅威にさらされるためです。</span><span class="sxs-lookup"><span data-stu-id="01f31-185">You should not to use the **forceLiterals** keyword in **select** statements, because it could expose code to an SQL injection security threat.</span></span>|
| <span data-ttu-id="01f31-186">forceNestedLoop</span><span class="sxs-lookup"><span data-stu-id="01f31-186">forceNestedLoop</span></span>   | <span data-ttu-id="01f31-187">このキーワードを使用すると、SQL Server データベースはネストループ アルゴリズムを使用して、結合アルゴリズムを含む特定の SQL ステートメントを処理します。</span><span class="sxs-lookup"><span data-stu-id="01f31-187">This keyword forces the SQL Server database to use a nested-loop algorithm to process a particular SQL statement that contains a join algorithm.</span></span> <span data-ttu-id="01f31-188">したがって、2 番目のテーブルのレコードがフェッチされる前に、1 番目のテーブルのレコードがフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="01f31-188">Therefore, a record from the first table is fetched before any records from the second table are fetched.</span></span> <span data-ttu-id="01f31-189">通常、ハッシュ結合やマージ結合などの他の結合アルゴリズムが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-189">Typically, other join algorithms, such as hash joins and merge joins, are considered.</span></span> <span data-ttu-id="01f31-190">このキーワードは、**forceSelectOrder** キーワードと組み合わされることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="01f31-190">This keyword is often combined with the **forceSelectOrder** keyword.</span></span> |
| <span data-ttu-id="01f31-191">forcePlaceholders</span><span class="sxs-lookup"><span data-stu-id="01f31-191">forcePlaceholders</span></span> | <span data-ttu-id="01f31-192">このキーワードは、最適化時に SQL Server データベースに対して **where** 句で使用される実際値を明らかに*しない*ように、カーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-192">This keyword instructs the kernel *not* to reveal the actual values that are used in **where** clauses to the SQL Server database at the time of optimization.</span></span> <span data-ttu-id="01f31-193">既定では、この動作は**結合**ステートメントではないすべてのステートメントで使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-193">By default, this behavior is used in all statements that aren't **join** statements.</span></span> <span data-ttu-id="01f31-194">このキーワードを使用する利点は、他の検索値がある同様の明細書のアクセス計画をカーネルが再利用できることです。</span><span class="sxs-lookup"><span data-stu-id="01f31-194">The advantage of using this keyword is that the kernel can reuse the access plan for similar statements that have other search values.</span></span> <span data-ttu-id="01f31-195">欠点は、アクセス計画が計算されることですが、データの配布が不均一である可能性があることは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="01f31-195">The disadvantage is that the access plan is computed, but the fact that data distribution might be uneven isn't considered.</span></span> <span data-ttu-id="01f31-196">アクセス計画は、平均的なアクセス計画です。</span><span class="sxs-lookup"><span data-stu-id="01f31-196">The access plan is an on-average access plan.</span></span> <span data-ttu-id="01f31-197">**forcePlaceholders** および **forceLiterals** キーワードは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="01f31-197">The **forcePlaceholders** and **forceLiterals** keywords are mutually exclusive.</span></span> |
| <span data-ttu-id="01f31-198">forceSelectOrder</span><span class="sxs-lookup"><span data-stu-id="01f31-198">forceSelectOrder</span></span>  | <span data-ttu-id="01f31-199">このキーワードを指定すると、SQL Server データベースは指定した順序で結合内のテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="01f31-199">This keyword forces the SQL Server database to access the tables in a join in the specified order.</span></span> <span data-ttu-id="01f31-200">2 つのテーブルが結合している場合、明細書の最初のテーブルに最初にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="01f31-200">If two tables are joined, the first table in the statement is always accessed first.</span></span> <span data-ttu-id="01f31-201">このキーワードは、**forceNestedLoop** キーワードと組み合わされることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="01f31-201">This keyword is often combined with the **forceNestedLoop** keyword.</span></span> |
| <span data-ttu-id="01f31-202">forUpdate</span><span class="sxs-lookup"><span data-stu-id="01f31-202">forUpdate</span></span>         | <span data-ttu-id="01f31-203">このキーワードは、更新のみのレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="01f31-203">This keyword selects records for update only.</span></span> <span data-ttu-id="01f31-204">基になるデータベースによっては、レコードが他のユーザーのためにロックされるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="01f31-204">Depending on the underlying database, the records might be locked for other users.</span></span> |
| <span data-ttu-id="01f31-205">group by</span><span class="sxs-lookup"><span data-stu-id="01f31-205">group by</span></span>          | <span data-ttu-id="01f31-206">このキーワードは、選択したレコードをフィールドごとにグループ化するようデータベースに指示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-206">This keyword instructs the database to group selected records by fields.</span></span> |
| <span data-ttu-id="01f31-207">指数</span><span class="sxs-lookup"><span data-stu-id="01f31-207">index</span></span>             | <span data-ttu-id="01f31-208">このキーワードは、インデックスで定義された方法で選択されたレコードをソートするようにデータベースに指示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-208">This keyword instructs the database to sort the selected records in the manner that is defined by the index.</span></span> |
| <span data-ttu-id="01f31-209">index hint</span><span class="sxs-lookup"><span data-stu-id="01f31-209">index hint</span></span>        | <span data-ttu-id="01f31-210">このキーワードは、インデックスで定義された方法で選択されたレコードをソートするために、データベースではインデックスを役立てます。</span><span class="sxs-lookup"><span data-stu-id="01f31-210">This keyword gives the database a hint to use this index to sort the selected records in the manner that is defined by the index.</span></span> <span data-ttu-id="01f31-211">データベースはヒントを無視できます。</span><span class="sxs-lookup"><span data-stu-id="01f31-211">The database can ignore the hint.</span></span> <span data-ttu-id="01f31-212">インデックス ヒントが正しくない場合はパフォーマンスに大きな影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="01f31-212">An incorrect index hint can greatly affect performance.</span></span> <span data-ttu-id="01f31-213">インデックス ヒントは、動的な **where** 句または **order by** 句がない SQL ステートメント、およびヒントの効果を確認できる SQL ステートメントにのみ適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-213">Index hints should be applied only to SQL statements that don't have dynamic **where** clauses or **order by** clauses, and where the effect of the hint can be verified.</span></span> |
| <span data-ttu-id="01f31-214">join</span><span class="sxs-lookup"><span data-stu-id="01f31-214">join</span></span>              | <span data-ttu-id="01f31-215">このキーワードは、両方のテーブルで共有される列のテーブルを結合するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-215">This keyword is used to join tables on a column that is shared by both tables.</span></span> <span data-ttu-id="01f31-216">結合基準は、**on** 節に指定されていないため、**where** 節に指定されています。</span><span class="sxs-lookup"><span data-stu-id="01f31-216">The join criteria are specified in a **where** clause, because there is no **on**.</span></span> <span data-ttu-id="01f31-217">このキーワードは、テーブルをループして関連テーブルのトランザクションを更新する場合に必要な SQL ステートメントの数を減らします。</span><span class="sxs-lookup"><span data-stu-id="01f31-217">This keyword reduces the number of SQL statements that are required if you want to loop through a table and update transactions in a related table.</span></span> <span data-ttu-id="01f31-218">たとえば、テーブル内の 500 のレコードを処理し、別のテーブルで関連するレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-218">For example, you process 500 records in a table and want to update related records in another table.</span></span> <span data-ttu-id="01f31-219">入れ子になった **while select** を使用する場合、データベースへの 501 トリップがあります。</span><span class="sxs-lookup"><span data-stu-id="01f31-219">If you use a nested **while select**, there will be 501 trips to the database.</span></span> <span data-ttu-id="01f31-220">ただし、**結合**を使用する場合、データベースへのトリップは 1 回だけになります。</span><span class="sxs-lookup"><span data-stu-id="01f31-220">However, if you use a **join**, there will be just one trip to the database.</span></span> |
| <span data-ttu-id="01f31-221">maxof</span><span class="sxs-lookup"><span data-stu-id="01f31-221">maxof</span></span>             | <span data-ttu-id="01f31-222">このキーワードはフィールドの最大値を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-222">This keyword returns the maximum of the fields.</span></span>  |
| <span data-ttu-id="01f31-223">minof</span><span class="sxs-lookup"><span data-stu-id="01f31-223">minof</span></span>             | <span data-ttu-id="01f31-224">このキーワードはフィールドの最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-224">This keyword returns the minimum of the fields.</span></span> |
| <span data-ttu-id="01f31-225">noFetch</span><span class="sxs-lookup"><span data-stu-id="01f31-225">noFetch</span></span>           | <span data-ttu-id="01f31-226">このキーワードは、今すぐレコードを取得する必要がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-226">This keyword indicates that no records should be fetched now.</span></span> <span data-ttu-id="01f31-227">このキーワードは通常、**select** 文の結果を、実際のフェッチを実行するクエリなどの別のアプリケーション オブジェクトに渡すときに使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-227">Typically, this keyword is used when the result of the **select** statement is passed on to another application object, such as a query that performs the actual fetch.</span></span> |
| <span data-ttu-id="01f31-228">notExists</span><span class="sxs-lookup"><span data-stu-id="01f31-228">notExists</span></span>         | <span data-ttu-id="01f31-229">転記がない場合にのみ、このキーワードが選択されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-229">This keyword is selected only if there are no posts.</span></span> |
| <span data-ttu-id="01f31-230">optimisticLock</span><span class="sxs-lookup"><span data-stu-id="01f31-230">optimisticLock</span></span>    | <span data-ttu-id="01f31-231">このキーワードは、テーブルに異なる値が設定されていても、オプティミスティック同時実行制御を使用してステートメントを実行させます。</span><span class="sxs-lookup"><span data-stu-id="01f31-231">This keyword forces a statement to run by using optimistic concurrency control, even if a different value is set on the table.</span></span> |
| <span data-ttu-id="01f31-232">order by</span><span class="sxs-lookup"><span data-stu-id="01f31-232">order by</span></span>          | <span data-ttu-id="01f31-233">このキーワードは、選択されたレコードを**順**リストのフィールドでソートするようデータベースに指示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-233">This keyword instructs the database to sort the selected records by the fields in the **order by** list.</span></span> |
| <span data-ttu-id="01f31-234">outer</span><span class="sxs-lookup"><span data-stu-id="01f31-234">outer</span></span>             | <span data-ttu-id="01f31-235">このキーワードは、2 番目に名前が付けられたテーブルに行が一致しない場合でも、最初に名前が付けられたテーブルからすべての行を戻します。</span><span class="sxs-lookup"><span data-stu-id="01f31-235">This keyword returns all rows from the table that is named first, even if rows have no match in the table that is named second.</span></span> <span data-ttu-id="01f31-236">**左**がなくても、この結合は左外部結合です。</span><span class="sxs-lookup"><span data-stu-id="01f31-236">This join is a left outer join, even though there is no **left**.</span></span> <span data-ttu-id="01f31-237">右外部結合はありません。</span><span class="sxs-lookup"><span data-stu-id="01f31-237">There is no right outer join.</span></span>  |
| <span data-ttu-id="01f31-238">pessimisticLock</span><span class="sxs-lookup"><span data-stu-id="01f31-238">pessimisticLock</span></span>   | <span data-ttu-id="01f31-239">このキーワードは、テーブルに異なる値が設定されていても、ペシミスティック同時実行制御を使用してステートメントを実行させます。</span><span class="sxs-lookup"><span data-stu-id="01f31-239">This keyword forces a statement to run by using pessimistic concurrency control, even if a different value is set on the table.</span></span>  |
| <span data-ttu-id="01f31-240">repeatableRead</span><span class="sxs-lookup"><span data-stu-id="01f31-240">repeatableRead</span></span>    | <span data-ttu-id="01f31-241">このキーワードは、他の取引が現在の取引内のロジックによって読み取られたデータを変更する前に、現在の取引を完了する必要があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="01f31-241">This keyword specifies that the current transaction must be completed before other transactions can modify data that has been read by logic inside the current transaction.</span></span> <span data-ttu-id="01f31-242">明示的なトランザクションは **ttsAbort** または最も外側の **ttsCommit** のいずれかで完了します。</span><span class="sxs-lookup"><span data-stu-id="01f31-242">An explicit transaction is completed at either **ttsAbort** or the outermost **ttsCommit**.</span></span> <span data-ttu-id="01f31-243">スタンドアロンの **select** 明細書では、トランザクション期間は **select** コマンドの期間です。</span><span class="sxs-lookup"><span data-stu-id="01f31-243">For a stand-alone **select** statement, the transaction duration is the duration of the **select** command.</span></span> <span data-ttu-id="01f31-244">ただし、このキーワードがコードに表示されない場合でも、データベースは時に、個々の**選択**ステートメントの **repeatableRead** と同等のものを実施します。</span><span class="sxs-lookup"><span data-stu-id="01f31-244">However, the database sometimes enforces the equivalent of **repeatableRead** in individual **select** statements, even if this keyword doesn't appear in your code.</span></span> <span data-ttu-id="01f31-245">(動作は、テーブルをスキャンするかどうかを決定するためにデータベースが使用する方法によって異なります。) 詳細については、基になるリレーショナル データベース製品のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f31-245">(The behavior depends on the method that the database uses to determine whether it should scan the tables.) For more information, see the documentation for the underlying relational database product.</span></span> |
| <span data-ttu-id="01f31-246">リバース</span><span class="sxs-lookup"><span data-stu-id="01f31-246">reverse</span></span>           | <span data-ttu-id="01f31-247">レコードが逆の順序で返されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-247">Records are returned in reverse order.</span></span>  |
| <span data-ttu-id="01f31-248">sum</span><span class="sxs-lookup"><span data-stu-id="01f31-248">sum</span></span>               | <span data-ttu-id="01f31-249">このキーワードはフィールドの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-249">This keyword returns the sum of the fields.</span></span> <span data-ttu-id="01f31-250">すべてのアカウント、注文明細行などの合計を計算するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="01f31-250">It can be used to sum all accounts, order lines, and so on.</span></span> |
| <span data-ttu-id="01f31-251">validTimeState</span><span class="sxs-lookup"><span data-stu-id="01f31-251">validTimeState</span></span>    | <span data-ttu-id="01f31-252">このキーワードは、**ValidTimeStateFieldType** プロパティが**なし**以外の値に設定されているテーブルの行をフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="01f31-252">This keyword filters rows from a table where the **ValidTimeStateFieldType** property is set to a value other than **None**.</span></span> |

#### <a name="keyword-examples"></a><span data-ttu-id="01f31-253">キーワードの例</span><span class="sxs-lookup"><span data-stu-id="01f31-253">Keyword examples</span></span>

```X++
// asc keyword example.
select * from custTable
    order by Name asc;

// avg keyword example. 
CustTable custTable;;
select avg(value) from custTable;
print custTable.value;

// count keyword example. 
CustTable xCT;int64 iCountRows; ;
Select COUNT(RecID) from xCT;
iCountRows = xCT.RecID;

// crossCompany keyword example.
CustTable custTable;
container conCompanies = ['dat','dmo'];
select crossCompany :conCompanies
    * from custTable;

// desc keyword example.
select * from custTable
    order by Name desc;

// exists keyword example. 
while select AccountNum, Name from custTable
    order by AccountNum
    exists join * from ctr
    where (ctr.AccountNum ==
        custTable.AccountNum)

// firstFast keyword example.
select firstFast custTable
    order by AccountNum;

// firstOnly keyword example.
static InventTable find(ItemIditemId, boolean update = false)
{
    InventTable inventTable;
    inventTable.selectForUpdate(update);
    if (itemId)
    {
        select firstonly inventTable
            index hint ItemIdx
            where inventTable.itemId == itemId;
    }
    return inventTable;
}

// forceNestedLoop keyword example.
while select forceSelectOrder
    forceNestedLoop inventTransThis
index hint TransIdIdx
where inventTransThis.InventTransId
    == inventTrans.InventTransId
    && inventTransThis.StatusIssue
    <= StatusIssue::ReservOrdered

// forcePlaceholders keyword example.
static void forcePlaceHoldersExample(Args _args){
    SalesTable salesTable;
    SalesLine salesLine;
    while select forcePlaceholders salesLine
        join salesTable
            where salesTable.SalesId ==
                salesLine.SalesId
                && salesTable.SalesId == '10'
    {
        //more code
    }
}

// forceSelectOrder keyword example.
display ForecastHasPurch hasForecastPurch(){
    ForecastPurch forecastPurch;
    InventDim nventDim;
select firstOnly forcePlaceholders
    forceSelectOrder recId
    from forecastPurch
    index hint ItemIdx
    where forecastPurch.itemId == this.itemId
exists join inventDim
    index hint DimIdIdx
    where inventDim.inventDimId == forecastPurch.inventDimId
        && inventDim.configId == this.configId;
    return forecastPurch.recId;
}

// forUpdate keyword example.
ttsBegin; while select forUpdate ledgerJournalTrans
    index hint NumVoucherIdx
    where ledgerJournalTrans.journalNum ==
    _journalNum &&
    ledgerJournalTrans.voucher == _voucher
{
    ledgerJournalTrans.doDelete();
    counter++;
}
if (counter
    && ledgerJournalTable.journalType
    != LedgerJournalType::Periodic)
{
    NumberSeq::release(
        ledgerJournalTable.voucherSeries,
        _voucher);
}
ttsCommit;

// group by keyword example.
CustTable custTable;;
while select sum(CreditMax) from custTable
    group by CustGroup
{
    print custTable.CustGroup, " ",custTable.CreditMax;
}

// index keyword example.
CustTable custTable;;
while select AccountNum, Name from custTable
    index AccountIdx
{
    print custTable.AccountNum, " ", custTable.Name;
}

// index hint keyword example.
while select forUpdate ledgerJournalTrans
    index hint NumVoucherIdx
    where ledgerJournalTrans.journalNum
        == _journalNum

// join keyword example.
while select ledgerTable
    join ledgerTrans
    where ledgerTrans.accountNum == ledgerTable.accountNum
{
    amountMST += ledgerTrans.amountMST;
}

// maxof keyword example.
CustTable custTable;;
select maxof(CreditMax) from custTable;

// minof keyword example.
CustTable custTable;;
select minof(CreditMax) from custTable;

// noFetch keyword example.
select noFetch custTable
    order by AccountNum

// notExists keyword example.
while select AccountNum, Name from custTable
    order by AccountNum
    notExists join * from ctr
    where (ctr.AccountNum ==
        custTable.AccountNum)

// optimisticLock keyword example.
select optimisticLock custTable
    where custTable.AccountNum > '1000'

// order by keyword example.
select * from custTable
    order by accountNum desc
    where custTable.AccountNum > "100";

// outer keyword example.
while select AccountNum
    from custTable
    order by AccountNum
    outer join * from custBankAccount
    where custBankAccount.AccountNum ==
        custTable.AccountNum
{
    print custTable.AccountNum,
    " , ", custBankAccount.DlvMode;
} 

// pessimisticLock keyword example.
select pessimisticLock custTable
    where custTable.AccountNum > '1000';

// reverse keyword example.
select reverse custTable
    order by AccountNum;

// sum keyword example.
CustTable custTable;;
select sum(CreditMax) from custTable;

// validTimeState keyword example.
static void VtsJob1(Args _args)
{
    // A validTimeState table.
    CustPackingSlipTransHistory xrec1;
    utcDateTime myDateFrom , myDateTo;
    anytype myAnytype = -1;
    myDateFrom = DateTimeUtil::utcNow();
    myDateTo = myDateFrom;
    SELECT
        validTimeState(myDateFrom, myDateTo)
            *
            FROM xrec1;
    myAnytype = xrec1.getFieldValue("RecId");
    info(myAnytype);
}
```

## <a name="select-statement-examples"></a><span data-ttu-id="01f31-254">select ステートメントの例</span><span class="sxs-lookup"><span data-stu-id="01f31-254">select statement examples</span></span>
<span data-ttu-id="01f31-255">次の例では、**select** ステートメントの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-255">The following examples show how you can use **select** statements.</span></span>

```X++
CustTable custTable;
// A customer is found and returned in custTable
select * from custTable;
info("A: " + custTable.AccountNum);

// A customer with account number > "100" is found
select * from custTable
    where custTable.AccountNum > "100";
info("B: " + custTable.AccountNum);

// Customer with the lowest account number > "100" found:
select *
    from custTable 
    order by accountNum
    where custTable.AccountNum > "100";
info("C1: " + custTable.AccountNum);

// The next customer is read
next custTable;
info("C2: " + custTable.AccountNum);

// Customer with highest account number
// (greater than 100) found: Fourth Coffee
select *
    from custTable 
    order by accountNum desc
    where custTable.accountNum > "100";
info("D1: " + custTable.AccountNum);

// The next record is read (DESC): Fabrikam, Inc.
next custTable;
info("D2: " + custTable.AccountNum);

// Customer with highest account number found: Fourth Coffee
select reverse custTable
    order by accountNum;
info("E: " + custTable.AccountNum);

// Customer with "lowest" name and account number
// in the interval 100 to 1000 is found. This is Coho Winery.
select *
    from custTable
    order by DlvMode
    where custTable.accountNum > "100"
        && custTable.accountNum < "1000";
info("F: " + custTable.AccountNum);

// The count select returns the number of customers.
select count(AccountNum)
    from custTable;

// Prints the result of the count
info(strFmt("G: %1 = Count of AccountNums", custTable.accountNum));

// Returns the average credit max for non-blocked customers.
select avg(CreditMax)
    from custTable
    where custTable.blocked == CustVendorBlocked::No;

// Prints the result of the avg
info(strFmt("H: %1 = Average CreditMax", custTable.CreditMax));

/*** Display from infolog:
Message (02:00:34 pm)
A: 4000
B: 4000
C1: 4000
C2: 4001
D1: 4507
D2: 4506
E: 4507
F: 
G: 29 = Count of AccountNums
H: 103.45 = Average CreditMax
***/
```

### <a name="join-example"></a><span data-ttu-id="01f31-256">join の例</span><span class="sxs-lookup"><span data-stu-id="01f31-256">join example</span></span>

<span data-ttu-id="01f31-257">次の例は、SQL **select** ステートメントの一部として内部結合を実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-257">The following example shows how an inner join can be performed as part of an SQL **select** statement.</span></span> <span data-ttu-id="01f31-258">この例では、**order by** 句も表示されており、各フィールドはテーブル名で修飾されています。</span><span class="sxs-lookup"><span data-stu-id="01f31-258">The example also shows an **order by** clause, where each field is qualified by a table name.</span></span> <span data-ttu-id="01f31-259">したがって、1 つの **order by** 句のみを使用して、取得したレコードのソート方法を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-259">Therefore, you can use just one **order by** clause to control how the retrieved records are sorted.</span></span>

```X++
CustTable xrecCustTable;
CashDisc xrecCashDisc;
struct sut4;
sut4 = new struct("str AccountNum; str CashDisc; str Description");
while select firstOnly10 *
    from xrecCustTable
    order by xrecCashDisc.Description
    join xrecCashDisc
    where xrecCustTable.CashDisc ==
        xrecCashDisc.CashDiscCode
        && xrecCashDisc.Description LIKE "*Days*"
    {
        sut4.value("AccountNum", xrecCustTable.AccountNum );
        sut4.value("CashDisc", xrecCashDisc.CashDiscCode );
        sut4.value("Description", xrecCashDisc.Description );
        info(sut4.toString());
    }
/*********  Actual Infolog output
Message (02:29:37 pm)
(AccountNum:"1101"; CashDisc:"0.5%D10"; Description:"0.5% 10 days")
(AccountNum:"4001"; CashDisc:"0.5%D10"; Description:"0.5% 10 days")
(AccountNum:"1102"; CashDisc:"0.5%D30"; Description:"0.5% 30 days")
(AccountNum:"1201"; CashDisc:"0.5%D30"; Description:"0.5% 30 days")
(AccountNum:"2211"; CashDisc:"0.5%D30"; Description:"0.5% 30 days")
(AccountNum:"1202"; CashDisc:"1%D15"; Description:"1% 15 days")
(AccountNum:"1203"; CashDisc:"1%D07"; Description:"1% 7 days")
(AccountNum:"2212"; CashDisc:"1%D07"; Description:"1% 7 days")
(AccountNum:"2213"; CashDisc:"1%D07"; Description:"1% 7 days")
(AccountNum:"2214"; CashDisc:"1%D07"; Description:"1% 7 days")
*********/
}
```

### <a name="group-by-and-order-by-example"></a><span data-ttu-id="01f31-260">group by および order by の例</span><span class="sxs-lookup"><span data-stu-id="01f31-260">group by and order by example</span></span>

<span data-ttu-id="01f31-261">次の例は、**group by** 句のフィールドをテーブル名で修飾できることを示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-261">The following example shows that the fields in the **group by** clause can be qualified by a table name.</span></span> <span data-ttu-id="01f31-262">複数の **group by** 句が存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-262">There can be multiple **group by** clauses.</span></span> <span data-ttu-id="01f31-263">ただし、フィールドは 1 つの **group by** 句のみのテーブル名により限定されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-263">However, the fields can be qualified by a table name in only one **group by** clause.</span></span> <span data-ttu-id="01f31-264">テーブル名の修飾子を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="01f31-264">We recommend that you use table name qualifiers.</span></span> <span data-ttu-id="01f31-265">**order by** 句は、**group by** と同じ構文パターンに従います。</span><span class="sxs-lookup"><span data-stu-id="01f31-265">The **order by** clause follows the same syntax patterns as **group by**.</span></span> <span data-ttu-id="01f31-266">両方の句が提供されている場合は、**join** (または **from**) 句の後に表示する必要があり、両方とも同じ **join** 句に存在する **where** 句よりも前にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-266">Both clauses, if they are provided, must appear after the **join** (or **from**) clause, and both must appear before any **where** clause that exists on the same **join** clause.</span></span> <span data-ttu-id="01f31-267">すべての **group by**、**order by**、および**where** の各句を、最後の **join** 句のすぐ後に表示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="01f31-267">We recommend that all **group by**, **order by**, and **where** clauses appear immediately after the last **join** clause.</span></span>

```X++
CustTable xrecCustTable;
CashDisc xrecCashDisc;
struct sut4;
sut4 = new struct("str AccountNum_Count; str CashDisc; str Description");
while select count(AccountNum)
    from xrecCustTable
    order by xrecCashDisc.Description
    join xrecCashDisc
        group by xrecCashDisc.CashDiscCode
            where xrecCustTable.CashDisc ==
                xrecCashDisc.CashDiscCode
                && xrecCashDisc.Description LIKE "*Days*"
    {
        sut4.value("AccountNum_Count", xrecCustTable.AccountNum );
        sut4.value("CashDisc", xrecCashDisc.CashDiscCode );
        sut4.value("Description", xrecCashDisc.Description );
        info(sut4.toString());
    }
/*********  Actual Infolog output
Message (02:45:26 pm)
(AccountNum_Count:"2"; CashDisc:"0.5%D10"; Description:"")
(AccountNum_Count:"3"; CashDisc:"0.5%D30"; Description:"")
(AccountNum_Count:"4"; CashDisc:"1%D07"; Description:"")
(AccountNum_Count:"1"; CashDisc:"1%D15"; Description:"")
(AccountNum_Count:"1"; CashDisc:"2%D30"; Description:"")
(AccountNum_Count:"1"; CashDisc:"3%D10"; Description:"")
*********/
}
```

### <a name="select-statement-that-has-an-outer-join"></a><span data-ttu-id="01f31-268">外部結合を持つ select ステートメント</span><span class="sxs-lookup"><span data-stu-id="01f31-268">select statement that has an outer join</span></span>

<span data-ttu-id="01f31-269">**select** ステートメントは、**where** 句において外部結合のフィルター処理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="01f31-269">The **select** statement supports filtering an outer join in the **where** clause.</span></span> <span data-ttu-id="01f31-270">標準 SQL の **join** 句には、フィルター基準の **on** キーワードがあります。</span><span class="sxs-lookup"><span data-stu-id="01f31-270">In the **join** clause of standard SQL, there is an **on** keyword for filter criteria.</span></span> <span data-ttu-id="01f31-271">ただし、このキーワードは X++ でサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="01f31-271">However, this keyword isn't supported in X++.</span></span> <span data-ttu-id="01f31-272">内部結合は、その他の連結テーブルの行に一致しないすべてのテーブル行を拒否します。</span><span class="sxs-lookup"><span data-stu-id="01f31-272">An inner join rejects all table rows that don't match a row in the other joined table.</span></span> <span data-ttu-id="01f31-273">ただし、他の連結テーブルに一致する行がない場合でも、外部結合には最初のテーブルからの行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="01f31-273">However, an outer join includes rows from the first table, even if there is no matching row in the other joined table.</span></span> <span data-ttu-id="01f31-274">既定値は、他の結合テーブルの一致する行から取得できなかったデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="01f31-274">Default values are substituted for the data that couldn't be obtained from a matching row in the other joined table.</span></span> <span data-ttu-id="01f31-275">**join** 句の一部である **on** 句に相当する、outer join をフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-275">You can filter an outer join at the equivalent of an **on** clause that is part of the **join** clause.</span></span> <span data-ttu-id="01f31-276">内部結合については、**on** 句でフィルター処理する場合の動作は **where** 句でフィルター処理する場合の動作と同じです。</span><span class="sxs-lookup"><span data-stu-id="01f31-276">For an inner join, the behavior if you filter on an **on** clause is the same as the behavior if you filter on the **where** clause.</span></span>

#### <a name="select-statement-example"></a><span data-ttu-id="01f31-277">select ステートメントの例</span><span class="sxs-lookup"><span data-stu-id="01f31-277">select statement example</span></span>

<span data-ttu-id="01f31-278">次の例は、2 つのテーブルに基づいています。</span><span class="sxs-lookup"><span data-stu-id="01f31-278">The following example is based on two tables.</span></span> <span data-ttu-id="01f31-279">フィールド タイプとサンプル データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="01f31-279">The field types and example data are included.</span></span> <span data-ttu-id="01f31-280">SalesOrder 親テーブルと SalesOrderLine 子テーブルの間には、一対多の関係があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-280">There is a one-to-many relationship between the SalesOrder parent table and the SalesOrderLine child table.</span></span> <span data-ttu-id="01f31-281">SalesOrder テーブルの各行に対して、 SalesOrderLine テーブルには 0 (ゼロ) またはそれ以上の行があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-281">For each row in the SalesOrder table, there are 0 (zero) or more rows in the SalesOrderLine table.</span></span> <span data-ttu-id="01f31-282">SalesOrder テーブルには 2 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-282">There are two rows in the SalesOrder table.</span></span>

| <span data-ttu-id="01f31-283">SalesOrderID (整数、主キー)</span><span class="sxs-lookup"><span data-stu-id="01f31-283">SalesOrderID (integer, primary key)</span></span> | <span data-ttu-id="01f31-284">DateAdded (日付)</span><span class="sxs-lookup"><span data-stu-id="01f31-284">DateAdded (date)</span></span> |
|-------------------------------------|------------------|
| <span data-ttu-id="01f31-285">1</span><span class="sxs-lookup"><span data-stu-id="01f31-285">1</span></span>                                   | <span data-ttu-id="01f31-286">2010-01-01</span><span class="sxs-lookup"><span data-stu-id="01f31-286">2010-01-01</span></span>       |
| <span data-ttu-id="01f31-287">2</span><span class="sxs-lookup"><span data-stu-id="01f31-287">2</span></span>                                   | <span data-ttu-id="01f31-288">2010-02-02</span><span class="sxs-lookup"><span data-stu-id="01f31-288">2010-02-02</span></span>       |

<span data-ttu-id="01f31-289">SalesOrderLine テーブルには、**SalesOrderID** という名前の外部キー フィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="01f31-289">The SalesOrderLine table contains a foreign key field that is named **SalesOrderID**.</span></span> <span data-ttu-id="01f31-290">このフィールドは、SalesOrder テーブルの主キー列を参照します。</span><span class="sxs-lookup"><span data-stu-id="01f31-290">This field references the primary key column of the SalesOrder table.</span></span> <span data-ttu-id="01f31-291">**2** の **SalesOrderID** 値は、SalesOrderLine テーブルのデータには発生しません。</span><span class="sxs-lookup"><span data-stu-id="01f31-291">A **SalesOrderID** value of **2** doesn't occur in the data for the SalesOrderLine table.</span></span>

| <span data-ttu-id="01f31-292">SalesOrderLineID (文字列、主キー)</span><span class="sxs-lookup"><span data-stu-id="01f31-292">SalesOrderLineID (string, primary key)</span></span> | <span data-ttu-id="01f31-293">数量 (整数)</span><span class="sxs-lookup"><span data-stu-id="01f31-293">Quantity (integer)</span></span> | <span data-ttu-id="01f31-294">SalesOrderID (整数、外部キー)</span><span class="sxs-lookup"><span data-stu-id="01f31-294">SalesOrderID (integer, foreign key)</span></span> |
|----------------------------------------|--------------------|-------------------------------------|
| <span data-ttu-id="01f31-295">AA</span><span class="sxs-lookup"><span data-stu-id="01f31-295">AA</span></span>                                     | <span data-ttu-id="01f31-296">32</span><span class="sxs-lookup"><span data-stu-id="01f31-296">32</span></span>                 | <span data-ttu-id="01f31-297">1</span><span class="sxs-lookup"><span data-stu-id="01f31-297">1</span></span>                                   |
| <span data-ttu-id="01f31-298">BB</span><span class="sxs-lookup"><span data-stu-id="01f31-298">BB</span></span>                                     | <span data-ttu-id="01f31-299">67</span><span class="sxs-lookup"><span data-stu-id="01f31-299">67</span></span>                 | <span data-ttu-id="01f31-300">1</span><span class="sxs-lookup"><span data-stu-id="01f31-300">1</span></span>                                   |
| <span data-ttu-id="01f31-301">CC</span><span class="sxs-lookup"><span data-stu-id="01f31-301">CC</span></span>                                     | <span data-ttu-id="01f31-302">66</span><span class="sxs-lookup"><span data-stu-id="01f31-302">66</span></span>                 | <span data-ttu-id="01f31-303">1</span><span class="sxs-lookup"><span data-stu-id="01f31-303">1</span></span>                                   |

<span data-ttu-id="01f31-304">次のコードでは、**select** ステートメントで 2 つのテーブルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="01f31-304">The following code has a **select** statement that reads the two tables.</span></span> <span data-ttu-id="01f31-305">**select** ステートメントには、左の **outer join** 句が含まれています。</span><span class="sxs-lookup"><span data-stu-id="01f31-305">The **select** statement includes a left **outer join** clause.</span></span> <span data-ttu-id="01f31-306">結合基準とデータ フィルターは両方とも **where** 句にあります。</span><span class="sxs-lookup"><span data-stu-id="01f31-306">Both the join criteria and the data filter are on the **where** clause.</span></span> <span data-ttu-id="01f31-307">コードからの出力も表示されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-307">The output from the code is also shown.</span></span> <span data-ttu-id="01f31-308">出力の 2 番目のレコードには、値が **2** の **SalesOrderID** があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-308">The second record in the output has a **SalesOrderID** value of **2**.</span></span> <span data-ttu-id="01f31-309">ただし、その値は SalesOrderLine テーブルに存在しません。</span><span class="sxs-lookup"><span data-stu-id="01f31-309">However, that value isn't present in the SalesOrderLine table.</span></span> <span data-ttu-id="01f31-310">したがって、2 番目のレコードのフィールドの一部には、整数の場合は **0**、文字列の場合は長さゼロの文字列が既定値となります。</span><span class="sxs-lookup"><span data-stu-id="01f31-310">Therefore, some of the fields in the second record have default values: **0** for an integer and a zero-length string for a string.</span></span>

```X++
static void SelectOuterJoinExample(Args _args)
{
    SalesOrder recSalesOrder;
    SalesOrderLine recSalesOrderLine;
    struct struct4;

    struct4 = new struct
        ("int SalesOrderID;"
        + "date DateAdded;"
        + "str SalesOrderLineID;"
        + "int Quantity"
        );
    while
    select
        *
        from
            recSalesOrder
            OUTER JOIN recSalesOrderLine
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
}
/*********  Actual Infolog output (with break spaces entered in between each output)
(SalesOrderID:1;
DateAdded:2010/1/1;
SalesOrderLineID:"CC";
Quantity:66)
(SalesOrderID:2;
DateAdded:2010/2/2;
SalesOrderLineID:"";
Quantity:0)
*********/
```

## <a name="while-select-statements"></a><span data-ttu-id="01f31-311">while select ステートメント</span><span class="sxs-lookup"><span data-stu-id="01f31-311">while select statements</span></span>
<span data-ttu-id="01f31-312">**while select** ステートメントは、データの処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-312">A **while select** statement is used to handle data.</span></span> <span data-ttu-id="01f31-313">**select** ステートメントの最も広く使用されている形式です。</span><span class="sxs-lookup"><span data-stu-id="01f31-313">It's the most widely used form of the **select** statement.</span></span> <span data-ttu-id="01f31-314">**while select** ステートメントは、特定の基準を満たす多くのレコードをループし、各レコードでステートメントを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-314">The **while select** statement loops over many records that meet specific criteria, and can run a statement on each record.</span></span> <span data-ttu-id="01f31-315">通常、データ操作のために **while select** 文を使用する場合、トランザクション内でデータ整合性を確保するために使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-315">Typically, when you use the **while select** statement for data manipulation, you do it in a transaction to ensure data integrity.</span></span> <span data-ttu-id="01f31-316">**while select** ステートメントの結果はテーブル バッファ変数に返されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-316">The results of a **while select** statement are returned in a table buffer variable.</span></span> <span data-ttu-id="01f31-317">**選択**ステートメントのフィールド リストを使用すると、これらのフィールドでは、テーブル変数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-317">If you use a field list in the **select** statement, only those fields are available in the table variable.</span></span> <span data-ttu-id="01f31-318">**sum** や **count** などの集計関数を使用すると、結果は **sum** または **count** を実行するフィールドに返されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-318">If you use aggregate functions, such as **sum** or **count**, the results are returned in the fields that you perform the **sum** or **count** over.</span></span> <span data-ttu-id="01f31-319">整数フィールドおよび実数フィールのみを計算、平均、または合計することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-319">You can count, average, or sum only integer and real fields.</span></span> <span data-ttu-id="01f31-320">**while select** ステートメントの構文は、**select** ステートメントの構文に似ていますが、このステートメントは**select** ではなく **while select** により処理されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-320">The syntax of a **while select** statement resembles the syntax of a **select** statement, but the statement is preceded by **while select** instead of **select**.</span></span> <span data-ttu-id="01f31-321">**select** ステートメント自体は、ループのステートメントの最初の繰り返しの直前に 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-321">The **select** statement itself is run only one time, immediately before the first iteration of the statements in the loop.</span></span> <span data-ttu-id="01f31-322">**while select** に追加されたブール式 (**iCounter &lt; 1** など) は 1 度だけテストされます。</span><span class="sxs-lookup"><span data-stu-id="01f31-322">Any Boolean expressions (such as **iCounter &lt; 1**) that are added to the **while select** are tested only one time.</span></span> <span data-ttu-id="01f31-323">この動作は、C ++ や C\# などの言語の **while** 文の動作とは異なります。</span><span class="sxs-lookup"><span data-stu-id="01f31-323">This behavior differs from the behavior of the **while** statement in languages such as C++ and C\#.</span></span> <span data-ttu-id="01f31-324">たとえば、次のループは、複数回繰り返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-324">For example, the following loop can have more than one iteration.</span></span>

```X++
static void JobWhileSelect(Args _args)
{
    int iCounter = 0;
    BankAccountTable xrecBAT;
    while select * from xrecBAT
        where iCounter < 1
    {
        iCounter++;
        Global::info(strFmt("%1 , %2", iCounter, xrecBAT.AccountID));
    }
}

/*** Display from infolog:
Message (04:59:38 pm)
1 , Cash1
2 , STB-DKK
3 , STB-EUR
***/
```

### <a name="while-select-example"></a><span data-ttu-id="01f31-325">while select の例</span><span class="sxs-lookup"><span data-stu-id="01f31-325">while select example</span></span>

<span data-ttu-id="01f31-326">次の例では、アカウント番号が指定された範囲内にある CustTable テーブルのすべての顧客のアカウント番号と売上グループを出力します。</span><span class="sxs-lookup"><span data-stu-id="01f31-326">The following example prints the account number and sales group of every customer in the CustTable table whose account number is within a specified range.</span></span>

```X++
static void JobPrintTel(Args _args)
{
    CustTable xrecCT;
    while select xrecCT
        order by xrecCT.AccountNum
            where  xrecCT.AccountNum >= "4010"
                && xrecCT.AccountNum <= "4100"
    {
        Global::info(strFmt("%1 , %2",
            xrecCT.AccountNum, xrecCT.SalesGroup));
    }
}

/*** Display from Infolog:
Message (06:04:03 pm)
4010 , CSG-EU
4011 , CSG-EU
4012 , CSG-OTH
4013 , CSG-OTH
4014 , CSG-OTH
4015 , CSG-OTH
4016 , CSG-EU
4017 , CSG-EU
4018 , CSG-EU
4020 , 
4024 , 
***/
```

### <a name="while-select-example"></a><span data-ttu-id="01f31-327">while select の例</span><span class="sxs-lookup"><span data-stu-id="01f31-327">while select example</span></span>

<span data-ttu-id="01f31-328">次の例では、**forUpdate** キーワードを使用しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-328">The following example uses the **forUpdate** keyword.</span></span>

```X++
static void LedgerJob(Args _args)
{
    LedgerJournalTrans ledgerJournalTrans;
    LedgerJournalTable ledgerJournalTable;
    LedgerJournalId    jnJournalNum;
    Voucher            vVoucher;
    Counter            counter = 0;
    jnJournalNum = "999999_999"; //"000012_003";
    vVoucher = "88888_888"; //"00001_IRG";
    ledgerJournalTable =
        ledgerJournalTable::find(jnJournalNum);
    ttsBegin;
    while select forUpdate ledgerJournalTrans
        index hint NumVoucherIdx
            where ledgerJournalTrans.journalNum == jnJournalNum
                && ledgerJournalTrans.voucher == vVoucher
    {
        ledgerJournalTrans.doDelete();
        counter++;
    }
    //NumberSeq updates needed?
    ttsCommit;
    Global::info(strFmt("counter = %1", counter));
}
```

### <a name="deleting-a-set-of-records"></a><span data-ttu-id="01f31-329">レコードのセットを削除します</span><span class="sxs-lookup"><span data-stu-id="01f31-329">Deleting a set of records</span></span>

<span data-ttu-id="01f31-330">**while select** ステートメントを使用して一部の基準を満たすレコードのセットを確認し、各レコードでアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-330">You can use a **while select** statement to loop over a set of records that meet some criteria, and perform an action on each record.</span></span> <span data-ttu-id="01f31-331">次の例では、ステートメントを使用して一連のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="01f31-331">In the following example, the statement is used to delete a set of records.</span></span>

```X++
TableName myXrec;
while select myXrec where conditions // conditions is a Boolean variable defined elsewhere.
{
    myXrec.delete();
}
```

<span data-ttu-id="01f31-332">同じ効果は **delete\_from** キーワードを使用して達成することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-332">You can achieve the same effect by using the **delete\_from** keyword.</span></span>

```X++
TableName myXrec;
delete_from myXrec where conditions; // conditions is a Boolean variable defined elsewhere.
```

### <a name="select-statements-on-fields"></a><span data-ttu-id="01f31-333">フィールド上の select ステートメント</span><span class="sxs-lookup"><span data-stu-id="01f31-333">select statements on fields</span></span>

<span data-ttu-id="01f31-334">**select** ステートメントをフィールド上のルックアップで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-334">You can use a **select** statement in a lookup on a field.</span></span> <span data-ttu-id="01f31-335">テーブルのレコードをフェッチする**選択**ステートメントの後、**.fieldName** を入力してテーブルのフィールドを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-335">After a **select** statement that fetches a record in a table, you can enter **.fieldName** to reference a field in the table.</span></span> <span data-ttu-id="01f31-336">これらの **select** ステートメントは、式で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-336">These **select** statements must be used in expressions.</span></span> <span data-ttu-id="01f31-337">*通常の **select** ステートメント* は *フィールド **select** ステートメント* と異なります:</span><span class="sxs-lookup"><span data-stu-id="01f31-337">A *normal **select** statement* differs from a *field **select** statement*:</span></span>

-   <span data-ttu-id="01f31-338">フィールド **select** ステートメントはテーブル上で直接動作します。</span><span class="sxs-lookup"><span data-stu-id="01f31-338">The field **select** statement operates directly on a table.</span></span>
-   <span data-ttu-id="01f31-339">通常の **select** ステートメントは、テーブル バッファ変数で動作します。</span><span class="sxs-lookup"><span data-stu-id="01f31-339">The normal **select** statement operates on a table buffer variable.</span></span>

### <a name="select-field-example"></a><span data-ttu-id="01f31-340">フィールド例を選択</span><span class="sxs-lookup"><span data-stu-id="01f31-340">select field example</span></span>

```X++
void selectFieldExamples ()
{
    // Prints the NameRef field from the selected customer
    print (select CustTable order by AccountStatement).AccountStatement;

    // Uses the balance field from the customer with AccountNum 3000
    if ((select custTable where CustTable.AccountNum == '3000').CreditMax < 50000)
        print "This customer has a credit maximum less than $50,000.";
}
```

### <a name="aggregate-functions-differences-between-x-and-sql"></a><span data-ttu-id="01f31-341">集計関数: X++ および SQL の差額</span><span class="sxs-lookup"><span data-stu-id="01f31-341">Aggregate functions: Differences between X++ and SQL</span></span>

<span data-ttu-id="01f31-342">業界標準の SQL では、データベース クエリに*集計関数*を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-342">In industry-standard SQL, a database query can contain *aggregate functions*.</span></span> <span data-ttu-id="01f31-343">例では、**count(RecID)** および **sum(columnA)** があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-343">Examples include **count(RecID)** and **sum(columnA)**.</span></span> <span data-ttu-id="01f31-344">集計関数が使用されるが、どの行も **WHERE** 句と一致しないときは、行は、集計の結果を保持するために行を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-344">When an aggregate function is used, but no rows match the **where** clause, a row must be returned to hold the result of the aggregates.</span></span> <span data-ttu-id="01f31-345">返された行では、**count** 関数には **0** (ゼロ)、**sum** 関数には **null** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-345">The row that is returned shows the value **0** (zero) for the **count** function and **null** for the **sum** function.</span></span> <span data-ttu-id="01f31-346">X++ はデータベースの **null** 値の概念をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="01f31-346">X++ doesn't support the concept of **null** values for the database.</span></span> <span data-ttu-id="01f31-347">したがって、**sum** 関数が **null** を返す場合、行はユーザーに返されません。</span><span class="sxs-lookup"><span data-stu-id="01f31-347">Therefore, in cases where the **sum** function will return **null**, no row is returned to the user.</span></span> <span data-ttu-id="01f31-348">また、すべてのデータ型は、状況によっては **null** 値として処理される特定の値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="01f31-348">Additionally, every data type has a specific value that is treated as a **null** value in some circumstances.</span></span>

### <a name="index-and-order-by-keywords-in-select-statements"></a><span data-ttu-id="01f31-349">select ステートメント内の index および order by キーワード</span><span class="sxs-lookup"><span data-stu-id="01f31-349">index and order by keywords in select statements</span></span>

<span data-ttu-id="01f31-350">返されるデータを並べ替えるには、**select** ステートメントで **order by** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-350">You use the **order by** keyword in **select** statements to order the data that is returned.</span></span> <span data-ttu-id="01f31-351">**index hint** キーワードを使用して、クエリで使用するインデックスを指定し、インデックスで定義された方法で選択したレコードをソートします。</span><span class="sxs-lookup"><span data-stu-id="01f31-351">Use the **index hint** keyword to specify the index that should be used in the query and to sort the selected records in the manner that is defined by the index.</span></span> <span data-ttu-id="01f31-352">インデックスは、レコードの選択を最適化します。</span><span class="sxs-lookup"><span data-stu-id="01f31-352">Indexes optimize the selection of records.</span></span> <span data-ttu-id="01f31-353">特定の順序でレコードを選択するには、**インデックス ヒント**キーワードを**並べ替え**の式と組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="01f31-353">To select records in a specific order, combine the **index hint** keyword with an **order by** expression.</span></span> <span data-ttu-id="01f31-354">出力を逆順に並べ替えるには、**逆**キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-354">If you want the output to be sorted in reverse order, use the **reverse** keyword.</span></span> <span data-ttu-id="01f31-355">テーブルのインデックスが無効になっている場合 (インデックスの**有効**プロパティが**いいえ**に設定されている場合)、索引を参照する**選択**ステートメントは引き続き有効です。</span><span class="sxs-lookup"><span data-stu-id="01f31-355">If a table index has been disabled (that is, if the index's **Enabled** property is set to **No**), the **select** statement that references the index is still valid.</span></span> <span data-ttu-id="01f31-356">ただし、インデックスがデータベースに存在しないため、データベースはデータを並べ替えるヒントとしてインデックスを使用できません。</span><span class="sxs-lookup"><span data-stu-id="01f31-356">However, the database can't use the index as a hint to sort the data, because the index doesn't exist in the database.</span></span> <span data-ttu-id="01f31-357">次のテーブルは、**select** ステートメントで **index hint** および **order by** キーワードを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-357">The following table shows how to use the **index hint** and **order by** keywords in **select** statements.</span></span>

| <span data-ttu-id="01f31-358">タスク</span><span class="sxs-lookup"><span data-stu-id="01f31-358">Task</span></span>                                                                                 | <span data-ttu-id="01f31-359">使用</span><span class="sxs-lookup"><span data-stu-id="01f31-359">Use</span></span>                                   |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="01f31-360">注文が重要でない場合は、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="01f31-360">Select records when the order isn't significant.</span></span>                                     | <span data-ttu-id="01f31-361">select ..</span><span class="sxs-lookup"><span data-stu-id="01f31-361">select ..</span></span> <span data-ttu-id="01f31-362">where ...</span><span class="sxs-lookup"><span data-stu-id="01f31-362">where ...</span></span>                   |
| <span data-ttu-id="01f31-363">注文が重要な場合は、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="01f31-363">Select records when the order is significant.</span></span>                                        | <span data-ttu-id="01f31-364">select ..</span><span class="sxs-lookup"><span data-stu-id="01f31-364">select ..</span></span> <span data-ttu-id="01f31-365">order by ... where ...</span><span class="sxs-lookup"><span data-stu-id="01f31-365">order by ... where ...</span></span>      |
| <span data-ttu-id="01f31-366">レコードを選択し、特定のインデックスを強制的に使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-366">Select records, and force a specific index to be used.</span></span>                               | <span data-ttu-id="01f31-367">select ..</span><span class="sxs-lookup"><span data-stu-id="01f31-367">select ..</span></span> <span data-ttu-id="01f31-368">index hint ... where ...</span><span class="sxs-lookup"><span data-stu-id="01f31-368">index hint ... where ...</span></span>    |
| <span data-ttu-id="01f31-369">注文が重要な場合は、レコードを選択し、特定のインデックスを強制的に使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-369">Select records when the order is significant, and force a specific index to be used.</span></span> | <span data-ttu-id="01f31-370">select ..</span><span class="sxs-lookup"><span data-stu-id="01f31-370">select ..</span></span> <span data-ttu-id="01f31-371">index hint ... order by ... where ...</span><span class="sxs-lookup"><span data-stu-id="01f31-371">index hint ... order by ... where ...</span></span> |

### <a name="index-and-order-by-example"></a><span data-ttu-id="01f31-372">index および order by の例</span><span class="sxs-lookup"><span data-stu-id="01f31-372">index and order by example</span></span>

<span data-ttu-id="01f31-373">次の例は、顧客の範囲と期日に基づいて、SalesTable テーブルからトランザクションを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-373">The following example shows how to select transactions from the SalesTable table, based on a range of customers and due dates.</span></span>

```X++
SalesTable salesTable;
    select salesTable
    index hint CustIdx
    order by CustAccount
    where salesTable.CustAccount >= '3000'
        && salesTable.CustAccount <= '4000'
        && salesTable.FixedDueDate >= 12\12\2004
        && salesTable.FixedDueDate <= 05\05\2009;
```

### <a name="index-hint"></a><span data-ttu-id="01f31-374">index hint</span><span class="sxs-lookup"><span data-stu-id="01f31-374">index hint</span></span>

<span data-ttu-id="01f31-375">クエリの**インデックス ヒント**を使用する前に、サーバー上で使用できるヒントを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-375">Before you can use **index hint** in queries, you must specify that hints can be used on the server.</span></span>

1.  <span data-ttu-id="01f31-376">**スタート**&gt; **管理ツール** &gt; **Microsoft Dynamics AX サーバー コンフィギュレーション**に移動します。</span><span class="sxs-lookup"><span data-stu-id="01f31-376">Go to **Start** &gt; **Administrative Tools** &gt; **Microsoft Dynamics AX Server Configuration**.</span></span>
2.  <span data-ttu-id="01f31-377">**データベースのチューニング** タブで、**クエリで INDEX のヒントを許可する** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01f31-377">On the **Database Tuning** tab, select **Allow INDEX hints in queries**, and then click **OK**.</span></span>
3.  <span data-ttu-id="01f31-378">Application Object Server (AOS) サービスの再起動を要求するメッセージ ボックスが表示されたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01f31-378">When a message box prompts you to restart the Application Object Server (AOS) service, click **Yes**.</span></span> <span data-ttu-id="01f31-379">サービスが再起動されるまで、インデックス ヒントは有効化されません。</span><span class="sxs-lookup"><span data-stu-id="01f31-379">Index hints won't be enabled until the service is restarted.</span></span>

<span data-ttu-id="01f31-380">**SELECT** ステートメント内の **インデックス ヒント** が非クラスター化インデックスを参照し、**WHERE** 句に同じテーブルのクラスタ化インデックスに存在するフィールドのみが含まれているときは、ヒントで指定されているインデックスではなく、クラスタ化インデックスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-380">When an **index hint** in a **select** statement refers to a non-clustered index, and the **where** clause contains only the fields that are found in a clustered index on the same table, the clustered index is used instead of the index that is specified in the hint.</span></span> <span data-ttu-id="01f31-381">たとえば、SQL Server Management Studio で **sp\_helpindex InventTable** を実行し、InventTable テーブルが **DataAreaId** および **ItemId** 列でクラスター インデックスを、さらに **DataAreaId**、**ItemProductId**、および **ItemType** 列で非クラスター化インデックスを持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="01f31-381">For example, you run **sp\_helpindex InventTable** in SQL Server Management Studio and you see that the InventTable table has a clustered index on the **DataAreaId** and **ItemId** columns, and a non-clustered index on the **DataAreaId**, **ItemProductId**, and **ItemType** columns.</span></span>

| <span data-ttu-id="01f31-382">インデックス名</span><span class="sxs-lookup"><span data-stu-id="01f31-382">Index name</span></span>       | <span data-ttu-id="01f31-383">説明</span><span class="sxs-lookup"><span data-stu-id="01f31-383">Description</span></span>                                        | <span data-ttu-id="01f31-384">キーの列</span><span class="sxs-lookup"><span data-stu-id="01f31-384">Key columns</span></span>                         |
|------------------|----------------------------------------------------|-------------------------------------|
| <span data-ttu-id="01f31-385">I\_175ITEMIDX</span><span class="sxs-lookup"><span data-stu-id="01f31-385">I\_175ITEMIDX</span></span>    | <span data-ttu-id="01f31-386">プライマリにあるクラスタ化された一意の主キー</span><span class="sxs-lookup"><span data-stu-id="01f31-386">Clustered, unique, primary key, located on PRIMARY</span></span> | <span data-ttu-id="01f31-387">DATAAREAID、ITEMID</span><span class="sxs-lookup"><span data-stu-id="01f31-387">DATAAREAID, ITEMID</span></span>                  |
| <span data-ttu-id="01f31-388">I\_175PRODUCTIDX</span><span class="sxs-lookup"><span data-stu-id="01f31-388">I\_175PRODUCTIDX</span></span> | <span data-ttu-id="01f31-389">非集合、プライマリに配置</span><span class="sxs-lookup"><span data-stu-id="01f31-389">Non-clustered, located on PRIMARY</span></span>                  | <span data-ttu-id="01f31-390">DATAAREAID、ITEMPRODUCTID、ITEMTYPE</span><span class="sxs-lookup"><span data-stu-id="01f31-390">DATAAREAID, ITEMPRODUCTID, ITEMTYPE</span></span> |

<span data-ttu-id="01f31-391">次のコードでは、**インデックス ヒント**で指定される非クラスター化インデックスではなく、クラスター化インデックスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-391">In the following code, the clustered index is used instead of the non-clustered index that is specified by **index hint**.</span></span>

```X++
static void IndexHint(Args _args)
{
    InventTable inv;
    select * from inv index hint GroupItemIdx
        where inv.ItemId == 'B-R14';
}
```

### <a name="writing-a-select-statement-as-an-expression"></a><span data-ttu-id="01f31-392">選択したステートメントを式として記述</span><span class="sxs-lookup"><span data-stu-id="01f31-392">Writing a select statement as an expression</span></span>

<span data-ttu-id="01f31-393">**select** ステートメントを式として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-393">You can use a **select** statement as an expression.</span></span> <span data-ttu-id="01f31-394">このタイプの **select** ステートメントは *式 **select** ステートメント* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="01f31-394">This type of **select** statement is known as an *expression **select** statement*.</span></span> <span data-ttu-id="01f31-395">テーブル バッファ変数は、式 **select** ステートメントで使用できません。</span><span class="sxs-lookup"><span data-stu-id="01f31-395">A table buffer variable can't be used in an expression **select** statement.</span></span> <span data-ttu-id="01f31-396">テーブルの名前は、**from** 句で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-396">The name of the table must be used in the **from** clause.</span></span> <span data-ttu-id="01f31-397">式**選択**明細書の 1 つの制限は、**結合**キーワードが式結合でサポートされていないことです。</span><span class="sxs-lookup"><span data-stu-id="01f31-397">One limitation of expression **select** statements is that the **join** keyword isn't supported in an expression join.</span></span>

### <a name="expression-select-examples"></a><span data-ttu-id="01f31-398">式選択の例</span><span class="sxs-lookup"><span data-stu-id="01f31-398">expression select examples</span></span>

<span data-ttu-id="01f31-399">次の例では、かっこ内の **select** ステートメントは 1 つの行を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-399">In the following example, the **select** statement inside the parentheses returns one row.</span></span> <span data-ttu-id="01f31-400">データを取り込むことができる唯一の列は、**select** 句の **from** 句の前に名前が付けられている列です。</span><span class="sxs-lookup"><span data-stu-id="01f31-400">The only column that can be populated with data is the column that is named before the **from** clause in the **select** clause.</span></span> <span data-ttu-id="01f31-401">閉じ括弧の後に、その列の名前を使用してデータ値を参照します: **).AccountNum;**。</span><span class="sxs-lookup"><span data-stu-id="01f31-401">After the closing parenthesis, the name of that column is used to reference the data value: **).AccountNum;**.</span></span> <span data-ttu-id="01f31-402">この例は、**firstonly** キーワードを使用するため、最大で 1 行を返します。</span><span class="sxs-lookup"><span data-stu-id="01f31-402">This example returns a maximum of one row, because it uses the **firstonly** keyword.</span></span> <span data-ttu-id="01f31-403">ただし、**firstonly** キーワードが省略されるとしても **sAccountNum** に割り当てられる値は同じです。</span><span class="sxs-lookup"><span data-stu-id="01f31-403">However, the value that is assigned to **sAccountNum** is the same, even if the **firstonly** keyword is omitted.</span></span> <span data-ttu-id="01f31-404">この例の **where** 句には、**where** 句が **order by** 句の後に配置されるべきであることを示し以外の目的がありません。</span><span class="sxs-lookup"><span data-stu-id="01f31-404">The **where** clause in this example serves no purpose except to show that the **where** clause must occur after the **order by** clause.</span></span> <span data-ttu-id="01f31-405">**order by** 句でフィールド名を修飾するために、テーブル名を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="01f31-405">The table name can't be used to qualify a field name in the **order by** clause.</span></span>

```X++
int64 nRecId, nCount;
str sAccountNum, sName;
sAccountNum = (select firstonly AccountNum from CustTable
    order by AccountNum desc
    where 0 == 0 // 'where' must occur after 'order by'. )
    .AccountNum;
info(strFmt("Test_1.a: %1", sAccountNum));
```

<span data-ttu-id="01f31-406">前の例と同じ結果を達成する単純な方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-406">Here is a simpler way to achieve the same result as the previous example.</span></span>

```X++
/********* Actual Infolog output
 Test_1.a: 4507Test_1.b: 4507
 *********/

int64 nRecId, nCount;
str sAccountNum, sName;
sAccountNum = (select maxof(AccountNum) from CustTable).AccountNum;
info(strFmt("Test_1.b: %1", sAccountNum));
```
<span data-ttu-id="01f31-407">次の例には、**where** 句が含まれています。</span><span class="sxs-lookup"><span data-stu-id="01f31-407">The following example includes a **where** clause.</span></span> <span data-ttu-id="01f31-408">**where** 句では、テーブル名をフィールドの修飾子として使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-408">In a **where** clause, the table name must be used as a qualifier of the field.</span></span> <span data-ttu-id="01f31-409">ここで、**maxof** 集計関数が使用され、**RecId** フィールドが機能に記載されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-409">Here, the **maxof** aggregate function is used, and the **RecId** field is mentioned in the function.</span></span> <span data-ttu-id="01f31-410">集計関数に記載されているフィールドは、閉じかっこの後のデータ値を参照するために使用されるフィールド名と同じでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="01f31-410">The field that is mentioned in the aggregate function must be the same as the field name that is used to reference the data value after the closing parenthesis.</span></span> <span data-ttu-id="01f31-411">それ以外の場合、空のデータが返されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-411">Otherwise, empty data is returned.</span></span>

```X++
int64 nRecId, nCount;
str sAccountNum, sName;
nRecId = (select maxof(RecId) from CustTable
    where CustTable.Blocked == CustVendorBlocked::No)
    .RecId;
info(strFmt("Test_2.c: %1", nRecId));

/********* Actual Infolog output
Test_2.c: 5637144604
*********/
```

<span data-ttu-id="01f31-412">次の例では、フィールド名 (この場合は **RecId**) は **RecId** の値ではないデータ値を参照するために使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-412">In the following example, a field name (in this case, **RecId**) is used to reference a data value that isn't a **RecId** value.</span></span> <span data-ttu-id="01f31-413">**count** 集計関数は、**RecId**値を返しません。</span><span class="sxs-lookup"><span data-stu-id="01f31-413">The **count** aggregate function doesn't return a **RecId** value.</span></span> <span data-ttu-id="01f31-414">**RecId** フィールドは通常 **cound** 関数と共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-414">Typically, the **RecId** field is used with the **count** function.</span></span>

```X++
int64 nRecId, nCount;
str sAccountNum, sName;
nRecId = (select count(RecId) from CustTable
    where CustTable.Blocked == CustVendorBlocked::No)
    .RecId;
info(strFmt("Test_2.d: %1", nRecId));

/********* Actual Infolog output
Test_2.d: 29
*********/
```

<span data-ttu-id="01f31-415">**join** キーワードは、式 **select** ステートメントでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="01f31-415">The **join** keyword isn't supported in expression **select** statements.</span></span> <span data-ttu-id="01f31-416">次の例は、サブセレクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-416">The following example shows a subselect.</span></span> <span data-ttu-id="01f31-417">ただし、式選択の**ステートメント**は、標準の内部結合に相当するサブセレクトをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="01f31-417">However, expression select **statements** don't support subselects that are equivalent to a standard inner join.</span></span> <span data-ttu-id="01f31-418">したがって、次の例では、1 つの式 **select** ステートメント内 (つまり、副選択内) に 2 つのテーブルが記述されているため、コンパイルは行われません。</span><span class="sxs-lookup"><span data-stu-id="01f31-418">Therefore, the following example doesn't compile, because it mentions two tables inside one expression **select** statement (that is, inside the subselect).</span></span> <span data-ttu-id="01f31-419">この例に示すように、サブセレクトはサポートされていますが、制限された方法でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="01f31-419">As this example shows, subselects are supported, but only in a limited manner.</span></span>

```X++
// This job does not compile.
static void BadJob(Args _args)
{
    sName = (select Name from AssetTable
        where AssetTable.AssetId ==
            // Here starts the subselect.
            (select AssetId from AssetTrans
                where AssetTrans.AssetId ==
                    AssetTable.AssetId // Compiler rejects this line.
            ).AssetId).Name;
    info(strFmt("Test_3: %1", sName));
}

/********* Actual Infolog output
Test_3: CNC-Metal shade
*********/
```

## <a name="update-method"></a><span data-ttu-id="01f31-420">update メソッド</span><span class="sxs-lookup"><span data-stu-id="01f31-420">update method</span></span>
<span data-ttu-id="01f31-421">**update** テーブル メソッドは、バッファーの内容で現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-421">The **update** table method updates the current record with the contents of the buffer.</span></span> <span data-ttu-id="01f31-422">また、適切なシステム フィールドも更新されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-422">It also updates the appropriate system fields.</span></span> <span data-ttu-id="01f31-423">**where** 句はオプションです。</span><span class="sxs-lookup"><span data-stu-id="01f31-423">The **where** clause is optional.</span></span> <span data-ttu-id="01f31-424">これが使用されるとき、**WHERE** 句は、テーブルの各行を処理するときに **更新** でテストされる条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="01f31-424">When it's used, the **where** clause specifies a condition that **update** tests as it processes each row of the table.</span></span> <span data-ttu-id="01f31-425">その条件に対する **true** をテストする行のみ新しい値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-425">Only those rows that test **true** against the condition are updated with the new values.</span></span> <span data-ttu-id="01f31-426">**update\_recordset** 演算子は、同時に複数のレコードを更新するレコード セット ベースの演算子です。</span><span class="sxs-lookup"><span data-stu-id="01f31-426">The **update\_recordset** operator is a record set–based operator that updates multiple records at the same time.</span></span> <span data-ttu-id="01f31-427">**update** の動作をオーバーライドするには、**doUpdate** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-427">To override the behavior of **update**, use the **doUpdate** method.</span></span> <span data-ttu-id="01f31-428">次の例では、更新する custTable テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="01f31-428">The following example selects the custTable table for update.</span></span> <span data-ttu-id="01f31-429">**AccountNum** フィールドの値が **4000** に等しいレコードは更新されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-429">Any records where the value of the **AccountNum** field is equal to **4000** are updated.</span></span> <span data-ttu-id="01f31-430">(この場合、レコードは 1 つだけ更新されます。) **CreditMax** フィールドの値は **5000** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-430">(In this case, only one record is updated.) The value of the **CreditMax** field is changed to **5000**.</span></span>

```X++
CustTable custTable;
ttsBegin;
    select forUpdate custTable
    where custTable.AccountNum == '4000';
    custTable.CreditMax = 5000;
    custTable.update();
ttsCommit;
```

## <a name="doupdate-method"></a><span data-ttu-id="01f31-431">doUpdate メソッド</span><span class="sxs-lookup"><span data-stu-id="01f31-431">doUpdate method</span></span>
<span data-ttu-id="01f31-432">**doUpdate** メソッドは、バッファーの内容で現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-432">The **doUpdate** method updates the current record with the contents of the buffer.</span></span> <span data-ttu-id="01f31-433">このメソッドでは、適切なシステム フィールドも更新されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-433">This method also updates the appropriate system fields.</span></span> <span data-ttu-id="01f31-434">テーブルでの **更新** メソッドをバイパスする必要があるときは、**doUpdate** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-434">You should use the **doUpdate** method when the **update** method on the table must be bypassed.</span></span> <span data-ttu-id="01f31-435">**doUpdate** テーブル メソッドの構文は、**void doUpdate()** です。</span><span class="sxs-lookup"><span data-stu-id="01f31-435">The syntax for a **doUpdate** table method is **void doUpdate()**.</span></span> <span data-ttu-id="01f31-436">次の例では、**CreditMax** フィールドの値は 1,000 ずつ増加します。</span><span class="sxs-lookup"><span data-stu-id="01f31-436">In the following example, the value of the **CreditMax** field is increased by 1,000.</span></span>

```X++
static void Job1(Args _args)
{
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
}
```

## <a name="delete-method"></a><span data-ttu-id="01f31-437">delete メソッド</span><span class="sxs-lookup"><span data-stu-id="01f31-437">delete method</span></span>
<span data-ttu-id="01f31-438">**削除** テーブル メソッドは、データベースから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="01f31-438">The **delete** table method deletes the current record from the database.</span></span> <span data-ttu-id="01f31-439">このメソッドを使用するには、**where** 句を使用して削除する行を指定します。</span><span class="sxs-lookup"><span data-stu-id="01f31-439">To use this method, use a **where** clause to specify the rows to delete.</span></span> <span data-ttu-id="01f31-440">一度に 1 つのレコードが、指定されたテーブルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-440">One record at a time is then removed from the specified table.</span></span> <span data-ttu-id="01f31-441">**delete\_from** 演算子は、同時に複数のレコードを削除するレコード セット ベースの演算子です。</span><span class="sxs-lookup"><span data-stu-id="01f31-441">The **delete\_from** operator is a record set–based operator that removes multiple records at the same time.</span></span> <span data-ttu-id="01f31-442">**delete** メソッドは上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-442">The **delete** method can be overridden.</span></span> <span data-ttu-id="01f31-443">たとえば、レコードが削除される前に、追加の検証を追加する場合があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-443">For example, you might want to add extra validation before records are deleted.</span></span> <span data-ttu-id="01f31-444">**削除**方法をオーバーライドする場合、**doDelete** を呼び出すことで、**削除**メソッドの元の (ベース) バージョンを実行できます。</span><span class="sxs-lookup"><span data-stu-id="01f31-444">If you override the **delete** method, you can run the original (base) version of the **delete** method by calling the **doDelete** method.</span></span> <span data-ttu-id="01f31-445">したがって、**doDelete** メソッドへの呼び出しは**delete** メソッドの **super()** への呼び出しに相当します。</span><span class="sxs-lookup"><span data-stu-id="01f31-445">Therefore, a call to the **doDelete** method is equivalent to a call to **super()** in the **delete** method.</span></span> <span data-ttu-id="01f31-446">次の例では、**where** 句の条件を満たす MyTable テーブル内のすべてのレコード (つまり、**AccountNum** フィールドの値が **1000** に等しいすべてのレコード) がデータベースから削除されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-446">In the following example, all records in the MyTable table that satisfy the criterion in the **where** clause (that is, all records where the value of the **AccountNum** field is equal to **1000**) are deleted from the database.</span></span> <span data-ttu-id="01f31-447">一度に 1 つのレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-447">One record is deleted at a time.</span></span>

```X++
ttsBegin;
while select forUpdate myTable
    where myTable.AccountNum == '1000'
{
    myTable.delete();
}
ttsCommit;
```

## <a name="dodelete-method"></a><span data-ttu-id="01f31-448">doDelete メソッド</span><span class="sxs-lookup"><span data-stu-id="01f31-448">doDelete method</span></span>
<span data-ttu-id="01f31-449">**delete** テーブル メソッドと同様に、**doDelete** テーブル メソッドは、データベースから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="01f31-449">Like the **delete** table method, the **doDelete** table method deletes the current record from the database.</span></span> <span data-ttu-id="01f31-450">**delete** テーブル メソッドがオーバーライドされていて、オーバーライドされているバージョンではなく **delete** メソッドの元の (基本) バージョンを実行する場合は **doDelete** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-450">Use the **doDelete** method if the **delete** table method has been overridden, and you want to run the original (base) version of the **delete** method instead of the overridden version.</span></span> <span data-ttu-id="01f31-451">したがって、**doDelete** メソッドへの呼び出しは**delete** メソッドの **super()** への呼び出しに相当します。</span><span class="sxs-lookup"><span data-stu-id="01f31-451">Therefore, a call to the **doDelete** method is equivalent to a call to **super()** in the **delete** method.</span></span> <span data-ttu-id="01f31-452">次の例では、**200** 以上のアカウント番号を持つ myTable テーブルのすべてのレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="01f31-452">The following example deletes all records in the myTable table that have an account number that is more than or equal to **200**.</span></span>

```X++
ttsBegin;
while select forUpdate myTable
    where myTable.AccountNum >='200';
{
    myTable.doDelete();
}
ttsCommit;
```

## <a name="insert-method"></a><span data-ttu-id="01f31-453">insert メソッド</span><span class="sxs-lookup"><span data-stu-id="01f31-453">insert method</span></span>
<span data-ttu-id="01f31-454">**insert** メソッドは、一度に 1 つのレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-454">The **insert** method updates one record at a time.</span></span> <span data-ttu-id="01f31-455">一度に複数のレコードを挿入するには、配列挿入、**挿入\_レコードセット**、または **RecordSortedList.insertDatabase** を挿入します。</span><span class="sxs-lookup"><span data-stu-id="01f31-455">To insert multiple records at a time, use array inserts, **insert\_recordset**, or **RecordSortedList.insertDatabase**.</span></span> <span data-ttu-id="01f31-456">**insert** メソッドの動作をオーバーライドするには、**doInsert** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-456">To override the behavior of the **insert** method, use the **doInsert** method.</span></span> <span data-ttu-id="01f31-457">**xRecord .insert** メソッドは、**RecId** フィールドおよびシステム フィールドの値を生成した後、データベースにバッファーの内容を挿入します。</span><span class="sxs-lookup"><span data-stu-id="01f31-457">The **xRecord .insert** method generates values for the **RecId** field and system fields, and then inserts the contents of the buffer into the database.</span></span> <span data-ttu-id="01f31-458">**挿入**メソッドが作用する方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-458">Here is how the **insert** method works:</span></span>

-   <span data-ttu-id="01f31-459">クエリによって選択されている行の指定された列のみ、名前付きテーブルに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-459">Only the specified columns of the rows that have been selected by the query are inserted into the named table.</span></span>
-   <span data-ttu-id="01f31-460">コピー元のテーブルの列とコピー先のテーブルの列は、互換性のある型であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="01f31-460">The columns of the table that is copied from and the columns of the table that is copied to must be type-compatible.</span></span>
-   <span data-ttu-id="01f31-461">両方のテーブルの列がタイプおよび順序において一致する場合、列リストは**挿入**句から省略されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-461">If the columns of both tables match in type and order, column list can be omitted from the **insert** clause.</span></span>

### <a name="insert-example-inserting-a-new-record"></a><span data-ttu-id="01f31-462">insert の例: 新規レコードの挿入</span><span class="sxs-lookup"><span data-stu-id="01f31-462">insert example: Inserting a new record</span></span>

<span data-ttu-id="01f31-463">次の例では、新しいレコードを CustTable テーブルに挿入します。</span><span class="sxs-lookup"><span data-stu-id="01f31-463">The following example inserts a new record into the CustTable table.</span></span> <span data-ttu-id="01f31-464">新しいレコードの **AccountNum** フィールドは **5000** に設定され、**Name** フィールドは **MyCompany** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-464">The **AccountNum** field of the new record is set to **5000**, and the **Name** field is set to **MyCompany**.</span></span> <span data-ttu-id="01f31-465">(レコードの他のフィールドは空白になります。)</span><span class="sxs-lookup"><span data-stu-id="01f31-465">(Other fields in the record will be blank.)</span></span>

```X++
CustTable custTable;
ttsBegin;
select forUpdate custTable;
custTable.AccountNum = '5000';
custTable.insert();
ttsCommit;
```

### <a name="insert-example-transaction-and-duplicate-key"></a><span data-ttu-id="01f31-466">insert の例: トランザクションと重複キー</span><span class="sxs-lookup"><span data-stu-id="01f31-466">insert example: Transaction and duplicate key</span></span>

<span data-ttu-id="01f31-467">次の例は、明示的なトランザクションのコンテキストで **DuplicateKeyException** 例外をキャッチする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-467">The following example shows how you can catch a **DuplicateKeyException** exception in the context of an explicit transaction.</span></span> <span data-ttu-id="01f31-468">既存の一意の値が重複しているため、**xRecord .insert**の 呼び出しが失敗した場合に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="01f31-468">The exception is thrown when a call to **xRecord .insert** fails because an existing unique value is duplicated.</span></span> <span data-ttu-id="01f31-469">**catch** ブロックでは、コードで修正アクションを実行するか、後で分析するためにエラーを記録したりできます。</span><span class="sxs-lookup"><span data-stu-id="01f31-469">In the **catch** block, your code can either take corrective action or log the error for later analysis.</span></span> <span data-ttu-id="01f31-470">これにより、トランザクションの保留中のすべての作業が失うことなく、コードの実行を続けることできます。</span><span class="sxs-lookup"><span data-stu-id="01f31-470">Your code can then continue without losing all the pending work of the transaction.</span></span> <span data-ttu-id="01f31-471">**挿入\_レコードセット** などのセットに基づく操作によって発生する重複キー例外を把握することはできません。</span><span class="sxs-lookup"><span data-stu-id="01f31-471">You can't catch a duplicate key exception that is caused by a set-based operation such as **insert\_recordset**.</span></span> <span data-ttu-id="01f31-472">この例は、TableNumberAとTableNumberB という 2 つのテーブルによって異なります。</span><span class="sxs-lookup"><span data-stu-id="01f31-472">This example depends on two tables: TableNumberA and TableNumberB.</span></span> <span data-ttu-id="01f31-473">両方のテーブルには 1 つの必須の整数フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="01f31-473">Both tables have one mandatory integer field.</span></span> <span data-ttu-id="01f31-474">これらのフィールドはそれぞれ、**NumberAKey** および **NumberBKey** と命名されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-474">These fields are named **NumberAKey** and **NumberBKey**, respectively.</span></span> <span data-ttu-id="01f31-475">固有インデックスは、各キー フィールドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-475">A unique index is defined on each key field.</span></span> <span data-ttu-id="01f31-476">TableNumberA テーブルには、少なくとも 1 つのレコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="01f31-476">The TableNumberA table must have at least one record in it.</span></span>

```X++
static void JobDuplicKeyException44Job(Args _args)
{
    TableNumberA tabNumA; // Has one record, key = 11.
    TableNumberB tabNumB;
    int iCountTries = 0, iNumberAdjust = 0, iNewKey, ii;
    container ctNotes;
    // Empty the B table.
    delete_from tabNumB;
    // Insert a copy of one record.
    insert_recordset tabNumB (NumberBKey)
    select firstOnly NumberAKey from tabNumA order by NumberAKey asc;
    ttsBegin;
    try
    {
        iCountTries++;
        ctNotes += strFmt("---- Inside the try block, try count is %1. ----", iCountTries);
        while select * from tabNumA order by NumberAKey asc
        {
            tabNumB .clear();
            iNewKey = tabNumA .NumberAKey + iNumberAdjust;
            tabNumB .NumberBKey = iNewKey;
            ctNotes += strFmT ("-- %1 is the key to be tried. --" ,iNewKey);
            tabNumB .insert();
            ctNotes += "-- .insert() successful. --";
            break; // Keeps demo simple.
        }
        ttsCommit;
    }
    catch (Exception ::DuplicateKeyException, tabNumB) // Table is optional.
    {
        ctNotes += "---- Inside the catch block. ----";
        ctNotes += infolog .text();
        if (iCountTries <= 1)
        {
            ctNotes += "-- Will issue retry. --";
            iNumberAdjust = 1;
            retry; // Erases Infolog.
        }
        else
        {
            ctNotes += "-- Aborting the transaction. --";
            ttsAbort;
        }
    }
    for (ii=1; ii <= conLen(ctNotes); ii++)
    {
        info(conPeek(ctNotes ,ii));
    }
}

/*********Actual Infolog output
        Message (10:53:13 am)
    ---- Inside the try block, try count is 1. ----
    -- 11 is the key to be tried. --
    ---- Inside the catch block. ----
    Cannot create a record in TableNumberB (TableNumberB).
    The record already exists.
    -- Will issue retry. --
    ---- Inside the try block, try count is 2. ----
    -- 12 is the key to be tried. --
    -- .insert() successful. --
*********/
```

## <a name="doinsert-method"></a><span data-ttu-id="01f31-477">doInsert メソッド</span><span class="sxs-lookup"><span data-stu-id="01f31-477">doInsert method</span></span>
<span data-ttu-id="01f31-478">**doInsert** メソッドは、**RecId** フィールドおよびその他のシステム フィールドの値を生成した後、データベースにバッファーの内容を挿入します。</span><span class="sxs-lookup"><span data-stu-id="01f31-478">The **doInsert** method generates values for the **RecId** field and other system fields, and then inserts the contents of the buffer into the database.</span></span> <span data-ttu-id="01f31-479">テーブルの **insert** メソッドをバイパスする必要がある場合は、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-479">Use this method when the **insert** method on the table must be bypassed.</span></span> <span data-ttu-id="01f31-480">次の例では、新しいレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-480">In the following example, a new record is inserted.</span></span> <span data-ttu-id="01f31-481">レコードの **name** フィールドは **Warren Langer** に設定され、**value** フィールドは **100** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-481">The **name** field of the record is set to **Warren Langer**, and the **value** field is set to **100**.</span></span>

```X++
ttsBegin;
myTable.name = 'Warren Langer';
myTable.value = 100;
myTable.doInsert();
ttsCommit;
```

## <a name="transactional-integrity"></a><span data-ttu-id="01f31-482">トランザクションの整合性</span><span class="sxs-lookup"><span data-stu-id="01f31-482">Transactional integrity</span></span>
<span data-ttu-id="01f31-483">手順で、トランザクションの整合性を保証しなかった場合、データが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-483">If steps aren't taken to help guarantee the integrity of transactions, data corruption could occur.</span></span> <span data-ttu-id="01f31-484">少なくとも、システム上の同時ユーザーに関してスケーラビリティが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-484">At the very least, you might experience poor scalability with respect to concurrent users on the system.</span></span> <span data-ttu-id="01f31-485">**forUpdate** チェックと **tssLevel** チェックの 2 つの内部チェック機能がトランザクションの完全性を保証します。</span><span class="sxs-lookup"><span data-stu-id="01f31-485">Two internal checking features help guarantee the integrity of transactions: the **forUpdate** check and the **tssLevel** check.</span></span> <span data-ttu-id="01f31-486">**forUpdate** チェックは、更新のために最初に選択されたレコードのみを更新または削除されるのを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="01f31-486">A **forUpdate** check helps guarantee that a record can be updated or deleted only if it has first been selected for update.</span></span> <span data-ttu-id="01f31-487">**select** ステートメント内の **forUpdate** キーワードまたはテーブル上の **selectForUpdate** メソッドのいずれかを使用することで、更新プログラムのレコードを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-487">You can select a record for update by using either the **forUpdate** keyword in the **select** statement or the **selectForUpdate** method on tables.</span></span> <span data-ttu-id="01f31-488">**ttsLevel** チェックは、レコードが更新のために選択されたのと同じトランザクション範囲内でのみ更新または削除できることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="01f31-488">A **ttsLevel** check helps guarantee that a record can be updated or deleted only within the same transaction scope where it was selected for update.</span></span> <span data-ttu-id="01f31-489">整合性を保証するために、次のステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-489">The following statements are used to help guarantee integrity:</span></span>

-   <span data-ttu-id="01f31-490">**ttsBegin** – このステートメントは、トランザクションの開始位置を示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-490">**ttsBegin** – This statement marks the beginning of a transaction.</span></span> <span data-ttu-id="01f31-491">これにより、データの整合性が保証され、トランザクションが終了するまで (**ttsCommit** または **ttsAbort** を通じて) 実行されるすべての更新が一貫したもの (すべてまたはなし) であることも保証されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-491">It helps guarantee data integrity, and also helps guarantees that all updates that are done until the transaction ends (through **ttsCommit** or **ttsAbort**) are consistent (all or none).</span></span>
-   <span data-ttu-id="01f31-492">**ttsCommit** – このステートメントは、トランザクションの正常終了を示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-492">**ttsCommit** – This statement marks the successful end of a transaction.</span></span> <span data-ttu-id="01f31-493">トランザクションを終了してコミットします。</span><span class="sxs-lookup"><span data-stu-id="01f31-493">It ends and commits a transaction.</span></span> <span data-ttu-id="01f31-494">Finance and Operations アプリケーションは、確定されたトランザクションが意図に従って実行されるのを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="01f31-494">The Finance and Operations application helps guarantee that a transaction that has been committed will be performed according to intentions.</span></span>
-   <span data-ttu-id="01f31-495">**ttsAbort** – このステートメントを使用すると、現在のトランザクションのすべての変更を明示的に破棄できます。</span><span class="sxs-lookup"><span data-stu-id="01f31-495">**ttsAbort** – This statement lets you explicitly discard all changes in the current transaction.</span></span> <span data-ttu-id="01f31-496">この場合、データベースは何も変更されていない元の状態にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="01f31-496">In this case, the database is rolled back to the original state where nothing has been changed.</span></span> <span data-ttu-id="01f31-497">この文は通常、ユーザーが現在のジョブを中断したいことを検出した場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-497">Typically, you use this statement if you've detected that the user wants to break the current job.</span></span> <span data-ttu-id="01f31-498">**ttsAbort** ステートメントは、データベースが一貫していることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="01f31-498">The **ttsAbort** statement helps guarantee that the database is consistent.</span></span>

<span data-ttu-id="01f31-499">通常、**ttsAbort** の代わりに、例外処理を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="01f31-499">Usually, it's a better idea to use exception handling instead of **ttsAbort**.</span></span> <span data-ttu-id="01f31-500">**throw** ステートメントは、自動的に現在のトランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="01f31-500">The **throw** statement automatically aborts the current transaction.</span></span> <span data-ttu-id="01f31-501">次の例が示すように、**ttsBegin** と **ttsCommit** の間の明細書には 1 つ以上のトランザクション ブロックを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-501">As the following example shows, statements between **ttsBegin** and **ttsCommit** can include one or more transaction blocks.</span></span> <span data-ttu-id="01f31-502">そのような場合、最後の **ttsCommit** ステートメントから正常に終了するまで実際にコミットされるものはありません。</span><span class="sxs-lookup"><span data-stu-id="01f31-502">In these cases, nothing is actually committed until the successful exit from the final **ttsCommit** statement.</span></span>

```X++
ttsBegin;
    // Some statements.
ttsBegin;
    // More statements.
ttsCommit;
ttsCommit;
```

<span data-ttu-id="01f31-503">次の例では、レコードのセットを選択し、**NameAlias** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-503">The following example selects a set of records and updates the **NameAlias** field.</span></span>

```X++
Custtable custTable;
ttsBegin;
select forUpdate custTable where custTable.AccountNum == '4000';
custTable.NameAlias = custTable.Name;
custTable.update();
ttsCommit;
```

### <a name="example-of-code-that-is-rejected-by-the-two-transaction-integrity-checks"></a><span data-ttu-id="01f31-504">2 つのトランザクションの整合性チェックが拒否したコード例</span><span class="sxs-lookup"><span data-stu-id="01f31-504">Example of code that is rejected by the two transaction integrity checks</span></span>

<span data-ttu-id="01f31-505">この例では、**forupdate** キーワードがないため、最初のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="01f31-505">In this example, the first failure occurs because the **forupdate** keyword is missing.</span></span> <span data-ttu-id="01f31-506">2 番目のエラーは、更新のトランザクション スコープが、レコードが **ttsCommit** の更新用に選択されたトランザクション スコープと異なるために発生します。</span><span class="sxs-lookup"><span data-stu-id="01f31-506">The second failure occurs because the transaction scope of the update differs from the transaction scope where the record was selected for update in **ttsCommit**.</span></span>

```X++
ttsBegin;
select myTable; // Rejected by the forUpdate check.
mytable.myField = 'xyz';
myTable.update();
ttsCommit;
ttsBegin;
select forUpdate * from myTable;
myTable.myField = 'xyz';
ttsCommit;
...
ttsBegin;
myTable.update(); // Rejected by the ttsLevel check.
ttsCommit;
```

## <a name="speeding-up-sql-operations"></a><span data-ttu-id="01f31-507">SQL 操作の高速化</span><span class="sxs-lookup"><span data-stu-id="01f31-507">Speeding up SQL operations</span></span>
<span data-ttu-id="01f31-508">次の構文では、複数のレコードを挿入、更新、または削除できます。</span><span class="sxs-lookup"><span data-stu-id="01f31-508">The following constructs let you insert, update, or delete multiple records.</span></span> <span data-ttu-id="01f31-509">これらのコンストラクトを使用することにより、アプリケーションとデータベース間の通信が減少するためパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="01f31-509">By using these constructs, you reduce communication between the application and the database, and therefore help increase performance.</span></span> <span data-ttu-id="01f31-510">場合によっては、レコードのセットに基づく操作をレコードごとの操作に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-510">In some situations, record set–based operations can fall back to record-by-record operations.</span></span>

| <span data-ttu-id="01f31-511">構築</span><span class="sxs-lookup"><span data-stu-id="01f31-511">Construct</span></span>         | <span data-ttu-id="01f31-512">説明</span><span class="sxs-lookup"><span data-stu-id="01f31-512">Description</span></span>                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f31-513">RecordSortedList</span><span class="sxs-lookup"><span data-stu-id="01f31-513">RecordSortedList</span></span>  | <span data-ttu-id="01f31-514">1 つのデータベース トリップに複数のレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="01f31-514">Insert multiple records in one database trip.</span></span> <span data-ttu-id="01f31-515">特定のテーブルのデータのサブセットを必要とし、現在インデックスとして存在しない順序でソートする場合は、このコンストラクトを使用します</span><span class="sxs-lookup"><span data-stu-id="01f31-515">Use this construct when you want a subset of data from a specific table, and you want that data to be sorted in an order that doesn't currently exist as an index.</span></span> |
| <span data-ttu-id="01f31-516">RecordInsertList</span><span class="sxs-lookup"><span data-stu-id="01f31-516">RecordInsertList</span></span>  | <span data-ttu-id="01f31-517">1 つのデータベース トリップに複数のレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="01f31-517">Insert multiple records in one database trip.</span></span> <span data-ttu-id="01f31-518">データをソートする必要がない場合は、この構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="01f31-518">Use this construct when you don't have to sort the data.</span></span> |
| <span data-ttu-id="01f31-519">insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="01f31-519">insert\_recordset</span></span> | <span data-ttu-id="01f31-520">複数のレコードを 1 つまたは複数のテーブルから別のテーブルに直接コピーします。</span><span class="sxs-lookup"><span data-stu-id="01f31-520">Copy multiple records directly from one or more tables into another table in one database trip.</span></span>        |
| <span data-ttu-id="01f31-521">update\_recordset</span><span class="sxs-lookup"><span data-stu-id="01f31-521">update\_recordset</span></span> | <span data-ttu-id="01f31-522">1 回のデータベース トリップでテーブルの複数の行を更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-522">Update multiple rows in a table in one database trip.</span></span>                                                  |
| <span data-ttu-id="01f31-523">delete\_from</span><span class="sxs-lookup"><span data-stu-id="01f31-523">delete\_from</span></span>      | <span data-ttu-id="01f31-524">1 回のデータベース トリップでデータベースから複数のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="01f31-524">Delete multiple records from the database in one database trip.</span></span>                                        |

## <a name="insert_recordset"></a><span data-ttu-id="01f31-525">insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="01f31-525">insert\_recordset</span></span>
<span data-ttu-id="01f31-526">**insert\_recordset** ステートメントは、1 回のサーバー トリップで、1 つ以上のソース テーブルからデータを直接 1 つのターゲット テーブルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="01f31-526">The **insert\_recordset** statement copies data directly from one or more source tables into one destination table in one server trip.</span></span> <span data-ttu-id="01f31-527">配列挿入より **insert\_recordset** を使用したほうが高速です。</span><span class="sxs-lookup"><span data-stu-id="01f31-527">It's faster to use **insert\_recordset** than an array insert.</span></span> <span data-ttu-id="01f31-528">ただし、配列挿入は、データを挿入する前に処理する場合より柔軟になります。</span><span class="sxs-lookup"><span data-stu-id="01f31-528">However, array inserts are more flexible if you want to handle the data before you insert it.</span></span> <span data-ttu-id="01f31-529">**挿入\_レコード セット**はレコード セットに基づく、一度に複数のレコードに対する操作を実行する演算子です。</span><span class="sxs-lookup"><span data-stu-id="01f31-529">**insert\_recordset** is a record set–based operator that performs operations on multiple records at a time.</span></span> <span data-ttu-id="01f31-530">ただし、多くの場合レコードごとの操作に戻れます。</span><span class="sxs-lookup"><span data-stu-id="01f31-530">However, it can fall back to record-by-record operations in many situations.</span></span>

### <a name="insert_recordset-syntax"></a><span data-ttu-id="01f31-531">insert\_recordset 構文</span><span class="sxs-lookup"><span data-stu-id="01f31-531">insert\_recordset syntax</span></span>

<span data-ttu-id="01f31-532">*ListOfFields* 出力先テーブルは、ソース テーブル内のフィールドのリストと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-532">*ListOfFields* in the destination table must match the list of fields in the source tables.</span></span> <span data-ttu-id="01f31-533">データは、フィールドの一覧に表示されている順に転送されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-533">Data is transferred in the order in which it appears in the list of fields.</span></span> <span data-ttu-id="01f31-534">フィールドの一覧に表示されていない出力先テーブルのフィールドは、他の領域と同じように、**0** (ゼロ) の値に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="01f31-534">Fields in the destination table that aren't present in the list of fields are assigned **0** (zero) values, as in other areas.</span></span> <span data-ttu-id="01f31-535">**RecId** などのシステム フィールドは、出力先テーブルのカーネルによって透過的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="01f31-535">System fields, such as **RecId**, are assigned transparently by the kernel in the destination table.</span></span>

<span data-ttu-id="01f31-536">**insert\_recordset** *DestinationTable* **(** *ListOfFields* **)**</span><span class="sxs-lookup"><span data-stu-id="01f31-536">**insert\_recordset** *DestinationTable* **(** *ListOfFields* **)**</span></span>

<span data-ttu-id="01f31-537">**select** *ListOfFields1* **from** *SourceTable* **\[ where** *WhereClause* **\]**</span><span class="sxs-lookup"><span data-stu-id="01f31-537">**select** *ListOfFields1* **from** *SourceTable* **\[ where** *WhereClause* **\]**</span></span> 

<span data-ttu-id="01f31-538">**\[ join** *ListOfFields2* **from** *JoinedSourceTable* **\[ where** *JoinedWhereClause* **\]\]**</span><span class="sxs-lookup"><span data-stu-id="01f31-538">**\[ join** *ListOfFields2* **from** *JoinedSourceTable* **\[ where** *JoinedWhereClause* **\]\]**</span></span>

### <a name="example-inserting-data-from-another-table"></a><span data-ttu-id="01f31-539">例: 別のテーブルからデータを挿入</span><span class="sxs-lookup"><span data-stu-id="01f31-539">Example: Inserting data from another table</span></span>

<span data-ttu-id="01f31-540">この例では、**myNum** および **mySum** レコードは anotherTable テーブルから取得され、myTable テーブルに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-540">In this example, the **myNum** and **mySum** records are retrieved from the anotherTable table and inserted into the myTable table.</span></span> <span data-ttu-id="01f31-541">レコードは **myNum** に基づいてグループ化されます。**100** 以下の値を持つ **myNum** のみが挿入に含まれます。</span><span class="sxs-lookup"><span data-stu-id="01f31-541">The records are grouped according to **myNum**, and only **myNum** records that have a value that is less than or equal to **100** are included in the insertion.</span></span>

```X++
insert_recordset myTable (myNum, mySum)
    select myNum, sum(myValue)
        from anotherTable
        group by myNum
        where myNum <= 100;
```

### <a name="example-inserting-data-from-variables"></a><span data-ttu-id="01f31-542">例: 変数からデータを挿入</span><span class="sxs-lookup"><span data-stu-id="01f31-542">Example: Inserting data from variables</span></span>

<span data-ttu-id="01f31-543">次の例は、**insert\_recordset** ステートメントが変数で提供されるデータを挿入できることを示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-543">The following example shows that the **insert\_recordset** statement can insert data that is provided in variables.</span></span> <span data-ttu-id="01f31-544">この例では、1 行だけ挿入するために **firstonly** キーワードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-544">In this example, the **firstonly** keyword is used so that only one row is inserted.</span></span> <span data-ttu-id="01f31-545">**128** または**このリテラル文字列**などのリテラルは、挿入されるデータのソースとして使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="01f31-545">Literals, such as **128** or **"this literal string"**, can't be used as a source of data that is inserted.</span></span>

```X++
static void InsertVariable3Job(Args _args)
{
    TableAlphabet    tabA2;
    BankAccountTable tabB3;
    str  1 sLetter = "a";
    str 16 sExampleWord = "apple";
    DELETE_FROM tabA2;
    INSERT_RECORDSET tabA2
        (Letter ,ExampleWord)
    select firstonly
        sLetter ,sExampleWord // Variables.
    from tabB3;
    WHILE SELECT * from tabA2
    {
        info(tabA2 .Letter + " , " + tabA2 .ExampleWord);
    }

/***********  Actual Infolog output
Message (04:03:52 pm)
a , apple
***********/
}
```

### <a name="example-inserting-data-by-using-a-join"></a><span data-ttu-id="01f31-546">例: 結合を使用してデータを挿入</span><span class="sxs-lookup"><span data-stu-id="01f31-546">Example: Inserting data by using a join</span></span>

<span data-ttu-id="01f31-547">次の例は、サブセレクトを持つ **insert\_recordset** ステートメント上の 3 つのテーブルの結合を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-547">The following example shows a join of three tables on an **insert\_recordset** statement that has a subselect.</span></span> <span data-ttu-id="01f31-548">また、同じ結合がある **while** **select** ステートメントも示します。</span><span class="sxs-lookup"><span data-stu-id="01f31-548">It also shows a **while** **select** statement that has a similar join.</span></span> <span data-ttu-id="01f31-549">変数は、1 つの列に挿入された値を供給するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-549">A variable is used to supply the inserted value for one column.</span></span> <span data-ttu-id="01f31-550">**str** 変数は、宣言する必要があり、長さを対応するデータベース フィールドの最大長さ以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-550">The **str** variable must be declared, and must have a length that is less than or equal to the maximum length of the corresponding database field.</span></span> <span data-ttu-id="01f31-551">この例では、tabEmplProj5 テーブルに対する **insert\_recordset** ステートメントがあります。</span><span class="sxs-lookup"><span data-stu-id="01f31-551">In this example, there is an **insert\_recordset** statement for the tabEmplProj5 table.</span></span> <span data-ttu-id="01f31-552">ターゲット フィールドの 1 つに**説明**という名前が付けられ、フィールドのデータはローカル変数 **sDescriptionVariable** から取得されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-552">One of the target fields is named **Description**, and the field's data comes from the local variable **sDescriptionVariable**.</span></span> <span data-ttu-id="01f31-553">**説明** フィールドの構成キーは無効の場合でも **insert\_recordset** ステートメントは成功します。</span><span class="sxs-lookup"><span data-stu-id="01f31-553">The **insert\_recordset** statement succeeds even when the configuration key for the **Description** field is turned off.</span></span> <span data-ttu-id="01f31-554">システムでは、**Description** フィールドと **sDescriptionVariable** 変数の両方を無視します。</span><span class="sxs-lookup"><span data-stu-id="01f31-554">The system ignores both the **Description** field and the **sDescriptionVariable** variable.</span></span> <span data-ttu-id="01f31-555">したがって、このコードは*コンフィギュレーション キーの自動化*の例を提供します。</span><span class="sxs-lookup"><span data-stu-id="01f31-555">Therefore, this code provides an example of *configuration key automation*.</span></span> <span data-ttu-id="01f31-556">コンフィギュレーション キーの自動化は、コンフィギュレーション キーがオフになっているフィールドにデータを挿入する **insert\_ recordset** ステートメントの動作を、システムが自動的に調整できるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="01f31-556">Configuration key automation occurs when the system can automatically adjust the behavior of an **insert\_recordset** statement that inserts data into fields that the configuration key is turned off for.</span></span>

```X++
static void InsertJoin42Job(Args _args)
{
    GmTabDepartment tabDept2;
    GmTabEmployee tabEmpl3;
    GmTabProject tabProj4;
    GmTabEmployeeProject tabEmplProj5;
    str 64 sDescriptionVariable = "From variable.";
    DELETE_FROM tabEmplProj5;
    INSERT_RECORDSET tabEmplProj5
        (
        Description
        , EmployeeRecId
        , ProjectRecId
        )
    Select
        sDescriptionVariable
        , RecId
    from
        tabEmpl3
        join
            tabDept2
            where tabEmpl3 .DepartmentGuid == tabDept2 .DepartmentGuid
        join RecId
            from tabProj4
            where tabDept2 .DepartmentGuid == tabProj4 .DepartmentGuid
    info(int642str(tabEmplProj5 .rowCount())
        + " ==Number of rows inserted.");
    WHILE SELECT *
        from
            tabEmplProj5
            join tabEmpl3
                where tabEmplProj5 .EmployeeRecId == tabEmpl3 .RecId
            join tabProj4
                where tabEmplProj5 .ProjectRecId == tabProj4 .RecId
    {
        info(
            tabEmpl3 .EmployeeName
            + "  --works on--  "
            + tabProj4 .ProjectName
            + " (" + tabEmplProj5 .Description + ")."
            );
    }

/*****************  Actual Infolog output
Message (01:05:41 pm)
4 ==Number of rows inserted.
Alice  --works on--  Project ZZZ (From variable.).
Alice  --works on--  Project YY (From variable.).
Beth  --works on--  Project ZZZ (From variable.).
Beth  --works on--  Project YY (From variable.).
*****************/
}
```

## <a name="update_recordset"></a><span data-ttu-id="01f31-557">update\_recordset</span><span class="sxs-lookup"><span data-stu-id="01f31-557">update\_recordset</span></span>
<span data-ttu-id="01f31-558">**update\_recordset** ステートメントでは、サーバーへの 1 回のアクセスで複数の行を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-558">The **update\_recordset** statement lets you update multiple rows in one trip to the server.</span></span> <span data-ttu-id="01f31-559">したがって、SQL Server の機能は、一部のタスクのパフォーマンスを向上させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="01f31-559">Therefore, the power of SQL Server can help improve the performance of some tasks.</span></span> <span data-ttu-id="01f31-560">\*\*\*\*update\_recordset\*\*\*\* ステートメントは X++ の **delete\_from** と SQL の **update set** に似ています。</span><span class="sxs-lookup"><span data-stu-id="01f31-560">The \*\*\*\*update\_recordset\*\*\*\* statement resembles **delete\_from** in X++ and **update set** in SQL.</span></span> <span data-ttu-id="01f31-561">フェッチ、変更、更新によって個別に各レコードを取得しません。代わりに、データベース サーバー側で設定された SQL スタイル レコードで動作します。</span><span class="sxs-lookup"><span data-stu-id="01f31-561">It doesn't retrieve each record separately by fetching, changing, and updating, Instead, it works on an SQL-style record set on the database server side.</span></span> <span data-ttu-id="01f31-562">**更新**メソッドがオーバーライドされた場合、実装は、一度に 1 つのレコードが更新される古典的なループ構造に戻されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-562">If the **update** method is overridden, the implementation falls back to a classic looping construction, where one record at a time is updated.</span></span> <span data-ttu-id="01f31-563">(この動作は、削除対象の **削除の\_対象** の動作に似ています。) したがって、構築は、一時テーブルとテーブル全体 - キャッシュされたテーブルで、ループ構造を使用して動作します。</span><span class="sxs-lookup"><span data-stu-id="01f31-563">(This behavior resembles the behavior of **delete\_from** for deletions.) Therefore, the construction works on temporary tables and whole table–cached tables by using the looping construction.</span></span>

### <a name="example-update-that-is-based-on-a-calculated-value"></a><span data-ttu-id="01f31-564">例: 計算値に基づく更新プログラム</span><span class="sxs-lookup"><span data-stu-id="01f31-564">Example: Update that is based on a calculated value</span></span>

<span data-ttu-id="01f31-565">次の例では、myTableBuffer テーブルを更新して、テーブルのすべてのレコードで **field1**フィールドの値を 10% 増分します。</span><span class="sxs-lookup"><span data-stu-id="01f31-565">The following example updates the myTableBuffer table and increments the value of the **field1** field by ten percent in all records in the table.</span></span>

```X++
MyTable myTableBuffer;
update_recordset myTableBuffer
setting field1 = field1 * 1.10;
```

### <a name="example-update-that-uses-a-where-clause"></a><span data-ttu-id="01f31-566">例: where 句を使用する更新プログラム</span><span class="sxs-lookup"><span data-stu-id="01f31-566">Example: Update that uses a where clause</span></span>

<span data-ttu-id="01f31-567">次の例では、**field1** フィールドの値が **0** の myTable テーブルのすべてのレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-567">The following example updates all records in the myTable table where the **field1** field has the value **0**.</span></span> <span data-ttu-id="01f31-568">**field1** フィールドには、新しい値 **1** が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="01f31-568">The **field1** field is assigned a new value of **1**.</span></span> <span data-ttu-id="01f31-569">**field2** フィールドには、**fieldX** および **fieldY** の合計値が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="01f31-569">The **field2** field is assigned a value that is the sum of **fieldX** and **fieldY**.</span></span> <span data-ttu-id="01f31-570">この例では、複数のフィールドを同時に更新し、**where** 句を満たす行のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="01f31-570">This example updates multiple fields at the same time, and it updates only those rows that satisfy the **where** clause.</span></span>

```X++
MyTable myTableBuffer;
update_recordset myTableBuffer
setting
    field1 = 1,
    field2 = fieldX + fieldY
where field1 == 0;
```

### <a name="example-updating-joined-tables"></a><span data-ttu-id="01f31-571">例: 結合されたテーブルの更新プログラム</span><span class="sxs-lookup"><span data-stu-id="01f31-571">Example: Updating joined tables</span></span>

<span data-ttu-id="01f31-572">次の例は、**update\_recordset** ステートメントが複数のテーブルの結合をサポートしていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-572">The following example shows that the **update\_recordset** statement supports joins of several tables.</span></span> <span data-ttu-id="01f31-573">結合されたテーブルのデータを使用して、更新中のテーブル内のフィールドに値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-573">Data from the joined tables can be used to assign values to fields in the table that is being updated.</span></span>

```X++
static void Join22aJob(Args _args)
{
    TableEmployee tabEmpl;
    TableDepartment tabDept;
    TableProject tabProj;
    update_recordset tabEmpl
    setting
        currentStatusDescription = tabDept .DeptName
            + ", " + tabProj .ProjName
    join tabDept
        where tabDept .DeptId == tabEmpl .DeptId
    join tabProj
        where tabProj .ProjId == tabEmpl .ProjId;
    info(strFmt("Number of records updated is %1."
        ,tabEmpl .rowCount()));
}
```

## <a name="delete_from"></a><span data-ttu-id="01f31-574">delete\_from</span><span class="sxs-lookup"><span data-stu-id="01f31-574">delete\_from</span></span>
<span data-ttu-id="01f31-575">**delete\_from** ステートメントを使用することにより、データベース テーブルから複数のレコードを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-575">You can delete multiple records from a database table by using a **delete\_from** statement.</span></span> <span data-ttu-id="01f31-576">この方法は、一度に 1 つのレコードを削除するループで **xRecord .delete** メソッドを使用する方法よりも効率的かつ高速になります。</span><span class="sxs-lookup"><span data-stu-id="01f31-576">This approach can be more efficient and faster than an approach that uses the **xRecord .delete** method in a loop to delete one record at a time.</span></span> <span data-ttu-id="01f31-577">**delete** メソッドをオーバーライドした場合、システムは削除される各行につき 1 回 **delete\_from** ステートメントを **delete** メソッドを呼び出すコードに解釈します。</span><span class="sxs-lookup"><span data-stu-id="01f31-577">If you've overridden the **delete** method, the system interprets the **delete\_from** statement into code that calls the **delete** method one time for each row that is deleted.</span></span>

### <a name="example-efficiently-deleting-records-by-using-delete_from"></a><span data-ttu-id="01f31-578">例: delete\_from を使用して、効率的にレコードを削除</span><span class="sxs-lookup"><span data-stu-id="01f31-578">Example: Efficiently deleting records by using delete\_from</span></span>

<span data-ttu-id="01f31-579">次の例は、複数のレコードを効率的に削除する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-579">The following example shows an efficient way to delete multiple records.</span></span>

```X++
static void DeleteMultiRow1aJob(Args _args)
{
    MyWidgetTable tabWidget;
    delete_from tabWidget
        where tabWidget .quantity <= 100;
}
```

#### <a name="example-inefficiently-deleting-records-by-using-forupdate"></a><span data-ttu-id="01f31-580">例: forUpdate を使用して、非効率的にレコードを削除</span><span class="sxs-lookup"><span data-stu-id="01f31-580">Example: Inefficiently deleting records by using forUpdate</span></span>

<span data-ttu-id="01f31-581">次の例は非効率的です。</span><span class="sxs-lookup"><span data-stu-id="01f31-581">The following example is inefficient.</span></span> <span data-ttu-id="01f31-582">個別の SQL **削除**呼び出しを、各レコードのデータベース サーバーに発行します。</span><span class="sxs-lookup"><span data-stu-id="01f31-582">It issues a separate SQL **delete** call to the database server for every record.</span></span> <span data-ttu-id="01f31-583">**xRecord** **.delete** メソッドが、呼び出しごとに複数のレコードを削除することはありません。</span><span class="sxs-lookup"><span data-stu-id="01f31-583">The **xRecord** **.delete** method never deletes more than one record per call.</span></span>

```X++
static void DeleteMultiRow1bJob(Args _args)
{
    MyWidgetTable tabWidget; // extends xRecord.
    ttsBegin;
    while select
        forUpdated
        tabWidget
        where tabWidget .quantity <= 100
    {
        tabWidget .delete();
    }
    ttsCommit;
}
```
### <a name="example-a-delete-operation-that-has-an-inner-join"></a><span data-ttu-id="01f31-584">例: 内部結合を持つ削除操作</span><span class="sxs-lookup"><span data-stu-id="01f31-584">Example: A delete operation that has an inner join</span></span>

<span data-ttu-id="01f31-585">内部結合は **delete\_from** ステートメントではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="01f31-585">Inner joins aren't supported on the **delete\_from** statement.</span></span> <span data-ttu-id="01f31-586">したがって、修正していない **join** キーワードを **delete\_from** ステートメント上で使用することができません。</span><span class="sxs-lookup"><span data-stu-id="01f31-586">Therefore, you can't use the unmodified **join** keyword on the **delete\_from** statement.</span></span> <span data-ttu-id="01f31-587">ただし、他の方法を使用して内部結合を論理的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="01f31-587">However, you can logically accomplish an inner join by using other techniques.</span></span> <span data-ttu-id="01f31-588">次の例は、一連のステートメントを通して内部結合ロジックを達成するための新旧の手法を示しています。</span><span class="sxs-lookup"><span data-stu-id="01f31-588">The following example shows the new and old techniques for achieving inner join logic through a sequence of statements.</span></span>

```X++
// This is the new and recommended way of using the delete_from method and inner joins.
// The following code example is relatively efficient. It issues a
// separate delete_from statement for each loop iteration. However, each
// delete_from statement can delete multiple records, a subset of all the
// records that the job deletes.
static void DeleteInnerJoin2bJob(Args _args)
{
    MyWidgetTable tabWidget; // extends xRecord.
    ttsBegin;
    while select
        from tabGalaxy
            where tabGalaxy .isTrusted == 0
    {
        delete_from tabWidget
            where tabWidget .GalaxyRecId ==
                tabGalaxy .RecId;
    }
    ttsCommit;
}

// This is the old way of using the delete method and inner joins.
// The following delete method is inefficient. It issues a
// separate SQL delete call to the database server for each record.
static void DeleteInnerJoin2aJob(Args _args)
{
    MyWidgetTable tabWidget; // extends xRecord.
    ttsBegin;
    while select
        forUpdate
        tabWidget
        join tabGalaxy
            where
                tabWidget .GalaxyRecId == tabGalaxy .RecId
                && tabGalaxy .isTrusted == 0
    {
        tabWidget .delete();
    }
    ttsCommit;
}
```
### <a name="example-a-delete-operation-that-uses-the-notexists-join-keyword"></a><span data-ttu-id="01f31-589">例: notexists 結合キーワードを使用する削除操作</span><span class="sxs-lookup"><span data-stu-id="01f31-589">Example: A delete operation that uses the notexists join keyword</span></span>

<span data-ttu-id="01f31-590">**notexists join** キーワード ペアは **delete\_from** ステートメント内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-590">You can use the **notexists join** keyword pair in a **delete\_from** statement.</span></span> <span data-ttu-id="01f31-591">次の例の **delete\_from** ステートメントが効率的です。</span><span class="sxs-lookup"><span data-stu-id="01f31-591">The **delete\_from** statements in the following example are efficient.</span></span> <span data-ttu-id="01f31-592">**notexists join** 句を使用すると、**delete\_from** ステートメントが特定の行セットを削除できるようになります。</span><span class="sxs-lookup"><span data-stu-id="01f31-592">The **notexists join** clause enables the **delete\_from** statement to delete a specific set of rows.</span></span> <span data-ttu-id="01f31-593">この例では、**delete\_from** ステートメントが子の注文明細行の行がない親の注文ヘッダー行をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="01f31-593">In this example, the **delete\_from** statement removes all parent-order header rows that there are no child-order line rows for.</span></span> <span data-ttu-id="01f31-594">また、**exists join** 句を **delete\_from** ステートメント上で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="01f31-594">You can also use the **exists join** clause on the **delete\_from** statement.</span></span>

```X++
static void DeleteFromNotexists3bJob(Args _args)
{
    GmTabOrderHeader tabOHeader;
    GmTabOrderLine tabOLine;
    AddressState tabAddressState;
    str 127 sOH_Info;
    str 127 sOL_Data;
    int64 i64OHRecId;
    delete_from tabOLine;
    delete_from tabOHeader;
    // Inserts into parent table.
    sOH_Info = "Albert needs tires.";
    insert_recordset tabOHeader
        (OH_Info)
        select firstOnly sOH_Info from tabAddressState;
    sOH_Info = "Benson wants plastic.";
    insert_recordset tabOHeader
        (OH_Info)
        select firstOnly sOH_Info from tabAddressState;
    // Obtain a OrderHeader RecId,
    // use it to insert one child row.
    sOL_Data = "4 re-treads.";
    while select firstOnly tabOHeader
        order by OH_Info
        where tabOHeader .OH_Info like "A*"
    {
        i64OHRecId = tabOHeader .RecId;
        insert_recordset tabOLine
            (OL_Data ,OrderHeaderRecId)
            select firstOnly
                sOL_Data ,i64OHRecId
                from tabAddressState;
        break;
    }
    // Before the delete notexists.
    // Display all parent, and then all child rows.
    while select tabOHeader
        order by OH_Info
    {
        info(strFmt(
            "Before: OHeader:  OH_Info==%1 , RecId==%2"
            ,tabOHeader .OH_Info ,tabOHeader .RecId
            ));
    }
    while select tabOLine
        order by OL_Data
    {
        info(strFmt(
            "Before: OLine:  OL_Data==%1 , OrderHeaderRecId==%2"
            ,tabOLine .OL_Data ,tabOLine .OrderHeaderRecId
            ));
    }
    // Delete_From NotExists Join, to remove from the
    // parent table all order headers without children.
    delete_from tabOHeader
        notexists join tabOLine
            where tabOHeader .RecId ==
                tabOLine .OrderHeaderRecId;
    info(strFmt
        ("%1 is the number of childless OHeader records deleted."
        ,tabOHeader.rowCount()));
    // After the delete notexists.
    // Display all parent, and then all child rows.
    info("- - - - - - - - - - - - - - -");
    while select tabOHeader
        order by OH_Info
    {
        info(strFmt(
            "After: OHeader:  OH_Info==%1 , RecId==%2"
            ,tabOHeader .OH_Info ,tabOHeader .RecId
            ));
    }
    while select tabOLine
        order by OL_Data
    {
        info(strFmt(
            "After: OLine:  OL_Data==%1 , OrderHeaderRecId==%2"
            ,tabOLine .OL_Data ,tabOLine .OrderHeaderRecId
            ));
    }

/**************  Actual Infolog output
Message (12:54:14 pm)
Before: OHeader:  OH_Info==Albert needs tires. , RecId==5637144608
Before: OHeader:  OH_Info==Benson wants plastic. , RecId==5637144609
Before: OLine:  OL_Data==4 re-treads. , OrderHeaderRecId==5637144608
1 is the number of childless OHeader records deleted.
- - - - - - - - - - - - - - -
After: OHeader:  OH_Info==Albert needs tires. , RecId==5637144608
After: OLine:  OL_Data==4 re-treads. , OrderHeaderRecId==5637144608
**************/
}
```

## <a name="maintain-fast-sql-operations"></a><span data-ttu-id="01f31-595">高速な SQL 操作の管理</span><span class="sxs-lookup"><span data-stu-id="01f31-595">Maintain fast SQL operations</span></span>
<span data-ttu-id="01f31-596">レコード セット ベースの操作をより低速のレコードごとの操作に変換できる状況があります。</span><span class="sxs-lookup"><span data-stu-id="01f31-596">There are situations where record set–based operations can be converted to slower record-by-record operations.</span></span> <span data-ttu-id="01f31-597">次の情報は、これらの状況を識別します。</span><span class="sxs-lookup"><span data-stu-id="01f31-597">The following information identifies these situations.</span></span>


### <a name="non-sql-tables"></a><span data-ttu-id="01f31-598">非 SQL テーブル</span><span class="sxs-lookup"><span data-stu-id="01f31-598">Non-SQL tables</span></span>

| <span data-ttu-id="01f31-599">工程</span><span class="sxs-lookup"><span data-stu-id="01f31-599">Operation</span></span> | <span data-ttu-id="01f31-600">変換可能</span><span class="sxs-lookup"><span data-stu-id="01f31-600">Can be converted</span></span> |
|---|---|
|<span data-ttu-id="01f31-601">DELETE_FROM</span><span class="sxs-lookup"><span data-stu-id="01f31-601">DELETE_FROM</span></span>|<span data-ttu-id="01f31-602">有</span><span class="sxs-lookup"><span data-stu-id="01f31-602">Yes</span></span>|
|<span data-ttu-id="01f31-603">UPDATE_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-603">UPDATE_RECORDSET</span></span>|<span data-ttu-id="01f31-604">有</span><span class="sxs-lookup"><span data-stu-id="01f31-604">Yes</span></span>|
|<span data-ttu-id="01f31-605">INSERT_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-605">INSERT_RECORDSET</span></span>|<span data-ttu-id="01f31-606">有</span><span class="sxs-lookup"><span data-stu-id="01f31-606">Yes</span></span>|
|<span data-ttu-id="01f31-607">ARRAY_INSERT</span><span class="sxs-lookup"><span data-stu-id="01f31-607">ARRAY_INSERT</span></span>|<span data-ttu-id="01f31-608">有</span><span class="sxs-lookup"><span data-stu-id="01f31-608">Yes</span></span>|
|<span data-ttu-id="01f31-609">オーバーライドにこの設定を使用する</span><span class="sxs-lookup"><span data-stu-id="01f31-609">Use this setting for overrides</span></span>|<span data-ttu-id="01f31-610">該当なし</span><span class="sxs-lookup"><span data-stu-id="01f31-610">Not applicable</span></span>|

### <a name="delete-actions"></a><span data-ttu-id="01f31-611">アクションの削除</span><span class="sxs-lookup"><span data-stu-id="01f31-611">Delete actions</span></span>

| <span data-ttu-id="01f31-612">工程</span><span class="sxs-lookup"><span data-stu-id="01f31-612">Operation</span></span> | <span data-ttu-id="01f31-613">変換可能</span><span class="sxs-lookup"><span data-stu-id="01f31-613">Can be converted</span></span> |
|---|---|
|<span data-ttu-id="01f31-614">DELETE_FROM</span><span class="sxs-lookup"><span data-stu-id="01f31-614">DELETE_FROM</span></span>|<span data-ttu-id="01f31-615">有</span><span class="sxs-lookup"><span data-stu-id="01f31-615">Yes</span></span>|
|<span data-ttu-id="01f31-616">UPDATE_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-616">UPDATE_RECORDSET</span></span>|<span data-ttu-id="01f31-617">無</span><span class="sxs-lookup"><span data-stu-id="01f31-617">No</span></span>|
|<span data-ttu-id="01f31-618">INSERT_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-618">INSERT_RECORDSET</span></span>|<span data-ttu-id="01f31-619">無</span><span class="sxs-lookup"><span data-stu-id="01f31-619">No</span></span>|
|<span data-ttu-id="01f31-620">ARRAY_INSERT</span><span class="sxs-lookup"><span data-stu-id="01f31-620">ARRAY_INSERT</span></span>|<span data-ttu-id="01f31-621">無</span><span class="sxs-lookup"><span data-stu-id="01f31-621">No</span></span>|
|<span data-ttu-id="01f31-622">オーバーライドにこの設定を使用する</span><span class="sxs-lookup"><span data-stu-id="01f31-622">Use this setting for overrides</span></span>|<span data-ttu-id="01f31-623">**skipDeleteActions**</span><span class="sxs-lookup"><span data-stu-id="01f31-623">**skipDeleteActions**</span></span>|

### <a name="the-database-log-is-enabled"></a><span data-ttu-id="01f31-624">データベース ログが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="01f31-624">The database log is enabled.</span></span>

| <span data-ttu-id="01f31-625">工程</span><span class="sxs-lookup"><span data-stu-id="01f31-625">Operation</span></span> | <span data-ttu-id="01f31-626">変換可能</span><span class="sxs-lookup"><span data-stu-id="01f31-626">Can be converted</span></span> |
|---|---|
|<span data-ttu-id="01f31-627">DELETE_FROM</span><span class="sxs-lookup"><span data-stu-id="01f31-627">DELETE_FROM</span></span>|<span data-ttu-id="01f31-628">有</span><span class="sxs-lookup"><span data-stu-id="01f31-628">Yes</span></span>|
|<span data-ttu-id="01f31-629">UPDATE_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-629">UPDATE_RECORDSET</span></span>|<span data-ttu-id="01f31-630">有</span><span class="sxs-lookup"><span data-stu-id="01f31-630">Yes</span></span>|
|<span data-ttu-id="01f31-631">INSERT_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-631">INSERT_RECORDSET</span></span>|<span data-ttu-id="01f31-632">有</span><span class="sxs-lookup"><span data-stu-id="01f31-632">Yes</span></span>|
|<span data-ttu-id="01f31-633">ARRAY_INSERT</span><span class="sxs-lookup"><span data-stu-id="01f31-633">ARRAY_INSERT</span></span>|<span data-ttu-id="01f31-634">無</span><span class="sxs-lookup"><span data-stu-id="01f31-634">No</span></span>|
|<span data-ttu-id="01f31-635">オーバーライドにこの設定を使用する</span><span class="sxs-lookup"><span data-stu-id="01f31-635">Use this setting for overrides</span></span>|<span data-ttu-id="01f31-636">**skipDatabaseLog**</span><span class="sxs-lookup"><span data-stu-id="01f31-636">**skipDatabaseLog**</span></span>|

### <a name="overridden-method"></a><span data-ttu-id="01f31-637">オーバーライドされたメソッド</span><span class="sxs-lookup"><span data-stu-id="01f31-637">Overridden method</span></span>

| <span data-ttu-id="01f31-638">工程</span><span class="sxs-lookup"><span data-stu-id="01f31-638">Operation</span></span> | <span data-ttu-id="01f31-639">変換可能</span><span class="sxs-lookup"><span data-stu-id="01f31-639">Can be converted</span></span> |
|---|---|
|<span data-ttu-id="01f31-640">DELETE_FROM</span><span class="sxs-lookup"><span data-stu-id="01f31-640">DELETE_FROM</span></span>|<span data-ttu-id="01f31-641">有</span><span class="sxs-lookup"><span data-stu-id="01f31-641">Yes</span></span>|
|<span data-ttu-id="01f31-642">UPDATE_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-642">UPDATE_RECORDSET</span></span>|<span data-ttu-id="01f31-643">有</span><span class="sxs-lookup"><span data-stu-id="01f31-643">Yes</span></span>|
|<span data-ttu-id="01f31-644">INSERT_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-644">INSERT_RECORDSET</span></span>|<span data-ttu-id="01f31-645">有</span><span class="sxs-lookup"><span data-stu-id="01f31-645">Yes</span></span>|
|<span data-ttu-id="01f31-646">ARRAY_INSERT</span><span class="sxs-lookup"><span data-stu-id="01f31-646">ARRAY_INSERT</span></span>|<span data-ttu-id="01f31-647">有</span><span class="sxs-lookup"><span data-stu-id="01f31-647">Yes</span></span>|
|<span data-ttu-id="01f31-648">オーバーライドにこの設定を使用する</span><span class="sxs-lookup"><span data-stu-id="01f31-648">Use this setting for overrides</span></span>|<span data-ttu-id="01f31-649">**skipDataMethods**</span><span class="sxs-lookup"><span data-stu-id="01f31-649">**skipDataMethods**</span></span>|

### <a name="alerts-are-set-up-for-the-table"></a><span data-ttu-id="01f31-650">警告はテーブルの設定をします。</span><span class="sxs-lookup"><span data-stu-id="01f31-650">Alerts are set up for the table.</span></span>

| <span data-ttu-id="01f31-651">工程</span><span class="sxs-lookup"><span data-stu-id="01f31-651">Operation</span></span> | <span data-ttu-id="01f31-652">変換可能</span><span class="sxs-lookup"><span data-stu-id="01f31-652">Can be converted</span></span> |
|---|---|
|<span data-ttu-id="01f31-653">DELETE_FROM</span><span class="sxs-lookup"><span data-stu-id="01f31-653">DELETE_FROM</span></span>|<span data-ttu-id="01f31-654">有</span><span class="sxs-lookup"><span data-stu-id="01f31-654">Yes</span></span>|
|<span data-ttu-id="01f31-655">UPDATE_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-655">UPDATE_RECORDSET</span></span>|<span data-ttu-id="01f31-656">有</span><span class="sxs-lookup"><span data-stu-id="01f31-656">Yes</span></span>|
|<span data-ttu-id="01f31-657">INSERT_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-657">INSERT_RECORDSET</span></span>|<span data-ttu-id="01f31-658">有</span><span class="sxs-lookup"><span data-stu-id="01f31-658">Yes</span></span>|
|<span data-ttu-id="01f31-659">ARRAY_INSERT</span><span class="sxs-lookup"><span data-stu-id="01f31-659">ARRAY_INSERT</span></span>|<span data-ttu-id="01f31-660">無</span><span class="sxs-lookup"><span data-stu-id="01f31-660">No</span></span>|
|<span data-ttu-id="01f31-661">オーバーライドにこの設定を使用する</span><span class="sxs-lookup"><span data-stu-id="01f31-661">Use this setting for overrides</span></span>|<span data-ttu-id="01f31-662">**skipEvents**</span><span class="sxs-lookup"><span data-stu-id="01f31-662">**skipEvents**</span></span>|

### <a name="the-validtimestatefieldtype-property-on-a-table-isnt-equal-to-none"></a><span data-ttu-id="01f31-663">テーブル上の ValidTimeStateFieldType プロパティは、[なし] とは等しくなりません。</span><span class="sxs-lookup"><span data-stu-id="01f31-663">The ValidTimeStateFieldType property on a table isn't equal to None.</span></span>

| <span data-ttu-id="01f31-664">工程</span><span class="sxs-lookup"><span data-stu-id="01f31-664">Operation</span></span> | <span data-ttu-id="01f31-665">変換可能</span><span class="sxs-lookup"><span data-stu-id="01f31-665">Can be converted</span></span> |
|---|---|
|<span data-ttu-id="01f31-666">DELETE_FROM</span><span class="sxs-lookup"><span data-stu-id="01f31-666">DELETE_FROM</span></span>|<span data-ttu-id="01f31-667">有</span><span class="sxs-lookup"><span data-stu-id="01f31-667">Yes</span></span>|
|<span data-ttu-id="01f31-668">UPDATE_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-668">UPDATE_RECORDSET</span></span>|<span data-ttu-id="01f31-669">有</span><span class="sxs-lookup"><span data-stu-id="01f31-669">Yes</span></span>|
|<span data-ttu-id="01f31-670">INSERT_RECORDSET</span><span class="sxs-lookup"><span data-stu-id="01f31-670">INSERT_RECORDSET</span></span>|<span data-ttu-id="01f31-671">有</span><span class="sxs-lookup"><span data-stu-id="01f31-671">Yes</span></span>|
|<span data-ttu-id="01f31-672">ARRAY_INSERT</span><span class="sxs-lookup"><span data-stu-id="01f31-672">ARRAY_INSERT</span></span>|<span data-ttu-id="01f31-673">有</span><span class="sxs-lookup"><span data-stu-id="01f31-673">Yes</span></span>|
|<span data-ttu-id="01f31-674">オーバーライドにこの設定を使用する</span><span class="sxs-lookup"><span data-stu-id="01f31-674">Use this setting for overrides</span></span>|<span data-ttu-id="01f31-675">該当なし</span><span class="sxs-lookup"><span data-stu-id="01f31-675">Not applicable</span></span>|


<span data-ttu-id="01f31-676">**オーバーライドにこの設定を使用**に対して表示される設定を使用して、パフォーマンスに悪影響を与える 1 つまたは複数の要因を明示的にスキップまたは無視します。</span><span class="sxs-lookup"><span data-stu-id="01f31-676">You can use the settings that are shown for **Use this setting for overrides** to explicitly skip or ignore one or more factors that adversely affect performance.</span></span> <span data-ttu-id="01f31-677">何らかの理由で前述の SQL 操作のひとつがレコードごとの操作にダウングレードされた場合、すべての **skip\*** 設定も無視されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-677">If, for some reason, one of the previously mentioned SQL operations is downgraded to a record-by-record operation, all the **skip\*** settings are also ignored.</span></span> <span data-ttu-id="01f31-678">たとえば、次のコードでは、コンテナーまたはメモ フィールドが myTable で定義されている場合はこの方法をスキップする必要があると明確に示されていても、myTable テーブルで**挿入**メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="01f31-678">For example, in the following code, the **insert** method on the myTable table is run, even though it's explicitly stated that this method should be skipped if a container or memo field is defined for myTable.</span></span>

```X++
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



