--- 
title: "RFQ の入札タイプとスコア基準の作成"
description: "このガイドでは、入札タイプの作成、および入札タイプにスコア方法を関連付ける方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 095855d552d228375635bdbaa9fca37c47a3b952
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="f6fd0-103">RFQ の入札タイプとスコア基準の作成</span><span class="sxs-lookup"><span data-stu-id="f6fd0-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6fd0-104">このガイドでは、入札タイプの作成、および入札タイプにスコア方法を関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="f6fd0-105">さらに見積依頼 (RFQ) で入札タイプを使用し、既定のスコア方法を設定する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="f6fd0-106">通常、これらのタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="f6fd0-107">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f6fd0-108">開始する前に、使用可能なスコア方法を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="f6fd0-109">入札タイプの作成</span><span class="sxs-lookup"><span data-stu-id="f6fd0-109">Create a solicitation type</span></span>
1. <span data-ttu-id="f6fd0-110">[調達] > [設定] > [見積依頼] > [入札タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="f6fd0-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-111">Click New.</span></span>
3. <span data-ttu-id="f6fd0-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f6fd0-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f6fd0-114">[スコア方法] フィールドで、この入札タイプに使用するスコア方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="f6fd0-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-115">Click Save.</span></span>
7. <span data-ttu-id="f6fd0-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="f6fd0-117">入札タイプの使用</span><span class="sxs-lookup"><span data-stu-id="f6fd0-117">Use the solicitation type</span></span>
1. <span data-ttu-id="f6fd0-118">[調達] > [見積依頼] > [すべての見積依頼] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="f6fd0-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-119">Click New.</span></span>
3. <span data-ttu-id="f6fd0-120">[入札タイプ] フィールドで、作成した入札タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
4. <span data-ttu-id="f6fd0-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-121">Click OK.</span></span>
5. <span data-ttu-id="f6fd0-122">[スコア基準] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="f6fd0-123">表示されるスコア基準は、入札タイプに関連付けたスコア方法からなる基準です。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="f6fd0-124">このページで基準を追加、または削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="f6fd0-125">他のスコア方法から新しい基準をコピーして追加することも可能です。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="f6fd0-126">[コピー基準] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="f6fd0-127">[スコア基準] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="f6fd0-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-128">Click OK.</span></span>
9. <span data-ttu-id="f6fd0-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f6fd0-129">Close the page.</span></span>

