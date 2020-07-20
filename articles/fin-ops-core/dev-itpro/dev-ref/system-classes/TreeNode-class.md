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
# <a name="class-treenode"></a>クラス TreeNode

[!include [banner](../../includes/banner.md)]

```xpp
class TreeNode extends Object
```

TreeNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内のノードを取得し、表します。

## <a name="remarks"></a>備考

このクラスとそれを拡張するクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API またはこのクラスから派生した API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 TreeNode クラスを使用すると、AOT 内の任意のノードへのハンドルを取得できます。 TreeNode クラスは、AOT内の任意の種類のノードへの参照となることができる一般的なクラスです。 このクラスには、AOT のショートカット メニューの一部の機能へのアクセスを提供することに加えて、ツリーで操作するために使用するメソッドも含まれます。 TreeNodeTraverser クラスは、AOT 内のナビゲーションでも役立ちます。 TreeNode::findNode および TreeNode::rootNode メソッドは treeNode オブジェクトを返します。これらのオブジェクトから、その他のノードを操作できます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                              | 説明                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public TreeNode SysObsoleteAttribute(UtilElementName name)                                                                                          |                                                                                                                                                                      |
| public TreeNode SysObsoleteAttribute(str name, Types type)                                                                                          |                                                                                                                                                                      |
| public TreeNode SysObsoleteAttribute()                                                                                                              |                                                                                                                                                                      |
| public TreeNode SysObsoleteAttribute(int nodetype)                                                                                                  |                                                                                                                                                                      |
| public boolean AOTAllowEdit()                                                                                                                       |                                                                                                                                                                      |
| public int AOTbitmapId()                                                                                                                            | ツリー ノードのビットマップのリソース ID を返します。                                                                                                              |
| public int AOTchildNodeCount()                                                                                                                      | 指定されたツリー ノードにある子ノードの数をカウントします。                                                                                                         |
| public boolean SysObsoleteAttribute(\[int flag\], \[boolean forceNoXRef\], \[boolean fastMode\])                                                    |                                                                                                                                                                      |
| public boolean AOTDrop(TreeNode sourcenode, \[TreeNode after\])                                                                                     | 指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。                                                                                           |
| public TreeNode AOTDuplicate()                                                                                                                      |                                                                                                                                                                      |
| public TreeNode AOTfindChild(str name, \[int nodeType\])                                                                                            | このノードの指定した子ノードを検索します。                                                                                                                         |
| public TreeNode AOTfirstChild()                                                                                                                     | ツリー ノードの最初の子ノードを取得します。                                                                                                                          |
| public TreeNode AOTfirstChildEx(\[boolean loadFullNode\])                                                                                           |                                                                                                                                                                      |
| public int AOTgetExecutableLineCount()                                                                                                              | このノードのコードの実行可能な行の数を返します。                                                                                                        |
| public Set AOTgetExecutableLines()                                                                                                                  | このノードのコードの実行可能な行を返します。                                                                                                                  |
| public int AOTGetModel()                                                                                                                            |                                                                                                                                                                      |
| public str AOTgetProperties(\[boolean includeInvisible\], \[boolean includeReadOnly\], \[boolean includeNonExportable\])                            | ツリー ノードのプロパティを含む文字列を返します。                                                                                                         |
| public Struct AOTgetPropertiesExt(\[str filter\])                                                                                                   |                                                                                                                                                                      |
| public AnyType AOTgetProperty(str name)                                                                                                             |                                                                                                                                                                      |
| public str AOTgetSource()                                                                                                                           | このノードのソース コードを返します。                                                                                                                                |
| public boolean AOTIncludeInCompare()                                                                                                                |                                                                                                                                                                      |
| public boolean AOTIsDirty()                                                                                                                         |                                                                                                                                                                      |
| public boolean AOTIsOld()                                                                                                                           | このノードが、古いモデル ストアにあるファイルのものかどうかを示します。                                                                                             |
| public boolean AOTIsPersisted()                                                                                                                     | このノードがモデル ストアに保持されているかどうかを示します。                                                                                                   |
| public boolean AOTIsProxyNode()                                                                                                                     |                                                                                                                                                                      |
| public TreeNodeIterator AOTiterator()                                                                                                               | ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。                                                                                     |
| public KernelHelpType AOTKernelHelpType()                                                                                                           |                                                                                                                                                                      |
| public UtilEntryLevel AOTLayer()                                                                                                                    | ツリー ノードのレイヤーを返します。                                                                                                                                  |
| public Set AOTLayers(\[boolean old\])                                                                                                               | そのツリー ノードで定義されているレイヤーのコレクションを返します。                                                                                                      |
| public str AOTname()                                                                                                                                | ノードの name プロパティの値を返します。                                                                                                                  |
| public int AOTnewWindow()                                                                                                                           | ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。                                                                                                          |
| public TreeNode AOTnextSibling()                                                                                                                    | ツリー ノードと同じレベルにある次のノードを返します。                                                                                                            |
| public boolean AOTObjectNode()                                                                                                                      | ノードがアプリケーション オブジェクトであるかどうかを示します。                                                                                                                 |
| public int AOToverlayBitmapId()                                                                                                                     | このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。                                                                                         |
| public TreeNode AOTparent()                                                                                                                         | ツリー ノードの親ノードを返します。                                                                                                                            |
| public TreeNode AOTprevious()                                                                                                                       | このツリー ノードの前の兄弟を返します。                                                                                                                      |
| public boolean SysObsoleteAttribute(str name)                                                                                                       |                                                                                                                                                                      |
| public str AOTtoolTip()                                                                                                                             | そのツリー ノードに関連付けられているツールヒントを返します。                                                                                                                  |
| public str AOTToString()                                                                                                                            |                                                                                                                                                                      |
| public str AOTtypeStr()                                                                                                                             | XPO ファイルで使用される要素タイプの文字列の内部コードを返します。                                                                                             |
| public UtilFileType AOTUtilFileType()                                                                                                               | TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。 UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。 |
| public int applObjectId()                                                                                                                           | 該当する場合は、アプリケーション オブジェクト ID を返します。                                                                                                                    |
| public int applObjectLayerMask()                                                                                                                    | この要素を含むレイヤーを指定するビットを返します。                                                                                                  |
| public int applObjectOldLayerMask()                                                                                                                 | ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。                                                                      |
| public TreeNode getNodeInLayer(UtilEntryLevel layer, \[boolean old\])                                                                               | 指定したレイヤーからツリー ノードのバージョンを取得します。                                                                                                         |
| public Int64 hashKey()                                                                                                                              |                                                                                                                                                                      |
| public TreeNode makeCopy()                                                                                                                          |                                                                                                                                                                      |
| public str newObjectName(\[str oldName\])                                                                                                           | 新しい要素の名前を含む文字列を返します。                                                                                                          |
| public str toString()                                                                                                                               | 現在のオブジェクトを表す文字列を返します。                                                                                                                 |
| public str treeNodeName()                                                                                                                           | ツリー ノードの名前を返します。                                                                                                                                   |
| public str treeNodePath()                                                                                                                           | アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。                                                                                   |
| public TreeNodeType treeNodeType()                                                                                                                  | ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。                                                                |
| public int updateNodePermissions(boolean throwExceptions)                                                                                           |                                                                                                                                                                      |
| public UtilElements utilElement()                                                                                                                   | ノードに関連する UtilElements レコードを返します。                                                                                                           |
| public UtilIdElements utilIdElement()                                                                                                               | ノードに関連する UtilIdElements レコードを返します。                                                                                                         |
| public boolean validateNameCharacters(str name)                                                                                                     |                                                                                                                                                                      |
| ::public static TreeNode findNode(str path)                                                                                                         | アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。                                                                                                       |
| ::public static str generateObjectName(str template)                                                                                                |                                                                                                                                                                      |
| ::public static int getMaximumNodeNameLength(int modelElementTypeId)                                                                                |                                                                                                                                                                      |
| ::public static boolean isNodeReferenceValid(TreeNode treeNode)                                                                                     |                                                                                                                                                                      |
| ::public static boolean isValidObjectName(str name)                                                                                                 | 引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。                                           |
| ::public static TreeNode rootNode()                                                                                                                 | AOT のルート ノードを返します。                                                                                                                                    |
| public void SysObsoleteAttribute()                                                                                                                  |                                                                                                                                                                      |
| public void treeNodeRelease()                                                                                                                       | ツリー ノードが明示的に解放されます。                                                                                                                                   |
| public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, \[XRefReference xrefRef\], \[ClassId parentTypeId\]) |                                                                                                                                                                      |
| public void AOTrun()                                                                                                                                | アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。                                                                                             |
| public void SysObsoleteAttribute()                                                                                                                  |                                                                                                                                                                      |
| public void AOTrefresh()                                                                                                                            | .aod ファイルを最新版に変更することによりノードを更新します。                                                                                                         |
| public void SysObsoleteAttribute(Struct struct1)                                                                                                    |                                                                                                                                                                      |
| public void SysObsoleteAttribute(str properties)                                                                                                    |                                                                                                                                                                      |
| public void AOTconfigure()                                                                                                                          |                                                                                                                                                                      |
| public void AOTload()                                                                                                                               | オブジェクトが読み込み済みであるか確認します。                                                                                                                                   |
| public void treeNodeExport(str filename, \[int flag\])                                                                                              | アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。                                                                                            |
| public void SysObsoleteAttribute(str source, \[boolean isStatic\])                                                                                  |                                                                                                                                                                      |
| public void AOTendXref()                                                                                                                            |                                                                                                                                                                      |
| public void AOTmessageLine(str text, int linenumber)                                                                                                | アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。                                                                                                     |
| public void SysObsoleteAttribute(str name, AnyType value)                                                                                           |                                                                                                                                                                      |
| public void AOTrestore(\[boolean forceReload\])                                                                                                     | 該当する場合は、ディスクからこのノードを再読み込みします。                                                                                                                      |
| public void AOTregenerate()                                                                                                                         |                                                                                                                                                                      |
| public void AOTmakeXref(\[int flag\], \[boolean xRefAll\])                                                                                          | このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。                                                                                  |
| public void AOTedit(\[int Line\], \[int Column\])                                                                                                   | このノードの適切なエディタを開きます。                                                                                                                          |
| public void AOTshowProperties()                                                                                                                     | プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。                                                                               |
| public void AOTinsert(TreeNode parent, \[TreeNode after\], \[boolean doNotDuplicate\])                                                              | このノードのサブノード間にノードを挿入します。                                                                                                                      |
| public void new()                                                                                                                                   | TreeNode クラスの新しいインスタンスを初期化します。                                                                                                                    |
| public void AOTMove(TreeNode parent, \[TreeNode after\])                                                                                            |                                                                                                                                                                      |
| public void SysObsoleteAttribute(int modelId)                                                                                                       |                                                                                                                                                                      |

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public TreeNode SysObsoleteAttribute(UtilElementName name)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

