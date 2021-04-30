---
title: 負債、資産、および経費トランザクションの表示
description: このトピックでは、リース資産のトランザクションを表示する方法について説明します。 これらのトランザクションには、リース負債トランザクションと、転記された履行費用トランザクションが含まれます。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 55b8019db6abdb3bd5ecdb6eadc4f7443f2bf071
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881641"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="0a863-104">負債、資産、および経費トランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="0a863-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a863-105">このトピックでは、リース資産のトランザクションを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a863-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="0a863-106">これらのトランザクションには、リース負債トランザクションと、転記された履行費用トランザクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0a863-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="0a863-107">負債および使用権資産のキャリー額は、いくつかのレポートで使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="0a863-108">また、調整値を計算するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="0a863-109">負債トランザクション</span><span class="sxs-lookup"><span data-stu-id="0a863-109">Liability transactions</span></span>

<span data-ttu-id="0a863-110">リース負債トランザクションを表示するには、**リースの概要** ページでリースを選択し、**帳簿** を選択して、リース レコードに関連付けられているブックを開きます。</span><span class="sxs-lookup"><span data-stu-id="0a863-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="0a863-111">最初の認識、請求書、または利子仕訳帳が転記された後、**負債トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a863-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="0a863-112">**負債トランザクション** ページには、リース負債を増減させるトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="0a863-113">このページの負の金額は、標準アプリケーションの貸方トランザクションを表します。</span><span class="sxs-lookup"><span data-stu-id="0a863-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="0a863-114">未収利息は負の値として表示され、リース負債の合計額が増加します。</span><span class="sxs-lookup"><span data-stu-id="0a863-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="0a863-115">リース調整は、リース帳簿の性質と影響に応じて、正または負の値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="0a863-116">選択したリースのリース負債の現在の正味残高がページの左下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="0a863-117">資産トランザクション</span><span class="sxs-lookup"><span data-stu-id="0a863-117">Asset transactions</span></span>

<span data-ttu-id="0a863-118">リース資産トランザクションを表示するには、**リースの概要** ページでリースを選択し、**帳簿** を選択して、リース レコードに関連付けられているリース帳簿を開きます。</span><span class="sxs-lookup"><span data-stu-id="0a863-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="0a863-119">**資産トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a863-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="0a863-120">**資産トランザクション** ページには、リース資産と累計減価償却勘定の増加または減少のトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="0a863-121">借方は正の値として表示され、**負債トランザクション** ページのように貸方が負の値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="0a863-122">転記された初期認識と、減価償却累計額の次の金額が、ページの左下に資産残高として表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="0a863-123">経費トランザクション</span><span class="sxs-lookup"><span data-stu-id="0a863-123">Expenses transactions</span></span>

<span data-ttu-id="0a863-124">リース経費トランザクションを表示するには、**リースの概要** ページでリースを選択し、**帳簿** を選択して、リース レコードに関連付けられているリース帳簿を開きます。</span><span class="sxs-lookup"><span data-stu-id="0a863-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="0a863-125">次に、**経費トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a863-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="0a863-126">**経費トランザクション** ページには、リースに対して転記されたすべての経費 (支払利息、減価償却費、履行費用など) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a863-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
