---
title: 出庫倉庫操作のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での出庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。
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
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993981"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="f14b1-103">出庫倉庫操作のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f14b1-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f14b1-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での出庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f14b1-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="f14b1-105">エラー メッセージ "販売注文をリリースできませんでした" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f14b1-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f14b1-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="f14b1-106">Issue description</span></span>

<span data-ttu-id="f14b1-107">この問題は、いくつかの理由で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f14b1-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="f14b1-108">たとえば、与信管理保留中の注文で、販売注文に関連付けられているすべての販売明細行に有効な住所が入力されるまで出荷を作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="f14b1-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="f14b1-109">また、注文を倉庫にリリースする前に対応する必要がある注文保留もあります。</span><span class="sxs-lookup"><span data-stu-id="f14b1-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="f14b1-110">この保留は注文固有の場合もありますが、顧客 ID に含まれている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="f14b1-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f14b1-111">問題の解決</span><span class="sxs-lookup"><span data-stu-id="f14b1-111">Issue resolution</span></span>

<span data-ttu-id="f14b1-112">販売注文と注文明細行の住所を追加または更新し、注文を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="f14b1-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="f14b1-113">注文は、有効な配送先住所がある場合にのみ倉庫にリリースできます (**組織管理** モジュールでの住所形式の設定に従って)。</span><span class="sxs-lookup"><span data-stu-id="f14b1-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="f14b1-114">注文の保留を調査し、問題に対処します。</span><span class="sxs-lookup"><span data-stu-id="f14b1-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="f14b1-115">次に、注文または顧客から保留を削除し、注文を倉庫に解放します。</span><span class="sxs-lookup"><span data-stu-id="f14b1-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="f14b1-116">メッセージ "積荷 1% の出荷が確認されました" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f14b1-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="f14b1-117">ただし、明細行は転記されません。</span><span class="sxs-lookup"><span data-stu-id="f14b1-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f14b1-118">問題の説明</span><span class="sxs-lookup"><span data-stu-id="f14b1-118">Issue description</span></span>

<span data-ttu-id="f14b1-119">積荷の出荷が確認されましたが、それ以上転記は行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="f14b1-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f14b1-120">問題の解決</span><span class="sxs-lookup"><span data-stu-id="f14b1-120">Issue resolution</span></span>

<span data-ttu-id="f14b1-121">出荷確認は転記に影響しません。</span><span class="sxs-lookup"><span data-stu-id="f14b1-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="f14b1-122">出荷と積荷のステータスが更新されるだけです。</span><span class="sxs-lookup"><span data-stu-id="f14b1-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="f14b1-123">転記は、別のプロセスで行われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f14b1-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="f14b1-124">エラー メッセージ "倉庫管理が有効になっているため、倉庫 1% に対して直納を処理できません。</span><span class="sxs-lookup"><span data-stu-id="f14b1-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="f14b1-125">倉庫管理で有効になっていない別の倉庫を指定してください" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f14b1-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f14b1-126">問題の説明</span><span class="sxs-lookup"><span data-stu-id="f14b1-126">Issue description</span></span>

<span data-ttu-id="f14b1-127">倉庫管理 (WMS) が有効になっている倉庫から直送するための品目が販売明細行に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f14b1-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="f14b1-128">販売明細行が更新されると、このエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f14b1-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="f14b1-129">問題の解決</span><span class="sxs-lookup"><span data-stu-id="f14b1-129">Issue resolution</span></span>

<span data-ttu-id="f14b1-130">Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。</span><span class="sxs-lookup"><span data-stu-id="f14b1-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f14b1-131">現時点では、WMS は直接配送をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f14b1-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="f14b1-132">したがって、直納を使用するには、WMS 以外の品目および倉庫を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f14b1-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
