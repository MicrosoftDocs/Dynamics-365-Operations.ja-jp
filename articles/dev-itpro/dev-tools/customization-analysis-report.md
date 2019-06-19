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
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 49681
ms.assetid: 540b08dd-9af7-42fc-aa0c-ba04af1f8002
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55f1b6dc6f8bcb714982cb890cc76247bd09636a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544161"
---
# <a name="customization-analysis-report-car"></a><span data-ttu-id="8670f-104">カスタマイズ分析のレポート (CAR)</span><span class="sxs-lookup"><span data-stu-id="8670f-104">Customization Analysis Report (CAR)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8670f-105">この記事では、モデルのカスタマイズ分析レポートを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8670f-105">This article describes how to generate a Customization Analysis Report for your model.</span></span> <span data-ttu-id="8670f-106">また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。</span><span class="sxs-lookup"><span data-stu-id="8670f-106">It also describes some best practice rules that are included in the report, and provides suggestions for fixing errors and warnings that are associated with these rules.</span></span> 

<a name="what-is-the-customization-analysis-report"></a><span data-ttu-id="8670f-107">カスタマイズ分析レポートとは</span><span class="sxs-lookup"><span data-stu-id="8670f-107">What is the Customization Analysis Report?</span></span>
------------------------------------------

<span data-ttu-id="8670f-108">カスタマイズ分析レポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行するツールです。</span><span class="sxs-lookup"><span data-stu-id="8670f-108">The Customization Analysis Report is a tool that analyzes your customization and extension models, and runs a predefined set of best practice rules.</span></span> <span data-ttu-id="8670f-109">このレポートは、ソリューション認証プロセスの要件の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="8670f-109">The report is one of the requirements of the solution certification process.</span></span> <span data-ttu-id="8670f-110">レポートは、Microsoft Excel のブック形式です。</span><span class="sxs-lookup"><span data-stu-id="8670f-110">The report is in the form of a Microsoft Excel workbook.</span></span>

## <a name="how-to-generate-the-report"></a><span data-ttu-id="8670f-111">レポートを生成する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-111">How to generate the report</span></span>
<span data-ttu-id="8670f-112">カスタマイズ分析レポートを生成するには、開発環境で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8670f-112">To generate the Customization Analysis Report, run the following command in a development environment.</span></span>

    xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>

<span data-ttu-id="8670f-113">**例**</span><span class="sxs-lookup"><span data-stu-id="8670f-113">**Example**</span></span>

    xppbp.exe -metadata=C:\Packages -all -model="MyAppSuiteCustomizations" -xmlLog=C:\temp\BPCheckLogcd.xml -module="ApplicationSuite" -car=c:\temp\CAReport.xlsx

<span data-ttu-id="8670f-114">xppbp.exe ツール、c:\\packages\\bin または I:\\AosService\\PackagesLocalDirectory\\bin にあります。</span><span class="sxs-lookup"><span data-stu-id="8670f-114">The xppbp.exe tool is located in c:\\packages\\bin or I:\\AosService\\PackagesLocalDirectory\\bin.</span></span>

## <a name="issues-list"></a><span data-ttu-id="8670f-115">問題リスト</span><span class="sxs-lookup"><span data-stu-id="8670f-115">Issues List</span></span>
<span data-ttu-id="8670f-116">このセクションでは、レポートの**問題リスト**ページに表示されるベスト プラクティスのルール (エラー、警告、または情報メッセージ) をすべて説明し、問題を解決するための提案を示します。</span><span class="sxs-lookup"><span data-stu-id="8670f-116">This section describes all best practice rules (errors, warnings, or informational messages) that can appear on the **Issues List** page of the report and provides suggestions for fixing the issues.</span></span> <span data-ttu-id="8670f-117">**メタデータ**または**コード**の型の問題です。</span><span class="sxs-lookup"><span data-stu-id="8670f-117">Issues are of the **metadata** or **code** type.</span></span> <span data-ttu-id="8670f-118">すべての**コード**問題に関しては、重ねたメソッドで警告またはエラーが発生する場合、ルールに違反しているコードの明細行は下位レイヤーのモデルに属していることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="8670f-118">For all **code** issues, keep in mind that, if the warning or error occurs in a method that you've overlaid, the lines of code that violate the rule might belong to a model in a lower layer.</span></span> <span data-ttu-id="8670f-119">その場合、自分のものではないコードの警告やエラーを修正する責任はありません。</span><span class="sxs-lookup"><span data-stu-id="8670f-119">In that case, you're not responsible for fixing warnings and errors in code that isn't yours.</span></span>

### <a name="bpcheckpackreturnsconnull"></a><span data-ttu-id="8670f-120">BPCheckPackReturnsConnull</span><span class="sxs-lookup"><span data-stu-id="8670f-120">BPCheckPackReturnsConnull</span></span>

| <span data-ttu-id="8670f-121">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-121">Description</span></span>         | <span data-ttu-id="8670f-122">このルールは、**SysPackable** インターフェイスを実装するすべてのクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-122">This rule applies to all classes that implement the **SysPackable** interface.</span></span> <span data-ttu-id="8670f-123">これは、**Pack** メソッドが **Connull()** を返さないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8670f-123">It makes sure that the **Pack** method doesn't return **Connull()**.</span></span> |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-124">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-124">Error message</span></span>       | <span data-ttu-id="8670f-125">コンテナー パック メソッドは、Runbase 派生クラスで connull を返します</span><span class="sxs-lookup"><span data-stu-id="8670f-125">Container pack method returns connull in a Runbase derived class</span></span>                                                                                    |
| <span data-ttu-id="8670f-126">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-126">Issue type/severity</span></span> | <span data-ttu-id="8670f-127">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-127">Code/Warning</span></span>                                                                                                                                        |
| <span data-ttu-id="8670f-128">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-128">How to fix it</span></span>       | <span data-ttu-id="8670f-129">該当する場合、**Pack** メソッドの戻り値を更新するか、**Super()** を返します。</span><span class="sxs-lookup"><span data-stu-id="8670f-129">Update the return value of the **Pack** method, or return **Super()** when applicable.</span></span>                                                              |

### <a name="bpcheckparametersmodified"></a><span data-ttu-id="8670f-130">BPCheckParametersModified</span><span class="sxs-lookup"><span data-stu-id="8670f-130">BPCheckParametersModified</span></span>

