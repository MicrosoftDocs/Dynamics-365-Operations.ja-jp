---
title: VSItemNode クラス
description: このトピックでは、VSItemNode クラスについて説明します。
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
ms.openlocfilehash: 2dc8bf1d7eea3add3dc9145a788014a4eadedd9b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502697"
---
# <a name="class-vsitemnode"></a>クラス VSItemNode

[!include [banner](../../includes/banner.md)]

```xpp
class VSItemNode extends TreeNode
```

VSItemNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードの基本クラスです。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                             | 説明                                          |
|--------------------------------------------------------------------|------------------------------------------------------|
| public str AOTgetSource()                                          | このノードのソース コードを返します。                |
| public BinData getFileData()                                       |                                                      |
| ::public static void notifyFileDeleted(TreeNode node, str aotPath) | ファイルが削除されたことをリスナーに通知します。     |
| ::public static void notifyFileUpdated(TreeNode node)              | ファイルが更新されたことをリスナーに通知します。     |
| public void setFileData(BinData data)                              |                                                      |
| public void AOTsetSource(str source, \[boolean isStatic\])         | このノードのソース コードを設定します。                   |
| public void getFile(str fileName)                                  |                                                      |
| ::public static void notifyFileCreated(TreeNode node)              | 新しいファイルが作成されたことをリスナーに通知します。 |
| ::public static void notifyFileRenamed(TreeNode node, str oldName) | ファイルの名前が変更されたことをリスナーに通知します。     |
| public void setFile(str fileName)                                  |                                                      |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---aotgetsource"></a>備考 - AOTgetSource

この関数はソース コードを持つノードによってオーバーライドされます。

## <a name="method-getfiledata"></a>メソッド getFileData

```xpp
public BinData getFileData()
```

### <a name="return-value---getfiledata"></a>戻り値 - getFileData

## <a name="method-notifyfiledeleted"></a>メソッド notifyFileDeleted

ファイルが削除されたことをリスナーに通知します。

```xpp
public static void notifyFileDeleted(TreeNode node, str aotPath)
```

### <a name="parameters---notifyfiledeleted"></a>パラメーター - notifyFileDeleted

node  
ファイルの AOT パス。

<!-- -->

aotPath  
ファイルの AOT パス。

## <a name="method-notifyfileupdated"></a>メソッド notifyFileUpdated

ファイルが更新されたことをリスナーに通知します。

```xpp
public static void notifyFileUpdated(TreeNode node)
```

### <a name="parameters---notifyfileupdated"></a>パラメーター - notifyFileUpdated

node  
更新ノード。

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

新しいファイルが作成されたことをリスナーに通知します。

```xpp
public static void notifyFileCreated(TreeNode node)
```

### <a name="parameters---notifyfilecreated"></a>パラメーター - notifyFileCreated

node  
作成されたノード。

## <a name="method-notifyfilerenamed"></a>メソッド notifyFileRenamed

ファイルの名前が変更されたことをリスナーに通知します。

```xpp
public static void notifyFileRenamed(TreeNode node, str oldName)
```

### <a name="parameters---notifyfilerenamed"></a>パラメーター - notifyFileRenamed

node  
ファイルの古い名前。

<!-- -->

oldName  
ファイルの古い名前。

## <a name="method-setfile"></a>メソッド setFile

```xpp
public void setFile(str fileName)
```

### <a name="parameters---setfile"></a>パラメーター - setFile

fileName  

