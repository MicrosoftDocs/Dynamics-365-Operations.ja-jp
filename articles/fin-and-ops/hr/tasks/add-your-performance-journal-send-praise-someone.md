--- 
title: "業績仕訳への追加および称賛の送信"
description: "パフォーマンスの仕訳帳には、目標を達成した方法、または期間中に実行した方法に関連する情報が保持されます。"
author: ShielaSogge
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a4595a259ecaa3cd8fea559b6f68d7f53af5f843
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="b21b6-103">業績仕訳への追加および称賛の送信</span><span class="sxs-lookup"><span data-stu-id="b21b6-103">Add to your performance journal and send praise to someone</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b21b6-104">パフォーマンスの仕訳帳には、目標を達成した方法、または期間中に実行した方法に関連する情報が保持されます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="b21b6-105">仕訳帳から同業者のアクションを賞賛できます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="b21b6-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b21b6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b21b6-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="b21b6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="b21b6-108">[すべてのワークスペース] > [従業員セルフ サービス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="b21b6-109">[業績仕訳] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-109">Click Performance journal.</span></span>
3. <span data-ttu-id="b21b6-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-110">Click New.</span></span>
4. <span data-ttu-id="b21b6-111">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="b21b6-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b21b6-113">パフォーマンス仕訳帳の日付は、仕訳帳が作成された日付です。</span><span class="sxs-lookup"><span data-stu-id="b21b6-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="b21b6-114">ソースは、パフォーマンス仕訳帳がどこから取得されたかを表します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="b21b6-115">1 つを作成すると、[自分の仕訳] から取得されます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="b21b6-116">マネージャーが 1 つを作成する場合、[マネージャーの仕訳帳] から取得されます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="b21b6-117">仕訳帳をマネージャーと共有するか、または作成者だけが表示できるようにできます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="b21b6-118">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="b21b6-119">[完了日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="b21b6-120">[開発計画] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="b21b6-121">[キーワード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="b21b6-122">[外部リンクの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-122">Click Add external link.</span></span>
11. <span data-ttu-id="b21b6-123">[説明] フィールドで「Envision」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="b21b6-124">インターネット アドレス フィールドには、「https://www.microsoft.com/en/envision/default」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="b21b6-125">グリッドに戻るには "パフォーマンス仕訳帳" と呼ばれる [保存] ボタンの下のキャプションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="b21b6-126">目標を開いた場合に表示されるように、選択した仕訳帳または仕訳帳を目標に追加できます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="b21b6-127">[クイック リンク] タブにリンクが追加されます。目標に仕訳帳を追加し、レビューに目標を追加すると、仕訳帳は自動的にレビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="b21b6-128">レビューを開いた場合に表示されるように、選択した仕訳帳または仕訳帳をレビューに追加できます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="b21b6-129">[クイック リンク] タブにリンクが追加されます。</span><span class="sxs-lookup"><span data-stu-id="b21b6-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="b21b6-130">[クイック追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-130">Click Quick add.</span></span>
15. <span data-ttu-id="b21b6-131">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="b21b6-132">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="b21b6-133">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-133">Click Save.</span></span>
18. <span data-ttu-id="b21b6-134">[称賛の送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-134">Click Send praise.</span></span>
19. <span data-ttu-id="b21b6-135">会社の従業員の一覧から個人を選択します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="b21b6-136">説明フィールドに、「会議でのすべての支援への感謝!」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b21b6-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="b21b6-137">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b21b6-137">Click Send.</span></span>


