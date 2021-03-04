---
title: ケース カテゴリ セキュリティの計画、ケース プロセス、およびケース カテゴリ
description: この記事では、ケースをコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CaseCategorySetup, CaseCategoryTypeSecurity
audience: IT Pro
ms.reviewer: sericks
ms.custom: 23581
ms.assetid: 0a1ffae4-5750-46a2-becb-604f7a989d32
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34f0c3780b898e433226266ed9b084021c93f286
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796984"
---
# <a name="plan-case-category-security-case-processes-and-case-categories"></a><span data-ttu-id="03d01-103">ケース カテゴリ セキュリティの計画、ケース プロセス、およびケース カテゴリ</span><span class="sxs-lookup"><span data-stu-id="03d01-103">Plan case category security, case processes, and case categories</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03d01-104">この記事では、ケースをコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="03d01-104">This article describes the considerations and decisions that you must make during the planning process, before you begin to configure cases.</span></span>

<span data-ttu-id="03d01-105">case 機能を使用すると、組織外の問題と内部の問題の両方を解決することができます。</span><span class="sxs-lookup"><span data-stu-id="03d01-105">You can use the case functionality to resolve both issues that are external to your organization and internal issues.</span></span>

## <a name="case-category-security-by-role"></a><span data-ttu-id="03d01-106">ロール別ケース カテゴリ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="03d01-106">Case category security by role</span></span>

<span data-ttu-id="03d01-107">組織内の適切な従業員のみ、ケースと関連情報にアクセスできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d01-107">Only appropriate employees in an organization should have access to cases and related information.</span></span> <span data-ttu-id="03d01-108">異なるタイプのケースを表示、作成、および更新するための従業員によるアクセスを制御するため、ケース カテゴリ タイプにセキュリティ ロールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="03d01-108">To control which employees have access to view, create, and update different types of cases, you can assign security roles to case category types.</span></span> <span data-ttu-id="03d01-109">さまざまなケース カテゴリへアクセスする必要のあるセキュリティ ロールを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d01-109">You must determine which security roles should have access to the various case category types.</span></span>

<span data-ttu-id="03d01-110">**意思決定:** 次のケース カテゴリ タイプにアクセスできるセキュリティ ロールを決定します。</span><span class="sxs-lookup"><span data-stu-id="03d01-110">**Decision:** Determine which security roles should have access to the following case category types.</span></span> <span data-ttu-id="03d01-111">組織はこれらのすべてのカテゴリ タイプを使用しないで、該当するカテゴリに対してのみ決定を行う可能性があります。</span><span class="sxs-lookup"><span data-stu-id="03d01-111">Your organization might not use all these category types, so make decisions only for those categories that are appropriate.</span></span>

- <span data-ttu-id="03d01-112">一般</span><span class="sxs-lookup"><span data-stu-id="03d01-112">General</span></span>
- <span data-ttu-id="03d01-113">売上</span><span class="sxs-lookup"><span data-stu-id="03d01-113">Sales</span></span>
- <span data-ttu-id="03d01-114">購買</span><span class="sxs-lookup"><span data-stu-id="03d01-114">Purchase</span></span>
- <span data-ttu-id="03d01-115">サービス</span><span class="sxs-lookup"><span data-stu-id="03d01-115">Service</span></span>
- <span data-ttu-id="03d01-116">Project</span><span class="sxs-lookup"><span data-stu-id="03d01-116">Project</span></span>
- <span data-ttu-id="03d01-117">実稼働</span><span class="sxs-lookup"><span data-stu-id="03d01-117">Production</span></span>
- <span data-ttu-id="03d01-118">取立</span><span class="sxs-lookup"><span data-stu-id="03d01-118">Collections</span></span>
- <span data-ttu-id="03d01-119">監査</span><span class="sxs-lookup"><span data-stu-id="03d01-119">Audit</span></span>
- <span data-ttu-id="03d01-120">Web</span><span class="sxs-lookup"><span data-stu-id="03d01-120">Web</span></span>
- <span data-ttu-id="03d01-121">人事管理</span><span class="sxs-lookup"><span data-stu-id="03d01-121">Human Resources</span></span>
- <span data-ttu-id="03d01-122">製品の変更</span><span class="sxs-lookup"><span data-stu-id="03d01-122">Product change</span></span>
- <span data-ttu-id="03d01-123">FMLA</span><span class="sxs-lookup"><span data-stu-id="03d01-123">FMLA</span></span>

## <a name="case-processes"></a><span data-ttu-id="03d01-124">ケース プロセス</span><span class="sxs-lookup"><span data-stu-id="03d01-124">Case processes</span></span>

<span data-ttu-id="03d01-125">所属する組織でオープンになっている従業員が従うべきケースにプロセスを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d01-125">You should set up processes that employees must follow for the cases that are opened in your organization.</span></span> <span data-ttu-id="03d01-126">プロセスは、ケースに関係する従業員の一貫性を保証することができ、従業員がケースを迅速かつ効率的に解決できるようにもします。</span><span class="sxs-lookup"><span data-stu-id="03d01-126">Processes help guarantee consistency for the people who are involved in cases, and also help employees resolve cases faster and more efficiently.</span></span> <span data-ttu-id="03d01-127">ケースが割り当てられている各ケース カテゴリのプロセスを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="03d01-127">You can set up a process for each case category that cases are assigned to.</span></span> <span data-ttu-id="03d01-128">ケース タイプごとに個別のプロセスを計画するには時間がかかりますが、プロセスが計画されていれば、ケースの解決はよりスムーズに進んでいきます。</span><span class="sxs-lookup"><span data-stu-id="03d01-128">Although planning a separate process for each case type takes time, case resolution will go much more smoothly if the processes are planned out.</span></span>

