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
ms.search.scope: Operations
ms.custom: 31081
ms.assetid: 09358d27-6edc-420a-a7b6-83785b8ba0c6
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89f1082670341b2e4b4c18944d0138f3d1a125ae
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329884"
---
# <a name="hierarchyviewer-control"></a><span data-ttu-id="d3ed6-103">HierarchyViewer コントロール</span><span class="sxs-lookup"><span data-stu-id="d3ed6-103">HierarchyViewer control</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3ed6-104">この記事では、HierarchyViewer コントロールについて説明します。このコントロールを使用して、人、製品、または組織の階層関係を表現できます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-104">This article provides information about the HierarchyViewer control, which lets you represent hierarchical relationships for people, products, or organizations.</span></span>

<a name="overview"></a><span data-ttu-id="d3ed6-105">概要</span><span class="sxs-lookup"><span data-stu-id="d3ed6-105">Overview</span></span>
--------

<span data-ttu-id="d3ed6-106">HierarchyViewer コントロールを使用して、人、製品、または組織の階層関係を表現できます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-106">The HierarchyViewer control lets you represent hierarchical relationships for people, products, or organizations.</span></span> <span data-ttu-id="d3ed6-107">これは主に、従来の上から順の階層構造の関係を理解するのに役立つ視覚的な方法、およびフォーカスされたノードで表されるエンティティに移動する方法として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-107">It's used primarily as a graphical means to help you understand hierarchical relationships in a traditional top-down manner, and as way to navigate to the entity that is represented by the focused node.</span></span> <span data-ttu-id="d3ed6-108">HierarchyViewer コントロールを使用すると、わずかなスペースで深く入れ子になった複数レベルの内容を精査できます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-108">The HierarchyViewer control lets you walk through deeply nested, multilevel content in a compact space.</span></span> <span data-ttu-id="d3ed6-109">コントロールは、表示されているツリー構造の部分を制御するために、ノードを展開したり折りたたんだりします。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-109">The control expands and collapses nodes to control the parts of the tree structure that are shown.</span></span> <span data-ttu-id="d3ed6-110">非連結コントロールであるため、HierarchyViewer データは抽象化クラスによって管理され、主に単純なツリー リレーションシップでデータを視覚化する方法として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-110">Because it's an unbound control, the HierarchyViewer data is managed by an abstraction class and is used primarily as a way to visualize data in a simple tree relationship.</span></span> <span data-ttu-id="d3ed6-111">従来のツリーでの階層データについては、標準のツリー コントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-111">For hierarchy data in a traditional tree, there is a standard tree control.</span></span> 

<span data-ttu-id="d3ed6-112">[![HierarchyViewer コントロールのツリー構造を示すダイアグラム](./media/hierarchyviewer_page.png)](./media/hierarchyviewer_page.png)</span><span class="sxs-lookup"><span data-stu-id="d3ed6-112">[![Diagram showing HierarchyViewer control tree structure](./media/hierarchyviewer_page.png)](./media/hierarchyviewer_page.png)</span></span> 

<span data-ttu-id="d3ed6-113">HierarchyViewer コントロールは、常に単一ブランチで最大 3 つのレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-113">The HierarchyViewer control shows, at most, three levels on a single branch at any time.</span></span> <span data-ttu-id="d3ed6-114">階層リンク証跡は、現在のツリーの分岐下にある親のパスを示します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-114">A breadcrumb trail shows the path of parents down the current tree branch.</span></span> <span data-ttu-id="d3ed6-115">最上位レベルは現在の上位ノードを示し、常に 1 つのメンバーを持ちます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-115">The top level shows the current top node and will always have one member.</span></span> <span data-ttu-id="d3ed6-116">このメンバーは必ずしも root である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-116">This member isn't necessarily the root.</span></span> <span data-ttu-id="d3ed6-117">第 2 レベルである子ノードは、不定数のメンバー ノードを有することができます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-117">The second level, the child node, can have an indefinite number of member nodes.</span></span> <span data-ttu-id="d3ed6-118">既定では、これらのメンバー ノードの 3 つは各ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-118">By default, three of these member nodes are shown on each page.</span></span> <span data-ttu-id="d3ed6-119">表示されるメンバー ノードの数は、**子供の数** プロパティを使用して設定できます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-119">The number of member nodes that is shown can be set by using the **Number of children** property.</span></span> <span data-ttu-id="d3ed6-120">コントロールは、子レベルのメンバーの右と左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-120">The control will page right and left through the members of the child level.</span></span> <span data-ttu-id="d3ed6-121">最後のレベルである孫ノードは、不定数のメンバー ノードを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-121">The last level, the grandchild node, can have an indefinite number of member nodes.</span></span> <span data-ttu-id="d3ed6-122">可視メンバー ノードの数は、**孫の数** プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-122">The number of visible member nodes is controlled by the **Number of Grandchildren** property.</span></span> <span data-ttu-id="d3ed6-123">HierarchyViewer コントロールは、孫レベルのメンバーの上と下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-123">The HierarchyViewer control will page up and down through members of the grandchild level.</span></span> <span data-ttu-id="d3ed6-124">ノードの対話型の表示にはビジネス ロジックは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-124">The interactive display of nodes requires no business logic.</span></span>

