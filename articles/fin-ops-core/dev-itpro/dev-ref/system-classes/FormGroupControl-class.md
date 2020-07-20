---
title: FormGroupControl クラス
description: このトピックでは、FormGroupControl クラスについて説明します。
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
ms.openlocfilehash: df8a5376ecadfa5b98f51bee3506e175e2727d26
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502942"
---
# <a name="class-formgroupcontrol"></a>クラス FormGroupControl

[!include [banner](../../includes/banner.md)]


```xpp
class FormGroupControl extends FormControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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
| public int displayTarget(\[int value\])                                                                             | クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。                             |
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

## <a name="method-addcontrol"></a>メソッド addControl

フォーム グループ コントロールにフォームのコントロールを追加します。

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a>パラメーター - addControl

controlType  
コントロールの位置を示す値、オプション。 既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。

<!-- -->

controlName  
コントロールの位置を示す値、オプション。 既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。

<!-- -->

insertAfter  
コントロールの位置を示す値、オプション。 既定値は、nullNothingnullptrunita null 参照 (Visual Basic にはない) です。

### <a name="return-value---addcontrol"></a>戻り値 - addControl

フォーム コントロールを構成する FormControl オブジェクト。

## <a name="method-addcontrolex"></a>メソッド addControlEx

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a>パラメーター - addControlEx

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

### <a name="return-value---addcontrolex"></a>戻り値 - addControlEx

## <a name="method-adddatafield"></a>メソッド addDataField

テーブル フィールドを追加します。

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a>パラメーター - addDataField

dataSourceId  

<!-- -->

fieldId  

<!-- -->

insertAfter  

<!-- -->

arrayIndex  

### <a name="return-value---adddatafield"></a>戻り値 - addDataField

フォーム コントロールを変更する FormControl オブジェクト。

## <a name="method-alignchild"></a>メソッド alignChild

フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値を設定するか返します。

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a>パラメーター - alignChild

値  
フォーム グループ コントロールが、フォーム内の他のコントロールと同じ方法で一致しているかどうかを示すブール値; オプション。

### <a name="return-value---alignchild"></a>戻り値 - alignChild

コントロールがアラインされた場合は true。それ以外の場合は false。

## <a name="method-alignchildren"></a>メソッド alignChildren

子コントロールが一致しているかどうかを示すブール値を設定するか返します。

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a>パラメーター - alignChildren

値  
子コントロールが一致しているかどうかを示すブール値; オプション。

### <a name="return-value---alignchildren"></a>戻り値 - alignChildren

子コントロールがアラインされた場合は true。それ以外の場合は false。

## <a name="method-aligncontrol"></a>メソッド alignControl

コントロールが他のコントロールと揃っているかどうかを決定します。

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a>パラメーター - alignControl

値  
フォーム グループ コントロールが他のコントロールと一致しているかどうかを示すブール値。

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
データを変更できるかどうかを示すブール値; オプション。

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

## <a name="method-allowusersetup"></a>メソッド allowUserSetup

フォーム グループ コントロールに実行できる変更のレベルを取得または設定します。

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a>パラメーター - allowUserSetup

値  
実行可能な変更のレベルを示す整数データ型です (オプション)。

### <a name="return-value---allowusersetup"></a>戻り値 - allowUserSetup

実行可能な変更のレベルを示す整数値。

### <a name="remarks---allowusersetup"></a>備考 - allowUserSetup

値パラメーターのために FormAllowUserSetup 列挙型値を使用することができます。

## <a name="method-arrangeguide"></a>メソッド arrangeGuide

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a>パラメーター - arrangeGuide

値  

### <a name="return-value---arrangeguide"></a>戻り値 - arrangeGuide

## <a name="method-arrangemethod"></a>メソッド arrangeMethod

フォーム グループ コントロールのコントロールを配置する方法を示す整数値を設定するか返します。

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a>パラメーター - arrangeMethod

値  
フォーム グループ コントロールのコントロールを配置する方法を示す整数値。オプション。

### <a name="return-value---arrangemethod"></a>戻り値 - arrangeMethod

フォーム グループ コントロールのコントロールを配置する方法を示す整数値。

### <a name="remarks---arrangemethod"></a>備考 - arrangeMethod

\_value パラメーターのために ArrangeMethod 列挙型値を使用することができます。

## <a name="method-arrangewhen"></a>メソッド arrangeWhen

コントロールが配置されるタイミングを指定する整数値を設定するか返します。

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a>パラメーター - arrangeWhen

値  
コントロールが配置されるタイミングを指定する整数値。オプション。

### <a name="return-value---arrangewhen"></a>戻り値 - arrangeWhen

コントロールが配置されるタイミングを指定する整数値。

## <a name="method-autodatagroup"></a>メソッド autoDataGroup

フォーム グループ コントロールに、コントロールに対して指定されているデータ グループ内のフィールドのみ含めることができるかどうかを指定するブール値を設定するか返します。

```xpp
public boolean autoDataGroup([boolean value])
```

### <a name="parameters---autodatagroup"></a>パラメーター - autoDataGroup

値  
フォーム グループ コントロールがデータ グループ内のフィールドのみを含めることができるかどうかを示すブール値データ型。

### <a name="return-value---autodatagroup"></a>戻り値 - autoDataGroup

フォーム グループ コントロールにデータ グループ内のフィールドのみを含めることができる場合は true。それ以外の場合は、false。

### <a name="remarks---autodatagroup"></a>備考 - autoDataGroup

フォーム グループ コントロールのデータ グループを設定または取得するには、FormGroupControl.dataGroup メソッドを使用します。

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  
フォーム グループ コントロールと同じ名前の変数を、システムが宣言するかどうかを示すブール値; オプション。

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
背景色を指定する整数データ型です (オプション)。

### <a name="return-value---backgroundcolor"></a>戻り値 - backgroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---backgroundcolor"></a>備考 - backgroundColor

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトは 0 (ゼロ) でなければなりません。
-   1 バイトの最大値は 255 です。

## <a name="method-backgroundimage"></a>メソッド backgroundImage

フォーム グループ コントロールの背景イメージを指定します。

```xpp
public Image backgroundImage([Image image], [int drawMode])
```

### <a name="parameters---backgroundimage"></a>パラメーター - backgroundImage

画像  
画像の描画方法を指定する整数データ型です (オプション)。

<!-- -->

drawMode  
画像の描画方法を指定する整数データ型です (オプション)。

### <a name="return-value---backgroundimage"></a>戻り値 - backgroundImage

イメージ オブジェクトです。

## <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a>パラメーター - backStyle

値  
背景スタイル示す整数データ型です (オプション)。

### <a name="return-value---backstyle"></a>戻り値 - backStyle

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

## <a name="method-begindrag"></a>メソッド beginDrag

ユーザーがフォーム グループ コントロールの移動を始めると呼び出されます。

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a>パラメーター - beginDrag

x  
移動イベントの y 座標を示す整数値。

<!-- -->

y  
移動イベントの y 座標を示す整数値。

### <a name="return-value---begindrag"></a>戻り値 - beginDrag

イベントが処理された場合は 0 (ゼロ) です。

## <a name="method-bold"></a>メソッド bold

コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a>パラメーター - bold

値  
フォントの太さを指定する整数値。オプション。

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

## <a name="method-bottommargin"></a>メソッド bottomMargin

フォーム グループ コントロールの下余白をピクセル単位で設定するか返し、余白が自動的に調整されるかどうかを指定します。

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a>パラメーター - bottomMargin

値  
下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---bottommargin"></a>戻り値 - bottomMargin

ピクセル単位の下余白を指定する整数データ型値です。

## <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

下余白が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a>パラメーター - bottomMarginMode

モード  
下余白が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---bottommarginmode"></a>戻り値 - bottomMarginMode

フォント サイズなどの他のフォーム設定に基づいて余白が自動的に調整される場合は AutoMode::Auto です。それ以外の場合は、AutoMode::Fixed です。

## <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

フォーム グループ コントロールの下余白をピクセル単位で設定するか返します。

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a>パラメーター - bottomMarginValue

値  
ピクセルの下余白を指定する整数データ型です (オプション)。

### <a name="return-value---bottommarginvalue"></a>戻り値 - bottomMarginValue

ピクセル単位の下余白を指定する整数データ型値です。

## <a name="method-breakable"></a>メソッド breakable

```xpp
public boolean breakable([boolean value])
```

### <a name="parameters---breakable"></a>パラメーター - breakable

値  

### <a name="return-value---breakable"></a>戻り値 - breakable

## <a name="method-calccontrolsize"></a>メソッド calcControlSize

文字数と明細行数に基づいて、フォーム グループ コントロールのフォント サイズを計算します。

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

フォーム グループ コントロールのサイズを指定するコンテナー データ型値。

## <a name="method-canadddatafield"></a>メソッド canAddDataField

テーブル フィールドを追加できるかどうかを示します。

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a>パラメーター - canAddDataField

dataSourceId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

### <a name="return-value---canadddatafield"></a>戻り値 - canAddDataField

テーブルを追加できる場合は true。それ以外の場合は、false。

## <a name="method-cancontain"></a>メソッド canContain

フォーム グループ コントロールに指定されたフォーム コントロールを含めることができるかどうかを指定します。

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a>パラメーター - canContain

control  
フォーム コントロールを指定する FormControl オブジェクト。

### <a name="return-value---cancontain"></a>戻り値 - canContain

フォーム グループ コントロールに指定フォーム コントロールを含めることができる場合は true。それ以外の場合は、false。

## <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a>パラメーター - caption

値  
キャプション テキストを指定する文字列データ型; オプション。

### <a name="return-value---caption"></a>戻り値 - caption

コントロールのキャプションとして使用される文字列。

## <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a>パラメーター - characterSet

値  
テキスト フォントの文字セットを指定する整数データ型です (オプション)。

### <a name="return-value---characterset"></a>戻り値 - characterSet

フォントの文字セット示す整数値。

### <a name="remarks---characterset"></a>備考 - characterSet

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

## <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a>パラメーター - colorScheme

値  
フォーム グループ コントロールのカラー パレットを指定する整数データ型です (オプション)。

### <a name="return-value---colorscheme"></a>戻り値 - colorScheme

0 (ゼロ) から 2 までの整数。

### <a name="remarks---colorscheme"></a>備考 - colorScheme

配色は次の表に従って定義されます。

| 先頭値 | スタイル                  |
|-------|------------------------|
| 0     | 既定。               |
| 1     | Windows パレット。   |
| 2     | 真の配色。 |

## <a name="method-columns"></a>メソッド columns

フォーム グループ コントロールの列の数をピクセル単位で設定するか返し、数が自動的に調整されるかどうかを指定します。

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a>パラメーター - columns

値  
列数が固定されているかどうか、またはフォーム サイズなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
列数が固定されているかどうか、またはフォーム サイズなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---columns"></a>戻り値 - columns

フォーム グループ コントロール内の列数をピクセル単位で指定する整数値。

## <a name="method-columnsmode"></a>メソッド columnsMode

フォーム グループ コントロール内の列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a>パラメーター - columnsMode

モード  
列数が固定されているかどうか、またはフォーム サイズなどのオプション、他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---columnsmode"></a>戻り値 - columnsMode

列の数が自動的に調整される場合は Automode::Auto、それ以外の場合は Automode::Fixed となります。

## <a name="method-columnspace"></a>メソッド columnspace

フォーム グループ コントロール内の列間のスペースの量をピクセル単位で設定するか返し、フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整されるかどうかを示します。

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a>パラメーター - columnspace

値  
列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---columnspace"></a>戻り値 - columnspace

フォーム グループ コントロール内の列の間のスペースをピクセル単位で指定する整数値。

## <a name="method-columnspacemode"></a>メソッド columnspaceMode

フォーム グループ コントロール内の列間のスペースの量が自動的に調整されるかどうかを示す AutoMode 列挙値を設定するか返します。

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a>パラメーター - columnspaceMode

モード  
列の間にスペースの量が固定されているかどうか、またはフォント サイズ、オプションなどの他のフォーム設定に基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---columnspacemode"></a>戻り値 - columnspaceMode

容量が自動的に調整される場合は AutoMode::Auto です。それ以外の場合は、AutoMode::Fixed です。

## <a name="method-columnspacevalue"></a>メソッド columnspaceValue

ピクセルでフォーム グループ コントロール内の列間のスペースの量を設定するか返します。

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a>パラメーター - columnspaceValue

値  
ピクセルにフォーム グループ コントロール内の列間のスペース量を指定する整数データ型です (オプション)。

### <a name="return-value---columnspacevalue"></a>戻り値 - columnspaceValue

フォーム グループ コントロール内のピクセル単位で列の間の容量を指定する整数値。

## <a name="method-columnsvalue"></a>メソッド columnsValue

フォーム グループ コントロール内のコントロールの数を設定するか返します。

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a>パラメーター - columnsValue

値  
フォーム グループ コントロールの列数を指定する整数データ型です (オプション)。

### <a name="return-value---columnsvalue"></a>戻り値 - columnsValue

フォーム グループ コントロールの列数を指定する整数データ型値です。

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  
コンフィギュレーション キーの ID を特定する configurationKeyId システム データ型; オプション。

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

## <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a>戻り値 - configurationKeyEx

フォーム グループ コントロールのために有効化されたコンフィギュレーション キーの ID を含むリスト オブジェクト。

### <a name="remarks---configurationkeyex"></a>備考 - configurationKeyEx

リストに重複 ID は含まれません。 コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。 さらに、返されたリストには、拡張データ型に適用される任意のコンフィギュレーション キー ID が含まれます。

## <a name="method-contains"></a>メソッド contains

フォーム グループ コントロールに指定されたフォーム コントロールが含まれるかどうかを指定します。

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a>パラメーター - contains

control  
フォーム コントロールを指定する FormControl オブジェクト。

### <a name="return-value---contains"></a>戻り値 - contains

フォーム グループ コントロールに指定フォーム コントロールが含まれる場合は true。それ以外の場合は、false。

## <a name="method-controlcount"></a>メソッド controlCount

フォーム グループ コントロール内のコントロールの数を返します。

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a>戻り値 - controlCount

フォーム グループ コントロールのコントロールの数を指定する整数データ型値です。

### <a name="remarks---controlcount"></a>備考 - controlCount

FormGroupControl.addControl メソッドを使用することにより、フォーム グループ コントロールに対してコントロールを追加することができます。

## <a name="method-controlnum"></a>メソッド controlNum

フォーム グループ コントロールで指定したコントロールの FormControl オブジェクトを返します。

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a>パラメーター - controlNum

controlNo  
フォーム グループ コントロール内で管理を指定する整数データ型です。

### <a name="return-value---controlnum"></a>戻り値 - controlNum

フォーム コントロールに関する情報を変更および提供するために使用できる FormControl オブジェクト。

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

## <a name="method-datagroup"></a>メソッド dataGroup

フォーム グループ コントロールのデータのグループを設定するか返します。

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a>パラメーター - dataGroup

値  
データ グループを指定する文字列データ型; オプション。

### <a name="return-value---datagroup"></a>戻り値 - dataGroup

データ グループを指定する文字列データ型値。

### <a name="remarks---datagroup"></a>備考 - dataGroup

データ グループは、フォームのデータ ソースであるテーブルのフィールド グループに対応します。

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
ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。

### <a name="return-value---dragdrop"></a>戻り値 - dragDrop

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="remarks---dragdrop"></a>備考 - dragDrop

動作を指定するには、FormGroupControl.dragLeave および FormGroupControl.dragOver メソッドを使用します。 値パラメーターに true または false の値を渡すことができます。

## <a name="method-dragover"></a>メソッド dragOver

オブジェクトがフォーム グループ コントロールの境界上にドラッグされると呼び出されます。

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a>パラメーター - dragOver

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

### <a name="return-value---dragover"></a>戻り値 - dragOver

オブジェクトが移動、コピー、または指定された位置に移動されていないかどうかを示す FormDrag システム列挙値。

### <a name="remarks---dragover"></a>備考 - dragOver

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、dragOver をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

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

## <a name="method-enablechilds"></a>メソッド enableChilds

フォーム グループ コントロールの子コントロールが有効かどうかを指定します。

```xpp
public boolean enableChilds([boolean enable])
```

### <a name="parameters---enablechilds"></a>パラメーター - enableChilds

enable  
子コントロールが有効かどうかを示すブール値; オプション。

### <a name="return-value---enablechilds"></a>戻り値 - enableChilds

子コントロールが有効にされた場合は true。それ以外の場合は false。

## <a name="method-enabled"></a>メソッド enabled

オブジェクトが有効か無効かを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  
フォーム グループ コントロールが有効かどうかを示すブール値; オプション。

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。

## <a name="method-expand"></a>メソッド expand

フォーム グループ コントロールが展開されているかどうかを指定します。

```xpp
public boolean expand([boolean expand])
```

### <a name="parameters---expand"></a>パラメーター - expand

expand  
フォーム グループ コントロールが展開されているかどうかを示すブール値; オプション。

### <a name="return-value---expand"></a>戻り値 - expand

フォーム グループ コントロールが拡張されている場合は true。それ以外の場合は、false。

## <a name="method-font"></a>メソッド font

コントロール内のテキストに使用されるフォントの名前を取得または設定します。

```xpp
public str font([str value])
```

### <a name="parameters---font"></a>パラメーター - font

値  
フォーム グループ コントロール内のテキストのフォントを示す文字列データ型; オプション。

### <a name="return-value---font"></a>戻り値 - font

Tahoma や Verdana など、使用されるべきフォントの名前。

## <a name="method-fontsize"></a>メソッド fontSize

コントロール内のテキストに使用するフォント サイズを取得または設定します。

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a>パラメーター - fontSize

値  
フォーム グループ コントロール内のテキストのフォント サイズをポイントで示す整数値。 オプション。

### <a name="return-value---fontsize"></a>戻り値 - fontSize

ポイント単位のフォントの高さ。

## <a name="method-frameoptionbutton"></a>メソッド frameOptionButton

フォーム グループ コントロールのオプション ボタンを設定するか返します。

```xpp
public int frameOptionButton([int value])
```

### <a name="parameters---frameoptionbutton"></a>パラメーター - frameOptionButton

値  
オプション ボタンのタイプを指定する整数データ型です (オプション)。

### <a name="return-value---frameoptionbutton"></a>戻り値 - frameOptionButton

オプション ボタンのタイプを指定する整数値。

### <a name="remarks---frameoptionbutton"></a>備考 - frameOptionButton

値パラメーターのために FormFrameOptionButton 列挙型値を使用することができます。

## <a name="method-frameposition"></a>メソッド framePosition

フォーム グループ コントロールのフレームの位置を設定するか返します。

```xpp
public int framePosition([int value])
```

### <a name="parameters---frameposition"></a>パラメーター - framePosition

値  
フレームの場所を指定する整数値。オプション。

### <a name="return-value---frameposition"></a>戻り値 - framePosition

フレームの場所を指定する整数値。

## <a name="method-frametype"></a>メソッド frameType

フォーム グループ コントロールのフレーム スタイルを設定するか返します。

```xpp
public int frameType([int value])
```

### <a name="parameters---frametype"></a>パラメーター - frameType

値  
フォーム グループ コントロールのフレーム スタイルを示す整数値。オプション。

### <a name="return-value---frametype"></a>戻り値 - frameType

フォーム グループ コントロールのフレーム スタイルを示す整数値。

### <a name="remarks---frametype"></a>備考 - frameType

値パラメーターのために FormFrameType 列挙型値を使用することができます。

## <a name="method-haschanged"></a>メソッド hasChanged

フォーム グループ コントロールの内容が変更されたかどうかを示すブール値を設定するか返します。

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a>パラメーター - hasChanged

val  
フォーム グループ コントロールの内容が変更されたかどうかを示すブール値; オプション。

### <a name="return-value---haschanged"></a>戻り値 - hasChanged

内容が変更された場合は true。それ以外の場合は、false。

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
```

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

