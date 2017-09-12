--- 
title: "仕入先の支払条件の定義"
description: "仕入先請求書の支払条件を設定します。"
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a00ca73b1bc301960132a86846749d12c39ed3f7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="23d97-103">仕入先の支払条件の定義</span><span class="sxs-lookup"><span data-stu-id="23d97-103">Define vendor payment terms</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23d97-104">仕入先請求書の支払条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="23d97-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="23d97-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="23d97-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="23d97-106">[買掛金勘定] > [支払設定] > [支払条件] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="23d97-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="23d97-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23d97-107">Click New.</span></span>
    * <span data-ttu-id="23d97-108">支払条件のページは期日を計算する方法を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="23d97-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="23d97-109">このページは現金割引日を計算する方法を定義するために使用されてはいません。</span><span class="sxs-lookup"><span data-stu-id="23d97-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="23d97-110">[支払条件] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="23d97-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23d97-112">[日] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="23d97-113">ここで入力された数値は、期日に、または支払方法で指定した期間の終了時に追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="23d97-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="23d97-114">たとえば、「正味」を選択する場合、数値は期日に追加されます。</span><span class="sxs-lookup"><span data-stu-id="23d97-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="23d97-115">「現在の月」を選択する場合、期日を計算するために、数値は現在の月の最終日に追加されます。</span><span class="sxs-lookup"><span data-stu-id="23d97-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="23d97-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23d97-116">Click Save.</span></span>
7. <span data-ttu-id="23d97-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="23d97-117">Close the page.</span></span>
8. <span data-ttu-id="23d97-118">[買掛金勘定] > [支払設定] > [現金割引] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="23d97-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="23d97-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23d97-119">Click New.</span></span>
10. <span data-ttu-id="23d97-120">[現金割引] フィールドに ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="23d97-121">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="23d97-122">仕入先が階層化された割引を提供すると、現在の割引の有効期限が経過した後に次の現金割引を選択します。</span><span class="sxs-lookup"><span data-stu-id="23d97-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="23d97-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="23d97-123">Close the page.</span></span>
14. <span data-ttu-id="23d97-124">[日] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="23d97-125">[日] フィールドに入力された数量は、[正味/現在] フィールドで選択したオプションに基づいて現金割引日を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="23d97-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="23d97-126">正味を選択した場合、数量が請求日に追加され、現金割引日が特定されます。</span><span class="sxs-lookup"><span data-stu-id="23d97-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="23d97-127">「現在の月」を選択した場合、数量が当月末に追加され、現金割引日が特定されます。</span><span class="sxs-lookup"><span data-stu-id="23d97-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="23d97-128">[割引] フィールドに、現金割引率を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="23d97-129">現金割引が転記される顧客請求書用の主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="23d97-130">現金割引が転記される仕入先請求書用の主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="23d97-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="23d97-131">「割引の相手勘定」に「仕入先割引の主勘定を使用」が設定されている場合、主勘定が使用されるようになります。</span><span class="sxs-lookup"><span data-stu-id="23d97-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="23d97-132">オプションで「請求明細行の勘定」を選択した場合、現金割引は、請求書明細行の資産/経費用勘定に転記されるようになります。</span><span class="sxs-lookup"><span data-stu-id="23d97-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="23d97-133">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23d97-133">Click Save.</span></span>


