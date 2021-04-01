---
title: 生産フロー バージョンの作成
description: この手順は、生産フローの新規バージョンに焦点を当てています。
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b57dbd2516a25b414193ca76367bd8d5c4a1b298
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255064"
---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="6b4ba-103">生産フロー バージョンの作成</span><span class="sxs-lookup"><span data-stu-id="6b4ba-103">Create a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b4ba-104">この手順は、生産フローの新規バージョンに焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="6b4ba-105">この手順では、リーン生産の生産パラメータおよびクラス時間の測定単位を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="6b4ba-106">また、バリュー ストリームと生産グループを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="6b4ba-107">生産フローおよびリーン生産の活動に関する詳細については、Microsoft Dynamics AX のリーン生産に関するホワイト ペーパーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="6b4ba-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="6b4ba-109">生産フローの作成</span><span class="sxs-lookup"><span data-stu-id="6b4ba-109">Create a production flow</span></span>
1. <span data-ttu-id="6b4ba-110">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="6b4ba-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-111">Click New.</span></span>
3. <span data-ttu-id="6b4ba-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6b4ba-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6b4ba-114">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6b4ba-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6b4ba-116">タイプ バリュー ストリームの作業単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="6b4ba-117">バリュー ストリームは、バリュー ストリームのすべての活動とフローを対象とする作業単位です。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="6b4ba-118">このステージでは、作業単位は法人に限定され、その以外の機能はありません。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="6b4ba-119">[生産グループ] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6b4ba-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6b4ba-121">生産フローの生産グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-121">Select a production group for the production flow.</span></span> <span data-ttu-id="6b4ba-122">生産グループにより、生産プロセスの材料、労務、および仕掛品勘定を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="6b4ba-123">生産フローに会計のコンテキストを関連付ける際には、生産グループを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="6b4ba-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="6b4ba-125">生産フロー バージョンの作成</span><span class="sxs-lookup"><span data-stu-id="6b4ba-125">Create a production flow version</span></span>
1. <span data-ttu-id="6b4ba-126">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-126">Click Add.</span></span>
2. <span data-ttu-id="6b4ba-127">[有効期限] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="6b4ba-128">必要に応じて、バージョンの [有効期限] を定義します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="6b4ba-129">有効なバージョンであっても、随時更新できます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="6b4ba-130">バージョンの段階的な撤去の計画に使用できます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="6b4ba-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-131">Click OK.</span></span>
4. <span data-ttu-id="6b4ba-132">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="6b4ba-133">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="6b4ba-134">[タクト単位の変更] を解決します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="6b4ba-135">[平均タクト タイム] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="6b4ba-136">バージョンの [平均タクト タイム] を定義します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="6b4ba-137">生産フロー バージョンのタクト コントロールに対して、対象となる平均タクト タイムを定義します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="6b4ba-138">タクトは期間ごとの数量として定義されます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="6b4ba-139">この例では、タクト タイムは 10 個につき 0.2 時間です。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="6b4ba-140">8 時間の作業時間の場合、これは毎日 400 個の処理能力に相当します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="6b4ba-141">[サイクルあたりの数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="6b4ba-142">[平均タクト タイム] に関連するサイクルあたりの数量を定義します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="6b4ba-143">[バージョンの詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="6b4ba-144">[最小タクト タイム] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="6b4ba-145">最小タクト タイムを定義します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-145">Define the minimum takt time.</span></span> <span data-ttu-id="6b4ba-146">最小タクト タイムは平均タクト タイム以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="6b4ba-147">[最大タクト タイム] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="6b4ba-148">最大タクト タイムは [平均タクト タイム] 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="6b4ba-149">[実際のサイクル時間 (日) の期間] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="6b4ba-150">[実際のサイクル時間の期間] に日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="6b4ba-151">実際のサイクル時間の期間は、実際のサイクル時間を計算するために実際の分数を遡って集計されるジョブの日数です。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="6b4ba-152">価は随時変更することができ、実際のサイクル時間の計算にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="6b4ba-153">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b4ba-153">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]