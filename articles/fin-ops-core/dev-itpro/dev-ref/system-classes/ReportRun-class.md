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
# <a name="class-reportrun"></a><span data-ttu-id="a6252-103">クラス ReportRun</span><span class="sxs-lookup"><span data-stu-id="a6252-103">Class ReportRun</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportRun extends ObjectRun
```

<span data-ttu-id="a6252-104">ReportRun クラスはレポートを生成および印刷するか、画面上のレポートをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="a6252-104">The ReportRun class generates and prints a report or previews a report on the screen.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6252-105">備考</span><span class="sxs-lookup"><span data-stu-id="a6252-105">Remarks</span></span>

<span data-ttu-id="a6252-106">レポートの構造を定義するのとは対照的に、ReportRun オブジェクトにはレポートのランタイム特性が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a6252-106">As opposed to the , which defines the structure of a report, a ReportRun object contains the runtime characteristics of the report.</span></span> <span data-ttu-id="a6252-107">ReportRun オブジェクトは、次の引数のいずれかを使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6252-107">A ReportRun object can be created by using one of the following arguments:</span></span>

-   <span data-ttu-id="a6252-108">Args オブジェクトは名前およびオプションの designName パラメータが指定しています。</span><span class="sxs-lookup"><span data-stu-id="a6252-108">An Args object where the name and optionally designName parameters are specified.</span></span>
-   <span data-ttu-id="a6252-109">例えで使用される、作成されたコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="a6252-109">A created container, by using the for example.</span></span>
-   <span data-ttu-id="a6252-110">レポート名とオプションのデザイン名。</span><span class="sxs-lookup"><span data-stu-id="a6252-110">The report name and an optional design name.</span></span>

<span data-ttu-id="a6252-111">セクション テンプレート ノード タイプを使用すると、セクションを一度定義して、さまざまなレポートで何度も再利用できます。</span><span class="sxs-lookup"><span data-stu-id="a6252-111">The section template node type allows the sections to be defined once and reuse them many times in different reports.</span></span> <span data-ttu-id="a6252-112">この一般的な例は、小切手または振替になります。</span><span class="sxs-lookup"><span data-stu-id="a6252-112">A typical example of this would be a check or a giro.</span></span>

## <a name="examples"></a><span data-ttu-id="a6252-113">例</span><span class="sxs-lookup"><span data-stu-id="a6252-113">Examples</span></span>

<span data-ttu-id="a6252-114">次の例では、既存の Cust レポートの Customer デザインを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-114">The following example runs the Customer design of the existing Cust report:</span></span>

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

## <a name="methods"></a><span data-ttu-id="a6252-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="a6252-115">Methods</span></span>

| <span data-ttu-id="a6252-116">方法</span><span class="sxs-lookup"><span data-stu-id="a6252-116">Method</span></span>                                                                                                                                                    | <span data-ttu-id="a6252-117">説明</span><span class="sxs-lookup"><span data-stu-id="a6252-117">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6252-118">public boolean allPages(\[boolean all\])</span><span class="sxs-lookup"><span data-stu-id="a6252-118">public boolean allPages(\[boolean all\])</span></span>                                                                                                                  |                                                                                                                                                   |
| <span data-ttu-id="a6252-119">public boolean callMenuFunction(xMenuFunction menuFunction)</span><span class="sxs-lookup"><span data-stu-id="a6252-119">public boolean callMenuFunction(xMenuFunction menuFunction)</span></span>                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-120">public str caption(str reportSpelling, str reportName, str designCaption, str designName)</span><span class="sxs-lookup"><span data-stu-id="a6252-120">public str caption(str reportSpelling, str reportName, str designCaption, str designName)</span></span>                                                                 | <span data-ttu-id="a6252-121">レポートをプレビューするときにキャプションを作成し、レポートを印刷するときにドキュメント名を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6252-121">Creates a caption when previewing a report, or a document name when printing a report.</span></span>                                                            |
| <span data-ttu-id="a6252-122">public boolean collate(\[boolean collate\])</span><span class="sxs-lookup"><span data-stu-id="a6252-122">public boolean collate(\[boolean collate\])</span></span>                                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-123">public TableId columnHeadings(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="a6252-123">public TableId columnHeadings(\[TableId tableId\])</span></span>                                                                                                        | <span data-ttu-id="a6252-124">レポートの列見出しのコントロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="a6252-124">Provides control of column headings in a report.</span></span>                                                                                                  |
| <span data-ttu-id="a6252-125">public ReportControl control()</span><span class="sxs-lookup"><span data-stu-id="a6252-125">public ReportControl control()</span></span>                                                                                                                            | <span data-ttu-id="a6252-126">実行されているコントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="a6252-126">Retrieves the control that is being executed.</span></span>                                                                                                     |
| <span data-ttu-id="a6252-127">public int copies(\[int numberOfCopies\])</span><span class="sxs-lookup"><span data-stu-id="a6252-127">public int copies(\[int numberOfCopies\])</span></span>                                                                                                                 |                                                                                                                                                   |
| <span data-ttu-id="a6252-128">public int copiesTotal()</span><span class="sxs-lookup"><span data-stu-id="a6252-128">public int copiesTotal()</span></span>                                                                                                                                  | <span data-ttu-id="a6252-129">レポートのマーキング コピーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a6252-129">Enables marking copies of reports.</span></span>                                                                                                                |
| <span data-ttu-id="a6252-130">public int copy()</span><span class="sxs-lookup"><span data-stu-id="a6252-130">public int copy()</span></span>                                                                                                                                         | <span data-ttu-id="a6252-131">レポートのコピーの数を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-131">Returns the number of the copy of a report.</span></span>                                                                                                       |
| <span data-ttu-id="a6252-132">public str copyDescription()</span><span class="sxs-lookup"><span data-stu-id="a6252-132">public str copyDescription()</span></span>                                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-133">public xFormRun createProgressForm()</span><span class="sxs-lookup"><span data-stu-id="a6252-133">public xFormRun createProgressForm()</span></span>                                                                                                                      | <span data-ttu-id="a6252-134">進捗情報を含むフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6252-134">Creates the form that contains progress information.</span></span>                                                                                              |
| <span data-ttu-id="a6252-135">public int currentYmm100()</span><span class="sxs-lookup"><span data-stu-id="a6252-135">public int currentYmm100()</span></span>                                                                                                                                |                                                                                                                                                   |
| <span data-ttu-id="a6252-136">public ReportDesign design(\[AnyType nameOrReportDesign\])</span><span class="sxs-lookup"><span data-stu-id="a6252-136">public ReportDesign design(\[AnyType nameOrReportDesign\])</span></span>                                                                                                | <span data-ttu-id="a6252-137">デザインの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a6252-137">Gets or sets the name of the design.</span></span>                                                                                                              |
| <span data-ttu-id="a6252-138">public str deviceName(\[str device\])</span><span class="sxs-lookup"><span data-stu-id="a6252-138">public str deviceName(\[str device\])</span></span>                                                                                                                     |                                                                                                                                                   |
| <span data-ttu-id="a6252-139">public Object dialog(Object dialog)</span><span class="sxs-lookup"><span data-stu-id="a6252-139">public Object dialog(Object dialog)</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-140">public str driverName()</span><span class="sxs-lookup"><span data-stu-id="a6252-140">public str driverName()</span></span>                                                                                                                                   | <span data-ttu-id="a6252-141">プリンター ドライバー名を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-141">Returns the printer driver name.</span></span>                                                                                                                  |
| <span data-ttu-id="a6252-142">public boolean enableAllBodies(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="a6252-142">public boolean enableAllBodies(\[boolean enable\])</span></span>                                                                                                        |                                                                                                                                                   |
| <span data-ttu-id="a6252-143">public boolean execute(int number)</span><span class="sxs-lookup"><span data-stu-id="a6252-143">public boolean execute(int number)</span></span>                                                                                                                        | <span data-ttu-id="a6252-144">レポートのプログラム可能なセクションを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-144">Prints the programmable sections of a report.</span></span>                                                                                                     |
| <span data-ttu-id="a6252-145">public boolean executeBodyColumnHeadings(TableId tableId, \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="a6252-145">public boolean executeBodyColumnHeadings(TableId tableId, \[FieldId fieldId\])</span></span>                                                                            | <span data-ttu-id="a6252-146">レポートの本文セクションの列ヘッダーを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-146">Prints the column headings of a body section in a report.</span></span>                                                                                         |
| <span data-ttu-id="a6252-147">public boolean executeColumnHeadings(ReportSection section)</span><span class="sxs-lookup"><span data-stu-id="a6252-147">public boolean executeColumnHeadings(ReportSection section)</span></span>                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-148">public boolean executeControlColumnHeadings(int number)</span><span class="sxs-lookup"><span data-stu-id="a6252-148">public boolean executeControlColumnHeadings(int number)</span></span>                                                                                                   | <span data-ttu-id="a6252-149">プログラム可能なセクションの列のヘッダーを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-149">Executes the column headings of a programmable section.</span></span>                                                                                           |
| <span data-ttu-id="a6252-150">public boolean executeFooter(\[TableId tableId\], \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="a6252-150">public boolean executeFooter(\[TableId tableId\], \[FieldId fieldId\])</span></span>                                                                                    | <span data-ttu-id="a6252-151">フッター セクションを実行を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-151">Execute a footer section.</span></span>                                                                                                                         |
| <span data-ttu-id="a6252-152">public boolean executeHeader(\[TableId tableId\], \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="a6252-152">public boolean executeHeader(\[TableId tableId\], \[FieldId fieldId\])</span></span>                                                                                    | <span data-ttu-id="a6252-153">ヘッダー セクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-153">Executes a header section.</span></span>                                                                                                                        |
| <span data-ttu-id="a6252-154">public boolean executeSection(ReportSection section)</span><span class="sxs-lookup"><span data-stu-id="a6252-154">public boolean executeSection(ReportSection section)</span></span>                                                                                                      | <span data-ttu-id="a6252-155">レポートの指定されたセクションを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-155">Prints the specified section in the report.</span></span>                                                                                                       |
| <span data-ttu-id="a6252-156">public boolean fetch()</span><span class="sxs-lookup"><span data-stu-id="a6252-156">public boolean fetch()</span></span>                                                                                                                                    | <span data-ttu-id="a6252-157">レポート クエリを実行し、クエリによって検出されたレコードの送信メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6252-157">Executes the report query and calls the send method for the record that is found by the query.</span></span>                                                    |
| <span data-ttu-id="a6252-158">public int from(\[int fromPage\])</span><span class="sxs-lookup"><span data-stu-id="a6252-158">public int from(\[int fromPage\])</span></span>                                                                                                                         |                                                                                                                                                   |
| <span data-ttu-id="a6252-159">public int generateDesign(\[Query query\], \[int designNo\])</span><span class="sxs-lookup"><span data-stu-id="a6252-159">public int generateDesign(\[Query query\], \[int designNo\])</span></span>                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-160">public boolean getDeclineOverwrite()</span><span class="sxs-lookup"><span data-stu-id="a6252-160">public boolean getDeclineOverwrite()</span></span>                                                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-161">public int getNumberOfPrinters()</span><span class="sxs-lookup"><span data-stu-id="a6252-161">public int getNumberOfPrinters()</span></span>                                                                                                                          |                                                                                                                                                   |
| <span data-ttu-id="a6252-162">public str getPrinter(int number)</span><span class="sxs-lookup"><span data-stu-id="a6252-162">public str getPrinter(int number)</span></span>                                                                                                                         |                                                                                                                                                   |
| <span data-ttu-id="a6252-163">public str getRangeDescription(int number)</span><span class="sxs-lookup"><span data-stu-id="a6252-163">public str getRangeDescription(int number)</span></span>                                                                                                                |                                                                                                                                                   |
| <span data-ttu-id="a6252-164">public ReportViewer getReportViewer()</span><span class="sxs-lookup"><span data-stu-id="a6252-164">public ReportViewer getReportViewer()</span></span>                                                                                                                     |                                                                                                                                                   |
| <span data-ttu-id="a6252-165">public PrintMedium getTarget()</span><span class="sxs-lookup"><span data-stu-id="a6252-165">public PrintMedium getTarget()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-166">public boolean hasGeneratedDesign()</span><span class="sxs-lookup"><span data-stu-id="a6252-166">public boolean hasGeneratedDesign()</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-167">public str headerDescription()</span><span class="sxs-lookup"><span data-stu-id="a6252-167">public str headerDescription()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-168">public int heightOfPageFooters()</span><span class="sxs-lookup"><span data-stu-id="a6252-168">public int heightOfPageFooters()</span></span>                                                                                                                          |                                                                                                                                                   |
| <span data-ttu-id="a6252-169">public int indent()</span><span class="sxs-lookup"><span data-stu-id="a6252-169">public int indent()</span></span>                                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-170">public boolean isBodyEnabled(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="a6252-170">public boolean isBodyEnabled(TableId tableId)</span></span>                                                                                                             |                                                                                                                                                   |
| <span data-ttu-id="a6252-171">public Int64 jobId()</span><span class="sxs-lookup"><span data-stu-id="a6252-171">public Int64 jobId()</span></span>                                                                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-172">public Common last(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="a6252-172">public Common last(TableId tableId)</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-173">public int mm100Left()</span><span class="sxs-lookup"><span data-stu-id="a6252-173">public int mm100Left()</span></span>                                                                                                                                    |                                                                                                                                                   |
| <span data-ttu-id="a6252-174">public int mm100PageHeight()</span><span class="sxs-lookup"><span data-stu-id="a6252-174">public int mm100PageHeight()</span></span>                                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-175">public str name(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="a6252-175">public str name(\[str name\])</span></span>                                                                                                                             | <span data-ttu-id="a6252-176">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a6252-176">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>                         |
| <span data-ttu-id="a6252-177">public container pack()</span><span class="sxs-lookup"><span data-stu-id="a6252-177">public container pack()</span></span>                                                                                                                                   | <span data-ttu-id="a6252-178">ReportRun クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="a6252-178">Serializes the current instance of the ReportRun class.</span></span>                                                                                           |
| <span data-ttu-id="a6252-179">public container packDesign()</span><span class="sxs-lookup"><span data-stu-id="a6252-179">public container packDesign()</span></span>                                                                                                                             |                                                                                                                                                   |
| <span data-ttu-id="a6252-180">public container packPageSettings()</span><span class="sxs-lookup"><span data-stu-id="a6252-180">public container packPageSettings()</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-181">public container packPrinterSettings()</span><span class="sxs-lookup"><span data-stu-id="a6252-181">public container packPrinterSettings()</span></span>                                                                                                                    |                                                                                                                                                   |
| <span data-ttu-id="a6252-182">public container packPrintJobSettings()</span><span class="sxs-lookup"><span data-stu-id="a6252-182">public container packPrintJobSettings()</span></span>                                                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-183">public container packSubtotalSettings()</span><span class="sxs-lookup"><span data-stu-id="a6252-183">public container packSubtotalSettings()</span></span>                                                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-184">public int page(\[int number\])</span><span class="sxs-lookup"><span data-stu-id="a6252-184">public int page(\[int number\])</span></span>                                                                                                                           |                                                                                                                                                   |
| <span data-ttu-id="a6252-185">public boolean pageFormatting()</span><span class="sxs-lookup"><span data-stu-id="a6252-185">public boolean pageFormatting()</span></span>                                                                                                                           | <span data-ttu-id="a6252-186">プリンターのプリンター プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="a6252-186">Displays the printer properties of the printer.</span></span>                                                                                                   |
| <span data-ttu-id="a6252-187">public int pagesTotal()</span><span class="sxs-lookup"><span data-stu-id="a6252-187">public int pagesTotal()</span></span>                                                                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-188">public str passThrough(str str)</span><span class="sxs-lookup"><span data-stu-id="a6252-188">public str passThrough(str str)</span></span>                                                                                                                           |                                                                                                                                                   |
| <span data-ttu-id="a6252-189">public int pixelsLeft()</span><span class="sxs-lookup"><span data-stu-id="a6252-189">public int pixelsLeft()</span></span>                                                                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-190">public int print()</span><span class="sxs-lookup"><span data-stu-id="a6252-190">public int print()</span></span>                                                                                                                                        | <span data-ttu-id="a6252-191">生成されたレポートを、プリンターや画面などの出力メディアに送信します。</span><span class="sxs-lookup"><span data-stu-id="a6252-191">Sends the generated report to a print medium, such as a printer or the screen.</span></span>                                                                    |
| <span data-ttu-id="a6252-192">public int printerAttributes()</span><span class="sxs-lookup"><span data-stu-id="a6252-192">public int printerAttributes()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-193">public int printerAveragePPM()</span><span class="sxs-lookup"><span data-stu-id="a6252-193">public int printerAveragePPM()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-194">public str printerComment()</span><span class="sxs-lookup"><span data-stu-id="a6252-194">public str printerComment()</span></span>                                                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-195">public str printerDatatype()</span><span class="sxs-lookup"><span data-stu-id="a6252-195">public str printerDatatype()</span></span>                                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-196">public int printerDefaultPriority()</span><span class="sxs-lookup"><span data-stu-id="a6252-196">public int printerDefaultPriority()</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-197">public str printerDriverName()</span><span class="sxs-lookup"><span data-stu-id="a6252-197">public str printerDriverName()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-198">public str printerFontInfo()</span><span class="sxs-lookup"><span data-stu-id="a6252-198">public str printerFontInfo()</span></span>                                                                                                                              | <span data-ttu-id="a6252-199">レポートの印刷に使用されるフォントを示します。</span><span class="sxs-lookup"><span data-stu-id="a6252-199">Indicates which font is used to print the report.</span></span>                                                                                                 |
| <span data-ttu-id="a6252-200">public str printerLocation()</span><span class="sxs-lookup"><span data-stu-id="a6252-200">public str printerLocation()</span></span>                                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-201">public int printerPageHeight()</span><span class="sxs-lookup"><span data-stu-id="a6252-201">public int printerPageHeight()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-202">public int printerPageWidth()</span><span class="sxs-lookup"><span data-stu-id="a6252-202">public int printerPageWidth()</span></span>                                                                                                                             |                                                                                                                                                   |
| <span data-ttu-id="a6252-203">public int printerPaper()</span><span class="sxs-lookup"><span data-stu-id="a6252-203">public int printerPaper()</span></span>                                                                                                                                 |                                                                                                                                                   |
| <span data-ttu-id="a6252-204">public str printerParameters()</span><span class="sxs-lookup"><span data-stu-id="a6252-204">public str printerParameters()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-205">public str printerPortName()</span><span class="sxs-lookup"><span data-stu-id="a6252-205">public str printerPortName()</span></span>                                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-206">public str printerPrinterName()</span><span class="sxs-lookup"><span data-stu-id="a6252-206">public str printerPrinterName()</span></span>                                                                                                                           |                                                                                                                                                   |
| <span data-ttu-id="a6252-207">public str printerPrintProcessor()</span><span class="sxs-lookup"><span data-stu-id="a6252-207">public str printerPrintProcessor()</span></span>                                                                                                                        |                                                                                                                                                   |
| <span data-ttu-id="a6252-208">public int printerPriority()</span><span class="sxs-lookup"><span data-stu-id="a6252-208">public int printerPriority()</span></span>                                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-209">public int printerQueuedJobs()</span><span class="sxs-lookup"><span data-stu-id="a6252-209">public int printerQueuedJobs()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-210">public str printerSepFile()</span><span class="sxs-lookup"><span data-stu-id="a6252-210">public str printerSepFile()</span></span>                                                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-211">public str printerServerName()</span><span class="sxs-lookup"><span data-stu-id="a6252-211">public str printerServerName()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-212">public boolean printerSettings(\[int showWhat\])</span><span class="sxs-lookup"><span data-stu-id="a6252-212">public boolean printerSettings(\[int showWhat\])</span></span>                                                                                                          | <span data-ttu-id="a6252-213">ユーザーがプリンターの設定を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a6252-213">Enables the user to select printer settings.</span></span>                                                                                                      |
| <span data-ttu-id="a6252-214">public str printerShareName()</span><span class="sxs-lookup"><span data-stu-id="a6252-214">public str printerShareName()</span></span>                                                                                                                             |                                                                                                                                                   |
| <span data-ttu-id="a6252-215">public TimeOfDay printerStartTime()</span><span class="sxs-lookup"><span data-stu-id="a6252-215">public TimeOfDay printerStartTime()</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-216">public int printerStatus()</span><span class="sxs-lookup"><span data-stu-id="a6252-216">public int printerStatus()</span></span>                                                                                                                                |                                                                                                                                                   |
| <span data-ttu-id="a6252-217">public TimeOfDay printerUntilTime()</span><span class="sxs-lookup"><span data-stu-id="a6252-217">public TimeOfDay printerUntilTime()</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-218">public PrintJobSettings printJobSettings(\[container packedPrintJobSettings\])</span><span class="sxs-lookup"><span data-stu-id="a6252-218">public PrintJobSettings printJobSettings(\[container packedPrintJobSettings\])</span></span>                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-219">public int printSum()</span><span class="sxs-lookup"><span data-stu-id="a6252-219">public int printSum()</span></span>                                                                                                                                     |                                                                                                                                                   |
| <span data-ttu-id="a6252-220">public xFormRun progressForm(\[xFormRun form\])</span><span class="sxs-lookup"><span data-stu-id="a6252-220">public xFormRun progressForm(\[xFormRun form\])</span></span>                                                                                                           |                                                                                                                                                   |
| <span data-ttu-id="a6252-221">public str progressInfo(int pageNo, int lineNo)</span><span class="sxs-lookup"><span data-stu-id="a6252-221">public str progressInfo(int pageNo, int lineNo)</span></span>                                                                                                           | <span data-ttu-id="a6252-222">セクションが実行されるたびに、レポートが実行中に生成されるレポートの量を記述する文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6252-222">Creates a string that describes how much of the report has been generated during the execution of a report every time that a section is executed.</span></span> |
| <span data-ttu-id="a6252-223">public boolean prompt(\[boolean enableCopy\], \[boolean enablePages\], \[boolean enableDevice\], \[boolean enableProperties\], \[boolean enablePrintTo\])</span><span class="sxs-lookup"><span data-stu-id="a6252-223">public boolean prompt(\[boolean enableCopy\], \[boolean enablePages\], \[boolean enableDevice\], \[boolean enableProperties\], \[boolean enablePrintTo\])</span></span> | <span data-ttu-id="a6252-224">レポートの実行をユーザーに求めます。</span><span class="sxs-lookup"><span data-stu-id="a6252-224">Prompts the user a report is run.</span></span>                                                                                                                 |
| <span data-ttu-id="a6252-225">public Query query(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="a6252-225">public Query query(\[Query query\])</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-226">public QueryRun queryRun(\[QueryRun queryRun\])</span><span class="sxs-lookup"><span data-stu-id="a6252-226">public QueryRun queryRun(\[QueryRun queryRun\])</span></span>                                                                                                           |                                                                                                                                                   |
| <span data-ttu-id="a6252-227">public Report report()</span><span class="sxs-lookup"><span data-stu-id="a6252-227">public Report report()</span></span>                                                                                                                                    |                                                                                                                                                   |
| <span data-ttu-id="a6252-228">public str reportUser(\[str user\])</span><span class="sxs-lookup"><span data-stu-id="a6252-228">public str reportUser(\[str user\])</span></span>                                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-229">public int rulerCM()</span><span class="sxs-lookup"><span data-stu-id="a6252-229">public int rulerCM()</span></span>                                                                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-230">public int rulerINCH()</span><span class="sxs-lookup"><span data-stu-id="a6252-230">public int rulerINCH()</span></span>                                                                                                                                    |                                                                                                                                                   |
| <span data-ttu-id="a6252-231">public str screenFontInfo()</span><span class="sxs-lookup"><span data-stu-id="a6252-231">public str screenFontInfo()</span></span>                                                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-232">public ReportSection section()</span><span class="sxs-lookup"><span data-stu-id="a6252-232">public ReportSection section()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-233">public int sectionsLeft(ReportSection section)</span><span class="sxs-lookup"><span data-stu-id="a6252-233">public int sectionsLeft(ReportSection section)</span></span>                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-234">public boolean send(Common cursor, \[int level\], \[boolean triggerOffBody\], \[boolean newPageBeforeBody\])</span><span class="sxs-lookup"><span data-stu-id="a6252-234">public boolean send(Common cursor, \[int level\], \[boolean triggerOffBody\], \[boolean newPageBeforeBody\])</span></span>                                              | <span data-ttu-id="a6252-235">セクション グループに属する本文セクションをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="a6252-235">Triggers the body sections that belong to a section group.</span></span>                                                                                        |
| <span data-ttu-id="a6252-236">public PrintMedium setTarget(PrintMedium target)</span><span class="sxs-lookup"><span data-stu-id="a6252-236">public PrintMedium setTarget(PrintMedium target)</span></span>                                                                                                          |                                                                                                                                                   |
| <span data-ttu-id="a6252-237">public boolean showMenuFunction(xMenuFunction menuFunction)</span><span class="sxs-lookup"><span data-stu-id="a6252-237">public boolean showMenuFunction(xMenuFunction menuFunction)</span></span>                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-238">public boolean showMenuReference(WebMenu menuReference)</span><span class="sxs-lookup"><span data-stu-id="a6252-238">public boolean showMenuReference(WebMenu menuReference)</span></span>                                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-239">public str sortInfo(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="a6252-239">public str sortInfo(Common cursor)</span></span>                                                                                                                        |                                                                                                                                                   |
| <span data-ttu-id="a6252-240">public Date startDate()</span><span class="sxs-lookup"><span data-stu-id="a6252-240">public Date startDate()</span></span>                                                                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-241">public DateTime startDateTime()</span><span class="sxs-lookup"><span data-stu-id="a6252-241">public DateTime startDateTime()</span></span>                                                                                                                           |                                                                                                                                                   |
| <span data-ttu-id="a6252-242">public Date startMachineDate()</span><span class="sxs-lookup"><span data-stu-id="a6252-242">public Date startMachineDate()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-243">public TimeOfDay startTime()</span><span class="sxs-lookup"><span data-stu-id="a6252-243">public TimeOfDay startTime()</span></span>                                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-244">public Real sum(TableId tableId, FieldId fieldId, \[int indent\])</span><span class="sxs-lookup"><span data-stu-id="a6252-244">public Real sum(TableId tableId, FieldId fieldId, \[int indent\])</span></span>                                                                                         |                                                                                                                                                   |
| <span data-ttu-id="a6252-245">public Real sumControl(str fieldName, \[int indent\])</span><span class="sxs-lookup"><span data-stu-id="a6252-245">public Real sumControl(str fieldName, \[int indent\])</span></span>                                                                                                     |                                                                                                                                                   |
| <span data-ttu-id="a6252-246">public Real sumControlNeg(str fieldName, \[int indent\])</span><span class="sxs-lookup"><span data-stu-id="a6252-246">public Real sumControlNeg(str fieldName, \[int indent\])</span></span>                                                                                                  |                                                                                                                                                   |
| <span data-ttu-id="a6252-247">public Real sumControlPos(str fieldName, \[int indent\])</span><span class="sxs-lookup"><span data-stu-id="a6252-247">public Real sumControlPos(str fieldName, \[int indent\])</span></span>                                                                                                  |                                                                                                                                                   |
| <span data-ttu-id="a6252-248">public str sumDescription()</span><span class="sxs-lookup"><span data-stu-id="a6252-248">public str sumDescription()</span></span>                                                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-249">public Real sumNeg(TableId tableId, FieldId fieldId, \[int indent\])</span><span class="sxs-lookup"><span data-stu-id="a6252-249">public Real sumNeg(TableId tableId, FieldId fieldId, \[int indent\])</span></span>                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-250">public Real sumPos(TableId tableId, FieldId fieldId, \[int indent\])</span><span class="sxs-lookup"><span data-stu-id="a6252-250">public Real sumPos(TableId tableId, FieldId fieldId, \[int indent\])</span></span>                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-251">public boolean suppressReportIsEmptyMessage(\[boolean suppress\])</span><span class="sxs-lookup"><span data-stu-id="a6252-251">public boolean suppressReportIsEmptyMessage(\[boolean suppress\])</span></span>                                                                                         |                                                                                                                                                   |
| <span data-ttu-id="a6252-252">public str title(\[str title\])</span><span class="sxs-lookup"><span data-stu-id="a6252-252">public str title(\[str title\])</span></span>                                                                                                                           | <span data-ttu-id="a6252-253">印刷ジョブの説明を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a6252-253">Gets or sets the print job description.</span></span>                                                                                                           |
| <span data-ttu-id="a6252-254">public int to(\[int toPage\])</span><span class="sxs-lookup"><span data-stu-id="a6252-254">public int to(\[int toPage\])</span></span>                                                                                                                             |                                                                                                                                                   |
| <span data-ttu-id="a6252-255">public str toString()</span><span class="sxs-lookup"><span data-stu-id="a6252-255">public str toString()</span></span>                                                                                                                                     | <span data-ttu-id="a6252-256">クラスのテキストの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-256">Returns a textual description of the class.</span></span>                                                                                                       |
| <span data-ttu-id="a6252-257">public boolean unpackPageSettings(container packedPageSetup)</span><span class="sxs-lookup"><span data-stu-id="a6252-257">public boolean unpackPageSettings(container packedPageSetup)</span></span>                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-258">public boolean unpackPrinterSettings(container packedPrinterSetup)</span><span class="sxs-lookup"><span data-stu-id="a6252-258">public boolean unpackPrinterSettings(container packedPrinterSetup)</span></span>                                                                                        |                                                                                                                                                   |
| <span data-ttu-id="a6252-259">public boolean unpackPrintJobSettings(container packedPrintJobSettings)</span><span class="sxs-lookup"><span data-stu-id="a6252-259">public boolean unpackPrintJobSettings(container packedPrintJobSettings)</span></span>                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-260">public boolean unpackSubtotalSettings(container packedSubtotalSetup)</span><span class="sxs-lookup"><span data-stu-id="a6252-260">public boolean unpackSubtotalSettings(container packedSubtotalSetup)</span></span>                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-261">public PrinterOrientation userSelectedOrientation()</span><span class="sxs-lookup"><span data-stu-id="a6252-261">public PrinterOrientation userSelectedOrientation()</span></span>                                                                                                       |                                                                                                                                                   |
| <span data-ttu-id="a6252-262">public void disableBody(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="a6252-262">public void disableBody(\[TableId tableId\])</span></span>                                                                                                              |                                                                                                                                                   |
| <span data-ttu-id="a6252-263">public void attach()</span><span class="sxs-lookup"><span data-stu-id="a6252-263">public void attach()</span></span>                                                                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-264">public void new(AnyType argsOrReportOrContainer, \[str designName\], \[boolean isWebReport\])</span><span class="sxs-lookup"><span data-stu-id="a6252-264">public void new(AnyType argsOrReportOrContainer, \[str designName\], \[boolean isWebReport\])</span></span>                                                             | <span data-ttu-id="a6252-265">ReportRun クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a6252-265">Initializes an instance of the ReportRun class.</span></span>                                                                                                   |
| <span data-ttu-id="a6252-266">public void disableSection(ReportSection section)</span><span class="sxs-lookup"><span data-stu-id="a6252-266">public void disableSection(ReportSection section)</span></span>                                                                                                         |                                                                                                                                                   |
| <span data-ttu-id="a6252-267">public void arrangeLevelGlobal()</span><span class="sxs-lookup"><span data-stu-id="a6252-267">public void arrangeLevelGlobal()</span></span>                                                                                                                          |                                                                                                                                                   |
| <span data-ttu-id="a6252-268">public void setEscapeSequence(str str)</span><span class="sxs-lookup"><span data-stu-id="a6252-268">public void setEscapeSequence(str str)</span></span>                                                                                                                    |                                                                                                                                                   |
| <span data-ttu-id="a6252-269">public void enableBody(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="a6252-269">public void enableBody(\[TableId tableId\])</span></span>                                                                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-270">public void clearAllRangeDescriptions()</span><span class="sxs-lookup"><span data-stu-id="a6252-270">public void clearAllRangeDescriptions()</span></span>                                                                                                                   |                                                                                                                                                   |
| <span data-ttu-id="a6252-271">public void header(ReportSection headerSection, TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="a6252-271">public void header(ReportSection headerSection, TableId tableId, FieldId fieldId)</span></span>                                                                         | <span data-ttu-id="a6252-272">ヘッダーを制御します。</span><span class="sxs-lookup"><span data-stu-id="a6252-272">Controls the header.</span></span>                                                                                                                              |
| <span data-ttu-id="a6252-273">public void unpackDesign(container packedDesign)</span><span class="sxs-lookup"><span data-stu-id="a6252-273">public void unpackDesign(container packedDesign)</span></span>                                                                                                          |                                                                                                                                                   |
| <span data-ttu-id="a6252-274">public void newPage(\[boolean doPageFooter\])</span><span class="sxs-lookup"><span data-stu-id="a6252-274">public void newPage(\[boolean doPageFooter\])</span></span>                                                                                                             |                                                                                                                                                   |
| <span data-ttu-id="a6252-275">public void footer(ReportSection footerSection, TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="a6252-275">public void footer(ReportSection footerSection, TableId tableId, FieldId fieldId)</span></span>                                                                         | <span data-ttu-id="a6252-276">フッターを制御します。</span><span class="sxs-lookup"><span data-stu-id="a6252-276">Controls the footer.</span></span>                                                                                                                              |
| <span data-ttu-id="a6252-277">public void reset(\[boolean delayExceptions\])</span><span class="sxs-lookup"><span data-stu-id="a6252-277">public void reset(\[boolean delayExceptions\])</span></span>                                                                                                            | <span data-ttu-id="a6252-278">複数のレポートを作成する ReportRun クラスの単一インスタンスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a6252-278">Enables a single instance of the ReportRun class to create multiple reports.</span></span>                                                                      |
| <span data-ttu-id="a6252-279">public void arrangeLevelNone()</span><span class="sxs-lookup"><span data-stu-id="a6252-279">public void arrangeLevelNone()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-280">public void run()</span><span class="sxs-lookup"><span data-stu-id="a6252-280">public void run()</span></span>                                                                                                                                         | <span data-ttu-id="a6252-281">レポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-281">Runs the report.</span></span>                                                                                                                                  |
| <span data-ttu-id="a6252-282">public void gotoYmm100(\[int mm100\])</span><span class="sxs-lookup"><span data-stu-id="a6252-282">public void gotoYmm100(\[int mm100\])</span></span>                                                                                                                     |                                                                                                                                                   |
| <span data-ttu-id="a6252-283">public void disableColumnHeadings(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="a6252-283">public void disableColumnHeadings(\[TableId tableId\])</span></span>                                                                                                    |                                                                                                                                                   |
| <span data-ttu-id="a6252-284">public void enablePageFooter()</span><span class="sxs-lookup"><span data-stu-id="a6252-284">public void enablePageFooter()</span></span>                                                                                                                            |                                                                                                                                                   |
| <span data-ttu-id="a6252-285">public void init()</span><span class="sxs-lookup"><span data-stu-id="a6252-285">public void init()</span></span>                                                                                                                                        |                                                                                                                                                   |
| <span data-ttu-id="a6252-286">public void arrangeLevelControl()</span><span class="sxs-lookup"><span data-stu-id="a6252-286">public void arrangeLevelControl()</span></span>                                                                                                                         |                                                                                                                                                   |
| <span data-ttu-id="a6252-287">public void disablePageFooter()</span><span class="sxs-lookup"><span data-stu-id="a6252-287">public void disablePageFooter()</span></span>                                                                                                                           |                                                                                                                                                   |
| <span data-ttu-id="a6252-288">public void addPendingSums()</span><span class="sxs-lookup"><span data-stu-id="a6252-288">public void addPendingSums()</span></span>                                                                                                                              | <span data-ttu-id="a6252-289">レポートの関連するフッターを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-289">Prints the relevant footers of the report.</span></span>                                                                                                        |
| <span data-ttu-id="a6252-290">public void arrangeLevelSection()</span><span class="sxs-lookup"><span data-stu-id="a6252-290">public void arrangeLevelSection()</span></span>                                                                                                                         |                                                                                                                                                   |
| <span data-ttu-id="a6252-291">public void enableSection(ReportSection section)</span><span class="sxs-lookup"><span data-stu-id="a6252-291">public void enableSection(ReportSection section)</span></span>                                                                                                          |                                                                                                                                                   |
| <span data-ttu-id="a6252-292">public void detach()</span><span class="sxs-lookup"><span data-stu-id="a6252-292">public void detach()</span></span>                                                                                                                                      |                                                                                                                                                   |
| <span data-ttu-id="a6252-293">public void addRangeDescription(int x, int y, str text, \[str fontName\], \[int fontSize\])</span><span class="sxs-lookup"><span data-stu-id="a6252-293">public void addRangeDescription(int x, int y, str text, \[str fontName\], \[int fontSize\])</span></span>                                                               |                                                                                                                                                   |
| <span data-ttu-id="a6252-294">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="a6252-294">public void finalize()</span></span>                                                                                                                                    |                                                                                                                                                   |

## <a name="method-allpages"></a><span data-ttu-id="a6252-295">メソッド allPages</span><span class="sxs-lookup"><span data-stu-id="a6252-295">Method allPages</span></span>

```xpp
public boolean allPages([boolean all])
```

### <a name="parameters---allpages"></a><span data-ttu-id="a6252-296">パラメーター - allPages</span><span class="sxs-lookup"><span data-stu-id="a6252-296">Parameters - allPages</span></span>

<span data-ttu-id="a6252-297">すべて</span><span class="sxs-lookup"><span data-stu-id="a6252-297">all</span></span>  

### <a name="return-value---allpages"></a><span data-ttu-id="a6252-298">戻り値 - allPages</span><span class="sxs-lookup"><span data-stu-id="a6252-298">Return Value - allPages</span></span>

## <a name="method-callmenufunction"></a><span data-ttu-id="a6252-299">メソッド callMenuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-299">Method callMenuFunction</span></span>

```xpp
public boolean callMenuFunction(xMenuFunction menuFunction)
```

### <a name="parameters---callmenufunction"></a><span data-ttu-id="a6252-300">パラメーター - callMenuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-300">Parameters - callMenuFunction</span></span>

<span data-ttu-id="a6252-301">menuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-301">menuFunction</span></span>  

### <a name="return-value---callmenufunction"></a><span data-ttu-id="a6252-302">戻り値 - callMenuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-302">Return Value - callMenuFunction</span></span>

## <a name="method-caption"></a><span data-ttu-id="a6252-303">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="a6252-303">Method caption</span></span>

<span data-ttu-id="a6252-304">レポートをプレビューするときにキャプションを作成し、レポートを印刷するときにドキュメント名を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6252-304">Creates a caption when previewing a report, or a document name when printing a report.</span></span>

```xpp
public str caption(str reportSpelling, str reportName, str designCaption, str designName)
```

### <a name="parameters---caption"></a><span data-ttu-id="a6252-305">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="a6252-305">Parameters - caption</span></span>

<span data-ttu-id="a6252-306">reportSpelling</span><span class="sxs-lookup"><span data-stu-id="a6252-306">reportSpelling</span></span>  
<span data-ttu-id="a6252-307">デザインの名前。</span><span class="sxs-lookup"><span data-stu-id="a6252-307">The name of the design.</span></span>

<!-- -->

<span data-ttu-id="a6252-308">reportName</span><span class="sxs-lookup"><span data-stu-id="a6252-308">reportName</span></span>  
<span data-ttu-id="a6252-309">デザインの名前。</span><span class="sxs-lookup"><span data-stu-id="a6252-309">The name of the design.</span></span>

<!-- -->

<span data-ttu-id="a6252-310">designCaption</span><span class="sxs-lookup"><span data-stu-id="a6252-310">designCaption</span></span>  
<span data-ttu-id="a6252-311">デザインの名前。</span><span class="sxs-lookup"><span data-stu-id="a6252-311">The name of the design.</span></span>

<!-- -->

<span data-ttu-id="a6252-312">designName</span><span class="sxs-lookup"><span data-stu-id="a6252-312">designName</span></span>  
<span data-ttu-id="a6252-313">デザインの名前。</span><span class="sxs-lookup"><span data-stu-id="a6252-313">The name of the design.</span></span>

### <a name="return-value---caption"></a><span data-ttu-id="a6252-314">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="a6252-314">Return Value - caption</span></span>

<span data-ttu-id="a6252-315">DesignLabel が空でない場合は、「DesignLabel - ReportSpelling」を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="a6252-315">A string that contains "DesignLabel - ReportSpelling" if the DesignLabel is not empty.</span></span> <span data-ttu-id="a6252-316">DesignLabel が空の場合は、「ReportName(DesignName) - ReportSpelling」を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="a6252-316">A string that contains "ReportName(DesignName) - ReportSpelling" if the DesignLabel is empty.</span></span>

### <a name="remarks---caption"></a><span data-ttu-id="a6252-317">備考 - caption</span><span class="sxs-lookup"><span data-stu-id="a6252-317">Remarks - caption</span></span>

<span data-ttu-id="a6252-318">このメソッドで super メソッドを呼び出すと、レポートをプレビューするときにキャプションとして使用され、レポートを印刷するときにドキュメント名として使用される文字列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-318">The call to the super method in this method creates a string that is used as a caption when previewing a report and as the document name when printing a report.</span></span> <span data-ttu-id="a6252-319">レポートのプレビュー時に使用されるキャプションが実際の言語になるようレポート デザインのキャプション プロパティを常に入力しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a6252-319">It is recommended that you always fill out the Caption property of the report design so that the caption that is used during the preview of the report is in the actual language.</span></span>

## <a name="method-collate"></a><span data-ttu-id="a6252-320">メソッド collate</span><span class="sxs-lookup"><span data-stu-id="a6252-320">Method collate</span></span>

```xpp
public boolean collate([boolean collate])
```

### <a name="parameters---collate"></a><span data-ttu-id="a6252-321">パラメーター - collate</span><span class="sxs-lookup"><span data-stu-id="a6252-321">Parameters - collate</span></span>

<span data-ttu-id="a6252-322">collate</span><span class="sxs-lookup"><span data-stu-id="a6252-322">collate</span></span>  

### <a name="return-value---collate"></a><span data-ttu-id="a6252-323">戻り値 - collate</span><span class="sxs-lookup"><span data-stu-id="a6252-323">Return Value - collate</span></span>

## <a name="method-columnheadings"></a><span data-ttu-id="a6252-324">メソッド columnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-324">Method columnHeadings</span></span>

<span data-ttu-id="a6252-325">レポートの列見出しのコントロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="a6252-325">Provides control of column headings in a report.</span></span>

```xpp
public TableId columnHeadings([TableId tableId])
```

### <a name="parameters---columnheadings"></a><span data-ttu-id="a6252-326">パラメーター - columnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-326">Parameters - columnHeadings</span></span>

<span data-ttu-id="a6252-327">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-327">tableId</span></span>  
<span data-ttu-id="a6252-328">テーブルのID、オプション。</span><span class="sxs-lookup"><span data-stu-id="a6252-328">A table ID; optional.</span></span>

### <a name="return-value---columnheadings"></a><span data-ttu-id="a6252-329">戻り値 - columnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-329">Return Value - columnHeadings</span></span>

<span data-ttu-id="a6252-330">columnHeading オブジェクトが最後に印刷された tableId 値。</span><span class="sxs-lookup"><span data-stu-id="a6252-330">The last tableId value for which columnHeading objects were printed.</span></span>

## <a name="method-control"></a><span data-ttu-id="a6252-331">メソッド control</span><span class="sxs-lookup"><span data-stu-id="a6252-331">Method control</span></span>

<span data-ttu-id="a6252-332">実行されているコントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="a6252-332">Retrieves the control that is being executed.</span></span>

```xpp
public ReportControl control()
```

### <a name="return-value---control"></a><span data-ttu-id="a6252-333">戻り値 - control</span><span class="sxs-lookup"><span data-stu-id="a6252-333">Return Value - control</span></span>

<span data-ttu-id="a6252-334">実行されているコントロール。</span><span class="sxs-lookup"><span data-stu-id="a6252-334">The control that is being executed.</span></span>

### <a name="remarks---control"></a><span data-ttu-id="a6252-335">備考 - control</span><span class="sxs-lookup"><span data-stu-id="a6252-335">Remarks - control</span></span>

<span data-ttu-id="a6252-336">このメソッドは、内部使用を目的としています。</span><span class="sxs-lookup"><span data-stu-id="a6252-336">This method is intended for internal use.</span></span>

## <a name="method-copies"></a><span data-ttu-id="a6252-337">メソッド copies</span><span class="sxs-lookup"><span data-stu-id="a6252-337">Method copies</span></span>

```xpp
public int copies([int numberOfCopies])
```

### <a name="parameters---copies"></a><span data-ttu-id="a6252-338">パラメーター - copies</span><span class="sxs-lookup"><span data-stu-id="a6252-338">Parameters - copies</span></span>

<span data-ttu-id="a6252-339">numberOfCopies</span><span class="sxs-lookup"><span data-stu-id="a6252-339">numberOfCopies</span></span>  

### <a name="return-value---copies"></a><span data-ttu-id="a6252-340">戻り値 - copies</span><span class="sxs-lookup"><span data-stu-id="a6252-340">Return Value - copies</span></span>

## <a name="method-copiestotal"></a><span data-ttu-id="a6252-341">メソッド copiesTotal</span><span class="sxs-lookup"><span data-stu-id="a6252-341">Method copiesTotal</span></span>

<span data-ttu-id="a6252-342">レポートのマーキング コピーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a6252-342">Enables marking copies of reports.</span></span>

```xpp
public int copiesTotal()
```

### <a name="return-value---copiestotal"></a><span data-ttu-id="a6252-343">戻り値 - copiesTotal</span><span class="sxs-lookup"><span data-stu-id="a6252-343">Return Value - copiesTotal</span></span>

<span data-ttu-id="a6252-344">ユーザーが sysPrintForm フォームで要求したコピーの数。</span><span class="sxs-lookup"><span data-stu-id="a6252-344">The number of copies the user requested in the sysPrintForm form.</span></span>

### <a name="remarks---copiestotal"></a><span data-ttu-id="a6252-345">備考 - copiesTotal</span><span class="sxs-lookup"><span data-stu-id="a6252-345">Remarks - copiesTotal</span></span>

<span data-ttu-id="a6252-346">コントロールは通常、レポートの実行中に評価されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-346">Controls are typically evaluated during the execution of a report.</span></span> <span data-ttu-id="a6252-347">このメソッドを使用するコントロールは、レポートを印刷するときに評価されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-347">A control that uses this method is evaluated when the report is printed.</span></span>

## <a name="method-copy"></a><span data-ttu-id="a6252-348">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="a6252-348">Method copy</span></span>

<span data-ttu-id="a6252-349">レポートのコピーの数を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-349">Returns the number of the copy of a report.</span></span>

```xpp
public int copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="a6252-350">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="a6252-350">Return Value - copy</span></span>

