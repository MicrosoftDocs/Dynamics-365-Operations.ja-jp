---
title: 在庫設定を適用する
description: このトピックでは在庫設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 737e71dc73750bf151629fd904081924ac15b91e
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621224"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="e4661-103">在庫設定を適用する</span><span class="sxs-lookup"><span data-stu-id="e4661-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4661-104">このトピックでは在庫設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4661-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e4661-105">概要</span><span class="sxs-lookup"><span data-stu-id="e4661-105">Overview</span></span>

<span data-ttu-id="e4661-106">在庫設定では、製品をカートに追加する前に在庫を確認するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e4661-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="e4661-107">また、"在庫あり" や "残りわずか" などの在庫関連の販売促進メッセージも定義します。</span><span class="sxs-lookup"><span data-stu-id="e4661-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="e4661-108">これらの設定により、在庫切れの製品は購入できなくなります。</span><span class="sxs-lookup"><span data-stu-id="e4661-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="e4661-109">Dynamics 365 Commerce は、製品の手持在庫の見積を提供します。</span><span class="sxs-lookup"><span data-stu-id="e4661-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="e4661-110">見積済手持在庫の計算方法については、[小売チャンネルの引当可能在庫数量の計算](calculated-inventory-retail-channels.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4661-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="e4661-111">Commerce サイト ビルダーでは、在庫のしきい値と範囲を製品またはカテゴリに対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="e4661-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="e4661-112">在庫を在庫あり、低在庫、または在庫切れに分類できるかを判定します。</span><span class="sxs-lookup"><span data-stu-id="e4661-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="e4661-113">詳細については、[在庫バッファーと在庫レベルのコンフィギュレーション](inventory-buffers-levels.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4661-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="e4661-114">在庫設定</span><span class="sxs-lookup"><span data-stu-id="e4661-114">Inventory settings</span></span>

<span data-ttu-id="e4661-115">Commerce では、在庫設定はサイト ビルダーの **サイト設定 \> 拡張機能 \> 在庫管理** で定義されています。</span><span class="sxs-lookup"><span data-stu-id="e4661-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="e4661-116">4 つの在庫設定があり、そのうちの 1 つは廃止されています (非推奨):</span><span class="sxs-lookup"><span data-stu-id="e4661-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="e4661-117">**アプリで在庫チェックを有効にする** – この設定により、製品の在庫確認が有効になります。</span><span class="sxs-lookup"><span data-stu-id="e4661-117">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="e4661-118">購入ボックス、カート、店舗で受け取り モジュールで製品在庫が確認され、在庫がある場合にのみ製品をカートに追加できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e4661-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="e4661-119">**基準となる在庫レベル** – この設定では、在庫レベルの計算方法が定義されます。</span><span class="sxs-lookup"><span data-stu-id="e4661-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="e4661-120">使用可能な値は、**引当可能合計数**、**引当可能現物数**、**在庫切れしきい** です。</span><span class="sxs-lookup"><span data-stu-id="e4661-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="e4661-121">Commerce では、在庫のしきい値と範囲を製品とカテゴリごとに定義できます。</span><span class="sxs-lookup"><span data-stu-id="e4661-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="e4661-122">在庫 API は、**引当可能合計数** プロパティと **引当可能現物数** プロパティ両方の製品在庫情報を返します。</span><span class="sxs-lookup"><span data-stu-id="e4661-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="e4661-123">小売業者は、**引当可能合計数** または **引当可能現物数** の値が、在庫数と在庫状況および在庫切れの状態に対応する範囲を決定するために使用されるべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e4661-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="e4661-124">設定に **基準となる在庫レベル** の **在庫切れしきい** 値 は、古い (レガシ)、廃止値です。</span><span class="sxs-lookup"><span data-stu-id="e4661-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="e4661-125">選択すると、在庫数は **引当可能合計数** 値の結果から決定されますが、しきい値は、後で説明する **在庫切れしきい値** 数値設定によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="e4661-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="e4661-126">このしきい値の設定は、E コマース サイト全体のすべての製品に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4661-126">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="e4661-127">在庫がしきい値数を下回ると、製品は在庫切れと見なされます。</span><span class="sxs-lookup"><span data-stu-id="e4661-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="e4661-128">それ以外の場合は、在庫ありと見なされます。</span><span class="sxs-lookup"><span data-stu-id="e4661-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="e4661-129">**在庫切れのしきい** 値の機能は制限されており、バージョン 10.0.12 以降で使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e4661-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="e4661-130">**在庫範囲** – この設定では、メッセージがサイト モジュールに表示される在庫範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="e4661-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="e4661-131">これは、設定に **基準となる在庫レベル** で **引当可能合計数** 値または **引当可能現物数** 値のいずれかが選択されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4661-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="e4661-132">使用できる値は、**すべて**、**在庫が少なく在庫切れ**、**在庫切れ** です。</span><span class="sxs-lookup"><span data-stu-id="e4661-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="e4661-133">**すべて** を選択すると、在庫あり (" 使用可能" メッセージ) から 在庫切れ ("在庫切れ" メッセージ) まで、すべての在庫範囲のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4661-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="e4661-134">**在庫が少なく在庫切れ** を選択すると、在庫あり (" 使用可能" メッセージ) を除くすべての在庫範囲のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4661-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="e4661-135">**在庫切れ** を選択すると、"在庫切れ" メッセージのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4661-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="e4661-136">**在庫切れしきい** – この古い数値設定は、**基準となる在庫レベル** 設定に対して **在庫切れしきい** 値が選択されている場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="e4661-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="e4661-137">在庫設定を使用するモジュール</span><span class="sxs-lookup"><span data-stu-id="e4661-137">Modules that use inventory settings</span></span>

<span data-ttu-id="e4661-138">購入ボックス、欲しい物リスト、店舗セレクター、カート、買い物カゴ アイコン モジュールは、在庫設定を使用して、在庫範囲とメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="e4661-138">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="e4661-139">次の図は、在庫あり ("利用可能") メッセージを表示している製品詳細ページ (PDP) の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e4661-139">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![在庫ありメッセージがある PDP モジュールの例](./media/pdp-InStock.png)

<span data-ttu-id="e4661-141">次の図は、"在庫切れ" メッセージを表示している PDP の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e4661-141">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![在庫切れメッセージがある PDP モジュールの例](./media/pdp-outofstock.png)

<span data-ttu-id="e4661-143">次の図は、"在庫あり" メッセージを表示している買い物カゴの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e4661-143">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![在庫ありメッセージがある買い物カゴモジュールの例](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="e4661-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e4661-145">Additional resources</span></span>

[<span data-ttu-id="e4661-146">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="e4661-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e4661-147">在庫バッファーと在庫レベルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e4661-147">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="e4661-148">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="e4661-148">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e4661-149">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="e4661-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e4661-150">アカウント管理ページとモジュール</span><span class="sxs-lookup"><span data-stu-id="e4661-150">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="e4661-151">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="e4661-151">Store selector module</span></span>](store-selector.md)