| <span data-ttu-id="8670f-131">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-131">Description</span></span>         | <span data-ttu-id="8670f-132">メソッドのパラメーターがメソッド内で変更された場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-132">This rule fails if a parameter of a method is modified inside a method.</span></span>                      |
|---------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-133">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-133">Error message</span></span>       | <span data-ttu-id="8670f-134">メソッド %1 のパラメーター 1% がメソッド内で変更されています</span><span class="sxs-lookup"><span data-stu-id="8670f-134">Parameter 1% in method %1 are modified inside the method</span></span>                                     |
| <span data-ttu-id="8670f-135">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-135">Issue type/severity</span></span> | <span data-ttu-id="8670f-136">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-136">Code/Warning</span></span>                                                                                 |
| <span data-ttu-id="8670f-137">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-137">How to fix it</span></span>       | <span data-ttu-id="8670f-138">コードをリファクターします。</span><span class="sxs-lookup"><span data-stu-id="8670f-138">Refactor your code.</span></span> <span data-ttu-id="8670f-139">呼び出されたメソッド内ではなく、呼び出し元によりパラメーターを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8670f-139">Parameters must be modified by the caller, not within the called method.</span></span> |

### <a name="bpchecksqlcode"></a><span data-ttu-id="8670f-140">BPCheckSQLCode</span><span class="sxs-lookup"><span data-stu-id="8670f-140">BPCheckSQLCode</span></span>

| <span data-ttu-id="8670f-141">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-141">Description</span></span>         | <span data-ttu-id="8670f-142">このルールは、X++ コードに直接 SQL コードが含まれていると失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-142">This rule fails if your X++ code contains direct SQL code.</span></span>                        |
|---------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-143">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-143">Error message</span></span>       | <span data-ttu-id="8670f-144">メソッド %1 に SQL コードが見つかりました</span><span class="sxs-lookup"><span data-stu-id="8670f-144">SQL code found in method %1</span></span>                                                       |
| <span data-ttu-id="8670f-145">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-145">Issue type/severity</span></span> | <span data-ttu-id="8670f-146">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-146">Code/Warning</span></span>                                                                      |
| <span data-ttu-id="8670f-147">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-147">How to fix it</span></span>       | <span data-ttu-id="8670f-148">X++ を使用してデータベースにアクセスするコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="8670f-148">Refactor your code to use X++ to access the database.</span></span> |

### <a name="bpchecknestedloopincode"></a><span data-ttu-id="8670f-149">BPCheckNestedLoopInCode</span><span class="sxs-lookup"><span data-stu-id="8670f-149">BPCheckNestedLoopInCode</span></span>

| <span data-ttu-id="8670f-150">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-150">Description</span></span>         | <span data-ttu-id="8670f-151">このルールは、**select** ループがループ内にネストされていることを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-151">This rule fails if it finds a **while select** loop nested within a loop.</span></span>                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-152">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-152">Error message</span></span>       | <span data-ttu-id="8670f-153">%1 メソッドに入れ子になったデータ アクセス ループが見つかりました</span><span class="sxs-lookup"><span data-stu-id="8670f-153">Nested data access loop found in %1 method</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="8670f-154">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-154">Issue type/severity</span></span> | <span data-ttu-id="8670f-155">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-155">Code/Warning</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="8670f-156">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-156">How to fix it</span></span>       | <span data-ttu-id="8670f-157">入れ子になったデータ アクセス ループの代わりに結合を使うコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="8670f-157">Refactor your code to use joins instead of nested data access loops.</span></span> <span data-ttu-id="8670f-158">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</span><span class="sxs-lookup"><span data-stu-id="8670f-158">If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span> |

### <a name="bpcheckinsertmethodinloop"></a><span data-ttu-id="8670f-159">BPCheckInsertMethodInLoop</span><span class="sxs-lookup"><span data-stu-id="8670f-159">BPCheckInsertMethodInLoop</span></span>

| <span data-ttu-id="8670f-160">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-160">Description</span></span>         | <span data-ttu-id="8670f-161">このルールは、ループの中に入れ子されたメソッド **insert** への呼び出しを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-161">This rules fails if it finds a call to the method **insert** nested inside a loop.</span></span> <span data-ttu-id="8670f-162">**InsertRecordList** を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8670f-162">We recommend that you use **InsertRecordList**.</span></span> <span data-ttu-id="8670f-163">このルールは、InMemory テーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="8670f-163">This rule doesn't apply to InMemory tables.</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-164">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-164">Error message</span></span>       | <span data-ttu-id="8670f-165">メソッド %1 で、Insert メソッドを RecordInsertList に置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="8670f-165">Insert method can be replaced with RecordInsertList in method %1</span></span>                                                                                                               |
| <span data-ttu-id="8670f-166">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-166">Issue type/severity</span></span> | <span data-ttu-id="8670f-167">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-167">Code/Warning</span></span>                                                                                                                                                                   |
| <span data-ttu-id="8670f-168">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-168">How to fix it</span></span>       | <span data-ttu-id="8670f-169">**InsertRecordList** など、設定に基づく操作を使用するコードをリファクターします。</span><span class="sxs-lookup"><span data-stu-id="8670f-169">Refactor your code to use set-based operations, such as **InsertRecordList**.</span></span>                                                                                                  |

### <a name="bpcheckselectwithjoin"></a><span data-ttu-id="8670f-170">BPCheckSelectwithJoin</span><span class="sxs-lookup"><span data-stu-id="8670f-170">BPCheckSelectwithJoin</span></span>

| <span data-ttu-id="8670f-171">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-171">Description</span></span>         | <span data-ttu-id="8670f-172">結合されていない入れ子になった **select** ステートメントが見つかった場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-172">This rule fails if it finds nested **select** statements that aren't joined.</span></span>                                                                                                                                                                        |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-173">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-173">Error message</span></span>       | <span data-ttu-id="8670f-174">%1 メソッドの入れ子になった select ステートメントは結合できます。</span><span class="sxs-lookup"><span data-stu-id="8670f-174">Nested select statement in %1 method can be joined</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="8670f-175">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-175">Issue type/severity</span></span> | <span data-ttu-id="8670f-176">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-176">Code/Warning</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="8670f-177">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-177">How to fix it</span></span>       | <span data-ttu-id="8670f-178">入れ子になった **select** ステートメントの代わりに結合を使うコードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="8670f-178">Refactor your code to use joins instead of a nested **select** statement.</span></span> <span data-ttu-id="8670f-179">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</span><span class="sxs-lookup"><span data-stu-id="8670f-179">If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span> |

### <a name="bpfunctioncallwithselect"></a><span data-ttu-id="8670f-180">BPFunctionCallwithSelect</span><span class="sxs-lookup"><span data-stu-id="8670f-180">BPFunctionCallwithSelect</span></span>

