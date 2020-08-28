---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661245"
---
# <a name="gift-card-module"></a><span data-ttu-id="b8a44-103">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8a44-104">このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b8a44-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b8a44-105">概要</span><span class="sxs-lookup"><span data-stu-id="b8a44-105">Overview</span></span>

<span data-ttu-id="b8a44-106">ギフト カードは一般的な支払形式であり、ギフト カード モジュールはチェックアウト モジュールで使用してギフト カードを受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="b8a44-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="b8a44-107">ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b8a44-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b8a44-108">SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="b8a44-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="b8a44-109">SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="b8a44-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="b8a44-110">以下の図は、精算ページにおけるギフト カード モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b8a44-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![ギフト カード モジュールの例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b8a44-112">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8a44-112">Module properties</span></span>

- <span data-ttu-id="b8a44-113">**追加フィールドの表示** - このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="b8a44-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b8a44-114">たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b8a44-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b8a44-115">または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b8a44-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b8a44-116">サポートされている値:</span><span class="sxs-lookup"><span data-stu-id="b8a44-116">Supported values:</span></span>
-   <span data-ttu-id="b8a44-117">暗証番号 (PIN)</span><span class="sxs-lookup"><span data-stu-id="b8a44-117">PIN</span></span>
-   <span data-ttu-id="b8a44-118">有効期限</span><span class="sxs-lookup"><span data-stu-id="b8a44-118">Expiration date</span></span>
-   <span data-ttu-id="b8a44-119">PIN と 有効期限</span><span class="sxs-lookup"><span data-stu-id="b8a44-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="b8a44-120">None</span><span class="sxs-lookup"><span data-stu-id="b8a44-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b8a44-121">ギフト カード モジュールのサイト設定</span><span class="sxs-lookup"><span data-stu-id="b8a44-121">Site settings for gift card modules</span></span>

<span data-ttu-id="b8a44-122">コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。</span><span class="sxs-lookup"><span data-stu-id="b8a44-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b8a44-123">この設定は 3 つの値をサポートします:</span><span class="sxs-lookup"><span data-stu-id="b8a44-123">This setting supports three values:</span></span>
- <span data-ttu-id="b8a44-124">**Dynamics 365 ギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8a44-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b8a44-125">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b8a44-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b8a44-126">**SVS と Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8a44-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b8a44-127">この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b8a44-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b8a44-128">**Dynamics 365、SVS、Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。</span><span class="sxs-lookup"><span data-stu-id="b8a44-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b8a44-129">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b8a44-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b8a44-130">ギフト カード モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="b8a44-130">Add a gift card module to a page</span></span>

<span data-ttu-id="b8a44-131">ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8a44-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8a44-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b8a44-132">Additional resources</span></span>

[<span data-ttu-id="b8a44-133">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b8a44-134">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b8a44-135">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b8a44-136">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b8a44-137">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b8a44-138">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b8a44-139">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="b8a44-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b8a44-140">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="b8a44-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
