---
title: 組織単位間のリレーションシップのデザイン
description: この手順では、組織単位間の関係をデザインする方法を説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner, OMNodeSelection,  HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 132b3133bd75cd2b47a96a60e943ff96e686fecf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229891"
---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="87629-103">組織単位間のリレーションシップのデザイン</span><span class="sxs-lookup"><span data-stu-id="87629-103">Design the relationships between organizational units</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87629-104">この手順では、組織単位間の関係をデザインする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="87629-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="87629-105">関係を定義する前に新しい組織の目的を作成する必要があります。または既存の組織の目的を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="87629-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="87629-106">この手順を完了するのに使用されるデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="87629-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="87629-107">このタスクは、管理者ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="87629-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="87629-108">[組織管理] > [組織] > [組織階層] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="87629-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="87629-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-109">Click New.</span></span>
3. <span data-ttu-id="87629-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87629-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="87629-111">[目的の割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="87629-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87629-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="87629-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-113">Click Add.</span></span>
7. <span data-ttu-id="87629-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87629-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="87629-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-115">Click OK.</span></span>
    * <span data-ttu-id="87629-116">組織の目的は、組織のために必要な数だけ選択できます。</span><span class="sxs-lookup"><span data-stu-id="87629-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="87629-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87629-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="87629-118">[既定として設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-118">Click Set as default.</span></span>
11. <span data-ttu-id="87629-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="87629-119">Close the page.</span></span>
12. <span data-ttu-id="87629-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-120">Click Save.</span></span>
13. <span data-ttu-id="87629-121">[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-121">Click View.</span></span>
14. <span data-ttu-id="87629-122">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-122">Click Edit.</span></span>
15. <span data-ttu-id="87629-123">[挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-123">Click Insert.</span></span>
16. <span data-ttu-id="87629-124">[事業単位] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-124">Click Business unit.</span></span>
17. <span data-ttu-id="87629-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87629-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="87629-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="87629-127">[挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-127">Click Insert.</span></span>
20. <span data-ttu-id="87629-128">Commerce チャネルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-128">Click Commerce channel.</span></span>
21. <span data-ttu-id="87629-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87629-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="87629-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="87629-131">組織単位は、必要な数だけ追加できます。</span><span class="sxs-lookup"><span data-stu-id="87629-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="87629-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-132">Click Save.</span></span>
24. <span data-ttu-id="87629-133">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-133">Click Close.</span></span>
25. <span data-ttu-id="87629-134">[発行] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="87629-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="87629-135">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="87629-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="87629-136">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="87629-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="87629-137">[変更の説明] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87629-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="87629-138">[発行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-138">Click Publish.</span></span>
30. <span data-ttu-id="87629-139">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87629-139">Click Close.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]