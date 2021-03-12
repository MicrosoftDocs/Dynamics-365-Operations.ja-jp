---
title: 倉庫へのリリースのルール
description: このトピックでは、倉庫にリリースする際に柔軟性を提供する、倉庫へのリリースのルール機能に関する情報を提供します。 部分的に引当済の注文明細行のリリースをシステムが許可するかどうかを制御する構成オプションを追加します。
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8c4775ca3f44486fd3cd557df49acd229048d186
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996176"
---
# <a name="release-to-warehouse-rule"></a><span data-ttu-id="024f2-104">倉庫へのリリースのルール</span><span class="sxs-lookup"><span data-stu-id="024f2-104">Release to warehouse rule</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="024f2-105">*倉庫へのリリースのルール* 機能は、倉庫へのリリース時の柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="024f2-105">The *Release to warehouse rule* feature provides flexibility during release to the warehouse.</span></span> <span data-ttu-id="024f2-106">各倉庫の構成オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="024f2-106">It adds a configuration option for each warehouse.</span></span> <span data-ttu-id="024f2-107">このオプションを使用して、その倉庫に対して部分的に引当済の注文明細行をリリースできるようにするかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="024f2-107">You can use this option to specify whether partially reserved order lines can be released for that warehouse.</span></span> <span data-ttu-id="024f2-108">この機能は、注文明細行の数量の一部が供給元に対してマークされているが、残りの部分は倉庫で処理できるような場合に、高度なクロスドッキング機能と連携して使用されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-108">The feature works together with advanced cross-docking functionality in situations where part of an order line quantity is marked against a supply source, but the remaining part can be processed in the warehouse.</span></span> <span data-ttu-id="024f2-109">したがって、明細行をリリースして、使用可能な在庫数量の倉庫処理を続行できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="024f2-109">Therefore, the line can be released so that warehouse processing of the available inventory quantity can continue.</span></span>

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a><span data-ttu-id="024f2-110">倉庫へのリリースのルール機能をオンにして初期化する</span><span class="sxs-lookup"><span data-stu-id="024f2-110">Turn on and initialize the Release to warehouse rule feature</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="024f2-111">機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="024f2-111">Turn on the feature</span></span>

<span data-ttu-id="024f2-112">*倉庫へのリリースのルール* 機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="024f2-112">Before you can use the *Warehouse release rule* feature, it must be turned on in your system.</span></span> <span data-ttu-id="024f2-113">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="024f2-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="024f2-114">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="024f2-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="024f2-115">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="024f2-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="024f2-116">**機能名 :** *倉庫へのリリースのルール*</span><span class="sxs-lookup"><span data-stu-id="024f2-116">**Feature name:** *Warehouse release rule*</span></span>

### <a name="initialize-the-feature"></a><span data-ttu-id="024f2-117">機能の初期化</span><span class="sxs-lookup"><span data-stu-id="024f2-117">Initialize the feature</span></span>

<span data-ttu-id="024f2-118">システムでこの機能が有効になったら、この機能を初期化して、すべての倉庫についてルールを正しい初期状態に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024f2-118">After the feature is turned on in your system, you must initialize it to set the rule to the correct initial state for all warehouses.</span></span>

- <span data-ttu-id="024f2-119">倉庫管理が有効になっていない倉庫では、ルールは **適用不可** に初期設定されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-119">For warehouses that aren't enabled for warehouse management, the rule is initially set to **Not applicable**.</span></span>
- <span data-ttu-id="024f2-120">倉庫管理が有効になっている倉庫では、ルールは **部分引当の許可** に初期設定されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-120">For warehouses that are enabled for warehouse management, the rule is initially set to **Allow partial reservation**</span></span>

<span data-ttu-id="024f2-121">機能を初期化し、すべての倉庫に倉庫へのリリースのルールを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="024f2-121">To initialize the feature and set the release to warehouse rule for all warehouses, follow these steps.</span></span>

