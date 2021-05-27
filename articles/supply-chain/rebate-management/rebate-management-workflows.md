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
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020390"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="71cb8-103">リベート管理取引のワークフロー</span><span class="sxs-lookup"><span data-stu-id="71cb8-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71cb8-104">リベート契約を承認するには、リベート管理が他の Finance and Operations アプリと同じワークフロー プラットフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="71cb8-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="71cb8-105">2 つのジョブ プロセスが各ワークフローに関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="71cb8-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="71cb8-106">ワークフローの 1 つの要素によって取引が有効化された場合、ユーザー プロセスまたはワークフロー プロセスによってトランザクションが承認されます。</span><span class="sxs-lookup"><span data-stu-id="71cb8-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="71cb8-107">ワークフローの 1 つの要素で取引が承認されます。</span><span class="sxs-lookup"><span data-stu-id="71cb8-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="71cb8-108">リベート契約を使用するには、**リベート管理** モジュールでリベート契約を有効にする必要 があります。</span><span class="sxs-lookup"><span data-stu-id="71cb8-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="71cb8-109">契約を有効にするには、最初に *リベート管理契約ワークフロー* を作成および構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71cb8-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="71cb8-110">リベート管理でワークフローが有効になると、ユーザーは取引を手動で承認できません。</span><span class="sxs-lookup"><span data-stu-id="71cb8-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="71cb8-111">ワークフローは常に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71cb8-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="71cb8-112">リベート管理取引のワークフローの作成と管理</span><span class="sxs-lookup"><span data-stu-id="71cb8-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="71cb8-113">自分のリベート管理契約ワークフローで作業を行うには、**リベート管理 \> 設定 \> リベート管理ワークフロー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="71cb8-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="71cb8-114">そのレポートで、必要に応じてワークフローを表示、作成、更新できます。</span><span class="sxs-lookup"><span data-stu-id="71cb8-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="71cb8-115">一度にこのタイプのワークフロー 1 つのみをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="71cb8-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="71cb8-116">ワークフローの詳細、**リベート管理ワークフロー** ページの使用方法、ワークフローの作成方法については、[ワークフロー システムの概要](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) および関連トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="71cb8-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="71cb8-117">ワークフローを使用した取引の有効化</span><span class="sxs-lookup"><span data-stu-id="71cb8-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="71cb8-118">ワークフローを通じて取引を有効にするには、取引を開きます (例えば **すべてのリベート管理契約** ページなど)。</span><span class="sxs-lookup"><span data-stu-id="71cb8-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="71cb8-119">その後、アクション ペインで、**ワークフロー \>提出** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71cb8-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="71cb8-120">ワークフローを通じて新しい取引が処理および承認されると、新しい取引が有効にされ、使用できる状態になります。</span><span class="sxs-lookup"><span data-stu-id="71cb8-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="71cb8-121">取引が有効化された後は、設定を変更できません。</span><span class="sxs-lookup"><span data-stu-id="71cb8-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="71cb8-122">有効な取引を変更する必要がある場合は、無効にしてから、新しい取引を作成します。</span><span class="sxs-lookup"><span data-stu-id="71cb8-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="71cb8-123">新しい取引が古い取引と似ている場合は、古い取引をコピーして作成できます。</span><span class="sxs-lookup"><span data-stu-id="71cb8-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
