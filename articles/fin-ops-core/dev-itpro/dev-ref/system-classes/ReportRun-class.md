---
title: ReportRun クラス
description: このトピックでは、ReportRun クラスについて説明します。
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
ms.openlocfilehash: 4a93df8175b21f4ef7ae677d7ce8c8288aba0954
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502832"
---
# <a name="class-reportrun"></a>クラス ReportRun

[!include [banner](../../includes/banner.md)]

```xpp
class ReportRun extends ObjectRun
```

ReportRun クラスはレポートを生成および印刷するか、画面上のレポートをプレビューします。

## <a name="remarks"></a>備考

レポートの構造を定義するのとは対照的に、ReportRun オブジェクトにはレポートのランタイム特性が含まれます。 ReportRun オブジェクトは、次の引数のいずれかを使用して作成できます。

-   Args オブジェクトは名前およびオプションの designName パラメータが指定しています。
-   例えで使用される、作成されたコンテナーです。
-   レポート名とオプションのデザイン名。

セクション テンプレート ノード タイプを使用すると、セクションを一度定義して、さまざまなレポートで何度も再利用できます。 この一般的な例は、小切手または振替になります。

## <a name="examples"></a>例

次の例では、既存の Cust レポートの Customer デザインを実行します。

```xpp
static void testReportRun(args a) 
{  
    reportRun rr; 
    args aa = new args("Cust"); 
    aa.designName("Customer"); 
    rr = new reportRun(aa); 
    rr.run(); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                    | 説明                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean allPages(\[boolean all\])                                                                                                                  |                                                                                                                                                   |
| public boolean callMenuFunction(xMenuFunction menuFunction)                                                                                               |                                                                                                                                                   |
| public str caption(str reportSpelling, str reportName, str designCaption, str designName)                                                                 | レポートをプレビューするときにキャプションを作成し、レポートを印刷するときにドキュメント名を作成します。                                                            |
| public boolean collate(\[boolean collate\])                                                                                                               |                                                                                                                                                   |
| public TableId columnHeadings(\[TableId tableId\])                                                                                                        | レポートの列見出しのコントロールを提供します。                                                                                                  |
| public ReportControl control()                                                                                                                            | 実行されているコントロールを取得します。                                                                                                     |
| public int copies(\[int numberOfCopies\])                                                                                                                 |                                                                                                                                                   |
| public int copiesTotal()                                                                                                                                  | レポートのマーキング コピーを有効にします。                                                                                                                |
| public int copy()                                                                                                                                         | レポートのコピーの数を返します。                                                                                                       |
| public str copyDescription()                                                                                                                              |                                                                                                                                                   |
| public xFormRun createProgressForm()                                                                                                                      | 進捗情報を含むフォームを作成します。                                                                                              |
| public int currentYmm100()                                                                                                                                |                                                                                                                                                   |
| public ReportDesign design(\[AnyType nameOrReportDesign\])                                                                                                | デザインの名前を取得または設定します。                                                                                                              |
| public str deviceName(\[str device\])                                                                                                                     |                                                                                                                                                   |
| public Object dialog(Object dialog)                                                                                                                       |                                                                                                                                                   |
| public str driverName()                                                                                                                                   | プリンター ドライバー名を返します。                                                                                                                  |
| public boolean enableAllBodies(\[boolean enable\])                                                                                                        |                                                                                                                                                   |
| public boolean execute(int number)                                                                                                                        | レポートのプログラム可能なセクションを印刷します。                                                                                                     |
| public boolean executeBodyColumnHeadings(TableId tableId, \[FieldId fieldId\])                                                                            | レポートの本文セクションの列ヘッダーを印刷します。                                                                                         |
| public boolean executeColumnHeadings(ReportSection section)                                                                                               |                                                                                                                                                   |
| public boolean executeControlColumnHeadings(int number)                                                                                                   | プログラム可能なセクションの列のヘッダーを実行します。                                                                                           |
| public boolean executeFooter(\[TableId tableId\], \[FieldId fieldId\])                                                                                    | フッター セクションを実行を実行します。                                                                                                                         |
| public boolean executeHeader(\[TableId tableId\], \[FieldId fieldId\])                                                                                    | ヘッダー セクションを実行します。                                                                                                                        |
| public boolean executeSection(ReportSection section)                                                                                                      | レポートの指定されたセクションを印刷します。                                                                                                       |
| public boolean fetch()                                                                                                                                    | レポート クエリを実行し、クエリによって検出されたレコードの送信メソッドを呼び出します。                                                    |
| public int from(\[int fromPage\])                                                                                                                         |                                                                                                                                                   |
| public int generateDesign(\[Query query\], \[int designNo\])                                                                                              |                                                                                                                                                   |
| public boolean getDeclineOverwrite()                                                                                                                      |                                                                                                                                                   |
| public int getNumberOfPrinters()                                                                                                                          |                                                                                                                                                   |
| public str getPrinter(int number)                                                                                                                         |                                                                                                                                                   |
| public str getRangeDescription(int number)                                                                                                                |                                                                                                                                                   |
| public ReportViewer getReportViewer()                                                                                                                     |                                                                                                                                                   |
| public PrintMedium getTarget()                                                                                                                            |                                                                                                                                                   |
| public boolean hasGeneratedDesign()                                                                                                                       |                                                                                                                                                   |
| public str headerDescription()                                                                                                                            |                                                                                                                                                   |
| public int heightOfPageFooters()                                                                                                                          |                                                                                                                                                   |
| public int indent()                                                                                                                                       |                                                                                                                                                   |
| public boolean isBodyEnabled(TableId tableId)                                                                                                             |                                                                                                                                                   |
| public Int64 jobId()                                                                                                                                      |                                                                                                                                                   |
| public Common last(TableId tableId)                                                                                                                       |                                                                                                                                                   |
| public int mm100Left()                                                                                                                                    |                                                                                                                                                   |
| public int mm100PageHeight()                                                                                                                              |                                                                                                                                                   |
| public str name(\[str name\])                                                                                                                             | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                         |
| public container pack()                                                                                                                                   | ReportRun クラスの現在のインスタンスをシリアル化します。                                                                                           |
| public container packDesign()                                                                                                                             |                                                                                                                                                   |
| public container packPageSettings()                                                                                                                       |                                                                                                                                                   |
| public container packPrinterSettings()                                                                                                                    |                                                                                                                                                   |
| public container packPrintJobSettings()                                                                                                                   |                                                                                                                                                   |
| public container packSubtotalSettings()                                                                                                                   |                                                                                                                                                   |
| public int page(\[int number\])                                                                                                                           |                                                                                                                                                   |
| public boolean pageFormatting()                                                                                                                           | プリンターのプリンター プロパティを表示します。                                                                                                   |
| public int pagesTotal()                                                                                                                                   |                                                                                                                                                   |
| public str passThrough(str str)                                                                                                                           |                                                                                                                                                   |
| public int pixelsLeft()                                                                                                                                   |                                                                                                                                                   |
| public int print()                                                                                                                                        | 生成されたレポートを、プリンターや画面などの出力メディアに送信します。                                                                    |
| public int printerAttributes()                                                                                                                            |                                                                                                                                                   |
| public int printerAveragePPM()                                                                                                                            |                                                                                                                                                   |
| public str printerComment()                                                                                                                               |                                                                                                                                                   |
| public str printerDatatype()                                                                                                                              |                                                                                                                                                   |
| public int printerDefaultPriority()                                                                                                                       |                                                                                                                                                   |
| public str printerDriverName()                                                                                                                            |                                                                                                                                                   |
| public str printerFontInfo()                                                                                                                              | レポートの印刷に使用されるフォントを示します。                                                                                                 |
| public str printerLocation()                                                                                                                              |                                                                                                                                                   |
| public int printerPageHeight()                                                                                                                            |                                                                                                                                                   |
| public int printerPageWidth()                                                                                                                             |                                                                                                                                                   |
| public int printerPaper()                                                                                                                                 |                                                                                                                                                   |
| public str printerParameters()                                                                                                                            |                                                                                                                                                   |
| public str printerPortName()                                                                                                                              |                                                                                                                                                   |
| public str printerPrinterName()                                                                                                                           |                                                                                                                                                   |
| public str printerPrintProcessor()                                                                                                                        |                                                                                                                                                   |
| public int printerPriority()                                                                                                                              |                                                                                                                                                   |
| public int printerQueuedJobs()                                                                                                                            |                                                                                                                                                   |
| public str printerSepFile()                                                                                                                               |                                                                                                                                                   |
| public str printerServerName()                                                                                                                            |                                                                                                                                                   |
| public boolean printerSettings(\[int showWhat\])                                                                                                          | ユーザーがプリンターの設定を選択できるようにします。                                                                                                      |
| public str printerShareName()                                                                                                                             |                                                                                                                                                   |
| public TimeOfDay printerStartTime()                                                                                                                       |                                                                                                                                                   |
| public int printerStatus()                                                                                                                                |                                                                                                                                                   |
| public TimeOfDay printerUntilTime()                                                                                                                       |                                                                                                                                                   |
| public PrintJobSettings printJobSettings(\[container packedPrintJobSettings\])                                                                            |                                                                                                                                                   |
| public int printSum()                                                                                                                                     |                                                                                                                                                   |
| public xFormRun progressForm(\[xFormRun form\])                                                                                                           |                                                                                                                                                   |
| public str progressInfo(int pageNo, int lineNo)                                                                                                           | セクションが実行されるたびに、レポートが実行中に生成されるレポートの量を記述する文字列を作成します。 |
| public boolean prompt(\[boolean enableCopy\], \[boolean enablePages\], \[boolean enableDevice\], \[boolean enableProperties\], \[boolean enablePrintTo\]) | レポートの実行をユーザーに求めます。                                                                                                                 |
| public Query query(\[Query query\])                                                                                                                       |                                                                                                                                                   |
| public QueryRun queryRun(\[QueryRun queryRun\])                                                                                                           |                                                                                                                                                   |
| public Report report()                                                                                                                                    |                                                                                                                                                   |
| public str reportUser(\[str user\])                                                                                                                       |                                                                                                                                                   |
| public int rulerCM()                                                                                                                                      |                                                                                                                                                   |
| public int rulerINCH()                                                                                                                                    |                                                                                                                                                   |
| public str screenFontInfo()                                                                                                                               |                                                                                                                                                   |
| public ReportSection section()                                                                                                                            |                                                                                                                                                   |
| public int sectionsLeft(ReportSection section)                                                                                                            |                                                                                                                                                   |
| public boolean send(Common cursor, \[int level\], \[boolean triggerOffBody\], \[boolean newPageBeforeBody\])                                              | セクション グループに属する本文セクションをトリガーします。                                                                                        |
| public PrintMedium setTarget(PrintMedium target)                                                                                                          |                                                                                                                                                   |
| public boolean showMenuFunction(xMenuFunction menuFunction)                                                                                               |                                                                                                                                                   |
| public boolean showMenuReference(WebMenu menuReference)                                                                                                   |                                                                                                                                                   |
| public str sortInfo(Common cursor)                                                                                                                        |                                                                                                                                                   |
| public Date startDate()                                                                                                                                   |                                                                                                                                                   |
| public DateTime startDateTime()                                                                                                                           |                                                                                                                                                   |
| public Date startMachineDate()                                                                                                                            |                                                                                                                                                   |
| public TimeOfDay startTime()                                                                                                                              |                                                                                                                                                   |
| public Real sum(TableId tableId, FieldId fieldId, \[int indent\])                                                                                         |                                                                                                                                                   |
| public Real sumControl(str fieldName, \[int indent\])                                                                                                     |                                                                                                                                                   |
| public Real sumControlNeg(str fieldName, \[int indent\])                                                                                                  |                                                                                                                                                   |
| public Real sumControlPos(str fieldName, \[int indent\])                                                                                                  |                                                                                                                                                   |
| public str sumDescription()                                                                                                                               |                                                                                                                                                   |
| public Real sumNeg(TableId tableId, FieldId fieldId, \[int indent\])                                                                                      |                                                                                                                                                   |
| public Real sumPos(TableId tableId, FieldId fieldId, \[int indent\])                                                                                      |                                                                                                                                                   |
| public boolean suppressReportIsEmptyMessage(\[boolean suppress\])                                                                                         |                                                                                                                                                   |
| public str title(\[str title\])                                                                                                                           | 印刷ジョブの説明を取得または設定します。                                                                                                           |
| public int to(\[int toPage\])                                                                                                                             |                                                                                                                                                   |
| public str toString()                                                                                                                                     | クラスのテキストの説明を返します。                                                                                                       |
| public boolean unpackPageSettings(container packedPageSetup)                                                                                              |                                                                                                                                                   |
| public boolean unpackPrinterSettings(container packedPrinterSetup)                                                                                        |                                                                                                                                                   |
| public boolean unpackPrintJobSettings(container packedPrintJobSettings)                                                                                   |                                                                                                                                                   |
| public boolean unpackSubtotalSettings(container packedSubtotalSetup)                                                                                      |                                                                                                                                                   |
| public PrinterOrientation userSelectedOrientation()                                                                                                       |                                                                                                                                                   |
| public void disableBody(\[TableId tableId\])                                                                                                              |                                                                                                                                                   |
| public void attach()                                                                                                                                      |                                                                                                                                                   |
| public void new(AnyType argsOrReportOrContainer, \[str designName\], \[boolean isWebReport\])                                                             | ReportRun クラスのインスタンスを初期化します。                                                                                                   |
| public void disableSection(ReportSection section)                                                                                                         |                                                                                                                                                   |
| public void arrangeLevelGlobal()                                                                                                                          |                                                                                                                                                   |
| public void setEscapeSequence(str str)                                                                                                                    |                                                                                                                                                   |
| public void enableBody(\[TableId tableId\])                                                                                                               |                                                                                                                                                   |
| public void clearAllRangeDescriptions()                                                                                                                   |                                                                                                                                                   |
| public void header(ReportSection headerSection, TableId tableId, FieldId fieldId)                                                                         | ヘッダーを制御します。                                                                                                                              |
| public void unpackDesign(container packedDesign)                                                                                                          |                                                                                                                                                   |
| public void newPage(\[boolean doPageFooter\])                                                                                                             |                                                                                                                                                   |
| public void footer(ReportSection footerSection, TableId tableId, FieldId fieldId)                                                                         | フッターを制御します。                                                                                                                              |
| public void reset(\[boolean delayExceptions\])                                                                                                            | 複数のレポートを作成する ReportRun クラスの単一インスタンスを有効にします。                                                                      |
| public void arrangeLevelNone()                                                                                                                            |                                                                                                                                                   |
| public void run()                                                                                                                                         | レポートを実行します。                                                                                                                                  |
| public void gotoYmm100(\[int mm100\])                                                                                                                     |                                                                                                                                                   |
| public void disableColumnHeadings(\[TableId tableId\])                                                                                                    |                                                                                                                                                   |
| public void enablePageFooter()                                                                                                                            |                                                                                                                                                   |
| public void init()                                                                                                                                        |                                                                                                                                                   |
| public void arrangeLevelControl()                                                                                                                         |                                                                                                                                                   |
| public void disablePageFooter()                                                                                                                           |                                                                                                                                                   |
| public void addPendingSums()                                                                                                                              | レポートの関連するフッターを印刷します。                                                                                                        |
| public void arrangeLevelSection()                                                                                                                         |                                                                                                                                                   |
| public void enableSection(ReportSection section)                                                                                                          |                                                                                                                                                   |
| public void detach()                                                                                                                                      |                                                                                                                                                   |
| public void addRangeDescription(int x, int y, str text, \[str fontName\], \[int fontSize\])                                                               |                                                                                                                                                   |
| public void finalize()                                                                                                                                    |                                                                                                                                                   |

## <a name="method-allpages"></a>メソッド allPages

```xpp
public boolean allPages([boolean all])
```

### <a name="parameters---allpages"></a>パラメーター - allPages

すべて  

### <a name="return-value---allpages"></a>戻り値 - allPages

## <a name="method-callmenufunction"></a>メソッド callMenuFunction

```xpp
public boolean callMenuFunction(xMenuFunction menuFunction)
```

### <a name="parameters---callmenufunction"></a>パラメーター - callMenuFunction

menuFunction  

### <a name="return-value---callmenufunction"></a>戻り値 - callMenuFunction

## <a name="method-caption"></a>メソッド caption

レポートをプレビューするときにキャプションを作成し、レポートを印刷するときにドキュメント名を作成します。

```xpp
public str caption(str reportSpelling, str reportName, str designCaption, str designName)
```

### <a name="parameters---caption"></a>パラメーター - caption

reportSpelling  
デザインの名前。

<!-- -->

reportName  
デザインの名前。

<!-- -->

designCaption  
デザインの名前。

<!-- -->

designName  
デザインの名前。

### <a name="return-value---caption"></a>戻り値 - caption

DesignLabel が空でない場合は、「DesignLabel - ReportSpelling」を含む文字列。 DesignLabel が空の場合は、「ReportName(DesignName) - ReportSpelling」を含む文字列。

### <a name="remarks---caption"></a>備考 - caption

このメソッドで super メソッドを呼び出すと、レポートをプレビューするときにキャプションとして使用され、レポートを印刷するときにドキュメント名として使用される文字列が作成されます。 レポートのプレビュー時に使用されるキャプションが実際の言語になるようレポート デザインのキャプション プロパティを常に入力しておくことをお勧めします。

## <a name="method-collate"></a>メソッド collate

```xpp
public boolean collate([boolean collate])
```

### <a name="parameters---collate"></a>パラメーター - collate

collate  

### <a name="return-value---collate"></a>戻り値 - collate

## <a name="method-columnheadings"></a>メソッド columnHeadings

レポートの列見出しのコントロールを提供します。

```xpp
public TableId columnHeadings([TableId tableId])
```

### <a name="parameters---columnheadings"></a>パラメーター - columnHeadings

tableId  
テーブルのID、オプション。

### <a name="return-value---columnheadings"></a>戻り値 - columnHeadings

columnHeading オブジェクトが最後に印刷された tableId 値。

## <a name="method-control"></a>メソッド control

実行されているコントロールを取得します。

```xpp
public ReportControl control()
```

### <a name="return-value---control"></a>戻り値 - control

実行されているコントロール。

### <a name="remarks---control"></a>備考 - control

このメソッドは、内部使用を目的としています。

## <a name="method-copies"></a>メソッド copies

```xpp
public int copies([int numberOfCopies])
```

### <a name="parameters---copies"></a>パラメーター - copies

numberOfCopies  

### <a name="return-value---copies"></a>戻り値 - copies

## <a name="method-copiestotal"></a>メソッド copiesTotal

レポートのマーキング コピーを有効にします。

```xpp
public int copiesTotal()
```

### <a name="return-value---copiestotal"></a>戻り値 - copiesTotal

ユーザーが sysPrintForm フォームで要求したコピーの数。

### <a name="remarks---copiestotal"></a>備考 - copiesTotal

コントロールは通常、レポートの実行中に評価されます。 このメソッドを使用するコントロールは、レポートを印刷するときに評価されます。

## <a name="method-copy"></a>メソッド copy

レポートのコピーの数を返します。

```xpp
public int copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

