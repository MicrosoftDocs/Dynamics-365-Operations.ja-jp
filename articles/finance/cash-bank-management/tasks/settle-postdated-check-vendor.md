---
title: 仕入先の先日付小切手の決済
description: 銀行が期限切れの小切手をクリアして、その小切手トランザクションを精算してしまったときに、仕入先へ発行した先日付小切手を決済します。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89acad0c9421960ff4d07ed8eec798b9068424d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834574"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="45a8e-103">仕入先の先日付小切手の決済</span><span class="sxs-lookup"><span data-stu-id="45a8e-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45a8e-104">銀行が期限切れの小切手をクリアして、その小切手トランザクションを精算してしまったときに、仕入先へ発行した先日付小切手を決済します。</span><span class="sxs-lookup"><span data-stu-id="45a8e-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="45a8e-105">これを始める前に、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="45a8e-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="45a8e-106">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="45a8e-106">Set up postdated checks</span></span>

2) <span data-ttu-id="45a8e-107">仕入先の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="45a8e-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="45a8e-108">この手順のロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="45a8e-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="45a8e-109">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="45a8e-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="45a8e-110">[買掛金勘定] > [支払] > [仕入先の先日付小切手] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="45a8e-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="45a8e-111">[決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a8e-111">Click Settle.</span></span>
3. <span data-ttu-id="45a8e-112">[清算項目の決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a8e-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="45a8e-113">小切手トランザクションのための仕入先を決済します。</span><span class="sxs-lookup"><span data-stu-id="45a8e-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="45a8e-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="45a8e-114">Close the page.</span></span>
5. <span data-ttu-id="45a8e-115">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45a8e-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="45a8e-116">[表示] フィールドで「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="45a8e-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="45a8e-117">[作成ユーザーのみ表示] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="45a8e-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="45a8e-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="45a8e-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="45a8e-119">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a8e-119">Click Lines.</span></span>
10. <span data-ttu-id="45a8e-120">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45a8e-120">Click Voucher.</span></span>
11. <span data-ttu-id="45a8e-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="45a8e-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]