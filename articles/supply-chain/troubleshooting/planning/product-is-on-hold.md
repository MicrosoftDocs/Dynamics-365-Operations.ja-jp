---
title: トランザクションの製品が保留中の場合
description: 計画オーダーを確定すると、トランザクションの品目が保留中であることを示すエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301282"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="402f1-103">トランザクションの製品が保留中の場合</span><span class="sxs-lookup"><span data-stu-id="402f1-103">Product is on hold for transactions</span></span>

<span data-ttu-id="402f1-104">エラーコード: SYS13295</span><span class="sxs-lookup"><span data-stu-id="402f1-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="402f1-105">現象</span><span class="sxs-lookup"><span data-stu-id="402f1-105">Symptoms</span></span>

<span data-ttu-id="402f1-106">計画オーダーの確定後に、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="402f1-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="402f1-107">品目 %1 は、%2 のトランザクションで保留中です。</span><span class="sxs-lookup"><span data-stu-id="402f1-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="402f1-108">原因</span><span class="sxs-lookup"><span data-stu-id="402f1-108">Cause</span></span>

<span data-ttu-id="402f1-109">ブロックされた品目を説明する際、システムは *ブロック済*、*停止済*、および *保留中* という用語を同じ意味で使用します。</span><span class="sxs-lookup"><span data-stu-id="402f1-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="402f1-110">このエラーは、品目が既定の注文設定で **停止済** に設定されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="402f1-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="402f1-111">品目がブロックされている場合、その品目を発注書または販売注文明細行に追加すると、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="402f1-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="402f1-112">1 つの品目がブロックされると、発注書や販売注文明細行に関連する在庫トランザクションを修正できません (たとえば、梱包明細や請求書を転記したとき)。</span><span class="sxs-lookup"><span data-stu-id="402f1-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="402f1-113">購買した品目をブロックし、同時にその品目を販売することもできます。</span><span class="sxs-lookup"><span data-stu-id="402f1-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="402f1-114">この場合、発注書で **停止済** チェック ボックスが選択されますが、その品目は在庫や販売注文ではブロックされません。</span><span class="sxs-lookup"><span data-stu-id="402f1-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="402f1-115">次に、品目番号の販売がブロックされる可能性のある条件のいくつかを示します:</span><span class="sxs-lookup"><span data-stu-id="402f1-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="402f1-116">品目がまだ開発中または製造中です。</span><span class="sxs-lookup"><span data-stu-id="402f1-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="402f1-117">そのため、販売や予約することは望ましくありません。</span><span class="sxs-lookup"><span data-stu-id="402f1-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="402f1-118">大量の欠陥品目が入庫し、欠陥を修正してから販売する必要があります。</span><span class="sxs-lookup"><span data-stu-id="402f1-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="402f1-119">このような場合は、問題が解決されるまで、この品目をブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="402f1-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="402f1-120">品目がブロックされた場合、返品注文の明細行を作成すると、メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="402f1-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="402f1-121">シリーズ単位またはロット単位で品目をブロックすることはできません。</span><span class="sxs-lookup"><span data-stu-id="402f1-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="402f1-122">品目の一部をブロックする場合は、在庫を移動してブロックするか、当該期間の品目の全在庫をブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="402f1-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="402f1-123">解決策</span><span class="sxs-lookup"><span data-stu-id="402f1-123">Resolution</span></span>

- <span data-ttu-id="402f1-124">品目の **既定の注文設定** ページを開き、**停止済** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="402f1-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
