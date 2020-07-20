---
title: ReportOutput クラス
description: このトピックでは、ReportOutput クラスについて説明します。
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
ms.openlocfilehash: 698564bf0956a38718db97ce7e23b31a93695552
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502837"
---
# <a name="class-reportoutput"></a>クラス ReportOutput

[!include [banner](../../includes/banner.md)]

```xpp
class ReportOutput extends Object
```

ReportOutput クラスは、プリンターやファイルへのレポートの出力を処理します。

## <a name="remarks"></a>備考

このクラスは、レポートのプレビューを処理する ReportViewer クラス、およびユーザー定義のターゲットへのレポートの出力をユーザー定義の形式で処理する ReportOutputUser クラスの基本クラスとして機能します。 一般に、プリンターにレポートを印刷する場合、印刷メソッドは ReportOutput オブジェクトを作成し、その印刷メソッドを呼び出します。 printJobSettings::outputToClient(TRUE) への呼び出しが行われている場合は、ReportViewer オブジェクトが作成されます。 ReportViewer オブジェクトはサーバー上ではなくクライアント上にしか存在しないため、印刷メソッドを呼び出すと、クライアントに設定されているプリンタでレポートが印刷されます。

## <a name="examples"></a>例

次の例では、現在の日付に printArchive テーブルに挿入されたジョブのジョブの説明とページ番号を出力し、既定のプリンタに 1 ページを出力します。

```xpp
static void aaaReportOutputExample(args a) 
{ 
    printJobHeader printJobHeader; 
    printJobPages printJobPages; 
    int myrecId; 
    reportViewer reportViewer; 
    while select printJobHeader where printJobHeader.createdDateTime >=
        str2datetime("01/01/2011 12:00:00", 123) 
    { 
        myrecId = printJobHeader.recId; 
        print printJobHeader.jobDescription; 
        while select printJobPages  
            where printJobPages.pagesHeaderRecId == myRecId 
        print printJobPages.PageNo; 
        reportViewer = new reportOutput(printJobHeader); 
        reportViewer.print(); 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                    | 説明                                     |
|---------------------------------------------------------------------------|-------------------------------------------------|
| public str description(\[str description\])                               |                                                 |
| public int getCopyNo()                                                    |                                                 |
| public boolean getDeclineOverwrite()                                      |                                                 |
| public int getLastCopyNo()                                                |                                                 |
| public int getLastPageNo()                                                |                                                 |
| public int getPageNo()                                                    |                                                 |
| public str getTempFileName(str prefix)                                    |                                                 |
| public PrintJobStatus jobStatus()                                         |                                                 |
| public PrintJobSettings printJobSettings()                                |                                                 |
| public boolean setNumberOfPages(int pageNo)                               |                                                 |
| public str type(\[str type\])                                             |                                                 |
| public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\]) | Object クラスの新しいインスタンスを初期化します。 |
| public void printAscii(str filename)                                      |                                                 |
| public void printTextUTF8(str filename)                                   | レポートを UTF-8 形式で印刷します。              |
| public void printRTF(str filename)                                        |                                                 |
| public void print()                                                       |                                                 |
| public void printPDF(str filename, \[boolean embedFonts\])                |                                                 |
| public void printHTML(str filename)                                       |                                                 |
| public void abort()                                                       |                                                 |
| public void dialogAndPrint()                                              |                                                 |
| public void printToTarget()                                               |                                                 |

## <a name="method-description"></a>メソッドの説明

```xpp
public str description([str description])
```

### <a name="parameters---description"></a>パラメーター - description

説明  

### <a name="return-value---description"></a>戻り値 - description

## <a name="method-getcopyno"></a>メソッド getCopyNo

```xpp
public int getCopyNo()
```

### <a name="return-value---getcopyno"></a>戻り値 - getCopyNo

## <a name="method-getdeclineoverwrite"></a>メソッド getDeclineOverwrite

```xpp
public boolean getDeclineOverwrite()
```

### <a name="return-value---getdeclineoverwrite"></a>戻り値 - getDeclineOverwrite

## <a name="method-getlastcopyno"></a>メソッド getLastCopyNo

```xpp
public int getLastCopyNo()
```

### <a name="return-value---getlastcopyno"></a>戻り値 - getLastCopyNo

## <a name="method-getlastpageno"></a>メソッド getLastPageNo

```xpp
public int getLastPageNo()
```

### <a name="return-value---getlastpageno"></a>戻り値 - getLastPageNo

## <a name="method-getpageno"></a>メソッド getPageNo

```xpp
public int getPageNo()
```

### <a name="return-value---getpageno"></a>戻り値 - getPageNo

## <a name="method-gettempfilename"></a>メソッド getTempFileName

```xpp
public str getTempFileName(str prefix)
```

### <a name="parameters---gettempfilename"></a>パラメーター - getTempFileName

prefix  

### <a name="return-value---gettempfilename"></a>戻り値 - getTempFileName

## <a name="method-jobstatus"></a>メソッド jobStatus

```xpp
public PrintJobStatus jobStatus()
```

### <a name="return-value---jobstatus"></a>戻り値 - jobStatus

## <a name="method-printjobsettings"></a>メソッド printJobSettings

```xpp
public PrintJobSettings printJobSettings()
```

### <a name="return-value---printjobsettings"></a>戻り値 - printJobSettings

## <a name="method-setnumberofpages"></a>メソッド setNumberOfPages

```xpp
public boolean setNumberOfPages(int pageNo)
```

### <a name="parameters---setnumberofpages"></a>パラメーター - setNumberOfPages

pageNo  

### <a name="return-value---setnumberofpages"></a>戻り値 - setNumberOfPages

## <a name="method-type"></a>メソッドのタイプ

```xpp
public str type([str type])
```

### <a name="parameters---type"></a>パラメーター - タイプ

タイプ  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(PrintJobHeader jobsCursor, [PrintJobPages pagesCursor])
```

