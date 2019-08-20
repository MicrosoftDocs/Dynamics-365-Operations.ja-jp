---
title: 生産フローおよびバージョンの検証
description: この手順では、新しい生産フローとリーン生産の最初のバージョンを作成する方法を示します。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 523f6414ec212aef48eece487f4199ea2cf4b87e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836156"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="a017b-103">生産フローおよびバージョンの検証</span><span class="sxs-lookup"><span data-stu-id="a017b-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a017b-104">この手順では、新しい生産フローとリーン生産の最初のバージョンを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a017b-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="a017b-105">必要条件: リーン生産の生産パラメーターおよびクラス時間の測定単位を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a017b-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="a017b-106">バリュー ストリームと生産グループを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a017b-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="a017b-107">生産フローおよび活動の概念をよく理解するため、リーン生産についてのホワイト ペーパーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a017b-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="a017b-108">この手順では、デモ データの法人 USMF を参照します。</span><span class="sxs-lookup"><span data-stu-id="a017b-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="a017b-109">ただし、法人がリーン生産としてコンフィギュレーションされていると仮定する場合、他の法人を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a017b-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="a017b-110">生産フローの作成</span><span class="sxs-lookup"><span data-stu-id="a017b-110">Create a production flow</span></span>
1. <span data-ttu-id="a017b-111">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a017b-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="a017b-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a017b-112">Click New.</span></span>
3. <span data-ttu-id="a017b-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a017b-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a017b-115">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a017b-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a017b-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a017b-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a017b-117">バリュー ストリームは、バリュー ストリームのすべての活動とフローを対象とする作業単位です。</span><span class="sxs-lookup"><span data-stu-id="a017b-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="a017b-118">このステージでは、作業単位は法人に限定され、その以外の機能はありません。</span><span class="sxs-lookup"><span data-stu-id="a017b-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="a017b-119">[生産グループ] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a017b-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a017b-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a017b-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a017b-121">生産グループにより、生産プロセスの材料、労務、および仕掛品勘定を定義できます。</span><span class="sxs-lookup"><span data-stu-id="a017b-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="a017b-122">生産フローに会計のコンテキストを関連付ける際には、生産グループを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a017b-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="a017b-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a017b-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="a017b-124">生産フロー バージョンの作成</span><span class="sxs-lookup"><span data-stu-id="a017b-124">Create a production flow version</span></span>
1. <span data-ttu-id="a017b-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a017b-125">Click Add.</span></span>
2. <span data-ttu-id="a017b-126">[有効期限] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="a017b-127">有効なバージョンを含め、バージョンの有効期限をいつでも更新できます。</span><span class="sxs-lookup"><span data-stu-id="a017b-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="a017b-128">バージョンの段階的な撤去の計画に、バージョンの有効期限を使用します。</span><span class="sxs-lookup"><span data-stu-id="a017b-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="a017b-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a017b-129">Click OK.</span></span>
4. <span data-ttu-id="a017b-130">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="a017b-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a017b-131">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="a017b-132">タクト単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="a017b-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="a017b-133">[平均タクト タイム] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="a017b-134">生産フロー バージョンのタクト コントロールに対して、対象となる平均タクト タイムを定義します。</span><span class="sxs-lookup"><span data-stu-id="a017b-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="a017b-135">タクトは期間ごとの数量として定義されます。</span><span class="sxs-lookup"><span data-stu-id="a017b-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="a017b-136">この例では、タクト タイムは 10 個につき 0.2 時間です。</span><span class="sxs-lookup"><span data-stu-id="a017b-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="a017b-137">8 時間の作業時間の場合、これは毎日 400 個の処理能力に相当します。</span><span class="sxs-lookup"><span data-stu-id="a017b-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="a017b-138">[サイクルあたりの数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="a017b-139">[バージョンの詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="a017b-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="a017b-140">[最小タクト タイム] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="a017b-141">最小タクト タイムは平均タクト タイム以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a017b-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="a017b-142">[最大タクト タイム] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a017b-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="a017b-143">最大タクト タイムは [平均タクト タイム] 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a017b-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="a017b-144">[実際のサイクル時間の期間] への日数の入力</span><span class="sxs-lookup"><span data-stu-id="a017b-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="a017b-145">実際のサイクル時間の期間は、実際のサイクル時間を計算するために実際の分数を遡って集計されるジョブの日数です。</span><span class="sxs-lookup"><span data-stu-id="a017b-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="a017b-146">価は随時変更することができ、実際のサイクル時間の計算にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a017b-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="a017b-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a017b-147">Click Save.</span></span>

