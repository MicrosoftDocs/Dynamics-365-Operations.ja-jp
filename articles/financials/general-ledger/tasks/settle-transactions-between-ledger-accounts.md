--- 
title: "勘定科目間でのトランザクションの決済"
description: "この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。"
author: aprilolson
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
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97a28069f8d560c98099a667852c932ba7658996
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="c9b66-103">勘定科目間でのトランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="c9b66-103">Settle transactions between ledger accounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9b66-104">この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c9b66-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="c9b66-105">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="c9b66-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="c9b66-106">勘定科目間でのトランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="c9b66-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="c9b66-107">[総勘定元帳] > [定期処理タスク] > [元帳決済] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9b66-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="c9b66-108">一覧で、決済するトランザクションを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c9b66-108">In the list, find the transaction that you want to settle.</span></span>
    * <span data-ttu-id="c9b66-109">残額は 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9b66-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="c9b66-110">[含む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9b66-110">Click Include.</span></span>
4. <span data-ttu-id="c9b66-111">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9b66-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="c9b66-112">元帳決済のキャンセル</span><span class="sxs-lookup"><span data-stu-id="c9b66-112">Cancel a ledger settlement</span></span>
1. <span data-ttu-id="c9b66-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c9b66-113">Close the page.</span></span>
2. <span data-ttu-id="c9b66-114">[総勘定元帳] > [照会およびレポート] > [試算表] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9b66-114">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
3. <span data-ttu-id="c9b66-115">[パラメーター] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="c9b66-115">Click Parameters to open the drop dialog.</span></span>
4. <span data-ttu-id="c9b66-116">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9b66-116">Click Update.</span></span>
5. <span data-ttu-id="c9b66-117">一覧で、トランザクションが決済した勘定を見つけます。</span><span class="sxs-lookup"><span data-stu-id="c9b66-117">In the list, find the account that has the settled transaction.</span></span>
6. <span data-ttu-id="c9b66-118">[すべてのトランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9b66-118">Click All transactions.</span></span>
7. <span data-ttu-id="c9b66-119">フィルターを使用すると、一覧内のトランザクションを簡単に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="c9b66-119">Use a filter to easily find the transaction in the list.</span></span>
8. <span data-ttu-id="c9b66-120">[元帳決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9b66-120">Click Ledger settlements.</span></span>
9. <span data-ttu-id="c9b66-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c9b66-121">In the list, mark the selected row.</span></span>