<span data-ttu-id="a6252-351">コピーの番号。</span><span class="sxs-lookup"><span data-stu-id="a6252-351">The number of the copy.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="a6252-352">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="a6252-352">Remarks - copy</span></span>

<span data-ttu-id="a6252-353">ユーザーが dataFunction メソッドを持つレポート コントロールを 3 枚印刷する場合、このメソッドは 1 枚目のコピーに対して 1、2 枚目のコピーに対して 2、最後のコピーに対して 3 を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-353">If the user prints three copies of a report a control that have a dataFunction method, this method will return one for the first copy, two for the second copy, and three for the last copy.</span></span>

## <a name="method-copydescription"></a><span data-ttu-id="a6252-354">メソッド copyDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-354">Method copyDescription</span></span>

```xpp
public str copyDescription()
```

### <a name="return-value---copydescription"></a><span data-ttu-id="a6252-355">戻り値 - copyDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-355">Return Value - copyDescription</span></span>

## <a name="method-createprogressform"></a><span data-ttu-id="a6252-356">メソッド createProgressForm</span><span class="sxs-lookup"><span data-stu-id="a6252-356">Method createProgressForm</span></span>

<span data-ttu-id="a6252-357">進捗情報を含むフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6252-357">Creates the form that contains progress information.</span></span>

