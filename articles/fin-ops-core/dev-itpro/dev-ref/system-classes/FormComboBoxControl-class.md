---
title: FormComboBoxControl クラス
description: このトピックでは、FormComboBoxControl クラスについて説明します。
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
ms.openlocfilehash: 6326f4b91792c0232349ed443bf13913db319e1c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502952"
---
# <a name="class-formcomboboxcontrol"></a>クラス FormComboBoxControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormComboBoxControl extends FormControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを他のコントロールと揃える必要があるかどうかを決定します。                                                                                                   |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を修正できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean appendNew(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロール� のバックグラウンドを透明にできるかどうかを決定します。                                                                                                         |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。                                                                                            |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                                              |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public int comboType(\[int value\])                                                                         | コントロールのコンボ ボックスのタイプを設定するか返します。                                                                                                                  |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。                                                                          |
| public int count()                                                                                          | コンボ ボックス コントロール内の項目の数を返します。                                                                                                                   |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 | コンボ ボックス コントロールのデータ フィールドを設定するか返します。                                                                                                               |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。                                                                                              |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                    |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コンボ ボックス コントロールをドラッグしたときに表示されるテキストを返します。                                                                                          |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトが有効か無効かを決定します。                                                                                                                   |
| public EnumId enumType(\[EnumId value\])                                                                    |                                                                                                                                                                         |
| public EnumId enumTypeValue()                                                                               |                                                                                                                                                                         |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                                                         |
| public int find(str string)                                                                                 |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | コントロールに使用するフォントの名前を取得または設定します。                                                                                                  |
| public int fontSize(\[int value\])                                                                          | コントロールに使用するフォントのサイズを取得または設定します。                                                                                                  |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public str getEditText()                                                                                    |                                                                                                                                                                         |
| public str getText(int index)                                                                               |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | フォーム コンボ ボックス コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                 |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | ピクセル単位でコントロールの高さを取得または設定します。                                                                                                                       |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを返します。                                                                                                                                  |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                         |
| public boolean hideFirstEntry(\[boolean value\])                                                            | コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値を設定するか返します。                                                                      |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを返します。                                                                                                                             |
| public boolean isContainer()                                                                                | コントロールがコンテナーかどうかを示す値を返します。                                                                                                      |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を返します。                                                                                                        |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
| public boolean isValid()                                                                                    |                                                                                                                                                                         |
| public boolean italic(\[boolean value\])                                                                    | コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。                                                                                       |
| public int item(\[int value\])                                                                              |                                                                                                                                                                         |
| public int items(\[int value\])                                                                             |                                                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         | コントロールのラベルの太字設定を示す値を設定するか返します。                                                                                   |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         | フォーム コンボ ボックス コントロールのラベル テキストのフォントを設定するか返します。                                                                                                  |
| public int labelFontSize(\[int value\])                                                                     | フォーム コンボ ボックス コントロールのラベル テキストのフォント サイズをポイント単位で設定するか返します。                                                                                 |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               | コントロールのラベルのテキストが斜体で表示されるかどうかを示す値を設定するか返します。                                                                          |
| public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                        | コントロールのラベルがユーザーにダブルクリックされると呼び出されます。                                                                                                 |
| public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                            | ユーザーがコントロールのラベル上でマウス ボタンをクリックすると呼び出されます。                                                                                         |
| public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                              | ユーザーがコントロールのラベル上でマウス ボタンを放すと呼び出されます。                                                                                       |
| public int labelPosition(\[int value\])                                                                     | コントロールのラベルの位置を設定するか返します。                                                                                                              |
| public boolean labelUnderline(\[boolean value\])                                                            | コントロールのラベルのテキストが下線付きで表示されるかどうかを示す値を設定するか返します。                                                                      |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                                                         |
| public boolean leave()                                                                                      |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public boolean modified()                                                                                   |                                                                                                                                                                         |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール上でマウス ボタンを放すと呼び出されます。                                                                                                     |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int selection(\[int value\])                                                                         |                                                                                                                                                                         |
| public int selectionChange()                                                                                | ユーザーがコンボ ボックス コントロールで選択した項目を変更したことを示します。                                                                                         |
| public int selectText(str string)                                                                           |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                 | コントロールのラベルがフォームに表示されるかどうかを示す値を設定するか返します。                                                                      |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public str text(\[str value\])                                                                              | コントロールのテキストを設定するか返します。                                                                                                                               |
| public str toolTip()                                                                                        | コントロールのツールヒント テキストを返します。                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                                                     |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | フォーム コンボ ボックス コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。                                                                    |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コンボ ボックス コントロールがスキップされるかどうかを示す値を設定するか返します。          |
| public int userWidth(\[int value\])                                                                         | ピクセル単位でフォーム コンボ ボックス コントロールの幅を設定するか返します。                                                                                                      |
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void beginUpdate()                                                                                   |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void setEditText(str string)                                                                         |                                                                                                                                                                         |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void paste()                                                                                         | フォーム コンボ ボックス コントロールをフォームに貼り付けます。                                                                                                                        |
| public void clear()                                                                                         | コンボ ボックス リストのエントリをクリアします。                                                                                                                               |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void copy()                                                                                          | フォームのコンボ ボックス コントロールをコピーします。                                                                                                                                      |
| private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])                        |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了すると呼び出されます。                                                                                                 |
| public void lookup()                                                                                        |                                                                                                                                                                         |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void insert(str string, int index)                                                                   | 指定した位置にあるコンボ ボックスに文字列の値を挿入します。                                                                                               |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。                                                                                                       |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void delete(str string)                                                                              | コンボ ボックスのリストから文字列値を削除します。                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void add(str string)                                                                                 | コンボ ボックス リストに文字列値を追加します。                                                                                                                              |
| public void prefColumnSize(int width, int height)                                                           | フォーム コンボ ボックス コントロールの最適な列の幅と高さを指定します。                                                                                         |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |
| public void undo()                                                                                          |                                                                                                                                                                         |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])                         |                                                                                                                                                                         |
| public void endUpdate()                                                                                     |                                                                                                                                                                         |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void setDropSize(\[int lines\])                                                                      |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを他のコントロールと揃える必要があるかどうかを決定します。

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a>パラメーター - alignControl