コピーの番号。

### <a name="remarks---copy"></a>備考 - copy

ユーザーが dataFunction メソッドを持つレポート コントロールを 3 枚印刷する場合、このメソッドは 1 枚目のコピーに対して 1、2 枚目のコピーに対して 2、最後のコピーに対して 3 を返します。

## <a name="method-copydescription"></a>メソッド copyDescription

```xpp
public str copyDescription()
```

### <a name="return-value---copydescription"></a>戻り値 - copyDescription

## <a name="method-createprogressform"></a>メソッド createProgressForm

進捗情報を含むフォームを作成します。

```xpp
public xFormRun createProgressForm()
```

### <a name="return-value---createprogressform"></a>戻り値 - createProgressForm

進捗情報の表示に使用するフォーム。

### <a name="remarks---createprogressform"></a>備考 - createProgressForm

このメソッドをオーバー ロードすることができます。 このメソッドは、最初のページが作成されるときに呼び出されます。 既定の実装では、SysPrintProgress フォームが開きます。 進捗状況フォームを実装する場合は、カーネル内でこれらのメソッドが呼び出されるため、setNames および setPagePercent メソッドを実装する必要があります。 このフォームは、ページの印刷時ではなくページの作成時に表示されます。

## <a name="method-currentymm100"></a>メソッド currentYmm100

