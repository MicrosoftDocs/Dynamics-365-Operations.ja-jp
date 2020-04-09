---
title: 顧客の支払方法の設定
description: このトピックでは、顧客支払の方法の作成について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b9960c3fdf0d65be19e28dbb41913a310ae7530
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140217"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="36a0d-103">顧客の支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="36a0d-103">Establish customer method of payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36a0d-104">このトピックでは、顧客支払の方法の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="36a0d-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="36a0d-106">ナビゲーション ウィンドウで、**モジュール > 売掛金勘定 > 支払設定 > 支払方法**に移動します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="36a0d-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-107">Select **New**.</span></span>
3. <span data-ttu-id="36a0d-108">**支払方法**フィールドに、支払い方法の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="36a0d-109">支払方法 ID は請求書や支払に表示されるので、支払方法の種類およびどの銀行口座が記録されるかが分かるように、それを記述します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="36a0d-110">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="36a0d-111">支払が転記されるために必要な支払ステータスを選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="36a0d-112">顧客支払を作成している時、支払ステータスはここに定義する支払ステータスと照合する時のみ、転記されます。</span><span class="sxs-lookup"><span data-stu-id="36a0d-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="36a0d-113">顧客の請求書支払を作成する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="36a0d-114">このオプションは、支払提案を実行するときにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="36a0d-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="36a0d-115">支払提案は、口座引落を行うおよび顧客の銀行口座の資金を引き出す場合に、顧客支払用に使用できます。</span><span class="sxs-lookup"><span data-stu-id="36a0d-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="36a0d-116">支払タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-116">Select the type of payment.</span></span> <span data-ttu-id="36a0d-117">支払タイプは支払検証が実行されるかを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="36a0d-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="36a0d-118">支払転記に使用する勘定タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-118">Select what account type payments will post to.</span></span> <span data-ttu-id="36a0d-119">通常、このオプションには「銀行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="36a0d-120">この支払が記録される銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="36a0d-121">銀行により使用される支払タイプを特定するために、銀行トランザクション タイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="36a0d-122">銀行トランザクション タイプは口座調整プロセスで使用され、調整を容易にすることができます。</span><span class="sxs-lookup"><span data-stu-id="36a0d-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="36a0d-123">この支払を一時的につなぎ勘定に転記するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="36a0d-124">銀行での精算を完了するために支払の浮動期間を試行する場合は、連結機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="36a0d-125">支払は、ここで定義した銀行口座に転送され、銀行で精算が完了になるまで、支払は勘定科目に一時的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="36a0d-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="36a0d-126">つなぎ転記に使用される主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="36a0d-127">これは、連結を使用する場合に、一時的に支払を転記する主勘定先です。</span><span class="sxs-lookup"><span data-stu-id="36a0d-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="36a0d-128">電子支払の設定を定義するには、**ファイル形式**タブを使用します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="36a0d-129">必須であるフィールドを定義するには、**支払管理タブ**を使用します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="36a0d-130">たとえば、この支払方法ですべての支払を預金する必要がある場合、このタブのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="36a0d-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="36a0d-131">この支払方法に使用する支払属性を定義するには、 **支払属性** タブを使用します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-131">Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="36a0d-132">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36a0d-132">Select **Save**.</span></span>

