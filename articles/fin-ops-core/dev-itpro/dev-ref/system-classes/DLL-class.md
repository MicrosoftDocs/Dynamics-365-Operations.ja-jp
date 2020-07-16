---
title: DLL クラス
description: このトピックでは、DLL クラスについて説明します。
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
ms.openlocfilehash: db06244b679d4e59bca6e1ab2841e2c5861014bb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502698"
---
# <a name="class-dll"></a>クラス DLL

[!include [banner](../../includes/banner.md)]

```xpp
class DLL extends Object
```

DLL クラスでは、Microsoft Windows 動的リンク ライブラリ (DLL) との通信が有効になります。

## <a name="remarks"></a>備考

Unicode DLL を使用している場合は、次の操作を行います。

-   ExtTypes::String の代わりに ExtTypes::WString を使用して、文字列型を指定します。
-   文字データがバイナリ構造に埋め込まれている場合は、Binary::String ではなく Binary::WString を使用します。
-   バイナリオ オブジェクトから文字列を読み取る必要がある場合は、Binary.string メソッドの代わりに Binary.wstring メソッドを使用します。

## <a name="examples"></a>例

次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。 この例では、コードがサーバー上で実行されている場合にのみ必要な InteropPermission クラスの使用をアサートします。 DLL を読み込み、成功した場合は DLLFunction クラスの呼び出しから戻り値の型を設定します。

```xpp
void DLLExample() 
{ 
    Dll               dll; 
    DllFunction       dllFunc; 
    anytype           retVal; 
    InteropPermission perm; 
    perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLL.new method.  
    // DLL.new runs under code access security. 
    perm.assert(); 
    dll = new Dll("Kernel32.dll"); 
    // Closes the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    if (dll != null) 
    { 
        perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLLFunction.new method.  
    // DLLFunction.new runs under code access security. 
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

## <a name="methods"></a>方法

| 方法                             | 説明                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------|
| ::public static int lastDLLError() | DLL によって報告された最後のエラーを設定または取得します。                            |
| public void new(str filename)      | DLL クラスのインスタンスを作成します。                                                     |
| public void finalize()             | リソースを解放し、DLL クラスのインスタンスがリリースされる前にクリーンアップを実行します。 |

## <a name="method-lastdllerror"></a>メソッド lastDLLError

DLL によって報告された最後のエラーを設定または取得します。

```xpp
public static int lastDLLError()
```

### <a name="return-value---lastdllerror"></a>戻り値 - lastDLLError

DLL によって報告された最後のエラー。

## <a name="method-new"></a>メソッド new

DLL クラスのインスタンスを作成します。

```xpp
public void new(str filename)
```

### <a name="parameters---new"></a>パラメーター - new

filename  
DLL クラスのインスタンスを作成するために使用する DLL のファイル名。

### <a name="remarks---new"></a>備考 - new

DLL 関数にアクセスするには、DLLFunction::new メソッドの呼び出しで、その DLL クラスの作成されたインスタンスを使用します。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---new"></a>例 - new

次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。 この例では、InteropPermission クラスの使用をアサートします。 DLL を読み込み、成功した場合は DLLFunction クラスでの呼び出しから戻り値の型を設定します。

```xpp
void DLLExample() 
{ 
    Dll               dll; 
    DllFunction       dllFunc; 
    anytype           retVal; 
    InteropPermission perm; 
    perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLL.new method. 
    // DLL.new runs under code access security. 
    perm.assert(); 
    dll = new Dll("Kernel32.dll"); 
    // Closes the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    if (dll != null) 
    { 
        perm = new InteropPermission(InteropKind::DllInterop); 
       // Grants permission to execute the DLLFunction.new method. 
       // DLLFunction.new runs under code access security. 
        perm.assert(); 
        dllFunc = new DllFunction(dll, "GetVersion"); 
        if (dllFunc != null) 
        { 
             dllFunc.returns(ExtTypes::DWord); 
            retVal = dllFunc.call(); 
        } 
        // Close the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    } 
}
```

## <a name="method-finalize"></a>メソッド finalize

リソースを解放し、DLL クラスのインスタンスがリリースされる前にクリーンアップを実行します。

```xpp
public void finalize()
```

