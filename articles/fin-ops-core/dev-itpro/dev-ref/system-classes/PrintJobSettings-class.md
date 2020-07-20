---
title: PrintJobSettings クラス
description: このトピックでは、PrintJobSettings クラスについて説明します。
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
ms.openlocfilehash: efe8608501b4df724e55c7565022d9dec8298c94
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502875"
---
# <a name="class-printjobsettings"></a>クラス PrintJobSettings

[!include [banner](../../includes/banner.md)]

```xpp
class PrintJobSettings extends Object
```

PrintJobSettings クラスを使用すると、ユーザーがプリンターおよびそのデバイス設定にアクセスできます。

## <a name="remarks"></a>備考

PrintJobSettings は、SysPrintForm フォームにより使用されます。

## <a name="examples"></a>例

次の例では、既定のプリンターの名前を書き込み、使用可能なプリンターを一覧表示します。

```xpp
void printerInfo() 
{    
    printJobSettings pjs; 
    int i; 
    pjs = new PrintJobSettings(); 
    print "The default printer is ", pjs.DeviceName(); 
    print "There are ", pjs.GetNumberOfPrinters(), " printers"; 
    i = 1; 
    while (i<=pjs.GetNumberOfPrinters())  
    { 
        print "Printer No. ", i, " is ", pjs.GetPrinter(i);  
        i++; 
    } 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                  | 説明                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| public boolean allPages(\[boolean all\])                                                                | sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。 |
| public boolean appendToTextFile(\[boolean append\])                                                     |                                                                                                   |
| public boolean banding()                                                                                |                                                                                                   |
| public PrintJobSettings clientPrintJobSettings()                                                        |                                                                                                   |
| public boolean collate(\[boolean collate\])                                                             |                                                                                                   |
| public int copies(\[int numberOfCopies\])                                                               |                                                                                                   |
| public str copyDescription(int number, \[str description\])                                             |                                                                                                   |
| public str deviceName(\[str device\], \[ClassRunMode runOn\])                                           | プリンターを選択するか、選択されているプリンター デバイス名を取得します。                            |
| public boolean doNotOverwrite(\[boolean warn\])                                                         |                                                                                                   |
| public boolean enableCopies(\[boolean enable\])                                                         |                                                                                                   |
| public boolean enableDevice(\[boolean enable\])                                                         |                                                                                                   |
| public boolean enablePages(\[boolean enable\])                                                          |                                                                                                   |
| public boolean enableProperties(\[boolean enable\])                                                     |                                                                                                   |
| public boolean enableStoreInPrintArchive(\[boolean enable\])                                            |                                                                                                   |
| public boolean enableTarget(\[boolean enable\])                                                         |                                                                                                   |
| public int facename2number(\[str facename\])                                                            |                                                                                                   |
| public str fileName(\[str FileName\])                                                                   |                                                                                                   |
| public boolean fitToPage(\[boolean fit\])                                                               |                                                                                                   |
| public PrintFormat format(\[PrintFormat format\])                                                       |                                                                                                   |
| public int from(\[int fromPage\])                                                                       |                                                                                                   |
| public str getFacename(int number)                                                                      |                                                                                                   |
| public str getFacenameInfo(int number)                                                                  |                                                                                                   |
| public Struct getFontInfo(str fontName)                                                                 |                                                                                                   |
| public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)                             |                                                                                                   |
| public int getNumberOfClientPrinters()                                                                  |                                                                                                   |
| public int getNumberOfFacenames()                                                                       |                                                                                                   |
| public int getNumberOfPrinters()                                                                        | コンピューターに設定されているプリンターの数を返します。                                   |
| public int getNumberOfServerPrinters()                                                                  |                                                                                                   |
| public int getNumberOfTrays()                                                                           |                                                                                                   |
| public str getPrinter(int number)                                                                       | プリンターの deviceName を取得します。                                                                 |
| public ClassRunMode getRunOn(int number)                                                                |                                                                                                   |
| public PrintMedium getTarget()                                                                          |                                                                                                   |
| public int getTray(int number)                                                                          |                                                                                                   |
| public str getTrayName(int number)                                                                      |                                                                                                   |
| public Int64 hDC()                                                                                      |                                                                                                   |
| public boolean lockDestinationProperties(\[boolean warn\])                                              |                                                                                                   |
| public str mailCc(\[str MailCc\])                                                                       |                                                                                                   |
| public str mailSubject(\[str MailSubject\])                                                             |                                                                                                   |
| public str mailTo(\[str MailTo\])                                                                       |                                                                                                   |
| public int numberOfCopyDescriptions(int number)                                                         |                                                                                                   |
| public boolean outputToClient(\[boolean toClient\])                                                     |                                                                                                   |
| public boolean outputToPrnFile(\[boolean writePrnFile\])                                                |                                                                                                   |
| public container packNamesAndPrinterData()                                                              |                                                                                                   |
| public container packPageSettings()                                                                     | ページの書式設定時に選択されているデータをコンテナーに格納します。                           |
| public container packPrinterSettings()                                                                  |                                                                                                   |
| public container packPrintJobSettings()                                                                 |                                                                                                   |
| public container packSubtotalSettings()                                                                 |                                                                                                   |
| public int pageCopy2Tray(int pageNumber, \[int copyNumber\])                                            |                                                                                                   |
| public boolean pageFormatting()                                                                         |                                                                                                   |
| public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])                          |                                                                                                   |
| public int paperTray(\[int tray\])                                                                      |                                                                                                   |
| public int paperTrayRaw(\[int tray\])                                                                   |                                                                                                   |
| public int performanceTest(\[int loops\])                                                               |                                                                                                   |
| public PrintFormat preferredFileFormat(\[PrintFormat format\])                                          |                                                                                                   |
| public PrintFormat preferredMailFormat(\[PrintFormat format\])                                          |                                                                                                   |
| public PrinterOrientation preferredOrientation(\[PrinterOrientation orientation\])                      |                                                                                                   |
| public PrintMedium preferredTarget(\[PrintMedium target\])                                              |                                                                                                   |
| public int printerAttributes()                                                                          |                                                                                                   |
| public int printerAveragePPM()                                                                          |                                                                                                   |
| public str printerComment()                                                                             |                                                                                                   |
| public str printerDatatype()                                                                            |                                                                                                   |
| public int printerDefaultPriority()                                                                     |                                                                                                   |
| public str printerDriverName()                                                                          |                                                                                                   |
| public str printerLocation()                                                                            |                                                                                                   |
| public int printerPageHeight()                                                                          |                                                                                                   |
| public int printerPageWidth()                                                                           |                                                                                                   |
| public int printerPaper()                                                                               |                                                                                                   |
| public str printerParameters()                                                                          |                                                                                                   |
| public str printerPortName()                                                                            |                                                                                                   |
| public str printerPrinterName()                                                                         |                                                                                                   |
| public str printerPrintProcessor()                                                                      |                                                                                                   |
| public int printerPriority()                                                                            |                                                                                                   |
| public int printerQueuedJobs()                                                                          |                                                                                                   |
| public ClassRunMode printerRunOn()                                                                      |                                                                                                   |
| public str printerSepFile()                                                                             |                                                                                                   |
| public str printerServerName()                                                                          |                                                                                                   |
| public boolean printerSettings(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\]) |                                                                                                   |
| public str printerShareName()                                                                           |                                                                                                   |
| public TimeOfDay printerStartTime()                                                                     |                                                                                                   |
| public int printerStatus()                                                                              |                                                                                                   |
| public TimeOfDay printerUntilTime()                                                                     |                                                                                                   |
| public ReportRun reportRun()                                                                            |                                                                                                   |
| public str requestedDeviceName()                                                                        |                                                                                                   |
| public ClassRunMode requestedRunOn()                                                                    |                                                                                                   |
| public boolean runClient()                                                                              |                                                                                                   |
| public boolean runServer()                                                                              |                                                                                                   |
| public int sectionsPerPage(\[int sectionsPerPage\])                                                     |                                                                                                   |
| public PrintMedium setTarget(PrintMedium target)                                                        | 印刷メディアを設定します。                                                                            |
| public boolean singleLargePage(\[boolean singleLargePage\])                                             |                                                                                                   |
| public boolean skipBitmapsInRTF(\[boolean skipBitmaps\])                                                | .rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。                   |
| public boolean storeInPrintArchive(\[boolean store\])                                                   |                                                                                                   |
| public boolean suppressScalingMessage(\[boolean suppress\])                                             |                                                                                                   |
| public int to(\[int toPage\])                                                                           |                                                                                                   |
| public str toString()                                                                                   | 現在のオブジェクトを表す文字列を返します。                                              |
| public boolean unpackPageSettings(container settings)                                                   | 用紙サイズと向きなど、ページ設定を設定します。                                       |
| public boolean unpackPrinterSettings(container settings)                                                |                                                                                                   |
| public boolean unpackPrintJobSettings(container settings)                                               |                                                                                                   |
| public boolean unpackSubtotalSettings(container settings)                                               |                                                                                                   |
| public int unprintableBottom()                                                                          |                                                                                                   |
| public int unprintableLeft()                                                                            |                                                                                                   |
| public int unprintableRight()                                                                           |                                                                                                   |
| public int unprintableTop()                                                                             | 用紙の最上部から用紙の印刷可能な範囲までの距離を示します。              |
| public ReportOutputUserType viewerType(\[ReportOutputUserType type\])                                   |                                                                                                   |
| public int virtualPageHeight(\[int height\])                                                            |                                                                                                   |
| public boolean warnIfFileExists(\[boolean warn\])                                                       |                                                                                                   |
| public void enableBody(\[TableId tableId\])                                                             |                                                                                                   |
| public void new(\[container Settings\], \[boolean infoOnly\])                                           | Object クラスの新しいインスタンスを初期化します。                                                   |
| public void addTrayPageCopy(int tray, int pageNumber, \[int copyNumber\])                               |                                                                                                   |
| public void disableBody(\[TableId tableId\])                                                            |                                                                                                   |
| public void clearTrayPageCopy()                                                                         |                                                                                                   |
| public void rulerInch()                                                                                 |                                                                                                   |
| public void finalize()                                                                                  |                                                                                                   |
| public void rulerOff()                                                                                  |                                                                                                   |
| public void rulerMetric()                                                                               |                                                                                                   |

## <a name="method-allpages"></a>メソッド allPages

sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。

```xpp
public boolean allPages([boolean all])
```

### <a name="parameters---allpages"></a>パラメーター - allPages

すべて  
true の場合、すべてのオプション ボタンが選択されるブール値; それ以外の場合は、ページ オプション ボタンが選択されます。

### <a name="return-value---allpages"></a>戻り値 - allPages

すべてのオプション ボタンを選択する必要がある場合は true。それ以外の場合は false で、ページのオプション ボタンが選択されます。

### <a name="remarks---allpages"></a>備考 - allPages

このメソッドは、sysPrintForm によって内部的に使用されます。

### <a name="examples---allpages"></a>例 - allPages

次の例では、2 〜 4 のページを印刷し、[すべてのオプション] ボタンではなく [ページのオプション] ボタンを選択します。

```xpp
static void PrintingToPDF(Args _args) 
{ 
    Args                args; 
    ReportRun           rr; 
    str reportName = 'Cust'; 
    int i; 
    int numReports = 10; 
    args = new Args(reportName); 
    rr = new ReportRun(args,''); 
    rr.setTarget(Printmedium::File); 
    rr.printJobSettings().format(PrintFormat::RTF); 
    rr.printJobSettings().fileName("C:\\tmp\\Cust_ReportRange2.rtf"); 
    // Select the Pages option button rather than the All option button. 
    rr.printJobSettings().allPages(false); 
    rr.printJobSettings().from(2); 
    rr.printJobSettings().to(4); 
    rr.query().interactive(false); 
    rr.report().interactive(false); 
    rr.run(); 
}
```

## <a name="method-appendtotextfile"></a>メソッド appendToTextFile

```xpp
public boolean appendToTextFile([boolean append])
```

### <a name="parameters---appendtotextfile"></a>パラメーター - appendToTextFile

append  

### <a name="return-value---appendtotextfile"></a>戻り値 - appendToTextFile

## <a name="method-banding"></a>メソッド banding

```xpp
public boolean banding()
```

### <a name="return-value---banding"></a>戻り値 - banding

## <a name="method-clientprintjobsettings"></a>メソッド clientPrintJobSettings

```xpp
public PrintJobSettings clientPrintJobSettings()
```

### <a name="return-value---clientprintjobsettings"></a>戻り値 - clientPrintJobSettings

## <a name="method-collate"></a>メソッド collate

```xpp
public boolean collate([boolean collate])
```

### <a name="parameters---collate"></a>パラメーター - collate

collate  

### <a name="return-value---collate"></a>戻り値 - collate

## <a name="method-copies"></a>メソッド copies

```xpp
public int copies([int numberOfCopies])
```

### <a name="parameters---copies"></a>パラメーター - copies

numberOfCopies  

### <a name="return-value---copies"></a>戻り値 - copies

## <a name="method-copydescription"></a>メソッド copyDescription

```xpp
public str copyDescription(int number, [str description])
```

### <a name="parameters---copydescription"></a>パラメーター - copyDescription

番号  

<!-- -->

説明  

### <a name="return-value---copydescription"></a>戻り値 - copyDescription

## <a name="method-devicename"></a>メソッド deviceName

プリンターを選択するか、選択されているプリンター デバイス名を取得します。

```xpp
public str deviceName([str device], [ClassRunMode runOn])
```

### <a name="parameters---devicename"></a>パラメーター - deviceName

デバイス  

<!-- -->

runOn  

### <a name="return-value---devicename"></a>戻り値 - deviceName

選択したプリンターの deviceName。

### <a name="remarks---devicename"></a>備考 - deviceName

選択されるプリンターの deviceName は、getPrinter メソッドを使用して検出できます。

### <a name="examples---devicename"></a>例 - deviceName

このジョブは、利用可能なプリンターと印刷できない領域を一覧表示します。

```xpp
static void aaaKJ(args a) 
{ 
    printJobSettings pjs; 
    str printer; 
    int i; 
    pjs = new printJobSettings(); 
    for (i=1; i<=pjs.GetNumberOfPrinters(); i++) 
    { 
        printer = pjs.GetPrinter(i); 
        pjs.DeviceName(printer); 
        print "printer No. ",i, " has name ",  printer; 
        print "   left:  ", pjs.UnprintableLeft(),   "/100 mm"; 
        print "   right: ", pjs.UnprintableRight(),  "/100 mm"; 
        print "   top:   ", pjs.UnprintableTop(),    "/100 mm"; 
        print "   bottom:", pjs.UnprintableBottom(), "/100 mm"; 
    } 
    pause; 
}
```

## <a name="method-donotoverwrite"></a>メソッド doNotOverwrite

```xpp
public boolean doNotOverwrite([boolean warn])
```

### <a name="parameters---donotoverwrite"></a>パラメーター - doNotOverwrite

警告  

### <a name="return-value---donotoverwrite"></a>戻り値 - doNotOverwrite

## <a name="method-enablecopies"></a>メソッド enableCopies

```xpp
public boolean enableCopies([boolean enable])
```

### <a name="parameters---enablecopies"></a>パラメーター - enableCopies

enable  

### <a name="return-value---enablecopies"></a>戻り値 - enableCopies

## <a name="method-enabledevice"></a>メソッド enableDevice

```xpp
public boolean enableDevice([boolean enable])
```

### <a name="parameters---enabledevice"></a>パラメーター - enableDevice

enable  

### <a name="return-value---enabledevice"></a>戻り値 - enableDevice

## <a name="method-enablepages"></a>メソッド enablePages

```xpp
public boolean enablePages([boolean enable])
```

### <a name="parameters---enablepages"></a>パラメーター - enablePages

enable  

### <a name="return-value---enablepages"></a>戻り値 - enablePages

## <a name="method-enableproperties"></a>メソッド enableProperties

```xpp
public boolean enableProperties([boolean enable])
```

### <a name="parameters---enableproperties"></a>パラメーター - enableProperties

enable  

### <a name="return-value---enableproperties"></a>戻り値 - enableProperties

## <a name="method-enablestoreinprintarchive"></a>メソッド enableStoreInPrintArchive

```xpp
public boolean enableStoreInPrintArchive([boolean enable])
```

### <a name="parameters---enablestoreinprintarchive"></a>パラメーター - enableStoreInPrintArchive

enable  

### <a name="return-value---enablestoreinprintarchive"></a>戻り値 - enableStoreInPrintArchive

## <a name="method-enabletarget"></a>メソッド enableTarget

```xpp
public boolean enableTarget([boolean enable])
```

### <a name="parameters---enabletarget"></a>パラメーター - enableTarget

enable  

### <a name="return-value---enabletarget"></a>戻り値 - enableTarget

## <a name="method-facename2number"></a>メソッド facename2number

```xpp
public int facename2number([str facename])
```

### <a name="parameters---facename2number"></a>パラメーター - facename2number

facename  

### <a name="return-value---facename2number"></a>戻り値 - facename2number

## <a name="method-filename"></a>メソッド fileName

```xpp
public str fileName([str FileName])
```

### <a name="parameters---filename"></a>パラメーター - fileName

FileName  

### <a name="return-value---filename"></a>戻り値 - fileName

## <a name="method-fittopage"></a>メソッド fitToPage

```xpp
public boolean fitToPage([boolean fit])
```

### <a name="parameters---fittopage"></a>パラメーター - fitToPage

fit  

### <a name="return-value---fittopage"></a>戻り値 - fitToPage

## <a name="method-format"></a>メソッド format

```xpp
public PrintFormat format([PrintFormat format])
```

### <a name="parameters---format"></a>パラメーター - format

形式  

### <a name="return-value---format"></a>戻り値 - format

## <a name="method-from"></a>メソッド from

```xpp
public int from([int fromPage])
```

### <a name="parameters---from"></a>パラメーター - from

fromPage  

### <a name="return-value---from"></a>戻り値 - from

## <a name="method-getfacename"></a>メソッド getFacename

```xpp
public str getFacename(int number)
```

### <a name="parameters---getfacename"></a>パラメーター - getFacename

番号  

### <a name="return-value---getfacename"></a>戻り値 - getFacename

## <a name="method-getfacenameinfo"></a>メソッド getFacenameInfo

```xpp
public str getFacenameInfo(int number)
```

### <a name="parameters---getfacenameinfo"></a>パラメーター - getFacenameInfo

番号  

### <a name="return-value---getfacenameinfo"></a>戻り値 - getFacenameInfo

## <a name="method-getfontinfo"></a>メソッド getFontInfo

```xpp
public Struct getFontInfo(str fontName)
```

### <a name="parameters---getfontinfo"></a>パラメーター - getFontInfo

fontName  

### <a name="return-value---getfontinfo"></a>戻り値 - getFontInfo

## <a name="method-getglyphwidthsarray"></a>メソッド getGlyphWidthsArray

```xpp
public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)
```

### <a name="parameters---getglyphwidthsarray"></a>パラメーター - getGlyphWidthsArray

fontName  

<!-- -->

firstChar  

<!-- -->

lastChar  

### <a name="return-value---getglyphwidthsarray"></a>戻り値 - getGlyphWidthsArray

## <a name="method-getnumberofclientprinters"></a>メソッド getNumberOfClientPrinters

```xpp
public int getNumberOfClientPrinters()
```

### <a name="return-value---getnumberofclientprinters"></a>戻り値 - getNumberOfClientPrinters

## <a name="method-getnumberoffacenames"></a>メソッド getNumberOfFacenames

```xpp
public int getNumberOfFacenames()
```

### <a name="return-value---getnumberoffacenames"></a>戻り値 - getNumberOfFacenames

## <a name="method-getnumberofprinters"></a>メソッド getNumberOfPrinters

コンピューターに設定されているプリンターの数を返します。

```xpp
public int getNumberOfPrinters()
```

### <a name="return-value---getnumberofprinters"></a>戻り値 - getNumberOfPrinters

コンピューターに設定されているプリンターの数。

## <a name="method-getnumberofserverprinters"></a>メソッド getNumberOfServerPrinters

```xpp
public int getNumberOfServerPrinters()
```

### <a name="return-value---getnumberofserverprinters"></a>戻り値 - getNumberOfServerPrinters

## <a name="method-getnumberoftrays"></a>メソッド getNumberOfTrays

```xpp
public int getNumberOfTrays()
```

### <a name="return-value---getnumberoftrays"></a>返り値 - getNumberOfTrays

## <a name="method-getprinter"></a>メソッド getPrinter

プリンターの deviceName を取得します。

```xpp
public str getPrinter(int number)
```

### <a name="parameters---getprinter"></a>パラメーター - getPrinter

番号  
1 から使用可能なプリンターの数までの値。

### <a name="return-value---getprinter"></a>戻り値 - getPrinter

指定されたプリンター番号の deviceName。

### <a name="examples---getprinter"></a>例 - getPrinter

```xpp
printJobSettings pjs; 
int i; 
pjs = new printJobSettings(); 
i = 1; 
while (i<=pjs.GetNumberOfPrinters()) 
{ 
    print "Printer No. ", i, " is ", pjs.GetPrinter(i); 
    i++; 
}
```

## <a name="method-getrunon"></a>メソッド getRunOn

```xpp
public ClassRunMode getRunOn(int number)
```

### <a name="parameters---getrunon"></a>パラメーター - getRunOn

番号  

### <a name="return-value---getrunon"></a>戻り値 - getRunOn

## <a name="method-gettarget"></a>メソッド getTarget

```xpp
public PrintMedium getTarget()
```

### <a name="return-value---gettarget"></a>戻り値 - getTarget

## <a name="method-gettray"></a>メソッド getTray

```xpp
public int getTray(int number)
```

### <a name="parameters---gettray"></a>パラメーター - getTray

番号  

### <a name="return-value---gettray"></a>戻り値 - getTray

## <a name="method-gettrayname"></a>メソッド getTrayName

```xpp
public str getTrayName(int number)
```

### <a name="parameters---gettrayname"></a>パラメーター - getTrayName

番号  

### <a name="return-value---gettrayname"></a>戻り値 - getTrayName

## <a name="method-hdc"></a>メソッド hDC

```xpp
public Int64 hDC()
```

### <a name="return-value---hdc"></a>戻り値 - hDC

## <a name="method-lockdestinationproperties"></a>メソッド lockDestinationProperties

```xpp
public boolean lockDestinationProperties([boolean warn])
```

### <a name="parameters---lockdestinationproperties"></a>パラメーター - lockDestinationProperties

警告  

### <a name="return-value---lockdestinationproperties"></a>戻り値 - lockDestinationProperties

## <a name="method-mailcc"></a>メソッド mailCc

```xpp
public str mailCc([str MailCc])
```

### <a name="parameters---mailcc"></a>パラメーター - mailCc

MailCc  

### <a name="return-value---mailcc"></a>戻り値 - mailCc

## <a name="method-mailsubject"></a>メソッド mailSubject

```xpp
public str mailSubject([str MailSubject])
```

### <a name="parameters---mailsubject"></a>パラメーター - mailSubject

MailSubject  

### <a name="return-value---mailsubject"></a>戻り値 - mailSubject

## <a name="method-mailto"></a>メソッド mailTo

```xpp
public str mailTo([str MailTo])
```

### <a name="parameters---mailto"></a>パラメーター - mailTo

MailTo  

### <a name="return-value---mailto"></a>戻り値 - mailTo

## <a name="method-numberofcopydescriptions"></a>メソッド numberOfCopyDescriptions

```xpp
public int numberOfCopyDescriptions(int number)
```

### <a name="parameters---numberofcopydescriptions"></a>パラメーター - numberOfCopyDescriptions

番号  

### <a name="return-value---numberofcopydescriptions"></a>戻り値 - numberOfCopyDescriptions

## <a name="method-outputtoclient"></a>メソッド outputToClient

```xpp
public boolean outputToClient([boolean toClient])
```

### <a name="parameters---outputtoclient"></a>パラメーター - outputToClient

toClient  

### <a name="return-value---outputtoclient"></a>戻り値 - outputToClient

## <a name="method-outputtoprnfile"></a>メソッド outputToPrnFile

```xpp
public boolean outputToPrnFile([boolean writePrnFile])
```

### <a name="parameters---outputtoprnfile"></a>パラメーター - outputToPrnFile

writePrnFile  

### <a name="return-value---outputtoprnfile"></a>戻り値 - outputToPrnFile

## <a name="method-packnamesandprinterdata"></a>メソッド packNamesAndPrinterData

```xpp
public container packNamesAndPrinterData()
```

### <a name="return-value---packnamesandprinterdata"></a>戻り値 - packNamesAndPrinterData

## <a name="method-packpagesettings"></a>メソッド packPageSettings

ページの書式設定時に選択されているデータをコンテナーに格納します。

```xpp
public container packPageSettings()
```

### <a name="return-value---packpagesettings"></a>戻り値 - packPageSettings

ページの書式設定時に選択されているデータを保持するコンテナーです。

### <a name="remarks---packpagesettings"></a>備考 - packPageSettings

返されたコンテナーは、unpackPageSettings メソッドへの入力として使用できます。

## <a name="method-packprintersettings"></a>メソッド packPrinterSettings

```xpp
public container packPrinterSettings()
```

### <a name="return-value---packprintersettings"></a>戻り値 - packPrinterSettings

## <a name="method-packprintjobsettings"></a>メソッド packPrintJobSettings

```xpp
public container packPrintJobSettings()
```

### <a name="return-value---packprintjobsettings"></a>戻り値 - packPrintJobSettings

## <a name="method-packsubtotalsettings"></a>メソッド packSubtotalSettings

```xpp
public container packSubtotalSettings()
```

### <a name="return-value---packsubtotalsettings"></a>戻り値 - packSubtotalSettings

## <a name="method-pagecopy2tray"></a>メソッド pageCopy2Tray

```xpp
public int pageCopy2Tray(int pageNumber, [int copyNumber])
```

### <a name="parameters---pagecopy2tray"></a>パラメーター - pageCopy2Tray

pageNumber  

<!-- -->

copyNumber  

### <a name="return-value---pagecopy2tray"></a>戻り値 - pageCopy2Tray

## <a name="method-pageformatting"></a>メソッド pageFormatting

```xpp
public boolean pageFormatting()
```

### <a name="return-value---pageformatting"></a>戻り値 - pageFormatting

## <a name="method-paperorientation"></a>メソッド paperOrientation

```xpp
public PrinterOrientation paperOrientation([PrinterOrientation orientation])
```

### <a name="parameters---paperorientation"></a>パラメーター - paperOrientation

orientation  

### <a name="return-value---paperorientation"></a>戻り値 - paperOrientation

## <a name="method-papertray"></a>メソッド paperTray

```xpp
public int paperTray([int tray])
```

### <a name="parameters---papertray"></a>パラメーター - paperTray

トレイ  

### <a name="return-value---papertray"></a>戻り値 - paperTray

## <a name="method-papertrayraw"></a>メソッド paperTrayRaw

```xpp
public int paperTrayRaw([int tray])
```

### <a name="parameters---papertrayraw"></a>パラメーター - paperTrayRaw

トレイ  

### <a name="return-value---papertrayraw"></a>戻り値 - paperTrayRaw

## <a name="method-performancetest"></a>メソッド performanceTest

```xpp
public int performanceTest([int loops])
```

### <a name="parameters---performancetest"></a>パラメーター - performanceTest

loops  

### <a name="return-value---performancetest"></a>戻り値 - performanceTest

## <a name="method-preferredfileformat"></a>メソッド preferredFileFormat

```xpp
public PrintFormat preferredFileFormat([PrintFormat format])
```

### <a name="parameters---preferredfileformat"></a>パラメーター - preferredFileFormat

形式  

### <a name="return-value---preferredfileformat"></a>戻り値 - preferredFileFormat

## <a name="method-preferredmailformat"></a>メソッド preferredMailFormat

```xpp
public PrintFormat preferredMailFormat([PrintFormat format])
```

### <a name="parameters---preferredmailformat"></a>パラメーター - preferredMailFormat

形式  

### <a name="return-value---preferredmailformat"></a>戻り値 - preferredMailFormat

## <a name="method-preferredorientation"></a>メソッド preferredOrientation

```xpp
public PrinterOrientation preferredOrientation([PrinterOrientation orientation])
```

### <a name="parameters---preferredorientation"></a>パラメーター - preferredOrientation

orientation  

### <a name="return-value---preferredorientation"></a>戻り値 - preferredOrientation

## <a name="method-preferredtarget"></a>メソッド preferredTarget

```xpp
public PrintMedium preferredTarget([PrintMedium target])
```

### <a name="parameters---preferredtarget"></a>パラメーター - preferredTarget

target  

### <a name="return-value---preferredtarget"></a>戻り値 - preferredTarget

## <a name="method-printerattributes"></a>メソッド printerAttributes

```xpp
public int printerAttributes()
```

### <a name="return-value---printerattributes"></a>戻り値 - printerAttributes

## <a name="method-printeraverageppm"></a>メソッド printerAveragePPM

```xpp
public int printerAveragePPM()
```

### <a name="return-value---printeraverageppm"></a>戻り値 - printerAveragePPM

## <a name="method-printercomment"></a>メソッド printerComment

```xpp
public str printerComment()
```

### <a name="return-value---printercomment"></a>戻り値 - printerComment

## <a name="method-printerdatatype"></a>メソッド printerDatatype

```xpp
public str printerDatatype()
```

### <a name="return-value---printerdatatype"></a>戻り値 - printerDatatype

## <a name="method-printerdefaultpriority"></a>メソッド printerDefaultPriority

```xpp
public int printerDefaultPriority()
```

### <a name="return-value---printerdefaultpriority"></a>戻り値 - printerDefaultPriority

## <a name="method-printerdrivername"></a>メソッド printerDriverName

```xpp
public str printerDriverName()
```

### <a name="return-value---printerdrivername"></a>戻り値 - printerDriverName

## <a name="method-printerlocation"></a>メソッド printerLocation

```xpp
public str printerLocation()
```

### <a name="return-value---printerlocation"></a>戻り値 - printerLocation

## <a name="method-printerpageheight"></a>メソッド printerPageHeight

```xpp
public int printerPageHeight()
```

### <a name="return-value---printerpageheight"></a>戻り値 - printerPageHeight

## <a name="method-printerpagewidth"></a>メソッド printerPageWidth

```xpp
public int printerPageWidth()
```

### <a name="return-value---printerpagewidth"></a>戻り値 - printerPageWidth

## <a name="method-printerpaper"></a>メソッド printerPaper

```xpp
public int printerPaper()
```

### <a name="return-value---printerpaper"></a>戻り値 - printerPaper

## <a name="method-printerparameters"></a>メソッド printerParameters

```xpp
public str printerParameters()
```

### <a name="return-value---printerparameters"></a>戻り値 - printerParameters

## <a name="method-printerportname"></a>メソッド printerPortName

```xpp
public str printerPortName()
```

### <a name="return-value---printerportname"></a>戻り値 - printerPortName

## <a name="method-printerprintername"></a>メソッド printerPrinterName

```xpp
public str printerPrinterName()
```

### <a name="return-value---printerprintername"></a>戻り値 - printerPrinterName

## <a name="method-printerprintprocessor"></a>メソッド printerPrintProcessor

```xpp
public str printerPrintProcessor()
```

### <a name="return-value---printerprintprocessor"></a>戻り値 - printerPrintProcessor

## <a name="method-printerpriority"></a>メソッド printerPriority

```xpp
public int printerPriority()
```

### <a name="return-value---printerpriority"></a>戻り値 - printerPriority

## <a name="method-printerqueuedjobs"></a>メソッド printerQueuedJobs

```xpp
public int printerQueuedJobs()
```

### <a name="return-value---printerqueuedjobs"></a>戻り値 - printerQueuedJobs

## <a name="method-printerrunon"></a>メソッド printerRunOn

```xpp
public ClassRunMode printerRunOn()
```

### <a name="return-value---printerrunon"></a>戻り値 - printerRunOn

## <a name="method-printersepfile"></a>メソッド printerSepFile

```xpp
public str printerSepFile()
```

### <a name="return-value---printersepfile"></a>戻り値 - printerSepFile

## <a name="method-printerservername"></a>メソッド printerServerName

```xpp
public str printerServerName()
```

### <a name="return-value---printerservername"></a>戻り値 - printerServerName

## <a name="method-printersettings"></a>メソッド printerSettings

```xpp
public boolean printerSettings(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])
```

### <a name="parameters---printersettings"></a>パラメーター - printerSettings

formName  

<!-- -->

args  

<!-- -->

reportRun  

<!-- -->

showWhat  

### <a name="return-value---printersettings"></a>戻り値 - printerSettings

## <a name="method-printersharename"></a>メソッド printerShareName

```xpp
public str printerShareName()
```

### <a name="return-value---printersharename"></a>戻り値 - printerShareName

## <a name="method-printerstarttime"></a>メソッド printerStartTime

```xpp
public TimeOfDay printerStartTime()
```

### <a name="return-value---printerstarttime"></a>戻り値 - printerStartTime

## <a name="method-printerstatus"></a>メソッド printerStatus

```xpp
public int printerStatus()
```

### <a name="return-value---printerstatus"></a>戻り値 - printerStatus

## <a name="method-printeruntiltime"></a>メソッド printerUntilTime

```xpp
public TimeOfDay printerUntilTime()
```

### <a name="return-value---printeruntiltime"></a>戻り値 - printerUntilTime

## <a name="method-reportrun"></a>メソッド reportRun

```xpp
public ReportRun reportRun()
```

### <a name="return-value---reportrun"></a>戻り値 - reportRun

## <a name="method-requesteddevicename"></a>メソッド requestedDeviceName

```xpp
public str requestedDeviceName()
```

### <a name="return-value---requesteddevicename"></a>戻り値 - requestedDeviceName

## <a name="method-requestedrunon"></a>メソッド requestedRunOn

```xpp
public ClassRunMode requestedRunOn()
```

### <a name="return-value---requestedrunon"></a>戻り値 - requestedRunOn

## <a name="method-runclient"></a>メソッド runClient

```xpp
public boolean runClient()
```

### <a name="return-value---runclient"></a>戻り値 - runClient

## <a name="method-runserver"></a>メソッド runServer

```xpp
public boolean runServer()
```

### <a name="return-value---runserver"></a>戻り値 - runServer

## <a name="method-sectionsperpage"></a>メソッド sectionsPerPage

```xpp
public int sectionsPerPage([int sectionsPerPage])
```

### <a name="parameters---sectionsperpage"></a>パラメーター - sectionsPerPage

sectionsPerPage  

### <a name="return-value---sectionsperpage"></a>戻り値 - sectionsPerPage

## <a name="method-settarget"></a>メソッド setTarget

印刷メディアを設定します。

```xpp
public PrintMedium setTarget(PrintMedium target)
```

### <a name="parameters---settarget"></a>パラメーター - setTarget

target  
印刷メディア。

### <a name="return-value---settarget"></a>戻り値 - setTarget

印刷メディア。

## <a name="method-singlelargepage"></a>メソッド singleLargePage

```xpp
public boolean singleLargePage([boolean singleLargePage])
```

### <a name="parameters---singlelargepage"></a>パラメーター - singleLargePage

singleLargePage  

### <a name="return-value---singlelargepage"></a>戻り値 - singleLargePage

## <a name="method-skipbitmapsinrtf"></a>メソッド skipBitmapsInRTF

.rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。

```xpp
public boolean skipBitmapsInRTF([boolean skipBitmaps])
```

### <a name="parameters---skipbitmapsinrtf"></a>パラメーター - skipBitmapsInRTF

skipBitmaps  
ビットマップが含まれるかどうかを判断するブール フラグ; オプション。

### <a name="return-value---skipbitmapsinrtf"></a>戻り値 - skipBitmapsInRTF

ビットマップが含まれる場合は true。それ以外の場合は、false。

## <a name="method-storeinprintarchive"></a>メソッド storeInPrintArchive

```xpp
public boolean storeInPrintArchive([boolean store])
```

### <a name="parameters---storeinprintarchive"></a>パラメーター - storeInPrintArchive

店舗  

### <a name="return-value---storeinprintarchive"></a>戻り値 - storeInPrintArchive

## <a name="method-suppressscalingmessage"></a>メソッド suppressScalingMessage

```xpp
public boolean suppressScalingMessage([boolean suppress])
```

### <a name="parameters---suppressscalingmessage"></a>パラメーター - suppressScalingMessage

suppress  

### <a name="return-value---suppressscalingmessage"></a>戻り値 - suppressScalingMessage

## <a name="method-to"></a>メソッド to

```xpp
public int to([int toPage])
```

### <a name="parameters---to"></a>パラメーター - to

toPage  

### <a name="return-value---to"></a>戻り値 - to

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。

## <a name="method-unpackpagesettings"></a>メソッド unpackPageSettings

用紙サイズと向きなど、ページ設定を設定します。

```xpp
public boolean unpackPageSettings(container settings)
```

### <a name="parameters---unpackpagesettings"></a>パラメーター - unpackPageSettings

設定  
packPageSettings メソッドを呼び出して取得されるコンテナーです。

### <a name="return-value---unpackpagesettings"></a>戻り値 - unpackPageSettings

pageSettings が正常に変更された場合は true。pageSettings が既定値に設定された場合は false。

### <a name="remarks---unpackpagesettings"></a>備考 - unpackPageSettings

reportDesign クラスと report クラスには、同じ名前のメソッドがあります。

## <a name="method-unpackprintersettings"></a>メソッド unpackPrinterSettings

```xpp
public boolean unpackPrinterSettings(container settings)
```

### <a name="parameters---unpackprintersettings"></a>パラメーター - unpackPrinterSettings

設定  

### <a name="return-value---unpackprintersettings"></a>戻り値 - unpackPrinterSettings

## <a name="method-unpackprintjobsettings"></a>メソッド unpackPrintJobSettings

```xpp
public boolean unpackPrintJobSettings(container settings)
```

### <a name="parameters---unpackprintjobsettings"></a>パラメーター - unpackPrintJobSettings

設定  

### <a name="return-value---unpackprintjobsettings"></a>戻り値 - unpackPrintJobSettings

## <a name="method-unpacksubtotalsettings"></a>メソッド unpackSubtotalSettings

```xpp
public boolean unpackSubtotalSettings(container settings)
```

### <a name="parameters---unpacksubtotalsettings"></a>パラメーター - unpackSubtotalSettings

設定  

### <a name="return-value---unpacksubtotalsettings"></a>戻り値 - unpackSubtotalSettings

## <a name="method-unprintablebottom"></a>メソッド unprintableBottom

```xpp
public int unprintableBottom()
```

### <a name="return-value---unprintablebottom"></a>戻り値 - unprintableBottom

## <a name="method-unprintableleft"></a>メソッド unprintableLeft

```xpp
public int unprintableLeft()
```

### <a name="return-value---unprintableleft"></a>戻り値 - unprintableLeft

## <a name="method-unprintableright"></a>メソッド unprintableRight

```xpp
public int unprintableRight()
```

### <a name="return-value---unprintableright"></a>戻り値 - unprintableRight

## <a name="method-unprintabletop"></a>メソッド unprintableTop

用紙の最上部から用紙の印刷可能な範囲までの距離を示します。

```xpp
public int unprintableTop()
```

### <a name="return-value---unprintabletop"></a>戻り値 - unprintableTop

印刷できない領域のサイズ。単位は 100 分の 1 ミリメートルです。

### <a name="remarks---unprintabletop"></a>備考 - unprintableTop

レポートでは、reportDesign の topMargin を unprintableTop よりも小さくしてはなりません。

### <a name="examples---unprintabletop"></a>例 - unprintableTop

```xpp
static void printerInfo(args a) 
{ 
    printJobSettings pjs; 
    str printer; 
    int i; 
    pjs = new printJobSettings(); 
    for (i=1; i<=pjs.GetNumberOfPrinters(); i++) 
    { 
        printer = pjs.GetPrinter(i); 
        pjs.DeviceName(printer); 
        print "printer No. ",i, " has name ",  printer; 
        print "   left:   ", pjs.UnprintableLeft(),   "/100 mm"; 
        print "   right:  ", pjs.UnprintableRight(),  "/100 mm"; 
        print "   totalWidth: ", pjs.UnprintableLeft() +  
            pjs.PrinterPageWidth() + pjs.UnprintableRight(); 
        print "   top:    ", pjs.UnprintableTop(),    "/100 mm"; 
        print "   bottom: ", pjs.UnprintableBottom(), "/100 mm"; 
        print "   totalHeight: ", pjs.UnprintableTop() +  
            pjs.PrinterPageHeight() + pjs.UnprintableBottom(); 
    } 
    pause; 
}
```

## <a name="method-viewertype"></a>メソッド viewerType

```xpp
public ReportOutputUserType viewerType([ReportOutputUserType type])
```

### <a name="parameters---viewertype"></a>パラメーター - viewerType

タイプ  

### <a name="return-value---viewertype"></a>戻り値 - viewerType

## <a name="method-virtualpageheight"></a>メソッド virtualPageHeight

```xpp
public int virtualPageHeight([int height])
```

### <a name="parameters---virtualpageheight"></a>パラメーター - virtualPageHeight

height  

### <a name="return-value---virtualpageheight"></a>戻り値 - virtualPageHeight

## <a name="method-warniffileexists"></a>メソッド warnIfFileExists

```xpp
public boolean warnIfFileExists([boolean warn])
```

### <a name="parameters---warniffileexists"></a>パラメーター - warnIfFileExists

警告  

### <a name="return-value---warniffileexists"></a>戻り値 - warnIfFileExists

## <a name="method-enablebody"></a>メソッド enableBody

```xpp
public void enableBody([TableId tableId])
```

### <a name="parameters---enablebody"></a>パラメーター - enableBody

tableId  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([container Settings], [boolean infoOnly])
```

### <a name="parameters---new"></a>パラメーター - new

設定  

<!-- -->

infoOnly  

## <a name="method-addtraypagecopy"></a>メソッド addTrayPageCopy

```xpp
public void addTrayPageCopy(int tray, int pageNumber, [int copyNumber])
```

### <a name="parameters---addtraypagecopy"></a>パラメーター - addTrayPageCopy

トレイ  

<!-- -->

pageNumber  

<!-- -->

copyNumber  

## <a name="method-disablebody"></a>メソッド disableBody

```xpp
public void disableBody([TableId tableId])
```

### <a name="parameters---disablebody"></a>パラメーター - disableBody

tableId  

## <a name="method-cleartraypagecopy"></a>メソッド clearTrayPageCopy

```xpp
public void clearTrayPageCopy()
```

## <a name="method-rulerinch"></a>メソッド rulerInch

```xpp
public void rulerInch()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-ruleroff"></a>メソッド rulerOff

```xpp
public void rulerOff()
```

## <a name="method-rulermetric"></a>メソッド rulerMetric

```xpp
public void rulerMetric()
```

