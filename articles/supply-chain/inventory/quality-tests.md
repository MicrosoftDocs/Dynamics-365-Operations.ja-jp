---
title: 品質管理テスト
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示に使用できるテストを作成する方法について説明します。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956728"
---
# <a name="quality-management-tests"></a><span data-ttu-id="67a94-103">品質管理テスト</span><span class="sxs-lookup"><span data-stu-id="67a94-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67a94-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示に使用できるテストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="67a94-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="67a94-105">**テスト** ページを使用して、製品が品質仕様を満たすかどうかを決定する個別のテストを定義して表示できます。</span><span class="sxs-lookup"><span data-stu-id="67a94-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="67a94-106">テスト グループに 1 つ以上の個別のテストを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="67a94-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="67a94-107">この場合、許容測定値などのテスト固有の情報も指定します。</span><span class="sxs-lookup"><span data-stu-id="67a94-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="67a94-108">測定値は、定量試験に使用されます。</span><span class="sxs-lookup"><span data-stu-id="67a94-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="67a94-109">定性試験では、テスト変数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="67a94-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="67a94-110">定量試験の場合は、**タイプ** フィールドは、*整数* または *分数* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="67a94-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="67a94-111">測定単位も指定されます。</span><span class="sxs-lookup"><span data-stu-id="67a94-111">A unit of measure is also specified.</span></span> <span data-ttu-id="67a94-112">品質仕様とテスト結果が数字で示されます。</span><span class="sxs-lookup"><span data-stu-id="67a94-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="67a94-113">定性試験では、**タイプ** フィールドは、*オプション* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="67a94-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="67a94-114">定性試験では、測定されるテスト変数と列挙されたオプションに関する追加情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="67a94-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="67a94-115">品質仕様とテスト結果が結果に応じて示されます。</span><span class="sxs-lookup"><span data-stu-id="67a94-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="67a94-116">必要に応じて、テスト機器にテストを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="67a94-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="67a94-117">ただし、品質指示のテストを作成して使用するために、テスト機器は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="67a94-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="67a94-118">詳細については、[品質管理テスト機器](quality-test-instruments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67a94-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="67a94-119">必要に応じて、テストの単位を指定して、テスト結果が記録される測定単位を示すこともできます。</span><span class="sxs-lookup"><span data-stu-id="67a94-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="67a94-120">たとえば、温度のテストには、華氏または摂氏のいずれかの単位が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="67a94-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="67a94-121">テストの例</span><span class="sxs-lookup"><span data-stu-id="67a94-121">Example of a test</span></span>

<span data-ttu-id="67a94-122">ある製造会社では、購入した材料に対して 2 種類のテストを行います。材料品質に関する定量試験と、梱包破損に関する定性試験です。</span><span class="sxs-lookup"><span data-stu-id="67a94-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="67a94-123">定性試験に関して、テスト変数 (たとえば、破損した梱包) とその結果を定義する追加情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="67a94-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="67a94-124">**テスト グループ** ページを使用して、これら 2 つのテストを 1 つのテスト グループに割り当て、テスト固有の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="67a94-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="67a94-125">2 つのテストの結果をレポートできるよう、テスト グループを品質指示に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="67a94-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="67a94-126">テストの作成</span><span class="sxs-lookup"><span data-stu-id="67a94-126">Create a test</span></span>

<span data-ttu-id="67a94-127">次の手順に従って、テストを作成します。</span><span class="sxs-lookup"><span data-stu-id="67a94-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="67a94-128">**在庫管理 \> 設定 \> 品質管理 \> テスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="67a94-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="67a94-129">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="67a94-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="67a94-130">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="67a94-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="67a94-131">**テスト** – テストの固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="67a94-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="67a94-132">**説明** – テストの詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="67a94-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="67a94-133">**タイプ** – テストで生成される結果のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="67a94-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="67a94-134">定量試験では、*分数* または *整数* を選択します。</span><span class="sxs-lookup"><span data-stu-id="67a94-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="67a94-135">定性試験では、*オプション* を選択します。</span><span class="sxs-lookup"><span data-stu-id="67a94-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="67a94-136">**テスト機器** – テストに使用する[テスト機器](quality-test-instruments.md) を選択します。</span><span class="sxs-lookup"><span data-stu-id="67a94-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="67a94-137">**単位** – **タイプ** フィールドで *分数* または *整数* を選択した場合 (テストが定量試験の場合)、テスト結果を記録する測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="67a94-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="67a94-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="67a94-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="67a94-139">テストを保存した後は、グリッドの **タイプ** フィールドを編集することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="67a94-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="67a94-140">テストについて記録されるテスト結果のタイプを変更する必要がある場合は、アクション ウィンドウで **品質テスト タイプの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="67a94-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="67a94-141">**品質テスト タイプの変更** ダイアログ ボックスで、**新しいタイプ** フィールドを目的のタイプに設定し、**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="67a94-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67a94-142">追加リソース</span><span class="sxs-lookup"><span data-stu-id="67a94-142">Additional resources</span></span>

- [<span data-ttu-id="67a94-143">品質管理テスト機器</span><span class="sxs-lookup"><span data-stu-id="67a94-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="67a94-144">品質管理テスト グループ</span><span class="sxs-lookup"><span data-stu-id="67a94-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="67a94-145">品質管理テスト変数</span><span class="sxs-lookup"><span data-stu-id="67a94-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="67a94-146">品質関連</span><span class="sxs-lookup"><span data-stu-id="67a94-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