```xpp
public int currentYmm100()
```

### <a name="return-value---currentymm100"></a>戻り値 - currentYmm100

## <a name="method-design"></a>メソッド design

デザインの名前を取得または設定します。

```xpp
public ReportDesign design([AnyType nameOrReportDesign])
```

### <a name="parameters---design"></a>パラメーター - design

nameOrReportDesign  
デザインの名前 (オプション)。

### <a name="return-value---design"></a>戻り値 - design

デザインの名前。

### <a name="remarks---design"></a>備考 - design

このメソッドを使用すると、レポートの実行中にあるデザインから別のデザインに変更できます。

## <a name="method-devicename"></a>メソッド deviceName

```xpp
public str deviceName([str device])
```

### <a name="parameters---devicename"></a>パラメーター - deviceName

デバイス  

### <a name="return-value---devicename"></a>戻り値 - deviceName

## <a name="method-dialog"></a>メソッド dialog

```xpp
public Object dialog(Object dialog)
```

### <a name="parameters---dialog"></a>パラメーター - dialog

ダイアログ  

### <a name="return-value---dialog"></a>戻り値 - dialog

## <a name="method-drivername"></a>メソッド driverName

プリンター ドライバー名を返します。

```xpp
public str driverName()
```

### <a name="return-value---drivername"></a>戻り値 - driverName

