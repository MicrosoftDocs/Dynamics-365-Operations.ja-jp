---
title: "派生帳簿を転記する"
description: "この記事は、派生帳簿を使用する方法について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: aaacf596f2ea1107a53647d779e9d2b6c37ab530
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---

# <a name="post-with-derived-books"></a><span data-ttu-id="15393-103">派生帳簿を転記する</span><span class="sxs-lookup"><span data-stu-id="15393-103">Post with derived books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="15393-104">この記事は、派生帳簿を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="15393-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="15393-105">派生帳簿を含む帳簿のトランザクションを転記すると、派生帳簿トランザクションは仕訳帳、発注書、または自由書式の請求書に自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="15393-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="15393-106">ただし、[固定資産] 仕訳で基本帳簿トランザクションを作成した場合は、派生トランザクションを転記する前にその金額を表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="15393-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="15393-107">売上税勘定、顧客勘定、仕入先勘定など一部の勘定は、基本帳簿の転記によって一度だけ更新されます。</span><span class="sxs-lookup"><span data-stu-id="15393-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="15393-108">派生帳簿トランザクションは、[固定資産転記プロファイル] ページの派生帳簿で定義されている勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="15393-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="15393-109">[取得] は、派生帳簿のトランザクション タイプとして頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="15393-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="15393-110">帳簿および派生帳簿を固定資産の取得時から固定資産に適用する必要がある場合は、このタイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="15393-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="15393-111">トランザクション タイプの他の値も適用できます。</span><span class="sxs-lookup"><span data-stu-id="15393-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="15393-112">たとえば、帳簿および派生帳簿の売却および処分の間隔が同一である場合は、すべての固定資産トランザクション タイプを派生帳簿の設定に使用できます。</span><span class="sxs-lookup"><span data-stu-id="15393-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="15393-113">派生帳簿に転記する減価償却額は、基本帳簿に転記した金額と同じになります。</span><span class="sxs-lookup"><span data-stu-id="15393-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="15393-114">これらの帳簿間で減価償却方法が異なる場合は、派生プロセスを使用して減価償却トランザクションを生成しないでください。</span><span class="sxs-lookup"><span data-stu-id="15393-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="15393-115">例</span><span class="sxs-lookup"><span data-stu-id="15393-115">Example</span></span> 
<span data-ttu-id="15393-116">ここでは、派生帳簿機能を使用して取得トランザクションを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="15393-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="15393-117">[帳簿] ページの帳簿を作成します。</span><span class="sxs-lookup"><span data-stu-id="15393-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="15393-118">会計用の帳簿: VM 1、現在の転記階層</span><span class="sxs-lookup"><span data-stu-id="15393-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="15393-119">税務用の帳簿: VM 2、税の転記階層</span><span class="sxs-lookup"><span data-stu-id="15393-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="15393-120">VM 1 で、[派生帳簿] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15393-120">On VM 1, click the Derived books tab.</span></span> <span data-ttu-id="15393-121">[帳簿] フィールドで VM 2 を選択し、[トランザクション タイプ] フィールドで [取得] を選択します。</span><span class="sxs-lookup"><span data-stu-id="15393-121">Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="15393-122">これにより、特定の固定資産に帳簿を関連付けることができるようになります。</span><span class="sxs-lookup"><span data-stu-id="15393-122">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="15393-123">帳簿 VM1 を使用して固定資産の取得を転記すると、VM 1 だけでなく派生帳簿 VM 2 にもその取得が転記されます。</span><span class="sxs-lookup"><span data-stu-id="15393-123">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="15393-124">両方の固定資産帳簿のステータスが [未処理] に更新されます。</span><span class="sxs-lookup"><span data-stu-id="15393-124">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="15393-125">派生帳簿を使用しない場合は、帳簿 VM 1 および帳簿 VM 2 の両方に対して固定資産の取得を転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15393-125">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="15393-126">詳細については、「[派生帳簿](derived-books.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="15393-126">For more information, see [Derived books](derived-books.md)</span></span>