名前  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public TreeNode SysObsoleteAttribute(str name, Types type)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

名前  

<!-- -->

タイプ  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public TreeNode SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public TreeNode SysObsoleteAttribute(int nodetype)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

nodetype  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-aotallowedit"></a>メソッド AOTAllowEdit

```xpp
public boolean AOTAllowEdit()
```

### <a name="return-value---aotallowedit"></a>戻り値 - AOTAllowEdit

## <a name="method-aotbitmapid"></a>メソッド AOTbitmapId

ツリー ノードのビットマップのリソース ID を返します。

```xpp
public int AOTbitmapId()
```

### <a name="return-value---aotbitmapid"></a>戻り値 - AOTbitmapId

ツリー ノードのビットマップのリソース ID。

### <a name="examples---aotbitmapid"></a>例 - AOTbitmapId

次の例では、アプリケーション オブジェクト ツリー (AOT) 内の拡張データ型ノードのリソース ID を出力します。

```xpp
AOT 
static void myJobAOTbitmapId(Args _args) 
{ 
    treeNode treeNode = TreeNode::findNode(#ExtendedDataTypesPath); 
    print treeNode.AOTbitmapId(); 
    pause; 
}
```

このジョブは整数 895 を出力します。 チュートリアルのリソース フォームを実行すると、ビットマップを参照し、それが AOT 内での拡張データ型に使用されるものと同じであることが分かります。

