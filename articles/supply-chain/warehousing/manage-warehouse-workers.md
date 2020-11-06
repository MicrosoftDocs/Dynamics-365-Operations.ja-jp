---
title: 倉庫作業者の管理
description: この記事では、倉庫の従業員によって実行される作業の管理と監視に、倉庫アプリを使用する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage, WHSResetUserPassword
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2156b5de6abc3751cae1822b3825acbbd0b9a712
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017092"
---
# <a name="manage-warehouse-workers"></a><span data-ttu-id="71786-103">倉庫作業者の管理</span><span class="sxs-lookup"><span data-stu-id="71786-103">Manage warehouse workers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71786-104">この記事では、倉庫の従業員によって実行される作業の管理と監視に、倉庫アプリを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="71786-104">This article describes how you can use the warehouse app to help control and monitor the work that's carried out by employees in your warehouses.</span></span>

<span data-ttu-id="71786-105">倉庫管理で機能を使用すると、すべての倉庫作業員の工程は *作業* 呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="71786-105">If you're using the functionality in Warehouse management, all warehouse worker operations are referred to as *work*.</span></span> <span data-ttu-id="71786-106">ピッキング、移動、および手持在庫の棚卸などの作業は、モバイル デバイスを使用して記録されます。</span><span class="sxs-lookup"><span data-stu-id="71786-106">Work such as picking, moving, and counting on-hand inventory is recorded by using mobile devices.</span></span> <span data-ttu-id="71786-107">倉庫作業者が作業を実行する前に、作業者は人事管理の作業者と関連付けられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="71786-107">Before a warehouse worker can perform work, he or she must be associated with a worker in Human resources.</span></span> <span data-ttu-id="71786-108">各 **作業者** のアカウントは、関連付けられる複数の倉庫のユーザーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="71786-108">Each **Worker** account can have multiple warehouse work users associated with it.</span></span> <span data-ttu-id="71786-109">これらの作業ユーザーは異なる倉庫で、異なるレベルのさまざまなモバイル デバイス メニューへのアクセスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="71786-109">Those work users can work in different warehouses and can have different levels of access to the various mobile device menus.</span></span> <span data-ttu-id="71786-110">倉庫の作業ユーザーを、選択した作業者に対しての複数のログオンとして考えることができます。</span><span class="sxs-lookup"><span data-stu-id="71786-110">You can think of the warehouse work users as multiple logons for the selected worker.</span></span> <span data-ttu-id="71786-111">各作業ユーザーには既定の倉庫があり、作業ユーザーに利用可能なメニュー項目によって特定のワークフローが公開されます。</span><span class="sxs-lookup"><span data-stu-id="71786-111">Each work user has a default warehouse, and specific workflows are exposed by the menus items that are available to that work user.</span></span> 

<span data-ttu-id="71786-112">新たな作業ユーザーを作成する場合は、 **倉庫** セクションの、 **一般** タブの、 **作業者** ページで、 **作業者** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71786-112">To create a new work user, on the **Workers** page, on the **General** tab, in the **Warehouses** section, click **Worker**.</span></span> <span data-ttu-id="71786-113">ユーザー ID、ユーザー名、既定の倉庫、およびメニュー名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71786-113">You must specify a user ID, a user name, a default warehouse, and a menu name.</span></span> <span data-ttu-id="71786-114">倉庫モバイル デバイス ポータルにユーザーがサインインするとき、このメニューが読み込まれ、どのメニュー項目へユーザーがアクセスできるかを定義できます。</span><span class="sxs-lookup"><span data-stu-id="71786-114">This menu is loaded when the user signs in to the Warehouse Mobile Device Portal, and lets you define which menu items the user has access to.</span></span> 

<span data-ttu-id="71786-115">各作業ユーザーの設定の一部として、特定のワークフロー プロセスも定義できます。</span><span class="sxs-lookup"><span data-stu-id="71786-115">As part of the setup for each work user, you can also define specific process workflows.</span></span> <span data-ttu-id="71786-116">たとえば、 **循環棚卸の監督ですか** フィールドを使用して、ユーザーが棚卸の工程中に循環棚卸の不一致の調整を処理できるか、または、これらの調整を別のユーザーが最初に確認するべきかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="71786-116">For example, you can use the **Is a cycle count supervisor** field to specify whether the user can process adjustments to cycle counting discrepancies during a counting operation, or whether these adjustments must first be reviewed by another person.</span></span>

