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
# <a name="class-reportoutput"></a><span data-ttu-id="2f512-103">クラス ReportOutput</span><span class="sxs-lookup"><span data-stu-id="2f512-103">Class ReportOutput</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportOutput extends Object
```

<span data-ttu-id="2f512-104">ReportOutput クラスは、プリンターやファイルへのレポートの出力を処理します。</span><span class="sxs-lookup"><span data-stu-id="2f512-104">The ReportOutput class handles the output of a report to a printer or file.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f512-105">備考</span><span class="sxs-lookup"><span data-stu-id="2f512-105">Remarks</span></span>

<span data-ttu-id="2f512-106">このクラスは、レポートのプレビューを処理する ReportViewer クラス、およびユーザー定義のターゲットへのレポートの出力をユーザー定義の形式で処理する ReportOutputUser クラスの基本クラスとして機能します。</span><span class="sxs-lookup"><span data-stu-id="2f512-106">This class serves as the base class for the ReportViewer class, which handles preview of reports, and for the ReportOutputUser class, which handles output of reports to a user-defined target in a user-defined format.</span></span> <span data-ttu-id="2f512-107">一般に、プリンターにレポートを印刷する場合、印刷メソッドは ReportOutput オブジェクトを作成し、その印刷メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2f512-107">In general, if a report is printed to the printer, the print method creates a ReportOutput object and calls its print method.</span></span> <span data-ttu-id="2f512-108">printJobSettings::outputToClient(TRUE) への呼び出しが行われている場合は、ReportViewer オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2f512-108">If the call printJobSettings::outputToClient(TRUE) has been made, a ReportViewer object is created instead.</span></span> <span data-ttu-id="2f512-109">ReportViewer オブジェクトはサーバー上ではなくクライアント上にしか存在しないため、印刷メソッドを呼び出すと、クライアントに設定されているプリンタでレポートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="2f512-109">The call to the print method prints the report on a printer that is set up on the client, because a ReportViewer object can only exist on the client, not on the server.</span></span>

## <a name="examples"></a><span data-ttu-id="2f512-110">例</span><span class="sxs-lookup"><span data-stu-id="2f512-110">Examples</span></span>

<span data-ttu-id="2f512-111">次の例では、現在の日付に printArchive テーブルに挿入されたジョブのジョブの説明とページ番号を出力し、既定のプリンタに 1 ページを出力します。</span><span class="sxs-lookup"><span data-stu-id="2f512-111">The following example prints the job descriptions and page numbers of jobs that have been inserted into the printArchive table on the current date, and prints page 1 on the default printer.</span></span>

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

## <a name="methods"></a><span data-ttu-id="2f512-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="2f512-112">Methods</span></span>

| <span data-ttu-id="2f512-113">方法</span><span class="sxs-lookup"><span data-stu-id="2f512-113">Method</span></span>                                                                    | <span data-ttu-id="2f512-114">説明</span><span class="sxs-lookup"><span data-stu-id="2f512-114">Description</span></span>                                     |
|---------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="2f512-115">public str description(\[str description\])</span><span class="sxs-lookup"><span data-stu-id="2f512-115">public str description(\[str description\])</span></span>                               |                                                 |
| <span data-ttu-id="2f512-116">public int getCopyNo()</span><span class="sxs-lookup"><span data-stu-id="2f512-116">public int getCopyNo()</span></span>                                                    |                                                 |
| <span data-ttu-id="2f512-117">public boolean getDeclineOverwrite()</span><span class="sxs-lookup"><span data-stu-id="2f512-117">public boolean getDeclineOverwrite()</span></span>                                      |                                                 |
| <span data-ttu-id="2f512-118">public int getLastCopyNo()</span><span class="sxs-lookup"><span data-stu-id="2f512-118">public int getLastCopyNo()</span></span>                                                |                                                 |
| <span data-ttu-id="2f512-119">public int getLastPageNo()</span><span class="sxs-lookup"><span data-stu-id="2f512-119">public int getLastPageNo()</span></span>                                                |                                                 |
| <span data-ttu-id="2f512-120">public int getPageNo()</span><span class="sxs-lookup"><span data-stu-id="2f512-120">public int getPageNo()</span></span>                                                    |                                                 |
| <span data-ttu-id="2f512-121">public str getTempFileName(str prefix)</span><span class="sxs-lookup"><span data-stu-id="2f512-121">public str getTempFileName(str prefix)</span></span>                                    |                                                 |
| <span data-ttu-id="2f512-122">public PrintJobStatus jobStatus()</span><span class="sxs-lookup"><span data-stu-id="2f512-122">public PrintJobStatus jobStatus()</span></span>                                         |                                                 |
| <span data-ttu-id="2f512-123">public PrintJobSettings printJobSettings()</span><span class="sxs-lookup"><span data-stu-id="2f512-123">public PrintJobSettings printJobSettings()</span></span>                                |                                                 |
| <span data-ttu-id="2f512-124">public boolean setNumberOfPages(int pageNo)</span><span class="sxs-lookup"><span data-stu-id="2f512-124">public boolean setNumberOfPages(int pageNo)</span></span>                               |                                                 |
| <span data-ttu-id="2f512-125">public str type(\[str type\])</span><span class="sxs-lookup"><span data-stu-id="2f512-125">public str type(\[str type\])</span></span>                                             |                                                 |
| <span data-ttu-id="2f512-126">public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\])</span><span class="sxs-lookup"><span data-stu-id="2f512-126">public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\])</span></span> | <span data-ttu-id="2f512-127">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2f512-127">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="2f512-128">public void printAscii(str filename)</span><span class="sxs-lookup"><span data-stu-id="2f512-128">public void printAscii(str filename)</span></span>                                      |                                                 |
| <span data-ttu-id="2f512-129">public void printTextUTF8(str filename)</span><span class="sxs-lookup"><span data-stu-id="2f512-129">public void printTextUTF8(str filename)</span></span>                                   | <span data-ttu-id="2f512-130">レポートを UTF-8 形式で印刷します。</span><span class="sxs-lookup"><span data-stu-id="2f512-130">Prints a report to a UTF-8 format.</span></span>              |
| <span data-ttu-id="2f512-131">public void printRTF(str filename)</span><span class="sxs-lookup"><span data-stu-id="2f512-131">public void printRTF(str filename)</span></span>                                        |                                                 |
| <span data-ttu-id="2f512-132">public void print()</span><span class="sxs-lookup"><span data-stu-id="2f512-132">public void print()</span></span>                                                       |                                                 |
| <span data-ttu-id="2f512-133">public void printPDF(str filename, \[boolean embedFonts\])</span><span class="sxs-lookup"><span data-stu-id="2f512-133">public void printPDF(str filename, \[boolean embedFonts\])</span></span>                |                                                 |
| <span data-ttu-id="2f512-134">public void printHTML(str filename)</span><span class="sxs-lookup"><span data-stu-id="2f512-134">public void printHTML(str filename)</span></span>                                       |                                                 |
| <span data-ttu-id="2f512-135">public void abort()</span><span class="sxs-lookup"><span data-stu-id="2f512-135">public void abort()</span></span>                                                       |                                                 |
| <span data-ttu-id="2f512-136">public void dialogAndPrint()</span><span class="sxs-lookup"><span data-stu-id="2f512-136">public void dialogAndPrint()</span></span>                                              |                                                 |
| <span data-ttu-id="2f512-137">public void printToTarget()</span><span class="sxs-lookup"><span data-stu-id="2f512-137">public void printToTarget()</span></span>                                               |                                                 |

## <a name="method-description"></a><span data-ttu-id="2f512-138">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="2f512-138">Method description</span></span>

```xpp
public str description([str description])
```

### <a name="parameters---description"></a><span data-ttu-id="2f512-139">パラメーター - description</span><span class="sxs-lookup"><span data-stu-id="2f512-139">Parameters - description</span></span>

<span data-ttu-id="2f512-140">説明</span><span class="sxs-lookup"><span data-stu-id="2f512-140">description</span></span>  

### <a name="return-value---description"></a><span data-ttu-id="2f512-141">戻り値 - description</span><span class="sxs-lookup"><span data-stu-id="2f512-141">Return Value - description</span></span>

## <a name="method-getcopyno"></a><span data-ttu-id="2f512-142">メソッド getCopyNo</span><span class="sxs-lookup"><span data-stu-id="2f512-142">Method getCopyNo</span></span>

```xpp
public int getCopyNo()
```

### <a name="return-value---getcopyno"></a><span data-ttu-id="2f512-143">戻り値 - getCopyNo</span><span class="sxs-lookup"><span data-stu-id="2f512-143">Return Value - getCopyNo</span></span>

## <a name="method-getdeclineoverwrite"></a><span data-ttu-id="2f512-144">メソッド getDeclineOverwrite</span><span class="sxs-lookup"><span data-stu-id="2f512-144">Method getDeclineOverwrite</span></span>

```xpp
public boolean getDeclineOverwrite()
```

### <a name="return-value---getdeclineoverwrite"></a><span data-ttu-id="2f512-145">戻り値 - getDeclineOverwrite</span><span class="sxs-lookup"><span data-stu-id="2f512-145">Return Value - getDeclineOverwrite</span></span>

## <a name="method-getlastcopyno"></a><span data-ttu-id="2f512-146">メソッド getLastCopyNo</span><span class="sxs-lookup"><span data-stu-id="2f512-146">Method getLastCopyNo</span></span>

```xpp
public int getLastCopyNo()
```

### <a name="return-value---getlastcopyno"></a><span data-ttu-id="2f512-147">戻り値 - getLastCopyNo</span><span class="sxs-lookup"><span data-stu-id="2f512-147">Return Value - getLastCopyNo</span></span>

## <a name="method-getlastpageno"></a><span data-ttu-id="2f512-148">メソッド getLastPageNo</span><span class="sxs-lookup"><span data-stu-id="2f512-148">Method getLastPageNo</span></span>

```xpp
public int getLastPageNo()
```

### <a name="return-value---getlastpageno"></a><span data-ttu-id="2f512-149">戻り値 - getLastPageNo</span><span class="sxs-lookup"><span data-stu-id="2f512-149">Return Value - getLastPageNo</span></span>

## <a name="method-getpageno"></a><span data-ttu-id="2f512-150">メソッド getPageNo</span><span class="sxs-lookup"><span data-stu-id="2f512-150">Method getPageNo</span></span>

```xpp
public int getPageNo()
```

### <a name="return-value---getpageno"></a><span data-ttu-id="2f512-151">戻り値 - getPageNo</span><span class="sxs-lookup"><span data-stu-id="2f512-151">Return Value - getPageNo</span></span>

## <a name="method-gettempfilename"></a><span data-ttu-id="2f512-152">メソッド getTempFileName</span><span class="sxs-lookup"><span data-stu-id="2f512-152">Method getTempFileName</span></span>

```xpp
public str getTempFileName(str prefix)
```

### <a name="parameters---gettempfilename"></a><span data-ttu-id="2f512-153">パラメーター - getTempFileName</span><span class="sxs-lookup"><span data-stu-id="2f512-153">Parameters - getTempFileName</span></span>

<span data-ttu-id="2f512-154">prefix</span><span class="sxs-lookup"><span data-stu-id="2f512-154">prefix</span></span>  

### <a name="return-value---gettempfilename"></a><span data-ttu-id="2f512-155">戻り値 - getTempFileName</span><span class="sxs-lookup"><span data-stu-id="2f512-155">Return Value - getTempFileName</span></span>

## <a name="method-jobstatus"></a><span data-ttu-id="2f512-156">メソッド jobStatus</span><span class="sxs-lookup"><span data-stu-id="2f512-156">Method jobStatus</span></span>

```xpp
public PrintJobStatus jobStatus()
```

### <a name="return-value---jobstatus"></a><span data-ttu-id="2f512-157">戻り値 - jobStatus</span><span class="sxs-lookup"><span data-stu-id="2f512-157">Return Value - jobStatus</span></span>

## <a name="method-printjobsettings"></a><span data-ttu-id="2f512-158">メソッド printJobSettings</span><span class="sxs-lookup"><span data-stu-id="2f512-158">Method printJobSettings</span></span>

```xpp
public PrintJobSettings printJobSettings()
```

### <a name="return-value---printjobsettings"></a><span data-ttu-id="2f512-159">戻り値 - printJobSettings</span><span class="sxs-lookup"><span data-stu-id="2f512-159">Return Value - printJobSettings</span></span>

## <a name="method-setnumberofpages"></a><span data-ttu-id="2f512-160">メソッド setNumberOfPages</span><span class="sxs-lookup"><span data-stu-id="2f512-160">Method setNumberOfPages</span></span>

```xpp
public boolean setNumberOfPages(int pageNo)
```

### <a name="parameters---setnumberofpages"></a><span data-ttu-id="2f512-161">パラメーター - setNumberOfPages</span><span class="sxs-lookup"><span data-stu-id="2f512-161">Parameters - setNumberOfPages</span></span>

<span data-ttu-id="2f512-162">pageNo</span><span class="sxs-lookup"><span data-stu-id="2f512-162">pageNo</span></span>  

### <a name="return-value---setnumberofpages"></a><span data-ttu-id="2f512-163">戻り値 - setNumberOfPages</span><span class="sxs-lookup"><span data-stu-id="2f512-163">Return Value - setNumberOfPages</span></span>

## <a name="method-type"></a><span data-ttu-id="2f512-164">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="2f512-164">Method type</span></span>

```xpp
public str type([str type])
```

### <a name="parameters---type"></a><span data-ttu-id="2f512-165">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="2f512-165">Parameters - type</span></span>

<span data-ttu-id="2f512-166">タイプ</span><span class="sxs-lookup"><span data-stu-id="2f512-166">type</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="2f512-167">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="2f512-167">Return Value - type</span></span>

## <a name="method-new"></a><span data-ttu-id="2f512-168">メソッド new</span><span class="sxs-lookup"><span data-stu-id="2f512-168">Method new</span></span>

<span data-ttu-id="2f512-169">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2f512-169">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(PrintJobHeader jobsCursor, [PrintJobPages pagesCursor])
```

