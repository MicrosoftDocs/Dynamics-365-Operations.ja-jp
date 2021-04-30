---
title: 調達ワークフロー
description: 組織によっては、取引を入力した個人以外のユーザーが購買要求と発注書を承認することを要求している場合があります。 承認プロセスを設定するには、ワークフローを作成できます。
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 126e9969f312ff7f6a6c64b733708754e7659214
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909234"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="9c76c-104">調達ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c76c-105">組織によっては、取引を入力した個人以外のユーザーが購買要求と発注書を承認することを要求している場合があります。</span><span class="sxs-lookup"><span data-stu-id="9c76c-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="9c76c-106">承認プロセスを設定するには、ワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="9c76c-107">1 つのワークフローは 1 つの業務プロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-107">A workflow represents a business process.</span></span> <span data-ttu-id="9c76c-108">ここでは、ドキュメントの処理および承認に携わるべきユーザーを示すことによって、システムにおけるドキュメントの流れを定義します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="9c76c-109">組織でワークフロー システムを使用することにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="9c76c-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="9c76c-110">**一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントの承認プロセスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="9c76c-111">ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="9c76c-112">**プロセスの可視性** - 特定のワークフロー インスタンスのステータス、履歴およびパフォーマンス測定方法を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="9c76c-113">これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="9c76c-114">**集中化された作業一覧** ユーザーはワークフローに参加するすべてのユーザーに割り当てられているワークフロー タスクおよび承認を表示するには、集中化された作業一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="9c76c-115">これは、[作業項目] ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="9c76c-116">作成できるワークフローのタイプ</span><span class="sxs-lookup"><span data-stu-id="9c76c-116">The types of workflows that you can create</span></span>

<span data-ttu-id="9c76c-117">調達には、次のワークフロー タイプが使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="9c76c-118">種類</span><span class="sxs-lookup"><span data-stu-id="9c76c-118">Type</span></span> | <span data-ttu-id="9c76c-119">このタイプは次の目的で使用します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="9c76c-120">購買要求の確認</span><span class="sxs-lookup"><span data-stu-id="9c76c-120">Purchase requisition review</span></span> | <span data-ttu-id="9c76c-121">購買要求の確認と承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="9c76c-122">購買要求明細行の確認</span><span class="sxs-lookup"><span data-stu-id="9c76c-122">Purchase requisition line review</span></span> | <span data-ttu-id="9c76c-123">購買要求の明細行の確認と承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="9c76c-124">発注書ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-124">Purchase order workflow</span></span> | <span data-ttu-id="9c76c-125">発注書の確認および承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="9c76c-126">購買注文明細行ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-126">Purchase order line workflow</span></span> | <span data-ttu-id="9c76c-127">発注書明細行の確認および承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="9c76c-128">仕入先追加申請ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-128">Vendor add application workflow</span></span> | <span data-ttu-id="9c76c-129">仕入先要求経由で新しい仕入先を追加するための確認と承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="9c76c-130">新しいワークフローを追加している場合は、**ワークフローの作成** ダイアログ ボックスに非推奨ワークフローが一覧表示されている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="9c76c-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="9c76c-131">これらは、[Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows) で使用できる *入庫の確認* 機能に関連していますが、現在は推奨されていません。</span><span class="sxs-lookup"><span data-stu-id="9c76c-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="9c76c-132">これらのワークフローは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9c76c-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="9c76c-133">出荷期日通知ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="9c76c-134">請求書受信済通知ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="9c76c-135">製品受領書が通知ワークフローに失敗しました</span><span class="sxs-lookup"><span data-stu-id="9c76c-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="9c76c-136">未確認の製品受領書否認通知ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="9c76c-137">ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="9c76c-137">Creating a workflow</span></span>

<span data-ttu-id="9c76c-138">ワークフローを作成するには、[購買および調達 &gt; 設定 &gt; 購買および調達ワークフロー] に移動し、ワークフローのタイプを選択して新しいワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c76c-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="9c76c-139">ワークフローのキャンバスにワークフロー要素をデザイナーにドラッグし、要素をフローにリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="9c76c-140">ワークフロー要素はコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c76c-140">The workflow elements should be configured.</span></span> <span data-ttu-id="9c76c-141">承認とタスクのワークフロー要素において、どの参加者がアクションを実行する必要があるかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="9c76c-142">参加者のタイプ</span><span class="sxs-lookup"><span data-stu-id="9c76c-142">Types of participants</span></span>

<span data-ttu-id="9c76c-143">参加者の次のグループに承認ステップを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="9c76c-144">ユーザー グループ</span><span class="sxs-lookup"><span data-stu-id="9c76c-144">User group</span></span> | <span data-ttu-id="9c76c-145">説明</span><span class="sxs-lookup"><span data-stu-id="9c76c-145">Description</span></span> |
|---|---|
| <span data-ttu-id="9c76c-146">参加者</span><span class="sxs-lookup"><span data-stu-id="9c76c-146">Participant</span></span> | <span data-ttu-id="9c76c-147">グループまたはロールのメンバに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="9c76c-148">階層</span><span class="sxs-lookup"><span data-stu-id="9c76c-148">Hierarchy</span></span> | <span data-ttu-id="9c76c-149">承認ステップを特定の組織階層のユーザーに割り当てます</span><span class="sxs-lookup"><span data-stu-id="9c76c-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="9c76c-150">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="9c76c-150">Workflow user</span></span> | <span data-ttu-id="9c76c-151">このワークフローのユーザーに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="9c76c-152">キュー</span><span class="sxs-lookup"><span data-stu-id="9c76c-152">Queue</span></span> | <span data-ttu-id="9c76c-153">作業項目キューに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="9c76c-154">ユーザー</span><span class="sxs-lookup"><span data-stu-id="9c76c-154">User</span></span> | <span data-ttu-id="9c76c-155">承認ステップを特定のユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9c76c-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9c76c-156">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="9c76c-156">Additional resources</span></span>

- [<span data-ttu-id="9c76c-157">購買要求のビジネス プロセスのワークフローの定義</span><span class="sxs-lookup"><span data-stu-id="9c76c-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="9c76c-158">購買要求ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9c76c-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="9c76c-159">Onboard 仕入先</span><span class="sxs-lookup"><span data-stu-id="9c76c-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]