| <span data-ttu-id="8670f-181">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-181">Description</span></span>         | <span data-ttu-id="8670f-182">このルールは、**select** ステートメント内で関数呼び出しが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-182">This rule fails if a function call is found within a **select** statement.</span></span>                                                                               |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-183">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-183">Error message</span></span>       | <span data-ttu-id="8670f-184">メソッド %1 の select ステートメントに、関数呼び出しが見つかりました</span><span class="sxs-lookup"><span data-stu-id="8670f-184">Function call found in select statement in method %1</span></span>                                                                                                     |
| <span data-ttu-id="8670f-185">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-185">Issue type/severity</span></span> | <span data-ttu-id="8670f-186">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-186">Code/Warning</span></span>                                                                                                                                             |
| <span data-ttu-id="8670f-187">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-187">How to fix it</span></span>       | <span data-ttu-id="8670f-188">**選択**ステートメントを呼び出す前に、関数の戻り値をローカル変数に割り当て、**選択**ステートメントでローカル変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="8670f-188">Assign the function’s return value to a local variable before you call the **select** statement, and use the local variable in the **select** statement.</span></span> |

### <a name="bpcheckinvalidexecutequery"></a><span data-ttu-id="8670f-189">BPCheckinvalidExecuteQuery</span><span class="sxs-lookup"><span data-stu-id="8670f-189">BPCheckinvalidExecuteQuery</span></span>

| <span data-ttu-id="8670f-190">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-190">Description</span></span>         | <span data-ttu-id="8670f-191">このルールは、**ExecuteQuery** メソッドで **super()** を呼び出した後に **addRange** への呼び出しが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-191">This rule fails if a call to **addRange** is found after a call to **super()** in the **ExecuteQuery** method.</span></span> |
|---------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-192">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-192">Error message</span></span>       | <span data-ttu-id="8670f-193">フォーム %1 の ExecuteQuery メソッドに、super() の後に add range を追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="8670f-193">Add range after super() should not be added in ExecuteQuery method for form %1</span></span>                                 |
| <span data-ttu-id="8670f-194">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-194">Issue type/severity</span></span> | <span data-ttu-id="8670f-195">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-195">Code/Warning</span></span>                                                                                                   |
| <span data-ttu-id="8670f-196">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-196">How to fix it</span></span>       | <span data-ttu-id="8670f-197">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="8670f-197">Refactor your code to avoid this pattern.</span></span>                                                                      |

### <a name="bpcheckinvalidinitformmethod"></a><span data-ttu-id="8670f-198">BPCheckInvalidInitFormMethod</span><span class="sxs-lookup"><span data-stu-id="8670f-198">BPCheckInvalidInitFormMethod</span></span>

| <span data-ttu-id="8670f-199">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-199">Description</span></span>         | <span data-ttu-id="8670f-200">このルールは、**super()** を呼び出す前に、フォームのコントロールとデータソースをフォームの **init** メソッドで初期化しないようにします。</span><span class="sxs-lookup"><span data-stu-id="8670f-200">This rule makes sure that you don't initialize form controls and data sources in a form’s **init** method before you call **super()**.</span></span> <span data-ttu-id="8670f-201">**element** または **this** を **super()** に対する呼び出し (**this.aMethod()** または **element.aMethod()**) の前に使用するステートメントが検出された場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-201">It fails if it finds a statement that uses **element** or **this** before the call to **super()** (**this.aMethod()** or **element.aMethod()**).</span></span> <span data-ttu-id="8670f-202">情報メッセージは番号順序の初期化など許可されたいくつかのパターンのみを表示します (**numberSeqPreInit**) 。</span><span class="sxs-lookup"><span data-stu-id="8670f-202">An informational message is shown only for some allowed patterns, such as initializing number sequences (**numberSeqPreInit**).</span></span> |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-203">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-203">Error message</span></span>       | <span data-ttu-id="8670f-204">フォーム要素ステートメントは、フォーム %1 の init メソッドで、super() の前に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8670f-204">Form element statements should not be used before super() in init method of form %1</span></span>                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8670f-205">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-205">Issue type/severity</span></span> | <span data-ttu-id="8670f-206">コード/情報または警告</span><span class="sxs-lookup"><span data-stu-id="8670f-206">Code/Info or Warning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8670f-207">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-207">How to fix it</span></span>       | <span data-ttu-id="8670f-208">**super()** の呼び出し後、コードをリファクターしてフォーム コントロールおよびデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8670f-208">Refactor your code to access form controls and data after the call to **super()**.</span></span> <span data-ttu-id="8670f-209">コードが任意のフォーム コントロールを初期化せず、**super()** の前にどのフォーム データ ソースにもアクセスしない場合、Microsoft にカスタマイズ分析のレポートを送信するときに例外をまとめます。</span><span class="sxs-lookup"><span data-stu-id="8670f-209">If your code doesn't initialize any form control and doesn't access any form data sources before **super()**, document an exception when you submit your Customization Analysis Report to Microsoft.</span></span>                                                                                                                                 |

### <a name="bpcheckemptyloop"></a><span data-ttu-id="8670f-210">BPCheckEmptyLoop</span><span class="sxs-lookup"><span data-stu-id="8670f-210">BPCheckEmptyLoop</span></span>

| <span data-ttu-id="8670f-211">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-211">Description</span></span>         | <span data-ttu-id="8670f-212">このルールは、ステートメントがないループを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-212">This rule fails if it finds loops that have no statements.</span></span> |
|---------------------|------------------------------------------------------------|
| <span data-ttu-id="8670f-213">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-213">Error message</span></span>       | <span data-ttu-id="8670f-214">クラス %2 の メソッド %1 で空のループが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="8670f-214">Empty loop found in method %1 in class %2</span></span>                  |
| <span data-ttu-id="8670f-215">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-215">Issue type/severity</span></span> | <span data-ttu-id="8670f-216">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-216">Code/Warning</span></span>                                               |
| <span data-ttu-id="8670f-217">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-217">How to fix it</span></span>       | <span data-ttu-id="8670f-218">ループをコードから削除します。</span><span class="sxs-lookup"><span data-stu-id="8670f-218">Remove the loop from your code.</span></span>                            |

### <a name="bpchecklockqueryrange"></a><span data-ttu-id="8670f-219">BPCheckLockQueryRange</span><span class="sxs-lookup"><span data-stu-id="8670f-219">BPCheckLockQueryRange</span></span>

| <span data-ttu-id="8670f-220">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-220">Description</span></span>         | <span data-ttu-id="8670f-221">フォームの **init** メソッドでコードが **AddRange** を呼び出し、その範囲をロックまたは非表示として設定しないと、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-221">This rule fails if the code calls **AddRange** in the **init** method of the form, and doesn't set the range as locked or hidden.</span></span>      |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-222">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-222">Error message</span></span>       | <span data-ttu-id="8670f-223">フォーム %1で、範囲はロックするか、非表示にする必要があります</span><span class="sxs-lookup"><span data-stu-id="8670f-223">Range should be locked or hidden in form %1</span></span>                                                                                            |
| <span data-ttu-id="8670f-224">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-224">Issue type/severity</span></span> | <span data-ttu-id="8670f-225">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-225">Code/Warning</span></span>                                                                                                                           |
| <span data-ttu-id="8670f-226">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-226">How to fix it</span></span>       | <span data-ttu-id="8670f-227">**AddRange** の呼び出しの後に、**QueryBuildRange.status(RangeStatus::Locked)** または **QueryBuildRange.status(RangeStatus::Hidden)** を追加します。</span><span class="sxs-lookup"><span data-stu-id="8670f-227">Add **QueryBuildRange.status(RangeStatus::Locked)** or **QueryBuildRange.status(RangeStatus::Hidden)** after the call to **AddRange**.</span></span> |

