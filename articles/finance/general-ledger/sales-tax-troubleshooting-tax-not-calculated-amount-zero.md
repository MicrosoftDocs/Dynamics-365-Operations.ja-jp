---
title: 税金が計算されない、または税額がゼロになる
description: このトピックでは、税額が 0 (ゼロ) になる場合、または税金が計算されていない場合に役立つトラブルシューティングの情報を提供します。
author: shtao
ms.date: 04/01/2021
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
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020118"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="45392-103">税金が計算されない、または税額がゼロになる</span><span class="sxs-lookup"><span data-stu-id="45392-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45392-104">トランザクションの明細金額は 0 (ゼロ) 以外になりますが、計算されない場合や計算された税額が 0 になることもあります。</span><span class="sxs-lookup"><span data-stu-id="45392-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="45392-105">この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="45392-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="45392-106">トランザクションで税コードが正しく選択されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="45392-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="45392-107">トランザクションで正しい税コードが選択されていない場合、または税コードが選択されていない場合、税金は計算されません。</span><span class="sxs-lookup"><span data-stu-id="45392-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="45392-108">次の手順に従って、トランザクションで税コードが正しく選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="45392-109">トランザクション明細行で、**明細行の詳細** クイック タブの、**設定** タブの、**消費税** セクションで、**品目消費税グループ** フィールドと **消費税グループ** フィールドに正しい税グループが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="45392-110">正しい税グループが選択されていない場合は、選択します。</span><span class="sxs-lookup"><span data-stu-id="45392-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="45392-111">[![品目消費税グループと消費税グループフィールド](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="45392-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="45392-112">**税** \> **間接税** \> **消費税** \> **消費税グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45392-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="45392-113">適切な消費税グループを選択し、**設定** クイック タブで、**消費税コード** フィールドの税コードをメモします。</span><span class="sxs-lookup"><span data-stu-id="45392-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="45392-114">[![消費税グループ ページ](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="45392-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="45392-115">**税** \> **間接税** \> **消費税** \> **品目消費税グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45392-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="45392-116">適切な品目消費税グループを選択し、**設定** クイック タブで、**消費税コード** フィールドの税コードが消費税グループの税コードと一致しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="45392-117">[![品目消費税グループ ページ](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="45392-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="45392-118">税コードが一致しない場合は、消費税コードをグループのいずれかに更新します。</span><span class="sxs-lookup"><span data-stu-id="45392-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="45392-119">選択した税コードが免税でないか、税率の値が正確かを確認する</span><span class="sxs-lookup"><span data-stu-id="45392-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="45392-120">税コードが免税の場合、または税率が 0 (ゼロ) の場合、税計算結果は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="45392-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="45392-121">次の手順に従って、選択した税コードが免税かどうか識別し、正確な税率が適用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="45392-122">**税** \> **間接税** \> **消費税** \> **消費税グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45392-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="45392-123">適切な消費税グループを選択し、**設定** クイック タブで、**免税** チェック ボックスがオフになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="45392-124">選択されている場合はオフにしてください。</span><span class="sxs-lookup"><span data-stu-id="45392-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="45392-125">[![消費税グループ ページの免税チェック ボックス](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="45392-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="45392-126">**税** \> **間接税** \> **消費税** \> **消費税コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45392-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="45392-127">適切な消費税コードを選択し、**値** フィールドの税率の値が 0 (ゼロ) でないかを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="45392-128">0 の場合は、フィールドを更新して、正確な税率を設定します。</span><span class="sxs-lookup"><span data-stu-id="45392-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="45392-129">[![消費税コード値ページの値フィールド](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="45392-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="45392-130">ゼロが正しい税額かどうかを判断する</span><span class="sxs-lookup"><span data-stu-id="45392-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="45392-131">シナリオによっては、税額が 0 (ゼロ) で正しい場合があります。</span><span class="sxs-lookup"><span data-stu-id="45392-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="45392-132">トランザクションの正確な税額が 0 かどうかを確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="45392-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="45392-133">**一般会計** \> **元帳の設定** \> **総勘定元帳パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45392-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="45392-134">**消費税** タブの、**計算方法** フィールドで、**合計** が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="45392-135">[![総勘定元帳パラメーター ページの計算フィールド](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="45392-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="45392-136">**税** \> **間接税** \> **消費税** \> **消費税コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45392-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="45392-137">適切な消費税コードを選択し、**計算** \> **基準金額** を選択して、基準金額が **請求書残高の正味金額** または **その他の売上税金額を含む請求合計** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="45392-138">詳細については、[その他の売上税金額を含む請求合計](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45392-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="45392-139">手順 2 と 4 で正しい値が設定されている場合は、トランザクションの合計金額が 0 (ゼロ) かどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="45392-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="45392-140">合計金額が 0 の場合、予想される結果は税額 0 です。</span><span class="sxs-lookup"><span data-stu-id="45392-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="45392-141">税額は請求書残高の合計金額に基づいて計算され、1 行ずつ計算されないため、税計算の後、各明細行に税額 0 が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="45392-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="45392-142">カスタマイズが存在するかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="45392-142">Determine whether customization exists</span></span>

<span data-ttu-id="45392-143">前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="45392-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="45392-144">カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="45392-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
