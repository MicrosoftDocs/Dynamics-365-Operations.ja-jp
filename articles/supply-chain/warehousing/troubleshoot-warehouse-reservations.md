---
title: 倉庫管理での引当のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。
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
ms.openlocfilehash: a9a5d20732a802fc58c392853af8334bbc07de73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248718"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="7b0f2-103">倉庫管理での引当のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="7b0f2-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b0f2-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="7b0f2-105">"予約に依存する作業が作成されているため、"引当を削除できません" というエラー メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7b0f2-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="7b0f2-106">Issue description</span></span>

<span data-ttu-id="7b0f2-107">販売明細行に対して未処理の作業があるため、その販売明細行の在庫引当を解除できません。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7b0f2-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="7b0f2-108">Issue resolution</span></span>

<span data-ttu-id="7b0f2-109">未処理の梱包グループ作業があるかどうかを調べて、品目を梱包ステーションから別の場所 (*Baydoor* など) に移動します。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="7b0f2-110">**作業の作成履歴ログ** ページと **作業の詳細** ページのレコードを確認して、在庫が物理的に引当されているかどうかを確認し、その作業を完了または削除して引当を解放します。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="7b0f2-111">エラー メッセージ "品目 %2 の在庫トランザクションが不足しているため、在庫数量 - %1 を更新できませんでした...." が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7b0f2-112">問題の説明</span><span class="sxs-lookup"><span data-stu-id="7b0f2-112">Issue description</span></span>

<span data-ttu-id="7b0f2-113">この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="7b0f2-114">次に、完全なエラー メッセージの全文を示します。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="7b0f2-115">品目 %2 (分析コード サイズ=%3、色=%4、追加=%5、サイト=%6、倉庫=%7、場所=%8、在庫ステータス=あり、ライセンス プレート=%9、ロット ID %12 での参照 ID %11 のバッチ番号=%10) の在庫トランザクションが不足しているため、在庫数量 -%1 を更新できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7b0f2-116">問題の解決</span><span class="sxs-lookup"><span data-stu-id="7b0f2-116">Issue resolution</span></span>

<span data-ttu-id="7b0f2-117">在庫トランザクションで、数量が物理的に引当されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="7b0f2-118">たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="7b0f2-119">エラー メッセージ "在庫で使用できるのは 0.00 のみであるため、現物手持在庫...を引当することはできません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7b0f2-120">問題の説明</span><span class="sxs-lookup"><span data-stu-id="7b0f2-120">Issue description</span></span>

<span data-ttu-id="7b0f2-121">この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="7b0f2-122">次に、完全なエラー メッセージの全文を示します。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="7b0f2-123">在庫で使用できるのは 0.00 のみであるため、現物手持在庫 (サイト=%1、倉庫=%2、在庫ステータス=あり、バッチ番号=%3、所有者=%4: %5) を引当することはできません。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7b0f2-124">問題の解決</span><span class="sxs-lookup"><span data-stu-id="7b0f2-124">Issue resolution</span></span>

<span data-ttu-id="7b0f2-125">この問題は、未処理の作業が原因で発生している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="7b0f2-126">作業を完了するか、作業の作成を行わずに入庫します。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="7b0f2-127">在庫トランザクションで、数量が物理的に引当されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="7b0f2-128">たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="7b0f2-129">エラー メッセージ "ウェーブに割り当てるには、積荷明細行は、その場所より上の分析コードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="7b0f2-130">これらの分析コードを割り当てるには、積荷明細行を準備して再作成します" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7b0f2-131">問題の説明</span><span class="sxs-lookup"><span data-stu-id="7b0f2-131">Issue description</span></span>

<span data-ttu-id="7b0f2-132">"上のバッチ" 引当階層を持つ品目 (**場所** 分析コードの *上* に **バッチ番号** 分析コードが配置されている) を使用すると、部分数量に対する **積荷計画ワークベンチ** ページの **倉庫にリリース** コマンドが機能しません。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="7b0f2-133">このエラー メッセージが表示され、部分数量に対して作業が作成されません。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="7b0f2-134">ただし、"下のバッチ" 引当階層を持つ品目 (**場所** 分析コードの *下* に **バッチ番号** 分析コードが配置されている) を使用した場合、部分数量に対する **積荷計画ワークベンチ** ページから積荷をリリースできます。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7b0f2-135">問題の解決</span><span class="sxs-lookup"><span data-stu-id="7b0f2-135">Issue resolution</span></span>

<span data-ttu-id="7b0f2-136">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-136">This behavior is by design.</span></span> <span data-ttu-id="7b0f2-137">引当階層で **場所** 分析コードの上に分析コードを配置する場合は、倉庫へのリリース前に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="7b0f2-138">Microsoft は、この問題を評価し、積荷計画ワークベンチから倉庫に対するリリースにおける制限事項であると判断しました。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="7b0f2-139">**場所** の上に 1 つ以上の分析コードが指定されていない場合、部分的な数量をリリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="7b0f2-140">詳細については、[柔軟な倉庫レベル分析コードの引当ポリシー](flexible-warehouse-level-dimension-reservation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b0f2-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]