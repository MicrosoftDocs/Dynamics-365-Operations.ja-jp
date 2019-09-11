---
title: メンテナンス予算の更新
description: このトピックでは、資産管理でメンテナンス予算を更新する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 486782968816cc585d9cf2d753f32e82f85e4f7e
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874788"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="54cd9-103">メンテナンス予算の更新</span><span class="sxs-lookup"><span data-stu-id="54cd9-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="54cd9-104">**メンテナンス予算明細行** ページには、**メンテナンス予算**ページで選択した予算に対して作成されたすべての予算明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="54cd9-105">詳細については、[メンテナンス予算の作成](create-maintenance-budget.md)を参照してください。メンテナンス予算が承認されるまで、メンテナンス予算明細行を再計算および調整できます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="54cd9-106">予算期間が過ぎ、原価が資産管理に転記された後は、実際原価で予算明細行を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="54cd9-107">メンテナンス予算の再計算</span><span class="sxs-lookup"><span data-stu-id="54cd9-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="54cd9-108">**メンテナンス予算明細行**ページで、メンテナンス予算を再計算できます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="54cd9-109">メンテナンス予算を再計算すると、既存の予算明細行が削除され、新しい計算が実行されます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="54cd9-110">**メンテナンス予算明細行**ページで、**再計算**を選択します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="54cd9-111">**予算の再計算**ダイアログボックスで、新しい計算に必要な変更を行い、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="54cd9-112">新しい予算明細行は、設定した値に従って作成されます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="54cd9-113">予算明細行の調整</span><span class="sxs-lookup"><span data-stu-id="54cd9-113">Adjust budget lines</span></span>

<span data-ttu-id="54cd9-114">メンテナンス予算全体を再計算する代わりに、予算原価に関連する選択された明細行を調整できます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="54cd9-115">**メンテナンス予算明細行**ページで、予算原価を更新する明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="54cd9-116">**調整**を選択します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="54cd9-117">選択した明細行に金額を追加するには、**原価の追加**チェック ボックスをオンにし、**値の追加**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="54cd9-118">選択した予算明細行のの予算原価に係数を乗算するには、**原価を乗算**チェック ボックスをオンにし、**乗算値**フィールドに係数を入力します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="54cd9-119">たとえば、**乗算値**フィールドに **1.2** と入力すると、選択した明細行の予算原価が 20 パーセント増加します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="54cd9-120">**0.7** を入力すると、選択した明細行の予算原価が 30 パーセント減少します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="54cd9-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-121">Select **OK**.</span></span>

<span data-ttu-id="54cd9-122">選択された予算明細行は、手順 3 または 4 で設定した値に従って更新されます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="54cd9-123">実際原価の更新</span><span class="sxs-lookup"><span data-stu-id="54cd9-123">Update actual costs</span></span>

<span data-ttu-id="54cd9-124">予算明細行の日付が過ぎ、実際原価が資産管理に転記された後は、メンテナンス予算で実際原価を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="54cd9-125">**メンテナンス予算明細行**ページで、**原価の更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="54cd9-126">**実際原価の計算**ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="54cd9-127">実際原価が転記されている場合は、予算明細行の**実際原価**フィールドが更新されます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="54cd9-128">予算を作成してから新しい資産タイプが作成され、これらの資産タイプが、作業指示書が作成され関連原価が転記された資産で使用されている場合、新しい予算明細行が生成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="54cd9-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="54cd9-129">予算原価が計算されないため、新しい予算明細行には実際原価のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="54cd9-130">予防的コスト、修正コスト、および投資コストに分割された実際原価の概要を表示するには、**資産原価管理**ページで同じ期間に対して計算を実行します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="54cd9-131">手動で予算明細行を追加する</span><span class="sxs-lookup"><span data-stu-id="54cd9-131">Manually add budget lines</span></span>

<span data-ttu-id="54cd9-132">**メンテナンス予算明細行**ページで**新規**を選択し、明細行で選択を行うことにより、新しい予算明細行を手動で追加できます。</span><span class="sxs-lookup"><span data-stu-id="54cd9-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="54cd9-133">次の例では、このアプローチが役立つ状況の例を示します。</span><span class="sxs-lookup"><span data-stu-id="54cd9-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="54cd9-134">一部の資産の改修は現在計画段階にありますが、関連するジョブはまだ資産管理に作成されていないことがわかっています。</span><span class="sxs-lookup"><span data-stu-id="54cd9-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="54cd9-135">ただし、これらのジョブの予算原価をメンテナンス予算に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="54cd9-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="54cd9-136">メンテナンス予算を作成してから新しい資産または資産タイプが作成されましたが、メンテナンス計画はそれらの資産または資産タイプに対してまだ設定されていません。</span><span class="sxs-lookup"><span data-stu-id="54cd9-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="54cd9-137">ただし、これらの資産タイプの予算原価をメンテナンス予算に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="54cd9-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
