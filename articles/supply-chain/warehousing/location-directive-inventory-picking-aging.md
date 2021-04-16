---
title: 場所のディレクティブ在庫ピッキング エイジング
description: このトピックでは、ピッキング中の先入れ先出し (FIFO) と後入れ先出し (LIFO) の場所ディレクティブ戦略の使用方法について説明します。
author: mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 937af7e24fc72b5b8bc741857913899a239a64d3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835537"
---
# <a name="location-directive-inventory-picking-aging"></a><span data-ttu-id="87847-103">場所のディレクティブ在庫ピッキング エイジング</span><span class="sxs-lookup"><span data-stu-id="87847-103">Location directive inventory picking aging</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87847-104">このトピックでは、ピッキング中の先入れ先出し (FIFO) と後入れ先出し (LIFO) の場所ディレクティブ戦略の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="87847-104">This topic explains how to use first in, first out (FIFO) and last in, first out (LIFO) location directive strategies during picking.</span></span> <span data-ttu-id="87847-105">これらの戦略は、場所に対して記録されるエイジング日付と連携して機能し、在庫が倉庫に最初に入ったときを追跡します。</span><span class="sxs-lookup"><span data-stu-id="87847-105">These strategies work in conjunction with the aging dates that are recorded for locations to track when inventory first entered the warehouse.</span></span> <span data-ttu-id="87847-106">*場所のディレクティブ在庫ピッキング エイジング* 機能は、場所の日付を使用してエイジングを決定します。</span><span class="sxs-lookup"><span data-stu-id="87847-106">The *Location directive inventory picking aging* feature uses the date on the location to determine aging.</span></span> <span data-ttu-id="87847-107">*倉庫の場所の状態* 機能により、ライセンス プレートの日付に基づいて、場所の日付が更新されます。</span><span class="sxs-lookup"><span data-stu-id="87847-107">The *Warehouse location status* feature updates the date on the location, based on the date from the license plate.</span></span>

<span data-ttu-id="87847-108">FIFO と LIFO 戦略を使用して、在庫が倉庫に入った日付に基づいて、バッチ追跡品目と非バッチ追跡品目の両方を出荷できます。</span><span class="sxs-lookup"><span data-stu-id="87847-108">You can use FIFO and LIFO strategies to ship both batch-tracked items and non-batch-tracked items, based on the date when the inventory entered the warehouse.</span></span> <span data-ttu-id="87847-109">この機能は、有効期限が並べ替えに使用できない、非バッチ追跡の在庫に特に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="87847-109">This capability can be especially useful for non-batch-tracked inventory, where an expiration date isn't available to use for sorting.</span></span>

<span data-ttu-id="87847-110">在庫が倉庫で最初に入庫または作成されると、システムは関連するライセンス プレートを更新して、現在の日付がエイジング日付として表示されます。</span><span class="sxs-lookup"><span data-stu-id="87847-110">When inventory is first received or created in the warehouse, the system updates the relevant license plate so that the current date is shown as the aging date.</span></span> <span data-ttu-id="87847-111">この日付は、場所のディレクティブ戦略で使用され、倉庫内の最も古い在庫または最新の在庫を識別します。</span><span class="sxs-lookup"><span data-stu-id="87847-111">This date is then used by the location directive strategies to identify the oldest or newest inventory in the warehouse.</span></span> <span data-ttu-id="87847-112">ライセンス プレートによって追跡されていない場所に在庫を移動すると、その場所自体はエイジング情報と共に更新され、この情報が戦略によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="87847-112">If inventory is moved to a location that isn't tracked by license plate, the location itself is updated with aging information, and this information will then be used by the strategies.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="87847-113">機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="87847-113">Turn on the feature</span></span>

<span data-ttu-id="87847-114">この機能を使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で次の機能を順にオンにします:</span><span class="sxs-lookup"><span data-stu-id="87847-114">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), in this order:</span></span>

