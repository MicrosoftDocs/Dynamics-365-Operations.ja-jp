---
title: FormTreeControl クラス
description: このトピックでは、FormTreeControl クラスについて説明します。
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
ms.openlocfilehash: a1d3eb39f31d1de510102f890114cfe20698ab51
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502619"
---
# <a name="class-formtreecontrol"></a>クラス FormTreeControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormTreeControl extends FormControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int add(int parent, int insertAfter, str Text, \[int image\], \[int children\])                      |                                                                                                                                                                         |
| public int addItem(int parent, int insertAfter, FormTreeItem item)                                          |                                                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を修正できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム ツリー コントロールのドラッグを始めると呼び出されます。                                                                                                             |
| public boolean beginLabelEdit(int Idx, str text, AnyType data)                                              |                                                                                                                                                                         |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。                                                                                               |
| public int border(\[int value\])                                                                            | コントロールの境界のスタイルを取得または設定します。                                                                                                                   |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public boolean canScroll(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean cascadeSelect(\[boolean value\])                                                             |                                                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public boolean checkBox(\[boolean value\])                                                                  |                                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。                                                                          |
| public int copyItem(int Idx, int newParent, \[int insertAfter\])                                            |                                                                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public Imagelist createDragImagelist()                                                                      |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public boolean delete(int Idx)                                                                              | フォーム ツリー コントロールから指定した項目を削除します。                                                                                                                  |
| public boolean deleteAll()                                                                                  | フォーム ツリー コントロールからすべての項目を削除します。                                                                                                                           |
| public int displayTarget(\[int value\])                                                                     | クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                    |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム ツリー コントロールをドラッグしたときに表示されるテキストを返します。                                                                                               |
| public boolean editLabels(\[boolean value\])                                                                |                                                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトが有効か無効かを決定します。                                                                                                                   |
| public int expand(int Idx, \[FormTreeExpand action\])                                                       |                                                                                                                                                                         |
| public boolean expanding(int Idx, FormTreeExpand action, AnyType data)                                      |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | コントロール内のテキストに使用されるフォントの名前を取得または設定します。                                                                                             |
| public int fontSize(\[int value\])                                                                          | コントロール内のテキストに使用されるフォント サイズを取得または設定します。                                                                                                    |
| public int foregroundColor(\[int value\])                                                                   | コントロール内のテキストに使用される色を取得または設定します。                                                                                                        |
| public int getChild(int Idx)                                                                                |                                                                                                                                                                         |
| public int getFirstSelected()                                                                               |                                                                                                                                                                         |
| public int getFirstVisible()                                                                                |                                                                                                                                                                         |
| public Imagelist getImagelist()                                                                             |                                                                                                                                                                         |
| public FormTreeItem getItem(int Idx)                                                                        |                                                                                                                                                                         |
| public int getNextSelected(int idx)                                                                         |                                                                                                                                                                         |
| public int getNextSibling(int Idx)                                                                          |                                                                                                                                                                         |
| public int getNextVisible(int Idx)                                                                          |                                                                                                                                                                         |
| public int getParent(int Idx)                                                                               |                                                                                                                                                                         |
| public int getPrevSelected(int idx)                                                                         |                                                                                                                                                                         |
| public int getPrevSibling(int Idx)                                                                          |                                                                                                                                                                         |
| public int getPrevVisible(int Idx)                                                                          |                                                                                                                                                                         |
| public int getRoot()                                                                                        |                                                                                                                                                                         |
| public int getSelectedCount()                                                                               |                                                                                                                                                                         |
| public int getSelection()                                                                                   |                                                                                                                                                                         |
| public Imagelist getStateImagelist()                                                                        |                                                                                                                                                                         |
| public int getVisibleCount()                                                                                | ツリー コントロール内の表示されている項目の数を返します。                                                                                                                |
| public boolean hasButtons(\[boolean value\])                                                                | ツリー コントロールが展開/折り畳みボタンを表示するかどうかを示す値を返します。                                                                                   |
| public boolean hasChanged(\[boolean val\])                                                                  | ツリー コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                           |
| public boolean hasLines(\[boolean value\])                                                                  | ツリー コントロールがツリー コネクタ明細行を表示するかどうかを示す値を返します。                                                                                  |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを返します。                                                                                                                                  |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                         |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public container hitTest(int x, int y)                                                                      |                                                                                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを返します。                                                                                                                             |
| public boolean isContainer()                                                                                | コントロールがコンテナーかどうかを示す値を返します。                                                                                                      |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を返します。                                                                                                        |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean italic(\[boolean value\])                                                                    | コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。                                                                                       |
| public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)                                               |                                                                                                                                                                         |
| public boolean leave()                                                                                      |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean linesAtRoot(\[boolean value\])                                                               |                                                                                                                                                                         |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターがコントロール上にある状態でクリックすると呼び出されます。                                                                                             |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | マウス ポインターがコントロール上にある状態で、ユーザーがマウス ボタンを放すと呼び出されます。                                                                          |
| public int moveItem(int Idx, int newParent, \[int insertAfter\])                                            |                                                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                               |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public boolean rowSelect(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int select(int Idx)                                                                                  |                                                                                                                                                                         |
| public int selectEx(int Idx, boolean setSelection)                                                          |                                                                                                                                                                         |
| public boolean selectionChanging(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)            |                                                                                                                                                                         |
| public int selectItems(int fromIdx, int toIdx)                                                              |                                                                                                                                                                         |
| public int selectSetFirstVisible(int Idx)                                                                   |                                                                                                                                                                         |
| public boolean setInsertMark(int Idx, boolean After)                                                        |                                                                                                                                                                         |
| public boolean setItem(FormTreeItem item)                                                                   |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showSelAlways(\[boolean value\])                                                             |                                                                                                                                                                         |
| public boolean singleSelection(\[boolean value\])                                                           |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public str toolTip()                                                                                        | コントロールのツールヒント テキストを返します。                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public boolean trackSelect(\[boolean value\])                                                               |                                                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | フォーム ツリー コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。                                                                         |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザー プロンプト テキストを設定または取得します。                                                                                                                 |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                         |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void checkedStateChanged(int Idx, FormTreeCheckedState newState)                                     |                                                                                                                                                                         |
| public void endLabelEdit(int Idx, str text, AnyType data)                                                   |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。                                                                                                       |
| private void OnExpanding(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void paste()                                                                                         | フォーム ツリー コントロールをフォームに貼り付けます。                                                                                                                               |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void itemMoved(int OldIdx, int NewIdx)                                                               |                                                                                                                                                                         |
| public void expanded(int Idx, FormTreeExpand action, AnyType data)                                          |                                                                                                                                                                         |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])                         |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void mouseLeave()                                                                                    | ユーザーがマウス ポインターをコントロールから移動させると呼び出されます。                                                                                                     |
| public void endDrag()                                                                                       | ユーザーがフォーム ツリー コントロールのドラッグを終了すると呼び出されます。                                                                                                      |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void itemCopy(int OldIdx, int NewIdx)                                                                |                                                                                                                                                                         |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void prefColumnSize(int width, int height)                                                           | フォーム ツリー コントロールの最適な列の幅と高さを指定します。                                                                                              |
| public void setImagelist(Imagelist imageList)                                                               |                                                                                                                                                                         |
| private void OnExpanded(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void itemDeleted(int Idx, AnyType data)                                                              |                                                                                                                                                                         |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void setStateImagelist(Imagelist imageList)                                                          |                                                                                                                                                                         |
| public void endEditLabel(boolean cancel)                                                                    |                                                                                                                                                                         |
| public void copy()                                                                                          | フォーム ツリー コントロールをコピーします。                                                                                                                                           |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void selectionChanged(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)                | ユーザーがフォーム ツリー コントロールで選択した項目を変更したことを示します。                                                                                         |
| public void beginEditLabel(int Idx)                                                                         |                                                                                                                                                                         |

## <a name="method-add"></a>メソッド add

```xpp
public int add(int parent, int insertAfter, str Text, [int image], [int children])
```

### <a name="parameters---add"></a>パラメーター - add

parent  

<!-- -->

insertAfter  

<!-- -->

テキスト  

<!-- -->

画像  

<!-- -->

children  

### <a name="return-value---add"></a>戻り値 - add

## <a name="method-additem"></a>メソッド addItem

```xpp
public int addItem(int parent, int insertAfter, FormTreeItem item)
```

### <a name="parameters---additem"></a>パラメーター - addItem

parent  

<!-- -->

insertAfter  

<!-- -->

品目  

### <a name="return-value---additem"></a>戻り値 - addItem

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
autoDeclaration プロパティに割り当てる値。

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

### <a name="remarks---autodeclaration"></a>備考 - autoDeclaration

コントロールには同じ名前を付けることはできません。

## <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a>パラメーター - backgroundColor

値  
コントロールの背景色として割り当てる値。

### <a name="return-value---backgroundcolor"></a>戻り値 - backgroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---backgroundcolor"></a>備考 - backgroundColor

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="examples---backgroundcolor"></a>例 - backgroundColor

次の例は、コントロールの背景色を返して設定する方法を示しています。

```xpp
// Retrieve the existing background color. 
info (strfmt("Background color: %1", this.backgroundColor())); 
// Set the background color. 
this.backgroundColor(WindowsPalette::DarkShadow3D);
```

## <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a>パラメーター - backStyle

値  
コントロールの背景スタイルとして割り当てる値。

### <a name="return-value---backstyle"></a>戻り値 - backStyle

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="examples---backstyle"></a>例 - backStyle

次の例は、背景スタイルを返して設定する方法を示しています。

```xpp
// Return the background style. 
info (strfmt("Background style: %1", this.backStyle())); 
// Set the background style. 
this.backStyle(FormBackStyle::Transparent);
```

## <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム ツリー コントロールのドラッグを始めると呼び出されます。

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a>パラメーター - beginDrag

x  
マウス ポインターの y 座標を示す整数データ型です。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数データ型です。 座標はコントロールの左上隅を基準にしています。

### <a name="return-value---begindrag"></a>戻り値 - beginDrag

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---begindrag"></a>備考 - beginDrag

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="examples---begindrag"></a>例 - beginDrag

次の例では、ユーザーがフォーム ツリー コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。

```xpp
public int beginDrag(int _x, int _y) 
{ 
    int ret; 
    info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
    ret = super(_x, _y); 
    return ret; 
}
```

## <a name="method-beginlabeledit"></a>メソッド beginLabelEdit

```xpp
public boolean beginLabelEdit(int Idx, str text, AnyType data)
```

### <a name="parameters---beginlabeledit"></a>パラメーター - beginLabelEdit

Idx  

<!-- -->

テキスト  

<!-- -->

データ  

### <a name="return-value---beginlabeledit"></a>戻り値 - beginLabelEdit

## <a name="method-bold"></a>メソッド bold

コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a>パラメーター - bold

値  
コントロールのボールド設定に割り当てる値。

### <a name="return-value---bold"></a>戻り値 - bold

0 (ゼロ) から 9 までの間の整数値。

### <a name="remarks---bold"></a>備考 - bold

返される整数には、次のようなフォントの重量が含まれます。

-   0 � 既定のフォントの重量を使用します。
-   1 � シン。
-   2 � エクストラ ライト。
-   3 � ライト。
-   4 � 標準。
-   5 � 中。
-   6 � セミボールド。
-   7 � 太字。
-   8 � 極太。
-   9 � ヘビー。

## <a name="method-border"></a>メソッド border

コントロールの境界のスタイルを取得または設定します。

```xpp
public int border([int value])
```

### <a name="parameters---border"></a>パラメーター - border

値  
コントロールの境界スタイルとして割り当てる値 (オプション)。

### <a name="return-value---border"></a>戻り値 - border

0 (ゼロ) から 4 までの整数。

### <a name="remarks---border"></a>備考 - border

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 1 行 |
| 3     | 集合住宅        |
| 4     | None        |

### <a name="examples---border"></a>例 - border

次の例は、コントロールの境界線のスタイルを取得および設定する方法を示しています。

```xpp
// Retrieve the border style. 
info (strfmt("border: %1", this.border())); 
// Set the border style. 
this.border(2);
```

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

## <a name="method-canscroll"></a>メソッド canScroll

```xpp
public boolean canScroll([boolean value])
```

### <a name="parameters---canscroll"></a>パラメーター - canScroll

値  

### <a name="return-value---canscroll"></a>戻り値 - canScroll

## <a name="method-cascadeselect"></a>メソッド cascadeSelect

```xpp
public boolean cascadeSelect([boolean value])
```

### <a name="parameters---cascadeselect"></a>パラメーター - cascadeSelect

値  

### <a name="return-value---cascadeselect"></a>戻り値 - cascadeSelect

## <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a>パラメーター - characterSet

値  

### <a name="return-value---characterset"></a>戻り値 - characterSet

フォントの文字セット示す整数値。

### <a name="remarks---characterset"></a>備考 - characterSet

返される整数の値は、次のテーブルに従って文字セットを示します。

| 先頭値 | 説明          |
|-------|----------------------|
| 0     | ANSI\_CHARSET        |
| 1     | DEFAULT\_CHARSET     |
| 2     | SYMBOL\_CHARSET      |
| 77    | MAC\_CHARSET         |
| 128   | SHIFTJIS\_CHARSET    |
| 129   | HANGUL\_CHARSET      |
| 134   | GB2312\_CHARSET      |
| 136   | CHINESEBIG5\_CHARSET |
| 161   | GREEK\_CHARSET       |
| 162   | TURKISH\_CHARSET     |
| 163   | VIETNAMESE\_CHARSET  |
| 186   | BALTIC\_CHARSET      |
| 204   | RUSSIAN\_CHARSET     |
| 238   | EASTEUROPE\_CHARSET  |
| 255   | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 金額 | 説明    |
|-------|----------------|
| 130   | JOHAB\_CHARSET |

次のテーブルの値は、中東言語語版 Windows の値です。

| 先頭値 | 説明     |
|-------|-----------------|
| 177   | HEBREW\_CHARSET |
| 178   | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 先頭値 | 説明   |
|-------|---------------|
| 222   | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

## <a name="method-checkbox"></a>メソッド checkBox

```xpp
public boolean checkBox([boolean value])
```

### <a name="parameters---checkbox"></a>パラメーター - checkBox

値  

### <a name="return-value---checkbox"></a>戻り値- checkBox

## <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a>パラメーター - colorScheme

値  

### <a name="return-value---colorscheme"></a>戻り値 - colorScheme

ゼロから 2 までの整数。

### <a name="remarks---colorscheme"></a>備考 - colorScheme

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  
コントロールに割り当てるコンフィギュレーション キーの ID。

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

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a>戻り値 - configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

### <a name="remarks---configurationkeyex"></a>備考 - configurationKeyEx

コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。 リストに重複 ID は含まれません。

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

## <a name="method-copyitem"></a>メソッド copyItem

```xpp
public int copyItem(int Idx, int newParent, [int insertAfter])
```

### <a name="parameters---copyitem"></a>パラメーター - copyItem

Idx  

<!-- -->

newParent  

<!-- -->

insertAfter  

### <a name="return-value---copyitem"></a>戻り値 - copyItem

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

## <a name="method-createdragimagelist"></a>メソッド createDragImagelist

```xpp
public Imagelist createDragImagelist()
```

### <a name="return-value---createdragimagelist"></a>戻り値 - createDragImagelist

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

## <a name="method-delete"></a>メソッド delete

フォーム ツリー コントロールから指定した項目を削除します。

```xpp
public boolean delete(int Idx)
```

### <a name="parameters---delete"></a>パラメーター - delete

Idx  
削除する項目のゼロベース インデックスを指定する整数。

### <a name="return-value---delete"></a>戻り値 - delete

項目が正常に削除された場合は true。それ以外の場合は、false。

### <a name="examples---delete"></a>例 - delete

次の例は、フォーム ツリー コントロールの最初の項目を削除する方法を示しています。

```xpp
// The ftc variable was a previously allocated  
// FormTreeControl variable. 
boolean bDelete; 
bDelete = ftc.delete(0);
```

## <a name="method-deleteall"></a>メソッド deleteAll

フォーム ツリー コントロールからすべての項目を削除します。

```xpp
public boolean deleteAll()
```

### <a name="return-value---deleteall"></a>戻り値 - deleteAll

すべての項目が正常に削除された場合は true。それ以外の場合は、false。

### <a name="examples---deleteall"></a>例 - deleteAll

次の例は、フォーム ツリー コントロールからすべての項目を削除する方法を示しています。

```xpp
// The ftc variable was a previously allocated 
// FormTreeControl variable. 
boolean bDelete; 
bDelete = ftc.deleteAll();
```

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
ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です。

### <a name="return-value---dragdrop"></a>戻り値 - dragDrop

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="examples---dragdrop"></a>例 - dragDrop

次の例は、ドラッグ アンド ドロップの動作が有効かどうかを示す値を返すか、設定する方法を示しています。

```xpp
boolean dDragDrop; 
// The ctrl variable was previously assigned  
// as a FormTreeControl value. 
// Retrieve the drag�and�drop-enabled value. 
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

フォーム ツリー コントロールをドラッグしたときに表示されるテキストを返します。

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a>戻り値 - dragText

ツリー コントロールをドラッグしたときに表示されるテキスト。ツリー コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

## <a name="method-editlabels"></a>メソッド editLabels

```xpp
public boolean editLabels([boolean value])
```

### <a name="parameters---editlabels"></a>パラメーター - editLabels

値  

### <a name="return-value---editlabels"></a>戻り値 - editLabels

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

## <a name="method-expand"></a>メソッド expand

```xpp
public int expand(int Idx, [FormTreeExpand action])
```

### <a name="parameters---expand"></a>パラメーター - expand

Idx  

<!-- -->

アクション  

### <a name="return-value---expand"></a>戻り値 - expand

## <a name="method-expanding"></a>メソッド expanding

```xpp
public boolean expanding(int Idx, FormTreeExpand action, AnyType data)
```

### <a name="parameters---expanding"></a>パラメーター - expanding

Idx  

<!-- -->

アクション  

<!-- -->

データ  

### <a name="return-value---expanding"></a>戻り値 - expanding

## <a name="method-font"></a>戻り値 - expand

コントロール内のテキストに使用されるフォントの名前を取得または設定します。

```xpp
public str font([str value])
```

### <a name="parameters---font"></a>パラメーター - font

値  
フォーム ツリー コントロールのテキストに使用するフォントを示す文字列値。

### <a name="return-value---font"></a>戻り値 - font

Tahoma や Verdana など、使用するフォントの名前。

### <a name="examples---font"></a>例 - font

次の例は、フォーム ツリー コントロールのフォントを返して設定する方法を示しています。

```xpp
str strFont; 
// The ctrl variable was previously assigned  
// as a form tree control variable. 
// Retrieve the font. 
strFont = ctrl.font(); 
// Set the font. 
ctrl.font("Times New Roman");
```

## <a name="method-fontsize"></a>メソッド fontSize

コントロール内のテキストに使用されるフォント サイズを取得または設定します。

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a>パラメーター - fontSize

値  
フォーム ツリー コントロール内のテキストのフォント サイズ、ポイントを示す整数データ型です。

### <a name="return-value---fontsize"></a>戻り値 - fontSize

ポイント単位のフォントの高さ。

### <a name="examples---fontsize"></a>例 - fontSize

次の例は、コントロールのフォント サイズを返して設定する方法を示しています。

```xpp
int nSize; 
// The ctrl variable was previously assigned  
// as a form tree control. 
// Retrieve the font size. 
nSize = ctrl.fontSize(); 
// Set the font size. 
ctrl.fontSize(16);
```

## <a name="method-foregroundcolor"></a>メソッド foregroundColor

コントロール内のテキストに使用される色を取得または設定します。

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a>パラメーター - foregroundColor

値  

### <a name="return-value---foregroundcolor"></a>戻り値 - foregroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---foregroundcolor"></a>備考 - foregroundColor

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

## <a name="method-getchild"></a>メソッド getChild

```xpp
public int getChild(int Idx)
```

### <a name="parameters---getchild"></a>パラメーター - getChild

Idx  

### <a name="return-value---getchild"></a>戻り値 - getChild

## <a name="method-getfirstselected"></a>メソッド getFirstSelected

```xpp
public int getFirstSelected()
```

### <a name="return-value---getfirstselected"></a>戻り値 - getFirstSelected

## <a name="method-getfirstvisible"></a>メソッド getFirstVisible

```xpp
public int getFirstVisible()
```

### <a name="return-value---getfirstvisible"></a>戻り値 - getFirstVisible

## <a name="method-getimagelist"></a>メソッド getImagelist

```xpp
public Imagelist getImagelist()
```

### <a name="return-value---getimagelist"></a>戻り値 - getImagelist

## <a name="method-getitem"></a>メソッド getItem

```xpp
public FormTreeItem getItem(int Idx)
```

### <a name="parameters---getitem"></a>パラメーター - getItem

Idx  

### <a name="return-value---getitem"></a>戻り値 - getItem

## <a name="method-getnextselected"></a>メソッド getNextSelected

```xpp
public int getNextSelected(int idx)
```

### <a name="parameters---getnextselected"></a>パラメーター - getNextSelected

idx  

### <a name="return-value---getnextselected"></a>戻り値 - getNextSelected

## <a name="method-getnextsibling"></a>メソッド getNextSibling

```xpp
public int getNextSibling(int Idx)
```

### <a name="parameters---getnextsibling"></a>パラメーター - getNextSibling

Idx  

### <a name="return-value---getnextsibling"></a>戻り値 - getNextSibling

## <a name="method-getnextvisible"></a>メソッド getNextVisible

```xpp
public int getNextVisible(int Idx)
```

### <a name="parameters---getnextvisible"></a>パラメーター - getNextVisible

Idx  

### <a name="return-value---getnextvisible"></a>戻り値 - getNextVisible

## <a name="method-getparent"></a>メソッド getParent

```xpp
public int getParent(int Idx)
```

### <a name="parameters---getparent"></a>パラメーター - getParent

Idx  

### <a name="return-value---getparent"></a>戻り値 - getParent

## <a name="method-getprevselected"></a>メソッド getPrevSelected

```xpp
public int getPrevSelected(int idx)
```

### <a name="parameters---getprevselected"></a>パラメーター - getPrevSelected

idx  

### <a name="return-value---getprevselected"></a>戻り値 - getPrevSelected

## <a name="method-getprevsibling"></a>メソッド getPrevSibling

```xpp
public int getPrevSibling(int Idx)
```

### <a name="parameters---getprevsibling"></a>パラメーター - getPrevSibling

Idx  

### <a name="return-value---getprevsibling"></a>戻り値 - getPrevSibling

## <a name="method-getprevvisible"></a>メソッド getPrevVisible

```xpp
public int getPrevVisible(int Idx)
```

### <a name="parameters---getprevvisible"></a>パラメーター - getPrevVisible

Idx  

### <a name="return-value---getprevvisible"></a>戻り値 - getPrevVisible

## <a name="method-getroot"></a>メソッド getRoot

```xpp
public int getRoot()
```

### <a name="return-value---getroot"></a>戻り値 - getRoot

## <a name="method-getselectedcount"></a>メソッド getSelectedCount

```xpp
public int getSelectedCount()
```

### <a name="return-value---getselectedcount"></a>戻り値 - getSelectedCount

## <a name="method-getselection"></a>メソッド getSelection

```xpp
public int getSelection()
```

### <a name="return-value---getselection"></a>戻り値 - getSelection

## <a name="method-getstateimagelist"></a>メソッド getStateImagelist

```xpp
public Imagelist getStateImagelist()
```

### <a name="return-value---getstateimagelist"></a>戻り値 - getStateImagelist

## <a name="method-getvisiblecount"></a>メソッド getVisibleCount

ツリー コントロール内の表示されている項目の数を返します。

```xpp
public int getVisibleCount()
```

### <a name="return-value---getvisiblecount"></a>戻り値 - getVisibleCount

ツリー コントロール内の表示されている項目の数。

### <a name="examples---getvisiblecount"></a>例 - getVisibleCount

次の例は、ツリー コントロール内の表示される項目の数を取得する方法を示しています。

```xpp
int nCount; 
nCount = this.getVisibleCount(); 
info (strfmt("getVisibleCount: %1", int2str(nCount)));
```

## <a name="method-hasbuttons"></a>メソッド hasButtons

ツリー コントロールが展開/折り畳みボタンを表示するかどうかを示す値を返します。

```xpp
public boolean hasButtons([boolean value])
```

### <a name="parameters---hasbuttons"></a>パラメーター - hasButtons

値  

### <a name="return-value---hasbuttons"></a>戻り値 - hasButtons

ツリー コントロールが展開/折りたたみボタンを使用する場合は true。それ以外の場合は、false。

### <a name="examples---hasbuttons"></a>例 - hasButtons

次の例は、ツリー コントロールが展開/折りたたみボタンを使用するかどうかを示す値を取得する方法を示しています。

```xpp
boolean bHasButtons; 
// Retrieve the value. 
bHasButtons = this.hasButtons(); 
info (strfmt("hasButtons: %1",bHasButtons)); 
// Set the value. 
this.hasButtons(false);
```

## <a name="method-haschanged"></a>メソッド hasChanged

ツリー コントロールの内容が変更されたかどうかを示す値を設定するか返します。

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a>パラメーター - hasChanged

val  
ツリー コントロールの hasChanged 値として割り当てる値。

### <a name="return-value---haschanged"></a>戻り値 - hasChanged

ツリー コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="examples---haschanged"></a>例 - hasChanged

次の例は、ツリー コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。

```xpp
boolean bHasChanged; 
// The ctrl variable was previously assigned 
// as a FormTreeControl variable. 
// Retrieve the hasChanged value. 
bHasChanged = ctrl.hasChanged(); 
// Modify the hasChanged value. 
ctrl.hasChanged(true);
```

## <a name="method-haslines"></a>メソッド hasLines

ツリー コントロールがツリー コネクタ明細行を表示するかどうかを示す値を返します。

```xpp
public boolean hasLines([boolean value])
```

### <a name="parameters---haslines"></a>パラメーター - hasLines

値  

### <a name="return-value---haslines"></a>戻り値 - hasLines

ツリー コントロールにツリー コネクタ行が表示される場合は true。それ以外の場合は、false。

### <a name="examples---haslines"></a>例 - hasLines

次の例は、ツリー コントロールがツリー コネクタ ラインを表示するかどうかを示す値を取得する方法を示しています。

```xpp
boolean bHasLines; 
// Retrieve the value. 
bHasLines = this.hasLines(); 
info (strfmt("hasLines: %1", bHasLines)); 
// Set the value. 
this.hasLines(false);
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
高さの計算方法を示す整数データ型です。オプションです。 これは、次のいずれかの値になります。

<!-- -->

モード  
高さの計算方法を示す整数データ型です。オプションです。 これは、次のいずれかの値になります。

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
コントロールの高さの計算方法を示す整数データ型値です。 この値は、 Exact モードの場合は -1、Auto モードの場合は 0、Column height モードの場合は 1 になります。

### <a name="return-value---heightmode"></a>戻り値 - heightMode

高さ計算モード。

### <a name="remarks---heightmode"></a>備考 - heightMode

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| 正確         | ピクセル単位のコントロールの正確な高さが使用されます。                                         |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                               |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="examples---heightmode"></a>例 - heightMode

次の例は、ツリー コントロールの高さ計算モードを返して設定する方法を示しています。

```xpp
int nHeightMode; 
; 
// The ctrl variable was previously assigned 
// as a form tree control variable. 
// Retrieve the height mode. 
nHeightMode = ctrl.HeightMode(); 
// Set the height mode. 
ctrl.heightMode(-1); 
// Set the height. 
ctrl.heightValue(160);
```

## <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  
高さをピクセル単位で指定する整数データ型です。

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

ピクセル単位の高さ。

### <a name="remarks---heightvalue"></a>備考 - heightValue

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="examples---heightvalue"></a>例 - heightValue

次の例は、フォーム ツリー コントロールの高さの値を返して設定する方法を示しています。

```xpp
int nHeightValue; 
// The ctrl variable was previously assigned 
// as a form tree control variable. 
// Retrieve the height value. 
nHeightValue = ctrl.heightValue(); 
// Set the height value. 
ctrl.heightMode(-1); 
ctrl.heightValue(160);
```

## <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを返します。

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
// Retrieve existing Help text. 
print objCtrl.helpText(); 
// Specify new Help text. 
objCtrl.helpText("My new Help text");
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

## <a name="method-hittest"></a>メソッド hitTest

```xpp
public container hitTest(int x, int y)
```

### <a name="parameters---hittest"></a>パラメーター - hitTest

x  

<!-- -->

y  

### <a name="return-value---hittest"></a>戻り値 - hitTest

## <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを返します。

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

## <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナーかどうかを示す値を返します。

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a>戻り値 - isContainer

コントロールがコンテナーである場合は true。それ以外の場合は false。

### <a name="examples---iscontainer"></a>例 - isContainer

次の例は、コントロールがコンテナーであるかどうかを判断する方法を示しています。

```xpp
info(strfmt("IsContainer: %1", this.isContainer()));
```

## <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を返します。

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

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。 「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="remarks---isusersetupenabled"></a>備考 - isUserSetupEnabled

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

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

## <a name="method-italic"></a>メソッド italic

コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a>パラメーター - italic

値  
コントロールのイタリック設定に割り当てる値。

### <a name="return-value---italic"></a>戻り値 - italic

コントロール内のテキストが斜体である場合は true。それ以外の場合は false。

## <a name="method-keydown"></a>メソッド keyDown

```xpp
public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)
```

### <a name="parameters---keydown"></a>パラメーター - keyDown

vKey  

<!-- -->

Ctrl  

<!-- -->

Shift  

### <a name="return-value---keydown"></a>戻り値 - keyDown

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

## <a name="method-linesatroot"></a>メソッド linesAtRoot

```xpp
public boolean linesAtRoot([boolean value])
```

### <a name="parameters---linesatroot"></a>パラメーター - linesAtRoot

値  

### <a name="return-value---linesatroot"></a>戻り値 - linesAtRoot

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

### <a name="examples---mousedblclick"></a>例 - mouseDblClick

次の例は、Infolog に mouseDblClick イベントのパラメーターを表示する方法を示しています。

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
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがマウス ポインターがコントロール上にある状態でクリックすると呼び出されます。

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
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
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

### <a name="remarks---mousemove"></a>備考 - mouseMove

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="examples---mousemove"></a>例 - mouseMove

次の例は、Infolog に mouseMove イベントのパラメーターを表示する方法を示しています。

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
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mouseup"></a>メソッド mouseUp

マウス ポインターがコントロール上にある状態で、ユーザーがマウス ボタンを放すと呼び出されます。

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
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-moveitem"></a>メソッド moveItem

```xpp
public int moveItem(int Idx, int newParent, [int insertAfter])
```

### <a name="parameters---moveitem"></a>パラメーター - moveItem

Idx  

<!-- -->

newParent  

<!-- -->

insertAfter  

### <a name="return-value---moveitem"></a>戻り値 - moveItem

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

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
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

## <a name="method-rowselect"></a>メソッド rowSelect

```xpp
public boolean rowSelect([boolean value])
```

### <a name="parameters---rowselect"></a>パラメーター - rowSelect

値  

### <a name="return-value---rowselect"></a>戻り値 - rowSelect

## <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  
コントロールに割り当てるセキュリティ キーの ID。

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

## <a name="method-select"></a>メソッド select

```xpp
public int select(int Idx)
```

### <a name="parameters---select"></a>パラメーター - select

Idx  

### <a name="return-value---select"></a>戻り値 - select

## <a name="method-selectex"></a>メソッド selectEx

```xpp
public int selectEx(int Idx, boolean setSelection)
```

### <a name="parameters---selectex"></a>パラメーター - selectEx

Idx  

<!-- -->

setSelection  

### <a name="return-value---selectex"></a>戻り値 - selectEx

## <a name="method-selectionchanging"></a>メソッド selectionChanging

```xpp
public boolean selectionChanging(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)
```

### <a name="parameters---selectionchanging"></a>パラメーター - selectionChanging

OldItem  

<!-- -->

NewItem  

<!-- -->

how  

### <a name="return-value---selectionchanging"></a>戻り値 - selectionChanging

## <a name="method-selectitems"></a>メソッド selectItems

```xpp
public int selectItems(int fromIdx, int toIdx)
```

### <a name="parameters---selectitems"></a>パラメーター - selectItems

fromIdx  

<!-- -->

toIdx  

### <a name="return-value---selectitems"></a>戻り値 - selectItems

## <a name="method-selectsetfirstvisible"></a>メソッド selectSetFirstVisible

```xpp
public int selectSetFirstVisible(int Idx)
```

### <a name="parameters---selectsetfirstvisible"></a>パラメーター - selectSetFirstVisible

Idx  

### <a name="return-value---selectsetfirstvisible"></a>戻り値 - selectSetFirstVisible

## <a name="method-setinsertmark"></a>メソッド setInsertMark

```xpp
public boolean setInsertMark(int Idx, boolean After)
```

### <a name="parameters---setinsertmark"></a>パラメーター - setInsertMark

Idx  

<!-- -->

変更後  

### <a name="return-value---setinsertmark"></a>戻り値 - setInsertMark

## <a name="method-setitem"></a>メソッド setItem

```xpp
public boolean setItem(FormTreeItem item)
```

### <a name="parameters---setitem"></a>パラメーター - setItem

品目  

### <a name="return-value---setitem"></a>戻り値 - setItem

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

## <a name="method-showselalways"></a>メソッド showSelAlways

```xpp
public boolean showSelAlways([boolean value])
```

### <a name="parameters---showselalways"></a>パラメーター - showSelAlways

値  

### <a name="return-value---showselalways"></a>戻り値 - showSelAlways

## <a name="method-singleselection"></a>メソッド singleSelection

```xpp
public boolean singleSelection([boolean value])
```

### <a name="parameters---singleselection"></a>パラメーター - singleSelection

値  

### <a name="return-value---singleselection"></a>戻り値 - singleSelection

## <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  
コントロールの skip プロパティに割り当てる値。

### <a name="return-value---skip"></a>戻り値 - skip

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="remarks---skip"></a>備考 - skip

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="examples---skip"></a>例 - skip

以下は、コントロールのスキップ プロパティを返す方法と設定する方法を示しています。

```xpp
// Return the value of the skip property. 
info(strfmt("skip: %1", this.skip())); 
// Set the value of the skip property. 
this.skip(true);
```

## <a name="method-tooltip"></a>メソッド toolTip

コントロールのツールヒント テキストを返します。

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

## <a name="method-trackselect"></a>メソッド trackSelect

```xpp
public boolean trackSelect([boolean value])
```

### <a name="parameters---trackselect"></a>パラメーター - trackSelect

値  

### <a name="return-value---trackselect"></a>戻り値 - trackSelect

## <a name="method-type"></a>メソッドのタイプ

```xpp
public int type([int value])
```

### <a name="parameters---type"></a>パラメーター - type

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-underline"></a>メソッド underline

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a>パラメーター - underline

値  

### <a name="return-value---underline"></a>戻り値 - underline

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

フォーム ツリー コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a>パラメーター - userHide

値  
フォーム ツリー コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

### <a name="return-value---userhide"></a>戻り値 - userHide

ツリー コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

### <a name="remarks---userhide"></a>備考 - userHide

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="examples---userhide"></a>例 - userHide

次の例は、フォーム ツリー コントロールがユーザーから隠されているかどうかを指定する値を返して設定する方法を示しています。

```xpp
int nUserHide; 
// The ctrl variable was previously assigned  
// as a form tree control variable. 
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

コントロールのユーザー プロンプト テキストを設定または取得します。

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a>パラメーター - userPromptText

値  
コントロールのユーザー プロンプト テキストとして割り当てる値。

### <a name="return-value---userprompttext"></a>戻り値 - userPromptText

コントロールのユーザー プロンプト テキスト。コントロールにユーザー プロンプト テキストが割り当てられていない場合は空の文字列。

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
userSkip プロパティに割り当てる値。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

### <a name="return-value---userskip"></a>戻り値 - userSkip

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="examples---userskip"></a>例 - userSkip

次の例は、userSkip プロパティを返して設定する方法を示しています。

```xpp
int nUserSkip 
// The ctrl variable was previously assigned 
// as a FormTreeControl value. 
// Return the userSkip property. 
nUserSkip = ctrl.userSkip(); 
// Set the userSkip property. 
ctrl.userSkip(1);
```

## <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

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

次の例は、フォーム ツリー コントロールのユーザーの幅を返して設定する方法を示しています。

```xpp
int nWidth; 
// The ctrl variable was previously defined 
// as a FormTreeControl value. 
// Return the width. 
nWidth = ctrl.userWidth(); 
// Specify the width. 
ctrl.userWidth(90);  // 15 characters * 6 pixels == 90
```

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
コントロールの可視化設定に割り当てる値。

### <a name="return-value---visible"></a>戻り値 - visible

コントロールが可視である場合は true。それ以外の場合は false。

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  
幅の計算方法を示す整数。オプション。

<!-- -->

モード  
幅の計算方法を示す整数。オプション。

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
コントロールの幅の計算方法を示す整数データ型値です。 この値は、 Exact モードの場合は -1、Auto モードの場合は 0、Column width モードの場合は 1 になります。

### <a name="return-value---widthmode"></a>戻り値 - widthMode

現在の幅の計算モードを示す整数値。

### <a name="remarks---widthmode"></a>備考 - widthMode

次の表に従って幅を計算します。

| モード         | 幅計算                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="examples---widthmode"></a>例 - widthMode

次の例は、フォーム ツリー コントロールの幅計算モードを返して設定する方法を示しています。

```xpp
int nWidthMode; 
// The ctrl variable was previously assigned 
// as a form tree control value. 
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
幅をピクセル単位で指定する整数データ型です。

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="examples---widthvalue"></a>例 - widthValue

次の例は、フォーム ツリー コントロールの幅の値を返して設定する方法を示しています。

```xpp
int nWidthValue; 
// The ctrl variable was previously assigned 
// as a form tree control value. 
// Retrieve the width value. 
nWidthValue = ctrl.widthValue(); 
// Set the width value. 
ctrl.widthMode(-1); 
ctrl.widthValue(160);
```

## <a name="method-checkedstatechanged"></a>メソッド checkedStateChanged

```xpp
public void checkedStateChanged(int Idx, FormTreeCheckedState newState)
```

### <a name="parameters---checkedstatechanged"></a>パラメーター - checkedStateChanged

Idx  

<!-- -->

newState  

## <a name="method-endlabeledit"></a>メソッド endLabelEdit

```xpp
public void endLabelEdit(int Idx, str text, AnyType data)
```

### <a name="parameters---endlabeledit"></a>パラメーター - endLabelEdit

Idx  

<!-- -->

テキスト  

<!-- -->

データ  

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

## <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。

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

### <a name="remarks---mouseenter"></a>備考 - mouseEnter

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

## <a name="method-onexpanding"></a>メソッド OnExpanding

```xpp
private void OnExpanding([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onexpanding"></a>パラメーター - OnExpanding

sender  

<!-- -->

e  

## <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

```xpp
public void cut()
```

## <a name="method-paste"></a>メソッド paste

フォーム ツリー コントロールをフォームに貼り付けます。

```xpp
public void paste()
```

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

```xpp
public void resetUserSetting()
```

## <a name="method-itemmoved"></a>メソッド itemMoved

```xpp
public void itemMoved(int OldIdx, int NewIdx)
```

### <a name="parameters---itemmoved"></a>パラメーター - itemMoved

OldIdx  

<!-- -->

NewIdx  

## <a name="method-expanded"></a>パラメーター - expand

```xpp
public void expanded(int Idx, FormTreeExpand action, AnyType data)
```

### <a name="parameters---expanded"></a>パラメーター - expanded

Idx  

<!-- -->

アクション  

<!-- -->

データ  

## <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

```xpp
public void setFocus()
```

## <a name="method-onselectionchanged"></a>メソッド OnSelectionChanged

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a>パラメーター - OnSelectionChanged

sender  

<!-- -->

e  

## <a name="method-onlostfocus"></a>メソッド OnLostFocus

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a>パラメーター - OnLostFocus

sender  

<!-- -->

e  

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

## <a name="method-mouseleave"></a>メソッド mouseLeave

ユーザーがマウス ポインターをコントロールから移動させると呼び出されます。

```xpp
public void mouseLeave()
```

### <a name="examples---mouseleave"></a>例 - mouseLeave

次の例では、マウス ポインタがコントロール エリアを離れるときに情報ログに書き込みます。

```xpp
public void mouseLeave() 
{ 
    info (strfmt("The mouse has left the %1 control.", this.name()) ); 
    super(); 
}
```

## <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム ツリー コントロールのドラッグを終了すると呼び出されます。

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a>備考 - endDrag

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="examples---enddrag"></a>例 - endDrag

次の例では、ユーザーがツリー コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。

```xpp
public void endDrag() 
{ 
    info("EndDrag completed"); 
    super(); 
}
```

## <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

```xpp
public void context()
```

## <a name="method-itemcopy"></a>メソッド itemCopy

```xpp
public void itemCopy(int OldIdx, int NewIdx)
```

### <a name="parameters---itemcopy"></a>パラメーター - itemCopy

OldIdx  

<!-- -->

NewIdx  

## <a name="method-enter"></a>メソッド enter

```xpp
public void enter()
```

## <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a>パラメーター - inputSearch

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

## <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

```xpp
public void displayControl()
```

## <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム ツリー コントロールの最適な列の幅と高さを指定します。

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a>パラメーター - prefColumnSize

width  
コントロールの適切な高さはピクセルで測定します。

<!-- -->

height  
コントロールの適切な高さはピクセルで測定します。

### <a name="examples---prefcolumnsize"></a>例 - prefColumnSize

次の例は、ツリー コントロールの優先幅と高さを設定する方法を示しています。

```xpp
// The nWidth and nHeight variables were previously assigned 
// as int variables. 
// The ctrl variable was previously assigned 
// as a FormTreeControl value. 
ctrl.prefColumnSize( nWidth, nHeight);
```

## <a name="method-setimagelist"></a>メソッド setImagelist

```xpp
public void setImagelist(Imagelist imageList)
```

### <a name="parameters---setimagelist"></a>パラメーター - setImagelist

imageList  

## <a name="method-onexpanded"></a>メソッド OnExpanded

```xpp
private void OnExpanded([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onexpanded"></a>パラメーター - OnExpanded

sender  

<!-- -->

e  

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

## <a name="method-onenter"></a>メソッド OnEnter

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a>パラメーター - OnEnter

sender  

<!-- -->

e  

## <a name="method-itemdeleted"></a>メソッド itemDeleted

```xpp
public void itemDeleted(int Idx, AnyType data)
```

### <a name="parameters---itemdeleted"></a>パラメーター - itemDeleted

Idx  

<!-- -->

データ  

## <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

```xpp
public void gotFocus()
```

## <a name="method-setstateimagelist"></a>メソッド setStateImagelist

```xpp
public void setStateImagelist(Imagelist imageList)
```

### <a name="parameters---setstateimagelist"></a>パラメーター - setStateImagelist

imageList  

## <a name="method-endeditlabel"></a>メソッド endEditLabel

```xpp
public void endEditLabel(boolean cancel)
```

### <a name="parameters---endeditlabel"></a>パラメーター - endEditLabel

キャンセル  

## <a name="method-copy"></a>メソッド copy

フォーム ツリー コントロールをコピーします。

```xpp
public void copy()
```

## <a name="method-ongotfocus"></a>メソッド OnGotFocus

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a>パラメーター - OnGotFocus

sender  

<!-- -->

e  

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

## <a name="method-onleaving"></a>メソッド OnLeaving

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a>パラメーター - OnLeaving

sender  

<!-- -->

e  

## <a name="method-selectionchanged"></a>メソッド selectionChanged

ユーザーがフォーム ツリー コントロールで選択した項目を変更したことを示します。

```xpp
public void selectionChanged(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)
```

### <a name="parameters---selectionchanged"></a>パラメーター - selectionChanged

OldItem  
\_NewItem パラメーターで指定された項目がどのように選択されたかを示す値。

<!-- -->

NewItem  
\_NewItem パラメーターで指定された項目がどのように選択されたかを示す値。

<!-- -->

how  
\_NewItem パラメーターで指定された項目がどのように選択されたかを示す値。

## <a name="method-begineditlabel"></a>メソッド beginEditLabel

```xpp
public void beginEditLabel(int Idx)
```

### <a name="parameters---begineditlabel"></a>パラメーター - beginEditLabel

Idx  

