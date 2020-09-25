---
title: 倉庫の場所の状態
description: このトピックでは、倉庫の場所のステータス機能の概要を示します。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 7b17df2afee22dde1af5c44de31c585069daa349
ms.sourcegitcommit: d03f301633175b15d46690fc97067820bf21579f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2020
ms.locfileid: "3775177"
---
# <a name="warehouse-location-status"></a><span data-ttu-id="62e65-103">倉庫の場所の状態</span><span class="sxs-lookup"><span data-stu-id="62e65-103">Warehouse location status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62e65-104">Microsoft Dynamics 365 Supply Chain Management には、場所を操作したり管理したりする際の柔軟性を備えたいくつかの場所フィールドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="62e65-104">Microsoft Dynamics 365 Supply Chain Management includes several location fields that give you flexibility when you work with and maintain locations.</span></span> <span data-ttu-id="62e65-105">場所のステータスを場所ディレクティブ クエリに含めて、倉庫のフローにわたるコントロールが向上します。</span><span class="sxs-lookup"><span data-stu-id="62e65-105">You can include location statuses in the location directive query to provide better control over warehouse flow.</span></span>

<span data-ttu-id="62e65-106">**場所**ページの次の 4 つのフィールドでは、場所の現在のステータスに関する情報を追跡します。</span><span class="sxs-lookup"><span data-stu-id="62e65-106">The following four fields on the **Locations** page track information about the current status of a location.</span></span> <span data-ttu-id="62e65-107">これらのフィールドにより、倉庫マネージャは倉庫の場所のステータスの概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="62e65-107">These fields let warehouse managers get an overview of the status of the warehouse locations.</span></span> <span data-ttu-id="62e65-108">また、詳細なレポートとフィルタ処理が可能です。</span><span class="sxs-lookup"><span data-stu-id="62e65-108">They also allow for advanced reporting and filtering.</span></span>

- <span data-ttu-id="62e65-109">**品目番号** – 場所に現在含まれている品目。</span><span class="sxs-lookup"><span data-stu-id="62e65-109">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="62e65-110">場所に複数の品目が含まれている場合、このフィールドは空白になります。</span><span class="sxs-lookup"><span data-stu-id="62e65-110">If the location contains multiple items, this field is blank.</span></span>
- <span data-ttu-id="62e65-111">**最終活動日時** – 場所に対して実行された最後の倉庫トランザクションのタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="62e65-111">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="62e65-112">**エイジング日付** – 場所の在庫が倉庫に取り込まれた日付。</span><span class="sxs-lookup"><span data-stu-id="62e65-112">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="62e65-113">この値は、ライセンス プレートのエイジング日付に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-113">This value is calculated based on the aging date of the license plate.</span></span> <span data-ttu-id="62e65-114">これは、ライセンス プレートで追跡されている場所では正確ですが、ライセンス プレートで追跡されていない場所では正確ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="62e65-114">It's accurate for locations that are license plate–tracked, but it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="62e65-115">**位置情報** – 場所のステータス。</span><span class="sxs-lookup"><span data-stu-id="62e65-115">**Location status** – The status of the location.</span></span> <span data-ttu-id="62e65-116">使用可能な値は 4 つあります。</span><span class="sxs-lookup"><span data-stu-id="62e65-116">There are four possible values:</span></span>

    - <span data-ttu-id="62e65-117">**未定義** – 場所プロファイルではステータスを追跡できません。</span><span class="sxs-lookup"><span data-stu-id="62e65-117">**Undetermined** – The location profile can't track status.</span></span> <span data-ttu-id="62e65-118">したがって、現在のステータスは不明になります。</span><span class="sxs-lookup"><span data-stu-id="62e65-118">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="62e65-119">**空** – 現在の場所に在庫はありません。</span><span class="sxs-lookup"><span data-stu-id="62e65-119">**Empty** – There is currently no inventory in the location.</span></span>
    - <span data-ttu-id="62e65-120">**ピッキング** – 最後に空になった後の場所に対して、出庫トランザクションが実行されています。</span><span class="sxs-lookup"><span data-stu-id="62e65-120">**Picking** – Outbound transactions have been performed against the location since it was last empty.</span></span>
    - <span data-ttu-id="62e65-121">**ストレージ** – 最後に空になった後の場所に対して、入庫トランザクションのみが実行されています。</span><span class="sxs-lookup"><span data-stu-id="62e65-121">**Storage** – Only inbound transactions have been performed against the location since the location was last empty.</span></span>

