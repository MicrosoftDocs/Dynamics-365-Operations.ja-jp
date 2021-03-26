---
title: 収益認識の再配賦 - シナリオ 1
description: このトピックでは、2 つの販売注文が入力されたが、まだ確認済の状態である、再配賦シナリオについて説明します。 3 つ以上の販売注文が確認済の状態にある場合も、同じシナリオで、同様の結果となります。
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25fb32ce72555e573cd37a0ab092b51b99bb4372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260880"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a><span data-ttu-id="d2794-104">収益認識の再配賦 – シナリオ 1</span><span class="sxs-lookup"><span data-stu-id="d2794-104">Revenue recognition reallocation – Scenario 1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2794-105">このトピックでは、2 つの販売注文が入力されたが、まだ確認済の状態である、再配賦シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2794-105">This topic goes through a reallocation scenario where two sales orders are entered, but they are only confirmed.</span></span> <span data-ttu-id="d2794-106">3 つ以上の販売注文が確認済の状態にある場合も、同じシナリオで、同様の結果となります。</span><span class="sxs-lookup"><span data-stu-id="d2794-106">The same scenario will produce similar results if more than two sales orders are in a confirmed state.</span></span>

<span data-ttu-id="d2794-107">このシナリオでは、**総勘定元帳パラメーター** ページの **収益認識** タブの **請求書の修正を売掛金勘定に転記** オプション (**収益認識 \> 設定 \> 総勘定元帳パラメーター**) は **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d2794-107">For this scenario, the **Post invoice corrections to Accounts receivable** option is set to **No** on the **Revenue recognition** tab of the **General ledger parameters** page (**Revenue recognition \> Setup \> General ledger parameters**).</span></span>

