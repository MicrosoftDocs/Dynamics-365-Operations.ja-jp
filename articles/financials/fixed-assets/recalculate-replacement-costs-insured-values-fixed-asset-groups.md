---
title: 固定資産グループの交換費用と保証金額の再計算
description: この記事は、固定資産の交換費用と保証金額を更新するプロセスを説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0756287406ad12237632ffbd455dbc6ba15d9915
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563368"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a><span data-ttu-id="4bec1-103">固定資産グループの交換費用と保証金額の再計算</span><span class="sxs-lookup"><span data-stu-id="4bec1-103">Recalculate replacement costs and insured values for fixed asset groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bec1-104">この記事は、固定資産の交換費用と保証金額を更新するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-104">This article explains the process to update the replacement costs and insured values for fixed assets.</span></span>

<span data-ttu-id="4bec1-105">定期的に、特定の固定資産を交換または保証する費用が変化したことが通知される場合があります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-105">Periodically, you might be notified that the cost to replace or insure specific fixed assets has changed.</span></span> <span data-ttu-id="4bec1-106">たとえば、前年が 3 パーセントのインフレであったため、すべての固定資産の交換費用を 3 パーセントだけ増やす必要があるという連絡を、マネージャから受け取る場合などです。</span><span class="sxs-lookup"><span data-stu-id="4bec1-106">For example, your manager might inform you that inflation was 3 percent last year, so you need to increase the replacement cost of all fixed assets by 3 percent.</span></span> 

<span data-ttu-id="4bec1-107">**固定資産** ページで固定資産の交換費用と保証金額を個別に編集することもできますが、**交換費用と保証金額の更新** ページを使用すると、資産のグループ全体でのこれらの値を一度に更新できます。</span><span class="sxs-lookup"><span data-stu-id="4bec1-107">Although you can edit the replacement cost and insured value for individual fixed assets in the **Fixed assets** page, you can use the **Update replacement costs and insured values** page to update these values for a group of assets at one time.</span></span> <span data-ttu-id="4bec1-108">ここでは、固定資産グループの値またはグループ内の特定資産の値を更新する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-108">This information describes how to update values for fixed asset groups or for specific assets in the groups.</span></span>

## <a name="how-values-are-updated"></a><span data-ttu-id="4bec1-109">値の更新方法</span><span class="sxs-lookup"><span data-stu-id="4bec1-109">How values are updated</span></span>
<span data-ttu-id="4bec1-110">固定資産グループの交換費用および保証金額を再計算するには、最初に既存の交換費用および保証金額を変更する率を指定した後、定期更新を実行して、実際に値を再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-110">To recalculate replacement costs and insured values for fixed asset groups, you must first specify the percentage by which to change the existing replacement costs and insured values, and then perform the periodic update to actually recalculate the values.</span></span> <span data-ttu-id="4bec1-111">変更率は、**固定資産グループ** ページの **交換費用係数** および **保証金額係数** フィールドで指定します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-111">You specify the percentage in the **Replacement cost factor** and **Insured value factor** fields in the **Fixed asset groups** page.</span></span> <span data-ttu-id="4bec1-112">これらの係数は固定資産グループに対して指定しますが、**交換費用と保証金額の更新** ページを使用すると、グループ内の特定の固定資産についてのみ、交換費用と保証金額の再計算を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4bec1-112">Although you specify these factors for the fixed asset group, when you use the **Update replacement costs and insured values** page, you can select to recalculate the replacement cost and insured value for only specific fixed assets in a group.</span></span> 

<span data-ttu-id="4bec1-113">**交換費用と保証金額の更新** ページを使用して資産の交換費用および保証金額を再計算する場合は、次の式が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4bec1-113">When you use the **Update replacement costs and insured values** page to recalculate the replacement cost and insured value for the assets, the following formulas are used:</span></span>

