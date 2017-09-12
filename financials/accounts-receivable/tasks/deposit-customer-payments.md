--- 
title: "顧客支払の預金"
description: "顧客支払を預金します。"
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dbf21bd5df70cd80e4fe3f2f5d699aa82b62423b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="b0b0c-103">顧客支払の預金</span><span class="sxs-lookup"><span data-stu-id="b0b0c-103">Deposit customer payments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0b0c-104">顧客支払を預金します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-104">Deposit customer payments.</span></span> <span data-ttu-id="b0b0c-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b0b0c-106">[売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b0b0c-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-107">Click New.</span></span>
3. <span data-ttu-id="b0b0c-108">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b0b0c-109">支払仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="b0b0c-110">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-110">Click Lines.</span></span>
6. <span data-ttu-id="b0b0c-111">[口座] フィールドで、支払を記録している顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="b0b0c-112">[貸方] フィールドに支払金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="b0b0c-113">金額を空白にし、支払済み請求書を選択してシステムに計算させることができます。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="b0b0c-114">[支払参照] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="b0b0c-115">支払の参照は、入力する支払の小切手番号にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="b0b0c-116">預金伝票に支払を含めるためには、支払参照が必要となります。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="b0b0c-117">[預金伝票の使用] ボックスをマークします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="b0b0c-118">支払額を預金残高に含める場合、この設定を「はい」に変更します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="b0b0c-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-119">Click New.</span></span>
11. <span data-ttu-id="b0b0c-120">[口座] フィールドで、次回に支払う顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="b0b0c-121">[貸方] フィールドに支払金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="b0b0c-122">[支払参照] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="b0b0c-123">[預金伝票の使用] ボックスをマークします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="b0b0c-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-124">Click Post.</span></span>
    * <span data-ttu-id="b0b0c-125">預金伝票を生成する前に、支払は転記されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="b0b0c-126">これは、預金伝票が生成された後に支払が変更しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="b0b0c-127">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-127">Click Functions.</span></span>
17. <span data-ttu-id="b0b0c-128">[預金伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="b0b0c-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-129">Click OK.</span></span>
    * <span data-ttu-id="b0b0c-130">最初のページは預金伝票を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="b0b0c-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-131">Click OK.</span></span>
    * <span data-ttu-id="b0b0c-132">2 番目の手順は、預金伝票を印刷することですが、この手順は必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="b0b0c-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


