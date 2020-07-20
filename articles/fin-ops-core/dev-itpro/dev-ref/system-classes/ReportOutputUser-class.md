---
title: ReportOutputUser クラス
description: このトピックでは、ReportOutputUser クラスについて説明します。
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
ms.openlocfilehash: 19058e8a1ec3932211c21a601fcc1958ebc94124
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502836"
---
# <a name="class-reportoutputuser"></a>クラス ReportOutputUser

[!include [banner](../../includes/banner.md)]

```xpp
class ReportOutputUser extends ReportOutput
```

ReportOutputUser クラスは、レポートの形式のユーザー定義のターゲットを実装します。

## <a name="remarks"></a>備考

既定では、画面、プリンター、ファイル、または電子メール アドレスにレポートを印刷します。 次の API アイテムは、ユーザー定義ノターゲットをサポートしています。

-   ReportOutputUserType システム列挙
-   PrintMedium システム列挙型の ViewerClass 値
-   ClassFactory::createViewer メソッド

レポートが実行されると、ターゲットが PrintMedium::Viewer クラスの場合、Print メソッドによって reportOutputUser オブジェクトが作成されます。 このオブジェクトは、createViewer メソッドを呼び出し、reportOutputUserType を引数の 1 つとして指定することによって作成されます。 その後、レポートは、オブジェクトのメソッド (startReport、startPage、startSection、writeField など) を呼び出すことによって出力されます。 一般に、ターゲットが、たとえばプリンターである場合、reportRun::print メソッドは reportOutput オブジェクトを作成し、印刷メソッドを呼び出してプリンターでレポートを印刷します。 ターゲットが viewerClass の場合、createViewer メソッドが呼び出され、ReportOutputUser オブジェクトが取得されます。 次に、オブジェクトのメソッド (startReport、startPage、startSection、startField、outputStringField など) を呼び出します。 レポートが実行されると、レポートのテキスト コントロールの Text プロパティが印刷ウィンドウに書き込まれます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                            | 説明                                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public boolean pageCreated(int page)                                                              |                                                 |
| public str result()                                                                               |                                                 |
| public void writeAutoLabel(OutputAutoLabelField field, OuputSection section)                      |                                                 |
| public void endHeaderSection(OutputHeaderSection section)                                         |                                                 |
| public void writeString(OutputStringField field, OuputSection section)                            |                                                 |
| public void endPageHeaderSection(OutputPageHeaderSection section)                                 |                                                 |
| public void writeBitmap(OutputBitmapField field, OuputSection section)                            |                                                 |
| public void endBodySection(OutputBodySection section)                                             |                                                 |
| public void startPageHeaderSection(OutputPageHeaderSection section)                               |                                                 |
| public void printViaClass()                                                                       |                                                 |
| public void endPageFooterSection(OutputPageFooterSection section)                                 |                                                 |
| public void writeReal(OutputRealField field, OuputSection section)                                |                                                 |
| public void startColumnHeadingsSection(OutputColumnHeadingsSection section)                       |                                                 |
| public void writeShape(OutputShapeField field, OuputSection section)                              |                                                 |
| public void writeDateTime(OutputDateTimeField field, OuputSection section)                        |                                                 |
| public void writeStaticText(OutputStaticTextField field, OuputSection section)                    |                                                 |
| public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\], \[container settings\]) | Object クラスの新しいインスタンスを初期化します。 |
| public void writeInteger(OutputIntegerField field, OuputSection section)                          |                                                 |
| public void startColumnSection()                                                                  |                                                 |
| public void startSection(OuputSection section)                                                    |                                                 |
| public void writeDate(OutputDateField field, OuputSection section)                                |                                                 |
| public void pagesTotal(int pagesTotal)                                                            |                                                 |
| public void writeInt64(OutputInt64Field field, OuputSection section)                              |                                                 |
| public void endReport(PrintJobStatus printJobStatus)                                              |                                                 |
| public void endColumnSection()                                                                    |                                                 |
| public void startReport(PrintJobSettings printJobSettings)                                        |                                                 |
| public void printPageViaClass(int page)                                                           |                                                 |
| public void endEpilogSection(OutputEpilogSection section)                                         |                                                 |
| public void endPrologSection(OutputPrologSection section)                                         |                                                 |
| public void endPage()                                                                             |                                                 |
| public void startFooterSection(OutputFooterSection section)                                       |                                                 |
| public void endProgrammableSection(OutputProgrammableSection section)                             |                                                 |
| public void startBodySection(OutputBodySection section)                                           |                                                 |
| public void endSection(OuputSection section)                                                      |                                                 |
| public void startProgrammableSection(OutputProgrammableSection section)                           |                                                 |
| public void startEpilogSection(OutputEpilogSection section)                                       |                                                 |
| public void startHeaderSection(OutputHeaderSection section)                                       |                                                 |
| public void endColumnHeadingsSection(OutputColumnHeadingsSection section)                         |                                                 |
| public void writeLabel(OutputLabelField field, OuputSection section)                              |                                                 |
| public void endFooterSection(OutputFooterSection section)                                         |                                                 |
| public void writeField(OutputField field, OuputSection section)                                   |                                                 |
| public void writeEnum(OutputEnumField field, OuputSection section)                                |                                                 |
| public void startPageFooterSection(OutputPageFooterSection section)                               |                                                 |
| public void writeSum(OutputSumField field, OuputSection section)                                  |                                                 |
| public void writeTime(OutputTimeField field, OuputSection section)                                |                                                 |
| public void startPage(OutputPage page)                                                            |                                                 |
| public void startPrologSection(OutputPrologSection section)                                       |                                                 |

