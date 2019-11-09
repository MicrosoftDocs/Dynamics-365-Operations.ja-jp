---
title: 先日付小切手
description: この記事は、Microsoft Dynamics 365 Finance の先日付小切手のサポートについて説明します。 先日付小切手とは、将来の日付で支払を履行または受け取るために発行される小切手です。 したがって、小切手は、特定の日付まで清算できません。
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38ee6c5b3d258c313a2066b388a83330bf696d39
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178682"
---
# <a name="postdated-checks"></a><span data-ttu-id="d09c2-105">先日付小切手</span><span class="sxs-lookup"><span data-stu-id="d09c2-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d09c2-106">この記事は、先日付小切手のサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d09c2-106">This article provides information about support for postdated checks.</span></span> <span data-ttu-id="d09c2-107">先日付小切手とは、将来の日付で支払を履行または受け取るために発行される小切手です。</span><span class="sxs-lookup"><span data-stu-id="d09c2-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="d09c2-108">したがって、小切手は、特定の日付まで清算できません。</span><span class="sxs-lookup"><span data-stu-id="d09c2-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="d09c2-109">Dynamics 365 Finance は、次の表に示すように、売掛金勘定と買掛金勘定の両方の先日付小切手の完全な管理サイクルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d09c2-109">Dynamics 365 Finance supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d09c2-110">シナリオ</span><span class="sxs-lookup"><span data-stu-id="d09c2-110">Scenario</span></span></th>
<th><span data-ttu-id="d09c2-111">細目</span><span class="sxs-lookup"><span data-stu-id="d09c2-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d09c2-112">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="d09c2-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="d09c2-113">新しい支払方法を設定し、発行された小切手、受領済みの小切手および源泉徴収税の精算勘定の支払業務を指定します。</span><span class="sxs-lookup"><span data-stu-id="d09c2-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d09c2-114">仕入先からの先日付小切手を登録および転記</span><span class="sxs-lookup"><span data-stu-id="d09c2-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d09c2-115">仕入先に発行した先日付小切手の詳細を登録します。</span><span class="sxs-lookup"><span data-stu-id="d09c2-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="d09c2-116">支払を転記すると、仕入先負債が認識されますが、銀行口座は、貸方とは見なされません。</span><span class="sxs-lookup"><span data-stu-id="d09c2-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="d09c2-117">代わりに、精算勘定がこの目的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d09c2-118">顧客の先日付小切手の登録と転記</span><span class="sxs-lookup"><span data-stu-id="d09c2-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="d09c2-119">顧客から受け取った先日付小切手の詳細を登録します。</span><span class="sxs-lookup"><span data-stu-id="d09c2-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="d09c2-120">支払を転記すると、顧客売掛金が貸方と見なされますが、銀行口座は、借方とは見なされません。</span><span class="sxs-lookup"><span data-stu-id="d09c2-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="d09c2-121">代わりに、精算勘定がこの目的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d09c2-122">顧客または仕入先からの交換先日付小切手を登録および転記します。</span><span class="sxs-lookup"><span data-stu-id="d09c2-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="d09c2-123">仕入先への、または顧客からの元の小切手が紛失または破損した場合、代替先日付小切手を発行することもできます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="d09c2-124">小切手の詳細を登録するときに、元の小切手への参照を提示し、新しい小切手が元の小切手の代替であることを示します。</span><span class="sxs-lookup"><span data-stu-id="d09c2-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="d09c2-125">代替小切手の転記もできます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d09c2-126">顧客の先日付小切手を仕入先に転送</span><span class="sxs-lookup"><span data-stu-id="d09c2-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="d09c2-127">顧客から先日付小切手を受け取ったら、支払として仕入先にその小切手を転送できます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d09c2-128">顧客または仕入先の先日付小切手を決済</span><span class="sxs-lookup"><span data-stu-id="d09c2-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="d09c2-129">小切手が最終的に満期になったとき、顧客または仕入先のつなぎ勘定に転記された先日付小切手を決済します。</span><span class="sxs-lookup"><span data-stu-id="d09c2-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="d09c2-130">小切手を決済すると、銀行が先に使用した精算勘定に対して最終的に借方または貸方となります。</span><span class="sxs-lookup"><span data-stu-id="d09c2-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d09c2-131">仕入先の先日付小切手をキャンセル</span><span class="sxs-lookup"><span data-stu-id="d09c2-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d09c2-132">これらの状況では、転記済みの先日付小切手を取り消すことができます : - 小切手は銀行から返されます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="d09c2-133">- 小切手は誤った請求書に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="d09c2-134">- 小切手に対して現金が支払われます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="d09c2-135">先日付小切手の支払を停止する</span><span class="sxs-lookup"><span data-stu-id="d09c2-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="d09c2-136">仕入先に発行した先日付小切手に対する支払は、資金不足、仕入先との契約条件の変更、仕入先による欠陥品目の供給、または仕入先への品目の返品などの理由で停止することができます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="d09c2-137">支払の停止は、クリアされていない小切手に対してのみ行えます。</span><span class="sxs-lookup"><span data-stu-id="d09c2-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="d09c2-138">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d09c2-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="d09c2-139">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="d09c2-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="d09c2-140">顧客の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="d09c2-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="d09c2-141">顧客からの先日付小切手の決済</span><span class="sxs-lookup"><span data-stu-id="d09c2-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="d09c2-142">仕入先の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="d09c2-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="d09c2-143">仕入先の先日付小切手の決済</span><span class="sxs-lookup"><span data-stu-id="d09c2-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)


