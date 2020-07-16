---
title: ProjectNode クラス
description: このトピックでは、ProjectNode クラスについて説明します。
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
ms.openlocfilehash: 664126a7be58f23dab115dde8de5932f1284cfe9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502872"
---
# <a name="class-projectnode"></a>クラス ProjectNode

[!include [banner](../../includes/banner.md)]

```xpp
class ProjectNode extends TreeNode
```

ProjectNode クラスは、AOT プロジェクトの動作を制御します。

## <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 このクラスから拡張して、新しいユーザー定義の AOT プロジェクトを作成します。 このクラスのメソッドを上書きすることによって、プロジェクトの動作を制御します。 Web プロジェクトとヘルプ プロジェクトの両方を作成するには、ProjectNode クラスを拡張するクラスを作成します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str addContextMenuItems()                                                             | プロジェクト ノードのショートカット メニューに品目のリストを追加します。                                                                                |
| public str changedBy(\[str value\])                                                          | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])                                                      | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])                                                        | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])                                                          | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])                                                     | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])                                                       |                                                                                                                                               |
| public str export(str buffer)                                                                |                                                                                                                                               |
| public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\]) | 特定の要素のプロジェクトまたはグループを検索します。                                                                                         |
| public str getProjectClassName()                                                             | プロジェクトの classid に対応するクラスの名前を返します。                                                                    |
| public ProjectNode getRunNode()                                                              | プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。  |
| public str import(str buffer)                                                                |                                                                                                                                               |
| public boolean isRunNode()                                                                   |                                                                                                                                               |
| public ProjectNode loadForInspection()                                                       | プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。                                                               |
| public str name(\[str value\])                                                               | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                                                           |                                                                                                                                               |
| public boolean removeFromProject(TreeNode node)                                              |                                                                                                                                               |
| public str tooltipText(TreeNode node)                                                        |                                                                                                                                               |
| ::public static str projectType()                                                            |                                                                                                                                               |
| public void lockUpdate()                                                                     | 一連のアクションを実行中に、視覚的な更新を禁止します。                                                                         |
| public void addSpecialOverlayIcon(str path, int resId, \[int xOffset\], \[int yOffset\])     |                                                                                                                                               |
| public void created(str name)                                                                | プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。                                     |
| public void setSpecialIcon(int type, str name, int resId)                                    | プロジェクト内の特定のノードに別のアイコンを割り当てます。                                                                                   |
| public void loadProject(str buffer)                                                          | プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。                                                |
| public void saveProject(str buffer)                                                          | アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。                                                      |
| public void unlockUpdate()                                                                   | lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。                                                                    |
| public void handleContextMenuItem(int id)                                                    | ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。                  |
| public void addNode(TreeNode node)                                                           | プロジェクトに既存のノードを追加します。                                                                                                         |
| public void addUtilNode(UtilElementType type, str name)                                      | プロジェクトにノードを追加します。                                                                                                                   |
| public void clear()                                                                          | プロジェクトの内容を削除します。                                                                                                            |
| public void setProjectClass(int classid)                                                     | クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。                                                      |
| public void removeSpecialOverlayIcons(str path)                                              |                                                                                                                                               |
| public void new()                                                                            | ProjectNode クラスの新しいインスタンスを初期化します。                                                                                          |

## <a name="method-addcontextmenuitems"></a>メソッド addContextMenuItems

プロジェクト ノードのショートカット メニューに品目のリストを追加します。

```xpp
public str addContextMenuItems()
```

### <a name="return-value---addcontextmenuitems"></a>戻り値 - addContextMenuItems

追加するメニュー項目のコンマ区切りリスト。

### <a name="remarks---addcontextmenuitems"></a>備考 - addContextMenuItems

プロジェクト ノードのショートカット メニューに品目のリストを追加するには、このメソッドを上書きします。 追加されたメニュー項目の 1 つがユーザーによって選択されると、handleContextMenuItem メソッドが呼び出されます。 適切なアクションを実行するには、このメソッドを上書きします。

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-export"></a>メソッド export

```xpp
public str export(str buffer)
```

### <a name="parameters---export"></a>パラメーター - export

バッファ  

### <a name="return-value---export"></a>戻り値 - export

## <a name="method-findgroupmember"></a>メソッド findGroupMember

特定の要素のプロジェクトまたはグループを検索します。

```xpp
public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])
```

### <a name="parameters---findgroupmember"></a>パラメーター - findGroupMember

名前  
検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。

<!-- -->

タイプ  
検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。

<!-- -->

searchSubgroups  
検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。

