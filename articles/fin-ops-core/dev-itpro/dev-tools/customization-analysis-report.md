---
title: カスタマイズ分析のレポート (CAR)
description: このトピックでは、モデルのカスタマイズ分析のレポートを生成する方法について説明し、レポートに含まれるいくつかのベスト プラクティス ルールについて説明します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 49681
ms.assetid: 540b08dd-9af7-42fc-aa0c-ba04af1f8002
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b46ccb9f1705c8528e2a1ed50068dc9230ba4cb
ms.sourcegitcommit: e9b078cea2d7953fe4efaa065480cc9e5befbec8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2021
ms.locfileid: "6277243"
---
# <a name="customization-analysis-report-car"></a><span data-ttu-id="6df9f-103">カスタマイズ分析のレポート (CAR)</span><span class="sxs-lookup"><span data-stu-id="6df9f-103">Customization Analysis Report (CAR)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6df9f-104">このトピックでは、モデルのカスタマイズ分析レポートを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-104">This topic describes how to generate a Customization Analysis Report for your model.</span></span> <span data-ttu-id="6df9f-105">また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-105">It also describes some best practice rules that are included in the report, and provides suggestions for fixing errors and warnings that are associated with these rules.</span></span> 

## <a name="what-is-the-customization-analysis-report"></a><span data-ttu-id="6df9f-106">カスタマイズ分析レポートとは</span><span class="sxs-lookup"><span data-stu-id="6df9f-106">What is the Customization Analysis Report?</span></span>

<span data-ttu-id="6df9f-107">カスタマイズ分析レポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行するツールです。</span><span class="sxs-lookup"><span data-stu-id="6df9f-107">The Customization Analysis Report is a tool that analyzes your customization and extension models, and runs a predefined set of best practice rules.</span></span> <span data-ttu-id="6df9f-108">このレポートは、ソリューション認証プロセスの要件の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="6df9f-108">The report is one of the requirements of the solution certification process.</span></span> <span data-ttu-id="6df9f-109">レポートは、Microsoft Excel のブック形式です。</span><span class="sxs-lookup"><span data-stu-id="6df9f-109">The report is in the form of a Microsoft Excel workbook.</span></span>

## <a name="how-to-generate-the-report"></a><span data-ttu-id="6df9f-110">レポートを生成する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-110">How to generate the report</span></span>
<span data-ttu-id="6df9f-111">xppbp.exe ツール、c:\\packages\\bin または I:\\AosService\\PackagesLocalDirectory\\bin にあります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-111">The xppbp.exe tool is located in c:\\packages\\bin or I:\\AosService\\PackagesLocalDirectory\\bin.</span></span>
<span data-ttu-id="6df9f-112">カスタマイズ分析レポートを生成するには、開発環境で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-112">To generate the Customization Analysis Report, run the following command in a development environment.</span></span>

```Console
xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>
```

### <a name="example"></a><span data-ttu-id="6df9f-113">例</span><span class="sxs-lookup"><span data-stu-id="6df9f-113">Example</span></span>

```Console
xppbp.exe -metadata=C:\Packages -all -model="MyAppSuiteCustomizations" -xmlLog=C:\temp\BPCheckLogcd.xml -module="ApplicationSuite" -car=c:\temp\CAReport.xlsx
```


## <a name="issues-list"></a><span data-ttu-id="6df9f-114">問題リスト</span><span class="sxs-lookup"><span data-stu-id="6df9f-114">Issues List</span></span>
<span data-ttu-id="6df9f-115">このセクションでは、レポートの **問題リスト** ページに表示されるベスト プラクティスのルール (エラー、警告、または情報メッセージ) をすべて説明し、問題を解決するための提案を示します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-115">This section describes all best practice rules (errors, warnings, or informational messages) that can appear on the **Issues List** page of the report and provides suggestions for fixing the issues.</span></span> <span data-ttu-id="6df9f-116">**メタデータ** または **コード** の型の問題です。</span><span class="sxs-lookup"><span data-stu-id="6df9f-116">Issues are of the **metadata** or **code** type.</span></span> <span data-ttu-id="6df9f-117">すべての **コード** 問題に関しては、重ねたメソッドで警告またはエラーが発生する場合、ルールに違反しているコードの明細行は下位レイヤーのモデルに属していることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="6df9f-117">For all **code** issues, keep in mind that, if the warning or error occurs in a method that you've overlaid, the lines of code that violate the rule might belong to a model in a lower layer.</span></span> <span data-ttu-id="6df9f-118">その場合、自分のものではないコードの警告やエラーを修正する責任はありません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-118">In that case, you're not responsible for fixing warnings and errors in code that isn't yours.</span></span>

### <a name="bpcheckpackreturnsconnull"></a><span data-ttu-id="6df9f-119">BPCheckPackReturnsConnull</span><span class="sxs-lookup"><span data-stu-id="6df9f-119">BPCheckPackReturnsConnull</span></span>

| <span data-ttu-id="6df9f-120">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-120">Description</span></span>         | <span data-ttu-id="6df9f-121">このルールは、**SysPackable** インターフェイスを実装するすべてのクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-121">This rule applies to all classes that implement the **SysPackable** interface.</span></span> <span data-ttu-id="6df9f-122">これは、**Pack** メソッドが **Connull()** を返さないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-122">It makes sure that the **Pack** method doesn't return **Connull()**.</span></span> |
|---------------------|-------------------------------------|
| <span data-ttu-id="6df9f-123">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-123">Error message</span></span>       | <span data-ttu-id="6df9f-124">コンテナー パック メソッドは、Runbase 派生クラスで connull を返します</span><span class="sxs-lookup"><span data-stu-id="6df9f-124">Container pack method returns connull in a Runbase derived class</span></span>                |
| <span data-ttu-id="6df9f-125">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-125">Issue type/severity</span></span> | <span data-ttu-id="6df9f-126">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-126">Code/Warning</span></span>  |
| <span data-ttu-id="6df9f-127">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-127">How to fix it</span></span>       | <span data-ttu-id="6df9f-128">該当する場合、**Pack** メソッドの戻り値を更新するか、**Super()** を返します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-128">Update the return value of the **Pack** method, or return **Super()** when applicable.</span></span>                 |

### <a name="bpcheckparametersmodified"></a><span data-ttu-id="6df9f-129">BPCheckParametersModified</span><span class="sxs-lookup"><span data-stu-id="6df9f-129">BPCheckParametersModified</span></span>

