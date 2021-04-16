---
title: 出荷コンテナー
description: このトピックでは、陸揚原価モジュールの出荷コンテナーを設定する方法について説明します。
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833716"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="fa1f9-103">出荷コンテナーの設定</span><span class="sxs-lookup"><span data-stu-id="fa1f9-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa1f9-104">このトピックでは、**陸揚原価** モジュールの出荷コンテナーを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a> <span data-ttu-id="fa1f9-105">コンテナー タイプを設定します</span><span class="sxs-lookup"><span data-stu-id="fa1f9-105">Set up shipping container types</span></span>

<span data-ttu-id="fa1f9-106">出荷コンテナのタイプは、出荷時および航海中に使用できる出荷コンテナーのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="fa1f9-107">出荷コンテナー タイプを使用するには、**陸揚原価 \> コンテナ―設定 \> 出荷コンテナー タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="fa1f9-108">そこで、コンテナ タイプのレコードを表示、追加、および削除できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="fa1f9-109">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa1f9-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="fa1f9-110">Field</span></span> | <span data-ttu-id="fa1f9-111">説明</span><span class="sxs-lookup"><span data-stu-id="fa1f9-111">Description</span></span> |
|---|---|
| <span data-ttu-id="fa1f9-112">出荷コンテナー タイプ</span><span class="sxs-lookup"><span data-stu-id="fa1f9-112">Shipping container type</span></span> | <span data-ttu-id="fa1f9-113">出荷コンテナー タイプの固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="fa1f9-114">説明</span><span class="sxs-lookup"><span data-stu-id="fa1f9-114">Description</span></span> | <span data-ttu-id="fa1f9-115">出荷コンテナー タイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="fa1f9-116">量</span><span class="sxs-lookup"><span data-stu-id="fa1f9-116">Volume</span></span> | <span data-ttu-id="fa1f9-117">このタイプの出荷コンテナーの最大容積を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="fa1f9-118">太さ</span><span class="sxs-lookup"><span data-stu-id="fa1f9-118">Weight</span></span> | <span data-ttu-id="fa1f9-119">このタイプの出荷コンテナーの最大重量を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="fa1f9-120">返品可能</span><span class="sxs-lookup"><span data-stu-id="fa1f9-120">Returnable</span></span> | <span data-ttu-id="fa1f9-121">このタイプの出荷コンテナーは、航海中に使用された後で仕入先に返品できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="fa1f9-122">このオプションが *はい* に設定されている場合、このタイプの出荷コンテナーを原産港に戻す場合に追加費用が適用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="fa1f9-123">出荷コンテナーの設定</span><span class="sxs-lookup"><span data-stu-id="fa1f9-123">Set up shipping containers</span></span>

<span data-ttu-id="fa1f9-124">出荷コンテナー レコードは、航海中に使用する各コンテナーを識別するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="fa1f9-125">航海を作成する場合、ここで定義した出荷コンテナー レコードの一覧で、特定のコンテナーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="fa1f9-126">この機能は、会社が独自の出荷コンテナーを所有している場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="fa1f9-127">1 回だけ使用される出荷コンテナーの出荷コンテナー番号を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="fa1f9-128">代わりに、航海を作成するときに出荷コンテナー番号を追加できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="fa1f9-129">出荷コンテナー レコードは、陸揚原価でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="fa1f9-130">標準の **輸送管理モジュール** (INS) では使用できません。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="fa1f9-131">出荷コンテナーを使用するには、**陸揚原価 \> コンテナ―設定 \> 出荷コンテナー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="fa1f9-132">そこで、出荷コンテナーのレコードを表示、追加、および削除できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="fa1f9-133">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa1f9-134">フィールド</span><span class="sxs-lookup"><span data-stu-id="fa1f9-134">Field</span></span> | <span data-ttu-id="fa1f9-135">説明</span><span class="sxs-lookup"><span data-stu-id="fa1f9-135">Description</span></span> |
|---|---|
| <span data-ttu-id="fa1f9-136">出荷コンテナー</span><span class="sxs-lookup"><span data-stu-id="fa1f9-136">Shipping container</span></span> | <span data-ttu-id="fa1f9-137">出荷コンテナーの固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="fa1f9-138">出荷コンテナー タイプ</span><span class="sxs-lookup"><span data-stu-id="fa1f9-138">Shipping container type</span></span> | <span data-ttu-id="fa1f9-139">出荷コンテナーのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-139">Select the type of shipping container.</span></span> <span data-ttu-id="fa1f9-140">詳細については、このトピックで前述した [出荷コンテナー タイプの設定](#shipping-container-types) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="fa1f9-141">出荷コンテナーの設定はオプションです。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-141">The shipping container setup is optional.</span></span> <span data-ttu-id="fa1f9-142">通常、このコンテナーは、会社が独自の出荷コンテナーを所有している場合、または多くの場合は同じ出荷コンテナーを再利用する場合にのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="fa1f9-143">出荷コンテナー番号のチェック ディジットは計算されません。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a> <span data-ttu-id="fa1f9-144">単位タイプの設定</span><span class="sxs-lookup"><span data-stu-id="fa1f9-144">Set up unit types</span></span>

