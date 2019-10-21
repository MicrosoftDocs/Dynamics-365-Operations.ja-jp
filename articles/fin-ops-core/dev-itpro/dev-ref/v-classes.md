---
title: V クラス
description: 文字 V で始まるシステム API クラス。
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
ms.custom: 55841
ms.assetid: fd3859a7-c0e5-41b3-9bd3-fc68099e727f
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e43aa3a4e481ddc8d6ae6d811c12cf2aa58228ef
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191606"
---
# <a name="v-classes"></a>V クラス

[!include [banner](../includes/banner.md)]

文字 V で始まるシステム API クラス。

<a name="class-validateeventargs"></a>クラス ValidateEventArgs
-----------------------

    class ValidateEventArgs extends DataEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                | 説明 |
|-------------------------------------------------------|-------------|
| public boolean parmValidateResult(\[boolean result\]) |             |
| public void new(boolean result)                       |             |

### <a name="method-parmvalidateresult"></a>メソッド parmValidateResult

    public boolean parmValidateResult([boolean result])

#### <a name="parameters"></a>パラメーター

件の結果  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(boolean result)

#### <a name="parameters"></a>パラメーター

件の結果  

## <a name="class-validatefieldeventargs"></a>クラス ValidateFieldEventArgs
    class ValidateFieldEventArgs extends ValidateEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                       | 説明 |
|----------------------------------------------|-------------|
| public int parmFieldId()                     |             |
| public void new(int fieldId, boolean result) |             |

### <a name="method-parmfieldid"></a>メソッド parmFieldId

    public int parmFieldId()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(int fieldId, boolean result)

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

件の結果  

## <a name="class-validatefieldvalueeventargs"></a>クラス ValidateFieldValueEventArgs
    class ValidateFieldValueEventArgs extends ValidateEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                         | 説明 |
|----------------------------------------------------------------|-------------|
| public str parmFieldName()                                     |             |
| public int parmArrayIndex()                                    |             |
| public void new(str fieldName, int arrayIndex, boolean result) |             |

### <a name="method-parmfieldname"></a>メソッド parmFieldName

    public str parmFieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-parmarrayindex"></a>メソッド parmArrayIndex

    public int parmArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(str fieldName, int arrayIndex, boolean result)

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

arrayIndex  

<!-- -->

件の結果  

## <a name="class-virtualchannelmanager"></a>クラス VirtualChannelManager
    class VirtualChannelManager extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明                                                    |
|------------------------------------------------|----------------------------------------------------------------|
| public void finalize()                         |                                                                |
| public void new()                              | VirtualChannelManager クラスの新しいインスタンスを初期化します。 |
| public void sendData(int listenerId, str data) |                                                                |

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

VirtualChannelManager クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-senddata"></a>メソッド sendData

    public void sendData(int listenerId, str data)

#### <a name="parameters"></a>パラメーター

listenerId  

<!-- -->

データ  

## <a name="class-vsitemnode"></a>クラス VSItemNode
    class VSItemNode extends TreeNode

VSItemNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードの基本クラスです。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-getfiledata"></a>メソッド getFileData

    public BinData getFileData()

#### <a name="return-value"></a>戻り値

### <a name="method-notifyfiledeleted"></a>メソッド notifyFileDeleted

ファイルが削除されたことをリスナーに通知します。

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a>パラメーター

node  
ファイルの AOT パス。

<!-- -->

aotPath  
ファイルの AOT パス。

### <a name="method-notifyfileupdated"></a>メソッド notifyFileUpdated

ファイルが更新されたことをリスナーに通知します。

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  
更新ノード。

