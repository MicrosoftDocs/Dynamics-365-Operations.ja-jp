---
title: FormListControl クラス
description: このトピックでは、FormListControl クラスについて説明します。
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
ms.openlocfilehash: b81ba8891d59eca89781f5d650b48289ea74af53
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502936"
---
# <a name="class-formlistcontrol"></a>クラス FormListControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormListControl extends FormControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int add(str Text, \[int image\], \[int index\])                                                      |                                                                                                                                                                         |
| public boolean addColumn(int Idx, FormListColumn Column)                                                    |                                                                                                                                                                         |
| public int addItem(FormListItem item)                                                                       |                                                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                              | コントロールが他のコントロールと揃っているかどうかを決定します。                                                                                                          |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を修正できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean arrangeItem(FormListArrange ArrangeMethod)                                                   |                                                                                                                                                                         |
| public boolean autoArrange(\[boolean value\])                                                               |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                           |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムの移動を開始するときを識別します。                                                                          |
| public int bold(\[int value\])                                                                              | コントロール内のテキストに使用されるフォントの重量を取得または設定します。                                                                                                     |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public container calcControlSize(int chars, int lines)                                                      | 文字数と明細行数に基づいて、フォームのリスト コントロールに使用されるフォント サイズを計算します。                                               |
| public boolean canScroll(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public boolean checkBox(\[boolean value\])                                                                  |                                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public boolean columnHeader(\[boolean value\])                                                              | フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型値を設定または取得します。                                                                  |
| public boolean columnHeaderButton(\[boolean value\])                                                        | フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型値を設定または取得します。                                                           |
| public boolean columnImages(\[boolean value\])                                                              | フォーム リスト コントロールに列イメージが含まれるかどうかを示すブール値データ型値を設定または取得します。                                                                    |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。                                                                |
| public int copyItem(int Item, int InsertAt)                                                                 | 指定した項目をフォーム リスト コントロールにコピーします。                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public boolean delete(int Idx)                                                                              | フォーム リスト コントロールから指定した項目を削除します。                                                                                                                      |
| public boolean deleteAll()                                                                                  | フォーム リスト コントロールからすべての項目を削除します。                                                                                                                         |
| public boolean deleteColumn(int Idx)                                                                        | フォーム リスト コントロールの指定した列を削除します。                                                                                                                      |
| public int displayTarget(\[int value\])                                                                     | クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | ユーザーがフォーム リスト コントロールの境界内のアイテムにオブジェクトをドラッグするときを識別します。                                                                           |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム リスト コントロールでユーザーが項目をドラッグしたときに表示されるテキストを取得します。                                                                                  |
| public boolean editLabels(\[boolean value\])                                                                | ユーザーがフォーム リスト コントロールで項目名を変更できるかどうかを示します。                                                                                                   |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public int ensureVisible(int Idx)                                                                           |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | コントロールのテキストの色を取得または設定します。                                                                                                                            |
| public FormListColumn getColumn(int Idx)                                                                    | フォーム リスト コントロール内の指定された列の FormListColumn オブジェクトを取得します。                                                                                        |
| public int getColumnCount()                                                                                 | フォーム リスト コントロール内の列の数を取得します。                                                                                                                 |
| public int getColumnWidth(int Idx)                                                                          | フォーム リスト コントロール内の列の幅を取得します。                                                                                                                 |
| public int getCount()                                                                                       | フォーム リスト コントロールに含まれる項目の数を取得します。                                                                                                |
| public int getCountPerPage()                                                                                |                                                                                                                                                                         |
| public Imagelist getImagelist(\[boolean GetLarge\])                                                         |                                                                                                                                                                         |
| public FormListItem getItem(int Idx, \[int SubItem\])                                                       | フォーム リスト コントロール内の項目の FormListItem オブジェクトを取得します。                                                                                                     |
| public container getItemPos(int Item)                                                                       | フォーム リスト コントロール内の項目の位置を取得します。                                                                                                               |
| public int getNextItem(FormListNext nextType, \[int startIdx\])                                             | フォーム リスト コントロール内の次の項目の数を取得します。                                                                                                           |
| public int getSelectedCount()                                                                               | フォーム リスト コントロールで選択されている項目の数を取得します。                                                                                                 |
| public int getStringWidth(str Text)                                                                         |                                                                                                                                                                         |
| public int getTopIndex()                                                                                    |                                                                                                                                                                         |
| public boolean gridLines(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public boolean headerdragdrop(\[boolean value\])                                                            |                                                                                                                                                                         |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public container hitTest(int x, int y)                                                                      |                                                                                                                                                                         |
| public container hitTestSubItem(int x, int y)                                                               |                                                                                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                        |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public int itemAlign(\[int value\])                                                                         |                                                                                                                                                                         |
| public boolean itemChanging(int Idx, AnyType Data)                                                          |                                                                                                                                                                         |
| public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)                                               |                                                                                                                                                                         |
| public boolean leave()                                                                                      | ユーザーがフォーム リスト コントロールからフォーカスを移動したら識別します。                                                                                                       |
| public int left(int value, \[int mode\])                                                                    | フォーム リスト コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。                                                 |
| public int leftMode(\[int value\])                                                                          | フォーム リスト コントロールの水平位置を計算する方法を示す値を設定するか返します。                                                                |
| public int leftValue(\[int value\])                                                                         | フォーム リスト コントロールの水平位置をピクセル単位で設定するか返します。                                                                                               |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがマウスの左ボタンが押すときを識別します。                                                                                                                   |
| public int moveItem(int Item, int InsertAt)                                                                 | 指定した項目をフォーム リスト コントロールに移動します。                                                                                                                          |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public boolean oneClickActivate(\[boolean value\])                                                          |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public boolean redrawItems(int idxFirst, int idxLast)                                                       | フォーム リスト コントロール内の広範囲の項目を更新します。                                                                                                                        |
| public boolean rowSelect(\[boolean value\])                                                                 | 行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型値を設定または取得します。                                         |
| public boolean scroll(int dx, int dy)                                                                       |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public boolean selectionChanging(int Idx, AnyType Data)                                                     |                                                                                                                                                                         |
| public boolean setColumn(int Idx, FormListColumn Column)                                                    |                                                                                                                                                                         |
| public boolean setColumnWidth(int Idx, int Width)                                                           | フォーム リスト コントロール内の列の幅を指定します。                                                                                                                 |
| public boolean setItem(FormListItem item)                                                                   | フォーム リスト コントロールに項目が含まれているかどうかを示します。                                                                                                          |
| public Imagelist setStateImagelist(Imagelist imageList)                                                     |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                  | ショートカット メニューがいつ表示されるかを示します。                                                                                                                                |
| public boolean showSelAlways(\[boolean value\])                                                             |                                                                                                                                                                         |
| public boolean singleSelection(\[boolean value\])                                                           | フォーム リスト コントロールで複数の項目を選択できるかどうかを示します。                                                                                                |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean sortTextItems(\[int column\], \[boolean ascending\])                                         |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。                                                   |
| public int topMode(\[int value\])                                                                           | フォーム リスト コントロールの垂直位置を計算する方法を示す値を設定するか返します。                                                                 |
| public int topValue(\[int value\])                                                                          | フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返します。                                                                                                 |
| public boolean trackSelect(\[boolean value\])                                                               |                                                                                                                                                                         |
| public boolean twoClickActivate(\[boolean value\])                                                          |                                                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティの値を設定するか返します。                                                                                        |
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
| public int userWidth(\[int value\])                                                                         | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定または取得し、スペースを計算する方法を指定します。                                              |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォーム リスト コントロールの上と下のスペースを計算する方法を示す値を設定するか返します。                                                                 |
| public int verticalSpacingValue(\[int value\])                                                              | ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定するか返します。                                                                                      |
| public int viewType(\[int value\])                                                                          |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void selectionChanged(int Idx, AnyType Data)                                                         |                                                                                                                                                                         |
| public void activateItem(int Idx)                                                                           |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定されたテキスト文字列の検索開始日を示します。                                                                                                          |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void update(\[int idx\])                                                                             | コントロールを更新します。                                                                                                                                                    |
| public void endDrag()                                                                                       | ユーザーがフォーム リスト コントロールの移動を終了した日を示します。                                                                                                       |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void setImagelist(Imagelist imageList, \[boolean SetLarge\])                                         |                                                                                                                                                                         |
| public void copy()                                                                                          | ユーザーがコピー操作を実行するときを識別します。                                                                                                                       |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void itemCopy(int Idx, int newIdx)                                                                   |                                                                                                                                                                         |
| public void cut()                                                                                           | ユーザーがカット操作を実行するときを識別します。                                                                                                                      |
| public void itemMoved(int Idx, int newIdx)                                                                  |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])                         |                                                                                                                                                                         |
| public void hotTrackItem(int Idx)                                                                           | ユーザーがマウス ポインターをフォーム リスト コントロール上に移動するときを識別します。                                                                                                |
| public void setCount(int count)                                                                             |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | ユーザーがフォーム リスト コントロールの境界からオブジェクトをドラッグするときを識別します。                                                                                        |
| public void itemDeleted(int Idx, AnyType Data)                                                              |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void setText(int Idx, str Text, \[int SubItem\])                                                     |                                                                                                                                                                         |
| public void itemChanged(int Idx, AnyType Data)                                                              |                                                                                                                                                                         |
| public void doubleClick()                                                                                   | ユーザーがフォーム内のリスト コントロールのアイテムをダブルクリックするときを識別します。                                                                                                    |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void allItemsDeleted()                                                                               | フォーム リスト コントロール内のすべてのアイテムが削除される日を示します。                                                                                                       |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムを新しい位置にドロップするときを識別します。                                                                 |
| public void columnClicked(int Column)                                                                       | ユーザーがフォーム内のリスト ビュー コントロールの列をクリックするときを識別します。                                                                                                |
| public void getStateImagelist()                                                                             |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void setItemPos(int Item, int x, int y)                                                              | フォーム リスト コントロール内の項目の位置を設定します。                                                                                                                    |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void enter()                                                                                         |                                                                                                                                                                         |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void context()                                                                                       | ユーザーがショートカット メニューをフォーム リスト コントロールで開くときを識別します。                                                                                                  |
| public void beginEditLabel(int Idx)                                                                         |                                                                                                                                                                         |
| public void itemInserted(int Idx, AnyType Data)                                                             |                                                                                                                                                                         |

