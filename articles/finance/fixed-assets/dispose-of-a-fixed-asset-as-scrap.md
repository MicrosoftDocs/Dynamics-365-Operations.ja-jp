---
title: 固定資産の仕損としての処分
description: このトピックでは、仕損として処分された固定資産のトランザクションを除去するプロセスについて説明します。
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 413847d350ca6b2bdd6153a598ea5b3f34a33818
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826278"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="ffe61-103">固定資産の仕損としての処分</span><span class="sxs-lookup"><span data-stu-id="ffe61-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffe61-104">このトピックでは、仕損として処分された固定資産のトランザクションを除去するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ffe61-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="ffe61-105">削除できるトランザクションタイプには、資産の取得、減価償却トランザクションなどの固定資産トランザクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="ffe61-106">これらのトランザクションが削除されると、取得原価調整、減価償却調整、再評価、評価増および評価減の勘定など、貸借対照表の勘定に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="ffe61-107">取引</span><span class="sxs-lookup"><span data-stu-id="ffe61-107">Transaction</span></span>                                         | <span data-ttu-id="ffe61-108">借方 (Dr.)</span><span class="sxs-lookup"><span data-stu-id="ffe61-108">Debit (Dr.)</span></span> | <span data-ttu-id="ffe61-109">貸方 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="ffe61-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="ffe61-110">Dr. 減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="ffe61-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="ffe61-111">x</span><span class="sxs-lookup"><span data-stu-id="ffe61-111">X</span></span>           |              |
| <span data-ttu-id="ffe61-112">Cr. 固定資産の利益/損失</span><span class="sxs-lookup"><span data-stu-id="ffe61-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="ffe61-113">x</span><span class="sxs-lookup"><span data-stu-id="ffe61-113">X</span></span>            |
| <span data-ttu-id="ffe61-114">Dr. 固定資産の利益/損失</span><span class="sxs-lookup"><span data-stu-id="ffe61-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="ffe61-115">x</span><span class="sxs-lookup"><span data-stu-id="ffe61-115">X</span></span>           |              |
| <span data-ttu-id="ffe61-116">Cr. 固定資産の取得勘定</span><span class="sxs-lookup"><span data-stu-id="ffe61-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="ffe61-117">x</span><span class="sxs-lookup"><span data-stu-id="ffe61-117">X</span></span>            |
| <span data-ttu-id="ffe61-118">Dr. 固定資産の利益/損失 (正味簿価額 \[NBV\])</span><span class="sxs-lookup"><span data-stu-id="ffe61-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="ffe61-119">x</span><span class="sxs-lookup"><span data-stu-id="ffe61-119">X</span></span>           |              |
| <span data-ttu-id="ffe61-120">Cr. 固定資産の利益/損失 (NBV)</span><span class="sxs-lookup"><span data-stu-id="ffe61-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="ffe61-121">x</span><span class="sxs-lookup"><span data-stu-id="ffe61-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="ffe61-122">会社の最高財務責任者 (CFO) または管理者と密接に協力して、各トランザクション タイプに使用する適切な勘定を識別し、処分プロセスとトランザクションを検証して、アカウントの正しい更新を生成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ffe61-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="ffe61-123">固定資産を仕損として処分する前に、資産の取得金額、今年度の減価償却、前年度の減価償却、および資産の NBV に関連付けられている勘定科目を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffe61-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="ffe61-124">固定資産トランザクション タイプは、**固定資産転記プロファイル** ページに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="ffe61-125"> **固定資産 \> 設定 \> 固定資産転記プロファイル** の順に移動し、**処分** クイック タブでグリッドの上のフィールドにある **仕損** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffe61-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="ffe61-126">次の図は、**固定資産の転記プロファイル** ページにある固定資産トランザクション タイプの一覧を示しています。</span><span class="sxs-lookup"><span data-stu-id="ffe61-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="ffe61-127">[![仕損としての資産の処分 (図1)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="ffe61-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="ffe61-128">次の例では、2018 年 1 月 1 日に取得された固定資産が 2019 年 3 月 31 日に仕損されます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="ffe61-129">**取得価格:** 24,000.00 米ドル (USD)</span><span class="sxs-lookup"><span data-stu-id="ffe61-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="ffe61-130">**耐用年数:** 2 年間</span><span class="sxs-lookup"><span data-stu-id="ffe61-130">**Service life:** Two years</span></span>
- <span data-ttu-id="ffe61-131">**減価償却方法:** 定額法耐用年数</span><span class="sxs-lookup"><span data-stu-id="ffe61-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="ffe61-132">**減価償却額:** 毎月 1,000.00 USD</span><span class="sxs-lookup"><span data-stu-id="ffe61-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="ffe61-133">固定資産の NBV は次の式を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="ffe61-134">正味簿価額 = 取得価格 – 減価償却</span><span class="sxs-lookup"><span data-stu-id="ffe61-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="ffe61-135">この例では、固定資産が取得されて、2018 年 1 月から 2019 年 3 月までの 15 か月間の減価償却が行われました。</span><span class="sxs-lookup"><span data-stu-id="ffe61-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="ffe61-136">したがって、資産の NBV は9,000.00 USD (24,000.00 USD – 15,000.00 USD) になります。</span><span class="sxs-lookup"><span data-stu-id="ffe61-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="ffe61-137">[![固定資産の減価償却の例](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="ffe61-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="ffe61-138">処分仕訳帳を作成するには、**固定資産 \> 仕訳入力 \> 固定資産仕訳帳l** の順に移動し、アクション ウィンドウで、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffe61-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="ffe61-139">**処分 - 仕損** を選択し、固定資産 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffe61-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="ffe61-140">資産を完全に処分するには、**借方** フィールドまたは **貸方** フィールドに値を入力しないようにします。</span><span class="sxs-lookup"><span data-stu-id="ffe61-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="ffe61-141">[![固定資産仕訳帳](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="ffe61-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="ffe61-142">固定資産の処分仕損トランザクションでは、固定資産帳簿のフィールド値が次のように変更されます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="ffe61-143">**残高** セクションで、**ステータス** フィールドが **仕損** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="ffe61-144">**払出** セクションで、**処分日** フィールドは資産が仕損された日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ffe61-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="ffe61-145">[![固定資産仕訳帳の詳細](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="ffe61-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="ffe61-146">次の図は、固定資産の残高を示しています。</span><span class="sxs-lookup"><span data-stu-id="ffe61-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="ffe61-147">[![固定資産の残高](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="ffe61-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="ffe61-148">次の図は、転記された伝票を示しています。</span><span class="sxs-lookup"><span data-stu-id="ffe61-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="ffe61-149">[![正味帳簿価格](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="ffe61-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]