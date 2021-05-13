---
title: テスト ケースのチェーンへの変数のコピー
description: このトピックでは、 Regression Suite Automation Tool を使用してテスト ケースを連鎖させる方法 (テストが他のテストに値を渡す機能) について説明します。
author: FrankDahl
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 317b428aa1601a35ff383408906cca86434896b1
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865936"
---
# <a name="copy-variables-to-chain-test-cases"></a><span data-ttu-id="d6609-103">テスト ケースのチェーンへの変数のコピー</span><span class="sxs-lookup"><span data-stu-id="d6609-103">Copy variables to chain test cases</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6609-104">Regression Suite Automation Tool の主要な機能の１つとして、テスト ケースの連鎖、つまり、テストが他のテストに値を渡す機能、があります。</span><span class="sxs-lookup"><span data-stu-id="d6609-104">One of the key features of the Regression Suite Automation Tool is the chaining of test cases, that is, the ability of a test to pass values to other tests.</span></span> <span data-ttu-id="d6609-105">テスト ケースは、 Azure DevOps テスト計画内で定義されている順序に従って実行され、テスト ツール自体で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="d6609-105">Test cases are executed according to their defined order in the Azure DevOps test plan, which can also be updated in the test tool itself.</span></span> <span data-ttu-id="d6609-106">１つのテスト ケースから別のテスト ケースに変数を渡す場合は、テストを正しく順序付けることが重要です。</span><span class="sxs-lookup"><span data-stu-id="d6609-106">It is important to correctly order the tests if you want to pass variables from one test case to the other.</span></span>

<span data-ttu-id="d6609-107">タスク レコーダーでテストを記録しながら変数の値を保存するには、次の図に示すように、フィールドを右クリックして **タスク レコーダー > コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d6609-107">To save the value of a variable while recording the test in Task Recorder, right-click the field and select **Task recorder > Copy**, as shown in the following image.</span></span> <span data-ttu-id="d6609-108">コピーすると、変数は記録ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="d6609-108">Copying will save the variable in the recording file.</span></span> <span data-ttu-id="d6609-109">この変数は、後続のテストで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d6609-109">This variable can be used in subsequent tests.</span></span>

:::image type="content" source="media/task-recorder-copy.png" alt-text="タスク レコーダーのメニュー項目のコピー":::

<span data-ttu-id="d6609-111">RSAT が Excel パラメーター ファイルを生成する場合、保存された変数は **一般** タブの **保存された変数** テーブルに表示されます。これらの変数は、**TestCaseSteps** タブのテスト ケース ステップのコンテキストにも表示されます。次の画像内では、テスト ケースの記録中に発注書 ID の値がコピーされています (手順 5)。</span><span class="sxs-lookup"><span data-stu-id="d6609-111">When RSAT generates the Excel parameters file, saved variables appear in the **Saved variables** table on the **General** Tab. These variables also appear in the context of the test case steps in the **TestCaseSteps** tab. In the image below, the purchase order ID value was copied during the recording of the test case (step 5).</span></span> <span data-ttu-id="d6609-112">この値は **{{PurchCreateOrder_PurchTable_PurchId_86_Copy}}** という名前の変数に格納されます 。</span><span class="sxs-lookup"><span data-stu-id="d6609-112">This value is stored in a variable named **{{PurchCreateOrder_PurchTable_PurchId_86_Copy}}**.</span></span>

![Excel に保存された変数](media/saved-variables.png)

<span data-ttu-id="d6609-114">これらの変数をテスト再生中に再利用するには、次に示すように、変数名をコピーして、別のテスト (または同じテスト) のデータ ファイルでパラメーター値の代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="d6609-114">To reuse these variables during test playback, copy the variable name and use it in place of a parameter value in the data file of another test (or the same test), as shown below.</span></span>

![Excel での変数の再利用](media/reuse-variables.png)

<span data-ttu-id="d6609-116">変数は、定義されている同じテストケースで使用できます。また、同じテストの実行中にテスト間で渡すこともできます。</span><span class="sxs-lookup"><span data-stu-id="d6609-116">Variables can be used in the same test case where they are defined and can also be passed between tests during the same test run.</span></span>

## <a name="support-for-formulas-of-saved-variables"></a><span data-ttu-id="d6609-117">保存された変数の式のサポート</span><span class="sxs-lookup"><span data-stu-id="d6609-117">Support for formulas of saved variables</span></span>

