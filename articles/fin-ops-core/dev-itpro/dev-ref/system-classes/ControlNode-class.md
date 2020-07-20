---
title: ControlNode クラス
description: このトピックでは、ControlNode クラスについて説明します。
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
ms.openlocfilehash: 25abfbe55ffa5b6cb615966b08b815d2d843ab63
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502703"
---
# <a name="class-controlnode"></a>クラス ControlNode

[!include [banner](../../includes/banner.md)]

```xpp
class ControlNode extends TreeNode
```

ControlNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                         | 説明                                       |
|------------------------------------------------|---------------------------------------------------|
| public void new(str name, \[TreeNode parent\]) | TreeNode クラスの新しいインスタンスを初期化します。 |

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new(str name, [TreeNode parent])
```

### <a name="parameters---new"></a>パラメーター - new

名前  

<!-- -->

parent  

