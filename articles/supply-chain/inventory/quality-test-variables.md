---
title: 品質管理テスト変数
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の定性試験に使用できるテスト変数を作成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021711"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="ff0f3-103">品質管理テスト変数</span><span class="sxs-lookup"><span data-stu-id="ff0f3-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff0f3-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の定性試験に使用できるテスト変数を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ff0f3-105">**テスト** ページで定義されているすべての定性試験について、テスト変数とその可能な結果 (結果) を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="ff0f3-106">(定性試験の場合、**テスト** ページの **タイプ** フィールドは、*オプション* に設定されます。)</span><span class="sxs-lookup"><span data-stu-id="ff0f3-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="ff0f3-107">**テスト変数** ページを使用して、定性試験に関連付けられているテスト変数の可能な結果を設定、編集、および表示します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="ff0f3-108">それぞれの結果について、*合格* または *不合格* のいずれかの結果ステータスを割り当て、その結果がテスト結果として選択された場合にテストが合格か不合格かを示します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="ff0f3-109">**テスト グループ** ページを使用して、テスト変数と既定の結果を個々の定性試験に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="ff0f3-110">すべてのテスト変数について、少なくとも 2 つの結果を定義することをお勧めします。1 つは結果ステータスが *合格* で、もう 1 つは結果ステータスが *不合格* です。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="ff0f3-111">定義できる変数または結果の合計数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="ff0f3-112">また、複数のテストで同じテスト変数を使用して結果を記録できます。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="ff0f3-113">テスト変数の例</span><span class="sxs-lookup"><span data-stu-id="ff0f3-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="ff0f3-114">例 1</span><span class="sxs-lookup"><span data-stu-id="ff0f3-114">Example 1</span></span>

<span data-ttu-id="ff0f3-115">製造会社で、製造材料に対する 2 つのテストを実行しています。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="ff0f3-116">1 つのテストでは、pH レベルが色のストリップに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="ff0f3-117">許容できる pH レベルは明るい色で、許容できない pH レベルは暗い色です。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="ff0f3-118">別のテストでは、複数の目視検査が実行され、品質作業員はその判断を使用して、品目が目視検査に合格か不合格かを決定します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="ff0f3-119">例 2</span><span class="sxs-lookup"><span data-stu-id="ff0f3-119">Example 2</span></span>

<span data-ttu-id="ff0f3-120">クッキーを製造しているある製造会社では、完成した製品の検査テストを採用しています。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="ff0f3-121">この検査テストには、複数の変数があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-121">This inspection test has several variables.</span></span> <span data-ttu-id="ff0f3-122">1 つの変数は味で、そのために考えられる結果は、良および不良です。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="ff0f3-123">2 つ目の変数は色で、そのために考えられる結果は、濃すぎる、薄すぎる、および適正です。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="ff0f3-124">テスト変数の作成</span><span class="sxs-lookup"><span data-stu-id="ff0f3-124">Create a test variable</span></span>

<span data-ttu-id="ff0f3-125">次の手順に従って、テスト変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="ff0f3-126">**在庫管理 \> 設定 \> 品質管理 \> テスト変数** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="ff0f3-127">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ff0f3-128">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ff0f3-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ff0f3-129">**変数** – 変数の固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="ff0f3-130">**説明** – 変数の詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="ff0f3-131">新しい行がまだ選択されている間に、アクション ウィンドウで **結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="ff0f3-132">アクション ウィンドウの **テスト変数の結果** ページで、**新規** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ff0f3-133">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ff0f3-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ff0f3-134">**結果** – 結果の固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="ff0f3-135">**説明** – 結果の詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="ff0f3-136">**結果ステータス** – *合格* または *不合格* のいずれかを選択して、結果がテスト結果として選択された場合に、テストが合格か不合格かを示します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="ff0f3-137">追加の結果ごとに前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="ff0f3-138">少なくとも 1 つの結果の結果ステータスが *合格* であり、少なくとも 1 つの結果の結果ステータスが *不合格* であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="ff0f3-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ff0f3-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff0f3-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ff0f3-140">Additional resources</span></span>

- [<span data-ttu-id="ff0f3-141">品質管理テスト機器</span><span class="sxs-lookup"><span data-stu-id="ff0f3-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="ff0f3-142">品質管理テスト</span><span class="sxs-lookup"><span data-stu-id="ff0f3-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="ff0f3-143">品質管理テスト グループ</span><span class="sxs-lookup"><span data-stu-id="ff0f3-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