<span data-ttu-id="d6609-118">保存された (コピーされた) 変数を含むフォーミュラを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d6609-118">You can create formulas that contain saved (copied) variables.</span></span> <span data-ttu-id="d6609-119">Regression Suite Automation Tool の古いバージョンのを使用している場合、この機能を利用するためには新しいExcel パラメーター ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6609-119">If you have been using an older version of the Regression Suite Automation Tool, you will need to regenerate new Excel parameter files to take advantage of this functionality.</span></span> <span data-ttu-id="d6609-120">サポートされている演算子は、`+`, `-`, `/` および '\' です。</span><span class="sxs-lookup"><span data-stu-id="d6609-120">Supported operators are `+`, `-`, `/` and '\'.</span></span> <span data-ttu-id="d6609-121">Regression Suite Automation Tool 式で使用できるのは、数値変数のみです。</span><span class="sxs-lookup"><span data-stu-id="d6609-121">Only numerical variables can be used in the Regression Suite Automation Tool formulas.</span></span> <span data-ttu-id="d6609-122">文字列または日付はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d6609-122">Strings or dates are not supported.</span></span> <span data-ttu-id="d6609-123">変数名は常に二重の中かっこ `{{varname}}` で指定します。</span><span class="sxs-lookup"><span data-stu-id="d6609-123">Always specify variable names within double braces `{{varname}}`.</span></span> <span data-ttu-id="d6609-124">たとえば、`{{var1}} + {{var2}}`。</span><span class="sxs-lookup"><span data-stu-id="d6609-124">For example, `{{var1}} + {{var2}}`.</span></span>

<span data-ttu-id="d6609-125">次の図では、2つの異なる変数が式で使用されています。</span><span class="sxs-lookup"><span data-stu-id="d6609-125">In the image below, two different variables are used in a formula.</span></span>

![Excelでの式の作成](media/formulas.png)

<span data-ttu-id="d6609-127">RSAT バージョン 1.220 の時点では、**ROUND**、**CONCAT**、**UPPER** などの Excel 関数を使用して、RAST 変数を使用した式を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d6609-127">As of RSAT version 1.220, you can also use Excel functions, such as **ROUND**, **CONCAT**, and **UPPER**, to create formulas with RSAT variables.</span></span> <span data-ttu-id="d6609-128">この機能は、Excel 式評価機能を使用して実装されるため、Excel でサポートされている関数は RSAT でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d6609-128">This feature is implemented using the Excel formula evaluation functionality, so any function supported by Excel is supported by RSAT.</span></span>

<span data-ttu-id="d6609-129">次にその例を示します。</span><span class="sxs-lookup"><span data-stu-id="d6609-129">For example,</span></span>

+ <span data-ttu-id="d6609-130">数値を最も近い整数に丸めるには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d6609-130">To round a value into the nearest whole number, use:</span></span>

    `=ROUND({{Item_Price_3274_Copy}}, 0)`

+ <span data-ttu-id="d6609-131">文字列を連結するには、以下を使用します。</span><span class="sxs-lookup"><span data-stu-id="d6609-131">To concatenate strings, use:</span></span>

    `=CONCATENATE({{AccountNum_3274_Copy}}, " ", {{ AddressBP_Locator_3274_Copy}})`

+ <span data-ttu-id="d6609-132">日付を計算して文字列に変換するには、以下を使用します。</span><span class="sxs-lookup"><span data-stu-id="d6609-132">To calculate and format a date and convert it to a string, use:</span></span>

    `=TEXT(DATEVALUE({{SystemDate_CurrentDate_3276_Copy}}) - 1, "mm/dd/yyyy")`

    <span data-ttu-id="d6609-133">信頼性の高いテスト ケースを実行するため、必ず RSAT の日付値をテキストに変換してください。</span><span class="sxs-lookup"><span data-stu-id="d6609-133">Always convert RSAT date values to text for reliable test case execution.</span></span>

<span data-ttu-id="d6609-134">RSAT では、テストの実行中にこれらの式が評価されるため、式の前に単一引用符 **\'** を付ける必要があります。これにより、Excel で式が不完全に計算されるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="d6609-134">RSAT evaluates these formulas during test execution, so you must precede the formula with a single quote **\'** to prevent Excel from attempting to prematurely calculate the formula.</span></span> <span data-ttu-id="d6609-135">この図には、例が示されています。</span><span class="sxs-lookup"><span data-stu-id="d6609-135">An example is shown in this image.</span></span>

![Excel 2 での式の作成](media/formulas-2.png)

## <a name="use-variables-in-message-validation"></a><span data-ttu-id="d6609-137">メッセージ検証での変数の使用</span><span class="sxs-lookup"><span data-stu-id="d6609-137">Use variables in message validation</span></span>

<span data-ttu-id="d6609-138">保存された変数を、メッセージ検証タブの文字列の一部として使用することもできます。以下は、`Customer account {{variable name}} already exists.` というメッセージを検証する例です。</span><span class="sxs-lookup"><span data-stu-id="d6609-138">You can also use a saved variable as part of a string in the Message Validation tab. Here is an example that validates that the message `Customer account {{variable name}} already exists.`.</span></span> <span data-ttu-id="d6609-139">これは、テストの実行中に情報ログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d6609-139">It appears in the Infolog during test execution.</span></span> <span data-ttu-id="d6609-140">`{{variable name}}` は、記録中にコピーされる変数です。</span><span class="sxs-lookup"><span data-stu-id="d6609-140">`{{variable name}}` is a variable that is copied during the recording.</span></span>

<span data-ttu-id="d6609-141">保存済 (コピー済) 変数は、同じテスト ケース内で、または同じテスト スイート内の複数のテスト ケース間で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d6609-141">Saved (Copied) variables can be used within the same test case or across more than one test case in the same test suite.</span></span>

![変数を含むメッセージ](media/rsat-message-with-variable.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]