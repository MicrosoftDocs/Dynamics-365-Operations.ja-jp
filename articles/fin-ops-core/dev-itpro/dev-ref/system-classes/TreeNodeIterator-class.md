---
title: TreeNodeIterator クラス
description: このトピックでは、TreeNodeIterator クラスについて説明します。
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
ms.openlocfilehash: 7ffdfd18a6b913052d06b78d741e44ef8970b278
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502786"
---
# <a name="class-treenodeiterator"></a>クラス TreeNodeIterator

[!include [banner](../../includes/banner.md)]

```xpp
class TreeNodeIterator extends Object
```

TreeNodeIterator クラスは、ツリー ノードの子ノード上を移動します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

次の例では、ルート ノードのすべての子ノードの名前を出力します。

```xpp
static void example()  
{ 
    treeNode myTreeNode; 
    xInfo xi = new xInfo(); 
    void printChildNames (treeNode t) 
    { 
        treeNode child; 
        treenodeIterator it; 
        it = t.AOTiterator(); 
        child = it.next(); 
        while (child) 
        { 
            print child.treeNodeName(); 
            child = it.next(); 
        } 
    } 
    myTreeNode = xi.rootNode(); 
    printChildNames(myTreeNode); 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                 | 説明                                                                                            |
|------------------------|--------------------------------------------------------------------------------------------------------|
| public TreeNode next() | 子ノードの一覧の次の要素を取得します。                                                 |
| public void reset()    | 次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。 |

## <a name="method-next"></a>メソッド next

子ノードの一覧の次の要素を取得します。

```xpp
public TreeNode next()
```

### <a name="return-value---next"></a>戻り値 - next

ツリー内の次の子ノード。

## <a name="method-reset"></a>メソッド reset

次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。

```xpp
public void reset()
```

