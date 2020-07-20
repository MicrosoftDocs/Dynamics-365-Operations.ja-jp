---
title: ReportDesign クラス
description: このトピックでは、ReportDesign クラスについて説明します。
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
ms.openlocfilehash: dc1d405c9782b2735257524657bc8272f3e634d2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502841"
---
# <a name="class-reportdesign"></a>クラス ReportDesign

[!include [banner](../../includes/banner.md)]

```xpp
class ReportDesign extends TreeNode
```

ReportDesign クラスは、レポートの内容を決定します。

## <a name="remarks"></a>備考

ReportDesign オブジェクトは、レポートの内容を決定する ReportSection オブジェクトまたは SectionTemplate オブジェクトの集合です。 各レポートは、Designs ノードの下のアプリケーション オブジェクト ツリー (AOT) に ReportDesign ノードを保持しています。 ReportDesign ノードには常に、AutoDesignSpecs という名前のノードが含まれ、生成されたデザインと呼ばれる Design という名前のノードを含めることができます。 ReportDesign ノードには、1 つ以上の SectionTemplate ノード (AutoDesignSpecs ノードの下) または生成されたデザインが含まれている必要があります。 両方が含まれている場合、生成されたデザインのみが使用されます。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 生成されたデザインがないレポートは、生成されたデザインがあるレポートよりもエンド ユーザーにさらに柔軟性を提供します。 たとえば、生成されたデザインがないレポートを実行するユーザーは、どの合計をレポートに含めるかをクエリで決定できます。 生成されたデザインはレポートの実行中に作成され、ユーザーの選択に対応するフッター セクションが含まれます。 レポートに生成されたデザインが含まれている場合、生成されたデザイン内にフッター セクションが存在するため、レポートにその合計が印刷されます。

## <a name="examples"></a>例

次の例では、AOT には存在しない簡易レポートを作成します。