プリンター ドライバー名。

### <a name="remarks---drivername"></a>備考 - driverName

メソッドはしばしば文字列「winspool」を返します。 これは、プリンター デバイス コンテキストが作成されるときに使用するプリンター ドライバー名です。 コンピューターにプリンタが設定されていない場合、文字列「画面」が返されます。

## <a name="method-enableallbodies"></a>メソッド enableAllBodies

```xpp
public boolean enableAllBodies([boolean enable])
```

### <a name="parameters---enableallbodies"></a>パラメーター - enableAllBodies

enable  

### <a name="return-value---enableallbodies"></a>戻り値 - enableAllBodies

## <a name="method-execute"></a>メソッド execute

レポートのプログラム可能なセクションを印刷します。

```xpp
public boolean execute(int number)
```

### <a name="parameters---execute"></a>パラメーター - execute

番号  
プログラム可能なセクションの controlNumber 値。

### <a name="return-value---execute"></a>戻り値 - execute

toPage オブジェクトが生成済みである場合は false; それ以外の場合は true。

## <a name="method-executebodycolumnheadings"></a>メソッド executeBodyColumnHeadings

レポートの本文セクションの列ヘッダーを印刷します。

```xpp
public boolean executeBodyColumnHeadings(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---executebodycolumnheadings"></a>パラメーター - executeBodyColumnHeadings

tableId  
セクション グループの DataField プロパティのフィールド ID (オプション)。

<!-- -->

fieldId  
セクション グループの DataField プロパティのフィールド ID (オプション)。

### <a name="return-value---executebodycolumnheadings"></a>戻り値 - executeBodyColumnHeadings

いずれかの列ヘッダーが印刷された場合は true。それ以外の場合は、false。

### <a name="remarks---executebodycolumnheadings"></a>備考 - executeBodyColumnHeadings

このメソッドは、レポートに自動的に印刷されるものより多くの列見出しをレポートに含める必要がある場合に便利です。

## <a name="method-executecolumnheadings"></a>メソッド executeColumnHeadings

```xpp
public boolean executeColumnHeadings(ReportSection section)
```

### <a name="parameters---executecolumnheadings"></a>パラメーター - executeColumnHeadings

セクション  

### <a name="return-value---executecolumnheadings"></a>戻り値 - executeColumnHeadings

## <a name="method-executecontrolcolumnheadings"></a>メソッド executeControlColumnHeadings

プログラム可能なセクションの列のヘッダーを実行します。

```xpp
public boolean executeControlColumnHeadings(int number)
```

### <a name="parameters---executecontrolcolumnheadings"></a>パラメーター - executeControlColumnHeadings

番号  
プログラム可能なセクションの controlNumber 値。

### <a name="return-value---executecontrolcolumnheadings"></a>戻り値 - executeControlColumnHeadings

いずれかのセクションが印刷された場合は true。それ以外の場合は、false。

### <a name="remarks---executecontrolcolumnheadings"></a>備考 - executeControlColumnHeadings

このメソッドは、プログラム可能なセクションに columnHeading オブジェクトを追加する場合に便利です。 プログラマブル セクションが改ページを引き起こす場合、セクションの columnHeadings オブジェクトが繰り返されます。 このような状況では、このメソッドを呼び出す必要はありません。

## <a name="method-executefooter"></a>メソッド executeFooter

フッター セクションを実行を実行します。

```xpp
public boolean executeFooter([TableId tableId], [FieldId fieldId])
```

### <a name="parameters---executefooter"></a>パラメーター - executeFooter

tableId  
フッター セクション グループの dataField プロパティのフィールド ID (オプション)。

<!-- -->

fieldId  
フッター セクション グループの dataField プロパティのフィールド ID (オプション)。

### <a name="return-value---executefooter"></a>戻り値 - executeFooter

何かが印刷された場合は true。それ以外の場合は、false。

## <a name="method-executeheader"></a>メソッド executeHeader

ヘッダー セクションを実行します。

```xpp
public boolean executeHeader([TableId tableId], [FieldId fieldId])
```

### <a name="parameters---executeheader"></a>パラメーター - executeHeader

tableId  
ヘッダー セクション グループの dataField プロパティのフィールド ID (オプション)。

<!-- -->

fieldId  
ヘッダー セクション グループの dataField プロパティのフィールド ID (オプション)。

### <a name="return-value---executeheader"></a>戻り値 - executeHeader

## <a name="method-executesection"></a>メソッド executeSection

レポートの指定されたセクションを印刷します。

```xpp
public boolean executeSection(ReportSection section)
```

### <a name="parameters---executesection"></a>パラメーター - executeSection

セクション  
印刷するセクション。

### <a name="return-value---executesection"></a>戻り値 - executeSection

## <a name="method-fetch"></a>メソッド fetch

レポート クエリを実行し、クエリによって検出されたレコードの送信メソッドを呼び出します。

```xpp
public boolean fetch()
```

### <a name="return-value---fetch"></a>戻り値 - fetch

そのレポートの実行を継続する必要がある場合は true。それ以外の場合は、false。

### <a name="remarks---fetch"></a>備考 - fetch

fetch メソッドは、run メソッドのスーパー コールから呼び出されます。

## <a name="method-from"></a>メソッド from

```xpp
public int from([int fromPage])
```

### <a name="parameters---from"></a>パラメーター - from

fromPage  

### <a name="return-value---from"></a>戻り値 - from

## <a name="method-generatedesign"></a>メソッド generateDesign

```xpp
public int generateDesign([Query query], [int designNo])
```

### <a name="parameters---generatedesign"></a>パラメーター - generateDesign

クエリ  

<!-- -->

designNo  

### <a name="return-value---generatedesign"></a>戻り値 - generateDesign

## <a name="method-getdeclineoverwrite"></a>メソッド getDeclineOverwrite

```xpp
public boolean getDeclineOverwrite()
```

### <a name="return-value---getdeclineoverwrite"></a>戻り値 - getDeclineOverwrite

## <a name="method-getnumberofprinters"></a>メソッド getNumberOfPrinters

```xpp
public int getNumberOfPrinters()
```

### <a name="return-value---getnumberofprinters"></a>戻り値 - getNumberOfPrinters

## <a name="method-getprinter"></a>メソッド getPrinter

```xpp
public str getPrinter(int number)
```

### <a name="parameters---getprinter"></a>パラメーター - getPrinter

番号  

### <a name="return-value---getprinter"></a>戻り値 - getPrinter

## <a name="method-getrangedescription"></a>メソッド getRangeDescription

```xpp
public str getRangeDescription(int number)
```

### <a name="parameters---getrangedescription"></a>パラメーター - getRangeDescription

番号  

### <a name="return-value---getrangedescription"></a>戻り値 - getRangeDescription

## <a name="method-getreportviewer"></a>メソッド getReportViewer

```xpp
public ReportViewer getReportViewer()
```

### <a name="return-value---getreportviewer"></a>戻り値 - getReportViewer

## <a name="method-gettarget"></a>メソッド getTarget

```xpp
public PrintMedium getTarget()
```

### <a name="return-value---gettarget"></a>戻り値 - getTarget

## <a name="method-hasgenerateddesign"></a>メソッド hasGeneratedDesign

```xpp
public boolean hasGeneratedDesign()
```

### <a name="return-value---hasgenerateddesign"></a>戻り値 - hasGeneratedDesign

## <a name="method-headerdescription"></a>メソッド headerDescription

```xpp
public str headerDescription()
```

### <a name="return-value---headerdescription"></a>戻り値 - headerDescription

## <a name="method-heightofpagefooters"></a>メソッド heightOfPageFooters

```xpp
public int heightOfPageFooters()
```

### <a name="return-value---heightofpagefooters"></a>戻り値 - heightOfPageFooters

## <a name="method-indent"></a>メソッド indent

```xpp
public int indent()
```

### <a name="return-value---indent"></a>戻り値 - indent

## <a name="method-isbodyenabled"></a>メソッド isBodyEnabled

```xpp
public boolean isBodyEnabled(TableId tableId)
```

### <a name="parameters---isbodyenabled"></a>パラメーター - isBodyEnabled

tableId  

### <a name="return-value---isbodyenabled"></a>戻り値 - isBodyEnabled

## <a name="method-jobid"></a>メソッド jobId

```xpp
public Int64 jobId()
```

### <a name="return-value---jobid"></a>戻り値 - jobId

## <a name="method-last"></a>メソッド last

```xpp
public Common last(TableId tableId)
```

### <a name="parameters---last"></a>パラメーター - last

tableId  

### <a name="return-value---last"></a>戻り値 - last

## <a name="method-mm100left"></a>メソッド mm100Left

```xpp
public int mm100Left()
```

### <a name="return-value---mm100left"></a>戻り値 - mm100Left

## <a name="method-mm100pageheight"></a>メソッド mm100PageHeight

```xpp
public int mm100PageHeight()
```

### <a name="return-value---mm100pageheight"></a>戻り値 - mm100PageHeight

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str name])
```