### <a name="parameters---new"></a><span data-ttu-id="2f512-170">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="2f512-170">Parameters - new</span></span>

<span data-ttu-id="2f512-171">jobsCursor</span><span class="sxs-lookup"><span data-stu-id="2f512-171">jobsCursor</span></span>  

<!-- -->

<span data-ttu-id="2f512-172">pagesCursor</span><span class="sxs-lookup"><span data-stu-id="2f512-172">pagesCursor</span></span>  

## <a name="method-printascii"></a><span data-ttu-id="2f512-173">メソッド printAscii</span><span class="sxs-lookup"><span data-stu-id="2f512-173">Method printAscii</span></span>

```xpp
public void printAscii(str filename)
```

### <a name="parameters---printascii"></a><span data-ttu-id="2f512-174">パラメーター - printAscii</span><span class="sxs-lookup"><span data-stu-id="2f512-174">Parameters - printAscii</span></span>

<span data-ttu-id="2f512-175">filename</span><span class="sxs-lookup"><span data-stu-id="2f512-175">filename</span></span>  

## <a name="method-printtextutf8"></a><span data-ttu-id="2f512-176">メソッド printTextUTF8</span><span class="sxs-lookup"><span data-stu-id="2f512-176">Method printTextUTF8</span></span>

<span data-ttu-id="2f512-177">レポートを UTF-8 形式で印刷します。</span><span class="sxs-lookup"><span data-stu-id="2f512-177">Prints a report to a UTF-8 format.</span></span>

