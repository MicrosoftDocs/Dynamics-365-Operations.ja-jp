---
title: 電子商取引のデジタル ギフト カード
description: Microsoft Dynamics 365 Commerce の電子商取引の実装におけるデジタル ギフト カードの機能について説明します。 重要な構成の手順の概要についても説明しています。
author: anupamar-ms
ms.date: 12/15/2020
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
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: bd93744cf947dcc343d2b31d3d52b2b748c062a9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792874"
---
# <a name="e-commerce-digital-gift-cards"></a><span data-ttu-id="438f8-104">電子商取引のデジタル ギフト カード</span><span class="sxs-lookup"><span data-stu-id="438f8-104">E-commerce digital gift cards</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="438f8-105">Microsoft Dynamics 365 Commerce の電子商取引の実装におけるデジタル ギフト カードの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="438f8-105">This topic describes how digital gift cards work in the e-commerce implementation of Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="438f8-106">重要な構成の手順の概要についても説明しています。</span><span class="sxs-lookup"><span data-stu-id="438f8-106">It also provides an overview of important configuration steps.</span></span>

<span data-ttu-id="438f8-107">Dynamics 365 Commerce では、デジタル ギフト カードの購入は、システ内のその他製品の購入と同じフローです。</span><span class="sxs-lookup"><span data-stu-id="438f8-107">In Dynamics 365 Commerce, the purchase of digital gift cards follows the same flow as the purchase of other products in the system.</span></span> <span data-ttu-id="438f8-108">追加のモジュールを構成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="438f8-108">No additional modules have to be configured.</span></span> <span data-ttu-id="438f8-109">複数のギフト カードをカートに追加した場合、そのギフト カード品目は1つの販売行には集計されません。</span><span class="sxs-lookup"><span data-stu-id="438f8-109">If multiple gift cards are added to the cart, the gift card items aren't aggregated on a single sales line.</span></span> <span data-ttu-id="438f8-110">この動作は、各販売の明細行が個別のギフト カード番号を使用して請求を行うため必要となります。</span><span class="sxs-lookup"><span data-stu-id="438f8-110">This behavior is required because each sales line is invoiced by using a separate gift card number.</span></span>

<span data-ttu-id="438f8-111">デジタル ギフト カードの購入は Dynamics 365 Commerce 10.0.16 以降でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="438f8-111">The purchase of digital gift cards is supported in the Dynamics 365 Commerce 10.0.16 release and later.</span></span>

<span data-ttu-id="438f8-112">次の図は、Fabrikam の電子商取引サイトのデジタル ギフト カードの製品詳細ページ (PDP) の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="438f8-112">The following illustration shows an example of the product details page (PDP) for a digital gift card on the Fabrikam e-commerce site.</span></span>