```xpp
static void test(args a) 
{  
    report r; 
    reportDesign rd; 
    reportSection rs; 
    reportRun rr; 
    r = new report(); 
    rd = r.addDesign("myDesign"); 
    // Add a section triggered by execute(1). 
    rs = rd.addProgrammableSection(1);  
    rs.addTextControl("Hello world"); 
    // Run the report. 
    rr = new reportRun(r); 
    // Run the sysPrintForm form. 
    if (rr.prompt())  
    { 
        // Execute the programmableSection. 
        rr.execute(1);  
        // Print the report to the target, such as printer or screen. 
        rr.print();    
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                 | 説明                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public ReportSection addProgrammableSection(int number)                                                |                                                                                                                                           |
| public ReportSection addSection(ReportBlockType sectionType, \[TableId tableId\], \[FieldId fieldId\]) | デザインにレポート セクションを追加します。                                                                                                        |
| public ReportSectionGroup addSectionGroup(TableId tableId, \[FieldId fieldId\])                        | デザインにセクション グループを追加します。                                                                                                         |
| public int arrange()                                                                                   |                                                                                                                                           |
| public int arrangeWhen(\[int value\])                                                                  |                                                                                                                                           |
| public boolean autoDeclaration(\[boolean value\])                                                      | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public ReportAutoDesignSpecs autoDesignSpecs()                                                         |                                                                                                                                           |
| public ReportSection autoSection(TableId tableId, \[int number\])                                      |                                                                                                                                           |
| public int autoSectionControlCount()                                                                   |                                                                                                                                           |
| public ReportControl autoSectionControlNumber(int number)                                              |                                                                                                                                           |
| public int autoSectionCount()                                                                          |                                                                                                                                           |
| public ReportSection autoSectionNumber(int number)                                                     |                                                                                                                                           |
| public int bold(\[int value\])                                                                         | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                               |
| public int bottomMarginMode(\[int value\])                                                             |                                                                                                                                           |
| public str bottomMarginStr(\[str value\])                                                              |                                                                                                                                           |
| public Units bottomMarginUnit(\[Units value\])                                                         |                                                                                                                                           |
| public Real bottomMarginValue(\[Real value\])                                                          |                                                                                                                                           |
| public str caption(\[str value\])                                                                      | コントロールのキャプションを取得または設定します。                                                                                                   |
| public int characterSet(\[int value\])                                                                 | フォントの文字セットを取得または設定します。                                                                                               |
| public boolean collate(\[boolean collate\])                                                            |                                                                                                                                           |
| public int colorScheme(\[int value\])                                                                  | コントロールの配色を取得または設定します。                                                                                             |
| public ReportControl control(TableId tableId, FieldId fieldId)                                         | コントロールのテーブルおよび dataField プロパティに基づいて、生成されたデザインのコントロールを検索します。                                           |
| public int controlCount()                                                                              |                                                                                                                                           |
| public ReportControl controlName(str name)                                                             | コントロールの Name プロパティに基づいて、生成されたデザインのコントロールを検索します。                                                            |
| public ReportControl controlNumber(int number)                                                         |                                                                                                                                           |
| public int copies(\[int numberOfCopies\])                                                              |                                                                                                                                           |
| public int delete()                                                                                    | ノードを AOT から削除します。                                                                                                            |
| public str description(\[str value\])                                                                  |                                                                                                                                           |
| public str deviceName(\[str device\])                                                                  |                                                                                                                                           |
| public str driverName()                                                                                |                                                                                                                                           |
| public boolean edit()                                                                                  |                                                                                                                                           |
| public str emptyReportPrompt(\[str value\])                                                            |                                                                                                                                           |
| public int fitToPage(\[int value\])                                                                    |                                                                                                                                           |
| public str font(\[str value\])                                                                         | 使用するコントロールのフォントの名前を取得または設定します。                                                                                 |
| public int fontSize(\[int value\])                                                                     | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                 |
| public int foregroundColor(\[int value\])                                                              | 使用するコントロールのテキストの色を取得または設定します。                                                                                       |
| public int from(\[int fromPage\])                                                                      |                                                                                                                                           |
| public int generateDesign()                                                                            |                                                                                                                                           |
| public int getNumberOfPrinters()                                                                       |                                                                                                                                           |
| public str getPrinter(int number)                                                                      |                                                                                                                                           |
| public PrintMedium getTarget()                                                                         | レポートの印刷メディア ターゲットを返します。                                                                                           |
| public boolean hideBorder(\[boolean value\])                                                           |                                                                                                                                           |
| public boolean italic(\[boolean value\])                                                               |                                                                                                                                           |
| public str jobType(\[str value\])                                                                      |                                                                                                                                           |
| public int language(\[int value\])                                                                     |                                                                                                                                           |
| public str languageID(\[str lan\])                                                                     |                                                                                                                                           |
| public int leftMarginMode(\[int value\])                                                               |                                                                                                                                           |
| public str leftMarginStr(\[str value\])                                                                |                                                                                                                                           |
| public Units leftMarginUnit(\[Units value\])                                                           |                                                                                                                                           |
| public Real leftMarginValue(\[Real value\])                                                            |                                                                                                                                           |
| public container loadDiskSettings()                                                                    |                                                                                                                                           |
| public str localWebMenu(\[str value\])                                                                 |                                                                                                                                           |
| public str lookupCaption(\[str lan\])                                                                  |                                                                                                                                           |
| public str lookupLabel(str label, \[str lan\])                                                         |                                                                                                                                           |
| public int makeAutoSection(\[Query query\])                                                            |                                                                                                                                           |
| public str name(\[str value\])                                                                         | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int orientation(\[int value\])                                                                  |                                                                                                                                           |
| public container pack()                                                                                | ReportDesign クラスの現在のインスタンスをシリアル化します。                                                                                |
| public container packPageSettings()                                                                    |                                                                                                                                           |
| public container packPrinterSettings()                                                                 |                                                                                                                                           |
| public container packPrintJobSettings()                                                                |                                                                                                                                           |
| public boolean pageFormatting()                                                                        |                                                                                                                                           |
| public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])                         |                                                                                                                                           |
| public int paperTray(\[int tray\])                                                                     |                                                                                                                                           |
| public int printerAttributes()                                                                         |                                                                                                                                           |
| public int printerAveragePPM()                                                                         |                                                                                                                                           |
| public str printerComment()                                                                            |                                                                                                                                           |
| public str printerDatatype()                                                                           |                                                                                                                                           |
| public int printerDefaultPriority()                                                                    |                                                                                                                                           |
| public str printerDriverName()                                                                         |                                                                                                                                           |
| public str printerLocation()                                                                           |                                                                                                                                           |
| public int printerPageHeight()                                                                         |                                                                                                                                           |
| public int printerPageWidth()                                                                          |                                                                                                                                           |
| public int printerPaper()                                                                              |                                                                                                                                           |
| public str printerParameters()                                                                         |                                                                                                                                           |
| public str printerPortName()                                                                           |                                                                                                                                           |
| public str printerPrinterName()                                                                        |                                                                                                                                           |
| public str printerPrintProcessor()                                                                     |                                                                                                                                           |
| public int printerPriority()                                                                           |                                                                                                                                           |
| public int printerQueuedJobs()                                                                         |                                                                                                                                           |
| public str printerSepFile()                                                                            |                                                                                                                                           |
| public str printerServerName()                                                                         |                                                                                                                                           |
| public boolean printerSettings(\[ReportRun reportRun\], \[int showWhat\])                              |                                                                                                                                           |
| public str printerShareName()                                                                          |                                                                                                                                           |
| public int printerStartTime()                                                                          |                                                                                                                                           |
| public int printerStatus()                                                                             |                                                                                                                                           |
| public int printerUntilTime()                                                                          |                                                                                                                                           |
| public str printFormName(\[str value\])                                                                |                                                                                                                                           |
| public PrintJobSettings printJobSettings()                                                             |                                                                                                                                           |
| public boolean removeRedundantFooters(\[boolean value\])                                               |                                                                                                                                           |
| public boolean removeRepeatedFooters(\[boolean value\])                                                |                                                                                                                                           |
| public boolean removeRepeatedHeaders(\[boolean value\])                                                |                                                                                                                                           |
| public str reportTemplate(\[str value\])                                                               |                                                                                                                                           |
| public str resolutionX(\[str value\])                                                                  |                                                                                                                                           |
| public int resolutionXStr(str value)                                                                   |                                                                                                                                           |
| public Units resolutionXUnit(\[Units value\])                                                          |                                                                                                                                           |
| public str resolutionY(\[str value\])                                                                  |                                                                                                                                           |
| public int resolutionYStr(str value)                                                                   |                                                                                                                                           |
| public Units resolutionYUnit(\[Units value\])                                                          |                                                                                                                                           |
| public int rightMarginMode(\[int value\])                                                              |                                                                                                                                           |
| public str rightMarginStr(\[str value\])                                                               |                                                                                                                                           |
| public Units rightMarginUnit(\[Units value\])                                                          |                                                                                                                                           |
| public Real rightMarginValue(\[Real value\])                                                           |                                                                                                                                           |
| public int ruler(\[int value\])                                                                        |                                                                                                                                           |
| public boolean saveDiskSettings(container buffer)                                                      |                                                                                                                                           |
| public ReportSection section(int number)                                                               | 生成されたデザイン ノードの下のセクションを検索します。                                                                                          |
| public int sectionCount()                                                                              |                                                                                                                                           |
| public ReportSectionGroup sectionGroup(TableId tableId, \[FieldId fieldId\])                           | reportDesign オブジェクトの下の reportSectionGroup オブジェクトを検索します。                                                                            |
| public ReportSection sectionName(str name)                                                             |                                                                                                                                           |
| public ReportSection sectionNumber(int number)                                                         |                                                                                                                                           |
| public PrintMedium setTarget(PrintMedium target)                                                       | レポートの印刷メディア ターゲットを設定します。                                                                                              |
| public int to(\[int toPage\])                                                                          |                                                                                                                                           |
| public int topMarginMode(\[int value\])                                                                |                                                                                                                                           |
| public str topMarginStr(\[str value\])                                                                 |                                                                                                                                           |
| public Units topMarginUnit(\[Units value\])                                                            |                                                                                                                                           |
| public Real topMarginValue(\[Real value\])                                                             |                                                                                                                                           |
| public str toString()                                                                                  | クラス ハンドルと名前を含む文字列を返します。                                                                                 |
| public boolean underline(\[boolean value\])                                                            |                                                                                                                                           |
| public boolean unpackPageSettings(container packedPageSetup)                                           |                                                                                                                                           |
| public boolean unpackPrinterSettings(container packedPrintSetup)                                       |                                                                                                                                           |
| public boolean unpackPrintJobSettings(container packedPrintJobSettings)                                |                                                                                                                                           |
| public void leftMargin(Real value, Units unit)                                                         |                                                                                                                                           |
| public void bottomMargin(Real value, Units unit)                                                       |                                                                                                                                           |
| public void rightMargin(Real value, Units unit)                                                        |                                                                                                                                           |
| public void topMargin(Real value, Units unit)                                                          |                                                                                                                                           |
| public void deleteDiskSettings(\[boolean allUsers\])                                                   |                                                                                                                                           |

## <a name="method-addprogrammablesection"></a>メソッド addProgrammableSection

```xpp
public ReportSection addProgrammableSection(int number)
```

### <a name="parameters---addprogrammablesection"></a>パラメーター - addProgrammableSection

番号  

### <a name="return-value---addprogrammablesection"></a>戻り値 - addProgrammableSection

## <a name="method-addsection"></a>メソッド addSection

デザインにレポート セクションを追加します。

```xpp
public ReportSection addSection(ReportBlockType sectionType, [TableId tableId], [FieldId fieldId])
```

### <a name="parameters---addsection"></a>パラメーター - addSection

sectionType  
sectionType パラメーターがヘッダー、本文、またはフッターに設定されている場合、セクションが属するセクション グループの dataField プロパティはオプションになります。

<!-- -->

tableId  
sectionType パラメーターがヘッダー、本文、またはフッターに設定されている場合、セクションが属するセクション グループの dataField プロパティはオプションになります。

<!-- -->

fieldId  
sectionType パラメーターがヘッダー、本文、またはフッターに設定されている場合、セクションが属するセクション グループの dataField プロパティはオプションになります。

### <a name="return-value---addsection"></a>戻り値 - addSection

作成されたセクション。

### <a name="remarks---addsection"></a>備考 - addSection

このメソッドは、生成されたデザインを作成します (存在しない場合)。 SectionType パラメーターが、ヘッダー、本文またはフッターに設定されている場合、セクション グループが存在しないと、メソッドはセクション グループを作成します。

## <a name="method-addsectiongroup"></a>メソッド addSectionGroup

デザインにセクション グループを追加します。

```xpp
public ReportSectionGroup addSectionGroup(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---addsectiongroup"></a>パラメーター - addSectionGroup

tableId  
セクション グループのデータ フィールドのプロパティ (オプション)。

<!-- -->

fieldId  
セクション グループのデータ フィールドのプロパティ (オプション)。

### <a name="return-value---addsectiongroup"></a>戻り値 - addSectionGroup

作成されたセクション グループ。

### <a name="remarks---addsectiongroup"></a>備考 - addSectionGroup

このメソッドは、生成されたデザインを作成します (存在しない場合)。

## <a name="method-arrange"></a>メソッド arrange

```xpp
public int arrange()
```

### <a name="return-value---arrange"></a>戻り値 - arrange

## <a name="method-arrangewhen"></a>メソッド arrangeWhen

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a>パラメーター - arrangeWhen

値  

### <a name="return-value---arrangewhen"></a>戻り値 - arrangeWhen

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

## <a name="method-autodesignspecs"></a>メソッド autoDesignSpecs

```xpp
public ReportAutoDesignSpecs autoDesignSpecs()
```

### <a name="return-value---autodesignspecs"></a>戻り値 - autoDesignSpecs

## <a name="method-autosection"></a>メソッド autoSection

```xpp
public ReportSection autoSection(TableId tableId, [int number])
```

### <a name="parameters---autosection"></a>パラメーター - autoSection

tableId  

<!-- -->

番号  

### <a name="return-value---autosection"></a>戻り値 - autoSection

## <a name="method-autosectioncontrolcount"></a>メソッド autoSectionControlCount

```xpp
public int autoSectionControlCount()
```

### <a name="return-value---autosectioncontrolcount"></a>戻り値 - autoSectionControlCount

## <a name="method-autosectioncontrolnumber"></a>メソッド autoSectionControlNumber

```xpp
public ReportControl autoSectionControlNumber(int number)
```

### <a name="parameters---autosectioncontrolnumber"></a>パラメーター - autoSectionControlNumber

番号  

### <a name="return-value---autosectioncontrolnumber"></a>戻り値 - autoSectionControlNumber

## <a name="method-autosectioncount"></a>メソッド autoSectionCount

```xpp
public int autoSectionCount()
```

### <a name="return-value---autosectioncount"></a>戻り値 - autoSectionCount

## <a name="method-autosectionnumber"></a>メソッド autoSectionNumber

```xpp
public ReportSection autoSectionNumber(int number)
```

### <a name="parameters---autosectionnumber"></a>パラメーター - autoSectionNumber

番号  

### <a name="return-value---autosectionnumber"></a>戻り値 - autoSectionNumber

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

次のテーブルの値は、中東言語語版 Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

## <a name="method-collate"></a>メソッド collate

```xpp
public boolean collate([boolean collate])
```

### <a name="parameters---collate"></a>パラメーター - collate

collate  

### <a name="return-value---collate"></a>戻り値 - collate

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

| 値です。 | スタイル。                 |
|--------|------------------------|
| 0      | 既定。               |
| 1      | Windows パレット。   |
| 2      | 真の配色。 |

## <a name="method-control"></a>メソッド control

コントロールのテーブルおよび dataField プロパティに基づいて、生成されたデザインのコントロールを検索します。

```xpp
public ReportControl control(TableId tableId, FieldId fieldId)
```

### <a name="parameters---control"></a>パラメーター - control

tableId  
コントロールのデータ フィールドのプロパティ。

<!-- -->

fieldId  
コントロールのデータ フィールドのプロパティ。

### <a name="return-value---control"></a>戻り値 - control

見つかったコントロール。

### <a name="examples---control"></a>例 - control

```xpp
reportDesign rd = ...; 
reportControl rc = rd.control(tablenum(CustGroup), 
    fieldnum(CustGroup, Name));
```

## <a name="method-controlcount"></a>メソッド controlCount

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a>戻り値 - controlCount

## <a name="method-controlname"></a>メソッド controlName

コントロールの Name プロパティに基づいて、生成されたデザインのコントロールを検索します。

```xpp
public ReportControl controlName(str name)
```

### <a name="parameters---controlname"></a>パラメーター - controlName

名前  
文字列としての表現される、コントロールの Name プロパティ。

### <a name="return-value---controlname"></a>戻り値 - controlName

見つかったコントロール。

## <a name="method-controlnumber"></a>メソッド controlNumber

```xpp
public ReportControl controlNumber(int number)
```

### <a name="parameters---controlnumber"></a>パラメーター - controlNumber

番号  

### <a name="return-value---controlnumber"></a>戻り値 - controlNumber

## <a name="method-copies"></a>メソッド copies

```xpp
public int copies([int numberOfCopies])
```

### <a name="parameters---copies"></a>パラメーター - copies

numberOfCopies  

### <a name="return-value---copies"></a>戻り値 - copies

## <a name="method-delete"></a>メソッド delete

ノードを AOT から削除します。

```xpp
public int delete()
```

### <a name="return-value---delete"></a>戻り値 - delete

整数。

## <a name="method-description"></a>メソッドの説明

```xpp
public str description([str value])
```

### <a name="parameters---description"></a>パラメーター - description

値  

### <a name="return-value---description"></a>戻り値 - description

## <a name="method-devicename"></a>メソッド deviceName

```xpp
public str deviceName([str device])
```

### <a name="parameters---devicename"></a>パラメーター - deviceName

デバイス  

### <a name="return-value---devicename"></a>戻り値 - deviceName

## <a name="method-drivername"></a>メソッド driverName

```xpp
public str driverName()
```

### <a name="return-value---drivername"></a>戻り値 - driverName

## <a name="method-edit"></a>メソッド edit

```xpp
public boolean edit()
```

### <a name="return-value---edit"></a>戻り値 - edit

## <a name="method-emptyreportprompt"></a>メソッド emptyReportPrompt

```xpp
public str emptyReportPrompt([str value])
```

### <a name="parameters---emptyreportprompt"></a>パラメーター - emptyReportPrompt

値  

### <a name="return-value---emptyreportprompt"></a>戻り値 - emptyReportPrompt

## <a name="method-fittopage"></a>メソッド fitToPage

```xpp
public int fitToPage([int value])
```

### <a name="parameters---fittopage"></a>パラメーター - fitToPage

値  

### <a name="return-value---fittopage"></a>戻り値 - fitToPage

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

## <a name="method-from"></a>メソッド from

```xpp
public int from([int fromPage])
```

### <a name="parameters---from"></a>パラメーター - from

fromPage  

### <a name="return-value---from"></a>戻り値 - from

## <a name="method-generatedesign"></a>メソッド generateDesign

```xpp
public int generateDesign()
```

### <a name="return-value---generatedesign"></a>戻り値 - generateDesign

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

## <a name="method-gettarget"></a>メソッド getTarget

レポートの印刷メディア ターゲットを返します。

```xpp
public PrintMedium getTarget()
```

### <a name="return-value---gettarget"></a>戻り値 - getTarget

レポートのターゲット。

## <a name="method-hideborder"></a>メソッド hideBorder

```xpp
public boolean hideBorder([boolean value])
```

### <a name="parameters---hideborder"></a>パラメーター - hideBorder

値  

### <a name="return-value---hideborder"></a>戻り値 - hideBorder

## <a name="method-italic"></a>メソッド italic

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a>パラメーター - italic

値  

### <a name="return-value---italic"></a>戻り値 - italic

## <a name="method-jobtype"></a>メソッド jobType

```xpp
public str jobType([str value])
```

### <a name="parameters---jobtype"></a>パラメーター - jobType

値  

### <a name="return-value---jobtype"></a>戻り値 - jobType

## <a name="method-language"></a>メソッド language

```xpp
public int language([int value])
```

### <a name="parameters---language"></a>パラメーター - language

値  

### <a name="return-value---language"></a>戻り値 - language

## <a name="method-languageid"></a>メソッド languageID

```xpp
public str languageID([str lan])
```

### <a name="parameters---languageid"></a>パラメーター - languageID

lan  

### <a name="return-value---languageid"></a>戻り値 - languageID

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

## <a name="method-loaddisksettings"></a>メソッド loadDiskSettings

```xpp
public container loadDiskSettings()
```

### <a name="return-value---loaddisksettings"></a>戻り値 - loadDiskSettings

## <a name="method-localwebmenu"></a>メソッド localWebMenu

```xpp
public str localWebMenu([str value])
```

### <a name="parameters---localwebmenu"></a>パラメーター - localWebMenu

値  

### <a name="return-value---localwebmenu"></a>戻り値 - localWebMenu

## <a name="method-lookupcaption"></a>メソッド lookupCaption

```xpp
public str lookupCaption([str lan])
```

### <a name="parameters---lookupcaption"></a>パラメーター - lookupCaption

lan  

### <a name="return-value---lookupcaption"></a>戻り値 - lookupCaption

## <a name="method-lookuplabel"></a>メソッド lookupLabel

```xpp
public str lookupLabel(str label, [str lan])
```

### <a name="parameters---lookuplabel"></a>パラメーター - lookupLabel

ラベル  

<!-- -->

lan  

### <a name="return-value---lookuplabel"></a>戻り値 - lookupLabel

## <a name="method-makeautosection"></a>メソッド makeAutoSection

```xpp
public int makeAutoSection([Query query])
```

### <a name="parameters---makeautosection"></a>パラメーター - makeAutoSection

クエリ  

### <a name="return-value---makeautosection"></a>戻り値 - makeAutoSection

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-orientation"></a>メソッド orientation

```xpp
public int orientation([int value])
```

### <a name="parameters---orientation"></a>パラメーター - orientation

値  

### <a name="return-value---orientation"></a>戻り値 - orientation

## <a name="method-pack"></a>メソッド pack

ReportDesign クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

ReportDesign クラスの現在のインスタンスを含むコンテナーです。

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
public boolean printerSettings([ReportRun reportRun], [int showWhat])
```

### <a name="parameters---printersettings"></a>パラメーター - printerSettings

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
public int printerStartTime()
```

### <a name="return-value---printerstarttime"></a>戻り値 - printerStartTime

## <a name="method-printerstatus"></a>メソッド printerStatus

```xpp
public int printerStatus()
```

### <a name="return-value---printerstatus"></a>戻り値 - printerStatus

## <a name="method-printeruntiltime"></a>メソッド printerUntilTime

```xpp
public int printerUntilTime()
```

### <a name="return-value---printeruntiltime"></a>戻り値 - printerUntilTime

## <a name="method-printformname"></a>メソッド printFormName

```xpp
public str printFormName([str value])
```

### <a name="parameters---printformname"></a>パラメーター - printFormName

値  

### <a name="return-value---printformname"></a>戻り値 - printFormName

## <a name="method-printjobsettings"></a>メソッド printJobSettings

```xpp
public PrintJobSettings printJobSettings()
```

### <a name="return-value---printjobsettings"></a>戻り値 - printJobSettings

## <a name="method-removeredundantfooters"></a>メソッド removeRedundantFooters

```xpp
public boolean removeRedundantFooters([boolean value])
```

### <a name="parameters---removeredundantfooters"></a>パラメーター - removeRedundantFooters

値  

### <a name="return-value---removeredundantfooters"></a>戻り値 - removeRedundantFooters

## <a name="method-removerepeatedfooters"></a>メソッド removeRepeatedFooters

```xpp
public boolean removeRepeatedFooters([boolean value])
```

### <a name="parameters---removerepeatedfooters"></a>パラメーター - removeRepeatedFooters

値  

### <a name="return-value---removerepeatedfooters"></a>戻り値 - removeRepeatedFooters

## <a name="method-removerepeatedheaders"></a>メソッド removeRepeatedHeaders

```xpp
public boolean removeRepeatedHeaders([boolean value])
```

### <a name="parameters---removerepeatedheaders"></a>パラメーター - removeRepeatedHeaders

値  

### <a name="return-value---removerepeatedheaders"></a>戻り値 - removeRepeatedHeaders

## <a name="method-reporttemplate"></a>メソッド reportTemplate

```xpp
public str reportTemplate([str value])
```

### <a name="parameters---reporttemplate"></a>パラメーター - reportTemplate

値  

### <a name="return-value---reporttemplate"></a>戻り値 - reportTemplate

## <a name="method-resolutionx"></a>メソッド resolutionX

```xpp
public str resolutionX([str value])
```

### <a name="parameters---resolutionx"></a>パラメーター - resolutionX

値  

### <a name="return-value---resolutionx"></a>戻り値 - resolutionX

## <a name="method-resolutionxstr"></a>メソッド resolutionXStr

```xpp
public int resolutionXStr(str value)
```

### <a name="parameters---resolutionxstr"></a>パラメーター - resolutionXStr

値  

### <a name="return-value---resolutionxstr"></a>戻り値 - resolutionXStr

## <a name="method-resolutionxunit"></a>メソッド resolutionXUnit

```xpp
public Units resolutionXUnit([Units value])
```

### <a name="parameters---resolutionxunit"></a>パラメーター - resolutionXUnit

値  

### <a name="return-value---resolutionxunit"></a>戻り値 - resolutionXUnit

## <a name="method-resolutiony"></a>メソッド resolutionY

```xpp
public str resolutionY([str value])
```

### <a name="parameters---resolutiony"></a>パラメーター - resolutionY

値  

### <a name="return-value---resolutiony"></a>戻り値 - resolutionY

## <a name="method-resolutionystr"></a>メソッド resolutionYStr

```xpp
public int resolutionYStr(str value)
```

### <a name="parameters---resolutionystr"></a>パラメーター - resolutionYStr

値  

### <a name="return-value---resolutionystr"></a>戻り値 - resolutionYStr

## <a name="method-resolutionyunit"></a>メソッド resolutionYUnit

```xpp
public Units resolutionYUnit([Units value])
```

### <a name="parameters---resolutionyunit"></a>パラメーター - resolutionYUnit

値  

### <a name="return-value---resolutionyunit"></a>戻り値 - resolutionYUnit

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

## <a name="method-ruler"></a>メソッド ruler

```xpp
public int ruler([int value])
```

### <a name="parameters---ruler"></a>パラメーター - ruler

値  

### <a name="return-value---ruler"></a>戻り値 - ruler

## <a name="method-savedisksettings"></a>メソッド saveDiskSettings

```xpp
public boolean saveDiskSettings(container buffer)
```

### <a name="parameters---savedisksettings"></a>パラメーター - saveDiskSettings

バッファ  

### <a name="return-value---savedisksettings"></a>戻り値 - saveDiskSettings

## <a name="method-section"></a>メソッド section

生成されたデザイン ノードの下のセクションを検索します。

```xpp
public ReportSection section(int number)
```

### <a name="parameters---section"></a>パラメーター - section

番号  
セクション番号。

### <a name="return-value---section"></a>戻り値 - section

検索されるレポート セクション。

## <a name="method-sectioncount"></a>メソッド sectionCount

```xpp
public int sectionCount()
```

### <a name="return-value---sectioncount"></a>戻り値 - sectionCount

## <a name="method-sectiongroup"></a>メソッド sectionGroup

reportDesign オブジェクトの下の reportSectionGroup オブジェクトを検索します。

```xpp
public ReportSectionGroup sectionGroup(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---sectiongroup"></a>パラメーター - sectionGroup

tableId  
セクション グループのフィールド (オプション)。

<!-- -->

fieldId  
セクション グループのフィールド (オプション)。

### <a name="return-value---sectiongroup"></a>戻り値 - sectionGroup

引数に一致するセクション グループ。

### <a name="examples---sectiongroup"></a>例 - sectionGroup

次の例では、addSection メソッドで作成されたセクション グループを検索します。

```xpp
static void test(args a) 
{ 
    reportRun rr; 
    inventTrans rec; 
    int i; 
    int t = tablenum(inventTrans); 
    int f = fieldnum(inventTrans, datePhysical); 
    // Create a simple report that is not present in 
    // the Application Object Tree. 
    report r = new report(); 
    reportDesign rd = r.addDesign("myDesign"); 
    reportSectionGroup rsg; 
    reportSection rs = rd.AddSection(reportBlockType::body, t); 
    rs.addControl(t,f); 
    rsg = rd.SectionGroup(t); 
    if (rsg) 
    { 
        rs = rsg.AddSection(ReportBlockType::Header); 
        rs.AddTextControl("This is the groupHeader"); 
    } 
    // Run the report. 
    rr = new reportRun(r); 
    // Run the sysPrintForm form 
    if (rr.prompt()) 
    { 
        select rec; 
        rr.send(rec); 
        // Print the report to the target, such as printer or screen, that  
        // was selected during the prompt call above. 
        rr.print();  
    } 
}
```

## <a name="method-sectionname"></a>メソッド sectionName

```xpp
public ReportSection sectionName(str name)
```

### <a name="parameters---sectionname"></a>パラメーター - sectionName

名前  

### <a name="return-value---sectionname"></a>戻り値 - sectionName

## <a name="method-sectionnumber"></a>メソッド sectionNumber

```xpp
public ReportSection sectionNumber(int number)
```

### <a name="parameters---sectionnumber"></a>パラメーター - sectionNumber

番号  

### <a name="return-value---sectionnumber"></a>戻り値 - sectionNumber

## <a name="method-settarget"></a>メソッド setTarget

レポートの印刷メディア ターゲットを設定します。

```xpp
public PrintMedium setTarget(PrintMedium target)
```

### <a name="parameters---settarget"></a>パラメーター - setTarget

target  
レポートの印刷メディア。

### <a name="return-value---settarget"></a>戻り値 - setTarget

レポートの印刷メディア。

### <a name="remarks---settarget"></a>備考 - setTarget

レポートの対象として特定のプリンターを選択するには、ReportDesign.printJobSettings メソッドによって返されるオブジェクトに対して PrintJobSettings.deviceName メソッドを呼び出します。

## <a name="method-to"></a>メソッド to

```xpp
public int to([int toPage])
```

### <a name="parameters---to"></a>パラメーター - to

toPage  

### <a name="return-value---to"></a>戻り値 - to

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

## <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前を含む文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

クラスのテキストの説明。

### <a name="remarks---tostring"></a>備考 - toString

一部のクラスでは、追加情報が文字列で返されます。

## <a name="method-underline"></a>メソッド underline

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a>パラメーター - underline

値  

### <a name="return-value---underline"></a>戻り値 - underline

## <a name="method-unpackpagesettings"></a>メソッド unpackPageSettings

```xpp
public boolean unpackPageSettings(container packedPageSetup)
```

### <a name="parameters---unpackpagesettings"></a>パラメーター - unpackPageSettings

packedPageSetup  

### <a name="return-value---unpackpagesettings"></a>戻り値 - unpackPageSettings

## <a name="method-unpackprintersettings"></a>メソッド unpackPrinterSettings

```xpp
public boolean unpackPrinterSettings(container packedPrintSetup)
```

### <a name="parameters---unpackprintersettings"></a>パラメーター - unpackPrinterSettings

packedPrintSetup  

### <a name="return-value---unpackprintersettings"></a>戻り値 - unpackPrinterSettings

## <a name="method-unpackprintjobsettings"></a>メソッド unpackPrintJobSettings

```xpp
public boolean unpackPrintJobSettings(container packedPrintJobSettings)
```

### <a name="parameters---unpackprintjobsettings"></a>パラメーター - unpackPrintJobSettings

packedPrintJobSettings  

### <a name="return-value---unpackprintjobsettings"></a>戻り値 - unpackPrintJobSettings

## <a name="method-leftmargin"></a>メソッド leftMargin

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a>パラメーター - leftMargin

値  

<!-- -->

単位  

## <a name="method-bottommargin"></a>メソッド bottomMargin

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a>パラメーター - bottomMargin

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

## <a name="method-topmargin"></a>メソッド topMargin

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a>パラメーター - topMargin

値  

<!-- -->

単位  

## <a name="method-deletedisksettings"></a>メソッド deleteDiskSettings

```xpp
public void deleteDiskSettings([boolean allUsers])
```

### <a name="parameters---deletedisksettings"></a>パラメーター - deleteDiskSettings

allUsers  

