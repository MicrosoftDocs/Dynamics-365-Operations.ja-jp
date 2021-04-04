---
title: 休暇の売買申請ワークフローの作成
description: 休暇の売買申請ワークフローを作成して、Dynamics 365 Human Resources で休暇申請の売買を一貫して管理します。
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 16260c66c2e92fb06664a8f20a5fc3ed4a964609
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468134"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="d412a-103">休暇の売買申請ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="d412a-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d412a-104">Dynamics 365 Human Resources でワークフローを作成して、休暇の売買申請を一貫して管理します。</span><span class="sxs-lookup"><span data-stu-id="d412a-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="d412a-105">**休暇の購入と売却** ワークフローでは、次の操作を行うことができます :</span><span class="sxs-lookup"><span data-stu-id="d412a-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="d412a-106">タスクの定義</span><span class="sxs-lookup"><span data-stu-id="d412a-106">Define tasks</span></span>
- <span data-ttu-id="d412a-107">タスクを完了すべきユーザーの決定</span><span class="sxs-lookup"><span data-stu-id="d412a-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="d412a-108">要求を承認または拒否できるユーザーの指定</span><span class="sxs-lookup"><span data-stu-id="d412a-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="d412a-109">休暇の売買申請ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="d412a-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="d412a-110">**休暇および欠勤** のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d412a-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d412a-111">**設定** で、**人事管理ワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d412a-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="d412a-112">**新規** を選択してから、**休暇の売買申請** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d412a-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="d412a-113">**このファイルを開きますか ?** メッセージ ボックスが表示されたら、**開く** を選択して、会社の資格情報でサイン インします。</span><span class="sxs-lookup"><span data-stu-id="d412a-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="d412a-114">ワークフロー エディターを使用して、休暇申請のワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="d412a-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="d412a-115">ワークフローの作成に関する詳細については、[ワークフローの作成の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.) を参照してください</span><span class="sxs-lookup"><span data-stu-id="d412a-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="d412a-116">休暇および欠勤申請ワークフローの日付要素</span><span class="sxs-lookup"><span data-stu-id="d412a-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="d412a-117">次のデータ要素を使用して、休暇の購入と売却の申請に対してワークフロー内で条件付の承認、または自動承認を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d412a-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="d412a-118">**金額**</span><span class="sxs-lookup"><span data-stu-id="d412a-118">**Amount**</span></span>
- <span data-ttu-id="d412a-119">**休暇売買ポリシー**</span><span class="sxs-lookup"><span data-stu-id="d412a-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="d412a-120">**法人**</span><span class="sxs-lookup"><span data-stu-id="d412a-120">**Company**</span></span>
- <span data-ttu-id="d412a-121">**作成者**</span><span class="sxs-lookup"><span data-stu-id="d412a-121">**Created by**</span></span>
- <span data-ttu-id="d412a-122">**作成日時**</span><span class="sxs-lookup"><span data-stu-id="d412a-122">**Created date and time**</span></span>
- <span data-ttu-id="d412a-123">**終了日**</span><span class="sxs-lookup"><span data-stu-id="d412a-123">**End date**</span></span>
- <span data-ttu-id="d412a-124">**休暇タイプ**</span><span class="sxs-lookup"><span data-stu-id="d412a-124">**Leave type**</span></span>
- <span data-ttu-id="d412a-125">**変更者**</span><span class="sxs-lookup"><span data-stu-id="d412a-125">**Modified by**</span></span>
- <span data-ttu-id="d412a-126">**変更日時**</span><span class="sxs-lookup"><span data-stu-id="d412a-126">**Modified date and time**</span></span>
- <span data-ttu-id="d412a-127">**申請 ID**</span><span class="sxs-lookup"><span data-stu-id="d412a-127">**Request ID**</span></span>
- <span data-ttu-id="d412a-128">**開始日**</span><span class="sxs-lookup"><span data-stu-id="d412a-128">**Start date**</span></span>
- <span data-ttu-id="d412a-129">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="d412a-129">**Status**</span></span> 
- <span data-ttu-id="d412a-130">**送信日**</span><span class="sxs-lookup"><span data-stu-id="d412a-130">**Submission date**</span></span>
- <span data-ttu-id="d412a-131">**送信者:**</span><span class="sxs-lookup"><span data-stu-id="d412a-131">**Submitted by**</span></span>
- <span data-ttu-id="d412a-132">**人事による提出**</span><span class="sxs-lookup"><span data-stu-id="d412a-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="d412a-133">**マネージャーによる提出**</span><span class="sxs-lookup"><span data-stu-id="d412a-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="d412a-134">**次のユーザーの代理で提出**</span><span class="sxs-lookup"><span data-stu-id="d412a-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="d412a-135">**ワーカー**</span><span class="sxs-lookup"><span data-stu-id="d412a-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="d412a-136">ワークフローの例</span><span class="sxs-lookup"><span data-stu-id="d412a-136">Workflow examples</span></span>

<span data-ttu-id="d412a-137">これらの例では、次のデータ要素を使用してさまざまなタイプのワークフロー条件を作成する方法を示します：</span><span class="sxs-lookup"><span data-stu-id="d412a-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="d412a-138">自動アクションで **人事担当者による提出** と **マネージャーによる提出** を使用して、これらの役割が従業員に代わって提出する休暇の購入と売却の申請を自動的に承認します。</span><span class="sxs-lookup"><span data-stu-id="d412a-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="d412a-139">自動アクションの詳細については、[ワークフローでの承認プロセスの構成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412a-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="d412a-140">条件文または自動アクションで **休暇タイプ** を使用して、特定の休暇タイプの申請をワークフローでどのようにルーティングするかを制御します。</span><span class="sxs-lookup"><span data-stu-id="d412a-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="d412a-141">参照</span><span class="sxs-lookup"><span data-stu-id="d412a-141">See also</span></span>

[<span data-ttu-id="d412a-142">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="d412a-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="d412a-143">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="d412a-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]