---
title: 会社間計画の作成
description: この手順では、会社間計画を作成する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a321f7e781f1ae93d8a69ee45a0e6e8e6eeb1e8d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150335"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="6ed10-103">会社間計画の作成</span><span class="sxs-lookup"><span data-stu-id="6ed10-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ed10-104">この手順では、会社間計画を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="6ed10-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6ed10-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="6ed10-106">会社間計画グループを設定する</span><span class="sxs-lookup"><span data-stu-id="6ed10-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="6ed10-107">**ナビゲーション ウィンドウ**で、**モジュール > マスター プラン > 設定 > 会社間計画グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="6ed10-108">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="6ed10-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6ed10-109">たとえば、値「10」を含む [名前] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="6ed10-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6ed10-111">**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-111">Click **Delete**.</span></span> <span data-ttu-id="6ed10-112">この手順は、会社間の計画実行の期間を短縮するのに必要です。</span><span class="sxs-lookup"><span data-stu-id="6ed10-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="6ed10-113">会社間計画では、最下位のスケジューリングシーケンスから始まる計画グループにおける会社のマスタープランが実施されます。</span><span class="sxs-lookup"><span data-stu-id="6ed10-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="6ed10-114">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-114">Click **Yes**.</span></span>
6. <span data-ttu-id="6ed10-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6ed10-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="6ed10-116">会社間計画の作成</span><span class="sxs-lookup"><span data-stu-id="6ed10-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="6ed10-117">**ナビゲーション ウィンドウ**で、**モジュール > マスター プラン > ワークスペース > マスター プラン**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="6ed10-118">**会社間マスター プラン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="6ed10-119">**会社間計画グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6ed10-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6ed10-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="6ed10-121">会社間計画グループ 10を選択する</span><span class="sxs-lookup"><span data-stu-id="6ed10-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="6ed10-122">**会社間計画の繰り返し回数**フィールドで、'2' と入力します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="6ed10-123">会社間計画グループ10にはメンバーが2名います。</span><span class="sxs-lookup"><span data-stu-id="6ed10-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="6ed10-124">顧客の会社 (DEMF) にソースの会社 (USMF) の遅延を反映させるには、両方の会社で会社間計画を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ed10-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="6ed10-125">最初の繰り返しが需要を反映し、ソースの会社 (USMF)の遅延を識別します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="6ed10-126">2番目の繰り返しはUSMFからDEMFへの遅延を反映します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="6ed10-127">**最初の繰り返し**フィールドで、'再生成' を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="6ed10-128">**後の繰り返し**フィールドで、'再生成' を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="6ed10-129">**スレッド数**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="6ed10-130">これは、計画に使用される並行スレッドの数を表します。</span><span class="sxs-lookup"><span data-stu-id="6ed10-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="6ed10-131">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="6ed10-132">計画の結果を表示する</span><span class="sxs-lookup"><span data-stu-id="6ed10-132">View the result of the plan</span></span>
1. <span data-ttu-id="6ed10-133">**計画**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6ed10-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="6ed10-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="6ed10-135">StaticPlanのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="6ed10-136">会社USMFにいる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ed10-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="6ed10-137">**計画オーダー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6ed10-137">Click **Planned orders**.</span></span>

