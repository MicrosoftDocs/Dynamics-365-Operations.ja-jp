--- 
title: "プロセス ジョブのかんばんルールの変更"
description: "この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。"
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="44e18-103">プロセス ジョブのかんばんルールの変更</span><span class="sxs-lookup"><span data-stu-id="44e18-103">Change kanban rules for a process job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44e18-104">この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。</span><span class="sxs-lookup"><span data-stu-id="44e18-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="44e18-105">これは負荷リソースのレベルに、または故障の場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="44e18-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="44e18-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="44e18-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="44e18-107">この手順は、リーン生産会社で働いていて、バリュー ストリームを担当するプランナーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="44e18-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="44e18-108">かんばんルールのコピー</span><span class="sxs-lookup"><span data-stu-id="44e18-108">Copy kanban rule</span></span>
1. <span data-ttu-id="44e18-109">[かんばんルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="44e18-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="44e18-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="44e18-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="44e18-111">L0001 のイベントかんばんルール 000022 を選択します。</span><span class="sxs-lookup"><span data-stu-id="44e18-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="44e18-112">[かんばんルールの複製] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44e18-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="44e18-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44e18-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="44e18-114">かんばんルールの変更</span><span class="sxs-lookup"><span data-stu-id="44e18-114">Change kanban rule</span></span>
1. <span data-ttu-id="44e18-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="44e18-115">Close the page.</span></span>
2. <span data-ttu-id="44e18-116">[かんばん作業のスケジューリング] に移動する。</span><span class="sxs-lookup"><span data-stu-id="44e18-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="44e18-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="44e18-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="44e18-118">かんばん 000177 の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="44e18-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="44e18-119">[代替かんばんルールの使用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44e18-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="44e18-120">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44e18-120">Click Next.</span></span>
6. <span data-ttu-id="44e18-121">[かんばんルール] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="44e18-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="44e18-122">先に作成されたかんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="44e18-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="44e18-123">これは、最大数のかんばんルールです。</span><span class="sxs-lookup"><span data-stu-id="44e18-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="44e18-124">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44e18-124">Click Finish.</span></span>
    * <span data-ttu-id="44e18-125">ここでは、かんばん作業は別のかんばんルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="44e18-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="44e18-126">これは負荷の作業セルのレベルに有用です。</span><span class="sxs-lookup"><span data-stu-id="44e18-126">This can be useful to level load work cells.</span></span>  


