---
title: 注文確認モジュール
description: このトピックでは、注文確認モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 407fc2724d4b589ef5f611974f9358e879dba7ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257150"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="d5552-103">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5552-104">このトピックでは、注文確認モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d5552-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d5552-105">注文確認モジュールを使用して、注文が行われた後、注文確認の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="d5552-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="d5552-106">注文の確認 ID、注文の連絡先情報、およびその他の注文の詳細 (購入された品目、支払情報、集荷オプション、出荷方法など) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5552-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="d5552-107">注文確認モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="d5552-107">Order confirmation module properties</span></span>

| <span data-ttu-id="d5552-108">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="d5552-108">Property name</span></span>  | <span data-ttu-id="d5552-109">値</span><span class="sxs-lookup"><span data-stu-id="d5552-109">Values</span></span> | <span data-ttu-id="d5552-110">説明</span><span class="sxs-lookup"><span data-stu-id="d5552-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d5552-111">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="d5552-111">Heading</span></span>        | <span data-ttu-id="d5552-112">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="d5552-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d5552-113">注文確認モジュールには、ヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d5552-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="d5552-114">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5552-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="d5552-115">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d5552-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="d5552-116">連絡先番号</span><span class="sxs-lookup"><span data-stu-id="d5552-116">Contact number</span></span> | <span data-ttu-id="d5552-117">テキスト</span><span class="sxs-lookup"><span data-stu-id="d5552-117">Text</span></span> | <span data-ttu-id="d5552-118">連絡先番号は、注文に関連する質問に対して発行できます。</span><span class="sxs-lookup"><span data-stu-id="d5552-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="d5552-119">集荷時間帯情報の表示</span><span class="sxs-lookup"><span data-stu-id="d5552-119">Show pickup timeslot information</span></span> | <span data-ttu-id="d5552-120">True または False</span><span class="sxs-lookup"><span data-stu-id="d5552-120">True or False</span></span> | <span data-ttu-id="d5552-121">このプロパティは Dynamics 365 Commerce、10.0.15 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5552-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="d5552-122">True の場合は、集荷品目に対して集荷の時間帯情報が表示されます</span><span class="sxs-lookup"><span data-stu-id="d5552-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="d5552-123">注文確認ページで使用可能なモジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="d5552-124">注文確認ページを作成するときに、注文確認モジュールに加えて、他の関連モジュールを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="d5552-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="d5552-125">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="d5552-125">Here are some examples:</span></span>

- <span data-ttu-id="d5552-126">**推奨モジュール** – 推奨モジュールを注文確認ページに追加して、顧客に他の製品を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="d5552-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="d5552-127">**マーケティング モジュール** - 注文確認ページにマーケティング モジュールを追加して、マーケティング コンテンツを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d5552-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="d5552-128">注文確認モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="d5552-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="d5552-129">新規ページに注文確認モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d5552-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d5552-130">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="d5552-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d5552-131">**テンプレート名** 下の **新規テンプレート** ダイアログ ボックスに、**注文確認テンプレート** の名称を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="d5552-132">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d5552-133">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d5552-134">**既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d5552-135">**モジュールの追加** ダイアログ ボックスで、**注文の確認** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d5552-136">**保存** を選択し、続いて **プレビュー** を選択してテンプレートをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="d5552-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="d5552-137">注文確認番号のコンテキストを必要とするため、注文確認モジュールは表示されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5552-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="d5552-138">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="d5552-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d5552-139">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="d5552-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d5552-140">**テンプレートの選択** ダイアログ ボックスで、**注文確認テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="d5552-141">**ページ名** で、**注文確認のページ** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="d5552-142">**既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d5552-143">**モジュールの追加** ダイアログ ボックスで、**注文の確認** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d5552-144">注文確認モジュールのプロパティ ウィンドウで、鉛筆の記号の横にある **見出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="d5552-145">**ヘッダー** ダイアログの **ヘッダー テキスト** フィールドで、ヘッダーテキストの **注文の確認** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5552-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="d5552-146">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="d5552-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="d5552-147">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="d5552-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5552-148">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d5552-148">Additional resources</span></span>

[<span data-ttu-id="d5552-149">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d5552-150">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d5552-151">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d5552-152">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d5552-153">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d5552-154">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d5552-155">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d5552-156">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="d5552-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]