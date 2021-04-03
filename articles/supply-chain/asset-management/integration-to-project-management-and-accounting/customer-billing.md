---
title: 顧客所有資産のメンテナンスに対する請求書
description: このトピックでは、顧客が所有する資産に対して行われるメンテナンス作業を作成、処理、および請求する方法について説明します。
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500457"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="d13c8-103">顧客所有資産のメンテナンスに対する請求書</span><span class="sxs-lookup"><span data-stu-id="d13c8-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="d13c8-104">*作業指示書請求* 機能を使用すると、顧客が所有する資産に対して行われるメンテナンス作業を作成、処理、および請求できます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="d13c8-105">この機能を使用すると、次のタスクを実行できます:</span><span class="sxs-lookup"><span data-stu-id="d13c8-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="d13c8-106">顧客と所有する資産を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="d13c8-107">顧客を選択し、作業指示書の作成時に顧客が所有する資産を表示します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="d13c8-108">各顧客の親プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="d13c8-109">作業指示書に対して時間、項目、経費、手数料を登録し、後で顧客の仮発行請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="d13c8-110">さらに、この機能には次の機能が含まれます:</span><span class="sxs-lookup"><span data-stu-id="d13c8-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="d13c8-111">顧客の親プロジェクトのプロジェクト契約が、関連する作業指示書プロジェクトに自動的にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="d13c8-112">資産管理で、作業指示書予測と作業指示書仕訳帳の両方で *手数料* プロジェクト トランザクション タイプを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d13c8-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="d13c8-113">顧客請求機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="d13c8-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="d13c8-114">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d13c8-115">管理者は、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d13c8-116">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="d13c8-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d13c8-117">**モジュール:** *プロジェクト管理および会計*</span><span class="sxs-lookup"><span data-stu-id="d13c8-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="d13c8-118">**機能名:** *作業指示書請求*</span><span class="sxs-lookup"><span data-stu-id="d13c8-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d13c8-119">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="d13c8-119">Example scenario</span></span>

