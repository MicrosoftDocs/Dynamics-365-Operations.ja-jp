---
title: DLLFunction クラス
description: このトピックでは、DLLFunction クラスについて説明します。
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
ms.openlocfilehash: 9ef1ff41742eca42ab9cdad08ed94dfadb019fba
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502743"
---
# <a name="class-dllfunction"></a>クラス DLLFunction

[!include [banner](../../includes/banner.md)]

```xpp
class DLLFunction extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                           | 説明                                     |
|--------------------------------------------------|-------------------------------------------------|
| public AnyType call(VarArg )                     |                                                 |
| public ExtTypes returns(\[ExtTypes returnType\]) |                                                 |
| public void new(DLL dll, str functionname)       | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                           |                                                 |
| public void arg(VarArg )                         |                                                 |

## <a name="method-call"></a>メソッド call

```xpp
public AnyType call(VarArg )
```

### <a name="parameters---call"></a>パラメーター - call


### <a name="return-value---call"></a>戻り値 - call

### <a name="remarks---call"></a>備考 - call

攻撃者が呼び出しメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---call"></a>例 - call

次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。 コードのアクセス保護を提供する InteropPermission クラスの使用をアサートして、DLL をロードします。 これが成功した場合は、戻り値の型は DLLFunction クラスの呼び出しからを設定されます。

```xpp
{ 
    Dll               dll; 
    DllFunction       dllFunc; 
    anytype           retVal; 
    InteropPermission perm; 
    perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLL.new method. 
    // DLL.new is protected by code access security. 
    perm.assert(); 
    dll = new Dll("Kernel32.dll"); 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
    if (dll != null) 
    { 
        // Grants permission to execute the DLLFunction.new method. 
        // DLLFunction.new is protected by code access security. 
        perm = new InteropPermission(InteropKind::DllInterop); 
        perm.assert(); 
        dllFunc = new DllFunction(dll, "GetVersion"); 
        if (dllFunc != null) 
         { 
            dllFunc.returns(ExtTypes::DWord); 
             retVal = dllFunc.call(); 
         } 
       // Closes the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    } 
}
```

## <a name="method-returns"></a>メソッド returns

```xpp
public ExtTypes returns([ExtTypes returnType])
```

### <a name="parameters---returns"></a>パラメーター - returns

returnType  

### <a name="return-value---returns"></a>戻り値 - returns

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(DLL dll, str functionname)
```

### <a name="parameters---new"></a>パラメーター - new

dll  

<!-- -->

functionname  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-arg"></a>メソッド arg

```xpp
public void arg(VarArg )
```

### <a name="parameters---arg"></a>パラメーター - arg


