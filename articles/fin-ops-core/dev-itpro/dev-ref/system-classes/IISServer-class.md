---
title: IISServer クラス
description: このトピックでは、IISServer クラスについて説明します。
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
ms.openlocfilehash: 26334a1111979ccb686b7693fa8eb054625aeb5f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502907"
---
# <a name="class-iisserver"></a>クラス IISServer

[!include [banner](../../includes/banner.md)]

```xpp
class IISServer extends Object
```

IISServer クラスは、インターネット インフォメーション サービス (IIS) によって提供される Server オブジェクトをラップします。

## <a name="remarks"></a>備考

IISServer クラスのメソッドと、IIS によって提供される Server オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISServer クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISServer クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                           | 説明                                        |
|--------------------------------------------------|----------------------------------------------------|
| public COM createObject(str progID)              |                                                    |
| public str htmlEncode(str txt)                   |                                                    |
| public ComInterface interface()                  |                                                    |
| public str mapPath(str logicalPath)              |                                                    |
| public int scriptTimeout(\[int timeoutSeconds\]) |                                                    |
| public str urlEncode(str txt)                    |                                                    |
| public str urlPathEncode(str txt)                |                                                    |
| public void execute(str logicalPath)             |                                                    |
| public void transfer(str logicalPath)            |                                                    |
| public void new()                                | IISServer クラスの新しいインスタンスを初期化します。 |
| public void finalize()                           |                                                    |

## <a name="method-createobject"></a>メソッド createObject

```xpp
public COM createObject(str progID)
```

### <a name="parameters---createobject"></a>パラメーター - createObject

progID  

### <a name="return-value---createobject"></a>戻り値 - createObject

## <a name="method-htmlencode"></a>メソッド htmlEncode

```xpp
public str htmlEncode(str txt)
```

### <a name="parameters---htmlencode"></a>パラメーター - htmlEncode

txt  

### <a name="return-value---htmlencode"></a>戻り値 - htmlEncode

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-mappath"></a>メソッド mapPath

```xpp
public str mapPath(str logicalPath)
```

### <a name="parameters---mappath"></a>パラメーター - mapPath

logicalPath  

### <a name="return-value---mappath"></a>戻り値 - mapPath

## <a name="method-scripttimeout"></a>メソッド scriptTimeout

```xpp
public int scriptTimeout([int timeoutSeconds])
```

### <a name="parameters---scripttimeout"></a>パラメーター - scriptTimeout

timeoutSeconds  

### <a name="return-value---scripttimeout"></a>戻り値 - scriptTimeout

## <a name="method-urlencode"></a>メソッド urlEncode

```xpp
public str urlEncode(str txt)
```

### <a name="parameters---urlencode"></a>パラメーター - urlEncode

txt  

### <a name="return-value---urlencode"></a>戻り値 - urlEncode

## <a name="method-urlpathencode"></a>メソッド urlPathEncode

```xpp
public str urlPathEncode(str txt)
```

### <a name="parameters---urlpathencode"></a>パラメーター - urlPathEncode

txt  

### <a name="return-value---urlpathencode"></a>戻り値 - urlPathEncode

## <a name="method-execute"></a>メソッド execute

```xpp
public void execute(str logicalPath)
```

### <a name="parameters---execute"></a>パラメーター - execute

logicalPath  

## <a name="method-transfer"></a>メソッド transfer

```xpp
public void transfer(str logicalPath)
```

### <a name="parameters---transfer"></a>パラメーター - transfer

logicalPath  

## <a name="method-new"></a>メソッド new

IISServer クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

