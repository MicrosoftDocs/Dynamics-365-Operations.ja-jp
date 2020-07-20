---
title: ExecutePermission クラス
description: このトピックでは、ExecutePermission クラスについて説明します。
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
ms.openlocfilehash: 5b6c6c35e9d20bad3afc2cdb451bde093a0e3629
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502668"
---
# <a name="class-executepermission"></a>クラス ExecutePermission

[!include [banner](../../includes/banner.md)]

```xpp
class ExecutePermission extends CodeAccessPermission
```

ExecutePermission クラスは、X++ コードの実行を制御します。

## <a name="remarks"></a>備考

このクラスは、特定の API のアクセス許可をチェックするように設計されています。 アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission::dema メソッドが呼び出される同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。 次のいずれかの方法でサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

## <a name="examples"></a>例

次のコード例は、ExecutePermission クラスの新しいインスタンスを示しています。 assert メソッドが呼び出され、コードが Thread.new メソッドを呼び出して新規スレッドを作成できることが宣言されます。

```xpp
server static void main(Args args) 
{ 
    Thread _t; 
    ExecutePermission _perm; 
    _perm = new ExecutePermission(); 
    if (!_perm) 
    { 
        return; 
    } 
    _perm.assert(); 
    // Invoke the protected API. 
     _t = new Thread(); 
    // Call member methods. 
    if (_t) 
    { 
        _t.removeOnComplete(true); 
        _t.run(classnum(SysCodeProfiler), identifierstr(transferFile)); 
    } 
    // Optionally, call revertAssert() to limit scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。               |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。 |
| public void new()                                      | ExecutePermission クラスの新しいインスタンスを初期化します。                       |

## <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在のアクセス許可オブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。

## <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a>パラメーター - isSubsetOf

target  
CodeAccessPermission クラス オブジェクト。

### <a name="return-value---issubsetof"></a>戻り値 - isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。

## <a name="method-new"></a>メソッド new

ExecutePermission クラスの新しいインスタンスを初期化します。 終了。

```xpp
public void new()
```


