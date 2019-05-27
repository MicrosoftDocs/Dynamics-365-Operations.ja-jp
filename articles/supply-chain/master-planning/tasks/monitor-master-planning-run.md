---
title: マスター プランの実行の監視
description: 生産計画担当者は、マスター プランの実行中であるかどうかを確認します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565615"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="48bff-103">マスター プランの実行の監視</span><span class="sxs-lookup"><span data-stu-id="48bff-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48bff-104">生産計画担当者は、マスター プランの実行中であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="48bff-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="48bff-105">この手順を完了するのにデモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="48bff-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="48bff-106">マスター プランの実行</span><span class="sxs-lookup"><span data-stu-id="48bff-106">Run master planning</span></span>
1. <span data-ttu-id="48bff-107">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-107">Click Master planning.</span></span>
    * <span data-ttu-id="48bff-108">既定のダッシュボードでこれが見つかります。</span><span class="sxs-lookup"><span data-stu-id="48bff-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="48bff-109">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="48bff-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="48bff-110">例: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="48bff-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="48bff-111">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-111">Click Run.</span></span>
4. <span data-ttu-id="48bff-112">[処理時間の追跡] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="48bff-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="48bff-113">そのフィールドがすでに選択されている場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="48bff-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="48bff-114">[スレッド数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48bff-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="48bff-115">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="48bff-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="48bff-116">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-116">Click Filter.</span></span>
8. <span data-ttu-id="48bff-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="48bff-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="48bff-118">フィールド = 品目番号の行をマークします。</span><span class="sxs-lookup"><span data-stu-id="48bff-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="48bff-119">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="48bff-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="48bff-120">例: T0001</span><span class="sxs-lookup"><span data-stu-id="48bff-120">Example: T0001</span></span>  
10. <span data-ttu-id="48bff-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-121">Click OK.</span></span>
11. <span data-ttu-id="48bff-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="48bff-123">マスター プランの実行の監視</span><span class="sxs-lookup"><span data-stu-id="48bff-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="48bff-124">[履歴] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-124">Click History.</span></span>
2. <span data-ttu-id="48bff-125">[照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-125">Click Inquiries.</span></span>
3. <span data-ttu-id="48bff-126">[プロセス タスク期間] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48bff-126">Click Process task duration.</span></span>
4. <span data-ttu-id="48bff-127">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="48bff-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48bff-128">各品目に対して、各計画ステップを完了するためにかかった期間の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="48bff-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

