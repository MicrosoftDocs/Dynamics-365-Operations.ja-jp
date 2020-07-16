---
title: ReportShapeControl クラス
description: このトピックでは、ReportShapeControl クラスについて説明します。
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
ms.openlocfilehash: 74aec881287a0a36d8cbac9fda8ba35c92a3acff
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502830"
---
# <a name="class-reportshapecontrol"></a>クラス ReportShapeControl

[!include [banner](../../includes/banner.md)]

```xpp
class ReportShapeControl extends ReportControl
```

ReportShapeControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                                                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| public boolean autoDeclaration(\[boolean value\])                        | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                |
| public int bottomMarginAndFrame()                                        |                                                                                                                   |
| public int bottomMarginMode(\[int value\])                               |                                                                                                                   |
| public str bottomMarginStr(\[str value\])                                |                                                                                                                   |
| public Units bottomMarginUnit(\[Units value\])                           |                                                                                                                   |
| public Real bottomMarginValue(\[Real value\])                            |                                                                                                                   |
| public int changeLabelCase(\[int value\])                                |                                                                                                                   |
| public int colorScheme(\[int value\])                                    | コントロールの配色を取得または設定します。                                                                     |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\]) | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                               |
| public ReportFieldType controlType()                                     |                                                                                                                   |
| public str cssClass(\[str value\])                                       |                                                                                                                   |
| public int delete()                                                      |                                                                                                                   |
| public str effectiveFont()                                               |                                                                                                                   |
| public str fontInfoPrinter()                                             |                                                                                                                   |
| public int fontInfoPrinterAscent()                                       |                                                                                                                   |
| public int fontInfoPrinterDescent()                                      |                                                                                                                   |
| public int fontInfoPrinterExtLead()                                      |                                                                                                                   |
| public int fontInfoPrinterHeight()                                       |                                                                                                                   |
| public int fontInfoPrinterIntLead()                                      |                                                                                                                   |
| public str fontInfoScreen()                                              |                                                                                                                   |
| public int fontInfoScreenAscent()                                        |                                                                                                                   |
| public int fontInfoScreenDescent()                                       |                                                                                                                   |
| public int fontInfoScreenExtLead()                                       |                                                                                                                   |
| public int fontInfoScreenHeight()                                        |                                                                                                                   |
| public int fontInfoScreenIntLead()                                       |                                                                                                                   |
| public int foregroundColor(\[int value\])                                | 使用するコントロールのテキストの色を取得または設定します。                                                               |
| public int height100mm(\[int heightExclBorder\])                         |                                                                                                                   |
| public int height100mmInclBorder(\[int heightInclBorder\])               |                                                                                                                   |
| public int heightMode(\[int value\])                                     | コントロールの高さの計算方法を取得または設定します。                                                    |
| public int heightOfWordWrappedString100mm(str string)                    |                                                                                                                   |
| public str heightStr(\[str value\])                                      |                                                                                                                   |
| public Units heightUnit(\[Units value\])                                 |                                                                                                                   |
| public Real heightValue(\[Real value\])                                  | コントロールの高さを取得または設定します。                                                                           |
| public str label(\[str value\])                                          | コントロールのラベルを取得または設定します。                                                                             |
| public int labelBold(\[int value\])                                      |                                                                                                                   |
| public int labelCharacterSet(\[int value\])                              |                                                                                                                   |
| public str labelCssClass(\[str value\])                                  |                                                                                                                   |
| public str labelFont(\[str value\])                                      |                                                                                                                   |
| public int labelFontSize(\[int value\])                                  |                                                                                                                   |
| public boolean labelItalic(\[boolean value\])                            |                                                                                                                   |
| public LineType labelLineBelow(\[LineType value\])                       |                                                                                                                   |
| public LineThickness labelLineThickness(\[LineThickness value\])         |                                                                                                                   |
| public int labelPosition(\[int value\])                                  |                                                                                                                   |
| public int labelTabLeader(\[int value\])                                 |                                                                                                                   |
| public boolean labelUnderline(\[boolean value\])                         |                                                                                                                   |
| public int labelWidthMode(\[int value\])                                 |                                                                                                                   |
| public str labelWidthStr(\[str value\])                                  |                                                                                                                   |
| public Units labelWidthUnit(\[Units value\])                             |                                                                                                                   |
| public Real labelWidthValue(\[Real value\])                              |                                                                                                                   |
| public int left100mm(\[int leftExclBorder\])                             |                                                                                                                   |
| public int left100mmInclBorder(\[int leftInclBorder\])                   |                                                                                                                   |
| public int leftMarginAnFrame()                                           |                                                                                                                   |
| public int leftMarginMode(\[int value\])                                 |                                                                                                                   |
| public str leftMarginStr(\[str value\])                                  |                                                                                                                   |
| public Units leftMarginUnit(\[Units value\])                             |                                                                                                                   |
| public Real leftMarginValue(\[Real value\])                              |                                                                                                                   |
| public int leftMode(\[int value\])                                       |                                                                                                                   |
| public str leftStr(\[str value\])                                        |                                                                                                                   |
| public Units leftUnit(\[Units value\])                                   |                                                                                                                   |
| public Real leftValue(\[Real value\])                                    |                                                                                                                   |
| public LineType line(\[LineType value\])                                 |                                                                                                                   |
| public LineType lineAbove(\[LineType value\])                            |                                                                                                                   |
| public LineType lineBelow(\[LineType value\])                            |                                                                                                                   |
| public LineType lineLeft(\[LineType value\])                             | セクションの左枠として使用される明細行のタイプを取得または設定します。                                       |
| public LineType lineRight(\[LineType value\])                            |                                                                                                                   |
| public str menuItemLabel(\[str value\])                                  |                                                                                                                   |
| public str menuItemName(\[str value\])                                   |                                                                                                                   |
| public MenuItemType menuItemType(\[MenuItemType value\])                 |                                                                                                                   |
| public str modelFieldName(\[str value\])                                 |                                                                                                                   |
| public str name(\[str value\])                                           | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int numberOfLines(int height100mm)                                |                                                                                                                   |
| public int position(\[int value\])                                       |                                                                                                                   |
| public str previewInfo(str string)                                       |                                                                                                                   |
| public int previewXCompensation100mm(str string)                         |                                                                                                                   |
| public int right100mm()                                                  |                                                                                                                   |
| public int right100mmInclBorder()                                        |                                                                                                                   |
| public int rightMarginAndFrame()                                         |                                                                                                                   |
| public int rightMarginMode(\[int value\])                                |                                                                                                                   |
| public str rightMarginStr(\[str value\])                                 |                                                                                                                   |
| public Units rightMarginUnit(\[Units value\])                            |                                                                                                                   |
| public Real rightMarginValue(\[Real value\])                             |                                                                                                                   |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                |                                                                                                                   |
| public str setHeightGetText(int lines, str string)                       |                                                                                                                   |
| public boolean showLabel(\[boolean value\])                              |                                                                                                                   |
| public LineThickness thickness(\[LineThickness value\])                  |                                                                                                                   |
| public int top100mm(\[int topExclBorder\])                               |                                                                                                                   |
| public int top100mmInclBorder(\[int topInclBorder\])                     |                                                                                                                   |
| public int topMarginAndFrame()                                           |                                                                                                                   |
| public int topMarginMode(\[int value\])                                  |                                                                                                                   |
| public str topMarginStr(\[str value\])                                   |                                                                                                                   |
| public Units topMarginUnit(\[Units value\])                              |                                                                                                                   |
| public Real topMarginValue(\[Real value\])                               |                                                                                                                   |
| public int topMode(\[int value\])                                        |                                                                                                                   |
| public str topStr(\[str value\])                                         |                                                                                                                   |
| public Units topUnit(\[Units value\])                                    |                                                                                                                   |
| public Real topValue(\[Real value\])                                     |                                                                                                                   |
| public ShapeType type(\[ShapeType value\])                               |                                                                                                                   |
| public boolean visible(\[boolean value\])                                |                                                                                                                   |
| public str webMenuItemName(\[str value\])                                |                                                                                                                   |
| public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])        |                                                                                                                   |
| public str webTarget(\[str value\])                                      |                                                                                                                   |
| public int width100mm(\[int widthExclBorder\])                           |                                                                                                                   |
| public int width100mmInclBorder(\[int widthInclBorder\])                 |                                                                                                                   |
| public int widthMode(\[int value\])                                      | コントロールの幅の計算方法を取得または設定します。                                                    |
| public int widthOfString100mm(str string)                                |                                                                                                                   |
| public str widthStr(\[str value\])                                       |                                                                                                                   |
| public Units widthUnit(\[Units value\])                                  |                                                                                                                   |
| public Real widthValue(\[Real value\])                                   | コントロールの幅を取得または設定します。                                                                            |
| public void bottomMargin(Real value, Units unit)                         |                                                                                                                   |
| public void left(Real value, Units unit)                                 |                                                                                                                   |
| public void top(Real value, Units unit)                                  |                                                                                                                   |
| public void labelWidth(Real value, Units unit)                           |                                                                                                                   |
| public void height(Real value, Units unit)                               | コントロールの高さを取得または設定します。                                                                           |
| public void leftMargin(Real value, Units unit)                           |                                                                                                                   |
| public void rightMargin(Real value, Units unit)                          |                                                                                                                   |
| public void hide()                                                       |                                                                                                                   |
| public void topMargin(Real value, Units unit)                            |                                                                                                                   |
| public void show()                                                       |                                                                                                                   |
| public void width(Real value, Units unit)                                | コントロールの幅を取得または設定します。                                                                            |

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

