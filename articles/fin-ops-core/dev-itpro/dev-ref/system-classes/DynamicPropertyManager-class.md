---
title: DynamicPropertyManager クラス
description: このトピックでは、DynamicPropertyManager クラスについて説明します。
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
ms.openlocfilehash: 4bd66ea7386ac06c3a81086771fa4cc5c2a1b27f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502670"
---
# <a name="class-dynamicpropertymanager"></a>クラス DynamicPropertyManager

[!include [banner](../../includes/banner.md)]

```xpp
class DynamicPropertyManager extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                      | 説明                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| public DynamicPropertyCallback callbackObject()                                                                                                                                             |                                                                 |
| public str getConfigString()                                                                                                                                                                | Microsoft 社内のみで使用。                                    |
| public int hasSheetChanged()                                                                                                                                                                | Microsoft 社内のみで使用。                                    |
| public Struct propertyValues()                                                                                                                                                              |                                                                 |
| public void allowEdit(str name, boolean allow)                                                                                                                                              |                                                                 |
| public void updateValue(str propertyname, str value)                                                                                                                                        |                                                                 |
| public void new()                                                                                                                                                                           | DynamicPropertyManager クラスの新しいインスタンスを初期化します。 |
| public void getPropertySheet(str configString, boolean canWebletTypeChange)                                                                                                                 | Microsoft 社内のみで使用。                                    |
| public void noProperties()                                                                                                                                                                  |                                                                 |
| public void allowDisplay(str name, boolean allow)                                                                                                                                           |                                                                 |
| public void refresh()                                                                                                                                                                       |                                                                 |
| public void setProperties(int propertySetId, str caption, Struct values, \[Struct defaultValues\], \[Struct categories\], \[DynamicPropertyCallback callbackObject\], \[boolean setFocus\]) |                                                                 |

## <a name="method-callbackobject"></a>メソッド callbackObject

```xpp
public DynamicPropertyCallback callbackObject()
```

### <a name="return-value---callbackobject"></a>戻り値 - callbackObject

## <a name="method-getconfigstring"></a>メソッド getConfigString

Microsoft 社内のみで使用。

```xpp
public str getConfigString()
```

### <a name="return-value---getconfigstring"></a>戻り値 - getConfigString

コンフィギュレーションの文字列。

## <a name="method-hassheetchanged"></a>メソッド hasSheetChanged

Microsoft 社内のみで使用。

```xpp
public int hasSheetChanged()
```

### <a name="return-value---hassheetchanged"></a>戻り値 - hasSheetChanged

シートが変更されたかどうかを示す値。

## <a name="method-propertyvalues"></a>メソッド propertyValues

```xpp
public Struct propertyValues()
```

### <a name="return-value---propertyvalues"></a>戻り値 - propertyValues

## <a name="method-allowedit"></a>メソッド allowEdit

```xpp
public void allowEdit(str name, boolean allow)
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

名前  

<!-- -->

allow  

## <a name="method-updatevalue"></a>メソッド updateValue

```xpp
public void updateValue(str propertyname, str value)
```

### <a name="parameters---updatevalue"></a>パラメーター - updateValue

propertyname  

<!-- -->

値  

## <a name="method-new"></a>メソッド new

DynamicPropertyManager クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-getpropertysheet"></a>メソッド getPropertySheet

Microsoft 社内のみで使用。

```xpp
public void getPropertySheet(str configString, boolean canWebletTypeChange)
```

### <a name="parameters---getpropertysheet"></a>パラメーター - getPropertySheet

configString  
Weblet タイプが変更されたかどうかを示す値。

<!-- -->

canWebletTypeChange  
Weblet タイプが変更されたかどうかを示す値。

## <a name="method-noproperties"></a>メソッド noProperties

```xpp
public void noProperties()
```

## <a name="method-allowdisplay"></a>メソッド allowDisplay

```xpp
public void allowDisplay(str name, boolean allow)
```

### <a name="parameters---allowdisplay"></a>パラメーター - allowDisplay

名前  

<!-- -->

allow  

## <a name="method-refresh"></a>メソッド refresh

```xpp
public void refresh()
```

## <a name="method-setproperties"></a>メソッド setProperties

```xpp
public void setProperties(int propertySetId, str caption, Struct values, [Struct defaultValues], [Struct categories], [DynamicPropertyCallback callbackObject], [boolean setFocus])
```

### <a name="parameters---setproperties"></a>パラメーター - setProperties

propertySetId  

<!-- -->

caption  

<!-- -->

値  

<!-- -->

defaultValues  

<!-- -->

カテゴリ  

<!-- -->

callbackObject  

<!-- -->

setFocus  



