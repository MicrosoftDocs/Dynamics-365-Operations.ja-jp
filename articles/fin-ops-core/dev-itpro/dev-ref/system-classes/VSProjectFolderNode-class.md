---
title: VSProjectFolderNode クラス
description: このトピックでは、VSProjectFolderNode クラスについて説明します。
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
ms.openlocfilehash: 23a621d60678b6504f55e533e9fa20c42f9addd5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502695"
---
# <a name="class-vsprojectfoldernode"></a>クラス VSProjectFolderNode

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectFolderNode extends TreeNode
```

VSProjectFolderNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでフォルダーを表します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                                                    | このノードのソース コードを返します。                                                                    |
| public VSProjectFileNode createFileNode(str name)                                            | この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。   |
| public VSProjectFolderNode createFolderNode(str name)                                        | この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。 |
| public VSProjectLinkNode createLinkNode(str name, str aotPath, \[boolean createLinkedNode\]) | この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。   |
| public BinData getFileData()                                                                 |                                                                                                          |
| ::public static void notifyFileUpdated(TreeNode node)                                        |                                                                                                          |
| ::public static void notifyFileDeleted(TreeNode node, str aotPath)                           |                                                                                                          |
| public void setFileData(BinData data)                                                        |                                                                                                          |
| public void AOTsetSource(str source, \[boolean isStatic\])                                   | このノードのソース コードを設定します。                                                                       |
| public void getFile(str fileName)                                                            |                                                                                                          |
| ::public static void notifyFileCreated(TreeNode node)                                        |                                                                                                          |
| ::public static void notifyFileRenamed(TreeNode node, str oldName)                           |                                                                                                          |
| public void setFile(str fileName)                                                            |                                                                                                          |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---aotgetsource"></a>備考 - AOTgetSource

この関数はソース コードを持つノードによってオーバーライドされます。

## <a name="method-createfilenode"></a>メソッド createFileNode

この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。

```xpp
public VSProjectFileNode createFileNode(str name)
```

### <a name="parameters---createfilenode"></a>パラメータ - createFileNode

名前  
ファイル ノードの名前。

### <a name="return-value---createfilenode"></a>戻り値 - createFileNode

VSProjectFileNode クラスの新しいインスタンス。

## <a name="method-createfoldernode"></a>メソッド createFolderNode

この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。

```xpp
public VSProjectFolderNode createFolderNode(str name)
```

### <a name="parameters---createfoldernode"></a>パラメーター - createFolderNode

名前  
フォルダー ノードの名前。

### <a name="return-value---createfoldernode"></a>戻り値 - createFolderNode

VSProjectFolderNode クラスの新しいインスタンス。

## <a name="method-createlinknode"></a>メソッド createLinkNode

この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。

```xpp
public VSProjectLinkNode createLinkNode(str name, str aotPath, [boolean createLinkedNode])
```

### <a name="parameters---createlinknode"></a>パラメーター - createLinkNode

名前  

<!-- -->

aotPath  

<!-- -->

createLinkedNode  

### <a name="return-value---createlinknode"></a>戻り値 - createLinkNode

VSProjectLinkNode クラスの新しいインスタンス。

## <a name="method-getfiledata"></a>メソッド getFileData

```xpp
public BinData getFileData()
```

### <a name="return-value---getfiledata"></a>戻り値 - getFileData

## <a name="method-notifyfileupdated"></a>メソッド notifyFileUpdated

```xpp
public static void notifyFileUpdated(TreeNode node)
```

### <a name="parameters---notifyfileupdated"></a>パラメーター - notifyFileUpdated

node  

## <a name="method-notifyfiledeleted"></a>メソッド notifyFileDeleted

```xpp
public static void notifyFileDeleted(TreeNode node, str aotPath)
```

### <a name="parameters---notifyfiledeleted"></a>パラメーター - notifyFileDeleted

node  

<!-- -->

aotPath  

## <a name="method-setfiledata"></a>メソッド setFileData

```xpp
public void setFileData(BinData data)
```

### <a name="parameters---setfiledata"></a>パラメーター - setFileData

データ  

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

## <a name="method-getfile"></a>メソッド getFile

```xpp
public void getFile(str fileName)
```

### <a name="parameters---getfile"></a>パラメーター - getFile

fileName  

## <a name="method-notifyfilecreated"></a>メソッド notifyFileCreated

```xpp
public static void notifyFileCreated(TreeNode node)
```

### <a name="parameters---notifyfilecreated"></a>パラメーター - notifyFileCreated

node  

## <a name="method-notifyfilerenamed"></a>メソッド notifyFileRenamed

```xpp
public static void notifyFileRenamed(TreeNode node, str oldName)
```

### <a name="parameters---notifyfilerenamed"></a>パラメーター - notifyFileRenamed

node  

<!-- -->

oldName  

## <a name="method-setfile"></a>メソッド setFile

```xpp
public void setFile(str fileName)
```

### <a name="parameters---setfile"></a>パラメーター - setFile

fileName  