| <span data-ttu-id="6df9f-130">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-130">Description</span></span>         | <span data-ttu-id="6df9f-131">メソッドのパラメーターがメソッド内で変更された場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-131">This rule fails if a parameter of a method is modified inside a method.</span></span>                      |
|---------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df9f-132">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-132">Error message</span></span>       | <span data-ttu-id="6df9f-133">メソッド %1 のパラメーター 1% がメソッド内で変更されています</span><span class="sxs-lookup"><span data-stu-id="6df9f-133">Parameter 1% in method %1 are modified inside the method</span></span>                                     |
| <span data-ttu-id="6df9f-134">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-134">Issue type/severity</span></span> | <span data-ttu-id="6df9f-135">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-135">Code/Warning</span></span>                                                                                 |
| <span data-ttu-id="6df9f-136">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-136">How to fix it</span></span>       | <span data-ttu-id="6df9f-137">コードをリファクターします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-137">Refactor your code.</span></span> <span data-ttu-id="6df9f-138">呼び出されたメソッド内ではなく、呼び出し元によりパラメーターを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-138">Parameters must be modified by the caller, not within the called method.</span></span> |

### <a name="bpchecksqlcode"></a><span data-ttu-id="6df9f-139">BPCheckSQLCode</span><span class="sxs-lookup"><span data-stu-id="6df9f-139">BPCheckSQLCode</span></span>

| <span data-ttu-id="6df9f-140">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-140">Description</span></span>         | <span data-ttu-id="6df9f-141">このルールは、X++ コードに直接 SQL コードが含まれていると失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-141">This rule fails if your X++ code contains direct SQL code.</span></span>       |
|---------------------|------------------------------------------------------------------|
| <span data-ttu-id="6df9f-142">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-142">Error message</span></span>       | <span data-ttu-id="6df9f-143">メソッド %1 に SQL コードが見つかりました</span><span class="sxs-lookup"><span data-stu-id="6df9f-143">SQL code found in method %1</span></span>                                      |
| <span data-ttu-id="6df9f-144">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-144">Issue type/severity</span></span> | <span data-ttu-id="6df9f-145">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-145">Code/Warning</span></span>                                                     |
| <span data-ttu-id="6df9f-146">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-146">How to fix it</span></span>       | <span data-ttu-id="6df9f-147">X++ を使用してデータベースにアクセスするコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-147">Refactor your code to use X++ to access the database.</span></span> |

### <a name="bpchecknestedloopincode"></a><span data-ttu-id="6df9f-148">BPCheckNestedLoopInCode</span><span class="sxs-lookup"><span data-stu-id="6df9f-148">BPCheckNestedLoopInCode</span></span>

| <span data-ttu-id="6df9f-149">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-149">Description</span></span>         | <span data-ttu-id="6df9f-150">このルールは、**select** ループがループ内にネストされていることを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-150">This rule fails if it finds a **while select** loop nested within a loop.</span></span>    |
|---------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="6df9f-151">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-151">Error message</span></span>       | <span data-ttu-id="6df9f-152">%1 メソッドに入れ子になったデータ アクセス ループが見つかりました</span><span class="sxs-lookup"><span data-stu-id="6df9f-152">Nested data access loop found in %1 method</span></span>                                                |
| <span data-ttu-id="6df9f-153">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-153">Issue type/severity</span></span> | <span data-ttu-id="6df9f-154">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-154">Code/Warning</span></span>                   |
| <span data-ttu-id="6df9f-155">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-155">How to fix it</span></span>       | <span data-ttu-id="6df9f-156">入れ子になったデータ アクセス ループの代わりに結合を使うコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-156">Refactor your code to use joins instead of nested data access loops.</span></span> <span data-ttu-id="6df9f-157">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-157">If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span> |

### <a name="bpcheckinsertmethodinloop"></a><span data-ttu-id="6df9f-158">BPCheckInsertMethodInLoop</span><span class="sxs-lookup"><span data-stu-id="6df9f-158">BPCheckInsertMethodInLoop</span></span>

| <span data-ttu-id="6df9f-159">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-159">Description</span></span>         | <span data-ttu-id="6df9f-160">このルールは、ループの中に入れ子されたメソッド **insert** への呼び出しを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-160">This rules fails if it finds a call to the method **insert** nested inside a loop.</span></span> <span data-ttu-id="6df9f-161">**InsertRecordList** を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-161">We recommend that you use **InsertRecordList**.</span></span> <span data-ttu-id="6df9f-162">このルールは、InMemory テーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-162">This rule doesn't apply to InMemory tables.</span></span> |
|---------------------|-------------------------------|
| <span data-ttu-id="6df9f-163">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-163">Error message</span></span>       | <span data-ttu-id="6df9f-164">メソッド %1 で、Insert メソッドを RecordInsertList に置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-164">Insert method can be replaced with RecordInsertList in method %1</span></span>                       |
| <span data-ttu-id="6df9f-165">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-165">Issue type/severity</span></span> | <span data-ttu-id="6df9f-166">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-166">Code/Warning</span></span>           |
| <span data-ttu-id="6df9f-167">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-167">How to fix it</span></span>       | <span data-ttu-id="6df9f-168">**InsertRecordList** など、設定に基づく操作を使用するコードをリファクターします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-168">Refactor your code to use set-based operations, such as **InsertRecordList**.</span></span>            |

### <a name="bpcheckselectwithjoin"></a><span data-ttu-id="6df9f-169">BPCheckSelectwithJoin</span><span class="sxs-lookup"><span data-stu-id="6df9f-169">BPCheckSelectwithJoin</span></span>

| <span data-ttu-id="6df9f-170">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-170">Description</span></span>         | <span data-ttu-id="6df9f-171">結合されていない入れ子になった **select** ステートメントが見つかった場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-171">This rule fails if it finds nested **select** statements that aren't joined.</span></span>  |
|---------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6df9f-172">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-172">Error message</span></span>       | <span data-ttu-id="6df9f-173">%1 メソッドの入れ子になった select ステートメントは結合できます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-173">Nested select statement in %1 method can be joined</span></span>                                |
| <span data-ttu-id="6df9f-174">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-174">Issue type/severity</span></span> | <span data-ttu-id="6df9f-175">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-175">Code/Warning</span></span>                                                                          |
| <span data-ttu-id="6df9f-176">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-176">How to fix it</span></span>       | <span data-ttu-id="6df9f-177">入れ子になった **select** ステートメントの代わりに結合を使うコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-177">Refactor your code to use joins instead of a nested **select** statement.</span></span> <span data-ttu-id="6df9f-178">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-178">If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span> |

### <a name="bpfunctioncallwithselect"></a><span data-ttu-id="6df9f-179">BPFunctionCallwithSelect</span><span class="sxs-lookup"><span data-stu-id="6df9f-179">BPFunctionCallwithSelect</span></span>

