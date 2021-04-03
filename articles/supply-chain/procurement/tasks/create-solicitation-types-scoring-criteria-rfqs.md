---
title: RFQ の入札タイプとスコア基準の作成
description: このガイドでは、入札タイプの作成、および入札タイプにスコア方法を関連付ける方法を示します。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf196711799b78d7f4106b6693127d7f356b1d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262216"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="ff1b1-103">RFQ の入札タイプとスコア基準の作成</span><span class="sxs-lookup"><span data-stu-id="ff1b1-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff1b1-104">このガイドでは、入札タイプの作成、および入札タイプにスコア方法を関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="ff1b1-105">さらに見積依頼 (RFQ) で入札タイプを使用し、既定のスコア方法を設定する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="ff1b1-106">通常、これらのタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="ff1b1-107">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="ff1b1-108">開始する前に、使用可能なスコア方法を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="ff1b1-109">入札タイプの作成</span><span class="sxs-lookup"><span data-stu-id="ff1b1-109">Create a solicitation type</span></span>
1. <span data-ttu-id="ff1b1-110">[調達] > [設定] > [見積依頼] > [入札タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="ff1b1-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-111">Click New.</span></span>
3. <span data-ttu-id="ff1b1-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ff1b1-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ff1b1-114">[スコア方法] フィールドで、この入札タイプに使用するスコア方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="ff1b1-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-115">Click Save.</span></span>
7. <span data-ttu-id="ff1b1-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="ff1b1-117">入札タイプの使用</span><span class="sxs-lookup"><span data-stu-id="ff1b1-117">Use the solicitation type</span></span>
1. <span data-ttu-id="ff1b1-118">[調達] > [見積依頼] > [すべての見積依頼] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="ff1b1-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-119">Click New.</span></span>
3. <span data-ttu-id="ff1b1-120">[入札タイプ] フィールドで、作成した入札タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="ff1b1-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-121">Click OK.</span></span>
5. <span data-ttu-id="ff1b1-122">[スコア基準] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="ff1b1-123">表示されるスコア基準は、入札タイプに関連付けたスコア方法からなる基準です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="ff1b1-124">このページで基準を追加、または削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="ff1b1-125">他のスコア方法から新しい基準をコピーして追加することも可能です。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="ff1b1-126">[コピー基準] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="ff1b1-127">[スコア基準] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="ff1b1-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-128">Click OK.</span></span>
9. <span data-ttu-id="ff1b1-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ff1b1-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]