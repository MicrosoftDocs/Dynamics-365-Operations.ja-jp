---
title: 会社間計画の作成
description: この手順では、会社間計画を作成する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978276"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="0a1a2-103">会社間計画の作成</span><span class="sxs-lookup"><span data-stu-id="0a1a2-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a1a2-104">この手順では、会社間計画を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="0a1a2-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="0a1a2-106">会社間計画グループを設定する</span><span class="sxs-lookup"><span data-stu-id="0a1a2-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="0a1a2-107">**ナビゲーション ウィンドウ**で、**モジュール > マスター プラン > 設定 > 会社間計画グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="0a1a2-108">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0a1a2-109">たとえば、値「10」を含む [名前] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="0a1a2-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0a1a2-111">**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-111">Click **Delete**.</span></span> <span data-ttu-id="0a1a2-112">この手順は、会社間の計画実行の期間を短縮するのに必要です。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="0a1a2-113">会社間計画では、最下位のスケジューリングシーケンスから始まる計画グループにおける会社のマスタープランが実施されます。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="0a1a2-114">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-114">Click **Yes**.</span></span>
6. <span data-ttu-id="0a1a2-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="0a1a2-116">会社間計画の作成</span><span class="sxs-lookup"><span data-stu-id="0a1a2-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="0a1a2-117">**ナビゲーション ウィンドウ**で、**モジュール > マスター プラン > ワークスペース > マスター プラン**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="0a1a2-118">**会社間マスター プラン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="0a1a2-119">**会社間計画グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0a1a2-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="0a1a2-121">会社間計画グループ 10を選択する</span><span class="sxs-lookup"><span data-stu-id="0a1a2-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="0a1a2-122">**会社間計画の繰り返し回数**フィールドで、'2' と入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="0a1a2-123">会社間計画グループ10にはメンバーが2名います。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="0a1a2-124">顧客の会社 (DEMF) にソースの会社 (USMF) の遅延を反映させるには、両方の会社で会社間計画を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="0a1a2-125">最初の繰り返しが需要を反映し、ソースの会社 (USMF)の遅延を識別します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="0a1a2-126">2番目の繰り返しはUSMFからDEMFへの遅延を反映します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="0a1a2-127">**最初の繰り返し**フィールドで、'再生成' を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="0a1a2-128">**後の繰り返し**フィールドで、'再生成' を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="0a1a2-129">**スレッド数**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="0a1a2-130">これは、計画に使用される並行スレッドの数を表します。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="0a1a2-131">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="0a1a2-132">計画の結果を表示する</span><span class="sxs-lookup"><span data-stu-id="0a1a2-132">View the result of the plan</span></span>
1. <span data-ttu-id="0a1a2-133">**計画**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="0a1a2-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="0a1a2-135">StaticPlanのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="0a1a2-136">会社USMFにいる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="0a1a2-137">**計画オーダー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a1a2-137">Click **Planned orders**.</span></span>

