---
title: カスタマイズ分析のレポート (CAR)
description: この記事では、モデルのカスタマイズ分析レポートを生成する方法について説明します。 また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 49681
ms.assetid: 540b08dd-9af7-42fc-aa0c-ba04af1f8002
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 094fcb40aa4f501a2b1cb13191424d36544a20de
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408895"
---
# <a name="customization-analysis-report-car"></a><span data-ttu-id="7f098-104">カスタマイズ分析のレポート (CAR)</span><span class="sxs-lookup"><span data-stu-id="7f098-104">Customization Analysis Report (CAR)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f098-105">この記事では、モデルのカスタマイズ分析レポートを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f098-105">This article describes how to generate a Customization Analysis Report for your model.</span></span> <span data-ttu-id="7f098-106">また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。</span><span class="sxs-lookup"><span data-stu-id="7f098-106">It also describes some best practice rules that are included in the report, and provides suggestions for fixing errors and warnings that are associated with these rules.</span></span> 

## <a name="what-is-the-customization-analysis-report"></a><span data-ttu-id="7f098-107">カスタマイズ分析レポートとは</span><span class="sxs-lookup"><span data-stu-id="7f098-107">What is the Customization Analysis Report?</span></span>

<span data-ttu-id="7f098-108">カスタマイズ分析レポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行するツールです。</span><span class="sxs-lookup"><span data-stu-id="7f098-108">The Customization Analysis Report is a tool that analyzes your customization and extension models, and runs a predefined set of best practice rules.</span></span> <span data-ttu-id="7f098-109">このレポートは、ソリューション認証プロセスの要件の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="7f098-109">The report is one of the requirements of the solution certification process.</span></span> <span data-ttu-id="7f098-110">レポートは、Microsoft Excel のブック形式です。</span><span class="sxs-lookup"><span data-stu-id="7f098-110">The report is in the form of a Microsoft Excel workbook.</span></span>

## <a name="how-to-generate-the-report"></a><span data-ttu-id="7f098-111">レポートを生成する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-111">How to generate the report</span></span>
<span data-ttu-id="7f098-112">カスタマイズ分析レポートを生成するには、開発環境で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f098-112">To generate the Customization Analysis Report, run the following command in a development environment.</span></span>

```Console
xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>
```

### <a name="example"></a><span data-ttu-id="7f098-113">例</span><span class="sxs-lookup"><span data-stu-id="7f098-113">Example</span></span>

```Console
xppbp.exe -metadata=C:\Packages -all -model="MyAppSuiteCustomizations" -xmlLog=C:\temp\BPCheckLogcd.xml -module="ApplicationSuite" -car=c:\temp\CAReport.xlsx
```

<span data-ttu-id="7f098-114">xppbp.exe ツール、c:\\packages\\bin または I:\\AosService\\PackagesLocalDirectory\\bin にあります。</span><span class="sxs-lookup"><span data-stu-id="7f098-114">The xppbp.exe tool is located in c:\\packages\\bin or I:\\AosService\\PackagesLocalDirectory\\bin.</span></span>

## <a name="issues-list"></a><span data-ttu-id="7f098-115">問題リスト</span><span class="sxs-lookup"><span data-stu-id="7f098-115">Issues List</span></span>
<span data-ttu-id="7f098-116">このセクションでは、レポートの **問題リスト** ページに表示されるベスト プラクティスのルール (エラー、警告、または情報メッセージ) をすべて説明し、問題を解決するための提案を示します。</span><span class="sxs-lookup"><span data-stu-id="7f098-116">This section describes all best practice rules (errors, warnings, or informational messages) that can appear on the **Issues List** page of the report and provides suggestions for fixing the issues.</span></span> <span data-ttu-id="7f098-117">**メタデータ** または **コード** の型の問題です。</span><span class="sxs-lookup"><span data-stu-id="7f098-117">Issues are of the **metadata** or **code** type.</span></span> <span data-ttu-id="7f098-118">すべての **コード** 問題に関しては、重ねたメソッドで警告またはエラーが発生する場合、ルールに違反しているコードの明細行は下位レイヤーのモデルに属していることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="7f098-118">For all **code** issues, keep in mind that, if the warning or error occurs in a method that you've overlaid, the lines of code that violate the rule might belong to a model in a lower layer.</span></span> <span data-ttu-id="7f098-119">その場合、自分のものではないコードの警告やエラーを修正する責任はありません。</span><span class="sxs-lookup"><span data-stu-id="7f098-119">In that case, you're not responsible for fixing warnings and errors in code that isn't yours.</span></span>

### <a name="bpcheckpackreturnsconnull"></a><span data-ttu-id="7f098-120">BPCheckPackReturnsConnull</span><span class="sxs-lookup"><span data-stu-id="7f098-120">BPCheckPackReturnsConnull</span></span>

| <span data-ttu-id="7f098-121">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-121">Description</span></span>         | <span data-ttu-id="7f098-122">このルールは、**SysPackable** インターフェイスを実装するすべてのクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-122">This rule applies to all classes that implement the **SysPackable** interface.</span></span> <span data-ttu-id="7f098-123">これは、**Pack** メソッドが **Connull()** を返さないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f098-123">It makes sure that the **Pack** method doesn't return **Connull()**.</span></span> |
|---------------------|-------------------------------------|
| <span data-ttu-id="7f098-124">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-124">Error message</span></span>       | <span data-ttu-id="7f098-125">コンテナー パック メソッドは、Runbase 派生クラスで connull を返します</span><span class="sxs-lookup"><span data-stu-id="7f098-125">Container pack method returns connull in a Runbase derived class</span></span>                |
| <span data-ttu-id="7f098-126">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-126">Issue type/severity</span></span> | <span data-ttu-id="7f098-127">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-127">Code/Warning</span></span>  |
| <span data-ttu-id="7f098-128">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-128">How to fix it</span></span>       | <span data-ttu-id="7f098-129">該当する場合、**Pack** メソッドの戻り値を更新するか、**Super()** を返します。</span><span class="sxs-lookup"><span data-stu-id="7f098-129">Update the return value of the **Pack** method, or return **Super()** when applicable.</span></span>                 |

### <a name="bpcheckparametersmodified"></a><span data-ttu-id="7f098-130">BPCheckParametersModified</span><span class="sxs-lookup"><span data-stu-id="7f098-130">BPCheckParametersModified</span></span>

