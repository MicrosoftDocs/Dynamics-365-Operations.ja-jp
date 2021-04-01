---
title: 購買トランザクションの源泉徴収税
description: 源泉徴収税を受け取る仕入先については、**すべての仕入先** ページで既定の **源泉徴収税グループ** を割り当てる必要があります。
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256670"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="6cfb0-103">購買トランザクションの源泉徴収税</span><span class="sxs-lookup"><span data-stu-id="6cfb0-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="6cfb0-104">源泉徴収税を受け取る仕入先については、**すべての仕入先** ページで既定の **源泉徴収税グループ** を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="6cfb0-105">**ナビゲーション ペイン > モジュール > 買掛金勘定 > 仕入先 > すべての仕入先** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="6cfb0-106">それぞれの仕入先をクリックし、**編集** を クリックします。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="6cfb0-107">**請求書と配送** タブで、**源泉徴収税の計算** フィールドを **はい** に設定 します。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="6cfb0-108">データでこの仕入先に対して **源泉徴収税の計算** がオンにされていない場合、源泉徴収税は計算されません。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="6cfb0-109">源泉徴収税グループ内の **源泉徴収税グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="6cfb0-110">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-110">Click **Save**.</span></span>

<span data-ttu-id="6cfb0-111">源泉徴収税を受け取る品目/サービスについては、**リリースされた製品** で既定の **品目源泉徴収税グループ** を割 り当てできます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="6cfb0-112">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="6cfb0-113">それぞれの品目番号をクリックし、**編集** を クリックします。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="6cfb0-114">**購買** タブで、**源泉徴収税の計算** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="6cfb0-115">**リリース済製品** ページの **購買** タブでこの品目について **源泉徴収税の税金** を計算する方法が **はい** に設定されていない場合、源泉徴収税は計算されません。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="6cfb0-116">**品目源泉徴収税グループ** リスト内で品目源泉徴収税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="6cfb0-117">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-117">Click **Save**.</span></span>

<span data-ttu-id="6cfb0-118">源泉徴収税グループと品目源泉徴収税グループは、次のページで割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="6cfb0-119">**発注書**</span><span class="sxs-lookup"><span data-stu-id="6cfb0-119">**Purchase order**</span></span>
- <span data-ttu-id="6cfb0-120">**仕入先請求書**</span><span class="sxs-lookup"><span data-stu-id="6cfb0-120">**Vendor invoice**</span></span>
- <span data-ttu-id="6cfb0-121">**請求仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="6cfb0-121">**Invoice journal**</span></span>

<span data-ttu-id="6cfb0-122">**発注書** や **保留中の仕入先請求書** の作成時に、既定の源泉徴収税グループと品目源泉徴収税グループが明細行に 転記されます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="6cfb0-123">**仕入先請求仕訳帳** の場合は、**源泉徴収税の計算** をオンにし、仕訳帳の **全般** タブで **品目の源泉徴収税グループ** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="6cfb0-124">源泉徴収税の一時的な金額は、**発注書** ページの **合計** タブの **調整済源泉徴収税** フィールド で使用 きます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![発注書には源泉徴収税が含まれます](media/withholding-tax-adjusted.png)

<span data-ttu-id="6cfb0-126">源泉徴収税は、**仕入先支払仕訳帳** で計算されます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="6cfb0-127">**トランザクションの決済** ページの **源泉徴収税** タブにある実際の源泉徴収税額と同様に、該当する源泉徴収税コードを手動で調整できます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![源泉徴収は、[トランザクションの決済] ページで手動で調整できます](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="6cfb0-129">派生した源泉徴収税額は仕入先支払から差し引き、関連する伝票の **源泉徴収税勘定** に転記されます。</span><span class="sxs-lookup"><span data-stu-id="6cfb0-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![関連する伝票が表示される源泉徴収税勘定](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]