値  
フォーム コンボ ボックス コントロールが他のコントロールと一致しているかどうかを示すブール値; オプション。

### <a name="return-value---aligncontrol"></a>戻り値 - alignControl

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

### <a name="remarks---aligncontrol"></a>備考 - alignControl

コントロールの左上隅は、最も長いラベルに基づいて配置されます。

### <a name="examples---aligncontrol"></a>例 - alignControl

次の例は、最も長いラベルの長さに基づいて、フォーム コンボ ボックス コントロールを他のコントロールと揃えるための alignControl メソッドの呼び出しを示しています。

```xpp
boolean bAlign; 
// The combo variable was previously assigned 
// as a FormComboBoxControl type. 
// Retrieve the alignControl property. 
bAlign = combo.alignControl(); 
// Set the alignControl property. 
combo.alignControl(false);
```

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を修正できるかどうかを決定します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  
allowEdit プロパティに割り当てる値 (オプション)。

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

## <a name="method-appendnew"></a>メソッド appendNew

```xpp
public boolean appendNew([boolean value])
```

### <a name="parameters---appendnew"></a>パラメーター - appendNew

値  

### <a name="return-value---appendnew"></a>戻り値 - appendNew

## <a name="method-arrayindex"></a>メソッド arrayIndex

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a>パラメーター - arrayIndex

値  

### <a name="return-value---arrayindex"></a>戻り値 - arrayIndex

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  
autoDeclaration プロパティに割り当てる値 (オプション)。

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
コントロールの背景色として割り当てる値 (オプション)。 これは、コントロール� の配色または Winapi::RGB2int 値のいずれかの値にできます。

### <a name="return-value---backgroundcolor"></a>戻り値 - backgroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---backgroundcolor"></a>備考 - backgroundColor

返される整数には、次のような RGB カラーが含まれます。

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

コントロール� のバックグラウンドを透明にできるかどうかを決定します。

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a>パラメーター - backStyle

値  
コントロールの背景スタイルとして割り当てる値 (オプション)。

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

次の例では、ユーザーがフォーム コンボ ボックス コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。

```xpp
public int beginDrag(int _x, int _y) 
{ 
    int ret; 
    info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
    ret = super(_x, _y); 
    return ret; 
}
```

## <a name="method-bold"></a>メソッド bold

コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a>パラメーター - bold

値  
コントロールのボールド設定に割り当てる値 (オプション)。

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

コントロールの境界線のスタイルを取得または設定します。

```xpp
public int border([int value])
```

### <a name="parameters---border"></a>パラメーター - border

値  
コントロールの境界スタイルとして割り当てる値 (オプション)。

### <a name="return-value---border"></a>戻り値 - border

0 (ゼロ) から 4 までの整数。

### <a name="remarks---border"></a>備考 - border

返される整数には、次のような境界線のスタイル線が含まれます。

-   0 � 自動。
-   1 � 3D。
-   2 � 単一明細行。
-   3 � 均一。
-   4 � なし。

### <a name="examples---border"></a>例 - border

次の例は、コントロールの境界線のスタイルを取得および設定する方法を示しています。

```xpp
// Retrieve the border style. 
info (strfmt("border: %1", this.border())); 
// Set the border style. 
this.border(2);
```

## <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a>パラメーター - cacheDataMethod

値  

### <a name="return-value---cachedatamethod"></a>戻り値 - cacheDataMethod

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

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語語版 Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

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

| 値です。 | スタイル。                 |
|--------|------------------------|
| 0      | 既定。               |
| 1      | Windows パレット。   |
| 2      | 真の配色。 |

## <a name="method-combotype"></a>メソッド comboType

コントロールのコンボ ボックスのタイプを設定するか返します。

```xpp
public int comboType([int value])
```

### <a name="parameters---combotype"></a>パラメーター - comboType

値  
コンボ ボックス コントロールのタイプとして割り当てる値 (オプション)。

### <a name="return-value---combotype"></a>戻り値 - comboType

コントロールのコンボ ボックスのタイプ。

### <a name="remarks---combotype"></a>備考 - comboType

次のテーブルは、コンボ ボックス タイプの値を示しています。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 標準    |
| 1     | リスト        |

