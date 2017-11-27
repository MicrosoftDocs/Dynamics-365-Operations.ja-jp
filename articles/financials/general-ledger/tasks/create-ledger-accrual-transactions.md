--- 
title: "元帳発生トランザクションの作成"
description: "このタスク ガイドでは、発生主義スキーマに基づく元帳計上トランザクションの生成について説明します。"
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
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
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: a05f0777a14d627dc57ef4f4666abb6f92eee59a
ms.contentlocale: ja-jp
ms.lasthandoff: 10/26/2017

---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="d7a82-103">元帳発生トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="d7a82-103">Create ledger accrual transactions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7a82-104">このタスク ガイドでは、発生主義スキーマに基づく元帳計上トランザクションの生成について説明します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="d7a82-105">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="d7a82-106">一覧で、目的の仕訳帳を検索し選択するか、新しい仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="d7a82-107">[仕訳帳バッチ番号] フィールドをクリックしてリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="d7a82-108">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d7a82-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d7a82-109">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="d7a82-110">この例では、保険の経費を定義します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="d7a82-111">これは定期的経費の金額になります。</span><span class="sxs-lookup"><span data-stu-id="d7a82-111">It will become a periodic expense amount.</span></span>  
6. <span data-ttu-id="d7a82-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="d7a82-113">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="d7a82-114">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="d7a82-115">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a82-115">Click Functions.</span></span>
10. <span data-ttu-id="d7a82-116">[元帳計上] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a82-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="d7a82-117">[発生主義スキーマ ID] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7a82-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d7a82-118">一覧で、適用する発生主義スキーマを検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-118">In the list, find and select the accrual scheme you want to apply.</span></span>
13. <span data-ttu-id="d7a82-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a82-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d7a82-120">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7a82-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="d7a82-121">[トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a82-121">Click Transactions.</span></span>
16. <span data-ttu-id="d7a82-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d7a82-122">Close the page.</span></span>
17. <span data-ttu-id="d7a82-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a82-123">Click OK.</span></span>
18. <span data-ttu-id="d7a82-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a82-124">Click Post.</span></span>


