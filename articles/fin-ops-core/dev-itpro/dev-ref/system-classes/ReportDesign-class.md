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
# <a name="class-reportdesign"></a><span data-ttu-id="241d0-103">クラス ReportDesign</span><span class="sxs-lookup"><span data-stu-id="241d0-103">Class ReportDesign</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportDesign extends TreeNode
```

<span data-ttu-id="241d0-104">ReportDesign クラスは、レポートの内容を決定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-104">The ReportDesign class determines the contents of a report.</span></span>

## <a name="remarks"></a><span data-ttu-id="241d0-105">備考</span><span class="sxs-lookup"><span data-stu-id="241d0-105">Remarks</span></span>

<span data-ttu-id="241d0-106">ReportDesign オブジェクトは、レポートの内容を決定する ReportSection オブジェクトまたは SectionTemplate オブジェクトの集合です。</span><span class="sxs-lookup"><span data-stu-id="241d0-106">A ReportDesign object is a collection of ReportSection objects or SectionTemplate objects that determines the contents of a report.</span></span> <span data-ttu-id="241d0-107">各レポートは、Designs ノードの下のアプリケーション オブジェクト ツリー (AOT) に ReportDesign ノードを保持しています。</span><span class="sxs-lookup"><span data-stu-id="241d0-107">Each report contains a ReportDesign node in the Application Object Tree (AOT), below the Designs node.</span></span> <span data-ttu-id="241d0-108">ReportDesign ノードには常に、AutoDesignSpecs という名前のノードが含まれ、生成されたデザインと呼ばれる Design という名前のノードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="241d0-108">The ReportDesign node always contains a node that is named AutoDesignSpecs, and it can contain a node that is named Design, which is referred to as the generated design.</span></span> <span data-ttu-id="241d0-109">ReportDesign ノードには、1 つ以上の SectionTemplate ノード (AutoDesignSpecs ノードの下) または生成されたデザインが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="241d0-109">A ReportDesign node should contain either one or more SectionTemplate nodes (below the AutoDesignSpecs node) or a generated design.</span></span> <span data-ttu-id="241d0-110">両方が含まれている場合、生成されたデザインのみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d0-110">If it contains both, only the generated design is used.</span></span> <span data-ttu-id="241d0-111">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="241d0-111">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="241d0-112">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="241d0-112">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="241d0-113">生成されたデザインがないレポートは、生成されたデザインがあるレポートよりもエンド ユーザーにさらに柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="241d0-113">A report that does not have a generated design offers more flexibility to the end user than a report that has a generated design.</span></span> <span data-ttu-id="241d0-114">たとえば、生成されたデザインがないレポートを実行するユーザーは、どの合計をレポートに含めるかをクエリで決定できます。</span><span class="sxs-lookup"><span data-stu-id="241d0-114">For example, a user who is running a report that does not have a generated design can decide in the query which sums to include in the report.</span></span> <span data-ttu-id="241d0-115">生成されたデザインはレポートの実行中に作成され、ユーザーの選択に対応するフッター セクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d0-115">A generated design is then created during the execution of the report, and it will contain footer sections that correspond to the user's choice.</span></span> <span data-ttu-id="241d0-116">レポートに生成されたデザインが含まれている場合、生成されたデザイン内にフッター セクションが存在するため、レポートにその合計が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="241d0-116">If a report has a generated design, the existence of footer sections in the generated design controls which sums are printed in the report.</span></span>

## <a name="examples"></a><span data-ttu-id="241d0-117">例</span><span class="sxs-lookup"><span data-stu-id="241d0-117">Examples</span></span>

<span data-ttu-id="241d0-118">次の例では、AOT には存在しない簡易レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="241d0-118">The following example creates a simple report that is not present in the AOT.</span></span>

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

## <a name="methods"></a><span data-ttu-id="241d0-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="241d0-119">Methods</span></span>

| <span data-ttu-id="241d0-120">方法</span><span class="sxs-lookup"><span data-stu-id="241d0-120">Method</span></span>                                                                                                 | <span data-ttu-id="241d0-121">説明</span><span class="sxs-lookup"><span data-stu-id="241d0-121">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d0-122">public ReportSection addProgrammableSection(int number)</span><span class="sxs-lookup"><span data-stu-id="241d0-122">public ReportSection addProgrammableSection(int number)</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-123">public ReportSection addSection(ReportBlockType sectionType, \[TableId tableId\], \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="241d0-123">public ReportSection addSection(ReportBlockType sectionType, \[TableId tableId\], \[FieldId fieldId\])</span></span> | <span data-ttu-id="241d0-124">デザインにレポート セクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="241d0-124">Adds a report section to a design.</span></span>                                                                                                        |
| <span data-ttu-id="241d0-125">public ReportSectionGroup addSectionGroup(TableId tableId, \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="241d0-125">public ReportSectionGroup addSectionGroup(TableId tableId, \[FieldId fieldId\])</span></span>                        | <span data-ttu-id="241d0-126">デザインにセクション グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="241d0-126">Adds a section group to a design.</span></span>                                                                                                         |
| <span data-ttu-id="241d0-127">public int arrange()</span><span class="sxs-lookup"><span data-stu-id="241d0-127">public int arrange()</span></span>                                                                                   |                                                                                                                                           |
| <span data-ttu-id="241d0-128">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-128">public int arrangeWhen(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-129">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-129">public boolean autoDeclaration(\[boolean value\])</span></span>                                                      | <span data-ttu-id="241d0-130">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-130">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="241d0-131">public ReportAutoDesignSpecs autoDesignSpecs()</span><span class="sxs-lookup"><span data-stu-id="241d0-131">public ReportAutoDesignSpecs autoDesignSpecs()</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-132">public ReportSection autoSection(TableId tableId, \[int number\])</span><span class="sxs-lookup"><span data-stu-id="241d0-132">public ReportSection autoSection(TableId tableId, \[int number\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="241d0-133">public int autoSectionControlCount()</span><span class="sxs-lookup"><span data-stu-id="241d0-133">public int autoSectionControlCount()</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="241d0-134">public ReportControl autoSectionControlNumber(int number)</span><span class="sxs-lookup"><span data-stu-id="241d0-134">public ReportControl autoSectionControlNumber(int number)</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="241d0-135">public int autoSectionCount()</span><span class="sxs-lookup"><span data-stu-id="241d0-135">public int autoSectionCount()</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-136">public ReportSection autoSectionNumber(int number)</span><span class="sxs-lookup"><span data-stu-id="241d0-136">public ReportSection autoSectionNumber(int number)</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="241d0-137">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-137">public int bold(\[int value\])</span></span>                                                                         | <span data-ttu-id="241d0-138">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-138">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="241d0-139">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-139">public int bottomMarginMode(\[int value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="241d0-140">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-140">public str bottomMarginStr(\[str value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="241d0-141">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-141">public Units bottomMarginUnit(\[Units value\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-142">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-142">public Real bottomMarginValue(\[Real value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-143">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-143">public str caption(\[str value\])</span></span>                                                                      | <span data-ttu-id="241d0-144">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-144">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="241d0-145">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-145">public int characterSet(\[int value\])</span></span>                                                                 | <span data-ttu-id="241d0-146">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-146">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="241d0-147">public boolean collate(\[boolean collate\])</span><span class="sxs-lookup"><span data-stu-id="241d0-147">public boolean collate(\[boolean collate\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-148">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-148">public int colorScheme(\[int value\])</span></span>                                                                  | <span data-ttu-id="241d0-149">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-149">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="241d0-150">public ReportControl control(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="241d0-150">public ReportControl control(TableId tableId, FieldId fieldId)</span></span>                                         | <span data-ttu-id="241d0-151">コントロールのテーブルおよび dataField プロパティに基づいて、生成されたデザインのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-151">Finds a control in the generated design, based on the control's table and dataField properties.</span></span>                                           |
| <span data-ttu-id="241d0-152">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="241d0-152">public int controlCount()</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="241d0-153">public ReportControl controlName(str name)</span><span class="sxs-lookup"><span data-stu-id="241d0-153">public ReportControl controlName(str name)</span></span>                                                             | <span data-ttu-id="241d0-154">コントロールの Name プロパティに基づいて、生成されたデザインのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-154">Finds a control in the generated design, based on the control's Name property.</span></span>                                                            |
| <span data-ttu-id="241d0-155">public ReportControl controlNumber(int number)</span><span class="sxs-lookup"><span data-stu-id="241d0-155">public ReportControl controlNumber(int number)</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-156">public int copies(\[int numberOfCopies\])</span><span class="sxs-lookup"><span data-stu-id="241d0-156">public int copies(\[int numberOfCopies\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="241d0-157">public int delete()</span><span class="sxs-lookup"><span data-stu-id="241d0-157">public int delete()</span></span>                                                                                    | <span data-ttu-id="241d0-158">ノードを AOT から削除します。</span><span class="sxs-lookup"><span data-stu-id="241d0-158">Deletes the node from the AOT.</span></span>                                                                                                            |
| <span data-ttu-id="241d0-159">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-159">public str description(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-160">public str deviceName(\[str device\])</span><span class="sxs-lookup"><span data-stu-id="241d0-160">public str deviceName(\[str device\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-161">public str driverName()</span><span class="sxs-lookup"><span data-stu-id="241d0-161">public str driverName()</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-162">public boolean edit()</span><span class="sxs-lookup"><span data-stu-id="241d0-162">public boolean edit()</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-163">public str emptyReportPrompt(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-163">public str emptyReportPrompt(\[str value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-164">public int fitToPage(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-164">public int fitToPage(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="241d0-165">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-165">public str font(\[str value\])</span></span>                                                                         | <span data-ttu-id="241d0-166">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-166">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="241d0-167">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-167">public int fontSize(\[int value\])</span></span>                                                                     | <span data-ttu-id="241d0-168">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-168">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="241d0-169">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-169">public int foregroundColor(\[int value\])</span></span>                                                              | <span data-ttu-id="241d0-170">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-170">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="241d0-171">public int from(\[int fromPage\])</span><span class="sxs-lookup"><span data-stu-id="241d0-171">public int from(\[int fromPage\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="241d0-172">public int generateDesign()</span><span class="sxs-lookup"><span data-stu-id="241d0-172">public int generateDesign()</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-173">public int getNumberOfPrinters()</span><span class="sxs-lookup"><span data-stu-id="241d0-173">public int getNumberOfPrinters()</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="241d0-174">public str getPrinter(int number)</span><span class="sxs-lookup"><span data-stu-id="241d0-174">public str getPrinter(int number)</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="241d0-175">public PrintMedium getTarget()</span><span class="sxs-lookup"><span data-stu-id="241d0-175">public PrintMedium getTarget()</span></span>                                                                         | <span data-ttu-id="241d0-176">レポートの印刷メディア ターゲットを返します。</span><span class="sxs-lookup"><span data-stu-id="241d0-176">Returns the print medium target for the report.</span></span>                                                                                           |
| <span data-ttu-id="241d0-177">public boolean hideBorder(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-177">public boolean hideBorder(\[boolean value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-178">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-178">public boolean italic(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="241d0-179">public str jobType(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-179">public str jobType(\[str value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="241d0-180">public int language(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-180">public int language(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="241d0-181">public str languageID(\[str lan\])</span><span class="sxs-lookup"><span data-stu-id="241d0-181">public str languageID(\[str lan\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="241d0-182">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-182">public int leftMarginMode(\[int value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="241d0-183">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-183">public str leftMarginStr(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-184">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-184">public Units leftMarginUnit(\[Units value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-185">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-185">public Real leftMarginValue(\[Real value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-186">public container loadDiskSettings()</span><span class="sxs-lookup"><span data-stu-id="241d0-186">public container loadDiskSettings()</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="241d0-187">public str localWebMenu(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-187">public str localWebMenu(\[str value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="241d0-188">public str lookupCaption(\[str lan\])</span><span class="sxs-lookup"><span data-stu-id="241d0-188">public str lookupCaption(\[str lan\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-189">public str lookupLabel(str label, \[str lan\])</span><span class="sxs-lookup"><span data-stu-id="241d0-189">public str lookupLabel(str label, \[str lan\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-190">public int makeAutoSection(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="241d0-190">public int makeAutoSection(\[Query query\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-191">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-191">public str name(\[str value\])</span></span>                                                                         | <span data-ttu-id="241d0-192">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-192">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="241d0-193">public int orientation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-193">public int orientation(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-194">public container pack()</span><span class="sxs-lookup"><span data-stu-id="241d0-194">public container pack()</span></span>                                                                                | <span data-ttu-id="241d0-195">ReportDesign クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="241d0-195">Serializes the current instance of the ReportDesign class.</span></span>                                                                                |
| <span data-ttu-id="241d0-196">public container packPageSettings()</span><span class="sxs-lookup"><span data-stu-id="241d0-196">public container packPageSettings()</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="241d0-197">public container packPrinterSettings()</span><span class="sxs-lookup"><span data-stu-id="241d0-197">public container packPrinterSettings()</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="241d0-198">public container packPrintJobSettings()</span><span class="sxs-lookup"><span data-stu-id="241d0-198">public container packPrintJobSettings()</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-199">public boolean pageFormatting()</span><span class="sxs-lookup"><span data-stu-id="241d0-199">public boolean pageFormatting()</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="241d0-200">public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])</span><span class="sxs-lookup"><span data-stu-id="241d0-200">public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="241d0-201">public int paperTray(\[int tray\])</span><span class="sxs-lookup"><span data-stu-id="241d0-201">public int paperTray(\[int tray\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="241d0-202">public int printerAttributes()</span><span class="sxs-lookup"><span data-stu-id="241d0-202">public int printerAttributes()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-203">public int printerAveragePPM()</span><span class="sxs-lookup"><span data-stu-id="241d0-203">public int printerAveragePPM()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-204">public str printerComment()</span><span class="sxs-lookup"><span data-stu-id="241d0-204">public str printerComment()</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-205">public str printerDatatype()</span><span class="sxs-lookup"><span data-stu-id="241d0-205">public str printerDatatype()</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-206">public int printerDefaultPriority()</span><span class="sxs-lookup"><span data-stu-id="241d0-206">public int printerDefaultPriority()</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="241d0-207">public str printerDriverName()</span><span class="sxs-lookup"><span data-stu-id="241d0-207">public str printerDriverName()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-208">public str printerLocation()</span><span class="sxs-lookup"><span data-stu-id="241d0-208">public str printerLocation()</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-209">public int printerPageHeight()</span><span class="sxs-lookup"><span data-stu-id="241d0-209">public int printerPageHeight()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-210">public int printerPageWidth()</span><span class="sxs-lookup"><span data-stu-id="241d0-210">public int printerPageWidth()</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-211">public int printerPaper()</span><span class="sxs-lookup"><span data-stu-id="241d0-211">public int printerPaper()</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="241d0-212">public str printerParameters()</span><span class="sxs-lookup"><span data-stu-id="241d0-212">public str printerParameters()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-213">public str printerPortName()</span><span class="sxs-lookup"><span data-stu-id="241d0-213">public str printerPortName()</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-214">public str printerPrinterName()</span><span class="sxs-lookup"><span data-stu-id="241d0-214">public str printerPrinterName()</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="241d0-215">public str printerPrintProcessor()</span><span class="sxs-lookup"><span data-stu-id="241d0-215">public str printerPrintProcessor()</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="241d0-216">public int printerPriority()</span><span class="sxs-lookup"><span data-stu-id="241d0-216">public int printerPriority()</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-217">public int printerQueuedJobs()</span><span class="sxs-lookup"><span data-stu-id="241d0-217">public int printerQueuedJobs()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-218">public str printerSepFile()</span><span class="sxs-lookup"><span data-stu-id="241d0-218">public str printerSepFile()</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-219">public str printerServerName()</span><span class="sxs-lookup"><span data-stu-id="241d0-219">public str printerServerName()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-220">public boolean printerSettings(\[ReportRun reportRun\], \[int showWhat\])</span><span class="sxs-lookup"><span data-stu-id="241d0-220">public boolean printerSettings(\[ReportRun reportRun\], \[int showWhat\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="241d0-221">public str printerShareName()</span><span class="sxs-lookup"><span data-stu-id="241d0-221">public str printerShareName()</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-222">public int printerStartTime()</span><span class="sxs-lookup"><span data-stu-id="241d0-222">public int printerStartTime()</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-223">public int printerStatus()</span><span class="sxs-lookup"><span data-stu-id="241d0-223">public int printerStatus()</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="241d0-224">public int printerUntilTime()</span><span class="sxs-lookup"><span data-stu-id="241d0-224">public int printerUntilTime()</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-225">public str printFormName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-225">public str printFormName(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-226">public PrintJobSettings printJobSettings()</span><span class="sxs-lookup"><span data-stu-id="241d0-226">public PrintJobSettings printJobSettings()</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="241d0-227">public boolean removeRedundantFooters(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-227">public boolean removeRedundantFooters(\[boolean value\])</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="241d0-228">public boolean removeRepeatedFooters(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-228">public boolean removeRepeatedFooters(\[boolean value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-229">public boolean removeRepeatedHeaders(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-229">public boolean removeRepeatedHeaders(\[boolean value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-230">public str reportTemplate(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-230">public str reportTemplate(\[str value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="241d0-231">public str resolutionX(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-231">public str resolutionX(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-232">public int resolutionXStr(str value)</span><span class="sxs-lookup"><span data-stu-id="241d0-232">public int resolutionXStr(str value)</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="241d0-233">public Units resolutionXUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-233">public Units resolutionXUnit(\[Units value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-234">public str resolutionY(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-234">public str resolutionY(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="241d0-235">public int resolutionYStr(str value)</span><span class="sxs-lookup"><span data-stu-id="241d0-235">public int resolutionYStr(str value)</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="241d0-236">public Units resolutionYUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-236">public Units resolutionYUnit(\[Units value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-237">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-237">public int rightMarginMode(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="241d0-238">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-238">public str rightMarginStr(\[str value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="241d0-239">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-239">public Units rightMarginUnit(\[Units value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-240">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-240">public Real rightMarginValue(\[Real value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-241">public int ruler(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-241">public int ruler(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="241d0-242">public boolean saveDiskSettings(container buffer)</span><span class="sxs-lookup"><span data-stu-id="241d0-242">public boolean saveDiskSettings(container buffer)</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="241d0-243">public ReportSection section(int number)</span><span class="sxs-lookup"><span data-stu-id="241d0-243">public ReportSection section(int number)</span></span>                                                               | <span data-ttu-id="241d0-244">生成されたデザイン ノードの下のセクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-244">Finds a section below the generated design node.</span></span>                                                                                          |
| <span data-ttu-id="241d0-245">public int sectionCount()</span><span class="sxs-lookup"><span data-stu-id="241d0-245">public int sectionCount()</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="241d0-246">public ReportSectionGroup sectionGroup(TableId tableId, \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="241d0-246">public ReportSectionGroup sectionGroup(TableId tableId, \[FieldId fieldId\])</span></span>                           | <span data-ttu-id="241d0-247">reportDesign オブジェクトの下の reportSectionGroup オブジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-247">Finds a reportSectionGroup object below a reportDesign object.</span></span>                                                                            |
| <span data-ttu-id="241d0-248">public ReportSection sectionName(str name)</span><span class="sxs-lookup"><span data-stu-id="241d0-248">public ReportSection sectionName(str name)</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="241d0-249">public ReportSection sectionNumber(int number)</span><span class="sxs-lookup"><span data-stu-id="241d0-249">public ReportSection sectionNumber(int number)</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-250">public PrintMedium setTarget(PrintMedium target)</span><span class="sxs-lookup"><span data-stu-id="241d0-250">public PrintMedium setTarget(PrintMedium target)</span></span>                                                       | <span data-ttu-id="241d0-251">レポートの印刷メディア ターゲットを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-251">Sets the print medium target for the report.</span></span>                                                                                              |
| <span data-ttu-id="241d0-252">public int to(\[int toPage\])</span><span class="sxs-lookup"><span data-stu-id="241d0-252">public int to(\[int toPage\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-253">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-253">public int topMarginMode(\[int value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="241d0-254">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-254">public str topMarginStr(\[str value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="241d0-255">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-255">public Units topMarginUnit(\[Units value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-256">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-256">public Real topMarginValue(\[Real value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="241d0-257">public str toString()</span><span class="sxs-lookup"><span data-stu-id="241d0-257">public str toString()</span></span>                                                                                  | <span data-ttu-id="241d0-258">クラス ハンドルと名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="241d0-258">Returns a string that contains the class handle and name.</span></span>                                                                                 |
| <span data-ttu-id="241d0-259">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d0-259">public boolean underline(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="241d0-260">public boolean unpackPageSettings(container packedPageSetup)</span><span class="sxs-lookup"><span data-stu-id="241d0-260">public boolean unpackPageSettings(container packedPageSetup)</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="241d0-261">public boolean unpackPrinterSettings(container packedPrintSetup)</span><span class="sxs-lookup"><span data-stu-id="241d0-261">public boolean unpackPrinterSettings(container packedPrintSetup)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="241d0-262">public boolean unpackPrintJobSettings(container packedPrintJobSettings)</span><span class="sxs-lookup"><span data-stu-id="241d0-262">public boolean unpackPrintJobSettings(container packedPrintJobSettings)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="241d0-263">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="241d0-263">public void leftMargin(Real value, Units unit)</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="241d0-264">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="241d0-264">public void bottomMargin(Real value, Units unit)</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="241d0-265">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="241d0-265">public void rightMargin(Real value, Units unit)</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="241d0-266">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="241d0-266">public void topMargin(Real value, Units unit)</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="241d0-267">public void deleteDiskSettings(\[boolean allUsers\])</span><span class="sxs-lookup"><span data-stu-id="241d0-267">public void deleteDiskSettings(\[boolean allUsers\])</span></span>                                                   |                                                                                                                                           |

## <a name="method-addprogrammablesection"></a><span data-ttu-id="241d0-268">メソッド addProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="241d0-268">Method addProgrammableSection</span></span>

```xpp
public ReportSection addProgrammableSection(int number)
```

### <a name="parameters---addprogrammablesection"></a><span data-ttu-id="241d0-269">パラメーター - addProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="241d0-269">Parameters - addProgrammableSection</span></span>

<span data-ttu-id="241d0-270">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-270">number</span></span>  

### <a name="return-value---addprogrammablesection"></a><span data-ttu-id="241d0-271">戻り値 - addProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="241d0-271">Return Value - addProgrammableSection</span></span>

## <a name="method-addsection"></a><span data-ttu-id="241d0-272">メソッド addSection</span><span class="sxs-lookup"><span data-stu-id="241d0-272">Method addSection</span></span>

<span data-ttu-id="241d0-273">デザインにレポート セクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="241d0-273">Adds a report section to a design.</span></span>

```xpp
public ReportSection addSection(ReportBlockType sectionType, [TableId tableId], [FieldId fieldId])
```

### <a name="parameters---addsection"></a><span data-ttu-id="241d0-274">パラメーター - addSection</span><span class="sxs-lookup"><span data-stu-id="241d0-274">Parameters - addSection</span></span>

<span data-ttu-id="241d0-275">sectionType</span><span class="sxs-lookup"><span data-stu-id="241d0-275">sectionType</span></span>  
<span data-ttu-id="241d0-276">sectionType パラメーターがヘッダー、本文、またはフッターに設定されている場合、セクションが属するセクション グループの dataField プロパティはオプションになります。</span><span class="sxs-lookup"><span data-stu-id="241d0-276">If the sectionType parameter is set to Header, Body, or Footer, the dataField property of the section group that the section belongs to; optional.</span></span>

<!-- -->

<span data-ttu-id="241d0-277">tableId</span><span class="sxs-lookup"><span data-stu-id="241d0-277">tableId</span></span>  
<span data-ttu-id="241d0-278">sectionType パラメーターがヘッダー、本文、またはフッターに設定されている場合、セクションが属するセクション グループの dataField プロパティはオプションになります。</span><span class="sxs-lookup"><span data-stu-id="241d0-278">If the sectionType parameter is set to Header, Body, or Footer, the dataField property of the section group that the section belongs to; optional.</span></span>

<!-- -->

<span data-ttu-id="241d0-279">fieldId</span><span class="sxs-lookup"><span data-stu-id="241d0-279">fieldId</span></span>  
<span data-ttu-id="241d0-280">sectionType パラメーターがヘッダー、本文、またはフッターに設定されている場合、セクションが属するセクション グループの dataField プロパティはオプションになります。</span><span class="sxs-lookup"><span data-stu-id="241d0-280">If the sectionType parameter is set to Header, Body, or Footer, the dataField property of the section group that the section belongs to; optional.</span></span>

### <a name="return-value---addsection"></a><span data-ttu-id="241d0-281">戻り値 - addSection</span><span class="sxs-lookup"><span data-stu-id="241d0-281">Return Value - addSection</span></span>

<span data-ttu-id="241d0-282">作成されたセクション。</span><span class="sxs-lookup"><span data-stu-id="241d0-282">The section that is created.</span></span>

### <a name="remarks---addsection"></a><span data-ttu-id="241d0-283">備考 - addSection</span><span class="sxs-lookup"><span data-stu-id="241d0-283">Remarks - addSection</span></span>

<span data-ttu-id="241d0-284">このメソッドは、生成されたデザインを作成します (存在しない場合)。</span><span class="sxs-lookup"><span data-stu-id="241d0-284">This method creates a generated design if it does not already exist.</span></span> <span data-ttu-id="241d0-285">SectionType パラメーターが、ヘッダー、本文またはフッターに設定されている場合、セクション グループが存在しないと、メソッドはセクション グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="241d0-285">If the sectionType parameter is set to Header, Body, or Footer, this method creates a section group if it does not already exist.</span></span>

## <a name="method-addsectiongroup"></a><span data-ttu-id="241d0-286">メソッド addSectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-286">Method addSectionGroup</span></span>

<span data-ttu-id="241d0-287">デザインにセクション グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="241d0-287">Adds a section group to a design.</span></span>

```xpp
public ReportSectionGroup addSectionGroup(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---addsectiongroup"></a><span data-ttu-id="241d0-288">パラメーター - addSectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-288">Parameters - addSectionGroup</span></span>

<span data-ttu-id="241d0-289">tableId</span><span class="sxs-lookup"><span data-stu-id="241d0-289">tableId</span></span>  
<span data-ttu-id="241d0-290">セクション グループのデータ フィールドのプロパティ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d0-290">The dataField property of the section group; optional.</span></span>

<!-- -->

<span data-ttu-id="241d0-291">fieldId</span><span class="sxs-lookup"><span data-stu-id="241d0-291">fieldId</span></span>  
<span data-ttu-id="241d0-292">セクション グループのデータ フィールドのプロパティ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d0-292">The dataField property of the section group; optional.</span></span>

### <a name="return-value---addsectiongroup"></a><span data-ttu-id="241d0-293">戻り値 - addSectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-293">Return Value - addSectionGroup</span></span>

<span data-ttu-id="241d0-294">作成されたセクション グループ。</span><span class="sxs-lookup"><span data-stu-id="241d0-294">The section group that is created.</span></span>

### <a name="remarks---addsectiongroup"></a><span data-ttu-id="241d0-295">備考 - addSectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-295">Remarks - addSectionGroup</span></span>

<span data-ttu-id="241d0-296">このメソッドは、生成されたデザインを作成します (存在しない場合)。</span><span class="sxs-lookup"><span data-stu-id="241d0-296">This method creates a generated design (if it does not already exist).</span></span>

## <a name="method-arrange"></a><span data-ttu-id="241d0-297">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="241d0-297">Method arrange</span></span>

```xpp
public int arrange()
```

### <a name="return-value---arrange"></a><span data-ttu-id="241d0-298">戻り値 - arrange</span><span class="sxs-lookup"><span data-stu-id="241d0-298">Return Value - arrange</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="241d0-299">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="241d0-299">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="241d0-300">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="241d0-300">Parameters - arrangeWhen</span></span>

<span data-ttu-id="241d0-301">値</span><span class="sxs-lookup"><span data-stu-id="241d0-301">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="241d0-302">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="241d0-302">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="241d0-303">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d0-303">Method autoDeclaration</span></span>

<span data-ttu-id="241d0-304">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-304">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="241d0-305">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d0-305">Parameters - autoDeclaration</span></span>

<span data-ttu-id="241d0-306">値</span><span class="sxs-lookup"><span data-stu-id="241d0-306">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="241d0-307">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d0-307">Return Value - autoDeclaration</span></span>

<span data-ttu-id="241d0-308">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d0-308">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="241d0-309">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d0-309">Remarks - autoDeclaration</span></span>

<span data-ttu-id="241d0-310">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="241d0-310">Controls cannot have identical names.</span></span>

## <a name="method-autodesignspecs"></a><span data-ttu-id="241d0-311">メソッド autoDesignSpecs</span><span class="sxs-lookup"><span data-stu-id="241d0-311">Method autoDesignSpecs</span></span>

```xpp
public ReportAutoDesignSpecs autoDesignSpecs()
```

### <a name="return-value---autodesignspecs"></a><span data-ttu-id="241d0-312">戻り値 - autoDesignSpecs</span><span class="sxs-lookup"><span data-stu-id="241d0-312">Return Value - autoDesignSpecs</span></span>

## <a name="method-autosection"></a><span data-ttu-id="241d0-313">メソッド autoSection</span><span class="sxs-lookup"><span data-stu-id="241d0-313">Method autoSection</span></span>

```xpp
public ReportSection autoSection(TableId tableId, [int number])
```

### <a name="parameters---autosection"></a><span data-ttu-id="241d0-314">パラメーター - autoSection</span><span class="sxs-lookup"><span data-stu-id="241d0-314">Parameters - autoSection</span></span>

<span data-ttu-id="241d0-315">tableId</span><span class="sxs-lookup"><span data-stu-id="241d0-315">tableId</span></span>  

<!-- -->

<span data-ttu-id="241d0-316">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-316">number</span></span>  

### <a name="return-value---autosection"></a><span data-ttu-id="241d0-317">戻り値 - autoSection</span><span class="sxs-lookup"><span data-stu-id="241d0-317">Return Value - autoSection</span></span>

## <a name="method-autosectioncontrolcount"></a><span data-ttu-id="241d0-318">メソッド autoSectionControlCount</span><span class="sxs-lookup"><span data-stu-id="241d0-318">Method autoSectionControlCount</span></span>

```xpp
public int autoSectionControlCount()
```

### <a name="return-value---autosectioncontrolcount"></a><span data-ttu-id="241d0-319">戻り値 - autoSectionControlCount</span><span class="sxs-lookup"><span data-stu-id="241d0-319">Return Value - autoSectionControlCount</span></span>

## <a name="method-autosectioncontrolnumber"></a><span data-ttu-id="241d0-320">メソッド autoSectionControlNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-320">Method autoSectionControlNumber</span></span>

```xpp
public ReportControl autoSectionControlNumber(int number)
```

### <a name="parameters---autosectioncontrolnumber"></a><span data-ttu-id="241d0-321">パラメーター - autoSectionControlNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-321">Parameters - autoSectionControlNumber</span></span>

<span data-ttu-id="241d0-322">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-322">number</span></span>  

### <a name="return-value---autosectioncontrolnumber"></a><span data-ttu-id="241d0-323">戻り値 - autoSectionControlNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-323">Return Value - autoSectionControlNumber</span></span>

## <a name="method-autosectioncount"></a><span data-ttu-id="241d0-324">メソッド autoSectionCount</span><span class="sxs-lookup"><span data-stu-id="241d0-324">Method autoSectionCount</span></span>

```xpp
public int autoSectionCount()
```

### <a name="return-value---autosectioncount"></a><span data-ttu-id="241d0-325">戻り値 - autoSectionCount</span><span class="sxs-lookup"><span data-stu-id="241d0-325">Return Value - autoSectionCount</span></span>

## <a name="method-autosectionnumber"></a><span data-ttu-id="241d0-326">メソッド autoSectionNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-326">Method autoSectionNumber</span></span>

```xpp
public ReportSection autoSectionNumber(int number)
```

### <a name="parameters---autosectionnumber"></a><span data-ttu-id="241d0-327">パラメーター - autoSectionNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-327">Parameters - autoSectionNumber</span></span>

<span data-ttu-id="241d0-328">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-328">number</span></span>  

### <a name="return-value---autosectionnumber"></a><span data-ttu-id="241d0-329">戻り値 - autoSectionNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-329">Return Value - autoSectionNumber</span></span>

## <a name="method-bold"></a><span data-ttu-id="241d0-330">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="241d0-330">Method bold</span></span>

<span data-ttu-id="241d0-331">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-331">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="241d0-332">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="241d0-332">Parameters - bold</span></span>

<span data-ttu-id="241d0-333">値</span><span class="sxs-lookup"><span data-stu-id="241d0-333">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="241d0-334">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="241d0-334">Return Value - bold</span></span>

<span data-ttu-id="241d0-335">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="241d0-335">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="241d0-336">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="241d0-336">Remarks - bold</span></span>

<span data-ttu-id="241d0-337">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d0-337">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="241d0-338">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="241d0-338">0 Use the default font weight.</span></span>
-   <span data-ttu-id="241d0-339">1 シン。</span><span class="sxs-lookup"><span data-stu-id="241d0-339">1 Thin.</span></span>
-   <span data-ttu-id="241d0-340">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="241d0-340">2 Extra-light.</span></span>
-   <span data-ttu-id="241d0-341">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="241d0-341">3 Light.</span></span>
-   <span data-ttu-id="241d0-342">4 標準。</span><span class="sxs-lookup"><span data-stu-id="241d0-342">4 Normal.</span></span>
-   <span data-ttu-id="241d0-343">5 中。</span><span class="sxs-lookup"><span data-stu-id="241d0-343">5 Medium.</span></span>
-   <span data-ttu-id="241d0-344">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="241d0-344">6 Semibold.</span></span>
-   <span data-ttu-id="241d0-345">7 太字。</span><span class="sxs-lookup"><span data-stu-id="241d0-345">7 Bold.</span></span>
-   <span data-ttu-id="241d0-346">8 極太。</span><span class="sxs-lookup"><span data-stu-id="241d0-346">8 Extra-bold.</span></span>
-   <span data-ttu-id="241d0-347">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="241d0-347">9 Heavy.</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="241d0-348">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-348">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="241d0-349">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-349">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="241d0-350">値</span><span class="sxs-lookup"><span data-stu-id="241d0-350">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="241d0-351">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-351">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="241d0-352">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-352">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="241d0-353">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-353">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="241d0-354">値</span><span class="sxs-lookup"><span data-stu-id="241d0-354">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="241d0-355">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-355">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="241d0-356">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-356">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="241d0-357">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-357">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="241d0-358">値</span><span class="sxs-lookup"><span data-stu-id="241d0-358">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="241d0-359">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-359">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="241d0-360">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-360">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="241d0-361">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-361">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="241d0-362">値</span><span class="sxs-lookup"><span data-stu-id="241d0-362">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="241d0-363">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-363">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="241d0-364">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="241d0-364">Method caption</span></span>

<span data-ttu-id="241d0-365">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-365">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="241d0-366">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="241d0-366">Parameters - caption</span></span>

<span data-ttu-id="241d0-367">値</span><span class="sxs-lookup"><span data-stu-id="241d0-367">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="241d0-368">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="241d0-368">Return Value - caption</span></span>

<span data-ttu-id="241d0-369">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="241d0-369">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="241d0-370">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="241d0-370">Method characterSet</span></span>

<span data-ttu-id="241d0-371">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-371">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="241d0-372">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="241d0-372">Parameters - characterSet</span></span>

<span data-ttu-id="241d0-373">値</span><span class="sxs-lookup"><span data-stu-id="241d0-373">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="241d0-374">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="241d0-374">Return Value - characterSet</span></span>

<span data-ttu-id="241d0-375">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d0-375">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="241d0-376">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="241d0-376">Remarks - characterSet</span></span>

<span data-ttu-id="241d0-377">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="241d0-377">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="241d0-378">値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-378">Value.</span></span> | <span data-ttu-id="241d0-379">説明。</span><span class="sxs-lookup"><span data-stu-id="241d0-379">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="241d0-380">0</span><span class="sxs-lookup"><span data-stu-id="241d0-380">0</span></span>      | <span data-ttu-id="241d0-381">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-381">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="241d0-382">1</span><span class="sxs-lookup"><span data-stu-id="241d0-382">1</span></span>      | <span data-ttu-id="241d0-383">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-383">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="241d0-384">2</span><span class="sxs-lookup"><span data-stu-id="241d0-384">2</span></span>      | <span data-ttu-id="241d0-385">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-385">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="241d0-386">77</span><span class="sxs-lookup"><span data-stu-id="241d0-386">77</span></span>     | <span data-ttu-id="241d0-387">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-387">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="241d0-388">128</span><span class="sxs-lookup"><span data-stu-id="241d0-388">128</span></span>    | <span data-ttu-id="241d0-389">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-389">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="241d0-390">129</span><span class="sxs-lookup"><span data-stu-id="241d0-390">129</span></span>    | <span data-ttu-id="241d0-391">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-391">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="241d0-392">134</span><span class="sxs-lookup"><span data-stu-id="241d0-392">134</span></span>    | <span data-ttu-id="241d0-393">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-393">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="241d0-394">136</span><span class="sxs-lookup"><span data-stu-id="241d0-394">136</span></span>    | <span data-ttu-id="241d0-395">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-395">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="241d0-396">161</span><span class="sxs-lookup"><span data-stu-id="241d0-396">161</span></span>    | <span data-ttu-id="241d0-397">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-397">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="241d0-398">162</span><span class="sxs-lookup"><span data-stu-id="241d0-398">162</span></span>    | <span data-ttu-id="241d0-399">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-399">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="241d0-400">163</span><span class="sxs-lookup"><span data-stu-id="241d0-400">163</span></span>    | <span data-ttu-id="241d0-401">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-401">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="241d0-402">186</span><span class="sxs-lookup"><span data-stu-id="241d0-402">186</span></span>    | <span data-ttu-id="241d0-403">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-403">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="241d0-404">204</span><span class="sxs-lookup"><span data-stu-id="241d0-404">204</span></span>    | <span data-ttu-id="241d0-405">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-405">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="241d0-406">238</span><span class="sxs-lookup"><span data-stu-id="241d0-406">238</span></span>    | <span data-ttu-id="241d0-407">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-407">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="241d0-408">255</span><span class="sxs-lookup"><span data-stu-id="241d0-408">255</span></span>    | <span data-ttu-id="241d0-409">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-409">OEM\_CHARSET</span></span>         |

<span data-ttu-id="241d0-410">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-410">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="241d0-411">値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-411">Value.</span></span> | <span data-ttu-id="241d0-412">説明。</span><span class="sxs-lookup"><span data-stu-id="241d0-412">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="241d0-413">130</span><span class="sxs-lookup"><span data-stu-id="241d0-413">130</span></span>    | <span data-ttu-id="241d0-414">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-414">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="241d0-415">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-415">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="241d0-416">値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-416">Value.</span></span> | <span data-ttu-id="241d0-417">説明。</span><span class="sxs-lookup"><span data-stu-id="241d0-417">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="241d0-418">177</span><span class="sxs-lookup"><span data-stu-id="241d0-418">177</span></span>    | <span data-ttu-id="241d0-419">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-419">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="241d0-420">178</span><span class="sxs-lookup"><span data-stu-id="241d0-420">178</span></span>    | <span data-ttu-id="241d0-421">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-421">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="241d0-422">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-422">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="241d0-423">値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-423">Value.</span></span> | <span data-ttu-id="241d0-424">説明。</span><span class="sxs-lookup"><span data-stu-id="241d0-424">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="241d0-425">222</span><span class="sxs-lookup"><span data-stu-id="241d0-425">222</span></span>    | <span data-ttu-id="241d0-426">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d0-426">THAI\_CHARSET</span></span> |

<span data-ttu-id="241d0-427">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="241d0-427">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="241d0-428">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="241d0-428">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="241d0-429">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="241d0-429">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-collate"></a><span data-ttu-id="241d0-430">メソッド collate</span><span class="sxs-lookup"><span data-stu-id="241d0-430">Method collate</span></span>

```xpp
public boolean collate([boolean collate])
```

### <a name="parameters---collate"></a><span data-ttu-id="241d0-431">パラメーター - collate</span><span class="sxs-lookup"><span data-stu-id="241d0-431">Parameters - collate</span></span>

<span data-ttu-id="241d0-432">collate</span><span class="sxs-lookup"><span data-stu-id="241d0-432">collate</span></span>  

### <a name="return-value---collate"></a><span data-ttu-id="241d0-433">戻り値 - collate</span><span class="sxs-lookup"><span data-stu-id="241d0-433">Return Value - collate</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="241d0-434">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d0-434">Method colorScheme</span></span>

<span data-ttu-id="241d0-435">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-435">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="241d0-436">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d0-436">Parameters - colorScheme</span></span>

<span data-ttu-id="241d0-437">値</span><span class="sxs-lookup"><span data-stu-id="241d0-437">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="241d0-438">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d0-438">Return Value - colorScheme</span></span>

<span data-ttu-id="241d0-439">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="241d0-439">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="241d0-440">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d0-440">Remarks - colorScheme</span></span>

<span data-ttu-id="241d0-441">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="241d0-441">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="241d0-442">値です。</span><span class="sxs-lookup"><span data-stu-id="241d0-442">Value.</span></span> | <span data-ttu-id="241d0-443">スタイル。</span><span class="sxs-lookup"><span data-stu-id="241d0-443">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="241d0-444">0</span><span class="sxs-lookup"><span data-stu-id="241d0-444">0</span></span>      | <span data-ttu-id="241d0-445">既定。</span><span class="sxs-lookup"><span data-stu-id="241d0-445">Default.</span></span>               |
| <span data-ttu-id="241d0-446">1</span><span class="sxs-lookup"><span data-stu-id="241d0-446">1</span></span>      | <span data-ttu-id="241d0-447">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="241d0-447">The Windows palette.</span></span>   |
| <span data-ttu-id="241d0-448">2</span><span class="sxs-lookup"><span data-stu-id="241d0-448">2</span></span>      | <span data-ttu-id="241d0-449">真の配色。</span><span class="sxs-lookup"><span data-stu-id="241d0-449">The true-color scheme.</span></span> |

## <a name="method-control"></a><span data-ttu-id="241d0-450">メソッド control</span><span class="sxs-lookup"><span data-stu-id="241d0-450">Method control</span></span>

<span data-ttu-id="241d0-451">コントロールのテーブルおよび dataField プロパティに基づいて、生成されたデザインのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-451">Finds a control in the generated design, based on the control's table and dataField properties.</span></span>

```xpp
public ReportControl control(TableId tableId, FieldId fieldId)
```

### <a name="parameters---control"></a><span data-ttu-id="241d0-452">パラメーター - control</span><span class="sxs-lookup"><span data-stu-id="241d0-452">Parameters - control</span></span>

<span data-ttu-id="241d0-453">tableId</span><span class="sxs-lookup"><span data-stu-id="241d0-453">tableId</span></span>  
<span data-ttu-id="241d0-454">コントロールのデータ フィールドのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="241d0-454">The dataField property of the control.</span></span>

<!-- -->

<span data-ttu-id="241d0-455">fieldId</span><span class="sxs-lookup"><span data-stu-id="241d0-455">fieldId</span></span>  
<span data-ttu-id="241d0-456">コントロールのデータ フィールドのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="241d0-456">The dataField property of the control.</span></span>

### <a name="return-value---control"></a><span data-ttu-id="241d0-457">戻り値 - control</span><span class="sxs-lookup"><span data-stu-id="241d0-457">Return Value - control</span></span>

<span data-ttu-id="241d0-458">見つかったコントロール。</span><span class="sxs-lookup"><span data-stu-id="241d0-458">The control that is found.</span></span>

### <a name="examples---control"></a><span data-ttu-id="241d0-459">例 - control</span><span class="sxs-lookup"><span data-stu-id="241d0-459">Examples - control</span></span>

```xpp
reportDesign rd = ...; 
reportControl rc = rd.control(tablenum(CustGroup), 
    fieldnum(CustGroup, Name));
```

## <a name="method-controlcount"></a><span data-ttu-id="241d0-460">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="241d0-460">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="241d0-461">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="241d0-461">Return Value - controlCount</span></span>

## <a name="method-controlname"></a><span data-ttu-id="241d0-462">メソッド controlName</span><span class="sxs-lookup"><span data-stu-id="241d0-462">Method controlName</span></span>

<span data-ttu-id="241d0-463">コントロールの Name プロパティに基づいて、生成されたデザインのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-463">Finds a control in the generated design, based on the control's Name property.</span></span>

```xpp
public ReportControl controlName(str name)
```

### <a name="parameters---controlname"></a><span data-ttu-id="241d0-464">パラメーター - controlName</span><span class="sxs-lookup"><span data-stu-id="241d0-464">Parameters - controlName</span></span>

<span data-ttu-id="241d0-465">名前</span><span class="sxs-lookup"><span data-stu-id="241d0-465">name</span></span>  
<span data-ttu-id="241d0-466">文字列としての表現される、コントロールの Name プロパティ。</span><span class="sxs-lookup"><span data-stu-id="241d0-466">The Name property of the control, expressed as a string.</span></span>

### <a name="return-value---controlname"></a><span data-ttu-id="241d0-467">戻り値 - controlName</span><span class="sxs-lookup"><span data-stu-id="241d0-467">Return Value - controlName</span></span>

<span data-ttu-id="241d0-468">見つかったコントロール。</span><span class="sxs-lookup"><span data-stu-id="241d0-468">The control that is found.</span></span>

## <a name="method-controlnumber"></a><span data-ttu-id="241d0-469">メソッド controlNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-469">Method controlNumber</span></span>

```xpp
public ReportControl controlNumber(int number)
```

### <a name="parameters---controlnumber"></a><span data-ttu-id="241d0-470">パラメーター - controlNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-470">Parameters - controlNumber</span></span>

<span data-ttu-id="241d0-471">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-471">number</span></span>  

### <a name="return-value---controlnumber"></a><span data-ttu-id="241d0-472">戻り値 - controlNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-472">Return Value - controlNumber</span></span>

## <a name="method-copies"></a><span data-ttu-id="241d0-473">メソッド copies</span><span class="sxs-lookup"><span data-stu-id="241d0-473">Method copies</span></span>

```xpp
public int copies([int numberOfCopies])
```

### <a name="parameters---copies"></a><span data-ttu-id="241d0-474">パラメーター - copies</span><span class="sxs-lookup"><span data-stu-id="241d0-474">Parameters - copies</span></span>

<span data-ttu-id="241d0-475">numberOfCopies</span><span class="sxs-lookup"><span data-stu-id="241d0-475">numberOfCopies</span></span>  

### <a name="return-value---copies"></a><span data-ttu-id="241d0-476">戻り値 - copies</span><span class="sxs-lookup"><span data-stu-id="241d0-476">Return Value - copies</span></span>

## <a name="method-delete"></a><span data-ttu-id="241d0-477">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="241d0-477">Method delete</span></span>

<span data-ttu-id="241d0-478">ノードを AOT から削除します。</span><span class="sxs-lookup"><span data-stu-id="241d0-478">Deletes the node from the AOT.</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="241d0-479">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="241d0-479">Return Value - delete</span></span>

<span data-ttu-id="241d0-480">整数。</span><span class="sxs-lookup"><span data-stu-id="241d0-480">An integer.</span></span>

## <a name="method-description"></a><span data-ttu-id="241d0-481">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="241d0-481">Method description</span></span>

```xpp
public str description([str value])
```

### <a name="parameters---description"></a><span data-ttu-id="241d0-482">パラメーター - description</span><span class="sxs-lookup"><span data-stu-id="241d0-482">Parameters - description</span></span>

<span data-ttu-id="241d0-483">値</span><span class="sxs-lookup"><span data-stu-id="241d0-483">value</span></span>  

### <a name="return-value---description"></a><span data-ttu-id="241d0-484">戻り値 - description</span><span class="sxs-lookup"><span data-stu-id="241d0-484">Return Value - description</span></span>

## <a name="method-devicename"></a><span data-ttu-id="241d0-485">メソッド deviceName</span><span class="sxs-lookup"><span data-stu-id="241d0-485">Method deviceName</span></span>

```xpp
public str deviceName([str device])
```

### <a name="parameters---devicename"></a><span data-ttu-id="241d0-486">パラメーター - deviceName</span><span class="sxs-lookup"><span data-stu-id="241d0-486">Parameters - deviceName</span></span>

<span data-ttu-id="241d0-487">デバイス</span><span class="sxs-lookup"><span data-stu-id="241d0-487">device</span></span>  

### <a name="return-value---devicename"></a><span data-ttu-id="241d0-488">戻り値 - deviceName</span><span class="sxs-lookup"><span data-stu-id="241d0-488">Return Value - deviceName</span></span>

## <a name="method-drivername"></a><span data-ttu-id="241d0-489">メソッド driverName</span><span class="sxs-lookup"><span data-stu-id="241d0-489">Method driverName</span></span>

```xpp
public str driverName()
```

### <a name="return-value---drivername"></a><span data-ttu-id="241d0-490">戻り値 - driverName</span><span class="sxs-lookup"><span data-stu-id="241d0-490">Return Value - driverName</span></span>

## <a name="method-edit"></a><span data-ttu-id="241d0-491">メソッド edit</span><span class="sxs-lookup"><span data-stu-id="241d0-491">Method edit</span></span>

```xpp
public boolean edit()
```

### <a name="return-value---edit"></a><span data-ttu-id="241d0-492">戻り値 - edit</span><span class="sxs-lookup"><span data-stu-id="241d0-492">Return Value - edit</span></span>

## <a name="method-emptyreportprompt"></a><span data-ttu-id="241d0-493">メソッド emptyReportPrompt</span><span class="sxs-lookup"><span data-stu-id="241d0-493">Method emptyReportPrompt</span></span>

```xpp
public str emptyReportPrompt([str value])
```

### <a name="parameters---emptyreportprompt"></a><span data-ttu-id="241d0-494">パラメーター - emptyReportPrompt</span><span class="sxs-lookup"><span data-stu-id="241d0-494">Parameters - emptyReportPrompt</span></span>

<span data-ttu-id="241d0-495">値</span><span class="sxs-lookup"><span data-stu-id="241d0-495">value</span></span>  

### <a name="return-value---emptyreportprompt"></a><span data-ttu-id="241d0-496">戻り値 - emptyReportPrompt</span><span class="sxs-lookup"><span data-stu-id="241d0-496">Return Value - emptyReportPrompt</span></span>

## <a name="method-fittopage"></a><span data-ttu-id="241d0-497">メソッド fitToPage</span><span class="sxs-lookup"><span data-stu-id="241d0-497">Method fitToPage</span></span>

```xpp
public int fitToPage([int value])
```

### <a name="parameters---fittopage"></a><span data-ttu-id="241d0-498">パラメーター - fitToPage</span><span class="sxs-lookup"><span data-stu-id="241d0-498">Parameters - fitToPage</span></span>

<span data-ttu-id="241d0-499">値</span><span class="sxs-lookup"><span data-stu-id="241d0-499">value</span></span>  

### <a name="return-value---fittopage"></a><span data-ttu-id="241d0-500">戻り値 - fitToPage</span><span class="sxs-lookup"><span data-stu-id="241d0-500">Return Value - fitToPage</span></span>

## <a name="method-font"></a><span data-ttu-id="241d0-501">メソッド font</span><span class="sxs-lookup"><span data-stu-id="241d0-501">Method font</span></span>

<span data-ttu-id="241d0-502">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-502">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="241d0-503">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="241d0-503">Parameters - font</span></span>

<span data-ttu-id="241d0-504">値</span><span class="sxs-lookup"><span data-stu-id="241d0-504">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="241d0-505">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="241d0-505">Return Value - font</span></span>

<span data-ttu-id="241d0-506">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="241d0-506">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="241d0-507">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="241d0-507">Method fontSize</span></span>

<span data-ttu-id="241d0-508">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-508">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="241d0-509">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="241d0-509">Parameters - fontSize</span></span>

<span data-ttu-id="241d0-510">値</span><span class="sxs-lookup"><span data-stu-id="241d0-510">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="241d0-511">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="241d0-511">Return Value - fontSize</span></span>

<span data-ttu-id="241d0-512">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="241d0-512">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="241d0-513">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d0-513">Method foregroundColor</span></span>

<span data-ttu-id="241d0-514">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-514">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="241d0-515">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d0-515">Parameters - foregroundColor</span></span>

<span data-ttu-id="241d0-516">値</span><span class="sxs-lookup"><span data-stu-id="241d0-516">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="241d0-517">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d0-517">Return Value - foregroundColor</span></span>

<span data-ttu-id="241d0-518">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="241d0-518">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="241d0-519">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d0-519">Remarks - foregroundColor</span></span>

<span data-ttu-id="241d0-520">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d0-520">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="241d0-521">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="241d0-521">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="241d0-522">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="241d0-522">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="241d0-523">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="241d0-523">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="241d0-524">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="241d0-524">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="241d0-525">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="241d0-525">The maximum value for a single byte is 255.</span></span>

## <a name="method-from"></a><span data-ttu-id="241d0-526">メソッド from</span><span class="sxs-lookup"><span data-stu-id="241d0-526">Method from</span></span>

```xpp
public int from([int fromPage])
```

### <a name="parameters---from"></a><span data-ttu-id="241d0-527">パラメーター - from</span><span class="sxs-lookup"><span data-stu-id="241d0-527">Parameters - from</span></span>

<span data-ttu-id="241d0-528">fromPage</span><span class="sxs-lookup"><span data-stu-id="241d0-528">fromPage</span></span>  

### <a name="return-value---from"></a><span data-ttu-id="241d0-529">戻り値 - from</span><span class="sxs-lookup"><span data-stu-id="241d0-529">Return Value - from</span></span>

## <a name="method-generatedesign"></a><span data-ttu-id="241d0-530">メソッド generateDesign</span><span class="sxs-lookup"><span data-stu-id="241d0-530">Method generateDesign</span></span>

```xpp
public int generateDesign()
```

### <a name="return-value---generatedesign"></a><span data-ttu-id="241d0-531">戻り値 - generateDesign</span><span class="sxs-lookup"><span data-stu-id="241d0-531">Return Value - generateDesign</span></span>

## <a name="method-getnumberofprinters"></a><span data-ttu-id="241d0-532">メソッド getNumberOfPrinters</span><span class="sxs-lookup"><span data-stu-id="241d0-532">Method getNumberOfPrinters</span></span>

```xpp
public int getNumberOfPrinters()
```

### <a name="return-value---getnumberofprinters"></a><span data-ttu-id="241d0-533">戻り値 - getNumberOfPrinters</span><span class="sxs-lookup"><span data-stu-id="241d0-533">Return Value - getNumberOfPrinters</span></span>

## <a name="method-getprinter"></a><span data-ttu-id="241d0-534">メソッド getPrinter</span><span class="sxs-lookup"><span data-stu-id="241d0-534">Method getPrinter</span></span>

```xpp
public str getPrinter(int number)
```

### <a name="parameters---getprinter"></a><span data-ttu-id="241d0-535">パラメーター - getPrinter</span><span class="sxs-lookup"><span data-stu-id="241d0-535">Parameters - getPrinter</span></span>

<span data-ttu-id="241d0-536">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-536">number</span></span>  

### <a name="return-value---getprinter"></a><span data-ttu-id="241d0-537">戻り値 - getPrinter</span><span class="sxs-lookup"><span data-stu-id="241d0-537">Return Value - getPrinter</span></span>

## <a name="method-gettarget"></a><span data-ttu-id="241d0-538">メソッド getTarget</span><span class="sxs-lookup"><span data-stu-id="241d0-538">Method getTarget</span></span>

<span data-ttu-id="241d0-539">レポートの印刷メディア ターゲットを返します。</span><span class="sxs-lookup"><span data-stu-id="241d0-539">Returns the print medium target for the report.</span></span>

```xpp
public PrintMedium getTarget()
```

### <a name="return-value---gettarget"></a><span data-ttu-id="241d0-540">戻り値 - getTarget</span><span class="sxs-lookup"><span data-stu-id="241d0-540">Return Value - getTarget</span></span>

<span data-ttu-id="241d0-541">レポートのターゲット。</span><span class="sxs-lookup"><span data-stu-id="241d0-541">The target for the report.</span></span>

## <a name="method-hideborder"></a><span data-ttu-id="241d0-542">メソッド hideBorder</span><span class="sxs-lookup"><span data-stu-id="241d0-542">Method hideBorder</span></span>

```xpp
public boolean hideBorder([boolean value])
```

### <a name="parameters---hideborder"></a><span data-ttu-id="241d0-543">パラメーター - hideBorder</span><span class="sxs-lookup"><span data-stu-id="241d0-543">Parameters - hideBorder</span></span>

<span data-ttu-id="241d0-544">値</span><span class="sxs-lookup"><span data-stu-id="241d0-544">value</span></span>  

### <a name="return-value---hideborder"></a><span data-ttu-id="241d0-545">戻り値 - hideBorder</span><span class="sxs-lookup"><span data-stu-id="241d0-545">Return Value - hideBorder</span></span>

## <a name="method-italic"></a><span data-ttu-id="241d0-546">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="241d0-546">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="241d0-547">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="241d0-547">Parameters - italic</span></span>

<span data-ttu-id="241d0-548">値</span><span class="sxs-lookup"><span data-stu-id="241d0-548">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="241d0-549">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="241d0-549">Return Value - italic</span></span>

## <a name="method-jobtype"></a><span data-ttu-id="241d0-550">メソッド jobType</span><span class="sxs-lookup"><span data-stu-id="241d0-550">Method jobType</span></span>

```xpp
public str jobType([str value])
```

### <a name="parameters---jobtype"></a><span data-ttu-id="241d0-551">パラメーター - jobType</span><span class="sxs-lookup"><span data-stu-id="241d0-551">Parameters - jobType</span></span>

<span data-ttu-id="241d0-552">値</span><span class="sxs-lookup"><span data-stu-id="241d0-552">value</span></span>  

### <a name="return-value---jobtype"></a><span data-ttu-id="241d0-553">戻り値 - jobType</span><span class="sxs-lookup"><span data-stu-id="241d0-553">Return Value - jobType</span></span>

## <a name="method-language"></a><span data-ttu-id="241d0-554">メソッド language</span><span class="sxs-lookup"><span data-stu-id="241d0-554">Method language</span></span>

```xpp
public int language([int value])
```

### <a name="parameters---language"></a><span data-ttu-id="241d0-555">パラメーター - language</span><span class="sxs-lookup"><span data-stu-id="241d0-555">Parameters - language</span></span>

<span data-ttu-id="241d0-556">値</span><span class="sxs-lookup"><span data-stu-id="241d0-556">value</span></span>  

### <a name="return-value---language"></a><span data-ttu-id="241d0-557">戻り値 - language</span><span class="sxs-lookup"><span data-stu-id="241d0-557">Return Value - language</span></span>

## <a name="method-languageid"></a><span data-ttu-id="241d0-558">メソッド languageID</span><span class="sxs-lookup"><span data-stu-id="241d0-558">Method languageID</span></span>

```xpp
public str languageID([str lan])
```

### <a name="parameters---languageid"></a><span data-ttu-id="241d0-559">パラメーター - languageID</span><span class="sxs-lookup"><span data-stu-id="241d0-559">Parameters - languageID</span></span>

<span data-ttu-id="241d0-560">lan</span><span class="sxs-lookup"><span data-stu-id="241d0-560">lan</span></span>  

### <a name="return-value---languageid"></a><span data-ttu-id="241d0-561">戻り値 - languageID</span><span class="sxs-lookup"><span data-stu-id="241d0-561">Return Value - languageID</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="241d0-562">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-562">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="241d0-563">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-563">Parameters - leftMarginMode</span></span>

<span data-ttu-id="241d0-564">値</span><span class="sxs-lookup"><span data-stu-id="241d0-564">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="241d0-565">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-565">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="241d0-566">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-566">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="241d0-567">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-567">Parameters - leftMarginStr</span></span>

<span data-ttu-id="241d0-568">値</span><span class="sxs-lookup"><span data-stu-id="241d0-568">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="241d0-569">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-569">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="241d0-570">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-570">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="241d0-571">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-571">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="241d0-572">値</span><span class="sxs-lookup"><span data-stu-id="241d0-572">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="241d0-573">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-573">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="241d0-574">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-574">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="241d0-575">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-575">Parameters - leftMarginValue</span></span>

<span data-ttu-id="241d0-576">値</span><span class="sxs-lookup"><span data-stu-id="241d0-576">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="241d0-577">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-577">Return Value - leftMarginValue</span></span>

## <a name="method-loaddisksettings"></a><span data-ttu-id="241d0-578">メソッド loadDiskSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-578">Method loadDiskSettings</span></span>

```xpp
public container loadDiskSettings()
```

### <a name="return-value---loaddisksettings"></a><span data-ttu-id="241d0-579">戻り値 - loadDiskSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-579">Return Value - loadDiskSettings</span></span>

## <a name="method-localwebmenu"></a><span data-ttu-id="241d0-580">メソッド localWebMenu</span><span class="sxs-lookup"><span data-stu-id="241d0-580">Method localWebMenu</span></span>

```xpp
public str localWebMenu([str value])
```

### <a name="parameters---localwebmenu"></a><span data-ttu-id="241d0-581">パラメーター - localWebMenu</span><span class="sxs-lookup"><span data-stu-id="241d0-581">Parameters - localWebMenu</span></span>

<span data-ttu-id="241d0-582">値</span><span class="sxs-lookup"><span data-stu-id="241d0-582">value</span></span>  

### <a name="return-value---localwebmenu"></a><span data-ttu-id="241d0-583">戻り値 - localWebMenu</span><span class="sxs-lookup"><span data-stu-id="241d0-583">Return Value - localWebMenu</span></span>

## <a name="method-lookupcaption"></a><span data-ttu-id="241d0-584">メソッド lookupCaption</span><span class="sxs-lookup"><span data-stu-id="241d0-584">Method lookupCaption</span></span>

```xpp
public str lookupCaption([str lan])
```

### <a name="parameters---lookupcaption"></a><span data-ttu-id="241d0-585">パラメーター - lookupCaption</span><span class="sxs-lookup"><span data-stu-id="241d0-585">Parameters - lookupCaption</span></span>

<span data-ttu-id="241d0-586">lan</span><span class="sxs-lookup"><span data-stu-id="241d0-586">lan</span></span>  

### <a name="return-value---lookupcaption"></a><span data-ttu-id="241d0-587">戻り値 - lookupCaption</span><span class="sxs-lookup"><span data-stu-id="241d0-587">Return Value - lookupCaption</span></span>

## <a name="method-lookuplabel"></a><span data-ttu-id="241d0-588">メソッド lookupLabel</span><span class="sxs-lookup"><span data-stu-id="241d0-588">Method lookupLabel</span></span>

```xpp
public str lookupLabel(str label, [str lan])
```

### <a name="parameters---lookuplabel"></a><span data-ttu-id="241d0-589">パラメーター - lookupLabel</span><span class="sxs-lookup"><span data-stu-id="241d0-589">Parameters - lookupLabel</span></span>

<span data-ttu-id="241d0-590">ラベル</span><span class="sxs-lookup"><span data-stu-id="241d0-590">label</span></span>  

<!-- -->

<span data-ttu-id="241d0-591">lan</span><span class="sxs-lookup"><span data-stu-id="241d0-591">lan</span></span>  

### <a name="return-value---lookuplabel"></a><span data-ttu-id="241d0-592">戻り値 - lookupLabel</span><span class="sxs-lookup"><span data-stu-id="241d0-592">Return Value - lookupLabel</span></span>

## <a name="method-makeautosection"></a><span data-ttu-id="241d0-593">メソッド makeAutoSection</span><span class="sxs-lookup"><span data-stu-id="241d0-593">Method makeAutoSection</span></span>

```xpp
public int makeAutoSection([Query query])
```

### <a name="parameters---makeautosection"></a><span data-ttu-id="241d0-594">パラメーター - makeAutoSection</span><span class="sxs-lookup"><span data-stu-id="241d0-594">Parameters - makeAutoSection</span></span>

<span data-ttu-id="241d0-595">クエリ</span><span class="sxs-lookup"><span data-stu-id="241d0-595">query</span></span>  

### <a name="return-value---makeautosection"></a><span data-ttu-id="241d0-596">戻り値 - makeAutoSection</span><span class="sxs-lookup"><span data-stu-id="241d0-596">Return Value - makeAutoSection</span></span>

## <a name="method-name"></a><span data-ttu-id="241d0-597">メソッド名</span><span class="sxs-lookup"><span data-stu-id="241d0-597">Method name</span></span>

<span data-ttu-id="241d0-598">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-598">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="241d0-599">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="241d0-599">Parameters - name</span></span>

<span data-ttu-id="241d0-600">値</span><span class="sxs-lookup"><span data-stu-id="241d0-600">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="241d0-601">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="241d0-601">Return Value - name</span></span>

<span data-ttu-id="241d0-602">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="241d0-602">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="241d0-603">備考 - name</span><span class="sxs-lookup"><span data-stu-id="241d0-603">Remarks - name</span></span>

<span data-ttu-id="241d0-604">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="241d0-604">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="241d0-605">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="241d0-605">Begins with a letter.</span></span>
-   <span data-ttu-id="241d0-606">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="241d0-606">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="241d0-607">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="241d0-607">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="241d0-608">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="241d0-608">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="241d0-609">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="241d0-609">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-orientation"></a><span data-ttu-id="241d0-610">メソッド orientation</span><span class="sxs-lookup"><span data-stu-id="241d0-610">Method orientation</span></span>

```xpp
public int orientation([int value])
```

### <a name="parameters---orientation"></a><span data-ttu-id="241d0-611">パラメーター - orientation</span><span class="sxs-lookup"><span data-stu-id="241d0-611">Parameters - orientation</span></span>

<span data-ttu-id="241d0-612">値</span><span class="sxs-lookup"><span data-stu-id="241d0-612">value</span></span>  

### <a name="return-value---orientation"></a><span data-ttu-id="241d0-613">戻り値 - orientation</span><span class="sxs-lookup"><span data-stu-id="241d0-613">Return Value - orientation</span></span>

## <a name="method-pack"></a><span data-ttu-id="241d0-614">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="241d0-614">Method pack</span></span>

<span data-ttu-id="241d0-615">ReportDesign クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="241d0-615">Serializes the current instance of the ReportDesign class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="241d0-616">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="241d0-616">Return Value - pack</span></span>

<span data-ttu-id="241d0-617">ReportDesign クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="241d0-617">A container that contains the current instance of the ReportDesign class.</span></span>

## <a name="method-packpagesettings"></a><span data-ttu-id="241d0-618">メソッド packPageSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-618">Method packPageSettings</span></span>

```xpp
public container packPageSettings()
```

### <a name="return-value---packpagesettings"></a><span data-ttu-id="241d0-619">戻り値 - packPageSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-619">Return Value - packPageSettings</span></span>

## <a name="method-packprintersettings"></a><span data-ttu-id="241d0-620">メソッド packPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-620">Method packPrinterSettings</span></span>

```xpp
public container packPrinterSettings()
```

### <a name="return-value---packprintersettings"></a><span data-ttu-id="241d0-621">戻り値 - packPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-621">Return Value - packPrinterSettings</span></span>

## <a name="method-packprintjobsettings"></a><span data-ttu-id="241d0-622">メソッド packPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-622">Method packPrintJobSettings</span></span>

```xpp
public container packPrintJobSettings()
```

### <a name="return-value---packprintjobsettings"></a><span data-ttu-id="241d0-623">戻り値 - packPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-623">Return Value - packPrintJobSettings</span></span>

## <a name="method-pageformatting"></a><span data-ttu-id="241d0-624">メソッド pageFormatting</span><span class="sxs-lookup"><span data-stu-id="241d0-624">Method pageFormatting</span></span>

```xpp
public boolean pageFormatting()
```

### <a name="return-value---pageformatting"></a><span data-ttu-id="241d0-625">戻り値 - pageFormatting</span><span class="sxs-lookup"><span data-stu-id="241d0-625">Return Value - pageFormatting</span></span>

## <a name="method-paperorientation"></a><span data-ttu-id="241d0-626">メソッド paperOrientation</span><span class="sxs-lookup"><span data-stu-id="241d0-626">Method paperOrientation</span></span>

```xpp
public PrinterOrientation paperOrientation([PrinterOrientation orientation])
```

### <a name="parameters---paperorientation"></a><span data-ttu-id="241d0-627">パラメーター - paperOrientation</span><span class="sxs-lookup"><span data-stu-id="241d0-627">Parameters - paperOrientation</span></span>

<span data-ttu-id="241d0-628">orientation</span><span class="sxs-lookup"><span data-stu-id="241d0-628">orientation</span></span>  

### <a name="return-value---paperorientation"></a><span data-ttu-id="241d0-629">戻り値 - paperOrientation</span><span class="sxs-lookup"><span data-stu-id="241d0-629">Return Value - paperOrientation</span></span>

## <a name="method-papertray"></a><span data-ttu-id="241d0-630">メソッド paperTray</span><span class="sxs-lookup"><span data-stu-id="241d0-630">Method paperTray</span></span>

```xpp
public int paperTray([int tray])
```

### <a name="parameters---papertray"></a><span data-ttu-id="241d0-631">パラメーター - paperTray</span><span class="sxs-lookup"><span data-stu-id="241d0-631">Parameters - paperTray</span></span>

<span data-ttu-id="241d0-632">トレイ</span><span class="sxs-lookup"><span data-stu-id="241d0-632">tray</span></span>  

### <a name="return-value---papertray"></a><span data-ttu-id="241d0-633">戻り値 - paperTray</span><span class="sxs-lookup"><span data-stu-id="241d0-633">Return Value - paperTray</span></span>

## <a name="method-printerattributes"></a><span data-ttu-id="241d0-634">メソッド printerAttributes</span><span class="sxs-lookup"><span data-stu-id="241d0-634">Method printerAttributes</span></span>

```xpp
public int printerAttributes()
```

### <a name="return-value---printerattributes"></a><span data-ttu-id="241d0-635">戻り値 - printerAttributes</span><span class="sxs-lookup"><span data-stu-id="241d0-635">Return Value - printerAttributes</span></span>

## <a name="method-printeraverageppm"></a><span data-ttu-id="241d0-636">メソッド printerAveragePPM</span><span class="sxs-lookup"><span data-stu-id="241d0-636">Method printerAveragePPM</span></span>

```xpp
public int printerAveragePPM()
```

### <a name="return-value---printeraverageppm"></a><span data-ttu-id="241d0-637">戻り値 - printerAveragePPM</span><span class="sxs-lookup"><span data-stu-id="241d0-637">Return Value - printerAveragePPM</span></span>

## <a name="method-printercomment"></a><span data-ttu-id="241d0-638">メソッド printerComment</span><span class="sxs-lookup"><span data-stu-id="241d0-638">Method printerComment</span></span>

```xpp
public str printerComment()
```

### <a name="return-value---printercomment"></a><span data-ttu-id="241d0-639">戻り値 - printerComment</span><span class="sxs-lookup"><span data-stu-id="241d0-639">Return Value - printerComment</span></span>

## <a name="method-printerdatatype"></a><span data-ttu-id="241d0-640">メソッド printerDatatype</span><span class="sxs-lookup"><span data-stu-id="241d0-640">Method printerDatatype</span></span>

```xpp
public str printerDatatype()
```

### <a name="return-value---printerdatatype"></a><span data-ttu-id="241d0-641">戻り値 - printerDatatype</span><span class="sxs-lookup"><span data-stu-id="241d0-641">Return Value - printerDatatype</span></span>

## <a name="method-printerdefaultpriority"></a><span data-ttu-id="241d0-642">メソッド printerDefaultPriority</span><span class="sxs-lookup"><span data-stu-id="241d0-642">Method printerDefaultPriority</span></span>

```xpp
public int printerDefaultPriority()
```

### <a name="return-value---printerdefaultpriority"></a><span data-ttu-id="241d0-643">戻り値 - printerDefaultPriority</span><span class="sxs-lookup"><span data-stu-id="241d0-643">Return Value - printerDefaultPriority</span></span>

## <a name="method-printerdrivername"></a><span data-ttu-id="241d0-644">メソッド printerDriverName</span><span class="sxs-lookup"><span data-stu-id="241d0-644">Method printerDriverName</span></span>

```xpp
public str printerDriverName()
```

### <a name="return-value---printerdrivername"></a><span data-ttu-id="241d0-645">戻り値 - printerDriverName</span><span class="sxs-lookup"><span data-stu-id="241d0-645">Return Value - printerDriverName</span></span>

## <a name="method-printerlocation"></a><span data-ttu-id="241d0-646">メソッド printerLocation</span><span class="sxs-lookup"><span data-stu-id="241d0-646">Method printerLocation</span></span>

```xpp
public str printerLocation()
```

### <a name="return-value---printerlocation"></a><span data-ttu-id="241d0-647">戻り値 - printerLocation</span><span class="sxs-lookup"><span data-stu-id="241d0-647">Return Value - printerLocation</span></span>

## <a name="method-printerpageheight"></a><span data-ttu-id="241d0-648">メソッド printerPageHeight</span><span class="sxs-lookup"><span data-stu-id="241d0-648">Method printerPageHeight</span></span>

```xpp
public int printerPageHeight()
```

### <a name="return-value---printerpageheight"></a><span data-ttu-id="241d0-649">戻り値 - printerPageHeight</span><span class="sxs-lookup"><span data-stu-id="241d0-649">Return Value - printerPageHeight</span></span>

## <a name="method-printerpagewidth"></a><span data-ttu-id="241d0-650">メソッド printerPageWidth</span><span class="sxs-lookup"><span data-stu-id="241d0-650">Method printerPageWidth</span></span>

```xpp
public int printerPageWidth()
```

### <a name="return-value---printerpagewidth"></a><span data-ttu-id="241d0-651">戻り値 - printerPageWidth</span><span class="sxs-lookup"><span data-stu-id="241d0-651">Return Value - printerPageWidth</span></span>

## <a name="method-printerpaper"></a><span data-ttu-id="241d0-652">メソッド printerPaper</span><span class="sxs-lookup"><span data-stu-id="241d0-652">Method printerPaper</span></span>

```xpp
public int printerPaper()
```

### <a name="return-value---printerpaper"></a><span data-ttu-id="241d0-653">戻り値 - printerPaper</span><span class="sxs-lookup"><span data-stu-id="241d0-653">Return Value - printerPaper</span></span>

## <a name="method-printerparameters"></a><span data-ttu-id="241d0-654">メソッド printerParameters</span><span class="sxs-lookup"><span data-stu-id="241d0-654">Method printerParameters</span></span>

```xpp
public str printerParameters()
```

### <a name="return-value---printerparameters"></a><span data-ttu-id="241d0-655">戻り値 - printerParameters</span><span class="sxs-lookup"><span data-stu-id="241d0-655">Return Value - printerParameters</span></span>

## <a name="method-printerportname"></a><span data-ttu-id="241d0-656">メソッド printerPortName</span><span class="sxs-lookup"><span data-stu-id="241d0-656">Method printerPortName</span></span>

```xpp
public str printerPortName()
```

### <a name="return-value---printerportname"></a><span data-ttu-id="241d0-657">戻り値 - printerPortName</span><span class="sxs-lookup"><span data-stu-id="241d0-657">Return Value - printerPortName</span></span>

## <a name="method-printerprintername"></a><span data-ttu-id="241d0-658">メソッド printerPrinterName</span><span class="sxs-lookup"><span data-stu-id="241d0-658">Method printerPrinterName</span></span>

```xpp
public str printerPrinterName()
```

### <a name="return-value---printerprintername"></a><span data-ttu-id="241d0-659">戻り値 - printerPrinterName</span><span class="sxs-lookup"><span data-stu-id="241d0-659">Return Value - printerPrinterName</span></span>

## <a name="method-printerprintprocessor"></a><span data-ttu-id="241d0-660">メソッド printerPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="241d0-660">Method printerPrintProcessor</span></span>

```xpp
public str printerPrintProcessor()
```

### <a name="return-value---printerprintprocessor"></a><span data-ttu-id="241d0-661">戻り値 - printerPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="241d0-661">Return Value - printerPrintProcessor</span></span>

## <a name="method-printerpriority"></a><span data-ttu-id="241d0-662">メソッド printerPriority</span><span class="sxs-lookup"><span data-stu-id="241d0-662">Method printerPriority</span></span>

```xpp
public int printerPriority()
```

### <a name="return-value---printerpriority"></a><span data-ttu-id="241d0-663">戻り値 - printerPriority</span><span class="sxs-lookup"><span data-stu-id="241d0-663">Return Value - printerPriority</span></span>

## <a name="method-printerqueuedjobs"></a><span data-ttu-id="241d0-664">メソッド printerQueuedJobs</span><span class="sxs-lookup"><span data-stu-id="241d0-664">Method printerQueuedJobs</span></span>

```xpp
public int printerQueuedJobs()
```

### <a name="return-value---printerqueuedjobs"></a><span data-ttu-id="241d0-665">戻り値 - printerQueuedJobs</span><span class="sxs-lookup"><span data-stu-id="241d0-665">Return Value - printerQueuedJobs</span></span>

## <a name="method-printersepfile"></a><span data-ttu-id="241d0-666">メソッド printerSepFile</span><span class="sxs-lookup"><span data-stu-id="241d0-666">Method printerSepFile</span></span>

```xpp
public str printerSepFile()
```

### <a name="return-value---printersepfile"></a><span data-ttu-id="241d0-667">戻り値 - printerSepFile</span><span class="sxs-lookup"><span data-stu-id="241d0-667">Return Value - printerSepFile</span></span>

## <a name="method-printerservername"></a><span data-ttu-id="241d0-668">メソッド printerServerName</span><span class="sxs-lookup"><span data-stu-id="241d0-668">Method printerServerName</span></span>

```xpp
public str printerServerName()
```

### <a name="return-value---printerservername"></a><span data-ttu-id="241d0-669">戻り値 - printerServerName</span><span class="sxs-lookup"><span data-stu-id="241d0-669">Return Value - printerServerName</span></span>

## <a name="method-printersettings"></a><span data-ttu-id="241d0-670">メソッド printerSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-670">Method printerSettings</span></span>

```xpp
public boolean printerSettings([ReportRun reportRun], [int showWhat])
```

### <a name="parameters---printersettings"></a><span data-ttu-id="241d0-671">パラメーター - printerSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-671">Parameters - printerSettings</span></span>

<span data-ttu-id="241d0-672">reportRun</span><span class="sxs-lookup"><span data-stu-id="241d0-672">reportRun</span></span>  

<!-- -->

<span data-ttu-id="241d0-673">showWhat</span><span class="sxs-lookup"><span data-stu-id="241d0-673">showWhat</span></span>  

### <a name="return-value---printersettings"></a><span data-ttu-id="241d0-674">戻り値 - printerSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-674">Return Value - printerSettings</span></span>

## <a name="method-printersharename"></a><span data-ttu-id="241d0-675">メソッド printerShareName</span><span class="sxs-lookup"><span data-stu-id="241d0-675">Method printerShareName</span></span>

```xpp
public str printerShareName()
```

### <a name="return-value---printersharename"></a><span data-ttu-id="241d0-676">戻り値 - printerShareName</span><span class="sxs-lookup"><span data-stu-id="241d0-676">Return Value - printerShareName</span></span>

## <a name="method-printerstarttime"></a><span data-ttu-id="241d0-677">メソッド printerStartTime</span><span class="sxs-lookup"><span data-stu-id="241d0-677">Method printerStartTime</span></span>

```xpp
public int printerStartTime()
```

### <a name="return-value---printerstarttime"></a><span data-ttu-id="241d0-678">戻り値 - printerStartTime</span><span class="sxs-lookup"><span data-stu-id="241d0-678">Return Value - printerStartTime</span></span>

## <a name="method-printerstatus"></a><span data-ttu-id="241d0-679">メソッド printerStatus</span><span class="sxs-lookup"><span data-stu-id="241d0-679">Method printerStatus</span></span>

```xpp
public int printerStatus()
```

### <a name="return-value---printerstatus"></a><span data-ttu-id="241d0-680">戻り値 - printerStatus</span><span class="sxs-lookup"><span data-stu-id="241d0-680">Return Value - printerStatus</span></span>

## <a name="method-printeruntiltime"></a><span data-ttu-id="241d0-681">メソッド printerUntilTime</span><span class="sxs-lookup"><span data-stu-id="241d0-681">Method printerUntilTime</span></span>

```xpp
public int printerUntilTime()
```

### <a name="return-value---printeruntiltime"></a><span data-ttu-id="241d0-682">戻り値 - printerUntilTime</span><span class="sxs-lookup"><span data-stu-id="241d0-682">Return Value - printerUntilTime</span></span>

## <a name="method-printformname"></a><span data-ttu-id="241d0-683">メソッド printFormName</span><span class="sxs-lookup"><span data-stu-id="241d0-683">Method printFormName</span></span>

```xpp
public str printFormName([str value])
```

### <a name="parameters---printformname"></a><span data-ttu-id="241d0-684">パラメーター - printFormName</span><span class="sxs-lookup"><span data-stu-id="241d0-684">Parameters - printFormName</span></span>

<span data-ttu-id="241d0-685">値</span><span class="sxs-lookup"><span data-stu-id="241d0-685">value</span></span>  

### <a name="return-value---printformname"></a><span data-ttu-id="241d0-686">戻り値 - printFormName</span><span class="sxs-lookup"><span data-stu-id="241d0-686">Return Value - printFormName</span></span>

## <a name="method-printjobsettings"></a><span data-ttu-id="241d0-687">メソッド printJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-687">Method printJobSettings</span></span>

```xpp
public PrintJobSettings printJobSettings()
```

### <a name="return-value---printjobsettings"></a><span data-ttu-id="241d0-688">戻り値 - printJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-688">Return Value - printJobSettings</span></span>

## <a name="method-removeredundantfooters"></a><span data-ttu-id="241d0-689">メソッド removeRedundantFooters</span><span class="sxs-lookup"><span data-stu-id="241d0-689">Method removeRedundantFooters</span></span>

```xpp
public boolean removeRedundantFooters([boolean value])
```

### <a name="parameters---removeredundantfooters"></a><span data-ttu-id="241d0-690">パラメーター - removeRedundantFooters</span><span class="sxs-lookup"><span data-stu-id="241d0-690">Parameters - removeRedundantFooters</span></span>

<span data-ttu-id="241d0-691">値</span><span class="sxs-lookup"><span data-stu-id="241d0-691">value</span></span>  

### <a name="return-value---removeredundantfooters"></a><span data-ttu-id="241d0-692">戻り値 - removeRedundantFooters</span><span class="sxs-lookup"><span data-stu-id="241d0-692">Return Value - removeRedundantFooters</span></span>

## <a name="method-removerepeatedfooters"></a><span data-ttu-id="241d0-693">メソッド removeRepeatedFooters</span><span class="sxs-lookup"><span data-stu-id="241d0-693">Method removeRepeatedFooters</span></span>

```xpp
public boolean removeRepeatedFooters([boolean value])
```

### <a name="parameters---removerepeatedfooters"></a><span data-ttu-id="241d0-694">パラメーター - removeRepeatedFooters</span><span class="sxs-lookup"><span data-stu-id="241d0-694">Parameters - removeRepeatedFooters</span></span>

<span data-ttu-id="241d0-695">値</span><span class="sxs-lookup"><span data-stu-id="241d0-695">value</span></span>  

### <a name="return-value---removerepeatedfooters"></a><span data-ttu-id="241d0-696">戻り値 - removeRepeatedFooters</span><span class="sxs-lookup"><span data-stu-id="241d0-696">Return Value - removeRepeatedFooters</span></span>

## <a name="method-removerepeatedheaders"></a><span data-ttu-id="241d0-697">メソッド removeRepeatedHeaders</span><span class="sxs-lookup"><span data-stu-id="241d0-697">Method removeRepeatedHeaders</span></span>

```xpp
public boolean removeRepeatedHeaders([boolean value])
```

### <a name="parameters---removerepeatedheaders"></a><span data-ttu-id="241d0-698">パラメーター - removeRepeatedHeaders</span><span class="sxs-lookup"><span data-stu-id="241d0-698">Parameters - removeRepeatedHeaders</span></span>

<span data-ttu-id="241d0-699">値</span><span class="sxs-lookup"><span data-stu-id="241d0-699">value</span></span>  

### <a name="return-value---removerepeatedheaders"></a><span data-ttu-id="241d0-700">戻り値 - removeRepeatedHeaders</span><span class="sxs-lookup"><span data-stu-id="241d0-700">Return Value - removeRepeatedHeaders</span></span>

## <a name="method-reporttemplate"></a><span data-ttu-id="241d0-701">メソッド reportTemplate</span><span class="sxs-lookup"><span data-stu-id="241d0-701">Method reportTemplate</span></span>

```xpp
public str reportTemplate([str value])
```

### <a name="parameters---reporttemplate"></a><span data-ttu-id="241d0-702">パラメーター - reportTemplate</span><span class="sxs-lookup"><span data-stu-id="241d0-702">Parameters - reportTemplate</span></span>

<span data-ttu-id="241d0-703">値</span><span class="sxs-lookup"><span data-stu-id="241d0-703">value</span></span>  

### <a name="return-value---reporttemplate"></a><span data-ttu-id="241d0-704">戻り値 - reportTemplate</span><span class="sxs-lookup"><span data-stu-id="241d0-704">Return Value - reportTemplate</span></span>

## <a name="method-resolutionx"></a><span data-ttu-id="241d0-705">メソッド resolutionX</span><span class="sxs-lookup"><span data-stu-id="241d0-705">Method resolutionX</span></span>

```xpp
public str resolutionX([str value])
```

### <a name="parameters---resolutionx"></a><span data-ttu-id="241d0-706">パラメーター - resolutionX</span><span class="sxs-lookup"><span data-stu-id="241d0-706">Parameters - resolutionX</span></span>

<span data-ttu-id="241d0-707">値</span><span class="sxs-lookup"><span data-stu-id="241d0-707">value</span></span>  

### <a name="return-value---resolutionx"></a><span data-ttu-id="241d0-708">戻り値 - resolutionX</span><span class="sxs-lookup"><span data-stu-id="241d0-708">Return Value - resolutionX</span></span>

## <a name="method-resolutionxstr"></a><span data-ttu-id="241d0-709">メソッド resolutionXStr</span><span class="sxs-lookup"><span data-stu-id="241d0-709">Method resolutionXStr</span></span>

```xpp
public int resolutionXStr(str value)
```

### <a name="parameters---resolutionxstr"></a><span data-ttu-id="241d0-710">パラメーター - resolutionXStr</span><span class="sxs-lookup"><span data-stu-id="241d0-710">Parameters - resolutionXStr</span></span>

<span data-ttu-id="241d0-711">値</span><span class="sxs-lookup"><span data-stu-id="241d0-711">value</span></span>  

### <a name="return-value---resolutionxstr"></a><span data-ttu-id="241d0-712">戻り値 - resolutionXStr</span><span class="sxs-lookup"><span data-stu-id="241d0-712">Return Value - resolutionXStr</span></span>

## <a name="method-resolutionxunit"></a><span data-ttu-id="241d0-713">メソッド resolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-713">Method resolutionXUnit</span></span>

```xpp
public Units resolutionXUnit([Units value])
```

### <a name="parameters---resolutionxunit"></a><span data-ttu-id="241d0-714">パラメーター - resolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-714">Parameters - resolutionXUnit</span></span>

<span data-ttu-id="241d0-715">値</span><span class="sxs-lookup"><span data-stu-id="241d0-715">value</span></span>  

### <a name="return-value---resolutionxunit"></a><span data-ttu-id="241d0-716">戻り値 - resolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-716">Return Value - resolutionXUnit</span></span>

## <a name="method-resolutiony"></a><span data-ttu-id="241d0-717">メソッド resolutionY</span><span class="sxs-lookup"><span data-stu-id="241d0-717">Method resolutionY</span></span>

```xpp
public str resolutionY([str value])
```

### <a name="parameters---resolutiony"></a><span data-ttu-id="241d0-718">パラメーター - resolutionY</span><span class="sxs-lookup"><span data-stu-id="241d0-718">Parameters - resolutionY</span></span>

<span data-ttu-id="241d0-719">値</span><span class="sxs-lookup"><span data-stu-id="241d0-719">value</span></span>  

### <a name="return-value---resolutiony"></a><span data-ttu-id="241d0-720">戻り値 - resolutionY</span><span class="sxs-lookup"><span data-stu-id="241d0-720">Return Value - resolutionY</span></span>

## <a name="method-resolutionystr"></a><span data-ttu-id="241d0-721">メソッド resolutionYStr</span><span class="sxs-lookup"><span data-stu-id="241d0-721">Method resolutionYStr</span></span>

```xpp
public int resolutionYStr(str value)
```

### <a name="parameters---resolutionystr"></a><span data-ttu-id="241d0-722">パラメーター - resolutionYStr</span><span class="sxs-lookup"><span data-stu-id="241d0-722">Parameters - resolutionYStr</span></span>

<span data-ttu-id="241d0-723">値</span><span class="sxs-lookup"><span data-stu-id="241d0-723">value</span></span>  

### <a name="return-value---resolutionystr"></a><span data-ttu-id="241d0-724">戻り値 - resolutionYStr</span><span class="sxs-lookup"><span data-stu-id="241d0-724">Return Value - resolutionYStr</span></span>

## <a name="method-resolutionyunit"></a><span data-ttu-id="241d0-725">メソッド resolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-725">Method resolutionYUnit</span></span>

```xpp
public Units resolutionYUnit([Units value])
```

### <a name="parameters---resolutionyunit"></a><span data-ttu-id="241d0-726">パラメーター - resolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-726">Parameters - resolutionYUnit</span></span>

<span data-ttu-id="241d0-727">値</span><span class="sxs-lookup"><span data-stu-id="241d0-727">value</span></span>  

### <a name="return-value---resolutionyunit"></a><span data-ttu-id="241d0-728">戻り値 - resolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-728">Return Value - resolutionYUnit</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="241d0-729">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-729">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="241d0-730">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-730">Parameters - rightMarginMode</span></span>

<span data-ttu-id="241d0-731">値</span><span class="sxs-lookup"><span data-stu-id="241d0-731">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="241d0-732">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-732">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="241d0-733">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-733">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="241d0-734">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-734">Parameters - rightMarginStr</span></span>

<span data-ttu-id="241d0-735">値</span><span class="sxs-lookup"><span data-stu-id="241d0-735">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="241d0-736">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-736">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="241d0-737">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-737">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="241d0-738">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-738">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="241d0-739">値</span><span class="sxs-lookup"><span data-stu-id="241d0-739">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="241d0-740">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-740">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="241d0-741">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-741">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="241d0-742">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-742">Parameters - rightMarginValue</span></span>

<span data-ttu-id="241d0-743">値</span><span class="sxs-lookup"><span data-stu-id="241d0-743">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="241d0-744">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-744">Return Value - rightMarginValue</span></span>

## <a name="method-ruler"></a><span data-ttu-id="241d0-745">メソッド ruler</span><span class="sxs-lookup"><span data-stu-id="241d0-745">Method ruler</span></span>

```xpp
public int ruler([int value])
```

### <a name="parameters---ruler"></a><span data-ttu-id="241d0-746">パラメーター - ruler</span><span class="sxs-lookup"><span data-stu-id="241d0-746">Parameters - ruler</span></span>

<span data-ttu-id="241d0-747">値</span><span class="sxs-lookup"><span data-stu-id="241d0-747">value</span></span>  

### <a name="return-value---ruler"></a><span data-ttu-id="241d0-748">戻り値 - ruler</span><span class="sxs-lookup"><span data-stu-id="241d0-748">Return Value - ruler</span></span>

## <a name="method-savedisksettings"></a><span data-ttu-id="241d0-749">メソッド saveDiskSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-749">Method saveDiskSettings</span></span>

```xpp
public boolean saveDiskSettings(container buffer)
```

### <a name="parameters---savedisksettings"></a><span data-ttu-id="241d0-750">パラメーター - saveDiskSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-750">Parameters - saveDiskSettings</span></span>

<span data-ttu-id="241d0-751">バッファ</span><span class="sxs-lookup"><span data-stu-id="241d0-751">buffer</span></span>  

### <a name="return-value---savedisksettings"></a><span data-ttu-id="241d0-752">戻り値 - saveDiskSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-752">Return Value - saveDiskSettings</span></span>

## <a name="method-section"></a><span data-ttu-id="241d0-753">メソッド section</span><span class="sxs-lookup"><span data-stu-id="241d0-753">Method section</span></span>

<span data-ttu-id="241d0-754">生成されたデザイン ノードの下のセクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-754">Finds a section below the generated design node.</span></span>

```xpp
public ReportSection section(int number)
```

### <a name="parameters---section"></a><span data-ttu-id="241d0-755">パラメーター - section</span><span class="sxs-lookup"><span data-stu-id="241d0-755">Parameters - section</span></span>

<span data-ttu-id="241d0-756">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-756">number</span></span>  
<span data-ttu-id="241d0-757">セクション番号。</span><span class="sxs-lookup"><span data-stu-id="241d0-757">The section number.</span></span>

### <a name="return-value---section"></a><span data-ttu-id="241d0-758">戻り値 - section</span><span class="sxs-lookup"><span data-stu-id="241d0-758">Return Value - section</span></span>

<span data-ttu-id="241d0-759">検索されるレポート セクション。</span><span class="sxs-lookup"><span data-stu-id="241d0-759">The report section that is found.</span></span>

## <a name="method-sectioncount"></a><span data-ttu-id="241d0-760">メソッド sectionCount</span><span class="sxs-lookup"><span data-stu-id="241d0-760">Method sectionCount</span></span>

```xpp
public int sectionCount()
```

### <a name="return-value---sectioncount"></a><span data-ttu-id="241d0-761">戻り値 - sectionCount</span><span class="sxs-lookup"><span data-stu-id="241d0-761">Return Value - sectionCount</span></span>

## <a name="method-sectiongroup"></a><span data-ttu-id="241d0-762">メソッド sectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-762">Method sectionGroup</span></span>

<span data-ttu-id="241d0-763">reportDesign オブジェクトの下の reportSectionGroup オブジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-763">Finds a reportSectionGroup object below a reportDesign object.</span></span>

```xpp
public ReportSectionGroup sectionGroup(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---sectiongroup"></a><span data-ttu-id="241d0-764">パラメーター - sectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-764">Parameters - sectionGroup</span></span>

<span data-ttu-id="241d0-765">tableId</span><span class="sxs-lookup"><span data-stu-id="241d0-765">tableId</span></span>  
<span data-ttu-id="241d0-766">セクション グループのフィールド (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d0-766">The field of the section group; optional.</span></span>

<!-- -->

<span data-ttu-id="241d0-767">fieldId</span><span class="sxs-lookup"><span data-stu-id="241d0-767">fieldId</span></span>  
<span data-ttu-id="241d0-768">セクション グループのフィールド (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d0-768">The field of the section group; optional.</span></span>

### <a name="return-value---sectiongroup"></a><span data-ttu-id="241d0-769">戻り値 - sectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-769">Return Value - sectionGroup</span></span>

<span data-ttu-id="241d0-770">引数に一致するセクション グループ。</span><span class="sxs-lookup"><span data-stu-id="241d0-770">The section group that matches the arguments.</span></span>

### <a name="examples---sectiongroup"></a><span data-ttu-id="241d0-771">例 - sectionGroup</span><span class="sxs-lookup"><span data-stu-id="241d0-771">Examples - sectionGroup</span></span>

<span data-ttu-id="241d0-772">次の例では、addSection メソッドで作成されたセクション グループを検索します。</span><span class="sxs-lookup"><span data-stu-id="241d0-772">The following example finds the section group that is created by the addSection method:</span></span>

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

## <a name="method-sectionname"></a><span data-ttu-id="241d0-773">メソッド sectionName</span><span class="sxs-lookup"><span data-stu-id="241d0-773">Method sectionName</span></span>

```xpp
public ReportSection sectionName(str name)
```

### <a name="parameters---sectionname"></a><span data-ttu-id="241d0-774">パラメーター - sectionName</span><span class="sxs-lookup"><span data-stu-id="241d0-774">Parameters - sectionName</span></span>

<span data-ttu-id="241d0-775">名前</span><span class="sxs-lookup"><span data-stu-id="241d0-775">name</span></span>  

### <a name="return-value---sectionname"></a><span data-ttu-id="241d0-776">戻り値 - sectionName</span><span class="sxs-lookup"><span data-stu-id="241d0-776">Return Value - sectionName</span></span>

## <a name="method-sectionnumber"></a><span data-ttu-id="241d0-777">メソッド sectionNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-777">Method sectionNumber</span></span>

```xpp
public ReportSection sectionNumber(int number)
```

### <a name="parameters---sectionnumber"></a><span data-ttu-id="241d0-778">パラメーター - sectionNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-778">Parameters - sectionNumber</span></span>

<span data-ttu-id="241d0-779">番号</span><span class="sxs-lookup"><span data-stu-id="241d0-779">number</span></span>  

### <a name="return-value---sectionnumber"></a><span data-ttu-id="241d0-780">戻り値 - sectionNumber</span><span class="sxs-lookup"><span data-stu-id="241d0-780">Return Value - sectionNumber</span></span>

## <a name="method-settarget"></a><span data-ttu-id="241d0-781">メソッド setTarget</span><span class="sxs-lookup"><span data-stu-id="241d0-781">Method setTarget</span></span>

<span data-ttu-id="241d0-782">レポートの印刷メディア ターゲットを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d0-782">Sets the print medium target for the report.</span></span>

```xpp
public PrintMedium setTarget(PrintMedium target)
```

### <a name="parameters---settarget"></a><span data-ttu-id="241d0-783">パラメーター - setTarget</span><span class="sxs-lookup"><span data-stu-id="241d0-783">Parameters - setTarget</span></span>

<span data-ttu-id="241d0-784">target</span><span class="sxs-lookup"><span data-stu-id="241d0-784">target</span></span>  
<span data-ttu-id="241d0-785">レポートの印刷メディア。</span><span class="sxs-lookup"><span data-stu-id="241d0-785">The print medium for the report.</span></span>

### <a name="return-value---settarget"></a><span data-ttu-id="241d0-786">戻り値 - setTarget</span><span class="sxs-lookup"><span data-stu-id="241d0-786">Return Value - setTarget</span></span>

<span data-ttu-id="241d0-787">レポートの印刷メディア。</span><span class="sxs-lookup"><span data-stu-id="241d0-787">The print medium for the report.</span></span>

### <a name="remarks---settarget"></a><span data-ttu-id="241d0-788">備考 - setTarget</span><span class="sxs-lookup"><span data-stu-id="241d0-788">Remarks - setTarget</span></span>

<span data-ttu-id="241d0-789">レポートの対象として特定のプリンターを選択するには、ReportDesign.printJobSettings メソッドによって返されるオブジェクトに対して PrintJobSettings.deviceName メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="241d0-789">To select a specific printer as the target for the report, call the PrintJobSettings.deviceName method on the object that is returned by the ReportDesign.printJobSettings method.</span></span>

## <a name="method-to"></a><span data-ttu-id="241d0-790">メソッド to</span><span class="sxs-lookup"><span data-stu-id="241d0-790">Method to</span></span>

```xpp
public int to([int toPage])
```

### <a name="parameters---to"></a><span data-ttu-id="241d0-791">パラメーター - to</span><span class="sxs-lookup"><span data-stu-id="241d0-791">Parameters - to</span></span>

<span data-ttu-id="241d0-792">toPage</span><span class="sxs-lookup"><span data-stu-id="241d0-792">toPage</span></span>  

### <a name="return-value---to"></a><span data-ttu-id="241d0-793">戻り値 - to</span><span class="sxs-lookup"><span data-stu-id="241d0-793">Return Value - to</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="241d0-794">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-794">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="241d0-795">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-795">Parameters - topMarginMode</span></span>

<span data-ttu-id="241d0-796">値</span><span class="sxs-lookup"><span data-stu-id="241d0-796">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="241d0-797">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="241d0-797">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="241d0-798">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-798">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="241d0-799">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-799">Parameters - topMarginStr</span></span>

<span data-ttu-id="241d0-800">値</span><span class="sxs-lookup"><span data-stu-id="241d0-800">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="241d0-801">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="241d0-801">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="241d0-802">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-802">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="241d0-803">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-803">Parameters - topMarginUnit</span></span>

<span data-ttu-id="241d0-804">値</span><span class="sxs-lookup"><span data-stu-id="241d0-804">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="241d0-805">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="241d0-805">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="241d0-806">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-806">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="241d0-807">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-807">Parameters - topMarginValue</span></span>

<span data-ttu-id="241d0-808">値</span><span class="sxs-lookup"><span data-stu-id="241d0-808">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="241d0-809">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="241d0-809">Return Value - topMarginValue</span></span>

## <a name="method-tostring"></a><span data-ttu-id="241d0-810">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="241d0-810">Method toString</span></span>

<span data-ttu-id="241d0-811">クラス ハンドルと名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="241d0-811">Returns a string that contains the class handle and name.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="241d0-812">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="241d0-812">Return Value - toString</span></span>

<span data-ttu-id="241d0-813">クラスのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="241d0-813">A textual description of the class.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="241d0-814">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="241d0-814">Remarks - toString</span></span>

<span data-ttu-id="241d0-815">一部のクラスでは、追加情報が文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="241d0-815">In some classes, additional information is returned in the string.</span></span>

## <a name="method-underline"></a><span data-ttu-id="241d0-816">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="241d0-816">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="241d0-817">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="241d0-817">Parameters - underline</span></span>

<span data-ttu-id="241d0-818">値</span><span class="sxs-lookup"><span data-stu-id="241d0-818">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="241d0-819">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="241d0-819">Return Value - underline</span></span>

## <a name="method-unpackpagesettings"></a><span data-ttu-id="241d0-820">メソッド unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-820">Method unpackPageSettings</span></span>

```xpp
public boolean unpackPageSettings(container packedPageSetup)
```

### <a name="parameters---unpackpagesettings"></a><span data-ttu-id="241d0-821">パラメーター - unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-821">Parameters - unpackPageSettings</span></span>

<span data-ttu-id="241d0-822">packedPageSetup</span><span class="sxs-lookup"><span data-stu-id="241d0-822">packedPageSetup</span></span>  

### <a name="return-value---unpackpagesettings"></a><span data-ttu-id="241d0-823">戻り値 - unpackPageSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-823">Return Value - unpackPageSettings</span></span>

## <a name="method-unpackprintersettings"></a><span data-ttu-id="241d0-824">メソッド unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-824">Method unpackPrinterSettings</span></span>

```xpp
public boolean unpackPrinterSettings(container packedPrintSetup)
```

### <a name="parameters---unpackprintersettings"></a><span data-ttu-id="241d0-825">パラメーター - unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-825">Parameters - unpackPrinterSettings</span></span>

<span data-ttu-id="241d0-826">packedPrintSetup</span><span class="sxs-lookup"><span data-stu-id="241d0-826">packedPrintSetup</span></span>  

### <a name="return-value---unpackprintersettings"></a><span data-ttu-id="241d0-827">戻り値 - unpackPrinterSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-827">Return Value - unpackPrinterSettings</span></span>

## <a name="method-unpackprintjobsettings"></a><span data-ttu-id="241d0-828">メソッド unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-828">Method unpackPrintJobSettings</span></span>

```xpp
public boolean unpackPrintJobSettings(container packedPrintJobSettings)
```

### <a name="parameters---unpackprintjobsettings"></a><span data-ttu-id="241d0-829">パラメーター - unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-829">Parameters - unpackPrintJobSettings</span></span>

<span data-ttu-id="241d0-830">packedPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-830">packedPrintJobSettings</span></span>  

### <a name="return-value---unpackprintjobsettings"></a><span data-ttu-id="241d0-831">戻り値 - unpackPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-831">Return Value - unpackPrintJobSettings</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="241d0-832">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-832">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="241d0-833">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-833">Parameters - leftMargin</span></span>

<span data-ttu-id="241d0-834">値</span><span class="sxs-lookup"><span data-stu-id="241d0-834">value</span></span>  

<!-- -->

<span data-ttu-id="241d0-835">単位</span><span class="sxs-lookup"><span data-stu-id="241d0-835">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="241d0-836">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-836">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="241d0-837">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-837">Parameters - bottomMargin</span></span>

<span data-ttu-id="241d0-838">値</span><span class="sxs-lookup"><span data-stu-id="241d0-838">value</span></span>  

<!-- -->

<span data-ttu-id="241d0-839">単位</span><span class="sxs-lookup"><span data-stu-id="241d0-839">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="241d0-840">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-840">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="241d0-841">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-841">Parameters - rightMargin</span></span>

<span data-ttu-id="241d0-842">値</span><span class="sxs-lookup"><span data-stu-id="241d0-842">value</span></span>  

<!-- -->

<span data-ttu-id="241d0-843">単位</span><span class="sxs-lookup"><span data-stu-id="241d0-843">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="241d0-844">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-844">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="241d0-845">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="241d0-845">Parameters - topMargin</span></span>

<span data-ttu-id="241d0-846">値</span><span class="sxs-lookup"><span data-stu-id="241d0-846">value</span></span>  

<!-- -->

<span data-ttu-id="241d0-847">単位</span><span class="sxs-lookup"><span data-stu-id="241d0-847">unit</span></span>  

## <a name="method-deletedisksettings"></a><span data-ttu-id="241d0-848">メソッド deleteDiskSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-848">Method deleteDiskSettings</span></span>

```xpp
public void deleteDiskSettings([boolean allUsers])
```

### <a name="parameters---deletedisksettings"></a><span data-ttu-id="241d0-849">パラメーター - deleteDiskSettings</span><span class="sxs-lookup"><span data-stu-id="241d0-849">Parameters - deleteDiskSettings</span></span>

<span data-ttu-id="241d0-850">allUsers</span><span class="sxs-lookup"><span data-stu-id="241d0-850">allUsers</span></span>  

