---
title: HierarchyViewer コントロール
description: この記事では、HierarchyViewer コントロールについて説明します。このコントロールを使用して、人、製品、または組織の階層関係を表現できます。
author: jasongre
ms.date: 08/25/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf61958cd3fa69107de126c85f0ede48fa9ed70b
ms.sourcegitcommit: f9201fc3f11532d82c926c4d7867375116026ca3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/05/2022
ms.locfileid: "9114343"
---
# <a name="hierarchyviewer-control"></a>HierarchyViewer コントロール

[!include [banner](../includes/banner.md)]

この記事では、HierarchyViewer コントロールについて説明します。このコントロールを使用して、人、製品、または組織の階層関係を表現できます。

## <a name="overview"></a>概要

HierarchyViewer コントロールを使用して、人、製品、または組織の階層関係を表現できます。 これは主に、従来の上から順の階層構造の関係を理解するのに役立つ視覚的な方法、およびフォーカスされたノードで表されるエンティティに移動する方法として使用されます。 HierarchyViewer コントロールを使用すると、わずかなスペースで深く入れ子になった複数レベルの内容を精査できます。 コントロールは、表示されているツリー構造の部分を制御するために、ノードを展開したり折りたたんだりします。 非連結コントロールであるため、HierarchyViewer データは抽象化クラスによって管理され、主に単純なツリー リレーションシップでデータを視覚化する方法として使用されます。 従来のツリーでの階層データについては、標準のツリー コントロールがあります。 

![HierarchyViewer コントロールのツリー構造を示す図。](./media/hierarchyViewer_refresh.png)

> [!NOTE]
> [財務と運用のバージョン 10.0.22 用のプラットフォーム更新プログラム](../get-started/whats-new-platform-updates-10-0-22.md) からこのビジュアルが使用可能です。

HierarchyViewer コントロールは、常に 4 つのレベルの情報を表示します。 現在のノードはツリーの現在のフォーカスであり、必ずしもルート ノードである必要はありません。 現在のノードは、現在のビューで最大の物理ノードで表され、左側に色付きバーが表示されます。 現在のノードの上には、ルート ノードから現在のノードまで小さい親ノードの軌跡があります。 現在のノードの下には子ノードのレベルがあり、このレベルでは無数のノードが存在する可能性があります。 既定では、各ページで一度に 3 つの子ノードが表示されますが、**子供の数** プロパティを調整することで変更できます。 **次へ** および **前に** リンク ボタンを使用すると、ユーザーは子レベルで他のノードにページングできます。 最後に、各子ノードに対して表示される孫ノードのレベルがあります。 各子には、無数の孫ノードがあります。また、各子ノードに対して一度に表示される孫の数は、**孫の数** プロパティによって制御されます。 ユーザーは、**次へ** および **前へ** 矢印ボタンを使用して、孫レベルでメンバを通じてページ を上または下に移動できます。 ノードの対話型の表示にはビジネス ロジックは必要ありません。

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

![プロパティ ウィンドウのスクリーン ショット。](./media/hierarchyviewer_properties-256x300.png)

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
ノードのビジュアルを変更することはできません。 このデザインは、一貫したビジュアルおよびユーザー操作を示します。 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

