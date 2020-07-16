---
title: FormControl クラス
description: このトピックでは、FormControl クラスについて説明します。
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
ms.openlocfilehash: 32733802fde280f73fc9b84eaa22a74e7d649cb7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502947"
---
# <a name="class-formcontrol"></a>クラス FormControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormControl extends Object
```

FormControl クラスは、すべてのフォーム コントロールの基本クラスとして機能します。

## <a name="remarks"></a>備考

このクラスのインスタンスは作成しないでください。 代わりに特定のコントロールを使用します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                 | 説明                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                                                                         | コントロールを揃える必要があるかどうかを決定します。                                                                                                                       |
| public boolean allowEdit(\[boolean value\])                                                                                                            | ユーザーがコントロールの内容を修正できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                                                                         | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                                                                      | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int beginDrag(int x, int y)                                                                                                                     | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public FormBuildControl build()                                                                                                                        |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                                                                 | コントロールのサイズを取得します。                                                                                                                                      |
| public FormChangeTracker changeTracker()                                                                                                               |                                                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                                                               | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                                                                       | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public int containerId()                                                                                                                               | コントロールの親コンテナーの ID を取得します。                                                                                                               |
| public str countryRegionCodes(\[str value\])                                                                                                           | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public int currentRow()                                                                                                                                |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                                                             | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public FormDataSource dataSourceObject()                                                                                                               |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                                                                | クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                                                                     | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                    |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                                                                      | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                                                                          | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                                                                  | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean editAutoPostback(\[boolean value\])                                                                                                     |                                                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                                                                                              | オブジェクトが有効か無効かを決定します。                                                                                                                   |
| public str extendedStyle(\[str value\])                                                                                                                |                                                                                                                                                                         |
| public FieldBinding fieldBinding()                                                                                                                     | FieldBinding 派生クラスへのコントロールのテーブルおよびフィールド バインディングを取得します。                                                                                |
| public str formatStr(\[int rowNumber\], \[boolean display\], \[int maxWidth\], \[boolean forceSignWhenDisplaceNegative\], \[boolean formatForExport\]) |                                                                                                                                                                         |
| public xFormRun formRun()                                                                                                                              |                                                                                                                                                                         |
| public FormBinding getBinding(str propertyName)                                                                                                        |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                                                             | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                                                                        | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                                                             | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                                                                   | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                                                                 | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                                                                     | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                         |
| public str hierarchyParent(\[str value\])                                                                                                              | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                                                                      | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public int id()                                                                                                                                        | コントロールの ID を取得します。                                                                                                                                        |
| public boolean isDisplayed()                                                                                                                           | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isEditable()                                                                                                                            |                                                                                                                                                                         |
| public boolean isEnabled()                                                                                                                             |                                                                                                                                                                         |
| public boolean isRestricted()                                                                                                                          | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                                                               | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean isVisible()                                                                                                                             | コントロールが表示されるかどうかを示す値を取得します。                                                                                                        |
| public boolean isVisibleOnClient()                                                                                                                     |                                                                                                                                                                         |
| public str labelText()                                                                                                                                 | コントロールのラベル テキストを取得します。                                                                                                                               |
| public int left(int value, \[int mode\])                                                                                                               | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                                                                     | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean lockWindowUpdate(boolean lock)                                                                                                          | 更新のコントロールのウィンドウをロックまたはロック解除します。                                                                                                                  |
| public boolean markAsUserAdd(\[boolean value\])                                                                                                        | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                                                        | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                                                            | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                                                            | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                                                              | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public str name(\[str value\])                                                                                                                         | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                                                             |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                                                                |                                                                                                                                                                         |
| public FormControl parentControl()                                                                                                                     | コントロールの親コントロールを取得します。                                                                                                                           |
| public str resourceBundleName()                                                                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                                                              | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                                                             | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public str getContextMenuOptions()                                                                                                                     |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                                                                 | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public str templateId()                                                                                                                                |                                                                                                                                                                         |
| public str toolTip()                                                                                                                                   | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                                                                | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                                                                      | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                                                                         |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                                                                    |                                                                                                                                                                         |
| public int updateWindow()                                                                                                                              | コントロールのウィンドウを更新します。                                                                                                                                     |
| public int userData(\[int value\])                                                                                                                     | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                                                                 | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                                                                | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                                                                  | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                                                                   | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                                                                     | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                                                             | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                                                               | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                                                               | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                                                            | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                                                                     | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                                                                    | ピクセル単位でコントロールの幅を設定するか返します。                                                                                                                     |
| public str valueStr()                                                                                                                                  | 文字列形式のコントロールの値を取得します。                                                                                                                    |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                                                           | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                                                                 | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                                                                         | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                                                              | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                                                              | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                                                                    | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void displayControl()                                                                                                                           | コントロールを表示します。                                                                                                                                                   |
| public void copy()                                                                                                                                     | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void paste()                                                                                                                                    | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void setFocus()                                                                                                                                 | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void cut()                                                                                                                                      | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void gotFocus()                                                                                                                                 | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void dragLeave()                                                                                                                                | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void lostFocus()                                                                                                                                | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void inputSearch(str searchStr)                                                                                                                 | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void setTemplateId(\[str value\])                                                                                                               |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                                                                      | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void update()                                                                                                                                   | コントロールを更新します。                                                                                                                                                    |
| public void run()                                                                                                                                      |                                                                                                                                                                         |
| public void lock()                                                                                                                                     | フォーム コントロールをロックします。                                                                                                                                                 |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                                                                          | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void applyBuild()                                                                                                                               |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                                                              | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void resetUserSetting()                                                                                                                         | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void new(FormBuildControl build, xFormRun formRun)                                                                                              |                                                                                                                                                                         |
| public void context()                                                                                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void unLock(boolean update)                                                                                                                     | フォーム コントロールのロックを解除します。                                                                                                                                                 |
| public void setResourceBundleName(\[str value\])                                                                                                       |                                                                                                                                                                         |
| public void selectedMenuOption(int selectedOption)                                                                                                     |                                                                                                                                                                         |
| public void mouseLeave()                                                                                                                               | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void onPropChanged(\[str propName\])                                                                                                            |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                                                                  | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void initialize()                                                                                                                               |                                                                                                                                                                         |
| public void endDrag()                                                                                                                                  | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |

## <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを揃える必要があるかどうかを決定します。

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a>パラメーター - alignControl

値  
プロパティの新しい値 (オプション)。

### <a name="return-value---aligncontrol"></a>戻り値 - alignControl

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

### <a name="remarks---aligncontrol"></a>備考 - alignControl

コントロールの左上隅は、最も長いラベルに基づいて配置されます。

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を修正できるかどうかを決定します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  
allowEdit プロパティに割り当てる値。

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを変更することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="examples---allowedit"></a>例 - allowEdit

次の例は、allowEdit プロパティの値を返して設定する方法を示しています。

```xpp
// Return the value. 
info (strfmt("allowEdit: %1", this.allowEdit())); 
// Set the value. 
this.allowEdit(false);
```

## <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a>戻り値 - allowSysSetup

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  
値が指定されている場合は、プロパティを設定する値。

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

### <a name="remarks---autodeclaration"></a>備考 - autoDeclaration

コントロールには同じ名前を付けることはできません。

## <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a>パラメーター - beginDrag

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

### <a name="return-value---begindrag"></a>戻り値 - beginDrag

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---begindrag"></a>備考 - beginDrag

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="examples---begindrag"></a>例 - beginDrag

次の例では、ユーザーがフォーム コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。

```xpp
public int beginDrag(int _x, int _y) 
{ 
    int ret; 
    info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
    ret = super(_x, _y); 
    return ret; 
}
```

## <a name="method-build"></a>メソッド build

```xpp
public FormBuildControl build()
```

### <a name="return-value---build"></a>戻り値 - build

## <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a>パラメーター - calcControlSize

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

### <a name="return-value---calccontrolsize"></a>戻り値 - calcControlSize

幅と高さを保持するコンテナー。

## <a name="method-changetracker"></a>メソッド changeTracker

```xpp
public FormChangeTracker changeTracker()
```

### <a name="return-value---changetracker"></a>戻り値 - changeTracker

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  
コントロールに割り当てるコンフィギュレーション キーの ID。オプション。

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーション キーの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="examples---configurationkey"></a>例 - configurationKey

次の例は、コントロールのコンフィギュレーション キーを設定して取得する方法を示しています。

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
// objCtrl previously assigned. 
// Assign a configuration key to the control. 
objCtrl.configurationKey(configurationkeynum(BankDeposit)); 
// Retrieve the configuration key ID from the control. 
cki = objCtrl.configurationKey(); 
if (cki != 0) 
{ 
    dck = new DictConfigurationKey(cki); 
    if (dck) 
    { 
    print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                  cki, 
                  dck.name()); 
    } 
}
```

