--- 
title: "特定の調達カテゴリに対する仕入先の承認"
description: "購買要求が作成されると、承認仕入先または優先仕入先を選択する必要があり、それは購入ポリシーの設定方法によって異なります。"
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 22cee269c77c9c9ab605dd56f19d43a49bf70b1c
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="73dca-103">特定の調達カテゴリに対する仕入先の承認</span><span class="sxs-lookup"><span data-stu-id="73dca-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73dca-104">購買要求が作成されると、承認仕入先または優先仕入先を選択する必要があり、それは購入ポリシーの設定方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="73dca-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="73dca-105">この手順では、特定の調達カテゴリに対して仕入先が承認、または優先されるよう指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="73dca-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="73dca-106">通常、このタスクを実行するのは、調達担当者です。</span><span class="sxs-lookup"><span data-stu-id="73dca-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="73dca-107">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="73dca-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="73dca-108">[調達] > [仕入先] > [すべての仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="73dca-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="73dca-109">カテゴリで承認仕入先または優先仕入先として設定する仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="73dca-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="73dca-110">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73dca-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="73dca-111">[カテゴリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73dca-111">Click Categories.</span></span>
5. <span data-ttu-id="73dca-112">[カテゴリの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73dca-112">Click Add category.</span></span>
6. <span data-ttu-id="73dca-113">カテゴリ フィールドで、オフィスとデスク アクセサリ (OFFICE AND DESK ACCESSORIES) を選択します。</span><span class="sxs-lookup"><span data-stu-id="73dca-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="73dca-114">[仕入先カテゴリ ステータス] フィールドで、「優先」を選択します。</span><span class="sxs-lookup"><span data-stu-id="73dca-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="73dca-115">カテゴリに複数の優先仕入先を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="73dca-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="73dca-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73dca-116">Click Save.</span></span>
9. <span data-ttu-id="73dca-117">[調達] > [調達カテゴリ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="73dca-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="73dca-118">ツリーで、「CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES」を選択します。</span><span class="sxs-lookup"><span data-stu-id="73dca-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="73dca-119">[仕入先] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="73dca-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="73dca-120">選択した仕入先がオフィスとデスク アクセサリ カテゴリの優先仕入先として表示されるかどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="73dca-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="73dca-121">この手順をタスク ガイドとして実行する場合、仕入先の一覧にスクロールできるようにロック解除のボタンをクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="73dca-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="73dca-122">このページに優先仕入先および承認済仕入先を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="73dca-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="73dca-123">ツリーで、「OFFICE AND DESK ACCESSORIES」を展開します。</span><span class="sxs-lookup"><span data-stu-id="73dca-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="73dca-124">ツリーで、「シザーズ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="73dca-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="73dca-125">親カテゴリからの継承仕入先で [いいえ] を選択します。フィールド。</span><span class="sxs-lookup"><span data-stu-id="73dca-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="73dca-126">親カテゴリからの継承仕入先で [はい] を選択します。フィールド。</span><span class="sxs-lookup"><span data-stu-id="73dca-126">Select Yes in the Inherit vendors from parent category: field.</span></span>


