---
title: 原価および日付の管理
description: このトピックでは、資産管理の価および日付の管理について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 74e42207e5f3418e6e80b46a1d2634fbd8065126
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652221"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="e0cae-103">原価および日付の管理</span><span class="sxs-lookup"><span data-stu-id="e0cae-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e0cae-104">資産管理では、原価を計算して、資産、機能的な場所、およびワーク オーダーの予算原価と比較した実際の原価の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="e0cae-105">実際原価は、転記されたトランザクションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="e0cae-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="e0cae-106">またスケジュールされた開始日と終了日を、作業指示書の実際の開始日と終了日と比較する場合に、日付計算を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="e0cae-107">資産、機能的な場所、および作業指示書の原価管理</span><span class="sxs-lookup"><span data-stu-id="e0cae-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="e0cae-108">資産、機能的な場所、およびワーク オーダーに対して行われる計算は、ほぼ同一です。</span><span class="sxs-lookup"><span data-stu-id="e0cae-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="e0cae-109">唯一の違いは、資産と機能的な場所に対して、下位資産とサブ場所を計算に含めることもできるという点です。</span><span class="sxs-lookup"><span data-stu-id="e0cae-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="e0cae-110">日付は、登録が記録されたトランザクション日付です。</span><span class="sxs-lookup"><span data-stu-id="e0cae-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="e0cae-111">**資産管理** > **照会** > **資産** > **資産原価管理**または**機能的な場所の原価管理**の順に、または**資産管理** > **照会** > **作業指示書** > **作業指示書の原価管理**の順にクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="e0cae-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="e0cae-112">**資産原価管理** / **機能的な場所の原価管理** / **作業指示書の原価管理**ダイアログで、計算する時間範囲を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="e0cae-113">必要に応じて、計算に含める財務分析コード セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="e0cae-114">原価がゼロの結果を表示しない場合は、**ゼロをスキップ** トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="e0cae-115">**レベル** フィールドを使用すると、機能的な場所に関する原価管理明細行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="e0cae-116">たとえば、フィールドに数値 "1" を挿入し、複数レベルの機能的な場所の階層がある場合、機能的な場所に対するすべての原価管理明細行が最上位レベルに表示されます。そのため、明細行の時間が下位レベルにある機能的な場所から追加されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="e0cae-117">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルのすべての原価管理明細行を示す詳細結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="e0cae-118">計算に列を含める場合は、**オープン状態の確定済み費用の表示**トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="e0cae-119">**下位資産を含める**トグルボタンで「はい」を選択し、下位資産に関連する原価を別の明細行として表示します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="e0cae-120">検索を制限する場合は、**対象に含めるレコード** クイック タブで特定の資産、機能的な場所、およびワーク オーダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="e0cae-121">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="e0cae-122">次の図は、**資産原価管理**ダイアログの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![資産原価管理ダイアログ ボックス](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="e0cae-124">**資産原価管理**ページの、**グループ化**ボタンをクリックすると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="e0cae-125">選択した**グループ化**ボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="e0cae-126">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="e0cae-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="e0cae-127">例</span><span class="sxs-lookup"><span data-stu-id="e0cae-127">Example</span></span>

<span data-ttu-id="e0cae-128">次のスクリーンショットは、**資産原価管理**の計算結果の例を示します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="e0cae-129">**元の予算**フィールドでは、作業指示書予測からの予算原価が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="e0cae-130">**確定済費用**フォールドでは、法人が支払を確定した経費の合計金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="e0cae-131">**オープン状態の確定済み費用**フィールドでは、注文または入庫したもののまだ支払われていない品目、時間、およびサービスに対する支払の確定が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="e0cae-132">すべての消費登録が転記された後、**実際原価**フィールドでは関連する原価が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![資産原価管理での計算結果の例](media/02-controlling-and-reporting.png)

<span data-ttu-id="e0cae-134">原価計算を行う別の方法は、**すべての資産**または**有効な資産**で複数の資産を選択することです。</span><span class="sxs-lookup"><span data-stu-id="e0cae-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="e0cae-135">その後、**一般**タブで**原価管理**ボタンをクリックします。**資産原価管理**ダイアログでは、選択された資産が**対象に含めるレコード**クイック タブの**資産**フィールドに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="e0cae-136">**OK** をクリックすると、選択された資産に対する原価計算が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="e0cae-137">同じ手順を、**すべての機能的な場所**または**有効な機能的な場所**の機能的な場所、および**すべてのワーク オーダー**または**有効なワーク オーダー**のワーク オーダーに対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="e0cae-138">作業指示書日付管理</span><span class="sxs-lookup"><span data-stu-id="e0cae-138">Work order date control</span></span>

<span data-ttu-id="e0cae-139">このページを使用して、予定された開始日および終了日を、作業指示書にある実際の開始日および終了日と比較した概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="e0cae-140">**資産管理** > **照会** > **作業指示書** > **作業指示書の日付管理**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0cae-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="e0cae-141">**計算** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0cae-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="e0cae-142">**機能的な場所**フィールドで、機能的な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="e0cae-143">**開始日**および**終了日**フィールドで、計算を実行する範囲を挿入します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="e0cae-144">範囲内の開始予定日のすべての作業指示書が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="e0cae-145">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0cae-145">Click **OK**.</span></span>

6. <span data-ttu-id="e0cae-146">**グループ化**ボタンをクリックすると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="e0cae-147">選択した**グループ化**ボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="e0cae-148">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="e0cae-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="e0cae-149">例</span><span class="sxs-lookup"><span data-stu-id="e0cae-149">Example</span></span>

<span data-ttu-id="e0cae-150">次のスクリーンショットは、**作業指示書の日付管理**の計算結果の例を示します。</span><span class="sxs-lookup"><span data-stu-id="e0cae-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="e0cae-151">**平均開始遅延**フィールドには、実際の開始日と比較した作業指示書での開始予定日との日数の差が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="e0cae-152">たとえば、実際の開始日が開始予定日の 2 日前だった場合、このフィールドに "-2" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="e0cae-153">**平均終了遅延**フィールドには、実際の終了日と比較した作業指示書での終了予定日との日数の差が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="e0cae-154">たとえば、実際の終了日が終了予定日の 3 日後だった場合、このフィールドに "3" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="e0cae-155">**発生回数**フィールドには、作業指示書での開始予定日と実際の開始日、および終了予定日と実際の終了日に関連して誤差が発生した回数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cae-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![作業指示書日付管理での計算結果の例](media/03-controlling-and-reporting.png)