### <a name="parameters---name"></a>パラメーター - name

名前  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-pack"></a>メソッド pack

ReportRun クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

ReportRun クラスの現在のインスタンスを含むコンテナーです。

## <a name="method-packdesign"></a>メソッド packDesign

```xpp
public container packDesign()
```

### <a name="return-value---packdesign"></a>戻り値 - packDesign

## <a name="method-packpagesettings"></a>メソッド packPageSettings

```xpp
public container packPageSettings()
```

### <a name="return-value---packpagesettings"></a>戻り値 - packPageSettings

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

## <a name="method-page"></a>メソッド page

```xpp
public int page([int number])
```

### <a name="parameters---page"></a>パラメーター - page

番号  

### <a name="return-value---page"></a>戻り値 - page

## <a name="method-pageformatting"></a>メソッド pageFormatting

プリンターのプリンター プロパティを表示します。

```xpp
public boolean pageFormatting()
```

### <a name="return-value---pageformatting"></a>戻り値 - pageFormatting

### <a name="remarks---pageformatting"></a>備考 - pageFormatting

レポート オブジェクトのこのメソッドは、カーネルによって呼び出されることはありません。 ユーザーがプロパティ ボタンをクリックすると sysPrintForm フォームによって呼び出すことができますが、代わりに sysPrintForm フォームは直接呼び出します。

## <a name="method-pagestotal"></a>メソッド pagesTotal

```xpp
public int pagesTotal()
```

### <a name="return-value---pagestotal"></a>戻り値 - pagesTotal

## <a name="method-passthrough"></a>メソッド passThrough

```xpp
public str passThrough(str str)
```

### <a name="parameters---passthrough"></a>パラメーター - passThrough

str  

### <a name="return-value---passthrough"></a>戻り値 - passThrough

## <a name="method-pixelsleft"></a>メソッド pixelsLeft

```xpp
public int pixelsLeft()
```

### <a name="return-value---pixelsleft"></a>戻り値 - pixelsLeft

## <a name="method-print"></a>メソッド print

生成されたレポートを、プリンターや画面などの出力メディアに送信します。

```xpp
public int print()
```

### <a name="return-value---print"></a>戻り値 - print

### <a name="remarks---print"></a>備考 - print

このメソッドで super メソッドを呼び出すと、生成されたレポートがプリンターやスクリーンなどの printMedium オブジェクトに送られます。 ターゲットが画像である場合、スーパー メソッドを呼び出すと、reportViewer オブジェクトがクライアント上で作成され、showPage メソッドが呼び出されます。 ターゲットがプリンターである場合、スーパー メソッドを呼び出すと、reportOutput オブジェクトが作成され、このオブジェクトの印刷メソッドが呼び出されます。 PrintJobSettings クラスの outputToClient メソッドが true のパラメーターで呼び出された場合、reportViewer オブジェクトが作成され、そのオブジェクトの印刷メソッドが呼び出されます。 この方法で、サーバーで生成されたレポートはクライアントで設定されているプリンターに出力できます。

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

