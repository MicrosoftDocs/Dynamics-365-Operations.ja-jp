---
title: サービスのステータスと進捗状況フィールドの相互作用
description: サービス注文フォームでは、サービス注文ヘッダーの進捗状況フィールドがサービス注文全体のステータスを反映し、ステータス レポートが個々のサービス注文明細行のステータスを示します。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a767f4fddb79e720e5466791e984025de16a932a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824465"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="3abd0-103">サービスのステータスと進捗状況フィールドの相互作用</span><span class="sxs-lookup"><span data-stu-id="3abd0-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3abd0-104">**ステータス** では、サービス注文ヘッダーの **進捗状況** フィールドがサービス注文全体のステータスを反映し、**ステータス** レポートが個々のサービス注文明細行のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="3abd0-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3abd0-105">進捗状況</span><span class="sxs-lookup"><span data-stu-id="3abd0-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="3abd0-106">明細行 1 のステータス</span><span class="sxs-lookup"><span data-stu-id="3abd0-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="3abd0-107">明細行 2 のステータス</span><span class="sxs-lookup"><span data-stu-id="3abd0-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="3abd0-108">明細行 3 のステータス</span><span class="sxs-lookup"><span data-stu-id="3abd0-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3abd0-109"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-110"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-111"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-112"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3abd0-113"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-114"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-115"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-116"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3abd0-117"><strong>進行中</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-118"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-119"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-120"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3abd0-121"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-122"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-123"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-124"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3abd0-125"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-126"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-127"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-128"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3abd0-129"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-130"><strong>転記済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-131"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="3abd0-132"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="3abd0-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3abd0-133">すべての明細行のステータスが **作成済** の場合、サービス注文の進捗状況は進行中であり、一部の明細行のステータスが **キャンセル済** または **転記済** の場合も進行中です。</span><span class="sxs-lookup"><span data-stu-id="3abd0-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="3abd0-134">サービス注文のすべての明細行が **転記済** とマークされている場合、サービス注文の進捗状況は **転記済** です。</span><span class="sxs-lookup"><span data-stu-id="3abd0-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="3abd0-135">一部の明細行が **転記済** で、一部の明細行が **キャンセル済** の場合も、進捗状況は **転記済** です。</span><span class="sxs-lookup"><span data-stu-id="3abd0-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]