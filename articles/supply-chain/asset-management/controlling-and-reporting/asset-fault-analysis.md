---
title: 資産エラー分析
description: このトピックでは、資産管理の資産エラー分析について説明します。
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
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918444"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="3914c-103">資産エラー分析</span><span class="sxs-lookup"><span data-stu-id="3914c-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3914c-104">資産管理では、資産エラー登録を分析して、特定の期間中に登録されたエラーの合計数の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="3914c-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="3914c-105">エラー登録は、資産、資産タイプ、機能的な場所、エラーの現象、エラー タイプなどに焦点を当て、異なる観点から分析できます。</span><span class="sxs-lookup"><span data-stu-id="3914c-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="3914c-106">**資産管理** > **照会** > **資産エラー** > **資産エラー分析**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3914c-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="3914c-107">**資産エラー分析計算**ダイアログでは、**レベル** フィールドを使用して、機能的な場所に関する資産エラー明細行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3914c-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> <span data-ttu-id="3914c-108">たとえば、フィールドに数値 "1" を挿入し、複数レベルの機能的な場所の構造がある場合、機能的な場所に対するすべての資産エラー明細行が最上位レベルに表示されます。そのため、明細行の時間が下位レベルにある機能的な場所から追加されます。</span><span class="sxs-lookup"><span data-stu-id="3914c-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="3914c-109">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルでのすべての資産エラー明細行を示す詳細結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3914c-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="3914c-110">検索を制限する場合は、**対象に含めるレコード** クイック タブで特定の資産、エラー日付、エラー原因、およびエラー救済を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3914c-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="3914c-111">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="3914c-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="3914c-112">**資産エラー分析**タブで、**グループ化...** アクション ウィンドウ グループで 1 つまたは複数のボタンをクリックして、表示する詳細レベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="3914c-112">On the **Asset fault analysis** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see.</span></span> <span data-ttu-id="3914c-113">有効になっているボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="3914c-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="3914c-114">ボタンをクリックして有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="3914c-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="3914c-115">**計算更新**をクリックして、選択内容を画面に表示します。</span><span class="sxs-lookup"><span data-stu-id="3914c-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="3914c-116">**グループ化...** アクション ウィンドウ グループのボタンを有効または無効にするたびに、選択内容を変更した後に**計算更新**ボタンを忘れずにクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="3914c-116">Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update calculations** button after you changed the selections.</span></span> <span data-ttu-id="3914c-117">これは、エラーの確度を再計算するときに大量のデータが処理されるために必要です。</span><span class="sxs-lookup"><span data-stu-id="3914c-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

<span data-ttu-id="3914c-118">エラー登録を分析する多くの方法があります。</span><span class="sxs-lookup"><span data-stu-id="3914c-118">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="3914c-119">以下の例では、データの選択内容によって異なる情報がどのように提供されるかを示す 5 つのスクリーンショットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3914c-119">Below you see examples in five screenshots of how different data selections provide different pieces of information.</span></span> <span data-ttu-id="3914c-120">選択内容によって、資産のエラー登録を分析する際の洞察や詳細情報がどう異なるかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3914c-120">You will see how different selections provide more insight and detail when analyzing asset fault registrations.</span></span>

<span data-ttu-id="3914c-121">次のスクリーンショットでは、**現象**ボタンのみが選択されています。</span><span class="sxs-lookup"><span data-stu-id="3914c-121">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="3914c-122">エラー登録は、"空気漏れ"、"ヒューズが飛んだ"、および "機器が詰まった" という 3 つのエラー現象に関して行われました。</span><span class="sxs-lookup"><span data-stu-id="3914c-122">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="3914c-123">**確度 %** 列では、すべての割合が 100% に設定されています。</span><span class="sxs-lookup"><span data-stu-id="3914c-123">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="3914c-124">確度は、このエラー分析内のすべての**現象**登録に基づきます。</span><span class="sxs-lookup"><span data-stu-id="3914c-124">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![図 1](media/06-controlling-and-reporting.png)


<span data-ttu-id="3914c-126">次のスクリーンショットでは、選択した期間中のエラー登録の表示方法を示すため、**年**および**月**が追加されています。</span><span class="sxs-lookup"><span data-stu-id="3914c-126">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="3914c-127">エラー現象が、年/月単位の登録として表示されます。</span><span class="sxs-lookup"><span data-stu-id="3914c-127">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="3914c-128">**確度 %** 列では、各月のすべての割合を加算すると、合計 100% になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-128">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="3914c-129">確度は、このエラー分析内の**現象**登録に基づきます。</span><span class="sxs-lookup"><span data-stu-id="3914c-129">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="3914c-130">資産に多数の明細行があっても、1 つの明細行で大きな割合が目立っている場合、それはエラー現象の兆候であり、そのエラー現象に対する登録数を制限する方法を探すためのより詳細な調査が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-130">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![図 2](media/07-controlling-and-reporting.png)


