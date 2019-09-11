---
title: 顧客支払手数料の設定
description: 顧客支払の支払手数料を作成します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5b94578e077834ce73c921dca18ad6e38c37659
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916303"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="1499a-103">顧客支払手数料の設定</span><span class="sxs-lookup"><span data-stu-id="1499a-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1499a-104">顧客支払の支払手数料を作成します。</span><span class="sxs-lookup"><span data-stu-id="1499a-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="1499a-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="1499a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1499a-106">**ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 支払設定 > 支払手数料**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1499a-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Payment fee**.</span></span>
2. <span data-ttu-id="1499a-107">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1499a-107">Click **New**.</span></span>
3. <span data-ttu-id="1499a-108">**手数料 ID** フィールドに、手数料 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="1499a-108">In the **Fee ID** field, enter a Fee ID.</span></span> <span data-ttu-id="1499a-109">支払仕訳帳には手数料 ID が表示されるため、どの手数料が算定されるかを分かるようにそれを記述します。</span><span class="sxs-lookup"><span data-stu-id="1499a-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="1499a-110">**名前**フィールドに、手数料名を入力します。</span><span class="sxs-lookup"><span data-stu-id="1499a-110">In the **Name** field, enter a fee name.</span></span>
5. <span data-ttu-id="1499a-111">**手数料の説明**フィールドに、手数料の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1499a-111">In the **Fee description** field, enter a description for the fee.</span></span>
6. <span data-ttu-id="1499a-112">**請求金額**フィールドで、手数料が顧客または勘定科目に請求されるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-112">In the **Charge** field, select whether the fee will be charged to the Customer or a Ledger account.</span></span> <span data-ttu-id="1499a-113">顧客が手数料を算定する場合、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="1499a-114">手数料が経費として組織に算定される場合、「元帳」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="1499a-115">このタスクに関しては、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="1499a-116">**仕訳帳タイプ**フィールドで、この支払手数料を使用できる仕訳帳タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-116">In the **Journal type** field, select the type of journal that can use this payment fee.</span></span> <span data-ttu-id="1499a-117">これらの手数料は、顧客支払に使用されると、仕訳帳タイプは顧客支払となる可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="1499a-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="1499a-118">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1499a-118">Click **Save**.</span></span>
9. <span data-ttu-id="1499a-119">**支払手数料の設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1499a-119">Click **Payment fee setup**.</span></span> <span data-ttu-id="1499a-120">支払手数料の設定は、支払手数料が評価されるときに、基準を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1499a-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="1499a-121">たとえば、銀行口座が USMF OPER であり、支払方法が小切手である場合、費用が計算されるように指定できます。</span><span class="sxs-lookup"><span data-stu-id="1499a-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="1499a-122">**グループ化**フィールドで、どの銀行口座がこの手数料を評価するかを定義するためには、テーブル、グループまたはすべてを選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-122">In the **Groupings** field, select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span> <span data-ttu-id="1499a-123">「すべて」を選択した場合、すべての銀行口座がこの手数料を評価する場合があります。</span><span class="sxs-lookup"><span data-stu-id="1499a-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="1499a-124">「テーブル」を選択し、選択した銀行口座のみがこの手数料を評価できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1499a-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="1499a-125">「グループ」を選択した場合、選択された銀行グループの銀行口座のみがこの手数料を評価できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1499a-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="1499a-126">**銀行関係**フィールドで、銀行グループまたは銀行口座のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-126">In the **Bank relation** field, select either a bank group or a bank account.</span></span> <span data-ttu-id="1499a-127">「テーブル」を選択した場合、ルックアップによって銀行口座を表示します。</span><span class="sxs-lookup"><span data-stu-id="1499a-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="1499a-128">「グループ」を選択した場合、ルックアップによって銀行グループを表示します。</span><span class="sxs-lookup"><span data-stu-id="1499a-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="1499a-129">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1499a-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="1499a-130">**支払方法**フィールドで、この手数料を査定する支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-130">In the **Mehtod of payment** field, select the Method of payment for which this fee will be assessed.</span></span> <span data-ttu-id="1499a-131">たとえば、支払を電子支払ではなく、小切手で行った場合、顧客の手数料を評価できます。</span><span class="sxs-lookup"><span data-stu-id="1499a-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="1499a-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="1499a-133">該当する場合は、**支払通貨**フィールドで、支払通貨を入力します。</span><span class="sxs-lookup"><span data-stu-id="1499a-133">If relevant, in the **Payment currency** field, enter a payment currency.</span></span> <span data-ttu-id="1499a-134">手数料が評価されるかどうかの追加の基準として、支払通貨が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1499a-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="1499a-135">たとえば、ユーザーの銀行は通常 EUR 通貨で処理するため、USD 通貨で受け取った支払に対して手数料を請求することがあります。</span><span class="sxs-lookup"><span data-stu-id="1499a-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="1499a-136">手数料が割合、金額、または間隔であるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="1499a-137">**割合 / 金額フィールド**で、手数料の割合または金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="1499a-137">In the **Percentage/Amount field**, enter either percentage or amount of the fee.</span></span> <span data-ttu-id="1499a-138">[割合/金額] フィールドで割合を選択した場合、ここに入力する値は割合となります。</span><span class="sxs-lookup"><span data-stu-id="1499a-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="1499a-139">[割合/金額] フィールドで金額を選択した場合、ここに入力する値は金額となります。</span><span class="sxs-lookup"><span data-stu-id="1499a-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="1499a-140">[割合/金額] フィールドで間隔を選択した場合、階層を定義している [間隔] タブを使用します。</span><span class="sxs-lookup"><span data-stu-id="1499a-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="1499a-141">**手数料の通貨**フィールドで、手数料の通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="1499a-141">In the **Fee currency** field, select the currency of the fee.</span></span> <span data-ttu-id="1499a-142">これは、作成される手数料の通貨です。</span><span class="sxs-lookup"><span data-stu-id="1499a-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="1499a-143">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1499a-143">Click **Save**.</span></span>

