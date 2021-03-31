---
title: 主勘定の作成
description: このタスクのガイドは、既存の勘定科目表への主勘定の追加方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccount, CompanyInfoList
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f1d1bfe358bbff1720e7d013c3bfeaba1a598ed0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216476"
---
# <a name="create-a-main-account"></a><span data-ttu-id="d9589-103">主勘定の作成</span><span class="sxs-lookup"><span data-stu-id="d9589-103">Create a main account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9589-104">このタスクのガイドは、既存の勘定科目表への主勘定の追加方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9589-104">This task guide steps through adding a main account to an existing chart of accounts.</span></span> <span data-ttu-id="d9589-105">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="d9589-105">This recording uses the USMF demo company.</span></span>  

1. <span data-ttu-id="d9589-106">**ナビゲーション ウィンドウ > モジュール > 総勘定元帳 > 勘定科目表 > 勘定 > 主勘定** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9589-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Accounts > Main accounts**.</span></span>
2. <span data-ttu-id="d9589-107">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9589-107">Click **New**.</span></span>
3. <span data-ttu-id="d9589-108">**主勘定** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9589-108">In the **Main account** field, type a value.</span></span>
4. <span data-ttu-id="d9589-109">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9589-109">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d9589-110">**主勘定タイプ** フィールドで、財務諸表で勘定残高および場所を最も適切に表すタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-110">In the **Main account type** field, select the type that best represents the accounts balance and location on financial statements.</span></span>
6. <span data-ttu-id="d9589-111">一覧から主勘定が属する勘定カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-111">In the list, select the account category the main account belongs to.</span></span> <span data-ttu-id="d9589-112">勘定カテゴリは既定の財務報告および Power BI ダッシュボードの内容に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d9589-112">Account category is used for default financial reports and Power BI dashboard content.</span></span>  
7. <span data-ttu-id="d9589-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9589-113">In the list, click the link in the selected row.</span></span> <span data-ttu-id="d9589-114">既定の借方または貸方残高を変更します。</span><span class="sxs-lookup"><span data-stu-id="d9589-114">Change the default debit or credit balance.</span></span>  
8. <span data-ttu-id="d9589-115">**既定通貨** フィールドで、通貨一覧から値を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-115">In the **Default currency** field, select a value from the list of currencies.</span></span>
9. <span data-ttu-id="d9589-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d9589-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9589-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d9589-118">**法人の上書き** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="d9589-118">Toggle the expansion of the **Legal entity overrides** section.</span></span>
12. <span data-ttu-id="d9589-119">**追加** をクリックして法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-119">Click **Add** to select a legal entity.</span></span>
13. <span data-ttu-id="d9589-120">一覧から [法人] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-120">In the list, select the Legal entity.</span></span>
14. <span data-ttu-id="d9589-121">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9589-121">Click **Add**.</span></span>
15. <span data-ttu-id="d9589-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d9589-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="d9589-123">**中断** チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="d9589-123">Check or uncheck the **Suspended** checkbox.</span></span>
17. <span data-ttu-id="d9589-124">**法定レポート** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d9589-124">Expand the **Financial reporting** section.</span></span>
18. <span data-ttu-id="d9589-125">**為替レート タイプ** フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d9589-125">In the **Exchange rate type** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="d9589-126">一覧から、**口座の為替レート タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-126">In the list, select the **Exchange rate type for the account**.</span></span>
20. <span data-ttu-id="d9589-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9589-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="d9589-128">**為替換算タイプ** フィールドで、口座の為替レートの計算方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9589-128">In the **Currency translation type** field, select the method for calculating exchange rates for the account.</span></span>
22. <span data-ttu-id="d9589-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9589-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]