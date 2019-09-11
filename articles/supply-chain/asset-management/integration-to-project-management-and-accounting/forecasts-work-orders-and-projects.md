---
title: 予測、作業指示書、およびプロジェクト
description: このトピックでは、資産管理におけるプロジェクト管理および会計モジュールの、予測および作業指示書との統合について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886819"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="0680d-103">予測、作業指示書、およびプロジェクト</span><span class="sxs-lookup"><span data-stu-id="0680d-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0680d-104">資産管理では、原価管理を最適化するために**プロジェクト管理および会計**モジュールへの統合が実行され、ユーザーはメンテナンス作業タイプの予測と作業指示書ジョブの原価を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0680d-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="0680d-105">メンテナンス作業タイプの予測を追跡するには、次の 2 つの設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0680d-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="0680d-106">**資産管理** > **設定** > **資産管理パラメーター** > **資産**リンク > **プロジェクト** クイック タブ > **メンテナンス予測プロジェクト**フィールドで、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="0680d-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="0680d-107">**メンテナンス作業タイプ**の既定では、メンテナンス作業タイプの既定の明細行を作成すると、その行の活動番号が自動的に作成されます (**資産** > **設定** > **ジョブ** > **メンテナンス作業タイプの既定**)。</span><span class="sxs-lookup"><span data-stu-id="0680d-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="0680d-108">メンテナンス作業タイプの予測は、次の 2 つの目的に役立ちます。**プロジェクト管理および会計**モジュールで、メンテナンス作業タイプの予測の原価を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0680d-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="0680d-109">さらに、予測は、作業指示書ジョブでメンテナンス作業タイプを選択したときに、自動的に作業指示書ジョブ プロジェクトに転送されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="0680d-110">作業指示書ジョブの原価を追跡するには、最初に作業指示書プロジェクトを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0680d-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="0680d-111">手順の説明については、[作業指示書プロジェクトの設定](../setup-for-work-orders/work-order-project-setup.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0680d-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="0680d-112">作業指示書ジョブ プロジェクト</span><span class="sxs-lookup"><span data-stu-id="0680d-112">Work order job projects</span></span>

<span data-ttu-id="0680d-113">作業指示書に作業指示書ジョブを作成する場合、作業指示書プロジェクトは、**資産管理** > **設定** > **作業指示書** > **プロジェクト設定**での、作業指示書の親プロジェクトの設定によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="0680d-114">作業指示書ジョブ プロジェクトは、次の作業指示書の情報の組み合わせを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="0680d-115">作業指示書で選択された作業指示書タイプ</span><span class="sxs-lookup"><span data-stu-id="0680d-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="0680d-116">作業指示書ジョブの資産に関連する機能の場所</span><span class="sxs-lookup"><span data-stu-id="0680d-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="0680d-117">作業指示書ジョブの資産に関連する資産タイプ</span><span class="sxs-lookup"><span data-stu-id="0680d-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="0680d-118">作業指示書に対して設定された開始予定時刻と終了予定時刻</span><span class="sxs-lookup"><span data-stu-id="0680d-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="0680d-119">上で説明したすべての情報が作業指示書に含まれているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="0680d-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="0680d-120">したがって、作業指示書の親プロジェクトの検索は、利用可能なデータの組み合わせを使用し、作業指示書データに対応するプロジェクト ID を選択することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="0680d-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="0680d-121">例: 下の図では、資産タイプ「トラック エンジン」の設定は、その資産タイプを使用して作成されたすべての作業指示書ジョブが、プロジェクト ID 「000186」のサブ プロジェクトであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="0680d-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![図 1](media/01-integration-to-pma.png)

<span data-ttu-id="0680d-123">作業指示書ジョブでのプロジェクト ID、および関連する活動番号の目的 (**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** > リストから作業指示書を選択 > **明細行の詳細**クイック タブ > **プロジェクト ID** フィールドおよび**活動番号** フィールド) は、**プロジェクト管理および会計**モジュールで、作業指示書ジョブと作業指示書ジョブで選択された資産に関連する原価を追跡することです。</span><span class="sxs-lookup"><span data-stu-id="0680d-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="0680d-124">下の図では、作業指示書プロジェクトおよび関連するプロジェクト活動のグラフィカルな概要を参照できます。</span><span class="sxs-lookup"><span data-stu-id="0680d-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![図 2](media/02-integration-to-pma.png)

