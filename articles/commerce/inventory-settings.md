---
title: 在庫設定を適用する
description: このトピックでは在庫設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ae0195f63b123a345b0cdcd4976bfd25b3b3d6d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019082"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="37c51-103">在庫設定の適用</span><span class="sxs-lookup"><span data-stu-id="37c51-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="37c51-104">このトピックでは在庫設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="37c51-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="37c51-105">在庫設定では、製品をカートに追加する前に在庫を確認するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="37c51-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="37c51-106">また、"在庫あり" や "残りわずか" などの在庫関連の販売促進メッセージも定義します。</span><span class="sxs-lookup"><span data-stu-id="37c51-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="37c51-107">これらの設定により、在庫切れの製品は購入できなくなります。</span><span class="sxs-lookup"><span data-stu-id="37c51-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="37c51-108">Dynamics 365 Commerce は、製品の手持在庫の見積を提供します。</span><span class="sxs-lookup"><span data-stu-id="37c51-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="37c51-109">見積済手持在庫の計算方法については、[小売チャンネルの引当可能在庫数量の計算](calculated-inventory-retail-channels.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37c51-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="37c51-110">Commerce サイト ビルダーでは、在庫のしきい値と範囲を製品またはカテゴリに対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="37c51-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="37c51-111">在庫を在庫あり、低在庫、または在庫切れに分類できるかを判定します。</span><span class="sxs-lookup"><span data-stu-id="37c51-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="37c51-112">詳細については、[在庫バッファーと在庫レベルのコンフィギュレーション](inventory-buffers-levels.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37c51-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="37c51-113">在庫のしきい値と範囲のサポートは、Dynamics 365 Commerce 10.0.12 リリースで利用できます。</span><span class="sxs-lookup"><span data-stu-id="37c51-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="37c51-114">在庫設定</span><span class="sxs-lookup"><span data-stu-id="37c51-114">Inventory settings</span></span>

