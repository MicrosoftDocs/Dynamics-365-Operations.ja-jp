--- 
title: "ロイヤルティ報酬ポイント調整の処理"
description: "この手順では、ロイヤルティ カード情報を検索し、ロイヤルティ報酬ポイントを調整する方法を示します。"
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 44e406c8869ec376858f1a9312d533029a534c09
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="80d96-103">ロイヤルティ報酬ポイント調整の処理</span><span class="sxs-lookup"><span data-stu-id="80d96-103">Process loyalty reward point adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="80d96-104">この手順では、ロイヤルティ カード情報を検索し、ロイヤルティ報酬ポイントを調整する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="80d96-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="80d96-105">このタスクの作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="80d96-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="80d96-106">このタスクは小売工程マネージャー ロールまたは顧客サービス マネージャ ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="80d96-106">This task is intended for the Retail operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="80d96-107">[ロイヤルティ カード] に移動</span><span class="sxs-lookup"><span data-stu-id="80d96-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="80d96-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="80d96-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="80d96-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="80d96-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="80d96-110">[カード トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80d96-110">Click Card transactions.</span></span>
    * <span data-ttu-id="80d96-111">このページでは、選択したロイヤルティ カードのすべてのロイヤルティ トランザクションを確認できます。</span><span class="sxs-lookup"><span data-stu-id="80d96-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="80d96-112">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="80d96-112">Close the page.</span></span>
6. <span data-ttu-id="80d96-113">[カードの調整] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80d96-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="80d96-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80d96-114">Click New.</span></span>
8. <span data-ttu-id="80d96-115">[報酬ポイント] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="80d96-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="80d96-116">[金額または数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="80d96-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="80d96-117">正の金額または負の金額を使用して、ロイヤルティ カードにポイントを追加、または削除できます。</span><span class="sxs-lookup"><span data-stu-id="80d96-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="80d96-118">[ロイヤルティ プログラム] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="80d96-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="80d96-119">[コメント] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="80d96-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="80d96-120">[調整の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80d96-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="80d96-121">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80d96-121">Click Yes.</span></span>
14. <span data-ttu-id="80d96-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="80d96-122">Close the page.</span></span>
    * <span data-ttu-id="80d96-123">通常、 [報酬のポイントの集計] タブの報酬ポイント調整の結果を表示するには、この時点でページを更新します。</span><span class="sxs-lookup"><span data-stu-id="80d96-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab.</span></span> <span data-ttu-id="80d96-124">しかし、タスク ガイドとしてこれを実行している場合、更新するとタスク ガイドが終了してしまうので、今すぐ更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="80d96-124">But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="80d96-125">[カード トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80d96-125">Click Card transactions.</span></span>
16. <span data-ttu-id="80d96-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="80d96-126">Close the page.</span></span>

