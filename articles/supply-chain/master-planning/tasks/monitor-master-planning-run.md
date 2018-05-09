--- 
title: "マスター プランの実行の監視"
description: "生産計画担当者は、マスター プランの実行中であるかどうかを確認します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 550e2de01187d889ef968a4ff6828f93bb44a8a1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="7d70d-103">マスター プランの実行の監視</span><span class="sxs-lookup"><span data-stu-id="7d70d-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d70d-104">生産計画担当者は、マスター プランの実行中であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="7d70d-105">この手順を完了するのにデモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="7d70d-106">マスター プランの実行</span><span class="sxs-lookup"><span data-stu-id="7d70d-106">Run master planning</span></span>
1. <span data-ttu-id="7d70d-107">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-107">Click Master planning.</span></span>
    * <span data-ttu-id="7d70d-108">既定のダッシュボードでこれが見つかります。</span><span class="sxs-lookup"><span data-stu-id="7d70d-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="7d70d-109">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="7d70d-110">例: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="7d70d-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="7d70d-111">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-111">Click Run.</span></span>
4. <span data-ttu-id="7d70d-112">[処理時間の追跡] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="7d70d-113">そのフィールドがすでに選択されている場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="7d70d-114">[スレッド数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="7d70d-115">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="7d70d-116">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-116">Click Filter.</span></span>
8. <span data-ttu-id="7d70d-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7d70d-118">フィールド = 品目番号の行をマークします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="7d70d-119">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="7d70d-120">例: T0001</span><span class="sxs-lookup"><span data-stu-id="7d70d-120">Example: T0001</span></span>  
10. <span data-ttu-id="7d70d-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-121">Click OK.</span></span>
11. <span data-ttu-id="7d70d-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="7d70d-123">マスター プランの実行の監視</span><span class="sxs-lookup"><span data-stu-id="7d70d-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="7d70d-124">[履歴] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-124">Click History.</span></span>
2. <span data-ttu-id="7d70d-125">[照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-125">Click Inquiries.</span></span>
3. <span data-ttu-id="7d70d-126">[プロセス タスク期間] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d70d-126">Click Process task duration.</span></span>
4. <span data-ttu-id="7d70d-127">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7d70d-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7d70d-128">各品目に対して、各計画ステップを完了するためにかかった期間の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="7d70d-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


