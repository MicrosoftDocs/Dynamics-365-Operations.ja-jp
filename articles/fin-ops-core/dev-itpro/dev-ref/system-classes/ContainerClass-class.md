---
title: ContainerClass クラス
description: このトピックでは、ContainerClass クラスについて説明します。
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
ms.openlocfilehash: fef01fdb5faf6fa6ad52dd7b02694b3aa57639b5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502704"
---
# <a name="class-containerclass"></a>クラス ContainerClass

[!include [banner](../../includes/banner.md)]

```xpp
class ContainerClass extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                              | 説明                                          |
|---------------------------------------------------------------------|------------------------------------------------------|
| public int length()                                                 |                                                      |
| public container toBlob()                                           |                                                      |
| public str toString()                                               | 現在のオブジェクトを表す文字列を返します。 |
| public container value()                                            |                                                      |
| ::public static container blob2Container(container blob\_container) |                                                      |
| ::public static int containerLength(container container)            |                                                      |
| public void new(container container)                                | Object クラスの新しいインスタンスを初期化します。      |

## <a name="method-length"></a>メソッド length

```xpp
public int length()
```

### <a name="return-value---length"></a>戻り値 - length

## <a name="method-toblob"></a>メソッド toBlob

```xpp
public container toBlob()
```

### <a name="return-value---toblob"></a>戻り値 - toBlob

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-value"></a>メソッド value

```xpp
public container value()
```

### <a name="return-value---value"></a>戻り値 - value

## <a name="method-blob2container"></a>メソッド blob2Container

```xpp
public static container blob2Container(container blob_container)
```

### <a name="parameters---blob2container"></a>パラメーター - blob2Container

blob\_container  

### <a name="return-value---blob2container"></a>戻り値 - blob2Container

## <a name="method-containerlength"></a>メソッド containerLength

```xpp
public static int containerLength(container container)
```

### <a name="parameters---containerlength"></a>パラメーター - containerLength

コンテナー  

### <a name="return-value---containerlength"></a>戻り値 - containerLength

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(container container)
```

### <a name="parameters---new"></a>パラメーター - new

コンテナー  

