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
# <a name="class-reportoutputuser"></a><span data-ttu-id="14dee-103">クラス ReportOutputUser</span><span class="sxs-lookup"><span data-stu-id="14dee-103">Class ReportOutputUser</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportOutputUser extends ReportOutput
```

<span data-ttu-id="14dee-104">ReportOutputUser クラスは、レポートの形式のユーザー定義のターゲットを実装します。</span><span class="sxs-lookup"><span data-stu-id="14dee-104">The ReportOutputUser class implements a user-defined target for report formatting.</span></span>

## <a name="remarks"></a><span data-ttu-id="14dee-105">備考</span><span class="sxs-lookup"><span data-stu-id="14dee-105">Remarks</span></span>

<span data-ttu-id="14dee-106">既定では、画面、プリンター、ファイル、または電子メール アドレスにレポートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="14dee-106">By default, reports are printed to a screen, printer, file, or email address.</span></span> <span data-ttu-id="14dee-107">次の API アイテムは、ユーザー定義ノターゲットをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="14dee-107">The following API items support a user-defined target:</span></span>

-   <span data-ttu-id="14dee-108">ReportOutputUserType システム列挙</span><span class="sxs-lookup"><span data-stu-id="14dee-108">ReportOutputUserType system enumeration</span></span>
-   <span data-ttu-id="14dee-109">PrintMedium システム列挙型の ViewerClass 値</span><span class="sxs-lookup"><span data-stu-id="14dee-109">ViewerClass value for the PrintMedium system enumeration</span></span>
-   <span data-ttu-id="14dee-110">ClassFactory::createViewer メソッド</span><span class="sxs-lookup"><span data-stu-id="14dee-110">ClassFactory::createViewer method</span></span>

<span data-ttu-id="14dee-111">レポートが実行されると、ターゲットが PrintMedium::Viewer クラスの場合、Print メソッドによって reportOutputUser オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="14dee-111">When a report is run, the print method creates a reportOutputUser object if the target is PrintMedium::Viewer class.</span></span> <span data-ttu-id="14dee-112">このオブジェクトは、createViewer メソッドを呼び出し、reportOutputUserType を引数の 1 つとして指定することによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="14dee-112">This object will be created by calling the createViewer method and giving reportOutputUserType as one of the arguments.</span></span> <span data-ttu-id="14dee-113">その後、レポートは、オブジェクトのメソッド (startReport、startPage、startSection、writeField など) を呼び出すことによって出力されます。</span><span class="sxs-lookup"><span data-stu-id="14dee-113">The report will then be printed by calling methods on the object: startReport, startPage, startSection, writeField, and so on.</span></span> <span data-ttu-id="14dee-114">一般に、ターゲットが、たとえばプリンターである場合、reportRun::print メソッドは reportOutput オブジェクトを作成し、印刷メソッドを呼び出してプリンターでレポートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="14dee-114">In general, if the target is, for example, a printer, the reportRun::print method will create a reportOutput object and call its print method to print the report to a printer.</span></span> <span data-ttu-id="14dee-115">ターゲットが viewerClass の場合、createViewer メソッドが呼び出され、ReportOutputUser オブジェクトが取得されます。</span><span class="sxs-lookup"><span data-stu-id="14dee-115">If the target is viewerClass, it will instead call the createViewer method to get a ReportOutputUser object.</span></span> <span data-ttu-id="14dee-116">次に、オブジェクトのメソッド (startReport、startPage、startSection、startField、outputStringField など) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="14dee-116">Then it will call methods on the object: startReport, startPage, startSection, startField, outputStringField, and so on.</span></span> <span data-ttu-id="14dee-117">レポートが実行されると、レポートのテキスト コントロールの Text プロパティが印刷ウィンドウに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="14dee-117">When the report is run, the Text property of the text controls of the report will be written to the print window.</span></span>

## <a name="examples"></a><span data-ttu-id="14dee-118">例</span><span class="sxs-lookup"><span data-stu-id="14dee-118">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="14dee-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="14dee-119">Methods</span></span>

| <span data-ttu-id="14dee-120">方法</span><span class="sxs-lookup"><span data-stu-id="14dee-120">Method</span></span>                                                                                            | <span data-ttu-id="14dee-121">説明</span><span class="sxs-lookup"><span data-stu-id="14dee-121">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="14dee-122">public boolean pageCreated(int page)</span><span class="sxs-lookup"><span data-stu-id="14dee-122">public boolean pageCreated(int page)</span></span>                                                              |                                                 |
| <span data-ttu-id="14dee-123">public str result()</span><span class="sxs-lookup"><span data-stu-id="14dee-123">public str result()</span></span>                                                                               |                                                 |
| <span data-ttu-id="14dee-124">public void writeAutoLabel(OutputAutoLabelField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-124">public void writeAutoLabel(OutputAutoLabelField field, OuputSection section)</span></span>                      |                                                 |
| <span data-ttu-id="14dee-125">public void endHeaderSection(OutputHeaderSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-125">public void endHeaderSection(OutputHeaderSection section)</span></span>                                         |                                                 |
| <span data-ttu-id="14dee-126">public void writeString(OutputStringField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-126">public void writeString(OutputStringField field, OuputSection section)</span></span>                            |                                                 |
| <span data-ttu-id="14dee-127">public void endPageHeaderSection(OutputPageHeaderSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-127">public void endPageHeaderSection(OutputPageHeaderSection section)</span></span>                                 |                                                 |
| <span data-ttu-id="14dee-128">public void writeBitmap(OutputBitmapField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-128">public void writeBitmap(OutputBitmapField field, OuputSection section)</span></span>                            |                                                 |
| <span data-ttu-id="14dee-129">public void endBodySection(OutputBodySection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-129">public void endBodySection(OutputBodySection section)</span></span>                                             |                                                 |
| <span data-ttu-id="14dee-130">public void startPageHeaderSection(OutputPageHeaderSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-130">public void startPageHeaderSection(OutputPageHeaderSection section)</span></span>                               |                                                 |
| <span data-ttu-id="14dee-131">public void printViaClass()</span><span class="sxs-lookup"><span data-stu-id="14dee-131">public void printViaClass()</span></span>                                                                       |                                                 |
| <span data-ttu-id="14dee-132">public void endPageFooterSection(OutputPageFooterSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-132">public void endPageFooterSection(OutputPageFooterSection section)</span></span>                                 |                                                 |
| <span data-ttu-id="14dee-133">public void writeReal(OutputRealField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-133">public void writeReal(OutputRealField field, OuputSection section)</span></span>                                |                                                 |
| <span data-ttu-id="14dee-134">public void startColumnHeadingsSection(OutputColumnHeadingsSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-134">public void startColumnHeadingsSection(OutputColumnHeadingsSection section)</span></span>                       |                                                 |
| <span data-ttu-id="14dee-135">public void writeShape(OutputShapeField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-135">public void writeShape(OutputShapeField field, OuputSection section)</span></span>                              |                                                 |
| <span data-ttu-id="14dee-136">public void writeDateTime(OutputDateTimeField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-136">public void writeDateTime(OutputDateTimeField field, OuputSection section)</span></span>                        |                                                 |
| <span data-ttu-id="14dee-137">public void writeStaticText(OutputStaticTextField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-137">public void writeStaticText(OutputStaticTextField field, OuputSection section)</span></span>                    |                                                 |
| <span data-ttu-id="14dee-138">public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\], \[container settings\])</span><span class="sxs-lookup"><span data-stu-id="14dee-138">public void new(PrintJobHeader jobsCursor, \[PrintJobPages pagesCursor\], \[container settings\])</span></span> | <span data-ttu-id="14dee-139">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14dee-139">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="14dee-140">public void writeInteger(OutputIntegerField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-140">public void writeInteger(OutputIntegerField field, OuputSection section)</span></span>                          |                                                 |
| <span data-ttu-id="14dee-141">public void startColumnSection()</span><span class="sxs-lookup"><span data-stu-id="14dee-141">public void startColumnSection()</span></span>                                                                  |                                                 |
| <span data-ttu-id="14dee-142">public void startSection(OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-142">public void startSection(OuputSection section)</span></span>                                                    |                                                 |
| <span data-ttu-id="14dee-143">public void writeDate(OutputDateField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-143">public void writeDate(OutputDateField field, OuputSection section)</span></span>                                |                                                 |
| <span data-ttu-id="14dee-144">public void pagesTotal(int pagesTotal)</span><span class="sxs-lookup"><span data-stu-id="14dee-144">public void pagesTotal(int pagesTotal)</span></span>                                                            |                                                 |
| <span data-ttu-id="14dee-145">public void writeInt64(OutputInt64Field field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-145">public void writeInt64(OutputInt64Field field, OuputSection section)</span></span>                              |                                                 |
| <span data-ttu-id="14dee-146">public void endReport(PrintJobStatus printJobStatus)</span><span class="sxs-lookup"><span data-stu-id="14dee-146">public void endReport(PrintJobStatus printJobStatus)</span></span>                                              |                                                 |
| <span data-ttu-id="14dee-147">public void endColumnSection()</span><span class="sxs-lookup"><span data-stu-id="14dee-147">public void endColumnSection()</span></span>                                                                    |                                                 |
| <span data-ttu-id="14dee-148">public void startReport(PrintJobSettings printJobSettings)</span><span class="sxs-lookup"><span data-stu-id="14dee-148">public void startReport(PrintJobSettings printJobSettings)</span></span>                                        |                                                 |
| <span data-ttu-id="14dee-149">public void printPageViaClass(int page)</span><span class="sxs-lookup"><span data-stu-id="14dee-149">public void printPageViaClass(int page)</span></span>                                                           |                                                 |
| <span data-ttu-id="14dee-150">public void endEpilogSection(OutputEpilogSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-150">public void endEpilogSection(OutputEpilogSection section)</span></span>                                         |                                                 |
| <span data-ttu-id="14dee-151">public void endPrologSection(OutputPrologSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-151">public void endPrologSection(OutputPrologSection section)</span></span>                                         |                                                 |
| <span data-ttu-id="14dee-152">public void endPage()</span><span class="sxs-lookup"><span data-stu-id="14dee-152">public void endPage()</span></span>                                                                             |                                                 |
| <span data-ttu-id="14dee-153">public void startFooterSection(OutputFooterSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-153">public void startFooterSection(OutputFooterSection section)</span></span>                                       |                                                 |
| <span data-ttu-id="14dee-154">public void endProgrammableSection(OutputProgrammableSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-154">public void endProgrammableSection(OutputProgrammableSection section)</span></span>                             |                                                 |
| <span data-ttu-id="14dee-155">public void startBodySection(OutputBodySection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-155">public void startBodySection(OutputBodySection section)</span></span>                                           |                                                 |
| <span data-ttu-id="14dee-156">public void endSection(OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-156">public void endSection(OuputSection section)</span></span>                                                      |                                                 |
| <span data-ttu-id="14dee-157">public void startProgrammableSection(OutputProgrammableSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-157">public void startProgrammableSection(OutputProgrammableSection section)</span></span>                           |                                                 |
| <span data-ttu-id="14dee-158">public void startEpilogSection(OutputEpilogSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-158">public void startEpilogSection(OutputEpilogSection section)</span></span>                                       |                                                 |
| <span data-ttu-id="14dee-159">public void startHeaderSection(OutputHeaderSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-159">public void startHeaderSection(OutputHeaderSection section)</span></span>                                       |                                                 |
| <span data-ttu-id="14dee-160">public void endColumnHeadingsSection(OutputColumnHeadingsSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-160">public void endColumnHeadingsSection(OutputColumnHeadingsSection section)</span></span>                         |                                                 |
| <span data-ttu-id="14dee-161">public void writeLabel(OutputLabelField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-161">public void writeLabel(OutputLabelField field, OuputSection section)</span></span>                              |                                                 |
| <span data-ttu-id="14dee-162">public void endFooterSection(OutputFooterSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-162">public void endFooterSection(OutputFooterSection section)</span></span>                                         |                                                 |
| <span data-ttu-id="14dee-163">public void writeField(OutputField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-163">public void writeField(OutputField field, OuputSection section)</span></span>                                   |                                                 |
| <span data-ttu-id="14dee-164">public void writeEnum(OutputEnumField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-164">public void writeEnum(OutputEnumField field, OuputSection section)</span></span>                                |                                                 |
| <span data-ttu-id="14dee-165">public void startPageFooterSection(OutputPageFooterSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-165">public void startPageFooterSection(OutputPageFooterSection section)</span></span>                               |                                                 |
| <span data-ttu-id="14dee-166">public void writeSum(OutputSumField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-166">public void writeSum(OutputSumField field, OuputSection section)</span></span>                                  |                                                 |
| <span data-ttu-id="14dee-167">public void writeTime(OutputTimeField field, OuputSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-167">public void writeTime(OutputTimeField field, OuputSection section)</span></span>                                |                                                 |
| <span data-ttu-id="14dee-168">public void startPage(OutputPage page)</span><span class="sxs-lookup"><span data-stu-id="14dee-168">public void startPage(OutputPage page)</span></span>                                                            |                                                 |
| <span data-ttu-id="14dee-169">public void startPrologSection(OutputPrologSection section)</span><span class="sxs-lookup"><span data-stu-id="14dee-169">public void startPrologSection(OutputPrologSection section)</span></span>                                       |                                                 |

## <a name="method-pagecreated"></a><span data-ttu-id="14dee-170">メソッド pageCreated</span><span class="sxs-lookup"><span data-stu-id="14dee-170">Method pageCreated</span></span>

```xpp
public boolean pageCreated(int page)
```

### <a name="parameters---pagecreated"></a><span data-ttu-id="14dee-171">パラメーター - pageCreated</span><span class="sxs-lookup"><span data-stu-id="14dee-171">Parameters - pageCreated</span></span>

<span data-ttu-id="14dee-172">ページ</span><span class="sxs-lookup"><span data-stu-id="14dee-172">page</span></span>  

### <a name="return-value---pagecreated"></a><span data-ttu-id="14dee-173">戻り値 - pageCreated</span><span class="sxs-lookup"><span data-stu-id="14dee-173">Return Value - pageCreated</span></span>

## <a name="method-result"></a><span data-ttu-id="14dee-174">メソッド result</span><span class="sxs-lookup"><span data-stu-id="14dee-174">Method result</span></span>

```xpp
public str result()
```

### <a name="return-value---result"></a><span data-ttu-id="14dee-175">戻り値 - result</span><span class="sxs-lookup"><span data-stu-id="14dee-175">Return Value - result</span></span>

## <a name="method-writeautolabel"></a><span data-ttu-id="14dee-176">メソッド writeAutoLabel</span><span class="sxs-lookup"><span data-stu-id="14dee-176">Method writeAutoLabel</span></span>

```xpp
public void writeAutoLabel(OutputAutoLabelField field, OuputSection section)
```

### <a name="parameters---writeautolabel"></a><span data-ttu-id="14dee-177">パラメーター - writeAutoLabel</span><span class="sxs-lookup"><span data-stu-id="14dee-177">Parameters - writeAutoLabel</span></span>

<span data-ttu-id="14dee-178"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-178">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-179">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-179">section</span></span>  

## <a name="method-endheadersection"></a><span data-ttu-id="14dee-180">メソッド endHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-180">Method endHeaderSection</span></span>

```xpp
public void endHeaderSection(OutputHeaderSection section)
```

### <a name="parameters---endheadersection"></a><span data-ttu-id="14dee-181">パラメーター - endHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-181">Parameters - endHeaderSection</span></span>

<span data-ttu-id="14dee-182">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-182">section</span></span>  

## <a name="method-writestring"></a><span data-ttu-id="14dee-183">メソッド writeString</span><span class="sxs-lookup"><span data-stu-id="14dee-183">Method writeString</span></span>

```xpp
public void writeString(OutputStringField field, OuputSection section)
```

### <a name="parameters---writestring"></a><span data-ttu-id="14dee-184">パラメーター - writeString</span><span class="sxs-lookup"><span data-stu-id="14dee-184">Parameters - writeString</span></span>

<span data-ttu-id="14dee-185"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-185">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-186">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-186">section</span></span>  

## <a name="method-endpageheadersection"></a><span data-ttu-id="14dee-187">メソッド endPageHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-187">Method endPageHeaderSection</span></span>

```xpp
public void endPageHeaderSection(OutputPageHeaderSection section)
```

### <a name="parameters---endpageheadersection"></a><span data-ttu-id="14dee-188">パラメーター - endPageHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-188">Parameters - endPageHeaderSection</span></span>

<span data-ttu-id="14dee-189">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-189">section</span></span>  

## <a name="method-writebitmap"></a><span data-ttu-id="14dee-190">メソッド writeBitmap</span><span class="sxs-lookup"><span data-stu-id="14dee-190">Method writeBitmap</span></span>

```xpp
public void writeBitmap(OutputBitmapField field, OuputSection section)
```

### <a name="parameters---writebitmap"></a><span data-ttu-id="14dee-191">パラメーター - writeBitmap</span><span class="sxs-lookup"><span data-stu-id="14dee-191">Parameters - writeBitmap</span></span>

<span data-ttu-id="14dee-192"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-192">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-193">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-193">section</span></span>  

## <a name="method-endbodysection"></a><span data-ttu-id="14dee-194">メソッド endBodySection</span><span class="sxs-lookup"><span data-stu-id="14dee-194">Method endBodySection</span></span>

```xpp
public void endBodySection(OutputBodySection section)
```

### <a name="parameters---endbodysection"></a><span data-ttu-id="14dee-195">パラメーター - endBodySection</span><span class="sxs-lookup"><span data-stu-id="14dee-195">Parameters - endBodySection</span></span>

<span data-ttu-id="14dee-196">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-196">section</span></span>  

## <a name="method-startpageheadersection"></a><span data-ttu-id="14dee-197">メソッド startPageHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-197">Method startPageHeaderSection</span></span>

```xpp
public void startPageHeaderSection(OutputPageHeaderSection section)
```

### <a name="parameters---startpageheadersection"></a><span data-ttu-id="14dee-198">パラメーター - startPageHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-198">Parameters - startPageHeaderSection</span></span>

<span data-ttu-id="14dee-199">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-199">section</span></span>  

## <a name="method-printviaclass"></a><span data-ttu-id="14dee-200">メソッド printViaClass</span><span class="sxs-lookup"><span data-stu-id="14dee-200">Method printViaClass</span></span>

```xpp
public void printViaClass()
```

## <a name="method-endpagefootersection"></a><span data-ttu-id="14dee-201">メソッド endPageFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-201">Method endPageFooterSection</span></span>

```xpp
public void endPageFooterSection(OutputPageFooterSection section)
```

### <a name="parameters---endpagefootersection"></a><span data-ttu-id="14dee-202">パラメーター - endPageFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-202">Parameters - endPageFooterSection</span></span>

<span data-ttu-id="14dee-203">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-203">section</span></span>  

## <a name="method-writereal"></a><span data-ttu-id="14dee-204">メソッド writeReal</span><span class="sxs-lookup"><span data-stu-id="14dee-204">Method writeReal</span></span>

```xpp
public void writeReal(OutputRealField field, OuputSection section)
```

### <a name="parameters---writereal"></a><span data-ttu-id="14dee-205">パラメーター - writeReal</span><span class="sxs-lookup"><span data-stu-id="14dee-205">Parameters - writeReal</span></span>

<span data-ttu-id="14dee-206"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-206">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-207">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-207">section</span></span>  

## <a name="method-startcolumnheadingssection"></a><span data-ttu-id="14dee-208">メソッド startColumnHeadingsSection</span><span class="sxs-lookup"><span data-stu-id="14dee-208">Method startColumnHeadingsSection</span></span>

```xpp
public void startColumnHeadingsSection(OutputColumnHeadingsSection section)
```

### <a name="parameters---startcolumnheadingssection"></a><span data-ttu-id="14dee-209">パラメーター - startColumnHeadingsSection</span><span class="sxs-lookup"><span data-stu-id="14dee-209">Parameters - startColumnHeadingsSection</span></span>

<span data-ttu-id="14dee-210">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-210">section</span></span>  

## <a name="method-writeshape"></a><span data-ttu-id="14dee-211">メソッド writeShape</span><span class="sxs-lookup"><span data-stu-id="14dee-211">Method writeShape</span></span>

```xpp
public void writeShape(OutputShapeField field, OuputSection section)
```

### <a name="parameters---writeshape"></a><span data-ttu-id="14dee-212">パラメーター - writeShape</span><span class="sxs-lookup"><span data-stu-id="14dee-212">Parameters - writeShape</span></span>

<span data-ttu-id="14dee-213"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-213">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-214">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-214">section</span></span>  

## <a name="method-writedatetime"></a><span data-ttu-id="14dee-215">メソッド writeDateTime</span><span class="sxs-lookup"><span data-stu-id="14dee-215">Method writeDateTime</span></span>

```xpp
public void writeDateTime(OutputDateTimeField field, OuputSection section)
```

### <a name="parameters---writedatetime"></a><span data-ttu-id="14dee-216">パラメーター - writeDateTime</span><span class="sxs-lookup"><span data-stu-id="14dee-216">Parameters - writeDateTime</span></span>

<span data-ttu-id="14dee-217"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-217">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-218">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-218">section</span></span>  

## <a name="method-writestatictext"></a><span data-ttu-id="14dee-219">メソッド writeStaticText</span><span class="sxs-lookup"><span data-stu-id="14dee-219">Method writeStaticText</span></span>

```xpp
public void writeStaticText(OutputStaticTextField field, OuputSection section)
```

### <a name="parameters---writestatictext"></a><span data-ttu-id="14dee-220">パラメーター - writeStaticText</span><span class="sxs-lookup"><span data-stu-id="14dee-220">Parameters - writeStaticText</span></span>

<span data-ttu-id="14dee-221"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-221">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-222">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-222">section</span></span>  

## <a name="method-new"></a><span data-ttu-id="14dee-223">メソッド new</span><span class="sxs-lookup"><span data-stu-id="14dee-223">Method new</span></span>

<span data-ttu-id="14dee-224">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14dee-224">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(PrintJobHeader jobsCursor, [PrintJobPages pagesCursor], [container settings])
```

