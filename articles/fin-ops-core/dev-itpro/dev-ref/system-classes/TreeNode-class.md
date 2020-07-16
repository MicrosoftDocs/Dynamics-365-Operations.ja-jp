---
title: TreeNode クラス
description: このトピックでは、TreeNode クラスについて説明します。
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
ms.openlocfilehash: d4f7627241e158e2cb0235cc588fa89f733d53c8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502788"
---
# <a name="class-treenode"></a><span data-ttu-id="5359d-103">クラス TreeNode</span><span class="sxs-lookup"><span data-stu-id="5359d-103">Class TreeNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class TreeNode extends Object
```

<span data-ttu-id="5359d-104">TreeNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内のノードを取得し、表します。</span><span class="sxs-lookup"><span data-stu-id="5359d-104">The TreeNode class retrieves and represents any node in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="5359d-105">備考</span><span class="sxs-lookup"><span data-stu-id="5359d-105">Remarks</span></span>

<span data-ttu-id="5359d-106">このクラスとそれを拡張するクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5359d-106">This class, and the classes that extend it, enable you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="5359d-107">ユーザーがこの API またはこのクラスから派生した API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5359d-107">Make sure that the user has access to the development security key (SysDevelopment) before calling this API or APIs that are derived from this class.</span></span> <span data-ttu-id="5359d-108">TreeNode クラスを使用すると、AOT 内の任意のノードへのハンドルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5359d-108">The TreeNode class can be used to get a handle to any node in the AOT.</span></span> <span data-ttu-id="5359d-109">TreeNode クラスは、AOT内の任意の種類のノードへの参照となることができる一般的なクラスです。</span><span class="sxs-lookup"><span data-stu-id="5359d-109">The TreeNode class is a generic class in that it can be a reference to any type of node in the AOT.</span></span> <span data-ttu-id="5359d-110">このクラスには、AOT のショートカット メニューの一部の機能へのアクセスを提供することに加えて、ツリーで操作するために使用するメソッドも含まれます。</span><span class="sxs-lookup"><span data-stu-id="5359d-110">In addition to providing access to some of the functions on the shortcut menu of the AOT, this class also contains methods that are used to maneuver in the tree.</span></span> <span data-ttu-id="5359d-111">TreeNodeTraverser クラスは、AOT 内のナビゲーションでも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5359d-111">The TreeNodeTraverser class is also useful in navigating in the AOT.</span></span> <span data-ttu-id="5359d-112">TreeNode::findNode および TreeNode::rootNode メソッドは treeNode オブジェクトを返します。これらのオブジェクトから、その他のノードを操作できます。</span><span class="sxs-lookup"><span data-stu-id="5359d-112">The TreeNode::findNode and TreeNode::rootNode methods return a treeNode object from which you can maneuver to any other node.</span></span>

## <a name="examples"></a><span data-ttu-id="5359d-113">例</span><span class="sxs-lookup"><span data-stu-id="5359d-113">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5359d-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="5359d-114">Methods</span></span>

| <span data-ttu-id="5359d-115">方法</span><span class="sxs-lookup"><span data-stu-id="5359d-115">Method</span></span>                                                                                                                                              | <span data-ttu-id="5359d-116">説明</span><span class="sxs-lookup"><span data-stu-id="5359d-116">Description</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5359d-117">public TreeNode SysObsoleteAttribute(UtilElementName name)</span><span class="sxs-lookup"><span data-stu-id="5359d-117">public TreeNode SysObsoleteAttribute(UtilElementName name)</span></span>                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="5359d-118">public TreeNode SysObsoleteAttribute(str name, Types type)</span><span class="sxs-lookup"><span data-stu-id="5359d-118">public TreeNode SysObsoleteAttribute(str name, Types type)</span></span>                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="5359d-119">public TreeNode SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="5359d-119">public TreeNode SysObsoleteAttribute()</span></span>                                                                                                              |                                                                                                                                                                      |
| <span data-ttu-id="5359d-120">public TreeNode SysObsoleteAttribute(int nodetype)</span><span class="sxs-lookup"><span data-stu-id="5359d-120">public TreeNode SysObsoleteAttribute(int nodetype)</span></span>                                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="5359d-121">public boolean AOTAllowEdit()</span><span class="sxs-lookup"><span data-stu-id="5359d-121">public boolean AOTAllowEdit()</span></span>                                                                                                                       |                                                                                                                                                                      |
| <span data-ttu-id="5359d-122">public int AOTbitmapId()</span><span class="sxs-lookup"><span data-stu-id="5359d-122">public int AOTbitmapId()</span></span>                                                                                                                            | <span data-ttu-id="5359d-123">ツリー ノードのビットマップのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-123">Returns the resource ID of the bitmap of the tree node.</span></span>                                                                                                              |
| <span data-ttu-id="5359d-124">public int AOTchildNodeCount()</span><span class="sxs-lookup"><span data-stu-id="5359d-124">public int AOTchildNodeCount()</span></span>                                                                                                                      | <span data-ttu-id="5359d-125">指定されたツリー ノードにある子ノードの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="5359d-125">Counts the number of child nodes that a given tree node has.</span></span>                                                                                                         |
| <span data-ttu-id="5359d-126">public boolean SysObsoleteAttribute(\[int flag\], \[boolean forceNoXRef\], \[boolean fastMode\])</span><span class="sxs-lookup"><span data-stu-id="5359d-126">public boolean SysObsoleteAttribute(\[int flag\], \[boolean forceNoXRef\], \[boolean fastMode\])</span></span>                                                    |                                                                                                                                                                      |
| <span data-ttu-id="5359d-127">public boolean AOTDrop(TreeNode sourcenode, \[TreeNode after\])</span><span class="sxs-lookup"><span data-stu-id="5359d-127">public boolean AOTDrop(TreeNode sourcenode, \[TreeNode after\])</span></span>                                                                                     | <span data-ttu-id="5359d-128">指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。</span><span class="sxs-lookup"><span data-stu-id="5359d-128">Creates a copy of a specified tree node as a child to the TreeNode object.</span></span>                                                                                           |
| <span data-ttu-id="5359d-129">public TreeNode AOTDuplicate()</span><span class="sxs-lookup"><span data-stu-id="5359d-129">public TreeNode AOTDuplicate()</span></span>                                                                                                                      |                                                                                                                                                                      |
| <span data-ttu-id="5359d-130">public TreeNode AOTfindChild(str name, \[int nodeType\])</span><span class="sxs-lookup"><span data-stu-id="5359d-130">public TreeNode AOTfindChild(str name, \[int nodeType\])</span></span>                                                                                            | <span data-ttu-id="5359d-131">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="5359d-131">Finds the specified child node of this node.</span></span>                                                                                                                         |
| <span data-ttu-id="5359d-132">public TreeNode AOTfirstChild()</span><span class="sxs-lookup"><span data-stu-id="5359d-132">public TreeNode AOTfirstChild()</span></span>                                                                                                                     | <span data-ttu-id="5359d-133">ツリー ノードの最初の子ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-133">Retrieves the first child of the tree node.</span></span>                                                                                                                          |
| <span data-ttu-id="5359d-134">public TreeNode AOTfirstChildEx(\[boolean loadFullNode\])</span><span class="sxs-lookup"><span data-stu-id="5359d-134">public TreeNode AOTfirstChildEx(\[boolean loadFullNode\])</span></span>                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="5359d-135">public int AOTgetExecutableLineCount()</span><span class="sxs-lookup"><span data-stu-id="5359d-135">public int AOTgetExecutableLineCount()</span></span>                                                                                                              | <span data-ttu-id="5359d-136">このノードのコードの実行可能な行の数を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-136">Returns the number of executable lines of code for this node.</span></span>                                                                                                        |
| <span data-ttu-id="5359d-137">public Set AOTgetExecutableLines()</span><span class="sxs-lookup"><span data-stu-id="5359d-137">public Set AOTgetExecutableLines()</span></span>                                                                                                                  | <span data-ttu-id="5359d-138">このノードのコードの実行可能な行を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-138">Returns the executable lines of code for this node.</span></span>                                                                                                                  |
| <span data-ttu-id="5359d-139">public int AOTGetModel()</span><span class="sxs-lookup"><span data-stu-id="5359d-139">public int AOTGetModel()</span></span>                                                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="5359d-140">public str AOTgetProperties(\[boolean includeInvisible\], \[boolean includeReadOnly\], \[boolean includeNonExportable\])</span><span class="sxs-lookup"><span data-stu-id="5359d-140">public str AOTgetProperties(\[boolean includeInvisible\], \[boolean includeReadOnly\], \[boolean includeNonExportable\])</span></span>                            | <span data-ttu-id="5359d-141">ツリー ノードのプロパティを含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-141">Returns a string containing the properties of the tree node.</span></span>                                                                                                         |
| <span data-ttu-id="5359d-142">public Struct AOTgetPropertiesExt(\[str filter\])</span><span class="sxs-lookup"><span data-stu-id="5359d-142">public Struct AOTgetPropertiesExt(\[str filter\])</span></span>                                                                                                   |                                                                                                                                                                      |
| <span data-ttu-id="5359d-143">public AnyType AOTgetProperty(str name)</span><span class="sxs-lookup"><span data-stu-id="5359d-143">public AnyType AOTgetProperty(str name)</span></span>                                                                                                             |                                                                                                                                                                      |
| <span data-ttu-id="5359d-144">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="5359d-144">public str AOTgetSource()</span></span>                                                                                                                           | <span data-ttu-id="5359d-145">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-145">Returns the source code of this node.</span></span>                                                                                                                                |
| <span data-ttu-id="5359d-146">public boolean AOTIncludeInCompare()</span><span class="sxs-lookup"><span data-stu-id="5359d-146">public boolean AOTIncludeInCompare()</span></span>                                                                                                                |                                                                                                                                                                      |
| <span data-ttu-id="5359d-147">public boolean AOTIsDirty()</span><span class="sxs-lookup"><span data-stu-id="5359d-147">public boolean AOTIsDirty()</span></span>                                                                                                                         |                                                                                                                                                                      |
| <span data-ttu-id="5359d-148">public boolean AOTIsOld()</span><span class="sxs-lookup"><span data-stu-id="5359d-148">public boolean AOTIsOld()</span></span>                                                                                                                           | <span data-ttu-id="5359d-149">このノードが、古いモデル ストアにあるファイルのものかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-149">Indicates whether this node is from a file found in the old model store.</span></span>                                                                                             |
| <span data-ttu-id="5359d-150">public boolean AOTIsPersisted()</span><span class="sxs-lookup"><span data-stu-id="5359d-150">public boolean AOTIsPersisted()</span></span>                                                                                                                     | <span data-ttu-id="5359d-151">このノードがモデル ストアに保持されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-151">Indicates whether this node has been persisted in the model store.</span></span>                                                                                                   |
| <span data-ttu-id="5359d-152">public boolean AOTIsProxyNode()</span><span class="sxs-lookup"><span data-stu-id="5359d-152">public boolean AOTIsProxyNode()</span></span>                                                                                                                     |                                                                                                                                                                      |
| <span data-ttu-id="5359d-153">public TreeNodeIterator AOTiterator()</span><span class="sxs-lookup"><span data-stu-id="5359d-153">public TreeNodeIterator AOTiterator()</span></span>                                                                                                               | <span data-ttu-id="5359d-154">ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-154">Returns an object which can be used to iterate the child nodes of the tree node.</span></span>                                                                                     |
| <span data-ttu-id="5359d-155">public KernelHelpType AOTKernelHelpType()</span><span class="sxs-lookup"><span data-stu-id="5359d-155">public KernelHelpType AOTKernelHelpType()</span></span>                                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="5359d-156">public UtilEntryLevel AOTLayer()</span><span class="sxs-lookup"><span data-stu-id="5359d-156">public UtilEntryLevel AOTLayer()</span></span>                                                                                                                    | <span data-ttu-id="5359d-157">ツリー ノードのレイヤーを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-157">Returns the layer of the tree node.</span></span>                                                                                                                                  |
| <span data-ttu-id="5359d-158">public Set AOTLayers(\[boolean old\])</span><span class="sxs-lookup"><span data-stu-id="5359d-158">public Set AOTLayers(\[boolean old\])</span></span>                                                                                                               | <span data-ttu-id="5359d-159">そのツリー ノードで定義されているレイヤーのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-159">Returns a collection of the layers the tree node is defined in.</span></span>                                                                                                      |
| <span data-ttu-id="5359d-160">public str AOTname()</span><span class="sxs-lookup"><span data-stu-id="5359d-160">public str AOTname()</span></span>                                                                                                                                | <span data-ttu-id="5359d-161">ノードの name プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-161">Returns the value of the name property of the node.</span></span>                                                                                                                  |
| <span data-ttu-id="5359d-162">public int AOTnewWindow()</span><span class="sxs-lookup"><span data-stu-id="5359d-162">public int AOTnewWindow()</span></span>                                                                                                                           | <span data-ttu-id="5359d-163">ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。</span><span class="sxs-lookup"><span data-stu-id="5359d-163">Opens a new AOT tree window with the tree node as the root.</span></span>                                                                                                          |
| <span data-ttu-id="5359d-164">public TreeNode AOTnextSibling()</span><span class="sxs-lookup"><span data-stu-id="5359d-164">public TreeNode AOTnextSibling()</span></span>                                                                                                                    | <span data-ttu-id="5359d-165">ツリー ノードと同じレベルにある次のノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-165">Returns the next node on the same level as the tree node.</span></span>                                                                                                            |
| <span data-ttu-id="5359d-166">public boolean AOTObjectNode()</span><span class="sxs-lookup"><span data-stu-id="5359d-166">public boolean AOTObjectNode()</span></span>                                                                                                                      | <span data-ttu-id="5359d-167">ノードがアプリケーション オブジェクトであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-167">Indicates whether the node is an application object.</span></span>                                                                                                                 |
| <span data-ttu-id="5359d-168">public int AOToverlayBitmapId()</span><span class="sxs-lookup"><span data-stu-id="5359d-168">public int AOToverlayBitmapId()</span></span>                                                                                                                     | <span data-ttu-id="5359d-169">このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-169">Returns the resource ID of the overlay in the AOT associated with this node.</span></span>                                                                                         |
| <span data-ttu-id="5359d-170">public TreeNode AOTparent()</span><span class="sxs-lookup"><span data-stu-id="5359d-170">public TreeNode AOTparent()</span></span>                                                                                                                         | <span data-ttu-id="5359d-171">ツリー ノードの親ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-171">Returns the parent node of the tree node.</span></span>                                                                                                                            |
| <span data-ttu-id="5359d-172">public TreeNode AOTprevious()</span><span class="sxs-lookup"><span data-stu-id="5359d-172">public TreeNode AOTprevious()</span></span>                                                                                                                       | <span data-ttu-id="5359d-173">このツリー ノードの前の兄弟を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-173">Returns the previous sibling of this tree node.</span></span>                                                                                                                      |
| <span data-ttu-id="5359d-174">public boolean SysObsoleteAttribute(str name)</span><span class="sxs-lookup"><span data-stu-id="5359d-174">public boolean SysObsoleteAttribute(str name)</span></span>                                                                                                       |                                                                                                                                                                      |
| <span data-ttu-id="5359d-175">public str AOTtoolTip()</span><span class="sxs-lookup"><span data-stu-id="5359d-175">public str AOTtoolTip()</span></span>                                                                                                                             | <span data-ttu-id="5359d-176">そのツリー ノードに関連付けられているツールヒントを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-176">Returns the tool tip associated with the tree node.</span></span>                                                                                                                  |
| <span data-ttu-id="5359d-177">public str AOTToString()</span><span class="sxs-lookup"><span data-stu-id="5359d-177">public str AOTToString()</span></span>                                                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="5359d-178">public str AOTtypeStr()</span><span class="sxs-lookup"><span data-stu-id="5359d-178">public str AOTtypeStr()</span></span>                                                                                                                             | <span data-ttu-id="5359d-179">XPO ファイルで使用される要素タイプの文字列の内部コードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-179">Returns the internal string code for the element type used in XPO files.</span></span>                                                                                             |
| <span data-ttu-id="5359d-180">public UtilFileType AOTUtilFileType()</span><span class="sxs-lookup"><span data-stu-id="5359d-180">public UtilFileType AOTUtilFileType()</span></span>                                                                                                               | <span data-ttu-id="5359d-181">TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-181">Retrieves the value of the UtilFileType enumeration type for the TreeNode object.</span></span> <span data-ttu-id="5359d-182">UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-182">The UtilFileType indicates which kind of file the application object is stored in.</span></span> |
| <span data-ttu-id="5359d-183">public int applObjectId()</span><span class="sxs-lookup"><span data-stu-id="5359d-183">public int applObjectId()</span></span>                                                                                                                           | <span data-ttu-id="5359d-184">該当する場合は、アプリケーション オブジェクト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-184">Returns the application object ID, if applicable.</span></span>                                                                                                                    |
| <span data-ttu-id="5359d-185">public int applObjectLayerMask()</span><span class="sxs-lookup"><span data-stu-id="5359d-185">public int applObjectLayerMask()</span></span>                                                                                                                    | <span data-ttu-id="5359d-186">この要素を含むレイヤーを指定するビットを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-186">Returns a bitmask that specifies which layers contain this element.</span></span>                                                                                                  |
| <span data-ttu-id="5359d-187">public int applObjectOldLayerMask()</span><span class="sxs-lookup"><span data-stu-id="5359d-187">public int applObjectOldLayerMask()</span></span>                                                                                                                 | <span data-ttu-id="5359d-188">ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-188">Returns a bitmask that specifies which layers contain this element in the baseline model store.</span></span>                                                                      |
| <span data-ttu-id="5359d-189">public TreeNode getNodeInLayer(UtilEntryLevel layer, \[boolean old\])</span><span class="sxs-lookup"><span data-stu-id="5359d-189">public TreeNode getNodeInLayer(UtilEntryLevel layer, \[boolean old\])</span></span>                                                                               | <span data-ttu-id="5359d-190">指定したレイヤーからツリー ノードのバージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-190">Retrieves a version of the tree node from a specified layer.</span></span>                                                                                                         |
| <span data-ttu-id="5359d-191">public Int64 hashKey()</span><span class="sxs-lookup"><span data-stu-id="5359d-191">public Int64 hashKey()</span></span>                                                                                                                              |                                                                                                                                                                      |
| <span data-ttu-id="5359d-192">public TreeNode makeCopy()</span><span class="sxs-lookup"><span data-stu-id="5359d-192">public TreeNode makeCopy()</span></span>                                                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="5359d-193">public str newObjectName(\[str oldName\])</span><span class="sxs-lookup"><span data-stu-id="5359d-193">public str newObjectName(\[str oldName\])</span></span>                                                                                                           | <span data-ttu-id="5359d-194">新しい要素の名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-194">Returns a string that contains the name of the new element.</span></span>                                                                                                          |
| <span data-ttu-id="5359d-195">public str toString()</span><span class="sxs-lookup"><span data-stu-id="5359d-195">public str toString()</span></span>                                                                                                                               | <span data-ttu-id="5359d-196">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-196">Returns a string that represents the current object.</span></span>                                                                                                                 |
| <span data-ttu-id="5359d-197">public str treeNodeName()</span><span class="sxs-lookup"><span data-stu-id="5359d-197">public str treeNodeName()</span></span>                                                                                                                           | <span data-ttu-id="5359d-198">ツリー ノードの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-198">Returns the name of the tree node.</span></span>                                                                                                                                   |
| <span data-ttu-id="5359d-199">public str treeNodePath()</span><span class="sxs-lookup"><span data-stu-id="5359d-199">public str treeNodePath()</span></span>                                                                                                                           | <span data-ttu-id="5359d-200">アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-200">Returns the unique path to the tree node within the Application Object Tree (AOT).</span></span>                                                                                   |
| <span data-ttu-id="5359d-201">public TreeNodeType treeNodeType()</span><span class="sxs-lookup"><span data-stu-id="5359d-201">public TreeNodeType treeNodeType()</span></span>                                                                                                                  | <span data-ttu-id="5359d-202">ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-202">Retrieves an instance of a TreeNodeType class that provides reflection information for the tree node.</span></span>                                                                |
| <span data-ttu-id="5359d-203">public int updateNodePermissions(boolean throwExceptions)</span><span class="sxs-lookup"><span data-stu-id="5359d-203">public int updateNodePermissions(boolean throwExceptions)</span></span>                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="5359d-204">public UtilElements utilElement()</span><span class="sxs-lookup"><span data-stu-id="5359d-204">public UtilElements utilElement()</span></span>                                                                                                                   | <span data-ttu-id="5359d-205">ノードに関連する UtilElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-205">Returns a UtilElements record that is related to the node.</span></span>                                                                                                           |
| <span data-ttu-id="5359d-206">public UtilIdElements utilIdElement()</span><span class="sxs-lookup"><span data-stu-id="5359d-206">public UtilIdElements utilIdElement()</span></span>                                                                                                               | <span data-ttu-id="5359d-207">ノードに関連する UtilIdElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-207">Returns a UtilIdElements record that is related to the node.</span></span>                                                                                                         |
| <span data-ttu-id="5359d-208">public boolean validateNameCharacters(str name)</span><span class="sxs-lookup"><span data-stu-id="5359d-208">public boolean validateNameCharacters(str name)</span></span>                                                                                                     |                                                                                                                                                                      |
| <span data-ttu-id="5359d-209">::public static TreeNode findNode(str path)</span><span class="sxs-lookup"><span data-stu-id="5359d-209">::public static TreeNode findNode(str path)</span></span>                                                                                                         | <span data-ttu-id="5359d-210">アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-210">Returns a specified node in the Application Object Tree (AOT).</span></span>                                                                                                       |
| <span data-ttu-id="5359d-211">::public static str generateObjectName(str template)</span><span class="sxs-lookup"><span data-stu-id="5359d-211">::public static str generateObjectName(str template)</span></span>                                                                                                |                                                                                                                                                                      |
| <span data-ttu-id="5359d-212">::public static int getMaximumNodeNameLength(int modelElementTypeId)</span><span class="sxs-lookup"><span data-stu-id="5359d-212">::public static int getMaximumNodeNameLength(int modelElementTypeId)</span></span>                                                                                |                                                                                                                                                                      |
| <span data-ttu-id="5359d-213">::public static boolean isNodeReferenceValid(TreeNode treeNode)</span><span class="sxs-lookup"><span data-stu-id="5359d-213">::public static boolean isNodeReferenceValid(TreeNode treeNode)</span></span>                                                                                     |                                                                                                                                                                      |
| <span data-ttu-id="5359d-214">::public static boolean isValidObjectName(str name)</span><span class="sxs-lookup"><span data-stu-id="5359d-214">::public static boolean isValidObjectName(str name)</span></span>                                                                                                 | <span data-ttu-id="5359d-215">引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5359d-215">Determines whether the string passed as an argument can be used as a name for a node in the Application Object Tree (AOT).</span></span>                                           |
| <span data-ttu-id="5359d-216">::public static TreeNode rootNode()</span><span class="sxs-lookup"><span data-stu-id="5359d-216">::public static TreeNode rootNode()</span></span>                                                                                                                 | <span data-ttu-id="5359d-217">AOT のルート ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-217">Returns the root node of the AOT.</span></span>                                                                                                                                    |
| <span data-ttu-id="5359d-218">public void SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="5359d-218">public void SysObsoleteAttribute()</span></span>                                                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="5359d-219">public void treeNodeRelease()</span><span class="sxs-lookup"><span data-stu-id="5359d-219">public void treeNodeRelease()</span></span>                                                                                                                       | <span data-ttu-id="5359d-220">ツリー ノードが明示的に解放されます。</span><span class="sxs-lookup"><span data-stu-id="5359d-220">Releases the tree node explicitly.</span></span>                                                                                                                                   |
| <span data-ttu-id="5359d-221">public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, \[XRefReference xrefRef\], \[ClassId parentTypeId\])</span><span class="sxs-lookup"><span data-stu-id="5359d-221">public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, \[XRefReference xrefRef\], \[ClassId parentTypeId\])</span></span> |                                                                                                                                                                      |
| <span data-ttu-id="5359d-222">public void AOTrun()</span><span class="sxs-lookup"><span data-stu-id="5359d-222">public void AOTrun()</span></span>                                                                                                                                | <span data-ttu-id="5359d-223">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="5359d-223">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>                                                                                             |
| <span data-ttu-id="5359d-224">public void SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="5359d-224">public void SysObsoleteAttribute()</span></span>                                                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="5359d-225">public void AOTrefresh()</span><span class="sxs-lookup"><span data-stu-id="5359d-225">public void AOTrefresh()</span></span>                                                                                                                            | <span data-ttu-id="5359d-226">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="5359d-226">Refreshes the node with the latest changes to the .aod file.</span></span>                                                                                                         |
| <span data-ttu-id="5359d-227">public void SysObsoleteAttribute(Struct struct1)</span><span class="sxs-lookup"><span data-stu-id="5359d-227">public void SysObsoleteAttribute(Struct struct1)</span></span>                                                                                                    |                                                                                                                                                                      |
| <span data-ttu-id="5359d-228">public void SysObsoleteAttribute(str properties)</span><span class="sxs-lookup"><span data-stu-id="5359d-228">public void SysObsoleteAttribute(str properties)</span></span>                                                                                                    |                                                                                                                                                                      |
| <span data-ttu-id="5359d-229">public void AOTconfigure()</span><span class="sxs-lookup"><span data-stu-id="5359d-229">public void AOTconfigure()</span></span>                                                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="5359d-230">public void AOTload()</span><span class="sxs-lookup"><span data-stu-id="5359d-230">public void AOTload()</span></span>                                                                                                                               | <span data-ttu-id="5359d-231">オブジェクトが読み込み済みであるか確認します。</span><span class="sxs-lookup"><span data-stu-id="5359d-231">Ensures that the object is loaded.</span></span>                                                                                                                                   |
| <span data-ttu-id="5359d-232">public void treeNodeExport(str filename, \[int flag\])</span><span class="sxs-lookup"><span data-stu-id="5359d-232">public void treeNodeExport(str filename, \[int flag\])</span></span>                                                                                              | <span data-ttu-id="5359d-233">アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="5359d-233">Exports this node and its subtree from the Application Object Tree (AOT).</span></span>                                                                                            |
| <span data-ttu-id="5359d-234">public void SysObsoleteAttribute(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="5359d-234">public void SysObsoleteAttribute(str source, \[boolean isStatic\])</span></span>                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="5359d-235">public void AOTendXref()</span><span class="sxs-lookup"><span data-stu-id="5359d-235">public void AOTendXref()</span></span>                                                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="5359d-236">public void AOTmessageLine(str text, int linenumber)</span><span class="sxs-lookup"><span data-stu-id="5359d-236">public void AOTmessageLine(str text, int linenumber)</span></span>                                                                                                | <span data-ttu-id="5359d-237">アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。</span><span class="sxs-lookup"><span data-stu-id="5359d-237">Writes text to the Application Object Tree (AOT) Message window.</span></span>                                                                                                     |
| <span data-ttu-id="5359d-238">public void SysObsoleteAttribute(str name, AnyType value)</span><span class="sxs-lookup"><span data-stu-id="5359d-238">public void SysObsoleteAttribute(str name, AnyType value)</span></span>                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="5359d-239">public void AOTrestore(\[boolean forceReload\])</span><span class="sxs-lookup"><span data-stu-id="5359d-239">public void AOTrestore(\[boolean forceReload\])</span></span>                                                                                                     | <span data-ttu-id="5359d-240">該当する場合は、ディスクからこのノードを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="5359d-240">Reloads this node from the disk, if applicable.</span></span>                                                                                                                      |
| <span data-ttu-id="5359d-241">public void AOTregenerate()</span><span class="sxs-lookup"><span data-stu-id="5359d-241">public void AOTregenerate()</span></span>                                                                                                                         |                                                                                                                                                                      |
| <span data-ttu-id="5359d-242">public void AOTmakeXref(\[int flag\], \[boolean xRefAll\])</span><span class="sxs-lookup"><span data-stu-id="5359d-242">public void AOTmakeXref(\[int flag\], \[boolean xRefAll\])</span></span>                                                                                          | <span data-ttu-id="5359d-243">このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。</span><span class="sxs-lookup"><span data-stu-id="5359d-243">Compiles this node and its subtree in the AOT, updating the cross-reference system.</span></span>                                                                                  |
| <span data-ttu-id="5359d-244">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="5359d-244">public void AOTedit(\[int Line\], \[int Column\])</span></span>                                                                                                   | <span data-ttu-id="5359d-245">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="5359d-245">Opens the appropriate editor for this node.</span></span>                                                                                                                          |
| <span data-ttu-id="5359d-246">public void AOTshowProperties()</span><span class="sxs-lookup"><span data-stu-id="5359d-246">public void AOTshowProperties()</span></span>                                                                                                                     | <span data-ttu-id="5359d-247">プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-247">Opens the property sheet (if not already open) and shows the properties for this node.</span></span>                                                                               |
| <span data-ttu-id="5359d-248">public void AOTinsert(TreeNode parent, \[TreeNode after\], \[boolean doNotDuplicate\])</span><span class="sxs-lookup"><span data-stu-id="5359d-248">public void AOTinsert(TreeNode parent, \[TreeNode after\], \[boolean doNotDuplicate\])</span></span>                                                              | <span data-ttu-id="5359d-249">このノードのサブノード間にノードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="5359d-249">Inserts a node among the subnodes of this node.</span></span>                                                                                                                      |
| <span data-ttu-id="5359d-250">public void new()</span><span class="sxs-lookup"><span data-stu-id="5359d-250">public void new()</span></span>                                                                                                                                   | <span data-ttu-id="5359d-251">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5359d-251">Initializes a new instance of the TreeNode class.</span></span>                                                                                                                    |
| <span data-ttu-id="5359d-252">public void AOTMove(TreeNode parent, \[TreeNode after\])</span><span class="sxs-lookup"><span data-stu-id="5359d-252">public void AOTMove(TreeNode parent, \[TreeNode after\])</span></span>                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="5359d-253">public void SysObsoleteAttribute(int modelId)</span><span class="sxs-lookup"><span data-stu-id="5359d-253">public void SysObsoleteAttribute(int modelId)</span></span>                                                                                                       |                                                                                                                                                                      |

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-254">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-254">Method SysObsoleteAttribute</span></span>

```xpp
public TreeNode SysObsoleteAttribute(UtilElementName name)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-255">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-255">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-256">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-256">name</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5359d-257">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-257">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-258">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-258">Method SysObsoleteAttribute</span></span>