### <a name="remarks---autodeclaration"></a>備考 - autoDeclaration

コントロールには同じ名前を付けることはできません。

## <a name="method-bottommarginandframe"></a>メソッド bottomMarginAndFrame

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a>戻り値 - bottomMarginAndFrame

## <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a>パラメーター - bottomMarginMode

値  

### <a name="return-value---bottommarginmode"></a>戻り値 - bottomMarginMode

## <a name="method-bottommarginstr"></a>メソッド bottomMarginStr

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a>パラメーター - bottomMarginStr

値  

### <a name="return-value---bottommarginstr"></a>戻り値 - bottomMarginStr

## <a name="method-bottommarginunit"></a>メソッド bottomMarginUnit

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a>パラメーター - bottomMarginUnit

値  

### <a name="return-value---bottommarginunit"></a>戻り値 - bottomMarginUnit

## <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a>パラメーター - bottomMarginValue

値  

### <a name="return-value---bottommarginvalue"></a>戻り値 - bottomMarginValue

## <a name="method-changelabelcase"></a>メソッド changeLabelCase

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a>パラメーター - changeLabelCase

値  

### <a name="return-value---changelabelcase"></a>戻り値 - changeLabelCase

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

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

## <a name="method-controltype"></a>メソッド controlType

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a>戻り値 - controlType

