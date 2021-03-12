---
title: 出荷連結ポリシーを構成する
description: このトピックでは、既定およびユーザー定義の出荷連結ポリシーの設定方法について説明します。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0d6ab6c034a5c341432f661cf1e729dfd3e5c239
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996401"
---
# <a name="configure-shipment-consolidation-policies"></a><span data-ttu-id="c8967-103">出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="c8967-103">Configure shipment consolidation policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8967-104">出荷連結ポリシーを使用した出荷連結のプロセスを使用することで、倉庫への自動リリースと手動リリースの処理にて自動出荷連結が可能となります。</span><span class="sxs-lookup"><span data-stu-id="c8967-104">The shipment consolidation process that uses shipment consolidation policies allows for automated shipment consolidation during automated and manual release to the warehouse.</span></span> <span data-ttu-id="c8967-105">この機能を有効にした後は、初期ポリシーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-105">After you turn on this feature, you must configure your initial policies.</span></span> <span data-ttu-id="c8967-106">ポリシーが構成されていない場合は、販売明細行ごとに1つの積荷明細行を持つ個別の出荷が生成されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-106">If no policies are configured, each sales line will generate a separate shipment that has a single load line.</span></span>

<span data-ttu-id="c8967-107">このトピックで説明するシナリオでは、既定およびユーザー定義の出荷連結ポリシーを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c8967-107">The scenarios that are presented in this topic show how to set up default and custom shipment consolidation policies.</span></span>

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a><span data-ttu-id="c8967-108">出荷連結ポリシーの機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="c8967-108">Turn on the Shipment consolidation policies feature</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8967-109">このトピックで説明する[最初のシナリオ](#scenario-1)では、まず以前の出荷連結機能を使用するよう、倉庫の設定をします。</span><span class="sxs-lookup"><span data-stu-id="c8967-109">In the [first scenario](#scenario-1) that is described in this topic, you will first set up a warehouse so that it uses the earlier shipment consolidation feature.</span></span> <span data-ttu-id="c8967-110">続いて、出荷統合ポリシーを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-110">You will then make shipment consolidation policies available.</span></span> <span data-ttu-id="c8967-111">このようにして、アップグレード シナリオの機能を体験できます。</span><span class="sxs-lookup"><span data-stu-id="c8967-111">In this way, you can experience how the upgrade scenario works.</span></span> <span data-ttu-id="c8967-112">デモ データ環境を使用して最初のシナリオを実行する場合は、この機能を有効にしてからシナリオを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-112">If you plan to use a demo data environment to go through the first scenario, don't turn on the feature before you do the scenario.</span></span>

<span data-ttu-id="c8967-113">*出荷連結ポリシー* 機能を使用する前に 、システムでこの機能を有効にしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-113">Before you can use the *Shipment consolidation policies* feature, you must turn it on in your system.</span></span> <span data-ttu-id="c8967-114">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c8967-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c8967-115">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="c8967-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c8967-116">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="c8967-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c8967-117">**機能名:** *出荷連結*</span><span class="sxs-lookup"><span data-stu-id="c8967-117">**Feature name:** *Consolidate shipment*</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="c8967-118">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="c8967-118">Make demo data available</span></span>

<span data-ttu-id="c8967-119">それぞれのトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management で利用可能な標準的なデモデータに含まれる値とレコードを参照し ます。</span><span class="sxs-lookup"><span data-stu-id="c8967-119">Each scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c8967-120">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-120">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a><span data-ttu-id="c8967-121">シナリオ1:既定の出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="c8967-121">Scenario 1: Configure default shipment consolidation policies</span></span>

<span data-ttu-id="c8967-122">*出荷連結ポリシー* 機能を有効にした後に、最低限の既定のポリシーを構成する必要がある場合には、次の2つの状況が想定されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-122">There are two situations where you must configure the minimum number of default policies after you turn on the *Shipment consolidation policies* feature:</span></span>

- <span data-ttu-id="c8967-123">既にデータが格納されている環境をアップグレードしている。</span><span class="sxs-lookup"><span data-stu-id="c8967-123">You're upgrading an environment that already contains data.</span></span>
- <span data-ttu-id="c8967-124">全く新しい環境を設定している。</span><span class="sxs-lookup"><span data-stu-id="c8967-124">You're setting up a completely new environment.</span></span>

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a><span data-ttu-id="c8967-125">クロス オーダー連結用に構成されている倉庫の環境をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="c8967-125">Upgrade an environment where warehouses are already configured for cross-order consolidation</span></span>

<span data-ttu-id="c8967-126">この手順を開始する、基本的なクロスオーダー連結の機能が既に使用されている環境をシミュレートするには、*出荷連結ポリシー* 機能を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-126">When you start this procedure, the *Shipment consolidation policies* feature should be turned off, to simulate an environment where the basic cross-order consolidation feature was already used.</span></span> <span data-ttu-id="c8967-127">続いて、機能管理を使用してこの機能を有効化することで、アップグレード後に出荷連結ポリシーを設定する方法を身につけることができます。</span><span class="sxs-lookup"><span data-stu-id="c8967-127">You will then use feature management to turn on the feature, so that you can learn how to set up shipment consolidation policies after the upgrade.</span></span>

<span data-ttu-id="c8967-128">クロスオーダー連結の使用が既に構成されている倉庫環境で、既定の出荷連結ポリシーを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8967-128">Follow these steps to set up default shipment consolidation policies in an environment where warehouses have already been configured for cross-order consolidation.</span></span>

