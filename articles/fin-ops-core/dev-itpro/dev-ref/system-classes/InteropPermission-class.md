---
title: InteropPermission クラス
description: このトピックでは、InteropPermission クラスについて説明します。
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
ms.openlocfilehash: 599d2bfeba84107e6868732a64658e76b3f8409d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502596"
---
# <a name="class-interoppermission"></a>クラス InteropPermission

[!include [banner](../../includes/banner.md)]

```xpp
class InteropPermission extends CodeAccessPermission
```

InteropPermission クラスは、アンマネージド コードとマネージド コードを呼び出す機能を制御します。

## <a name="remarks"></a>備考

InteropPermission クラスは、特定の API のアクセス許可をチェックするように設計されています。 アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API を実行する前に、対応する CodeAccessPermission::demand メソッドが呼び出されている同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。 次のいずれかの方法でサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。

## <a name="examples"></a>例

次のコード例は、InteropPermission クラスの新しいインスタンスを示しています。 assert メソッドが呼び出され、コードが、Microsoft Windows ダイナミックリンク ライブラリ (DLL) と通信する機能を提供する DLL クラスをインスタンス化できることが宣言されます。

```xpp
server static void main(Args args) 
{ 
    InteropPermission _perm; 
    DLL _dll; 
    _perm = new InteropPermission(InteropKind::DllInterop); 
    _perm.assert(); 
    // Invoke the protected API. 
    _dll = new DLL('cfx2032.dll'); 
    // Optionally, call revertAssert() to limit the scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a>方法

| 方法                                                 | 説明                                                                        |
|--------------------------------------------------------|------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。                 |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。 |
| public void new(InteropKind kind)                      | InteropPermission クラスの新しいインスタンスを作成します。                            |

## <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在のアクセス許可オブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「メソッドのコピー」を参照してください。

## <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a>パラメーター - isSubsetOf

target  
CodeAccessPermission クラス オブジェクト。

### <a name="return-value---issubsetof"></a>戻り値 - isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「isSubsetOf メソッド」を参照してください。

## <a name="method-new"></a>メソッド new

InteropPermission クラスの新しいインスタンスを作成します。

```xpp
public void new(InteropKind kind)
```

### <a name="parameters---new"></a>パラメーター - new

kind  
マネージドまたはアンマネージド コードへのアクセスを指定する InteropKind システム列挙値です。

### <a name="examples---new"></a>例 - new

次のコード例は、Win32 DLL へのアクセス許可を指定する InteropPermission クラスの新しいインスタンスを示しています。

```xpp
server static void main(Args args) 
{ 
    InteropPermission _perm; 
    _perm = new InteropPermission(InteropKind::DllInterop); 
}
```

