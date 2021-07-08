---
title: 循環棚卸のシナリオ例
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management 循環棚卸機能を参照する一連のシナリオを示します。
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 828954402d223c62f52d7a13fcc9efab84630c80
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261787"
---
# <a name="cycle-counting-example-scenarios"></a><span data-ttu-id="ef21d-103">循環棚卸のシナリオ例</span><span class="sxs-lookup"><span data-stu-id="ef21d-103">Cycle counting example scenarios</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef21d-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management 循環棚卸機能を参照する一連のシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-104">This topic provides a collection of scenarios that explore the cycle counting features of Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ef21d-105">最初に、既存の Supply Chain Management 環境の要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-105">It first describes the requirements for your existing Supply Chain Management environment.</span></span> <span data-ttu-id="ef21d-106">その後、循環棚卸の構成方法と、すべての循環棚卸ステージについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-106">It then explains how to configure cycle counting and describes all the cycle counting stages.</span></span> <span data-ttu-id="ef21d-107">完了したら、ガイド付き循環棚卸、ブラインド循環棚卸、スポット循環棚卸、循環棚卸のしきい値、循環棚卸計画など循環棚卸を深く解釈している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-107">When you've finished, you should have a good understanding of cycle counting, including guided cycle counting, blind cycle counting, spot cycle counting, cycle count thresholds, and cycle count plans.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef21d-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="ef21d-108">Prerequisites</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ef21d-109">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="ef21d-109">Make demo data available</span></span>

<span data-ttu-id="ef21d-110">このトピックの各シナリオでは、Supply Chain Management に向けて提供されている標準のデモ データに含まれる値とレコードを参照しています。</span><span class="sxs-lookup"><span data-stu-id="ef21d-110">Each scenario in this topic references values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="ef21d-111">シナリオを実行してここで提供されている値を使用する場合は、必ずデモ データがインストールされている環境で作業し、開始する前に法人 (会社) を **USMF** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-111">If you want to use the values that are provided here as you work through the scenarios, be sure to work in an environment where the demo data is installed, and set the legal entity (company) to **USMF** before you begin.</span></span>

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="ef21d-112">Warehouse Management モバイル アプリのサポートをオンにする</span><span class="sxs-lookup"><span data-stu-id="ef21d-112">Turn on support for the Warehouse Management mobile app</span></span>

<span data-ttu-id="ef21d-113">新しい Warehouse Management モバイル アプリを使用する前に、サポートをシステムに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-113">Before you can use the new Warehouse Management mobile app, you must add support for it in your system.</span></span> <span data-ttu-id="ef21d-114">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ef21d-115">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="ef21d-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ef21d-116">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="ef21d-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ef21d-117">**機能名:** *新しい倉庫アプリのユーザー設定、アイコン、ステップ タイトル*</span><span class="sxs-lookup"><span data-stu-id="ef21d-117">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a><span data-ttu-id="ef21d-118">シナリオのデモ データの準備</span><span class="sxs-lookup"><span data-stu-id="ef21d-118">Prepare demo data for the scenarios</span></span>

<span data-ttu-id="ef21d-119">次の手順に従って、シナリオに必要なすべてのデモ データがシステム内の USMF 企業で利用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-119">Follow these steps to confirm that all the demo data that is required for the scenarios is available in the USMF company in your system.</span></span> <span data-ttu-id="ef21d-120">欠落しているレコードまたは値を作成します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-120">Create any records or values that are missing.</span></span>

1. <span data-ttu-id="ef21d-121">**倉庫管理 \> 設定 \> 作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-121">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="ef21d-122">リスト ウィンドウで、**Julia Funderburk** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-122">In the list pane, select **Julia Funderburk**.</span></span>
1. <span data-ttu-id="ef21d-123">**ユーザー** クイック タブで、次の値を持つ行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-123">On the **Users** FastTab, select the row that has the following values.</span></span> <span data-ttu-id="ef21d-124">既存の行にこれらの値がない場合は、作成します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-124">If no existing row has these values, create it.</span></span>

    - <span data-ttu-id="ef21d-125">**ユーザー ID:** *61*</span><span class="sxs-lookup"><span data-stu-id="ef21d-125">**User ID:** *61*</span></span>
    - <span data-ttu-id="ef21d-126">**ユーザー名:** *WH61*</span><span class="sxs-lookup"><span data-stu-id="ef21d-126">**User name:** *WH61*</span></span>
    - <span data-ttu-id="ef21d-127">**既定の倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="ef21d-127">**Default warehouse:** *61*</span></span>
    - <span data-ttu-id="ef21d-128">**メニュー名:** *メイン*</span><span class="sxs-lookup"><span data-stu-id="ef21d-128">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="ef21d-129">**作業** クイック タブで、次の値をユーザー *61* 用に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-129">On the **Work** FastTab, set the following values for user *61* if they aren't already set:</span></span>

    - <span data-ttu-id="ef21d-130">**循環棚卸監修者ですか:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="ef21d-130">**Is a cycle count supervisor:** *No*</span></span>
    - <span data-ttu-id="ef21d-131">**割合の上限:** *0*</span><span class="sxs-lookup"><span data-stu-id="ef21d-131">**Maximum percentage limit:** *0*</span></span>
    - <span data-ttu-id="ef21d-132">**数量の上限:** *0*</span><span class="sxs-lookup"><span data-stu-id="ef21d-132">**Maximum quantity limit:** *0*</span></span>
    - <span data-ttu-id="ef21d-133">**値の上限:** *0*</span><span class="sxs-lookup"><span data-stu-id="ef21d-133">**Maximum value limit:** *0*</span></span>

1. <span data-ttu-id="ef21d-134">**倉庫管理 \> 設定 \> 作業 \> 作業プール** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-134">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="ef21d-135">作業プールは、倉庫作業を作業のタイプ (この場合、循環棚卸作業) に基づいて分類するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-135">Work pools are used to segregate warehouse work, based on the type of work (in this case, cycle counting work).</span></span> <span data-ttu-id="ef21d-136">次の設定を持つレコードが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-136">Make sure that a record exists that has the following settings:</span></span>

    - <span data-ttu-id="ef21d-137">**作業プール ID:** *CycleCount*</span><span class="sxs-lookup"><span data-stu-id="ef21d-137">**Work pool ID:** *CycleCount*</span></span>
    - <span data-ttu-id="ef21d-138">**説明:** *循環棚卸*</span><span class="sxs-lookup"><span data-stu-id="ef21d-138">**Description:** *Cycle Count*</span></span>

