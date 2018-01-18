--- 
title: "POS アクセス許可グループの作成"
description: "この手順は、POS アクセス許可グループを作成する方法を示します。"
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: e2fb5255c8f1c4994e7f53b5d05a2782350259ab
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="f9031-103">POS アクセス許可グループの作成</span><span class="sxs-lookup"><span data-stu-id="f9031-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f9031-104">この手順は、POS アクセス許可グループを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f9031-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="f9031-105">このタスクの作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="f9031-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f9031-106">このタスクは「小売工程マネージャー ロール」を対象としています。</span><span class="sxs-lookup"><span data-stu-id="f9031-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="f9031-107">アクセス許可グループに移動します。</span><span class="sxs-lookup"><span data-stu-id="f9031-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="f9031-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9031-108">Click New.</span></span>
3. <span data-ttu-id="f9031-109">[POS アクセス許可グループ ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9031-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="f9031-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9031-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f9031-111">[タイム レコーダー エントリの表示] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="f9031-112">これで、POS アクセス許可グループのさまざまなアクセス許可を有効、または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f9031-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="f9031-113">複数のアクセス許可に対して、POS ユーザーが操作を実行することができるかどうか評価するために使用する値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f9031-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="f9031-114">このタスク ガイドは、レジ担当者に支給される可能性があるいくつかのアクセス許可を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f9031-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="f9031-115">[注文の作成を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="f9031-116">[注文の編集を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="f9031-117">[注文の取得を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="f9031-118">[パスワードの変更を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="f9031-119">[ブラインド クローズを許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="f9031-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9031-120">Click Save.</span></span>
    * <span data-ttu-id="f9031-121">変更が保存された後、小売チャンネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9031-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="f9031-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f9031-122">Close the page.</span></span>
13. <span data-ttu-id="f9031-123">ジョブに移動</span><span class="sxs-lookup"><span data-stu-id="f9031-123">Go to Jobs.</span></span>
    * <span data-ttu-id="f9031-124">次に、ジョブに対して POS アクセス許可グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f9031-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="f9031-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f9031-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9031-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f9031-127">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9031-127">Click Edit.</span></span>
17. <span data-ttu-id="f9031-128">[ジョブ分類] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f9031-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="f9031-129">[POS アクセス許可グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f9031-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="f9031-130">作業者のPOS アクセス許可が職位のレベルで上書きされない場合、このジョブの職位のすべての作業者は、このPOS アクセス許可グループの設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9031-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="f9031-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9031-131">Click Save.</span></span>
    * <span data-ttu-id="f9031-132">変更が保存された後、小売チャンネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9031-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


