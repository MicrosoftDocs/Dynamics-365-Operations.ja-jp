---
title: ReportSection クラス
description: このトピックでは、ReportSection クラスについて説明します。
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
ms.openlocfilehash: 900c5a2782429a67fb585216b75a160fdcce1b03
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502831"
---
# <a name="class-reportsection"></a><span data-ttu-id="f4f1c-103">クラス ReportSection</span><span class="sxs-lookup"><span data-stu-id="f4f1c-103">Class ReportSection</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportSection extends TreeNode
```

<span data-ttu-id="f4f1c-104">ReportSection クラスには、レポート コントロールのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-104">The ReportSection class contains a collection of report controls.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f1c-105">備考</span><span class="sxs-lookup"><span data-stu-id="f4f1c-105">Remarks</span></span>

<span data-ttu-id="f4f1c-106">セクションは、レポートのクエリが実行されたとき、またはレポートのメソッドが実行されたときに、レポートに印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-106">A section is printed on the report when the query for the report is executed or when the methods of the report are executed.</span></span> <span data-ttu-id="f4f1c-107">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-107">This class lets you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="f4f1c-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="f4f1c-109">レポート セクションは、プロローグ、ページ ヘッダー、ヘッダー、フッター、ページ フッター、エピローグ、プログラム可能なセクション、ヘッダー、本文またはフッターのいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-109">A report section can be one of the following types: prologue, page header, header, footer, page footer, epilogue, programmable section, header, body, or footer.</span></span> <span data-ttu-id="f4f1c-110">セクション テンプレート ノード タイプを使用すると、セクションを一度定義して、さまざまなレポートで何度も再利用できます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-110">The section template node type lets you define sections one time and then reuse them many times in different reports.</span></span> <span data-ttu-id="f4f1c-111">この一般的な例は、小切手または振替です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-111">A typical example of this is a check or a giro.</span></span>

## <a name="examples"></a><span data-ttu-id="f4f1c-112">例</span><span class="sxs-lookup"><span data-stu-id="f4f1c-112">Examples</span></span>

<span data-ttu-id="f4f1c-113">次の例では、セクションをレポートに追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-113">The following example adds a section to a report:</span></span>

```xpp
static void test(args a) 
{  
    report r; 
    reportDesign rd; 
    reportSection rs; 
    reportRun rr; 
    // Create a simple report that is not present in  
    // the Application Object Tree. 
    r = new report(); 
    rd = r.addDesign("myDesign"); 
    rs = rd.addProgrammableSection(1);  
    // Add a section triggered by execute(1). 
    rs.addTextControl("Hello world"); 
    // Run the report. 
    rr = new reportRun(r); 
    if (rr.prompt()) // Run the sysPrintForm form. 
    { 
        rr.execute(1); // Execute the programmableSection. 
        rr.print();   // Print report to the target 
                      // (for example, printer or screen) 
                      // selected during the previous prompt call. 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="f4f1c-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="f4f1c-114">Methods</span></span>

| <span data-ttu-id="f4f1c-115">方法</span><span class="sxs-lookup"><span data-stu-id="f4f1c-115">Method</span></span>                                                                                       | <span data-ttu-id="f4f1c-116">説明</span><span class="sxs-lookup"><span data-stu-id="f4f1c-116">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f1c-117">public ReportBitmapControl addBitmapControl()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-117">public ReportBitmapControl addBitmapControl()</span></span>                                                | <span data-ttu-id="f4f1c-118">レポート セクションにビットマップ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-118">Adds a bitmap control to a report section.</span></span>                                                                                                |
| <span data-ttu-id="f4f1c-119">public ReportShapeControl addBoxControl(\[ShapeType type\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-119">public ReportShapeControl addBoxControl(\[ShapeType type\])</span></span>                                  | <span data-ttu-id="f4f1c-120">レポート セクションにシェイプ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-120">Adds a shape control to a report section.</span></span>                                                                                                 |
| <span data-ttu-id="f4f1c-121">public ReportControl addControl(TableId tableId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-121">public ReportControl addControl(TableId tableId, FieldId fieldId, \[int arrayIndex\])</span></span>        | <span data-ttu-id="f4f1c-122">レポート セクションにレポート コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-122">Adds a report control to a report section.</span></span>                                                                                                |
| <span data-ttu-id="f4f1c-123">public ReportDateControl addDateControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-123">public ReportDateControl addDateControl(TableId tableId, FieldId fieldId)</span></span>                    | <span data-ttu-id="f4f1c-124">レポート セクションにデータ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-124">Adds a date control to a report section.</span></span>                                                                                                  |
| <span data-ttu-id="f4f1c-125">public ReportDateControl addDateDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-125">public ReportDateControl addDateDisplayControl(str displayFunc, \[TableId tableId\])</span></span>         | <span data-ttu-id="f4f1c-126">レポート セクションにデータ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-126">Adds a date control to a report section.</span></span>                                                                                                  |
| <span data-ttu-id="f4f1c-127">public ReportDateTimeControl addDateTimeControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-127">public ReportDateTimeControl addDateTimeControl(TableId tableId, FieldId fieldId)</span></span>            |                                                                                                                                           |
| <span data-ttu-id="f4f1c-128">public ReportDateTimeControl addDateTimeDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-128">public ReportDateTimeControl addDateTimeDisplayControl(str displayFunc, \[TableId tableId\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="f4f1c-129">public ReportControl addDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-129">public ReportControl addDisplayControl(str displayFunc, \[TableId tableId\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-130">public ReportEnumControl addEnumControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-130">public ReportEnumControl addEnumControl(TableId tableId, FieldId fieldId)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-131">public ReportEnumControl addEnumDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-131">public ReportEnumControl addEnumDisplayControl(str displayFunc, \[TableId tableId\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-132">public ReportFieldGroup addFieldGroup(TableId tableId, str name)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-132">public ReportFieldGroup addFieldGroup(TableId tableId, str name)</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="f4f1c-133">public ReportGuidControl addGuidControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-133">public ReportGuidControl addGuidControl(TableId tableId, FieldId fieldId)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-134">public ReportGuidControl addGuidDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-134">public ReportGuidControl addGuidDisplayControl(str displayFunc, \[TableId tableId\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-135">public ReportInt64Control addInt64Control(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-135">public ReportInt64Control addInt64Control(TableId tableId, FieldId fieldId)</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="f4f1c-136">public ReportInt64Control addInt64DisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-136">public ReportInt64Control addInt64DisplayControl(str displayFunc, \[TableId tableId\])</span></span>       |                                                                                                                                           |
| <span data-ttu-id="f4f1c-137">public ReportIntegerControl addIntegerControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-137">public ReportIntegerControl addIntegerControl(TableId tableId, FieldId fieldId)</span></span>              |                                                                                                                                           |
| <span data-ttu-id="f4f1c-138">public ReportIntegerControl addIntegerDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-138">public ReportIntegerControl addIntegerDisplayControl(str displayFunc, \[TableId tableId\])</span></span>   |                                                                                                                                           |
| <span data-ttu-id="f4f1c-139">public ReportPromptControl addPromptControl(TableId tableId, \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-139">public ReportPromptControl addPromptControl(TableId tableId, \[FieldId fieldId\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="f4f1c-140">public ReportRealControl addRealControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-140">public ReportRealControl addRealControl(TableId tableId, FieldId fieldId)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-141">public ReportRealControl addRealDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-141">public ReportRealControl addRealDisplayControl(str displayFunc, \[TableId tableId\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-142">public ReportSectionGroup addSection(TableId tableId, \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-142">public ReportSectionGroup addSection(TableId tableId, \[FieldId fieldId\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="f4f1c-143">public ReportShapeControl addShapeControl(\[ShapeType type\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-143">public ReportShapeControl addShapeControl(\[ShapeType type\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-144">public ReportStringControl addStringControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-144">public ReportStringControl addStringControl(TableId tableId, FieldId fieldId)</span></span>                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-145">public ReportStringControl addStringDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-145">public ReportStringControl addStringDisplayControl(str displayFunc, \[TableId tableId\])</span></span>     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-146">public ReportSumControl addSumControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-146">public ReportSumControl addSumControl(TableId tableId, FieldId fieldId)</span></span>                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-147">public ReportSumControl addSumNameControl(str name)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-147">public ReportSumControl addSumNameControl(str name)</span></span>                                          |                                                                                                                                           |
| <span data-ttu-id="f4f1c-148">public ReportTextControl addTextControl(str text)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-148">public ReportTextControl addTextControl(str text)</span></span>                                            |                                                                                                                                           |
| <span data-ttu-id="f4f1c-149">public ReportTimeControl addTimeControl(TableId tableId, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-149">public ReportTimeControl addTimeControl(TableId tableId, FieldId fieldId)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-150">public ReportTimeControl addTimeDisplayControl(str displayFunc, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-150">public ReportTimeControl addTimeDisplayControl(str displayFunc, \[TableId tableId\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-151">public int arrange()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-151">public int arrange()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-152">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-152">public int arrangeMethod(\[int value\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-153">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-153">public int arrangeWhen(\[int value\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="f4f1c-154">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-154">public boolean autoDeclaration(\[boolean value\])</span></span>                                            | <span data-ttu-id="f4f1c-155">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-155">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="f4f1c-156">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-156">public boolean autoHeader(\[boolean value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-157">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-157">public int bold(\[int value\])</span></span>                                                               | <span data-ttu-id="f4f1c-158">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-158">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="f4f1c-159">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-159">public int bottomMarginAndFrame()</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="f4f1c-160">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-160">public int bottomMarginMode(\[int value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="f4f1c-161">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-161">public str bottomMarginStr(\[str value\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-162">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-162">public Units bottomMarginUnit(\[Units value\])</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="f4f1c-163">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-163">public Real bottomMarginValue(\[Real value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-164">public int bottomMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-164">public int bottomMode(\[int value\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-165">public str bottomStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-165">public str bottomStr(\[str value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="f4f1c-166">public Units bottomUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-166">public Units bottomUnit(\[Units value\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-167">public Real bottomValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-167">public Real bottomValue(\[Real value\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-168">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-168">public int characterSet(\[int value\])</span></span>                                                       | <span data-ttu-id="f4f1c-169">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-169">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="f4f1c-170">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-170">public int colorScheme(\[int value\])</span></span>                                                        | <span data-ttu-id="f4f1c-171">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-171">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="f4f1c-172">public int columnHeadingsStrategy(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-172">public int columnHeadingsStrategy(\[int value\])</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="f4f1c-173">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-173">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-174">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-174">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-175">public int columnspaceMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-175">public int columnspaceMode(\[int value\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-176">public str columnspaceStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-176">public str columnspaceStr(\[str value\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-177">public Units columnspaceUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-177">public Units columnspaceUnit(\[Units value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-178">public Real columnspaceValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-178">public Real columnspaceValue(\[Real value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-179">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-179">public int columnsValue(\[int value\])</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="f4f1c-180">public ReportControl control(FieldId fieldId, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-180">public ReportControl control(FieldId fieldId, \[TableId tableId\])</span></span>                           | <span data-ttu-id="f4f1c-181">コントロールのテーブルおよび dataField プロパティに基づいて、セクションのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-181">Finds a control in the section, based on the control�s table and dataField properties.</span></span>                                                    |
| <span data-ttu-id="f4f1c-182">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-182">public int controlCount()</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-183">public ReportControl controlName(str name)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-183">public ReportControl controlName(str name)</span></span>                                                   | <span data-ttu-id="f4f1c-184">コントロールの Name プロパティに基づいて、セクションのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-184">Finds a control in a section, based on the control's Name property.</span></span>                                                                       |
| <span data-ttu-id="f4f1c-185">public ReportControl controlNo(int number)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-185">public ReportControl controlNo(int number)</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="f4f1c-186">public int controlNumber(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-186">public int controlNumber(\[int value\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-187">public int delete()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-187">public int delete()</span></span>                                                                          | <span data-ttu-id="f4f1c-188">現在のノードを AOT から削除します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-188">Deletes the current node from the AOT.</span></span>                                                                                                    |
| <span data-ttu-id="f4f1c-189">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-189">public str font(\[str value\])</span></span>                                                               | <span data-ttu-id="f4f1c-190">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-190">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="f4f1c-191">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-191">public int fontSize(\[int value\])</span></span>                                                           | <span data-ttu-id="f4f1c-192">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-192">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="f4f1c-193">public str footerText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-193">public str footerText(\[str value\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-194">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-194">public int foregroundColor(\[int value\])</span></span>                                                    | <span data-ttu-id="f4f1c-195">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-195">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="f4f1c-196">public boolean grandHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-196">public boolean grandHeader(\[boolean value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-197">public boolean grandTotal(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-197">public boolean grandTotal(\[boolean value\])</span></span>                                                 | <span data-ttu-id="f4f1c-198">FooterText プロパティ値が表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-198">Determines whether the FooterText property value can be displayed.</span></span>                                                                        |
| <span data-ttu-id="f4f1c-199">public boolean hasButtons(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-199">public boolean hasButtons(\[boolean value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-200">public int headerDetailLevel(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-200">public int headerDetailLevel(\[int value\], \[AutoMode mode\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="f4f1c-201">public AutoMode headerDetailLevelMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-201">public AutoMode headerDetailLevelMode(\[AutoMode mode\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-202">public int headerDetailLevelValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-202">public int headerDetailLevelValue(\[int value\])</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="f4f1c-203">public str headerText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-203">public str headerText(\[str value\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-204">public int height100mm(\[int height\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-204">public int height100mm(\[int height\])</span></span>                                                       | <span data-ttu-id="f4f1c-205">枠線および上下の余白の高さを除く、セクションの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-205">Gets or sets the height of a section, excluding the height of the border and the top and bottom margins.</span></span>                                  |
| <span data-ttu-id="f4f1c-206">public int heightmm100(\[int heightInclMargins\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-206">public int heightmm100(\[int heightInclMargins\])</span></span>                                            | <span data-ttu-id="f4f1c-207">枠線および上下の余白の高さを含む、セクションの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-207">Gets or sets the height of a section, including the height of the border and the top and bottom margins.</span></span>                                  |
| <span data-ttu-id="f4f1c-208">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-208">public int heightMode(\[int value\])</span></span>                                                         | <span data-ttu-id="f4f1c-209">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-209">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="f4f1c-210">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-210">public str heightStr(\[str value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="f4f1c-211">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-211">public Units heightUnit(\[Units value\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-212">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-212">public Real heightValue(\[Real value\])</span></span>                                                      | <span data-ttu-id="f4f1c-213">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-213">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="f4f1c-214">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-214">public boolean italic(\[boolean value\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-215">public str label()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-215">public str label()</span></span>                                                                           | <span data-ttu-id="f4f1c-216">AOT 内のセクション ノードの説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-216">Gets the description of the section node in the AOT.</span></span>                                                                                      |
| <span data-ttu-id="f4f1c-217">public int labelBottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-217">public int labelBottomMarginMode(\[int value\])</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="f4f1c-218">public str labelBottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-218">public str labelBottomMarginStr(\[str value\])</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="f4f1c-219">public Units labelBottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-219">public Units labelBottomMarginUnit(\[Units value\])</span></span>                                          |                                                                                                                                           |
| <span data-ttu-id="f4f1c-220">public Real labelBottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-220">public Real labelBottomMarginValue(\[Real value\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="f4f1c-221">public int labelTopMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-221">public int labelTopMarginMode(\[int value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-222">public str labelTopMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-222">public str labelTopMarginStr(\[str value\])</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="f4f1c-223">public Units labelTopMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-223">public Units labelTopMarginUnit(\[Units value\])</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="f4f1c-224">public Real labelTopMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-224">public Real labelTopMarginValue(\[Real value\])</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="f4f1c-225">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-225">public int leftMarginMode(\[int value\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-226">public int leftMarginsEtc()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-226">public int leftMarginsEtc()</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="f4f1c-227">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-227">public str leftMarginStr(\[str value\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-228">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-228">public Units leftMarginUnit(\[Units value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-229">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-229">public Real leftMarginValue(\[Real value\])</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="f4f1c-230">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-230">public LineType lineAbove(\[LineType value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-231">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-231">public LineType lineBelow(\[LineType value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-232">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-232">public LineType lineLeft(\[LineType value\])</span></span>                                                 | <span data-ttu-id="f4f1c-233">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-233">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="f4f1c-234">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-234">public LineType lineRight(\[LineType value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-235">public TableId map(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-235">public TableId map(\[TableId value\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="f4f1c-236">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-236">public str name(\[str value\])</span></span>                                                               | <span data-ttu-id="f4f1c-237">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-237">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="f4f1c-238">public int noOfHeadingLines(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-238">public int noOfHeadingLines(\[int value\], \[AutoMode mode\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-239">public AutoMode noOfHeadingLinesMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-239">public AutoMode noOfHeadingLinesMode(\[AutoMode mode\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-240">public int noOfHeadingLinesValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-240">public int noOfHeadingLinesValue(\[int value\])</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="f4f1c-241">public str resolutionX(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-241">public str resolutionX(\[str value\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="f4f1c-242">public int resolutionXStr(str value)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-242">public int resolutionXStr(str value)</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-243">public Units resolutionXUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-243">public Units resolutionXUnit(\[Units value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-244">public str resolutionY(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-244">public str resolutionY(\[str value\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="f4f1c-245">public int resolutionYStr(str value)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-245">public int resolutionYStr(str value)</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-246">public Units resolutionYUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-246">public Units resolutionYUnit(\[Units value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-247">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-247">public int rightMarginMode(\[int value\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="f4f1c-248">public int rightMarginsEtc()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-248">public int rightMarginsEtc()</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-249">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-249">public str rightMarginStr(\[str value\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="f4f1c-250">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-250">public Units rightMarginUnit(\[Units value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-251">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-251">public Real rightMarginValue(\[Real value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="f4f1c-252">public int ruler(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-252">public int ruler(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="f4f1c-253">public ReportSectionGroup sectionGroup(TableId tableId, \[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-253">public ReportSectionGroup sectionGroup(TableId tableId, \[FieldId fieldId\])</span></span>                 | <span data-ttu-id="f4f1c-254">生成されたデザインで、既存のセクション グループを検索します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-254">Finds an existing section group in the generated design.</span></span>                                                                                  |
| <span data-ttu-id="f4f1c-255">public ReportBlockType sectionType()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-255">public ReportBlockType sectionType()</span></span>                                                         | <span data-ttu-id="f4f1c-256">ReportBlockType::Prolog、ReportBlockType::PageHeader、ReportBlockType::Body などの特定のレポート セクションのタイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-256">Retrieves the type of a given report section, such as ReportBlockType::Prolog, ReportBlockType::PageHeader, or ReportBlockType::Body.</span></span>     |
| <span data-ttu-id="f4f1c-257">public int sumDetailLevel(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-257">public int sumDetailLevel(\[int value\], \[AutoMode mode\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f4f1c-258">public AutoMode sumDetailLevelMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-258">public AutoMode sumDetailLevelMode(\[AutoMode mode\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f4f1c-259">public int sumDetailLevelValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-259">public int sumDetailLevelValue(\[int value\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-260">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-260">public TableId table(\[TableId value\])</span></span>                                                      | <span data-ttu-id="f4f1c-261">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-261">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="f4f1c-262">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-262">public LineThickness thickness(\[LineThickness value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-263">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-263">public int topMarginAndFrame()</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="f4f1c-264">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-264">public int topMarginMode(\[int value\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-265">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-265">public str topMarginStr(\[str value\])</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="f4f1c-266">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-266">public Units topMarginUnit(\[Units value\])</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="f4f1c-267">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-267">public Real topMarginValue(\[Real value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="f4f1c-268">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-268">public int topMode(\[int value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="f4f1c-269">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-269">public str topStr(\[str value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="f4f1c-270">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-270">public Units topUnit(\[Units value\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="f4f1c-271">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-271">public Real topValue(\[Real value\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="f4f1c-272">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f4f1c-272">public boolean underline(\[boolean value\])</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="f4f1c-273">public void columnspace(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-273">public void columnspace(Real value, Units unit)</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="f4f1c-274">public void bottom(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-274">public void bottom(Real value, Units unit)</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="f4f1c-275">public void labelBottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-275">public void labelBottomMargin(Real value, Units unit)</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f4f1c-276">public void labelTopMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-276">public void labelTopMargin(Real value, Units unit)</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="f4f1c-277">public void executeColumnHeadings()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-277">public void executeColumnHeadings()</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="f4f1c-278">public void executeSection()</span><span class="sxs-lookup"><span data-stu-id="f4f1c-278">public void executeSection()</span></span>                                                                 | <span data-ttu-id="f4f1c-279">レポートにセクションを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-279">Prints the section on the report.</span></span>                                                                                                         |
| <span data-ttu-id="f4f1c-280">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-280">public void rightMargin(Real value, Units unit)</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="f4f1c-281">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-281">public void bottomMargin(Real value, Units unit)</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="f4f1c-282">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-282">public void topMargin(Real value, Units unit)</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="f4f1c-283">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-283">public void leftMargin(Real value, Units unit)</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="f4f1c-284">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-284">public void top(Real value, Units unit)</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="f4f1c-285">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f4f1c-285">public void height(Real value, Units unit)</span></span>                                                   | <span data-ttu-id="f4f1c-286">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-286">Gets or sets the height of the control.</span></span>                                                                                                   |

## <a name="method-addbitmapcontrol"></a><span data-ttu-id="f4f1c-287">メソッド addBitmapControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-287">Method addBitmapControl</span></span>

<span data-ttu-id="f4f1c-288">レポート セクションにビットマップ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-288">Adds a bitmap control to a report section.</span></span>

```xpp
public ReportBitmapControl addBitmapControl()
```

### <a name="return-value---addbitmapcontrol"></a><span data-ttu-id="f4f1c-289">戻り値 - addBitmapControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-289">Return Value - addBitmapControl</span></span>

<span data-ttu-id="f4f1c-290">ビットマップ コントロールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-290">The bitmap control that is created.</span></span>

## <a name="method-addboxcontrol"></a><span data-ttu-id="f4f1c-291">メソッド addBoxControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-291">Method addBoxControl</span></span>

<span data-ttu-id="f4f1c-292">レポート セクションにシェイプ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-292">Adds a shape control to a report section.</span></span>

```xpp
public ReportShapeControl addBoxControl([ShapeType type])
```

### <a name="parameters---addboxcontrol"></a><span data-ttu-id="f4f1c-293">パラメーター - addBoxControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-293">Parameters - addBoxControl</span></span>

<span data-ttu-id="f4f1c-294">タイプ</span><span class="sxs-lookup"><span data-stu-id="f4f1c-294">type</span></span>  
<span data-ttu-id="f4f1c-295">追加するシェイプコントロールのタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-295">The type of shape control to add; optional.</span></span>

### <a name="return-value---addboxcontrol"></a><span data-ttu-id="f4f1c-296">戻り値 - addBoxControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-296">Return Value - addBoxControl</span></span>

<span data-ttu-id="f4f1c-297">作成されるシェイプ コントロール。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-297">The shape control that is created.</span></span>

## <a name="method-addcontrol"></a><span data-ttu-id="f4f1c-298">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-298">Method addControl</span></span>

<span data-ttu-id="f4f1c-299">レポート セクションにレポート コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-299">Adds a report control to a report section.</span></span>

```xpp
public ReportControl addControl(TableId tableId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="f4f1c-300">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-300">Parameters - addControl</span></span>

<span data-ttu-id="f4f1c-301">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-301">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-302">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-302">fieldId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-303">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="f4f1c-303">arrayIndex</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="f4f1c-304">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-304">Return Value - addControl</span></span>

<span data-ttu-id="f4f1c-305">作成されるレポート コントロール。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-305">The report control that is created.</span></span>

### <a name="remarks---addcontrol"></a><span data-ttu-id="f4f1c-306">備考 - addControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-306">Remarks - addControl</span></span>

<span data-ttu-id="f4f1c-307">このメソッドは、引数で指定されたフィールドの型に応じて、文字列、列挙、整数、実数、日付など、指定したコントロールの種類を追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-307">This method adds the specified type of control, such as string, enumeration, integer, real, or date, depending on the type of the field that is specified by the arguments.</span></span>

## <a name="method-adddatecontrol"></a><span data-ttu-id="f4f1c-308">メソッド addDateControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-308">Method addDateControl</span></span>

<span data-ttu-id="f4f1c-309">レポート セクションにデータ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-309">Adds a date control to a report section.</span></span>

```xpp
public ReportDateControl addDateControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---adddatecontrol"></a><span data-ttu-id="f4f1c-310">パラメーター - addDateControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-310">Parameters - addDateControl</span></span>

<span data-ttu-id="f4f1c-311">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-311">tableId</span></span>  
<span data-ttu-id="f4f1c-312">フィールド ID。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-312">The field ID.</span></span>

<!-- -->

<span data-ttu-id="f4f1c-313">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-313">fieldId</span></span>  
<span data-ttu-id="f4f1c-314">フィールド ID。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-314">The field ID.</span></span>

### <a name="return-value---adddatecontrol"></a><span data-ttu-id="f4f1c-315">戻り値 - addDateControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-315">Return Value - addDateControl</span></span>

<span data-ttu-id="f4f1c-316">日付コントロールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-316">The date control that is created.</span></span>

### <a name="examples---adddatecontrol"></a><span data-ttu-id="f4f1c-317">例 - addDateControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-317">Examples - addDateControl</span></span>

```xpp
static void test(args a) 
{ 
    reportRun rr; 
    inventTrans rec; 
    int i; 
    // Create a simple report that is not present in 
    // the Application Object Tree. 
    report r = new report(); 
    reportDesign rd = r.addDesign("myDesign"); 
    reportSection rs = rd.AddSection(reportBlockType::body,  
    tablenum(inventTrans)); 
    int t = tablenum(inventTrans); 
    int f; 
    f = fieldnum(inventTrans, datePhysical); 
    rs.addDateControl(t,f); 
    // run the report 
    rr = new reportRun(r); 
    // Run the sysPrintForm form. 
    if (rr.prompt())  
    { 
        while select rec 
            rr.send(rec); 
        // Print report to the target (e.g. printer or screen) selected during the  
        // prompt call above. 
        rr.print();  
    } 
}
```

## <a name="method-adddatedisplaycontrol"></a><span data-ttu-id="f4f1c-318">メソッド addDateDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-318">Method addDateDisplayControl</span></span>

<span data-ttu-id="f4f1c-319">レポート セクションにデータ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-319">Adds a date control to a report section.</span></span>

```xpp
public ReportDateControl addDateDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---adddatedisplaycontrol"></a><span data-ttu-id="f4f1c-320">パラメーター - addDateDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-320">Parameters - addDateDisplayControl</span></span>

<span data-ttu-id="f4f1c-321">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-321">displayFunc</span></span>  
<span data-ttu-id="f4f1c-322">表示メソッドが宣言されているテーブルの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-322">The name of the table on which the display method is declared; optional.</span></span>

<!-- -->

<span data-ttu-id="f4f1c-323">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-323">tableId</span></span>  
<span data-ttu-id="f4f1c-324">表示メソッドが宣言されているテーブルの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-324">The name of the table on which the display method is declared; optional.</span></span>

### <a name="return-value---adddatedisplaycontrol"></a><span data-ttu-id="f4f1c-325">戻り値 - addDateDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-325">Return Value - addDateDisplayControl</span></span>

<span data-ttu-id="f4f1c-326">日付コントロールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-326">The date control that is created.</span></span>

### <a name="remarks---adddatedisplaycontrol"></a><span data-ttu-id="f4f1c-327">備考 - addDateDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-327">Remarks - addDateDisplayControl</span></span>

<span data-ttu-id="f4f1c-328">データ コントロールは、表示メソッドが日付を返すときの結果を示します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-328">The data control shows the result when a display method returns a date.</span></span>

## <a name="method-adddatetimecontrol"></a><span data-ttu-id="f4f1c-329">メソッド addDateTimeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-329">Method addDateTimeControl</span></span>

```xpp
public ReportDateTimeControl addDateTimeControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---adddatetimecontrol"></a><span data-ttu-id="f4f1c-330">パラメーター - addDateTimeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-330">Parameters - addDateTimeControl</span></span>

<span data-ttu-id="f4f1c-331">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-331">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-332">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-332">fieldId</span></span>  

### <a name="return-value---adddatetimecontrol"></a><span data-ttu-id="f4f1c-333">戻り値 - addDateTimeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-333">Return Value - addDateTimeControl</span></span>

## <a name="method-adddatetimedisplaycontrol"></a><span data-ttu-id="f4f1c-334">メソッド addDateTimeDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-334">Method addDateTimeDisplayControl</span></span>

```xpp
public ReportDateTimeControl addDateTimeDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---adddatetimedisplaycontrol"></a><span data-ttu-id="f4f1c-335">パラメーター - addDateTimeDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-335">Parameters - addDateTimeDisplayControl</span></span>

<span data-ttu-id="f4f1c-336">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-336">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-337">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-337">tableId</span></span>  

### <a name="return-value---adddatetimedisplaycontrol"></a><span data-ttu-id="f4f1c-338">戻り値 - addDateTimeDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-338">Return Value - addDateTimeDisplayControl</span></span>

## <a name="method-adddisplaycontrol"></a><span data-ttu-id="f4f1c-339">メソッド addDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-339">Method addDisplayControl</span></span>

```xpp
public ReportControl addDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---adddisplaycontrol"></a><span data-ttu-id="f4f1c-340">パラメーター - addDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-340">Parameters - addDisplayControl</span></span>

<span data-ttu-id="f4f1c-341">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-341">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-342">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-342">tableId</span></span>  

### <a name="return-value---adddisplaycontrol"></a><span data-ttu-id="f4f1c-343">戻り値 - addDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-343">Return Value - addDisplayControl</span></span>

## <a name="method-addenumcontrol"></a><span data-ttu-id="f4f1c-344">メソッド addEnumControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-344">Method addEnumControl</span></span>

```xpp
public ReportEnumControl addEnumControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addenumcontrol"></a><span data-ttu-id="f4f1c-345">パラメーター - addEnumControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-345">Parameters - addEnumControl</span></span>

<span data-ttu-id="f4f1c-346">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-346">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-347">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-347">fieldId</span></span>  

### <a name="return-value---addenumcontrol"></a><span data-ttu-id="f4f1c-348">戻り値 - addEnumControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-348">Return Value - addEnumControl</span></span>

## <a name="method-addenumdisplaycontrol"></a><span data-ttu-id="f4f1c-349">メソッド addEnumDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-349">Method addEnumDisplayControl</span></span>

```xpp
public ReportEnumControl addEnumDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addenumdisplaycontrol"></a><span data-ttu-id="f4f1c-350">パラメーター - addEnumDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-350">Parameters - addEnumDisplayControl</span></span>

<span data-ttu-id="f4f1c-351">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-351">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-352">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-352">tableId</span></span>  

### <a name="return-value---addenumdisplaycontrol"></a><span data-ttu-id="f4f1c-353">戻り値 - addEnumDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-353">Return Value - addEnumDisplayControl</span></span>

## <a name="method-addfieldgroup"></a><span data-ttu-id="f4f1c-354">メソッド addFieldGroup</span><span class="sxs-lookup"><span data-stu-id="f4f1c-354">Method addFieldGroup</span></span>

```xpp
public ReportFieldGroup addFieldGroup(TableId tableId, str name)
```

### <a name="parameters---addfieldgroup"></a><span data-ttu-id="f4f1c-355">パラメーター - addFieldGroup</span><span class="sxs-lookup"><span data-stu-id="f4f1c-355">Parameters - addFieldGroup</span></span>

<span data-ttu-id="f4f1c-356">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-356">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-357">名前</span><span class="sxs-lookup"><span data-stu-id="f4f1c-357">name</span></span>  

### <a name="return-value---addfieldgroup"></a><span data-ttu-id="f4f1c-358">戻り値 - addFieldGroup</span><span class="sxs-lookup"><span data-stu-id="f4f1c-358">Return Value - addFieldGroup</span></span>

## <a name="method-addguidcontrol"></a><span data-ttu-id="f4f1c-359">メソッド addGuidControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-359">Method addGuidControl</span></span>

```xpp
public ReportGuidControl addGuidControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addguidcontrol"></a><span data-ttu-id="f4f1c-360">パラメーター - addGuidControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-360">Parameters - addGuidControl</span></span>

<span data-ttu-id="f4f1c-361">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-361">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-362">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-362">fieldId</span></span>  

### <a name="return-value---addguidcontrol"></a><span data-ttu-id="f4f1c-363">戻り値 - addGuidControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-363">Return Value - addGuidControl</span></span>

## <a name="method-addguiddisplaycontrol"></a><span data-ttu-id="f4f1c-364">メソッド addGuidDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-364">Method addGuidDisplayControl</span></span>

```xpp
public ReportGuidControl addGuidDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addguiddisplaycontrol"></a><span data-ttu-id="f4f1c-365">パラメーター - addGuidDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-365">Parameters - addGuidDisplayControl</span></span>

<span data-ttu-id="f4f1c-366">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-366">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-367">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-367">tableId</span></span>  

### <a name="return-value---addguiddisplaycontrol"></a><span data-ttu-id="f4f1c-368">戻り値 - addGuidDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-368">Return Value - addGuidDisplayControl</span></span>

## <a name="method-addint64control"></a><span data-ttu-id="f4f1c-369">メソッド addInt64Control</span><span class="sxs-lookup"><span data-stu-id="f4f1c-369">Method addInt64Control</span></span>

```xpp
public ReportInt64Control addInt64Control(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addint64control"></a><span data-ttu-id="f4f1c-370">パラメーター - addInt64Control</span><span class="sxs-lookup"><span data-stu-id="f4f1c-370">Parameters - addInt64Control</span></span>

<span data-ttu-id="f4f1c-371">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-371">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-372">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-372">fieldId</span></span>  

### <a name="return-value---addint64control"></a><span data-ttu-id="f4f1c-373">戻り値 - addInt64Control</span><span class="sxs-lookup"><span data-stu-id="f4f1c-373">Return Value - addInt64Control</span></span>

## <a name="method-addint64displaycontrol"></a><span data-ttu-id="f4f1c-374">メソッド addInt64DisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-374">Method addInt64DisplayControl</span></span>

```xpp
public ReportInt64Control addInt64DisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addint64displaycontrol"></a><span data-ttu-id="f4f1c-375">パラメーター - addInt64DisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-375">Parameters - addInt64DisplayControl</span></span>

<span data-ttu-id="f4f1c-376">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-376">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-377">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-377">tableId</span></span>  

### <a name="return-value---addint64displaycontrol"></a><span data-ttu-id="f4f1c-378">戻り値 - addInt64DisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-378">Return Value - addInt64DisplayControl</span></span>

## <a name="method-addintegercontrol"></a><span data-ttu-id="f4f1c-379">メソッド addIntegerControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-379">Method addIntegerControl</span></span>

```xpp
public ReportIntegerControl addIntegerControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addintegercontrol"></a><span data-ttu-id="f4f1c-380">パラメーター - addIntegerControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-380">Parameters - addIntegerControl</span></span>

<span data-ttu-id="f4f1c-381">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-381">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-382">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-382">fieldId</span></span>  

### <a name="return-value---addintegercontrol"></a><span data-ttu-id="f4f1c-383">戻り値 - addIntegerControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-383">Return Value - addIntegerControl</span></span>

## <a name="method-addintegerdisplaycontrol"></a><span data-ttu-id="f4f1c-384">メソッド addIntegerDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-384">Method addIntegerDisplayControl</span></span>

```xpp
public ReportIntegerControl addIntegerDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addintegerdisplaycontrol"></a><span data-ttu-id="f4f1c-385">パラメーター - addIntegerDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-385">Parameters - addIntegerDisplayControl</span></span>

<span data-ttu-id="f4f1c-386">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-386">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-387">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-387">tableId</span></span>  

### <a name="return-value---addintegerdisplaycontrol"></a><span data-ttu-id="f4f1c-388">戻り値 - addIntegerDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-388">Return Value - addIntegerDisplayControl</span></span>

## <a name="method-addpromptcontrol"></a><span data-ttu-id="f4f1c-389">メソッド addPromptControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-389">Method addPromptControl</span></span>

```xpp
public ReportPromptControl addPromptControl(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---addpromptcontrol"></a><span data-ttu-id="f4f1c-390">パラメーター - addPromptControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-390">Parameters - addPromptControl</span></span>

<span data-ttu-id="f4f1c-391">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-391">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-392">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-392">fieldId</span></span>  

### <a name="return-value---addpromptcontrol"></a><span data-ttu-id="f4f1c-393">戻り値 - addPromptControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-393">Return Value - addPromptControl</span></span>

## <a name="method-addrealcontrol"></a><span data-ttu-id="f4f1c-394">メソッド addRealControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-394">Method addRealControl</span></span>

```xpp
public ReportRealControl addRealControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addrealcontrol"></a><span data-ttu-id="f4f1c-395">パラメーター - addRealControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-395">Parameters - addRealControl</span></span>

<span data-ttu-id="f4f1c-396">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-396">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-397">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-397">fieldId</span></span>  

### <a name="return-value---addrealcontrol"></a><span data-ttu-id="f4f1c-398">戻り値 - addRealControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-398">Return Value - addRealControl</span></span>

## <a name="method-addrealdisplaycontrol"></a><span data-ttu-id="f4f1c-399">メソッド addRealDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-399">Method addRealDisplayControl</span></span>

```xpp
public ReportRealControl addRealDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addrealdisplaycontrol"></a><span data-ttu-id="f4f1c-400">パラメーター - addRealDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-400">Parameters - addRealDisplayControl</span></span>

<span data-ttu-id="f4f1c-401">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-401">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-402">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-402">tableId</span></span>  

### <a name="return-value---addrealdisplaycontrol"></a><span data-ttu-id="f4f1c-403">戻り値 - addRealDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-403">Return Value - addRealDisplayControl</span></span>

## <a name="method-addsection"></a><span data-ttu-id="f4f1c-404">メソッド addSection</span><span class="sxs-lookup"><span data-stu-id="f4f1c-404">Method addSection</span></span>

```xpp
public ReportSectionGroup addSection(TableId tableId, [FieldId fieldId])
```

### <a name="parameters---addsection"></a><span data-ttu-id="f4f1c-405">パラメーター - addSection</span><span class="sxs-lookup"><span data-stu-id="f4f1c-405">Parameters - addSection</span></span>

<span data-ttu-id="f4f1c-406">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-406">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-407">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-407">fieldId</span></span>  

### <a name="return-value---addsection"></a><span data-ttu-id="f4f1c-408">戻り値 - addSection</span><span class="sxs-lookup"><span data-stu-id="f4f1c-408">Return Value - addSection</span></span>

## <a name="method-addshapecontrol"></a><span data-ttu-id="f4f1c-409">メソッド addShapeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-409">Method addShapeControl</span></span>

```xpp
public ReportShapeControl addShapeControl([ShapeType type])
```

### <a name="parameters---addshapecontrol"></a><span data-ttu-id="f4f1c-410">パラメーター - addShapeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-410">Parameters - addShapeControl</span></span>

<span data-ttu-id="f4f1c-411">タイプ</span><span class="sxs-lookup"><span data-stu-id="f4f1c-411">type</span></span>  

### <a name="return-value---addshapecontrol"></a><span data-ttu-id="f4f1c-412">戻り値 - addShapeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-412">Return Value - addShapeControl</span></span>

## <a name="method-addstringcontrol"></a><span data-ttu-id="f4f1c-413">メソッド addStringControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-413">Method addStringControl</span></span>

```xpp
public ReportStringControl addStringControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addstringcontrol"></a><span data-ttu-id="f4f1c-414">パラメーター - addStringControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-414">Parameters - addStringControl</span></span>

<span data-ttu-id="f4f1c-415">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-415">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-416">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-416">fieldId</span></span>  

### <a name="return-value---addstringcontrol"></a><span data-ttu-id="f4f1c-417">戻り値 - addStringControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-417">Return Value - addStringControl</span></span>

## <a name="method-addstringdisplaycontrol"></a><span data-ttu-id="f4f1c-418">メソッド addStringDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-418">Method addStringDisplayControl</span></span>

```xpp
public ReportStringControl addStringDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addstringdisplaycontrol"></a><span data-ttu-id="f4f1c-419">パラメーター - addStringDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-419">Parameters - addStringDisplayControl</span></span>

<span data-ttu-id="f4f1c-420">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-420">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-421">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-421">tableId</span></span>  

### <a name="return-value---addstringdisplaycontrol"></a><span data-ttu-id="f4f1c-422">戻り値 - addStringDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-422">Return Value - addStringDisplayControl</span></span>

## <a name="method-addsumcontrol"></a><span data-ttu-id="f4f1c-423">メソッド addSumControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-423">Method addSumControl</span></span>

```xpp
public ReportSumControl addSumControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addsumcontrol"></a><span data-ttu-id="f4f1c-424">パラメーター - addSumControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-424">Parameters - addSumControl</span></span>

<span data-ttu-id="f4f1c-425">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-425">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-426">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-426">fieldId</span></span>  

### <a name="return-value---addsumcontrol"></a><span data-ttu-id="f4f1c-427">戻り値 - addSumControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-427">Return Value - addSumControl</span></span>

## <a name="method-addsumnamecontrol"></a><span data-ttu-id="f4f1c-428">メソッド addSumNameControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-428">Method addSumNameControl</span></span>

```xpp
public ReportSumControl addSumNameControl(str name)
```

### <a name="parameters---addsumnamecontrol"></a><span data-ttu-id="f4f1c-429">パラメーター - addSumNameControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-429">Parameters - addSumNameControl</span></span>

<span data-ttu-id="f4f1c-430">名前</span><span class="sxs-lookup"><span data-stu-id="f4f1c-430">name</span></span>  

### <a name="return-value---addsumnamecontrol"></a><span data-ttu-id="f4f1c-431">戻り値 - addSumNameControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-431">Return Value - addSumNameControl</span></span>

## <a name="method-addtextcontrol"></a><span data-ttu-id="f4f1c-432">メソッド addTextControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-432">Method addTextControl</span></span>

```xpp
public ReportTextControl addTextControl(str text)
```

### <a name="parameters---addtextcontrol"></a><span data-ttu-id="f4f1c-433">パラメーター - addTextControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-433">Parameters - addTextControl</span></span>

<span data-ttu-id="f4f1c-434">テキスト</span><span class="sxs-lookup"><span data-stu-id="f4f1c-434">text</span></span>  

### <a name="return-value---addtextcontrol"></a><span data-ttu-id="f4f1c-435">戻り値 - addTextControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-435">Return Value - addTextControl</span></span>

## <a name="method-addtimecontrol"></a><span data-ttu-id="f4f1c-436">メソッド addTimeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-436">Method addTimeControl</span></span>

```xpp
public ReportTimeControl addTimeControl(TableId tableId, FieldId fieldId)
```

### <a name="parameters---addtimecontrol"></a><span data-ttu-id="f4f1c-437">パラメーター - addTimeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-437">Parameters - addTimeControl</span></span>

<span data-ttu-id="f4f1c-438">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-438">tableId</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-439">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-439">fieldId</span></span>  

### <a name="return-value---addtimecontrol"></a><span data-ttu-id="f4f1c-440">戻り値 - addTimeControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-440">Return Value - addTimeControl</span></span>

## <a name="method-addtimedisplaycontrol"></a><span data-ttu-id="f4f1c-441">メソッド addTimeDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-441">Method addTimeDisplayControl</span></span>

```xpp
public ReportTimeControl addTimeDisplayControl(str displayFunc, [TableId tableId])
```

### <a name="parameters---addtimedisplaycontrol"></a><span data-ttu-id="f4f1c-442">パラメーター - addTimeDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-442">Parameters - addTimeDisplayControl</span></span>

<span data-ttu-id="f4f1c-443">displayFunc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-443">displayFunc</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-444">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-444">tableId</span></span>  

### <a name="return-value---addtimedisplaycontrol"></a><span data-ttu-id="f4f1c-445">戻り値 - addTimeDisplayControl</span><span class="sxs-lookup"><span data-stu-id="f4f1c-445">Return Value - addTimeDisplayControl</span></span>

## <a name="method-arrange"></a><span data-ttu-id="f4f1c-446">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="f4f1c-446">Method arrange</span></span>

```xpp
public int arrange()
```

### <a name="return-value---arrange"></a><span data-ttu-id="f4f1c-447">戻り値 - arrange</span><span class="sxs-lookup"><span data-stu-id="f4f1c-447">Return Value - arrange</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="f4f1c-448">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="f4f1c-448">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="f4f1c-449">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="f4f1c-449">Parameters - arrangeMethod</span></span>

<span data-ttu-id="f4f1c-450">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-450">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="f4f1c-451">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="f4f1c-451">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="f4f1c-452">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="f4f1c-452">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="f4f1c-453">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="f4f1c-453">Parameters - arrangeWhen</span></span>

<span data-ttu-id="f4f1c-454">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-454">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="f4f1c-455">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="f4f1c-455">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="f4f1c-456">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f4f1c-456">Method autoDeclaration</span></span>

<span data-ttu-id="f4f1c-457">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-457">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="f4f1c-458">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f4f1c-458">Parameters - autoDeclaration</span></span>

<span data-ttu-id="f4f1c-459">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-459">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="f4f1c-460">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f4f1c-460">Return Value - autoDeclaration</span></span>

<span data-ttu-id="f4f1c-461">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-461">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="f4f1c-462">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f4f1c-462">Remarks - autoDeclaration</span></span>

<span data-ttu-id="f4f1c-463">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-463">Controls cannot have identical names.</span></span>

## <a name="method-autoheader"></a><span data-ttu-id="f4f1c-464">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="f4f1c-464">Method autoHeader</span></span>

```xpp
public boolean autoHeader([boolean value])
```

### <a name="parameters---autoheader"></a><span data-ttu-id="f4f1c-465">パラメーター - autoHeader</span><span class="sxs-lookup"><span data-stu-id="f4f1c-465">Parameters - autoHeader</span></span>

<span data-ttu-id="f4f1c-466">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-466">value</span></span>  

### <a name="return-value---autoheader"></a><span data-ttu-id="f4f1c-467">戻り値 - autoHeader</span><span class="sxs-lookup"><span data-stu-id="f4f1c-467">Return Value - autoHeader</span></span>

## <a name="method-bold"></a><span data-ttu-id="f4f1c-468">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="f4f1c-468">Method bold</span></span>

<span data-ttu-id="f4f1c-469">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-469">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="f4f1c-470">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="f4f1c-470">Parameters - bold</span></span>

<span data-ttu-id="f4f1c-471">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-471">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="f4f1c-472">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="f4f1c-472">Return Value - bold</span></span>

<span data-ttu-id="f4f1c-473">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-473">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="f4f1c-474">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="f4f1c-474">Remarks - bold</span></span>

<span data-ttu-id="f4f1c-475">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-475">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="f4f1c-476">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-476">0 Use the default font weight.</span></span>
-   <span data-ttu-id="f4f1c-477">1 シン。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-477">1 Thin.</span></span>
-   <span data-ttu-id="f4f1c-478">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-478">2 Extra-light.</span></span>
-   <span data-ttu-id="f4f1c-479">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-479">3 Light.</span></span>
-   <span data-ttu-id="f4f1c-480">4 標準。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-480">4 Normal.</span></span>
-   <span data-ttu-id="f4f1c-481">5 中。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-481">5 Medium.</span></span>
-   <span data-ttu-id="f4f1c-482">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-482">6 Semibold.</span></span>
-   <span data-ttu-id="f4f1c-483">7 太字。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-483">7 Bold.</span></span>
-   <span data-ttu-id="f4f1c-484">8 極太。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-484">8 Extra-bold.</span></span>
-   <span data-ttu-id="f4f1c-485">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-485">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="f4f1c-486">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f4f1c-486">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="f4f1c-487">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f4f1c-487">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="f4f1c-488">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-488">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="f4f1c-489">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-489">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="f4f1c-490">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-490">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="f4f1c-491">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-491">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="f4f1c-492">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-492">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="f4f1c-493">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-493">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="f4f1c-494">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-494">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="f4f1c-495">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-495">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="f4f1c-496">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-496">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="f4f1c-497">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-497">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="f4f1c-498">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-498">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="f4f1c-499">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-499">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="f4f1c-500">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-500">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="f4f1c-501">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-501">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="f4f1c-502">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-502">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="f4f1c-503">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-503">Return Value - bottomMarginValue</span></span>

## <a name="method-bottommode"></a><span data-ttu-id="f4f1c-504">メソッド bottomMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-504">Method bottomMode</span></span>

```xpp
public int bottomMode([int value])
```

### <a name="parameters---bottommode"></a><span data-ttu-id="f4f1c-505">パラメーター - bottomMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-505">Parameters - bottomMode</span></span>

<span data-ttu-id="f4f1c-506">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-506">value</span></span>  

### <a name="return-value---bottommode"></a><span data-ttu-id="f4f1c-507">戻り値 - bottomMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-507">Return Value - bottomMode</span></span>

## <a name="method-bottomstr"></a><span data-ttu-id="f4f1c-508">メソッド bottomStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-508">Method bottomStr</span></span>

```xpp
public str bottomStr([str value])
```

### <a name="parameters---bottomstr"></a><span data-ttu-id="f4f1c-509">パラメーター - bottomStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-509">Parameters - bottomStr</span></span>

<span data-ttu-id="f4f1c-510">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-510">value</span></span>  

### <a name="return-value---bottomstr"></a><span data-ttu-id="f4f1c-511">戻り値 - bottomStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-511">Return Value - bottomStr</span></span>

## <a name="method-bottomunit"></a><span data-ttu-id="f4f1c-512">メソッド bottomUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-512">Method bottomUnit</span></span>

```xpp
public Units bottomUnit([Units value])
```

### <a name="parameters---bottomunit"></a><span data-ttu-id="f4f1c-513">パラメーター - bottomUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-513">Parameters - bottomUnit</span></span>

<span data-ttu-id="f4f1c-514">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-514">value</span></span>  

### <a name="return-value---bottomunit"></a><span data-ttu-id="f4f1c-515">戻り値 - bottomUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-515">Return Value - bottomUnit</span></span>

## <a name="method-bottomvalue"></a><span data-ttu-id="f4f1c-516">メソッド bottomValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-516">Method bottomValue</span></span>

```xpp
public Real bottomValue([Real value])
```

### <a name="parameters---bottomvalue"></a><span data-ttu-id="f4f1c-517">パラメーター - bottomValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-517">Parameters - bottomValue</span></span>

<span data-ttu-id="f4f1c-518">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-518">value</span></span>  

### <a name="return-value---bottomvalue"></a><span data-ttu-id="f4f1c-519">戻り値 - bottomValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-519">Return Value - bottomValue</span></span>

## <a name="method-characterset"></a><span data-ttu-id="f4f1c-520">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="f4f1c-520">Method characterSet</span></span>

<span data-ttu-id="f4f1c-521">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-521">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="f4f1c-522">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="f4f1c-522">Parameters - characterSet</span></span>

<span data-ttu-id="f4f1c-523">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-523">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="f4f1c-524">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="f4f1c-524">Return Value - characterSet</span></span>

<span data-ttu-id="f4f1c-525">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-525">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="f4f1c-526">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="f4f1c-526">Remarks - characterSet</span></span>

<span data-ttu-id="f4f1c-527">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-527">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="f4f1c-528">値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-528">Value.</span></span> | <span data-ttu-id="f4f1c-529">説明。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-529">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="f4f1c-530">0</span><span class="sxs-lookup"><span data-stu-id="f4f1c-530">0</span></span>      | <span data-ttu-id="f4f1c-531">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-531">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="f4f1c-532">1</span><span class="sxs-lookup"><span data-stu-id="f4f1c-532">1</span></span>      | <span data-ttu-id="f4f1c-533">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-533">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="f4f1c-534">2</span><span class="sxs-lookup"><span data-stu-id="f4f1c-534">2</span></span>      | <span data-ttu-id="f4f1c-535">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-535">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="f4f1c-536">77</span><span class="sxs-lookup"><span data-stu-id="f4f1c-536">77</span></span>     | <span data-ttu-id="f4f1c-537">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-537">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="f4f1c-538">128</span><span class="sxs-lookup"><span data-stu-id="f4f1c-538">128</span></span>    | <span data-ttu-id="f4f1c-539">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-539">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="f4f1c-540">129</span><span class="sxs-lookup"><span data-stu-id="f4f1c-540">129</span></span>    | <span data-ttu-id="f4f1c-541">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-541">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="f4f1c-542">134</span><span class="sxs-lookup"><span data-stu-id="f4f1c-542">134</span></span>    | <span data-ttu-id="f4f1c-543">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-543">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="f4f1c-544">136</span><span class="sxs-lookup"><span data-stu-id="f4f1c-544">136</span></span>    | <span data-ttu-id="f4f1c-545">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-545">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="f4f1c-546">161</span><span class="sxs-lookup"><span data-stu-id="f4f1c-546">161</span></span>    | <span data-ttu-id="f4f1c-547">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-547">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="f4f1c-548">162</span><span class="sxs-lookup"><span data-stu-id="f4f1c-548">162</span></span>    | <span data-ttu-id="f4f1c-549">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-549">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="f4f1c-550">163</span><span class="sxs-lookup"><span data-stu-id="f4f1c-550">163</span></span>    | <span data-ttu-id="f4f1c-551">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-551">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="f4f1c-552">186</span><span class="sxs-lookup"><span data-stu-id="f4f1c-552">186</span></span>    | <span data-ttu-id="f4f1c-553">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-553">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="f4f1c-554">204</span><span class="sxs-lookup"><span data-stu-id="f4f1c-554">204</span></span>    | <span data-ttu-id="f4f1c-555">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-555">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="f4f1c-556">238</span><span class="sxs-lookup"><span data-stu-id="f4f1c-556">238</span></span>    | <span data-ttu-id="f4f1c-557">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-557">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="f4f1c-558">255</span><span class="sxs-lookup"><span data-stu-id="f4f1c-558">255</span></span>    | <span data-ttu-id="f4f1c-559">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-559">OEM\_CHARSET</span></span>         |

<span data-ttu-id="f4f1c-560">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-560">The value in the following table is for the Korean language edition of Microsoft Windows:</span></span>

| <span data-ttu-id="f4f1c-561">値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-561">Value.</span></span> | <span data-ttu-id="f4f1c-562">説明。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-562">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="f4f1c-563">130</span><span class="sxs-lookup"><span data-stu-id="f4f1c-563">130</span></span>    | <span data-ttu-id="f4f1c-564">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-564">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="f4f1c-565">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-565">The values in the following table are for the Middle East language edition of Windows:</span></span>

| <span data-ttu-id="f4f1c-566">値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-566">Value.</span></span> | <span data-ttu-id="f4f1c-567">説明。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-567">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="f4f1c-568">177</span><span class="sxs-lookup"><span data-stu-id="f4f1c-568">177</span></span>    | <span data-ttu-id="f4f1c-569">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-569">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="f4f1c-570">178</span><span class="sxs-lookup"><span data-stu-id="f4f1c-570">178</span></span>    | <span data-ttu-id="f4f1c-571">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-571">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="f4f1c-572">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-572">The value in the following table is for the Thai language edition of Windows:</span></span>

| <span data-ttu-id="f4f1c-573">値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-573">Value.</span></span> | <span data-ttu-id="f4f1c-574">説明。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-574">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="f4f1c-575">222</span><span class="sxs-lookup"><span data-stu-id="f4f1c-575">222</span></span>    | <span data-ttu-id="f4f1c-576">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f4f1c-576">THAI\_CHARSET</span></span> |

<span data-ttu-id="f4f1c-577">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-577">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="f4f1c-578">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-578">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="f4f1c-579">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-579">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="f4f1c-580">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="f4f1c-580">Method colorScheme</span></span>

<span data-ttu-id="f4f1c-581">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-581">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="f4f1c-582">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f4f1c-582">Parameters - colorScheme</span></span>

<span data-ttu-id="f4f1c-583">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-583">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="f4f1c-584">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f4f1c-584">Return Value - colorScheme</span></span>

<span data-ttu-id="f4f1c-585">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-585">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="f4f1c-586">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f4f1c-586">Remarks - colorScheme</span></span>

<span data-ttu-id="f4f1c-587">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-587">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="f4f1c-588">値です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-588">Value.</span></span> | <span data-ttu-id="f4f1c-589">スタイル。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-589">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="f4f1c-590">0</span><span class="sxs-lookup"><span data-stu-id="f4f1c-590">0</span></span>      | <span data-ttu-id="f4f1c-591">既定。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-591">Default.</span></span>               |
| <span data-ttu-id="f4f1c-592">1</span><span class="sxs-lookup"><span data-stu-id="f4f1c-592">1</span></span>      | <span data-ttu-id="f4f1c-593">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-593">The Windows palette.</span></span>   |
| <span data-ttu-id="f4f1c-594">2</span><span class="sxs-lookup"><span data-stu-id="f4f1c-594">2</span></span>      | <span data-ttu-id="f4f1c-595">真の配色。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-595">The true-color scheme.</span></span> |

## <a name="method-columnheadingsstrategy"></a><span data-ttu-id="f4f1c-596">メソッド columnHeadingsStrategy</span><span class="sxs-lookup"><span data-stu-id="f4f1c-596">Method columnHeadingsStrategy</span></span>

```xpp
public int columnHeadingsStrategy([int value])
```

### <a name="parameters---columnheadingsstrategy"></a><span data-ttu-id="f4f1c-597">パラメーター - columnHeadingsStrategy</span><span class="sxs-lookup"><span data-stu-id="f4f1c-597">Parameters - columnHeadingsStrategy</span></span>

<span data-ttu-id="f4f1c-598">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-598">value</span></span>  

### <a name="return-value---columnheadingsstrategy"></a><span data-ttu-id="f4f1c-599">戻り値 - columnHeadingsStrategy</span><span class="sxs-lookup"><span data-stu-id="f4f1c-599">Return Value - columnHeadingsStrategy</span></span>

## <a name="method-columns"></a><span data-ttu-id="f4f1c-600">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="f4f1c-600">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="f4f1c-601">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="f4f1c-601">Parameters - columns</span></span>

<span data-ttu-id="f4f1c-602">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-602">value</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-603">モード</span><span class="sxs-lookup"><span data-stu-id="f4f1c-603">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="f4f1c-604">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="f4f1c-604">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="f4f1c-605">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-605">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="f4f1c-606">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-606">Parameters - columnsMode</span></span>

<span data-ttu-id="f4f1c-607">モード</span><span class="sxs-lookup"><span data-stu-id="f4f1c-607">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="f4f1c-608">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-608">Return Value - columnsMode</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="f4f1c-609">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-609">Method columnspaceMode</span></span>

```xpp
public int columnspaceMode([int value])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="f4f1c-610">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-610">Parameters - columnspaceMode</span></span>

<span data-ttu-id="f4f1c-611">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-611">value</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="f4f1c-612">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-612">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacestr"></a><span data-ttu-id="f4f1c-613">メソッド columnspaceStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-613">Method columnspaceStr</span></span>

```xpp
public str columnspaceStr([str value])
```

### <a name="parameters---columnspacestr"></a><span data-ttu-id="f4f1c-614">パラメーター - columnspaceStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-614">Parameters - columnspaceStr</span></span>

<span data-ttu-id="f4f1c-615">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-615">value</span></span>  

### <a name="return-value---columnspacestr"></a><span data-ttu-id="f4f1c-616">戻り値 - columnspaceStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-616">Return Value - columnspaceStr</span></span>

## <a name="method-columnspaceunit"></a><span data-ttu-id="f4f1c-617">メソッド columnspaceUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-617">Method columnspaceUnit</span></span>

```xpp
public Units columnspaceUnit([Units value])
```

### <a name="parameters---columnspaceunit"></a><span data-ttu-id="f4f1c-618">パラメーター - columnspaceUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-618">Parameters - columnspaceUnit</span></span>

<span data-ttu-id="f4f1c-619">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-619">value</span></span>  

### <a name="return-value---columnspaceunit"></a><span data-ttu-id="f4f1c-620">戻り値 - columnspaceUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-620">Return Value - columnspaceUnit</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="f4f1c-621">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-621">Method columnspaceValue</span></span>

```xpp
public Real columnspaceValue([Real value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="f4f1c-622">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-622">Parameters - columnspaceValue</span></span>

<span data-ttu-id="f4f1c-623">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-623">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="f4f1c-624">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-624">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="f4f1c-625">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-625">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="f4f1c-626">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-626">Parameters - columnsValue</span></span>

<span data-ttu-id="f4f1c-627">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-627">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="f4f1c-628">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-628">Return Value - columnsValue</span></span>

## <a name="method-control"></a><span data-ttu-id="f4f1c-629">メソッド control</span><span class="sxs-lookup"><span data-stu-id="f4f1c-629">Method control</span></span>

<span data-ttu-id="f4f1c-630">コントロールのテーブルおよび dataField プロパティに基づいて、セクションのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-630">Finds a control in the section, based on the control�s table and dataField properties.</span></span>

```xpp
public ReportControl control(FieldId fieldId, [TableId tableId])
```

### <a name="parameters---control"></a><span data-ttu-id="f4f1c-631">パラメーター - control</span><span class="sxs-lookup"><span data-stu-id="f4f1c-631">Parameters - control</span></span>

<span data-ttu-id="f4f1c-632">fieldId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-632">fieldId</span></span>  
<span data-ttu-id="f4f1c-633">コントロールのテーブル プロパティ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-633">The control's table property; optional.</span></span>

<!-- -->

<span data-ttu-id="f4f1c-634">tableId</span><span class="sxs-lookup"><span data-stu-id="f4f1c-634">tableId</span></span>  
<span data-ttu-id="f4f1c-635">コントロールのテーブル プロパティ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-635">The control's table property; optional.</span></span>

### <a name="return-value---control"></a><span data-ttu-id="f4f1c-636">戻り値 - control</span><span class="sxs-lookup"><span data-stu-id="f4f1c-636">Return Value - control</span></span>

<span data-ttu-id="f4f1c-637">検索されるレポート コントロール。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-637">The report control that is found.</span></span>

### <a name="remarks---control"></a><span data-ttu-id="f4f1c-638">備考 - control</span><span class="sxs-lookup"><span data-stu-id="f4f1c-638">Remarks - control</span></span>

<span data-ttu-id="f4f1c-639">テーブル ID が指定されていない場合は、セクションの親セクション グループからテーブル プロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-639">If the table ID is not supplied, the table property from the section�s parent section group is used.</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="f4f1c-640">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="f4f1c-640">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="f4f1c-641">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="f4f1c-641">Return Value - controlCount</span></span>

## <a name="method-controlname"></a><span data-ttu-id="f4f1c-642">メソッド controlName</span><span class="sxs-lookup"><span data-stu-id="f4f1c-642">Method controlName</span></span>

<span data-ttu-id="f4f1c-643">コントロールの Name プロパティに基づいて、セクションのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-643">Finds a control in a section, based on the control's Name property.</span></span>

```xpp
public ReportControl controlName(str name)
```

### <a name="parameters---controlname"></a><span data-ttu-id="f4f1c-644">パラメーター - controlName</span><span class="sxs-lookup"><span data-stu-id="f4f1c-644">Parameters - controlName</span></span>

<span data-ttu-id="f4f1c-645">名前</span><span class="sxs-lookup"><span data-stu-id="f4f1c-645">name</span></span>  
<span data-ttu-id="f4f1c-646">コントロール Name プロパティ。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-646">The Name property of the control.</span></span>

### <a name="return-value---controlname"></a><span data-ttu-id="f4f1c-647">戻り値 - controlName</span><span class="sxs-lookup"><span data-stu-id="f4f1c-647">Return Value - controlName</span></span>

<span data-ttu-id="f4f1c-648">見つかったコントロール。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-648">The control that is found.</span></span>

## <a name="method-controlno"></a><span data-ttu-id="f4f1c-649">メソッド controlNo</span><span class="sxs-lookup"><span data-stu-id="f4f1c-649">Method controlNo</span></span>

```xpp
public ReportControl controlNo(int number)
```

### <a name="parameters---controlno"></a><span data-ttu-id="f4f1c-650">パラメーター - controlNo</span><span class="sxs-lookup"><span data-stu-id="f4f1c-650">Parameters - controlNo</span></span>

<span data-ttu-id="f4f1c-651">番号</span><span class="sxs-lookup"><span data-stu-id="f4f1c-651">number</span></span>  

### <a name="return-value---controlno"></a><span data-ttu-id="f4f1c-652">戻り値 - controlNo</span><span class="sxs-lookup"><span data-stu-id="f4f1c-652">Return Value - controlNo</span></span>

## <a name="method-controlnumber"></a><span data-ttu-id="f4f1c-653">メソッド controlNumber</span><span class="sxs-lookup"><span data-stu-id="f4f1c-653">Method controlNumber</span></span>

```xpp
public int controlNumber([int value])
```

### <a name="parameters---controlnumber"></a><span data-ttu-id="f4f1c-654">パラメーター - controlNumber</span><span class="sxs-lookup"><span data-stu-id="f4f1c-654">Parameters - controlNumber</span></span>

<span data-ttu-id="f4f1c-655">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-655">value</span></span>  

### <a name="return-value---controlnumber"></a><span data-ttu-id="f4f1c-656">戻り値 - controlNumber</span><span class="sxs-lookup"><span data-stu-id="f4f1c-656">Return Value - controlNumber</span></span>

## <a name="method-delete"></a><span data-ttu-id="f4f1c-657">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="f4f1c-657">Method delete</span></span>

<span data-ttu-id="f4f1c-658">現在のノードを AOT から削除します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-658">Deletes the current node from the AOT.</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="f4f1c-659">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="f4f1c-659">Return Value - delete</span></span>

## <a name="method-font"></a><span data-ttu-id="f4f1c-660">メソッド font</span><span class="sxs-lookup"><span data-stu-id="f4f1c-660">Method font</span></span>

<span data-ttu-id="f4f1c-661">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-661">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="f4f1c-662">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="f4f1c-662">Parameters - font</span></span>

<span data-ttu-id="f4f1c-663">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-663">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="f4f1c-664">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="f4f1c-664">Return Value - font</span></span>

<span data-ttu-id="f4f1c-665">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-665">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="f4f1c-666">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="f4f1c-666">Method fontSize</span></span>

<span data-ttu-id="f4f1c-667">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-667">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="f4f1c-668">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="f4f1c-668">Parameters - fontSize</span></span>

<span data-ttu-id="f4f1c-669">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-669">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="f4f1c-670">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="f4f1c-670">Return Value - fontSize</span></span>

<span data-ttu-id="f4f1c-671">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-671">The height of the font in points.</span></span>

## <a name="method-footertext"></a><span data-ttu-id="f4f1c-672">メソッド footerText</span><span class="sxs-lookup"><span data-stu-id="f4f1c-672">Method footerText</span></span>

```xpp
public str footerText([str value])
```

### <a name="parameters---footertext"></a><span data-ttu-id="f4f1c-673">パラメーター - footerText</span><span class="sxs-lookup"><span data-stu-id="f4f1c-673">Parameters - footerText</span></span>

<span data-ttu-id="f4f1c-674">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-674">value</span></span>  

### <a name="return-value---footertext"></a><span data-ttu-id="f4f1c-675">戻り値 - footerText</span><span class="sxs-lookup"><span data-stu-id="f4f1c-675">Return Value - footerText</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="f4f1c-676">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f4f1c-676">Method foregroundColor</span></span>

<span data-ttu-id="f4f1c-677">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-677">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="f4f1c-678">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f4f1c-678">Parameters - foregroundColor</span></span>

<span data-ttu-id="f4f1c-679">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-679">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="f4f1c-680">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f4f1c-680">Return Value - foregroundColor</span></span>

<span data-ttu-id="f4f1c-681">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-681">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="f4f1c-682">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f4f1c-682">Remarks - foregroundColor</span></span>

<span data-ttu-id="f4f1c-683">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-683">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="f4f1c-684">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-684">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="f4f1c-685">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-685">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="f4f1c-686">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-686">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="f4f1c-687">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-687">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="f4f1c-688">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-688">The maximum value for a single byte is 255.</span></span>

## <a name="method-grandheader"></a><span data-ttu-id="f4f1c-689">メソッド grandHeader</span><span class="sxs-lookup"><span data-stu-id="f4f1c-689">Method grandHeader</span></span>

```xpp
public boolean grandHeader([boolean value])
```

### <a name="parameters---grandheader"></a><span data-ttu-id="f4f1c-690">パラメーター - grandHeader</span><span class="sxs-lookup"><span data-stu-id="f4f1c-690">Parameters - grandHeader</span></span>

<span data-ttu-id="f4f1c-691">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-691">value</span></span>  

### <a name="return-value---grandheader"></a><span data-ttu-id="f4f1c-692">戻り値 - grandHeader</span><span class="sxs-lookup"><span data-stu-id="f4f1c-692">Return Value - grandHeader</span></span>

## <a name="method-grandtotal"></a><span data-ttu-id="f4f1c-693">メソッド grandTotal</span><span class="sxs-lookup"><span data-stu-id="f4f1c-693">Method grandTotal</span></span>

<span data-ttu-id="f4f1c-694">FooterText プロパティ値が表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-694">Determines whether the FooterText property value can be displayed.</span></span>

```xpp
public boolean grandTotal([boolean value])
```

### <a name="parameters---grandtotal"></a><span data-ttu-id="f4f1c-695">パラメーター - grandTotal</span><span class="sxs-lookup"><span data-stu-id="f4f1c-695">Parameters - grandTotal</span></span>

<span data-ttu-id="f4f1c-696">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-696">value</span></span>  

### <a name="return-value---grandtotal"></a><span data-ttu-id="f4f1c-697">戻り値 - grandTotal</span><span class="sxs-lookup"><span data-stu-id="f4f1c-697">Return Value - grandTotal</span></span>

<span data-ttu-id="f4f1c-698">FooterText プロパティ値が表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-698">true if the FooterText property value is displayed; otherwise, false.</span></span>

### <a name="remarks---grandtotal"></a><span data-ttu-id="f4f1c-699">備考 - grandTotal</span><span class="sxs-lookup"><span data-stu-id="f4f1c-699">Remarks - grandTotal</span></span>

<span data-ttu-id="f4f1c-700">grandTotal プロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-700">The grandTotal property is available only when a report has unnested, multiple data sources.</span></span>

## <a name="method-hasbuttons"></a><span data-ttu-id="f4f1c-701">メソッド hasButtons</span><span class="sxs-lookup"><span data-stu-id="f4f1c-701">Method hasButtons</span></span>

```xpp
public boolean hasButtons([boolean value])
```

### <a name="parameters---hasbuttons"></a><span data-ttu-id="f4f1c-702">パラメーター - hasButtons</span><span class="sxs-lookup"><span data-stu-id="f4f1c-702">Parameters - hasButtons</span></span>

<span data-ttu-id="f4f1c-703">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-703">value</span></span>  

### <a name="return-value---hasbuttons"></a><span data-ttu-id="f4f1c-704">戻り値 - hasButtons</span><span class="sxs-lookup"><span data-stu-id="f4f1c-704">Return Value - hasButtons</span></span>

## <a name="method-headerdetaillevel"></a><span data-ttu-id="f4f1c-705">メソッド headerDetailLevel</span><span class="sxs-lookup"><span data-stu-id="f4f1c-705">Method headerDetailLevel</span></span>

```xpp
public int headerDetailLevel([int value], [AutoMode mode])
```

### <a name="parameters---headerdetaillevel"></a><span data-ttu-id="f4f1c-706">パラメーター - headerDetailLevel</span><span class="sxs-lookup"><span data-stu-id="f4f1c-706">Parameters - headerDetailLevel</span></span>

<span data-ttu-id="f4f1c-707">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-707">value</span></span>  

<!-- -->

<span data-ttu-id="f4f1c-708">モード</span><span class="sxs-lookup"><span data-stu-id="f4f1c-708">mode</span></span>  

### <a name="return-value---headerdetaillevel"></a><span data-ttu-id="f4f1c-709">戻り値 - headerDetailLevel</span><span class="sxs-lookup"><span data-stu-id="f4f1c-709">Return Value - headerDetailLevel</span></span>

## <a name="method-headerdetaillevelmode"></a><span data-ttu-id="f4f1c-710">メソッド headerDetailLevelMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-710">Method headerDetailLevelMode</span></span>

```xpp
public AutoMode headerDetailLevelMode([AutoMode mode])
```

### <a name="parameters---headerdetaillevelmode"></a><span data-ttu-id="f4f1c-711">パラメーター - headerDetailLevelMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-711">Parameters - headerDetailLevelMode</span></span>

<span data-ttu-id="f4f1c-712">モード</span><span class="sxs-lookup"><span data-stu-id="f4f1c-712">mode</span></span>  

### <a name="return-value---headerdetaillevelmode"></a><span data-ttu-id="f4f1c-713">戻り値 - headerDetailLevelMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-713">Return Value - headerDetailLevelMode</span></span>

## <a name="method-headerdetaillevelvalue"></a><span data-ttu-id="f4f1c-714">メソッド headerDetailLevelValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-714">Method headerDetailLevelValue</span></span>

```xpp
public int headerDetailLevelValue([int value])
```

### <a name="parameters---headerdetaillevelvalue"></a><span data-ttu-id="f4f1c-715">パラメーター - headerDetailLevelValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-715">Parameters - headerDetailLevelValue</span></span>

<span data-ttu-id="f4f1c-716">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-716">value</span></span>  

### <a name="return-value---headerdetaillevelvalue"></a><span data-ttu-id="f4f1c-717">戻り値 - headerDetailLevelValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-717">Return Value - headerDetailLevelValue</span></span>

## <a name="method-headertext"></a><span data-ttu-id="f4f1c-718">メソッド headerText</span><span class="sxs-lookup"><span data-stu-id="f4f1c-718">Method headerText</span></span>

```xpp
public str headerText([str value])
```

### <a name="parameters---headertext"></a><span data-ttu-id="f4f1c-719">パラメーター - headerText</span><span class="sxs-lookup"><span data-stu-id="f4f1c-719">Parameters - headerText</span></span>

<span data-ttu-id="f4f1c-720">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-720">value</span></span>  

### <a name="return-value---headertext"></a><span data-ttu-id="f4f1c-721">戻り値 - headerText</span><span class="sxs-lookup"><span data-stu-id="f4f1c-721">Return Value - headerText</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="f4f1c-722">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="f4f1c-722">Method height100mm</span></span>

<span data-ttu-id="f4f1c-723">枠線および上下の余白の高さを除く、セクションの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-723">Gets or sets the height of a section, excluding the height of the border and the top and bottom margins.</span></span>

```xpp
public int height100mm([int height])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="f4f1c-724">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="f4f1c-724">Parameters - height100mm</span></span>

<span data-ttu-id="f4f1c-725">height</span><span class="sxs-lookup"><span data-stu-id="f4f1c-725">height</span></span>  
<span data-ttu-id="f4f1c-726">1/100 mm の新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-726">The new value in 1/100 mm; optional.</span></span>

### <a name="return-value---height100mm"></a><span data-ttu-id="f4f1c-727">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="f4f1c-727">Return Value - height100mm</span></span>

<span data-ttu-id="f4f1c-728">1/100 mm 単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-728">The height in 1/100 mm.</span></span>

### <a name="remarks---height100mm"></a><span data-ttu-id="f4f1c-729">備考 - height100mm</span><span class="sxs-lookup"><span data-stu-id="f4f1c-729">Remarks - height100mm</span></span>

<span data-ttu-id="f4f1c-730">このメソッドは、heightExclBorderAndMargins メソッドとして機能します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-730">This method acts as a heightExclBorderAndMargins method.</span></span> <span data-ttu-id="f4f1c-731">返される高さは、height プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-731">The height that is returned corresponds to the value of the height property.</span></span> <span data-ttu-id="f4f1c-732">この関数を使用して height プロパティを設定する前に、height プロパティが AUTO に設定されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-732">Before you use this function to set the height property, make sure that the height property is not set to AUTO.</span></span> <span data-ttu-id="f4f1c-733">それ以外の場合、組み込みロジックは、値を再計算する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-733">Otherwise, built-in logic might recalculate the value.</span></span>

## <a name="method-heightmm100"></a><span data-ttu-id="f4f1c-734">メソッド heightmm100</span><span class="sxs-lookup"><span data-stu-id="f4f1c-734">Method heightmm100</span></span>

<span data-ttu-id="f4f1c-735">枠線および上下の余白の高さを含む、セクションの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-735">Gets or sets the height of a section, including the height of the border and the top and bottom margins.</span></span>

```xpp
public int heightmm100([int heightInclMargins])
```

### <a name="parameters---heightmm100"></a><span data-ttu-id="f4f1c-736">パラメーター - heightmm100</span><span class="sxs-lookup"><span data-stu-id="f4f1c-736">Parameters - heightmm100</span></span>

<span data-ttu-id="f4f1c-737">heightInclMargins</span><span class="sxs-lookup"><span data-stu-id="f4f1c-737">heightInclMargins</span></span>  
<span data-ttu-id="f4f1c-738">セクションの新しい合計高さ (1/100 mm) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-738">The new total height of the section in 1/100 mm; optional.</span></span>

### <a name="return-value---heightmm100"></a><span data-ttu-id="f4f1c-739">戻り値 - heightmm100</span><span class="sxs-lookup"><span data-stu-id="f4f1c-739">Return Value - heightmm100</span></span>

<span data-ttu-id="f4f1c-740">1/100 mm 単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-740">The height in 1/100 mm.</span></span>

### <a name="remarks---heightmm100"></a><span data-ttu-id="f4f1c-741">備考 - heightmm100</span><span class="sxs-lookup"><span data-stu-id="f4f1c-741">Remarks - heightmm100</span></span>

<span data-ttu-id="f4f1c-742">このメソッドは、heightInclBorderAndMargins メソッドとして機能します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-742">This method acts as a heightInclBorderAndMargins method.</span></span> <span data-ttu-id="f4f1c-743">この関数を使用して height プロパティを設定する前に、height プロパティが AUTO に設定されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-743">Before you use this function to set the height property, make sure that the height property is not set to AUTO.</span></span> <span data-ttu-id="f4f1c-744">それ以外の場合、組み込みロジックは、高さを設定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-744">Otherwise, the built-in logic might set the height.</span></span> <span data-ttu-id="f4f1c-745">Heightmm100 メソッドに 1000 が返される場合は、セクションの合計の高さは 10 mm になります。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-745">If the heightmm100 method returns 1000, the total height of the section is 10 mm.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="f4f1c-746">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-746">Method heightMode</span></span>

<span data-ttu-id="f4f1c-747">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-747">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="f4f1c-748">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-748">Parameters - heightMode</span></span>

<span data-ttu-id="f4f1c-749">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-749">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="f4f1c-750">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-750">Return Value - heightMode</span></span>

<span data-ttu-id="f4f1c-751">計算モード。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-751">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="f4f1c-752">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-752">Remarks - heightMode</span></span>

<span data-ttu-id="f4f1c-753">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="f4f1c-753">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="f4f1c-754">モード。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-754">Mode.</span></span>          | <span data-ttu-id="f4f1c-755">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-755">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f1c-756">正確。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-756">Exact.</span></span>         | <span data-ttu-id="f4f1c-757">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-757">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f4f1c-758">自動。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-758">Auto.</span></span>          | <span data-ttu-id="f4f1c-759">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-759">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f4f1c-760">列の高さ</span><span class="sxs-lookup"><span data-stu-id="f4f1c-760">Column height.</span></span> | <span data-ttu-id="f4f1c-761">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-761">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="f4f1c-762">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-762">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="f4f1c-763">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-763">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="f4f1c-764">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-764">Parameters - heightStr</span></span>

<span data-ttu-id="f4f1c-765">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-765">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="f4f1c-766">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-766">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="f4f1c-767">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-767">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="f4f1c-768">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-768">Parameters - heightUnit</span></span>

<span data-ttu-id="f4f1c-769">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-769">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="f4f1c-770">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-770">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="f4f1c-771">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-771">Method heightValue</span></span>

<span data-ttu-id="f4f1c-772">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-772">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="f4f1c-773">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-773">Parameters - heightValue</span></span>

<span data-ttu-id="f4f1c-774">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-774">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="f4f1c-775">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-775">Return Value - heightValue</span></span>

<span data-ttu-id="f4f1c-776">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-776">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="f4f1c-777">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-777">Remarks - heightValue</span></span>

<span data-ttu-id="f4f1c-778">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-778">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="f4f1c-779">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="f4f1c-779">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="f4f1c-780">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="f4f1c-780">Parameters - italic</span></span>

<span data-ttu-id="f4f1c-781">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-781">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="f4f1c-782">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="f4f1c-782">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="f4f1c-783">メソッド label</span><span class="sxs-lookup"><span data-stu-id="f4f1c-783">Method label</span></span>

<span data-ttu-id="f4f1c-784">AOT 内のセクション ノードの説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-784">Gets the description of the section node in the AOT.</span></span>

```xpp
public str label()
```

### <a name="return-value---label"></a><span data-ttu-id="f4f1c-785">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="f4f1c-785">Return Value - label</span></span>

<span data-ttu-id="f4f1c-786">セクション ノードの説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f4f1c-786">A string that contains the description of the section node.</span></span>

## <a name="method-labelbottommarginmode"></a><span data-ttu-id="f4f1c-787">メソッド labelBottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-787">Method labelBottomMarginMode</span></span>

```xpp
public int labelBottomMarginMode([int value])
```

### <a name="parameters---labelbottommarginmode"></a><span data-ttu-id="f4f1c-788">パラメーター - labelBottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-788">Parameters - labelBottomMarginMode</span></span>

<span data-ttu-id="f4f1c-789">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-789">value</span></span>  

### <a name="return-value---labelbottommarginmode"></a><span data-ttu-id="f4f1c-790">戻り値 - labelBottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-790">Return Value - labelBottomMarginMode</span></span>

## <a name="method-labelbottommarginstr"></a><span data-ttu-id="f4f1c-791">メソッド labelBottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-791">Method labelBottomMarginStr</span></span>

```xpp
public str labelBottomMarginStr([str value])
```

### <a name="parameters---labelbottommarginstr"></a><span data-ttu-id="f4f1c-792">パラメーター - labelBottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-792">Parameters - labelBottomMarginStr</span></span>

<span data-ttu-id="f4f1c-793">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-793">value</span></span>  

### <a name="return-value---labelbottommarginstr"></a><span data-ttu-id="f4f1c-794">戻り値 - labelBottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-794">Return Value - labelBottomMarginStr</span></span>

## <a name="method-labelbottommarginunit"></a><span data-ttu-id="f4f1c-795">メソッド labelBottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-795">Method labelBottomMarginUnit</span></span>

```xpp
public Units labelBottomMarginUnit([Units value])
```

### <a name="parameters---labelbottommarginunit"></a><span data-ttu-id="f4f1c-796">パラメーター - labelBottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-796">Parameters - labelBottomMarginUnit</span></span>

<span data-ttu-id="f4f1c-797">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-797">value</span></span>  

### <a name="return-value---labelbottommarginunit"></a><span data-ttu-id="f4f1c-798">戻り値 - labelBottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-798">Return Value - labelBottomMarginUnit</span></span>

## <a name="method-labelbottommarginvalue"></a><span data-ttu-id="f4f1c-799">メソッド labelBottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-799">Method labelBottomMarginValue</span></span>

```xpp
public Real labelBottomMarginValue([Real value])
```

### <a name="parameters---labelbottommarginvalue"></a><span data-ttu-id="f4f1c-800">パラメーター - labelBottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-800">Parameters - labelBottomMarginValue</span></span>

<span data-ttu-id="f4f1c-801">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-801">value</span></span>  

### <a name="return-value---labelbottommarginvalue"></a><span data-ttu-id="f4f1c-802">戻り値 - labelBottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-802">Return Value - labelBottomMarginValue</span></span>

## <a name="method-labeltopmarginmode"></a><span data-ttu-id="f4f1c-803">メソッド labelTopMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-803">Method labelTopMarginMode</span></span>

```xpp
public int labelTopMarginMode([int value])
```

### <a name="parameters---labeltopmarginmode"></a><span data-ttu-id="f4f1c-804">パラメーター - labelTopMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-804">Parameters - labelTopMarginMode</span></span>

<span data-ttu-id="f4f1c-805">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-805">value</span></span>  

### <a name="return-value---labeltopmarginmode"></a><span data-ttu-id="f4f1c-806">戻り値 - labelTopMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-806">Return Value - labelTopMarginMode</span></span>

## <a name="method-labeltopmarginstr"></a><span data-ttu-id="f4f1c-807">メソッド labelTopMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-807">Method labelTopMarginStr</span></span>

```xpp
public str labelTopMarginStr([str value])
```

### <a name="parameters---labeltopmarginstr"></a><span data-ttu-id="f4f1c-808">パラメーター - labelTopMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-808">Parameters - labelTopMarginStr</span></span>

<span data-ttu-id="f4f1c-809">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-809">value</span></span>  

### <a name="return-value---labeltopmarginstr"></a><span data-ttu-id="f4f1c-810">戻り値 - labelTopMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-810">Return Value - labelTopMarginStr</span></span>

## <a name="method-labeltopmarginunit"></a><span data-ttu-id="f4f1c-811">メソッド labelTopMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-811">Method labelTopMarginUnit</span></span>

```xpp
public Units labelTopMarginUnit([Units value])
```

### <a name="parameters---labeltopmarginunit"></a><span data-ttu-id="f4f1c-812">パラメーター - labelTopMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-812">Parameters - labelTopMarginUnit</span></span>

<span data-ttu-id="f4f1c-813">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-813">value</span></span>  

### <a name="return-value---labeltopmarginunit"></a><span data-ttu-id="f4f1c-814">戻り値 - labelTopMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-814">Return Value - labelTopMarginUnit</span></span>

## <a name="method-labeltopmarginvalue"></a><span data-ttu-id="f4f1c-815">メソッド labelTopMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-815">Method labelTopMarginValue</span></span>

```xpp
public Real labelTopMarginValue([Real value])
```

### <a name="parameters---labeltopmarginvalue"></a><span data-ttu-id="f4f1c-816">パラメーター - labelTopMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-816">Parameters - labelTopMarginValue</span></span>

<span data-ttu-id="f4f1c-817">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-817">value</span></span>  

### <a name="return-value---labeltopmarginvalue"></a><span data-ttu-id="f4f1c-818">戻り値 - labelTopMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-818">Return Value - labelTopMarginValue</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="f4f1c-819">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-819">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="f4f1c-820">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-820">Parameters - leftMarginMode</span></span>

<span data-ttu-id="f4f1c-821">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-821">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="f4f1c-822">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f4f1c-822">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginsetc"></a><span data-ttu-id="f4f1c-823">メソッド leftMarginsEtc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-823">Method leftMarginsEtc</span></span>

```xpp
public int leftMarginsEtc()
```

### <a name="return-value---leftmarginsetc"></a><span data-ttu-id="f4f1c-824">戻り値 - leftMarginsEtc</span><span class="sxs-lookup"><span data-stu-id="f4f1c-824">Return Value - leftMarginsEtc</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="f4f1c-825">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-825">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="f4f1c-826">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-826">Parameters - leftMarginStr</span></span>

<span data-ttu-id="f4f1c-827">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-827">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="f4f1c-828">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-828">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="f4f1c-829">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-829">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="f4f1c-830">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f4f1c-830">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="f4f1c-831">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-831">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="f4f1c-832">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f4f1c-832">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="f4f1c-833">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-833">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="f4f1c-834">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-834">Parameters - leftMarginValue</span></span>

<span data-ttu-id="f4f1c-835">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-835">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="f4f1c-836">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f4f1c-836">Return Value - leftMarginValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="f4f1c-837">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="f4f1c-837">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="f4f1c-838">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="f4f1c-838">Parameters - lineAbove</span></span>

<span data-ttu-id="f4f1c-839">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-839">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="f4f1c-840">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="f4f1c-840">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="f4f1c-841">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="f4f1c-841">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="f4f1c-842">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="f4f1c-842">Parameters - lineBelow</span></span>

<span data-ttu-id="f4f1c-843">値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-843">value</span></span>  

### <a name="return-valu"></a><span data-ttu-id="f4f1c-844">戻り値</span><span class="sxs-lookup"><span data-stu-id="f4f1c-844">Return Valu</span></span>
