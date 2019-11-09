---
title: ツリー コントロールでのチェック ボックスのサポート
description: この記事は、ツリー コントロールのチェック ボックス コントロールを使用するための入門書として作成されています。 ツリー コントロールを使用するための一般的な「方法」ではありません。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 31501
ms.assetid: 57c0fa59-ef48-4913-9f92-407ff2566c72
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1ffb940a27f055eb42d7975b9fafc25f1b3fb3c
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578298"
---
# <a name="check-box-support-in-tree-controls"></a><span data-ttu-id="58c82-104">ツリー コントロールでのチェック ボックスのサポート</span><span class="sxs-lookup"><span data-stu-id="58c82-104">Check box support in tree controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58c82-105">この記事は、ツリー コントロールのチェック ボックス コントロールを使用するための入門書として作成されています。</span><span class="sxs-lookup"><span data-stu-id="58c82-105">This article is intended as a primer for using check box controls in the tree control.</span></span> <span data-ttu-id="58c82-106">ツリー コントロールを使用するための一般的な「方法」ではありません。</span><span class="sxs-lookup"><span data-stu-id="58c82-106">It's not a general “how to” for using tree controls.</span></span>

<span data-ttu-id="58c82-107">Microsoft Dynamics AX 2012 には、データをツリー階層で表示し、ユーザーがチェック ボックスを使用して 1 つまたは複数のノードを選択できるようにするために強化されたツリー コントロールの例がいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="58c82-107">Microsoft Dynamics AX 2012 includes several examples of tree controls that were enhanced so that they both show data in a tree hierarchy and let the user select one or more nodes by using check boxes.</span></span> <span data-ttu-id="58c82-108">Dynamics AX 2012 では、ツリー コントロールには、チェック ボックスのコントロールに対して、組み込みのサポートがありませんでした。</span><span class="sxs-lookup"><span data-stu-id="58c82-108">In Dynamics AX 2012, the tree control had no built-in support for check box controls.</span></span> <span data-ttu-id="58c82-109">代わりに、チェック ボックスのイメージがツリー コントロール内の各ノードに対して追加されました。</span><span class="sxs-lookup"><span data-stu-id="58c82-109">Instead, an image of a check box was added for each node in the tree control.</span></span> <span data-ttu-id="58c82-110">ユーザーがチェックボックスをクリックすると、各ノードのイメージの状態が切り替わりました。</span><span class="sxs-lookup"><span data-stu-id="58c82-110">The image state for each node was then toggled as the user clicked the check box.</span></span> 

![以前のバージョンでのツリー コントロールのスクリーン ショット](./media/treecontrol_legacycheckbox.png) 

<span data-ttu-id="58c82-112">現在のバージョンでは、開発者の経験が大幅に簡素化されています。</span><span class="sxs-lookup"><span data-stu-id="58c82-112">The current version has greatly simplified the experience for the developer.</span></span> <span data-ttu-id="58c82-113">チェック ボックスのサポートがツリー コントロールに組み込まれました。</span><span class="sxs-lookup"><span data-stu-id="58c82-113">Check box support is now built into the tree control.</span></span> 

![現在のバージョンでのツリー コントロールのスクリーン ショット](./media/treecontrol_ax7checkbox.png) 