## <a name="turn-on-the-warehouse-location-status-feature"></a><span data-ttu-id="62e65-122">倉庫の場所のステータス機能をオンにします</span><span class="sxs-lookup"><span data-stu-id="62e65-122">Turn on the Warehouse location status feature</span></span>

<span data-ttu-id="62e65-123">*倉庫の場所のステータス*機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e65-123">Before you can use the *Warehouse location status* feature, it must be turned on in your system.</span></span> <span data-ttu-id="62e65-124">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="62e65-124">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="62e65-125">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="62e65-125">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="62e65-126">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="62e65-126">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="62e65-127">**機能名:** *倉庫の場所のステータス*</span><span class="sxs-lookup"><span data-stu-id="62e65-127">**Feature name:** *Warehouse location status*</span></span>

## <a name="set-up-warehouse-location-status"></a><span data-ttu-id="62e65-128">倉庫の場所のステータスの設定</span><span class="sxs-lookup"><span data-stu-id="62e65-128">Set up warehouse location status</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a><span data-ttu-id="62e65-129">シナリオ例に必要なサンプルデータを用意します</span><span class="sxs-lookup"><span data-stu-id="62e65-129">Prepare the sample data that is required for the example scenario</span></span>

<span data-ttu-id="62e65-130">シナリオの作業を開始する前に、サンプル データを有効にして、このセクションの説明に従って機能を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e65-130">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section.</span></span> <span data-ttu-id="62e65-131">シナリオ例を完了するには、ウェアハウス アプリまたはブラウザベースのエミュレーターのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e65-131">To complete the example scenario, you must use either the warehouse app or the browser-based emulator.</span></span> <span data-ttu-id="62e65-132">ここで提供される手順では、ウェアハウス アプリを使用します。</span><span class="sxs-lookup"><span data-stu-id="62e65-132">The steps that are provided here use the warehouse app.</span></span> <span data-ttu-id="62e65-133">ブラウザベースのエミュレーターの手順も同様です。</span><span class="sxs-lookup"><span data-stu-id="62e65-133">The steps for the browser-based emulator are similar.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="62e65-134">USMF 法人を使用します</span><span class="sxs-lookup"><span data-stu-id="62e65-134">Use the USMF legal entity</span></span>