### <a name="parameters---new"></a><span data-ttu-id="14dee-225">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="14dee-225">Parameters - new</span></span>

<span data-ttu-id="14dee-226">jobsCursor</span><span class="sxs-lookup"><span data-stu-id="14dee-226">jobsCursor</span></span>  

<!-- -->

<span data-ttu-id="14dee-227">pagesCursor</span><span class="sxs-lookup"><span data-stu-id="14dee-227">pagesCursor</span></span>  

<!-- -->

<span data-ttu-id="14dee-228">設定</span><span class="sxs-lookup"><span data-stu-id="14dee-228">settings</span></span>  

## <a name="method-writeinteger"></a><span data-ttu-id="14dee-229">メソッド writeInteger</span><span class="sxs-lookup"><span data-stu-id="14dee-229">Method writeInteger</span></span>

```xpp
public void writeInteger(OutputIntegerField field, OuputSection section)
```

### <a name="parameters---writeinteger"></a><span data-ttu-id="14dee-230">パラメーター - writeInteger</span><span class="sxs-lookup"><span data-stu-id="14dee-230">Parameters - writeInteger</span></span>

<span data-ttu-id="14dee-231"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-231">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-232">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-232">section</span></span>  

## <a name="method-startcolumnsection"></a><span data-ttu-id="14dee-233">メソッド startColumnSection</span><span class="sxs-lookup"><span data-stu-id="14dee-233">Method startColumnSection</span></span>

