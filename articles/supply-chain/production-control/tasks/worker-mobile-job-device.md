---
title: モバイル ジョブ デバイスを使用した作業者のコンフィギュレーション
description: このトピックでは、作業者のユーザー アカウントに適切なロールを割り当てる方法を表示します。それによって、作業者が作業現場の登録を行う方法を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1086a88c341b95d6af03adc81c4e3e5d76adc69
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210206"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="3f397-103">モバイル ジョブ デバイスを使用した作業者のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3f397-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f397-104">このトピックでは、作業者のユーザー アカウントに適切なロールを割り当てる方法を表示します。それによって、作業者が作業現場の登録を行う方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3f397-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="3f397-105">作業者に特定のロールが割り当てられていることを確認する</span><span class="sxs-lookup"><span data-stu-id="3f397-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="3f397-106">この例では、作業者アカウントを構成する前に、ユーザー "SHANNON" に機械オペレータのロールが割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3f397-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="3f397-107">**ナビゲーション ウィンドウ > モジュール > システム管理 > ユーザー > ユーザー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3f397-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="3f397-108">クイック フィルターでユーザーを検索します。</span><span class="sxs-lookup"><span data-stu-id="3f397-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="3f397-109">この例では、`shannon` を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f397-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="3f397-110">表示されるユーザー アカウントの**ユーザー ID** 列のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="3f397-111">**ユーザーのロール** ツリーで、**ロール > 機械オペレーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="3f397-112">**ユーザーの詳細**ページと**ユーザー** ページを閉じて、ホーム ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="3f397-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="3f397-113">作業者のアカウンの構成</span><span class="sxs-lookup"><span data-stu-id="3f397-113">Configure worker account</span></span>
1. <span data-ttu-id="3f397-114">**ナビゲーション ウィンドウ > モジュール > 人事部 > 作業者 > 作業者**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3f397-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="3f397-115">クイック フィルターでユーザーを検索します。</span><span class="sxs-lookup"><span data-stu-id="3f397-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="3f397-116">この例では、`shannon` を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f397-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="3f397-117">表示されるユーザー アカウントの**名前**列のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="3f397-118">**時間登録**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="3f397-119">**登録ターミナルで有効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="3f397-120">次のフィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="3f397-121">**計算グループ**</span><span class="sxs-lookup"><span data-stu-id="3f397-121">**Calculation group**</span></span>  
    - <span data-ttu-id="3f397-122">**既定の計算グループ**</span><span class="sxs-lookup"><span data-stu-id="3f397-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="3f397-123">**承認グループ**</span><span class="sxs-lookup"><span data-stu-id="3f397-123">**Approval group**</span></span>  
    - <span data-ttu-id="3f397-124">**標準プロファイル**</span><span class="sxs-lookup"><span data-stu-id="3f397-124">**Standard profile**</span></span>  
    - <span data-ttu-id="3f397-125">**プロファイル グループ**</span><span class="sxs-lookup"><span data-stu-id="3f397-125">**Profile group**</span></span>  

7. <span data-ttu-id="3f397-126">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-126">Select **OK**.</span></span>
8. <span data-ttu-id="3f397-127">**編集**を選択して、新しい時間登録作業者のバッジ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f397-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="3f397-128">**バッジ ID** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f397-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="3f397-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-129">Select **Save**.</span></span>
10. <span data-ttu-id="3f397-130">**作業者の詳細**と**作業者**のページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3f397-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="3f397-131">デバイス グループに作業者を割り当てる</span><span class="sxs-lookup"><span data-stu-id="3f397-131">Assign worker to device group</span></span>
1. <span data-ttu-id="3f397-132">**生産産管理 > 設定 > 製造実行 > デバイスのジョブ カードのコンフィギュレーション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3f397-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="3f397-133">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-133">Select **Add**.</span></span>
3. <span data-ttu-id="3f397-134">一覧で、目的の作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-134">In the list, select the desired worker.</span></span> <span data-ttu-id="3f397-135">この例では、**SHANNON** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="3f397-136">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-136">Select **OK**.</span></span>
5. <span data-ttu-id="3f397-137">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f397-137">Select **Edit**.</span></span>
6. <span data-ttu-id="3f397-138">**生産単位**フィールドで、作業者の既定のフィルターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3f397-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="3f397-139">これにより作業者がデバイスにログオンするときに、選択した生産単位の生産ジョブのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f397-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="3f397-140">目的の値の入力します。</span><span class="sxs-lookup"><span data-stu-id="3f397-140">Enter the desired value.</span></span>
7. <span data-ttu-id="3f397-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3f397-141">Close the page.</span></span>