<span data-ttu-id="58c82-115">チェック ボックスを含めるイメージを使用する必要がなくなり、選択されている場合にチェック ボックスの状態を明示的に設定する必要もありません。</span><span class="sxs-lookup"><span data-stu-id="58c82-115">You no longer have to use images to include a check box, and you also don't have to explicitly set the state of the check box state when it's selected.</span></span> <span data-ttu-id="58c82-116">コントロールは画像を使用せず、チェック ボックスの状態は、トライステートのチェック ボックスで期待どおりに管理されます。</span><span class="sxs-lookup"><span data-stu-id="58c82-116">The control doesn’t use images, and the check box state is managed in the way that you would expect for a tri-state check box.</span></span> <span data-ttu-id="58c82-117">状態チェック ボックスの例では、ほとんどのインストール シナリオで検出が可能です。</span><span class="sxs-lookup"><span data-stu-id="58c82-117">Examples of tri-state check boxes can be found in most installation scenarios.</span></span> <span data-ttu-id="58c82-118">状態チェック ボックスが使用されているとき、ユーザーが親ノードを選択すると、その親のすべての子も選択されます。</span><span class="sxs-lookup"><span data-stu-id="58c82-118">When tri-state check boxes are used, if the user selects a parent node, all children of that parent also become selected.</span></span> <span data-ttu-id="58c82-119">チェックボックスの操作は、ノードの展開/折りたたみ機能とは独立しています。</span><span class="sxs-lookup"><span data-stu-id="58c82-119">The check box interaction is independent of the node's expand/collapse functionality.</span></span> <span data-ttu-id="58c82-120">親ノードが折りたたまれているのとき (子が非表示のとき)、親ノードに付いているチェック マークは、すべての子も選択されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="58c82-120">When the parent node is collapsed (no children are visible), a check mark on the parent node indicates that all children are also selected.</span></span> <span data-ttu-id="58c82-121">ただし、複数の子を持つ親の 1 つの子が選択されない場合、親ノードの外観が変化します。</span><span class="sxs-lookup"><span data-stu-id="58c82-121">However, if one child of a parent that has multiple children isn't selected, the appearance of the parent node changes.</span></span> <span data-ttu-id="58c82-122">チェックボックスにチェックマークは含まれなくなりましたが、記入されています。</span><span class="sxs-lookup"><span data-stu-id="58c82-122">The check box no longer contains a check mark but is filled in.</span></span> <span data-ttu-id="58c82-123">この状態は、部分チェックと見なされます。</span><span class="sxs-lookup"><span data-stu-id="58c82-123">This state is considered a partial check.</span></span> <span data-ttu-id="58c82-124">したがって、親ノードには 3 つの状態があります。</span><span class="sxs-lookup"><span data-stu-id="58c82-124">Therefore, a parent node has three states:</span></span>

-   <span data-ttu-id="58c82-125">確認済</span><span class="sxs-lookup"><span data-stu-id="58c82-125">Checked</span></span>
-   <span data-ttu-id="58c82-126">未チェック</span><span class="sxs-lookup"><span data-stu-id="58c82-126">Unchecked</span></span>
-   <span data-ttu-id="58c82-127">部分的</span><span class="sxs-lookup"><span data-stu-id="58c82-127">Partial</span></span>

<span data-ttu-id="58c82-128">ユーザーが部分的状態にある親ノードのチェック ボックスをクリックすると、親とそのすべての子の状態はチェックされた状態に変更されます。</span><span class="sxs-lookup"><span data-stu-id="58c82-128">If the user clicks the check box on a parent node that is in a partial state, the state of the parent and all its children changes to checked.</span></span> <span data-ttu-id="58c82-129">(親ノードおよびそのすべての子ノードが選択されるようになります。)</span><span class="sxs-lookup"><span data-stu-id="58c82-129">(The parent node and all its child nodes are now selected.)</span></span> 

<span data-ttu-id="58c82-130">**部分的状態にある親ノード**</span><span class="sxs-lookup"><span data-stu-id="58c82-130">**Parent node in a partial state**</span></span> 

![部分的状態にある親ノードの例](./media/treecontrol_partialparent.png) 

<span data-ttu-id="58c82-132">**親ノードが選択された後、チェックされた状態の親ノードおよびすべての子ノード**</span><span class="sxs-lookup"><span data-stu-id="58c82-132">**Parent node and all child nodes in a checked state after the parent node is selected**</span></span>

![チェックされた状態にある親ノードと子ノードの例](./media/treecontrol_parent.png) 

<span data-ttu-id="58c82-134">ユーザーがチェックされた状態にある親ノードのチェック ボックスをクリックすると、親とそのすべての子の状態は未チェックの状態に変更されます。</span><span class="sxs-lookup"><span data-stu-id="58c82-134">If the user clicks the check box on a parent node that is in a checked state, the state of the parent and all its children changes to unchecked.</span></span> <span data-ttu-id="58c82-135">(親ノードおよびそのすべての子ノードが消去されるようになります。)</span><span class="sxs-lookup"><span data-stu-id="58c82-135">(The parent node and all its child nodes are now cleared.)</span></span> 

<span data-ttu-id="58c82-136">**チェックされた状態にある親ノード**</span><span class="sxs-lookup"><span data-stu-id="58c82-136">**Parent node in a checked state**</span></span> 

