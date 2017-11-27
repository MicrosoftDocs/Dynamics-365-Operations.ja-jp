---
title: "生産の設定の要件"
description: "この記事は、生産管理を使用して作業できるようにするための、設定の要件に関する情報を提供します。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47fe11168ad2ddea2a7033eda8d8bd8220efea32
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="production-setup-requirements"></a><span data-ttu-id="09b01-103">生産の設定の要件</span><span class="sxs-lookup"><span data-stu-id="09b01-103">Production setup requirements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="09b01-104">この記事は、生産管理を使用して作業できるようにするための、設定の要件に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="09b01-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="09b01-105">生産管理は、他のモジュールの機能と統合されます。</span><span class="sxs-lookup"><span data-stu-id="09b01-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="09b01-106">この相互接続により、製造オーダーを変更でき、システム内の他の関連プロセスや計算がすべて自動更新されることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="09b01-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="09b01-107">次の設定プロセスは、実行する順番に記載されています。</span><span class="sxs-lookup"><span data-stu-id="09b01-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="09b01-108">他のモジュールに対して必要な基本設定</span><span class="sxs-lookup"><span data-stu-id="09b01-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="09b01-109">生産コントロールを使用する前に、他のモジュールの情報を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09b01-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="09b01-110">この設定には、次のタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="09b01-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="09b01-111">会社に関する一般情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="09b01-111">Set up general company information.</span></span>
-   <span data-ttu-id="09b01-112">総勘定元帳を設定します。</span><span class="sxs-lookup"><span data-stu-id="09b01-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="09b01-113">品目グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-113">Define item groups.</span></span>
-   <span data-ttu-id="09b01-114">品目グループの勘定科目を設定します。</span><span class="sxs-lookup"><span data-stu-id="09b01-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="09b01-115">在庫管理で在庫品目テーブルを設定します。</span><span class="sxs-lookup"><span data-stu-id="09b01-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="09b01-116">部品表 (BOM) および BOM バージョンを在庫管理で作成します。</span><span class="sxs-lookup"><span data-stu-id="09b01-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="09b01-117">必須のカレンダーおよびリソース設定</span><span class="sxs-lookup"><span data-stu-id="09b01-117">Required calendar and resource setup</span></span>
<span data-ttu-id="09b01-118">生産コントロールを使用する前に、組織管理を開き、カレンダーと運営リソースの作成と定義を次の順序で行います。</span><span class="sxs-lookup"><span data-stu-id="09b01-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="09b01-119">**作業時間テンプレート** – 作業時間テンプレートを設定して、生産のスケジュールに使用できる時間を定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="09b01-120">**カレンダー** – 作業時間カレンダーを設定して、生産のスケジュールに使用できる日付を定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="09b01-121">**リソース グループ** – リソース グループを設定して、スケジュール中に空いている能力の概要を取得するための運営リソースをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="09b01-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="09b01-122">運営リソースを設定する前に、リソース グループを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="09b01-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="09b01-123">ただし、生産コントロールの設定時にリソースをグループ化する方法を理解することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="09b01-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="09b01-124">**リソース** – 運営リソースを設定して、生産プロセスの実行と能力の計画に使用するリソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="09b01-125">生産パラメータに対して必要な設定</span><span class="sxs-lookup"><span data-stu-id="09b01-125">Required production parameters setup</span></span>
<span data-ttu-id="09b01-126">**生産コントロール パラメーター** – 基本的な生産パラメーターを設定して、システムによる製造オーダーの処理方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="09b01-127">製造オーダーの作成方法、見積方法、スケジュール方法、および消費方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="09b01-128">フィードバックの種類や、コスト会計の実行方法を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="09b01-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="09b01-129">仕訳帳名に関して必要な識別</span><span class="sxs-lookup"><span data-stu-id="09b01-129">Required journal name identification</span></span>
<span data-ttu-id="09b01-130">**生産仕訳帳名** – トランザクションの記録と転記で使用される生産仕訳帳名を指定します。</span><span class="sxs-lookup"><span data-stu-id="09b01-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="09b01-131">工程を使用する場合の設定</span><span class="sxs-lookup"><span data-stu-id="09b01-131">Setup if you use operations</span></span>
<span data-ttu-id="09b01-132">工程とは、完成製品を製造するために完了させる特定の活動を表します。</span><span class="sxs-lookup"><span data-stu-id="09b01-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="09b01-133">**注記:** 品目の製造に必要な活動の種類およびそれらの活動の順序と優先順位を把握している必要があります。</span><span class="sxs-lookup"><span data-stu-id="09b01-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="09b01-134">また、担当のリソースとその数を把握している必要があります。</span><span class="sxs-lookup"><span data-stu-id="09b01-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="09b01-135">**工程** – 完成品目の製造に必要なタスクを表す工程を設定します。</span><span class="sxs-lookup"><span data-stu-id="09b01-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="09b01-136">**リレーション** – 関連工程を設定して、詳細プロパティを決定します。</span><span class="sxs-lookup"><span data-stu-id="09b01-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="09b01-137">関連工程を定義するには、[**工程**] ページで [**リレーション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="09b01-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="09b01-138">工順を使用する場合の設定</span><span class="sxs-lookup"><span data-stu-id="09b01-138">Setup if you use routes</span></span>
<span data-ttu-id="09b01-139">工順を使用する場合は、設定する生産工順ごとに工程を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09b01-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="09b01-140">工順とは、生産プロセスの開始から終了までに、工程から工程へと品目が移動する経路を表します。</span><span class="sxs-lookup"><span data-stu-id="09b01-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="09b01-141">**原価カテゴリ** – 指定した処理時間と段取り時間の時間単位原価を定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="09b01-142">**原価グループ** – 原価グループを設定して、さまざまな種類の原価設定を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="09b01-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="09b01-143">**工順グループ** – 工順グループを設定して、工順のグループに関連するパラメータを定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="09b01-144">工順グループの設定は、生産工順を作成する前に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="09b01-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="09b01-145">**工順** – 生産工順を設定して、工順工程のスケジューリング、原価設定、および価格決定と、処理状況レポートを制御する既定の設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="09b01-146">**工順** – 工順バージョンを設定して、生産時の品目の変動を可能にします。</span><span class="sxs-lookup"><span data-stu-id="09b01-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="09b01-147">オプションの詳細設定の定義</span><span class="sxs-lookup"><span data-stu-id="09b01-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="09b01-148">**生産グループ** – 生産グループを設定して、製造オーダーと勘定科目を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="09b01-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="09b01-149">勘定科目を使用すると、注文がレポート用に転記またはグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="09b01-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="09b01-150">**生産管理グループ** – 生産管理グループを作成して、製造オーダーをグループ化します。そのため、緊急の製造オーダーの処理や、注文グループの削除と転記が可能になります。</span><span class="sxs-lookup"><span data-stu-id="09b01-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="09b01-151">[**プロパティ**] – 生産の順序を制御するために自分のリソースに割り当てることができる、特別な属性を作成するためのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="09b01-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="09b01-152">これらの属性は、作業時間テンプレートに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="09b01-152">These attributes are connected to the working time template.</span></span>





