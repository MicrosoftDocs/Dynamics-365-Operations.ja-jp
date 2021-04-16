---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797674"
---
# <a name="gift-card-module"></a><span data-ttu-id="b69f2-103">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b69f2-104">このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b69f2-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b69f2-105">ギフト カード モジュールは、精算モジュールで使用することができ、電子商取引で使用される一般的な支払い方法であるギフトカードを受け付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="b69f2-106">ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b69f2-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b69f2-107">SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="b69f2-108">SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b69f2-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b69f2-109">精算フロー中の SVS および Givex ギフトカードの引き換えは、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b69f2-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="b69f2-110">ギフト カード モジュールは2つ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="b69f2-111">**ギフト カード** - このモジュールは、精算ページで使用でき、支払/入金としてギフトカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="b69f2-112">**ギフト カードの残高** - このモジュールは、ギフトカードの残高を確認するために任意のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="b69f2-113">このモジュールは、コマースのリリース 10.0.14 およびこれ以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="b69f2-114">ギフトカード残高チェック モジュールのサポートは、Dynamics 365 Commerce の営々ース バージョン 10.0.14 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b69f2-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="b69f2-115">以下の図は、精算ページにおけるギフト カード モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b69f2-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![ギフト カード モジュールの例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b69f2-117">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="b69f2-117">Module properties</span></span>

- <span data-ttu-id="b69f2-118">**追加フィールドの表示** - このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="b69f2-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b69f2-119">たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b69f2-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b69f2-120">または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b69f2-121">サポートされている値:</span><span class="sxs-lookup"><span data-stu-id="b69f2-121">Supported values:</span></span>
-   <span data-ttu-id="b69f2-122">暗証番号 (PIN)</span><span class="sxs-lookup"><span data-stu-id="b69f2-122">PIN</span></span>
-   <span data-ttu-id="b69f2-123">有効期限</span><span class="sxs-lookup"><span data-stu-id="b69f2-123">Expiration date</span></span>
-   <span data-ttu-id="b69f2-124">PIN と 有効期限</span><span class="sxs-lookup"><span data-stu-id="b69f2-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="b69f2-125">None</span><span class="sxs-lookup"><span data-stu-id="b69f2-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b69f2-126">ギフト カード モジュールのサイト設定</span><span class="sxs-lookup"><span data-stu-id="b69f2-126">Site settings for gift card modules</span></span>

<span data-ttu-id="b69f2-127">コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。</span><span class="sxs-lookup"><span data-stu-id="b69f2-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b69f2-128">この設定は 3 つの値をサポートします:</span><span class="sxs-lookup"><span data-stu-id="b69f2-128">This setting supports three values:</span></span>
- <span data-ttu-id="b69f2-129">**Dynamics 365 ギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="b69f2-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b69f2-130">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b69f2-131">**SVS と Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="b69f2-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b69f2-132">この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b69f2-133">**Dynamics 365、SVS、Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b69f2-134">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b69f2-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b69f2-135">これらの設定は、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能であり 、SVS や Givex のギフトカードに対応する必要がある場合にのみ必要となります。</span><span class="sxs-lookup"><span data-stu-id="b69f2-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="b69f2-136">古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b69f2-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b69f2-137">appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="b69f2-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b69f2-138">ギフト カード モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="b69f2-138">Add a gift card module to a page</span></span>

<span data-ttu-id="b69f2-139">ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b69f2-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b69f2-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b69f2-140">Additional resources</span></span>

[<span data-ttu-id="b69f2-141">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b69f2-142">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b69f2-143">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b69f2-144">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b69f2-145">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b69f2-146">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b69f2-147">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b69f2-148">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="b69f2-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b69f2-149">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="b69f2-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="b69f2-150">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="b69f2-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]