---
title: B2B eコマース サイトの製品数量制限の設定
description: このトピックでは、企業間 (B2B) の eコマースサイトに対して製品の数量制限を設定する方法について説明します。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e9f14bc9aa6586e87f3e8ccb82e63d0ec2e46534
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799784"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="7fe1a-103">B2B eコマース サイトの製品数量制限の設定</span><span class="sxs-lookup"><span data-stu-id="7fe1a-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7fe1a-104">このトピックでは、企業間 (B2B) の eコマースサイトに対して製品の数量制限を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="7fe1a-105">ほとんどの製品には、グループ化を定義する単位を持っています。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="7fe1a-106">このグループは、製品の販売方法に影響します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="7fe1a-107">商品によっては、数量のグループが追加されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="7fe1a-108">このグループにより、製品を個別の単位として販売できるか、複数の単位として販売できるか、また、従う必要がある最小または最大の注文数量制限があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="7fe1a-109">数量制限機能を使用することで、Microsoft Dynamics 365 Commerce で設定されている最小、最大、複数、標準の数量 (既定の注文設定または Commerce サイト ビルダーのサイト設定) が、eコマースで発注された顧客の注文に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="7fe1a-110">製品数量の制限は、販売時点管理 (POS) およびコール センターでは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="7fe1a-111">多くの小売業者は、様々な製品や条件を満たすための顧客注文 (特別注文と呼ばれる場合もあります) のオプションを提供しています。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="7fe1a-112">以下に一般的なシナリオを挙げます。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="7fe1a-113">顧客は、特定のバリエーションの製品をいくつかの倍数で販売したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="7fe1a-114">顧客は、その製品を購入した店舗または場所とは異なる店舗または場所から製品の集荷を希望しています。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="7fe1a-115">しかし、店舗の梱包基準は、オンライン販売流通の梱包基準とは異なります。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="7fe1a-116">顧客は、購入できる商品の数量に上限がある限定商品を購入したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="7fe1a-117">Commerce 本部の既定の注文設定機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="7fe1a-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="7fe1a-118">商品の数量制限を設定する前に、Commerce 本部で既定の注文設定機能をオンにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="7fe1a-119">既定の注文設定機能を有効にするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="7fe1a-120">**システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="7fe1a-121">**顧客注文でサイトと既定の注文設定をサポートする** 機能を探して選択します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="7fe1a-122">右ウィンドウの下で、**今すぐ有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="7fe1a-123">数量設定の定義</span><span class="sxs-lookup"><span data-stu-id="7fe1a-123">Define quantity settings</span></span> 

<span data-ttu-id="7fe1a-124">**既定の注文設定** ページで、数量の設定を定義できます。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="7fe1a-125">数量設定を定義するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="7fe1a-126">製品 **小売りとコマース \> 製品とカテゴリー \> カテゴリー別に製品を販売する** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="7fe1a-127">リリース済製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-127">Select a released product.</span></span>
1. <span data-ttu-id="7fe1a-128">アクション ペインで、**在庫の管理** タブの **注文設定** グループで、**既定の注文設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="7fe1a-129">**既定の注文設定** ページの **販売注文** クイック タブの **販売数量**  セクションで、製品の販売数量を設定します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="7fe1a-130">**複数** - 製品を複数の数量で購入できます。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="7fe1a-131">**最小注文数量** - 購入する必要がある製品の最小数です。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="7fe1a-132">**最大注文数量** - 購入可能な製品の最大数量です。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="7fe1a-133">**標準注文数量** - 商品選択時に自動的に入力される既定の数量です。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="7fe1a-134">Commerce サイトビルダーの B2B 注文数量制限機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="7fe1a-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="7fe1a-135">Commerce サイトビルダーの B2B 注文数量制限機能を有効にするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7fe1a-136">**サイト 設定 \> 拡張機能** に移動します</span><span class="sxs-lookup"><span data-stu-id="7fe1a-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="7fe1a-137">**注文数量制限の有効化** で、ドロップダウン メニューの **B2B 顧客に対して有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="7fe1a-138">更新されたサイトビルダーの設定は、app.settings.json ファイルが更新された後にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="7fe1a-139">詳細については、[SDK およびモジュール ライブラリの更新プログラム](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7fe1a-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fe1a-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7fe1a-140">Additional resources</span></span>

[<span data-ttu-id="7fe1a-141">B2B eコマース サイトの設定</span><span class="sxs-lookup"><span data-stu-id="7fe1a-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="7fe1a-142">B2B 組織の組織モデリング階層の作成</span><span class="sxs-lookup"><span data-stu-id="7fe1a-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="7fe1a-143">B2B eコマース サイトでのビジネス パートナー ユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="7fe1a-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="7fe1a-144">B2B eコマース サイト用の顧客アカウントの支払方法の構成</span><span class="sxs-lookup"><span data-stu-id="7fe1a-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]