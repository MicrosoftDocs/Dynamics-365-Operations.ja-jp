---
title: "F クラス (FormFastTabSummarySeparator から FormGridControl)"
description: "FormFastTabSummarySeparator から FormGridControl までのクラスの API 参照。"
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 63473
ms.assetid: 95c712f2-d71d-4dd1-a9fd-f1b88fe21807
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 44fa0f36ec65469a58518f434def1421b849012b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="f-classes-formfasttabsummaryseparator-to-formgridcontrol"></a>F クラス (FormFastTabSummarySeparator から FormGridControl)

[!include [banner](../includes/banner.md)]

FormFastTabSummarySeparator から FormGridControl までのクラスの API 参照。

<a name="class-formfasttabsummaryseparator"></a>クラス FormFastTabSummarySeparator
---------------------------------

    class FormFastTabSummarySeparator extends FormControl

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
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                                                     |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int displayTarget(\[int value\])                                                                     | コントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
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
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
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
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                                                         |
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
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |

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
設定する値 (オプション)。

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

### <a name="method-displaytarget"></a>メソッド displayTarget

クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

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

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

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
設定する値 (オプション)。

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

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

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

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

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

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

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

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

## <a name="class-formfilterpanecontrol"></a>クラス FormFilterPaneControl
    class FormFilterPaneControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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
| public int displayTarget(\[int value\])                                                                     | クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
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