次の例は、正確なピクセル値に基づいてコントロールの高さを調整する heightMode メソッドの呼び出しを示しています。

```xpp
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

次の例は、高さを 5 ピクセルに設定する heightValue メソッドの呼び出しを示しています。

```xpp
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
```

## <a name="method-helpfield"></a>メソッド helpField

フォーム グループ コントロールが選択されている場合にステータス バーに表示されるヘルプ テキストを返します。

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a>戻り値 - helpField

ヘルプ テキストを含む文字列データ型値。

## <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  
ヘルプ テキストを含む文字列データ型値。

### <a name="return-value---helptext"></a>戻り値 - helpText

画面の下部に表示される文字列。

### <a name="remarks---helptext"></a>備考 - helpText

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

## <a name="method-hideifempty"></a>メソッド hideIfEmpty

グループ内のコントロールが表示されないときフォーム グループ コントロールを表示するかどうかを示すブール値を設定または取得します。

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a>パラメーター - hideIfEmpty

値  
フォーム グループ コントロールが表示されているかどうかを示すブール値; オプション。

### <a name="return-value---hideifempty"></a>戻り値 - hideIfEmpty

フォーム グループ コントロールが表示されない場合は true。それ以外の場合は、false。

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

フォーム グループ コントロールのハンドルを返します。

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a>戻り値 - hWnd

ハンドルを指定する整数値。

## <a name="method-iscontainer"></a>メソッド isContainer

フォーム グループ コントロールがコンテナーであるかどうかを示します。

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a>戻り値 - isContainer

フォーム グループ コントロールがコンテナーである場合は true。それ以外の場合は、false。

## <a name="method-isdisplayed"></a>メソッド isDisplayed

フォーム グループ コントロールが表示されるかどうかを示します。

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a>戻り値 - isDisplayed

フォーム グループ コントロールが表示されている場合は true。それ以外の場合は、false。

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

neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。 「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。

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

フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値を設定するか返します。

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a>パラメーター - italic

値  
フォーム グループ コントロールのテキストが斜体であるかどうかを示すブール値; オプション。

### <a name="return-value---italic"></a>戻り値 - italic

テキストが斜体である場合は true。それ以外の場合は false。

## <a name="method-labelbold"></a>メソッド labelBold

フォーム グループ コントロールのラベル テキストのフォントの太さを設定するか返します。

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a>パラメーター - labelBold

値  
ラベル テキストのフォントの太さを指定する整数値。オプション。

### <a name="return-value---labelbold"></a>戻り値 - labelBold

ラベル テキストのフォントの太さを指定する整数値。

### <a name="remarks---labelbold"></a>備考 - labelBold

値パラメーターおよび戻り値の使用可能な値の詳細については、太字のメソッドを参照してください。

## <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

フォーム グループ コントロールのラベル テキストのフォントの文字セットを設定するか返します。

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a>パラメーター - labelCharacterSet

値  
ラベル テキストのフォントの文字セットを指定する整数値。オプション。

### <a name="return-value---labelcharacterset"></a>戻り値 - labelCharacterSet

ラベル テキストのフォントの文字セットを指定する整数データ型値です。

### <a name="remarks---labelcharacterset"></a>備考 - labelCharacterSet

文字セットは、共通の関係を持つアルファベット、数字、およびその他の文字のグループです。 たとえば、特定の国/地域または言語に対して文字セットを使用する可能性があります。 値パラメーターの可能な値の一覧については、characterSet メソッドを参照してください。 可能な戻り値の一覧については、characterSet メソッドを参照してください。

## <a name="method-labelfont"></a>メソッド labelFont

フォーム グループ コントロールのラベル テキストのフォントを設定するか返します。

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a>パラメーター - labelFont

値  
ラベル テキストのフォントを指定する文字列データ型; オプション。

### <a name="return-value---labelfont"></a>戻り値 - labelFont

ラベル テキストのフォントを指定する文字列データ型値。

## <a name="method-labelfontsize"></a>メソッド labelFontSize

フォーム グループ コントロールのラベル テキストのフォント サイズを設定するか返します。

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a>パラメーター - labelFontSize

値  
ラベル テキストのフォント サイズを指定する整数値。オプション。

### <a name="return-value---labelfontsize"></a>戻り値 - labelFontSize

ラベル テキストのフォント サイズを指定する整数値。

## <a name="method-labelitalic"></a>メソッド labelItalic

フォーム グループ コントロールのラベル テキストが斜体であるかどうかを示すブール値データ型を設定するか返します。

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a>パラメーター - labelItalic

値  
ラベル テキストが斜体かどうかを示すブール値; オプション。

### <a name="return-value---labelitalic"></a>戻り値 - labelItalic

ラベル テキストが斜体である場合は true。それ以外の場合は false。

## <a name="method-labelunderline"></a>メソッド labelUnderline

フォーム グループ コントロールのラベル テキストが下線付きであるかどうかを示すブール値データ型を設定するか返します。

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a>パラメーター - labelUnderline

値  
ラベル テキストに下線が引かれているかどうかを示すブール値; オプション。

### <a name="return-value---labelunderline"></a>戻り値 - labelUnderline

ラベル テキストが下線付きである場合は true。それ以外の場合は false。

## <a name="method-leave"></a>メソッド leave

ユーザーがマウス ポインターをフォーム グループ コントロールから離すと呼び出されます。

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a>戻り値 - leave

マウス ポインターがフォーム グループ コントロールの外に移動する場合は true。それ以外の場合は、false。

### <a name="remarks---leave"></a>備考 - leave

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、leave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-left"></a>メソッド left

フォーム グループ コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a>パラメーター - left

値  
位置の計算方法を示す整数値。オプション。

<!-- -->

モード  
位置の計算方法を示す整数値。オプション。

### <a name="return-value---left"></a>戻り値 - left

フォーム グループ コントロールの水平位置をピクセル単位で示す整数値。

### <a name="remarks---left"></a>備考 - left

mode パラメーターは、次の値のいずれかになります。

-   -1 (既定) � 値パラメーターの値が正確に使用される Exact モードを使用します。
-   FormLeft 列挙値。

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
```

