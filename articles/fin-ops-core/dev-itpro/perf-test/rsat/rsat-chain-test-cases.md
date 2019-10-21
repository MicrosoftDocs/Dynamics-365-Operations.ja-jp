---
title: テスト ケースの連鎖
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
ms.openlocfilehash: 2891866ea62ee588d4f9844f52f4b24651e25729
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183091"
---
# <a name="chain-test-cases"></a><span data-ttu-id="ce91a-103">テスト ケースの連鎖</span><span class="sxs-lookup"><span data-stu-id="ce91a-103">Chain test cases</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce91a-104">Regression Suite Automation Tool の主要な機能の１つとして、テスト ケースの連鎖、つまり、テストが他のテストに値を渡す機能、があります。</span><span class="sxs-lookup"><span data-stu-id="ce91a-104">One of the key features of the Regression Suite Automation Tool is the chaining of test cases, that is, the ability of a test to pass values to other tests.</span></span> <span data-ttu-id="ce91a-105">テスト ケースは、 Azure DevOps テスト計画内で定義されている順序に従って実行され、テスト ツール自体で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="ce91a-105">Test cases are executed according to their defined order in the Azure DevOps test plan, which can also be updated in the test tool itself.</span></span> <span data-ttu-id="ce91a-106">１つのテスト ケースから別のテスト ケースに変数を渡す場合は、テストを正しく順序付けることが重要です。</span><span class="sxs-lookup"><span data-stu-id="ce91a-106">It is important to correctly order the tests if you want to pass variables from one test case to the other.</span></span>

<span data-ttu-id="ce91a-107">タスク レコーダーでテストを記録しながら変数の値を保存するには、次に示すように、フィールドを右クリックして **タスク レコーダー > コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce91a-107">To save the value of a variable while recording the test in Task Recorder, right-click the field and select **Task recorder > Copy**, as shown below.</span></span> <span data-ttu-id="ce91a-108">これにより、変数が記録ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="ce91a-108">This will save the variable in the recording file.</span></span> <span data-ttu-id="ce91a-109">この変数は、後続のテストで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce91a-109">This variable can be used in subsequent tests.</span></span> 
 
![タスク レコーダーのメニュー項目のコピー](media/task-recorder-copy.png)

<span data-ttu-id="ce91a-111">Excel パラメーター ファイルでは、これらの保存された値は、 **一般** タブの **保存された変数** テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce91a-111">In the Excel parameters file, these saved values appear in the **Saved variables** table on the **General** Tab.</span></span>
 
![Excel に保存された変数](media/saved-variables.png)
 
<span data-ttu-id="ce91a-113">テスト再生時にこれらの変数を再利用するには、次に示すように、変数名をコピーして、別のテスト (または同じテスト) のデータ ファイルでパラメーター値の代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="ce91a-113">To reuse these variables during test play back, copy the variable name and use it in place of a parameter value in the data file of another test (or the same test), as shown below.</span></span> 
 
![Excel での変数の再利用](media/reuse-variables.png)
 
<span data-ttu-id="ce91a-115">変数は、定義されている同じテストケースで使用できます。また、同じテストの実行中にテスト間で渡すこともできます。</span><span class="sxs-lookup"><span data-stu-id="ce91a-115">Variables can be used in the same test case where they are defined and can also be passed between tests during the same test run.</span></span>

## <a name="support-for-formulas-of-saved-variables"></a><span data-ttu-id="ce91a-116">保存された変数の式のサポート</span><span class="sxs-lookup"><span data-stu-id="ce91a-116">Support for formulas of saved variables</span></span>

<span data-ttu-id="ce91a-117">保存された (コピーされた) 変数を含むフォーミュラを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ce91a-117">You can create formulas that contain saved (copied) variables.</span></span> <span data-ttu-id="ce91a-118">Regression Suite Automation Tool の古いバージョンのを使用している場合、この機能を利用するためには新しいExcel パラメーター ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce91a-118">If you have been using an older version of the Regression Suite Automation Tool, you will need to regenerate new Excel parameter files to take advantage of this functionality.</span></span> <span data-ttu-id="ce91a-119">サポートされ演算子は、 **+**、 **-**、 **/** および **\*** です。</span><span class="sxs-lookup"><span data-stu-id="ce91a-119">Supported operators are **+**, **-**, **/** and **\***.</span></span> <span data-ttu-id="ce91a-120">Regression Suite Automation Tool 式で使用できるのは、数値変数のみです。</span><span class="sxs-lookup"><span data-stu-id="ce91a-120">Only numerical variables can be used in the Regression Suite Automation Tool formulas.</span></span> <span data-ttu-id="ce91a-121">文字列または日付はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ce91a-121">Strings or dates are not supported.</span></span> <span data-ttu-id="ce91a-122">変数名は常に二重の中かっこ **{{varname}}** で指定します。</span><span class="sxs-lookup"><span data-stu-id="ce91a-122">Always specify variable names within double braces **{{varname}}**.</span></span> <span data-ttu-id="ce91a-123">たとえば、 **{{var1}} + {{var2}}**。</span><span class="sxs-lookup"><span data-stu-id="ce91a-123">For example, **{{var1}} + {{var2}}**.</span></span>

<span data-ttu-id="ce91a-124">次の図では、2つの異なる変数が式で使用されています。</span><span class="sxs-lookup"><span data-stu-id="ce91a-124">In the image below, two different variables are used in a formula.</span></span>
 
![Excelでの式の作成](media/formulas.png)
 
