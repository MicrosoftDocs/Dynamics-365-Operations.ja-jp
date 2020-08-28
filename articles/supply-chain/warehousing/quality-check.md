---
title: 品質チェック
description: このトピックでは、品質確認機能に関して説明します。 この機能により、倉庫の作業者は入庫ドック エリアに品目を受領する間に、品質を確認することができます。
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate,WHSWorkClass,WHSWorkTemplateTable.WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 44a4694281f3dd53581c9d8245a0105b37b2b155
ms.sourcegitcommit: 7dc2ff9461c310324937bea2fc160ff056fefd8a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686360"
---
# <a name="quality-check"></a><span data-ttu-id="bfc42-104">品質チェック</span><span class="sxs-lookup"><span data-stu-id="bfc42-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfc42-105">この *品質チェック* 機能により、倉庫の作業者は入庫ドック エリアに品目を受領しながら、品質の迅速なスポット チェックをすることができます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="bfc42-106">これらのスポット チェックは、作業者がその品目の梱包やその他簡単に認識できる部分を検査するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="bfc42-107">この機能により、作業者は、在庫をプットアウェイ場所に保管する前に、何らかの明らかな欠陥や破損があるかどうかを簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="bfc42-108">この機能は、標準の品質チェック プロセスの代わりとなります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="bfc42-109">これは、より高い柔軟性と迅速な処理を実現します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="bfc42-110">この機能を使用すると、着荷と品質チェックが次の方法で行われます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="bfc42-111">荷物が到着すると、倉庫の作業者が着荷を登録します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="bfc42-112">この作業者は、ライセンス プレートをスキャンして場所を登録することもできます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="bfc42-113">作業者は簡易的な品質チェックをおこない、そのライセンス プレートの結果 (合格または不合格) を記録します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="bfc42-114">次のいずれかのアクションが発生します:</span><span class="sxs-lookup"><span data-stu-id="bfc42-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="bfc42-115">品質チェックが合格した場合は、ライセンス プレートは通常通り受領され、入荷場所へとガイドされます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="bfc42-116">品質チェックが不合格となった場合は、そのライセンス プレートは拒否され、さらなる検査のために既存のプットアウェイ作業が別の場所にリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="bfc42-117">新しい品質指示が作成されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-117">A new quality order is created.</span></span> <span data-ttu-id="bfc42-118">不合格となった品質チェックから作成された品質指示を表示するには、**在庫管理 \>定期タスク \> 品質管理 \> 品質指示** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="bfc42-119">また、スキャンされたすべてのライセンス プレートが直ちに品質チェック場所へと迂回するように、このプロセスを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="bfc42-120">品質チェック機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="bfc42-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="bfc42-121">*品質チェック* 機能を使用するには、自分のシステムで有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="bfc42-122">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bfc42-123">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="bfc42-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bfc42-124">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="bfc42-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bfc42-125">**機能名:** *品質チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="bfc42-126">シナリオ例の機能の設定</span><span class="sxs-lookup"><span data-stu-id="bfc42-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="bfc42-127">このセクションでは、*品質チェック* 機能の設定方法と、本トピックの後で紹介するシナリオ例にサンプル データを準備する方法を示すガイドラインと例を説明します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="bfc42-128">サンプル データを有効化する</span><span class="sxs-lookup"><span data-stu-id="bfc42-128">Make sample data available</span></span>

