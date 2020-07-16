---
title: SqlDataDictionary クラス
description: このトピックでは、SqlDataDictionary クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0582ebb116bf09f00a8041b41840f6b7caf22e1e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502801"
---
# <a name="class-sqldatadictionary"></a><span data-ttu-id="95445-103">クラス SqlDataDictionary</span><span class="sxs-lookup"><span data-stu-id="95445-103">Class SqlDataDictionary</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SqlDataDictionary extends Object
```

<span data-ttu-id="95445-104">SqlDataDictionary クラスは、データ ディクショナリ保守のメソッドのコレクションを提供します。</span><span class="sxs-lookup"><span data-stu-id="95445-104">The SqlDataDictionary class provides a collection of methods for data dictionary maintenance.</span></span>

## <a name="remarks"></a><span data-ttu-id="95445-105">備考</span><span class="sxs-lookup"><span data-stu-id="95445-105">Remarks</span></span>

<span data-ttu-id="95445-106">この API には、実行時に呼び出される組み込み認証チェックがあります。</span><span class="sxs-lookup"><span data-stu-id="95445-106">This API has a built-in authorization check that is invoked at run time.</span></span> <span data-ttu-id="95445-107">開発セキュリティ キー (SysDevelopment) にアクセスせずにユーザーが SQLDataDictionary クラスのメンバーを呼び出すと、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="95445-107">Calls to members of the SQLDataDictionary class by users without access to the development security key (SysDevelopment) results in an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="95445-108">例</span><span class="sxs-lookup"><span data-stu-id="95445-108">Examples</span></span>

<span data-ttu-id="95445-109">次の例では、UserInfo テーブルがデータベースに存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="95445-109">The following example checks whether the UserInfo table exists in the database.</span></span>

```xpp
server static public void Main(Args _args) 
{ 
    SqlDataDictionary sqlDict; 
    boolean b; 
    sqlDict = new SqlDataDictionary(); 
    if (sqlDict) 
    { 
        b = sqlDict.tableExist("USERINFO"); 
        print b; 
        pause; 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="95445-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="95445-110">Methods</span></span>

| <span data-ttu-id="95445-111">方法</span><span class="sxs-lookup"><span data-stu-id="95445-111">Method</span></span>                                                                                                               | <span data-ttu-id="95445-112">説明</span><span class="sxs-lookup"><span data-stu-id="95445-112">Description</span></span>                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95445-113">public int indexCreate(\[TableId tableId\], \[IndexId indexId\])</span><span class="sxs-lookup"><span data-stu-id="95445-113">public int indexCreate(\[TableId tableId\], \[IndexId indexId\])</span></span>                                                     | <span data-ttu-id="95445-114">テーブルのインデックスを SQL データベースで作成します。</span><span class="sxs-lookup"><span data-stu-id="95445-114">Creates the indexes of a table in the SQL database.</span></span> <span data-ttu-id="95445-115">このメソッドを使用してインデックスを再作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="95445-115">You can also use this method to re-create indexes.</span></span> |
| <span data-ttu-id="95445-116">public str indexCreateDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95445-116">public str indexCreateDDL(TableId tableId)</span></span>                                                                           | <span data-ttu-id="95445-117">テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-117">Generates and returns the SQL statements needed to create the indexes of a table.</span></span>                      |
| <span data-ttu-id="95445-118">public int indexDrop(\[TableId tableId\], \[IndexId indexId\], \[boolean onlyNonUnique\])</span><span class="sxs-lookup"><span data-stu-id="95445-118">public int indexDrop(\[TableId tableId\], \[IndexId indexId\], \[boolean onlyNonUnique\])</span></span>                            | <span data-ttu-id="95445-119">テーブルのインデックスを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="95445-119">Drops the indexes of a table in the SQL database.</span></span>                                                      |
| <span data-ttu-id="95445-120">public str name(str bmsname, \[FieldId fieldId\], \[int arrayindex\])</span><span class="sxs-lookup"><span data-stu-id="95445-120">public str name(str bmsname, \[FieldId fieldId\], \[int arrayindex\])</span></span>                                                | <span data-ttu-id="95445-121">任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。</span><span class="sxs-lookup"><span data-stu-id="95445-121">Translates any object name into a valid SQL database object-name; that is, valid for the database currently connected.</span></span>        |
| <span data-ttu-id="95445-122">public int tableCreate(\[boolean indexes\], \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="95445-122">public int tableCreate(\[boolean indexes\], \[TableId tableId\])</span></span>                                                     | <span data-ttu-id="95445-123">1 つ以上のテーブルを SQL データベース内に作成します。</span><span class="sxs-lookup"><span data-stu-id="95445-123">Creates one or more  tables in the SQL database.</span></span> <span data-ttu-id="95445-124">また、インデックス用に作成するオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="95445-124">Also, provides an option to create for index.</span></span>           |
| <span data-ttu-id="95445-125">public str tableCreateDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95445-125">public str tableCreateDDL(TableId tableId)</span></span>                                                                           | <span data-ttu-id="95445-126">テーブルを作成するため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-126">Generates and returns the SQL statement to create a table.</span></span>                                             |
| <span data-ttu-id="95445-127">public int tableDrop(TableId tableId, \[boolean prompt\_before\_drop\])</span><span class="sxs-lookup"><span data-stu-id="95445-127">public int tableDrop(TableId tableId, \[boolean prompt\_before\_drop\])</span></span>                                              | <span data-ttu-id="95445-128">テーブルを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="95445-128">Drops the  table in the SQL database.</span></span>                                                                    |
| <span data-ttu-id="95445-129">public str tableDropDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95445-129">public str tableDropDDL(TableId tableId)</span></span>                                                                             | <span data-ttu-id="95445-130">テーブルをドロップするため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-130">Generates and returns the SQL statement to drop a table.</span></span>                                               |
| <span data-ttu-id="95445-131">public boolean tableEmpty(TableId tableId, \[str company\], \[boolean not\_this\_company\])</span><span class="sxs-lookup"><span data-stu-id="95445-131">public boolean tableEmpty(TableId tableId, \[str company\], \[boolean not\_this\_company\])</span></span>                          | <span data-ttu-id="95445-132">テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="95445-132">Returns true if table is not empty; otherwise false.</span></span>                                                                          |
| <span data-ttu-id="95445-133">public boolean tableExist(str sqltablename, \[boolean use\_within\_transaction\])</span><span class="sxs-lookup"><span data-stu-id="95445-133">public boolean tableExist(str sqltablename, \[boolean use\_within\_transaction\])</span></span>                                    | <span data-ttu-id="95445-134">テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="95445-134">Returns true if table exists; otherwise false.</span></span>                                                                                |
| <span data-ttu-id="95445-135">public int tableMetaData(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95445-135">public int tableMetaData(TableId tableId)</span></span>                                                                            | <span data-ttu-id="95445-136">データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。</span><span class="sxs-lookup"><span data-stu-id="95445-136">Fills the SqlDescribe table with data dictionary meta data.</span></span>                                                                   |
| <span data-ttu-id="95445-137">public int tableReindex(\[TableId tableId\], \[IndexId indexId\])</span><span class="sxs-lookup"><span data-stu-id="95445-137">public int tableReindex(\[TableId tableId\], \[IndexId indexId\])</span></span>                                                    | <span data-ttu-id="95445-138">テーブルのインデックスを更新します。</span><span class="sxs-lookup"><span data-stu-id="95445-138">Updates index for the table.</span></span>                                                                                                  |
| <span data-ttu-id="95445-139">public int tableSynchronize(TableId tableId, \[boolean update\_dict\_info\_only\], \[boolean check\_indexes\])</span><span class="sxs-lookup"><span data-stu-id="95445-139">public int tableSynchronize(TableId tableId, \[boolean update\_dict\_info\_only\], \[boolean check\_indexes\])</span></span>       | <span data-ttu-id="95445-140">テーブルと、SQL データベースのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="95445-140">Synchronizes the  table and the table of the SQL database.</span></span>                                               |
| <span data-ttu-id="95445-141">public int tableTruncate(TableId tableId, \[boolean prompt\_before\_truncate\], \[boolean truncate\_system\_table\])</span><span class="sxs-lookup"><span data-stu-id="95445-141">public int tableTruncate(TableId tableId, \[boolean prompt\_before\_truncate\], \[boolean truncate\_system\_table\])</span></span> | <span data-ttu-id="95445-142">テーブルの切り詰め</span><span class="sxs-lookup"><span data-stu-id="95445-142">Truncates the  table.</span></span>                                                                                    |
| <span data-ttu-id="95445-143">public str tableTruncateDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95445-143">public str tableTruncateDDL(TableId tableId)</span></span>                                                                         | <span data-ttu-id="95445-144">テーブルを切り詰めるため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-144">Generates and returns a SQL statement to truncate a table.</span></span>                                             |
| <span data-ttu-id="95445-145">::public static int synchronize(\[boolean synchronize\_all\])</span><span class="sxs-lookup"><span data-stu-id="95445-145">::public static int synchronize(\[boolean synchronize\_all\])</span></span>                                                        | <span data-ttu-id="95445-146">データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。</span><span class="sxs-lookup"><span data-stu-id="95445-146">Synchronizes the  data dictionary and the data dictionary of the SQL database.</span></span>                           |
| <span data-ttu-id="95445-147">public void new()</span><span class="sxs-lookup"><span data-stu-id="95445-147">public void new()</span></span>                                                                                                    | <span data-ttu-id="95445-148">SqlDataDictionary クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="95445-148">Initializes a new instance of the SqlDataDictionary class.</span></span>                                                                    |
| <span data-ttu-id="95445-149">public void tableDelete(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95445-149">public void tableDelete(TableId tableId)</span></span>                                                                             | <span data-ttu-id="95445-150">SQL データベースでテーブルを削除します。</span><span class="sxs-lookup"><span data-stu-id="95445-150">Deletes the  table in the SQL database.</span></span>                                                                  |

## <a name="method-indexcreate"></a><span data-ttu-id="95445-151">メソッド indexCreate</span><span class="sxs-lookup"><span data-stu-id="95445-151">Method indexCreate</span></span>

<span data-ttu-id="95445-152">テーブルのインデックスを SQL データベースで作成します。</span><span class="sxs-lookup"><span data-stu-id="95445-152">Creates the indexes of a table in the SQL database.</span></span> <span data-ttu-id="95445-153">このメソッドを使用してインデックスを再作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="95445-153">You can also use this method to re-create indexes.</span></span>

```xpp
public int indexCreate([TableId tableId], [IndexId indexId])
```

### <a name="parameters---indexcreate"></a><span data-ttu-id="95445-154">パラメーター - indexCreate</span><span class="sxs-lookup"><span data-stu-id="95445-154">Parameters - indexCreate</span></span>

<span data-ttu-id="95445-155">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-155">tableId</span></span>  
<span data-ttu-id="95445-156">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-156">The index handle (0 for all); optional.</span></span>

<!-- -->

<span data-ttu-id="95445-157">indexId</span><span class="sxs-lookup"><span data-stu-id="95445-157">indexId</span></span>  
<span data-ttu-id="95445-158">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-158">The index handle (0 for all); optional.</span></span>

### <a name="return-value---indexcreate"></a><span data-ttu-id="95445-159">戻り値 - indexCreate</span><span class="sxs-lookup"><span data-stu-id="95445-159">Return Value - indexCreate</span></span>

<span data-ttu-id="95445-160">メソッドが成功した場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="95445-160">0 if the method succeeds.</span></span>

### <a name="remarks---indexcreate"></a><span data-ttu-id="95445-161">備考 - indexCreate</span><span class="sxs-lookup"><span data-stu-id="95445-161">Remarks - indexCreate</span></span>

<span data-ttu-id="95445-162">このメソッドを使用すると、インデックスを再作成できます。</span><span class="sxs-lookup"><span data-stu-id="95445-162">This method can be used to re-create indexes.</span></span> <span data-ttu-id="95445-163">パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="95445-163">Use 0 for the parameters to indicate all tables or indexes.</span></span>

### <a name="examples---indexcreate"></a><span data-ttu-id="95445-164">例 - indexCreate</span><span class="sxs-lookup"><span data-stu-id="95445-164">Examples - indexCreate</span></span>

```xpp
{ 
    SqlDataDictionary DD = new SqlDataDictionary(); 
    DD.indexCreate(TableName2Id("Address")); 
}
```

## <a name="method-indexcreateddl"></a><span data-ttu-id="95445-165">メソッド indexCreateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-165">Method indexCreateDDL</span></span>

<span data-ttu-id="95445-166">テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-166">Generates and returns the SQL statements needed to create the indexes of a table.</span></span>

```xpp
public str indexCreateDDL(TableId tableId)
```

### <a name="parameters---indexcreateddl"></a><span data-ttu-id="95445-167">パラメーター - indexCreateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-167">Parameters - indexCreateDDL</span></span>

<span data-ttu-id="95445-168">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-168">tableId</span></span>  
<span data-ttu-id="95445-169">インデックスを作成する必要があるテーブル ハンドル。</span><span class="sxs-lookup"><span data-stu-id="95445-169">The table handle that the index should be created for.</span></span>

### <a name="return-value---indexcreateddl"></a><span data-ttu-id="95445-170">戻り値 - indexCreateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-170">Return Value - indexCreateDDL</span></span>

<span data-ttu-id="95445-171">テーブルのインデックスを作成するための SQL ステートメントを返します。</span><span class="sxs-lookup"><span data-stu-id="95445-171">Returns SQL statements to create the indexes of the  table.</span></span>

## <a name="method-indexdrop"></a><span data-ttu-id="95445-172">メソッド indexDrop</span><span class="sxs-lookup"><span data-stu-id="95445-172">Method indexDrop</span></span>

<span data-ttu-id="95445-173">テーブルのインデックスを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="95445-173">Drops the indexes of a table in the SQL database.</span></span>

```xpp
public int indexDrop([TableId tableId], [IndexId indexId], [boolean onlyNonUnique])
```

### <a name="parameters---indexdrop"></a><span data-ttu-id="95445-174">パラメーター - indexDrop</span><span class="sxs-lookup"><span data-stu-id="95445-174">Parameters - indexDrop</span></span>

<span data-ttu-id="95445-175">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-175">tableId</span></span>  

<!-- -->

<span data-ttu-id="95445-176">indexId</span><span class="sxs-lookup"><span data-stu-id="95445-176">indexId</span></span>  

<!-- -->

<span data-ttu-id="95445-177">onlyNonUnique</span><span class="sxs-lookup"><span data-stu-id="95445-177">onlyNonUnique</span></span>  

### <a name="return-value---indexdrop"></a><span data-ttu-id="95445-178">戻り値 - indexDrop</span><span class="sxs-lookup"><span data-stu-id="95445-178">Return Value - indexDrop</span></span>

<span data-ttu-id="95445-179">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="95445-179">Zero if the method succeeds.</span></span>

### <a name="remarks---indexdrop"></a><span data-ttu-id="95445-180">備考 - indexDrop</span><span class="sxs-lookup"><span data-stu-id="95445-180">Remarks - indexDrop</span></span>

<span data-ttu-id="95445-181">パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="95445-181">Use 0 for the parameters to indicate all tables or indexes.</span></span>

### <a name="examples---indexdrop"></a><span data-ttu-id="95445-182">例 - indexDrop</span><span class="sxs-lookup"><span data-stu-id="95445-182">Examples - indexDrop</span></span>

```xpp
{ 
    SqlDataDictionary DD = new SqlDataDictionary(); 
    DD.indexDrop(TableName2Id("Address")); 
}
```

## <a name="method-name"></a><span data-ttu-id="95445-183">メソッド名</span><span class="sxs-lookup"><span data-stu-id="95445-183">Method name</span></span>

<span data-ttu-id="95445-184">任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。</span><span class="sxs-lookup"><span data-stu-id="95445-184">Translates any object name into a valid SQL database object-name; that is, valid for the database currently connected.</span></span>

```xpp
public str name(str bmsname, [FieldId fieldId], [int arrayindex])
```

### <a name="parameters---name"></a><span data-ttu-id="95445-185">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="95445-185">Parameters - name</span></span>

<span data-ttu-id="95445-186">bmsname</span><span class="sxs-lookup"><span data-stu-id="95445-186">bmsname</span></span>  
<span data-ttu-id="95445-187">フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-187">A field index (0 for not applicable), that is, an array field's arrayindex'th entry, such as Dimension\[2\]; optional.</span></span>

<!-- -->

<span data-ttu-id="95445-188">fieldId</span><span class="sxs-lookup"><span data-stu-id="95445-188">fieldId</span></span>  
<span data-ttu-id="95445-189">フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-189">A field index (0 for not applicable), that is, an array field's arrayindex'th entry, such as Dimension\[2\]; optional.</span></span>

<!-- -->

<span data-ttu-id="95445-190">arrayindex</span><span class="sxs-lookup"><span data-stu-id="95445-190">arrayindex</span></span>  
<span data-ttu-id="95445-191">フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-191">A field index (0 for not applicable), that is, an array field's arrayindex'th entry, such as Dimension\[2\]; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="95445-192">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="95445-192">Return Value - name</span></span>

<span data-ttu-id="95445-193">有効なオブジェクト名。</span><span class="sxs-lookup"><span data-stu-id="95445-193">The valid object name.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="95445-194">備考 - name</span><span class="sxs-lookup"><span data-stu-id="95445-194">Remarks - name</span></span>

<span data-ttu-id="95445-195">名前は切り捨てられる可能性があるため、固有のオブジェクト識別子が指定される場合があります。</span><span class="sxs-lookup"><span data-stu-id="95445-195">Because names may be truncated, a unique object identifier may be supplied.</span></span> <span data-ttu-id="95445-196">また、3 番目のパラメータは、メソッドが配列フィールドの個別の SQL フィールド名を返すことを可能にします。</span><span class="sxs-lookup"><span data-stu-id="95445-196">Also, a third parameter enables the method to return discrete SQL field names for  array fields.</span></span>

## <a name="method-tablecreate"></a><span data-ttu-id="95445-197">メソッド tableCreate</span><span class="sxs-lookup"><span data-stu-id="95445-197">Method tableCreate</span></span>

<span data-ttu-id="95445-198">1 つ以上のテーブルを SQL データベース内に作成します。</span><span class="sxs-lookup"><span data-stu-id="95445-198">Creates one or more  tables in the SQL database.</span></span> <span data-ttu-id="95445-199">また、インデックス用に作成するオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="95445-199">Also, provides an option to create for index.</span></span>

```xpp
public int tableCreate([boolean indexes], [TableId tableId])
```

### <a name="parameters---tablecreate"></a><span data-ttu-id="95445-200">パラメーター - tableCreate</span><span class="sxs-lookup"><span data-stu-id="95445-200">Parameters - tableCreate</span></span>

<span data-ttu-id="95445-201">indexes</span><span class="sxs-lookup"><span data-stu-id="95445-201">indexes</span></span>  
<span data-ttu-id="95445-202">テーブル ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-202">The table handle (0 for all); optional.</span></span>

<!-- -->

<span data-ttu-id="95445-203">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-203">tableId</span></span>  
<span data-ttu-id="95445-204">テーブル ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-204">The table handle (0 for all); optional.</span></span>

### <a name="return-value---tablecreate"></a><span data-ttu-id="95445-205">戻り値 - tableCreate</span><span class="sxs-lookup"><span data-stu-id="95445-205">Return Value - tableCreate</span></span>

<span data-ttu-id="95445-206">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="95445-206">Zero if the method succeeds.</span></span>

### <a name="remarks---tablecreate"></a><span data-ttu-id="95445-207">備考 - tableCreate</span><span class="sxs-lookup"><span data-stu-id="95445-207">Remarks - tableCreate</span></span>

<span data-ttu-id="95445-208">低レベルのメンテナンスにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="95445-208">Used for low-level maintenance only.</span></span>

### <a name="examples---tablecreate"></a><span data-ttu-id="95445-209">例 - tableCreate</span><span class="sxs-lookup"><span data-stu-id="95445-209">Examples - tableCreate</span></span>

```xpp
{ 
    SqlDataDictionary DD = new SqlDataDictionary(); 
    DD.tableCreate(TableName2Id("Address")); 
}
```

## <a name="method-tablecreateddl"></a><span data-ttu-id="95445-210">メソッド tableCreateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-210">Method tableCreateDDL</span></span>

<span data-ttu-id="95445-211">テーブルを作成するため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-211">Generates and returns the SQL statement to create a table.</span></span>

```xpp
public str tableCreateDDL(TableId tableId)
```

### <a name="parameters---tablecreateddl"></a><span data-ttu-id="95445-212">パラメーター - tableCreateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-212">Parameters - tableCreateDDL</span></span>

<span data-ttu-id="95445-213">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-213">tableId</span></span>  
<span data-ttu-id="95445-214">作成するテーブルのテーブル ハンドルです。</span><span class="sxs-lookup"><span data-stu-id="95445-214">The table handle of the table to be created.</span></span>

### <a name="return-value---tablecreateddl"></a><span data-ttu-id="95445-215">戻り値 - tableCreateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-215">Return Value - tableCreateDDL</span></span>

<span data-ttu-id="95445-216">テーブルを作成する SQL ステートメント。</span><span class="sxs-lookup"><span data-stu-id="95445-216">The SQL statement to create a table.</span></span>

## <a name="method-tabledrop"></a><span data-ttu-id="95445-217">メソッド tableDrop</span><span class="sxs-lookup"><span data-stu-id="95445-217">Method tableDrop</span></span>

<span data-ttu-id="95445-218">テーブルを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="95445-218">Drops the  table in the SQL database.</span></span>

```xpp
public int tableDrop(TableId tableId, [boolean prompt_before_drop])
```

### <a name="parameters---tabledrop"></a><span data-ttu-id="95445-219">パラメーター - tableDrop</span><span class="sxs-lookup"><span data-stu-id="95445-219">Parameters - tableDrop</span></span>

<span data-ttu-id="95445-220">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-220">tableId</span></span>  
<span data-ttu-id="95445-221">テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-221">A boolean flag that determines whether to ask user before dropping the table; optional.</span></span> <span data-ttu-id="95445-222">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="95445-222">By default, true.</span></span>

<!-- -->

<span data-ttu-id="95445-223">prompt\_before\_drop</span><span class="sxs-lookup"><span data-stu-id="95445-223">prompt\_before\_drop</span></span>  
<span data-ttu-id="95445-224">テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-224">A boolean flag that determines whether to ask user before dropping the table; optional.</span></span> <span data-ttu-id="95445-225">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="95445-225">By default, true.</span></span>

### <a name="return-value---tabledrop"></a><span data-ttu-id="95445-226">戻り値 - tableDrop</span><span class="sxs-lookup"><span data-stu-id="95445-226">Return Value - tableDrop</span></span>

<span data-ttu-id="95445-227">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="95445-227">Zero if the method succeeds.</span></span>

## <a name="method-tabledropddl"></a><span data-ttu-id="95445-228">メソッド tableDropDDL</span><span class="sxs-lookup"><span data-stu-id="95445-228">Method tableDropDDL</span></span>

<span data-ttu-id="95445-229">テーブルをドロップするため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-229">Generates and returns the SQL statement to drop a table.</span></span>

```xpp
public str tableDropDDL(TableId tableId)
```

### <a name="parameters---tabledropddl"></a><span data-ttu-id="95445-230">パラメーター - tableDropDDL</span><span class="sxs-lookup"><span data-stu-id="95445-230">Parameters - tableDropDDL</span></span>

<span data-ttu-id="95445-231">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-231">tableId</span></span>  
<span data-ttu-id="95445-232">削除するテーブル。</span><span class="sxs-lookup"><span data-stu-id="95445-232">The table to be dropped.</span></span>

### <a name="return-value---tabledropddl"></a><span data-ttu-id="95445-233">戻り値 - tableDropDDL</span><span class="sxs-lookup"><span data-stu-id="95445-233">Return Value - tableDropDDL</span></span>

<span data-ttu-id="95445-234">指定されたテーブルを削除する SQL ステートメント。</span><span class="sxs-lookup"><span data-stu-id="95445-234">The SQL statement that drops the specified  table.</span></span>

## <a name="method-tableempty"></a><span data-ttu-id="95445-235">メソッド tableEmpty</span><span class="sxs-lookup"><span data-stu-id="95445-235">Method tableEmpty</span></span>

<span data-ttu-id="95445-236">テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="95445-236">Returns true if table is not empty; otherwise false.</span></span>

```xpp
public boolean tableEmpty(TableId tableId, [str company], [boolean not_this_company])
```

### <a name="parameters---tableempty"></a><span data-ttu-id="95445-237">パラメーター - tableEmpty</span><span class="sxs-lookup"><span data-stu-id="95445-237">Parameters - tableEmpty</span></span>

<span data-ttu-id="95445-238">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-238">tableId</span></span>  
<span data-ttu-id="95445-239">true の場合、クエリーから会社に属するレコードを除外します: オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-239">If true excludes records that belongs to the company from the query; optional.</span></span> <span data-ttu-id="95445-240">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-240">By default, false.</span></span>

<!-- -->

<span data-ttu-id="95445-241">会社</span><span class="sxs-lookup"><span data-stu-id="95445-241">company</span></span>  
<span data-ttu-id="95445-242">true の場合、クエリーから会社に属するレコードを除外します: オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-242">If true excludes records that belongs to the company from the query; optional.</span></span> <span data-ttu-id="95445-243">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-243">By default, false.</span></span>

<!-- -->

<span data-ttu-id="95445-244">not\_this\_company</span><span class="sxs-lookup"><span data-stu-id="95445-244">not\_this\_company</span></span>  
<span data-ttu-id="95445-245">true の場合、クエリーから会社に属するレコードを除外します: オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-245">If true excludes records that belongs to the company from the query; optional.</span></span> <span data-ttu-id="95445-246">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-246">By default, false.</span></span>

### <a name="return-value---tableempty"></a><span data-ttu-id="95445-247">戻り値 - tableEmpty</span><span class="sxs-lookup"><span data-stu-id="95445-247">Return Value - tableEmpty</span></span>

<span data-ttu-id="95445-248">テーブルが空の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="95445-248">true if the table empty; otherwise, false.</span></span>

## <a name="method-tableexist"></a><span data-ttu-id="95445-249">メソッド tableExist</span><span class="sxs-lookup"><span data-stu-id="95445-249">Method tableExist</span></span>

<span data-ttu-id="95445-250">テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="95445-250">Returns true if table exists; otherwise false.</span></span>

```xpp
public boolean tableExist(str sqltablename, [boolean use_within_transaction])
```

### <a name="parameters---tableexist"></a><span data-ttu-id="95445-251">パラメーター - tableExist</span><span class="sxs-lookup"><span data-stu-id="95445-251">Parameters - tableExist</span></span>

<span data-ttu-id="95445-252">sqltablename</span><span class="sxs-lookup"><span data-stu-id="95445-252">sqltablename</span></span>  
<span data-ttu-id="95445-253">トランザクションを使用するかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-253">A boolean flag that determines whether transactions are to be used; optional.</span></span> <span data-ttu-id="95445-254">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-254">By default, false.</span></span>

<!-- -->

<span data-ttu-id="95445-255">use\_within\_transaction</span><span class="sxs-lookup"><span data-stu-id="95445-255">use\_within\_transaction</span></span>  
<span data-ttu-id="95445-256">トランザクションを使用するかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-256">A boolean flag that determines whether transactions are to be used; optional.</span></span> <span data-ttu-id="95445-257">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-257">By default, false.</span></span>

### <a name="return-value---tableexist"></a><span data-ttu-id="95445-258">戻り値 - tableExist</span><span class="sxs-lookup"><span data-stu-id="95445-258">Return Value - tableExist</span></span>

<span data-ttu-id="95445-259">テーブルが存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="95445-259">true if the table exists; otherwise, false.</span></span>

## <a name="method-tablemetadata"></a><span data-ttu-id="95445-260">メソッド tableMetaData</span><span class="sxs-lookup"><span data-stu-id="95445-260">Method tableMetaData</span></span>

<span data-ttu-id="95445-261">データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。</span><span class="sxs-lookup"><span data-stu-id="95445-261">Fills the SqlDescribe table with data dictionary meta data.</span></span>

```xpp
public int tableMetaData(TableId tableId)
```

### <a name="parameters---tablemetadata"></a><span data-ttu-id="95445-262">パラメーター - tableMetaData</span><span class="sxs-lookup"><span data-stu-id="95445-262">Parameters - tableMetaData</span></span>

<span data-ttu-id="95445-263">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-263">tableId</span></span>  
<span data-ttu-id="95445-264">テーブル ハンドル。</span><span class="sxs-lookup"><span data-stu-id="95445-264">The table handle.</span></span>

### <a name="return-value---tablemetadata"></a><span data-ttu-id="95445-265">戻り値 - tableMetaData</span><span class="sxs-lookup"><span data-stu-id="95445-265">Return Value - tableMetaData</span></span>

<span data-ttu-id="95445-266">メソッドが成功した場合は true。</span><span class="sxs-lookup"><span data-stu-id="95445-266">true if the method succeeds.</span></span>

## <a name="method-tablereindex"></a><span data-ttu-id="95445-267">メソッド tableReindex</span><span class="sxs-lookup"><span data-stu-id="95445-267">Method tableReindex</span></span>

<span data-ttu-id="95445-268">テーブルのインデックスを更新します。</span><span class="sxs-lookup"><span data-stu-id="95445-268">Updates index for the table.</span></span>

```xpp
public int tableReindex([TableId tableId], [IndexId indexId])
```

### <a name="parameters---tablereindex"></a><span data-ttu-id="95445-269">パラメーター - tableReindex</span><span class="sxs-lookup"><span data-stu-id="95445-269">Parameters - tableReindex</span></span>

<span data-ttu-id="95445-270">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-270">tableId</span></span>  
<span data-ttu-id="95445-271">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-271">The index handle (0 for all); optional.</span></span> <span data-ttu-id="95445-272">既定では 0 です。</span><span class="sxs-lookup"><span data-stu-id="95445-272">By default, 0.</span></span>

<!-- -->

<span data-ttu-id="95445-273">indexId</span><span class="sxs-lookup"><span data-stu-id="95445-273">indexId</span></span>  
<span data-ttu-id="95445-274">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="95445-274">The index handle (0 for all); optional.</span></span> <span data-ttu-id="95445-275">既定では 0 です。</span><span class="sxs-lookup"><span data-stu-id="95445-275">By default, 0.</span></span>

### <a name="return-value---tablereindex"></a><span data-ttu-id="95445-276">戻り値 - tableReindex</span><span class="sxs-lookup"><span data-stu-id="95445-276">Return Value - tableReindex</span></span>

<span data-ttu-id="95445-277">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="95445-277">Zero if the method succeeds.</span></span>

## <a name="method-tablesynchronize"></a><span data-ttu-id="95445-278">メソッド tableSynchronize</span><span class="sxs-lookup"><span data-stu-id="95445-278">Method tableSynchronize</span></span>

<span data-ttu-id="95445-279">テーブルと、SQL データベースのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="95445-279">Synchronizes the  table and the table of the SQL database.</span></span>

```xpp
public int tableSynchronize(TableId tableId, [boolean update_dict_info_only], [boolean check_indexes])
```

### <a name="parameters---tablesynchronize"></a><span data-ttu-id="95445-280">パラメーター - tableSynchronize</span><span class="sxs-lookup"><span data-stu-id="95445-280">Parameters - tableSynchronize</span></span>

<span data-ttu-id="95445-281">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-281">tableId</span></span>  
<span data-ttu-id="95445-282">設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。</span><span class="sxs-lookup"><span data-stu-id="95445-282">When set forces reindex of the table indexes; optional.</span></span> <span data-ttu-id="95445-283">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="95445-283">By default, true.</span></span>

<!-- -->

<span data-ttu-id="95445-284">update\_dict\_info\_only</span><span class="sxs-lookup"><span data-stu-id="95445-284">update\_dict\_info\_only</span></span>  
<span data-ttu-id="95445-285">設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。</span><span class="sxs-lookup"><span data-stu-id="95445-285">When set forces reindex of the table indexes; optional.</span></span> <span data-ttu-id="95445-286">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="95445-286">By default, true.</span></span>

<!-- -->

<span data-ttu-id="95445-287">check\_indexes</span><span class="sxs-lookup"><span data-stu-id="95445-287">check\_indexes</span></span>  
<span data-ttu-id="95445-288">設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。</span><span class="sxs-lookup"><span data-stu-id="95445-288">When set forces reindex of the table indexes; optional.</span></span> <span data-ttu-id="95445-289">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="95445-289">By default, true.</span></span>

### <a name="return-value---tablesynchronize"></a><span data-ttu-id="95445-290">返り値 - tableSynchronize</span><span class="sxs-lookup"><span data-stu-id="95445-290">Return Value - tableSynchronize</span></span>

<span data-ttu-id="95445-291">メソッドが成功した場合は true。</span><span class="sxs-lookup"><span data-stu-id="95445-291">true if the method succeeds.</span></span>

## <a name="method-tabletruncate"></a><span data-ttu-id="95445-292">メソッド tableTruncate</span><span class="sxs-lookup"><span data-stu-id="95445-292">Method tableTruncate</span></span>

<span data-ttu-id="95445-293">テーブルの切り詰め</span><span class="sxs-lookup"><span data-stu-id="95445-293">Truncates the  table.</span></span>

```xpp
public int tableTruncate(TableId tableId, [boolean prompt_before_truncate], [boolean truncate_system_table])
```

### <a name="parameters---tabletruncate"></a><span data-ttu-id="95445-294">パラメーター - tableTruncate</span><span class="sxs-lookup"><span data-stu-id="95445-294">Parameters - tableTruncate</span></span>

<span data-ttu-id="95445-295">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-295">tableId</span></span>  
<span data-ttu-id="95445-296">選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-296">A boolean flag that determines whether to truncate table in case if selected table is system; optional.</span></span> <span data-ttu-id="95445-297">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-297">By default, false.</span></span>

<!-- -->

<span data-ttu-id="95445-298">prompt\_before\_truncate</span><span class="sxs-lookup"><span data-stu-id="95445-298">prompt\_before\_truncate</span></span>  
<span data-ttu-id="95445-299">選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-299">A boolean flag that determines whether to truncate table in case if selected table is system; optional.</span></span> <span data-ttu-id="95445-300">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-300">By default, false.</span></span>

<!-- -->

<span data-ttu-id="95445-301">truncate\_system\_table</span><span class="sxs-lookup"><span data-stu-id="95445-301">truncate\_system\_table</span></span>  
<span data-ttu-id="95445-302">選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-302">A boolean flag that determines whether to truncate table in case if selected table is system; optional.</span></span> <span data-ttu-id="95445-303">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-303">By default, false.</span></span>

### <a name="return-value---tabletruncate"></a><span data-ttu-id="95445-304">戻り値 - tableTruncate</span><span class="sxs-lookup"><span data-stu-id="95445-304">Return Value - tableTruncate</span></span>

<span data-ttu-id="95445-305">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="95445-305">Zero if the method succeeds.</span></span>

## <a name="method-tabletruncateddl"></a><span data-ttu-id="95445-306">メソッド tableTruncateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-306">Method tableTruncateDDL</span></span>

<span data-ttu-id="95445-307">テーブルを切り詰めるため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="95445-307">Generates and returns a SQL statement to truncate a table.</span></span>

```xpp
public str tableTruncateDDL(TableId tableId)
```

### <a name="parameters---tabletruncateddl"></a><span data-ttu-id="95445-308">パラメーター - tableTruncateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-308">Parameters - tableTruncateDDL</span></span>

<span data-ttu-id="95445-309">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-309">tableId</span></span>  
<span data-ttu-id="95445-310">切り詰めるテーブルのテーブル ハンドルです。</span><span class="sxs-lookup"><span data-stu-id="95445-310">The table handle of the table to be truncated.</span></span>

### <a name="return-value---tabletruncateddl"></a><span data-ttu-id="95445-311">戻り値 - tableTruncateDDL</span><span class="sxs-lookup"><span data-stu-id="95445-311">Return Value - tableTruncateDDL</span></span>

<span data-ttu-id="95445-312">テーブルを切り詰める SQL ステートメント。</span><span class="sxs-lookup"><span data-stu-id="95445-312">The SQL statement to truncate the table.</span></span>

## <a name="method-synchronize"></a><span data-ttu-id="95445-313">メソッド synchronize</span><span class="sxs-lookup"><span data-stu-id="95445-313">Method synchronize</span></span>

<span data-ttu-id="95445-314">データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。</span><span class="sxs-lookup"><span data-stu-id="95445-314">Synchronizes the  data dictionary and the data dictionary of the SQL database.</span></span>

```xpp
public static int synchronize([boolean synchronize_all])
```

### <a name="parameters---synchronize"></a><span data-ttu-id="95445-315">パラメーター - synchronize</span><span class="sxs-lookup"><span data-stu-id="95445-315">Parameters - synchronize</span></span>

<span data-ttu-id="95445-316">synchronize\_all</span><span class="sxs-lookup"><span data-stu-id="95445-316">synchronize\_all</span></span>  
<span data-ttu-id="95445-317">すべてのテーブルを同期するかどうかを示すブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="95445-317">A boolean flag that determines whether to synchronize all tables; optional.</span></span> <span data-ttu-id="95445-318">True の場合、このメソッドは (カーネルによって欠陥とマークされているテーブルのみでなく) すべてのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="95445-318">If true, this method synchronizes all tables (instead of only those marked dirty by the  kernel).</span></span> <span data-ttu-id="95445-319">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="95445-319">By default, false.</span></span>

### <a name="return-value---synchronize"></a><span data-ttu-id="95445-320">戻り値 - synchronize</span><span class="sxs-lookup"><span data-stu-id="95445-320">Return Value - synchronize</span></span>

<span data-ttu-id="95445-321">同期が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="95445-321">true if synchronization was successful; otherwise false.</span></span>

## <a name="method-new"></a><span data-ttu-id="95445-322">メソッド new</span><span class="sxs-lookup"><span data-stu-id="95445-322">Method new</span></span>

<span data-ttu-id="95445-323">SqlDataDictionary クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="95445-323">Initializes a new instance of the SqlDataDictionary class.</span></span>

```xpp
public void new()
```

## <a name="method-tabledelete"></a><span data-ttu-id="95445-324">メソッド tableDelete</span><span class="sxs-lookup"><span data-stu-id="95445-324">Method tableDelete</span></span>

<span data-ttu-id="95445-325">SQL データベースでテーブルを削除します。</span><span class="sxs-lookup"><span data-stu-id="95445-325">Deletes the  table in the SQL database.</span></span>

```xpp
public void tableDelete(TableId tableId)
```

### <a name="parameters---tabledelete"></a><span data-ttu-id="95445-326">パラメーター - tableDelete</span><span class="sxs-lookup"><span data-stu-id="95445-326">Parameters - tableDelete</span></span>

<span data-ttu-id="95445-327">tableId</span><span class="sxs-lookup"><span data-stu-id="95445-327">tableId</span></span>  

