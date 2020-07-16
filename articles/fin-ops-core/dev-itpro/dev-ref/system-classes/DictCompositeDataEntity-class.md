---
title: DictCompositeDataEntity クラス
description: このトピックでは、DictCompositeDataEntity クラスについて説明します。
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
ms.openlocfilehash: 75ff38b93b57fbbac7673f063f3c43e787b20f1d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502726"
---
# <a name="class-dictcompositedataentity"></a>クラス DictCompositeDataEntity

[!include [banner](../../includes/banner.md)]

```xpp
class DictCompositeDataEntity extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                       | 説明 |
|--------------------------------------------------------------|-------------|
| ::public static List listOfCompositeDataEntities()           |             |
| public str label()                                           |             |
| public boolean isReadOnly()                                  |             |
| public str modules()                                         |             |
| public str configurationKey()                                |             |
| public str countryRegionCodes()                              |             |
| public str countryRegionContextField()                       |             |
| public str developerDocumentation()                          |             |
| public EntityCategory entityCategory()                       |             |
| public str formRef()                                         |             |
| public str singularLabel()                                   |             |
| public str tags()                                            |             |
| public str publicCollectionName()                            |             |
| public str publicEntityName()                                |             |
| public int dataEntityCount()                                 |             |
| public DictCompositeChildDataEntity childDataEntityNo(int n) |             |
| public void new(str compositeDataEntityName)                 |             |

## <a name="method-listofcompositedataentities"></a>メソッド listOfCompositeDataEntities

```xpp
public static List listOfCompositeDataEntities()
```

### <a name="return-value---listofcompositedataentities"></a>戻り値 - listOfCompositeDataEntities

## <a name="method-label"></a>メソッド label

```xpp
public str label()
```

### <a name="return-value---label"></a>戻り値 - label

## <a name="method-isreadonly"></a>メソッド isReadOnly

```xpp
public boolean isReadOnly()
```

### <a name="return-value---isreadonly"></a>戻り値 - DictDataEntity

## <a name="method-modules"></a>メソッド modules

```xpp
public str modules()
```

### <a name="return-value---modules"></a>戻り値 - modules

## <a name="method-configurationkey"></a>メソッド configurationKey

```xpp
public str configurationKey()
```

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

## <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

```xpp
public str countryRegionCodes()
```

### <a name="return-value---countryregioncodes"></a>戻り値 - countryRegionCodes

## <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

```xpp
public str countryRegionContextField()
```

### <a name="return-value---countryregioncontextfield"></a>戻り値 - countryRegionContextField

## <a name="method-developerdocumentation"></a>メソッド developerDocumentation

```xpp
public str developerDocumentation()
```

### <a name="return-value---developerdocumentation"></a>戻り値 - developerDocumentation

## <a name="method-entitycategory"></a>メソッド entityCategory

```xpp
public EntityCategory entityCategory()
```

### <a name="return-value---entitycategory"></a>戻り値 - entityCategory

## <a name="method-formref"></a>メソッド formRef

```xpp
public str formRef()
```

### <a name="return-value---formref"></a>戻り値 - formRef

## <a name="method-singularlabel"></a>メソッド singularLabel

```xpp
public str singularLabel()
```

### <a name="return-value---singularlabel"></a>戻り値 - singularLabel

## <a name="method-tags"></a>メソッド tags

```xpp
public str tags()
```

### <a name="return-value---tags"></a>戻り値 - tags

## <a name="method-publiccollectionname"></a>メソッド publicCollectionName

```xpp
public str publicCollectionName()
```

### <a name="return-value---publiccollectionname"></a>戻り値 - publicCollectionName

## <a name="method-publicentityname"></a>メソッド publicEntityName

```xpp
public str publicEntityName()
```

### <a name="return-value---publicentityname"></a>戻り値 - publicEntityName

## <a name="method-dataentitycount"></a>メソッド dataEntityCount

```xpp
public int dataEntityCount()
```

### <a name="return-value---dataentitycount"></a>戻り値 - dataEntityCount

## <a name="method-childdataentityno"></a>メソッド childDataEntityNo

```xpp
public DictCompositeChildDataEntity childDataEntityNo(int n)
```

### <a name="parameters---childdataentityno"></a>パラメーター - childDataEntityNo

n  

### <a name="return-value---childdataentityno"></a>戻り値 - childDataEntityNo

## <a name="method-new"></a>メソッド new

```xpp
public void new(str compositeDataEntityName)
```

### <a name="parameters---new"></a>パラメーター - new

compositeDataEntityName  