## <a name="method-add"></a>メソッド add

```xpp
public int add(str Text, [int image], [int index])
```

### <a name="parameters---add"></a>パラメーター - add

テキスト  

<!-- -->

画像  

<!-- -->

指数  

### <a name="return-value---add"></a>戻り値 - add

## <a name="method-addcolumn"></a>メソッド addColumn

```xpp
public boolean addColumn(int Idx, FormListColumn Column)
```

### <a name="parameters---addcolumn"></a>パラメーター - addColumn

Idx  

<!-- -->

円柱  

### <a name="return-value---addcolumn"></a>戻り値 - addColumn

## <a name="method-additem"></a>メソッド addItem

```xpp
public int addItem(FormListItem item)
```

### <a name="parameters---additem"></a>パラメーター - addItem

品目  

### <a name="return-value---additem"></a>戻り値 - addItem

## <a name="method-aligncontrol"></a>メソッド alignControl

コントロールが他のコントロールと揃っているかどうかを決定します。

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a>パラメーター - alignControl

値  
フォーム リスト コントロールが他のコントロールと一致しているかどうかを示すブール値。

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
データを変更できるかどうかを示すブール値データ型。

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを変更することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

## <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a>戻り値 - allowSysSetup

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

## <a name="method-arrangeitem"></a>メソッド arrangeItem

```xpp
public boolean arrangeItem(FormListArrange ArrangeMethod)
```

### <a name="parameters---arrangeitem"></a>パラメーター - arrangeItem

ArrangeMethod  

### <a name="return-value---arrangeitem"></a>戻り値 - arrangeItem

## <a name="method-autoarrange"></a>メソッド autoArrange

```xpp
public boolean autoArrange([boolean value])
```

### <a name="parameters---autoarrange"></a>パラメーター - autoArrange

値  

### <a name="return-value---autoarrange"></a>戻り値 - autoArrange

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  
システムがフォーム リスト コントロールと同じ名前の変数を宣言できるかどうかを示すブール データ型。

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

### <a name="remarks---autodeclaration"></a>備考 - autoDeclaration

コントロールには同じ名前を付けることはできません。

### <a name="examples---autodeclaration"></a>例 - autoDeclaration

次の例は、システムがフォーム リスト コントロールと同じ名前を持つ変数を宣言できることを指定する autoDeclaration メソッドの呼び出しを示しています。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.autoDeclaration(true); 
}
```

## <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a>パラメーター - backgroundColor

値  
背景色を指定する整数データ型です。

### <a name="return-value---backgroundcolor"></a>戻り値 - backgroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---backgroundcolor"></a>備考 - backgroundColor

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

## <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a>パラメーター - backStyle

値  
背景スタイルを示す整数データ型です。

### <a name="return-value---backstyle"></a>戻り値 - backStyle

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

## <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムの移動を開始するときを識別します。

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a>パラメーター - beginDrag

x  
移動イベントのための y 座標を示す整数データ型です。

<!-- -->

y  
移動イベントのための y 座標を示す整数データ型です。

### <a name="return-value---begindrag"></a>戻り値 - beginDrag

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---begindrag"></a>備考 - beginDrag

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [beginDrag] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-bold"></a>メソッド bold

コントロール内のテキストに使用されるフォントの重量を取得または設定します。

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a>パラメーター - bold

値  
フォントの太さを指定する整数データ型です。

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

### <a name="examples---bold"></a>例 - bold

次の例は、フォントの重量を、重いことを示す、9 に設定する太字のメソッドの呼び出しを示しています。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    int boldLevel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    boldLevel = formListControl.bold(9); 
}
```

## <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

```xpp
public int border([int value])
```

### <a name="parameters---border"></a>パラメーター - border

値  

### <a name="return-value---border"></a>戻り値 - border

ゼロから 4 までの整数。

### <a name="remarks---border"></a>備考 - border

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 単一明細行 |
| 3     | 均一        |
| 4     | None        |

## <a name="method-calccontrolsize"></a>メソッド calcControlSize

文字数と明細行数に基づいて、フォームのリスト コントロールに使用されるフォント サイズを計算します。

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a>パラメーター - calcControlSize

chars  
行数を指定する整数データ型です。

<!-- -->

明細行  
行数を指定する整数データ型です。

### <a name="return-value---calccontrolsize"></a>戻り値 - calcControlSize

フォーム リスト コントロールのサイズを指定するコンテナー データ型値。

## <a name="method-canscroll"></a>メソッド canScroll

```xpp
public boolean canScroll([boolean value])
```

### <a name="parameters---canscroll"></a>パラメーター - canScroll

値  

### <a name="return-value---canscroll"></a>戻り値 - canScroll

## <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a>パラメーター - characterSet

値  
テキスト フォントの文字セットを指定する整数データ型です。

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

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づいて設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

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
フォーム リスト コントロールのカラー パレットを指定する整数データ型です。

### <a name="return-value---colorscheme"></a>戻り値 - colorScheme

0 (ゼロ) から 2 までの整数。

### <a name="remarks---colorscheme"></a>備考 - colorScheme

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

## <a name="method-columnheader"></a>メソッド columnHeader

フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型値を設定または取得します。

```xpp
public boolean columnHeader([boolean value])
```

