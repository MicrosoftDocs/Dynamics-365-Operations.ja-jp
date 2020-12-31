---
title: 転記階層への固定資産トランザクションを転記する
description: この記事は、固定資産トランザクションの転記階層機能の概要を示します。
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a80e4d1a081b5bd8c58238b0f154f8fbdc660ccb
ms.sourcegitcommit: f80819c67c0a7475315fc68ce1cb568831e2c0e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2020
ms.locfileid: "4493675"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="bce47-103">転記階層への固定資産トランザクションを転記する</span><span class="sxs-lookup"><span data-stu-id="bce47-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bce47-104">この記事は、固定資産トランザクションの転記階層機能の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="bce47-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="bce47-105">固定資産の減価償却は多くの場合、目的に応じて異なる方法で行われます。</span><span class="sxs-lookup"><span data-stu-id="bce47-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="bce47-106">税申告用の減価償却は、税引前の減価償却が可能な限り最大になるように現在の税制を使用して計算されますが、報告のための減価償却は、会計法および標準に従って計算されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="bce47-107">さまざまな種類の減価償却が計算されて、それぞれ異なる転記階層に記録されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="bce47-108">固定資産に関連付けられる各帳簿は、全体的な減価償却の目的を持つ特定の転記階層に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="bce47-109">次の 10 の転記階層があります。現在、操作、税金、および 7 つのカスタム階層。</span><span class="sxs-lookup"><span data-stu-id="bce47-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="bce47-110">[総勘定元帳への転記] フィールドを [いいえ] に設定すると、帳簿の総勘定元帳への転記を無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="bce47-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="bce47-111">[転記階層] フィールドが [なし] に自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="bce47-112">通常、総勘定元帳に転記しない帳簿は、税務報告のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="bce47-113">この方法によって資産帳簿の履歴トランザクションが総勘定元帳にコミットされなかったため、さらに柔軟に削除を行えます。</span><span class="sxs-lookup"><span data-stu-id="bce47-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="bce47-114">固定資産仕訳帳は、[総勘定元帳]、[仕訳帳の設定]、[仕訳帳名] の順に表示して、[仕訳帳名] ページを使用して定義できます。</span><span class="sxs-lookup"><span data-stu-id="bce47-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="bce47-115">減価償却を転記できる各仕訳帳は、単独の転記階層に対して仕訳帳名で定義されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="bce47-116">仕訳帳の転記階層は変更できません。</span><span class="sxs-lookup"><span data-stu-id="bce47-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="bce47-117">この制限は、各転記階層のトランザクションが分離しておくのを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bce47-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="bce47-118">個々の転記階層には、仕訳帳名を少なくとも 1 つ作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bce47-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="bce47-119">総勘定元帳に転記しない帳簿を使用している場合は、転記階層が [なし] に設定されている仕訳帳を作成する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="bce47-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="bce47-120">[固定資産転記プロファイル] ページで、固定資産トランザクションのための勘定科目を指定できます。</span><span class="sxs-lookup"><span data-stu-id="bce47-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="bce47-121">各転記プロファイルに対して、関連するトランザクション タイプと帳簿を選択してから、勘定科目を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bce47-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="bce47-122">総勘定元帳に転記する各帳簿の転記プロファイルのレコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="bce47-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="bce47-123">固定資産は、**現在** の転記レイヤー (**発注書**、**保留中の仕入先請求書**、**販売注文**、**自由書式の請求書** など) のみをサポートするドキュメントに入力できます。</span><span class="sxs-lookup"><span data-stu-id="bce47-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="bce47-124">いずれかのドキュメントで固定資産 ID を選択すると、資産帳簿は **最新** の転記階層の帳簿に対してフィルター処理され、固定資産転記階層が **最新** であることがシステムによって検証されたときに転記時に自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="bce47-125">検証を完了できない場合、転記プロセスは停止されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bce47-126">派生帳簿を使用することによって、複数の転記階層にトランザクションを同時に転記することができます。</span><span class="sxs-lookup"><span data-stu-id="bce47-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="bce47-127">帳簿の転記レイヤーに対応する転記レイヤーの仕訳帳または元伝票で、基本帳簿のトランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="bce47-128">転記の際には、派生帳簿のトランザクションが、適切な転記レイヤーに転記されます。</span><span class="sxs-lookup"><span data-stu-id="bce47-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="bce47-129">詳細については、[派生帳簿](derived-books.md) および[派生帳簿による転記](post-derived-value-models.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bce47-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