### <a name="bpcheckskipstatementvalidation"></a><span data-ttu-id="8670f-228">BPCheckSkipStatementValidation</span><span class="sxs-lookup"><span data-stu-id="8670f-228">BPCheckSkipStatementValidation</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8670f-229">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-229">Description</span></span></td>
<td><span data-ttu-id="8670f-230">このルールは、<strong>Skip</strong> ステートメントを持たないセットベースの操作を検出した場合に通知メッセージを報告します。</span><span class="sxs-lookup"><span data-stu-id="8670f-230">This rule reports an informational message if it finds a set-based operation that doesn&#39;t have <strong>Skip</strong> statements.</span></span>
<ul>
<li><span data-ttu-id="8670f-231"><strong>update_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="8670f-231">When <strong>update_recordset</strong> is found, the rule checks for <strong>skipDataMethods(true)</strong>.</span></span> <span data-ttu-id="8670f-232">テーブルの <strong>update</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-232">The rule applies only when the <strong>update</strong> method on the table is overridden.</span></span></li>
<li><span data-ttu-id="8670f-233"><strong>insert_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="8670f-233">When <strong>insert_recordset</strong> is found, the rule checks for <strong>skipDataMethods(true)</strong>.</span></span> <span data-ttu-id="8670f-234">テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-234">The rule applies only when the <strong>insert</strong> method on the table is overridden.</span></span></li>
<li><span data-ttu-id="8670f-235"><strong>delete_from</strong> が見つかると、ルールによって <strong>skipDeleteActions(true)</strong> がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="8670f-235">When <strong>delete_from</strong> is found, the rule checks for <strong>skipDeleteActions(true)</strong>.</span></span> <span data-ttu-id="8670f-236">テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-236">The rule applies only when the <strong>insert</strong> method on the table is overridden.</span></span></li>
</ul>
<span data-ttu-id="8670f-237">これは、セットベースの操作のパフォーマンス向上を最大限に活用するために、<strong>スキップ</strong>メソッドを呼び出す必要があることを示す情報メッセージです。</span><span class="sxs-lookup"><span data-stu-id="8670f-237">This is an informational message that highlights the need to call <strong>skip</strong> methods to take full advantage of the performance gains of set-based operations.</span></span> <span data-ttu-id="8670f-238"><strong>スキップ</strong> メソッドが使用されていない場合は、実行は行ごとの操作に戻ります。</span><span class="sxs-lookup"><span data-stu-id="8670f-238">If <strong>skip</strong> methods aren&#39;t used, the execution falls back to a row-by-row operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-239">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-239">Error message</span></span></td>
<td><span data-ttu-id="8670f-240">セット ベースの操作はクラス %2 のメソッド %1 で Skip ステートメントを呼び出す必要があります。それ以外の場合、行ごとの操作にフォールバックされます。</span><span class="sxs-lookup"><span data-stu-id="8670f-240">Set-based operation must invoke Skip statements in method %1 in class %2; otherwise, execution will fall back to a row by row operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8670f-241">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-241">Issue type/severity</span></span></td>
<td><span data-ttu-id="8670f-242">コード/情報</span><span class="sxs-lookup"><span data-stu-id="8670f-242">Code/Information</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-243">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-243">How to fix it</span></span></td>
<td><span data-ttu-id="8670f-244">該当する場合は、<strong>skipDataMethods(true)</strong> または <strong>skipDeleteActions(true)</strong> を使用します。</span><span class="sxs-lookup"><span data-stu-id="8670f-244">Use <strong>skipDataMethods(true)</strong> or <strong>skipDeleteActions(true)</strong> when applicable.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpchecknottstryblock"></a><span data-ttu-id="8670f-245">BPCheckNoTTSTryBlock</span><span class="sxs-lookup"><span data-stu-id="8670f-245">BPCheckNoTTSTryBlock</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8670f-246">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-246">Description</span></span></td>
<td><span data-ttu-id="8670f-247">このルールは、正しく処理されない <strong>tts</strong> ブロック内の <strong>try</strong> ステートメントを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-247">This rule fails if it finds a <strong>try</strong> statement within a <strong>tts</strong> block that isn&#39;t handled correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-248">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-248">Error message</span></span></td>
<td><span data-ttu-id="8670f-249">try 文の tts ブロックは、メソッド %1 の例外を明示的にキャッチしません。</span><span class="sxs-lookup"><span data-stu-id="8670f-249">Tts block with Try statement does not explicitly catch exceptions in method %1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8670f-250">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-250">Issue type/severity</span></span></td>
<td><span data-ttu-id="8670f-251">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-251">Code/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-252">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-252">How to fix it</span></span></td>
<td><span data-ttu-id="8670f-253">次の例では、ルールが失敗するか、合格するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="8670f-253">The following examples show when the rule will fail or pass.</span></span> <span data-ttu-id="8670f-254">次の例を参考にして、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="8670f-254">Use these examples as guidelines to refactor your code.</span></span>
<pre><code>ttsbegin;
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
catch(Exception::UpdateConflictNotRecovered) {}</code></pre></td>
</tr>
</tbody>
</table>

### <a name="bpcheckemptytablemethod"></a><span data-ttu-id="8670f-255">BPCheckEmptyTableMethod</span><span class="sxs-lookup"><span data-stu-id="8670f-255">BPCheckEmptyTableMethod</span></span>

| <span data-ttu-id="8670f-256">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-256">Description</span></span>         | <span data-ttu-id="8670f-257">このルールは、ソース コードのないテーブル メソッドをチェックします。</span><span class="sxs-lookup"><span data-stu-id="8670f-257">This rule checks for table methods that have no source code.</span></span> <span data-ttu-id="8670f-258">空テーブルのメソッドは、テーブルのレコードセット オペレーションを行単位の操作に戻す原因となります。</span><span class="sxs-lookup"><span data-stu-id="8670f-258">Empty table methods cause record-set operations on the table to fall back to a row-by-row operation.</span></span> |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-259">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-259">Error message</span></span>       | <span data-ttu-id="8670f-260">%1 テーブルに空の %2 メソッドがあります</span><span class="sxs-lookup"><span data-stu-id="8670f-260">%1 table has an empty %2 method</span></span>                                                                                                                                   |
| <span data-ttu-id="8670f-261">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-261">Issue type/severity</span></span> | <span data-ttu-id="8670f-262">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-262">Code/Warning</span></span>                                                                                                                                                      |
| <span data-ttu-id="8670f-263">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-263">How to fix it</span></span>       | <span data-ttu-id="8670f-264">このメソッドをコードから削除します。</span><span class="sxs-lookup"><span data-stu-id="8670f-264">Remove this method from your code.</span></span>                                                                                                                                |

