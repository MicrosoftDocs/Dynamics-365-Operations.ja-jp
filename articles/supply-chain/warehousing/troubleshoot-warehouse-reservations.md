---
title: 倉庫管理での引当のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828109"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="4a4ea-103">倉庫管理での引当のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="4a4ea-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a4ea-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="4a4ea-105">バッチ番号とシリアル番号の登録に関連するトピックについては、[倉庫バッチおよびシリアル予約階層に関するトラブルシューティング](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="4a4ea-106">"予約に依存する作業が作成されているため、"引当を削除できません" というエラー メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4a4ea-107">問題の説明</span><span class="sxs-lookup"><span data-stu-id="4a4ea-107">Issue description</span></span>

<span data-ttu-id="4a4ea-108">販売明細行に対して未処理の作業があるため、その販売明細行の在庫引当を解除できません。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4a4ea-109">問題の解決</span><span class="sxs-lookup"><span data-stu-id="4a4ea-109">Issue resolution</span></span>

<span data-ttu-id="4a4ea-110">未処理の梱包グループ作業があるかどうかを調べて、品目を梱包ステーションから別の場所 (*Baydoor* など) に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="4a4ea-111">**作業の作成履歴ログ** ページと **作業の詳細** ページのレコードを確認して、在庫が物理的に引当されているかどうかを確認し、その作業を完了または削除して引当を解放します。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="4a4ea-112">エラー メッセージ "品目 %2 の在庫トランザクションが不足しているため、在庫数量 - %1 を更新できませんでした...." が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4a4ea-113">問題の説明</span><span class="sxs-lookup"><span data-stu-id="4a4ea-113">Issue description</span></span>

<span data-ttu-id="4a4ea-114">この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="4a4ea-115">次に、完全なエラー メッセージの全文を示します。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="4a4ea-116">品目 %2 (分析コード サイズ=%3、色=%4、追加=%5、サイト=%6、倉庫=%7、場所=%8、在庫ステータス=あり、ライセンス プレート=%9、ロット ID %12 での参照 ID %11 のバッチ番号=%10) の在庫トランザクションが不足しているため、在庫数量 -%1 を更新できませんでした。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4a4ea-117">問題の解決</span><span class="sxs-lookup"><span data-stu-id="4a4ea-117">Issue resolution</span></span>

<span data-ttu-id="4a4ea-118">在庫トランザクションで、数量が物理的に引当されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="4a4ea-119">たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="4a4ea-120">エラー メッセージ "在庫で使用できるのは 0.00 のみであるため、現物手持在庫...を引当することはできません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4a4ea-121">問題の説明</span><span class="sxs-lookup"><span data-stu-id="4a4ea-121">Issue description</span></span>

<span data-ttu-id="4a4ea-122">この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="4a4ea-123">次に、完全なエラー メッセージの全文を示します。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="4a4ea-124">在庫で使用できるのは 0.00 のみであるため、現物手持在庫 (サイト=%1、倉庫=%2、在庫ステータス=あり、バッチ番号=%3、所有者=%4: %5) を引当することはできません。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4a4ea-125">問題の解決</span><span class="sxs-lookup"><span data-stu-id="4a4ea-125">Issue resolution</span></span>

<span data-ttu-id="4a4ea-126">この問題は、未処理の作業が原因で発生している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="4a4ea-127">作業を完了するか、作業の作成を行わずに入庫します。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="4a4ea-128">在庫トランザクションで、数量が物理的に引当されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="4a4ea-129">たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="4a4ea-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
