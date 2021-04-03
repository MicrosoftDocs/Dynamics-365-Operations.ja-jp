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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617b5d99973e630cca2973227c2e54a63bd1ec4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263303"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="abca8-103">支払のリベートの処理</span><span class="sxs-lookup"><span data-stu-id="abca8-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abca8-104">この手順は、承認済および処理済の顧客リベートを貸方票に変換する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="abca8-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="abca8-105">USMF デモ データ会社でこのガイドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="abca8-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="abca8-106">このガイドの前提条件は、[マーク] の状態のリベート要求が 1 つ以上あることです。</span><span class="sxs-lookup"><span data-stu-id="abca8-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="abca8-107">USMF を使用している場合は、このガイドを開始する前に、"顧客リベートの生成と処理" ガイドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abca8-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="abca8-108">リベート要求の貸方票への変換</span><span class="sxs-lookup"><span data-stu-id="abca8-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="abca8-109">[すべての顧客] に移動します。</span><span class="sxs-lookup"><span data-stu-id="abca8-109">Go to All customers.</span></span>
2. <span data-ttu-id="abca8-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="abca8-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="abca8-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="abca8-112">[アクション] ウィンドウで、[回収] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="abca8-113">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="abca8-114">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-114">Click Functions.</span></span>
7. <span data-ttu-id="abca8-115">[リベート プログラム] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-115">Click Rebate program.</span></span>
    * <span data-ttu-id="abca8-116">[リベート] ページには、顧客リベートワークベンチで処理され、「マーク」が付いた状態になっているリベート請求が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="abca8-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="abca8-117">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-117">Click Edit.</span></span>
    * <span data-ttu-id="abca8-118">貸方票に含める要求の [マーク] フィールドにチェックマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="abca8-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="abca8-119">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-119">Click Functions.</span></span>
10. <span data-ttu-id="abca8-120">[訂正票の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-120">Click Create credit note.</span></span>
    * <span data-ttu-id="abca8-121">仕訳帳が転記されたことを通知するメッセージが表示されます (これは、[売掛金勘定パラメーター] ページで指定された売掛金管理消費仕訳帳です)。</span><span class="sxs-lookup"><span data-stu-id="abca8-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="abca8-122">これにより、実際の負債 (貸方) 金額が顧客残高に移動します。</span><span class="sxs-lookup"><span data-stu-id="abca8-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="abca8-123">つまり、顧客勘定は貸方に転記され、リベート見越計上勘定は借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="abca8-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="abca8-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="abca8-124">Close the page.</span></span>
12. <span data-ttu-id="abca8-125">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-125">Click Cancel.</span></span>
    * <span data-ttu-id="abca8-126">これによっては、ページを更新し、更新を確認できます。</span><span class="sxs-lookup"><span data-stu-id="abca8-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="abca8-127">[アクション] ウィンドウで、[回収] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="abca8-128">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="abca8-129">合計リベート金額を表す請求書参照のないマイナスの金額のトランザクションが顧客残高に追加されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="abca8-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="abca8-130">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="abca8-130">Click Cancel.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]