## <a name="defining-labor-standards"></a><span data-ttu-id="71786-117">労務標準の定義</span><span class="sxs-lookup"><span data-stu-id="71786-117">Defining labor standards</span></span>
<span data-ttu-id="71786-118">**労務標準** ページで、システムが特定のタイプの作業が必要とする見積時間の計算に使用する計算方法を定義できます。</span><span class="sxs-lookup"><span data-stu-id="71786-118">The **Labor standards** page lets you define the calculation methods that the system uses to calculate the estimated time that a particular type of work should require.</span></span> <span data-ttu-id="71786-119">この定義は、一般レベルまたは特定のレベルで設定できます。</span><span class="sxs-lookup"><span data-stu-id="71786-119">This definition can be set on a generic level or on a specific level.</span></span> <span data-ttu-id="71786-120">たとえば、特定のピッキング プロセスが使用されるとき、特定の定義単位重量あたりの、販売注文のピッキング処理をするために必要な時間を定義できます。</span><span class="sxs-lookup"><span data-stu-id="71786-120">For example, you can define the time that should be required in order to process a sales order pick per weight for a specific unit definition when a specific picking process is used.</span></span> <span data-ttu-id="71786-121">同時に、ピッキング済の手持在庫のプット工程を、別の計算方法に基づいて記録できます。</span><span class="sxs-lookup"><span data-stu-id="71786-121">At the same time, you can record the time, based on another calculation method, for the put operation of the on-hand inventory that is picked.</span></span> 

<span data-ttu-id="71786-122">ユーザー定義の労務標準を有効にするには、労務標準を使用する各倉庫の **労務標準の許可** オプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71786-122">To enable the labor standards that you've defined, you must select the **Allow labor standards** option for each warehouse where labor standards will be used.</span></span>

## <a name="monitoring-and-controlling-warehouse-work"></a><span data-ttu-id="71786-123">倉庫作業の監視および制御</span><span class="sxs-lookup"><span data-stu-id="71786-123">Monitoring and controlling warehouse work</span></span>
<span data-ttu-id="71786-124">**すべての作業** ページで、計画された、処理中の、および完了したすべての作業を監視および管理することができます。</span><span class="sxs-lookup"><span data-stu-id="71786-124">The **All work** page lets you monitor and maintain all work that is planned, in progress, and completed.</span></span> <span data-ttu-id="71786-125">このページで、倉庫のユーザーの割り当ておよび作業優先順位のさまざまなプロセスを更新できます。</span><span class="sxs-lookup"><span data-stu-id="71786-125">From this page, you can update various processes, such as warehouse work user assignments and work priority.</span></span> <span data-ttu-id="71786-126">予定あるいは完成作業プロセスを理解するために、作業ヘッダーおよび作業明細行に関連付けられた詳細にドリルダウンすることもできます。</span><span class="sxs-lookup"><span data-stu-id="71786-126">You can also drill down into the details that are related to the work header and work lines to gain an understanding of the expected or completed work processes.</span></span> 

<span data-ttu-id="71786-127">**労務標準** オプションを有効にすると、作業の計算された見積時間を確認できます。</span><span class="sxs-lookup"><span data-stu-id="71786-127">If you enable the **Labor standards** option, you can see the calculated estimated time for the work.</span></span> <span data-ttu-id="71786-128">その後、作業を処理する場合、各作業の実際の時間も示されます。</span><span class="sxs-lookup"><span data-stu-id="71786-128">Then, when the work is processed, the actual time will also be shown for each work operation.</span></span> <span data-ttu-id="71786-129">これにより、実際の時間と見積時間を比較できます。</span><span class="sxs-lookup"><span data-stu-id="71786-129">In this way, you can compare the estimated time calculations to the actual time.</span></span> 

<span data-ttu-id="71786-130">また、作業の作成時に自動的に作業を分割するルールで見積時間を使用できます。</span><span class="sxs-lookup"><span data-stu-id="71786-130">Additionally, you can use the estimated time in the rules for automatically splitting work during work creation.</span></span> <span data-ttu-id="71786-131">これにより、タスクを完了する予想時間に基づいて、負荷分散作業をすることができます。</span><span class="sxs-lookup"><span data-stu-id="71786-131">In this way, you can load balance work, based on the expected time to complete the tasks.</span></span> 

<span data-ttu-id="71786-132">作業項目の処理に使用される時間の分析は、倉庫作業員の効率の改善に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="71786-132">Analysis of the time that is used to process work items can help drive improvements in the warehouse workers’ efficiency.</span></span> <span data-ttu-id="71786-133">次のレポートがこの分析に使用できます:</span><span class="sxs-lookup"><span data-stu-id="71786-133">The following reports are available to help with this analysis:</span></span>

-   <span data-ttu-id="71786-134">**ユーザー別の労務** – このレポートは、予想時間に対して、実際の時間に基づいて作業者の生産性を表示します。</span><span class="sxs-lookup"><span data-stu-id="71786-134">**Labor by user** – This report shows worker productivity, based on actual times against expected times.</span></span>
-   <span data-ttu-id="71786-135">**作業トランザクション タイプ別の労務** – 特定の倉庫プロセスの非能率性を調査するのに、このレポートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="71786-135">**Labor by work transaction type** – You can use this report to investigate inefficiencies in specific warehouse processes.</span></span> <span data-ttu-id="71786-136">たとえば、移動オーダーのピッキングが、今週は前の週よりも長い時間がかかっていることに気づきます。</span><span class="sxs-lookup"><span data-stu-id="71786-136">For example, you notice that picks for transfer orders are taking longer this week than in previous weeks.</span></span> <span data-ttu-id="71786-137">詳細な調査に対してこの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="71786-137">You can then use this information for further investigation.</span></span>




