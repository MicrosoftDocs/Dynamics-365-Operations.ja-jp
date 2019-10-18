---
title: Dynamics 365 Talent - Core HR (2018 年 9 月 10 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 59cb0203422b7d81b5ca0077370fd9cbdb4a7f89
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010087"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-september-10-2018"></a><span data-ttu-id="49a8b-103">Dynamics 365 Talent: Core HR (2018 年 9 月 10 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="49a8b-103">What's new or changed in Dynamics 365 Talent: Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49a8b-104">**ビルド 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="49a8b-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="49a8b-105">このトピックでは、Microsoft Dynamics 365 Talent: Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="49a8b-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="49a8b-106">休暇申請で特定の時刻を許可 (半日数)</span><span class="sxs-lookup"><span data-stu-id="49a8b-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="49a8b-107">休暇を日数で申請できるよう休暇および欠勤を設定する場合、半日の定義も有効化できるようになります。</span><span class="sxs-lookup"><span data-stu-id="49a8b-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="49a8b-108">その後、ユーザーが休暇申請を送信するときに、一日の前半または後半に休暇申請しているのかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="49a8b-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="49a8b-109">既定では、このオプションは無効になっています。</span><span class="sxs-lookup"><span data-stu-id="49a8b-109">By default, this option is turned off.</span></span> <span data-ttu-id="49a8b-110">一日の前半または後半に休暇申請する従業員については、人事管理パラメータの**休暇と欠勤**区分でこのオプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="49a8b-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="49a8b-111">この機能のセキュリティ権限は、人事管理パラメーターの管理にあります。</span><span class="sxs-lookup"><span data-stu-id="49a8b-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="49a8b-112">休暇と欠勤エントリの検証</span><span class="sxs-lookup"><span data-stu-id="49a8b-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="49a8b-113">休暇の構成方法により、各自の作業日よりも長い休暇申請を送信しようとするする従業員には、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="49a8b-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="49a8b-114">つまり、特定の日に全日以上の休暇を取ろうとすると、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="49a8b-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="49a8b-115">この検証は常に有効になっています。</span><span class="sxs-lookup"><span data-stu-id="49a8b-115">This validation is always turned on.</span></span> <span data-ttu-id="49a8b-116">従業員が定義された日のしきい値を超えるたびに、休暇申請の警告を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="49a8b-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="49a8b-117">ワークフローの条件付きステートメントの追加フィールド</span><span class="sxs-lookup"><span data-stu-id="49a8b-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="49a8b-118">追加のフィールドが、Core HR でいくつかのワークフローの条件付きステートメントおよびプレースホルダーに追加されました。</span><span class="sxs-lookup"><span data-stu-id="49a8b-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="49a8b-119">次のフィールドが、報酬、退職、および移動ワークフローに追加されました。</span><span class="sxs-lookup"><span data-stu-id="49a8b-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="49a8b-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="49a8b-120">EmploymentType</span></span>
- <span data-ttu-id="49a8b-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="49a8b-121">LegalEntity</span></span>
- <span data-ttu-id="49a8b-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="49a8b-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="49a8b-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="49a8b-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="49a8b-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="49a8b-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="49a8b-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="49a8b-125">TransitionDate</span></span>
- <span data-ttu-id="49a8b-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="49a8b-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="49a8b-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="49a8b-127">WorkerStartDate</span></span>
- <span data-ttu-id="49a8b-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="49a8b-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="49a8b-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="49a8b-129">ProbationEndDate</span></span>
- <span data-ttu-id="49a8b-130">配置</span><span class="sxs-lookup"><span data-stu-id="49a8b-130">Position</span></span>
- <span data-ttu-id="49a8b-131">結合</span><span class="sxs-lookup"><span data-stu-id="49a8b-131">Union</span></span>
- <span data-ttu-id="49a8b-132">部門</span><span class="sxs-lookup"><span data-stu-id="49a8b-132">Department</span></span>
- <span data-ttu-id="49a8b-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="49a8b-133">PositionType</span></span>
- <span data-ttu-id="49a8b-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="49a8b-134">CompLocation</span></span>
- <span data-ttu-id="49a8b-135">肩書き</span><span class="sxs-lookup"><span data-stu-id="49a8b-135">Title</span></span>
- <span data-ttu-id="49a8b-136">職務</span><span class="sxs-lookup"><span data-stu-id="49a8b-136">Job</span></span>
- <span data-ttu-id="49a8b-137">JobType</span><span class="sxs-lookup"><span data-stu-id="49a8b-137">JobType</span></span>
- <span data-ttu-id="49a8b-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="49a8b-138">JobFamily</span></span>
- <span data-ttu-id="49a8b-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="49a8b-139">JobFunction</span></span>

<span data-ttu-id="49a8b-140">次のフィールドが職位ワークフローに追加されました。</span><span class="sxs-lookup"><span data-stu-id="49a8b-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="49a8b-141">配置</span><span class="sxs-lookup"><span data-stu-id="49a8b-141">Position</span></span>
- <span data-ttu-id="49a8b-142">結合</span><span class="sxs-lookup"><span data-stu-id="49a8b-142">Union</span></span>
- <span data-ttu-id="49a8b-143">部門</span><span class="sxs-lookup"><span data-stu-id="49a8b-143">Department</span></span>
- <span data-ttu-id="49a8b-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="49a8b-144">PositionType</span></span>
- <span data-ttu-id="49a8b-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="49a8b-145">CompLocation</span></span>
- <span data-ttu-id="49a8b-146">肩書き</span><span class="sxs-lookup"><span data-stu-id="49a8b-146">Title</span></span>
- <span data-ttu-id="49a8b-147">職務</span><span class="sxs-lookup"><span data-stu-id="49a8b-147">Job</span></span>
- <span data-ttu-id="49a8b-148">JobType</span><span class="sxs-lookup"><span data-stu-id="49a8b-148">JobType</span></span>
- <span data-ttu-id="49a8b-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="49a8b-149">JobFamily</span></span>
- <span data-ttu-id="49a8b-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="49a8b-150">JobFunction</span></span>

<span data-ttu-id="49a8b-151">条件付きステートメントおよびプレースホルダーのフィールドは、前述のワークフローのコンフィギュレーションにアクセスできるすべてのユーザーが利用できます。</span><span class="sxs-lookup"><span data-stu-id="49a8b-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="49a8b-152">人事管理から Attract への移動</span><span class="sxs-lookup"><span data-stu-id="49a8b-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="49a8b-153">人事管理では、Attract が設定されていない場合、"ここに表示する情報が見つかりませんでした。" というメッセージを表示する代わりに、**採用候補者**セクションで Attract の使用を開始するようユーザーに指示します。</span><span class="sxs-lookup"><span data-stu-id="49a8b-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="49a8b-154">その他の変更</span><span class="sxs-lookup"><span data-stu-id="49a8b-154">Other changes</span></span>

<span data-ttu-id="49a8b-155">このリリースには、いくつかの追加のバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="49a8b-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="49a8b-156">契約社員の雇用時には、**報酬**タブは要求/アクション ページで使用できないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="49a8b-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="49a8b-157">退職申請プロセス中には、すべての必須フィールドにデータが入力されるまで続行できません。</span><span class="sxs-lookup"><span data-stu-id="49a8b-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="49a8b-158">人事管理分析上の並べ替え順序と日付表示の問題は、解決されました。</span><span class="sxs-lookup"><span data-stu-id="49a8b-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
