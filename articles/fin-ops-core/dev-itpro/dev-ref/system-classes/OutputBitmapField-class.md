---
title: OutputBitmapField クラス
description: このトピックでは、OutputBitmapField クラスについて説明します。
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
ms.openlocfilehash: 12682c836a65bfd4b27f52568f17ea779a4e18df
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502558"
---
# <a name="class-outputbitmapfield"></a>クラス OutputBitmapField

[!include [banner](../../includes/banner.md)]

```xpp
class OutputBitmapField extends OutputField
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                     | 説明                                                |
|----------------------------|------------------------------------------------------------|
| public str imageFileName() |                                                            |
| public boolean resize()    |                                                            |
| public int resourceId()    |                                                            |
| public str toString()      | 現在のオブジェクトを表す文字列を返します。       |
| public container value()   |                                                            |
| public void new()          | OutputBitmapField クラスの新しいインスタンスを初期化します。 |

## <a name="method-imagefilename"></a>メソッド imageFileName

```xpp
public str imageFileName()
```

### <a name="return-value---imagefilename"></a>戻り値 - imageFileName

## <a name="method-resize"></a>メソッド resize

```xpp
public boolean resize()
```

### <a name="return-value---resize"></a>戻り値 - resize

## <a name="method-resourceid"></a>メソッド resourceId

```xpp
public int resourceId()
```

### <a name="return-value---resourceid"></a>戻り値 - resourceId

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

## <a name="method-new"></a>メソッド new

OutputBitmapField クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