### <a name="return-value---findgroupmember"></a>戻り値 - findGroupMember

オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---findgroupmember"></a>備考 - findGroupMember

このメソッドは ProjectGroupNode にもあります。

## <a name="method-getprojectclassname"></a>メソッド getProjectClassName

プロジェクトの classid に対応するクラスの名前を返します。

```xpp
public str getProjectClassName()
```

### <a name="return-value---getprojectclassname"></a>戻り値 - getProjectClassName

プロジェクトの classid に対応するクラスの名前。

### <a name="remarks---getprojectclassname"></a>備考 - getProjectClassName

setClassId メソッドは、クラス ID をプロジェクトに割り当てます。

## <a name="method-getrunnode"></a>メソッド getRunNode

プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。

```xpp
public ProjectNode getRunNode()
```

### <a name="return-value---getrunnode"></a>戻り値 - getRunNode

実行中の projectNode。

### <a name="remarks---getrunnode"></a>備考 - getRunNode

[プロジェクト] ウィンドウを開くことがなく実行中の projectNode を取得するには、ProjectNode.loadForInspection メソッドを使用します。

## <a name="method-import"></a>メソッド import

```xpp
public str import(str buffer)
```

### <a name="parameters---import"></a>パラメーター - import

バッファ  

### <a name="return-value---import"></a>戻り値 - import

## <a name="method-isrunnode"></a>メソッド isRunNode

```xpp
public boolean isRunNode()
```

### <a name="return-value---isrunnode"></a>戻り値 - isRunNode

## <a name="method-loadforinspection"></a>メソッド loadForInspection

プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。

```xpp
public ProjectNode loadForInspection()
```

### <a name="return-value---loadforinspection"></a>戻り値 - loadForInspection

読み込まれた projectNode。

### <a name="remarks---loadforinspection"></a>備考 - loadForInspection

[プロジェクト] ウィンドウを開いたときに projectNode を読み込むには、getRunNode メソッドを使用します。

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-removefromproject"></a>メソッド removeFromProject

```xpp
public boolean removeFromProject(TreeNode node)
```

### <a name="parameters---removefromproject"></a>パラメーター - removeFromProject

node  

### <a name="return-value---removefromproject"></a>戻り値 - removeFromProject

## <a name="method-tooltiptext"></a>メソッド tooltipText

```xpp
public str tooltipText(TreeNode node)
```

### <a name="parameters---tooltiptext"></a>パラメーター - tooltipText

node  

### <a name="return-value---tooltiptext"></a>戻り値 - tooltipText

## <a name="method-projecttype"></a>メソッド projectType

```xpp
public static str projectType()
```

### <a name="return-value---projecttype"></a>戻り値 - projectType

## <a name="method-lockupdate"></a>メソッド lockUpdate

一連のアクションを実行中に、視覚的な更新を禁止します。

```xpp
public void lockUpdate()
```

### <a name="remarks---lockupdate"></a>備考 - lockUpdate

一連のアクションの後にビジュアル アップデートを実行するには、unlockUpdate を呼び出します。

## <a name="method-addspecialoverlayicon"></a>メソッド addSpecialOverlayIcon

```xpp
public void addSpecialOverlayIcon(str path, int resId, [int xOffset], [int yOffset])
```

### <a name="parameters---addspecialoverlayicon"></a>パラメーター - addSpecialOverlayIcon

path  

<!-- -->

resId  

<!-- -->

xOffset  

<!-- -->

yOffset  

## <a name="method-created"></a>メソッド created

プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。

```xpp
public void created(str name)
```

### <a name="parameters---created"></a>パラメーター - created

名前  
プロジェクト インスタンスの名前。

### <a name="remarks---created"></a>備考 - created

このメソッドは、プロジェクトの新しいインスタンスが作成されるときに呼び出されます。 プロジェクトでカスタム アクションを実行するには、このメソッドを上書きします。

## <a name="method-setspecialicon"></a>メソッド setSpecialIcon

プロジェクト内の特定のノードに別のアイコンを割り当てます。

```xpp
public void setSpecialIcon(int type, str name, int resId)
```

### <a name="parameters---setspecialicon"></a>パラメーター - setSpecialIcon

タイプ  
指定されたノードに使用する必要があるアイコンの ID。

<!-- -->

名前  
指定されたノードに使用する必要があるアイコンの ID。

<!-- -->

resId  
指定されたノードに使用する必要があるアイコンの ID。

## <a name="method-loadproject"></a>メソッド loadProject

プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。

```xpp
public void loadProject(str buffer)
```

### <a name="parameters---loadproject"></a>パラメーター - loadProject

