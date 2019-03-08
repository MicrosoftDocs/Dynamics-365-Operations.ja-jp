---
title: 日本消費税レポートの生成
description: この手順では、日本の消費税申告の生成について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsumptionTaxCalcTrans_JP, LedgerConsumptionTaxReportTrans_JP
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adf62667a12b6bbb64c8e8188c83f962e8b7a65b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371072"
---
# <a name="generate-japan-consumption-tax-report"></a><span data-ttu-id="05a4e-103">日本消費税レポートの生成</span><span class="sxs-lookup"><span data-stu-id="05a4e-103">Generate Japan consumption tax report</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05a4e-104">この手順では、日本の消費税申告の生成について説明します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-104">This procedure walks you through generating the Japan consumption tax report.</span></span> <span data-ttu-id="05a4e-105">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="05a4e-105">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="05a4e-106">[税] > [申告] > [売上税] > [消費税申告書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-106">Go to Tax > Declarations > Sales tax > Japanese sales tax report.</span></span>
2. <span data-ttu-id="05a4e-107">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-107">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="05a4e-108">例: 2012/1/1</span><span class="sxs-lookup"><span data-stu-id="05a4e-108">For example: 2012/1/1</span></span>  
3. <span data-ttu-id="05a4e-109">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-109">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="05a4e-110">例: 2012/12/31</span><span class="sxs-lookup"><span data-stu-id="05a4e-110">For example: 2012/12/31</span></span>  
4. <span data-ttu-id="05a4e-111">[決済期間] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-111">In the Settlement period field, type a value.</span></span>
5. <span data-ttu-id="05a4e-112">[申告のタイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-112">In the Declaration type field, select an option.</span></span>
6. <span data-ttu-id="05a4e-113">[計算方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-113">In the Calculation method field, select an option.</span></span>
7. <span data-ttu-id="05a4e-114">[修正] フィールドで、 [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-114">Select Yes in the Amendment field.</span></span>
    * <span data-ttu-id="05a4e-115">以前にレポートを生成し、もう一度生成する場合は、既存のレコードの修正を更新するように選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05a4e-115">If you have already generated the report previously and you are generating it again, you must choose to update the existing record on the amendment.</span></span>  
8. <span data-ttu-id="05a4e-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-116">Click OK.</span></span>
9. <span data-ttu-id="05a4e-117">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-117">Click Edit.</span></span>
10. <span data-ttu-id="05a4e-118">[項目 6] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-118">In the Item 6 field, enter a number.</span></span>
    * <span data-ttu-id="05a4e-119">データはトランザクションから取得され、集計されます。</span><span class="sxs-lookup"><span data-stu-id="05a4e-119">The data is retrieved and summarized from the transactions.</span></span> <span data-ttu-id="05a4e-120">調整のために編集可能なフィールドを更新できます。</span><span class="sxs-lookup"><span data-stu-id="05a4e-120">You can update the editable fields for adjustment purposes.</span></span>  
11. <span data-ttu-id="05a4e-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-121">Click Save.</span></span>
12. <span data-ttu-id="05a4e-122">[金額の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-122">Click Update amount.</span></span>
    * <span data-ttu-id="05a4e-123">これにより、金額を再計算します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-123">This recalculates the amounts.</span></span>  
13. <span data-ttu-id="05a4e-124">[確定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-124">Click Finalize.</span></span>
14. <span data-ttu-id="05a4e-125">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-125">Click Yes.</span></span>
15. <span data-ttu-id="05a4e-126">[消費税申告] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-126">Click Consumption tax report.</span></span>
16. <span data-ttu-id="05a4e-127">[税額の計算] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-127">Click the Tax calculation tab.</span></span>
17. <span data-ttu-id="05a4e-128">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-128">Click Edit.</span></span>
18. <span data-ttu-id="05a4e-129">[項目 10] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-129">In the Item 10 field, enter a number.</span></span>
19. <span data-ttu-id="05a4e-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-130">Click Save.</span></span>
20. <span data-ttu-id="05a4e-131">[金額の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-131">Click Update amount.</span></span>
21. <span data-ttu-id="05a4e-132">[追加情報] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-132">Click the Additional information tab.</span></span>
    * <span data-ttu-id="05a4e-133">[追加情報] タブでは、情報を、コンフィギュレーションされたとおりに印刷します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-133">In the Additional information tab, the information is printed as configured.</span></span>  
    * <span data-ttu-id="05a4e-134">例: [割賦基準の適用] スライダーを「はい」に変更して、最終レポート上に印刷します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-134">For example: you can change the Installment basis slider to be 'Yes' to print a yes on the final report.</span></span>  
22. <span data-ttu-id="05a4e-135">[確定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-135">Click Finalize.</span></span>
23. <span data-ttu-id="05a4e-136">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-136">Click Yes.</span></span>
24. <span data-ttu-id="05a4e-137">[アクション] ペインで [消費税申告] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05a4e-137">On the Action Pane, click Consumption tax report.</span></span>
    * <span data-ttu-id="05a4e-138">[レポートを印刷] をクリックして、最終レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="05a4e-138">Click Print reports to generate the final report.</span></span>  

