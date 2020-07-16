---
title: UserConnection クラス
description: このトピックでは、UserConnection クラスについて説明します。
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
ms.openlocfilehash: 6a21b9a2ba349432b8f9348609dd6cf01693bd56
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502783"
---
# <a name="class-userconnection"></a><span data-ttu-id="4337d-103">クラス UserConnection</span><span class="sxs-lookup"><span data-stu-id="4337d-103">Class UserConnection</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class UserConnection extends Connection
```

<span data-ttu-id="4337d-104">UserConnection クラスは、主要な接続と同じログオン プロパティに基づいて、SQL データベースへの補助接続を表します。</span><span class="sxs-lookup"><span data-stu-id="4337d-104">The UserConnection class represents an auxiliary connection to the SQL database, based on the same logon properties as the main connection.</span></span>

## <a name="remarks"></a><span data-ttu-id="4337d-105">備考</span><span class="sxs-lookup"><span data-stu-id="4337d-105">Remarks</span></span>

<span data-ttu-id="4337d-106">SQL ステートメントが実行され、結果が UserConnection クラスのコンテキストで返されます。</span><span class="sxs-lookup"><span data-stu-id="4337d-106">SQL statements are executed, and results are returned in the context of a UserConnection class.</span></span> <span data-ttu-id="4337d-107">UserConnection クラスを使用して、別個のトランザクション スコープを取得できます。</span><span class="sxs-lookup"><span data-stu-id="4337d-107">The UserConnection class can be used to obtain a separate transaction scope.</span></span>

<span data-ttu-id="4337d-108">注記: ユーザー接続リークを防ぐため、finally ブロックで Userconnection.finalize() を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4337d-108">Note: Userconnection.finalize() needs to be called in the finally block to prevent user connection leak.</span></span>  <span data-ttu-id="4337d-109">オープン ユーザー接続の数がサーバー上で制限されており、制限に達すると、それ以上接続を開くことができなくなり、ビジネス ロジックのエラーになる可能性があります</span><span class="sxs-lookup"><span data-stu-id="4337d-109">Number of open user connections is limited on the server, when it reaches the limit, no more connections can be opened, which can leads to business logic failures</span></span>

## <a name="examples"></a><span data-ttu-id="4337d-110">例</span><span class="sxs-lookup"><span data-stu-id="4337d-110">Examples</span></span>

```xpp
static void example()  
{ 
    UserConnection Con;
    try
    {
        Statement Stmt; 
        Str sql; 
        ResultSet R; 
        SqlStatementExecutePermission perm; 
        Con = new UserConnection(); 
        sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
        Stmt = Con.createStatement(); 
        perm = new SqlStatementExecutePermission(sql); 
        // Check for permission to use the statement. 
        perm.assert(); 
        R = Stmt.executeQuery(sql); 
        while ( R.next() ) 
        { 
            print R.getString(1); 
        } 
    }
    finally
    {
        con.finalize();
    }
 }
```

## <a name="methods"></a><span data-ttu-id="4337d-111">方法</span><span class="sxs-lookup"><span data-stu-id="4337d-111">Methods</span></span>

| <span data-ttu-id="4337d-112">方法</span><span class="sxs-lookup"><span data-stu-id="4337d-112">Method</span></span>                                                | <span data-ttu-id="4337d-113">説明</span><span class="sxs-lookup"><span data-stu-id="4337d-113">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="4337d-114">public void new(\[boolean generateNewTransactionID\])</span><span class="sxs-lookup"><span data-stu-id="4337d-114">public void new(\[boolean generateNewTransactionID\])</span></span> | <span data-ttu-id="4337d-115">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4337d-115">Initializes a new instance of the Connection class.</span></span> |

## <a name="method-new"></a><span data-ttu-id="4337d-116">メソッド new</span><span class="sxs-lookup"><span data-stu-id="4337d-116">Method new</span></span>

<span data-ttu-id="4337d-117">Connection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4337d-117">Initializes a new instance of the Connection class.</span></span>

```xpp
public void new([boolean generateNewTransactionID])
```

### <a name="parameters---new"></a><span data-ttu-id="4337d-118">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="4337d-118">Parameters - new</span></span>

<span data-ttu-id="4337d-119">generateNewTransactionID</span><span class="sxs-lookup"><span data-stu-id="4337d-119">generateNewTransactionID</span></span>  

