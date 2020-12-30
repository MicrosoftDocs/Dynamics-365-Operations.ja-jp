---
title: 有効在庫数の確認
description: この手順では、特定の品目番号において現物手持在庫を確認する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28446e32c8f126e76b13f41f379ecf994a7b7a0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432232"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="886a2-103">有効在庫数の確認</span><span class="sxs-lookup"><span data-stu-id="886a2-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="886a2-104">この手順では、特定の品目番号において現物手持在庫を確認する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="886a2-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="886a2-105">またこれらは品目に関連する供給情報を取得する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="886a2-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="886a2-106">現物手持在庫とは使用可能である、つまり、購入済、受領済、登録済である手持在庫です。</span><span class="sxs-lookup"><span data-stu-id="886a2-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="886a2-107">手持在庫には使用可能な手持在庫が含まれる一方で、注文し、予定されているがまだ入庫されていない、または登録されていない在庫も含まれます。</span><span class="sxs-lookup"><span data-stu-id="886a2-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="886a2-108">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="886a2-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="886a2-109">USMF を使用すると、表示される例の値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="886a2-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="886a2-110">通常、これらのタスクを実施するのは、倉庫作業者です。</span><span class="sxs-lookup"><span data-stu-id="886a2-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="886a2-111">品目の手持在庫の確認</span><span class="sxs-lookup"><span data-stu-id="886a2-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="886a2-112">**ナビゲーション ウィンドウ > モジュール > 在庫管理 > 照会およびレポート > 手持在庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="886a2-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="886a2-113">**品目番号** 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="886a2-113">Select the **Item number** row.</span></span> <span data-ttu-id="886a2-114">手持在庫を品目番号で照会するには、**手持在庫** が設定されているテーブルおよび **品目** 番号が設定されているフィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="886a2-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="886a2-115">**基準** フィールドで、クエリする品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="886a2-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="886a2-116">デモ データの会社 USMF を使用する場合は、「M9201」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="886a2-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="886a2-117">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-117">Click **OK**.</span></span>
5. <span data-ttu-id="886a2-118">**アクション ウィンドウ** で、**分析コード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="886a2-119">**分析コード** タブでは、自分の手持在庫をどれだけ詳細に表示するかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="886a2-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="886a2-120">引当に関連するデータが必要な場合、高度な倉庫 (WMS) プロセスを使用する品目の在庫分析コードすべてを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="886a2-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="886a2-121">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-121">Click **OK**.</span></span>
7. <span data-ttu-id="886a2-122">**アクション ウィンドウ** で、**関連情報** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="886a2-123">このオプションが表示されない場合、追加のアクション ウィンドウの選択を確認するには、省略記号ボタン (…) をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="886a2-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="886a2-124">**供給の概要** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-124">Click **Supply overview**.</span></span> <span data-ttu-id="886a2-125">**供給の概要** タブには、手持在庫の数量、リード タイム、仕入先情報などの特定の品目における供給情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="886a2-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="886a2-126">**手持** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="886a2-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="886a2-127">**仕入先** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="886a2-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="886a2-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="886a2-128">Close the page.</span></span>
12. <span data-ttu-id="886a2-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="886a2-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="886a2-130">現物手持在庫の確認</span><span class="sxs-lookup"><span data-stu-id="886a2-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="886a2-131">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 照会およびレポート > 現物手持在庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="886a2-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="886a2-132">**品目番号** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="886a2-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="886a2-133">品目の一覧をフィルタ処理するための [サイト] および[倉庫] フィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="886a2-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="886a2-134">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="886a2-134">Refresh the page.</span></span>
4. <span data-ttu-id="886a2-135">**アクション ウィンドウ** で、**分析コードの表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="886a2-136">分析コード表示タブでは、自分の手持在庫をどれだけ詳細に表示するかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="886a2-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="886a2-137">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-137">Click **OK**.</span></span>
6. <span data-ttu-id="886a2-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="886a2-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="886a2-139">手持在庫を保管場所ごとに確認する</span><span class="sxs-lookup"><span data-stu-id="886a2-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="886a2-140">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 照会およびレポート > 保管場所ごとの手持在庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="886a2-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="886a2-141">**倉庫** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="886a2-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="886a2-142">USMF のデモ データ会社を使用すると、「51」を使用できます。</span><span class="sxs-lookup"><span data-stu-id="886a2-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="886a2-143">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="886a2-143">Refresh the page.</span></span>
4. <span data-ttu-id="886a2-144">**分析コードの表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="886a2-145">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="886a2-145">Click **OK**.</span></span>
6. <span data-ttu-id="886a2-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="886a2-146">Close the page.</span></span>

