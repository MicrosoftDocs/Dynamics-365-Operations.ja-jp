---
title: Report クラス
description: このトピックでは、Report クラスについて説明します。
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
ms.openlocfilehash: 05da263dd215d3bffdd602fc79728aa2235dd96c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502849"
---
# <a name="class-report"></a><span data-ttu-id="46d30-103">クラス レポート</span><span class="sxs-lookup"><span data-stu-id="46d30-103">Class Report</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Report extends TreeNode
```

<span data-ttu-id="46d30-104">Report クラスを使用すると、ユーザーは AOT ではなくコードを使用することにより、アプリケーション オブジェクト ツリー (AOT) とレポート作成に格納されているレポートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="46d30-104">The Report class lets users use reports that are present in the Application Object Tree (AOT) and report creation by using code instead of the AOT.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d30-105">備考</span><span class="sxs-lookup"><span data-stu-id="46d30-105">Remarks</span></span>

<span data-ttu-id="46d30-106">レポート オブジェクトには、クエリと、ゼロかそれ以上のデザインが含まれます。</span><span class="sxs-lookup"><span data-stu-id="46d30-106">A Report object contains a query and zero or more designs.</span></span> <span data-ttu-id="46d30-107">各デザインは、画面に表示または印刷が可能なレポートのレイアウトの定義です。</span><span class="sxs-lookup"><span data-stu-id="46d30-107">Each design is a definition of the layout of a report that can be displayed on screen or printed.</span></span> <span data-ttu-id="46d30-108">レポート オブジェクトには、上書きできる ReportRun メソッドもあります。</span><span class="sxs-lookup"><span data-stu-id="46d30-108">A Report object also has ReportRun methods that can be overridden.</span></span> <span data-ttu-id="46d30-109">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="46d30-109">This class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="46d30-110">例</span><span class="sxs-lookup"><span data-stu-id="46d30-110">Examples</span></span>

<span data-ttu-id="46d30-111">次のコード例は、AOT には存在しないレポートを作成して実行します。</span><span class="sxs-lookup"><span data-stu-id="46d30-111">The following code example creates and runs a report that is not present in the AOT.</span></span>

```xpp
static void test(args a) 
{ 
    report r; 
    reportDesign rd; 
    reportSection rs; 
    reportRun rr; 
    // Creates a simple report that is not present in  
    // the AOT. 
    r = new report(); 
    rd = r.addDesign("myDesign"); 
    // Adds a section that is triggered by execute(1). 
    rs = rd.addProgrammableSection(1);
    rs.addTextControl("Hello world"); 
    // Runs the report. 
    rr = new reportRun(r); 
    // Runs the SysPrintForm form. 
    if (rr.prompt())  
    { 
        // Executes the programmable section. 
        rr.execute(1);  
        // Prints the report to the target selected 
        // during the previous prompt call. 
        rr.print();    
    } 
}
```

## <a name="methods"></a><span data-ttu-id="46d30-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="46d30-112">Methods</span></span>

| <span data-ttu-id="46d30-113">方法</span><span class="sxs-lookup"><span data-stu-id="46d30-113">Method</span></span>                                                              | <span data-ttu-id="46d30-114">説明</span><span class="sxs-lookup"><span data-stu-id="46d30-114">Description</span></span>                                                                                                                               |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d30-115">public ReportDesign addDesign(\[str name\], \[container buffer\])</span><span class="sxs-lookup"><span data-stu-id="46d30-115">public ReportDesign addDesign(\[str name\], \[container buffer\])</span></span>   | <span data-ttu-id="46d30-116">レポートが属している reportDesign を作成します。</span><span class="sxs-lookup"><span data-stu-id="46d30-116">Creates a reportDesign that belongs to a report.</span></span>                                                                                          |
| <span data-ttu-id="46d30-117">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-117">public boolean allowCheck(\[boolean value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="46d30-118">public boolean autoJoin(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-118">public boolean autoJoin(\[boolean value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="46d30-119">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-119">public str changedBy(\[str value\])</span></span>                                 | <span data-ttu-id="46d30-120">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-120">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="46d30-121">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-121">public Date changedDate(\[Date value\])</span></span>                             | <span data-ttu-id="46d30-122">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-122">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="46d30-123">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-123">public str changedTime(\[str value\])</span></span>                               | <span data-ttu-id="46d30-124">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-124">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="46d30-125">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-125">public str createdBy(\[str value\])</span></span>                                 | <span data-ttu-id="46d30-126">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-126">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="46d30-127">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-127">public Date creationDate(\[Date value\])</span></span>                            | <span data-ttu-id="46d30-128">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-128">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="46d30-129">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-129">public str creationTime(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="46d30-130">public ReportDesign design(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="46d30-130">public ReportDesign design(\[str name\])</span></span>                            | <span data-ttu-id="46d30-131">既存のデザインを取得します。</span><span class="sxs-lookup"><span data-stu-id="46d30-131">Retrieves an existing design.</span></span>                                                                                                             |
| <span data-ttu-id="46d30-132">public int designCount()</span><span class="sxs-lookup"><span data-stu-id="46d30-132">public int designCount()</span></span>                                            | <span data-ttu-id="46d30-133">特定のレポートのデザインの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="46d30-133">Retrieves the number of designs in a given report.</span></span>                                                                                        |
| <span data-ttu-id="46d30-134">public ReportDesign designNumber(\[int number\])</span><span class="sxs-lookup"><span data-stu-id="46d30-134">public ReportDesign designNumber(\[int number\])</span></span>                    | <span data-ttu-id="46d30-135">既存のデザインを取得します。</span><span class="sxs-lookup"><span data-stu-id="46d30-135">Gets an existing design.</span></span>                                                                                                                  |
| <span data-ttu-id="46d30-136">public boolean interactive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-136">public boolean interactive(\[boolean value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="46d30-137">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-137">public str name(\[str value\])</span></span>                                      | <span data-ttu-id="46d30-138">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-138">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="46d30-139">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="46d30-139">public Guid origin(\[Guid value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="46d30-140">public container pack()</span><span class="sxs-lookup"><span data-stu-id="46d30-140">public container pack()</span></span>                                             | <span data-ttu-id="46d30-141">Report クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="46d30-141">Serializes the current instance of the Report class.</span></span>                                                                                      |
| <span data-ttu-id="46d30-142">public Query query(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="46d30-142">public Query query(\[Query query\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="46d30-143">public boolean saved()</span><span class="sxs-lookup"><span data-stu-id="46d30-143">public boolean saved()</span></span>                                              | <span data-ttu-id="46d30-144">レポートがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46d30-144">Indicates whether the report has been saved to disk.</span></span>                                                                                      |
| <span data-ttu-id="46d30-145">public void new(\[AnyType nameOrContainer\], \[AnyType container\])</span><span class="sxs-lookup"><span data-stu-id="46d30-145">public void new(\[AnyType nameOrContainer\], \[AnyType container\])</span></span> | <span data-ttu-id="46d30-146">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="46d30-146">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |
| <span data-ttu-id="46d30-147">public void dump()</span><span class="sxs-lookup"><span data-stu-id="46d30-147">public void dump()</span></span>                                                  | <span data-ttu-id="46d30-148">レポートの内容の概要を情報ログに記述します。</span><span class="sxs-lookup"><span data-stu-id="46d30-148">Writes an overview of the report's contents to the Infolog.</span></span>                                                                               |

## <a name="method-adddesign"></a><span data-ttu-id="46d30-149">メソッド addDesign</span><span class="sxs-lookup"><span data-stu-id="46d30-149">Method addDesign</span></span>

<span data-ttu-id="46d30-150">レポートが属している reportDesign を作成します。</span><span class="sxs-lookup"><span data-stu-id="46d30-150">Creates a reportDesign that belongs to a report.</span></span>

```xpp
public ReportDesign addDesign([str name], [container buffer])
```

### <a name="parameters---adddesign"></a><span data-ttu-id="46d30-151">パラメーター - addDesign</span><span class="sxs-lookup"><span data-stu-id="46d30-151">Parameters - addDesign</span></span>

<span data-ttu-id="46d30-152">名前</span><span class="sxs-lookup"><span data-stu-id="46d30-152">name</span></span>  
<span data-ttu-id="46d30-153">デザインでバッファで指定されたコンテンツを準備します。</span><span class="sxs-lookup"><span data-stu-id="46d30-153">Lets the design have the contents given by buffer.</span></span>

<!-- -->

<span data-ttu-id="46d30-154">バッファ</span><span class="sxs-lookup"><span data-stu-id="46d30-154">buffer</span></span>  
<span data-ttu-id="46d30-155">デザインでバッファで指定されたコンテンツを準備します。</span><span class="sxs-lookup"><span data-stu-id="46d30-155">Lets the design have the contents given by buffer.</span></span>

### <a name="return-value---adddesign"></a><span data-ttu-id="46d30-156">戻り値 - addDesign</span><span class="sxs-lookup"><span data-stu-id="46d30-156">Return Value - addDesign</span></span>

<span data-ttu-id="46d30-157">作成した reportDesign。</span><span class="sxs-lookup"><span data-stu-id="46d30-157">The created reportDesign.</span></span>

### <a name="remarks---adddesign"></a><span data-ttu-id="46d30-158">備考 - addDesign</span><span class="sxs-lookup"><span data-stu-id="46d30-158">Remarks - addDesign</span></span>

<span data-ttu-id="46d30-159">バッファ引数は、pack メソッドによって作成されたコンテナーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="46d30-159">The buffer argument can be a container created by the pack method.</span></span>

### <a name="examples---adddesign"></a><span data-ttu-id="46d30-160">例 - addDesign</span><span class="sxs-lookup"><span data-stu-id="46d30-160">Examples - addDesign</span></span>

<span data-ttu-id="46d30-161">このジョブは、別のデザインのコピーであるデザインを生成するために addDesign を使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="46d30-161">This job demonstrates how addDesign can be used to generate a design that is a copy of another design.</span></span>

```xpp
static void demoAddDesign(args a) 
{  
    report r1; 
    report r2; 
    reportDesign rd; 
    reportSection rs; 
    reportRun rr; 
    container c; 
    // Create a simple report r1. 
    r1 = new report(); 
    rd = r1.addDesign("Design1"); 
    rs = rd.addProgrammableSection(1); 
    rs.addTextControl("Hello world"); 
    c = rd.Pack(); // make a container containing r1's design 
    // Create a report r2 having a design that is a copy of r1's design. 
    r2 = new report(); 
    r2.AddDesign("design2", c); 
    // Run the report. 
    rr = new reportRun(r2, "design2"); 
    // Run the sysPrintForm form. 
    if (rr.prompt()) 
    { 
        // Execute the programableSection. 
        rr.execute(1);  
        // Print report to the target, such as printer or screen. 
        rr.print();    
    } 
}
```

## <a name="method-allowcheck"></a><span data-ttu-id="46d30-162">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="46d30-162">Method allowCheck</span></span>

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a><span data-ttu-id="46d30-163">パラメーター - allowCheck</span><span class="sxs-lookup"><span data-stu-id="46d30-163">Parameters - allowCheck</span></span>

<span data-ttu-id="46d30-164">値</span><span class="sxs-lookup"><span data-stu-id="46d30-164">value</span></span>  

### <a name="return-value---allowcheck"></a><span data-ttu-id="46d30-165">戻り値 - allowCheck</span><span class="sxs-lookup"><span data-stu-id="46d30-165">Return Value - allowCheck</span></span>

## <a name="method-autojoin"></a><span data-ttu-id="46d30-166">メソッド autoJoin</span><span class="sxs-lookup"><span data-stu-id="46d30-166">Method autoJoin</span></span>

```xpp
public boolean autoJoin([boolean value])
```

### <a name="parameters---autojoin"></a><span data-ttu-id="46d30-167">パラメーター - autoJoin</span><span class="sxs-lookup"><span data-stu-id="46d30-167">Parameters - autoJoin</span></span>

<span data-ttu-id="46d30-168">値</span><span class="sxs-lookup"><span data-stu-id="46d30-168">value</span></span>  

### <a name="return-value---autojoin"></a><span data-ttu-id="46d30-169">戻り値 - autoJoin</span><span class="sxs-lookup"><span data-stu-id="46d30-169">Return Value - autoJoin</span></span>

## <a name="method-changedby"></a><span data-ttu-id="46d30-170">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="46d30-170">Method changedBy</span></span>

<span data-ttu-id="46d30-171">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-171">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="46d30-172">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="46d30-172">Parameters - changedBy</span></span>

<span data-ttu-id="46d30-173">値</span><span class="sxs-lookup"><span data-stu-id="46d30-173">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="46d30-174">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="46d30-174">Return Value - changedBy</span></span>

<span data-ttu-id="46d30-175">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="46d30-175">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="46d30-176">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="46d30-176">Method changedDate</span></span>

<span data-ttu-id="46d30-177">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-177">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="46d30-178">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="46d30-178">Parameters - changedDate</span></span>

<span data-ttu-id="46d30-179">値</span><span class="sxs-lookup"><span data-stu-id="46d30-179">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="46d30-180">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="46d30-180">Return Value - changedDate</span></span>

<span data-ttu-id="46d30-181">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="46d30-181">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="46d30-182">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="46d30-182">Method changedTime</span></span>

<span data-ttu-id="46d30-183">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-183">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="46d30-184">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="46d30-184">Parameters - changedTime</span></span>

<span data-ttu-id="46d30-185">値</span><span class="sxs-lookup"><span data-stu-id="46d30-185">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="46d30-186">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="46d30-186">Return Value - changedTime</span></span>

<span data-ttu-id="46d30-187">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="46d30-187">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="46d30-188">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="46d30-188">Method createdBy</span></span>

<span data-ttu-id="46d30-189">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-189">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="46d30-190">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="46d30-190">Parameters - createdBy</span></span>

<span data-ttu-id="46d30-191">値</span><span class="sxs-lookup"><span data-stu-id="46d30-191">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="46d30-192">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="46d30-192">Return Value - createdBy</span></span>

<span data-ttu-id="46d30-193">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="46d30-193">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="46d30-194">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="46d30-194">Method creationDate</span></span>

<span data-ttu-id="46d30-195">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-195">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="46d30-196">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="46d30-196">Parameters - creationDate</span></span>

<span data-ttu-id="46d30-197">値</span><span class="sxs-lookup"><span data-stu-id="46d30-197">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="46d30-198">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="46d30-198">Return Value - creationDate</span></span>

<span data-ttu-id="46d30-199">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="46d30-199">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="46d30-200">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="46d30-200">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="46d30-201">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="46d30-201">Parameters - creationTime</span></span>

<span data-ttu-id="46d30-202">値</span><span class="sxs-lookup"><span data-stu-id="46d30-202">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="46d30-203">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="46d30-203">Return Value - creationTime</span></span>

## <a name="method-design"></a><span data-ttu-id="46d30-204">メソッド design</span><span class="sxs-lookup"><span data-stu-id="46d30-204">Method design</span></span>

<span data-ttu-id="46d30-205">既存のデザインを取得します。</span><span class="sxs-lookup"><span data-stu-id="46d30-205">Retrieves an existing design.</span></span>

```xpp
public ReportDesign design([str name])
```

### <a name="parameters---design"></a><span data-ttu-id="46d30-206">パラメーター - design</span><span class="sxs-lookup"><span data-stu-id="46d30-206">Parameters - design</span></span>

<span data-ttu-id="46d30-207">名前</span><span class="sxs-lookup"><span data-stu-id="46d30-207">name</span></span>  
<span data-ttu-id="46d30-208">返されるレポートの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46d30-208">The name of the report to be returned; optional.</span></span>

### <a name="return-value---design"></a><span data-ttu-id="46d30-209">戻り値 - design</span><span class="sxs-lookup"><span data-stu-id="46d30-209">Return Value - design</span></span>

<span data-ttu-id="46d30-210">指定した名前を持つデザイン、または見つからなかった場合は nullNothingnullptrunita null 参照 (Visual Basic にはない)。</span><span class="sxs-lookup"><span data-stu-id="46d30-210">The design that has the specified name, or nullNothingnullptrunita null reference (Nothing in Visual Basic) if it was not found.</span></span>

### <a name="remarks---design"></a><span data-ttu-id="46d30-211">備考 - design</span><span class="sxs-lookup"><span data-stu-id="46d30-211">Remarks - design</span></span>

<span data-ttu-id="46d30-212">引数が指定されず、レポートに 1 つのデザインのみ含まれている場合は、1 つのデザインを返します。</span><span class="sxs-lookup"><span data-stu-id="46d30-212">If no argument is supplied and the report only contains one design, the method returns the one design.</span></span>

### <a name="examples---design"></a><span data-ttu-id="46d30-213">例 - design</span><span class="sxs-lookup"><span data-stu-id="46d30-213">Examples - design</span></span>

```xpp
static void testDesign(args a) 
{ 
    report r; 
    reportDesign rd; 
    r = new report("Cust"); 
    rd = r.Design(); 
    if (rd) 
        print "a) r.design() : ", rd.Name(); 
    rd = r.Design(""); 
    if (rd) 
        print "b) r.design(emptyString) : ", rd.Name(); 
    rd = r.Design('customer'); 
    if (rd) 
        print "c) r.design(customer) : ", rd.Name(); 
    pause; 
}
```

## <a name="method-designcount"></a><span data-ttu-id="46d30-214">メソッド designCount</span><span class="sxs-lookup"><span data-stu-id="46d30-214">Method designCount</span></span>

<span data-ttu-id="46d30-215">特定のレポートのデザインの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="46d30-215">Retrieves the number of designs in a given report.</span></span>

```xpp
public int designCount()
```

### <a name="return-value---designcount"></a><span data-ttu-id="46d30-216">戻り値 - designCount</span><span class="sxs-lookup"><span data-stu-id="46d30-216">Return Value - designCount</span></span>

<span data-ttu-id="46d30-217">デザインの番号。</span><span class="sxs-lookup"><span data-stu-id="46d30-217">The number of designs.</span></span>

### <a name="examples---designcount"></a><span data-ttu-id="46d30-218">例 - designCount</span><span class="sxs-lookup"><span data-stu-id="46d30-218">Examples - designCount</span></span>

```xpp
static void testDesign(args a) 
{ 
    report r = new report(); 
    print "A newly created report has ", r.DesignCount(), " designs"; 
    pause; 
}
```

## <a name="method-designnumber"></a><span data-ttu-id="46d30-219">メソッド designNumber</span><span class="sxs-lookup"><span data-stu-id="46d30-219">Method designNumber</span></span>

<span data-ttu-id="46d30-220">既存のデザインを取得します。</span><span class="sxs-lookup"><span data-stu-id="46d30-220">Gets an existing design.</span></span>

```xpp
public ReportDesign designNumber([int number])
```

### <a name="parameters---designnumber"></a><span data-ttu-id="46d30-221">パラメーター - designNumber</span><span class="sxs-lookup"><span data-stu-id="46d30-221">Parameters - designNumber</span></span>

<span data-ttu-id="46d30-222">番号</span><span class="sxs-lookup"><span data-stu-id="46d30-222">number</span></span>  
<span data-ttu-id="46d30-223">希望するデザインを指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="46d30-223">An integer that specifies the desired design; optional.</span></span>

### <a name="return-value---designnumber"></a><span data-ttu-id="46d30-224">戻り値 - designNumber</span><span class="sxs-lookup"><span data-stu-id="46d30-224">Return Value - designNumber</span></span>

<span data-ttu-id="46d30-225">指定した reportDesign、またはデザインが存在しない場合は nullNothingnullptrunita null 参照 (Visual Basic にはない)。</span><span class="sxs-lookup"><span data-stu-id="46d30-225">The specified reportDesign, or nullNothingnullptrunita null reference (Nothing in Visual Basic) if the design did not exist.</span></span>

### <a name="remarks---designnumber"></a><span data-ttu-id="46d30-226">備考 - designNumber</span><span class="sxs-lookup"><span data-stu-id="46d30-226">Remarks - designNumber</span></span>

<span data-ttu-id="46d30-227">番号が &lt; 1 である場合は、デザイン 1 が返されます。</span><span class="sxs-lookup"><span data-stu-id="46d30-227">If number is &lt; 1, design 1 is returned.</span></span>

### <a name="examples---designnumber"></a><span data-ttu-id="46d30-228">例 - designNumber</span><span class="sxs-lookup"><span data-stu-id="46d30-228">Examples - designNumber</span></span>

```xpp
void testDesign(args a) 
{ 
    report r; 
    reportDesign rd; 
    int i; 
    r = new report("myReport"); 
    if (r.DesignCount() == 0) 
    { 
        print "The report has no designs"; pause; 
    } 
    for (i=1; i<=r.DesignCount();i++) 
    { 
        rd = r.DesignNumber(i); 
        print "Design No. ", i, " has name ", rd.Name(); 
    } 
    pause; 
}
```

## <a name="method-interactive"></a><span data-ttu-id="46d30-229">メソッド interactive</span><span class="sxs-lookup"><span data-stu-id="46d30-229">Method interactive</span></span>

```xpp
public boolean interactive([boolean value])
```

### <a name="parameters---interactive"></a><span data-ttu-id="46d30-230">パラメーター - interactive</span><span class="sxs-lookup"><span data-stu-id="46d30-230">Parameters - interactive</span></span>

<span data-ttu-id="46d30-231">値</span><span class="sxs-lookup"><span data-stu-id="46d30-231">value</span></span>  

### <a name="return-value---interactive"></a><span data-ttu-id="46d30-232">戻り値 - interactive</span><span class="sxs-lookup"><span data-stu-id="46d30-232">Return Value - interactive</span></span>

## <a name="method-name"></a><span data-ttu-id="46d30-233">メソッド名</span><span class="sxs-lookup"><span data-stu-id="46d30-233">Method name</span></span>

<span data-ttu-id="46d30-234">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46d30-234">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="46d30-235">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="46d30-235">Parameters - name</span></span>

<span data-ttu-id="46d30-236">値</span><span class="sxs-lookup"><span data-stu-id="46d30-236">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="46d30-237">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="46d30-237">Return Value - name</span></span>

<span data-ttu-id="46d30-238">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="46d30-238">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="46d30-239">備考 - name</span><span class="sxs-lookup"><span data-stu-id="46d30-239">Remarks - name</span></span>

<span data-ttu-id="46d30-240">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="46d30-240">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="46d30-241">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="46d30-241">Begins with a letter.</span></span>
-   <span data-ttu-id="46d30-242">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="46d30-242">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="46d30-243">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="46d30-243">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="46d30-244">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="46d30-244">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="46d30-245">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="46d30-245">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="46d30-246">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="46d30-246">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="46d30-247">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="46d30-247">Parameters - origin</span></span>

<span data-ttu-id="46d30-248">値</span><span class="sxs-lookup"><span data-stu-id="46d30-248">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="46d30-249">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="46d30-249">Return Value - origin</span></span>

## <a name="method-pack"></a><span data-ttu-id="46d30-250">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="46d30-250">Method pack</span></span>

<span data-ttu-id="46d30-251">Report クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="46d30-251">Serializes the current instance of the Report class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="46d30-252">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="46d30-252">Return Value - pack</span></span>

<span data-ttu-id="46d30-253">Report クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="46d30-253">A container that contains the current instance of the Report class.</span></span>

### <a name="remarks---pack"></a><span data-ttu-id="46d30-254">備考 - pack</span><span class="sxs-lookup"><span data-stu-id="46d30-254">Remarks - pack</span></span>

<span data-ttu-id="46d30-255">返されたコンテナーは、レポート コンストラクターの最初の引数として使用できます。</span><span class="sxs-lookup"><span data-stu-id="46d30-255">The returned container can be used as first argument to the report constructor.</span></span>

### <a name="examples---pack"></a><span data-ttu-id="46d30-256">例 - pack</span><span class="sxs-lookup"><span data-stu-id="46d30-256">Examples - pack</span></span>

<span data-ttu-id="46d30-257">次の例では、「cust」という名前のレポートをコンテナーに格納し、そのコンテナーでレポートを実行します (AOT のコンテナではありません)。</span><span class="sxs-lookup"><span data-stu-id="46d30-257">The following example stores a report named "cust" in a container and runs the report in the container (not the container in the AOT).</span></span>

```xpp
static void testReportPack(args a) 
{ 
    report r1; 
    report r2; 
    reportRun rr; 
    container c; 
    r1 = new report("cust"); 
    c = r1.Pack(); 
    r2 = new report(c); 
    rr = new reportrun(r2); 
    rr.Run(); 
}
```

## <a name="method-query"></a><span data-ttu-id="46d30-258">メソッド query</span><span class="sxs-lookup"><span data-stu-id="46d30-258">Method query</span></span>

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a><span data-ttu-id="46d30-259">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="46d30-259">Parameters - query</span></span>

<span data-ttu-id="46d30-260">クエリ</span><span class="sxs-lookup"><span data-stu-id="46d30-260">query</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="46d30-261">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="46d30-261">Return Value - query</span></span>

## <a name="method-saved"></a><span data-ttu-id="46d30-262">メソッド saved</span><span class="sxs-lookup"><span data-stu-id="46d30-262">Method saved</span></span>

<span data-ttu-id="46d30-263">レポートがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46d30-263">Indicates whether the report has been saved to disk.</span></span>

```xpp
public boolean saved()
```

### <a name="return-value---saved"></a><span data-ttu-id="46d30-264">戻り値 - saved</span><span class="sxs-lookup"><span data-stu-id="46d30-264">Return Value - saved</span></span>

<span data-ttu-id="46d30-265">レコードがディスクに保存されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46d30-265">true if the report has been saved to disc; otherwise false.</span></span>

### <a name="remarks---saved"></a><span data-ttu-id="46d30-266">備考 - saved</span><span class="sxs-lookup"><span data-stu-id="46d30-266">Remarks - saved</span></span>

<span data-ttu-id="46d30-267">AOT のレポートは、ディスクに保存されている場合にのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="46d30-267">A report in the AOT can only be run if it has been saved to disk.</span></span>

### <a name="examples---saved"></a><span data-ttu-id="46d30-268">例 - saved</span><span class="sxs-lookup"><span data-stu-id="46d30-268">Examples - saved</span></span>

```xpp
static void testReportSaved(args a) 
{ 
    report r; 
    reportRun rr; 
    r = new report(); 
    r.AddDesign(); 
    print "before save, saved : ", r.Saved(); pause; 
    r.saved(); 
    print "after save, saved : ", r.Saved(); pause; 
    rr = new reportrun(r); 
    rr.Run(); 
}
```

## <a name="method-new"></a><span data-ttu-id="46d30-269">メソッド new</span><span class="sxs-lookup"><span data-stu-id="46d30-269">Method new</span></span>

<span data-ttu-id="46d30-270">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="46d30-270">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new([AnyType nameOrContainer], [AnyType container])
```

