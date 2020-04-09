---
title: 会社間プロジェクト請求のコンフィギュレーション
description: このトピックでは、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144282"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="cd457-103">会社間プロジェクト請求のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cd457-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd457-104">このトピックでは、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cd457-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="cd457-105">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd457-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="cd457-106">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 仕入先 > すべての仕入先**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd457-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="cd457-107">**すべての仕入先**一覧で、目的のレコードを検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="cd457-108">アクション ウィンドウで、**一般**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="cd457-109">**会社間**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="cd457-110">会社間取引を有効にするには、**アクティブ**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="cd457-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="cd457-111">**顧客の会社**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="cd457-112">**自社会社コード** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="cd457-113">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-113">Select **Save**.</span></span>
9. <span data-ttu-id="cd457-114">ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="cd457-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="cd457-115">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > プロジェクト管理および会計パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd457-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="cd457-116">**会社間**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="cd457-117">スライダーを**はい**まで動かして、会社間リソース スケジューリングとタイムシートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="cd457-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="cd457-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cd457-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="cd457-119">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-119">Select **New**.</span></span>
15. <span data-ttu-id="cd457-120">**借入側の法人**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="cd457-121">**未収収益**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="cd457-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="cd457-122">**既定のタイムシート カテゴリ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="cd457-123">**既定の経費カテゴリ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="cd457-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-124">Select **Save**.</span></span>
20. <span data-ttu-id="cd457-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cd457-125">Close the page.</span></span>
21. <span data-ttu-id="cd457-126">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 転記 > 元帳転記の設定**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd457-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="cd457-127">**勘定タイプ** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="cd457-128">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-128">Select **New**.</span></span>
24. <span data-ttu-id="cd457-129">新しい行の**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd457-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="cd457-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-130">Select **Save**.</span></span>
26. <span data-ttu-id="cd457-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cd457-131">Close the page.</span></span>
27. <span data-ttu-id="cd457-132">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 移転価格**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd457-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="cd457-133">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-133">Select **New**.</span></span>
29. <span data-ttu-id="cd457-134">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd457-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="cd457-135">**借入側の法人**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="cd457-136">**移転価格モデル** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="cd457-137">**価格決定**フィールドに、数を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd457-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="cd457-138">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd457-138">Select **Save**.</span></span>

