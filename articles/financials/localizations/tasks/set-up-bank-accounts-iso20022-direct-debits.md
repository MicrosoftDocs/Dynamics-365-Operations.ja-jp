--- 
title: "顧客の設定と ISO20022 口座引落用の顧客銀行口座の設定"
description: "このタスクでは、顧客の銀行口座の設定、および ISO20022 口座引落などの顧客支払ファイルを生成するために必要な顧客口座引落の委任状の設定について説明します。"
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e7d7d79b1d496223b027d800beca105ecaa0bd4c
ms.contentlocale: ja-jp
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="40e7b-103">顧客の設定と ISO20022 口座引落用の顧客銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="40e7b-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40e7b-104">このタスクでは、顧客の銀行口座の設定、および ISO20022 口座引落などの顧客支払ファイルを生成するために必要な顧客口座引落の委任状の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="40e7b-105">設定された顧客支払形式によって、顧客または顧客の銀行口座について、この手順に含まれていない追加情報が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="40e7b-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="40e7b-106">このタスクは、ドイツ内に通常の住所がある法人とデモ データの会社 DEMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="40e7b-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="40e7b-107">これは、5 つのうち 4 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="40e7b-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="40e7b-108">顧客銀行口座のの設定</span><span class="sxs-lookup"><span data-stu-id="40e7b-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="40e7b-109">[売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="40e7b-110">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="40e7b-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="40e7b-111">たとえば、値「DE-010」で [口座] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="40e7b-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="40e7b-113">[アクション] ウィンドウで、[顧客] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="40e7b-114">[銀行口座] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="40e7b-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-115">Click New.</span></span>
7. <span data-ttu-id="40e7b-116">[銀行口座] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="40e7b-117">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="40e7b-118">たとえば、「EUR bank」を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="40e7b-119">[銀行グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="40e7b-120">[IBAN] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="40e7b-121">たとえば、「DE36200400000628808808」を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="40e7b-122">[SWIFT コード] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="40e7b-123">たとえば、「COBADEFFXXX」を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="40e7b-124">SWIFT \ BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="40e7b-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="40e7b-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-125">Click Save.</span></span>
13. <span data-ttu-id="40e7b-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="40e7b-126">Close the page.</span></span>
14. <span data-ttu-id="40e7b-127">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-127">Click Edit.</span></span>
15. <span data-ttu-id="40e7b-128">[支払の既定値] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="40e7b-129">[銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="40e7b-130">口座引落の委任状の追加</span><span class="sxs-lookup"><span data-stu-id="40e7b-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="40e7b-131">[口座引落委任状] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="40e7b-132">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-132">Click Add.</span></span>
3. <span data-ttu-id="40e7b-133">[債権者の銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="40e7b-134">たとえば、[DEMF OPER] を選択します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="40e7b-135">[署名日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="40e7b-136">「はい」をクリックして、日付の更新を確認します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="40e7b-137">[署名場所] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="40e7b-138">[予定されている支払回数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="40e7b-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="40e7b-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-139">Click OK.</span></span>
9. <span data-ttu-id="40e7b-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40e7b-140">Click Save.</span></span>


