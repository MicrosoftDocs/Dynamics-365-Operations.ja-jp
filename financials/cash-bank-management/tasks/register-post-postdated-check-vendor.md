--- 
title: "仕入先の先日付小切手の登録および転記"
description: "仕訳伝票を使用して、ベンダーに小切手を発行する前に先日付小切手の詳細を登録できます。"
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8689421d3281f93af9298f777f92c5c3b2c1c86c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="270e6-103">仕入先の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="270e6-103">Register and post a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="270e6-104">仕訳伝票を使用して、ベンダーに小切手を発行する前に先日付小切手の詳細を登録できます。</span><span class="sxs-lookup"><span data-stu-id="270e6-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="270e6-105">先日付小切手を転記して財務トランザクションを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="270e6-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="270e6-106">仕入先からの先日付小切手を登録および転記する前に、次のタスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="270e6-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="270e6-107">[現金および銀行管理] ページで、先日付小切手を設定します。</span><span class="sxs-lookup"><span data-stu-id="270e6-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="270e6-108">このタスク ガイドのロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="270e6-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="270e6-109">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="270e6-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="270e6-110">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="270e6-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="270e6-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="270e6-111">Click New.</span></span>
3. <span data-ttu-id="270e6-112">[名前] フィールドに、「VendaPay」と入力します。</span><span class="sxs-lookup"><span data-stu-id="270e6-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="270e6-113">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="270e6-113">Click Lines.</span></span>
5. <span data-ttu-id="270e6-114">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="270e6-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="270e6-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="270e6-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="270e6-116">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="270e6-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="270e6-117">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="270e6-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="270e6-118">先日付小切手に対する支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="270e6-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="270e6-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="270e6-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="270e6-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="270e6-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="270e6-121">[先日付小切手] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="270e6-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="270e6-122">[小切手番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="270e6-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="270e6-123">先日付小切手番号を入力または変更します。</span><span class="sxs-lookup"><span data-stu-id="270e6-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="270e6-124">[発行銀行名] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="270e6-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="270e6-125">発行銀行の銀行詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="270e6-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="270e6-126">[一覧] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="270e6-126">Click the List tab.</span></span>
15. <span data-ttu-id="270e6-127">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="270e6-127">Click Post.</span></span>
16. <span data-ttu-id="270e6-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="270e6-128">Close the page.</span></span>
17. <span data-ttu-id="270e6-129">[先日付小切手] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="270e6-129">Click the Postdated checks tab.</span></span>