<span data-ttu-id="37c51-115">Commerce では、在庫設定はサイト ビルダーの **サイト設定 \> 拡張機能 \> 在庫管理** で定義されています。</span><span class="sxs-lookup"><span data-stu-id="37c51-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="37c51-116">5 つの在庫設定があり、そのうちの 1 つは廃止されています (非推奨):</span><span class="sxs-lookup"><span data-stu-id="37c51-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="37c51-117">**アプリで在庫チェックを有効にする** – この設定により、製品の在庫確認が有効になります。</span><span class="sxs-lookup"><span data-stu-id="37c51-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="37c51-118">購入ボックス、カート、店舗で受け取り モジュールで製品在庫が確認され、在庫がある場合にのみ製品をカートに追加できるようになります。</span><span class="sxs-lookup"><span data-stu-id="37c51-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="37c51-119">**基準となる在庫レベル** – この設定では、在庫レベルの計算方法が定義されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="37c51-120">使用可能な値は、**引当可能合計数**、**引当可能現物数**、**在庫切れしきい** です。</span><span class="sxs-lookup"><span data-stu-id="37c51-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="37c51-121">Commerce では、在庫のしきい値と範囲を製品とカテゴリごとに定義できます。</span><span class="sxs-lookup"><span data-stu-id="37c51-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="37c51-122">在庫 API は、**引当可能合計数** プロパティと **引当可能現物数** プロパティ両方の製品在庫情報を返します。</span><span class="sxs-lookup"><span data-stu-id="37c51-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="37c51-123">小売業者は、**引当可能合計数** または **引当可能現物数** の値が、在庫数と在庫状況および在庫切れの状態に対応する範囲を決定するために使用されるべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="37c51-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="37c51-124">設定に **基準となる在庫レベル** の **在庫切れしきい** 値 は、古い (レガシ)、廃止値です。</span><span class="sxs-lookup"><span data-stu-id="37c51-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="37c51-125">選択すると、在庫数は **引当可能合計数** 値の結果から決定されますが、しきい値は、後で説明する **在庫切れしきい値** 数値設定によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="37c51-126">このしきい値の設定は、E コマース サイト全体のすべての製品に適用されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="37c51-127">在庫がしきい値数を下回ると、製品は在庫切れと見なされます。</span><span class="sxs-lookup"><span data-stu-id="37c51-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="37c51-128">それ以外の場合は、在庫ありと見なされます。</span><span class="sxs-lookup"><span data-stu-id="37c51-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="37c51-129">**在庫切れのしきい** 値の機能は制限されており、バージョン 10.0.12 以降で使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="37c51-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="37c51-130">**複数の倉庫の在庫レベル** – この設定により、既定の倉庫または複数の倉庫に対して在庫レベルを計算できます。</span><span class="sxs-lookup"><span data-stu-id="37c51-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="37c51-131">**個々の倉庫に基づく** オプションは、既定の倉庫に基づいて在庫レベルを計算します。</span><span class="sxs-lookup"><span data-stu-id="37c51-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="37c51-132">また、eコマース サイトでは、フルフィルメントを容易にするために複数の倉庫を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="37c51-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="37c51-133">この場合、**出荷倉庫と集荷倉庫の集計に基づく** オプションを使用して有効在庫数が示されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="37c51-134">たとえば、顧客が品目を購入し、配送方法として「配送」を選択した場合、その品目は、利用可能な在庫があるフルフィルメント グループのどの倉庫からでも出荷することができます。</span><span class="sxs-lookup"><span data-stu-id="37c51-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="37c51-135">製品の詳細ページ (PDP) では、フルフィルメント グループ内の出荷倉庫に在庫がある場合、出荷時に「在庫あり」のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="37c51-136">**複数の倉庫の在庫レベル** 設定は、Commerce バージョン 10.0.19 リリースで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="37c51-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="37c51-137">古いバージョンの Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37c51-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="37c51-138">手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37c51-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="37c51-139">**在庫範囲** – この設定では、メッセージがサイト モジュールに表示される在庫範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="37c51-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="37c51-140">これは、設定に **基準となる在庫レベル** で **引当可能合計数** 値または **引当可能現物数** 値のいずれかが選択されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="37c51-141">使用できる値は、**すべて**、**在庫が少なく在庫切れ**、**在庫切れ** です。</span><span class="sxs-lookup"><span data-stu-id="37c51-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="37c51-142">**すべて** を選択すると、在庫あり (" 使用可能" メッセージ) から 在庫切れ ("在庫切れ" メッセージ) まで、すべての在庫範囲のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="37c51-143">**在庫が少なく在庫切れ** を選択すると、在庫あり (" 使用可能" メッセージ) を除くすべての在庫範囲のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="37c51-144">**在庫切れ** を選択すると、"在庫切れ" メッセージのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37c51-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="37c51-145">**在庫切れしきい** – この古い数値設定は、**基準となる在庫レベル** 設定に対して **在庫切れしきい** 値が選択されている場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="37c51-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="37c51-146">これらの設定は、Dynamics 365 Commerce のリリース バージョン 10.0.12 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="37c51-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="37c51-147">古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37c51-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="37c51-148">appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="37c51-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="37c51-149">在庫設定を使用するモジュール</span><span class="sxs-lookup"><span data-stu-id="37c51-149">Modules that use inventory settings</span></span>

<span data-ttu-id="37c51-150">購入ボックス、欲しい物リスト、店舗セレクター、カート、買い物カゴ アイコン モジュールは、在庫設定を使用して、在庫範囲とメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="37c51-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="37c51-151">次の図の例では、PDP に在庫あり (「利用可」) メッセージが示されています。</span><span class="sxs-lookup"><span data-stu-id="37c51-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![在庫ありメッセージがある PDP モジュールの例](./media/pdp-InStock.png)

<span data-ttu-id="37c51-153">次の図の例では、PDP に「在庫なし」メッセージが示されています。</span><span class="sxs-lookup"><span data-stu-id="37c51-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![在庫切れメッセージがある PDP モジュールの例](./media/pdp-outofstock.png)

<span data-ttu-id="37c51-155">次の図の例では、カートに在庫あり (「利用可」) メッセージが示されています。</span><span class="sxs-lookup"><span data-stu-id="37c51-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![在庫ありメッセージがある買い物カゴモジュールの例](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="37c51-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="37c51-157">Additional resources</span></span>

[<span data-ttu-id="37c51-158">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="37c51-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="37c51-159">在庫バッファーと在庫レベルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="37c51-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="37c51-160">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="37c51-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="37c51-161">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="37c51-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="37c51-162">アカウント管理ページとモジュール</span><span class="sxs-lookup"><span data-stu-id="37c51-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="37c51-163">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="37c51-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="37c51-164">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="37c51-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
