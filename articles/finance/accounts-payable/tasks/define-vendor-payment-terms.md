---
title: 仕入先の支払条件の定義
description: このトピックでは、仕入先請求書の支払条件の設定方法について説明します。
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e6778f61a9367399e4b71d5b2bb2459c09ba508
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445025"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="792ec-103">仕入先の支払条件の定義</span><span class="sxs-lookup"><span data-stu-id="792ec-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="792ec-104">このトピックでは、仕入先請求書の支払条件の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="792ec-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="792ec-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="792ec-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="792ec-106">**ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > 支払の設定 > 支払条件** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="792ec-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="792ec-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="792ec-107">Select **New**.</span></span> <span data-ttu-id="792ec-108">支払条件のページは期日を計算する方法を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="792ec-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="792ec-109">このページは現金割引日を計算する方法を定義するために使用されてはいません。</span><span class="sxs-lookup"><span data-stu-id="792ec-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="792ec-110">**支払条件** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="792ec-111">**説明フィールド** で、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="792ec-112">**日** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="792ec-113">ここで入力された数値は、期日に、または支払方法で指定した期間の終了時に追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="792ec-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="792ec-114">たとえば、**正味** を選択する場合、数値は期日に追加されます。</span><span class="sxs-lookup"><span data-stu-id="792ec-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="792ec-115">**現在の月** を選択する場合、期日を計算するために、数値は現在の月の最終日に追加されます。</span><span class="sxs-lookup"><span data-stu-id="792ec-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="792ec-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="792ec-116">Select **Save**.</span></span>
7. <span data-ttu-id="792ec-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="792ec-117">Close the page.</span></span>
8. <span data-ttu-id="792ec-118">**買掛金勘定 > 支払設定 > 現金割引** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="792ec-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="792ec-119">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="792ec-119">Select **New**.</span></span>
10. <span data-ttu-id="792ec-120">**現金割引** フィールドに ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="792ec-121">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="792ec-122">仕入先が階層化された割引を提供すると、現在の割引の有効期限が経過した後に次の現金割引を選択します。</span><span class="sxs-lookup"><span data-stu-id="792ec-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="792ec-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="792ec-123">Close the page.</span></span>
14. <span data-ttu-id="792ec-124">**日** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="792ec-125">**日** フィールドに入力された数量は、**正味/現在** フィールドで選択したオプションに基づいて現金割引日を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="792ec-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="792ec-126">**正味** を選択した場合、数量が請求日に追加され、現金割引日が特定されます。</span><span class="sxs-lookup"><span data-stu-id="792ec-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="792ec-127">**現在の月** を選択した場合、数量が当月末に追加され、現金割引日が特定されます。</span><span class="sxs-lookup"><span data-stu-id="792ec-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="792ec-128">**割引** フィールドに、現金割引率を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="792ec-129">顧客請求書に対して現金割引が転記される主勘定を入力してから、仕入先請求書に対して現金割引を転記する主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="792ec-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="792ec-130">**割引の相手勘定** が **仕入先割引の主勘定を使用** に設定されている場合、主勘定が使用されるようになります。</span><span class="sxs-lookup"><span data-stu-id="792ec-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="792ec-131">オプションで **請求明細行の勘定** を選択した場合、現金割引は、請求書明細行の資産/経費用勘定に転記されるようになります。</span><span class="sxs-lookup"><span data-stu-id="792ec-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="792ec-132">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="792ec-132">Select **Save**.</span></span>

