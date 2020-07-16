---
title: ImportTableSchemaInfo クラス
description: このトピックでは、ImportTableSchemaInfo クラスについて説明します。
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
ms.openlocfilehash: fec4c4416668dfb00ea73e46c41cddcb2a00ec44
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502597"
---
# <a name="class-importtableschemainfo"></a>クラス ImportTableSchemaInfo

[!include [banner](../../includes/banner.md)]

```xpp
class ImportTableSchemaInfo extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                             | 説明                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------|
| public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd) |                                                 |
| public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)        |                                                 |
| public int hasEqualityCriteria(boolean fHasEqualityCriteria)                       |                                                 |
| public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)                 |                                                 |
| public void new(int usTableId)                                                     | Object クラスの新しいインスタンスを初期化します。 |

## <a name="method-addcolumninfo"></a>メソッド addColumnInfo

```xpp
public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)
```

### <a name="parameters---addcolumninfo"></a>パラメーター - addColumnInfo

szColName  

<!-- -->

eColType  

<!-- -->

eColRole  

<!-- -->

lColOrd  

### <a name="return-value---addcolumninfo"></a>戻り値 - addColumnInfo

## <a name="method-addcolumnmapping"></a>メソッド addColumnMapping

```xpp
public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)
```

### <a name="parameters---addcolumnmapping"></a>戻り値 - addColumnMapping

szRefRecIdColName  

<!-- -->

szRefTableIdColName  

### <a name="return-value---addcolumnmapping"></a>戻り値 - addColumnMapping

## <a name="method-hasequalitycriteria"></a>メソッド hasEqualityCriteria

```xpp
public int hasEqualityCriteria(boolean fHasEqualityCriteria)
```

### <a name="parameters---hasequalitycriteria"></a>パラメーター - hasEqualityCriteria

fHasEqualityCriteria  

### <a name="return-value---hasequalitycriteria"></a>戻り値 - hasEqualityCriteria

## <a name="method-shreddedmetadatatable"></a>メソッド shreddedMetadataTable

```xpp
public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)
```

### <a name="parameters---shreddedmetadatatable"></a>パラメーター - shreddedMetadataTable

fIsShreddedMetadataTable  

### <a name="return-value---shreddedmetadatatable"></a>戻り値 - shreddedMetadataTable

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(int usTableId)
```

### <a name="parameters---new"></a>パラメーター - new

usTableId  

