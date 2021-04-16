---
title: オンライン注文用の消費税のコンフィギュレーション
description: このトピックでは、Dynamics 365 Commerce のさまざまなオンライン注文タイプに対する消費税グループの選択の概要を示します。
author: gvrmohanreddy
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 68b7e59a1e1ea18bdcd4e7a9117e4892407f40ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791850"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="d97f1-103">オンライン注文用の消費税のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d97f1-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d97f1-104">このトピックでは、さまざまなオンライン注文タイプに対する消費税グループの選択の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="d97f1-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="d97f1-105">電子商取引チャンネルでは、注文の配送や集配などのオプションをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d97f1-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="d97f1-106">消費税の適用は、オンライン ユーザーによって選択されたオプションに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="d97f1-107">サイト顧客が品目をオンラインで購入して住所に出荷することを選択した場合、その消費税は、顧客の出荷住所税グループ設定に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="d97f1-108">顧客が購買品目を店舗でピックアップすることを選択した場合、その消費税は、集配店舗の税グループ設定に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="d97f1-109">顧客住所への出荷注文</span><span class="sxs-lookup"><span data-stu-id="d97f1-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="d97f1-110">一般に、顧客の住所に送付されるオンライン注文の税は、宛先によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="d97f1-111">各消費税グループには、ビジネスが国/地域、都道府県、郡、市区町村などの出荷先の詳細を階層形式で定義できる、小売の宛先に基づく税コンフィギュレーションがあります。</span><span class="sxs-lookup"><span data-stu-id="d97f1-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="d97f1-112">オンライン注文が行われると、Commerce 税エンジンにより、その注文の各明細行品目の配送先住所が使用され、宛先に基づく税基準が一致する消費税グループが検索されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="d97f1-113">たとえば、明細行品目の配送先がカリフォルニア州サンフランシスコになっているオンライン注文では、税エンジンにより、カリフォルニア州の消費税グループと消費税コードが検出され、それに応じて明細行品目ごとに税金が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="d97f1-114">顧客ベースの税グループ</span><span class="sxs-lookup"><span data-stu-id="d97f1-114">Customer-based tax groups</span></span>

<span data-ttu-id="d97f1-115">Commerce 本社には、顧客税グループがコンフィギュレーションされている場所が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="d97f1-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="d97f1-116">**顧客のプロファイル**</span><span class="sxs-lookup"><span data-stu-id="d97f1-116">**Customer's profile**</span></span>
- <span data-ttu-id="d97f1-117">**顧客の出荷先住所**</span><span class="sxs-lookup"><span data-stu-id="d97f1-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="d97f1-118">顧客のプロファイルに税グループがコンフィギュレーションされている場合</span><span class="sxs-lookup"><span data-stu-id="d97f1-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="d97f1-119">本社の顧客プロファイル レコードに消費税グループがコンフィギュレーションされている場合がありますが、オンライン注文では、顧客のプロファイルでコンフィギュレーションされた消費税グループは、税エンジンによって使用されません。</span><span class="sxs-lookup"><span data-stu-id="d97f1-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="d97f1-120">顧客の出荷先住所に税グループがコンフィギュレーションされている場合</span><span class="sxs-lookup"><span data-stu-id="d97f1-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="d97f1-121">顧客の出荷先住所レコードに税グループがコンフィギュレーションされていて、オンライン注文 (または明細行品目) が顧客の出荷先住所に出荷される場合、顧客の住所レコードにコンフィギュレーションされている税グループは、税計算のために税エンジンによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="d97f1-122">顧客の出荷先住所レコードの税グループのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d97f1-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="d97f1-123">Commerce 本社の顧客の出荷先住所レコードに対する税グループをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d97f1-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d97f1-124">**すべての顧客** に移動し、目的の顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="d97f1-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="d97f1-125">**住所** クイックタブで、目的の住所を選択し、**その他のオプション \> 詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d97f1-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="d97f1-126">**住所の管理** ページの **全般** タブで、必要に応じ て消費税額を設定します。</span><span class="sxs-lookup"><span data-stu-id="d97f1-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="d97f1-127">税グループは、注文明細行の配送先住所を使用して定義され、宛先に基づく税は税グループ自体でコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="d97f1-128">詳細については、[宛先に基づくオンライン ストアのための税の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d97f1-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="d97f1-129">店舗での注文の受け取り</span><span class="sxs-lookup"><span data-stu-id="d97f1-129">Order pickup in store</span></span>

<span data-ttu-id="d97f1-130">店舗での受け取りまたはカーブサイド ピックアップが指定されている注文明細行の場合は、選択したピックアップ店舗の税グループが適用されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="d97f1-131">特定の店舗の税グループをコンフィギュレーションする方法の詳細については、[店舗のその他の税オプションの設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d97f1-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="d97f1-132">店舗で注文明細行がピックアップされると、顧客の住所の税設定 (設定されている場合) が税エンジンによって無視され、ピックアップ店舗の税コンフィギュレーションが適用されます。</span><span class="sxs-lookup"><span data-stu-id="d97f1-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d97f1-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d97f1-133">Additional resources</span></span>

[<span data-ttu-id="d97f1-134">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="d97f1-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

<span data-ttu-id="d97f1-135">[[発生元] フィールドでの消費税計算方法](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="d97f1-135">[Sales tax calculation methods in the Origin field](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json)</span></span> 

[<span data-ttu-id="d97f1-136">消費税の割り当ておよび上書き</span><span class="sxs-lookup"><span data-stu-id="d97f1-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="d97f1-137">消費税コードの合計額と間隔計算オプション</span><span class="sxs-lookup"><span data-stu-id="d97f1-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="d97f1-138">非課税の計算</span><span class="sxs-lookup"><span data-stu-id="d97f1-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]