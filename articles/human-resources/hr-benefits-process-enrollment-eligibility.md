---
title: 登録の適格性を処理
description: この記事では、登録資格のプロセスを実行する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfb7f13dce48f33c111af491918702763f7e3b8a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429292"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="00677-103">登録の適格性を処理</span><span class="sxs-lookup"><span data-stu-id="00677-103">Process enrollment eligibility</span></span>

<span data-ttu-id="00677-104">この記事では、登録資格のプロセスを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="00677-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="00677-105">**給付金管理**ワークスペースにて、**処理**の下の**登録適格性の処理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="00677-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="00677-106">**給付金登録の適格性の処理を実行**ダイアログ ボックスで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="00677-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="00677-107">フィールド</span><span class="sxs-lookup"><span data-stu-id="00677-107">Field</span></span> | <span data-ttu-id="00677-108">説明</span><span class="sxs-lookup"><span data-stu-id="00677-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="00677-109">**登録期間**</span><span class="sxs-lookup"><span data-stu-id="00677-109">**Enrollment period**</span></span> | <span data-ttu-id="00677-110">登録適格性を処理する登録期間。</span><span class="sxs-lookup"><span data-stu-id="00677-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="00677-111">**法人エンティティ**</span><span class="sxs-lookup"><span data-stu-id="00677-111">**Legal entity**</span></span> | <span data-ttu-id="00677-112">登録適格性を処理する法人が変更されます。</span><span class="sxs-lookup"><span data-stu-id="00677-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="00677-113">**ワーカー**</span><span class="sxs-lookup"><span data-stu-id="00677-113">**Worker**</span></span> | <span data-ttu-id="00677-114">登録適格性を処理する作業者が変更されます。</span><span class="sxs-lookup"><span data-stu-id="00677-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="00677-115">このフィールドを空白のままにすると、登録適格性がすべての作業者に対して処理されます。</span><span class="sxs-lookup"><span data-stu-id="00677-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="00677-116">**給付金計画**</span><span class="sxs-lookup"><span data-stu-id="00677-116">**Benefit plan**</span></span> | <span data-ttu-id="00677-117">登録適格性を処理する給付金プランが変更されます。</span><span class="sxs-lookup"><span data-stu-id="00677-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="00677-118">バックグラウンドで処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="00677-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="00677-119">処理情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="00677-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="00677-120">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00677-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="00677-121">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00677-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="00677-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00677-122">Select **OK**.</span></span> <span data-ttu-id="00677-123">設定したパラメータで処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="00677-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="00677-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00677-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="00677-125">プロセス結果の表示</span><span class="sxs-lookup"><span data-stu-id="00677-125">View Process Results</span></span>

<span data-ttu-id="00677-126">この記事では、適格性処理の結果を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="00677-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="00677-127">**福利厚生の管理** ワークスペースの **処理中** で **プロセス結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00677-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="00677-128">**プロセス結果** フォームで、次のフィールドが指定されています:</span><span class="sxs-lookup"><span data-stu-id="00677-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="00677-129">フィールド</span><span class="sxs-lookup"><span data-stu-id="00677-129">Field</span></span> | <span data-ttu-id="00677-130">説明</span><span class="sxs-lookup"><span data-stu-id="00677-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="00677-131">**プロセス ID**</span><span class="sxs-lookup"><span data-stu-id="00677-131">**Process ID**</span></span> | <span data-ttu-id="00677-132">従業員、法人、プロセスの実行の組み合わせに対する固有 ID。</span><span class="sxs-lookup"><span data-stu-id="00677-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="00677-133">**プロセスのタイプ**</span><span class="sxs-lookup"><span data-stu-id="00677-133">**Process type**</span></span> | <span data-ttu-id="00677-134">これにより、実行されたプロセスが識別されます。</span><span class="sxs-lookup"><span data-stu-id="00677-134">This identifies the process that was run.</span></span> <span data-ttu-id="00677-135">例: 登録。</span><span class="sxs-lookup"><span data-stu-id="00677-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="00677-136">**タイム スタンプ**</span><span class="sxs-lookup"><span data-stu-id="00677-136">**Time stamp**</span></span> | <span data-ttu-id="00677-137">適格性処理が実行された時刻。</span><span class="sxs-lookup"><span data-stu-id="00677-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="00677-138">**個法**</span><span class="sxs-lookup"><span data-stu-id="00677-138">**Legal entity**</span></span> | <span data-ttu-id="00677-139">登録プロセス中に指定された法人。</span><span class="sxs-lookup"><span data-stu-id="00677-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="00677-140">**ワーカー**</span><span class="sxs-lookup"><span data-stu-id="00677-140">**Worker**</span></span> | <span data-ttu-id="00677-141">処理された従業員。</span><span class="sxs-lookup"><span data-stu-id="00677-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="00677-142">\*\*計画</span><span class="sxs-lookup"><span data-stu-id="00677-142">\*\*Plan</span></span> | <span data-ttu-id="00677-143">登録が試行された福利厚生計画。</span><span class="sxs-lookup"><span data-stu-id="00677-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="00677-144">**適格性ルール**</span><span class="sxs-lookup"><span data-stu-id="00677-144">**Eligibility rule**</span></span> | <span data-ttu-id="00677-145">処理された適格性ルール。</span><span class="sxs-lookup"><span data-stu-id="00677-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="00677-146">適格性が実行される前にエラーが発生した場合、これは空白になります。</span><span class="sxs-lookup"><span data-stu-id="00677-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="00677-147">例: 報酬が従業員に対して定義されていない場合、適格性プロセスは実行されず、このフィールドは空白のままになります。</span><span class="sxs-lookup"><span data-stu-id="00677-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="00677-148">**結果状態**</span><span class="sxs-lookup"><span data-stu-id="00677-148">**Result status**</span></span> | <span data-ttu-id="00677-149">これは、適格または不適格です。</span><span class="sxs-lookup"><span data-stu-id="00677-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="00677-150">従業員が適格性ルールの基準を満たしていない場合、従業員が支払頻度や固定報酬などの必要な情報を欠落している場合、または、従業員の登録をさまたげる福利厚生計画の情報が欠落している場合、結果の状態は不適格になります。</span><span class="sxs-lookup"><span data-stu-id="00677-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="00677-151">**結果メッセージ**</span><span class="sxs-lookup"><span data-stu-id="00677-151">**Result message**</span></span> | <span data-ttu-id="00677-152">従業員が福利厚生計画に不適格である理由、または適格性ルールに合格したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="00677-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