```xpp
public void startColumnSection()
```

## <a name="method-startsection"></a><span data-ttu-id="14dee-234">メソッド startSection</span><span class="sxs-lookup"><span data-stu-id="14dee-234">Method startSection</span></span>

```xpp
public void startSection(OuputSection section)
```

### <a name="parameters---startsection"></a><span data-ttu-id="14dee-235">パラメーター - startSection</span><span class="sxs-lookup"><span data-stu-id="14dee-235">Parameters - startSection</span></span>

<span data-ttu-id="14dee-236">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-236">section</span></span>  

## <a name="method-writedate"></a><span data-ttu-id="14dee-237">メソッド writeDate</span><span class="sxs-lookup"><span data-stu-id="14dee-237">Method writeDate</span></span>

```xpp
public void writeDate(OutputDateField field, OuputSection section)
```

### <a name="parameters---writedate"></a><span data-ttu-id="14dee-238">パラメーター - writeDate</span><span class="sxs-lookup"><span data-stu-id="14dee-238">Parameters - writeDate</span></span>

<span data-ttu-id="14dee-239"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-239">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-240">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-240">section</span></span>  

## <a name="method-pagestotal"></a><span data-ttu-id="14dee-241">メソッド pagesTotal</span><span class="sxs-lookup"><span data-stu-id="14dee-241">Method pagesTotal</span></span>

