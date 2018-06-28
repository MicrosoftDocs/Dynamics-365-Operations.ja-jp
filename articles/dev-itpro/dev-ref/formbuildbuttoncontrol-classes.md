---
title: "F クラス - FormBuildFastTabSummarySeparator への FormBuildButtonControl"
description: "文字 F で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 11/06/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 58741
ms.assetid: 9af62525-aa36-4d6f-b138-c9002a4b21e2
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 971ef2a39b21f6dd4d668bf2090f1de9f114b93b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="f-classes---formbuildbuttoncontrol-to-formbuildfasttabsummaryseparator"></a>F クラス - FormBuildFastTabSummarySeparator への FormBuildButtonControl

[!include [banner](../includes/banner.md)]

文字 F で始まるシステム API クラス。

<a name="class-formbuildbuttoncontrol"></a>クラス FormBuildButtonControl
----------------------------

    class FormBuildButtonControl extends FormBuildControl

FormBuildButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public int acquireFocus(\[int value\])                                                                      |                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public boolean autoRefreshData(\[boolean value\])                                                           |                                                                                                                                         |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                           |
| public boolean big(\[boolean value\])                                                                       |                                                                                                                                         |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                     |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public int buttonDisplay(\[int value\])                                                                     | ボタン コントロールの外観を取得または設定します。                                                                                      |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public boolean defaultButton(\[boolean value\])                                                             | ボタンをフォーム上の既定のボタンにするかどうかを指定します。                                                                 |
| public str disabledImage(\[str value\])                                                                     | コントロールの無効な画像を取得または設定します。                                                                                          |
| public int disabledImageLocation(\[int value\])                                                             |                                                                                                                                         |
| public int disabledResource(\[int value\])                                                                  | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                          |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public boolean forcedToOverflow(\[boolean value\])                                                          |                                                                                                                                         |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public int imageLocation(\[int value\])                                                                     |                                                                                                                                         |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int multiSelect(\[int value\])                                                                       |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int needsRecord(\[int value\])                                                                       |                                                                                                                                         |
| public str normalImage(\[str value\])                                                                       |                                                                                                                                         |
| public int normalResource(\[int value\])                                                                    |                                                                                                                                         |
| public boolean primary(\[boolean value\])                                                                   |                                                                                                                                         |
| public boolean saveRecord(\[boolean value\])                                                                |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public int shortkey(\[int value\])                                                                          |                                                                                                                                         |
| public boolean showShortCut(\[boolean value\])                                                              |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                         |
| public int toggleButton(\[int value\])                                                                      |                                                                                                                                         |
| public int toggleValue(\[int value\])                                                                       |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public boolean value(\[boolean value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-acquirefocus"></a>メソッド acquireFocus

    public int acquireFocus([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

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

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

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

### <a name="method-defaultbutton"></a>メソッド defaultButton

ボタンをフォーム上の既定のボタンにするかどうかを指定します。

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

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-shortkey"></a>メソッド shortkey

    public int shortkey([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
コントロールの skip プロパティに割り当てる値。

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

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

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

### <a name="method-value"></a>メソッド value

    public boolean value([boolean value])

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildbuttongroupcontrol"></a>クラス FormBuildButtonGroupControl
    class FormBuildButtonGroupControl extends FormBuildControl

FormBuildButtonGroupControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignChild(\[boolean value\])                                                                |                                                                                                                                         |
| public boolean alignChildren(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int allowUserSetup(\[int value\])                                                                    |                                                                                                                                         |
| public int arrangeGuide(\[int value\])                                                                      |                                                                                                                                         |
| public int arrangeMethod(\[int value\])                                                                     |                                                                                                                                         |
| public int arrangeWhen(\[int value\])                                                                       |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                          |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                     |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                         |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                         |                                                                                                                                         |
| public int bottomMarginValue(\[int value\])                                                                 |                                                                                                                                         |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                 |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                     |                                                                                                                                         |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                        |                                                                                                                                         |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                         |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                          |                                                                                                                                         |
| public int columnspaceValue(\[int value\])                                                                  |                                                                                                                                         |
| public int columnsValue(\[int value\])                                                                      |                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                       |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int framePosition(\[int value\])                                                                     |                                                                                                                                         |
| public int frameType(\[int value\])                                                                         |                                                                                                                                         |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public boolean hideIfEmpty(\[boolean value\])                                                               |                                                                                                                                         |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                     |                                                                                                                                         |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                           |                                                                                                                                         |
| public int leftMarginValue(\[int value\])                                                                   |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         | コントロールに指定されたコントロールを移動します。                                                                                               |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                         |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                          |                                                                                                                                         |
| public int rightMarginValue(\[int value\])                                                                  |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean sizeHeight(\[boolean value\])                                                                |                                                                                                                                         |
| public boolean sizeWidth(\[boolean value\])                                                                 |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                         |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                            |                                                                                                                                         |
| public int topMarginValue(\[int value\])                                                                    |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public boolean useUserLayout(\[boolean value\])                                                             |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

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

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

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

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-frameposition"></a>メソッド framePosition

    public int framePosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-frametype"></a>メソッド frameType

    public int frameType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

### <a name="method-movecontrol"></a>メソッド moveControl

コントロールに指定されたコントロールを移動します。

    public int moveControl(int controlId, [int insertAfterControlId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterControlId  

#### <a name="return-value"></a>戻り値

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

#### <a name="remarks"></a>備考

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

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

### <a name="method-sizeheight"></a>メソッド sizeHeight

    public boolean sizeHeight([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sizewidth"></a>メソッド sizeWidth

    public boolean sizeWidth([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildbuttonseparatorcontrol"></a>クラス FormBuildButtonSeparatorControl
    class FormBuildButtonSeparatorControl extends FormBuildControl

FormBuildButtonSeparatorControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                      |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                           |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                            |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                           |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                     |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                               |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                               |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                               |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                             |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                           |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                       |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                       |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                               |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                              |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                  |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                               |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                               |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                               |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                               |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                               |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                               |
| public str text(\[str value\])                                                                              |                                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                               |
| public int topMode(\[int value\])                                                                           |                                                                                                                                               |
| public int topValue(\[int value\])                                                                          |                                                                                                                                               |
| public int type(\[int value\])                                                                              |                                                                                                                                               |
| public int userData(\[int value\])                                                                          |                                                                                                                                               |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                               |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                               |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                               |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                               |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                               |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                               |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                        |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                        |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                               |

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

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

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

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

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

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildcheckboxcontrol"></a>クラス FormBuildCheckBoxControl
    class FormBuildCheckBoxControl extends FormBuildControl

FormBuildCheckBoxControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                           |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                     |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean drawFocusRect(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public boolean optionalRecordControl(\[boolean value\])                                                     |                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int value(\[int value\])                                                                             |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

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

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

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

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-optionalrecordcontrol"></a>メソッド optionalRecordControl

    public boolean optionalRecordControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-value"></a>メソッド value

    public int value([int value])

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

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildcomboboxcontrol"></a>クラス FormBuildComboBoxControl
    class FormBuildComboBoxControl extends FormBuildControl

FormBuildComboBoxControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                      |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                           |
| public boolean appendNew(\[boolean value\])                                                                 |                                                                                                                                               |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                               |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                            |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                             |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                   |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                      |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                               |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                   |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                 |
| public int comboType(\[int value\])                                                                         |                                                                                                                                               |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                           |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                     |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                               |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                               |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                               |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                               |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                               |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                      |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                               |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                               |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                               |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                               |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                             |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                           |
| public EnumId enumType(\[EnumId value\])                                                                    |                                                                                                                                               |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                               |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                               |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                     |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                     |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                           |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                       |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                       |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public boolean hideFirstEntry(\[boolean value\])                                                            |                                                                                                                                               |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                               |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                              |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                  |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                               |
| public int item(\[int value\])                                                                              |                                                                                                                                               |
| public int items(\[int value\])                                                                             |                                                                                                                                               |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                         |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                               |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                               |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                               |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                               |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                               |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                               |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                               |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                               |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                               |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                               |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                               |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                               |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                               |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                               |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                               |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                               |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                               |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                               |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                               |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                               |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                               |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                               |
| public int selection(\[int value\])                                                                         |                                                                                                                                               |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                               |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。               |
| public str text(\[str value\])                                                                              |                                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                               |
| public int topMode(\[int value\])                                                                           |                                                                                                                                               |
| public int topValue(\[int value\])                                                                          |                                                                                                                                               |
| public int type(\[int value\])                                                                              |                                                                                                                                               |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                               |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                               |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                               |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                               |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                               |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                               |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                               |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                               |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                        |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                        |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                               |

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

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

### <a name="method-combotype"></a>メソッド comboType

    public int comboType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-enumtype"></a>メソッド enumType

    public EnumId enumType([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hidefirstentry"></a>メソッド hideFirstEntry

    public boolean hideFirstEntry([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-selection"></a>メソッド selection

    public int selection([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

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

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildcommandbuttoncontrol"></a>クラス FormBuildCommandButtonControl
    class FormBuildCommandButtonControl extends FormBuildControl

FormBuildCommandButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public boolean autoRefreshData(\[boolean value\])                                                           |                                                                                                                                         |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                          |
| public boolean big(\[boolean value\])                                                                       |                                                                                                                                         |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                     |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public int buttonDisplay(\[int value\])                                                                     | ボタン コントロールの外観を取得または設定します。                                                                                      |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                 |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public int command(\[int value\])                                                                           |                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public boolean defaultButton(\[boolean value\])                                                             | ボタンをフォーム上の既定のボタンにするかどうかを指定します。                                                                 |
| public str disabledImage(\[str value\])                                                                     | コントロールの無効な画像を取得または設定します。                                                                                          |
| public int disabledImageLocation(\[int value\])                                                             |                                                                                                                                         |
| public int disabledResource(\[int value\])                                                                  | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                          |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public boolean forcedToOverflow(\[boolean value\])                                                          |                                                                                                                                         |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public int imageLocation(\[int value\])                                                                     |                                                                                                                                         |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int multiSelect(\[int value\])                                                                       |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int needsRecord(\[int value\])                                                                       |                                                                                                                                         |
| public str normalImage(\[str value\])                                                                       |                                                                                                                                         |
| public int normalResource(\[int value\])                                                                    |                                                                                                                                         |
| public str parameters(\[str value\])                                                                        |                                                                                                                                         |
| public boolean primary(\[boolean value\])                                                                   |                                                                                                                                         |
| public boolean saveRecord(\[boolean value\])                                                                |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public int shortkey(\[int value\])                                                                          |                                                                                                                                         |
| public boolean showShortCut(\[boolean value\])                                                              |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public str text(\[str value\])                                                                              |                                                                                                                                         |
| public int toggleButton(\[int value\])                                                                      |                                                                                                                                         |
| public int toggleValue(\[int value\])                                                                       |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public boolean value(\[boolean value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

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

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

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

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
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

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

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

### <a name="method-defaultbutton"></a>メソッド defaultButton

ボタンをフォーム上の既定のボタンにするかどうかを指定します。

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

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-parameters"></a>メソッド parameters

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-shortkey"></a>メソッド shortkey

    public int shortkey([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
コントロールの skip プロパティに割り当てる値。

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

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

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

### <a name="method-value"></a>メソッド value

    public boolean value([boolean value])

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildcontainercontrol"></a>クラス FormBuildContainerControl
    class FormBuildContainerControl extends FormBuildControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明 |
|-------------------------------------------------------------------------------------------------------------|-------------|
| public boolean alignControl(\[boolean value\])                                                              |             |
| public boolean allowEdit(\[boolean value\])                                                                 |             |
| public boolean autoDeclaration(\[boolean value\])                                                           |             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    |             |
| public int containerId()                                                                                    |             |
| public str countryRegionCodes(\[str value\])                                                                |             |
| public str dataRelationPath(\[str value\])                                                                  |             |
| public int displayTarget(\[int value\])                                                                     |             |
| public int dragDrop(\[int value\])                                                                          |             |
| public boolean enabled(\[boolean value\])                                                                   |             |
| public int height(int value, \[int mode\])                                                                  |             |
| public int heightMode(\[int value\])                                                                        |             |
| public int heightValue(\[int value\])                                                                       |             |
| public str helpText(\[str value\])                                                                          |             |
| public str hierarchyParent(\[str value\])                                                                   |             |
| public int id()                                                                                             |             |
| public boolean isContainer()                                                                                |             |
| public int left(int value, \[int mode\])                                                                    |             |
| public int leftMode(\[int value\])                                                                          |             |
| public int leftValue(\[int value\])                                                                         |             |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         |             |
| public str name(\[str value\])                                                                              |             |
| public int neededPermission(\[int value\])                                                                  |             |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |             |
| public boolean skip(\[boolean value\])                                                                      |             |
| public int top(int value, \[int mode\])                                                                     |             |
| public int topMode(\[int value\])                                                                           |             |
| public int topValue(\[int value\])                                                                          |             |
| public int type(\[int value\])                                                                              |             |
| public int userData(\[int value\])                                                                          |             |
| public int userDataItem(\[int value\])                                                                      |             |
| public int userDataItems(\[int value\])                                                                     |             |
| public boolean useUserLayout(\[boolean value\])                                                             |             |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |             |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |             |
| public int verticalSpacingValue(\[int value\])                                                              |             |
| public boolean visible(\[boolean value\])                                                                   |             |
| public int width(int value, \[int mode\])                                                                   |             |
| public int widthMode(\[int value\])                                                                         |             |
| public int widthValue(\[int value\])                                                                        |             |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |             |

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

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-containerid"></a>メソッド containerId

    public int containerId()

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

### <a name="method-enabled"></a>メソッド enabled

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-helptext"></a>メソッド helpText

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

    public int id()

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-movecontrol"></a>メソッド moveControl

    public int moveControl(int controlId, [int insertAfterControlId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterControlId  

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

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildcontrol"></a>クラス FormBuildControl
    class FormBuildControl extends Object

FormBuildControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                    | 説明                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| public FormBuildControl addControl(FormControlType controlType, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\]) | 指定したコントロール タイプに基づいて、コントロールにコントロールを追加します。                                                                                |
| public FormBuildControl addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])          |                                                                                                                                                    |
| public FormBuildControl addDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                                               | 指定したデータ フィールド情報に基づいて、コントロールにコントロールを追加します。                                                                      |
| public boolean allowEdit(\[boolean value\])                                                                                               |                                                                                                                                                    |
| public boolean autoDeclaration(\[boolean value\])                                                                                         |                                                                                                                                                    |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                                                     | 指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示す値を取得します。                                  |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                                                  |                                                                                                                                                    |
| public int containerId()                                                                                                                  | コントロールの親コンテナーの ID を取得します。                                                                                          |
| public int controlCount()                                                                                                                 | コントロールに含まれるコントロールの数を取得します。                                                                                |
| public FormBuildControl controlNum(int controlNo)                                                                                         | 指定したインデックスを使用して、上位のコントロールを取得します。                                                                                        |
| public str countryRegionCodes(\[str value\])                                                                                              |                                                                                                                                                    |
| public boolean editAutoPostback(\[boolean value\])                                                                                        |                                                                                                                                                    |
| public boolean enabled(\[boolean value\])                                                                                                 |                                                                                                                                                    |
| public str helpText(\[str value\])                                                                                                        |                                                                                                                                                    |
| public str extendedStyle(\[str value\])                                                                                                   |                                                                                                                                                    |
| public int height(int value, \[int mode\])                                                                                                |                                                                                                                                                    |
| public int heightMode(\[int value\])                                                                                                      |                                                                                                                                                    |
| public int heightValue(\[int value\])                                                                                                     |                                                                                                                                                    |
| public str GetXppILImplementation()                                                                                                       |                                                                                                                                                    |
| public boolean hasUserSetting()                                                                                                           | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                            |
| public int id()                                                                                                                           | コントロールの ID を取得します。                                                                                                                   |
| public boolean isContainer()                                                                                                              | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                       |
| public boolean markAsUserAdd(\[boolean value\])                                                                                           | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                              |
| public int moveControl(int controlId, \[int insertAfterId\])                                                                              | コントロールに指定されたコントロールを移動します。                                                                                                          |
| public str name(\[str value\])                                                                                                            |                                                                                                                                                    |
| public int neededPermission(\[int value\])                                                                                                |                                                                                                                                                    |
| public container SysObsoleteAttribute()                                                                                                   |                                                                                                                                                    |
| public str previewPartRef(\[str value\])                                                                                                  |                                                                                                                                                    |
| public boolean skip(\[boolean value\])                                                                                                    |                                                                                                                                                    |
| public boolean SysObsoleteAttribute(container data)                                                                                       |                                                                                                                                                    |
| public int userDisable(\[int value\])                                                                                                     | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                |
| public int userHeight(\[int value\])                                                                                                      | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                               |
| public int userHide(\[int value\])                                                                                                        | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                 |
| public int userOrgContainer(\[int value\])                                                                                                | コントロールの組織コンテナを取得または設定します。                                                                                           |
| public int userOrgSibling(\[int value\])                                                                                                  | コントロールの組織兄弟を取得または設定します。                                                                                             |
| public str userPromptText(\[str value\])                                                                                                  | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                  |
| public int userSecurityLevel(\[int value\])                                                                                               | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                              |
| public int userSkip(\[int value\])                                                                                                        | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。 |
| public int userWidth(\[int value\])                                                                                                       | ピクセル単位でコントロールの幅を設定するか返します。                                                                                                |
| public boolean visible(\[boolean value\])                                                                                                 |                                                                                                                                                    |
| public int width(int value, \[int mode\])                                                                                                 |                                                                                                                                                    |
| public int widthMode(\[int value\])                                                                                                       |                                                                                                                                                    |
| public int widthValue(\[int value\])                                                                                                      |                                                                                                                                                    |
| public void RegisterXppILImplementation(str className)                                                                                    |                                                                                                                                                    |
| public void new(FormContainer container)                                                                                                  |                                                                                                                                                    |
| public void resetUserSetting()                                                                                                            | コントロールのユーザー設定をリセットします。                                                                                                          |

### <a name="method-addcontrol"></a>メソッド addControl

指定したコントロール タイプに基づいて、コントロールにコントロールを追加します。

    public FormBuildControl addControl(FormControlType controlType, str controlName, [FormBuildControl insertAfter], [boolean pushFront])

#### <a name="parameters"></a>パラメーター

controlType  
新しいコントロールの名前を設定する文字列値。

<!-- -->

controlName  
新しいコントロールの名前を設定する文字列値。

<!-- -->

insertAfter  

<!-- -->

pushFront  

#### <a name="return-value"></a>戻り値

新たに追加されたコントロールを表す FormBuildControl オブジェクトです。

### <a name="method-addcontrolex"></a>メソッド addControlEx

    public FormBuildControl addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])

#### <a name="parameters"></a>パラメーター

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

<!-- -->

pushFront  

#### <a name="return-value"></a>戻り値

### <a name="method-adddatafield"></a>メソッド addDataField

指定したデータ フィールド情報に基づいて、コントロールにコントロールを追加します。

    public FormBuildControl addDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSourceId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

fieldId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

arrayIndex  
データ フィールド型のインデックスを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

新たに追加されたコントロールを表す FormBuildControl オブジェクトです。

#### <a name="remarks"></a>備考

追加するコントロールのタイプは、指定されたデータ フィールド情報に基づいて自動的に決定されます。 値が指定されていないときは、arrayIndex パラメーターが既定値の 1 であるため、最初のインデックスが想定されます。

### <a name="method-allowedit"></a>メソッド allowEdit

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-canadddatafield"></a>メソッド canAddDataField

指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示す値を取得します。

    public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSourceId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

fieldId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

arrayIndex  
データ フィールド型のインデックスを示す整数値。オプション。

#### <a name="return-value"></a>戻り値

指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示すブール値。

### <a name="method-configurationkey"></a>メソッド configurationKey

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-controlcount"></a>メソッド controlCount

コントロールに含まれるコントロールの数を取得します。

    public int controlCount()

#### <a name="return-value"></a>戻り値

コンテナー コントロールの場合、コントロール内に含まれているコントロールの数を示す整数値。それ以外の場合は、0 。

### <a name="method-controlnum"></a>メソッド controlNum

指定したインデックスを使用して、上位のコントロールを取得します。

    public FormBuildControl controlNum(int controlNo)

#### <a name="parameters"></a>パラメーター

controlNo  
取得する子コントロールのインデックスを示す整数値。

#### <a name="return-value"></a>戻り値

コンテナー コントロールである場合は、指定されたインデックスを持つ子コントロールを表す FormBuildControl オブジェクト; それ以外の場合は、nullNothingnullptrunita null参照 (Visual Basicにはなし)。

#### <a name="remarks"></a>備考

指定した controlNo パラメーターが範囲外にある場合は、例外が発生します。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-editautopostback"></a>メソッド editAutoPostback

    public boolean editAutoPostback([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-extendedstyle"></a>メソッド extendedStyle

    public str extendedStyle([str value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-getxppilimplementation"></a>メソッド GetXppILImplementation

    public str GetXppILImplementation()

#### <a name="return-value"></a>戻り値

### <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

    public boolean hasUserSetting()

#### <a name="return-value"></a>戻り値

コントロールにカスタム ユーザー設定があるかどうかを示すブール値。

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールをユーザーが追加したコントロールとしてマークするかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

ユーザーが追加したコントロールとして、コントロールがマークされたかどうかを示すブール値。

### <a name="method-movecontrol"></a>メソッド moveControl

コントロールに指定されたコントロールを移動します。

    public int moveControl(int controlId, [int insertAfterId])

#### <a name="parameters"></a>パラメーター

controlId  
後にコントロールを挿入するコントロールの ID を示す整数値。オプション。

<!-- -->

insertAfterId  
後にコントロールを挿入するコントロールの ID を示す整数値。オプション。

#### <a name="return-value"></a>戻り値

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

#### <a name="remarks"></a>備考

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

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

### <a name="method-previewpartref"></a>メソッド previewPartRef

    public str previewPartRef([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

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

ピクセル単位でコントロールの幅を設定するか返します。

    public int userWidth([int value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの幅として使用するピクセル数 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

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

### <a name="method-registerxppilimplementation"></a>メソッド RegisterXppILImplementation

    public void RegisterXppILImplementation(str className)

#### <a name="parameters"></a>パラメーター

className  

### <a name="method-new"></a>メソッド new

    public void new(FormContainer container)

#### <a name="parameters"></a>パラメーター

コンテナー  

### <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

    public void resetUserSetting()

## <a name="class-formbuilddatasource"></a>クラス FormBuildDataSource
    class FormBuildDataSource extends FormBuildObjectSet

FormBuildDataSource クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                            | 説明                                                                                                               |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public FormBuildDataSource addReferenceDataSource(str name, \[str joinRelation\]) |                                                                                                                           |
| public boolean allowCheck(\[boolean value\])                                      |                                                                                                                           |
| public boolean allowCreate(\[boolean value\])                                     |                                                                                                                           |
| public boolean allowDeferredLoad(\[boolean value\])                               |                                                                                                                           |
| public boolean allowDelete(\[boolean value\])                                     |                                                                                                                           |
| public boolean allowEdit(\[boolean value\])                                       | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                       |
| public boolean autoNotify(\[boolean value\])                                      |                                                                                                                           |
| public boolean autoQuery(\[boolean value\])                                       |                                                                                                                           |
| public boolean autoSearch(\[boolean value\])                                      |                                                                                                                           |
| public FormBuildDataSource baseDataSource()                                       |                                                                                                                           |
| public str company(\[str value\])                                                 |                                                                                                                           |
| public FieldId counterField(\[FieldId value\])                                    |                                                                                                                           |
| public boolean crossCompanyAutoQuery(\[boolean value\])                           |                                                                                                                           |
| public boolean delayActive(\[boolean value\])                                     |                                                                                                                           |
| public int extends(\[AnyType value\])                                             |                                                                                                                           |
| public str GetXppILImplementation()                                               |                                                                                                                           |
| public IndexId index(\[IndexId value\])                                           |                                                                                                                           |
| public boolean insertAtEnd(\[boolean value\])                                     |                                                                                                                           |
| public boolean insertIfEmpty(\[boolean value\])                                   |                                                                                                                           |
| public boolean isBaseDataSource()                                                 |                                                                                                                           |
| public boolean isInheritanceDataSource()                                          |                                                                                                                           |
| public boolean isMasterDataSource()                                               |                                                                                                                           |
| public str joinRelation(\[str value\])                                            |                                                                                                                           |
| public int joinSource(\[AnyType value\])                                          |                                                                                                                           |
| public int linkType(\[int value\])                                                |                                                                                                                           |
| public FormBuildDataSource masterDataSource()                                     |                                                                                                                           |
| public int maxAccessRight(\[int value\])                                          |                                                                                                                           |
| public int maxRecordsToLoad(\[int value\])                                        |                                                                                                                           |
| public str name(\[str value\])                                                    | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public boolean onlyFetchActive(\[boolean value\])                                 |                                                                                                                           |
| public int optionalRecordMode(\[int value\])                                      |                                                                                                                           |
| public int startPosition(\[int value\])                                           |                                                                                                                           |
| public TableId table(\[TableId value\])                                           | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                     |
| public int validTimeStateAutoQuery(\[int value\])                                 |                                                                                                                           |
| public int validTimeStateUpdate(\[int value\])                                    |                                                                                                                           |
| public void RegisterXppDataFieldILImplementation(str fieldName, str className)    |                                                                                                                           |
| public void RegisterXppILImplementation(str className)                            |                                                                                                                           |
| public void SetDataLinkType(QueryDataLinkType linkType, str parentDataSource)     |                                                                                                                           |

### <a name="method-addreferencedatasource"></a>メソッド addReferenceDataSource

    public FormBuildDataSource addReferenceDataSource(str name, [str joinRelation])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

joinRelation  

#### <a name="return-value"></a>戻り値

### <a name="method-allowcheck"></a>メソッド allowCheck

    public boolean allowCheck([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowcreate"></a>メソッド allowCreate

    public boolean allowCreate([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowdeferredload"></a>メソッド allowDeferredLoad

    public boolean allowDeferredLoad([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowdelete"></a>メソッド allowDelete

    public boolean allowDelete([boolean value])

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

### <a name="method-autonotify"></a>メソッド autoNotify

    public boolean autoNotify([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autoquery"></a>メソッド autoQuery

    public boolean autoQuery([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autosearch"></a>メソッド autoSearch

    public boolean autoSearch([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-basedatasource"></a>メソッド baseDataSource

    public FormBuildDataSource baseDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-company"></a>メソッド company

    public str company([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-counterfield"></a>メソッド counterField

    public FieldId counterField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-crosscompanyautoquery"></a>メソッド crossCompanyAutoQuery

    public boolean crossCompanyAutoQuery([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-delayactive"></a>メソッド delayActive

    public boolean delayActive([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-extends"></a>メソッド extends

    public int extends([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getxppilimplementation"></a>メソッド GetXppILImplementation

    public str GetXppILImplementation()

#### <a name="return-value"></a>戻り値

### <a name="method-index"></a>メソッド index

    public IndexId index([IndexId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-insertatend"></a>メソッド insertAtEnd

    public boolean insertAtEnd([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-insertifempty"></a>メソッド insertIfEmpty

    public boolean insertIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-isbasedatasource"></a>メソッド isBaseDataSource

    public boolean isBaseDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-isinheritancedatasource"></a>メソッド isInheritanceDataSource

    public boolean isInheritanceDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-ismasterdatasource"></a>メソッド isMasterDataSource

    public boolean isMasterDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-joinrelation"></a>メソッド joinRelation

    public str joinRelation([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-joinsource"></a>メソッド joinSource

    public int joinSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linktype"></a>メソッド linkType

    public int linkType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-masterdatasource"></a>メソッド masterDataSource

    public FormBuildDataSource masterDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-maxaccessright"></a>メソッド maxAccessRight

    public int maxAccessRight([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-maxrecordstoload"></a>メソッド maxRecordsToLoad

    public int maxRecordsToLoad([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-onlyfetchactive"></a>メソッド onlyFetchActive

    public boolean onlyFetchActive([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-optionalrecordmode"></a>メソッド optionalRecordMode

    public int optionalRecordMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-startposition"></a>メソッド startPosition

    public int startPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

    public TableId table([TableId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに関連付けられたテーブル ID の現在の値。

### <a name="method-validtimestateautoquery"></a>メソッド validTimeStateAutoQuery

    public int validTimeStateAutoQuery([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-validtimestateupdate"></a>メソッド validTimeStateUpdate

    public int validTimeStateUpdate([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-registerxppdatafieldilimplementation"></a>メソッド RegisterXppDataFieldILImplementation

    public void RegisterXppDataFieldILImplementation(str fieldName, str className)

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

className  

### <a name="method-registerxppilimplementation"></a>メソッド RegisterXppILImplementation

    public void RegisterXppILImplementation(str className)

#### <a name="parameters"></a>パラメーター

className  

### <a name="method-setdatalinktype"></a>メソッド SetDataLinkType

    public void SetDataLinkType(QueryDataLinkType linkType, str parentDataSource)

#### <a name="parameters"></a>パラメーター

linkType  

<!-- -->

parentDataSource  

## <a name="class-formbuilddatecontrol"></a>クラス FormBuildDateControl
    class FormBuildDateControl extends FormBuildControl

FormBuildDateControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                      |
| public int alignment(\[int value\])                                                                         |                                                                                                                                               |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                           |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                               |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                            |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                             |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                 |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。                                                                  |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                      |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                               |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                   |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                 |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                           |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                     |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                               |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                               |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                               |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                               |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                               |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                      |
| public int dateDay(\[int value\])                                                                           |                                                                                                                                               |
| public int dateFormat(\[int value\])                                                                        |                                                                                                                                               |
| public int dateMonth(\[int value\])                                                                         |                                                                                                                                               |
| public int dateSeparator(\[int value\])                                                                     |                                                                                                                                               |
| public Date dateValue(\[Date value\])                                                                       |                                                                                                                                               |
| public int dateYear(\[int value\])                                                                          |                                                                                                                                               |
| public int direction(\[int value\])                                                                         |                                                                                                                                               |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                               |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                               |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                               |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                               |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                               |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                               |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                               |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                             |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                           |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                               |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                               |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                     |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                     |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                           |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                       |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                       |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                               |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                              |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                               |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                  |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                               |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                         |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                               |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                               |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                               |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                               |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                               |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                               |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                               |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                               |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                               |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                               |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                               |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                               |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                               |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                               |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                               |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                               |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                               |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                               |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                               |
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                               |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                               |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                               |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                               |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                               |
| public str maxDateLabel(\[str value\])                                                                      |                                                                                                                                               |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                               |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                               |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                               |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                               |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                               |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                               |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                               |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。               |
| public int style(\[int value\])                                                                             |                                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                               |
| public int topMode(\[int value\])                                                                           |                                                                                                                                               |
| public int topValue(\[int value\])                                                                          |                                                                                                                                               |
| public int type(\[int value\])                                                                              |                                                                                                                                               |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                               |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                               |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                               |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                               |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                               |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                               |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                               |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                               |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                        |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                        |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                               |

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

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

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
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-dateday"></a>メソッド dateDay

    public int dateDay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dateformat"></a>メソッド dateFormat

    public int dateFormat([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datemonth"></a>メソッド dateMonth

    public int dateMonth([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dateseparator"></a>メソッド dateSeparator

    public int dateSeparator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datevalue"></a>メソッド dateValue

    public Date dateValue([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dateyear"></a>メソッド dateYear

    public int dateYear([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-maxdatelabel"></a>メソッド maxDateLabel

    public str maxDateLabel([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

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

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

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

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuilddatetimecontrol"></a>クラス FormBuildDateTimeControl
    class FormBuildDateTimeControl extends FormBuildControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                  |
| public int alignment(\[int value\])                                                                         |                                                                                                                                           |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                       |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                           |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                         |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                             |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                               |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                  |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                           |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                               |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                       |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                 |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                           |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                           |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                           |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                           |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                  |
| public int dateDay(\[int value\])                                                                           |                                                                                                                                           |
| public int dateFormat(\[int value\])                                                                        |                                                                                                                                           |
| public int dateMonth(\[int value\])                                                                         |                                                                                                                                           |
| public int dateSeparator(\[int value\])                                                                     |                                                                                                                                           |
| public DateTime dateTimeValue(\[DateTime value\])                                                           |                                                                                                                                           |
| public int dateYear(\[int value\])                                                                          |                                                                                                                                           |
| public int displayOption(\[int value\])                                                                     |                                                                                                                                           |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                           |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                           |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                           |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                 |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                 |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                       |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                   |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                            |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                   |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                           |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                          |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                              |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                           |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                     |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                           |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                           |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                           |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                           |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                           |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                           |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                           |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                           |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                           |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                           |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                           |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                           |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                           |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                           |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                           |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                           |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                           |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                           |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                           |
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                           |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                           |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                           |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                           |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                           |
| public str maxDateLabel(\[str value\])                                                                      |                                                                                                                                           |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                           |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                           |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                           |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                           |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                           |
| public int timeFormat(\[int value\])                                                                        |                                                                                                                                           |
| public int timeHours(\[int value\])                                                                         |                                                                                                                                           |
| public int timeMinute(\[int value\])                                                                        |                                                                                                                                           |
| public int timeSeconds(\[int value\])                                                                       |                                                                                                                                           |
| public int timeSeparator(\[int value\])                                                                     |                                                                                                                                           |
| public int timeZoneIndicator(\[int value\])                                                                 |                                                                                                                                           |
| public int timezonePreference(\[int value\])                                                                |                                                                                                                                           |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                           |
| public int topMode(\[int value\])                                                                           |                                                                                                                                           |
| public int topValue(\[int value\])                                                                          |                                                                                                                                           |
| public int type(\[int value\])                                                                              |                                                                                                                                           |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                           |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                           |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                           |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                           |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                           |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                    |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                            |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                    |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                           |

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

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

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-dateday"></a>メソッド dateDay

    public int dateDay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dateformat"></a>メソッド dateFormat

    public int dateFormat([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datemonth"></a>メソッド dateMonth

    public int dateMonth([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dateseparator"></a>メソッド dateSeparator

    public int dateSeparator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datetimevalue"></a>メソッド dateTimeValue

    public DateTime dateTimeValue([DateTime value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dateyear"></a>メソッド dateYear

    public int dateYear([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayoption"></a>メソッド displayOption

    public int displayOption([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-maxdatelabel"></a>メソッド maxDateLabel

    public str maxDateLabel([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-timeformat"></a>メソッド timeFormat

    public int timeFormat([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-timehours"></a>メソッド timeHours

    public int timeHours([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-timeminute"></a>メソッド timeMinute

    public int timeMinute([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-timeseconds"></a>メソッド timeSeconds

    public int timeSeconds([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-timeseparator"></a>メソッド timeSeparator

    public int timeSeparator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-timezoneindicator"></a>メソッド timeZoneIndicator

    public int timeZoneIndicator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-timezonepreference"></a>メソッド timezonePreference

    public int timezonePreference([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuilddesign"></a>クラス FormBuildDesign
    class FormBuildDesign extends Object

FormBuildDesign クラスは、フォーム デザインを変更します。

### <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                          | 説明                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| public Object addControl(FormControlType controlType, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\]) |                                                                             |
| public Object addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])          |                                                                             |
| public boolean alignChild(\[boolean value\])                                                                                    |                                                                             |
| public boolean alignChildren(\[boolean value\])                                                                                 |                                                                             |
| public boolean allowDocking(\[boolean value\])                                                                                  |                                                                             |
| public boolean allowFormCompanyChange(\[boolean value\])                                                                        |                                                                             |
| public boolean allowImplicitParent(\[boolean value\])                                                                           |                                                                             |
| public int allowUserSetup(\[int value\])                                                                                        |                                                                             |
| public boolean alwaysOnTop(\[boolean value\])                                                                                   |                                                                             |
| public int arrangeGuide(\[int value\])                                                                                          |                                                                             |
| public int arrangeMethod(\[int value\])                                                                                         |                                                                             |
| public int arrangeWhen(\[int value\])                                                                                           |                                                                             |
| public int backgroundColor(\[int value\])                                                                                       | コントロールの背景色を取得または設定します。                           |
| public int bold(\[int value\])                                                                                                  | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。 |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                                       |                                                                             |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                                             |                                                                             |
| public int bottomMarginValue(\[int value\])                                                                                     |                                                                             |
| public str caption(\[str value\])                                                                                               | コントロールのキャプションを取得または設定します。                                     |
| public int characterSet(\[int value\])                                                                                          | フォントの文字セットを取得または設定します。                                 |
| public int colorScheme(\[int value\])                                                                                           | コントロールの配色を取得または設定します。                               |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                                         |                                                                             |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                                            |                                                                             |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                                        |                                                                             |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                                              |                                                                             |
| public int columnspaceValue(\[int value\])                                                                                      |                                                                             |
| public int columnsValue(\[int value\])                                                                                          |                                                                             |
| public Object control(AnyType control)                                                                                          |                                                                             |
| public int controlCount()                                                                                                       |                                                                             |
| public FormBuildControl controlNum(int controlNo)                                                                               |                                                                             |
| public str cssClass(\[str value\])                                                                                              |                                                                             |
| public int dataSource(\[AnyType value\])                                                                                        | コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。  |
| public str defaultAction(\[str value\])                                                                                         |                                                                             |
| public str font(\[str value\])                                                                                                  | 使用するコントロールのフォントの名前を取得または設定します。                   |
| public int fontSize(\[int value\])                                                                                              | 使用するコントロールのフォントのサイズを取得または設定します。                   |
| public int frame(\[int value\])                                                                                                 |                                                                             |
| public int height(int value, \[int mode\])                                                                                      | コントロールの高さを取得または設定します。                                     |
| public int heightMode(\[int value\])                                                                                            | コントロールの高さの計算方法を取得または設定します。              |
| public int heightValue(\[int value\])                                                                                           | コントロールの高さを取得または設定します。                                     |
| public boolean hideIfEmpty(\[boolean value\])                                                                                   |                                                                             |
| public boolean hideToolbar(\[boolean value\])                                                                                   |                                                                             |
| public int imagemode(\[int value\])                                                                                             |                                                                             |
| public str imageName(\[str value\])                                                                                             |                                                                             |
| public int imageResource(\[int value\])                                                                                         |                                                                             |
| public boolean italic(\[boolean value\])                                                                                        |                                                                             |
| public int labelBold(\[int value\])                                                                                             |                                                                             |
| public int labelCharacterSet(\[int value\])                                                                                     |                                                                             |
| public str labelFont(\[str value\])                                                                                             |                                                                             |
| public int labelFontSize(\[int value\])                                                                                         |                                                                             |
| public boolean labelItalic(\[boolean value\])                                                                                   |                                                                             |
| public boolean labelUnderline(\[boolean value\])                                                                                |                                                                             |
| public int left(int value, \[int mode\])                                                                                        |                                                                             |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                                         |                                                                             |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                                               |                                                                             |
| public int leftMarginValue(\[int value\])                                                                                       |                                                                             |
| public int leftMode(\[int value\])                                                                                              |                                                                             |
| public int leftValue(\[int value\])                                                                                             |                                                                             |
| public str localWebMenu(\[str value\])                                                                                          |                                                                             |
| public boolean maximizeBox(\[boolean value\])                                                                                   |                                                                             |
| public boolean minimizeBox(\[boolean value\])                                                                                   |                                                                             |
| public int mode(\[int value\])                                                                                                  |                                                                             |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                                             |                                                                             |
| public str newRecordAction(\[str value\])                                                                                       |                                                                             |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                                        |                                                                             |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                                              |                                                                             |
| public int rightMarginValue(\[int value\])                                                                                      |                                                                             |
| public boolean saveSize(\[boolean value\])                                                                                      |                                                                             |
| public int scrollbars(\[int value\])                                                                                            |                                                                             |
| public boolean setCompany(\[boolean value\])                                                                                    |                                                                             |
| public int showDeleteButton(\[int value\])                                                                                      |                                                                             |
| public int showNewButton(\[int value\])                                                                                         |                                                                             |
| public int showWebHelp(\[int value\])                                                                                           |                                                                             |
| public int statusBarStyle(\[int value\])                                                                                        |                                                                             |
| public int style(\[int value\])                                                                                                 |                                                                             |
| public int submitMethod(\[int value\])                                                                                          |                                                                             |
| public boolean supportReload(\[boolean value\])                                                                                 |                                                                             |
| public int titleDatasource(\[AnyType value\])                                                                                   |                                                                             |
| public int top(int value, \[int mode\])                                                                                         |                                                                             |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                                          |                                                                             |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                                                |                                                                             |
| public int topMarginValue(\[int value\])                                                                                        |                                                                             |
| public int topMode(\[int value\])                                                                                               |                                                                             |
| public int topValue(\[int value\])                                                                                              |                                                                             |
| public boolean underline(\[boolean value\])                                                                                     |                                                                             |
| public int useCaptionFromMenuItem(\[int value\])                                                                                |                                                                             |
| public int viewEditMode(\[int value\])                                                                                          |                                                                             |
| public boolean visible(\[boolean value\])                                                                                       |                                                                             |
| public int width(int value, \[int mode\])                                                                                       | コントロールの幅を取得または設定します。                                      |
| public int widthMode(\[int value\])                                                                                             | コントロールの幅の計算方法を取得または設定します。              |
| public int widthValue(\[int value\])                                                                                            | コントロールの幅を取得または設定します。                                      |
| public int windowResize(\[int value\])                                                                                          |                                                                             |
| public int windowType(\[int value\])                                                                                            |                                                                             |
| public int workflowDatasource(\[AnyType value\])                                                                                |                                                                             |
| public boolean workflowEnabled(\[boolean value\])                                                                               |                                                                             |
| public str workflowType(\[str value\])                                                                                          |                                                                             |
| public int dialogSize(\[int value\])                                                                                            |                                                                             |

### <a name="method-addcontrol"></a>メソッド addControl

    public Object addControl(FormControlType controlType, str controlName, [FormBuildControl insertAfter], [boolean pushFront])

#### <a name="parameters"></a>パラメーター

controlType  

<!-- -->

controlName  

<!-- -->

insertAfter  

<!-- -->

pushFront  

#### <a name="return-value"></a>戻り値

### <a name="method-addcontrolex"></a>メソッド addControlEx

    public Object addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])

#### <a name="parameters"></a>パラメーター

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

<!-- -->

pushFront  

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

### <a name="method-allowdocking"></a>メソッド allowDocking

    public boolean allowDocking([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowformcompanychange"></a>メソッド allowFormCompanyChange

    public boolean allowFormCompanyChange([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowimplicitparent"></a>メソッド allowImplicitParent

    public boolean allowImplicitParent([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowusersetup"></a>メソッド allowUserSetup

    public int allowUserSetup([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-alwaysontop"></a>メソッド alwaysOnTop

    public boolean alwaysOnTop([boolean value])

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

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

### <a name="method-control"></a>メソッド control

    public Object control(AnyType control)

#### <a name="parameters"></a>パラメーター

control  

#### <a name="return-value"></a>戻り値

### <a name="method-controlcount"></a>メソッド controlCount

    public int controlCount()

#### <a name="return-value"></a>戻り値

### <a name="method-controlnum"></a>メソッド controlNum

    public FormBuildControl controlNum(int controlNo)

#### <a name="parameters"></a>パラメーター

controlNo  

#### <a name="return-value"></a>戻り値

### <a name="method-cssclass"></a>メソッド cssClass

    public str cssClass([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-defaultaction"></a>メソッド defaultAction

    public str defaultAction([str value])

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

### <a name="method-frame"></a>メソッド frame

    public int frame([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hidetoolbar"></a>メソッド hideToolbar

    public boolean hideToolbar([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-imagemode"></a>メソッド imagemode

    public int imagemode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-imagename"></a>メソッド imageName

    public str imageName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-imageresource"></a>メソッド imageResource

    public int imageResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

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

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-localwebmenu"></a>メソッド localWebMenu

    public str localWebMenu([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-maximizebox"></a>メソッド maximizeBox

    public boolean maximizeBox([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-minimizebox"></a>メソッド minimizeBox

    public boolean minimizeBox([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mode"></a>メソッド mode

    public int mode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-movecontrol"></a>メソッド moveControl

    public int moveControl(int controlId, [int insertAfterControlId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterControlId  

#### <a name="return-value"></a>戻り値

### <a name="method-newrecordaction"></a>メソッド newRecordAction

    public str newRecordAction([str value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-savesize"></a>メソッド saveSize

    public boolean saveSize([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-scrollbars"></a>メソッド scrollbars

    public int scrollbars([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-setcompany"></a>メソッド setCompany

    public boolean setCompany([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showdeletebutton"></a>メソッド showDeleteButton

    public int showDeleteButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-shownewbutton"></a>メソッド showNewButton

    public int showNewButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showwebhelp"></a>メソッド showWebHelp

    public int showWebHelp([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-statusbarstyle"></a>メソッド statusBarStyle

    public int statusBarStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-submitmethod"></a>メソッド submitMethod

    public int submitMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-supportreload"></a>メソッド supportReload

    public boolean supportReload([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-titledatasource"></a>メソッド titleDatasource

    public int titleDatasource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-usecaptionfrommenuitem"></a>メソッド useCaptionFromMenuItem

    public int useCaptionFromMenuItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-windowresize"></a>メソッド windowResize

    public int windowResize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-windowtype"></a>メソッド windowType

    public int windowType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-workflowdatasource"></a>メソッド workflowDatasource

    public int workflowDatasource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-workflowenabled"></a>メソッド workflowEnabled

    public boolean workflowEnabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-workflowtype"></a>メソッド workflowType

    public str workflowType([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dialogsize"></a>メソッド dialogSize

    public int dialogSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

## <a name="class-formbuilddropdialogbuttoncontrol"></a>クラス FormBuildDropDialogButtonControl
    class FormBuildDropDialogButtonControl extends FormBuildControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                  |
| public int alignment(\[int value\])                                                                         |                                                                                                                                           |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                       |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public boolean autoRefreshData(\[boolean value\])                                                           |                                                                                                                                           |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                         |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                             |
| public boolean big(\[boolean value\])                                                                       |                                                                                                                                           |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                               |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                  |
| public int buttonDisplay(\[int value\])                                                                     | ボタン コントロールの外観を取得または設定します。                                                                                        |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                   |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                               |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                       |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                 |
| public int copyCallerQuery(\[int value\])                                                                   |                                                                                                                                           |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                           |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                           |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                  |
| public boolean defaultButton(\[boolean value\])                                                             | ボタンをフォーム上の既定のボタンにするかどうかを指定します。                                                                   |
| public str disabledImage(\[str value\])                                                                     | コントロールの無効な画像を取得または設定します。                                                                                            |
| public int disabledImageLocation(\[int value\])                                                             |                                                                                                                                           |
| public int disabledResource(\[int value\])                                                                  | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                            |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                           |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                 |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                 |
| public boolean forcedToOverflow(\[boolean value\])                                                          |                                                                                                                                           |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                       |
| public int formViewOption(\[int value\])                                                                    |                                                                                                                                           |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                   |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                            |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                   |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                           |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                          |
| public int imageLocation(\[int value\])                                                                     |                                                                                                                                           |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                              |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                           |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                           |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                           |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                           |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                           |
| public str menuItemName(\[str value\])                                                                      |                                                                                                                                           |
| public int multiSelect(\[int value\])                                                                       |                                                                                                                                           |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                           |
| public int needsRecord(\[int value\])                                                                       |                                                                                                                                           |
| public str normalImage(\[str value\])                                                                       |                                                                                                                                           |
| public int normalResource(\[int value\])                                                                    |                                                                                                                                           |
| public int openMode(\[int value\])                                                                          |                                                                                                                                           |
| public str parameters(\[str value\])                                                                        | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                    |
| public boolean primary(\[boolean value\])                                                                   |                                                                                                                                           |
| public boolean saveRecord(\[boolean value\])                                                                |                                                                                                                                           |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                           |
| public boolean sendExternalContext(\[boolean value\])                                                       |                                                                                                                                           |
| public int shortkey(\[int value\])                                                                          |                                                                                                                                           |
| public boolean showShortCut(\[boolean value\])                                                              |                                                                                                                                           |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                           |
| public int style(\[int value\])                                                                             |                                                                                                                                           |
| public str text(\[str value\])                                                                              |                                                                                                                                           |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                           |
| public int topMode(\[int value\])                                                                           |                                                                                                                                           |
| public int topValue(\[int value\])                                                                          |                                                                                                                                           |
| public int type(\[int value\])                                                                              |                                                                                                                                           |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                           |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                           |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                           |
| public boolean value(\[boolean value\])                                                                     |                                                                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                           |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                           |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                    |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                            |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                    |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                           |

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

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

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
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-copycallerquery"></a>メソッド copyCallerQuery

    public int copyCallerQuery([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-defaultbutton"></a>メソッド defaultButton

ボタンをフォーム上の既定のボタンにするかどうかを指定します。

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

このプロパティは、disabledResourceproperty に優先します。 これらのプロパティの両方が設定されている場合に使用されます。

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

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

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

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-multiselect"></a>メソッド multiSelect

    public int multiSelect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 ignore が渡された場合、パラメータが認識されません。

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

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

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

### <a name="method-showshortcut"></a>メソッド showShortCut

    public boolean showShortCut([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-value"></a>メソッド value

    public boolean value([boolean value])

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildfasttabheadercontrol"></a>クラス FormBuildFastTabHeaderControl
    class FormBuildFastTabHeaderControl extends FormBuildControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignChild(\[boolean value\])                                                                |                                                                                                                                           |
| public boolean alignChildren(\[boolean value\])                                                             |                                                                                                                                           |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                  |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                       |
| public int allowUserSetup(\[int value\])                                                                    |                                                                                                                                           |
| public int arrangeGuide(\[int value\])                                                                      |                                                                                                                                           |
| public int arrangeMethod(\[int value\])                                                                     |                                                                                                                                           |
| public int arrangeWhen(\[int value\])                                                                       |                                                                                                                                           |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                         |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                            |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                       |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                           |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                         |                                                                                                                                           |
| public int bottomMarginValue(\[int value\])                                                                 |                                                                                                                                           |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                   |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                               |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                             |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                     |                                                                                                                                           |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                        |                                                                                                                                           |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                           |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                          |                                                                                                                                           |
| public int columnspaceValue(\[int value\])                                                                  |                                                                                                                                           |
| public int columnsValue(\[int value\])                                                                      |                                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                       |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                 |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                           |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                           |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                           |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                 |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                   |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                            |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                   |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public boolean hideIfEmpty(\[boolean value\])                                                               |                                                                                                                                           |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                           |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                          |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                              |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                           |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                           |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                     |                                                                                                                                           |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                           |                                                                                                                                           |
| public int leftMarginValue(\[int value\])                                                                   |                                                                                                                                           |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                           |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                           |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         | コントロールに指定されたコントロールを移動します。                                                                                                 |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                           |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                           |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                          |                                                                                                                                           |
| public int rightMarginValue(\[int value\])                                                                  |                                                                                                                                           |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                           |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                           |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                           |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                           |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                            |                                                                                                                                           |
| public int topMarginValue(\[int value\])                                                                    |                                                                                                                                           |
| public int topMode(\[int value\])                                                                           |                                                                                                                                           |
| public int topValue(\[int value\])                                                                          |                                                                                                                                           |
| public int type(\[int value\])                                                                              |                                                                                                                                           |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                           |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                           |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                           |
| public boolean useUserLayout(\[boolean value\])                                                             |                                                                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                           |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                           |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                    |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                            |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                    |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                           |

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

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

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

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

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

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

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-movecontrol"></a>メソッド moveControl

コントロールに指定されたコントロールを移動します。

    public int moveControl(int controlId, [int insertAfterControlId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterControlId  

#### <a name="return-value"></a>戻り値

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

#### <a name="remarks"></a>備考

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildfasttabsummaryseparator"></a>クラス FormBuildFastTabSummarySeparator
    class FormBuildFastTabSummarySeparator extends FormBuildControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                  |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                       |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                         |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                            |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                               |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                               |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                       |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                 |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                           |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                           |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                           |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                 |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                 |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                   |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                            |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                   |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                           |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                          |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                              |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                           |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                           |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                           |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                           |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                           |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                           |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                           |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                           |
| public int topMode(\[int value\])                                                                           |                                                                                                                                           |
| public int topValue(\[int value\])                                                                          |                                                                                                                                           |
| public int type(\[int value\])                                                                              |                                                                                                                                           |
| public boolean underline(\[boolean value\])                                                                 |                                                                                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                           |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                           |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                           |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                           |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                    |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                            |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                    |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                           |

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

次のテーブルの値は、中東言語語版 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については、MSDN Web サイト、http://go.microsoft.com/fwlink/?LinkID=85972 で LOGFONT 構造を参照してください。

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
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

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

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

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

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

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

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

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

### <a name="method-underline"></a>メソッド underline

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

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

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  






