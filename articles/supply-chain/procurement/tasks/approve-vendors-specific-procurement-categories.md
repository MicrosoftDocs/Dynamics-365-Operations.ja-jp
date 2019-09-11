---
title: 特定の調達カテゴリに対する仕入先の承認
description: このトピックでは、Dynamics 365 for Finance and Operations の特定の調達カテゴリの仕入先を承認する方法について説明します。
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1583a2eedc535f81b84e3094fee1574451f6f209
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867152"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="f0104-103">特定の調達カテゴリに対する仕入先の承認</span><span class="sxs-lookup"><span data-stu-id="f0104-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0104-104">このトピックでは、Dynamics 365 for Finance and Operations の特定の調達カテゴリの仕入先を承認する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f0104-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="f0104-105">購買要求が作成されると、承認仕入先または優先仕入先を選択する必要があり、それは購入ポリシーの設定方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f0104-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="f0104-106">この手順では、特定の調達カテゴリに対して仕入先が承認、または優先されるよう指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f0104-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="f0104-107">通常、このタスクを実行するのは、調達担当者です。</span><span class="sxs-lookup"><span data-stu-id="f0104-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="f0104-108">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f0104-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="f0104-109">ナビゲーション ウィンドウで、**モジュール > 調達 > 仕入先 > すべての仕入先**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0104-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="f0104-110">カテゴリで承認仕入先または優先仕入先として設定する仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="f0104-111">アクション ウィンドウで、**一般**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="f0104-112">**カテゴリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-112">Select **Categories**.</span></span>
5. <span data-ttu-id="f0104-113">**カテゴリの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-113">Select **Add category**.</span></span>
6. <span data-ttu-id="f0104-114">**カテゴリ** フィールドで、**オフィスとデスク アクセサリ (OFFICE AND DESK ACCESSORIES)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="f0104-115">**仕入先カテゴリ ステータス** フィールドで、**優先**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="f0104-116">カテゴリに複数の優先仕入先を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="f0104-116">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="f0104-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-117">Select **Save**.</span></span>
9. <span data-ttu-id="f0104-118">ナビゲーション ウィンドウで、**モジュール > 調達 > 調達カテゴリ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0104-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="f0104-119">ツリーで、**CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="f0104-120">**仕入先**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f0104-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="f0104-121">選択した仕入先が、オフィスとデスク アクセサリ カテゴリの優先仕入先として表示されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="f0104-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="f0104-122">この手順をタスク ガイドとして実行する場合、仕入先の一覧にスクロールできるように**ロック解除**ボタンを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0104-122">If you’re running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="f0104-123">このページに優先仕入先および承認済仕入先を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="f0104-123">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="f0104-124">ツリーで、**OFFICE AND DESK ACCESSORIES** を展開し、**シザーズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="f0104-125">**親カテゴリからの継承仕入先:** フィールドで、**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="f0104-126">**親カテゴリからの継承仕入先:** フィールドで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0104-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