## <a name="method-aotchildnodecount"></a>メソッド AOTchildNodeCount

指定されたツリー ノードにある子ノードの数をカウントします。

```xpp
public int AOTchildNodeCount()
```

### <a name="return-value---aotchildnodecount"></a>戻り値 - AOTchildNodeCount

ツリー ノードの子ノードの数を示す整数。

### <a name="examples---aotchildnodecount"></a>例 - AOTchildNodeCount

次の例では、アプリケーション オブジェクト ツリー (AOT) のメニュー アイテム ノードの下に表示される子ノードの数を出力します。

```xpp
AOT 
static void myJobAOTchildNodeCount(Args _args) 
{ 
    treeNode treeNode = TreeNode::findNode(#MenuItemsPath); 
    print "Number of nodes below Menu Items: ", treeNode.AOTchildNodeCount(); 
    pause; 
}
```

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public boolean SysObsoleteAttribute([int flag], [boolean forceNoXRef], [boolean fastMode])
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

flag  

<!-- -->

forceNoXRef  

<!-- -->

fastMode  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-aotdrop"></a>メソッド AOTDrop

指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。

```xpp
public boolean AOTDrop(TreeNode sourcenode, [TreeNode after])
```

### <a name="parameters---aotdrop"></a>パラメーター - AOTDrop

sourcenode  
ソースが後で挿入されるツリー ノードの子ノード (オプション)。

<!-- -->

以後  
ソースが後で挿入されるツリー ノードの子ノード (オプション)。

### <a name="return-value---aotdrop"></a>戻り値 - AOTDrop

ドロップ操作が成功した場合は true。それ以外の場合は、false。

### <a name="examples---aotdrop"></a>例 - AOTDrop

次の例では、tutorial\_Form\_Controls フォームの underTab:Tab の最後のノードとして、tabPage:CopyOfContainers ツリー ノードを作成します。

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

## <a name="method-aotduplicate"></a>メソッド AOTDuplicate

```xpp
public TreeNode AOTDuplicate()
```

### <a name="return-value---aotduplicate"></a>戻り値 - AOTDuplicate

## <a name="method-aotfindchild"></a>メソッド AOTfindChild

このノードの指定した子ノードを検索します。

```xpp
public TreeNode AOTfindChild(str name, [int nodeType])
```

### <a name="parameters---aotfindchild"></a>パラメーター - AOTfindChild

名前  

<!-- -->

nodeType  

### <a name="return-value---aotfindchild"></a>戻り値 - AOTfindChild

指定した TreeNode。

## <a name="method-aotfirstchild"></a>メソッド AOTfirstChild

ツリー ノードの最初の子ノードを取得します。

```xpp
public TreeNode AOTfirstChild()
```

### <a name="return-value---aotfirstchild"></a>戻り値 - AOTfirstChild

ツリー ノードの最初の子ノード。

## <a name="method-aotfirstchildex"></a>メソッド AOTfirstChildEx

```xpp
public TreeNode AOTfirstChildEx([boolean loadFullNode])
```