| <span data-ttu-id="7f098-131">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-131">Description</span></span>         | <span data-ttu-id="7f098-132">メソッドのパラメーターがメソッド内で変更された場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-132">This rule fails if a parameter of a method is modified inside a method.</span></span>                      |
|---------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f098-133">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-133">Error message</span></span>       | <span data-ttu-id="7f098-134">メソッド %1 のパラメーター 1% がメソッド内で変更されています</span><span class="sxs-lookup"><span data-stu-id="7f098-134">Parameter 1% in method %1 are modified inside the method</span></span>                                     |
| <span data-ttu-id="7f098-135">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-135">Issue type/severity</span></span> | <span data-ttu-id="7f098-136">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-136">Code/Warning</span></span>                                                                                 |
| <span data-ttu-id="7f098-137">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-137">How to fix it</span></span>       | <span data-ttu-id="7f098-138">コードをリファクターします。</span><span class="sxs-lookup"><span data-stu-id="7f098-138">Refactor your code.</span></span> <span data-ttu-id="7f098-139">呼び出されたメソッド内ではなく、呼び出し元によりパラメーターを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f098-139">Parameters must be modified by the caller, not within the called method.</span></span> |

### <a name="bpchecksqlcode"></a><span data-ttu-id="7f098-140">BPCheckSQLCode</span><span class="sxs-lookup"><span data-stu-id="7f098-140">BPCheckSQLCode</span></span>

| <span data-ttu-id="7f098-141">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-141">Description</span></span>         | <span data-ttu-id="7f098-142">このルールは、X++ コードに直接 SQL コードが含まれていると失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-142">This rule fails if your X++ code contains direct SQL code.</span></span>       |
|---------------------|------------------------------------------------------------------|
| <span data-ttu-id="7f098-143">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-143">Error message</span></span>       | <span data-ttu-id="7f098-144">メソッド %1 に SQL コードが見つかりました</span><span class="sxs-lookup"><span data-stu-id="7f098-144">SQL code found in method %1</span></span>                                      |
| <span data-ttu-id="7f098-145">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-145">Issue type/severity</span></span> | <span data-ttu-id="7f098-146">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-146">Code/Warning</span></span>                                                     |
| <span data-ttu-id="7f098-147">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-147">How to fix it</span></span>       | <span data-ttu-id="7f098-148">X++ を使用してデータベースにアクセスするコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="7f098-148">Refactor your code to use X++ to access the database.</span></span> |

### <a name="bpchecknestedloopincode"></a><span data-ttu-id="7f098-149">BPCheckNestedLoopInCode</span><span class="sxs-lookup"><span data-stu-id="7f098-149">BPCheckNestedLoopInCode</span></span>

| <span data-ttu-id="7f098-150">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-150">Description</span></span>         | <span data-ttu-id="7f098-151">このルールは、**select** ループがループ内にネストされていることを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-151">This rule fails if it finds a **while select** loop nested within a loop.</span></span>    |
|---------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="7f098-152">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-152">Error message</span></span>       | <span data-ttu-id="7f098-153">%1 メソッドに入れ子になったデータ アクセス ループが見つかりました</span><span class="sxs-lookup"><span data-stu-id="7f098-153">Nested data access loop found in %1 method</span></span>                                                |
| <span data-ttu-id="7f098-154">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-154">Issue type/severity</span></span> | <span data-ttu-id="7f098-155">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-155">Code/Warning</span></span>                   |
| <span data-ttu-id="7f098-156">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-156">How to fix it</span></span>       | <span data-ttu-id="7f098-157">入れ子になったデータ アクセス ループの代わりに結合を使うコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="7f098-157">Refactor your code to use joins instead of nested data access loops.</span></span> <span data-ttu-id="7f098-158">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</span><span class="sxs-lookup"><span data-stu-id="7f098-158">If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span> |

### <a name="bpcheckinsertmethodinloop"></a><span data-ttu-id="7f098-159">BPCheckInsertMethodInLoop</span><span class="sxs-lookup"><span data-stu-id="7f098-159">BPCheckInsertMethodInLoop</span></span>

| <span data-ttu-id="7f098-160">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-160">Description</span></span>         | <span data-ttu-id="7f098-161">このルールは、ループの中に入れ子されたメソッド **insert** への呼び出しを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-161">This rules fails if it finds a call to the method **insert** nested inside a loop.</span></span> <span data-ttu-id="7f098-162">**InsertRecordList** を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7f098-162">We recommend that you use **InsertRecordList**.</span></span> <span data-ttu-id="7f098-163">このルールは、InMemory テーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="7f098-163">This rule doesn't apply to InMemory tables.</span></span> |
|---------------------|-------------------------------|
| <span data-ttu-id="7f098-164">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-164">Error message</span></span>       | <span data-ttu-id="7f098-165">メソッド %1 で、Insert メソッドを RecordInsertList に置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="7f098-165">Insert method can be replaced with RecordInsertList in method %1</span></span>                       |
| <span data-ttu-id="7f098-166">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-166">Issue type/severity</span></span> | <span data-ttu-id="7f098-167">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-167">Code/Warning</span></span>           |
| <span data-ttu-id="7f098-168">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-168">How to fix it</span></span>       | <span data-ttu-id="7f098-169">**InsertRecordList** など、設定に基づく操作を使用するコードをリファクターします。</span><span class="sxs-lookup"><span data-stu-id="7f098-169">Refactor your code to use set-based operations, such as **InsertRecordList**.</span></span>            |

### <a name="bpcheckselectwithjoin"></a><span data-ttu-id="7f098-170">BPCheckSelectwithJoin</span><span class="sxs-lookup"><span data-stu-id="7f098-170">BPCheckSelectwithJoin</span></span>

| <span data-ttu-id="7f098-171">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-171">Description</span></span>         | <span data-ttu-id="7f098-172">結合されていない入れ子になった **select** ステートメントが見つかった場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-172">This rule fails if it finds nested **select** statements that aren't joined.</span></span>  |
|---------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7f098-173">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-173">Error message</span></span>       | <span data-ttu-id="7f098-174">%1 メソッドの入れ子になった select ステートメントは結合できます。</span><span class="sxs-lookup"><span data-stu-id="7f098-174">Nested select statement in %1 method can be joined</span></span>                                |
| <span data-ttu-id="7f098-175">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-175">Issue type/severity</span></span> | <span data-ttu-id="7f098-176">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-176">Code/Warning</span></span>                                                                          |
| <span data-ttu-id="7f098-177">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-177">How to fix it</span></span>       | <span data-ttu-id="7f098-178">入れ子になった **select** ステートメントの代わりに結合を使うコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="7f098-178">Refactor your code to use joins instead of a nested **select** statement.</span></span> <span data-ttu-id="7f098-179">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</span><span class="sxs-lookup"><span data-stu-id="7f098-179">If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span> |

### <a name="bpfunctioncallwithselect"></a><span data-ttu-id="7f098-180">BPFunctionCallwithSelect</span><span class="sxs-lookup"><span data-stu-id="7f098-180">BPFunctionCallwithSelect</span></span>