## <a name="method-cssclass"></a>メソッド cssClass

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a>パラメーター - cssClass

値  

### <a name="return-value---cssclass"></a>戻り値 - cssClass

## <a name="method-delete"></a>メソッド delete

```xpp
public int delete()
```

### <a name="return-value---delete"></a>戻り値 - delete

## <a name="method-effectivefont"></a>メソッド effectiveFont

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a>戻り値 - effectiveFont

## <a name="method-fontinfoprinter"></a>メソッド fontInfoPrinter

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a>戻り値 - fontInfoPrinter

## <a name="method-fontinfoprinterascent"></a>メソッド fontInfoPrinterAscent

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a>戻り値 - fontInfoPrinterAscent

## <a name="method-fontinfoprinterdescent"></a>メソッド fontInfoPrinterDescent

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a>戻り値 - fontInfoPrinterDescent

## <a name="method-fontinfoprinterextlead"></a>メソッド fontInfoPrinterExtLead

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a>戻り値 - fontInfoPrinterExtLead

## <a name="method-fontinfoprinterheight"></a>メソッド fontInfoPrinterHeight

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a>戻り値 - fontInfoPrinterHeight

## <a name="method-fontinfoprinterintlead"></a>メソッド fontInfoPrinterIntLead

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a>戻り値 - fontInfoPrinterIntLead

