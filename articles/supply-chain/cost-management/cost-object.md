---
title: 原価オブジェクト
description: この記事は、原価オブジェクトに関する情報を提供し、原価と数量を累計する方法を説明します。 原価オブジェクトは、原価と数量を累計するエンティティです。 原価オブジェクトのエンティティは、製品またはスタイル、および色のバリアントなどの製品バリアントのいずれかです。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e590322c75cfb2ad21236af56656061037a4b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432104"
---
# <a name="cost-objects"></a><span data-ttu-id="f8c5d-105">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f8c5d-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8c5d-106">この記事は、原価オブジェクトに関する情報を提供し、原価と数量を累計する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="f8c5d-107">原価オブジェクトは、原価と数量を累計するエンティティです。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="f8c5d-108">原価オブジェクトのエンティティは、製品またはスタイル、および色のバリアントなどの製品バリアントのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="f8c5d-109">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f8c5d-109">Cost objects</span></span>

<span data-ttu-id="f8c5d-110">**原価オブジェクト** ページは、製品に登録されるすべての原価オブジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="f8c5d-111">原価オブジェクトは、次のソースのデータによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="f8c5d-112">品目</span><span class="sxs-lookup"><span data-stu-id="f8c5d-112">Product</span></span>
-   <span data-ttu-id="f8c5d-113">製品分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-113">Product dimension group</span></span>
-   <span data-ttu-id="f8c5d-114">保管分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-114">Storage dimension group</span></span>
-   <span data-ttu-id="f8c5d-115">追跡用分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-115">Tracking dimension group</span></span>

<span data-ttu-id="f8c5d-116">**注記:** 原価オブジェクトは、**直接材料** タイプの原価要素のみ表します。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="f8c5d-117">原価オブジェクトと在庫オブジェクトは、資産在庫のために選択した在庫分析コードによる原価オブジェクトの定義方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="f8c5d-118">たとえば、品目には次のコンフィギュレーションがあります。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="f8c5d-119">**サイト:** 現物在庫 = 有、資産在庫 = 有</span><span class="sxs-lookup"><span data-stu-id="f8c5d-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="f8c5d-120">**倉庫:** 現物在庫 = 有、資産在庫 = 無</span><span class="sxs-lookup"><span data-stu-id="f8c5d-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="f8c5d-121">**バッチ番号:** 現物在庫 = 有、資産在庫 = 無</span><span class="sxs-lookup"><span data-stu-id="f8c5d-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="f8c5d-122">次の表に、原価オブジェクトと在庫オブジェクトの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="f8c5d-123">オブジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-123">Object type</span></span>      | <span data-ttu-id="f8c5d-124">品目番号</span><span class="sxs-lookup"><span data-stu-id="f8c5d-124">Item number</span></span> | <span data-ttu-id="f8c5d-125">サービス拠点</span><span class="sxs-lookup"><span data-stu-id="f8c5d-125">Site</span></span> | <span data-ttu-id="f8c5d-126">倉庫</span><span class="sxs-lookup"><span data-stu-id="f8c5d-126">Warehouse</span></span> | <span data-ttu-id="f8c5d-127">バッチ番号</span><span class="sxs-lookup"><span data-stu-id="f8c5d-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="f8c5d-128">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f8c5d-128">Cost object</span></span>      | <span data-ttu-id="f8c5d-129"> x</span><span class="sxs-lookup"><span data-stu-id="f8c5d-129">x</span></span>           | <span data-ttu-id="f8c5d-130"> x</span><span class="sxs-lookup"><span data-stu-id="f8c5d-130">x</span></span>    |           |           |
| <span data-ttu-id="f8c5d-131">在庫オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f8c5d-131">Inventory object</span></span> | <span data-ttu-id="f8c5d-132"> x</span><span class="sxs-lookup"><span data-stu-id="f8c5d-132">x</span></span>           | <span data-ttu-id="f8c5d-133"> x</span><span class="sxs-lookup"><span data-stu-id="f8c5d-133">x</span></span>    |  <span data-ttu-id="f8c5d-134"> x</span><span class="sxs-lookup"><span data-stu-id="f8c5d-134">x</span></span>        | <span data-ttu-id="f8c5d-135"> x</span><span class="sxs-lookup"><span data-stu-id="f8c5d-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="f8c5d-136">原価と数量の累計</span><span class="sxs-lookup"><span data-stu-id="f8c5d-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="f8c5d-137">**値** フィールドの値は、次の値の合計です。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="f8c5d-138">現物原価金額</span><span class="sxs-lookup"><span data-stu-id="f8c5d-138">Physical cost amount</span></span>
    -   <span data-ttu-id="f8c5d-139">財務費用金額</span><span class="sxs-lookup"><span data-stu-id="f8c5d-139">Financial cost amount</span></span>
    -   <span data-ttu-id="f8c5d-140">調整</span><span class="sxs-lookup"><span data-stu-id="f8c5d-140">Adjustments</span></span>
-   <span data-ttu-id="f8c5d-141">**数量** フィールドの値は、次の値の合計です。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="f8c5d-142">受取済</span><span class="sxs-lookup"><span data-stu-id="f8c5d-142">Received</span></span>
    -   <span data-ttu-id="f8c5d-143">払出済</span><span class="sxs-lookup"><span data-stu-id="f8c5d-143">Deducted</span></span>
    -   <span data-ttu-id="f8c5d-144">転記された数量</span><span class="sxs-lookup"><span data-stu-id="f8c5d-144">Posted quantity</span></span>
-   <span data-ttu-id="f8c5d-145">**平均単位原価** フィールドは計算済フィールドです。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="f8c5d-146">この値は、**値** の値を **数量** の値で割ることにより計算されます。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="f8c5d-147">**注記:** **現物価格を含める**パラメーターは、前の計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="f8c5d-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f8c5d-148">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f8c5d-148">Additional resources</span></span>
--------

[<span data-ttu-id="f8c5d-149">製品分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="f8c5d-150">保管分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="f8c5d-151">追跡用分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="f8c5d-152">新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="f8c5d-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="f8c5d-153">コスト エントリ</span><span class="sxs-lookup"><span data-stu-id="f8c5d-153">Cost entries</span></span>](cost-entries.md)



