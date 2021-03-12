---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9626f33ced0433bc96ed58429e95d4f75af6508
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980385"
---
# <a name="gift-card-module"></a><span data-ttu-id="b33ca-103">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b33ca-104">このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b33ca-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b33ca-105">概要</span><span class="sxs-lookup"><span data-stu-id="b33ca-105">Overview</span></span>

<span data-ttu-id="b33ca-106">ギフト カード モジュールは、精算モジュールで使用することができ、電子商取引で使用される一般的な支払い方法であるギフトカードを受け付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="b33ca-107">ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b33ca-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b33ca-108">SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="b33ca-109">SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b33ca-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b33ca-110">精算フロー中の SVS および Givex ギフトカードの引き換えは、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b33ca-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="b33ca-111">ギフト カード モジュールは2つ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="b33ca-112">**ギフト カード** - このモジュールは、精算ページで使用でき、支払/入金としてギフトカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="b33ca-113">**ギフト カードの残高** - このモジュールは、ギフトカードの残高を確認するために任意のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="b33ca-114">このモジュールは、コマースのリリース 10.0.14 およびこれ以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="b33ca-115">ギフトカード残高チェック モジュールのサポートは、Dynamics 365 Commerce の営々ース バージョン 10.0.14 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b33ca-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="b33ca-116">以下の図は、精算ページにおけるギフト カード モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b33ca-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![ギフト カード モジュールの例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b33ca-118">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="b33ca-118">Module properties</span></span>

- <span data-ttu-id="b33ca-119">**追加フィールドの表示** - このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="b33ca-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b33ca-120">たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b33ca-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b33ca-121">または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b33ca-122">サポートされている値:</span><span class="sxs-lookup"><span data-stu-id="b33ca-122">Supported values:</span></span>
-   <span data-ttu-id="b33ca-123">暗証番号 (PIN)</span><span class="sxs-lookup"><span data-stu-id="b33ca-123">PIN</span></span>
-   <span data-ttu-id="b33ca-124">有効期限</span><span class="sxs-lookup"><span data-stu-id="b33ca-124">Expiration date</span></span>
-   <span data-ttu-id="b33ca-125">PIN と 有効期限</span><span class="sxs-lookup"><span data-stu-id="b33ca-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="b33ca-126">None</span><span class="sxs-lookup"><span data-stu-id="b33ca-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b33ca-127">ギフト カード モジュールのサイト設定</span><span class="sxs-lookup"><span data-stu-id="b33ca-127">Site settings for gift card modules</span></span>

<span data-ttu-id="b33ca-128">コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。</span><span class="sxs-lookup"><span data-stu-id="b33ca-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b33ca-129">この設定は 3 つの値をサポートします:</span><span class="sxs-lookup"><span data-stu-id="b33ca-129">This setting supports three values:</span></span>
- <span data-ttu-id="b33ca-130">**Dynamics 365 ギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="b33ca-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b33ca-131">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b33ca-132">**SVS と Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="b33ca-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b33ca-133">この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b33ca-134">**Dynamics 365、SVS、Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b33ca-135">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b33ca-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b33ca-136">これらの設定は、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能であり 、SVS や Givex のギフトカードに対応する必要がある場合にのみ必要となります。</span><span class="sxs-lookup"><span data-stu-id="b33ca-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="b33ca-137">古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b33ca-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b33ca-138">appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="b33ca-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b33ca-139">ギフト カード モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="b33ca-139">Add a gift card module to a page</span></span>

<span data-ttu-id="b33ca-140">ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b33ca-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b33ca-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b33ca-141">Additional resources</span></span>

[<span data-ttu-id="b33ca-142">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b33ca-143">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b33ca-144">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b33ca-145">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b33ca-146">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b33ca-147">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b33ca-148">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b33ca-149">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="b33ca-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b33ca-150">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="b33ca-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="b33ca-151">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="b33ca-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
