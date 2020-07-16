---
title: ClientPrintJobSettings クラス
description: このトピックでは、ClientPrintJobSettings クラスについて説明します。
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
ms.openlocfilehash: 362be465f969b9d6e608e024cec8147293e4056b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502711"
---
# <a name="class-clientprintjobsettings"></a>クラス ClientPrintJobSettings

[!include [banner](../../includes/banner.md)]

```xpp
class ClientPrintJobSettings extends PrintJobSettings
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                  | 説明                                     |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public container getFontDimension(container container)                                                                  |                                                 |
| public container getInfoStrings()                                                                                       |                                                 |
| public int getNextLineOffset(container container)                                                                       |                                                 |
| public container getPageInfo()                                                                                          |                                                 |
| public container getPrinterNames()                                                                                      |                                                 |
| public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)                     |                                                 |
| public container getTextWidthExt(container container)                                                                   |                                                 |
| public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight) |                                                 |
| public container getWordWrapInfoExt(container container)                                                                |                                                 |
| public container printerSettingsExt(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])            |                                                 |
| public container setOrientationGetPageInfo(PrinterOrientation orientation)                                              |                                                 |
| public void new(\[container Settings\], \[boolean infoOnly\])                                                           | Object クラスの新しいインスタンスを初期化します。 |

## <a name="method-getfontdimension"></a>メソッド getFontDimension

```xpp
public container getFontDimension(container container)
```

### <a name="parameters---getfontdimension"></a>パラメーター - getFontDimension

コンテナー  

### <a name="return-value---getfontdimension"></a>戻り値 - getFontDimension

## <a name="method-getinfostrings"></a>メソッド getInfoStrings

```xpp
public container getInfoStrings()
```

### <a name="return-value---getinfostrings"></a>戻り値 - getInfoStrings

## <a name="method-getnextlineoffset"></a>メソッド getNextLineOffset

```xpp
public int getNextLineOffset(container container)
```

### <a name="parameters---getnextlineoffset"></a>パラメーター - getNextLineOffset

コンテナー  

### <a name="return-value---getnextlineoffset"></a>戻り値 - getNextLineOffset

## <a name="method-getpageinfo"></a>メソッド getPageInfo

```xpp
public container getPageInfo()
```

### <a name="return-value---getpageinfo"></a>戻り値 - getPageInfo

## <a name="method-getprinternames"></a>メソッド getPrinterNames

```xpp
public container getPrinterNames()
```

### <a name="return-value---getprinternames"></a>戻り値 - getPrinterNames

## <a name="method-gettextwidth"></a>メソッド getTextWidth

```xpp
public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)
```

### <a name="parameters---gettextwidth"></a>パラメーター - getTextWidth

テキスト  

<!-- -->

fontName  

<!-- -->

charSet  

<!-- -->

fontHeight  

<!-- -->

スタイル  

<!-- -->

重量  

### <a name="return-value---gettextwidth"></a>戻り値 - getTextWidth

## <a name="method-gettextwidthext"></a>メソッド getTextWidthExt

```xpp
public container getTextWidthExt(container container)
```

### <a name="parameters---gettextwidthext"></a>パラメーター - getTextWidthExt

コンテナー  

### <a name="return-value---gettextwidthext"></a>戻り値 - getTextWidthExt

## <a name="method-getwordwrapinfo"></a>メソッド getWordWrapInfo

```xpp
public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)
```

### <a name="parameters---getwordwrapinfo"></a>パラメーター - getWordWrapInfo

テキスト  

<!-- -->

width  

<!-- -->

fontName  

<!-- -->

charSet  

<!-- -->

fontHeight  

<!-- -->

スタイル  

<!-- -->

重量  

### <a name="return-value---getwordwrapinfo"></a>戻り値 - getWordWrapInfo

## <a name="method-getwordwrapinfoext"></a>メソッド getWordWrapInfoExt

```xpp
public container getWordWrapInfoExt(container container)
```

### <a name="parameters---getwordwrapinfoext"></a>パラメーター - getWordWrapInfoExt

コンテナー  

### <a name="return-value---getwordwrapinfoext"></a>戻り値 - getWordWrapInfoExt

## <a name="method-printersettingsext"></a>メソッド printerSettingsExt

```xpp
public container printerSettingsExt(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])
```

### <a name="parameters---printersettingsext"></a>パラメーター - printerSettingsExt

formName  

<!-- -->

args  

<!-- -->

reportRun  

<!-- -->

showWhat  

### <a name="return-value---printersettingsext"></a>戻り値 - printerSettingsExt

## <a name="method-setorientationgetpageinfo"></a>メソッド setOrientationGetPageInfo

```xpp
public container setOrientationGetPageInfo(PrinterOrientation orientation)
```

### <a name="parameters---setorientationgetpageinfo"></a>パラメーター - setOrientationGetPageInfo

orientation  

### <a name="return-value---setorientationgetpageinfo"></a>戻り値 - setOrientationGetPageInfo

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([container Settings], [boolean infoOnly])
```

### <a name="parameters---new"></a>パラメーター - new

設定  

<!-- -->

infoOnly  