| <span data-ttu-id="6df9f-180">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-180">Description</span></span>         | <span data-ttu-id="6df9f-181">このルールは、**select** ステートメント内で関数呼び出しが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-181">This rule fails if a function call is found within a **select** statement.</span></span>   |
|---------------------|------------------|
| <span data-ttu-id="6df9f-182">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-182">Error message</span></span>       | <span data-ttu-id="6df9f-183">メソッド %1 の select ステートメントに、関数呼び出しが見つかりました</span><span class="sxs-lookup"><span data-stu-id="6df9f-183">Function call found in select statement in method %1</span></span>     |
| <span data-ttu-id="6df9f-184">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-184">Issue type/severity</span></span> | <span data-ttu-id="6df9f-185">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-185">Code/Warning</span></span>    |
| <span data-ttu-id="6df9f-186">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-186">How to fix it</span></span>       | <span data-ttu-id="6df9f-187">**選択** ステートメントを呼び出す前に、関数の戻り値をローカル変数へと割り当て、**選択** ステートメントでローカル変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-187">Assign the function's return value to a local variable before you call the **select** statement, and use the local variable in the **select** statement.</span></span> |

### <a name="bpcheckinvalidexecutequery"></a><span data-ttu-id="6df9f-188">BPCheckinvalidExecuteQuery</span><span class="sxs-lookup"><span data-stu-id="6df9f-188">BPCheckinvalidExecuteQuery</span></span>

| <span data-ttu-id="6df9f-189">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-189">Description</span></span>         | <span data-ttu-id="6df9f-190">このルールは、**ExecuteQuery** メソッドで **super()** を呼び出した後に **addRange** への呼び出しが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-190">This rule fails if a call to **addRange** is found after a call to **super()** in the **ExecuteQuery** method.</span></span> |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="6df9f-191">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-191">Error message</span></span>       | <span data-ttu-id="6df9f-192">フォーム %1 の ExecuteQuery メソッドに、super() の後に add range を追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="6df9f-192">Add range after super() should not be added in ExecuteQuery method for form %1</span></span>               |
| <span data-ttu-id="6df9f-193">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-193">Issue type/severity</span></span> | <span data-ttu-id="6df9f-194">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-194">Code/Warning</span></span>                                          |
| <span data-ttu-id="6df9f-195">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-195">How to fix it</span></span>       | <span data-ttu-id="6df9f-196">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-196">Refactor your code to avoid this pattern.</span></span>             |

### <a name="bpcheckinvalidinitformmethod"></a><span data-ttu-id="6df9f-197">BPCheckInvalidInitFormMethod</span><span class="sxs-lookup"><span data-stu-id="6df9f-197">BPCheckInvalidInitFormMethod</span></span>

| <span data-ttu-id="6df9f-198">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-198">Description</span></span>         | <span data-ttu-id="6df9f-199">このルールは、**super()** を呼び出す前にフォームの **init** メソッドでフォーム コントロールとデータソースを初期化しないようにします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-199">This rule makes sure that you don't initialize form controls and data sources in a form's **init** method before you call **super()**.</span></span> <span data-ttu-id="6df9f-200">**element** または **this** を **super()** に対する呼び出し (**this.aMethod()** または **element.aMethod()**) の前に使用するステートメントが検出された場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-200">It fails if it finds a statement that uses **element** or **this** before the call to **super()** (**this.aMethod()** or **element.aMethod()**).</span></span> <span data-ttu-id="6df9f-201">情報メッセージは番号順序の初期化など許可されたいくつかのパターンのみを表示します (**numberSeqPreInit**) 。</span><span class="sxs-lookup"><span data-stu-id="6df9f-201">An informational message is shown only for some allowed patterns, such as initializing number sequences (**numberSeqPreInit**).</span></span> |
|---------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df9f-202">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-202">Error message</span></span>       | <span data-ttu-id="6df9f-203">フォーム要素ステートメントは、フォーム %1 の init メソッドで、super() の前に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6df9f-203">Form element statements should not be used before super() in init method of form %1</span></span>      |
| <span data-ttu-id="6df9f-204">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-204">Issue type/severity</span></span> | <span data-ttu-id="6df9f-205">コード/情報または警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-205">Code/Info or Warning</span></span>                                   |
| <span data-ttu-id="6df9f-206">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-206">How to fix it</span></span>       | <span data-ttu-id="6df9f-207">**super()** の呼び出し後、コードをリファクターしてフォーム コントロールおよびデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-207">Refactor your code to access form controls and data after the call to **super()**.</span></span> <span data-ttu-id="6df9f-208">コードが任意のフォーム コントロールを初期化せず、**super()** の前にどのフォーム データ ソースにもアクセスしない場合、Microsoft にカスタマイズ分析のレポートを送信するときに例外をまとめます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-208">If your code doesn't initialize any form control and doesn't access any form data sources before **super()**, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span>   |

### <a name="bpcheckemptyloop"></a><span data-ttu-id="6df9f-209">BPCheckEmptyLoop</span><span class="sxs-lookup"><span data-stu-id="6df9f-209">BPCheckEmptyLoop</span></span>

| <span data-ttu-id="6df9f-210">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-210">Description</span></span>         | <span data-ttu-id="6df9f-211">このルールは、ステートメントがないループを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-211">This rule fails if it finds loops that have no statements.</span></span> |
|---------------------|------------------------------------------------------------|
| <span data-ttu-id="6df9f-212">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-212">Error message</span></span>       | <span data-ttu-id="6df9f-213">クラス %2 の メソッド %1 で空のループが見つかりました</span><span class="sxs-lookup"><span data-stu-id="6df9f-213">Empty loop found in method %1 in class %2</span></span>                  |
| <span data-ttu-id="6df9f-214">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-214">Issue type/severity</span></span> | <span data-ttu-id="6df9f-215">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-215">Code/Warning</span></span>                                               |
| <span data-ttu-id="6df9f-216">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-216">How to fix it</span></span>       | <span data-ttu-id="6df9f-217">ループをコードから削除します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-217">Remove the loop from your code.</span></span>                            |

### <a name="bpchecklockqueryrange"></a><span data-ttu-id="6df9f-218">BPCheckLockQueryRange</span><span class="sxs-lookup"><span data-stu-id="6df9f-218">BPCheckLockQueryRange</span></span>

