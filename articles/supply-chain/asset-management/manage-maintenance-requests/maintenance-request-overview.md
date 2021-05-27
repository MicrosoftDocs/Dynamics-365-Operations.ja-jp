---
title: メンテナンス要求
description: このトピックでは、資産管理のメンテナンス要求の管理についての概要を説明します。
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c72a16b8f3865129ad737c511e50eb34c9f2e91
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015881"
---
# <a name="maintenance-requests"></a><span data-ttu-id="ca5c2-103">メンテナンス要求</span><span class="sxs-lookup"><span data-stu-id="ca5c2-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca5c2-104">メンテナンス要求は、ワーク オーダーを作成せずに、資産がメンテナンスまたは修復作業を必要とする可能性があることをマネージャーまたはプランナーに通知するために作成されたメモまたは申告です。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="ca5c2-105">メンテナンス要求の内容が有効と見なされる場合は、メンテナンス要求に基づいてワーク オーダーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="ca5c2-106">資産管理のどの資産に対しても、メンテナンス要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="ca5c2-107">会社のメンテナンス要求の使用方法に応じて、さまざまなタイプのメンテナンス要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="ca5c2-108">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-108">Here are some examples:</span></span>

- <span data-ttu-id="ca5c2-109">メンテナンス要求</span><span class="sxs-lookup"><span data-stu-id="ca5c2-109">Maintenance requests</span></span>
- <span data-ttu-id="ca5c2-110">摘要</span><span class="sxs-lookup"><span data-stu-id="ca5c2-110">Notes</span></span>
- <span data-ttu-id="ca5c2-111">訂正または機能拡張</span><span class="sxs-lookup"><span data-stu-id="ca5c2-111">Corrections or enhancements</span></span>
- <span data-ttu-id="ca5c2-112">投資</span><span class="sxs-lookup"><span data-stu-id="ca5c2-112">Investments</span></span>
- <span data-ttu-id="ca5c2-113">Depot 修復 (このタイプは、別の場所から資産を受け取りメンテナンスまたは修復作業を行い、そのジョブが完了した後に資産を返す場合に使用されます。)</span><span class="sxs-lookup"><span data-stu-id="ca5c2-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="ca5c2-114">メンテナンス要求の表示</span><span class="sxs-lookup"><span data-stu-id="ca5c2-114">View maintenance requests</span></span>

<span data-ttu-id="ca5c2-115">メンテナンス要求を表示するには、**資産管理**\>**共通**\>**メンテンナンス要求**\>**すべてのメンテナンス要求**、**有効なメンテナンス要求**、または **個人用の機能的な場所のメンテナンス要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="ca5c2-116">各リスト ページには、メンテナンス要求に関連する情報の一部が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![メンテナンス要求の表示](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="ca5c2-118">**個人用の機能的な場所のメンテナンス要求** リスト ページを使用して、作業者として関連付けられている機能的な場所、またはその機能的な場所に導入されている資産を含むメンテナンス要求のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="ca5c2-119">(メンテナンス作業者の機能的な場所を設定する方法については、[メンテナンス作業者および作業者グループ](../setup-for-objects/workers-and-worker-groups.md) を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="ca5c2-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="ca5c2-120">顧客アカウント情報は資産サービス管理 (外部メンテナンス) で使用できますが、資産管理 (内部メンテナンス) では使用できません。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="ca5c2-121">レコードの詳細ビューを開くには、**すべてのメンテナンス要求** リスト ページのグリッド ビューで、**メンテナンス要求** 列のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![メンテナンス要求の詳細の表示](media/02-manage-maintenance-requests.png)

<span data-ttu-id="ca5c2-123">アクション ウィンドウのボタンはタブで整理されます。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="ca5c2-124">次のテーブルで、資産管理に関連するボタンについて簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="ca5c2-125">ボタンの名前</span><span class="sxs-lookup"><span data-stu-id="ca5c2-125">Button name</span></span>                      | <span data-ttu-id="ca5c2-126">説明</span><span class="sxs-lookup"><span data-stu-id="ca5c2-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="ca5c2-127">編集</span><span class="sxs-lookup"><span data-stu-id="ca5c2-127">Edit</span></span>                             | <span data-ttu-id="ca5c2-128">選択したメンテナンス要求を編集します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-129">新規</span><span class="sxs-lookup"><span data-stu-id="ca5c2-129">New</span></span>                              | <span data-ttu-id="ca5c2-130">新しいメンテナンス要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-131">消去</span><span class="sxs-lookup"><span data-stu-id="ca5c2-131">Delete</span></span>                           | <span data-ttu-id="ca5c2-132">選択したメンテナンス要求を削除します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-133">ワーク オーダー プール</span><span class="sxs-lookup"><span data-stu-id="ca5c2-133">Work order pool</span></span>                  | <span data-ttu-id="ca5c2-134">選択したメンテナンス要求をワーク オーダー プールに接続します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="ca5c2-135">ワーク オーダー</span><span class="sxs-lookup"><span data-stu-id="ca5c2-135">Work order</span></span>                       | <span data-ttu-id="ca5c2-136">選択したメンテナンス要求に基づいて、ワーク オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-137">資産エラー</span><span class="sxs-lookup"><span data-stu-id="ca5c2-137">Asset fault</span></span>                      | <span data-ttu-id="ca5c2-138">**資産エラー** をクリックすると、選択したメンテナンス要求でエラー登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-139">ワーク オーダー</span><span class="sxs-lookup"><span data-stu-id="ca5c2-139">Work orders</span></span>                      | <span data-ttu-id="ca5c2-140">選択したメンテナンス要求に接続されているすべてのワーク オーダーのリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-141">メンテナンス要求の状態の更新</span><span class="sxs-lookup"><span data-stu-id="ca5c2-141">Update maintenance request state</span></span> | <span data-ttu-id="ca5c2-142">メンテナンス要求の状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="ca5c2-143">ライフサイクルの状態ログ</span><span class="sxs-lookup"><span data-stu-id="ca5c2-143">Lifecycle state log</span></span>              | <span data-ttu-id="ca5c2-144">選択したメンテナンス要求のライフサイクル状態を表すログを表示します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-145">メンテナンス要求の詳細</span><span class="sxs-lookup"><span data-stu-id="ca5c2-145">Maintenance request details</span></span>      | <span data-ttu-id="ca5c2-146">選択したメンテナンス要求の詳細を表示するレポートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-147">ローン資産の送信</span><span class="sxs-lookup"><span data-stu-id="ca5c2-147">Send loan asset</span></span>                  | <span data-ttu-id="ca5c2-148">選択したメンテナンス要求で選択された資産の一時的な置換となるローン資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="ca5c2-149">ローン資産の返却</span><span class="sxs-lookup"><span data-stu-id="ca5c2-149">Return loan asset</span></span>                | <span data-ttu-id="ca5c2-150">ローン資産を返却済として登録します。</span><span class="sxs-lookup"><span data-stu-id="ca5c2-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]