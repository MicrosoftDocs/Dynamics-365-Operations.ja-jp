---
title: 固定資産の減価償却
description: このトピックは、固定資産の償却の概要を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1056dadab4294072cc064670f5cfcda239e22e19
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445169"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="b371b-103">固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="b371b-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b371b-104">このトピックは、固定資産の償却の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="b371b-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="b371b-105">減価償却は、一般に、貸借対照表の固定資産の価値を減少させる定期処理取引であり、損益勘定では支出として記帳します。</span><span class="sxs-lookup"><span data-stu-id="b371b-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="b371b-106">したがって、通常、主勘定を使用して貸借対照表の定期減価償却を貸方に転記します。</span><span class="sxs-lookup"><span data-stu-id="b371b-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="b371b-107">相手勘定は、勘定科目の損益部分の勘定です。</span><span class="sxs-lookup"><span data-stu-id="b371b-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="b371b-108">減価償却調整</span><span class="sxs-lookup"><span data-stu-id="b371b-108">Depreciation adjustment</span></span>
<span data-ttu-id="b371b-109">通常は、転記済みの減価償却取引に対する修正のみが減価償却調整として転記されます。</span><span class="sxs-lookup"><span data-stu-id="b371b-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="b371b-110">したがって、主勘定と相手勘定は、減価償却の勘定と同様に設定します。</span><span class="sxs-lookup"><span data-stu-id="b371b-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="b371b-111">減価償却調整額は、正にも負にもなりますが、主勘定 (貸借対照表の勘定として) と相手勘定 (通常、損益勘定として) の機能は変わりません。</span><span class="sxs-lookup"><span data-stu-id="b371b-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="b371b-112">特別減価償却</span><span class="sxs-lookup"><span data-stu-id="b371b-112">Extraordinary depreciation</span></span>
<span data-ttu-id="b371b-113">特別減価償却は基本的な減価償却として処理されます。</span><span class="sxs-lookup"><span data-stu-id="b371b-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="b371b-114">したがって、主勘定は減価償却金額を貸借対照表の貸方に転記するために使用され、固定資産の価値を減少させます。</span><span class="sxs-lookup"><span data-stu-id="b371b-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="b371b-115">相手勘定は、会計年度期間に対して計算された減価償却が経費として請求される損益勘定です。</span><span class="sxs-lookup"><span data-stu-id="b371b-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="b371b-116">特別減価償却は、基本減価償却とは関係なく処理されます。</span><span class="sxs-lookup"><span data-stu-id="b371b-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="b371b-117">特別減価償却を異なる取引タイプにすると、通常の基本減価償却とは別に特別減価償却の転記と報告ができます。</span><span class="sxs-lookup"><span data-stu-id="b371b-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="b371b-118">特別減価償却費</span><span class="sxs-lookup"><span data-stu-id="b371b-118">Special depreciation allowance</span></span>
<span data-ttu-id="b371b-119">特別割引減価償却を使用すると、資産を供用し、減価償却を開始した初年度に、追加の減価償却金額を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b371b-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="b371b-120">特別減価償却費は、他の減価償却計算の前に処理される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b371b-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="b371b-121">特別減価償却費は固定資産の耐用年数までは不明なことが多いので、総勘定元帳に転記しない帳簿では、このタイプの減価償却を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b371b-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="b371b-122">総勘定元帳の周期機能に転記されないトランザクションの [削除] を使用して、これらの帳簿のトランザクション履歴を削除できます。</span><span class="sxs-lookup"><span data-stu-id="b371b-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="b371b-123">次に固定資産に関する減価償却履歴を削除し、削除の確認後、特別減価償却費を転記できます。それからその会計年度の残りの減価償却トランザクションを転記できます。</span><span class="sxs-lookup"><span data-stu-id="b371b-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="b371b-124">特別減価償却費レコードは無数に作成できます。</span><span class="sxs-lookup"><span data-stu-id="b371b-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="b371b-125">固定資産グループ帳簿にこのレコードを割り当てた後、これらは固定資産帳簿に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b371b-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="b371b-126">特別減価償却費はパーセンテージまたは固定金額として入力されます。</span><span class="sxs-lookup"><span data-stu-id="b371b-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="b371b-127">減価償却提案を転記すると、特別減価償却費トランザクションが、減価償却トランザクションとは異なるトランザクションとして、帳簿に転記されます。</span><span class="sxs-lookup"><span data-stu-id="b371b-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="b371b-128">償却年 : カレンダー</span><span class="sxs-lookup"><span data-stu-id="b371b-128">Depreciation calendars</span></span>
<span data-ttu-id="b371b-129">各帳簿には、固定資産の減価償却時に使用されるカレンダーがあります。</span><span class="sxs-lookup"><span data-stu-id="b371b-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="b371b-130">帳簿上でカレンダーを指定していない場合、帳簿では既定で元帳の会計カレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b371b-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="b371b-131">帳簿に関連付けられた減価償却プロファイルによって減価償却会計年度が使用される場合、帳簿の会計カレンダーを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b371b-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="b371b-132">総勘定元帳の **会計カレンダー** ページを使用して、共用カレンダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="b371b-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="b371b-133">詳細については、[減価償却方法](depreciation-methods-conventions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b371b-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



