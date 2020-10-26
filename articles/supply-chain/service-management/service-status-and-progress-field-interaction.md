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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94f2df6a4ddb71a29ff951dfe38618ac7762783
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975491"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="306da-103">サービスのステータスと進捗状況フィールドの相互作用</span><span class="sxs-lookup"><span data-stu-id="306da-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="306da-104">**ステータス**では、サービス注文ヘッダーの**進捗状況**フィールドがサービス注文全体のステータスを反映し、**ステータス**レポートが個々のサービス注文明細行のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="306da-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="306da-105">進捗状況</span><span class="sxs-lookup"><span data-stu-id="306da-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="306da-106">明細行 1 のステータス</span><span class="sxs-lookup"><span data-stu-id="306da-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="306da-107">明細行 2 のステータス</span><span class="sxs-lookup"><span data-stu-id="306da-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="306da-108">明細行 3 のステータス</span><span class="sxs-lookup"><span data-stu-id="306da-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="306da-109"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="306da-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-110"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-111"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-112"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="306da-113"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="306da-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-114"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-115"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-116"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="306da-117"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="306da-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-118"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-119"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-120"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="306da-121"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-122"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-123"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-124"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="306da-125"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-126"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-127"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-128"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="306da-129"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-130"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-131"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="306da-132"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="306da-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="306da-133">すべての明細行のステータスが**作成済**の場合、サービス注文の進捗状況は進行中であり、一部の明細行のステータスが**キャンセル済**または**転記済**の場合も進行中です。</span><span class="sxs-lookup"><span data-stu-id="306da-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="306da-134">サービス注文のすべての明細行が**転記済**とマークされている場合、サービス注文の進捗状況は**転記済**です。</span><span class="sxs-lookup"><span data-stu-id="306da-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="306da-135">一部の明細行が**転記済**で、一部の明細行が**キャンセル済**の場合も、進捗状況は**転記済**です。</span><span class="sxs-lookup"><span data-stu-id="306da-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