### <a name="parameters---columnheader"></a>パラメーター - columnHeader

値  
フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型。

### <a name="return-value---columnheader"></a>戻り値 - columnHeader

コントロールに列ヘッダーがある場合は true。それ以外の場合は、false。

### <a name="remarks---columnheader"></a>備考 - columnHeader

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。 フォームに列を追加する前に、columnHeader メソッドを呼び出す必要があります。それ以外の場合、列はフォーム リスト コントロールに表示されません。

### <a name="examples---columnheader"></a>例 - columnHeader

次の例は、フォーム リスト コントロールに列ヘッダーがないことを示す columnHeader メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    boolean columnHeader; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    columnHeader = formListControl.columnHeader(false); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
}
```

## <a name="method-columnheaderbutton"></a>メソッド columnHeaderButton

フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型値を設定または取得します。

```xpp
public boolean columnHeaderButton([boolean value])
```

### <a name="parameters---columnheaderbutton"></a>パラメーター - columnHeaderButton

値  
フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型。

### <a name="return-value---columnheaderbutton"></a>戻り値 - columnHeaderButton

コントロールに列ヘッダー ボタンがある場合は true。それ以外の場合は、false。

### <a name="remarks---columnheaderbutton"></a>備考 - columnHeaderButton

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。 フォームに列を追加する前に、columnHeaderButton メソッドを呼び出す必要があります。それ以外の場合、列はフォーム リスト コントロールに表示されません。

### <a name="examples---columnheaderbutton"></a>例 - columnHeaderButton

次の例は、フォーム リスト コントロールに列ヘッダー ボタンがあることを示す columnHeaderButton メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    boolean columnHeaderBtn; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    columnHeaderBtn = formListControl.columnHeaderButton(true); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
}
```

## <a name="method-columnimages"></a>メソッド columnImages

フォーム リスト コントロールに列イメージが含まれるかどうかを示すブール値データ型値を設定または取得します。

```xpp
public boolean columnImages([boolean value])
```

### <a name="parameters---columnimages"></a>パラメーター - columnImages

値  
フォーム リスト コントロールに列の画像が含まれるかどうかを示すブール値データ型。

### <a name="return-value---columnimages"></a>戻り値 - columnImages

フォーム リスト コントロールに列イメージがある場合は true。それ以外の場合は、false。

### <a name="remarks---columnimages"></a>備考 - columnImages

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

### <a name="examples---columnimages"></a>例 - columnImages

次の例は、フォーム リスト コントロールに列イメージがあることを示す columnImages メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。


```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.columnImages(true); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
}
```

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  
コンフィギュレーション キーの ID を特定する configurationKeyId システム データ型。

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="examples---configurationkey"></a>例 - configurationKey

次の例は、フォーム リスト コントロールに銀行コンフィギュレーション キーを割り当てる configurationKey メソッドの呼び出しを示しています。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    configurationKeyId ID; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run time-form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    ID = formListControl.configurationKey(configurationKeyNum(Bank)); 
}
```

## <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a>戻り値 - configurationKeyEx

フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリスト オブジェクト。

### <a name="remarks---configurationkeyex"></a>備考 - configurationKeyEx

コントロールがデータソースにバインドされている場合、取得された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 さらに、取得したリストには、拡張データ型に適用される任意のコンフィギュレーション キー ID が含まれます。 リストに重複 ID は含まれません。

### <a name="examples---configurationkeyex"></a>例 - configurationKeyEx

次の例は、configurationKeyEx メソッドの呼び出しを示しています。 ListEnumerator オブジェクトを使用すると、一覧全体の要素上を移動できます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    configurationKeyId ID; 
    List list; 
    ListEnumerator enum; 
    DictConfigurationKey dck; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    ID = formListControl.configurationKey(configurationKeyNum(Bank)); 
    list = formListControl.configurationKeyEx(); 
    if (0 != list.elements()) 
    { 
        enum = list.getEnumerator(); 
        while (enum.moveNext()) 
        { 
            dck = new DictConfigurationKey(enum.current()); 
            if (dck) 
            { 
                print strfmt("Configuration Key ID: %1" 
                  + "Configuration Key Name: %2",enum.current(),dck.name()); 
                pause; 
            } 
        } 
    } 
}
```

## <a name="method-copyitem"></a>メソッド copyItem

指定した項目をフォーム リスト コントロールにコピーします。

```xpp
public int copyItem(int Item, int InsertAt)
```

### <a name="parameters---copyitem"></a>パラメーター - copyItem

項目  
品目がコピーされるリスト内の位置を指定する整数データ型です。

<!-- -->

InsertAt  
品目がコピーされるリスト内の位置を指定する整数データ型です。

### <a name="return-value---copyitem"></a>戻り値 - copyItem

品目がコピーされるリスト内の位置を指定する整数データ型です。

### <a name="remarks---copyitem"></a>備考 - copyItem

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

### <a name="examples---copyitem"></a>例 - copyItem

次の例は、フォーム リスト コントロールの 10 番目の位置にアイテムをコピーする copyItem メソッドの呼び出しを示しています。 FormListControl.getCount メソッドは、コントロール内の項目の数を返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
   } 
    formListControl.getCount(); 
    formListControl.copyItem(2,10); 
}
```

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

フォーム リスト コントロールから指定した項目を削除します。

```xpp
public boolean delete(int Idx)
```

### <a name="parameters---delete"></a>パラメーター - delete

Idx  
削除される項目の 0 から始まるインデックス。

### <a name="return-value---delete"></a>戻り値 - delete

項目が削除された場合は true。それ以外の場合は false。

### <a name="examples---delete"></a>例 - delete

次の例は、フォーム リスト コントロールから項目を削除する delete メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    boolean itemDel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    // Delete an item. 
    itemDel = formListControl.delete(2); 
}
```

## <a name="method-deleteall"></a>メソッド deleteAll

フォーム リスト コントロールからすべての項目を削除します。

```xpp
public boolean deleteAll()
```

### <a name="return-value---deleteall"></a>戻り値 - deleteAll

すべての項目が削除された場合は true。それ以外の場合は、false。

### <a name="examples---deleteall"></a>例 - deleteAll