### <a name="parameters---aotfirstchildex"></a>パラメーター - AOTfirstChildEx

loadFullNode  

### <a name="return-value---aotfirstchildex"></a>戻り値 - AOTfirstChildEx

## <a name="method-aotgetexecutablelinecount"></a>メソッド AOTgetExecutableLineCount

このノードのコードの実行可能な行の数を返します。

```xpp
public int AOTgetExecutableLineCount()
```

### <a name="return-value---aotgetexecutablelinecount"></a>戻り値 - AOTgetExecutableLineCount

存在する場合のこのノードの実行可能コード行数。存在しない場合は、ゼロ。

### <a name="remarks---aotgetexecutablelinecount"></a>備考 - AOTgetExecutableLineCount

この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。

## <a name="method-aotgetexecutablelines"></a>メソッド AOTgetExecutableLines

このノードのコードの実行可能な行を返します。

```xpp
public Set AOTgetExecutableLines()
```

### <a name="return-value---aotgetexecutablelines"></a>戻り値 - AOTgetExecutableLines

このノードに実行可能なコード行が含まれているセット オブジェクト; それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---aotgetexecutablelines"></a>備考 - AOTgetExecutableLines

この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。

## <a name="method-aotgetmodel"></a>メソッド AOTGetModel

```xpp
public int AOTGetModel()
```

### <a name="return-value---aotgetmodel"></a>戻り値 - AOTGetModel

## <a name="method-aotgetproperties"></a>メソッド AOTgetProperties

ツリー ノードのプロパティを含む文字列を返します。

```xpp
public str AOTgetProperties([boolean includeInvisible], [boolean includeReadOnly], [boolean includeNonExportable])
```

### <a name="parameters---aotgetproperties"></a>パラメーター - AOTgetProperties

includeInvisible  

<!-- -->

includeReadOnly  

<!-- -->

includeNonExportable  

### <a name="return-value---aotgetproperties"></a>戻り値 - AOTgetProperties

ツリー ノードのプロパティを含む文字列。

### <a name="examples---aotgetproperties"></a>例 - AOTgetProperties

次の例では、一時テーブルのリストを示します。

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

## <a name="method-aotgetpropertiesext"></a>メソッド AOTgetPropertiesExt

```xpp
public Struct AOTgetPropertiesExt([str filter])
```

### <a name="parameters---aotgetpropertiesext"></a>パラメーター - AOTgetPropertiesExt

フィルター  

### <a name="return-value---aotgetpropertiesext"></a>戻り値 - AOTgetPropertiesExt

## <a name="method-aotgetproperty"></a>メソッド AOTgetProperty

```xpp
public AnyType AOTgetProperty(str name)
```

### <a name="parameters---aotgetproperty"></a>パラメーター - AOTgetProperty

名前  

### <a name="return-value---aotgetproperty"></a>戻り値 - AOTgetProperty

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---aotgetsource"></a>備考 - AOTgetSource

この関数はソース コードを持つノードによってオーバーライドされます。

## <a name="method-aotincludeincompare"></a>メソッド AOTIncludeInCompare

```xpp
public boolean AOTIncludeInCompare()
```

### <a name="return-value---aotincludeincompare"></a>戻り値 - AOTIncludeInCompare

## <a name="method-aotisdirty"></a>メソッド AOTIsDirty

```xpp
public boolean AOTIsDirty()
```

### <a name="return-value---aotisdirty"></a>戻り値 - AOTIsDirty

## <a name="method-aotisold"></a>メソッド AOTIsOld

このノードが、古いモデル ストアにあるファイルのものかどうかを示します。

```xpp
public boolean AOTIsOld()
```

### <a name="return-value---aotisold"></a>戻り値 - AOTIsOld

このノードが古いモデル ストアに由来する場合は true。それ以外の場合は、false。

## <a name="method-aotispersisted"></a>メソッド AOTIsPersisted

このノードがモデル ストアに保持されているかどうかを示します。

```xpp
public boolean AOTIsPersisted()
```

### <a name="return-value---aotispersisted"></a>戻り値 - AOTIsPersisted

このノードが保持された場合は true。それ以外の場合は、false。

### <a name="remarks---aotispersisted"></a>備考 - AOTIsPersisted

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isModelElement() メソッドを使用します。

## <a name="method-aotisproxynode"></a>メソッド AOTIsProxyNode

```xpp
public boolean AOTIsProxyNode()
```

### <a name="return-value---aotisproxynode"></a>戻り値 - AOTIsProxyNode

## <a name="method-aotiterator"></a>メソッド AOTiterator

ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。

```xpp
public TreeNodeIterator AOTiterator()
```

### <a name="return-value---aotiterator"></a>戻り値 - AOTiterator

ツリー ノードの子を反復処理するために使用する TreeNodeIterator オブジェクト。

## <a name="method-aotkernelhelptype"></a>メソッド AOTKernelHelpType

```xpp
public KernelHelpType AOTKernelHelpType()
```

### <a name="return-value---aotkernelhelptype"></a>戻り値 - AOTKernelHelpType

## <a name="method-aotlayer"></a>メソッド AOTLayer

ツリー ノードのレイヤーを返します。

