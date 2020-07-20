---
title: FormListItem クラス
description: このトピックでは、FormListItem クラスについて説明します。
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
ms.openlocfilehash: 2216f006d1465ec783fa24c0f06f6fa4dceec3ae
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502929"
---
# <a name="class-formlistitem"></a>クラス FormListItem

[!include [banner](../../includes/banner.md)]

```xpp
class FormListItem extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                         | 説明                                          |
|----------------------------------------------------------------|------------------------------------------------------|
| public AnyType data(\[AnyType value\])                         |                                                      |
| public int idx(\[int value\])                                  |                                                      |
| public int image(\[int value\])                                |                                                      |
| public int indent(\[int value\])                               |                                                      |
| public int overlayImage(\[int value\])                         |                                                      |
| public boolean stateChecked(\[boolean value\])                 |                                                      |
| public boolean stateCut(\[boolean value\])                     |                                                      |
| public boolean stateDropHilited(\[boolean value\])             |                                                      |
| public boolean stateFocus(\[boolean value\])                   |                                                      |
| public int stateImage(\[int value\])                           |                                                      |
| public boolean stateSelected(\[boolean value\])                |                                                      |
| public int subItem(\[int value\])                              |                                                      |
| public str text(\[str value\])                                 |                                                      |
| public str toString()                                          | 現在のオブジェクトを表す文字列を返します。 |
| public void finalize()                                         |                                                      |
| public void new(\[str Text\], \[int Image\], \[AnyType Data\]) | Object クラスの新しいインスタンスを初期化します。      |

## <a name="method-data"></a>メソッド data

```xpp
public AnyType data([AnyType value])
```

### <a name="parameters---data"></a>パラメーター - data

値  

### <a name="return-value---data"></a>戻り値 - data

## <a name="method-idx"></a>メソッド idx

```xpp
public int idx([int value])
```

### <a name="parameters---idx"></a>パラメーター - idx

値  

### <a name="return-value---idx"></a>戻り値 - idx

## <a name="method-image"></a>メソッド image

```xpp
public int image([int value])
```

### <a name="parameters---image"></a>パラメーター - image

値  

### <a name="return-value---image"></a>戻り値 - image

## <a name="method-indent"></a>メソッド indent

```xpp
public int indent([int value])
```

### <a name="parameters---indent"></a>パラメーター - indent

値  

### <a name="return-value---indent"></a>戻り値 - indent

## <a name="method-overlayimage"></a>メソッド overlayImage

```xpp
public int overlayImage([int value])
```

### <a name="parameters---overlayimage"></a>パラメーター - overlayImage

値  

### <a name="return-value---overlayimage"></a>戻り値 - overlayImage

## <a name="method-statechecked"></a>メソッド stateChecked

```xpp
public boolean stateChecked([boolean value])
```

### <a name="parameters---statechecked"></a>パラメーター - stateChecked

値  

### <a name="return-value---statechecked"></a>戻り値 - stateChecked

## <a name="method-statecut"></a>メソッド stateCut

```xpp
public boolean stateCut([boolean value])
```

### <a name="parameters---statecut"></a>パラメーター - stateCut

値  

### <a name="return-value---statecut"></a>戻り値 - stateCut

## <a name="method-statedrophilited"></a>メソッド stateDropHilited

```xpp
public boolean stateDropHilited([boolean value])
```

### <a name="parameters---statedrophilited"></a>パラメーター - stateDropHilited

値  

### <a name="return-value---statedrophilited"></a>戻り値 - stateDropHilited

## <a name="method-statefocus"></a>メソッド stateFocus

```xpp
public boolean stateFocus([boolean value])
```

### <a name="parameters---statefocus"></a>パラメーター - stateFocus

値  

### <a name="return-value---statefocus"></a>戻り値 - stateFocus

## <a name="method-stateimage"></a>メソッド stateImage

```xpp
public int stateImage([int value])
```

### <a name="parameters---stateimage"></a>パラメーター - stateImage

値  

### <a name="return-value---stateimage"></a>戻り値 - stateImage

## <a name="method-stateselected"></a>メソッド stateSelected

```xpp
public boolean stateSelected([boolean value])
```

### <a name="parameters---stateselected"></a>パラメーター - stateSelected

値  

### <a name="return-value---stateselected"></a>戻り値 - stateSelected

## <a name="method-subitem"></a>メソッド subItem

```xpp
public int subItem([int value])
```

### <a name="parameters---subitem"></a>パラメーター - subItem

値  

### <a name="return-value---subitem"></a>戻り値 - subItem

## <a name="method-text"></a>メソッド text

```xpp
public str text([str value])
```

### <a name="parameters---text"></a>パラメーター - text

値  

### <a name="return-value---text"></a>戻り値 - text

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

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([str Text], [int Image], [AnyType Data])
```

### <a name="parameters---new"></a>パラメーター - new

テキスト  

<!-- -->

画像  

<!-- -->

データ  

