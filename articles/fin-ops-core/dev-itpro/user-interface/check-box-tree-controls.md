---
title: ツリー コントロールでのチェック ボックスのサポート
description: この記事は、ツリー コントロールのチェック ボックス コントロールを使用するための入門書として作成されています。 ツリー コントロールを使用するための一般的な「方法」ではありません。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31501
ms.assetid: 57c0fa59-ef48-4913-9f92-407ff2566c72
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b2ff302a2ba85b1f42f74a6f809adadf1ed0c7976c808c792d3f9483c054fea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728977"
---
# <a name="check-box-support-in-tree-controls"></a>ツリー コントロールでのチェック ボックスのサポート

[!include [banner](../includes/banner.md)]

この記事は、ツリー コントロールのチェック ボックス コントロールを使用するための入門書として作成されています。 ツリー コントロールを使用するための一般的な「方法」ではありません。

Microsoft Dynamics AX 2012 には、データをツリー階層で表示し、ユーザーがチェック ボックスを使用して 1 つまたは複数のノードを選択できるようにするために強化されたツリー コントロールの例がいくつか含まれています。 Dynamics AX 2012 では、ツリー コントロールには、チェック ボックスのコントロールに対して、組み込みのサポートがありませんでした。 代わりに、チェック ボックスのイメージがツリー コントロール内の各ノードに対して追加されました。 ユーザーがチェックボックスをクリックすると、各ノードのイメージの状態が切り替わりました。 

![以前のバージョンでのツリー コントロールのスクリーン ショット。](./media/treecontrol_legacycheckbox.png) 

現在のバージョンでは、開発者の経験が大幅に簡素化されています。 チェック ボックスのサポートがツリー コントロールに組み込まれました。 

![現在のバージョンでのツリー コントロールのスクリーン ショット。](./media/treecontrol_ax7checkbox.png) 

チェック ボックスを含めるイメージを使用する必要がなくなり、選択されている場合にチェック ボックスの状態を明示的に設定する必要もありません。 コントロールは画像を使用せず、チェック ボックスの状態は、トライステートのチェック ボックスで期待どおりに管理されます。 状態チェック ボックスの例では、ほとんどのインストール シナリオで検出が可能です。 状態チェック ボックスが使用されているとき、ユーザーが親ノードを選択すると、その親のすべての子も選択されます。 チェックボックスの操作は、ノードの展開/折りたたみ機能とは独立しています。 親ノードが折りたたまれているのとき (子が非表示のとき)、親ノードに付いているチェック マークは、すべての子も選択されていることを示します。 ただし、複数の子を持つ親の 1 つの子が選択されない場合、親ノードの外観が変化します。 チェックボックスにチェックマークは含まれなくなりましたが、記入されています。 この状態は、部分チェックと見なされます。 したがって、親ノードには 3 つの状態があります。

-   確認済
-   未チェック
-   部分的

ユーザーが部分的状態にある親ノードのチェック ボックスをクリックすると、親とそのすべての子の状態はチェックされた状態に変更されます。 (親ノードおよびそのすべての子ノードが選択されるようになります。) 

**部分的状態にある親ノード** 

![部分的状態にある親ノードの例。](./media/treecontrol_partialparent.png) 

**親ノードが選択された後、チェックされた状態の親ノードおよびすべての子ノード**

![チェックされた状態にある親ノードと子ノードの例。](./media/treecontrol_parent.png) 

ユーザーがチェックされた状態にある親ノードのチェック ボックスをクリックすると、親とそのすべての子の状態は未チェックの状態に変更されます。 (親ノードおよびそのすべての子ノードが消去されるようになります。) 

**チェックされた状態にある親ノード** 

![チェックされた状態にある親ノードの例。](./media/treecontrol_parent.png)

**親ノードがクリアされた後、チェックされていない状態の親ノードおよびすべての子ノード** 

![未チェック状態にある親ノードと子ノードの例。](./media/treecontrol_noparent1.png) 

ユーザーが未チェック状態にある親ノードのチェック ボックスをクリックすると、親とそのすべての子の状態はチェックされた状態に変更されます。 (親ノードおよびそのすべての子ノードが選択されるようになります。) 

**未チェック状態にある親ノード** 

![未チェック状態にある親ノードの例。](./media/treecontrol_noparent1.png) 

**親ノードが選択された後、チェックされた状態の親ノードおよびすべての子ノード** 

![チェックされた状態にある親ノードと子ノードの例。](./media/treecontrol_parent.png) 

子を持たない子ノード (つまり、それ自体が親ではない子ノード) には、2 つの状態: チェックされているか未チェックかしかありません。 チェックされた状態の唯一の子である子ノードは、その親の状態に影響します。 子ノードが選択されている場合、その親の状態は部分的な状態に変更されます。 **注記:** ツリー内の 1 つのノードにも、現在のノードであることを示す「選択」状態があります。 この状態は、チェックされた状態とは異なります。

## <a name="tree-controls-that-contain-check-boxes-in-dynamics-ax-2012"></a>Dynamics AX 2012 のチェック ボックスを含むツリー コントロール
次の例は、SysConfiguration の例です。

1.  プログラムは **mouseDown** イベントがないかどうかを確認します。
2.  **mouseDown** イベントが検出されると、プログラムによって、ユーザーがノードまたは画像のどちらをクリックしたかが決定されます。
3.  ユーザーが画像をクリックすると、プログラムはイメージの状態を切り替えます。

このコードは、現在のバージョンでは必要ありません。

```xpp
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
```

現在のバージョンでは、まだあらかじめ選択されているノードがユーザーに表示されるシナリオの選択されている状態を設定します。 また、開発者は、FormTreeItem の作成時に、状態を明示的にまだ設定することができます。 ただし、現在の画像を指定する代わりに、開発者は FormTreeItem の **stateChecked** プロパティを設定できます。 開発者は、チェック ボックスの状態がいつ変更されるかを知る必要がある場合、**checkedStateChanged()** メソッドをオーバーライドできます。

## <a name="basic-check-box-use-for-tree-controls-in-the-current-version"></a>現在のバージョンのツリー コントロールに使用する基本的なチェック ボックス
モデル化されたツリー コントロールの **チェック ボックス** プロパティが **はい** に設定されていることを確認します。 ノードの状態を明示的に設定するには、次のコードを使用します。

```xpp
formTreeItem.stateChecked(FormTreeCheckedState::Checked);
formTreeControl.setItem(formTreeItem);
```

現在の状態のノードを調べるには、次のコードを使用します。

```xpp
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
```

ノードのチェック状態 (**idx** はノード インデックス) に対応または追跡するには、次のコードを使用します。

```xpp
public void checkedStateChanged(int _Idx, FormTreeCheckedState _newState)
{
    super(_Idx, _newState);
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]