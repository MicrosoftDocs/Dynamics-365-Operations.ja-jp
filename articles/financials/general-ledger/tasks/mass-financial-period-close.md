--- 
title: "財務期間一括終了"
description: "この手順では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。"
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: cafd837be054e96afc10d3b78402bdcc67c43c33
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="mass-financial-period-close"></a><span data-ttu-id="5b929-103">財務期間一括終了</span><span class="sxs-lookup"><span data-stu-id="5b929-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b929-104">この手順では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5b929-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="5b929-105">またこのタスクは、特定のモジュールに転記されたユーザー グループを制限する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5b929-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="5b929-106">[総勘定元帳] > [期間の締め] > [元帳カレンダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b929-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="5b929-107">表示された法人の一覧は、ページで選択した会計カレンダーに依存することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5b929-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="5b929-108">選択された会計カレンダーを使用する法人のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b929-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="5b929-109">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b929-109">Click Edit.</span></span>
3. <span data-ttu-id="5b929-110">状態を変更する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b929-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="5b929-111">状態を更新する法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b929-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="5b929-112">グリッドの左上のチェック マークを選択することにより、すべての法人をすばやく選択できます。</span><span class="sxs-lookup"><span data-stu-id="5b929-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="5b929-113">[モジュール アクセスの更新] を選択して、選択されたモジュールへのアクセスの転記を定義します。</span><span class="sxs-lookup"><span data-stu-id="5b929-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="5b929-114">モジュールの状態は、グリッドのレコードを編集することにより順番に更新できます。</span><span class="sxs-lookup"><span data-stu-id="5b929-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="5b929-115">ボタンは、複数の法人のレコードをすばやく更新する場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="5b929-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="5b929-116">[アプリケーション モジュール] フィールドで、状態を更新するモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b929-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="5b929-117">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b929-117">Click Select.</span></span>
7. <span data-ttu-id="5b929-118">[アクセス レベル] で、[すべて]、[なし]、または特定のユーザー グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b929-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="5b929-119">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b929-119">Click Select.</span></span>
    * <span data-ttu-id="5b929-120">[すべて] は、オープン期間の場合、モジュールの編集アクセス許可を持つすべてのユーザーが転記できることを示します。</span><span class="sxs-lookup"><span data-stu-id="5b929-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="5b929-121">[なし] は、オープン期間の場合、ユーザーがモジュールに転記できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5b929-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="5b929-122">[特定のユーザー グループ] は、オープン期間の場合に、このグループのユーザーのみがモジュールに転記できることを示します。</span><span class="sxs-lookup"><span data-stu-id="5b929-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="5b929-123">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b929-123">Click Update.</span></span>
9. <span data-ttu-id="5b929-124">状態を更新する別の期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b929-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="5b929-125">状態を更新する法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b929-125">Select the legal entities for which you want to update the period status.</span></span>
11. <span data-ttu-id="5b929-126">[期間の状態の更新] を選択し、状態を [保留中]、[未処理]、または [完全に終了] に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b929-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="5b929-127">[オープン] は、ユーザーにアクセス許可がある場合に転記できる期間を示します。</span><span class="sxs-lookup"><span data-stu-id="5b929-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="5b929-128">[保留中] は、期間は転記できないが、再度開くことができることを意味します。</span><span class="sxs-lookup"><span data-stu-id="5b929-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="5b929-129">[完全に閉じる] は、期間が終了され、開くことができないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="5b929-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="5b929-130">調整は転記できません。</span><span class="sxs-lookup"><span data-stu-id="5b929-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="5b929-131">すべての調整と監査が完了するまで、期間を [完全に閉じる] と設定しないようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5b929-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="5b929-132">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b929-132">Click Update.</span></span>


