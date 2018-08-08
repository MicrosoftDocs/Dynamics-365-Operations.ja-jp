---
title: "派生帳簿"
description: "この記事は、派生帳簿機能の概要を示します。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 153b6437205d5a849fa6a90c0d3b9f3d51dd6768
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="derived-books"></a><span data-ttu-id="0b320-103">派生帳簿</span><span class="sxs-lookup"><span data-stu-id="0b320-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b320-104">この記事は、派生帳簿機能の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="0b320-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="0b320-105">派生帳簿の目的は、定期的に計画されている固定資産帳簿トランザクションの転記を簡素化することです。</span><span class="sxs-lookup"><span data-stu-id="0b320-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="0b320-106">1 つの帳簿を基本帳簿として選択します。</span><span class="sxs-lookup"><span data-stu-id="0b320-106">You choose one book as the primary book.</span></span> <span data-ttu-id="0b320-107">通常、これは会計上の減価償却に使用される帳簿です。</span><span class="sxs-lookup"><span data-stu-id="0b320-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="0b320-108">この価値モデルに、同じ期間にトランザクションを転記するように設定された他の帳簿を基本帳簿として関連付けます。</span><span class="sxs-lookup"><span data-stu-id="0b320-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="0b320-109">派生帳簿としてよく設定されるのが減価償却簿です。</span><span class="sxs-lookup"><span data-stu-id="0b320-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="0b320-110">派生帳簿に転記するように設定するトランザクションとして最も一般的なものは、取得、取得原価調整、および処分です。</span><span class="sxs-lookup"><span data-stu-id="0b320-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="0b320-111">例</span><span class="sxs-lookup"><span data-stu-id="0b320-111">Example</span></span>

<span data-ttu-id="0b320-112">帳簿 B および C は、取得トランザクション タイプの帳簿 A に対して、派生帳簿として設定されます。</span><span class="sxs-lookup"><span data-stu-id="0b320-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="0b320-113">帳簿 A で、価額 1,500.00 の資産 123 に対して取得トランザクションを入力します。</span><span class="sxs-lookup"><span data-stu-id="0b320-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="0b320-114">トランザクションの転記時に、取得トランザクションが生成され、帳簿 B の資産 123 および帳簿 C の資産 123 に 1,500.00 として転記されます。</span><span class="sxs-lookup"><span data-stu-id="0b320-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="0b320-115">基本帳簿のトランザクションを固定資産仕訳帳で転記対象として作成した場合は、派生減価償却帳簿のトランザクションも表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="0b320-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="0b320-116">基本帳簿のトランザクションを別の仕訳帳で作成した場合は、派生価値モデルのトランザクションは表示されません。</span><span class="sxs-lookup"><span data-stu-id="0b320-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="0b320-117">ただし、基本帳簿のトランザクションを転記するときに適切な勘定および転記階層に転記されます。</span><span class="sxs-lookup"><span data-stu-id="0b320-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="0b320-118">基本帳簿とは異なる間隔でトランザクションを転記するように設定された帳簿は、派生帳簿ではなく別の帳簿として、固定資産に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b320-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="0b320-119">詳細については、「[派生帳簿による転記](post-derived-value-models.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b320-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




