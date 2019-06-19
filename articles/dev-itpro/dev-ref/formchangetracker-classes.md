---
title: F クラス (FormChangeTracker から FormControlEventArgs)
description: FormChangeTracker から FormControlEventArgs までのクラスの API 参照。
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
ms.custom: 63793
ms.assetid: 9e05d1b3-530a-4f87-a8f0-197ad35616ef
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e859dfb04a726c981416e6571ae783650b4eaa1
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595426"
---
# <a name="f-classes-formchangetracker-to-formcontroleventargs"></a>F クラス (FormChangeTracker から FormControlEventArgs)

[!include [banner](../includes/banner.md)]

FormChangeTracker から FormControlEventArgs までのクラスの API 参照。

<a name="class-formchangetracker"></a>クラス FormChangeTracker
-----------------------

    class FormChangeTracker extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明 |
|------------------------------------------------|-------------|
| public void notifyUpdate(\[str propertyName\]) |             |
| private void new()                             |             |

### <a name="method-notifyupdate"></a>メソッド notifyUpdate

    public void notifyUpdate([str propertyName])

#### <a name="parameters"></a>パラメーター

propertyName  

### <a name="method-new"></a>メソッド new

    private void new()

## <a name="class-formcheckboxcontrol"></a>クラス FormCheckBoxControl
    class FormCheckBoxControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public boolean checked(\[boolean check\])                                                                   | チェック ボックスの値を取得または設定します。                                                                                                                                  |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean drawFocusRect(\[boolean value\])                                                             |                                                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
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
| public boolean optionalRecordControl(\[boolean value\])                                                     |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
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
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public int value(\[int value\])                                                                             |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void clicked()                                                                                       |                                                                                                                                                                         |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void undo()                                                                                          |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void lookup()                                                                                        |                                                                                                                                                                         |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-checked"></a>メソッド checked

チェック ボックスの値を取得または設定します。

    public boolean checked([boolean check])

#### <a name="parameters"></a>パラメーター

小切手  
チェック ボックスが選択されているかどうかを示すブール値; オプション。 true の値は、チェック ボックスをオンにし、false の値は、オフにします。

#### <a name="return-value"></a>戻り値

チェック ボックスがオンになっている場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

このメソッドは、Win32 API を使用してプロパティを照会せずにチェック ボックスの値を取得および設定します。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                        |
|--------|-------------------------------|
| 0      | 既定。                      |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。        |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

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

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

### <a name="method-drawfocusrect"></a>メソッド drawFocusRect

    public boolean drawFocusRect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

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

<!-- -->

モード  

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

### <a name="method-optionalrecordcontrol"></a>メソッド optionalRecordControl

    public boolean optionalRecordControl([boolean value])

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
コントロールに割り当てられているセキュリティ キーの ID。オプション。

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

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

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

