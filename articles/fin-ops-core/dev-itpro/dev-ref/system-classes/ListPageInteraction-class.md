---
title: ListPageInteraction クラス
description: このトピックでは、ListPageInteraction クラスについて説明します。
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
ms.openlocfilehash: a750d21cc16a0f8282b3b80a6e06e652d31b3e4f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502589"
---
# <a name="class-listpageinteraction"></a>クラス ListPageInteraction

[!include [banner](../../includes/banner.md)]

```xpp
class ListPageInteraction extends PageInteraction
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                           | 説明                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| public ListPage listPage()                       |                                                               |
| public void tabChanged(container activeTabNames) | アクティブなタブが変更されたときに呼び出されます。                        |
| public void initializing()                       |                                                               |
| public void initialized()                        |                                                               |
| public void selectionChanged()                   |                                                               |
| public void initializeQuery(Query query)         |                                                               |
| public void new(ListPage listPage)               | listPage 上で動作する新しい PageInteraction オブジェクトを作成します。 |

## <a name="method-listpage"></a>メソッド listPage

```xpp
public ListPage listPage()
```

### <a name="return-value---listpage"></a>戻り値 - listPage

## <a name="method-tabchanged"></a>メソッド tabChanged

アクティブなタブが変更されたときに呼び出されます。

```xpp
public void tabChanged(container activeTabNames)
```

### <a name="parameters---tabchanged"></a>パラメーター - tabChanged

activeTabNames  
アクティブなタブの名前を含むコンテナーです。

## <a name="method-initializing"></a>メソッド initializing

```xpp
public void initializing()
```

## <a name="method-initialized"></a>メソッド initialized

```xpp
public void initialized()
```

## <a name="method-selectionchanged"></a>メソッド selectionChanged

```xpp
public void selectionChanged()
```

## <a name="method-initializequery"></a>メソッド initializeQuery

```xpp
public void initializeQuery(Query query)
```

### <a name="parameters---initializequery"></a>パラメーター - initializeQuery

クエリ  

## <a name="method-new"></a>メソッド new

listPage 上で動作する新しい PageInteraction オブジェクトを作成します。

```xpp
public void new(ListPage listPage)
```

### <a name="parameters---new"></a>パラメーター - new

listPage  
指定した ListPage オブジェクト。

