---
title: 定期的な自由書式の請求書の生成と転記
description: 定期請求書は、顧客に対して同じ金額を定期的に請求する際に使用します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysLookupMultiSelectGrid, CustRecurrenceInvoiceGroup, CustFreeInvoice, CustRecurrenceInvoiceTotals
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 294e7ac5b1d548982ad402214934afe0cfce475d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188789"
---
# <a name="generate-and-post-recurring-free-text-invoices"></a><span data-ttu-id="98930-103">定期的な自由書式の請求書の生成と転記</span><span class="sxs-lookup"><span data-stu-id="98930-103">Generate and post recurring free text invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98930-104">定期請求書は、顧客に対して同じ金額を定期的に請求する際に使用します。</span><span class="sxs-lookup"><span data-stu-id="98930-104">Recurring invoices are used to invoice customers regularly for the same amount.</span></span> <span data-ttu-id="98930-105">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="98930-105">This recording uses the USMF demo company.</span></span> <span data-ttu-id="98930-106">記録は A/R 請求書の管理および処理を行う担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="98930-106">The recording is intended for the person responsible for managing and processing A/R invoices.</span></span>


## <a name="generate-recurring-invoices"></a><span data-ttu-id="98930-107">定期請求書の生成</span><span class="sxs-lookup"><span data-stu-id="98930-107">Generate recurring invoices</span></span>

## <a name="post-recurring-invoices"></a><span data-ttu-id="98930-108">定期請求書の転記</span><span class="sxs-lookup"><span data-stu-id="98930-108">Post recurring invoices</span></span>
1. <span data-ttu-id="98930-109">[売掛金勘定] > [請求書] > [定期請求書] > [定期請求書の転記] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="98930-109">Go to Accounts receivable > Invoices > Recurring invoices > Post recurring invoices.</span></span>
    * <span data-ttu-id="98930-110">既に生成されている定期請求書に表示および印刷されるこのページを使用します。</span><span class="sxs-lookup"><span data-stu-id="98930-110">Use this page to view and print recurring invoices that have already been generated.</span></span>  
2. <span data-ttu-id="98930-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98930-111">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98930-112">定期請求書グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="98930-112">Select the recurring invoice group.</span></span>  
3. <span data-ttu-id="98930-113">[合計] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98930-113">Click Totals.</span></span>
    * <span data-ttu-id="98930-114">定期請求書グループの合計を確認します。</span><span class="sxs-lookup"><span data-stu-id="98930-114">Verify totals for the recurring invoice group.</span></span>  
4. <span data-ttu-id="98930-115">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98930-115">Click Close.</span></span>
    * <span data-ttu-id="98930-116">各行の下には、定期的な自由書式の請求書が記載されます。</span><span class="sxs-lookup"><span data-stu-id="98930-116">Each line below is a recurring free text invoice.</span></span> <span data-ttu-id="98930-117">行を選択し、[詳細] ボタンをクリックし、自由書式の請求書の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="98930-117">You can select a line and click 'Details' button to view free text invoice details.</span></span>  
5. <span data-ttu-id="98930-118">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98930-118">Click Validate.</span></span>
    * <span data-ttu-id="98930-119">選択した請求書にエラーがないことを確認してください。しかし、請求書は転記しません。</span><span class="sxs-lookup"><span data-stu-id="98930-119">Verify that the selected invoices do not have errors, but do not post the invoices.</span></span>  
6. <span data-ttu-id="98930-120">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98930-120">Click Post.</span></span>
    * <span data-ttu-id="98930-121">選択した請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="98930-121">Post the selected invoices.</span></span>  

