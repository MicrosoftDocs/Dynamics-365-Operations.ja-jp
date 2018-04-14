--- 
title: "仕入先の先日付小切手の登録および転記"
description: "仕訳伝票を使用して、ベンダーに小切手を発行する前に先日付小切手の詳細を登録できます。"
author: kweekley
manager: AnnBe
ms.date: 10/31/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cd00227ed6d288a4b2041630bc7a604ac94d3c70
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="9db53-103">仕入先の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="9db53-103">Register and post a postdated check for a vendor</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9db53-104">仕訳伝票を使用して、ベンダーに小切手を発行する前に先日付小切手の詳細を登録できます。</span><span class="sxs-lookup"><span data-stu-id="9db53-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="9db53-105">先日付小切手を転記して財務トランザクションを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="9db53-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="9db53-106">仕入先からの先日付小切手を登録および転記する前に、次のタスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="9db53-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="9db53-107">[現金および銀行管理] ページで、先日付小切手を設定します。</span><span class="sxs-lookup"><span data-stu-id="9db53-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="9db53-108">このタスク ガイドのロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="9db53-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="9db53-109">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="9db53-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9db53-110">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9db53-110">Go to Accounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="9db53-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9db53-111">Click New.</span></span>
3. <span data-ttu-id="9db53-112">[名前] フィールドに、「VendaPay」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9db53-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="9db53-113">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9db53-113">Click Lines.</span></span>
5. <span data-ttu-id="9db53-114">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9db53-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="9db53-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9db53-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="9db53-116">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9db53-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="9db53-117">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9db53-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9db53-118">先日付小切手に対する支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db53-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="9db53-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9db53-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9db53-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9db53-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9db53-121">[先日付小切手] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9db53-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="9db53-122">[小切手番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9db53-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="9db53-123">先日付小切手番号を入力または変更します。</span><span class="sxs-lookup"><span data-stu-id="9db53-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="9db53-124">[発行銀行名] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9db53-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="9db53-125">発行銀行の銀行詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="9db53-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="9db53-126">[一覧] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9db53-126">Click the List tab.</span></span>
15. <span data-ttu-id="9db53-127">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9db53-127">Click Post.</span></span>
16. <span data-ttu-id="9db53-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9db53-128">Close the page.</span></span>
17. <span data-ttu-id="9db53-129">[先日付小切手] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9db53-129">Click the Postdated checks tab.</span></span>