### <a name="examples---combotype"></a>例 - comboType

次の例は、コントロールに使用されるコンボ ボックスのタイプを取得および設定する方法を示しています。

```xpp
// Retrieve the type of combo box control. 
info(strfmt("comboType: %1", this.comboType())); 
// Set the type of combo box control. 
this.comboType(1);
```

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

次の例は、コントロールのコンフィギュレーション キーの設定と取得を示しています。

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

リストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 さらに、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="examples---configurationkeyex"></a>例 - configurationKeyEx

次の例は、コントロールのコンフィギュレーション キー ID の取得を示しています。

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

## <a name="method-count"></a>メソッド count

コンボ ボックス コントロール内の項目の数を返します。

```xpp
public int count()
```

### <a name="return-value---count"></a>戻り値 - count

コンボ ボックス コントロール内の項目の数。

### <a name="examples---count"></a>例 - count

次の例は、count メソッドの使用方法を示しています。

```xpp
int j; 
j = this.count();
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

## <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a>パラメーター - countryRegionContextField

値  

### <a name="return-value---countryregioncontextfield"></a>戻り値 - countryRegionContextField

## <a name="method-datafield"></a>メソッド dataField

コンボ ボックス コントロールのデータ フィールドを設定するか返します。

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a>パラメーター - dataField

値  
コンボ ボックス コントロールのデータ フィールド ID として割り当てる値 (オプション)。

### <a name="return-value---datafield"></a>戻り値 - dataField

コンボ ボックス コントロールのデータ フィールド ID の値。

### <a name="examples---datafield"></a>例 - dataField

次の例は、コンボ ボックス コントロールのデータ フィールドを設定して返す方法を示しています。

```xpp
fieldID i; 
// The combo variable is a previously assigned  
// FormComboBoxControl value. 
// Retrieve the data Field. 
i = combo.dataField(); 
// Set the data field. 
combo.dataField(fieldnum(CustTable, IdentificationNumber));
```

## <a name="method-datamethod"></a>メソッド dataMethod

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a>パラメーター - dataMethod

値  

### <a name="return-value---datamethod"></a>戻り値 - dataMethod

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

コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

値  
コンボ ボックス コントロールのデータ ソースとして割り当てる値 (オプション)。

### <a name="return-value---datasource"></a>戻り値 - dataSource

使用する必要のあるデータ ソースの ID。

### <a name="examples---datasource"></a>例 - dataSource

次の例は、コンボ ボックス コントロールのデータ ソースを設定して返す方法を示しています。

```xpp
int i; 
// The combo variable was previously assigned  
// as a FormComboBoxControl variable. 
// Retrieve the data source. 
i = combo.dataSource(); 
// Set the data source. 
combo.dataSource(tablenum(CustTable));
```

## <a name="method-displaylength"></a>メソッド displayLength

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a>パラメーター - displayLength

値  

<!-- -->

モード  

### <a name="return-value---displaylength"></a>戻り値 - displayLength

## <a name="method-displaylengthmode"></a>メソッド displayLengthMode

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a>パラメーター - displayLengthMode

モード  

### <a name="return-value---displaylengthmode"></a>戻り値 - displayLengthMode

## <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a>パラメーター - displayLengthValue

値  

### <a name="return-value---displaylengthvalue"></a>戻り値 - displayLengthValue

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
boolean bDragDrop; 
// The combo variable was previously assigned  
// as a FormComboBoxControl value. 
// Retrieve the drag-and-drop-enabled value. 
bDragDrop = combo.dragDrop(); 
// Set the drag-and-drop-enabled value. 
combo.dragDrop(true);
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

フォーム コンボ ボックス コントロールをドラッグしたときに表示されるテキストを返します。

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a>戻り値 - dragText

コンボ ボックス コントロールをドラッグしたときに表示されるテキスト。コンボ ボックス コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

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

## <a name="method-enumtype"></a>メソッド enumType

```xpp
public EnumId enumType([EnumId value])
```

### <a name="parameters---enumtype"></a>パラメーター - enumType

値  

### <a name="return-value---enumtype"></a>戻り値 - enumType

## <a name="method-enumtypevalue"></a>メソッド enumTypeValue

```xpp
public EnumId enumTypeValue()
```

### <a name="return-value---enumtypevalue"></a>戻り値 - enumTypeValue

## <a name="method-extendeddatatype"></a>メソッド extendedDataType

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a>パラメーター - extendedDataType

値  

### <a name="return-value---extendeddatatype"></a>戻り値 - extendedDataType

## <a name="method-fasttabsummary"></a>メソッド fastTabSummary

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a>パラメーター - fastTabSummary

値  

### <a name="return-value---fasttabsummary"></a>戻り値 - fastTabSummary

## <a name="method-find"></a>メソッド find

```xpp
public int find(str string)
```

### <a name="parameters---find"></a>パラメーター - find

文字列  

### <a name="return-value---find"></a>戻り値 - find

## <a name="method-font"></a>メソッド font

コントロールに使用するフォントの名前を取得または設定します。

```xpp
public str font([str value])
```

### <a name="parameters---font"></a>パラメーター - font

値  
フォーム コンボ ボックス コントロール内のテキストに使用するフォントを示す文字列データ型; オプション。

### <a name="return-value---font"></a>戻り値 - font

Tahoma や Verdana など、使用されるべきフォントの名前。

### <a name="examples---font"></a>例 - font

次の例は、フォーム コンボ ボックス コントロールのフォントを返して設定する方法を示しています。

```xpp
str strFont; 
; 
// The ctrl variable was previously assigned  
// as a form combo box control value. 
// Retrieve the font. 
strFont = ctrl.font(); 
// Set the font. 
ctrl.font("Times New Roman");
```

## <a name="method-fontsize"></a>メソッド fontSize

コントロールに使用するフォントのサイズを取得または設定します。

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a>パラメーター - fontSize

値  
フォームのコンボ ボック スコントロール内のテキストのフォント サイズをポイント単位で示す整数データ型 (オプション)。

### <a name="return-value---fontsize"></a>戻り値 - fontSize

ポイント単位のフォントの高さ。

### <a name="examples---fontsize"></a>例 - fontSize

次の例は、フォーム コンボ ボックス コントロールのフォント サイズを返して設定する方法を示しています。

```xpp
int nSize; 
// The ctrl variable was previously assigned  
// as a form combo box control. 
// Retrieve the font size. 
nSize = ctrl.fontSize(); 
// Set the font size. 
ctrl.fontSize(16);
```

## <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

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
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

## <a name="method-getedittext"></a>メソッド getEditText

```xpp
public str getEditText()
```

### <a name="return-value---getedittext"></a>戻り値 - getEditText

## <a name="method-gettext"></a>メソッド getText

```xpp
public str getText(int index)
```

### <a name="parameters---gettext"></a>パラメーター - getText

指数  

### <a name="return-value---gettext"></a>戻り値 - getText

## <a name="method-haschanged"></a>メソッド hasChanged

フォーム コンボ ボックス コントロールの内容が変更されたかどうかを示す値を設定するか返します。

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a>パラメーター - hasChanged

val  
コンボ ボックス コントロールの hasChanged 値として割り当てる値、オプション。

### <a name="return-value---haschanged"></a>戻り値 - hasChanged

コンボ ボックス コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="examples---haschanged"></a>例 - hasChanged

次の例は、コンボ ボックス コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。

```xpp
boolean bHasChanged; 
// The ctrl variable was previously assigned 
// as a FormComboBoxControl variable. 
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

