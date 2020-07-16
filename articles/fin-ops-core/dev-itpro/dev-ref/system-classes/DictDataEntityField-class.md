---
title: DictDataEntityField クラス
description: このトピックでは、DictDataEntityField クラスについて説明します。
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
ms.openlocfilehash: 3336006f589102b5abbbae6375edfa69866e7eb1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502989"
---
# <a name="class-dictdataentityfield"></a>クラス DictDataEntityField

[!include [banner](../../includes/banner.md)]

```xpp
class DictDataEntityField extends DictField
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                | 説明 |
|-----------------------------------------------------------------------|-------------|
| public FieldAccessModifier accessModifier()                           |             |
| public str dataEntityViewMethod()                                     |             |
| public str dataField()                                                |             |
| public str dataSource()                                               |             |
| public str dimensionLegalEntityContextField()                         |             |
| public str dynamicDimensionEnumerationField()                         |             |
| public boolean IsComputedField()                                      |             |
| public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\]) |             |

## <a name="method-accessmodifier"></a>メソッド accessModifier

```xpp
public FieldAccessModifier accessModifier()
```

### <a name="return-value---accessmodifier"></a>戻り値 - accessModifier

## <a name="method-dataentityviewmethod"></a>メソッド dataEntityViewMethod

```xpp
public str dataEntityViewMethod()
```

### <a name="return-value---dataentityviewmethod"></a>戻り値 - dataEntityViewMethod

## <a name="method-datafield"></a>メソッド dataField

```xpp
public str dataField()
```

### <a name="return-value---datafield"></a>戻り値 - dataField

## <a name="method-datasource"></a>メソッド dataSource

```xpp
public str dataSource()
```

### <a name="return-value---datasource"></a>戻り値 - dataSource

## <a name="method-dimensionlegalentitycontextfield"></a>メソッド dimensionLegalEntityContextField

```xpp
public str dimensionLegalEntityContextField()
```

### <a name="return-value---dimensionlegalentitycontextfield"></a>戻り値 - dimensionLegalEntityContextField

## <a name="method-dynamicdimensionenumerationfield"></a>メソッド dynamicDimensionEnumerationField

```xpp
public str dynamicDimensionEnumerationField()
```

### <a name="return-value---dynamicdimensionenumerationfield"></a>戻り値 - dynamicDimensionEnumerationField

## <a name="method-iscomputedfield"></a>メソッド IsComputedField

```xpp
public boolean IsComputedField()
```

### <a name="return-value---iscomputedfield"></a>戻り値 - IsComputedField

## <a name="method-new"></a>メソッド new

```xpp
public void new(TableId tableId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---new"></a>パラメーター - new

tableId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

