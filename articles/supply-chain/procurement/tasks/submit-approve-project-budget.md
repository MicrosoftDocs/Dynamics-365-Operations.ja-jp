--- 
title: "プロジェクト予算の送信および承認"
description: "この手順ではプロジェクトの予算を作成して送信する方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 02/09/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9aa94d31a0ebeab4e4dac148e663c631a130878d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="submit-and-approve-project-budgets"></a><span data-ttu-id="220ee-103">プロジェクト予算の送信および承認</span><span class="sxs-lookup"><span data-stu-id="220ee-103">Submit and approve project budgets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="220ee-104">この手順ではプロジェクトの予算を作成して送信する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="220ee-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="220ee-105">プロジェクト予算を作成するとき、プロジェクトの収益および原価の見積を入力してから、実際のプロジェクト トランザクションの管理に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="220ee-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="220ee-106">プロジェクトの予算作成では、元の予算と修正内容をプロジェクト ワークフローに送って認証を申請する必要があります。</span><span class="sxs-lookup"><span data-stu-id="220ee-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="220ee-107">ワークフローを使用すると、プロセスの管理を強化できるうえ、変更履歴レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="220ee-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="220ee-108">このタスクは、USSI データ セットを使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="220ee-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="220ee-109">[プロジェクト管理および会計] > [プロジェクト] > [すべてのプロジェクト] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="220ee-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="220ee-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="220ee-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="220ee-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="220ee-112">[アクション] ペインで [計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="220ee-113">[プロジェクト予算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-113">Click Project budget.</span></span>
6. <span data-ttu-id="220ee-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="220ee-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="220ee-115">[原価] セクションを展開</span><span class="sxs-lookup"><span data-stu-id="220ee-115">Expand the Cost section</span></span>
8. <span data-ttu-id="220ee-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-116">Click New.</span></span>
9. <span data-ttu-id="220ee-117">[トランザクション タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="220ee-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="220ee-118">[カテゴリ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="220ee-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="220ee-119">[元の予算] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="220ee-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="220ee-120">[収益] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="220ee-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="220ee-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-121">Click New.</span></span>
14. <span data-ttu-id="220ee-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="220ee-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="220ee-123">[トランザクション タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="220ee-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="220ee-124">[カテゴリ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="220ee-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="220ee-125">[元の予算] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="220ee-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="220ee-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-126">Click Save.</span></span>
19. <span data-ttu-id="220ee-127">[ワークフロー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-127">Click Workflow.</span></span>
20. <span data-ttu-id="220ee-128">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-128">Click Submit.</span></span>
21. <span data-ttu-id="220ee-129">[コメント] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="220ee-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="220ee-130">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="220ee-130">Click Submit.</span></span>