<span data-ttu-id="bfc42-129">ここで指定されたサンプル レコードと値を使用して [シナリオ例](#example-scenario) を実行するには、標準の [デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bfc42-130">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="bfc42-131">品質チェック テンプレート</span><span class="sxs-lookup"><span data-stu-id="bfc42-131">Quality check template</span></span>

<span data-ttu-id="bfc42-132">品質チェック テンプレートでは、受領時に品質の簡易スポット チェックを実行するためのルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="bfc42-133">**倉庫管理 \> 設定 \> 作業 \> 品質チェック テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="bfc42-134">**新規** を選択して、グリッドにテンプレートを追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="bfc42-135">新規テンプレートを定義するために次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="bfc42-136">**品質チェック テンプレート名:** *ドック チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="bfc42-137">このテンプレートに適用されるポリシーを特定する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="bfc42-138">**受け入れポリシー:** *ユーザーに確認する*</span><span class="sxs-lookup"><span data-stu-id="bfc42-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="bfc42-139">作業の処理中にユーザーに在庫の品質の承認か否認を確認するメッセージを表示するか、品質を自動的に否認するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="bfc42-140">使用できるオプションは、*自動的に却下する* と *ユーザーに確認する* です。</span><span class="sxs-lookup"><span data-stu-id="bfc42-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="bfc42-141">**品質処理ポリシー:** *品質指示の作成*</span><span class="sxs-lookup"><span data-stu-id="bfc42-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="bfc42-142">在庫の品質を却下する際に使用すべきポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="bfc42-143">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-143">The following options are available:</span></span>

        - <span data-ttu-id="bfc42-144">*作業のみ作成* - 在庫の移動を促進するための作業のみを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="bfc42-145">*品質指示の作成* - 品質テストを促進するための品質指示を作成します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="bfc42-146">**テストグループ:** *エンクロージャ*</span><span class="sxs-lookup"><span data-stu-id="bfc42-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="bfc42-147">作成された品質指示で使用するテスト グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="bfc42-148">テストグループは、**在庫管理** モジュールで設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="bfc42-149">テスト グループに対して **破壊テキスト** オプションはオフのままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="bfc42-150">このオプションは、テスト グループ内のテストの一環としてサンプルを破壊するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="bfc42-151">破壊試験を使用する場合、そのアイテムに対して品質指示を作成する際にシステムは在庫トランザクションを生成します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="bfc42-152">新しい在庫トランザクションは、テスト数量の在庫の減少を予測します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="bfc42-153">品質指示が検証ステップによって完了すると在庫が減少します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="bfc42-154">在庫トランザクションは品質指示として識別されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="bfc42-155">作業クラス - 品質チェック</span><span class="sxs-lookup"><span data-stu-id="bfc42-155">Work class – Quality check</span></span>

<span data-ttu-id="bfc42-156">作業クラスは、倉庫作業者がモバイル デバイスで処理できる作業指示書明細行の種類を指示または制限するために使用します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="bfc42-157">**倉庫管理 \> 設定 \> 作業 \> 作業クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="bfc42-158">**新規** を選択して、作業クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="bfc42-159">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="bfc42-160">**作業クラス ID:** *QC チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bfc42-161">作業クラスを特定する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="bfc42-162">**説明:** *QC チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="bfc42-163">作業クラスの使用目的を示す簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="bfc42-164">**作業指示のタイプ:** *品質チェックの品質*</span><span class="sxs-lookup"><span data-stu-id="bfc42-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="bfc42-165">作業クラスによって作成される作業指示書のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="bfc42-166">品質管理作業を設定する場合は、常に *品質チェックでの品質* を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="bfc42-167">**有効なプット場所のタイプ** クイック タブで、**場所のタイプ** フィールドを空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="bfc42-168">場所のタイプを選択した場合は、アイテムをピッキングした後にプットできる場所を制限します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="bfc42-169">このフィールドは、場所ディレクティブがその場所を解決しようとする場合、または倉庫作業者がモバイル デバイスのメニュー項目に手動で場所を特定する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="bfc42-170">作業クラスとその作成方法の詳細については、[作業クラスの作成](tasks/create-work-class.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfc42-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="bfc42-171">作業テンプレート</span><span class="sxs-lookup"><span data-stu-id="bfc42-171">Work template</span></span>

<span data-ttu-id="bfc42-172">作業テンプレート ページで、倉庫で実行しなければならない作業を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="bfc42-173">通常、倉庫での作業は、倉庫作業者が 1 つの場所の手持在庫をピッキングし、次にピッキングした在庫を別の場所にプットするという、1 ペアのアクションから構成されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="bfc42-174">品質管理の作業テンプレートは、品質チェックを実行するための作業を定義します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="bfc42-175">発注書</span><span class="sxs-lookup"><span data-stu-id="bfc42-175">Purchase orders</span></span>

1. <span data-ttu-id="bfc42-176">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="bfc42-177">ヘッダーでは、**作業指示書のタイプ** フィールドを *発注書* に設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="bfc42-178">アクション ウィンドウで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bfc42-179">品質チェック手順を含めなければなならい作業テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="bfc42-180">**概要** セクションの **作業テンプレート** フィールドで、*51 PO 受入* を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="bfc42-181">**作業テンプレートの詳細** セクションには、グリッドに 2 つの既存の明細行 (*ピッキング* 用が 1 行と *プット* 用が 1 行) ありますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="bfc42-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="bfc42-182">**作業テンプレートの詳細** セクションで、**新規** を選択して品質管理の行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="bfc42-183">新しい明細行の **行番号** フィールドが *3* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="bfc42-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="bfc42-184">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-184">On the new line, set the following values.</span></span> <span data-ttu-id="bfc42-185">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bfc42-186">**作業タイプ:** *品質チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="bfc42-187">**作業クラス ID:** *購入*</span><span class="sxs-lookup"><span data-stu-id="bfc42-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="bfc42-188">**品質チェック テンプレート名:** *ドック チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="bfc42-189">作業クラスの固有 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="bfc42-190">モバイル デバイスのメニュー項目と、それらのメニュー項目で処理できる作業タイプをコンフィギュレーションするには、この値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="bfc42-191">アクション ウィンドウで、**保存** を選択して今までの作業を保存します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="bfc42-192">"無効 - 品質チェックはピックの後に直接取得する必要があります" という内容のメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="bfc42-193">したがって、追加した明細行の **行番号** の値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="bfc42-194">新しい明細行の **行番号** の値を変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bfc42-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="bfc42-195">**作業テンプレートの詳細** セクションで、**作業タイプ** フィールドが *品質チェック* に設定されている明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="bfc42-196">**上へ移動** または **下へ移動** をクリックして、*品質チェック* 行を *ピック* 行の後になるように移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="bfc42-197">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="bfc42-198">品質チェックの品質</span><span class="sxs-lookup"><span data-stu-id="bfc42-198">Quality in quality check</span></span>

<span data-ttu-id="bfc42-199">次に、品質チェック用の作業テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="bfc42-200">**作業テンプレート** ページのヘッダーで、**作業指示タイプ** フィールドの値を *品質チェックの品質* に変更します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="bfc42-201">アクション ウィンドウで、**新規** を選択して、行を **概要** セクションのグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="bfc42-202">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bfc42-203">**作業テンプレート:** *51 品質チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="bfc42-204">テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="bfc42-205">**作業テンプレートの説明:** *51 品質チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="bfc42-206">アクション ウィンドウで、**保存** を選択して、**作業テンプレートの詳細** セクションを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bfc42-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="bfc42-207">新規テンプレートがまだ **概要** セクションで選択されている場合に、**新規** を **作業テンプレートの詳細** セクションで選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="bfc42-208">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bfc42-209">**作業タイプ:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="bfc42-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="bfc42-210">**作業クラス ID:** *QC チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bfc42-211">品質管理作業のために以前に作成した [作業クラス](#work-class) の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="bfc42-212">**作業テンプレートの詳細** セクションで、**新規** を再度選択して別の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="bfc42-213">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bfc42-214">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="bfc42-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bfc42-215">**作業クラス ID:** *QC チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bfc42-216">品質管理作業のために以前に作成した [作業クラス](#work-class) の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="bfc42-217">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="bfc42-218">作業テンプレートの詳細については、[作業テンプレートと場所ディレクティブを使用して倉庫作業を管理する](control-warehouse-location-directives.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfc42-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="bfc42-219">場所ディレクティブ – 品質エラー</span><span class="sxs-lookup"><span data-stu-id="bfc42-219">Location directive – Quality failures</span></span>

<span data-ttu-id="bfc42-220">場所ディレクティブは、棚卸資産移動のピッキングとプットの場所を識別するのにに役立つルールです。</span><span class="sxs-lookup"><span data-stu-id="bfc42-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="bfc42-221">たとえば、販売注文トランザクションでは、場所ディレクティブが品目がピッキングされる場所とピッキングされた品目がプットされる場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="bfc42-222">不合格だった品質チェックをどのように処理するかを定義するには、場所ディレクティブのルールをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="bfc42-223">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="bfc42-224">左ウィンドウで、**作業指示タイプ** フィールドを *発注書* に設定し、そのタイプの場所ディレクティブで作業をします。</span><span class="sxs-lookup"><span data-stu-id="bfc42-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="bfc42-225">アクション ウィンドウで、**新規** を選択して、品質チェックの場所ディレクティブを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="bfc42-226">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="bfc42-227">**シーケンス番号:** 規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="bfc42-228">**名前:** *51 から品質*</span><span class="sxs-lookup"><span data-stu-id="bfc42-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="bfc42-229">**場所のディレクティブ** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="bfc42-230">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bfc42-231">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="bfc42-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bfc42-232">**サイト:** *5*</span><span class="sxs-lookup"><span data-stu-id="bfc42-232">**Site:** *5*</span></span>
    - <span data-ttu-id="bfc42-233">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="bfc42-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bfc42-234">アクション ウィンドウで、**保存** を選択して、場所ディレクティブを保存し、**明細行** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bfc42-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="bfc42-235">**明細行**クイック タブで、**新規**を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bfc42-236">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-236">On the new line, set the following values.</span></span> <span data-ttu-id="bfc42-237">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bfc42-238">**開始数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="bfc42-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="bfc42-239">**上限数量:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="bfc42-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="bfc42-240">アクション ウィンドウで、**保存** を選択して、新しい明細行を保存して、**場所ディレクティブ アクション** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bfc42-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="bfc42-241">新しい明細行が **明細行** クイックタブでまだ選択されている間に、**新規** を **場所ディレクティブのアクション** クイック タブ上で選択すると、そのグリッドに行を追加して、明細行に対するアクションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="bfc42-242">新しい行で、**名前** フィールドを *品質* に設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="bfc42-243">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="bfc42-244">アクション ウィンドウで、**保存** を選択すると、**場所ディレクティブ アクション** クイック タブの **クエリの編集** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="bfc42-245">追加した明細が **場所’ディレクティブ アクション** クイックタブで選択されたままの状態で、**クエリの編集** を選択すると、ダイアログ ボックスが開き、アクションのクエリを編集できます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="bfc42-246">**範囲** タブで、**追加** を選択してクエリに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="bfc42-247">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bfc42-248">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="bfc42-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="bfc42-249">**派生テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="bfc42-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="bfc42-250">**フィールド :** *場所*</span><span class="sxs-lookup"><span data-stu-id="bfc42-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="bfc42-251">**基準:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="bfc42-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="bfc42-252">*QMS* 場所は、品質のための倉庫の場所です。</span><span class="sxs-lookup"><span data-stu-id="bfc42-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="bfc42-253">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="bfc42-254">次に、倉庫 *51* の発注書の場所ディレクティブの順序を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="bfc42-255">新規 *51 から品質* 場所ディレクティブに保存し、ページを更新して、リストの場所ディレクティブを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="bfc42-256">次に、アクションウィンドウの **上へ移動** または **下へ移動** ボタンを使用して、倉庫 *51* の場所ディレクティブを次の順序で配置します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="bfc42-257">(**上へ移動** または **下へ移動** に移動する前に、一覧で場所ディレクティブを選択する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="bfc42-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="bfc42-258">51 から品質</span><span class="sxs-lookup"><span data-stu-id="bfc42-258">51 To Quality</span></span>
    2. <span data-ttu-id="bfc42-259">51 発注書ダイレクト</span><span class="sxs-lookup"><span data-stu-id="bfc42-259">51 PO Direct</span></span>
    3. <span data-ttu-id="bfc42-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="bfc42-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="bfc42-261">モバイル デバイスのメニュー品目</span><span class="sxs-lookup"><span data-stu-id="bfc42-261">Mobile device menu items</span></span>

<span data-ttu-id="bfc42-262">メニュー項目をコンフィギュレーションして、モバイル デバイスで **品質チェック** 機能を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bfc42-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="bfc42-263">購入プットアウェイ</span><span class="sxs-lookup"><span data-stu-id="bfc42-263">Purchase putaway</span></span>

1. <span data-ttu-id="bfc42-264">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bfc42-265">リストで、**購入品のプットアウェイ** メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="bfc42-266">アクション ウィンドウで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bfc42-267">**作業クラス** セクションで、**新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="bfc42-268">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="bfc42-269">**作業クラス ID:** *QC チェック*</span><span class="sxs-lookup"><span data-stu-id="bfc42-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="bfc42-270">品質管理作業に以前に作成した [作業クラス](#work-class) の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="bfc42-271">**作業指示のタイプ:** *品質チェックの品質*</span><span class="sxs-lookup"><span data-stu-id="bfc42-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="bfc42-272">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="bfc42-273">発注書明細行受取</span><span class="sxs-lookup"><span data-stu-id="bfc42-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="bfc42-274">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bfc42-275">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bfc42-276">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="bfc42-277">**メニュー項目名 :** *発注書明細行受取*</span><span class="sxs-lookup"><span data-stu-id="bfc42-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="bfc42-278">**タイトル :** *発注書明細行受取*</span><span class="sxs-lookup"><span data-stu-id="bfc42-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="bfc42-279">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="bfc42-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="bfc42-280">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="bfc42-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="bfc42-281">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="bfc42-282">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="bfc42-283">**作業の作成プロセス:** *発注書明細行の入荷とプットアウェイ*</span><span class="sxs-lookup"><span data-stu-id="bfc42-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="bfc42-284">**ライセンスプレートの生成:** *はい*</span><span class="sxs-lookup"><span data-stu-id="bfc42-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="bfc42-285">**作業テンプレート:** *51 PO Receipt*</span><span class="sxs-lookup"><span data-stu-id="bfc42-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="bfc42-286">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="bfc42-287">モバイル デバイス メニューへのメニュー項目の追加</span><span class="sxs-lookup"><span data-stu-id="bfc42-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="bfc42-288">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="bfc42-289">左ウィンドウで、**入庫** メニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="bfc42-290">アクション ウィンドウで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="bfc42-291">**使用可能なメニューとメニュー項目** 列で、新規 **発注書明細行の入荷** メニュー項目を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="bfc42-292">右矢印ボタンを選択して、**発注書明細行の入荷** を **メニュー構造** 列に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="bfc42-293">**メニュー構造** 列で、**発注書明細行の入荷** を選択し、上矢印または下矢印ボタンをクリックして、モバイル デバイス メニューで目的の位置にメニュー項目を移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="bfc42-294">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="bfc42-295">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="bfc42-295">Example scenario</span></span>

<span data-ttu-id="bfc42-296">上記で説明したサンプル データをすべて入手して設定したら、このシナリオを使用して *品質チェック* 機能を試すことができます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="bfc42-297">このシナリオに示されている値は、標準のデモデータで作業していて、**USMF** 法人を選択し、このトピックで既に説明したサンプル レコードを準備していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="bfc42-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="bfc42-298">このシナリオは、製品の設定で機能を使用する方法を示す例としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="bfc42-299">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="bfc42-299">Create a purchase order</span></span>

1. <span data-ttu-id="bfc42-300">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="bfc42-301">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bfc42-302">**発注書の作成**ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bfc42-303">**仕入先勘定 :** *104*</span><span class="sxs-lookup"><span data-stu-id="bfc42-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="bfc42-304">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="bfc42-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bfc42-305">**OK** を選択して新しい発注書を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="bfc42-306">**発注書明細行** クイック タブには、グリッドに新規の空欄の明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="bfc42-307">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="bfc42-308">**品目番号:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bfc42-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="bfc42-309">**数量:** *3*</span><span class="sxs-lookup"><span data-stu-id="bfc42-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="bfc42-310">**ユニット:** *PL*</span><span class="sxs-lookup"><span data-stu-id="bfc42-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="bfc42-311">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="bfc42-312">品質チェック入荷のプロセス</span><span class="sxs-lookup"><span data-stu-id="bfc42-312">Process quality check receiving</span></span>

<span data-ttu-id="bfc42-313">作成された発注書は、**発注書明細行の入荷** メニュー項目と *品質チェック機能* 機能を使用して受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="bfc42-314">受領パレット 1</span><span class="sxs-lookup"><span data-stu-id="bfc42-314">Receive pallet 1</span></span>

1. <span data-ttu-id="bfc42-315">倉庫 *51* のユーザーとして倉庫アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="bfc42-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="bfc42-316">(ユーザー ID として *51* を、パスワードとして *1* を入力します。)</span><span class="sxs-lookup"><span data-stu-id="bfc42-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="bfc42-317">**入庫 \> 発注書明細行の入荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="bfc42-318">**PONUM** フィールドに発注書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="bfc42-319">発注書番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="bfc42-320">**LINENUM** フィールドに、受領した発注書明細行の番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="bfc42-321">このシナリオではこの注文には 1 行しかないので、*1* を入荷ステップごとに **LINENUM** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="bfc42-322">行番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-322">Confirm the line number.</span></span>
1. <span data-ttu-id="bfc42-323">**数量** フィールドに、入荷した数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="bfc42-324">このシナリオでは、発注書は 3 パレット(*PL*) の注文であり、3 つの入荷ステップがあるので、各入荷ステップに対して *1* を **数量** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="bfc42-325">数量を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-325">Confirm the quantity.</span></span>

    <span data-ttu-id="bfc42-326">表示される **品質チェック** ページには入力フィールドがありません。</span><span class="sxs-lookup"><span data-stu-id="bfc42-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="bfc42-327">一番下にある確認 (チェック マーク) ボタンと、上部にあるメニューボタン (**≡**) のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="bfc42-328">(メニュー ボタンは、ハンバーガーまたはハンバーガー ボタンと呼ばれることがあります。) 品質チェック プロセスを早めるために、パレットが品質チェックに合格した場合、ユーザーは **品質チェック** ページを確認するだけです。</span><span class="sxs-lookup"><span data-stu-id="bfc42-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="bfc42-329">![品質チェック ページ](media/quality-check.png "品質チェック ページ")</span><span class="sxs-lookup"><span data-stu-id="bfc42-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="bfc42-330">[確認] ボタンをクリックして、1 行目からパレット 1 の品質チェックを渡します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="bfc42-331">次のプット作業の詳細を表示する **発注書: プット** ページ:</span><span class="sxs-lookup"><span data-stu-id="bfc42-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bfc42-332">**LOC:** システムが決定した場所</span><span class="sxs-lookup"><span data-stu-id="bfc42-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="bfc42-333">この場所は、発注書の受入に対して指定されたプットアウェイです。</span><span class="sxs-lookup"><span data-stu-id="bfc42-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="bfc42-334">**LP:** システムが生成したライセンス プレート ID</span><span class="sxs-lookup"><span data-stu-id="bfc42-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bfc42-335">**品目:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bfc42-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bfc42-336">**数量:** *1 PL: 各 100 個*</span><span class="sxs-lookup"><span data-stu-id="bfc42-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bfc42-337">アイテムの説明も表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-337">The item description is also shown.</span></span>

1. <span data-ttu-id="bfc42-338">プットアウェイ作業を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="bfc42-339">発注書明細行入荷の **タスク** ページで、"作業が完了しました" メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bfc42-340">**LINENUM** フィールドは、次のパレットの入荷を開始できるようにするために用意されています。</span><span class="sxs-lookup"><span data-stu-id="bfc42-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="bfc42-341">入荷パレット 2</span><span class="sxs-lookup"><span data-stu-id="bfc42-341">Receive pallet 2</span></span>

<span data-ttu-id="bfc42-342">このシナリオでは、パレット 2 は拒否されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="bfc42-343">**LINENUM** フィールドに *1* を入力し、行番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="bfc42-344">**数量** フィールドが使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bfc42-344">The **QTY** field is now available.</span></span> <span data-ttu-id="bfc42-345">*1* を入力し、数量を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="bfc42-346">**品質チェック** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-346">The **Quality check** page appears.</span></span> <span data-ttu-id="bfc42-347">この受領で、このパレットは品質で拒否され、*QMS* 品質の場所にプットされます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="bfc42-348">ページの上部にあるメニューボタン (**≡**) を選択し、メニューで **却下** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="bfc42-349">表示される **タスク** ページに、**QMS** を *プット* 場所として入力して、パレットを更なる検査へと送ります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="bfc42-350">表示された **品質チェックの品質: プット** ページがプット作業の詳細を表示します:</span><span class="sxs-lookup"><span data-stu-id="bfc42-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bfc42-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="bfc42-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="bfc42-352">この場所は、拒否された品質の入荷に対する指定されたプットアウェイです。</span><span class="sxs-lookup"><span data-stu-id="bfc42-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="bfc42-353">**LP:** システムが生成したライセンス プレート ID</span><span class="sxs-lookup"><span data-stu-id="bfc42-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bfc42-354">**品目:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bfc42-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bfc42-355">**数量:** *1 PL: 各 100 個*</span><span class="sxs-lookup"><span data-stu-id="bfc42-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bfc42-356">アイテムの説明も表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-356">The item description is also shown.</span></span>

1. <span data-ttu-id="bfc42-357">プットアウェイ作業を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="bfc42-358">発注書明細行入荷の **タスク** ページで、"作業が完了しました" メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bfc42-359">**LINENUM** フィールドは、次のパレットの入荷を開始できるようにするために用意されています。</span><span class="sxs-lookup"><span data-stu-id="bfc42-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="bfc42-360">これで、品質チェックが完了し、否認したパレットの品質指示が作成されました。</span><span class="sxs-lookup"><span data-stu-id="bfc42-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="bfc42-361">作成された注文を表示するには、**在庫管理 \> 定期タスク \> 品質管理 \> 品質指示** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="bfc42-362">これで、品質指示のテストを処理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="bfc42-363">このトピックでは、品質テストについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="bfc42-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="bfc42-364">品質管理の詳細については [品質管理の概要](../inventory/enable-quality-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfc42-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="bfc42-365">入荷パレット 3</span><span class="sxs-lookup"><span data-stu-id="bfc42-365">Receive pallet 3</span></span>

<span data-ttu-id="bfc42-366">このシナリオでは、パレット 3 は受入されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="bfc42-367">**LINENUM** フィールドに *1* を入力し、行番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="bfc42-368">**数量** フィールドが使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bfc42-368">The **QTY** field is now available.</span></span> <span data-ttu-id="bfc42-369">*1* を入力し、数量を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="bfc42-370">**品質チェック** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-370">The **Quality check** page appears.</span></span> <span data-ttu-id="bfc42-371">この受領で、このパレットは品質を受け入れ、バルク プットアウェイ場所にプットされます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="bfc42-372">確認ボタンを選択して、品質チェックを合格にします。</span><span class="sxs-lookup"><span data-stu-id="bfc42-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="bfc42-373">次のプット作業の詳細を表示する **発注書: プット** ページ:</span><span class="sxs-lookup"><span data-stu-id="bfc42-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="bfc42-374">**LOC:** システムが決定した場所</span><span class="sxs-lookup"><span data-stu-id="bfc42-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="bfc42-375">この場所は、発注書の受入に対して指定されたプットアウェイです。</span><span class="sxs-lookup"><span data-stu-id="bfc42-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="bfc42-376">**LP:** システムが生成したライセンス プレート ID</span><span class="sxs-lookup"><span data-stu-id="bfc42-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="bfc42-377">**品目:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="bfc42-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="bfc42-378">**数量:** *1 PL: 各 100 個*</span><span class="sxs-lookup"><span data-stu-id="bfc42-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="bfc42-379">アイテムの説明も表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-379">The item description is also shown.</span></span>

1. <span data-ttu-id="bfc42-380">プットアウェイ作業を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfc42-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="bfc42-381">発注書明細行入荷の **タスク** ページで、"作業が完了しました" メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="bfc42-382">**LINENUM** フィールドは、次のパレットの入荷を開始できるようにするために用意されています。</span><span class="sxs-lookup"><span data-stu-id="bfc42-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="bfc42-383">ページの上部にあるメニューボタン (**≡**) を選択し、メニューで **キャンセル** を選択してメニューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="bfc42-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="bfc42-384">これでモバイル アプリを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="bfc42-384">You can now close the mobile app.</span></span>