ピクセル単位でコントロールの高さを取得または設定します。

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

次の例は、フォーム コンボ ボックス コントロールの高さ計算モードを返して設定する方法を示しています。

```xpp
int nHeightMode; 
// The ctrl variable was previously assigned 
// as a form combo box control type. 
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

次の例は、コンボ ボックス コントロールの高さの値を返して設定する方法を示しています。

```xpp
int nHeightValue; 
// The ctrl variable was previously assigned 
// as a form combo box control type. 
// Retrieve the height value. 
nHeightValue = ctrl.heightValue(); 
// Set the height value. 
ctrl.heightMode(-1); 
ctrl.heightValue(22);
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
コントロールのヘルプ テキストとして割り当てる値 (オプション)。

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

## <a name="method-hidefirstentry"></a>メソッド hideFirstEntry

コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値を設定するか返します。

```xpp
public boolean hideFirstEntry([boolean value])
```

### <a name="parameters---hidefirstentry"></a>パラメーター - hideFirstEntry

値  
コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値、オプション。

### <a name="return-value---hidefirstentry"></a>戻り値 - hideFirstEntry

コンボ ボックス コントロール内の最初のエントリが非表示の場合は true。それ以外の場合は、false。

### <a name="remarks---hidefirstentry"></a>備考 - hideFirstEntry

コンボ ボックス コントロールの最初のエントリを非表示にすることにより、必須プロパティがはいに設定されている列挙データベース フィールドの動作をエミュレートするコントロールを有効にします。

### <a name="examples---hidefirstentry"></a>例 - hideFirstEntry

次の例は、コンボ ボックス コントロールの最初のエントリが非表示になっているかどうかを示す値を返して設定する方法を示しています。

