---
title: SqlSystem クラス
description: このトピックでは、SqlSystem クラスについて説明します。
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
ms.openlocfilehash: b7deeb330dea4de64044fdd3140959d1b1d7f85e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502797"
---
# <a name="class-sqlsystem"></a><span data-ttu-id="f32a5-103">クラス SqlSystem</span><span class="sxs-lookup"><span data-stu-id="f32a5-103">Class SqlSystem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SqlSystem extends Object
```

<span data-ttu-id="f32a5-104">SqlSystem クラスには、有効な SQL システムに関する情報 (通常はログイン情報) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f32a5-104">The SqlSystem class holds information about the active SQL system, typically login information.</span></span>

## <a name="remarks"></a><span data-ttu-id="f32a5-105">備考</span><span class="sxs-lookup"><span data-stu-id="f32a5-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f32a5-106">例</span><span class="sxs-lookup"><span data-stu-id="f32a5-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f32a5-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="f32a5-107">Methods</span></span>

| <span data-ttu-id="f32a5-108">方法</span><span class="sxs-lookup"><span data-stu-id="f32a5-108">Method</span></span>                                                                                                                                   | <span data-ttu-id="f32a5-109">説明</span><span class="sxs-lookup"><span data-stu-id="f32a5-109">Description</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32a5-110">public LoginProperty createLoginProperty()</span><span class="sxs-lookup"><span data-stu-id="f32a5-110">public LoginProperty createLoginProperty()</span></span>                                                                                               | <span data-ttu-id="f32a5-111">データベースにログイン プロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-111">Creates the login property to the  database.</span></span>                                       |
| <span data-ttu-id="f32a5-112">public DatabaseId databaseId()</span><span class="sxs-lookup"><span data-stu-id="f32a5-112">public DatabaseId databaseId()</span></span>                                                                                                           | <span data-ttu-id="f32a5-113">SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-113">Returns the  ID for the database vendor used as the SQL database backend.</span></span>          |
| <span data-ttu-id="f32a5-114">public str databaseName()</span><span class="sxs-lookup"><span data-stu-id="f32a5-114">public str databaseName()</span></span>                                                                                                                | <span data-ttu-id="f32a5-115">SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-115">Returns the name of the database vendor used as the SQL database backend.</span></span>                               |
| <span data-ttu-id="f32a5-116">public boolean dbRequestedUnicodeEnabled()</span><span class="sxs-lookup"><span data-stu-id="f32a5-116">public boolean dbRequestedUnicodeEnabled()</span></span>                                                                                               | <span data-ttu-id="f32a5-117">Unicode がデータベースでサポートされているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-117">Retrieves the value that indicates if Unicode is supported in the database.</span></span>                             |
| <span data-ttu-id="f32a5-118">public str filenameDeadlocks(str Userid)</span><span class="sxs-lookup"><span data-stu-id="f32a5-118">public str filenameDeadlocks(str Userid)</span></span>                                                                                                 | <span data-ttu-id="f32a5-119">デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-119">Retrieves the name of the user specific deadlocks trace logfile.</span></span>                                        |
| <span data-ttu-id="f32a5-120">public str filenameQuerytimelimit(str Userid)</span><span class="sxs-lookup"><span data-stu-id="f32a5-120">public str filenameQuerytimelimit(str Userid)</span></span>                                                                                            | <span data-ttu-id="f32a5-121">ユーザー固有の querytime 期限ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-121">Retrieves the name of the user specific querytime limit logfile.</span></span>                                        |
| <span data-ttu-id="f32a5-122">public str filenameSqlTrace(str Userid)</span><span class="sxs-lookup"><span data-stu-id="f32a5-122">public str filenameSqlTrace(str Userid)</span></span>                                                                                                  | <span data-ttu-id="f32a5-123">特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-123">Retrieves the filename of the SQL trace log file for specific user.</span></span>                                     |
| <span data-ttu-id="f32a5-124">public str filenameWarnings(str Userid)</span><span class="sxs-lookup"><span data-stu-id="f32a5-124">public str filenameWarnings(str Userid)</span></span>                                                                                                  | <span data-ttu-id="f32a5-125">警告ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-125">Retrieves the name of the user specific warnings log file.</span></span>                                              |
| <span data-ttu-id="f32a5-126">public str logfileName(\[boolean fromCommandline\])</span><span class="sxs-lookup"><span data-stu-id="f32a5-126">public str logfileName(\[boolean fromCommandline\])</span></span>                                                                                      | <span data-ttu-id="f32a5-127">標準的な SQL エラー ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-127">Retrieves the name of the standard  SQL error log file.</span></span>                            |
| <span data-ttu-id="f32a5-128">public str loginConnectString()</span><span class="sxs-lookup"><span data-stu-id="f32a5-128">public str loginConnectString()</span></span>                                                                                                          | <span data-ttu-id="f32a5-129">ODBC の完全な接続文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-129">Retrieves the full ODBC connection string.</span></span>                                                              |
| <span data-ttu-id="f32a5-130">public str loginDatabase()</span><span class="sxs-lookup"><span data-stu-id="f32a5-130">public str loginDatabase()</span></span>                                                                                                               | <span data-ttu-id="f32a5-131">現在接続されているデータベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-131">Retrieves the name of the database currently connected to.</span></span>                                              |
| <span data-ttu-id="f32a5-132">public str loginDSN()</span><span class="sxs-lookup"><span data-stu-id="f32a5-132">public str loginDSN()</span></span>                                                                                                                    | <span data-ttu-id="f32a5-133">データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-133">Retrieves the open database connectivity (ODBC) data source name (DSN) used to connect to the database.</span></span> |
| <span data-ttu-id="f32a5-134">public str loginName()</span><span class="sxs-lookup"><span data-stu-id="f32a5-134">public str loginName()</span></span>                                                                                                                   | <span data-ttu-id="f32a5-135">データベースにログインするために使用されるユーザー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-135">Retrieves the user name that is used to log-in to the database.</span></span>                                         |
| <span data-ttu-id="f32a5-136">public str loginServer()</span><span class="sxs-lookup"><span data-stu-id="f32a5-136">public str loginServer()</span></span>                                                                                                                 | <span data-ttu-id="f32a5-137">現在接続されているデータベース サーバーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-137">Retrieves the name of the database server currently connected to.</span></span>                                       |
| <span data-ttu-id="f32a5-138">public str monocaseFmt(\[TableId tableId\], \[FieldId fieldId\], \[boolean includingFieldName\], \[boolean considerSystemVariables\])</span><span class="sxs-lookup"><span data-stu-id="f32a5-138">public str monocaseFmt(\[TableId tableId\], \[FieldId fieldId\], \[boolean includingFieldName\], \[boolean considerSystemVariables\])</span></span>    | <span data-ttu-id="f32a5-139">文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。</span><span class="sxs-lookup"><span data-stu-id="f32a5-139">Retrieves the format string that is used for casting the string to one case (e.g. "NLS\_LOWER(%1)").</span></span>    |
| <span data-ttu-id="f32a5-140">public str sqlLiteral(AnyType data, \[boolean forWhereClause\], \[boolean likeOperand\], \[boolean rightJustify\], \[int stringLength\])</span><span class="sxs-lookup"><span data-stu-id="f32a5-140">public str sqlLiteral(AnyType data, \[boolean forWhereClause\], \[boolean likeOperand\], \[boolean rightJustify\], \[int stringLength\])</span></span> | <span data-ttu-id="f32a5-141">SQL タイプを修正するため入力 AX データ型を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-141">Formats the input AX datatype to correct SQL type.</span></span>                                                      |
| <span data-ttu-id="f32a5-142">::public static boolean clusteredIndexes()</span><span class="sxs-lookup"><span data-stu-id="f32a5-142">::public static boolean clusteredIndexes()</span></span>                                                                                               |                                                                                                         |
| <span data-ttu-id="f32a5-143">::public static str databaseBackendDesc()</span><span class="sxs-lookup"><span data-stu-id="f32a5-143">::public static str databaseBackendDesc()</span></span>                                                                                                |                                                                                                         |
| <span data-ttu-id="f32a5-144">::public static DatabaseId databaseBackendId()</span><span class="sxs-lookup"><span data-stu-id="f32a5-144">::public static DatabaseId databaseBackendId()</span></span>                                                                                           |                                                                                                         |
| <span data-ttu-id="f32a5-145">::public static str databaseBackendName()</span><span class="sxs-lookup"><span data-stu-id="f32a5-145">::public static str databaseBackendName()</span></span>                                                                                                |                                                                                                         |
| <span data-ttu-id="f32a5-146">::public static DatabaseCLI databaseCallLevelInterface()</span><span class="sxs-lookup"><span data-stu-id="f32a5-146">::public static DatabaseCLI databaseCallLevelInterface()</span></span>                                                                                 |                                                                                                         |
| <span data-ttu-id="f32a5-147">::public static int databaseHints(\[int new\_hint\_value\])</span><span class="sxs-lookup"><span data-stu-id="f32a5-147">::public static int databaseHints(\[int new\_hint\_value\])</span></span>                                                                              |                                                                                                         |
| <span data-ttu-id="f32a5-148">::public static boolean functionalIndexes()</span><span class="sxs-lookup"><span data-stu-id="f32a5-148">::public static boolean functionalIndexes()</span></span>                                                                                              |                                                                                                         |
| <span data-ttu-id="f32a5-149">::public static str modelDatabaseBackendName()</span><span class="sxs-lookup"><span data-stu-id="f32a5-149">::public static str modelDatabaseBackendName()</span></span>                                                                                           | <span data-ttu-id="f32a5-150">現在接続されているモデル データベース AOS の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-150">Retrieves the name of the model database AOS currently connected to.</span></span>                                    |
| <span data-ttu-id="f32a5-151">::public static str managedConnectionString()</span><span class="sxs-lookup"><span data-stu-id="f32a5-151">::public static str managedConnectionString()</span></span>                                                                                            |                                                                                                         |
| <span data-ttu-id="f32a5-152">public void new()</span><span class="sxs-lookup"><span data-stu-id="f32a5-152">public void new()</span></span>                                                                                                                        | <span data-ttu-id="f32a5-153">SqlSystem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-153">Initializes a new instance of the SqlSystem class.</span></span>                                                      |
| <span data-ttu-id="f32a5-154">public void logfileWrite(str Text)</span><span class="sxs-lookup"><span data-stu-id="f32a5-154">public void logfileWrite(str Text)</span></span>                                                                                                       | <span data-ttu-id="f32a5-155">テキスト文字列を標準 SQL エラー ログファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-155">Writes a text string into the standard  SQL error logfile.</span></span>                         |

## <a name="method-createloginproperty"></a><span data-ttu-id="f32a5-156">メソッド createLoginProperty</span><span class="sxs-lookup"><span data-stu-id="f32a5-156">Method createLoginProperty</span></span>

<span data-ttu-id="f32a5-157">データベースにログイン プロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-157">Creates the login property to the  database.</span></span>

```xpp
public LoginProperty createLoginProperty()
```

### <a name="return-value---createloginproperty"></a><span data-ttu-id="f32a5-158">戻り値 - createLoginProperty</span><span class="sxs-lookup"><span data-stu-id="f32a5-158">Return Value - createLoginProperty</span></span>

<span data-ttu-id="f32a5-159">作成されたログイン プロパティ。</span><span class="sxs-lookup"><span data-stu-id="f32a5-159">The login property that was created.</span></span>

## <a name="method-databaseid"></a><span data-ttu-id="f32a5-160">メソッド databaseId</span><span class="sxs-lookup"><span data-stu-id="f32a5-160">Method databaseId</span></span>

<span data-ttu-id="f32a5-161">SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-161">Returns the  ID for the database vendor used as the SQL database backend.</span></span>

```xpp
public DatabaseId databaseId()
```

### <a name="return-value---databaseid"></a><span data-ttu-id="f32a5-162">戻り値 - databaseId</span><span class="sxs-lookup"><span data-stu-id="f32a5-162">Return Value - databaseId</span></span>

<span data-ttu-id="f32a5-163">SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID。</span><span class="sxs-lookup"><span data-stu-id="f32a5-163">The  ID for the database vendor used as the SQL database backend.</span></span>

### <a name="remarks---databaseid"></a><span data-ttu-id="f32a5-164">備考 - databaseId</span><span class="sxs-lookup"><span data-stu-id="f32a5-164">Remarks - databaseId</span></span>

<span data-ttu-id="f32a5-165">データベースの仕入先が、何らかの理由で特定できない場合、列挙 DbBackend::UNKNOWN が返されます。</span><span class="sxs-lookup"><span data-stu-id="f32a5-165">If the database vendor cannot be determined for any reason, the enumeration DbBackend::UNKNOWN is returned.</span></span>

## <a name="method-databasename"></a><span data-ttu-id="f32a5-166">メソッド databaseName</span><span class="sxs-lookup"><span data-stu-id="f32a5-166">Method databaseName</span></span>

<span data-ttu-id="f32a5-167">SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-167">Returns the name of the database vendor used as the SQL database backend.</span></span>

```xpp
public str databaseName()
```

### <a name="return-value---databasename"></a><span data-ttu-id="f32a5-168">戻り値 - databaseName</span><span class="sxs-lookup"><span data-stu-id="f32a5-168">Return Value - databaseName</span></span>

<span data-ttu-id="f32a5-169">SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-169">The name of the database vendor used as the SQL database backend.</span></span>

## <a name="method-dbrequestedunicodeenabled"></a><span data-ttu-id="f32a5-170">メソッド dbRequestedUnicodeEnabled</span><span class="sxs-lookup"><span data-stu-id="f32a5-170">Method dbRequestedUnicodeEnabled</span></span>

<span data-ttu-id="f32a5-171">Unicode がデータベースでサポートされているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-171">Retrieves the value that indicates if Unicode is supported in the database.</span></span>

```xpp
public boolean dbRequestedUnicodeEnabled()
```

### <a name="return-value---dbrequestedunicodeenabled"></a><span data-ttu-id="f32a5-172">戻り値 - dbRequestedUnicodeEnabled</span><span class="sxs-lookup"><span data-stu-id="f32a5-172">Return Value - dbRequestedUnicodeEnabled</span></span>

<span data-ttu-id="f32a5-173">Unicode がデータベースでサポートされているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="f32a5-173">The value that indicates if Unicode is supported in the database.</span></span>

## <a name="method-filenamedeadlocks"></a><span data-ttu-id="f32a5-174">メソッド filenameDeadlocks</span><span class="sxs-lookup"><span data-stu-id="f32a5-174">Method filenameDeadlocks</span></span>

<span data-ttu-id="f32a5-175">デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-175">Retrieves the name of the user specific deadlocks trace logfile.</span></span>

```xpp
public str filenameDeadlocks(str Userid)
```

### <a name="parameters---filenamedeadlocks"></a><span data-ttu-id="f32a5-176">パラメーター - filenameDeadlocks</span><span class="sxs-lookup"><span data-stu-id="f32a5-176">Parameters - filenameDeadlocks</span></span>

<span data-ttu-id="f32a5-177">Userid</span><span class="sxs-lookup"><span data-stu-id="f32a5-177">Userid</span></span>  

### <a name="return-value---filenamedeadlocks"></a><span data-ttu-id="f32a5-178">戻り値 - filenameDeadlocks</span><span class="sxs-lookup"><span data-stu-id="f32a5-178">Return Value - filenameDeadlocks</span></span>

<span data-ttu-id="f32a5-179">デッドロックのトレース ログ ファイルに固有のユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-179">The name of the user specific to deadlocks trace log file.</span></span>

## <a name="method-filenamequerytimelimit"></a><span data-ttu-id="f32a5-180">メソッド filenameQuerytimelimit</span><span class="sxs-lookup"><span data-stu-id="f32a5-180">Method filenameQuerytimelimit</span></span>

<span data-ttu-id="f32a5-181">ユーザー固有の querytime 期限ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-181">Retrieves the name of the user specific querytime limit logfile.</span></span>

```xpp
public str filenameQuerytimelimit(str Userid)
```

### <a name="parameters---filenamequerytimelimit"></a><span data-ttu-id="f32a5-182">パラメーター - filenameQuerytimelimit</span><span class="sxs-lookup"><span data-stu-id="f32a5-182">Parameters - filenameQuerytimelimit</span></span>

<span data-ttu-id="f32a5-183">Userid</span><span class="sxs-lookup"><span data-stu-id="f32a5-183">Userid</span></span>  

### <a name="return-value---filenamequerytimelimit"></a><span data-ttu-id="f32a5-184">戻り値 - filenameQuerytimelimit</span><span class="sxs-lookup"><span data-stu-id="f32a5-184">Return Value - filenameQuerytimelimit</span></span>

<span data-ttu-id="f32a5-185">ユーザー固有の querytime 期限ログ ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-185">The name of the user specific querytime limit logfile.</span></span>

## <a name="method-filenamesqltrace"></a><span data-ttu-id="f32a5-186">メソッド filenameSqlTrace</span><span class="sxs-lookup"><span data-stu-id="f32a5-186">Method filenameSqlTrace</span></span>

<span data-ttu-id="f32a5-187">特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-187">Retrieves the filename of the SQL trace log file for specific user.</span></span>

```xpp
public str filenameSqlTrace(str Userid)
```

### <a name="parameters---filenamesqltrace"></a><span data-ttu-id="f32a5-188">パラメーター - filenameSqlTrace</span><span class="sxs-lookup"><span data-stu-id="f32a5-188">Parameters - filenameSqlTrace</span></span>

<span data-ttu-id="f32a5-189">Userid</span><span class="sxs-lookup"><span data-stu-id="f32a5-189">Userid</span></span>  
<span data-ttu-id="f32a5-190">ユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="f32a5-190">The User Id.</span></span>

### <a name="return-value---filenamesqltrace"></a><span data-ttu-id="f32a5-191">戻り値 - filenameSqlTrace</span><span class="sxs-lookup"><span data-stu-id="f32a5-191">Return Value - filenameSqlTrace</span></span>

<span data-ttu-id="f32a5-192">SQL 追跡ログのファイル名。</span><span class="sxs-lookup"><span data-stu-id="f32a5-192">The filename of SQL trace log.</span></span>

## <a name="method-filenamewarnings"></a><span data-ttu-id="f32a5-193">メソッド filenameWarnings</span><span class="sxs-lookup"><span data-stu-id="f32a5-193">Method filenameWarnings</span></span>

<span data-ttu-id="f32a5-194">警告ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-194">Retrieves the name of the user specific warnings log file.</span></span>

```xpp
public str filenameWarnings(str Userid)
```

### <a name="parameters---filenamewarnings"></a><span data-ttu-id="f32a5-195">パラメーター - filenameWarnings</span><span class="sxs-lookup"><span data-stu-id="f32a5-195">Parameters - filenameWarnings</span></span>

<span data-ttu-id="f32a5-196">Userid</span><span class="sxs-lookup"><span data-stu-id="f32a5-196">Userid</span></span>  
<span data-ttu-id="f32a5-197">関係ユーザーの識別子。</span><span class="sxs-lookup"><span data-stu-id="f32a5-197">The identifier of interested user.</span></span>

### <a name="return-value---filenamewarnings"></a><span data-ttu-id="f32a5-198">戻り値 - filenameWarnings</span><span class="sxs-lookup"><span data-stu-id="f32a5-198">Return Value - filenameWarnings</span></span>

<span data-ttu-id="f32a5-199">警告ログ ファイルに固有のユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-199">The name of the user specific warnings log file.</span></span>

## <a name="method-logfilename"></a><span data-ttu-id="f32a5-200">メソッド logfileName</span><span class="sxs-lookup"><span data-stu-id="f32a5-200">Method logfileName</span></span>

<span data-ttu-id="f32a5-201">標準的な SQL エラー ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-201">Retrieves the name of the standard  SQL error log file.</span></span>

```xpp
public str logfileName([boolean fromCommandline])
```

### <a name="parameters---logfilename"></a><span data-ttu-id="f32a5-202">パラメーター - logfileName</span><span class="sxs-lookup"><span data-stu-id="f32a5-202">Parameters - logfileName</span></span>

<span data-ttu-id="f32a5-203">fromCommandline</span><span class="sxs-lookup"><span data-stu-id="f32a5-203">fromCommandline</span></span>  
<span data-ttu-id="f32a5-204">ブール値。</span><span class="sxs-lookup"><span data-stu-id="f32a5-204">A boolean value.</span></span> <span data-ttu-id="f32a5-205">パラメーターとしてゼロ以外の値を渡すと、コマンド ラインで渡されるログファイル名が呼び出しにより返されます (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f32a5-205">Passing a non-zero value as parameter makes the call return the logfile name passed on the command line; optional.</span></span>

### <a name="return-value---logfilename"></a><span data-ttu-id="f32a5-206">戻り値 - logfileName</span><span class="sxs-lookup"><span data-stu-id="f32a5-206">Return Value - logfileName</span></span>

<span data-ttu-id="f32a5-207">標準 SQL エラー ログ ファイルのファイル名。</span><span class="sxs-lookup"><span data-stu-id="f32a5-207">The file name of the standard  SQL error log file.</span></span>

### <a name="remarks---logfilename"></a><span data-ttu-id="f32a5-208">備考 - logfileName</span><span class="sxs-lookup"><span data-stu-id="f32a5-208">Remarks - logfileName</span></span>

<span data-ttu-id="f32a5-209">バージョン 2.11 以降では、空の文字列が返されます (下位互換性のため)。</span><span class="sxs-lookup"><span data-stu-id="f32a5-209">In version 2.11 or higher, an empty string is returned (for backward compatibility).</span></span> <span data-ttu-id="f32a5-210">ログ ファイル名を取得するには、filenameSqlError メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-210">Use the filenameSqlError method to retrieve the log file name.</span></span>

## <a name="method-loginconnectstring"></a><span data-ttu-id="f32a5-211">メソッド loginConnectString</span><span class="sxs-lookup"><span data-stu-id="f32a5-211">Method loginConnectString</span></span>

<span data-ttu-id="f32a5-212">ODBC の完全な接続文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-212">Retrieves the full ODBC connection string.</span></span>

```xpp
public str loginConnectString()
```

### <a name="return-value---loginconnectstring"></a><span data-ttu-id="f32a5-213">戻り値 - loginConnectString</span><span class="sxs-lookup"><span data-stu-id="f32a5-213">Return Value - loginConnectString</span></span>

<span data-ttu-id="f32a5-214">ODBC の完全な接続文字列。</span><span class="sxs-lookup"><span data-stu-id="f32a5-214">The full ODBC connection string.</span></span>

## <a name="method-logindatabase"></a><span data-ttu-id="f32a5-215">メソッド loginDatabase</span><span class="sxs-lookup"><span data-stu-id="f32a5-215">Method loginDatabase</span></span>

<span data-ttu-id="f32a5-216">現在接続されているデータベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-216">Retrieves the name of the database currently connected to.</span></span>

```xpp
public str loginDatabase()
```

### <a name="return-value---logindatabase"></a><span data-ttu-id="f32a5-217">戻り値 - loginDatabase</span><span class="sxs-lookup"><span data-stu-id="f32a5-217">Return Value - loginDatabase</span></span>

<span data-ttu-id="f32a5-218">現在接続されているデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-218">The name of the database currently connected to.</span></span>

### <a name="examples---logindatabase"></a><span data-ttu-id="f32a5-219">例 - loginDatabase</span><span class="sxs-lookup"><span data-stu-id="f32a5-219">Examples - loginDatabase</span></span>

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginDatabase(); 
}
```