| <span data-ttu-id="6df9f-219">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-219">Description</span></span>         | <span data-ttu-id="6df9f-220">フォームの **init** メソッドでコードが **AddRange** を呼び出し、その範囲をロックまたは非表示として設定しないと、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-220">This rule fails if the code calls **AddRange** in the **init** method of the form, and doesn't set the range as locked or hidden.</span></span>      |
|---------------------|-------------------------------------------|
| <span data-ttu-id="6df9f-221">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-221">Error message</span></span>       | <span data-ttu-id="6df9f-222">フォーム %1で、範囲はロックするか、非表示にする必要があります</span><span class="sxs-lookup"><span data-stu-id="6df9f-222">Range should be locked or hidden in form %1</span></span>    |
| <span data-ttu-id="6df9f-223">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-223">Issue type/severity</span></span> | <span data-ttu-id="6df9f-224">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-224">Code/Warning</span></span>     |
| <span data-ttu-id="6df9f-225">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-225">How to fix it</span></span>       | <span data-ttu-id="6df9f-226">**AddRange** の呼び出しの後に、**QueryBuildRange.status(RangeStatus::Locked)** または **QueryBuildRange.status(RangeStatus::Hidden)** を追加します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-226">Add **QueryBuildRange.status(RangeStatus::Locked)** or **QueryBuildRange.status(RangeStatus::Hidden)** after the call to **AddRange**.</span></span> |

