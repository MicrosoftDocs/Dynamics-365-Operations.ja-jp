---
title: ピッキングと梱包のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management でピッキングおよび梱包する際に発生する可能性がある一般的な問題の修正方法について説明します。
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
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993936"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="9479a-103">ピッキングと梱包のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9479a-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9479a-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management でピッキングおよび梱包する際に発生する可能性がある一般的な問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9479a-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="9479a-105">エラー メッセージ "分析コード シリアル番号が設定されている場合、分析コードの場所を空白にすることはできません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-106">Issue description</span></span>

<span data-ttu-id="9479a-107">このエラー メッセージは、高度な倉庫管理 (WMS) が有効になっている倉庫を使用してシリアル品目の移動オーダーを作成し、作業が完了した後、出荷を確認しようとした場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-108">Issue resolution</span></span>

<span data-ttu-id="9479a-109">"移動元" 倉庫の流通倉庫の **既定の受入場所** フィールドが空白になっています。</span><span class="sxs-lookup"><span data-stu-id="9479a-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="9479a-110">この問題を解決するには、流通倉庫の既定の受入場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="9479a-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="9479a-111">この場所がライセンス プレートによって制御されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9479a-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="9479a-112">"ライセンス プレートが無効です" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-113">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-113">Issue description</span></span>

<span data-ttu-id="9479a-114">ライセンス プレート ID をスキャンすると、倉庫アプリでこのエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-115">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-115">Issue resolution</span></span>

<span data-ttu-id="9479a-116">ライセンス プレート ID がライセンス プレート テーブルに存在し、ライセンス プレートの品目と数量が使用可能である (つまりブロックされていない) ことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9479a-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="9479a-117">エラー メッセージ "フィールド \[積載重量\] (=-%1) には正の数のみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9479a-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="9479a-118">更新はキャンセルされました" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-119">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-119">Issue description</span></span>

<span data-ttu-id="9479a-120">梱包場所からステージング場所への作業またはステージング場所からドッキング場所への作業を処理するときに未処理の作業がある場合に、このエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-121">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-121">Issue resolution</span></span>

<span data-ttu-id="9479a-122">この問題を解決するには、**システム管理 \> 定期タスク \>データベース \> 整合性チェック** を実行し、**倉庫積荷重量の整合性チェック** のプロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="9479a-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="9479a-123">"単位 %1 の数量が有効ではありません" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-124">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-124">Issue description</span></span>

<span data-ttu-id="9479a-125">複数のバッチ間で *分割ピッキング* を実行しようとすると、このエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-126">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-126">Issue resolution</span></span>

<span data-ttu-id="9479a-127">倉庫の作業者は、倉庫アプリで *ショート ピッキング* プロセスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9479a-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="9479a-128">同じ場所から複数のバッチを選択する場合は、ウェアハウス アプリの **完全** オプションを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="9479a-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="9479a-129">ライセンス プレートとして管理されている場所に在庫を移動できません。</span><span class="sxs-lookup"><span data-stu-id="9479a-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-130">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-130">Issue description</span></span>

<span data-ttu-id="9479a-131">積荷のピッキング済数量を減少させることはできません。</span><span class="sxs-lookup"><span data-stu-id="9479a-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-132">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-132">Issue resolution</span></span>

<span data-ttu-id="9479a-133">以前のバージョンでは、積荷のピッキング済数量を減少させることはできません。</span><span class="sxs-lookup"><span data-stu-id="9479a-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="9479a-134">ただし、現在では、ライセンス プレートによって制御された場所にピッキング解除できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9479a-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="9479a-135">**ピッキング済数量の削減** ページでは、**場所** 値と **ライセンス プレート** 値の両方を積荷明細行に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9479a-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="9479a-136">納品書を印刷することはできますか。または倉庫でコンテンツを梱包できますか。</span><span class="sxs-lookup"><span data-stu-id="9479a-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-137">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-137">Issue description</span></span>

<span data-ttu-id="9479a-138">**作業監査テンプレート行の更新** ページで、倉庫またはサイト別に納品書または梱包コンテンツを印刷しようとしています。</span><span class="sxs-lookup"><span data-stu-id="9479a-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-139">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-139">Issue resolution</span></span>

<span data-ttu-id="9479a-140">印刷管理設定を使用してドキュメントを印刷する場合は、**作業監査テンプレート行の更新** ページの **印刷設定の編集** を選択するのではなく、印刷管理を使用してスコープ (サイト/倉庫) を制限します。</span><span class="sxs-lookup"><span data-stu-id="9479a-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="9479a-141">販売注文から転記された後に梱包明細をキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="9479a-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-142">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-142">Issue description</span></span>

<span data-ttu-id="9479a-143">WMS に対してピッキングおよび出荷プロセスが有効になっている場合は、販売注文から転記された後に梱包明細をキャンセルすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9479a-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-144">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-144">Issue resolution</span></span>

<span data-ttu-id="9479a-145">WMS が有効になっている品目に対して転記された梱包明細を修正するには、注文からではなく、積荷から転記を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9479a-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="9479a-146">Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。</span><span class="sxs-lookup"><span data-stu-id="9479a-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="9479a-147">一般に、倉庫管理プロセスを通じてピッキングおよび出荷された販売注文は、梱包明細として、積荷または出荷と販売注文ドキュメント自体から更新することができます。</span><span class="sxs-lookup"><span data-stu-id="9479a-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="9479a-148">ただし、梱包明細の販売注文を販売注文ドキュメントから更新した場合は、梱包明細の取消を、積荷または販売注文から行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="9479a-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="9479a-149">したがって、積荷から梱包明細の転記を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9479a-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="9479a-150">この場合、積荷から実行する必要がある取消が有効になります。</span><span class="sxs-lookup"><span data-stu-id="9479a-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="9479a-151">エラー メッセージ "クラスターのための十分な作業が見つかりません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9479a-152">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9479a-152">Issue description</span></span>

<span data-ttu-id="9479a-153">*システム主導のクラスター ピッキング* プロセスを使用するとき、(たとえば 10 個の職位をピッキング可能な) クラスター プロファイルを構成している場合は、10 個の職位にピッキングするために十分な作業があればそのプロセスは計画どおりに機能します。</span><span class="sxs-lookup"><span data-stu-id="9479a-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="9479a-154">ただし、ピッキングする職位が 8 しかない場合、1 つのクラスターに十分な作業がないので、このエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9479a-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9479a-155">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9479a-155">Issue resolution</span></span>

<span data-ttu-id="9479a-156">この問題を修正するには、クラスター プロファイルを編集し、**職位のアクティブ化** オプションを *いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="9479a-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