<span data-ttu-id="d2794-108">[![請求書の修正を売掛金勘定に転記のオプションをいいえに設定する](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="d2794-108">[![Post invoice corrections to Accounts receivable option set to No](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="d2794-109">顧客 US\_SI\_0003 の販売注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-109">A sales order is created for customer US\_SI\_0003.</span></span> <span data-ttu-id="d2794-110">顧客は、ラップトップ (品目番号 S0012) とそのサポート プラン (品目番号S0008、「継続的なエンジニアリング サービス」) を購入しています。</span><span class="sxs-lookup"><span data-stu-id="d2794-110">The customer is purchasing a laptop (item number S0012) and a support plan for it (item number S0008, "Sustained Engineering Service").</span></span> <span data-ttu-id="d2794-111">ラップトップの収益は直ちに認識されます (収益認識スケジュールはありません)。</span><span class="sxs-lookup"><span data-stu-id="d2794-111">The revenue for the laptop is immediately recognized (there is no revenue recognition schedule).</span></span> <span data-ttu-id="d2794-112">サポート プランの収益は、契約の日付範囲で定義された 12 か月にわたって繰り延べて認識されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-112">The revenue for the support plan will be deferred and recognized over 12 months, as defined by the date range in the contract.</span></span>

<span data-ttu-id="d2794-113">[![ラップトップとサポート プランの販売注文明細行](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="d2794-113">[![Sales order lines for the laptop and support plan](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="d2794-114">販売注文が確認済になりました。</span><span class="sxs-lookup"><span data-stu-id="d2794-114">The sales order is confirmed.</span></span> <span data-ttu-id="d2794-115">両方の品目が収益価格配賦に設定されているため、販売注文が確認されたときに、収益価格が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-115">Because both items are set up for revenue price allocation, the revenue price is calculated when the sales order is confirmed.</span></span> <span data-ttu-id="d2794-116">認識される収益は、**収益価格配賦** ページ (**販売注文** ページ、アクション ウィンドウ、**管理** タブの **収益認識** グループで、**収益価格の配賦** を選択) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-116">You can view the revenue that will be recognized on the **Revenue price allocation** page (on the **Sales order** page, on the Action Pane, on the **Manage** tab, in the **Revenue recognition** group, select **Revenue price allocation**).</span></span> <span data-ttu-id="d2794-117">ラップトップの収益は、1,008.01 ドルの金額で収益勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-117">The revenue for the laptop will be posted to the Revenue account in the amount of $1,008.01.</span></span> <span data-ttu-id="d2794-118">サポート プランの収益は、190.99 ドルの金額で、繰延収益勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-118">The revenue for the support plan will be posted to the Deferred revenue account in the amount of $190.99.</span></span> <span data-ttu-id="d2794-119">収益価格の合計は、収益価格の配賦を取得するために設定された明細行の合計 (1,199.00 ドル) と等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d2794-119">The sum of the revenue prices must equal the sum of the lines that were set up to capture revenue price allocation ($1,199.00).</span></span>

<span data-ttu-id="d2794-120">[![収益価格の配賦ページ](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="d2794-120">[![Revenue price allocation page](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="d2794-121">顧客は、販売時にはインストール サービス (品目番号 S0001) を購入しない選択をしましたが、後で気が変わりました。</span><span class="sxs-lookup"><span data-stu-id="d2794-121">The customer chose not to purchase installation services (item number S0001) at the time of the sale but later changed their mind.</span></span> <span data-ttu-id="d2794-122">このため、同じ顧客に 2 つめの販売注文が入力されました。</span><span class="sxs-lookup"><span data-stu-id="d2794-122">Therefore, a second sales order is entered for the same customer.</span></span>

<span data-ttu-id="d2794-123">[![インストール サービスの販売注文明細行](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="d2794-123">[![Sales order line for installation services](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="d2794-124">2 つめの販売注文が確認済になりました。</span><span class="sxs-lookup"><span data-stu-id="d2794-124">The second sales order is confirmed.</span></span> <span data-ttu-id="d2794-125">この販売注文は 1 つの明細行のみであるため、販売注文の確認時には、収益価格の配賦は実行されません。</span><span class="sxs-lookup"><span data-stu-id="d2794-125">Because this sales order contains only one line, revenue price allocation isn't done when the sales order is confirmed.</span></span> <span data-ttu-id="d2794-126">収益価格の配賦は、複数の固有品目があり、それらの品目が収益価格配賦用に設定されている場合にのみ行われます。</span><span class="sxs-lookup"><span data-stu-id="d2794-126">Revenue price allocation occurs only if there are two or more unique items, and if those items are set up for revenue price allocation.</span></span>

<span data-ttu-id="d2794-127">この新しい販売注文が顧客の契約に対する唯一の変更である場合は、再配賦プロセスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d2794-127">If this new sales order is the only change to the customer's contract, the reallocation process can now be run.</span></span> <span data-ttu-id="d2794-128">2 つの販売注文の 1 つで、**新しい注文明細行で価格を再配賦** を選択して、**新しい注文明細行で価格を再配賦** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d2794-128">In one of the two sales orders, select **Reallocate price with new order lines** to open the **Reallocate price with new order lines** page.</span></span> <span data-ttu-id="d2794-129">または、**収益認識\> 定期処理のタスク \> 新しい注文明細行で価格を再配賦** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d2794-129">Alternatively, go to **Revenue recognition \> Periodic tasks \> Reallocate price with new order lines**.</span></span> <span data-ttu-id="d2794-130">2 つの販売注文と対応する販売注文明細行を選択し、**再配賦の更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2794-130">Select the two sales orders and the corresponding sales order lines, and then select **Update reallocation**.</span></span> <span data-ttu-id="d2794-131">**再配賦金額** 列には、各販売注文明細行の新しい収益価格が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-131">The **Reallocated amount** column shows the new revenue price for each sales order line.</span></span>

<span data-ttu-id="d2794-132">[![新しい注文明細行で価格を再配賦のページの新しい収益価格](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="d2794-132">[![New revenue prices on the Reallocate price with new order lines page](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="d2794-133">**予想伝票** を選択した場合は、請求書が転記されていないため、何も表示されません。</span><span class="sxs-lookup"><span data-stu-id="d2794-133">If you select **Expected voucher**, nothing is shown, because no invoices have been posted.</span></span>

<span data-ttu-id="d2794-134">再配賦を完了するには、**プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2794-134">To complete the reallocation, select **Process**.</span></span> <span data-ttu-id="d2794-135">転記日付の入力を求められますが、転記は行われません。</span><span class="sxs-lookup"><span data-stu-id="d2794-135">You're prompted for a posting date, even if nothing is posted.</span></span> <span data-ttu-id="d2794-136">再配賦が完了すると、各販売注文の **収益価格の配賦** ページに、両方の販売注文のすべての品目の価格配賦が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2794-136">After the reallocation is completed, the **Revenue price allocation** page for each sales order will show the price allocation for all items across both sales orders.</span></span> <span data-ttu-id="d2794-137">つまり、各販売注文の **収益価格の配賦** ページには、その販売注文には存在しない品目が含まれます。それは、同じ契約の一部であるが、別の販売注文にあるためです。</span><span class="sxs-lookup"><span data-stu-id="d2794-137">In other words, the **Revenue price allocation** page for each sales order will include an item that doesn't exist on that sales order, because it's part of the same contract but on a different sales order.</span></span>

> [!TIP]
> <span data-ttu-id="d2794-138">これらの追加の品目が表示される理由に関する背景を提供するため、**再配賦 ID** や **販売注文** などの他の列をグリッドに追加できます。</span><span class="sxs-lookup"><span data-stu-id="d2794-138">To provide context about why these additional items are shown, you can add other columns to the grid, such as **Reallocation ID** and **Sales order**.</span></span>
> 
> <span data-ttu-id="d2794-139">[![収益価格の配賦ページの追加列](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="d2794-139">[![Additional columns on the Revenue price allocations page](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]