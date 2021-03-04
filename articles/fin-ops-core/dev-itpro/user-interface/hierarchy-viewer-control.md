---
title: HierarchyViewer コントロール
description: この記事では、HierarchyViewer コントロールについて説明します。このコントロールを使用して、人、製品、または組織の階層関係を表現できます。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31081
ms.assetid: 09358d27-6edc-420a-a7b6-83785b8ba0c6
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfd0eed2be6ca941b9462d182d75a5764afae7af
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130769"
---
# <a name="hierarchyviewer-control"></a>HierarchyViewer コントロール

[!include [banner](../includes/banner.md)]

この記事では、HierarchyViewer コントロールについて説明します。このコントロールを使用して、人、製品、または組織の階層関係を表現できます。

<a name="overview"></a>概要
--------

HierarchyViewer コントロールを使用して、人、製品、または組織の階層関係を表現できます。 これは主に、従来の上から順の階層構造の関係を理解するのに役立つ視覚的な方法、およびフォーカスされたノードで表されるエンティティに移動する方法として使用されます。 HierarchyViewer コントロールを使用すると、わずかなスペースで深く入れ子になった複数レベルの内容を精査できます。 コントロールは、表示されているツリー構造の部分を制御するために、ノードを展開したり折りたたんだりします。 非連結コントロールであるため、HierarchyViewer データは抽象化クラスによって管理され、主に単純なツリー リレーションシップでデータを視覚化する方法として使用されます。 従来のツリーでの階層データについては、標準のツリー コントロールがあります。 

[![HierarchyViewer コントロールのツリー構造を示すダイアグラム](./media/hierarchyviewer_page.png)](./media/hierarchyviewer_page.png) 

HierarchyViewer コントロールは、常に単一ブランチで最大 3 つのレベルを示します。 階層リンク証跡は、現在のツリーの分岐下にある親のパスを示します。 最上位レベルは現在の上位ノードを示し、常に 1 つのメンバーを持ちます。 このメンバーは必ずしも root である必要はありません。 第 2 レベルである子ノードは、不定数のメンバー ノードを有することができます。 既定では、これらのメンバー ノードの 3 つは各ページに表示されます。 表示されるメンバー ノードの数は、**子供の数** プロパティを使用して設定できます。 コントロールは、子レベルのメンバーの右と左に表示されます。 最後のレベルである孫ノードは、不定数のメンバー ノードを持つことができます。 可視メンバー ノードの数は、**孫の数** プロパティによって制御されます。 HierarchyViewer コントロールは、孫レベルのメンバーの上と下に表示されます。 ノードの対話型の表示にはビジネス ロジックは必要ありません。

## <a name="business-logic-interaction"></a>ビジネス ロジック インタラクション
HierarchyViewer コントロールは、データの視覚化とナビゲーションを提供します。 HierarchyViewer コントロールは、読み取り専用のコントロールです。 エンティティ (従業員、製品、または組織) を選択するために使用でき、HierarchyViewer コントロール外のフォームのその他の表示および入力フィールドで、対応するデータを管理できます。 これは、各ノードの各ユーザーのフォーカスで発生する選択イベントによって実行されます。

```xpp
public void init(){
    …    
    // HierarchyViewer is the auto-declared name for the control.
    // handleNodeSelected is your event handler.
    HierarchyViewer.notfiyNodeSelected += eventhandler(element.handleNodeSelected);
}
public void handeNodeSelected(int _nodeId)
{
    // do something
}
```

## <a name="authoring-a-hierarchyviewer-instance"></a>HierarchyViewer インスタンスの作成
HierarchyViewer インスタンスを作成するには、次のようにします。

1.  フォーム デザイナーで、フォームに HierarchyViewer のインスタンスを追加します。
2.  **プロパティ** ウィンドウで、表示されている子および孫の既定値を承認するか、新しい値を設定します。 

![プロパティ ウィンドウのスクリーン ショット](./media/hierarchyviewer_properties-256x300.png)

HierarchyViewer コントロールは、主に静的な方法でノードを移動および調査する視覚的で対話的な方法です。 HierarchyViewer コントロールは、データ ソースにバインドされていません。 代わりに、コントロールは基準 **HierarcyDesignerBase** を拡張する対応したコントローラー クラスによって管理されます。 データを含むそのクラスの初期化し、コントロール インスタンスおよび HierarchyViewer ノードの表示フィールドにバインドします。

コントロールの一般的な使用方法は、階層のサーバー側「メモリ内」マップを初期化し、ロードオンデマンド セマンティクスを使用してユーザーが対話型で階層を探索するときに、コントロールを動的に更新します。

```xpp
public void init()
{
    HcmPositionNode node;
    nodeMap = new Map(Types::Int64, Types::Class);
    hierarchyMap = new Map(Types::Int64, Types::Int64);
    firstNodeId = 0;
    // Initialize the organization node
    node = HcmPositionNode::newParameters(this.getNextNodeId(), HcmPositionNodeType::Enterprise, -1, 0, "@SYS317690", "");
    rootNode = node;
    if (selectedNode == null)
    {
        selectedNode = rootNode;
    }
    this.insertNewNodeAndUpdateParent(node);
}
```

コントロールの **applyBuild** メソッドをオーバーライドします。 ここで、コントローラー クラスのインスタンスを渡します。

```xpp
    public void applyBuild()
{
    super();
    YourControllerClass controller = new YourControllerClass();
    this.initControl(controller);
}
```

ノード構造全体を設定する必要はありません。 代わりに、必要に応じてノードを設定します。

```xpp
public void initHcmPositionFromCurrentNode(HcmPosition _hcmPosition)
protected void insertNewNodeAndLoadDescendants(HcmPositionNode _node, int _depth, HcmPositionNode _parentNode = null, Common _common = null)
protected void loadNodeDescendants(HcmPositionNode _node, int _depth, Common _common = null)
```

## <a name="changing-node-visuals"></a>ノード ビジュアルの変更
ノードのビジュアルを変更することはできません。 **ExtendedStyle** プロパティを使用して操作することができる既定のレイアウトを持つ一連のバインドされていないコントロールをコントロールが提供して、作成者が選択できる既定の代替セットを提供することが設計の目的です。



