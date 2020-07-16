---
title: SqlStatementExecutePermission クラス
description: このトピックでは、SqlStatementExecutePermission クラスについて説明します。
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
ms.openlocfilehash: db99dcff542b2f8d8f470734faf20a8fa438fc5f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502799"
---
# <a name="class-sqlstatementexecutepermission"></a><span data-ttu-id="ddc97-103">クラス SqlStatementExecutePermission</span><span class="sxs-lookup"><span data-stu-id="ddc97-103">Class SqlStatementExecutePermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SqlStatementExecutePermission extends CodeAccessPermission
```

<span data-ttu-id="ddc97-104">SQL を使用する機能をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="ddc97-104">Controls the ability to use SQL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddc97-105">備考</span><span class="sxs-lookup"><span data-stu-id="ddc97-105">Remarks</span></span>

<span data-ttu-id="ddc97-106">このクラスは、特定の API のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ddc97-106">This class is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="ddc97-107">保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ddc97-107">For a list of all protected APIs, see Secured APIs.</span></span> <span data-ttu-id="ddc97-108">保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddc97-108">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission::demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="ddc97-109">次のいずれかでサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="ddc97-109">Call a method on the server tier from one of the following:</span></span>

-   <span data-ttu-id="ddc97-110">サーバー静的メソッド �または�</span><span class="sxs-lookup"><span data-stu-id="ddc97-110">A server static method �or�</span></span>
-   <span data-ttu-id="ddc97-111">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="ddc97-111">A class instance method that is set to run on the server by using the RunOn class property</span></span>

## <a name="examples"></a><span data-ttu-id="ddc97-112">例</span><span class="sxs-lookup"><span data-stu-id="ddc97-112">Examples</span></span>

<span data-ttu-id="ddc97-113">この例では、サーバー上で実行される CustTable テーブルで SQL クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-113">This example performs an SQL query on the CustTable table, which runs on the server.</span></span> <span data-ttu-id="ddc97-114">クエリの結果は、\_resultSet オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="ddc97-114">The result of the query is stored in the \_resultSet object.</span></span> <span data-ttu-id="ddc97-115">assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="ddc97-115">The assert method is called to declare that the code can then instantiate the AsciiIo class that is used to read and write data to a file.</span></span>

```xpp
server static void main(Args _args) 
{ 
    DictTable  _dictTable; 
    Connection _connection; 
    Statement  _statement; 
    str        _sql; 
    ResultSet  _resultSet; 
    SqlStatementExecutePermission _perm; 
    _dictTable = new DictTable(tableNum(CustTable)); 
    if (_dictTable != null) 
        { 
           _connection = new Connection(); 
           _sql = strfmt( "SELECT * FROM %1", _dictTable.name(DbBackend::Sql) ); 
           _perm = new SqlStatementExecutePermission(_sql); 
           // Check for permission to use the _statement. 
           _perm.assert(); 
           _statement = _connection.createStatement(); 
           _resultSet = _statement.executeQuery(_sql); 
           // End the scope of the assert call. 
           CodeAccessPermission::revertAssert(); 
        } 
}
```

## <a name="methods"></a><span data-ttu-id="ddc97-116">メソッド</span><span class="sxs-lookup"><span data-stu-id="ddc97-116">Methods</span></span>

| <span data-ttu-id="ddc97-117">方法</span><span class="sxs-lookup"><span data-stu-id="ddc97-117">Method</span></span>                                                 | <span data-ttu-id="ddc97-118">説明</span><span class="sxs-lookup"><span data-stu-id="ddc97-118">Description</span></span>                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ddc97-119">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="ddc97-119">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="ddc97-120">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-120">Creates and returns a copy of the current permission class object.</span></span>               |
| <span data-ttu-id="ddc97-121">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="ddc97-121">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="ddc97-122">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-122">Determines whether a current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="ddc97-123">public void new(str sqlStatement)</span><span class="sxs-lookup"><span data-stu-id="ddc97-123">public void new(str sqlStatement)</span></span>                      | <span data-ttu-id="ddc97-124">SQLStatementExecutePermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-124">Creates a new instance of the SQLStatementExecutePermission class.</span></span>               |

## <a name="method-copy"></a><span data-ttu-id="ddc97-125">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="ddc97-125">Method copy</span></span>

<span data-ttu-id="ddc97-126">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-126">Creates and returns a copy of the current permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="ddc97-127">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="ddc97-127">Return Value - copy</span></span>

<span data-ttu-id="ddc97-128">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="ddc97-128">A copy of the current permission object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="ddc97-129">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="ddc97-129">Remarks - copy</span></span>

<span data-ttu-id="ddc97-130">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ddc97-130">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="ddc97-131">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ddc97-131">For more information, see .</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="ddc97-132">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ddc97-132">Method isSubsetOf</span></span>

<span data-ttu-id="ddc97-133">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-133">Determines whether a current permission is a subset of the specified permission.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="ddc97-134">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ddc97-134">Parameters - isSubsetOf</span></span>

<span data-ttu-id="ddc97-135">target</span><span class="sxs-lookup"><span data-stu-id="ddc97-135">target</span></span>  
<span data-ttu-id="ddc97-136">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ddc97-136">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="ddc97-137">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ddc97-137">Return Value - isSubsetOf</span></span>

<span data-ttu-id="ddc97-138">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ddc97-138">true if a current permission is a subset of a specified permission; otherwise false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="ddc97-139">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="ddc97-139">Remarks - isSubsetOf</span></span>

<span data-ttu-id="ddc97-140">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ddc97-140">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="ddc97-141">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ddc97-141">For more information, see .</span></span>

## <a name="method-new"></a><span data-ttu-id="ddc97-142">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ddc97-142">Method new</span></span>

<span data-ttu-id="ddc97-143">SQLStatementExecutePermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-143">Creates a new instance of the SQLStatementExecutePermission class.</span></span>

```xpp
public void new(str sqlStatement)
```

### <a name="parameters---new"></a><span data-ttu-id="ddc97-144">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="ddc97-144">Parameters - new</span></span>

<span data-ttu-id="ddc97-145">sqlStatement</span><span class="sxs-lookup"><span data-stu-id="ddc97-145">sqlStatement</span></span>  
<span data-ttu-id="ddc97-146">実行する SQL 文字列。</span><span class="sxs-lookup"><span data-stu-id="ddc97-146">The SQL string to be executed.</span></span>

### <a name="examples---new"></a><span data-ttu-id="ddc97-147">例 - new</span><span class="sxs-lookup"><span data-stu-id="ddc97-147">Examples - new</span></span>

<span data-ttu-id="ddc97-148">次の例では、サーバー上で実行される、CustTable テーブルで SQL クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="ddc97-148">The following example performs an SQL query on the CustTable table, which runs on the server.</span></span> <span data-ttu-id="ddc97-149">クエリの結果は、resultSet オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="ddc97-149">The result of the query is stored in the resultSet object.</span></span>

```xpp
server static void main(Args _args) 
{ 
    DictTable  dictTable; 
    Connection connection; 
    Statement  statement; 
    str        sql; 
    ResultSet  resultSet; 
    SqlStatementExecutePermission perm; 
    dictTable = new DictTable(tableNum(CustTable)); 
    if (dictTable != null) 
        { 
           connection = new Connection(); 
           sql = strfmt( "SELECT * FROM %1", dictTable.name(DbBackend::Sql) ); 
           //Instantiate the permission class 
           perm = new SqlStatementExecutePermission(sql); 
           //check for permission to use statement 
           perm.assert(); 
           statement = connection.createStatement(); 
           resultSet = statement.executeQuery(sql); 
           //end the scope of the assert call 
           CodeAccessPermission::revertAssert(); 
        } 
}
```

