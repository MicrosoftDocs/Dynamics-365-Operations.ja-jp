---
title: 交換するかんばんルールの作成
description: この手順では、既存のかんばんルールを特定日付の新しいかんばんルールに置き換えることを対象としています。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae589f81811c1586e0e24de94eaf5f467f19debb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431677"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="1287a-103">交換するかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="1287a-103">Create a replacement kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1287a-104">この手順では、既存のかんばんルールを特定日付の新しいかんばんルールに置き換えることを対象としています。</span><span class="sxs-lookup"><span data-stu-id="1287a-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="1287a-105">これは、生産フローの変更または補充ルールを調整およびスケジューリングする必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1287a-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="1287a-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="1287a-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="1287a-107">この手順は、変更された生産フローまたは新しい補充ルールに対する生産を準備しているプロセス エンジニアまたはバリュー ストリーム マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="1287a-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="1287a-108">このタスクは、新しいルールでかんばんルール 000022 を交換し、新しいルールについて最大数量を 48 から 100 に増加させます。</span><span class="sxs-lookup"><span data-stu-id="1287a-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="1287a-109">置換するかんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="1287a-110">[かんばんルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="1287a-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="1287a-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1287a-112">かんばんルール 000022 を選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="1287a-113">交換するかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="1287a-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="1287a-114">かんばんルールの置換をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1287a-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="1287a-115">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="1287a-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="1287a-116">今から 1 週間など、将来の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="1287a-117">これは、新しいかんばんルールが有効になり、古いかんばんルールを置き換える日付と時刻です。</span><span class="sxs-lookup"><span data-stu-id="1287a-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="1287a-118">かんばんルールが生産フローのパスを変更する場合は、別の活動を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1287a-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="1287a-119">この手順では、活動をそのままの状態にします。</span><span class="sxs-lookup"><span data-stu-id="1287a-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="1287a-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1287a-120">Click OK.</span></span>
    * <span data-ttu-id="1287a-121">新しいかんばんルールを作成すると、かんばんルール 000022 が置換されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1287a-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="1287a-122">有効日は、選択した日付に従ってかんばんルールを置き換える場合に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1287a-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="1287a-123">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1287a-124">置換されたかんばんルール 000022 を選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="1287a-125">置換されたかんばんルールが有効期限と同じ日付をもつと、これが切れる日付であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1287a-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="1287a-126">一覧で行 1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="1287a-127">リストの先頭にある新しいかんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="1287a-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="1287a-128">これは、最大かんばん番号のかんばんルールです。</span><span class="sxs-lookup"><span data-stu-id="1287a-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="1287a-129">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1287a-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1287a-130">かんばんルールを開くには、かんばんルール番号をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1287a-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="1287a-131">交換するかんばんルールの最大数量の変更</span><span class="sxs-lookup"><span data-stu-id="1287a-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="1287a-132">最大数量を「100」に設定します。</span><span class="sxs-lookup"><span data-stu-id="1287a-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="1287a-133">Quantities FastTab を展開して、Maximum quantity field を確認します。</span><span class="sxs-lookup"><span data-stu-id="1287a-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="1287a-134">100 に最大数量を変更すると、100 のかんばんが処理されるようになります。</span><span class="sxs-lookup"><span data-stu-id="1287a-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="1287a-135">これは、このタスクの最後のステップです。</span><span class="sxs-lookup"><span data-stu-id="1287a-135">This is the last step in this task.</span></span>  

