---
title: 仕入先請求仕訳帳および請求書承認仕訳帳の既定の相手勘定
description: このトピックは、請求仕訳の既定の勘定を割り当てる場所を決定するのに役立ちます。
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6ff4e209f1d1c41d7c05cad735aacc320bdeb83
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189686"
---
# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="ebde3-103">仕入先請求仕訳帳および請求書承認仕訳帳の既定の相手勘定</span><span class="sxs-lookup"><span data-stu-id="ebde3-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebde3-104">既定の相手勘定は、次の仕入先請求仕訳帳のページで使用されます:</span><span class="sxs-lookup"><span data-stu-id="ebde3-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="ebde3-105">請求仕訳帳</span><span class="sxs-lookup"><span data-stu-id="ebde3-105">Invoice journal</span></span>
-   <span data-ttu-id="ebde3-106">請求書承認仕訳帳</span><span class="sxs-lookup"><span data-stu-id="ebde3-106">Invoice approval journal</span></span>

<span data-ttu-id="ebde3-107">次の表を使用して、請求仕訳の既定の勘定を割り当てる場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebde3-108">既定の勘定を設定する</span><span class="sxs-lookup"><span data-stu-id="ebde3-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="ebde3-109">既定の勘定が提供される場所</span><span class="sxs-lookup"><span data-stu-id="ebde3-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="ebde3-110">このオプションが処理に与える影響</span><span class="sxs-lookup"><span data-stu-id="ebde3-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="ebde3-111">このオプションを使用する状況</span><span class="sxs-lookup"><span data-stu-id="ebde3-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ebde3-112"><strong>仕入先グループ</strong> – <strong>仕入先グループ</strong>ページから開くことができる<strong>既定の勘定の設定</strong>ページで、仕入先グループの既定の相手勘定を設定します 。</span><span class="sxs-lookup"><span data-stu-id="ebde3-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="ebde3-113">仕入先</span><span class="sxs-lookup"><span data-stu-id="ebde3-113">Vendor account</span></span></li>
<li><span data-ttu-id="ebde3-114">既定の勘定が仕入先勘定に対して指定されていない場合の仕入先グループ内の仕入先勘定の仕訳エントリ</span><span class="sxs-lookup"><span data-stu-id="ebde3-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="ebde3-115">仕入先グループの既定の相手勘定は、<strong>既定の勘定の設定</strong>ページに仕入先の既定の相手勘定として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ebde3-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="ebde3-116"><strong>すべての仕入先</strong>リスト ページから、このページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="ebde3-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="ebde3-117">同じ仕入先グループから繰り返し同種の物品に対して支払を行っている場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebde3-118"><strong>仕入先</strong> – <strong>仕入先</strong>ページから開くことができる<strong>既定の勘定の設定</strong>ページで、仕入先の既定の勘定を設定します 。</span><span class="sxs-lookup"><span data-stu-id="ebde3-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="ebde3-119">仕入先勘定の仕訳入力</span><span class="sxs-lookup"><span data-stu-id="ebde3-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="ebde3-120">仕入先勘定の既定の相手勘定は、仕入先勘定の仕訳入力の既定の相手勘定として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ebde3-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="ebde3-121">同じ仕入先から繰り返し同種の物品に対して支払を行っている場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebde3-122"><strong>仕訳帳名</strong> – は、<strong>仕訳帳名</strong>ページの仕訳帳の既定の相手勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="ebde3-123"><strong>固定相手勘定</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="ebde3-124">仕訳帳名の仕訳帳タイプが<strong>仕入帳</strong>または<strong>承認</strong>の場合は、仕訳帳名で既定の相手勘定を指定することができないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ebde3-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="ebde3-125">仕訳帳名を使用する仕訳帳のヘッダー</span><span class="sxs-lookup"><span data-stu-id="ebde3-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="ebde3-126">仕訳帳名を使用する仕訳帳の仕訳入力</span><span class="sxs-lookup"><span data-stu-id="ebde3-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="ebde3-127"><strong>仕訳帳名</strong>ページの<strong>固定相手勘定</strong>オプションがオンの場合、仕訳帳名の相手勘定は、仕入先または仕入先グループの既定の相手勘定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="ebde3-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="ebde3-128">このオプションを使用すると、特定の勘定に請求する特定の原価および経費の仕訳帳を、仕入先や仕入先グループの所属先に関わらず、設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ebde3-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebde3-129"><strong>仕訳帳名</strong> – は、<strong>仕訳帳名</strong>ページの仕訳帳の既定の相手勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="ebde3-130"><strong>固定相手勘定</strong>オプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="ebde3-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="ebde3-131">仕訳帳名の仕訳帳タイプが<strong>仕入帳</strong>または<strong>承認</strong>の場合は、仕訳帳名で既定の相手勘定を指定することができないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ebde3-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="ebde3-132">仕訳帳ヘッダー</span><span class="sxs-lookup"><span data-stu-id="ebde3-132">Journal header</span></span></li>
<li><span data-ttu-id="ebde3-133">仕訳帳名を使用する仕訳帳の仕訳入力</span><span class="sxs-lookup"><span data-stu-id="ebde3-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="ebde3-134">これらの既定のエントリは、仕訳帳ヘッダーのページで使用され、仕訳帳ヘッダー ページの相手勘定は仕訳帳伝票ページで既定のエントリとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="ebde3-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="ebde3-135"><strong>仕訳帳名</strong>ページの既定の勘定は、既定の勘定が仕入先勘定に設定されていない場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="ebde3-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="ebde3-136">このオプションを使用して、既定の仕入先相手勘定が割り当てられていないときに使用する既定の勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebde3-137"><strong>仕訳帳ヘッダー</strong> – 仕訳帳の既定の相手勘定を設定して、仕訳伝票ページの既定のエントリとして使用します。</span><span class="sxs-lookup"><span data-stu-id="ebde3-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="ebde3-138">仕訳帳名の仕訳帳タイプが<strong>仕入帳</strong>または<strong>承認</strong>の場合は、仕訳帳ヘッダーで既定の相手勘定を指定することができないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ebde3-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="ebde3-139">仕訳帳の仕訳入力</span><span class="sxs-lookup"><span data-stu-id="ebde3-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="ebde3-140">仕訳帳の既定の相手勘定は、仕訳伝票ページの既定のエントリとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="ebde3-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="ebde3-141">仕訳帳のほとんどのエントリに同じ相手勘定が存在する場合は、このオプションを使用するとデータ入力が速くなります。</span><span class="sxs-lookup"><span data-stu-id="ebde3-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>