<span data-ttu-id="fa1f9-145">単位タイプにより、出荷コンテナーの追加のグループ化と識別方法が設定されます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="fa1f9-146">通常、単位タイプは、パレットまたはドラムなど、商品が梱包されているコンテナーのタイプを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="fa1f9-147">単位タイプは、**すべての出荷コンテナー** ページでコンテナーを設定するときに選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="fa1f9-148">単位タイプは、陸揚原価でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="fa1f9-149">TMS では使用できません。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-149">They aren't available in TMS.</span></span>

<span data-ttu-id="fa1f9-150">単位タイプを使用するには、**陸揚原価 \> コンテナ―設定 \> 単位タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="fa1f9-151">そこで、単位タイプのレコードを表示、追加、および削除できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="fa1f9-152">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa1f9-153">フィールド</span><span class="sxs-lookup"><span data-stu-id="fa1f9-153">Field</span></span> | <span data-ttu-id="fa1f9-154">説明</span><span class="sxs-lookup"><span data-stu-id="fa1f9-154">Description</span></span> |
|---|---|
| <span data-ttu-id="fa1f9-155">単位タイプ</span><span class="sxs-lookup"><span data-stu-id="fa1f9-155">Unit type</span></span> | <span data-ttu-id="fa1f9-156">単位タイプの固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="fa1f9-157">説明</span><span class="sxs-lookup"><span data-stu-id="fa1f9-157">Description</span></span> | <span data-ttu-id="fa1f9-158">単位タイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a> <span data-ttu-id="fa1f9-159">冷却タイプの設定</span><span class="sxs-lookup"><span data-stu-id="fa1f9-159">Set up refrigeration types</span></span>

<span data-ttu-id="fa1f9-160">冷却タイプは、出荷コンテナーを追加のグループ化と、識別方法を確立します (通常、冷却コンテナーの出荷コンテナー)。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="fa1f9-161">冷却タイプは、**すべての出荷コンテナー** ページでコンテナーを設定するときに選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="fa1f9-162">冷却タイプを使用するには、**陸揚原価 \> コンテナ―設定 \> 冷却タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="fa1f9-163">そこで、冷却タイプのレコードを表示、追加、および削除できます。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="fa1f9-164">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa1f9-165">フィールド</span><span class="sxs-lookup"><span data-stu-id="fa1f9-165">Field</span></span> | <span data-ttu-id="fa1f9-166">説明</span><span class="sxs-lookup"><span data-stu-id="fa1f9-166">Description</span></span> |
|---|---|
| <span data-ttu-id="fa1f9-167">冷却タイプ</span><span class="sxs-lookup"><span data-stu-id="fa1f9-167">Refrigeration type</span></span> | <span data-ttu-id="fa1f9-168">冷却タイプの固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="fa1f9-169">説明</span><span class="sxs-lookup"><span data-stu-id="fa1f9-169">Description</span></span> | <span data-ttu-id="fa1f9-170">冷却タイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa1f9-170">Enter a description of the refrigeration type.</span></span> |