## <a name="business-logic-interaction"></a><span data-ttu-id="d3ed6-125">ビジネス ロジック インタラクション</span><span class="sxs-lookup"><span data-stu-id="d3ed6-125">Business logic interaction</span></span>
<span data-ttu-id="d3ed6-126">HierarchyViewer コントロールは、データの視覚化とナビゲーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-126">The HierarchyViewer control offers data visualization and navigation.</span></span> <span data-ttu-id="d3ed6-127">HierarchyViewer コントロールは、読み取り専用のコントロールです。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-127">The HierarchyViewer control is a read-only control.</span></span> <span data-ttu-id="d3ed6-128">エンティティ (従業員、製品、または組織) を選択するために使用でき、HierarchyViewer コントロール外のフォームのその他の表示および入力フィールドで、対応するデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-128">It can be used to select an entity (employee, product, or organization), and corresponding data can then be managed though other display and input fields on the form, outside the HierarchyViewer control.</span></span> <span data-ttu-id="d3ed6-129">これは、各ノードの各ユーザーのフォーカスで発生する選択イベントによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-129">This is accomplished by a selection event that is raised on each user focus on each node.</span></span>

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

## <a name="authoring-a-hierarchyviewer-instance"></a><span data-ttu-id="d3ed6-130">HierarchyViewer インスタンスの作成</span><span class="sxs-lookup"><span data-stu-id="d3ed6-130">Authoring a HierarchyViewer instance</span></span>
<span data-ttu-id="d3ed6-131">HierarchyViewer インスタンスを作成するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-131">To create a HierarchyViewer instance:</span></span>

1.  <span data-ttu-id="d3ed6-132">フォーム デザイナーで、フォームに HierarchyViewer のインスタンスを追加します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-132">In the form designer, add an instance of HierarchyViewer to your form.</span></span>
2.  <span data-ttu-id="d3ed6-133">**プロパティ** ウィンドウで、表示されている子および孫の既定値を承認するか、新しい値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-133">In the **Properties** pane, accept the default number of visible children and grandchildren, or set new values.</span></span> 

![プロパティ ウィンドウのスクリーン ショット](./media/hierarchyviewer_properties-256x300.png)

<span data-ttu-id="d3ed6-135">HierarchyViewer コントロールは、主に静的な方法でノードを移動および調査する視覚的で対話的な方法です。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-135">The HierarchyViewer control is primarily a visually interactive way of navigating or interrogating nodes in a static manner.</span></span> <span data-ttu-id="d3ed6-136">HierarchyViewer コントロールは、データ ソースにバインドされていません。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-136">The HierarchyViewer control isn't bound to a data source.</span></span> <span data-ttu-id="d3ed6-137">代わりに、コントロールは基準 **HierarcyDesignerBase** を拡張する対応したコントローラー クラスによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-137">Instead, the control is managed by a corresponding controller class that extends the base **HierarcyDesignerBase**.</span></span> <span data-ttu-id="d3ed6-138">データを含むそのクラスの初期化し、コントロール インスタンスおよび HierarchyViewer ノードの表示フィールドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-138">You initialize that class with data, and bind to the control instance and the visible fields of the HierarchyViewer node.</span></span>

<span data-ttu-id="d3ed6-139">コントロールの一般的な使用方法は、階層のサーバー側「メモリ内」マップを初期化し、ロードオンデマンド セマンティクスを使用してユーザーが対話型で階層を探索するときに、コントロールを動的に更新します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-139">A typical use of the control is to initialize a server-side “in-memory” map of the hierarchy and then dynamically update the control as the user interactively explores the hierarchy by using load-on-demand semantics.</span></span>

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

<span data-ttu-id="d3ed6-140">コントロールの **applyBuild** メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-140">Override the **applyBuild** method of the control.</span></span> <span data-ttu-id="d3ed6-141">ここで、コントローラー クラスのインスタンスを渡します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-141">This is where you will pass the instance of your controller class.</span></span>

```xpp
    public void applyBuild()
{
    super();
    YourControllerClass controller = new YourControllerClass();
    this.initControl(controller);
}
```

<span data-ttu-id="d3ed6-142">ノード構造全体を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-142">You don’t have to populate the whole node structure.</span></span> <span data-ttu-id="d3ed6-143">代わりに、必要に応じてノードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-143">Instead, you can populate nodes on demand.</span></span>

```xpp
public void initHcmPositionFromCurrentNode(HcmPosition _hcmPosition)
protected void insertNewNodeAndLoadDescendants(HcmPositionNode _node, int _depth, HcmPositionNode _parentNode = null, Common _common = null)
protected void loadNodeDescendants(HcmPositionNode _node, int _depth, Common _common = null)
```

## <a name="changing-node-visuals"></a><span data-ttu-id="d3ed6-144">ノード ビジュアルの変更</span><span class="sxs-lookup"><span data-stu-id="d3ed6-144">Changing node visuals</span></span>
<span data-ttu-id="d3ed6-145">ノードのビジュアルを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-145">You can't change node visuals.</span></span> <span data-ttu-id="d3ed6-146">**ExtendedStyle** プロパティを使用して操作することができる既定のレイアウトを持つ一連のバインドされていないコントロールをコントロールが提供して、作成者が選択できる既定の代替セットを提供することが設計の目的です。</span><span class="sxs-lookup"><span data-stu-id="d3ed6-146">The intended design is for the control to offer a set of unbound controls that have a default layout that you can manipulate by using an **ExtendedStyle** property to offer a predefined set of alternatives that the author can select.</span></span>



