---
title: FormObject クラス
description: このトピックでは、FormObject クラスについて説明します。
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
ms.openlocfilehash: fe27976739e8a42c1270e274759af48bf1b4a3a2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502927"
---
# <a name="class-formobject"></a>クラス FormObject

[!include [banner](../../includes/banner.md)]


```xpp
class FormObject extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                        | 説明                             |
|-----------------------------------------------|-----------------------------------------|
| public boolean getAllowEdit(\[int rowIndex\]) |                                         |
| public AnyType getValue(\[int rowIndex\])     |                                         |
| public boolean getVisible()                   |                                         |
| public str helpField()                        | コントロールのヘルプ テキストを返します。  |
| public str labelText()                        | コントロールのラベル テキストを返します。 |
| public boolean setValue(AnyType value)        |                                         |
| public str toolTip()                          |                                         |
| public boolean validate()                     |                                         |
| public void jumpRef()                         |                                         |
| public void modified()                        |                                         |
| public void restore()                         |                                         |
| public void find()                            |                                         |
| public void context()                         |                                         |

## <a name="method-getallowedit"></a>メソッド getAllowEdit

```xpp
public boolean getAllowEdit([int rowIndex])
```

### <a name="parameters---getallowedit"></a>パラメーター - getAllowEdit

rowIndex  

### <a name="return-value---getallowedit"></a>戻り値 - getAllowEdit

## <a name="method-getvalue"></a>メソッド getValue

```xpp
public AnyType getValue([int rowIndex])
```

### <a name="parameters---getvalue"></a>パラメーター - getValue

rowIndex  

### <a name="return-value---getvalue"></a>戻り値 - getValue

## <a name="method-getvisible"></a>メソッド getVisible

```xpp
public boolean getVisible()
```

### <a name="return-value---getvisible"></a>戻り値 - getVisible

## <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを返します。

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a>戻り値 - helpField

コントロールのヘルプ テキスト。ヘルプ テキストがない場合は空の文字列。

### <a name="examples---helpfield"></a>例 - helpField

次の例は、helpField メソッドの使用方法を示しています。

```xpp
str strHelp;
strHelp = this.helpField();
```

## <a name="method-labeltext"></a>メソッド labelText

コントロールのラベル テキストを返します。

```xpp
public str labelText()
```

### <a name="return-value---labeltext"></a>戻り値 - labelText

コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。

## <a name="method-setvalue"></a>メソッド setValue

```xpp
public boolean setValue(AnyType value)
```

### <a name="parameters---setvalue"></a>パラメーター - setValue

値  

### <a name="return-value---setvalue"></a>戻り値 - setValue

## <a name="method-tooltip"></a>メソッド toolTip

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a>戻り値 - toolTip

## <a name="method-validate"></a>メソッド validate

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a>戻り値 - validate

## <a name="method-jumpref"></a>メソッド jumpRef

```xpp
public void jumpRef()
```

## <a name="method-modified"></a>メソッド modified

```xpp
public void modified()
```

## <a name="method-restore"></a>メソッド restore

```xpp
public void restore()
```

## <a name="method-find"></a>メソッド find

```xpp
public void find()
```

## <a name="method-context"></a>メソッド context

```xpp
public void context()
```