## <a name="method-pagecreated"></a>メソッド pageCreated

```xpp
public boolean pageCreated(int page)
```

### <a name="parameters---pagecreated"></a>パラメーター - pageCreated

ページ  

### <a name="return-value---pagecreated"></a>戻り値 - pageCreated

## <a name="method-result"></a>メソッド result

```xpp
public str result()
```

### <a name="return-value---result"></a>戻り値 - result

## <a name="method-writeautolabel"></a>メソッド writeAutoLabel

```xpp
public void writeAutoLabel(OutputAutoLabelField field, OuputSection section)
```

### <a name="parameters---writeautolabel"></a>パラメーター - writeAutoLabel

 フィールド  

<!-- -->

セクション  

## <a name="method-endheadersection"></a>メソッド endHeaderSection

```xpp
public void endHeaderSection(OutputHeaderSection section)
```

### <a name="parameters---endheadersection"></a>パラメーター - endHeaderSection

セクション  

## <a name="method-writestring"></a>メソッド writeString

```xpp
public void writeString(OutputStringField field, OuputSection section)
```

### <a name="parameters---writestring"></a>パラメーター - writeString

 フィールド  

<!-- -->

セクション  

## <a name="method-endpageheadersection"></a>メソッド endPageHeaderSection

```xpp
public void endPageHeaderSection(OutputPageHeaderSection section)
```

### <a name="parameters---endpageheadersection"></a>パラメーター - endPageHeaderSection

セクション  

## <a name="method-writebitmap"></a>メソッド writeBitmap

```xpp
public void writeBitmap(OutputBitmapField field, OuputSection section)
```

### <a name="parameters---writebitmap"></a>パラメーター - writeBitmap

 フィールド  

<!-- -->

セクション  

## <a name="method-endbodysection"></a>メソッド endBodySection

```xpp
public void endBodySection(OutputBodySection section)
```

### <a name="parameters---endbodysection"></a>パラメーター - endBodySection

セクション  

## <a name="method-startpageheadersection"></a>メソッド startPageHeaderSection

```xpp
public void startPageHeaderSection(OutputPageHeaderSection section)
```

### <a name="parameters---startpageheadersection"></a>パラメーター - startPageHeaderSection

セクション  

## <a name="method-printviaclass"></a>メソッド printViaClass

```xpp
public void printViaClass()
```

## <a name="method-endpagefootersection"></a>メソッド endPageFooterSection

```xpp
public void endPageFooterSection(OutputPageFooterSection section)
```

### <a name="parameters---endpagefootersection"></a>パラメーター - endPageFooterSection

セクション  

## <a name="method-writereal"></a>メソッド writeReal