## <a name="method-leftmargin"></a>メソッド leftMargin

フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a>パラメーター - leftMargin

値  
左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---leftmargin"></a>戻り値 - leftMargin

フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。

## <a name="method-leftmarginmode"></a>メソッド leftMarginMode

フォーム グループ コントロールの左余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a>パラメーター - leftMarginMode

モード  
左余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---leftmarginmode"></a>戻り値 - leftMarginMode

左余白のサイズが自動的に調整される場合は Automode::Auto、それ以外の場合は Automode::Fixed となります。

## <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

フォーム グループ コントロールの左余白のサイズをピクセル単位で設定するか返します。

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a>パラメーター - leftMarginValue

値  
フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。オプション。

### <a name="return-value---leftmarginvalue"></a>戻り値 - leftMarginValue

フォーム グループ コントロールの左余白のサイズをピクセル単位で指定する整数値。

## <a name="method-leftmode"></a>メソッド leftMode

フォーム グループ コントロールの水平位置を計算する方法を示す値を設定するか返します。

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a>パラメーター - leftMode

値  
水平位置の計算方法を示す整数データ型です。オプションです。

### <a name="return-value---leftmode"></a>戻り値 - leftMode

水平位置の計算方法を示す整数データ型値です。正確なピクセル値、または FormLeft 列挙値は -1 のいずれかになります。