-   <span data-ttu-id="4bec1-114">\[(資産グループの交換費用係数 / 100) + 1\] \* 資産の既存の交換費用</span><span class="sxs-lookup"><span data-stu-id="4bec1-114">\[(Asset group's replacement cost factor / 100) + 1\] \* Asset's existing replacement cost</span></span>
-   <span data-ttu-id="4bec1-115">\[(資産グループの保証金額係数 / 100) + 1\] \* 資産の既存の保証金額</span><span class="sxs-lookup"><span data-stu-id="4bec1-115">\[(Asset group's insured value factor / 100) + 1\] \* Asset's existing insured value</span></span>

> [!NOTE] 
> <span data-ttu-id="4bec1-116">**交換費用と保証金額の更新** ページを使用するときは、交換費用と保証金額の両方が、選択した資産について更新されます。どちらか一方の値のみを更新するようには指定できません。</span><span class="sxs-lookup"><span data-stu-id="4bec1-116">When you use the **Update replacement costs and insured values** page, both the replacement cost and insured value are updated for the selected assets; you cannot specify that only one value be updated.</span></span> <span data-ttu-id="4bec1-117">一方の値を同じままにして他方の値を更新するには、**固定資産グループ** ページで係数として 0 (ゼロ) を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-117">To leave one value the same and update the other value, enter 0 (zero) as the factor in the **Fixed asset groups** page.</span></span> <span data-ttu-id="4bec1-118">係数にゼロを指定するか空白のままにすると、更新で計算が省略されます。</span><span class="sxs-lookup"><span data-stu-id="4bec1-118">A zero or blank factor causes the calculation to be skipped in the update.</span></span> <span data-ttu-id="4bec1-119">固定資産の簿価額および正味簿価額は、定期更新では更新されません。</span><span class="sxs-lookup"><span data-stu-id="4bec1-119">The book value and net book value of fixed assets are not affected by the periodic update.</span></span> 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a><span data-ttu-id="4bec1-120">日付を使用して、更新する品目を選択する方法</span><span class="sxs-lookup"><span data-stu-id="4bec1-120">How to use a date to select which items to update</span></span>
<span data-ttu-id="4bec1-121">既定では、選択された資産のうち、当日に更新されていないものが更新プロセスで更新されますが、その資産が前日までに更新されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-121">By default, the update process updates the selected assets that have not been updated on the current day, but that might have been updated on previous days.</span></span> <span data-ttu-id="4bec1-122">たとえば、&lt; 現在の日付は「今日の日付より前」になります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-122">For example, &lt; current date means “before today.”</span></span> <span data-ttu-id="4bec1-123">**選択** ボタンをクリックすると、**交換費用と保証金額の更新** ページで日付を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="4bec1-123">You can change the date in the **Update replacement costs and insured values** page by clicking the **Select** button.</span></span> <span data-ttu-id="4bec1-124">指定した日付条件は、その資産が最後に定期更新された日付と比較されます (**固定資産** ページの **値/原価の最後の定期更新** フィールド)。</span><span class="sxs-lookup"><span data-stu-id="4bec1-124">The date criteria that you specify is compared to the date of the last periodic update for the asset (the **Last periodic value/cost update** field in the **Fixed assets** page).</span></span> <span data-ttu-id="4bec1-125">固定資産の交換費用または保証金額が正常に更新されるたびに、**値/原価の最後の定期更新** フィールドが当日の日付で自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="4bec1-125">Each time that you successfully update the replacement cost or insured value for a fixed asset, the **Last periodic value/cost update** field is automatically updated with the current date.</span></span> 

<span data-ttu-id="4bec1-126">例</span><span class="sxs-lookup"><span data-stu-id="4bec1-126">Example</span></span> 

<span data-ttu-id="4bec1-127">昨日、車両、オフィス家具、および建物の各グループの交換費用を 5% 更新しており、これらの資産については正しく更新されているものと考えられます。</span><span class="sxs-lookup"><span data-stu-id="4bec1-127">You updated the replacement cost of the Vehicles, Office Furniture, and Buildings groups by 5 percent yesterday, and you now consider these assets to be accurately updated.</span></span> <span data-ttu-id="4bec1-128">今日、他のすべての固定資産を更新するときにこれらの資産を除外するには、**値/原価の最後の定期更新** フィールドに、昨日より前の日付 (&lt; 昨日の日付) を入力します。このようにすると、**車両**、**オフィス家具**、**建物** のグループの最後の更新は、入力した日付条件の範囲外で行われたことになります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-128">To exclude these assets when you update all other fixed assets today, you enter a date in the **Last periodic value/cost update** field that is before yesterday (&lt; yesterday's date), because the last update for the **Vehicles**, **Office Furniture**, and **Buildings** groups occurred outside the date criteria you entered.</span></span>

## <a name="cumulative-effect-of-each-update"></a><span data-ttu-id="4bec1-129">各更新の累積効果</span><span class="sxs-lookup"><span data-stu-id="4bec1-129">Cumulative effect of each update</span></span>
<span data-ttu-id="4bec1-130">各更新には累積効果があります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-130">Each update has a cumulative effect.</span></span> <span data-ttu-id="4bec1-131">したがって、更新は慎重に計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-131">Therefore, you should plan your updates carefully.</span></span> <span data-ttu-id="4bec1-132">たとえば、火曜日にすべての資産を 3% 上げ、金曜日にオフィス家具を 4% 上げた場合は、オフィス家具は合計 7.12% 上昇することになります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-132">For example, if you increase all assets by 3 percent on Tuesday and then increase office furniture by 4 percent on Friday, office furniture will increase by a total of 7.12 percent.</span></span>

## <a name="scenario"></a><span data-ttu-id="4bec1-133">シナリオ</span><span class="sxs-lookup"><span data-stu-id="4bec1-133">Scenario</span></span>
<span data-ttu-id="4bec1-134">マネージャから、固定資産に対する次のような変更を指示されました。</span><span class="sxs-lookup"><span data-stu-id="4bec1-134">Your manager notifies you of the following changes to fixed assets:</span></span>
-   <span data-ttu-id="4bec1-135">コンピュータを除くすべての固定資産の交換費用を、3.25% 高くする。</span><span class="sxs-lookup"><span data-stu-id="4bec1-135">Increase the replacement cost of all fixed assets, except computers, by 3.25 percent.</span></span>
-   <span data-ttu-id="4bec1-136">すべてのオフィス家具の交換費用を、さらに 1% 高くする。</span><span class="sxs-lookup"><span data-stu-id="4bec1-136">Increase the replacement cost of all office furniture by an additional 1 percent.</span></span>
-   <span data-ttu-id="4bec1-137">すべてのコンピュータの交換費用および保証金額を、10% 低くする。</span><span class="sxs-lookup"><span data-stu-id="4bec1-137">Decrease the replacement cost and insured value of all computers by 10 percent.</span></span>

<span data-ttu-id="4bec1-138">次の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="4bec1-138">You make the following changes:</span></span>
1.  <span data-ttu-id="4bec1-139">**オフィス家具** グループと **コンピューター** グループを除くすべての固定資産グループについて、**固定資産グループ** ページで、**交換費用係数** フィールドに 3.25、そして **保証金額係数** フィールドに 0 と入力します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-139">In the **Fixed asset groups** page, for all fixed asset groups except the **Office Furniture** group and **Computers** group, you type 3.25 in the **Replacement cost factor** field and 0 in the **Insured value factor** field.</span></span>
2.  <span data-ttu-id="4bec1-140">**オフィス家具** グループについては、**交換費用係数** フィールドに 4.25、そして **保証金額係数** フィールドに 0 と入力します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-140">For the **Office Furniture** group, you type 4.25 in the **Replacement cost factor** field and 0 in the **Insured value factor** field.</span></span>
3.  <span data-ttu-id="4bec1-141">**コンピューター** グループについては、**交換費用係数** フィールドに -10、**保証金額係数** フィールドに -10 と入力します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-141">For the **Computers** group, you type -10 in the **Replacement cost factor** field and -10 in the **Insured value factor** field.</span></span>
4.  <span data-ttu-id="4bec1-142">**交換費用と保証金額の更新** ページで、**OK** をクリックし、すべての固定資産の再計算を実行します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-142">In the **Update replacement costs and insured values** page, you click **OK** to perform the recalculation for all fixed assets.</span></span>

<span data-ttu-id="4bec1-143">翌日、マネージャーから、コンピュータは 10% ではなく、8% 下げるように指示されたため、交換費用と保証金額を修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-143">The next day, your manager informs you that computers decreased 8 percent instead of 10 percent, so that you have to correct the replacement costs and insured values.</span></span> <span data-ttu-id="4bec1-144">誤りを修正するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="4bec1-144">To fix the error, you can use either of two methods:</span></span>
-   <span data-ttu-id="4bec1-145">**コンピューター** 固定資産グループの各固定資産ごとに、**固定資産** ページの **保証金額** フィールドと **交換費用** フィールドを手作業で変更します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-145">Manually change the **Insured value** and **Replacement cost** fields in the **Fixed assets** page for each fixed asset in the **Computers** fixed asset group.</span></span> <span data-ttu-id="4bec1-146">元の金額を 8% だけ減らしたかのように計算して、値を手作業で入力します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-146">Calculate and manually enter the values as if you had decreased the original amount by 8 percent.</span></span> <span data-ttu-id="4bec1-147">この方法を使用することで、**交換費用と保証金額の更新** ページは使用しません。</span><span class="sxs-lookup"><span data-stu-id="4bec1-147">By using this method, you do not use the **Update replacement costs and insured values** page.</span></span>
-   <span data-ttu-id="4bec1-148">**固定資産グループ** ページの **交換費用係数** フィールドと **保証金額係数** フィールドに、**コンピューター** グループの交換費用と保証金額の係数を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-148">Enter replacement cost and insured value factors for the **Computers** group in the **Replacement cost factor** and **Insured value factor** fields in the **Fixed asset groups** page.</span></span> <span data-ttu-id="4bec1-149">これは、資産を元の値 (10% 下げる前) にリセットしてから、元の値を 8% 下げる方法です。</span><span class="sxs-lookup"><span data-stu-id="4bec1-149">This will both reset the assets back to their original value (before the 10 percent decrease) and apply the 8 percent decrease to the original value.</span></span> <span data-ttu-id="4bec1-150">その後、**交換費用と保証金額の更新** ページを使用し、入力した係数に応じて値を再計算します。</span><span class="sxs-lookup"><span data-stu-id="4bec1-150">Then use the **Update replacement costs and insured values** page to recalculate the values, depending on the factors that you entered.</span></span>

> [!NOTE]  
> <span data-ttu-id="4bec1-151">正の係数 10 (または –10 と –8 の差の係数 2) を入力して、-10 という係数を元に戻すことはできません。これでは、正しい金額は算出されません。</span><span class="sxs-lookup"><span data-stu-id="4bec1-151">You cannot reverse the -10 factor by entering a factor of positive 10 (or a factor of 2, the difference between -10 and -8), because the amounts will not be calculated as you intend.</span></span> 