バッファ  
saveProject によってプロジェクトに保存されたカスタム データを含む文字列。

### <a name="remarks---loadproject"></a>備考 - loadProject

このメソッドは、プロジェクトが読み込まれたときに呼び出されます。 saveProject および loadProject を上書きすることにより、ユーザーはカスタム データをプロジェクト定義に保存して取得できます。 読み込みを続行するには、プロジェクトの super() を呼び出す必要があります。

## <a name="method-saveproject"></a>メソッド saveProject

アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。

```xpp
public void saveProject(str buffer)
```

### <a name="parameters---saveproject"></a>パラメーター - saveProject

バッファ  
データをパッキングするために使用する必要がある文字列バッファ。 その後、バッファ はsuper() に渡されなければなりません。

### <a name="remarks---saveproject"></a>備考 - saveProject

このメソッドを上書きすることにより、アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データを保存できます。 データは「&lt;APPDATA&gt; ... &lt;/APPDATA&gt;」の形式で XML 文字列として形成することをお勧めします。このデータは loadProject メソッドをオーバーライドして取得できます。

## <a name="method-unlockupdate"></a>メソッド unlockUpdate

lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。

```xpp
public void unlockUpdate()
```

## <a name="method-handlecontextmenuitem"></a>メソッド handleContextMenuItem

ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。

```xpp
public void handleContextMenuItem(int id)
```

### <a name="parameters---handlecontextmenuitem"></a>パラメーター - handleContextMenuItem

id  
メニュー項目の ID。 これは、addContextMenuItems メソッドによって設定されたリスト内の 0 から始まる数値です。 accContextMenuItems が文字列である "item1,item2" を返し、ユーザーがショートカット メニューの品目である "item2" を選択した場合、この方法では値 1 を使用します。

### <a name="remarks---handlecontextmenuitem"></a>備考 - handleContextMenuItem

このメソッドは、ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するときに呼び出されます。

## <a name="method-addnode"></a>メソッド addNode

プロジェクトに既存のノードを追加します。

```xpp
public void addNode(TreeNode node)
```

### <a name="parameters---addnode"></a>パラメーター - addNode

node  
追加するノード。

## <a name="method-addutilnode"></a>メソッド addUtilNode

プロジェクトにノードを追加します。

```xpp
public void addUtilNode(UtilElementType type, str name)
```

### <a name="parameters---addutilnode"></a>パラメーター - addUtilNode

タイプ  
ノードの名前。

<!-- -->

名前  
ノードの名前。

### <a name="remarks---addutilnode"></a>備考 - addUtilNode

この関数は ProjectGroupNode にもあります。

## <a name="method-clear"></a>メソッド clear

プロジェクトの内容を削除します。

```xpp
public void clear()
```

### <a name="remarks---clear"></a>備考 - clear

このメソッドは、アプリケーション オブジェクト ツリー (AOT) からプロジェクトの内容を削除しません。�プロジェクト自体からのみです。 このメソッドはプロジェクトの内容を削除しますが、プロジェクト フォルダーは削除しません。 1 回のメソッド呼び出しでプロジェクトとその内容を削除するには、AOTdelete メソッドを使用します。 オブジェクトを AOT から削除するには、AOTdelete メソッドを使用します。

### <a name="examples---clear"></a>例 - clear

次の例では、Project1 プロジェクト内のプライベート フォルダー内のオブジェクトをすべて削除します。

```xpp
static void clearProjectObjects(Args _args) 
    { 
        ProjectNode privatePn; 
        ProjectNode pn; 
        // Navigate to the Private projects folder. 
        privatePn = infolog.projectRootNode().AOTfindChild("Private"); 
        // Get a reference to the project. 
        pn = privatePn.AOTfindChild("Project1"); 
        // Clear the project. 
        pn.clear(); 
    }
```

## <a name="method-setprojectclass"></a>メソッド setProjectClass

クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。

```xpp
public void setProjectClass(int classid)
```

### <a name="parameters---setprojectclass"></a>パラメーター - setProjectClass

classid  
プロジェクトに割り当てるクラスの ID。

### <a name="remarks---setprojectclass"></a>備考 - setProjectClass

指定されたクラスは、projectNode クラスを拡張する必要があります。

## <a name="method-removespecialoverlayicons"></a>メソッド removeSpecialOverlayIcons

```xpp
public void removeSpecialOverlayIcons(str path)
```

### <a name="parameters---removespecialoverlayicons"></a>パラメーター - removeSpecialOverlayIcons

path  

## <a name="method-new"></a>メソッド new

ProjectNode クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