<span data-ttu-id="0680d-126">作業指示書に新しい作業指示書ジョブが作成されると、そのジョブの作業指示書プロジェクトが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="0680d-127">作業指示書ジョブに関連する資産の財務分析コードが自動的に作業指示書プロジェクトに転送されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="0680d-128">作業指示書ジョブに対して作成されたプロジェクト活動には、メンテナンス作業タイプ、メンテナンス作業タイプ バリアント、および取引についての関連情報が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="0680d-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="0680d-129">このようなデータは、たとえば、作業指示書から発注書を作成する場合 ([調達](../work-orders/procurement.md) を参照してください) や、時間登録のために**プロジェクト管理と会計**モジュールを使用する場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0680d-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="0680d-130">資産が機能の場所にインストールされていて、その資産が後で別の機能の場所にインストールされた場合は、新しい機能の場所に関連する財務分析コードは資産上で自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="0680d-131">その後、資産の作業指示書ジョブを作成すると、作業指示書ジョブの作業指示書プロジェクトがその資産に関連付けられている財務分析コードを自動的に取得します。</span><span class="sxs-lookup"><span data-stu-id="0680d-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="0680d-132">つまり、機能の場所を使用すると、常に、特定の時点にインストールされていた資産の機能の場所で原価を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0680d-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="0680d-133">財務分析コードの自動更新により、プロジェクトの制御とレポート作成の原価を完全に追跡可能にします。</span><span class="sxs-lookup"><span data-stu-id="0680d-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="0680d-134">作業指示書プロジェクト、作業指示書のライフサイクルの状態、プロジェクト ステージ、およびプロジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="0680d-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="0680d-135">作業指示書のライフサイクルの状態と関連するプロジェクト ステージを作業指示書で正しく使用するには、**プロジェクト管理と会計**モジュールに関する依存関係を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="0680d-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="0680d-136">**プロジェクト管理と会計**モジュールでは、プロジェクト ステージが**プロジェクト管理および会計パラメーター**のプロジェクト タイプに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="0680d-137">**プロジェクト管理および会計パラメーター**では、使用するすべてのプロジェクト タイプについて、関連するプロジェクト ステージのチェック ボックスを必ずオンにしてください。</span><span class="sxs-lookup"><span data-stu-id="0680d-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="0680d-138">次の図では、**作成済** - **見積済** - **スケジュール済** - **処理中** - **完了済**の 5 つのステージが「時間/実費払」および「内部」プロジェクト タイプに対して選択されています。</span><span class="sxs-lookup"><span data-stu-id="0680d-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="0680d-139">この 5 つのステージは、内部メンテナンスおよびサービスメンテナンス作業の両方に関連しています。</span><span class="sxs-lookup"><span data-stu-id="0680d-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="0680d-140">**資産管理**では、プロジェクト タイプは、**作業指示書プロジェクトの設定**フォーム > **プロジェクト グループ** リンクで設定したプロジェクト グループによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="0680d-141">**作業指示書プロジェクトの設定**のプロジェクト グループの設定は、作業指示書を作成するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="0680d-142">作業指示書が作成されると、その作業指示書の作業指示書プロジェクトが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="0680d-143">作業指示書のライフサイクルの状態には、それぞれ関連するプロジェクト ステージが必要です。</span><span class="sxs-lookup"><span data-stu-id="0680d-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="0680d-144">作業指示書のライフサイクルの状態に関連するプロジェクト ステージは、作業指示書プロジェクトで定義されているプロジェクト グループの有効ステージとして定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0680d-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="0680d-145">作業指示書プロジェクトが作業指示書に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="0680d-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="0680d-146">新しい作業指示書を作成する場合、作業指示書プロジェクトの自動割り当ては、**作業指示書プロジェクトの設定** (**資産管理** > **設定** > **作業指示書** > **プロジェクトの設定**) での設定に基づきます。</span><span class="sxs-lookup"><span data-stu-id="0680d-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="0680d-147">次の図に、作業指示プロジェクト グループ、関連するプロジェクト タイプ、プロジェクト ステージと、作業指示書のライフサイクルの状態の間のアソシエーションを示します。</span><span class="sxs-lookup"><span data-stu-id="0680d-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![図 3](media/03-integration-to-pma.png)

![図 4](media/04-integration-to-pma.png)

![図 5](media/05-integration-to-pma.png)

<span data-ttu-id="0680d-151">作業指示書プロジェクトの設定方法については[作業指示書プロジェクトの設定](../setup-for-work-orders/work-order-project-setup.md) を、作業指示書のライフサイクルの状態を作成する方法については[作業指示書のライフサイクルの状態](../setup-for-work-orders/work-order-lifecycle-states.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0680d-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="0680d-152">以下の図は、**プロジェクト管理および会計**モジュールとの統合を可能にする**資産管理**モジュールで作成されるさまざまなプロジェクトと、プロジェクトが関連する作業プロセスのグラフィカルな概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="0680d-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![図 6](media/06-integration-to-pma.png)

