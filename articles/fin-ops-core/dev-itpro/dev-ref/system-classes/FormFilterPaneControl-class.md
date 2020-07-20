---
title: FormFilterPaneControl クラス
description: このトピックでは、FormFilterPaneControl クラスについて説明します。
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
ms.openlocfilehash: 09191578c74f0222c015b32e1835d8bf9c07e71c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502940"
---
# <a name="class-formfilterpanecontrol"></a>クラス FormFilterPaneControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormFilterPaneControl extends FormControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignChild(\[boolean value\])                                                                |                                                                                                                                                                         |
| public boolean alignChildren(\[boolean value\])                                                             |                                                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public int allowUserSetup(\[int value\])                                                                    |                                                                                                                                                                         |
| public int arrangeGuide(\[int value\])                                                                      |                                                                                                                                                                         |
| public int arrangeMethod(\[int value\])                                                                     |                                                                                                                                                                         |
| public int arrangeWhen(\[int value\])                                                                       |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                                                         |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                         |                                                                                                                                                                         |
| public int bottomMarginValue(\[int value\])                                                                 |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                                                 |
| public int columns(\[int value\], \[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public AutoMode columnsMode(\[AutoMode mode\])                                                              |                                                                                                                                                                         |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                                                         |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                          |                                                                                                                                                                         |
| public int columnspaceValue(\[int value\])                                                                  |                                                                                                                                                                         |
| public int columnsValue(\[int value\])                                                                      |                                                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int displayTarget(\[int value\])                                                                     | クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public boolean hideIfEmpty(\[boolean value\])                                                               |                                                                                                                                                                         |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean leave()                                                                                      |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                     |                                                                                                                                                                         |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                           |                                                                                                                                                                         |
| public int leftMarginValue(\[int value\])                                                                   |                                                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                                                         |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                          |                                                                                                                                                                         |
| public int rightMarginValue(\[int value\])                                                                  |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                                                         |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                            |                                                                                                                                                                         |
| public int topMarginValue(\[int value\])                                                                    |                                                                                                                                                                         |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ピクセル単位でコントロールの幅を設定するか返します。                                                                                                                     |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |

## <a name="method-alignchild"></a>メソッド alignChild

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a>パラメーター - alignChild

値  

### <a name="return-value---alignchild"></a>戻り値 - alignChild

## <a name="method-alignchildren"></a>メソッド alignChildren

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a>パラメーター - alignChildren

値  

### <a name="return-value---alignchildren"></a>戻り値 - alignChildren

## <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a>パラメーター - alignControl

値  
プロパティの新しい値 (オプション)。

### <a name="return-value---aligncontrol"></a>戻り値 - alignControl

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

### <a name="remarks---aligncontrol"></a>備考 - alignControl

コントロールの左上隅は、最も長いラベルに従って配置されます。

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  
allowEdit プロパティに割り当てる値。

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを編集することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

## <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a>戻り値 - allowSysSetup

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

## <a name="method-allowusersetup"></a>メソッド allowUserSetup

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a>パラメーター - allowUserSetup

値  

### <a name="return-value---allowusersetup"></a>戻り値 - allowUserSetup

## <a name="method-arrangeguide"></a>メソッド arrangeGuide

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a>パラメーター - arrangeGuide

値  

### <a name="return-value---arrangeguide"></a>戻り値 - arrangeGuide

## <a name="method-arrangemethod"></a>メソッド arrangeMethod

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a>パラメーター - arrangeMethod

値  

### <a name="return-value---arrangemethod"></a>戻り値 - arrangeMethod

## <a name="method-arrangewhen"></a>メソッド arrangeWhen

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a>パラメーター - arrangeWhen

値  

### <a name="return-value---arrangewhen"></a>戻り値 - arrangeWhen

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  
プロパティの新しい値 (オプション)。

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

## <a name="method-bottommargin"></a>メソッド bottomMargin

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a>パラメーター - bottomMargin

値  

<!-- -->

モード  

### <a name="return-value---bottommargin"></a>戻り値 - bottomMargin

## <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a>パラメーター - bottomMarginMode

モード  

### <a name="return-value---bottommarginmode"></a>戻り値 - bottomMarginMode

## <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a>パラメーター - bottomMarginValue

値  

### <a name="return-value---bottommarginvalue"></a>戻り値 - bottomMarginValue

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

## <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a>パラメーター - caption

値  

### <a name="return-value---caption"></a>戻り値 - caption

コントロールのキャプションとして使用される文字列。

## <a name="method-columns"></a>メソッド columns

```xpp
public int columns([int value], [AutoMode mode])
```

### <a name="parameters---columns"></a>パラメーター - columns

値  

<!-- -->

モード  

### <a name="return-value---columns"></a>戻り値 - columns

## <a name="method-columnsmode"></a>メソッド columnsMode

```xpp
public AutoMode columnsMode([AutoMode mode])
```

### <a name="parameters---columnsmode"></a>パラメーター - columnsMode

モード  

### <a name="return-value---columnsmode"></a>戻り値 - columnsMode

## <a name="method-columnspace"></a>メソッド columnspace

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a>パラメーター - columnspace

値  

<!-- -->

モード  

### <a name="return-value---columnspace"></a>戻り値 - columnspace

## <a name="method-columnspacemode"></a>メソッド columnspaceMode

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a>パラメーター - columnspaceMode

モード  

### <a name="return-value---columnspacemode"></a>戻り値 - columnspaceMode

## <a name="method-columnspacevalue"></a>メソッド columnspaceValue

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a>パラメーター - columnspaceValue

値  

### <a name="return-value---columnspacevalue"></a>戻り値 - columnspaceValue

## <a name="method-columnsvalue"></a>メソッド columnsValue

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a>パラメーター - columnsValue

値  

### <a name="return-value---columnsvalue"></a>戻り値 - columnsValue

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  
コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

## <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a>戻り値 - configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

### <a name="remarks---configurationkeyex"></a>備考 - configurationKeyEx

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

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

## <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a>パラメーター - countryRegionContextField

値  

### <a name="return-value---countryregioncontextfield"></a>戻り値 - countryRegionContextField

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

## <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

値  

### <a name="return-value---datasource"></a>戻り値 - dataSource

使用されるデータ ソースの ID。

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
ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。

### <a name="return-value---dragdrop"></a>戻り値 - dragDrop

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="remarks---dragdrop"></a>備考 - dragDrop

dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。

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

## <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  
コントロールが有効かどうかを示すブール値; オプション。

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

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
高さの計算方法を示す整数です (オプション)。

<!-- -->

モード  
高さの計算方法を示す整数です (オプション)。

### <a name="return-value---height"></a>戻り値 - height

ピクセル単位のコントロールの高さ。

### <a name="remarks---height"></a>備考 - height

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

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

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

## <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  
高さをピクセル単位で指定する整数です (オプション)。

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

ピクセル単位の高さ。

### <a name="remarks---heightvalue"></a>備考 - heightValue

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

## <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a>戻り値 - helpField

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

### <a name="remarks---helpfield"></a>備考 - helpField

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

## <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  
コントロールのヘルプ テキストとして割り当てられる値。

### <a name="return-value---helptext"></a>戻り値 - helpText

画面の下部に表示される文字列。

### <a name="remarks---helptext"></a>備考 - helpText

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

## <a name="method-hideifempty"></a>メソッド hideIfEmpty

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a>パラメーター - hideIfEmpty

値  

### <a name="return-value---hideifempty"></a>戻り値 - hideIfEmpty

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

## <a name="method-iscontainer"></a>メソッド isContainer

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a>戻り値 - isContainer

## <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a>戻り値 - isDisplayed

コントロールが表示される場合は true。それ以外の場合は false。

### <a name="remarks---isdisplayed"></a>備考 - isDisplayed

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

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

## <a name="method-leave"></a>メソッド leave

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a>戻り値 - leave

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

## <a name="method-leftmargin"></a>メソッド leftMargin

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a>パラメーター - leftMargin

値  

<!-- -->

モード  

### <a name="return-value---leftmargin"></a>戻り値 - leftMargin

## <a name="method-leftmarginmode"></a>メソッド leftMarginMode

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a>パラメーター - leftMarginMode

モード  

### <a name="return-value---leftmarginmode"></a>戻り値 - leftMarginMode

## <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a>パラメーター - leftMarginValue

値  

### <a name="return-value---leftmarginvalue"></a>戻り値 - leftMarginValue

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

### <a name="remarks---mousedblclick"></a>備考 - mouseDblClick

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

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

### <a name="remarks---mousemove"></a>備考 - mouseMove

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

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

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  
コントロールに割り当てる名前。

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

## <a name="method-rightmargin"></a>メソッド rightMargin

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a>パラメーター - rightMargin

値  

<!-- -->

モード  

### <a name="return-value---rightmargin"></a>戻り値 - rightMargin

## <a name="method-rightmarginmode"></a>メソッド rightMarginMode

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a>パラメーター - rightMarginMode

モード  

### <a name="return-value---rightmarginmode"></a>戻り値 - rightMarginMode

## <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a>パラメーター - rightMarginValue

値  

### <a name="return-value---rightmarginvalue"></a>戻り値 - rightMarginValue

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

## <a name="method-sort"></a>メソッド sort

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a>パラメーター - sort

sortDirection  

### <a name="return-value---sort"></a>戻り値 - sort

## <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a>戻り値 - toolTip

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

### <a name="remarks---tooltip"></a>備考 - toolTip

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

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

## <a name="method-topmargin"></a>メソッド topMargin

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a>パラメーター - topMargin

値  

<!-- -->

モード  

### <a name="return-value---topmargin"></a>戻り値 - topMargin

## <a name="method-topmarginmode"></a>メソッド topMarginMode

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a>パラメーター - topMarginMode

モード  

### <a name="return-value---topmarginmode"></a>戻り値 - topMarginMode

## <a name="method-topmarginvalue"></a>メソッド topMarginValue

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a>パラメーター - topMarginValue

値  

### <a name="return-value---topmarginvalue"></a>戻り値 - topMarginValue

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

## <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a>パラメーター - verticalSpacing

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

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
幅の計算方法を示す整数です (オプション)。

<!-- -->

モード  
幅の計算方法を示す整数です (オプション)。

### <a name="return-value---width"></a>戻り値 - width

ピクセル単位のコントロールの幅。

### <a name="remarks---width"></a>備考 - width

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

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

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

## <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  
幅をピクセル単位で指定する整数です (オプション)。

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

## <a name="method-onenter"></a>メソッド OnEnter

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a>パラメーター - OnEnter

sender  

<!-- -->

e  

## <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

```xpp
public void lostFocus()
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

## <a name="method-onleaving"></a>メソッド OnLeaving

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a>パラメーター - OnLeaving

sender  

<!-- -->

e  

## <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

```xpp
public void mouseLeave()
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

## <a name="method-enter"></a>メソッド enter

```xpp
public void enter()
```

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

## <a name="method-jumpref"></a>メソッド jumpRef

```xpp
public void jumpRef()
```

## <a name="method-onlostfocus"></a>メソッド OnLostFocus

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a>パラメーター - OnLostFocus

sender  

<!-- -->

e  

## <a name="method-ongotfocus"></a>メソッド OnGotFocus

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a>パラメーター - OnGotFocus

sender  

<!-- -->

e  

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

## <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

```xpp
public void cut()
```

## <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a>パラメーター - registerOverrideMethod

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

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

## <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

```xpp
public void context()
```

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

```xpp
public void resetUserSetting()
```

## <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a>パラメーター - inputSearch

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

## <a name="method-filter"></a>メソッド filter

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a>パラメーター - filter

filterStr  

## <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a>備考 - endDrag

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