## <a name="method-fontinfoscreen"></a>メソッド fontInfoScreen

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a>戻り値 - fontInfoScreen

## <a name="method-fontinfoscreenascent"></a>メソッド fontInfoScreenAscent

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a>戻り値 - fontInfoScreenAscent

## <a name="method-fontinfoscreendescent"></a>メソッド fontInfoScreenDescent

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a>戻り値 - fontInfoScreenDescent

## <a name="method-fontinfoscreenextlead"></a>メソッド fontInfoScreenExtLead

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a>戻り値 - fontInfoScreenExtLead

## <a name="method-fontinfoscreenheight"></a>メソッド fontInfoScreenHeight

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a>戻り値 - fontInfoScreenHeight

## <a name="method-fontinfoscreenintlead"></a>メソッド fontInfoScreenIntLead

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a>戻り値 - fontInfoScreenIntLead

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

## <a name="method-height100mm"></a>メソッド height100mm

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a>パラメーター - height100mm

heightExclBorder  

### <a name="return-value---height100mm"></a>戻り値 - height100mm

## <a name="method-height100mminclborder"></a>メソッド height100mmInclBorder

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a>パラメーター - height100mmInclBorder

heightInclBorder  

### <a name="return-value---height100mminclborder"></a>戻り値 - height100mmInclBorder

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

## <a name="method-heightofwordwrappedstring100mm"></a>メソッド heightOfWordWrappedString100mm

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a>パラメーター - heightOfWordWrappedString100mm

文字列  

### <a name="return-value---heightofwordwrappedstring100mm"></a>戻り値 - heightOfWordWrappedString100mm

## <a name="method-heightstr"></a>メソッド heightStr

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a>パラメーター - heightStr

値  

### <a name="return-value---heightstr"></a>戻り値 - heightStr

## <a name="method-heightunit"></a>メソッド heightUnit

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a>パラメーター - heightUnit

値  

### <a name="return-value---heightunit"></a>戻り値 - heightUnit

## <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

ピクセル単位の高さ。

### <a name="remarks---heightvalue"></a>備考 - heightValue

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

## <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

```xpp
public str label([str value])
```

### <a name="parameters---label"></a>パラメーター - label

値  

### <a name="return-value---label"></a>戻り値 - label

ラベル文字列の現在の値。

### <a name="remarks---label"></a>備考 - label

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

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

## <a name="method-labelcssclass"></a>メソッド labelCssClass

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a>パラメーター - labelCssClass

値  

### <a name="return-value---labelcssclass"></a>戻り値 - labelCssClass

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

## <a name="method-labellinebelow"></a>メソッド labelLineBelow

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a>パラメーター - labelLineBelow

値  

### <a name="return-value---labellinebelow"></a>戻り値 - labelLineBelow

## <a name="method-labellinethickness"></a>メソッド labelLineThickness

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a>パラメーター - labelLineThickness

値  

### <a name="return-value---labellinethickness"></a>戻り値 - labelLineThickness

## <a name="method-labelposition"></a>メソッド labelPosition

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a>パラメーター - labelPosition

値  

### <a name="return-value---labelposition"></a>戻り値 - labelPosition

## <a name="method-labeltableader"></a>メソッド labelTabLeader

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a>パラメーター - labelTabLeader

値  

### <a name="return-value---labeltableader"></a>戻り値 - labelTabLeader

## <a name="method-labelunderline"></a>メソッド labelUnderline

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a>パラメーター - labelUnderline

値  

### <a name="return-value---labelunderline"></a>戻り値 - labelUnderline

## <a name="method-labelwidthmode"></a>メソッド labelWidthMode

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a>パラメーター - labelWidthMode

値  