```xpp
public void printTextUTF8(str filename)
```

### <a name="parameters---printtextutf8"></a><span data-ttu-id="2f512-178">パラメーター - printTextUTF8</span><span class="sxs-lookup"><span data-stu-id="2f512-178">Parameters - printTextUTF8</span></span>

<span data-ttu-id="2f512-179">filename</span><span class="sxs-lookup"><span data-stu-id="2f512-179">filename</span></span>  
<span data-ttu-id="2f512-180">レポートを印刷するファイルの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="2f512-180">A string that specifies the name of the file that the report is printed to.</span></span>

### <a name="remarks---printtextutf8"></a><span data-ttu-id="2f512-181">備考 - printTextUTF8</span><span class="sxs-lookup"><span data-stu-id="2f512-181">Remarks - printTextUTF8</span></span>

<span data-ttu-id="2f512-182">UTF-8 は、1 つの文字列にシングルバイト文字とマルチバイト文字の両方を使用できる文字エンコード方法です。</span><span class="sxs-lookup"><span data-stu-id="2f512-182">UTF-8 is a method of character encoding that allows for both single and multibyte characters in one string.</span></span>

### <a name="examples---printtextutf8"></a><span data-ttu-id="2f512-183">例 - printTextUTF8</span><span class="sxs-lookup"><span data-stu-id="2f512-183">Examples - printTextUTF8</span></span>