### <a name="method-setfiledata"></a>メソッド setFileData

    public void setFileData(BinData data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

### <a name="method-getfile"></a>メソッド getFile

    public void getFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

### <a name="method-notifyfilecreated"></a>メソッド notifyFileCreated

新しいファイルが作成されたことをリスナーに通知します。

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  
作成されたノード。

### <a name="method-notifyfilerenamed"></a>メソッド notifyFileRenamed

ファイルの名前が変更されたことをリスナーに通知します。

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a>パラメーター

node  
ファイルの古い名前。

<!-- -->

oldName  
ファイルの古い名前。

### <a name="method-setfile"></a>メソッド setFile

    public void setFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

## <a name="class-vsprojectfilenode"></a>クラス VSProjectFileNode
    class VSProjectFileNode extends VSItemNode

VSProjectFileNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでファイルを表します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                             | 説明                           |
|--------------------------------------------------------------------|---------------------------------------|
| public str AOTgetSource()                                          | このノードのソース コードを返します。 |
| public BinData getFileData()                                       |                                       |
| ::public static void notifyFileCreated(TreeNode node)              |                                       |
| public void setFileData(BinData data)                              |                                       |
| public void getFile(str fileName)                                  |                                       |
| ::public static void notifyFileDeleted(TreeNode node, str aotPath) |                                       |
| ::public static void notifyFileUpdated(TreeNode node)              |                                       |
| public void setFile(str fileName)                                  |                                       |
| ::public static void notifyFileRenamed(TreeNode node, str oldName) |                                       |
| public void AOTsetSource(str source, \[boolean isStatic\])         | このノードのソース コードを設定します。    |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-getfiledata"></a>メソッド getFileData

    public BinData getFileData()

#### <a name="return-value"></a>戻り値

### <a name="method-notifyfilecreated"></a>メソッド notifyFileCreated

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-setfiledata"></a>メソッド setFileData

    public void setFileData(BinData data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-getfile"></a>メソッド getFile

    public void getFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

### <a name="method-notifyfiledeleted"></a>メソッド notifyFileDeleted

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

aotPath  

### <a name="method-notifyfileupdated"></a>メソッド notifyFileUpdated

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-setfile"></a>メソッド setFile

    public void setFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

### <a name="method-notifyfilerenamed"></a>メソッド notifyFileRenamed

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

oldName  

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="class-vsprojectfoldernode"></a>クラス VSProjectFolderNode
    class VSProjectFolderNode extends TreeNode

VSProjectFolderNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでフォルダーを表します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-createfilenode"></a>メソッド createFileNode

この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。

    public VSProjectFileNode createFileNode(str name)

#### <a name="parameters"></a>パラメーター

名前  
ファイル ノードの名前。

#### <a name="return-value"></a>戻り値

VSProjectFileNode クラスの新しいインスタンス。

### <a name="method-createfoldernode"></a>メソッド createFolderNode

この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。

    public VSProjectFolderNode createFolderNode(str name)

#### <a name="parameters"></a>パラメーター

名前  
フォルダー ノードの名前。

#### <a name="return-value"></a>戻り値

VSProjectFolderNode クラスの新しいインスタンス。

### <a name="method-createlinknode"></a>メソッド createLinkNode

この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。

    public VSProjectLinkNode createLinkNode(str name, str aotPath, [boolean createLinkedNode])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

aotPath  

<!-- -->

createLinkedNode  

#### <a name="return-value"></a>戻り値

VSProjectLinkNode クラスの新しいインスタンス。

### <a name="method-getfiledata"></a>メソッド getFileData

    public BinData getFileData()

#### <a name="return-value"></a>戻り値

### <a name="method-notifyfileupdated"></a>メソッド notifyFileUpdated

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-notifyfiledeleted"></a>メソッド notifyFileDeleted

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

aotPath  

### <a name="method-setfiledata"></a>メソッド setFileData

    public void setFileData(BinData data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

### <a name="method-getfile"></a>メソッド getFile

    public void getFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

### <a name="method-notifyfilecreated"></a>メソッド notifyFileCreated

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-notifyfilerenamed"></a>メソッド notifyFileRenamed

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

oldName  

### <a name="method-setfile"></a>メソッド setFile

    public void setFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

## <a name="class-vsprojectlinknode"></a>クラス VSProjectLinkNode
    class VSProjectLinkNode extends VSItemNode

VSProjectLinkNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードにある別の AOT へのリンクを表します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

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

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-getaotpath"></a>メソッド getAOTPath

    public str getAOTPath()

#### <a name="return-value"></a>戻り値

### <a name="method-getfiledata"></a>メソッド getFileData

    public BinData getFileData()

#### <a name="return-value"></a>戻り値

### <a name="method-notifyfilecreated"></a>メソッド notifyFileCreated

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-setfile"></a>メソッド setFile

    public void setFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

### <a name="method-setfiledata"></a>メソッド setFileData

    public void setFileData(BinData data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-getfile"></a>メソッド getFile

    public void getFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

### <a name="method-notifyfileupdated"></a>メソッド notifyFileUpdated

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

### <a name="method-notifyfilerenamed"></a>メソッド notifyFileRenamed

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

oldName  

### <a name="method-notifyfiledeleted"></a>メソッド notifyFileDeleted

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

aotPath  

## <a name="class-vsprojectnode"></a>クラス VSProjectNode
    class VSProjectNode extends xResourceNode

VSProjectNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでプロジェクトを表します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                | 説明                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| public container extract(\[str path\], \[boolean extractReferenced\]) | ディスクにプロジェクト全体を展開します。                                                               |
| public VSProjectFolderNode getContentNode()                           | Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。        |
| public DeployTo getDeployTo()                                         | deployTo プロパティの値を取得します。                                                              |
| public VSProjectFolderNode getOutputNode()                            | Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。  |
| public VSProjectFileNode getPrimaryOutputNode()                       | Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。 |
| public str getPrimaryTargetFileName()                                 | Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。                                   |
| public Map getProxies()                                               | このプロジェクトでのプロキシを取得します。                                                                 |
| public container getProxiesContainer()                                | このプロジェクトでのプロキシを取得します。                                                                 |
| public str getReferencedProjectsInAOT()                               | この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。             |
| public str referencedProjects(\[str value\])                          |                                                                                                   |
| public void setPrimaryTargetFileName(str targetFileName)              | Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。                                   |
| public void extractToSpecificDir(str directory)                       |                                                                                                   |
| public void setDeployTo(DeployTo deployTo)                            | deployTo プロパティの値を設定します。                                                          |

### <a name="method-extract"></a>メソッド extract

ディスクにプロジェクト全体を展開します。

    public container extract([str path], [boolean extractReferenced])

#### <a name="parameters"></a>パラメーター

path  
参照されるプロジェクトを抽出するかどうかを決定するブール値。

<!-- -->

extractReferenced  
参照されるプロジェクトを抽出するかどうかを決定するブール値。

#### <a name="return-value"></a>戻り値

プロジェクトの展開先のパスの一覧。

### <a name="method-getcontentnode"></a>メソッド getContentNode

Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。

    public VSProjectFolderNode getContentNode()

#### <a name="return-value"></a>戻り値

Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクト。

### <a name="method-getdeployto"></a>メソッド getDeployTo

deployTo プロパティの値を取得します。

    public DeployTo getDeployTo()

#### <a name="return-value"></a>戻り値

deployTo プロパティ値。

### <a name="method-getoutputnode"></a>メソッド getOutputNode

Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。

    public VSProjectFolderNode getOutputNode()

#### <a name="return-value"></a>戻り値

Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクト。

### <a name="method-getprimaryoutputnode"></a>メソッド getPrimaryOutputNode

Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。

    public VSProjectFileNode getPrimaryOutputNode()

#### <a name="return-value"></a>戻り値

Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクト。

### <a name="method-getprimarytargetfilename"></a>メソッド getPrimaryTargetFileName

Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。

    public str getPrimaryTargetFileName()

#### <a name="return-value"></a>戻り値

Visual Studio プロジェクトのプライマリ ターゲット ファイル名。

### <a name="method-getproxies"></a>メソッド getProxies

このプロジェクトでのプロキシを取得します。

    public Map getProxies()

#### <a name="return-value"></a>戻り値

クラス、列挙、およびテーブルのキーを含むマップ。 各キーには、プロキシのリストが含まれています。

### <a name="method-getproxiescontainer"></a>メソッド getProxiesContainer

このプロジェクトでのプロキシを取得します。

    public container getProxiesContainer()

#### <a name="return-value"></a>戻り値

マップの梱包済み表現を保持するコンテナーには、Class、Enum、Table のキーが含まれています。 各キーには、プロキシのリストが含まれています。

### <a name="method-getreferencedprojectsinaot"></a>メソッド getReferencedProjectsInAOT

この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。

    public str getReferencedProjectsInAOT()

#### <a name="return-value"></a>戻り値

この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスの一覧。

### <a name="method-referencedprojects"></a>メソッド referencedProjects

    public str referencedProjects([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-setprimarytargetfilename"></a>メソッド setPrimaryTargetFileName

Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。

    public void setPrimaryTargetFileName(str targetFileName)

#### <a name="parameters"></a>パラメーター

targetFileName  
Visual Studio プロジェクトのプライマリ ターゲット ファイル名。

### <a name="method-extracttospecificdir"></a>メソッド extractToSpecificDir

    public void extractToSpecificDir(str directory)

#### <a name="parameters"></a>パラメーター

directory  

### <a name="method-setdeployto"></a>メソッド setDeployTo

deployTo プロパティの値を設定します。

    public void setDeployTo(DeployTo deployTo)

#### <a name="parameters"></a>パラメーター

deployTo  
deployTo プロパティ値。

## <a name="class-vsprojectsnode"></a>クラス VSProjectsNode
    class VSProjectsNode extends xResourceNode

VSProjectNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードのルートです。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                            | 説明                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| public TreeNode AOTfindChild(str name, \[int nodeType\])                                          | このノードの指定した子ノードを検索します。                                               |
| public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\]) | VSProjectNode クラスの新しいインスタンスを作成します。                                         |
| public container getProjectsDeployingTo(DeployTo deployTo)                                        | 指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。            |
| public container getProjectsModifiedAfter(DateTime timestamp)                                     | 指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。 |
| public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)                              |                                                                                            |
| public Object getVSProjectNodeObservable()                                                        | VSProjectNodeObservable オブジェクトを取得します。                                                   |
| public void AOTrefresh()                                                                          | .aod ファイルを最新版に変更することによりノードを更新します。                                 |

### <a name="method-aotfindchild"></a>メソッド AOTfindChild

このノードの指定した子ノードを検索します。

    public TreeNode AOTfindChild(str name, [int nodeType])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

nodeType  

#### <a name="return-value"></a>戻り値

指定したツリー ノード。

### <a name="method-createprojectnode"></a>メソッド createProjectNode

VSProjectNode クラスの新しいインスタンスを作成します。

    public VSProjectNode createProjectNode(str name, str projectTypesString, [boolean virtualNode])

#### <a name="parameters"></a>パラメーター

名前  
ノードがメモリ内でのみ作成されるかどうかを示すブール値。 この場合、ノードは Finance and Operations ストアで保持されません。

<!-- -->

projectTypesString  
ノードがメモリ内でのみ作成されるかどうかを示すブール値。 この場合、ノードは Finance and Operations ストアで保持されません。

<!-- -->

virtualNode  
ノードがメモリ内でのみ作成されるかどうかを示すブール値。 この場合、ノードは Finance and Operations ストアで保持されません。

#### <a name="return-value"></a>戻り値

作成された VSProjectNode オブジェクト。

### <a name="method-getprojectsdeployingto"></a>メソッド getProjectsDeployingTo

指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。

    public container getProjectsDeployingTo(DeployTo deployTo)

#### <a name="parameters"></a>パラメーター

deployTo  
deployTo プロパティの値。

#### <a name="return-value"></a>戻り値

VSProjectNode オブジェクトの一覧。

### <a name="method-getprojectsmodifiedafter"></a>メソッド getProjectsModifiedAfter

指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。

    public container getProjectsModifiedAfter(DateTime timestamp)

#### <a name="parameters"></a>パラメーター

timestamp  
DB\_DATETIME\_TYPE 値としての日時。

#### <a name="return-value"></a>戻り値

VSProjectNode オブジェクトの一覧。

### <a name="method-gettypenodefromguid"></a>メソッド getTypeNodeFromGuid

    public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)

#### <a name="parameters"></a>パラメーター

projectTypesString  

#### <a name="return-value"></a>戻り値

### <a name="method-getvsprojectnodeobservable"></a>メソッド getVSProjectNodeObservable

VSProjectNodeObservable オブジェクトを取得します。

    public Object getVSProjectNodeObservable()

#### <a name="return-value"></a>戻り値

VSProjectNodeObservable オブジェクト。

#### <a name="remarks"></a>備考

オブザーバーはこれで登録でき、Visual Studio プロジェクトで CRUD 操作の通知を受け取ります。

### <a name="method-aotrefresh"></a>メソッド AOTrefresh

.aod ファイルを最新版に変更することによりノードを更新します。

    public void AOTrefresh()

## <a name="class-vsprojecttypenode"></a>クラス VSProjectTypeNode
    class VSProjectTypeNode extends TreeNode

VSProjectTypeNode クラスは、AOT 内の Visual Studio プロジェクト ノードでプロジェクトの種類を表します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法 | 説明 |
|--------|-------------|
|        |             |

## <a name="class-vss"></a>クラス VSS
    class VSS extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                        | 説明                               |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| public boolean connect()                                                                                      |                                           |
| public boolean connected()                                                                                    |                                           |
| public boolean disconnect()                                                                                   |                                           |
| public container getCheckedoutFiles()                                                                         |                                           |
| public container getConnectionInfo()                                                                          |                                           |
| public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])      |                                           |
| public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)                |                                           |
| public VSSItem newSubProject(str name, str localPath)                                                         |                                           |
| public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\]) |                                           |
| public void new()                                                                                             | VSS クラスのインスタンスを初期化します。 |