1. <span data-ttu-id="87847-115">倉庫の場所の状態</span><span class="sxs-lookup"><span data-stu-id="87847-115">Warehouse location status</span></span>
1. <span data-ttu-id="87847-116">場所のディレクティブ在庫ピッキング エイジング</span><span class="sxs-lookup"><span data-stu-id="87847-116">Location directive inventory picking aging</span></span>

## <a name="feature-requirements"></a><span data-ttu-id="87847-117">機能要件</span><span class="sxs-lookup"><span data-stu-id="87847-117">Feature requirements</span></span>

<span data-ttu-id="87847-118">この機能を使用するには、在庫の保管に使用されるすべての [場所プロファイル](tasks/create-location-profile.md) について、**場所の状態の有効化** オプションを *はい* に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87847-118">To use this feature, you must set the **Enable location status** option set to *Yes* for every [location profile](tasks/create-location-profile.md) that is used to store inventory.</span></span> <span data-ttu-id="87847-119">このオプションを場所プロファイルに設定するには、**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動し、場所プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-119">To set this option for a location profile, go to **Warehouse management \> Setup \> Warehouse \> Location profiles**, and select the location profile.</span></span> <span data-ttu-id="87847-120">このオプションは、**一般** クイック タブにあります。</span><span class="sxs-lookup"><span data-stu-id="87847-120">You can find the option on the **General** FastTab.</span></span>

## <a name="feature-scenarios"></a><span data-ttu-id="87847-121">フィーチャー シナリオ</span><span class="sxs-lookup"><span data-stu-id="87847-121">Feature scenarios</span></span>

<span data-ttu-id="87847-122">このセクションでは、FIFO および LIFO 戦略の設定方法と使用方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="87847-122">This section provides examples that show how to set up and use FIFO and LIFO strategies.</span></span>

> [!TIP]
> <span data-ttu-id="87847-123">このセクションでは、FIFO と LIFO の 2 つのシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="87847-123">This section provides two scenarios, one for FIFO and one for LIFO.</span></span> <span data-ttu-id="87847-124">ここで説明する手順は、両方のシナリオを順番に実行することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="87847-124">The procedures that are provided assume that you will do both scenarios, in order.</span></span> <span data-ttu-id="87847-125">この 2 つの戦略の違いを体験できるように、両方のシナリオを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="87847-125">We recommend that you do both scenarios, so that you can experience the differences between the two strategies.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="87847-126">サンプル データを有効化する</span><span class="sxs-lookup"><span data-stu-id="87847-126">Make sample data available</span></span>