### <a name="examples---leftmode"></a>例 - leftMode

次の例は、正確なピクセル値に基づいて、フォーム グループ コントロールの水平方向位置を計算する leftMode メソッドの呼び出しを示しています。

```xpp
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
```

## <a name="method-leftvalue"></a>メソッド leftValue

フォーム グループ コントロールの水平位置をピクセル単位で設定するか返します。

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a>パラメーター - leftValue

値  
水平位置をピクセル単位で示す整数値。オプション。

### <a name="return-value---leftvalue"></a>戻り値 - leftValue

水平位置をピクセル単位で示す整数値。

### <a name="remarks---leftvalue"></a>備考 - leftValue

正確なピクセル値に左モードが設定されていない限り、水平位置は変更されません。

### <a name="examples---leftvalue"></a>例 - leftValue

次の例は、水平方向の位置を 50 ピクセルに設定する leftValue メソッドの呼び出しを示しています。

```xpp
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

ユーザーがフォーム グループ コントロールをダブルクリックすると呼び出されます。

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a>パラメーター - mouseDblClick

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

### <a name="return-value---mousedblclick"></a>戻り値 - mouseDblClick

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---mousedblclick"></a>備考 - mouseDblClick

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseDblClick をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-mousedown"></a>メソッド mouseDown

ユーザーがフォーム グループ コントロールでマウス ボタンを押すと呼び出されます。

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a>パラメーター - mouseDown

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

### <a name="return-value---mousedown"></a>戻り値 - mouseDown

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---mousedown"></a>備考 - mouseDown

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseDown をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-mousemove"></a>メソッド mouseMove

ユーザーがマウス ポインターをフォーム グループ コントロール上に移動させると呼び出されます。

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a>パラメーター - mouseMove

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

### <a name="return-value---mousemove"></a>戻り値 - mouseMove

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---mousemove"></a>備考 - mouseMove

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 \_button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseMove をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-mouseup"></a>メソッド mouseUp

ユーザーがマウス ボタンをフォーム グループ コントロール上で放すと呼び出されます。

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a>パラメーター - mouseUp

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

### <a name="return-value---mouseup"></a>戻り値 - mouseUp

イベントが処理された場合は 0 (ゼロ) です。

### <a name="remarks---mouseup"></a>備考 - mouseUp

通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。 \_button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseUp をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-movecontrol"></a>メソッド moveControl

指定されたコントロールを移動します。

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a>パラメーター - moveControl

controlId  
指定されたコントロールが後で挿入されるコントロールを示す整数値。オプション。

<!-- -->

insertAfterId  
指定されたコントロールが後で挿入されるコントロールを示す整数値。オプション。

### <a name="return-value---movecontrol"></a>戻り値 - moveControl

コントロール ID を指定する整数データ型値です。

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

## <a name="method-optionvalue"></a>メソッド optionValue

フォーム グループ コントロールに関連付けられているオプション ボタンの値を設定するか返します。

```xpp
public int optionValue([int value])
```

### <a name="parameters---optionvalue"></a>パラメーター - optionValue

値  
オプション ボタンの値を指定する整数値。オプション。

### <a name="return-value---optionvalue"></a>戻り値 - optionValue

オプション ボタンの値を指定する整数値。

### <a name="remarks---optionvalue"></a>備考 - optionValue

フォーム グループ コントロールのオプション ボタンを設定または返すには、FormGroupControl.frameOptionButton メソッドを使用します。

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

フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a>パラメーター - rightMargin

値  
右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---rightmargin"></a>戻り値 - rightMargin

フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。

## <a name="method-rightmarginmode"></a>メソッド rightMarginMode

フォーム グループ コントロールの右余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a>パラメーター - rightMarginMode

モード  
右余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---rightmarginmode"></a>戻り値 - rightMarginMode

右余白のサイズを固定したかどうか、または自動的に調整するかどうかを指定する Automode 列挙値です。右余白のサイズが自動的に調整される場合は自動、そうでなければ、固定します。

## <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

フォーム グループ コントロールの右余白のサイズをピクセル単位で設定するか返します。

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a>パラメーター - rightMarginValue

値  
フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。オプション。

### <a name="return-value---rightmarginvalue"></a>戻り値 - rightMarginValue

フォーム グループ コントロールの右余白のサイズをピクセル単位で指定する整数値。

## <a name="method-savefilter"></a>メソッド saveFilter

```xpp
public boolean saveFilter([boolean value])
```

### <a name="parameters---savefilter"></a>パラメーター - saveFilter

値  

### <a name="return-value---savefilter"></a>戻り値 - saveFilter

## <a name="method-securitykey"></a>メソッド securityKey

フォーム グループ コントロールのセキュリティ キー ID を設定するか返します。

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  
ID を含む SecurityKeyId データ型、オプション。

### <a name="return-value---securitykey"></a>戻り値 - securityKey

ID を含む SecurityKeyId データ型の値。

## <a name="method-showcontextmenu"></a>メソッド showContextMenu

フォーム グループ コントロールのショートカット メニューを表示します。

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a>パラメーター - showContextMenu

menuHandle  
ショートカット メニューのハンドルを指定する整数値。

### <a name="return-value---showcontextmenu"></a>戻り値 - showContextMenu

ユーザーの選択を指定する整数値。

## <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示すブール値を設定するか返します。

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  
コントロールがスキップされたかどうかを示すブール値; オプション。

### <a name="return-value---skip"></a>戻り値 - skip

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

## <a name="method-sort"></a>メソッド sort

フォーム グループ コントロールに格納されているコントロールを並べ替えます。

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a>パラメーター - sort

sortDirection  
コントロールの並べ替え順序を示すシステム列挙値、オプション。

### <a name="return-value---sort"></a>戻り値 - sort

並べ替え順序を含む整数値。

## <a name="method-style"></a>メソッド style

```xpp
public int style([int value])
```

### <a name="parameters---style"></a>パラメーター - style

値  

### <a name="return-value---style"></a>戻り値 - style

## <a name="method-tooltip"></a>メソッド toolTip

フォーム グループ コントロールのツールヒントのテキスト文字列を返します。

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a>戻り値 - toolTip

ツールヒントのテキストを含む文字列値。

## <a name="method-top"></a>メソッド top

フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a>パラメーター - top

値  
垂直位置の計算方法を示す整数値。オプション。

<!-- -->

モード  
垂直位置の計算方法を示す整数値。オプション。

### <a name="return-value---top"></a>戻り値 - top

フォーム グループ コントロールの垂直位置をピクセル単位で示す整数値。

### <a name="remarks---top"></a>備考 - top

mode パラメーターは、次の値のいずれかになります。

-   -1 (既定) � 値パラメーターの値が正確に使用される Exact モードを使用します。
-   FormTop 列挙値。

### <a name="examples---top"></a>例 - top

次の例では、上位メソッドを呼び出して、垂直位置を 50 ピクセルに設定します。

```xpp
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
```

## <a name="method-topmargin"></a>メソッド topMargin

フォーム グループ コントロールの上余白をピクセル単位で設定するか返し、サイズが自動的に調整されるかどうかを指定します。

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a>パラメーター - topMargin

値  
上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

<!-- -->

モード  
上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す AutoMode 列挙値です。

### <a name="return-value---topmargin"></a>戻り値 - topMargin

フォーム グループ コントロールの上余白のサイズをピクセル単位で指定する整数。

## <a name="method-topmarginmode"></a>メソッド topMarginMode

フォーム グループ コントロールの上余白のサイズが固定されているかどうか、またはフォーム プロパティ設定に基づいて自動的に調整されるかどうかを示す値を設定するか返します。

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a>パラメーター - topMarginMode

モード  
上余白のサイズが固定されているかどうか、または他のフォーム プロパティ設定、オプションなどに基づいて自動的に調整されるかどうかを示す Automode 列挙値です。

### <a name="return-value---topmarginmode"></a>戻り値 - topMarginMode

左余白のサイズが自動的に調整される場合は自動の Automode 列挙値、そうでない場合は、固定します。

## <a name="method-topmarginvalue"></a>メソッド topMarginValue

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a>パラメーター - topMarginValue

値  

### <a name="return-value---topmarginvalue"></a>戻り値 - topMarginValue

## <a name="method-topmode"></a>メソッド topMode

フォーム グループ コントロールの垂直位置を計算する方法を示す値を設定するか返します。

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a>パラメーター - topMode

値  
垂直位置の計算方法を示す整数。オプション。

### <a name="return-value---topmode"></a>戻り値 - topMode

垂直位置の計算方法を示す整数値。正確なピクセル値、または FormTop 列挙値は -1 。

### <a name="examples---topmode"></a>例 - topMode

次の例は、正確なピクセル値に基づいて、垂直位置を計算する topMode メソッドの呼び出しを示しています。

```xpp
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
```

## <a name="method-topvalue"></a>メソッド topValue

フォーム グループ コントロールの垂直位置をピクセル単位で設定するか返します。

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a>パラメーター - topValue

値  
垂直位置を指定する整数データ型です。

### <a name="return-value---topvalue"></a>戻り値 - topValue

フォーム グループ コントロールの垂直位置を指定する整数データ型値です。

### <a name="remarks---topvalue"></a>備考 - topValue

正確なピクセル値に上部モードが設定されていない限り、垂直位置は変更されません。 詳細については、「topMode メソッド」を参照してください。

### <a name="examples---topvalue"></a>例 - topValue

次の例は、垂直位置を 50 ピクセルに設定する topValue メソッドの呼び出しを示しています。

```xpp
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
```

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

コントロールがユーザーから非表示になっているかどうかを示す整数データ型を設定するか返します。

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a>パラメーター - userHide

値  
フォーム グループ コントロールはユーザーから隠されているかどうかを示す整数値。オプション。

### <a name="return-value---userhide"></a>戻り値 - userHide

フォーム グループ コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

### <a name="remarks---userhide"></a>備考 - userHide

ユーザーは、コントロールを右クリックして [非表示] をクリックして、フォーム グループ コントロールを非表示にできます。 このメソッドでは、プログラムを使用してコントロールが非表示にするかどうかを指定できます。

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

ユーザーが Tab キーを押してコントロールに移動するときにフォーム グループ コントロールがスキップされるかどうかを示す整数を設定するか返します。

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a>パラメーター - userSkip

値  
フォーム グループ コントロールをスキップするかどうかのユーザー設定を示す整数。オプション。

### <a name="return-value---userskip"></a>戻り値 - userSkip

フォーム グループ コントロールがスキップされる場合は 1、それ以外の場合、0 です。

### <a name="remarks---userskip"></a>備考 - userSkip

ユーザーは、ユーザー設定フォームを使用してフォーム グループ コントロールをスキップするかどうかを選択します。

## <a name="method-userwidth"></a>メソッド userWidth

フォーム グループ コントロールの幅をピクセル単位で示す整数を設定するか返します。

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a>パラメーター - userWidth

値  
フォーム グループ コントロールの幅をピクセル単位で示す整数。オプション。

### <a name="return-value---userwidth"></a>戻り値 - userWidth

フォーム グループ コントロールの幅をピクセル単位で示す整数値。ユーザーが幅を指定していない場合は 0 (ゼロ) 。

### <a name="remarks---userwidth"></a>備考 - userWidth

ユーザーは、ユーザー設定フォームを使用して文字の幅を指定します。 このメソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。

## <a name="method-useuserlayout"></a>メソッド useUserLayout

フォーム グループ コントロールのユーザー指定レイアウトを使用するかどうかを指定します。

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a>パラメーター - useUserLayout

値  
フォーム グループ コントロールのユーザー指定のレイアウトを使用するかどうかを指定するブール値; オプション。

### <a name="return-value---useuserlayout"></a>戻り値 - useUserLayout

フォーム グループ コントロールのユーザー指定レイアウトが使用される場合は true。それ以外の場合は、false。

### <a name="remarks---useuserlayout"></a>備考 - useUserLayout

ユーザーは、ユーザー設定フォームを使用してレイアウトを指定します。

## <a name="method-verticalspacing"></a>メソッド verticalSpacing

ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定し、スペースを計算する方法を指定します。

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

コントロールの上と下のスペースの量を示す整数値。

## <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

フォーム グループ コントロールの上と下のスペースの量を計算する方法を示す値を設定するか返します。

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a>パラメーター - verticalSpacingMode

モード  
領域の計算方法を示す AutoMode システムの列挙値、オプションです。

### <a name="return-value---verticalspacingmode"></a>戻り値 - verticalSpacingMode

フォント サイズなどの他のフォーム設定に基づいてスペースが自動的に調整される場合 AutoMode 列挙は自動に設定しますが、それ以外の場合は、固定します。

## <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

ピクセルでフォーム グループ コントロールの上と下のスペースの量を取得または設定します。

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a>パラメーター - verticalSpacingValue

値  
コントロールの上と下のスペースの量を示す整数。オプション。

### <a name="return-value---verticalspacingvalue"></a>戻り値 - verticalSpacingValue

コントロールの上と下のスペースの量を示す整数値。

## <a name="method-vieweditmode"></a>メソッド viewEditMode

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a>パラメーター - viewEditMode

値  

### <a name="return-value---vieweditmode"></a>戻り値 - viewEditMode

## <a name="method-visible"></a>メソッド visible

フォーム グループ コントロールを表示または非表示にするブール値データ型を取得または設定します。

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  
フォーム グループ コントロールを表示または非表示にするブール値; オプション。

### <a name="return-value---visible"></a>戻り値 - visible

フォーム グループ コントロールが表示される場合は true。それ以外の場合は、false。

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  
幅の計算方法を示す整数。 これは、次のいずれかの値になります。

<!-- -->

モード  
幅の計算方法を示す整数。 これは、次のいずれかの値になります。

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

次の例は、コントロールの幅を 200 ピクセルに設定する width メソッドの呼び出しを示しています。

```xpp
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
```

## <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a>パラメーター - widthMode

値  
コントロール幅の計算方法を示す整数値。オプション。

### <a name="return-value---widthmode"></a>戻り値 - widthMode

現在の計算モードの幅を示す整数値。

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
```

