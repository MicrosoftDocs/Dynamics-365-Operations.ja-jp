---
title: PageInteraction クラス
description: このトピックでは、PageInteraction クラスについて説明します。
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
ms.openlocfilehash: f5f7dc807d9e292c6f27b45b22b2dfee2e72153a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502536"
---
# <a name="class-pageinteraction"></a>クラス PageInteraction

[!include [banner](../../includes/banner.md)]

```xpp
class PageInteraction extends Object
```

PageInteraction クラスは、リスト ページとやり取りするための機能を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                           | 説明                                                        |
|--------------------------------------------------|--------------------------------------------------------------------|
| public Page page()                               | ListPage インスタンスを取得します。                                        |
| public void tabChanged(container activeTabNames) |                                                                    |
| public void new(Page page)                       | リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。 |

## <a name="method-page"></a>メソッド page

ListPage インスタンスを取得します。

```xpp
public Page page()
```

### <a name="return-value---page"></a>戻り値 - page

この PageInteraction インスタンスの ListPage インスタンスを返します。

## <a name="method-tabchanged"></a>メソッド tabChanged

```xpp
public void tabChanged(container activeTabNames)
```

### <a name="parameters---tabchanged"></a>パラメーター - tabChanged

activeTabNames  

## <a name="method-new"></a>メソッド new

リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。

```xpp
public void new(Page page)
```

### <a name="parameters---new"></a>パラメーター - new

ページ  