```xpp
public void pagesTotal(int pagesTotal)
```

### <a name="parameters---pagestotal"></a><span data-ttu-id="14dee-242">パラメーター - pagesTotal</span><span class="sxs-lookup"><span data-stu-id="14dee-242">Parameters - pagesTotal</span></span>

<span data-ttu-id="14dee-243">pagesTotal</span><span class="sxs-lookup"><span data-stu-id="14dee-243">pagesTotal</span></span>  

## <a name="method-writeint64"></a><span data-ttu-id="14dee-244">メソッド writeInt64</span><span class="sxs-lookup"><span data-stu-id="14dee-244">Method writeInt64</span></span>

```xpp
public void writeInt64(OutputInt64Field field, OuputSection section)
```

### <a name="parameters---writeint64"></a><span data-ttu-id="14dee-245">パラメーター - writeInt64</span><span class="sxs-lookup"><span data-stu-id="14dee-245">Parameters - writeInt64</span></span>

<span data-ttu-id="14dee-246"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-246">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-247">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-247">section</span></span>  

## <a name="method-endreport"></a><span data-ttu-id="14dee-248">メソッド endReport</span><span class="sxs-lookup"><span data-stu-id="14dee-248">Method endReport</span></span>

```xpp
public void endReport(PrintJobStatus printJobStatus)
```