```xpp
public xFormRun createProgressForm()
```

### <a name="return-value---createprogressform"></a><span data-ttu-id="a6252-358">戻り値 - createProgressForm</span><span class="sxs-lookup"><span data-stu-id="a6252-358">Return Value - createProgressForm</span></span>

<span data-ttu-id="a6252-359">進捗情報の表示に使用するフォーム。</span><span class="sxs-lookup"><span data-stu-id="a6252-359">The form to use to display the progress information.</span></span>

### <a name="remarks---createprogressform"></a><span data-ttu-id="a6252-360">備考 - createProgressForm</span><span class="sxs-lookup"><span data-stu-id="a6252-360">Remarks - createProgressForm</span></span>

<span data-ttu-id="a6252-361">このメソッドをオーバー ロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="a6252-361">You can overload this method.</span></span> <span data-ttu-id="a6252-362">このメソッドは、最初のページが作成されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-362">The method is called when the first page is created.</span></span> <span data-ttu-id="a6252-363">既定の実装では、SysPrintProgress フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="a6252-363">The default implementation will open the SysPrintProgress form.</span></span> <span data-ttu-id="a6252-364">進捗状況フォームを実装する場合は、カーネル内でこれらのメソッドが呼び出されるため、setNames および setPagePercent メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6252-364">If you implement your own progress form, you must implement the setNames and setPagePercent methods because these methods are called within the kernel.</span></span> <span data-ttu-id="a6252-365">このフォームは、ページの印刷時ではなくページの作成時に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-365">This form is shown when the pages are created, not when the pages are printed.</span></span>

## <a name="method-currentymm100"></a><span data-ttu-id="a6252-366">メソッド currentYmm100</span><span class="sxs-lookup"><span data-stu-id="a6252-366">Method currentYmm100</span></span>

```xpp
public int currentYmm100()
```

### <a name="return-value---currentymm100"></a><span data-ttu-id="a6252-367">戻り値 - currentYmm100</span><span class="sxs-lookup"><span data-stu-id="a6252-367">Return Value - currentYmm100</span></span>

## <a name="method-design"></a><span data-ttu-id="a6252-368">メソッド design</span><span class="sxs-lookup"><span data-stu-id="a6252-368">Method design</span></span>

<span data-ttu-id="a6252-369">デザインの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a6252-369">Gets or sets the name of the design.</span></span>

```xpp
public ReportDesign design([AnyType nameOrReportDesign])
```

### <a name="parameters---design"></a><span data-ttu-id="a6252-370">パラメーター - design</span><span class="sxs-lookup"><span data-stu-id="a6252-370">Parameters - design</span></span>

<span data-ttu-id="a6252-371">nameOrReportDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-371">nameOrReportDesign</span></span>  
<span data-ttu-id="a6252-372">デザインの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-372">The name of the design; optional.</span></span>

### <a name="return-value---design"></a><span data-ttu-id="a6252-373">戻り値 - design</span><span class="sxs-lookup"><span data-stu-id="a6252-373">Return Value - design</span></span>

<span data-ttu-id="a6252-374">デザインの名前。</span><span class="sxs-lookup"><span data-stu-id="a6252-374">The name of the design.</span></span>

### <a name="remarks---design"></a><span data-ttu-id="a6252-375">備考 - design</span><span class="sxs-lookup"><span data-stu-id="a6252-375">Remarks - design</span></span>

<span data-ttu-id="a6252-376">このメソッドを使用すると、レポートの実行中にあるデザインから別のデザインに変更できます。</span><span class="sxs-lookup"><span data-stu-id="a6252-376">This method can be used to change from one design to another while the report is executed.</span></span>

## <a name="method-devicename"></a><span data-ttu-id="a6252-377">メソッド deviceName</span><span class="sxs-lookup"><span data-stu-id="a6252-377">Method deviceName</span></span>

```xpp
public str deviceName([str device])
```

### <a name="parameters---devicename"></a><span data-ttu-id="a6252-378">パラメーター - deviceName</span><span class="sxs-lookup"><span data-stu-id="a6252-378">Parameters - deviceName</span></span>

<span data-ttu-id="a6252-379">デバイス</span><span class="sxs-lookup"><span data-stu-id="a6252-379">device</span></span>  

### <a name="return-value---devicename"></a><span data-ttu-id="a6252-380">戻り値 - deviceName</span><span class="sxs-lookup"><span data-stu-id="a6252-380">Return Value - deviceName</span></span>

## <a name="method-dialog"></a><span data-ttu-id="a6252-381">メソッド dialog</span><span class="sxs-lookup"><span data-stu-id="a6252-381">Method dialog</span></span>

```xpp
public Object dialog(Object dialog)
```

### <a name="parameters---dialog"></a><span data-ttu-id="a6252-382">パラメーター - dialog</span><span class="sxs-lookup"><span data-stu-id="a6252-382">Parameters - dialog</span></span>

<span data-ttu-id="a6252-383">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="a6252-383">dialog</span></span>  

### <a name="return-value---dialog"></a><span data-ttu-id="a6252-384">戻り値 - dialog</span><span class="sxs-lookup"><span data-stu-id="a6252-384">Return Value - dialog</span></span>

## <a name="method-drivername"></a><span data-ttu-id="a6252-385">メソッド driverName</span><span class="sxs-lookup"><span data-stu-id="a6252-385">Method driverName</span></span>

<span data-ttu-id="a6252-386">プリンター ドライバー名を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-386">Returns the printer driver name.</span></span>

```xpp
public str driverName()
```

### <a name="return-value---drivername"></a><span data-ttu-id="a6252-387">戻り値 - driverName</span><span class="sxs-lookup"><span data-stu-id="a6252-387">Return Value - driverName</span></span>

<span data-ttu-id="a6252-388">プリンター ドライバー名。</span><span class="sxs-lookup"><span data-stu-id="a6252-388">The printer driver name.</span></span>

### <a name="remarks---drivername"></a><span data-ttu-id="a6252-389">備考 - driverName</span><span class="sxs-lookup"><span data-stu-id="a6252-389">Remarks - driverName</span></span>

<span data-ttu-id="a6252-390">メソッドはしばしば文字列「winspool」を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-390">The method often returns the string "winspool".</span></span> <span data-ttu-id="a6252-391">これは、プリンター デバイス コンテキストが作成されるときに使用するプリンター ドライバー名です。</span><span class="sxs-lookup"><span data-stu-id="a6252-391">This is the printer driver name that is used when the printer device context is created.</span></span> <span data-ttu-id="a6252-392">コンピューターにプリンタが設定されていない場合、文字列「画面」が返されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-392">If no printers have been set up on the computer, the string "Screen" is returned.</span></span>

## <a name="method-enableallbodies"></a><span data-ttu-id="a6252-393">メソッド enableAllBodies</span><span class="sxs-lookup"><span data-stu-id="a6252-393">Method enableAllBodies</span></span>

```xpp
public boolean enableAllBodies([boolean enable])
```

### <a name="parameters---enableallbodies"></a><span data-ttu-id="a6252-394">パラメーター - enableAllBodies</span><span class="sxs-lookup"><span data-stu-id="a6252-394">Parameters - enableAllBodies</span></span>

<span data-ttu-id="a6252-395">enable</span><span class="sxs-lookup"><span data-stu-id="a6252-395">enable</span></span>  

### <a name="return-value---enableallbodies"></a><span data-ttu-id="a6252-396">戻り値 - enableAllBodies</span><span class="sxs-lookup"><span data-stu-id="a6252-396">Return Value - enableAllBodies</span></span>

## <a name="method-execute"></a><span data-ttu-id="a6252-397">メソッド execute</span><span class="sxs-lookup"><span data-stu-id="a6252-397">Method execute</span></span>