1. <span data-ttu-id="ef21d-139">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-139">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ef21d-140">リスト ウィンドウで、*循環棚卸* という名前のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-140">In the list pane, select the record that is named *Cycle Count*.</span></span> <span data-ttu-id="ef21d-141">既存のレコードにこの名前が存在しない場合は作成します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-141">If no existing record has this name, create it.</span></span> <span data-ttu-id="ef21d-142">次の値をレコードに対して確認または設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-142">Confirm or set the following values for the record:</span></span>

    - <span data-ttu-id="ef21d-143">**メニュー項目名:** *循環棚卸*</span><span class="sxs-lookup"><span data-stu-id="ef21d-143">**Menu item name:** *Cycle Count*</span></span>
    - <span data-ttu-id="ef21d-144">**タイトル:** *循環棚卸ガイド付き*</span><span class="sxs-lookup"><span data-stu-id="ef21d-144">**Title:** *Cycle Count Guided*</span></span>
    - <span data-ttu-id="ef21d-145">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="ef21d-145">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ef21d-146">**既存の作業を使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="ef21d-146">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="ef21d-147">**作業指示:** *システム主導* (この値は、Supply Chain Management が循環棚卸作業 ID を作業者に割り当てることを示します。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-147">**Directed by:** *System directed* (This value indicates that Supply Chain Management will assign a cycle counting work ID to the worker.)</span></span>
    - <span data-ttu-id="ef21d-148">**在庫状態の表示:** *はい*</span><span class="sxs-lookup"><span data-stu-id="ef21d-148">**Display inventory status:** *Yes*</span></span>

1. <span data-ttu-id="ef21d-149">アクション ウィンドウで、**循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-149">On the Action Pane, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ef21d-150">**モバイル デバイス循環棚卸** ダイアログ ボックスで、次の値を確認または設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-150">In the **Mobile device cycle counting** dialog box, confirm or set the following values:</span></span>

    - <span data-ttu-id="ef21d-151">**品目番号の表示:** *はい*</span><span class="sxs-lookup"><span data-stu-id="ef21d-151">**Display item number:** *Yes*</span></span>
    - <span data-ttu-id="ef21d-152">**ライセンス プレートの表示:** *はい*</span><span class="sxs-lookup"><span data-stu-id="ef21d-152">**Display license plate:** *Yes*</span></span>
    - <span data-ttu-id="ef21d-153">**試行回数:** *1*</span><span class="sxs-lookup"><span data-stu-id="ef21d-153">**Number of attempts:** *1*</span></span>

1. <span data-ttu-id="ef21d-154">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-154">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ef21d-155">リスト ウィンドウで、*循環棚卸ブラインド* という名前のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-155">In the list pane, select the record that is named *Cycle Count Blind*.</span></span> <span data-ttu-id="ef21d-156">既存のレコードにこの名前が存在しない場合は作成します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-156">If no existing record has this name, create it.</span></span> <span data-ttu-id="ef21d-157">次の値をレコードに対して確認または設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-157">Confirm or set the following values for the record:</span></span>

    - <span data-ttu-id="ef21d-158">**メニュー項目名:** *循環棚卸ブラインド*</span><span class="sxs-lookup"><span data-stu-id="ef21d-158">**Menu item name:** *Cycle Count Blind*</span></span>
    - <span data-ttu-id="ef21d-159">**タイトル:** *循環棚卸ブラインド*</span><span class="sxs-lookup"><span data-stu-id="ef21d-159">**Title:** *Cycle Count Blind*</span></span>
    - <span data-ttu-id="ef21d-160">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="ef21d-160">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ef21d-161">**既存の作業を使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="ef21d-161">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="ef21d-162">**作業指示:** *循環棚卸のグループ化* (この値は、作業者が場所、ゾーン、または作業プールに固有の、循環棚卸作業の ID をグループ化できることを示しています。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-162">**Directed by:** *Cycle count grouping* (This value indicates that the worker can group cycle counting work IDs that are specific to a location, zone, or work pool.)</span></span>

1. <span data-ttu-id="ef21d-163">アクション ウィンドウで、**循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-163">On the Action Pane, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ef21d-164">**モバイル デバイス循環棚卸** ダイアログ ボックスで、次の値を確認または設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-164">In the **Mobile device cycle counting** dialog box, confirm or set the following values:</span></span>

    - <span data-ttu-id="ef21d-165">**品目番号の表示:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="ef21d-165">**Display item number:** *No*</span></span>
    - <span data-ttu-id="ef21d-166">**ライセンス プレートの表示:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="ef21d-166">**Display license plate:** *No*</span></span>
    - <span data-ttu-id="ef21d-167">**試行回数:** *0*</span><span class="sxs-lookup"><span data-stu-id="ef21d-167">**Number of attempts:** *0*</span></span>