次の例は、フォーム リスト コントロールからすべての項目を削除する deleteAll メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    boolean itemsDel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    // Delete all items. 
    itemsDel = formListControl.deleteAll(); 
}
```

## <a name="method-deletecolumn"></a>メソッド deleteColumn

フォーム リスト コントロールの指定した列を削除します。

```xpp
public boolean deleteColumn(int Idx)
```

### <a name="parameters---deletecolumn"></a>パラメーター - deleteColumn

Idx  
フォーム リスト コントロール内で列を指定する整数データ型です。

### <a name="return-value---deletecolumn"></a>戻り値 - deleteColumn

列が削除された場合は true。それ以外の場合は false。

### <a name="examples---deletecolumn"></a>例 - deleteColumn

次の例は、フォーム リスト コントロールから第 1 列を削除する deleteColumn メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、2 列をフォーム リスト コントロールに追加します。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    boolean columnDel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add columns to the form list control. 
    formListControl.addColumn(0, new FormListColumn("Column1",1,120)); 
    formListControl.addColumn(1, new FormListColumn("Column2",2,120)); 
    // Delete a column. 
    columnDel = formListControl.deleteColumn(0); 
}
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
ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。

### <a name="return-value---dragdrop"></a>戻り値 - dragDrop

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="remarks---dragdrop"></a>備考 - dragDrop

dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。

## <a name="method-dragover"></a>メソッド dragOver

ユーザーがフォーム リスト コントロールの境界内のアイテムにオブジェクトをドラッグするときを識別します。

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a>パラメーター - dragOver

dragSource  
オブジェクトの位置の y 座標を示す整数データ型です。

<!-- -->

dragMode  
オブジェクトの位置の y 座標を示す整数データ型です。

<!-- -->

x  
オブジェクトの位置の y 座標を示す整数データ型です。

<!-- -->

y  
オブジェクトの位置の y 座標を示す整数データ型です。

### <a name="return-value---dragover"></a>戻り値 - dragOver

オブジェクトが移動、コピー、または指定された位置に移動されていないかどうかを示す FormDrag システム列挙値。

### <a name="remarks---dragover"></a>備考 - dragOver

このメソッドは、DragDrop プロパティがコントロールの手動に設定されていて、beginDrag イベントがすでに開始されている場合にのみ呼び出されます。 イベントの詳細については、beginDrag を参照してください。 リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [dragOver] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

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

フォーム リスト コントロールでユーザーが項目をドラッグしたときに表示されるテキストを取得します。

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a>戻り値 - dragText

ユーザーがフォーム リスト コントロールをドラッグするときに表示されるテキストを指定する文字列データ型値。

### <a name="remarks---dragtext"></a>備考 - dragText

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [dragText] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-editlabels"></a>メソッド editLabels

ユーザーがフォーム リスト コントロールで項目名を変更できるかどうかを示します。

```xpp
public boolean editLabels([boolean value])
```

### <a name="parameters---editlabels"></a>パラメーター - editLabels

値  
ユーザーがフォーム リスト コントロール内の項目名を変更できるかどうかを指定するブール値データ型。

### <a name="return-value---editlabels"></a>戻り値 - editLabels

ユーザーが項目名を変更することができる場合は true。それ以外の場合は、false。

### <a name="remarks---editlabels"></a>備考 - editLabels

フォーム リスト コントロールに列を追加する前に、editLabels メソッドを呼び出す必要があります。それ以外の場合、列はコントロールに表示されません。

### <a name="examples---editlabels"></a>例 - editLabels

次の例は、ユーザーがフォーム リスト コントロール内の項目名を変更できるようにする editLabels メソッドの呼び出しを示しています。 DictField.label メソッドは、フォーム リスト コントロールへの品目として追加される指定のテーブル フィールドのラベルを返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    DictField dictField; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.editLabels(true); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        dictField = new DictField(77,1); 
        formListItem = new FormListItem(dictField.label()); 
        item = formListControl.addItem(formListItem); 
    } 
}
```

## <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  
コントロールが有効かどうかを指定するブール値; オプション。

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

## <a name="method-ensurevisible"></a>メソッド ensureVisible

```xpp
public int ensureVisible(int Idx)
```

### <a name="parameters---ensurevisible"></a>パラメーター - ensureVisible

Idx  

### <a name="return-value---ensurevisible"></a>戻り値 - ensureVisible

## <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

```xpp
public str font([str value])
```

### <a name="parameters---font"></a>パラメーター - font

値  

### <a name="return-value---font"></a>戻り値 - font

Tahoma や Verdana など、使用するフォントの名前。

## <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a>パラメーター - fontSize

値  

### <a name="return-value---fontsize"></a>戻り値 - fontSize

ポイント単位のフォントの高さ。

## <a name="method-foregroundcolor"></a>メソッド foregroundColor

コントロールのテキストの色を取得または設定します。

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a>パラメーター - foregroundColor

値  
前景色を指定する整数データ型です。

### <a name="return-value---foregroundcolor"></a>戻り値 - foregroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---foregroundcolor"></a>備考 - foregroundColor

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="examples---foregroundcolor"></a>例 - foregroundColor

次の例は、前景色をデスクトップ上のメニュー テキストの色に設定する foregroundColor メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.foregroundColor(WindowsPalette::MenuText); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
}
```

## <a name="method-getcolumn"></a>メソッド getColumn

フォーム リスト コントロール内の指定された列の FormListColumn オブジェクトを取得します。

```xpp
public FormListColumn getColumn(int Idx)
```

### <a name="parameters---getcolumn"></a>パラメーター - getColumn

Idx  
フォーム リスト コントロール内で列を指定する整数データ型です。

### <a name="return-value---getcolumn"></a>戻り値 - getColumn

フォーム リスト コントロール内の指定された列の FormListColumn オブジェクト。

### <a name="remarks---getcolumn"></a>備考 - getColumn

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

### <a name="examples---getcolumn"></a>例 - getColumn

次の例は、フォーム リスト コントロール内の列の FormListColumn オブジェクトを返す getColumn メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。


```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    str columnName; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control, 
    // and then set the column width. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    formListColumn = formListControl.getColumn(0); 
    columnName = formListColumn.toString(); 
}
```

## <a name="method-getcolumncount"></a>メソッド getColumnCount

フォーム リスト コントロール内の列の数を取得します。

```xpp
public int getColumnCount()
```

### <a name="return-value---getcolumncount"></a>戻り値 - getColumnCount

フォーム リスト コントロールの列数を指定する整数データ型値です。

### <a name="remarks---getcolumncount"></a>備考 - getColumnCount

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

### <a name="examples---getcolumncount"></a>例 - getColumnCount

次の例は、フォーム リスト コントロールの列数を返す getColumnCount メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。


```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    int columnCnt; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    columnCnt = formListControl.getColumnCount(); 
}
```

## <a name="method-getcolumnwidth"></a>メソッド getColumnWidth

フォーム リスト コントロール内の列の幅を取得します。

```xpp
public int getColumnWidth(int Idx)
```

### <a name="parameters---getcolumnwidth"></a>パラメーター - getColumnWidth

Idx  
フォーム リスト コントロール内で列を指定する整数データ型です。

### <a name="return-value---getcolumnwidth"></a>戻り値 - getColumnWidth

フォーム リスト コントロール内で列幅を指定する整数データ型です。

### <a name="remarks---getcolumnwidth"></a>備考 - getColumnWidth

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

### <a name="examples---getcolumnwidth"></a>例 - getColumnWidth

次の例は、フォーム リスト コントロール内の列の幅を返す getColumnWidth メソッドの呼び出しを示しています。 FormListControl.setColumnWidth メソッドは、列の幅を指定します。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    int width; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control, 
    // and then set the column width. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    formListControl.setColumnWidth(0,100); 
    width = formListControl.getColumnWidth(0); 
}
```

## <a name="method-getcount"></a>メソッド getCount

フォーム リスト コントロールに含まれる項目の数を取得します。

```xpp
public int getCount()
```

### <a name="return-value---getcount"></a>戻り値 - getCount

フォーム リスト コントロールに含まれている品目数を指定する整数データ型値です。

### <a name="examples---getcount"></a>例 - getCount

次の例は、getCount メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    numItems = formListControl.getCount(); 
}
```

## <a name="method-getcountperpage"></a>メソッド getCountPerPage

```xpp
public int getCountPerPage()
```

### <a name="return-value---getcountperpage"></a>戻り値 - getCountPerPage

## <a name="method-getimagelist"></a>メソッド getImagelist

```xpp
public Imagelist getImagelist([boolean GetLarge])
```

### <a name="parameters---getimagelist"></a>パラメーター - getImagelist

GetLarge  

### <a name="return-value---getimagelist"></a>戻り値 - getImagelist

## <a name="method-getitem"></a>メソッド getItem

フォーム リスト コントロール内の項目の FormListItem オブジェクトを取得します。

```xpp
public FormListItem getItem(int Idx, [int SubItem])
```

### <a name="parameters---getitem"></a>パラメーター - getItem

Idx  
フォーム リスト コントロール内でサブ項目を指定する整数データ型です。

<!-- -->

SubItem  
フォーム リスト コントロール内でサブ項目を指定する整数データ型です。

### <a name="return-value---getitem"></a>戻り値 - getItem

フォーム リスト コントロール内の項目の FormListItem オブジェクト。

### <a name="examples---getitem"></a>例 - getItem

次の例は、フォーム リスト コントロール内の各項目の列の FormListItem オブジェクトを返す getItem メソッドの呼び出しを示しています。 FormListItem.toString メソッドは、各項目のテキスト文字列を返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    boolean columnadd; 
    str string; 
    str itemTxt; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add an item to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        formListItem = formListControl.getItem(item); 
        itemTxt = formListItem.toString(); 
    } 
}
```