| <span data-ttu-id="7f098-181">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-181">Description</span></span>         | <span data-ttu-id="7f098-182">このルールは、**select** ステートメント内で関数呼び出しが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-182">This rule fails if a function call is found within a **select** statement.</span></span>   |
|---------------------|------------------|
| <span data-ttu-id="7f098-183">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-183">Error message</span></span>       | <span data-ttu-id="7f098-184">メソッド %1 の select ステートメントに、関数呼び出しが見つかりました</span><span class="sxs-lookup"><span data-stu-id="7f098-184">Function call found in select statement in method %1</span></span>     |
| <span data-ttu-id="7f098-185">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-185">Issue type/severity</span></span> | <span data-ttu-id="7f098-186">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-186">Code/Warning</span></span>    |
| <span data-ttu-id="7f098-187">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-187">How to fix it</span></span>       | <span data-ttu-id="7f098-188">**選択** ステートメントを呼び出す前に、関数の戻り値をローカル変数へと割り当て、**選択** ステートメントでローカル変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f098-188">Assign the function's return value to a local variable before you call the **select** statement, and use the local variable in the **select** statement.</span></span> |

### <a name="bpcheckinvalidexecutequery"></a><span data-ttu-id="7f098-189">BPCheckinvalidExecuteQuery</span><span class="sxs-lookup"><span data-stu-id="7f098-189">BPCheckinvalidExecuteQuery</span></span>

| <span data-ttu-id="7f098-190">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-190">Description</span></span>         | <span data-ttu-id="7f098-191">このルールは、**ExecuteQuery** メソッドで **super()** を呼び出した後に **addRange** への呼び出しが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-191">This rule fails if a call to **addRange** is found after a call to **super()** in the **ExecuteQuery** method.</span></span> |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="7f098-192">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-192">Error message</span></span>       | <span data-ttu-id="7f098-193">フォーム %1 の ExecuteQuery メソッドに、super() の後に add range を追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="7f098-193">Add range after super() should not be added in ExecuteQuery method for form %1</span></span>               |
| <span data-ttu-id="7f098-194">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-194">Issue type/severity</span></span> | <span data-ttu-id="7f098-195">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-195">Code/Warning</span></span>                                          |
| <span data-ttu-id="7f098-196">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-196">How to fix it</span></span>       | <span data-ttu-id="7f098-197">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="7f098-197">Refactor your code to avoid this pattern.</span></span>             |

### <a name="bpcheckinvalidinitformmethod"></a><span data-ttu-id="7f098-198">BPCheckInvalidInitFormMethod</span><span class="sxs-lookup"><span data-stu-id="7f098-198">BPCheckInvalidInitFormMethod</span></span>

| <span data-ttu-id="7f098-199">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-199">Description</span></span>         | <span data-ttu-id="7f098-200">このルールは、**super()** を呼び出す前にフォームの **init** メソッドでフォーム コントロールとデータソースを初期化しないようにします。</span><span class="sxs-lookup"><span data-stu-id="7f098-200">This rule makes sure that you don't initialize form controls and data sources in a form's **init** method before you call **super()**.</span></span> <span data-ttu-id="7f098-201">**element** または **this** を **super()** に対する呼び出し (**this.aMethod()** または **element.aMethod()**) の前に使用するステートメントが検出された場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-201">It fails if it finds a statement that uses **element** or **this** before the call to **super()** (**this.aMethod()** or **element.aMethod()**).</span></span> <span data-ttu-id="7f098-202">情報メッセージは番号順序の初期化など許可されたいくつかのパターンのみを表示します (**numberSeqPreInit**) 。</span><span class="sxs-lookup"><span data-stu-id="7f098-202">An informational message is shown only for some allowed patterns, such as initializing number sequences (**numberSeqPreInit**).</span></span> |
|---------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f098-203">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-203">Error message</span></span>       | <span data-ttu-id="7f098-204">フォーム要素ステートメントは、フォーム %1 の init メソッドで、super() の前に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="7f098-204">Form element statements should not be used before super() in init method of form %1</span></span>      |
| <span data-ttu-id="7f098-205">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-205">Issue type/severity</span></span> | <span data-ttu-id="7f098-206">コード/情報または警告</span><span class="sxs-lookup"><span data-stu-id="7f098-206">Code/Info or Warning</span></span>                                   |
| <span data-ttu-id="7f098-207">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-207">How to fix it</span></span>       | <span data-ttu-id="7f098-208">**super()** の呼び出し後、コードをリファクターしてフォーム コントロールおよびデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7f098-208">Refactor your code to access form controls and data after the call to **super()**.</span></span> <span data-ttu-id="7f098-209">コードが任意のフォーム コントロールを初期化せず、**super()** の前にどのフォーム データ ソースにもアクセスしない場合、Microsoft にカスタマイズ分析のレポートを送信するときに例外をまとめます。</span><span class="sxs-lookup"><span data-stu-id="7f098-209">If your code doesn't initialize any form control and doesn't access any form data sources before **super()**, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span>   |

### <a name="bpcheckemptyloop"></a><span data-ttu-id="7f098-210">BPCheckEmptyLoop</span><span class="sxs-lookup"><span data-stu-id="7f098-210">BPCheckEmptyLoop</span></span>

| <span data-ttu-id="7f098-211">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-211">Description</span></span>         | <span data-ttu-id="7f098-212">このルールは、ステートメントがないループを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-212">This rule fails if it finds loops that have no statements.</span></span> |
|---------------------|------------------------------------------------------------|
| <span data-ttu-id="7f098-213">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-213">Error message</span></span>       | <span data-ttu-id="7f098-214">クラス %2 の メソッド %1 で空のループが見つかりました</span><span class="sxs-lookup"><span data-stu-id="7f098-214">Empty loop found in method %1 in class %2</span></span>                  |
| <span data-ttu-id="7f098-215">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-215">Issue type/severity</span></span> | <span data-ttu-id="7f098-216">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-216">Code/Warning</span></span>                                               |
| <span data-ttu-id="7f098-217">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-217">How to fix it</span></span>       | <span data-ttu-id="7f098-218">ループをコードから削除します。</span><span class="sxs-lookup"><span data-stu-id="7f098-218">Remove the loop from your code.</span></span>                            |

### <a name="bpchecklockqueryrange"></a><span data-ttu-id="7f098-219">BPCheckLockQueryRange</span><span class="sxs-lookup"><span data-stu-id="7f098-219">BPCheckLockQueryRange</span></span>

