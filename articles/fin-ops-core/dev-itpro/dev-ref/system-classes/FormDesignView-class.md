---
title: FormDesignView クラス
description: このトピックでは、FormDesignView クラスについて説明します。
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
ms.openlocfilehash: 25d8b6974cbd766d02c2337a3fb5b0ba40467387
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502946"
---
# <a name="class-formdesignview"></a>クラス FormDesignView

[!include [banner](../../includes/banner.md)]

```xpp
class FormDesignView extends ObjectRun
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                     |
|--------------------------------------------------------|-------------------------------------------------|
| public FormBuildDesign design(\[int value\])           |                                                 |
| public Form form(\[Form value\])                       |                                                 |
| public str name()                                      |                                                 |
| public FormBuildObjectSet objectPool(\[AnyType pool\]) |                                                 |
| public void finalize()                                 |                                                 |
| public void new(\[str name\], \[Form form\])           | Object クラスの新しいインスタンスを初期化します。 |

## <a name="method-design"></a>メソッド design

```xpp
public FormBuildDesign design([int value])
```

### <a name="parameters---design"></a>パラメーター - design

値  

### <a name="return-value---design"></a>戻り値 - design

## <a name="method-form"></a>メソッド form

```xpp
public Form form([Form value])
```

### <a name="parameters---form"></a>パラメーター - form

値  

### <a name="return-value---form"></a>戻り値 - form

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-objectpool"></a>メソッド objectPool

```xpp
public FormBuildObjectSet objectPool([AnyType pool])
```

### <a name="parameters---objectpool"></a>パラメーター - objectPool

管理グループ  

### <a name="return-value---objectpool"></a>戻り値 - objectPool

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([str name], [Form form])
```

### <a name="parameters---new"></a>パラメーター - new

名前  

<!-- -->

フォーム  

