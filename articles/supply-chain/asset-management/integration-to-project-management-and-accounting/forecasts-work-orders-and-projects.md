---
title: 予測、作業指示書、およびプロジェクト
description: このトピックでは、資産管理におけるプロジェクト管理および会計モジュールの、予測および作業指示書との統合について説明します。
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3a55564875afa9125ee0dbb808a514f7b4b17b0b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205325"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="2a27e-103">予測、作業指示書、およびプロジェクト</span><span class="sxs-lookup"><span data-stu-id="2a27e-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2a27e-104">資産管理では、原価管理を最適化するために**プロジェクト管理および会計**モジュールへの統合が実行され、ユーザーはメンテナンス作業タイプの予測と作業指示書ジョブの原価を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-104">In Asset Management, integration with the **Project management and accounting** module helps optimize cost control, so that users can track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="2a27e-105">メンテナンス作業タイプの予測を追跡するには、次の 2 つの設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a27e-105">Tracking of maintenance job type forecasts requires two settings:</span></span>

1. <span data-ttu-id="2a27e-106">**資産管理** > **設定** > **資産管理パラメーター**でプロジェクトを選択してから、**資産**タブ > **プロジェクト** クイック タブ、**メンテナンス予測プロジェクト** フィールドでプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a27e-106">Select a project in **Asset management** > **Setup** > **Asset management parameters**, and then, on the **Assets** tab > on the **Project** FastTab, in the **Maintenance forecast project** field, select a project.</span></span>

