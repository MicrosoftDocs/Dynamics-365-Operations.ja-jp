---
title: ワークフローを使用した従業員情報の管理
description: この記事では、従業員情報を管理するために人事管理のワークフロー機能を使用する方法を説明します。 たとえば、ワークフローを職位と関連付け、従業員がレコードを変更した際に開始された承認ワークフローをコンフィギュレーションすることができます。
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b76adc228a949d334213eda605972f062aa0e46b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791272"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="7eb7a-104">ワークフローを使用した従業員情報の管理</span><span class="sxs-lookup"><span data-stu-id="7eb7a-104">Use workflows to manage employee information</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7eb7a-105">この記事では、従業員情報を管理するために人事管理のワークフロー機能を使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="7eb7a-106">たとえば、ワークフローを職位と関連付け、従業員がレコードを変更した際に開始された承認ワークフローをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="7eb7a-107">人事管理のワークフロー機能は、人事管理の活動を管理するための数多くのワークフローを提供します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="7eb7a-108">また、特定のワークフローを変更しそれらをレポート階層に関連付けるための数多くのオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="7eb7a-109">複数の標準タイプの従業員情報への変更を管理するのに役立つワークフローが使用できます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="7eb7a-110">職位とワークフローを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="7eb7a-111">その後、従業員が従業員レコードを変更した場合、新しい情報が保存される前に承認が必要なワークフローが開始されます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="7eb7a-112">ワークフローは変更を効率的に管理し従業員のデータを正確な状態に維持するため、次のタイプの情報に対して事前に定義されています。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="7eb7a-113">ID 番号</span><span class="sxs-lookup"><span data-stu-id="7eb7a-113">Identification numbers</span></span>
-   <span data-ttu-id="7eb7a-114">コース</span><span class="sxs-lookup"><span data-stu-id="7eb7a-114">Courses</span></span>
-   <span data-ttu-id="7eb7a-115">教育</span><span class="sxs-lookup"><span data-stu-id="7eb7a-115">Education</span></span>
-   <span data-ttu-id="7eb7a-116">画像</span><span class="sxs-lookup"><span data-stu-id="7eb7a-116">Image</span></span>
-   <span data-ttu-id="7eb7a-117">貸与品目</span><span class="sxs-lookup"><span data-stu-id="7eb7a-117">Loaned items</span></span>
-   <span data-ttu-id="7eb7a-118">職務経験</span><span class="sxs-lookup"><span data-stu-id="7eb7a-118">Professional experience</span></span>
-   <span data-ttu-id="7eb7a-119">プロジェクト経験</span><span class="sxs-lookup"><span data-stu-id="7eb7a-119">Project experience</span></span>
-   <span data-ttu-id="7eb7a-120">スキル</span><span class="sxs-lookup"><span data-stu-id="7eb7a-120">Skills</span></span>
-   <span data-ttu-id="7eb7a-121">要職</span><span class="sxs-lookup"><span data-stu-id="7eb7a-121">Positions of trust</span></span>
-   <span data-ttu-id="7eb7a-122">人事管理アクション</span><span class="sxs-lookup"><span data-stu-id="7eb7a-122">Human resources actions</span></span>
-   <span data-ttu-id="7eb7a-123">コース登録</span><span class="sxs-lookup"><span data-stu-id="7eb7a-123">Course registration</span></span>

<span data-ttu-id="7eb7a-124">従業員の雇用、異動、退職の際、ワークフローに確認プロセスを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="7eb7a-125">これにより、ドキュメントは変更されるか、もしくはアクションの条件がワークフローの一部として定義されます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="7eb7a-126">確認プロセスが完了すると、ドキュメントまたはアクションが完了し、ワークフローは最終的な承認ステップへ移動します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="7eb7a-127">職位階層とワークフローの関連付け</span><span class="sxs-lookup"><span data-stu-id="7eb7a-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="7eb7a-128">コンフィギュレーションした任意の階層とワークフローを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="7eb7a-129">たとえば、職位がマトリックス レポート階層と関連付けられている場合、その職位と関連付けられている従業員の管理者の代わりに、プロジェクト リーダーへ特定のプロジェクト経費を送信するワークフローをコンフィギュレーションする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="7eb7a-130">新しいワークフローを作成もしくは既存のワークフローを変更するには、**人事管理ワークフロー** ページで **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="7eb7a-131">ワークフロー デザイナーの開始には、一覧からワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="7eb7a-132">新しいワークフローの作成、もしくは既存のワークフローのステップ変更のためにデザイナーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="7eb7a-133">既存のワークフローを変更すると、変更は新しいバージョンとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="7eb7a-134">したがって、必要に応じていつでも以前のバージョンに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="7eb7a-135">人事管理ワークフローのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7eb7a-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="7eb7a-136">従業員が個人 ID の変更を要求するときに開始される基本ワークフローをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="7eb7a-137">**人事管理ワークフロー** ページで **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="7eb7a-138">利用可能なワークフローの一覧で **ID 番号** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="7eb7a-139">**実行** をクリックしてワークフロー デザイナーを開始し、メッセージが表示されたらユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="7eb7a-140">ワークフロー要素の一覧から、デザイナー キャンバスに **ID 番号の承認** 要素をドラッグします。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="7eb7a-141">承認要素を **開始** と **完了** に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="7eb7a-142">**承認要素** をダブルクリックしてから、右クリックして **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="7eb7a-143">作業項目の指示を追加するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="7eb7a-144">**割り当て** を選択してから、割り当てタイプで **階層** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="7eb7a-145">**階層** 選択で **コンフィギュレーション可能階層** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="7eb7a-146">停止条件を追加して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="7eb7a-147">追加の指示があればすべて完了させます (追加の警告は存在しません) 。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="7eb7a-148">**保存して終了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-148">Click **Save and close**.</span></span> <span data-ttu-id="7eb7a-149">ダイアログ ボックスが開いたら新しいワークフローを有効化し **有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="7eb7a-150">**人事管理** &gt; **職位** &gt; **職位階層タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="7eb7a-151">**マトリックス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="7eb7a-152">**作業者 ID 番号** ワークフローを一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="7eb7a-152">Add the **Worker identification number** workflow to the list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7eb7a-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7eb7a-153">Additional resources</span></span>

[<span data-ttu-id="7eb7a-154">住所変更の表示と管理</span><span class="sxs-lookup"><span data-stu-id="7eb7a-154">View and manage address changes</span></span>](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]