### <a name="method-connect"></a>メソッド connect

    public boolean connect()

#### <a name="return-value"></a>戻り値

### <a name="method-connected"></a>メソッド connected

    public boolean connected()

#### <a name="return-value"></a>戻り値

### <a name="method-disconnect"></a>メソッド disconnect

    public boolean disconnect()

#### <a name="return-value"></a>戻り値

### <a name="method-getcheckedoutfiles"></a>メソッド getCheckedoutFiles

    public container getCheckedoutFiles()

#### <a name="return-value"></a>戻り値

### <a name="method-getconnectioninfo"></a>メソッド getConnectionInfo

    public container getConnectionInfo()

#### <a name="return-value"></a>戻り値

### <a name="method-getvssitem"></a>メソッド getVSSItem

    public VSSItem getVSSItem(str vssItemPath, str localFilePath, [boolean completePath], [int version])

#### <a name="parameters"></a>パラメーター

vssItemPath  

<!-- -->

localFilePath  

<!-- -->

completePath  

<!-- -->

のバージョン  

#### <a name="return-value"></a>戻り値

### <a name="method-init"></a>メソッド init

    public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)

#### <a name="parameters"></a>パラメーター

vssIni  

<!-- -->

vssPrjRoot  

<!-- -->

vssWorkingFolder  