## <a name="method-getitempos"></a>メソッド getItemPos

フォーム リスト コントロール内の項目の位置を取得します。

```xpp
public container getItemPos(int Item)
```

### <a name="parameters---getitempos"></a>パラメーター - getItemPos

項目  
フォーム リスト コントロール内の項目を指定する整数データ型です。

### <a name="return-value---getitempos"></a>戻り値 - getItemPos

フォーム リスト コントロールの項目の位置を含むコンテナー データ型。 項目の位置は、x 座標と y 座標によって指定されます。

### <a name="remarks---getitempos"></a>備考 - getItemPos

コンテナから項目を抽出するには conPeek 関数を使用します。

### <a name="examples---getitempos"></a>例 - getItemPos

次の例は、フォーム リスト コントロール内の各項目の位置を返す getItemPos メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    boolean columnadd; 
    str string; 
    container conAccountNum; 
    container itemPos; 
    CustTable custTable; 
    int numAccounts; 
    int numItems; 
    int i; 
    int x; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add an item to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        itemPos = formListControl.getItemPos(item); 
        numItems = conlen(itemPos); 
        for(x = 1; x<= numItems; x++) 
        { 
            print conpeek(itemPos,x); 
            pause; 
        } 
    } 
}
```

## <a name="method-getnextitem"></a>メソッド getNextItem

フォーム リスト コントロール内の次の項目の数を取得します。

```xpp
public int getNextItem(FormListNext nextType, [int startIdx])
```

### <a name="parameters---getnextitem"></a>パラメーター - getNextItem

nextType  
次の項目の前にある項目を指定する整数データ型です。

<!-- -->

startIdx  
次の項目の前にある項目を指定する整数データ型です。

### <a name="return-value---getnextitem"></a>戻り値 - getNextItem

フォーム リスト コントロールでどの項目が次の品目であるかを示す整数データ型値です。

### <a name="examples---getnextitem"></a>例 - getNextItem

次の例は、フォーム リスト コントロールの次の項目数を取得する getNextItem メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の品目は、フォーム リスト コントロールの一覧の管理に追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    boolean columnadd; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(77); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = new FormRun(Args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add an item to the form list control. 
    while select custTable 
       where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        formListControl.addItem(formListItem); 
    } 
    item = formListControl.getNextItem(FormListNext::ToRight); 
}
```

## <a name="method-getselectedcount"></a>メソッド getSelectedCount

フォーム リスト コントロールで選択されている項目の数を取得します。

```xpp
public int getSelectedCount()
```

### <a name="return-value---getselectedcount"></a>戻り値 - getSelectedCount

フォーム リスト コントロールで選択されている品目の数を示す整数データ型値です。

### <a name="examples---getselectedcount"></a>例 - getSelectedCount

次の例は、フォーム リスト コントロールの選択した項目数を返す getSelectedCount メソッドの呼び出しを示しています。 FormListControl.singleSelection メソッドは、複数の項目を選択するかどうかを示します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    int numItemsSel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.singleSelection(false); 
    // Add columns to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    numItemsSel = formListControl.getSelectedCount(); 
}
```

## <a name="method-getstringwidth"></a>メソッド getStringWidth

```xpp
public int getStringWidth(str Text)
```

### <a name="parameters---getstringwidth"></a>パラメーター - getStringWidth

テキスト  

### <a name="return-value---getstringwidth"></a>戻り値 - getStringWidth

## <a name="method-gettopindex"></a>メソッド getTopIndex

```xpp
public int getTopIndex()
```

### <a name="return-value---gettopindex"></a>戻り値 - getTopIndex

## <a name="method-gridlines"></a>メソッド gridLines

```xpp
public boolean gridLines([boolean value])
```

### <a name="parameters---gridlines"></a>パラメーター - gridLines

値  

### <a name="return-value---gridlines"></a>戻り値 - gridLines

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

## <a name="method-headerdragdrop"></a>メソッド headerdragdrop

```xpp
public boolean headerdragdrop([boolean value])
```

### <a name="parameters---headerdragdrop"></a>パラメーター - headerdragdrop

値  

### <a name="return-value---headerdragdrop"></a>戻り値 - headerdragdrop

## <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a>パラメーター - height

値  
高さの計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

<!-- -->

モード  
高さの計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

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

### <a name="examples---height"></a>例 - height

次の例は、コントロールの高さを 120 ピクセルに設定する height メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.height(120,-1); 
}
```

## <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a>パラメーター - heightMode

値  
コントロールの高さの計算方法を示す整数。オプション。 この値は、 Exact モードの場合は -1、Auto モードの場合は 0、Column height 幅の場合は 1 になります。

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

次の例は、正確なピクセル値に基づいてコントロールの高さを調整する heightMode メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.heightMode(-1); 
    formListControl.heightValue(120); 
}
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

次の例は、高さを 120 ピクセルに設定する heightValue メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.heightMode(-1); 
    formListControl.heightValue(120); 
}
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

## <a name="method-hittestsubitem"></a>メソッド hitTestSubItem

```xpp
public container hitTestSubItem(int x, int y)
```

### <a name="parameters---hittestsubitem"></a>パラメーター - hitTestSubItem

x  

<!-- -->

y  

### <a name="return-value---hittestsubitem"></a>戻り値 - hitTestSubItem

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
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙値。

### <a name="return-value---isusersetupenabled"></a>戻り値 - isUserSetupEnabled

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

### <a name="remarks---isusersetupenabled"></a>備考 - isUserSetupEnabled

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。 次のテーブルでは、neededSetupRights パラメーターの値について説明します。

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

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a>パラメーター - italic

値  

### <a name="return-value---italic"></a>戻り値 - italic

## <a name="method-itemalign"></a>メソッド itemAlign

```xpp
public int itemAlign([int value])
```

### <a name="parameters---itemalign"></a>パラメーター - itemAlign

値  

### <a name="return-value---itemalign"></a>戻り値 - itemAlign

## <a name="method-itemchanging"></a>メソッド itemChanging

```xpp
public boolean itemChanging(int Idx, AnyType Data)
```

### <a name="parameters---itemchanging"></a>パラメーター - itemChanging

Idx  

<!-- -->

データ  

### <a name="return-value---itemchanging"></a>戻り値 - itemChanging

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

ユーザーがフォーム リスト コントロールからフォーカスを移動したら識別します。

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a>戻り値 - leave

フォーカスがコントロールから移動された場合は true。それ以外の場合は、false。

### <a name="remarks---leave"></a>備考 - leave

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[leave] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-left"></a>メソッド left

フォーム リスト コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a>パラメーター - left

値  
位置の計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

<!-- -->

モード  
位置の計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

### <a name="return-value---left"></a>戻り値 - left

フォーム リスト コントロールの水平位置をピクセル単位で示す整数。

### <a name="examples---left"></a>例 - left

次の例は、水平方向の位置を 50 ピクセルに設定する left メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.left(50,-1); 
}
```

## <a name="method-leftmode"></a>メソッド leftMode

フォーム リスト コントロールの水平位置を計算する方法を示す値を設定するか返します。

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a>パラメーター - leftMode

値  
水平位置の計算方法を示す整数。オプション。

### <a name="return-value---leftmode"></a>戻り値 - leftMode

水平位置の計算方法を示す整数。 戻り値は、-1 または FormLeft 列挙値です。

### <a name="remarks---leftmode"></a>備考 - leftMode

value パラメーターと戻り値は、水平位置の計算方法を指定する整数値です。 この値は、正確なピクセル値の場合は -1、FormLeft 列挙値の場合は -1 のいずれかになります。 詳細については、「FormLeft 列挙」を参照してください。

### <a name="examples---leftmode"></a>例 - leftMode

次の例は、正確なピクセル値に基づいて、フォーム リスト コントロールの水平方向位置を計算する leftMode メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form.  
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.leftMode(-1); 
    formListControl.leftValue(100); 
}
```

