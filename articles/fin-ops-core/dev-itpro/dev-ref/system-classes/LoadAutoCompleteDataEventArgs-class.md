---
title: LoadAutoCompleteDataEventArgs クラス
description: このトピックでは、LoadAutoCompleteDataEventArgs クラスについて説明します。
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
ms.openlocfilehash: 9b23200afd7f1dd20124238bca457a84a4067ab2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502891"
---
# <a name="class-loadautocompletedataeventargs"></a>クラス LoadAutoCompleteDataEventArgs

[!include [banner](../../includes/banner.md)]

```xpp
class LoadAutoCompleteDataEventArgs extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                          | 説明 |
|-------------------------------------------------------------------------------------------------|-------------|
| public AutoCompleteDataMode autoCompleteDataMode(\[AutoCompleteDataMode autoCompleteDataMode\]) |             |
| public boolean canPage(\[boolean canPage\])                                                     |             |
| public str filterValue()                                                                        |             |
| public AnyType lastPagedTag()                                                                   |             |
| public FormSegment segment()                                                                    |             |
| public void addAutoCompleteData(str value, str description, AnyType tag)                        |             |

## <a name="method-autocompletedatamode"></a>メソッド autoCompleteDataMode

```xpp
public AutoCompleteDataMode autoCompleteDataMode([AutoCompleteDataMode autoCompleteDataMode])
```

### <a name="parameters---autocompletedatamode"></a>パラメーター - autoCompleteDataMode

autoCompleteDataMode  

### <a name="return-value---autocompletedatamode"></a>戻り値 - autoCompleteDataMode

## <a name="method-canpage"></a>メソッド canPage

```xpp
public boolean canPage([boolean canPage])
```

### <a name="parameters---canpage"></a>パラメーター - canPage

canPage  

### <a name="return-value---canpage"></a>戻り値 - canPage

## <a name="method-filtervalue"></a>メソッド filterValue

```xpp
public str filterValue()
```

### <a name="return-value---filtervalue"></a>戻り値 - filterValue

## <a name="method-lastpagedtag"></a>メソッド lastPagedTag

```xpp
public AnyType lastPagedTag()
```

### <a name="return-value---lastpagedtag"></a>戻り値 - lastPagedTag

## <a name="method-segment"></a>メソッド segment

```xpp
public FormSegment segment()
```

### <a name="return-value---segment"></a>戻り値 - segment

## <a name="method-addautocompletedata"></a>メソッド addAutoCompleteData

```xpp
public void addAutoCompleteData(str value, str description, AnyType tag)
```

### <a name="parameters---addautocompletedata"></a>パラメーター - addAutoCompleteData

値  

<!-- -->

説明  

<!-- -->

タグ  

