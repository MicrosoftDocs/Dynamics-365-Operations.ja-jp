---
title: 与信および回収の概要
description: このトピックでは、与信および回収の機能の概要を示します。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a822e5f5a6cb71a0234b1776211788578470b0bb
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124303"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="dce2c-103">与信および回収の概要</span><span class="sxs-lookup"><span data-stu-id="dce2c-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dce2c-104">顧客の与信限度額を管理し、必要に応じて回収活動を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="dce2c-105">与信の管理</span><span class="sxs-lookup"><span data-stu-id="dce2c-105">Credit management</span></span>

<span data-ttu-id="dce2c-106">顧客の与信管理では、作成した与信ルールに基づいて、転記プロセスを通じて与信限度額の管理と販売注文のフロー制御を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="dce2c-107">与信管理プロセスには、次の手順のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="dce2c-108">顧客の与信属性を更新して、顧客の与信価値に関する追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="dce2c-109">与信限度額調整を使用して、顧客の与信限度額を作成します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="dce2c-110">与信限度額調整を使用して、顧客の一時的な与信限度額を作成します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="dce2c-111">このように、業務上の要件に基づいて、顧客の与信限度額を一時的に増減することができます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="dce2c-112">保険や保証に関する情報など、与信限度額に影響を与える可能性のある情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="dce2c-113">顧客間をリンクして 1 つの与信限度額を共有する顧客の与信グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="dce2c-114">顧客にリスク スコアを割り当てた後、スコアを使用して、与信限度額調整を通じて顧客の与信限度額を自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="dce2c-115">リスク、支払条件、与信限度額、期限切れ金額、使用された与信限度額の割合などの要因に基づいて、1 つ以上の転記プロセス中に注文を保留するブロック ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="dce2c-116">保留中の販売注文の一覧を管理し、保留の理由を確認して、問題を軽減します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="dce2c-117">販売注文をリリースして、転記プロセスを続けます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="dce2c-118">与信限度額の変更と販売注文リリースの承認を管理するためのワークフローを設定します。</span><span class="sxs-lookup"><span data-stu-id="dce2c-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="dce2c-119">回収管理</span><span class="sxs-lookup"><span data-stu-id="dce2c-119">Collections management</span></span>

<span data-ttu-id="dce2c-120">**回収**ページでは、売掛金勘定回収情報が管理される一元的な表示が提供されます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="dce2c-121">回収マネージャーは、この一元的な表示を使用して回収を管理できます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="dce2c-122">回収代行業者は、定義済の回収基準を使用して生成された顧客リスト、または**顧客**ページから回収プロセスを開始できます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="dce2c-123">回収を設定または作業を開始する前に、次の概念を理解する必要があります:</span><span class="sxs-lookup"><span data-stu-id="dce2c-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="dce2c-124">顧客エイジング スナップショットには、特定の時点でのエイジングした残高の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="dce2c-125">回収の顧客プールを使用して、作業を整理することができます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="dce2c-126">回収代行業者は、独自の顧客プールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="dce2c-127">リスト ページには、回収の顧客、活動、およびケースが記載されます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="dce2c-128">顧客の回収情報はすべて、1 つのページにまとめられ、そのページからアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="dce2c-129">1 つのステップで、利息や手数料を免除、再開、または取消をすることができます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="dce2c-130">1 つのステップで、損金処理トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="dce2c-131">1 つのステップで、預金不足 (NSF) の支払を処理できます。</span><span class="sxs-lookup"><span data-stu-id="dce2c-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="dce2c-132">これらの概念の詳細については、[回収管理の主要概念](./cm-collections-concepts.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dce2c-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dce2c-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="dce2c-133">Additional resources</span></span>

[<span data-ttu-id="dce2c-134">顧客与信管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="dce2c-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="dce2c-135">顧客与信管理の設定情報</span><span class="sxs-lookup"><span data-stu-id="dce2c-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="dce2c-136">顧客の与信管理情報の追加</span><span class="sxs-lookup"><span data-stu-id="dce2c-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="dce2c-137">顧客の与信グループ</span><span class="sxs-lookup"><span data-stu-id="dce2c-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="dce2c-138">顧客の与信限度額調整</span><span class="sxs-lookup"><span data-stu-id="dce2c-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="dce2c-139">販売注文の与信保留</span><span class="sxs-lookup"><span data-stu-id="dce2c-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="dce2c-140">顧客与信管理の定期処理タスク</span><span class="sxs-lookup"><span data-stu-id="dce2c-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)