### <a name="return-value---labelwidthmode"></a>戻り値 - labelWidthMode

## <a name="method-labelwidthstr"></a>メソッド labelWidthStr

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a>パラメーター - labelWidthStr

値  

### <a name="return-value---labelwidthstr"></a>戻り値 - labelWidthStr

## <a name="method-labelwidthunit"></a>メソッド labelWidthUnit

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a>パラメーター - labelWidthUnit

値  

### <a name="return-value---labelwidthunit"></a>戻り値 - labelWidthUnit

## <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a>パラメーター - labelWidthValue

値  

### <a name="return-value---labelwidthvalue"></a>戻り値 - labelWidthValue

## <a name="method-left100mm"></a>メソッド left100mm

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a>パラメーター - left100mm

leftExclBorder  

### <a name="return-value---left100mm"></a>戻り値 - left100mm

## <a name="method-left100mminclborder"></a>メソッド left100mmInclBorder

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a>パラメーター - left100mmInclBorder

leftInclBorder  

### <a name="return-value---left100mminclborder"></a>戻り値 - left100mmInclBorder

## <a name="method-leftmarginanframe"></a>メソッド leftMarginAnFrame

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a>戻り値 - leftMarginAnFrame

## <a name="method-leftmarginmode"></a>メソッド leftMarginMode

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a>パラメーター - leftMarginMode

値  

### <a name="return-value---leftmarginmode"></a>戻り値 - leftMarginMode

## <a name="method-leftmarginstr"></a>メソッド leftMarginStr

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a>パラメーター - leftMarginStr

値  

### <a name="return-value---leftmarginstr"></a>戻り値 - leftMarginStr

## <a name="method-leftmarginunit"></a>メソッド leftMarginUnit

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a>パラメーター - leftMarginUnit

値  

### <a name="return-value---leftmarginunit"></a>戻り値 - leftMarginStr

## <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