![Fabrikam 電子商取引サイトのデジタル ギフト カード PDP の例](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a><span data-ttu-id="438f8-114">Commerce 本部のデジタル ギフト カード機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="438f8-114">Turn on the digital gift card feature in Commerce headquarters</span></span>

<span data-ttu-id="438f8-115">デジタル ギフト カードの購入フローを Dynamics 365 Commerce で実行するには、Commerce 本部で **電子商取引機能の購買ギフト カード** 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-115">For the purchase flow for digital gift cards to work in Dynamics 365 Commerce, the **Purchasing gift card on e-Commerce feature** feature must be turned on in Commerce headquarters.</span></span> <span data-ttu-id="438f8-116">Commerce 本部の **機能管理** ワークスペースには、以下の図のような特徴があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-116">You can find the feature in the **Feature management** workspace in Commerce headquarters, as shown in the following illustration.</span></span>

![Commerce 本部の機能管理ワークスペース](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a><span data-ttu-id="438f8-118">Commerce 本部のデジタル ギフト カードを構成する</span><span class="sxs-lookup"><span data-stu-id="438f8-118">Configure a digital gift card in Commerce headquarters</span></span>

<span data-ttu-id="438f8-119">デジタル ギフトカード製品は Commerce 本部で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-119">Digital gift card products should be configured in Commerce headquarters.</span></span> <span data-ttu-id="438f8-120">このプロセスは、他の製品のプロセスと共通しています。</span><span class="sxs-lookup"><span data-stu-id="438f8-120">The process resembles the process for other products.</span></span> <span data-ttu-id="438f8-121">ただし、次の重要な手順は、購買用ギフト カードの構成に固有のものです。</span><span class="sxs-lookup"><span data-stu-id="438f8-121">However, the following important steps are specific to the configuration of gift cards for purchase.</span></span> <span data-ttu-id="438f8-122">製品の作成および構成方法の詳細については、[Commerce で新製品を作成する](create-new-product-commerce.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-122">For more information about how to create and configure products, see [Create a new product in Commerce](create-new-product-commerce.md).</span></span>

- <span data-ttu-id="438f8-123">**新しい製品** ダイアログ ボックスでデジタル ギフト カード製品を構成する場合は、**製品タイプ** フィールドを **サービス** に設定します。</span><span class="sxs-lookup"><span data-stu-id="438f8-123">When you configure digital gift card products in the **New product** dialog box, set the **Product type** field to **Service**.</span></span> <span data-ttu-id="438f8-124">(ダイアログ ボックスを開くには、 **小売およびコマース \> 製品とカテゴリ \> カテゴリ別製品** に移動し、**新規** を選択します。) **サービス** タイプの商品は、注文を行う前に利用可能な在庫が確認されません。</span><span class="sxs-lookup"><span data-stu-id="438f8-124">(To open the dialog box, go to **Retail and commerce \> Products and categories \> Products by category**, and select **New**.) Products of the **Service** type aren't checked for available inventory before an order is placed.</span></span> <span data-ttu-id="438f8-125">詳細については、[新しい製品の作成](create-new-product-commerce.md#create-a-new-product) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-125">For more information, see [Create a new product](create-new-product-commerce.md#create-a-new-product).</span></span>
- <span data-ttu-id="438f8-126">**コマース パラメーター** ページの **転記** タブで、次の図に示すように、**ギフト カード製品** フィールドを **デジタル ギフト カード** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-126">On the **Commerce parameters** page, on the **Posting** tab, the **Gift card product** field must be set to **Digital Gift Card**, as shown in the following illustration.</span></span> <span data-ttu-id="438f8-127">商品が外部ギフトカードの場合は、[外部ギフト カードへの対応](./dev-itpro/gift-card.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-127">If the product is an external gift card, see [Support for external gift cards](./dev-itpro/gift-card.md) for more information.</span></span>

    ![Commerce 本部のギフト カード製品フィールド](./media/PostGiftcard.png)

- <span data-ttu-id="438f8-129">ギフト カードで、定義済の複数の金額 ($25、$50、$100 など) に対応する必要がある場合は、**サイズ** 分析コードを使用して、定義済金額を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-129">If a gift card must support multiple predefined amounts (for example, $25, $50, and $100), the **Size** dimension should be used to set up those predefined amounts.</span></span> <span data-ttu-id="438f8-130">定義済の各金額はバリアント型です。</span><span class="sxs-lookup"><span data-stu-id="438f8-130">Each predefined amount will be a variant.</span></span> <span data-ttu-id="438f8-131">詳細については、[製品分析コード](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-131">For more information, see [Product dimensions](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).</span></span>
- <span data-ttu-id="438f8-132">顧客がギフト カードのカスタム金額を指定できるようにする必要がある場合は、最初にカスタム金額を許可するバリアントを設定します。</span><span class="sxs-lookup"><span data-stu-id="438f8-132">If customers must be able to specify a custom amount for a gift card, first set up a variant that allows for a custom amount.</span></span> <span data-ttu-id="438f8-133">次に、**カテゴリ内のリリース済み製品** ページで製品を開き、 **Commerce** クイックタブで、**価格のキー** フィールドを、次の図に示すように **新しい価格内の必須キー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="438f8-133">Next, open the product from the **Released products in category** page, and then, on the **Commerce** FastTab, set the **Key in price** field to **Must key in new price**, as shown in the following illustration.</span></span> <span data-ttu-id="438f8-134">この設定により、顧客が PDP で製品を参照する際に価格を入力できます。</span><span class="sxs-lookup"><span data-stu-id="438f8-134">This setting ensures that customers can enter a price when they browse the product on a PDP.</span></span>

    ![Commerce 本部の価格フィールドのキー](./media/KeyInPrice.png)

- <span data-ttu-id="438f8-136">デジタル ギフト カードの配信モードを **電子** に設定する 必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-136">The mode of delivery for a digital gift card must be set to **Electronic**.</span></span> <span data-ttu-id="438f8-137">**配送方法** ページ (**小売およびコマース  \> チャネルの設定 \> 配送方法**) で、一覧ペインで配送方法に **電子** を選択し、 次の図に示すように、**製品** クイックタブでグリッドにデジタル ギフト カード製品を追加します。</span><span class="sxs-lookup"><span data-stu-id="438f8-137">On the **Modes of delivery** page (**Retail and commerce \> Channel setup \> Modes of delivery**), select the **Electronic** mode of delivery in the list pane, and then add the digital gift card product to the grid on the **Products** FastTab, as shown in the following illustration.</span></span> <span data-ttu-id="438f8-138">詳細については、[配送方法の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-138">For more information, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

    ![Commerce 本部の配信モードページのデジタル ギフトカード商品](./media/ElectronicMode.PNG)

- <span data-ttu-id="438f8-140">オンライン機能プロファイルが作成され、Commerce 本部のオンライン ストアに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-140">Make sure that an online functionality profile has been created and associated with your online store in Commerce headquarters.</span></span> <span data-ttu-id="438f8-141">機能プロファイルで、**製品の集計** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="438f8-141">In the functionality profile, set the **Aggregate products** option to **Yes**.</span></span> <span data-ttu-id="438f8-142">この設定により、ギフト カードを除くすべての品目が集計されます。</span><span class="sxs-lookup"><span data-stu-id="438f8-142">This setting ensures that all items except gift cards are aggregated.</span></span> <span data-ttu-id="438f8-143">詳細については、[オンライン機能プロファイルの作成](online-functionality-profile.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-143">For more information, see [Create an online functionality profile](online-functionality-profile.md).</span></span>
- <span data-ttu-id="438f8-144">ギフト カードの請求後に顧客にメールが届くようにするには、**電子メール通知プロファイル** ページに新しいメール通知タイプを作成し、**電子メール通知タイプ** フィールドを **ギフト カードの発行** に設定します。</span><span class="sxs-lookup"><span data-stu-id="438f8-144">To ensure that customers receive an email after a gift card is invoiced, create a new email notification type on the **Email notification profiles** page, and set the **Email notification type** field to **Issue gift card**.</span></span> <span data-ttu-id="438f8-145">詳細については、[電子メールの通知プロファイルの設定](email-notification-profiles.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-145">For more information, see [Set up an email notification profile](email-notification-profiles.md).</span></span>

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a><span data-ttu-id="438f8-146">Commerce サイト ビルダー メディア ライブラリに製品画像を追加する</span><span class="sxs-lookup"><span data-stu-id="438f8-146">Add product images to the Commerce site builder Media library</span></span>

<span data-ttu-id="438f8-147">デジタル ギフト カード製品の製品イメージを Commerce サイト ビルダのメディア ライブラリに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-147">You must add product images for digital gift card products to the Commerce site builder Media library.</span></span> <span data-ttu-id="438f8-148">ギフト カード イメージ ファイルのファイル名が、製品イメージのサイトの命名規則に従っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-148">Make sure that the file names of the gift card image files follow your site's naming conventions for product images.</span></span> <span data-ttu-id="438f8-149">詳細については、[画像のアップロード](dam-upload-images.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="438f8-149">For more information, see [Upload images](dam-upload-images.md).</span></span>

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a><span data-ttu-id="438f8-150">Commerce サイト ビルダでデジタル ギフト カードのカスタム金額を構成する</span><span class="sxs-lookup"><span data-stu-id="438f8-150">Configure a custom amount for a digital gift card in Commerce site builder</span></span>

<span data-ttu-id="438f8-151">デジタル ギフト カードがカスタム金額を許容するように構成されている場合は、この動作は、サイトの PDP で使用される [購入ボックス モジュール](add-buy-box.md) でも有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-151">If a digital gift card is configured to allow for a custom amount, this behavior must also be enabled in the [buy box module](add-buy-box.md) that is used on your site's PDPs.</span></span> <span data-ttu-id="438f8-152">購入ボックス モジュールは、カスタム金額を許可するモジュールの構成に対応しています。</span><span class="sxs-lookup"><span data-stu-id="438f8-152">The buy box module supports module configuration to allow for custom amounts.</span></span> <span data-ttu-id="438f8-153">また、カスタム金額に対して許可される最小額と最大金額を定義できます。</span><span class="sxs-lookup"><span data-stu-id="438f8-153">You can also define the minimum and maximum amounts that are allowed for custom amounts.</span></span>

<span data-ttu-id="438f8-154">Commerce サイト ビルダでデジタル ギフト カードのカスタム金額を構成します。</span><span class="sxs-lookup"><span data-stu-id="438f8-154">To configure a custom amount for a digital gift card in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="438f8-155">サイトの PDP で使用されている [購入ボックス モジュール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="438f8-155">Go to the buy box module that is used on your site's PDPs.</span></span> <span data-ttu-id="438f8-156">この購入ボックス モジュールは、フラグメント、テンプレート、またはページで実装されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="438f8-156">This buy box module might be implemented in a fragment, in a template, or on a page.</span></span>
1. <span data-ttu-id="438f8-157">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="438f8-157">Select **Edit**.</span></span>
1. <span data-ttu-id="438f8-158">右側のプロパティ ウィンドウで、**カスタム価格を許可する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="438f8-158">In the properties pane on the right, select the **Allow custom price** check box.</span></span>
1. <span data-ttu-id="438f8-159">オプション : カスタム金額の最小金額と最大金額を定義するには、**最大価格** と **最小価格** に金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="438f8-159">Optional: To define minimum and maximum amounts for custom amounts, enter amounts under **Minimum price** and **Maximum price**.</span></span>
1. <span data-ttu-id="438f8-160">**編集の終了** を選択し、**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="438f8-160">Select **Finish editing**, and then select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="438f8-161">追加リソース</span><span class="sxs-lookup"><span data-stu-id="438f8-161">Additional resources</span></span>

[<span data-ttu-id="438f8-162">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="438f8-162">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="438f8-163">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="438f8-163">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="438f8-164">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="438f8-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="438f8-165">Commerce での新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="438f8-165">Create a new product in Commerce</span></span>](create-new-product-commerce.md)

[<span data-ttu-id="438f8-166">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="438f8-166">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="438f8-167">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="438f8-167">Product dimensions</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[<span data-ttu-id="438f8-168">電子メール通知プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="438f8-168">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="438f8-169">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="438f8-169">Create an online functionality profile</span></span>](online-functionality-profile.md)

[<span data-ttu-id="438f8-170">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="438f8-170">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]