![チェックされた状態にある親ノードの例](./media/treecontrol_parent.png)

<span data-ttu-id="58c82-138">**親ノードがクリアされた後、チェックされていない状態の親ノードおよびすべての子ノード**</span><span class="sxs-lookup"><span data-stu-id="58c82-138">**Parent node and all child nodes in an unchecked state after the parent node is cleared**</span></span> 

![未チェック状態にある親ノードと子ノードの例](./media/treecontrol_noparent1.png) 

<span data-ttu-id="58c82-140">ユーザーが未チェック状態にある親ノードのチェック ボックスをクリックすると、親とそのすべての子の状態はチェックされた状態に変更されます。</span><span class="sxs-lookup"><span data-stu-id="58c82-140">If the user clicks the check box on a parent node that is in an unchecked state, the state of the parent and all its children changes to checked.</span></span> <span data-ttu-id="58c82-141">(親ノードおよびそのすべての子ノードが選択されるようになります。)</span><span class="sxs-lookup"><span data-stu-id="58c82-141">(The parent node and all its child nodes are now selected.)</span></span> 

<span data-ttu-id="58c82-142">**未チェック状態にある親ノード**</span><span class="sxs-lookup"><span data-stu-id="58c82-142">**Parent node in an unchecked state**</span></span> 

![未チェック状態にある親ノードの例](./media/treecontrol_noparent1.png) 

<span data-ttu-id="58c82-144">**親ノードが選択された後、チェックされた状態の親ノードおよびすべての子ノード**</span><span class="sxs-lookup"><span data-stu-id="58c82-144">**Parent node and all child nodes in a checked state after the parent node is selected**</span></span> 

![チェックされた状態にある親ノードと子ノードの例](./media/treecontrol_parent.png) 

