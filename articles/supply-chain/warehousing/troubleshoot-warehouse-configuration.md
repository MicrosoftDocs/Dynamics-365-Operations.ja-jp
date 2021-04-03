---
title: 倉庫コンフィギュレーションのトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management を構成する際に発生する可能性がある一般的な問題の修正方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1fe285f05e5f1ddcb7bd206290b9954cbdaffc75
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487100"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="a88bd-103">倉庫コンフィギュレーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a88bd-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a88bd-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management を構成する際に発生する可能性がある一般的な問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="a88bd-105">"ライセンス プレートまたは場所が有効ではありません" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-106">Issue description</span></span>

<span data-ttu-id="a88bd-107">ライセンス プレート ID または場所をスキャンすると、このエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-108">Issue resolution</span></span>

<span data-ttu-id="a88bd-109">ライセンス プレート ID が別のものによって予約されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a88bd-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="a88bd-110">この問題は、ウェアハウス アプリでユーザーがスキャンした値が有効な場所と有効なライセンス プレート ID の両方である場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="a88bd-111">ただし、この問題はバージョン 10.0.11 で解決されました。</span><span class="sxs-lookup"><span data-stu-id="a88bd-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="a88bd-112">"この場所にはライセンス プレートを指定する必要があります" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-113">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-113">Issue description</span></span>

<span data-ttu-id="a88bd-114">このエラー メッセージは、高度な倉庫管理 (WMS) が有効になっている倉庫を使用して移動オーダーを作成し、作業が完了した後、出荷を確認しようとした場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-115">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-115">Issue resolution</span></span>

<span data-ttu-id="a88bd-116">"移動元" 倉庫の流通倉庫の **既定の受入場所** フィールドが空白になっています。</span><span class="sxs-lookup"><span data-stu-id="a88bd-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="a88bd-117">この問題を解決するには、流通倉庫の既定の受入場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="a88bd-118">この場所がライセンス プレートによって制御されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a88bd-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="a88bd-119">エラー メッセージ "作業タイプが無効なので、在庫ステータスを変更するための作業テンプレート行を作成できません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="a88bd-120">別の作業タイプを選択してください" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-121">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-121">Issue description</span></span>

<span data-ttu-id="a88bd-122">作業テンプレートの場合、**作業テンプレートの詳細** セクションの **作業タイプ** 列で *在庫ステータスの変更* を選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-123">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-123">Issue resolution</span></span>

<span data-ttu-id="a88bd-124">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="a88bd-124">This behavior is by design.</span></span> <span data-ttu-id="a88bd-125">*在庫ステータス変更* 作業タイプは、システム プロセスでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="a88bd-126">この値は構成できません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-126">It can't be configured.</span></span> <span data-ttu-id="a88bd-127">作業タイプのリストは列挙として固定されているため、追加のエントリを **作業タイプ** ドロップダウン メニューからフィルターで除外することはできません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="a88bd-128">"単位 1% の数量が有効ではありません" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-129">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-129">Issue description</span></span>

<span data-ttu-id="a88bd-130">複数のライセンス プレートを含むピッキング作業が 1 つの場所にある場合に、*ea* 単位の数量が無効です。</span><span class="sxs-lookup"><span data-stu-id="a88bd-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-131">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-131">Issue resolution</span></span>

<span data-ttu-id="a88bd-132">リリース済み製品または製品バリアントの **単位順序グループ ID** フィールドと **単位換算** フィールドが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="a88bd-133">バージョン 10.0.15 では、エラー メッセージが改善されていることに注意してください ([KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531) を参照)。</span><span class="sxs-lookup"><span data-stu-id="a88bd-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="a88bd-134">新しいエラー メッセージは、"数量が無効です。</span><span class="sxs-lookup"><span data-stu-id="a88bd-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="a88bd-135">期待値: %1 %2" です。</span><span class="sxs-lookup"><span data-stu-id="a88bd-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="a88bd-136">販売注文のプット作業の場所ディレクティブでは、複数の SKU オプションにより複数の場所ディレクティブのアクションが評価されることはありません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-137">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-137">Issue description</span></span>

<span data-ttu-id="a88bd-138">**複数 SKU** オプションが選択されているときは、*販売注文* 作業指示タイプおよび *プット* 作業タイプの場所ディレクティブにより、複数の場所ディレクティブ アクションが評価されることはありません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="a88bd-139">最初の場所ディレクティブ アクションのみが評価されます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-140">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-140">Issue resolution</span></span>

