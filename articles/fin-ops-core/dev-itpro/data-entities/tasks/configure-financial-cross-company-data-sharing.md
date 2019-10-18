---
title: 会社間財務データ共有のコンフィギュレーション
description: この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc368351641f3e2432dfdbbaf8eed8694595bd4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184373"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="1bf9c-103">会社間財務データ共有のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1bf9c-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bf9c-104">この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="1bf9c-105">これは、USMF 社と財務データ共有テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="1bf9c-106">このタスク ガイドでは、Dynamics AX platform 7.1 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="1bf9c-107">**ナビゲーション ウィンドウ > モジュール > システム管理 > ワークスペース > データ管理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="1bf9c-108">**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-108">Click **Import**.</span></span>
3. <span data-ttu-id="1bf9c-109">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="1bf9c-110">**ソース データ形式**フィールドで、「パッケージ」タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="1bf9c-111">**アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-111">Click **Upload**.</span></span> <span data-ttu-id="1bf9c-112">財務データ共有テンプレート パッケージ ファイルの場所に移動し、そのファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="1bf9c-113">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-113">Click **Save**.</span></span>
6. <span data-ttu-id="1bf9c-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-114">In the list, mark the selected row.</span></span> <span data-ttu-id="1bf9c-115">作成したデータ共有ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="1bf9c-116">**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-116">Click **Import**.</span></span>
8. <span data-ttu-id="1bf9c-117">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-117">Click **Close**.</span></span>
9. <span data-ttu-id="1bf9c-118">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-118">Refresh the page.</span></span>
10. <span data-ttu-id="1bf9c-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-119">Close the page.</span></span>
11. <span data-ttu-id="1bf9c-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-120">Close the page.</span></span>
12. <span data-ttu-id="1bf9c-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-121">Close the page.</span></span>
13. <span data-ttu-id="1bf9c-122">**ナビゲーション ウィンドウ > モジュール > システム管理 > セットアップ > 会社間データ共有のコンフィギュレーション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="1bf9c-123">一覧で**支払期日**を検索して、選択します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="1bf9c-124">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-124">Click **Add**.</span></span>
16. <span data-ttu-id="1bf9c-125">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="1bf9c-126">**会社**フィールドで、「USSI」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="1bf9c-127">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-127">Click **Add**.</span></span>
19. <span data-ttu-id="1bf9c-128">**会社**フィールドで、「USMF」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="1bf9c-129">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-129">Click **Save**.</span></span>
21. <span data-ttu-id="1bf9c-130">**有効化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-130">Click **Enable**.</span></span>
22. <span data-ttu-id="1bf9c-131">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-131">Click **Yes**.</span></span>
23. <span data-ttu-id="1bf9c-132">**共有の問題を検索する**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="1bf9c-133">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-133">Click **Yes**.</span></span>
25. <span data-ttu-id="1bf9c-134">**フィールド値の更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="1bf9c-135">**会社 1 の値を使用**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="1bf9c-136">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-136">Refresh the page.</span></span>
28. <span data-ttu-id="1bf9c-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1bf9c-137">Close the page.</span></span>