<!-- -->

vssUser  

<!-- -->

vssPwd  

#### <a name="return-value"></a>戻り値

### <a name="method-newsubproject"></a>メソッド newSubProject

    public VSSItem newSubProject(str name, str localPath)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

localPath  

#### <a name="return-value"></a>戻り値

### <a name="method-synchronizeprojects"></a>メソッド synchronizeProjects

    public Map synchronizeProjects([Set projects], [boolean force], [boolean delLocalFiles], [str label])

#### <a name="parameters"></a>パラメーター

プロジェクト  

<!-- -->

force  

<!-- -->

delLocalFiles  

<!-- -->

ラベル  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

VSS クラスのインスタンスを初期化します。

    public void new()

## <a name="class-vssitem"></a>クラス VSSItem
    class VSSItem extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                               | 説明                                      |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| public boolean add(\[boolean keepCheckedout\], \[str comment\])                      |                                                  |
| public boolean checkin(\[str comment\])                                              |                                                  |
| public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\]) |                                                  |
| public boolean delete()                                                              |                                                  |
| public boolean destroy()                                                             |                                                  |
| public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\]) |                                                  |
| public str getActionText()                                                           |                                                  |
| public container getCheckedOutTo()                                                   |                                                  |
| public int getCheckoutVersion()                                                      |                                                  |
| public container getHistory()                                                        |                                                  |
| public ComInterface getIUnknown()                                                    |                                                  |
| public int getVersionNo()                                                            |                                                  |
| public str getVSSPath()                                                              |                                                  |
| public boolean isCheckedOut()                                                        |                                                  |
| public boolean isRenamed()                                                           |                                                  |
| public str name(str newName)                                                         |                                                  |
| public boolean rename(str newName)                                                   |                                                  |
| public boolean undoCheckout()                                                        |                                                  |
| private void new()                                                                   | VSSItem クラスの新しいインスタンスを初期化します。 |

