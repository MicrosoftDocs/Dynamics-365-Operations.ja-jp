---
title: スキルの入力
description: 作業者とマネージャは、Dynamics 365 Human Resources でスキルを入力できます。
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076602"
---
# <a name="enter-skills"></a><span data-ttu-id="52dd9-103">スキルの入力</span><span class="sxs-lookup"><span data-stu-id="52dd9-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="52dd9-104">Dynamics 365 Human Resourcesでは、作業者、申請者、連絡担当者の目標スキルまたは実際のスキルを入力できます。</span><span class="sxs-lookup"><span data-stu-id="52dd9-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="52dd9-105">目標スキルとは、その従業員が達成を計画しているスキルです。</span><span class="sxs-lookup"><span data-stu-id="52dd9-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="52dd9-106">実際のスキルとは、従業員が現在持っているスキルです。</span><span class="sxs-lookup"><span data-stu-id="52dd9-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="52dd9-107">スキルの自動承認のワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="52dd9-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="52dd9-108">承認を必要としないスキル入力を設定するには、スキルを自動承認するワークフローを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52dd9-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="52dd9-109">作業者が入力するスキルには、常に管理者の承認が必要となります。</span><span class="sxs-lookup"><span data-stu-id="52dd9-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="52dd9-110">このワークフローでは、従業員の代理としてマネージャが入力したスキルの自動承認のみ行います。</span><span class="sxs-lookup"><span data-stu-id="52dd9-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="52dd9-111">**人事管理** ワークスペースで、**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="52dd9-112">**設定** で、**人事管理ワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="52dd9-113">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-113">Select **New**.</span></span>

4. <span data-ttu-id="52dd9-114">**ワークフローの作成** ウィンドウで、**作業者のスキル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="52dd9-115">[![作業者のスキル ワークフローの選択](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="52dd9-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="52dd9-116">**このファイル を開きますか？** というダイアログで、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="52dd9-117">メッセージが表示されたら、 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="52dd9-118">ワークフロー エディタで、**スキルの承認** ワークフローの要素を 選択し、その要素をドラッグします。</span><span class="sxs-lookup"><span data-stu-id="52dd9-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="52dd9-119">[![スキルの承認ワークフロー要素の選択](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="52dd9-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="52dd9-120">**開始** 要素を **スキル 1 の承認** 要素に関連付け、**スキル1の承認** 要素を **終了** に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="52dd9-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="52dd9-121">**終了** 要素を表示するには、下部までスクロールする必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="52dd9-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="52dd9-122">他の要素の近くまでドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="52dd9-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="52dd9-123">[![ワークフロー要素の関連付け](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="52dd9-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="52dd9-124">**スキル 1 の承認** ワークフロー要素をダブルクリックし、**手順 1** の要素を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="52dd9-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="52dd9-125">**ステップ 1** の要素を右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="52dd9-126">**プロパティ** ウィンドウで、左側のナビゲーション バーで **条件** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="52dd9-127">**次の条件が満たされた場合にのみこのステップを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="52dd9-128">**条件の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-128">Select **Add condition**.</span></span> <span data-ttu-id="52dd9-129">**場所** の後で、**従業員セルフサービス スキル** を選択し、**従業員セルフサービス skills.Person** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="52dd9-130">**である** の後に、**フィールド** を選択し、**ユーザーと相手方の relationship.Person** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="52dd9-131">[![ 条件の指定](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="52dd9-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="52dd9-132">左側のナビゲーション バーで **割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="52dd9-133">**割り当てタイプ** タブで、**階層** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="52dd9-134">**階層タイプ:** フィールドの **階層の選択** タブで、**管理者階層** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="52dd9-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="52dd9-135">[![管理階層の指定](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="52dd9-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="52dd9-136">**閉じる** を選択し、パンくずキャンバスで **ワークフロー** を選択し、**保存して終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="52dd9-137">ワークフロー作成の詳細については、[ワークフロー システムの概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52dd9-137">For more information about creating workflows, see [Workflow system overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="52dd9-138">作業者のスキルの入力</span><span class="sxs-lookup"><span data-stu-id="52dd9-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="52dd9-139">作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-139">Select a worker.</span></span>

2. <span data-ttu-id="52dd9-140">**作業者** ページのアクション バー で 、**人物** を選択し、**スキル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="52dd9-141">**スキル** ページ で、各スキルについて次のフィールドに情報を入力します:</span><span class="sxs-lookup"><span data-stu-id="52dd9-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="52dd9-142">**スキル** : スキルを選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="52dd9-143">**レベル タイプ**: 作業者が既に持っているスキルの **実績** を選択するか、作業者が取り組むスキルの **目標** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="52dd9-144">**レベル**: 作業者のスキルのレベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="52dd9-145">**レベルの日付け**: 日付を選択するには、カレンダーの日付をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52dd9-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="52dd9-146">**査定者**: 該当する場合は、一覧から査定者を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="52dd9-147">検索にはフィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="52dd9-147">You can filter your search.</span></span>
   - <span data-ttu-id="52dd9-148">**経験年数** : 経験年数を入力します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="52dd9-149">**検証済**: スキルが検証された場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="52dd9-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="52dd9-150">**検証者**: 検証者の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="52dd9-151">スキルの入力が完了したら、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52dd9-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="52dd9-152">参照</span><span class="sxs-lookup"><span data-stu-id="52dd9-152">See also</span></span>

[<span data-ttu-id="52dd9-153">スキルの構成</span><span class="sxs-lookup"><span data-stu-id="52dd9-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="52dd9-154">スキルのマップ</span><span class="sxs-lookup"><span data-stu-id="52dd9-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]