## <a name="method-printerfontinfo"></a>メソッド printerFontInfo

レポートの印刷に使用されるフォントを示します。

```xpp
public str printerFontInfo()
```

### <a name="return-value---printerfontinfo"></a>戻り値 - printerFontInfo

フォントの名前。

### <a name="remarks---printerfontinfo"></a>備考 - printerFontInfo

レポートの印刷に使用するフォントは、そのフォントがユーザー システムで使用できない可能性があるため、コントロールのフォント プロパティで設定したフォントと必ずしも同じではありません。

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

ユーザーがプリンターの設定を選択できるようにします。

```xpp
public boolean printerSettings([int showWhat])
```

### <a name="parameters---printersettings"></a>パラメーター - printerSettings

showWhat  
このパラメーターは現在機能していません。

### <a name="return-value---printersettings"></a>戻り値 - printerSettings

そのレポートの実行を継続する必要がある場合は true。それ以外の場合は、false。

### <a name="remarks---printersettings"></a>備考 - printerSettings

このメソッドで super メソッドを呼び出すと、sysPrintForm フォームが実行されます。 prompt メソッドは、prompt メソッドの super メソッド呼び出しから呼び出されます。 reportDesign オブジェクトの PrintFormName プロパティは、printerSettings オブジェクトの super メソッドの呼び出しが実行されるフォームを決定します。

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

## <a name="method-printjobsettings"></a>メソッド printJobSettings

```xpp
public PrintJobSettings printJobSettings([container packedPrintJobSettings])
```

### <a name="parameters---printjobsettings"></a>パラメーター - printJobSettings

packedPrintJobSettings  

### <a name="return-value---printjobsettings"></a>戻り値 - printJobSettings

## <a name="method-printsum"></a>メソッド printSum

```xpp
public int printSum()
```

### <a name="return-value---printsum"></a>戻り値 - printSum

## <a name="method-progressform"></a>メソッド progressForm

```xpp
public xFormRun progressForm([xFormRun form])
```

### <a name="parameters---progressform"></a>パラメーター - progressForm

フォーム  

### <a name="return-value---progressform"></a>戻り値 - progressForm

## <a name="method-progressinfo"></a>メソッド progressInfo

セクションが実行されるたびに、レポートが実行中に生成されるレポートの量を記述する文字列を作成します。

```xpp
public str progressInfo(int pageNo, int lineNo)
```

### <a name="parameters---progressinfo"></a>パラメーター - progressInfo

pageNo  
ページのセクション番号。

<!-- -->

lineNo  
ページのセクション番号。

### <a name="return-value---progressinfo"></a>戻り値 - progressInfo

生産されたレポートの量を示す文字列。

## <a name="method-prompt"></a>メソッド prompt

レポートの実行をユーザーに求めます。

```xpp
public boolean prompt([boolean enableCopy], [boolean enablePages], [boolean enableDevice], [boolean enableProperties], [boolean enablePrintTo])
```

### <a name="parameters---prompt"></a>パラメーター - prompt

enableCopy  
ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。

<!-- -->

enablePages  
ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。

<!-- -->

enableDevice  
ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。

<!-- -->

enableProperties  
ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。

<!-- -->

enablePrintTo  
ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。

### <a name="return-value---prompt"></a>戻り値 - prompt

レポートの実行を継続する必要がある場合は true。それ以外の場合は、false。

### <a name="remarks---prompt"></a>備考 - prompt

確認メソッドで super メソッドを呼び出すと、sysPrintForm フォームが実行されます。 このメソッドは、run メソッドから呼び出されます。

## <a name="method-query"></a>メソッド query

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a>パラメーター - query

クエリ  

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-queryrun"></a>メソッド queryRun

```xpp
public QueryRun queryRun([QueryRun queryRun])
```

### <a name="parameters---queryrun"></a>パラメーター - queryRun

queryRun  

### <a name="return-value---queryrun"></a>戻り値 - queryRun

## <a name="method-report"></a>メソッド report

```xpp
public Report report()
```

### <a name="return-value---report"></a>戻り値 - report

## <a name="method-reportuser"></a>メソッド reportUser

```xpp
public str reportUser([str user])
```

### <a name="parameters---reportuser"></a>パラメーター - reportUser

ユーザー  

### <a name="return-value---reportuser"></a>戻り値 - reportUser

## <a name="method-rulercm"></a>メソッド rulerCM

```xpp
public int rulerCM()
```

### <a name="return-value---rulercm"></a>戻り値 - rulerCM

## <a name="method-rulerinch"></a>メソッド rulerINCH

```xpp
public int rulerINCH()
```

### <a name="return-value---rulerinch"></a>戻り値 - rulerINCH

## <a name="method-screenfontinfo"></a>メソッド screenFontInfo

```xpp
public str screenFontInfo()
```

### <a name="return-value---screenfontinfo"></a>戻り値 - screenFontInfo

## <a name="method-section"></a>メソッド section

```xpp
public ReportSection section()
```

### <a name="return-value---section"></a>戻り値 - section

## <a name="method-sectionsleft"></a>メソッド sectionsLeft

```xpp
public int sectionsLeft(ReportSection section)
```

### <a name="parameters---sectionsleft"></a>パラメーター - sectionsLeft

セクション  

### <a name="return-value---sectionsleft"></a>戻り値 - sectionsLeft

## <a name="method-send"></a>メソッド send

セクション グループに属する本文セクションをトリガーします。

```xpp
public boolean send(Common cursor, [int level], [boolean triggerOffBody], [boolean newPageBeforeBody])
```

### <a name="parameters---send"></a>パラメーター - send

cursor  

<!-- -->

level  

<!-- -->

triggerOffBody  

<!-- -->

newPageBeforeBody  

### <a name="return-value---send"></a>戻り値 - send

toPage オブジェクトが生成済みである場合は false; それ以外の場合は true。

### <a name="remarks---send"></a>備考 - send

ReportSection クラスの executeSection メソッドは、トリガーされた各セクションで呼び出されます。 マスター詳細レポートの既定では、マスター テーブルのレコードは 1 のレベルで、詳細テーブルのレコードのレベルは 2 です。

## <a name="method-settarget"></a>メソッド setTarget

```xpp
public PrintMedium setTarget(PrintMedium target)
```

### <a name="parameters---settarget"></a>パラメーター - setTarget

target  

### <a name="return-value---settarget"></a>戻り値 - setTarget

## <a name="method-showmenufunction"></a>メソッド showMenuFunction

```xpp
public boolean showMenuFunction(xMenuFunction menuFunction)
```

### <a name="parameters---showmenufunction"></a>パラメーター - showMenuFunction

menuFunction  

### <a name="return-value---showmenufunction"></a>戻り値 - showMenuFunction

