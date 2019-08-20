---
title: 会社間財務データ共有のコンフィギュレーション
description: この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 049ffeee7db95cc2e5a31526d5d99026303456be
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848258"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="6c5a3-103">会社間財務データ共有のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6c5a3-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c5a3-104">この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="6c5a3-105">これは、USMF 社と財務データ共有テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="6c5a3-106">このタスク ガイドでは、Dynamics AX platform 7.1 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="6c5a3-107">[システム管理] > [ワークスペース] > [データ管理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="6c5a3-108">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-108">Click Import.</span></span>
3. <span data-ttu-id="6c5a3-109">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6c5a3-110">[ソース データ形式] フィールドで、[パッケージ] タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="6c5a3-111">[アップロード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-111">Click Upload.</span></span> <span data-ttu-id="6c5a3-112">財務データ共有テンプレート パッケージ ファイルの場所に移動し、そのファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="6c5a3-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-113">Click Save.</span></span>
6. <span data-ttu-id="6c5a3-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6c5a3-115">作成したデータ共有ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="6c5a3-116">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-116">Click Import.</span></span>
8. <span data-ttu-id="6c5a3-117">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-117">Click Close.</span></span>
9. <span data-ttu-id="6c5a3-118">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-118">Refresh the page.</span></span>
10. <span data-ttu-id="6c5a3-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-119">Close the page.</span></span>
11. <span data-ttu-id="6c5a3-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-120">Close the page.</span></span>
12. <span data-ttu-id="6c5a3-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-121">Close the page.</span></span>
13. <span data-ttu-id="6c5a3-122">[システム管理] > [設定] > [会社間データ共有のコンフィギュレーション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="6c5a3-123">一覧で、[支払期日] を検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="6c5a3-124">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-124">Click Add.</span></span>
16. <span data-ttu-id="6c5a3-125">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="6c5a3-126">[会社] フィールドで、「USSI」と入力します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="6c5a3-127">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-127">Click Add.</span></span>
19. <span data-ttu-id="6c5a3-128">[会社] フィールドで、「USMF」と入力します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="6c5a3-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-129">Click Save.</span></span>
21. <span data-ttu-id="6c5a3-130">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-130">Click Enable.</span></span>
22. <span data-ttu-id="6c5a3-131">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-131">Click Yes.</span></span>
23. <span data-ttu-id="6c5a3-132">[共有の問題を検索する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="6c5a3-133">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-133">Click Yes.</span></span>
25. <span data-ttu-id="6c5a3-134">[フィールド値の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-134">Click Update field value.</span></span>
26. <span data-ttu-id="6c5a3-135">[会社 1 の値を使用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="6c5a3-136">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-136">Refresh the page.</span></span>
28. <span data-ttu-id="6c5a3-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-137">Close the page.</span></span>

