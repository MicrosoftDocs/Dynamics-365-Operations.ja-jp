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
# <a name="class-printjobsettings"></a><span data-ttu-id="7c5d2-103">クラス PrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-103">Class PrintJobSettings</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PrintJobSettings extends Object
```

<span data-ttu-id="7c5d2-104">PrintJobSettings クラスを使用すると、ユーザーがプリンターおよびそのデバイス設定にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-104">The PrintJobSettings class lets users access printers and their device settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c5d2-105">備考</span><span class="sxs-lookup"><span data-stu-id="7c5d2-105">Remarks</span></span>

<span data-ttu-id="7c5d2-106">PrintJobSettings は、SysPrintForm フォームにより使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-106">PrintJobSettings is used by the SysPrintForm form.</span></span>

## <a name="examples"></a><span data-ttu-id="7c5d2-107">例</span><span class="sxs-lookup"><span data-stu-id="7c5d2-107">Examples</span></span>

<span data-ttu-id="7c5d2-108">次の例では、既定のプリンターの名前を書き込み、使用可能なプリンターを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-108">The following example writes the name of the default printer and lists the available printers.</span></span>

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

## <a name="methods"></a><span data-ttu-id="7c5d2-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="7c5d2-109">Methods</span></span>

| <span data-ttu-id="7c5d2-110">方法</span><span class="sxs-lookup"><span data-stu-id="7c5d2-110">Method</span></span>                                                                                                  | <span data-ttu-id="7c5d2-111">説明</span><span class="sxs-lookup"><span data-stu-id="7c5d2-111">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5d2-112">public boolean allPages(\[boolean all\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-112">public boolean allPages(\[boolean all\])</span></span>                                                                | <span data-ttu-id="7c5d2-113">sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-113">Controls whether the All or Pages option button should be selected when you run the sysPrintForm.</span></span> |
| <span data-ttu-id="7c5d2-114">public boolean appendToTextFile(\[boolean append\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-114">public boolean appendToTextFile(\[boolean append\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="7c5d2-115">public boolean banding()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-115">public boolean banding()</span></span>                                                                                |                                                                                                   |
| <span data-ttu-id="7c5d2-116">public PrintJobSettings clientPrintJobSettings()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-116">public PrintJobSettings clientPrintJobSettings()</span></span>                                                        |                                                                                                   |
| <span data-ttu-id="7c5d2-117">public boolean collate(\[boolean collate\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-117">public boolean collate(\[boolean collate\])</span></span>                                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-118">public int copies(\[int numberOfCopies\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-118">public int copies(\[int numberOfCopies\])</span></span>                                                               |                                                                                                   |
| <span data-ttu-id="7c5d2-119">public str copyDescription(int number, \[str description\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-119">public str copyDescription(int number, \[str description\])</span></span>                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-120">public str deviceName(\[str device\], \[ClassRunMode runOn\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-120">public str deviceName(\[str device\], \[ClassRunMode runOn\])</span></span>                                           | <span data-ttu-id="7c5d2-121">プリンターを選択するか、選択されているプリンター デバイス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-121">Selects a printer or retrieves the deviceName of the selected printer.</span></span>                            |
| <span data-ttu-id="7c5d2-122">public boolean doNotOverwrite(\[boolean warn\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-122">public boolean doNotOverwrite(\[boolean warn\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-123">public boolean enableCopies(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-123">public boolean enableCopies(\[boolean enable\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-124">public boolean enableDevice(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-124">public boolean enableDevice(\[boolean enable\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-125">public boolean enablePages(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-125">public boolean enablePages(\[boolean enable\])</span></span>                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-126">public boolean enableProperties(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-126">public boolean enableProperties(\[boolean enable\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="7c5d2-127">public boolean enableStoreInPrintArchive(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-127">public boolean enableStoreInPrintArchive(\[boolean enable\])</span></span>                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-128">public boolean enableTarget(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-128">public boolean enableTarget(\[boolean enable\])</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-129">public int facename2number(\[str facename\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-129">public int facename2number(\[str facename\])</span></span>                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-130">public str fileName(\[str FileName\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-130">public str fileName(\[str FileName\])</span></span>                                                                   |                                                                                                   |
| <span data-ttu-id="7c5d2-131">public boolean fitToPage(\[boolean fit\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-131">public boolean fitToPage(\[boolean fit\])</span></span>                                                               |                                                                                                   |
| <span data-ttu-id="7c5d2-132">public PrintFormat format(\[PrintFormat format\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-132">public PrintFormat format(\[PrintFormat format\])</span></span>                                                       |                                                                                                   |
| <span data-ttu-id="7c5d2-133">public int from(\[int fromPage\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-133">public int from(\[int fromPage\])</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="7c5d2-134">public str getFacename(int number)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-134">public str getFacename(int number)</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="7c5d2-135">public str getFacenameInfo(int number)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-135">public str getFacenameInfo(int number)</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="7c5d2-136">public Struct getFontInfo(str fontName)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-136">public Struct getFontInfo(str fontName)</span></span>                                                                 |                                                                                                   |
| <span data-ttu-id="7c5d2-137">public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-137">public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)</span></span>                             |                                                                                                   |
| <span data-ttu-id="7c5d2-138">public int getNumberOfClientPrinters()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-138">public int getNumberOfClientPrinters()</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="7c5d2-139">public int getNumberOfFacenames()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-139">public int getNumberOfFacenames()</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="7c5d2-140">public int getNumberOfPrinters()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-140">public int getNumberOfPrinters()</span></span>                                                                        | <span data-ttu-id="7c5d2-141">コンピューターに設定されているプリンターの数を返します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-141">Returns the number of printers that are set up on the computer.</span></span>                                   |
| <span data-ttu-id="7c5d2-142">public int getNumberOfServerPrinters()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-142">public int getNumberOfServerPrinters()</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="7c5d2-143">public int getNumberOfTrays()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-143">public int getNumberOfTrays()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="7c5d2-144">public str getPrinter(int number)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-144">public str getPrinter(int number)</span></span>                                                                       | <span data-ttu-id="7c5d2-145">プリンターの deviceName を取得します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-145">Gets the deviceName of a printer.</span></span>                                                                 |
| <span data-ttu-id="7c5d2-146">public ClassRunMode getRunOn(int number)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-146">public ClassRunMode getRunOn(int number)</span></span>                                                                |                                                                                                   |
| <span data-ttu-id="7c5d2-147">public PrintMedium getTarget()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-147">public PrintMedium getTarget()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-148">public int getTray(int number)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-148">public int getTray(int number)</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-149">public str getTrayName(int number)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-149">public str getTrayName(int number)</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="7c5d2-150">public Int64 hDC()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-150">public Int64 hDC()</span></span>                                                                                      |                                                                                                   |
| <span data-ttu-id="7c5d2-151">public boolean lockDestinationProperties(\[boolean warn\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-151">public boolean lockDestinationProperties(\[boolean warn\])</span></span>                                              |                                                                                                   |
| <span data-ttu-id="7c5d2-152">public str mailCc(\[str MailCc\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-152">public str mailCc(\[str MailCc\])</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="7c5d2-153">public str mailSubject(\[str MailSubject\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-153">public str mailSubject(\[str MailSubject\])</span></span>                                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-154">public str mailTo(\[str MailTo\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-154">public str mailTo(\[str MailTo\])</span></span>                                                                       |                                                                                                   |
| <span data-ttu-id="7c5d2-155">public int numberOfCopyDescriptions(int number)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-155">public int numberOfCopyDescriptions(int number)</span></span>                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-156">public boolean outputToClient(\[boolean toClient\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-156">public boolean outputToClient(\[boolean toClient\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="7c5d2-157">public boolean outputToPrnFile(\[boolean writePrnFile\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-157">public boolean outputToPrnFile(\[boolean writePrnFile\])</span></span>                                                |                                                                                                   |
| <span data-ttu-id="7c5d2-158">public container packNamesAndPrinterData()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-158">public container packNamesAndPrinterData()</span></span>                                                              |                                                                                                   |
| <span data-ttu-id="7c5d2-159">public container packPageSettings()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-159">public container packPageSettings()</span></span>                                                                     | <span data-ttu-id="7c5d2-160">ページの書式設定時に選択されているデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-160">Stores the data that is selected during page formatting in a container.</span></span>                           |
| <span data-ttu-id="7c5d2-161">public container packPrinterSettings()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-161">public container packPrinterSettings()</span></span>                                                                  |                                                                                                   |
| <span data-ttu-id="7c5d2-162">public container packPrintJobSettings()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-162">public container packPrintJobSettings()</span></span>                                                                 |                                                                                                   |
| <span data-ttu-id="7c5d2-163">public container packSubtotalSettings()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-163">public container packSubtotalSettings()</span></span>                                                                 |                                                                                                   |
| <span data-ttu-id="7c5d2-164">public int pageCopy2Tray(int pageNumber, \[int copyNumber\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-164">public int pageCopy2Tray(int pageNumber, \[int copyNumber\])</span></span>                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-165">public boolean pageFormatting()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-165">public boolean pageFormatting()</span></span>                                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-166">public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-166">public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])</span></span>                          |                                                                                                   |
| <span data-ttu-id="7c5d2-167">public int paperTray(\[int tray\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-167">public int paperTray(\[int tray\])</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="7c5d2-168">public int paperTrayRaw(\[int tray\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-168">public int paperTrayRaw(\[int tray\])</span></span>                                                                   |                                                                                                   |
| <span data-ttu-id="7c5d2-169">public int performanceTest(\[int loops\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-169">public int performanceTest(\[int loops\])</span></span>                                                               |                                                                                                   |
| <span data-ttu-id="7c5d2-170">public PrintFormat preferredFileFormat(\[PrintFormat format\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-170">public PrintFormat preferredFileFormat(\[PrintFormat format\])</span></span>                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-171">public PrintFormat preferredMailFormat(\[PrintFormat format\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-171">public PrintFormat preferredMailFormat(\[PrintFormat format\])</span></span>                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-172">public PrinterOrientation preferredOrientation(\[PrinterOrientation orientation\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-172">public PrinterOrientation preferredOrientation(\[PrinterOrientation orientation\])</span></span>                      |                                                                                                   |
| <span data-ttu-id="7c5d2-173">public PrintMedium preferredTarget(\[PrintMedium target\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-173">public PrintMedium preferredTarget(\[PrintMedium target\])</span></span>                                              |                                                                                                   |
| <span data-ttu-id="7c5d2-174">public int printerAttributes()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-174">public int printerAttributes()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-175">public int printerAveragePPM()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-175">public int printerAveragePPM()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-176">public str printerComment()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-176">public str printerComment()</span></span>                                                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-177">public str printerDatatype()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-177">public str printerDatatype()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-178">public int printerDefaultPriority()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-178">public int printerDefaultPriority()</span></span>                                                                     |                                                                                                   |
| <span data-ttu-id="7c5d2-179">public str printerDriverName()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-179">public str printerDriverName()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-180">public str printerLocation()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-180">public str printerLocation()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-181">public int printerPageHeight()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-181">public int printerPageHeight()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-182">public int printerPageWidth()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-182">public int printerPageWidth()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="7c5d2-183">public int printerPaper()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-183">public int printerPaper()</span></span>                                                                               |                                                                                                   |
| <span data-ttu-id="7c5d2-184">public str printerParameters()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-184">public str printerParameters()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-185">public str printerPortName()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-185">public str printerPortName()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-186">public str printerPrinterName()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-186">public str printerPrinterName()</span></span>                                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-187">public str printerPrintProcessor()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-187">public str printerPrintProcessor()</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="7c5d2-188">public int printerPriority()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-188">public int printerPriority()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-189">public int printerQueuedJobs()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-189">public int printerQueuedJobs()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-190">public ClassRunMode printerRunOn()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-190">public ClassRunMode printerRunOn()</span></span>                                                                      |                                                                                                   |
| <span data-ttu-id="7c5d2-191">public str printerSepFile()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-191">public str printerSepFile()</span></span>                                                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-192">public str printerServerName()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-192">public str printerServerName()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-193">public boolean printerSettings(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-193">public boolean printerSettings(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span></span> |                                                                                                   |
| <span data-ttu-id="7c5d2-194">public str printerShareName()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-194">public str printerShareName()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="7c5d2-195">public TimeOfDay printerStartTime()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-195">public TimeOfDay printerStartTime()</span></span>                                                                     |                                                                                                   |
| <span data-ttu-id="7c5d2-196">public int printerStatus()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-196">public int printerStatus()</span></span>                                                                              |                                                                                                   |
| <span data-ttu-id="7c5d2-197">public TimeOfDay printerUntilTime()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-197">public TimeOfDay printerUntilTime()</span></span>                                                                     |                                                                                                   |
| <span data-ttu-id="7c5d2-198">public ReportRun reportRun()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-198">public ReportRun reportRun()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-199">public str requestedDeviceName()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-199">public str requestedDeviceName()</span></span>                                                                        |                                                                                                   |
| <span data-ttu-id="7c5d2-200">public ClassRunMode requestedRunOn()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-200">public ClassRunMode requestedRunOn()</span></span>                                                                    |                                                                                                   |
| <span data-ttu-id="7c5d2-201">public boolean runClient()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-201">public boolean runClient()</span></span>                                                                              |                                                                                                   |
| <span data-ttu-id="7c5d2-202">public boolean runServer()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-202">public boolean runServer()</span></span>                                                                              |                                                                                                   |
| <span data-ttu-id="7c5d2-203">public int sectionsPerPage(\[int sectionsPerPage\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-203">public int sectionsPerPage(\[int sectionsPerPage\])</span></span>                                                     |                                                                                                   |
| <span data-ttu-id="7c5d2-204">public PrintMedium setTarget(PrintMedium target)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-204">public PrintMedium setTarget(PrintMedium target)</span></span>                                                        | <span data-ttu-id="7c5d2-205">印刷メディアを設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-205">Sets the print medium.</span></span>                                                                            |
| <span data-ttu-id="7c5d2-206">public boolean singleLargePage(\[boolean singleLargePage\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-206">public boolean singleLargePage(\[boolean singleLargePage\])</span></span>                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-207">public boolean skipBitmapsInRTF(\[boolean skipBitmaps\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-207">public boolean skipBitmapsInRTF(\[boolean skipBitmaps\])</span></span>                                                | <span data-ttu-id="7c5d2-208">.rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-208">Controls whether bitmaps are included when reports are printed to an .rtf file.</span></span>                   |
| <span data-ttu-id="7c5d2-209">public boolean storeInPrintArchive(\[boolean store\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-209">public boolean storeInPrintArchive(\[boolean store\])</span></span>                                                   |                                                                                                   |
| <span data-ttu-id="7c5d2-210">public boolean suppressScalingMessage(\[boolean suppress\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-210">public boolean suppressScalingMessage(\[boolean suppress\])</span></span>                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-211">public int to(\[int toPage\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-211">public int to(\[int toPage\])</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="7c5d2-212">public str toString()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-212">public str toString()</span></span>                                                                                   | <span data-ttu-id="7c5d2-213">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-213">Returns a string that represents the current object.</span></span>                                              |
| <span data-ttu-id="7c5d2-214">public boolean unpackPageSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-214">public boolean unpackPageSettings(container settings)</span></span>                                                   | <span data-ttu-id="7c5d2-215">用紙サイズと向きなど、ページ設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-215">Sets the page settings, such as paper size and orientation.</span></span>                                       |
| <span data-ttu-id="7c5d2-216">public boolean unpackPrinterSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-216">public boolean unpackPrinterSettings(container settings)</span></span>                                                |                                                                                                   |
| <span data-ttu-id="7c5d2-217">public boolean unpackPrintJobSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-217">public boolean unpackPrintJobSettings(container settings)</span></span>                                               |                                                                                                   |
| <span data-ttu-id="7c5d2-218">public boolean unpackSubtotalSettings(container settings)</span><span class="sxs-lookup"><span data-stu-id="7c5d2-218">public boolean unpackSubtotalSettings(container settings)</span></span>                                               |                                                                                                   |
| <span data-ttu-id="7c5d2-219">public int unprintableBottom()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-219">public int unprintableBottom()</span></span>                                                                          |                                                                                                   |
| <span data-ttu-id="7c5d2-220">public int unprintableLeft()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-220">public int unprintableLeft()</span></span>                                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-221">public int unprintableRight()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-221">public int unprintableRight()</span></span>                                                                           |                                                                                                   |
| <span data-ttu-id="7c5d2-222">public int unprintableTop()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-222">public int unprintableTop()</span></span>                                                                             | <span data-ttu-id="7c5d2-223">用紙の最上部から用紙の印刷可能な範囲までの距離を示します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-223">Indicates the distance from the top of the paper to the printable area of the paper.</span></span>              |
| <span data-ttu-id="7c5d2-224">public ReportOutputUserType viewerType(\[ReportOutputUserType type\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-224">public ReportOutputUserType viewerType(\[ReportOutputUserType type\])</span></span>                                   |                                                                                                   |
| <span data-ttu-id="7c5d2-225">public int virtualPageHeight(\[int height\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-225">public int virtualPageHeight(\[int height\])</span></span>                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-226">public boolean warnIfFileExists(\[boolean warn\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-226">public boolean warnIfFileExists(\[boolean warn\])</span></span>                                                       |                                                                                                   |
| <span data-ttu-id="7c5d2-227">public void enableBody(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-227">public void enableBody(\[TableId tableId\])</span></span>                                                             |                                                                                                   |
| <span data-ttu-id="7c5d2-228">public void new(\[container Settings\], \[boolean infoOnly\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-228">public void new(\[container Settings\], \[boolean infoOnly\])</span></span>                                           | <span data-ttu-id="7c5d2-229">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-229">Initializes a new instance of the Object class.</span></span>                                                   |
| <span data-ttu-id="7c5d2-230">public void addTrayPageCopy(int tray, int pageNumber, \[int copyNumber\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-230">public void addTrayPageCopy(int tray, int pageNumber, \[int copyNumber\])</span></span>                               |                                                                                                   |
| <span data-ttu-id="7c5d2-231">public void disableBody(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="7c5d2-231">public void disableBody(\[TableId tableId\])</span></span>                                                            |                                                                                                   |
| <span data-ttu-id="7c5d2-232">public void clearTrayPageCopy()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-232">public void clearTrayPageCopy()</span></span>                                                                         |                                                                                                   |
| <span data-ttu-id="7c5d2-233">public void rulerInch()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-233">public void rulerInch()</span></span>                                                                                 |                                                                                                   |
| <span data-ttu-id="7c5d2-234">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-234">public void finalize()</span></span>                                                                                  |                                                                                                   |
| <span data-ttu-id="7c5d2-235">public void rulerOff()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-235">public void rulerOff()</span></span>                                                                                  |                                                                                                   |
| <span data-ttu-id="7c5d2-236">public void rulerMetric()</span><span class="sxs-lookup"><span data-stu-id="7c5d2-236">public void rulerMetric()</span></span>                                                                               |                                                                                                   |

## <a name="method-allpages"></a><span data-ttu-id="7c5d2-237">メソッド allPages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-237">Method allPages</span></span>

<span data-ttu-id="7c5d2-238">sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-238">Controls whether the All or Pages option button should be selected when you run the sysPrintForm.</span></span>

```xpp
public boolean allPages([boolean all])
```

### <a name="parameters---allpages"></a><span data-ttu-id="7c5d2-239">パラメーター - allPages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-239">Parameters - allPages</span></span>

<span data-ttu-id="7c5d2-240">すべて</span><span class="sxs-lookup"><span data-stu-id="7c5d2-240">all</span></span>  
<span data-ttu-id="7c5d2-241">true の場合、すべてのオプション ボタンが選択されるブール値; それ以外の場合は、ページ オプション ボタンが選択されます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-241">A boolean value that, if true, the All option button is selected; otherwise, the Pages option button is selected.</span></span>

### <a name="return-value---allpages"></a><span data-ttu-id="7c5d2-242">戻り値 - allPages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-242">Return Value - allPages</span></span>

<span data-ttu-id="7c5d2-243">すべてのオプション ボタンを選択する必要がある場合は true。それ以外の場合は false で、ページのオプション ボタンが選択されます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-243">true if the All radio button should be selected; otherwise, false, and the Pages option button is selected.</span></span>

### <a name="remarks---allpages"></a><span data-ttu-id="7c5d2-244">備考 - allPages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-244">Remarks - allPages</span></span>

<span data-ttu-id="7c5d2-245">このメソッドは、sysPrintForm によって内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-245">The method is for internal use by sysPrintForm.</span></span>

### <a name="examples---allpages"></a><span data-ttu-id="7c5d2-246">例 - allPages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-246">Examples - allPages</span></span>

<span data-ttu-id="7c5d2-247">次の例では、2 〜 4 のページを印刷し、[すべてのオプション] ボタンではなく [ページのオプション] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-247">The following example prints pages 2 to 4 and selects the Pages option button instead of the All option button.</span></span>

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

## <a name="method-appendtotextfile"></a><span data-ttu-id="7c5d2-248">メソッド appendToTextFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-248">Method appendToTextFile</span></span>

```xpp
public boolean appendToTextFile([boolean append])
```

### <a name="parameters---appendtotextfile"></a><span data-ttu-id="7c5d2-249">パラメーター - appendToTextFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-249">Parameters - appendToTextFile</span></span>

<span data-ttu-id="7c5d2-250">append</span><span class="sxs-lookup"><span data-stu-id="7c5d2-250">append</span></span>  

### <a name="return-value---appendtotextfile"></a><span data-ttu-id="7c5d2-251">戻り値 - appendToTextFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-251">Return Value - appendToTextFile</span></span>

## <a name="method-banding"></a><span data-ttu-id="7c5d2-252">メソッド banding</span><span class="sxs-lookup"><span data-stu-id="7c5d2-252">Method banding</span></span>

```xpp
public boolean banding()
```

### <a name="return-value---banding"></a><span data-ttu-id="7c5d2-253">戻り値 - banding</span><span class="sxs-lookup"><span data-stu-id="7c5d2-253">Return Value - banding</span></span>

## <a name="method-clientprintjobsettings"></a><span data-ttu-id="7c5d2-254">メソッド clientPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-254">Method clientPrintJobSettings</span></span>

```xpp
public PrintJobSettings clientPrintJobSettings()
```

### <a name="return-value---clientprintjobsettings"></a><span data-ttu-id="7c5d2-255">戻り値 - clientPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-255">Return Value - clientPrintJobSettings</span></span>

## <a name="method-collate"></a><span data-ttu-id="7c5d2-256">メソッド collate</span><span class="sxs-lookup"><span data-stu-id="7c5d2-256">Method collate</span></span>

```xpp
public boolean collate([boolean collate])
```

### <a name="parameters---collate"></a><span data-ttu-id="7c5d2-257">パラメーター - collate</span><span class="sxs-lookup"><span data-stu-id="7c5d2-257">Parameters - collate</span></span>

<span data-ttu-id="7c5d2-258">collate</span><span class="sxs-lookup"><span data-stu-id="7c5d2-258">collate</span></span>  

### <a name="return-value---collate"></a><span data-ttu-id="7c5d2-259">戻り値 - collate</span><span class="sxs-lookup"><span data-stu-id="7c5d2-259">Return Value - collate</span></span>

## <a name="method-copies"></a><span data-ttu-id="7c5d2-260">メソッド copies</span><span class="sxs-lookup"><span data-stu-id="7c5d2-260">Method copies</span></span>

```xpp
public int copies([int numberOfCopies])
```

### <a name="parameters---copies"></a><span data-ttu-id="7c5d2-261">パラメーター - copies</span><span class="sxs-lookup"><span data-stu-id="7c5d2-261">Parameters - copies</span></span>

<span data-ttu-id="7c5d2-262">numberOfCopies</span><span class="sxs-lookup"><span data-stu-id="7c5d2-262">numberOfCopies</span></span>  

### <a name="return-value---copies"></a><span data-ttu-id="7c5d2-263">戻り値 - copies</span><span class="sxs-lookup"><span data-stu-id="7c5d2-263">Return Value - copies</span></span>

## <a name="method-copydescription"></a><span data-ttu-id="7c5d2-264">メソッド copyDescription</span><span class="sxs-lookup"><span data-stu-id="7c5d2-264">Method copyDescription</span></span>

```xpp
public str copyDescription(int number, [str description])
```

### <a name="parameters---copydescription"></a><span data-ttu-id="7c5d2-265">パラメーター - copyDescription</span><span class="sxs-lookup"><span data-stu-id="7c5d2-265">Parameters - copyDescription</span></span>

<span data-ttu-id="7c5d2-266">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-266">number</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-267">説明</span><span class="sxs-lookup"><span data-stu-id="7c5d2-267">description</span></span>  

### <a name="return-value---copydescription"></a><span data-ttu-id="7c5d2-268">戻り値 - copyDescription</span><span class="sxs-lookup"><span data-stu-id="7c5d2-268">Return Value - copyDescription</span></span>

## <a name="method-devicename"></a><span data-ttu-id="7c5d2-269">メソッド deviceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-269">Method deviceName</span></span>

<span data-ttu-id="7c5d2-270">プリンターを選択するか、選択されているプリンター デバイス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-270">Selects a printer or retrieves the deviceName of the selected printer.</span></span>

```xpp
public str deviceName([str device], [ClassRunMode runOn])
```

### <a name="parameters---devicename"></a><span data-ttu-id="7c5d2-271">パラメーター - deviceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-271">Parameters - deviceName</span></span>

<span data-ttu-id="7c5d2-272">デバイス</span><span class="sxs-lookup"><span data-stu-id="7c5d2-272">device</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-273">runOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-273">runOn</span></span>  

### <a name="return-value---devicename"></a><span data-ttu-id="7c5d2-274">戻り値 - deviceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-274">Return Value - deviceName</span></span>

<span data-ttu-id="7c5d2-275">選択したプリンターの deviceName。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-275">The deviceName of the selected printer.</span></span>

### <a name="remarks---devicename"></a><span data-ttu-id="7c5d2-276">備考 - deviceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-276">Remarks - deviceName</span></span>

<span data-ttu-id="7c5d2-277">選択されるプリンターの deviceName は、getPrinter メソッドを使用して検出できます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-277">The deviceName of a printer to be selected could be found by using the getPrinter method.</span></span>

### <a name="examples---devicename"></a><span data-ttu-id="7c5d2-278">例 - deviceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-278">Examples - deviceName</span></span>

<span data-ttu-id="7c5d2-279">このジョブは、利用可能なプリンターと印刷できない領域を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-279">This job lists the available printers and their nonprintable area.</span></span>

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

## <a name="method-donotoverwrite"></a><span data-ttu-id="7c5d2-280">メソッド doNotOverwrite</span><span class="sxs-lookup"><span data-stu-id="7c5d2-280">Method doNotOverwrite</span></span>

```xpp
public boolean doNotOverwrite([boolean warn])
```

### <a name="parameters---donotoverwrite"></a><span data-ttu-id="7c5d2-281">パラメーター - doNotOverwrite</span><span class="sxs-lookup"><span data-stu-id="7c5d2-281">Parameters - doNotOverwrite</span></span>

<span data-ttu-id="7c5d2-282">警告</span><span class="sxs-lookup"><span data-stu-id="7c5d2-282">warn</span></span>  

### <a name="return-value---donotoverwrite"></a><span data-ttu-id="7c5d2-283">戻り値 - doNotOverwrite</span><span class="sxs-lookup"><span data-stu-id="7c5d2-283">Return Value - doNotOverwrite</span></span>

## <a name="method-enablecopies"></a><span data-ttu-id="7c5d2-284">メソッド enableCopies</span><span class="sxs-lookup"><span data-stu-id="7c5d2-284">Method enableCopies</span></span>

```xpp
public boolean enableCopies([boolean enable])
```

### <a name="parameters---enablecopies"></a><span data-ttu-id="7c5d2-285">パラメーター - enableCopies</span><span class="sxs-lookup"><span data-stu-id="7c5d2-285">Parameters - enableCopies</span></span>

<span data-ttu-id="7c5d2-286">enable</span><span class="sxs-lookup"><span data-stu-id="7c5d2-286">enable</span></span>  

### <a name="return-value---enablecopies"></a><span data-ttu-id="7c5d2-287">戻り値 - enableCopies</span><span class="sxs-lookup"><span data-stu-id="7c5d2-287">Return Value - enableCopies</span></span>

## <a name="method-enabledevice"></a><span data-ttu-id="7c5d2-288">メソッド enableDevice</span><span class="sxs-lookup"><span data-stu-id="7c5d2-288">Method enableDevice</span></span>

```xpp
public boolean enableDevice([boolean enable])
```

### <a name="parameters---enabledevice"></a><span data-ttu-id="7c5d2-289">パラメーター - enableDevice</span><span class="sxs-lookup"><span data-stu-id="7c5d2-289">Parameters - enableDevice</span></span>

<span data-ttu-id="7c5d2-290">enable</span><span class="sxs-lookup"><span data-stu-id="7c5d2-290">enable</span></span>  

### <a name="return-value---enabledevice"></a><span data-ttu-id="7c5d2-291">戻り値 - enableDevice</span><span class="sxs-lookup"><span data-stu-id="7c5d2-291">Return Value - enableDevice</span></span>

## <a name="method-enablepages"></a><span data-ttu-id="7c5d2-292">メソッド enablePages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-292">Method enablePages</span></span>

```xpp
public boolean enablePages([boolean enable])
```

### <a name="parameters---enablepages"></a><span data-ttu-id="7c5d2-293">パラメーター - enablePages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-293">Parameters - enablePages</span></span>

<span data-ttu-id="7c5d2-294">enable</span><span class="sxs-lookup"><span data-stu-id="7c5d2-294">enable</span></span>  

### <a name="return-value---enablepages"></a><span data-ttu-id="7c5d2-295">戻り値 - enablePages</span><span class="sxs-lookup"><span data-stu-id="7c5d2-295">Return Value - enablePages</span></span>

## <a name="method-enableproperties"></a><span data-ttu-id="7c5d2-296">メソッド enableProperties</span><span class="sxs-lookup"><span data-stu-id="7c5d2-296">Method enableProperties</span></span>

```xpp
public boolean enableProperties([boolean enable])
```

### <a name="parameters---enableproperties"></a><span data-ttu-id="7c5d2-297">パラメーター - enableProperties</span><span class="sxs-lookup"><span data-stu-id="7c5d2-297">Parameters - enableProperties</span></span>

<span data-ttu-id="7c5d2-298">enable</span><span class="sxs-lookup"><span data-stu-id="7c5d2-298">enable</span></span>  

### <a name="return-value---enableproperties"></a><span data-ttu-id="7c5d2-299">戻り値 - enableProperties</span><span class="sxs-lookup"><span data-stu-id="7c5d2-299">Return Value - enableProperties</span></span>

## <a name="method-enablestoreinprintarchive"></a><span data-ttu-id="7c5d2-300">メソッド enableStoreInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="7c5d2-300">Method enableStoreInPrintArchive</span></span>

```xpp
public boolean enableStoreInPrintArchive([boolean enable])
```

### <a name="parameters---enablestoreinprintarchive"></a><span data-ttu-id="7c5d2-301">パラメーター - enableStoreInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="7c5d2-301">Parameters - enableStoreInPrintArchive</span></span>

<span data-ttu-id="7c5d2-302">enable</span><span class="sxs-lookup"><span data-stu-id="7c5d2-302">enable</span></span>  

### <a name="return-value---enablestoreinprintarchive"></a><span data-ttu-id="7c5d2-303">戻り値 - enableStoreInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="7c5d2-303">Return Value - enableStoreInPrintArchive</span></span>

## <a name="method-enabletarget"></a><span data-ttu-id="7c5d2-304">メソッド enableTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-304">Method enableTarget</span></span>

```xpp
public boolean enableTarget([boolean enable])
```

### <a name="parameters---enabletarget"></a><span data-ttu-id="7c5d2-305">パラメーター - enableTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-305">Parameters - enableTarget</span></span>

<span data-ttu-id="7c5d2-306">enable</span><span class="sxs-lookup"><span data-stu-id="7c5d2-306">enable</span></span>  

### <a name="return-value---enabletarget"></a><span data-ttu-id="7c5d2-307">戻り値 - enableTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-307">Return Value - enableTarget</span></span>

## <a name="method-facename2number"></a><span data-ttu-id="7c5d2-308">メソッド facename2number</span><span class="sxs-lookup"><span data-stu-id="7c5d2-308">Method facename2number</span></span>

```xpp
public int facename2number([str facename])
```

### <a name="parameters---facename2number"></a><span data-ttu-id="7c5d2-309">パラメーター - facename2number</span><span class="sxs-lookup"><span data-stu-id="7c5d2-309">Parameters - facename2number</span></span>

<span data-ttu-id="7c5d2-310">facename</span><span class="sxs-lookup"><span data-stu-id="7c5d2-310">facename</span></span>  

### <a name="return-value---facename2number"></a><span data-ttu-id="7c5d2-311">戻り値 - facename2number</span><span class="sxs-lookup"><span data-stu-id="7c5d2-311">Return Value - facename2number</span></span>

## <a name="method-filename"></a><span data-ttu-id="7c5d2-312">メソッド fileName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-312">Method fileName</span></span>

```xpp
public str fileName([str FileName])
```

### <a name="parameters---filename"></a><span data-ttu-id="7c5d2-313">パラメーター - fileName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-313">Parameters - fileName</span></span>

<span data-ttu-id="7c5d2-314">FileName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-314">FileName</span></span>  

### <a name="return-value---filename"></a><span data-ttu-id="7c5d2-315">戻り値 - fileName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-315">Return Value - fileName</span></span>

## <a name="method-fittopage"></a><span data-ttu-id="7c5d2-316">メソッド fitToPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-316">Method fitToPage</span></span>

```xpp
public boolean fitToPage([boolean fit])
```

### <a name="parameters---fittopage"></a><span data-ttu-id="7c5d2-317">パラメーター - fitToPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-317">Parameters - fitToPage</span></span>

<span data-ttu-id="7c5d2-318">fit</span><span class="sxs-lookup"><span data-stu-id="7c5d2-318">fit</span></span>  

### <a name="return-value---fittopage"></a><span data-ttu-id="7c5d2-319">戻り値 - fitToPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-319">Return Value - fitToPage</span></span>

## <a name="method-format"></a><span data-ttu-id="7c5d2-320">メソッド format</span><span class="sxs-lookup"><span data-stu-id="7c5d2-320">Method format</span></span>

```xpp
public PrintFormat format([PrintFormat format])
```

### <a name="parameters---format"></a><span data-ttu-id="7c5d2-321">パラメーター - format</span><span class="sxs-lookup"><span data-stu-id="7c5d2-321">Parameters - format</span></span>

<span data-ttu-id="7c5d2-322">形式</span><span class="sxs-lookup"><span data-stu-id="7c5d2-322">format</span></span>  

### <a name="return-value---format"></a><span data-ttu-id="7c5d2-323">戻り値 - format</span><span class="sxs-lookup"><span data-stu-id="7c5d2-323">Return Value - format</span></span>

## <a name="method-from"></a><span data-ttu-id="7c5d2-324">メソッド from</span><span class="sxs-lookup"><span data-stu-id="7c5d2-324">Method from</span></span>

```xpp
public int from([int fromPage])
```

### <a name="parameters---from"></a><span data-ttu-id="7c5d2-325">パラメーター - from</span><span class="sxs-lookup"><span data-stu-id="7c5d2-325">Parameters - from</span></span>

<span data-ttu-id="7c5d2-326">fromPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-326">fromPage</span></span>  

### <a name="return-value---from"></a><span data-ttu-id="7c5d2-327">戻り値 - from</span><span class="sxs-lookup"><span data-stu-id="7c5d2-327">Return Value - from</span></span>

## <a name="method-getfacename"></a><span data-ttu-id="7c5d2-328">メソッド getFacename</span><span class="sxs-lookup"><span data-stu-id="7c5d2-328">Method getFacename</span></span>

```xpp
public str getFacename(int number)
```

### <a name="parameters---getfacename"></a><span data-ttu-id="7c5d2-329">パラメーター - getFacename</span><span class="sxs-lookup"><span data-stu-id="7c5d2-329">Parameters - getFacename</span></span>

<span data-ttu-id="7c5d2-330">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-330">number</span></span>  

### <a name="return-value---getfacename"></a><span data-ttu-id="7c5d2-331">戻り値 - getFacename</span><span class="sxs-lookup"><span data-stu-id="7c5d2-331">Return Value - getFacename</span></span>

## <a name="method-getfacenameinfo"></a><span data-ttu-id="7c5d2-332">メソッド getFacenameInfo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-332">Method getFacenameInfo</span></span>

```xpp
public str getFacenameInfo(int number)
```

### <a name="parameters---getfacenameinfo"></a><span data-ttu-id="7c5d2-333">パラメーター - getFacenameInfo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-333">Parameters - getFacenameInfo</span></span>

<span data-ttu-id="7c5d2-334">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-334">number</span></span>  

### <a name="return-value---getfacenameinfo"></a><span data-ttu-id="7c5d2-335">戻り値 - getFacenameInfo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-335">Return Value - getFacenameInfo</span></span>

## <a name="method-getfontinfo"></a><span data-ttu-id="7c5d2-336">メソッド getFontInfo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-336">Method getFontInfo</span></span>

```xpp
public Struct getFontInfo(str fontName)
```

### <a name="parameters---getfontinfo"></a><span data-ttu-id="7c5d2-337">パラメーター - getFontInfo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-337">Parameters - getFontInfo</span></span>

<span data-ttu-id="7c5d2-338">fontName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-338">fontName</span></span>  

### <a name="return-value---getfontinfo"></a><span data-ttu-id="7c5d2-339">戻り値 - getFontInfo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-339">Return Value - getFontInfo</span></span>

## <a name="method-getglyphwidthsarray"></a><span data-ttu-id="7c5d2-340">メソッド getGlyphWidthsArray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-340">Method getGlyphWidthsArray</span></span>

```xpp
public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)
```

### <a name="parameters---getglyphwidthsarray"></a><span data-ttu-id="7c5d2-341">パラメーター - getGlyphWidthsArray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-341">Parameters - getGlyphWidthsArray</span></span>

<span data-ttu-id="7c5d2-342">fontName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-342">fontName</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-343">firstChar</span><span class="sxs-lookup"><span data-stu-id="7c5d2-343">firstChar</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-344">lastChar</span><span class="sxs-lookup"><span data-stu-id="7c5d2-344">lastChar</span></span>  

### <a name="return-value---getglyphwidthsarray"></a><span data-ttu-id="7c5d2-345">戻り値 - getGlyphWidthsArray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-345">Return Value - getGlyphWidthsArray</span></span>

## <a name="method-getnumberofclientprinters"></a><span data-ttu-id="7c5d2-346">メソッド getNumberOfClientPrinters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-346">Method getNumberOfClientPrinters</span></span>

```xpp
public int getNumberOfClientPrinters()
```

### <a name="return-value---getnumberofclientprinters"></a><span data-ttu-id="7c5d2-347">戻り値 - getNumberOfClientPrinters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-347">Return Value - getNumberOfClientPrinters</span></span>

## <a name="method-getnumberoffacenames"></a><span data-ttu-id="7c5d2-348">メソッド getNumberOfFacenames</span><span class="sxs-lookup"><span data-stu-id="7c5d2-348">Method getNumberOfFacenames</span></span>

```xpp
public int getNumberOfFacenames()
```

### <a name="return-value---getnumberoffacenames"></a><span data-ttu-id="7c5d2-349">戻り値 - getNumberOfFacenames</span><span class="sxs-lookup"><span data-stu-id="7c5d2-349">Return Value - getNumberOfFacenames</span></span>

## <a name="method-getnumberofprinters"></a><span data-ttu-id="7c5d2-350">メソッド getNumberOfPrinters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-350">Method getNumberOfPrinters</span></span>

<span data-ttu-id="7c5d2-351">コンピューターに設定されているプリンターの数を返します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-351">Returns the number of printers that are set up on the computer.</span></span>

```xpp
public int getNumberOfPrinters()
```

### <a name="return-value---getnumberofprinters"></a><span data-ttu-id="7c5d2-352">戻り値 - getNumberOfPrinters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-352">Return Value - getNumberOfPrinters</span></span>

<span data-ttu-id="7c5d2-353">コンピューターに設定されているプリンターの数。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-353">The number of printers that are set up on the computer.</span></span>

## <a name="method-getnumberofserverprinters"></a><span data-ttu-id="7c5d2-354">メソッド getNumberOfServerPrinters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-354">Method getNumberOfServerPrinters</span></span>

```xpp
public int getNumberOfServerPrinters()
```

### <a name="return-value---getnumberofserverprinters"></a><span data-ttu-id="7c5d2-355">戻り値 - getNumberOfServerPrinters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-355">Return Value - getNumberOfServerPrinters</span></span>

## <a name="method-getnumberoftrays"></a><span data-ttu-id="7c5d2-356">メソッド getNumberOfTrays</span><span class="sxs-lookup"><span data-stu-id="7c5d2-356">Method getNumberOfTrays</span></span>

```xpp
public int getNumberOfTrays()
```

### <a name="return-value---getnumberoftrays"></a><span data-ttu-id="7c5d2-357">返り値 - getNumberOfTrays</span><span class="sxs-lookup"><span data-stu-id="7c5d2-357">Return Value - getNumberOfTrays</span></span>

## <a name="method-getprinter"></a><span data-ttu-id="7c5d2-358">メソッド getPrinter</span><span class="sxs-lookup"><span data-stu-id="7c5d2-358">Method getPrinter</span></span>

<span data-ttu-id="7c5d2-359">プリンターの deviceName を取得します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-359">Gets the deviceName of a printer.</span></span>

```xpp
public str getPrinter(int number)
```

### <a name="parameters---getprinter"></a><span data-ttu-id="7c5d2-360">パラメーター - getPrinter</span><span class="sxs-lookup"><span data-stu-id="7c5d2-360">Parameters - getPrinter</span></span>

<span data-ttu-id="7c5d2-361">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-361">number</span></span>  
<span data-ttu-id="7c5d2-362">1 から使用可能なプリンターの数までの値。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-362">A value between 1 and the number of available printers.</span></span>

### <a name="return-value---getprinter"></a><span data-ttu-id="7c5d2-363">戻り値 - getPrinter</span><span class="sxs-lookup"><span data-stu-id="7c5d2-363">Return Value - getPrinter</span></span>

<span data-ttu-id="7c5d2-364">指定されたプリンター番号の deviceName。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-364">The deviceName of the given printer number.</span></span>

### <a name="examples---getprinter"></a><span data-ttu-id="7c5d2-365">例 - getPrinter</span><span class="sxs-lookup"><span data-stu-id="7c5d2-365">Examples - getPrinter</span></span>

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

## <a name="method-getrunon"></a><span data-ttu-id="7c5d2-366">メソッド getRunOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-366">Method getRunOn</span></span>

```xpp
public ClassRunMode getRunOn(int number)
```

### <a name="parameters---getrunon"></a><span data-ttu-id="7c5d2-367">パラメーター - getRunOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-367">Parameters - getRunOn</span></span>

<span data-ttu-id="7c5d2-368">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-368">number</span></span>  

### <a name="return-value---getrunon"></a><span data-ttu-id="7c5d2-369">戻り値 - getRunOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-369">Return Value - getRunOn</span></span>

## <a name="method-gettarget"></a><span data-ttu-id="7c5d2-370">メソッド getTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-370">Method getTarget</span></span>

```xpp
public PrintMedium getTarget()
```

### <a name="return-value---gettarget"></a><span data-ttu-id="7c5d2-371">戻り値 - getTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-371">Return Value - getTarget</span></span>

## <a name="method-gettray"></a><span data-ttu-id="7c5d2-372">メソッド getTray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-372">Method getTray</span></span>

```xpp
public int getTray(int number)
```

### <a name="parameters---gettray"></a><span data-ttu-id="7c5d2-373">パラメーター - getTray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-373">Parameters - getTray</span></span>

<span data-ttu-id="7c5d2-374">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-374">number</span></span>  

### <a name="return-value---gettray"></a><span data-ttu-id="7c5d2-375">戻り値 - getTray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-375">Return Value - getTray</span></span>

## <a name="method-gettrayname"></a><span data-ttu-id="7c5d2-376">メソッド getTrayName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-376">Method getTrayName</span></span>

```xpp
public str getTrayName(int number)
```

### <a name="parameters---gettrayname"></a><span data-ttu-id="7c5d2-377">パラメーター - getTrayName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-377">Parameters - getTrayName</span></span>

<span data-ttu-id="7c5d2-378">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-378">number</span></span>  

### <a name="return-value---gettrayname"></a><span data-ttu-id="7c5d2-379">戻り値 - getTrayName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-379">Return Value - getTrayName</span></span>

## <a name="method-hdc"></a><span data-ttu-id="7c5d2-380">メソッド hDC</span><span class="sxs-lookup"><span data-stu-id="7c5d2-380">Method hDC</span></span>

```xpp
public Int64 hDC()
```

### <a name="return-value---hdc"></a><span data-ttu-id="7c5d2-381">戻り値 - hDC</span><span class="sxs-lookup"><span data-stu-id="7c5d2-381">Return Value - hDC</span></span>

## <a name="method-lockdestinationproperties"></a><span data-ttu-id="7c5d2-382">メソッド lockDestinationProperties</span><span class="sxs-lookup"><span data-stu-id="7c5d2-382">Method lockDestinationProperties</span></span>

```xpp
public boolean lockDestinationProperties([boolean warn])
```

### <a name="parameters---lockdestinationproperties"></a><span data-ttu-id="7c5d2-383">パラメーター - lockDestinationProperties</span><span class="sxs-lookup"><span data-stu-id="7c5d2-383">Parameters - lockDestinationProperties</span></span>

<span data-ttu-id="7c5d2-384">警告</span><span class="sxs-lookup"><span data-stu-id="7c5d2-384">warn</span></span>  

### <a name="return-value---lockdestinationproperties"></a><span data-ttu-id="7c5d2-385">戻り値 - lockDestinationProperties</span><span class="sxs-lookup"><span data-stu-id="7c5d2-385">Return Value - lockDestinationProperties</span></span>

## <a name="method-mailcc"></a><span data-ttu-id="7c5d2-386">メソッド mailCc</span><span class="sxs-lookup"><span data-stu-id="7c5d2-386">Method mailCc</span></span>

```xpp
public str mailCc([str MailCc])
```

### <a name="parameters---mailcc"></a><span data-ttu-id="7c5d2-387">パラメーター - mailCc</span><span class="sxs-lookup"><span data-stu-id="7c5d2-387">Parameters - mailCc</span></span>

<span data-ttu-id="7c5d2-388">MailCc</span><span class="sxs-lookup"><span data-stu-id="7c5d2-388">MailCc</span></span>  

### <a name="return-value---mailcc"></a><span data-ttu-id="7c5d2-389">戻り値 - mailCc</span><span class="sxs-lookup"><span data-stu-id="7c5d2-389">Return Value - mailCc</span></span>

## <a name="method-mailsubject"></a><span data-ttu-id="7c5d2-390">メソッド mailSubject</span><span class="sxs-lookup"><span data-stu-id="7c5d2-390">Method mailSubject</span></span>

```xpp
public str mailSubject([str MailSubject])
```

### <a name="parameters---mailsubject"></a><span data-ttu-id="7c5d2-391">パラメーター - mailSubject</span><span class="sxs-lookup"><span data-stu-id="7c5d2-391">Parameters - mailSubject</span></span>

<span data-ttu-id="7c5d2-392">MailSubject</span><span class="sxs-lookup"><span data-stu-id="7c5d2-392">MailSubject</span></span>  

### <a name="return-value---mailsubject"></a><span data-ttu-id="7c5d2-393">戻り値 - mailSubject</span><span class="sxs-lookup"><span data-stu-id="7c5d2-393">Return Value - mailSubject</span></span>

## <a name="method-mailto"></a><span data-ttu-id="7c5d2-394">メソッド mailTo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-394">Method mailTo</span></span>

```xpp
public str mailTo([str MailTo])
```

### <a name="parameters---mailto"></a><span data-ttu-id="7c5d2-395">パラメーター - mailTo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-395">Parameters - mailTo</span></span>

<span data-ttu-id="7c5d2-396">MailTo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-396">MailTo</span></span>  

### <a name="return-value---mailto"></a><span data-ttu-id="7c5d2-397">戻り値 - mailTo</span><span class="sxs-lookup"><span data-stu-id="7c5d2-397">Return Value - mailTo</span></span>

## <a name="method-numberofcopydescriptions"></a><span data-ttu-id="7c5d2-398">メソッド numberOfCopyDescriptions</span><span class="sxs-lookup"><span data-stu-id="7c5d2-398">Method numberOfCopyDescriptions</span></span>

```xpp
public int numberOfCopyDescriptions(int number)
```

### <a name="parameters---numberofcopydescriptions"></a><span data-ttu-id="7c5d2-399">パラメーター - numberOfCopyDescriptions</span><span class="sxs-lookup"><span data-stu-id="7c5d2-399">Parameters - numberOfCopyDescriptions</span></span>

<span data-ttu-id="7c5d2-400">番号</span><span class="sxs-lookup"><span data-stu-id="7c5d2-400">number</span></span>  

### <a name="return-value---numberofcopydescriptions"></a><span data-ttu-id="7c5d2-401">戻り値 - numberOfCopyDescriptions</span><span class="sxs-lookup"><span data-stu-id="7c5d2-401">Return Value - numberOfCopyDescriptions</span></span>

## <a name="method-outputtoclient"></a><span data-ttu-id="7c5d2-402">メソッド outputToClient</span><span class="sxs-lookup"><span data-stu-id="7c5d2-402">Method outputToClient</span></span>

```xpp
public boolean outputToClient([boolean toClient])
```

### <a name="parameters---outputtoclient"></a><span data-ttu-id="7c5d2-403">パラメーター - outputToClient</span><span class="sxs-lookup"><span data-stu-id="7c5d2-403">Parameters - outputToClient</span></span>

<span data-ttu-id="7c5d2-404">toClient</span><span class="sxs-lookup"><span data-stu-id="7c5d2-404">toClient</span></span>  

### <a name="return-value---outputtoclient"></a><span data-ttu-id="7c5d2-405">戻り値 - outputToClient</span><span class="sxs-lookup"><span data-stu-id="7c5d2-405">Return Value - outputToClient</span></span>

## <a name="method-outputtoprnfile"></a><span data-ttu-id="7c5d2-406">メソッド outputToPrnFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-406">Method outputToPrnFile</span></span>

```xpp
public boolean outputToPrnFile([boolean writePrnFile])
```

### <a name="parameters---outputtoprnfile"></a><span data-ttu-id="7c5d2-407">パラメーター - outputToPrnFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-407">Parameters - outputToPrnFile</span></span>

<span data-ttu-id="7c5d2-408">writePrnFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-408">writePrnFile</span></span>  

### <a name="return-value---outputtoprnfile"></a><span data-ttu-id="7c5d2-409">戻り値 - outputToPrnFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-409">Return Value - outputToPrnFile</span></span>

## <a name="method-packnamesandprinterdata"></a><span data-ttu-id="7c5d2-410">メソッド packNamesAndPrinterData</span><span class="sxs-lookup"><span data-stu-id="7c5d2-410">Method packNamesAndPrinterData</span></span>

```xpp
public container packNamesAndPrinterData()
```

### <a name="return-value---packnamesandprinterdata"></a><span data-ttu-id="7c5d2-411">戻り値 - packNamesAndPrinterData</span><span class="sxs-lookup"><span data-stu-id="7c5d2-411">Return Value - packNamesAndPrinterData</span></span>

## <a name="method-packpagesettings"></a><span data-ttu-id="7c5d2-412">メソッド packPageSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-412">Method packPageSettings</span></span>

<span data-ttu-id="7c5d2-413">ページの書式設定時に選択されているデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-413">Stores the data that is selected during page formatting in a container.</span></span>

```xpp
public container packPageSettings()
```

### <a name="return-value---packpagesettings"></a><span data-ttu-id="7c5d2-414">戻り値 - packPageSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-414">Return Value - packPageSettings</span></span>

<span data-ttu-id="7c5d2-415">ページの書式設定時に選択されているデータを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-415">A container that holds data that is selected during page formatting.</span></span>

### <a name="remarks---packpagesettings"></a><span data-ttu-id="7c5d2-416">備考 - packPageSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-416">Remarks - packPageSettings</span></span>

<span data-ttu-id="7c5d2-417">返されたコンテナーは、unpackPageSettings メソッドへの入力として使用できます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-417">The returned container can be used as input to the unpackPageSettings method.</span></span>

## <a name="method-packprintersettings"></a><span data-ttu-id="7c5d2-418">メソッド packPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-418">Method packPrinterSettings</span></span>

```xpp
public container packPrinterSettings()
```

### <a name="return-value---packprintersettings"></a><span data-ttu-id="7c5d2-419">戻り値 - packPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-419">Return Value - packPrinterSettings</span></span>

## <a name="method-packprintjobsettings"></a><span data-ttu-id="7c5d2-420">メソッド packPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-420">Method packPrintJobSettings</span></span>

```xpp
public container packPrintJobSettings()
```

### <a name="return-value---packprintjobsettings"></a><span data-ttu-id="7c5d2-421">戻り値 - packPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-421">Return Value - packPrintJobSettings</span></span>

## <a name="method-packsubtotalsettings"></a><span data-ttu-id="7c5d2-422">メソッド packSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-422">Method packSubtotalSettings</span></span>

```xpp
public container packSubtotalSettings()
```

### <a name="return-value---packsubtotalsettings"></a><span data-ttu-id="7c5d2-423">戻り値 - packSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-423">Return Value - packSubtotalSettings</span></span>

## <a name="method-pagecopy2tray"></a><span data-ttu-id="7c5d2-424">メソッド pageCopy2Tray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-424">Method pageCopy2Tray</span></span>

```xpp
public int pageCopy2Tray(int pageNumber, [int copyNumber])
```

### <a name="parameters---pagecopy2tray"></a><span data-ttu-id="7c5d2-425">パラメーター - pageCopy2Tray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-425">Parameters - pageCopy2Tray</span></span>

<span data-ttu-id="7c5d2-426">pageNumber</span><span class="sxs-lookup"><span data-stu-id="7c5d2-426">pageNumber</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-427">copyNumber</span><span class="sxs-lookup"><span data-stu-id="7c5d2-427">copyNumber</span></span>  

### <a name="return-value---pagecopy2tray"></a><span data-ttu-id="7c5d2-428">戻り値 - pageCopy2Tray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-428">Return Value - pageCopy2Tray</span></span>

## <a name="method-pageformatting"></a><span data-ttu-id="7c5d2-429">メソッド pageFormatting</span><span class="sxs-lookup"><span data-stu-id="7c5d2-429">Method pageFormatting</span></span>

```xpp
public boolean pageFormatting()
```

### <a name="return-value---pageformatting"></a><span data-ttu-id="7c5d2-430">戻り値 - pageFormatting</span><span class="sxs-lookup"><span data-stu-id="7c5d2-430">Return Value - pageFormatting</span></span>

## <a name="method-paperorientation"></a><span data-ttu-id="7c5d2-431">メソッド paperOrientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-431">Method paperOrientation</span></span>

```xpp
public PrinterOrientation paperOrientation([PrinterOrientation orientation])
```

### <a name="parameters---paperorientation"></a><span data-ttu-id="7c5d2-432">パラメーター - paperOrientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-432">Parameters - paperOrientation</span></span>

<span data-ttu-id="7c5d2-433">orientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-433">orientation</span></span>  

### <a name="return-value---paperorientation"></a><span data-ttu-id="7c5d2-434">戻り値 - paperOrientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-434">Return Value - paperOrientation</span></span>

## <a name="method-papertray"></a><span data-ttu-id="7c5d2-435">メソッド paperTray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-435">Method paperTray</span></span>

```xpp
public int paperTray([int tray])
```

### <a name="parameters---papertray"></a><span data-ttu-id="7c5d2-436">パラメーター - paperTray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-436">Parameters - paperTray</span></span>

<span data-ttu-id="7c5d2-437">トレイ</span><span class="sxs-lookup"><span data-stu-id="7c5d2-437">tray</span></span>  

### <a name="return-value---papertray"></a><span data-ttu-id="7c5d2-438">戻り値 - paperTray</span><span class="sxs-lookup"><span data-stu-id="7c5d2-438">Return Value - paperTray</span></span>

## <a name="method-papertrayraw"></a><span data-ttu-id="7c5d2-439">メソッド paperTrayRaw</span><span class="sxs-lookup"><span data-stu-id="7c5d2-439">Method paperTrayRaw</span></span>

```xpp
public int paperTrayRaw([int tray])
```

### <a name="parameters---papertrayraw"></a><span data-ttu-id="7c5d2-440">パラメーター - paperTrayRaw</span><span class="sxs-lookup"><span data-stu-id="7c5d2-440">Parameters - paperTrayRaw</span></span>

<span data-ttu-id="7c5d2-441">トレイ</span><span class="sxs-lookup"><span data-stu-id="7c5d2-441">tray</span></span>  

### <a name="return-value---papertrayraw"></a><span data-ttu-id="7c5d2-442">戻り値 - paperTrayRaw</span><span class="sxs-lookup"><span data-stu-id="7c5d2-442">Return Value - paperTrayRaw</span></span>

## <a name="method-performancetest"></a><span data-ttu-id="7c5d2-443">メソッド performanceTest</span><span class="sxs-lookup"><span data-stu-id="7c5d2-443">Method performanceTest</span></span>

```xpp
public int performanceTest([int loops])
```

### <a name="parameters---performancetest"></a><span data-ttu-id="7c5d2-444">パラメーター - performanceTest</span><span class="sxs-lookup"><span data-stu-id="7c5d2-444">Parameters - performanceTest</span></span>

<span data-ttu-id="7c5d2-445">loops</span><span class="sxs-lookup"><span data-stu-id="7c5d2-445">loops</span></span>  

### <a name="return-value---performancetest"></a><span data-ttu-id="7c5d2-446">戻り値 - performanceTest</span><span class="sxs-lookup"><span data-stu-id="7c5d2-446">Return Value - performanceTest</span></span>

## <a name="method-preferredfileformat"></a><span data-ttu-id="7c5d2-447">メソッド preferredFileFormat</span><span class="sxs-lookup"><span data-stu-id="7c5d2-447">Method preferredFileFormat</span></span>

```xpp
public PrintFormat preferredFileFormat([PrintFormat format])
```

### <a name="parameters---preferredfileformat"></a><span data-ttu-id="7c5d2-448">パラメーター - preferredFileFormat</span><span class="sxs-lookup"><span data-stu-id="7c5d2-448">Parameters - preferredFileFormat</span></span>

<span data-ttu-id="7c5d2-449">形式</span><span class="sxs-lookup"><span data-stu-id="7c5d2-449">format</span></span>  

### <a name="return-value---preferredfileformat"></a><span data-ttu-id="7c5d2-450">戻り値 - preferredFileFormat</span><span class="sxs-lookup"><span data-stu-id="7c5d2-450">Return Value - preferredFileFormat</span></span>

## <a name="method-preferredmailformat"></a><span data-ttu-id="7c5d2-451">メソッド preferredMailFormat</span><span class="sxs-lookup"><span data-stu-id="7c5d2-451">Method preferredMailFormat</span></span>

```xpp
public PrintFormat preferredMailFormat([PrintFormat format])
```

### <a name="parameters---preferredmailformat"></a><span data-ttu-id="7c5d2-452">パラメーター - preferredMailFormat</span><span class="sxs-lookup"><span data-stu-id="7c5d2-452">Parameters - preferredMailFormat</span></span>

<span data-ttu-id="7c5d2-453">形式</span><span class="sxs-lookup"><span data-stu-id="7c5d2-453">format</span></span>  

### <a name="return-value---preferredmailformat"></a><span data-ttu-id="7c5d2-454">戻り値 - preferredMailFormat</span><span class="sxs-lookup"><span data-stu-id="7c5d2-454">Return Value - preferredMailFormat</span></span>

## <a name="method-preferredorientation"></a><span data-ttu-id="7c5d2-455">メソッド preferredOrientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-455">Method preferredOrientation</span></span>

```xpp
public PrinterOrientation preferredOrientation([PrinterOrientation orientation])
```

### <a name="parameters---preferredorientation"></a><span data-ttu-id="7c5d2-456">パラメーター - preferredOrientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-456">Parameters - preferredOrientation</span></span>

<span data-ttu-id="7c5d2-457">orientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-457">orientation</span></span>  

### <a name="return-value---preferredorientation"></a><span data-ttu-id="7c5d2-458">戻り値 - preferredOrientation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-458">Return Value - preferredOrientation</span></span>

## <a name="method-preferredtarget"></a><span data-ttu-id="7c5d2-459">メソッド preferredTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-459">Method preferredTarget</span></span>

```xpp
public PrintMedium preferredTarget([PrintMedium target])
```

### <a name="parameters---preferredtarget"></a><span data-ttu-id="7c5d2-460">パラメーター - preferredTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-460">Parameters - preferredTarget</span></span>

<span data-ttu-id="7c5d2-461">target</span><span class="sxs-lookup"><span data-stu-id="7c5d2-461">target</span></span>  

### <a name="return-value---preferredtarget"></a><span data-ttu-id="7c5d2-462">戻り値 - preferredTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-462">Return Value - preferredTarget</span></span>

## <a name="method-printerattributes"></a><span data-ttu-id="7c5d2-463">メソッド printerAttributes</span><span class="sxs-lookup"><span data-stu-id="7c5d2-463">Method printerAttributes</span></span>

```xpp
public int printerAttributes()
```

### <a name="return-value---printerattributes"></a><span data-ttu-id="7c5d2-464">戻り値 - printerAttributes</span><span class="sxs-lookup"><span data-stu-id="7c5d2-464">Return Value - printerAttributes</span></span>

## <a name="method-printeraverageppm"></a><span data-ttu-id="7c5d2-465">メソッド printerAveragePPM</span><span class="sxs-lookup"><span data-stu-id="7c5d2-465">Method printerAveragePPM</span></span>

```xpp
public int printerAveragePPM()
```

### <a name="return-value---printeraverageppm"></a><span data-ttu-id="7c5d2-466">戻り値 - printerAveragePPM</span><span class="sxs-lookup"><span data-stu-id="7c5d2-466">Return Value - printerAveragePPM</span></span>

## <a name="method-printercomment"></a><span data-ttu-id="7c5d2-467">メソッド printerComment</span><span class="sxs-lookup"><span data-stu-id="7c5d2-467">Method printerComment</span></span>

```xpp
public str printerComment()
```

### <a name="return-value---printercomment"></a><span data-ttu-id="7c5d2-468">戻り値 - printerComment</span><span class="sxs-lookup"><span data-stu-id="7c5d2-468">Return Value - printerComment</span></span>

## <a name="method-printerdatatype"></a><span data-ttu-id="7c5d2-469">メソッド printerDatatype</span><span class="sxs-lookup"><span data-stu-id="7c5d2-469">Method printerDatatype</span></span>

```xpp
public str printerDatatype()
```

### <a name="return-value---printerdatatype"></a><span data-ttu-id="7c5d2-470">戻り値 - printerDatatype</span><span class="sxs-lookup"><span data-stu-id="7c5d2-470">Return Value - printerDatatype</span></span>

## <a name="method-printerdefaultpriority"></a><span data-ttu-id="7c5d2-471">メソッド printerDefaultPriority</span><span class="sxs-lookup"><span data-stu-id="7c5d2-471">Method printerDefaultPriority</span></span>

```xpp
public int printerDefaultPriority()
```

### <a name="return-value---printerdefaultpriority"></a><span data-ttu-id="7c5d2-472">戻り値 - printerDefaultPriority</span><span class="sxs-lookup"><span data-stu-id="7c5d2-472">Return Value - printerDefaultPriority</span></span>

## <a name="method-printerdrivername"></a><span data-ttu-id="7c5d2-473">メソッド printerDriverName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-473">Method printerDriverName</span></span>

```xpp
public str printerDriverName()
```

### <a name="return-value---printerdrivername"></a><span data-ttu-id="7c5d2-474">戻り値 - printerDriverName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-474">Return Value - printerDriverName</span></span>

## <a name="method-printerlocation"></a><span data-ttu-id="7c5d2-475">メソッド printerLocation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-475">Method printerLocation</span></span>

```xpp
public str printerLocation()
```

### <a name="return-value---printerlocation"></a><span data-ttu-id="7c5d2-476">戻り値 - printerLocation</span><span class="sxs-lookup"><span data-stu-id="7c5d2-476">Return Value - printerLocation</span></span>

## <a name="method-printerpageheight"></a><span data-ttu-id="7c5d2-477">メソッド printerPageHeight</span><span class="sxs-lookup"><span data-stu-id="7c5d2-477">Method printerPageHeight</span></span>

```xpp
public int printerPageHeight()
```

### <a name="return-value---printerpageheight"></a><span data-ttu-id="7c5d2-478">戻り値 - printerPageHeight</span><span class="sxs-lookup"><span data-stu-id="7c5d2-478">Return Value - printerPageHeight</span></span>

## <a name="method-printerpagewidth"></a><span data-ttu-id="7c5d2-479">メソッド printerPageWidth</span><span class="sxs-lookup"><span data-stu-id="7c5d2-479">Method printerPageWidth</span></span>

```xpp
public int printerPageWidth()
```

### <a name="return-value---printerpagewidth"></a><span data-ttu-id="7c5d2-480">戻り値 - printerPageWidth</span><span class="sxs-lookup"><span data-stu-id="7c5d2-480">Return Value - printerPageWidth</span></span>

## <a name="method-printerpaper"></a><span data-ttu-id="7c5d2-481">メソッド printerPaper</span><span class="sxs-lookup"><span data-stu-id="7c5d2-481">Method printerPaper</span></span>

```xpp
public int printerPaper()
```

### <a name="return-value---printerpaper"></a><span data-ttu-id="7c5d2-482">戻り値 - printerPaper</span><span class="sxs-lookup"><span data-stu-id="7c5d2-482">Return Value - printerPaper</span></span>

## <a name="method-printerparameters"></a><span data-ttu-id="7c5d2-483">メソッド printerParameters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-483">Method printerParameters</span></span>

```xpp
public str printerParameters()
```

### <a name="return-value---printerparameters"></a><span data-ttu-id="7c5d2-484">戻り値 - printerParameters</span><span class="sxs-lookup"><span data-stu-id="7c5d2-484">Return Value - printerParameters</span></span>

## <a name="method-printerportname"></a><span data-ttu-id="7c5d2-485">メソッド printerPortName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-485">Method printerPortName</span></span>

```xpp
public str printerPortName()
```

### <a name="return-value---printerportname"></a><span data-ttu-id="7c5d2-486">戻り値 - printerPortName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-486">Return Value - printerPortName</span></span>

## <a name="method-printerprintername"></a><span data-ttu-id="7c5d2-487">メソッド printerPrinterName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-487">Method printerPrinterName</span></span>

```xpp
public str printerPrinterName()
```

### <a name="return-value---printerprintername"></a><span data-ttu-id="7c5d2-488">戻り値 - printerPrinterName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-488">Return Value - printerPrinterName</span></span>

## <a name="method-printerprintprocessor"></a><span data-ttu-id="7c5d2-489">メソッド printerPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="7c5d2-489">Method printerPrintProcessor</span></span>

```xpp
public str printerPrintProcessor()
```

### <a name="return-value---printerprintprocessor"></a><span data-ttu-id="7c5d2-490">戻り値 - printerPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="7c5d2-490">Return Value - printerPrintProcessor</span></span>

## <a name="method-printerpriority"></a><span data-ttu-id="7c5d2-491">メソッド printerPriority</span><span class="sxs-lookup"><span data-stu-id="7c5d2-491">Method printerPriority</span></span>

```xpp
public int printerPriority()
```

### <a name="return-value---printerpriority"></a><span data-ttu-id="7c5d2-492">戻り値 - printerPriority</span><span class="sxs-lookup"><span data-stu-id="7c5d2-492">Return Value - printerPriority</span></span>

## <a name="method-printerqueuedjobs"></a><span data-ttu-id="7c5d2-493">メソッド printerQueuedJobs</span><span class="sxs-lookup"><span data-stu-id="7c5d2-493">Method printerQueuedJobs</span></span>

```xpp
public int printerQueuedJobs()
```

### <a name="return-value---printerqueuedjobs"></a><span data-ttu-id="7c5d2-494">戻り値 - printerQueuedJobs</span><span class="sxs-lookup"><span data-stu-id="7c5d2-494">Return Value - printerQueuedJobs</span></span>

## <a name="method-printerrunon"></a><span data-ttu-id="7c5d2-495">メソッド printerRunOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-495">Method printerRunOn</span></span>

```xpp
public ClassRunMode printerRunOn()
```

### <a name="return-value---printerrunon"></a><span data-ttu-id="7c5d2-496">戻り値 - printerRunOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-496">Return Value - printerRunOn</span></span>

## <a name="method-printersepfile"></a><span data-ttu-id="7c5d2-497">メソッド printerSepFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-497">Method printerSepFile</span></span>

```xpp
public str printerSepFile()
```

### <a name="return-value---printersepfile"></a><span data-ttu-id="7c5d2-498">戻り値 - printerSepFile</span><span class="sxs-lookup"><span data-stu-id="7c5d2-498">Return Value - printerSepFile</span></span>

## <a name="method-printerservername"></a><span data-ttu-id="7c5d2-499">メソッド printerServerName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-499">Method printerServerName</span></span>

```xpp
public str printerServerName()
```

### <a name="return-value---printerservername"></a><span data-ttu-id="7c5d2-500">戻り値 - printerServerName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-500">Return Value - printerServerName</span></span>

## <a name="method-printersettings"></a><span data-ttu-id="7c5d2-501">メソッド printerSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-501">Method printerSettings</span></span>

```xpp
public boolean printerSettings(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])
```

### <a name="parameters---printersettings"></a><span data-ttu-id="7c5d2-502">パラメーター - printerSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-502">Parameters - printerSettings</span></span>

<span data-ttu-id="7c5d2-503">formName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-503">formName</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-504">args</span><span class="sxs-lookup"><span data-stu-id="7c5d2-504">args</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-505">reportRun</span><span class="sxs-lookup"><span data-stu-id="7c5d2-505">reportRun</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-506">showWhat</span><span class="sxs-lookup"><span data-stu-id="7c5d2-506">showWhat</span></span>  

### <a name="return-value---printersettings"></a><span data-ttu-id="7c5d2-507">戻り値 - printerSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-507">Return Value - printerSettings</span></span>

## <a name="method-printersharename"></a><span data-ttu-id="7c5d2-508">メソッド printerShareName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-508">Method printerShareName</span></span>

```xpp
public str printerShareName()
```

### <a name="return-value---printersharename"></a><span data-ttu-id="7c5d2-509">戻り値 - printerShareName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-509">Return Value - printerShareName</span></span>

## <a name="method-printerstarttime"></a><span data-ttu-id="7c5d2-510">メソッド printerStartTime</span><span class="sxs-lookup"><span data-stu-id="7c5d2-510">Method printerStartTime</span></span>

```xpp
public TimeOfDay printerStartTime()
```

### <a name="return-value---printerstarttime"></a><span data-ttu-id="7c5d2-511">戻り値 - printerStartTime</span><span class="sxs-lookup"><span data-stu-id="7c5d2-511">Return Value - printerStartTime</span></span>

## <a name="method-printerstatus"></a><span data-ttu-id="7c5d2-512">メソッド printerStatus</span><span class="sxs-lookup"><span data-stu-id="7c5d2-512">Method printerStatus</span></span>

```xpp
public int printerStatus()
```

### <a name="return-value---printerstatus"></a><span data-ttu-id="7c5d2-513">戻り値 - printerStatus</span><span class="sxs-lookup"><span data-stu-id="7c5d2-513">Return Value - printerStatus</span></span>

## <a name="method-printeruntiltime"></a><span data-ttu-id="7c5d2-514">メソッド printerUntilTime</span><span class="sxs-lookup"><span data-stu-id="7c5d2-514">Method printerUntilTime</span></span>

```xpp
public TimeOfDay printerUntilTime()
```

### <a name="return-value---printeruntiltime"></a><span data-ttu-id="7c5d2-515">戻り値 - printerUntilTime</span><span class="sxs-lookup"><span data-stu-id="7c5d2-515">Return Value - printerUntilTime</span></span>

## <a name="method-reportrun"></a><span data-ttu-id="7c5d2-516">メソッド reportRun</span><span class="sxs-lookup"><span data-stu-id="7c5d2-516">Method reportRun</span></span>

```xpp
public ReportRun reportRun()
```

### <a name="return-value---reportrun"></a><span data-ttu-id="7c5d2-517">戻り値 - reportRun</span><span class="sxs-lookup"><span data-stu-id="7c5d2-517">Return Value - reportRun</span></span>

## <a name="method-requesteddevicename"></a><span data-ttu-id="7c5d2-518">メソッド requestedDeviceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-518">Method requestedDeviceName</span></span>

```xpp
public str requestedDeviceName()
```

### <a name="return-value---requesteddevicename"></a><span data-ttu-id="7c5d2-519">戻り値 - requestedDeviceName</span><span class="sxs-lookup"><span data-stu-id="7c5d2-519">Return Value - requestedDeviceName</span></span>

## <a name="method-requestedrunon"></a><span data-ttu-id="7c5d2-520">メソッド requestedRunOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-520">Method requestedRunOn</span></span>

```xpp
public ClassRunMode requestedRunOn()
```

### <a name="return-value---requestedrunon"></a><span data-ttu-id="7c5d2-521">戻り値 - requestedRunOn</span><span class="sxs-lookup"><span data-stu-id="7c5d2-521">Return Value - requestedRunOn</span></span>

## <a name="method-runclient"></a><span data-ttu-id="7c5d2-522">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="7c5d2-522">Method runClient</span></span>

```xpp
public boolean runClient()
```

### <a name="return-value---runclient"></a><span data-ttu-id="7c5d2-523">戻り値 - runClient</span><span class="sxs-lookup"><span data-stu-id="7c5d2-523">Return Value - runClient</span></span>

## <a name="method-runserver"></a><span data-ttu-id="7c5d2-524">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="7c5d2-524">Method runServer</span></span>

```xpp
public boolean runServer()
```

### <a name="return-value---runserver"></a><span data-ttu-id="7c5d2-525">戻り値 - runServer</span><span class="sxs-lookup"><span data-stu-id="7c5d2-525">Return Value - runServer</span></span>

## <a name="method-sectionsperpage"></a><span data-ttu-id="7c5d2-526">メソッド sectionsPerPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-526">Method sectionsPerPage</span></span>

```xpp
public int sectionsPerPage([int sectionsPerPage])
```

### <a name="parameters---sectionsperpage"></a><span data-ttu-id="7c5d2-527">パラメーター - sectionsPerPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-527">Parameters - sectionsPerPage</span></span>

<span data-ttu-id="7c5d2-528">sectionsPerPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-528">sectionsPerPage</span></span>  

### <a name="return-value---sectionsperpage"></a><span data-ttu-id="7c5d2-529">戻り値 - sectionsPerPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-529">Return Value - sectionsPerPage</span></span>

## <a name="method-settarget"></a><span data-ttu-id="7c5d2-530">メソッド setTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-530">Method setTarget</span></span>

<span data-ttu-id="7c5d2-531">印刷メディアを設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-531">Sets the print medium.</span></span>

```xpp
public PrintMedium setTarget(PrintMedium target)
```

### <a name="parameters---settarget"></a><span data-ttu-id="7c5d2-532">パラメーター - setTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-532">Parameters - setTarget</span></span>

<span data-ttu-id="7c5d2-533">target</span><span class="sxs-lookup"><span data-stu-id="7c5d2-533">target</span></span>  
<span data-ttu-id="7c5d2-534">印刷メディア。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-534">The print medium.</span></span>

### <a name="return-value---settarget"></a><span data-ttu-id="7c5d2-535">戻り値 - setTarget</span><span class="sxs-lookup"><span data-stu-id="7c5d2-535">Return Value - setTarget</span></span>

<span data-ttu-id="7c5d2-536">印刷メディア。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-536">The print medium.</span></span>

## <a name="method-singlelargepage"></a><span data-ttu-id="7c5d2-537">メソッド singleLargePage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-537">Method singleLargePage</span></span>

```xpp
public boolean singleLargePage([boolean singleLargePage])
```

### <a name="parameters---singlelargepage"></a><span data-ttu-id="7c5d2-538">パラメーター - singleLargePage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-538">Parameters - singleLargePage</span></span>

<span data-ttu-id="7c5d2-539">singleLargePage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-539">singleLargePage</span></span>  

### <a name="return-value---singlelargepage"></a><span data-ttu-id="7c5d2-540">戻り値 - singleLargePage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-540">Return Value - singleLargePage</span></span>

## <a name="method-skipbitmapsinrtf"></a><span data-ttu-id="7c5d2-541">メソッド skipBitmapsInRTF</span><span class="sxs-lookup"><span data-stu-id="7c5d2-541">Method skipBitmapsInRTF</span></span>

<span data-ttu-id="7c5d2-542">.rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-542">Controls whether bitmaps are included when reports are printed to an .rtf file.</span></span>

```xpp
public boolean skipBitmapsInRTF([boolean skipBitmaps])
```

### <a name="parameters---skipbitmapsinrtf"></a><span data-ttu-id="7c5d2-543">パラメーター - skipBitmapsInRTF</span><span class="sxs-lookup"><span data-stu-id="7c5d2-543">Parameters - skipBitmapsInRTF</span></span>

<span data-ttu-id="7c5d2-544">skipBitmaps</span><span class="sxs-lookup"><span data-stu-id="7c5d2-544">skipBitmaps</span></span>  
<span data-ttu-id="7c5d2-545">ビットマップが含まれるかどうかを判断するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-545">A boolean flag that determines whether bitmaps are included; optional.</span></span>

### <a name="return-value---skipbitmapsinrtf"></a><span data-ttu-id="7c5d2-546">戻り値 - skipBitmapsInRTF</span><span class="sxs-lookup"><span data-stu-id="7c5d2-546">Return Value - skipBitmapsInRTF</span></span>

<span data-ttu-id="7c5d2-547">ビットマップが含まれる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-547">true if the bitmaps are included; otherwise, false.</span></span>

## <a name="method-storeinprintarchive"></a><span data-ttu-id="7c5d2-548">メソッド storeInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="7c5d2-548">Method storeInPrintArchive</span></span>

```xpp
public boolean storeInPrintArchive([boolean store])
```

### <a name="parameters---storeinprintarchive"></a><span data-ttu-id="7c5d2-549">パラメーター - storeInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="7c5d2-549">Parameters - storeInPrintArchive</span></span>

<span data-ttu-id="7c5d2-550">店舗</span><span class="sxs-lookup"><span data-stu-id="7c5d2-550">store</span></span>  

### <a name="return-value---storeinprintarchive"></a><span data-ttu-id="7c5d2-551">戻り値 - storeInPrintArchive</span><span class="sxs-lookup"><span data-stu-id="7c5d2-551">Return Value - storeInPrintArchive</span></span>

## <a name="method-suppressscalingmessage"></a><span data-ttu-id="7c5d2-552">メソッド suppressScalingMessage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-552">Method suppressScalingMessage</span></span>

```xpp
public boolean suppressScalingMessage([boolean suppress])
```

### <a name="parameters---suppressscalingmessage"></a><span data-ttu-id="7c5d2-553">パラメーター - suppressScalingMessage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-553">Parameters - suppressScalingMessage</span></span>

<span data-ttu-id="7c5d2-554">suppress</span><span class="sxs-lookup"><span data-stu-id="7c5d2-554">suppress</span></span>  

### <a name="return-value---suppressscalingmessage"></a><span data-ttu-id="7c5d2-555">戻り値 - suppressScalingMessage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-555">Return Value - suppressScalingMessage</span></span>

## <a name="method-to"></a><span data-ttu-id="7c5d2-556">メソッド to</span><span class="sxs-lookup"><span data-stu-id="7c5d2-556">Method to</span></span>

```xpp
public int to([int toPage])
```

### <a name="parameters---to"></a><span data-ttu-id="7c5d2-557">パラメーター - to</span><span class="sxs-lookup"><span data-stu-id="7c5d2-557">Parameters - to</span></span>

<span data-ttu-id="7c5d2-558">toPage</span><span class="sxs-lookup"><span data-stu-id="7c5d2-558">toPage</span></span>  

### <a name="return-value---to"></a><span data-ttu-id="7c5d2-559">戻り値 - to</span><span class="sxs-lookup"><span data-stu-id="7c5d2-559">Return Value - to</span></span>

## <a name="method-tostring"></a><span data-ttu-id="7c5d2-560">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="7c5d2-560">Method toString</span></span>

<span data-ttu-id="7c5d2-561">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-561">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="7c5d2-562">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="7c5d2-562">Return Value - toString</span></span>

<span data-ttu-id="7c5d2-563">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-563">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="7c5d2-564">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="7c5d2-564">Remarks - toString</span></span>

<span data-ttu-id="7c5d2-565">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-565">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="7c5d2-566">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-566">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="7c5d2-567">たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-567">For example, an instance of the class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-unpackpagesettings"></a><span data-ttu-id="7c5d2-568">メソッド unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-568">Method unpackPageSettings</span></span>

<span data-ttu-id="7c5d2-569">用紙サイズと向きなど、ページ設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-569">Sets the page settings, such as paper size and orientation.</span></span>

```xpp
public boolean unpackPageSettings(container settings)
```

### <a name="parameters---unpackpagesettings"></a><span data-ttu-id="7c5d2-570">パラメーター - unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-570">Parameters - unpackPageSettings</span></span>

<span data-ttu-id="7c5d2-571">設定</span><span class="sxs-lookup"><span data-stu-id="7c5d2-571">settings</span></span>  
<span data-ttu-id="7c5d2-572">packPageSettings メソッドを呼び出して取得されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-572">A container that is obtained by calling the packPageSettings method.</span></span>

### <a name="return-value---unpackpagesettings"></a><span data-ttu-id="7c5d2-573">戻り値 - unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-573">Return Value - unpackPageSettings</span></span>

<span data-ttu-id="7c5d2-574">pageSettings が正常に変更された場合は true。pageSettings が既定値に設定された場合は false。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-574">true if the pageSettings were successfully changed; false if the pageSettings were set to the default values.</span></span>

### <a name="remarks---unpackpagesettings"></a><span data-ttu-id="7c5d2-575">備考 - unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-575">Remarks - unpackPageSettings</span></span>

<span data-ttu-id="7c5d2-576">reportDesign クラスと report クラスには、同じ名前のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-576">The classes reportDesign and report have a method with the same name.</span></span>

## <a name="method-unpackprintersettings"></a><span data-ttu-id="7c5d2-577">メソッド unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-577">Method unpackPrinterSettings</span></span>

```xpp
public boolean unpackPrinterSettings(container settings)
```

### <a name="parameters---unpackprintersettings"></a><span data-ttu-id="7c5d2-578">パラメーター - unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-578">Parameters - unpackPrinterSettings</span></span>

<span data-ttu-id="7c5d2-579">設定</span><span class="sxs-lookup"><span data-stu-id="7c5d2-579">settings</span></span>  

### <a name="return-value---unpackprintersettings"></a><span data-ttu-id="7c5d2-580">戻り値 - unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-580">Return Value - unpackPrinterSettings</span></span>

## <a name="method-unpackprintjobsettings"></a><span data-ttu-id="7c5d2-581">メソッド unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-581">Method unpackPrintJobSettings</span></span>

```xpp
public boolean unpackPrintJobSettings(container settings)
```

### <a name="parameters---unpackprintjobsettings"></a><span data-ttu-id="7c5d2-582">パラメーター - unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-582">Parameters - unpackPrintJobSettings</span></span>

<span data-ttu-id="7c5d2-583">設定</span><span class="sxs-lookup"><span data-stu-id="7c5d2-583">settings</span></span>  

### <a name="return-value---unpackprintjobsettings"></a><span data-ttu-id="7c5d2-584">戻り値 - unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-584">Return Value - unpackPrintJobSettings</span></span>

## <a name="method-unpacksubtotalsettings"></a><span data-ttu-id="7c5d2-585">メソッド unpackSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-585">Method unpackSubtotalSettings</span></span>

```xpp
public boolean unpackSubtotalSettings(container settings)
```

### <a name="parameters---unpacksubtotalsettings"></a><span data-ttu-id="7c5d2-586">パラメーター - unpackSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-586">Parameters - unpackSubtotalSettings</span></span>

<span data-ttu-id="7c5d2-587">設定</span><span class="sxs-lookup"><span data-stu-id="7c5d2-587">settings</span></span>  

### <a name="return-value---unpacksubtotalsettings"></a><span data-ttu-id="7c5d2-588">戻り値 - unpackSubtotalSettings</span><span class="sxs-lookup"><span data-stu-id="7c5d2-588">Return Value - unpackSubtotalSettings</span></span>

## <a name="method-unprintablebottom"></a><span data-ttu-id="7c5d2-589">メソッド unprintableBottom</span><span class="sxs-lookup"><span data-stu-id="7c5d2-589">Method unprintableBottom</span></span>

```xpp
public int unprintableBottom()
```

### <a name="return-value---unprintablebottom"></a><span data-ttu-id="7c5d2-590">戻り値 - unprintableBottom</span><span class="sxs-lookup"><span data-stu-id="7c5d2-590">Return Value - unprintableBottom</span></span>

## <a name="method-unprintableleft"></a><span data-ttu-id="7c5d2-591">メソッド unprintableLeft</span><span class="sxs-lookup"><span data-stu-id="7c5d2-591">Method unprintableLeft</span></span>

```xpp
public int unprintableLeft()
```

### <a name="return-value---unprintableleft"></a><span data-ttu-id="7c5d2-592">戻り値 - unprintableLeft</span><span class="sxs-lookup"><span data-stu-id="7c5d2-592">Return Value - unprintableLeft</span></span>

## <a name="method-unprintableright"></a><span data-ttu-id="7c5d2-593">メソッド unprintableRight</span><span class="sxs-lookup"><span data-stu-id="7c5d2-593">Method unprintableRight</span></span>

```xpp
public int unprintableRight()
```

### <a name="return-value---unprintableright"></a><span data-ttu-id="7c5d2-594">戻り値 - unprintableRight</span><span class="sxs-lookup"><span data-stu-id="7c5d2-594">Return Value - unprintableRight</span></span>

## <a name="method-unprintabletop"></a><span data-ttu-id="7c5d2-595">メソッド unprintableTop</span><span class="sxs-lookup"><span data-stu-id="7c5d2-595">Method unprintableTop</span></span>

<span data-ttu-id="7c5d2-596">用紙の最上部から用紙の印刷可能な範囲までの距離を示します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-596">Indicates the distance from the top of the paper to the printable area of the paper.</span></span>

```xpp
public int unprintableTop()
```

### <a name="return-value---unprintabletop"></a><span data-ttu-id="7c5d2-597">戻り値 - unprintableTop</span><span class="sxs-lookup"><span data-stu-id="7c5d2-597">Return Value - unprintableTop</span></span>

<span data-ttu-id="7c5d2-598">印刷できない領域のサイズ。単位は 100 分の 1 ミリメートルです。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-598">The size of nonprintable area, measured in hundredths of a millimeter.</span></span>

### <a name="remarks---unprintabletop"></a><span data-ttu-id="7c5d2-599">備考 - unprintableTop</span><span class="sxs-lookup"><span data-stu-id="7c5d2-599">Remarks - unprintableTop</span></span>

<span data-ttu-id="7c5d2-600">レポートでは、reportDesign の topMargin を unprintableTop よりも小さくしてはなりません。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-600">In reports, the topMargin of a reportDesign must not be less than unprintableTop.</span></span>

### <a name="examples---unprintabletop"></a><span data-ttu-id="7c5d2-601">例 - unprintableTop</span><span class="sxs-lookup"><span data-stu-id="7c5d2-601">Examples - unprintableTop</span></span>

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

## <a name="method-viewertype"></a><span data-ttu-id="7c5d2-602">メソッド viewerType</span><span class="sxs-lookup"><span data-stu-id="7c5d2-602">Method viewerType</span></span>

```xpp
public ReportOutputUserType viewerType([ReportOutputUserType type])
```

### <a name="parameters---viewertype"></a><span data-ttu-id="7c5d2-603">パラメーター - viewerType</span><span class="sxs-lookup"><span data-stu-id="7c5d2-603">Parameters - viewerType</span></span>

<span data-ttu-id="7c5d2-604">タイプ</span><span class="sxs-lookup"><span data-stu-id="7c5d2-604">type</span></span>  

### <a name="return-value---viewertype"></a><span data-ttu-id="7c5d2-605">戻り値 - viewerType</span><span class="sxs-lookup"><span data-stu-id="7c5d2-605">Return Value - viewerType</span></span>

## <a name="method-virtualpageheight"></a><span data-ttu-id="7c5d2-606">メソッド virtualPageHeight</span><span class="sxs-lookup"><span data-stu-id="7c5d2-606">Method virtualPageHeight</span></span>

```xpp
public int virtualPageHeight([int height])
```

### <a name="parameters---virtualpageheight"></a><span data-ttu-id="7c5d2-607">パラメーター - virtualPageHeight</span><span class="sxs-lookup"><span data-stu-id="7c5d2-607">Parameters - virtualPageHeight</span></span>

<span data-ttu-id="7c5d2-608">height</span><span class="sxs-lookup"><span data-stu-id="7c5d2-608">height</span></span>  

### <a name="return-value---virtualpageheight"></a><span data-ttu-id="7c5d2-609">戻り値 - virtualPageHeight</span><span class="sxs-lookup"><span data-stu-id="7c5d2-609">Return Value - virtualPageHeight</span></span>

## <a name="method-warniffileexists"></a><span data-ttu-id="7c5d2-610">メソッド warnIfFileExists</span><span class="sxs-lookup"><span data-stu-id="7c5d2-610">Method warnIfFileExists</span></span>

```xpp
public boolean warnIfFileExists([boolean warn])
```

### <a name="parameters---warniffileexists"></a><span data-ttu-id="7c5d2-611">パラメーター - warnIfFileExists</span><span class="sxs-lookup"><span data-stu-id="7c5d2-611">Parameters - warnIfFileExists</span></span>

<span data-ttu-id="7c5d2-612">警告</span><span class="sxs-lookup"><span data-stu-id="7c5d2-612">warn</span></span>  

### <a name="return-value---warniffileexists"></a><span data-ttu-id="7c5d2-613">戻り値 - warnIfFileExists</span><span class="sxs-lookup"><span data-stu-id="7c5d2-613">Return Value - warnIfFileExists</span></span>

## <a name="method-enablebody"></a><span data-ttu-id="7c5d2-614">メソッド enableBody</span><span class="sxs-lookup"><span data-stu-id="7c5d2-614">Method enableBody</span></span>

```xpp
public void enableBody([TableId tableId])
```

### <a name="parameters---enablebody"></a><span data-ttu-id="7c5d2-615">パラメーター - enableBody</span><span class="sxs-lookup"><span data-stu-id="7c5d2-615">Parameters - enableBody</span></span>

<span data-ttu-id="7c5d2-616">tableId</span><span class="sxs-lookup"><span data-stu-id="7c5d2-616">tableId</span></span>  

## <a name="method-new"></a><span data-ttu-id="7c5d2-617">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7c5d2-617">Method new</span></span>

<span data-ttu-id="7c5d2-618">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-618">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([container Settings], [boolean infoOnly])
```

