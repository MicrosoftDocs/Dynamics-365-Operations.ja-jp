---
title: VSProjectLinkNode クラス
description: このトピックでは、VSProjectLinkNode クラスについて説明します。
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
ms.openlocfilehash: 0c98e2c992e0798005cc496f9164d09c4c7d00f6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502694"
---
# <a name="class-vsprojectlinknode"></a>クラス VSProjectLinkNode

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectLinkNode extends VSItemNode
```

VSProjectLinkNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードにある別の AOT へのリンクを表します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>方法

| 方法                                                             | 説明                           |
|--------------------------------------------------------------------|---------------------------------------|
| public str AOTgetSource()                                          | このノードのソース コードを返します。 |
| public str getAOTPath()                                            |                                       |
| public BinData getFileData()                                       |                                       |
| ::public static void notifyFileCreated(TreeNode node)              |                                       |
| public void setFile(str fileName)                                  |                                       |
| public void setFileData(BinData data)                              |                                       |
| public void getFile(str fileName)                                  |                                       |
| ::public static void notifyFileUpdated(TreeNode node)              |                                       |
| public void AOTsetSource(str source, \[boolean isStatic\])         | このノードのソース コードを設定します。    |
| ::public static void notifyFileRenamed(TreeNode node, str oldName) |                                       |
| ::public static void notifyFileDeleted(TreeNode node, str aotPath) |                                       |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---aotgetsource"></a>備考 - AOTgetSource

この関数はソース コードを持つノードによってオーバーライドされます。

## <a name="method-getaotpath"></a>メソッド getAOTPath

```xpp
public str getAOTPath()
```

### <a name="return-value---getaotpath"></a>戻り値 - getAOTPath

## <a name="method-getfiledata"></a>メソッド getFileData

```xpp
public BinData getFileData()
```

### <a name="return-value---getfiledata"></a>戻り値 - getFileData

## <a name="method-notifyfilecreated"></a>メソッド notifyFileCreated

```xpp
public static void notifyFileCreated(TreeNode node)
```

### <a name="parameters---notifyfilecreated"></a>パラメーター - notifyFileCreated

node  

## <a name="method-setfile"></a>メソッド setFile

```xpp
public void setFile(str fileName)
```

### <a name="parameters---setfile"></a>パラメーター - setFile

fileName  

## <a name="method-setfiledata"></a>メソッド setFileData

```xpp
public void setFileData(BinData data)
```

### <a name="parameters---setfiledata"></a>パラメーター - setFileData

データ  

## <a name="method-getfile"></a>メソッド getFile

```xpp
public void getFile(str fileName)
```

### <a name="parameters---getfile"></a>パラメーター - getFile

fileName  

## <a name="method-notifyfileupdated"></a>メソッド notifyFileUpdated

```xpp
public static void notifyFileUpdated(TreeNode node)
```

### <a name="parameters---notifyfileupdated"></a>パラメーター - notifyFileUpdated

node  

## <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a>パラメーター - AOTsetSource

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

### <a name="remarks---aotsetsource"></a>備考 - AOTgetSource

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="method-notifyfilerenamed"></a>メソッド notifyFileRenamed

```xpp
public static void notifyFileRenamed(TreeNode node, str oldName)
```

### <a name="parameters---notifyfilerenamed"></a>パラメーター - notifyFileRenamed

node  

<!-- -->

oldName  

## <a name="method-notifyfiledeleted"></a>メソッド notifyFileDeleted

```xpp
public static void notifyFileDeleted(TreeNode node, str aotPath)
```

### <a name="parameters---notifyfiledeleted"></a>パラメーター - notifyFileDeleted

node  

<!-- -->

aotPath  

