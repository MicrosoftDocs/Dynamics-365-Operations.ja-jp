--- 
title: "組織単位間のリレーションシップのデザイン"
description: "この手順では、組織単位間の関係をデザインする方法を説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e35915d2300755249ecd54bf2e4939d3a8df4f61
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="1cbd3-103">組織単位間のリレーションシップのデザイン</span><span class="sxs-lookup"><span data-stu-id="1cbd3-103">Design the relationships between organizational units</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1cbd3-104">この手順では、組織単位間の関係をデザインする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="1cbd3-105">関係を定義する前に新しい組織の目的を作成する必要があります。または既存の組織の目的を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="1cbd3-106">この手順を完了するのに使用されるデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="1cbd3-107">このタスクは、管理者ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="1cbd3-108">[組織管理] > [組織] > [組織階層] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="1cbd3-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-109">Click New.</span></span>
3. <span data-ttu-id="1cbd3-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1cbd3-111">[目的の割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="1cbd3-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="1cbd3-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-113">Click Add.</span></span>
7. <span data-ttu-id="1cbd3-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="1cbd3-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-115">Click OK.</span></span>
    * <span data-ttu-id="1cbd3-116">組織の目的は、組織のために必要な数だけ選択できます。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="1cbd3-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="1cbd3-118">[既定として設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-118">Click Set as default.</span></span>
11. <span data-ttu-id="1cbd3-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-119">Close the page.</span></span>
12. <span data-ttu-id="1cbd3-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-120">Click Save.</span></span>
13. <span data-ttu-id="1cbd3-121">[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-121">Click View.</span></span>
14. <span data-ttu-id="1cbd3-122">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-122">Click Edit.</span></span>
15. <span data-ttu-id="1cbd3-123">[挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-123">Click Insert.</span></span>
16. <span data-ttu-id="1cbd3-124">[事業単位] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-124">Click Business unit.</span></span>
17. <span data-ttu-id="1cbd3-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="1cbd3-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="1cbd3-127">[挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-127">Click Insert.</span></span>
20. <span data-ttu-id="1cbd3-128">[小売チャンネル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-128">Click Retail channel.</span></span>
21. <span data-ttu-id="1cbd3-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="1cbd3-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1cbd3-131">組織単位は、必要な数だけ追加できます。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="1cbd3-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-132">Click Save.</span></span>
24. <span data-ttu-id="1cbd3-133">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-133">Click Close.</span></span>
25. <span data-ttu-id="1cbd3-134">[発行] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="1cbd3-135">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="1cbd3-136">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="1cbd3-137">[変更の説明] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="1cbd3-138">[発行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-138">Click Publish.</span></span>
30. <span data-ttu-id="1cbd3-139">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cbd3-139">Click Close.</span></span>


