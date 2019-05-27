---
title: 資産除去責務の支払利子の減価償却および見越計上
description: 日本では、資産除去責務 (ARO) の減価償却は固定資産と一緒に処理されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 499424f361c8e764e198ac056e058b0bf196a82f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565083"
---
# <a name="depreciate-and-accrue-the-interest-expense-for-asset-retirement-obligations"></a><span data-ttu-id="33d03-103">資産除去責務の支払利子の減価償却および見越計上</span><span class="sxs-lookup"><span data-stu-id="33d03-103">Depreciate and accrue the interest expense for asset retirement obligations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33d03-104">日本では、資産除去責務 (ARO) の減価償却は固定資産と一緒に処理されます。</span><span class="sxs-lookup"><span data-stu-id="33d03-104">For Japan, the depreciation of the asset retirement obligations (ARO) is processed along with the fixed asset.</span></span> <span data-ttu-id="33d03-105">また、ARO の総額を認識するためには、支払利子を見越計上する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33d03-105">In addition, interest expenses need to be accrued to recognize the full amount of the ARO.</span></span>



<span data-ttu-id="33d03-106">このタスクを使用して、ARO を減価償却し支払利子を見越計上します。</span><span class="sxs-lookup"><span data-stu-id="33d03-106">Use this task to depreciate the ARO and accrue the interest expense.</span></span> 



<span data-ttu-id="33d03-107">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33d03-107">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="33d03-108">このタスクはデモ会社 JPMF のデータを使用して完了しました。</span><span class="sxs-lookup"><span data-stu-id="33d03-108">This task was completed using the JPMF demo company data.</span></span>


## <a name="depreciate-a-fixed-asset-with-asset-retirement-obligation"></a><span data-ttu-id="33d03-109">資産除去責務がある固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="33d03-109">Depreciate a fixed asset with asset retirement obligation</span></span>
1. <span data-ttu-id="33d03-110">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="33d03-110">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="33d03-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-111">Click New.</span></span>
3. <span data-ttu-id="33d03-112">[名前] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="33d03-112">In the Name field, select a value.</span></span>
4. <span data-ttu-id="33d03-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-113">Click Save.</span></span>
5. <span data-ttu-id="33d03-114">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-114">Click Lines.</span></span>
6. <span data-ttu-id="33d03-115">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-115">Click Proposals.</span></span>
7. <span data-ttu-id="33d03-116">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-116">Click Depreciation proposal.</span></span>
8. <span data-ttu-id="33d03-117">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="33d03-117">In the To date field, enter a date.</span></span>
9. <span data-ttu-id="33d03-118">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-118">Click Filter.</span></span>
10. <span data-ttu-id="33d03-119">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="33d03-119">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="33d03-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-120">Click OK.</span></span>
12. <span data-ttu-id="33d03-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-121">Click OK.</span></span>
    * <span data-ttu-id="33d03-122">資産除去責務の減価償却は、[ドキュメント タイプ] フィールドごとに示されます。</span><span class="sxs-lookup"><span data-stu-id="33d03-122">The depreciation of asset retirement obligation is indicated by Document type field.</span></span>  
13. <span data-ttu-id="33d03-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-123">Click Post.</span></span>

## <a name="accrue-the-interest-expense"></a><span data-ttu-id="33d03-124">支払利子の計上</span><span class="sxs-lookup"><span data-stu-id="33d03-124">Accrue the interest expense</span></span>
1. <span data-ttu-id="33d03-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="33d03-125">Close the page.</span></span>
2. <span data-ttu-id="33d03-126">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="33d03-126">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
3. <span data-ttu-id="33d03-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-127">Click New.</span></span>
4. <span data-ttu-id="33d03-128">[名前] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="33d03-128">In the Name field, select a value.</span></span>
5. <span data-ttu-id="33d03-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-129">Click Save.</span></span>
6. <span data-ttu-id="33d03-130">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-130">Click Lines.</span></span>
7. <span data-ttu-id="33d03-131">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-131">Click Proposals.</span></span>
8. <span data-ttu-id="33d03-132">[除去費用の費用配分] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-132">Click Asset retirement obligation - accretion expense.</span></span>
9. <span data-ttu-id="33d03-133">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="33d03-133">In the To date field, enter a date.</span></span>
10. <span data-ttu-id="33d03-134">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-134">Click Filter.</span></span>
11. <span data-ttu-id="33d03-135">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="33d03-135">In the Criteria field, type a value.</span></span>
12. <span data-ttu-id="33d03-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-136">Click OK.</span></span>
13. <span data-ttu-id="33d03-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-137">Click OK.</span></span>
    * <span data-ttu-id="33d03-138">支払利子のレコードが提案されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="33d03-138">Confirm that the records for interest expenses are proposed.</span></span>  
    * <span data-ttu-id="33d03-139">支払利子は、トランザクション タイプごとに示されます。</span><span class="sxs-lookup"><span data-stu-id="33d03-139">The interest expenses are indicated by Transaction type</span></span>  
14. <span data-ttu-id="33d03-140">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d03-140">Click Post.</span></span>