1. <span data-ttu-id="024f2-122">**倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="024f2-122">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="024f2-123">**倉庫管理パラメーター** ページの **一般** タブの **会社情報** セクションで、**倉庫へのリリースを初期化** ルールのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-123">On the **Warehouse management parameters** page, on the **General** tab, in the **Company information** section, select the link for the **Initialize release to warehouse** rule.</span></span> <span data-ttu-id="024f2-124">(このリンクが表示されていない場合は、機能が有効になっていないか、既に初期化されています。)</span><span class="sxs-lookup"><span data-stu-id="024f2-124">(If this link isn't shown, either the feature isn't turned on or it has already been initialized.)</span></span>
1. <span data-ttu-id="024f2-125">アクションを確認するメッセージが表示されたら、**はい** を選択して機能を初期化します。</span><span class="sxs-lookup"><span data-stu-id="024f2-125">When you're prompted to confirm the action, select **Yes** to initialize the feature.</span></span>

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a><span data-ttu-id="024f2-126">各倉庫に倉庫へのリリースのルールを設定する</span><span class="sxs-lookup"><span data-stu-id="024f2-126">Set the release to warehouse rule for each warehouse</span></span>

<span data-ttu-id="024f2-127">この機能を有効にして初期化した後は、すべての倉庫の初期設定が前のセクションで説明したようになります。</span><span class="sxs-lookup"><span data-stu-id="024f2-127">After the feature is turned on and initialized, all your warehouses will have an initial setting, as described in the previous section.</span></span> <span data-ttu-id="024f2-128">この設定は、次の手順で個々の倉庫に対して変更できます。</span><span class="sxs-lookup"><span data-stu-id="024f2-128">You can change this setting for individual warehouses by following these steps.</span></span>

1. <span data-ttu-id="024f2-129">**倉庫管理 \> 設定 \> 倉庫 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="024f2-129">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="024f2-130">構成する倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-130">Select the warehouse to configure.</span></span>
1. <span data-ttu-id="024f2-131">**編集** を選択し、ページを編集モードにします。</span><span class="sxs-lookup"><span data-stu-id="024f2-131">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="024f2-132">**倉庫** クイック タブにある **引当** セクションの **在庫引当要件** フィールドで、注文の部分的なリリースを許可するかどうかが制御されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-132">On the **Warehouse** FastTab, in the **Reservations** section, the **Requirement for inventory reservation** field controls whether partial release of orders is allowed.</span></span> <span data-ttu-id="024f2-133">次の値からいずれか 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-133">Select one of the following values:</span></span>

    - <span data-ttu-id="024f2-134">**適用不可** – この機能を最初にオンにして初期化すると、この値は倉庫管理が有効になっていないすべての倉庫に自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="024f2-134">**Not applicable** – When the feature is first turned on and initialized, this value is automatically assigned to all warehouses that aren't enabled for warehouse management.</span></span> <span data-ttu-id="024f2-135">この値は変更できません。</span><span class="sxs-lookup"><span data-stu-id="024f2-135">It can't be changed.</span></span> <span data-ttu-id="024f2-136">この値は、倉庫管理が有効になっている倉庫では使用できません。</span><span class="sxs-lookup"><span data-stu-id="024f2-136">This value isn't available for warehouses that are enabled for warehouse management.</span></span>
    - <span data-ttu-id="024f2-137">**部分的な引当の許可** – 注文は、任意の数量が引当されたときにリリースできます。</span><span class="sxs-lookup"><span data-stu-id="024f2-137">**Allow partial reservation** – Orders can be released when any quantity is reserved.</span></span> <span data-ttu-id="024f2-138">引当されていない数量を高度なクロスドッキングとしてマークするかどうかを評価し、その数量を必要に応じてマークします。</span><span class="sxs-lookup"><span data-stu-id="024f2-138">The system will evaluate whether the unreserved quantity should be marked for advanced cross-docking and will mark that quantity as required.</span></span> <span data-ttu-id="024f2-139">マーキングが存在しない場合、引当済数量に対してのみ作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-139">If no marking exists, the system will create work only for the reserved quantity.</span></span> <span data-ttu-id="024f2-140">この機能を最初にオンにして初期化すると、この値は倉庫管理が有効になっているすべての倉庫に自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="024f2-140">When the feature is first turned on and initialized, this value is automatically assigned to all warehouses that are enabled for warehouse management.</span></span> <span data-ttu-id="024f2-141">この値は、倉庫管理が有効になっていない倉庫では使用できません。</span><span class="sxs-lookup"><span data-stu-id="024f2-141">This value isn't available for warehouses that aren't enabled for warehouse management.</span></span>
    - <span data-ttu-id="024f2-142">**完全引当を要求** – 注文は、数量全体が引当されている場合にのみリリースできます。</span><span class="sxs-lookup"><span data-stu-id="024f2-142">**Require full reservation** – Orders can be released only if the whole quantity is reserved.</span></span> <span data-ttu-id="024f2-143">合計数量が現物引当されているか、クロスドッキングが計画されている場合は、リリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="024f2-143">They can't be released if the total quantity isn't either physically reserved or planned for cross-docking.</span></span> <span data-ttu-id="024f2-144">この値は、倉庫管理が有効になっていない倉庫では使用できません。</span><span class="sxs-lookup"><span data-stu-id="024f2-144">This value isn't available for warehouses that aren't enabled for warehouse management.</span></span>

