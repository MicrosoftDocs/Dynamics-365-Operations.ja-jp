---
title: CLRObject クラス
description: このトピックでは、CLRObject クラスについて説明します。
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
ms.openlocfilehash: d6edf1e79b28908a8079adff4459b2b6849ac0b1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502714"
---
# <a name="class-clrobject"></a>クラス CLRObject

[!include [banner](../../includes/banner.md)]

```xpp
class CLRObject extends Object
```

CLRObject クラスは、共通言語ランタイム (CLR) オブジェクトのインスタンスへの参照を保持し、X++ からの呼び出しを対応するラップされたマネージド インスタンスにディスパッチします。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                            | 説明                                   |
|---------------------------------------------------|-----------------------------------------------|
| private CLRObject dispatch(VarArg )               | 予約済み: メソッドを明示的に呼び出さないでください。 |
| public void new(str className, \[VarArg params\]) | CLRObject クラスのインスタンスを作成します。   |

## <a name="method-dispatch"></a>メソッド dispatch

予約済み: メソッドを明示的に呼び出さないでください。

```xpp
private CLRObject dispatch(VarArg )
```

### <a name="parameters---dispatch"></a>パラメーター - dispatch


### <a name="return-value---dispatch"></a>戻り値 - dispatch

### <a name="remarks---dispatch"></a>備考 - dispatch

攻撃者が出荷メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。

## <a name="method-new"></a>メソッド new

CLRObject クラスのインスタンスを作成します。

```xpp
public void new(str className, [VarArg params])
```

### <a name="parameters---new"></a>パラメーター - new

className  
インスタンスを作成する CLR クラスのコンストラクターの引数。

<!-- -->

params  
インスタンスを作成する CLR クラスのコンストラクターの引数。

### <a name="remarks---new"></a>備考 - new

CLRObject クラスのインスタンスは、CLR メソッドの呼び出しから返される値をラップするために使用されます。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーが新しいメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 新しい ClrObject オブジェクトをインスタンス化できない場合、例外: 例外内部はスローします。 元の CLR 例外を取得するには、CLRInterop::getLastException メソッドを呼び出します。

### <a name="examples---new"></a>例 - new

この例では、新しい System.Int32 CLR オブジェクトを作成します。

```xpp
void ClrObjectExample() 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    anytype retVal; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    perm.assert(); 
```

```xpp
    clrObj = new CLRObject("System.Int32"); 
```

```xpp
    CodeAccessPermission::revertAssert(); 
}
```

