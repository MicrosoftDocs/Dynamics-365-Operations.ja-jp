---
title: 支払のリベートの処理
description: この手順は、承認済および処理済の顧客リベートを貸方票に変換する方法を示します。
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2e9af7167e4a4209b708d00493b8866f6d5f7e0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209930"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="3b098-103">支払のリベートの処理</span><span class="sxs-lookup"><span data-stu-id="3b098-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b098-104">この手順は、承認済および処理済の顧客リベートを貸方票に変換する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3b098-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="3b098-105">USMF デモ データ会社でこのガイドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b098-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="3b098-106">このガイドの前提条件は、[マーク] の状態のリベート要求が 1 つ以上あることです。</span><span class="sxs-lookup"><span data-stu-id="3b098-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="3b098-107">USMF を使用している場合は、このガイドを開始する前に、"顧客リベートの生成と処理" ガイドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b098-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="3b098-108">リベート要求の貸方票への変換</span><span class="sxs-lookup"><span data-stu-id="3b098-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="3b098-109">[すべての顧客] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b098-109">Go to All customers.</span></span>
2. <span data-ttu-id="3b098-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="3b098-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3b098-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3b098-112">[アクション] ウィンドウで、[回収] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="3b098-113">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="3b098-114">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-114">Click Functions.</span></span>
7. <span data-ttu-id="3b098-115">[リベート プログラム] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-115">Click Rebate program.</span></span>
    * <span data-ttu-id="3b098-116">[リベート] ページには、顧客リベートワークベンチで処理され、「マーク」が付いた状態になっているリベート請求が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b098-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="3b098-117">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-117">Click Edit.</span></span>
    * <span data-ttu-id="3b098-118">貸方票に含める要求の [マーク] フィールドにチェックマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="3b098-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="3b098-119">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-119">Click Functions.</span></span>
10. <span data-ttu-id="3b098-120">[訂正票の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-120">Click Create credit note.</span></span>
    * <span data-ttu-id="3b098-121">仕訳帳が転記されたことを通知するメッセージが表示されます (これは、[売掛金勘定パラメーター] ページで指定された売掛金管理消費仕訳帳です)。</span><span class="sxs-lookup"><span data-stu-id="3b098-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="3b098-122">これにより、実際の負債 (貸方) 金額が顧客残高に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b098-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="3b098-123">つまり、顧客勘定は貸方に転記され、リベート見越計上勘定は借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="3b098-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="3b098-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b098-124">Close the page.</span></span>
12. <span data-ttu-id="3b098-125">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-125">Click Cancel.</span></span>
    * <span data-ttu-id="3b098-126">これによっては、ページを更新し、更新を確認できます。</span><span class="sxs-lookup"><span data-stu-id="3b098-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="3b098-127">[アクション] ウィンドウで、[回収] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="3b098-128">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="3b098-129">合計リベート金額を表す請求書参照のないマイナスの金額のトランザクションが顧客残高に追加されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3b098-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="3b098-130">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b098-130">Click Cancel.</span></span>