<span data-ttu-id="d13c8-120">この機能の動作の詳細については、次のシナリオ例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d13c8-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="d13c8-121">ここで指定されたサンプル レコードと値を使用してシナリオを実行するには、標準[デモ データ](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d13c8-122">開始する前に、**USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="d13c8-123">このシナリオは、実稼働システムで作業するときにこの機能を使用するためのガイダンスとして使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="d13c8-124">ただし、その場合は、独自の値に置き換える必要があり、標準のデモ データが提供するいくつかのタイプの必要なレコードが不足している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="d13c8-125">手順 1: 顧客に対して新しいプロジェクト契約を作成する</span><span class="sxs-lookup"><span data-stu-id="d13c8-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="d13c8-126">**プロジェクト管理および会計 \> プロジェクト \> プロジェクト契約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="d13c8-127">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d13c8-128">**新規プロジェクト契約** ダイアログ ボックスで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="d13c8-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d13c8-129">**名前:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="d13c8-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="d13c8-130">**資金調達タイプ:** *顧客*</span><span class="sxs-lookup"><span data-stu-id="d13c8-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="d13c8-131">**資金調達ソース:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="d13c8-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="d13c8-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="d13c8-133">手順 2: 顧客に対して新しい親プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="d13c8-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="d13c8-134">ここで作成する親プロジェクトは、顧客の作業指示書が作成される際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="d13c8-135">**プロジェクト管理および会計 \> プロジェクト \> すべてのプロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="d13c8-136">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d13c8-137">**新規プロジェクト** ダイアログ ボックスに次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="d13c8-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d13c8-138">**プロジェクト タイプ:** *時間/実費払い*</span><span class="sxs-lookup"><span data-stu-id="d13c8-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="d13c8-139">**プロジェクト名:** *Pelican Wholesales 作業指示書*</span><span class="sxs-lookup"><span data-stu-id="d13c8-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="d13c8-140">**プロジェクト グループ:** *TM*</span><span class="sxs-lookup"><span data-stu-id="d13c8-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="d13c8-141">**プロジェクト契約 ID:** *Pelican Wholesales* (前に作成した契約)</span><span class="sxs-lookup"><span data-stu-id="d13c8-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="d13c8-142">**開始日:** 今日の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="d13c8-143">**プロジェクトの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-143">Select **Create project**.</span></span>
1. <span data-ttu-id="d13c8-144">新規プロジェクトが開きます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-144">The new project is opened.</span></span> <span data-ttu-id="d13c8-145">**プロジェクト ID** 値をメモします。</span><span class="sxs-lookup"><span data-stu-id="d13c8-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="d13c8-146">後で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="d13c8-147">手順 3: 資産管理で新しい作業指示書タイプを作成する</span><span class="sxs-lookup"><span data-stu-id="d13c8-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="d13c8-148">**資産管理 \> 設定 \> 作業指示書 \> 作業指示書タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="d13c8-149">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d13c8-150">新しいレコードが一覧に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-150">A new record is added to the list.</span></span> <span data-ttu-id="d13c8-151">次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="d13c8-151">Set the following values for it:</span></span>

    - <span data-ttu-id="d13c8-152">**作業指示書タイプ:** *サービス*</span><span class="sxs-lookup"><span data-stu-id="d13c8-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="d13c8-153">**名前:** *サービス作業指示書*</span><span class="sxs-lookup"><span data-stu-id="d13c8-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="d13c8-154">**作業指示書ライフサイクルの状態:** *標準*</span><span class="sxs-lookup"><span data-stu-id="d13c8-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="d13c8-155">手順 4: 顧客アカウントを親プロジェクトにリンクする</span><span class="sxs-lookup"><span data-stu-id="d13c8-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="d13c8-156">これで、資産管理のプロジェクト設定で、親プロジェクトに顧客アカウントをリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="d13c8-157">**資産管理 \> 設定 \> 作業指示書 \> プロジェクト設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="d13c8-158">**親プロジェクト** タブで、**追加** を選択して新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="d13c8-159">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d13c8-160">**顧客アカウント:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="d13c8-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="d13c8-161">**プロジェクト ID:** 前にメモしたプロジェクト IDを入力します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="d13c8-162">手順 5: プロジェクト グループをリンクし、作業指示書プロジェクトに入力する</span><span class="sxs-lookup"><span data-stu-id="d13c8-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="d13c8-163">まだ、**プロジェクトの設定** ページ (**資産管理 \> 設定 \> 作業指示書 \> プロジェクトの設定**) が表示されているはずです。</span><span class="sxs-lookup"><span data-stu-id="d13c8-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="d13c8-164">**プロジェクト グループ** タブで、**追加** を選択して新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="d13c8-165">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d13c8-166">**作業指示書タイプ:** *サービス* (以前に作成した作業指示書タイプ)</span><span class="sxs-lookup"><span data-stu-id="d13c8-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="d13c8-167">**プロジェクト グループ:** *TM*</span><span class="sxs-lookup"><span data-stu-id="d13c8-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="d13c8-168">作業指示書プロジェクトのプロジェクト契約は、常に親プロジェクトから継承されます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="d13c8-169">手順 6: 顧客 ID に資産をリンクする</span><span class="sxs-lookup"><span data-stu-id="d13c8-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="d13c8-170">**資産管理 \> 資産 \> 有効な資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="d13c8-171">**フィルター** フィールドに *VE-102* と入力し、**資産** によるフィルターを選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="d13c8-172">資産を選択して設定を開きます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="d13c8-173">**顧客** クイック タブで、**顧客アカウント** フィールドを *US-013* (*Pelican Wholesales*) に設定します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="d13c8-174">**名前** フィールドが、自動的に *Pelican Wholesales* に更新されます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="d13c8-175">手順 7: 資産で新しい作業指示書を作成する</span><span class="sxs-lookup"><span data-stu-id="d13c8-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="d13c8-176">**資産管理 \> 作業指示書 \> 有効な作業指示書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="d13c8-177">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d13c8-178">**作業指示書の作成** ダイアログ ボックスで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="d13c8-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d13c8-179">**作業指示書タイプ:** *サービス*</span><span class="sxs-lookup"><span data-stu-id="d13c8-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="d13c8-180">**説明:** *修理トラック*</span><span class="sxs-lookup"><span data-stu-id="d13c8-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="d13c8-181">**顧客アカウント:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="d13c8-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="d13c8-182">**資産:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="d13c8-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="d13c8-183">ルックアップには、選択した顧客アカウントにリンクされている資産だけが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="d13c8-184">**メンテナンス作業タイプ** *修理*</span><span class="sxs-lookup"><span data-stu-id="d13c8-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="d13c8-185">**取引:** *整備士*</span><span class="sxs-lookup"><span data-stu-id="d13c8-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="d13c8-186">**サービス レベル:** *4*</span><span class="sxs-lookup"><span data-stu-id="d13c8-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="d13c8-187">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="d13c8-188">手順 8: 作業指示書を確認し、作業を開始する</span><span class="sxs-lookup"><span data-stu-id="d13c8-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="d13c8-189">このセクションでは、前のセクションで作成した作業指示書に従って作業します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="d13c8-190">次の手順に従って、親プロジェクトが *Pelican wholesales 作業指示書* プロジェクトであることを確認します:</span><span class="sxs-lookup"><span data-stu-id="d13c8-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="d13c8-191">**作業指示書メンテナンス作業** セクションで、行を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="d13c8-192">**行の詳細** クイックタブで、**プロジェクト ID** の値を検査します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="d13c8-193">*\<Parent-Project-ID\>-\<Project-ID\>* 形式のハイフン付き番号である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="d13c8-194">この値はリンクです。</span><span class="sxs-lookup"><span data-stu-id="d13c8-194">This value is a link.</span></span>
    1. <span data-ttu-id="d13c8-195">プロジェクト ID リンクを選択して、親プロジェクトとプロジェクト名を表示できるページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="d13c8-196">アクション ペインにある **作業指示書** タブの **ライフサイクルの状態** グループで、**作業指示書の状態の更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="d13c8-197">**作業指示書の状態の更新** ダイアログ ボックスにある **選択** 列で、**ライフサイクルの状態** フィールドが *処理中* に設定されている行のチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="d13c8-198">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-198">Select **OK**.</span></span>
1. <span data-ttu-id="d13c8-199">**ライフサイクルの状態: InProgress** ダイアログ ボックスで **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="d13c8-200">手順 9: 作業指示書に費やした時間を記入し、新しい仮発行請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="d13c8-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="d13c8-201">このセクションでは、前のセクションで取り組んだ作業指示書の作業を続けます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="d13c8-202">アクション ペインにある **作業指示書** タブの **プロジェクト** グループで **仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="d13c8-203">**作業指示書仕訳帳** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="d13c8-204">ここでは、作業指示書に費やした時間を登録できます。</span><span class="sxs-lookup"><span data-stu-id="d13c8-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="d13c8-205">**時間** クイックタブの **行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="d13c8-206">新しい行で、**時間** フィールドを *4* に設定します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="d13c8-207">アクション ペインで、**仕訳帳の転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="d13c8-208">**作業指示書仕訳帳** ページを閉じて、作業指示書に戻ります。</span><span class="sxs-lookup"><span data-stu-id="d13c8-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="d13c8-209">アクション ペインの **請求** タブで、**新しい仮発行請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="d13c8-210">**仮発行請求書の作成** ダイアログ ボックスの **プロジェクト トランザクション** セクションで、請求を行うすべての行に対して **選択** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="d13c8-211">**OK** を選択してダイアログ ボックスを閉じ、新しい仮発行請求書を表示します。</span><span class="sxs-lookup"><span data-stu-id="d13c8-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]