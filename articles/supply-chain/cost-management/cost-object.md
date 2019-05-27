---
title: 原価オブジェクト
description: この記事は、原価オブジェクトに関する情報を提供し、原価と数量を累計する方法を説明します。 原価オブジェクトは、原価と数量を累計するエンティティです。 原価オブジェクトのエンティティは、製品またはスタイル、および色のバリアントなどの製品バリアントのいずれかです。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275855f2fb4d32df91449d7ebb9ad9ba2bd3f36b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558552"
---
# <a name="cost-objects"></a><span data-ttu-id="3b571-105">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3b571-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b571-106">この記事は、原価オブジェクトに関する情報を提供し、原価と数量を累計する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3b571-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="3b571-107">原価オブジェクトは、原価と数量を累計するエンティティです。</span><span class="sxs-lookup"><span data-stu-id="3b571-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="3b571-108">原価オブジェクトのエンティティは、製品またはスタイル、および色のバリアントなどの製品バリアントのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="3b571-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="3b571-109">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3b571-109">Cost objects</span></span>

<span data-ttu-id="3b571-110">**原価オブジェクト**ページは、製品に登録されるすべての原価オブジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="3b571-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="3b571-111">原価オブジェクトは、次のソースのデータによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="3b571-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="3b571-112">品目</span><span class="sxs-lookup"><span data-stu-id="3b571-112">Product</span></span>
-   <span data-ttu-id="3b571-113">製品分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="3b571-113">Product dimension group</span></span>
-   <span data-ttu-id="3b571-114">保管分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="3b571-114">Storage dimension group</span></span>
-   <span data-ttu-id="3b571-115">追跡用分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="3b571-115">Tracking dimension group</span></span>

<span data-ttu-id="3b571-116">**注記:** 原価オブジェクトは、**直接材料** タイプの原価要素のみ表します。</span><span class="sxs-lookup"><span data-stu-id="3b571-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="3b571-117">原価オブジェクトと在庫オブジェクトは、資産在庫のために選択した在庫分析コードによる原価オブジェクトの定義方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="3b571-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="3b571-118">たとえば、品目には次のコンフィギュレーションがあります。</span><span class="sxs-lookup"><span data-stu-id="3b571-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="3b571-119">**サイト:** 現物在庫 = 有、資産在庫 = 有</span><span class="sxs-lookup"><span data-stu-id="3b571-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="3b571-120">**倉庫:** 現物在庫 = 有、資産在庫 = 無</span><span class="sxs-lookup"><span data-stu-id="3b571-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="3b571-121">**バッチ番号:** 現物在庫 = 有、資産在庫 = 無</span><span class="sxs-lookup"><span data-stu-id="3b571-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="3b571-122">次の表に、原価オブジェクトと在庫オブジェクトの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="3b571-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="3b571-123">オブジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="3b571-123">Object type</span></span>      | <span data-ttu-id="3b571-124">品目番号</span><span class="sxs-lookup"><span data-stu-id="3b571-124">Item number</span></span> | <span data-ttu-id="3b571-125">サービス拠点</span><span class="sxs-lookup"><span data-stu-id="3b571-125">Site</span></span> | <span data-ttu-id="3b571-126">倉庫</span><span class="sxs-lookup"><span data-stu-id="3b571-126">Warehouse</span></span> | <span data-ttu-id="3b571-127">バッチ番号</span><span class="sxs-lookup"><span data-stu-id="3b571-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="3b571-128">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3b571-128">Cost object</span></span>      | <span data-ttu-id="3b571-129"> x</span><span class="sxs-lookup"><span data-stu-id="3b571-129">x</span></span>           | <span data-ttu-id="3b571-130"> x</span><span class="sxs-lookup"><span data-stu-id="3b571-130">x</span></span>    |           |           |
| <span data-ttu-id="3b571-131">在庫オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3b571-131">Inventory object</span></span> | <span data-ttu-id="3b571-132"> x</span><span class="sxs-lookup"><span data-stu-id="3b571-132">x</span></span>           | <span data-ttu-id="3b571-133"> x</span><span class="sxs-lookup"><span data-stu-id="3b571-133">x</span></span>    |  <span data-ttu-id="3b571-134"> x</span><span class="sxs-lookup"><span data-stu-id="3b571-134">x</span></span>        | <span data-ttu-id="3b571-135"> x</span><span class="sxs-lookup"><span data-stu-id="3b571-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="3b571-136">原価と数量の累計</span><span class="sxs-lookup"><span data-stu-id="3b571-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="3b571-137">**値** フィールドの値は、次の値の合計です。</span><span class="sxs-lookup"><span data-stu-id="3b571-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="3b571-138">現物原価金額</span><span class="sxs-lookup"><span data-stu-id="3b571-138">Physical cost amount</span></span>
    -   <span data-ttu-id="3b571-139">財務費用金額</span><span class="sxs-lookup"><span data-stu-id="3b571-139">Financial cost amount</span></span>
    -   <span data-ttu-id="3b571-140">調整</span><span class="sxs-lookup"><span data-stu-id="3b571-140">Adjustments</span></span>
-   <span data-ttu-id="3b571-141">**数量**フィールドの値は、次の値の合計です。</span><span class="sxs-lookup"><span data-stu-id="3b571-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="3b571-142">受取済</span><span class="sxs-lookup"><span data-stu-id="3b571-142">Received</span></span>
    -   <span data-ttu-id="3b571-143">払出済</span><span class="sxs-lookup"><span data-stu-id="3b571-143">Deducted</span></span>
    -   <span data-ttu-id="3b571-144">転記された数量</span><span class="sxs-lookup"><span data-stu-id="3b571-144">Posted quantity</span></span>
-   <span data-ttu-id="3b571-145">**平均単位原価**フィールドは計算済フィールドです。</span><span class="sxs-lookup"><span data-stu-id="3b571-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="3b571-146">この値は、**値** の値を**数量**の値で割ることにより計算されます。</span><span class="sxs-lookup"><span data-stu-id="3b571-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="3b571-147">**注記:** **現物価格を含める**パラメーターは、前の計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="3b571-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="3b571-148">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="3b571-148">Additional resources</span></span>
--------

[<span data-ttu-id="3b571-149">製品分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="3b571-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="3b571-150">保管分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="3b571-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="3b571-151">追跡用分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="3b571-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="3b571-152">新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="3b571-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="3b571-153">コスト エントリ</span><span class="sxs-lookup"><span data-stu-id="3b571-153">Cost entries</span></span>](cost-entries.md)