1. <span data-ttu-id="024f2-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-145">Select **Save**.</span></span>

## <a name="scenarios"></a><span data-ttu-id="024f2-146">シナリオ</span><span class="sxs-lookup"><span data-stu-id="024f2-146">Scenarios</span></span>

<span data-ttu-id="024f2-147">このセクションでは、この機能の動作と使用方法を学ぶための 2 つのシナリオを提供します。</span><span class="sxs-lookup"><span data-stu-id="024f2-147">This section provides two scenarios that you can work through to learn what the feature does and how to use it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="024f2-148">サンプル データを有効化する</span><span class="sxs-lookup"><span data-stu-id="024f2-148">Make sample data available</span></span>

<span data-ttu-id="024f2-149">指定されたサンプル レコードと値を使用してこれらのシナリオを実行するには、標準の[デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024f2-149">To work through these scenarios by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="024f2-150">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024f2-150">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="024f2-151">これらのシナリオは、実稼働システムで作業するときにこの機能を使用するためのガイダンスとして使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="024f2-151">You can also use these scenarios as guidance for the feature when you work on a production system.</span></span> <span data-ttu-id="024f2-152">ただし、その場合は、独自の値に置き換える必要があり、標準のデモ データが提供するいくつかのタイプの必要なレコードが不足している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="024f2-152">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a><span data-ttu-id="024f2-153">シナリオ 1: 完全リリースを必須にする (計画されたクロスドッキングなし)</span><span class="sxs-lookup"><span data-stu-id="024f2-153">Scenario 1: Require full release (no planned cross-docking)</span></span>

<span data-ttu-id="024f2-154">このシナリオでは、**完全引当を要求** するように設定されている倉庫に対して機能がどのように動作するかを示します。</span><span class="sxs-lookup"><span data-stu-id="024f2-154">This scenario shows how the feature works for warehouses that are set to **Require full reservation**.</span></span>

1. <span data-ttu-id="024f2-155">**倉庫管理 \> 設定 \> 倉庫 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="024f2-155">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="024f2-156">倉庫 _62_ については、このトピックで前述の [各倉庫に倉庫へのリリースのルールを設定する](#set-option-warehouse) セクションで説明したように、**在庫引当要件** フィールドを **完全引当を要求する** に設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-156">For warehouse _62_, set the **Requirement for inventory reservation** field to **Require full reservation**, as described in the [Set the release to warehouse rule for each warehouse](#set-option-warehouse) section earlier in this topic.</span></span>
1. <span data-ttu-id="024f2-157">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="024f2-157">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="024f2-158">**新規** を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="024f2-158">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="024f2-159">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-159">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="024f2-160">**顧客** クイック タブで、**顧客 ID** フィールドを _US-004_ に設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-160">On the **Customer** FastTab, set the **Customer account** field to _US-004_.</span></span>
    - <span data-ttu-id="024f2-161">**一般** クイック タブの **倉庫** フィールドを _62_ に設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-161">On the **General** FastTab, set the **Warehouse** field to _62_.</span></span>

1. <span data-ttu-id="024f2-162">**OK** を選択して新しい販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="024f2-162">Select **OK** to create the new sales order and close the dialog box.</span></span>
1. <span data-ttu-id="024f2-163">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="024f2-163">Your new sales order is opened.</span></span> <span data-ttu-id="024f2-164">**販売注文行** セクションのグリッドに空白行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="024f2-164">It includes an empty line in the grid in the **Sales order lines** section.</span></span> <span data-ttu-id="024f2-165">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-165">On this line, set the following values:</span></span>

    - <span data-ttu-id="024f2-166">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="024f2-166">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="024f2-167">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="024f2-167">**Quantity:** *2*</span></span>

1. <span data-ttu-id="024f2-168">**行の追加** を選択して新しい行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-168">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="024f2-169">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="024f2-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="024f2-170">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="024f2-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="024f2-171">最初の注文明細行を選択し、グリッドの上にある **在庫** メニューで、**引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-171">Select the first order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="024f2-172">**引当** ページで、**引当ロット** を選択して、選択した明細行の全数量を倉庫に引当します。</span><span class="sxs-lookup"><span data-stu-id="024f2-172">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="024f2-173">**引当** ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="024f2-173">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="024f2-174">2 番目の注文明細行を引当しないでください。</span><span class="sxs-lookup"><span data-stu-id="024f2-174">Don't reserve the second order line.</span></span>
1. <span data-ttu-id="024f2-175">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-175">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="024f2-176">次のエラー メッセージが表示されることに注意してください。「すべての数量を現物引当する必要があります。」</span><span class="sxs-lookup"><span data-stu-id="024f2-176">Notice that you receive the following error message: "The full quantity must be physically reserved."</span></span> <span data-ttu-id="024f2-177">したがって、注文に対する作業、出荷、または積荷がシステムによって作成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="024f2-177">Therefore, the system doesn't create any work, shipment, or load for the order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="024f2-178">2 つ目の明細行を部分的に引当した場合も、同じエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-178">You will receive the same error message if you partially reserve the second line.</span></span>

### <a name="scenario-2-allow-partial-release"></a><span data-ttu-id="024f2-179">シナリオ 2: 部分的なリリースの許可</span><span class="sxs-lookup"><span data-stu-id="024f2-179">Scenario 2: Allow partial release</span></span>

<span data-ttu-id="024f2-180">このシナリオでは、**部分的なリリースを許可** するように設定されている倉庫に対して機能がどのように動作するかを示します。</span><span class="sxs-lookup"><span data-stu-id="024f2-180">This scenario shows how the feature works for warehouses that are set to **Allow partial release**.</span></span>

1. <span data-ttu-id="024f2-181">**倉庫管理 \> 設定 \> 倉庫 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="024f2-181">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="024f2-182">倉庫 _62_ については、このトピックで前述の [各倉庫に倉庫へのリリースのルールを設定する](#set-option-warehouse) セクションで説明したように、**在庫引当要件** フィールドを **部分的なリリースを許可する** に設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-182">For warehouse _62_, set the **Requirement for inventory reservation** field to **Allow partial reservation**, as described in the [Set the release to warehouse rule for each warehouse](#set-option-warehouse) section earlier in this topic.</span></span>
1. <span data-ttu-id="024f2-183">[前のシナリオ](#scenario1) のように、**販売とマーケティング \> 販売注文 \> すべての販売注文** に移動して、倉庫 _62_ から顧客アカウント _US-004_ に販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="024f2-183">As you did in the [previous scenario](#scenario1), go to **Sales and marketing \> Sales orders \> All sales orders**, and create a sales order for customer account _US-004_ from warehouse _62_.</span></span> <span data-ttu-id="024f2-184">の 2 つの注文明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="024f2-184">Add the following two order lines:</span></span>

    - <span data-ttu-id="024f2-185">**明細行 1:** **品目番号** フィールドを _A0001_ に、**数量** フィールドを _2_ に、**単位** フィールドを _Pcs_ に設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-185">**Line 1:** Set the **Item number** field to _A0001_, the **Quantity** field to _2_, and the **Unit** field to _Pcs_.</span></span>
    - <span data-ttu-id="024f2-186">**明細行 2:** **品目番号** フィールドを _A0002_ に、**数量** フィールドを _2_ に、**単位** フィールドを _Pcs_ に設定します。</span><span class="sxs-lookup"><span data-stu-id="024f2-186">**Line 2:** Set the **Item number** field to _A0002_, the **Quantity** field to _2_, and the **Unit** field to _Pcs_.</span></span>

1. <span data-ttu-id="024f2-187">[前のシナリオ](#scenario1) のように、注文明細行 1 に対して全数量を引当ますが、注文明細行 2 は引当しません。</span><span class="sxs-lookup"><span data-stu-id="024f2-187">As you did in the [previous scenario](#scenario1), reserve the full quantity for order line 1, but don't reserve order line 2.</span></span>
1. <span data-ttu-id="024f2-188">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-188">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="024f2-189">この時点では、エラー メッセージは表示されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="024f2-189">Notice that you don't receive an error message this time.</span></span> <span data-ttu-id="024f2-190">代わりに、必要に応じて作業、出荷、および積荷が作成され、結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-190">Instead, the system creates work, shipments, and loads as required, and shows the results.</span></span>
1. <span data-ttu-id="024f2-191">出荷、積荷、および作業に関する情報を表示するには、グリッドの上にある **倉庫** メニューのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="024f2-191">To view the shipment, load, and work information, use the options on the **Warehouse** menu above the grid:</span></span>

    - <span data-ttu-id="024f2-192">**明細行 1:** **出荷詳細**、**積荷の詳細**、および **作業の詳細** の 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="024f2-192">**Line 1:** Three options are available: **Shipment details**, **Load details**, and **Work details**.</span></span> <span data-ttu-id="024f2-193">注文が倉庫にリリースされたときに作成された出荷、積荷、および作業の詳細を表示するには、各オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="024f2-193">Select each option to view the details of the shipment, load, and work that were created when the order was released to the warehouse.</span></span>
    - <span data-ttu-id="024f2-194">**明細行 2:** **作業の詳細** オプションのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="024f2-194">**Line 2:** Only the **Work details** option is available.</span></span> <span data-ttu-id="024f2-195">選択すると、在庫が引当されていないため、作業が作成されていないことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="024f2-195">Select it, and notice that no work has been created, because no inventory was reserved.</span></span> <span data-ttu-id="024f2-196">したがって、出荷または積荷は作成されていません。</span><span class="sxs-lookup"><span data-stu-id="024f2-196">Therefore, no shipment or load was created either.</span></span>

> [!NOTE]
> <span data-ttu-id="024f2-197">2 つ目の明細行が部分的に引当されている場合は、同じ結果が予想されます。</span><span class="sxs-lookup"><span data-stu-id="024f2-197">The same result is expected when the second line is partially reserved.</span></span> <span data-ttu-id="024f2-198">この場合、引当済の明細行の数量に対して作業が作成されますが、引当されていない数量に対しては作成されません。</span><span class="sxs-lookup"><span data-stu-id="024f2-198">In this case, work will be created for the reserved line quantity but not for the unreserved quantity.</span></span>
