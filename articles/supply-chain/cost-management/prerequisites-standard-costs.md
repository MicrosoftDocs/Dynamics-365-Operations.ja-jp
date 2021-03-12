---
title: 標準原価の前提条件概要
description: このトピックでは、標準原価を使用するための基本的な手順について説明します。
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9333bda96ceae378ab74892534db13761038a06c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967361"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="45fa8-103">標準原価の前提条件概要</span><span class="sxs-lookup"><span data-stu-id="45fa8-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45fa8-104">このトピックでは、標準原価を使用するための基本的な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="45fa8-105">次の手順は、会社の工程に依存します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="45fa8-106">例えば、非製造環境、工順を使用しない製造環境、工順を使用する製造環境では手順が異なります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="45fa8-107">標準原価を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="45fa8-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="45fa8-108">**1. 標準原価用の品目モデル グループを作成します。**</span><span class="sxs-lookup"><span data-stu-id="45fa8-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="45fa8-109">**品目モデル グループ** ページを使用して標準原価用の新しいグループを作成し、**標準原価** の在庫モデルを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="45fa8-110">品目モデル グループの ID は、意味のあるもの (**Std Cost** など) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="45fa8-111">チェック ボックスをオンにすると、グループによる財務上のマイナス在庫が許可され、現物在庫および資産在庫が転記されます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="45fa8-112">この標準原価グループは、品目に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="45fa8-113">**2. 準原価差異に関連する勘定科目を定義します。**</span><span class="sxs-lookup"><span data-stu-id="45fa8-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="45fa8-114">**勘定科目表** ページを使用して、標準原価差異に関連する勘定科目を定義します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="45fa8-115">これらの勘定科目は、**転記** ページに割り当てる前に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="45fa8-116">勘定科目は、品目グループと原価グループを反映できます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="45fa8-117">**3. 勘定科目を、標準原価差異に関連する品目の転記に割り当てます。**</span><span class="sxs-lookup"><span data-stu-id="45fa8-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="45fa8-118">**転記** ページを使用して、標準原価差異に関連する勘定科目を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="45fa8-119">差異の勘定科目を、品目 (または品目グループ) 別と原価グループ (または原価グループ タイプ) 別に指定するか、または勘定科目がすべての品目とすべての原価グループに適用されるように指定することができます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="45fa8-120">これらのオプションは、テーブル、グループ、およびすべてに対する原価関係に対応します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="45fa8-121">品目転記ルールを定義する前に、**トランザクションの組み合わせ** ページを使用して、(テーブル、グループ、およびすべてに対する) 原価関係を有効にします。</span><span class="sxs-lookup"><span data-stu-id="45fa8-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="45fa8-122">**4. 標準原価に関連する在庫パラメータを定義します。**</span><span class="sxs-lookup"><span data-stu-id="45fa8-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="45fa8-123">**在庫会計ポリシーの設定 > パラメーター** ページの **在庫会計** タブを使用して、標準原価に関連する 2 つの原価管理パラメータを定義します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="45fa8-124">**原価内訳** フィールドで、**なし** または **補助元帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="45fa8-125">**補助元帳** を選択した場合、原価内訳は *有効* な原価内訳になります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="45fa8-126">有効な原価内訳は、標準原価品目の複数レベルの製品構成全体で、原価グループ セグメントを計算、保持、および表示するために不可欠です。</span><span class="sxs-lookup"><span data-stu-id="45fa8-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="45fa8-127">原価内訳が有効な場合は、原価グループごとの在庫、仕掛品 (WIP)、および販売済商品原価 (COGS) の報告と分析を、単一レベル、複数レベル、または総計形式で実行できます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="45fa8-128">原価内訳が有効な時に、製造品目のコストを有効にすると、品目の原価レコードの中に原価グループ区分が保存されます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="45fa8-129">**なし** を選択した場合、標準原価品目の原価グループ区分は維持されません。</span><span class="sxs-lookup"><span data-stu-id="45fa8-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="45fa8-130">つまり、製造された品目の標準原価は、原価グループ区分を持たない単一の金額として計算および管理されます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="45fa8-131">製造後のコンポーネントの原価貢献度が、単一の金額に集計されます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="45fa8-132">**標準に対する差異** フィールドの、**集計済** または **原価グループ別** と選択します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="45fa8-133">**原価グループ別** を選択した場合、コスト グループにより購買価格差異と製造差異を識別できます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="45fa8-134">製造差異 (ロット サイズ、数量、価格、および代替差異) の 4 種類が識別できるようになります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="45fa8-135">**集計済** を選択すると、コスト グループ別の差異と、4 種類の製造差異が区別できなくなります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="45fa8-136">確認できるのは、集計された製造差異だけとなります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="45fa8-137">標準に対する差異に関するポリシーは、原価計算ポリシーとは別に機能します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="45fa8-138">つまり、**なし** の原価計算ポリシーを選択しても、原価グループ別の差異を選択することで、原価グループ別の製造差異を把握できます。</span><span class="sxs-lookup"><span data-stu-id="45fa8-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="45fa8-139">**5. 標準原価用の原価バージョンを作成します。**</span><span class="sxs-lookup"><span data-stu-id="45fa8-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="45fa8-140">**原価バージョン設定** ページを使用して、標準原価用の 1 つ以上の原価計算バージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="45fa8-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="45fa8-141">各原価バージョンは、**標準原価** の原価タイプで指定される必要があり、原価データを含む内容を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="45fa8-142">**6. 標準原価を使用する既存の顧客を準備します。**</span><span class="sxs-lookup"><span data-stu-id="45fa8-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="45fa8-143">既存の品目を標準原価在庫モデルに変更する顧客は、**標準原価換算** ページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45fa8-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="45fa8-144">関連トピック</span><span class="sxs-lookup"><span data-stu-id="45fa8-144">Related topics</span></span>
--------

[<span data-ttu-id="45fa8-145">標準原価換算の概要</span><span class="sxs-lookup"><span data-stu-id="45fa8-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="45fa8-146">ブログ</span><span class="sxs-lookup"><span data-stu-id="45fa8-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="45fa8-147">コミュニティのブログ</span><span class="sxs-lookup"><span data-stu-id="45fa8-147">Community blogs</span></span>

- [<span data-ttu-id="45fa8-148">Dynamics 365 for Finance and Operations で直接材料の標準原価を設定する方法</span><span class="sxs-lookup"><span data-stu-id="45fa8-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="45fa8-149">Dynamics 365 for Finance and Operations での標準直接人件費</span><span class="sxs-lookup"><span data-stu-id="45fa8-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
