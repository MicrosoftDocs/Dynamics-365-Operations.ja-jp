---
title: F クラス (FormListBoxControl から FormNotifyEventArgs)
description: FormListBoxControl から FormNotifyEventArgs までのクラスの API 参照。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 63763
ms.assetid: 55d76f8e-ad30-4ee1-bed8-bbb1eb4f8296
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa5e2a60f5edcc7ca92afa2125799fd55a1119f3
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537044"
---
# <a name="f-classes-formlistboxcontrol-to-formnotifyeventargs"></a>F クラス (FormListBoxControl から FormNotifyEventArgs)

[!include [banner](../includes/banner.md)]

FormListBoxControl から FormNotifyEventArgs までのクラスの API 参照。

<a name="class-formlistboxcontrol"></a>クラス FormListBoxControl
------------------------

    class FormListBoxControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                                     |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールでチェックされているコンフィギュレーション キーの名前を含む一覧を取得します。                                                                        |
| public int count()                                                                                          |                                                                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int doubleClick()                                                                                    |                                                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public EnumId enumType(\[EnumId value\])                                                                    |                                                                                                                                                                         |
| public EnumId enumTypeValue()                                                                               |                                                                                                                                                                         |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                                                         |
| public int find(str string)                                                                                 |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public str getText(int index)                                                                               |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public boolean hideFirstEntry(\[boolean value\])                                                            |                                                                                                                                                                         |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドル (hWnd) を返します。                                                                                                                       |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
| public boolean isValid()                                                                                    |                                                                                                                                                                         |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public int item(\[int value\])                                                                              |                                                                                                                                                                         |
| public int items(\[int value\])                                                                             |                                                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                                                         |
| public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                        |                                                                                                                                                                         |
| public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                            |                                                                                                                                                                         |
| public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                              |                                                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                                                         |
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
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int selection(\[int value\])                                                                         |                                                                                                                                                                         |
| public int selectionChange()                                                                                |                                                                                                                                                                         |
| public int selectText(str string)                                                                           |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツールヒントを取得します。                                                                                                                                    |
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
| public int userHide(\[int value\])                                                                          | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ピクセル単位でコントロールの幅を設定するか返します。                                                                                                                     |
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void insert(str string, int index)                                                                   |                                                                                                                                                                         |
| public void delete(str string)                                                                              |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void add(str string)                                                                                 |                                                                                                                                                                         |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void undo()                                                                                          |                                                                                                                                                                         |
| public void endUpdate()                                                                                     |                                                                                                                                                                         |
| public void clear()                                                                                         |                                                                                                                                                                         |
| public void beginUpdate()                                                                                   |                                                                                                                                                                         |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])                        |                                                                                                                                                                         |
| public void lookup()                                                                                        |                                                                                                                                                                         |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])                         |                                                                                                                                                                         |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

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

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                 |
|--------|------------------------|
| 0      | 既定。               |
| 1      | Windows パレット。   |
| 2      | 真の配色。 |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールでチェックされているコンフィギュレーション キーの名前を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コンフィギュレーション キー名を持つ文字列の一覧。

#### <a name="remarks"></a>備考

取得されたリストに重複が含まれていません。 すべてのフォーム コントロールに適用されます。 コントロールがデータ バインドの場合は、一覧には、テーブルとフィールドのコンフィギュレーション キーも含まれます。 コントロールがプロパティ、拡張データ型、または Enumtype メソッドに空でない値を持っている場合は、これらの要素のコンフィギュレーション キーもリストに追加されます。 FormBuildMenuButtonControl クラスの実装の詳細のため、指定されたメニュー項目にある構成キーはリストに含まれません。 ただし、FormMenuButtonControl クラスでメソッドが呼び出される場合、一覧にはこれらが含まれます。