```xpp
public TreeNode SysObsoleteAttribute(str name, Types type)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-259">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-259">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-260">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-260">name</span></span>  

<!-- -->

<span data-ttu-id="5359d-261">タイプ</span><span class="sxs-lookup"><span data-stu-id="5359d-261">type</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5359d-262">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-262">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-263">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-263">Method SysObsoleteAttribute</span></span>

```xpp
public TreeNode SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5359d-264">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-264">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-265">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-265">Method SysObsoleteAttribute</span></span>

```xpp
public TreeNode SysObsoleteAttribute(int nodetype)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-266">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-266">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-267">nodetype</span><span class="sxs-lookup"><span data-stu-id="5359d-267">nodetype</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5359d-268">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-268">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-aotallowedit"></a><span data-ttu-id="5359d-269">メソッド AOTAllowEdit</span><span class="sxs-lookup"><span data-stu-id="5359d-269">Method AOTAllowEdit</span></span>

```xpp
public boolean AOTAllowEdit()
```

### <a name="return-value---aotallowedit"></a><span data-ttu-id="5359d-270">戻り値 - AOTAllowEdit</span><span class="sxs-lookup"><span data-stu-id="5359d-270">Return Value - AOTAllowEdit</span></span>

## <a name="method-aotbitmapid"></a><span data-ttu-id="5359d-271">メソッド AOTbitmapId</span><span class="sxs-lookup"><span data-stu-id="5359d-271">Method AOTbitmapId</span></span>

<span data-ttu-id="5359d-272">ツリー ノードのビットマップのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-272">Returns the resource ID of the bitmap of the tree node.</span></span>

```xpp
public int AOTbitmapId()
```

### <a name="return-value---aotbitmapid"></a><span data-ttu-id="5359d-273">戻り値 - AOTbitmapId</span><span class="sxs-lookup"><span data-stu-id="5359d-273">Return Value - AOTbitmapId</span></span>

<span data-ttu-id="5359d-274">ツリー ノードのビットマップのリソース ID。</span><span class="sxs-lookup"><span data-stu-id="5359d-274">The resource ID of the bitmap of the tree node.</span></span>

### <a name="examples---aotbitmapid"></a><span data-ttu-id="5359d-275">例 - AOTbitmapId</span><span class="sxs-lookup"><span data-stu-id="5359d-275">Examples - AOTbitmapId</span></span>

<span data-ttu-id="5359d-276">次の例では、アプリケーション オブジェクト ツリー (AOT) 内の拡張データ型ノードのリソース ID を出力します。</span><span class="sxs-lookup"><span data-stu-id="5359d-276">The following example prints the resource ID of the Extended Data Types node in the Application Object Tree (AOT).</span></span>

```xpp
AOT 
static void myJobAOTbitmapId(Args _args) 
{ 
    treeNode treeNode = TreeNode::findNode(#ExtendedDataTypesPath); 
    print treeNode.AOTbitmapId(); 
    pause; 
}
```

<span data-ttu-id="5359d-277">このジョブは整数 895 を出力します。</span><span class="sxs-lookup"><span data-stu-id="5359d-277">This job will print the integer 895.</span></span> <span data-ttu-id="5359d-278">チュートリアルのリソース フォームを実行すると、ビットマップを参照し、それが AOT 内での拡張データ型に使用されるものと同じであることが分かります。</span><span class="sxs-lookup"><span data-stu-id="5359d-278">If you run the Tutorial resources form, you can see the bitmap and verify that it is the same as the one that is used for Extended Data Types in the AOT.</span></span>

## <a name="method-aotchildnodecount"></a><span data-ttu-id="5359d-279">メソッド AOTchildNodeCount</span><span class="sxs-lookup"><span data-stu-id="5359d-279">Method AOTchildNodeCount</span></span>

<span data-ttu-id="5359d-280">指定されたツリー ノードにある子ノードの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="5359d-280">Counts the number of child nodes that a given tree node has.</span></span>

```xpp
public int AOTchildNodeCount()
```

### <a name="return-value---aotchildnodecount"></a><span data-ttu-id="5359d-281">戻り値 - AOTchildNodeCount</span><span class="sxs-lookup"><span data-stu-id="5359d-281">Return Value - AOTchildNodeCount</span></span>

<span data-ttu-id="5359d-282">ツリー ノードの子ノードの数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="5359d-282">An integer that indicates the number of child nodes for the tree node.</span></span>

### <a name="examples---aotchildnodecount"></a><span data-ttu-id="5359d-283">例 - AOTchildNodeCount</span><span class="sxs-lookup"><span data-stu-id="5359d-283">Examples - AOTchildNodeCount</span></span>

<span data-ttu-id="5359d-284">次の例では、アプリケーション オブジェクト ツリー (AOT) のメニュー アイテム ノードの下に表示される子ノードの数を出力します。</span><span class="sxs-lookup"><span data-stu-id="5359d-284">The following example prints the number of child nodes that appear under the Menu Items node in the Application Object Tree (AOT).</span></span>

```xpp
AOT 
static void myJobAOTchildNodeCount(Args _args) 
{ 
    treeNode treeNode = TreeNode::findNode(#MenuItemsPath); 
    print "Number of nodes below Menu Items: ", treeNode.AOTchildNodeCount(); 
    pause; 
}
```

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-285">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-285">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute([int flag], [boolean forceNoXRef], [boolean fastMode])
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-286">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-286">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-287">flag</span><span class="sxs-lookup"><span data-stu-id="5359d-287">flag</span></span>  

<!-- -->

<span data-ttu-id="5359d-288">forceNoXRef</span><span class="sxs-lookup"><span data-stu-id="5359d-288">forceNoXRef</span></span>  

<!-- -->

<span data-ttu-id="5359d-289">fastMode</span><span class="sxs-lookup"><span data-stu-id="5359d-289">fastMode</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5359d-290">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-290">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-aotdrop"></a><span data-ttu-id="5359d-291">メソッド AOTDrop</span><span class="sxs-lookup"><span data-stu-id="5359d-291">Method AOTDrop</span></span>

<span data-ttu-id="5359d-292">指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。</span><span class="sxs-lookup"><span data-stu-id="5359d-292">Creates a copy of a specified tree node as a child to the TreeNode object.</span></span>

```xpp
public boolean AOTDrop(TreeNode sourcenode, [TreeNode after])
```

### <a name="parameters---aotdrop"></a><span data-ttu-id="5359d-293">パラメーター - AOTDrop</span><span class="sxs-lookup"><span data-stu-id="5359d-293">Parameters - AOTDrop</span></span>

<span data-ttu-id="5359d-294">sourcenode</span><span class="sxs-lookup"><span data-stu-id="5359d-294">sourcenode</span></span>  
<span data-ttu-id="5359d-295">ソースが後で挿入されるツリー ノードの子ノード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5359d-295">The child node of the tree node that the source should be inserted after; optional.</span></span>

<!-- -->

<span data-ttu-id="5359d-296">以後</span><span class="sxs-lookup"><span data-stu-id="5359d-296">after</span></span>  
<span data-ttu-id="5359d-297">ソースが後で挿入されるツリー ノードの子ノード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5359d-297">The child node of the tree node that the source should be inserted after; optional.</span></span>

### <a name="return-value---aotdrop"></a><span data-ttu-id="5359d-298">戻り値 - AOTDrop</span><span class="sxs-lookup"><span data-stu-id="5359d-298">Return Value - AOTDrop</span></span>

<span data-ttu-id="5359d-299">ドロップ操作が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5359d-299">true if the drop operation was successful; otherwise, false.</span></span>

### <a name="examples---aotdrop"></a><span data-ttu-id="5359d-300">例 - AOTDrop</span><span class="sxs-lookup"><span data-stu-id="5359d-300">Examples - AOTDrop</span></span>

<span data-ttu-id="5359d-301">次の例では、tutorial\_Form\_Controls フォームの underTab:Tab の最後のノードとして、tabPage:CopyOfContainers ツリー ノードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5359d-301">The following example creates the tabPage:CopyOfContainers tree node as the last node underTab:Tab in the tutorial\_Form\_Controls form.</span></span>

```xpp
AOT 
static void myJobAOTDrop(Args _args) 
{ 
    treeNode treeNodeTab; 
    treeNode treeNodeTabPageContainers; 
    treeNodeTab = TreeNode::findNode(#FormsPath + '\\' +  
        formStr(tutorial_form_controls)+ '\\Designs\\Design\\[Tab:Tab]'); 
    treeNodeTabPageContainers = TreeNode::findNode(#FormsPath + '\\' +  
        formStr(tutorial_form_controls)+  
        '\\Designs\\Design\\[Tab:Tab]\\[TabPage:Containers]'); 
    if (treeNodeTab && treeNodeTabPageContainers) 
    { 
        // Drop the TabPage:Containers node on the Tab:Tab node. 
        print treeNodeTab.AOTDrop(treeNodeTabPageContainers); 
    } 
    else 
    { 
        print "Could not find treeNodeTab or treeNodeTabPageContainers"; 
    } 
    pause; 
}
```

## <a name="method-aotduplicate"></a><span data-ttu-id="5359d-302">メソッド AOTDuplicate</span><span class="sxs-lookup"><span data-stu-id="5359d-302">Method AOTDuplicate</span></span>

```xpp
public TreeNode AOTDuplicate()
```

### <a name="return-value---aotduplicate"></a><span data-ttu-id="5359d-303">戻り値 - AOTDuplicate</span><span class="sxs-lookup"><span data-stu-id="5359d-303">Return Value - AOTDuplicate</span></span>

## <a name="method-aotfindchild"></a><span data-ttu-id="5359d-304">メソッド AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="5359d-304">Method AOTfindChild</span></span>

<span data-ttu-id="5359d-305">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="5359d-305">Finds the specified child node of this node.</span></span>

```xpp
public TreeNode AOTfindChild(str name, [int nodeType])
```

### <a name="parameters---aotfindchild"></a><span data-ttu-id="5359d-306">パラメーター - AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="5359d-306">Parameters - AOTfindChild</span></span>

<span data-ttu-id="5359d-307">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-307">name</span></span>  

<!-- -->

<span data-ttu-id="5359d-308">nodeType</span><span class="sxs-lookup"><span data-stu-id="5359d-308">nodeType</span></span>  

### <a name="return-value---aotfindchild"></a><span data-ttu-id="5359d-309">戻り値 - AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="5359d-309">Return Value - AOTfindChild</span></span>

<span data-ttu-id="5359d-310">指定した TreeNode。</span><span class="sxs-lookup"><span data-stu-id="5359d-310">The specified TreeNode.</span></span>

## <a name="method-aotfirstchild"></a><span data-ttu-id="5359d-311">メソッド AOTfirstChild</span><span class="sxs-lookup"><span data-stu-id="5359d-311">Method AOTfirstChild</span></span>

<span data-ttu-id="5359d-312">ツリー ノードの最初の子ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-312">Retrieves the first child of the tree node.</span></span>

```xpp
public TreeNode AOTfirstChild()
```

### <a name="return-value---aotfirstchild"></a><span data-ttu-id="5359d-313">戻り値 - AOTfirstChild</span><span class="sxs-lookup"><span data-stu-id="5359d-313">Return Value - AOTfirstChild</span></span>

<span data-ttu-id="5359d-314">ツリー ノードの最初の子ノード。</span><span class="sxs-lookup"><span data-stu-id="5359d-314">The first child node of the tree node.</span></span>

## <a name="method-aotfirstchildex"></a><span data-ttu-id="5359d-315">メソッド AOTfirstChildEx</span><span class="sxs-lookup"><span data-stu-id="5359d-315">Method AOTfirstChildEx</span></span>

```xpp
public TreeNode AOTfirstChildEx([boolean loadFullNode])
```

### <a name="parameters---aotfirstchildex"></a><span data-ttu-id="5359d-316">パラメーター - AOTfirstChildEx</span><span class="sxs-lookup"><span data-stu-id="5359d-316">Parameters - AOTfirstChildEx</span></span>

<span data-ttu-id="5359d-317">loadFullNode</span><span class="sxs-lookup"><span data-stu-id="5359d-317">loadFullNode</span></span>  

### <a name="return-value---aotfirstchildex"></a><span data-ttu-id="5359d-318">戻り値 - AOTfirstChildEx</span><span class="sxs-lookup"><span data-stu-id="5359d-318">Return Value - AOTfirstChildEx</span></span>

## <a name="method-aotgetexecutablelinecount"></a><span data-ttu-id="5359d-319">メソッド AOTgetExecutableLineCount</span><span class="sxs-lookup"><span data-stu-id="5359d-319">Method AOTgetExecutableLineCount</span></span>

<span data-ttu-id="5359d-320">このノードのコードの実行可能な行の数を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-320">Returns the number of executable lines of code for this node.</span></span>

```xpp
public int AOTgetExecutableLineCount()
```

### <a name="return-value---aotgetexecutablelinecount"></a><span data-ttu-id="5359d-321">戻り値 - AOTgetExecutableLineCount</span><span class="sxs-lookup"><span data-stu-id="5359d-321">Return Value - AOTgetExecutableLineCount</span></span>

<span data-ttu-id="5359d-322">存在する場合のこのノードの実行可能コード行数。存在しない場合は、ゼロ。</span><span class="sxs-lookup"><span data-stu-id="5359d-322">The number of executable lines of code for this node if any; otherwise, zero.</span></span>

### <a name="remarks---aotgetexecutablelinecount"></a><span data-ttu-id="5359d-323">備考 - AOTgetExecutableLineCount</span><span class="sxs-lookup"><span data-stu-id="5359d-323">Remarks - AOTgetExecutableLineCount</span></span>

<span data-ttu-id="5359d-324">この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5359d-324">This function calls a method which is overridden by nodes which have source code.</span></span>

## <a name="method-aotgetexecutablelines"></a><span data-ttu-id="5359d-325">メソッド AOTgetExecutableLines</span><span class="sxs-lookup"><span data-stu-id="5359d-325">Method AOTgetExecutableLines</span></span>

<span data-ttu-id="5359d-326">このノードのコードの実行可能な行を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-326">Returns the executable lines of code for this node.</span></span>

```xpp
public Set AOTgetExecutableLines()
```

### <a name="return-value---aotgetexecutablelines"></a><span data-ttu-id="5359d-327">戻り値 - AOTgetExecutableLines</span><span class="sxs-lookup"><span data-stu-id="5359d-327">Return Value - AOTgetExecutableLines</span></span>

<span data-ttu-id="5359d-328">このノードに実行可能なコード行が含まれているセット オブジェクト; それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="5359d-328">A Set object containing the executable lines of code for this node if any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetexecutablelines"></a><span data-ttu-id="5359d-329">備考 - AOTgetExecutableLines</span><span class="sxs-lookup"><span data-stu-id="5359d-329">Remarks - AOTgetExecutableLines</span></span>

<span data-ttu-id="5359d-330">この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5359d-330">This function calls a method which is overridden by nodes which have source code.</span></span>

## <a name="method-aotgetmodel"></a><span data-ttu-id="5359d-331">メソッド AOTGetModel</span><span class="sxs-lookup"><span data-stu-id="5359d-331">Method AOTGetModel</span></span>

```xpp
public int AOTGetModel()
```

### <a name="return-value---aotgetmodel"></a><span data-ttu-id="5359d-332">戻り値 - AOTGetModel</span><span class="sxs-lookup"><span data-stu-id="5359d-332">Return Value - AOTGetModel</span></span>

## <a name="method-aotgetproperties"></a><span data-ttu-id="5359d-333">メソッド AOTgetProperties</span><span class="sxs-lookup"><span data-stu-id="5359d-333">Method AOTgetProperties</span></span>

<span data-ttu-id="5359d-334">ツリー ノードのプロパティを含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-334">Returns a string containing the properties of the tree node.</span></span>

```xpp
public str AOTgetProperties([boolean includeInvisible], [boolean includeReadOnly], [boolean includeNonExportable])
```

### <a name="parameters---aotgetproperties"></a><span data-ttu-id="5359d-335">パラメーター - AOTgetProperties</span><span class="sxs-lookup"><span data-stu-id="5359d-335">Parameters - AOTgetProperties</span></span>

<span data-ttu-id="5359d-336">includeInvisible</span><span class="sxs-lookup"><span data-stu-id="5359d-336">includeInvisible</span></span>  

<!-- -->

<span data-ttu-id="5359d-337">includeReadOnly</span><span class="sxs-lookup"><span data-stu-id="5359d-337">includeReadOnly</span></span>  

<!-- -->

<span data-ttu-id="5359d-338">includeNonExportable</span><span class="sxs-lookup"><span data-stu-id="5359d-338">includeNonExportable</span></span>  

### <a name="return-value---aotgetproperties"></a><span data-ttu-id="5359d-339">戻り値 - AOTgetProperties</span><span class="sxs-lookup"><span data-stu-id="5359d-339">Return Value - AOTgetProperties</span></span>

<span data-ttu-id="5359d-340">ツリー ノードのプロパティを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-340">A string containing the properties of the tree node.</span></span>

### <a name="examples---aotgetproperties"></a><span data-ttu-id="5359d-341">例 - AOTgetProperties</span><span class="sxs-lookup"><span data-stu-id="5359d-341">Examples - AOTgetProperties</span></span>

<span data-ttu-id="5359d-342">次の例では、一時テーブルのリストを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-342">The following example provides a list of temporary tables.</span></span>

```xpp
{ 
    #aot 
    #properties 
    TreeNode        tn = TreeNode::findNode(#TablesPath); 
    str             tableName; 
    str             temporaryProperty; 
    tn = tn.AOTfirstChild(); 
    while (tn) 
    { 
        tableName = findProperty(tn.AOTgetProperties(), #PropertyName); 
        temporaryProperty = findProperty( 
            tn.AOTgetProperties(), 
            #PropertyTemporary); 
        info (strfmt( 
            'Table %1 has the temporary property specified as %2', 
            tableName, temporaryProperty)); 
        tn = tn.AOTnextSibling(); 
    } 
}
```

## <a name="method-aotgetpropertiesext"></a><span data-ttu-id="5359d-343">メソッド AOTgetPropertiesExt</span><span class="sxs-lookup"><span data-stu-id="5359d-343">Method AOTgetPropertiesExt</span></span>

```xpp
public Struct AOTgetPropertiesExt([str filter])
```

### <a name="parameters---aotgetpropertiesext"></a><span data-ttu-id="5359d-344">パラメーター - AOTgetPropertiesExt</span><span class="sxs-lookup"><span data-stu-id="5359d-344">Parameters - AOTgetPropertiesExt</span></span>

<span data-ttu-id="5359d-345">フィルター</span><span class="sxs-lookup"><span data-stu-id="5359d-345">filter</span></span>  

### <a name="return-value---aotgetpropertiesext"></a><span data-ttu-id="5359d-346">戻り値 - AOTgetPropertiesExt</span><span class="sxs-lookup"><span data-stu-id="5359d-346">Return Value - AOTgetPropertiesExt</span></span>

## <a name="method-aotgetproperty"></a><span data-ttu-id="5359d-347">メソッド AOTgetProperty</span><span class="sxs-lookup"><span data-stu-id="5359d-347">Method AOTgetProperty</span></span>

```xpp
public AnyType AOTgetProperty(str name)
```

### <a name="parameters---aotgetproperty"></a><span data-ttu-id="5359d-348">パラメーター - AOTgetProperty</span><span class="sxs-lookup"><span data-stu-id="5359d-348">Parameters - AOTgetProperty</span></span>

<span data-ttu-id="5359d-349">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-349">name</span></span>  

### <a name="return-value---aotgetproperty"></a><span data-ttu-id="5359d-350">戻り値 - AOTgetProperty</span><span class="sxs-lookup"><span data-stu-id="5359d-350">Return Value - AOTgetProperty</span></span>

## <a name="method-aotgetsource"></a><span data-ttu-id="5359d-351">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="5359d-351">Method AOTgetSource</span></span>

<span data-ttu-id="5359d-352">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-352">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="5359d-353">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="5359d-353">Return Value - AOTgetSource</span></span>

<span data-ttu-id="5359d-354">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="5359d-354">The string that contains source code if any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="5359d-355">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="5359d-355">Remarks - AOTgetSource</span></span>

<span data-ttu-id="5359d-356">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="5359d-356">This function is overridden by nodes which have source code.</span></span>

## <a name="method-aotincludeincompare"></a><span data-ttu-id="5359d-357">メソッド AOTIncludeInCompare</span><span class="sxs-lookup"><span data-stu-id="5359d-357">Method AOTIncludeInCompare</span></span>

```xpp
public boolean AOTIncludeInCompare()
```

### <a name="return-value---aotincludeincompare"></a><span data-ttu-id="5359d-358">戻り値 - AOTIncludeInCompare</span><span class="sxs-lookup"><span data-stu-id="5359d-358">Return Value - AOTIncludeInCompare</span></span>

## <a name="method-aotisdirty"></a><span data-ttu-id="5359d-359">メソッド AOTIsDirty</span><span class="sxs-lookup"><span data-stu-id="5359d-359">Method AOTIsDirty</span></span>

```xpp
public boolean AOTIsDirty()
```

### <a name="return-value---aotisdirty"></a><span data-ttu-id="5359d-360">戻り値 - AOTIsDirty</span><span class="sxs-lookup"><span data-stu-id="5359d-360">Return Value - AOTIsDirty</span></span>

## <a name="method-aotisold"></a><span data-ttu-id="5359d-361">メソッド AOTIsOld</span><span class="sxs-lookup"><span data-stu-id="5359d-361">Method AOTIsOld</span></span>

<span data-ttu-id="5359d-362">このノードが、古いモデル ストアにあるファイルのものかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-362">Indicates whether this node is from a file found in the old model store.</span></span>

```xpp
public boolean AOTIsOld()
```

### <a name="return-value---aotisold"></a><span data-ttu-id="5359d-363">戻り値 - AOTIsOld</span><span class="sxs-lookup"><span data-stu-id="5359d-363">Return Value - AOTIsOld</span></span>

<span data-ttu-id="5359d-364">このノードが古いモデル ストアに由来する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5359d-364">true if this node is from the old model store; otherwise false.</span></span>

## <a name="method-aotispersisted"></a><span data-ttu-id="5359d-365">メソッド AOTIsPersisted</span><span class="sxs-lookup"><span data-stu-id="5359d-365">Method AOTIsPersisted</span></span>

<span data-ttu-id="5359d-366">このノードがモデル ストアに保持されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-366">Indicates whether this node has been persisted in the model store.</span></span>

```xpp
public boolean AOTIsPersisted()
```

### <a name="return-value---aotispersisted"></a><span data-ttu-id="5359d-367">戻り値 - AOTIsPersisted</span><span class="sxs-lookup"><span data-stu-id="5359d-367">Return Value - AOTIsPersisted</span></span>

<span data-ttu-id="5359d-368">このノードが保持された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5359d-368">true if this node has been persisted; otherwise false.</span></span>

### <a name="remarks---aotispersisted"></a><span data-ttu-id="5359d-369">備考 - AOTIsPersisted</span><span class="sxs-lookup"><span data-stu-id="5359d-369">Remarks - AOTIsPersisted</span></span>

<span data-ttu-id="5359d-370">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5359d-370">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="5359d-371">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isModelElement() メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5359d-371">Use the TreeNode.TreeNodeType().isModelElement() method to determine if the method is supported.</span></span>

## <a name="method-aotisproxynode"></a><span data-ttu-id="5359d-372">メソッド AOTIsProxyNode</span><span class="sxs-lookup"><span data-stu-id="5359d-372">Method AOTIsProxyNode</span></span>

```xpp
public boolean AOTIsProxyNode()
```

### <a name="return-value---aotisproxynode"></a><span data-ttu-id="5359d-373">戻り値 - AOTIsProxyNode</span><span class="sxs-lookup"><span data-stu-id="5359d-373">Return Value - AOTIsProxyNode</span></span>

## <a name="method-aotiterator"></a><span data-ttu-id="5359d-374">メソッド AOTiterator</span><span class="sxs-lookup"><span data-stu-id="5359d-374">Method AOTiterator</span></span>

<span data-ttu-id="5359d-375">ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-375">Returns an object which can be used to iterate the child nodes of the tree node.</span></span>

```xpp
public TreeNodeIterator AOTiterator()
```

### <a name="return-value---aotiterator"></a><span data-ttu-id="5359d-376">戻り値 - AOTiterator</span><span class="sxs-lookup"><span data-stu-id="5359d-376">Return Value - AOTiterator</span></span>

<span data-ttu-id="5359d-377">ツリー ノードの子を反復処理するために使用する TreeNodeIterator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5359d-377">The TreeNodeIterator object used to iterate the children of the tree node.</span></span>

## <a name="method-aotkernelhelptype"></a><span data-ttu-id="5359d-378">メソッド AOTKernelHelpType</span><span class="sxs-lookup"><span data-stu-id="5359d-378">Method AOTKernelHelpType</span></span>

```xpp
public KernelHelpType AOTKernelHelpType()
```

### <a name="return-value---aotkernelhelptype"></a><span data-ttu-id="5359d-379">戻り値 - AOTKernelHelpType</span><span class="sxs-lookup"><span data-stu-id="5359d-379">Return Value - AOTKernelHelpType</span></span>

## <a name="method-aotlayer"></a><span data-ttu-id="5359d-380">メソッド AOTLayer</span><span class="sxs-lookup"><span data-stu-id="5359d-380">Method AOTLayer</span></span>

<span data-ttu-id="5359d-381">ツリー ノードのレイヤーを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-381">Returns the layer of the tree node.</span></span>

```xpp
public UtilEntryLevel AOTLayer()
```

### <a name="return-value---aotlayer"></a><span data-ttu-id="5359d-382">戻り値 - AOTLayer</span><span class="sxs-lookup"><span data-stu-id="5359d-382">Return Value - AOTLayer</span></span>

<span data-ttu-id="5359d-383">このノードが存在するレイヤー。</span><span class="sxs-lookup"><span data-stu-id="5359d-383">The layer that this node resides in.</span></span>

### <a name="remarks---aotlayer"></a><span data-ttu-id="5359d-384">備考 - AOTLayer</span><span class="sxs-lookup"><span data-stu-id="5359d-384">Remarks - AOTLayer</span></span>

<span data-ttu-id="5359d-385">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5359d-385">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="5359d-386">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5359d-386">Use the TreeNode.TreeNodeType().isLayerAware() method to determine if the method is supported.</span></span>

## <a name="method-aotlayers"></a><span data-ttu-id="5359d-387">メソッド AOTLayers</span><span class="sxs-lookup"><span data-stu-id="5359d-387">Method AOTLayers</span></span>

<span data-ttu-id="5359d-388">そのツリー ノードで定義されているレイヤーのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-388">Returns a collection of the layers the tree node is defined in.</span></span>

```xpp
public Set AOTLayers([boolean old])
```

### <a name="parameters---aotlayers"></a><span data-ttu-id="5359d-389">パラメーター - AOTLayers</span><span class="sxs-lookup"><span data-stu-id="5359d-389">Parameters - AOTLayers</span></span>

<span data-ttu-id="5359d-390">old</span><span class="sxs-lookup"><span data-stu-id="5359d-390">old</span></span>  
<span data-ttu-id="5359d-391">古いモデル ストアからツリー ノード定義のレイヤーを返すかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="5359d-391">A Boolean value that indicates whether to return the layers of the tree node definitions from the old model store; optional.</span></span>

### <a name="return-value---aotlayers"></a><span data-ttu-id="5359d-392">戻り値 - AOTLayers</span><span class="sxs-lookup"><span data-stu-id="5359d-392">Return Value - AOTLayers</span></span>

<span data-ttu-id="5359d-393">レイヤーを持つセット オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5359d-393">A Set object with the layers.</span></span>

### <a name="remarks---aotlayers"></a><span data-ttu-id="5359d-394">備考 - AOTLayers</span><span class="sxs-lookup"><span data-stu-id="5359d-394">Remarks - AOTLayers</span></span>

<span data-ttu-id="5359d-395">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5359d-395">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="5359d-396">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5359d-396">Use the TreeNode.TreeNodeType().isLayerAware() method to determine if the method is supported.</span></span>

## <a name="method-aotname"></a><span data-ttu-id="5359d-397">メソッド AOTname</span><span class="sxs-lookup"><span data-stu-id="5359d-397">Method AOTname</span></span>

<span data-ttu-id="5359d-398">ノードの name プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-398">Returns the value of the name property of the node.</span></span>

```xpp
public str AOTname()
```

### <a name="return-value---aotname"></a><span data-ttu-id="5359d-399">戻り値 - AOTname</span><span class="sxs-lookup"><span data-stu-id="5359d-399">Return Value - AOTname</span></span>

<span data-ttu-id="5359d-400">name プロパティの値を含む文字列</span><span class="sxs-lookup"><span data-stu-id="5359d-400">The string that contains the value of the name property</span></span>

### <a name="remarks---aotname"></a><span data-ttu-id="5359d-401">備考 - AOTname</span><span class="sxs-lookup"><span data-stu-id="5359d-401">Remarks - AOTname</span></span>

<span data-ttu-id="5359d-402">ほとんどの場合、メソッド TreeNodeName と同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="5359d-402">In most cases, this yields the same result as the method TreeNodeName.</span></span>

### <a name="examples---aotname"></a><span data-ttu-id="5359d-403">例 - AOTname</span><span class="sxs-lookup"><span data-stu-id="5359d-403">Examples - AOTname</span></span>

<span data-ttu-id="5359d-404">次の例では、ツリー ノードの最初の子の名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="5359d-404">The following example prints out the name of the first child of the tree node.</span></span>

```xpp
static void Job(Args _args) 
{ 
    treeNode t = infolog.findNode('\\Reports\\AssetAcquisition\\Designs\\ReportDesign1\\AutoDesignSpecs'); 
    t = t.AOTfirstChild(); 
    print "treeNodeName: " + t.treeNodeName(); 
    print "AOTName:" + t.AOTName(); 
    pause; 
}
```

## <a name="method-aotnewwindow"></a><span data-ttu-id="5359d-405">メソッド AOTnewWindow</span><span class="sxs-lookup"><span data-stu-id="5359d-405">Method AOTnewWindow</span></span>

<span data-ttu-id="5359d-406">ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。</span><span class="sxs-lookup"><span data-stu-id="5359d-406">Opens a new AOT tree window with the tree node as the root.</span></span>

```xpp
public int AOTnewWindow()
```

### <a name="return-value---aotnewwindow"></a><span data-ttu-id="5359d-407">戻り値 - AOTnewWindow</span><span class="sxs-lookup"><span data-stu-id="5359d-407">Return Value - AOTnewWindow</span></span>

## <a name="method-aotnextsibling"></a><span data-ttu-id="5359d-408">メソッド AOTnextSibling</span><span class="sxs-lookup"><span data-stu-id="5359d-408">Method AOTnextSibling</span></span>

<span data-ttu-id="5359d-409">ツリー ノードと同じレベルにある次のノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-409">Returns the next node on the same level as the tree node.</span></span>

```xpp
public TreeNode AOTnextSibling()
```

### <a name="return-value---aotnextsibling"></a><span data-ttu-id="5359d-410">戻り値 - AOTnextSibling</span><span class="sxs-lookup"><span data-stu-id="5359d-410">Return Value - AOTnextSibling</span></span>

<span data-ttu-id="5359d-411">現在のツリー ノードと同じレベルにある次のノード。</span><span class="sxs-lookup"><span data-stu-id="5359d-411">The next node on the same level as the current tree node.</span></span>

## <a name="method-aotobjectnode"></a><span data-ttu-id="5359d-412">メソッド AOTObjectNode</span><span class="sxs-lookup"><span data-stu-id="5359d-412">Method AOTObjectNode</span></span>

<span data-ttu-id="5359d-413">ノードがアプリケーション オブジェクトであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-413">Indicates whether the node is an application object.</span></span>

```xpp
public boolean AOTObjectNode()
```

### <a name="return-value---aotobjectnode"></a><span data-ttu-id="5359d-414">戻り値 - AOTObjectNode</span><span class="sxs-lookup"><span data-stu-id="5359d-414">Return Value - AOTObjectNode</span></span>

<span data-ttu-id="5359d-415">ノードがアプリケーション オブジェクトである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5359d-415">true if the node is an application object; otherwise false.</span></span>

### <a name="remarks---aotobjectnode"></a><span data-ttu-id="5359d-416">備考 - AOTObjectNode</span><span class="sxs-lookup"><span data-stu-id="5359d-416">Remarks - AOTObjectNode</span></span>

<span data-ttu-id="5359d-417">フォームまたはレポートは、アプリケーション オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="5359d-417">A form or report is an application object.</span></span> <span data-ttu-id="5359d-418">フォーム、またはその他のサブパートのコントロールはありません。</span><span class="sxs-lookup"><span data-stu-id="5359d-418">A control on a form, or any other subpart, is not.</span></span>

## <a name="method-aotoverlaybitmapid"></a><span data-ttu-id="5359d-419">メソッド AOToverlayBitmapId</span><span class="sxs-lookup"><span data-stu-id="5359d-419">Method AOToverlayBitmapId</span></span>

<span data-ttu-id="5359d-420">このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-420">Returns the resource ID of the overlay in the AOT associated with this node.</span></span>

```xpp
public int AOToverlayBitmapId()
```

### <a name="return-value---aotoverlaybitmapid"></a><span data-ttu-id="5359d-421">戻り値 - AOToverlayBitmapId</span><span class="sxs-lookup"><span data-stu-id="5359d-421">Return Value - AOToverlayBitmapId</span></span>

<span data-ttu-id="5359d-422">このノードに関連付けられた AOT のオーバーレイのリソース ID。</span><span class="sxs-lookup"><span data-stu-id="5359d-422">The resource ID of the overlay in the AOT associated with this node.</span></span>

## <a name="method-aotparent"></a><span data-ttu-id="5359d-423">メソッド AOTparent</span><span class="sxs-lookup"><span data-stu-id="5359d-423">Method AOTparent</span></span>

<span data-ttu-id="5359d-424">ツリー ノードの親ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-424">Returns the parent node of the tree node.</span></span>

```xpp
public TreeNode AOTparent()
```

### <a name="return-value---aotparent"></a><span data-ttu-id="5359d-425">戻り値 - AOTparent</span><span class="sxs-lookup"><span data-stu-id="5359d-425">Return Value - AOTparent</span></span>

<span data-ttu-id="5359d-426">ツリー ノードの親ノード。</span><span class="sxs-lookup"><span data-stu-id="5359d-426">The parent node of the tree node.</span></span>

## <a name="method-aotprevious"></a><span data-ttu-id="5359d-427">メソッド AOTprevious</span><span class="sxs-lookup"><span data-stu-id="5359d-427">Method AOTprevious</span></span>

<span data-ttu-id="5359d-428">このツリー ノードの前の兄弟を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-428">Returns the previous sibling of this tree node.</span></span>

```xpp
public TreeNode AOTprevious()
```

### <a name="return-value---aotprevious"></a><span data-ttu-id="5359d-429">戻り値 - AOTprevious</span><span class="sxs-lookup"><span data-stu-id="5359d-429">Return Value - AOTprevious</span></span>

<span data-ttu-id="5359d-430">同じレベルにある、このツリー ノードの前のツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="5359d-430">The previous tree node relative to this one on the same level.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-431">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-431">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(str name)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-432">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-432">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-433">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-433">name</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5359d-434">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-434">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-aottooltip"></a><span data-ttu-id="5359d-435">メソッド AOTtoolTip</span><span class="sxs-lookup"><span data-stu-id="5359d-435">Method AOTtoolTip</span></span>

<span data-ttu-id="5359d-436">そのツリー ノードに関連付けられているツールヒントを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-436">Returns the tool tip associated with the tree node.</span></span>

```xpp
public str AOTtoolTip()
```

### <a name="return-value---aottooltip"></a><span data-ttu-id="5359d-437">戻り値 - AOTtoolTip</span><span class="sxs-lookup"><span data-stu-id="5359d-437">Return Value - AOTtoolTip</span></span>

<span data-ttu-id="5359d-438">ツール チップを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-438">The string that contains the tool tip.</span></span>

## <a name="method-aottostring"></a><span data-ttu-id="5359d-439">メソッド AOTToString</span><span class="sxs-lookup"><span data-stu-id="5359d-439">Method AOTToString</span></span>

```xpp
public str AOTToString()
```

### <a name="return-value---aottostring"></a><span data-ttu-id="5359d-440">戻り値 - AOTToString</span><span class="sxs-lookup"><span data-stu-id="5359d-440">Return Value - AOTToString</span></span>

## <a name="method-aottypestr"></a><span data-ttu-id="5359d-441">メソッド AOTtypeStr</span><span class="sxs-lookup"><span data-stu-id="5359d-441">Method AOTtypeStr</span></span>

<span data-ttu-id="5359d-442">XPO ファイルで使用される要素タイプの文字列の内部コードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-442">Returns the internal string code for the element type used in XPO files.</span></span>

```xpp
public str AOTtypeStr()
```

### <a name="return-value---aottypestr"></a><span data-ttu-id="5359d-443">戻り値 - AOTtypeStr</span><span class="sxs-lookup"><span data-stu-id="5359d-443">Return Value - AOTtypeStr</span></span>

<span data-ttu-id="5359d-444">ツリー ノードのタイプを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-444">The string that contains the tree node type.</span></span>

## <a name="method-aotutilfiletype"></a><span data-ttu-id="5359d-445">メソッド AOTUtilFileType</span><span class="sxs-lookup"><span data-stu-id="5359d-445">Method AOTUtilFileType</span></span>

<span data-ttu-id="5359d-446">TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-446">Retrieves the value of the UtilFileType enumeration type for the TreeNode object.</span></span> <span data-ttu-id="5359d-447">UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-447">The UtilFileType indicates which kind of file the application object is stored in.</span></span>

```xpp
public UtilFileType AOTUtilFileType()
```

### <a name="return-value---aotutilfiletype"></a><span data-ttu-id="5359d-448">戻り値 - AOTUtilFileType</span><span class="sxs-lookup"><span data-stu-id="5359d-448">Return Value - AOTUtilFileType</span></span>

<span data-ttu-id="5359d-449">ツリー ノードの UtilFileType 列挙値。</span><span class="sxs-lookup"><span data-stu-id="5359d-449">The value of the UtilFileType enumeration for the tree node.</span></span> <span data-ttu-id="5359d-450">可能な値を次の一覧に示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-450">The possible values are in the following list.</span></span> <span data-ttu-id="5359d-451">UtilFileType::Application は、要素 (フォーム、レポート、クエリ、テーブルなど) が .aod ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="5359d-451">UtilFileType::Application means that the element is stored in the .aod file (form, report, query, table, and so on).</span></span> <span data-ttu-id="5359d-452">UtilFileType::ApplicationCodeDocumentation は、要素が .add ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="5359d-452">UtilFileType::ApplicationCodeDocumentation means that the element is stored in the .add file.</span></span> <span data-ttu-id="5359d-453">UtilFileType::ApplicationHelp は、要素が .ahd ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="5359d-453">UtilFileType::ApplicationHelp means that the element is stored in the .ahd file.</span></span> <span data-ttu-id="5359d-454">UtilFileType::KernelHelp は、要素が .akh ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="5359d-454">UtilFileType::KernelHelp means that the element is stored in the .akh file.</span></span>

### <a name="examples---aotutilfiletype"></a><span data-ttu-id="5359d-455">例 - AOTUtilFileType</span><span class="sxs-lookup"><span data-stu-id="5359d-455">Examples - AOTUtilFileType</span></span>

<span data-ttu-id="5359d-456">次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。</span><span class="sxs-lookup"><span data-stu-id="5359d-456">The following example finds a TreeNode object of each UtilFileType, and then prints the path of the UtilFileType to the Infolog.</span></span>

```xpp
static void myJob(Args _args) 
{ 
    treeNode tn; 
    tn = treeNode::findNode("\\Forms"); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
         "Path: %1 \nUtilFileType: %2", 
         tn.treeNodePath(), 
         tn.AOTUtilFileType())); 
    tn = treeNode::findNode("\\System Documentation"); 
    tn = tn.AOTfirstChild(); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
         "Path: %1 \nUtilFileType: %2", 
         tn.treeNodePath(), 
         tn.AOTUtilFileType())); 
    tn = treeNode::findNode("\\Application Developer Documentation"); 
    tn = tn.AOTfirstChild(); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
        "Path: %1 \nUtilFileType: %2", 
        tn.treeNodePath(), 
        tn.AOTUtilFileType())); 
    tn = treeNode::findNode("\\Application Documentation"); 
    tn = tn.AOTfirstChild(); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
        "Path: %1 \nUtilFileType: %2", 
        tn.treeNodePath(), 
        tn.AOTUtilFileType())); 
}
```

## <a name="method-applobjectid"></a><span data-ttu-id="5359d-457">メソッド applObjectId</span><span class="sxs-lookup"><span data-stu-id="5359d-457">Method applObjectId</span></span>

<span data-ttu-id="5359d-458">該当する場合は、アプリケーション オブジェクト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-458">Returns the application object ID, if applicable.</span></span>

```xpp
public int applObjectId()
```

### <a name="return-value---applobjectid"></a><span data-ttu-id="5359d-459">戻り値 - applObjectId</span><span class="sxs-lookup"><span data-stu-id="5359d-459">Return Value - applObjectId</span></span>

<span data-ttu-id="5359d-460">アプリケーション オブジェクトの ID。</span><span class="sxs-lookup"><span data-stu-id="5359d-460">The ID of the application object.</span></span>

## <a name="method-applobjectlayermask"></a><span data-ttu-id="5359d-461">メソッド applObjectLayerMask</span><span class="sxs-lookup"><span data-stu-id="5359d-461">Method applObjectLayerMask</span></span>

<span data-ttu-id="5359d-462">この要素を含むレイヤーを指定するビットを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-462">Returns a bitmask that specifies which layers contain this element.</span></span>

```xpp
public int applObjectLayerMask()
```

### <a name="return-value---applobjectlayermask"></a><span data-ttu-id="5359d-463">戻り値 - applObjectLayerMask</span><span class="sxs-lookup"><span data-stu-id="5359d-463">Return Value - applObjectLayerMask</span></span>

<span data-ttu-id="5359d-464">この要素を含むレイヤーを指定するビット。</span><span class="sxs-lookup"><span data-stu-id="5359d-464">A bitmask that specifies which layers contain this element.</span></span>

## <a name="method-applobjectoldlayermask"></a><span data-ttu-id="5359d-465">メソッド applObjectOldLayerMask</span><span class="sxs-lookup"><span data-stu-id="5359d-465">Method applObjectOldLayerMask</span></span>

<span data-ttu-id="5359d-466">ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-466">Returns a bitmask that specifies which layers contain this element in the baseline model store.</span></span>

```xpp
public int applObjectOldLayerMask()
```

### <a name="return-value---applobjectoldlayermask"></a><span data-ttu-id="5359d-467">戻り値 - applObjectOldLayerMask</span><span class="sxs-lookup"><span data-stu-id="5359d-467">Return Value - applObjectOldLayerMask</span></span>

<span data-ttu-id="5359d-468">この要素を含むレイヤーを指定するビット。</span><span class="sxs-lookup"><span data-stu-id="5359d-468">A bitmask that specifies which layers contain this element.</span></span>

## <a name="method-getnodeinlayer"></a><span data-ttu-id="5359d-469">メソッド getNodeInLayer</span><span class="sxs-lookup"><span data-stu-id="5359d-469">Method getNodeInLayer</span></span>

<span data-ttu-id="5359d-470">指定したレイヤーからツリー ノードのバージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-470">Retrieves a version of the tree node from a specified layer.</span></span>

```xpp
public TreeNode getNodeInLayer(UtilEntryLevel layer, [boolean old])
```

### <a name="parameters---getnodeinlayer"></a><span data-ttu-id="5359d-471">パラメーター - getNodeInLayer</span><span class="sxs-lookup"><span data-stu-id="5359d-471">Parameters - getNodeInLayer</span></span>

<span data-ttu-id="5359d-472"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="5359d-472">layer</span></span>  
<span data-ttu-id="5359d-473">古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5359d-473">The value specifying whether or not the node should be retrieved from the layer file in the old model store; optional.</span></span>

<!-- -->

<span data-ttu-id="5359d-474">old</span><span class="sxs-lookup"><span data-stu-id="5359d-474">old</span></span>  
<span data-ttu-id="5359d-475">古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5359d-475">The value specifying whether or not the node should be retrieved from the layer file in the old model store; optional.</span></span>

### <a name="return-value---getnodeinlayer"></a><span data-ttu-id="5359d-476">戻り値 - getNodeInLayer</span><span class="sxs-lookup"><span data-stu-id="5359d-476">Return Value - getNodeInLayer</span></span>

<span data-ttu-id="5359d-477">新しい TreeNode。</span><span class="sxs-lookup"><span data-stu-id="5359d-477">The new TreeNode.</span></span>

### <a name="remarks---getnodeinlayer"></a><span data-ttu-id="5359d-478">備考 - getNodeInLayer</span><span class="sxs-lookup"><span data-stu-id="5359d-478">Remarks - getNodeInLayer</span></span>

<span data-ttu-id="5359d-479">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5359d-479">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="5359d-480">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isGetNodeInLayerSupported メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5359d-480">Use the TreeNode.TreeNodeType().isGetNodeInLayerSupported method to determine if the method is supported.</span></span>

## <a name="method-hashkey"></a><span data-ttu-id="5359d-481">メソッド hashKey</span><span class="sxs-lookup"><span data-stu-id="5359d-481">Method hashKey</span></span>

```xpp
public Int64 hashKey()
```

### <a name="return-value---hashkey"></a><span data-ttu-id="5359d-482">戻り値 - hashKey</span><span class="sxs-lookup"><span data-stu-id="5359d-482">Return Value - hashKey</span></span>

## <a name="method-makecopy"></a><span data-ttu-id="5359d-483">メソッド makeCopy</span><span class="sxs-lookup"><span data-stu-id="5359d-483">Method makeCopy</span></span>

```xpp
public TreeNode makeCopy()
```

### <a name="return-value---makecopy"></a><span data-ttu-id="5359d-484">戻り値 - makeCopy</span><span class="sxs-lookup"><span data-stu-id="5359d-484">Return Value - makeCopy</span></span>

## <a name="method-newobjectname"></a><span data-ttu-id="5359d-485">メソッド newObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-485">Method newObjectName</span></span>

<span data-ttu-id="5359d-486">新しい要素の名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-486">Returns a string that contains the name of the new element.</span></span>

```xpp
public str newObjectName([str oldName])
```

### <a name="parameters---newobjectname"></a><span data-ttu-id="5359d-487">パラメーター - newObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-487">Parameters - newObjectName</span></span>

<span data-ttu-id="5359d-488">oldName</span><span class="sxs-lookup"><span data-stu-id="5359d-488">oldName</span></span>  
<span data-ttu-id="5359d-489">ノードの新しい名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5359d-489">The new name of the node; optional.</span></span> <span data-ttu-id="5359d-490">引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="5359d-490">If no argument is passed, the new node name is determined by the child node type.</span></span>

### <a name="return-value---newobjectname"></a><span data-ttu-id="5359d-491">戻り値 - newObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-491">Return Value - newObjectName</span></span>

<span data-ttu-id="5359d-492">新しい要素の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-492">The string that contains the name of the new element.</span></span>

### <a name="remarks---newobjectname"></a><span data-ttu-id="5359d-493">備考 - newObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-493">Remarks - newObjectName</span></span>

<span data-ttu-id="5359d-494">引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="5359d-494">If no argument is passed, the new node name is determined by the child node type.</span></span> <span data-ttu-id="5359d-495">たとえば、TreeNode に子としてフォームがある場合、引数なしのこのメソッドの呼び出しは「Form1」を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-495">For example, if the TreeNode has forms as children, calling this method without an argument will return "Form1".</span></span> <span data-ttu-id="5359d-496">ツリー ノードに複数の子ノードがある場合は、メソッドは "object" という文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-496">If the tree node has several child node types, the method returns the string "object".</span></span>

### <a name="examples---newobjectname"></a><span data-ttu-id="5359d-497">例 - newObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-497">Examples - newObjectName</span></span>

<span data-ttu-id="5359d-498">次の Treenode.newObjectName の呼び出しでは、データ ディクショナリ ノードに複数のオブジェクト型を表す子があるため、「object」が返されます。</span><span class="sxs-lookup"><span data-stu-id="5359d-498">The following call to Treenode.newObjectName returns "object" because the data dictionary node has children that represent several object types.</span></span>

```xpp
{ 
    TreeNode t; 
    str s; 
    t = TreeNode::findNode("\Data dictionary"); 
    s = t.newObjectName(); 
    print s; 
    pause; 
}
```

## <a name="method-tostring"></a><span data-ttu-id="5359d-499">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="5359d-499">Method toString</span></span>

<span data-ttu-id="5359d-500">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-500">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="5359d-501">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="5359d-501">Return Value - toString</span></span>

<span data-ttu-id="5359d-502">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-502">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="5359d-503">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="5359d-503">Remarks - toString</span></span>

<span data-ttu-id="5359d-504">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-504">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="5359d-505">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5359d-505">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="5359d-506">たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-506">For example, an instance of the class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-treenodename"></a><span data-ttu-id="5359d-507">メソッド treeNodeName</span><span class="sxs-lookup"><span data-stu-id="5359d-507">Method treeNodeName</span></span>

<span data-ttu-id="5359d-508">ツリー ノードの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-508">Returns the name of the tree node.</span></span>

```xpp
public str treeNodeName()
```

### <a name="return-value---treenodename"></a><span data-ttu-id="5359d-509">戻り値 - treeNodeName</span><span class="sxs-lookup"><span data-stu-id="5359d-509">Return Value - treeNodeName</span></span>

<span data-ttu-id="5359d-510">ツリー ノードの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-510">The string that contains the name of the tree node.</span></span>

## <a name="method-treenodepath"></a><span data-ttu-id="5359d-511">メソッド treeNodePath</span><span class="sxs-lookup"><span data-stu-id="5359d-511">Method treeNodePath</span></span>

<span data-ttu-id="5359d-512">アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-512">Returns the unique path to the tree node within the Application Object Tree (AOT).</span></span>

```xpp
public str treeNodePath()
```

### <a name="return-value---treenodepath"></a><span data-ttu-id="5359d-513">戻り値 - treeNodePath</span><span class="sxs-lookup"><span data-stu-id="5359d-513">Return Value - treeNodePath</span></span>

<span data-ttu-id="5359d-514">AOT 内のツリー ノードの一意のパスを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-514">Returns the unique path of the tree node in the AOT.</span></span>

### <a name="examples---treenodepath"></a><span data-ttu-id="5359d-515">例 - treeNodePath</span><span class="sxs-lookup"><span data-stu-id="5359d-515">Examples - treeNodePath</span></span>

<span data-ttu-id="5359d-516">次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。</span><span class="sxs-lookup"><span data-stu-id="5359d-516">The following example finds a TreeNode object of each UtilFileType and prints the path of the UtilFileType to the Infolog.</span></span>

```xpp
static void myJob(Args _args) 
{ 
    treeNode tn; 
    tn = treeNode::findNode("\\Forms"); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
         "Path: %1 \nUtilFileType: %2", 
         tn.treeNodePath(), 
         tn.AOTUtilFileType())); 
    tn = treeNode::findNode("\\System Documentation"); 
    tn = tn.AOTfirstChild(); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
         "Path: %1 \nUtilFileType: %2", 
         tn.treeNodePath(), 
         tn.AOTUtilFileType())); 
    tn = treeNode::findNode("\\Application Developer Documentation"); 
    tn = tn.AOTfirstChild(); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
        "Path: %1 \nUtilFileType: %2", 
        tn.treeNodePath(), 
        tn.AOTUtilFileType())); 
    tn = treeNode::findNode("\\Application Documentation"); 
    tn = tn.AOTfirstChild(); 
    tn = tn.AOTfirstChild(); 
    info(strfmt( 
        "Path: %1 \nUtilFileType: %2", 
        tn.treeNodePath(), 
        tn.AOTUtilFileType())); 
}
```

## <a name="method-treenodetype"></a><span data-ttu-id="5359d-517">メソッド treeNodeType</span><span class="sxs-lookup"><span data-stu-id="5359d-517">Method treeNodeType</span></span>

<span data-ttu-id="5359d-518">ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-518">Retrieves an instance of a TreeNodeType class that provides reflection information for the tree node.</span></span>

```xpp
public TreeNodeType treeNodeType()
```

### <a name="return-value---treenodetype"></a><span data-ttu-id="5359d-519">戻り値 - treeNodeType</span><span class="sxs-lookup"><span data-stu-id="5359d-519">Return Value - treeNodeType</span></span>

<span data-ttu-id="5359d-520">TreeNodeType クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="5359d-520">An instance of a TreeNodeType class.</span></span>

## <a name="method-updatenodepermissions"></a><span data-ttu-id="5359d-521">メソッド updateNodePermissions</span><span class="sxs-lookup"><span data-stu-id="5359d-521">Method updateNodePermissions</span></span>

```xpp
public int updateNodePermissions(boolean throwExceptions)
```

### <a name="parameters---updatenodepermissions"></a><span data-ttu-id="5359d-522">パラメーター - updateNodePermissions</span><span class="sxs-lookup"><span data-stu-id="5359d-522">Parameters - updateNodePermissions</span></span>

<span data-ttu-id="5359d-523">throwExceptions</span><span class="sxs-lookup"><span data-stu-id="5359d-523">throwExceptions</span></span>  

### <a name="return-value---updatenodepermissions"></a><span data-ttu-id="5359d-524">戻り値 - updateNodePermissions</span><span class="sxs-lookup"><span data-stu-id="5359d-524">Return Value - updateNodePermissions</span></span>

## <a name="method-utilelement"></a><span data-ttu-id="5359d-525">メソッド utilElement</span><span class="sxs-lookup"><span data-stu-id="5359d-525">Method utilElement</span></span>

<span data-ttu-id="5359d-526">ノードに関連する UtilElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-526">Returns a UtilElements record that is related to the node.</span></span>

```xpp
public UtilElements utilElement()
```

### <a name="return-value---utilelement"></a><span data-ttu-id="5359d-527">戻り値 - utilElement</span><span class="sxs-lookup"><span data-stu-id="5359d-527">Return Value - utilElement</span></span>

<span data-ttu-id="5359d-528">ノードに関連する UtilElements レコード。</span><span class="sxs-lookup"><span data-stu-id="5359d-528">The UtilElements record that is related to the node.</span></span>

### <a name="remarks---utilelement"></a><span data-ttu-id="5359d-529">備考 - utilElement</span><span class="sxs-lookup"><span data-stu-id="5359d-529">Remarks - utilElement</span></span>

<span data-ttu-id="5359d-530">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5359d-530">This method throws an exception if the method is not supported for the tree node.</span></span>

## <a name="method-utilidelement"></a><span data-ttu-id="5359d-531">メソッド utilIdElement</span><span class="sxs-lookup"><span data-stu-id="5359d-531">Method utilIdElement</span></span>

<span data-ttu-id="5359d-532">ノードに関連する UtilIdElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-532">Returns a UtilIdElements record that is related to the node.</span></span>

```xpp
public UtilIdElements utilIdElement()
```

### <a name="return-value---utilidelement"></a><span data-ttu-id="5359d-533">戻り値 - utilIdElement</span><span class="sxs-lookup"><span data-stu-id="5359d-533">Return Value - utilIdElement</span></span>

<span data-ttu-id="5359d-534">ノードに関連する UtilIdElements レコード。</span><span class="sxs-lookup"><span data-stu-id="5359d-534">The UtilIdElements record that is related to the node.</span></span>

### <a name="remarks---utilidelement"></a><span data-ttu-id="5359d-535">備考 - utilIdElement</span><span class="sxs-lookup"><span data-stu-id="5359d-535">Remarks - utilIdElement</span></span>

<span data-ttu-id="5359d-536">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="5359d-536">This method throws an exception if the method is not supported for the tree node.</span></span>

## <a name="method-validatenamecharacters"></a><span data-ttu-id="5359d-537">メソッド validateNameCharacters</span><span class="sxs-lookup"><span data-stu-id="5359d-537">Method validateNameCharacters</span></span>

```xpp
public boolean validateNameCharacters(str name)
```

### <a name="parameters---validatenamecharacters"></a><span data-ttu-id="5359d-538">パラメーター - validateNameCharacters</span><span class="sxs-lookup"><span data-stu-id="5359d-538">Parameters - validateNameCharacters</span></span>

<span data-ttu-id="5359d-539">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-539">name</span></span>  

### <a name="return-value---validatenamecharacters"></a><span data-ttu-id="5359d-540">戻り値 - validateNameCharacters</span><span class="sxs-lookup"><span data-stu-id="5359d-540">Return Value - validateNameCharacters</span></span>

## <a name="method-findnode"></a><span data-ttu-id="5359d-541">メソッド findNode</span><span class="sxs-lookup"><span data-stu-id="5359d-541">Method findNode</span></span>

<span data-ttu-id="5359d-542">アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-542">Returns a specified node in the Application Object Tree (AOT).</span></span>

```xpp
public static TreeNode findNode(str path)
```

### <a name="parameters---findnode"></a><span data-ttu-id="5359d-543">パラメーター - findNode</span><span class="sxs-lookup"><span data-stu-id="5359d-543">Parameters - findNode</span></span>

<span data-ttu-id="5359d-544">path</span><span class="sxs-lookup"><span data-stu-id="5359d-544">path</span></span>  
<span data-ttu-id="5359d-545">検索で使用されるパスを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-545">A string that indicates the path that is used in the search.</span></span>

### <a name="return-value---findnode"></a><span data-ttu-id="5359d-546">戻り値 - findNode</span><span class="sxs-lookup"><span data-stu-id="5359d-546">Return Value - findNode</span></span>

<span data-ttu-id="5359d-547">指定されたパスのノードが存在しない場合の、要求された TreeNode オブジェクトまたは nullNothingnullptrunita null 参照 (Visual Basic ではなし)。</span><span class="sxs-lookup"><span data-stu-id="5359d-547">The requested TreeNode object or nullNothingnullptrunita null reference (Nothing in Visual Basic) if no node with the specified path exists.</span></span>

### <a name="remarks---findnode"></a><span data-ttu-id="5359d-548">備考 - findNode</span><span class="sxs-lookup"><span data-stu-id="5359d-548">Remarks - findNode</span></span>

<span data-ttu-id="5359d-549">TreeNode オブジェクトを取得する別の方法は、Info.getNode メソッドを使用することです。</span><span class="sxs-lookup"><span data-stu-id="5359d-549">Another way of getting a TreeNode object is by using the Info.getNode method.</span></span> <span data-ttu-id="5359d-550">2 つのメソッド間の重要な違いは、Info.getNode メソッドが AOT から分離されているノードを提供するのに対して一方 findNode メソッドは AOT のノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-550">An important difference between the two methods is that the Info.getNode method will give you a node that is detached from the AOT, whereas the findNode method will return the node in the AOT.</span></span> <span data-ttu-id="5359d-551">つまり、Info.getNode メソッドから返されるノードは親ノードを持たず、findNode メソッドから返されるノードは親ノードを持ちます。</span><span class="sxs-lookup"><span data-stu-id="5359d-551">This means that the node that is returned by the Info.getNode method will not have a parent node, whereas the one returned by the findNode method will have a parent node.</span></span>

### <a name="examples---findnode"></a><span data-ttu-id="5359d-552">例 - findNode</span><span class="sxs-lookup"><span data-stu-id="5359d-552">Examples - findNode</span></span>

<span data-ttu-id="5359d-553">次の例では、TreeNode::findNode メソッドが呼び出される時に検出される ツリー ノードの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="5359d-553">The following example retrieves the name of the tree node that is found the TreeNode::findNode method is called.</span></span> <span data-ttu-id="5359d-554">この例では、TreeNode.findNode メソッドを呼び出す前に、ユーザーに必要なセキュリティ キーがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5359d-554">This example checks whether the user has the required security key before it calls the TreeNode.findNode method.</span></span>

```xpp
server static public void Main(Args _args) 
{ 
    TreeNode tn; 
    str name; 
    tn = TreeNode::findNode(@"\Classes"); 
    if (tn) 
    { 
        name = tn.treeNodeName(); 
    } 
}
```

## <a name="method-generateobjectname"></a><span data-ttu-id="5359d-555">メソッド generateObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-555">Method generateObjectName</span></span>

```xpp
public static str generateObjectName(str template)
```

### <a name="parameters---generateobjectname"></a><span data-ttu-id="5359d-556">パラメーター - generateObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-556">Parameters - generateObjectName</span></span>

<span data-ttu-id="5359d-557">テンプレート</span><span class="sxs-lookup"><span data-stu-id="5359d-557">template</span></span>  

### <a name="return-value---generateobjectname"></a><span data-ttu-id="5359d-558">戻り値 - generateObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-558">Return Value - generateObjectName</span></span>

## <a name="method-getmaximumnodenamelength"></a><span data-ttu-id="5359d-559">メソッド getMaximumNodeNameLength</span><span class="sxs-lookup"><span data-stu-id="5359d-559">Method getMaximumNodeNameLength</span></span>

```xpp
public static int getMaximumNodeNameLength(int modelElementTypeId)
```

### <a name="parameters---getmaximumnodenamelength"></a><span data-ttu-id="5359d-560">パラメーター - getMaximumNodeNameLength</span><span class="sxs-lookup"><span data-stu-id="5359d-560">Parameters - getMaximumNodeNameLength</span></span>

<span data-ttu-id="5359d-561">modelElementTypeId</span><span class="sxs-lookup"><span data-stu-id="5359d-561">modelElementTypeId</span></span>  

### <a name="return-value---getmaximumnodenamelength"></a><span data-ttu-id="5359d-562">戻り値 - getMaximumNodeNameLength</span><span class="sxs-lookup"><span data-stu-id="5359d-562">Return Value - getMaximumNodeNameLength</span></span>

## <a name="method-isnodereferencevalid"></a><span data-ttu-id="5359d-563">メソッド isNodeReferenceValid</span><span class="sxs-lookup"><span data-stu-id="5359d-563">Method isNodeReferenceValid</span></span>

```xpp
public static boolean isNodeReferenceValid(TreeNode treeNode)
```

### <a name="parameters---isnodereferencevalid"></a><span data-ttu-id="5359d-564">パラメーター - isNodeReferenceValid</span><span class="sxs-lookup"><span data-stu-id="5359d-564">Parameters - isNodeReferenceValid</span></span>

<span data-ttu-id="5359d-565">treeNode</span><span class="sxs-lookup"><span data-stu-id="5359d-565">treeNode</span></span>  

### <a name="return-value---isnodereferencevalid"></a><span data-ttu-id="5359d-566">戻り値 - isNodeReferenceValid</span><span class="sxs-lookup"><span data-stu-id="5359d-566">Return Value - isNodeReferenceValid</span></span>

## <a name="method-isvalidobjectname"></a><span data-ttu-id="5359d-567">メソッド isValidObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-567">Method isValidObjectName</span></span>

<span data-ttu-id="5359d-568">引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5359d-568">Determines whether the string passed as an argument can be used as a name for a node in the Application Object Tree (AOT).</span></span>

```xpp
public static boolean isValidObjectName(str name)
```

### <a name="parameters---isvalidobjectname"></a><span data-ttu-id="5359d-569">パラメーター - isValidObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-569">Parameters - isValidObjectName</span></span>

<span data-ttu-id="5359d-570">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-570">name</span></span>  
<span data-ttu-id="5359d-571">検証するツリー ノードの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5359d-571">The string that contains the tree node name to validate.</span></span>

### <a name="return-value---isvalidobjectname"></a><span data-ttu-id="5359d-572">戻り値 - isValidObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-572">Return Value - isValidObjectName</span></span>

<span data-ttu-id="5359d-573">各条件が一致している場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5359d-573">true if each condition is met; otherwise false.</span></span>

### <a name="remarks---isvalidobjectname"></a><span data-ttu-id="5359d-574">備考 - isValidObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-574">Remarks - isValidObjectName</span></span>

<span data-ttu-id="5359d-575">候補者の名前は、次の条件を満たす必要があります:</span><span class="sxs-lookup"><span data-stu-id="5359d-575">A candidate name must meet the following conditions:</span></span>

-   <span data-ttu-id="5359d-576">最初の文字は数字、記号ではない文字でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5359d-576">The first character must be a letter.</span></span>
-   <span data-ttu-id="5359d-577">文字、数字、またはアンダースコアだけを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5359d-577">It can only contain letters, numbers or an underscore.</span></span>
-   <span data-ttu-id="5359d-578">トークンに対して評価してはなりません。</span><span class="sxs-lookup"><span data-stu-id="5359d-578">It must not evaluate to a token.</span></span>

<span data-ttu-id="5359d-579">このメソッドは、同じ名前の要素がすでに存在するかどうかをチェックしません。</span><span class="sxs-lookup"><span data-stu-id="5359d-579">This method does not check if an element of the same name already exists.</span></span> <span data-ttu-id="5359d-580">これは引数が AOT オブジェクトの有効な名前であることのみを検証します。</span><span class="sxs-lookup"><span data-stu-id="5359d-580">It only validates that the argument is a valid name for an AOT object.</span></span> <span data-ttu-id="5359d-581">重複する名前は、クラス、テーブル、拡張データ型または列挙内では存在しません。</span><span class="sxs-lookup"><span data-stu-id="5359d-581">Duplicate names may not exist within classes, tables, extended data types, or enums.</span></span>

### <a name="examples---isvalidobjectname"></a><span data-ttu-id="5359d-582">例 - isValidObjectName</span><span class="sxs-lookup"><span data-stu-id="5359d-582">Examples - isValidObjectName</span></span>

<span data-ttu-id="5359d-583">次の例では、有効な引数と無効な引数の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="5359d-583">The following example gives examples of valid and invalid arguments.</span></span>

```xpp
boolean validName; 
validName = TreeNode::isValidObjectName('ValidName'); //true 
validName = TreeNode::isValidObjectName('Name with spaces'); //false 
validName = TreeNode::isValidObjectName('4StartsWithDigit'); //false 
validName = TreeNode::isValidObjectName('Illegal;Character'); //false 
validName = TreeNode::isValidObjectName('if'); // false (token name)
```

## <a name="method-rootnode"></a><span data-ttu-id="5359d-584">メソッド rootNode</span><span class="sxs-lookup"><span data-stu-id="5359d-584">Method rootNode</span></span>

<span data-ttu-id="5359d-585">AOT のルート ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="5359d-585">Returns the root node of the AOT.</span></span>

```xpp
public static TreeNode rootNode()
```

### <a name="return-value---rootnode"></a><span data-ttu-id="5359d-586">戻り値 - rootNode</span><span class="sxs-lookup"><span data-stu-id="5359d-586">Return Value - rootNode</span></span>

<span data-ttu-id="5359d-587">AOT のルート ノード。</span><span class="sxs-lookup"><span data-stu-id="5359d-587">The root node of the AOT.</span></span>

### <a name="remarks---rootnode"></a><span data-ttu-id="5359d-588">備考 - rootNode</span><span class="sxs-lookup"><span data-stu-id="5359d-588">Remarks - rootNode</span></span>

<span data-ttu-id="5359d-589">このメソッドは、同様の機能を rootNode メソッドに提供します。</span><span class="sxs-lookup"><span data-stu-id="5359d-589">The method provides similar functionality to the rootNode method.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-590">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-590">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute()
```

