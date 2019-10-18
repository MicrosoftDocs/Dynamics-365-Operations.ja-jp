---
title: 仕入先の先日付小切手の決済
description: 銀行が期限切れの小切手をクリアして、その小切手トランザクションを精算してしまったときに、仕入先へ発行した先日付小切手を決済します。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d935ec24d97ca76a088cbe41d57c12c6e8a6689
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188053"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="d47ac-103">仕入先の先日付小切手の決済</span><span class="sxs-lookup"><span data-stu-id="d47ac-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d47ac-104">銀行が期限切れの小切手をクリアして、その小切手トランザクションを精算してしまったときに、仕入先へ発行した先日付小切手を決済します。</span><span class="sxs-lookup"><span data-stu-id="d47ac-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="d47ac-105">これを始める前に、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="d47ac-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="d47ac-106">先日付小切手の設定</span><span class="sxs-lookup"><span data-stu-id="d47ac-106">Set up postdated checks</span></span>

2) <span data-ttu-id="d47ac-107">仕入先の先日付小切手の登録および転記</span><span class="sxs-lookup"><span data-stu-id="d47ac-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="d47ac-108">この手順のロールは会計登録者です。</span><span class="sxs-lookup"><span data-stu-id="d47ac-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="d47ac-109">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="d47ac-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="d47ac-110">[買掛金勘定] > [支払] > [仕入先の先日付小切手] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="d47ac-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="d47ac-111">[決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d47ac-111">Click Settle.</span></span>
3. <span data-ttu-id="d47ac-112">[清算項目の決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d47ac-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="d47ac-113">小切手トランザクションのための仕入先を決済します。</span><span class="sxs-lookup"><span data-stu-id="d47ac-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="d47ac-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d47ac-114">Close the page.</span></span>
5. <span data-ttu-id="d47ac-115">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d47ac-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="d47ac-116">[表示] フィールドで「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d47ac-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="d47ac-117">[作成ユーザーのみ表示] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="d47ac-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="d47ac-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d47ac-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d47ac-119">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d47ac-119">Click Lines.</span></span>
10. <span data-ttu-id="d47ac-120">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d47ac-120">Click Voucher.</span></span>
11. <span data-ttu-id="d47ac-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d47ac-121">Close the page.</span></span>

