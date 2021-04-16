---
title: 特別償却
description: この記事は、特別償却機能の概要を示します。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f811b913f751a860c21fc120b15bac406281d7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827029"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="b7aac-103">特別償却</span><span class="sxs-lookup"><span data-stu-id="b7aac-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7aac-104">この記事は、特別償却機能の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="b7aac-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="b7aac-105">特別減価償却に関しては、資産を利用し始め、償却を開始した最初の年に追加の減価償却額または特別減価償却額を適用できます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="b7aac-106">特別減価償却は、他の減価償却計算の前に実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7aac-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="b7aac-107">したがって、総勘定元帳の機能への転記が無効となった帳簿との特別償却の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b7aac-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="b7aac-108">**総勘定元帳に転記されないトランザクションの削除** オプションを使用して、総勘定元帳に転記しない帳簿のトランザクション履歴を削除できます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="b7aac-109">それから以前に転記された減価償却トランザクションを消去することにより、特別減価償却トランザクションに対応できます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="b7aac-110">提案プロセスを使用して特別償却を計算することも、手動特別償却トランザクションを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="b7aac-111">該当する固定資産帳簿に対し、減価償却トランザクションまたは減価償却調整トランザクションが存在する場合には、特別償却トランザクションは作成できません。</span><span class="sxs-lookup"><span data-stu-id="b7aac-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="b7aac-112">特別償却の計算に提案プロセスを使用すると、既存のすべての特別償却トランザクションに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="b7aac-113">この計算には、資産に対して手動で入力する以前の特別減価償却も含まれます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="b7aac-114">資産に適用される特別減価償却が複数ある場合には、優先順位が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="b7aac-115">特別償却はそれぞれ次の特別償却の資産基準を低下させます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="b7aac-116">救済価格は特別償却計算の資産基準と見なされず、特別償却には減価償却方法が適用されません。</span><span class="sxs-lookup"><span data-stu-id="b7aac-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="b7aac-117">現在米国では、いくつかの資産がセクション 179 資産とみなされます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="b7aac-118">セクション 179 控除を使用して、上限までいくつかの資産の原価の全体または一部を回収できます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="b7aac-119">資産の供用年度の控除によって、コストを回収できます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="b7aac-120">例</span><span class="sxs-lookup"><span data-stu-id="b7aac-120">Example</span></span>
<span data-ttu-id="b7aac-121">次の特別償却は固定資産却簿に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="b7aac-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="b7aac-122">**セクション 179:** 1,000.00、優先順位 1</span><span class="sxs-lookup"><span data-stu-id="b7aac-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="b7aac-123">**リバティ ゾーン:** 30%、優先順位 2</span><span class="sxs-lookup"><span data-stu-id="b7aac-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="b7aac-124">固定資産取得原価は 5,000.00 です。</span><span class="sxs-lookup"><span data-stu-id="b7aac-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="b7aac-125">特別減価償却を計算した場合、セクション 179 控除に対する最初の特別償却額は $1,000,00 となります。</span><span class="sxs-lookup"><span data-stu-id="b7aac-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="b7aac-126">次のリバティ ゾーン控除に対する特別減価償却額は、次の計算結果を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="b7aac-127">取得原価 : $1,000 (セクション 179 控除) x 30% = $1,200</span><span class="sxs-lookup"><span data-stu-id="b7aac-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="b7aac-128">特別償却額が残存取得原価より大きい場合、特別償却額は、特別償却計算額または残存取得原価のうち小さい方です。</span><span class="sxs-lookup"><span data-stu-id="b7aac-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="b7aac-129">残存取得原価がゼロまたはマイナスの場合、特別償却トランザクションは生成されません。</span><span class="sxs-lookup"><span data-stu-id="b7aac-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="b7aac-130">提案プロセスを使用して特別償却を計算する場合は、固定資産帳簿に関連付けられた適用可能なすべての特別償却レコードに対して特別償却トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="b7aac-131">特別償却レコードは無数に作成できます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="b7aac-132">固定資産グループ帳簿にこのレコードを割り当てた後、これらは固定資産帳簿に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="b7aac-133">特別償却はパーセンテージまたは固定金額として入力します。</span><span class="sxs-lookup"><span data-stu-id="b7aac-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="b7aac-134">減価償却提案を転記すると、特別償却トランザクションが、減価償却トランザクションとは別のトランザクションとして、減価償却簿に転記されます。</span><span class="sxs-lookup"><span data-stu-id="b7aac-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]