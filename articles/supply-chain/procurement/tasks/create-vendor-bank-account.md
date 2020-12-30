---
title: 仕入先銀行口座の作成
description: この手順では、仕入先用の銀行口座の作成方法を説明します。
author: mkirknel
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8092ab7f960fd36515afb8448dfe1e262197595
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431829"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="7aa29-103">仕入先銀行口座の作成</span><span class="sxs-lookup"><span data-stu-id="7aa29-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7aa29-104">この手順では、仕入先用の銀行口座の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="7aa29-105">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7aa29-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="7aa29-106">**ナビゲーション ウィンドウ > モジュール > 調達 > 仕入先 > すべての仕入先** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="7aa29-107">銀行口座を作成する対象の仕入先を選択し、**仕入先 ID** フィールドのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7aa29-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="7aa29-108">**アクション ウィンドウ** で、 **仕入先** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7aa29-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="7aa29-109">**銀行口座** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7aa29-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="7aa29-110">**アクション ペイン** で **新規作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7aa29-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="7aa29-111">**銀行口座** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="7aa29-112">この ID を使用して仕入先レコードの銀行口座を識別します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="7aa29-113">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="7aa29-114">**銀行グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="7aa29-115">**ルーティン番号タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="7aa29-116">これは国際送金に使用されるルーティング番号のタイプです。</span><span class="sxs-lookup"><span data-stu-id="7aa29-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="7aa29-117">**銀行口座番号** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="7aa29-118">**SWIFT コード** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="7aa29-119">**IBAN** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="7aa29-120">IBAN 番号は正しい形式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aa29-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="7aa29-121">たとえば「DE89370400440532013000」のような形式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7aa29-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="7aa29-122">銀行口座の状態は、有効日が来て、有効期限を超過していない場合は [有効] です。</span><span class="sxs-lookup"><span data-stu-id="7aa29-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="7aa29-123">有効日と有効期限フィールドの両方が空白の場合でも有効です。</span><span class="sxs-lookup"><span data-stu-id="7aa29-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="7aa29-124">[有効日] および [有効期限] の両フィールドの日付が将来の日付である場合、電子支払は使用できません。</span><span class="sxs-lookup"><span data-stu-id="7aa29-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="7aa29-125">他の支払タイプは使用可能であり、銀行口座は有効です。</span><span class="sxs-lookup"><span data-stu-id="7aa29-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="7aa29-126">**設定** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="7aa29-127">**テキスト コード** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="7aa29-128">このフィールドでは、受取人の口座取引明細書に表示されるコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="7aa29-129">**銀行へのメッセージ** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="7aa29-130">**為替参照** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="7aa29-131">これは、先物為替レートまたは固定期間為替レートの参照番号です。</span><span class="sxs-lookup"><span data-stu-id="7aa29-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="7aa29-132">**通貨** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="7aa29-133">事前通知が発行される場合、このセクションではステータス (保留中または承認済) の概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="7aa29-134">**住所** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="7aa29-135">**事前通知** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="7aa29-136">**連絡先情報** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="7aa29-137">**電話** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="7aa29-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7aa29-138">Close the page.</span></span>
23. <span data-ttu-id="7aa29-139">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7aa29-139">Click **Edit**.</span></span>
24. <span data-ttu-id="7aa29-140">**支払** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="7aa29-141">**銀行口座** フィールドにて、作成した口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa29-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="7aa29-142">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7aa29-142">Click **Save**.</span></span> <span data-ttu-id="7aa29-143">指定するか、ここに追加する場合、住所は銀行グループから継承される場合があります。</span><span class="sxs-lookup"><span data-stu-id="7aa29-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

