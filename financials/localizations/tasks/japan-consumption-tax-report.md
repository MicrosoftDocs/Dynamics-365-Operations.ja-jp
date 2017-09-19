--- 
title: "消費税レポートの生成 (日本)"
description: "この手順では、日本の消費税申告の生成について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3ae9b58469eaed4e01df520c51c165b22e95083a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="generate-consumption-tax-report-japan"></a><span data-ttu-id="14bb7-103">消費税レポートの生成 (日本)</span><span class="sxs-lookup"><span data-stu-id="14bb7-103">Generate consumption tax report (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14bb7-104">この手順では、日本の消費税申告の生成について説明します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-104">This procedure walks you through generating the Japan consumption tax report.</span></span>



<span data-ttu-id="14bb7-105">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="14bb7-105">This procedure was created using the demo data company JPMF.</span></span>





1. <span data-ttu-id="14bb7-106">[税] > [申告] > [売上税] > [消費税申告書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-106">Go to Tax > Declarations > Sales tax > Japanese sales tax report.</span></span>
2. <span data-ttu-id="14bb7-107">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-107">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="14bb7-108">例: 2012/1/1</span><span class="sxs-lookup"><span data-stu-id="14bb7-108">For example: 2012/1/1</span></span>  
3. <span data-ttu-id="14bb7-109">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-109">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="14bb7-110">例: 2012/12/31</span><span class="sxs-lookup"><span data-stu-id="14bb7-110">For example: 2012/12/31</span></span>  
4. <span data-ttu-id="14bb7-111">[決済期間] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-111">In the Settlement period field, type a value.</span></span>
5. <span data-ttu-id="14bb7-112">[申告のタイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-112">In the Declaration type field, select an option.</span></span>
6. <span data-ttu-id="14bb7-113">[計算方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-113">In the Calculation method field, select an option.</span></span>
7. <span data-ttu-id="14bb7-114">[修正] フィールドで、 [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-114">Select Yes in the Amendment field.</span></span>
    * <span data-ttu-id="14bb7-115">以前にレポートを生成し、もう一度生成する場合は、既存のレコードの修正を更新するように選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14bb7-115">If you have already generated the report previously and you are generating it again, you must choose to update the existing record on the amendment.</span></span>  
8. <span data-ttu-id="14bb7-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-116">Click OK.</span></span>
9. <span data-ttu-id="14bb7-117">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-117">Click Edit.</span></span>
10. <span data-ttu-id="14bb7-118">[項目 6] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-118">In the Item 6 field, enter a number.</span></span>
    * <span data-ttu-id="14bb7-119">データはトランザクションから取得され、集計されます。</span><span class="sxs-lookup"><span data-stu-id="14bb7-119">The data is retrieved and summarized from the transactions.</span></span> <span data-ttu-id="14bb7-120">調整のために編集可能なフィールドを更新できます。</span><span class="sxs-lookup"><span data-stu-id="14bb7-120">You can update the editable fields for adjustment purposes.</span></span>  
11. <span data-ttu-id="14bb7-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-121">Click Save.</span></span>
12. <span data-ttu-id="14bb7-122">[金額の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-122">Click Update amount.</span></span>
    * <span data-ttu-id="14bb7-123">これにより、金額を再計算します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-123">This recalculates the amounts.</span></span>  
13. <span data-ttu-id="14bb7-124">[確定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-124">Click Finalize.</span></span>
14. <span data-ttu-id="14bb7-125">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-125">Click Yes.</span></span>
15. <span data-ttu-id="14bb7-126">[消費税申告] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-126">Click Consumption tax report.</span></span>
16. <span data-ttu-id="14bb7-127">[税額の計算] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-127">Click the Tax calculation tab.</span></span>
17. <span data-ttu-id="14bb7-128">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-128">Click Edit.</span></span>
18. <span data-ttu-id="14bb7-129">[項目 10] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-129">In the Item 10 field, enter a number.</span></span>
19. <span data-ttu-id="14bb7-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-130">Click Save.</span></span>
20. <span data-ttu-id="14bb7-131">[金額の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-131">Click Update amount.</span></span>
21. <span data-ttu-id="14bb7-132">[追加情報] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-132">Click the Additional information tab.</span></span>
    * <span data-ttu-id="14bb7-133">[追加情報] タブでは、情報を、コンフィギュレーションされたとおりに印刷します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-133">In the Additional information tab, the information is printed as configured.</span></span>  
    * <span data-ttu-id="14bb7-134">例: [割賦基準の適用] スライダーを「はい」に変更して、最終レポート上に印刷します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-134">For example: you can change the Installment basis slider to be 'Yes' to print a yes on the final report.</span></span>  
22. <span data-ttu-id="14bb7-135">[確定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-135">Click Finalize.</span></span>
23. <span data-ttu-id="14bb7-136">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-136">Click Yes.</span></span>
24. <span data-ttu-id="14bb7-137">[アクション] ペインで [消費税申告] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14bb7-137">On the Action Pane, click Consumption tax report.</span></span>
    * <span data-ttu-id="14bb7-138">[レポートを印刷] をクリックして、最終レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="14bb7-138">Click Print reports to generate the final report.</span></span>  

