---
title: TreeNodeType クラス
description: このトピックでは、TreeNodeType クラスについて説明します。
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
ms.openlocfilehash: e61c9b5596df888f092e2f7b1cb8c2cb475f8c3b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502787"
---
# <a name="class-treenodetype"></a>クラス TreeNodeType

[!include [banner](../../includes/banner.md)]

```xpp
class TreeNodeType extends Object
```

TreeNodeType クラスは、TreeNode クラスのタイプに関する情報を取得します。

## <a name="remarks"></a>備考

このクラスを使用すると、TreeNode クラスのインスタンスを反映させることができます。 リフレクション情報は、TreeNode クラスのインスタンスに固有ではありません。 同じ NodeType を持つすべての TreeNode インスタンスは、同じ TreeNodeType を共有します。 TreeNode.TreeNodeType メソッドは、リフレクション情報を含む treeNodeType オブジェクトを返します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                     | 説明                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------|
| public int id()                            | タイプの ID を返します。                                                                                 |
| public boolean isConsumingMemory()         | このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。 |
| public boolean isGetNodeInLayerSupported() | このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。              |
| public boolean isLayerAware()              | このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。                    |
| public boolean isModelElement()            | このノード タイプのインスタンスがモデル要素かどうかを示します。                                      |
| public boolean isRootElement()             | このノード タイプのインスタンスがルート要素かどうかを示します。                                       |
| public boolean isUtilElement()             | このノード タイプのインスタンスがユーティリティ要素かどうかを示します。                                       |
| public boolean isVCSControllableElement()  |                                                                                                        |
| private void new()                         | TreeNodeType クラスの新しいインスタンスを初期化します。                                                  |

## <a name="method-id"></a>メソッド id

タイプの ID を返します。

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

TreeNodeType の ID。

## <a name="method-isconsumingmemory"></a>メソッド isConsumingMemory

このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。

```xpp
public boolean isConsumingMemory()
```

### <a name="return-value---isconsumingmemory"></a>戻り値 - isConsumingMemory

このタイプのツリー ノードがメモリを消費する場合は true。それ以外の場合は、false。

### <a name="remarks---isconsumingmemory"></a>備考 - isConsumingMemory

このタイプの TreeNode インスタンスで作業した後は、TreeNode.TreeNodeRelease メソッドを呼び出して、消費されたメモリを解放することが重要です。 これを行わないと、メモリ不足の例外が発生します。 構成階層における TreeNode クラスの全てのインスタンスがガベージ コレクションになる前に、TreeNode.TreeNodeRelease メソッドを呼び出さないでください。 たとえば、MyClass.myMethod の TreeNode がまだある場合、MyClass で TreeNode.TreeNodeRelease() メソッドを呼び出さないでください。

## <a name="method-isgetnodeinlayersupported"></a>メソッド isGetNodeInLayerSupported

このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。

```xpp
public boolean isGetNodeInLayerSupported()
```

### <a name="return-value---isgetnodeinlayersupported"></a>戻り値 - isGetNodeInLayerSupported

このタイプのツリー ノードが TreeNode.GetNodeInLayer メソッドをサポートする場合は true。それ以外の場合は、false。

## <a name="method-islayeraware"></a>メソッド isLayerAware

このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。

```xpp
public boolean isLayerAware()
```

### <a name="return-value---islayeraware"></a>戻り値 - isLayerAware

このタイプのツリー ノードがレイヤーで修飾された場合は true。それ以外の場合は、false。

### <a name="remarks---islayeraware"></a>備考 - isLayerAware

このタイプのツリー ノードは、AOTLayer メソッドと AOTLayers メソッドをサポートします。

## <a name="method-ismodelelement"></a>メソッド isModelElement

このノード タイプのインスタンスがモデル要素かどうかを示します。

```xpp
public boolean isModelElement()
```

### <a name="return-value---ismodelelement"></a>備考 - isModelElement

このタイプのツリー ノードがモデル要素である場合は true。それ以外の場合は、false。

### <a name="remarks---ismodelelement"></a>備考 - isModelElement

モデル要素は、モデル ストアに保持される (または保持できる) ツリー ノードです。 各モデル要素ツリー ノードについては、1 つのレコードはモデル ストアの ModelElements テーブル内に表示されます。 モデル要素は、AOT 内で含まれているモデルの名前で視覚的に修飾されます。

## <a name="method-isrootelement"></a>メソッド isRootElement

このノード タイプのインスタンスがルート要素かどうかを示します。

```xpp
public boolean isRootElement()
```

### <a name="return-value---isrootelement"></a>戻り値 - isRootElement

このタイプのツリー ノードがルート要素である場合は true。それ以外の場合は、false。

### <a name="remarks---isrootelement"></a>備考 - isRootElement

ルート要素は、ツリー ノードの構成階層のルートです。 ルート要素は、モデル要素の親を持つことはありません。 例には、MyTable、MyClass、MyForm が含まれます。

## <a name="method-isutilelement"></a>メソッド isUtilElement

このノード タイプのインスタンスがユーティリティ要素かどうかを示します。

```xpp
public boolean isUtilElement()
```

### <a name="return-value---isutilelement"></a>戻り値 - isUtilElement

このタイプのツリー ノードがユーティリティ要素である場合は true。それ以外の場合は、false。

### <a name="remarks---isutilelement"></a>備考 - isUtilElement

ユーティリティ要素は UtilElements と UtilIdElements ビューからアクセスできるツリー ノードです。 Util 要素はモデル要素のサブセットです。

## <a name="method-isvcscontrollableelement"></a>メソッド isVCSControllableElement

```xpp
public boolean isVCSControllableElement()
```

### <a name="return-value---isvcscontrollableelement"></a>戻り値 - isVCSControllableElement

## <a name="method-new"></a>メソッド new

TreeNodeType クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```