- <span data-ttu-id="3914c-132">資産と資産タイプの組み合わせは、下の 3 つのスクリーンショットに表示される計算の基準として使用され、詳細レベルが上がります。</span><span class="sxs-lookup"><span data-stu-id="3914c-132">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  
- <span data-ttu-id="3914c-133">一般に、**日付別にグループ化**、**資産別にグループ化**、**機能的な場所別にグループ化**アクション ウィンドウ グループのボタン、および**エラー** ボタン (エラー ID) には、期間または資産関係が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3914c-133">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="3914c-134">**現象**、**領域**、**タイプ**、**原因**、**救済**ボタンは、資産エラー登録の分析および問題領域を特定するためエラー管理で使用される分類です。</span><span class="sxs-lookup"><span data-stu-id="3914c-134">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="3914c-135">下のスクリーンショットでは、エラー登録に関する詳細を提供するため、**資産**および**資産タイプ**が追加されました。</span><span class="sxs-lookup"><span data-stu-id="3914c-135">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="3914c-136">エラー現象が**資産** / **資産タイプ** / **現象**の組み合わせで分割されるようになります。</span><span class="sxs-lookup"><span data-stu-id="3914c-136">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="3914c-137">**確度 %** 列では、**資産** / **資産タイプ** / **現象**の組み合わせのすべての割合をそれぞれ加算すると、各々が 100% になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-137">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="3914c-138">確度は、このエラー分析内の**現象**登録に基づきます。</span><span class="sxs-lookup"><span data-stu-id="3914c-138">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="3914c-139">資産に多数の明細行があっても、1 つの明細行で大きな割合が目立っている場合、それはエラー現象の兆候であり、そのエラー現象に対する登録数を制限する方法を探すためのより詳細な調査が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-139">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![図 3](media/08-controlling-and-reporting.png)


<span data-ttu-id="3914c-141">下のスクリーンショットでは、エラー登録に関する詳細を提供するため、**資産**が**現象**、**資産**、および**資産タイプ**に追加されました。</span><span class="sxs-lookup"><span data-stu-id="3914c-141">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="3914c-142">**確度 %** 列では、資産で**資産** / **資産タイプ** / **現象**の組み合わせのすべての割合を加算すると、それぞれが 100% になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-142">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="3914c-143">確度は、このエラー分析内の**現象**および**領域**の組み合わせに基づきます。</span><span class="sxs-lookup"><span data-stu-id="3914c-143">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="3914c-144">資産に多数の明細行があっても、1 つの明細行で大きな割合が目立っている場合、それはエラー領域の兆候であり、そのエラー領域に対する登録数を制限する方法を探すためのより詳細な調査が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-144">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![図 4](media/09-controlling-and-reporting.png)


<span data-ttu-id="3914c-146">下のスクリーンショットでは**タイプ**が追加されており、この例での最も詳細な計算が示されています。</span><span class="sxs-lookup"><span data-stu-id="3914c-146">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="3914c-147">**確度 %** 列では、資産で**資産** / **資産タイプ** / **現象**の組み合わせのすべての割合を加算すると、それぞれが 100% になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="3914c-148">確度は、このエラー分析内の**現象**、**領域**、および**タイプ**の組み合わせに基づきます。</span><span class="sxs-lookup"><span data-stu-id="3914c-148">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="3914c-149">資産に多数の明細行があっても、1 つの明細行で大きな割合が目立っている場合、それはエラー タイプの兆候であり、そのエラー タイプに対する登録数を制限する方法を探すためのより詳細な調査が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3914c-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![図 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="3914c-151">作業指示書およびメンテナンス要求で作成されたすべてのエラー登録の概要については、**資産管理** > **照会** > **資産エラー** > **資産エラー**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3914c-151">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="3914c-152">**資産エラー** ページで、資産エラー登録を選択し、**関連する情報**ウィンドウを展開して、関連する作業指示書またはメンテナンス要求に関する情報を参照します。</span><span class="sxs-lookup"><span data-stu-id="3914c-152">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

