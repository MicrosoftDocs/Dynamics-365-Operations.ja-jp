---
title: 休暇申請ワークフローの作成
description: 休暇および欠勤申請ワークフローを作成して、Dynamics 365 Human Resources で休暇申請を一貫して管理します。
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 218e5a6fc95e92bb631ee568a79b7dfe05f425e6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794544"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="ca739-103">休暇申請ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="ca739-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ca739-104">Dynamics 365 Human Resources でワークフローを作成して、休暇および欠勤申請を一貫して管理します。</span><span class="sxs-lookup"><span data-stu-id="ca739-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="ca739-105">**休暇および欠勤** ワークフローでは、次の操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ca739-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="ca739-106">タスクの定義</span><span class="sxs-lookup"><span data-stu-id="ca739-106">Define tasks</span></span>
- <span data-ttu-id="ca739-107">タスクを完了すべきユーザーの決定</span><span class="sxs-lookup"><span data-stu-id="ca739-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="ca739-108">要求を承認または拒否できるユーザーの指定</span><span class="sxs-lookup"><span data-stu-id="ca739-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="ca739-109">休暇および欠勤申請ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="ca739-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="ca739-110">**休暇および欠勤** のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca739-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ca739-111">**設定** で、**人事管理ワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca739-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="ca739-112">**新規** を選択してから、**休暇及び欠勤申請** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca739-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="ca739-113">**このファイルを開きますか ?** メッセージ ボックスが表示されたら、**開く** を選択して、会社の資格情報でサイン インします。</span><span class="sxs-lookup"><span data-stu-id="ca739-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="ca739-114">ワークフロー エディターを使用して、休暇申請のワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="ca739-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="ca739-115">ワークフローの作成に関する詳細については、[ワークフローの作成の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.) を参照してください</span><span class="sxs-lookup"><span data-stu-id="ca739-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="ca739-116">休暇および欠勤申請ワークフローの日付要素</span><span class="sxs-lookup"><span data-stu-id="ca739-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="ca739-117">次のデータ要素を使用して、休暇と欠勤の要求に対してワークフロー内で条件付の承認、または自動承認を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ca739-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="ca739-118">**金額**</span><span class="sxs-lookup"><span data-stu-id="ca739-118">**Amount**</span></span>
- <span data-ttu-id="ca739-119">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ca739-119">**Comment**</span></span>
- <span data-ttu-id="ca739-120">**法人**</span><span class="sxs-lookup"><span data-stu-id="ca739-120">**Company**</span></span>
- <span data-ttu-id="ca739-121">**作成者**</span><span class="sxs-lookup"><span data-stu-id="ca739-121">**Created by**</span></span>
- <span data-ttu-id="ca739-122">**作成日時**</span><span class="sxs-lookup"><span data-stu-id="ca739-122">**Created date and time**</span></span>
- <span data-ttu-id="ca739-123">**終了日**</span><span class="sxs-lookup"><span data-stu-id="ca739-123">**End date**</span></span>
- <span data-ttu-id="ca739-124">**休暇タイプ**</span><span class="sxs-lookup"><span data-stu-id="ca739-124">**Leave type**</span></span>
- <span data-ttu-id="ca739-125">**変更者**</span><span class="sxs-lookup"><span data-stu-id="ca739-125">**Modified by**</span></span>
- <span data-ttu-id="ca739-126">**変更日時**</span><span class="sxs-lookup"><span data-stu-id="ca739-126">**Modified date and time**</span></span>
- <span data-ttu-id="ca739-127">**理由コード**</span><span class="sxs-lookup"><span data-stu-id="ca739-127">**Reason code**</span></span>
- <span data-ttu-id="ca739-128">**申請 ID**</span><span class="sxs-lookup"><span data-stu-id="ca739-128">**Request ID**</span></span>
- <span data-ttu-id="ca739-129">**入社日**</span><span class="sxs-lookup"><span data-stu-id="ca739-129">**Start date**</span></span>
- <span data-ttu-id="ca739-130">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="ca739-130">**Status**</span></span> 
- <span data-ttu-id="ca739-131">**送信日**</span><span class="sxs-lookup"><span data-stu-id="ca739-131">**Submission date**</span></span>
- <span data-ttu-id="ca739-132">**送信者:**</span><span class="sxs-lookup"><span data-stu-id="ca739-132">**Submitted by**</span></span>
- <span data-ttu-id="ca739-133">**人事による提出**</span><span class="sxs-lookup"><span data-stu-id="ca739-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="ca739-134">**マネージャーによる提出**</span><span class="sxs-lookup"><span data-stu-id="ca739-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="ca739-135">**次のユーザーの代理で提出**</span><span class="sxs-lookup"><span data-stu-id="ca739-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="ca739-136">**ワーカー**</span><span class="sxs-lookup"><span data-stu-id="ca739-136">**Worker**</span></span>
- <span data-ttu-id="ca739-137">**作業者タイプ**</span><span class="sxs-lookup"><span data-stu-id="ca739-137">**Worker type**</span></span>

<span data-ttu-id="ca739-138">これらの例では、次のデータ要素を使用してさまざまなタイプのワークフロー条件を作成する方法を示します：</span><span class="sxs-lookup"><span data-stu-id="ca739-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="ca739-139">条件付きステートメントで **理由コード** を使用して、理由コード **Surgery** を含む病欠の休暇申請を人事部に提出して承認を得る一方で、その他の理由コードはすべてマネージャーに提出します。</span><span class="sxs-lookup"><span data-stu-id="ca739-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="ca739-140">条件付きステートメントの詳細については、[ワークフローの条件付き決定の構成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca739-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="ca739-141">自動アクションで **人事担当者による提出** と **マネージャーによる提出** を使用して、これらの役割が従業員に代わって提出する休暇申請を自動的に承認します。</span><span class="sxs-lookup"><span data-stu-id="ca739-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="ca739-142">自動アクションの詳細については、[ワークフローでの承認プロセスの構成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca739-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="ca739-143">条件文または自動アクションで **休暇タイプ** を使用して、特定の休暇タイプの申請をワークフローでどのようにルーティングするかを制御します。</span><span class="sxs-lookup"><span data-stu-id="ca739-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca739-144">参照</span><span class="sxs-lookup"><span data-stu-id="ca739-144">See also</span></span>

- [<span data-ttu-id="ca739-145">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="ca739-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]