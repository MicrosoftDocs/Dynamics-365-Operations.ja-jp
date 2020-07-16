---
title: ResultSet クラス
description: このトピックでは、ResultSet クラスについて説明します。
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
ms.openlocfilehash: bc53d9eaa15cf239178f06ca142fa64c8a9effed
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502823"
---
# <a name="class-resultset"></a><span data-ttu-id="62e77-103">クラス ResultSet</span><span class="sxs-lookup"><span data-stu-id="62e77-103">Class ResultSet</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ResultSet extends Object
```

<span data-ttu-id="62e77-104">ResultSet クラスは、ステートメントを実行することによって生成されるデータ テーブルへのアクセス許可を提供します。</span><span class="sxs-lookup"><span data-stu-id="62e77-104">The ResultSet class provides access to a table of data generated by executing a Statement.</span></span>

## <a name="remarks"></a><span data-ttu-id="62e77-105">備考</span><span class="sxs-lookup"><span data-stu-id="62e77-105">Remarks</span></span>

<span data-ttu-id="62e77-106">最大可搬性については、各行内の ResultSet 列は左から右の順に読み込まれ、各列は 1 回だけ読み込まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e77-106">For maximum portability, ResultSet columns within each row should be read in left-to-right order and each column should be read only once.</span></span> <span data-ttu-id="62e77-107">ResultSet は、インスタンスを実行することによって生成されるデータ テーブルへのアクセス許可を提供します。</span><span class="sxs-lookup"><span data-stu-id="62e77-107">A ResultSet provides access to a table of data generated by executing an instance.</span></span> <span data-ttu-id="62e77-108">テーブル行は順番に取得されます。</span><span class="sxs-lookup"><span data-stu-id="62e77-108">The table rows are retrieved in sequence.</span></span> <span data-ttu-id="62e77-109">行内の列の値は任意の順序でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="62e77-109">Within a row its column values can be accessed in any order.</span></span> <span data-ttu-id="62e77-110">ResultSet は、現在のデータ行を指すカーソルを保持します。</span><span class="sxs-lookup"><span data-stu-id="62e77-110">A ResultSet maintains a cursor that points to its current row of data.</span></span> <span data-ttu-id="62e77-111">最初、カーソルは最初の行の前に配置されます。</span><span class="sxs-lookup"><span data-stu-id="62e77-111">Initially the cursor is positioned before the first row.</span></span> <span data-ttu-id="62e77-112">"next" メソッドは、次の行にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="62e77-112">The 'next' method moves the cursor to the next row.</span></span> <span data-ttu-id="62e77-113">getXX メソッドについては、アプリケーションは基になるデータを指定したタイプに変換し、適切な値を返そうとします。</span><span class="sxs-lookup"><span data-stu-id="62e77-113">For the getXX methods, the application attempts to convert the underlying data to the specified type and returns a suitable value.</span></span> <span data-ttu-id="62e77-114">getXX メソッドは、現在の行の列の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-114">The getXX methods retrieve column values for the current row.</span></span> <span data-ttu-id="62e77-115">列のインデックス番号を使用して値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-115">You retrieve values using the index number of the column.</span></span> <span data-ttu-id="62e77-116">列は、連番が 1 から振られます。</span><span class="sxs-lookup"><span data-stu-id="62e77-116">Columns are numbered from 1.</span></span> <span data-ttu-id="62e77-117">ResultSet は、そのステートメントがクローズ、再実行、または複数の結果のシーケンスから次の結果を取得されるために使用されるときに、ResultSet を作成したステートメントによって自動的に終了されます。</span><span class="sxs-lookup"><span data-stu-id="62e77-117">A ResultSet is automatically closed by the statement that generated it when that Statement is closed, re-executed, or is used to retrieve the next result from a sequence of multiple results.</span></span>

## <a name="examples"></a><span data-ttu-id="62e77-118">例</span><span class="sxs-lookup"><span data-stu-id="62e77-118">Examples</span></span>

```xpp
static void example() 
{ 
    Connection Con; 
    Statement Stmt; 
    ResultSet R; 
    SqlStatementExecutePermission perm; 
    str sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
    Con = new Connection(); 
    Stmt = Con.createStatement(); 
    perm = new SqlStatementExecutePermission(sql); 
    perm.assert(); 
    R = Stmt.executeQuery(sql); 
    while ( R.next() ) 
    { 
        print R.getString(1); 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="62e77-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="62e77-119">Methods</span></span>

| <span data-ttu-id="62e77-120">方法</span><span class="sxs-lookup"><span data-stu-id="62e77-120">Method</span></span>                                    | <span data-ttu-id="62e77-121">説明</span><span class="sxs-lookup"><span data-stu-id="62e77-121">Description</span></span>                                                                               |
|-------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="62e77-122">public boolean getBoolean(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-122">public boolean getBoolean(int ColumnID)</span></span>   | <span data-ttu-id="62e77-123">現在の行で列のブール値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-123">Retrieves the Boolean value of a column in the current row.</span></span>                               |
| <span data-ttu-id="62e77-124">public int getByte(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-124">public int getByte(int ColumnID)</span></span>          |                                                                                           |
| <span data-ttu-id="62e77-125">public Date getDate(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-125">public Date getDate(int ColumnID)</span></span>         | <span data-ttu-id="62e77-126">現在の行で列のブール値を日付値として取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-126">Retrieves the value of a column in the current row as a date value.</span></span> |
| <span data-ttu-id="62e77-127">public DateTime getDateTime(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-127">public DateTime getDateTime(int ColumnID)</span></span> |                                                                                           |
| <span data-ttu-id="62e77-128">public Guid getGuid(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-128">public Guid getGuid(int ColumnID)</span></span>         |                                                                                           |
| <span data-ttu-id="62e77-129">public int getInt(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-129">public int getInt(int ColumnID)</span></span>           | <span data-ttu-id="62e77-130">現在の行で列のブール値を整数として取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-130">Retrieves the value of a column in the current row as an integer.</span></span>                         |
| <span data-ttu-id="62e77-131">public Int64 getInt64(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-131">public Int64 getInt64(int ColumnID)</span></span>       |                                                                                           |
| <span data-ttu-id="62e77-132">public ResultSetMetaData getMetaData()</span><span class="sxs-lookup"><span data-stu-id="62e77-132">public ResultSetMetaData getMetaData()</span></span>    |                                                                                           |
| <span data-ttu-id="62e77-133">public Real getReal(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-133">public Real getReal(int ColumnID)</span></span>         | <span data-ttu-id="62e77-134">タイプ実数の値として現在の行の列の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-134">Retrieves the value of a column in the current row as a value of the type real.</span></span>           |
| <span data-ttu-id="62e77-135">public str getString(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-135">public str getString(int ColumnID)</span></span>        | <span data-ttu-id="62e77-136">現在の行で列の文字列値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-136">Gets the string value of a column in the current row.</span></span>                                     |
| <span data-ttu-id="62e77-137">public boolean next()</span><span class="sxs-lookup"><span data-stu-id="62e77-137">public boolean next()</span></span>                     | <span data-ttu-id="62e77-138">1 番目またはそれ以降の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e77-138">Selects the first or subsequent row.</span></span>                                                      |
| <span data-ttu-id="62e77-139">public boolean wasNull(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="62e77-139">public boolean wasNull(int ColumnID)</span></span>      | <span data-ttu-id="62e77-140">最後の列の読み取りが SQL NULL 値を持つかどうかを報告します。</span><span class="sxs-lookup"><span data-stu-id="62e77-140">Reports whether the last column read has the value SQL NULL.</span></span>                              |
| <span data-ttu-id="62e77-141">public void close()</span><span class="sxs-lookup"><span data-stu-id="62e77-141">public void close()</span></span>                       | <span data-ttu-id="62e77-142">オブジェクトのデータベースのリソースをすぐに解放します。</span><span class="sxs-lookup"><span data-stu-id="62e77-142">Releases the object's database resources immediately.</span></span>                                     |

## <a name="method-getboolean"></a><span data-ttu-id="62e77-143">メソッド getBoolean</span><span class="sxs-lookup"><span data-stu-id="62e77-143">Method getBoolean</span></span>

<span data-ttu-id="62e77-144">現在の行で列のブール値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-144">Retrieves the Boolean value of a column in the current row.</span></span>

```xpp
public boolean getBoolean(int ColumnID)
```

### <a name="parameters---getboolean"></a><span data-ttu-id="62e77-145">パラメーター - getBoolean</span><span class="sxs-lookup"><span data-stu-id="62e77-145">Parameters - getBoolean</span></span>

<span data-ttu-id="62e77-146">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-146">ColumnID</span></span>  
<span data-ttu-id="62e77-147">列 ID。</span><span class="sxs-lookup"><span data-stu-id="62e77-147">The column ID.</span></span>

### <a name="return-value---getboolean"></a><span data-ttu-id="62e77-148">戻り値 - getBoolean</span><span class="sxs-lookup"><span data-stu-id="62e77-148">Return Value - getBoolean</span></span>

<span data-ttu-id="62e77-149">現在の行で列の値。</span><span class="sxs-lookup"><span data-stu-id="62e77-149">The value of a column in the current row.</span></span>

## <a name="method-getbyte"></a><span data-ttu-id="62e77-150">メソッド getByte</span><span class="sxs-lookup"><span data-stu-id="62e77-150">Method getByte</span></span>

```xpp
public int getByte(int ColumnID)
```

### <a name="parameters---getbyte"></a><span data-ttu-id="62e77-151">パラメーター - getByte</span><span class="sxs-lookup"><span data-stu-id="62e77-151">Parameters - getByte</span></span>

<span data-ttu-id="62e77-152">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-152">ColumnID</span></span>  

### <a name="return-value---getbyte"></a><span data-ttu-id="62e77-153">戻り値 - getByte</span><span class="sxs-lookup"><span data-stu-id="62e77-153">Return Value - getByte</span></span>

## <a name="method-getdate"></a><span data-ttu-id="62e77-154">メソッド getDate</span><span class="sxs-lookup"><span data-stu-id="62e77-154">Method getDate</span></span>

<span data-ttu-id="62e77-155">現在の行で列のブール値を日付値として取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-155">Retrieves the value of a column in the current row as a date value.</span></span>

```xpp
public Date getDate(int ColumnID)
```

### <a name="parameters---getdate"></a><span data-ttu-id="62e77-156">パラメーター - getDate</span><span class="sxs-lookup"><span data-stu-id="62e77-156">Parameters - getDate</span></span>

<span data-ttu-id="62e77-157">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-157">ColumnID</span></span>  
<span data-ttu-id="62e77-158">列の ID。</span><span class="sxs-lookup"><span data-stu-id="62e77-158">The ID of the column.</span></span>

### <a name="return-value---getdate"></a><span data-ttu-id="62e77-159">戻り値 - getDate</span><span class="sxs-lookup"><span data-stu-id="62e77-159">Return Value - getDate</span></span>

<span data-ttu-id="62e77-160">日付。</span><span class="sxs-lookup"><span data-stu-id="62e77-160">The date.</span></span>

## <a name="method-getdatetime"></a><span data-ttu-id="62e77-161">メソッド getDateTime</span><span class="sxs-lookup"><span data-stu-id="62e77-161">Method getDateTime</span></span>

```xpp
public DateTime getDateTime(int ColumnID)
```

### <a name="parameters---getdatetime"></a><span data-ttu-id="62e77-162">パラメーター - getDateTime</span><span class="sxs-lookup"><span data-stu-id="62e77-162">Parameters - getDateTime</span></span>

<span data-ttu-id="62e77-163">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-163">ColumnID</span></span>  

### <a name="return-value---getdatetime"></a><span data-ttu-id="62e77-164">戻り値 - getDateTime</span><span class="sxs-lookup"><span data-stu-id="62e77-164">Return Value - getDateTime</span></span>

## <a name="method-getguid"></a><span data-ttu-id="62e77-165">メソッド getGuid</span><span class="sxs-lookup"><span data-stu-id="62e77-165">Method getGuid</span></span>

```xpp
public Guid getGuid(int ColumnID)
```

### <a name="parameters---getguid"></a><span data-ttu-id="62e77-166">パラメーター - getGuid</span><span class="sxs-lookup"><span data-stu-id="62e77-166">Parameters - getGuid</span></span>

<span data-ttu-id="62e77-167">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-167">ColumnID</span></span>  

### <a name="return-value---getguid"></a><span data-ttu-id="62e77-168">戻り値 - getGuid</span><span class="sxs-lookup"><span data-stu-id="62e77-168">Return Value - getGuid</span></span>

## <a name="method-getint"></a><span data-ttu-id="62e77-169">メソッド getInt</span><span class="sxs-lookup"><span data-stu-id="62e77-169">Method getInt</span></span>

<span data-ttu-id="62e77-170">現在の行で列のブール値を整数として取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-170">Retrieves the value of a column in the current row as an integer.</span></span>

```xpp
public int getInt(int ColumnID)
```

### <a name="parameters---getint"></a><span data-ttu-id="62e77-171">パラメーター - getInt</span><span class="sxs-lookup"><span data-stu-id="62e77-171">Parameters - getInt</span></span>

<span data-ttu-id="62e77-172">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-172">ColumnID</span></span>  
<span data-ttu-id="62e77-173">列 ID。</span><span class="sxs-lookup"><span data-stu-id="62e77-173">The column ID.</span></span>

### <a name="return-value---getint"></a><span data-ttu-id="62e77-174">戻り値 - getInt</span><span class="sxs-lookup"><span data-stu-id="62e77-174">Return Value - getInt</span></span>

<span data-ttu-id="62e77-175">列の整数値。</span><span class="sxs-lookup"><span data-stu-id="62e77-175">The integer value of the column.</span></span>

## <a name="method-getint64"></a><span data-ttu-id="62e77-176">メソッド getInt64</span><span class="sxs-lookup"><span data-stu-id="62e77-176">Method getInt64</span></span>

```xpp
public Int64 getInt64(int ColumnID)
```

### <a name="parameters---getint64"></a><span data-ttu-id="62e77-177">パラメーター - getInt64</span><span class="sxs-lookup"><span data-stu-id="62e77-177">Parameters - getInt64</span></span>

<span data-ttu-id="62e77-178">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-178">ColumnID</span></span>  

### <a name="return-value---getint64"></a><span data-ttu-id="62e77-179">戻り値 - getInt64</span><span class="sxs-lookup"><span data-stu-id="62e77-179">Return Value - getInt64</span></span>

## <a name="method-getmetadata"></a><span data-ttu-id="62e77-180">メソッド getMetaData</span><span class="sxs-lookup"><span data-stu-id="62e77-180">Method getMetaData</span></span>

```xpp
public ResultSetMetaData getMetaData()
```

### <a name="return-value---getmetadata"></a><span data-ttu-id="62e77-181">戻り値 - getMetaData</span><span class="sxs-lookup"><span data-stu-id="62e77-181">Return Value - getMetaData</span></span>

## <a name="method-getreal"></a><span data-ttu-id="62e77-182">メソッド getReal</span><span class="sxs-lookup"><span data-stu-id="62e77-182">Method getReal</span></span>

<span data-ttu-id="62e77-183">タイプ実数の値として現在の行の列の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-183">Retrieves the value of a column in the current row as a value of the type real.</span></span>

```xpp
public Real getReal(int ColumnID)
```

### <a name="parameters---getreal"></a><span data-ttu-id="62e77-184">パラメーター - getReal</span><span class="sxs-lookup"><span data-stu-id="62e77-184">Parameters - getReal</span></span>

<span data-ttu-id="62e77-185">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-185">ColumnID</span></span>  
<span data-ttu-id="62e77-186">列の ID。</span><span class="sxs-lookup"><span data-stu-id="62e77-186">The ID of the column.</span></span> <span data-ttu-id="62e77-187">最初の列は 1、2 番目の列は 2 などとなります。</span><span class="sxs-lookup"><span data-stu-id="62e77-187">The first column is 1, the second is 2, and so on.</span></span>

### <a name="return-value---getreal"></a><span data-ttu-id="62e77-188">戻り値 - getReal</span><span class="sxs-lookup"><span data-stu-id="62e77-188">Return Value - getReal</span></span>

### <a name="examples---getreal"></a><span data-ttu-id="62e77-189">例 - getReal</span><span class="sxs-lookup"><span data-stu-id="62e77-189">Examples - getReal</span></span>

```xpp
while ( R.next() ) 
{ 
    print R.getReal(3); 
}
```

## <a name="method-getstring"></a><span data-ttu-id="62e77-190">メソッド getString</span><span class="sxs-lookup"><span data-stu-id="62e77-190">Method getString</span></span>

<span data-ttu-id="62e77-191">現在の行で列の文字列値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62e77-191">Gets the string value of a column in the current row.</span></span>

```xpp
public str getString(int ColumnID)
```

### <a name="parameters---getstring"></a><span data-ttu-id="62e77-192">パラメーター - getString</span><span class="sxs-lookup"><span data-stu-id="62e77-192">Parameters - getString</span></span>

<span data-ttu-id="62e77-193">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-193">ColumnID</span></span>  
<span data-ttu-id="62e77-194">列 ID。</span><span class="sxs-lookup"><span data-stu-id="62e77-194">The column ID.</span></span>

### <a name="return-value---getstring"></a><span data-ttu-id="62e77-195">戻り値 - getString</span><span class="sxs-lookup"><span data-stu-id="62e77-195">Return Value - getString</span></span>

<span data-ttu-id="62e77-196">列の文字列値</span><span class="sxs-lookup"><span data-stu-id="62e77-196">The string value of the column.</span></span>

## <a name="method-next"></a><span data-ttu-id="62e77-197">メソッド next</span><span class="sxs-lookup"><span data-stu-id="62e77-197">Method next</span></span>

<span data-ttu-id="62e77-198">1 番目またはそれ以降の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e77-198">Selects the first or subsequent row.</span></span>

```xpp
public boolean next()
```

### <a name="return-value---next"></a><span data-ttu-id="62e77-199">戻り値 - next</span><span class="sxs-lookup"><span data-stu-id="62e77-199">Return Value - next</span></span>

<span data-ttu-id="62e77-200">現在の新しい行が有効である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="62e77-200">true if the new current row is valid; otherwise false.</span></span>

### <a name="remarks---next"></a><span data-ttu-id="62e77-201">備考 - next</span><span class="sxs-lookup"><span data-stu-id="62e77-201">Remarks - next</span></span>

<span data-ttu-id="62e77-202">ResultSet は、最初に、最初の行の前に配置されます。</span><span class="sxs-lookup"><span data-stu-id="62e77-202">A ResultSet is initially positioned before its first row.</span></span> <span data-ttu-id="62e77-203">次のメソッドへの最初の呼び出しは、最初の行を現在の行にします。</span><span class="sxs-lookup"><span data-stu-id="62e77-203">The first call to the next method makes the first row the current row.</span></span> <span data-ttu-id="62e77-204">2 番目の呼び出しで 2 番目の行が現在の行になります。</span><span class="sxs-lookup"><span data-stu-id="62e77-204">The second call makes the second row the current row, and so on.</span></span>

## <a name="method-wasnull"></a><span data-ttu-id="62e77-205">メソッド wasNull</span><span class="sxs-lookup"><span data-stu-id="62e77-205">Method wasNull</span></span>

<span data-ttu-id="62e77-206">最後の列の読み取りが SQL NULL 値を持つかどうかを報告します。</span><span class="sxs-lookup"><span data-stu-id="62e77-206">Reports whether the last column read has the value SQL NULL.</span></span>

```xpp
public boolean wasNull(int ColumnID)
```

### <a name="parameters---wasnull"></a><span data-ttu-id="62e77-207">パラメーター - wasNull</span><span class="sxs-lookup"><span data-stu-id="62e77-207">Parameters - wasNull</span></span>

<span data-ttu-id="62e77-208">ColumnID</span><span class="sxs-lookup"><span data-stu-id="62e77-208">ColumnID</span></span>  
<span data-ttu-id="62e77-209">列 ID。</span><span class="sxs-lookup"><span data-stu-id="62e77-209">The column ID.</span></span>

### <a name="return-value---wasnull"></a><span data-ttu-id="62e77-210">戻り値 - wasNull</span><span class="sxs-lookup"><span data-stu-id="62e77-210">Return Value - wasNull</span></span>

<span data-ttu-id="62e77-211">最後の列の読み取りに SQL nullNothingnullptrunita null 参照の値 (Visual Basic にはない) がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="62e77-211">true if the last column read has the value SQL nullNothingnullptrunita null reference (Nothing in Visual Basic); otherwise false.</span></span>

### <a name="remarks---wasnull"></a><span data-ttu-id="62e77-212">備考 - wasNull</span><span class="sxs-lookup"><span data-stu-id="62e77-212">Remarks - wasNull</span></span>

<span data-ttu-id="62e77-213">最初にその値を読み取るには、列で、ResultSet.getInt メソッドなどの取得メソッドを呼び出し、次に wasNull メソッドを呼び出して値が NULL SQL かどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e77-213">You must first call a get method, like the ResultSet.getInt method, on a column to try to read its value; then call the wasNull method to find whether the value was the SQL NULL.</span></span>

## <a name="method-close"></a><span data-ttu-id="62e77-214">メソッド close</span><span class="sxs-lookup"><span data-stu-id="62e77-214">Method close</span></span>

<span data-ttu-id="62e77-215">オブジェクトのデータベースのリソースをすぐに解放します。</span><span class="sxs-lookup"><span data-stu-id="62e77-215">Releases the object's database resources immediately.</span></span>

```xpp
public void close()
```
