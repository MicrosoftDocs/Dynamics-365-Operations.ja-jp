---
title: "有効在庫数の確認"
description: "この手順では、特定の品目番号において現物手持在庫を確認する方法を示します。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a0c440250588e38b4bc8ebdb6830b026361f1d96
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="3336c-103">有効在庫数の確認</span><span class="sxs-lookup"><span data-stu-id="3336c-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3336c-104">この手順では、特定の品目番号において現物手持在庫を確認する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3336c-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="3336c-105">またこれらは品目に関連する供給情報を取得する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="3336c-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="3336c-106">現物手持在庫とは使用可能である、つまり、購入済、受領済、登録済である手持ち在庫です。</span><span class="sxs-lookup"><span data-stu-id="3336c-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="3336c-107">手持在庫には使用可能な手持在庫が含まれる一方で、注文し、予想されているがまだ入庫されていないまたは登録されていない在庫も含まれます。</span><span class="sxs-lookup"><span data-stu-id="3336c-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="3336c-108">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="3336c-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="3336c-109">USMF を使用すると、表示される例の値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3336c-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="3336c-110">通常、これらのタスクを実施するのは、倉庫作業者です。</span><span class="sxs-lookup"><span data-stu-id="3336c-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="3336c-111">品目の手持在庫の確認</span><span class="sxs-lookup"><span data-stu-id="3336c-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="3336c-112">[在庫管理] > [照会およびレポート] > [手持在庫] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3336c-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="3336c-113">品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="3336c-113">Select the Item number row.</span></span>
    * <span data-ttu-id="3336c-114">手持在庫を品目番号で照会するには、手持在庫が設定されているテーブルおよび品目番号が設定されているフィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="3336c-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="3336c-115">[基準] フィールドで、クエリする品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3336c-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="3336c-116">デモ データの会社 USMF を使用する場合は、「M9201」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3336c-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="3336c-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-117">Click OK.</span></span>
5. <span data-ttu-id="3336c-118">[分析コード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-118">Click Dimensions.</span></span>
    * <span data-ttu-id="3336c-119">分析コード タブでは、自分の手持在庫をどれだけ詳細に表示するかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3336c-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="3336c-120">引当に関連するデータが必要な場合、高度な倉庫 (WHS) プロセスを使用する品目の在庫分析コードすべてを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3336c-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="3336c-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-121">Click OK.</span></span>
7. <span data-ttu-id="3336c-122">[アクション] ウィンドウで、「関連情報」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="3336c-123">これが表示されない場合、追加のアクション ウィンドウの選択を確認するために、[省略記号] ボタン (…) をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3336c-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="3336c-124">[供給の概要] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-124">Click Supply overview.</span></span>
    * <span data-ttu-id="3336c-125">供給の概要タブには、手持在庫の数量、リード タイム、仕入先情報などの特定の品目における供給情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3336c-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="3336c-126">[手持] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3336c-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="3336c-127">[仕入先] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3336c-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="3336c-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3336c-128">Close the page.</span></span>
12. <span data-ttu-id="3336c-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3336c-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="3336c-130">現物手持在庫の確認</span><span class="sxs-lookup"><span data-stu-id="3336c-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="3336c-131">[倉庫管理] > [照会およびレポート] > [現物手持在庫] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3336c-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="3336c-132">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3336c-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="3336c-133">品目の一覧をフィルタ処理するための [サイト] および[倉庫] フィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3336c-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="3336c-134">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="3336c-134">Refresh the page.</span></span>
4. <span data-ttu-id="3336c-135">[分析コードの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="3336c-136">分析コード表示タブでは、自分の手持在庫をどれだけ詳細に表示するかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3336c-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="3336c-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-137">Click OK.</span></span>
6. <span data-ttu-id="3336c-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3336c-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="3336c-139">手持在庫を保管場所ごとに確認する</span><span class="sxs-lookup"><span data-stu-id="3336c-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="3336c-140">[倉庫管理] > [照会およびレポート] > [保管場所ごとの手持在庫] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3336c-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="3336c-141">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3336c-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="3336c-142">USMF のデモ データ会社を使用すると、「51」を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3336c-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="3336c-143">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="3336c-143">Refresh the page.</span></span>
4. <span data-ttu-id="3336c-144">[分析コードの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="3336c-145">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3336c-145">Click OK.</span></span>
6. <span data-ttu-id="3336c-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3336c-146">Close the page.</span></span>