### <a name="bpcheckbatchjobsenabled"></a><span data-ttu-id="8670f-265">BPCheckBatchJobsEnabled</span><span class="sxs-lookup"><span data-stu-id="8670f-265">BPCheckBatchJobsEnabled</span></span>

| <span data-ttu-id="8670f-266">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-266">Description</span></span>         | <span data-ttu-id="8670f-267">このルールは、**RunBaseBatch** を拡張するすべてのクラスが **true** を返す **canGoBatch** メソッドを持つことを保証します。</span><span class="sxs-lookup"><span data-stu-id="8670f-267">This rule makes sure that all classes that extend **RunBaseBatch** have a **canGoBatch** method that returns **true**.</span></span> |
|---------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-268">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-268">Error message</span></span>       | <span data-ttu-id="8670f-269">カスタム ジョブがクラス %1 でバッチ対応でありません</span><span class="sxs-lookup"><span data-stu-id="8670f-269">Custom job is not batch-enabled in class %1</span></span>                                                                            |
| <span data-ttu-id="8670f-270">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-270">Issue type/severity</span></span> | <span data-ttu-id="8670f-271">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-271">Code/Warning</span></span>                                                                                                           |
| <span data-ttu-id="8670f-272">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-272">How to fix it</span></span>       | <span data-ttu-id="8670f-273">**canGoBatch** メソッドは、すべてのバッチ クラスに **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="8670f-273">The **canGoBatch** method must return **true** for all batch classes.</span></span>                                                  |

### <a name="bpcheckdisplaymethodcached"></a><span data-ttu-id="8670f-274">BPCheckDisplayMethodCached</span><span class="sxs-lookup"><span data-stu-id="8670f-274">BPCheckDisplayMethodCached</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8670f-275">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-275">Description</span></span></td>
<td><span data-ttu-id="8670f-276">データ メソッドにバインドされている各コントロールについては、これらの条件のいずれかが満たされている場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-276">For each control that is bound to a data method, this rules fails if one of these conditions is met:</span></span>
<ul>
<li><span data-ttu-id="8670f-277"><strong>データのキャッシュ方法</strong>プロパティが<strong>自動</strong>に設定され、対応するテーブルの <strong>display</strong>/<strong>edit</strong> メソッドには <strong>SysClientCacheDataMethodAttribute</strong> がなく、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</span><span class="sxs-lookup"><span data-stu-id="8670f-277">The <strong>Cache Data Method</strong> property is set to <strong>Auto</strong>, the corresponding table <strong>display</strong>/<strong>edit</strong> method doesn&#39;t have the <strong>SysClientCacheDataMethodAttribute</strong>, and the <strong>init</strong> method of the data source doesn&#39;t use <strong>CacheAddMethod</strong>.</span></span></li>
<li><span data-ttu-id="8670f-278"><strong>データのキャッシュ方法</strong> プロパティは <strong>いいえ</strong> に設定され、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</span><span class="sxs-lookup"><span data-stu-id="8670f-278">The <strong>Cache Data Method</strong> property is set to <strong>No</strong>, and the <strong>init</strong> method of the data source doesn&#39;t use <strong>CacheAddMethod</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-279">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-279">Error message</span></span></td>
<td><span data-ttu-id="8670f-280">フォーム %2 の 表示メソッド %1 がキャッシュされていません</span><span class="sxs-lookup"><span data-stu-id="8670f-280">Display method %1 in form %2 not cached</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8670f-281">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-281">Issue type/severity</span></span></td>
<td><span data-ttu-id="8670f-282">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-282">Code/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-283">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-283">How to fix it</span></span></td>
<td><span data-ttu-id="8670f-284">この警告は、次のいずれかのパターンを使用して修正することができます。</span><span class="sxs-lookup"><span data-stu-id="8670f-284">You can fix this warning by using one of the following patterns:</span></span>
<ul>
<li><span data-ttu-id="8670f-285"><strong>キャッシュ データ メソッド</strong> プロパティを <strong>はい</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="8670f-285">Set the <strong>Cache Data Method</strong> property to <strong>Yes</strong>.</span></span></li>
<li><p><span data-ttu-id="8670f-286"><strong>キャッシュ データ メソッド</strong> プロパティを <strong>自動</strong> に設定し、<strong>SysClientCacheDataMethodAttribute</strong> 属性を使用してテーブルのデータ メソッドをマークします。</span><span class="sxs-lookup"><span data-stu-id="8670f-286">Set the <strong>Cache Data Method</strong> property to <strong>Auto</strong>, and mark the data method of the table with the <strong>SysClientCacheDataMethodAttribute</strong> attribute.</span></span> <span data-ttu-id="8670f-287">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="8670f-287">Here is an example.</span></span></p>
<pre><code>[SysClientCacheDataMethodAttribute(true)]
Display TransDate myDateMethod()
{
    ...
}</code></pre></li>
<li><span data-ttu-id="8670f-288">フォームの <strong>init</strong> メソッドで <strong>CacheAddMethod</strong> を使用すると、そのメソッドをキャッシュ済みとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="8670f-288">Use <strong>CacheAddMethod</strong> in the <strong>init</strong> method of the form to mark the method as cached.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="bpchecksqlqueryininit"></a><span data-ttu-id="8670f-289">BPCheckSQLQueryInInit</span><span class="sxs-lookup"><span data-stu-id="8670f-289">BPCheckSQLQueryInInit</span></span>

| <span data-ttu-id="8670f-290">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-290">Description</span></span>         | <span data-ttu-id="8670f-291">このルールは、フォームの **init** メソッドで **while** ループを持つデータ アクセス クエリが見つかった場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-291">This rule fails if a data access query that has a **while** loop is found in the **init** method of a form.</span></span> <span data-ttu-id="8670f-292">このパターンは、フォームの初期化時にパフォーマンスの問題を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8670f-292">This pattern could cause performance issues when the form is initalized.</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-293">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-293">Error message</span></span>       | <span data-ttu-id="8670f-294">フォーム %1 の init メソッドで、while ループを持つ SQL クエリが見つかりました</span><span class="sxs-lookup"><span data-stu-id="8670f-294">SQL query with while loop was found in init method of form %1</span></span>                                                                                                                        |
| <span data-ttu-id="8670f-295">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-295">Issue type/severity</span></span> | <span data-ttu-id="8670f-296">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-296">Code/Warning</span></span>                                                                                                                                                                         |
| <span data-ttu-id="8670f-297">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-297">How to fix it</span></span>       | <span data-ttu-id="8670f-298">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="8670f-298">Refactor your code to avoid this pattern.</span></span>                                                                                                                                            |