### <a name="parameters---endreport"></a><span data-ttu-id="14dee-249">パラメーター - endReport</span><span class="sxs-lookup"><span data-stu-id="14dee-249">Parameters - endReport</span></span>

<span data-ttu-id="14dee-250">printJobStatus</span><span class="sxs-lookup"><span data-stu-id="14dee-250">printJobStatus</span></span>  

## <a name="method-endcolumnsection"></a><span data-ttu-id="14dee-251">メソッド endColumnSection</span><span class="sxs-lookup"><span data-stu-id="14dee-251">Method endColumnSection</span></span>

```xpp
public void endColumnSection()
```

## <a name="method-startreport"></a><span data-ttu-id="14dee-252">メソッド startReport</span><span class="sxs-lookup"><span data-stu-id="14dee-252">Method startReport</span></span>

```xpp
public void startReport(PrintJobSettings printJobSettings)
```

### <a name="parameters---startreport"></a><span data-ttu-id="14dee-253">パラメーター - startReport</span><span class="sxs-lookup"><span data-stu-id="14dee-253">Parameters - startReport</span></span>

<span data-ttu-id="14dee-254">printJobSettings</span><span class="sxs-lookup"><span data-stu-id="14dee-254">printJobSettings</span></span>  

## <a name="method-printpageviaclass"></a><span data-ttu-id="14dee-255">メソッド printPageViaClass</span><span class="sxs-lookup"><span data-stu-id="14dee-255">Method printPageViaClass</span></span>

