---
title: オンラインの販売と支払の転記
description: この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802674"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="c7567-103">オンラインの販売と支払の転記</span><span class="sxs-lookup"><span data-stu-id="c7567-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7567-104">この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c7567-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="c7567-105">オンライン販売と支払の転記は、2 段階のプロセスで行われます。</span><span class="sxs-lookup"><span data-stu-id="c7567-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="c7567-106">HQ でオンライン コマース トランザクション データを引き出します。</span><span class="sxs-lookup"><span data-stu-id="c7567-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="c7567-107">HQ でオーダーを同期させて、販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="c7567-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="c7567-108">オンライン トランザクション データの取得は、手動で P ジョブを実行することによって、または反復バッチ ジョブを作成することによって行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="c7567-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="c7567-109">手動による P ジョブの実行</span><span class="sxs-lookup"><span data-stu-id="c7567-109">Manually running the P-job</span></span>

1. <span data-ttu-id="c7567-110">すべてのワークスペース > Retail とコマース IT に移動します。</span><span class="sxs-lookup"><span data-stu-id="c7567-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="c7567-111">配送スケジュールをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="c7567-112">P-0001 を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-112">Select P-0001.</span></span>
4. <span data-ttu-id="c7567-113">必要に応じて、チャネル データベース グループを調整します。</span><span class="sxs-lookup"><span data-stu-id="c7567-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="c7567-114">今すぐ実行をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-114">Click Run now.</span></span>
6. <span data-ttu-id="c7567-115">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="c7567-116">定期的な P ジョブのスケジューリング</span><span class="sxs-lookup"><span data-stu-id="c7567-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="c7567-117">すべてのワークスペース > Retail とコマース IT に移動します。</span><span class="sxs-lookup"><span data-stu-id="c7567-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="c7567-118">配送スケジュールをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="c7567-119">P-0001 を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-119">Select P-0001.</span></span>
4. <span data-ttu-id="c7567-120">バッチ ジョブの作成をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-120">Click Create batch job.</span></span>
5. <span data-ttu-id="c7567-121">バックグラウンドで実行をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-121">Click Run in the background.</span></span>
5. <span data-ttu-id="c7567-122">バッチ処理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c7567-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="c7567-123">再実行をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-123">Click Recurrence..</span></span>
7. <span data-ttu-id="c7567-124">[終了日なし] のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-124">Select the No end date option.</span></span>
8. <span data-ttu-id="c7567-125">カウント フィールドで、実行の間隔を分単位で入力します。</span><span class="sxs-lookup"><span data-stu-id="c7567-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="c7567-126">通常、これは 5-10 になります。</span><span class="sxs-lookup"><span data-stu-id="c7567-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="c7567-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-127">Click OK.</span></span>
10. <span data-ttu-id="c7567-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-128">Click OK.</span></span>

<span data-ttu-id="c7567-129">注文を同期するには、「同期注文」ジョブを手動で実行するか、定期的なバッチジョブを作成します。</span><span class="sxs-lookup"><span data-stu-id="c7567-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="c7567-130">注文の同期を手動で実行</span><span class="sxs-lookup"><span data-stu-id="c7567-130">Manually running order synchronization</span></span> 

<span data-ttu-id="c7567-131">「注文の同期」ジョブを一度手動で実行するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c7567-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="c7567-132">すべてのワークスペース > 店舗の財務に移動します。</span><span class="sxs-lookup"><span data-stu-id="c7567-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="c7567-133">[注文の同期] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="c7567-134">組織階層のフィールドで、'地域ごとの店舗' を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="c7567-135">店舗グループのバッチ ジョブを作成する場合は、特定のオンライン ストアまたはノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c7567-136">選択した項目を追加するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="c7567-137">[バックグラウンドで実行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="c7567-138">バッチ処理を無効にする</span><span class="sxs-lookup"><span data-stu-id="c7567-138">Disable Batch processing</span></span>
6. <span data-ttu-id="c7567-139">[再実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-139">Click Recurrence.</span></span>
7. <span data-ttu-id="c7567-140">後に終了オプションを選択</span><span class="sxs-lookup"><span data-stu-id="c7567-140">Select End After option</span></span>
8. <span data-ttu-id="c7567-141">後に終了フィールドに、1 と入力します。</span><span class="sxs-lookup"><span data-stu-id="c7567-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="c7567-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-142">Click OK.</span></span>
10. <span data-ttu-id="c7567-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="c7567-144">繰返し注文の同期をスケジューリングする</span><span class="sxs-lookup"><span data-stu-id="c7567-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="c7567-145">この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c7567-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="c7567-146">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="c7567-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c7567-147">すべてのワークスペース > 店舗の財務に移動します。</span><span class="sxs-lookup"><span data-stu-id="c7567-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="c7567-148">[注文の同期] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="c7567-149">組織階層のフィールドで、'地域ごとの店舗' を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="c7567-150">店舗グループのバッチ ジョブを作成する場合は、特定のオンライン ストアまたはノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c7567-151">選択した項目を追加するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="c7567-152">[バックグラウンドで実行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="c7567-153">バッチ処理を有効にする</span><span class="sxs-lookup"><span data-stu-id="c7567-153">Enable Batch processing</span></span>
6. <span data-ttu-id="c7567-154">[再実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-154">Click Recurrence.</span></span>
7. <span data-ttu-id="c7567-155">[終了日なし] のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c7567-155">Select the No end date option.</span></span>
8. <span data-ttu-id="c7567-156">カウント フィールドで、実行の間隔を分単位で入力します。</span><span class="sxs-lookup"><span data-stu-id="c7567-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="c7567-157">通常、これは 2-20 になります</span><span class="sxs-lookup"><span data-stu-id="c7567-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="c7567-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-158">Click OK.</span></span>
10. <span data-ttu-id="c7567-159">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7567-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="c7567-160">プロセスに含まれるデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="c7567-160">Data entities involved in the process</span></span>

- <span data-ttu-id="c7567-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="c7567-161">RetailTransactionTable</span></span>
- <span data-ttu-id="c7567-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="c7567-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="c7567-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="c7567-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="c7567-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="c7567-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="c7567-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="c7567-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="c7567-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="c7567-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="c7567-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="c7567-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="c7567-171">RetailTransactionAttributeTrans</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]