## <a name="method-showmenureference"></a>メソッド showMenuReference

```xpp
public boolean showMenuReference(WebMenu menuReference)
```

### <a name="parameters---showmenureference"></a>パラメーター - showMenuReference

menuReference  

### <a name="return-value---showmenureference"></a>戻り値 - showMenuReference

## <a name="method-sortinfo"></a>メソッド sortInfo

```xpp
public str sortInfo(Common cursor)
```

### <a name="parameters---sortinfo"></a>パラメーター - sortInfo

cursor  

### <a name="return-value---sortinfo"></a>戻り値 - sortInfo

## <a name="method-startdate"></a>メソッド startDate

```xpp
public Date startDate()
```

### <a name="return-value---startdate"></a>戻り値 - startDate

## <a name="method-startdatetime"></a>メソッド startDateTime

```xpp
public DateTime startDateTime()
```

### <a name="return-value---startdatetime"></a>戻り値 - startDateTime

## <a name="method-startmachinedate"></a>メソッド startMachineDate

```xpp
public Date startMachineDate()
```

### <a name="return-value---startmachinedate"></a>戻り値 - startMachineDate

## <a name="method-starttime"></a>メソッド startTime

```xpp
public TimeOfDay startTime()
```

### <a name="return-value---starttime"></a>戻り値 - startTime

## <a name="method-sum"></a>メソッド sum

```xpp
public Real sum(TableId tableId, FieldId fieldId, [int indent])
```

### <a name="parameters---sum"></a>パラメーター - sum

tableId  

<!-- -->

fieldId  

<!-- -->

インデント  

### <a name="return-value---sum"></a>戻り値 - sum

## <a name="method-sumcontrol"></a>メソッド sumControl

```xpp
public Real sumControl(str fieldName, [int indent])
```

### <a name="parameters---sumcontrol"></a>パラメーター - sumControl

fieldName  

<!-- -->

インデント  

### <a name="return-value---sumcontrol"></a>戻り値 - sumControl

## <a name="method-sumcontrolneg"></a>メソッド sumControlNeg

```xpp
public Real sumControlNeg(str fieldName, [int indent])
```

### <a name="parameters---sumcontrolneg"></a>パラメーター - sumControlNeg

fieldName  

<!-- -->

インデント  

### <a name="return-value---sumcontrolneg"></a>戻り値 - sumControlNeg

## <a name="method-sumcontrolpos"></a>メソッド sumControlPos

```xpp
public Real sumControlPos(str fieldName, [int indent])
```

### <a name="parameters---sumcontrolpos"></a>パラメーター - sumControlPos

fieldName  

<!-- -->

インデント  

### <a name="return-value---sumcontrolpos"></a>戻り値 - sumControlPos

## <a name="method-sumdescription"></a>メソッド sumDescription

```xpp
public str sumDescription()
```

### <a name="return-value---sumdescription"></a>戻り値 - sumDescription

## <a name="method-sumneg"></a>メソッド sumNeg

```xpp
public Real sumNeg(TableId tableId, FieldId fieldId, [int indent])
```

### <a name="parameters---sumneg"></a>パラメーター - sumNeg

tableId  

<!-- -->

fieldId  

<!-- -->

インデント  

### <a name="return-value---sumneg"></a>戻り値 - sumNeg

## <a name="method-sumpos"></a>メソッド sumPos

```xpp
public Real sumPos(TableId tableId, FieldId fieldId, [int indent])
```

### <a name="parameters---sumpos"></a>パラメーター - sumPos

tableId  

<!-- -->

fieldId  

<!-- -->

インデント  

### <a name="return-value---sumpos"></a>戻り値 - sumPos

## <a name="method-suppressreportisemptymessage"></a>メソッド suppressReportIsEmptyMessage

```xpp
public boolean suppressReportIsEmptyMessage([boolean suppress])
```

### <a name="parameters---suppressreportisemptymessage"></a>パラメーター - suppressReportIsEmptyMessage

suppress  

### <a name="return-value---suppressreportisemptymessage"></a>戻り値 - suppressReportIsEmptyMessage

## <a name="method-title"></a>メソッド title

印刷ジョブの説明を取得または設定します。

```xpp
public str title([str title])
```

### <a name="parameters---title"></a>パラメーター - title

タイトル  
新しい printJobDescription 値 (オプション)。

### <a name="return-value---title"></a>戻り値 - title

ジョブの説明を含む文字列。

### <a name="remarks---title"></a>備考 - title

レポートが printArchive オブジェクトに書き込まれている場合、印刷ジョブの説明が printJobHeader テーブルの jobDescription フィールドに格納されます。 レポートをプレビューすると、印刷ジョブの説明がキャプションとして使用されます。 このメソッドは、レポートの実行中にカーネルから呼び出されることはありません。 したがって、メソッドを上書きしても影響はありません。

## <a name="method-to"></a>メソッド to

```xpp
public int to([int toPage])
```

### <a name="parameters---to"></a>パラメーター - to

toPage  

### <a name="return-value---to"></a>戻り値 - to

## <a name="method-tostring"></a>メソッド toString

クラスのテキストの説明を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

クラスを説明する文字列。

### <a name="remarks---tostring"></a>備考 - toString

ほとんどのクラスについては、toString メソッドがクラス ハンドルおよび名前を含む文字列を返しますが、一部のクラスでは文字列で詳細情報が返されます。

## <a name="method-unpackpagesettings"></a>メソッド unpackPageSettings

```xpp
public boolean unpackPageSettings(container packedPageSetup)
```

### <a name="parameters---unpackpagesettings"></a>パラメーター - unpackPageSettings

packedPageSetup  

### <a name="return-value---unpackpagesettings"></a>戻り値 - unpackPageSettings

## <a name="method-unpackprintersettings"></a>メソッド unpackPrinterSettings

```xpp
public boolean unpackPrinterSettings(container packedPrinterSetup)
```

### <a name="parameters---unpackprintersettings"></a>パラメーター - unpackPrinterSettings

packedPrinterSetup  

### <a name="return-value---unpackprintersettings"></a>戻り値 - unpackPrinterSettings

## <a name="method-unpackprintjobsettings"></a>メソッド unpackPrintJobSettings

```xpp
public boolean unpackPrintJobSettings(container packedPrintJobSettings)
```

### <a name="parameters---unpackprintjobsettings"></a>パラメーター - unpackPrintJobSettings

packedPrintJobSettings  

### <a name="return-value---unpackprintjobsettings"></a>戻り値 - unpackPrintJobSettings

## <a name="method-unpacksubtotalsettings"></a>メソッド unpackSubtotalSettings

```xpp
public boolean unpackSubtotalSettings(container packedSubtotalSetup)
```

### <a name="parameters---unpacksubtotalsettings"></a>パラメーター - unpackSubtotalSettings