## <a name="method-logindsn"></a><span data-ttu-id="f32a5-220">メソッド loginDSN</span><span class="sxs-lookup"><span data-stu-id="f32a5-220">Method loginDSN</span></span>

<span data-ttu-id="f32a5-221">データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-221">Retrieves the open database connectivity (ODBC) data source name (DSN) used to connect to the database.</span></span>

```xpp
public str loginDSN()
```

### <a name="return-value---logindsn"></a><span data-ttu-id="f32a5-222">戻り値 - loginDSN</span><span class="sxs-lookup"><span data-stu-id="f32a5-222">Return Value - loginDSN</span></span>

<span data-ttu-id="f32a5-223">データベースへの接続に使用される ODBC データ ソース名の名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-223">The name of the ODBC data source name that is used for connecting to the database.</span></span>

### <a name="remarks---logindsn"></a><span data-ttu-id="f32a5-224">備考 - loginDSN</span><span class="sxs-lookup"><span data-stu-id="f32a5-224">Remarks - loginDSN</span></span>

<span data-ttu-id="f32a5-225">既定の DSN は「BMSDSN」です。</span><span class="sxs-lookup"><span data-stu-id="f32a5-225">The default DSN is "BMSDSN".</span></span>

### <a name="examples---logindsn"></a><span data-ttu-id="f32a5-226">例 - loginDSN</span><span class="sxs-lookup"><span data-stu-id="f32a5-226">Examples - loginDSN</span></span>

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginDSN(); 
}
```

## <a name="method-loginname"></a><span data-ttu-id="f32a5-227">メソッド loginName</span><span class="sxs-lookup"><span data-stu-id="f32a5-227">Method loginName</span></span>

<span data-ttu-id="f32a5-228">データベースにログインするために使用されるユーザー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-228">Retrieves the user name that is used to log-in to the database.</span></span>

```xpp
public str loginName()
```

### <a name="return-value---loginname"></a><span data-ttu-id="f32a5-229">戻り値 - loginName</span><span class="sxs-lookup"><span data-stu-id="f32a5-229">Return Value - loginName</span></span>

<span data-ttu-id="f32a5-230">データベースにログインするために使用されるユーザー名。</span><span class="sxs-lookup"><span data-stu-id="f32a5-230">The user name that is used to log-in to the database.</span></span>

### <a name="examples---loginname"></a><span data-ttu-id="f32a5-231">例 - loginName</span><span class="sxs-lookup"><span data-stu-id="f32a5-231">Examples - loginName</span></span>

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginName(); 
}
```