### <a name="parameters---new"></a><span data-ttu-id="46d30-271">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="46d30-271">Parameters - new</span></span>

<span data-ttu-id="46d30-272">nameOrContainer</span><span class="sxs-lookup"><span data-stu-id="46d30-272">nameOrContainer</span></span>  

<!-- -->

<span data-ttu-id="46d30-273">コンテナー</span><span class="sxs-lookup"><span data-stu-id="46d30-273">container</span></span>  

### <a name="remarks---new"></a><span data-ttu-id="46d30-274">備考 - new</span><span class="sxs-lookup"><span data-stu-id="46d30-274">Remarks - new</span></span>

<span data-ttu-id="46d30-275">パラメーターの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="46d30-275">The parameter format is as follows:</span></span>

-   <span data-ttu-id="46d30-276">() � AOT 内に存在しないレポート オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="46d30-276">() � Creates a report object that is not present in the AOT.</span></span>
-   <span data-ttu-id="46d30-277">(c) � AOT には存在しないレポート オブジェクトを作成します。その内容はコンテナー c によって与えられます。</span><span class="sxs-lookup"><span data-stu-id="46d30-277">(c) � Creates a report object that is not present in the AOT, the contents of which are given by the container c.</span></span>
-   <span data-ttu-id="46d30-278">("existingReportName") � AOT 内にあるレポート オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="46d30-278">("existingReportName") � Retrieves a report object that is found in the AOT.</span></span>
-   <span data-ttu-id="46d30-279">("nonExistingReportName") � AOT 内でレポート オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="46d30-279">("nonExistingReportName") � Creates a report object in the AOT.</span></span>
-   <span data-ttu-id="46d30-280">("nonExistingReportName", c) � AOT 内でレポート オブジェクトを作成します。内容はコンテナ c によって与えられます。</span><span class="sxs-lookup"><span data-stu-id="46d30-280">("nonExistingReportName", c) � Creates a report object in the AOT, the contents of which are given by the container c.</span></span>