<span data-ttu-id="03d01-129">**意思決定:** 各ケース プロセスは次の決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d01-129">**Decisions:** For each case process, you must make the following decisions:</span></span>

- <span data-ttu-id="03d01-130">プロセスの名前と説明とは</span><span class="sxs-lookup"><span data-stu-id="03d01-130">What are the name and description of the process?</span></span>
- <span data-ttu-id="03d01-131">プロセスが有効になっており、従業員がプロセスが割り当てられているケースを処理するときに使用する必要はありますか。</span><span class="sxs-lookup"><span data-stu-id="03d01-131">Is the process active, and should employees use it when they handle a case that the process is assigned to?</span></span>
- <span data-ttu-id="03d01-132">組織内のだれがケースへのプロセスの適用を担当しますか。</span><span class="sxs-lookup"><span data-stu-id="03d01-132">Who in the organization will be responsible for applying the process to a case?</span></span> <span data-ttu-id="03d01-133">たとえば、原価会計または人事管理は、いくつかのケース プロセスを担当する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="03d01-133">For example, Cost accounting or Human resources might be responsible for some case processes.</span></span> <span data-ttu-id="03d01-134">複数の領域が 1 つのプロセスの完了の責任を担っていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="03d01-134">Note that multiple areas can be responsible for completing one process.</span></span>

## <a name="case-categories"></a><span data-ttu-id="03d01-135">ケース カテゴリ</span><span class="sxs-lookup"><span data-stu-id="03d01-135">Case categories</span></span>

<span data-ttu-id="03d01-136">ケース カテゴリ階層は、ケースを割り当てることができるカテゴリの一覧を提供します (「ロールごとのケース カテゴリ セキュリティ」セクションを参照)。</span><span class="sxs-lookup"><span data-stu-id="03d01-136">The Case category hierarchy provides a list of categories that you can assign cases to (see the "Case category security by role" section).</span></span> <span data-ttu-id="03d01-137">各トップレベル カテゴリには、サブカテゴリが含まれているため、組織で使用されているケースについてより具体的なカテゴリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="03d01-137">Each top-level category includes subcategories, so that you can create more specific categories for the cases that your organization works with.</span></span> <span data-ttu-id="03d01-138">既存のカテゴリおよびサブカテゴリの一覧を確認し、さらに作成する必要があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="03d01-138">Review the list of existing categories and subcategories to determine whether you must create more.</span></span> <span data-ttu-id="03d01-139">カテゴリとサブカテゴリをさらに作成する必要がある場合、追加するたびに、次の決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d01-139">If you must create more categories and subcategories, you must make the following decisions for each addition.</span></span>

<span data-ttu-id="03d01-140">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="03d01-140">**Decisions:**</span></span>

- <span data-ttu-id="03d01-141">新しいトップレベル カテゴリを作成していますか。</span><span class="sxs-lookup"><span data-stu-id="03d01-141">Are you creating a new top-level category?</span></span>

    - <span data-ttu-id="03d01-142">カテゴリの名前とは</span><span class="sxs-lookup"><span data-stu-id="03d01-142">What is the name of the category</span></span>

- <span data-ttu-id="03d01-143">新しいサブカテゴリを作成していますか。</span><span class="sxs-lookup"><span data-stu-id="03d01-143">Are you creating a new subcategory?</span></span>

    - <span data-ttu-id="03d01-144">サブカテゴリの親カテゴリは何ですか ?</span><span class="sxs-lookup"><span data-stu-id="03d01-144">What is the parent category of the subcategory?</span></span>
    - <span data-ttu-id="03d01-145">サブカテゴリの名前は何ですか ?</span><span class="sxs-lookup"><span data-stu-id="03d01-145">What is the name of the subcategory?</span></span>
    - <span data-ttu-id="03d01-146">どの作業者がサブカテゴリを所有しますか。</span><span class="sxs-lookup"><span data-stu-id="03d01-146">Which worker will own the subcategory?</span></span>
    - <span data-ttu-id="03d01-147">どのような部門にサブカテゴリが割り当てられていますか ?</span><span class="sxs-lookup"><span data-stu-id="03d01-147">What department is the subcategory assigned to?</span></span>
    - <span data-ttu-id="03d01-148">どのようなケース プロセスをこのサブカテゴリに割り当てられますか ?</span><span class="sxs-lookup"><span data-stu-id="03d01-148">What case process will be assigned to this subcategory?</span></span>
    - <span data-ttu-id="03d01-149">このサブカテゴリに割り当てられている既定のサービス レベル アグリーメント (SLA) は何ですか ?</span><span class="sxs-lookup"><span data-stu-id="03d01-149">What is the default service level agreement (SLA) that is assigned to this subcategory?</span></span>
    - <span data-ttu-id="03d01-150">このサブカテゴリが割り当てられているケースが開いているときに、活動を作成する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="03d01-150">Should an activity be created when a case that this subcategory is assigned to is opened?</span></span>
    - <span data-ttu-id="03d01-151">その場合は、活動のカテゴリ、タイプ、目的、およびフェーズは何でしょうか?</span><span class="sxs-lookup"><span data-stu-id="03d01-151">If so, what are the activity category, type, purpose, and phase?</span></span>
    - <span data-ttu-id="03d01-152">ケースのフォロー アップ活動を作成する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="03d01-152">Should a follow-up activity for the case be created?</span></span>
    - <span data-ttu-id="03d01-153">その場合は、フォローアップ活動のカテゴリ、タイプ、目的、およびフェーズは何でしょうか?</span><span class="sxs-lookup"><span data-stu-id="03d01-153">If so, what are the follow-up activity category, type, purpose, and phase?</span></span>