| <span data-ttu-id="7f098-220">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-220">Description</span></span>         | <span data-ttu-id="7f098-221">フォームの **init** メソッドでコードが **AddRange** を呼び出し、その範囲をロックまたは非表示として設定しないと、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-221">This rule fails if the code calls **AddRange** in the **init** method of the form, and doesn't set the range as locked or hidden.</span></span>      |
|---------------------|-------------------------------------------|
| <span data-ttu-id="7f098-222">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-222">Error message</span></span>       | <span data-ttu-id="7f098-223">フォーム %1で、範囲はロックするか、非表示にする必要があります</span><span class="sxs-lookup"><span data-stu-id="7f098-223">Range should be locked or hidden in form %1</span></span>    |
| <span data-ttu-id="7f098-224">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-224">Issue type/severity</span></span> | <span data-ttu-id="7f098-225">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-225">Code/Warning</span></span>     |
| <span data-ttu-id="7f098-226">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-226">How to fix it</span></span>       | <span data-ttu-id="7f098-227">**AddRange** の呼び出しの後に、**QueryBuildRange.status(RangeStatus::Locked)** または **QueryBuildRange.status(RangeStatus::Hidden)** を追加します。</span><span class="sxs-lookup"><span data-stu-id="7f098-227">Add **QueryBuildRange.status(RangeStatus::Locked)** or **QueryBuildRange.status(RangeStatus::Hidden)** after the call to **AddRange**.</span></span> |