<span data-ttu-id="2f512-184">次の例は、printTextUTF8 メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="2f512-184">The following example shows a call to the printTextUTF8 method.</span></span>

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

## <a name="method-printrtf"></a><span data-ttu-id="2f512-185">メソッド printRTF</span><span class="sxs-lookup"><span data-stu-id="2f512-185">Method printRTF</span></span>

```xpp
public void printRTF(str filename)
```

### <a name="parameters---printrtf"></a><span data-ttu-id="2f512-186">パラメーター - printRTF</span><span class="sxs-lookup"><span data-stu-id="2f512-186">Parameters - printRTF</span></span>

<span data-ttu-id="2f512-187">filename</span><span class="sxs-lookup"><span data-stu-id="2f512-187">filename</span></span>  

## <a name="method-print"></a><span data-ttu-id="2f512-188">メソッド print</span><span class="sxs-lookup"><span data-stu-id="2f512-188">Method print</span></span>

```xpp
public void print()
```

## <a name="method-printpdf"></a><span data-ttu-id="2f512-189">メソッド printPDF</span><span class="sxs-lookup"><span data-stu-id="2f512-189">Method printPDF</span></span>

```xpp
public void printPDF(str filename, [boolean embedFonts])
```

### <a name="parameters---printpdf"></a><span data-ttu-id="2f512-190">パラメーター - printPDF</span><span class="sxs-lookup"><span data-stu-id="2f512-190">Parameters - printPDF</span></span>