```xpp
public void printPageViaClass(int page)
```

### <a name="parameters---printpageviaclass"></a><span data-ttu-id="14dee-256">パラメーター - printPageViaClass</span><span class="sxs-lookup"><span data-stu-id="14dee-256">Parameters - printPageViaClass</span></span>

<span data-ttu-id="14dee-257">ページ</span><span class="sxs-lookup"><span data-stu-id="14dee-257">page</span></span>  

## <a name="method-endepilogsection"></a><span data-ttu-id="14dee-258">メソッド endEpilogSection</span><span class="sxs-lookup"><span data-stu-id="14dee-258">Method endEpilogSection</span></span>

```xpp
public void endEpilogSection(OutputEpilogSection section)
```

### <a name="parameters---endepilogsection"></a><span data-ttu-id="14dee-259">パラメーター - endEpilogSection</span><span class="sxs-lookup"><span data-stu-id="14dee-259">Parameters - endEpilogSection</span></span>

<span data-ttu-id="14dee-260">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-260">section</span></span>  

## <a name="method-endprologsection"></a><span data-ttu-id="14dee-261">メソッド endPrologSection</span><span class="sxs-lookup"><span data-stu-id="14dee-261">Method endPrologSection</span></span>

```xpp
public void endPrologSection(OutputPrologSection section)
```

### <a name="parameters---endprologsection"></a><span data-ttu-id="14dee-262">パラメーター - endPrologSection</span><span class="sxs-lookup"><span data-stu-id="14dee-262">Parameters - endPrologSection</span></span>

