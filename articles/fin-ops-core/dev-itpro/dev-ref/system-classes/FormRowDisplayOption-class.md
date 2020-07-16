---
title: FormRowDisplayOption クラス
description: このトピックでは、FormRowDisplayOption クラスについて説明します。
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
ms.openlocfilehash: 8cb3ab5c164cb788c414c6f7c773700f13772236
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502621"
---
# <a name="class-formrowdisplayoption"></a>クラス FormRowDisplayOption

[!include [banner](../../includes/banner.md)]

```xpp
class FormRowDisplayOption extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                            | 説明 |
|-------------------------------------------------------------------|-------------|
| public int backColor(\[int color\])                               |             |
| public boolean fontBold(\[boolean bold\])                         |             |
| public boolean fontItalic(\[boolean italic\])                     |             |
| public boolean fontStrikethrough(\[boolean strikethrough\])       |             |
| public boolean fontUnderline(\[boolean underline\])               |             |
| public int textColor(\[int color\])                               |             |
| public void clear()                                               |             |
| public void clearTextColor()                                      |             |
| public void affectedElementsByField(\[FieldId fieldId\], VarArg ) |             |
| public void affectedElementsByControl(\[int controlId\], VarArg ) |             |
| public void clearBackColor()                                      |             |

## <a name="method-backcolor"></a>メソッド backColor

```xpp
public int backColor([int color])
```

### <a name="parameters---backcolor"></a>パラメーター - backColor

色  

### <a name="return-value---backcolor"></a>戻り値 - backColor

## <a name="method-fontbold"></a>メソッド fontBold

```xpp
public boolean fontBold([boolean bold])
```

### <a name="parameters---fontbold"></a>パラメーター - fontBold

太字  

### <a name="return-value---fontbold"></a>戻り値 - fontBold

## <a name="method-fontitalic"></a>メソッド fontItalic

```xpp
public boolean fontItalic([boolean italic])
```

### <a name="parameters---fontitalic"></a>パラメーター - fontItalic

斜体  

### <a name="return-value---fontitalic"></a>戻り値 - fontItalic

## <a name="method-fontstrikethrough"></a>メソッド fontStrikethrough

```xpp
public boolean fontStrikethrough([boolean strikethrough])
```

### <a name="parameters---fontstrikethrough"></a>パラメーター - fontStrikethrough

取り消し線  

### <a name="return-value---fontstrikethrough"></a>戻り値 - fontStrikethrough

## <a name="method-fontunderline"></a>メソッド fontUnderline

```xpp
public boolean fontUnderline([boolean underline])
```

### <a name="parameters---fontunderline"></a>パラメーター - fontUnderline

下線  

### <a name="return-value---fontunderline"></a>戻り値 - fontUnderline

## <a name="method-textcolor"></a>メソッド textColor

```xpp
public int textColor([int color])
```

### <a name="parameters---textcolor"></a>パラメーター - textColor

色  

### <a name="return-value---textcolor"></a>戻り値 - textColor

## <a name="method-clear"></a>メソッド clear

```xpp
public void clear()
```

## <a name="method-cleartextcolor"></a>メソッド clearTextColor

```xpp
public void clearTextColor()
```

## <a name="method-affectedelementsbyfield"></a>メソッド affectedElementsByField

```xpp
public void affectedElementsByField([FieldId fieldId], VarArg )
```

### <a name="parameters---affectedelementsbyfield"></a>パラメーター - affectedElementsByField

fieldId  

<!-- -->


## <a name="method-affectedelementsbycontrol"></a>メソッド affectedElementsByControl

```xpp
public void affectedElementsByControl([int controlId], VarArg )
```

### <a name="parameters---affectedelementsbycontrol"></a>パラメーター - affectedElementsByControl

controlId  

<!-- -->


## <a name="method-clearbackcolor"></a>メソッド clearBackColor

```xpp
public void clearBackColor()
```

