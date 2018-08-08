--- 
title: "帳簿の設定"
description: "この手順では、新しい固定資産帳簿を作成する方法およびそれを固定資産グループに関連付ける方法を説明します。"
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: b18f52254b9073cd95bf50539a4414598a8c19cc
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-books"></a><span data-ttu-id="a1c07-103">帳簿の設定</span><span class="sxs-lookup"><span data-stu-id="a1c07-103">Set up books</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a1c07-104">この手順では、新しい固定資産帳簿を作成する方法およびそれを固定資産グループに関連付ける方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="a1c07-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="a1c07-106">帳簿の作成</span><span class="sxs-lookup"><span data-stu-id="a1c07-106">Create a book</span></span>
1. <span data-ttu-id="a1c07-107">[固定資産] > [設定] > [帳簿] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="a1c07-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a1c07-108">Click New.</span></span>
3. <span data-ttu-id="a1c07-109">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="a1c07-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a1c07-111">減価償却の計算を選択すると、関連する資産帳簿は償却提案に含まれます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="a1c07-112">選択しない場合は、資産帳簿は自動的に償却されません。</span><span class="sxs-lookup"><span data-stu-id="a1c07-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="a1c07-113">[減価償却の計算] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="a1c07-114">[減価償却プロファイル] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="a1c07-115">代替減価償却プロファイルは、減価償却の切り替え方法としても知られています。</span><span class="sxs-lookup"><span data-stu-id="a1c07-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="a1c07-116">既定の減価償却プロファイルと同じまたはそれより高額である代替プロファイル減価償却金額を計算するとき、償却提案はこのプロファイルに切り替わります。</span><span class="sxs-lookup"><span data-stu-id="a1c07-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="a1c07-117">特別減価償却プロファイルは、特殊な状況で資産の割増償却に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="a1c07-118">たとえば、自然災害の結果の減価償却を記録する場合などに、このフィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="a1c07-119">基準調整を含む減価償却調整の作成を選択する場合、資産の値が更新される時に減価償却調整が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="a1c07-120">選択しない場合は、更新された資産価値は減価償却計算にのみ影響するようになります。</span><span class="sxs-lookup"><span data-stu-id="a1c07-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="a1c07-121">[基準調整と減価償却調整を作成する] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="a1c07-122">既定では、固定資産帳簿トランザクションは総勘定元帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="a1c07-123">[総勘定元帳への転記] フィールドを [いいえ] に設定すると、帳簿の総勘定元帳への転記を無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="a1c07-124">総勘定元帳に転記する帳簿は、税務報告のために通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="a1c07-125">これによって資産帳簿の履歴トランザクションが総勘定元帳にコミットされなかったため、さらに柔軟に削除を行えます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="a1c07-126">帳簿が総勘定元帳に転記される場合は転記階層が現在レイヤーに既定で設定され、総勘定元帳に転記されない場合はなしに設定されます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="a1c07-127">この帳簿のトランザクションを別のレイヤーに転記する必要がある場合は、転記階層を更新します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="a1c07-128">[カレンダー] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="a1c07-129">派生帳簿は、同時に別の帳簿にトランザクションを転記します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="a1c07-130">基本の帳簿でトランザクションを作成すると、転記時にトランザクションの正確なコピーが派生帳簿に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="a1c07-131">派生帳簿のトランザクションでの再計算がなければ、減価償却トランザクションに使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a1c07-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="a1c07-132">帳簿を固定資産グループに関連付ける</span><span class="sxs-lookup"><span data-stu-id="a1c07-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="a1c07-133">[固定資産グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a1c07-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="a1c07-134">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="a1c07-135">[耐用年数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1c07-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="a1c07-136">耐用年数を設定した後に減価償却期間が計算されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a1c07-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="a1c07-137">税務用の減価償却方法を必要に応じて設定できます。</span><span class="sxs-lookup"><span data-stu-id="a1c07-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


