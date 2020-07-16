---
title: SqlDataDictionaryPermission クラス
description: このトピックでは、SqlDataDictionaryPermission クラスについて説明します。
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
ms.openlocfilehash: af3ed2311289f170328d1cc9d0f4cebcacc2333b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502800"
---
# <a name="class-sqldatadictionarypermission"></a><span data-ttu-id="9c7c5-103">クラス SqlDataDictionaryPermission</span><span class="sxs-lookup"><span data-stu-id="9c7c5-103">Class SqlDataDictionaryPermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SqlDataDictionaryPermission extends CodeAccessPermission
```

<span data-ttu-id="9c7c5-104">SqlDataDictionaryPermission クラスは、メソッドにアクセスする機能を制御し、特定の API のアクセス許可を確認するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-104">The SqlDataDictionaryPermission class controls the ability to access the methods on the and is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="9c7c5-105">保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-105">For a list of all protected APIs, see Secured APIs.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c7c5-106">備考</span><span class="sxs-lookup"><span data-stu-id="9c7c5-106">Remarks</span></span>

<span data-ttu-id="9c7c5-107">保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-107">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission::demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="9c7c5-108">次のいずれかでサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="9c7c5-108">Call a method on the server tier from one of the following:</span></span>

-   <span data-ttu-id="9c7c5-109">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="9c7c5-109">A server static method</span></span>
-   <span data-ttu-id="9c7c5-110">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-110">A class instance method that is set to run on the server by using the RunOn class property.</span></span>

## <a name="examples"></a><span data-ttu-id="9c7c5-111">例</span><span class="sxs-lookup"><span data-stu-id="9c7c5-111">Examples</span></span>

<span data-ttu-id="9c7c5-112">次の例では、xRefNames テーブルからデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-112">The following example deletes data from the xRefNames table.</span></span> <span data-ttu-id="9c7c5-113">assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-113">The assert method is called to declare that the code can then instantiate the AsciiIo class that is used to read and write data to a file.</span></span>

```xpp
{ 
    DictTable dictTable = new DictTable(tablenum(xRefNames)); 
    str sqlTableName; 
    SqlDataDictionary sqlTable; 
    if (dictTable && dictTable.enabled()) 
    { 
        sqlTableName = dictTable.name(DbBackend::Sql); 
        sqlTable = new SqlDataDictionary(); 
        // Try to truncate only if the table does exist 
        // in the SQL database. 
        if (sqlTable.tableExist(sqlTableName)) 
        { 
            new SqlDataDictionaryPermission( 
                methodstr(SqlDataDictionary, tableTruncate)).assert(); 
            sqlTable.tableTruncate(tablenum(xRefNames)); 
            CodeAccessPermission::revertAssert(); 
        } 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="9c7c5-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="9c7c5-114">Methods</span></span>

| <span data-ttu-id="9c7c5-115">方法</span><span class="sxs-lookup"><span data-stu-id="9c7c5-115">Method</span></span>                                                 | <span data-ttu-id="9c7c5-116">説明</span><span class="sxs-lookup"><span data-stu-id="9c7c5-116">Description</span></span>                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9c7c5-117">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="9c7c5-117">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="9c7c5-118">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-118">Creates and returns a copy of the current permission class object.</span></span>               |
| <span data-ttu-id="9c7c5-119">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="9c7c5-119">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="9c7c5-120">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-120">Determines whether a current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="9c7c5-121">public void new(IdentifierName methodName)</span><span class="sxs-lookup"><span data-stu-id="9c7c5-121">public void new(IdentifierName methodName)</span></span>             | <span data-ttu-id="9c7c5-122">SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-122">Creates a new instance of the SQLDataDictionaryPermission class.</span></span>                 |

## <a name="method-copy"></a><span data-ttu-id="9c7c5-123">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="9c7c5-123">Method copy</span></span>

<span data-ttu-id="9c7c5-124">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-124">Creates and returns a copy of the current permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="9c7c5-125">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="9c7c5-125">Return Value - copy</span></span>

<span data-ttu-id="9c7c5-126">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-126">A copy of the current permission object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="9c7c5-127">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="9c7c5-127">Remarks - copy</span></span>

<span data-ttu-id="9c7c5-128">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-128">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="9c7c5-129">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-129">For more information, see .</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="9c7c5-130">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="9c7c5-130">Method isSubsetOf</span></span>

<span data-ttu-id="9c7c5-131">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-131">Determines whether a current permission is a subset of the specified permission.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="9c7c5-132">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="9c7c5-132">Parameters - isSubsetOf</span></span>

<span data-ttu-id="9c7c5-133">target</span><span class="sxs-lookup"><span data-stu-id="9c7c5-133">target</span></span>  
<span data-ttu-id="9c7c5-134">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-134">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="9c7c5-135">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="9c7c5-135">Return Value - isSubsetOf</span></span>

<span data-ttu-id="9c7c5-136">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-136">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="9c7c5-137">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="9c7c5-137">Remarks - isSubsetOf</span></span>

<span data-ttu-id="9c7c5-138">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-138">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="9c7c5-139">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-139">For more information, see .</span></span>

## <a name="method-new"></a><span data-ttu-id="9c7c5-140">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9c7c5-140">Method new</span></span>

<span data-ttu-id="9c7c5-141">SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-141">Creates a new instance of the SQLDataDictionaryPermission class.</span></span>

```xpp
public void new(IdentifierName methodName)
```

### <a name="parameters---new"></a><span data-ttu-id="9c7c5-142">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="9c7c5-142">Parameters - new</span></span>

<span data-ttu-id="9c7c5-143">methodName</span><span class="sxs-lookup"><span data-stu-id="9c7c5-143">methodName</span></span>  
<span data-ttu-id="9c7c5-144">呼び出されるメソッドの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-144">The string that represents the name of the method to be called.</span></span>

### <a name="examples---new"></a><span data-ttu-id="9c7c5-145">例 - new</span><span class="sxs-lookup"><span data-stu-id="9c7c5-145">Examples - new</span></span>

<span data-ttu-id="9c7c5-146">次のコード例は、xRefNames テーブルのデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-146">The following code example deletes the data in the xRefNames table.</span></span>

```xpp
server static void main(Args _args) 
{ 
    DictTable dictTable = new DictTable(tablenum(xRefNames)); 
    str sqlTableName; 
    SqlDataDictionary sqlTable; 
    if (dictTable && dictTable.enabled()) 
    { 
        sqlTableName = dictTable.name(DbBackend::Sql); 
        sqlTable = new SqlDataDictionary(); 
        // Only try to truncate if the table does exist 
        // in the SQL database 
        if (sqlTable.tableExist(sqlTableName)) 
        { 
            new SqlDataDictionaryPermission( 
                methodstr(SqlDataDictionary, tableTruncate)).assert(); 
            sqlTable.tableTruncate(tablenum(xRefNames)); 
            CodeAccessPermission::revertAssert(); 
        } 
    } 
}
```