## <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  
コントロールの幅をピクセル単位で指定する整数。

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="examples---widthvalue"></a>例 - widthValue

次の例は、コントロールの幅を 200 ピクセルに設定する widthValue メソッドの呼び出しを示しています。

```xpp
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

## <a name="method-drop"></a>メソッド drop

ユーザーがフォーム グループ コントロールまたはフォーム グループ コントロールのアイテムを新しい位置にドロップすると呼び出されます。

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a>パラメーター - drop

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

### <a name="remarks---drop"></a>備考 - drop

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、drop をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-onlostfocus"></a>メソッド OnLostFocus

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a>パラメーター - OnLostFocus

sender  

<!-- -->

e  

## <a name="method-onenter"></a>メソッド OnEnter

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a>パラメーター - OnEnter

sender  

<!-- -->

e  

## <a name="method-mouseleave"></a>メソッド mouseLeave

ユーザーがマウス ポインターをコントロールから離すと呼び出されます。

```xpp
public void mouseLeave()
```

### <a name="remarks---mouseleave"></a>備考 - mouseLeave

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseLeave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-context"></a>メソッド context

ユーザーがフォーム グループ コントロールを右クリックすると呼び出されます。

```xpp
public void context()
```

### <a name="remarks---context"></a>備考 - context

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、コンテキストをクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-copy"></a>メソッド copy

フォーム グループ コントロールをコピーします。

```xpp
public void copy()
```

## <a name="method-cut"></a>メソッド cut

コントロールのコンテンツを切り取りします。

```xpp
public void cut()
```

## <a name="method-paste"></a>メソッド paste

フォーム グループ コントロールを貼り付けます。

```xpp
public void paste()
```

## <a name="method-arrange"></a>メソッド arrange

```xpp
public void arrange()
```

## <a name="method-clicked"></a>メソッド clicked

フォーム グループ コントロールがユーザーにクリックされると呼び出されます。

```xpp
public void clicked()
```

## <a name="method-onleaving"></a>メソッド OnLeaving

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a>パラメーター - OnLeaving

sender  

<!-- -->

e  

## <a name="method-inputsearch"></a>メソッド inputSearch

ユーザーがバインドされたコントロールに検索文字列を入力すると呼び出されます。

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a>パラメーター - inputSearch

searchStr  
検索テキストを含む文字列データ型; オプション。

### <a name="remarks---inputsearch"></a>備考 - inputSearch

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、inputSearch をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

フォーム グループ コントロールのユーザー設定をリセットします。

```xpp
public void resetUserSetting()
```

## <a name="method-onclicked"></a>メソッド OnClicked

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a>パラメーター - OnClicked

sender  

<!-- -->

e  

## <a name="method-lostfocus"></a>メソッド lostFocus

ユーザーがフォーム グループ コントロールをフォーカス外に持っていくと呼び出されます。

```xpp
public void lostFocus()
```

### <a name="remarks---lostfocus"></a>備考 - lostFocus

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、lostFocus をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」フォームを参照してください。

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

## <a name="method-enddrag"></a>メソッド endDrag

ユーザーがフォーム グループ コントロールの移動を終了すると呼び出されます。

```xpp
public void endDrag()
```

## <a name="method-jumpref"></a>メソッド jumpRef

ユーザーがフォーム グループ コントロールのコントロール ショートカット メニューでメイン テーブルへ移動フォーム コマンドをクリックすると呼び出されます。

```xpp
public void jumpRef()
```

## <a name="method-setfocus"></a>メソッド setFocus

コントロールにフォーカスを設定します。

```xpp
public void setFocus()
```

## <a name="method-filter"></a>メソッド filter

ユーザーがフォーム グループ コントロールを右クリックしてから選択フィルタをクリックすると呼び出されます。

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a>パラメーター - filter

filterStr  
フィルターのテキストを指定する文字列データ型; オプション。

### <a name="remarks---filter"></a>備考 - filter

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、filter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-displaycontrol"></a>メソッド displayControl

フォーム グループ コントロールを表示します。

```xpp
public void displayControl()
```

## <a name="method-gotfocus"></a>メソッド gotFocus

ユーザーがフォーム グループ コントロールにフォーカスを移すタイミングを指定します。

```xpp
public void gotFocus()
```

### <a name="remarks---gotfocus"></a>備考 - gotFocus

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、gotFocus をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

フォーム グループ コントロールの列の高さと幅を指定します。

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a>パラメーター - prefColumnSize

width  
列の高さを指定する整数値。

<!-- -->

height  
列の高さを指定する整数値。

## <a name="method-dragleave"></a>メソッド dragLeave

ユーザーがフォーム グループ コントロールの境界からオブジェクトをドラッグすると呼び出されます。

```xpp
public void dragLeave()
```

### <a name="remarks---dragleave"></a>備考 - dragLeave

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、dragLeave をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-ongotfocus"></a>メソッド OnGotFocus

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a>パラメーター - OnGotFocus

sender  

<!-- -->

e  

## <a name="method-enter"></a>メソッド enter

ユーザーがフォーム グループ コントロールにフォーカスを移動すると呼び出されます。

```xpp
public void enter()
```

### <a name="remarks---enter"></a>備考 - enter

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、enter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

## <a name="method-mouseenter"></a>メソッド mouseEnter

ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a>パラメーター - mouseEnter

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

### <a name="remarks---mouseenter"></a>備考 - mouseEnter

button パラメーターに指定できる値は次のとおりです。

|     |                      |
|-----|----------------------|
| 1   | マウスの左ボタン   |
| 2   | マウスの中央ボタン。 |
| 3   | マウスの右ボタン  |

コントロールの下のメソッド ノードを右クリックして、Override メソッドをクリックし、mouseEnter をクリックすることにより、フォーム グループでこのメソッドをオーバーライドすることができます。 フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。

