---
title: TableExtension クラス
description: このトピックでは、TableExtension クラスについて説明します。
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
ms.openlocfilehash: a37db7c68c8050bb3862d6d9102aaac2a8bc32d8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502791"
---
# <a name="class-tableextension"></a>クラス TableExtension

[!include [banner](../../includes/banner.md)]


```xpp
class TableExtension extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                    | 説明                                             |
|-----------------------------------------------------------|---------------------------------------------------------|
| public void new()                                         | TableExtension クラスの新しいインスタンスを初期化します。 |
| public void modifiedField(Common record, FieldId fieldId) |                                                         |
| public void defaultRow(Common record)                     |                                                         |
| public void defaultField(Common record, FieldId fieldId)  |                                                         |

## <a name="method-new"></a>メソッド new

TableExtension クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-modifiedfield"></a>メソッド modifiedField

```xpp
public void modifiedField(Common record, FieldId fieldId)
```

### <a name="parameters---modifiedfield"></a>パラメーター - modifiedField

記録  

<!-- -->

fieldId  

## <a name="method-defaultrow"></a>メソッド defaultRow

```xpp
public void defaultRow(Common record)
```

### <a name="parameters---defaultrow"></a>パラメーター - defaultRow

記録  

## <a name="method-defaultfield"></a>メソッド defaultField

```xpp
public void defaultField(Common record, FieldId fieldId)
```

### <a name="parameters---defaultfield"></a>パラメーター - defaultField

記録  

<!-- -->

fieldId  