### <a name="parameters---new"></a>パラメーター - new

jobsCursor  

<!-- -->

pagesCursor  

## <a name="method-printascii"></a>メソッド printAscii

```xpp
public void printAscii(str filename)
```

### <a name="parameters---printascii"></a>パラメーター - printAscii

filename  

## <a name="method-printtextutf8"></a>メソッド printTextUTF8

レポートを UTF-8 形式で印刷します。

```xpp
public void printTextUTF8(str filename)
```

### <a name="parameters---printtextutf8"></a>パラメーター - printTextUTF8

filename  
レポートを印刷するファイルの名前を指定する文字列。

### <a name="remarks---printtextutf8"></a>備考 - printTextUTF8

UTF-8 は、1 つの文字列にシングルバイト文字とマルチバイト文字の両方を使用できる文字エンコード方法です。

### <a name="examples---printtextutf8"></a>例 - printTextUTF8

次の例は、printTextUTF8 メソッドの呼び出しを示しています。

```xpp
void printTextUTF8() 
{ 
    ReportOutput reportOutput; 
    printJobHeader printJobHeader; 
    while select printJobHeader where printJobHeader.createdDateTime >= 
        str2datetime("01/01/2011 12:00:00", 123)
    { 
        print printJobHeader.jobDescription; 
        reportOutput = new ReportOutput(printJobHeader); 
        reportOutput.printTextUTF8("c:\\report.txt"); 
    } 
}
```

## <a name="method-printrtf"></a>メソッド printRTF

```xpp
public void printRTF(str filename)
```

### <a name="parameters---printrtf"></a>パラメーター - printRTF

filename  

## <a name="method-print"></a>メソッド print

```xpp
public void print()
```

## <a name="method-printpdf"></a>メソッド printPDF

```xpp
public void printPDF(str filename, [boolean embedFonts])
```

### <a name="parameters---printpdf"></a>パラメーター - printPDF

filename  

<!-- -->

embedFonts  

## <a name="method-printhtml"></a>メソッド printHTML

```xpp
public void printHTML(str filename)
```

### <a name="parameters---printhtml"></a>パラメーター - printHTML

filename  

## <a name="method-abort"></a>メソッド abort

```xpp
public void abort()
```

## <a name="method-dialogandprint"></a>メソッド dialogAndPrint

```xpp
public void dialogAndPrint()
```

## <a name="method-printtotarget"></a>メソッド printToTarget

```xpp
public void printToTarget()
```