<span data-ttu-id="14dee-263">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-263">section</span></span>  

## <a name="method-endpage"></a><span data-ttu-id="14dee-264">メソッド endPage</span><span class="sxs-lookup"><span data-stu-id="14dee-264">Method endPage</span></span>

```xpp
public void endPage()
```

## <a name="method-startfootersection"></a><span data-ttu-id="14dee-265">メソッド startFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-265">Method startFooterSection</span></span>

```xpp
public void startFooterSection(OutputFooterSection section)
```

### <a name="parameters---startfootersection"></a><span data-ttu-id="14dee-266">パラメーター - startFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-266">Parameters - startFooterSection</span></span>

<span data-ttu-id="14dee-267">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-267">section</span></span>  

## <a name="method-endprogrammablesection"></a><span data-ttu-id="14dee-268">メソッド endProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="14dee-268">Method endProgrammableSection</span></span>

```xpp
public void endProgrammableSection(OutputProgrammableSection section)
```

### <a name="parameters---endprogrammablesection"></a><span data-ttu-id="14dee-269">パラメーター - endProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="14dee-269">Parameters - endProgrammableSection</span></span>

<span data-ttu-id="14dee-270">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-270">section</span></span>  

## <a name="method-startbodysection"></a><span data-ttu-id="14dee-271">メソッド startBodySection</span><span class="sxs-lookup"><span data-stu-id="14dee-271">Method startBodySection</span></span>

```xpp
public void startBodySection(OutputBodySection section)
```

### <a name="parameters---startbodysection"></a><span data-ttu-id="14dee-272">パラメーター - startBodySection</span><span class="sxs-lookup"><span data-stu-id="14dee-272">Parameters - startBodySection</span></span>

<span data-ttu-id="14dee-273">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-273">section</span></span>  

## <a name="method-endsection"></a><span data-ttu-id="14dee-274">メソッド endSection</span><span class="sxs-lookup"><span data-stu-id="14dee-274">Method endSection</span></span>

```xpp
public void endSection(OuputSection section)
```

### <a name="parameters---endsection"></a><span data-ttu-id="14dee-275">パラメーター - endSection</span><span class="sxs-lookup"><span data-stu-id="14dee-275">Parameters - endSection</span></span>

<span data-ttu-id="14dee-276">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-276">section</span></span>  

## <a name="method-startprogrammablesection"></a><span data-ttu-id="14dee-277">メソッド startProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="14dee-277">Method startProgrammableSection</span></span>

```xpp
public void startProgrammableSection(OutputProgrammableSection section)
```

### <a name="parameters---startprogrammablesection"></a><span data-ttu-id="14dee-278">パラメーター - startProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="14dee-278">Parameters - startProgrammableSection</span></span>

<span data-ttu-id="14dee-279">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-279">section</span></span>  

## <a name="method-startepilogsection"></a><span data-ttu-id="14dee-280">メソッド startEpilogSection</span><span class="sxs-lookup"><span data-stu-id="14dee-280">Method startEpilogSection</span></span>

```xpp
public void startEpilogSection(OutputEpilogSection section)
```

### <a name="parameters---startepilogsection"></a><span data-ttu-id="14dee-281">パラメーター - startEpilogSection</span><span class="sxs-lookup"><span data-stu-id="14dee-281">Parameters - startEpilogSection</span></span>

<span data-ttu-id="14dee-282">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-282">section</span></span>  

## <a name="method-startheadersection"></a><span data-ttu-id="14dee-283">メソッド startHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-283">Method startHeaderSection</span></span>

```xpp
public void startHeaderSection(OutputHeaderSection section)
```

### <a name="parameters---startheadersection"></a><span data-ttu-id="14dee-284">パラメーター - startHeaderSection</span><span class="sxs-lookup"><span data-stu-id="14dee-284">Parameters - startHeaderSection</span></span>

<span data-ttu-id="14dee-285">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-285">section</span></span>  

## <a name="method-endcolumnheadingssection"></a><span data-ttu-id="14dee-286">メソッド endColumnHeadingsSection</span><span class="sxs-lookup"><span data-stu-id="14dee-286">Method endColumnHeadingsSection</span></span>

```xpp
public void endColumnHeadingsSection(OutputColumnHeadingsSection section)
```

### <a name="parameters---endcolumnheadingssection"></a><span data-ttu-id="14dee-287">パラメーター - endColumnHeadingsSection</span><span class="sxs-lookup"><span data-stu-id="14dee-287">Parameters - endColumnHeadingsSection</span></span>

<span data-ttu-id="14dee-288">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-288">section</span></span>  

## <a name="method-writelabel"></a><span data-ttu-id="14dee-289">メソッド writeLabel</span><span class="sxs-lookup"><span data-stu-id="14dee-289">Method writeLabel</span></span>

```xpp
public void writeLabel(OutputLabelField field, OuputSection section)
```