### <a name="parameters---new"></a><span data-ttu-id="7c5d2-619">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="7c5d2-619">Parameters - new</span></span>

<span data-ttu-id="7c5d2-620">設定</span><span class="sxs-lookup"><span data-stu-id="7c5d2-620">Settings</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-621">infoOnly</span><span class="sxs-lookup"><span data-stu-id="7c5d2-621">infoOnly</span></span>  

## <a name="method-addtraypagecopy"></a><span data-ttu-id="7c5d2-622">メソッド addTrayPageCopy</span><span class="sxs-lookup"><span data-stu-id="7c5d2-622">Method addTrayPageCopy</span></span>

```xpp
public void addTrayPageCopy(int tray, int pageNumber, [int copyNumber])
```

### <a name="parameters---addtraypagecopy"></a><span data-ttu-id="7c5d2-623">パラメーター - addTrayPageCopy</span><span class="sxs-lookup"><span data-stu-id="7c5d2-623">Parameters - addTrayPageCopy</span></span>

<span data-ttu-id="7c5d2-624">トレイ</span><span class="sxs-lookup"><span data-stu-id="7c5d2-624">tray</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-625">pageNumber</span><span class="sxs-lookup"><span data-stu-id="7c5d2-625">pageNumber</span></span>  

<!-- -->

