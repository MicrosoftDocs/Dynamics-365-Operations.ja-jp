---
title: 先日付小切手の設定
description: このトピックでは、先日付小切手の仕訳入力を転記するかどうかと、どの転記仕訳帳を清算項目と仕入先支払に使用するかを指定する方法について説明します。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4b18ebe1388998b45e5ef38318b0ade9153f7c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "342618"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="86b0c-103">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="86b0c-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86b0c-104">このトピックでは、先日付小切手の仕訳入力を転記するかどうかと、どの転記仕訳帳を清算項目と仕入先支払に使用するかを指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="86b0c-105">発行済小切手、受領済小切手、および源泉徴収税の精算勘定も指定できます。</span><span class="sxs-lookup"><span data-stu-id="86b0c-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="86b0c-106">将来の日付で支払を履行または受け取るために発行される先日付小切手です。</span><span class="sxs-lookup"><span data-stu-id="86b0c-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="86b0c-107">小切手が、その有効期限前に、会計帳簿に反映する必要があるかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="86b0c-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="86b0c-108">この手順のロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="86b0c-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="86b0c-109">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="86b0c-110">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="86b0c-110">Set up postdated checks</span></span>
1. <span data-ttu-id="86b0c-111">[現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="86b0c-112">[先日付小切手] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="86b0c-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="86b0c-113">[先日付小切手の有効化] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="86b0c-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="86b0c-114">[先日付小切手用の仕訳入力の転記] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="86b0c-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="86b0c-115">[発行済の小切手の清算勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="86b0c-116">[受領済みの小切手の清算勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="86b0c-117">[清算項目用の一般仕訳帳] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="86b0c-118">[この仕入先の支払仕訳帳への先日付小切手の転送] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="86b0c-119">[源泉徴収税の清算勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="86b0c-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86b0c-120">Click Save.</span></span>
11. <span data-ttu-id="86b0c-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86b0c-121">Close the page.</span></span>
12. <span data-ttu-id="86b0c-122">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="86b0c-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86b0c-123">Click New.</span></span>
14. <span data-ttu-id="86b0c-124">[支払方法] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="86b0c-125">小切手金額を精算勘定に転記されたことを示すには、[先日付小切手の清算の転記] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="86b0c-126">[勘定タイプ] フィールドで、「銀行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="86b0c-127">支払方法の相手勘定は銀行となります。</span><span class="sxs-lookup"><span data-stu-id="86b0c-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="86b0c-128">[支払勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="86b0c-129">請求書額を控除するために使用される銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="86b0c-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86b0c-130">Close the page.</span></span>
19. <span data-ttu-id="86b0c-131">[売掛金管理] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="86b0c-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86b0c-132">Click New.</span></span>
21. <span data-ttu-id="86b0c-133">[支払方法] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="86b0c-134">小切手金額を精算勘定に転記されたことを示すには、[先日付小切手の清算の転記] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="86b0c-135">[勘定タイプ] フィールドで、「銀行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="86b0c-136">支払方法の相手勘定は銀行となります。</span><span class="sxs-lookup"><span data-stu-id="86b0c-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="86b0c-137">[支払勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="86b0c-138">請求書額を控除するために使用される銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="86b0c-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="86b0c-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86b0c-139">Close the page.</span></span>