packedSubtotalSetup  

### <a name="return-value---unpacksubtotalsettings"></a>戻り値 - unpackSubtotalSettings

## <a name="method-userselectedorientation"></a>メソッド userSelectedOrientation

```xpp
public PrinterOrientation userSelectedOrientation()
```

### <a name="return-value---userselectedorientation"></a>戻り値 - userSelectedOrientation

## <a name="method-disablebody"></a>メソッド disableBody

```xpp
public void disableBody([TableId tableId])
```

### <a name="parameters---disablebody"></a>パラメーター - disableBody

tableId  

## <a name="method-attach"></a>メソッド attach

```xpp
public void attach()
```

## <a name="method-new"></a>メソッド new

ReportRun クラスのインスタンスを初期化します。

```xpp
public void new(AnyType argsOrReportOrContainer, [str designName], [boolean isWebReport])
```

### <a name="parameters---new"></a>パラメーター - new

argsOrReportOrContainer  

<!-- -->

designName  

<!-- -->

isWebReport  

## <a name="method-disablesection"></a>メソッド disableSection

```xpp
public void disableSection(ReportSection section)
```

### <a name="parameters---disablesection"></a>パラメーター - disableSection

セクション  

## <a name="method-arrangelevelglobal"></a>メソッド arrangeLevelGlobal

```xpp
public void arrangeLevelGlobal()
```

## <a name="method-setescapesequence"></a>メソッド setEscapeSequence

```xpp
public void setEscapeSequence(str str)
```

### <a name="parameters---setescapesequence"></a>パラメーター - setEscapeSequence

str  

## <a name="method-enablebody"></a>メソッド enableBody

```xpp
public void enableBody([TableId tableId])
```

### <a name="parameters---enablebody"></a>パラメーター - enableBody

tableId  

## <a name="method-clearallrangedescriptions"></a>メソッド clearAllRangeDescriptions

```xpp
public void clearAllRangeDescriptions()
```

## <a name="method-header"></a>メソッド header

ヘッダーを制御します。

```xpp
public void header(ReportSection headerSection, TableId tableId, FieldId fieldId)
```

### <a name="parameters---header"></a>パラメーター - header

headerSection  
変更された値を含むフィールドの ID。

<!-- -->

tableId  
変更された値を含むフィールドの ID。

<!-- -->

fieldId  
変更された値を含むフィールドの ID。

### <a name="remarks---header"></a>備考 - header

このメソッドは、フッター メソッドと同様に機能しますが、レコード グループの前に呼び出される点が異なりますが、フッター メソッドはレコード グループの後に呼び出されます。

## <a name="method-unpackdesign"></a>メソッド unpackDesign

```xpp
public void unpackDesign(container packedDesign)
```

### <a name="parameters---unpackdesign"></a>パラメーター - unpackDesign

packedDesign  

## <a name="method-newpage"></a>メソッド newPage

```xpp
public void newPage([boolean doPageFooter])
```

### <a name="parameters---newpage"></a>パラメーター - newPage

doPageFooter  

## <a name="method-footer"></a>メソッド footer

フッターを制御します。

```xpp
public void footer(ReportSection footerSection, TableId tableId, FieldId fieldId)
```

### <a name="parameters---footer"></a>パラメーター - footer

footerSection  
変更された値を含むフィールドの ID。

<!-- -->

tableId  
変更された値を含むフィールドの ID。

<!-- -->

fieldId  
変更された値を含むフィールドの ID。

### <a name="remarks---footer"></a>備考 - footer

このメソッドは、ユーザーがヘッダーまたはフッターを印刷しないように選択した場合でも、値が変更された後にフィールドがソートされたときに呼び出されます。 送信メソッドを 1 回呼び出すと、複数のフッター セクションとヘッダー セクションの印刷を本文セクションの前にトリガーすることができます。 ヘッダーおよびフッター メソッドを使用すると、ユーザーはヘッダーまたはフッターを印刷する前または後にコードを実行できます。

## <a name="method-reset"></a>メソッド reset

複数のレポートを作成する ReportRun クラスの単一インスタンスを有効にします。

```xpp
public void reset([boolean delayExceptions])
```

### <a name="parameters---reset"></a>パラメーター - reset

delayExceptions  

## <a name="method-arrangelevelnone"></a>メソッド arrangeLevelNone

```xpp
public void arrangeLevelNone()
```

## <a name="method-run"></a>メソッド run

レポートを実行します。

```xpp
public void run()
```

### <a name="remarks---run"></a>備考 - run

このメソッドで super メソッドを呼び出すと、次のメソッドが呼び出されます。

-   prompt - ユーザーが sysPrintForm フォームでプリンターを選択することができます
-   fetch - レポート クエリを実行します
-   print - レポートをプリンターまたはディスプレイに導きます。

## <a name="method-gotoymm100"></a>メソッド gotoYmm100

```xpp
public void gotoYmm100([int mm100])
```

### <a name="parameters---gotoymm100"></a>パラメーター - gotoYmm100

mm100  

## <a name="method-disablecolumnheadings"></a>メソッド disableColumnHeadings

```xpp
public void disableColumnHeadings([TableId tableId])
```

### <a name="parameters---disablecolumnheadings"></a>パラメーター - disableColumnHeadings

tableId  

## <a name="method-enablepagefooter"></a>メソッド enablePageFooter

```xpp
public void enablePageFooter()
```

## <a name="method-init"></a>メソッド init

```xpp
public void init()
```

## <a name="method-arrangelevelcontrol"></a>メソッド arrangeLevelControl

```xpp
public void arrangeLevelControl()
```

## <a name="method-disablepagefooter"></a>メソッド disablePageFooter

```xpp
public void disablePageFooter()
```

## <a name="method-addpendingsums"></a>メソッド addPendingSums

レポートの関連するフッターを印刷します。

```xpp
public void addPendingSums()
```

### <a name="remarks---addpendingsums"></a>備考 - addPendingSums

このメソッドは、フェッチ メソッドが複数回呼び出されたレポートでのみ呼び出される必要があります。

## <a name="method-arrangelevelsection"></a>メソッド arrangeLevelSection

```xpp
public void arrangeLevelSection()
```

## <a name="method-enablesection"></a>メソッド enableSection

```xpp
public void enableSection(ReportSection section)
```

### <a name="parameters---enablesection"></a>パラメーター - enableSection

セクション  

## <a name="method-detach"></a>メソッド detach

```xpp
public void detach()
```

## <a name="method-addrangedescription"></a>メソッド addRangeDescription

```xpp
public void addRangeDescription(int x, int y, str text, [str fontName], [int fontSize])
```

### <a name="parameters---addrangedescription"></a>パラメーター - addRangeDescription

x  

<!-- -->

y  

<!-- -->

テキスト  

<!-- -->

fontName  

<!-- -->

fontSize  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

