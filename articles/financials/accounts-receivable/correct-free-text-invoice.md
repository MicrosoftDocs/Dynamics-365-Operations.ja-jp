---
title: "自由書式の請求書を訂正"
description: "この記事では、自由書式の請求書を転記後に修正し、修正済請求書として再発行する方法を説明します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cbae4c444db29a8dc7f3040aa78e45c0da092efd
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="2a330-103">自由書式の請求書を訂正</span><span class="sxs-lookup"><span data-stu-id="2a330-103">Correct a free text invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2a330-104">この記事では、自由書式の請求書を転記後に修正し、修正済請求書として再発行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2a330-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="2a330-105">転記済みの自由書式の請求書を修正するには、転記された自由書式の請求書を開きます。</span><span class="sxs-lookup"><span data-stu-id="2a330-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="2a330-106">**請求書**ページで、[**キャンセル**] を選択してから、[**請求書の修正**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a330-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="2a330-107">理由コードを選択し、コメントを追加して、および新しい訂正請求書の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a330-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="2a330-108">訂正請求書を変更して、転記できます。</span><span class="sxs-lookup"><span data-stu-id="2a330-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="2a330-109">訂正請求書を転記すると、キャンセル請求書が元の請求金額と一致する貸方金額に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="2a330-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="2a330-110">したがって、元の請求書とキャンセル請求書の合計残高が 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="2a330-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="2a330-111">キャンセル請求書が元の請求書に対して決済されます。</span><span class="sxs-lookup"><span data-stu-id="2a330-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="2a330-112">訂正請求書を転記すると、3 つの請求書ができます。</span><span class="sxs-lookup"><span data-stu-id="2a330-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="2a330-113">**元の請求書** – 修正している情報を含む請求書。</span><span class="sxs-lookup"><span data-stu-id="2a330-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="2a330-114">**キャンセル請求書** – システム生成の貸方請求書。最後に修正された請求書をキャンセルするために作成されます。</span><span class="sxs-lookup"><span data-stu-id="2a330-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="2a330-115">**訂正請求書** – 修正された請求書情報を含む請求書。</span><span class="sxs-lookup"><span data-stu-id="2a330-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="2a330-116">2 つの方法でキャンセル請求書と訂正請求書を識別できます。</span><span class="sxs-lookup"><span data-stu-id="2a330-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="2a330-117">**すべての自由書式の請求書**ページには、[**訂正**] 列が含まれており、ここでキャンセル請求書か訂正請求書かを確認できます。</span><span class="sxs-lookup"><span data-stu-id="2a330-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="2a330-118">自由書式の請求書ヘッダーには、**キャンセル請求書 '\[請求書番号\]'** または **訂正請求書 '\[請求書番号\]'** のステータスが示されます。</span><span class="sxs-lookup"><span data-stu-id="2a330-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="2a330-119">この機能は、[**自由書式の請求訂正**] コンフィギュレーション キーが選択されている場合にのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="2a330-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>




