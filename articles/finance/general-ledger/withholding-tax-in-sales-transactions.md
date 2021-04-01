---
title: 販売トランザクションの源泉徴収税
description: このトピックでは、選択した顧客に対する源泉徴収税の計算を回避する手順を示します。 支払で源泉徴収税を指定する顧客については、既定の源泉徴収税グループを割り当てる必要があります。
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
ms.openlocfilehash: c839df1b54cdb60beefa6dc6c3fc6e945a6eac85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256646"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="f5cc6-104">販売トランザクションの源泉徴収税</span><span class="sxs-lookup"><span data-stu-id="f5cc6-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="f5cc6-105">このトピックでは、選択した顧客に対する源泉徴収税の計算を回避する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="f5cc6-106">支払で源泉徴収税を指定する顧客については、**顧客** ページで既定の **源泉徴収税グループ** を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="f5cc6-107">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 顧客 > すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="f5cc6-108">それぞれの顧客をクリックし、**編集** を クリックします。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="f5cc6-109">**請求書と配送** タブで、**源泉徴収税の計算** フィールドを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f5cc6-110">マスター データでこの顧客に対して **源泉徴収税の計算** がオンにされていない場合、源泉徴収税は計算されません。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="f5cc6-111">源泉徴収税グループ内の **源泉徴収税グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="f5cc6-112">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-112">Click **Save**.</span></span>

<span data-ttu-id="f5cc6-113">源泉徴収税を受け取る品目/サービスについては、**リリースされた製品** で既定の **品目源泉徴収税グループ** を割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="f5cc6-114">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="f5cc6-115">それぞれの品目番号をクリックし、**編集** を クリックします。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="f5cc6-116">**販売** タブで、**源泉徴収税の計算** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f5cc6-117">**リリース済製品** ページの **販売** タブでこの品目について **源泉徴収税の税金** を計算する方法が **はい** に設定されていない場合、源泉徴収税は計算されません。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="f5cc6-118">**品目源泉徴収税グループ** リスト内で品目源泉徴収税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="f5cc6-119">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-119">Click **Save**.</span></span>

<span data-ttu-id="f5cc6-120">源泉徴収税グループと品目源泉徴収税グループは、**販売注文** ページで割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="f5cc6-121">新しい販売注文を作成する場合は、既定の源泉徴収税グループと品目源泉徴収税グループが、販売注文明細行の既定の入力値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="f5cc6-122">源泉徴収税が計算され、**顧客支払仕訳帳** と一緒に転記されます。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="f5cc6-123">**トランザクションの決済** ページの **源泉徴収税** タブにある実際の源泉徴収税額と同様に、該当する源泉徴収税コードを手動で調整できます。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="f5cc6-124">算出されたした源泉徴収税額は顧客の支払から差し引き、関連する伝票の **源泉徴収税勘定オフセット** 勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="f5cc6-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]