2. <span data-ttu-id="2a27e-107">**メンテナンス作業タイプの既定**ページでは、メンテナンス作業タイプの既定の明細行を作成すると、その行の活動番号が自動的に作成されます (**資産管理** > **設定** > **ジョブ** > **メンテナンス作業タイプの既定**)。</span><span class="sxs-lookup"><span data-stu-id="2a27e-107">When you create a maintenance job type default line, an activity number is automatically created for the line on the **Maintenance job type defaults** page (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="2a27e-108">メンテナンス作業タイプの予測では、次の 2 つの目的があります。</span><span class="sxs-lookup"><span data-stu-id="2a27e-108">Maintenance job type forecasts serve two purposes:</span></span> 

- <span data-ttu-id="2a27e-109">**プロジェクト管理および会計**モジュールで、メンテナンス作業タイプの予測原価を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-109">You can track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> 
- <span data-ttu-id="2a27e-110">予測は、作業指示書ジョブでメンテナンス作業タイプを選択したときに、自動的に作業指示書ジョブ プロジェクトに転送されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-110">Forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="2a27e-111">作業指示書ジョブの原価を追跡するには、最初に作業指示書プロジェクトを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a27e-111">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="2a27e-112">詳細については、[作業指示書プロジェクトの設定](../setup-for-work-orders/work-order-project-setup.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a27e-112">For more information, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="2a27e-113">作業指示書ジョブ プロジェクト</span><span class="sxs-lookup"><span data-stu-id="2a27e-113">Work order job projects</span></span>

<span data-ttu-id="2a27e-114">作業指示書に作業指示書ジョブを作成する場合、作業指示書プロジェクトは、**作業指示書プロジェクトの設定**ページ (**資産管理** > **設定** > **作業指示書** > **プロジェクト設定**) での作業指示書の親プロジェクト設定によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-114">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders on the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>

<span data-ttu-id="2a27e-115">作業指示書ジョブ プロジェクトは、次の作業指示書の情報の組み合わせを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-115">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="2a27e-116">作業指示書で選択された作業指示書タイプ</span><span class="sxs-lookup"><span data-stu-id="2a27e-116">The work order type selected on the work order</span></span> 
- <span data-ttu-id="2a27e-117">作業指示書ジョブの資産に関連する機能の場所</span><span class="sxs-lookup"><span data-stu-id="2a27e-117">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="2a27e-118">作業指示書ジョブの資産に関連する資産タイプ</span><span class="sxs-lookup"><span data-stu-id="2a27e-118">The asset type that is related to the asset on the work order job</span></span>  
- <span data-ttu-id="2a27e-119">作業指示書に対して設定された開始予定時刻および終了予定時刻</span><span class="sxs-lookup"><span data-stu-id="2a27e-119">The expected start and end times that are set on the work order</span></span>  

<span data-ttu-id="2a27e-120">この情報の一部は、作業指示書に含まれていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2a27e-120">Some of this information might not be found on a work order.</span></span> <span data-ttu-id="2a27e-121">したがって、作業指示書の親プロジェクトの検索は、利用可能なデータの組み合わせを使用し、作業指示書データに対応するプロジェクト ID を選択することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-121">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds to work order data.</span></span>

<span data-ttu-id="2a27e-122">たとえば、次の図では、**トラック エンジン**資産タイプが設定されているため、**トラック エンジン**資産タイプで作成されたすべての作業指示書ジョブが、プロジェクト ID 000186 のサブ プロジェクトであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="2a27e-122">For example, in the following illustration, because of the way that the **Truck Engine** asset type is set up, every work order job that is created with the **Truck Engine** asset type will be a sub-project of project ID 000186.</span></span>

![図 1](media/01-integration-to-pma.png)

<span data-ttu-id="2a27e-124">作業指示書ジョブのプロジェクト ID、および関連する活動番号の目的は、**プロジェクト管理および会計**モジュールで、作業指示書ジョブに関連する原価と、そのジョブで選択された資産を追跡することです。</span><span class="sxs-lookup"><span data-stu-id="2a27e-124">The purpose of the project ID on the work order job, and the related activity number, is to track costs that are related to the work order job, and the asset that is selected on it, in the **Project management and accounting** module.</span></span> <span data-ttu-id="2a27e-125">(プロジェクト ID および活動番号を表示するには、**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**を選択してから、作業指示書を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a27e-125">(To view the project ID and activity number, select **Asset management** > **Common** > **Work orders** > **All work orders**, and then select the work order.</span></span> <span data-ttu-id="2a27e-126">**行の詳細**クイック タブでは、**プロジェクト ID** フィールドにプロジェクト ID が表示され、**活動番号**フィールドには活動番号が表示されます。) 資産管理の原価管理の詳細については [原価および日付の管理](../controlling-and-reporting/cost-and-date-control.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a27e-126">On the **Line details** FastTab, the **Project ID** field shows the project ID, and the **Activity number** field shows the activity number.) For more information about cost control in Asset Management, see [Cost and date control](../controlling-and-reporting/cost-and-date-control.md).</span></span>

<span data-ttu-id="2a27e-127">下の図では、作業指示書プロジェクトおよび関連するプロジェクト活動の概要をグラフィカルに表示しています。</span><span class="sxs-lookup"><span data-stu-id="2a27e-127">The following illustration shows a graphical overview of work order projects and related project activities.</span></span>

![図 2](media/02-integration-to-pma.png)

<span data-ttu-id="2a27e-129">作業指示書に新しい作業指示書ジョブが作成されると、そのジョブの作業指示書プロジェクトが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-129">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="2a27e-130">作業指示書ジョブに関連する資産の財務分析コードが自動的に作業指示書プロジェクトに転送されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-130">The financial dimensions for the asset that is related to the work order job are automatically transferred to the work order project.</span></span>

<span data-ttu-id="2a27e-131">作業指示書ジョブに対して作成されたプロジェクト活動には、関連する情報が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="2a27e-131">The project activity that is created for a work order job has related information attached to it.</span></span> <span data-ttu-id="2a27e-132">この情報は、メンテナンス作業タイプ、メンテナンス作業タイプ バリアントおよび取引に関する情報です。</span><span class="sxs-lookup"><span data-stu-id="2a27e-132">This information is about the maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="2a27e-133">このようなデータは、たとえば、作業指示書から発注書を作成する場合 ([調達](../work-orders/procurement.md) を参照してください) や、時間登録のために**プロジェクト管理および会計**モジュールを使用する場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-133">It's useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>

<span data-ttu-id="2a27e-134">資産を機能的な場所にインストールしていたのに、後でその資産を別の機能的な場所にインストールした場合は、新しい機能的な場所に関連する財務分析コードは資産上で自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-134">If the asset was installed on a functional location but is later installed on a different functional location, the financial dimensions that are related to the new functional location are automatically updated on the asset.</span></span> <span data-ttu-id="2a27e-135">その後、資産の作業指示書ジョブを作成すると、作業指示書ジョブの作業指示書プロジェクトがその資産に関連付けられている財務分析コードを自動的に取得します。</span><span class="sxs-lookup"><span data-stu-id="2a27e-135">Then, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="2a27e-136">つまり、機能的な場所を使用すると、常に、特定の時点にインストールされていた資産の機能的な場所で原価を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-136">Therefore, when you use functional locations, costs can always be tracked on the functional locations that an asset was installed on at any given time.</span></span> <span data-ttu-id="2a27e-137">財務分析コードの自動更新により、プロジェクトの制御とレポート作成の原価を完全に追跡するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-137">The automatic update of financial dimensions helps guarantee complete traceability of costs for project control and reporting.</span></span>

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="2a27e-138">作業指示書プロジェクト、作業指示書のライフサイクルの状態、プロジェクト ステージ、およびプロジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="2a27e-138">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="2a27e-139">作業指示書のライフサイクル状態と関連するプロジェクト ステージを作業指示書で正しく使用するためには、**プロジェクト管理および会計**モジュールに関する依存関係を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="2a27e-139">To help guarantee that work order lifecycle states and related project stages on work orders are used correctly, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="2a27e-140">**プロジェクト管理および会計**モジュールでは、プロジェクト ステージが**プロジェクト管理および会計パラメーター** ページのプロジェクト タイプに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-140">In the **Project management and accounting** module, project stages are set up on project types on the **Project management and accounting parameters** page.</span></span>  
- <span data-ttu-id="2a27e-141">**プロジェクト管理および会計パラメーター** ページで、使用するすべてのプロジェクト タイプの関連するプロジェクト ステージを選択するためにはこのチェック ボックスを使用します。</span><span class="sxs-lookup"><span data-stu-id="2a27e-141">On the **Project management and accounting parameters** page, use the check boxes to select relevant project stages for all the project types that you will use.</span></span> <span data-ttu-id="2a27e-142">次の図では、5 つのステージ (**作成済**、**見積済**、**スケジュール済**、**処理中**、および**完了済**) が、**時間/実費払い**および**内部**プロジェクト タイプに対して選択されています。</span><span class="sxs-lookup"><span data-stu-id="2a27e-142">In the following illustrations, five stages (**Created**, **Estimated**, **Scheduled**, **In process**, and **Finished**) have been selected for the **Time and material** and **Internal** project types.</span></span> <span data-ttu-id="2a27e-143">この 5 つのステージは、内部メンテナンス作業およびサービス メンテナンス作業の両方に関連しています。</span><span class="sxs-lookup"><span data-stu-id="2a27e-143">Those five stages are relevant to both internal maintenance jobs and service maintenance jobs.</span></span>
- <span data-ttu-id="2a27e-144">**資産管理**モジュールで、プロジェクト タイプは、**作業指示書プロジェクトの設定**ページ > **プロジェクト グループ** タブ (**資産管理** > **設定** > **作業指示書** > **プロジェクト設定**) で設定するプロジェクト グループによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-144">In the **Asset Management** module, project types are defined by the project groups that you set up on the **Work order project setup** page > **Project group** tab (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  
- <span data-ttu-id="2a27e-145">**作業指示書プロジェクトの設定**ページで設定するプロジェクト グループは、作業指示書を作成するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-145">The project groups that are set up on the **Work order project setup** page are used when you create work orders.</span></span> <span data-ttu-id="2a27e-146">作業指示書が作成されると、その作業指示書の作業指示書プロジェクトが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-146">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="2a27e-147">作業指示書ライフサイクルの状態には、それぞれ関連するプロジェクト ステージが必要です。</span><span class="sxs-lookup"><span data-stu-id="2a27e-147">Every work order lifecycle state must have a related project stage.</span></span>  
- <span data-ttu-id="2a27e-148">作業指示書ライフサイクルの状態に関連するプロジェクト ステージは、作業指示書プロジェクトで定義されているプロジェクト グループの有効ステージとして定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a27e-148">The project stage that is related to a work order lifecycle state must be defined as an active stage for the project group that is defined in the work order project.</span></span> <span data-ttu-id="2a27e-149">作業指示書プロジェクトが作業指示書に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-149">The work order project is automatically created on a work order.</span></span>
- <span data-ttu-id="2a27e-150">新しい作業指示書を作成する場合、作業指示書プロジェクトの自動割り当ては、**作業指示書プロジェクトの設定**ページでの設定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="2a27e-150">When you create a new work order, the automatic allocation of a work order project is based on the setup on the **Work order project setup** page.</span></span>  

<span data-ttu-id="2a27e-151">次の図は、作業指示書プロジェクト グループ、関連するプロジェクト タイプ、プロジェクト ステージ、および作業指示書ライフサイクルの状態の間の関連付けを示しています。</span><span class="sxs-lookup"><span data-stu-id="2a27e-151">The following illustrations show the associations between work order project groups, related project types, project stages, and work order lifecycle states.</span></span>

![図 3](media/03-integration-to-pma.png)

![図 4](media/04-integration-to-pma.png)

![図 5](media/05-integration-to-pma.png)

<span data-ttu-id="2a27e-155">作業指示書プロジェクト設定方法の詳細については、[作業指示書プロジェクト設定](../setup-for-work-orders/work-order-project-setup.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a27e-155">For information about how to set up work order projects, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span> <span data-ttu-id="2a27e-156">作業指示書ライフサイクル状態の作成方法の詳細については、[作業指示書ライフサイクルの状態](../setup-for-work-orders/work-order-lifecycle-states.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a27e-156">For information about how to create work order lifecycle states, see [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md).</span></span>

<span data-ttu-id="2a27e-157">次の図は、**資産管理**モジュールで作成された各種プロジェクトの概要をグラフィカルに表示して、**プロジェクト管理および会計**モジュールと統合できるようにしたものです。</span><span class="sxs-lookup"><span data-stu-id="2a27e-157">The following illustration shows a graphical overview of the various projects that are created in the **Asset management** module to enable integration with the **Project management and accounting** module.</span></span> <span data-ttu-id="2a27e-158">プロジェクトが関連付けられている作業プロセスも表示されます。</span><span class="sxs-lookup"><span data-stu-id="2a27e-158">It also shows the work processes that the projects are related to.</span></span>

![図 6](media/06-integration-to-pma.png)

