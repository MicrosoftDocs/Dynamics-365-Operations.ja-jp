---
title: FormBuildDesign クラス
description: このトピックでは、FormBuildDesign クラスについて説明します。
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
ms.openlocfilehash: 355e0be156dedcc9549b275ca84abe8c4d1ce4b6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502652"
---
# <a name="class-formbuilddesign"></a>クラス FormBuildDesign

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildDesign extends Object
```

FormBuildDesign クラスは、フォーム デザインを変更します。

## <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-addcontrol"></a>メソッド addControl

```xpp
public Object addControl(FormControlType controlType, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrol"></a>パラメーター - addControl

controlType  

<!-- -->

controlName  

<!-- -->

insertAfter  

<!-- -->

pushFront  

### <a name="return-value---addcontrol"></a>戻り値 - addControl

## <a name="method-addcontrolex"></a>メソッド addControlEx

```xpp
public Object addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrolex"></a>パラメーター - addControlEx

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

<!-- -->

pushFront  

### <a name="return-value---addcontrolex"></a>戻り値 - addControlEx

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

## <a name="method-allowdocking"></a>メソッド allowDocking

```xpp
public boolean allowDocking([boolean value])
```

### <a name="parameters---allowdocking"></a>パラメーター - allowDocking

値  

### <a name="return-value---allowdocking"></a>戻り値 - allowDocking

## <a name="method-allowformcompanychange"></a>メソッド allowFormCompanyChange

```xpp
public boolean allowFormCompanyChange([boolean value])
```

### <a name="parameters---allowformcompanychange"></a>パラメーター - allowFormCompanyChange

値  

### <a name="return-value---allowformcompanychange"></a>戻り値 - allowFormCompanyChange

## <a name="method-allowimplicitparent"></a>メソッド allowImplicitParent

```xpp
public boolean allowImplicitParent([boolean value])
```

### <a name="parameters---allowimplicitparent"></a>パラメーター - allowImplicitParent

値  

### <a name="return-value---allowimplicitparent"></a>戻り値 - allowImplicitParent

## <a name="method-allowusersetup"></a>メソッド allowUserSetup

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a>パラメーター - allowUserSetup

値  

### <a name="return-value---allowusersetup"></a>戻り値 - allowUserSetup

## <a name="method-alwaysontop"></a>メソッド alwaysOnTop

```xpp
public boolean alwaysOnTop([boolean value])
```

### <a name="parameters---alwaysontop"></a>パラメーター - alwaysOnTop

値  

### <a name="return-value---alwaysontop"></a>戻り値 - alwaysOnTop

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

## <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a>パラメーター - backgroundColor

値  

### <a name="return-value---backgroundcolor"></a>戻り値 - backgroundColor

パックされた RGB カラーを含む整数。

### <a name="remarks---backgroundcolor"></a>備考 - backgroundColor

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

## <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a>パラメーター - bold

値  

### <a name="return-value---bold"></a>戻り値 - bold

0 から 9 までの間の整数値。

### <a name="remarks---bold"></a>備考 - bold

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

## <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a>パラメーター - caption

値  

### <a name="return-value---caption"></a>戻り値 - caption

コントロールのキャプションとして使用される文字列。

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

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

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

| 値です。 | スタイル。                        |
|--------|-------------------------------|
| 0      | 既定。                      |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。        |

## <a name="method-columns"></a>メソッド columns

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a>パラメーター - columns

値  

<!-- -->

モード  

### <a name="return-value---columns"></a>戻り値 - columns

## <a name="method-columnsmode"></a>メソッド columnsMode

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
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

## <a name="method-control"></a>メソッド control

```xpp
public Object control(AnyType control)
```

### <a name="parameters---control"></a>パラメーター - control

control  

### <a name="return-value---control"></a>戻り値 - control

## <a name="method-controlcount"></a>メソッド controlCount

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a>戻り値 - controlCount

## <a name="method-controlnum"></a>メソッド controlNum

```xpp
public FormBuildControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a>パラメーター - controlNum

controlNo  

### <a name="return-value---controlnum"></a>戻り値 - controlNum

## <a name="method-cssclass"></a>メソッド cssClass

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a>パラメーター - cssClass

値  

### <a name="return-value---cssclass"></a>戻り値 - cssClass

## <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

値  

### <a name="return-value---datasource"></a>戻り値 - dataSource

使用されるデータ ソースの ID。

## <a name="method-defaultaction"></a>メソッド defaultAction

```xpp
public str defaultAction([str value])
```

### <a name="parameters---defaultaction"></a>パラメーター - defaultAction

値  

### <a name="return-value---defaultaction"></a>戻り値 - defaultAction

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

## <a name="method-frame"></a>メソッド frame

```xpp
public int frame([int value])
```

### <a name="parameters---frame"></a>パラメーター - frame

値  

### <a name="return-value---frame"></a>戻り値 - frame

## <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a>パラメーター - height

値  

<!-- -->

モード  

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

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

ピクセル単位の高さ。

### <a name="remarks---heightvalue"></a>備考 - heightValue

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

## <a name="method-hideifempty"></a>メソッド hideIfEmpty

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a>パラメーター - hideIfEmpty

値  

### <a name="return-value---hideifempty"></a>戻り値 - hideIfEmpty

## <a name="method-hidetoolbar"></a>メソッド hideToolbar

```xpp
public boolean hideToolbar([boolean value])
```

### <a name="parameters---hidetoolbar"></a>パラメーター - hideToolbar

値  

### <a name="return-value---hidetoolbar"></a>戻り値 - hideToolbar

## <a name="method-imagemode"></a>メソッド imagemode

```xpp
public int imagemode([int value])
```

### <a name="parameters---imagemode"></a>パラメーター - imagemode

値  

### <a name="return-value---imagemode"></a>戻り値 - imagemode

## <a name="method-imagename"></a>メソッド imageName

```xpp
public str imageName([str value])
```

### <a name="parameters---imagename"></a>パラメーター - imageName

値  

### <a name="return-value---imagename"></a>戻り値 - imageName

## <a name="method-imageresource"></a>メソッド imageResource

```xpp
public int imageResource([int value])
```

### <a name="parameters---imageresource"></a>パラメーター - imageResource

値  

### <a name="return-value---imageresource"></a>戻り値 - imageResource

## <a name="method-italic"></a>メソッド italic

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a>パラメーター - italic

値  

### <a name="return-value---italic"></a>戻り値 - italic

## <a name="method-labelbold"></a>メソッド labelBold

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a>パラメーター - labelBold

値  

### <a name="return-value---labelbold"></a>戻り値 - labelBold

## <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a>パラメーター - labelCharacterSet

値  

### <a name="return-value---labelcharacterset"></a>戻り値 - labelCharacterSet

## <a name="method-labelfont"></a>メソッド labelFont

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a>パラメーター - labelFont

値  

### <a name="return-value---labelfont"></a>戻り値 - labelFont

## <a name="method-labelfontsize"></a>メソッド labelFontSize

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a>パラメーター - labelFontSize

値  

### <a name="return-value---labelfontsize"></a>戻り値 - labelFontSize

## <a name="method-labelitalic"></a>メソッド labelItalic

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a>パラメーター - labelItalic

値  

### <a name="return-value---labelitalic"></a>戻り値 - labelItalic

## <a name="method-labelunderline"></a>メソッド labelUnderline

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a>パラメーター - labelUnderline

値  

### <a name="return-value---labelunderline"></a>戻り値 - labelUnderline

## <a name="method-left"></a>メソッド left

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a>パラメーター - left

値  

<!-- -->

モード  

### <a name="return-value---left"></a>戻り値 - left

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

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a>パラメーター - leftMode

値  

### <a name="return-value---leftmode"></a>戻り値 - leftMode

## <a name="method-leftvalue"></a>メソッド leftValue

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a>パラメーター - leftValue

値  

### <a name="return-value---leftvalue"></a>戻り値 - leftValue

## <a name="method-localwebmenu"></a>メソッド localWebMenu

```xpp
public str localWebMenu([str value])
```

### <a name="parameters---localwebmenu"></a>パラメーター - localWebMenu

値  

### <a name="return-value---localwebmenu"></a>戻り値 - localWebMenu

## <a name="method-maximizebox"></a>メソッド maximizeBox

```xpp
public boolean maximizeBox([boolean value])
```

### <a name="parameters---maximizebox"></a>パラメーター - maximizeBox

値  

### <a name="return-value---maximizebox"></a>戻り値 - maximizeBox

## <a name="method-minimizebox"></a>メソッド minimizeBox

```xpp
public boolean minimizeBox([boolean value])
```

### <a name="parameters---minimizebox"></a>パラメーター - minimizeBox

値  

### <a name="return-value---minimizebox"></a>戻り値 - minimizeBox

## <a name="method-mode"></a>メソッド mode

```xpp
public int mode([int value])
```

### <a name="parameters---mode"></a>パラメーター - mode

値  

### <a name="return-value---mode"></a>戻り値 - mode

## <a name="method-movecontrol"></a>メソッド moveControl

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a>パラメーター - moveControl

controlId  

<!-- -->

insertAfterControlId  

### <a name="return-value---movecontrol"></a>戻り値 - moveControl

## <a name="method-newrecordaction"></a>メソッド newRecordAction

```xpp
public str newRecordAction([str value])
```

### <a name="parameters---newrecordaction"></a>パラメーター - newRecordAction

値  

### <a name="return-value---newrecordaction"></a>戻り値 - newRecordAction

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

## <a name="method-savesize"></a>メソッド saveSize

```xpp
public boolean saveSize([boolean value])
```

### <a name="parameters---savesize"></a>パラメーター - saveSize

値  

### <a name="return-value---savesize"></a>戻り値 - saveSize

## <a name="method-scrollbars"></a>メソッド scrollbars

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a>パラメーター - scrollbars

値  

### <a name="return-value---scrollbars"></a>戻り値 - scrollbars

## <a name="method-setcompany"></a>メソッド setCompany

```xpp
public boolean setCompany([boolean value])
```

### <a name="parameters---setcompany"></a>パラメーター - setCompany

値  

### <a name="return-value---setcompany"></a>戻り値 - setCompany

## <a name="method-showdeletebutton"></a>メソッド showDeleteButton

```xpp
public int showDeleteButton([int value])
```

### <a name="parameters---showdeletebutton"></a>パラメーター - showDeleteButton

値  

### <a name="return-value---showdeletebutton"></a>戻り値 - showDeleteButton

## <a name="method-shownewbutton"></a>メソッド showNewButton

```xpp
public int showNewButton([int value])
```

### <a name="parameters---shownewbutton"></a>パラメーター - showNewButton

値  

### <a name="return-value---shownewbutton"></a>戻り値 - showNewButton

## <a name="method-showwebhelp"></a>メソッド showWebHelp

```xpp
public int showWebHelp([int value])
```

### <a name="parameters---showwebhelp"></a>パラメーター - showWebHelp

値  

### <a name="return-value---showwebhelp"></a>戻り値 - showWebHelp

## <a name="method-statusbarstyle"></a>メソッド statusBarStyle

```xpp
public int statusBarStyle([int value])
```

### <a name="parameters---statusbarstyle"></a>パラメーター - statusBarStyle

値  

### <a name="return-value---statusbarstyle"></a>戻り値 - statusBarStyle

## <a name="method-style"></a>メソッド style

```xpp
public int style([int value])
```

### <a name="parameters---style"></a>パラメーター - style

値  

### <a name="return-value---style"></a>戻り値 - style

## <a name="method-submitmethod"></a>メソッド submitMethod

```xpp
public int submitMethod([int value])
```

### <a name="parameters---submitmethod"></a>パラメーター - submitMethod

値  

### <a name="return-value---submitmethod"></a>戻り値 - submitMethod

## <a name="method-supportreload"></a>メソッド supportReload

```xpp
public boolean supportReload([boolean value])
```

### <a name="parameters---supportreload"></a>パラメーター - supportReload

値  

### <a name="return-value---supportreload"></a>戻り値 - supportReload

## <a name="method-titledatasource"></a>メソッド titleDatasource

```xpp
public int titleDatasource([AnyType value])
```

### <a name="parameters---titledatasource"></a>パラメーター - titleDatasource

値  

### <a name="return-value---titledatasource"></a>戻り値 - titleDatasource

## <a name="method-top"></a>メソッド top

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a>パラメーター - top

値  

<!-- -->

モード  

### <a name="return-value---top"></a>戻り値 - top

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

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a>パラメーター - topMode

値  

### <a name="return-value---topmode"></a>戻り値 - topMode

## <a name="method-topvalue"></a>メソッド topValue

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a>パラメーター - topValue

値  

### <a name="return-value---topvalue"></a>戻り値 - topValue

## <a name="method-underline"></a>メソッド underline

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a>パラメーター - underline

値  

### <a name="return-value---underline"></a>戻り値 - underline

## <a name="method-usecaptionfrommenuitem"></a>メソッド useCaptionFromMenuItem

```xpp
public int useCaptionFromMenuItem([int value])
```

### <a name="parameters---usecaptionfrommenuitem"></a>パラメーター - useCaptionFromMenuItem

値  

### <a name="return-value---usecaptionfrommenuitem"></a>戻り値 - useCaptionFromMenuItem

## <a name="method-vieweditmode"></a>メソッド viewEditMode

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a>パラメーター - viewEditMode

値  

### <a name="return-value---vieweditmode"></a>戻り値 - viewEditMode

## <a name="method-visible"></a>メソッド visible

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  

### <a name="return-value---visible"></a>戻り値 - visible

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  

<!-- -->

モード  

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

### <a name="parameters---widthmode"></a>パラメーター - widthValue

値  

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

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

## <a name="method-windowresize"></a>メソッド windowResize

```xpp
public int windowResize([int value])
```

### <a name="parameters---windowresize"></a>パラメーター - windowResize

値  

### <a name="return-value---windowresize"></a>戻り値 - windowResize

## <a name="method-windowtype"></a>メソッド windowType

```xpp
public int windowType([int value])
```

### <a name="parameters---windowtype"></a>パラメーター - windowType

値  

### <a name="return-value---windowtype"></a>戻り値 - windowType

## <a name="method-workflowdatasource"></a>メソッド workflowDatasource

```xpp
public int workflowDatasource([AnyType value])
```

### <a name="parameters---workflowdatasource"></a>パラメーター - workflowDatasource

値  

### <a name="return-value---workflowdatasource"></a>戻り値 - workflowDatasource

## <a name="method-workflowenabled"></a>メソッド workflowEnabled

```xpp
public boolean workflowEnabled([boolean value])
```

### <a name="parameters---workflowenabled"></a>パラメーター - workflowEnabled

値  

### <a name="return-value---workflowenabled"></a>戻り値 - workflowEnabled

## <a name="method-workflowtype"></a>メソッド workflowType

```xpp
public str workflowType([str value])
```

### <a name="parameters---workflowtype"></a>パラメーター - workflowType

値  

### <a name="return-value---workflowtype"></a>戻り値 - workflowType

## <a name="method-dialogsize"></a>メソッド dialogSize

```xpp
public int dialogSize([int value])
```

### <a name="parameters---dialogsize"></a>パラメーター - dialogSize

値  

### <a name="return-value---dialogsize"></a>戻り値 - dialogSize

