---
title: QueryBuildStaticlink クラス
description: このトピックでは、QueryBuildStaticlink クラスについて説明します。
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
ms.openlocfilehash: e175167010565f1e356ab31e6aac689950d14f6e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502863"
---
# <a name="class-querybuildstaticlink"></a>クラス QueryBuildStaticlink

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildStaticlink extends Object
```

QueryBuildStaticLink クラスは、QueryBuildDataSource クラスで定義されている静的リンクに関する情報を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                 | 説明                                                         |
|------------------------|---------------------------------------------------------------------|
| public FieldId field() | 静的リンクが定義されているフィールド情報を提供します/ |
| public AnyType value() | 静的リンクが定義されているフィールドの値を取得します。    |
| public void finalize() |                                                                     |

## <a name="method-field"></a>メソッド field

静的リンクが定義されているフィールド情報を提供します/

```xpp
public FieldId field()
```

### <a name="return-value---field"></a>戻り値 - field

静的リンクが定義されているフィールドの FieldId 値。

## <a name="method-value"></a>メソッド value

静的リンクが定義されているフィールドの値を取得します。

```xpp
public AnyType value()
```

### <a name="return-value---value"></a>戻り値 - value

静的リンクの値。

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