## <a name="method-loginserver"></a><span data-ttu-id="f32a5-232">メソッド loginServer</span><span class="sxs-lookup"><span data-stu-id="f32a5-232">Method loginServer</span></span>

<span data-ttu-id="f32a5-233">現在接続されているデータベース サーバーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-233">Retrieves the name of the database server currently connected to.</span></span>

```xpp
public str loginServer()
```

### <a name="return-value---loginserver"></a><span data-ttu-id="f32a5-234">戻り値 - loginServer</span><span class="sxs-lookup"><span data-stu-id="f32a5-234">Return Value - loginServer</span></span>

<span data-ttu-id="f32a5-235">現在接続されているデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-235">The name of the database currently connected to.</span></span>

### <a name="remarks---loginserver"></a><span data-ttu-id="f32a5-236">備考 - loginServer</span><span class="sxs-lookup"><span data-stu-id="f32a5-236">Remarks - loginServer</span></span>

<span data-ttu-id="f32a5-237">データベースがサーバーの概念をサポートしていない場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="f32a5-237">An empty string is returned if the database does not support a server concept.</span></span>

### <a name="examples---loginserver"></a><span data-ttu-id="f32a5-238">例 - loginServer</span><span class="sxs-lookup"><span data-stu-id="f32a5-238">Examples - loginServer</span></span>

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginServer(); 
}
```

## <a name="method-monocasefmt"></a><span data-ttu-id="f32a5-239">メソッド monocaseFmt</span><span class="sxs-lookup"><span data-stu-id="f32a5-239">Method monocaseFmt</span></span>

<span data-ttu-id="f32a5-240">文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。</span><span class="sxs-lookup"><span data-stu-id="f32a5-240">Retrieves the format string that is used for casting the string to one case (e.g. "NLS\_LOWER(%1)").</span></span>

```xpp
public str monocaseFmt([TableId tableId], [FieldId fieldId], [boolean includingFieldName], [boolean considerSystemVariables])
```

### <a name="parameters---monocasefmt"></a><span data-ttu-id="f32a5-241">パラメーター - monocaseFmt</span><span class="sxs-lookup"><span data-stu-id="f32a5-241">Parameters - monocaseFmt</span></span>

<span data-ttu-id="f32a5-242">tableId</span><span class="sxs-lookup"><span data-stu-id="f32a5-242">tableId</span></span>  

<!-- -->

<span data-ttu-id="f32a5-243">fieldId</span><span class="sxs-lookup"><span data-stu-id="f32a5-243">fieldId</span></span>  

<!-- -->

<span data-ttu-id="f32a5-244">includingFieldName</span><span class="sxs-lookup"><span data-stu-id="f32a5-244">includingFieldName</span></span>  

<!-- -->

<span data-ttu-id="f32a5-245">considerSystemVariables</span><span class="sxs-lookup"><span data-stu-id="f32a5-245">considerSystemVariables</span></span>  

### <a name="return-value---monocasefmt"></a><span data-ttu-id="f32a5-246">戻り値 - monocaseFmt</span><span class="sxs-lookup"><span data-stu-id="f32a5-246">Return Value - monocaseFmt</span></span>

<span data-ttu-id="f32a5-247">文字列を 1 つのケースにキャストするために使用される書式文字列。</span><span class="sxs-lookup"><span data-stu-id="f32a5-247">The format string that is used for casting the string to one case.</span></span>

### <a name="remarks---monocasefmt"></a><span data-ttu-id="f32a5-248">備考 - monocaseFmt</span><span class="sxs-lookup"><span data-stu-id="f32a5-248">Remarks - monocaseFmt</span></span>

<span data-ttu-id="f32a5-249">プレースホルダーの Finance and Operations アプリケーション スタイルが使用されます ("%1" など)。</span><span class="sxs-lookup"><span data-stu-id="f32a5-249">Finance and Operations application style for placeholder(s) is used (i.e. "%1").</span></span>

## <a name="method-sqlliteral"></a><span data-ttu-id="f32a5-250">メソッド sqlLiteral</span><span class="sxs-lookup"><span data-stu-id="f32a5-250">Method sqlLiteral</span></span>

<span data-ttu-id="f32a5-251">SQL タイプを修正するため入力 AX データ型を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-251">Formats the input AX datatype to correct SQL type.</span></span>

```xpp
public str sqlLiteral(AnyType data, [boolean forWhereClause], [boolean likeOperand], [boolean rightJustify], [int stringLength])
```

### <a name="parameters---sqlliteral"></a><span data-ttu-id="f32a5-252">パラメーター - sqlLiteral</span><span class="sxs-lookup"><span data-stu-id="f32a5-252">Parameters - sqlLiteral</span></span>

<span data-ttu-id="f32a5-253">データ</span><span class="sxs-lookup"><span data-stu-id="f32a5-253">data</span></span>  
<span data-ttu-id="f32a5-254">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="f32a5-254">The length of the string.</span></span> <span data-ttu-id="f32a5-255">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="f32a5-255">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="f32a5-256">forWhereClause</span><span class="sxs-lookup"><span data-stu-id="f32a5-256">forWhereClause</span></span>  
<span data-ttu-id="f32a5-257">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="f32a5-257">The length of the string.</span></span> <span data-ttu-id="f32a5-258">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="f32a5-258">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="f32a5-259">likeOperand</span><span class="sxs-lookup"><span data-stu-id="f32a5-259">likeOperand</span></span>  
<span data-ttu-id="f32a5-260">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="f32a5-260">The length of the string.</span></span> <span data-ttu-id="f32a5-261">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="f32a5-261">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="f32a5-262">rightJustify</span><span class="sxs-lookup"><span data-stu-id="f32a5-262">rightJustify</span></span>  
<span data-ttu-id="f32a5-263">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="f32a5-263">The length of the string.</span></span> <span data-ttu-id="f32a5-264">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="f32a5-264">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="f32a5-265">stringLength</span><span class="sxs-lookup"><span data-stu-id="f32a5-265">stringLength</span></span>  
<span data-ttu-id="f32a5-266">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="f32a5-266">The length of the string.</span></span> <span data-ttu-id="f32a5-267">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="f32a5-267">By default equals zero.</span></span>

### <a name="return-value---sqlliteral"></a><span data-ttu-id="f32a5-268">戻り値 - sqlLiteral</span><span class="sxs-lookup"><span data-stu-id="f32a5-268">Return Value - sqlLiteral</span></span>

<span data-ttu-id="f32a5-269">書式設定された SQL 型文字列。</span><span class="sxs-lookup"><span data-stu-id="f32a5-269">The formatted SQL type string.</span></span>

## <a name="method-clusteredindexes"></a><span data-ttu-id="f32a5-270">メソッド clusteredIndexes</span><span class="sxs-lookup"><span data-stu-id="f32a5-270">Method clusteredIndexes</span></span>

```xpp
public static boolean clusteredIndexes()
```

### <a name="return-value---clusteredindexes"></a><span data-ttu-id="f32a5-271">戻り値 - clusteredIndexes</span><span class="sxs-lookup"><span data-stu-id="f32a5-271">Return Value - clusteredIndexes</span></span>

## <a name="method-databasebackenddesc"></a><span data-ttu-id="f32a5-272">メソッド databaseBackendDesc</span><span class="sxs-lookup"><span data-stu-id="f32a5-272">Method databaseBackendDesc</span></span>

```xpp
public static str databaseBackendDesc()
```

### <a name="return-value---databasebackenddesc"></a><span data-ttu-id="f32a5-273">戻り値 - databaseBackendDesc</span><span class="sxs-lookup"><span data-stu-id="f32a5-273">Return Value - databaseBackendDesc</span></span>

## <a name="method-databasebackendid"></a><span data-ttu-id="f32a5-274">メソッド databaseBackendId</span><span class="sxs-lookup"><span data-stu-id="f32a5-274">Method databaseBackendId</span></span>

```xpp
public static DatabaseId databaseBackendId()
```

### <a name="return-value---databasebackendid"></a><span data-ttu-id="f32a5-275">戻り値 - databaseBackendId</span><span class="sxs-lookup"><span data-stu-id="f32a5-275">Return Value - databaseBackendId</span></span>

## <a name="method-databasebackendname"></a><span data-ttu-id="f32a5-276">メソッド databaseBackendName</span><span class="sxs-lookup"><span data-stu-id="f32a5-276">Method databaseBackendName</span></span>

```xpp
public static str databaseBackendName()
```

### <a name="return-value---databasebackendname"></a><span data-ttu-id="f32a5-277">戻り値 - databaseBackendName</span><span class="sxs-lookup"><span data-stu-id="f32a5-277">Return Value - databaseBackendName</span></span>

## <a name="method-databasecalllevelinterface"></a><span data-ttu-id="f32a5-278">メソッド databaseCallLevelInterface</span><span class="sxs-lookup"><span data-stu-id="f32a5-278">Method databaseCallLevelInterface</span></span>

```xpp
public static DatabaseCLI databaseCallLevelInterface()
```

### <a name="return-value---databasecalllevelinterface"></a><span data-ttu-id="f32a5-279">戻り値 - databaseCallLevelInterface</span><span class="sxs-lookup"><span data-stu-id="f32a5-279">Return Value - databaseCallLevelInterface</span></span>

## <a name="method-databasehints"></a><span data-ttu-id="f32a5-280">メソッド databaseHints</span><span class="sxs-lookup"><span data-stu-id="f32a5-280">Method databaseHints</span></span>

```xpp
public static int databaseHints([int new_hint_value])
```

### <a name="parameters---databasehints"></a><span data-ttu-id="f32a5-281">パラメーター - databaseHints</span><span class="sxs-lookup"><span data-stu-id="f32a5-281">Parameters - databaseHints</span></span>

<span data-ttu-id="f32a5-282">new\_hint\_value</span><span class="sxs-lookup"><span data-stu-id="f32a5-282">new\_hint\_value</span></span>  

### <a name="return-value---databasehints"></a><span data-ttu-id="f32a5-283">戻り値 - databaseHints</span><span class="sxs-lookup"><span data-stu-id="f32a5-283">Return Value - databaseHints</span></span>

## <a name="method-functionalindexes"></a><span data-ttu-id="f32a5-284">メソッド functionalIndexes</span><span class="sxs-lookup"><span data-stu-id="f32a5-284">Method functionalIndexes</span></span>

```xpp
public static boolean functionalIndexes()
```

### <a name="return-value---functionalindexes"></a><span data-ttu-id="f32a5-285">戻り値 - functionalIndexes</span><span class="sxs-lookup"><span data-stu-id="f32a5-285">Return Value - functionalIndexes</span></span>

## <a name="method-modeldatabasebackendname"></a><span data-ttu-id="f32a5-286">メソッド modelDatabaseBackendName</span><span class="sxs-lookup"><span data-stu-id="f32a5-286">Method modelDatabaseBackendName</span></span>

<span data-ttu-id="f32a5-287">現在接続されているモデル データベース AOS の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-287">Retrieves the name of the model database AOS currently connected to.</span></span>

```xpp
public static str modelDatabaseBackendName()
```

### <a name="return-value---modeldatabasebackendname"></a><span data-ttu-id="f32a5-288">戻り値 - modelDatabaseBackendName</span><span class="sxs-lookup"><span data-stu-id="f32a5-288">Return Value - modelDatabaseBackendName</span></span>

<span data-ttu-id="f32a5-289">現在接続されているモデル データベースの名前。</span><span class="sxs-lookup"><span data-stu-id="f32a5-289">The name of the model database currently connected to.</span></span>

## <a name="method-managedconnectionstring"></a><span data-ttu-id="f32a5-290">メソッド managedConnectionString</span><span class="sxs-lookup"><span data-stu-id="f32a5-290">Method managedConnectionString</span></span>

```xpp
public static str managedConnectionString()
```

### <a name="return-value---managedconnectionstring"></a><span data-ttu-id="f32a5-291">戻り値 - managedConnectionString</span><span class="sxs-lookup"><span data-stu-id="f32a5-291">Return Value - managedConnectionString</span></span>

## <a name="method-new"></a><span data-ttu-id="f32a5-292">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f32a5-292">Method new</span></span>

<span data-ttu-id="f32a5-293">SqlSystem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-293">Initializes a new instance of the SqlSystem class.</span></span>

```xpp
public void new()
```

## <a name="method-logfilewrite"></a><span data-ttu-id="f32a5-294">メソッド logfileWrite</span><span class="sxs-lookup"><span data-stu-id="f32a5-294">Method logfileWrite</span></span>

<span data-ttu-id="f32a5-295">テキスト文字列を標準 SQL エラー ログファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-295">Writes a text string into the standard  SQL error logfile.</span></span>

```xpp
public void logfileWrite(str Text)
```

### <a name="parameters---logfilewrite"></a><span data-ttu-id="f32a5-296">パラメーター - logfileWrite</span><span class="sxs-lookup"><span data-stu-id="f32a5-296">Parameters - logfileWrite</span></span>

<span data-ttu-id="f32a5-297">テキスト</span><span class="sxs-lookup"><span data-stu-id="f32a5-297">Text</span></span>  
<span data-ttu-id="f32a5-298">ログファイルに書き込むテキスト (ブックマークなど)。</span><span class="sxs-lookup"><span data-stu-id="f32a5-298">The text (for example, a bookmark) to write to the logfile.</span></span>

### <a name="remarks---logfilewrite"></a><span data-ttu-id="f32a5-299">備考 - logfileWrite</span><span class="sxs-lookup"><span data-stu-id="f32a5-299">Remarks - logfileWrite</span></span>

<span data-ttu-id="f32a5-300">あらゆる種類のエラー状況 (ログ ファイルに記録される) に従い、現在のシナリオを説明する個人用ブックマークを挿入します。</span><span class="sxs-lookup"><span data-stu-id="f32a5-300">Following an error situation of any kind (which is logged in the logfile), you may want to insert a personal bookmark that explains the current scenario.</span></span>

### <a name="examples---logfilewrite"></a><span data-ttu-id="f32a5-301">例 - logfileWrite</span><span class="sxs-lookup"><span data-stu-id="f32a5-301">Examples - logfileWrite</span></span>

```xpp
static void myExample(Args _args) 
{ 
    SqlSystem SqlSystem; 
    SqlSystem = new SqlSystem(); 
    SqlSystem.logfileWrite("Recheck the returned data."); 
}
```

