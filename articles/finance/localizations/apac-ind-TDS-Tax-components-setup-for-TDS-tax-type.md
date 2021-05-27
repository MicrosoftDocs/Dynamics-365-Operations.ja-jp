---
title: TDS の税タイプの税コンポーネントの設定
description: このトピックでは、源泉徴収税 (TDS) 税タイプの源泉徴収税コンポーネントを設定する方法について説明します。 また、各 TDS コンポーネントごとに TDS の算出に使用するしきい値を定義する方法についても説明しています。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023383"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="8cbaf-104">TDS の税タイプの税コンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="8cbaf-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cbaf-105">このトピックでは、源泉徴収税 (TDS) 税タイプの源泉徴収税コンポーネントを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="8cbaf-106">TDS コンポーネントは、TDS、割増金、PE-Cess、SHE Cess です。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="8cbaf-107">このトピックではまた、各 TDS コンポーネントごとに TDS の算出に使用するしきい値を定義する方法についても説明しています。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="8cbaf-108">さらに、各 TDS コンポーネントの TDS 算出に使用される例外的なしきい値を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="8cbaf-109">以下の手順で、TDS のコンポーネントを設定します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="8cbaf-110">**税 \> 設定 \> 源泉徴収税 \> 源泉徴収税のコンポーネント** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="8cbaf-111">[![源泉徴収税グループ コンポーネントのページ](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="8cbaf-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="8cbaf-112">**税 タイプ** フィールドで、**TDS** を選択して、TDS 税タイプの源泉徴収税コンポーネントを設定します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="8cbaf-113">アクション ウィンドウで **新規** を選択して、明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="8cbaf-114">**源泉徴収税コンポーネント** フィールドに、TDS コンポーネントの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="8cbaf-115">**源泉徴収税コンポーネント グループ** フィールドで、TDS コンポーネントを関連付ける TDS 源泉徴収税コンポーネント グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="8cbaf-116">**一般** クイック タブの **説明** フィールドに、TDS コンポーネントの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="8cbaf-117">アクション ウィンドウで、**しきい値** を選択して **しきい値** のページを開き、TDS コンポーネントの TDS 計算に使用されるしきい値を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="8cbaf-118">**開始日** フィールドおよび **終了日** フィールドを使用して、しきい値を適用できる期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="8cbaf-119">**一般** クイック タブの **しきい値** フィールドに、TDS コンポーネントの TDS の計算に使用するしきい値の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="8cbaf-120">請求書の累積金額が基準額を超えた場合にのみ、税金が源泉徴収されます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="8cbaf-121">たとえば、しきい値が 10,000 の場合、請求書の累積金額が 10,000 を超えた後に (つまり、10,001 以上になってから) TDS を計算します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="8cbaf-122">**例外しきい値** フィールドに、TDS コンポーネントの TDS の計算に使用する例外しきい値の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="8cbaf-123">請求書明細行の税金は、その金額が例外的なしきい値を超えた場合にのみ、源泉で差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="8cbaf-124">たとえば、例外のしきい値金額が 5,000 である場合、請求明細金額が 5,000 を超える場合 (つまり、5,001 以上の場合)、TDS が特定の請求明細に対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="8cbaf-125">[![しきい値のページ](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="8cbaf-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="8cbaf-126">例外のしきい値の金額がしきい値以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="8cbaf-127">請求書の累積金額が **しきい値** フィールドで指定されたしきい値を超えていない場合でも、取引金額が例外的にしきい値を超えた場合には、その取引に対して税金が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="8cbaf-128">**しきい値** ページを閉じて、**源泉徴収税コンポーネント** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="8cbaf-129">アクション ウィンドウで、**コピー** を選択して **源泉徴収税コンポーネントのコピー** ダイアログ ボックスを開き、1 つの TDS コンポーネント グループに設定された TDS コンポーネントを別の TDS コンポーネント グループにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="8cbaf-130">**コピー元** フィールドで、TDS コンポーネントのコピー元の TDS コンポーネント グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="8cbaf-131">**コピー先** フィールドで、源泉徴収税 コンポーネントのコピー先の TDS コンポーネント グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8cbaf-132">TDS コンポーネント グループの両方に関連付けられた一般的な TDS コンポーネントはコピーされません。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="8cbaf-133">**OK** を選択し、**源泉徴収票コンポーネント** ページでもう一方の TDS コンポーネント グループの TDS コンポーネントをコピー、作成します。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="8cbaf-134">[![源泉徴収税コンポーネントのダイアログ ボックスをコピーする](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="8cbaf-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="8cbaf-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8cbaf-135">Close the page.</span></span>
