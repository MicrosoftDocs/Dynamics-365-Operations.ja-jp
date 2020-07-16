---
title: xNavPane クラス
description: このトピックでは、xNavPane クラスについて説明します。
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
ms.openlocfilehash: c389b0dcbbbabbe21c2accfc0f37cb610f1e0d23
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502678"
---
# <a name="class-xnavpane"></a>クラス xNavPane

[!include [banner](../../includes/banner.md)]

```xpp
class xNavPane extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                | 説明                                       |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| public boolean collapseFavoriteNode(str path)                                                         |                                                   |
| public boolean collapseNode(str path)                                                                 |                                                   |
| public boolean expandFavoriteNode(str path)                                                           |                                                   |
| public boolean expandNode(str path)                                                                   |                                                   |
| public boolean favPaneVisible(\[boolean value\])                                                      |                                                   |
| public container getButtons()                                                                         |                                                   |
| public str getCurrMenuName()                                                                          |                                                   |
| public TreeNode getSelectedFavoriteNode()                                                             |                                                   |
| public TreeNode getSelectedNode()                                                                     |                                                   |
| public boolean navPaneVisible(\[boolean value\])                                                      |                                                   |
| public boolean runFavoriteNode(str path)                                                              |                                                   |
| public boolean runNode(str path)                                                                      |                                                   |
| public str selectedFavoriteGroup(\[str groupName\])                                                   |                                                   |
| public str selectedGroup(\[str groupName\])                                                           |                                                   |
| public boolean setSelectedFavoriteNode(str path)                                                      |                                                   |
| public boolean setSelectedNode(str path)                                                              |                                                   |
| public void refreshFavorites(\[str selectFavoriteGroup\], \[int workspaceNum\], \[boolean saveToDB\]) |                                                   |
| public void setCurrMenuButtons(container buttons)                                                     |                                                   |
| public void loadStartupButtons()                                                                      |                                                   |
| public void new()                                                                                     | xNavPane クラスの新しいインスタンスを初期化します。 |

## <a name="method-collapsefavoritenode"></a>メソッド collapseFavoriteNode

```xpp
public boolean collapseFavoriteNode(str path)
```

### <a name="parameters---collapsefavoritenode"></a>パラメーター - collapseFavoriteNode

path  

### <a name="return-value---collapsefavoritenode"></a>戻り値 - collapseFavoriteNode

## <a name="method-collapsenode"></a>メソッド collapseNode

```xpp
public boolean collapseNode(str path)
```

### <a name="parameters---collapsenode"></a>パラメーター - collapseNode

path  

### <a name="return-value---collapsenode"></a>戻り値 - collapseNode

## <a name="method-expandfavoritenode"></a>メソッド expandFavoriteNode

```xpp
public boolean expandFavoriteNode(str path)
```

### <a name="parameters---expandfavoritenode"></a>パラメーター - expandFavoriteNode

path  

### <a name="return-value---expandfavoritenode"></a>戻り値 - expandFavoriteNode

## <a name="method-expandnode"></a>メソッド expandNode

```xpp
public boolean expandNode(str path)
```

### <a name="parameters---expandnode"></a>パラメーター - expandNode

path  

### <a name="return-value---expandnode"></a>戻り値 - expandNode

## <a name="method-favpanevisible"></a>メソッド favPaneVisible

```xpp
public boolean favPaneVisible([boolean value])
```

### <a name="parameters---favpanevisible"></a>パラメーター - favPaneVisible

値  

### <a name="return-value---favpanevisible"></a>戻り値 - favPaneVisible

## <a name="method-getbuttons"></a>メソッド getButtons

```xpp
public container getButtons()
```

### <a name="return-value---getbuttons"></a>戻り値 - getButtons

## <a name="method-getcurrmenuname"></a>メソッド getCurrMenuName

```xpp
public str getCurrMenuName()
```

### <a name="return-value---getcurrmenuname"></a>戻り値 - getCurrMenuName

## <a name="method-getselectedfavoritenode"></a>メソッド getSelectedFavoriteNode

```xpp
public TreeNode getSelectedFavoriteNode()
```

### <a name="return-value---getselectedfavoritenode"></a>戻り値 - getSelectedFavoriteNode

## <a name="method-getselectednode"></a>メソッド getSelectedNode

```xpp
public TreeNode getSelectedNode()
```

### <a name="return-value---getselectednode"></a>戻り値 - getSelectedNode

## <a name="method-navpanevisible"></a>メソッド navPaneVisible

```xpp
public boolean navPaneVisible([boolean value])
```

### <a name="parameters---navpanevisible"></a>パラメーター - navPaneVisible

値  

### <a name="return-value---navpanevisible"></a>戻り値 - navPaneVisible

## <a name="method-runfavoritenode"></a>メソッド runFavoriteNode

```xpp
public boolean runFavoriteNode(str path)
```

### <a name="parameters---runfavoritenode"></a>パラメーター - runFavoriteNode

path  

### <a name="return-value---runfavoritenode"></a>戻り値 - runFavoriteNode

## <a name="method-runnode"></a>メソッド runNode

```xpp
public boolean runNode(str path)
```

### <a name="parameters---runnode"></a>パラメーター - runNode

path  

### <a name="return-value---runnode"></a>戻り値 - runNode

## <a name="method-selectedfavoritegroup"></a>メソッド selectedFavoriteGroup

```xpp
public str selectedFavoriteGroup([str groupName])
```

### <a name="parameters---selectedfavoritegroup"></a>パラメーター - selectedFavoriteGroup

groupName  

### <a name="return-value---selectedfavoritegroup"></a>戻り値 - selectedFavoriteGroup

## <a name="method-selectedgroup"></a>メソッド selectedGroup

```xpp
public str selectedGroup([str groupName])
```

### <a name="parameters---selectedgroup"></a>パラメーター - selectedGroup

groupName  

### <a name="return-value---selectedgroup"></a>戻り値 - selectedGroup

## <a name="method-setselectedfavoritenode"></a>メソッド setSelectedFavoriteNode

```xpp
public boolean setSelectedFavoriteNode(str path)
```

### <a name="parameters---setselectedfavoritenode"></a>パラメーター - setSelectedFavoriteNode

path  

### <a name="return-value---setselectedfavoritenode"></a>戻り値 - setSelectedFavoriteNode

## <a name="method-setselectednode"></a>メソッド setSelectedNode

```xpp
public boolean setSelectedNode(str path)
```

### <a name="parameters---setselectednode"></a>パラメーター - setSelectedNode

path  

### <a name="return-value---setselectednode"></a>戻り値 - setSelectedNode

## <a name="method-refreshfavorites"></a>メソッド refreshFavorites

```xpp
public void refreshFavorites([str selectFavoriteGroup], [int workspaceNum], [boolean saveToDB])
```

### <a name="parameters---refreshfavorites"></a>パラメーター - refreshFavorites

selectFavoriteGroup  

<!-- -->

workspaceNum  

<!-- -->

saveToDB  

## <a name="method-setcurrmenubuttons"></a>メソッド setCurrMenuButtons

```xpp
public void setCurrMenuButtons(container buttons)
```

### <a name="parameters---setcurrmenubuttons"></a>パラメーター - setCurrMenuButtons

buttons  

## <a name="method-loadstartupbuttons"></a>メソッド loadStartupButtons

```xpp
public void loadStartupButtons()
```

## <a name="method-new"></a>メソッド new

xNavPane クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