### <a name="bpcheckskipstatementvalidation"></a><span data-ttu-id="6df9f-227">BPCheckSkipStatementValidation</span><span class="sxs-lookup"><span data-stu-id="6df9f-227">BPCheckSkipStatementValidation</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6df9f-228">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-228">Description</span></span></td>
<td><span data-ttu-id="6df9f-229">このルールは、<strong>Skip</strong> ステートメントを持たないセットベースの操作を検出した場合に通知メッセージを報告します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-229">This rule reports an informational message if it finds a set-based operation that doesn&#39;t have <strong>Skip</strong> statements.</span></span>
<ul>
<li><span data-ttu-id="6df9f-230"><strong>update_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-230">When <strong>update_recordset</strong> is found, the rule checks for <strong>skipDataMethods(true)</strong>.</span></span> <span data-ttu-id="6df9f-231">テーブルの <strong>update</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-231">The rule applies only when the <strong>update</strong> method on the table is overridden.</span></span></li>
<li><span data-ttu-id="6df9f-232"><strong>insert_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-232">When <strong>insert_recordset</strong> is found, the rule checks for <strong>skipDataMethods(true)</strong>.</span></span> <span data-ttu-id="6df9f-233">テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-233">The rule applies only when the <strong>insert</strong> method on the table is overridden.</span></span></li>
<li><span data-ttu-id="6df9f-234"><strong>delete_from</strong> が見つかると、ルールによって <strong>skipDeleteActions(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-234">When <strong>delete_from</strong> is found, the rule checks for <strong>skipDeleteActions(true)</strong>.</span></span> <span data-ttu-id="6df9f-235">テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-235">The rule applies only when the <strong>insert</strong> method on the table is overridden.</span></span></li>
</ul>
<span data-ttu-id="6df9f-236">これは、セットベースの操作のパフォーマンス向上を最大限に活用するために、<strong>スキップ</strong>メソッドを呼び出す必要があることを示す情報メッセージです。</span><span class="sxs-lookup"><span data-stu-id="6df9f-236">This is an informational message that highlights the need to call <strong>skip</strong> methods to take full advantage of the performance gains of set-based operations.</span></span> <span data-ttu-id="6df9f-237"><strong>スキップ</strong>  メソッドが使用されていない場合は、実行は行ごとの操作に戻ります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-237">If <strong>skip</strong> methods are not used, the execution falls back to a row-by-row operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-238">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-238">Error message</span></span></td>
<td><span data-ttu-id="6df9f-239">セット ベースの操作はクラス %2 のメソッド %1 で Skip ステートメントを呼び出す必要があります。それ以外の場合、行ごとの操作にフォールバックされます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-239">Set-based operation must invoke Skip statements in method %1 in class %2; otherwise, execution will fall back to a row by row operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6df9f-240">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-240">Issue type/severity</span></span></td>
<td><span data-ttu-id="6df9f-241">コード/情報</span><span class="sxs-lookup"><span data-stu-id="6df9f-241">Code/Information</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-242">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-242">How to fix it</span></span></td>
<td><span data-ttu-id="6df9f-243">該当する場合は、<strong>skipDataMethods(true)</strong> または <strong>skipDeleteActions(true)</strong> を使用します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-243">Use <strong>skipDataMethods(true)</strong> or <strong>skipDeleteActions(true)</strong> when applicable.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpchecknottstryblock"></a><span data-ttu-id="6df9f-244">BPCheckNoTTSTryBlock</span><span class="sxs-lookup"><span data-stu-id="6df9f-244">BPCheckNoTTSTryBlock</span></span>

| <span data-ttu-id="6df9f-245">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-245">Description</span></span> | <span data-ttu-id="6df9f-246">このルールは、正しく処理されない <strong>tts</strong> ブロック内の <strong>try</strong> ステートメントを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-246">This rule fails if it finds a <strong>try</strong> statement within a <strong>tts</strong> block that isn&#39;t handled correctly.</span></span> |
|---|---|
| <span data-ttu-id="6df9f-247">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-247">Error message</span></span> | <span data-ttu-id="6df9f-248">try 文の tts ブロックは、メソッド %1 の例外を明示的にキャッチしません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-248">Tts block with Try statement does not explicitly catch exceptions in method %1</span></span> |
| <span data-ttu-id="6df9f-249">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-249">Issue type/severity</span></span> | <span data-ttu-id="6df9f-250">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-250">Code/Warning</span></span> |
| <span data-ttu-id="6df9f-251">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-251">How to fix it</span></span> | <span data-ttu-id="6df9f-252">この表に続くコードの例を使用します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-252">Use the code example that follows this table.</span></span> |

<span data-ttu-id="6df9f-253">次の例では、ルールが失敗するか、合格するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="6df9f-253">The following examples show when the rule will fail or pass.</span></span> <span data-ttu-id="6df9f-254">次の例を参考にして、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-254">Use these examples as guidelines to refactor your code.</span></span>

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

### <a name="bpcheckemptytablemethod"></a><span data-ttu-id="6df9f-255">BPCheckEmptyTableMethod</span><span class="sxs-lookup"><span data-stu-id="6df9f-255">BPCheckEmptyTableMethod</span></span>

| <span data-ttu-id="6df9f-256">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-256">Description</span></span>         | <span data-ttu-id="6df9f-257">このルールは、ソース コードのないテーブル メソッドをチェックします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-257">This rule checks for table methods that have no source code.</span></span> <span data-ttu-id="6df9f-258">空テーブルのメソッドは、テーブルのレコードセット オペレーションを行単位の操作に戻す原因となります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-258">Empty table methods cause record-set operations on the table to fall back to a row-by-row operation.</span></span> |
|---------------------|-------------------------------------------|
| <span data-ttu-id="6df9f-259">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-259">Error message</span></span>       | <span data-ttu-id="6df9f-260">%1 テーブルに空の %2 メソッドがあります</span><span class="sxs-lookup"><span data-stu-id="6df9f-260">%1 table has an empty %2 method</span></span>           |
| <span data-ttu-id="6df9f-261">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-261">Issue type/severity</span></span> | <span data-ttu-id="6df9f-262">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-262">Code/Warning</span></span>                              |
| <span data-ttu-id="6df9f-263">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-263">How to fix it</span></span>       | <span data-ttu-id="6df9f-264">このメソッドをコードから削除します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-264">Remove this method from your code.</span></span>        |

### <a name="bpcheckbatchjobsenabled"></a><span data-ttu-id="6df9f-265">BPCheckBatchJobsEnabled</span><span class="sxs-lookup"><span data-stu-id="6df9f-265">BPCheckBatchJobsEnabled</span></span>

| <span data-ttu-id="6df9f-266">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-266">Description</span></span>         | <span data-ttu-id="6df9f-267">このルールは、**RunBaseBatch** を拡張するすべてのクラスが **true** を返す **canGoBatch** メソッドを持つことを保証します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-267">This rule makes sure that all classes that extend **RunBaseBatch** have a **canGoBatch** method that returns **true**.</span></span> |
|---------------------|----------------------------------------------------------------|
| <span data-ttu-id="6df9f-268">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-268">Error message</span></span>       | <span data-ttu-id="6df9f-269">カスタム ジョブがクラス %1 でバッチ対応でありません</span><span class="sxs-lookup"><span data-stu-id="6df9f-269">Custom job is not batch-enabled in class %1</span></span>         |
| <span data-ttu-id="6df9f-270">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-270">Issue type/severity</span></span> | <span data-ttu-id="6df9f-271">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-271">Code/Warning</span></span>       |
| <span data-ttu-id="6df9f-272">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-272">How to fix it</span></span>       | <span data-ttu-id="6df9f-273">**canGoBatch** メソッドは、すべてのバッチ クラスに **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-273">The **canGoBatch** method must return **true** for all batch classes.</span></span>     |

### <a name="bpcheckdisplaymethodcached"></a><span data-ttu-id="6df9f-274">BPCheckDisplayMethodCached</span><span class="sxs-lookup"><span data-stu-id="6df9f-274">BPCheckDisplayMethodCached</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6df9f-275">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-275">Description</span></span></td>
<td><span data-ttu-id="6df9f-276">データ メソッドにバインドされている各コントロールについては、これらの条件のいずれかが満たされている場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-276">For each control that is bound to a data method, this rules fails if one of these conditions is met:</span></span>
<ul>
<li><span data-ttu-id="6df9f-277"><strong>データのキャッシュ方法</strong>プロパティが<strong>自動</strong>に設定され、対応するテーブルの <strong>display</strong>/<strong>edit</strong> メソッドには <strong>SysClientCacheDataMethodAttribute</strong> がなく、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-277">The <strong>Cache Data Method</strong> property is set to <strong>Auto</strong>, the corresponding table <strong>display</strong>/<strong>edit</strong> method doesn&#39;t have the <strong>SysClientCacheDataMethodAttribute</strong>, and the <strong>init</strong> method of the data source doesn&#39;t use <strong>CacheAddMethod</strong>.</span></span></li>
<li><span data-ttu-id="6df9f-278"><strong>データのキャッシュ方法</strong> プロパティは <strong>いいえ</strong> に設定され、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-278">The <strong>Cache Data Method</strong> property is set to <strong>No</strong>, and the <strong>init</strong> method of the data source doesn&#39;t use <strong>CacheAddMethod</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-279">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-279">Error message</span></span></td>
<td><span data-ttu-id="6df9f-280">フォーム %2 の 表示メソッド %1 がキャッシュされていません</span><span class="sxs-lookup"><span data-stu-id="6df9f-280">Display method %1 in form %2 not cached</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6df9f-281">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-281">Issue type/severity</span></span></td>
<td><span data-ttu-id="6df9f-282">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-282">Code/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-283">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-283">How to fix it</span></span></td>
<td><span data-ttu-id="6df9f-284">この表に続くメモを使用します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-284">Use the note that follows this table.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6df9f-285">この警告は、次のいずれかのパターンを使用して修正することができます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-285">You can fix this warning by using one of the following patterns:</span></span>

+ <span data-ttu-id="6df9f-286">**キャッシュ データ メソッド** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-286">Set the **Cache Data Method** property to **Yes**.</span></span>
+ <span data-ttu-id="6df9f-287">**キャッシュ データ メソッド** プロパティを **自動** に設定し、**SysClientCacheDataMethodAttribute** 属性を使用してテーブルのデータ メソッドをマークします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-287">Set the **Cache Data Method** property to **Auto**, and mark the data method of the table with the **SysClientCacheDataMethodAttribute** attribute.</span></span> <span data-ttu-id="6df9f-288">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-288">Here is an example.</span></span>

    ```xp
    [SysClientCacheDataMethodAttribute(true)]
    Display TransDate myDateMethod()
    {
        //...
    }
    ```

+ <span data-ttu-id="6df9f-289">フォームの **init** メソッドで **CacheAddMethod** を使用すると、そのメソッドをキャッシュ済みとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-289">Use **CacheAddMethod** in the **init** method of the form to mark the method as cached.</span></span>

### <a name="bpchecksqlqueryininit"></a><span data-ttu-id="6df9f-290">BPCheckSQLQueryInInit</span><span class="sxs-lookup"><span data-stu-id="6df9f-290">BPCheckSQLQueryInInit</span></span>

| <span data-ttu-id="6df9f-291">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-291">Description</span></span>         | <span data-ttu-id="6df9f-292">このルールは、フォームの **init** メソッドで **while** ループを持つデータ アクセス クエリが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-292">This rule fails if a data access query that has a **while** loop is found in the **init** method of a form.</span></span> <span data-ttu-id="6df9f-293">このパターンは、フォームの初期化時にパフォーマンスの問題を引き起こす場合があります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-293">This pattern could cause performance issues when the form is initialized.</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="6df9f-294">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-294">Error message</span></span>       | <span data-ttu-id="6df9f-295">フォーム %1 の init メソッドで、while ループを持つ SQL クエリが見つかりました</span><span class="sxs-lookup"><span data-stu-id="6df9f-295">SQL query with while loop was found in init method of form %1</span></span>            |
| <span data-ttu-id="6df9f-296">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-296">Issue type/severity</span></span> | <span data-ttu-id="6df9f-297">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-297">Code/Warning</span></span>   |
| <span data-ttu-id="6df9f-298">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-298">How to fix it</span></span>       | <span data-ttu-id="6df9f-299">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-299">Refactor your code to avoid this pattern.</span></span>  |

### <a name="bpchecknewquerywithform"></a><span data-ttu-id="6df9f-300">BPCheckNewQueryWithForm</span><span class="sxs-lookup"><span data-stu-id="6df9f-300">BPCheckNewQueryWithForm</span></span>

| <span data-ttu-id="6df9f-301">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-301">Description</span></span>         | <span data-ttu-id="6df9f-302">このルールは、フォームの **init** または **executeQuery** メソッドで **new Query()** ステートメントを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-302">This rule fails if it finds the **new Query()** statement in the **init** or **executeQuery** method of a form.</span></span> |
|---------------------|--------------------------------------------------|
| <span data-ttu-id="6df9f-303">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-303">Error message</span></span>       | <span data-ttu-id="6df9f-304">フォーム メソッド %1 で、データ ソース クエリが上書きされます</span><span class="sxs-lookup"><span data-stu-id="6df9f-304">Data source query overridden in form method %1</span></span>      |
| <span data-ttu-id="6df9f-305">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-305">Issue type/severity</span></span> | <span data-ttu-id="6df9f-306">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-306">Code/Warning</span></span>                                |
| <span data-ttu-id="6df9f-307">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-307">How to fix it</span></span>       | <span data-ttu-id="6df9f-308">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="6df9f-308">Refactor your code to avoid this pattern.</span></span>            |

### <a name="bpcheckselectforupdateabsent"></a><span data-ttu-id="6df9f-309">BPCheckSelectForUpdateAbsent</span><span class="sxs-lookup"><span data-stu-id="6df9f-309">BPCheckSelectForUpdateAbsent</span></span>

| <span data-ttu-id="6df9f-310">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-310">Description</span></span>         | <span data-ttu-id="6df9f-311">**Select ForUpdate** を使用してレコードを選択したが、更新が実行されていない場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-311">This rule fails if **Select ForUpdate** is used to select records, but an update isn't being performed.</span></span> <span data-ttu-id="6df9f-312">このルールは、オプティミスティック同時実行制御 (OCC) が有効になっているテーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-312">This rules doesn't apply to tables that are enabled for Optimistic Concurrency Control (OCC).</span></span> |
|---------------------|------------------|
| <span data-ttu-id="6df9f-313">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-313">Error message</span></span>       | <span data-ttu-id="6df9f-314">メソッド %1 に Select ForUpdate が実装されていません</span><span class="sxs-lookup"><span data-stu-id="6df9f-314">Select ForUpdate not implemented in method %1</span></span>   |
| <span data-ttu-id="6df9f-315">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-315">Issue type/severity</span></span> | <span data-ttu-id="6df9f-316">コード/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-316">Code/Warning</span></span>      |
| <span data-ttu-id="6df9f-317">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-317">How to fix it</span></span>       | <span data-ttu-id="6df9f-318">**ForUpdate を選択** の代わりに **選択** を使用するか、**OCC を有効** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-318">Use **Select** instead of **Select ForUpdate**, or set the **OCC Enabled** property to **Yes** on the table.</span></span>                                                                                          |

### <a name="bpchecktablepropertymismatch"></a><span data-ttu-id="6df9f-319">BPCheckTablePropertyMismatch</span><span class="sxs-lookup"><span data-stu-id="6df9f-319">BPCheckTablePropertyMismatch</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6df9f-320">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-320">Description</span></span></td>
<td><span data-ttu-id="6df9f-321">このルールは、テーブルがテーブル グループに属しているが、適切な<strong>キャッシュ ルックアップ</strong>値を持たない場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-321">This rule fails when the table belongs to a table group but doesn&#39;t have the appropriate <strong>Cache Lookup</strong> value.</span></span> <span data-ttu-id="6df9f-322">次の条件がすべて満たされていると、ルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-322">The rule fails if one of these conditions is met:</span></span>
<ul>
<li><span data-ttu-id="6df9f-323"><strong>テーブル グループ</strong> プロパティは <strong>メイン</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> または <strong>EntireTable</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-323">The <strong>Table Group</strong> property is set to <strong>Main</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>NotinTTS</strong> or <strong>EntireTable</strong>.</span></span></li>
<li><span data-ttu-id="6df9f-324"><strong>テーブル グループ</strong> プロパティは <strong>グループ</strong> または <strong>パラメーター</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-324">The <strong>Table Group</strong> property is set to <strong>Group</strong> or <strong>Parameter</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>NotinTTS</strong>.</span></span></li>
<li><span data-ttu-id="6df9f-325"><strong>テーブル グループ</strong> プロパティは <strong>WorksheetHeader</strong>、<strong>WorksheetLine</strong>、または <strong>Transaction</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>Found</strong>、<strong>FoundAndEmpty</strong>、または <strong>EntireTable</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-325">The <strong>Table Group</strong> property is set to <strong>WorksheetHeader</strong>, <strong>WorksheetLine</strong>, or <strong>Transaction</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>Found</strong>, <strong>FoundAndEmpty</strong>, or <strong>EntireTable</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-326">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-326">Error message</span></span></td>
<td><span data-ttu-id="6df9f-327">%1 テーブルにテーブル グループとキャッシュ ルックアップの無効な組み合わせがあります</span><span class="sxs-lookup"><span data-stu-id="6df9f-327">%1 table has an invalid combination of table group and cache lookup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6df9f-328">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-328">Issue type/severity</span></span></td>
<td><span data-ttu-id="6df9f-329">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-329">MetaData/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-330">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-330">How to fix it</span></span></td>
<td><span data-ttu-id="6df9f-331">テーブルで適切な <strong>キャッシュ ルックアップ</strong> 値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-331">Set an appropriate <strong>Cache Lookup</strong> value on the table.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpcheckmissingdeleteactions"></a><span data-ttu-id="6df9f-332">BPCheckMissingDeleteActions</span><span class="sxs-lookup"><span data-stu-id="6df9f-332">BPCheckMissingDeleteActions</span></span>

| <span data-ttu-id="6df9f-333">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-333">Description</span></span>         | <span data-ttu-id="6df9f-334">このルールは、テーブル関係の **削除** アクションまたは **削除時** プロパティの値が **なし** と等しくないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-334">This rule validates that the value of either a **delete** action or the **On Delete** property of a table relation isn't equal to **None**.</span></span> <span data-ttu-id="6df9f-335">関連するテーブルまたは現在のテーブルが tempDB、メモリ テーブル、参照テーブル、ステージング テーブル、パラメーター テーブルの場合、ルールはトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-335">The rule isn't triggered when the related or current table is a tempDB, in memory table, reference table, staging table, or parameter table.</span></span> |
|---------------------|---------------------------------------------------|
| <span data-ttu-id="6df9f-336">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-336">Error message</span></span>       | <span data-ttu-id="6df9f-337">リレーション名 %3 でテーブル %2 に関連付けられているテーブル %1 に欠けているアクションを削除します</span><span class="sxs-lookup"><span data-stu-id="6df9f-337">Delete actions missing in table %1 which is related to table %2 with relation name %3</span></span>      |
| <span data-ttu-id="6df9f-338">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-338">Issue type/severity</span></span> | <span data-ttu-id="6df9f-339">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-339">MetaData/Warning</span></span>   |
| <span data-ttu-id="6df9f-340">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-340">How to fix it</span></span>       | <span data-ttu-id="6df9f-341">**None** と等しくない **delete** アクションを設定します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-341">Set a **delete** action value that isn't equal to **None**.</span></span> |

### <a name="bpcheckaddressmodel"></a><span data-ttu-id="6df9f-342">BPCheckAddressModel</span><span class="sxs-lookup"><span data-stu-id="6df9f-342">BPCheckAddressModel</span></span>

| <span data-ttu-id="6df9f-343">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-343">Description</span></span>         | <span data-ttu-id="6df9f-344">テーブル フィールドが **AddressZipCodeId** または **AddressStateId** タイプの場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-344">This rule fails if a table field is of the **AddressZipCodeId** or **AddressStateId** type.</span></span> <span data-ttu-id="6df9f-345">これらのタイプは、コードが新しいアドレス フレームワークを受け入れなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-345">These types indicate that the code didn't uptake the newer Address framework.</span></span> |
|---------------------|-------------------------|
| <span data-ttu-id="6df9f-346">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-346">Error message</span></span>       | <span data-ttu-id="6df9f-347">テーブル %2 のフィールド %1 は、アドレスの場所モデルの一部ではありません</span><span class="sxs-lookup"><span data-stu-id="6df9f-347">Field %1 of table %2 is not part of address location model</span></span>   |
| <span data-ttu-id="6df9f-348">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-348">Issue type/severity</span></span> | <span data-ttu-id="6df9f-349">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-349">MetaData/Warning</span></span>  |
| <span data-ttu-id="6df9f-350">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-350">How to fix it</span></span>       | <span data-ttu-id="6df9f-351">これらのタイプをディレクトリ モデルのその他の適切な EDT タイプに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-351">Replace these types with any other appropriate EDT type in the Directory model.</span></span>        |

### <a name="bpcheckdimensionmodel"></a><span data-ttu-id="6df9f-352">BPCheckDimensionModel</span><span class="sxs-lookup"><span data-stu-id="6df9f-352">BPCheckDimensionModel</span></span>

| <span data-ttu-id="6df9f-353">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-353">Description</span></span>         | <span data-ttu-id="6df9f-354">テーブル フィールドが、**分析コード** または **LedgerAccount** タイプの場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-354">This rule fails if a table field is of the **Dimension** or **LedgerAccount** type.</span></span> <span data-ttu-id="6df9f-355">これらのタイプは、コードが新しい財務分析コード フレームワークを受け入れなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-355">These types indicate that the code didn't uptake the newer Financial Dimension framework.</span></span> |
|---------------------|----------|
| <span data-ttu-id="6df9f-356">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-356">Error message</span></span>       | <span data-ttu-id="6df9f-357">テーブル %2 のフィールド %1 は、財務分析コード フレームワークの一部ではありません</span><span class="sxs-lookup"><span data-stu-id="6df9f-357">Field %1 of table %2 is not part of financial dimension framework</span></span>               |
| <span data-ttu-id="6df9f-358">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-358">Issue type/severity</span></span> | <span data-ttu-id="6df9f-359">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-359">MetaData/Warning</span></span>   |
| <span data-ttu-id="6df9f-360">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-360">How to fix it</span></span>       | <span data-ttu-id="6df9f-361">これらのタイプを分析コード モデルのその他の適切な EDT タイプに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-361">Replace these types with any other appropriate EDT type in the Dimensions model.</span></span>       |

### <a name="bpchecknumberofnewfields"></a><span data-ttu-id="6df9f-362">BPCheckNumberofNewFields</span><span class="sxs-lookup"><span data-stu-id="6df9f-362">BPCheckNumberofNewFields</span></span>

| <span data-ttu-id="6df9f-363">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-363">Description</span></span>         | <span data-ttu-id="6df9f-364">このルールは、そのテーブルのカスタマイズまたは拡張のプロセスで、テーブルに 10 個以下のフィールドが追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-364">This rule verifies that no more than 10 fields were added to a table during the process of customizing or extending that table.</span></span> <span data-ttu-id="6df9f-365">このルールは、ステージング テーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-365">This rule doesn't apply to staging tables.</span></span> |
|---------------------|-------------------------------------|
| <span data-ttu-id="6df9f-366">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-366">Error message</span></span>       | <span data-ttu-id="6df9f-367">次の値より大きいテーブル %1 の新しいフィールドの数</span><span class="sxs-lookup"><span data-stu-id="6df9f-367">Number of new fields in table %1 is greater than</span></span>      |
| <span data-ttu-id="6df9f-368">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-368">Issue type/severity</span></span> | <span data-ttu-id="6df9f-369">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-369">Metadata/Warning</span></span>   |
| <span data-ttu-id="6df9f-370">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-370">How to fix it</span></span>       | <span data-ttu-id="6df9f-371">スキーマをリファクタリングし、既存のテーブルに多数のフィールドを追加する代わりに関連するテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-371">Refactor your schema and create related tables instead of adding too many fields to an existing table.</span></span> |

### <a name="bpcheckenumupgradeissue"></a><span data-ttu-id="6df9f-372">BPCheckEnumUpgradeIssue</span><span class="sxs-lookup"><span data-stu-id="6df9f-372">BPCheckEnumUpgradeIssue</span></span>

| <span data-ttu-id="6df9f-373">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-373">Description</span></span>         | <span data-ttu-id="6df9f-374">このルールは、次の条件が満たされた場合に失敗します。列挙型 (オーバーレイ) をカスタマイズすると、新しい列挙型の値は既存の最大値 + 10 未満になります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-374">This rule fails when the following condition is met: When you customize an enum (overlayer), new enum values are less than the maximum existing value + 10.</span></span> <span data-ttu-id="6df9f-375">このルールは、拡張可能な列挙型には適用されません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-375">This rules doesn't apply to extensible enums.</span></span> |
|---------------------|--------------------------------------|
| <span data-ttu-id="6df9f-376">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-376">Error message</span></span>       | <span data-ttu-id="6df9f-377">列挙 %1 で、アップグレード問題があります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-377">Enum %1 will have upgrade issues</span></span>    |
| <span data-ttu-id="6df9f-378">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-378">Issue type/severity</span></span> | <span data-ttu-id="6df9f-379">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-379">MetaData/Warning</span></span>       |
| <span data-ttu-id="6df9f-380">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-380">How to fix it</span></span>       | <span data-ttu-id="6df9f-381">大きな列挙値を使用するか、列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-381">Use larger enum values, or extend the enum.</span></span>       |

### <a name="bpcheckpassivejoinuse"></a><span data-ttu-id="6df9f-382">BPCheckPassiveJoinUse</span><span class="sxs-lookup"><span data-stu-id="6df9f-382">BPCheckPassiveJoinUse</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6df9f-383">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-383">Description</span></span></td>
<td><span data-ttu-id="6df9f-384">このルールは、フォームがデータのプリロードを許可する場合、タブ ページ データソースのリンク タイプがパッシブであることを検証します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-384">This rule validates that, when a form allows for pre-loading of data, the link type of tab page data sources is passive.</span></span> <span data-ttu-id="6df9f-385">次の条件がすべて満たされていると、ルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-385">The rule fails if all the following conditions are met:</span></span>
<ul>
<li><span data-ttu-id="6df9f-386"><strong>Yes</strong> に設定された <strong>AllowPreLoading</strong> プロパティのフォームがあります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-386">A form has the <strong>AllowPreLoading</strong> property set to <strong>Yes</strong>.</span></span></li>
<li><span data-ttu-id="6df9f-387">フォームのタブ ページは、最上位レベルのデータ ソースにバインドされています。</span><span class="sxs-lookup"><span data-stu-id="6df9f-387">A tab page on the form is bound to a top-level data source.</span></span></li>
<li><span data-ttu-id="6df9f-388">データ ソースの<strong>結合ソース</strong>プロパティが設定されます。</span><span class="sxs-lookup"><span data-stu-id="6df9f-388">The data source's <strong>Join Source </strong>property is set.</span></span></li>
<li><span data-ttu-id="6df9f-389">データ ソースの <strong>リンク タイプ</strong> プロパティが <strong>パッシブ</strong> に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-389">The data source's <strong>Link Type</strong> property isn&#39;t set to <strong>Passive</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-390">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-390">Error message</span></span></td>
<td><span data-ttu-id="6df9f-391">新しいメッセージは、「フォームの %2 タブ ページ コントロールにバインドされたデータソース %1 でパッシブ結合を使用する」 ことを提案しています</span><span class="sxs-lookup"><span data-stu-id="6df9f-391">New message suggest: "Use passive joins on data sources %1 bound to a tab page control in form %2"</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6df9f-392">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-392">Issue type/severity</span></span></td>
<td><span data-ttu-id="6df9f-393">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-393">MetaData/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6df9f-394">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-394">How to fix it</span></span></td>
<td><span data-ttu-id="6df9f-395">フォームで <strong>AllowPreLoading</strong> プロパティを <strong>いいえ</strong> に設定するか、データ ソースでパッシブ結合を使用します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-395">Set the <strong>AllowPreLoading</strong> property to <strong>No</strong> on the form, or use passive joins on the data source.</span></span> <span data-ttu-id="6df9f-396">パッシブ結合では、タブ ページのクエリの実行時に明示的にプログラミングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-396">Passive joins require that you explicitly program when the query of a tab page is run.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpcheckalternatekeyabsent"></a><span data-ttu-id="6df9f-397">BPCheckAlternateKeyAbsent</span><span class="sxs-lookup"><span data-stu-id="6df9f-397">BPCheckAlternateKeyAbsent</span></span>

| <span data-ttu-id="6df9f-398">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-398">Description</span></span>         | <span data-ttu-id="6df9f-399">このルールは、一意のインデックスを持つテーブルに少なくとも 1 つの代替キーがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-399">This rule verifies that tables that have a unique index have at least one alternate key.</span></span> |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df9f-400">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-400">Error message</span></span>       | <span data-ttu-id="6df9f-401">テーブル %1 には、代替キーがありません</span><span class="sxs-lookup"><span data-stu-id="6df9f-401">Table %1 does not have an alternate key</span></span>                                                  |
| <span data-ttu-id="6df9f-402">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-402">Issue type/severity</span></span> | <span data-ttu-id="6df9f-403">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-403">MetaData/Warning</span></span>                                                                         |
| <span data-ttu-id="6df9f-404">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-404">How to fix it</span></span>       | <span data-ttu-id="6df9f-405">テーブルの一意のインデックスで **代替キー** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6df9f-405">Set the **Alternate Key** property to **Yes** on a unique index of the table.</span></span>            |

### <a name="bpcheckbasetablemodified"></a><span data-ttu-id="6df9f-406">BPCheckBaseTableModified</span><span class="sxs-lookup"><span data-stu-id="6df9f-406">BPCheckBaseTableModified</span></span>

| <span data-ttu-id="6df9f-407">説明</span><span class="sxs-lookup"><span data-stu-id="6df9f-407">Description</span></span>         | <span data-ttu-id="6df9f-408">このルールは、Microsoft によって出荷される特定のベース テーブルの一覧のカスタマイズ (オーバーレイ化) を推奨しません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-408">This rule discourages the customization (overlayering) of a list of specific base tables that are shipped by Microsoft.</span></span> <span data-ttu-id="6df9f-409">例では、SourceDocumentHeader および SourceDocumentLine テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="6df9f-409">Examples are the SourceDocumentHeader and SourceDocumentLine tables.</span></span> |
|---------------------|----------------------------|
| <span data-ttu-id="6df9f-410">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="6df9f-410">Error message</span></span>       | <span data-ttu-id="6df9f-411">%1 はベース テーブルであり、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="6df9f-411">%1 is a base table and must not be modified</span></span>   |
| <span data-ttu-id="6df9f-412">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="6df9f-412">Issue type/severity</span></span> | <span data-ttu-id="6df9f-413">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="6df9f-413">MetaData/Warning</span></span>     |
| <span data-ttu-id="6df9f-414">修正する方法</span><span class="sxs-lookup"><span data-stu-id="6df9f-414">How to fix it</span></span>       | <span data-ttu-id="6df9f-415">テーブルをカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="6df9f-415">Don't customize the table.</span></span>    |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
