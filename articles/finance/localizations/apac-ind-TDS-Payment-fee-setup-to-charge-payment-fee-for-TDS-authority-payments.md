---
title: TDS 所轄官庁支払の支払手数料の設定
description: このトピックでは、源泉徴収 (TDS) 所轄官庁の支払いに課金される支払い手数料を設定する方法について説明します。
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023403"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="ee7c5-103">TDS 所轄官庁支払の支払手数料の設定</span><span class="sxs-lookup"><span data-stu-id="ee7c5-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee7c5-104">このトピックでは、源泉徴収 (TDS) 所轄官庁の支払いに課金される支払い手数料を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="ee7c5-105">**買掛金勘定 \> 支払の設定 \> 支払手数料** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="ee7c5-106">[![支払手数料のページ](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="ee7c5-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="ee7c5-107">**新規** を支払手数料を作成し、必要な情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="ee7c5-108">**支払いの種類** フィールドで、支払手数料の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="ee7c5-109">**None**</span><span class="sxs-lookup"><span data-stu-id="ee7c5-109">**None**</span></span>
    - <span data-ttu-id="ee7c5-110">**利子** - 利息は、TDS 所轄官庁の仕入先に対して行われた支払の延滞に対して請求されます。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="ee7c5-111">**その他** - その他の手数料は、TDS 所轄官庁の仕入先に対して行われた支払の延滞に対して請求されます。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="ee7c5-112">**利息** または **その他** を選択した場合、**請求** ィールドは自動的に **元帳** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="ee7c5-113">**フィールド タイプ** フィールドで **利子など** や **その他** を選択した場合は、**主要勘定** フィールドで、利息や他の請求費用を転記する勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="ee7c5-114">他に必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-114">Enter the other required details.</span></span>
6. <span data-ttu-id="ee7c5-115">アクション ウィンドウで、**支払手数料の設定** を選択して **支払手数料の設定** ページを開きます。このページでは、銀行、支払方法、支払仕様、通貨、および日付間隔の各種の組み合わせに対して支払手数料を設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="ee7c5-116">[![支払手数料の設定ページ](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="ee7c5-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="ee7c5-117">**概要** タブの **グループ化** フィールドで、支払手数料を設定する銀行を 指定します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="ee7c5-118">**テーブル** - 手数料は特定の銀行口座に対して有効です。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="ee7c5-119">**グループ** - 手数料は特定の銀行グループに対して有効です。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="ee7c5-120">**すべて** – 手数料は、すべての銀行口座に対して有効です。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="ee7c5-121">**グループ化** フィールドで **テーブル** または **グループ** を選択した場合は、**銀行の関連付け** フィールドで、支払手数料を設定する特定の銀行口座または銀行グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="ee7c5-122">**支払い方法** で、料金の支払い方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="ee7c5-123">**支払の仕様** フィールドで、**支払の仕様** ページで生成された支払仕様コードを選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="ee7c5-124">支払仕様は、電子資金振替に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="ee7c5-125">**支払通貨** フィールドで、手数料を有効にする通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="ee7c5-126">手数料を有効化できるのは、選択した通貨を使用するトランザクションのみです。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="ee7c5-127">このフィールドを空白にすると、すべての通貨で手数料が有効になります。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="ee7c5-128">**割合/金額** フィールドで、計算方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="ee7c5-129">オプションは、**金額**、**割合**、**間隔** です。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="ee7c5-130">**手数料金額** フィールドで、手数料の金額を、支払額に対する割合または 1 回の支払額のいずれかで指定します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="ee7c5-131">**手数料の通貨** フィールドで、手数料の通貨コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="ee7c5-132">**全般** タブを選択して、選択した銀行口座の詳細を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="ee7c5-133">[![[全般] タブ](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="ee7c5-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="ee7c5-134">**最小** フィールドに、手数料を有効にする最小トランザクション金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="ee7c5-135">**最大** フィールドに、手数料を有効にする最大トランザクション金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="ee7c5-136">**開始日** フィールドおよび **終了日** フィールドで、計算手数料の日付範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="ee7c5-137">**最小金額** フィールドで、支払額に対する割合または 1 回の支払額のいずれかで、手数料の金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="ee7c5-138">**売上税グループ** フィールドで、手数料金額に対する売上税の計算に使用する売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="ee7c5-139">**品目の売上税グループ** フィールドで、手数料金額に対する品目の売上税の計算に使用する品目の売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="ee7c5-140">**間隔** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="ee7c5-141">[![間隔タブ](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="ee7c5-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="ee7c5-142">**日数** フィールドで、支払いの計上日 (割引日) から約束手形の支払期日までの日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="ee7c5-143">**割合/金額** フィールドで、詳細が割合か設定金額かを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="ee7c5-144">**手数料の金額金額** フィールドで、支払額に対する割合または 1 回の支払額のいずれかで、手数料の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="ee7c5-145">**支払手数料の設定** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="ee7c5-146">**支払手数料の** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ee7c5-146">Close the **Payment fee** page.</span></span>