### <a name="bpchecknewquerywithform"></a><span data-ttu-id="8670f-299">BPCheckNewQueryWithForm</span><span class="sxs-lookup"><span data-stu-id="8670f-299">BPCheckNewQueryWithForm</span></span>

| <span data-ttu-id="8670f-300">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-300">Description</span></span>         | <span data-ttu-id="8670f-301">このルールは、フォームの **init** または **executeQuery** メソッドで **new Query()** ステートメントを検出すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-301">This rule fails if it finds the **new Query()** statement in the **init** or **executeQuery** method of a form.</span></span> |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-302">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-302">Error message</span></span>       | <span data-ttu-id="8670f-303">フォーム メソッド %1 で、データ ソース クエリが上書きされます</span><span class="sxs-lookup"><span data-stu-id="8670f-303">Data source query overridden in form method %1</span></span>                                                                  |
| <span data-ttu-id="8670f-304">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-304">Issue type/severity</span></span> | <span data-ttu-id="8670f-305">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-305">Code/Warning</span></span>                                                                                                    |
| <span data-ttu-id="8670f-306">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-306">How to fix it</span></span>       | <span data-ttu-id="8670f-307">このパターンを回避するために、コードをリファクタリングします。</span><span class="sxs-lookup"><span data-stu-id="8670f-307">Refactor your code to avoid this pattern.</span></span>                                                                       |

### <a name="bpcheckselectforupdateabsent"></a><span data-ttu-id="8670f-308">BPCheckSelectForUpdateAbsent</span><span class="sxs-lookup"><span data-stu-id="8670f-308">BPCheckSelectForUpdateAbsent</span></span>

| <span data-ttu-id="8670f-309">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-309">Description</span></span>         | <span data-ttu-id="8670f-310">**Select ForUpdate** を使用してレコードを選択したが、更新が実行されていない場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-310">This rule fails if **Select ForUpdate** is used to select records, but an update isn't being performed.</span></span> <span data-ttu-id="8670f-311">このルールは、オプティミスティック同時実行制御 (OCC) が有効になっているテーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="8670f-311">This rules doesn't apply to tables that are enabled for Optimistic Concurrency Control (OCC).</span></span> |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-312">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-312">Error message</span></span>       | <span data-ttu-id="8670f-313">メソッド %1 に Select ForUpdate が実装されていません</span><span class="sxs-lookup"><span data-stu-id="8670f-313">Select ForUpdate not implemented in method %1</span></span>                                                                                                                                                         |
| <span data-ttu-id="8670f-314">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-314">Issue type/severity</span></span> | <span data-ttu-id="8670f-315">コード/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-315">Code/Warning</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="8670f-316">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-316">How to fix it</span></span>       | <span data-ttu-id="8670f-317">**ForUpdate を選択** の代わりに **選択** を使用するか、**OCC を有効** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8670f-317">Use **Select** instead of **Select ForUpdate**, or set the **OCC Enabled** property to **Yes** on the table.</span></span>                                                                                          |

### <a name="bpchecktablepropertymismatch"></a><span data-ttu-id="8670f-318">BPCheckTablePropertyMismatch</span><span class="sxs-lookup"><span data-stu-id="8670f-318">BPCheckTablePropertyMismatch</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8670f-319">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-319">Description</span></span></td>
<td><span data-ttu-id="8670f-320">このルールは、テーブルがテーブル グループに属しているが、適切な<strong>キャッシュ ルックアップ</strong>値を持たない場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-320">This rule fails when the table belongs to a table group but doesn&#39;t have the appropriate <strong>Cache Lookup</strong> value.</span></span> <span data-ttu-id="8670f-321">次の条件がすべて満たされていると、ルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-321">The rule fails if one of these conditions is met:</span></span>
<ul>
<li><span data-ttu-id="8670f-322"><strong>テーブル グループ</strong> プロパティは <strong>メイン</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> または <strong>EntireTable</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-322">The <strong>Table Group</strong> property is set to <strong>Main</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>NotinTTS</strong> or <strong>EntireTable</strong>.</span></span></li>
<li><span data-ttu-id="8670f-323"><strong>テーブル グループ</strong> プロパティは <strong>グループ</strong> または <strong>パラメーター</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-323">The <strong>Table Group</strong> property is set to <strong>Group</strong> or <strong>Parameter</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>NotinTTS</strong>.</span></span></li>
<li><span data-ttu-id="8670f-324"><strong>テーブル グループ</strong> プロパティは <strong>WorksheetHeader</strong>、<strong>WorksheetLine</strong>、または <strong>Transaction</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>Found</strong>、<strong>FoundAndEmpty</strong>、または <strong>EntireTable</strong> に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-324">The <strong>Table Group</strong> property is set to <strong>WorksheetHeader</strong>, <strong>WorksheetLine</strong>, or <strong>Transaction</strong>, and the <strong>Cache Lookup</strong> property is set to <strong>Found</strong>, <strong>FoundAndEmpty</strong>, or <strong>EntireTable</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-325">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-325">Error message</span></span></td>
<td><span data-ttu-id="8670f-326">%1 テーブルにテーブル グループとキャッシュ ルックアップの無効な組み合わせがあります</span><span class="sxs-lookup"><span data-stu-id="8670f-326">%1 table has an invalid combination of table group and cache lookup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8670f-327">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-327">Issue type/severity</span></span></td>
<td><span data-ttu-id="8670f-328">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-328">MetaData/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-329">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-329">How to fix it</span></span></td>
<td><span data-ttu-id="8670f-330">テーブルで適切な <strong>キャッシュ ルックアップ</strong> 値を設定します。</span><span class="sxs-lookup"><span data-stu-id="8670f-330">Set an appropriate <strong>Cache Lookup</strong> value on the table.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpcheckmissingdeleteactions"></a><span data-ttu-id="8670f-331">BPCheckMissingDeleteActions</span><span class="sxs-lookup"><span data-stu-id="8670f-331">BPCheckMissingDeleteActions</span></span>