1. <span data-ttu-id="ef21d-168">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-168">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ef21d-169">リスト ウィンドウで、*スポット棚卸* という名前のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-169">In the list pane, select the record that is named *Spot Counting*.</span></span> <span data-ttu-id="ef21d-170">既存のレコードにこの名前が存在しない場合は作成します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-170">If no existing record has this name, create it.</span></span> <span data-ttu-id="ef21d-171">次の値をレコードに対して確認または設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-171">Confirm or set the following values for the record:</span></span>

    - <span data-ttu-id="ef21d-172">**メニュー項目名:** *スポット棚卸*</span><span class="sxs-lookup"><span data-stu-id="ef21d-172">**Menu item name:** *Spot Counting*</span></span>
    - <span data-ttu-id="ef21d-173">**タイトル:** *スポット棚卸*</span><span class="sxs-lookup"><span data-stu-id="ef21d-173">**Title:** *Spot Counting*</span></span>
    - <span data-ttu-id="ef21d-174">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="ef21d-174">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ef21d-175">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="ef21d-175">**Use existing work:** *No*</span></span>
    - <span data-ttu-id="ef21d-176">**作業作成プロセス:** *スポット循環棚卸* (この値は、作業者が循環棚卸作業を作成せずに、いつでも倉庫の場所の品目を棚卸できることを示しています。</span><span class="sxs-lookup"><span data-stu-id="ef21d-176">**Work creation process:** *Spot cycle counting* (This value indicates that the worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="ef21d-177">場所でスポット 循環棚卸を行うには、作業者が場所 ID を入力します。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-177">To do spot cycle counting in a location, the worker enters the location ID.)</span></span>

1. <span data-ttu-id="ef21d-178">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-178">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="ef21d-179">リスト ウィンドウで、*在庫* という名前のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-179">In the list pane, select the record that is named *Inventory*.</span></span> <span data-ttu-id="ef21d-180">既存のレコードにこの名前が存在しない場合は作成します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-180">If no existing record has this name, create it.</span></span> <span data-ttu-id="ef21d-181">次の循環棚卸メニューが、**メニュー構造** の列に表示されることを確認します:</span><span class="sxs-lookup"><span data-stu-id="ef21d-181">Confirm that the following cycle counting menu items appear in the **Menu structure** column:</span></span>

    - <span data-ttu-id="ef21d-182">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ef21d-182">Cycle Count</span></span>
    - <span data-ttu-id="ef21d-183">循環棚卸ブラインド</span><span class="sxs-lookup"><span data-stu-id="ef21d-183">Cycle Count Blind</span></span>
    - <span data-ttu-id="ef21d-184">スポット棚卸</span><span class="sxs-lookup"><span data-stu-id="ef21d-184">Spot counting</span></span>

1. <span data-ttu-id="ef21d-185">**倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-185">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="ef21d-186">**循環棚卸** タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-186">On the **Cycle counting** tab, set the following values:</span></span>

    - <span data-ttu-id="ef21d-187">**既定の循環棚卸調整タイプ:** *循環棚卸* (このフィールドでは、循環棚卸の完了時に転記される仕訳帳タイプを指定します。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-187">**Default cycle counting adjustment type:** *Cycle Count* (This field specifies the journal type that is posted when cycle counting is done.)</span></span>
    - <span data-ttu-id="ef21d-188">**既定の循環棚卸作業クラス ID:** *CCount* (このフィールドは、循環棚卸に使用される作業クラスを指定します。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-188">**Default cycle counting work class ID:** *CCount* (This field specifies the work class that is used for cycle counting.)</span></span>
    - <span data-ttu-id="ef21d-189">**既定の循環棚卸作業の優先順位:** *50* (このフィールドでは、循環棚卸作業が倉庫内の他のタイプの作業を基準とする優先順位を設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-189">**Default cycle count work priority:** *50* (This field sets the priority that cycle counting work has relative to other types of work in the warehouse.</span></span> <span data-ttu-id="ef21d-190">他のタイプの作業に入力された番号よりも小さい番号を入力すると、循環棚卸作業の優先順位が上がります。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-190">By entering a number that is lower than the number that is entered for other types of work, you raise the priority of the cycle counting work.)</span></span>

1. <span data-ttu-id="ef21d-191">**Warehouse Management \> 設定 \> 在庫 \> 調整タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-191">Go to **Warehouse management \> Setup \> Inventory \> Adjustment types**.</span></span>
1. <span data-ttu-id="ef21d-192">**調整タイプ** ページは、発生する可能性があるさまざまな調整のコードを作成できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ef21d-192">The **Adjustment types** page lets you create codes for the different in and out adjustments that might occur.</span></span> <span data-ttu-id="ef21d-193">次の設定を持つレコードが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-193">Confirm that a record exists that has the following settings:</span></span>

    - <span data-ttu-id="ef21d-194">**在庫調整タイプ:** *循環棚卸*</span><span class="sxs-lookup"><span data-stu-id="ef21d-194">**Inventory adjustment type:** *Cycle Count*</span></span>
    - <span data-ttu-id="ef21d-195">**説明:** *循環棚卸*</span><span class="sxs-lookup"><span data-stu-id="ef21d-195">**Description:** *Cycle Count*</span></span>
    - <span data-ttu-id="ef21d-196">**名前:** *ICnt*</span><span class="sxs-lookup"><span data-stu-id="ef21d-196">**Name:** *ICnt*</span></span>

1. <span data-ttu-id="ef21d-197">**Warehouse Management \> 設定 \> 倉庫設定 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-197">Go to **Warehouse management \> Setup \> Warehouse setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ef21d-198">リスト ウィンドウで、倉庫 *61* を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-198">In the list pane, select warehouse *61*.</span></span> <span data-ttu-id="ef21d-199">既存のレコードにこの名前が存在しない場合は作成します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-199">If no existing record has this name, create it.</span></span>
1. <span data-ttu-id="ef21d-200">**倉庫** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-200">On the **Warehouse** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ef21d-201">**Warehouse Managementプロセスを使用する:** *はい* (この値は、Warehouse Managementプロセスの倉庫を有効にします。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-201">**Use warehouse management process:** *Yes* (This value enables the warehouse for warehouse management processes.)</span></span>
    - <span data-ttu-id="ef21d-202">**循環棚卸中にライセンス プレートの移動を許可する:** *はい* (この値により、作業者は循環棚卸中にライセンス プレートを移動できます。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-202">**Allow license plate moves during cycle counting:** *Yes* (This value enables workers to move license plates during a cycle count.)</span></span>

## <a name="scenario-1-guided-cycle-counting"></a><span data-ttu-id="ef21d-203">シナリオ 1: ガイド付き循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ef21d-203">Scenario 1: Guided cycle counting</span></span>

<span data-ttu-id="ef21d-204">ガイド付きの循環棚卸を行う前に、いくつかの作業を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-204">Before guided cycle counting can occur, you must create some work.</span></span> <span data-ttu-id="ef21d-205">この作業は、割り当てられた人物を倉庫を通じて場所から場所にガイドし、作業で設定された棚卸を完了します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-205">This work will guide the assigned person through the warehouse, from location to location, to complete the counts that are set up in the work.</span></span>

### <a name="create-cycle-counting-work-for-scenario-1"></a><span data-ttu-id="ef21d-206">シナリオ 1 の循環棚卸作業の作成</span><span class="sxs-lookup"><span data-stu-id="ef21d-206">Create cycle counting work for scenario 1</span></span>

<span data-ttu-id="ef21d-207">倉庫 *61* の品目場所 *01A02R2S2B* (BULK-06) の循環棚卸作業を作成するには次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ef21d-207">Follow these steps to create cycle counting work for item location *01A02R2S2B* (BULK-06) in warehouse *61*.</span></span>

1. <span data-ttu-id="ef21d-208">**Warehouse Management \> 循環棚卸 \> 場所別循環棚卸作業** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-208">Go to **Warehouse management \> Cycle counting \> Cycle count work by location**.</span></span>
1. <span data-ttu-id="ef21d-209">**場所別循環棚卸作業の作成** ダイアログ ボックスで、**作業プール ID** フィールドを *CycleCount* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-209">In the **Create cycle count work by location** dialog box, set the **Work pool ID** field to *CycleCount*.</span></span>
1. <span data-ttu-id="ef21d-210">**対象に含めるレコード** クイック タブで、**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-210">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ef21d-211">クエリ エディター ダイアログ ボックスの、**範囲** タブで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ef21d-211">In the query editor dialog box, on the **Range** tab, follow these steps:</span></span>

    - <span data-ttu-id="ef21d-212">**フィールド** フィールドが *倉庫* に設定されている行で、**基準** フィールドを *61* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-212">For the row where the **Field** field is set to *Warehouse*, set the **Criteria** field to *61*.</span></span>
    - <span data-ttu-id="ef21d-213">**フィールド** フィールドが *場所* に設定されている行で、**基準** フィールドを *01A02R2S2B* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-213">For the row where the **Field** field is set to *Location,* set the **Criteria** field to *01A02R2S2B*.</span></span>

1. <span data-ttu-id="ef21d-214">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-214">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ef21d-215">**OK** を選択し、**場所別循環棚卸作業の作成** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-215">Select **OK** to close the **Create cycle count work by location** dialog box.</span></span>

    <span data-ttu-id="ef21d-216">作業作成プロセスが完了すると、アクション センターにメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-216">When the work creation process is completed, a message appears in the Action center.</span></span>

1. <span data-ttu-id="ef21d-217">**倉庫管理 \> 作業 \> 作業の詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-217">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ef21d-218">新しく作成された作業を検索するには、**作業プール ID** 列にフィルターを設定し、*CycleCount* の値を持つレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-218">Find the newly created work by setting a filter on the **Work pool ID** column to find records that have a value of *CycleCount*.</span></span>

### <a name="do-cycle-counting-work-for-scenario-1"></a><span data-ttu-id="ef21d-219">シナリオ 1 の循環棚卸作業の実行</span><span class="sxs-lookup"><span data-stu-id="ef21d-219">Do cycle counting work for scenario 1</span></span>

<span data-ttu-id="ef21d-220">循環棚卸作業の作成後、倉庫の場所で品目の棚卸をして、モバイル デバイスを使用して Supply Chain Management に結果を入力して作業を行います。</span><span class="sxs-lookup"><span data-stu-id="ef21d-220">After you've created the cycle counting work, you do the work by counting items in a warehouse location and then using a mobile device to enter the results in Supply Chain Management.</span></span> <span data-ttu-id="ef21d-221">次の手順に従って、Warehouse Management モバイル アプリで循環棚卸作業を実行します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-221">Follow these steps to do the cycle counting work in the Warehouse Management mobile app.</span></span>

1. <span data-ttu-id="ef21d-222">このトピック前半の[シナリオのデモ データの準備](#prepare-demo-data) セクションで設定した作業ユーザーとして Warehouse Management モバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="ef21d-222">Sign in to the Warehouse Management mobile app as the work user that you set up in the [Prepare demo data for the scenarios](#prepare-demo-data) section earlier in this topic.</span></span> <span data-ttu-id="ef21d-223">このトピックの例で、ユーザーの名前は *Julia Funderburk*、倉庫 *61* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ef21d-223">For the example in this topic, the user is named *Julia Funderburk* and is set up for warehouse *61*.</span></span> <span data-ttu-id="ef21d-224">(USMF デモ データでは、ユーザー ID として *61*、パスワードとして *1* を入力することにより、この作業ユーザーとしてサインインできます。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-224">(The USMF demo data should let you sign in as this work user by entering *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ef21d-225">メイン メニューで、**在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-225">On the main menu, select **Inventory**.</span></span>
1. <span data-ttu-id="ef21d-226">**在庫** メニューで、**循環棚卸ガイド付き** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-226">On the **Inventory** menu, select **Cycle Count Guided**.</span></span>
1. <span data-ttu-id="ef21d-227">**数量** フィールドを選択し、数字パッドを使用して *9* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-227">Select the **Qty** field, enter *9* by using the number pad, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ef21d-228">この品目、場所、およびライセンス プレートの 10 個の数を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-228">The system was expecting you to enter a count of 10 pieces for this item, location, and license plate.</span></span> <span data-ttu-id="ef21d-229">したがって、再棚卸が求められます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-229">Therefore, you're asked to recount.</span></span> <span data-ttu-id="ef21d-230">**数量** フィールドを選択し、数字パッドを使用して *9* を再入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-230">Select the **Qty** field, enter *9* again by using the number pad, and then select **OK** (the check mark button).</span></span> <span data-ttu-id="ef21d-231">2 回目の試行では、棚卸が承認されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-231">On the second attempt, your count will be accepted.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef21d-232">システムにより予測される手持数量と入力した数量の差異が検出されると、**循環棚卸ガイド付き** モバイル デバイス メニュー項目の **試行回数** フィールドが *1* として設定されているため、2 回目の棚卸をするように求められます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-232">When the system detected a difference between the expected on-hand quantity and the quantity that you entered, it asked you to count a second time because the **Number of attempts** field is set to *1* for the **Cycle Count Guided** mobile device menu item.</span></span> <span data-ttu-id="ef21d-233">モバイル デバイス メニュー項目の **品目番号の表示** オプションと **ライセンス プレートの表示** オプションの両方が *はい* に設定されているため、特定の品目番号とライセンス プレート番号にガイドされます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-233">You were guided to a specific item number and license plate number because both the **Display item number** option and the **Display license plate** option are set to *Yes* for the mobile device menu item.</span></span>

1. <span data-ttu-id="ef21d-234">**OK** ボタン (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-234">Select **OK** (the check mark button).</span></span>

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a><span data-ttu-id="ef21d-235">シナリオ 1 の循環棚卸の差異を確認する</span><span class="sxs-lookup"><span data-stu-id="ef21d-235">Review the cycle counting differences for scenario 1</span></span>

<span data-ttu-id="ef21d-236">次の手順に従って、循環棚卸の差異を確認します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-236">Follow these steps to review the cycle counting differences.</span></span>

1. <span data-ttu-id="ef21d-237">Supply Chain Management に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-237">Return to Supply Chain Management.</span></span>
1. <span data-ttu-id="ef21d-238">**倉庫管理 \> 作業 \> 作業の詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-238">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ef21d-239">前半で参照した循環棚卸作業を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-239">Find and select the cycle counting work that you looked at earlier.</span></span> <span data-ttu-id="ef21d-240">(たとえば、**作業プール ID** 列をフィルター設定し、*CycleCount* の値を持つレコードを検索します。) この作業の **作業状態** フィールドが *確認待ち* に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ef21d-240">(For example, set a filter on the **Work pool ID** column to find records that have a value of *CycleCount*.) Notice that the **Work status** field for this work is now set to *Pending review*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef21d-241">棚卸作業の実行に使用した作業ユーザー アカウントの場合、**循環棚卸監修者** オプションは *いいえ* に設定され、**割合の上限**、**数量の上限**、および **値の上限** フィールドはすべて *0* (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-241">For the work user account that you used to do the counting work, the **Cycle count supervisor** option is set to *No*, and the **Maximum percentage limit**, **Maximum quantity limit**, and **Maximum value limit** fields are all set to *0* (zero).</span></span> <span data-ttu-id="ef21d-242">したがって、このユーザーが報告するすべての棚卸の差異は手動で承認される必要があり、関連する作業の **作業状態** フィールドが *確認待ち* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-242">Therefore, all counting differences that this user reports must be manually approved, and the **Work status** field for the related work is set to *Pending review*.</span></span> <span data-ttu-id="ef21d-243">カウントされた値が、誤差限度内 (**作業ユーザー** ページの **割合の上限** または **数量の上限** フィールドで指定された) にある場合、またはユーザーの **循環棚卸監修者** オプションが *はい* に設定されている場合、作業は自動的に終了します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-243">If the counted value were within the deviation limits (as specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page), or if the **Cycle count supervisor** option were set to *Yes* for the user, the work would have automatically been closed.</span></span>

1. <span data-ttu-id="ef21d-244">アクション ウィンドウの、**作業** タブで、**循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-244">On the Action Pane, on the **Work** tab, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ef21d-245">アクション ウィンドウで、**受け入れ数量** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-245">On the Action Pane, select **Accept count**.</span></span>

    <span data-ttu-id="ef21d-246">この差異は、標準棚卸仕訳帳を使用して転記され、新しい作業指示書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-246">The difference is posted by using the standard counting journal, and a new work order is created.</span></span>

1. <span data-ttu-id="ef21d-247">**循環棚卸トランザクション** ページのアクション ウィンドウで **派生作業** を選択し、承認された差異に対して作成された作業を検索します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-247">On the **Cycle counting transactions** page, on the Action Pane, select **Derived work** to find the work that was created for the approved difference.</span></span>

## <a name="scenario-2-blind-cycle-counting"></a><span data-ttu-id="ef21d-248">シナリオ 2: ブラインド循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ef21d-248">Scenario 2: Blind cycle counting</span></span>

<span data-ttu-id="ef21d-249">このシナリオでは、システムでシナリオ 1 が既に完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-249">This scenario requires that scenario 1 already be completed in your system.</span></span>

### <a name="create-cycle-counting-work-for-scenario-2"></a><span data-ttu-id="ef21d-250">シナリオ 2 の循環棚卸作業の作成</span><span class="sxs-lookup"><span data-stu-id="ef21d-250">Create cycle counting work for scenario 2</span></span>

<span data-ttu-id="ef21d-251">ブラインドの循環棚卸を行う前に、いくつかの作業を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-251">Before blind cycle counting can occur, you must create some work.</span></span> <span data-ttu-id="ef21d-252">倉庫 *61* の品目場所 *01A02R2S2B* (BULK-06) の循環棚卸作業を作成するには次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ef21d-252">Follow these steps to create cycle counting work for item location *01A02R2S2B* (BULK-06) in warehouse *61*.</span></span>

1. <span data-ttu-id="ef21d-253">**Warehouse Management \> 循環棚卸 \> 品目別循環棚卸作業** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-253">Go to **Warehouse management \> Cycle counting \> Cycle count work by item**.</span></span>
1. <span data-ttu-id="ef21d-254">**品目別循環棚卸作業の作成** ダイアログ ボックスで、**作業プール ID** フィールドを *CycleCount* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-254">In the **Create cycle count work by item** dialog box, set the **Work pool ID** field to *CycleCount*.</span></span>
1. <span data-ttu-id="ef21d-255">**対象に含めるレコード** クイック タブで、**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-255">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ef21d-256">クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定を持つ 3 つの行を追加します :</span><span class="sxs-lookup"><span data-stu-id="ef21d-256">In the query editor dialog box, on the **Range** tab, add three rows that have the following settings:</span></span>

    - <span data-ttu-id="ef21d-257">行 1:</span><span class="sxs-lookup"><span data-stu-id="ef21d-257">Row 1:</span></span>

        - <span data-ttu-id="ef21d-258">**テーブル:** *品目*</span><span class="sxs-lookup"><span data-stu-id="ef21d-258">**Table:** *Items*</span></span>
        - <span data-ttu-id="ef21d-259">**フィールド:** *品目番号*</span><span class="sxs-lookup"><span data-stu-id="ef21d-259">**Field:** *Item number*</span></span>
        - <span data-ttu-id="ef21d-260">**基準:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="ef21d-260">**Criteria:** *L0101*</span></span>

    - <span data-ttu-id="ef21d-261">行 2:</span><span class="sxs-lookup"><span data-stu-id="ef21d-261">Row 2:</span></span>

        - <span data-ttu-id="ef21d-262">**テーブル:** *在庫分析コード*</span><span class="sxs-lookup"><span data-stu-id="ef21d-262">**Table:** *Inventory dimensions*</span></span>
        - <span data-ttu-id="ef21d-263">**フィールド :** *倉庫*</span><span class="sxs-lookup"><span data-stu-id="ef21d-263">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="ef21d-264">**基準 :** *61*</span><span class="sxs-lookup"><span data-stu-id="ef21d-264">**Criteria:** *61*</span></span>

    - <span data-ttu-id="ef21d-265">行 3:</span><span class="sxs-lookup"><span data-stu-id="ef21d-265">Row 3:</span></span>

        - <span data-ttu-id="ef21d-266">**テーブル:** *在庫分析コード*</span><span class="sxs-lookup"><span data-stu-id="ef21d-266">**Table:** *Inventory dimensions*</span></span>
        - <span data-ttu-id="ef21d-267">**フィールド :** *場所*</span><span class="sxs-lookup"><span data-stu-id="ef21d-267">**Field:** *Location*</span></span>
        - <span data-ttu-id="ef21d-268">**基準:** *01A02R2S2B*</span><span class="sxs-lookup"><span data-stu-id="ef21d-268">**Criteria:** *01A02R2S2B*</span></span>

1. <span data-ttu-id="ef21d-269">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-269">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ef21d-270">**OK** を選択し、**品目別循環棚卸作業の作成** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-270">Select **OK** to close the **Create cycle count work by item** dialog box.</span></span>

    <span data-ttu-id="ef21d-271">作業作成プロセスが完了すると、情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-271">When the work creation process is completed, you receive an informational message.</span></span>

### <a name="do-cycle-counting-work-for-scenario-2"></a><span data-ttu-id="ef21d-272">シナリオ 2 の循環棚卸作業の実行</span><span class="sxs-lookup"><span data-stu-id="ef21d-272">Do cycle counting work for scenario 2</span></span>

<span data-ttu-id="ef21d-273">循環棚卸作業を作成した後、次の手順に従って、Warehouse Management モバイル アプリで作業を実行します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-273">After you've created the cycle counting work, following these steps to do the work in the Warehouse Management mobile app.</span></span>

1. <span data-ttu-id="ef21d-274">このトピック前半の[シナリオのデモ データの準備](#prepare-demo-data) セクションで設定した作業ユーザーとして Warehouse Management モバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="ef21d-274">Sign in to the Warehouse Management mobile app as the work user that you set up in the [Prepare demo data for the scenarios](#prepare-demo-data) section earlier in this topic.</span></span> <span data-ttu-id="ef21d-275">このトピックの例で、ユーザーの名前は *Julia Funderburk*、倉庫 *61* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ef21d-275">For the example in this topic, the user is named *Julia Funderburk* and is set up for warehouse *61*.</span></span> <span data-ttu-id="ef21d-276">(USMF デモ データでは、ユーザー ID として *61*、パスワードとして *1* を入力することにより、この作業ユーザーとしてサインインできます。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-276">(The USMF demo data should let you sign in as this work user by entering *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ef21d-277">メイン メニューで、**在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-277">On the main menu, select **Inventory**.</span></span>
1. <span data-ttu-id="ef21d-278">**在庫** メニューで、**循環棚卸ブラインド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-278">On the **Inventory** menu, select **Cycle Count Blind**.</span></span>
1. <span data-ttu-id="ef21d-279">**ゾーン ID** フィールドを選択し、*BULK06* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-279">Select the **Zone ID** field, enter *BULK06*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ef21d-280">**品目** フィールドを選択し、*L0101* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-280">Select the **Item** field, enter *L0101*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ef21d-281">**ライセンス プレート** フィールドを選択し、*LP\_BULK\_06\_01* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-281">Select the **License plate** field, enter *LP\_BULK\_06\_01*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ef21d-282">**数量** フィールドを選択し、*10* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-282">Select the **Qty** field, enter *10*, and then select **OK** (the check mark button).</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef21d-283">システムにより予測される手持数量とスキャンした数量の差異が検出された場合でも、**循環棚卸ブラインド** モバイル デバイス メニュー項目の **試行回数** フィールドが *0* (ゼロ) として設定されているため、2 回目の棚卸をするように求められませんでした。</span><span class="sxs-lookup"><span data-stu-id="ef21d-283">Even though the system detected a difference between the expected on-hand quantity and the quantity that you scanned, it didn't ask you to count a second time because the **Number of attempts** field is set to *0* (zero) for the **Cycle Count Blind** mobile device menu item.</span></span> <span data-ttu-id="ef21d-284">モバイル デバイス メニュー項目の **品目番号の表示** オプションと **ライセンス プレートの表示** オプションの両方が *いいえ* に設定されているため、品目番号とライセンス プレートをスキャンするように求められました。</span><span class="sxs-lookup"><span data-stu-id="ef21d-284">You were asked to scan the item number and license plate because both the **Display item number** option and the **Display license plate** option are set to *No* for the mobile device menu item.</span></span>

1. <span data-ttu-id="ef21d-285">**OK** ボタン (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-285">Select **OK** (the check mark button).</span></span>

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a><span data-ttu-id="ef21d-286">シナリオ 2 の循環棚卸の差異を確認する</span><span class="sxs-lookup"><span data-stu-id="ef21d-286">Review the cycle counting differences for scenario 2</span></span>

<span data-ttu-id="ef21d-287">次の手順に従って、循環棚卸の差異を確認します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-287">Follow these steps to review the cycle counting differences.</span></span>

1. <span data-ttu-id="ef21d-288">Supply Chain Management に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-288">Return to Supply Chain Management.</span></span>
1. <span data-ttu-id="ef21d-289">**Warehouse Management \> 共通 \> 作業 \> 循環棚卸作業が検討保留** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-289">Go to **Warehouse management \> Common \> Work \> Cycle count work pending review**.</span></span>
1. <span data-ttu-id="ef21d-290">アクション ウィンドウの、**作業** タブで、**循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-290">On the Action Pane, on the **Work** tab, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ef21d-291">アクション ウィンドウで、**拒否数量** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-291">On the Action Pane, select **Reject count**.</span></span>

    <span data-ttu-id="ef21d-292">棚卸の差額は拒否されたため、作業は終了しています。</span><span class="sxs-lookup"><span data-stu-id="ef21d-292">Because the counting difference was rejected, the work is closed.</span></span>

## <a name="scenario-3-spot-cycle-counting"></a><span data-ttu-id="ef21d-293">シナリオ 3: スポット循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ef21d-293">Scenario 3: Spot cycle counting</span></span>

<span data-ttu-id="ef21d-294">手持在庫レコードでは、場所 *01A02R2S2B* に品目 *L0101* の手持数量があることが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-294">The on-hand record states that there is an on-hand quantity of item *L0101* at location *01A02R2S2B*.</span></span> <span data-ttu-id="ef21d-295">倉庫作業者は、場所 *01A02R2S1B* にいます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-295">The warehouse worker is at location *01A02R2S1B*.</span></span> <span data-ttu-id="ef21d-296">この場所は空である必要がありますが、いっぱいです。</span><span class="sxs-lookup"><span data-stu-id="ef21d-296">Although this location should be empty, it's full.</span></span> <span data-ttu-id="ef21d-297">したがって、倉庫作業者は直ちにこの場所のスポット棚卸を行います。</span><span class="sxs-lookup"><span data-stu-id="ef21d-297">Therefore, the warehouse worker immediately does a spot count of this location.</span></span>

### <a name="do-cycle-counting-work-for-scenario-3"></a><span data-ttu-id="ef21d-298">シナリオ 3 の循環棚卸作業の実行</span><span class="sxs-lookup"><span data-stu-id="ef21d-298">Do cycle counting work for scenario 3</span></span>

<span data-ttu-id="ef21d-299">次の手順に従って、Warehouse Management モバイル アプリで循環棚卸作業を実行します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-299">Follow these steps to do the cycle counting work in the Warehouse Management mobile app.</span></span>

1. <span data-ttu-id="ef21d-300">このトピック前半の[シナリオのデモ データの準備](#prepare-demo-data) セクションで設定した作業ユーザーとして Warehouse Management モバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="ef21d-300">Sign in to the Warehouse Management mobile app as the work user that you set up in the [Prepare demo data for the scenarios](#prepare-demo-data) section earlier in this topic.</span></span> <span data-ttu-id="ef21d-301">このトピックの例で、ユーザーの名前は *Julia Funderburk*、倉庫 *61* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ef21d-301">For the example in this topic, the user is named *Julia Funderburk* and is set up for warehouse *61*.</span></span> <span data-ttu-id="ef21d-302">(USMF デモ データでは、ユーザー ID として *61*、パスワードとして *1* を入力することにより、この作業ユーザーとしてサインインできます。)</span><span class="sxs-lookup"><span data-stu-id="ef21d-302">(The USMF demo data should let you sign in as this work user by entering *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ef21d-303">メイン メニューで、**在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-303">On the main menu, select **Inventory**.</span></span>
1. <span data-ttu-id="ef21d-304">**在庫** メニューで、**スポット循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-304">On the **Inventory** menu, select **Spot counting**.</span></span>
1. <span data-ttu-id="ef21d-305">**場所** フィールドを選択し、*01A02R2S1B* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-305">Select the **Location** field, enter *01A02R2S1B*, and then select **OK** (the check mark button).</span></span>

    <span data-ttu-id="ef21d-306">システムにより、Supply Chain Management の場所が空であることが検出されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-306">The system detects that the location is empty in Supply Chain Management.</span></span>

1. <span data-ttu-id="ef21d-307">**LP または品目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-307">Select **Add LP or Item**.</span></span>
1. <span data-ttu-id="ef21d-308">**品目** フィールドを選択し、*L0101* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-308">Select the **Item** field, enter *L0101*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ef21d-309">**ライセンス プレート** フィールドを選択し、*LP\_BULK\_06\_01* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-309">Select the **License plate** field, enter *LP\_BULK\_06\_01*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ef21d-310">**数量** フィールドを選択し、*9* を入力し、**OK** (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-310">Select the **Qty** field, enter *9*, and then select **OK** (the check mark button).</span></span>

    <span data-ttu-id="ef21d-311">システムにより、指定したライセンス プレートが Supply Chain Management の別の場所で使用できることが検出されたため、そのライセンス プレートは現在の場所に移動されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-311">Because the system detects that the specified license plate is already available at another location in Supply Chain Management, that license plate will be moved to the current location.</span></span> <span data-ttu-id="ef21d-312">したがって、移動を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-312">Therefore, the system asks you to confirm the movement.</span></span>

1. <span data-ttu-id="ef21d-313">**OK** ボタン (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-313">Select **OK** (the check mark button).</span></span>

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a><span data-ttu-id="ef21d-314">シナリオ 3 の循環棚卸の差異を確認する</span><span class="sxs-lookup"><span data-stu-id="ef21d-314">Review the cycle counting differences for scenario 3</span></span>

<span data-ttu-id="ef21d-315">次の手順に従って、棚卸の結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-315">Follow these steps to review the counting results.</span></span>

1. <span data-ttu-id="ef21d-316">Supply Chain Management に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ef21d-316">Return to Supply Chain Management.</span></span>
1. <span data-ttu-id="ef21d-317">**Warehouse Management \> 共通 \> 作業の詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-317">Go to **Warehouse management \> Common \> Work details**.</span></span>
1. <span data-ttu-id="ef21d-318">グリッドの上部で **クローズ済の表示** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-318">Select the **Show closed** checkbox at the top of the grid.</span></span>
1. <span data-ttu-id="ef21d-319">**作業指示書タイプ** 列のフィルターを、*在庫移動* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-319">Set the filter for the **Work order type** column to *Inventory movement*.</span></span>

    <span data-ttu-id="ef21d-320">システムにより、この棚卸が在庫移動として自動的に検出されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-320">The system automatically detected this count as an inventory movement.</span></span> <span data-ttu-id="ef21d-321">**倉庫** ページの倉庫 *61* で、**循環棚卸中にライセンス プレートの移動を許可する** オプションが *はい* に設定されているため、この移動は許可されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-321">This movement is permitted because the **Allow license plate moves during cycle counting** option is set to *Yes* for warehouse *61* on the **Warehouses** page.</span></span>

## <a name="scenario-4-define-cycle-count-thresholds"></a><span data-ttu-id="ef21d-322">シナリオ 4: 循環棚卸のしきい値の定義</span><span class="sxs-lookup"><span data-stu-id="ef21d-322">Scenario 4: Define cycle count thresholds</span></span>

<span data-ttu-id="ef21d-323">循環棚卸作業を作成する 1 つの方法は、しきい値を使用することです。</span><span class="sxs-lookup"><span data-stu-id="ef21d-323">One way to create cycle counting work is to use thresholds.</span></span> <span data-ttu-id="ef21d-324">循環棚卸のしきい値は、在庫品目の数量または割合の限度を示します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-324">A cycle count threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="ef21d-325">循環棚卸作業は、しきい値に達したときに自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-325">Cycle counting work is automatically created when the threshold is reached.</span></span>

<span data-ttu-id="ef21d-326">たとえば、循環棚卸のしきい値が 40 の場所に 60 品目あるとします。</span><span class="sxs-lookup"><span data-stu-id="ef21d-326">For example, there are 60 items in a location that has a cycle count threshold of 40.</span></span> <span data-ttu-id="ef21d-327">販売注文トランザクション中に、25 品目がその場所からピッキングされてステージング場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-327">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="ef21d-328">新しい品目の総数 35 はしきい値の数量より少ないため、その場所のための循環棚卸作業が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-328">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

<span data-ttu-id="ef21d-329">循環棚卸しきい値を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ef21d-329">Follow these steps to set up cycle count thresholds.</span></span>

1. <span data-ttu-id="ef21d-330">**Warehouse Management \> 設定 \> 循環棚卸 \> 循環棚卸のしきい値** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-330">Go to **Warehouse management \> Setup \> Cycle counting \> Cycle count thresholds**.</span></span>
1. <span data-ttu-id="ef21d-331">アクション ウィンドウで、**新規** を選択してしきい値を作成し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-331">On the Action Pane, select **New** to create a threshold, and set the following values for it:</span></span>

    - <span data-ttu-id="ef21d-332">**循環棚卸のしきい値 ID:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="ef21d-332">**Cycle counting threshold ID:** *L0101*</span></span>
    - <span data-ttu-id="ef21d-333">**説明:** *しきい値 L0101*</span><span class="sxs-lookup"><span data-stu-id="ef21d-333">**Description:** *Threshold L0101*</span></span>
    - <span data-ttu-id="ef21d-334">**しきい値の数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="ef21d-334">**Threshold quantity:** *2*</span></span>
    - <span data-ttu-id="ef21d-335">**単位:** *個*</span><span class="sxs-lookup"><span data-stu-id="ef21d-335">**Unit:** *ea*</span></span>
    - <span data-ttu-id="ef21d-336">**割合に基づく容量しきい値:** *0.00*</span><span class="sxs-lookup"><span data-stu-id="ef21d-336">**Capacity threshold based on percentage:** *0.00*</span></span>
    - <span data-ttu-id="ef21d-337">**循環棚卸しきい値タイプ:** *数量*</span><span class="sxs-lookup"><span data-stu-id="ef21d-337">**Cycle counting threshold type:** *Quantity*</span></span>
    - <span data-ttu-id="ef21d-338">**即座の循環棚卸の処理:** *はい*</span><span class="sxs-lookup"><span data-stu-id="ef21d-338">**Process cycle count immediately:** *Yes*</span></span>
    - <span data-ttu-id="ef21d-339">**次回の循環棚卸までの日数:** *1*</span><span class="sxs-lookup"><span data-stu-id="ef21d-339">**Days between cycle counting:** *1*</span></span>
    - <span data-ttu-id="ef21d-340">**作業プール ID:** *CycleCount*</span><span class="sxs-lookup"><span data-stu-id="ef21d-340">**Work pool ID:** *CycleCount*</span></span>

1. <span data-ttu-id="ef21d-341">アクション ウィンドウで、**品目の選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-341">On the Action Pane, select **Select items**.</span></span>
1. <span data-ttu-id="ef21d-342">**範囲** タブのクエリ エディター ダイアログ ボックスで、**フィールド** フィールドが *品目番号* に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-342">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Item number*.</span></span> <span data-ttu-id="ef21d-343">その行の **基準** フィールドを *L0101* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-343">Set the **Criteria** field for that row to *L0101*.</span></span>
1. <span data-ttu-id="ef21d-344">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-344">Select **OK** to close the query editor dialog box.</span></span>

    <span data-ttu-id="ef21d-345">これで、品目 *L0101* の循環棚卸のしきい値が定義されました。</span><span class="sxs-lookup"><span data-stu-id="ef21d-345">You've now defined a cycle count threshold for item *L0101*.</span></span>

<span data-ttu-id="ef21d-346">手持数量が 2 未満の場合、および場所の最後循環棚卸の日付が今日ではない場合は、任意の場所で循環棚卸が品目 *L0101* に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-346">Cycle counting will now be created for item *L0101* at any location if the on-hand quantity is less than 2, and if the date of the last cycle count for the location isn't today.</span></span>

## <a name="scenario-5-define-cycle-count-plans"></a><span data-ttu-id="ef21d-347">シナリオ 5: 循環棚卸計画の定義</span><span class="sxs-lookup"><span data-stu-id="ef21d-347">Scenario 5: Define cycle count plans</span></span>

<span data-ttu-id="ef21d-348">サイクル棚卸計画を使用すると、循環棚卸作業の作成を自動化できます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-348">Cycle count plans let you automate the creation of cycle counting work.</span></span> <span data-ttu-id="ef21d-349">各循環棚卸計画を、特定の品目クエリおよび場所クエリを使用して設定できます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-349">You can set up each cycle count plan with specific item and location queries.</span></span> <span data-ttu-id="ef21d-350">バッチ ジョブを実行すると、品目および場所の基準に一致するすべての場所 (計画に対して指定された循棚卸の最大数まで) の循環棚卸作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-350">When the batch job runs, it will create cycle counting work for all locations that match the item and location criteria (up to the maximum number of counts that is specified for the plan).</span></span> <span data-ttu-id="ef21d-351">循環棚卸作業が作成されるときには、どの場所をカウントする必要があるかに関する情報が棚卸作業明細行に含まれます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-351">When cycle counting work is created, the counting work line includes information about the location that must be counted.</span></span> <span data-ttu-id="ef21d-352">その場所に関連付けられている手持在庫はブロックされません。</span><span class="sxs-lookup"><span data-stu-id="ef21d-352">The on-hand inventory that is associated with that location isn't blocked.</span></span> <span data-ttu-id="ef21d-353">したがって、未処理の棚卸作業がある場合でも、引当や出荷処理で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-353">Therefore, it's available for reservation and outbound processing, even though open counting work exists.</span></span>

<span data-ttu-id="ef21d-354">循環棚卸計画を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ef21d-354">Follow these steps to set up a cycle count plan.</span></span>

1. <span data-ttu-id="ef21d-355">**Warehouse Management \> 設定 \> 循環棚卸 \> 循環棚卸計画** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-355">Go to **Warehouse management \> Setup \> Cycle counting \> Cycle count plans**.</span></span>
1. <span data-ttu-id="ef21d-356">アクション ウィンドウで、**新規** を選択して行をグリッドに追加し、それに対して次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-356">On the Action Pane, select **New** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="ef21d-357">**循環棚卸計画 ID:** *BULK06*</span><span class="sxs-lookup"><span data-stu-id="ef21d-357">**Cycle counting plan ID:** *BULK06*</span></span>
    - <span data-ttu-id="ef21d-358">**説明:** *BULK06 の場所の棚卸*</span><span class="sxs-lookup"><span data-stu-id="ef21d-358">**Description:** *Counting of location for BULK06*</span></span>
    - <span data-ttu-id="ef21d-359">**作業プール ID:** *CycleCount*</span><span class="sxs-lookup"><span data-stu-id="ef21d-359">**Work pool ID:** *CycleCount*</span></span>
    - <span data-ttu-id="ef21d-360">**循環棚卸の最大数:** *10*</span><span class="sxs-lookup"><span data-stu-id="ef21d-360">**Maximum number of cycle counts:** *10*</span></span>
    - <span data-ttu-id="ef21d-361">**次回の循環棚卸までの日数:** *10*</span><span class="sxs-lookup"><span data-stu-id="ef21d-361">**Days between cycle counting:** *10*</span></span>
    - <span data-ttu-id="ef21d-362">**空の場所:** *空を除外*</span><span class="sxs-lookup"><span data-stu-id="ef21d-362">**Empty locations:** *Exclude empty*</span></span>
    - <span data-ttu-id="ef21d-363">**作業テンプレート** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-363">**Work template:** Leave this field blank.</span></span>

1. <span data-ttu-id="ef21d-364">アクション ウィンドウで、**場所の選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-364">On the Action Pane, select **Select locations**.</span></span>
1. <span data-ttu-id="ef21d-365">標準のクエリ エディター ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-365">A standard query editor dialog box appears.</span></span> <span data-ttu-id="ef21d-366">**範囲** タブで、新しい行を追加してそれに対して次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-366">On the **Range** tab, add a row, and set the following values for it:</span></span>

    - <span data-ttu-id="ef21d-367">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="ef21d-367">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ef21d-368">**フィールド:** *ゾーン ID*</span><span class="sxs-lookup"><span data-stu-id="ef21d-368">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="ef21d-369">**基準:** *BULK06*</span><span class="sxs-lookup"><span data-stu-id="ef21d-369">**Criteria:** *BULK06*</span></span>

1. <span data-ttu-id="ef21d-370">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-370">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ef21d-371">アクション ウィンドウで、**循環棚卸計画のプロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-371">On the Action Pane, select **Process cycle counting plan**.</span></span>
1. <span data-ttu-id="ef21d-372">**循環棚卸計画** ダイアログ ボックスの、**バックグラウンドで実行する** クイックタブで、**バッチ処理** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-372">In the **Cycle count plans** dialog box, on the **Run in the background** FastTab, set the **Batch processing** option to *Yes*.</span></span>
1. <span data-ttu-id="ef21d-373">**繰り返し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-373">Select **Recurrence**.</span></span>
1. <span data-ttu-id="ef21d-374">**繰り返しの定義** ダイアログ ボックスで、バッチ ジョブを設定することにより、それがすぐに開始され、1 分ごとに実行され、終了日がないようにします。</span><span class="sxs-lookup"><span data-stu-id="ef21d-374">In the **Define recurrence** dialog box, set up the batch job so that it begins immediately and runs once every minute, and so that there is no end date.</span></span>
1. <span data-ttu-id="ef21d-375">**OK** を選択して **繰り返しの定義** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-375">Select **OK** to close the **Define recurrence** dialog box.</span></span>
1. <span data-ttu-id="ef21d-376">**OK** を選択して **循環棚卸計画** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-376">Select **OK** to close the **Cycle count plans** dialog box.</span></span>

    <span data-ttu-id="ef21d-377">メッセージは、ジョブがバッチ キューに追加されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-377">A message informs you that the job was added to the batch queue.</span></span>

1. <span data-ttu-id="ef21d-378">**Warehouse Management \> 共通 \> 循環棚卸のスケジューリング** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-378">Go to **Warehouse management \> Common \> Cycle count scheduling**.</span></span> <span data-ttu-id="ef21d-379">計画は即座に開始され、棚卸作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-379">The plan begins immediately and creates counting work.</span></span> <span data-ttu-id="ef21d-380">棚卸作業が完了しないので、**状態** フィールドは *処理中* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-380">Because counting work hasn't been completed, the **Status** field is set to *In process*.</span></span> <span data-ttu-id="ef21d-381">1 分後に、**合計循環棚卸** 列の値が *1* に変更されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-381">After one minute, the value in the **Total cycle counts** column changes to *1*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef21d-382">最後の循環棚卸以降の日数が、循環棚卸計画の **次回の循環棚卸までの日数** フィールドに設定した値よりも少ない場合、循環棚卸作業は作成されません。</span><span class="sxs-lookup"><span data-stu-id="ef21d-382">Cycle count work won't be created if the number of days since the last cycle counting is less than value that you set for the **Days between cycle counting** field for the cycle counting plan.</span></span> <span data-ttu-id="ef21d-383">たとえば、**次回の循環棚卸までの日数** フィールドを *5* に設定すると、循環棚卸作業は 5 日ごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-383">For example, if the **Days between cycle counting** field is set to *5*, cycle counting work will be created every five days.</span></span> <span data-ttu-id="ef21d-384">ただし、循環棚卸作業が 3 日目に処理される場合は、次の循環棚卸作業は、最後の循環棚卸処理の 5 日後の 8 日目に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ef21d-384">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

1. <span data-ttu-id="ef21d-385">アクション ウィンドウで、**作業** を選択して、作成された棚卸作業を表示します。</span><span class="sxs-lookup"><span data-stu-id="ef21d-385">On Action Pane, select **Work** to view the counting work that was created.</span></span>