<span data-ttu-id="a6252-398">レポートのプログラム可能なセクションを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-398">Prints the programmable sections of a report.</span></span>

```xpp
public boolean execute(int number)
```

### <a name="parameters---execute"></a><span data-ttu-id="a6252-399">パラメーター - execute</span><span class="sxs-lookup"><span data-stu-id="a6252-399">Parameters - execute</span></span>

<span data-ttu-id="a6252-400">番号</span><span class="sxs-lookup"><span data-stu-id="a6252-400">number</span></span>  
<span data-ttu-id="a6252-401">プログラム可能なセクションの controlNumber 値。</span><span class="sxs-lookup"><span data-stu-id="a6252-401">The controlNumber value of the programmable section.</span></span>

### <a name="return-value---execute"></a><span data-ttu-id="a6252-402">戻り値 - execute</span><span class="sxs-lookup"><span data-stu-id="a6252-402">Return Value - execute</span></span>

<span data-ttu-id="a6252-403">toPage オブジェクトが生成済みである場合は false; それ以外の場合は true。</span><span class="sxs-lookup"><span data-stu-id="a6252-403">false if the toPage object has been generated; otherwise, true.</span></span>

## <a name="method-executebodycolumnheadings"></a><span data-ttu-id="a6252-404">メソッド executeBodyColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-404">Method executeBodyColumnHeadings</span></span>

<span data-ttu-id="a6252-405">レポートの本文セクションの列ヘッダーを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-405">Prints the column headings of a body section in a report.</span></span>

