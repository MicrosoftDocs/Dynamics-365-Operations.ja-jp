---
title: 仕入先の支払手数料の定義
description: 仕入先支払手数料を設定します。
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0871e0889b078c08e4bcbd86bf749bcfe39463
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837270"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="1fc89-103">仕入先の支払手数料の定義</span><span class="sxs-lookup"><span data-stu-id="1fc89-103">Define vendor payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1fc89-104">仕入先支払手数料を設定します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-104">Set up vendor payment fees.</span></span> <span data-ttu-id="1fc89-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1fc89-106">[買掛金勘定] > [支払の設定] > [支払手数料] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="1fc89-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fc89-107">Click New.</span></span>
3. <span data-ttu-id="1fc89-108">[手数料 ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="1fc89-109">手数料 ID は、「EFT_Fee」などの手数料が使用される日を定義します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="1fc89-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1fc89-111">[手数料説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="1fc89-112">手数料の算定日に関する詳細情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="1fc89-113">[請求] フィールドで、「仕入先」または「元帳」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="1fc89-114">手数料が自分の組織で処理されるとき、元帳が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="1fc89-115">手数料が仕入先で算定されるとき、仕入先が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="1fc89-116">手数料が経費で処理される主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="1fc89-117">このオプションは、元帳を [請求] オプションとして選択する場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="1fc89-118">この手数料が使用できる仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="1fc89-119">仕入先支払手数料に関しては、「仕入先出金」仕訳帳を選択します。　</span><span class="sxs-lookup"><span data-stu-id="1fc89-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="1fc89-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fc89-120">Click Save.</span></span>
10. <span data-ttu-id="1fc89-121">[支払手数料の設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fc89-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="1fc89-122">手数料が選択した仕訳帳の既定値としていつ設定されるかを定義する [支払手数料の設定] に進みます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="1fc89-123">「テーブル」、「グループ」または「全て」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="1fc89-124">「テーブル」は一つの銀行口座を選択するために使用され、「グループ」は銀行グループを選択するために使用され、「すべて」はすべての銀行口座にこの費用の設定を適用するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="1fc89-125">銀行グループまたは銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="1fc89-126">「グループ」を選択した場合、ルックアップには銀行グループが表示され、「テーブル」を選択した場合、銀行口座が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="1fc89-127">支払手数料が評価される時に使用する支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="1fc89-128">選択した支払方法の支払詳細を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="1fc89-129">支払仕様は、電子資金振替に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="1fc89-130">手数料が割合、金額、または間隔であるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="1fc89-131">手数料の金額の割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="1fc89-132">手数料が割合である場合、割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="1fc89-133">手数料が金額である場合、金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="1fc89-134">手数料が間隔である場合、階層化された手数料を定義する [間隔] タブを使用します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="1fc89-135">[手数料の通貨] フィールドで、算定される手数料の通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fc89-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="1fc89-136">この通貨はこの手数料に適用されます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-136">This currency is for the fee.</span></span> <span data-ttu-id="1fc89-137">支払通貨は、支払通貨に基づいて手数料に関するルールをいつ評価するかを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1fc89-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="1fc89-138">たとえば、支払が EUR で行われた場合、銀行は手数料を請求しますが、その他の支払手数料はすべて算定されません。</span><span class="sxs-lookup"><span data-stu-id="1fc89-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="1fc89-139">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fc89-139">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]