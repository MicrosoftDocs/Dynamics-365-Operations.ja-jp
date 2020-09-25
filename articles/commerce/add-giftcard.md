---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761084"
---
# <a name="gift-card-module"></a><span data-ttu-id="05a52-103">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="05a52-104">このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="05a52-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="05a52-105">概要</span><span class="sxs-lookup"><span data-stu-id="05a52-105">Overview</span></span>

<span data-ttu-id="05a52-106">ギフト カード モジュールは、精算モジュールで使用することができ、電子商取引で使用される一般的な支払い方法であるギフトカードを受け付けることができます。</span><span class="sxs-lookup"><span data-stu-id="05a52-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="05a52-107">ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="05a52-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="05a52-108">SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="05a52-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="05a52-109">SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05a52-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="05a52-110">ギフト カード モジュールは2つ使用できます。</span><span class="sxs-lookup"><span data-stu-id="05a52-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="05a52-111">**ギフト カード** - このモジュールは、精算ページで使用でき、支払/入金としてギフトカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="05a52-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="05a52-112">**ギフト カードの残高** - このモジュールは、ギフトカードの残高を確認するために任意のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="05a52-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="05a52-113">このモジュールは、コマースのリリース 10.0.14 およびこれ以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="05a52-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="05a52-114">以下の図は、精算ページにおけるギフト カード モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="05a52-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![ギフト カード モジュールの例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="05a52-116">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="05a52-116">Module properties</span></span>

- <span data-ttu-id="05a52-117">**追加フィールドの表示** - このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="05a52-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="05a52-118">たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="05a52-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="05a52-119">または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="05a52-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="05a52-120">サポートされている値:</span><span class="sxs-lookup"><span data-stu-id="05a52-120">Supported values:</span></span>
-   <span data-ttu-id="05a52-121">暗証番号 (PIN)</span><span class="sxs-lookup"><span data-stu-id="05a52-121">PIN</span></span>
-   <span data-ttu-id="05a52-122">有効期限</span><span class="sxs-lookup"><span data-stu-id="05a52-122">Expiration date</span></span>
-   <span data-ttu-id="05a52-123">PIN と 有効期限</span><span class="sxs-lookup"><span data-stu-id="05a52-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="05a52-124">None</span><span class="sxs-lookup"><span data-stu-id="05a52-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="05a52-125">ギフト カード モジュールのサイト設定</span><span class="sxs-lookup"><span data-stu-id="05a52-125">Site settings for gift card modules</span></span>

<span data-ttu-id="05a52-126">コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。</span><span class="sxs-lookup"><span data-stu-id="05a52-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="05a52-127">この設定は 3 つの値をサポートします:</span><span class="sxs-lookup"><span data-stu-id="05a52-127">This setting supports three values:</span></span>
- <span data-ttu-id="05a52-128">**Dynamics 365 ギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="05a52-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="05a52-129">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="05a52-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="05a52-130">**SVS と Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="05a52-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="05a52-131">この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="05a52-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="05a52-132">**Dynamics 365、SVS、Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。</span><span class="sxs-lookup"><span data-stu-id="05a52-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="05a52-133">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="05a52-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="05a52-134">ギフト カード モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="05a52-134">Add a gift card module to a page</span></span>

<span data-ttu-id="05a52-135">ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05a52-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05a52-136">追加リソース</span><span class="sxs-lookup"><span data-stu-id="05a52-136">Additional resources</span></span>

[<span data-ttu-id="05a52-137">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="05a52-138">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="05a52-139">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="05a52-140">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="05a52-141">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="05a52-142">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="05a52-143">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="05a52-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="05a52-144">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="05a52-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
