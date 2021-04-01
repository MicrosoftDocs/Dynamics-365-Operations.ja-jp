---
title: 積荷構築と出荷のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での積荷構築と出荷の処理中に発生する可能性がある問題を修正する方法について説明します。
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
ms.openlocfilehash: c7dc9cc9de4d5089d497c36759931669ee2e9e55
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259509"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="ca3e7-103">積荷構築と出荷のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ca3e7-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca3e7-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での積荷構築と出荷の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="ca3e7-105">"無効な在庫分析コードがあるため、この注文明細行には積荷明細行を作成できません" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca3e7-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="ca3e7-106">Issue description</span></span>

<span data-ttu-id="ca3e7-107">返品販売注文を倉庫にリリースするときに、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="ca3e7-108">無効な在庫分析コードがあるため、この注文明細行には積荷明細行を作成できません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="ca3e7-109">引当階層の場所分析コードの下に配置されている在庫分析コードを参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="ca3e7-110">無効な分析コードを注文明細行から削除します。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca3e7-111">問題の解決</span><span class="sxs-lookup"><span data-stu-id="ca3e7-111">Issue resolution</span></span>

<span data-ttu-id="ca3e7-112">残念ながら、この製品は、販売返品プロセスの積荷プロセスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="ca3e7-113">したがって、返品販売注文を倉庫にリリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="ca3e7-114">販売注文トランザクションで、引当階層の **場所** 分析コードの下に配置されている在庫分析コードを参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="ca3e7-115">無効な分析コードを注文明細行から削除すると解決できます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="ca3e7-116">エラー メッセージ "いずれかの明細行が既に積荷にあります。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="ca3e7-117">倉庫にリリースできません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca3e7-118">問題の説明</span><span class="sxs-lookup"><span data-stu-id="ca3e7-118">Issue description</span></span>

<span data-ttu-id="ca3e7-119">手動で積荷を作成する場合、または販売注文明細行のエントリが発生する前に積荷を作成するようにプロセスを設定した場合は、後続のリリースが手動で行われること、および積荷からの工順と評価が使用されることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="ca3e7-120">倉庫に対して自動リリースを実行しようとしたが、ウェーブ プロセスで作業を作成できなかった、というシナリオも考えられます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="ca3e7-121">したがって、この場合も未処理の出荷または積荷が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="ca3e7-122">その場合、未処理の出荷または積荷を削除するか、ウェーブを手動で再処理するまで、この未処理の出荷または積荷により、自動的に注文をリリースする試みがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca3e7-123">問題の解決</span><span class="sxs-lookup"><span data-stu-id="ca3e7-123">Issue resolution</span></span>

<span data-ttu-id="ca3e7-124">倉庫へのリリース前に負荷が存在しない場合にのみ、販売注文ページからリリースするか、販売注文のリリース ページから自動リリースを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="ca3e7-125">ウェーブが処理されると、自動的に積荷が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="ca3e7-126">エラー メッセージ "納品書の修正を処理できません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="ca3e7-127">納品書の修正でサポートされていないために倉庫管理プロセスの対象となる品目のみが納品書に含まれています" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca3e7-128">問題の説明</span><span class="sxs-lookup"><span data-stu-id="ca3e7-128">Issue description</span></span>

<span data-ttu-id="ca3e7-129">**キャンセル** ボタンが使用できないため、納品書を転記した後にキャンセルすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="ca3e7-130">また、納品書を修正することもできません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="ca3e7-131">実行しようとすると、このエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca3e7-132">問題の解決</span><span class="sxs-lookup"><span data-stu-id="ca3e7-132">Issue resolution</span></span>

<span data-ttu-id="ca3e7-133">高度な倉庫管理 (WMS) が有効になっている品目に対して転記された梱包明細を修正するには、注文から直接ではなく、積荷から転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="ca3e7-134">ウェーブではなく出庫積荷から作業を作成する方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca3e7-135">問題の説明</span><span class="sxs-lookup"><span data-stu-id="ca3e7-135">Issue description</span></span>

<span data-ttu-id="ca3e7-136">この問題を再現する 1 つの方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="ca3e7-137">販売注文または移動オーダーを使用して、出庫積荷を手動で作成します。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="ca3e7-138">積荷を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="ca3e7-139">ピッキング作業がまだ生成されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca3e7-140">問題の解決</span><span class="sxs-lookup"><span data-stu-id="ca3e7-140">Issue resolution</span></span>

<span data-ttu-id="ca3e7-141">積荷がリリースされたときに作業をすぐに生成する必要がある場合は、それに応じてウェーブ テンプレートを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="ca3e7-142">ウェーブ テンプレートでは、次のオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="ca3e7-143">ウェーブの作成を自動化</span><span class="sxs-lookup"><span data-stu-id="ca3e7-143">Automate wave creation</span></span>
- <span data-ttu-id="ca3e7-144">倉庫へのリリース時にウェーブを処理する</span><span class="sxs-lookup"><span data-stu-id="ca3e7-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="ca3e7-145">ウェーブを自動的にリリースする</span><span class="sxs-lookup"><span data-stu-id="ca3e7-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="ca3e7-146">部分的に出荷された積荷を再リリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca3e7-147">問題の説明</span><span class="sxs-lookup"><span data-stu-id="ca3e7-147">Issue description</span></span>

<span data-ttu-id="ca3e7-148">部分的に出荷された積荷を倉庫にリリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="ca3e7-149">倉庫にリリースすると、"操作完了" のメッセージが表示されますが、何も発生せず、残りの数量に対して作業が作成されません。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="ca3e7-150">この問題は、輸送積荷機能を使用しているときに不完全な引当がある場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca3e7-151">問題の解決</span><span class="sxs-lookup"><span data-stu-id="ca3e7-151">Issue resolution</span></span>

<span data-ttu-id="ca3e7-152">[KB の問題 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("部分的に出荷された積荷が再ウェーブおよび再処理される") は[リリース 10.0.15](../get-started/whats-new-scm-10-0-15.md) で修正されています。</span><span class="sxs-lookup"><span data-stu-id="ca3e7-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]