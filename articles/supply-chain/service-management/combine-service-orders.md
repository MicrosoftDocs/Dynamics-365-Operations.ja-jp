---
title: サービス注文の組み合わせ
description: サービス注文を組み合わせることができます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17fbed59b1fe7bec80f25f74451872efd61bed62
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977003"
---
# <a name="combine-service-orders"></a><span data-ttu-id="a5f27-103">サービス注文の組み合わせ</span><span class="sxs-lookup"><span data-stu-id="a5f27-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a5f27-104">**サービス合意**フォームでサービス注文明細行を自動的に作成する場合、次のいずれかのオプションを選択してそれらをグループ化する方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a5f27-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="a5f27-105">**サービス契約別**</span><span class="sxs-lookup"><span data-stu-id="a5f27-105">**By service agreement**</span></span>

  - <span data-ttu-id="a5f27-106">**サービス作業別**</span><span class="sxs-lookup"><span data-stu-id="a5f27-106">**By service task**</span></span>

  - <span data-ttu-id="a5f27-107">**従業員別**</span><span class="sxs-lookup"><span data-stu-id="a5f27-107">**By employee**</span></span>

  - <span data-ttu-id="a5f27-108">**サービス対象別**</span><span class="sxs-lookup"><span data-stu-id="a5f27-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="a5f27-109">例</span><span class="sxs-lookup"><span data-stu-id="a5f27-109">Example</span></span>

<span data-ttu-id="a5f27-110">開始日が 2007 年 3 月 31 日のサービス合意を作成します。</span><span class="sxs-lookup"><span data-stu-id="a5f27-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="a5f27-111">**サービス注文の組み合わせ**フィールドで、**サービス対象別**を指定します。</span><span class="sxs-lookup"><span data-stu-id="a5f27-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="a5f27-112">その後、次のサービス合意項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="a5f27-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5f27-113">契約明細行番号</span><span class="sxs-lookup"><span data-stu-id="a5f27-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="a5f27-114">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="a5f27-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="a5f27-115">説明</span><span class="sxs-lookup"><span data-stu-id="a5f27-115">Description</span></span></p></th>
<th><p><span data-ttu-id="a5f27-116">間隔</span><span class="sxs-lookup"><span data-stu-id="a5f27-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="a5f27-117">サービス対象</span><span class="sxs-lookup"><span data-stu-id="a5f27-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="a5f27-118">入社日</span><span class="sxs-lookup"><span data-stu-id="a5f27-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f27-119">1</span><span class="sxs-lookup"><span data-stu-id="a5f27-119">1</span></span></p></td>
<td><p><span data-ttu-id="a5f27-120"><strong>時</strong></span><span class="sxs-lookup"><span data-stu-id="a5f27-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f27-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="a5f27-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="a5f27-122">毎週</span><span class="sxs-lookup"><span data-stu-id="a5f27-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="a5f27-123">X-1</span><span class="sxs-lookup"><span data-stu-id="a5f27-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="a5f27-124">2007 - 04 - 01</span><span class="sxs-lookup"><span data-stu-id="a5f27-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f27-125">2</span><span class="sxs-lookup"><span data-stu-id="a5f27-125">2</span></span></p></td>
<td><p><span data-ttu-id="a5f27-126"><strong>時</strong></span><span class="sxs-lookup"><span data-stu-id="a5f27-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f27-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="a5f27-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="a5f27-128">隔週</span><span class="sxs-lookup"><span data-stu-id="a5f27-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="a5f27-129">X-2</span><span class="sxs-lookup"><span data-stu-id="a5f27-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="a5f27-130">2007 - 04 - 01</span><span class="sxs-lookup"><span data-stu-id="a5f27-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f27-131">3</span><span class="sxs-lookup"><span data-stu-id="a5f27-131">3</span></span></p></td>
<td><p><span data-ttu-id="a5f27-132"><strong>時</strong></span><span class="sxs-lookup"><span data-stu-id="a5f27-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f27-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="a5f27-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="a5f27-134">毎週</span><span class="sxs-lookup"><span data-stu-id="a5f27-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="a5f27-135">X-2</span><span class="sxs-lookup"><span data-stu-id="a5f27-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="a5f27-136">2007 - 04 - 01</span><span class="sxs-lookup"><span data-stu-id="a5f27-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5f27-137">どのサービス合意項目でも時間枠は指定しません。</span><span class="sxs-lookup"><span data-stu-id="a5f27-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="a5f27-138">したがって、サービス注文明細行は、該当する算出日から移動しません。</span><span class="sxs-lookup"><span data-stu-id="a5f27-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="a5f27-139">次に、**サービス注文の作成**フォームで 2007 年 4 月 1 日から 2007 年 4 月 30 日までのサービス注文明細行を生成します。</span><span class="sxs-lookup"><span data-stu-id="a5f27-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="a5f27-140">合計で 10 件のサービス注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a5f27-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="a5f27-141">選択した組み合わせの設定が**サービス対象別**であるため、作成されるすべてのサービス注文の明細行が、1 つの特定のサービス対象を含むサービス注文明細行のみになります。</span><span class="sxs-lookup"><span data-stu-id="a5f27-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="a5f27-142">サービス合意から生成され、同じサービス日付と対象を含むサービス注文明細行が、同じサービス注文に組み合わせられます。</span><span class="sxs-lookup"><span data-stu-id="a5f27-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a5f27-143">この例では、<STRONG>サービス管理パラメーター</STRONG>フォームで指定されたカレンダーに休業日がないものとします。</span><span class="sxs-lookup"><span data-stu-id="a5f27-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="a5f27-144">サービス注文明細行をさらにサービス注文にグループ化する場合は、サービス合意項目に対して指定する時間枠に基づきます。</span><span class="sxs-lookup"><span data-stu-id="a5f27-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5f27-145">参照</span><span class="sxs-lookup"><span data-stu-id="a5f27-145">See also</span></span>

[<span data-ttu-id="a5f27-146">サービス注文の自動作成</span><span class="sxs-lookup"><span data-stu-id="a5f27-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