<span data-ttu-id="46d30-281">コンテナー c は、pack メソッドで作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46d30-281">The container c should be created by the pack method.</span></span>

## <a name="method-dump"></a><span data-ttu-id="46d30-282">メソッド dump</span><span class="sxs-lookup"><span data-stu-id="46d30-282">Method dump</span></span>

<span data-ttu-id="46d30-283">レポートの内容の概要を情報ログに記述します。</span><span class="sxs-lookup"><span data-stu-id="46d30-283">Writes an overview of the report's contents to the Infolog.</span></span>

```xpp
public void dump()
```

### <a name="remarks---dump"></a><span data-ttu-id="46d30-284">備考 - dump</span><span class="sxs-lookup"><span data-stu-id="46d30-284">Remarks - dump</span></span>

<span data-ttu-id="46d30-285">情報ログに書き込まれる行は、AOT でレポートを展開するときに表示される情報と同じです。</span><span class="sxs-lookup"><span data-stu-id="46d30-285">The lines written to the Infolog are identical to the information shown when you expand the report in the AOT.</span></span>

### <a name="examples---dump"></a><span data-ttu-id="46d30-286">例 - dump</span><span class="sxs-lookup"><span data-stu-id="46d30-286">Examples - dump</span></span>

```xpp
static void testReportDump(args a) 
{ 
    report r = new report("cust"); 
    r.Dump(); 
}
```