## <a name="method-leftvalue"></a>メソッド leftValue

フォーム リスト コントロールの水平位置をピクセル単位で設定するか返します。

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a>パラメーター - leftValue

値  
水平位置をピクセル単位で示す整数。オプション。

### <a name="return-value---leftvalue"></a>戻り値 - leftValue

水平位置をピクセル単位で示す整数。

### <a name="remarks---leftvalue"></a>備考 - leftValue

正確なピクセル値に左モードが設定されていない限り、水平位置は変更されません。 詳細については、「leftMode」を参照してください。

### <a name="examples---leftvalue"></a>例 - leftValue

次の例は、水平方向の位置を 100 ピクセルに設定する leftValue メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.leftMode(-1); 
    formListControl.leftValue(100); 
}
```

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

ユーザーがマウスの左ボタンが押すときを識別します。

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

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[mouseUp] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-moveitem"></a>メソッド moveItem

指定した項目をフォーム リスト コントロールに移動します。

```xpp
public int moveItem(int Item, int InsertAt)
```

### <a name="parameters---moveitem"></a>パラメーター - moveItem

項目  
品目が移動されるリスト内の位置を指定する整数データ型です。

<!-- -->

InsertAt  
品目が移動されるリスト内の位置を指定する整数データ型です。

### <a name="return-value---moveitem"></a>戻り値 - moveItem

品目が移動されるリスト内の位置を指定する整数データ型です。

### <a name="examples---moveitem"></a>例 - moveItem

次の例は、フォーム リスト コントロールの 10 番目の位置にアイテムを移動する moveItem メソッドの呼び出しを示しています。 FormListControl.getCount メソッドは、コントロール内の項目の数を返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(77); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = new FormRun(Args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add columns to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Account Numbers",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    formListControl.getCount(); 
    formListControl.moveItem(2,10); 
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

## <a name="method-oneclickactivate"></a>メソッド oneClickActivate

```xpp
public boolean oneClickActivate([boolean value])
```

### <a name="parameters---oneclickactivate"></a>パラメーター - oneClickActivate

値  

### <a name="return-value---oneclickactivate"></a>戻り値 - oneClickActivate

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

## <a name="method-redrawitems"></a>メソッド redrawItems

フォーム リスト コントロール内の広範囲の項目を更新します。

```xpp
public boolean redrawItems(int idxFirst, int idxLast)
```

### <a name="parameters---redrawitems"></a>パラメーター - redrawItems

idxFirst  
範囲内の最後の項目のゼロベースのインデックスを指定する整数データ型です。

<!-- -->

idxLast  
範囲内の最後の項目のゼロベースのインデックスを指定する整数データ型です。

### <a name="return-value---redrawitems"></a>戻り値 - redrawItems

項目が更新された場合は true。それ以外の場合は、false。

### <a name="examples---redrawitems"></a>例 - redrawItems

次の例は、フォーム リスト コントロール内の項目の範囲を更新する redrawItems メソッドの呼び出しを示しています。 FormListControl.moveItem メソッドは、指定された項目を移動します。 FormListControl.getCount メソッドは、コントロール内の項目の数を取得します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(77); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = new FormRun(Args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add columns to form list control. 
    formListControl.addColumn(1, new FormListColumn("Account Numbers",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= "4000" 
            && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    formListControl.getCount(); 
    formListControl.moveItem(2,10); 
    formListControl.redrawItems(0,20); 
}
```

## <a name="method-rowselect"></a>メソッド rowSelect

行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型値を設定または取得します。

```xpp
public boolean rowSelect([boolean value])
```

### <a name="parameters---rowselect"></a>パラメーター - rowSelect

値  
行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型。

### <a name="return-value---rowselect"></a>戻り値 - rowSelect

フォーム リスト コントロール内の行が選択されている場合は true。それ以外の場合は、false。

### <a name="examples---rowselect"></a>例 - rowSelect

次の例は、行がクリックされたときにフォーム リスト コントロール内の行が選択されるように指定する、rowSelect メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。 列は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn1; 
    FormListColumn formListColumn2; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.rowSelect(true); 
    // Add columns to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1",1,120)); 
    formListControl.addColumn(2, new FormListColumn("Column2",2,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    }}
```

## <a name="method-scroll"></a>メソッド scroll

```xpp
public boolean scroll(int dx, int dy)
```

### <a name="parameters---scroll"></a>パラメーター - scroll

dx  

<!-- -->

dy  

### <a name="return-value---scroll"></a>戻り値 - scroll

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

## <a name="method-selectionchanging"></a>メソッド selectionChanging

```xpp
public boolean selectionChanging(int Idx, AnyType Data)
```

### <a name="parameters---selectionchanging"></a>パラメーター - selectionChanging

Idx  

<!-- -->

データ  

### <a name="return-value---selectionchanging"></a>戻り値 - selectionChanging

## <a name="method-setcolumn"></a>メソッド setColumn

```xpp
public boolean setColumn(int Idx, FormListColumn Column)
```

### <a name="parameters---setcolumn"></a>パラメーター - setColumn

Idx  

<!-- -->

円柱  

### <a name="return-value---setcolumn"></a>戻り値 - setColumn

## <a name="method-setcolumnwidth"></a>メソッド setColumnWidth

フォーム リスト コントロール内の列の幅を指定します。

```xpp
public boolean setColumnWidth(int Idx, int Width)
```

### <a name="parameters---setcolumnwidth"></a>パラメーター - setColumnWidth

Idx  
フォーム リスト コントロール内で列の幅を指定する整数データ型です。

<!-- -->

幅  
フォーム リスト コントロール内で列の幅を指定する整数データ型です。

### <a name="return-value---setcolumnwidth"></a>戻り値 - setColumnWidth

幅がセットされている場合は true。それ以外の場合は、false。

### <a name="remarks---setcolumnwidth"></a>備考 - setColumnWidth

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

### <a name="examples---setcolumnwidth"></a>例 - setColumnWidth

次の例は、フォーム リスト コントロール内の列の幅を指定する setColumnWidth メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control, and then set the column width. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    formListControl.setColumnWidth(0,100); 
}
```

## <a name="method-setitem"></a>メソッド setItem

フォーム リスト コントロールに項目が含まれているかどうかを示します。

```xpp
public boolean setItem(FormListItem item)
```

### <a name="parameters---setitem"></a>パラメーター - setItem

品目  
フォーム リスト コントロール内の項目の FormListItem オブジェクト。

### <a name="return-value---setitem"></a>戻り値 - setItem

フォーム リスト コントロールに項目が含まれている場合は true。それ以外の場合は、false。

### <a name="examples---setitem"></a>例 - setItem