1. <span data-ttu-id="c8967-129">**倉庫管理 \> 設定 \> 倉庫 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-129">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="c8967-130">一覧から、目的の倉庫レコードを検索して開きます (例:**USMF** デモデータ内倉庫 *24*)。</span><span class="sxs-lookup"><span data-stu-id="c8967-130">In the list, find and open the desired warehouse record (for example, warehouse *24* in the **USMF** demo data).</span></span>
1. <span data-ttu-id="c8967-131">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-131">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c8967-132">**倉庫** のクイックタブで、 **倉庫にリリースする出荷を連結する** オプションを *はい* に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="c8967-132">On the **Warehouse** FastTab, set the **Consolidate shipment at release to warehouse** option to *Yes*.</span></span>
1. <span data-ttu-id="c8967-133">連結が必要となるその他すべての倉庫に対して、手順 2 から 手順 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="c8967-133">Repeat steps 2 through 4 for all other warehouses where consolidation is required.</span></span>
1. <span data-ttu-id="c8967-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-134">Close the page.</span></span>
1. <span data-ttu-id="c8967-135">[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して、*出荷連結ポリシー* 機能を有効化します。</span><span class="sxs-lookup"><span data-stu-id="c8967-135">Use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the *Shipment consolidation policies* feature.</span></span> <span data-ttu-id="c8967-136">**機能管理** ワークスペースでは、この機能は *出荷連結* と呼ばれ ます。</span><span class="sxs-lookup"><span data-stu-id="c8967-136">In the **Feature management** workspace, the feature is named *Consolidate shipment*.</span></span>
1. <span data-ttu-id="c8967-137">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-137">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span> <span data-ttu-id="c8967-138">機能の有効化後は、新しい **出荷連結ポリシー** メニュー項目を表示するには、ブラウザーの更新が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-138">You might have to refresh your browser to see the new **Shipment consolidation policies** menu item after you turn on the feature.</span></span>
1. <span data-ttu-id="c8967-139">アクション ウィンドウで、**既定の設定の作成** を選択して次のポリシーを作成します:</span><span class="sxs-lookup"><span data-stu-id="c8967-139">On the Action Pane, select **Create default setup** to create the following policies:</span></span>

    - <span data-ttu-id="c8967-140">ポリシータイプ *販売注文* で使用する **クロスオーダー** のポリシー (以前の連結機能を使用するように設定している倉庫が少なくとも1つ存在する場合)</span><span class="sxs-lookup"><span data-stu-id="c8967-140">A **CrossOrder** policy for the *Sales orders* policy type (provided that you have at least one warehouse that is set up to use the earlier consolidation feature)</span></span>
    - <span data-ttu-id="c8967-141">ポリシータイプ *販売注文* で使用する **既定** のポリシー</span><span class="sxs-lookup"><span data-stu-id="c8967-141">A **Default** policy for the *Sales orders* policy type</span></span>
    - <span data-ttu-id="c8967-142">ポリシータイプ *移管の問題* で使用する **既定** のポリシー</span><span class="sxs-lookup"><span data-stu-id="c8967-142">A **Default** policy for the *Transfer issue* policy type</span></span>
    - <span data-ttu-id="c8967-143">ポリシータイプ *移管の問題* で使用する **クロスオーダー** のポリシー (以前の連結機能を使用するように設定している倉庫が少なくとも1つ存在する場合)</span><span class="sxs-lookup"><span data-stu-id="c8967-143">A **CrossOrder** policy for the *Transfer issue* policy type (provided you have at least one warehouse that is set up to use the earlier consolidation feature)</span></span>

    > [!NOTE]
    > - <span data-ttu-id="c8967-144">いずれの **クロスオーダー ポリシー** も、注文番号のフィールドを除いて、以前のロジックと同じフィールドのセットを考慮します。</span><span class="sxs-lookup"><span data-stu-id="c8967-144">Both **CrossOrder** policies consider the same set of fields as the earlier logic, except for the field for the order number.</span></span> <span data-ttu-id="c8967-145">(このフィールドは、倉庫、輸送モード、住所などの要因に基づいて明細行を出荷に統合する目的で使用されます。)</span><span class="sxs-lookup"><span data-stu-id="c8967-145">(That field is used to consolidate lines into shipments, based on factors such as the warehouse, transportation mode of delivery, and address.)</span></span>
    > - <span data-ttu-id="c8967-146">いずれの **既定** のポリシーも、注文番号のフィールドを含め、以前のロジックと同じフィールドのセットを考慮します。</span><span class="sxs-lookup"><span data-stu-id="c8967-146">Both **Default** policies consider the same set of fields as the earlier logic, including the field for the order number.</span></span> <span data-ttu-id="c8967-147">(このフィールドは、注文番号、倉庫、輸送モード、住所などの要因に基づいて明細行を出荷に統合する目的で使用されます。)</span><span class="sxs-lookup"><span data-stu-id="c8967-147">(That field is used to consolidate lines into shipments, based on factors such as the order number, warehouse, transportation mode of delivery, and address.)</span></span>

1. <span data-ttu-id="c8967-148">ポリシータイプ *販売注文* が使用する **クロスオーダー** ポリシーを選択し、続いてアクション ウィンドウで **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-148">Select the **CrossOrder** policy for the *Sales orders* policy type, and then, on the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c8967-149">[クエリの編集] ダイアログボックスで、**倉庫にリリースする出荷を連結する** オプションが *はい* に設定されている倉庫が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-149">In the query editor dialog box, notice that warehouses where the **Consolidate shipment at release to warehouse** option is set to *Yes* are listed.</span></span> <span data-ttu-id="c8967-150">そのため、これらはクエリに含まれます。</span><span class="sxs-lookup"><span data-stu-id="c8967-150">Therefore, they are included in the query.</span></span>

### <a name="create-default-policies-for-a-new-environment"></a><span data-ttu-id="c8967-151">新規環境で使用する既定のポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="c8967-151">Create default policies for a new environment</span></span>

<span data-ttu-id="c8967-152">次の手順に従って、新規環境における既定の出荷連結ポリシーを設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-152">Follow these steps to set up default shipment consolidation policies in a brand-new environment.</span></span>

1. <span data-ttu-id="c8967-153">[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して、*出荷連結ポリシー* 機能を有効化します (まだ有効化していない場合)。</span><span class="sxs-lookup"><span data-stu-id="c8967-153">Use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the *Shipment consolidation policies* feature, if you haven't already turned it on.</span></span> <span data-ttu-id="c8967-154">**機能管理** ワークスペースでは、この機能は *出荷連結* と呼ばれ ます。</span><span class="sxs-lookup"><span data-stu-id="c8967-154">In the **Feature management** workspace, the feature is named *Consolidate shipment*.</span></span>
1. <span data-ttu-id="c8967-155">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-155">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c8967-156">アクション ウィンドウで、**既定の設定の作成** を選択して次のポリシーを作成します:</span><span class="sxs-lookup"><span data-stu-id="c8967-156">On the Action Pane, select **Create default setup** to create the following policies:</span></span>

    - <span data-ttu-id="c8967-157">ポリシータイプ *販売注文* で使用する **既定** のポリシー</span><span class="sxs-lookup"><span data-stu-id="c8967-157">A **Default** policy for the *Sales orders* policy type</span></span>
    - <span data-ttu-id="c8967-158">ポリシータイプ *移管の問題* で使用する **既定** のポリシー</span><span class="sxs-lookup"><span data-stu-id="c8967-158">A **Default** policy for the *Transfer issue* policy type</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8967-159">いずれの **既定** のポリシーも、注文番号のフィールドを含め、以前のロジックと同じフィールドのセットを考慮します。</span><span class="sxs-lookup"><span data-stu-id="c8967-159">Both **Default** policies consider the same set of fields as the earlier logic, including the field for the order number.</span></span> <span data-ttu-id="c8967-160">(このフィールドは、注文番号、倉庫、輸送モード、住所などの要因に基づいて明細行を出荷に統合する目的で使用されます。)</span><span class="sxs-lookup"><span data-stu-id="c8967-160">(That field is used to consolidate lines into shipments, based on factors such as the order number, warehouse, transportation mode of delivery, and address.)</span></span>

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a><span data-ttu-id="c8967-161">シナリオ 2: ユーザー定義の出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="c8967-161">Scenario 2: Configure custom shipment consolidation policies</span></span>

<span data-ttu-id="c8967-162">このシナリオでは、ユーザー定義の出荷連結ポリシーを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c8967-162">This scenario shows how to set up custom shipment consolidation policies.</span></span> <span data-ttu-id="c8967-163">ユーザー定義のポリシーでは、出荷連結が複数の条件に基づいている場合であっても、複雑な業務要件に対応できます。</span><span class="sxs-lookup"><span data-stu-id="c8967-163">Custom policies can support complex business requirements where shipment consolidation depends on several conditions.</span></span> <span data-ttu-id="c8967-164">このシナリオ後半であつかう各ポリシーの例には、ビジネス ケースの簡単な説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c8967-164">For each example policy later in this scenario, a short description of the business case is included.</span></span> <span data-ttu-id="c8967-165">これらのサンプル ポリシーは、ピラミッド型のクエリの評価を確実に実行するような順序で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-165">These example policies should be set up in a sequence that ensures a pyramid-like evaluation of the queries.</span></span> <span data-ttu-id="c8967-166">(つまり、最も条件が揃っている政策を優先的に評価する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="c8967-166">(In other words, the policies that have the most conditions should be evaluated as having the highest priority.)</span></span>

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a><span data-ttu-id="c8967-167">機能を有効化して、このシナリオで使用するマスター データを準備する</span><span class="sxs-lookup"><span data-stu-id="c8967-167">Turn on the feature and prepare master data for this scenario</span></span>

<span data-ttu-id="c8967-168">このシナリオの演習を行う前に、次のサブセクションで説明するとおり、機能を有効にして、フィルタ処理を行うために必要となるマスターデータを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-168">Before you can go through the exercises in this scenario, you must turn on the feature and prepare the master data that is required to do the filtering, as described in the following subsections.</span></span> <span data-ttu-id="c8967-169">(これら前提条件は、[出荷連結ポリシーの使用方法のシナリオ例](#example-scenarios)に記載されているシナリオにも適用されます。)</span><span class="sxs-lookup"><span data-stu-id="c8967-169">(These prerequisites also apply to the scenarios listed in [Example scenarios of how to use shipment consolidation policies](#example-scenarios).)</span></span>

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a><span data-ttu-id="c8967-170">機能を有効にして既定のポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-170">Turn on the feature and create the default policies</span></span>

<span data-ttu-id="c8967-171">機能管理を使用してこの機能を有効化し (まだ有効化していない場合)、[シナリオ 1](#scenario-1)に記載されている既定の連結ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c8967-171">Use feature management to turn on the feature, if you haven't already turned it on, and create the default consolidation polices that are described in [scenario 1](#scenario-1).</span></span>

#### <a name="create-two-new-product-filter-codes"></a><span data-ttu-id="c8967-172">2 つの新しい製品フィルター コードを作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-172">Create two new product filter codes</span></span>

1. <span data-ttu-id="c8967-173">**倉庫管理 \> 設定 \> 製品フィルター \>  製品フィルター** に移動し、2つの製品フィルターを追加します:</span><span class="sxs-lookup"><span data-stu-id="c8967-173">Go to **Warehouse management \> Setup \> Product filters \> Product filters**, and add two product filters:</span></span>

    - <span data-ttu-id="c8967-174">製品フィルター 1:</span><span class="sxs-lookup"><span data-stu-id="c8967-174">Product filter 1:</span></span>

        - <span data-ttu-id="c8967-175">**フィルターコード :** *可燃性*</span><span class="sxs-lookup"><span data-stu-id="c8967-175">**Filter code:** *Flammable*</span></span>
        - <span data-ttu-id="c8967-176">**フィルタータイトル :** *コード 4*</span><span class="sxs-lookup"><span data-stu-id="c8967-176">**Filter title:** *Code 4*</span></span>

    - <span data-ttu-id="c8967-177">製品フィルター 2:</span><span class="sxs-lookup"><span data-stu-id="c8967-177">Product filter 2:</span></span>

        - <span data-ttu-id="c8967-178">**フィルターコード :** *爆発性*</span><span class="sxs-lookup"><span data-stu-id="c8967-178">**Filter code:** *Explosive*</span></span>
        - <span data-ttu-id="c8967-179">**フィルタータイトル :** *コード 4*</span><span class="sxs-lookup"><span data-stu-id="c8967-179">**Filter title:** *Code 4*</span></span>

1. <span data-ttu-id="c8967-180">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-180">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c8967-181">品目番号 *M9200* の製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="c8967-181">Open the product that has item number *M9200*.</span></span> <span data-ttu-id="c8967-182">(選択する製品は、高度な \[WMS\] 処理が有効化されている必要があり、この製品は **USMF** のデモ データのWMSに対応しています。)</span><span class="sxs-lookup"><span data-stu-id="c8967-182">(The product that you select must be enabled for advanced warehouse \[WMS\] processes, and this product is pre-enabled for WMS processes in the **USMF** demo data.)</span></span>
1. <span data-ttu-id="c8967-183">**倉庫** のクイックタブで、**コード 4** フィールドを *可燃性* に設定 します。</span><span class="sxs-lookup"><span data-stu-id="c8967-183">On the **Warehouse** FastTab, set the **Code 4** field to *Flammable*.</span></span>
1. <span data-ttu-id="c8967-184">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-184">Close the page.</span></span>
1. <span data-ttu-id="c8967-185">品目番号 *M9201* の製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="c8967-185">Open the product that has item number *M9201*.</span></span> <span data-ttu-id="c8967-186">(この製品は、**USMF** デモデータ内の WMS のプロセスにも対応しています。)</span><span class="sxs-lookup"><span data-stu-id="c8967-186">(This product is also pre-enabled for WMS processes in the in the **USMF** demo data.)</span></span>
1. <span data-ttu-id="c8967-187">**倉庫** のクイックタブで、**コード 4** フィールドを *爆発性* に設定 します。</span><span class="sxs-lookup"><span data-stu-id="c8967-187">On the **Warehouse** FastTab, set the **Code 4** field to *Explosive*.</span></span>
1. <span data-ttu-id="c8967-188">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-188">Close the page.</span></span>

#### <a name="create-a-new-transportation-mode-of-delivery"></a><span data-ttu-id="c8967-189">新規配送モードを作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-189">Create a new transportation mode of delivery</span></span>

1. <span data-ttu-id="c8967-190">**輸送管理 \> 設定 \> 配送業者 \> 方式** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-190">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="c8967-191">連結クエリでで使用する輸送モードを作成し、*航空路* と名付けます。</span><span class="sxs-lookup"><span data-stu-id="c8967-191">Create a transportation mode that will be used in consolidation queries, and name it *Airways*.</span></span>
1. <span data-ttu-id="c8967-192">**輸送管理 \> 設定 \> 配送業者 \> 出荷の配送業者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-192">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="c8967-193">配送業者を作成し、以下の設定を行います:</span><span class="sxs-lookup"><span data-stu-id="c8967-193">Create a carrier that has the following settings:</span></span>

    - <span data-ttu-id="c8967-194">**配送業者 :** *航空路*</span><span class="sxs-lookup"><span data-stu-id="c8967-194">**Shipping carrier:** *Airways*</span></span>
    - <span data-ttu-id="c8967-195">**名前 :** *航空路*</span><span class="sxs-lookup"><span data-stu-id="c8967-195">**Name:** *Airways*</span></span>
    - <span data-ttu-id="c8967-196">**モード :** *航空路*</span><span class="sxs-lookup"><span data-stu-id="c8967-196">**Mode:** *Airways*</span></span>

1. <span data-ttu-id="c8967-197">新たな配送業者の **サービス** クイックタブで、次の設定を含む行を追加します:</span><span class="sxs-lookup"><span data-stu-id="c8967-197">On the **Services** FastTab for the new carrier, add a row that has the following settings:</span></span>

    - <span data-ttu-id="c8967-198">**配送サービス :** *Air*</span><span class="sxs-lookup"><span data-stu-id="c8967-198">**Carrier service:** *Air*</span></span>
    - <span data-ttu-id="c8967-199">**輸送方法 :** *Air*</span><span class="sxs-lookup"><span data-stu-id="c8967-199">**Transportation method:** *Air*</span></span>

1. <span data-ttu-id="c8967-200">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-200">On the Action Pane, select **Save**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8967-201">新たな配送業者を保存すると、新たな行の **サービス** グリッドの **荷渡方法** フィールドが自動的に *Airwa-Air* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-201">When you save the new carrier, the **Mode of delivery** field for the new row in the **Services** grid is automatically set to *Airwa-Air*.</span></span> <span data-ttu-id="c8967-202">*Airwa-Air* モードで販売注文を使用する場合は 、関連する出荷に対しては輸送モード *航空路* が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-202">When you use the *Airwa-Air* mode of delivery for a sales order, the *Airways* transportation mode will be used for related shipments.</span></span>

#### <a name="create-an-order-pool"></a><span data-ttu-id="c8967-203">オーダー プールの作成</span><span class="sxs-lookup"><span data-stu-id="c8967-203">Create an order pool</span></span>

1. <span data-ttu-id="c8967-204">**販売とマーケティング \> 設定\> 販売注文 \>オ ーダープール** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-204">Go to **Sales and marketing \> Setup \> Sales orders \> Order pools**.</span></span>
1. <span data-ttu-id="c8967-205">連結クエリで使用する注文管理グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="c8967-205">Create an order pool that will be used for the consolidation query.</span></span> <span data-ttu-id="c8967-206">このオーダー プールには、次の設定が必要となります :</span><span class="sxs-lookup"><span data-stu-id="c8967-206">This order pool should have the following settings:</span></span>

    - <span data-ttu-id="c8967-207">**プール :** 他のプールで使用されていない整数を入力します。</span><span class="sxs-lookup"><span data-stu-id="c8967-207">**Pool:** Enter an integer that isn't already used by any other pool.</span></span>
    - <span data-ttu-id="c8967-208">**名前 :** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="c8967-208">**Name:** *ShipCons*</span></span>

1. <span data-ttu-id="c8967-209">**販売とマーケティング \> 顧客 \> すべての顧客** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-209">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="c8967-210">顧客番号 *US-003* の顧客を開きます。</span><span class="sxs-lookup"><span data-stu-id="c8967-210">Open the customer that has account number *US-003*.</span></span>
1. <span data-ttu-id="c8967-211">**販売注文の既定の設定** クイックタブで、**販売注文のオーダープール** フィールドを、作成した注文管理グループに設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-211">On the **Sales order defaults** FastTab, set the **Sales order pool** field to the order pool that you just created.</span></span>
1. <span data-ttu-id="c8967-212">ページを閉じ、顧客番号 *US-004* の顧客に対して、手順 4 と 手順 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="c8967-212">Close the page, and then repeat the steps 4 and 5 for the customer that has account number *US-004*.</span></span>

### <a name="create-example-policy-1"></a><span data-ttu-id="c8967-213">ポリシー例 1 を作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-213">Create example policy 1</span></span>

<span data-ttu-id="c8967-214">この例では、以下のビジネス ケースにて使用可能なポリシー、*顧客 + モード* を作成します :</span><span class="sxs-lookup"><span data-stu-id="c8967-214">In this example, you will create a *Customer+Mode* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="c8967-215">このポリシーでは、顧客アカウント (*US-001*) と荷渡方法 (*Airwa-Air*) を照会します。</span><span class="sxs-lookup"><span data-stu-id="c8967-215">The policy will query for a specific customer account (*US-001*) and a specific mode of delivery (*Airwa-Air*).</span></span>
- <span data-ttu-id="c8967-216">未出荷に対する連結をオフにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-216">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="c8967-217">連結は注文 ID ごとに行われます。</span><span class="sxs-lookup"><span data-stu-id="c8967-217">Consolidation is done per order ID.</span></span> <span data-ttu-id="c8967-218">(つまり、注文や倉庫などにおける出荷ごとに別の出荷が存在することになります。)</span><span class="sxs-lookup"><span data-stu-id="c8967-218">(In other words, there will be separate shipments per order, warehouse, and so on.)</span></span>

<span data-ttu-id="c8967-219">このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8967-219">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="c8967-220">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-220">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c8967-221">**ポリシー タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-221">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c8967-222">アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:</span><span class="sxs-lookup"><span data-stu-id="c8967-222">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="c8967-223">**ポリシー名 :** *CustomerMode*</span><span class="sxs-lookup"><span data-stu-id="c8967-223">**Policy name:** *CustomerMode*</span></span>
    - <span data-ttu-id="c8967-224">**ポリシーの説明 :** *顧客アカウントと荷渡方法*</span><span class="sxs-lookup"><span data-stu-id="c8967-224">**Policy description:** *Customer account and mode of delivery*</span></span>

1. <span data-ttu-id="c8967-225">**未処理の出荷を含む連結** オプションは、 *いいえ* のままにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-225">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="c8967-226">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-226">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c8967-227">**連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-227">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="c8967-228">**追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-228">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="c8967-229">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-229">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c8967-230">[クエリの編集] ダイアログ ボックスのグリッド内の **範囲** タブで、**フィールド** のフィールドが、*顧客アカウント* に設定されている行を探し、その行の **基準** フィールドを *US-001* に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="c8967-230">In the query editor dialog box, on the **Range** tab, in the grid, find the row where the **Field** field is set to *Customer account*, and set the **Criteria** field for that row to *US-001*.</span></span>
1. <span data-ttu-id="c8967-231">**追加** を選択して、グリッドに以下の設定を持つ行を追加します:</span><span class="sxs-lookup"><span data-stu-id="c8967-231">Select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="c8967-232">**テーブル :** *注文明細行*</span><span class="sxs-lookup"><span data-stu-id="c8967-232">**Table:** *Order lines*</span></span>
    - <span data-ttu-id="c8967-233">**派生テーブル :** *注文明細行*</span><span class="sxs-lookup"><span data-stu-id="c8967-233">**Derived table:** *Order lines*</span></span>
    - <span data-ttu-id="c8967-234">**フィールド :** *荷渡方法*</span><span class="sxs-lookup"><span data-stu-id="c8967-234">**Field:** *Mode of delivery*</span></span>
    - <span data-ttu-id="c8967-235">**基準 :** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c8967-235">**Criteria:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c8967-236">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-236">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="c8967-237">このビジネス ケースでは、荷渡方法に *Airwa-Air* を利用している顧客 *US-001* の注文ラインが、注文をまたいで連結されることはありません。</span><span class="sxs-lookup"><span data-stu-id="c8967-237">For this business case, order lines for customer *US-001* that use the *Airwa-Air* mode of delivery won't be consolidated across orders.</span></span> <span data-ttu-id="c8967-238">このポリシーは、この顧客に対して他のすべての荷渡方法の出荷が連結されている場合に、順序どおりに使用されることを意図しています。</span><span class="sxs-lookup"><span data-stu-id="c8967-238">This policy is intended to be used first in a sequence, in cases where shipments for all other modes of delivery are consolidated for this customer.</span></span>

### <a name="create-example-policy-2"></a><span data-ttu-id="c8967-239">ポリシー例 2 を作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-239">Create example policy 2</span></span>

<span data-ttu-id="c8967-240">この例では、以下のビジネス ケースにて使用可能なポリシー、*危険物* を作成します :</span><span class="sxs-lookup"><span data-stu-id="c8967-240">In this example, you will create a *Hazardous goods* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="c8967-241">このポリシーでは、フィルターコード (*危険物*) と荷渡方法 (*Airwa-Air*) を照会します。</span><span class="sxs-lookup"><span data-stu-id="c8967-241">The policy will query for a specific filter code (*hazardous*) and a specific mode of delivery (*Airwa-Air*).</span></span>
- <span data-ttu-id="c8967-242">未出荷に対する連結をオンにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-242">Consolidation with open shipments is turned on.</span></span>
- <span data-ttu-id="c8967-243">連結は複数の注文を横断して行われます。</span><span class="sxs-lookup"><span data-stu-id="c8967-243">Consolidation is done across orders.</span></span> <span data-ttu-id="c8967-244">(アカウント、倉庫などには別々の出荷がありますが、クエリで指定された品目グループ内でのみ出荷されます。)</span><span class="sxs-lookup"><span data-stu-id="c8967-244">(In other words, there will be separate shipments per account, warehouse, and so on, but only within the item group that is specified in the query.)</span></span>

<span data-ttu-id="c8967-245">このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8967-245">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="c8967-246">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-246">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c8967-247">**ポリシー タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-247">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c8967-248">アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:</span><span class="sxs-lookup"><span data-stu-id="c8967-248">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="c8967-249">**ポリシー名 :** *品目のタイプ*</span><span class="sxs-lookup"><span data-stu-id="c8967-249">**Policy name:** *Item type*</span></span>
    - <span data-ttu-id="c8967-250">**ポリシーの説明 :** *複数の注文間で同じタイプの品目を統合します*</span><span class="sxs-lookup"><span data-stu-id="c8967-250">**Policy description:** *Consolidate the same type of item across orders*</span></span>

1. <span data-ttu-id="c8967-251">**未処理の出荷を含む連結** オプションは、 *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-251">Set the **Consolidate with open shipments** option to *Yes*.</span></span>
1. <span data-ttu-id="c8967-252">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-252">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c8967-253">**連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-253">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="c8967-254">**追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-254">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="c8967-255">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-255">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c8967-256">[クエリの編集] ダイアログボックスの **結合** タブで、ツリー **テーブル \> 積荷の詳細** を展開して選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-256">In the query editor dialog box, on the **Joins** tab, expand and select **Tables \> Load details** in the tree.</span></span>
1. <span data-ttu-id="c8967-257">**結合するテーブルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-257">Select **Add table join**.</span></span>
1. <span data-ttu-id="c8967-258">表示されたリレーション グリッドで、**関係性** フィールドが *倉庫品目番号 (品目番号)* に設定されている行を探して選択し、**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-258">In the grid of relations that appears, find and select the row where the **Relation** field is set to *Warehouse item number (Item number)*, and then select **Select**.</span></span> 
1. <span data-ttu-id="c8967-259">**範囲** タブで、 **追加** を選択して、グリッドに以下の設定を持つ行を追加します:</span><span class="sxs-lookup"><span data-stu-id="c8967-259">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="c8967-260">**テーブル :** *倉庫の品目番号*</span><span class="sxs-lookup"><span data-stu-id="c8967-260">**Table:** *Warehouse item number*</span></span>
    - <span data-ttu-id="c8967-261">**派生テーブル :** *倉庫の品目番号*</span><span class="sxs-lookup"><span data-stu-id="c8967-261">**Derived table:** *Warehouse item number*</span></span>
    - <span data-ttu-id="c8967-262">**フィールド :** *コード4*</span><span class="sxs-lookup"><span data-stu-id="c8967-262">**Field:** *Code 4*</span></span>
    - <span data-ttu-id="c8967-263">**基準 :** *可燃性*</span><span class="sxs-lookup"><span data-stu-id="c8967-263">**Criteria:** *Flammable*</span></span>

1. <span data-ttu-id="c8967-264">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-264">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="c8967-265">このビジネス ケースでは、品目に特定のフィルターコードを含むすべての注文明細行 (つまり、**code 4** フィールドが *可燃性* に設定されているフィルターコード ) は、複数の注文間で同じタイプの他の品目と統合されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-265">For this business case, all order lines where items have a specific filter code (that is, the filter code where the **Code 4** field is set to *Flammable*) will be consolidated with other items of the same type across orders.</span></span> <span data-ttu-id="c8967-266">同じアカウント、倉庫、品目グループが未出荷である場合は、新たな明細行が関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c8967-266">If there is an open shipment for the same account, warehouse, and group of items, the new lines will be attached to it.</span></span>

### <a name="create-example-policy-3"></a><span data-ttu-id="c8967-267">ポリシー例 3 を作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-267">Create example policy 3</span></span>

<span data-ttu-id="c8967-268">この例では、以下のビジネス ケースにて使用可能なポリシー、*顧客要求* を作成します :</span><span class="sxs-lookup"><span data-stu-id="c8967-268">In this example, you will create a *Customers' requirements* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="c8967-269">このポリシーでは、特定の顧客アカウントを照会します。</span><span class="sxs-lookup"><span data-stu-id="c8967-269">The policy will query for a specific customer account.</span></span>
- <span data-ttu-id="c8967-270">未出荷に対する連結をオンにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-270">Consolidation with open shipments is turned on.</span></span>
- <span data-ttu-id="c8967-271">連結は複数の注文間で行われますが、これは顧客の要求に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="c8967-271">Consolidation is done across orders but is based on customer requisitions.</span></span> <span data-ttu-id="c8967-272">(複数の注文が、同じ顧客要求番号と倉庫に基づいて出荷にグループ化されます。)</span><span class="sxs-lookup"><span data-stu-id="c8967-272">(In other words, multiple orders will be grouped into shipments, based on the same customer requisition number and warehouse.)</span></span>

<span data-ttu-id="c8967-273">このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8967-273">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="c8967-274">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-274">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c8967-275">**ポリシー タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-275">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c8967-276">アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:</span><span class="sxs-lookup"><span data-stu-id="c8967-276">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="c8967-277">**ポリシー名 :** *CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="c8967-277">**Policy name:** *CustomerOrderNo*</span></span>
    - <span data-ttu-id="c8967-278">**ポリシーの説明 :** *顧客の PO に基づいて明細行を連結する*</span><span class="sxs-lookup"><span data-stu-id="c8967-278">**Policy description:** *Consolidate lines based on customer PO*</span></span>

1. <span data-ttu-id="c8967-279">**未処理の出荷を含む連結** オプションは、 *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-279">Set the **Consolidate with open shipments** option to *Yes*.</span></span>
1. <span data-ttu-id="c8967-280">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-280">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c8967-281">**連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *顧客の要求* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-281">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Customer requisition*.</span></span>
1. <span data-ttu-id="c8967-282">**追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-282">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="c8967-283">**残りのフィールド** の一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-283">In the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="c8967-284">**追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-284">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="c8967-285">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-285">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c8967-286">[クエリの編集] ダイアログ ボックスの **範囲** タブで、**フィールド** のフィールドが、*顧客アカウント* に設定されている行を探し、その行の **基準** フィールドを *US-001* に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="c8967-286">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Customer account*, and set the **Criteria** field for that row to *US-001*.</span></span>
1. <span data-ttu-id="c8967-287">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-287">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="c8967-288">このビジネス ケースでは、販売注文にて同じ顧客要求番号を持つすべての注文明細行が、販売注文番号に関係なく、1つの出荷に連結されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-288">For this business case, all order lines where sales orders have the same customer requisition number will be consolidated into one shipment, regardless of the sales order number.</span></span> <span data-ttu-id="c8967-289">(顧客要求番号は顧客の発注書の \[PO\]番号として使用されます。) 同一のアカウント、倉庫、顧客要求で未処理の出荷がある場合は、新たな明細行が関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c8967-289">(The customer requisition number is used as the customer's purchase order \[PO\] number.) If there is an open shipment for the same account, warehouse, and customer requisition, the new lines will be attached to it.</span></span> <span data-ttu-id="c8967-290">このポリシーは、顧客が1日の内に同一の PO 番号を含む追加の注文明細行を複数回送信し、すべての明細行を 1 つの出荷にグループ化する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c8967-290">This policy can be used if the customer sends additional order lines that have the same PO number several times during a day and wants all the lines to be grouped into one shipment.</span></span> <span data-ttu-id="c8967-291">(例としては、単一の船荷証券と単一の梱包明細がある場合が考えられます。)</span><span class="sxs-lookup"><span data-stu-id="c8967-291">(In other words, there will be one bill of lading and one packing slip.)</span></span>

### <a name="create-example-policy-4"></a><span data-ttu-id="c8967-292">ポリシー例 4 を作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-292">Create example policy 4</span></span>

<span data-ttu-id="c8967-293">この例では、以下のビジネス ケースにて使用可能なポリシー、*顧客が許可する連結* を作成します :</span><span class="sxs-lookup"><span data-stu-id="c8967-293">In this example, you will create a *Customers allowing consolidation* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="c8967-294">このポリシーでは、特定のオーダープールにクエリを実行して、連結出荷を承認する顧客を識別します。</span><span class="sxs-lookup"><span data-stu-id="c8967-294">The policy will query for a specific order pool to identify customers who accept consolidated shipments.</span></span>
- <span data-ttu-id="c8967-295">未出荷に対する連結をオフにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-295">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="c8967-296">連結は、既定の連結注文ポリシーで選択されたフィールドを使用して、 (**倉庫へのリリースで出荷を連結する** チェック ボックスを複製する目的で) 複数の注文間で行われます。</span><span class="sxs-lookup"><span data-stu-id="c8967-296">Consolidation is done across orders using the fields selected by default CrossOrder policy (to replicate the previous **Consolidate shipment at release to warehouse** check box).</span></span>

- <span data-ttu-id="c8967-297">別のオーダー プールを選択することで、販売注文のルールを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="c8967-297">You can override the rule on a sales order by selecting a different order pool.</span></span>

<span data-ttu-id="c8967-298">このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8967-298">Follow these steps to create the shipment consolidation policy for this business case.</span></span>

1. <span data-ttu-id="c8967-299">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-299">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c8967-300">**ポリシー タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-300">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c8967-301">アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:</span><span class="sxs-lookup"><span data-stu-id="c8967-301">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="c8967-302">**ポリシー名 :** *オーダー プール*</span><span class="sxs-lookup"><span data-stu-id="c8967-302">**Policy name:** *Order pool*</span></span>
    - <span data-ttu-id="c8967-303">**ポリシーの説明 :** *オーダー プールに基づいて複数の注文を連結します*</span><span class="sxs-lookup"><span data-stu-id="c8967-303">**Policy description:** *Consolidate across orders based on order pool*</span></span>

1. <span data-ttu-id="c8967-304">**未処理の出荷を含む連結** オプションは、 *いいえ* のままにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-304">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="c8967-305">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-305">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c8967-306">**連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-306">On the **Consolidation fields** FastTab, in the **Remaining fields** list, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="c8967-307">**追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-307">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="c8967-308">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-308">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c8967-309">[クエリの編集] ダイアログ ボックスの **範囲** タブで、**追加** を選択して、グリッドに次の設定を持つ行を追加します:</span><span class="sxs-lookup"><span data-stu-id="c8967-309">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="c8967-310">**テーブル:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="c8967-310">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="c8967-311">**派生テーブル:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="c8967-311">**Derived table:** *Sales orders*</span></span>
    - <span data-ttu-id="c8967-312">**フィールド :** *プール*</span><span class="sxs-lookup"><span data-stu-id="c8967-312">**Field:** *Pool*</span></span>
    - <span data-ttu-id="c8967-313">**基準 :** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="c8967-313">**Criteria:** *ShipCons*</span></span>

1. <span data-ttu-id="c8967-314">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-314">Select **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="c8967-315">このビジネス ケースでは、販売注文が同じオーダー プールに属するすべての注文明細行が、同一のアカウント、倉庫、荷渡方法が使用する販売注文を通じて 1 つの出荷に連結されます。</span><span class="sxs-lookup"><span data-stu-id="c8967-315">For this business case, all order lines where sales orders belong to the same order pool will be consolidated into one shipment across sales orders for the same account, warehouse, and transportation mode of delivery.</span></span> <span data-ttu-id="c8967-316">オーダー プールの代わりに、その他の任意のフィールドを使用して顧客のグループを識別し、既定の販売注文ヘッダーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c8967-316">Instead of the order pool, you can use any other field to distinguish a group of customers and use the sales order header by default.</span></span> <span data-ttu-id="c8967-317">これは、倉庫ではなく顧客が連結の必要性を推進している場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c8967-317">You can use this approach if the customer, not the warehouse, is driving the need for consolidation.</span></span> <span data-ttu-id="c8967-318">(これまでの連結ロジックでは、倉庫が連結の必要性を推進していました。)</span><span class="sxs-lookup"><span data-stu-id="c8967-318">(In the earlier consolidation logic, the warehouse drove the need for consolidation.)</span></span>

### <a name="create-example-policy-5"></a><span data-ttu-id="c8967-319">ポリシー例 5 を作成する</span><span class="sxs-lookup"><span data-stu-id="c8967-319">Create example policy 5</span></span>

<span data-ttu-id="c8967-320">この例では、以下のビジネス ケースにて使用可能なポリシー、*倉庫が許可する連結* を作成します :</span><span class="sxs-lookup"><span data-stu-id="c8967-320">In this example, you will create a *Warehouses allowing consolidation* policy that can be used for the following business case:</span></span>

- <span data-ttu-id="c8967-321">このポリシーでは、特定のオーダープールにクエリを実行して、連結出荷が可能な倉庫を識別します。</span><span class="sxs-lookup"><span data-stu-id="c8967-321">The policy will query for a specific order pool to identify warehouses that can consolidate shipments.</span></span>
- <span data-ttu-id="c8967-322">未出荷に対する連結をオフにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-322">Consolidation with open shipments is turned off.</span></span>
- <span data-ttu-id="c8967-323">連結は、既定の連結注文ポリシーで選択されたフィールドを使用して、 (**倉庫へのリリースで出荷を連結する** チェック ボックスを複製する目的で) 複数の注文間で行われます。</span><span class="sxs-lookup"><span data-stu-id="c8967-323">Consolidation is done across orders using the fields selected by default CrossOrder policy (to replicate the previous **Consolidate shipment at release to warehouse** check box).</span></span>

<span data-ttu-id="c8967-324">通常、このビジネスケースでは、 [シナリオ 1](#scenario-1)で作成した既定のポリシーを使用して対処することができます。</span><span class="sxs-lookup"><span data-stu-id="c8967-324">Typically, this business case can be addressed by using the default policies that you created in [scenario 1](#scenario-1).</span></span> <span data-ttu-id="c8967-325">ただし、以下の手順で同様のポリシーを手動で作成することも可能です。</span><span class="sxs-lookup"><span data-stu-id="c8967-325">However, you can also manually create similar policies by following these steps.</span></span>

1. <span data-ttu-id="c8967-326">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-326">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c8967-327">**ポリシー タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-327">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c8967-328">アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:</span><span class="sxs-lookup"><span data-stu-id="c8967-328">On the Action Pane, select **New** to create a policy that has the following settings:</span></span>

    - <span data-ttu-id="c8967-329">**ポリシー名 :** *クロス オーダー*</span><span class="sxs-lookup"><span data-stu-id="c8967-329">**Policy name:** *Cross-order*</span></span>
    - <span data-ttu-id="c8967-330">**ポリシーの説明 :** *特定の倉庫のクロス オーダー連結*</span><span class="sxs-lookup"><span data-stu-id="c8967-330">**Policy description:** *Cross-order consolidation for specific warehouses*</span></span>

1. <span data-ttu-id="c8967-331">**未処理の出荷を含む連結** オプションは、 *いいえ* のままにします。</span><span class="sxs-lookup"><span data-stu-id="c8967-331">Leave the **Consolidate with open shipments** option set to *No*.</span></span>
1. <span data-ttu-id="c8967-332">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-332">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c8967-333">**連結フィールド** クイックタブの **残りのフィールド** フィールドで、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-333">On the **Consolidation fields** FastTab, in the **Remaining fields** field, select the row where the **Field name** field is set to *Mode of delivery*.</span></span>
1. <span data-ttu-id="c8967-334">**追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-334">Select the **Add** button ![Right arrow](media/forward-button.png) to move the field to the **Selected fields** list.</span></span>
1. <span data-ttu-id="c8967-335">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8967-335">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c8967-336">[クエリの編集] ダイアログ ボックスの **範囲** タブで、**フィールド** のフィールドが、*倉庫* に設定されている行を探し、その行の **基準** フィールドを *61, 63* に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="c8967-336">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Warehouse*, and set the **Criteria** field for that row to *61, 63*.</span></span>
1. <span data-ttu-id="c8967-337">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8967-337">Select **OK** to close the dialog box.</span></span>

### <a name="set-the-order"></a><span data-ttu-id="c8967-338">順序を設定する</span><span class="sxs-lookup"><span data-stu-id="c8967-338">Set the order</span></span>

<span data-ttu-id="c8967-339">以上ですべてのポリシーの作成が完了しました。続いて、ポリシーが適用される順序を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8967-339">Now that you've created all your policies, you must establish the order that they will be applied in.</span></span> <span data-ttu-id="c8967-340">以下の手順では、条件数が最も多いポリシーの優先度を高く評価する、ピラミッド型方式の設定例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c8967-340">To use a pyramid-like approach, where the policies that have the most conditions are evaluated as having the highest priority, follow these steps.</span></span>

1. <span data-ttu-id="c8967-341">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8967-341">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="c8967-342">**ポリシー タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="c8967-342">Set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="c8967-343">左の列に表示されているポリシーをそれぞれ選択し、続いてアクション ウィンドウの **上へ移動** または **下へ移動** ボタンを使用して、ポリシーを次の順序で配置します :</span><span class="sxs-lookup"><span data-stu-id="c8967-343">Select each policy that is listed in the left column, and then use the **Move up** and **Move down** buttons on the Action Pane to arrange the policies in the following order:</span></span>

    1. <span data-ttu-id="c8967-344">CustomerMode</span><span class="sxs-lookup"><span data-stu-id="c8967-344">CustomerMode</span></span>
    1. <span data-ttu-id="c8967-345">品目タイプ</span><span class="sxs-lookup"><span data-stu-id="c8967-345">Item type</span></span>
    1. <span data-ttu-id="c8967-346">CustomerOrderNo</span><span class="sxs-lookup"><span data-stu-id="c8967-346">CustomerOrderNo</span></span>
    1. <span data-ttu-id="c8967-347">注文管理グループ</span><span class="sxs-lookup"><span data-stu-id="c8967-347">Order pool</span></span>
    1. <span data-ttu-id="c8967-348">クロス オーダー</span><span class="sxs-lookup"><span data-stu-id="c8967-348">Cross-order</span></span>
    1. <span data-ttu-id="c8967-349">既定</span><span class="sxs-lookup"><span data-stu-id="c8967-349">Default</span></span>

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a><span data-ttu-id="c8967-350">出荷連結ポリシーの使用方法を示すシナリオ例</span><span class="sxs-lookup"><span data-stu-id="c8967-350">Example scenarios of how to use shipment consolidation policies</span></span>

<span data-ttu-id="c8967-351">次のシナリオでは、このトピックで作成した出荷連結ポリシーの使用例を説明しています。</span><span class="sxs-lookup"><span data-stu-id="c8967-351">The following scenarios illustrate how you could use the shipment consolidation policies that you created while reading this topic.</span></span> <span data-ttu-id="c8967-352">各シナリオでは、倉庫への自動リリースや手動リリース処理を行う過程で、出荷連結ポリシーを使用した出荷連結処理を行う方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="c8967-352">Each scenario walks you through a shipment consolidation process that uses shipment consolidation policies during automated or manual release to the warehouse:</span></span>

- <span data-ttu-id="c8967-353">シナリオ 1: [販売注文の自動リリースを使用して、出荷が倉庫にリリースされた場合に出荷を連結する](../warehousing/consolidate-shipments-automatic.md)</span><span class="sxs-lookup"><span data-stu-id="c8967-353">Scenario 1: [Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders](../warehousing/consolidate-shipments-automatic.md)</span></span>
- <span data-ttu-id="c8967-354">シナリオ 2: [出荷連結ポリシーが、[倉庫へのリリース] ページで上書きされている場合に出荷を連結する](../warehousing/consolidate-shipments-release-to-warehouse-override.md)</span><span class="sxs-lookup"><span data-stu-id="c8967-354">Scenario 2: [Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page](../warehousing/consolidate-shipments-release-to-warehouse-override.md)</span></span>
- <span data-ttu-id="c8967-355">シナリオ 3 - [積荷計画ワークベンチから倉庫へのリリース機能を使用して出荷を連結する](../warehousing/consolidate-shipments-load-planning-workbench.md)</span><span class="sxs-lookup"><span data-stu-id="c8967-355">Scenario 3: [Consolidate shipments by using Release to warehouse from the load planning workbench](../warehousing/consolidate-shipments-load-planning-workbench.md)</span></span>
- <span data-ttu-id="c8967-356">シナリオ 4: [出荷連結ワークベンチを使用して出荷を連結する](../warehousing/consolidate-shipments-manual-workbench.md)</span><span class="sxs-lookup"><span data-stu-id="c8967-356">Scenario 4: [Consolidate shipments by using the shipment consolidation workbench](../warehousing/consolidate-shipments-manual-workbench.md)</span></span>
- <span data-ttu-id="c8967-357">シナリオ 5: [出荷連結ページを使用して出荷を手動で連結する](../warehousing/consolidate-shipments-manual-form.md)</span><span class="sxs-lookup"><span data-stu-id="c8967-357">Scenario 5: [Consolidate shipments manually by using the Consolidate shipments page](../warehousing/consolidate-shipments-manual-form.md)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c8967-358">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c8967-358">Additional resources</span></span>

- [<span data-ttu-id="c8967-359">出荷連結ポリシー</span><span class="sxs-lookup"><span data-stu-id="c8967-359">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