```xpp
public UtilEntryLevel AOTLayer()
```

### <a name="return-value---aotlayer"></a>戻り値 - AOTLayer

このノードが存在するレイヤー。

### <a name="remarks---aotlayer"></a>備考 - AOTLayer

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。

## <a name="method-aotlayers"></a>メソッド AOTLayers

そのツリー ノードで定義されているレイヤーのコレクションを返します。

```xpp
public Set AOTLayers([boolean old])
```

### <a name="parameters---aotlayers"></a>パラメーター - AOTLayers

old  
古いモデル ストアからツリー ノード定義のレイヤーを返すかどうかを示すブール値; オプション。

### <a name="return-value---aotlayers"></a>戻り値 - AOTLayers

レイヤーを持つセット オブジェクト。

### <a name="remarks---aotlayers"></a>備考 - AOTLayers

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。

## <a name="method-aotname"></a>メソッド AOTname

ノードの name プロパティの値を返します。

```xpp
public str AOTname()
```

### <a name="return-value---aotname"></a>戻り値 - AOTname

name プロパティの値を含む文字列

### <a name="remarks---aotname"></a>備考 - AOTname

ほとんどの場合、メソッド TreeNodeName と同じ結果が得られます。

### <a name="examples---aotname"></a>例 - AOTname

次の例では、ツリー ノードの最初の子の名前を出力します。

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

## <a name="method-aotnewwindow"></a>メソッド AOTnewWindow

ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。

```xpp
public int AOTnewWindow()
```

### <a name="return-value---aotnewwindow"></a>戻り値 - AOTnewWindow

## <a name="method-aotnextsibling"></a>メソッド AOTnextSibling

ツリー ノードと同じレベルにある次のノードを返します。

```xpp
public TreeNode AOTnextSibling()
```

### <a name="return-value---aotnextsibling"></a>戻り値 - AOTnextSibling

現在のツリー ノードと同じレベルにある次のノード。

## <a name="method-aotobjectnode"></a>メソッド AOTObjectNode

ノードがアプリケーション オブジェクトであるかどうかを示します。

```xpp
public boolean AOTObjectNode()
```

### <a name="return-value---aotobjectnode"></a>戻り値 - AOTObjectNode

ノードがアプリケーション オブジェクトである場合は true。それ以外の場合は false。

### <a name="remarks---aotobjectnode"></a>備考 - AOTObjectNode

フォームまたはレポートは、アプリケーション オブジェクトです。 フォーム、またはその他のサブパートのコントロールはありません。

## <a name="method-aotoverlaybitmapid"></a>メソッド AOToverlayBitmapId

このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。

```xpp
public int AOToverlayBitmapId()
```

### <a name="return-value---aotoverlaybitmapid"></a>戻り値 - AOToverlayBitmapId

このノードに関連付けられた AOT のオーバーレイのリソース ID。

## <a name="method-aotparent"></a>メソッド AOTparent

ツリー ノードの親ノードを返します。

```xpp
public TreeNode AOTparent()
```

### <a name="return-value---aotparent"></a>戻り値 - AOTparent

ツリー ノードの親ノード。

## <a name="method-aotprevious"></a>メソッド AOTprevious

このツリー ノードの前の兄弟を返します。

```xpp
public TreeNode AOTprevious()
```

### <a name="return-value---aotprevious"></a>戻り値 - AOTprevious

同じレベルにある、このツリー ノードの前のツリー ノード。

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public boolean SysObsoleteAttribute(str name)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

名前  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-aottooltip"></a>メソッド AOTtoolTip

そのツリー ノードに関連付けられているツールヒントを返します。

```xpp
public str AOTtoolTip()
```

### <a name="return-value---aottooltip"></a>戻り値 - AOTtoolTip

ツール チップを含む文字列。

## <a name="method-aottostring"></a>メソッド AOTToString

```xpp
public str AOTToString()
```

### <a name="return-value---aottostring"></a>戻り値 - AOTToString

## <a name="method-aottypestr"></a>メソッド AOTtypeStr

XPO ファイルで使用される要素タイプの文字列の内部コードを返します。

```xpp
public str AOTtypeStr()
```

### <a name="return-value---aottypestr"></a>戻り値 - AOTtypeStr

ツリー ノードのタイプを含む文字列。

## <a name="method-aotutilfiletype"></a>メソッド AOTUtilFileType

TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。 UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。

```xpp
public UtilFileType AOTUtilFileType()
```

### <a name="return-value---aotutilfiletype"></a>戻り値 - AOTUtilFileType

ツリー ノードの UtilFileType 列挙値。 可能な値を次の一覧に示します。 UtilFileType::Application は、要素 (フォーム、レポート、クエリ、テーブルなど) が .aod ファイルに保存されていることを意味します。 UtilFileType::ApplicationCodeDocumentation は、要素が .add ファイルに保存されていることを意味します。 UtilFileType::ApplicationHelp は、要素が .ahd ファイルに保存されていることを意味します。 UtilFileType::KernelHelp は、要素が .akh ファイルに保存されていることを意味します。

### <a name="examples---aotutilfiletype"></a>例 - AOTUtilFileType

次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。

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

## <a name="method-applobjectid"></a>メソッド applObjectId