<span data-ttu-id="a88bd-141">バージョン 10.0.15 では、新しい機能 *複数の SKU の場所ディレクティブのすべてのアクションを評価する* が追加されています ([KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091) を参照)。</span><span class="sxs-lookup"><span data-stu-id="a88bd-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="a88bd-142">この機能は、複数 SKU の場所ディレクティブのすべてのアクションを評価します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="a88bd-143">この機能が必要な場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用してオンにします。</span><span class="sxs-lookup"><span data-stu-id="a88bd-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="a88bd-144">倉庫アプリを使用して部分的なピッキングを実行できません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-145">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-145">Issue description</span></span>

<span data-ttu-id="a88bd-146">販売注文および移動オーダーの場合は、品目のスキップや部分ピッキングを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-147">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-147">Issue resolution</span></span>

<span data-ttu-id="a88bd-148">販売注文または移動オーダーを処理するように設定されているメニュー項目ごとに、**モバイル デバイス メニュー項目** ページで、**全般** クイックタブの **作業の分割を許可する** オプション を *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="a88bd-149">部分的な数量作業に対して在庫ステータスの変更を行うにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="a88bd-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-150">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-150">Issue description</span></span>

<span data-ttu-id="a88bd-151">バッチの一部の数量の在庫ステータス変更を行おうとしています。</span><span class="sxs-lookup"><span data-stu-id="a88bd-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-152">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-152">Issue resolution</span></span>

<span data-ttu-id="a88bd-153">作業者がこの変更を行うことができるようにするには、ウェアハウス アプリのメニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="a88bd-154">**モバイル デバイスのメニュー項目** ページで、次の設定を持つメニュー項目を作成 (または編集) します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="a88bd-155">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="a88bd-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="a88bd-156">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="a88bd-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="a88bd-157">**作業作成プロセス:** *移動*</span><span class="sxs-lookup"><span data-stu-id="a88bd-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="a88bd-158">**在庫状態の表示:** *はい*</span><span class="sxs-lookup"><span data-stu-id="a88bd-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="a88bd-159">必要に応じて、ページの他のフィールドを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a88bd-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="a88bd-160">場所プロファイルのドック管理プロファイルは、在庫タイプの混合を防ぎません。</span><span class="sxs-lookup"><span data-stu-id="a88bd-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a88bd-161">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a88bd-161">Issue description</span></span>

<span data-ttu-id="a88bd-162">*出荷連結ポリシー* を使用しています。</span><span class="sxs-lookup"><span data-stu-id="a88bd-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="a88bd-163">*場所プロファイル* の *ドック管理プロファイル* を設定しましたが、作業の作成時には、最終的な場所で在庫タイプが混合します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a88bd-164">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a88bd-164">Issue resolution</span></span>

<span data-ttu-id="a88bd-165">ドック管理プロファイルでは、事前に作業を分割する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a88bd-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="a88bd-166">つまり、ドック管理プロファイルでは、作業ヘッダーに複数のプット場所がないことを想定しています。</span><span class="sxs-lookup"><span data-stu-id="a88bd-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="a88bd-167">ドック管理プロファイルで在庫の混合を効果的に管理するには、作業ヘッダーの区切りを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a88bd-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="a88bd-168">この例では、ドック管理プロファイルは **混合しない在庫タイプ** を *出荷 ID* に設定されるように構成しています。その場合は、作業ヘッダーの区切りを設定します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="a88bd-169">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a88bd-170">編集する **作業指示書のタイプ** (*発注書* など) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="a88bd-171">編集するには、作業テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="a88bd-172">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="a88bd-173">**並べ替え** タブを開き、次の設定で行を追加します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="a88bd-174">**テーブル** - *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="a88bd-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="a88bd-175">**派生テーブル** - *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="a88bd-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="a88bd-176">**フィールド** - *出荷 ID*</span><span class="sxs-lookup"><span data-stu-id="a88bd-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="a88bd-177">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-177">Select **OK**.</span></span>
1. <span data-ttu-id="a88bd-178">**作業テンプレート** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="a88bd-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="a88bd-179">アクション ウィンドウで、**作業ヘッダーの分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="a88bd-180">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a88bd-181">\**フィールド名\*\*\*出荷 ID* に関連付けられているチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a88bd-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="a88bd-182">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a88bd-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
