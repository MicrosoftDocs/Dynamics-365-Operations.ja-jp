---
title: 顧客の設定と ISO20022 口座引落用の顧客銀行口座の設定
description: このタスクでは、顧客の銀行口座の設定、および ISO20022 口座引落などの顧客支払ファイルを生成するために必要な顧客口座引落の委任状の設定について説明します。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a8a3eff1f882d0d9b3d4943e352a8f3d1a6ae4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185730"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="bc001-103">顧客の設定と ISO20022 口座引落用の顧客銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="bc001-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc001-104">このタスクでは、顧客の銀行口座の設定、および ISO20022 口座引落などの顧客支払ファイルを生成するために必要な顧客口座引落の委任状の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc001-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="bc001-105">設定された顧客支払形式によって、顧客または顧客の銀行口座について、この手順に含まれていない追加情報が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bc001-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="bc001-106">このタスクは、ドイツ内に通常の住所がある法人とデモ データの会社 DEMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="bc001-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="bc001-107">これは、5 つのうち 4 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="bc001-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="bc001-108">顧客銀行口座のの設定</span><span class="sxs-lookup"><span data-stu-id="bc001-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="bc001-109">[売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc001-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="bc001-110">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="bc001-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bc001-111">たとえば、値「DE-010」で [口座] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="bc001-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="bc001-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bc001-113">[アクション] ウィンドウで、[顧客] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="bc001-114">[銀行口座] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="bc001-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-115">Click New.</span></span>
7. <span data-ttu-id="bc001-116">[銀行口座] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="bc001-117">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="bc001-118">たとえば、「EUR bank」を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="bc001-119">[銀行グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bc001-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="bc001-120">[IBAN] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="bc001-121">たとえば、「DE36200400000628808808」を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="bc001-122">[SWIFT コード] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="bc001-123">たとえば、「COBADEFFXXX」を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="bc001-124">SWIFT \ BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bc001-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="bc001-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-125">Click Save.</span></span>
13. <span data-ttu-id="bc001-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bc001-126">Close the page.</span></span>
14. <span data-ttu-id="bc001-127">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-127">Click Edit.</span></span>
15. <span data-ttu-id="bc001-128">[支払の既定値] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="bc001-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="bc001-129">[銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bc001-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="bc001-130">口座引落の委任状の追加</span><span class="sxs-lookup"><span data-stu-id="bc001-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="bc001-131">[口座引落委任状] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="bc001-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="bc001-132">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-132">Click Add.</span></span>
3. <span data-ttu-id="bc001-133">[債権者の銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bc001-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="bc001-134">たとえば、[DEMF OPER] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc001-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="bc001-135">[署名日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="bc001-136">「はい」をクリックして、日付の更新を確認します。</span><span class="sxs-lookup"><span data-stu-id="bc001-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="bc001-137">[署名場所] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bc001-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="bc001-138">[予定されている支払回数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc001-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="bc001-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-139">Click OK.</span></span>
9. <span data-ttu-id="bc001-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc001-140">Click Save.</span></span>