### <a name="method-add"></a>メソッド add

    public boolean add([boolean keepCheckedout], [str comment])

#### <a name="parameters"></a>パラメーター

keepCheckedout  

<!-- -->

comment  

#### <a name="return-value"></a>戻り値

### <a name="method-checkin"></a>メソッド checkin

    public boolean checkin([str comment])

#### <a name="parameters"></a>パラメーター

comment  

#### <a name="return-value"></a>戻り値

### <a name="method-checkout"></a>メソッド checkout

    public boolean checkout([boolean allowMultipleCheckout], [boolean replaceLocal])

#### <a name="parameters"></a>パラメーター

allowMultipleCheckout  

<!-- -->

replaceLocal  

#### <a name="return-value"></a>戻り値

### <a name="method-delete"></a>メソッド delete

    public boolean delete()

#### <a name="return-value"></a>戻り値

### <a name="method-destroy"></a>メソッド destroy

    public boolean destroy()

#### <a name="return-value"></a>戻り値

### <a name="method-get"></a>メソッド get

    public Map get([boolean force], [int version], [str label], [str localFile])

#### <a name="parameters"></a>パラメーター

force  

<!-- -->

のバージョン  

<!-- -->

ラベル  

<!-- -->

localFile  

#### <a name="return-value"></a>戻り値

