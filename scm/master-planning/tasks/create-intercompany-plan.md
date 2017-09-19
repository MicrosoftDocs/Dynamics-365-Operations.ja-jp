--- 
title: "会社間計画の作成"
description: "この手順では、会社間計画を作成する方法を示します。"
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="c7c51-103">会社間計画の作成</span><span class="sxs-lookup"><span data-stu-id="c7c51-103">Create an intercompany plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7c51-104">この手順では、会社間計画を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="c7c51-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c7c51-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="c7c51-106">会社間計画グループを設定する</span><span class="sxs-lookup"><span data-stu-id="c7c51-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="c7c51-107">[会社間計画グループ] に進みます。</span><span class="sxs-lookup"><span data-stu-id="c7c51-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="c7c51-108">[マスター プラン] > [設定] > [会社間計画グループ]</span><span class="sxs-lookup"><span data-stu-id="c7c51-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="c7c51-109">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c7c51-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c7c51-110">たとえば、値「10」を含む [名前] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="c7c51-111">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c7c51-112">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-112">Click Delete.</span></span>
    * <span data-ttu-id="c7c51-113">この手順は、会社間の計画実行の期間を短縮するのに必要です。</span><span class="sxs-lookup"><span data-stu-id="c7c51-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="c7c51-114">会社間計画では、最下位のスケジューリングシーケンスから始まる計画グループにおける会社のマスタープランが実施されます。</span><span class="sxs-lookup"><span data-stu-id="c7c51-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="c7c51-115">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-115">Click Yes.</span></span>
6. <span data-ttu-id="c7c51-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7c51-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="c7c51-117">会社間計画の作成</span><span class="sxs-lookup"><span data-stu-id="c7c51-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="c7c51-118">[会社間マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="c7c51-119">これはマスタープランのワークスペースにあります。</span><span class="sxs-lookup"><span data-stu-id="c7c51-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="c7c51-120">[会社間計画グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c7c51-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c7c51-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7c51-122">会社間計画グループ 10を選択する</span><span class="sxs-lookup"><span data-stu-id="c7c51-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="c7c51-123">[会社間計画の繰り返し回数] フィールドで、「2」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="c7c51-124">会社間計画グループ10にはメンバーが2名います。</span><span class="sxs-lookup"><span data-stu-id="c7c51-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="c7c51-125">顧客の会社 (DEMF) にソースの会社 (USMF) の遅延を反映させるには、両方の会社で会社間計画を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7c51-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="c7c51-126">最初の繰り返しが需要を反映し、ソースの会社 (USMF)の遅延を識別します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="c7c51-127">2番目の繰り返しはUSMFからDEMFへの遅延を反映します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="c7c51-128">[最初の繰り返し] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="c7c51-129">[最初の繰り返し] フィールドで、[再生成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="c7c51-130">[後の繰り返し] フィールドで、[再生成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="c7c51-131">[スレッド数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="c7c51-132">これは、計画に使用される並行スレッドの数を表します。</span><span class="sxs-lookup"><span data-stu-id="c7c51-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="c7c51-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="c7c51-134">計画の結果を表示する</span><span class="sxs-lookup"><span data-stu-id="c7c51-134">View the result of the plan</span></span>
1. <span data-ttu-id="c7c51-135">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c7c51-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c7c51-136">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7c51-137">StaticPlanのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="c7c51-138">会社USMFにいる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7c51-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="c7c51-139">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7c51-139">Click Planned orders.</span></span>

