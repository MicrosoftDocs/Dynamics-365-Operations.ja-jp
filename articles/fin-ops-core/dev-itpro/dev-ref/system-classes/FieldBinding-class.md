---
title: FieldBinding クラス
description: このトピックでは、FieldBinding クラスについて説明します。
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
ms.openlocfilehash: 9528d2c7ea59bb5fef17ecf6f27b6385dc437c9e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502980"
---
# <a name="class-fieldbinding"></a>クラス FieldBinding

[!include [banner](../../includes/banner.md)]


```xpp
class FieldBinding extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                   | 説明                                                |
|----------------------------------------------------------|------------------------------------------------------------|
| public int fieldArrayIndex()                             |                                                            |
| public int fieldId()                                     |                                                            |
| public str fieldName()                                   |                                                            |
| public boolean isEqualTo(FieldBinding otherFieldBinding) |                                                            |
| public boolean isNull()                                  |                                                            |
| public boolean isValid()                                 |                                                            |
| public container pack()                                  | FieldBinding クラスの現在のインスタンスをシリアル化します。 |
| public int tableId()                                     |                                                            |
| public str tableName()                                   |                                                            |
| public void new()                                        | FieldBinding クラスの新しいインスタンスを初期化します。      |

## <a name="method-fieldarrayindex"></a>メソッド fieldArrayIndex

```xpp
public int fieldArrayIndex()
```

### <a name="return-value---fieldarrayindex"></a>戻り値 - fieldArrayIndex

## <a name="method-fieldid"></a>メソッド fieldId

```xpp
public int fieldId()
```

### <a name="return-value---fieldid"></a>戻り値 - fieldId

## <a name="method-fieldname"></a>メソッド fieldName

```xpp
public str fieldName()
```

### <a name="return-value---fieldname"></a>戻り値 - fieldName

## <a name="method-isequalto"></a>メソッド isEqualTo

```xpp
public boolean isEqualTo(FieldBinding otherFieldBinding)
```

### <a name="parameters---isequalto"></a>パラメーター - isEqualTo

otherFieldBinding  

### <a name="return-value---isequalto"></a>戻り値 - isEqualTo

## <a name="method-isnull"></a>メソッド isNull

```xpp
public boolean isNull()
```

### <a name="return-value---isnull"></a>戻り値 - isNull

## <a name="method-isvalid"></a>メソッド isValid

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a>戻り値 - isValid

## <a name="method-pack"></a>メソッド pack

FieldBinding クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

FieldBinding クラスの現在のインスタンスを含むコンテナーです。

## <a name="method-tableid"></a>メソッド tableId

```xpp
public int tableId()
```

### <a name="return-value---tableid"></a>戻り値 - tableId

## <a name="method-tablename"></a>メソッド tableName

```xpp
public str tableName()
```

### <a name="return-value---tablename"></a>戻り値 - tableName

## <a name="method-new"></a>メソッド new

FieldBinding クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