## <a name="method-treenoderelease"></a><span data-ttu-id="5359d-591">メソッド treeNodeRelease</span><span class="sxs-lookup"><span data-stu-id="5359d-591">Method treeNodeRelease</span></span>

<span data-ttu-id="5359d-592">ツリー ノードが明示的に解放されます。</span><span class="sxs-lookup"><span data-stu-id="5359d-592">Releases the tree node explicitly.</span></span>

```xpp
public void treeNodeRelease()
```

### <a name="remarks---treenoderelease"></a><span data-ttu-id="5359d-593">備考 - treeNodeRelease</span><span class="sxs-lookup"><span data-stu-id="5359d-593">Remarks - treeNodeRelease</span></span>

<span data-ttu-id="5359d-594">ガベージコレクターが自動的にオブジェクトをアンロードするので、通常、オブジェクトを明示的にアンロードする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5359d-594">Usually you do not have to explicitly unload objects, because the garbage collector will do it automatically.</span></span> <span data-ttu-id="5359d-595">ただし、ツリー ノードは、通常 AOT にリンクされているため、ガベージ コレクションではありません。</span><span class="sxs-lookup"><span data-stu-id="5359d-595">However, because tree nodes are ordinarily linked to the AOT, they are not garbage-collected.</span></span> <span data-ttu-id="5359d-596">同じ方法で多くのツリー ノードでこのメソッドを実行する場合、リソースを要求する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5359d-596">If you run this method on many tree nodes in the same execution, it can be demanding on resources.</span></span> <span data-ttu-id="5359d-597">ガベージ コレクターがツリー ノードを削除できるようにするには、作業中にツリー ノードをアンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5359d-597">You should unload the tree nodes as you go along to give the garbage collector a chance to remove them.</span></span> <span data-ttu-id="5359d-598">このメソッドを呼び出す前に、そのツリー ノードとそのサブノードに対するすべての参照を削除してください。</span><span class="sxs-lookup"><span data-stu-id="5359d-598">Make sure to remove all references to the tree node and its subnodes before you call this method.</span></span> <span data-ttu-id="5359d-599">このメソッドを呼び出す必要があるかどうかを判断するには、TreeNode.TreeNodeType().isConsumingMemory メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5359d-599">Use the TreeNode.TreeNodeType().isConsumingMemory method to determine if you need to call this method.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-600">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-600">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, [XRefReference xrefRef], [ClassId parentTypeId])
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-601">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-601">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-602">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-602">name</span></span>  

