---
title: F くらす (FormGroupControl から FormIntControl)
description: このトピックには、FormGroupControl から FormIntControl までのクラスの API リファレンス ドキュメントが含まれています。
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
ms.custom: 63823
ms.assetid: f28e493d-2766-466d-a597-ef82e87cdfa6
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51a7f3ffdc9e65357b55dd70081948f3b2f6edad
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595425"
---
# <a name="f-classes-formgroupcontrol-to-formintcontrol"></a>F くらす (FormGroupControl から FormIntControl)

[!include [banner](../includes/banner.md)]

このトピックには、FormGroupControl から FormIntControl までのクラスの API リファレンス ドキュメントが含まれています。

<a name="class-formgroupcontrol"></a>クラス FormGroupControl
----------------------

    class FormGroupControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                              | 説明                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])            | フォーム グループ コントロールにフォームのコントロールを追加します。                                                                                                                                                        |
| public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])                     |                                                                                                                                                                                                     |
| public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\]) | テーブル フィールドを追加します。                                                                                                                                                                                 |
| public boolean alignChild(\[boolean value\])                                                                        | フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値を設定するか返します。                                                              |
| public boolean alignChildren(\[boolean value\])                                                                     | 子コントロールが一致しているかどうかを示すブール値を設定するか返します。                                                                                                              |
| public boolean alignControl(\[boolean value\])                                                                      | コントロールが他のコントロールと揃っているかどうかを決定します。                                                                                                                                      |
| public boolean allowEdit(\[boolean value\])                                                                         | ユーザーがコントロールの内容を修正できるかどうかを決定します。                                                                                                                                 |
| public boolean allowSysSetup()                                                                                      | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                                                 |
| public int allowUserSetup(\[int value\])                                                                            | フォーム グループ コントロールに実行できる変更のレベルを取得または設定します。                                                                                                              |
| public int arrangeGuide(\[int value\])                                                                              |                                                                                                                                                                                                     |
| public int arrangeMethod(\[int value\])                                                                             | フォーム グループ コントロールのコントロールを配置する方法を示す整数値を設定するか返します。                                                                                                  |
| public int arrangeWhen(\[int value\])                                                                               | コントロールが配置されるタイミングを指定する整数値を設定するか返します。                                                                                                                     |
| public boolean autoDataGroup(\[boolean value\])                                                                     | フォーム グループ コントロールに、コントロールに対して指定されているデータ グループ内のフィールドのみ含めることができるかどうかを指定するブール値を設定するか返します。                                       |
| public boolean autoDeclaration(\[boolean value\])                                                                   | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                                                  |
| public int backgroundColor(\[int value\])                                                                           | コントロールの背景色を取得または設定します。                                                                                                                                                   |
| public Image backgroundImage(\[Image image\], \[int drawMode\])                                                     | フォーム グループ コントロールの背景イメージを指定します。                                                                                                                                            |
| public int backStyle(\[int value\])                                                                                 | コントロールの背景色を透明にできるかどうかを決定します。                                                                                                                                       |
| public int beginDrag(int x, int y)                                                                                  | ユーザーがフォーム グループ コントロールの移動を始めると呼び出されます。                                                                                                                                        |
| public int bold(\[int value\])                                                                                      | コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。                                                                                                                        |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                           | フォーム グループ コントロールの下余白をピクセル単位で設定するか返し、余白が自動的に調整されるかどうかを指定します。                                                                     |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                                 | 下余白が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。                                                                                   |
| public int bottomMarginValue(\[int value\])                                                                         | フォーム グループ コントロールの下余白をピクセル単位で設定するか返します。                                                                                                                                |
| public boolean breakable(\[boolean value\])                                                                         |                                                                                                                                                                                                     |
| public container calcControlSize(int chars, int lines)                                                              | 文字数と明細行数に基づいて、フォーム グループ コントロールのフォント サイズを計算します。                                                                                             |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                               | テーブル フィールドを追加できるかどうかを示します。                                                                                                                                                       |
| public boolean canContain(FormControl control)                                                                      | フォーム グループ コントロールに指定されたフォーム コントロールを含めることができるかどうかを指定します。                                                                                                                      |
| public str caption(\[str value\])                                                                                   | コントロールのキャプションを取得または設定します。                                                                                                                                                             |
| public int characterSet(\[int value\])                                                                              | フォントの文字セットを取得または設定します。                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                               | コントロールの配色を取得または設定します。                                                                                                                                                       |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                             | フォーム グループ コントロールの列の数をピクセル単位で設定するか返し、数が自動的に調整されるかどうかを指定します。                                                                |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                                | フォーム グループ コントロール内の列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。 |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                            | フォーム グループ コントロール内の列間のスペースの量をピクセル単位で設定するか返し、フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整されるかどうかを示します。   |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                                  | フォーム グループ コントロール内の列間のスペースの量が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。                                         |
| public int columnspaceValue(\[int value\])                                                                          | ピクセルでフォーム グループ コントロール内の列間のスペースの量を設定するか返します。                                                                                                              |
| public int columnsValue(\[int value\])                                                                              | フォーム グループ コントロール内のコントロールの数を設定するか返します。                                                                                                                                      |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                            | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                                                 |
| public List configurationKeyEx()                                                                                    | フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。                                                                                           |
| public boolean contains(FormControl control)                                                                        | フォーム グループ コントロールに指定されたフォーム コントロールが含まれるかどうかを指定します。                                                                                                                           |
| public int controlCount()                                                                                           | フォーム グループ コントロール内のコントロールの数を返します。                                                                                                                                             |
| public FormControl controlNum(int controlNo)                                                                        | フォーム グループ コントロールで指定したコントロールの FormControl オブジェクトを返します。                                                                                                                       |
| public str countryRegionCodes(\[str value\])                                                                        | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                                                      |
| public FieldId countryRegionContextField(\[FieldId value\])                                                         |                                                                                                                                                                                                     |
| public str dataGroup(\[str value\])                                                                                 | フォーム グループ コントロールのデータのグループを設定するか返します。                                                                                                                                              |
| public str dataRelationPath(\[str value\])                                                                          | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                                                       |
| public int dataSource(\[AnyType value\])                                                                            | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                                            |
| public int displayTarget(\[int value\])                                                                             | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。                             |
| public int dragDrop(\[int value\])                                                                                  | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                                                |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | オブジェクトがフォーム グループ コントロールの境界上にドラッグされると呼び出されます。                                                                                                                        |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                                                    |
| public str dragText()                                                                                               | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                                              |
| public boolean enableChilds(\[boolean enable\])                                                                     | フォーム グループ コントロールの子コントロールが有効かどうかを指定します。                                                                                                                          |
| public boolean enabled(\[boolean value\])                                                                           | オブジェクトが有効か無効かを決定します。                                                                                                                                               |
| public boolean expand(\[boolean expand\])                                                                           | フォーム グループ コントロールが展開されているかどうかを指定します。                                                                                                                                                 |
| public str font(\[str value\])                                                                                      | コントロール内のテキストに使用されるフォントの名前を取得または設定します。                                                                                                                               |
| public int fontSize(\[int value\])                                                                                  | コントロール内のテキストに使用するフォント サイズを取得または設定します。                                                                                                                                            |
| public int frameOptionButton(\[int value\])                                                                         | フォーム グループ コントロールのオプション ボタンを設定するか返します。                                                                                                                                         |
| public int framePosition(\[int value\])                                                                             | フォーム グループ コントロールのフレームの位置を設定するか返します。                                                                                                                                 |
| public int frameType(\[int value\])                                                                                 | フォーム グループ コントロールのフレーム スタイルを設定するか返します。                                                                                                                                           |
| public boolean hasChanged(\[boolean val\])                                                                          | フォーム グループ コントロールの内容が変更されたかどうかを示すブール値を設定するか返します。                                                                                           |
| public boolean hasUserSetting()                                                                                     | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                                             |
| public int height(int value, \[int mode\])                                                                          | コントロールの高さを取得または設定します。                                                                                                                                                             |
| public int heightMode(\[int value\])                                                                                | コントロールの高さの計算方法を取得または設定します。                                                                                                                                      |
| public int heightValue(\[int value\])                                                                               | コントロールの高さを取得または設定します。                                                                                                                                                             |
| public str helpField()                                                                                              | フォーム グループ コントロールが選択されている場合にステータス バーに表示されるヘルプ テキストを返します。                                                                                                    |
| public str helpText(\[str value\])                                                                                  | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                                     |
| public boolean hideIfEmpty(\[boolean value\])                                                                       | グループ内のコントロールが表示されないときフォーム グループ コントロールを表示するかどうかを示すブール値を設定または取得します。                                                                 |
| public str hierarchyParent(\[str value\])                                                                           | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                                                     |
| public int hWnd()                                                                                                   | フォーム グループ コントロールのハンドルを返します。                                                                                                                                                          |
| public boolean isContainer()                                                                                        | フォーム グループ コントロールがコンテナーであるかどうかを示します。                                                                                                                                              |
| public boolean isDisplayed()                                                                                        | フォーム グループ コントロールが表示されるかどうかを示します。                                                                                                                                                |
| public boolean isRestricted()                                                                                       | コントロールが制限されるかどうかを示す値を取得します。                                                                                                                                 |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                            | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                                                 |
| public boolean italic(\[boolean value\])                                                                            | フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値を設定するか返します。                                                                                                 |
| public int labelBold(\[int value\])                                                                                 | フォーム グループ コントロールのラベル テキストのフォントの太さを設定するか返します。                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                         | フォーム グループ コントロールのラベル テキストのフォントの文字セットを設定するか返します。                                                                                                          |
| public str labelFont(\[str value\])                                                                                 | フォーム グループ コントロールのラベル テキストのフォントを設定するか返します。                                                                                                                               |
| public int labelFontSize(\[int value\])                                                                             | フォーム グループ コントロールのラベル テキストのフォント サイズを設定するか返します。                                                                                                                           |
| public boolean labelItalic(\[boolean value\])                                                                       | フォーム グループ コントロールのラベル テキストが斜体であるかどうかを示すブール値データ型を設定するか返します。                                                                                       |
| public boolean labelUnderline(\[boolean value\])                                                                    | フォーム グループ コントロールのラベル テキストが下線付きであるかどうかを示すブール値データ型を設定するか返します。                                                                                   |
| public boolean leave()                                                                                              | ユーザーがマウス ポインターをフォーム グループ コントロールから離すと呼び出されます。                                                                                                                        |
| public int left(int value, \[int mode\])                                                                            | フォーム グループ コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。                                                                             |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                             | フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。                                                            |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                                   | フォーム グループ コントロールの左余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。        |
| public int leftMarginValue(\[int value\])                                                                           | フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返します。                                                                                                                     |
| public int leftMode(\[int value\])                                                                                  | フォーム グループ コントロールの水平位置を計算する方法を示す値を設定するか返します。                                                                                           |
| public int leftValue(\[int value\])                                                                                 | フォーム グループ コントロールの水平位置をピクセル単位で設定するか返します。                                                                                                                          |
| public boolean markAsUserAdd(\[boolean value\])                                                                     | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                                                                               |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                     | ユーザーがフォーム グループ コントロールをダブルクリックすると呼び出されます。                                                                                                                                         |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがフォーム グループ コントロールでマウス ボタンを押すと呼び出されます。                                                                                                                           |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                         | ユーザーがマウス ポインターをフォーム グループ コントロール上に移動させると呼び出されます。                                                                                                                          |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                           | ユーザーがマウス ボタンをフォーム グループ コントロール上で放すと呼び出されます。                                                                                                                        |
| public int moveControl(int controlId, \[int insertAfterId\])                                                        | 指定されたコントロールを移動します。                                                                                                                                                                          |
| public str name(\[str value\])                                                                                      | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                                             |
| public int neededPermission(\[int value\])                                                                          |                                                                                                                                                                                                     |
| public int optionValue(\[int value\])                                                                               | フォーム グループ コントロールに関連付けられているオプション ボタンの値を設定するか返します。                                                                                                       |
| public container SysObsoleteAttribute()                                                                             |                                                                                                                                                                                                     |
| public FormControl parentControl()                                                                                  | コントロールの親コントロールを取得します。                                                                                                                                                       |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                            | フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。                                                           |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                                  | フォーム グループ コントロールの右余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。       |
| public int rightMarginValue(\[int value\])                                                                          | フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返します。                                                                                                                    |
| public boolean saveFilter(\[boolean value\])                                                                        |                                                                                                                                                                                                     |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                           | フォーム グループ コントロールのセキュリティ キー ID を設定するか返します。                                                                                                                                       |
| public int showContextMenu(int menuHandle)                                                                          | フォーム グループ コントロールのショートカット メニューを表示します。                                                                                                                                                     |
| public boolean skip(\[boolean value\])                                                                              | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示すブール値を設定するか返します。                                                             |
| public int sort(\[SortOrder sortDirection\])                                                                        | フォーム グループ コントロールに格納されているコントロールを並べ替えます。                                                                                                                                      |
| public int style(\[int value\])                                                                                     |                                                                                                                                                                                                     |
| public str toolTip()                                                                                                | フォーム グループ コントロールのツールヒントのテキスト文字列を返します。                                                                                                                                   |
| public int top(int value, \[int mode\])                                                                             | フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。                                                                               |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                              | フォーム グループ コントロールの上余白をピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。                                                                         |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                                    | フォーム グループ コントロールの上余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。         |
| public int topMarginValue(\[int value\])                                                                            |                                                                                                                                                                                                     |
| public int topMode(\[int value\])                                                                                   | フォーム グループ コントロールの垂直位置を計算する方法を示す値を設定するか返します。                                                                                             |
| public int topValue(\[int value\])                                                                                  | フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返します。                                                                                                                            |
| public int type(\[int value\])                                                                                      |                                                                                                                                                                                                     |
| public boolean underline(\[boolean value\])                                                                         | コントロール内のテキストの下線プロパティを設定するか返します。                                                                                                                                 |
| public boolean SysObsoleteAttribute(container data)                                                                 |                                                                                                                                                                                                     |
| public int userData(\[int value\])                                                                                  | コントロールのユーザー データを取得または設定します。                                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                              | コントロールのユーザー データ品目を取得または設定します。                                                                                                                                                    |
| public int userDataItems(\[int value\])                                                                             | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                                                         |
| public int userDisable(\[int value\])                                                                               | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                                                 |
| public int userHeight(\[int value\])                                                                                | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                                                |
| public int userHide(\[int value\])                                                                                  | コントロールがユーザーから非表示になっているかどうかを示す整数データ型を設定するか返します。                                                                                                      |
| public int userOrgContainer(\[int value\])                                                                          | コントロールの組織コンテナを取得または設定します。                                                                                                                                            |
| public int userOrgSibling(\[int value\])                                                                            | コントロールの組織兄弟を取得または設定します。                                                                                                                                              |
| public str userPromptText(\[str value\])                                                                            | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                                                   |
| public int userSecurityLevel(\[int value\])                                                                         | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                                               |
| public int userSkip(\[int value\])                                                                                  | ユーザーが Tab キーを押してコントロールに移動するときにフォーム グループ コントロールがスキップされるかどうかを示す整数を設定するか返します。                                                          |
| public int userWidth(\[int value\])                                                                                 | フォーム グループ コントロールの幅をピクセル単位で示す整数を設定するか返します。                                                                                                              |
| public boolean useUserLayout(\[boolean value\])                                                                     | フォーム グループ コントロールのユーザー指定レイアウトを使用するかどうかを指定します。                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                        | ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定し、スペースを計算する方法を指定します。                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                              | フォーム グループ コントロールの上と下のスペースの量を計算する方法を示す値を設定するか返します。                                                                                  |
| public int verticalSpacingValue(\[int value\])                                                                      | ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定します。                                                                                                                    |
| public int viewEditMode(\[int value\])                                                                              |                                                                                                                                                                                                     |
| public boolean visible(\[boolean value\])                                                                           | フォーム グループ コントロールを表示または非表示にするブール値データ型を取得または設定します。                                                                                                                       |
| public int width(int value, \[int mode\])                                                                           | コントロールの幅を取得または設定します。                                                                                                                                                              |
| public int widthMode(\[int value\])                                                                                 | コントロールの幅の計算方法を取得または設定します。                                                                                                                                     |
| public int widthValue(\[int value\])                                                                                | コントロールの幅を取得または設定します。                                                                                                                                                              |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])         |                                                                                                                                                                                                     |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                           | ユーザーがフォーム グループ コントロールまたはフォーム グループ コントロールのアイテムを新しい位置にドロップすると呼び出されます。                                                                                            |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                        |                                                                                                                                                                                                     |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                            |                                                                                                                                                                                                     |
| public void mouseLeave()                                                                                            | ユーザーがマウス ポインターをコントロールから離すと呼び出されます。                                                                                                                              |
| public void context()                                                                                               | ユーザーがフォーム グループ コントロールを右クリックすると呼び出されます。                                                                                                                                          |
| public void copy()                                                                                                  | フォーム グループ コントロールをコピーします。                                                                                                                                                                        |
| public void cut()                                                                                                   | コントロールのコンテンツを切り取りします。                                                                                                                                                                   |
| public void paste()                                                                                                 | フォーム グループ コントロールを貼り付けます。                                                                                                                                                                        |
| public void arrange()                                                                                               |                                                                                                                                                                                                     |
| public void clicked()                                                                                               | フォーム グループ コントロールがユーザーにクリックされると呼び出されます。                                                                                                                                         |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                          |                                                                                                                                                                                                     |
| public void inputSearch(str searchStr)                                                                              | ユーザーがバインドされたコントロールに検索文字列を入力すると呼び出されます。                                                                                                                                  |
| public void resetUserSetting()                                                                                      | フォーム グループ コントロールのユーザー設定をリセットします。                                                                                                                                                  |
| private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])                                          |                                                                                                                                                                                                     |
| public void lostFocus()                                                                                             | ユーザーがフォーム グループ コントロールをフォーカス外に持っていくと呼び出されます。                                                                                                                                   |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                               | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                                                |
| public void endDrag()                                                                                               | ユーザーがフォーム グループ コントロールの移動を終了すると呼び出されます。                                                                                                                                   |
| public void jumpRef()                                                                                               | ユーザーがフォーム グループ コントロールのコントロール ショートカット メニューでメイン テーブルへ移動フォーム コマンドをクリックすると呼び出されます。                                                                              |
| public void setFocus()                                                                                              | コントロールにフォーカスを設定します。                                                                                                                                                                      |
| public void filter(\[str filterStr\])                                                                               | ユーザーがフォーム グループ コントロールを右クリックしてから選択フィルタをクリックすると呼び出されます。                                                                                                      |
| public void displayControl()                                                                                        | フォーム グループ コントロールを表示します。                                                                                                                                                                      |
| public void gotFocus()                                                                                              | ユーザーがフォーム グループ コントロールにフォーカスを移すタイミングを指定します。                                                                                                                                    |
| public void prefColumnSize(int width, int height)                                                                   | フォーム グループ コントロールの列の高さと幅を指定します。                                                                                                                                 |
| public void dragLeave()                                                                                             | ユーザーがフォーム グループ コントロールの境界からオブジェクトをドラッグすると呼び出されます。                                                                                                                  |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                         |                                                                                                                                                                                                     |
| public void enter()                                                                                                 | ユーザーがフォーム グループ コントロールにフォーカスを移動すると呼び出されます。                                                                                                                                        |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                                       | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                                              |

