---
title: 顧客の先日付小切手の登録および転記
description: 顧客から受け取った先日付小切手の詳細を登録できます。
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 131e4f364c62d03b95fb4b77f472828b9483d5e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566090"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="0d8fe-103">顧客の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="0d8fe-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d8fe-104">顧客から受け取った先日付小切手の詳細を登録できます。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="0d8fe-105">先日付小切手を転記して財務トランザクションを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="0d8fe-106">顧客から受け取った先日付小切手を登録し転記する前に、次のタスクを完了します。:   • [現金および銀行管理] ページで、先日付小切手を設定します。 • 先日小切手用の支払方法を設定します。   この手順のロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="0d8fe-107">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="0d8fe-108">[売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="0d8fe-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-109">Click New.</span></span>
3. <span data-ttu-id="0d8fe-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0d8fe-111">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-111">Click Lines.</span></span>
5. <span data-ttu-id="0d8fe-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0d8fe-113">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="0d8fe-114">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="0d8fe-115">先日付小切手に指定された金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="0d8fe-116">[支払] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="0d8fe-117">[支払方法] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="0d8fe-118">先日付小切手に対する支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="0d8fe-119">[先日付小切手] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="0d8fe-120">[振出日] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="0d8fe-121">先日付小切手が支払期限になる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="0d8fe-122">[発行銀行支店] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="0d8fe-123">先日付小切手の銀行詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="0d8fe-124">[小切手番号] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="0d8fe-125">[発行銀行名] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="0d8fe-126">先日付小切手の銀行詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="0d8fe-127">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-127">Click Post.</span></span>
16. <span data-ttu-id="0d8fe-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0d8fe-128">Close the page.</span></span>