### <a name="bpcheckskipstatementvalidation"></a><span data-ttu-id="7f098-228">BPCheckSkipStatementValidation</span><span class="sxs-lookup"><span data-stu-id="7f098-228">BPCheckSkipStatementValidation</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f098-229">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-229">Description</span></span></td>
<td><span data-ttu-id="7f098-230">このルールは、<strong>Skip</strong> ステートメントを持たないセットベースの操作を検出した場合に通知メッセージを報告します。</span><span class="sxs-lookup"><span data-stu-id="7f098-230">This rule reports an informational message if it finds a set-based operation that doesn&#39;t have <strong>Skip</strong> statements.</span></span>
<ul>
<li><span data-ttu-id="7f098-231"><strong>update_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="7f098-231">When <strong>update_recordset</strong> is found, the rule checks for <strong>skipDataMethods(true)</strong>.</span></span> <span data-ttu-id="7f098-232">テーブルの <strong>update</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-232">The rule applies only when the <strong>update</strong> method on the table is overridden.</span></span></li>
<li><span data-ttu-id="7f098-233"><strong>insert_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="7f098-233">When <strong>insert_recordset</strong> is found, the rule checks for <strong>skipDataMethods(true)</strong>.</span></span> <span data-ttu-id="7f098-234">テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-234">The rule applies only when the <strong>insert</strong> method on the table is overridden.</span></span></li>
<li><span data-ttu-id="7f098-235"><strong>delete_from</strong> が見つかると、ルールによって <strong>skipDeleteActions(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="7f098-235">When <strong>delete_from</strong> is found, the rule checks for <strong>skipDeleteActions(true)</strong>.</span></span> <span data-ttu-id="7f098-236">テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-236">The rule applies only when the <strong>insert</strong> method on the table is overridden.</span></span></li>
</ul>
<span data-ttu-id="7f098-237">これは、セットベースの操作のパフォーマンス向上を最大限に活用するために、<strong>スキップ</strong>メソッドを呼び出す必要があることを示す情報メッセージです。</span><span class="sxs-lookup"><span data-stu-id="7f098-237">This is an informational message that highlights the need to call <strong>skip</strong> methods to take full advantage of the performance gains of set-based operations.</span></span> <span data-ttu-id="7f098-238"><strong>スキップ</strong>  メソッドが使用されていない場合は、実行は行ごとの操作に戻ります。</span><span class="sxs-lookup"><span data-stu-id="7f098-238">If <strong>skip</strong> methods are not used, the execution falls back to a row-by-row operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-239">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-239">Error message</span></span></td>
<td><span data-ttu-id="7f098-240">セット ベースの操作はクラス %2 のメソッド %1 で Skip ステートメントを呼び出す必要があります。それ以外の場合、行ごとの操作にフォールバックされます。</span><span class="sxs-lookup"><span data-stu-id="7f098-240">Set-based operation must invoke Skip statements in method %1 in class %2; otherwise, execution will fall back to a row by row operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f098-241">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-241">Issue type/severity</span></span></td>
<td><span data-ttu-id="7f098-242">コード/情報</span><span class="sxs-lookup"><span data-stu-id="7f098-242">Code/Information</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-243">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-243">How to fix it</span></span></td>
<td><span data-ttu-id="7f098-244">該当する場合は、<strong>skipDataMethods(true)</strong> または <strong>skipDeleteActions(true)</strong> を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f098-244">Use <strong>skipDataMethods(true)</strong> or <strong>skipDeleteActions(true)</strong> when applicable.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpchecknottstryblock"></a><span data-ttu-id="7f098-245">BPCheckNoTTSTryBlock</span><span class="sxs-lookup"><span data-stu-id="7f098-245">BPCheckNoTTSTryBlock</span></span>

| <span data-ttu-id="7f098-246">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-246">Description</span></span> | <span data-ttu-id="7f098-247">このルールは、正しく処理されない <strong>tts</strong> ブロック内の <strong>try</strong> ステートメントを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-247">This rule fails if it finds a <strong>try</strong> statement within a <strong>tts</strong> block that isn&#39;t handled correctly.</span></span> |
|---|---|
| <span data-ttu-id="7f098-248">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-248">Error message</span></span> | <span data-ttu-id="7f098-249">try 文の tts ブロックは、メソッド %1 の例外を明示的にキャッチしません。</span><span class="sxs-lookup"><span data-stu-id="7f098-249">Tts block with Try statement does not explicitly catch exceptions in method %1</span></span> |
| <span data-ttu-id="7f098-250">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-250">Issue type/severity</span></span> | <span data-ttu-id="7f098-251">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-251">Code/Warning</span></span> |
| <span data-ttu-id="7f098-252">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-252">How to fix it</span></span> | <span data-ttu-id="7f098-253">この表に続くコードの例を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f098-253">Use the code example that follows this table.</span></span> |

<span data-ttu-id="7f098-254">次の例では、ルールが失敗するか、合格するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="7f098-254">The following examples show when the rule will fail or pass.</span></span> <span data-ttu-id="7f098-255">次の例を参考にして、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="7f098-255">Use these examples as guidelines to refactor your code.</span></span>

```xpp
ttsbegin;
try {
}
// fail
catch {
}
try {
}
// pass
catch(Exception::UpdateConflict) {
}
try {
}
// pass
catch(Exception::UpdateConflictNotRecovered) {}
```

### <a name="bpcheckemptytablemethod"></a><span data-ttu-id="7f098-256">BPCheckEmptyTableMethod</span><span class="sxs-lookup"><span data-stu-id="7f098-256">BPCheckEmptyTableMethod</span></span>

| <span data-ttu-id="7f098-257">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-257">Description</span></span>         | <span data-ttu-id="7f098-258">このルールは、ソース コードのないテーブル メソッドをチェックします。</span><span class="sxs-lookup"><span data-stu-id="7f098-258">This rule checks for table methods that have no source code.</span></span> <span data-ttu-id="7f098-259">空テーブルのメソッドは、テーブルのレコードセット オペレーションを行単位の操作に戻す原因となります。</span><span class="sxs-lookup"><span data-stu-id="7f098-259">Empty table methods cause record-set operations on the table to fall back to a row-by-row operation.</span></span> |
|---------------------|-------------------------------------------|
| <span data-ttu-id="7f098-260">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-260">Error message</span></span>       | <span data-ttu-id="7f098-261">%1 テーブルに空の %2 メソッドがあります</span><span class="sxs-lookup"><span data-stu-id="7f098-261">%1 table has an empty %2 method</span></span>           |
| <span data-ttu-id="7f098-262">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-262">Issue type/severity</span></span> | <span data-ttu-id="7f098-263">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-263">Code/Warning</span></span>                              |
| <span data-ttu-id="7f098-264">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-264">How to fix it</span></span>       | <span data-ttu-id="7f098-265">このメソッドをコードから削除します。</span><span class="sxs-lookup"><span data-stu-id="7f098-265">Remove this method from your code.</span></span>        |

### <a name="bpcheckbatchjobsenabled"></a><span data-ttu-id="7f098-266">BPCheckBatchJobsEnabled</span><span class="sxs-lookup"><span data-stu-id="7f098-266">BPCheckBatchJobsEnabled</span></span>

| <span data-ttu-id="7f098-267">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-267">Description</span></span>         | <span data-ttu-id="7f098-268">このルールは、**RunBaseBatch** を拡張するすべてのクラスが **true** を返す **canGoBatch** メソッドを持つことを保証します。</span><span class="sxs-lookup"><span data-stu-id="7f098-268">This rule makes sure that all classes that extend **RunBaseBatch** have a **canGoBatch** method that returns **true**.</span></span> |
|---------------------|----------------------------------------------------------------|
| <span data-ttu-id="7f098-269">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-269">Error message</span></span>       | <span data-ttu-id="7f098-270">カスタム ジョブがクラス %1 でバッチ対応でありません</span><span class="sxs-lookup"><span data-stu-id="7f098-270">Custom job is not batch-enabled in class %1</span></span>         |
| <span data-ttu-id="7f098-271">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-271">Issue type/severity</span></span> | <span data-ttu-id="7f098-272">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-272">Code/Warning</span></span>       |
| <span data-ttu-id="7f098-273">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-273">How to fix it</span></span>       | <span data-ttu-id="7f098-274">**canGoBatch** メソッドは、すべてのバッチ クラスに **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="7f098-274">The **canGoBatch** method must return **true** for all batch classes.</span></span>     |

### <a name="bpcheckdisplaymethodcached"></a><span data-ttu-id="7f098-275">BPCheckDisplayMethodCached</span><span class="sxs-lookup"><span data-stu-id="7f098-275">BPCheckDisplayMethodCached</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f098-276">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-276">Description</span></span></td>
<td><span data-ttu-id="7f098-277">データ メソッドにバインドされている各コントロールについては、これらの条件のいずれかが満たされている場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-277">For each control that is bound to a data method, this rules fails if one of these conditions is met:</span></span>
<ul>
<li><span data-ttu-id="7f098-278"><strong>データのキャッシュ方法</strong>プロパティが<strong>自動</strong>に設定され、対応するテーブルの <strong>display</strong>/<strong>edit</strong> メソッドには <strong>SysClientCacheDataMethodAttribute</strong> がなく、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</span><span class="sxs-lookup"><span data-stu-id="7f098-278">The <strong>Cache Data Method</strong> property is set to <strong>Auto</strong>, the corresponding table <strong>display</strong>/<strong>edit</strong> method doesn&#39;t have the <strong>SysClientCacheDataMethodAttribute</strong>, and the <strong>init</strong> method of the data source doesn&#39;t use <strong>CacheAddMethod</strong>.</span></span></li>
<li><span data-ttu-id="7f098-279"><strong>データのキャッシュ方法</strong> プロパティは <strong>いいえ</strong> に設定され、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</span><span class="sxs-lookup"><span data-stu-id="7f098-279">The <strong>Cache Data Method</strong> property is set to <strong>No</strong>, and the <strong>init</strong> method of the data source doesn&#39;t use <strong>CacheAddMethod</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-280">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-280">Error message</span></span></td>
<td><span data-ttu-id="7f098-281">フォーム %2 の 表示メソッド %1 がキャッシュされていません</span><span class="sxs-lookup"><span data-stu-id="7f098-281">Display method %1 in form %2 not cached</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f098-282">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-282">Issue type/severity</span></span></td>
<td><span data-ttu-id="7f098-283">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-283">Code/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-284">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-284">How to fix it</span></span></td>
<td><span data-ttu-id="7f098-285">この表に続くメモを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f098-285">Use the note that follows this table.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7f098-286">この警告は、次のいずれかのパターンを使用して修正することができます。</span><span class="sxs-lookup"><span data-stu-id="7f098-286">You can fix this warning by using one of the following patterns:</span></span>

+ <span data-ttu-id="7f098-287">**キャッシュ データ メソッド** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f098-287">Set the **Cache Data Method** property to **Yes**.</span></span>
+ <span data-ttu-id="7f098-288">**キャッシュ データ メソッド** プロパティを **自動** に設定し、**SysClientCacheDataMethodAttribute** 属性を使用してテーブルのデータ メソッドをマークします。</span><span class="sxs-lookup"><span data-stu-id="7f098-288">Set the **Cache Data Method** property to **Auto**, and mark the data method of the table with the **SysClientCacheDataMethodAttribute** attribute.</span></span> <span data-ttu-id="7f098-289">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7f098-289">Here is an example.</span></span>

    ```xp
    [SysClientCacheDataMethodAttribute(true)]
    Display TransDate myDateMethod()
    {
        //...
    }
    ```

+ <span data-ttu-id="7f098-290">フォームの **init** メソッドで **CacheAddMethod** を使用すると、そのメソッドをキャッシュ済みとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="7f098-290">Use **CacheAddMethod** in the **init** method of the form to mark the method as cached.</span></span>

### <a name="bpchecksqlqueryininit"></a><span data-ttu-id="7f098-291">BPCheckSQLQueryInInit</span><span class="sxs-lookup"><span data-stu-id="7f098-291">BPCheckSQLQueryInInit</span></span>

| <span data-ttu-id="7f098-292">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-292">Description</span></span>         | <span data-ttu-id="7f098-293">このルールは、フォームの **init** メソッドで **while** ループを持つデータ アクセス クエリが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-293">This rule fails if a data access query that has a **while** loop is found in the **init** method of a form.</span></span> <span data-ttu-id="7f098-294">このパターンは、フォームの初期化時にパフォーマンスの問題を引き起こす場合があります。</span><span class="sxs-lookup"><span data-stu-id="7f098-294">This pattern could cause performance issues when the form is initialized.</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="7f098-295">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-295">Error message</span></span>       | <span data-ttu-id="7f098-296">フォーム %1 の init メソッドで、while ループを持つ SQL クエリが見つかりました</span><span class="sxs-lookup"><span data-stu-id="7f098-296">SQL query with while loop was found in init method of form %1</span></span>            |
| <span data-ttu-id="7f098-297">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-297">Issue type/severity</span></span> | <span data-ttu-id="7f098-298">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-298">Code/Warning</span></span>   |
| <span data-ttu-id="7f098-299">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-299">How to fix it</span></span>       | <span data-ttu-id="7f098-300">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="7f098-300">Refactor your code to avoid this pattern.</span></span>  |

### <a name="bpchecknewquerywithform"></a><span data-ttu-id="7f098-301">BPCheckNewQueryWithForm</span><span class="sxs-lookup"><span data-stu-id="7f098-301">BPCheckNewQueryWithForm</span></span>

| <span data-ttu-id="7f098-302">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-302">Description</span></span>         | <span data-ttu-id="7f098-303">このルールは、フォームの **init** または **executeQuery** メソッドで **new Query()** ステートメントを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-303">This rule fails if it finds the **new Query()** statement in the **init** or **executeQuery** method of a form.</span></span> |
|---------------------|--------------------------------------------------|
| <span data-ttu-id="7f098-304">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-304">Error message</span></span>       | <span data-ttu-id="7f098-305">フォーム メソッド %1 で、データ ソース クエリが上書きされます</span><span class="sxs-lookup"><span data-stu-id="7f098-305">Data source query overridden in form method %1</span></span>      |
| <span data-ttu-id="7f098-306">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-306">Issue type/severity</span></span> | <span data-ttu-id="7f098-307">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-307">Code/Warning</span></span>                                |
| <span data-ttu-id="7f098-308">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-308">How to fix it</span></span>       | <span data-ttu-id="7f098-309">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="7f098-309">Refactor your code to avoid this pattern.</span></span>            |

### <a name="bpcheckselectforupdateabsent"></a><span data-ttu-id="7f098-310">BPCheckSelectForUpdateAbsent</span><span class="sxs-lookup"><span data-stu-id="7f098-310">BPCheckSelectForUpdateAbsent</span></span>

| <span data-ttu-id="7f098-311">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-311">Description</span></span>         | <span data-ttu-id="7f098-312">**Select ForUpdate** を使用してレコードを選択したが、更新が実行されていない場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-312">This rule fails if **Select ForUpdate** is used to select records, but an update isn't being performed.</span></span> <span data-ttu-id="7f098-313">このルールは、オプティミスティック同時実行制御 (OCC) が有効になっているテーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="7f098-313">This rules doesn't apply to tables that are enabled for Optimistic Concurrency Control (OCC).</span></span> |
|---------------------|------------------|
| <span data-ttu-id="7f098-314">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-314">Error message</span></span>       | <span data-ttu-id="7f098-315">メソッド %1 に Select ForUpdate が実装されていません</span><span class="sxs-lookup"><span data-stu-id="7f098-315">Select ForUpdate not implemented in method %1</span></span>   |
| <span data-ttu-id="7f098-316">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-316">Issue type/severity</span></span> | <span data-ttu-id="7f098-317">コード/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-317">Code/Warning</span></span>      |
| <span data-ttu-id="7f098-318">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-318">How to fix it</span></span>       | <span data-ttu-id="7f098-319">**ForUpdate を選択** の代わりに **選択** を使用するか、**OCC を有効** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f098-319">Use **Select** instead of **Select ForUpdate**, or set the **OCC Enabled** property to **Yes** on the table.</span></span>                                                                                          |

### <a name="bpchecktablepropertymismatch"></a><span data-ttu-id="7f098-320">BPCheckTablePropertyMismatch</span><span class="sxs-lookup"><span data-stu-id="7f098-320">BPCheckTablePropertyMismatch</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f098-321">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-321">Description</span></span></td>
<td><span data-ttu-id="7f098-322">このルールは、テーブルがテーブル グループに属しているが、適切な<strong>キャッシュ ルックアップ</strong>値を持たない場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-322">This rule fails when the table belongs to a table group but doesn&#39;t have the appropriate <strong>Cache Lookup</strong> value.</span></span> <span data-ttu-id="7f098-323">次の条件がすべて満たされていると、ルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-323">The rule fails if one of these conditions is met:</span></span>
<ul>
<li><span data-ttu-id="7f098-324"><strong>テーブル グループ</strong> プロパティは <strong>メイン</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> または <strong>EntireTable</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-324">The <strong>Table Group</strong> property is set to <strong>Main</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>NotinTTS</strong> or <strong>EntireTable</strong>.</span></span></li>
<li><span data-ttu-id="7f098-325"><strong>テーブル グループ</strong> プロパティは <strong>グループ</strong> または <strong>パラメーター</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-325">The <strong>Table Group</strong> property is set to <strong>Group</strong> or <strong>Parameter</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>NotinTTS</strong>.</span></span></li>
<li><span data-ttu-id="7f098-326"><strong>テーブル グループ</strong> プロパティは <strong>WorksheetHeader</strong>、<strong>WorksheetLine</strong>、または <strong>Transaction</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>Found</strong>、<strong>FoundAndEmpty</strong>、または <strong>EntireTable</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-326">The <strong>Table Group</strong> property is set to <strong>WorksheetHeader</strong>, <strong>WorksheetLine</strong>, or <strong>Transaction</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>Found</strong>, <strong>FoundAndEmpty</strong>, or <strong>EntireTable</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-327">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-327">Error message</span></span></td>
<td><span data-ttu-id="7f098-328">%1 テーブルにテーブル グループとキャッシュ ルックアップの無効な組み合わせがあります</span><span class="sxs-lookup"><span data-stu-id="7f098-328">%1 table has an invalid combination of table group and cache lookup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f098-329">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-329">Issue type/severity</span></span></td>
<td><span data-ttu-id="7f098-330">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-330">MetaData/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-331">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-331">How to fix it</span></span></td>
<td><span data-ttu-id="7f098-332">テーブルで適切な <strong>キャッシュ ルックアップ</strong> 値を設定します。</span><span class="sxs-lookup"><span data-stu-id="7f098-332">Set an appropriate <strong>Cache Lookup</strong> value on the table.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpcheckmissingdeleteactions"></a><span data-ttu-id="7f098-333">BPCheckMissingDeleteActions</span><span class="sxs-lookup"><span data-stu-id="7f098-333">BPCheckMissingDeleteActions</span></span>

| <span data-ttu-id="7f098-334">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-334">Description</span></span>         | <span data-ttu-id="7f098-335">このルールは、テーブル関係の **削除** アクションまたは **削除時** プロパティの値が **なし** と等しくないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="7f098-335">This rule validates that the value of either a **delete** action or the **On Delete** property of a table relation isn't equal to **None**.</span></span> <span data-ttu-id="7f098-336">関連するテーブルまたは現在のテーブルが tempDB、メモリ テーブル、参照テーブル、ステージング テーブル、パラメーター テーブルの場合、ルールはトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="7f098-336">The rule isn't triggered when the related or current table is a tempDB, in memory table, reference table, staging table, or parameter table.</span></span> |
|---------------------|---------------------------------------------------|
| <span data-ttu-id="7f098-337">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-337">Error message</span></span>       | <span data-ttu-id="7f098-338">リレーション名 %3 でテーブル %2 に関連付けられているテーブル %1 に欠けているアクションを削除します</span><span class="sxs-lookup"><span data-stu-id="7f098-338">Delete actions missing in table %1 which is related to table %2 with relation name %3</span></span>      |
| <span data-ttu-id="7f098-339">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-339">Issue type/severity</span></span> | <span data-ttu-id="7f098-340">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-340">MetaData/Warning</span></span>   |
| <span data-ttu-id="7f098-341">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-341">How to fix it</span></span>       | <span data-ttu-id="7f098-342">**None** と等しくない **delete** アクションを設定します。</span><span class="sxs-lookup"><span data-stu-id="7f098-342">Set a **delete** action value that isn't equal to **None**.</span></span> |

### <a name="bpcheckaddressmodel"></a><span data-ttu-id="7f098-343">BPCheckAddressModel</span><span class="sxs-lookup"><span data-stu-id="7f098-343">BPCheckAddressModel</span></span>

| <span data-ttu-id="7f098-344">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-344">Description</span></span>         | <span data-ttu-id="7f098-345">テーブル フィールドが **AddressZipCodeId** または **AddressStateId** タイプの場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-345">This rule fails if a table field is of the **AddressZipCodeId** or **AddressStateId** type.</span></span> <span data-ttu-id="7f098-346">これらのタイプは、コードが新しいアドレス フレームワークを受け入れなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7f098-346">These types indicate that the code didn't uptake the newer Address framework.</span></span> |
|---------------------|-------------------------|
| <span data-ttu-id="7f098-347">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-347">Error message</span></span>       | <span data-ttu-id="7f098-348">テーブル %2 のフィールド %1 は、アドレスの場所モデルの一部ではありません</span><span class="sxs-lookup"><span data-stu-id="7f098-348">Field %1 of table %2 is not part of address location model</span></span>   |
| <span data-ttu-id="7f098-349">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-349">Issue type/severity</span></span> | <span data-ttu-id="7f098-350">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-350">MetaData/Warning</span></span>  |
| <span data-ttu-id="7f098-351">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-351">How to fix it</span></span>       | <span data-ttu-id="7f098-352">これらのタイプをディレクトリ モデルのその他の適切な EDT タイプに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="7f098-352">Replace these types with any other appropriate EDT type in the Directory model.</span></span>        |

### <a name="bpcheckdimensionmodel"></a><span data-ttu-id="7f098-353">BPCheckDimensionModel</span><span class="sxs-lookup"><span data-stu-id="7f098-353">BPCheckDimensionModel</span></span>

| <span data-ttu-id="7f098-354">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-354">Description</span></span>         | <span data-ttu-id="7f098-355">テーブル フィールドが、**分析コード** または **LedgerAccount** タイプの場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-355">This rule fails if a table field is of the **Dimension** or **LedgerAccount** type.</span></span> <span data-ttu-id="7f098-356">これらのタイプは、コードが新しい財務分析コード フレームワークを受け入れなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7f098-356">These types indicate that the code didn't uptake the newer Financial Dimension framework.</span></span> |
|---------------------|----------|
| <span data-ttu-id="7f098-357">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-357">Error message</span></span>       | <span data-ttu-id="7f098-358">テーブル %2 のフィールド %1 は、財務分析コード フレームワークの一部ではありません</span><span class="sxs-lookup"><span data-stu-id="7f098-358">Field %1 of table %2 is not part of financial dimension framework</span></span>               |
| <span data-ttu-id="7f098-359">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-359">Issue type/severity</span></span> | <span data-ttu-id="7f098-360">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-360">MetaData/Warning</span></span>   |
| <span data-ttu-id="7f098-361">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-361">How to fix it</span></span>       | <span data-ttu-id="7f098-362">これらのタイプを分析コード モデルのその他の適切な EDT タイプに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="7f098-362">Replace these types with any other appropriate EDT type in the Dimensions model.</span></span>       |

### <a name="bpchecknumberofnewfields"></a><span data-ttu-id="7f098-363">BPCheckNumberofNewFields</span><span class="sxs-lookup"><span data-stu-id="7f098-363">BPCheckNumberofNewFields</span></span>

| <span data-ttu-id="7f098-364">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-364">Description</span></span>         | <span data-ttu-id="7f098-365">このルールは、そのテーブルのカスタマイズまたは拡張のプロセスで、テーブルに 10 個以下のフィールドが追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f098-365">This rule verifies that no more than 10 fields were added to a table during the process of customizing or extending that table.</span></span> <span data-ttu-id="7f098-366">このルールは、ステージング テーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="7f098-366">This rule doesn't apply to staging tables.</span></span> |
|---------------------|-------------------------------------|
| <span data-ttu-id="7f098-367">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-367">Error message</span></span>       | <span data-ttu-id="7f098-368">次の値より大きいテーブル %1 の新しいフィールドの数</span><span class="sxs-lookup"><span data-stu-id="7f098-368">Number of new fields in table %1 is greater than</span></span>      |
| <span data-ttu-id="7f098-369">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-369">Issue type/severity</span></span> | <span data-ttu-id="7f098-370">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-370">Metadata/Warning</span></span>   |
| <span data-ttu-id="7f098-371">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-371">How to fix it</span></span>       | <span data-ttu-id="7f098-372">スキーマをリファクタリングし、既存のテーブルに多数のフィールドを追加する代わりに関連するテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f098-372">Refactor your schema and create related tables instead of adding too many fields to an existing table.</span></span> |

### <a name="bpcheckenumupgradeissue"></a><span data-ttu-id="7f098-373">BPCheckEnumUpgradeIssue</span><span class="sxs-lookup"><span data-stu-id="7f098-373">BPCheckEnumUpgradeIssue</span></span>

| <span data-ttu-id="7f098-374">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-374">Description</span></span>         | <span data-ttu-id="7f098-375">このルールは、次の条件が満たされた場合に失敗します。列挙型 (オーバーレイ) をカスタマイズすると、新しい列挙型の値は既存の最大値 + 10 未満になります。</span><span class="sxs-lookup"><span data-stu-id="7f098-375">This rule fails when the following condition is met: When you customize an enum (overlayer), new enum values are less than the maximum existing value + 10.</span></span> <span data-ttu-id="7f098-376">このルールは、拡張可能な列挙型には適用されません。</span><span class="sxs-lookup"><span data-stu-id="7f098-376">This rules doesn't apply to extensible enums.</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="7f098-377">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-377">Error message</span></span>       | <span data-ttu-id="7f098-378">列挙 %1 で、アップグレード問題があります。</span><span class="sxs-lookup"><span data-stu-id="7f098-378">Enum %1 will have upgrade issues</span></span>    |
| <span data-ttu-id="7f098-379">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-379">Issue type/severity</span></span> | <span data-ttu-id="7f098-380">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-380">MetaData/Warning</span></span>       |
| <span data-ttu-id="7f098-381">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-381">How to fix it</span></span>       | <span data-ttu-id="7f098-382">大きな列挙値を使用するか、列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="7f098-382">Use larger enum values, or extend the enum.</span></span>       |

### <a name="bpcheckpassivejoinuse"></a><span data-ttu-id="7f098-383">BPCheckPassiveJoinUse</span><span class="sxs-lookup"><span data-stu-id="7f098-383">BPCheckPassiveJoinUse</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f098-384">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-384">Description</span></span></td>
<td><span data-ttu-id="7f098-385">このルールは、フォームがデータのプリロードを許可する場合、タブ ページ データソースのリンク タイプがパッシブであることを検証します。</span><span class="sxs-lookup"><span data-stu-id="7f098-385">This rule validates that, when a form allows for pre-loading of data, the link type of tab page data sources is passive.</span></span> <span data-ttu-id="7f098-386">次の条件がすべて満たされていると、ルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7f098-386">The rule fails if all the following conditions are met:</span></span>
<ul>
<li><span data-ttu-id="7f098-387"><strong>Yes</strong> に設定された <strong>AllowPreLoading</strong> プロパティのフォームがあります。</span><span class="sxs-lookup"><span data-stu-id="7f098-387">A form has the <strong>AllowPreLoading</strong> property set to <strong>Yes</strong>.</span></span></li>
<li><span data-ttu-id="7f098-388">フォームのタブ ページは、最上位レベルのデータ ソースにバインドされています。</span><span class="sxs-lookup"><span data-stu-id="7f098-388">A tab page on the form is bound to a top-level data source.</span></span></li>
<li><span data-ttu-id="7f098-389">データ ソースの<strong>結合ソース</strong>プロパティが設定されます。</span><span class="sxs-lookup"><span data-stu-id="7f098-389">The data source's <strong>Join Source </strong>property is set.</span></span></li>
<li><span data-ttu-id="7f098-390">データ ソースの <strong>リンク タイプ</strong> プロパティが <strong>パッシブ</strong> に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="7f098-390">The data source's <strong>Link Type</strong> property isn&#39;t set to <strong>Passive</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-391">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-391">Error message</span></span></td>
<td><span data-ttu-id="7f098-392">新しいメッセージは、「フォームの %2 タブ ページ コントロールにバインドされたデータソース %1 でパッシブ結合を使用する」 ことを提案しています</span><span class="sxs-lookup"><span data-stu-id="7f098-392">New message suggest: "Use passive joins on data sources %1 bound to a tab page control in form %2"</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f098-393">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-393">Issue type/severity</span></span></td>
<td><span data-ttu-id="7f098-394">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-394">MetaData/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f098-395">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-395">How to fix it</span></span></td>
<td><span data-ttu-id="7f098-396">フォームで <strong>AllowPreLoading</strong> プロパティを <strong>いいえ</strong> に設定するか、データ ソースでパッシブ結合を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f098-396">Set the <strong>AllowPreLoading</strong> property to <strong>No</strong> on the form, or use passive joins on the data source.</span></span> <span data-ttu-id="7f098-397">パッシブ結合では、タブ ページのクエリの実行時に明示的にプログラミングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f098-397">Passive joins require that you explicitly program when the query of a tab page is run.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpcheckalternatekeyabsent"></a><span data-ttu-id="7f098-398">BPCheckAlternateKeyAbsent</span><span class="sxs-lookup"><span data-stu-id="7f098-398">BPCheckAlternateKeyAbsent</span></span>

| <span data-ttu-id="7f098-399">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-399">Description</span></span>         | <span data-ttu-id="7f098-400">このルールは、一意のインデックスを持つテーブルに少なくとも 1 つの代替キーがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f098-400">This rule verifies that tables that have a unique index have at least one alternate key.</span></span> |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f098-401">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-401">Error message</span></span>       | <span data-ttu-id="7f098-402">テーブル %1 には、代替キーがありません</span><span class="sxs-lookup"><span data-stu-id="7f098-402">Table %1 does not have an alternate key</span></span>                                                  |
| <span data-ttu-id="7f098-403">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-403">Issue type/severity</span></span> | <span data-ttu-id="7f098-404">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-404">MetaData/Warning</span></span>                                                                         |
| <span data-ttu-id="7f098-405">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-405">How to fix it</span></span>       | <span data-ttu-id="7f098-406">テーブルの一意のインデックスで **代替キー** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f098-406">Set the **Alternate Key** property to **Yes** on a unique index of the table.</span></span>            |

### <a name="bpcheckbasetablemodified"></a><span data-ttu-id="7f098-407">BPCheckBaseTableModified</span><span class="sxs-lookup"><span data-stu-id="7f098-407">BPCheckBaseTableModified</span></span>

| <span data-ttu-id="7f098-408">説明</span><span class="sxs-lookup"><span data-stu-id="7f098-408">Description</span></span>         | <span data-ttu-id="7f098-409">このルールは、Microsoft によって出荷される特定のベース テーブルの一覧のカスタマイズ (オーバーレイ化) を推奨しません。</span><span class="sxs-lookup"><span data-stu-id="7f098-409">This rule discourages the customization (overlayering) of a list of specific base tables that are shipped by Microsoft.</span></span> <span data-ttu-id="7f098-410">例では、SourceDocumentHeader および SourceDocumentLine テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="7f098-410">Examples are the SourceDocumentHeader and SourceDocumentLine tables.</span></span> |
|---------------------|----------------------------|
| <span data-ttu-id="7f098-411">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="7f098-411">Error message</span></span>       | <span data-ttu-id="7f098-412">%1 はベース テーブルであり、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="7f098-412">%1 is a base table and must not be modified</span></span>   |
| <span data-ttu-id="7f098-413">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="7f098-413">Issue type/severity</span></span> | <span data-ttu-id="7f098-414">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="7f098-414">MetaData/Warning</span></span>     |
| <span data-ttu-id="7f098-415">修正する方法</span><span class="sxs-lookup"><span data-stu-id="7f098-415">How to fix it</span></span>       | <span data-ttu-id="7f098-416">テーブルをカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="7f098-416">Don't customize the table.</span></span>    |
