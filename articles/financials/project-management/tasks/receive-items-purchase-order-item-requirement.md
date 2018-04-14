--- 
title: "在庫品目要求からの発注書の品目の入庫"
description: "この手順は、在庫品目要求から発注書の品目を受け取る方法を示します。"
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fef6a597ed126ff4e1148fd9710b214c0425c3ab
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="f2094-103">在庫品目要求からの発注書の品目の入庫</span><span class="sxs-lookup"><span data-stu-id="f2094-103">Receive items on purchase order from item requirement</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2094-104">この手順は、在庫品目要求から発注書の品目を受け取る方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f2094-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="f2094-105">品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="f2094-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="f2094-106">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="f2094-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f2094-107">[プロジェクト管理および会計] > [プロジェクト] > [すべてのプロジェクト] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="f2094-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="f2094-108">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f2094-109">アクション ウィンドウで、[計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="f2094-110">[在庫品目要求] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-110">Click Item requirements.</span></span>
5. <span data-ttu-id="f2094-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-111">Click New.</span></span>
6. <span data-ttu-id="f2094-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f2094-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f2094-113">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f2094-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="f2094-114">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2094-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="f2094-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-115">Click Save.</span></span>
10. <span data-ttu-id="f2094-116">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="f2094-117">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-117">Click Functions.</span></span>
12. <span data-ttu-id="f2094-118">[発注書の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="f2094-119">[含む] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f2094-119">Select the Include check box.</span></span>
14. <span data-ttu-id="f2094-120">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f2094-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="f2094-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-121">Click OK.</span></span>
16. <span data-ttu-id="f2094-122">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f2094-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="f2094-123">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f2094-124">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="f2094-125">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-125">Click Confirm.</span></span>
20. <span data-ttu-id="f2094-126">アクション ウィンドウで、[入庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="f2094-127">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-127">Click Product receipt.</span></span>
22. <span data-ttu-id="f2094-128">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f2094-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="f2094-129">[製品受領書] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2094-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="f2094-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2094-130">Click OK.</span></span>