```xpp
boolean bHideFirstEntry; 
// The ctrl variable was previously assigned 
// as a form combo box control type. 
// Retrieve the hideFirstEntry value. 
bHideFirstEntry = ctrl.hideFirstEntry(); 
// Set the hideFirstEntry value. 
bHideFirstEntry = ctrl.hideFirstEntry(true);
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

コントロールがコンテナーである場合は true。それ以外の場合は、false。

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

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。

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

「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメータで指定されたレベル以上である必要があります。

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

## <a name="method-isvalid"></a>メソッド isValid

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a>戻り値 - isValid

## <a name="method-italic"></a>メソッド italic

コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a>パラメーター - italic

値  
コントロールのイタリック設定に割り当てる値 (オプション)。

### <a name="return-value---italic"></a>戻り値 - italic

コントロール内のテキストが斜体である場合は true。それ以外の場合は false。

## <a name="method-item"></a>メソッド item

```xpp
public int item([int value])
```

### <a name="parameters---item"></a>パラメーター - item

値  

### <a name="return-value---item"></a>戻り値 - item

## <a name="method-items"></a>メソッド items

```xpp
public int items([int value])
```

### <a name="parameters---items"></a>パラメーター - items

値  

### <a name="return-value---items"></a>戻り値 - items

## <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

```xpp
public str label([str value])
```

### <a name="parameters---label"></a>パラメーター - label

値  
コントロールのラベルとして割り当てる値 (オプション)。

### <a name="return-value---label"></a>戻り値 - label

ラベル文字列の現在の値。

### <a name="remarks---label"></a>備考 - label

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="examples---label"></a>例 - label

次の例は、コントロールのラベルを返して設定する方法を示しています。

```xpp
// Return the label value. 
info(strfmt("label: %1", this.label())); 
// Set the label value. 
this.label("New label text goes here");
```

## <a name="method-labelalignment"></a>メソッド labelAlignment

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a>パラメーター - labelAlignment

値  

### <a name="return-value---labelalignment"></a>戻り値 - labelAlignment

## <a name="method-labelbold"></a>メソッド labelBold

コントロールのラベルの太字設定を示す値を設定するか返します。

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a>パラメーター - labelBold

値  
ラベルのボールド設定に割り当てる値。 これは、ReportControlBold 列挙型からの値の 1 つです。

### <a name="return-value---labelbold"></a>戻り値 - labelBold

コントロールのラベルの太字設定を示す ReportControlBold 列挙の値。

## <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a>パラメーター - labelCharacterSet

値  

### <a name="return-value---labelcharacterset"></a>戻り値 - labelCharacterSet

## <a name="method-labelfont"></a>メソッド labelFont

フォーム コンボ ボックス コントロールのラベル テキストのフォントを設定するか返します。

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a>パラメーター - labelFont

値  
フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型; オプション。

### <a name="return-value---labelfont"></a>戻り値 - labelFont

フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型値。

### <a name="examples---labelfont"></a>例 - labelFont

次の例は、フォーム コンボ ボックス コントロール内のラベル テキストのフォントを返して設定する方法を示しています。

```xpp
str strLabelFont; 
// The ctrl variable was previously assigned  
// as a form combo box control variable. 
// Retrieve the font. 
strLabelFont = ctrl.labelFont(); 
// Set the label font. 
ctrl.labelFont("Times New Roman");
```

## <a name="method-labelfontsize"></a>メソッド labelFontSize

フォーム コンボ ボックス コントロールのラベル テキストのフォント サイズをポイント単位で設定するか返します。

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a>パラメーター - labelFontSize

値  
フォーム コンボ ボックス コントロール内にラベル テキストのフォント サイズをポイントで示す整数データ型 (オプション)。

### <a name="return-value---labelfontsize"></a>戻り値 - labelFontSize

フォーム コンボ ボックス コントロール内にテキストのラベル フォント サイズをポイントで示す整数データ型値です。

### <a name="examples---labelfontsize"></a>例 - labelFontSize

次の例は、フォーム コンボ ボックス コントロールのラベルのフォント サイズを返して設定する方法を示しています。

```xpp
int nSize; 
// The ctrl variable was previously assigned  
// as a form combo box control. 
// Retrieve the label font size. 
nSize = ctrl.labelFontSize(); 
// Set the label font size. 
ctrl.labelFontSize(16);
```

## <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a>パラメーター - labelForegroundColor

値  

### <a name="return-value---labelforegroundcolor"></a>戻り値 - labelForegroundColor

## <a name="method-labelguide"></a>メソッド labelGuide

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a>パラメーター - labelGuide

値  

### <a name="return-value---labelguide"></a>戻り値 - labelGuide

## <a name="method-labelheight"></a>メソッド labelHeight

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a>パラメーター - labelHeight

値  

<!-- -->

モード  

### <a name="return-value---labelheight"></a>戻り値 - labelHeight

## <a name="method-labelheightmode"></a>メソッド labelHeightMode

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a>パラメーター - labelHeightMode

値  

### <a name="return-value---labelheightmode"></a>戻り値 - labelHeightMode

## <a name="method-labelheightvalue"></a>メソッド labelHeightValue

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a>パラメーター - labelHeightValue

値  

### <a name="return-value---labelheightvalue"></a>戻り値 - labelHeightValue

## <a name="method-labelitalic"></a>メソッド labelItalic

コントロールのラベルのテキストが斜体で表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a>パラメーター - labelItalic

値  
コントロールのラベルのイタリック設定に割り当てる値 (オプション)。

### <a name="return-value---labelitalic"></a>戻り値 - labelItalic

コントロールのラベル内のテキストが斜体である場合は true。それ以外の場合は false。

## <a name="method-labelmousedblclick"></a>メソッド labelMouseDblClick

コントロールのラベルがユーザーにダブルクリックされると呼び出されます。

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a>パラメーター - labelMouseDblClick

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

### <a name="return-value---labelmousedblclick"></a>戻り値 - labelMouseDblClick

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---labelmousedblclick"></a>備考 - labelMouseDblClick

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="examples---labelmousedblclick"></a>例 - labelMouseDblClick

次の例は、Infolog に labelMouseDblClick イベントのパラメーターを表示する方法を示しています。

```xpp
public int labelMouseDblClick(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    ; 
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

## <a name="method-labelmousedown"></a>メソッド labelMouseDown

ユーザーがコントロールのラベル上でマウス ボタンをクリックすると呼び出されます。

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a>パラメーター - labelMouseDown

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

### <a name="return-value---labelmousedown"></a>戻り値 - labelMouseDown

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---labelmousedown"></a>備考 - labelMouseDown

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="examples---labelmousedown"></a>例 - labelMouseDown

次の例は、Infolog に labelMouseDown イベントのパラメーターを表示する方法を示しています。

```xpp
public int labelMouseDown(int x,  
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

## <a name="method-labelmouseup"></a>メソッド labelMouseUp

ユーザーがコントロールのラベル上でマウス ボタンを放すと呼び出されます。

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a>パラメーター - labelMouseUp

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

### <a name="return-value---labelmouseup"></a>戻り値 - labelMouseUp

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---labelmouseup"></a>備考 - labelMouseUp

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="examples---labelmouseup"></a>例 - labelMouseUp

次の例は、Infolog に labelMouseUp イベントのパラメーターを表示する方法を示しています。

```xpp
public int labelMouseUp(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    ; 
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

## <a name="method-labelposition"></a>メソッド labelPosition

コントロールのラベルの位置を設定するか返します。

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a>パラメーター - labelPosition

値  
ラベル位置に割り当てる値 (オプション)。

### <a name="return-value---labelposition"></a>戻り値 - labelPosition

ラベルの位置を表す整数。

### <a name="remarks---labelposition"></a>備考 - labelPosition

値パラメーターが 0 (ゼロ) に設定されている場合、ラベルは、コントロールの左側に配置されます。 値パラメーターが 1 に設定されている場合、ラベルはコントロールの上に配置されます。 0 (ゼロ) の戻り値は、ラベルがコントロールの左側に置かれていることを示します。 1 の戻り値は、ラベルがコントロールの上に置かれていることを示します。

### <a name="examples---labelposition"></a>例 - labelPosition

次の例は、ラベルの位置を返して設定する方法を示しています。

```xpp
// Retrieve the label position. 
info (strfmt("label: %1", this.labelPosition())); 
// Set the label position. 
this.labelPosition(1);  // 1 == Above, 0 == Left
```

## <a name="method-labelunderline"></a>メソッド labelUnderline

コントロールのラベルのテキストが下線付きで表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a>パラメーター - labelUnderline

値  
コントロールのラベルの下線設定に割り当てる値 (オプション)。

### <a name="return-value---labelunderline"></a>戻り値 - labelUnderline

コントロールのラベル内のテキストが下線付きである場合は true。それ以外の場合は false。

## <a name="method-labelwidth"></a>メソッド labelWidth

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a>パラメーター - labelWidth

値  

<!-- -->

モード  

### <a name="return-value---labelwidth"></a>戻り値 - labelWidth

## <a name="method-labelwidthmode"></a>メソッド labelWidthMode

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a>パラメーター - labelWidthMode

値  

### <a name="return-value---labelwidthmode"></a>戻り値 - labelWidthMode

## <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a>パラメーター - labelWidthValue

値  

### <a name="return-value---labelwidthvalue"></a>戻り値 - labelWidthValue

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

## <a name="method-modified"></a>メソッド modified

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a>戻り値 - modified

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
    ; 
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

ユーザーがコントロール上でマウス ボタンを放すと呼び出されます。

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

### <a name="examples---mouseup"></a>例 - mouseUp

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseUp イベントのパラメーターを表示する方法を示しています。

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

## <a name="method-previewpartref"></a>メソッド previewPartRef

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a>パラメーター - previewPartRef

値  

### <a name="return-value---previewpartref"></a>戻り値 - previewPartRef

## <a name="method-promptrect"></a>メソッド promptrect

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a>パラメーター - promptrect

値  

### <a name="return-value---promptrect"></a>戻り値 - promptrect

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

次の例は、コントロールのセキュリティ キー IDの取得と割り当てを示しています。

```xpp
DictSecurityKey dsk; 
securityKeyId ski; 
; 
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

## <a name="method-selection"></a>メソッド selection

```xpp
public int selection([int value])
```

### <a name="parameters---selection"></a>パラメーター - selection

値  

### <a name="return-value---selection"></a>戻り値 - selection

## <a name="method-selectionchange"></a>メソッド selectionChange

ユーザーがコンボ ボックス コントロールで選択した項目を変更したことを示します。

```xpp
public int selectionChange()
```

### <a name="return-value---selectionchange"></a>戻り値 - selectionChange

イベントが正常に処理された場合は true。それ以外の場合は、false。

### <a name="examples---selectionchange"></a>例 - selectionChange

次の例は、ユーザーがコンボ ボックス コントロールで選択した項目を変更するときに、Infolog メッセージを表示するために selectionChange メソッドを上書きする方法を示しています。

```xpp
public int selectionChange() 
{ 
    int ret; 
    info("The selection has changed."); 
    ret = super(); 
    return ret; 
}
```

## <a name="method-selecttext"></a>メソッド selectText

```xpp
public int selectText(str string)
```

### <a name="parameters---selecttext"></a>パラメーター - selectText

文字列  

### <a name="return-value---selecttext"></a>戻り値 - selectText

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

## <a name="method-showlabel"></a>メソッド showLabel

コントロールのラベルがフォームに表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a>パラメーター - showLabel

値  
コントロールの showLabel プロパティに割り当てる値。

### <a name="return-value---showlabel"></a>戻り値 - showLabel

ラベルを表示する必要がある場合は true。それ以外の場合は false。

### <a name="examples---showlabel"></a>例 - showLabel

次の例は、コントロールの showLabel プロパティを返して設定する方法を示しています。

```xpp
// Return the showLabel value. 
info(strfmt("showLabel: %1", this.showLabel())); 
// Set the showLabel value. 
this.showLabel(false);
```

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

## <a name="method-sort"></a>メソッド sort

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a>パラメーター - sort

sortDirection  

### <a name="return-value---sort"></a>戻り値 - sort

## <a name="method-text"></a>メソッド text

コントロールのテキストを設定するか返します。

```xpp
public str text([str value])
```

### <a name="parameters---text"></a>パラメーター - text

値  
コントロールのテキストとして割り当てる値 (オプション)。

### <a name="return-value---text"></a>戻り値 - text

コントロールのテキスト。コントロールにテキストが割り当てられていない場合は空の文字列。

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

## <a name="method-type"></a>メソッドのタイプ

```xpp
public int type([int value])
```

### <a name="parameters---type"></a>パラメーター - type

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

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

フォーム コンボ ボックス コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a>パラメーター - userHide

値  
コントロールがユーザーから非表示になっているどうかを示す値、オプション。

### <a name="return-value---userhide"></a>戻り値 - userHide

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

### <a name="remarks---userhide"></a>備考 - userHide

ユーザーは、コンボ ボックス コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コンボ ボックス コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 userHide メソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="examples---userhide"></a>例 - userHide

次の例は、コンボ ボックス コントロールがユーザーから隠されているかどうかを示す値を返して設定する方法を示しています。

```xpp
int nUserHide; 
// The ctrl variable was previously assigned  
// as a form combo box control variable. 
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

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コンボ ボックス コントロールがスキップされるかどうかを示す値を設定するか返します。

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
// The ctrl variable was previously assigned as a 
// FormComboBoxControl variable. 
// Return the userSkip property. 
nUserSkip = ctrl.userSkip(); 
// Set the userSkip property. 
ctrl.userSkip(1);
```

## <a name="method-userwidth"></a>メソッド userWidth

ピクセル単位でフォーム コンボ ボックス コントロールの幅を設定するか返します。

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

次の例は、フォーム コンボ ボックス コントロールのユーザーの幅を返して設定する方法を示しています。

```xpp
int nWidth; 
// The ctrl variable was previously defined  
// as the FormComboBoxControl variable. 
// Return the width. 
nWidth = ctrl.userWidth(); 
// Specify the width. 
ctrl.userWidth(90);  // 15 characters * 6 pixels == 90
```

## <a name="method-validate"></a>メソッド validate

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a>戻り値 - validate

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
コントロールの AutoMode 列挙値; オプション。

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

## <a name="method-vieweditmode"></a>メソッド viewEditMode

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a>パラメーター - viewEditMode

値  

### <a name="return-value---vieweditmode"></a>戻り値 - viewEditMode

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
コントロール幅の計算方法を示す整数値。 値は、Exact モードの場合は -1、Auto モードの場合は 0、Column width モードの場合は 1 になります。

### <a name="return-value---widthmode"></a>戻り値 - widthMode

現在の計算モードを示す整数値。

### <a name="remarks---widthmode"></a>備考 - widthMode

次の表に従って幅を計算します。

| モード         | 幅計算。                                                                        |
|--------------|-------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="examples---widthmode"></a>例 - widthMode

次の例は、フォーム コンボ ボックス コントロールの幅の計算モードを返す方法と設定する方法を示しています。

```xpp
int nWidthMode; 
; 
// The ctrl variable was previously assigned 
// as a form combo box control variable. 
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

次の例は、フォーム コンボ ボックス コントロールの幅の値を返して設定する方法を示しています。

```xpp
int nWidthValue; 
// The ctrl variable was previously assigned 
// as a form combo box control variable. 
// Retrieve the width value. 
nWidthValue = ctrl.widthValue(); 
// Set the width value. 
ctrl.widthMode(-1); 
ctrl.widthValue(160);
```

## <a name="method-filter"></a>メソッド filter

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a>パラメーター - filter

filterStr  

## <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

```xpp
public void displayControl()
```

## <a name="method-onvalidated"></a>メソッド OnValidated

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a>パラメーター - OnValidated

sender  

<!-- -->

e  

## <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

```xpp
public void dragLeave()
```

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

```xpp
public void resetUserSetting()
```

## <a name="method-onmodified"></a>メソッド OnModified

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a>パラメーター - OnModified

sender  

<!-- -->

e  

## <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

```xpp
public void context()
```

## <a name="method-beginupdate"></a>メソッド beginUpdate

```xpp
public void beginUpdate()
```

## <a name="method-ongotfocus"></a>メソッド OnGotFocus

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a>パラメーター - OnGotFocus

sender  

<!-- -->

e  

## <a name="method-setedittext"></a>メソッド setEditText

```xpp
public void setEditText(str string)
```

### <a name="parameters---setedittext"></a>パラメーター - setEditText

文字列  

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

## <a name="method-paste"></a>メソッド paste

フォーム コンボ ボックス コントロールをフォームに貼り付けます。

```xpp
public void paste()
```

## <a name="method-clear"></a>メソッド clear

コンボ ボックス リストのエントリをクリアします。

```xpp
public void clear()
```

### <a name="examples---clear"></a>例 - clear

次の例は、コンボ ボックス リスト内のエントリをクリアする方法を示しています。

```xpp
this.clear();
```

## <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

```xpp
public void gotFocus()
```

## <a name="method-onlostfocus"></a>メソッド OnLostFocus

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a>パラメーター - OnLostFocus

sender  

<!-- -->

e  

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

## <a name="method-copy"></a>メソッド copy

フォームのコンボ ボックス コントロールをコピーします。

```xpp
public void copy()
```

## <a name="method-onselectionchanging"></a>メソッド OnSelectionChanging

```xpp
private void OnSelectionChanging([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanging"></a>パラメーター - OnSelectionChanging

sender  

<!-- -->

e  

## <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了すると呼び出されます。

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a>備考 - endDrag

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="examples---enddrag"></a>例 - endDrag

次の例では、ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。

```xpp
public void endDrag() 
{ 
    info("EndDrag completed"); 
    super(); 
}
```

## <a name="method-lookup"></a>メソッド lookup

```xpp
public void lookup()
```

## <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

```xpp
public void setFocus()
```

## <a name="method-insert"></a>メソッド insert

指定した位置にあるコンボ ボックスに文字列の値を挿入します。

```xpp
public void insert(str string, int index)
```

### <a name="parameters---insert"></a>パラメーター - insert

文字列  
後に続く文字列を挿入する位置。 文字列をリストの最初の項目にする場合は、値を 0 (ゼロ) に設定します。

<!-- -->

指数  
後に続く文字列を挿入する位置。 文字列をリストの最初の項目にする場合は、値を 0 (ゼロ) に設定します。

### <a name="examples---insert"></a>例 - insert

次の例は、コンボ ボックス リストに文字列を挿入する方法を示しています。

```xpp
this.insert("willow", 3);
```

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

### <a name="examples---mouseenter"></a>例 - mouseEnter

次の例は、Infolog に mouseEnter イベントのパラメーターを表示する方法を示しています。

```xpp
public void mouseEnter(int x,  
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
}
```

## <a name="method-onenter"></a>メソッド OnEnter

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a>パラメーター - OnEnter

sender  

<!-- -->

e  

## <a name="method-delete"></a>メソッド delete

コンボ ボックスのリストから文字列値を削除します。

```xpp
public void delete(str string)
```

### <a name="parameters---delete"></a>パラメーター - delete

文字列  
コンボ ボックスのリストから削除する文字列値。

### <a name="examples---delete"></a>例 - delete

次の例は、コンボ ボックス リストから文字列値を削除する方法を示しています。

```xpp
this.delete("Model 12357");
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

## <a name="method-add"></a>メソッド add

コンボ ボックス リストに文字列値を追加します。

```xpp
public void add(str string)
```

### <a name="parameters---add"></a>パラメーター - add

文字列  
コンボ ボックスのリストに追加する文字列値。

### <a name="remarks---add"></a>備考 - add

文字列はリストの末尾に追加されます。 文字列を一覧の特定の位置に格納するには、insert メソッドを使用します。

### <a name="examples---add"></a>例 - add

次の例は、コンボ ボックス リストに文字列を追加する方法を示しています。

```xpp
this.add("maple"); 
this.add("oak"); 
this.add("pine");
```

## <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コンボ ボックス コントロールの最適な列の幅と高さを指定します。

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

次の例は、コンボ ボックス コントロールの優先幅と高さを設定する方法を示しています。

```xpp
// The nWidth and nHeight variables were  
// previously assigned as int variables. 
// The ctrl variable was previously assigned 
// as a FormComboBoxControl variable. 
ctrl.prefColumnSize( nWidth, nHeight);
```

## <a name="method-onvalidating"></a>メソッド OnValidating

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a>パラメーター - OnValidating

sender  

<!-- -->

e  

## <a name="method-undo"></a>メソッド undo

```xpp
public void undo()
```

## <a name="method-jumpref"></a>メソッド jumpRef

```xpp
public void jumpRef()
```

## <a name="method-onselectionchanged"></a>メソッド OnSelectionChanged

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a>パラメーター - OnSelectionChanged

sender  

<!-- -->

e  

## <a name="method-endupdate"></a>メソッド endUpdate

```xpp
public void endUpdate()
```

## <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

```xpp
public void lostFocus()
```

## <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

```xpp
public void mouseLeave()
```

## <a name="method-onlookup"></a>メソッド OnLookup

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a>パラメーター - OnLookup

sender  

<!-- -->

e  

## <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

```xpp
public void cut()
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

## <a name="method-onleaving"></a>メソッド OnLeaving

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a>パラメーター - OnLeaving

sender  

<!-- -->

e  

## <a name="method-setdropsize"></a>メソッド setDropSize

```xpp
public void setDropSize([int lines])
```

### <a name="parameters---setdropsize"></a>パラメーター - setDropSize

明細行  

