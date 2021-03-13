---
title: 作業者の福利厚生の登録および削除
description: この手順では、1 人の作業者が 1 つ以上の福利厚生に登録する方法、および複数の作業者が 1 つの福利厚生に登録する方法を示します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 13e32c9bc77470d6b8e157e7a7805d3d72850478
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113226"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="b0209-103">作業者の福利厚生の登録および削除</span><span class="sxs-lookup"><span data-stu-id="b0209-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="b0209-104">この手順では、1 人の作業者が 1 つ以上の福利厚生に登録する方法、および複数の作業者が 1 つの福利厚生に登録する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b0209-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="b0209-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b0209-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="b0209-106">福利厚生に単一の作業者を登録</span><span class="sxs-lookup"><span data-stu-id="b0209-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="b0209-107">[人事管理] > [作業者] > [従業員] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0209-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="b0209-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b0209-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0209-109">[福利厚生] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0209-109">Click Benefits.</span></span>
4. <span data-ttu-id="b0209-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0209-110">Click New.</span></span>
5. <span data-ttu-id="b0209-111">[福利厚生] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b0209-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="b0209-112">[適用開始日] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0209-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="b0209-113">[適用終了日] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0209-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="b0209-114">受益者を福利厚生に追加する必要がある場合は、[受益者] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b0209-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="b0209-115">福利厚生に適用可能な場合は、このページから被扶養者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b0209-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="b0209-116">福利厚生の登録詳細の編集、登録の削除をこのページですることもできます。</span><span class="sxs-lookup"><span data-stu-id="b0209-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="b0209-117">福利厚生の登録変更が完了したら、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b0209-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="b0209-118">福利厚生に複数の作業者を登録</span><span class="sxs-lookup"><span data-stu-id="b0209-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="b0209-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b0209-119">Close the page.</span></span>
2. <span data-ttu-id="b0209-120">[人事管理] > [作業者] > [従業員] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0209-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="b0209-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b0209-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b0209-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b0209-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b0209-123">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b0209-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b0209-124">[福利厚生への登録] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0209-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="b0209-125">[福利厚生] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b0209-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="b0209-126">[適用開始日] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0209-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="b0209-127">[適用終了日] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0209-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="b0209-128">[登録] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0209-128">Click Enroll.</span></span>
11. <span data-ttu-id="b0209-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b0209-129">Close the page.</span></span>
12. <span data-ttu-id="b0209-130">[人事管理] > [福利厚生] > [登録] > [福利厚生の登録結果] に移動</span><span class="sxs-lookup"><span data-stu-id="b0209-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="b0209-131">探している福利厚生の結果のレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="b0209-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="b0209-132">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0209-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="b0209-133">このページは、福利厚生に登録された従業員と、登録されていない従業員を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b0209-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

