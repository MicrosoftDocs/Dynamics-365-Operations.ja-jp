---
title: "委託販売補充注文の作成"
description: "この手順では、委託製品の補充注文の作成方法が説明され、仕入先から該当する委託製品在庫までの予定配送を追跡確認できます。"
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 6286e8f52b8131a8e4779f1e11d84233b8e0760e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="0e510-103">委託販売補充注文の作成</span><span class="sxs-lookup"><span data-stu-id="0e510-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e510-104">この手順では、委託製品の補充注文の作成方法が説明され、仕入先から該当する委託製品在庫までの予定配送を追跡確認できます。</span><span class="sxs-lookup"><span data-stu-id="0e510-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="0e510-105">このほか、委託製品が仕入先所有の手持在庫として登録されるように製品の受領を記録する方法についても記述されています。</span><span class="sxs-lookup"><span data-stu-id="0e510-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="0e510-106">この作業は通常、調達担当者が行います。</span><span class="sxs-lookup"><span data-stu-id="0e510-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="0e510-107">デモ データの会社 USMF でこのガイドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e510-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="0e510-108">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="0e510-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="0e510-109">委託販売補充注文の作成</span><span class="sxs-lookup"><span data-stu-id="0e510-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="0e510-110">[調達] > [委託販売] > [委託販売補充注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0e510-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="0e510-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-111">Click New.</span></span>
3. <span data-ttu-id="0e510-112">[仕入先アカウント] フィールドで「US-104」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e510-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="0e510-113">在庫所有者ページで、所有者として登録されている仕入先を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e510-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="0e510-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-114">Click OK.</span></span>
5. <span data-ttu-id="0e510-115">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-115">Click Add line.</span></span>
6. <span data-ttu-id="0e510-116">[品目番号] フィールドで「M9211CI」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e510-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="0e510-117">委託販売積送品の在庫に設定されている品目を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e510-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="0e510-118">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e510-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="0e510-119">[配送希望日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e510-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="0e510-120">要求、確認された日付は、製品の予定着荷のMRPエンジンにより使用されています。</span><span class="sxs-lookup"><span data-stu-id="0e510-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="0e510-121">[確認済配送日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e510-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="0e510-122">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="0e510-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="0e510-123">[在庫分析コード] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="0e510-124">在庫規模所有者フィールドで所有者を表示するには、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="0e510-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="0e510-125">仕入先US-104は所有者としてリストアップされています。</span><span class="sxs-lookup"><span data-stu-id="0e510-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="0e510-126">在庫トランザクション状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="0e510-127">[在庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-127">Click Inventory.</span></span>
2. <span data-ttu-id="0e510-128">[トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-128">Click Transactions.</span></span>
3. <span data-ttu-id="0e510-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0e510-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0e510-130">[受領] フィールドが [注文済] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e510-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="0e510-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0e510-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="0e510-132">品目の受信 (複数)</span><span class="sxs-lookup"><span data-stu-id="0e510-132">Receive items</span></span>
1. <span data-ttu-id="0e510-133">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-133">Click Product receipt.</span></span>
2. <span data-ttu-id="0e510-134">[外部製品受領] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e510-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="0e510-135">[数量] フィールドにおいて、ここに表示される数値より小さい数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e510-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="0e510-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="0e510-137">手持在庫を確認します。</span><span class="sxs-lookup"><span data-stu-id="0e510-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="0e510-138">[在庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-138">Click Inventory.</span></span>
2. <span data-ttu-id="0e510-139">[手持] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-139">Click On-hand.</span></span>
3. <span data-ttu-id="0e510-140">[概要] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-140">Click Overview.</span></span>
    * <span data-ttu-id="0e510-141">仕入先が所有する委託製品在庫として受領された品目は手持在庫として使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e510-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="0e510-142">委託製品補充注文の残余数量は [合計] フィールドの [注文済] に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e510-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="0e510-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0e510-143">Close the page.</span></span>
5. <span data-ttu-id="0e510-144">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e510-144">Click Close.</span></span>