### <a name="method-getactiontext"></a>メソッド getActionText

    public str getActionText()

#### <a name="return-value"></a>戻り値

### <a name="method-getcheckedoutto"></a>メソッド getCheckedOutTo

    public container getCheckedOutTo()

#### <a name="return-value"></a>戻り値

### <a name="method-getcheckoutversion"></a>メソッド getCheckoutVersion

    public int getCheckoutVersion()

#### <a name="return-value"></a>戻り値

### <a name="method-gethistory"></a>メソッド getHistory

    public container getHistory()

#### <a name="return-value"></a>戻り値

### <a name="method-getiunknown"></a>メソッド getIUnknown

    public ComInterface getIUnknown()

#### <a name="return-value"></a>戻り値

### <a name="method-getversionno"></a>メソッド getVersionNo

    public int getVersionNo()

#### <a name="return-value"></a>戻り値

### <a name="method-getvsspath"></a>メソッド getVSSPath

    public str getVSSPath()

#### <a name="return-value"></a>戻り値

### <a name="method-ischeckedout"></a>メソッド isCheckedOut

    public boolean isCheckedOut()

#### <a name="return-value"></a>戻り値

### <a name="method-isrenamed"></a>メソッド isRenamed

    public boolean isRenamed()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name(str newName)

#### <a name="parameters"></a>パラメーター

newName  

#### <a name="return-value"></a>戻り値

### <a name="method-rename"></a>メソッド rename

    public boolean rename(str newName)

#### <a name="parameters"></a>パラメーター

newName  

#### <a name="return-value"></a>戻り値

### <a name="method-undocheckout"></a>メソッド undoCheckout

    public boolean undoCheckout()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

VSSItem クラスの新しいインスタンスを初期化します。

    private void new()