該当する場合は、アプリケーション オブジェクト ID を返します。

```xpp
public int applObjectId()
```

### <a name="return-value---applobjectid"></a>戻り値 - applObjectId

アプリケーション オブジェクトの ID。

## <a name="method-applobjectlayermask"></a>メソッド applObjectLayerMask

この要素を含むレイヤーを指定するビットを返します。

```xpp
public int applObjectLayerMask()
```

### <a name="return-value---applobjectlayermask"></a>戻り値 - applObjectLayerMask

この要素を含むレイヤーを指定するビット。

## <a name="method-applobjectoldlayermask"></a>メソッド applObjectOldLayerMask

ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。

```xpp
public int applObjectOldLayerMask()
```

### <a name="return-value---applobjectoldlayermask"></a>戻り値 - applObjectOldLayerMask

この要素を含むレイヤーを指定するビット。

## <a name="method-getnodeinlayer"></a>メソッド getNodeInLayer

指定したレイヤーからツリー ノードのバージョンを取得します。

```xpp
public TreeNode getNodeInLayer(UtilEntryLevel layer, [boolean old])
```

### <a name="parameters---getnodeinlayer"></a>パラメーター - getNodeInLayer

 レイヤー  
古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。

<!-- -->

old  
古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。

### <a name="return-value---getnodeinlayer"></a>戻り値 - getNodeInLayer

新しい TreeNode。

### <a name="remarks---getnodeinlayer"></a>備考 - getNodeInLayer

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isGetNodeInLayerSupported メソッドを使用します。

## <a name="method-hashkey"></a>メソッド hashKey

```xpp
public Int64 hashKey()
```

### <a name="return-value---hashkey"></a>戻り値 - hashKey

## <a name="method-makecopy"></a>メソッド makeCopy

```xpp
public TreeNode makeCopy()
```

### <a name="return-value---makecopy"></a>戻り値 - makeCopy

## <a name="method-newobjectname"></a>メソッド newObjectName

新しい要素の名前を含む文字列を返します。

```xpp
public str newObjectName([str oldName])
```

### <a name="parameters---newobjectname"></a>パラメーター - newObjectName

oldName  
ノードの新しい名前 (オプション)。 引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。

### <a name="return-value---newobjectname"></a>戻り値 - newObjectName

新しい要素の名前を含む文字列。

### <a name="remarks---newobjectname"></a>備考 - newObjectName

引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。 たとえば、TreeNode に子としてフォームがある場合、引数なしのこのメソッドの呼び出しは「Form1」を返します。 ツリー ノードに複数の子ノードがある場合は、メソッドは "object" という文字列を返します。

### <a name="examples---newobjectname"></a>例 - newObjectName

次の Treenode.newObjectName の呼び出しでは、データ ディクショナリ ノードに複数のオブジェクト型を表す子があるため、「object」が返されます。

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

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。

## <a name="method-treenodename"></a>メソッド treeNodeName

ツリー ノードの名前を返します。

```xpp
public str treeNodeName()
```

### <a name="return-value---treenodename"></a>戻り値 - treeNodeName

ツリー ノードの名前を含む文字列。

## <a name="method-treenodepath"></a>メソッド treeNodePath

アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。

```xpp
public str treeNodePath()
```

### <a name="return-value---treenodepath"></a>戻り値 - treeNodePath

AOT 内のツリー ノードの一意のパスを返します。

### <a name="examples---treenodepath"></a>例 - treeNodePath

次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。

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

## <a name="method-treenodetype"></a>メソッド treeNodeType

ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。

```xpp
public TreeNodeType treeNodeType()
```

### <a name="return-value---treenodetype"></a>戻り値 - treeNodeType

TreeNodeType クラスのインスタンス。

## <a name="method-updatenodepermissions"></a>メソッド updateNodePermissions

```xpp
public int updateNodePermissions(boolean throwExceptions)
```

### <a name="parameters---updatenodepermissions"></a>パラメーター - updateNodePermissions

throwExceptions  

### <a name="return-value---updatenodepermissions"></a>戻り値 - updateNodePermissions

## <a name="method-utilelement"></a>メソッド utilElement

ノードに関連する UtilElements レコードを返します。

```xpp
public UtilElements utilElement()
```

### <a name="return-value---utilelement"></a>戻り値 - utilElement

ノードに関連する UtilElements レコード。

### <a name="remarks---utilelement"></a>備考 - utilElement

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。

## <a name="method-utilidelement"></a>メソッド utilIdElement

ノードに関連する UtilIdElements レコードを返します。

```xpp
public UtilIdElements utilIdElement()
```

### <a name="return-value---utilidelement"></a>戻り値 - utilIdElement

ノードに関連する UtilIdElements レコード。

### <a name="remarks---utilidelement"></a>備考 - utilIdElement

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。

## <a name="method-validatenamecharacters"></a>メソッド validateNameCharacters

```xpp
public boolean validateNameCharacters(str name)
```

### <a name="parameters---validatenamecharacters"></a>パラメーター - validateNameCharacters

名前  

### <a name="return-value---validatenamecharacters"></a>戻り値 - validateNameCharacters