### <a name="method-columns"></a>メソッド columns

    public int columns([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnsmode"></a>メソッド columnsMode

    public AutoMode columnsMode([AutoMode mode])

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

クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

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
コントロールの高さの計算方法を示す整数値。オプション。

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
コントロール幅の計算方法を示す整数値。オプション。

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
幅をピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

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

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-enter"></a>メソッド enter

    public void enter()

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

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

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

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

## <a name="class-formfunctionbuttoncontrol"></a>クラス FormFunctionButtonControl
    class FormFunctionButtonControl extends FormControl

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
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public int copyCallerQuery(\[int value\])                                                                   |                                                                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public boolean defaultButton(\[boolean value\])                                                             | ボタンをフォームの既定のボタンにするかどうかを指定します。                                                                                                 |
| public str disabledImage(\[str value\])                                                                     | コントロールの無効な画像を取得または設定します。                                                                                                                          |
| public int disabledImageLocation(\[int value\])                                                             |                                                                                                                                                                         |
| public int disabledResource(\[int value\])                                                                  | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                                                          |
| public int displayTarget(\[int value\])                                                                     | クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public boolean forcedToOverflow(\[boolean value\])                                                          |                                                                                                                                                                         |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public int formViewOption(\[int value\])                                                                    |                                                                                                                                                                         |
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
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMode(\[int value\])                                                                          | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                         | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean markAsUserAdd(\[boolean value\])                                                             | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public xMenuFunction menufunction()                                                                         |                                                                                                                                                                         |
| public str menuItemName(\[str value\])                                                                      |                                                                                                                                                                         |
| public MenuItemType menuItemType(\[MenuItemType value\])                                                    |                                                                                                                                                                         |
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
| public int openMode(\[int value\])                                                                          |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                     |                                                                                                                                                                         |
| public str parameters(\[str value\])                                                                        | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                                                  |
| public FormControl parentControl()                                                                          | コントロールの親コントロールを取得します。                                                                                                                           |
| public boolean primary(\[boolean value\])                                                                   |                                                                                                                                                                         |
| public boolean saveRecord(\[boolean value\])                                                                |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public boolean sendExternalContext(\[boolean value\])                                                       |                                                                                                                                                                         |
| public int shortkey(\[int value\])                                                                          |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showShortCut(\[boolean value\])                                                              |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                                                         |
| public str toolTip()                                                                                        | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                     | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMode(\[int value\])                                                                           | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                          | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                              |                                                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                                                         |
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
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void clicked()                                                                                       |                                                                                                                                                                         |
| private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |

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

次のテーブルの値は、韓国語版 msCoNameWindows の値です。

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

### <a name="method-copycallerquery"></a>メソッド copyCallerQuery

    public int copyCallerQuery([int value])

#### <a name="parameters"></a>パラメーター

値  

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

クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

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

### <a name="method-formviewoption"></a>メソッド formViewOption

    public int formViewOption([int value])

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
コントロールの高さの計算方法を示す整数値。オプション。

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

### <a name="method-menufunction"></a>メソッド menufunction

    public xMenuFunction menufunction()

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-openmode"></a>メソッド openMode

    public int openMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

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

### <a name="method-sendexternalcontext"></a>メソッド sendExternalContext

    public boolean sendExternalContext([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public boolean underline([boolean value])

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
コントロール幅の計算方法を示す整数値。オプション。

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
幅をピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

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

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-clicked"></a>メソッド clicked

    public void clicked()

### <a name="method-onclicked"></a>メソッド OnClicked

    private void OnClicked([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formgridcontrol"></a>クラス FormGridControl
    class FormGridControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                              | 説明                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int activeBackColor(\[int value\])                                                                           |                                                                                                                                                                         |
| public int activeForeColor(\[int value\])                                                                           |                                                                                                                                                                         |
| public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])            |                                                                                                                                                                         |
| public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])                     |                                                                                                                                                                         |
| public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\]) |                                                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                                      | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                         | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                                      | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public int alternateRowShading(\[int value\])                                                                       |                                                                                                                                                                         |
| public boolean autoDataGroup(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                                   | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int backgroundColor(\[int value\])                                                                           | コントロールの背景色を取得または設定します。                                                                                                                       |
| public int backStyle(\[int value\])                                                                                 | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                          |
| public int beginDrag(int x, int y)                                                                                  | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public int border(\[int value\])                                                                                    | コントロールの境界線のスタイルを取得または設定します。                                                                                                                |
| public int bottomMargin(\[int value\])                                                                              |                                                                                                                                                                         |
| public container calcControlSize(int chars, int lines)                                                              | コントロールのサイズを取得します。                                                                                                                                      |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                               |                                                                                                                                                                         |
| public boolean canContain(FormControl control)                                                                      |                                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                               | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                            | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                                    | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public boolean contains(FormControl control)                                                                        |                                                                                                                                                                         |
| public int controlCount()                                                                                           |                                                                                                                                                                         |
| public FormControl controlNum(int controlNo)                                                                        |                                                                                                                                                                         |
| public str countryRegionCodes(\[str value\])                                                                        | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                         |                                                                                                                                                                         |
| public str dataGroup(\[str value\])                                                                                 |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                          | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                            | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public str defaultAction(\[str value\])                                                                             |                                                                                                                                                                         |
| public str defaultActionLabel(\[str value\])                                                                        |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                             | クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                                  | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                               | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                           | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public boolean exportAllowed(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public str exportLabel(\[str value\])                                                                               |                                                                                                                                                                         |
| public Struct getLineData(int lineNumber)                                                                           |                                                                                                                                                                         |
| public Struct getSelectedData()                                                                                     |                                                                                                                                                                         |
| public boolean gridLines(\[boolean value\])                                                                         |                                                                                                                                                                         |
| public int gridLinesStyle(\[int value\])                                                                            |                                                                                                                                                                         |
| public str groupBy(\[str value\])                                                                                   |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                          | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                                     | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                          | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                                | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                               | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                              | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                                  | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                           | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public boolean highlightActive(\[boolean value\])                                                                   |                                                                                                                                                                         |
| public int hWnd()                                                                                                   | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public boolean isContainer()                                                                                        |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                        | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                                       | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                            | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。                                                                   |
| public boolean leave()                                                                                              |                                                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                            | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public int leftMargin(\[int value\])                                                                                |                                                                                                                                                                         |
| public int leftMode(\[int value\])                                                                                  | フォームのコントロールの水平配置モードを設定します。                                                                                                           |
| public int leftValue(\[int value\])                                                                                 | フォームのコントロールの水平位置を取得または設定します。                                                                                                        |
| public boolean markAsUserAdd(\[boolean value\])                                                                     | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                   |
| public int moreRowsIndicator(\[int value\])                                                                         |                                                                                                                                                                         |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                     | コントロールがユーザーにダブルクリックされると呼び出されます。                                                                                                               |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。                                                                                                       |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。                                                                                                       |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                           | ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。                                                                                                |
| public int moveControl(int controlId, \[int insertAfterId\])                                                        |                                                                                                                                                                         |
| public boolean multiSelect(\[boolean value\])                                                                       |                                                                                                                                                                         |
| public str name(\[str value\])                                                                                      | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                 |
| public int neededPermission(\[int value\])                                                                          |                                                                                                                                                                         |
| public container SysObsoleteAttribute()                                                                             |                                                                                                                                                                         |
| public FormControl parentControl()                                                                                  | コントロールの親コントロールを取得します。                                                                                                                           |
| public int rightMargin(\[int value\])                                                                               |                                                                                                                                                                         |
| public int scrollbars(\[int value\])                                                                                |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                           | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public boolean showColLabels(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public int showContextMenu(int menuHandle)                                                                          | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showRowLabels(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                              | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                        |                                                                                                                                                                         |
| public int style(\[int value\])                                                                                     |                                                                                                                                                                         |
| public str toolTip()                                                                                                | コントロールのツール ヒント テキストを取得します。                                                                                                                             |
| public int top(int value, \[int mode\])                                                                             | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int topMargin(\[int value\])                                                                                 |                                                                                                                                                                         |
| public int topMode(\[int value\])                                                                                   | フォームのコントロールの垂直配置モードを設定します。                                                                                                             |
| public int topValue(\[int value\])                                                                                  | フォームのコントロールの垂直位置を取得または設定します。                                                                                                          |
| public int type(\[int value\])                                                                                      |                                                                                                                                                                         |
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
| public int userWidth(\[int value\])                                                                                 | ピクセル単位でコントロールの幅を設定するか返します。                                                                                                                     |
| public boolean useUserLayout(\[boolean value\])                                                                     |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                        | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                              | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                                      | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                           | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int visibleCols(\[int value\], \[AutoMode mode\])                                                            |                                                                                                                                                                         |
| public AutoMode visibleColsMode(\[AutoMode mode\])                                                                  |                                                                                                                                                                         |
| public int visibleColsValue(\[int value\])                                                                          |                                                                                                                                                                         |
| public int visibleRows(\[int value\], \[AutoMode mode\])                                                            |                                                                                                                                                                         |
| public AutoMode visibleRowsMode(\[AutoMode mode\])                                                                  |                                                                                                                                                                         |
| public int visibleRowsValue(\[int value\])                                                                          |                                                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                           | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                                 | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                                | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void cut()                                                                                                   | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void applyQuickFilter(\[int controlId\], \[str filterValue\])                                                |                                                                                                                                                                         |
| public void autoSizeColumns(\[boolean autoSizeColumns\])                                                            |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                           | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void context()                                                                                               | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void jumpRef()                                                                                               |                                                                                                                                                                         |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                           |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                        |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])         |                                                                                                                                                                         |
| public void copy()                                                                                                  | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void enter()                                                                                                 |                                                                                                                                                                         |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                                       | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void displayControl()                                                                                        | コントロールを表示します。                                                                                                                                                   |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                          |                                                                                                                                                                         |
| public void paste()                                                                                                 | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void resetUserSetting()                                                                                      | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void quickFilterProvider(\[GridQuickFilterProvider quickFilterProvider\])                                    |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                               | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                            |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                              | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void filter(\[str filterStr\])                                                                               |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                                   | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void dragLeave()                                                                                             | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                         |                                                                                                                                                                         |
| public void lostFocus()                                                                                             | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void endDrag()                                                                                               | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void arrange()                                                                                               |                                                                                                                                                                         |
| public void gotFocus()                                                                                              | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void mouseLeave()                                                                                            | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void setFocus()                                                                                              | コントロールにフォーカスを設定します。                                                                                                                                          |

### <a name="method-activebackcolor"></a>メソッド activeBackColor

    public int activeBackColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-activeforecolor"></a>メソッド activeForeColor

    public int activeForeColor([int value])

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

### <a name="method-alternaterowshading"></a>メソッド alternateRowShading

    public int alternateRowShading([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodatagroup"></a>メソッド autoDataGroup

    public boolean autoDataGroup([boolean value])

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

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value])

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

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datagroup"></a>メソッド dataGroup

    public str dataGroup([str value])

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

使用する必要のあるデータ ソースの ID。

### <a name="method-defaultaction"></a>メソッド defaultAction

    public str defaultAction([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-defaultactionlabel"></a>メソッド defaultActionLabel

    public str defaultActionLabel([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

クライアント、エンタープライズ ポータル、Finance and Operations、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが表示される場所を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  
ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。

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

### <a name="method-exportallowed"></a>メソッド exportAllowed

    public boolean exportAllowed([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-exportlabel"></a>メソッド exportLabel

    public str exportLabel([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getlinedata"></a>メソッド getLineData

    public Struct getLineData(int lineNumber)

#### <a name="parameters"></a>パラメーター

lineNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-getselecteddata"></a>メソッド getSelectedData

    public Struct getSelectedData()

#### <a name="return-value"></a>戻り値

### <a name="method-gridlines"></a>メソッド gridLines

    public boolean gridLines([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-gridlinesstyle"></a>メソッド gridLinesStyle

    public int gridLinesStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-groupby"></a>メソッド groupBy

    public str groupBy([str value])

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

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
高さの計算方法を示す整数。オプション。

<!-- -->

モード  
高さの計算方法を示す整数。オプション。

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
コントロールの高さの計算方法を示す整数値。オプション。

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

### <a name="method-highlightactive"></a>メソッド highlightActive

    public boolean highlightActive([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-morerowsindicator"></a>メソッド moreRowsIndicator

    public int moreRowsIndicator([int value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-movecontrol"></a>メソッド moveControl

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterId  

#### <a name="return-value"></a>戻り値

### <a name="method-multiselect"></a>メソッド multiSelect

    public boolean multiSelect([boolean value])

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

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-scrollbars"></a>メソッド scrollbars

    public int scrollbars([int value])

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

### <a name="method-showcollabels"></a>メソッド showColLabels

    public boolean showColLabels([boolean value])

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

### <a name="method-showrowlabels"></a>メソッド showRowLabels

    public boolean showRowLabels([boolean value])

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

### <a name="method-useuserlayout"></a>メソッド useUserLayout

    public boolean useUserLayout([boolean value])

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

### <a name="method-visiblecols"></a>メソッド visibleCols

    public int visibleCols([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblecolsmode"></a>メソッド visibleColsMode

    public AutoMode visibleColsMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblecolsvalue"></a>メソッド visibleColsValue

    public int visibleColsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblerows"></a>メソッド visibleRows

    public int visibleRows([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblerowsmode"></a>メソッド visibleRowsMode

    public AutoMode visibleRowsMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblerowsvalue"></a>メソッド visibleRowsValue

    public int visibleRowsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
コントロール幅の計算方法を示す整数値。オプション。

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
幅をピクセル単位で指定する整数です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-applyquickfilter"></a>メソッド applyQuickFilter

    public void applyQuickFilter([int controlId], [str filterValue])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

filterValue  

### <a name="method-autosizecolumns"></a>メソッド autoSizeColumns

    public void autoSizeColumns([boolean autoSizeColumns])

#### <a name="parameters"></a>パラメーター

autoSizeColumns  

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

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-enter"></a>メソッド enter

    public void enter()

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

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-quickfilterprovider"></a>メソッド quickFilterProvider

    public void quickFilterProvider([GridQuickFilterProvider quickFilterProvider])

#### <a name="parameters"></a>パラメーター

quickFilterProvider  

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

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-arrange"></a>メソッド arrange

    public void arrange()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()