次の例は、各項目がフォーム リスト コントロールに含まれているかどうかを判断する setItem メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    boolean itemSet; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        itemSet = formListControl.setItem(formListItem); 
    } 
}
```

## <a name="method-setstateimagelist"></a>メソッド setStateImagelist

```xpp
public Imagelist setStateImagelist(Imagelist imageList)
```

### <a name="parameters---setstateimagelist"></a>パラメーター - setStateImagelist

imageList  

### <a name="return-value---setstateimagelist"></a>戻り値 - setStateImagelist

## <a name="method-showcontextmenu"></a>メソッド showContextMenu

ショートカット メニューがいつ表示されるかを示します。

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a>パラメーター - showContextMenu

menuHandle  
メニュー ハンドルを指定する整数データ型です。

### <a name="return-value---showcontextmenu"></a>戻り値 - showContextMenu

メニュー ハンドルを指定する整数データ型です。

### <a name="remarks---showcontextmenu"></a>備考 - showContextMenu

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [showContextMenu] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-showselalways"></a>メソッド showSelAlways

```xpp
public boolean showSelAlways([boolean value])
```

### <a name="parameters---showselalways"></a>パラメーター - showSelAlways

値  

### <a name="return-value---showselalways"></a>戻り値 - showSelAlways

## <a name="method-singleselection"></a>メソッド singleSelection

フォーム リスト コントロールで複数の項目を選択できるかどうかを示します。

```xpp
public boolean singleSelection([boolean value])
```

### <a name="parameters---singleselection"></a>パラメーター - singleSelection

値  
フォーム リスト コントロールで複数の項目を選択できるかどうかを示すブール値データ型。

### <a name="return-value---singleselection"></a>戻り値 - singleSelection

複数の項目を選択することができない場合 true。それ以外の場合は、false。

### <a name="remarks---singleselection"></a>備考 - singleSelection

フォームのリスト コントロールにアイテムを追加する前に、singleSelection メソッドを呼び出します。 それ以外の場合は、項目はコントロールに表示されません。

### <a name="examples---singleselection"></a>例 - singleSelection

次の例は、複数の項目を選択できるように指定するための singleSelection メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void testFormListControl(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn1; 
    FormListColumn formListColumn2; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    boolean columnAdd; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::List); 
    formListControl.height(120); 
    formListControl.singleSelection(false); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
}
```

## <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  
コントロールのスキップ プロパティに割り当てるブール値; オプション。

### <a name="return-value---skip"></a>戻り値 - skip

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

## <a name="method-sort"></a>メソッド sort

```xpp
public int sort([int value])
```

### <a name="parameters---sort"></a>パラメーター - sort

値  

### <a name="return-value---sort"></a>戻り値 - sort

## <a name="method-sorttextitems"></a>メソッド sortTextItems

```xpp
public boolean sortTextItems([int column], [boolean ascending])
```

### <a name="parameters---sorttextitems"></a>パラメーター - sortTextItems

column  

<!-- -->

ascending  

### <a name="return-value---sorttextitems"></a>戻り値 - sortTextItems

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

フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a>パラメーター - top

値  
垂直位置の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

<!-- -->

モード  
垂直位置の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

### <a name="return-value---top"></a>戻り値 - top

フォーム リスト コントロールの垂直位置をピクセル単位で示す整数。

### <a name="examples---top"></a>例 - top

次の例は、垂直位置を 50 ピクセルに設定する top メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.top(50,-1); 
}
```

## <a name="method-topmode"></a>メソッド topMode

フォーム リスト コントロールの垂直位置を計算する方法を示す値を設定するか返します。

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a>パラメーター - topMode

値  
垂直位置の計算方法を示す整数。オプション。

### <a name="return-value---topmode"></a>戻り値 - topMode

垂直位置の計算方法を示す整数データ型値です。 戻り値は、-1 または FormTop 列挙値です。

### <a name="remarks---topmode"></a>備考 - topMode

value パラメーターと戻り値は、正確なピクセル値の場合は -1、FormTop 列挙値または -1 のいずれかの整数値です。 詳細については、「FormTop 列挙」を参照してください。

### <a name="examples---topmode"></a>例 - topMode

次の例は、正確なピクセル値に基づいて垂直位置を計算する topMode メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.topMode(-1); 
    formListControl.topValue(50); 
}
```

## <a name="method-topvalue"></a>メソッド topValue

フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返します。

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a>パラメーター - topValue

値  
垂直位置を指定する整数。オプション。

### <a name="return-value---topvalue"></a>戻り値 - topValue

フォーム リスト コントロールの垂直位置を指定する整数。

### <a name="remarks---topvalue"></a>備考 - topValue

正確なピクセル値に上部モードが設定されていない限り、垂直位置は変更されません。 詳細については、「topMode」を参照してください。

### <a name="examples---topvalue"></a>例 - topValue

次の例は、垂直位置を 50 ピクセルに設定する topValue メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.topMode(-1); 
    formListControl.topValue(50); 
}
```

## <a name="method-trackselect"></a>メソッド trackSelect

```xpp
public boolean trackSelect([boolean value])
```

### <a name="parameters---trackselect"></a>パラメーター - trackSelect

値  

### <a name="return-value---trackselect"></a>戻り値 - trackSelect

## <a name="method-twoclickactivate"></a>メソッド twoClickActivate

```xpp
public boolean twoClickActivate([boolean value])
```

### <a name="parameters---twoclickactivate"></a>パラメーター - twoClickActivate

値  

### <a name="return-value---twoclickactivate"></a>戻り値 - twoClickActivate

## <a name="method-type"></a>メソッドのタイプ

```xpp
public int type([int value])
```

### <a name="parameters---type"></a>パラメーター - type

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティの値を設定するか返します。

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a>パラメーター - underline

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

### <a name="return-value---underline"></a>戻り値 - underline

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

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
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合は 0 です。

### <a name="return-value---userskip"></a>戻り値 - userSkip

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

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

## <a name="method-verticalspacing"></a>メソッド verticalSpacing

ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定または取得し、スペースを計算する方法を指定します。

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a>パラメーター - verticalSpacing

値  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

<!-- -->

モード  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

### <a name="return-value---verticalspacing"></a>戻り値 - verticalSpacing

コントロールの上と下のスペースの量を示す整数。

## <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォーム リスト コントロールの上と下のスペースを計算する方法を示す値を設定するか返します。

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a>パラメーター - verticalSpacingMode

モード  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

### <a name="return-value---verticalspacingmode"></a>戻り値 - verticalSpacingMode

スペースがフォント サイズなどの他のフォーム設定に基づいて自動的に調整される場合は自動です。そうでなければ、固定です。

## <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定するか返します。

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a>パラメーター - verticalSpacingValue

値  
コントロールの上と下のスペースの量を示す整数。オプション。

### <a name="return-value---verticalspacingvalue"></a>戻り値 - verticalSpacingValue

コントロールの上と下のスペースの量を示す整数。

## <a name="method-viewtype"></a>メソッド viewType

```xpp
public int viewType([int value])
```

### <a name="parameters---viewtype"></a>パラメーター - viewType

値  

### <a name="return-value---viewtype"></a>戻り値 - viewType

## <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  
コントロールの表示設定に割り当てられる値 (オプション)。

### <a name="return-value---visible"></a>戻り値 - visible

コントロールが可視である場合は true。それ以外の場合は false。

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  
幅の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

<!-- -->

モード  
幅の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

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

### <a name="examples---width"></a>例 - width

次の例は、コントロールの幅を 120 ピクセルに設定する width メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.width(120,-1); 
}
```

## <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a>パラメーター - widthMode

値  
コントロールの幅の計算方法を示す整数。オプション。

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

次の例は、正確なピクセル値に基づいて、コントロールの幅を計算する widthMode メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.widthMode(-1); 
    formListControl.widthValue(120); 
}
```

## <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  
コントロールの幅をピクセル単位で指定する整数。オプション。

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="examples---widthvalue"></a>例 - widthValue

次の例は、コントロールの幅を 120 ピクセルに設定する widthValue メソッドの呼び出しを示しています。

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.widthMode(-1); 
    formListControl.widthValue(120); 
}
```

## <a name="method-selectionchanged"></a>メソッド selectionChanged

```xpp
public void selectionChanged(int Idx, AnyType Data)
```

### <a name="parameters---selectionchanged"></a>パラメーター - selectionChanged

Idx  

<!-- -->

データ  

## <a name="method-activateitem"></a>メソッド activateItem

```xpp
public void activateItem(int Idx)
```

### <a name="parameters---activateitem"></a>パラメーター - activateItem

Idx  

## <a name="method-inputsearch"></a>メソッド inputSearch

