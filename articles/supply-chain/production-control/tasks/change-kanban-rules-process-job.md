---
title: プロセス ジョブのかんばんルールの変更
description: この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 485afff3747a87a6e36f0249b146a39361d81b23
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147138"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="ac7a3-103">プロセス ジョブのかんばんルールの変更</span><span class="sxs-lookup"><span data-stu-id="ac7a3-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac7a3-104">この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="ac7a3-105">これは負荷リソースのレベルに、または故障の場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="ac7a3-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ac7a3-107">この手順は、リーン生産会社で働いていて、バリュー ストリームを担当するプランナーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="ac7a3-108">かんばんルールのコピー</span><span class="sxs-lookup"><span data-stu-id="ac7a3-108">Copy kanban rule</span></span>
1. <span data-ttu-id="ac7a3-109">[かんばんルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ac7a3-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ac7a3-111">L0001 のイベントかんばんルール 000022 を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="ac7a3-112">[かんばんルールの複製] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="ac7a3-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="ac7a3-114">かんばんルールの変更</span><span class="sxs-lookup"><span data-stu-id="ac7a3-114">Change kanban rule</span></span>
1. <span data-ttu-id="ac7a3-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-115">Close the page.</span></span>
2. <span data-ttu-id="ac7a3-116">[かんばん作業のスケジューリング] に移動する。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="ac7a3-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ac7a3-118">かんばん 000177 の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="ac7a3-119">[代替かんばんルールの使用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="ac7a3-120">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-120">Click Next.</span></span>
6. <span data-ttu-id="ac7a3-121">[かんばんルール] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="ac7a3-122">先に作成されたかんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="ac7a3-123">これは、最大数のかんばんルールです。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="ac7a3-124">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-124">Click Finish.</span></span>
    * <span data-ttu-id="ac7a3-125">ここでは、かんばん作業は別のかんばんルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="ac7a3-126">これは負荷の作業セルのレベルに有用です。</span><span class="sxs-lookup"><span data-stu-id="ac7a3-126">This can be useful to level load work cells.</span></span>  