<span data-ttu-id="62e65-135">ここで指定されたサンプル レコードと値を使用してシナリオ例を実行するには、標準の[デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e65-135">To work through the example scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="62e65-136">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e65-136">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="set-up-location-profiles"></a><span data-ttu-id="62e65-137">場所プロファイルを設定します</span><span class="sxs-lookup"><span data-stu-id="62e65-137">Set up location profiles</span></span>

<span data-ttu-id="62e65-138">このシナリオ例では、2 つの場所プロファイルを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e65-138">The example scenario requires that you prepare two location profiles.</span></span>

1. <span data-ttu-id="62e65-139">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-139">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="62e65-140">**編集**を選択し、ページを編集モードにします。</span><span class="sxs-lookup"><span data-stu-id="62e65-140">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="62e65-141">**バルク-06** プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-141">Select the **BULK-06** profile.</span></span>
1. <span data-ttu-id="62e65-142">**一般**クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="62e65-142">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="62e65-143">**場所の品目の有効化:** このオプションでは_はい_に設定します。</span><span class="sxs-lookup"><span data-stu-id="62e65-143">**Enable item in location:** Set this option to _Yes_.</span></span>
    - <span data-ttu-id="62e65-144">**場所の活動日時の有効化:** このオプションは_はい_に設定します。</span><span class="sxs-lookup"><span data-stu-id="62e65-144">**Enable location activity date and time:** Set this option to _Yes_.</span></span>
    - <span data-ttu-id="62e65-145">**場所の品目の有効化:** このオプションでは_はい_に設定します。</span><span class="sxs-lookup"><span data-stu-id="62e65-145">**Enable location status:** Set this option to _Yes_.</span></span>

    <span data-ttu-id="62e65-146">これらのオプションは、場所の参照フィールドを有効にするかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="62e65-146">These options control whether the reference fields on the location are active.</span></span>

1. <span data-ttu-id="62e65-147">**ピック-06** プロファイルについて、手順 3 から 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="62e65-147">Repeat steps 3 through 4 for the **PICK-06** profile.</span></span>

> [!NOTE]
> <span data-ttu-id="62e65-148">場所のプロファイルのパラメータ (**場所の有効化**、**場所の状態の有効化**、**場所のステータスの有効化**) が *はい* に設定されている場合、*倉庫の場所のステータスの整合性チェック* ジョブを実行すると、関連する場所がすぐに更新されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-148">When the parameters on the location profile (**Enable item in location**, **Enable location activity**, **Enable location status**) are set to *Yes*, the system immediately updates the relevant locations by executing the *warehouse location status consistency check* job.</span></span>

### <a name="scenario"></a><span data-ttu-id="62e65-149">シナリオ</span><span class="sxs-lookup"><span data-stu-id="62e65-149">Scenario</span></span>

1. <span data-ttu-id="62e65-150">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-150">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="62e65-151">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-151">Select **New**.</span></span>
1. <span data-ttu-id="62e65-152">**発注書の作成**ダイアログ ボックスでは、**仕入先**クイックタブの**仕入先**フィールドで *104* を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-152">In the **Create purchase order** dialog box, on the **Vendor** FastTab, in the **Vendor account** field, select *104*.</span></span>
1. <span data-ttu-id="62e65-153">**一般** クイック タブの **倉庫** フィールドで、 *61* を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-153">On the **General** FastTab, in the **Warehouse** field, select *61*.</span></span>
1. <span data-ttu-id="62e65-154">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-154">Select **OK**.</span></span>
1. <span data-ttu-id="62e65-155">新しい発注書 (PO) が開かれます。</span><span class="sxs-lookup"><span data-stu-id="62e65-155">Your new purchase order (PO) is opened.</span></span> <span data-ttu-id="62e65-156">**購買注文明細行**グリッドに空白行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62e65-156">It includes an empty line in the **Purchase order lines** grid.</span></span> <span data-ttu-id="62e65-157">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="62e65-157">On this line, set the following values:</span></span>

    - <span data-ttu-id="62e65-158">**品目番号:** _A0002_</span><span class="sxs-lookup"><span data-stu-id="62e65-158">**Item number:** _A0002_</span></span>
    - <span data-ttu-id="62e65-159">**数量:** _5_</span><span class="sxs-lookup"><span data-stu-id="62e65-159">**Quantity:** _5_</span></span>

1. <span data-ttu-id="62e65-160">発注書を確認する場合は、アクション ウィンドウの**アクション** グループの**購入**タブで、**確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-160">On the Action Pane, on the **Purchase** tab, in the **Actions** group, select **Confirm** to confirm the purchase order.</span></span>
1. <span data-ttu-id="62e65-161">モバイル デバイスで、**入庫 \> 購入の受信**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-161">On the mobile device, go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="62e65-162">**PONUM** フィールドを選択し、PO 番号を入力してから確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-162">Select the **PONUM** field, enter the PO number, and confirm.</span></span>
1. <span data-ttu-id="62e65-163">**アイテム** フィールドを選択し、品目番号 *A0002* を入力してから確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-163">Select the **ITEM** field, enter *A0002* as the item number, and confirm.</span></span>
1. <span data-ttu-id="62e65-164">**数量**ページで、数量として *5* と入力し、確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-164">On the **QTY** page, enter *5* as the quantity, and confirm.</span></span>

    <span data-ttu-id="62e65-165">数量は、次のいずれかの方法で入力できます。</span><span class="sxs-lookup"><span data-stu-id="62e65-165">You can enter the quantity in either of the following ways:</span></span>

    - <span data-ttu-id="62e65-166">数値を加算または減算するには、プラス記号 (**+**) またはマイナス記号 (**–**) ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-166">Select the plus sign (**+**) or minus sign (**–**) button to add or subtract a numerical value.</span></span>
    - <span data-ttu-id="62e65-167">数字パッドを開くには、プラス記号 (**+**) ボタンとマイナス記号 (**–**) ボタンの間にある空白のフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-167">Select the blank field between the plus sign (**+**) and minus sign (**–**) buttons to open the number pad.</span></span>

1. <span data-ttu-id="62e65-168">選択した品目番号 *A0002* と数量 *5* を確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-168">Confirm your selection of item number *A0002* and a quantity of *5*.</span></span> <span data-ttu-id="62e65-169">ページ下部に「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-169">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="62e65-170">右上隅にあるメニューボタン (ハンバーガーあるいはハンバーガー ボタンと呼ばれることがあります) を選択してから**キャンセル**を選択し、**購入の受信**を終了して、**入庫**メニューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="62e65-170">Select the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-right corner, and then select **Cancel** to exit **Purchase Receive** and return to the **Inbound** menu.</span></span>
1. <span data-ttu-id="62e65-171">発注書ページで、**購買注文明細行**グリッドの上にある**作業詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-171">On the purchase order page, select **Work details** above the **Purchase order lines** grid.</span></span>
1. <span data-ttu-id="62e65-172">**一般**タブで、作成された**作業 ID** と**ターゲット ライセンス プレート ID** 値を通知します。</span><span class="sxs-lookup"><span data-stu-id="62e65-172">On the **General** tab, notice the **Work ID** and **Target license plate ID** values that were created.</span></span>
1. <span data-ttu-id="62e65-173">**明細行**セクションで、**場所**値の*ピッキング*と*プット*作業タイプを通知します。</span><span class="sxs-lookup"><span data-stu-id="62e65-173">In the **Lines** section, notice the **Location** values for the *Pick* and *Put* work types.</span></span>
1. <span data-ttu-id="62e65-174">モバイル デバイスで、**入庫 \> 購入品のプットアウェイ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-174">On the mobile device, go to **Inbound \> Purchase Put-away**.</span></span>
1. <span data-ttu-id="62e65-175">**ID** フィールドを選択し、作業 ID を入力してから確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-175">Select the **ID** field, enter the work ID, and confirm.</span></span>
1. <span data-ttu-id="62e65-176">*ピッキング* エントリが完了するまでもう一度確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-176">Confirm once more to complete the *Pick* entry.</span></span>
1. <span data-ttu-id="62e65-177">右上隅にあるメニュー ボタンを選択してから**完了**を選択して、*ピッキング*作業を完了します。</span><span class="sxs-lookup"><span data-stu-id="62e65-177">Select the Menu button in the upper-right corner, and then select **Done** to complete the *Pick* work.</span></span>
1. <span data-ttu-id="62e65-178">プットアウェイの場所をメモして、確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-178">Make a note of the Putaway location, and confirm.</span></span> <span data-ttu-id="62e65-179">ページ下部に「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-179">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="62e65-180">右上隅にあるメニュー ボタンを選択してから**キャンセル**を選択して**購入品のプットアウェイ**を完了し、**入庫**メニューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="62e65-180">Select the Menu button in the upper-right corner, and then select **Cancel** to exit **Purchase Put-away** and return to the **Inbound** menu.</span></span>
1. <span data-ttu-id="62e65-181">**戻る**を選択してメイン メニューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="62e65-181">Select **Back** to return to the main menu.</span></span>
1. <span data-ttu-id="62e65-182">Dynamics 365 Supply Chain Management で、**倉庫管理 \> 設定 \> 倉庫 \> 場所**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-182">In Dynamics 365 Supply Chain Management, go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="62e65-183">**場所**をフィルタ処理し、発注書の作業からプットアウェイの場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="62e65-183">Filter on **Location**, and enter the putaway location from the purchase order work.</span></span> <span data-ttu-id="62e65-184">次の結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-184">You should see the following results:</span></span>

    - <span data-ttu-id="62e65-185">この場所に対する最後のトランザクションがプットであったため、**位置情報**列に*ストレージ*値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-185">The **Location status** column shows a value of *Storage*, because the last transaction against this location was a put.</span></span>
    - <span data-ttu-id="62e65-186">品目が入庫されてその場所に配置されたために、**品目番号**列には *A0002* 値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-186">The **Item number** column shows a value of *A0002*, because that item was received and put to the location.</span></span>
    - <span data-ttu-id="62e65-187">**最後のアクティビティ日時**列には、その場所で作業が完了した日時のタイムスタンプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-187">The **Last activity date and time** column shows the timestamp for the date and time when the work was completed at the location.</span></span>

1. <span data-ttu-id="62e65-188">モバイル デバイスで、**品質 \> 移動**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-188">On the mobile device, go to **Quality \> Movement**.</span></span>
1. <span data-ttu-id="62e65-189">**LOC/LP** フィールドを選択してから、前の手順で書き留めた場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="62e65-189">Select the **LOC/LP** field, and enter the location you made note of in the previous steps.</span></span>
1. <span data-ttu-id="62e65-190">表示される情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-190">Confirm the information that is shown.</span></span> <span data-ttu-id="62e65-191">生成されたライセンス プレート番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="62e65-191">Make a note of the license plate number that is generated.</span></span>
1. <span data-ttu-id="62e65-192">品目の移動先として**宛先情報**画面で、**LOC/LP** フィールドを選択し、*06A07R2S1B* と入力します。</span><span class="sxs-lookup"><span data-stu-id="62e65-192">On the **To Information** screen, select the **LOC/LP** field, and enter *06A07R2S1B* as the location to move the item to.</span></span>
1. <span data-ttu-id="62e65-193">**宛先情報**画面で、自動的に生成される **LP** 値 (ターゲット ライセンス プレート ID) を確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-193">On the **To Information** screen, confirm the **LP** value (the target license plate ID), which is automatically generated.</span></span> <span data-ttu-id="62e65-194">ページ下部に「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-194">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="62e65-195">右上隅にあるメニュー ボタンを選択し、**キャンセル**を選択して**移動**を完了し、**品質管理**メニューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="62e65-195">Select the Menu button in the upper-right corner, and then select **Cancel** to exit **Movement** and return to the **Quality Management** menu.</span></span>
1. <span data-ttu-id="62e65-196">**戻る**を選択してメイン メニューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="62e65-196">Select **Back** to return to the main menu.</span></span>
1. <span data-ttu-id="62e65-197">Dynamics 365 Supply Chain Management で、**倉庫管理 \> 設定 \> 倉庫 \> 場所**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-197">In Dynamics 365 Supply Chain Management, go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="62e65-198">**場所**ページを更新し、元のプットアウェイの場所を再度表示します。</span><span class="sxs-lookup"><span data-stu-id="62e65-198">Refresh the **Locations** page, and view the original putaway location again.</span></span> <span data-ttu-id="62e65-199">**位置情報**フィールドが*空*に設定され、**品目番号**列が空白になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-199">Notice that the **Location status** field is now set to *Empty*, and the **Item number** column is blank.</span></span>
1. <span data-ttu-id="62e65-200">場所 *06A07R2S1B* のレコードを表示し、**ステータス**値が*ストレージ*に変更され、**品目番号**および**最後の活動日時**フィールドが更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-200">View the record for location *06A07R2S1B*, and notice that the **Status** value has changed to *Storage*, and the **Item number** and **Last activity date and time** fields have been updated.</span></span>
1. <span data-ttu-id="62e65-201">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-201">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="62e65-202">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-202">Select **New**.</span></span>
1. <span data-ttu-id="62e65-203">**販売注文の作成**ダイアログ ボックスの**顧客 ID** フィールドで、*US-002* を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-203">In the **Create sales order** dialog box, in the **Customer account** field, select *US-002*.</span></span>
1. <span data-ttu-id="62e65-204">**倉庫** フィールドで、 *61* を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-204">In the **Warehouse** field, select *61*.</span></span>
1. <span data-ttu-id="62e65-205">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-205">Select **OK**.</span></span>
1. <span data-ttu-id="62e65-206">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="62e65-206">Your new sales order is opened.</span></span> <span data-ttu-id="62e65-207">**販売注文行**グリッドに空白行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62e65-207">It includes an empty line in the **Sales order lines** grid.</span></span> <span data-ttu-id="62e65-208">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="62e65-208">On this line, set the following values:</span></span>

    - <span data-ttu-id="62e65-209">**品目番号:** _A0002_</span><span class="sxs-lookup"><span data-stu-id="62e65-209">**Item number:** _A0002_</span></span>
    - <span data-ttu-id="62e65-210">**数量:** _1_</span><span class="sxs-lookup"><span data-stu-id="62e65-210">**Quantity:** _1_</span></span>

1. <span data-ttu-id="62e65-211">**販売注文行**クイック タブの**在庫**メニューで、**予約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-211">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
1. <span data-ttu-id="62e65-212">**予約**ページで、**引当ロット**を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="62e65-212">On the **Reservation** page, select **Reserve lot** to reserve the order line.</span></span> <span data-ttu-id="62e65-213">次に、右上隅の**閉じる**ボタン (**X**) を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="62e65-213">Then select the **Close** button (**X**) in the upper-right corner to close the page.</span></span>
1. <span data-ttu-id="62e65-214">アクション ペインの、**倉庫**タブにある**アクション**グループで、**倉庫にリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-214">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="62e65-215">**販売注文行**セクションにある**倉庫**メニューで、**作業の詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-215">In the **Sales order lines** section, on the **Warehouse** menu, select **Work details**.</span></span>
1. <span data-ttu-id="62e65-216">作成された**作業 ID** 値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="62e65-216">Copy the **Work ID** value that was created.</span></span>
1. <span data-ttu-id="62e65-217">モバイル デバイスで、**出荷 \> 販売ピッキング**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-217">On the mobile device, go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="62e65-218">**ID** フィールドを選択し、前述の手順でコピーした作業 ID を入力して、確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-218">Select the **ID** field, enter the work ID that you copied earlier, and confirm.</span></span>
1. <span data-ttu-id="62e65-219">**販売注文: ピッキング** ページの **LOC** フィールドでは、ピッキング場所を先ほど作成したプットアウェイの場所として提示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-219">On the **Sales orders: Pick** page, the **LOC** field suggests the picking location as the putaway location that was created earlier.</span></span> <span data-ttu-id="62e65-220">場所をメモします。</span><span class="sxs-lookup"><span data-stu-id="62e65-220">Make a note of the location.</span></span>
1. <span data-ttu-id="62e65-221">**LOC** フィールドを選択し、場所を入力してから確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-221">Select the **LOC** field, enter the location, and confirm.</span></span>
1. <span data-ttu-id="62e65-222">**LP** フィールドを選択し、移動アクティビティ中にメモしたライセンス プレート番号を入力して、確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-222">Select the **LP** field, enter the license plate number that you made a note of during the Movement activity, and confirm.</span></span>
1. <span data-ttu-id="62e65-223">**品目**フィールドを選択し、品目番号 *A0002* を入力して、確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-223">Select the **Item** field, enter the *A0002* as the item number, and confirm.</span></span>
1. <span data-ttu-id="62e65-224">**数量**ページで、数量として *1* と入力し、確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-224">On the **QTY** page, enter *1* as the quantity, and confirm.</span></span>

    <span data-ttu-id="62e65-225">数量は、次のいずれかの方法で入力できます。</span><span class="sxs-lookup"><span data-stu-id="62e65-225">You can enter the quantity in either of the following ways:</span></span>

    - <span data-ttu-id="62e65-226">数値を加算または減算するには、プラス記号 (**+**) またはマイナス記号 (**–**) ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-226">Select the plus sign (**+**) or minus sign (**–**) button to add or subtract a numerical value.</span></span>
    - <span data-ttu-id="62e65-227">数字パッドを開くには、プラス記号 (**+**) ボタンとマイナス記号 (**–**) ボタンの間にある空白のフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="62e65-227">Select the blank field between the plus sign (**+**) and minus sign (**–**) buttons to open the number pad.</span></span>

1. <span data-ttu-id="62e65-228">**ターゲット LP** フィールドを選択し、ユーザー定義のターゲット ライセンス プレート ID を入力して、確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-228">Select the **TARGET LP** field, enter a user-defined target license plate ID, and confirm.</span></span>
1. <span data-ttu-id="62e65-229">ピッキング作業が完了するまでもう一度確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-229">Confirm once more to complete the picking work.</span></span> <span data-ttu-id="62e65-230">ページ下部に「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-230">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="62e65-231">右上隅にあるメニュー ボタンを選択してから**キャンセル**を選択すると、ピッキング活動を完了して**出荷プロセス** メニューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="62e65-231">Select the Menu button in the upper-right corner, and then select **Cancel** to complete the picking activity and return to the **Outbound** menu.</span></span>
1. <span data-ttu-id="62e65-232">Dynamics 365 Supply Chain Management で、**倉庫管理 \> 設定 \> 倉庫 \> 場所**に移動します。</span><span class="sxs-lookup"><span data-stu-id="62e65-232">In Dynamics 365 Supply Chain Management, go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="62e65-233">**場所**をフィルタ処理し、販売注文作業からピッキング場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="62e65-233">Filter on **Location**, and enter the pick location from the sales order work.</span></span>
1. <span data-ttu-id="62e65-234">販売注文作業が選択された**位置情報**フィールドが*ピッキング*に設定され、**最終活動日時**フィールドが更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="62e65-234">Notice that the **Location status** field for the location that the sales order work picked from is now set to *Picking*, and the **Last activity date and time** field has been updated.</span></span>

> [!NOTE]
> <span data-ttu-id="62e65-235">場所フィールドは、倉庫トランザクションによってのみ更新されます。</span><span class="sxs-lookup"><span data-stu-id="62e65-235">The location fields are updated only by warehouse transactions.</span></span> <span data-ttu-id="62e65-236">仕訳帳またはその他の非 WHS プロセスを使用して在庫を移動した場合、フィールドは更新されません。</span><span class="sxs-lookup"><span data-stu-id="62e65-236">If you move inventory by using a journal or other non-WHS processes, the fields won't be updated.</span></span>
