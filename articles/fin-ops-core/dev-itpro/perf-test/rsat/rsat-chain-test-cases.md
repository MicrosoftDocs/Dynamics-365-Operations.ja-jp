---
title: テスト ケースのチェーンへの変数のコピー
description: このトピックでは、 Regression Suite Automation Tool を使用してテスト ケースを連鎖させる方法 (テストが他のテストに値を渡す機能) について説明します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c625bc4f9ce57489c20a9f4f0e490d4df8d5f6f2
ms.sourcegitcommit: c5ef9a1d1853095ab537389b9a8e2d2adb39ed8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2020
ms.locfileid: "3033079"
---
# <a name="copy-variables-to-chain-test-cases"></a><span data-ttu-id="7e006-103">テスト ケースのチェーンへの変数のコピー</span><span class="sxs-lookup"><span data-stu-id="7e006-103">Copy variables to chain test cases</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e006-104">Regression Suite Automation Tool の主要な機能の１つとして、テスト ケースの連鎖、つまり、テストが他のテストに値を渡す機能、があります。</span><span class="sxs-lookup"><span data-stu-id="7e006-104">One of the key features of the Regression Suite Automation Tool is the chaining of test cases, that is, the ability of a test to pass values to other tests.</span></span> <span data-ttu-id="7e006-105">テスト ケースは、 Azure DevOps テスト計画内で定義されている順序に従って実行され、テスト ツール自体で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="7e006-105">Test cases are executed according to their defined order in the Azure DevOps test plan, which can also be updated in the test tool itself.</span></span> <span data-ttu-id="7e006-106">１つのテスト ケースから別のテスト ケースに変数を渡す場合は、テストを正しく順序付けることが重要です。</span><span class="sxs-lookup"><span data-stu-id="7e006-106">It is important to correctly order the tests if you want to pass variables from one test case to the other.</span></span>

<span data-ttu-id="7e006-107">タスク レコーダーでテストを記録しながら変数の値を保存するには、次に示すように、フィールドを右クリックして **タスク レコーダー > コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e006-107">To save the value of a variable while recording the test in Task Recorder, right-click the field and select **Task recorder > Copy**, as shown below.</span></span> <span data-ttu-id="7e006-108">これにより、変数が記録ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="7e006-108">This will save the variable in the recording file.</span></span> <span data-ttu-id="7e006-109">この変数は、後続のテストで使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e006-109">This variable can be used in subsequent tests.</span></span> 
 
![タスク レコーダーのメニュー項目のコピー](media/task-recorder-copy.png)

<span data-ttu-id="7e006-111">RSAT が Excel パラメーター ファイルを生成すると、これらの保存された値が、**一般**タブの**保存された変数**テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e006-111">When RSAT generates the Excel parameters file, these saved values appear in the **Saved variables** table on the **General** Tab.</span></span>
 
![Excel に保存された変数](media/saved-variables.png)
 
<span data-ttu-id="7e006-113">テスト再生時にこれらの変数を再利用するには、次に示すように、変数名をコピーして、別のテスト (または同じテスト) のデータ ファイルでパラメーター値の代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="7e006-113">To reuse these variables during test play back, copy the variable name and use it in place of a parameter value in the data file of another test (or the same test), as shown below.</span></span> 
 
![Excel での変数の再利用](media/reuse-variables.png)
 
<span data-ttu-id="7e006-115">変数は、定義されている同じテストケースで使用できます。また、同じテストの実行中にテスト間で渡すこともできます。</span><span class="sxs-lookup"><span data-stu-id="7e006-115">Variables can be used in the same test case where they are defined and can also be passed between tests during the same test run.</span></span>

## <a name="support-for-formulas-of-saved-variables"></a><span data-ttu-id="7e006-116">保存された変数の式のサポート</span><span class="sxs-lookup"><span data-stu-id="7e006-116">Support for formulas of saved variables</span></span>

<span data-ttu-id="7e006-117">保存された (コピーされた) 変数を含むフォーミュラを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7e006-117">You can create formulas that contain saved (copied) variables.</span></span> <span data-ttu-id="7e006-118">Regression Suite Automation Tool の古いバージョンのを使用している場合、この機能を利用するためには新しいExcel パラメーター ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e006-118">If you have been using an older version of the Regression Suite Automation Tool, you will need to regenerate new Excel parameter files to take advantage of this functionality.</span></span> <span data-ttu-id="7e006-119">サポートされ演算子は、 **+**、 **-**、 **/** および **\*** です。</span><span class="sxs-lookup"><span data-stu-id="7e006-119">Supported operators are **+**, **-**, **/** and **\***.</span></span> <span data-ttu-id="7e006-120">Regression Suite Automation Tool 式で使用できるのは、数値変数のみです。</span><span class="sxs-lookup"><span data-stu-id="7e006-120">Only numerical variables can be used in the Regression Suite Automation Tool formulas.</span></span> <span data-ttu-id="7e006-121">文字列または日付はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7e006-121">Strings or dates are not supported.</span></span> <span data-ttu-id="7e006-122">変数名は常に二重の中かっこ **{{varname}}** で指定します。</span><span class="sxs-lookup"><span data-stu-id="7e006-122">Always specify variable names within double braces **{{varname}}**.</span></span> <span data-ttu-id="7e006-123">たとえば、 **{{var1}} + {{var2}}**。</span><span class="sxs-lookup"><span data-stu-id="7e006-123">For example, **{{var1}} + {{var2}}**.</span></span>

<span data-ttu-id="7e006-124">次の図では、2つの異なる変数が式で使用されています。</span><span class="sxs-lookup"><span data-stu-id="7e006-124">In the image below, two different variables are used in a formula.</span></span>
 
![Excelでの式の作成](media/formulas.png)

## <a name="use-variables-in-message-validation"></a><span data-ttu-id="7e006-126">メッセージ検証での変数の使用</span><span class="sxs-lookup"><span data-stu-id="7e006-126">Use variables in message validation</span></span>

<span data-ttu-id="7e006-127">保存された変数を、メッセージ検証タブの文字列の一部として使用することもできます。以下は、`Customer account {{variable name}} already exists.` というメッセージを検証する例です。これは、テストの実行中に情報ログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e006-127">You can also use a saved variable as part of a string in the Message Validation tab. Here is an example that validates that the message `Customer account {{variable name}} already exists.` It appears in the infolog during test execution.</span></span> <span data-ttu-id="7e006-128">`{{variable name}}` は、記録中にコピーされる変数です。</span><span class="sxs-lookup"><span data-stu-id="7e006-128">`{{variable name}}` is a variable that is copied during the recording.</span></span>

<span data-ttu-id="7e006-129">保存済 (コピー済) 変数は、同じテスト ケース内で、または同じテスト スイート内の複数のテスト ケース間で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e006-129">Saved (Copied) variables can be used within the same test case or across more than one test case in the same test suite.</span></span>

![変数を含むメッセージ](media/rsat-message-with-variable.png)