## <a name="method-findnode"></a>メソッド findNode

アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。

```xpp
public static TreeNode findNode(str path)
```

### <a name="parameters---findnode"></a>パラメーター - findNode

path  
検索で使用されるパスを示す文字列。

### <a name="return-value---findnode"></a>戻り値 - findNode

指定されたパスのノードが存在しない場合の、要求された TreeNode オブジェクトまたは nullNothingnullptrunita null 参照 (Visual Basic ではなし)。

### <a name="remarks---findnode"></a>備考 - findNode

TreeNode オブジェクトを取得する別の方法は、Info.getNode メソッドを使用することです。 2 つのメソッド間の重要な違いは、Info.getNode メソッドが AOT から分離されているノードを提供するのに対して一方 findNode メソッドは AOT のノードを返します。 つまり、Info.getNode メソッドから返されるノードは親ノードを持たず、findNode メソッドから返されるノードは親ノードを持ちます。

### <a name="examples---findnode"></a>例 - findNode

次の例では、TreeNode::findNode メソッドが呼び出される時に検出される ツリー ノードの名前を取得します。 この例では、TreeNode.findNode メソッドを呼び出す前に、ユーザーに必要なセキュリティ キーがあるかどうかを確認します。

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

## <a name="method-generateobjectname"></a>メソッド generateObjectName

```xpp
public static str generateObjectName(str template)
```

### <a name="parameters---generateobjectname"></a>パラメーター - generateObjectName

テンプレート  

### <a name="return-value---generateobjectname"></a>戻り値 - generateObjectName

## <a name="method-getmaximumnodenamelength"></a>メソッド getMaximumNodeNameLength

```xpp
public static int getMaximumNodeNameLength(int modelElementTypeId)
```

### <a name="parameters---getmaximumnodenamelength"></a>パラメーター - getMaximumNodeNameLength

modelElementTypeId  

### <a name="return-value---getmaximumnodenamelength"></a>戻り値 - getMaximumNodeNameLength

## <a name="method-isnodereferencevalid"></a>メソッド isNodeReferenceValid

```xpp
public static boolean isNodeReferenceValid(TreeNode treeNode)
```

### <a name="parameters---isnodereferencevalid"></a>パラメーター - isNodeReferenceValid

treeNode  

### <a name="return-value---isnodereferencevalid"></a>戻り値 - isNodeReferenceValid

## <a name="method-isvalidobjectname"></a>メソッド isValidObjectName

引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。

```xpp
public static boolean isValidObjectName(str name)
```

### <a name="parameters---isvalidobjectname"></a>パラメーター - isValidObjectName

名前  
検証するツリー ノードの名前を含む文字列。

### <a name="return-value---isvalidobjectname"></a>戻り値 - isValidObjectName

各条件が一致している場合は true。それ以外の場合は false。

### <a name="remarks---isvalidobjectname"></a>備考 - isValidObjectName

候補者の名前は、次の条件を満たす必要があります:

-   最初の文字は数字、記号ではない文字でなければなりません。
-   文字、数字、またはアンダースコアだけを含めることができます。
-   トークンに対して評価してはなりません。

このメソッドは、同じ名前の要素がすでに存在するかどうかをチェックしません。 これは引数が AOT オブジェクトの有効な名前であることのみを検証します。 重複する名前は、クラス、テーブル、拡張データ型または列挙内では存在しません。

### <a name="examples---isvalidobjectname"></a>例 - isValidObjectName

次の例では、有効な引数と無効な引数の例を示しています。

```xpp
boolean validName; 
validName = TreeNode::isValidObjectName('ValidName'); //true 
validName = TreeNode::isValidObjectName('Name with spaces'); //false 
validName = TreeNode::isValidObjectName('4StartsWithDigit'); //false 
validName = TreeNode::isValidObjectName('Illegal;Character'); //false 
validName = TreeNode::isValidObjectName('if'); // false (token name)
```

## <a name="method-rootnode"></a>メソッド rootNode

AOT のルート ノードを返します。

```xpp
public static TreeNode rootNode()
```

### <a name="return-value---rootnode"></a>戻り値 - rootNode

AOT のルート ノード。

### <a name="remarks---rootnode"></a>備考 - rootNode

このメソッドは、同様の機能を rootNode メソッドに提供します。

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute()
```

## <a name="method-treenoderelease"></a>メソッド treeNodeRelease

ツリー ノードが明示的に解放されます。

```xpp
public void treeNodeRelease()
```

### <a name="remarks---treenoderelease"></a>備考 - treeNodeRelease

ガベージコレクターが自動的にオブジェクトをアンロードするので、通常、オブジェクトを明示的にアンロードする必要はありません。 ただし、ツリー ノードは、通常 AOT にリンクされているため、ガベージ コレクションではありません。 同じ方法で多くのツリー ノードでこのメソッドを実行する場合、リソースを要求する可能性があります。 ガベージ コレクターがツリー ノードを削除できるようにするには、作業中にツリー ノードをアンロードする必要があります。 このメソッドを呼び出す前に、そのツリー ノードとそのサブノードに対するすべての参照を削除してください。 このメソッドを呼び出す必要があるかどうかを判断するには、TreeNode.TreeNodeType().isConsumingMemory メソッドを使用します。

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, [XRefReference xrefRef], [ClassId parentTypeId])
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

名前  

<!-- -->

xrefKind  

<!-- -->

lineNumber  

<!-- -->

columNumber  

<!-- -->

xrefRef  

<!-- -->

parentTypeId  

## <a name="method-aotrun"></a>メソッド AOTrun

アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

```xpp
public void AOTrun()
```

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute()
```

