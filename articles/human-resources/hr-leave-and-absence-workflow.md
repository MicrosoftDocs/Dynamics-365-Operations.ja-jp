---
title: 休暇申請ワークフローの作成
description: 休暇および欠勤申請ワークフローを作成して、Dynamics 365 Human Resources で休暇申請を一貫して管理します。
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2e994d11bbd45907a48c1f3955fa751a676a327
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353691"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="5f30c-103">休暇申請ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="5f30c-103">Create a leave request workflow</span></span>

<span data-ttu-id="5f30c-104">Dynamics 365 Human Resources でワークフローを作成して、休暇および欠勤申請を一貫して管理します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="5f30c-105">**休暇および欠勤**ワークフローでは、次の操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5f30c-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="5f30c-106">タスクの定義</span><span class="sxs-lookup"><span data-stu-id="5f30c-106">Define tasks</span></span>
- <span data-ttu-id="5f30c-107">タスクを完了すべきユーザーの決定</span><span class="sxs-lookup"><span data-stu-id="5f30c-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="5f30c-108">要求を承認または拒否できるユーザーの指定</span><span class="sxs-lookup"><span data-stu-id="5f30c-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="5f30c-109">休暇および欠勤申請ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="5f30c-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="5f30c-110">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="5f30c-111">**設定**で、**人事管理ワークフロー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="5f30c-112">**新規**を選択してから、**休暇及び欠勤申請**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="5f30c-113">**このファイルを開きますか ?** メッセージ ボックスが表示されたら、**開く**を選択して、会社の資格情報でサイン インします。</span><span class="sxs-lookup"><span data-stu-id="5f30c-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="5f30c-114">ワークフロー エディターを使用して、休暇申請のワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="5f30c-115">ワークフローの作成に関する詳細については、[ワークフローの作成の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.) を参照してください</span><span class="sxs-lookup"><span data-stu-id="5f30c-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="5f30c-116">休暇および欠勤申請ワークフローの日付要素</span><span class="sxs-lookup"><span data-stu-id="5f30c-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="5f30c-117">次のデータ要素を使用して、休暇と欠勤の要求に対してワークフロー内で条件付の承認、または自動承認を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5f30c-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="5f30c-118">**コメント**</span><span class="sxs-lookup"><span data-stu-id="5f30c-118">**Comment**</span></span>
- <span data-ttu-id="5f30c-119">**法人**</span><span class="sxs-lookup"><span data-stu-id="5f30c-119">**Company**</span></span>
- <span data-ttu-id="5f30c-120">**作成者**</span><span class="sxs-lookup"><span data-stu-id="5f30c-120">**Created by**</span></span>
- <span data-ttu-id="5f30c-121">**作成日時**</span><span class="sxs-lookup"><span data-stu-id="5f30c-121">**Created date and time**</span></span>
- <span data-ttu-id="5f30c-122">**終了日**</span><span class="sxs-lookup"><span data-stu-id="5f30c-122">**End date**</span></span>
- <span data-ttu-id="5f30c-123">**休暇タイプ**</span><span class="sxs-lookup"><span data-stu-id="5f30c-123">**Leave type**</span></span>
- <span data-ttu-id="5f30c-124">**変更者**</span><span class="sxs-lookup"><span data-stu-id="5f30c-124">**Modified by**</span></span>
- <span data-ttu-id="5f30c-125">**変更日時**</span><span class="sxs-lookup"><span data-stu-id="5f30c-125">**Modified date and time**</span></span>
- <span data-ttu-id="5f30c-126">**理由コード**</span><span class="sxs-lookup"><span data-stu-id="5f30c-126">**Reason code**</span></span>
- <span data-ttu-id="5f30c-127">**申請 ID**</span><span class="sxs-lookup"><span data-stu-id="5f30c-127">**Request ID**</span></span>
- <span data-ttu-id="5f30c-128">**入社日**</span><span class="sxs-lookup"><span data-stu-id="5f30c-128">**Start date**</span></span>
- <span data-ttu-id="5f30c-129">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="5f30c-129">**Status**</span></span> 
- <span data-ttu-id="5f30c-130">**送信日**</span><span class="sxs-lookup"><span data-stu-id="5f30c-130">**Submission date**</span></span>
- <span data-ttu-id="5f30c-131">**送信者:**</span><span class="sxs-lookup"><span data-stu-id="5f30c-131">**Submitted by**</span></span>
- <span data-ttu-id="5f30c-132">**人事による提出**</span><span class="sxs-lookup"><span data-stu-id="5f30c-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="5f30c-133">**マネージャーによる提出**</span><span class="sxs-lookup"><span data-stu-id="5f30c-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="5f30c-134">**次のユーザーの代理で提出**</span><span class="sxs-lookup"><span data-stu-id="5f30c-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="5f30c-135">**ワーカー**</span><span class="sxs-lookup"><span data-stu-id="5f30c-135">**Worker**</span></span>
- <span data-ttu-id="5f30c-136">**作業者タイプ**</span><span class="sxs-lookup"><span data-stu-id="5f30c-136">**Worker type**</span></span>

<span data-ttu-id="5f30c-137">これらの例では、次のデータ要素を使用してさまざまなタイプのワークフロー条件を作成する方法を示します：</span><span class="sxs-lookup"><span data-stu-id="5f30c-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="5f30c-138">条件付きステートメントで **理由コード** を使用して、理由コード **Surgery** を含む病欠の休暇申請を人事部に提出して承認を得る一方で、その他の理由コードはすべてマネージャーに提出します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-138">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="5f30c-139">条件付きステートメントの詳細については、[ワークフローの条件付き決定の構成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f30c-139">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="5f30c-140">自動アクションで **人事担当者による提出** と **マネージャーによる提出** を使用して、これらの役割が従業員に代わって提出する休暇申請を自動的に承認します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-140">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="5f30c-141">自動アクションの詳細については、[ワークフローでの承認プロセスの構成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f30c-141">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="5f30c-142">条件文または自動アクションで **休暇タイプ** を使用して、特定の休暇タイプの申請をワークフローでどのようにルーティングするかを制御します。</span><span class="sxs-lookup"><span data-stu-id="5f30c-142">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f30c-143">参照</span><span class="sxs-lookup"><span data-stu-id="5f30c-143">See also</span></span>

- [<span data-ttu-id="5f30c-144">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="5f30c-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
