---
title: 先日付小切手の設定
description: このトピックでは、先日付小切手の仕訳入力を転記するかどうかと、どの転記仕訳帳を清算項目と仕入先支払に使用するかを指定する方法について説明します。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026208"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="2ee29-103">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="2ee29-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ee29-104">このトピックでは、先日付小切手の仕訳入力を転記するかどうかと、どの転記仕訳帳を清算項目と仕入先支払に使用するかを指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="2ee29-105">発行済小切手、受領済小切手、および源泉徴収税の精算勘定も指定できます。</span><span class="sxs-lookup"><span data-stu-id="2ee29-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="2ee29-106">将来の日付で支払を履行または受け取るために発行される先日付小切手です。</span><span class="sxs-lookup"><span data-stu-id="2ee29-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="2ee29-107">小切手が、その有効期限前に、会計帳簿に反映する必要があるかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2ee29-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="2ee29-108">この手順のロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="2ee29-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="2ee29-109">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="2ee29-110">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="2ee29-110">Set up postdated checks</span></span>
1. <span data-ttu-id="2ee29-111">[現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="2ee29-112">[先日付小切手] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee29-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="2ee29-113">[先日付小切手の有効化] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="2ee29-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="2ee29-114">[先日付小切手用の仕訳入力の転記] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="2ee29-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="2ee29-115">[発行済の小切手の清算勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="2ee29-116">[受領済みの小切手の清算勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="2ee29-117">[清算項目用の一般仕訳帳] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="2ee29-118">[この仕入先の支払仕訳帳への先日付小切手の転送] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="2ee29-119">[源泉徴収税の清算勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="2ee29-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee29-120">Click Save.</span></span>
11. <span data-ttu-id="2ee29-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2ee29-121">Close the page.</span></span>
12. <span data-ttu-id="2ee29-122">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="2ee29-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee29-123">Click New.</span></span>
14. <span data-ttu-id="2ee29-124">[支払方法] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="2ee29-125">小切手金額を精算勘定に転記されたことを示すには、[先日付小切手の清算の転記] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="2ee29-126">[勘定タイプ] フィールドで、「銀行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="2ee29-127">支払方法の相手勘定は銀行となります。</span><span class="sxs-lookup"><span data-stu-id="2ee29-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="2ee29-128">[支払勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="2ee29-129">請求書額を控除するために使用される銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ee29-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="2ee29-130">保存 をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ee29-130">Click Save.</span></span>
19. <span data-ttu-id="2ee29-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2ee29-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="2ee29-132">セッション日付が満期日付より後の場合に転記済み小切手を銀行口座に転記するには、**銀行口座に小切手が転記された支払仕訳帳を転記する際に、機能の満期日検証する** 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ee29-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="2ee29-133">この機能により、セッション日付が満期日より後の場合に、小切手が転記された仕入先または顧客に対する支払仕訳帳を転記できます。</span><span class="sxs-lookup"><span data-stu-id="2ee29-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="2ee29-134">**支払方法** (**買掛金勘定 > 支払設定 > 支払方法**) を設定する場合は、**つなぎ勘定** に入力しないでください。</span><span class="sxs-lookup"><span data-stu-id="2ee29-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="2ee29-135">この場合、相手勘定には、**支払方法** で設定された銀行口座が入力されます。</span><span class="sxs-lookup"><span data-stu-id="2ee29-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="2ee29-136">機能が有効で、セッション日付が満期日より前の場合、支払仕訳帳の転記時に次のエラー メッセージが表示されます。"相手勘定タイプが銀行の場合は、満期日以前にする必要があります"。</span><span class="sxs-lookup"><span data-stu-id="2ee29-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="2ee29-137">この機能が有効になっていない場合、セッション日付が満期日付よりも前であれば、先日付小切手を使って支払仕訳帳を転記できます。</span><span class="sxs-lookup"><span data-stu-id="2ee29-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