```xpp
public Real leftMarginValue([Real value])
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

## <a name="method-leftstr"></a>メソッド leftStr

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a>パラメーター - leftStr

値  

### <a name="return-value---leftstr"></a>戻り値 - leftStr

## <a name="method-leftunit"></a>メソッド leftUnit

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a>パラメーター - leftUnit

値  

### <a name="return-value---leftunit"></a>戻り値 - leftUnit

## <a name="method-leftvalue"></a>メソッド leftValue

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a>パラメーター - leftValue

値  

### <a name="return-value---leftvalue"></a>戻り値 - leftValue

## <a name="method-line"></a>メソッド line

```xpp
public LineType line([LineType value])
```

### <a name="parameters---line"></a>パラメーター - line

値  

### <a name="return-value---line"></a>戻り値 - line

## <a name="method-lineabove"></a>メソッド lineAbove

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a>パラメーター - lineAbove

値  

### <a name="return-value---lineabove"></a>戻り値 - lineAbove

## <a name="method-linebelow"></a>メソッド lineBelow

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a>パラメーター - lineBelow

値  

### <a name="return-value---linebelow"></a>戻り値 - lineBelow

## <a name="method-lineleft"></a>メソッド lineLeft

セクションの左枠として使用される明細行のタイプを取得または設定します。

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a>パラメーター - lineLeft

値  

### <a name="return-value---lineleft"></a>戻り値 - lineLeft

左境界線として使用される線のタイプ。

## <a name="method-lineright"></a>メソッド lineRight

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a>パラメーター - lineRight

値  

### <a name="return-value---lineright"></a>戻り値 - lineRight

## <a name="method-menuitemlabel"></a>メソッド menuItemLabel

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a>パラメーター - menuItemLabel

値  

### <a name="return-value---menuitemlabel"></a>戻り値 - menuItemLabel

## <a name="method-menuitemname"></a>メソッド menuItemName

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a>パラメーター - menuItemName

値  

### <a name="return-value---menuitemname"></a>戻り値 - menuItemName

## <a name="method-menuitemtype"></a>メソッド menuItemType

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a>パラメーター - menuItemType

値  

### <a name="return-value---menuitemtype"></a>戻り値 - menuItemType

## <a name="method-modelfieldname"></a>メソッド modelFieldName

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a>パラメーター - modelFieldName

値  

### <a name="return-value---modelfieldname"></a>戻り値 - modelFieldName

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - 名前

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-numberoflines"></a>メソッド numberOfLines

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a>パラメーター - numberOfLines

height100mm  

### <a name="return-value---numberoflines"></a>戻り値 - numberOfLines

## <a name="method-position"></a>メソッドの位置

```xpp
public int position([int value])
```

### <a name="parameters---position"></a>パラメーター - position

値  

### <a name="return-value---position"></a>戻り値 - position

## <a name="method-previewinfo"></a>メソッド previewInfo

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a>パラメーター - previewInfo

文字列  

### <a name="return-value---previewinfo"></a>戻り値 - previewInfo

## <a name="method-previewxcompensation100mm"></a>メソッド previewXCompensation100mm

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a>パラメーター - previewXCompensation100mm

文字列  

### <a name="return-value---previewxcompensation100mm"></a>戻り値 - previewXCompensation100mm

## <a name="method-right100mm"></a>メソッド right100mm

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a>戻り値 - right100mm

## <a name="method-right100mminclborder"></a>メソッド right100mmInclBorder

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a>戻り値 - right100mmInclBorder

## <a name="method-rightmarginandframe"></a>メソッド rightMarginAndFrame

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a>戻り値 - rightMarginAndFrame

## <a name="method-rightmarginmode"></a>メソッド rightMarginMode

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a>パラメーター - rightMarginMode

値  

### <a name="return-value---rightmarginmode"></a>戻り値 - rightMarginMode

## <a name="method-rightmarginstr"></a>メソッド rightMarginStr

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a>パラメーター - rightMarginStr

値  

### <a name="return-value---rightmarginstr"></a>戻り値 - rightMarginStr

## <a name="method-rightmarginunit"></a>メソッド rightMarginUnit

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a>パラメーター - rightMarginUnit

値  

### <a name="return-value---rightmarginunit"></a>戻り値 - rightMarginUnit

## <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a>パラメーター - rightMarginValue

値  

### <a name="return-value---rightmarginvalue"></a>戻り値 - rightMarginValue

## <a name="method-securitykey"></a>メソッド securityKey

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  

### <a name="return-value---securitykey"></a>戻り値 - securityKey

## <a name="method-setheightgettext"></a>メソッド setHeightGetText

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a>パラメーター - setHeightGetText

明細行  

<!-- -->

文字列  

### <a name="return-value---setheightgettext"></a>戻り値 - setHeightGetText

## <a name="method-showlabel"></a>メソッド showLabel

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a>パラメーター - showLabel

値  

### <a name="return-value---showlabel"></a>戻り値 - showLabel

## <a name="method-thickness"></a>メソッド thickness

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a>パラメーター - thickness

値  

### <a name="return-value---thickness"></a>戻り値 - thickness

## <a name="method-top100mm"></a>メソッド top100mm

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a>パラメーター - top100mm

topExclBorder  

### <a name="return-value---top100mm"></a>戻り値 - top100mm

## <a name="method-top100mminclborder"></a>メソッド top100mmInclBorder

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a>パラメーター - top100mmInclBorder

topInclBorder  

### <a name="return-value---top100mminclborder"></a>戻り値 - top100mmInclBorder

## <a name="method-topmarginandframe"></a>メソッド topMarginAndFrame

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a>戻り値 - topMarginAndFrame

## <a name="method-topmarginmode"></a>メソッド topMarginMode

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a>パラメーター - topMarginMode

値  

### <a name="return-value---topmarginmode"></a>戻り値 - topMarginMode

## <a name="method-topmarginstr"></a>メソッド topMarginStr

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a>パラメーター - topMarginStr

値  

### <a name="return-value---topmarginstr"></a>戻り値 - topMarginStr

## <a name="method-topmarginunit"></a>メソッド topMarginUnit

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a>パラメーター - topMarginUnit

値  

### <a name="return-value---topmarginunit"></a>戻り値 - topMarginUnit

## <a name="method-topmarginvalue"></a>メソッド topMarginValue

```xpp
public Real topMarginValue([Real value])
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

