---
title: 勘定科目間でのトランザクションの決済
description: この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "325828"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="bcd02-103">勘定科目間でのトランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="bcd02-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bcd02-104">この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd02-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="bcd02-105">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcd02-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="bcd02-106">勘定科目間でのトランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="bcd02-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="bcd02-107">[総勘定元帳] > [定期処理タスク] > [元帳決済] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcd02-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="bcd02-108">一覧で、決済するトランザクションを見つけます。</span><span class="sxs-lookup"><span data-stu-id="bcd02-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="bcd02-109">残額は 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcd02-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="bcd02-110">[含む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bcd02-110">Click Include.</span></span>
4. <span data-ttu-id="bcd02-111">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bcd02-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="bcd02-112">元帳決済のキャンセル</span><span class="sxs-lookup"><span data-stu-id="bcd02-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="bcd02-113">[総勘定元帳] > [照会およびレポート] > [試算表] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcd02-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="bcd02-114">[パラメーター] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="bcd02-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="bcd02-115">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bcd02-115">Click Update.</span></span>
4. <span data-ttu-id="bcd02-116">一覧で、トランザクションが決済した勘定を見つけます。</span><span class="sxs-lookup"><span data-stu-id="bcd02-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="bcd02-117">[すべてのトランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bcd02-117">Click All transactions.</span></span>
6. <span data-ttu-id="bcd02-118">フィルターを使用すると、一覧内のトランザクションを簡単に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="bcd02-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="bcd02-119">[元帳決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bcd02-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="bcd02-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bcd02-120">In the list, mark the selected row.</span></span>

