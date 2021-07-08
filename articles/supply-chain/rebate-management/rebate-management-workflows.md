---
title: リベート管理取引のワークフロー
description: このトピックでは、リベート管理の契約ワークフローを設定して、取引を承認および有効化する方法について説明します。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270960"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="c9705-103">リベート管理取引のワークフロー</span><span class="sxs-lookup"><span data-stu-id="c9705-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9705-104">リベート契約を承認するには、リベート管理が他の Finance and Operations アプリと同じワークフロー プラットフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="c9705-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="c9705-105">2 つのジョブ プロセスが各ワークフローに関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="c9705-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="c9705-106">ワークフローの 1 つの要素で取引が承認されます。</span><span class="sxs-lookup"><span data-stu-id="c9705-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="c9705-107">ワークフローの 1 つの要素によって取引が有効化された場合、ユーザー プロセスまたはワークフロー プロセスによってトランザクションが承認されます。</span><span class="sxs-lookup"><span data-stu-id="c9705-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="c9705-108">リベート契約を使用するには、**リベート管理** モジュールでリベート契約を有効にする必要 があります。</span><span class="sxs-lookup"><span data-stu-id="c9705-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="c9705-109">契約を有効にするには、最初に *リベート管理契約ワークフロー* を作成および構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9705-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="c9705-110">ユーザーは取引を手動で承認することはできません。</span><span class="sxs-lookup"><span data-stu-id="c9705-110">Users can't manually approve deals.</span></span> <span data-ttu-id="c9705-111">ワークフローを常に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9705-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="c9705-112">リベート管理取引のワークフローの作成と管理</span><span class="sxs-lookup"><span data-stu-id="c9705-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="c9705-113">自分のリベート管理契約ワークフローで作業を行うには、**リベート管理 \> 設定 \> リベート管理ワークフロー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9705-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="c9705-114">そのレポートで、必要に応じてワークフローを表示、作成、更新できます。</span><span class="sxs-lookup"><span data-stu-id="c9705-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="c9705-115">一度にこのタイプのワークフロー 1 つのみをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9705-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="c9705-116">ワークフローの詳細、**リベート管理ワークフロー** ページの使用方法、ワークフローの作成方法については、[ワークフロー システムの概要](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) および関連トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9705-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="c9705-117">ワークフローを使用した取引の有効化</span><span class="sxs-lookup"><span data-stu-id="c9705-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="c9705-118">ワークフローを通じて取引を有効にするには、取引を開きます (例えば **すべてのリベート管理契約** ページなど)。</span><span class="sxs-lookup"><span data-stu-id="c9705-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="c9705-119">その後、アクション ペインで、**ワークフロー \>提出** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9705-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="c9705-120">ワークフローを通じて新しい取引が処理および承認されると、新しい取引が有効にされ、使用できる状態になります。</span><span class="sxs-lookup"><span data-stu-id="c9705-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="c9705-121">取引が有効化された後は、設定の大部分は変更できません。</span><span class="sxs-lookup"><span data-stu-id="c9705-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="c9705-122">有効な取引を変更する必要がある場合は、まず無効にしてから、新しい取引を作成します。</span><span class="sxs-lookup"><span data-stu-id="c9705-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="c9705-123">新しい取引が古い取引と似ている場合は、古い取引をコピーして作成できます。</span><span class="sxs-lookup"><span data-stu-id="c9705-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="c9705-124">取引が有効化された後に、次の設定を変更できます:</span><span class="sxs-lookup"><span data-stu-id="c9705-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="c9705-125">調整基準</span><span class="sxs-lookup"><span data-stu-id="c9705-125">Reconcile by</span></span>
- <span data-ttu-id="c9705-126">累積保証</span><span class="sxs-lookup"><span data-stu-id="c9705-126">Cumulative guarantee</span></span>
- <span data-ttu-id="c9705-127">転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="c9705-127">Posting profile</span></span>
- <span data-ttu-id="c9705-128">保証用の転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="c9705-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="c9705-129">ドキュメント メモ</span><span class="sxs-lookup"><span data-stu-id="c9705-129">Document notes</span></span>
- <span data-ttu-id="c9705-130">通貨</span><span class="sxs-lookup"><span data-stu-id="c9705-130">Currency</span></span>
- <span data-ttu-id="c9705-131">自</span><span class="sxs-lookup"><span data-stu-id="c9705-131">From date</span></span>
- <span data-ttu-id="c9705-132">最終日</span><span class="sxs-lookup"><span data-stu-id="c9705-132">To date</span></span>

<span data-ttu-id="c9705-133">さらに、リベート明細行を削除できます。</span><span class="sxs-lookup"><span data-stu-id="c9705-133">In addition, rebate lines can be removed.</span></span>
