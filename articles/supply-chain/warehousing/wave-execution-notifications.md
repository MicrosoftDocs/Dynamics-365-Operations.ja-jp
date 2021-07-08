---
title: ウェーブの実行通知
description: このトピックでは、ウェーブの実行通知についての説明と、設定方法について解説します。
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 47f270b5fff37e8e231d8a9c4a011172df3d9385
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271380"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="bedcf-103">ウェーブの実行通知</span><span class="sxs-lookup"><span data-stu-id="bedcf-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bedcf-104">*ウェーブの実行通知* 機能は、ビジネス イベントとアクション センターを使用して、ウェーブの実行に関する通知を配信します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="bedcf-105">通知を生成するイベントのタイプや倉庫、および通知を受信するユーザーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="bedcf-106">ナビゲーション バーの右側にある **メッセージを表示** ボタン (ベルの記号) は、現在のユーザーにアクション センター メッセージが表示される日を示します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="bedcf-107">ユーザーは、**メッセージの表示** ボタンを選択してアクション センターを開き、メッセージを確認できます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="bedcf-108">ビジネス プロセスの実行時に、ビジネス イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="bedcf-109">業務プロセスはタスクで構成されます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="bedcf-110">ビジネス プロセス中には、それに参加するユーザーは、タスクを完了するビジネス アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="bedcf-111">ビジネス イベントは外部システムが Finance and Operations アプリケーションから通知を受信するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="bedcf-112">これにより、システムは、ビジネス イベントに対してビジネス アクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="bedcf-113">詳細については、[ビジネス イベントの概要](../../fin-ops-core/dev-itpro/business-events/home-page.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bedcf-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="bedcf-114">ウェーブの実行通知機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="bedcf-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="bedcf-115">*ウェーブの実行通知* 機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bedcf-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="bedcf-116">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bedcf-117">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bedcf-118">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="bedcf-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bedcf-119">**機能名:** *ウェーブの実行通知*</span><span class="sxs-lookup"><span data-stu-id="bedcf-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="bedcf-120">シナリオ: アクション センターにウェーブのバッチ実行通知を送信する</span><span class="sxs-lookup"><span data-stu-id="bedcf-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="bedcf-121">このシナリオは、アクション センターを介して特定のロールにウェーブのバッチ実行エラーに関する通知を送信する、エンドツーエンドのフローについてです。</span><span class="sxs-lookup"><span data-stu-id="bedcf-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="bedcf-122">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="bedcf-122">Make demo data available</span></span>

<span data-ttu-id="bedcf-123">このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bedcf-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="bedcf-124">ウェーブがバッチ モードで実行されるのを確認する</span><span class="sxs-lookup"><span data-stu-id="bedcf-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="bedcf-125">**倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="bedcf-126">**ウェーブの処理中** クイックタブで、**ウェーブのバッチ処理** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="bedcf-127">ウェーブのバッチ実行通知を無効にする場合は、**ウェーブのバッチ処理通知** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="bedcf-128">ウェーブの通知ポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="bedcf-128">Configure a wave notification policy</span></span>

<span data-ttu-id="bedcf-129">ウェーブの通知ポリシーは、送信する通知のタイプと通知を受け取るユーザーを定義します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="bedcf-130">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブの通知ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="bedcf-131">以下の設定をしたレコードを作成します:</span><span class="sxs-lookup"><span data-stu-id="bedcf-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="bedcf-132">**ウェーブの通知ポリシー:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="bedcf-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="bedcf-133">**説明:** *倉庫 24 バッチ エラー*</span><span class="sxs-lookup"><span data-stu-id="bedcf-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="bedcf-134">**送信通知を有効にする:** *エラーのみ*</span><span class="sxs-lookup"><span data-stu-id="bedcf-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="bedcf-135">**ロール:** *システム管理者*</span><span class="sxs-lookup"><span data-stu-id="bedcf-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="bedcf-136">このシナリオではデモ データを使用するため、*システム管理者* ロールは、シンプルになるように選択されています。</span><span class="sxs-lookup"><span data-stu-id="bedcf-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="bedcf-137">したがって、システム管理者ユーザーとしてログインすると通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="bedcf-138">ただし通常は、*倉庫マネージャー* など、特定のロールを選択して、ウェーブのバッチ実行エラーを通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bedcf-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="bedcf-139">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="bedcf-140">ウェーブのテンプレートを構成する</span><span class="sxs-lookup"><span data-stu-id="bedcf-140">Configure a wave template</span></span>

