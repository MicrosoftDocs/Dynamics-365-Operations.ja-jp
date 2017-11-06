--- 
title: "顧客からの先日付小切手の決済"
description: "先日付小切手は、銀行で精算された後に決済できます。"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a905166dcfbf8cee5b0e5831b47c95d443a74f8d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="73a2c-103">顧客からの先日付小切手の決済</span><span class="sxs-lookup"><span data-stu-id="73a2c-103">Settle a postdated check from a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73a2c-104">先日付小切手は、銀行で精算された後に決済できます。</span><span class="sxs-lookup"><span data-stu-id="73a2c-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="73a2c-105">この財務トランザクションによって、先日付小切手のつなぎ勘定トランザクションも精算されます。</span><span class="sxs-lookup"><span data-stu-id="73a2c-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="73a2c-106">こちらを始める前に、次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73a2c-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="73a2c-107">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="73a2c-107">Set up postdated checks</span></span>

2) <span data-ttu-id="73a2c-108">顧客の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="73a2c-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="73a2c-109">このタスク ガイドのロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="73a2c-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="73a2c-110">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="73a2c-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="73a2c-111">[貸方転記および取立] > [照会およびレポート] > [支払] > [顧客の先日付小切手] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="73a2c-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="73a2c-112">[決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73a2c-112">Click Settle.</span></span>
3. <span data-ttu-id="73a2c-113">[清算項目の決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73a2c-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="73a2c-114">小切手トランザクションの顧客 ID を決済します。</span><span class="sxs-lookup"><span data-stu-id="73a2c-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="73a2c-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="73a2c-115">Close the page.</span></span>
5. <span data-ttu-id="73a2c-116">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="73a2c-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="73a2c-117">[表示] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="73a2c-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="73a2c-118">[作成ユーザーのみ表示] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="73a2c-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="73a2c-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="73a2c-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="73a2c-120">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73a2c-120">Click Lines.</span></span>
10. <span data-ttu-id="73a2c-121">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73a2c-121">Click Voucher.</span></span>
11. <span data-ttu-id="73a2c-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="73a2c-122">Close the page.</span></span>

