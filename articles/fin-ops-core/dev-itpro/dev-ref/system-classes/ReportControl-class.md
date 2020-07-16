---
title: ReportControl クラス
description: このトピックでは、ReportControl クラスについて説明します。
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
ms.openlocfilehash: 1e3a72b41283df067be9d5913abf446f3770b62a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502846"
---
# <a name="class-reportcontrol"></a>クラス ReportControl

[!include [banner](../../includes/banner.md)]

```xpp
class ReportControl extends TreeNode
```

ReportControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                     | 説明 |
|------------------------------------------------------------|-------------|
| public int bottomMarginAndFrame()                          |             |
| public ReportFieldType controlType()                       |             |
| public int delete()                                        |             |
| public str effectiveFont()                                 |             |
| public str fontInfoPrinter()                               |             |
| public int fontInfoPrinterAscent()                         |             |
| public int fontInfoPrinterDescent()                        |             |
| public int fontInfoPrinterExtLead()                        |             |
| public int fontInfoPrinterHeight()                         |             |
| public int fontInfoPrinterIntLead()                        |             |
| public str fontInfoScreen()                                |             |
| public int fontInfoScreenAscent()                          |             |
| public int fontInfoScreenDescent()                         |             |
| public int fontInfoScreenExtLead()                         |             |
| public int fontInfoScreenHeight()                          |             |
| public int fontInfoScreenIntLead()                         |             |
| public int height100mm(\[int heightExclBorder\])           |             |
| public int height100mmInclBorder(\[int heightInclBorder\]) |             |
| public int heightOfWordWrappedString100mm(str string)      |             |
| public int left100mm(\[int leftExclBorder\])               |             |
| public int left100mmInclBorder(\[int leftInclBorder\])     |             |
| public int leftMarginAnFrame()                             |             |
| public int numberOfLines(int height100mm)                  |             |
| public int position(\[int value\])                         |             |
| public str previewInfo(str string)                         |             |
| public int previewXCompensation100mm(str string)           |             |
| public int right100mm()                                    |             |
| public int right100mmInclBorder()                          |             |
| public int rightMarginAndFrame()                           |             |
| public str setHeightGetText(int lines, str string)         |             |
| public int top100mm(\[int topExclBorder\])                 |             |
| public int top100mmInclBorder(\[int topInclBorder\])       |             |
| public int topMarginAndFrame()                             |             |
| public int width100mm(\[int widthExclBorder\])             |             |
| public int width100mmInclBorder(\[int widthInclBorder\])   |             |
| public int widthOfString100mm(str string)                  |             |
| public void show()                                         |             |
| public void hide()                                         |             |

## <a name="method-bottommarginandframe"></a>メソッド bottomMarginAndFrame

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a>戻り値 - bottomMarginAndFrame

## <a name="method-controltype"></a>メソッド controlType

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a>戻り値 - controlType

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

## <a name="method-heightofwordwrappedstring100mm"></a>メソッド heightOfWordWrappedString100mm

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a>パラメーター - heightOfWordWrappedString100mm

文字列  

### <a name="return-value---heightofwordwrappedstring100mm"></a>戻り値 - heightOfWordWrappedString100mm

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

## <a name="method-setheightgettext"></a>メソッド setHeightGetText

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a>パラメーター - setHeightGetText

明細行  

<!-- -->

文字列  

### <a name="return-value---setheightgettext"></a>戻り値 - setHeightGetText

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

## <a name="method-widthofstring100mm"></a>メソッド widthOfString100mm

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a>パラメーター - widthOfString100mm

文字列  

### <a name="return-value---widthofstring100mm"></a>戻り値 - widthOfString100mm

## <a name="method-show"></a>メソッド show

```xpp
public void show()
```

## <a name="method-hide"></a>メソッド hide

```xpp
public void hide()
```

