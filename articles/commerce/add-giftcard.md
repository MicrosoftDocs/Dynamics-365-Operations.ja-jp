---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962766"
---
# <a name="gift-card-module"></a><span data-ttu-id="93b43-103">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93b43-104">このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="93b43-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="93b43-105">ギフト カード モジュールは、精算モジュールで使用することができ、電子商取引で使用される一般的な支払い方法であるギフトカードを受け付けることができます。</span><span class="sxs-lookup"><span data-stu-id="93b43-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="93b43-106">ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="93b43-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="93b43-107">SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="93b43-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="93b43-108">SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93b43-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="93b43-109">精算フロー中の SVS および Givex ギフトカードの引き換えは、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="93b43-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="93b43-110">ギフト カード モジュールは2つ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93b43-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="93b43-111">**ギフト カード** – このモジュールは、精算ページで使用でき、支払/入金としてギフトカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93b43-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="93b43-112">**ギフト カードの残高** – このモジュールは、ギフトカードの残高を確認するために任意のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="93b43-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="93b43-113">このモジュールは、コマースのリリース 10.0.14 およびこれ以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="93b43-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="93b43-114">ギフトカード残高チェック モジュールのサポートは、Dynamics 365 Commerce の営々ース バージョン 10.0.14 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="93b43-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="93b43-115">以下の図は、精算ページにおけるギフト カード モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="93b43-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![ギフト カード モジュールの例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="93b43-117">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="93b43-117">Module properties</span></span>

- <span data-ttu-id="93b43-118">**追加フィールドの表示** – このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="93b43-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="93b43-119">たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="93b43-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="93b43-120">または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="93b43-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="93b43-121">サポートされている値:</span><span class="sxs-lookup"><span data-stu-id="93b43-121">Supported values:</span></span>
-   <span data-ttu-id="93b43-122">暗証番号 (PIN)</span><span class="sxs-lookup"><span data-stu-id="93b43-122">PIN</span></span>
-   <span data-ttu-id="93b43-123">有効期限</span><span class="sxs-lookup"><span data-stu-id="93b43-123">Expiration date</span></span>
-   <span data-ttu-id="93b43-124">PIN と 有効期限</span><span class="sxs-lookup"><span data-stu-id="93b43-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="93b43-125">None</span><span class="sxs-lookup"><span data-stu-id="93b43-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="93b43-126">ギフト カード モジュールのサイト設定</span><span class="sxs-lookup"><span data-stu-id="93b43-126">Site settings for gift card modules</span></span>

<span data-ttu-id="93b43-127">コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。</span><span class="sxs-lookup"><span data-stu-id="93b43-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="93b43-128">この設定は 3 つの値をサポートします:</span><span class="sxs-lookup"><span data-stu-id="93b43-128">This setting supports three values:</span></span>
- <span data-ttu-id="93b43-129">**Dynamics 365 ギフト カード** – この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="93b43-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="93b43-130">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="93b43-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="93b43-131">**SVS と Givex のギフト カード** – この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。</span><span class="sxs-lookup"><span data-stu-id="93b43-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="93b43-132">この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="93b43-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="93b43-133">**Dynamics 365、SVS、Givex のギフト カード** – この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。</span><span class="sxs-lookup"><span data-stu-id="93b43-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="93b43-134">この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="93b43-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93b43-135">これらの設定は、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能であり 、SVS や Givex のギフトカードに対応する必要がある場合にのみ必要となります。</span><span class="sxs-lookup"><span data-stu-id="93b43-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="93b43-136">古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93b43-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="93b43-137">appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="93b43-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="93b43-138">電子商取引店舗で使用する内部ギフト カードの拡張</span><span class="sxs-lookup"><span data-stu-id="93b43-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="93b43-139">既定では、内部ギフト カードは電子商取引店舗で使用するのに最適化されていません。</span><span class="sxs-lookup"><span data-stu-id="93b43-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="93b43-140">したがって、内部ギフト カードを支払に使用できるようにする前に、セキュリティを向上させる拡張機能を使用して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93b43-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="93b43-141">内部ギフト カードを運用で使用できるようにする前に拡張する必要があるギフト カード領域を次に示します。</span><span class="sxs-lookup"><span data-stu-id="93b43-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="93b43-142">**ギフト カード番号** – 番号順序は、内部ギフト カードにギフト カード番号を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93b43-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="93b43-143">番号順序は簡単に予測できるので、ギフト カード番号の生成を拡張し、発行されるギフト カード番号に対してランダムで暗号化された安全な文字列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93b43-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="93b43-144">**GetBalance** – **GetBalance** API はギフト カードの残高を検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93b43-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="93b43-145">既定では、この API は公開されています。</span><span class="sxs-lookup"><span data-stu-id="93b43-145">By default, this API public.</span></span> <span data-ttu-id="93b43-146">ギフト カードの残高を検索するのに PIN が必要でない場合、ブルートフォース攻撃が **GetBalance** API を使用し、残高のあるギフト カード番号を検索しようとするリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="93b43-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="93b43-147">内部ギフト カードの PIN 要件と API 調整の両方の実装は、リスクを軽減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="93b43-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="93b43-148">**PIN** – 既定では、内部ギフト カードでは PIN はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="93b43-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="93b43-149">残高の検索に PIN が必要となるようにするために、内部ギフト カードを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93b43-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="93b43-150">この機能を使用して、誤った PIN 入力を連続して試行した後でギフト カードをロックすることもできます。</span><span class="sxs-lookup"><span data-stu-id="93b43-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="93b43-151">ゲスト チェックアウトに対するギフト カードの支払を有効にする</span><span class="sxs-lookup"><span data-stu-id="93b43-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="93b43-152">既定では、ゲスト (匿名) のチェックアウトに対してギフト カードの支払は有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="93b43-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="93b43-153">有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="93b43-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="93b43-154">Commerce 本部で、**Retail と Commerce \> チャネルの設定 \> POS 設定 \> POS \> POS 操作** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="93b43-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="93b43-155">グリッドのヘッダーを選択したまま (または右クリック)、**列を挿入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93b43-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="93b43-156">**列を挿入** ダイアログ ボックスで、**AllowAnonymousAccess** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="93b43-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="93b43-157">**更新プログラム** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93b43-157">Select **Update**.</span></span>
1. <span data-ttu-id="93b43-158">操作 **520** (ギフト カード残高) および **214** の場合、**AllowAnonymousAccess** の値を **1** に設定します。</span><span class="sxs-lookup"><span data-stu-id="93b43-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="93b43-159">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93b43-159">Select **Save**.</span></span>
1. <span data-ttu-id="93b43-160">チャネル データベースへ変更を同期するために、**1090** スケジューラ ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="93b43-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="93b43-161">ギフト カード モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="93b43-161">Add a gift card module to a page</span></span>

<span data-ttu-id="93b43-162">ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93b43-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93b43-163">追加リソース</span><span class="sxs-lookup"><span data-stu-id="93b43-163">Additional resources</span></span>

[<span data-ttu-id="93b43-164">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="93b43-165">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="93b43-166">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="93b43-167">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="93b43-168">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="93b43-169">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="93b43-170">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="93b43-171">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="93b43-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="93b43-172">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="93b43-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="93b43-173">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="93b43-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
