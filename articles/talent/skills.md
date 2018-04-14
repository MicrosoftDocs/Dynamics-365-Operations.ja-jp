---
title: "個人スキルと業務ニーズの調整"
description: "作業者、申請者、または連絡担当者がロールを効果的に遂行するために必要なスキルを追跡できます。 また、特定のジョブに必要なスキルを指定できます。"
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3a5b9f98b371dbad9b6b0538e0d9975dc5ed701c
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="b7b5e-104">個人スキルと業務ニーズの調整</span><span class="sxs-lookup"><span data-stu-id="b7b5e-104">Align workforce skills with business needs</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="b7b5e-105">作業者、申請者、または連絡担当者がロールを効果的に遂行するために必要なスキルを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="b7b5e-106">また、特定のジョブに必要なスキルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="b7b5e-107">ユーザーが追跡できるスキルの例は次が含まれます:</span><span class="sxs-lookup"><span data-stu-id="b7b5e-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="b7b5e-108">監督 : 他の従業員の作業を監督する能力。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="b7b5e-109">リーダーシップ : 従業員や業務を率いる能力。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="b7b5e-110">計画 : 先を見通し、その展望を形作り、さらに、それを行動に移す能力。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="b7b5e-111">HTML : HTML コードを記述する能力。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="b7b5e-112">個人またはジョブへのスキル割り当て、スキル マッピング検索の作成、スキル プロファイルの作成の前に、**スキル** ページでスキルに関する情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="b7b5e-113">各スキルに対して、スキル タイプおよび評価モデルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="b7b5e-114">評価モデル</span><span class="sxs-lookup"><span data-stu-id="b7b5e-114">Rating models</span></span>
<span data-ttu-id="b7b5e-115">評価モデルにより、従業員の実際のスキル レベル、達成に必要な作業レベル、ジョブに必要なスキルを評価できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="b7b5e-116">評価モデルには、最大 10 個のレベルを入力できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="b7b5e-117">評価モデルの各レベルに係数が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="b7b5e-118">係数の値は、異なる評価モデルを使用するスキルを正規化するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="b7b5e-119">係数は 0 から 9 までの数値である必要があり、各レベルには固有の係数が必要です。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="b7b5e-120">レベルの係数の値が大きいほど、評価モデルで重要になります。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="b7b5e-121">職務スキルの指定</span><span class="sxs-lookup"><span data-stu-id="b7b5e-121">Specify job skills</span></span>
<span data-ttu-id="b7b5e-122">ジョブに関する情報を入力すると、そのジョブに必要な作業を実行するために従業員が持つべきスキルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="b7b5e-123">また、各スキルに要望するレベルや、そのスキルの重要性レベルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="b7b5e-124">同じスキルでも、職務によって要求される重要性レベルが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="b7b5e-125">作業者、申請者、または連絡担当者のスキルの入力</span><span class="sxs-lookup"><span data-stu-id="b7b5e-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="b7b5e-126">作業者、申請者、または連絡担当者の目標スキルまたは実際のスキルを入力できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="b7b5e-127">目標スキルとは、その従業員が達成を計画しているスキルです。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="b7b5e-128">実際のスキルとは、従業員が現在持っているスキルです。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="b7b5e-129">スキル マッピングとスキル マッピング プロファイル</span><span class="sxs-lookup"><span data-stu-id="b7b5e-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="b7b5e-130">スキル マッピング検索を作成して、特定のタイプのタスクを実行する能力を持つ作業者、申請者、連絡担当者を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="b7b5e-131">スキル マッピングの検索では、スキル、教育、証明書、要職とプロジェクト経験の職位について、入力した基準に一致する結果を返します。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="b7b5e-132">たとえば、組織のどの作業者が CPA を取得しているか調べるときに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="b7b5e-133">スキル マッピング プロファイルを使用すると、現在の従業員から、業務のニーズに直接対応する資格を持つ候補者を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="b7b5e-134">たとえば、その組織で空いている職位のスキル マッピング プロファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="b7b5e-135">特定のジョブのプロファイルを作成して、そのジョブからスキル、教育、証明書をコピーすることにより、プロファイルに入力される基準の 1 つ以上に一致する作業者、申請者、連絡担当者を簡単に検索できます。また、ジョブに要求されるスキルに最も適合する候補者を一覧表示できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="b7b5e-136">**注記** スキル マッピング検索に含めるよう選択した作業者、申請者、および連絡担当者のみを、スキル マッピングの結果一覧に表示したり、スキル プロファイルに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="b7b5e-137">作業者、申請者、連絡担当者をスキル マッピング検索に含める場合は、次の各ページで、**スキル マッピングの対象に含める**の選択を [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="b7b5e-138">ワーカー</span><span class="sxs-lookup"><span data-stu-id="b7b5e-138">Worker</span></span>
> + <span data-ttu-id="b7b5e-139">従業員</span><span class="sxs-lookup"><span data-stu-id="b7b5e-139">Employee</span></span>
> + <span data-ttu-id="b7b5e-140">申請者</span><span class="sxs-lookup"><span data-stu-id="b7b5e-140">Applicant</span></span>
> + <span data-ttu-id="b7b5e-141">連絡先</span><span class="sxs-lookup"><span data-stu-id="b7b5e-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="b7b5e-142">スキル ギャップ分析およびスキル プロファイル分析</span><span class="sxs-lookup"><span data-stu-id="b7b5e-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="b7b5e-143">特定の日付における作業者、申請者、または連絡担当者のコンピテンシーの一覧を表示するスキル プロファイル分析を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="b7b5e-144">個人のスキルを特定のジョブに必要なスキルと比較するスキル ギャップ分析を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b7b5e-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="see-also"></a><span data-ttu-id="b7b5e-145">参照</span><span class="sxs-lookup"><span data-stu-id="b7b5e-145">See also</span></span>
--------

[<span data-ttu-id="b7b5e-146">人事管理</span><span class="sxs-lookup"><span data-stu-id="b7b5e-146">Human resources</span></span>](index.md)




