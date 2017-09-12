--- 
title: "会社間プロジェクト請求のコンフィギュレーション"
description: "この手順では、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。"
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4de7257ed5e9c9c08ec6cc423c29739a541926d5
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="81e6d-103">会社間プロジェクト請求のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="81e6d-103">Configure intercompany project invoicing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81e6d-104">この手順では、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="81e6d-105">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="81e6d-106">[買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="81e6d-107">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="81e6d-108">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="81e6d-109">[会社間] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-109">Click Intercompany.</span></span>
5. <span data-ttu-id="81e6d-110">会社間取引を有効にするには、[アクティブ] に [はい] を設定します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="81e6d-111">[顧客の会社] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="81e6d-112">[自社会社コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="81e6d-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-113">Click Save.</span></span>
9. <span data-ttu-id="81e6d-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81e6d-114">Close the page.</span></span>
10. <span data-ttu-id="81e6d-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81e6d-115">Close the page.</span></span>
11. <span data-ttu-id="81e6d-116">[プロジェクト管理および会計] > [設定] > [プロジェクト管理および会計パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="81e6d-117">[会社間] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="81e6d-118">スライダーを [はい] まで動かして、会社間リソース スケジューリングとタイムシートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="81e6d-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="81e6d-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-120">Click New.</span></span>
16. <span data-ttu-id="81e6d-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="81e6d-122">[借入側の法人] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="81e6d-123">[未収収益] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="81e6d-124">[既定のタイムシート カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="81e6d-125">[既定の経費カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="81e6d-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-126">Click Save.</span></span>
22. <span data-ttu-id="81e6d-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81e6d-127">Close the page.</span></span>
23. <span data-ttu-id="81e6d-128">[プロジェクト管理および会計] > [設定] > [転記] > [元帳転記の設定] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="81e6d-129">[勘定タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="81e6d-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-130">Click New.</span></span>
26. <span data-ttu-id="81e6d-131">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="81e6d-132">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="81e6d-133">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="81e6d-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-134">Click Save.</span></span>
30. <span data-ttu-id="81e6d-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="81e6d-135">Close the page.</span></span>
31. <span data-ttu-id="81e6d-136">[プロジェクト管理および会計] > [設定] > [価格] > [移転価格] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="81e6d-137">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-137">Click New.</span></span>
33. <span data-ttu-id="81e6d-138">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="81e6d-139">[借入側の法人] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="81e6d-140">[移転価格モデル] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="81e6d-141">[価格決定] フィールドに、数を入力します。</span><span class="sxs-lookup"><span data-stu-id="81e6d-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="81e6d-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81e6d-142">Click Save.</span></span>


