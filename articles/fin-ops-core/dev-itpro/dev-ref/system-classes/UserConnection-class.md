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
# <a name="class-userconnection"></a>クラス UserConnection

[!include [banner](../../includes/banner.md)]

```xpp
class UserConnection extends Connection
```

UserConnection クラスは、主要な接続と同じログオン プロパティに基づいて、SQL データベースへの補助接続を表します。

## <a name="remarks"></a>備考

SQL ステートメントが実行され、結果が UserConnection クラスのコンテキストで返されます。 UserConnection クラスを使用して、別個のトランザクション スコープを取得できます。

注記: ユーザー接続リークを防ぐため、finally ブロックで Userconnection.finalize() を呼び出す必要があります。  オープン ユーザー接続の数がサーバー上で制限されており、制限に達すると、それ以上接続を開くことができなくなり、ビジネス ロジックのエラーになる可能性があります

## <a name="examples"></a>例

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

## <a name="methods"></a>方法

| 方法                                                | 説明                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| public void new(\[boolean generateNewTransactionID\]) | Connection クラスの新しいインスタンスを初期化します。 |

## <a name="method-new"></a>メソッド new

Connection クラスの新しいインスタンスを初期化します。

```xpp
public void new([boolean generateNewTransactionID])
```

### <a name="parameters---new"></a>パラメーター - new

generateNewTransactionID  

