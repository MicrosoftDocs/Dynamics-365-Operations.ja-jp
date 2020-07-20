---
title: QueryBuildFieldList クラス
description: このトピックでは、QueryBuildFieldList クラスについて説明します。
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
ms.openlocfilehash: 96b8a8de2a3a02e5fc14abc8b010da40ddf53dd4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502867"
---
# <a name="class-querybuildfieldlist"></a>クラス QueryBuildFieldList

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildFieldList extends TreeNode
```

QueryBuildFieldList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                 | 説明 |
|--------------------------------------------------------------------------------------------------------|-------------|
| public int addAllFields(TableName tableName)                                                           |             |
| public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\]) |             |
| public int dynamic(\[int value\])                                                                      |             |
| public FieldId field(int index)                                                                        |             |
| public int fieldCount()                                                                                |             |
| public SelectionField fieldKind(int index)                                                             |             |
| public TableId tableSelector(int index)                                                                |             |
| public void clearFieldList()                                                                           |             |

## <a name="method-addallfields"></a>メソッド addAllFields

```xpp
public int addAllFields(TableName tableName)
```

### <a name="parameters---addallfields"></a>パラメーター - addAllFields

tableName  

### <a name="return-value---addallfields"></a>戻り値 - addAllFields

## <a name="method-addfield"></a>メソッド addField

```xpp
public QueryBuildFieldList addField(FieldId fieldId, [SelectionField fieldType], [int arrayIndex])
```

### <a name="parameters---addfield"></a>パラメーター - addField

fieldId  

<!-- -->

fieldType  

<!-- -->

arrayIndex  

### <a name="return-value---addfield"></a>戻り値 - addField

## <a name="method-dynamic"></a>メソッド dynamic

```xpp
public int dynamic([int value])
```

### <a name="parameters---dynamic"></a>パラメーター - dynamic

値  

### <a name="return-value---dynamic"></a>戻り値 - dynamic

## <a name="method-field"></a>メソッド field

```xpp
public FieldId field(int index)
```

### <a name="parameters---field"></a>パラメーター - field

指数  

### <a name="return-value---field"></a>戻り値 - field

## <a name="method-fieldcount"></a>メソッド fieldCount

```xpp
public int fieldCount()
```

### <a name="return-value---fieldcount"></a>戻り値 - fieldCount

## <a name="method-fieldkind"></a>メソッド fieldKind

```xpp
public SelectionField fieldKind(int index)
```

### <a name="parameters---fieldkind"></a>パラメーター - fieldKind

指数  

### <a name="return-value---fieldkind"></a>戻り値 - fieldKind

## <a name="method-tableselector"></a>メソッド tableSelector

```xpp
public TableId tableSelector(int index)
```

### <a name="parameters---tableselector"></a>パラメーター - tableSelector

指数  

### <a name="return-value---tableselector"></a>戻り値 - tableSelector

## <a name="method-clearfieldlist"></a>メソッド clearFieldList

```xpp
public void clearFieldList()
```