| <span data-ttu-id="8670f-332">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-332">Description</span></span>         | <span data-ttu-id="8670f-333">このルールは、テーブル関係の**削除**アクションまたは**削除時**プロパティの値が**なし**と等しくないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="8670f-333">This rule validates that the value of either a **delete** action or the **On Delete** property of a table relation isn't equal to **None**.</span></span> <span data-ttu-id="8670f-334">関連するテーブルまたは現在のテーブルが tempDB、メモリ テーブル、参照テーブル、ステージング テーブル、パラメーター テーブルの場合、ルールはトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="8670f-334">The rule isn't triggered when the related or current table is a tempDB, in memory table, reference table, staging table, or parameter table.</span></span> |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-335">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-335">Error message</span></span>       | <span data-ttu-id="8670f-336">リレーション名 %3 でテーブル %2 に関連付けられているテーブル %1 に欠けているアクションを削除します</span><span class="sxs-lookup"><span data-stu-id="8670f-336">Delete actions missing in table %1 which is related to table %2 with relation name %3</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="8670f-337">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-337">Issue type/severity</span></span> | <span data-ttu-id="8670f-338">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-338">MetaData/Warning</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8670f-339">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-339">How to fix it</span></span>       | <span data-ttu-id="8670f-340">**None** と等しくない **delete** アクションを設定します。</span><span class="sxs-lookup"><span data-stu-id="8670f-340">Set a **delete** action value that isn't equal to **None**.</span></span>                                                                                                                                                                                                                              |

### <a name="bpcheckaddressmodel"></a><span data-ttu-id="8670f-341">BPCheckAddressModel</span><span class="sxs-lookup"><span data-stu-id="8670f-341">BPCheckAddressModel</span></span>

| <span data-ttu-id="8670f-342">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-342">Description</span></span>         | <span data-ttu-id="8670f-343">テーブル フィールドが **AddressZipCodeId** または **AddressStateId** タイプの場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-343">This rule fails if a table field is of the **AddressZipCodeId** or **AddressStateId** type.</span></span> <span data-ttu-id="8670f-344">これらのタイプは、コードが新しいアドレス フレームワークを受け入れなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="8670f-344">These types indicate that the code didn't uptake the newer Address framework.</span></span> |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-345">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-345">Error message</span></span>       | <span data-ttu-id="8670f-346">テーブル %2 のフィールド %1 は、アドレスの場所モデルの一部ではありません</span><span class="sxs-lookup"><span data-stu-id="8670f-346">Field %1 of table %2 is not part of address location model</span></span>                                                                                                                |
| <span data-ttu-id="8670f-347">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-347">Issue type/severity</span></span> | <span data-ttu-id="8670f-348">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-348">MetaData/Warning</span></span>                                                                                                                                                          |
| <span data-ttu-id="8670f-349">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-349">How to fix it</span></span>       | <span data-ttu-id="8670f-350">これらのタイプをディレクトリ モデルのその他の適切な EDT タイプに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8670f-350">Replace these types with any other appropriate EDT type in the Directory model.</span></span>                                                                                           |

### <a name="bpcheckdimensionmodel"></a><span data-ttu-id="8670f-351">BPCheckDimensionModel</span><span class="sxs-lookup"><span data-stu-id="8670f-351">BPCheckDimensionModel</span></span>

| <span data-ttu-id="8670f-352">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-352">Description</span></span>         | <span data-ttu-id="8670f-353">テーブル フィールドが、**分析コード**または **LedgerAccount** タイプの場合、このルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-353">This rule fails if a table field is of the **Dimension** or **LedgerAccount** type.</span></span> <span data-ttu-id="8670f-354">これらのタイプは、コードが新しい財務分析コード フレームワークを受け入れなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="8670f-354">These types indicate that the code didn't uptake the newer Financial Dimension framework.</span></span> |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-355">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-355">Error message</span></span>       | <span data-ttu-id="8670f-356">テーブル %2 のフィールド %1 は、財務分析コード フレームワークの一部ではありません</span><span class="sxs-lookup"><span data-stu-id="8670f-356">Field %1 of table %2 is not part of financial dimension framework</span></span>                                                                                                             |
| <span data-ttu-id="8670f-357">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-357">Issue type/severity</span></span> | <span data-ttu-id="8670f-358">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-358">MetaData/Warning</span></span>                                                                                                                                                              |
| <span data-ttu-id="8670f-359">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-359">How to fix it</span></span>       | <span data-ttu-id="8670f-360">これらのタイプを分析コード モデルのその他の適切な EDT タイプに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8670f-360">Replace these types with any other appropriate EDT type in the Dimensions model.</span></span>                                                                                              |

### <a name="bpchecknumberofnewfields"></a><span data-ttu-id="8670f-361">BPCheckNumberofNewFields</span><span class="sxs-lookup"><span data-stu-id="8670f-361">BPCheckNumberofNewFields</span></span>

| <span data-ttu-id="8670f-362">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-362">Description</span></span>         | <span data-ttu-id="8670f-363">このルールは、そのテーブルのカスタマイズまたは拡張のプロセスで、テーブルに 10 個以下のフィールドが追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8670f-363">This rule verifies that no more than 10 fields were added to a table during the process of customizing or extending that table.</span></span> <span data-ttu-id="8670f-364">このルールは、ステージング テーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="8670f-364">This rule doesn't apply to staging tables.</span></span> |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-365">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-365">Error message</span></span>       | <span data-ttu-id="8670f-366">次の値より大きいテーブル %1 の新しいフィールドの数</span><span class="sxs-lookup"><span data-stu-id="8670f-366">Number of new fields in table %1 is greater than</span></span>                                                                                                                           |
| <span data-ttu-id="8670f-367">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-367">Issue type/severity</span></span> | <span data-ttu-id="8670f-368">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-368">Metadata/Warning</span></span>                                                                                                                                                           |
| <span data-ttu-id="8670f-369">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-369">How to fix it</span></span>       | <span data-ttu-id="8670f-370">スキーマをリファクタリングし、既存のテーブルに多数のフィールドを追加する代わりに関連するテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8670f-370">Refactor your schema and create related tables instead of adding too many fields to an existing table.</span></span>                                                                     |

### <a name="bpcheckenumupgradeissue"></a><span data-ttu-id="8670f-371">BPCheckEnumUpgradeIssue</span><span class="sxs-lookup"><span data-stu-id="8670f-371">BPCheckEnumUpgradeIssue</span></span>

| <span data-ttu-id="8670f-372">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-372">Description</span></span>         | <span data-ttu-id="8670f-373">このルールは、次の条件が満たされた場合に失敗します。列挙型 (オーバーレイ) をカスタマイズすると、新しい列挙型の値は既存の最大値 + 10 未満になります。</span><span class="sxs-lookup"><span data-stu-id="8670f-373">This rule fails when the following condition is met: When you customize an enum (overlayer), new enum values are less than the maximum existing value + 10.</span></span> <span data-ttu-id="8670f-374">このルールは、拡張可能な列挙型には適用されません。</span><span class="sxs-lookup"><span data-stu-id="8670f-374">This rules doesn't apply to extensible enums.</span></span> |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-375">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-375">Error message</span></span>       | <span data-ttu-id="8670f-376">列挙 %1 で、アップグレード問題があります。</span><span class="sxs-lookup"><span data-stu-id="8670f-376">Enum %1 will have upgrade issues</span></span>                                                                                                                                                                          |
| <span data-ttu-id="8670f-377">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-377">Issue type/severity</span></span> | <span data-ttu-id="8670f-378">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-378">MetaData/Warning</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="8670f-379">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-379">How to fix it</span></span>       | <span data-ttu-id="8670f-380">大きな列挙値を使用するか、列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="8670f-380">Use larger enum values, or extend the enum.</span></span>                                                                                                                                                               |