```xpp
public void writeReal(OutputRealField field, OuputSection section)
```

### <a name="parameters---writereal"></a>パラメーター - writeReal

 フィールド  

<!-- -->

セクション  

## <a name="method-startcolumnheadingssection"></a>メソッド startColumnHeadingsSection

```xpp
public void startColumnHeadingsSection(OutputColumnHeadingsSection section)
```

### <a name="parameters---startcolumnheadingssection"></a>パラメーター - startColumnHeadingsSection

セクション  

## <a name="method-writeshape"></a>メソッド writeShape

```xpp
public void writeShape(OutputShapeField field, OuputSection section)
```

### <a name="parameters---writeshape"></a>パラメーター - writeShape

 フィールド  

<!-- -->

セクション  

## <a name="method-writedatetime"></a>メソッド writeDateTime

```xpp
public void writeDateTime(OutputDateTimeField field, OuputSection section)
```

### <a name="parameters---writedatetime"></a>パラメーター - writeDateTime

 フィールド  

<!-- -->

セクション  

## <a name="method-writestatictext"></a>メソッド writeStaticText

```xpp
public void writeStaticText(OutputStaticTextField field, OuputSection section)
```

### <a name="parameters---writestatictext"></a>パラメーター - writeStaticText

 フィールド  

<!-- -->