## <a name="method-aotrefresh"></a>メソッド AOTrefresh

.aod ファイルを最新版に変更することによりノードを更新します。

```xpp
public void AOTrefresh()
```

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute(Struct struct1)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

struct1  

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute(str properties)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

プロパティ  

## <a name="method-aotconfigure"></a>メソッド AOTconfigure

```xpp
public void AOTconfigure()
```

## <a name="method-aotload"></a>メソッド AOTload

オブジェクトが読み込み済みであるか確認します。

```xpp
public void AOTload()
```

## <a name="method-treenodeexport"></a>メソッド treeNodeExport

アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。

```xpp
public void treeNodeExport(str filename, [int flag])
```

### <a name="parameters---treenodeexport"></a>パラメーター - treeNodeExport

filename  

<!-- -->

flag  

### <a name="remarks---treenodeexport"></a>備考 - treeNodeExport

攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。

### <a name="examples---treenodeexport"></a>例 - treeNodeExport

この例では、treeNodeExport メソッドを使用して、ExampleClass クラスを .xpo ファイルにエクスポートします。

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

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute(str source, [boolean isStatic])
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

ソース  

<!-- -->

isStatic  

## <a name="method-aotendxref"></a>メソッド AOTendXref

```xpp
public void AOTendXref()
```

## <a name="method-aotmessageline"></a>メソッド AOTmessageLine

アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。

```xpp
public void AOTmessageLine(str text, int linenumber)
```

### <a name="parameters---aotmessageline"></a>パラメーター - AOTmessageLine

テキスト  
無視される整数。 出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。

<!-- -->

linenumber  
無視される整数。 出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。

### <a name="remarks---aotmessageline"></a>備考 - AOTmessageLine

このメソッドは、テキストを出力するために使用されます。そのためユーザーは後でメッセージ ウィンドウ内のそのテキスト行をダブルクリックすると、このノードに関して何らかのアクションが発生します。

### <a name="examples---aotmessageline"></a>例 - AOTmessageLine

次の例では、フォームが TreeNode からこのメソッドを継承するために、フォーム オブジェクトに対して AOTmessageLine メソッドを実行します。

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

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute(str name, AnyType value)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

名前  

<!-- -->

値  

## <a name="method-aotrestore"></a>メソッド AOTrestore

該当する場合は、ディスクからこのノードを再読み込みします。

```xpp
public void AOTrestore([boolean forceReload])
```

### <a name="parameters---aotrestore"></a>パラメーター - AOTrestore

forceReload  

## <a name="method-aotregenerate"></a>メソッド AOTregenerate

```xpp
public void AOTregenerate()
```

## <a name="method-aotmakexref"></a>メソッド AOTmakeXref

このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。

```xpp
public void AOTmakeXref([int flag], [boolean xRefAll])
```

### <a name="parameters---aotmakexref"></a>パラメーター - AOTmakeXref

flag  

<!-- -->

xRefAll  

### <a name="remarks---aotmakexref"></a>備考 - AOTmakeXref

このメソッドは、任意の場所で呼び出すことができます。

-   リスト ノード (AOT、テーブル、フォーム、プロジェクトのルート、およびグループ)
-   アプリケーション オブジェクト (テーブルやフォームなど)
-   メソッドの分岐
-   メソッド

## <a name="method-aotedit"></a>メソッド AOTedit

このノードの適切なエディタを開きます。

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a>パラメーター - AOTedit

折れ線  
カーソル位置の列 (オプション)。

<!-- -->

円柱  
カーソル位置の列 (オプション)。

### <a name="remarks---aotedit"></a>備考 - AOTedit

ノードがメソッドである場合は、コード エディタが開きます。 ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。

### <a name="examples---aotedit"></a>例 - AOTedit

次のコード例は、X++ エディターを開き、クラス Tax のクラス宣言を表示し、ポインタを 6 行目、8 列目に配置します。

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

## <a name="method-aotshowproperties"></a>メソッド AOTshowProperties

プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。

```xpp
public void AOTshowProperties()
```

## <a name="method-aotinsert"></a>メソッド AOTinsert

このノードのサブノード間にノードを挿入します。

```xpp
public void AOTinsert(TreeNode parent, [TreeNode after], [boolean doNotDuplicate])
```

### <a name="parameters---aotinsert"></a>パラメーター - AOTinsert

parent  

<!-- -->

以後  

<!-- -->

doNotDuplicate  

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-aotmove"></a>メソッド AOTMove

```xpp
public void AOTMove(TreeNode parent, [TreeNode after])
```

### <a name="parameters---aotmove"></a>パラメーター - AOTMove

parent  

<!-- -->

以後  

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public void SysObsoleteAttribute(int modelId)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

modelId  