### <a name="method-value"></a>メソッド value

    public int value([int value])

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
コントロールの表示設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-clicked"></a>メソッド clicked

    public void clicked()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onclicked"></a>メソッド OnClicked

    private void OnClicked([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

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

## <a name="class-formcomboboxcontrol"></a>クラス FormComboBoxControl
    class FormComboBoxControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを他のコントロールと揃える必要があるかどうかを決定します。                                                                                                   |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を修正できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean appendNew(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                         |
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
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
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

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを他のコントロールと揃える必要があるかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム コンボ ボックス コントロールが他のコントロールと一致しているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに基づいて配置されます。

#### <a name="examples"></a>例

次の例は、最も長いラベルの長さに基づいて、フォーム コンボ ボックス コントロールを他のコントロールと揃えるための alignControl メソッドの呼び出しを示しています。

    boolean bAlign; 
    // The combo variable was previously assigned 
    // as a FormComboBoxControl type. 
    // Retrieve the alignControl property. 
    bAlign = combo.alignControl(); 
    // Set the alignControl property. 
    combo.alignControl(false);

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を修正できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールを変更することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

#### <a name="examples"></a>例

次の例は、allowEdit プロパティの値を返して設定する方法を示しています。

    // Return the value. 
    info (strfmt("allowEdit: %1", this.allowEdit())); 
    // Set the value. 
    this.allowEdit(false);

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-appendnew"></a>メソッド appendNew

    public boolean appendNew([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
autoDeclaration プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの背景色として割り当てる値 (オプション)。 これは、コントロールの配色または Winapi::RGB2int 値のいずれかの値にできます。

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のような RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

#### <a name="examples"></a>例

次の例は、コントロールの背景色を返して設定する方法を示しています。

    // Retrieve the existing background color. 
    info (strfmt("Background color: %1", this.backgroundColor())); 
    // Set the background color. 
    this.backgroundColor(WindowsPalette::DarkShadow3D);

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの背景スタイルとして割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

#### <a name="examples"></a>例

次の例は、背景スタイルを返して設定する方法を示しています。

    // Return the background style. 
    info (strfmt("Background style: %1", this.backStyle())); 
    // Set the background style. 
    this.backStyle(FormBackStyle::Transparent);

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

#### <a name="examples"></a>例

次の例では、ユーザーがフォーム コンボ ボックス コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。

    public int beginDrag(int _x, int _y) 
    { 
        int ret; 
        info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
        ret = super(_x, _y); 
        return ret; 
    }

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのボールド設定に割り当てる値 (オプション)。

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

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの境界スタイルとして割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

0 (ゼロ) から 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のような境界線のスタイル線が含まれます。

-   0 - 自動。
-   1 - 3D。
-   2 - 単一明細行。
-   3 - 均一。
-   4 - なし。

#### <a name="examples"></a>例

次の例は、コントロールの境界線のスタイルを取得および設定する方法を示しています。

    // Retrieve the border style. 
    info (strfmt("border: %1", this.border())); 
    // Set the border style. 
    this.border(2);

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

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

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

### <a name="method-combotype"></a>メソッド comboType

コントロールのコンボ ボックスのタイプを設定するか返します。

    public int comboType([int value])

#### <a name="parameters"></a>パラメーター

値  
コンボ ボックス コントロールのタイプとして割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのコンボ ボックスのタイプ。

#### <a name="remarks"></a>備考

次のテーブルは、コンボ ボックス タイプの値を示しています。

| 先頭値 | 説明 |
|-------|-------------|
| 0     | 標準    |
| 1     | リスト        |

#### <a name="examples"></a>例

次の例は、コントロールに使用されるコンボ ボックスのタイプを取得および設定する方法を示しています。

    // Retrieve the type of combo box control. 
    info(strfmt("comboType: %1", this.comboType())); 
    // Set the type of combo box control. 
    this.comboType(1);

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるコンフィギュレーション キーの ID。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーション キーの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

#### <a name="examples"></a>例

次の例は、コントロールのコンフィギュレーション キーの設定と取得を示しています。

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

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

リストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 さらに、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

#### <a name="examples"></a>例

次の例は、コントロールのコンフィギュレーション キー ID の取得を示しています。

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

### <a name="method-count"></a>メソッド count

コンボ ボックス コントロール内の項目の数を返します。

    public int count()

#### <a name="return-value"></a>戻り値

コンボ ボックス コントロール内の項目の数。

#### <a name="examples"></a>例

次の例は、count メソッドの使用方法を示しています。

    int j; 
    j = this.count();

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

コンボ ボックス コントロールのデータ フィールドを設定するか返します。

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  
コンボ ボックス コントロールのデータ フィールド ID として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コンボ ボックス コントロールのデータ フィールド ID の値。

#### <a name="examples"></a>例

次の例は、コンボ ボックス コントロールのデータ フィールドを設定して返す方法を示しています。

    fieldID i; 
    // The combo variable is a previously assigned  
    // FormComboBoxControl value. 
    // Retrieve the data Field. 
    i = combo.dataField(); 
    // Set the data field. 
    combo.dataField(fieldnum(CustTable, IdentificationNumber));

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

コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  
コンボ ボックス コントロールのデータ ソースとして割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

使用する必要のあるデータ ソースの ID。

#### <a name="examples"></a>例

次の例は、コンボ ボックス コントロールのデータ ソースを設定して返す方法を示しています。

    int i; 
    // The combo variable was previously assigned  
    // as a FormComboBoxControl variable. 
    // Retrieve the data source. 
    i = combo.dataSource(); 
    // Set the data source. 
    combo.dataSource(tablenum(CustTable));

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

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="examples"></a>例

次の例は、ドラッグ アンド ドロップの動作が有効かどうかを示す値を返すか、設定する方法を示しています。

    boolean bDragDrop; 
    // The combo variable was previously assigned  
    // as a FormComboBoxControl value. 
    // Retrieve the drag-and-drop-enabled value. 
    bDragDrop = combo.dragDrop(); 
    // Set the drag-and-drop-enabled value. 
    combo.dragDrop(true);

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

フォーム コンボ ボックス コントロールをドラッグしたときに表示されるテキストを返します。

    public str dragText()

#### <a name="return-value"></a>戻り値

コンボ ボックス コントロールをドラッグしたときに表示されるテキスト。コンボ ボックス コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトが有効か無効かを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。

#### <a name="examples"></a>例

次の例は、コントロールの有効なプロパティを返して設定する方法を示しています。

    // Return the value of the enabled property. 
    info(strfmt("enabled: %1",this.enabled())); 
    // Set the enabled property. 
    this.enabled(false);

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

### <a name="method-fasttabsummary"></a>メソッド fastTabSummary

    public int fastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-find"></a>メソッド find

    public int find(str string)

#### <a name="parameters"></a>パラメーター

string  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

コントロールに使用するフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  
フォーム コンボ ボックス コントロール内のテキストに使用するフォントを示す文字列データ型; オプション。

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用されるべきフォントの名前。

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロールのフォントを返して設定する方法を示しています。

    str strFont; 
    ; 
    // The ctrl variable was previously assigned  
    // as a form combo box control value. 
    // Retrieve the font. 
    strFont = ctrl.font(); 
    // Set the font. 
    ctrl.font("Times New Roman");

### <a name="method-fontsize"></a>メソッド fontSize

コントロールに使用するフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  
フォームのコンボ ボック スコントロール内のテキストのフォント サイズをポイント単位で示す整数データ型 (オプション)。

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロールのフォント サイズを返して設定する方法を示しています。

    int nSize; 
    // The ctrl variable was previously assigned  
    // as a form combo box control. 
    // Retrieve the font size. 
    nSize = ctrl.fontSize(); 
    // Set the font size. 
    ctrl.fontSize(16);

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

### <a name="method-getedittext"></a>メソッド getEditText

    public str getEditText()

#### <a name="return-value"></a>戻り値

### <a name="method-gettext"></a>メソッド getText

    public str getText(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-haschanged"></a>メソッド hasChanged

フォーム コンボ ボックス コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コンボ ボックス コントロールの hasChanged 値として割り当てる値、オプション。

#### <a name="return-value"></a>戻り値

コンボ ボックス コントロールの内容が変更された場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、コンボ ボックス コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。

    boolean bHasChanged; 
    // The ctrl variable was previously assigned 
    // as a FormComboBoxControl variable. 
    // Retrieve the hasChanged value. 
    bHasChanged = ctrl.hasChanged(); 
    // Modify the hasChanged value. 
    ctrl.hasChanged(true);

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。

### <a name="method-height"></a>メソッド height

ピクセル単位でコントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を示す整数値。オプション。

<!-- -->

モード  
高さの計算方法を示す整数値。オプション。

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

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| 正確         | ピクセル単位のコントロールの正確な高さが使用されます。                                         |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                               |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロールの高さ計算モードを返して設定する方法を示しています。

    int nHeightMode; 
    // The ctrl variable was previously assigned 
    // as a form combo box control type. 
    // Retrieve the height mode. 
    nHeightMode = ctrl.HeightMode(); 
    // Set the height mode. 
    ctrl.heightMode(-1); 
    // Set the height. 
    ctrl.heightValue(16);

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

#### <a name="examples"></a>例

次の例は、コンボ ボックス コントロールの高さの値を返して設定する方法を示しています。

    int nHeightValue; 
    // The ctrl variable was previously assigned 
    // as a form combo box control type. 
    // Retrieve the height value. 
    nHeightValue = ctrl.heightValue(); 
    // Set the height value. 
    ctrl.heightMode(-1); 
    ctrl.heightValue(22);

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを返します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

#### <a name="examples"></a>例

次の例は、helpField メソッドの使用方法を示しています。

    str strHelp; 
    strHelp = this.helpField();

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

#### <a name="examples"></a>例

次の例は、コントロールのヘルプ テキストを設定して返す方法を示しています。

    // objCtrl previously assigned to a control 
    // Retrieve existing help text. 
    print objCtrl.helpText(); 
    // Specify new help text. 
    objCtrl.helpText("My new help text");

### <a name="method-hidefirstentry"></a>メソッド hideFirstEntry

コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値を設定するか返します。

    public boolean hideFirstEntry([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値、オプション。

#### <a name="return-value"></a>戻り値

コンボ ボックス コントロール内の最初のエントリが非表示の場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンボ ボックス コントロールの最初のエントリを非表示にすることにより、必須プロパティがはいに設定されている列挙データベース フィールドの動作をエミュレートするコントロールを有効にします。

#### <a name="examples"></a>例

次の例は、コンボ ボックス コントロールの最初のエントリが非表示になっているかどうかを示す値を返して設定する方法を示しています。

    boolean bHideFirstEntry; 
    // The ctrl variable was previously assigned 
    // as a form combo box control type. 
    // Retrieve the hideFirstEntry value. 
    bHideFirstEntry = ctrl.hideFirstEntry(); 
    // Set the hideFirstEntry value. 
    bHideFirstEntry = ctrl.hideFirstEntry(true);

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

コントロールの Windows ハンドルを返します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドラーコントロールのハンドルです。

#### <a name="remarks"></a>備考

この処理は、Windows API で使用できます。

#### <a name="examples"></a>例

次の例は、コントロールの Windows ハンドルを取得する方法を示しています。

    int h; 
    h = this.hWnd(); 
    info (strfmt("hWnd: %1", h));

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナーかどうかを示す値を返します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナーである場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、コントロールがコンテナーであるかどうかを判断する方法を示しています。

    info(strfmt("IsContainer: %1", this.isContainer()));

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を返します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

#### <a name="examples"></a>例

次の例は、コントロールが可視かどうかを判断する方法を示しています。

    info(strfmt("isDisplayed: %1", this.isDisplayed()));

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

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメータで指定されたレベル以上である必要があります。

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

### <a name="method-isvalid"></a>メソッド isValid

    public boolean isValid()

#### <a name="return-value"></a>戻り値

### <a name="method-italic"></a>メソッド italic

コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのイタリック設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが斜体である場合は true。それ以外の場合は false。

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
コントロールのラベルとして割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

#### <a name="examples"></a>例

次の例は、コントロールのラベルを返して設定する方法を示しています。

    // Return the label value. 
    info(strfmt("label: %1", this.label())); 
    // Set the label value. 
    this.label("New label text goes here");

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

コントロールのラベルの太字設定を示す値を設定するか返します。

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  
ラベルのボールド設定に割り当てる値。 これは、ReportControlBold 列挙型からの値の 1 つです。

#### <a name="return-value"></a>戻り値

コントロールのラベルの太字設定を示す ReportControlBold 列挙の値。

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

フォーム コンボ ボックス コントロールのラベル テキストのフォントを設定するか返します。

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  
フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型; オプション。

#### <a name="return-value"></a>戻り値

フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型値。

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロール内のラベル テキストのフォントを返して設定する方法を示しています。

    str strLabelFont; 
    // The ctrl variable was previously assigned  
    // as a form combo box control variable. 
    // Retrieve the font. 
    strLabelFont = ctrl.labelFont(); 
    // Set the label font. 
    ctrl.labelFont("Times New Roman");

### <a name="method-labelfontsize"></a>メソッド labelFontSize

フォーム コンボ ボックス コントロールのラベル テキストのフォント サイズをポイント単位で設定するか返します。

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム コンボ ボックス コントロール内にラベル テキストのフォント サイズをポイントで示す整数データ型 (オプション)。

#### <a name="return-value"></a>戻り値

フォーム コンボ ボックス コントロール内にテキストのラベル フォント サイズをポイントで示す整数データ型値です。

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロールのラベルのフォント サイズを返して設定する方法を示しています。

    int nSize; 
    // The ctrl variable was previously assigned  
    // as a form combo box control. 
    // Retrieve the label font size. 
    nSize = ctrl.labelFontSize(); 
    // Set the label font size. 
    ctrl.labelFontSize(16);

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

コントロールのラベルのテキストが斜体で表示されるかどうかを示す値を設定するか返します。

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのラベルのイタリック設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのラベル内のテキストが斜体である場合は true。それ以外の場合は false。

### <a name="method-labelmousedblclick"></a>メソッド labelMouseDblClick

コントロールのラベルがユーザーにダブルクリックされると呼び出されます。

    public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

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

#### <a name="examples"></a>例

次の例は、Infolog に labelMouseDblClick イベントのパラメーターを表示する方法を示しています。

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

### <a name="method-labelmousedown"></a>メソッド labelMouseDown

ユーザーがコントロールのラベル上でマウス ボタンをクリックすると呼び出されます。

    public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

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

#### <a name="examples"></a>例

次の例は、Infolog に labelMouseDown イベントのパラメーターを表示する方法を示しています。

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

### <a name="method-labelmouseup"></a>メソッド labelMouseUp

ユーザーがコントロールのラベル上でマウス ボタンを放すと呼び出されます。

    public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

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

#### <a name="examples"></a>例

次の例は、Infolog に labelMouseUp イベントのパラメーターを表示する方法を示しています。

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

### <a name="method-labelposition"></a>メソッド labelPosition

コントロールのラベルの位置を設定するか返します。

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  
ラベル位置に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

ラベルの位置を表す整数。

#### <a name="remarks"></a>備考

値パラメーターが 0 (ゼロ) に設定されている場合、ラベルは、コントロールの左側に配置されます。 値パラメーターが 1 に設定されている場合、ラベルはコントロールの上に配置されます。 0 (ゼロ) の戻り値は、ラベルがコントロールの左側に置かれていることを示します。 1 の戻り値は、ラベルがコントロールの上に置かれていることを示します。

#### <a name="examples"></a>例

次の例は、ラベルの位置を返して設定する方法を示しています。

    // Retrieve the label position. 
    info (strfmt("label: %1", this.labelPosition())); 
    // Set the label position. 
    this.labelPosition(1);  // 1 == Above, 0 == Left

### <a name="method-labelunderline"></a>メソッド labelUnderline

コントロールのラベルのテキストが下線付きで表示されるかどうかを示す値を設定するか返します。

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのラベルの下線設定に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのラベル内のテキストが下線付きである場合は true。それ以外の場合は false。

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

#### <a name="examples"></a>例

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseDblClick イベントのパラメーターを表示する方法を示しています。

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

#### <a name="examples"></a>例

次の例は、Infolog に mouseDown イベントのパラメーターを表示する方法を示しています。

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

#### <a name="examples"></a>例

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseMove イベントのパラメーターを表示する方法を示しています。

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

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがコントロール上でマウス ボタンを放すと呼び出されます。

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

#### <a name="examples"></a>例

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseUp イベントのパラメーターを表示する方法を示しています。

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

#### <a name="examples"></a>例

次の例は、コントロールのセキュリティ キー IDの取得と割り当てを示しています。

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

### <a name="method-selection"></a>メソッド selection

    public int selection([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-selectionchange"></a>メソッド selectionChange

ユーザーがコンボ ボックス コントロールで選択した項目を変更したことを示します。

    public int selectionChange()

#### <a name="return-value"></a>戻り値

イベントが正常に処理された場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、ユーザーがコンボ ボックス コントロールで選択した項目を変更するときに、Infolog メッセージを表示するために selectionChange メソッドを上書きする方法を示しています。

    public int selectionChange() 
    { 
        int ret; 
        info("The selection has changed."); 
        ret = super(); 
        return ret; 
    }

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

コントロールのラベルがフォームに表示されるかどうかを示す値を設定するか返します。

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの showLabel プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

ラベルを表示する必要がある場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、コントロールの showLabel プロパティを返して設定する方法を示しています。

    // Return the showLabel value. 
    info(strfmt("showLabel: %1", this.showLabel())); 
    // Set the showLabel value. 
    this.showLabel(false);

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-sort"></a>メソッド sort

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

コントロールのテキストを設定するか返します。

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのテキストとして割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールのテキスト。コントロールにテキストが割り当てられていない場合は空の文字列。

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツールヒント テキストを返します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

#### <a name="examples"></a>例

次の例は、toolTip メソッドを上書きする方法を示しています。

    str toolTip() 
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

フォーム コンボ ボックス コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがユーザーから非表示になっているどうかを示す値、オプション。

#### <a name="return-value"></a>戻り値

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コンボ ボックス コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コンボ ボックス コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 userHide メソッドを使用すると、プログラムによって値を決定して設定できます。

#### <a name="examples"></a>例

次の例は、コンボ ボックス コントロールがユーザーから隠されているかどうかを示す値を返して設定する方法を示しています。

    int nUserHide; 
    // The ctrl variable was previously assigned  
    // as a form combo box control variable. 
    // Retrieve the userHide value. 
    nUserHide = ctrl.userHide(); 
    // Set the userHide value. 
    ctrl.userHide(1);

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

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コンボ ボックス コントロールがスキップされるかどうかを示す値を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。

#### <a name="return-value"></a>戻り値

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

#### <a name="examples"></a>例

次の例は、userSkip プロパティを返して設定する方法を示しています。

    int nUserSkip 
    // The ctrl variable was previously assigned as a 
    // FormComboBoxControl variable. 
    // Return the userSkip property. 
    nUserSkip = ctrl.userSkip(); 
    // Set the userSkip property. 
    ctrl.userSkip(1);

### <a name="method-userwidth"></a>メソッド userWidth

ピクセル単位でフォーム コンボ ボックス コントロールの幅を設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロールのユーザーの幅を返して設定する方法を示しています。

    int nWidth; 
    // The ctrl variable was previously defined  
    // as the FormComboBoxControl variable. 
    // Return the width. 
    nWidth = ctrl.userWidth(); 
    // Specify the width. 
    ctrl.userWidth(90);  // 15 characters * 6 pixels == 90

### <a name="method-validate"></a>メソッド validate

    public boolean validate()

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォームのコントロールの垂直スペーシング。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォームのコントロールの垂直スペーシング モードを設定します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
コントロールの AutoMode 列挙値; オプション。

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
幅の計算方法を示す整数値。オプション。

<!-- -->

モード  
幅の計算方法を示す整数値。オプション。

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

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロール幅の計算方法を示す整数値。 値は、Exact モードの場合は -1、Auto モードの場合は 0、Column width モードの場合は 1 になります。

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算。                                                                        |
|--------------|-------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロールの幅の計算モードを返す方法と設定する方法を示しています。

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

#### <a name="examples"></a>例

次の例は、フォーム コンボ ボックス コントロールの幅の値を返して設定する方法を示しています。

    int nWidthValue; 
    // The ctrl variable was previously assigned 
    // as a form combo box control variable. 
    // Retrieve the width value. 
    nWidthValue = ctrl.widthValue(); 
    // Set the width value. 
    ctrl.widthMode(-1); 
    ctrl.widthValue(160);

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-beginupdate"></a>メソッド beginUpdate

    public void beginUpdate()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setedittext"></a>メソッド setEditText

    public void setEditText(str string)

#### <a name="parameters"></a>パラメーター

string  

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-paste"></a>メソッド paste

フォーム コンボ ボックス コントロールをフォームに貼り付けます。

    public void paste()

### <a name="method-clear"></a>メソッド clear

コンボ ボックス リストのエントリをクリアします。

    public void clear()

#### <a name="examples"></a>例

次の例は、コンボ ボックス リスト内のエントリをクリアする方法を示しています。

    this.clear();

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

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

### <a name="method-copy"></a>メソッド copy

フォームのコンボ ボックス コントロールをコピーします。

    public void copy()

### <a name="method-onselectionchanging"></a>メソッド OnSelectionChanging

    private void OnSelectionChanging([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

#### <a name="examples"></a>例

次の例では、ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。

    public void endDrag() 
    { 
        info("EndDrag completed"); 
        super(); 
    }

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-insert"></a>メソッド insert

指定した位置にあるコンボ ボックスに文字列の値を挿入します。

    public void insert(str string, int index)

#### <a name="parameters"></a>パラメーター

string  
後に続く文字列を挿入する位置。 文字列をリストの最初の項目にする場合は、値を 0 (ゼロ) に設定します。

<!-- -->

指数  
後に続く文字列を挿入する位置。 文字列をリストの最初の項目にする場合は、値を 0 (ゼロ) に設定します。

#### <a name="examples"></a>例

次の例は、コンボ ボックス リストに文字列を挿入する方法を示しています。

    this.insert("willow", 3);

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。

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

#### <a name="examples"></a>例

次の例は、Infolog に mouseEnter イベントのパラメーターを表示する方法を示しています。

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

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-delete"></a>メソッド delete

コンボ ボックスのリストから文字列値を削除します。

    public void delete(str string)

#### <a name="parameters"></a>パラメーター

string  
コンボ ボックスのリストから削除する文字列値。

#### <a name="examples"></a>例

次の例は、コンボ ボックス リストから文字列値を削除する方法を示しています。

    this.delete("Model 12357");

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-add"></a>メソッド add

コンボ ボックス リストに文字列値を追加します。

    public void add(str string)

#### <a name="parameters"></a>パラメーター

string  
コンボ ボックスのリストに追加する文字列値。

#### <a name="remarks"></a>備考

文字列はリストの末尾に追加されます。 文字列を一覧の特定の位置に格納するには、insert メソッドを使用します。

#### <a name="examples"></a>例

次の例は、コンボ ボックス リストに文字列を追加する方法を示しています。

    this.add("maple"); 
    this.add("oak"); 
    this.add("pine");

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コンボ ボックス コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

#### <a name="examples"></a>例

次の例は、コンボ ボックス コントロールの優先幅と高さを設定する方法を示しています。

    // The nWidth and nHeight variables were  
    // previously assigned as int variables. 
    // The ctrl variable was previously assigned 
    // as a FormComboBoxControl variable. 
    ctrl.prefColumnSize( nWidth, nHeight);

### <a name="method-onvalidating"></a>メソッド OnValidating

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-onselectionchanged"></a>メソッド OnSelectionChanged

    private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-endupdate"></a>メソッド endUpdate

    public void endUpdate()

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

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

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setdropsize"></a>メソッド setDropSize

    public void setDropSize([int lines])

#### <a name="parameters"></a>パラメーター

明細行  

## <a name="class-formcommandbuttoncontrol"></a>クラス FormCommandButtonControl
    class FormCommandButtonControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public boolean autoRefreshData(\[boolean value\])                                                           |                                                                                                                                                                         |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public boolean big(\[boolean value\])                                                                       |                                                                                                                                                                         |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                                     |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public int buttonDisplay(\[int value\])                                                                     | ボタン コントロールの外観を取得または設定します。                                                                                                                      |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                                                 |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public int command(\[int value\])                                                                           |                                                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public boolean defaultButton(\[boolean value\])                                                             | ボタンをフォームの既定のボタンにするかどうかを指定します。                                                                                                 |
| public str disabledImage(\[str value\])                                                                     | コントロールの無効な画像を取得または設定します。                                                                                                                          |
| public int disabledImageLocation(\[int value\])                                                             |                                                                                                                                                                         |
| public int disabledResource(\[int value\])                                                                  | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                                                          |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public boolean forcedToOverflow(\[boolean value\])                                                          |                                                                                                                                                                         |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public int imageLocation(\[int value\])                                                                     |                                                                                                                                                                         |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                             | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                 | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                   | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public int multiSelect(\[int value\])                                                                       |                                                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                                                         |
| public int needsRecord(\[int value\])                                                                       |                                                                                                                                                                         |
| public str normalImage(\[str value\])                                                                       |                                                                                                                                                                         |
| public int normalResource(\[int value\])                                                                    |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public str parameters(\[str value\])                                                                        |                                                                                                                                                                         |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public boolean primary(\[boolean value\])                                                                   |                                                                                                                                                                         |
| public boolean saveRecord(\[boolean value\])                                                                |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int shortkey(\[int value\])                                                                          |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showShortCut(\[boolean value\])                                                              |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                                                         |
| public int toggleButton(\[int value\])                                                                      |                                                                                                                                                                         |
| public int toggleValue(\[int value\])                                                                       |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
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
| public boolean value(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void clicked()                                                                                       |                                                                                                                                                                         |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |

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
指定されている場合、プロパティはこの値に設定されます。

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

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-buttondisplay"></a>メソッド buttonDisplay

ボタン コントロールの外観を取得または設定します。

    public int buttonDisplay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 5 までの整数。

#### <a name="remarks"></a>備考

プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。 このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。 返される整数値には、次のようなボタン コントロールの外観が含まれます。

| 値です。 | 説明。                                                     |
|--------|------------------------------------------------------------------|
| 0      | テキストのみ。                                                       |
| 1      | イメージのみ。                                                      |
| 2      | テキストと画像。画像はテキストの下に表示されます。           |
| 3      | テキストと画像。画像はテキストの上に表示されます。           |
| 4      | テキストと画像。画像はテキストの左に表示されます。  |
| 5      | テキストと画像。画像はテキストの右に表示されます。 |

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

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

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

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windowsパレット。 |
| 2      | 真の配色。         |

### <a name="method-command"></a>メソッド command

    public int command([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です (オプション)。

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
コントロールが有効かどうかを指定するブール値; オプション。

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
高さの計算方法を示す整数データ型です。オプションです。

<!-- -->

モード  
高さの計算方法を示す整数データ型です。オプションです。

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
コントロールの高さの計算方法を示す整数データ型値です (オプション)。

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
高さをピクセル単位で指定する整数データ型です (オプション)。

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
コントロールのヘルプ テキストとして割り当てる値。

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

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| FormAllowUserSetup::No 0         | コントロールに対する変更は加えられません。 この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。 |
| FormAllowUserSetup::Restricted 1 | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーがコントロールを移動できません。   |
| FormAllowUserSetup::Yes 2        | ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。 ユーザーはコントロールを移動することもできます。 |

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

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

### <a name="method-parameters"></a>メソッド parameters

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

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

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

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

### <a name="method-togglebutton"></a>メソッド toggleButton

    public int toggleButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-togglevalue"></a>メソッド toggleValue

    public int toggleValue([int value])

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
コントロールの AutoMode を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode を示す整数値。オプション。

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
幅の計算方法を示す整数データ型です。オプションです。

<!-- -->

モード  
幅の計算方法を示す整数データ型です。オプションです。

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
コントロールの幅の計算方法を示す整数データ型値です (オプション)。

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
幅をピクセル単位で指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-onclicked"></a>メソッド OnClicked

    private void OnClicked([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

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

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

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

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-clicked"></a>メソッド clicked

    public void clicked()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

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

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

## <a name="class-formcontainer"></a>クラス FormContainer
    class FormContainer extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法             | 説明 |
|--------------------|-------------|
| private void new() |             |

### <a name="method-new"></a>メソッド new

    private void new()

## <a name="class-formcontainercontrol"></a>クラス FormContainerControl
    class FormContainerControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                              | 説明 |
|---------------------------------------------------------------------------------------------------------------------|-------------|
| public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])            |             |
| public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])                     |             |
| public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\]) |             |
| public boolean alignChild(\[boolean value\])                                                                        |             |
| public boolean alignChildren(\[boolean value\])                                                                     |             |
| public boolean alignControl(\[boolean value\])                                                                      |             |
| public boolean allowEdit(\[boolean value\])                                                                         |             |
| public boolean allowSysSetup()                                                                                      |             |
| public int allowUserSetup(\[int value\])                                                                            |             |
| public int arrangeGuide(\[int value\])                                                                              |             |
| public int arrangeMethod(\[int value\])                                                                             |             |
| public int arrangeWhen(\[int value\])                                                                               |             |
| public boolean autoDataGroup(\[boolean value\])                                                                     |             |
| public boolean autoDeclaration(\[boolean value\])                                                                   |             |
| public int beginDrag(int x, int y)                                                                                  |             |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                           |             |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                                 |             |
| public int bottomMarginValue(\[int value\])                                                                         |             |
| public container calcControlSize(int chars, int lines)                                                              |             |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                               |             |
| public boolean canContain(FormControl control)                                                                      |             |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                             |             |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                                |             |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                            |             |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                                  |             |
| public int columnspaceValue(\[int value\])                                                                          |             |
| public int columnsValue(\[int value\])                                                                              |             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                            |             |
| public List configurationKeyEx()                                                                                    |             |
| public boolean contains(FormControl control)                                                                        |             |
| public int controlCount()                                                                                           |             |
| public FormControl controlNum(int controlNo)                                                                        |             |
| public str countryRegionCodes(\[str value\])                                                                        |             |
| public str dataRelationPath(\[str value\])                                                                          |             |
| public int displayTarget(\[int value\])                                                                             |             |
| public int dragDrop(\[int value\])                                                                                  |             |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                                   |             |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                                       |             |
| public str dragText()                                                                                               |             |
| public boolean enabled(\[boolean value\])                                                                           |             |
| public boolean hasChanged(\[boolean val\])                                                                          |             |
| public boolean hasUserSetting()                                                                                     |             |
| public int height(int value, \[int mode\])                                                                          |             |
| public int heightMode(\[int value\])                                                                                |             |
| public int heightValue(\[int value\])                                                                               |             |
| public str helpField()                                                                                              |             |
| public str helpText(\[str value\])                                                                                  |             |
| public boolean hideIfEmpty(\[boolean value\])                                                                       |             |
| public str hierarchyParent(\[str value\])                                                                           |             |
| public int hWnd()                                                                                                   |             |
| public boolean isContainer()                                                                                        |             |
| public boolean isDisplayed()                                                                                        |             |
| public boolean isRestricted()                                                                                       |             |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                            |             |
| public boolean isVisible()                                                                                          |             |
| public boolean isVisibleOnClient()                                                                                  |             |
| public int left(int value, \[int mode\])                                                                            |             |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                             |             |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                                   |             |
| public int leftMarginValue(\[int value\])                                                                           |             |
| public int leftMode(\[int value\])                                                                                  |             |
| public int leftValue(\[int value\])                                                                                 |             |
| public boolean markAsUserAdd(\[boolean value\])                                                                     |             |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                     |             |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                         |             |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                         |             |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                           |             |
| public int moveControl(int controlId, \[int insertAfterId\])                                                        |             |
| public str name(\[str value\])                                                                                      |             |
| public int neededPermission(\[int value\])                                                                          |             |
| public container SysObsoleteAttribute()                                                                             |             |
| public FormControl parentControl()                                                                                  |             |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                            |             |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                                  |             |
| public int rightMarginValue(\[int value\])                                                                          |             |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                           |             |
| public int showContextMenu(int menuHandle)                                                                          |             |
| public boolean skip(\[boolean value\])                                                                              |             |
| public str toolTip()                                                                                                |             |
| public int top(int value, \[int mode\])                                                                             |             |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                              |             |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                                    |             |
| public int topMarginValue(\[int value\])                                                                            |             |
| public int topMode(\[int value\])                                                                                   |             |
| public int topValue(\[int value\])                                                                                  |             |
| public int type(\[int value\])                                                                                      |             |
| public boolean SysObsoleteAttribute(container data)                                                                 |             |
| public int userData(\[int value\])                                                                                  |             |
| public int userDataItem(\[int value\])                                                                              |             |
| public int userDataItems(\[int value\])                                                                             |             |
| public int userDisable(\[int value\])                                                                               |             |
| public int userHeight(\[int value\])                                                                                |             |
| public int userHide(\[int value\])                                                                                  |             |
| public int userOrgContainer(\[int value\])                                                                          |             |
| public int userOrgSibling(\[int value\])                                                                            |             |
| public str userPromptText(\[str value\])                                                                            |             |
| public int userSecurityLevel(\[int value\])                                                                         |             |
| public int userSkip(\[int value\])                                                                                  |             |
| public int userWidth(\[int value\])                                                                                 |             |
| public boolean useUserLayout(\[boolean value\])                                                                     |             |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                        |             |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                              |             |
| public int verticalSpacingValue(\[int value\])                                                                      |             |
| public boolean visible(\[boolean value\])                                                                           |             |
| public int width(int value, \[int mode\])                                                                           |             |
| public int widthMode(\[int value\])                                                                                 |             |
| public int widthValue(\[int value\])                                                                                |             |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                               |             |
| public void inputSearch(str searchStr)                                                                              |             |
| public void prefColumnSize(int width, int height)                                                                   |             |
| public void gotFocus()                                                                                              |             |
| public void lostFocus()                                                                                             |             |
| public void mouseLeave()                                                                                            |             |
| public void setFocus()                                                                                              |             |
| public void copy()                                                                                                  |             |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                         |             |
| public void displayControl()                                                                                        |             |
| public void paste()                                                                                                 |             |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                           |             |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                        |             |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                                       |             |
| public void resetUserSetting()                                                                                      |             |
| public void endDrag()                                                                                               |             |
| public void arrange()                                                                                               |             |
| public void dragLeave()                                                                                             |             |
| public void cut()                                                                                                   |             |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])         |             |
| public void context()                                                                                               |             |

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

### <a name="method-alignchild"></a>メソッド alignChild

    public boolean alignChild([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-alignchildren"></a>メソッド alignChildren

    public boolean alignChildren([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

### <a name="method-allowusersetup"></a>メソッド allowUserSetup

    public int allowUserSetup([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangeguide"></a>メソッド arrangeGuide

    public int arrangeGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangemethod"></a>メソッド arrangeMethod

    public int arrangeMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangewhen"></a>メソッド arrangeWhen

    public int arrangeWhen([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodatagroup"></a>メソッド autoDataGroup

    public boolean autoDataGroup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-begindrag"></a>メソッド beginDrag

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

    public int bottomMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  

<!-- -->

明細行  

#### <a name="return-value"></a>戻り値

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

### <a name="method-columns"></a>メソッド columns

    public int columns([int value], [ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnsmode"></a>メソッド columnsMode

    public ColumnsMode columnsMode([ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspace"></a>メソッド columnspace

    public int columnspace([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspacemode"></a>メソッド columnspaceMode

    public AutoMode columnspaceMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspacevalue"></a>メソッド columnspaceValue

    public int columnspaceValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-columnsvalue"></a>メソッド columnsValue

    public int columnsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

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

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragover"></a>メソッド dragOver

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

#### <a name="return-value"></a>戻り値

### <a name="method-dragoverex"></a>メソッド dragOverEx

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

#### <a name="return-value"></a>戻り値

### <a name="method-dragtext"></a>メソッド dragText

    public str dragText()

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-haschanged"></a>メソッド hasChanged

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  

#### <a name="return-value"></a>戻り値

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-heightmode"></a>メソッド heightMode

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-heightvalue"></a>メソッド heightValue

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helpfield"></a>メソッド helpField

    public str helpField()

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hwnd"></a>メソッド hWnd

    public int hWnd()

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayed"></a>メソッド isDisplayed

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

### <a name="method-isrestricted"></a>メソッド isRestricted

    public boolean isRestricted()

#### <a name="return-value"></a>戻り値

### <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a>パラメーター

neededSetupRights  

#### <a name="return-value"></a>戻り値

### <a name="method-isvisible"></a>メソッド isVisible

    public boolean isVisible()

#### <a name="return-value"></a>戻り値

### <a name="method-isvisibleonclient"></a>メソッド isVisibleOnClient

    public boolean isVisibleOnClient()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginmode"></a>メソッド leftMarginMode

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

    public int leftMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mousedblclick"></a>メソッド mouseDblClick

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

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

### <a name="method-mousedown"></a>メソッド mouseDown

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

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

### <a name="method-mousemove"></a>メソッド mouseMove

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

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

### <a name="method-mouseup"></a>メソッド mouseUp

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

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

### <a name="method-movecontrol"></a>メソッド moveControl

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterId  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginmode"></a>メソッド rightMarginMode

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

    public int rightMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

    public str toolTip()

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginmode"></a>メソッド topMarginMode

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginvalue"></a>メソッド topMarginValue

    public int topMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdisable"></a>メソッド userDisable

    public int userDisable([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userheight"></a>メソッド userHeight

    public int userHeight([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userhide"></a>メソッド userHide

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userorgcontainer"></a>メソッド userOrgContainer

    public int userOrgContainer([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userorgsibling"></a>メソッド userOrgSibling

    public int userOrgSibling([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userprompttext"></a>メソッド userPromptText

    public str userPromptText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

    public int userSecurityLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userskip"></a>メソッド userSkip

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userwidth"></a>メソッド userWidth

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-useuserlayout"></a>メソッド useUserLayout

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-widthmode"></a>メソッド widthMode

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-widthvalue"></a>メソッド widthValue

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dropex"></a>メソッド dropEx

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

### <a name="method-inputsearch"></a>メソッド inputSearch

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  

<!-- -->

height  

### <a name="method-gotfocus"></a>メソッド gotFocus

    public void gotFocus()

### <a name="method-lostfocus"></a>メソッド lostFocus

    public void lostFocus()

### <a name="method-mouseleave"></a>メソッド mouseLeave

    public void mouseLeave()

### <a name="method-setfocus"></a>メソッド setFocus

    public void setFocus()

### <a name="method-copy"></a>メソッド copy

    public void copy()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-displaycontrol"></a>メソッド displayControl

    public void displayControl()

### <a name="method-paste"></a>メソッド paste

    public void paste()

### <a name="method-drop"></a>メソッド drop

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-mouseenter"></a>メソッド mouseEnter

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

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

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

    public void resetUserSetting()

### <a name="method-enddrag"></a>メソッド endDrag

    public void endDrag()

### <a name="method-arrange"></a>メソッド arrange

    public void arrange()

### <a name="method-dragleave"></a>メソッド dragLeave

    public void dragLeave()

### <a name="method-cut"></a>メソッド cut

    public void cut()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-context"></a>メソッド context

    public void context()

## <a name="class-formcontrol"></a>クラス FormControl
    class FormControl extends Object

FormControl クラスは、すべてのフォーム コントロールの基本クラスとして機能します。

### <a name="remarks"></a>備考

このクラスのインスタンスは作成しないでください。 代わりに特定のコントロールを使用します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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
| public int displayTarget(\[int value\])                                                                                                                | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
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

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを揃える必要があるかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに基づいて配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を修正できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
allowEdit プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールを変更することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

#### <a name="examples"></a>例

次の例は、allowEdit プロパティの値を返して設定する方法を示しています。

    // Return the value. 
    info (strfmt("allowEdit: %1", this.allowEdit())); 
    // Set the value. 
    this.allowEdit(false);

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
値が指定されている場合は、プロパティを設定する値。

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

#### <a name="examples"></a>例

次の例では、ユーザーがフォーム コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。

    public int beginDrag(int _x, int _y) 
    { 
        int ret; 
        info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
        ret = super(_x, _y); 
        return ret; 
    }

### <a name="method-build"></a>メソッド build

    public FormBuildControl build()

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

### <a name="method-changetracker"></a>メソッド changeTracker

    public FormChangeTracker changeTracker()

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるコンフィギュレーション キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーション キーの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

#### <a name="examples"></a>例

次の例は、コントロールのコンフィギュレーション キーを設定して取得する方法を示しています。

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

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。

#### <a name="remarks"></a>備考

返されるリストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。

#### <a name="examples"></a>例

次の例は、コントロールのコンフィギュレーション キー ID を取得する方法を示しています。

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

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する国/地域コードを含む文字列 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの国/地域コードのコンマ区切りのリスト。

### <a name="method-currentrow"></a>メソッド currentRow

    public int currentRow()

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

### <a name="method-datasourceobject"></a>メソッド dataSourceObject

    public FormDataSource dataSourceObject()

#### <a name="return-value"></a>戻り値

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
ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="examples"></a>例

次の例は、ドラッグ アンド ドロップの動作が有効かどうかを示す値を返すか、設定する方法を示しています。

    boolean dDragDrop; 
    // The ctrl variable was previously assigned  
    // as a FormControl value. 
    // Retrieve the drag-and-drop-enabled value. 
    dDragDrop = ctrl.dragDrop(); 
    // Set the drag–and–drop-enabled value. 
    ctrl.dragDrop(true);

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

### <a name="method-editautopostback"></a>メソッド editAutoPostback

    public boolean editAutoPostback([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトが有効か無効かを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。

#### <a name="examples"></a>例

次の例は、コントロールの有効なプロパティを返して設定する方法を示しています。

    // Return the value of the enabled property. 
    info(strfmt("enabled: %1",this.enabled())); 
    // Set the enabled property. 
    this.enabled(false);

### <a name="method-extendedstyle"></a>メソッド extendedStyle

    public str extendedStyle([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fieldbinding"></a>メソッド fieldBinding

FieldBinding 派生クラスへのコントロールのテーブルおよびフィールド バインディングを取得します。

    public FieldBinding fieldBinding()

#### <a name="return-value"></a>戻り値

コントロールのテーブルおよびフィールド バインディングを含む FieldBinding 派生クラス。

### <a name="method-formatstr"></a>メソッド formatStr

    public str formatStr([int rowNumber], [boolean display], [int maxWidth], [boolean forceSignWhenDisplaceNegative], [boolean formatForExport])

#### <a name="parameters"></a>パラメーター

rowNumber  

<!-- -->

表示  

<!-- -->

maxWidth  

<!-- -->

forceSignWhenDisplaceNegative  

<!-- -->

formatForExport  

#### <a name="return-value"></a>戻り値

### <a name="method-formrun"></a>メソッド formRun

    public xFormRun formRun()

#### <a name="return-value"></a>戻り値

### <a name="method-getbinding"></a>メソッド getBinding

    public FormBinding getBinding(str propertyName)

#### <a name="parameters"></a>パラメーター

propertyName  

#### <a name="return-value"></a>戻り値

### <a name="method-haschanged"></a>メソッド hasChanged

コントロールの内容が変更されたかどうかを示す値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
コントロールの hasChanged 値として割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの内容が変更された場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。

    boolean bHasChanged; 
    // The ctrl variable was previously assigned 
    // as a FormControl value. 
    // Retrieve the hasChanged value. 
    bHasChanged = ctrl.hasChanged(); 
    // Modify the hasChanged value. 
    ctrl.hasChanged(true);

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
高さの計算方法を示す整数値。オプション。

<!-- -->

モード  
高さの計算方法を示す整数値。オプション。

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

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの高さの計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します。

| モード          | 高さの計算                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| 正確         | ピクセル単位のコントロールの正確な高さが使用されます。                                         |
| 自動          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                               |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

#### <a name="examples"></a>例

次の例は、フォーム コントロールの高さ計算モードを返して設定する方法を示しています。

    int nHeightMode; 
    // The ctrl variable was previously assigned 
    // as a form control variable. 
    // Retrieve the height mode. 
    nHeightMode = ctrl.HeightMode(); 
    // Set the height mode. 
    ctrl.heightMode(-1); 
    // Set the height. 
    ctrl.heightValue(16);

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  
高さをピクセル単位で指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

#### <a name="examples"></a>例

次の例は、フォーム コントロールの高さの値を返して設定する方法を示しています。

    int nHeightValue; 
    // The ctrl variable was previously assigned 
    // as a form control variable. 
    // Retrieve the height value. 
    nHeightValue = ctrl.heightValue(); 
    // Set the height value. 
    ctrl.heightMode(-1); 
    ctrl.heightValue(22);

### <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを取得します。

    public str helpField()

#### <a name="return-value"></a>戻り値

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

helpField メソッドを使用してヘルプテキストの値を設定することはできません。 ヘルプ テキストの値を設定するには、helpText メソッドを使用します。

#### <a name="examples"></a>例

次の例は、helpField メソッドの使用方法を示しています。

    str strHelp; 
    strHelp = this.helpField();

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールのヘルプ テキストとして割り当てる値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

#### <a name="examples"></a>例

次の例は、コントロールのヘルプ テキストを設定して返す方法を示しています。

    // objCtrl previously assigned to a control 
    // Retrieve existing help text. 
    print objCtrl.helpText(); 
    // Specify new help text. 
    objCtrl.helpText("My new help text");

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

#### <a name="examples"></a>例

次の例は、コントロールの Windows ハンドルを取得する方法を示しています。

    int h; 
    h = this.hWnd(); 
    info (strfmt("hWnd: %1", h));

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-isdisplayed"></a>メソッド isDisplayed

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

コントロールが表示される場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。

#### <a name="examples"></a>例

次の例は、コントロールが可視かどうかを判断する方法を示しています。

    info(strfmt("isDisplayed: %1", this.isDisplayed()));

### <a name="method-iseditable"></a>メソッド isEditable

    public boolean isEditable()

#### <a name="return-value"></a>戻り値

### <a name="method-isenabled"></a>メソッド isEnabled

    public boolean isEnabled()

#### <a name="return-value"></a>戻り値

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

### <a name="method-isvisible"></a>メソッド isVisible

コントロールが表示されるかどうかを示す値を取得します。

    public boolean isVisible()

#### <a name="return-value"></a>戻り値

コントロールが可視である場合は true。それ以外の場合は false。

### <a name="method-isvisibleonclient"></a>メソッド isVisibleOnClient

    public boolean isVisibleOnClient()

#### <a name="return-value"></a>戻り値

### <a name="method-labeltext"></a>メソッド labelText

コントロールのラベル テキストを取得します。

    public str labelText()

#### <a name="return-value"></a>戻り値

コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。

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

### <a name="method-lockwindowupdate"></a>メソッド lockWindowUpdate

更新のコントロールのウィンドウをロックまたはロック解除します。

    public boolean lockWindowUpdate(boolean lock)

#### <a name="parameters"></a>パラメーター

lock  
ブール値: ウィンドウをロックする場合は true、ウィンドウをロック解除するには false。

#### <a name="return-value"></a>戻り値

操作が成功した場合は true。それ以外の場合は、false。

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

#### <a name="examples"></a>例

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseDblClick イベントのパラメーターを表示する方法を示しています。

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

#### <a name="examples"></a>例

次の例は、Infolog に mouseDown イベントのパラメーターを表示する方法を示しています。

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

#### <a name="examples"></a>例

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 次の例は、Infolog に mouseMove イベントのパラメーターを表示する方法を示しています。

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

#### <a name="examples"></a>例

次の例は、Infolog に mouseUp イベントのパラメーターを表示する方法を示しています。

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

### <a name="method-resourcebundlename"></a>メソッド resourceBundleName

    public str resourceBundleName()

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

コントロールのセキュリティ キーの ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てるセキュリティ キーの ID。オプション。

#### <a name="return-value"></a>戻り値

コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例では、コントロールのセキュリティ キー IDを取得して割り当てる方法を示しています。

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

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
表示するメニューの ID。

#### <a name="return-value"></a>戻り値

通話が成功したかどうかを示す整数値。

### <a name="method-getcontextmenuoptions"></a>メソッド getContextMenuOptions

    public str getContextMenuOptions()

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

#### <a name="examples"></a>例

次のコード例は、コントロールのスキップ プロパティを返して設定する方法を示しています。

    // Return the value of the skip property. 
    info(strfmt("skip: %1", this.skip())); 
    // Set the value of the skip property. 
    this.skip(true);

### <a name="method-templateid"></a>メソッド templateId

    public str templateId()

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

コントロールのツール ヒント テキストを取得します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドを上書きして、toolTip メソッドに値を渡すことができます。

#### <a name="examples"></a>例

次の例は、toolTip メソッドを上書きする方法を示しています。

    str toolTip() 
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

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-updatewindow"></a>メソッド updateWindow

コントロールのウィンドウを更新します。

    public int updateWindow()

#### <a name="return-value"></a>戻り値

更新が成功した場合は 1、それ以外の場合は 0 です。

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

#### <a name="examples"></a>例

次の例は、コントロールがユーザーから隠されているかどうかを示す値を返して設定する方法を示しています。

    int nUserHide; 
    // The ctrl variable was previously assigned  
    // as a control variable. 
    // Retrieve the userHide value. 
    nUserHide = ctrl.userHide(); 
    // Set the userHide value. 
    ctrl.userHide(1);

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

#### <a name="examples"></a>例

次の例は、userSkip プロパティを返して設定する方法を示しています。

    int nUserSkip 
    // The ctrl variable was previously assigned  
    // as a FormControl value. 
    // Return the userSkip property. 
    nUserSkip = ctrl.userSkip(); 
    // Set the userSkip property. 
    ctrl.userSkip(1);

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

#### <a name="examples"></a>例

次の例は、フォーム コントロールのユーザーの幅を返して設定する方法を示しています。

    int nWidth; 
    // The ctrl variable was previously defined 
    // as a FormControl value. 
    // Return the width. 
    nWidth = ctrl.userWidth(); 
    // Specify the width. 
    ctrl.userWidth(90);  // 15 characters * 6 pixels == 90

### <a name="method-valuestr"></a>メソッド valueStr

文字列形式のコントロールの値を取得します。

    public str valueStr()

#### <a name="return-value"></a>戻り値

文字列形式のコントロールの値。

#### <a name="remarks"></a>備考

valueStr メソッドは、データ ソースにバインドできます。 valueStr メソッドは、コントロールの検証メソッドでは使用しないでください。 代わりに、管理検証メソッドでテキスト メソッドを使用します。

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

フォームのコントロールの上下の間隔を取得または設定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
コントロールの AutoMode を示す整数値。オプション。

<!-- -->

モード  
コントロールの AutoMode を示す整数値。オプション。

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
幅の計算方法を示す整数値。オプション。

<!-- -->

モード  
幅の計算方法を示す整数値。オプション。

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

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロール幅の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します。

| モード         | 幅計算                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| 正確        | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

#### <a name="examples"></a>例

次の例は、フォーム コントロールの幅計算モードを返して設定する方法を示しています。

    int nWidthMode; 
    // The ctrl variable was previously assigned 
    // as a form control variable. 
    // Retrieve the width mode. 
    nWidthMode = ctrl.widthMode (); 
    // Set the width mode. 
    ctrl.widthMode(-1); 
    // Set the width. 
    ctrl.widthValue(180);

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

#### <a name="examples"></a>例

次の例は、フォーム コントロールの幅の値を返して設定する方法を示しています。

    int nWidthValue; 
    // The ctrl variable was previously assigned 
    // as a form control value. 
    // Retrieve the width value. 
    nWidthValue = ctrl.widthValue(); 
    // Set the width value. 
    ctrl.widthMode(-1); 
    ctrl.widthValue(160);

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-settemplateid"></a>メソッド setTemplateId

    public void setTemplateId([str value])

#### <a name="parameters"></a>パラメーター

値  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

#### <a name="examples"></a>例

次の例は、フォーム コントロールの優先幅と高さを設定する方法を示しています。

    // nWidth and nHeight are previously assigned int variables. 
    // ctrl is a previously assigned FormControl variable. 
    ctrl.prefColumnSize( nWidth, nHeight);

### <a name="method-update"></a>メソッド update

コントロールを更新します。

    public void update()

### <a name="method-run"></a>メソッド run

    public void run()

### <a name="method-lock"></a>メソッド lock

フォーム コントロールをロックします。

    public void lock()

#### <a name="remarks"></a>備考

オブジェクトを変更し、他のユーザーが変更を加えるかどうか確信が持てない場合には、Lock コマンドを使用します。 更新内容の保存が完了したら、ロック解除コマンドを使用します。

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

#### <a name="examples"></a>例

次の例は、Infolog に mouseEnter イベントのパラメーターを表示する方法を示しています。

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

### <a name="method-applybuild"></a>メソッド applyBuild

    public void applyBuild()

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

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-new"></a>メソッド new

    public void new(FormBuildControl build, xFormRun formRun)

#### <a name="parameters"></a>パラメーター

build  

<!-- -->

formRun  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-unlock"></a>メソッド unLock

フォーム コントロールのロックを解除します。

    public void unLock(boolean update)

#### <a name="parameters"></a>パラメーター

更新  
コントロールに加えられる変更を保存するかどうかを示すブール値。

### <a name="method-setresourcebundlename"></a>メソッド setResourceBundleName

    public void setResourceBundleName([str value])

#### <a name="parameters"></a>パラメーター

値  

### <a name="method-selectedmenuoption"></a>メソッド selectedMenuOption

    public void selectedMenuOption(int selectedOption)

#### <a name="parameters"></a>パラメーター

selectedOption  

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-onpropchanged"></a>メソッド onPropChanged

    public void onPropChanged([str propName])

#### <a name="parameters"></a>パラメーター

propName  

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

### <a name="method-initialize"></a>メソッド initialize

    public void initialize()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

#### <a name="examples"></a>例

次の例では、ユーザーがフォーム コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。

    public void endDrag() 
    {  
        info("EndDrag completed"); 
        super(); 
    }

## <a name="class-formcontrolcancelablesupereventargs"></a>クラス FormControlCancelableSuperEventArgs
    class FormControlCancelableSuperEventArgs extends FormControlEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明 |
|-------------------------------|-------------|
| public void CancelSuperCall() |             |
| private void new()            |             |

### <a name="method-cancelsupercall"></a>メソッド CancelSuperCall

    public void CancelSuperCall()

### <a name="method-new"></a>メソッド new

    private void new()

## <a name="class-formcontrolcanceleventargs"></a>クラス FormControlCancelEventArgs
    class FormControlCancelEventArgs extends FormControlEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                      | 説明 |
|---------------------------------------------|-------------|
| ::public static boolean cancelled()         |             |
| ::public static void cancel(boolean cancel) |             |
| public void new(boolean cancel)             |             |

### <a name="method-cancelled"></a>メソッド cancelled

    public static boolean cancelled()

#### <a name="return-value"></a>戻り値

### <a name="method-cancel"></a>メソッド cancel

    public static void cancel(boolean cancel)

#### <a name="parameters"></a>パラメーター

キャンセル  

### <a name="method-new"></a>メソッド new

    public void new(boolean cancel)

#### <a name="parameters"></a>パラメーター

キャンセル  

## <a name="class-formcontroleventargs"></a>クラス FormControlEventArgs
    class FormControlEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法 | 説明 |
|--------|-------------|
|        |             |