### <a name="bpcheckpassivejoinuse"></a><span data-ttu-id="8670f-381">BPCheckPassiveJoinUse</span><span class="sxs-lookup"><span data-stu-id="8670f-381">BPCheckPassiveJoinUse</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8670f-382">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-382">Description</span></span></td>
<td><span data-ttu-id="8670f-383">このルールは、フォームがデータのプリロードを許可する場合、タブ ページ データソースのリンク タイプがパッシブであることを検証します。</span><span class="sxs-lookup"><span data-stu-id="8670f-383">This rule validates that, when a form allows for pre-loading of data, the link type of tab page data sources is passive.</span></span> <span data-ttu-id="8670f-384">次の条件がすべて満たされていると、ルールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8670f-384">The rule fails if all the following conditions are met:</span></span>
<ul>
<li><span data-ttu-id="8670f-385"><strong>Yes</strong> に設定された <strong>AllowPreLoading</strong> プロパティのフォームがあります。</span><span class="sxs-lookup"><span data-stu-id="8670f-385">A form has the <strong>AllowPreLoading</strong> property set to <strong>Yes</strong>.</span></span></li>
<li><span data-ttu-id="8670f-386">フォームのタブ ページは、最上位レベルのデータ ソースにバインドされています。</span><span class="sxs-lookup"><span data-stu-id="8670f-386">A tab page on the form is bound to a top-level data source.</span></span></li>
<li><span data-ttu-id="8670f-387">データ ソースの<strong>結合ソース</strong>プロパティが設定されます。</span><span class="sxs-lookup"><span data-stu-id="8670f-387">The data source’s <strong>Join Source </strong>property is set.</span></span></li>
<li><span data-ttu-id="8670f-388">データ ソースの<strong>リンク タイプ</strong> プロパティが<strong>パッシブ</strong>に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="8670f-388">The data source’s <strong>Link Type</strong> property isn&#39;t set to <strong>Passive</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-389">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-389">Error message</span></span></td>
<td><span data-ttu-id="8670f-390">新しいメッセージは、「フォーム %2 のタブ ページ コントロールにバインドされているデータ ソース %1 にパッシブ結合を使用する」ことを提案しています</span><span class="sxs-lookup"><span data-stu-id="8670f-390">New message suggest: “Use passive joins on data sources %1 bound to a tab page control in form %2”</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8670f-391">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-391">Issue type/severity</span></span></td>
<td><span data-ttu-id="8670f-392">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-392">MetaData/Warning</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8670f-393">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-393">How to fix it</span></span></td>
<td><span data-ttu-id="8670f-394">フォームで <strong>AllowPreLoading</strong> プロパティを <strong>いいえ</strong> に設定するか、データ ソースでパッシブ結合を使用します。</span><span class="sxs-lookup"><span data-stu-id="8670f-394">Set the <strong>AllowPreLoading</strong> property to <strong>No</strong> on the form, or use passive joins on the data source.</span></span> <span data-ttu-id="8670f-395">パッシブ結合では、タブ ページのクエリの実行時に明示的にプログラミングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8670f-395">Passive joins require that you explicitly program when the query of a tab page is run.</span></span></td>
</tr>
</tbody>
</table>

### <a name="bpcheckaltenatekeyabsent"></a><span data-ttu-id="8670f-396">BPCheckAltenateKeyAbsent</span><span class="sxs-lookup"><span data-stu-id="8670f-396">BPCheckAltenateKeyAbsent</span></span>

| <span data-ttu-id="8670f-397">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-397">Description</span></span>         | <span data-ttu-id="8670f-398">このルールは、一意のインデックスを持つテーブルに少なくとも 1 つの代替キーがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8670f-398">This rule verifies that tables that have a unique index have at least one alternate key.</span></span> |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-399">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-399">Error message</span></span>       | <span data-ttu-id="8670f-400">テーブル %1 には、代替キーがありません</span><span class="sxs-lookup"><span data-stu-id="8670f-400">Table %1 does not have an alternate key</span></span>                                                  |
| <span data-ttu-id="8670f-401">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-401">Issue type/severity</span></span> | <span data-ttu-id="8670f-402">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-402">MetaData/Warning</span></span>                                                                         |
| <span data-ttu-id="8670f-403">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-403">How to fix it</span></span>       | <span data-ttu-id="8670f-404">テーブルの一意のインデックスで **代替キー** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8670f-404">Set the **Alternate Key** property to **Yes** on a unique index of the table.</span></span>            |

### <a name="bpcheckbasetablemodified"></a><span data-ttu-id="8670f-405">BPCheckBaseTableModified</span><span class="sxs-lookup"><span data-stu-id="8670f-405">BPCheckBaseTableModified</span></span>

| <span data-ttu-id="8670f-406">説明</span><span class="sxs-lookup"><span data-stu-id="8670f-406">Description</span></span>         | <span data-ttu-id="8670f-407">このルールは、Microsoft によって出荷される特定のベース テーブルの一覧のカスタマイズ (オーバーレイ化) を推奨しません。</span><span class="sxs-lookup"><span data-stu-id="8670f-407">This rule discourages the customization (overlayering) of a list of specific base tables that are shipped by Microsoft.</span></span> <span data-ttu-id="8670f-408">例では、SourceDocumentHeader および SourceDocumentLine テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="8670f-408">Examples are the SourceDocumentHeader and SourceDocumentLine tables.</span></span> |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8670f-409">エラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="8670f-409">Error message</span></span>       | <span data-ttu-id="8670f-410">%1 はベース テーブルであり、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="8670f-410">%1 is a base table and must not be modified</span></span>                                                                                                                                                  |
| <span data-ttu-id="8670f-411">出庫タイプ/重要度</span><span class="sxs-lookup"><span data-stu-id="8670f-411">Issue type/severity</span></span> | <span data-ttu-id="8670f-412">メタデータ/警告</span><span class="sxs-lookup"><span data-stu-id="8670f-412">MetaData/Warning</span></span>                                                                                                                                                                             |
| <span data-ttu-id="8670f-413">修正する方法</span><span class="sxs-lookup"><span data-stu-id="8670f-413">How to fix it</span></span>       | <span data-ttu-id="8670f-414">テーブルをカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="8670f-414">Don't customize the table.</span></span>                                                                                                                                                                   |