指定されたテキスト文字列の検索開始日を示します。

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a>パラメーター - inputSearch

searchStr  
テキスト文字列を指定する文字列データ型。

### <a name="remarks---inputsearch"></a>備考 - inputSearch

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[inputSearch] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

```xpp
public void displayControl()
```

## <a name="method-onleaving"></a>メソッド OnLeaving

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a>パラメーター - OnLeaving

sender  

<!-- -->

e  

## <a name="method-update"></a>メソッド update

コントロールを更新します。

```xpp
public void update([int idx])
```

### <a name="parameters---update"></a>パラメーター - update

idx  

## <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム リスト コントロールの移動を終了した日を示します。

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a>備考 - endDrag

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[endDrag] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

```xpp
public void mouseLeave()
```

## <a name="method-setimagelist"></a>メソッド setImagelist

```xpp
public void setImagelist(Imagelist imageList, [boolean SetLarge])
```

### <a name="parameters---setimagelist"></a>パラメーター - setImagelist

imageList  

<!-- -->

SetLarge  

## <a name="method-copy"></a>メソッド copy

ユーザーがコピー操作を実行するときを識別します。

```xpp
public void copy()
```

### <a name="remarks---copy"></a>備考 - copy

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [copy] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

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

## <a name="method-itemcopy"></a>メソッド itemCopy

```xpp
public void itemCopy(int Idx, int newIdx)
```

### <a name="parameters---itemcopy"></a>パラメーター - itemCopy

Idx  

<!-- -->

newIdx  

## <a name="method-cut"></a>メソッド cut

ユーザーがカット操作を実行するときを識別します。

```xpp
public void cut()
```

### <a name="remarks---cut"></a>備考 - cut

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [cut] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-itemmoved"></a>メソッド itemMoved

```xpp
public void itemMoved(int Idx, int newIdx)
```

### <a name="parameters---itemmoved"></a>パラメーター - itemMoved

Idx  

<!-- -->

newIdx  

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

## <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

```xpp
public void paste()
```

## <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

```xpp
public void lostFocus()
```

## <a name="method-onselectionchanged"></a>メソッド OnSelectionChanged

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a>パラメーター - OnSelectionChanged

sender  

<!-- -->

e  

## <a name="method-hottrackitem"></a>メソッド hotTrackItem

ユーザーがマウス ポインターをフォーム リスト コントロール上に移動するときを識別します。

```xpp
public void hotTrackItem(int Idx)
```

### <a name="parameters---hottrackitem"></a>パラメーター - hotTrackItem

Idx  
フォーム リスト コントロールのインデックスを指定する整数データ型です。

### <a name="remarks---hottrackitem"></a>備考 - hotTrackItem

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[hotTrackItem] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-setcount"></a>メソッド setCount

```xpp
public void setCount(int count)
```

### <a name="parameters---setcount"></a>パラメーター - setCount

カウント  

## <a name="method-dragleave"></a>メソッド dragLeave

ユーザーがフォーム リスト コントロールの境界からオブジェクトをドラッグするときを識別します。

```xpp
public void dragLeave()
```

### <a name="remarks---dragleave"></a>備考 - dragLeave

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[dragLeave] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-itemdeleted"></a>メソッド itemDeleted

```xpp
public void itemDeleted(int Idx, AnyType Data)
```

### <a name="parameters---itemdeleted"></a>パラメーター - itemDeleted

Idx  

<!-- -->

データ  

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

## <a name="method-ongotfocus"></a>メソッド OnGotFocus

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a>パラメーター - OnGotFocus

sender  

<!-- -->

e  

## <a name="method-settext"></a>メソッド setText

```xpp
public void setText(int Idx, str Text, [int SubItem])
```

### <a name="parameters---settext"></a>パラメーター - setText

Idx  

<!-- -->

テキスト  

<!-- -->

SubItem  

## <a name="method-itemchanged"></a>メソッド itemChanged

```xpp
public void itemChanged(int Idx, AnyType Data)
```

### <a name="parameters---itemchanged"></a>パラメーター - itemChanged

Idx  

<!-- -->

データ  

## <a name="method-doubleclick"></a>メソッド doubleClick

ユーザーがフォーム内のリスト コントロールのアイテムをダブルクリックするときを識別します。

```xpp
public void doubleClick()
```

### <a name="remarks---doubleclick"></a>備考 - doubleClick

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [doubleClick] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

```xpp
public void resetUserSetting()
```

## <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

```xpp
public void setFocus()
```

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

## <a name="method-allitemsdeleted"></a>メソッド allItemsDeleted

フォーム リスト コントロール内のすべてのアイテムが削除される日を示します。

```xpp
public void allItemsDeleted()
```

### <a name="remarks---allitemsdeleted"></a>備考 - allItemsDeleted

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[allItemsDeleted] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-drop"></a>メソッド drop

ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムを新しい位置にドロップするときを識別します。

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a>パラメーター - drop

dragSource  
オブジェクトの位置の y 座標を示す整数データ型です。

<!-- -->

dragMode  
オブジェクトの位置の y 座標を示す整数データ型です。

<!-- -->

x  
オブジェクトの位置の y 座標を示す整数データ型です。

<!-- -->

y  
オブジェクトの位置の y 座標を示す整数データ型です。

### <a name="remarks---drop"></a>備考 - drop

このメソッドは、DragDrop プロパティがコントロールの手動に設定されていて、beginDrag イベントがすでに開始されている場合にのみ呼び出されます。 イベントの詳細については、beginDrag を参照してください。 リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [drop] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-columnclicked"></a>メソッド columnClicked

ユーザーがフォーム内のリスト ビュー コントロールの列をクリックするときを識別します。

```xpp
public void columnClicked(int Column)
```

### <a name="parameters---columnclicked"></a>パラメーター - columnClicked

円柱  
フォーム列を指定する整数データ型です。

### <a name="remarks---columnclicked"></a>備考 - columnClicked

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をクリックして [columnClicked] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-getstateimagelist"></a>メソッド getStateImagelist

```xpp
public void getStateImagelist()
```

## <a name="method-onlostfocus"></a>メソッド OnLostFocus

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a>パラメーター - OnLostFocus

sender  

<!-- -->

e  

## <a name="method-setitempos"></a>メソッド setItemPos

フォーム リスト コントロール内の項目の位置を設定します。

```xpp
public void setItemPos(int Item, int x, int y)
```

### <a name="parameters---setitempos"></a>パラメーター - setItemPos

項目  
項目の位置の y 座標を指定する整数データ型です。

<!-- -->

x  
項目の位置の y 座標を指定する整数データ型です。

<!-- -->

y  
項目の位置の y 座標を指定する整数データ型です。

### <a name="examples---setitempos"></a>例 - setItemPos

次の例は、フォーム リスト コントロール内の各項目の位置を指定する setItemPos メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        formListControl.setItemPos(item,1,5); 
    } 
}
```

## <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

```xpp
public void gotFocus()
```

## <a name="method-enter"></a>メソッド enter

```xpp
public void enter()
```

## <a name="method-onenter"></a>メソッド OnEnter

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a>パラメーター - OnEnter

sender  

<!-- -->

e  

## <a name="method-context"></a>メソッド context

ユーザーがショートカット メニューをフォーム リスト コントロールで開くときを識別します。

```xpp
public void context()
```

### <a name="remarks---context"></a>備考 - context

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [context] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-begineditlabel"></a>メソッド beginEditLabel

```xpp
public void beginEditLabel(int Idx)
```

### <a name="parameters---begineditlabel"></a>パラメーター - beginEditLabel

Idx  

## <a name="method-iteminserted"></a>メソッド itemInserted

```xpp
public void itemInserted(int Idx, AnyType Data)
```

### <a name="parameters---iteminserted"></a>パラメーター - itemInserted

Idx  

<!-- -->

データ  