```xpp
public boolean executeBodyColumnHeadings(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---executebodycolumnheadings"></a><span data-ttu-id="a6252-406">パラメーター - executeBodyColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-406">Parameters - executeBodyColumnHeadings</span></span>

<span data-ttu-id="a6252-407">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-407">tableId</span></span>  
<span data-ttu-id="a6252-408">セクション グループの DataField プロパティのフィールド ID (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-408">The field ID of the DataField property of a section group; optional.</span></span>

<!-- -->

<span data-ttu-id="a6252-409">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-409">fieldId</span></span>  
<span data-ttu-id="a6252-410">セクション グループの DataField プロパティのフィールド ID (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-410">The field ID of the DataField property of a section group; optional.</span></span>

### <a name="return-value---executebodycolumnheadings"></a><span data-ttu-id="a6252-411">戻り値 - executeBodyColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-411">Return Value - executeBodyColumnHeadings</span></span>

<span data-ttu-id="a6252-412">いずれかの列ヘッダーが印刷された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a6252-412">true if any column headings were printed; otherwise, false.</span></span>

### <a name="remarks---executebodycolumnheadings"></a><span data-ttu-id="a6252-413">備考 - executeBodyColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-413">Remarks - executeBodyColumnHeadings</span></span>

<span data-ttu-id="a6252-414">このメソッドは、レポートに自動的に印刷されるものより多くの列見出しをレポートに含める必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="a6252-414">This method is useful when a report should contain more column headings than those automatically printed in the report.</span></span>

## <a name="method-executecolumnheadings"></a><span data-ttu-id="a6252-415">メソッド executeColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-415">Method executeColumnHeadings</span></span>

```xpp
public boolean executeColumnHeadings(ReportSection section)
```

### <a name="parameters---executecolumnheadings"></a><span data-ttu-id="a6252-416">パラメーター - executeColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-416">Parameters - executeColumnHeadings</span></span>

<span data-ttu-id="a6252-417">セクション</span><span class="sxs-lookup"><span data-stu-id="a6252-417">section</span></span>  

### <a name="return-value---executecolumnheadings"></a><span data-ttu-id="a6252-418">戻り値 - executeColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-418">Return Value - executeColumnHeadings</span></span>

## <a name="method-executecontrolcolumnheadings"></a><span data-ttu-id="a6252-419">メソッド executeControlColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-419">Method executeControlColumnHeadings</span></span>

<span data-ttu-id="a6252-420">プログラム可能なセクションの列のヘッダーを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-420">Executes the column headings of a programmable section.</span></span>

```xpp
public boolean executeControlColumnHeadings(int number)
```

### <a name="parameters---executecontrolcolumnheadings"></a><span data-ttu-id="a6252-421">パラメーター - executeControlColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-421">Parameters - executeControlColumnHeadings</span></span>

<span data-ttu-id="a6252-422">番号</span><span class="sxs-lookup"><span data-stu-id="a6252-422">number</span></span>  
<span data-ttu-id="a6252-423">プログラム可能なセクションの controlNumber 値。</span><span class="sxs-lookup"><span data-stu-id="a6252-423">The controlNumber value of the programmable section.</span></span>

### <a name="return-value---executecontrolcolumnheadings"></a><span data-ttu-id="a6252-424">戻り値 - executeControlColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-424">Return Value - executeControlColumnHeadings</span></span>

<span data-ttu-id="a6252-425">いずれかのセクションが印刷された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a6252-425">true if any sections were printed; otherwise, false.</span></span>

### <a name="remarks---executecontrolcolumnheadings"></a><span data-ttu-id="a6252-426">備考 - executeControlColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-426">Remarks - executeControlColumnHeadings</span></span>

<span data-ttu-id="a6252-427">このメソッドは、プログラム可能なセクションに columnHeading オブジェクトを追加する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="a6252-427">This method is useful if you want to add columnHeading objects to a programmable section.</span></span> <span data-ttu-id="a6252-428">プログラマブル セクションが改ページを引き起こす場合、セクションの columnHeadings オブジェクトが繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-428">If a programmable section causes a page break, the columnHeadings objects of the section are repeated.</span></span> <span data-ttu-id="a6252-429">このような状況では、このメソッドを呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a6252-429">Under these circumstances this method not have to be called.</span></span>

## <a name="method-executefooter"></a><span data-ttu-id="a6252-430">メソッド executeFooter</span><span class="sxs-lookup"><span data-stu-id="a6252-430">Method executeFooter</span></span>

<span data-ttu-id="a6252-431">フッター セクションを実行を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-431">Execute a footer section.</span></span>

```xpp
public boolean executeFooter([TableId tableId], [FieldId fieldId])
```

### <a name="parameters---executefooter"></a><span data-ttu-id="a6252-432">パラメーター - executeFooter</span><span class="sxs-lookup"><span data-stu-id="a6252-432">Parameters - executeFooter</span></span>

<span data-ttu-id="a6252-433">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-433">tableId</span></span>  
<span data-ttu-id="a6252-434">フッター セクション グループの dataField プロパティのフィールド ID (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-434">The field ID of the dataField property of the footer section group; optional.</span></span>

<!-- -->

<span data-ttu-id="a6252-435">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-435">fieldId</span></span>  
<span data-ttu-id="a6252-436">フッター セクション グループの dataField プロパティのフィールド ID (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-436">The field ID of the dataField property of the footer section group; optional.</span></span>

### <a name="return-value---executefooter"></a><span data-ttu-id="a6252-437">戻り値 - executeFooter</span><span class="sxs-lookup"><span data-stu-id="a6252-437">Return Value - executeFooter</span></span>

<span data-ttu-id="a6252-438">何かが印刷された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a6252-438">true if anything was printed; otherwise, false.</span></span>

## <a name="method-executeheader"></a><span data-ttu-id="a6252-439">メソッド executeHeader</span><span class="sxs-lookup"><span data-stu-id="a6252-439">Method executeHeader</span></span>

<span data-ttu-id="a6252-440">ヘッダー セクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-440">Executes a header section.</span></span>

```xpp
public boolean executeHeader([TableId tableId], [FieldId fieldId])
```

### <a name="parameters---executeheader"></a><span data-ttu-id="a6252-441">パラメーター - executeHeader</span><span class="sxs-lookup"><span data-stu-id="a6252-441">Parameters - executeHeader</span></span>

<span data-ttu-id="a6252-442">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-442">tableId</span></span>  
<span data-ttu-id="a6252-443">ヘッダー セクション グループの dataField プロパティのフィールド ID (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-443">The field ID of the dataField property of the header section group; optional.</span></span>

<!-- -->

<span data-ttu-id="a6252-444">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-444">fieldId</span></span>  
<span data-ttu-id="a6252-445">ヘッダー セクション グループの dataField プロパティのフィールド ID (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-445">The field ID of the dataField property of the header section group; optional.</span></span>

### <a name="return-value---executeheader"></a><span data-ttu-id="a6252-446">戻り値 - executeHeader</span><span class="sxs-lookup"><span data-stu-id="a6252-446">Return Value - executeHeader</span></span>

## <a name="method-executesection"></a><span data-ttu-id="a6252-447">メソッド executeSection</span><span class="sxs-lookup"><span data-stu-id="a6252-447">Method executeSection</span></span>

<span data-ttu-id="a6252-448">レポートの指定されたセクションを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-448">Prints the specified section in the report.</span></span>

```xpp
public boolean executeSection(ReportSection section)
```

### <a name="parameters---executesection"></a><span data-ttu-id="a6252-449">パラメーター - executeSection</span><span class="sxs-lookup"><span data-stu-id="a6252-449">Parameters - executeSection</span></span>

<span data-ttu-id="a6252-450">セクション</span><span class="sxs-lookup"><span data-stu-id="a6252-450">section</span></span>  
<span data-ttu-id="a6252-451">印刷するセクション。</span><span class="sxs-lookup"><span data-stu-id="a6252-451">The section to print.</span></span>

### <a name="return-value---executesection"></a><span data-ttu-id="a6252-452">戻り値 - executeSection</span><span class="sxs-lookup"><span data-stu-id="a6252-452">Return Value - executeSection</span></span>

## <a name="method-fetch"></a><span data-ttu-id="a6252-453">メソッド fetch</span><span class="sxs-lookup"><span data-stu-id="a6252-453">Method fetch</span></span>

<span data-ttu-id="a6252-454">レポート クエリを実行し、クエリによって検出されたレコードの送信メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6252-454">Executes the report query and calls the send method for the record that is found by the query.</span></span>

```xpp
public boolean fetch()
```

### <a name="return-value---fetch"></a><span data-ttu-id="a6252-455">戻り値 - fetch</span><span class="sxs-lookup"><span data-stu-id="a6252-455">Return Value - fetch</span></span>

<span data-ttu-id="a6252-456">そのレポートの実行を継続する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a6252-456">true if execution of the report should continue; otherwise, false.</span></span>

### <a name="remarks---fetch"></a><span data-ttu-id="a6252-457">備考 - fetch</span><span class="sxs-lookup"><span data-stu-id="a6252-457">Remarks - fetch</span></span>

<span data-ttu-id="a6252-458">fetch メソッドは、run メソッドのスーパー コールから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-458">The fetch method is called from the super call in the run method.</span></span>

## <a name="method-from"></a><span data-ttu-id="a6252-459">メソッド from</span><span class="sxs-lookup"><span data-stu-id="a6252-459">Method from</span></span>

```xpp
public int from([int fromPage])
```

### <a name="parameters---from"></a><span data-ttu-id="a6252-460">パラメーター - from</span><span class="sxs-lookup"><span data-stu-id="a6252-460">Parameters - from</span></span>

<span data-ttu-id="a6252-461">fromPage</span><span class="sxs-lookup"><span data-stu-id="a6252-461">fromPage</span></span>  

### <a name="return-value---from"></a><span data-ttu-id="a6252-462">戻り値 - from</span><span class="sxs-lookup"><span data-stu-id="a6252-462">Return Value - from</span></span>

## <a name="method-generatedesign"></a><span data-ttu-id="a6252-463">メソッド generateDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-463">Method generateDesign</span></span>

```xpp
public int generateDesign([Query query], [int designNo])
```

### <a name="parameters---generatedesign"></a><span data-ttu-id="a6252-464">パラメーター - generateDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-464">Parameters - generateDesign</span></span>

<span data-ttu-id="a6252-465">クエリ</span><span class="sxs-lookup"><span data-stu-id="a6252-465">query</span></span>  

<!-- -->

<span data-ttu-id="a6252-466">designNo</span><span class="sxs-lookup"><span data-stu-id="a6252-466">designNo</span></span>  

### <a name="return-value---generatedesign"></a><span data-ttu-id="a6252-467">戻り値 - generateDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-467">Return Value - generateDesign</span></span>

## <a name="method-getdeclineoverwrite"></a><span data-ttu-id="a6252-468">メソッド getDeclineOverwrite</span><span class="sxs-lookup"><span data-stu-id="a6252-468">Method getDeclineOverwrite</span></span>

```xpp
public boolean getDeclineOverwrite()
```

### <a name="return-value---getdeclineoverwrite"></a><span data-ttu-id="a6252-469">戻り値 - getDeclineOverwrite</span><span class="sxs-lookup"><span data-stu-id="a6252-469">Return Value - getDeclineOverwrite</span></span>

## <a name="method-getnumberofprinters"></a><span data-ttu-id="a6252-470">メソッド getNumberOfPrinters</span><span class="sxs-lookup"><span data-stu-id="a6252-470">Method getNumberOfPrinters</span></span>

```xpp
public int getNumberOfPrinters()
```

### <a name="return-value---getnumberofprinters"></a><span data-ttu-id="a6252-471">戻り値 - getNumberOfPrinters</span><span class="sxs-lookup"><span data-stu-id="a6252-471">Return Value - getNumberOfPrinters</span></span>

## <a name="method-getprinter"></a><span data-ttu-id="a6252-472">メソッド getPrinter</span><span class="sxs-lookup"><span data-stu-id="a6252-472">Method getPrinter</span></span>

```xpp
public str getPrinter(int number)
```

### <a name="parameters---getprinter"></a><span data-ttu-id="a6252-473">パラメーター - getPrinter</span><span class="sxs-lookup"><span data-stu-id="a6252-473">Parameters - getPrinter</span></span>

<span data-ttu-id="a6252-474">番号</span><span class="sxs-lookup"><span data-stu-id="a6252-474">number</span></span>  

### <a name="return-value---getprinter"></a><span data-ttu-id="a6252-475">戻り値 - getPrinter</span><span class="sxs-lookup"><span data-stu-id="a6252-475">Return Value - getPrinter</span></span>

## <a name="method-getrangedescription"></a><span data-ttu-id="a6252-476">メソッド getRangeDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-476">Method getRangeDescription</span></span>

```xpp
public str getRangeDescription(int number)
```

### <a name="parameters---getrangedescription"></a><span data-ttu-id="a6252-477">パラメーター - getRangeDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-477">Parameters - getRangeDescription</span></span>

<span data-ttu-id="a6252-478">番号</span><span class="sxs-lookup"><span data-stu-id="a6252-478">number</span></span>  

### <a name="return-value---getrangedescription"></a><span data-ttu-id="a6252-479">戻り値 - getRangeDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-479">Return Value - getRangeDescription</span></span>

## <a name="method-getreportviewer"></a><span data-ttu-id="a6252-480">メソッド getReportViewer</span><span class="sxs-lookup"><span data-stu-id="a6252-480">Method getReportViewer</span></span>

```xpp
public ReportViewer getReportViewer()
```

### <a name="return-value---getreportviewer"></a><span data-ttu-id="a6252-481">戻り値 - getReportViewer</span><span class="sxs-lookup"><span data-stu-id="a6252-481">Return Value - getReportViewer</span></span>

## <a name="method-gettarget"></a><span data-ttu-id="a6252-482">メソッド getTarget</span><span class="sxs-lookup"><span data-stu-id="a6252-482">Method getTarget</span></span>

```xpp
public PrintMedium getTarget()
```

### <a name="return-value---gettarget"></a><span data-ttu-id="a6252-483">戻り値 - getTarget</span><span class="sxs-lookup"><span data-stu-id="a6252-483">Return Value - getTarget</span></span>

## <a name="method-hasgenerateddesign"></a><span data-ttu-id="a6252-484">メソッド hasGeneratedDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-484">Method hasGeneratedDesign</span></span>

```xpp
public boolean hasGeneratedDesign()
```

### <a name="return-value---hasgenerateddesign"></a><span data-ttu-id="a6252-485">戻り値 - hasGeneratedDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-485">Return Value - hasGeneratedDesign</span></span>

## <a name="method-headerdescription"></a><span data-ttu-id="a6252-486">メソッド headerDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-486">Method headerDescription</span></span>

```xpp
public str headerDescription()
```

### <a name="return-value---headerdescription"></a><span data-ttu-id="a6252-487">戻り値 - headerDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-487">Return Value - headerDescription</span></span>

## <a name="method-heightofpagefooters"></a><span data-ttu-id="a6252-488">メソッド heightOfPageFooters</span><span class="sxs-lookup"><span data-stu-id="a6252-488">Method heightOfPageFooters</span></span>

```xpp
public int heightOfPageFooters()
```

### <a name="return-value---heightofpagefooters"></a><span data-ttu-id="a6252-489">戻り値 - heightOfPageFooters</span><span class="sxs-lookup"><span data-stu-id="a6252-489">Return Value - heightOfPageFooters</span></span>

## <a name="method-indent"></a><span data-ttu-id="a6252-490">メソッド indent</span><span class="sxs-lookup"><span data-stu-id="a6252-490">Method indent</span></span>

```xpp
public int indent()
```

### <a name="return-value---indent"></a><span data-ttu-id="a6252-491">戻り値 - indent</span><span class="sxs-lookup"><span data-stu-id="a6252-491">Return Value - indent</span></span>

## <a name="method-isbodyenabled"></a><span data-ttu-id="a6252-492">メソッド isBodyEnabled</span><span class="sxs-lookup"><span data-stu-id="a6252-492">Method isBodyEnabled</span></span>

```xpp
public boolean isBodyEnabled(TableId tableId)
```

### <a name="parameters---isbodyenabled"></a><span data-ttu-id="a6252-493">パラメーター - isBodyEnabled</span><span class="sxs-lookup"><span data-stu-id="a6252-493">Parameters - isBodyEnabled</span></span>

<span data-ttu-id="a6252-494">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-494">tableId</span></span>  

### <a name="return-value---isbodyenabled"></a><span data-ttu-id="a6252-495">戻り値 - isBodyEnabled</span><span class="sxs-lookup"><span data-stu-id="a6252-495">Return Value - isBodyEnabled</span></span>

## <a name="method-jobid"></a><span data-ttu-id="a6252-496">メソッド jobId</span><span class="sxs-lookup"><span data-stu-id="a6252-496">Method jobId</span></span>

```xpp
public Int64 jobId()
```

### <a name="return-value---jobid"></a><span data-ttu-id="a6252-497">戻り値 - jobId</span><span class="sxs-lookup"><span data-stu-id="a6252-497">Return Value - jobId</span></span>

## <a name="method-last"></a><span data-ttu-id="a6252-498">メソッド last</span><span class="sxs-lookup"><span data-stu-id="a6252-498">Method last</span></span>

```xpp
public Common last(TableId tableId)
```

### <a name="parameters---last"></a><span data-ttu-id="a6252-499">パラメーター - last</span><span class="sxs-lookup"><span data-stu-id="a6252-499">Parameters - last</span></span>

<span data-ttu-id="a6252-500">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-500">tableId</span></span>  

### <a name="return-value---last"></a><span data-ttu-id="a6252-501">戻り値 - last</span><span class="sxs-lookup"><span data-stu-id="a6252-501">Return Value - last</span></span>

## <a name="method-mm100left"></a><span data-ttu-id="a6252-502">メソッド mm100Left</span><span class="sxs-lookup"><span data-stu-id="a6252-502">Method mm100Left</span></span>

```xpp
public int mm100Left()
```

### <a name="return-value---mm100left"></a><span data-ttu-id="a6252-503">戻り値 - mm100Left</span><span class="sxs-lookup"><span data-stu-id="a6252-503">Return Value - mm100Left</span></span>

## <a name="method-mm100pageheight"></a><span data-ttu-id="a6252-504">メソッド mm100PageHeight</span><span class="sxs-lookup"><span data-stu-id="a6252-504">Method mm100PageHeight</span></span>

```xpp
public int mm100PageHeight()
```

### <a name="return-value---mm100pageheight"></a><span data-ttu-id="a6252-505">戻り値 - mm100PageHeight</span><span class="sxs-lookup"><span data-stu-id="a6252-505">Return Value - mm100PageHeight</span></span>

## <a name="method-name"></a><span data-ttu-id="a6252-506">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a6252-506">Method name</span></span>

<span data-ttu-id="a6252-507">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a6252-507">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

```xpp
public str name([str name])
```

### <a name="parameters---name"></a><span data-ttu-id="a6252-508">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="a6252-508">Parameters - name</span></span>

<span data-ttu-id="a6252-509">名前</span><span class="sxs-lookup"><span data-stu-id="a6252-509">name</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="a6252-510">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="a6252-510">Return Value - name</span></span>

<span data-ttu-id="a6252-511">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="a6252-511">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="a6252-512">備考 - name</span><span class="sxs-lookup"><span data-stu-id="a6252-512">Remarks - name</span></span>

<span data-ttu-id="a6252-513">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6252-513">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="a6252-514">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="a6252-514">Begins with a letter.</span></span>
-   <span data-ttu-id="a6252-515">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="a6252-515">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="a6252-516">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a6252-516">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="a6252-517">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a6252-517">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="a6252-518">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="a6252-518">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-pack"></a><span data-ttu-id="a6252-519">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="a6252-519">Method pack</span></span>

<span data-ttu-id="a6252-520">ReportRun クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="a6252-520">Serializes the current instance of the ReportRun class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="a6252-521">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="a6252-521">Return Value - pack</span></span>

<span data-ttu-id="a6252-522">ReportRun クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="a6252-522">A container that contains the current instance of the ReportRun class.</span></span>

## <a name="method-packdesign"></a><span data-ttu-id="a6252-523">メソッド packDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-523">Method packDesign</span></span>

```xpp
public container packDesign()
```

### <a name="return-value---packdesign"></a><span data-ttu-id="a6252-524">戻り値 - packDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-524">Return Value - packDesign</span></span>

## <a name="method-packpagesettings"></a><span data-ttu-id="a6252-525">メソッド packPageSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-525">Method packPageSettings</span></span>

```xpp
public container packPageSettings()
```

### <a name="return-value---packpagesettings"></a><span data-ttu-id="a6252-526">戻り値 - packPageSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-526">Return Value - packPageSettings</span></span>

## <a name="method-packprintersettings"></a><span data-ttu-id="a6252-527">メソッド packPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-527">Method packPrinterSettings</span></span>

```xpp
public container packPrinterSettings()
```

### <a name="return-value---packprintersettings"></a><span data-ttu-id="a6252-528">戻り値 - packPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-528">Return Value - packPrinterSettings</span></span>

## <a name="method-packprintjobsettings"></a><span data-ttu-id="a6252-529">メソッド packPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-529">Method packPrintJobSettings</span></span>

```xpp
public container packPrintJobSettings()
```

### <a name="return-value---packprintjobsettings"></a><span data-ttu-id="a6252-530">戻り値 - packPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-530">Return Value - packPrintJobSettings</span></span>

## <a name="method-packsubtotalsettings"></a><span data-ttu-id="a6252-531">メソッド packSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-531">Method packSubtotalSettings</span></span>

```xpp
public container packSubtotalSettings()
```

### <a name="return-value---packsubtotalsettings"></a><span data-ttu-id="a6252-532">戻り値 - packSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-532">Return Value - packSubtotalSettings</span></span>

## <a name="method-page"></a><span data-ttu-id="a6252-533">メソッド page</span><span class="sxs-lookup"><span data-stu-id="a6252-533">Method page</span></span>

```xpp
public int page([int number])
```

### <a name="parameters---page"></a><span data-ttu-id="a6252-534">パラメーター - page</span><span class="sxs-lookup"><span data-stu-id="a6252-534">Parameters - page</span></span>

<span data-ttu-id="a6252-535">番号</span><span class="sxs-lookup"><span data-stu-id="a6252-535">number</span></span>  

### <a name="return-value---page"></a><span data-ttu-id="a6252-536">戻り値 - page</span><span class="sxs-lookup"><span data-stu-id="a6252-536">Return Value - page</span></span>

## <a name="method-pageformatting"></a><span data-ttu-id="a6252-537">メソッド pageFormatting</span><span class="sxs-lookup"><span data-stu-id="a6252-537">Method pageFormatting</span></span>

<span data-ttu-id="a6252-538">プリンターのプリンター プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="a6252-538">Displays the printer properties of the printer.</span></span>

```xpp
public boolean pageFormatting()
```

### <a name="return-value---pageformatting"></a><span data-ttu-id="a6252-539">戻り値 - pageFormatting</span><span class="sxs-lookup"><span data-stu-id="a6252-539">Return Value - pageFormatting</span></span>

### <a name="remarks---pageformatting"></a><span data-ttu-id="a6252-540">備考 - pageFormatting</span><span class="sxs-lookup"><span data-stu-id="a6252-540">Remarks - pageFormatting</span></span>

<span data-ttu-id="a6252-541">レポート オブジェクトのこのメソッドは、カーネルによって呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="a6252-541">This method on the Report object is never called by the kernel.</span></span> <span data-ttu-id="a6252-542">ユーザーがプロパティ ボタンをクリックすると sysPrintForm フォームによって呼び出すことができますが、代わりに sysPrintForm フォームは直接呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6252-542">It could be called by the sysPrintForm form when the user clicks the Properties button, but instead, the sysPrintForm form calls the directly.</span></span>

## <a name="method-pagestotal"></a><span data-ttu-id="a6252-543">メソッド pagesTotal</span><span class="sxs-lookup"><span data-stu-id="a6252-543">Method pagesTotal</span></span>

```xpp
public int pagesTotal()
```

### <a name="return-value---pagestotal"></a><span data-ttu-id="a6252-544">戻り値 - pagesTotal</span><span class="sxs-lookup"><span data-stu-id="a6252-544">Return Value - pagesTotal</span></span>

## <a name="method-passthrough"></a><span data-ttu-id="a6252-545">メソッド passThrough</span><span class="sxs-lookup"><span data-stu-id="a6252-545">Method passThrough</span></span>

```xpp
public str passThrough(str str)
```

### <a name="parameters---passthrough"></a><span data-ttu-id="a6252-546">パラメーター - passThrough</span><span class="sxs-lookup"><span data-stu-id="a6252-546">Parameters - passThrough</span></span>

<span data-ttu-id="a6252-547">str</span><span class="sxs-lookup"><span data-stu-id="a6252-547">str</span></span>  

### <a name="return-value---passthrough"></a><span data-ttu-id="a6252-548">戻り値 - passThrough</span><span class="sxs-lookup"><span data-stu-id="a6252-548">Return Value - passThrough</span></span>

## <a name="method-pixelsleft"></a><span data-ttu-id="a6252-549">メソッド pixelsLeft</span><span class="sxs-lookup"><span data-stu-id="a6252-549">Method pixelsLeft</span></span>

```xpp
public int pixelsLeft()
```

### <a name="return-value---pixelsleft"></a><span data-ttu-id="a6252-550">戻り値 - pixelsLeft</span><span class="sxs-lookup"><span data-stu-id="a6252-550">Return Value - pixelsLeft</span></span>

## <a name="method-print"></a><span data-ttu-id="a6252-551">メソッド print</span><span class="sxs-lookup"><span data-stu-id="a6252-551">Method print</span></span>

<span data-ttu-id="a6252-552">生成されたレポートを、プリンターや画面などの出力メディアに送信します。</span><span class="sxs-lookup"><span data-stu-id="a6252-552">Sends the generated report to a print medium, such as a printer or the screen.</span></span>

```xpp
public int print()
```

### <a name="return-value---print"></a><span data-ttu-id="a6252-553">戻り値 - print</span><span class="sxs-lookup"><span data-stu-id="a6252-553">Return Value - print</span></span>

### <a name="remarks---print"></a><span data-ttu-id="a6252-554">備考 - print</span><span class="sxs-lookup"><span data-stu-id="a6252-554">Remarks - print</span></span>

<span data-ttu-id="a6252-555">このメソッドで super メソッドを呼び出すと、生成されたレポートがプリンターやスクリーンなどの printMedium オブジェクトに送られます。</span><span class="sxs-lookup"><span data-stu-id="a6252-555">The call to the super method in this method directs the generated report to a printMedium object, such as printer or screen.</span></span> <span data-ttu-id="a6252-556">ターゲットが画像である場合、スーパー メソッドを呼び出すと、reportViewer オブジェクトがクライアント上で作成され、showPage メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-556">If the target is a screen, the call to the super method will create a reportViewer object on the client and call the showPage method.</span></span> <span data-ttu-id="a6252-557">ターゲットがプリンターである場合、スーパー メソッドを呼び出すと、reportOutput オブジェクトが作成され、このオブジェクトの印刷メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-557">If the target is a printer, the call to the super method will create a reportOutput object and call the print method on this object.</span></span> <span data-ttu-id="a6252-558">PrintJobSettings クラスの outputToClient メソッドが true のパラメーターで呼び出された場合、reportViewer オブジェクトが作成され、そのオブジェクトの印刷メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-558">If the outputToClient method of the PrintJobSettings class has been called with a parameter of true, a reportViewer object will be created and the print method of that object will be called.</span></span> <span data-ttu-id="a6252-559">この方法で、サーバーで生成されたレポートはクライアントで設定されているプリンターに出力できます。</span><span class="sxs-lookup"><span data-stu-id="a6252-559">In in this manner, a report that is generated on the server can be output to a printer that is set up on the client.</span></span>

## <a name="method-printerattributes"></a><span data-ttu-id="a6252-560">メソッド printerAttributes</span><span class="sxs-lookup"><span data-stu-id="a6252-560">Method printerAttributes</span></span>

```xpp
public int printerAttributes()
```

### <a name="return-value---printerattributes"></a><span data-ttu-id="a6252-561">戻り値 - printerAttributes</span><span class="sxs-lookup"><span data-stu-id="a6252-561">Return Value - printerAttributes</span></span>

## <a name="method-printeraverageppm"></a><span data-ttu-id="a6252-562">メソッド printerAveragePPM</span><span class="sxs-lookup"><span data-stu-id="a6252-562">Method printerAveragePPM</span></span>

```xpp
public int printerAveragePPM()
```

### <a name="return-value---printeraverageppm"></a><span data-ttu-id="a6252-563">戻り値 - printerAveragePPM</span><span class="sxs-lookup"><span data-stu-id="a6252-563">Return Value - printerAveragePPM</span></span>

## <a name="method-printercomment"></a><span data-ttu-id="a6252-564">メソッド printerComment</span><span class="sxs-lookup"><span data-stu-id="a6252-564">Method printerComment</span></span>

```xpp
public str printerComment()
```

### <a name="return-value---printercomment"></a><span data-ttu-id="a6252-565">戻り値 - printerComment</span><span class="sxs-lookup"><span data-stu-id="a6252-565">Return Value - printerComment</span></span>

## <a name="method-printerdatatype"></a><span data-ttu-id="a6252-566">メソッド printerDatatype</span><span class="sxs-lookup"><span data-stu-id="a6252-566">Method printerDatatype</span></span>

```xpp
public str printerDatatype()
```

### <a name="return-value---printerdatatype"></a><span data-ttu-id="a6252-567">戻り値 - printerDatatype</span><span class="sxs-lookup"><span data-stu-id="a6252-567">Return Value - printerDatatype</span></span>

## <a name="method-printerdefaultpriority"></a><span data-ttu-id="a6252-568">メソッド printerDefaultPriority</span><span class="sxs-lookup"><span data-stu-id="a6252-568">Method printerDefaultPriority</span></span>

```xpp
public int printerDefaultPriority()
```

### <a name="return-value---printerdefaultpriority"></a><span data-ttu-id="a6252-569">戻り値 - printerDefaultPriority</span><span class="sxs-lookup"><span data-stu-id="a6252-569">Return Value - printerDefaultPriority</span></span>

## <a name="method-printerdrivername"></a><span data-ttu-id="a6252-570">メソッド printerDriverName</span><span class="sxs-lookup"><span data-stu-id="a6252-570">Method printerDriverName</span></span>

```xpp
public str printerDriverName()
```

### <a name="return-value---printerdrivername"></a><span data-ttu-id="a6252-571">戻り値 - printerDriverName</span><span class="sxs-lookup"><span data-stu-id="a6252-571">Return Value - printerDriverName</span></span>

## <a name="method-printerfontinfo"></a><span data-ttu-id="a6252-572">メソッド printerFontInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-572">Method printerFontInfo</span></span>

<span data-ttu-id="a6252-573">レポートの印刷に使用されるフォントを示します。</span><span class="sxs-lookup"><span data-stu-id="a6252-573">Indicates which font is used to print the report.</span></span>

```xpp
public str printerFontInfo()
```

### <a name="return-value---printerfontinfo"></a><span data-ttu-id="a6252-574">戻り値 - printerFontInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-574">Return Value - printerFontInfo</span></span>

<span data-ttu-id="a6252-575">フォントの名前。</span><span class="sxs-lookup"><span data-stu-id="a6252-575">The name of the font.</span></span>

### <a name="remarks---printerfontinfo"></a><span data-ttu-id="a6252-576">備考 - printerFontInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-576">Remarks - printerFontInfo</span></span>

<span data-ttu-id="a6252-577">レポートの印刷に使用するフォントは、そのフォントがユーザー システムで使用できない可能性があるため、コントロールのフォント プロパティで設定したフォントと必ずしも同じではありません。</span><span class="sxs-lookup"><span data-stu-id="a6252-577">The font to use to print the report is not necessarily the same as that set on the font property of the control as that font might not be available on the user system.</span></span>

## <a name="method-printerlocation"></a><span data-ttu-id="a6252-578">メソッド printerLocation</span><span class="sxs-lookup"><span data-stu-id="a6252-578">Method printerLocation</span></span>

```xpp
public str printerLocation()
```

### <a name="return-value---printerlocation"></a><span data-ttu-id="a6252-579">戻り値 - printerLocation</span><span class="sxs-lookup"><span data-stu-id="a6252-579">Return Value - printerLocation</span></span>

## <a name="method-printerpageheight"></a><span data-ttu-id="a6252-580">メソッド printerPageHeight</span><span class="sxs-lookup"><span data-stu-id="a6252-580">Method printerPageHeight</span></span>

```xpp
public int printerPageHeight()
```

### <a name="return-value---printerpageheight"></a><span data-ttu-id="a6252-581">戻り値 - printerPageHeight</span><span class="sxs-lookup"><span data-stu-id="a6252-581">Return Value - printerPageHeight</span></span>

## <a name="method-printerpagewidth"></a><span data-ttu-id="a6252-582">メソッド printerPageWidth</span><span class="sxs-lookup"><span data-stu-id="a6252-582">Method printerPageWidth</span></span>

```xpp
public int printerPageWidth()
```

### <a name="return-value---printerpagewidth"></a><span data-ttu-id="a6252-583">戻り値 - printerPageWidth</span><span class="sxs-lookup"><span data-stu-id="a6252-583">Return Value - printerPageWidth</span></span>

## <a name="method-printerpaper"></a><span data-ttu-id="a6252-584">メソッド printerPaper</span><span class="sxs-lookup"><span data-stu-id="a6252-584">Method printerPaper</span></span>

```xpp
public int printerPaper()
```

### <a name="return-value---printerpaper"></a><span data-ttu-id="a6252-585">戻り値 - printerPaper</span><span class="sxs-lookup"><span data-stu-id="a6252-585">Return Value - printerPaper</span></span>

## <a name="method-printerparameters"></a><span data-ttu-id="a6252-586">メソッド printerParameters</span><span class="sxs-lookup"><span data-stu-id="a6252-586">Method printerParameters</span></span>

```xpp
public str printerParameters()
```

### <a name="return-value---printerparameters"></a><span data-ttu-id="a6252-587">戻り値 - printerParameters</span><span class="sxs-lookup"><span data-stu-id="a6252-587">Return Value - printerParameters</span></span>

## <a name="method-printerportname"></a><span data-ttu-id="a6252-588">メソッド printerPortName</span><span class="sxs-lookup"><span data-stu-id="a6252-588">Method printerPortName</span></span>

```xpp
public str printerPortName()
```

### <a name="return-value---printerportname"></a><span data-ttu-id="a6252-589">戻り値 - printerPortName</span><span class="sxs-lookup"><span data-stu-id="a6252-589">Return Value - printerPortName</span></span>

## <a name="method-printerprintername"></a><span data-ttu-id="a6252-590">メソッド printerPrinterName</span><span class="sxs-lookup"><span data-stu-id="a6252-590">Method printerPrinterName</span></span>

```xpp
public str printerPrinterName()
```

### <a name="return-value---printerprintername"></a><span data-ttu-id="a6252-591">戻り値 - printerPrinterName</span><span class="sxs-lookup"><span data-stu-id="a6252-591">Return Value - printerPrinterName</span></span>

## <a name="method-printerprintprocessor"></a><span data-ttu-id="a6252-592">メソッド printerPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="a6252-592">Method printerPrintProcessor</span></span>

```xpp
public str printerPrintProcessor()
```

### <a name="return-value---printerprintprocessor"></a><span data-ttu-id="a6252-593">戻り値 - printerPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="a6252-593">Return Value - printerPrintProcessor</span></span>

## <a name="method-printerpriority"></a><span data-ttu-id="a6252-594">メソッド printerPriority</span><span class="sxs-lookup"><span data-stu-id="a6252-594">Method printerPriority</span></span>

```xpp
public int printerPriority()
```

### <a name="return-value---printerpriority"></a><span data-ttu-id="a6252-595">戻り値 - printerPriority</span><span class="sxs-lookup"><span data-stu-id="a6252-595">Return Value - printerPriority</span></span>

## <a name="method-printerqueuedjobs"></a><span data-ttu-id="a6252-596">メソッド printerQueuedJobs</span><span class="sxs-lookup"><span data-stu-id="a6252-596">Method printerQueuedJobs</span></span>

```xpp
public int printerQueuedJobs()
```

### <a name="return-value---printerqueuedjobs"></a><span data-ttu-id="a6252-597">戻り値 - printerQueuedJobs</span><span class="sxs-lookup"><span data-stu-id="a6252-597">Return Value - printerQueuedJobs</span></span>

## <a name="method-printersepfile"></a><span data-ttu-id="a6252-598">メソッド printerSepFile</span><span class="sxs-lookup"><span data-stu-id="a6252-598">Method printerSepFile</span></span>

```xpp
public str printerSepFile()
```

### <a name="return-value---printersepfile"></a><span data-ttu-id="a6252-599">戻り値 - printerSepFile</span><span class="sxs-lookup"><span data-stu-id="a6252-599">Return Value - printerSepFile</span></span>

## <a name="method-printerservername"></a><span data-ttu-id="a6252-600">メソッド printerServerName</span><span class="sxs-lookup"><span data-stu-id="a6252-600">Method printerServerName</span></span>

```xpp
public str printerServerName()
```

### <a name="return-value---printerservername"></a><span data-ttu-id="a6252-601">戻り値 - printerServerName</span><span class="sxs-lookup"><span data-stu-id="a6252-601">Return Value - printerServerName</span></span>

## <a name="method-printersettings"></a><span data-ttu-id="a6252-602">メソッド printerSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-602">Method printerSettings</span></span>

<span data-ttu-id="a6252-603">ユーザーがプリンターの設定を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a6252-603">Enables the user to select printer settings.</span></span>

```xpp
public boolean printerSettings([int showWhat])
```

### <a name="parameters---printersettings"></a><span data-ttu-id="a6252-604">パラメーター - printerSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-604">Parameters - printerSettings</span></span>

<span data-ttu-id="a6252-605">showWhat</span><span class="sxs-lookup"><span data-stu-id="a6252-605">showWhat</span></span>  
<span data-ttu-id="a6252-606">このパラメーターは現在機能していません。</span><span class="sxs-lookup"><span data-stu-id="a6252-606">This parameter is currently not functional.</span></span>

### <a name="return-value---printersettings"></a><span data-ttu-id="a6252-607">戻り値 - printerSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-607">Return Value - printerSettings</span></span>

<span data-ttu-id="a6252-608">そのレポートの実行を継続する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a6252-608">true if execution of the report should continue; otherwise, false.</span></span>

### <a name="remarks---printersettings"></a><span data-ttu-id="a6252-609">備考 - printerSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-609">Remarks - printerSettings</span></span>

<span data-ttu-id="a6252-610">このメソッドで super メソッドを呼び出すと、sysPrintForm フォームが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-610">The call to the super method in this method runs the sysPrintForm form.</span></span> <span data-ttu-id="a6252-611">prompt メソッドは、prompt メソッドの super メソッド呼び出しから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-611">The prompt method is called from the super method call in the prompt method.</span></span> <span data-ttu-id="a6252-612">reportDesign オブジェクトの PrintFormName プロパティは、printerSettings オブジェクトの super メソッドの呼び出しが実行されるフォームを決定します。</span><span class="sxs-lookup"><span data-stu-id="a6252-612">The PrintFormName property on the reportDesign object determines which form the call to the super method in the printerSettings object will run.</span></span>

## <a name="method-printersharename"></a><span data-ttu-id="a6252-613">メソッド printerShareName</span><span class="sxs-lookup"><span data-stu-id="a6252-613">Method printerShareName</span></span>

```xpp
public str printerShareName()
```

### <a name="return-value---printersharename"></a><span data-ttu-id="a6252-614">戻り値 - printerShareName</span><span class="sxs-lookup"><span data-stu-id="a6252-614">Return Value - printerShareName</span></span>

## <a name="method-printerstarttime"></a><span data-ttu-id="a6252-615">メソッド printerStartTime</span><span class="sxs-lookup"><span data-stu-id="a6252-615">Method printerStartTime</span></span>

```xpp
public TimeOfDay printerStartTime()
```

### <a name="return-value---printerstarttime"></a><span data-ttu-id="a6252-616">戻り値 - printerStartTime</span><span class="sxs-lookup"><span data-stu-id="a6252-616">Return Value - printerStartTime</span></span>

## <a name="method-printerstatus"></a><span data-ttu-id="a6252-617">メソッド printerStatus</span><span class="sxs-lookup"><span data-stu-id="a6252-617">Method printerStatus</span></span>

```xpp
public int printerStatus()
```

### <a name="return-value---printerstatus"></a><span data-ttu-id="a6252-618">戻り値 - printerStatus</span><span class="sxs-lookup"><span data-stu-id="a6252-618">Return Value - printerStatus</span></span>

## <a name="method-printeruntiltime"></a><span data-ttu-id="a6252-619">メソッド printerUntilTime</span><span class="sxs-lookup"><span data-stu-id="a6252-619">Method printerUntilTime</span></span>

```xpp
public TimeOfDay printerUntilTime()
```

### <a name="return-value---printeruntiltime"></a><span data-ttu-id="a6252-620">戻り値 - printerUntilTime</span><span class="sxs-lookup"><span data-stu-id="a6252-620">Return Value - printerUntilTime</span></span>

## <a name="method-printjobsettings"></a><span data-ttu-id="a6252-621">メソッド printJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-621">Method printJobSettings</span></span>

```xpp
public PrintJobSettings printJobSettings([container packedPrintJobSettings])
```

### <a name="parameters---printjobsettings"></a><span data-ttu-id="a6252-622">パラメーター - printJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-622">Parameters - printJobSettings</span></span>

<span data-ttu-id="a6252-623">packedPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-623">packedPrintJobSettings</span></span>  

### <a name="return-value---printjobsettings"></a><span data-ttu-id="a6252-624">戻り値 - printJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-624">Return Value - printJobSettings</span></span>

## <a name="method-printsum"></a><span data-ttu-id="a6252-625">メソッド printSum</span><span class="sxs-lookup"><span data-stu-id="a6252-625">Method printSum</span></span>

```xpp
public int printSum()
```

### <a name="return-value---printsum"></a><span data-ttu-id="a6252-626">戻り値 - printSum</span><span class="sxs-lookup"><span data-stu-id="a6252-626">Return Value - printSum</span></span>

## <a name="method-progressform"></a><span data-ttu-id="a6252-627">メソッド progressForm</span><span class="sxs-lookup"><span data-stu-id="a6252-627">Method progressForm</span></span>

```xpp
public xFormRun progressForm([xFormRun form])
```

### <a name="parameters---progressform"></a><span data-ttu-id="a6252-628">パラメーター - progressForm</span><span class="sxs-lookup"><span data-stu-id="a6252-628">Parameters - progressForm</span></span>

<span data-ttu-id="a6252-629">フォーム</span><span class="sxs-lookup"><span data-stu-id="a6252-629">form</span></span>  

### <a name="return-value---progressform"></a><span data-ttu-id="a6252-630">戻り値 - progressForm</span><span class="sxs-lookup"><span data-stu-id="a6252-630">Return Value - progressForm</span></span>

## <a name="method-progressinfo"></a><span data-ttu-id="a6252-631">メソッド progressInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-631">Method progressInfo</span></span>

<span data-ttu-id="a6252-632">セクションが実行されるたびに、レポートが実行中に生成されるレポートの量を記述する文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6252-632">Creates a string that describes how much of the report has been generated during the execution of a report every time that a section is executed.</span></span>

```xpp
public str progressInfo(int pageNo, int lineNo)
```

### <a name="parameters---progressinfo"></a><span data-ttu-id="a6252-633">パラメーター - progressInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-633">Parameters - progressInfo</span></span>

<span data-ttu-id="a6252-634">pageNo</span><span class="sxs-lookup"><span data-stu-id="a6252-634">pageNo</span></span>  
<span data-ttu-id="a6252-635">ページのセクション番号。</span><span class="sxs-lookup"><span data-stu-id="a6252-635">The section number of the page.</span></span>

<!-- -->

<span data-ttu-id="a6252-636">lineNo</span><span class="sxs-lookup"><span data-stu-id="a6252-636">lineNo</span></span>  
<span data-ttu-id="a6252-637">ページのセクション番号。</span><span class="sxs-lookup"><span data-stu-id="a6252-637">The section number of the page.</span></span>

### <a name="return-value---progressinfo"></a><span data-ttu-id="a6252-638">戻り値 - progressInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-638">Return Value - progressInfo</span></span>

<span data-ttu-id="a6252-639">生産されたレポートの量を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="a6252-639">A string that describes how much of the report has been generated.</span></span>

## <a name="method-prompt"></a><span data-ttu-id="a6252-640">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="a6252-640">Method prompt</span></span>

<span data-ttu-id="a6252-641">レポートの実行をユーザーに求めます。</span><span class="sxs-lookup"><span data-stu-id="a6252-641">Prompts the user a report is run.</span></span>

```xpp
public boolean prompt([boolean enableCopy], [boolean enablePages], [boolean enableDevice], [boolean enableProperties], [boolean enablePrintTo])
```

### <a name="parameters---prompt"></a><span data-ttu-id="a6252-642">パラメーター - prompt</span><span class="sxs-lookup"><span data-stu-id="a6252-642">Parameters - prompt</span></span>

<span data-ttu-id="a6252-643">enableCopy</span><span class="sxs-lookup"><span data-stu-id="a6252-643">enableCopy</span></span>  
<span data-ttu-id="a6252-644">ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a6252-644">A Boolean value that indicates whether the user can select the target in the sysPrintForm form; optional.</span></span>

<!-- -->

<span data-ttu-id="a6252-645">enablePages</span><span class="sxs-lookup"><span data-stu-id="a6252-645">enablePages</span></span>  
<span data-ttu-id="a6252-646">ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a6252-646">A Boolean value that indicates whether the user can select the target in the sysPrintForm form; optional.</span></span>

<!-- -->

<span data-ttu-id="a6252-647">enableDevice</span><span class="sxs-lookup"><span data-stu-id="a6252-647">enableDevice</span></span>  
<span data-ttu-id="a6252-648">ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a6252-648">A Boolean value that indicates whether the user can select the target in the sysPrintForm form; optional.</span></span>

<!-- -->

<span data-ttu-id="a6252-649">enableProperties</span><span class="sxs-lookup"><span data-stu-id="a6252-649">enableProperties</span></span>  
<span data-ttu-id="a6252-650">ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a6252-650">A Boolean value that indicates whether the user can select the target in the sysPrintForm form; optional.</span></span>

<!-- -->

<span data-ttu-id="a6252-651">enablePrintTo</span><span class="sxs-lookup"><span data-stu-id="a6252-651">enablePrintTo</span></span>  
<span data-ttu-id="a6252-652">ユーザーが sysPrintForm フォームでターゲットを選択できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a6252-652">A Boolean value that indicates whether the user can select the target in the sysPrintForm form; optional.</span></span>

### <a name="return-value---prompt"></a><span data-ttu-id="a6252-653">戻り値 - prompt</span><span class="sxs-lookup"><span data-stu-id="a6252-653">Return Value - prompt</span></span>

<span data-ttu-id="a6252-654">レポートの実行を継続する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a6252-654">true if execution of report should continue; otherwise, false.</span></span>

### <a name="remarks---prompt"></a><span data-ttu-id="a6252-655">備考 - prompt</span><span class="sxs-lookup"><span data-stu-id="a6252-655">Remarks - prompt</span></span>

<span data-ttu-id="a6252-656">確認メソッドで super メソッドを呼び出すと、sysPrintForm フォームが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-656">The call to the super method in the prompt method runs the sysPrintForm form.</span></span> <span data-ttu-id="a6252-657">このメソッドは、run メソッドから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-657">This method is called from the run method.</span></span>

## <a name="method-query"></a><span data-ttu-id="a6252-658">メソッド query</span><span class="sxs-lookup"><span data-stu-id="a6252-658">Method query</span></span>

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a><span data-ttu-id="a6252-659">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="a6252-659">Parameters - query</span></span>

<span data-ttu-id="a6252-660">クエリ</span><span class="sxs-lookup"><span data-stu-id="a6252-660">query</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="a6252-661">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="a6252-661">Return Value - query</span></span>

## <a name="method-queryrun"></a><span data-ttu-id="a6252-662">メソッド queryRun</span><span class="sxs-lookup"><span data-stu-id="a6252-662">Method queryRun</span></span>

```xpp
public QueryRun queryRun([QueryRun queryRun])
```

### <a name="parameters---queryrun"></a><span data-ttu-id="a6252-663">パラメーター - queryRun</span><span class="sxs-lookup"><span data-stu-id="a6252-663">Parameters - queryRun</span></span>

<span data-ttu-id="a6252-664">queryRun</span><span class="sxs-lookup"><span data-stu-id="a6252-664">queryRun</span></span>  

### <a name="return-value---queryrun"></a><span data-ttu-id="a6252-665">戻り値 - queryRun</span><span class="sxs-lookup"><span data-stu-id="a6252-665">Return Value - queryRun</span></span>

## <a name="method-report"></a><span data-ttu-id="a6252-666">メソッド report</span><span class="sxs-lookup"><span data-stu-id="a6252-666">Method report</span></span>

```xpp
public Report report()
```

### <a name="return-value---report"></a><span data-ttu-id="a6252-667">戻り値 - report</span><span class="sxs-lookup"><span data-stu-id="a6252-667">Return Value - report</span></span>

## <a name="method-reportuser"></a><span data-ttu-id="a6252-668">メソッド reportUser</span><span class="sxs-lookup"><span data-stu-id="a6252-668">Method reportUser</span></span>

```xpp
public str reportUser([str user])
```

### <a name="parameters---reportuser"></a><span data-ttu-id="a6252-669">パラメーター - reportUser</span><span class="sxs-lookup"><span data-stu-id="a6252-669">Parameters - reportUser</span></span>

<span data-ttu-id="a6252-670">ユーザー</span><span class="sxs-lookup"><span data-stu-id="a6252-670">user</span></span>  

### <a name="return-value---reportuser"></a><span data-ttu-id="a6252-671">戻り値 - reportUser</span><span class="sxs-lookup"><span data-stu-id="a6252-671">Return Value - reportUser</span></span>

## <a name="method-rulercm"></a><span data-ttu-id="a6252-672">メソッド rulerCM</span><span class="sxs-lookup"><span data-stu-id="a6252-672">Method rulerCM</span></span>

```xpp
public int rulerCM()
```

### <a name="return-value---rulercm"></a><span data-ttu-id="a6252-673">戻り値 - rulerCM</span><span class="sxs-lookup"><span data-stu-id="a6252-673">Return Value - rulerCM</span></span>

## <a name="method-rulerinch"></a><span data-ttu-id="a6252-674">メソッド rulerINCH</span><span class="sxs-lookup"><span data-stu-id="a6252-674">Method rulerINCH</span></span>

```xpp
public int rulerINCH()
```

### <a name="return-value---rulerinch"></a><span data-ttu-id="a6252-675">戻り値 - rulerINCH</span><span class="sxs-lookup"><span data-stu-id="a6252-675">Return Value - rulerINCH</span></span>

## <a name="method-screenfontinfo"></a><span data-ttu-id="a6252-676">メソッド screenFontInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-676">Method screenFontInfo</span></span>

```xpp
public str screenFontInfo()
```

### <a name="return-value---screenfontinfo"></a><span data-ttu-id="a6252-677">戻り値 - screenFontInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-677">Return Value - screenFontInfo</span></span>

## <a name="method-section"></a><span data-ttu-id="a6252-678">メソッド section</span><span class="sxs-lookup"><span data-stu-id="a6252-678">Method section</span></span>

```xpp
public ReportSection section()
```

### <a name="return-value---section"></a><span data-ttu-id="a6252-679">戻り値 - section</span><span class="sxs-lookup"><span data-stu-id="a6252-679">Return Value - section</span></span>

## <a name="method-sectionsleft"></a><span data-ttu-id="a6252-680">メソッド sectionsLeft</span><span class="sxs-lookup"><span data-stu-id="a6252-680">Method sectionsLeft</span></span>

```xpp
public int sectionsLeft(ReportSection section)
```

### <a name="parameters---sectionsleft"></a><span data-ttu-id="a6252-681">パラメーター - sectionsLeft</span><span class="sxs-lookup"><span data-stu-id="a6252-681">Parameters - sectionsLeft</span></span>

<span data-ttu-id="a6252-682">セクション</span><span class="sxs-lookup"><span data-stu-id="a6252-682">section</span></span>  

### <a name="return-value---sectionsleft"></a><span data-ttu-id="a6252-683">戻り値 - sectionsLeft</span><span class="sxs-lookup"><span data-stu-id="a6252-683">Return Value - sectionsLeft</span></span>

## <a name="method-send"></a><span data-ttu-id="a6252-684">メソッド send</span><span class="sxs-lookup"><span data-stu-id="a6252-684">Method send</span></span>

<span data-ttu-id="a6252-685">セクション グループに属する本文セクションをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="a6252-685">Triggers the body sections that belong to a section group.</span></span>

```xpp
public boolean send(Common cursor, [int level], [boolean triggerOffBody], [boolean newPageBeforeBody])
```

### <a name="parameters---send"></a><span data-ttu-id="a6252-686">パラメーター - send</span><span class="sxs-lookup"><span data-stu-id="a6252-686">Parameters - send</span></span>

<span data-ttu-id="a6252-687">cursor</span><span class="sxs-lookup"><span data-stu-id="a6252-687">cursor</span></span>  

<!-- -->

<span data-ttu-id="a6252-688">level</span><span class="sxs-lookup"><span data-stu-id="a6252-688">level</span></span>  

<!-- -->

<span data-ttu-id="a6252-689">triggerOffBody</span><span class="sxs-lookup"><span data-stu-id="a6252-689">triggerOffBody</span></span>  

<!-- -->

<span data-ttu-id="a6252-690">newPageBeforeBody</span><span class="sxs-lookup"><span data-stu-id="a6252-690">newPageBeforeBody</span></span>  

### <a name="return-value---send"></a><span data-ttu-id="a6252-691">戻り値 - send</span><span class="sxs-lookup"><span data-stu-id="a6252-691">Return Value - send</span></span>

<span data-ttu-id="a6252-692">toPage オブジェクトが生成済みである場合は false; それ以外の場合は true。</span><span class="sxs-lookup"><span data-stu-id="a6252-692">false if the toPage object has been generated; otherwise true.</span></span>

### <a name="remarks---send"></a><span data-ttu-id="a6252-693">備考 - send</span><span class="sxs-lookup"><span data-stu-id="a6252-693">Remarks - send</span></span>

<span data-ttu-id="a6252-694">ReportSection クラスの executeSection メソッドは、トリガーされた各セクションで呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-694">The executeSection method of the ReportSection class is called on each triggered section.</span></span> <span data-ttu-id="a6252-695">マスター詳細レポートの既定では、マスター テーブルのレコードは 1 のレベルで、詳細テーブルのレコードのレベルは 2 です。</span><span class="sxs-lookup"><span data-stu-id="a6252-695">By default in a master-detail report, the records from the master table have level of one, and the records from the details table have level of two.</span></span>

## <a name="method-settarget"></a><span data-ttu-id="a6252-696">メソッド setTarget</span><span class="sxs-lookup"><span data-stu-id="a6252-696">Method setTarget</span></span>

```xpp
public PrintMedium setTarget(PrintMedium target)
```

### <a name="parameters---settarget"></a><span data-ttu-id="a6252-697">パラメーター - setTarget</span><span class="sxs-lookup"><span data-stu-id="a6252-697">Parameters - setTarget</span></span>

<span data-ttu-id="a6252-698">target</span><span class="sxs-lookup"><span data-stu-id="a6252-698">target</span></span>  

### <a name="return-value---settarget"></a><span data-ttu-id="a6252-699">戻り値 - setTarget</span><span class="sxs-lookup"><span data-stu-id="a6252-699">Return Value - setTarget</span></span>

## <a name="method-showmenufunction"></a><span data-ttu-id="a6252-700">メソッド showMenuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-700">Method showMenuFunction</span></span>

```xpp
public boolean showMenuFunction(xMenuFunction menuFunction)
```

### <a name="parameters---showmenufunction"></a><span data-ttu-id="a6252-701">パラメーター - showMenuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-701">Parameters - showMenuFunction</span></span>

<span data-ttu-id="a6252-702">menuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-702">menuFunction</span></span>  

### <a name="return-value---showmenufunction"></a><span data-ttu-id="a6252-703">戻り値 - showMenuFunction</span><span class="sxs-lookup"><span data-stu-id="a6252-703">Return Value - showMenuFunction</span></span>

## <a name="method-showmenureference"></a><span data-ttu-id="a6252-704">メソッド showMenuReference</span><span class="sxs-lookup"><span data-stu-id="a6252-704">Method showMenuReference</span></span>

```xpp
public boolean showMenuReference(WebMenu menuReference)
```

### <a name="parameters---showmenureference"></a><span data-ttu-id="a6252-705">パラメーター - showMenuReference</span><span class="sxs-lookup"><span data-stu-id="a6252-705">Parameters - showMenuReference</span></span>

<span data-ttu-id="a6252-706">menuReference</span><span class="sxs-lookup"><span data-stu-id="a6252-706">menuReference</span></span>  

### <a name="return-value---showmenureference"></a><span data-ttu-id="a6252-707">戻り値 - showMenuReference</span><span class="sxs-lookup"><span data-stu-id="a6252-707">Return Value - showMenuReference</span></span>

## <a name="method-sortinfo"></a><span data-ttu-id="a6252-708">メソッド sortInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-708">Method sortInfo</span></span>

```xpp
public str sortInfo(Common cursor)
```

### <a name="parameters---sortinfo"></a><span data-ttu-id="a6252-709">パラメーター - sortInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-709">Parameters - sortInfo</span></span>

<span data-ttu-id="a6252-710">cursor</span><span class="sxs-lookup"><span data-stu-id="a6252-710">cursor</span></span>  

### <a name="return-value---sortinfo"></a><span data-ttu-id="a6252-711">戻り値 - sortInfo</span><span class="sxs-lookup"><span data-stu-id="a6252-711">Return Value - sortInfo</span></span>

## <a name="method-startdate"></a><span data-ttu-id="a6252-712">メソッド startDate</span><span class="sxs-lookup"><span data-stu-id="a6252-712">Method startDate</span></span>

```xpp
public Date startDate()
```

### <a name="return-value---startdate"></a><span data-ttu-id="a6252-713">戻り値 - startDate</span><span class="sxs-lookup"><span data-stu-id="a6252-713">Return Value - startDate</span></span>

## <a name="method-startdatetime"></a><span data-ttu-id="a6252-714">メソッド startDateTime</span><span class="sxs-lookup"><span data-stu-id="a6252-714">Method startDateTime</span></span>

```xpp
public DateTime startDateTime()
```

### <a name="return-value---startdatetime"></a><span data-ttu-id="a6252-715">戻り値 - startDateTime</span><span class="sxs-lookup"><span data-stu-id="a6252-715">Return Value - startDateTime</span></span>

## <a name="method-startmachinedate"></a><span data-ttu-id="a6252-716">メソッド startMachineDate</span><span class="sxs-lookup"><span data-stu-id="a6252-716">Method startMachineDate</span></span>

```xpp
public Date startMachineDate()
```

### <a name="return-value---startmachinedate"></a><span data-ttu-id="a6252-717">戻り値 - startMachineDate</span><span class="sxs-lookup"><span data-stu-id="a6252-717">Return Value - startMachineDate</span></span>

## <a name="method-starttime"></a><span data-ttu-id="a6252-718">メソッド startTime</span><span class="sxs-lookup"><span data-stu-id="a6252-718">Method startTime</span></span>

```xpp
public TimeOfDay startTime()
```

### <a name="return-value---starttime"></a><span data-ttu-id="a6252-719">戻り値 - startTime</span><span class="sxs-lookup"><span data-stu-id="a6252-719">Return Value - startTime</span></span>

## <a name="method-sum"></a><span data-ttu-id="a6252-720">メソッド sum</span><span class="sxs-lookup"><span data-stu-id="a6252-720">Method sum</span></span>

```xpp
public Real sum(TableId tableId, FieldId fieldId, [int indent])
```

### <a name="parameters---sum"></a><span data-ttu-id="a6252-721">パラメーター - sum</span><span class="sxs-lookup"><span data-stu-id="a6252-721">Parameters - sum</span></span>

<span data-ttu-id="a6252-722">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-722">tableId</span></span>  

<!-- -->

<span data-ttu-id="a6252-723">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-723">fieldId</span></span>  

<!-- -->

<span data-ttu-id="a6252-724">インデント</span><span class="sxs-lookup"><span data-stu-id="a6252-724">indent</span></span>  

### <a name="return-value---sum"></a><span data-ttu-id="a6252-725">戻り値 - sum</span><span class="sxs-lookup"><span data-stu-id="a6252-725">Return Value - sum</span></span>

## <a name="method-sumcontrol"></a><span data-ttu-id="a6252-726">メソッド sumControl</span><span class="sxs-lookup"><span data-stu-id="a6252-726">Method sumControl</span></span>

```xpp
public Real sumControl(str fieldName, [int indent])
```

### <a name="parameters---sumcontrol"></a><span data-ttu-id="a6252-727">パラメーター - sumControl</span><span class="sxs-lookup"><span data-stu-id="a6252-727">Parameters - sumControl</span></span>

<span data-ttu-id="a6252-728">fieldName</span><span class="sxs-lookup"><span data-stu-id="a6252-728">fieldName</span></span>  

<!-- -->

<span data-ttu-id="a6252-729">インデント</span><span class="sxs-lookup"><span data-stu-id="a6252-729">indent</span></span>  

### <a name="return-value---sumcontrol"></a><span data-ttu-id="a6252-730">戻り値 - sumControl</span><span class="sxs-lookup"><span data-stu-id="a6252-730">Return Value - sumControl</span></span>

## <a name="method-sumcontrolneg"></a><span data-ttu-id="a6252-731">メソッド sumControlNeg</span><span class="sxs-lookup"><span data-stu-id="a6252-731">Method sumControlNeg</span></span>

```xpp
public Real sumControlNeg(str fieldName, [int indent])
```

### <a name="parameters---sumcontrolneg"></a><span data-ttu-id="a6252-732">パラメーター - sumControlNeg</span><span class="sxs-lookup"><span data-stu-id="a6252-732">Parameters - sumControlNeg</span></span>

<span data-ttu-id="a6252-733">fieldName</span><span class="sxs-lookup"><span data-stu-id="a6252-733">fieldName</span></span>  

<!-- -->

<span data-ttu-id="a6252-734">インデント</span><span class="sxs-lookup"><span data-stu-id="a6252-734">indent</span></span>  

### <a name="return-value---sumcontrolneg"></a><span data-ttu-id="a6252-735">戻り値 - sumControlNeg</span><span class="sxs-lookup"><span data-stu-id="a6252-735">Return Value - sumControlNeg</span></span>

## <a name="method-sumcontrolpos"></a><span data-ttu-id="a6252-736">メソッド sumControlPos</span><span class="sxs-lookup"><span data-stu-id="a6252-736">Method sumControlPos</span></span>

```xpp
public Real sumControlPos(str fieldName, [int indent])
```

### <a name="parameters---sumcontrolpos"></a><span data-ttu-id="a6252-737">パラメーター - sumControlPos</span><span class="sxs-lookup"><span data-stu-id="a6252-737">Parameters - sumControlPos</span></span>

<span data-ttu-id="a6252-738">fieldName</span><span class="sxs-lookup"><span data-stu-id="a6252-738">fieldName</span></span>  

<!-- -->

<span data-ttu-id="a6252-739">インデント</span><span class="sxs-lookup"><span data-stu-id="a6252-739">indent</span></span>  

### <a name="return-value---sumcontrolpos"></a><span data-ttu-id="a6252-740">戻り値 - sumControlPos</span><span class="sxs-lookup"><span data-stu-id="a6252-740">Return Value - sumControlPos</span></span>

## <a name="method-sumdescription"></a><span data-ttu-id="a6252-741">メソッド sumDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-741">Method sumDescription</span></span>

```xpp
public str sumDescription()
```

### <a name="return-value---sumdescription"></a><span data-ttu-id="a6252-742">戻り値 - sumDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-742">Return Value - sumDescription</span></span>

## <a name="method-sumneg"></a><span data-ttu-id="a6252-743">メソッド sumNeg</span><span class="sxs-lookup"><span data-stu-id="a6252-743">Method sumNeg</span></span>

```xpp
public Real sumNeg(TableId tableId, FieldId fieldId, [int indent])
```

### <a name="parameters---sumneg"></a><span data-ttu-id="a6252-744">パラメーター - sumNeg</span><span class="sxs-lookup"><span data-stu-id="a6252-744">Parameters - sumNeg</span></span>

<span data-ttu-id="a6252-745">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-745">tableId</span></span>  

<!-- -->

<span data-ttu-id="a6252-746">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-746">fieldId</span></span>  

<!-- -->

<span data-ttu-id="a6252-747">インデント</span><span class="sxs-lookup"><span data-stu-id="a6252-747">indent</span></span>  

### <a name="return-value---sumneg"></a><span data-ttu-id="a6252-748">戻り値 - sumNeg</span><span class="sxs-lookup"><span data-stu-id="a6252-748">Return Value - sumNeg</span></span>

## <a name="method-sumpos"></a><span data-ttu-id="a6252-749">メソッド sumPos</span><span class="sxs-lookup"><span data-stu-id="a6252-749">Method sumPos</span></span>

```xpp
public Real sumPos(TableId tableId, FieldId fieldId, [int indent])
```

### <a name="parameters---sumpos"></a><span data-ttu-id="a6252-750">パラメーター - sumPos</span><span class="sxs-lookup"><span data-stu-id="a6252-750">Parameters - sumPos</span></span>

<span data-ttu-id="a6252-751">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-751">tableId</span></span>  

<!-- -->

<span data-ttu-id="a6252-752">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-752">fieldId</span></span>  

<!-- -->

<span data-ttu-id="a6252-753">インデント</span><span class="sxs-lookup"><span data-stu-id="a6252-753">indent</span></span>  

### <a name="return-value---sumpos"></a><span data-ttu-id="a6252-754">戻り値 - sumPos</span><span class="sxs-lookup"><span data-stu-id="a6252-754">Return Value - sumPos</span></span>

## <a name="method-suppressreportisemptymessage"></a><span data-ttu-id="a6252-755">メソッド suppressReportIsEmptyMessage</span><span class="sxs-lookup"><span data-stu-id="a6252-755">Method suppressReportIsEmptyMessage</span></span>

```xpp
public boolean suppressReportIsEmptyMessage([boolean suppress])
```

### <a name="parameters---suppressreportisemptymessage"></a><span data-ttu-id="a6252-756">パラメーター - suppressReportIsEmptyMessage</span><span class="sxs-lookup"><span data-stu-id="a6252-756">Parameters - suppressReportIsEmptyMessage</span></span>

<span data-ttu-id="a6252-757">suppress</span><span class="sxs-lookup"><span data-stu-id="a6252-757">suppress</span></span>  

### <a name="return-value---suppressreportisemptymessage"></a><span data-ttu-id="a6252-758">戻り値 - suppressReportIsEmptyMessage</span><span class="sxs-lookup"><span data-stu-id="a6252-758">Return Value - suppressReportIsEmptyMessage</span></span>

## <a name="method-title"></a><span data-ttu-id="a6252-759">メソッド title</span><span class="sxs-lookup"><span data-stu-id="a6252-759">Method title</span></span>

<span data-ttu-id="a6252-760">印刷ジョブの説明を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a6252-760">Gets or sets the print job description.</span></span>

```xpp
public str title([str title])
```

### <a name="parameters---title"></a><span data-ttu-id="a6252-761">パラメーター - title</span><span class="sxs-lookup"><span data-stu-id="a6252-761">Parameters - title</span></span>

<span data-ttu-id="a6252-762">タイトル</span><span class="sxs-lookup"><span data-stu-id="a6252-762">title</span></span>  
<span data-ttu-id="a6252-763">新しい printJobDescription 値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a6252-763">The new printJobDescription value; optional.</span></span>

### <a name="return-value---title"></a><span data-ttu-id="a6252-764">戻り値 - title</span><span class="sxs-lookup"><span data-stu-id="a6252-764">Return Value - title</span></span>

<span data-ttu-id="a6252-765">ジョブの説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="a6252-765">A string that contains the job description.</span></span>

### <a name="remarks---title"></a><span data-ttu-id="a6252-766">備考 - title</span><span class="sxs-lookup"><span data-stu-id="a6252-766">Remarks - title</span></span>

<span data-ttu-id="a6252-767">レポートが printArchive オブジェクトに書き込まれている場合、印刷ジョブの説明が printJobHeader テーブルの jobDescription フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-767">If reports are written to the printArchive object, the print job description is stored in the jobDescription field of the printJobHeader table.</span></span> <span data-ttu-id="a6252-768">レポートをプレビューすると、印刷ジョブの説明がキャプションとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-768">If the report is previewed, the print job description is used as the caption.</span></span> <span data-ttu-id="a6252-769">このメソッドは、レポートの実行中にカーネルから呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="a6252-769">This method is not called by the kernel during the execution of a report.</span></span> <span data-ttu-id="a6252-770">したがって、メソッドを上書きしても影響はありません。</span><span class="sxs-lookup"><span data-stu-id="a6252-770">Therefore, overriding the method will have no effect.</span></span>

## <a name="method-to"></a><span data-ttu-id="a6252-771">メソッド to</span><span class="sxs-lookup"><span data-stu-id="a6252-771">Method to</span></span>

```xpp
public int to([int toPage])
```

### <a name="parameters---to"></a><span data-ttu-id="a6252-772">パラメーター - to</span><span class="sxs-lookup"><span data-stu-id="a6252-772">Parameters - to</span></span>

<span data-ttu-id="a6252-773">toPage</span><span class="sxs-lookup"><span data-stu-id="a6252-773">toPage</span></span>  

### <a name="return-value---to"></a><span data-ttu-id="a6252-774">戻り値 - to</span><span class="sxs-lookup"><span data-stu-id="a6252-774">Return Value - to</span></span>

## <a name="method-tostring"></a><span data-ttu-id="a6252-775">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="a6252-775">Method toString</span></span>

<span data-ttu-id="a6252-776">クラスのテキストの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="a6252-776">Returns a textual description of the class.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="a6252-777">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="a6252-777">Return Value - toString</span></span>

<span data-ttu-id="a6252-778">クラスを説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="a6252-778">A string that describes the class.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="a6252-779">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="a6252-779">Remarks - toString</span></span>

<span data-ttu-id="a6252-780">ほとんどのクラスについては、toString メソッドがクラス ハンドルおよび名前を含む文字列を返しますが、一部のクラスでは文字列で詳細情報が返されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-780">For most classes the toString method returns a string that contains the class handle and name, but for some classes more information is returned in the string.</span></span>

## <a name="method-unpackpagesettings"></a><span data-ttu-id="a6252-781">メソッド unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-781">Method unpackPageSettings</span></span>

```xpp
public boolean unpackPageSettings(container packedPageSetup)
```

### <a name="parameters---unpackpagesettings"></a><span data-ttu-id="a6252-782">パラメーター - unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-782">Parameters - unpackPageSettings</span></span>

<span data-ttu-id="a6252-783">packedPageSetup</span><span class="sxs-lookup"><span data-stu-id="a6252-783">packedPageSetup</span></span>  

### <a name="return-value---unpackpagesettings"></a><span data-ttu-id="a6252-784">戻り値 - unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-784">Return Value - unpackPageSettings</span></span>

## <a name="method-unpackprintersettings"></a><span data-ttu-id="a6252-785">メソッド unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-785">Method unpackPrinterSettings</span></span>

```xpp
public boolean unpackPrinterSettings(container packedPrinterSetup)
```

### <a name="parameters---unpackprintersettings"></a><span data-ttu-id="a6252-786">パラメーター - unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-786">Parameters - unpackPrinterSettings</span></span>

<span data-ttu-id="a6252-787">packedPrinterSetup</span><span class="sxs-lookup"><span data-stu-id="a6252-787">packedPrinterSetup</span></span>  

### <a name="return-value---unpackprintersettings"></a><span data-ttu-id="a6252-788">戻り値 - unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-788">Return Value - unpackPrinterSettings</span></span>

## <a name="method-unpackprintjobsettings"></a><span data-ttu-id="a6252-789">メソッド unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-789">Method unpackPrintJobSettings</span></span>

```xpp
public boolean unpackPrintJobSettings(container packedPrintJobSettings)
```

### <a name="parameters---unpackprintjobsettings"></a><span data-ttu-id="a6252-790">パラメーター - unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-790">Parameters - unpackPrintJobSettings</span></span>

<span data-ttu-id="a6252-791">packedPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-791">packedPrintJobSettings</span></span>  

### <a name="return-value---unpackprintjobsettings"></a><span data-ttu-id="a6252-792">戻り値 - unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-792">Return Value - unpackPrintJobSettings</span></span>

## <a name="method-unpacksubtotalsettings"></a><span data-ttu-id="a6252-793">メソッド unpackSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-793">Method unpackSubtotalSettings</span></span>

```xpp
public boolean unpackSubtotalSettings(container packedSubtotalSetup)
```

### <a name="parameters---unpacksubtotalsettings"></a><span data-ttu-id="a6252-794">パラメーター - unpackSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-794">Parameters - unpackSubtotalSettings</span></span>

<span data-ttu-id="a6252-795">packedSubtotalSetup</span><span class="sxs-lookup"><span data-stu-id="a6252-795">packedSubtotalSetup</span></span>  

### <a name="return-value---unpacksubtotalsettings"></a><span data-ttu-id="a6252-796">戻り値 - unpackSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="a6252-796">Return Value - unpackSubtotalSettings</span></span>

## <a name="method-userselectedorientation"></a><span data-ttu-id="a6252-797">メソッド userSelectedOrientation</span><span class="sxs-lookup"><span data-stu-id="a6252-797">Method userSelectedOrientation</span></span>

```xpp
public PrinterOrientation userSelectedOrientation()
```

### <a name="return-value---userselectedorientation"></a><span data-ttu-id="a6252-798">戻り値 - userSelectedOrientation</span><span class="sxs-lookup"><span data-stu-id="a6252-798">Return Value - userSelectedOrientation</span></span>

## <a name="method-disablebody"></a><span data-ttu-id="a6252-799">メソッド disableBody</span><span class="sxs-lookup"><span data-stu-id="a6252-799">Method disableBody</span></span>

```xpp
public void disableBody([TableId tableId])
```

### <a name="parameters---disablebody"></a><span data-ttu-id="a6252-800">パラメーター - disableBody</span><span class="sxs-lookup"><span data-stu-id="a6252-800">Parameters - disableBody</span></span>

<span data-ttu-id="a6252-801">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-801">tableId</span></span>  

## <a name="method-attach"></a><span data-ttu-id="a6252-802">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="a6252-802">Method attach</span></span>

```xpp
public void attach()
```

## <a name="method-new"></a><span data-ttu-id="a6252-803">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a6252-803">Method new</span></span>

<span data-ttu-id="a6252-804">ReportRun クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a6252-804">Initializes an instance of the ReportRun class.</span></span>

```xpp
public void new(AnyType argsOrReportOrContainer, [str designName], [boolean isWebReport])
```

### <a name="parameters---new"></a><span data-ttu-id="a6252-805">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="a6252-805">Parameters - new</span></span>

<span data-ttu-id="a6252-806">argsOrReportOrContainer</span><span class="sxs-lookup"><span data-stu-id="a6252-806">argsOrReportOrContainer</span></span>  

<!-- -->

<span data-ttu-id="a6252-807">designName</span><span class="sxs-lookup"><span data-stu-id="a6252-807">designName</span></span>  

<!-- -->

<span data-ttu-id="a6252-808">isWebReport</span><span class="sxs-lookup"><span data-stu-id="a6252-808">isWebReport</span></span>  

## <a name="method-disablesection"></a><span data-ttu-id="a6252-809">メソッド disableSection</span><span class="sxs-lookup"><span data-stu-id="a6252-809">Method disableSection</span></span>

```xpp
public void disableSection(ReportSection section)
```

### <a name="parameters---disablesection"></a><span data-ttu-id="a6252-810">パラメーター - disableSection</span><span class="sxs-lookup"><span data-stu-id="a6252-810">Parameters - disableSection</span></span>

<span data-ttu-id="a6252-811">セクション</span><span class="sxs-lookup"><span data-stu-id="a6252-811">section</span></span>  

## <a name="method-arrangelevelglobal"></a><span data-ttu-id="a6252-812">メソッド arrangeLevelGlobal</span><span class="sxs-lookup"><span data-stu-id="a6252-812">Method arrangeLevelGlobal</span></span>

```xpp
public void arrangeLevelGlobal()
```

## <a name="method-setescapesequence"></a><span data-ttu-id="a6252-813">メソッド setEscapeSequence</span><span class="sxs-lookup"><span data-stu-id="a6252-813">Method setEscapeSequence</span></span>

```xpp
public void setEscapeSequence(str str)
```

### <a name="parameters---setescapesequence"></a><span data-ttu-id="a6252-814">パラメーター - setEscapeSequence</span><span class="sxs-lookup"><span data-stu-id="a6252-814">Parameters - setEscapeSequence</span></span>

<span data-ttu-id="a6252-815">str</span><span class="sxs-lookup"><span data-stu-id="a6252-815">str</span></span>  

## <a name="method-enablebody"></a><span data-ttu-id="a6252-816">メソッド enableBody</span><span class="sxs-lookup"><span data-stu-id="a6252-816">Method enableBody</span></span>

```xpp
public void enableBody([TableId tableId])
```

### <a name="parameters---enablebody"></a><span data-ttu-id="a6252-817">パラメーター - enableBody</span><span class="sxs-lookup"><span data-stu-id="a6252-817">Parameters - enableBody</span></span>

<span data-ttu-id="a6252-818">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-818">tableId</span></span>  

## <a name="method-clearallrangedescriptions"></a><span data-ttu-id="a6252-819">メソッド clearAllRangeDescriptions</span><span class="sxs-lookup"><span data-stu-id="a6252-819">Method clearAllRangeDescriptions</span></span>

```xpp
public void clearAllRangeDescriptions()
```

## <a name="method-header"></a><span data-ttu-id="a6252-820">メソッド header</span><span class="sxs-lookup"><span data-stu-id="a6252-820">Method header</span></span>

<span data-ttu-id="a6252-821">ヘッダーを制御します。</span><span class="sxs-lookup"><span data-stu-id="a6252-821">Controls the header.</span></span>

```xpp
public void header(ReportSection headerSection, TableId tableId, FieldId fieldId)
```

### <a name="parameters---header"></a><span data-ttu-id="a6252-822">パラメーター - header</span><span class="sxs-lookup"><span data-stu-id="a6252-822">Parameters - header</span></span>

<span data-ttu-id="a6252-823">headerSection</span><span class="sxs-lookup"><span data-stu-id="a6252-823">headerSection</span></span>  
<span data-ttu-id="a6252-824">変更された値を含むフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="a6252-824">The ID of the field that contains the changed value.</span></span>

<!-- -->

<span data-ttu-id="a6252-825">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-825">tableId</span></span>  
<span data-ttu-id="a6252-826">変更された値を含むフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="a6252-826">The ID of the field that contains the changed value.</span></span>

<!-- -->

<span data-ttu-id="a6252-827">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-827">fieldId</span></span>  
<span data-ttu-id="a6252-828">変更された値を含むフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="a6252-828">The ID of the field that contains the changed value.</span></span>

### <a name="remarks---header"></a><span data-ttu-id="a6252-829">備考 - header</span><span class="sxs-lookup"><span data-stu-id="a6252-829">Remarks - header</span></span>

<span data-ttu-id="a6252-830">このメソッドは、フッター メソッドと同様に機能しますが、レコード グループの前に呼び出される点が異なりますが、フッター メソッドはレコード グループの後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-830">This method works just like the footer method, except it is called before a group of records, whereas the footer method is called after a group of records.</span></span>

## <a name="method-unpackdesign"></a><span data-ttu-id="a6252-831">メソッド unpackDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-831">Method unpackDesign</span></span>

```xpp
public void unpackDesign(container packedDesign)
```

### <a name="parameters---unpackdesign"></a><span data-ttu-id="a6252-832">パラメーター - unpackDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-832">Parameters - unpackDesign</span></span>

<span data-ttu-id="a6252-833">packedDesign</span><span class="sxs-lookup"><span data-stu-id="a6252-833">packedDesign</span></span>  

## <a name="method-newpage"></a><span data-ttu-id="a6252-834">メソッド newPage</span><span class="sxs-lookup"><span data-stu-id="a6252-834">Method newPage</span></span>

```xpp
public void newPage([boolean doPageFooter])
```

### <a name="parameters---newpage"></a><span data-ttu-id="a6252-835">パラメーター - newPage</span><span class="sxs-lookup"><span data-stu-id="a6252-835">Parameters - newPage</span></span>

<span data-ttu-id="a6252-836">doPageFooter</span><span class="sxs-lookup"><span data-stu-id="a6252-836">doPageFooter</span></span>  

## <a name="method-footer"></a><span data-ttu-id="a6252-837">メソッド footer</span><span class="sxs-lookup"><span data-stu-id="a6252-837">Method footer</span></span>

<span data-ttu-id="a6252-838">フッターを制御します。</span><span class="sxs-lookup"><span data-stu-id="a6252-838">Controls the footer.</span></span>

```xpp
public void footer(ReportSection footerSection, TableId tableId, FieldId fieldId)
```

### <a name="parameters---footer"></a><span data-ttu-id="a6252-839">パラメーター - footer</span><span class="sxs-lookup"><span data-stu-id="a6252-839">Parameters - footer</span></span>

<span data-ttu-id="a6252-840">footerSection</span><span class="sxs-lookup"><span data-stu-id="a6252-840">footerSection</span></span>  
<span data-ttu-id="a6252-841">変更された値を含むフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="a6252-841">The ID of the field that contains the changed value.</span></span>

<!-- -->

<span data-ttu-id="a6252-842">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-842">tableId</span></span>  
<span data-ttu-id="a6252-843">変更された値を含むフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="a6252-843">The ID of the field that contains the changed value.</span></span>

<!-- -->

<span data-ttu-id="a6252-844">fieldId</span><span class="sxs-lookup"><span data-stu-id="a6252-844">fieldId</span></span>  
<span data-ttu-id="a6252-845">変更された値を含むフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="a6252-845">The ID of the field that contains the changed value.</span></span>

### <a name="remarks---footer"></a><span data-ttu-id="a6252-846">備考 - footer</span><span class="sxs-lookup"><span data-stu-id="a6252-846">Remarks - footer</span></span>

<span data-ttu-id="a6252-847">このメソッドは、ユーザーがヘッダーまたはフッターを印刷しないように選択した場合でも、値が変更された後にフィールドがソートされたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-847">This method is called when a field is sorted after it changes value, even if the user has chosen not to print headers or footers.</span></span> <span data-ttu-id="a6252-848">送信メソッドを 1 回呼び出すと、複数のフッター セクションとヘッダー セクションの印刷を本文セクションの前にトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="a6252-848">One call of the send method can trigger the printing of multiple footer sections and header sections before the body sections.</span></span> <span data-ttu-id="a6252-849">ヘッダーおよびフッター メソッドを使用すると、ユーザーはヘッダーまたはフッターを印刷する前または後にコードを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a6252-849">The header and footer methods allow the user to execute code before or after printing the header or footer.</span></span>

## <a name="method-reset"></a><span data-ttu-id="a6252-850">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="a6252-850">Method reset</span></span>

<span data-ttu-id="a6252-851">複数のレポートを作成する ReportRun クラスの単一インスタンスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a6252-851">Enables a single instance of the ReportRun class to create multiple reports.</span></span>

```xpp
public void reset([boolean delayExceptions])
```

### <a name="parameters---reset"></a><span data-ttu-id="a6252-852">パラメーター - reset</span><span class="sxs-lookup"><span data-stu-id="a6252-852">Parameters - reset</span></span>

<span data-ttu-id="a6252-853">delayExceptions</span><span class="sxs-lookup"><span data-stu-id="a6252-853">delayExceptions</span></span>  

## <a name="method-arrangelevelnone"></a><span data-ttu-id="a6252-854">メソッド arrangeLevelNone</span><span class="sxs-lookup"><span data-stu-id="a6252-854">Method arrangeLevelNone</span></span>

```xpp
public void arrangeLevelNone()
```

## <a name="method-run"></a><span data-ttu-id="a6252-855">メソッド run</span><span class="sxs-lookup"><span data-stu-id="a6252-855">Method run</span></span>

<span data-ttu-id="a6252-856">レポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6252-856">Runs the report.</span></span>

```xpp
public void run()
```

### <a name="remarks---run"></a><span data-ttu-id="a6252-857">備考 - run</span><span class="sxs-lookup"><span data-stu-id="a6252-857">Remarks - run</span></span>

<span data-ttu-id="a6252-858">このメソッドで super メソッドを呼び出すと、次のメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6252-858">The call to the super method in this method calls the following methods:</span></span>

-   <span data-ttu-id="a6252-859">prompt - ユーザーが sysPrintForm フォームでプリンターを選択することができます</span><span class="sxs-lookup"><span data-stu-id="a6252-859">prompt - Lets the user select the printer in the sysPrintForm form</span></span>
-   <span data-ttu-id="a6252-860">fetch - レポート クエリを実行します</span><span class="sxs-lookup"><span data-stu-id="a6252-860">fetch - Runs the report query</span></span>
-   <span data-ttu-id="a6252-861">print - レポートをプリンターまたはディスプレイに導きます。</span><span class="sxs-lookup"><span data-stu-id="a6252-861">print - Directs the report to the printer or display.</span></span>

## <a name="method-gotoymm100"></a><span data-ttu-id="a6252-862">メソッド gotoYmm100</span><span class="sxs-lookup"><span data-stu-id="a6252-862">Method gotoYmm100</span></span>

```xpp
public void gotoYmm100([int mm100])
```

### <a name="parameters---gotoymm100"></a><span data-ttu-id="a6252-863">パラメーター - gotoYmm100</span><span class="sxs-lookup"><span data-stu-id="a6252-863">Parameters - gotoYmm100</span></span>

<span data-ttu-id="a6252-864">mm100</span><span class="sxs-lookup"><span data-stu-id="a6252-864">mm100</span></span>  

## <a name="method-disablecolumnheadings"></a><span data-ttu-id="a6252-865">メソッド disableColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-865">Method disableColumnHeadings</span></span>

```xpp
public void disableColumnHeadings([TableId tableId])
```

### <a name="parameters---disablecolumnheadings"></a><span data-ttu-id="a6252-866">パラメーター - disableColumnHeadings</span><span class="sxs-lookup"><span data-stu-id="a6252-866">Parameters - disableColumnHeadings</span></span>

<span data-ttu-id="a6252-867">tableId</span><span class="sxs-lookup"><span data-stu-id="a6252-867">tableId</span></span>  

## <a name="method-enablepagefooter"></a><span data-ttu-id="a6252-868">メソッド enablePageFooter</span><span class="sxs-lookup"><span data-stu-id="a6252-868">Method enablePageFooter</span></span>

```xpp
public void enablePageFooter()
```

## <a name="method-init"></a><span data-ttu-id="a6252-869">メソッド init</span><span class="sxs-lookup"><span data-stu-id="a6252-869">Method init</span></span>

```xpp
public void init()
```

## <a name="method-arrangelevelcontrol"></a><span data-ttu-id="a6252-870">メソッド arrangeLevelControl</span><span class="sxs-lookup"><span data-stu-id="a6252-870">Method arrangeLevelControl</span></span>

```xpp
public void arrangeLevelControl()
```

## <a name="method-disablepagefooter"></a><span data-ttu-id="a6252-871">メソッド disablePageFooter</span><span class="sxs-lookup"><span data-stu-id="a6252-871">Method disablePageFooter</span></span>

```xpp
public void disablePageFooter()
```

## <a name="method-addpendingsums"></a><span data-ttu-id="a6252-872">メソッド addPendingSums</span><span class="sxs-lookup"><span data-stu-id="a6252-872">Method addPendingSums</span></span>

<span data-ttu-id="a6252-873">レポートの関連するフッターを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a6252-873">Prints the relevant footers of the report.</span></span>

```xpp
public void addPendingSums()
```

### <a name="remarks---addpendingsums"></a><span data-ttu-id="a6252-874">備考 - addPendingSums</span><span class="sxs-lookup"><span data-stu-id="a6252-874">Remarks - addPendingSums</span></span>

<span data-ttu-id="a6252-875">このメソッドは、フェッチ メソッドが複数回呼び出されたレポートでのみ呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6252-875">This method should only be called in reports where the fetch method is called more than once.</span></span>

## <a name="method-arrangelevelsection"></a><span data-ttu-id="a6252-876">メソッド arrangeLevelSection</span><span class="sxs-lookup"><span data-stu-id="a6252-876">Method arrangeLevelSection</span></span>

```xpp
public void arrangeLevelSection()
```

## <a name="method-enablesection"></a><span data-ttu-id="a6252-877">メソッド enableSection</span><span class="sxs-lookup"><span data-stu-id="a6252-877">Method enableSection</span></span>

```xpp
public void enableSection(ReportSection section)
```

### <a name="parameters---enablesection"></a><span data-ttu-id="a6252-878">パラメーター - enableSection</span><span class="sxs-lookup"><span data-stu-id="a6252-878">Parameters - enableSection</span></span>

<span data-ttu-id="a6252-879">セクション</span><span class="sxs-lookup"><span data-stu-id="a6252-879">section</span></span>  

## <a name="method-detach"></a><span data-ttu-id="a6252-880">メソッド detach</span><span class="sxs-lookup"><span data-stu-id="a6252-880">Method detach</span></span>

```xpp
public void detach()
```

## <a name="method-addrangedescription"></a><span data-ttu-id="a6252-881">メソッド addRangeDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-881">Method addRangeDescription</span></span>

```xpp
public void addRangeDescription(int x, int y, str text, [str fontName], [int fontSize])
```

### <a name="parameters---addrangedescription"></a><span data-ttu-id="a6252-882">パラメーター - addRangeDescription</span><span class="sxs-lookup"><span data-stu-id="a6252-882">Parameters - addRangeDescription</span></span>

<span data-ttu-id="a6252-883">x</span><span class="sxs-lookup"><span data-stu-id="a6252-883">x</span></span>  

<!-- -->

<span data-ttu-id="a6252-884">y</span><span class="sxs-lookup"><span data-stu-id="a6252-884">y</span></span>  

<!-- -->

<span data-ttu-id="a6252-885">テキスト</span><span class="sxs-lookup"><span data-stu-id="a6252-885">text</span></span>  

<!-- -->

<span data-ttu-id="a6252-886">fontName</span><span class="sxs-lookup"><span data-stu-id="a6252-886">fontName</span></span>  

<!-- -->

<span data-ttu-id="a6252-887">fontSize</span><span class="sxs-lookup"><span data-stu-id="a6252-887">fontSize</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="a6252-888">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="a6252-888">Method finalize</span></span>

```xpp
public void finalize()
```

