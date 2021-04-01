---
title: ワークロード能力のスケジューリング
description: このトピックでは、倉庫内の従業員または倉庫全体のワークロード能力を設定およびスケジュールする方法について説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4eac4838a4df8f1f5863f1ce1895e7aded5fb08b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239281"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="ca2eb-103">ワークロード能力のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="ca2eb-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ca2eb-104">倉庫に対して作業負荷能力をスケジューリングすることも、倉庫ごとに作業者の現在および将来の作業負荷を予測することもできます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="ca2eb-105">倉庫全体の作業負荷を予測することも、入荷作業負荷および出荷作業負荷を個別に予測することもできます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="ca2eb-106">選択した倉庫の作業負荷出力を予測するには、マスター スケジューリング データがそれらの倉庫に対して使用可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="ca2eb-107">詳細については、[マスター プランの概要](../master-planning/master-plans.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="ca2eb-108">倉庫の作業負荷のスケジューリングおよび表示</span><span class="sxs-lookup"><span data-stu-id="ca2eb-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="ca2eb-109">倉庫に対して作業負荷能力をスケジューリングするには、1 つ以上の倉庫に対して作業負荷設定を作成し、作業負荷設定をマスター プランに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="ca2eb-110">作業負荷能力の設定で、出入荷トランザクションの重量、または量の制限を定義できます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="ca2eb-111">各倉庫に対して 1 つ以上の設定を作成し、個々のマスター プランに設定を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="ca2eb-112">たとえば、労働力の季節的な変更に応じて、このアプローチを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="ca2eb-113">倉庫の作業者が出入荷の作業負荷のトランザクションを使用する場合、結合されたビューでワークロードを予測されるように倉庫の能力設定をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="ca2eb-114">倉庫の作業負荷をスケジューリングおよび表示するには、次の作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="ca2eb-115">ワークロードの能力設定を作成し、1 つ以上の倉庫の作業負荷の能力制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="ca2eb-116">作業負荷能力設定をマスター プランに関連付けて、作業負荷予測を作成し、それらの予測が適応される期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="ca2eb-117">倉庫の作業負荷能力設定を作成する</span><span class="sxs-lookup"><span data-stu-id="ca2eb-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="ca2eb-118">**在庫管理** \> **設定** \> **倉庫の監視** \> **ワークロード能力** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ca2eb-119">アクション ウィンドウで、**新規** を選択してワークロード能力設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="ca2eb-120">**倉庫** クイック タブで、**新規** を選択し、明細行に値を入力して、ワークロード能力の設定に倉庫を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="ca2eb-121">**ワークロード能力** レポートが 1 つのビューで出入荷トランザクションの合計ワークロードを表示する必要がある場合、**入庫/出庫ワークロードの組み合わせ** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="ca2eb-122">**トランザクション タイプ** クイック タブで、ワークロードの制限が適用される出入荷トランザクションのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca2eb-123">入荷作業負荷および出荷作業負荷両方に対して 1 つ以上のトランザクション タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="ca2eb-124">量または重量の制限を定義</span><span class="sxs-lookup"><span data-stu-id="ca2eb-124">Define limits for volume or weight</span></span>

<span data-ttu-id="ca2eb-125">該当する倉庫の労働力の制限に応じて、数量または重量の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="ca2eb-126">指定した限度は、**ワークロード能力** レポートで表示できる作業負荷能力の予想に含まれます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="ca2eb-127">数量および品目の重量に関する情報を予測するには、在庫品目 1 つあたりの標準数量および在庫品目 1 つあたりの重量をすべての製品に対して指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="ca2eb-128">必要なフィールドは、**リリース済製品の詳細** ページの **在庫の管理** クイック タブの以下のフィールド グループで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="ca2eb-129">処理</span><span class="sxs-lookup"><span data-stu-id="ca2eb-129">Handling</span></span>
- <span data-ttu-id="ca2eb-130">現物分析コード</span><span class="sxs-lookup"><span data-stu-id="ca2eb-130">Physical dimensions</span></span>
- <span data-ttu-id="ca2eb-131">測定の重み付け</span><span class="sxs-lookup"><span data-stu-id="ca2eb-131">Weight measurements</span></span>

<span data-ttu-id="ca2eb-132">この情報が正しく指定されていない場合、**ワークロード能力** レポートが生成される際にメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="ca2eb-133">レポートから、将来のワークロードを予測するのに必要である不足情報をドリルダウンできます。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="ca2eb-134">マスター プランに作業負荷能力設定を関連付ける</span><span class="sxs-lookup"><span data-stu-id="ca2eb-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="ca2eb-135">**在庫管理** \> **定期処理** \> **ワークロードのスケジュール** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="ca2eb-136">**マスター プラン** フィールドで、作業負荷の予想に使用するマスター プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="ca2eb-137">**日数** フィールドで、作業負荷予想がカバーする日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="ca2eb-138">**ワークロード** フィールドで、マスター プランに関連付ける作業負荷設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="ca2eb-139">作業負荷能力の表示</span><span class="sxs-lookup"><span data-stu-id="ca2eb-139">View workload capacity</span></span>

1. <span data-ttu-id="ca2eb-140">**在庫管理** \> **照会およびレポート** \> **現物在庫レポート** \> **ワークロード能力** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ca2eb-141">**列数** フィールドで、レポートに表示する列数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="ca2eb-142">**注文タイプ** フィールドで、**計画済かつ確認済**、**計画済**、または **確認済** を選択し、レポートで予測する注文のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="ca2eb-143">**負荷タイプ** フィールドで、負荷タイプを選択して、量、または重量のワークロード能力を予測するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="ca2eb-144">**ワークロード能力** フィールドで、ワークロード能力の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca2eb-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]