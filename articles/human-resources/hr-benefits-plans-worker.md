---
title: 作業者の給付金プランの作成
description: Microsoft Dynamics 365 Human Resources で作業者の給付金プランを作成して、従業員の給付金プランを選択および給付金プランの選択を確認することができます。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 45b9a669d63620a15e6dc8047fed24c2db64438f
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230042"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="b397a-103">作業者の給付金プランの作成</span><span class="sxs-lookup"><span data-stu-id="b397a-103">Create worker benefit plans</span></span>

<span data-ttu-id="b397a-104">Microsoft Dynamics 365 Human Resources で作業者の給付金プランを作成して、従業員の給付金プランを選択および給付金プランの選択を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="b397a-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="b397a-105">通常、従業員は従業員のセルフ サービスを使用して給付金プランを選択し、給付金プランの管理者はその選択を確認します。</span><span class="sxs-lookup"><span data-stu-id="b397a-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="b397a-106">**給付金管理**ワーク スペースの**プラン**で、**作業者の給付金プラン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b397a-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="b397a-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b397a-107">Select **New**.</span></span>

3. <span data-ttu-id="b397a-108">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b397a-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b397a-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="b397a-109">Field</span></span> | <span data-ttu-id="b397a-110">説明</span><span class="sxs-lookup"><span data-stu-id="b397a-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b397a-111">期間</span><span class="sxs-lookup"><span data-stu-id="b397a-111">Period</span></span> | <span data-ttu-id="b397a-112">プラン クイック タブでプランをフィルタ処理するために使用する給付金期間を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="b397a-113">たとえば、2015 という名前で作成した期間を選択して、2015 に対して給付金登録のすべての選択を確認します。</span><span class="sxs-lookup"><span data-stu-id="b397a-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="b397a-114">ワーカー</span><span class="sxs-lookup"><span data-stu-id="b397a-114">Worker</span></span> | <span data-ttu-id="b397a-115">プラン クイック タブでプランをフィルター処理するために使用する作業者を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="b397a-116">法人エンティティ</span><span class="sxs-lookup"><span data-stu-id="b397a-116">Legal entity</span></span> | <span data-ttu-id="b397a-117">プラン クイック タブでプランをフィルター処理するために使用する法人を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="b397a-118">補償オプション</span><span class="sxs-lookup"><span data-stu-id="b397a-118">Coverage option</span></span> | <span data-ttu-id="b397a-119">プラン クイック タブでプランをフィルタ処理するために使用する補償オプションを指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="b397a-120">既定</span><span class="sxs-lookup"><span data-stu-id="b397a-120">Default</span></span> | <span data-ttu-id="b397a-121">既定のプランであるかどうかに基づいて、給付金プランをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="b397a-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="b397a-122">プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="b397a-123">ステータス</span><span class="sxs-lookup"><span data-stu-id="b397a-123">Status</span></span> | <span data-ttu-id="b397a-124">それらの状態に基づいて、給付金プランをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="b397a-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="b397a-125">プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="b397a-126">確認書</span><span class="sxs-lookup"><span data-stu-id="b397a-126">Confirmation</span></span> | <span data-ttu-id="b397a-127">プラン クイック タブでプランをフィルター処理するために使用する確認状態を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="b397a-128">取消</span><span class="sxs-lookup"><span data-stu-id="b397a-128">Cancellation</span></span> | <span data-ttu-id="b397a-129">プラン クイック タブでプランをフィルター処理するために使用する削除状態を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b397a-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="b397a-130">有効な日付フィルター</span><span class="sxs-lookup"><span data-stu-id="b397a-130">Effective date filter</span></span> | <span data-ttu-id="b397a-131">有効期限が切れているか、有効になっているか、または将来有効になるかに基づいて、プランをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="b397a-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="b397a-132">プラン クイック タブに表示するプランに対応するチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b397a-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="b397a-133">計画</span><span class="sxs-lookup"><span data-stu-id="b397a-133">Plans</span></span> | <span data-ttu-id="b397a-134">プラン クイック タブには、指定したフィルター基準を満たすプランが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b397a-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="b397a-135">HR スタッフによって設定された関連コンフィギュレーション オプションと、従業員によって選択された登録の選択は、各行に含まれています。</span><span class="sxs-lookup"><span data-stu-id="b397a-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="b397a-136">修飾フィールドでは、プランの選択に検証の競合があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b397a-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="b397a-137">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b397a-137">Select **Save**.</span></span>
