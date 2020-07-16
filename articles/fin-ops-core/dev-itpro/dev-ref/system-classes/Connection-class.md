---
title: 接続クラス
description: このトピックでは、接続クラスについて説明します。
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
ms.openlocfilehash: 8ad277098946056d4fc9c8b12010404a616af0a0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502706"
---
# <a name="class-connection"></a><span data-ttu-id="b441a-103">クラス接続</span><span class="sxs-lookup"><span data-stu-id="b441a-103">Class Connection</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Connection extends Object
```

<span data-ttu-id="b441a-104">接続クラスは、SQL ステートメントを実行して結果を返す現在のデータベース セッションを確立します。</span><span class="sxs-lookup"><span data-stu-id="b441a-104">The Connection class establishes a current database session that you can use to execute SQL statements and return results.</span></span>

## <a name="remarks"></a><span data-ttu-id="b441a-105">備考</span><span class="sxs-lookup"><span data-stu-id="b441a-105">Remarks</span></span>

<span data-ttu-id="b441a-106">次のクラスは Connection クラスを拡張しています。</span><span class="sxs-lookup"><span data-stu-id="b441a-106">The following classes extend the Connection class:</span></span>

-   <span data-ttu-id="b441a-107">OdbcConnection</span><span class="sxs-lookup"><span data-stu-id="b441a-107">OdbcConnection</span></span>
-   <span data-ttu-id="b441a-108">OciConnection</span><span class="sxs-lookup"><span data-stu-id="b441a-108">OciConnection</span></span>
-   <span data-ttu-id="b441a-109">UserConnection</span><span class="sxs-lookup"><span data-stu-id="b441a-109">UserConnection</span></span>

## <a name="examples"></a><span data-ttu-id="b441a-110">例</span><span class="sxs-lookup"><span data-stu-id="b441a-110">Examples</span></span>

<span data-ttu-id="b441a-111">次の例では、createStatement メソッドはステートメント オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b441a-111">In the following example, the createStatement method initializes the Statement object.</span></span> <span data-ttu-id="b441a-112">Statement.executeQuery メソッドは、SQL ステートメントを実行し、ResultSet オブジェクトに取得したデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="b441a-112">The Statement.executeQuery method executes an SQL statement and then stores the retrieved data in the ResultSet object.</span></span>

```xpp
server static void main(Args args) 
{ 
    Connection con = new Connection(); 
    Statement stmt = con.createStatement(); 
    ResultSet r; 
    str sql; 
    SqlStatementExecutePermission perm; 
```

```xpp
    sql = strfmt('SELECT VALUE FROM SQLSYSTEMVARIABLES'); 
```

```xpp
    // Set code access permission to help protect the use of 
    // Statement.executeUpdate. 
    perm = new SqlStatementExecutePermission(sql); 
    perm.assert(); 
```

```xpp
    try 
    { 
        r = stmt.executeQuery(sql); 
        while (r.next()) 
        { 
            print r.getString(1); 
            pause; 
        } 
    } 
    catch (exception::Error) 
    { 
        print "An error occurred in the query."; 
        pause; 
    } 
    // Code access permission scope ends here. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a><span data-ttu-id="b441a-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="b441a-113">Methods</span></span>

| <span data-ttu-id="b441a-114">方法</span><span class="sxs-lookup"><span data-stu-id="b441a-114">Method</span></span>                                                                                                           | <span data-ttu-id="b441a-115">説明</span><span class="sxs-lookup"><span data-stu-id="b441a-115">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b441a-116">public Statement createStatement(\[ResultSetType resultSetType\], \[ResultSetConcurrency resultSetConcurrency\])</span><span class="sxs-lookup"><span data-stu-id="b441a-116">public Statement createStatement(\[ResultSetType resultSetType\], \[ResultSetConcurrency resultSetConcurrency\])</span></span> | <span data-ttu-id="b441a-117">SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b441a-117">Creates a Statement object that is used to execute an SQL statement.</span></span>                                                                                                                    |
| <span data-ttu-id="b441a-118">public int odbcGetInfoInt(int InfoId)</span><span class="sxs-lookup"><span data-stu-id="b441a-118">public int odbcGetInfoInt(int InfoId)</span></span>                                                                            | <span data-ttu-id="b441a-119">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b441a-119">Provides an interface to the SQLGetInfo Open Database Connectivity (ODBC) function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span> |
| <span data-ttu-id="b441a-120">public int odbcGetInfoLong(int InfoId)</span><span class="sxs-lookup"><span data-stu-id="b441a-120">public int odbcGetInfoLong(int InfoId)</span></span>                                                                           | <span data-ttu-id="b441a-121">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b441a-121">Provides an interface to the SQLGetInfo ODBC function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span>                              |
| <span data-ttu-id="b441a-122">public str odbcGetInfoStr(int InfoId)</span><span class="sxs-lookup"><span data-stu-id="b441a-122">public str odbcGetInfoStr(int InfoId)</span></span>                                                                            | <span data-ttu-id="b441a-123">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b441a-123">Provides an interface to the SQLGetInfo ODBC function to retrieve information, in string format, about the ODBC driver and data source that are associated with a connection.</span></span>           |
| <span data-ttu-id="b441a-124">public str toString()</span><span class="sxs-lookup"><span data-stu-id="b441a-124">public str toString()</span></span>                                                                                            | <span data-ttu-id="b441a-125">接続オブジェクトを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="b441a-125">Converts the Connection object to a string.</span></span>                                                                                                                                             |
| <span data-ttu-id="b441a-126">public int ttsLevel()</span><span class="sxs-lookup"><span data-stu-id="b441a-126">public int ttsLevel()</span></span>                                                                                            | <span data-ttu-id="b441a-127">トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。</span><span class="sxs-lookup"><span data-stu-id="b441a-127">Returns the number for the last call to the ttsbegin method that is used to begin a transaction.</span></span>                                                                                        |
| <span data-ttu-id="b441a-128">public boolean isInTransactionScope()</span><span class="sxs-lookup"><span data-stu-id="b441a-128">public boolean isInTransactionScope()</span></span>                                                                            |                                                                                                                                                                                         |
| <span data-ttu-id="b441a-129">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="b441a-129">public void finalize()</span></span>                                                                                           |                                                                                                                                                                                         |
| <span data-ttu-id="b441a-130">public void transactionScopeAbort()</span><span class="sxs-lookup"><span data-stu-id="b441a-130">public void transactionScopeAbort()</span></span>                                                                              |                                                                                                                                                                                         |
| <span data-ttu-id="b441a-131">public void ttsNotifyCommit()</span><span class="sxs-lookup"><span data-stu-id="b441a-131">public void ttsNotifyCommit()</span></span>                                                                                    | <span data-ttu-id="b441a-132">ttscommit メソッドが呼び出されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b441a-132">Is called when the ttscommit method is called.</span></span>                                                                                                                                          |
| <span data-ttu-id="b441a-133">public void transactionScopeBegin()</span><span class="sxs-lookup"><span data-stu-id="b441a-133">public void transactionScopeBegin()</span></span>                                                                              |                                                                                                                                                                                         |
| <span data-ttu-id="b441a-134">public void transactionScopeCommit()</span><span class="sxs-lookup"><span data-stu-id="b441a-134">public void transactionScopeCommit()</span></span>                                                                             |                                                                                                                                                                                         |
| <span data-ttu-id="b441a-135">public void ttsNotifyBegin()</span><span class="sxs-lookup"><span data-stu-id="b441a-135">public void ttsNotifyBegin()</span></span>                                                                                     |                                                                                                                                                                                         |
| <span data-ttu-id="b441a-136">public void ttsbegin()</span><span class="sxs-lookup"><span data-stu-id="b441a-136">public void ttsbegin()</span></span>                                                                                           | <span data-ttu-id="b441a-137">トランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="b441a-137">Begins a transaction.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b441a-138">public void ttsabort()</span><span class="sxs-lookup"><span data-stu-id="b441a-138">public void ttsabort()</span></span>                                                                                           | <span data-ttu-id="b441a-139">トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。</span><span class="sxs-lookup"><span data-stu-id="b441a-139">Discards changes that are associated with a transaction and rolls the database back to the original state.</span></span>                                                                              |
| <span data-ttu-id="b441a-140">public void new()</span><span class="sxs-lookup"><span data-stu-id="b441a-140">public void new()</span></span>                                                                                                | <span data-ttu-id="b441a-141">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b441a-141">Initializes a new instance of the Connection class.</span></span>                                                                                                                                     |
| <span data-ttu-id="b441a-142">public void ttsNotifyAbort()</span><span class="sxs-lookup"><span data-stu-id="b441a-142">public void ttsNotifyAbort()</span></span>                                                                                     | <span data-ttu-id="b441a-143">例外がスローされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b441a-143">Is called when an exception is thrown.</span></span>                                                                                                                                                  |
| <span data-ttu-id="b441a-144">public void ttscommit()</span><span class="sxs-lookup"><span data-stu-id="b441a-144">public void ttscommit()</span></span>                                                                                          | <span data-ttu-id="b441a-145">トランザクションに関連付けられている変更をデータベースにコミットします。</span><span class="sxs-lookup"><span data-stu-id="b441a-145">Commits the changes that are associated with a transaction to the database.</span></span>                                                                                                             |

## <a name="method-createstatement"></a><span data-ttu-id="b441a-146">メソッド createStatement</span><span class="sxs-lookup"><span data-stu-id="b441a-146">Method createStatement</span></span>

<span data-ttu-id="b441a-147">SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b441a-147">Creates a Statement object that is used to execute an SQL statement.</span></span>

```xpp
public Statement createStatement([ResultSetType resultSetType], [ResultSetConcurrency resultSetConcurrency])
```

### <a name="parameters---createstatement"></a><span data-ttu-id="b441a-148">パラメータ - createStatement</span><span class="sxs-lookup"><span data-stu-id="b441a-148">Parameters - createStatement</span></span>

<span data-ttu-id="b441a-149">resultSetType</span><span class="sxs-lookup"><span data-stu-id="b441a-149">resultSetType</span></span>  
<span data-ttu-id="b441a-150">既定で読み取り専用を指定する ResultSetConcurrency 列挙。</span><span class="sxs-lookup"><span data-stu-id="b441a-150">A ResultSetConcurrency enumeration that specifies ReadOnly by default.</span></span>

<!-- -->

<span data-ttu-id="b441a-151">resultSetConcurrency</span><span class="sxs-lookup"><span data-stu-id="b441a-151">resultSetConcurrency</span></span>  
<span data-ttu-id="b441a-152">既定で読み取り専用を指定する ResultSetConcurrency 列挙。</span><span class="sxs-lookup"><span data-stu-id="b441a-152">A ResultSetConcurrency enumeration that specifies ReadOnly by default.</span></span>

### <a name="return-value---createstatement"></a><span data-ttu-id="b441a-153">戻り値 - createStatement</span><span class="sxs-lookup"><span data-stu-id="b441a-153">Return Value - createStatement</span></span>

<span data-ttu-id="b441a-154">新しいステートメント オブジェクトであるデータ型の値です。</span><span class="sxs-lookup"><span data-stu-id="b441a-154">A data type value that is a new Statement object.</span></span>

### <a name="remarks---createstatement"></a><span data-ttu-id="b441a-155">備考 - createStatement</span><span class="sxs-lookup"><span data-stu-id="b441a-155">Remarks - createStatement</span></span>

<span data-ttu-id="b441a-156">createStatement メソッドを使用して SQL ステートメントを作成し、ユーザーがステートメントへの入力を制御できるようにすると、SQL インジェクション脅威の危険性があります。</span><span class="sxs-lookup"><span data-stu-id="b441a-156">There is risk of an SQL injection threat when you use the createStatement method to create an SQL statement and then allow a user to control input to the statement.</span></span> <span data-ttu-id="b441a-157">詳細については [SQL インジェクション](https://go.microsoft.com/fwlink/?LinkId=114986) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b441a-157">For information, see [SQL Injection](https://go.microsoft.com/fwlink/?LinkId=114986).</span></span> <span data-ttu-id="b441a-158">AOT、ビュー、および X++ Select ステートメントでは、SQL ステートメントを実行するための安全な代替手段として、クエリ要素を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b441a-158">You can use Query Elements in the AOT, views, and X++ Select statements as safer alternatives to executing SQL statements.</span></span>

## <a name="method-odbcgetinfoint"></a><span data-ttu-id="b441a-159">メソッド odbcGetInfoInt</span><span class="sxs-lookup"><span data-stu-id="b441a-159">Method odbcGetInfoInt</span></span>

<span data-ttu-id="b441a-160">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b441a-160">Provides an interface to the SQLGetInfo Open Database Connectivity (ODBC) function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span>

```xpp
public int odbcGetInfoInt(int InfoId)
```

### <a name="parameters---odbcgetinfoint"></a><span data-ttu-id="b441a-161">パラメーター - odbcGetInfoInt</span><span class="sxs-lookup"><span data-stu-id="b441a-161">Parameters - odbcGetInfoInt</span></span>

<span data-ttu-id="b441a-162">InfoId</span><span class="sxs-lookup"><span data-stu-id="b441a-162">InfoId</span></span>  
<span data-ttu-id="b441a-163">ODBC 標準に従って要求された情報の ID を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="b441a-163">An integer that specifies an ID for the requested information according to the ODBC standard.</span></span>

### <a name="return-value---odbcgetinfoint"></a><span data-ttu-id="b441a-164">戻り値 - odbcGetInfoInt</span><span class="sxs-lookup"><span data-stu-id="b441a-164">Return Value - odbcGetInfoInt</span></span>

<span data-ttu-id="b441a-165">取得される情報の整数値。</span><span class="sxs-lookup"><span data-stu-id="b441a-165">An integer value for the information that is retrieved.</span></span>

### <a name="examples---odbcgetinfoint"></a><span data-ttu-id="b441a-166">例 - odbcGetInfoInt</span><span class="sxs-lookup"><span data-stu-id="b441a-166">Examples - odbcGetInfoInt</span></span>

<span data-ttu-id="b441a-167">次の例では、odbcGetInfoInt メソッドは列名の最大の長さの整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="b441a-167">In the following example, the odbcGetInfoInt method returns an integer value for the maximum length of the column name.</span></span>

```xpp
void getConnection() 
{ 
    Connection con; 
    Statement stmt; 
    int info; 
```

```xpp
    #define.SQL_MAX_COLUMN_NAME_LEN(30) 
    con = new Connection(); 
```

```xpp
    try 
    { 
        info = con.odbcGetInfoInt(#SQL_MAX_COLUMN_NAME_LEN); 
```

```xpp
        print info; 
        pause; 
     } 
```

```xpp
    catch(exception::Error) 
    { 
        print "An error occurred."; 
```

```xpp
    } 
```

```xpp
}
```

## <a name="method-odbcgetinfolong"></a><span data-ttu-id="b441a-168">メソッド odbcGetInfoLong</span><span class="sxs-lookup"><span data-stu-id="b441a-168">Method odbcGetInfoLong</span></span>

<span data-ttu-id="b441a-169">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b441a-169">Provides an interface to the SQLGetInfo ODBC function to retrieve information about the ODBC driver and data source that are associated with a connection.</span></span>

```xpp
public int odbcGetInfoLong(int InfoId)
```

### <a name="parameters---odbcgetinfolong"></a><span data-ttu-id="b441a-170">パラメーター - odbcGetInfoLong</span><span class="sxs-lookup"><span data-stu-id="b441a-170">Parameters - odbcGetInfoLong</span></span>

<span data-ttu-id="b441a-171">InfoId</span><span class="sxs-lookup"><span data-stu-id="b441a-171">InfoId</span></span>  
<span data-ttu-id="b441a-172">ODBC 標準による要求された情報の ID を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="b441a-172">An Integer data type that specifies an ID for the requested information, according to the ODBC standard.</span></span>

### <a name="return-value---odbcgetinfolong"></a><span data-ttu-id="b441a-173">戻り値 - odbcGetInfoLong</span><span class="sxs-lookup"><span data-stu-id="b441a-173">Return Value - odbcGetInfoLong</span></span>

<span data-ttu-id="b441a-174">取得される情報の整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="b441a-174">An Integer data type value for the information that is retrieved.</span></span>

### <a name="remarks---odbcgetinfolong"></a><span data-ttu-id="b441a-175">備考 - odbcGetInfoLong</span><span class="sxs-lookup"><span data-stu-id="b441a-175">Remarks - odbcGetInfoLong</span></span>

<span data-ttu-id="b441a-176">このメソッドは 32 ビット整数を取得し、整数として返します。</span><span class="sxs-lookup"><span data-stu-id="b441a-176">This method retrieves a 32-bit integer and returns it as an integer.</span></span>

### <a name="examples---odbcgetinfolong"></a><span data-ttu-id="b441a-177">例 - odbcGetInfoLong</span><span class="sxs-lookup"><span data-stu-id="b441a-177">Examples - odbcGetInfoLong</span></span>

<span data-ttu-id="b441a-178">次の例では、odbcGetInfoLong メソッドは行の最大サイズの整数を返します。</span><span class="sxs-lookup"><span data-stu-id="b441a-178">In the following example, the odbcGetInfoLong method returns an integer for the maximum row size.</span></span>

```xpp
void getConnection() 
{ 
    Connection con; 
    Statement stmt; 
    int info; 
```

```xpp
    #define.SQL_MAX_ROW_SIZE(104) 
    con = new Connection(); 
```

```xpp
    try 
    { 
        info = con.odbcGetInfoLong(#SQL_MAX_ROW_SIZE); 
```

```xpp
        print info; 
        pause; 
     } 
```

```xpp
    catch(exception::Error) 
    { 
        print "An error occurred."; 
```

```xpp
    } 
```

```xpp
}
```

## <a name="method-odbcgetinfostr"></a><span data-ttu-id="b441a-179">メソッド odbcGetInfoStr</span><span class="sxs-lookup"><span data-stu-id="b441a-179">Method odbcGetInfoStr</span></span>

<span data-ttu-id="b441a-180">ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b441a-180">Provides an interface to the SQLGetInfo ODBC function to retrieve information, in string format, about the ODBC driver and data source that are associated with a connection.</span></span>

```xpp
public str odbcGetInfoStr(int InfoId)
```

### <a name="parameters---odbcgetinfostr"></a><span data-ttu-id="b441a-181">パラメーター - odbcGetInfoStr</span><span class="sxs-lookup"><span data-stu-id="b441a-181">Parameters - odbcGetInfoStr</span></span>

<span data-ttu-id="b441a-182">InfoId</span><span class="sxs-lookup"><span data-stu-id="b441a-182">InfoId</span></span>  
<span data-ttu-id="b441a-183">ODBC 標準による要求された情報の ID を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="b441a-183">An Integer data type that specifies an ID for the requested information, according to the ODBC standard.</span></span>

### <a name="return-value---odbcgetinfostr"></a><span data-ttu-id="b441a-184">戻り値 - odbcGetInfoStr</span><span class="sxs-lookup"><span data-stu-id="b441a-184">Return Value - odbcGetInfoStr</span></span>

<span data-ttu-id="b441a-185">取得される情報の文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="b441a-185">A String data type value for the information that is retrieved.</span></span>

### <a name="examples---odbcgetinfostr"></a><span data-ttu-id="b441a-186">例 - odbcGetInfoStr</span><span class="sxs-lookup"><span data-stu-id="b441a-186">Examples - odbcGetInfoStr</span></span>

<span data-ttu-id="b441a-187">次の例では、odbcGetInfoStr メソッドはデータベース管理システムの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="b441a-187">In the following example, the odbcGetInfoStr method returns the name of the database management system.</span></span>

```xpp
void getConnection() 
{ 
    Connection con; 
    str info; 
```

```xpp
    #define.SQL_DBMS_NAME(17) 
    con = new Connection(); 
```

```xpp
    try 
    { 
        info = con.odbcGetInfoStr(#SQL_DBMS_NAME); 
```

```xpp
        print info; 
        pause; 
     } 
```

```xpp
    catch(exception::Error) 
    { 
        print "An error occurred."; 
    } 
}
```

## <a name="method-tostring"></a><span data-ttu-id="b441a-188">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="b441a-188">Method toString</span></span>

<span data-ttu-id="b441a-189">接続オブジェクトを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="b441a-189">Converts the Connection object to a string.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="b441a-190">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="b441a-190">Return Value - toString</span></span>

<span data-ttu-id="b441a-191">接続オブジェクトの文字列値。</span><span class="sxs-lookup"><span data-stu-id="b441a-191">A string value for the Connection object.</span></span>

## <a name="method-ttslevel"></a><span data-ttu-id="b441a-192">メソッド ttsLevel</span><span class="sxs-lookup"><span data-stu-id="b441a-192">Method ttsLevel</span></span>

<span data-ttu-id="b441a-193">トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。</span><span class="sxs-lookup"><span data-stu-id="b441a-193">Returns the number for the last call to the ttsbegin method that is used to begin a transaction.</span></span>

```xpp
public int ttsLevel()
```

### <a name="return-value---ttslevel"></a><span data-ttu-id="b441a-194">戻り値 - ttsLevel</span><span class="sxs-lookup"><span data-stu-id="b441a-194">Return Value - ttsLevel</span></span>

<span data-ttu-id="b441a-195">ttsbegin メソッドに最後の呼び出しの番号を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b441a-195">An integer value that indicates the number for the last call to the ttsbegin method.</span></span> <span data-ttu-id="b441a-196">たとえば、ttsLevel メソッドが ttsbegin メソッドへの 3 回目の呼び出し後に呼び出されると、戻り値は 3 になります。</span><span class="sxs-lookup"><span data-stu-id="b441a-196">For example, if the ttsLevel method is called after the third call to the ttsbegin method, the return value is 3.</span></span>

## <a name="method-isintransactionscope"></a><span data-ttu-id="b441a-197">メソッド isInTransactionScope</span><span class="sxs-lookup"><span data-stu-id="b441a-197">Method isInTransactionScope</span></span>

```xpp
public boolean isInTransactionScope()
```

### <a name="return-value---isintransactionscope"></a><span data-ttu-id="b441a-198">戻り値 - isInTransactionScope</span><span class="sxs-lookup"><span data-stu-id="b441a-198">Return Value - isInTransactionScope</span></span>

## <a name="method-finalize"></a><span data-ttu-id="b441a-199">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="b441a-199">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-transactionscopeabort"></a><span data-ttu-id="b441a-200">メソッド transactionScopeAbort</span><span class="sxs-lookup"><span data-stu-id="b441a-200">Method transactionScopeAbort</span></span>

```xpp
public void transactionScopeAbort()
```

## <a name="method-ttsnotifycommit"></a><span data-ttu-id="b441a-201">メソッド ttsNotifyCommit</span><span class="sxs-lookup"><span data-stu-id="b441a-201">Method ttsNotifyCommit</span></span>

<span data-ttu-id="b441a-202">ttscommit メソッドが呼び出されると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b441a-202">Is called when the ttscommit method is called.</span></span>

```xpp
public void ttsNotifyCommit()
```

## <a name="method-transactionscopebegin"></a><span data-ttu-id="b441a-203">メソッド transactionScopeBegin</span><span class="sxs-lookup"><span data-stu-id="b441a-203">Method transactionScopeBegin</span></span>

```xpp
public void transactionScopeBegin()
```

## <a name="method-transactionscopecommit"></a><span data-ttu-id="b441a-204">メソッド transactionScopeCommit</span><span class="sxs-lookup"><span data-stu-id="b441a-204">Method transactionScopeCommit</span></span>

```xpp
public void transactionScopeCommit()
```

## <a name="method-ttsnotifybegin"></a><span data-ttu-id="b441a-205">メソッド ttsNotifyBegin</span><span class="sxs-lookup"><span data-stu-id="b441a-205">Method ttsNotifyBegin</span></span>

```xpp
public void ttsNotifyBegin()
```

## <a name="method-ttsbegin"></a><span data-ttu-id="b441a-206">メソッド ttsbegin</span><span class="sxs-lookup"><span data-stu-id="b441a-206">Method ttsbegin</span></span>

<span data-ttu-id="b441a-207">トランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="b441a-207">Begins a transaction.</span></span>

```xpp
public void ttsbegin()
```

## <a name="method-ttsabort"></a><span data-ttu-id="b441a-208">メソッド ttsabort</span><span class="sxs-lookup"><span data-stu-id="b441a-208">Method ttsabort</span></span>

<span data-ttu-id="b441a-209">トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。</span><span class="sxs-lookup"><span data-stu-id="b441a-209">Discards changes that are associated with a transaction and rolls the database back to the original state.</span></span>

```xpp
public void ttsabort()
```

## <a name="method-new"></a><span data-ttu-id="b441a-210">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b441a-210">Method new</span></span>

<span data-ttu-id="b441a-211">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b441a-211">Initializes a new instance of the Connection class.</span></span>

```xpp
public void new()
```

## <a name="method-ttsnotifyabort"></a><span data-ttu-id="b441a-212">メソッド ttsNotifyAbort</span><span class="sxs-lookup"><span data-stu-id="b441a-212">Method ttsNotifyAbort</span></span>

<span data-ttu-id="b441a-213">例外がスローされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b441a-213">Is called when an exception is thrown.</span></span>

```xpp
public void ttsNotifyAbort()
```

## <a name="method-ttscommit"></a><span data-ttu-id="b441a-214">メソッド ttscommit</span><span class="sxs-lookup"><span data-stu-id="b441a-214">Method ttscommit</span></span>

<span data-ttu-id="b441a-215">トランザクションに関連付けられている変更をデータベースにコミットします。</span><span class="sxs-lookup"><span data-stu-id="b441a-215">Commits the changes that are associated with a transaction to the database.</span></span>

```xpp
public void ttscommit()
```

