---
title: プロジェクトの発注書
description: この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。 発注書を作成する方法は、発注書の目的、購入する品目の消費時期、プロジェクトに請求される時期で決まります。
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174561"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="8e7c3-104">プロジェクトの発注書</span><span class="sxs-lookup"><span data-stu-id="8e7c3-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e7c3-105">この記事では、プロジェクトの発注書を作成するために使用できるさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="8e7c3-106">発注書を作成する方法は、発注書の目的、購入する品目の消費時期、プロジェクトに請求される時期で決まります。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="8e7c3-107">発注書を作成する方法</span><span class="sxs-lookup"><span data-stu-id="8e7c3-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="8e7c3-108">プロジェクト管理と会計で発注書を作成するには、次の方法のうち 1 つを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="8e7c3-109">発注書の目的は、発注書が消費される時点、つまり品目がプロジェクトで請求される時点を決定することです。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e7c3-110">方式</span><span class="sxs-lookup"><span data-stu-id="8e7c3-110">Method</span></span></th>
<th><span data-ttu-id="8e7c3-111">目的</span><span class="sxs-lookup"><span data-stu-id="8e7c3-111">Purpose</span></span></th>
<th><span data-ttu-id="8e7c3-112">品目の消費</span><span class="sxs-lookup"><span data-stu-id="8e7c3-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e7c3-113">プロジェクトからの発注書を直接作成します。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="8e7c3-114">プロジェクトでの消費用に外部仕入先から品目を購買するには、この方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="8e7c3-115">発注書を次の 2 つの方法で作成できます。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="8e7c3-116">プロジェクト自体から作成します。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-116">From the project itself.</span></span> <span data-ttu-id="8e7c3-117">この場合、プロジェクトはすでに発注書のために定義されています。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="8e7c3-118">プロジェクト発注書に移動することで作成します。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="8e7c3-119">発注書の作成対象となる仕入先とプロジェクトを両方とも選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="8e7c3-120">品目は、仕入先請求書が更新された時点で消費されます。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e7c3-121">販売注文から発注書を作成する。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="8e7c3-122">プロジェクトから販売注文を作成する際に品目を購買する場合は、この方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="8e7c3-123">品目は、販売注文が顧客に請求された時点で消費されます。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e7c3-124">在庫品目要求から発注書を作成する。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="8e7c3-125">プロジェクトから在庫品目要求を作成する際に品目を購買する場合は、この方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="8e7c3-126">品目は、在庫品目要求梱包明細が更新された時点で消費されます。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="8e7c3-127">仕入先請求書または梱包明細を更新するときに、在庫品目要求の梱包明細を更新するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="8e7c3-128">詳細については、「[在庫品目要求から発注書の品目を受け取る](tasks/receive-items-purchase-order-item-requirement.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e7c3-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