### <a name="parameters---writelabel"></a><span data-ttu-id="14dee-290">パラメーター - writeLabel</span><span class="sxs-lookup"><span data-stu-id="14dee-290">Parameters - writeLabel</span></span>

<span data-ttu-id="14dee-291"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-291">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-292">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-292">section</span></span>  

## <a name="method-endfootersection"></a><span data-ttu-id="14dee-293">メソッド endFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-293">Method endFooterSection</span></span>

```xpp
public void endFooterSection(OutputFooterSection section)
```

### <a name="parameters---endfootersection"></a><span data-ttu-id="14dee-294">パラメーター - endFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-294">Parameters - endFooterSection</span></span>

<span data-ttu-id="14dee-295">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-295">section</span></span>  

## <a name="method-writefield"></a><span data-ttu-id="14dee-296">メソッド writeField</span><span class="sxs-lookup"><span data-stu-id="14dee-296">Method writeField</span></span>

```xpp
public void writeField(OutputField field, OuputSection section)
```

### <a name="parameters---writefield"></a><span data-ttu-id="14dee-297">パラメーター - writeField</span><span class="sxs-lookup"><span data-stu-id="14dee-297">Parameters - writeField</span></span>

<span data-ttu-id="14dee-298"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-298">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-299">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-299">section</span></span>  

## <a name="method-writeenum"></a><span data-ttu-id="14dee-300">メソッド writeEnum</span><span class="sxs-lookup"><span data-stu-id="14dee-300">Method writeEnum</span></span>

```xpp
public void writeEnum(OutputEnumField field, OuputSection section)
```

### <a name="parameters---writeenum"></a><span data-ttu-id="14dee-301">パラメーター - writeEnum</span><span class="sxs-lookup"><span data-stu-id="14dee-301">Parameters - writeEnum</span></span>

<span data-ttu-id="14dee-302"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-302">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-303">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-303">section</span></span>  

## <a name="method-startpagefootersection"></a><span data-ttu-id="14dee-304">メソッド startPageFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-304">Method startPageFooterSection</span></span>

```xpp
public void startPageFooterSection(OutputPageFooterSection section)
```

### <a name="parameters---startpagefootersection"></a><span data-ttu-id="14dee-305">パラメーター - startPageFooterSection</span><span class="sxs-lookup"><span data-stu-id="14dee-305">Parameters - startPageFooterSection</span></span>

<span data-ttu-id="14dee-306">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-306">section</span></span>  

## <a name="method-writesum"></a><span data-ttu-id="14dee-307">メソッド writeSum</span><span class="sxs-lookup"><span data-stu-id="14dee-307">Method writeSum</span></span>

```xpp
public void writeSum(OutputSumField field, OuputSection section)
```

### <a name="parameters---writesum"></a><span data-ttu-id="14dee-308">パラメーター - writeSum</span><span class="sxs-lookup"><span data-stu-id="14dee-308">Parameters - writeSum</span></span>

<span data-ttu-id="14dee-309"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-309">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-310">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-310">section</span></span>  

## <a name="method-writetime"></a><span data-ttu-id="14dee-311">メソッド writeTime</span><span class="sxs-lookup"><span data-stu-id="14dee-311">Method writeTime</span></span>

```xpp
public void writeTime(OutputTimeField field, OuputSection section)
```

### <a name="parameters---writetime"></a><span data-ttu-id="14dee-312">パラメーター - writeTime</span><span class="sxs-lookup"><span data-stu-id="14dee-312">Parameters - writeTime</span></span>

<span data-ttu-id="14dee-313"> フィールド</span><span class="sxs-lookup"><span data-stu-id="14dee-313">field</span></span>  

<!-- -->

<span data-ttu-id="14dee-314">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-314">section</span></span>  

## <a name="method-startpage"></a><span data-ttu-id="14dee-315">メソッド startPage</span><span class="sxs-lookup"><span data-stu-id="14dee-315">Method startPage</span></span>

```xpp
public void startPage(OutputPage page)
```

### <a name="parameters---startpage"></a><span data-ttu-id="14dee-316">パラメーター - startPage</span><span class="sxs-lookup"><span data-stu-id="14dee-316">Parameters - startPage</span></span>

<span data-ttu-id="14dee-317">ページ</span><span class="sxs-lookup"><span data-stu-id="14dee-317">page</span></span>  

## <a name="method-startprologsection"></a><span data-ttu-id="14dee-318">メソッド startPrologSection</span><span class="sxs-lookup"><span data-stu-id="14dee-318">Method startPrologSection</span></span>

```xpp
public void startPrologSection(OutputPrologSection section)
```

### <a name="parameters---startprologsection"></a><span data-ttu-id="14dee-319">パラメーター - startPrologSection</span><span class="sxs-lookup"><span data-stu-id="14dee-319">Parameters - startPrologSection</span></span>

<span data-ttu-id="14dee-320">セクション</span><span class="sxs-lookup"><span data-stu-id="14dee-320">section</span></span>  

