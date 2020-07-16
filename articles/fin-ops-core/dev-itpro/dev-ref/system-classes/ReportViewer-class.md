---
title: ReportViewer クラス
description: このトピックでは、ReportViewer クラスについて説明します。
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
ms.openlocfilehash: 2662b9622e6f8d5cf92e57d0cf193ea81abf1f21
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502824"
---
# <a name="class-reportviewer"></a>クラス ReportViewer

[!include [banner](../../includes/banner.md)]

```xpp
class ReportViewer extends ReportOutput
```

ReportViewer クラスを使用すると、ユーザーがレポートをプレビューできます。

## <a name="remarks"></a>備考

レポート プレビューはクライアントでのみ可能なため、クライアント上にのみ ReportViewer オブジェクトが存在することができます。

## <a name="examples"></a>例

次のコードは、現在の日付の printArchive に挿入されているジョブの説明とジョブのページ番号を出力し、ページ 1 をレポート ビューアーに表示します。

```xpp
static void aaaReportOutputExample(args a) 
{ 
    PrintJobHeader printJobHeader; 
    PrintJobPages printJobPages; 
    int myrecId; 
    reportViewer reportViewer; 
    while select printJobHeader where printJobHeader.CreatedDate >= 
            str2datetime("01/01/2011 12:00:00 am",123)
    { 
        myrecId = printJobHeader.recId; 
        print printJobHeader.jobDescription; 
        while select printJobPages  
            where printJobPages.pagesHeaderRecId == myRecId 
                print printJobPages.PageNo; 
        reportViewer = new reportViewer(printJobHeader); 
        reportViewer.showPage(1); 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                          | 説明                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public boolean setNumberOfPages(int pageNo, \[boolean updataProgressForm\])                                     |                                                 |
| public void nextPage()                                                                                          |                                                 |
| public void lastPage()                                                                                          |                                                 |
| public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\], \[container packedPrintJobSettings\]) | Object クラスの新しいインスタンスを初期化します。 |
| public void gotoPage(int pageNo)                                                                                |                                                 |
| public void pause()                                                                                             |                                                 |
| public void showPage(int pageNo)                                                                                |                                                 |
| public void firstPage()                                                                                         |                                                 |
| public void setAborted()                                                                                        |                                                 |
| public void close()                                                                                             |                                                 |
| public void prevPage()                                                                                          |                                                 |
| public void setCompleted()                                                                                      |                                                 |

## <a name="method-setnumberofpages"></a>メソッド setNumberOfPages

```xpp
public boolean setNumberOfPages(int pageNo, [boolean updataProgressForm])
```

### <a name="parameters---setnumberofpages"></a>パラメーター - setNumberOfPages

pageNo  

<!-- -->

updataProgressForm  

### <a name="return-value---setnumberofpages"></a>戻り値 - setNumberOfPages

## <a name="method-nextpage"></a>メソッド nextPage

```xpp
public void nextPage()
```

## <a name="method-lastpage"></a>メソッド lastPage

```xpp
public void lastPage()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(PrintJobHeader jobsCursor, [PrintJobPages pagesCursor], [container packedPrintJobSettings])
```

### <a name="parameters---new"></a>パラメーター - new

jobsCursor  

<!-- -->

pagesCursor  

<!-- -->

packedPrintJobSettings  

## <a name="method-gotopage"></a>メソッド gotoPage

```xpp
public void gotoPage(int pageNo)
```

### <a name="parameters---gotopage"></a>パラメーター - gotoPage

pageNo  

## <a name="method-pause"></a>メソッド pause

```xpp
public void pause()
```

## <a name="method-showpage"></a>メソッド showPage

```xpp
public void showPage(int pageNo)
```

### <a name="parameters---showpage"></a>パラメーター - showPage

pageNo  

## <a name="method-firstpage"></a>メソッド firstPage

```xpp
public void firstPage()
```

## <a name="method-setaborted"></a>メソッド setAborted

```xpp
public void setAborted()
```

## <a name="method-close"></a>メソッド close

```xpp
public void close()
```

## <a name="method-prevpage"></a>メソッド prevPage

```xpp
public void prevPage()
```

## <a name="method-setcompleted"></a>メソッド setCompleted

```xpp
public void setCompleted()
```

