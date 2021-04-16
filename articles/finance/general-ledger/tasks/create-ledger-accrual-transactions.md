---
title: 元帳発生トランザクションの作成
description: このタスク ガイドでは、発生主義スキーマに基づく元帳計上トランザクションの生成について説明します。
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6eb0d20c530e25c3ec5c1e013859b9d7e776b30f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832829"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="70ee9-103">元帳発生トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="70ee9-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70ee9-104">このタスク ガイドでは、発生主義スキーマに基づく元帳計上トランザクションの生成について説明します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="70ee9-105">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="70ee9-106">一覧で、目的の仕訳帳を検索し選択するか、新しい仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="70ee9-107">[仕訳帳バッチ番号] フィールドをクリックしてリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="70ee9-108">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="70ee9-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="70ee9-109">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="70ee9-110">この例では、保険の経費を定義します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="70ee9-111">これは定期的経費の金額になります。</span><span class="sxs-lookup"><span data-stu-id="70ee9-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="70ee9-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="70ee9-113">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="70ee9-114">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="70ee9-115">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70ee9-115">Click Functions.</span></span>
10. <span data-ttu-id="70ee9-116">[元帳計上] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70ee9-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="70ee9-117">[発生主義スキーマ ID] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="70ee9-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="70ee9-118">一覧で、適用する発生主義スキーマを検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="70ee9-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="70ee9-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="70ee9-120">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="70ee9-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="70ee9-121">[トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70ee9-121">Click Transactions.</span></span>
16. <span data-ttu-id="70ee9-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="70ee9-122">Close the page.</span></span>
17. <span data-ttu-id="70ee9-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70ee9-123">Click OK.</span></span>
18. <span data-ttu-id="70ee9-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70ee9-124">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]