<span data-ttu-id="2f512-191">filename</span><span class="sxs-lookup"><span data-stu-id="2f512-191">filename</span></span>  

<!-- -->

<span data-ttu-id="2f512-192">embedFonts</span><span class="sxs-lookup"><span data-stu-id="2f512-192">embedFonts</span></span>  

## <a name="method-printhtml"></a><span data-ttu-id="2f512-193">メソッド printHTML</span><span class="sxs-lookup"><span data-stu-id="2f512-193">Method printHTML</span></span>

```xpp
public void printHTML(str filename)
```

### <a name="parameters---printhtml"></a><span data-ttu-id="2f512-194">パラメーター - printHTML</span><span class="sxs-lookup"><span data-stu-id="2f512-194">Parameters - printHTML</span></span>

<span data-ttu-id="2f512-195">filename</span><span class="sxs-lookup"><span data-stu-id="2f512-195">filename</span></span>  

## <a name="method-abort"></a><span data-ttu-id="2f512-196">メソッド abort</span><span class="sxs-lookup"><span data-stu-id="2f512-196">Method abort</span></span>

```xpp
public void abort()
```

## <a name="method-dialogandprint"></a><span data-ttu-id="2f512-197">メソッド dialogAndPrint</span><span class="sxs-lookup"><span data-stu-id="2f512-197">Method dialogAndPrint</span></span>

```xpp
public void dialogAndPrint()
```

## <a name="method-printtotarget"></a><span data-ttu-id="2f512-198">メソッド printToTarget</span><span class="sxs-lookup"><span data-stu-id="2f512-198">Method printToTarget</span></span>

```xpp
public void printToTarget()
```

