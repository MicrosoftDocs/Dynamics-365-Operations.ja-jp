---
title: これを選択するのオプションがカートまたは製品の詳細ページに表示されません
description: このトピックでは、店舗内での集荷のオプションがカートページまたは製品の詳細ページに表示されない場合に役立つトラブルシューティングガイドを示します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585408"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="bff35-103">「これを選択する」のオプションがカートまたは製品の詳細ページに表示されません</span><span class="sxs-lookup"><span data-stu-id="bff35-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bff35-104">このトピックでは、店舗内での集荷のオプションがカートページまたは製品の詳細ページに表示されない場合に役立つトラブルシューティングガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="bff35-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="bff35-105">説明</span><span class="sxs-lookup"><span data-stu-id="bff35-105">Description</span></span>

<span data-ttu-id="bff35-106">**これを選択する** ボタンがカートまたは製品の詳細ページに表示されません。</span><span class="sxs-lookup"><span data-stu-id="bff35-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="bff35-107">次の図は、**これを選択する** ボタンを含むページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="bff35-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![これを選択するボタン](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="bff35-109">解像度</span><span class="sxs-lookup"><span data-stu-id="bff35-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="bff35-110">Commerce サイト ビルダーで BOPIS 拡張子を有効にする</span><span class="sxs-lookup"><span data-stu-id="bff35-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="bff35-111">Commerce サイト ビルダーの「オンラインで購入する、店舗で受け取る」(BOPIS) 拡張機能を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bff35-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bff35-112">サイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="bff35-112">Select your site.</span></span>
1. <span data-ttu-id="bff35-113">**サイトの設定** を選択し、**拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bff35-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="bff35-114">**BOPIS を無効にする** オプションがオフになっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bff35-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="bff35-115">Commerce 本社の出荷モードの構成</span><span class="sxs-lookup"><span data-stu-id="bff35-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="bff35-116">Commerce 本社の出荷モードの構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bff35-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="bff35-117">**調達 \> 設定 \> 配送モード** に順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bff35-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="bff35-118">**顧客の集荷** の配送モードが作成されており、製品と住所が割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bff35-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="bff35-119">**Retail と Commerce \> 本社の設定 \> パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bff35-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="bff35-120">左側のナビゲーションで、**顧客注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bff35-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="bff35-121">**配送の集荷モード** が適切に構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bff35-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="bff35-122">顧客注文支払の構成</span><span class="sxs-lookup"><span data-stu-id="bff35-122">Configure customer orders payments</span></span>

<span data-ttu-id="bff35-123">Commerce 本社で顧客注文支払を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bff35-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="bff35-124">**Retail と Commerce \> 本社の設定 \> パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bff35-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="bff35-125">左側のナビゲーションで、**顧客注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bff35-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="bff35-126">**支払** クイック タブで、**支払条件** および **支払方法** フィールドが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bff35-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bff35-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bff35-127">Additional resources</span></span>

[<span data-ttu-id="bff35-128">BOPIS の構成</span><span class="sxs-lookup"><span data-stu-id="bff35-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="bff35-129">顧客注文に対して複数の受け取り配送モードを有効にする</span><span class="sxs-lookup"><span data-stu-id="bff35-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="bff35-130">オムニチャネル Commerce 注文支払</span><span class="sxs-lookup"><span data-stu-id="bff35-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="bff35-131">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="bff35-131">Store selector module</span></span>](../store-selector.md)