<span data-ttu-id="58c82-146">子を持たない子ノード (つまり、それ自体が親ではない子ノード) には、2 つの状態: チェックされているか未チェックかしかありません。</span><span class="sxs-lookup"><span data-stu-id="58c82-146">A child node that has no children (in other words, a child node that isn't a parent itself) has only two states: checked and unchecked.</span></span> <span data-ttu-id="58c82-147">チェックされた状態の唯一の子である子ノードは、その親の状態に影響します。</span><span class="sxs-lookup"><span data-stu-id="58c82-147">A child node that is the only child in a checked state affects the state of its parent.</span></span> <span data-ttu-id="58c82-148">子ノードが選択されている場合、その親の状態は部分的な状態に変更されます。</span><span class="sxs-lookup"><span data-stu-id="58c82-148">If a child node is selected, the state of its parent changes to partial.</span></span> <span data-ttu-id="58c82-149">**注記:** ツリー内の 1 つのノードにも、現在のノードであることを示す「選択」状態があります。</span><span class="sxs-lookup"><span data-stu-id="58c82-149">**Note:** A single node in a tree also has a “selected” state to indicate that it's the current node.</span></span> <span data-ttu-id="58c82-150">この状態は、チェックされた状態とは異なります。</span><span class="sxs-lookup"><span data-stu-id="58c82-150">This state differs from the checked state.</span></span>

## <a name="tree-controls-that-contain-check-boxes-in-dynamics-ax-2012"></a><span data-ttu-id="58c82-151">Dynamics AX 2012 のチェック ボックスを含むツリー コントロール</span><span class="sxs-lookup"><span data-stu-id="58c82-151">Tree controls that contain check boxes in Dynamics AX 2012</span></span>
<span data-ttu-id="58c82-152">次の例は、SysConfiguration の例です。</span><span class="sxs-lookup"><span data-stu-id="58c82-152">The following example is from SysConfiguration.</span></span>

1.  <span data-ttu-id="58c82-153">プログラムは **mouseDown** イベントがないかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="58c82-153">The program checks for the **mouseDown** event.</span></span>
2.  <span data-ttu-id="58c82-154">**mouseDown** イベントが検出されると、プログラムによって、ユーザーがノードまたは画像のどちらをクリックしたかが決定されます。</span><span class="sxs-lookup"><span data-stu-id="58c82-154">When the **mouseDown** event is detected, the program determines whether the user clicked the node or the image.</span></span>
3.  <span data-ttu-id="58c82-155">ユーザーが画像をクリックすると、プログラムはイメージの状態を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="58c82-155">If the user clicked the image, the program toggles the image state.</span></span>

<span data-ttu-id="58c82-156">このコードは、現在のバージョンでは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="58c82-156">None of this code is required for the current version.</span></span>

    int mouseDown(int x, int y, int button, boolean ctrl, boolean shift)
    {
        int idx,f;
        FormTreeItem        parentNode, node;
        int                 parentMode;
        boolean             enabled;
        #FormTreeControl;
        [idx,f] = this.hitTest(x,y);
        parentNode  = this.getItem(this.getParent(idx));
        node        = this.getItem(idx);
        if (node)
        {
            if(parentNode)
            {
                if (element.enabled(parentNode.data()))
                parentMode = true;
            }
            else
                parentMode  = true;
            if ((f & #FTCHT_ONITEMICON) && parentMode)
            {
                if (!node.overlayImage())
                {
                    enabled = (element.enabled(this.getItem(idx).data()) ? false : true);
                    element.enabled(this.getItem(idx).data(), enabled);
                    element.drawTree();
                }
                return 1;
            }
        }
        return super(x, y, button, ctrl, shift);
    }

<span data-ttu-id="58c82-157">現在のバージョンでは、まだあらかじめ選択されているノードがユーザーに表示されるシナリオの選択されている状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="58c82-157">In the current version, you still set the selected state for scenarios where the user is presented with preselected nodes.</span></span> <span data-ttu-id="58c82-158">また、開発者は、FormTreeItem の作成時に、状態を明示的にまだ設定することができます。</span><span class="sxs-lookup"><span data-stu-id="58c82-158">Additionally, the developer can still set the state explicitly when the FormTreeItem is created.</span></span> <span data-ttu-id="58c82-159">ただし、現在の画像を指定する代わりに、開発者は FormTreeItem の **stateChecked** プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="58c82-159">However, instead of specifying the current image, the developer now sets the **stateChecked** property on the FormTreeItem.</span></span> <span data-ttu-id="58c82-160">開発者は、チェック ボックスの状態がいつ変更されるかを知る必要がある場合、**checkedStateChanged()** メソッドをオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="58c82-160">If developers must know when the state of a check box changes, they can override the **checkedStateChanged()** method.</span></span>

## <a name="basic-check-box-use-for-tree-controls-in-the-current-version"></a><span data-ttu-id="58c82-161">現在のバージョンのツリー コントロールに使用する基本的なチェック ボックス</span><span class="sxs-lookup"><span data-stu-id="58c82-161">Basic check box use for tree controls in the current version</span></span>
<span data-ttu-id="58c82-162">モデル化されたツリー コントロールの**チェック ボックス** プロパティが**はい**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="58c82-162">Make sure that the **Check Box** property on the modeled tree control is set to **Yes**.</span></span> <span data-ttu-id="58c82-163">ノードの状態を明示的に設定するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="58c82-163">To explicitly set the state on a node, use the following code.</span></span>

    formTreeItem.stateChecked(FormTreeCheckedState::Checked);
    formTreeControl.setItem(formTreeItem);

<span data-ttu-id="58c82-164">現在の状態のノードを調べるには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="58c82-164">To interrogate a node for its current state, use the following code.</span></span>

    FormTreeItem formTreeItem = formTreeControl.getItem(formTreeControl.getSelection());
    FormTreeCheckedState currentState;
    if (formTreeItem != null)
    {
        currentState = formTreeItem.stateChecked();
        switch (currentState)
        {
            case FormTreeCheckedState::Unchecked:
                /* unchecked */
                break;
            case FormTreeCheckedState::Checked:
                /*checked */
                break;
            case FormTreeCheckedState::Partial:
                /* parent has children checked */
                break;
            default:
                /* shouldn’t get here */
                break;
        }
    }

<span data-ttu-id="58c82-165">ノードのチェック状態 (**idx** はノード インデックス) に対応または追跡するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="58c82-165">To react to or track the checked state of a node (**idx** is the node index), use the following code.</span></span>

    public void checkedStateChanged(int _Idx, FormTreeCheckedState _newState)
    {
        super(_Idx, _newState);
    }