### <a name="method-addcontrol"></a>メソッド addControl

フォーム グループ コントロールにフォームのコントロールを追加します。

    public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])

#### <a name="parameters"></a>パラメーター

controlType  
コントロールの位置を示す値、オプション。 既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。

<!-- -->

controlName  
コントロールの位置を示す値、オプション。 既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。

<!-- -->

insertAfter  
コントロールの位置を示す値、オプション。 既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。

#### <a name="return-value"></a>戻り値

フォーム コントロールを構成する FormControl オブジェクト。

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

テーブル フィールドを追加します。

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

フォーム コントロールを変更する FormControl オブジェクト。

### <a name="method-alignchild"></a>メソッド alignChild

フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値を設定するか返します。

    public boolean alignChild([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

コントロールがアラインされた場合は true。それ以外の場合は false。

### <a name="method-alignchildren"></a>メソッド alignChildren

子コントロールが一致しているかどうかを示すブール値を設定するか返します。

    public boolean alignChildren([boolean value])

#### <a name="parameters"></a>パラメーター

値  
子コントロールが一致しているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

子コントロールがアラインされた場合は true。それ以外の場合は false。

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールが他のコントロールと揃っているかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールが他のコントロールと一致しているかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに基づいて配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を修正できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  
データを変更できるかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

コントロールを変更することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowsyssetup"></a>メソッド allowSysSetup

SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。

    public boolean allowSysSetup()

#### <a name="return-value"></a>戻り値

コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。

### <a name="method-allowusersetup"></a>メソッド allowUserSetup

フォーム グループ コントロールに実行できる変更のレベルを取得または設定します。

    public int allowUserSetup([int value])

#### <a name="parameters"></a>パラメーター

値  
実行可能な変更のレベルを示す整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

実行可能な変更のレベルを示す整数値。

#### <a name="remarks"></a>備考

値パラメーターのために FormAllowUserSetup 列挙型値を使用することができます。

### <a name="method-arrangeguide"></a>メソッド arrangeGuide

    public int arrangeGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangemethod"></a>メソッド arrangeMethod

フォーム グループ コントロールのコントロールを配置する方法を示す整数値を設定するか返します。

    public int arrangeMethod([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールのコントロールを配置する方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールのコントロールを配置する方法を示す整数値。

#### <a name="remarks"></a>備考

\_value パラメーターのために ArrangeMethod 列挙型値を使用することができます。

### <a name="method-arrangewhen"></a>メソッド arrangeWhen

コントロールが配置されるタイミングを指定する整数値を設定するか返します。

    public int arrangeWhen([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールが配置されるタイミングを指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールが配置されるタイミングを指定する整数値。

### <a name="method-autodatagroup"></a>メソッド autoDataGroup

フォーム グループ コントロールに、コントロールに対して指定されているデータ グループ内のフィールドのみ含めることができるかどうかを指定するブール値を設定するか返します。

    public boolean autoDataGroup([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールがデータ グループ内のフィールドのみを含めることができるかどうかを示すブール値データ型。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールにデータ グループ内のフィールドのみを含めることができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

フォーム グループ コントロールのデータ グループを設定または取得するには、FormGroupControl.dataGroup メソッドを使用します。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールと同じ名前の変数を、システムが宣言するかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  
背景色を指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backgroundimage"></a>メソッド backgroundImage

フォーム グループ コントロールの背景イメージを指定します。

    public Image backgroundImage([Image image], [int drawMode])

#### <a name="parameters"></a>パラメーター

image  
画像の描画方法を指定する整数データ型です (オプション)。

<!-- -->

drawMode  
画像の描画方法を指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

イメージ オブジェクトです。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  
背景スタイル示す整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム グループ コントロールの移動を始めると呼び出されます。

    public int beginDrag(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
移動イベントの y 座標を示す整数値。

<!-- -->

y  
移動イベントの y 座標を示す整数値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  
フォントの太さを指定する整数値。オプション。

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

### <a name="method-bottommargin"></a>メソッド bottomMargin

フォーム グループ コントロールの下余白をピクセル単位で設定するか返し、余白が自動的に調整されるかどうかを指定します。

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

ピクセル単位の下余白を指定する整数データ型値です。

### <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

下余白が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

フォント サイズなどの他のフォーム設定に基づいて余白が自動的に調整される場合は AutoMode::Auto です。それ以外の場合は、AutoMode::Fixed です。

### <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

フォーム グループ コントロールの下余白をピクセル単位で設定するか返します。

    public int bottomMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  
ピクセルの下余白を指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

ピクセル単位の下余白を指定する整数データ型値です。

### <a name="method-breakable"></a>メソッド breakable

    public boolean breakable([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-calccontrolsize"></a>メソッド calcControlSize

文字数と明細行数に基づいて、フォーム グループ コントロールのフォント サイズを計算します。

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a>パラメーター

chars  
行数を指定する整数データ型です。

<!-- -->

明細行  
行数を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールのサイズを指定するコンテナー データ型値。

### <a name="method-canadddatafield"></a>メソッド canAddDataField

テーブル フィールドを追加できるかどうかを示します。

    public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSourceId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

テーブルを追加できる場合は true。それ以外の場合は、false。

### <a name="method-cancontain"></a>メソッド canContain

フォーム グループ コントロールに指定されたフォーム コントロールを含めることができるかどうかを指定します。

    public boolean canContain(FormControl control)

#### <a name="parameters"></a>パラメーター

control  
フォーム コントロールを指定する FormControl オブジェクト。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールに指定フォーム コントロールを含めることができる場合は true。それ以外の場合は、false。

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  
キャプション テキストを指定する文字列データ型; オプション。

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  
テキスト フォントの文字セットを指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに示されるように文字セットを示します。

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

既定の文字が設定される値は、現在のシステム ロケールに応じて設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールのカラー パレットを指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

0 (ゼロ) から 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 先頭値 | スタイル                  |
|-------|------------------------|
| 0     | 既定。               |
| 1     | Windows パレット。   |
| 2     | 真の配色。 |

### <a name="method-columns"></a>メソッド columns

フォーム グループ コントロールの列の数をピクセル単位で設定するか返し、数が自動的に調整されるかどうかを指定します。

    public int columns([int value], [ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

値  
列数が固定されているかどうか、またはフォーム サイズなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
列数が固定されているかどうか、またはフォーム サイズなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロール内の列数をピクセル単位で指定する整数値。

### <a name="method-columnsmode"></a>メソッド columnsMode

フォーム グループ コントロール内の列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

    public ColumnsMode columnsMode([ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

モード  
列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

列の数が自動的に調整される場合は Automode::Auto、それ以外の場合は Automode::Fixed となります。

### <a name="method-columnspace"></a>メソッド columnspace

フォーム グループ コントロール内の列間のスペースの量をピクセル単位で設定するか返し、フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整されるかどうかを示します。

    public int columnspace([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロール内の列の間のスペースをピクセル単位で指定する整数値。

### <a name="method-columnspacemode"></a>メソッド columnspaceMode

フォーム グループ コントロール内の列間のスペースの量が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。

    public AutoMode columnspaceMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

容量が自動的に調整される場合は AutoMode::Auto です。それ以外の場合は、AutoMode::Fixed です。

### <a name="method-columnspacevalue"></a>メソッド columnspaceValue

ピクセルでフォーム グループ コントロール内の列間のスペースの量を設定するか返します。

    public int columnspaceValue([int value])

#### <a name="parameters"></a>パラメーター

値  
ピクセルにフォーム グループ コントロール内の列間のスペース量を指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロール内のピクセル単位で列の間の容量を指定する整数値。

### <a name="method-columnsvalue"></a>メソッド columnsValue

フォーム グループ コントロール内のコントロールの数を設定するか返します。

    public int columnsValue([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールの列数を指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの列数を指定する整数データ型値です。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
コンフィギュレーション キーの ID を特定する configurationKeyId システム データ型; オプション。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。

    public List configurationKeyEx()

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリスト オブジェクト。

#### <a name="remarks"></a>備考

リストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 さらに、返されたリストには、拡張データ型に適用される任意のコンフィギュレーション キー ID が含まれます。

### <a name="method-contains"></a>メソッド contains

フォーム グループ コントロールに指定されたフォーム コントロールが含まれるかどうかを指定します。

    public boolean contains(FormControl control)

#### <a name="parameters"></a>パラメーター

control  
フォーム コントロールを指定する FormControl オブジェクト。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールに指定フォーム コントロールが含まれる場合は true。それ以外の場合は、false。

### <a name="method-controlcount"></a>メソッド controlCount

フォーム グループ コントロール内のコントロールの数を返します。

    public int controlCount()

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールのコントロールの数を指定する整数データ型値です。

#### <a name="remarks"></a>備考

FormGroupControl.addControl メソッドを使用することにより、フォーム グループ コントロールに対してコントロールを追加することができます。

### <a name="method-controlnum"></a>メソッド controlNum

フォーム グループ コントロールで指定したコントロールの FormControl オブジェクトを返します。

    public FormControl controlNum(int controlNo)

#### <a name="parameters"></a>パラメーター

controlNo  
フォーム グループ コントロール内で管理を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム コントロールに関する情報を変更および提供するために使用できる FormControl オブジェクト。

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

フォーム グループ コントロールのデータのグループを設定するか返します。

    public str dataGroup([str value])

#### <a name="parameters"></a>パラメーター

値  
データ グループを指定する文字列データ型; オプション。

#### <a name="return-value"></a>戻り値

データ グループを指定する文字列データ型値。

#### <a name="remarks"></a>備考

データ グループは、フォームのデータ ソースであるテーブルのフィールド グループに対応します。

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
ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

#### <a name="remarks"></a>備考

動作を指定するには、FormGroupControl.dragLeave および FormGroupControl.dragOver メソッドを使用します。 値パラメーターに true または false の値を渡すことができます。

### <a name="method-dragover"></a>メソッド dragOver

オブジェクトがフォーム グループ コントロールの境界上にドラッグされると呼び出されます。

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
オブジェクト位置の y 座標を示す整数データ型です。

<!-- -->

dragMode  
オブジェクト位置の y 座標を示す整数データ型です。

<!-- -->

x  
オブジェクト位置の y 座標を示す整数データ型です。

<!-- -->

y  
オブジェクト位置の y 座標を示す整数データ型です。

#### <a name="return-value"></a>戻り値

オブジェクトが移動、コピー、または指定された位置に移動されていないかどうかを示す FormDrag システム列挙値。

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、dragOver をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

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

### <a name="method-enablechilds"></a>メソッド enableChilds

フォーム グループ コントロールの子コントロールが有効かどうかを指定します。

    public boolean enableChilds([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  
子コントロールが有効かどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

子コントロールが有効にされた場合は true。それ以外の場合は false。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトが有効か無効かを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールが有効かどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-expand"></a>メソッド expand

フォーム グループ コントロールが展開されているかどうかを指定します。

    public boolean expand([boolean expand])

#### <a name="parameters"></a>パラメーター

expand  
フォーム グループ コントロールが展開されているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールが拡張されている場合は true。それ以外の場合は、false。

### <a name="method-font"></a>メソッド font

コントロール内のテキストに使用されるフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロール内のテキストのフォントを示す文字列データ型; オプション。

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用されるべきフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

コントロール内のテキストに使用するフォント サイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロール内のテキストのフォント サイズをポイントで示す整数値。 オプション。

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-frameoptionbutton"></a>メソッド frameOptionButton

フォーム グループ コントロールのオプション ボタンを設定するか返します。

    public int frameOptionButton([int value])

#### <a name="parameters"></a>パラメーター

値  
オプション ボタンのタイプを指定する整数データ型です (オプション)。

#### <a name="return-value"></a>戻り値

オプション ボタンのタイプを指定する整数値。

#### <a name="remarks"></a>備考

値パラメーターのために FormFrameOptionButton 列挙型値を使用することができます。

### <a name="method-frameposition"></a>メソッド framePosition

フォーム グループ コントロールのフレームの位置を設定するか返します。

    public int framePosition([int value])

#### <a name="parameters"></a>パラメーター

値  
フレームの場所を指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

フレームの場所を指定する整数値。

### <a name="method-frametype"></a>メソッド frameType

フォーム グループ コントロールのフレーム スタイルを設定するか返します。

    public int frameType([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールのフレーム スタイルを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールのフレーム スタイルを示す整数値。

#### <a name="remarks"></a>備考

値パラメーターのために FormFrameType 列挙型値を使用することができます。

### <a name="method-haschanged"></a>メソッド hasChanged

フォーム グループ コントロールの内容が変更されたかどうかを示すブール値を設定するか返します。

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a>パラメーター

val  
フォーム グループ コントロールの内容が変更されたかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

内容が変更された場合は true。それ以外の場合は、false。

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

#### <a name="examples"></a>例

次の例は、コントロールの高さを 120 ピクセルに設定する height メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.height(120, -1); 
    }

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

次の例は、正確なピクセル値に基づいてコントロールの高さを調整する heightMode メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.heightMode(-1); 
        formGroupControl.heightValue(120); 
    }

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

次の例は、高さを 5 ピクセルに設定する heightValue メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
       Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.heightMode(-1); 
        formGroupControl.heightValue(120); 
    }

### <a name="method-helpfield"></a>メソッド helpField

フォーム グループ コントロールが選択されている場合にステータス バーに表示されるヘルプ テキストを返します。

    public str helpField()

#### <a name="return-value"></a>戻り値

ヘルプ テキストを含む文字列データ型値。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  
ヘルプ テキストを含む文字列データ型値。

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

グループ内のコントロールが表示されないときフォーム グループ コントロールを表示するかどうかを示すブール値を設定または取得します。

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールが表示されているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールが表示されない場合は true。それ以外の場合は、false。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

コントロールの HierarchyParent プロパティ値を取得または設定します。

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの HierarchyParent プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールの HierarchyParent プロパティ値。

### <a name="method-hwnd"></a>メソッド hWnd

フォーム グループ コントロールのハンドルを返します。

    public int hWnd()

#### <a name="return-value"></a>戻り値

ハンドルを指定する整数値。

### <a name="method-iscontainer"></a>メソッド isContainer

フォーム グループ コントロールがコンテナーであるかどうかを示します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールがコンテナーである場合は true。それ以外の場合は、false。

### <a name="method-isdisplayed"></a>メソッド isDisplayed

フォーム グループ コントロールが表示されるかどうかを示します。

    public boolean isDisplayed()

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールが表示されている場合は true。それ以外の場合は、false。

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

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。 「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

#### <a name="remarks"></a>備考

次のテーブルでは、neededSetupRights パラメーターの値について説明します。

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

フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値を設定するか返します。

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

テキストが斜体である場合は true。それ以外の場合は false。

### <a name="method-labelbold"></a>メソッド labelBold

フォーム グループ コントロールのラベル テキストのフォントの太さを設定するか返します。

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  
ラベル テキストのフォントの太さを指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

ラベル テキストのフォントの太さを指定する整数値。

#### <a name="remarks"></a>備考

値パラメーターおよび戻り値の使用可能な値の詳細については、太字のメソッドを参照してください。

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

フォーム グループ コントロールのラベル テキストのフォントの文字セットを設定するか返します。

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  
ラベル テキストのフォントの文字セットを指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

ラベル テキストのフォントの文字セットを指定する整数データ型値です。

#### <a name="remarks"></a>備考

文字セットは、共通の関係を持つアルファベット、数字、およびその他の文字のグループです。 たとえば、特定の国/地域または言語に対して文字セットを使用する可能性があります。 値パラメーターの可能な値の一覧については、characterSet メソッドを参照してください。 可能な戻り値の一覧については、characterSet メソッドを参照してください。

### <a name="method-labelfont"></a>メソッド labelFont

フォーム グループ コントロールのラベル テキストのフォントを設定するか返します。

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  
ラベル テキストのフォントを指定する文字列データ型; オプション。

#### <a name="return-value"></a>戻り値

ラベル テキストのフォントを指定する文字列データ型値。

### <a name="method-labelfontsize"></a>メソッド labelFontSize

フォーム グループ コントロールのラベル テキストのフォント サイズを設定するか返します。

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  
ラベル テキストのフォント サイズを指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

ラベル テキストのフォント サイズを指定する整数値。

### <a name="method-labelitalic"></a>メソッド labelItalic

フォーム グループ コントロールのラベル テキストが斜体であるかどうかを示すブール値データ型を設定するか返します。

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ラベル テキストが斜体かどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

ラベル テキストが斜体である場合は true。それ以外の場合は false。

### <a name="method-labelunderline"></a>メソッド labelUnderline

フォーム グループ コントロールのラベル テキストが下線付きであるかどうかを示すブール値データ型を設定するか返します。

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
ラベル テキストに下線が引かれているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

ラベル テキストが下線付きである場合は true。それ以外の場合は false。

### <a name="method-leave"></a>メソッド leave

ユーザーがマウス ポインターをフォーム グループ コントロールから離すと呼び出されます。

    public boolean leave()

#### <a name="return-value"></a>戻り値

マウス ポインターがフォーム グループ コントロールの外に移動する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、leave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-left"></a>メソッド left

フォーム グループ コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
位置の計算方法を示す整数値。オプション。

<!-- -->

モード  
位置の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの水平位置をピクセル単位で示す整数値。

#### <a name="remarks"></a>備考

mode パラメーターは、次の値のいずれかになります。

-   -1 (既定) - 値パラメーターの値が正確に使用される Exact モードを使用します。
-   FormLeft 列挙値。

#### <a name="examples"></a>例

次の例は、水平方向の位置を 50 ピクセルに設定する left メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.left(50,-1); 
    }

### <a name="method-leftmargin"></a>メソッド leftMargin

フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。

### <a name="method-leftmarginmode"></a>メソッド leftMarginMode

フォーム グループ コントロールの左余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

左余白のサイズが自動的に調整される場合は Automode::Auto、それ以外の場合は Automode::Fixed となります。

### <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返します。

    public int leftMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。

### <a name="method-leftmode"></a>メソッド leftMode

フォーム グループ コントロールの水平位置を計算する方法を示す値を設定するか返します。

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  
水平位置の計算方法を示す整数データ型です。オプションです。

#### <a name="return-value"></a>戻り値

水平位置の計算方法を示す整数データ型値です。正確なピクセル値、または FormLeft 列挙値は -1 のいずれかになります。

#### <a name="examples"></a>例

次の例は、正確なピクセル値に基づいて、フォーム グループ コントロールの水平方向位置を計算する leftMode メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.leftMode(-1); 
        formGroupControl.leftValue(50); 
    }

### <a name="method-leftvalue"></a>メソッド leftValue

フォーム グループ コントロールの水平位置をピクセル単位で設定するか返します。

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  
水平位置をピクセル単位で示す整数値。オプション。

#### <a name="return-value"></a>戻り値

水平位置をピクセル単位で示す整数値。

#### <a name="remarks"></a>備考

正確なピクセル値に左モードが設定されていない限り、水平位置は変更されません。

#### <a name="examples"></a>例

次の例は、水平方向の位置を 50 ピクセルに設定する leftValue メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        //C reate the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.leftMode(-1); 
        formGroupControl.leftValue(50); 
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

ユーザーがフォーム グループ コントロールをダブルクリックすると呼び出されます。

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

y  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを指定するブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseDblClick をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがフォーム グループ コントロールでマウス ボタンを押すと呼び出されます。

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

y  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを指定するブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseDown をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをフォーム グループ コントロール上に移動させると呼び出されます。

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

y  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを指定するブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 \_button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseMove をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがマウス ボタンをフォーム グループ コントロール上で放すと呼び出されます。

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

y  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを指定するブール値。

#### <a name="return-value"></a>戻り値

イベントが処理された場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 \_button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseUp をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-movecontrol"></a>メソッド moveControl

指定されたコントロールを移動します。

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a>パラメーター

controlId  
指定されたコントロールが後で挿入されるコントロールを示す整数値。オプション。

<!-- -->

insertAfterId  
指定されたコントロールが後で挿入されるコントロールを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロール ID を指定する整数データ型値です。

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

### <a name="method-optionvalue"></a>メソッド optionValue

フォーム グループ コントロールに関連付けられているオプション ボタンの値を設定するか返します。

    public int optionValue([int value])

#### <a name="parameters"></a>パラメーター

値  
オプション ボタンの値を指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

オプション ボタンの値を指定する整数値。

#### <a name="remarks"></a>備考

フォーム グループ コントロールのオプション ボタンを設定または返すには、FormGroupControl.frameOptionButton メソッドを使用します。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public container SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-parentcontrol"></a>メソッド parentControl

コントロールの親コントロールを取得します。

    public FormControl parentControl()

#### <a name="return-value"></a>戻り値

コントロールの親コントロール。

### <a name="method-rightmargin"></a>メソッド rightMargin

フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。

### <a name="method-rightmarginmode"></a>メソッド rightMarginMode

フォーム グループ コントロールの右余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

右余白のサイズを固定したかどうか、または自動的に調整するかどうかを指定する Automode 列挙値です。右余白のサイズが自動的に調整される場合は自動、そうでなければ、固定します。

### <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返します。

    public int rightMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。

### <a name="method-savefilter"></a>メソッド saveFilter

    public boolean saveFilter([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

フォーム グループ コントロールのセキュリティ キー ID を設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
ID を含む SecurityKeyId データ型、オプション。

#### <a name="return-value"></a>戻り値

ID を含む SecurityKeyId データ型の値。

### <a name="method-showcontextmenu"></a>メソッド showContextMenu

フォーム グループ コントロールのショートカット メニューを表示します。

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a>パラメーター

menuHandle  
ショートカット メニューのハンドルを指定する整数値。

#### <a name="return-value"></a>戻り値

ユーザーの選択を指定する整数値。

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示すブール値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールがスキップされたかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-sort"></a>メソッド sort

フォーム グループ コントロールに格納されているコントロールを並べ替えます。

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a>パラメーター

sortDirection  
コントロールの並べ替え順序を示すシステム列挙値、オプション。

#### <a name="return-value"></a>戻り値

並べ替え順序を含む整数値。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltip"></a>メソッド toolTip

フォーム グループ コントロールのツールヒントのテキスト文字列を返します。

    public str toolTip()

#### <a name="return-value"></a>戻り値

ツールヒントのテキストを含む文字列値。

### <a name="method-top"></a>メソッド top

フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
垂直位置の計算方法を示す整数値。オプション。

<!-- -->

モード  
垂直位置の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの垂直位置をピクセル単位で示す整数値。

#### <a name="remarks"></a>備考

mode パラメーターは、次の値のいずれかになります。

-   -1 (既定) - 値パラメーターの値が正確に使用される Exact モードを使用します。
-   FormTop 列挙値。

#### <a name="examples"></a>例

次の例では、上位メソッドを呼び出して、垂直位置を 50 ピクセルに設定します。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.top(50,-1); 
    }

### <a name="method-topmargin"></a>メソッド topMargin

フォーム グループ コントロールの上余白をピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの上余白のサイズをピクセル単位で指定する整数。

### <a name="method-topmarginmode"></a>メソッド topMarginMode

フォーム グループ コントロールの上余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す Automode 列挙値です。

#### <a name="return-value"></a>戻り値

左余白のサイズが自動的に調整される場合は自動の Automode 列挙値、そうでない場合は、固定します。

### <a name="method-topmarginvalue"></a>メソッド topMarginValue

    public int topMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

フォーム グループ コントロールの垂直位置を計算する方法を示す値を設定するか返します。

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  
垂直位置の計算方法を示す整数。オプション。

#### <a name="return-value"></a>戻り値

垂直位置の計算方法を示す整数値。正確なピクセル値、または FormTop 列挙値は -1 。

#### <a name="examples"></a>例

次の例は、正確なピクセル値に基づいて、垂直位置を計算する topMode メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run time-form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.topMode(-1); 
        formGroupControl.topValue(50); 
    }

### <a name="method-topvalue"></a>メソッド topValue

フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返します。

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  
垂直位置を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの垂直位置を指定する整数データ型値です。

#### <a name="remarks"></a>備考

正確なピクセル値に上部モードが設定されていない限り、垂直位置は変更されません。 詳細については、「topMode メソッド」を参照してください。

#### <a name="examples"></a>例

次の例は、垂直位置を 50 ピクセルに設定する topValue メソッドの呼び出しを示しています。

    void FormGoupControl() 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.topMode(-1); 
        formGroupControl.topValue(50); 
    }

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

コントロールがユーザーから非表示になっているかどうかを示す整数データ型を設定するか返します。

    public int userHide([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールはユーザーから隠されているかどうかを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

ユーザーは、コントロールを右クリックして [非表示] をクリックして、フォーム グループ コントロールを非表示にできます。 このメソッドでは、プログラムを使用してコントロールが非表示にするかどうかを指定できます。

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

ユーザーが Tab キーを押してコントロールに移動するときにフォーム グループ コントロールがスキップされるかどうかを示す整数を設定するか返します。

    public int userSkip([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールをスキップするかどうかのユーザー設定を示す整数。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールがスキップされる場合は 1、それ以外の場合、0 です。

#### <a name="remarks"></a>備考

ユーザーは、ユーザー設定フォームを使用してフォーム グループ コントロールをスキップするかどうかを選択します。

### <a name="method-userwidth"></a>メソッド userWidth

フォーム グループ コントロールの幅をピクセル単位で示す整数を設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールの幅をピクセル単位で示す整数。オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールの幅をピクセル単位で示す整数値。ユーザーが幅を指定していない場合は 0 (ゼロ) 。

#### <a name="remarks"></a>備考

ユーザーは、ユーザー設定フォームを使用して文字の幅を指定します。 このメソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。

### <a name="method-useuserlayout"></a>メソッド useUserLayout

フォーム グループ コントロールのユーザー指定レイアウトを使用するかどうかを指定します。

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールのユーザー指定のレイアウトを使用するかどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールのユーザー指定レイアウトが使用される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

ユーザーは、ユーザー設定フォームを使用してレイアウトを指定します。

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定し、スペースを計算する方法を指定します。

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

<!-- -->

モード  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

#### <a name="return-value"></a>戻り値

コントロールの上と下のスペースの量を示す整数値。

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォーム グループ コントロールの上と下のスペースの量を計算する方法を示す値を設定するか返します。

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

#### <a name="return-value"></a>戻り値

フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整される場合 AutoMode 列挙は自動に設定しますが、それ以外の場合は、固定します。

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定します。

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの上と下のスペースの量を示す整数。オプション。

#### <a name="return-value"></a>戻り値

コントロールの上と下のスペースの量を示す整数値。

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

フォーム グループ コントロールを表示または非表示にするブール値データ型を取得または設定します。

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フォーム グループ コントロールを表示または非表示にするブール値; オプション。

#### <a name="return-value"></a>戻り値

フォーム グループ コントロールが表示される場合は true。それ以外の場合は、false。

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  
幅の計算方法を示す整数。 これは、次のいずれかの値になります。

<!-- -->

モード  
幅の計算方法を示す整数。 これは、次のいずれかの値になります。

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

次の例は、コントロールの幅を 200 ピクセルに設定する width メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.width(200,-1); 
    }

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロール幅の計算方法を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

現在の計算モードの幅を示す整数値。

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
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.widthMode(-1); 
        formGroupControl.widthValue(200); 
    }

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅をピクセル単位で指定する整数。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

#### <a name="examples"></a>例

次の例は、コントロールの幅を 200 ピクセルに設定する widthValue メソッドの呼び出しを示しています。

    static void createForm(Args _args) 
    { 
        Args args; 
        Form form; 
        FormRun formRun; 
        FormBuildDesign formBuildDesign; 
        FormBuildDataSource formBuildDataSource; 
        FormBuildStringControl formBuildStringControl; 
        FormBuildGroupControl formBuildGroupControl; 
        FormGroupControl formGroupControl; 
        int idx; 
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
        // Add controls. 
        formBuildGroupControl = 
     formBuildDesign.addControl(FormControlType::Group,"Group"); 
        idx = formBuildGroupControl.id(); 
        formBuildStringControl = 
     formBuildGroupControl.addControl(FormControlType::String,"String"); 
        // Add data fields to the controls. 
        formBuildGroupControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataSource(formBuildDataSource.id()); 
        formBuildStringControl.dataField(2); 
        args = new Args(); 
        args.object(form); 
        // Create the run-time form. 
        formRun = classfactory.formRunClass(args); 
        formRun.run(); 
        formRun.detach(); 
        formGroupControl = formRun.control(idx); 
        formGroupControl.widthMode(-1); 
        formGroupControl.widthValue(200); 
    }

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-drop"></a>メソッド drop

ユーザーがフォーム グループ コントロールまたはフォーム グループ コントロールのアイテムを新しい位置にドロップすると呼び出されます。

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a>パラメーター

dragSource  
オブジェクト位置の y 座標を示す整数値。

<!-- -->

dragMode  
オブジェクト位置の y 座標を示す整数値。

<!-- -->

x  
オブジェクト位置の y 座標を示す整数値。

<!-- -->

y  
オブジェクト位置の y 座標を示す整数値。

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、drop をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-mouseleave"></a>メソッド mouseLeave

ユーザーがマウス ポインターをコントロールから離すと呼び出されます。

    public void mouseLeave()

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseLeave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-context"></a>メソッド context

ユーザーがフォーム グループ コントロールを右クリックすると呼び出されます。

    public void context()

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、コンテキストをクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-copy"></a>メソッド copy

フォーム グループ コントロールをコピーします。

    public void copy()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-paste"></a>メソッド paste

フォーム グループ コントロールを貼り付けます。

    public void paste()

### <a name="method-arrange"></a>メソッド arrange

    public void arrange()

### <a name="method-clicked"></a>メソッド clicked

フォーム グループ コントロールがユーザーにクリックされると呼び出されます。

    public void clicked()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-inputsearch"></a>メソッド inputSearch

ユーザーがバインドされたコントロールに検索文字列を入力すると呼び出されます。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
検索テキストを含む文字列データ型; オプション。

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、inputSearch をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

フォーム グループ コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-onclicked"></a>メソッド OnClicked

    private void OnClicked([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lostfocus"></a>メソッド lostFocus

ユーザーがフォーム グループ コントロールをフォーカス外に持っていくと呼び出されます。

    public void lostFocus()

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、lostFocus をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」フォームを参照してください。

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

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム グループ コントロールの移動を終了すると呼び出されます。

    public void endDrag()

### <a name="method-jumpref"></a>メソッド jumpRef

ユーザーがフォーム グループ コントロールのコントロール ショートカット メニューでメイン テーブルへ移動フォーム コマンドをクリックすると呼び出されます。

    public void jumpRef()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-filter"></a>メソッド filter

ユーザーがフォーム グループ コントロールを右クリックしてから選択フィルタをクリックすると呼び出されます。

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  
フィルターのテキストを指定する文字列データ型; オプション。

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、filter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-displaycontrol"></a>メソッド displayControl

フォーム グループ コントロールを表示します。

    public void displayControl()

### <a name="method-gotfocus"></a>メソッド gotFocus

ユーザーがフォーム グループ コントロールにフォーカスを移すタイミングを指定します。

    public void gotFocus()

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、gotFocus をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム グループ コントロールの列の高さと幅を指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
列の高さを指定する整数値。

<!-- -->

height  
列の高さを指定する整数値。

### <a name="method-dragleave"></a>メソッド dragLeave

ユーザーがフォーム グループ コントロールの境界からオブジェクトをドラッグすると呼び出されます。

    public void dragLeave()

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、dragLeave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-enter"></a>メソッド enter

ユーザーがフォーム グループ コントロールにフォーカスを移動すると呼び出されます。

    public void enter()

#### <a name="remarks"></a>備考

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、enter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

### <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a>パラメーター

x  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

y  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

ボタン  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

Ctrl  
Shift キーが押されているかどうかを指定するブール値。

<!-- -->

シフト  
Shift キーが押されているかどうかを指定するブール値。

#### <a name="remarks"></a>備考

button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseEnter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="class-formguidcontrol"></a>クラス FormGuidControl
    class FormGuidControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                                                         |
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
| public int charFromPos(int x, int y)                                                                        |                                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public int dataFieldArrayIndex()                                                                            |                                                                                                                                                                         |
| public FieldName dataFieldName()                                                                            |                                                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int direction(\[int value\])                                                                         |                                                                                                                                                                         |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public container getCursorPos()                                                                             |                                                                                                                                                                         |
| public int getFirstVisibleLine()                                                                            |                                                                                                                                                                         |
| public str getLine(int lineNo)                                                                              |                                                                                                                                                                         |
| public int getLineCount()                                                                                   |                                                                                                                                                                         |
| public container getSelection()                                                                             |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                                                         |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
| public boolean isValid()                                                                                    |                                                                                                                                                                         |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
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
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                                                         |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                                                         |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                                                         |
| public int lineFromChar(int charIndex)                                                                      |                                                                                                                                                                         |
| public int lineIndex(int lineNo)                                                                            |                                                                                                                                                                         |
| public int lineLength(int lineNo)                                                                           |                                                                                                                                                                         |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                                                         |
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
| public container posFromChar(int charIndex)                                                                 |                                                                                                                                                                         |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                                                         |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                                                         |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                                                         |
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
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                                                     |
| public boolean SysObsoleteAttribute(container data)                                                         |                                                                                                                                                                         |
| public int userData(\[int value\])                                                                          | コントロールのユーザー データを取得または設定します。                                                                                                                             |
| public int userDataItem(\[int value\])                                                                      | コントロールのユーザー データ品目を取得または設定します。                                                                                                                        |
| public int userDataItems(\[int value\])                                                                     | コントロールのユーザー データ項目の数を取得または設定します。                                                                                                             |
| public int userDisable(\[int value\])                                                                       | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                                     |
| public int userFastTabSummary(\[int value\])                                                                |                                                                                                                                                                         |
| public int userHeight(\[int value\])                                                                        | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                                                    |
| public int userHide(\[int value\])                                                                          | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                                      |
| public int userOrgContainer(\[int value\])                                                                  | コントロールの組織コンテナを取得または設定します。                                                                                                                |
| public int userOrgSibling(\[int value\])                                                                    | コントロールの組織兄弟を取得または設定します。                                                                                                                  |
| public str userPromptText(\[str value\])                                                                    | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                                       |
| public int userSecurityLevel(\[int value\])                                                                 | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                                                   |
| public int userSkip(\[int value\])                                                                          | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。                    |
| public int userWidth(\[int value\])                                                                         | ピクセル単位でコントロールの幅を設定するか返します。                                                                                                                     |
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public Guid value(\[Guid value\])                                                                           |                                                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void setCursorPos(int x, int y)                                                                      |                                                                                                                                                                         |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])       |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void undo()                                                                                          |                                                                                                                                                                         |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void lineScroll(int dx, int dy)                                                                      |                                                                                                                                                                         |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void performFormLookup(xFormRun form)                                                                |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void scrollCursor()                                                                                  |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void setSelection(int charIndexFrom, int charIndexTo)                                                |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void pasteText(str pasteStr, \[boolean InsertSel\])                                                  |                                                                                                                                                                         |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])         |                                                                                                                                                                         |
| public void textChange()                                                                                    |                                                                                                                                                                         |
| public void lookup()                                                                                        |                                                                                                                                                                         |

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
プロパティに割り当てる値。

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

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-charfrompos"></a>メソッド charFromPos

    public int charFromPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

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

### <a name="method-datafieldarrayindex"></a>メソッド dataFieldArrayIndex

    public int dataFieldArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-datafieldname"></a>メソッド dataFieldName

    public FieldName dataFieldName()

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

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

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

### <a name="method-getcursorpos"></a>メソッド getCursorPos

    public container getCursorPos()

#### <a name="return-value"></a>戻り値

### <a name="method-getfirstvisibleline"></a>メソッド getFirstVisibleLine

    public int getFirstVisibleLine()

#### <a name="return-value"></a>戻り値

### <a name="method-getline"></a>メソッド getLine

    public str getLine(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-getlinecount"></a>メソッド getLineCount

    public int getLineCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getselection"></a>メソッド getSelection

    public container getSelection()

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

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

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
コントロールに要求されているカスタマイズのレベルを指定する FormAllowUserSetup 列挙値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。 「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメータで指定されたレベル以上である必要があります。

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

### <a name="method-limittext"></a>メソッド limitText

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextmode"></a>メソッド limitTextMode

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextvalue"></a>メソッド limitTextValue

    public int limitTextValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linefromchar"></a>メソッド lineFromChar

    public int lineFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-lineindex"></a>メソッド lineIndex

    public int lineIndex(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-linelength"></a>メソッド lineLength

    public int lineLength(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupbutton"></a>メソッド lookupButton

    public int lookupButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-posfromchar"></a>メソッド posFromChar

    public container posFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

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

### <a name="method-replaceonlookup"></a>メソッド replaceOnLookup

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchafterinput"></a>メソッド searchAfterInput

    public int searchAfterInput([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchmode"></a>メソッド searchMode

    public int searchMode([int value])

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

### <a name="method-userfasttabsummary"></a>メソッド userFastTabSummary

    public int userFastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public Guid value([Guid value])

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

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-setcursorpos"></a>メソッド setCursorPos

    public void setCursorPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

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

### <a name="method-performdblookup"></a>メソッド performDBLookup

    public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

tableId  

<!-- -->

会社  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-linescroll"></a>メソッド lineScroll

    public void lineScroll(int dx, int dy)

#### <a name="parameters"></a>パラメーター

dx  

<!-- -->

dy  

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-performformlookup"></a>メソッド performFormLookup

    public void performFormLookup(xFormRun form)

#### <a name="parameters"></a>パラメーター

フォーム  

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

### <a name="method-scrollcursor"></a>メソッド scrollCursor

    public void scrollCursor()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-setselection"></a>メソッド setSelection

    public void setSelection(int charIndexFrom, int charIndexTo)

#### <a name="parameters"></a>パラメーター

charIndexFrom  

<!-- -->

charIndexTo  

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

### <a name="method-pastetext"></a>メソッド pasteText

    public void pasteText(str pasteStr, [boolean InsertSel])

#### <a name="parameters"></a>パラメーター

pasteStr  

<!-- -->

InsertSel  

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-performtypelookup"></a>メソッド performTypeLookup

    public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

userType  

<!-- -->

arrayIndex  

<!-- -->

会社  

### <a name="method-textchange"></a>メソッド textChange

    public void textChange()

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

## <a name="class-formhtmlcontrol"></a>クラス FormHTMLControl
    class FormHTMLControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public boolean allowSysSetup()                                                                              | SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。                                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                                                      |
| public int beginDrag(int x, int y)                                                                          | ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。                                                                                                                  |
| public container calcControlSize(int chars, int lines)                                                      | コントロールのサイズを取得します。                                                                                                                                      |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                                                 |
| public str className(\[str value\])                                                                         |                                                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public str custom(\[str value\])                                                                            |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public AnyType dispatch(VarArg )                                                                            |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public COMError error()                                                                                     |                                                                                                                                                                         |
| public str getText()                                                                                        |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public ComInterface interface()                                                                             |                                                                                                                                                                         |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
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
| public str processPicture(str picture)                                                                      |                                                                                                                                                                         |
| public boolean rTLCapable(\[boolean value\])                                                                |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
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
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      | フォームのコントロールの垂直スペーシング モードを設定します。                                                                                                             |
| public int verticalSpacingValue(\[int value\])                                                              | フォームのコントロールの上下の間隔を取得または設定します。                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                                                  |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void insertText(str Text, \[NoYes repaint\])                                                         |                                                                                                                                                                         |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void processBase(str base)                                                                           |                                                                                                                                                                         |
| public void setFont(int fontid, HtmlFont htmlFont, \[NoYes repaint\])                                       |                                                                                                                                                                         |
| public void getFont(int fontid, HtmlFont htmlFont)                                                          |                                                                                                                                                                         |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void updateSize()                                                                                    |                                                                                                                                                                         |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void processLink(str link)                                                                           |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void processTitle(str title)                                                                         |                                                                                                                                                                         |
| public void read(str FileName, \[str TagName\])                                                             |                                                                                                                                                                         |
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| public void setText(str Text, \[str TagName\])                                                              |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void save(str FileName)                                                                              |                                                                                                                                                                         |
| public void command(int command)                                                                            |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void insertLink(str Text, str Url, str Name, \[NoYes repaint\])                                      |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void clearWindow()                                                                                   |                                                                                                                                                                         |
| public void processForm(int formHandle)                                                                     |                                                                                                                                                                         |
| public void setMargin(int Left, int Right, int Top, int Bottom, \[NoYes repaint\])                          |                                                                                                                                                                         |

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

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-classname"></a>メソッド className

    public str className([str value])

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

### <a name="method-custom"></a>メソッド custom

    public str custom([str value])

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

### <a name="method-dispatch"></a>メソッド dispatch

    public AnyType dispatch(VarArg )

#### <a name="parameters"></a>パラメーター



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
コントロールが有効かどうかを指定するブール値; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-error"></a>メソッド error

    public COMError error()

#### <a name="return-value"></a>戻り値

### <a name="method-gettext"></a>メソッド getText

    public str getText()

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
高さをピクセル単位で指定する整数。オプション。

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

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

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
コントロールに要求されているカスタマイズのレベルを指定する FormAllowUserSetup 列挙値。

#### <a name="return-value"></a>戻り値

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。 「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメータで指定されたレベル以上である必要があります。

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

### <a name="method-processpicture"></a>メソッド processPicture

    public str processPicture(str picture)

#### <a name="parameters"></a>パラメーター

picture  

#### <a name="return-value"></a>戻り値

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

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

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
幅の計算方法を示す整数。オプション。

<!-- -->

モード  
幅の計算方法を示す整数。オプション。

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
幅をピクセル単位で指定する整数。オプション。

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-inserttext"></a>メソッド insertText

    public void insertText(str Text, [NoYes repaint])

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

repaint  

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-processbase"></a>メソッド processBase

    public void processBase(str base)

#### <a name="parameters"></a>パラメーター

基本  

### <a name="method-setfont"></a>メソッド setFont

    public void setFont(int fontid, HtmlFont htmlFont, [NoYes repaint])

#### <a name="parameters"></a>パラメーター

fontid  

<!-- -->

htmlFont  

<!-- -->

repaint  

### <a name="method-getfont"></a>メソッド getFont

    public void getFont(int fontid, HtmlFont htmlFont)

#### <a name="parameters"></a>パラメーター

fontid  

<!-- -->

htmlFont  

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

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

### <a name="method-updatesize"></a>メソッド updateSize

    public void updateSize()

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

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-processlink"></a>メソッド processLink

    public void processLink(str link)

#### <a name="parameters"></a>パラメーター

リンク  

### <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム コントロールの最適な列の幅と高さを指定します。

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  
コントロールの適切な高さです。

<!-- -->

height  
コントロールの適切な高さです。

### <a name="method-processtitle"></a>メソッド processTitle

    public void processTitle(str title)

#### <a name="parameters"></a>パラメーター

title  

### <a name="method-read"></a>メソッド read

    public void read(str FileName, [str TagName])

#### <a name="parameters"></a>パラメーター

FileName  

<!-- -->

TagName  

### <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

    public void setFocus()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-settext"></a>メソッド setText

    public void setText(str Text, [str TagName])

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

TagName  

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

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

### <a name="method-save"></a>メソッド save

    public void save(str FileName)

#### <a name="parameters"></a>パラメーター

FileName  

### <a name="method-command"></a>メソッド command

    public void command(int command)

#### <a name="parameters"></a>パラメーター

command  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-insertlink"></a>メソッド insertLink

    public void insertLink(str Text, str Url, str Name, [NoYes repaint])

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

URL  

<!-- -->

氏名  

<!-- -->

repaint  

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-clearwindow"></a>メソッド clearWindow

    public void clearWindow()

### <a name="method-processform"></a>メソッド processForm

    public void processForm(int formHandle)

#### <a name="parameters"></a>パラメーター

formHandle  

### <a name="method-setmargin"></a>メソッド setMargin

    public void setMargin(int Left, int Right, int Top, int Bottom, [NoYes repaint])

#### <a name="parameters"></a>パラメーター

左  

<!-- -->

右  

<!-- -->

上  

<!-- -->

下  

<!-- -->

repaint  

## <a name="class-formintcontrol"></a>クラス FormIntControl
    class FormIntControl extends FormControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                                     |
| public int allowNegative(\[int value\])                                                                     |                                                                                                                                                                         |
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
| public int charFromPos(int x, int y)                                                                        |                                                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                                                     |
| public List configurationKeyEx()                                                                            | コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。                                                                        |
| public str countryRegionCodes(\[str value\])                                                                | コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。                                                                                          |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public int dataFieldArrayIndex()                                                                            |                                                                                                                                                                         |
| public FieldName dataFieldName()                                                                            |                                                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  | DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                                                       |
| public int direction(\[int value\])                                                                         |                                                                                                                                                                         |
| public int displaceNegative(\[int value\], \[AutoMode mode\])                                               |                                                                                                                                                                         |
| public AutoMode displaceNegativeMode(\[AutoMode mode\])                                                     |                                                                                                                                                                         |
| public int displaceNegativeValue(\[int value\])                                                             |                                                                                                                                                                         |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     | Finance and Operations クライアント、Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。 |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                                                       |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                           | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。                                                                          |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                               | マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。                                                                        |
| public str dragText()                                                                                       | フォーム コントロールをドラッグしたときに表示されるテキストを取得します。                                                                                                  |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                                                     |
| public container getCursorPos()                                                                             |                                                                                                                                                                         |
| public int getFirstVisibleLine()                                                                            |                                                                                                                                                                         |
| public str getLine(int lineNo)                                                                              |                                                                                                                                                                         |
| public int getLineCount()                                                                                   |                                                                                                                                                                         |
| public container getSelection()                                                                             |                                                                                                                                                                         |
| public boolean hasChanged(\[boolean val\])                                                                  | コントロールの内容が変更されたかどうかを示す値を設定するか返します。                                                                                |
| public boolean hasUserSetting()                                                                             | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                                                 |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを取得します。                                                                                                                                |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                                                |
| public str hierarchyParent(\[str value\])                                                                   | コントロールの HierarchyParent プロパティ値を取得または設定します。                                                                                                         |
| public int hWnd()                                                                                           | コントロールの Windows ハンドルを取得します。                                                                                                                           |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                                                         |
| public boolean isContainer()                                                                                |                                                                                                                                                                         |
| public boolean isDisplayed()                                                                                | コントロールが表示されるかどうかを示す値を取得します。                                                                                                      |
| public boolean isRestricted()                                                                               | コントロールが制限されるかどうかを示す値を取得します。                                                                                                     |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                    | コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。                                                                     |
| public boolean isValid()                                                                                    |                                                                                                                                                                         |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                                                         |
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
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                                                         |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                                                         |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                                                         |
| public int lineFromChar(int charIndex)                                                                      |                                                                                                                                                                         |
| public int lineIndex(int lineNo)                                                                            |                                                                                                                                                                         |
| public int lineLength(int lineNo)                                                                           |                                                                                                                                                                         |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                                                         |
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
| public container posFromChar(int charIndex)                                                                 |                                                                                                                                                                         |
| public str previewPartRef(\[str value\])                                                                    |                                                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                                                         |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                                                         |
| public int rotateSign(\[int value\])                                                                        |                                                                                                                                                                         |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                                                         |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   | コントロールのセキュリティ キーの ID を設定するか返します。                                                                                                             |
| public int showContextMenu(int menuHandle)                                                                  | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                                                         |
| public int showZero(\[int value\])                                                                          |                                                                                                                                                                         |
| public int signDisplay(\[int value\])                                                                       |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。                                         |
| public int sort(\[SortOrder sortDirection\])                                                                |                                                                                                                                                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                                                         |
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
| public int userFastTabSummary(\[int value\])                                                                |                                                                                                                                                                         |
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
| public void setFocus()                                                                                      | コントロールにフォーカスを設定します。                                                                                                                                          |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                               | ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。                                                                                                  |
| private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                 |                                                                                                                                                                         |
| public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])         |                                                                                                                                                                         |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                   | ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。                                                                      |
| public void endDrag()                                                                                       | ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。                                                                                                           |
| public void textChange()                                                                                    |                                                                                                                                                                         |
| public void pasteText(str pasteStr, \[boolean InsertSel\])                                                  |                                                                                                                                                                         |
| public void lookup()                                                                                        |                                                                                                                                                                         |
| public void mouseLeave()                                                                                    | マウス ポインターがコントロールを離れたことを示します。                                                                                                                  |
| public void scrollCursor()                                                                                  |                                                                                                                                                                         |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])                               |                                                                                                                                                                         |
| public void context()                                                                                       | コントロールのショートカット メニューを表示します。                                                                                                                                |
| public void setSelection(int charIndexFrom, int charIndexTo)                                                |                                                                                                                                                                         |
| public void inputSearch(str searchStr)                                                                      | 指定した文字列を基に、コントロールのデータ フィルター処理を実行します。                                                                                                 |
| public void enter()                                                                                         |                                                                                                                                                                         |
| public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])       |                                                                                                                                                                         |
| private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])                                    |                                                                                                                                                                         |
| public void displayControl()                                                                                | コントロールを表示します。                                                                                                                                                   |
| public void filter(\[str filterStr\])                                                                       |                                                                                                                                                                         |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                       | ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。                                                                    |
| public void copy()                                                                                          | コントロールの内容をクリップボードにコピーします。                                                                                                                    |
| public void gotFocus()                                                                                      | コントロールがフォーカスを受信したことを示します。                                                                                                                          |
| public void undo()                                                                                          |                                                                                                                                                                         |
| public void resetUserSetting()                                                                              | コントロールのユーザー設定をリセットします。                                                                                                                               |
| public void setCursorPos(int x, int y)                                                                      |                                                                                                                                                                         |
| public void lineScroll(int dx, int dy)                                                                      |                                                                                                                                                                         |
| public void dragLeave()                                                                                     | マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。                                                                        |
| private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])                                  |                                                                                                                                                                         |
| public void paste()                                                                                         | クリップボードの内容をコントロールに貼り付けます。                                                                                                                  |
| public void cut()                                                                                           | コントロールのコンテンツを切り取りします。                                                                                                                                       |
| public void performFormLookup(xFormRun form)                                                                |                                                                                                                                                                         |
| private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])                                |                                                                                                                                                                         |
| private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])                                   |                                                                                                                                                                         |
| public void prefColumnSize(int width, int height)                                                           | フォーム コントロールの最適な列の幅と高さを指定します。                                                                                                   |
| public void lostFocus()                                                                                     | コントロールがフォーカスを失ったことを示します。                                                                                                                              |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allownegative"></a>メソッド allowNegative

    public int allowNegative([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-charfrompos"></a>メソッド charFromPos

    public int charFromPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

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

### <a name="method-datafieldarrayindex"></a>メソッド dataFieldArrayIndex

    public int dataFieldArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-datafieldname"></a>メソッド dataFieldName

    public FieldName dataFieldName()

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

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegative"></a>メソッド displaceNegative

    public int displaceNegative([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegativemode"></a>メソッド displaceNegativeMode

    public AutoMode displaceNegativeMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegativevalue"></a>メソッド displaceNegativeValue

    public int displaceNegativeValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-getcursorpos"></a>メソッド getCursorPos

    public container getCursorPos()

#### <a name="return-value"></a>戻り値

### <a name="method-getfirstvisibleline"></a>メソッド getFirstVisibleLine

    public int getFirstVisibleLine()

#### <a name="return-value"></a>戻り値

### <a name="method-getline"></a>メソッド getLine

    public str getLine(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-getlinecount"></a>メソッド getLineCount

    public int getLineCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getselection"></a>メソッド getSelection

    public container getSelection()

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

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

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

「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。 次のテーブルでは、neededSetupRights パラメーターの値について説明します。

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

### <a name="method-limittext"></a>メソッド limitText

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextmode"></a>メソッド limitTextMode

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextvalue"></a>メソッド limitTextValue

    public int limitTextValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linefromchar"></a>メソッド lineFromChar

    public int lineFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-lineindex"></a>メソッド lineIndex

    public int lineIndex(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-linelength"></a>メソッド lineLength

    public int lineLength(int lineNo)

#### <a name="parameters"></a>パラメーター

lineNo  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupbutton"></a>メソッド lookupButton

    public int lookupButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-posfromchar"></a>メソッド posFromChar

    public container posFromChar(int charIndex)

#### <a name="parameters"></a>パラメーター

charIndex  

#### <a name="return-value"></a>戻り値

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

### <a name="method-replaceonlookup"></a>メソッド replaceOnLookup

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rotatesign"></a>メソッド rotateSign

    public int rotateSign([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchafterinput"></a>メソッド searchAfterInput

    public int searchAfterInput([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchmode"></a>メソッド searchMode

    public int searchMode([int value])

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

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showzero"></a>メソッド showZero

    public int showZero([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-signdisplay"></a>メソッド signDisplay

    public int signDisplay([int value])

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

### <a name="method-userfasttabsummary"></a>メソッド userFastTabSummary

    public int userFastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-onmodified"></a>メソッド OnModified

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-jumpref"></a>メソッド jumpRef

    public void jumpRef()

### <a name="method-ongotfocus"></a>メソッド OnGotFocus

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-performtypelookup"></a>メソッド performTypeLookup

    public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

userType  

<!-- -->

arrayIndex  

<!-- -->

会社  

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

### <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。

    public void endDrag()

#### <a name="remarks"></a>備考

DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。 コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。

### <a name="method-textchange"></a>メソッド textChange

    public void textChange()

### <a name="method-pastetext"></a>メソッド pasteText

    public void pasteText(str pasteStr, [boolean InsertSel])

#### <a name="parameters"></a>パラメーター

pasteStr  

<!-- -->

InsertSel  

### <a name="method-lookup"></a>メソッド lookup

    public void lookup()

### <a name="method-mouseleave"></a>メソッド mouseLeave

マウス ポインターがコントロールを離れたことを示します。

    public void mouseLeave()

### <a name="method-scrollcursor"></a>メソッド scrollCursor

    public void scrollCursor()

### <a name="method-onlostfocus"></a>メソッド OnLostFocus

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-context"></a>メソッド context

コントロールのショートカット メニューを表示します。

    public void context()

### <a name="method-setselection"></a>メソッド setSelection

    public void setSelection(int charIndexFrom, int charIndexTo)

#### <a name="parameters"></a>パラメーター

charIndexFrom  

<!-- -->

charIndexTo  

### <a name="method-inputsearch"></a>メソッド inputSearch

指定した文字列を基に、コントロールのデータ フィルター処理を実行します。

    public void inputSearch(str searchStr)

#### <a name="parameters"></a>パラメーター

searchStr  
データのフィルタリングに使用する文字列値 (オプション)。

### <a name="method-enter"></a>メソッド enter

    public void enter()

### <a name="method-performdblookup"></a>メソッド performDBLookup

    public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

tableId  

<!-- -->

会社  

### <a name="method-onenter"></a>メソッド OnEnter

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-displaycontrol"></a>メソッド displayControl

コントロールを表示します。

    public void displayControl()

### <a name="method-filter"></a>メソッド filter

    public void filter([str filterStr])

#### <a name="parameters"></a>パラメーター

filterStr  

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

### <a name="method-copy"></a>メソッド copy

コントロールの内容をクリップボードにコピーします。

    public void copy()

### <a name="method-gotfocus"></a>メソッド gotFocus

コントロールがフォーカスを受信したことを示します。

    public void gotFocus()

### <a name="method-undo"></a>メソッド undo

    public void undo()

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

### <a name="method-setcursorpos"></a>メソッド setCursorPos

    public void setCursorPos(int x, int y)

#### <a name="parameters"></a>パラメーター

x  

<!-- -->

y  

### <a name="method-linescroll"></a>メソッド lineScroll

    public void lineScroll(int dx, int dy)

#### <a name="parameters"></a>パラメーター

dx  

<!-- -->

dy  

### <a name="method-dragleave"></a>メソッド dragLeave

マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。

    public void dragLeave()

### <a name="method-onleaving"></a>メソッド OnLeaving

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-paste"></a>メソッド paste

クリップボードの内容をコントロールに貼り付けます。

    public void paste()

### <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

    public void cut()

### <a name="method-performformlookup"></a>メソッド performFormLookup

    public void performFormLookup(xFormRun form)

#### <a name="parameters"></a>パラメーター

フォーム  

### <a name="method-onvalidated"></a>メソッド OnValidated

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-onlookup"></a>メソッド OnLookup

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

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

### <a name="method-lostfocus"></a>メソッド lostFocus

コントロールがフォーカスを失ったことを示します。

    public void lostFocus()

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  





