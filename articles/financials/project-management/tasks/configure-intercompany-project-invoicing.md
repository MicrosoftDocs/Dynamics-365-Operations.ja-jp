---
title: 会社間プロジェクト請求のコンフィギュレーション
description: この手順では、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "352761"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="d718b-103">会社間プロジェクト請求のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d718b-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d718b-104">この手順では、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d718b-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="d718b-105">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="d718b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d718b-106">[買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d718b-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d718b-107">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d718b-108">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="d718b-109">[会社間] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-109">Click Intercompany.</span></span>
5. <span data-ttu-id="d718b-110">会社間取引を有効にするには、[アクティブ] に [はい] を設定します。</span><span class="sxs-lookup"><span data-stu-id="d718b-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="d718b-111">[顧客の会社] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="d718b-112">[自社会社コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="d718b-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-113">Click Save.</span></span>
9. <span data-ttu-id="d718b-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d718b-114">Close the page.</span></span>
10. <span data-ttu-id="d718b-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d718b-115">Close the page.</span></span>
11. <span data-ttu-id="d718b-116">[プロジェクト管理および会計] > [設定] > [プロジェクト管理および会計パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d718b-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="d718b-117">[会社間] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="d718b-118">スライダーを [はい] まで動かして、会社間リソース スケジューリングとタイムシートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d718b-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="d718b-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d718b-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="d718b-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-120">Click New.</span></span>
16. <span data-ttu-id="d718b-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d718b-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d718b-122">[借入側の法人] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="d718b-123">[未収収益] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="d718b-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="d718b-124">[既定のタイムシート カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="d718b-125">[既定の経費カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="d718b-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-126">Click Save.</span></span>
22. <span data-ttu-id="d718b-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d718b-127">Close the page.</span></span>
23. <span data-ttu-id="d718b-128">[プロジェクト管理および会計] > [設定] > [転記] > [元帳転記の設定] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d718b-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="d718b-129">[勘定タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="d718b-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-130">Click New.</span></span>
26. <span data-ttu-id="d718b-131">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d718b-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="d718b-132">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d718b-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="d718b-133">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d718b-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="d718b-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-134">Click Save.</span></span>
30. <span data-ttu-id="d718b-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d718b-135">Close the page.</span></span>
31. <span data-ttu-id="d718b-136">[プロジェクト管理および会計] > [設定] > [価格] > [移転価格] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="d718b-137">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-137">Click New.</span></span>
33. <span data-ttu-id="d718b-138">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="d718b-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="d718b-139">[借入側の法人] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="d718b-140">[移転価格モデル] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d718b-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="d718b-141">[価格決定] フィールドに、数を入力します。</span><span class="sxs-lookup"><span data-stu-id="d718b-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="d718b-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d718b-142">Click Save.</span></span>