セクション  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(PrintJobHeader jobsCursor, [PrintJobPages pagesCursor], [container settings])
```

### <a name="parameters---new"></a>パラメーター - new

jobsCursor  

<!-- -->

pagesCursor  

<!-- -->

設定  

## <a name="method-writeinteger"></a>メソッド writeInteger

```xpp
public void writeInteger(OutputIntegerField field, OuputSection section)
```

### <a name="parameters---writeinteger"></a>パラメーター - writeInteger

 フィールド  

<!-- -->

セクション  

## <a name="method-startcolumnsection"></a>メソッド startColumnSection

```xpp
public void startColumnSection()
```

## <a name="method-startsection"></a>メソッド startSection

```xpp
public void startSection(OuputSection section)
```

### <a name="parameters---startsection"></a>パラメーター - startSection

セクション  

## <a name="method-writedate"></a>メソッド writeDate

```xpp
public void writeDate(OutputDateField field, OuputSection section)
```

### <a name="parameters---writedate"></a>パラメーター - writeDate

 フィールド  

<!-- -->

セクション  

## <a name="method-pagestotal"></a>メソッド pagesTotal

```xpp
public void pagesTotal(int pagesTotal)
```

### <a name="parameters---pagestotal"></a>パラメーター - pagesTotal

pagesTotal  

## <a name="method-writeint64"></a>メソッド writeInt64

```xpp
public void writeInt64(OutputInt64Field field, OuputSection section)
```

### <a name="parameters---writeint64"></a>パラメーター - writeInt64

 フィールド  

<!-- -->

セクション  

## <a name="method-endreport"></a>メソッド endReport

```xpp
public void endReport(PrintJobStatus printJobStatus)
```

### <a name="parameters---endreport"></a>パラメーター - endReport

printJobStatus  

## <a name="method-endcolumnsection"></a>メソッド endColumnSection

```xpp
public void endColumnSection()
```

## <a name="method-startreport"></a>メソッド startReport

```xpp
public void startReport(PrintJobSettings printJobSettings)
```

### <a name="parameters---startreport"></a>パラメーター - startReport

printJobSettings  

## <a name="method-printpageviaclass"></a>メソッド printPageViaClass

```xpp
public void printPageViaClass(int page)
```

### <a name="parameters---printpageviaclass"></a>パラメーター - printPageViaClass

ページ  

## <a name="method-endepilogsection"></a>メソッド endEpilogSection

```xpp
public void endEpilogSection(OutputEpilogSection section)
```

### <a name="parameters---endepilogsection"></a>パラメーター - endEpilogSection

セクション  

## <a name="method-endprologsection"></a>メソッド endPrologSection

```xpp
public void endPrologSection(OutputPrologSection section)
```

### <a name="parameters---endprologsection"></a>パラメーター - endPrologSection

セクション  

## <a name="method-endpage"></a>メソッド endPage

```xpp
public void endPage()
```

## <a name="method-startfootersection"></a>メソッド startFooterSection

```xpp
public void startFooterSection(OutputFooterSection section)
```

### <a name="parameters---startfootersection"></a>パラメーター - startFooterSection

セクション  

## <a name="method-endprogrammablesection"></a>メソッド endProgrammableSection

```xpp
public void endProgrammableSection(OutputProgrammableSection section)
```

### <a name="parameters---endprogrammablesection"></a>パラメーター - endProgrammableSection

セクション  

## <a name="method-startbodysection"></a>メソッド startBodySection

```xpp
public void startBodySection(OutputBodySection section)
```

### <a name="parameters---startbodysection"></a>パラメーター - startBodySection

セクション  

## <a name="method-endsection"></a>メソッド endSection

```xpp
public void endSection(OuputSection section)
```

### <a name="parameters---endsection"></a>パラメーター - endSection

セクション  

## <a name="method-startprogrammablesection"></a>メソッド startProgrammableSection

```xpp
public void startProgrammableSection(OutputProgrammableSection section)
```

### <a name="parameters---startprogrammablesection"></a>パラメーター - startProgrammableSection

セクション  

## <a name="method-startepilogsection"></a>メソッド startEpilogSection

```xpp
public void startEpilogSection(OutputEpilogSection section)
```

### <a name="parameters---startepilogsection"></a>パラメーター - startEpilogSection

セクション  

## <a name="method-startheadersection"></a>メソッド startHeaderSection

```xpp
public void startHeaderSection(OutputHeaderSection section)
```

### <a name="parameters---startheadersection"></a>パラメーター - startHeaderSection

セクション  

## <a name="method-endcolumnheadingssection"></a>メソッド endColumnHeadingsSection

```xpp
public void endColumnHeadingsSection(OutputColumnHeadingsSection section)
```

### <a name="parameters---endcolumnheadingssection"></a>パラメーター - endColumnHeadingsSection

セクション  

## <a name="method-writelabel"></a>メソッド writeLabel

```xpp
public void writeLabel(OutputLabelField field, OuputSection section)
```

### <a name="parameters---writelabel"></a>パラメーター - writeLabel

 フィールド  

<!-- -->

セクション  

## <a name="method-endfootersection"></a>メソッド endFooterSection

```xpp
public void endFooterSection(OutputFooterSection section)
```

### <a name="parameters---endfootersection"></a>パラメーター - endFooterSection

セクション  

## <a name="method-writefield"></a>メソッド writeField

```xpp
public void writeField(OutputField field, OuputSection section)
```

### <a name="parameters---writefield"></a>パラメーター - writeField

 フィールド  

<!-- -->

セクション  

## <a name="method-writeenum"></a>メソッド writeEnum

```xpp
public void writeEnum(OutputEnumField field, OuputSection section)
```

### <a name="parameters---writeenum"></a>パラメーター - writeEnum

 フィールド  

<!-- -->

セクション  

## <a name="method-startpagefootersection"></a>メソッド startPageFooterSection

```xpp
public void startPageFooterSection(OutputPageFooterSection section)
```

### <a name="parameters---startpagefootersection"></a>パラメーター - startPageFooterSection

セクション  

## <a name="method-writesum"></a>メソッド writeSum

```xpp
public void writeSum(OutputSumField field, OuputSection section)
```

### <a name="parameters---writesum"></a>パラメーター - writeSum

 フィールド  

<!-- -->

セクション  

## <a name="method-writetime"></a>メソッド writeTime

```xpp
public void writeTime(OutputTimeField field, OuputSection section)
```

### <a name="parameters---writetime"></a>パラメーター - writeTime

 フィールド  

<!-- -->

セクション  

## <a name="method-startpage"></a>メソッド startPage

```xpp
public void startPage(OutputPage page)
```

### <a name="parameters---startpage"></a>パラメーター - startPage

ページ  

## <a name="method-startprologsection"></a>メソッド startPrologSection

```xpp
public void startPrologSection(OutputPrologSection section)
```

### <a name="parameters---startprologsection"></a>パラメーター - startPrologSection

セクション  

