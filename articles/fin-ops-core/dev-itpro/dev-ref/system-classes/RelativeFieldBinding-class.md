---
title: RelativeFieldBinding クラス
description: このトピックでは、RelativeFieldBinding クラスについて説明します。
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
ms.openlocfilehash: 13ee2d4bd331854c60c5f38240f7286eaa496dc9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502850"
---
# <a name="class-relativefieldbinding"></a>クラス RelativeFieldBinding

[!include [banner](../../includes/banner.md)]

```xpp
class RelativeFieldBinding extends FieldBinding
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                   | 説明                                                   |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| public RelationPath relationPath()                                                       |                                                               |
| ::public static RelativeFieldBinding construct(str fieldName, RelationPath relationPath) |                                                               |
| ::public static RelativeFieldBinding create(container packedRelativeFieldBinding)        |                                                               |
| private void new()                                                                       | RelativeFieldBinding クラスの新しいインスタンスを初期化します。 |

## <a name="method-relationpath"></a>メソッド relationPath

```xpp
public RelationPath relationPath()
```

### <a name="return-value---relationpath"></a>戻り値 - relationPath

## <a name="method-construct"></a>メソッド construct

```xpp
public static RelativeFieldBinding construct(str fieldName, RelationPath relationPath)
```

### <a name="parameters---construct"></a>パラメーター - construct

fieldName  

<!-- -->

relationPath  

### <a name="return-value---construct"></a>戻り値 - construct

## <a name="method-create"></a>メソッド create

```xpp
public static RelativeFieldBinding create(container packedRelativeFieldBinding)
```

### <a name="parameters---create"></a>パラメーター - create

packedRelativeFieldBinding  

### <a name="return-value---create"></a>戻り値 - create

## <a name="method-new"></a>メソッド new

RelativeFieldBinding クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