<span data-ttu-id="7c5d2-626">copyNumber</span><span class="sxs-lookup"><span data-stu-id="7c5d2-626">copyNumber</span></span>  

## <a name="method-disablebody"></a><span data-ttu-id="7c5d2-627">メソッド disableBody</span><span class="sxs-lookup"><span data-stu-id="7c5d2-627">Method disableBody</span></span>

```xpp
public void disableBody([TableId tableId])
```

### <a name="parameters---disablebody"></a><span data-ttu-id="7c5d2-628">パラメーター - disableBody</span><span class="sxs-lookup"><span data-stu-id="7c5d2-628">Parameters - disableBody</span></span>

<span data-ttu-id="7c5d2-629">tableId</span><span class="sxs-lookup"><span data-stu-id="7c5d2-629">tableId</span></span>  

## <a name="method-cleartraypagecopy"></a><span data-ttu-id="7c5d2-630">メソッド clearTrayPageCopy</span><span class="sxs-lookup"><span data-stu-id="7c5d2-630">Method clearTrayPageCopy</span></span>

```xpp
public void clearTrayPageCopy()
```

## <a name="method-rulerinch"></a><span data-ttu-id="7c5d2-631">メソッド rulerInch</span><span class="sxs-lookup"><span data-stu-id="7c5d2-631">Method rulerInch</span></span>

```xpp
public void rulerInch()
```

## <a name="method-finalize"></a><span data-ttu-id="7c5d2-632">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="7c5d2-632">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-ruleroff"></a><span data-ttu-id="7c5d2-633">メソッド rulerOff</span><span class="sxs-lookup"><span data-stu-id="7c5d2-633">Method rulerOff</span></span>

```xpp
public void rulerOff()
```

## <a name="method-rulermetric"></a><span data-ttu-id="7c5d2-634">メソッド rulerMetric</span><span class="sxs-lookup"><span data-stu-id="7c5d2-634">Method rulerMetric</span></span>

```xpp
public void rulerMetric()
```

