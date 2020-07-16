---
title: COMDispFunction クラス
description: このトピックでは、COMDispFunction クラスについて説明します。
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
ms.openlocfilehash: 05c71715d1bcfe33b2cbd3d30fe25779e46fbbda
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502717"
---
# <a name="class-comdispfunction"></a>クラス COMDispFunction

[!include [banner](../../includes/banner.md)]

```xpp
class COMDispFunction extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                                                                          |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| public int call(VarArg )                                                 |                                                                                                      |
| public AnyType callContainerOfParms(container parms)                     |                                                                                                      |
| public str toString()                                                    | 現在のオブジェクトを表す文字列を返します。                                                 |
| public void finalize()                                                   |                                                                                                      |
| public void new(COM comObject, str functionName, COMDispContext context) | オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。 |

## <a name="method-call"></a>メソッド call

```xpp
public int call(VarArg )
```

### <a name="parameters---call"></a>パラメーター - call


### <a name="return-value---call"></a>戻り値 - call

### <a name="remarks---call"></a>備考 - call

攻撃者が呼び出しメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

## <a name="method-callcontainerofparms"></a>メソッド callContainerOfParms

```xpp
public AnyType callContainerOfParms(container parms)
```

### <a name="parameters---callcontainerofparms"></a>パラメーター - callContainerOfParms

parms  

### <a name="return-value---callcontainerofparms"></a>戻り値 - callContainerOfParms

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。

```xpp
public void new(COM comObject, str functionName, COMDispContext context)
```

### <a name="parameters---new"></a>パラメーター - new

comObject  
アクセスする機能のコンテキスト。 次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF

<!-- -->

functionName  
アクセスする機能のコンテキスト。 次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF

<!-- -->

context  
アクセスする機能のコンテキスト。 次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF

### <a name="remarks---new"></a>備考 - new

COM オブジェクトは、同じ名前を使用する最大 4 つの機能を指定できるので、アクセスする COM オブジェクトで機能の正しいコンテキストを指定することが重要です。 使用可能な名前の衝突のため、コンテキストはメソッドまたはプロパティを区別するために使用されます。 正しいコンテキストを指定するには、アクセスする COM オブジェクトのドキュメントを参照してください。

### <a name="examples---new"></a>例 - new



```xpp
{ 
    InteropPermission perm; 
    COM com; 
    COMDispFunction funcShow; 
    COMDispFunction getValue; 
    COMDispFunction putValue; 
    ; 
```

```xpp
    perm = new InteropPermission(InteropKind::ComInterop); 
    perm.assert(); 
    com = new COM("MyCOM.Object"); 
    funcShow = 
        new COMDispFunction(com, "show",  COMDispContext::METHOD); 
    getValue = 
        new COMDispFunction(com, "value", COMDispContext::PROPERTYGET); 
    putValue = 
        new COMDispFunction(com, "value", COMDispContext::PROPERTYPUT); 
}
```