<span data-ttu-id="87847-127">指定されたサンプル レコードと値を使用してこれらのシナリオを実行するには、標準の[デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87847-127">To work through these scenarios by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="87847-128">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87847-128">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="87847-129">これらのシナリオは、実稼働システムで機能を使用するためのガイダンスとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="87847-129">You can also use these scenarios as guidance for using the feature on a production system.</span></span> <span data-ttu-id="87847-130">ただし、その場合は、ここで説明する設定ごとに独自の値に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="87847-130">However, in that case, you must substitute your own values for each setting that is described here.</span></span>

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a><span data-ttu-id="87847-131">シナリオを設定する</span><span class="sxs-lookup"><span data-stu-id="87847-131">Set up the scenarios</span></span>

<span data-ttu-id="87847-132">デモ データには、シナリオをサポートするための設定と在庫調整が必要です。</span><span class="sxs-lookup"><span data-stu-id="87847-132">The demo data requires setup and inventory adjustments to support the scenarios.</span></span> <span data-ttu-id="87847-133">FIFO シナリオと LIFO シナリオで作業するために必要な在庫データを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="87847-133">Follow these steps to create the inventory data that is required to work through the FIFO and LIFO scenarios.</span></span>

1. <span data-ttu-id="87847-134">デモ データがインストールされているシステムサインインし、**USMF** 法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-134">Sign in to a system where demo data is installed, and select the **USMF** legal entity.</span></span>
1. <span data-ttu-id="87847-135">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="87847-135">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="87847-136">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-136">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="87847-137">場所プロファイルの一覧で、**FLOOR-05** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-137">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="87847-138">**一般** クイック タブで、**場所の状態の有効化** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="87847-138">On the **General** FastTab, set the **Enable location status** option to *Yes*.</span></span>
1. <span data-ttu-id="87847-139">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-139">Select **Save**.</span></span>
1. <span data-ttu-id="87847-140">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="87847-140">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="87847-141">場所ディレクティブの一覧で、**63 ピッキング コンテナー詰め** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-141">In the list of location directives, select **63 Pick containerization**.</span></span>
1. <span data-ttu-id="87847-142">**編集** を選択し、ページを編集モードにします。</span><span class="sxs-lookup"><span data-stu-id="87847-142">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="87847-143">**場所のディレクティブ アクション** クイック タブで、**シーケンス番号** フィールドが *1* に設定されている行を見つけ、次のいずれかの手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="87847-143">On the **Location directive actions** FastTab, find the line where the **Sequence number** field is set to *1*, and follow one of these steps:</span></span>

    - <span data-ttu-id="87847-144">FIFO シナリオを設定する場合は、**戦略** フィールドの値を *場所エイジング FIFO* に変更します。</span><span class="sxs-lookup"><span data-stu-id="87847-144">If you're setting up a FIFO scenario, change the value of the **Strategy** field to *Location aging FIFO*.</span></span>
    - <span data-ttu-id="87847-145">LIFO シナリオを設定する場合は、**戦略** フィールドの値を *場所エイジング LIFO* に変更します。</span><span class="sxs-lookup"><span data-stu-id="87847-145">If you're setting up a LIFO scenario, change the value of the **Strategy** field to *Location aging LIFO*.</span></span>

1. <span data-ttu-id="87847-146">**場所ディレクティブ アクション** クイック タブで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-146">On the **Location directive actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="87847-147">クエリのダイアログ ボックスの **範囲** タブで **追加** を選択して、明細行を追加し、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="87847-147">In the query dialog box, on the **Range** tab, select **Add** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="87847-148">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="87847-148">**Table:** *Locations*</span></span>
    - <span data-ttu-id="87847-149">**派生テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="87847-149">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="87847-150">**フィールド:** *ゾーン ID*</span><span class="sxs-lookup"><span data-stu-id="87847-150">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="87847-151">**基準:** *フロア*</span><span class="sxs-lookup"><span data-stu-id="87847-151">**Criteria:** *Floor*</span></span>

1. <span data-ttu-id="87847-152">**OK** を選択して設定を適用し、クエリのダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="87847-152">Select **OK** to apply your settings and close the query dialog box.</span></span>
1. <span data-ttu-id="87847-153">**保存** を選択し、場所のディレクティブへの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="87847-153">Select **Save** to save your changes to the location directive.</span></span>
1. <span data-ttu-id="87847-154">モバイル デバイスまたは PC の *Dynamics 365 for Finance and Operations - Warehousing* アプリで、次の手順に従って、シナリオをサポートするために倉庫の場所から既存の在庫を削除します:</span><span class="sxs-lookup"><span data-stu-id="87847-154">On a mobile device or in the *Dynamics 365 for Finance and Operations - Warehousing* app on your PC, follow these steps to remove existing inventory from the warehouse location to support the scenarios:</span></span>

    1. <span data-ttu-id="87847-155">適切なユーザー ID とパスワードを使用して、倉庫 *63* にサインインします。</span><span class="sxs-lookup"><span data-stu-id="87847-155">Sign in to warehouse *63* by using the appropriate user ID and password.</span></span>
    1. <span data-ttu-id="87847-156">メイン メニューで **品質** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-156">On the main menu, select **Quality**.</span></span>
    1. <span data-ttu-id="87847-157">**品質管理** メニューで **仕損** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-157">On the **Quality management** menu, select **Scrap**.</span></span>
    1. <span data-ttu-id="87847-158">**仕損** ページで、**LOC/LP** フィールドを選択し、*63\_1* を入力します。</span><span class="sxs-lookup"><span data-stu-id="87847-158">On the **Scrap** page, select the **LOC/LP** field, and then enter *63\_1*.</span></span>
    1. <span data-ttu-id="87847-159">**入力** または **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-159">Select **Enter** or **OK**.</span></span>
    1. <span data-ttu-id="87847-160">**入力** または **OK** を選択して、**調整外** の **仕損** の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="87847-160">Confirm the **Scrap** details for **Adjustment out** by selecting **Enter** or **OK**.</span></span>

    <span data-ttu-id="87847-161">ライセンスプレートの在庫が調整されると、「作業が完了しました」 というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87847-161">When the license plate inventory is adjusted out, you receive a "Work Completed" message.</span></span>

    <span data-ttu-id="87847-162">これらのステップにより、デモ データの 2 つの場所に在庫が残ります。</span><span class="sxs-lookup"><span data-stu-id="87847-162">These steps leave inventory in two locations in the demo data.</span></span> <span data-ttu-id="87847-163">各場所には、それぞれ異なるエイジング日付があります。</span><span class="sxs-lookup"><span data-stu-id="87847-163">Each location has a different aging date.</span></span> <span data-ttu-id="87847-164">場所 *FL-001* のエイジング日付は 2017 年 4 月 15 日、場所 *FL-002* の エイジング日付は 2017 年 1 月 29 日です。</span><span class="sxs-lookup"><span data-stu-id="87847-164">Location *FL-001* has an aging date of April 15, 2017, and location *FL-002* has an aging date of January 29, 2017.</span></span> <span data-ttu-id="87847-165">どちらの場所にも品目 *A0001* が含まれています。</span><span class="sxs-lookup"><span data-stu-id="87847-165">Both locations contain item *A0001*.</span></span>

    <span data-ttu-id="87847-166">このデータを表示するには、**在庫管理 \> 照会およびレポート \> 手持在庫一覧** に移動し、倉庫 *63* と品目 *A0001* でフィルターします。</span><span class="sxs-lookup"><span data-stu-id="87847-166">To view this data, go to **Inventory management \> Inquiries and reports \> On-hand list**, and then filter on warehouse *63* and item *A0001*.</span></span> <span data-ttu-id="87847-167">**場所** フィールドが *FL-001* または *FL-002* に設定されている行で 、**現物在庫** 値が正である明細行を選択し、アクション ペインで **トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-167">In the rows where the **Location** field is set to *FL-001* or *FL-002*, select a line that has a positive **Physical inventory** value, and then, on the Action Pane, select **Transactions**.</span></span> <span data-ttu-id="87847-168">**現物日付** フィールドには、前述のエイジング日付のいずれかに対応する日付が表示されます。</span><span class="sxs-lookup"><span data-stu-id="87847-168">The **Physical date** field will show a date that corresponds to one of the previously mentioned aging dates.</span></span>

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a><span data-ttu-id="87847-169">シナリオ 1: FIFO 場所エイジングを設定および使用する</span><span class="sxs-lookup"><span data-stu-id="87847-169">Scenario 1: Set up and use FIFO location aging</span></span>

<span data-ttu-id="87847-170">FIFO 戦略は、最も古いエイジング日付含む場所を検出し、そのエイジング日付に基づいてピッキングを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="87847-170">The FIFO strategy finds the location that contains the oldest aging date, and it allocates picking based on that aging date.</span></span>

1. <span data-ttu-id="87847-171">まだ行っていない場合は、このシナリオに必要な [サンプル データ](#demo-set-up) を用意します。</span><span class="sxs-lookup"><span data-stu-id="87847-171">If you haven't already done so, [prepare the sample data](#demo-set-up) that is required for this scenario.</span></span>
1. <span data-ttu-id="87847-172">**販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="87847-172">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="87847-173">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-173">Select **New**.</span></span>
1. <span data-ttu-id="87847-174">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="87847-174">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="87847-175">**顧客** クイック タブで、**顧客 ID** フィールドを *US-001* に設定します。</span><span class="sxs-lookup"><span data-stu-id="87847-175">On the **Customer** FastTab, set the **Customer account** field to *US-001*.</span></span>
    - <span data-ttu-id="87847-176">**一般** クイック タブの **倉庫** フィールドを *63* に設定します。</span><span class="sxs-lookup"><span data-stu-id="87847-176">On the **General** FastTab, set the **Warehouse** field to *63*.</span></span>

1. <span data-ttu-id="87847-177">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="87847-177">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="87847-178">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="87847-178">The new sales order is opened.</span></span> <span data-ttu-id="87847-179">これには、**販売注文明細行** クイック タブのグリッドに新しい空の行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="87847-179">It includes a new, empty row in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="87847-180">この注文明細行では、**品目番号** フィールドを *A0001* に、**数量** フィールドを *1* に設定します。</span><span class="sxs-lookup"><span data-stu-id="87847-180">For this order line, set the **Item number** field to *A0001* and the **Quantity** field to *1*.</span></span>
1. <span data-ttu-id="87847-181">グリッドの上部にある **在庫** メニューで、**引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-181">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="87847-182">**引当** ページで、**引当ロット** を選択して、選択した倉庫の在庫からこの品目の注文済数量を引当します。</span><span class="sxs-lookup"><span data-stu-id="87847-182">On the **Reservation** page, select **Reserve lot** to reserve the ordered quantity of this item from inventory at the selected warehouse.</span></span>
1. <span data-ttu-id="87847-183">**引当** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="87847-183">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="87847-184">**販売注文** ページのアクション ペインの **倉庫** タブの **アクション** グループで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-184">On the **Sales order** page, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span> <span data-ttu-id="87847-185">情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87847-185">You receive informational messages.</span></span> <span data-ttu-id="87847-186">システムは出荷を作成し、それを新しい積荷に追加して、必要な作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="87847-186">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="87847-187">**販売注文行** クイック タブで、**倉庫** メニューの **作業の詳細** を選択して、この販売注文に対して作成された作業を開きます。</span><span class="sxs-lookup"><span data-stu-id="87847-187">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details** to open the work that was created for this sales order.</span></span> <span data-ttu-id="87847-188">**作業タイプ** の値が *ピッキング* となっている行は、**場所** の値が *FL-002* であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="87847-188">Notice that the line where the **Work type** value is *Pick* shows a **Location** value of *FL-002*.</span></span> <span data-ttu-id="87847-189">この場所には、最も古いエイジング日付 (FIFO) を持つライセンス プレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="87847-189">This location contains the license plate that has the oldest aging date (FIFO).</span></span>
1. <span data-ttu-id="87847-190">**倉庫 \> 出荷詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-190">Select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="87847-191">**一般** クイック タブで、シナリオ 2 で使用できるように、ウェーブ ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="87847-191">On the **General** FastTab, make a note of the wave ID, so that you can use it in scenario 2.</span></span>

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a><span data-ttu-id="87847-192">シナリオ 2: LIFO 場所エイジングを設定および使用する</span><span class="sxs-lookup"><span data-stu-id="87847-192">Scenario 2: Set up and use LIFO location aging</span></span>

<span data-ttu-id="87847-193">LIFO 戦略は、最新のエイジング日付を含む場所を検出し、そのエイジング日付に基づいてピッキングを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="87847-193">The LIFO strategy finds the location that contains the newest aging date, and it allocates picking based on that aging date.</span></span> <span data-ttu-id="87847-194">シナリオ 2 では、シナリオ 1 (FIFO) の設定を編集し、そのシナリオ中に作成した販売注文とウェーブを再利用します。</span><span class="sxs-lookup"><span data-stu-id="87847-194">In scenario 2, you will edit the setup for scenario 1 (FIFO), and reuse the sales order and wave that were created during that scenario.</span></span>

1. <span data-ttu-id="87847-195">このシナリオを開始する前に、[前のセクション](#fifo-demo) で説明されているように、完全な FIFO シナリオを設定して完了します。</span><span class="sxs-lookup"><span data-stu-id="87847-195">Before you start this scenario, set up and complete the full FIFO scenario as described in the [previous section](#fifo-demo).</span></span> <span data-ttu-id="87847-196">このシナリオでは、シナリオに対して作成されたウェーブとそのほとんどの設定を再利用します。</span><span class="sxs-lookup"><span data-stu-id="87847-196">In this scenario, you will reuse the wave and most of the setup that were created for that scenario.</span></span>
1. <span data-ttu-id="87847-197">[シナリオを設定する](#demo-set-up) 手順の最初の部分で説明されているように、**63 ピッキング コンテナー詰め** の場所のディレクティブを編集して、*場所エイジング LIFO* 戦略を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="87847-197">Edit the **63 Pick containerization** location directive so that it uses the *Location aging LIFO* strategy, as described in the first part of the [Set up the scenarios](#demo-set-up) procedure.</span></span>

    <span data-ttu-id="87847-198">次に、シナリオ 1 で販売注文に対して作成されたウェーブを変更し、*場所エイジング LIFO* 戦略を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="87847-198">Next, you will modify the wave that was created for the sales order in scenario 1, so that is uses the *Location aging LIFO* strategy.</span></span>

1. <span data-ttu-id="87847-199">**倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="87847-199">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="87847-200">FIFO シナリオに対して作成した注文を含むウェーブを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="87847-200">Select and open the wave that contains the order that you created for the FIFO scenario.</span></span>
1. <span data-ttu-id="87847-201">アクション ペインの **作業** タブで、**キャンセル** を選択して、FIFO シナリオに対して作成した作業をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="87847-201">On the Action Pane, on the **Work** tab, select **Cancel** to cancel the work that you created for the FIFO scenario.</span></span>
1. <span data-ttu-id="87847-202">アクション ペインの、**ウェーブ** タブの、**ウェーブ** グループで、**処理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-202">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Process**.</span></span>
1. <span data-ttu-id="87847-203">処理が完了したら、アクション ペインの **ウェーブ** タブの **関連情報** グループで、**作業** を選択して、このウェーブに対して作成された作業を開きます。</span><span class="sxs-lookup"><span data-stu-id="87847-203">When the processing is completed, on the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to open the work that was created for this wave.</span></span>
1. <span data-ttu-id="87847-204">**作業** ページの **概要** タブに、2 つの明細行があります。</span><span class="sxs-lookup"><span data-stu-id="87847-204">On the **Work** page, on the **Overview** tab, there should be two lines.</span></span> <span data-ttu-id="87847-205">**作業状態** フィールドが *オープン* に設定されている明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="87847-205">Select the line where the **Work status** field is set to *Open*.</span></span>
1. <span data-ttu-id="87847-206">**作業タイプ** の値が *ピッキング* となっている行は、**場所** の値が *FL-001* であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="87847-206">Notice that the line where the **Work type** value is *Pick* shows a **Location** value of *FL-001*.</span></span> <span data-ttu-id="87847-207">この場所には、最新のエイジング日付 (LIFO) を持つライセンス プレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="87847-207">This location contains the license plate that has the newest aging date (LIFO).</span></span>

<span data-ttu-id="87847-208">このようなシナリオでは、選択した戦略に応じて、場所のエージング戦略が、最も古い在庫または最新の在庫のいずれかを持つ在庫場所に作業をどのように指示するかを見てきました。</span><span class="sxs-lookup"><span data-stu-id="87847-208">In these scenarios, you've seen how the location aging strategy directs work to the inventory location that has either the oldest inventory or the newest inventory, depending on the selected strategy.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]