## <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a>戻り値 - configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

### <a name="remarks---configurationkeyex"></a>備考 - configurationKeyEx

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="examples---configurationkeyex"></a>例 - configurationKeyEx

次の例は、コントロールのコンフィギュレーション キー ID を取得する方法を示しています。

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
List list; 
ListEnumerator enum; 
// objCtrl previously assigned. 
list = objCtrl.configurationKeyEx(); 
if (0 != list.elements()) 
{ 
    enum = list.getEnumerator(); 
    while (enum.moveNext()) 
    { 
       dck = new DictConfigurationKey(enum.current()); 
       if (dck) 
       { 
        print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                     enum.current(), 
                     dck.name() ); 
       } 
    } 
}
```

## <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a>戻り値 - containerId

親コンテナーの ID。

## <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a>パラメーター - countryRegionCodes

値  
設定する国/地域コードを含む文字列 (オプション)。

### <a name="return-value---countryregioncodes"></a>戻り値 - countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリスト。

## <a name="method-currentrow"></a>メソッド currentRow

```xpp
public int currentRow()
```

### <a name="return-value---currentrow"></a>戻り値 - currentRow

## <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a>パラメーター - dataRelationPath

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

### <a name="return-value---datarelationpath"></a>戻り値 - dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

### <a name="remarks---datarelationpath"></a>備考 - dataRelationPath

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

## <a name="method-datasourceobject"></a>メソッド dataSourceObject

```xpp
public FormDataSource dataSourceObject()
```

### <a name="return-value---datasourceobject"></a>戻り値 - dataSourceObject

## <a name="method-displaytarget"></a>メソッド displayTarget

クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a>パラメーター - displayTarget

値  
コントロールが表示される場所を示す整数値。オプション。

### <a name="return-value---displaytarget"></a>戻り値 - displayTarget

クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

## <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a>パラメーター - dragDrop

値  
ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。

### <a name="return-value---dragdrop"></a>戻り値 - dragDrop

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="examples---dragdrop"></a>例 - dragDrop

次の例は、ドラッグ アンド ドロップの動作が有効かどうかを示す値を返すか、設定する方法を示しています。

```xpp
boolean dDragDrop; 
// The ctrl variable was previously assigned  
// as a FormControl value. 
// Retrieve the drag-and-drop-enabled value. 
dDragDrop = ctrl.dragDrop(); 
// Set the drag�and�drop-enabled value. 
ctrl.dragDrop(true);
```

## <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a>パラメーター - dragOver

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="return-value---dragover"></a>戻り値 - dragOver

ドラッグ モードを示す FormDrag 列挙値。

## <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a>パラメーター - dragOverEx

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

### <a name="return-value---dragoverex"></a>戻り値 - dragOverEx

ドラッグ モードを示す FormDrag 列挙値。

## <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a>戻り値 - dragText

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

## <a name="method-editautopostback"></a>メソッド editAutoPostback

```xpp
public boolean editAutoPostback([boolean value])
```

### <a name="parameters---editautopostback"></a>パラメーター - editAutoPostback

値  

### <a name="return-value---editautopostback"></a>戻り値 - editAutoPostback

## <a name="method-enabled"></a>メソッド enabled

オブジェクトが有効か無効かを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  
コントロールが有効かどうかを指定するブール値; オプション。

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="examples---enabled"></a>例 - enabled

次の例は、コントロールの有効なプロパティを返して設定する方法を示しています。

```xpp
// Return the value of the enabled property. 
info(strfmt("enabled: %1",this.enabled())); 
// Set the enabled property. 
this.enabled(false);
```

## <a name="method-extendedstyle"></a>メソッド extendedStyle

```xpp
public str extendedStyle([str value])
```

### <a name="parameters---extendedstyle"></a>パラメーター - extendedStyle

値  

### <a name="return-value---extendedstyle"></a>戻り値 - extendedStyle

## <a name="method-fieldbinding"></a>メソッド fieldBinding

FieldBinding 派生クラスへのコントロールのテーブルおよびフィールド バインディングを取得します。

```xpp
public FieldBinding fieldBinding()
```

### <a name="return-value---fieldbinding"></a>戻り値 - fieldBinding

コントロールのテーブルおよびフィールド バインディングを含む FieldBinding 派生クラス。

## <a name="method-formatstr"></a>メソッド formatStr

```xpp
public str formatStr([int rowNumber], [boolean display], [int maxWidth], [boolean forceSignWhenDisplaceNegative], [boolean formatForExport])
```

### <a name="parameters---formatstr"></a>パラメーター - formatStr

rowNumber  

<!-- -->

表示  

<!-- -->

maxWidth  

<!-- -->

forceSignWhenDisplaceNegative  

<!-- -->

formatForExport  

### <a name="return-value---formatstr"></a>戻り値 - formatStr

## <a name="method-formrun"></a>メソッド formRun

```xpp
public xFormRun formRun()
```

### <a name="return-value---formrun"></a>戻り値 - formRun

## <a name="method-getbinding"></a>メソッド getBinding

```xpp
public FormBinding getBinding(str propertyName)
```

### <a name="parameters---getbinding"></a>パラメーター - getBinding

propertyName  

### <a name="return-value---getbinding"></a>戻り値 - getBinding

## <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a>パラメーター - hasChanged

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

### <a name="return-value---haschanged"></a>戻り値 - hasChanged

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="examples---haschanged"></a>例 - hasChanged

次の例は、コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。

```xpp
boolean bHasChanged; 
// The ctrl variable was previously assigned 
// as a FormControl value. 
// Retrieve the hasChanged value. 
bHasChanged = ctrl.hasChanged(); 
// Modify the hasChanged value. 
ctrl.hasChanged(true);
```

## <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a>戻り値 - hasUserSetting

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

## <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a>パラメーター - height

値  
高さの計算方法を示す整数値。オプション。

<!-- -->

モード  
高さの計算方法を示す整数値。オプション。

### <a name="return-value---height"></a>戻り値 - height

ピクセル単位のコントロールの高さ。

### <a name="remarks---height"></a>備考 - height

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード              | 高さの計算                                                                         |
|-------------------|--------------------------------------------------------------------------------------------|
| -1 � 正確        | ピクセル単位のコントロールの正確な高さが使用されます。                                         |
| 0 � 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 � 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                               |

高さと高さ計算モードは別々に設定できます。

## <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a>パラメーター - heightMode

値  
コントロールの高さの計算方法を示す整数値。オプション。

### <a name="return-value---heightmode"></a>戻り値 - heightMode

計算モード。

### <a name="remarks---heightmode"></a>備考 - heightMode

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| 正確         | ピクセル単位のコントロールの正確な高さが使用されます。                                         |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                               |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="examples---heightmode"></a>例 - heightMode

次の例は、フォーム コントロールの高さ計算モードを返して設定する方法を示しています。

```xpp
int nHeightMode; 
// The ctrl variable was previously assigned 
// as a form control variable. 
// Retrieve the height mode. 
nHeightMode = ctrl.HeightMode(); 
// Set the height mode. 
ctrl.heightMode(-1); 
// Set the height. 
ctrl.heightValue(16);
```

## <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  
高さをピクセル単位で指定する整数値。オプション。

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

ピクセル単位の高さ。

### <a name="remarks---heightvalue"></a>備考 - heightValue

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="examples---heightvalue"></a>例 - heightValue

次の例は、フォーム コントロールの高さの値を返して設定する方法を示しています。

```xpp
int nHeightValue; 
// The ctrl variable was previously assigned 
// as a form control variable. 
// Retrieve the height value. 
nHeightValue = ctrl.heightValue(); 
// Set the height value. 
ctrl.heightMode(-1); 
ctrl.heightValue(22);
```

## <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a>戻り値 - helpField

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

### <a name="remarks---helpfield"></a>備考 - helpField

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="examples---helpfield"></a>例 - helpField

次の例は、helpField メソッドの使用方法を示しています。

```xpp
str strHelp; 
strHelp = this.helpField();
```

## <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  
コントロールのヘルプ テキストとして割り当てる値。

### <a name="return-value---helptext"></a>戻り値 - helpText

画面の下部に表示される文字列。

### <a name="remarks---helptext"></a>備考 - helpText

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="examples---helptext"></a>例 - helpText

次の例は、コントロールのヘルプ テキストを設定して返す方法を示しています。

```xpp
// objCtrl previously assigned to a control 
// Retrieve existing help text. 
print objCtrl.helpText(); 
// Specify new help text. 
objCtrl.helpText("My new help text");
```

## <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a>パラメーター - hierarchyParent

値  
コントロールの HierarchyParent プロパティに割り当てる値。

### <a name="return-value---hierarchyparent"></a>戻り値 - hierarchyParent

コントロールの HierarchyParent プロパティ値。

## <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a>戻り値 - hWnd

ハンドラーコントロールのハンドルです。

### <a name="remarks---hwnd"></a>備考 - hWnd

この処理は、Windows API で使用できます。

### <a name="examples---hwnd"></a>例 - hWnd

次の例は、コントロールの Windows ハンドルを取得する方法を示しています。

```xpp
int h; 
h = this.hWnd(); 
info (strfmt("hWnd: %1", h));
```

## <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

コントロールの ID。

## <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a>戻り値 - isDisplayed

コントロールが表示される場合は true。それ以外の場合は false。

### <a name="remarks---isdisplayed"></a>備考 - isDisplayed

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="examples---isdisplayed"></a>例 - isDisplayed

次の例は、コントロールが可視かどうかを判断する方法を示しています。

```xpp
info(strfmt("isDisplayed: %1", this.isDisplayed()));
```

## <a name="method-iseditable"></a>メソッド isEditable

```xpp
public boolean isEditable()
```

### <a name="return-value---iseditable"></a>戻り値 - isEditable

## <a name="method-isenabled"></a>メソッド isEnabled

```xpp
public boolean isEnabled()
```

### <a name="return-value---isenabled"></a>戻り値 - isEnabled

## <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a>戻り値 - isRestricted

コントロールが制限される場合は true。それ以外の場合は false。

## <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a>パラメーター - isUserSetupEnabled

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

### <a name="return-value---isusersetupenabled"></a>戻り値 - isUserSetupEnabled

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

### <a name="remarks---isusersetupenabled"></a>備考 - isUserSetupEnabled

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="examples---isusersetupenabled"></a>例 - isUserSetupEnabled

次の例は、コントロールのユーザー設定権限を決定する方法を示しています。

```xpp
FormAllowUserSetup formAllowUserSetup = FormAllowUserSetup::No; 
switch (true) 
{ 
    case this.isUserSetupEnabled(FormAllowUserSetup::Yes): 
        formAllowUserSetup = FormAllowUserSetup::Yes; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::Restricted): 
        formAllowUserSetup = FormAllowUserSetup::Restricted; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::No): 
       formAllowUserSetup = FormAllowUserSetup::No; 
        break; 
} 
info (strfmt("formAllowUserSetup: %1", formAllowUserSetup));
```

## <a name="method-isvisible"></a>メソッド isVisible

コントロールが表示されるかどうかを示す値を取得します。

```xpp
public boolean isVisible()
```

### <a name="return-value---isvisible"></a>戻り値 - isVisible

コントロールが可視である場合は true。それ以外の場合は false。

## <a name="method-isvisibleonclient"></a>メソッド isVisibleOnClient

```xpp
public boolean isVisibleOnClient()
```

### <a name="return-value---isvisibleonclient"></a>戻り値 - isVisibleOnClient

## <a name="method-labeltext"></a>メソッド labelText

コントロールのラベル テキストを取得します。

```xpp
public str labelText()
```

### <a name="return-value---labeltext"></a>戻り値 - labelText

コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。

## <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a>パラメーター - left

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

### <a name="return-value---left"></a>戻り値 - left

フォーム内のコントロールの水平位置。

## <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a>パラメーター - leftMode

値  
コントロールの水平配置モードを示す整数値。オプション。

### <a name="return-value---leftmode"></a>戻り値 - leftMode

フォームのコントロールの水平配置モード。

## <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a>パラメーター - leftValue

値  
コントロールの水平位置を示す整数値。オプション。

### <a name="return-value---leftvalue"></a>戻り値 - leftValue

フォーム内のコントロールの水平位置。

## <a name="method-lockwindowupdate"></a>メソッド lockWindowUpdate

更新のコントロールのウィンドウをロックまたはロック解除します。

```xpp
public boolean lockWindowUpdate(boolean lock)
```

### <a name="parameters---lockwindowupdate"></a>パラメーター - lockWindowUpdate

lock  
ブール値: ウィンドウをロックする場合は true、ウィンドウをロック解除するには false。

### <a name="return-value---lockwindowupdate"></a>戻り値 - lockWindowUpdate

操作が成功した場合は true。それ以外の場合は、false。

## <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a>パラメーター - markAsUserAdd

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

### <a name="return-value---markasuseradd"></a>戻り値 - markAsUserAdd

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

## <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a>パラメーター - mouseDblClick

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="return-value---mousedblclick"></a>戻り値 - mouseDblClick

イベントが処理された場合は 0 (ゼロ) です。

### <a name="examples---mousedblclick"></a>例 - mouseDblClick

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseDblClick イベントのパラメーターを表示する方法を示しています。

```xpp
public int mouseDblClick(int x,  
                         int y,  
                         int button, 
                         boolean Ctrl, 
                         boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a>パラメーター - mouseDown

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="return-value---mousedown"></a>戻り値 - mouseDown

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---mousedown"></a>備考 - mouseDown

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="examples---mousedown"></a>例 - mouseDown

次の例は、Infolog に mouseDown イベントのパラメーターを表示する方法を示しています。

```xpp
public int mouseDown(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a>パラメーター - mouseMove

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="return-value---mousemove"></a>戻り値 - mouseMove

イベントが処理された場合は 0 (ゼロ) です。

### <a name="examples---mousemove"></a>例 - mouseMove

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseMove イベントのパラメーターを表示する方法を示しています。

```xpp
public int mouseMove(int x,  
                     int y,  
                     int button, 
                     boolean Ctrl, 
                     boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a>パラメーター - mouseUp

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="return-value---mouseup"></a>戻り値 - mouseUp

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---mouseup"></a>備考 - mouseUp

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="examples---mouseup"></a>例 - mouseUp

次の例は、Infolog に mouseUp イベントのパラメーターを表示する方法を示しています。

```xpp
public int mouseUp(int x,  
                   int y,  
                   int button, 
                   boolean Ctrl, 
                   boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  
コントロールに割り当てる名前 (オプション)。

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-neededpermission"></a>メソッド neededPermission

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a>パラメーター - neededPermission

値  

### <a name="return-value---neededpermission"></a>戻り値 - neededPermission

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a>戻り値 - parentControl

コントロールの親コントロール。

## <a name="method-resourcebundlename"></a>メソッド resourceBundleName

```xpp
public str resourceBundleName()
```

### <a name="return-value---resourcebundlename"></a>戻り値 - resourceBundleName

## <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

### <a name="return-value---securitykey"></a>戻り値 - securityKey

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="examples---securitykey"></a>例 - securityKey

次の例では、コントロールのセキュリティ キー IDを取得して割り当てる方法を示しています。

```xpp
DictSecurityKey dsk; 
securityKeyId ski; 
// objCtrl previously assigned. 
// Assign a security key ID to the control. 
objCtrl.securityKey(securitykeynum(AdminDaily)); 
// Retrieve the security key ID from the control. 
ski = objCtrl.securityKey(); 
if (ski != 0) 
{ 
    dsk = new DictSecurityKey(ski); 
    if (dsk) 
    { 
        print strfmt("Security Key ID: %1 Security Key Name: %2", 
                     ski, 
                     dsk.name()); 
    } 
}
```

## <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a>パラメーター - showContextMenu

menuHandle  
表示するメニューの ID。

### <a name="return-value---showcontextmenu"></a>戻り値 - showContextMenu

通話が成功したかどうかを示す整数値。

## <a name="method-getcontextmenuoptions"></a>メソッド getContextMenuOptions

```xpp
public str getContextMenuOptions()
```

### <a name="return-value---getcontextmenuoptions"></a>戻り値 - getContextMenuOptions

## <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

### <a name="return-value---skip"></a>戻り値 - skip

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="remarks---skip"></a>備考 - skip

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="examples---skip"></a>例 - skip

次のコード例は、コントロールのスキップ プロパティを返して設定する方法を示しています。

```xpp
// Return the value of the skip property. 
info(strfmt("skip: %1", this.skip())); 
// Set the value of the skip property. 
this.skip(true);
```

## <a name="method-templateid"></a>メソッド templateId

```xpp
public str templateId()
```

### <a name="return-value---templateid"></a>戻り値 - templateId

## <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a>戻り値 - toolTip

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

### <a name="remarks---tooltip"></a>備考 - toolTip

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="examples---tooltip"></a>例 - toolTip

次の例は、toolTip メソッドを上書きする方法を示しています。

```xpp
str toolTip() 
{ 
    return "Account numbers of customers eligible for discount"; 
}
```

## <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a>パラメーター - top

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

### <a name="return-value---top"></a>戻り値 - top

フォーム内のコントロールの垂直位置。

## <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a>パラメーター - topMode

値  
コントロールの垂直配置モードを示す整数値。オプション。

### <a name="return-value---topmode"></a>戻り値 - topMode

フォームのコントロールの垂直配置モード。

## <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a>パラメーター - topValue

値  
コントロールの垂直位置を示す整数値。オプション。

### <a name="return-value---topvalue"></a>戻り値 - topValue

フォーム内のコントロールの垂直位置。

## <a name="method-type"></a>メソッドのタイプ

```xpp
public int type([int value])
```

### <a name="parameters---type"></a>パラメーター - type

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

データ  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-updatewindow"></a>メソッド updateWindow

コントロールのウィンドウを更新します。

```xpp
public int updateWindow()
```

### <a name="return-value---updatewindow"></a>戻り値 - updateWindow

更新が成功した場合は 1、それ以外の場合は 0 です。

## <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a>パラメーター - userData

値  
コントロールのユーザー データを示す整数値。オプション。

### <a name="return-value---userdata"></a>戻り値 - userData

コントロールのユーザー データ。

## <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a>パラメーター - userDataItem

値  
コントロールのユーザー データ項目を示す整数値。オプション。

### <a name="return-value---userdataitem"></a>戻り値 - userDataItem

コントロールのユーザー データ アイテム。

## <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a>パラメーター - userDataItems

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

### <a name="return-value---userdataitems"></a>戻り値 - userDataItems

コントロールのユーザー データ項目の数。

## <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a>パラメーター - userDisable

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

### <a name="return-value---userdisable"></a>戻り値 - userDisable

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

## <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a>パラメーター - userHeight

値  
コントロールのユーザーの高さ (オプション)。

### <a name="return-value---userheight"></a>戻り値 - userHeight

コントロールのカスタム ユーザーの高さ。

## <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a>パラメーター - userHide

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

### <a name="return-value---userhide"></a>戻り値 - userHide

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

### <a name="remarks---userhide"></a>備考 - userHide

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="examples---userhide"></a>例 - userHide

次の例は、コントロールがユーザーから隠されているかどうかを示す値を返して設定する方法を示しています。

```xpp
int nUserHide; 
// The ctrl variable was previously assigned  
// as a control variable. 
// Retrieve the userHide value. 
nUserHide = ctrl.userHide(); 
// Set the userHide value. 
ctrl.userHide(1);
```

## <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a>パラメーター - userOrgContainer

値  
コントロールに設定する組織コンテナー (オプション)。

### <a name="return-value---userorgcontainer"></a>戻り値 - userOrgContainer

コントロールの組織コンテナー。

## <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a>パラメーター - userOrgSibling

値  
コントロールに設定する組織の兄弟 (オプション)。

### <a name="return-value---userorgsibling"></a>戻り値 - userOrgSibling

コントロールの組織の兄弟。

## <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a>パラメーター - userPromptText

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

### <a name="return-value---userprompttext"></a>戻り値 - userPromptText

コントロールのユーザーラベル テキスト。

## <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a>パラメーター - userSecurityLevel

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

### <a name="return-value---usersecuritylevel"></a>戻り値 - userSecurityLevel

コントロールのユーザー セキュリティ レベル。

## <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a>パラメーター - userSkip

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

### <a name="return-value---userskip"></a>戻り値 - userSkip

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="examples---userskip"></a>例 - userSkip

次の例は、userSkip プロパティを返して設定する方法を示しています。

```xpp
int nUserSkip 
// The ctrl variable was previously assigned  
// as a FormControl value. 
// Return the userSkip property. 
nUserSkip = ctrl.userSkip(); 
// Set the userSkip property. 
ctrl.userSkip(1);
```

## <a name="method-userwidth"></a>メソッド userWidth

ピクセル単位でコントロールの幅を設定するか返します。

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a>パラメーター - userWidth

値  
コントロールの幅として使用するピクセル数 (オプション)。

### <a name="return-value---userwidth"></a>戻り値 - userWidth

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

### <a name="remarks---userwidth"></a>備考 - userWidth

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="examples---userwidth"></a>例 - userWidth

次の例は、フォーム コントロールのユーザーの幅を返して設定する方法を示しています。

```xpp
int nWidth; 
// The ctrl variable was previously defined 
// as a FormControl value. 
// Return the width. 
nWidth = ctrl.userWidth(); 
// Specify the width. 
ctrl.userWidth(90);  // 15 characters * 6 pixels == 90
```

## <a name="method-valuestr"></a>メソッド valueStr

文字列形式のコントロールの値を取得します。

```xpp
public str valueStr()
```

### <a name="return-value---valuestr"></a>戻り値 - valueStr

文字列形式のコントロールの値。

### <a name="remarks---valuestr"></a>備考 - valueStr

valueStr メソッドは、データ ソースにバインドできます。 valueStr メソッドは、コントロールの検証メソッドでは使用しないでください。 代わりに、管理検証メソッドでテキスト メソッドを使用します。

## <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a>パラメーター - verticalSpacing

値  
コントロールの AutoMode を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode を示す整数値。オプション。

### <a name="return-value---verticalspacing"></a>戻り値 - verticalSpacing

フォームのコントロールの垂直スペーシング。

## <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a>パラメーター - verticalSpacingMode

モード  

### <a name="return-value---verticalspacingmode"></a>戻り値 - verticalSpacingMode

フォームのコントロールの垂直スペーシング モード。

## <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a>パラメーター - verticalSpacingValue

値  
コントロールの上下の間隔を示す整数値。オプション。

### <a name="return-value---verticalspacingvalue"></a>戻り値 - verticalSpacingValue

フォームのコントロールの垂直スペーシング。

## <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  
コントロールの可視化設定に割り当てる値 (オプション)。

### <a name="return-value---visible"></a>戻り値 - visible

コントロールが可視である場合は true。それ以外の場合は false。

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  
幅の計算方法を示す整数値。オプション。

<!-- -->

モード  
幅の計算方法を示す整数値。オプション。

### <a name="return-value---width"></a>戻り値 - width

ピクセル単位のコントロールの幅。

### <a name="remarks---width"></a>備考 - width

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード             | 幅計算                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| -1 � 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 0 � 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 � 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

幅と幅計算モードは別々に設定できます。

## <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a>パラメーター - widthMode

値  
コントロール幅の計算方法を示す整数値。オプション。

### <a name="return-value---widthmode"></a>戻り値 - widthMode

現在の計算モードを示す整数値。

### <a name="remarks---widthmode"></a>備考 - widthMode

次の表に従って幅を計算します。

| モード         | 幅計算                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="examples---widthmode"></a>例 - widthMode

次の例は、フォーム コントロールの幅計算モードを返して設定する方法を示しています。

```xpp
int nWidthMode; 
// The ctrl variable was previously assigned 
// as a form control variable. 
// Retrieve the width mode. 
nWidthMode = ctrl.widthMode (); 
// Set the width mode. 
ctrl.widthMode(-1); 
// Set the width. 
ctrl.widthValue(180);
```

## <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  
幅をピクセル単位で指定する整数値。オプション。

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="examples---widthvalue"></a>例 - widthValue

次の例は、フォーム コントロールの幅の値を返して設定する方法を示しています。

```xpp
int nWidthValue; 
// The ctrl variable was previously assigned 
// as a form control value. 
// Retrieve the width value. 
nWidthValue = ctrl.widthValue(); 
// Set the width value. 
ctrl.widthMode(-1); 
ctrl.widthValue(160);
```

## <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

```xpp
public void displayControl()
```

## <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

```xpp
public void copy()
```

## <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

```xpp
public void paste()
```

## <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

```xpp
public void setFocus()
```

## <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

```xpp
public void cut()
```

## <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

```xpp
public void gotFocus()
```

## <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

```xpp
public void dragLeave()
```

## <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

```xpp
public void lostFocus()
```

## <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a>パラメーター - inputSearch

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

## <a name="method-settemplateid"></a>メソッド setTemplateId

```xpp
public void setTemplateId([str value])
```

### <a name="parameters---settemplateid"></a>パラメーター - setTemplateId

値  

## <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a>パラメーター - prefColumnSize

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="examples---prefcolumnsize"></a>例 - prefColumnSize

次の例は、フォーム コントロールの優先幅と高さを設定する方法を示しています。

```xpp
// nWidth and nHeight are previously assigned int variables. 
// ctrl is a previously assigned FormControl variable. 
ctrl.prefColumnSize( nWidth, nHeight);
```

## <a name="method-update"></a>メソッド update

コントロールを更新します。

```xpp
public void update()
```

## <a name="method-run"></a>メソッド run

```xpp
public void run()
```

## <a name="method-lock"></a>メソッド lock

フォーム コントロールをロックします。

```xpp
public void lock()
```

### <a name="remarks---lock"></a>備考 - lock

オブジェクトを変更し、他のユーザーが変更を加えるかどうか確信が持てない場合には、Lock コマンドを使用します。 更新内容の保存が完了したら、ロック解除コマンドを使用します。

## <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a>パラメーター - mouseEnter

x  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

y  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを示すブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを示すブール値。

### <a name="examples---mouseenter"></a>例 - mouseEnter

次の例は、Infolog に mouseEnter イベントのパラメーターを表示する方法を示しています。

```xpp
public void mouseEnter(int x,  
                      int y,  
                      int button, 
                      boolean Ctrl, 
                      boolean Shift) 
{ 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
}
```

## <a name="method-applybuild"></a>メソッド applyBuild

```xpp
public void applyBuild()
```

## <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a>パラメーター - drop

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

```xpp
public void resetUserSetting()
```

## <a name="method-new"></a>メソッド new

```xpp
public void new(FormBuildControl build, xFormRun formRun)
```

### <a name="parameters---new"></a>パラメーター - new

build  

<!-- -->

formRun  

## <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

```xpp
public void context()
```

## <a name="method-unlock"></a>メソッド unLock

フォーム コントロールのロックを解除します。

```xpp
public void unLock(boolean update)
```

### <a name="parameters---unlock"></a>パラメーター - unLock

更新  
コントロールに加えられる変更を保存するかどうかを示すブール値。

## <a name="method-setresourcebundlename"></a>メソッド setResourceBundleName

```xpp
public void setResourceBundleName([str value])
```

### <a name="parameters---setresourcebundlename"></a>パラメーター - setResourceBundleName

値  

## <a name="method-selectedmenuoption"></a>メソッド selectedMenuOption

```xpp
public void selectedMenuOption(int selectedOption)
```

### <a name="parameters---selectedmenuoption"></a>パラメーター - selectedMenuOption

selectedOption  

## <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

```xpp
public void mouseLeave()
```

## <a name="method-onpropchanged"></a>メソッド onPropChanged

```xpp
public void onPropChanged([str propName])
```

### <a name="parameters---onpropchanged"></a>パラメーター - onPropChanged

propName  

## <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a>パラメーター - dropEx

dragSource  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

dragMode  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

x  
マウス位置の垂直クライアント座標を示す整数値。

<!-- -->

y  
マウス位置の垂直クライアント座標を示す整数値。

## <a name="method-initialize"></a>メソッド initialize

```xpp
public void initialize()
```

## <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a>備考 - endDrag

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="examples---enddrag"></a>例 - endDrag

次の例では、ユーザーがフォーム コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。

```xpp
public void endDrag() 
{  
    info("EndDrag completed"); 
    super(); 
}
```

