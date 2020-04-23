---
title: サービスのステータスと進捗状況フィールドの相互作用
description: サービス注文フォームでは、サービス注文ヘッダーの進捗状況フィールドがサービス注文全体のステータスを反映し、ステータス レポートが個々のサービス注文明細行のステータスを示します。
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
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207327"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="f78a3-103">サービスのステータスと進捗状況フィールドの相互作用</span><span class="sxs-lookup"><span data-stu-id="f78a3-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f78a3-104">**ステータス**では、サービス注文ヘッダーの**進捗状況**フィールドがサービス注文全体のステータスを反映し、**ステータス**レポートが個々のサービス注文明細行のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="f78a3-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f78a3-105">進捗状況</span><span class="sxs-lookup"><span data-stu-id="f78a3-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="f78a3-106">明細行 1 のステータス</span><span class="sxs-lookup"><span data-stu-id="f78a3-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="f78a3-107">明細行 2 のステータス</span><span class="sxs-lookup"><span data-stu-id="f78a3-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="f78a3-108">明細行 3 のステータス</span><span class="sxs-lookup"><span data-stu-id="f78a3-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f78a3-109"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-110"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-111"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-112"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f78a3-113"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-114"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-115"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-116"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f78a3-117"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-118"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-119"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-120"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f78a3-121"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-122"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-123"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-124"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f78a3-125"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-126"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-127"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-128"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f78a3-129"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-130"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-131"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="f78a3-132"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="f78a3-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f78a3-133">すべての明細行のステータスが**作成済**の場合、サービス注文の進捗状況は進行中であり、一部の明細行のステータスが**キャンセル済**または**転記済**の場合も進行中です。</span><span class="sxs-lookup"><span data-stu-id="f78a3-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="f78a3-134">サービス注文のすべての明細行が**転記済**とマークされている場合、サービス注文の進捗状況は**転記済**です。</span><span class="sxs-lookup"><span data-stu-id="f78a3-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="f78a3-135">一部の明細行が**転記済**で、一部の明細行が**キャンセル済**の場合も、進捗状況は**転記済**です。</span><span class="sxs-lookup"><span data-stu-id="f78a3-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


