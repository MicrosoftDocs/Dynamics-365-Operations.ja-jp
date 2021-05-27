---
title: 税計算のパフォーマンスがトランザクションに与える影響
description: このトピックでは、税計算のパフォーマンスおよびトランザクションに対する影響に関するトラブルシューティングの情報を提供します。
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020142"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="6eae1-103">税計算のパフォーマンスがトランザクションに与える影響</span><span class="sxs-lookup"><span data-stu-id="6eae1-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6eae1-104">トランザクションは、税計算で発生するパフォーマンスの問題によって影響を受ける場合があります。</span><span class="sxs-lookup"><span data-stu-id="6eae1-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="6eae1-105">この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6eae1-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="6eae1-106">トランザクション明細行の数の確認</span><span class="sxs-lookup"><span data-stu-id="6eae1-106">Review the transaction line count</span></span>

<span data-ttu-id="6eae1-107">トランザクション明細行の数が多くないか (数百行以上など) を確認します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="6eae1-108">多くない場合には、次のセクションに進みます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="6eae1-109">トランザクションに数百行の明細行がある場合は、税計算を遅延させます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="6eae1-110">詳細については、[仕訳帳の税金計算遅延の有効化](enable-delayed-tax-calculation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6eae1-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="6eae1-111">次に、次の条件が満たされているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="6eae1-112">大きなファイルからのインポート トランザクションが存在します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="6eae1-113">複数のセッションで、同じ取引税計算を同時に処理します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="6eae1-114">トランザクションには複数の明細行が作成され、ビューはリアルタイムで更新されます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="6eae1-115">たとえば、**一般仕訳帳** ページの **計算上の消費税金額** フィールドは、明細行のフィールドが変更された場合にリアルタイムで更新されます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="6eae1-116">[![仕訳伝票ページの計算上の消費税金額フィールド](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="6eae1-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="6eae1-117">これらの条件が満たされている場合は、税計算を遅延させます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="6eae1-118">コール スタックの確認</span><span class="sxs-lookup"><span data-stu-id="6eae1-118">Review the call stack</span></span>

<span data-ttu-id="6eae1-119">コール スタックを確認して、税計算が複数回呼び出されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="6eae1-120">呼び出されない場合には、次のセクションに進みます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="6eae1-121">コール スタックが複数回呼び出される場合は、次の手順に従って税計算時間を短縮します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="6eae1-122">仕訳帳でトランザクションが考慮される場合は、税計算を遅延させます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="6eae1-123">詳細については、[仕訳帳の税金計算遅延の有効化](enable-delayed-tax-calculation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6eae1-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="6eae1-124">トランザクションが発注書で、アプリケーション バージョンが 10.0.15 以降の場合、**PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** のフライティングを有効にして、税計算を最終計算まで遅延できます。</span><span class="sxs-lookup"><span data-stu-id="6eae1-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="6eae1-125">コール スタック タイムラインの確認</span><span class="sxs-lookup"><span data-stu-id="6eae1-125">Review the call stack timeline</span></span>

<span data-ttu-id="6eae1-126">コール スタック タイムラインを確認して、次の問題が存在するかどうかを識別します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="6eae1-127">問題が発生している場合、**TaxUncommittedDoIsolateScopeFlighting** のフライティングを有効にして、問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="6eae1-128">トランザクションにより、システムはセッションが終了するまで応答を停止します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="6eae1-129">そのため、トランザクションで税の結果を計算できません。</span><span class="sxs-lookup"><span data-stu-id="6eae1-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="6eae1-130">次の図は、表示される「セッション終了」メッセージ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="6eae1-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="6eae1-131">[![セッション終了メッセージ](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="6eae1-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="6eae1-132">**TaxUncommitted** メソッドは、他のメソッドより時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="6eae1-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="6eae1-133">たとえば、次の図では、**TaxUncommitted::updateTaxUncommitted()** メソッドの所要時間は 43,347.42 秒ですが、他のメソッドの所要時間は 0.09 秒です。</span><span class="sxs-lookup"><span data-stu-id="6eae1-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="6eae1-134">[![メソッドの期間](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="6eae1-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="6eae1-135">税計算のカスタマイズと呼び出し</span><span class="sxs-lookup"><span data-stu-id="6eae1-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="6eae1-136">カスタマイズする場合は、各行の **insert()** または **update()** メソッドで税計算を呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="6eae1-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="6eae1-137">税計算をトランザクション レベルで呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6eae1-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="6eae1-138">カスタマイズが存在するかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="6eae1-138">Determine whether customization exists</span></span>

<span data-ttu-id="6eae1-139">前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="6eae1-140">カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="6eae1-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
