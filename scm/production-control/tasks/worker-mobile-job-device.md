--- 
title: "モバイル ジョブ デバイスを使用した作業者のコンフィギュレーション"
description: "この手順では、作業者のユーザー アカウントに適切なロールを割り当てる方法を表示します。それによって、作業者が作業現場の登録を行うことをできるようになります。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d56f861dbbf579e44fcd3fc4d8b45c24029acecc
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="446e8-103">モバイル ジョブ デバイスを使用した作業者のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="446e8-103">Configure a worker using the mobile job device</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="446e8-104">この手順では、作業者のユーザー アカウントに適切なロールを割り当てる方法を表示します。それによって、作業者が作業現場の登録を行うことをできるようになります。</span><span class="sxs-lookup"><span data-stu-id="446e8-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="446e8-105">ユーザー アカウントへのロールの割り当て</span><span class="sxs-lookup"><span data-stu-id="446e8-105">Assign roles to user account</span></span>
1. <span data-ttu-id="446e8-106">[システム管理] > [ユーザー] > [ユーザー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="446e8-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="446e8-107">ユーザー アカウントが機械オペレータのロールに関連付けられる場合に、[クイック フィルター] を使用して、作業者の名前をフィルターします。</span><span class="sxs-lookup"><span data-stu-id="446e8-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="446e8-108">サンプル データでは、名前はシャノンです。</span><span class="sxs-lookup"><span data-stu-id="446e8-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="446e8-109">ユーザー アカウントのレコードを強調表示します。</span><span class="sxs-lookup"><span data-stu-id="446e8-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="446e8-110">一覧から、選択した行で「名前」のリンクをクリックして、ユーザー アカウントの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="446e8-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="446e8-111">ツリーで、「Roles\Machine operator」を選択します。</span><span class="sxs-lookup"><span data-stu-id="446e8-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="446e8-112">ユーザー アカウントの詳細ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="446e8-112">Close the user account details page.</span></span>
7. <span data-ttu-id="446e8-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="446e8-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="446e8-114">作業者のアカウントを構成します。</span><span class="sxs-lookup"><span data-stu-id="446e8-114">Configure worker account.</span></span>
1. <span data-ttu-id="446e8-115">[人事管理] > [作業者] > [作業者] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="446e8-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="446e8-116">ユーザー アカウントが機械オペレータのロールに関連付けられる場合に、[クイック フィルター] を使用して、作業者の名前をフィルターします。</span><span class="sxs-lookup"><span data-stu-id="446e8-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="446e8-117">サンプル データでは、名前はシャノンです。</span><span class="sxs-lookup"><span data-stu-id="446e8-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="446e8-118">ユーザー アカウントのレコードを強調表示します。</span><span class="sxs-lookup"><span data-stu-id="446e8-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="446e8-119">一覧から、選択した行で「名前」のリンクをクリックして、ユーザー アカウントの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="446e8-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="446e8-120">[雇用] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="446e8-121">[時間登録のクイックタブ] を展開し、[登録ターミナルで有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="446e8-122">[登録ターミナルで有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="446e8-123">[計算グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="446e8-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="446e8-124">[既定の計算グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="446e8-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="446e8-125">[承認グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="446e8-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="446e8-126">[標準プロファイル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="446e8-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="446e8-127">[プロファイル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="446e8-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="446e8-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-128">Click OK.</span></span>
14. <span data-ttu-id="446e8-129">[編集] をクリックして、新しい時間登録作業者のバッジ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="446e8-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="446e8-130">[バッジ ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="446e8-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="446e8-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-131">Click Save.</span></span>
17. <span data-ttu-id="446e8-132">[ショートカットの記録保存] を使用します。</span><span class="sxs-lookup"><span data-stu-id="446e8-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="446e8-133">作業者の詳細ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="446e8-133">Close the worker details page.</span></span>
19. <span data-ttu-id="446e8-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="446e8-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="446e8-135">デバイス グループに作業者を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="446e8-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="446e8-136">[生産管理] > [設定] > [製造実行] > [デバイスのジョブ カードのコンフィギュレーション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="446e8-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="446e8-137">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-137">Click Add.</span></span>
3. <span data-ttu-id="446e8-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="446e8-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="446e8-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-139">Click OK.</span></span>
5. <span data-ttu-id="446e8-140">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="446e8-140">Click Edit.</span></span>
6. <span data-ttu-id="446e8-141">[生産単位] フィールドで、作業者の既定のフィルターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="446e8-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="446e8-142">これにより作業者がデバイスにログオンするときに、選択した生産単位の生産ジョブのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="446e8-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="446e8-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="446e8-143">Close the page.</span></span>