### <a name="method-count"></a>メソッド count

    public int count()

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-doubleclick"></a>メソッド doubleClick

    public int doubleClick()

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-enumtype"></a>メソッド enumType

    public EnumId enumType([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enumtypevalue"></a>メソッド enumTypeValue

    public EnumId enumTypeValue()

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-find"></a>メソッド find

    public int find(str string)

#### <a name="parameters"></a>パラメーター

string  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-gettext"></a>メソッド getText

    public str getText(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を指定する整数データ型。オプション。

<!-- -->

モード  
高さの計算方法を指定する整数データ型。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を指定する整数データ型値。オプション。

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数データ型。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして割り当てられる値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hidefirstentry"></a>メソッド hideFirstEntry

    public boolean hideFirstEntry([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドル (hWnd) を返します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

32 ビット ハンドル (hWnd)。

#### <a name="remarks"></a>備考

この処理は、すべてのコントロールに適用されます。 これは、Windows API を使用する場合に便利です。

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は false。 「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

### <a name="method-isvalid"></a>メソッド isValid

    public boolean isValid()

#### <a name="return-value"></a>戻り値

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public int item([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-items"></a>メソッド items

    public int items([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedblclick"></a>メソッド labelMouseDblClick

    public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmousedown"></a>メソッド labelMouseDown

    public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelmouseup"></a>メソッド labelMouseUp

    public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leave"></a>メソッド leave

    public boolean leave()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-modified"></a>メソッド modified

    public boolean modified()

#### <a name="return-value"></a>戻り値

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前 (オプション)。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-previewpartref"></a>メソッド previewPartRef

    public str previewPartRef([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-selection"></a>メソッド selection

    public int selection([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-selectionchange"></a>メソッド selectionChange

    public int selectionChange()

#### <a name="return-value"></a>戻り値

### <a name="method-selecttext"></a>メソッド selectText

    public int selectText(str string)

#### <a name="parameters"></a>パラメーター

string  

#### <a name="return-value"></a>戻り値

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は false。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツールヒントを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

ツールヒントに表示されるテキスト。

#### <a name="remarks"></a>備考

ポインターをコントロール上に移動するときはいつでも、ツールヒントがユーザーに表示されます。 このメソッドをオーバーライドして、コントロールに入力された値についてユーザーに指示テキストを表示できます。

#### <a name="examples"></a>例

    str tooltip() 
    { 
        return "Account numbers of customers eligible for discount"; 
    }

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は false。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ピクセル単位でコントロールの幅を設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-validate"></a>メソッド validate

    public boolean validate()

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
幅の計算方法を示す整数データ型。オプション。

<!-- -->

モード  
幅の計算方法を示す整数データ型。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅の計算方法を示す整数データ型値。オプション。

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  
幅をピクセル単位で指定する整数データ型。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-insert"></a>メソッド insert

    public void insert(str string, int index)

#### <a name="parameters"></a>パラメーター

string  

<!-- -->

指数  

### <a name="method-delete"></a>メソッド delete

    public void delete(str string)

#### <a name="parameters"></a>パラメーター

string  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-add"></a>メソッド add

    public void add(str string)

#### <a name="parameters"></a>パラメーター

string  

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-endupdate"></a>メソッド endUpdate

    public void endUpdate()

### <a name="method-clear"></a>メソッド clear

    public void clear()

### <a name="method-beginupdate"></a>メソッド beginUpdate

    public void beginUpdate()

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-onselectionchanging"></a>メソッド OnSelectionChanging

    private void OnSelectionChanging([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onselectionchanged"></a>メソッド OnSelectionChanged

    private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onvalidating"></a>メソッド OnValidating

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

## <a name="class-formlistcolumn"></a>クラス FormListColumn
    class FormListColumn extends Object

FormListColumn クラスは、フォームのリスト列機能を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                      | 説明                                               |
|-------------------------------------------------------------|-----------------------------------------------------------|
| public FormListFormat format(\[FormListFormat value\])      |                                                           |
| public int image(\[int value\])                             |                                                           |
| public int order(\[int value\])                             |                                                           |
| public int subItem(\[int value\])                           |                                                           |
| public str text(\[str value\])                              |                                                           |
| public str toString()                                       | クラス ハンドルと名前を含む文字列を返します。 |
| public int width(\[int value\])                             | コントロールの幅を取得または設定します。                    |
| public void new(\[str Text\], \[int ColNo\], \[int Width\]) | Object クラスの新しいインスタンスを初期化します。           |
| public void finalize()                                      |                                                           |

### <a name="method-format"></a>メソッド format

    public FormListFormat format([FormListFormat value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-image"></a>メソッド image

    public int image([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-order"></a>メソッド order

    public int order([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-subitem"></a>メソッド subItem

    public int subItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前を含む文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

クラスのテキスト表現。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width([int value])

#### <a name="parameters"></a>パラメーター

値  
リストの列幅として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード             | 幅計算                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| -1 - 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 0 - 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 - 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

幅と幅計算モードは別々に設定できます。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([str Text], [int ColNo], [int Width])

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

ColNo  

<!-- -->

幅  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-formlistcontrol"></a>クラス FormListControl
    class FormListControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
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

### <a name="method-add"></a>メソッド add

    public int add(str Text, [int image], [int index])

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

image  

<!-- -->

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-addcolumn"></a>メソッド addColumn

    public boolean addColumn(int Idx, FormListColumn Column)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

円柱  

#### <a name="return-value"></a>戻り値

### <a name="method-additem"></a>メソッド addItem

    public int addItem(FormListItem item)

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールが他のコントロールと揃っているかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム リスト コントロールが他のコントロールと一致しているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに基づいて配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を修正できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
データを変更できるかどうかを示すブール値データ型。

#### <a name="return-value"></a>戻り値

コントロールを変更することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-arrangeitem"></a>メソッド arrangeItem

    public boolean arrangeItem(FormListArrange ArrangeMethod)

#### <a name="parameters"></a>パラメーター

ArrangeMethod  

#### <a name="return-value"></a>戻り値

### <a name="method-autoarrange"></a>メソッド autoArrange

    public boolean autoArrange([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  
システムがフォーム リスト コントロールと同じ名前の変数を宣言できるかどうかを示すブール データ型。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

#### <a name="examples"></a>例

次の例は、システムがフォーム リスト コントロールと同じ名前を持つ変数を宣言できることを指定する autoDeclaration メソッドの呼び出しを示しています。

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

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  
背景色を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  
背景スタイルを示す整数データ型です。

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムの移動を開始するときを識別します。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
移動イベントのための y 座標を示す整数データ型です。

<!-- -->

y  
移動イベントのための y 座標を示す整数データ型です。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [beginDrag] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  
フォントの太さを指定する整数データ型です。

#### <a name="return-value"></a>戻り値

0 (ゼロ) から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 - 既定のフォントの重量を使用します。
-   1 - シン。
-   2 - エクストラ ライト。
-   3 - ライト。
-   4 - 標準。
-   5 - 中。
-   6 - セミボールド。
-   7 - 太字。
-   8 - 極太。
-   9 - ヘビー。

#### <a name="examples"></a>例

次の例は、フォントの重量を、重いことを示す、9 に設定する太字のメソッドの呼び出しを示しています。

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

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 単一明細行 |
| 3     | 均一        |
| 4     | None        |

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

文字数と明細行数に基づいて、フォームのリスト コントロールに使用されるフォント サイズを計算します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
行数を指定する整数データ型です。

<!-- -->

明細行  
行数を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールのサイズを指定するコンテナー データ型値。

### <a name="method-canscroll"></a>メソッド canScroll

    public boolean canScroll([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  
テキスト フォントの文字セットを指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

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

既定の文字セットは、現在のシステム ロケールに基づいて設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

### <a name="method-checkbox"></a>メソッド checkBox

    public boolean checkBox([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム リスト コントロールのカラー パレットを指定する整数データ型です。

#### <a name="return-value"></a>戻り値

0 (ゼロ) から 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

### <a name="method-columnheader"></a>メソッド columnHeader

フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型値を設定または取得します。

    public boolean columnHeader([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型。

#### <a name="return-value"></a>戻り値

コントロールに列ヘッダーがある場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。 フォームに列を追加する前に、columnHeader メソッドを呼び出す必要があります。それ以外の場合、列はフォーム リスト コントロールに表示されません。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールに列ヘッダーがないことを示す columnHeader メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

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

### <a name="method-columnheaderbutton"></a>メソッド columnHeaderButton

フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型値を設定または取得します。

    public boolean columnHeaderButton([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型。

#### <a name="return-value"></a>戻り値

コントロールに列ヘッダー ボタンがある場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。 フォームに列を追加する前に、columnHeaderButton メソッドを呼び出す必要があります。それ以外の場合、列はフォーム リスト コントロールに表示されません。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールに列ヘッダー ボタンがあることを示す columnHeaderButton メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

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

### <a name="method-columnimages"></a>メソッド columnImages

フォーム リスト コントロールに列イメージが含まれるかどうかを示すブール値データ型値を設定または取得します。

    public boolean columnImages([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム リスト コントロールに列の画像が含まれるかどうかを示すブール値データ型。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールに列イメージがある場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールに列イメージがあることを示す columnImages メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。


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

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コンフィギュレーション キーの ID を特定する configurationKeyId システム データ型。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールに銀行コンフィギュレーション キーを割り当てる configurationKey メソッドの呼び出しを示しています。

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

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリスト オブジェクト。

#### <a name="remarks"></a>備考

コントロールがデータソースにバインドされている場合、取得された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 さらに、取得したリストには、拡張データ型に適用される任意のコンフィギュレーション キー ID が含まれます。 リストに重複 ID は含まれません。

#### <a name="examples"></a>例

次の例は、configurationKeyEx メソッドの呼び出しを示しています。 ListEnumerator オブジェクトを使用すると、一覧全体の要素上を移動できます。

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

### <a name="method-copyitem"></a>メソッド copyItem

指定した項目をフォーム リスト コントロールにコピーします。

    public int copyItem(int Item, int InsertAt)

#### <a name="parameters"></a>パラメーター

項目  
品目がコピーされるリスト内の位置を指定する整数データ型です。

<!-- -->

InsertAt  
品目がコピーされるリスト内の位置を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

品目がコピーされるリスト内の位置を指定する整数データ型です。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールの 10 番目の位置にアイテムをコピーする copyItem メソッドの呼び出しを示しています。 FormListControl.getCount メソッドは、コントロール内の項目の数を返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-delete"></a>メソッド delete

フォーム リスト コントロールから指定した項目を削除します。

    public boolean delete(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  
削除される項目の 0 から始まるインデックス。

#### <a name="return-value"></a>戻り値

項目が削除された場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールから項目を削除する delete メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-deleteall"></a>メソッド deleteAll

フォーム リスト コントロールからすべての項目を削除します。

    public boolean deleteAll()

#### <a name="return-value"></a>戻り値

すべての項目が削除された場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールからすべての項目を削除する deleteAll メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-deletecolumn"></a>メソッド deleteColumn

フォーム リスト コントロールの指定した列を削除します。

    public boolean deleteColumn(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  
フォーム リスト コントロール内で列を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

列が削除された場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールから第 1 列を削除する deleteColumn メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、2 列をフォーム リスト コントロールに追加します。

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

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。

### <a name="method-dragover"></a>メソッド dragOver

ユーザーがフォーム リスト コントロールの境界内のアイテムにオブジェクトをドラッグするときを識別します。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

オブジェクトが移動、コピー、または指定された位置に移動されていないかどうかを示す FormDrag システム列挙値。

#### <a name="remarks"></a>備考

このメソッドは、DragDrop プロパティがコントロールの手動に設定されていて、beginDrag イベントがすでに開始されている場合にのみ呼び出されます。 イベントの詳細については、beginDrag を参照してください。 リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [dragOver] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム リスト コントロールでユーザーが項目をドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

ユーザーがフォーム リスト コントロールをドラッグするときに表示されるテキストを指定する文字列データ型値。

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [dragText] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-editlabels"></a>メソッド editLabels

ユーザーがフォーム リスト コントロールで項目名を変更できるかどうかを示します。

    public boolean editLabels([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーがフォーム リスト コントロール内の項目名を変更できるかどうかを指定するブール値データ型。

#### <a name="return-value"></a>戻り値

ユーザーが項目名を変更することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を追加する前に、editLabels メソッドを呼び出す必要があります。それ以外の場合、列はコントロールに表示されません。

#### <a name="examples"></a>例

次の例は、ユーザーがフォーム リスト コントロール内の項目名を変更できるようにする editLabels メソッドの呼び出しを示しています。 DictField.label メソッドは、フォーム リスト コントロールへの品目として追加される指定のテーブル フィールドのラベルを返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-ensurevisible"></a>メソッド ensureVisible

    public int ensureVisible(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

コントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  
前景色を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

#### <a name="examples"></a>例

次の例は、前景色をデスクトップ上のメニュー テキストの色に設定する foregroundColor メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-getcolumn"></a>メソッド getColumn

フォーム リスト コントロール内の指定された列の FormListColumn オブジェクトを取得します。

    public FormListColumn getColumn(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  
フォーム リスト コントロール内で列を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロール内の指定された列の FormListColumn オブジェクト。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロール内の列の FormListColumn オブジェクトを返す getColumn メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。


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

### <a name="method-getcolumncount"></a>メソッド getColumnCount

フォーム リスト コントロール内の列の数を取得します。

    public int getColumnCount()

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールの列数を指定する整数データ型値です。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールの列数を返す getColumnCount メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。


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

### <a name="method-getcolumnwidth"></a>メソッド getColumnWidth

フォーム リスト コントロール内の列の幅を取得します。

    public int getColumnWidth(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  
フォーム リスト コントロール内で列を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロール内で列幅を指定する整数データ型です。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロール内の列の幅を返す getColumnWidth メソッドの呼び出しを示しています。 FormListControl.setColumnWidth メソッドは、列の幅を指定します。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

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

### <a name="method-getcount"></a>メソッド getCount

フォーム リスト コントロールに含まれる項目の数を取得します。

    public int getCount()

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールに含まれている品目数を指定する整数データ型値です。

#### <a name="examples"></a>例

次の例は、getCount メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-getcountperpage"></a>メソッド getCountPerPage

    public int getCountPerPage()

#### <a name="return-value"></a>戻り値

### <a name="method-getimagelist"></a>メソッド getImagelist

    public Imagelist getImagelist([boolean GetLarge])

#### <a name="parameters"></a>パラメーター

GetLarge  

#### <a name="return-value"></a>戻り値

### <a name="method-getitem"></a>メソッド getItem

フォーム リスト コントロール内の項目の FormListItem オブジェクトを取得します。

    public FormListItem getItem(int Idx, [int SubItem])

#### <a name="parameters"></a>パラメーター

Idx  
フォーム リスト コントロール内でサブ項目を指定する整数データ型です。

<!-- -->

SubItem  
フォーム リスト コントロール内でサブ項目を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロール内の項目の FormListItem オブジェクト。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロール内の各項目の列の FormListItem オブジェクトを返す getItem メソッドの呼び出しを示しています。 FormListItem.toString メソッドは、各項目のテキスト文字列を返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-getitempos"></a>メソッド getItemPos

フォーム リスト コントロール内の項目の位置を取得します。

    public container getItemPos(int Item)

#### <a name="parameters"></a>パラメーター

項目  
フォーム リスト コントロール内の項目を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールの項目の位置を含むコンテナー データ型。 項目の位置は、x 座標と y 座標によって指定されます。

#### <a name="remarks"></a>備考

コンテナから項目を抽出するには conPeek 関数を使用します。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロール内の各項目の位置を返す getItemPos メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-getnextitem"></a>メソッド getNextItem

フォーム リスト コントロール内の次の項目の数を取得します。

    public int getNextItem(FormListNext nextType, [int startIdx])

#### <a name="parameters"></a>パラメーター

nextType  
次の項目の前にある項目を指定する整数データ型です。

<!-- -->

startIdx  
次の項目の前にある項目を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールでどの項目が次の品目であるかを示す整数データ型値です。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールの次の項目数を取得する getNextItem メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の品目は、フォーム リスト コントロールの一覧の管理に追加されます。

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

### <a name="method-getselectedcount"></a>メソッド getSelectedCount

フォーム リスト コントロールで選択されている項目の数を取得します。

    public int getSelectedCount()

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールで選択されている品目の数を示す整数データ型値です。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールの選択した項目数を返す getSelectedCount メソッドの呼び出しを示しています。 FormListControl.singleSelection メソッドは、複数の項目を選択するかどうかを示します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-getstringwidth"></a>メソッド getStringWidth

    public int getStringWidth(str Text)

#### <a name="parameters"></a>パラメーター

テキスト  

#### <a name="return-value"></a>戻り値

### <a name="method-gettopindex"></a>メソッド getTopIndex

    public int getTopIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-gridlines"></a>メソッド gridLines

    public boolean gridLines([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-headerdragdrop"></a>メソッド headerdragdrop

    public boolean headerdragdrop([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

<!-- -->

モード  
高さの計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します。

| モード              | 高さの計算                                                                         |
|-------------------|--------------------------------------------------------------------------------------------|
| -1 - 正確        | ピクセル単位のコントロールの正確な高さが使用されます。                                         |
| 0 - 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 - 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                               |

高さと高さ計算モードは別々に設定できます。

#### <a name="examples"></a>例

次の例は、コントロールの高さを 120 ピクセルに設定する height メソッドの呼び出しを示しています。

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

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を示す整数。オプション。 この値は、 Exact モードの場合は -1、Auto モードの場合は 0、Column height 幅の場合は 1 になります。

#### <a name="return-value"></a>戻り値

高さ計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| 正確         | ピクセル単位のコントロールの正確な高さが使用されます。                                         |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                               |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

#### <a name="examples"></a>例

次の例は、正確なピクセル値に基づいてコントロールの高さを調整する heightMode メソッドの呼び出しを示しています。

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

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数データ型です。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

#### <a name="examples"></a>例

次の例は、高さを 120 ピクセルに設定する heightValue メソッドの呼び出しを示しています。

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

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして割り当てられる値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hittest"></a>メソッド hitTest

    public container hitTest(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

#### <a name="return-value"></a>戻り値

### <a name="method-hittestsubitem"></a>メソッド hitTestSubItem

    public container hitTestSubItem(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

#### <a name="return-value"></a>戻り値

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。 次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

#### <a name="examples"></a>例

次の例は、コントロールのユーザー設定権限を決定する方法を示しています。

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

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-itemalign"></a>メソッド itemAlign

    public int itemAlign([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-itemchanging"></a>メソッド itemChanging

    public boolean itemChanging(int Idx, AnyType Data)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-keydown"></a>メソッド keyDown

    public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

vKey  

<!-- -->

Ctrl  

<!-- -->

シフト  

#### <a name="return-value"></a>戻り値

### <a name="method-leave"></a>メソッド leave

ユーザーがフォーム リスト コントロールからフォーカスを移動したら識別します。

    public boolean leave()

#### <a name="return-value"></a>戻り値

フォーカスがコントロールから移動された場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[leave] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-left"></a>メソッド left

フォーム リスト コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
位置の計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

<!-- -->

モード  
位置の計算方法を示す整数。オプション。 これは、次のいずれかの値になります。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールの水平位置をピクセル単位で示す整数。

#### <a name="examples"></a>例

次の例は、水平方向の位置を 50 ピクセルに設定する left メソッドの呼び出しを示しています。

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

### <a name="method-leftmode"></a>メソッド leftMode

フォーム リスト コントロールの水平位置を計算する方法を示す値を設定するか返します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
水平位置の計算方法を示す整数。オプション。

#### <a name="return-value"></a>戻り値

水平位置の計算方法を示す整数。 戻り値は、-1 または FormLeft 列挙値です。

#### <a name="remarks"></a>備考

value パラメーターと戻り値は、水平位置の計算方法を指定する整数値です。 この値は、正確なピクセル値の場合は -1、FormLeft 列挙値の場合は -1 のいずれかになります。 詳細については、「FormLeft 列挙」を参照してください。

#### <a name="examples"></a>例

次の例は、正確なピクセル値に基づいて、フォーム リスト コントロールの水平方向位置を計算する leftMode メソッドの呼び出しを示しています。

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

### <a name="method-leftvalue"></a>メソッド leftValue

フォーム リスト コントロールの水平位置をピクセル単位で設定するか返します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
水平位置をピクセル単位で示す整数。オプション。

#### <a name="return-value"></a>戻り値

水平位置をピクセル単位で示す整数。

#### <a name="remarks"></a>備考

正確なピクセル値に左モードが設定されていない限り、水平位置は変更されません。 詳細については、「leftMode」を参照してください。

#### <a name="examples"></a>例

次の例は、水平方向の位置を 100 ピクセルに設定する leftValue メソッドの呼び出しを示しています。

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

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがマウスの左ボタンが押すときを識別します。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[mouseUp] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-moveitem"></a>メソッド moveItem

指定した項目をフォーム リスト コントロールに移動します。

    public int moveItem(int Item, int InsertAt)

#### <a name="parameters"></a>パラメーター

項目  
品目が移動されるリスト内の位置を指定する整数データ型です。

<!-- -->

InsertAt  
品目が移動されるリスト内の位置を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

品目が移動されるリスト内の位置を指定する整数データ型です。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロールの 10 番目の位置にアイテムを移動する moveItem メソッドの呼び出しを示しています。 FormListControl.getCount メソッドは、コントロール内の項目の数を返します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前 (オプション)。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-oneclickactivate"></a>メソッド oneClickActivate

    public boolean oneClickActivate([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-redrawitems"></a>メソッド redrawItems

フォーム リスト コントロール内の広範囲の項目を更新します。

    public boolean redrawItems(int idxFirst, int idxLast)

#### <a name="parameters"></a>パラメーター

idxFirst  
範囲内の最後の項目のゼロベースのインデックスを指定する整数データ型です。

<!-- -->

idxLast  
範囲内の最後の項目のゼロベースのインデックスを指定する整数データ型です。

#### <a name="return-value"></a>戻り値

項目が更新された場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロール内の項目の範囲を更新する redrawItems メソッドの呼び出しを示しています。 FormListControl.moveItem メソッドは、指定された項目を移動します。 FormListControl.getCount メソッドは、コントロール内の項目の数を取得します。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-rowselect"></a>メソッド rowSelect

行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型値を設定または取得します。

    public boolean rowSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  
行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロール内の行が選択されている場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、行がクリックされたときにフォーム リスト コントロール内の行が選択されるように指定する、rowSelect メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。 列は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-scroll"></a>メソッド scroll

    public boolean scroll(int dx, int dy)

#### <a name="parameters"></a>パラメーター

dx  

<!-- -->

dy  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-selectionchanging"></a>メソッド selectionChanging

    public boolean selectionChanging(int Idx, AnyType Data)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-setcolumn"></a>メソッド setColumn

    public boolean setColumn(int Idx, FormListColumn Column)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

円柱  

#### <a name="return-value"></a>戻り値

### <a name="method-setcolumnwidth"></a>メソッド setColumnWidth

フォーム リスト コントロール内の列の幅を指定します。

    public boolean setColumnWidth(int Idx, int Width)

#### <a name="parameters"></a>パラメーター

Idx  
フォーム リスト コントロール内で列の幅を指定する整数データ型です。

<!-- -->

幅  
フォーム リスト コントロール内で列の幅を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

幅がセットされている場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロール内の列の幅を指定する setColumnWidth メソッドの呼び出しを示しています。 FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。

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

### <a name="method-setitem"></a>メソッド setItem

フォーム リスト コントロールに項目が含まれているかどうかを示します。

    public boolean setItem(FormListItem item)

#### <a name="parameters"></a>パラメーター

項目  
フォーム リスト コントロール内の項目の FormListItem オブジェクト。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールに項目が含まれている場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、各項目がフォーム リスト コントロールに含まれているかどうかを判断する setItem メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-setstateimagelist"></a>メソッド setStateImagelist

    public Imagelist setStateImagelist(Imagelist imageList)

#### <a name="parameters"></a>パラメーター

imageList  

#### <a name="return-value"></a>戻り値

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

ショートカット メニューがいつ表示されるかを示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
メニュー ハンドルを指定する整数データ型です。

#### <a name="return-value"></a>戻り値

メニュー ハンドルを指定する整数データ型です。

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [showContextMenu] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-showselalways"></a>メソッド showSelAlways

    public boolean showSelAlways([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-singleselection"></a>メソッド singleSelection

フォーム リスト コントロールで複数の項目を選択できるかどうかを示します。

    public boolean singleSelection([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム リスト コントロールで複数の項目を選択できるかどうかを示すブール値データ型。

#### <a name="return-value"></a>戻り値

複数の項目を選択することができない場合 true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォームのリスト コントロールにアイテムを追加する前に、singleSelection メソッドを呼び出します。 それ以外の場合は、項目はコントロールに表示されません。

#### <a name="examples"></a>例

次の例は、複数の項目を選択できるように指定するための singleSelection メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのスキップ プロパティに割り当てるブール値; オプション。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-sort"></a>メソッド sort

    public int sort([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sorttextitems"></a>メソッド sortTextItems

    public boolean sortTextItems([int column], [boolean ascending])

#### <a name="parameters"></a>パラメーター

column  

<!-- -->

ascending  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
垂直位置の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

<!-- -->

モード  
垂直位置の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールの垂直位置をピクセル単位で示す整数。

#### <a name="examples"></a>例

次の例は、垂直位置を 50 ピクセルに設定する top メソッドの呼び出しを示しています。

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

### <a name="method-topmode"></a>メソッド topMode

フォーム リスト コントロールの垂直位置を計算する方法を示す値を設定するか返します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
垂直位置の計算方法を示す整数。オプション。

#### <a name="return-value"></a>戻り値

垂直位置の計算方法を示す整数データ型値です。 戻り値は、-1 または FormTop 列挙値です。

#### <a name="remarks"></a>備考

value パラメーターと戻り値は、正確なピクセル値の場合は -1、FormTop 列挙値または -1 のいずれかの整数値です。 詳細については、「FormTop 列挙」を参照してください。

#### <a name="examples"></a>例

次の例は、正確なピクセル値に基づいて垂直位置を計算する topMode メソッドの呼び出しを示しています。

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

### <a name="method-topvalue"></a>メソッド topValue

フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
垂直位置を指定する整数。オプション。

#### <a name="return-value"></a>戻り値

フォーム リスト コントロールの垂直位置を指定する整数。

#### <a name="remarks"></a>備考

正確なピクセル値に上部モードが設定されていない限り、垂直位置は変更されません。 詳細については、「topMode」を参照してください。

#### <a name="examples"></a>例

次の例は、垂直位置を 50 ピクセルに設定する topValue メソッドの呼び出しを示しています。

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

### <a name="method-trackselect"></a>メソッド trackSelect

    public boolean trackSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-twoclickactivate"></a>メソッド twoClickActivate

    public boolean twoClickActivate([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティの値を設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定または取得し、スペースを計算する方法を指定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

<!-- -->

モード  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

#### <a name="return-value"></a>戻り値

コントロールの上と下のスペースの量を示す整数。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォーム リスト コントロールの上と下のスペースを計算する方法を示す値を設定するか返します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

#### <a name="return-value"></a>戻り値

スペースがフォント サイズなどの他のフォーム設定に基づいて自動的に調整される場合は自動です。そうでなければ、固定です。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定するか返します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上と下のスペースの量を示す整数。オプション。

#### <a name="return-value"></a>戻り値

コントロールの上と下のスペースの量を示す整数。

### <a name="method-viewtype"></a>メソッド viewType

    public int viewType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの表示設定に割り当てられる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
幅の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

<!-- -->

モード  
幅の計算方法を示す整数。オプション。 このパラメーターは、次のいずれかの値にすることができます。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード             | 幅計算                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| -1 - 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 0 - 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 - 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

幅と幅計算モードは別々に設定できます。

#### <a name="examples"></a>例

次の例は、コントロールの幅を 120 ピクセルに設定する width メソッドの呼び出しを示しています。

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

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅の計算方法を示す整数。オプション。

#### <a name="return-value"></a>戻り値

現在の幅の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

#### <a name="examples"></a>例

次の例は、正確なピクセル値に基づいて、コントロールの幅を計算する widthMode メソッドの呼び出しを示しています。

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

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅をピクセル単位で指定する整数。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

#### <a name="examples"></a>例

次の例は、コントロールの幅を 120 ピクセルに設定する widthValue メソッドの呼び出しを示しています。

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

### <a name="method-selectionchanged"></a>メソッド selectionChanged

    public void selectionChanged(int Idx, AnyType Data)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

データ  

### <a name="method-activateitem"></a>メソッド activateItem

    public void activateItem(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  

### <a name="method-inputsearch"></a>メソッド inputSearch

指定されたテキスト文字列の検索開始日を示します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
テキスト文字列を指定する文字列データ型。

#### <a name="remarks"></a>備考

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[inputSearch] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-update"></a>メソッド update

コントロールを更新します。

    public void update([int idx])

#### <a name="parameters"></a>パラメーター

idx  

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム リスト コントロールの移動を終了した日を示します。

    public void endDrag()

#### <a name="remarks"></a>備考

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[endDrag] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-setimagelist"></a>メソッド setImagelist

    public void setImagelist(Imagelist imageList, [boolean SetLarge])

#### <a name="parameters"></a>パラメーター

imageList  

<!-- -->

SetLarge  

### <a name="method-copy"></a>メソッド copy

ユーザーがコピー操作を実行するときを識別します。

    public void copy()

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [copy] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-itemcopy"></a>メソッド itemCopy

    public void itemCopy(int Idx, int newIdx)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

newIdx  

### <a name="method-cut"></a>メソッド cut

ユーザーがカット操作を実行するときを識別します。

    public void cut()

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [cut] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-itemmoved"></a>メソッド itemMoved

    public void itemMoved(int Idx, int newIdx)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

newIdx  

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-onselectionchanged"></a>メソッド OnSelectionChanged

    private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-hottrackitem"></a>メソッド hotTrackItem

ユーザーがマウス ポインターをフォーム リスト コントロール上に移動するときを識別します。

    public void hotTrackItem(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  
フォーム リスト コントロールのインデックスを指定する整数データ型です。

#### <a name="remarks"></a>備考

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[hotTrackItem] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-setcount"></a>メソッド setCount

    public void setCount(int count)

#### <a name="parameters"></a>パラメーター

カウント  

### <a name="method-dragleave"></a>メソッド dragLeave

ユーザーがフォーム リスト コントロールの境界からオブジェクトをドラッグするときを識別します。

    public void dragLeave()

#### <a name="remarks"></a>備考

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[dragLeave] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-itemdeleted"></a>メソッド itemDeleted

    public void itemDeleted(int Idx, AnyType Data)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

データ  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-settext"></a>メソッド setText

    public void setText(int Idx, str Text, [int SubItem])

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

テキスト  

<!-- -->

SubItem  

### <a name="method-itemchanged"></a>メソッド itemChanged

    public void itemChanged(int Idx, AnyType Data)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

データ  

### <a name="method-doubleclick"></a>メソッド doubleClick

ユーザーがフォーム内のリスト コントロールのアイテムをダブルクリックするときを識別します。

    public void doubleClick()

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [doubleClick] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-allitemsdeleted"></a>メソッド allItemsDeleted

フォーム リスト コントロール内のすべてのアイテムが削除される日を示します。

    public void allItemsDeleted()

#### <a name="remarks"></a>備考

フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[allItemsDeleted] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-drop"></a>メソッド drop

ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムを新しい位置にドロップするときを識別します。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="remarks"></a>備考

このメソッドは、DragDrop プロパティがコントロールの手動に設定されていて、beginDrag イベントがすでに開始されている場合にのみ呼び出されます。 イベントの詳細については、beginDrag を参照してください。 リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [drop] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-columnclicked"></a>メソッド columnClicked

ユーザーがフォーム内のリスト ビュー コントロールの列をクリックするときを識別します。

    public void columnClicked(int Column)

#### <a name="parameters"></a>パラメーター

円柱  
フォーム列を指定する整数データ型です。

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をクリックして [columnClicked] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-getstateimagelist"></a>メソッド getStateImagelist

    public void getStateImagelist()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setitempos"></a>メソッド setItemPos

フォーム リスト コントロール内の項目の位置を設定します。

    public void setItemPos(int Item, int x, int y)

#### <a name="parameters"></a>パラメーター

項目  
項目の位置の y 座標を指定する整数データ型です。

<!-- -->

x  
項目の位置の y 座標を指定する整数データ型です。

<!-- -->

y  
項目の位置の y 座標を指定する整数データ型です。

#### <a name="examples"></a>例

次の例は、フォーム リスト コントロール内の各項目の位置を指定する setItemPos メソッドの呼び出しを示しています。 while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。 変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。

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

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-context"></a>メソッド context

ユーザーがショートカット メニューをフォーム リスト コントロールで開くときを識別します。

    public void context()

#### <a name="remarks"></a>備考

リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [context] をクリックします。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-begineditlabel"></a>メソッド beginEditLabel

    public void beginEditLabel(int Idx)

#### <a name="parameters"></a>パラメーター

Idx  

### <a name="method-iteminserted"></a>メソッド itemInserted

    public void itemInserted(int Idx, AnyType Data)

#### <a name="parameters"></a>パラメーター

Idx  

<!-- -->

データ  

## <a name="class-formlistitem"></a>クラス FormListItem
    class FormListItem extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                         | 説明                                          |
|----------------------------------------------------------------|------------------------------------------------------|
| public AnyType data(\[AnyType value\])                         |                                                      |
| public int idx(\[int value\])                                  |                                                      |
| public int image(\[int value\])                                |                                                      |
| public int indent(\[int value\])                               |                                                      |
| public int overlayImage(\[int value\])                         |                                                      |
| public boolean stateChecked(\[boolean value\])                 |                                                      |
| public boolean stateCut(\[boolean value\])                     |                                                      |
| public boolean stateDropHilited(\[boolean value\])             |                                                      |
| public boolean stateFocus(\[boolean value\])                   |                                                      |
| public int stateImage(\[int value\])                           |                                                      |
| public boolean stateSelected(\[boolean value\])                |                                                      |
| public int subItem(\[int value\])                              |                                                      |
| public str text(\[str value\])                                 |                                                      |
| public str toString()                                          | 現在のオブジェクトを表す文字列を返します。 |
| public void finalize()                                         |                                                      |
| public void new(\[str Text\], \[int Image\], \[AnyType Data\]) | Object クラスの新しいインスタンスを初期化します。      |

### <a name="method-data"></a>メソッド data

    public AnyType data([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-idx"></a>メソッド idx

    public int idx([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-image"></a>メソッド image

    public int image([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-indent"></a>メソッド indent

    public int indent([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-overlayimage"></a>メソッド overlayImage

    public int overlayImage([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-statechecked"></a>メソッド stateChecked

    public boolean stateChecked([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-statecut"></a>メソッド stateCut

    public boolean stateCut([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-statedrophilited"></a>メソッド stateDropHilited

    public boolean stateDropHilited([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-statefocus"></a>メソッド stateFocus

    public boolean stateFocus([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-stateimage"></a>メソッド stateImage

    public int stateImage([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-stateselected"></a>メソッド stateSelected

    public boolean stateSelected([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-subitem"></a>メソッド subItem

    public int subItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([str Text], [int Image], [AnyType Data])

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

画像  

<!-- -->

データ  

## <a name="class-formmanagedhostcontrol"></a>クラス FormManagedHostControl
    class FormManagedHostControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public str assemblyName(\[str value\])                                                                      |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public CLRObject control()                                                                                  |                                                                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
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
| public boolean rTLCapable(\[boolean value\])                                                                |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public int sizing(\[int value\])                                                                            |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public str typeName(\[str value\])                                                                          |                                                                                                                                                                         |
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
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void enter()                                                                                         |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-assemblyname"></a>メソッド assemblyName

    public str assemblyName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるコンフィギュレーション キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-control"></a>メソッド control

    public CLRObject control()

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

FormControl.dragLeave、FormControl.dragOver、および FormControl.dragOverEx メソッドを使用して、ビヘイビアーを指定します。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を示す整数です (オプション)。

<!-- -->

モード  
高さの計算方法を示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード          | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして設定する値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

### <a name="method-leave"></a>メソッド leave

    public boolean leave()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-rtlcapable"></a>メソッド rTLCapable

    public boolean rTLCapable([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-sizing"></a>メソッド sizing

    public int sizing([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-typename"></a>メソッド typeName

    public str typeName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
幅の計算方法を示す整数です (オプション)。

<!-- -->

モード  
幅の計算方法を示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロール幅の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  
幅をピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

## <a name="class-formmenubuttoncontrol"></a>クラス FormMenuButtonControl
    class FormMenuButtonControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                              | 説明                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int acquireFocus(\[int value\])                                                                              |                                                                                                                                                                         |
| public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])            |                                                                                                                                                                         |
| public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])                     |                                                                                                                                                                         |
| public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\]) |                                                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                                      | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public int alignment(\[int value\])                                                                                 |                                                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                         | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                                      | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                                   | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public boolean autoRefreshData(\[boolean value\])                                                                   |                                                                                                                                                                         |
| public int backgroundColor(\[int value\])                                                                           | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                                 | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                                  | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public boolean big(\[boolean value\])                                                                               |                                                                                                                                                                         |
| public int bold(\[int value\])                                                                                      | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                                     |
| public int border(\[int value\])                                                                                    | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public int bottomMargin(\[int value\])                                                                              |                                                                                                                                                                         |
| public int buttonDisplay(\[int value\])                                                                             | ボタン コントロールの外観を取得または設定します。                                                                                                                      |
| public container calcControlSize(int chars, int lines)                                                              | コントロールのサイズを取得します。                                                                                                                                      |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                               |                                                                                                                                                                         |
| public boolean canContain(FormControl control)                                                                      |                                                                                                                                                                         |
| public int characterSet(\[int value\])                                                                              | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int colorScheme(\[int value\])                                                                               | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                            | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                                    | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public boolean contains(FormControl control)                                                                        |                                                                                                                                                                         |
| public int controlCount()                                                                                           |                                                                                                                                                                         |
| public FormControl controlNum(int controlNo)                                                                        |                                                                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                        | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public str dataRelationPath(\[str value\])                                                                          | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public boolean defaultButton(\[boolean value\])                                                                     | ボタンをフォームの既定のボタンにするかどうかを指定します。                                                                                                 |
| public str disabledImage(\[str value\])                                                                             | コントロールの無効な画像を取得または設定します。                                                                                                                          |
| public int disabledImageLocation(\[int value\])                                                                     |                                                                                                                                                                         |
| public int disabledResource(\[int value\])                                                                          | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                                                          |
| public int displayTarget(\[int value\])                                                                             | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                                  | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                               | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                           | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public str font(\[str value\])                                                                                      | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                                  | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public boolean forcedToOverflow(\[boolean value\])                                                                  |                                                                                                                                                                         |
| public int foregroundColor(\[int value\])                                                                           | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public boolean hasChanged(\[boolean val\])                                                                          | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                                     | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                          | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                                | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                               | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                              | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                                  | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                           | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                                   | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public int imageLocation(\[int value\])                                                                             |                                                                                                                                                                         |
| public boolean isContainer()                                                                                        |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                        | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                                       | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                            | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
| public boolean italic(\[boolean value\])                                                                            |                                                                                                                                                                         |
| public str keyTip(\[str value\])                                                                                    |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                            | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMargin(\[int value\])                                                                                |                                                                                                                                                                         |
| public int leftMode(\[int value\])                                                                                  | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                                 | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean markAsUserAdd(\[boolean value\])                                                                     | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                     | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                           | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public int moveControl(int controlId, \[int insertAfterId\])                                                        |                                                                                                                                                                         |
| public int multiSelect(\[int value\])                                                                               |                                                                                                                                                                         |
| public str name(\[str value\])                                                                                      | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                          |                                                                                                                                                                         |
| public int needsRecord(\[int value\])                                                                               |                                                                                                                                                                         |
| public str normalImage(\[str value\])                                                                               |                                                                                                                                                                         |
| public int normalResource(\[int value\])                                                                            |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                             |                                                                                                                                                                         |
| public FormControl parentControl()                                                                                  | コントロールの親コントロールを取得します。                                                                                                                           |
| public boolean primary(\[boolean value\])                                                                           |                                                                                                                                                                         |
| public int rightMargin(\[int value\])                                                                               |                                                                                                                                                                         |
| public boolean saveRecord(\[boolean value\])                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                           | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int shortkey(\[int value\])                                                                                  |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                          | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showShortCut(\[boolean value\])                                                                      |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                              | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int style(\[int value\])                                                                                     |                                                                                                                                                                         |
| public str text(\[str value\])                                                                                      |                                                                                                                                                                         |
| public str toolTip()                                                                                                | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                             | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMargin(\[int value\])                                                                                 |                                                                                                                                                                         |
| public int topMode(\[int value\])                                                                                   | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                                  | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                                      |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                         | コントロール内のテキストの下線プロパティを設定するか返します。                                                                                                     |
| public boolean SysObsoleteAttribute(container data)                                                                 |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                                  | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                              | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                             | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                               | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userHeight(\[int value\])                                                                                | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                                  | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                          | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                            | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                            | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                         | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                                  | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                                 | ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。                                                                                           |
| public boolean useUserLayout(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public boolean value(\[boolean value\])                                                                             |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                        | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                              | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                                      | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                           | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                           | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                                 | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                                | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                           | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void prefColumnSize(int width, int height)                                                                   | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void resetUserSetting()                                                                                      | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                               | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                         |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])         |                                                                                                                                                                         |
| public void arrange()                                                                                               |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                              | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void gotFocus()                                                                                              | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void clicked()                                                                                               |                                                                                                                                                                         |
| public void copy()                                                                                                  | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void setFocus()                                                                                              | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void cut()                                                                                                   | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])                                          |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                        |                                                                                                                                                                         |
| public void dragLeave()                                                                                             | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void context()                                                                                               | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void endDrag()                                                                                               | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void mouseLeave()                                                                                            | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                                       | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void lostFocus()                                                                                             | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void paste()                                                                                                 | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void displayControl()                                                                                        | コントロールを表示します。                                                                                                                                                   |

### <a name="method-acquirefocus"></a>メソッド acquireFocus

    public int acquireFocus([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-addcontrol"></a>メソッド addControl

    public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a>パラメーター

controlType  

<!-- -->

controlName  

<!-- -->

insertAfter  

#### <a name="return-value"></a>戻り値

### <a name="method-addcontrolex"></a>メソッド addControlEx

    public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a>パラメーター

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

#### <a name="return-value"></a>戻り値

### <a name="method-adddatafield"></a>メソッド addDataField

    public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSourceId  

<!-- -->

fieldId  

<!-- -->

insertAfter  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-autorefreshdata"></a>メソッド autoRefreshData

    public boolean autoRefreshData([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

<!-- -->

y  
マウス ポインターの y 座標を示す整数値。 座標はコントロールの左上隅を基準にしています。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-big"></a>メソッド big

    public boolean big([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 自動        |
| 1     | 3D          |
| 2     | 単一明細行 |
| 3     | 均一        |
| 4     | None        |

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-buttondisplay"></a>メソッド buttonDisplay

ボタン コントロールの外観を取得または設定します。

    public int buttonDisplay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 5 までの整数。

#### <a name="remarks"></a>備考

プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。 このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。 返される整数値には、次のようなボタン コントロールの外観が含まれます。

| 先頭値 | 説明                                                      |
|-------|------------------------------------------------------------------|
| 0     | テキストのみ                                                        |
| 1     | イメージのみ                                                       |
| 2     | テキストと画像。画像はテキストの下に表示されます。           |
| 3     | テキストと画像。画像はテキストの上に表示されます。           |
| 4     | テキストと画像。画像はテキストの左に表示されます。  |
| 5     | テキストと画像。画像はテキストの右に表示されます。 |

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

コントロールのサイズを取得します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
高さを決定するために使用する行数。

<!-- -->

明細行  
高さを決定するために使用する行数。

#### <a name="return-value"></a>戻り値

幅と高さを保持するコンテナー。

### <a name="method-canadddatafield"></a>メソッド canAddDataField

    public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSourceId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-cancontain"></a>メソッド canContain

    public boolean canContain(FormControl control)

#### <a name="parameters"></a>パラメーター

control  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

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

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 先頭値 | スタイル                 |
|-------|-----------------------|
| 0     | 既定               |
| 1     | Windows パレット   |
| 2     | 真の配色 |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるコンフィギュレーション キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-contains"></a>メソッド contains

    public boolean contains(FormControl control)

#### <a name="parameters"></a>パラメーター

control  

#### <a name="return-value"></a>戻り値

### <a name="method-controlcount"></a>メソッド controlCount

    public int controlCount()

#### <a name="return-value"></a>戻り値

### <a name="method-controlnum"></a>メソッド controlNum

    public FormControl controlNum(int controlNo)

#### <a name="parameters"></a>パラメーター

controlNo  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  
ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。

#### <a name="remarks"></a>備考

このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。 参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。

### <a name="method-defaultbutton"></a>メソッド defaultButton

ボタンをフォームの既定のボタンにするかどうかを指定します。

    public boolean defaultButton([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ボタンが既定のボタンである場合は true。それ以外の場合は、false。

### <a name="method-disabledimage"></a>メソッド disabledImage

コントロールの無効な画像を取得または設定します。

    public str disabledImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画像ファイルのフル ネーム。 システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。

#### <a name="remarks"></a>備考

このプロパティは、disabledResource プロパティに優先します。 これらのプロパティの両方が設定されている場合に使用されます。

### <a name="method-disabledimagelocation"></a>メソッド disabledImageLocation

    public int disabledImageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-disabledresource"></a>メソッド disabledResource

無効なボタン画像として使用する画像リソース ID を取得または設定します。

    public int disabledResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

無効なボタン画像として使用する画像リソース ID。 アイコンとビットマップ イメージの両方がサポートされます。

### <a name="method-displaytarget"></a>メソッド displayTarget

Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations、クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。

### <a name="method-dragover"></a>メソッド dragOver

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragoverex"></a>メソッド dragOverEx

マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

ドラッグ モードを示す FormDrag 列挙値。

### <a name="method-dragtext"></a>メソッド dragText

フォーム コントロールをドラッグしたときに表示されるテキストを取得します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-forcedtooverflow"></a>メソッド forcedToOverflow

    public boolean forcedToOverflow([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を示す整数です (オプション)。

<!-- -->

モード  
高さの計算方法を示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード            | 高さの計算                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| -1 正確        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード          | 高さの計算                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| 正確         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして割り当てられる値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを取得します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

### <a name="method-isrestricted"></a>メソッド isRestricted

コントロールが制限されるかどうかを示す値を取得します。

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

コントロールが制限される場合は true。それ以外の場合は false。

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  
コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。 「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

クリックされたメソッドが上書きされる場合、ユーザーは制限されているカスタマイズのみに限定されます。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-keytip"></a>メソッド keyTip

    public str keyTip([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

フォームのコントロールの水平位置を取得または設定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

フォームのコントロールの水平配置モードを設定します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの水平配置モード。

### <a name="method-leftvalue"></a>メソッド leftValue

フォームのコントロールの水平位置を取得または設定します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの水平位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの水平位置。

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

コントロールがユーザーにダブルクリックされると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。

### <a name="method-movecontrol"></a>メソッド moveControl

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterId  

#### <a name="return-value"></a>戻り値

### <a name="method-multiselect"></a>メソッド multiSelect

    public int multiSelect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-needsrecord"></a>メソッド needsRecord

    public int needsRecord([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalresource"></a>メソッド normalResource

    public int normalResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-primary"></a>メソッド primary

    public boolean primary([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-saverecord"></a>メソッド saveRecord

    public boolean saveRecord([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

### <a name="method-shortkey"></a>メソッド shortkey

    public int shortkey([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-showshortcut"></a>メソッド showShortCut

    public boolean showShortCut([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

### <a name="method-top"></a>メソッド top

フォームのコントロールの垂直位置を取得または設定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

<!-- -->

モード  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

フォームのコントロールの垂直配置モードを設定します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直配置モードを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直配置モード。

### <a name="method-topvalue"></a>メソッド topValue

フォームのコントロールの垂直位置を取得または設定します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの垂直位置を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム内のコントロールの垂直位置。

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は false。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

コントロールのユーザー データを取得または設定します。

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ。

### <a name="method-userdataitem"></a>メソッド userDataItem

コントロールのユーザー データ品目を取得または設定します。

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ アイテム。

### <a name="method-userdataitems"></a>メソッド userDataItems

コントロールのユーザー データ項目の数を取得または設定します。

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザー データ項目の数を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールのユーザー データ項目の数。

### <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

### <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのユーザーの高さ (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのカスタム ユーザーの高さ。

### <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織コンテナー (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織コンテナー。

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定する組織の兄弟 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの組織の兄弟。

### <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザーラベル テキスト。

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのユーザー セキュリティ レベル。

### <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

### <a name="method-userwidth"></a>メソッド userWidth

ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

### <a name="method-useuserlayout"></a>メソッド useUserLayout

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public boolean value([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode 値を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode 値を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング モード。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上下の間隔を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの可視化設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
幅の計算方法を示す整数です (オプション)。

<!-- -->

モード  
幅の計算方法を示す整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード           | 幅計算                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| -1 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロール幅の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード         | 幅計算                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  
幅をピクセル単位で指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-drop"></a>メソッド drop

ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-dropex"></a>メソッド dropEx

ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-arrange"></a>メソッド arrange

    public void arrange()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-clicked"></a>メソッド clicked

    public void clicked()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-onclicked"></a>メソッド OnClicked

    private void OnClicked([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

## <a name="class-formnotifyeventargs"></a>クラス FormNotifyEventArgs
    class FormNotifyEventArgs extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                  | 説明                                                  |
|-------------------------------------------------------------------------|--------------------------------------------------------------|
| public FormDataSource formDataSource(\[FormDataSource formDataSource\]) |                                                              |
| public void new()                                                       | FormNotifyEventArgs クラスの新しいインスタンスを初期化します。 |

### <a name="method-formdatasource"></a>メソッド formDataSource

    public FormDataSource formDataSource([FormDataSource formDataSource])

#### <a name="parameters"></a>パラメーター

formDataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

FormNotifyEventArgs クラスの新しいインスタンスを初期化します。

    public void new()