<span data-ttu-id="bedcf-141">ウェーブのテンプレートを使用すると、特定のウェーブ メソッドのインスタンスをこれに対応するウェーブ ラベルのテンプレートにリンクさせることができます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="bedcf-142">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="bedcf-143">リスト ペインで、**ウェーブ テンプレート タイプ** フィールドを *出荷* に設定し、倉庫 24 の *24 出荷の既定* ウェーブ テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="bedcf-144">**一般** クイックタブで、**ウェーブの通知ポリシー** フィールドを *24BatchError* に設定します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="bedcf-145">作業テンプレートを構成する</span><span class="sxs-lookup"><span data-stu-id="bedcf-145">Configure a work template</span></span>

<span data-ttu-id="bedcf-146">作業テンプレートは、作業を生成するために、ウェーブの実行中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="bedcf-147">このシナリオでは、ウェーブの実行がエラーを引き起こします。</span><span class="sxs-lookup"><span data-stu-id="bedcf-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="bedcf-148">作業テンプレート クエリに存在しない倉庫を設定すると、ウェーブの実行が失敗するため通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="bedcf-149">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="bedcf-150">リスト ペインで、**作業テンプレート タイプ** フィールドを *販売注文* に設定し、倉庫 24 の *24 SO ステージ* 作業テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="bedcf-151">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="bedcf-152">クエリ エディターのダイアログ ボックスにある **範囲** タブで、次の行を編集します (存在しない場合は追加します)。</span><span class="sxs-lookup"><span data-stu-id="bedcf-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="bedcf-153">**テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="bedcf-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="bedcf-154">**派生テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="bedcf-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="bedcf-155">**フィールド :** *倉庫*</span><span class="sxs-lookup"><span data-stu-id="bedcf-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="bedcf-156">**基準:** 値を *24* から *エラー* に変更します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="bedcf-157">**OK** を選択して、変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="bedcf-158">販売注文を作成して倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="bedcf-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="bedcf-159">**販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="bedcf-160">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="bedcf-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="bedcf-161">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="bedcf-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="bedcf-162">**倉庫:** *24*</span><span class="sxs-lookup"><span data-stu-id="bedcf-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="bedcf-163">**販売注文明細行** クイックタブで、次を設定されている販売注文の明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="bedcf-164">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="bedcf-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="bedcf-165">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="bedcf-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="bedcf-166">これらの品目と数量は一例です。</span><span class="sxs-lookup"><span data-stu-id="bedcf-166">These items and quantities are only examples.</span></span> <span data-ttu-id="bedcf-167">指定された倉庫に十分な在庫が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bedcf-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="bedcf-168">新しい明細行が **販売注文明細行** クイック タブで選択されている間に、ツールバーで **在庫 \> 予約** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="bedcf-169">**引当** ページのアクション ウィンドウで、**引当ロット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="bedcf-170">その後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-170">Then close the page.</span></span>
1. <span data-ttu-id="bedcf-171">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bedcf-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="bedcf-172">ウェーブのバッチ ジョブ実行からの通知</span><span class="sxs-lookup"><span data-stu-id="bedcf-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="bedcf-173">ビジネス イベントの設定に応じて、ウェーブの実行失敗に関する通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="bedcf-174">アクション センターからのメッセージは次の例のようになり、失敗したウェーブへのリンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bedcf-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="bedcf-175">**ウェーブ実行中のエラー**</span><span class="sxs-lookup"><span data-stu-id="bedcf-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="bedcf-176">ウェーブ USMF-000000001 を実行中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="bedcf-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="bedcf-177">最後のメッセージ: ウェーブ USMF-000000001 に必要な作業が作成されていません。</span><span class="sxs-lookup"><span data-stu-id="bedcf-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="bedcf-178">**状態**</span><span class="sxs-lookup"><span data-stu-id="bedcf-178">**STATUS**</span></span>  
> <span data-ttu-id="bedcf-179">有効</span><span class="sxs-lookup"><span data-stu-id="bedcf-179">Active</span></span>
>
> <span data-ttu-id="bedcf-180">ウェーブの詳細を開く</span><span class="sxs-lookup"><span data-stu-id="bedcf-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