## <a name="method-topstr"></a>メソッド topStr

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a>パラメーター - topStr

値  

### <a name="return-value---topstr"></a>戻り値 - topStr

## <a name="method-topunit"></a>メソッド topUnit

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a>パラメーター - topUnit

値  

### <a name="return-value---topunit"></a>戻り値 - topUnit

## <a name="method-topvalue"></a>メソッド topValue

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a>パラメーター - topValue

値  

### <a name="return-value---topvalue"></a>戻り値 - topValue

## <a name="method-type"></a>メソッドのタイプ

```xpp
public ShapeType type([ShapeType value])
```

### <a name="parameters---type"></a>パラメーター - タイプ

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-visible"></a>メソッド visible

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  

### <a name="return-value---visible"></a>戻り値 - visible

## <a name="method-webmenuitemname"></a>メソッド webMenuItemName

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a>パラメーター - webMenuItemName

値  

### <a name="return-value---webmenuitemname"></a>戻り値 - webMenuItemName

## <a name="method-webmenuitemtype"></a>メソッド webMenuItemType

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a>パラメーター - webMenuItemType

値  

### <a name="return-value---webmenuitemtype"></a>戻り値 - webMenuItemType

## <a name="method-webtarget"></a>メソッド webTarget

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a>パラメーター - webTarget

値  

### <a name="return-value---webtarget"></a>戻り値 - webTarget

## <a name="method-width100mm"></a>メソッド width100mm

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a>パラメーター - width100mm

widthExclBorder  

### <a name="return-value---width100mm"></a>戻り値 - width100mm

## <a name="method-width100mminclborder"></a>メソッド width100mmInclBorder

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a>パラメーター - width100mmInclBorder

widthInclBorder  

### <a name="return-value---width100mminclborder"></a>戻り値 - width100mmInclBorder

## <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a>パラメーター - widthMode

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

## <a name="method-widthofstring100mm"></a>メソッド widthOfString100mm

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a>パラメーター - widthOfString100mm

文字列  

### <a name="return-value---widthofstring100mm"></a>戻り値 - widthOfString100mm

## <a name="method-widthstr"></a>メソッド widthStr

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a>パラメーター - widthStr

値  

### <a name="return-value---widthstr"></a>戻り値 - widthStr

## <a name="method-widthunit"></a>メソッド widthUnit

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a>パラメーター - widthUnit

値  

### <a name="return-value---widthunit"></a>戻り値 - widthUnit

## <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

## <a name="method-bottommargin"></a>メソッド bottomMargin

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a>パラメーター - bottomMargin

値  

<!-- -->

単位  

## <a name="method-left"></a>メソッド left

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a>パラメーター - left

値  

<!-- -->

単位  

## <a name="method-top"></a>メソッド top

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a>パラメーター - top

値  

<!-- -->

単位  

## <a name="method-labelwidth"></a>メソッド labelWidth

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a>パラメーター - labelWidth

値  

<!-- -->

単位  

## <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a>パラメーター - height

値  

<!-- -->

単位  

### <a name="remarks---height"></a>備考 - height

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

## <a name="method-leftmargin"></a>メソッド leftMargin

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a>パラメーター - leftMargin

値  

<!-- -->

単位  

## <a name="method-rightmargin"></a>メソッド rightMargin

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a>パラメーター - rightMargin

値  

<!-- -->

単位  

## <a name="method-hide"></a>メソッド hide

```xpp
public void hide()
```

## <a name="method-topmargin"></a>メソッド topMargin

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a>パラメーター - topMargin

値  

<!-- -->

単位  

## <a name="method-show"></a>メソッド show

```xpp
public void show()
```

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a>パラメーター - width

値  

<!-- -->

単位  

### <a name="remarks---width"></a>備考 - width

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

