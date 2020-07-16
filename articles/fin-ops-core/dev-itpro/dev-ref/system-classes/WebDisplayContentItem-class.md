---
title: WebDisplayContentItem クラス
description: このトピックでは、WebDisplayContentItem クラスについて説明します。
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
ms.openlocfilehash: 60459a8c2aa122c7e7ff237706dd4cf7b66c6555
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503003"
---
# <a name="class-webdisplaycontentitem"></a>クラス WebDisplayContentItem

[!include [banner](../../includes/banner.md)]

```xpp
class WebDisplayContentItem extends WebContentItem
```

WebDisplayContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                    | 説明                          |
|---------------------------|--------------------------------------|
| public void new(str name) | 新しい WebDisplayContentItem を作成します。 |

## <a name="method-new"></a>メソッド new

新しい WebDisplayContentItem を作成します。

```xpp
public void new(str name)
```

### <a name="parameters---new"></a>パラメーター - new

名前  

