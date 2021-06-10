---
title: スキルの構成
description: Dynamics 365 Human Resources では作業者のスキルを追跡できます。 また、特定のジョブに必要なスキルを指定できます。
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076562"
---
# <a name="configure-skills"></a><span data-ttu-id="eb641-104">スキルの構成</span><span class="sxs-lookup"><span data-stu-id="eb641-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eb641-105">Dynamics 365 Human Resources では作業者のスキルを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="eb641-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="eb641-106">また、特定のジョブに必要なスキルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="eb641-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="eb641-107">ユーザーが追跡できるスキルの例には次が含まれます:</span><span class="sxs-lookup"><span data-stu-id="eb641-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="eb641-108">監督 : 他の従業員の作業を監督する能力。</span><span class="sxs-lookup"><span data-stu-id="eb641-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="eb641-109">リーダーシップ : 従業員や業務を率いる能力。</span><span class="sxs-lookup"><span data-stu-id="eb641-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="eb641-110">計画 - 先を見通す力、ビジョン ステートメントを形作る力、それをやり遂げる力。</span><span class="sxs-lookup"><span data-stu-id="eb641-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="eb641-111">HTML : HTML コードを記述する能力。</span><span class="sxs-lookup"><span data-stu-id="eb641-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="eb641-112">スキル タイプと評価モデルをまだ設定していない場合は、スキルを作成する前にいくつかを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb641-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="eb641-113">従業員にスキルを入力できるユーザーは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="eb641-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="eb641-114">作業者は従業員セルフサービスでスキルを自分で入力できます。</span><span class="sxs-lookup"><span data-stu-id="eb641-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="eb641-115">これらのスキルには管理者の承認が必要です。</span><span class="sxs-lookup"><span data-stu-id="eb641-115">These skills require manager approval.</span></span>
- <span data-ttu-id="eb641-116">管理者は従業員のスキルを入力できます。</span><span class="sxs-lookup"><span data-stu-id="eb641-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="eb641-117">これらのスキルを自動承認するワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="eb641-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="eb641-118">スキル タイプの作成</span><span class="sxs-lookup"><span data-stu-id="eb641-118">Create a skill type</span></span>

<span data-ttu-id="eb641-119">スキルのタイプは、管理や販売など、個々のスキルに該当するカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="eb641-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="eb641-120">**従業員開発** ワークスペースで、**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="eb641-121">**能力の設定** で 、**スキルのタイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="eb641-122">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-122">Select **New**.</span></span>

4. <span data-ttu-id="eb641-123">次のすべてのフィールドに入力します:</span><span class="sxs-lookup"><span data-stu-id="eb641-123">Complete the following fields:</span></span>

   - <span data-ttu-id="eb641-124">**スキル タイプ** : スキル タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="eb641-125">**説明**: スキル タイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="eb641-126">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="eb641-127">評価モデルの作成</span><span class="sxs-lookup"><span data-stu-id="eb641-127">Create a rating model</span></span>

<span data-ttu-id="eb641-128">評価モデルは、従業員の実際のスキル レベル、達成すべきレベル、あるいは仕事に必要なスキル レベルの評価に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="eb641-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="eb641-129">評価モデルの各レベルに係数が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="eb641-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="eb641-130">**従業員開発** ワークスペースで、**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="eb641-131">**能力の設定** で 、**評価モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="eb641-132">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-132">Select **New**.</span></span>

4. <span data-ttu-id="eb641-133">次のすべてのフィールドに入力します:</span><span class="sxs-lookup"><span data-stu-id="eb641-133">Complete the following fields:</span></span>

   - <span data-ttu-id="eb641-134">**評価**: 評価モデルの名前 (**スキル** など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="eb641-135">**説明**: **スキル評価** など、評価モデルの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="eb641-136">**レベル** セクションで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="eb641-137">追加するレベルごとに、以下のフィールドに入力してください:</span><span class="sxs-lookup"><span data-stu-id="eb641-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="eb641-138">**レベル**: レベルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="eb641-139">**説明**: レベルの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="eb641-140">**係数**: 0 ~ 9 の係数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="eb641-141">係数は、異なる評価モデルを使用するスキルのスコアの正規化に使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb641-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="eb641-142">各レベルには、固有の係数を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb641-142">Each level must have a unique factor.</span></span> <span data-ttu-id="eb641-143">レベルの係数の値が大きいほど、評価モデルで重要になります。</span><span class="sxs-lookup"><span data-stu-id="eb641-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="eb641-144">必要に応じてレベルの追加を続行します。</span><span class="sxs-lookup"><span data-stu-id="eb641-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="eb641-145">評価モデルには、最大 10 個のレベルを入力できます。</span><span class="sxs-lookup"><span data-stu-id="eb641-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="eb641-146">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="eb641-147">スキルの作成</span><span class="sxs-lookup"><span data-stu-id="eb641-147">Create a skill</span></span>

<span data-ttu-id="eb641-148">スキルを割り当てたり、スキル マッピング検索やスキルのプロファイルを作成する前に、**スキル** ページでスキルに関する情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb641-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="eb641-149">各スキルに対して、スキル タイプおよび評価モデルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="eb641-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="eb641-150">**従業員開発** ワークスペースで、**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="eb641-151">**能力の設定** で 、**スキル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="eb641-152">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-152">Select **New**.</span></span>

4. <span data-ttu-id="eb641-153">次のすべてのフィールドに入力します:</span><span class="sxs-lookup"><span data-stu-id="eb641-153">Complete the following fields:</span></span>

   - <span data-ttu-id="eb641-154">**スキル**: スキルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="eb641-155">**説明**: スキルの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb641-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="eb641-156">**評価**: このスキルに使用する評価モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="eb641-157">**スキル タイプ**: スキル タイプのリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="eb641-158">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb641-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb641-159">参照</span><span class="sxs-lookup"><span data-stu-id="eb641-159">See also</span></span>

[<span data-ttu-id="eb641-160">スキルの入力</span><span class="sxs-lookup"><span data-stu-id="eb641-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="eb641-161">スキルのマップ</span><span class="sxs-lookup"><span data-stu-id="eb641-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]