<!-- -->

<span data-ttu-id="5359d-603">xrefKind</span><span class="sxs-lookup"><span data-stu-id="5359d-603">xrefKind</span></span>  

<!-- -->

<span data-ttu-id="5359d-604">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5359d-604">lineNumber</span></span>  

<!-- -->

<span data-ttu-id="5359d-605">columNumber</span><span class="sxs-lookup"><span data-stu-id="5359d-605">columNumber</span></span>  

<!-- -->

<span data-ttu-id="5359d-606">xrefRef</span><span class="sxs-lookup"><span data-stu-id="5359d-606">xrefRef</span></span>  

<!-- -->

<span data-ttu-id="5359d-607">parentTypeId</span><span class="sxs-lookup"><span data-stu-id="5359d-607">parentTypeId</span></span>  

## <a name="method-aotrun"></a><span data-ttu-id="5359d-608">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="5359d-608">Method AOTrun</span></span>

<span data-ttu-id="5359d-609">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="5359d-609">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>

```xpp
public void AOTrun()
```

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-610">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-610">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute()
```

## <a name="method-aotrefresh"></a><span data-ttu-id="5359d-611">メソッド AOTrefresh</span><span class="sxs-lookup"><span data-stu-id="5359d-611">Method AOTrefresh</span></span>

<span data-ttu-id="5359d-612">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="5359d-612">Refreshes the node with the latest changes to the .aod file.</span></span>

```xpp
public void AOTrefresh()
```

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-613">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-613">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute(Struct struct1)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-614">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-614">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-615">struct1</span><span class="sxs-lookup"><span data-stu-id="5359d-615">struct1</span></span>  

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-616">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-616">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute(str properties)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-617">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-617">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-618">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5359d-618">properties</span></span>  

## <a name="method-aotconfigure"></a><span data-ttu-id="5359d-619">メソッド AOTconfigure</span><span class="sxs-lookup"><span data-stu-id="5359d-619">Method AOTconfigure</span></span>

```xpp
public void AOTconfigure()
```

## <a name="method-aotload"></a><span data-ttu-id="5359d-620">メソッド AOTload</span><span class="sxs-lookup"><span data-stu-id="5359d-620">Method AOTload</span></span>

<span data-ttu-id="5359d-621">オブジェクトが読み込み済みであるか確認します。</span><span class="sxs-lookup"><span data-stu-id="5359d-621">Ensures that the object is loaded.</span></span>

```xpp
public void AOTload()
```

## <a name="method-treenodeexport"></a><span data-ttu-id="5359d-622">メソッド treeNodeExport</span><span class="sxs-lookup"><span data-stu-id="5359d-622">Method treeNodeExport</span></span>

<span data-ttu-id="5359d-623">アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="5359d-623">Exports this node and its subtree from the Application Object Tree (AOT).</span></span>

```xpp
public void treeNodeExport(str filename, [int flag])
```

### <a name="parameters---treenodeexport"></a><span data-ttu-id="5359d-624">パラメーター - treeNodeExport</span><span class="sxs-lookup"><span data-stu-id="5359d-624">Parameters - treeNodeExport</span></span>

<span data-ttu-id="5359d-625">filename</span><span class="sxs-lookup"><span data-stu-id="5359d-625">filename</span></span>  

<!-- -->

<span data-ttu-id="5359d-626">flag</span><span class="sxs-lookup"><span data-stu-id="5359d-626">flag</span></span>  

### <a name="remarks---treenodeexport"></a><span data-ttu-id="5359d-627">備考 - treeNodeExport</span><span class="sxs-lookup"><span data-stu-id="5359d-627">Remarks - treeNodeExport</span></span>

<span data-ttu-id="5359d-628">攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="5359d-628">If an attacker can control input to this method, a security risk exists.</span></span> <span data-ttu-id="5359d-629">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="5359d-629">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="5359d-630">サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="5359d-630">Calls to this method on the server require permission from the .</span></span> <span data-ttu-id="5359d-631">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5359d-631">Ensure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---treenodeexport"></a><span data-ttu-id="5359d-632">例 - treeNodeExport</span><span class="sxs-lookup"><span data-stu-id="5359d-632">Examples - treeNodeExport</span></span>

<span data-ttu-id="5359d-633">この例では、treeNodeExport メソッドを使用して、ExampleClass クラスを .xpo ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="5359d-633">This example uses the treeNodeExport method to export the ExampleClass class to an .xpo file.</span></span>

```xpp
void TreeNodeExample() 
{ 
    TreeNode treeNode; 
    TreeNode childNode; 
    FileIoPermission perm; 
    #define.ExportFile(@"c:\TreeNodeExportExampleClass.xpo") 
    #define.ExportMode("w") 
    perm = new FileIoPermission(#ExportFile, #ExportMode); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
    treeNode = TreeNode::findNode(@"\Classes"); 
    if (treeNode != null) 
    { 
        childNode = treeNode.AOTfindChild(@"ExampleClass"); 
        // BP deviation documented. 
        childNode.treeNodeExport(#ExportFile); 
    } 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-634">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-634">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute(str source, [boolean isStatic])
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-635">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-635">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-636">ソース</span><span class="sxs-lookup"><span data-stu-id="5359d-636">source</span></span>  

<!-- -->

<span data-ttu-id="5359d-637">isStatic</span><span class="sxs-lookup"><span data-stu-id="5359d-637">isStatic</span></span>  

## <a name="method-aotendxref"></a><span data-ttu-id="5359d-638">メソッド AOTendXref</span><span class="sxs-lookup"><span data-stu-id="5359d-638">Method AOTendXref</span></span>

```xpp
public void AOTendXref()
```

## <a name="method-aotmessageline"></a><span data-ttu-id="5359d-639">メソッド AOTmessageLine</span><span class="sxs-lookup"><span data-stu-id="5359d-639">Method AOTmessageLine</span></span>

<span data-ttu-id="5359d-640">アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。</span><span class="sxs-lookup"><span data-stu-id="5359d-640">Writes text to the Application Object Tree (AOT) Message window.</span></span>

```xpp
public void AOTmessageLine(str text, int linenumber)
```

### <a name="parameters---aotmessageline"></a><span data-ttu-id="5359d-641">パラメーター - AOTmessageLine</span><span class="sxs-lookup"><span data-stu-id="5359d-641">Parameters - AOTmessageLine</span></span>

<span data-ttu-id="5359d-642">テキスト</span><span class="sxs-lookup"><span data-stu-id="5359d-642">text</span></span>  
<span data-ttu-id="5359d-643">無視される整数。</span><span class="sxs-lookup"><span data-stu-id="5359d-643">An integer that is ignored.</span></span> <span data-ttu-id="5359d-644">出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。</span><span class="sxs-lookup"><span data-stu-id="5359d-644">It does not currently direct the written text to a specific line number in the output Message window.</span></span>

<!-- -->

<span data-ttu-id="5359d-645">linenumber</span><span class="sxs-lookup"><span data-stu-id="5359d-645">linenumber</span></span>  
<span data-ttu-id="5359d-646">無視される整数。</span><span class="sxs-lookup"><span data-stu-id="5359d-646">An integer that is ignored.</span></span> <span data-ttu-id="5359d-647">出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。</span><span class="sxs-lookup"><span data-stu-id="5359d-647">It does not currently direct the written text to a specific line number in the output Message window.</span></span>

### <a name="remarks---aotmessageline"></a><span data-ttu-id="5359d-648">備考 - AOTmessageLine</span><span class="sxs-lookup"><span data-stu-id="5359d-648">Remarks - AOTmessageLine</span></span>

<span data-ttu-id="5359d-649">このメソッドは、テキストを出力するために使用されます。そのためユーザーは後でメッセージ ウィンドウ内のそのテキスト行をダブルクリックすると、このノードに関して何らかのアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="5359d-649">This method is intended to be used to output text so that when the user later double-clicks that line of text in the message window, some action will happen regarding this node.</span></span>

### <a name="examples---aotmessageline"></a><span data-ttu-id="5359d-650">例 - AOTmessageLine</span><span class="sxs-lookup"><span data-stu-id="5359d-650">Examples - AOTmessageLine</span></span>

<span data-ttu-id="5359d-651">次の例では、フォームが TreeNode からこのメソッドを継承するために、フォーム オブジェクトに対して AOTmessageLine メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5359d-651">The following example executes the AOTmessageLine method on a Form object, because Form inherits this method from TreeNode.</span></span>

```xpp
static void JobAOTmessageLineDemo(Args _args) 
{ 
    Form f = new Form('testAOTMessageLine'); 
    // 
    f.AOTmessageLine('test message 1a',1); 
    f.AOTmessageLine('test message 2a',2); 
    f.AOTmessageLine('test message 3a',3); 
    f.AOTmessageLine('test message 1b',1); 
    f.AOTmessageLine('test message 2b',2); 
    f.AOTmessageLine('test message 3b',3); 
    f.AOTmessageLine('test message 2c',2); 
    // 
    /******* 
    Actual Output in the Message window 
    (the 7 identical lines): 
    test message 2c 
    test message 2c 
    test message 2c 
    test message 2c 
    test message 2c 
    test message 2c 
    test message 2c 
    *******/ 
}
```

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-652">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-652">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute(str name, AnyType value)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-653">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-653">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-654">名前</span><span class="sxs-lookup"><span data-stu-id="5359d-654">name</span></span>  

<!-- -->

<span data-ttu-id="5359d-655">値</span><span class="sxs-lookup"><span data-stu-id="5359d-655">value</span></span>  

## <a name="method-aotrestore"></a><span data-ttu-id="5359d-656">メソッド AOTrestore</span><span class="sxs-lookup"><span data-stu-id="5359d-656">Method AOTrestore</span></span>

<span data-ttu-id="5359d-657">該当する場合は、ディスクからこのノードを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="5359d-657">Reloads this node from the disk, if applicable.</span></span>

```xpp
public void AOTrestore([boolean forceReload])
```

### <a name="parameters---aotrestore"></a><span data-ttu-id="5359d-658">パラメーター - AOTrestore</span><span class="sxs-lookup"><span data-stu-id="5359d-658">Parameters - AOTrestore</span></span>

<span data-ttu-id="5359d-659">forceReload</span><span class="sxs-lookup"><span data-stu-id="5359d-659">forceReload</span></span>  

## <a name="method-aotregenerate"></a><span data-ttu-id="5359d-660">メソッド AOTregenerate</span><span class="sxs-lookup"><span data-stu-id="5359d-660">Method AOTregenerate</span></span>

```xpp
public void AOTregenerate()
```

## <a name="method-aotmakexref"></a><span data-ttu-id="5359d-661">メソッド AOTmakeXref</span><span class="sxs-lookup"><span data-stu-id="5359d-661">Method AOTmakeXref</span></span>

<span data-ttu-id="5359d-662">このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。</span><span class="sxs-lookup"><span data-stu-id="5359d-662">Compiles this node and its subtree in the AOT, updating the cross-reference system.</span></span>

```xpp
public void AOTmakeXref([int flag], [boolean xRefAll])
```

### <a name="parameters---aotmakexref"></a><span data-ttu-id="5359d-663">パラメーター - AOTmakeXref</span><span class="sxs-lookup"><span data-stu-id="5359d-663">Parameters - AOTmakeXref</span></span>

<span data-ttu-id="5359d-664">flag</span><span class="sxs-lookup"><span data-stu-id="5359d-664">flag</span></span>  

<!-- -->

<span data-ttu-id="5359d-665">xRefAll</span><span class="sxs-lookup"><span data-stu-id="5359d-665">xRefAll</span></span>  

### <a name="remarks---aotmakexref"></a><span data-ttu-id="5359d-666">備考 - AOTmakeXref</span><span class="sxs-lookup"><span data-stu-id="5359d-666">Remarks - AOTmakeXref</span></span>

<span data-ttu-id="5359d-667">このメソッドは、任意の場所で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5359d-667">This method can be called at any:</span></span>

-   <span data-ttu-id="5359d-668">リスト ノード (AOT、テーブル、フォーム、プロジェクトのルート、およびグループ)</span><span class="sxs-lookup"><span data-stu-id="5359d-668">list node (such as AOT, Tables, Forms, Project roots, and groups)</span></span>
-   <span data-ttu-id="5359d-669">アプリケーション オブジェクト (テーブルやフォームなど)</span><span class="sxs-lookup"><span data-stu-id="5359d-669">Application Object (such as a Table or Form)</span></span>
-   <span data-ttu-id="5359d-670">メソッドの分岐</span><span class="sxs-lookup"><span data-stu-id="5359d-670">methods branch</span></span>
-   <span data-ttu-id="5359d-671">メソッド</span><span class="sxs-lookup"><span data-stu-id="5359d-671">method</span></span>

## <a name="method-aotedit"></a><span data-ttu-id="5359d-672">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="5359d-672">Method AOTedit</span></span>

<span data-ttu-id="5359d-673">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="5359d-673">Opens the appropriate editor for this node.</span></span>

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a><span data-ttu-id="5359d-674">パラメーター - AOTedit</span><span class="sxs-lookup"><span data-stu-id="5359d-674">Parameters - AOTedit</span></span>

<span data-ttu-id="5359d-675">折れ線</span><span class="sxs-lookup"><span data-stu-id="5359d-675">Line</span></span>  
<span data-ttu-id="5359d-676">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5359d-676">The column of the cursor position; optional.</span></span>

<!-- -->

<span data-ttu-id="5359d-677">円柱</span><span class="sxs-lookup"><span data-stu-id="5359d-677">Column</span></span>  
<span data-ttu-id="5359d-678">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5359d-678">The column of the cursor position; optional.</span></span>

### <a name="remarks---aotedit"></a><span data-ttu-id="5359d-679">備考 - AOTedit</span><span class="sxs-lookup"><span data-stu-id="5359d-679">Remarks - AOTedit</span></span>

<span data-ttu-id="5359d-680">ノードがメソッドである場合は、コード エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="5359d-680">If the node is a method, the code editor will open.</span></span> <span data-ttu-id="5359d-681">ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="5359d-681">If the node is a documentation object, the Help editor will open.</span></span>

### <a name="examples---aotedit"></a><span data-ttu-id="5359d-682">例 - AOTedit</span><span class="sxs-lookup"><span data-stu-id="5359d-682">Examples - AOTedit</span></span>

<span data-ttu-id="5359d-683">次のコード例は、X++ エディターを開き、クラス Tax のクラス宣言を表示し、ポインタを 6 行目、8 列目に配置します。</span><span class="sxs-lookup"><span data-stu-id="5359d-683">The following code example opens the X++ editor, shows the class declaration of the class Tax, and positions the pointer at line 6, column 8.</span></span>

```xpp
AOT 
static void myJobAOTEdit(Args _args) 
{ 
    treeNode treeNode; 
    treeNode = TreeNode::findNode(#ClassesPath + '\\' + classStr(Tax)+ '\\ClassDeclaration'); 
    if (treeNode) 
    { 
        treeNode.AOTedit(6,8); 
    } 
    else 
    { 
        print "Could not find treeNode"; 
    } 
    pause; 
}
```

## <a name="method-aotshowproperties"></a><span data-ttu-id="5359d-684">メソッド AOTshowProperties</span><span class="sxs-lookup"><span data-stu-id="5359d-684">Method AOTshowProperties</span></span>

<span data-ttu-id="5359d-685">プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="5359d-685">Opens the property sheet (if not already open) and shows the properties for this node.</span></span>

```xpp
public void AOTshowProperties()
```

## <a name="method-aotinsert"></a><span data-ttu-id="5359d-686">メソッド AOTinsert</span><span class="sxs-lookup"><span data-stu-id="5359d-686">Method AOTinsert</span></span>

<span data-ttu-id="5359d-687">このノードのサブノード間にノードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="5359d-687">Inserts a node among the subnodes of this node.</span></span>

```xpp
public void AOTinsert(TreeNode parent, [TreeNode after], [boolean doNotDuplicate])
```

### <a name="parameters---aotinsert"></a><span data-ttu-id="5359d-688">パラメーター - AOTinsert</span><span class="sxs-lookup"><span data-stu-id="5359d-688">Parameters - AOTinsert</span></span>

<span data-ttu-id="5359d-689">parent</span><span class="sxs-lookup"><span data-stu-id="5359d-689">parent</span></span>  

<!-- -->

<span data-ttu-id="5359d-690">以後</span><span class="sxs-lookup"><span data-stu-id="5359d-690">after</span></span>  

<!-- -->

<span data-ttu-id="5359d-691">doNotDuplicate</span><span class="sxs-lookup"><span data-stu-id="5359d-691">doNotDuplicate</span></span>  

## <a name="method-new"></a><span data-ttu-id="5359d-692">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5359d-692">Method new</span></span>

<span data-ttu-id="5359d-693">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5359d-693">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new()
```

## <a name="method-aotmove"></a><span data-ttu-id="5359d-694">メソッド AOTMove</span><span class="sxs-lookup"><span data-stu-id="5359d-694">Method AOTMove</span></span>

```xpp
public void AOTMove(TreeNode parent, [TreeNode after])
```

### <a name="parameters---aotmove"></a><span data-ttu-id="5359d-695">パラメーター - AOTMove</span><span class="sxs-lookup"><span data-stu-id="5359d-695">Parameters - AOTMove</span></span>

<span data-ttu-id="5359d-696">parent</span><span class="sxs-lookup"><span data-stu-id="5359d-696">parent</span></span>  

<!-- -->

<span data-ttu-id="5359d-697">以後</span><span class="sxs-lookup"><span data-stu-id="5359d-697">after</span></span>  

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5359d-698">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-698">Method SysObsoleteAttribute</span></span>

```xpp
public void SysObsoleteAttribute(int modelId)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5359d-699">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5359d-699">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5359d-700">modelId</span><span class="sxs-lookup"><span data-stu-id="5359d-700">modelId</span></span>  

